---
title: 建立主體許可權要求
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
description: 瞭解如何在 Microsoft Priva 中建立新的主體許可權要求。
ms.openlocfilehash: b2d846aa4020be315705bbd16e00378c7514146c
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930604"
---
# <a name="create-a-subject-rights-request"></a>建立主體許可權要求

主體版權管理管理員可以透過 Priva 的主要主體許可權要求頁面來開啟新的要求。 精靈會引導您完成尋找資料主體相關個人資料的程式，並開始完成其要求的程式。

您也可以選擇上傳其他資料，讓 Priva 能夠根據確切提供的資料值來識別資料主體。 若要深入瞭解，請 [參閱主體許可權要求的資料比對](subject-rights-requests-data-match.md)。

## <a name="request-types"></a>要求類型

Priva Subject Rights Requests 支援三種不同類型的要求：

1. **存取**：提供貴組織在Microsoft 365中保存的資料主體個人資訊摘要。

2. **導** 出：提供包含資料主體個人資訊的內容專案摘要和匯出的檔案。 這些專案會在您檢閱搜尋設定所收集的資料期間檢閱並標示為 [ **已** 包含]。

3. **已標記的待處理清單**：產生在資料檢閱期間標記的任何檔案摘要，這些檔案可能需要在 Priva 外部採取其他動作。 例如，您可能需要根據其要求來協助刪除資料主體的個人資訊。 您可以在 [Priva 設定](priva-settings.md)中檢視包含的標籤，並為您的組織設定自訂標籤。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用主體許可權要求建立精靈

1. 在 [Microsoft Purview 合規性入口網站](https://compliance.microsoft.com/)中，移至 [Priva] 區段，然後選取 **[Priva Subject Rights Requests]**。
1. 若要啟動新的要求，請選取 **[建立要求]**。
1. 識別提出要求的資料主體，並指定其與貴公司的關係。
1. 我們將針對與資料主體相關的專案執行預設搜尋。 如果您想要在我們擷取資料之前先精簡搜尋或取得估計值，您可以在這個階段進行這些選擇。 您也可以將所有專案保留空白，並移至下一個步驟。 如需選項的詳細資訊，請參閱 [定義搜尋設定](#define-search-settings) 和 [精簡搜尋](#refine-your-search)。
1. 根據資料主體希望您使用其資料執行的動作，選擇要求類型。 如果他們的要求與特定資料隱私權規定有關，您也可以從提供的清單中選取它，以新增更多內容。 設定期限 (必要) 可讓您輕鬆排序接近或逾期的要求，並及時解決這些要求。 要求類型包括：
   - **存取**：提供貴組織在Microsoft 365中保存的資料主體個人資訊摘要。
   - **匯出**：提供資料主體個人資訊的摘要和匯出，如檢閱期間所收集和標注。
   - **已標記的待處理清單**：產生使用者在檢閱期間標記的任何檔案摘要，這些檔案可能需要在 Priva 以外執行其他動作。 例如，您可能需要協助刪除每個要求的資料主體個人資訊。 主體許可權要求的自訂資料檢閱標籤可在全域設定中管理 **。**
1. 確認此要求的名稱，並新增選擇性描述以供參考。
1. 檢閱您在先前步驟中輸入的內容摘要。 在您選取 [ **建立要求**] 之前，可以編輯任何欄位。

針對每個主體許可權要求，您可以設定搜尋，以在 Exchange 和 Sharepoint 內的所有或特定位置中尋找資料。 將切換開關移至 [ **開啟** ] 位置，以選擇位置。 您可以選擇搜尋所有帳戶和網站，或指定每個位置內的特定帳戶或網站。 請參閱下方有關每個位置所涵蓋內容的詳細資料。

- **Exchange**：此選項會在Exchange信箱中，以及在個別或群組Teams聊天中尋找資料。 您可以選擇搜尋組織中的所有Exchange帳戶，或選取 [**選擇帳戶**] 從 **[Exchange信箱**] 飛出視窗窗格中選取個別使用者。

- **SharePoint**：此選項會在SharePoint網站、商務用 OneDrive網站和Teams通道中尋找資料。 您可以選擇搜尋組織中的所有SharePoint網站，或選取 [**選擇網站**] 從 **[SharePoint 網站**] 飛出視窗窗格中選取個別使用者。

如需識別適當搜尋字詞的說明，請參閱下列主題：

- **SharePoint網站和 URL**：[在SharePoint系統管理中心管理網站](/sharepoint/manage-sites-in-new-admin-center)提供如何排序和篩選網站，以及如何搜尋SharePoint網站的指引。 使用此選項來尋找要在 [**SharePoint 網站**] 飛出視窗窗格的搜尋欄位中輸入的 URL。

- **Teams聊天和頻道**：[Get-Team](/powershell/module/teams/get-team)會示範如何藉由提供特定屬性或資訊，在Microsoft Teams中尋找小組。

- **OneDrive網站和 URL**：[關於OneDrive URL](/onedrive/list-onedrive-urls#about-onedrive-urls)會提供使用者OneDrive URL 之適當格式和屬性的相關資訊。 使用此選項可協助您識別搜尋中OneDrive網站。

建議您仔細檢閱您的選取專案，以確保您識別出正確的資料主體。 例如，如果您依名稱搜尋信箱，並尋找多個具有類似名稱的個人，請先確認正確的名稱，再將它們新增至您的要求。

## <a name="define-search-settings"></a>定義搜尋設定

當您建立主體許可權要求時，預設搜尋會根據您在建立精靈 [ **位置** ] 頁面上的選取專案執行。 如果您想要進行更具目標的搜尋，或如果您想要在擷取內容專案之前選擇取得資料的估計值，您可以在要求建立精靈的 [ **搜尋設定** ] 頁面上進行這些選擇。

### <a name="advanced-search-options"></a>進階搜尋選項

- **精簡搜尋**：此選項可讓您指定其他屬性，以協助識別組織資料中的資料主體。 選擇此選項之後，系統會提示您新增更多搜尋參數，如下列 [精簡搜尋](#refine-your-search)中所述。
- **包含資料主體所撰寫的內容**：此選項會尋找資料主體所撰寫的內容。 範例包括由資料主體建立或上傳至SharePoint者所建立的檔案。 選取此選項可能會大幅增加傳回的資料量。
- **包含所有版本的專案**：如果您選取SharePoint作為搜尋位置，預設搜尋查詢只會傳回目前版本的SharePoint專案。 核取此方塊會傳回目前和所有舊版的SharePoint專案，產生大量資料供您檢閱。

### <a name="data-estimate"></a>資料估計

[ **取得預估第一個** ] 選項會顯示在自動擷取資料之前，預期會找到多少資料的估計值。 當您的估計值顯示在要求的詳細資料頁面上時，您可以選擇檢視搜尋結果，並預覽已探索到專案的取樣。 如果專案代表預期的結果，您必須選取 [ **擷取資料** ]，才能繼續實際擷取內容專案。

## <a name="refine-your-search"></a>精簡您的搜尋

如果您在 [**搜尋設定**] 頁面上選擇 **[精簡搜尋**]，當您選取 [**下一步**] 時，系統會提示您提供個人屬性和條件的詳細資料，以進一步以搜尋結果為目標。 您可以在其中一個或兩個類別中進行新增。 當您在本節中完成選取時，要求的資料擷取將會以您的搜尋設定為基礎。

#### <a name="add-personal-attributes"></a>新增個人屬性

在文字欄位中輸入資料主體名稱、昵稱、電子郵件地址和位址的值。 您可以新增其他識別碼，例如出生日期或電話號碼，而文字欄位則支援以分號分隔的多個專案。 當您完成時，請選取 [ **下一步** ] 繼續前往 [ **條件** ] 頁面。

#### <a name="conditions"></a>條件

選取 [ **新增條件]** 按鈕，在一系列條件中選擇，以進一步以搜尋為目標，包括專案名稱、寄件者和收件者名稱、個人資料類型，以及專案是否在組織外部共用。 文字欄位支援以分號分隔的多個專案。 當您完成時，請選取 [ **下一步** ] 以儲存您的搜尋設定和進度至要求類型設定。

## <a name="next-steps"></a>後續步驟

建立要求之後，您會看到它列在您的主體許可權要求頁面上。 若要深入瞭解如何繼續進行檢閱，請參 [閱檢閱資料並針對要求共同作業](subject-rights-requests-data-review.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
