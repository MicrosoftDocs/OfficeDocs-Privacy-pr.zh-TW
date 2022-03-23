---
title: 深入瞭解 Priva 的主體權力要求
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
description: Microsoft Priva 中的主體權力要求解決方案可協助您找出個人資料，並共同查看內容和建立報告。
ms.openlocfilehash: 25eb785651ec0edd1035aba54b20d19404619b80
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758442"
---
# <a name="learn-about-priva-subject-rights-requests"></a>深入瞭解 Priva 的主體權力要求

根據世界各地的某些隱私權規定，個人 (或 *資料主體*) 可能要求複查或管理公司所收集的個人資料。 這些要求有時也稱為資料主體要求 (Dsr) 、資料主體存取要求 (DSARs) 或使用者權限要求。 針對儲存大量資訊的公司，尋找相關資料可能是一項艱巨的工作。

Microsoft Priva 可協助您透過主體權利要求解決方案來處理這些查詢。 它提供工作流程、自動化和共同作業功能，協助您搜尋主體資料、查看您的結果、收集適當的檔案，並產生報告。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva 對主體權力要求履行的支援

主體權利要求週期始于組織的個人要求。 收到之後，您可以使用 Priva 的功能來收集該資料、共同作業、審閱及建立報告。 然後，您可以通知結果的資料主體，並在 Priva 之外進行其他任何必要的動作，以完成要求，例如刪除資料。 若要協助您同時管理和自動化工作流程，您也可以使用整合的 Power Automate 範本。

### <a name="create-requests-and-collect-data"></a>建立要求並收集資料

Priva 提供強大的搜尋選項，可讓您在組織儲存的內容中，尋找與您的資料主體相關的資料 Microsoft 365。 它也可協助您排定專案的優先順序，以在您為這些要求收集的資料中進行審閱。 Priva 知道 Microsoft 資訊保護敏感度標籤，表示有潛在機密的內容，而且可能需要特殊檢查，並使用這些標籤專案。 此外，Priva 可以偵測和旗標專案，其中可能包含多個人員的資料，在這種情況下，您可能需要將內容密文，再將其提供給資料主體。

若要深入瞭解，請參閱 [建立主體權力要求](subject-rights-requests-create.md)。

### <a name="data-matching"></a>資料符合

使用資料比對，您可以讓 Priva 根據正確提供的資料值來識別資料主體。 上傳這種類型的資訊有助於提高尋找內容的精確度，也簡化了建立主體許可權要求時手動提供欄位的需要。 它也會提供主題許可權要求中的內容，以及顯示最多資料主體內容之專案的總覽磚。 若要深入瞭解，請參閱 [主體權力要求的資料比對](subject-rights-requests-data-match.md)。

### <a name="review-data-and-collaborate-on-requests"></a>查看要求的資料並進行共同作業

收集資料後，您可以評估結果，選取要包含在報表和匯出中的最相關專案，以及進行任何必要的密文。 這可以在主體權力要求管線中的小組成員之間，以一致的方式完成。

若要深入瞭解，請參閱 [查看主體權力要求的資料](subject-rights-requests-data-review.md)。

### <a name="fulfill-requests"></a>完成要求

Priva 提供您用來建立報表及收集要傳送回資料主體的檔的工具。 若要深入瞭解，請參閱 [產生報表及履行主體權力要求](subject-rights-requests-reports.md)。

### <a name="automate-tasks"></a>自動化工作

您可以使用內建的 Power Automate 範本，在 Priva 中建立及自動化工作流程處理常式。 這些範本支援 ServiceNow 中的「歸檔票據」或設定行事曆邀請等工作。 若要深入瞭解，請參閱 [自動化主題許可權要求中的](subject-rights-requests-automate.md)工作。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
