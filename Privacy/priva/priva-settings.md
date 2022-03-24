---
title: 設定 Priva 設定
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
- MET150
description: 深入瞭解 Microsoft Priva 的通用設定選項。
ms.openlocfilehash: 1cbb508d8c1dd98dfa846595d81e8aaeecdbaeb4
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758422"
---
# <a name="configure-priva-settings"></a>設定 Priva 設定

您可以選取畫面右上角的齒輪圖示，以管理 Microsoft Priva 的設定。 這裡的選項可讓您設定高層首選項及自訂重要屬性。 此頁面提供主要設定類別的概覽。

## <a name="anonymization"></a>匿名

您可以針對特定角色中的使用者，顯示隱私權風險管理功能中的匿名版本的使用者名稱。 匿名功能會以一般標籤取代可辨識的顯示名稱，以協助掩蓋使用者在查看機密資料時的身分識別。 此選項不適用於「主體權利要求」方案。

## <a name="user-notification-emails"></a>使用者通知電子郵件  

隱私權風險管理中的原則可讓您設定用來評估環境中潛在隱私權風險的參數。 偵測到原則相符時，隱私權風險管理可以將電子郵件傳送給您的使用者，並提供修正動作的建議，以及隱私權訓練的連結。 在 **設定** 中，您可以啟用或停用以整體進行隱私權風險管理的電子郵件通知功能。 如果在設定中關閉通知功能，將會停用所有電子郵件。 若要深入瞭解原則，請參閱 [Create In 隱私政策 In 隱私權風險管理](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams 共同作業  

整合 Microsoft Teams 功能與 Priva 的主體權力要求，以加強與專案關係人的共同作業。 每次建立主體權力要求時，就會在 Teams 中建立相關聯的小組。 使用者可以從 [要求的合作者] 索引標籤中新增至小組。若要深入瞭解主題權力要求，請參閱 [瞭解 Priva 的主體權力要求](subject-rights-requests.md)。

## <a name="data-matching"></a>資料符合  

使用此區段可上傳描述資料主體之屬性的資料架構，可協助您在 Microsoft 365 環境中搜尋個人資料時，識別正確的資料主體。 架構和規則套件是以 XML 格式建立及上傳。 在 **[個人資料上傳**] 底下，您也可以提交與所提供架構相符的個人資料。 您可以建立和上傳您自己的檔案，或選擇從 Azure 上傳個人資料。 若要深入瞭解主題權力要求，請參閱 [瞭解 Priva 的主體權力要求](subject-rights-requests.md)。

## <a name="data-retention-periods"></a>資料保留期間

此設定與 Priva 主體權利要求相關。 它可讓您控制您要保留收集的資料和報告在要求關閉之後所產生之時間的喜好設定。 這可以設定為30或90天，並套用至您建立的所有主體權力要求。 建議您確認您的資料保留期間符合組織的原則和法律義務。 深入瞭解 [設定主體許可權要求的資料保留](subject-rights-requests-reports.md#manage-data-retention)。

## <a name="data-review-tags"></a>資料審閱標記

資料審閱標記可用來標示以主體權力要求所檢索的內容專案。 [設定] 區域可讓您管理標記。 Priva 提供三個預設標記： **跟進**、 **刪除** 和 **更新**。 這些標記名稱無法編輯，但您可以為組織提供有意義之這些標記的描述。

Priva 也提供兩個自訂標記，您可以為組織的用途命名並加以定義。 您會看到這些列是 **自訂標記 1** 和 **自訂標記 2** ，直到您編輯名稱為止。

請遵循下列步驟編輯標記名稱和描述：

- 在 [Priva **設定**] 頁面上，選取 [**資料審閱標記**]。
- 在清單中尋找您要編輯的標記，並選取其名稱旁邊的 [ **編輯** 鉛筆] 圖示。
- 在飛入窗格中，在可用欄位中進行編輯。 對於系統標記，您只能編輯描述。 若為自訂標記，您可以編輯 [名稱] 和 [描述]。
- 完成後，請選取 [ **提交** ] 以儲存您的變更。

標記設定會套用至所有主體權力要求。

深入瞭解 [在查看主體權力要求的資料時套用標記](subject-rights-requests-data-review.md#apply-tags)。