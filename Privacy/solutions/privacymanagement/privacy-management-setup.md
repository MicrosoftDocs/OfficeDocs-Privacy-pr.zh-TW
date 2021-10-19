---
title: 開始使用記錄管理
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
- MET150fcf
description: 瞭解如何為組織設定隱私權管理、設定角色和許可權，以及設定重要設定。
ms.openlocfilehash: 0f64c581fbeb13726ee9ca2a0f695a5d4f55eb97
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478126"
---
# <a name="get-started-with-privacy-management"></a>開始使用記錄管理

如果您準備好開始使用 Microsoft 隱私權管理來識別及降低隱私權風險，請遵循下列步驟來設定必要條件，並開始探索隱私權深入瞭解。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>步驟1：確認訂閱和授權

您可以在[Microsoft 365 合規性中心](https://compliance.microsoft.com/)內使用隱私權管理，並可由具有下列授權的組織購買：

- Microsoft 365 E3，E5，A3，A5
- Office 365 E1，E3，E5，A1，A3，A5

隱私權管理為解決方案的兩個不同模組提供授權選項：風險和主體權利要求。 這些可以個別購買，也可以一起購買。 取得主體權利要求的授權時，您可以針對需要處理的要求數量，選擇適當的授權層級。 您可以隨時購買其他要求。

如需授權指南的詳細資料，請參閱：[Microsoft 365 安全性與合規性的授權指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)。

> [!Note]
> 隱私權管理不適用於美國政府 Community (GCC) 適中、GCC 高或國防部 (DoD) 客戶。

### <a name="get-free-trial-license"></a>取得免費試用版授權

您可以使用免費試用版授權開始使用隱私權管理。 若要瞭解資格及如何加入的相關資訊，請參閱 [瞭解免費的隱私權管理試用版](privacy-management-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>步驟2：啟用 Microsoft 365 審核記錄

Microsoft 365 的審計記錄檔是組織內所有活動的摘要。 隱私權管理原則可能會使用這些活動來產生原則 insights。

您的組織可能已開啟審核記錄。 如果您第一次必須開始使用它們，請參閱 [開啟或關閉審核記錄搜尋](/microsoft-365/compliance/turn-audit-log-search-on-or-off) ，以開啟審計的逐步指示。 開啟稽核後，就會顯示一則訊息，表示正在準備稽核記錄，而您可以在準備完成 (約幾小時) 後執行搜尋。 您只須執行此動作一次。 如需使用 Microsoft 365 審核記錄的詳細資訊，請參閱[搜尋審核記錄](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)檔。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>步驟3：設定使用者許可權及指派角色

隱私權管理使用以角色為基礎的存取控制 (RBAC) 許可權模型。 只有獲指派角色的使用者才可存取隱私權管理，且每個使用者所允許的動作受到角色類型的限制。

您的全域系統管理員具有存取隱私權管理的許可權，並將其他使用者指派給角色。 使用者可以在隱私權管理的[Microsoft 365 合規性中心](https://compliance.microsoft.com/)中登入和設定使用者權限。 若要快速開始，隱私權管理角色群組具有存取隱私權管理所有功能的許可權。 這個群組可能非常適合於相同人員可以在隱私權管理解決方案內執行所有工作的組織。 其他隱私權角色可讓您進行更細微的控制，並將使用者指派給選取的功能。

若要深入瞭解角色群組以及如何授與存取權，請參閱 [Set user 權力和 assign role](privacy-management-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>步驟4：開始尋找及形象地進行資料

登入隱私權管理之後，您將會看到 [ **概述** ] 頁面。 此頁面提供有關如何在 Microsoft 365 環境中對個人資料進行演變的動態深入資訊，以協助您快速找出問題、識別風險指標，並採取行動以修正問題。 您的概要應該在註冊前24小時內填入初步深入資訊。 當您繼續使用隱私權管理時，[一覽] 頁面會重新整理，以繼續提供目前的資訊。

若要進一步深入瞭解您在一段時間內的資料，您的 **資料設定檔** 頁面將提供更多視覺化效果和分析，並提供組織資料的整體觀點，依地理位置和 Microsoft 365 位置。

若要深入瞭解這些頁面，請參閱 [尋找及形象化您的資料](privacy-management-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>步驟5：開始使用預設原則來管理風險

隱私權管理將開始評估您的資料，並讓您瞭解資料最小化、資料 overexposure 及資料傳輸的重要風險案例。 預設會開啟這些原則。 您可以使用這些原則評估風險的所在位置，然後為使用者開啟使用者電子郵件通知，以引發問題，並引導這些風險的修復。 此外，您也可以從提供的原則範本建立及自訂您自己的原則。 您可以調整原則，以符合法律顧問對您的組織法律和法規合規性需求。 若要深入瞭解，請參閱 [使用隱私權管理中的原則管理隱私權風險](privacy-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>步驟6：開始使用主體權力要求

隱私權管理可讓遵循現有商務程式的資料與可自訂工作流程的簡易存取，使主體權利要求履行處理常式自動化。 您可以輕鬆地找到相關的資料、查看結果，並產生報告。 同時，您可以安全地與組織中的其他專家合作，以完成主體權利要求。 您也可以使用內建的範本管理及自訂商務工作流程。 若要深入瞭解使用這些功能，請參閱 [管理主體權力要求](privacy-management-subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[隱私權管理法律免責聲明](privacy-management-disclaimer.md)
