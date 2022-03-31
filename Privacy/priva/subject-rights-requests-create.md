---
title: 建立主體權力要求
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
description: 瞭解如何在 Microsoft Priva 中建立新的主體權力要求。
ms.openlocfilehash: 9de1047950a556b4456fd4453ea8d860a0a01c38
ms.sourcegitcommit: 16dd1c0320bf1c58ad75edbbe2113fc79013f504
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2022
ms.locfileid: "64404607"
---
# <a name="create-a-subject-rights-request"></a>建立主體權力要求

主旨 rights management 管理員可以透過 Priva 的主要主體權力要求] 頁面來開啟新的要求。 [！附注] 您將會引導您完成尋找資料主體的個人資料，以及開始完成要求的處理常式。

您也可以選擇上載其他材料，讓 Priva 根據正確提供的資料值來識別資料主體。 若要深入瞭解，請參閱 [主體權力要求的資料比對](subject-rights-requests-data-match.md)。

## <a name="request-types"></a>要求類型

Priva 的主體權力要求支援三種不同類型的要求：

1. **Access**：提供組織在 Microsoft 365 中所用之資料主體個人資訊的摘要。

2. **匯出**：提供包含資料主體個人資訊的內容專案摘要和匯出檔案。 當您複查搜尋設定所收集的資料時，這些專案就是已複查及標示為 **包含** 的專案。

3. **後續的加上標記清單**：會產生在資料評審期間所標示的任何檔案摘要，可能需要在 Priva 之外進行其他動作。 例如，您可能需要根據他們的要求來協助刪除資料主體的個人資訊。 您可以在 [ [Priva 設定](priva-settings.md)] 中查看包含的標記，並為您的組織設定自訂標記。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用主題許可權要求建立嚮導

1. 在 [Microsoft 365 合規性中心](https://compliance.microsoft.com/)中，從左側導覽選取 [ **Priva 主體許可權要求**]。

2. 在右上角，選取 [ **建立要求**]。

3. 在 [ **資料主體資訊** ] 頁面上，新增資料主體的名字和姓氏、電子郵件地址、居住的國家/地區，並指定其與貴公司的關聯性。 然後選取 **[下一步]**。

4. 在 [**位置**] 頁面上，選擇您要尋找資料主體個人資料的 Microsoft 365 位置。 取得 [位置設定](#choose-locations)的詳細資料。 當您選擇位置後，請選取 **[下一步]。**

5. 在 [ **搜尋設定** ] 頁面上，您可以變更搜尋設定，以精煉搜尋，並選擇是否要先取得估計，再進行資料檢索。 您不需要選擇此頁面上的任何選項，這會根據您在上一個步驟中所指定的位置，而產生預設搜尋。 如需您在這裡選項的詳細資訊，請參閱 [定義搜尋設定](#define-search-settings)。 在您準備好繼續時，請選取 **[下一步]**。

6. 在 [ **要求類型** ] 頁面上，根據資料主體想要對其資料執行的動作，選擇 [要求類型](#request-types) ： [ **存取**]、[ **匯出**] 或 [已 **標記清單以供追蹤**]。 如果他們的要求與特定的資料隱私權規定有關，您也可以從提供的清單中選取，以新增更多內容。  (必要) 設定期限，可讓您輕鬆地排序臨近或逾期的要求，並及時解決。 完成時，選取 **[下一步]**。

7. 在 **要求名稱** 上，確認或編輯此要求的名稱，並新增參考的選擇性描述。 然後選取 **[下一步]**。

8. 在 [ **檢查和完成]** 頁面上，複查您的選取範圍。 任何區段均可供編輯。 完成後，請選取 [ **建立要求**]。

您的要求會有它自己的詳細資料頁面，並會列在您的主要主題許可權要求頁面上。 在建立要求之後，Priva 會開始尋找與您在指定位置中所提供的資料主體資訊相符的專案。 視您的搜尋範圍而定，在要求的詳細資料頁面上顯示資料預估可能需要數分鐘的時間。

## <a name="choose-locations"></a>選擇位置

針對每個主體權利要求，您可以設定搜尋，以尋找 Exchange 和 Sharepoint 內所有或特定位置中的資料。 將其切換開關移至 [ **開啟** ] 位置，選擇位置。 您可以選擇搜尋所有帳戶和網站，或指定每個位置內的特定帳戶或網站。 請參閱以下詳細資訊，瞭解每個位置涵蓋的內容。

- **Exchange**：此選項會尋找 Exchange 信箱中的資料，以及在個人或群組中 Teams 聊天的資料。 您可以選擇搜尋組織中的所有 Exchange 帳戶，或選取 [**選擇帳戶**]，從 [ **Exchange 信箱**] 浮出] 窗格中選取個別的使用者。

- **SharePoint**：此選項會尋找 SharePoint 網站、商務用 OneDrive 網站及 Teams 通道中的資料。 您可以選擇搜尋組織中的所有 SharePoint 網站，或從 [ **SharePoint 網站**] 飛入窗格中，選取 **[選擇** 要選取個別使用者的網站]。

如需識別適當搜尋字詞的協助，請參閱下列主題：

- **SharePoint 網站與 URLs**：[管理 SharePoint 系統管理中心中的網站](/sharepoint/manage-sites-in-new-admin-center)提供有關如何排序和篩選網站，以及如何搜尋 SharePoint 網站的指導方針。 使用此功能，可在 [ **SharePoint 網站**] 飛入窗格的 [搜尋] 欄位中尋找要輸入的 URLs。

- **Teams 聊天與管道**： [[取得小組](/powershell/module/teams/get-team)] 示範如何透過提供特定屬性或資訊，尋找 Microsoft Teams 中的團隊。

- **OneDrive 網站與 URLs**：[關於 OneDrive URLs](/onedrive/list-onedrive-urls#about-onedrive-urls)提供使用者 OneDrive URL 之正確格式及屬性的相關資訊。 使用此資訊可協助您識別搜尋中 OneDrive 網站。

建議您認真檢查您的選擇，以確保您識別正確的資料主體。 例如，如果您依名稱搜尋信箱，並尋找具有類似名稱的多個使用者，請先確認是否正確，再將其新增至您的要求。

## <a name="define-search-settings"></a>定義搜尋設定

當您建立主體權力要求時，會根據您在 [建立] 嚮導的 [ **位置** ] 頁面上所做的選擇來執行預設搜尋。 如果您想要執行更具針對性的搜尋，或想要選擇在取得內容專案之前先估計資料，您可以在 [要求建立] 嚮導的 [ **搜尋設定** ] 頁面上進行這些選擇。

### <a name="advanced-search-options"></a>高級搜尋選項

- **縮小搜尋**：此選項可讓您指定其他屬性，以協助識別組織資料中的資料主體。 選擇此選項後，系統會提示您新增更多搜尋參數，請在下面說明 [精簡搜尋](#refine-your-search)。
- **包含資料主體所** 製作的內容：此選項會尋找資料主體所創作的內容。 範例包括由資料主體所建立或上傳至 SharePoint 的檔案。 選取此選項時，可能會大幅增加傳回的資料量。
- **包含專案的所有版本**：如果選取 [SharePoint] 做為搜尋位置，預設的搜尋查詢只會傳回目前版本的 SharePoint 專案。 勾選此方塊將會傳回目前及所有先前版本的 SharePoint 專案，因此會產生大量的資料供您審閱。

### <a name="data-estimate"></a>資料預估

[ **取得估計優先** ] 選項，會在自動檢索資料之前，顯示預計要尋找的資料量。 當您估計顯示在要求的 [詳細資料] 頁面上時，您可以選擇查看搜尋結果，並預覽已探索的專案樣本。 如果專案代表預期的結果，則您必須選取 [ **取回資料** ]，以繼續實際的內容專案的檢索。

## <a name="refine-your-search"></a>縮小搜尋

如果您選擇 [**搜尋設定**] 頁面上的 [**縮小搜尋**]，當您選取 **[下一步]** 時，系統會提示您提供個人屬性和條件的詳細資料，以進一步瞄準您的搜尋結果。 您可以在其中一個或兩個類別中進行新增。 當您完成此區段中的選取時，要求的資料檢索會以您的搜尋設定為基礎。

#### <a name="add-personal-attributes"></a>新增個人屬性

在 [資料主體] 的名稱、昵稱、電子郵件地址和位址的文字欄位中輸入值。 您可以新增其他識別碼，例如出生日期或電話號碼，而文字欄位則支援以分號分隔的多個專案。 完成後，請選取 **[下一步]** 繼續進行 [ **條件** ] 頁面。

#### <a name="conditions"></a>條件

選取 [ **新增條件** ] 按鈕，以選擇要進一步瞄準搜尋的條件範圍，包括專案名稱、寄件者和收件者名稱、個人資料類型，以及是否在組織外部共用該專案。 文字欄位支援以分號分隔的多個專案。 當您完成時，選取 **[下一步]** ，以儲存搜尋設定並進行 [要求類型] 設定。

## <a name="next-steps"></a>後續步驟

在您建立要求之後，您會看到它會列在 [主體權力要求] 頁面上。 若要深入瞭解如何繼續進行審閱，請參閱 [查看資料並共同處理要求](subject-rights-requests-data-review.md)。

## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva 法律免責聲明](priva-disclaimer.md)
