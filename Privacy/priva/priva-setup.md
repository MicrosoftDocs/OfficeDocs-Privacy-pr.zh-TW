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
description: 瞭解如何為您的組織設定 Microsoft Priva、設定角色和許可權，以及設定重要設定。
ms.openlocfilehash: e88145dc999e210f36a8dc82e1bc9996bc15bb88
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930554"
---
# <a name="get-started-with-priva"></a>開始使用 Priva

如果您已準備好開始使用 Microsoft Priva，以取得識別和降低隱私權風險的協助，請遵循下列步驟來設定先決條件，並開始使用隱私權深入解析。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>步驟 1：確認訂用帳戶和授權

Priva 可在 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/) 中取得，且可由具有下列授權的組織購買：

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1、E3、E5、A1、A3、A5

Priva 提供兩種不同解決方案的授權選項：Priva Privacy Risk Management 和 Priva Subject Rights Requests。 這些可以個別或一起購買。 取得主體許可權要求的授權時，您可以針對需要處理的要求數目選擇適當的授權層級。 您可以隨時購買其他要求。

如需授權指南的詳細資料，請參閱：[Microsoft 365 安全性與合規性的授權指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva)。

> [!Note]
> 美國政府Community (GCC) 中度、GCC High 或美國國防部 (DoD) 客戶無法使用 Priva。

### <a name="get-free-trial-license"></a>取得免費試用版授權

免費試用版授權可用於開始使用 Priva。 若要瞭解資格和加入方式，請參閱 [瞭解免費的 Priva 試用版](priva-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>步驟 2：啟用Microsoft 365稽核記錄

Microsoft 365稽核記錄是組織內所有活動的摘要。 隱私權風險管理原則可能會使用這些活動來產生原則深入解析。

您的組織可能已經開啟稽核記錄。 如果您需要第一次開始使用它們，請 [參閱開啟或關閉稽核記錄搜尋](/microsoft-365/compliance/turn-audit-log-search-on-or-off) ，以取得開啟稽核的逐步指示。 開啟稽核後，就會顯示一則訊息，表示正在準備稽核記錄，而您可以在準備完成 (約幾小時) 後執行搜尋。 您只須執行此動作一次。 如需使用Microsoft 365稽核記錄的詳細資訊，請參閱[搜尋稽核記錄](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>步驟 3：設定使用者權限並指派角色

Priva 會使用角色型存取控制 (RBAC) 許可權模型。 只有獲指派角色的使用者可以存取 Priva，而且每個使用者所允許的動作會受限於角色類型。

您的全域管理員有權存取 Priva，並將其他使用者指派給角色。 他們可以在適用于 Priva 的 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/) 中登入並設定使用者權限。 為了快速入門，隱私權管理角色群組具有存取 Priva 所有功能的許可權。 此群組可能適合同一個人可以執行所有職責的組織。 其他隱私權角色可讓您採取更細微的控制，並將使用者指派給選取的功能。

若要深入瞭解角色群組和如何授與存取權，請參閱 [在 Priva 中設定使用者權限和指派角色](priva-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>步驟 4：開始尋找並視覺化您的資料

登入 Priva 之後，您會看到 [ **概觀** ] 頁面。 此頁面提供有關個人資料如何在Microsoft 365環境中演進的動態深入解析，以協助您快速找出問題、識別風險指標，以及採取動作來修正問題。 您的概觀應該會在註冊的前 24 小時內填入初始見解。 當您繼續使用 Priva 時，概觀頁面將會重新整理，以繼續提供目前的資訊。

如需一段時間資料的進一步深入解析，您的 **[資料設定檔**] 頁面會提供更多視覺效果和分析，並依地理位置和Microsoft 365位置提供您組織資料的整體檢視。

若要深入瞭解這些頁面，請 [參閱在 Priva 中尋找個人資料並將其視覺化](priva-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>步驟 5：使用預設原則開始管理風險

隱私權風險管理會開始評估您的資料，並讓您查看資料最小化、資料過度使用和資料傳輸的主要風險案例。 預設會開啟這些原則。 您可以使用這些原則來評估風險所在位置，然後開啟使用者的電子郵件通知，讓使用者注意這些問題，並引導補救這些風險。 此外，您可以從提供的原則範本建立和自訂您自己的原則。 您可以量身打造原則，以符合貴組織的法律和法規合規性需求，如與法律顧問諮詢中所發現。 若要深入瞭解，請 [參閱在隱私權風險管理中建立原則](risk-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>步驟 6：使用主體許可權要求開始

Priva Subject Rights Requests 會將主體許可權要求履行程式自動化，提供資料的輕鬆存取，以及符合現有商務程式的可自訂工作流程。 您可以輕鬆地找到相關資料、檢閱結果，以及產生報告。 在此過程中，您可以安全地與組織中的其他專家共同作業，以完成主體許可權要求。 您也可以使用內建範本來管理和自訂您的商務工作流程。 若要深入瞭解如何使用這些功能，請參 [閱瞭解 Priva Subject Rights Requests](subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
