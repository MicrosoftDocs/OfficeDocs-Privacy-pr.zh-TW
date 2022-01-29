---
title: 在 Microsoft Priva 中設定使用者權限並指派角色
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
- M365-priva-privacy-risk-management
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: 瞭解如何設定 Microsoft Priva 許可權，以及將使用者指派給角色群組。
ms.openlocfilehash: bcc2e108f10e427e55034621f2f8b5c40e6d9184
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248892"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>在 Microsoft Priva 中設定使用者權限並指派角色

若要授與組織成員使用 Microsoft Priva 的許可權，請將其指派給 Microsoft 365 合規性中心中適當的角色群組。

> [!NOTE]
> 大多數的 Priva 角色目前都指定為「隱私權管理」。 如需完整清單，請參閱下一節。 Priva 特有的角色不會出現在 Azure Active Directory 中。

## <a name="sign-in-and-set-permissions"></a>登入和設定許可權

1. 移至 [ [Microsoft 365 合規性中心](https://compliance.microsoft.com/)]，然後選取左側導覽中的 [**許可權**]。  
2. 在 [ **規範中心** ] 下拉式清單中，選取 [ **角色**]。 將會顯示完整的角色群組清單。
3. 尋找您要新增一或多個使用者的角色群組，然後選取 [組名] 左側的方塊。
4. 在該群組的彈出窗格上，選取 [**成員**] 標題底下的 [**編輯**]。  
5. 選取 **[選擇成員**]。 會出現另一個快顯視窗。
6. 選取 [ **+ 新增** ] 選擇一或多個要新增至群組的使用者。  
7. 選取您要新增之名稱旁邊的核取方塊，然後選取底部的 [ **新增** ] 按鈕。  
8. 當您完成指派使用者時，請選取 [ **完成**]，然後按一下 [ **儲存**]，再按一下 [ **關閉**]。

## <a name="learn-more-about-role-groups-and-roles"></a>深入瞭解角色群組和角色

根據小組的結構，您可以選擇將使用者指派至特定角色群組，以管理不同的 Priva 功能集合。 根據需要完成的工作及適當的檔案存取層級，應將成員指派給角色群組。 每個角色群組都包含一或多個角色。 這些角色可能與特定 Priva 工作或為該群組成員啟用或限制的重要功能相關。 因此，不同的使用者可能會有不同的可見度層級和存取權 Priva 某些功能。

如有需要，可以自訂角色群組。 為了避免意外遺失存取，我們建議您建立您想要自訂之現有角色群組的複本，讓複製可辨識的名稱，並對新的群組進行變更並驗證您的變更，並視需要指派使用者。

## <a name="privacy-management-role-group"></a>隱私權管理角色群組

此群組包含單一群組中的所有 Priva 許可權角色。 這個角色群組可能非常適合相同人員可以執行所有責任的組織。 在此角色群組中提供成員資格，會授與該帳戶對您持有授權之 Priva 所有功能的完整存取權。

建議您確定此群組中永遠至少有一個作用中的成員。

角色包括：

- 案例管理  
- 資料分類內容檢視器  
- 資料分類清單檢視器  
- 隱私權管理系統管理員  
- 隱私權管理分析  
- 隱私權管理調查  
- 隱私權管理永久貢獻  
- 隱私權管理的暫存份額  
- 隱私權管理檢視器  
- 主體權利要求系統管理員  
- View-Only 案例

## <a name="privacy-management-administrators-role-group"></a>隱私權管理系統管理員角色群組

這個角色群組的成員具有對 Priva 函式的廣泛存取權，包括建立、讀取、更新及刪除隱私權風險管理原則、主體權利要求、許可權及設定。

角色包括：

- 案例管理  
- 隱私權管理系統管理員  
- View-Only 案例

## <a name="privacy-management-analysts-role-group"></a>隱私權管理分析員角色群組

此角色群組的成員充當案例分析師。 他們可以調查原則相符、查看檔案中繼資料，以及採取修正動作。 這個群組無法透過內容瀏覽器存取完整檔案。

角色包括：

- 案例管理  
- 資料分類清單檢視器  
- 隱私權管理分析  
- View-Only 案例

### <a name="privacy-management-investigators-role-group"></a>隱私權管理調查人員角色群組

此群組的成員擔當資料調查人員。 他們可以調查原則相符、查看關聯的檔案內容，以及採取修正動作。 這個群組可以透過內容瀏覽器存取檔。

角色包括：

- 案例管理  
- 資料分類內容檢視器  
- 資料分類清單檢視器  
- 隱私權管理調查  
- View-Only 案例

## <a name="privacy-management-viewer-role-group"></a>隱私權管理檢視器角色群組

這個群組的成員可以在 Priva 中查看分析資訊，例如「一覽」、「資料設定檔」及「主題要求報告」。

角色包括：

- 隱私權管理檢視器

## <a name="subject-rights-request-administrators-role-group"></a>主體許可權要求系統管理員角色群組

此群組的成員具有管理的完整存取權及建立主體許可權要求。

角色包括：

- 主體權利要求系統管理員

## <a name="privacy-management-contributors-role-group"></a>隱私權管理參與者角色群組

此群組的成員可以存取已經新增為合作者的主體權力要求。  

角色包括：

- 隱私權管理的暫存份額  
- 隱私權管理永久貢獻

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)