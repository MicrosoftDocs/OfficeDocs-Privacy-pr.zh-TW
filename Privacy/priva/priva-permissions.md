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
description: 瞭解如何設定Microsoft Priva許可權，並將使用者指派給角色群組。
ms.openlocfilehash: eca08327e2db909475dbf4c072b8f6843de3d57b
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678220"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>在 Microsoft Priva 中設定使用者權限並指派角色

若要授與組織成員使用Microsoft Priva的許可權，請將這些許可權指派給Microsoft Purview 合規性入口網站中的適當角色群組。

> [!NOTE]
> 大部分Priva角色目前都指定為「隱私權管理」。 如需完整清單，請參閱下方。 Priva特有的角色不會出現在Azure Active Directory中。

## <a name="sign-in-and-set-permissions"></a>登入並設定許可權

1. 移至 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)，**然後選取** 左側導覽中的 [許可權]。  
2. 在 [**Microsoft Purview 解決方案**] 下拉式清單中，選取 [**角色]**。 角色群組的完整清單隨即出現。
3. 尋找您要新增一或多個使用者的角色群組， (查看下) 的角色群組描述，然後選取組名左邊的方塊。
4. 在該群組的飛出視窗窗格中，選取 [ **成員** ] 標頭下的 [ **編輯]**。  
5. 在飛出視窗窗格中，選取左側導覽中的 [ **選擇成員** ]。 另一個飛出視窗隨即出現。
6. 選取 **[+ 新增** ] 以選擇要新增至群組的一或多個使用者。  
7. 選取您要新增之名稱旁邊的核取方塊，然後選取底部的 [ **新增** ] 按鈕。  
8. 當您完成指派使用者時，請依序選取 [ **完成]**、[ **儲存**] 和 [ **關閉]**。

## <a name="learn-more-about-role-groups-and-roles"></a>深入瞭解角色群組和角色

視小組的結構而定，您可以選擇將使用者指派給特定的角色群組，以管理不同的Priva功能集。 成員應該根據需要完成的工作以及適當的檔案存取層級，指派給角色群組。 每個角色群組都包含一或多個角色。 這些角色可能與針對該群組成員啟用或限制的特定Priva工作或主要函式有關。 因此，不同的使用者可能會對特定Priva功能有不同的可見度和存取權。

如有需要，可以自訂角色群組。 若要避免意外遺失存取權，建議您建立您想要自訂的現有角色群組複本、為複本提供可識別的名稱、對新群組進行變更及驗證，並視需要將人員指派給該群組。

## <a name="privacy-management-role-group"></a>隱私權管理角色群組

此群組包含單一群組中的所有Priva許可權角色。 此角色群組可能適合同一個人可以執行所有職責的組織。 提供此角色群組的成員資格，會將該帳戶的完整存取權授與您擁有授權之Priva的所有功能。

建議您確定此群組一律至少有一個作用中成員。

角色包括：

- 案例管理  
- 資料分類內容檢視器  
- 資料分類清單檢視器  
- 隱私權管理管理員  
- 隱私權管理分析  
- 隱私權管理調查  
- 隱私權管理永久貢獻  
- 隱私權管理暫時貢獻  
- 隱私權管理檢視器  
- 主體許可權要求管理員  
- View-Only案例

## <a name="privacy-management-administrators-role-group"></a>隱私權管理系統管理員角色群組

此角色群組的成員可以廣泛存取Priva功能，包括建立、讀取、更新和刪除隱私權風險管理原則、主體許可權要求、許可權和設定。

角色包括：

- 案例管理  
- 隱私權管理管理員  
- View-Only案例

## <a name="privacy-management-analysts-role-group"></a>隱私權管理分析師角色群組

此角色群組的成員是案例分析師。 他們可以調查原則相符專案、檢視檔案中繼資料，以及採取補救動作。 此群組無法透過內容總管存取完整檔案。

角色包括：

- 案例管理  
- 資料分類清單檢視器  
- 隱私權管理分析  
- View-Only案例

### <a name="privacy-management-investigators-role-group"></a>隱私權管理調查人員角色群組

此群組的成員會擔任資料調查員。 他們可以調查原則相符專案、檢視相關聯的檔案內容，以及採取補救動作。 此群組可以透過內容總管存取檔案。

角色包括：

- 案例管理  
- 資料分類內容檢視器  
- 資料分類清單檢視器  
- 隱私權管理調查  
- View-Only案例

## <a name="privacy-management-viewer-role-group"></a>隱私權管理檢視器角色群組

此群組的成員可以在Priva中檢視分析資訊，例如概觀、資料設定檔和主體要求報告。

角色包括：

- 隱私權管理檢視器

## <a name="subject-rights-request-administrators-role-group"></a>主體許可權要求系統管理員角色群組

此群組的成員具有管理和建立主體許可權要求的完整存取權。

角色包括：

- 主體許可權要求管理員

## <a name="privacy-management-contributors-role-group"></a>隱私權管理參與者角色群組

此群組的成員可以存取已新增為共同作業者的主體許可權要求。  

角色包括：

- 隱私權管理暫時貢獻  
- 隱私權管理永久貢獻

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva法律免責聲明](priva-disclaimer.md)