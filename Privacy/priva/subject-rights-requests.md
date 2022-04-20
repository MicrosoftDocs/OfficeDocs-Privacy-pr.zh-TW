---
title: 瞭解 Priva Subject Rights Requests
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
description: Microsoft Priva 中的主體權利要求解決方案可協助您尋找個人資料，並共同檢閱內容和建立報表。
ms.openlocfilehash: 37ee3fc795559d216a7a8cd620cff2c3ca689c2b
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930624"
---
# <a name="learn-about-priva-subject-rights-requests"></a>瞭解 Priva Subject Rights Requests

根據世界各地的特定隱私權法規，個人 (或 *資料主體*) 可能會要求檢閱或管理公司所收集的個人資料。 這些要求有時也稱為資料主體要求， (DSR) 、資料主體存取要求 (DSAR) 或取用者權利要求。 對於儲存大量資訊的公司而言，尋找相關資料可能是一項相當龐大的工作。

Microsoft Priva 可協助您透過主體權利要求解決方案來處理這些查詢。 它提供工作流程、自動化和共同作業功能，可協助您搜尋主體資料、檢閱結果、收集適當的檔案，以及產生報告。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva 如何支援主體權利要求履行

主體許可權要求週期從個人對組織的要求開始。 收到後，您可以使用 Priva 的功能來收集該資料、共同作業、檢閱及建立報告。 然後，您可以通知資料主體您的結果，並採取 Priva 外部所需的任何其他動作來完成要求，例如刪除資料。 為了協助管理和自動化您的工作流程，您也可以使用整合式Power Automate範本。

### <a name="create-requests-and-collect-data"></a>建立要求並收集資料

Priva 提供功能強大的搜尋選項，可在組織儲存在Microsoft 365的內容中尋找與資料主體相關的資料。 它也可協助您排定專案優先順序，以在您針對這些要求收集的資料內檢閱。 Priva 知道來自 Microsoft Purview 資訊保護 的敏感度標籤，這表示可能機密且可能需要特殊檢閱的內容，並以這些標籤標示專案。 此外，Priva 可以偵測並標幟可能包含多人資料的專案，您可能需要在將內容提供給資料主體之前先進行修訂。

若要深入瞭解，請 [參閱建立主體許可權要求](subject-rights-requests-create.md)。

### <a name="data-matching"></a>資料比對

透過資料比對，您可以讓 Priva 根據確切提供的資料值來識別資料主體。 上傳此類型的資訊有助於提高尋找內容的精確度，並簡化在主體許可權要求建立期間手動提供欄位的需求。 它也會在主體許可權要求和 [概觀] 圖格中提供內容，以展示具有最多資料主體內容的專案。 若要深入瞭解，請 [參閱主體許可權要求的資料比對](subject-rights-requests-data-match.md)。

### <a name="review-data-and-collaborate-on-requests"></a>檢閱資料並共同處理要求

收集資料之後，您可以評估結果、選取要包含在報表和匯出中的最相關專案，以及進行任何必要的修訂。 您可以在 [主體權利要求] 管線內，共同完成此作業。

若要深入瞭解，請 [參閱檢閱主體許可權要求的資料](subject-rights-requests-data-review.md)。

### <a name="fulfill-requests"></a>履行要求

Priva 提供您工具來建立報表，並收集要傳回給資料主體的檔案。 若要深入瞭解，請 [參閱產生報告並履行主體許可權要求](subject-rights-requests-reports.md)。

### <a name="automate-tasks"></a>自動化工作

您可以使用內建的Power Automate範本，在 Priva 內建立和自動化工作流程程式。 這些範本支援在 ServiceNow 中提出票證或設定行事曆邀請等工作。 若要深入瞭解，請參閱 [主體許可權要求中的自動化工作](subject-rights-requests-automate.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
