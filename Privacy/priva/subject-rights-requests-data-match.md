---
title: 主體許可權要求的資料比對
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: 瞭解如何將資料主體的其他資訊上傳至 Microsoft Priva。
ms.openlocfilehash: 90ee0e8e21d25954c11113992cbb7ece847c85ab
ms.sourcegitcommit: 6b88d22d0250cbb9a4ba1f71665f29cb67939851
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2022
ms.locfileid: "65059737"
---
# <a name="data-matching-for-subject-rights-requests"></a>主體許可權要求的資料比對

透過資料比對，組織可以讓 Microsoft Priva 根據確切提供的資料值來識別資料主體。 這有助於提高尋找資料主體內容的精確度，這些內容對應于內部人員和與您互動之外部使用者的資料值。 它也簡化了在主體許可權要求建立期間手動提供欄位的需求，並提供主體許可權要求和 [概觀] 圖格中的內容，以展示具有最多資料主體內容的專案。 若要深入瞭解該檢視，請 [參閱在 Priva 中尋找個人資料並將其視覺化](priva-data-profile.md#items-with-the-most-data-subject-content)。

若要使用資料比對功能，您必須是隱私權管理角色群組的成員。 從 [Microsoft Purview 合規性](https://compliance.microsoft.com/)入口網站的 Priva 內，選取頂端導 **覽中的 [設定**]，然後選取 **[資料比對]**。 從這裡開始，您必須定義個人資料架構，並提供個人資料上傳，如下所示。 請注意，您可以新增專案，而且可以刪除新增的專案，但無法修改專案。

## <a name="prepare-for-data-import"></a>準備資料匯入

在定義架構或上傳資料之前，您必須識別資料主體資訊的來源。 所需的檔案格式.csv，可由應用程式讀取，例如Microsoft Excel。 將此匯出結構化，讓您的資料行標頭出現在第一個資料列中。 這些標頭應該包含您個人資料架構的屬性名稱。 檢查每個欄位中的資料格式。 如果任何資料包含逗號，請以雙引號括住這些值，以確保不會剖析成個別的欄位。

## <a name="define-the-personal-data-schema"></a>定義個人資料架構

設定資料比對的第一個步驟是定義個人資料架構，以描述資料主體的屬性。 您將在資料比對設定區域的第一個索引標籤上傳此架構。 必要的檔案包括 **個人資料架構** XML 檔案和 **規則套** 件 XML 檔案。

### <a name="personal-data-schema-xml"></a>個人資料架構 XML

個人資料架構檔案是 XML 檔案，可定義預期的資料行名稱。

- 將此架構檔案 *命名為pdm.xml*。
- 使用功能變數名稱標籤定義每個資料行名稱，如下列範例所示。
- 針對您想要搜尋的欄位使用可搜尋 = 「true」，最多五個欄位。 您至少必須要搜尋其中一個功能變數名稱。 範例語法： `\<Field name="" searchable=""/>` 。
- 個人資料架構具有 DataStore 標記區段。 四個必要欄位必須對應至您的功能變數名稱：primaryKeyField、upnField、firstNameField、lastNameField。

例如，下列 XML 檔案會定義範例架構，其中五個欄位指定為可搜尋：PatientID、MRN、SSN、電話 和 DOB。 primaryKeyField 會對應至 PatientID、upnField 會對應至 MRN、firstNameField 會對應至 FirstName，而 lastNameField 會對應至 LastName。

您可以複製、修改及使用我們的範例。

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>規則套件 XML

當您設定規則套件時，請務必正確參考上面建立的個人資料架構檔案：pdm.xml。 在下列範例規則套件 XML 中，必須自訂下欄欄位，才能建立您的資料比對敏感性類型：

- **RulePack 識別碼**  & **PrivacyMatch 識別碼**：使用 New-GUID 來產生 GUID。
- **資料存放區**：此欄位會指定要使用的個人資料比對查閱資料存放區。 提供已設定個人資料架構的已定義 DataStore 名稱。
- **idMatch**：此欄位指向個人資料相符的主要元素。
  - **相符項目**：指定要在精確查閱中使用的欄位。 從個人資料架構提供可搜尋的功能變數名稱。
  - **分類**：此欄位會指定觸發個人資料比對查閱的敏感性類型比對。 您可以提供現有內建或自訂敏感性資訊類型的名稱或 GUID。 為了避免造成效能問題，如果您在個人資料比對中使用自訂敏感性資訊類型作為分類元素，請勿使用符合大量內容百分比的自訂敏感性資訊類型 (例如「任何數位」或「任何五個字母的字」) 。 建議您新增支援的關鍵字，或在自訂分類敏感性資訊類型的定義中包含格式設定。
- **相符項目**：此欄位會指向 idMatch 鄰近位置的其他辨識項。
  - **相符** 專案：在 DataStore 的個人資料架構中提供任何功能變數名稱。
- **資源**：本節會在多個地區設定中指定敏感性類型的名稱和描述。
  - **idRef**：提供 ExactMatch 識別碼的 GUID。
  - **名稱&描述**：視需要自訂。

在下列規則套件 XML 範例中，我們會參考上一個步驟中建立個人資料架構 XML 的pdm.xml範例檔案：

- **資料存放區：dataStore** 名稱會參考我們稍早建立的架構檔案：dataStore = 「PatientRecords」。
- **idMatch**：idMatch 值會參考我們稍早建立的pdm.xml檔案中所列的可搜尋欄位：idMatch 符合 = 「SSN」。
  - **分類**：分類值會參考現有或自訂敏感性資訊類型：分類 = 「美國社會安全號碼 (SSN) 」。 (在此案例中，我們使用美國社會安全號碼作為現有的敏感性資訊類型)。

使用 Unicode 編碼) 建立 XML 格式 (規則套件，如下列範例程式碼所示。 您可以複製、修改及使用此範例。

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="sensitive-info-types"></a>敏感性資訊類型

設定資料比對的第二個步驟是建立個人資料比對的唯一敏感性資訊類型 (PDM) 。 [ (SIT) 的敏感性資訊類型 ](/microsoft-365/compliance/sensitive-information-type-learn-about)是模式型分類器，可偵測社會安全或信用卡號碼等敏感性資訊。 設定 PDM 敏感性資訊類型可讓您使用確切的資料值，而不是一般值來偵測相符專案。 若要開始此步驟，請選 **取 [建立 PDM 敏感性資訊類型** ] 以開始建立精靈。

## <a name="upload-personal-data"></a>Upload個人資料

定義個人資料架構和敏感性資訊類型之後，第三個步驟是上傳個人資料。 移至 [ **個人資料上傳] 索引卷** 標，選取 [ **新增**]，然後選擇您在第一個步驟中定義的個人架構，然後上傳包含個人資料的檔案。

您可以選擇本機檔案，或將 SAS URL 提供給包含您個人資料檔案的現有Microsoft Azure 儲存體位置，來上傳此個人資料。
如果您將檔案備妥為此程式中符合所建立架構的第一個步驟，您可以使用該檔案進行上傳。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
