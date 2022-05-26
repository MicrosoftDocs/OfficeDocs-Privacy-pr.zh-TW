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
description: 瞭解如何為您的組織設定Microsoft Priva、設定角色和許可權，以及設定重要設定。
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678210"
---
# <a name="get-started-with-priva"></a>開始使用 Priva

如果您已準備好開始使用Microsoft Priva來協助您的組織找出並降低隱私權風險，請遵循下列步驟來協助進行設定。

## <a name="confirm-subscriptions-and-licensing"></a>確認訂用帳戶和授權

Priva可在[Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)內取得，且可由具有下列授權的組織購買：

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1、E3、E5、A1、A3、A5

Priva提供兩種不同解決方案的授權選項：Priva 隱私權風險管理和Priva 主體權利要求。 這些可以個別或一起購買。 取得主體許可權要求的授權時，您可以針對需要處理的要求數目選擇適當的授權層級。 您可以隨時購買其他要求。

如需授權指南的詳細資料，請參閱：[Microsoft 365 安全性與合規性的授權指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva)。

> [!Note]
> Priva不適用於美國政府Community (GCC) 中度、GCC高或美國國防部 (DoD) 客戶。

### <a name="start-a-free-trial"></a>開始免費試用

使用免費試用訂用帳戶來探索Priva解決方案的所有功能。 瞭解如何註冊[Priva試用版](priva-trial.md)。

## <a name="enable-the-microsoft-365-audit-log"></a>啟用Microsoft 365稽核記錄

Microsoft 365稽核記錄是組織內所有活動的摘要。 隱私權風險管理原則可能會使用這些活動來產生原則深入解析。

您的組織可能已經開啟稽核記錄。 如果您需要第一次開始使用它們，請 [參閱開啟或關閉稽核記錄搜尋](/microsoft-365/compliance/turn-audit-log-search-on-or-off) ，以取得開啟稽核的逐步指示。 開啟稽核後，就會顯示一則訊息，表示正在準備稽核記錄，而您可以在準備完成 (約幾小時) 後執行搜尋。 您只須執行此動作一次。 如需使用Microsoft 365稽核記錄的詳細資訊，請參閱[搜尋稽核記錄](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)。

## <a name="set-user-permissions-and-assign-roles"></a>設定使用者權限並指派角色

Priva使用角色型存取控制 (RBAC) 許可權模型。 只有獲指派角色的使用者可以存取Priva，而且每個使用者所允許的動作會受到角色類型限制。

您的全域系統管理員有權存取Priva，並將其他使用者指派給角色。 他們可以在[Priva的Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)中登入並設定使用者權限。 為了快速入門，隱私權管理角色群組有權存取Priva的所有功能。 此群組可能適合同一個人可以執行所有職責的組織。 其他隱私權角色可讓您採取更細微的控制，並將使用者指派給選取的功能。

若要深入瞭解角色群組和如何授與存取權，請參閱[在Priva中設定使用者權限和指派角色](priva-permissions.md)。

## <a name="start-finding-and-visualizing-your-data"></a>開始尋找並視覺化您的資料

登入Priva之後，您會看到 [**概觀**] 頁面。 此頁面提供有關個人資料如何在Microsoft 365環境中演進的動態深入解析，以協助您快速找出問題、識別風險指標，以及採取動作來修正問題。 您的概觀應該會在註冊的前 24 小時內填入初始見解。 當您繼續使用Priva時，概觀頁面將會重新整理，以繼續提供目前的資訊。

如需一段時間資料的進一步深入解析，您的 **[資料設定檔**] 頁面會提供更多視覺效果和分析，並依地理位置和Microsoft 365位置提供您組織資料的整體檢視。

若要深入瞭解這些頁面，請參閱[在Priva中尋找個人資料並將其視覺化](priva-data-profile.md)。

## <a name="start-managing-risks-with-default-policies"></a>使用預設原則開始管理風險

隱私權風險管理會開始評估您的資料，並讓您查看資料最小化、資料過度使用和資料傳輸的主要風險案例。 預設會開啟這些原則。 您可以使用這些原則來評估風險所在位置，然後開啟使用者的電子郵件通知，讓使用者注意這些問題，並引導補救這些風險。 此外，您可以從提供的原則範本建立和自訂您自己的原則。 您可以量身打造原則，以符合貴組織的法律和法規合規性需求，如與法律顧問諮詢中所發現。 若要深入瞭解，請 [參閱在隱私權風險管理中建立原則](risk-management-policies.md)。

## <a name="get-started-with-subject-rights-requests"></a>具有主體許可權要求的開始

Priva 主體權利要求自動化主體許可權要求履行程式，提供資料的輕鬆存取，以及符合現有商務程式的可自訂工作流程。 您可以輕鬆地找到相關資料、檢閱結果，以及產生報告。 在此過程中，您可以安全地與組織中的其他專家共同作業，以完成主體許可權要求。 您也可以使用內建範本來管理和自訂您的商務工作流程。 若要深入瞭解如何使用這些功能，請參閱[瞭解Priva 主體權利要求](subject-rights-requests.md)。

## <a name="priva-availability"></a>Priva可用性

Microsoft Priva可供全球客戶使用。 如果您的組織在下列其中一個本機資料中心布建其租使用者，以符合資料落地需求，Priva解決方案將無法在Microsoft Purview 合規性入口網站的左側導覽中使用：

- 挪威
- 波蘭
- 卡達
- 新加坡
- 南非
- 韓國
- 西班牙
- 瑞典
- 瑞士
- 阿拉伯聯合大公國

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva法律免責聲明](priva-disclaimer.md)
