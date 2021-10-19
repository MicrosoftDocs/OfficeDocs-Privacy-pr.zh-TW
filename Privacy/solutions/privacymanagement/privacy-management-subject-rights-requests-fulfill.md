---
title: 管理主體權力要求報告並在隱私權管理中完成要求
f1.keywords:
- CSH
ms.author: v-jgriffee
author: jmgriffee
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-privacy-management
search.appverid:
- MOE150
- MET150
description: 瞭解如何管理隱私權管理所建立的資料檔案套件，以進行主體權利要求，以及如何對資料主體進行要求。
ms.openlocfilehash: 424bb4edc6ddcab86200d76cee767bc9699b281a
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478129"
---
# <a name="manage-subject-rights-requests-reports-and-fulfill-requests"></a>管理主體權力要求報告及完成要求

在您完成主體權利要求的資料複查之後，您可以繼續要求履行。 隱私權管理會建立報告，並收集標記為在資料審查程式期間 **包含** 的檔案。 這些資料套件中所選的檔案，可提交給您的資料主體，以完成其要求。 隱私權管理還支援利用 Microsoft 365 的主體權力要求 API，以引入自動化功能。

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

您可以利用 Microsoft 365 的主體權力要求 API，將 Microsoft 365 主旨權利要求模組與現有的商務程式及工具整合。 這為您提供您的主旨權利策略的簡單而又強大的方式。

當資料主體要求組織中的資訊時，您可以利用 APIs，根據該要求的自訂準則，在 Microsoft 365 中建立這些要求。 您可以在 Microsoft 365 中建立主體權利要求、追蹤要求的進度，並在要求完成處理且內容已準備好可供檢索時加以確認。 我們的 APIs 可供任何人使用，讓其解決方案更具可擴充性：無論是針對 isv、合作夥伴，還是要用於其解決方案中的 Microsoft 365，或是組織使用其業務線應用程式。

若要深入瞭解，請參閱[使用 Microsoft Graph 主體權力要求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>管理資料保留

透過此工具及相關資料（如儲存在 Azure 的批註檔案）所產生的報告會儲存指定的時間長度。 這段期間是透過「**資料保留期間**」區段中 **設定**，在全域層級定義，可讓您選擇30到90天。 請確認這些資料保留期間符合您的原則和法律義務。

## <a name="legal-disclaimer"></a>法律免責聲明

[隱私權管理法律免責聲明](privacy-management-disclaimer.md)
