---
title: 主體許可權要求中的資料估計和擷取
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
description: 瞭解如何擷取資料，以及如何修改Microsoft Priva 主體權利要求中的搜尋設定。
ms.openlocfilehash: 9d35a7f37861d7d3ecc5d1bac7db92c75939b4c3
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046723"
---
# <a name="data-estimate-and-retrieval"></a>資料估計和擷取

**在本文** 中：瞭解主體許可權要求的資料估計和資料擷取階段。 瞭解如何檢視要求的搜尋查詢，並進行編輯以精簡搜尋。

## <a name="data-estimate"></a>資料估計
建立要求之後，Priva會立即開始在Microsoft 365環境中的內容中尋找與資料主體相符的專案。 一旦我們識別出所有我們認為符合您準則的專案，您就會在要求的 [**概觀**] 頁面上，于 **[資料估計摘要**] 卡片中看到估計值。 搜尋範圍內的資料量會影響完成估計所需的時間長度。

您的要求會自動移至 **資料擷取** 的下一個階段，其中所有內容專案會一起收集，讓專案關係人共同檢閱資料。 在某些情況下，我們會先暫停資料估計，再繼續進行擷取，並通知您後續要採取的步驟，再繼續進行。

### <a name="pause-in-data-estimate"></a>資料估計中的暫停

要求在 **資料預估** 階段暫停的原因有兩個：

1. 當您第一次建立要求時，可以選擇先取得估計值。 如需詳細資訊，請參閱 [建立要求](subject-rights-requests-create.md#create-a-request) 中的步驟 5。

2. 如果估計值預計會傳回大量的專案來檢閱 (超過 10K 個專案) ，則工作流程會暫停。 此時，您可以預覽結果，並決定是否要 [編輯搜尋查詢](subject-rights-requests-create.md#refining-your-search) ，或繼續擷取已識別的專案。

當要求在 **[資料估計**] 暫停時，您會在要求的詳細資料頁面上看到一張卡片，其中包含專案數、磁片區、其位置的摘要資訊，以及可讓您 **檢視搜尋查詢詳細資料** 的連結。

![資料估計卡片。](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>檢視和編輯搜尋查詢

若要查看有關要求搜尋的詳細資訊，請選取 [**資料估計摘要**] 卡片上的 [**檢視搜尋查詢詳細** 資料]。 飛出視窗窗格隨即開啟，其中會摘要說明查詢，並顯示找到之內容的進一步詳細資料。 從這裡，您有下列選項：

- 選 **取 [預覽結果** ]，以取得將在目前搜尋設定下傳回的內容類型預覽。
- 選 **取 [編輯搜尋查詢** ] 以變更搜尋設定。

當您選取 **[編輯搜尋查詢**] 時，系統會引導您進行引導式程式來變更或新增屬性，以識別資料主體、變更條件，以及調整您想要搜尋涵蓋的位置。 請遵循 [精簡搜尋](subject-rights-requests-create.md#refining-your-search) 中的指示，以取得更詳細的資訊。 您可以檢閱新搜尋查詢的最終版本，然後選取 [ **儲存** ] 再次開始搜尋。

將會產生新的估計值，而且要求的狀態會回到 **[資料估計]**。 新的搜尋可能需要 60 分鐘才能完成。 完成後，您會在要求的詳細資料頁面上看到更新的結果。

當您準備好繼續進行時，請選取畫面右上方的 [擷 **取資料** ] 以進入資料擷取階段。

## <a name="retrieve-data"></a>擷取

資料擷取階段是擷取包含資料主體個人資料的所有檔案、電子郵件、聊天、影像和其他內容專案。 這些專案會放在 Azure Blob 儲存體容器中，以供檢閱。 視資料量而定，資料擷取可能需要幾分鐘或更長的時間。

當此階段完成時，要求會自動移至 [ **檢閱資料**] 的下一個階段。

## <a name="next-steps"></a>後續步驟

請 [造訪檢閱主體許可權要求的資料](subject-rights-requests-data-review.md) ，以瞭解重要工作，並與專案關係人共同進行 **檢閱資料** 步驟。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva法律免責聲明](priva-disclaimer.md)