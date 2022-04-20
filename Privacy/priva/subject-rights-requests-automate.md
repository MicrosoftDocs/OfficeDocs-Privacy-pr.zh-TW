---
title: '自動化主體許可權要求中的工作 '
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
description: 瞭解如何使用 Microsoft Power Automate，協助您將 Priva 中主體許可權要求的基本工作自動化。
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930494"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>自動化主體許可權要求中的工作 

Microsoft Power Automate是一項工作流程服務，可將應用程式和服務之間的動作自動化。 當您為 Microsoft Priva Subject Rights Requests 啟用Power Automate流程時，您可以自動化案例和使用者的重要工作，例如在 ServiceNow 中建立票證，或新增到期日相關行事曆提醒。 若要深入瞭解Power Automate，請造訪其[檔網站](/power-automate/getting-started)。

具有主體許可權要求訂用帳戶的客戶不需要另一個Power Automate授權，即可使用 Priva 的建議Power Automate範本。 這些範本可以自訂以支援您的組織，並涵蓋核心主體權利要求案例。 如果您選擇在這些範本中使用進階Power Automate功能、使用Microsoft 365合規性連接器建立自訂範本，或針對Microsoft 365中的其他合規性區域使用Power Automate範本，您可能需要更多Power Automate授權。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>從範本建立新的Power Automate流程

1. 在 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)中，移至導覽的 [Priva] 區段，然後選取 **[Priva Subject Rights Requests]**。
1. 從清單中開啟您想要使用的主體許可權要求，然後選取 [**自動化**]，然後選取 [**管理Power Automate流程]**。 這會開啟 [流程] 飛出視窗窗格。
1. 使用 **[新增]** 選項，然後從可用的選項中選擇您想要使用的範本。 從這裡，依照精靈中的提示完成設定。 選項會根據您的範本類型而有所不同。

儲存範本的實例之後，您必須從主體許可權要求的詳細資料頁面執行它，以便流程實例具有正確的內容和識別碼。 開啟要求，返回 **[自動化]** 功能表，選取範本，然後選取 [ **執行流程]**。 您可以選取 [ **查看流程執行活動**]，以查看您過去的活動。

### <a name="power-automate-templates-in-priva"></a>在 Priva 中Power Automate範本

- **在 ServiceNow 中建立隱私權管理案例的記錄**：此範本適用于想要使用其 ServiceNow 解決方案來追蹤主體許可權要求案例的組織。 系統會要求您輸入 ServiceNow 實例詳細資料，包括連線到 ServiceNow 的帳戶。 此帳戶必須能夠在 ServiceNow 中建立事件，並填入事件詳細資料。 連線到您的實例之後，主體許可權要求系統管理員將能夠在 ServiceNow 中建立案例的記錄，而且如有需要，可以自訂範本將填入選取欄位的內容。 如需連接器的詳細資訊，請參閱 [ServiceNow 連接器參考頁面](/connectors/service-now/)。
- **建立行事曆提醒**：此範本用於在您的Outlook行事曆中設定主體許可權要求的到期日提醒。 此工具會從要求的屬性中為您填入特定詳細資料，例如要求的名稱及其到期日。 您可以新增描述性詳細資料、指定收件者，以及調整其他進階設定。
- **依標籤取得主旨許可權要求的檔案**：此範本可讓您搜尋已提供特定標籤之主體許可權要求的檔案。 您可以編輯流程以執行自訂動作，或檢視要用於內部程式或工具的傳回檔案清單。

## <a name="share-a-power-automate-flow"></a>共用Power Automate流程

藉由共用Power Automate流程，您可以新增另一個擁有者，並允許他們編輯、更新和刪除流程。 所有擁有者也可以存取執行歷程記錄，並新增或移除其他擁有者。 若要共用流程，請開啟您要使用的主體許可權要求，選取 [**自動化**]，然後選取 [**管理Power Automate流程]**。 您可以從此窗格選取現有的流程，然後使用 [共用] 選項來新增使用者或群組。

此窗格也可讓您選擇管理Power Automate流程中所使用之服務的內嵌連線。 變更這些設定可能會影響您執行流程的能力。

## <a name="edit-or-delete-power-automate-flow"></a>編輯或刪除Power Automate流程

若要調整Power Automate流程的詳細資料，請開啟主體許可權要求，選取 [**自動化**]，然後選 **取 [管理Power Automate流程]**。 在此窗格中，您可以選取現有的流程來檢視詳細資料。 在任何區段中使用 [編輯] 來變更屬性，然後儲存。

若要完全移除流程，請使用 **[刪除** ] 選項。 它會移除所有擁有者流程，並針對所有使用者卸載流程。 先前的流程實例會繼續執行，以避免資料遺失。 您可以在刪除完成之前確認您的選擇。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
