---
title: 主體權力要求的資料符合
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
description: 瞭解如何將其他資訊上傳至 Priva 資料主體的 Microsoft。
ms.openlocfilehash: 1339962a1c4dba18a1d0b21d8a2cebb17ad0f91a
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248927"
---
# <a name="data-matching-for-subject-rights-requests"></a>主體權力要求的資料符合

透過資料比對，組織可以讓 Microsoft Priva 根據正確提供的資料值來識別資料主體。 這有助於提高針對內部人員和您與您互動的外部使用者，尋找與這些資料值相對應的資料主體內容的準確性。 此外，它也可簡化在建立主體許可權時手動提供欄位的需求，並提供主題許可權要求中的內容，以及顯示最具資料主體內容之專案的總覽磚。 若要深入瞭解該視圖，請參閱 [在 Priva 中尋找及顯示個人資料](priva-data-profile.md#items-with-the-most-data-subject-content)。

若要使用資料符合功能，您必須是隱私權管理角色群組的成員。 在 [Microsoft 365 合規性中心](https://compliance.microsoft.com/)的 [Priva] 中，選取上方導覽中的 [**設定**]，然後選取 [**資料** 比對]。 在這裡，您將需要定義個人資料架構，並提供個人資料上傳，如下所示。 請注意，您可以新增專案，也可以刪除透過 UI 新增的專案。 不過，您此時無法從 UI 修改專案。

## <a name="prepare-for-data-import"></a>準備資料匯入

在定義架構或上傳資料之前，您需要識別資料主體資訊的來源。 必要的檔案格式為 .csv，可由諸如 Microsoft Excel 等應用程式讀取。 結構此匯出，使欄標題出現在第一列。 這些標題應包含您個人資料架構的屬性名稱。 檢查每個欄位中的資料格式。 如果有任何資料包含逗號，請使用雙引號括住這些值，以確保不會將它剖析成不同的欄位。

## <a name="define-the-personal-data-schema"></a>定義個人資料架構

個人資料架構會說明資料主體的屬性。 在 [資料對應設定] 區域的第一個索引標籤上 Upload 此架構。 必要檔案包含 **個人資料架構** xml 檔和 **規則套件** xml 檔案。

### <a name="personal-data-schema-xml"></a>個人資料架構 XML

個人資料架構檔案是一個 XML 檔，可定義預期的欄名稱。

- 將此架構檔案命名為 *pdm.xml*。
- 使用下列範例所示的功能變數名稱標記，定義每個欄名稱。
- 可搜尋 = "true" 為您想要搜尋的欄位，最多可以有五個欄位。 您必須至少有一個功能變數名稱可供搜尋。 範例語法： `\<Field name="" searchable=""/>` 。
- 個人資料架構具有「資料存儲」標記區段。 必須將四個強制欄位對應至您的功能變數名稱： primaryKeyField、upnField、firstNameField、lastNameField。

舉例來說，下列 XML 檔案會定義一個範例架構，其中有五個指定為可搜尋的欄位： PatientID、MRN、SSN、電話及 DOB。 PrimaryKeyField 會對應至 PatientID，upnField 會對應至 MRN，firstNameField 會對應至 FirstName，而 lastNameField 會對應至 LastName。

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

當您設定規則套件時，請務必正確參考上述建立的個人資料架構檔案： pdm.xml。 在下列範例規則套件 XML 中，必須自訂下欄欄位，以建立資料符合機密類型：

- **RulePack 識別碼**  & **PrivacyMatch 識別碼**：使用新的 guid 來產生 GUID。
- **資料** 儲存：此欄位會指定要使用的個人資料相符的查閱資料存放區。 為已設定的個人資料架構提供已定義的資料存儲名稱。
- **idMatch**：此欄位指向 [個人資料相符] 的主要元素。
  - **相符項目**：指定要在精確查閱中使用的欄位。 提供個人資料架構的可搜尋功能變數名稱。
  - **分類**：此欄位指定觸發個人資料相符的敏感類型相符專案。 您可以提供現有內建或自訂敏感性資訊類型的名稱或 GUID。 為了避免出現效能問題，如果您使用自訂的機密資訊類型做為個人資料符合中的分類元素，請勿使用會符合大量內容 (的自訂敏感資訊類型，例如 "任何數位" 或 "任何五個字母的字" ) 。 建議您新增支援關鍵字，或在自訂分類機密資訊類型的定義中包含格式設定。
- **相符項目**：此欄位會指向 idMatch 鄰近位置的其他辨識項。
  - **相符**：在資料存儲的個人資料架構中提供任何功能變數名稱。
- **Resource**：此區段會在多個地區設定中指定敏感類型的名稱和描述。
  - **idRef**：提供 ExactMatch 識別碼的 GUID。
  - **名稱 & 描述**：按需自訂。

在下列的規則套件 XML 範例中，我們會參考上一個步驟中建立個人資料架構 XML 的 pdm.xml 範例檔案：

- **資料** 檔：資料檔案名稱參考我們先前建立的架構檔案：資料檔案 = "PatientRecords"。
- **idMatch**： idMatch 值會參照先前建立的 pdm.xml 檔案中所列出的可搜尋欄位： idMatch 相符 = "SSN"。
  - **分類**：分類值參考現有或自訂的機密資訊類型：分類 = "U.S. Social Security NUMBER (SSN) "。 (在此案例中，我們使用美國社會安全號碼作為現有的敏感性資訊類型)。

以 Unicode 編碼) 以 XML 格式 (建立規則套件，如下列程式碼範例所示。 您可以複製、修改及使用此範例。

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

## <a name="upload-personal-data"></a>Upload 個人資料
在定義個人資料架構之後，您可以在 [資料比對設定] 頁面的第二個索引標籤上執行 [ **個人資料上傳** ]。 當您選取 [ **新增**] 時，請選擇您在第一個步驟中定義的個人架構，然後上傳包含個人資料的檔。

您可以選擇本機檔，或提供 SAS URL 至包含您個人資料檔的現有 Microsoft Azure 儲存體位置，以上傳此個人資料。
如果您已在此程式中，將檔案當做符合建立之架構的第一個步驟，您可以使用該檔案進行上傳。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
