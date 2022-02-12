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
ms.openlocfilehash: 9931422434414146601ede959af910caf1befcc1
ms.sourcegitcommit: 1f3f2757f456628ec904bc3df985b00ffba8f892
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2022
ms.locfileid: "62542831"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>產生報表並履行主體權力要求

在 Microsoft Priva 中完成主題許可權要求的資料複查之後，您可以繼續進行要求的履行。 Priva 將會建立報告，並收集標記為 **包含** 在資料審查程式中的檔案。 這些資料套件中所選的檔案，可提交給您的資料主體，以完成其要求。 Priva 也支援利用 Microsoft 365 的主體權力要求 API，以引入自動化功能。

## <a name="prepare-final-reports-for-the-data-subject"></a>準備資料主體的最終報表

主體權力要求資料包會產生為 zip 檔案。 最多可能需要30分鐘才能產生此套件。 做好準備後，請從 [主體權利要求] 頁面開啟您的主體權力要求，開啟 [ **報告** ] 索引標籤，尋找您的下載，然後開啟 zip 檔案。

資料包包含一分類的檔。 Azure 資料夾以外的檔案提供參考，且應該主要由系統管理員使用。 資料主體的重要材料會包含在 **Azure** 資料夾中。

建議您仔細查看此資料夾的內容，並將所需的檔案只提交至您的資料主體。 您應該評估您的回應，以確保其符合適用法律的需求。

### <a name="azure-folder-contents"></a>Azure 資料夾內容

開啟此資料夾，然後開啟 **AEDExport.zip** 檔案。 內容包括：

- **Extracted_text_files** 資料夾包含從原生檔案解壓縮的文字 (（支援) ）。
- **NativeFiles** 資料夾包含以原生檔 **格式包含的所有專案。**
- Redacted 檔案位於 **NativeFiles** 資料夾中，且其後綴為 "_burn.pdf"。
- 匯出的檔案會使用唯一識別碼重新命名，以協助保護個人資料。 您可以使用 **Export_load_file.csv**，以原始的檔案名來交叉參照唯一的名稱。 由於原始檔案名可能包含機密資訊，因此應該遵循適用于這類資訊的原則。

檢查您的 zip 檔案內容之後，視需要加以修改，以移除您不想要包含在最終套件中的任何內容。 完成後，請將其安全地傳送至您的資料主體。

## <a name="integrate-with-partner-solutions"></a>與合作夥伴解決方案整合

您可以利用 Microsoft 365 的主體許可權要求 API，將 Priva 主體權利要求解決方案與現有的商務程式和工具整合。 這為您提供您的主旨權利策略的簡單而又強大的方式。

當資料主體要求組織中的資訊時，您可以利用 APIs，根據該要求的自訂準則，在 Microsoft 365 中建立這些要求。 您可以在 Microsoft 365 中建立主體權利要求、追蹤要求的進度，並在要求完成處理且內容已準備好可供檢索時加以確認。 我們的 APIs 可供任何人使用，讓其解決方案更具可擴充性：無論是針對 isv、合作夥伴，還是要用於其解決方案中的 Microsoft 365，或是組織使用其業務線應用程式。

若要深入瞭解，請參閱[使用 Microsoft Graph 主體權力要求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>管理資料保留

透過此工具及相關資料（如儲存在 Azure 的批註檔案）所產生的報告會儲存指定的時間長度。 資料保留期間是在 Priva **設定** 中定義，而且會套用到所有主體許可權要求。 若要查看或變更您的資料保留期間，請遵循下列步驟：

1. 在 Priva 主體許可權要求的任何地方，**設定** 選取螢幕右上角) 的齒輪圖示 (。
2. 選取左側導覽的 **資料保留期間** 。
3. 使用下拉式功能表選取 [30 天] 或 [90 天] 作為保留期間。

請務必確認您所選擇的資料保留期間符合組織的原則和法律義務。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
