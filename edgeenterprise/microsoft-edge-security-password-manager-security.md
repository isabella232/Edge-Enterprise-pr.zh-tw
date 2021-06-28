---
title: 'Microsoft Edge 密碼管理員安全性 '
ms.author: v-andreabarr
author: AndreaLBarr
manager: collw
ms.date: 05/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 密碼管理員安全性
ms.openlocfilehash: 830658dd1ff577bfb88be5512c955d556c437bcb
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618082"
---
# <a name="microsoft-edge-password-manager-security"></a>Microsoft Edge 密碼管理員安全性 

本文中的常見問題集說明 Microsoft Edge 內建密碼管理員如何提供使用者密碼的安全性。

> [!Note]
>本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="how-are-passwords-stored-in-microsoft-edge-and-how-safe-is-this-approach"></a>密碼如何儲存在 Microsoft Edge 中，這個方法的安全性如何？

Microsoft Edge 儲存在磁碟上已加密的密碼。 它們使用 AES256 加密，而且加密金鑰會儲存於作業系統 (OS) 存放區域中。 這項技術稱為本機資料加密。 雖然並非所有瀏覽器的資料都經過加密，但密碼、信用卡號碼和 Cookie 等敏感性資料在儲存時會加密。

Microsoft Edge 密碼管理員會加密密碼，以便使用者登入作業系統時才能存取密碼。 即使攻擊者具有系統管理員權限或離線存取權，而且可以存取本機儲存的資料，系統的設計是防止攻擊者取得未登入之使用者的純文字密碼。

解密其他使用者密碼的方法，是該使用者已登入，而攻擊者擁有使用者的密碼，或已入侵網域控制站。

### <a name="about-the-encryption-method"></a>關於加密方法

設定檔的加密金鑰會使用 Chromium OSCrypt 受到保護，並使用下列平台特定的作業系統儲存位置：

- 在 Windows，存放區域是 DPAPI

- 在 Mac 上，存放區域是 Keychain

- 在 Linux 上，存放區域為 Gnome Keyring 或 KWallet

所有這些存放區域會使用以使用者方式執行之部分或所有處理序可存取的金鑰來加密 AES256 金鑰。 這種攻擊向量通常在部落格中被解釋為可能的 '攻擊' 或 '弱點'，這是對瀏覽器威脅模型和安全性狀態的錯誤理解。

不過，實體本機攻擊和惡意程式碼在威脅模型之外，在這種情況下，加密資料會容易受到攻擊。 如果您的電腦受到惡意程式碼感染，攻擊者可以解密瀏覽器的存放區域存取權。 以您的使用者帳戶執行攻擊者的程式碼，可以執行任何您可以執行的事。

## <a name="why-encrypt-data-locally-why-not-store-the-encryption-key-elsewhere-or-make-it-harder-to-obtain"></a>為什麼要在本機加密資料？ 為何不將加密金鑰儲存在其他地方，或讓其難以取得？

網際網路瀏覽器 (包括 Microsoft Edge) 沒有提供防護功能，以保護整個裝置因以使用者身份在電腦上執行惡意程式碼而遭到威脅。 不過，Microsoft Defender SmartScreen 和 OS 層級保護 (如 Windows Defender) 設計來確保裝置一開始就不會遭入侵。

雖然無法防範完全信任的惡意程式碼，但在某些情況下，本機資料加密還是很實用。 例如，如果攻擊者找到從磁碟竊取檔案的方法，但無法執行程式碼，或已竊取未受完整磁碟加密保護的膝上型電腦，則本機資料加密將使竊取者難以取得已儲存的資料。

## <a name="do-you-recommend-storing-passwords-in-microsoft-edge"></a>您是否建議在 Microsoft Edge 中儲存密碼？

仰賴 Microsoft Edge 內建密碼管理員的使用者可以 (也確實) 使用更強大且唯一的密碼，因為他們不需要記住所有密碼並經常輸入密碼。 此外，由於密碼管理員只會自動填入其所屬網站上的密碼，因此使用者不太可能遭到網路釣魚攻擊。

> [!Note]
>產業報告顯示，80% 的線上事件與網路釣魚有關，超過 37% 未受訓練的使用者未通過網路釣魚測試。

Microsoft Edge 密碼管理員方便且容易散佈，有助於提升安全性。 與同步處理結合時，您可以在所有裝置上取得所有密碼，而且每個網站都可以輕鬆使用不同的密碼。 您可以針對每個網站使用不需要記住的長而複雜的密碼，並略過每次輸入複雜字串的麻煩。 密碼管理員的便利性表示網路釣魚攻擊的風險較低。

不過，使用與使用者作業系統登入工作階段相關聯的密碼管理員，也表示在該工作階段中的攻擊者可以立即擷取使用者儲存的所有密碼。 如果沒有從密碼管理員竊取，攻擊者必須追蹤按鍵或監視提交的密碼。

決定是否要使用密碼管理員，取決於評估我們所描述的許多優點，以防範整個裝置遭到入侵的可能性。 針對大部分的威脅模型，建議使用 Microsoft Edge 密碼管理員。

> [!Note]
>如果企業擔心特定密碼遭竊或網站因為密碼遭竊而遭入侵，則應採取其他預防措施。 一些可協助減輕這類事件的有效解決方案是透過 Active Directory、Azure Active Directory 或協力廠商的單一登入 (SSO)。 其他解決方案包括 2FA (例如 [MS Authenticator](/azure/active-directory/user-help/user-help-auth-app-download-install)) 或 [WebAuthN](https://webauthn.guide/)。

## <a name="should-a-password-manager-be-enabled-by-an-organization"></a>組織是否應該啟用密碼管理員？

簡單且容易的答案為：是的，請使用瀏覽器的密碼管理員。

更完整的回應表示深入了解您的威脅模型，因為安全性選項和選擇會因不同的威脅模型而異。 考慮是否要為貴組織啟用密碼管理員時，要考慮的一些相關問題包括：

- 您擔心哪些類型的攻擊者？

- 您的使用者會登入哪些類型的網站？

- 您的使用者是否選取高強度、唯一的密碼？

- 您的使用者帳戶是否受到 2FA 保護？

- 最有可能發生哪種類型的攻擊？

- 如何保護您的企業裝置不受惡意程式碼攻擊？

- 您的使用者對造成不便的個人容忍度如何？

- 考慮資料同步處理的影響。

使用者資料會同步處理至各種使用者裝置，以及組織對自動填入資料同步處理所擁有控制權的數量，考慮使用者資料的安全性非常重要。

資料同步處理和 Microsoft Edge：

- 您可以根據整個組織需要啟用或停用資料同步處理。

- 傳輸中的資料安全性，以及雲端中其餘的資料：所有同步處理的資料在瀏覽器與 Microsoft 伺服器之間傳輸時，都會經由 HTTPS 傳輸加密。 同步處理的資料也會以加密狀態儲存在 Microsoft 伺服器上。 在同步處理之前，會先在裝置上進一步加密敏感性資料類型 ，例如位址和密碼。 如果您使用的是公司或學校帳戶，所有資料類型會先進一步加密，再使用 Microsoft 資訊保護進行同步處理。

## <a name="why-do-microsoft-security-baselines-recommend-disabling-the-password-manager"></a>為什麼 Microsoft 安全性基準建議停用密碼管理員？

Microsoft 安全性小組目前已將入侵企業電腦網路 (導致所有裝置密碼管理員中所有登入資訊遺失) 的蠕蟲影響，視為比入侵單一使用者輸入登入資訊的目標網路釣魚攻擊風險 (較可能但較低影響) 更嚴重。

此評定正在討論之中，並可能會隨著 Microsoft Edge 中新增安全性增強功能而變更。

## <a name="can-malicious-extensions-gain-access-to-passwords"></a>惡意擴充功能可以存取密碼嗎？

具有與頁面互動權限的擴充功能，在本質上可以存取該頁面上的任何東西，包括自動填入的密碼。 同樣地，惡意擴充功能也可以修改表單欄位和網路要求/回應的內容，以盜用目前使用者登入內容授權。

不過，Microsoft Edge 提供一組廣泛的原則，可精細控制已安裝的擴充功能。 若要保護公司資料，使用下表中的原則是必要的。

| 原則 | 標題 |
|-|-|
|[BlockExternalExtensions](/deployedge/microsoft-edge-policies#blockexternalextensions)|封鎖安裝外部擴充功能|
|[ExtensionAllowedTypes](/deployedge/microsoft-edge-policies#extensionallowedtypes)|設定允許的擴充功能類型|
|[ExtensionInstallAllowlist](/deployedge/microsoft-edge-policies#extensioninstallallowlist)|允許安裝特定擴充功能|
|[ExtensionInstallBlocklist](/deployedge/microsoft-edge-policies#extensioninstallblocklist)|控制不能安裝哪些擴充功能|
|[ExtensionInstallForcelist](/deployedge/microsoft-edge-policies#extensioninstallforcelist)|控制哪些擴充功能會以無訊息方式安裝|
|[ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources)|設定擴充功能與使用者指令碼安裝來源|
| [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) |設定擴充功能管理設定 |

## <a name="how-does-the-microsoft-edge-password-manager-compare-with-a-third-party-product"></a>Microsoft Edge 密碼管理員與協力廠商產品相比如何？

下表顯示 Microsoft Edge 密碼管理員與協力廠商密碼管理員的比較。

| 協力廠商密碼管理員 | Microsoft Edge 密碼管理員|
|-|-|
| *伺服器同步處理*。有些產品會將密碼儲存在雲端中，以同步您的所有裝置。 這項功能很實用，但如果雲端服務遭到入侵且您的資料遭到公開，則有風險。 **備註：**  透過在雲端中加密密碼，以及將加密金鑰儲存到您的裝置上，讓攻擊者無法取得金鑰和密碼，就可以減輕風險。| 因為密碼會跨已安裝 Microsoft Edge 的 Windows 裝置同步處理，因此存在雲端暴露的風險。 **備註：**  本文內容涵蓋的資料安全性步驟可減輕此風險。|
| *信任*。 必須信任協力廠商沒有做任何惡意行為，例如將您的密碼傳送給另一方。 **備註：**  可以透過檢閱原始程式碼 (在開放原始碼產品的情況下) 或相信供應商關心他們的聲譽和收入，來減輕此風險。 | **備註：** Microsoft 是一家知名且值得信賴的廠商，在提供企業級安全性和生產力方面擁有數十年的歷史，擁有專為保護您全球密碼所設計的資源。 |
| *供應鏈安全性*。 很難驗證廠商是否擁有安全的供應鏈/建置/發行程序。 |**備註：** Microsoft 擁有強大的內部程式，可確保將原始程式碼的風險降至最低。 |
| *用戶端或帳戶遭到入侵*。如果用戶端裝置或使用者帳戶遭到入侵，攻擊者可以取得密碼。 **備註：** 某些密碼管理員需要使用者輸入未儲存在本機的主密碼來解密密碼，因此可以減輕此風險。主密碼只是部分緩解措施，攻擊者可能在填寫表單欄位時讀取按鍵動作，並在輸入時取得主密碼，或從處理程序記憶體中讀取密碼。。 | **備註：** Microsoft 提供 OS 層級保護，例如 Windows Defender，其設計目的是確保裝置不會從一開始受到入侵。 不過，如果用戶端裝置遭到入侵，攻擊者或許可以解密密碼。 |

> [!Note]
> 協力廠商產品可能會針對其他威脅模型提供防護，但這會以複雜度或易用性為代價。 Microsoft Edge 密碼管理員是專為提供方便且易於使用的密碼管理所設計，IT 系統管理員可以使用群組原則完全控制，而且不需要信任協力廠商。

## <a name="why-doesnt-microsoft-offer-a-master-password-to-protect-the-data"></a>為什麼 Microsoft 沒有提供主密碼來保護資料？

在磁碟上加密瀏覽器密碼時，加密金鑰可供您裝置上的任何程式使用，包括任何在本機執行的惡意程式碼。 即使密碼是由主鍵在「保存庫」中加密，在瀏覽器記憶體空間中載入時，密碼也會被解密，並在您解除鎖定保存庫後收集密碼。

主密碼功能 (自動填入使用者資料之前先驗證使用者) 為更廣泛的威脅降低提供了便利性的取捨。 具體來說，它有助於減少針對潛在惡意程式碼或實體本機攻擊者的資料公開時間。 不過，主密碼並非靈丹妙藥，而本機攻擊者和專用惡意程式碼有各種規避主密碼保護的策略。

> [!Note]
> Microsoft 在自動填入之前，會先確認使用者驗證值，這項功能將在未來版本中新增到 Microsoft Edge。

## <a name="can-using-a-password-manager-impact-my-privacy"></a>使用密碼管理員會影響我的隱私權嗎？

否，如果已採取步驟來保護您儲存密碼的存取權，則不會影響隱私權。

有些廣告客戶使用已知惡意探索，使用已儲存的密碼進行唯一識別及追蹤使用者。 如需詳細資訊，請參閱 [廣告目標正從瀏覽器的密碼管理員提取資料](https://www.theverge.com/2017/12/30/16829804/browser-password-manager-adthink-princeton-research)。 瀏覽器已採取步驟來降低此 [隱私權問題](https://bugs.chromium.org/p/chromium/issues/detail?id=798492)。PasswordValueGatekeeper 類別可用來限制密碼欄位資料的存取權，即使瀏覽器已設定為載入時自動填入。

您可以啟用選擇性的 edge://flags/#fill-on-account-select 功能，輕鬆降低此使用者資訊收集威脅。 此功能只允許在使用者明確選擇認證之後，將密碼新增到表單欄位，這可確保使用者知道誰正在接收其密碼。

## <a name="see-also"></a>另請參閱

[Microsoft Edge 企業登陸頁面](https://www.microsoft.com/edge/business/download)

[Microsoft Edge 如何比 Windows 10 上的商務用 Chrome 更安全](/DeployEdge/ms-edge-security-for-business)
