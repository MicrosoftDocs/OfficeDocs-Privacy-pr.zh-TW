---
title: 產生報表並履行主體權力要求
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
description: 瞭解如何管理 Microsoft Priva 所建立的主體許可權要求的套件，以及如何對資料主體進行要求。
ms.openlocfilehash: a72dfb53e4f642cd2c567896c854af2beaedd416
ms.sourcegitcommit: beeb693075ef692e95d679f366301df8517b2ac3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2022
ms.locfileid: "63765516"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>產生報表並履行主體權力要求

完成 Microsoft Priva 中的主體許可權要求資料複查之後，您可以繼續執行要求。 Priva 將會建立報告，並收集在資料審查程式期間標示為 **包含** 的檔案。 這些資料套件中所選的檔案，可提交給您的資料主體，以完成其要求。 Priva 也支援利用 Microsoft 365 的主體權力要求 API，以引入自動化功能。

## <a name="understanding-reports"></a>瞭解報表

在主體權利要求的「**複查資料**」階段中選取 [**完成複查**] 之後，就會自動開始產生要求的最終報告。 在 [主體權利要求詳細資料] 頁面的 [ **報告** ] 索引標籤上，[ **狀態** ] 欄會指出何時 **進行** 報表產生，以及當報告 **可供下載**。 最多可能需要30分鐘才能完成建立報告。

報告分為兩個區段：
1. **資料主體的報告**：這些報告包含的資訊可在要求履行時傳回給資料主體。 您可以在此找到包含檔案的 **資料包** ，供您傳送給資料主體。
   > [!IMPORTANT]
   > 只有在資料評審過程中將專案標示為 **包含** 專案時，才會產生資料封裝。

   > [!IMPORTANT]
   > 只會針對 **出口** 和 **Access** 類型的要求產生資料封裝。 不會為後續要求的 **標記清單** 產生資料封裝。 查看 [主體權力要求類型](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard)的詳細資料。

2. **內部使用的報告**：這些報告適用于您組織的與主體權利要求相關的內部記錄。 它們包括一個審核記錄，以及您在資料檢查期間對標籤所套用之所有檔案的清單，以進行後續動作或進行進一步的動作。

> [!NOTE]
> 當報告產生時，組織會以安全的方式將適當的報告傳送給資料主體，以履行主體權力要求，以完成要求。 如果資料主體已要求刪除其資料，則組織負責識別待刪除的專案，並執行刪除。

## <a name="data-package"></a>資料套件

主體權利要求資料封裝包含的專案會標示為 **包含** 在處理常式的資料審查階段期間。 資料包會產生為 zip 檔案。 準備好下載時，請在 [主體權利要求詳細資料] 頁面的 [ **報告** ] 索引標籤上，選取報告的列。 隨即會以按鈕來開啟彈出面板，以 **下載** 報表。 飛入面板上的 [執行 **後續動作]** ，可提供如何使用內容的快速參考。

當您準備好下載資料套件時，請選取 [ **下載**]，尋找您的下載，然後開啟下載的 zip 檔案。

### <a name="contents-of-the-data-package"></a>資料套件的內容

資料包 zip 檔案包含下列專案：

- 名為 **Azure** 的資料夾：此資料夾包含資料主體的重要材料。 請參閱下列詳細說明。
- **Azure** 資料夾以外的檔案：這些檔案可能包含兩個名為 **Results** 的試算表，以及 **摘要**。 Azure 資料夾以外的這些檔案提供供參考，且應該主要由組織的管理員使用。

當 Priva 識別及取得主體權利要求的檔案時，它在此程式中匯出的檔案會使用唯一識別碼重新命名，以協助保護個人資料。 您可以使用 **Export_load_file.csv** 檔案，以原始的檔案名來交叉參照唯一的名稱。 由於原始檔案名可能包含機密資訊，因此應該遵循適用于這類資訊的原則。

> [!NOTE]
> 建議您仔細查看此資料夾的內容，並將所需的檔案只提交至您的資料主體。 您應該評估您的回應，以確保其符合適用法律的需求。

### <a name="azure-folder-contents"></a>Azure 資料夾內容

開啟 **Azure** 資料夾，然後開啟 **AEDExport.zip** 檔案，該檔案包含另一個副檔名為由數位和字母組成的資料夾。 開啟具有長名稱的資料夾，以顯示如下所述的內容：

- **Extracted_text_files** 資料夾：包含從原生檔案解壓縮的文字 (（支援) ）。
- **NativeFiles** 資料夾：包含以原生檔案格式包含在資料審閱 **時所標示** 的所有專案。 會為此資料夾中的每個專案指定唯一的檔案名，以保護個人資料。 您可以使用 Export_load_file.csv 檔案，以與其原始的檔案名相互交叉參照，如下所述。
  - 在資料審閱過程中使用 [ **批註** ] 功能 redacted 的檔案位於 **NativeFiles** 資料夾中，且具有尾碼 "_burn.pdf"。
- **Export_load_file.csv** 檔案：包含原始的檔案名，所以您可以使用 NativeFiles 資料夾中提供的唯一檔案名，對這些檔案名進行互交。
- **摘要** 文字檔：提供資料封裝中的檔案類型、檔案數目及其大小的摘要。

##### <a name="what-to-do-with-the-folder-contents"></a>使用資料夾內容做什麼

如以上所述，開啟 **Azure** 資料夾和 zip 檔案。 下一個工作是複查專案、決定要傳送至資料主旨的內容，以及視需要修改 zip 檔案內容。

例如，如果匯出要求的資料主體想要接收所有包含其個人資料之專案的副本，您會想要仔細查看 **NativeFiles** 資料夾中的專案，並移除您不想傳送回資料主體的任何專案。

若為存取要求，當資料主體想要接收組織所持有之所有個人資訊的摘要時，您會想要將重點放在 **摘要** 文字檔上。

修改 zip 檔案，以移除您不想要包含在最終套件中的任何內容。 完成後，以安全方式將 zip 檔案傳送給進行主體許可權要求的資料主體。

## <a name="audit-log"></a>審核記錄

「審核記錄檔」是 CSV 檔，提供每個主體權力要求之階段的進展記錄。 它會列出處理常式的每個階段，以及完成該步驟的個人的日期和時間，以及其使用者名稱。

## <a name="tagged-files-reports"></a>標記檔報告

標示為 [檔案標示 **為 ...** ] 的報表是 CSV 檔案，列出在資料審閱過程中所套用標記的內容專案。 標記是用來標示內容專案，以供組織進行進一步的關注或動作。 深入瞭解 [標記的設定](priva-settings.md#data-review-tags)。

## <a name="retention-periods-for-reports-and-data"></a>報表和資料的保留期間

由主體權利要求和相關聯的資料所產生的報告（例如，在 Azure 中儲存的批註檔案）會儲存指定的時間長度。 預設的保留期間是從關閉主體許可權要求之日期起的30天。

資料保留期間是在 Priva **設定** 中定義，並套用至所有主體權力要求。 若要查看或變更您的資料保留期間，請遵循下列步驟：

1. 在 Priva 主體許可權要求的任何地方，**設定** 選取螢幕右上角) 的齒輪圖示 (。
2. 選取左側導覽的 **資料保留期間** 。
3. 從 [ **收集的資料與報告** ] 下拉式清單功能表中，選取 [30 天] 或 [90 天] 作為保留期間。
4. 選取 [ **儲存** ] 以儲存您的設定。

請務必確認您所選擇的資料保留期間符合組織的原則和法律義務。

## <a name="integrate-with-partner-solutions"></a>與合作夥伴解決方案整合

您可以利用 Microsoft 365 的主體許可權要求 API，將 Priva 主體權利要求解決方案與現有的商務程式和工具整合。 這為您提供您的主旨權利策略的簡單而又強大的方式。

當資料主體要求組織中的資訊時，您可以利用 APIs，根據該要求的自訂準則，在 Microsoft 365 中建立這些要求。 您可以在 Microsoft 365 中建立主體權利要求、追蹤要求的進度，並在要求完成處理且內容已準備好可供檢索時加以確認。 我們的 APIs 可供任何人使用，讓其解決方案更具可擴充性：無論是針對 isv、合作夥伴，還是要用於其解決方案中的 Microsoft 365，或是組織使用其業務線應用程式。

若要深入瞭解，請參閱[使用 Microsoft Graph 主體權力要求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
