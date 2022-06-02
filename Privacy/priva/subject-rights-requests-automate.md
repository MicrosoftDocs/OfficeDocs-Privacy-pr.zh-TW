---
title: 與 Microsoft 圖形 API 和 Power Automate 整合
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
description: 瞭解如何藉由與 Microsoft 圖形 API 和 Power Automate 整合來擴充Priva 主體權利要求功能。
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851638"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>透過 Microsoft 圖形 API 與 Power Automate 整合和擴充

您可以使用 Microsoft Graph 主體權利要求 API，將Priva 主體權利要求與現有的商務程式和工具整合。 您也可以針對設定行事曆提醒和在 ServiceNow 中建立案例等工作，使用內建的Power Automate流程來擴充主體許可權要求的自動化功能。

## <a name="microsoft-graph-subject-rights-requests-api"></a>Microsoft Graph主體權利要求 API

Microsoft 365主體權利要求 API 提供簡單但強大的方法，讓您將自動化引入現有的主體權限原則。 當個人向您的組織要求資訊時，我們的 API 可讓您根據該要求的準則，在Microsoft 365內建立這些要求。 您可以在Microsoft 365中建立主體許可權要求、追蹤其進度，以及確認要求何時完成處理，且內容已準備好擷取。

我們的 API 可供任何人用來使其解決方案更具擴充性，例如 ISV、想要在其解決方案中容納Microsoft 365的合作夥伴，以及想要搭配其企業營運應用程式使用 API 的組織。

檢視使用[Microsoft Graph主體許可權要求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)的完整檔。

## <a name="power-automate-templates-for-subject-rights-requests"></a>Power Automate主體許可權要求的範本

Microsoft Power Automate是一項工作流程服務，可將應用程式和服務之間的動作自動化。 主體許可權要求包含內建的Power Automate範本，可協助使用者管理主體許可權要求。 使用者可以設定流程的自動化流程，例如在 ServiceNow 中建立票證，以及新增到期日相關行事曆提醒。 若要深入瞭解Power Automate，請流覽[Power Automate檔](/power-automate/getting-started)。

如果您已購買主體許可權要求訂用帳戶，則不需要個別的Power Automate授權即可使用建議的Power Automate範本。 這些範本可以自訂以支援您的組織，並涵蓋核心主體權利要求案例。 不過，您可能需要額外的授權，才能在這些範本中使用進階Power Automate功能，或建立您自己的範本。

### <a name="available-templates"></a>可用的範本

- **在 ServiceNow 中建立Priva隱私權管理案例的記錄**：此範本適用于想要使用其 ServiceNow 解決方案來追蹤主體許可權要求案例的組織。 系統會要求您輸入 ServiceNow 實例詳細資料，包括用來連線至 ServiceNow 的帳戶。 此帳戶必須能夠在 ServiceNow 中建立事件，並填入事件詳細資料。 連線到您的實例之後，主體許可權要求系統管理員將能夠在 ServiceNow 中建立案例的記錄，而且如有需要，可以自訂範本將填入選取欄位的內容。 如需連接器的詳細資訊，請參閱 [ServiceNow 連接器檔](/connectors/service-now/)。

- **新增行事曆提醒以追蹤Priva隱私權管理案例**：此範本適用于在您的Outlook行事曆中設定主體許可權要求的到期日提醒。 此工具會從要求的屬性中為您填入特定詳細資料，例如要求的名稱及其到期日。 您可以新增描述性詳細資料、指定收件者，以及調整其他進階設定。

- **依標籤取得Priva主體許可權要求的檔案**：此範本可讓您搜尋已指定特定標籤之主體許可權要求的檔案。 您可以編輯流程以執行自訂動作，或檢視要用於內部進程或工具的傳回檔案清單。

### <a name="create-a-new-power-automate-flow-from-a-template"></a>從範本建立新的Power Automate流程

1. 在 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)中，選取左側導 **覽中的 [Priva 主體權利要求**]。

2. 尋找您想要處理的主體許可權要求，並從清單中選取它，以開啟其詳細資料頁面。

3. 在右上角，選取 **[自動化]**，然後選 **取 [管理Power Automate流程**] 以開啟流程飛出視窗窗格。

4. 選取 **[新增** ]，然後從可用的選項中選擇您想要使用的範本。 從這裡，遵循提示來自訂並新增步驟，以完成流程的建置。 選項會根據您使用的範本而有所不同 (請參閱下方的範本類型) 。

5. 完成後，選取 **[儲存]**。

儲存範本的實例之後，您必須從要求的詳細資料頁面執行它，以便流程實例具有正確的內容和識別碼。 開啟要求，返回 **[自動化]** 功能表，選取範本，然後選取 [ **執行流程]**。 您可以選取 [ **查看流程執行活動**]，以查看您過去的活動。

### <a name="share-a-power-automate-flow"></a>共用Power Automate流程

共用Power Automate流程可讓您新增另一個擁有者，並允許他們編輯、更新和刪除流程。 所有擁有者都可以存取執行歷程記錄，並新增或移除其他擁有者。 

若要共用流程，請開啟您要使用的主體許可權要求，選取 [**自動化**]，然後選取 [**管理Power Automate流程]**。 您可以從此窗格選取現有的流程，然後使用 **[共用** ] 選項來新增使用者或群組。

此窗格也可讓您選擇管理Power Automate流程中所使用之服務的內嵌連線。 變更這些設定可能會影響您執行流程的能力。

### <a name="edit-or-delete-power-automate-flow"></a>編輯或刪除Power Automate流程

若要調整Power Automate流程的詳細資料，請選取要求詳細資料頁面右上角的 [**自動化**]，然後選取 [**管理Power Automate流程]**。

從 **[Power Automate流程**] 窗格中，選取您要編輯的流程，然後從命令列選取 [**編輯**] 以編輯或新增步驟。 完成時，選取 [ **儲存]**。

若要刪除流程，請從 [**Power Automate流程**] 窗格的清單中選取該流程，然後從命令列選取 [**刪除**]。 所有擁有者都會移除流程，並針對所有使用者卸載流程。 先前的流程實例會繼續執行，以避免資料遺失。 系統會要求您在刪除完成之前進行確認。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva法律免責聲明](priva-disclaimer.md)
