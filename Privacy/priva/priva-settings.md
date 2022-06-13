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
description: 瞭解Microsoft Priva的全域設定選項。
ms.openlocfilehash: a6f2fe55600d6cc3018c9d15f05a6d9e459a1486
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046597"
---
# <a name="configure-priva-settings"></a>設定 Priva 設定

您可以選取畫面右上角的齒輪圖示來管理Microsoft Priva的設定。 這裡的選項可讓您設定高階喜好設定和自訂索引鍵屬性。 此頁面提供主要設定類別的概觀。

## <a name="anonymization"></a>匿名

您可以向特定角色中的使用者顯示隱私權風險管理功能內的匿名使用者名稱版本。 匿名功能會將可識別的顯示名稱取代為一般標籤，以協助遮罩使用者在檢閱敏感性資料時的身分識別。 此選項不適用於主體權利要求解決方案。

## <a name="user-notification-emails"></a>使用者通知電子郵件  

隱私權風險管理中的原則可讓您設定參數來評估環境中的潛在隱私權風險。 偵測到原則相符專案時，隱私權風險管理可以傳送電子郵件給您的使用者，其中包含要採取之矯正措施的建議，以及隱私權訓練的連結。 在 **設定** 中，您可以啟用或停用整體隱私權風險管理的電子郵件通知功能。 如果在設定中關閉通知功能，則會停用所有電子郵件。 若要深入瞭解原則，請參閱 [在隱私權風險管理中建立原則](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams 共同作業  

將Microsoft Teams功能與Priva 主體權利要求整合，以加強與專案關係人的共同作業。 選取 [**開啟主體許可權要求的Microsoft Teams功能**] 核取方塊會自動為每個要求建立相關聯的Teams通道。 您可以從要求的共同作業者索引 **標籤，** 將使用者新增至Teams通道。

開啟此功能會將Teams功能套用至所有要求。 取消核取方塊會關閉所有要求的這些功能。 深入瞭解 [資料檢閱程式期間的共同](subject-rights-requests-data-review.md#collaboration-for-data-review)作業。

## <a name="data-matching"></a>資料比對  

使用本節上傳描述資料主體屬性的資料架構，這有助於在您Microsoft 365環境中搜尋個人資料時識別正確的資料主體。 架構和規則套件是以 XML 格式建立和上傳。 在 [ **個人資料上傳**] 下，您也可以提交符合所提供架構的個人資料。 您可以建立並上傳自己的檔案，或選擇從 Azure 上傳個人資料。 深入瞭解 [主體許可權要求的資料比對](subject-rights-requests-data-match.md)。

## <a name="data-retention-periods"></a>資料保留期間

此設定與Priva 主體權利要求相關。 它可讓您控制您想要保留所收集資料和要求關閉後所產生報表的時間長度喜好設定。 這可以設定為 30 或 90 天，並適用于您建立的所有主體許可權要求。 建議您確認資料保留期間符合貴組織的原則和法律義務。 深入瞭解 [主體許可權要求的資料保留](subject-rights-requests-reports.md#retention-periods-for-reports-and-data)。

## <a name="data-review-tags"></a>資料檢閱標籤

資料檢閱標籤可用來標記在主體許可權要求中擷取的內容專案。 此設定區域可讓您管理標籤。 Priva提供三個預設標籤：**後續追蹤**、**刪除** 和 **更新**。 這些標籤名稱無法編輯，但您可以提供對組織有意義的這些標籤描述。

Priva也提供兩個自訂標籤，供您為組織使用命名和定義。 您會看到這些專案列為 **自訂標籤 1** 和 **自訂標籤 2** ，直到您編輯名稱為止。

請遵循下列步驟來編輯標籤名稱和描述：

- 從 [Priva **設定**] 頁面，選取 **[資料檢閱標籤]**。
- 在您要編輯的清單上尋找標記，然後選取其名稱旁邊的 **[編輯** 鉛筆] 圖示。
- 在飛出視窗窗格中，在可用的欄位中進行編輯。 針對系統磁碟區標，您只能編輯描述。 針對自訂標籤，您可以編輯名稱和描述。
- 當您完成時，請選取 **[提交** ] 以儲存變更。

標籤設定適用于所有主體許可權要求。

深入瞭解在 [檢閱主體許可權要求的資料時套用標籤](subject-rights-requests-data-review.md#apply-tags)。