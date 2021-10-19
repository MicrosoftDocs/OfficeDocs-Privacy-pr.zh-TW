---
title: 自動化主體許可權要求隱私權管理中的工作
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
description: 瞭解如何使用 Microsoft Power Automate 協助您自動化隱私權管理中的主體權力要求的必要工作。
ms.openlocfilehash: df76e87e3298b2ccc6c897d485e695d0f1ae35c9
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478125"
---
# <a name="automate-subject-rights-requests-tasks"></a>自動要求任務的主體權力

Microsoft Power Automate 是一種工作流程服務，可在應用程式和服務間自動執行動作。 當您為 Microsoft 365 啟用隱私權管理的 Power Automate 流程時，您可以自動執行案例和使用者的重要工作，例如在 ServiceNow 中建立入場券，或新增到期日的行事曆提醒。 若要深入瞭解 Power Automate，請流覽其[檔網站](/power-automate/getting-started)。

使用包含隱私權管理的 Microsoft 365 訂閱的客戶不需要另一個 Power Automate 授權，即可使用建議的隱私權管理 Power Automate 範本。 您可以自訂這些範本，以支援您的組織及涵蓋核心隱私權管理案例。 如果您選擇在這些範本中使用特優 Power Automate 功能，請使用 Microsoft 365 規範連接器建立自訂範本，或在 Microsoft 365 中使用其他規範區域的 Power Automate 範本，您可能需要更多 Power Automate 授權。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>從範本建立新的 Power Automate 流程

1. 在 [Microsoft 365 合規性中心](https://compliance.microsoft.com/)中，移至導覽的 [隱私權管理] 區段，然後選取 [**主體權力要求**]。
1. 從清單中開啟您想要使用的主體權力要求，然後選取 [**自動**]，然後 **管理 Power Automate 流程**。 這會開啟 [資料流程] 飛彈出窗格。
1. 使用 [ **新增** ] 選項，然後從可用的選項中選擇您要使用的範本。 從這裡，依照嚮導中的提示完成安裝程式。 選項會隨著範本類型而異。

在儲存範本的實例之後，您必須從主體權利要求的詳細資料頁面執行它，使流程實例具有正確的內容和識別碼。 開啟要求，回到 [ **自動化** ] 功能表中，選取範本，然後選取 [ **執行流程**]。 您可以選取 [ **查看流程執行活動**]，以查看過去的活動。

### <a name="power-automate-templates-in-privacy-management"></a>在隱私權管理中 Power Automate 範本

- **在 ServiceNow 中建立隱私權管理案例的記錄**：此範本適用于想要使用其 ServiceNow 解決方案追蹤主體權力要求案例的組織。 系統會要求您輸入您的 ServiceNow 實例詳細資料（包含帳戶）以連接至 ServiceNow。 此帳戶必須能夠在 ServiceNow 中建立事件，並填入事件詳細資料。 連線至您的實例之後，系統管理員就可以在 ServiceNow 中為案例建立記錄，如果需要，可以自訂範本將填入至選取的欄位。 如需連接器的詳細資訊，請參閱 [ServiceNow connector reference] 頁面](/connectors/service-now/)。
- **建立行事曆提醒**：此範本是用於設定 Outlook 行事曆中的主體許可權要求的到期日期提醒。 該工具會為您從要求的屬性填入特定詳細資料，例如要求的名稱及其到期日。 您可以新增描述性詳細資料、指定收件者，以及調整其他的高級設定。
- **以標記方式取得主體權利要求** 的檔案：此範本可讓您搜尋提供特定標記的主體許可權要求檔案。 您可以編輯流程以執行自訂動作，或查看傳回檔案的清單，以供內部程式或工具利用。

## <a name="share-a-power-automate-flow"></a>共用 Power Automate 流程

透過分享 Power Automate 流程，您可以新增另一個擁有者，並允許他們編輯、更新和刪除流程。 所有擁有者也可以存取「執行歷程記錄」，並新增或移除其他擁有者。 若要共用流程，請開啟您要使用的主體權力要求，選取 [**自動**]，然後選取 [**管理 Power Automate 流程**]。 您可以從這個窗格選取現有的流程，然後使用 [共用] 選項新增使用者或群組。

此窗格也可讓您選擇管理內嵌連線至 Power Automate 流程中所使用的服務。 變更這些設定可能會影響您執行流程的能力。

## <a name="edit-or-delete-power-automate-flow"></a>編輯或刪除 Power Automate 流程

若要調整 Power Automate 流程的詳細資料，請開啟主體權利要求，選取 [**自動**]，然後選取 [**管理 Power Automate 流程**]。 您可以從這個窗格選取現有流程以查看詳細資料。 使用任何區段中的 Edit 若要變更屬性，請使用 [儲存]。

若要徹底移除流程，請使用 [ **刪除** ] 選項。 它會移除所有擁有者的流程，並將其卸載給所有使用者。 先前的流程實例將繼續執行，以避免資料遺失。 您可以先確認您的選擇，最後再刪除。

## <a name="legal-disclaimer"></a>法律免責聲明

[隱私權管理法律免責聲明](privacy-management-disclaimer.md)
