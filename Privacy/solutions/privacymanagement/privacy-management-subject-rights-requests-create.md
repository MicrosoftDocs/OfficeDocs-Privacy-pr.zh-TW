---
title: 在隱私權管理中建立主體權力要求
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
- MET150
description: 瞭解如何在隱私權管理中建立新的主體權力要求。
ms.openlocfilehash: 316d515be454b6aceed95f68c6f3da6fa0e7567c
ms.sourcegitcommit: 85e085eb17af8b4efd1f45207445e1b3c3679600
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2021
ms.locfileid: "60478148"
---
# <a name="create-a-subject-rights-request"></a>建立主體權力要求

主旨 rights management 管理員可以透過隱私權管理的 [主要主體許可權要求] 頁面，開啟新的主體權力要求。 [！附注] 您將會引導您完成尋找資料主體的個人資料，以及開始完成要求的處理常式。

您也可以選擇上載其他材料，以啟用隱私權管理，以根據實際提供的資料值來識別資料主體。 若要深入瞭解，請參閱 [管理資料符合](privacy-management-subject-rights-requests-data-matching.md)。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用主題許可權要求建立嚮導

1. 在 [Microsoft 365 合規性中心](https://compliance.microsoft.com/)中，移至 [隱私權管理] 區段，然後選取 [**主體權力要求**]。
1. 若要開始新的要求，請選取 [ **建立要求**]。
1. 識別提出要求的資料主體，並指定其與貴公司的關聯性。
1. 我們會對與資料主體相關的專案執行預設搜尋。 如果您想要在取得資料之前精煉搜尋或取得預估，您可以在此階段進行選取。 您也可以將所有專案保留空白，並移至下一個步驟。 如需有關選項的詳細資訊，請參閱 [定義搜尋設定](#define-search-settings) 和 [縮小搜尋](#refine-your-search)。
1. 根據資料主體想要在資料中執行的動作，選擇要求類型。 如果他們的要求與特定的資料隱私權規定有關，您也可以從提供的清單中選取，以新增更多內容。  (必要) 設定期限，可讓您輕鬆地排序臨近或逾期的要求，並及時解決。 要求類型包括：
   - **Access**：提供組織在 Microsoft 365 中所用之資料主體個人資訊的摘要。
   - **匯出**：提供資料主體的個人資訊的摘要及匯出，如審閱時所收集及批註。
   - **後續的標籤清單**：會產生使用者在複查時標記的任何檔案摘要，可能需要在隱私權管理以外進行其他動作。 例如，您可能需要根據其要求，協助刪除資料主體的個人資訊。 您可以在全域設定中管理主體權力要求的自訂資料審閱標記 **。**
1. 確認此要求的名稱，並新增參考的選擇性描述。
1. 請複查您在先前步驟中輸入的內容摘要。 您可以先編輯任何欄位，然後再選取 [ **建立要求**]。

### <a name="define-search-settings"></a>定義搜尋設定

建立主體權利要求時，您可以選擇下列其中一個或所有搜尋選項，以尋找主旨的相關資料：

- **包含資料主體所** 製作的內容：這包括資料主體所製作的內容，而且可能會傳回較高的資料量。
- **精簡搜尋**：這可讓您指定額外的屬性，以協助您識別資料主體。 您可以在這裡將搜尋的範圍限定為特定 Microsoft 365 服務或資源，或選取其他條件來調整要求的範圍。 選擇此選項後，系統會提示您輸入自訂的搜尋參數。
- **先取得預估**：這樣可讓您在自動檢索資料之前，查看預計會找到多少資料。

### <a name="refine-your-search"></a>縮小搜尋

如果您選擇在定義搜尋設定時精煉搜尋，系統會要求您填寫您的高級搜尋參數。 您可以在 Microsoft 365 進行搜尋時 **，加入識別碼、** 設定 **條件** 及選擇特定 **位置**。

- **新增識別碼**：提供更多有關資料主體的資訊，例如名稱、電子郵件地址和/或其他選項。 使用分號分隔每個欄位中的多個值。
- **條件**：從下拉式清單中選擇一種類型，開始新增搜尋的條件。 這些類型對應于可能的資料屬性，如時間範圍、大小、保留標籤、寄件者和收件者，以及許多其他類型。 選取任何類型以加以新增，然後設定您想要的屬性。 若為文字欄位專案，您可以新增多個關鍵字，以分號分隔。 您可以視需要新增任意數目的內容類型。
- **位置**：您可以設定搜尋的範圍，以針對特定 SharePoint 網站、Teams 通道和商務用 OneDrive 位置。 您可以針對每個位置選取所有實例（如所有 Exchange 信箱）或特定實例（例如一個使用者的信箱）。 選取 [ **選擇** 每個位置的連結] 選項，以輸入特定實例的相關資訊。 如需識別適當搜尋字詞的說明，請參閱下列各項：
  - [管理新 SharePoint 系統管理中心中的網站](/sharepoint/manage-sites-in-new-admin-center)：提供如何排序和篩選網站以及如何搜尋 SharePoint 網站的指導方針。 使用此來尋找 SharePoint 搜尋欄位的 URLs。
  - [取得-小組](/powershell/module/teams/get-team)：提供如何在特定屬性/資訊 Microsoft Teams 中尋找小組的相關資訊。 使用此資訊可協助您找出 Teams 聊天和頻道。
  - [關於 OneDrive URLs](/onedrive/list-onedrive-urls#about-onedrive-urls)：提供使用者 OneDrive URL 之正確格式及屬性的相關資訊。 使用此資訊可協助您識別搜尋中 OneDrive 網站。

建議您認真檢查您的選擇，以確保您識別正確的資料主體。 例如，如果您依名稱搜尋信箱，並尋找具有類似名稱的多個使用者，請先確認是否正確，再將其新增至您的要求。

## <a name="next-steps"></a>後續步驟

在您建立要求之後，您會看到它會列在 [主體權力要求] 頁面上。 若要深入瞭解如何繼續進行審閱，請參閱 [查看資料並共同處理要求](privacy-management-subject-rights-requests-review.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[隱私權管理法律免責聲明](privacy-management-disclaimer.md)
