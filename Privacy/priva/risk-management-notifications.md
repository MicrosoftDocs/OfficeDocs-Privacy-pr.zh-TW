---
title: 隱私權風險管理中的使用者通知
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
search.appverid:
- MOE150
- MET150
description: 瞭解如何通知內容擁有者Microsoft Priva 隱私權風險管理找到的原則相符專案，以及如何使用這些電子郵件通知來補救問題。
ms.openlocfilehash: ae02d3bca9c63f8645cd9671628de61d83cb6117
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851648"
---
# <a name="user-notifications-in-privacy-risk-management"></a>隱私權風險管理中的使用者通知

當您在隱私權風險管理中設定原則時，您可以選擇在使用者的動作符合您在原則中設定的條件時通知使用者。 通知有兩種類型：三種原則類型皆可使用的電子郵件，以及出現在Teams中的秘訣，僅適用于資料傳輸原則類型。 當您建立或編輯原則時，您可以決定是否要開啟這些通知、傳送通知的頻率，以及自訂其內容。

傳送通知給使用者可能是協助貴組織達成其隱私權目標的重要元件。 通知的設計目的如下：

- 當使用者的動作可能會將個人資料公開給隱私權風險時，立即讓使用者察覺。
- 直接在電子郵件中提供補救方法，讓使用者可以迅速採取動作來保護有風險的資料。
- 將使用者導向貴組織的隱私權指導方針和最佳做法。

通知使用者目前的潛在問題，並讓他們能夠補救問題並重新整理其技能，可以是強大的工具，可讓您在整個組織中建置健全的資料處理做法。

請檢閱下列各節，以協助您準備和管理原則相符專案的使用者通知。

## <a name="prepare-training-content-for-notifications"></a>準備通知的訓練內容

如果您選擇在偵測到原則相符專案時傳送使用者通知，則需要包含隱私權訓練的連結。 提供貴組織隱私權指導方針的存取權，可讓您讓使用者掌握您自己的最佳做法和原則。 它也可以提供電子郵件中建議補救動作的內容，並協助您的使用者為未來良好的資料管理決策做好準備。

設定原則之前，請決定您想要包含的訓練 URL。 每個原則可以提供一個連結，因此建議您選擇每個案例的特定參考。

## <a name="set-user-email-notifications"></a>設定使用者電子郵件通知

您可以在建立新原則或編輯現有原則時，為所有原則類型設定電子郵件通知。 這些設定可在原則建立精靈的 [ **結果** ] 頁面上找到。 如需完整指示，請造訪 [定義結果：使用者通知和秘訣](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips) 。

> [!NOTE]
> 隱私權風險管理傳送電子郵件通知的整體功能是在Priva **設定** 中控制。 預設會啟用此功能。 即使已在個別原則層級設定通知，關閉此設定也會停止所有電子郵件。 深入瞭解 [使用者通知電子郵件設定](priva-settings.md#user-notification-emails)。

## <a name="send-notifications-in-teams"></a>在 Teams 中傳送通知

針對資料傳輸原則，您可以選擇在偵測到原則相符專案時，讓使用者在安全Teams通道中接收原則提示和建議。 這些秘訣會教育使用者如何負責任地使用個人資料。 提示也會包含相關訓練的連結。

若要深入瞭解如何設定這些通知，請造訪 [定義結果：使用者通知和提示](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips)。

## <a name="preview-and-customize-email-content"></a>預覽和自訂電子郵件內容

當使用者收到有關原則相符專案的電子郵件通知時，他們可以遵循電子郵件中的提示，立即採取更正動作。 例如，如果資料過度使用原則發現個人資料的相符專案可能太廣泛，通知電子郵件會包含內容專案的連結，讓使用者可以檢閱，以及使用者將專案標示為私用或保留其目前存取層級的按鈕。 建議的動作會與每種不同類型的原則相關。

您可以預覽電子郵件內容，並在原則建立或編輯程式中調整此設定時進行自己的變更。 若要預覽和編輯您的通知電子郵件內容，請遵循下列步驟：

1. 啟動 [引導式原則建立程式](risk-management-policies.md#custom-setup-guided-process-to-choose-all-settings)中所述的步驟，以建立或編輯原則。

2. 在程式的 [ **結果** ] 步驟中，選取 [當 **原則相符時傳送通知電子郵件給使用者**] 旁的方塊。

3. 選取 [通知電子郵件] 核取方塊下方顯示的 [ **預覽和編輯通知電子郵件** ] 按鈕。

4. 飛出視窗窗格隨即出現，其中已預先填入預設電子郵件內容的文字欄位。 您可以編輯任何或所有欄位，包括：電子郵件的主旨行、本文標頭、本文內容、隱私權訓練顯示名稱和訓練 URL。電子郵件的預覽位於飛出視窗窗格的底部，它會在您編輯預設文字時變更。 當您滿意電子郵件內容時，請選取 [ **儲存** ] 以儲存您的設定。 若要捨棄預設電子郵件的任何變更，請選取飛出視窗窗格右上角的 **X** 來關閉它，並還原回預設內容。

5. 回到 [ **結果]** 頁面，選取 [ **下一步]**。 繼續進行精靈，當您到達最終的 **[完成]** 頁面時，請檢閱您的設定，然後選取 [ **提交]**。

您的通知設定現在將在此原則中生效。 如果您的原則正在測試，則不會傳送通知。 如果您的原則已開啟，則會傳送通知。 檢視有關 [建立和管理原則的詳細資料](risk-management-policies.md)。


## <a name="legal-disclaimer"></a>法律免責聲明

[Microsoft Priva法律免責聲明](priva-disclaimer.md)
