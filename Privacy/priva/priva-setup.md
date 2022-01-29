---
title: 開始使用 Priva
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150fcf
description: 瞭解如何為您的組織設定 Microsoft Priva，設定角色和許可權，以及設定重要設定。
ms.openlocfilehash: 62e28361b57dd866b95ce566616473ed1a71e4ad
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248891"
---
# <a name="get-started-with-priva"></a>開始使用 Priva

如果您準備好開始使用 Microsoft Priva 以協助識別及降低隱私權風險，請遵循下列步驟來設定必要條件，並開始探索隱私權深入瞭解。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>步驟1：確認訂閱和授權

Priva 可在[Microsoft 365 合規性中心](https://compliance.microsoft.com/)內取得，而且可由具有下列授權的組織購買：

- Microsoft 365 E3，E5，A3，A5
- Office 365 E1，E3，E5，A1，A3，A5

Priva 提供兩種不同解決方案的授權選項： Priva 隱私權風險管理和 Priva 主體權力要求。 這些可以個別購買，也可以一起購買。 取得主體權利要求的授權時，您可以針對需要處理的要求數量，選擇適當的授權層級。 您可以隨時購買其他要求。

如需授權指南的詳細資料，請參閱：[Microsoft 365 安全性與合規性的授權指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)。

> [!Note]
> Priva 不適用於美國政府 Community (GCC) 適中、GCC 高或國防部 (DoD) 客戶。

### <a name="get-free-trial-license"></a>取得免費試用版授權

免費試用授權可用於 Priva 的快速入門。 若要瞭解資格和如何加入的方式，請參閱 [瞭解免費的 Priva 試用版](priva-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>步驟2：啟用 Microsoft 365 審核記錄

Microsoft 365 的審計記錄檔是組織內所有活動的摘要。 隱私權風險管理原則可能會使用這些活動來產生原則洞察力。

您的組織可能已開啟審核記錄。 如果您第一次必須開始使用它們，請參閱 [開啟或關閉審核記錄搜尋](/microsoft-365/compliance/turn-audit-log-search-on-or-off) ，以開啟審計的逐步指示。 開啟稽核後，就會顯示一則訊息，表示正在準備稽核記錄，而您可以在準備完成 (約幾小時) 後執行搜尋。 您只須執行此動作一次。 如需使用 Microsoft 365 審核記錄的詳細資訊，請參閱[搜尋審核記錄](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)檔。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>步驟3：設定使用者許可權及指派角色

Priva 使用以角色為基礎的存取控制 (RBAC) 許可權模型。 只有獲指派角色的使用者可以存取 Priva，且每個使用者所允許的動作受到角色類型的限制。

您的全域系統管理員具有存取 Priva 的許可權，並將其他使用者指派給角色。 使用者可以在 Priva 中登入和設定[Microsoft 365 合規性中心](https://compliance.microsoft.com/)的使用者權限。 為了快速開始，隱私權管理角色群組具有存取 Priva 所有功能的許可權。 在相同個人可能執行所有責任的組織中，此群組可能非常適合。 其他隱私權角色可讓您進行更細微的控制，並將使用者指派給選取的功能。

若要深入瞭解角色群組及如何授與存取權，請參閱 [Set user 權力和指派 Priva 中的角色](priva-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>步驟4：開始尋找及形象地進行資料

登入 Priva 後，您將會看到 [ **概述** ] 頁面。 此頁面提供有關如何在 Microsoft 365 環境中對個人資料進行演變的動態深入資訊，以協助您快速找出問題、識別風險指標，並採取行動以修正問題。 您的概要應該在註冊前24小時內填入初步深入資訊。 當您繼續使用 Priva 時，[一覽] 頁面會重新整理，以繼續提供目前的資訊。

若要進一步深入瞭解您在一段時間內的資料，您的 **資料設定檔** 頁面將提供更多視覺化效果和分析，並提供組織資料的整體觀點，依地理位置和 Microsoft 365 位置。

若要深入瞭解這些頁面，請參閱 [在 Priva 中尋找及顯示個人資料](priva-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>步驟5：開始使用預設原則來管理風險

隱私權風險管理將開始評估您的資料，並讓您瞭解資料最小化、資料 overexposure 及資料傳輸的重要風險案例。 預設會開啟這些原則。 您可以使用這些原則評估風險的所在位置，然後為使用者開啟使用者電子郵件通知，以引發問題，並引導這些風險的修復。 此外，您也可以從提供的原則範本建立及自訂您自己的原則。 您可以調整原則，以符合法律顧問對您的組織法律和法規合規性需求。 若要深入瞭解，請參閱 [Create a In 隱私政策 In 隱私權風險管理](risk-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>步驟6：開始使用主體權力要求

Priva 的主體權力要求會自動化主體權利要求的履行處理常式，讓您可以輕鬆存取可納入現有商務程式的資料和可自訂的工作流程。 您可以輕鬆地找到相關的資料、查看結果，並產生報告。 同時，您可以安全地與組織中的其他專家合作，以完成主體權利要求。 您也可以使用內建的範本管理及自訂商務工作流程。 若要深入瞭解使用這些功能，請參閱 [瞭解 Priva 的主體許可權要求](subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
