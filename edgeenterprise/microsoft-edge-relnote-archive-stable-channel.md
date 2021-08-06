---
title: 封存的 Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 封存的 Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: 662ebb40ce14714365b257a1a6127960df6baf90ecc8106cec5e49f35b9c51ea
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727436"
---
# <a name="archived-release-notes-for-microsoft-edge-stable-channel"></a>封存的 Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。

## <a name="version-88070581-february-25"></a>版本 88.0.705.81：2 月 25 日

修正各種錯誤和效能問題。

## <a name="version-88070574-february-17"></a>版本 88.0.705.74：2 月 17 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-17-2021)。

## <a name="version-88070568-february-11"></a>版本 88.0.705.68：2 月 11 日

修正各種錯誤和效能問題。

## <a name="version-88070563-february-5"></a>版本 88.0.705.63：2 月 5 日

> [!IMPORTANT]
> 此更新包含已由 Chromium 小組報告為已在市面上有惡意探索問題的 [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148)。

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-5-2021)。

## <a name="version-88070562-february-4"></a>版本 88.0.705.62：2 月 4 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-4-2021)。

修正各種錯誤和效能問題。

## <a name="version-88070556-january-28"></a>版本 88.0.705.56：1 月 28 日

修正各種錯誤和效能問題。

## <a name="version-88070553-january-26"></a>版本 88.0.705.53：1 月 26 日

已修正各種錯誤和效能問題。

## <a name="version-88070550-january-21"></a>版本 88.0.705.50: 1 月 21 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#january-21-2021)。

<!--- begin major 88  --->
### <a name="feature-updates"></a>功能更新

- **取代的項目：**

  - 取代 FTP 通訊協定的支援。 已從 Microsoft Edge 移除對舊版 FTP 通訊協定的支援。 嘗試瀏覽至 FTP 連結會造成瀏覽器將作業系統導向開啟外部應用程式以處理 FTP 連結。 或者，IT 系統管理員可以設定 Microsoft Edge，以對仰賴於 FTP 通訊協定的網站使用 IE 模式。
  - 將移除對 Adobe Flash 的支援。 從 Microsoft Edge Beta 版本 88 開始，將會移除 Adobe Flash 功能和支援。 深入了解：[Adobe Flash Player 終止支援的更新 - Microsoft Edge 部落格 (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **驗證：**

  - 單一登入 (SSO) 目前可供下層 Windows 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用。 在下層 Microsoft Windows (7、8.1) 上於 Microsoft Edge 登入的使用者，現在會自動登入已設定為允許使用公司和 Microsoft 帳戶進行單一登入的網站 (例如，bing.com、office.com、msn.com、outlook.com)。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。
  
  - 在採用非 Azure AD Microsoft Edge 設定檔的系統上，使用任何 Windows Azure Active Directory (Azure AD) 帳戶單一登入 (SSO) 至公司網站。 您可以針對未使用公司/學校帳戶登入且並非來賓或私密瀏覽的任何設定檔啟用此功能，並允許在使用該設定檔的作業系統上使用任何登入的公司/學校帳戶。 此功能可在 [設定]****  >  [設定檔]****  >  [設定檔喜好設定]****  >  [對使用此設定檔的公司或學校網站允許單一登入]**** 中設定。
  
    > [!NOTE]
    > 「使用 Microsoft Edge 設定檔的所有 Windows 帳戶的單一登入 (SSO)」是 1 月 21 日版本資訊的更新。

- **結束工作階段的 kiosk 模式選項**。 「結束工作階段」按鈕現在可於 kiosk 模式公開瀏覽體驗中使用。 此功能可確保在 Microsoft Edge 關閉時，瀏覽器資料和設定隨即會刪除。 深入了解 kiosk 模式功能和藍圖，[設定 Microsoft Edge kiosk 模式](./microsoft-edge-configure-kiosk-mode.md)。

- **安全性及隱私權：**

  - 如果在線上洩漏中發現使用者的密碼，就會產生警示。 將對照已知遭入侵認證的儲存庫檢查使用者的密碼，並在發現相符項目時傳送警示給使用者。 若要確保安全性與隱私權，請在針對洩漏認證的資料庫檢查使用者密碼時，對其進行雜湊處理和加密。
  - 自動升級混合內容。 透過 HTTPS 提供的安全頁面可能包含會透過非安全 HTTP 提供的參考影像。 為了改善 Microsoft Edge 88 中的隱私權和安全性，將改為透過 HTTPS 來擷取這些影像。 如果無法透過 HTTPS 取得影像，將無法載入影像。
  - 依網站和最近的活動來檢視網站權限。 從 Microsoft Edge 88 開始，使用者將能更輕鬆地管理網站權限。 他們將可以依網站而不只是依權限類型檢視權限。 此外，我們新增了最近的活動區段，該區段將向使用者顯示對其網站權限的所有最近的變更。
  - 增加瀏覽器 Cookie 的控制項。 從 Microsoft Edge 88 開始，使用者可以刪除第三方 Cookie，而不會影響第一方 Cookie。 使用者也可以依據第一方或第三方篩選其 Cookie，並依名稱、Cookie 數量，以及儲存的資料數量和上次修改時間排序。

- **密碼：**

  - 密碼產生器。 Microsoft Edge 提供內建的強式密碼產生器，可在註冊新帳戶或變更現有密碼時使用。 只要在密碼欄位中尋找瀏覽器建議的密碼下拉式清單，系統就會在選取時自動將其儲存到瀏覽器並跨裝置同步，方便日後使用。
  - 密碼監視器。 當您儲存至瀏覽器的密碼與洩漏認證清單中顯示的密碼一樣時，Microsoft Edge 會通知您並提示您更新密碼。 密碼監視器會代表您掃描相符項目，且預設為啟用。
  - 編輯密碼。 現在，您可以直接在 Microsoft Edge 設定中編輯已儲存的密碼。 每次 Microsoft Edge 更新密碼之後，都可以透過在 [設定] 中編輯儲存的項目輕鬆地將儲存的舊密碼替換為新密碼。 

- **利用啟動加速來改善 Microsoft Edge 啟動速度**。 為了改善 Microsoft Edge 啟動速度，我們開發了名為啟動加速的功能。 啟動加速利用讓 Microsoft Edge 在背景中執行，讓 Microsoft Edge 更快速啟動。 注意：此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

- **生產力：**

  - 使用垂直索引標籤來改善生產力和多工功能。 隨著水平索引標籤數量增加，網站標題會開始被截斷，而索引標籤控制項會隨著索引標籤縮減而失去。 這會中斷使用者工作流程，因為他們會用更多時間來尋找、切換和管理其索引標籤，以及用更少時間在手邊的工作上。 垂直索引標籤可讓使用者將索引標籤移至側面，在其中，垂直對齊的圖示和較長的網站標題可讓您更輕鬆地快速掃描、識別並切換到要開啟的索引標籤。
  - 自動填入生日欄位。 Microsoft Edge 已能透過自動填入使用者資料 (例如地址、名稱、電話號碼等)，來協助您節省在填入表單和線上建立帳戶時的時間和精力。Microsoft Edge 現在支援生日欄位，使用者可以儲存並自動填入。 使用者可以隨時在其設定檔設定中檢視、編輯及刪除此資訊。
  - 歷程記錄中「最近關閉的項目」的增強功能。 最近關閉的項目現在會保持來過去任何瀏覽工作階段 (而不僅僅是上一個工作階段) 的最後 25 個索引標籤和視窗。 使用者可在新的歷程記錄體驗中選取 [最近關閉的]，以查看之前開啟的所有索引標籤。
  - 預設啟用 [Your day at a glance] 功能。 從 Microsoft Edge 版本 88 開始，資訊工作者可受益於新索引標籤頁面 (NTP) 上的智慧生產力功能。 Microsoft Edge 87 使用者也會在 Microsoft Edge 88 發行後的 2 周內體驗這些功能。 我們為使用工作或學校帳戶登入的使用者提供個人化且由 M365 Graph 支援的相關內容。 使用者可以快速瀏覽 [Your day at a glance] 模組，輕鬆追蹤他們的會議與最近的工作，以及快速啟動他們想要使用的應用程式。

- **歷程記錄和開啟的索引標籤同步**。歷程記錄和開啟的索引標籤同步現在可供使用者使用。 啟用這些功能會透過讓使用者的瀏覽歷程記錄和開啟的索引標籤可在所有同步中的裝置上取得，藉此協助使用者從前次離開的位置繼續作業。 我們已更新同步和瀏覽器的歷程記錄原則，因此透過使用 Microsoft Edge，使用者現在於任何裝置上都能保持連線並具生產力。 [深入了解](https://blogs.windows.com/windowsexperience/2021/01/21/this-year-lets-resolve-to-make-the-most-of-our-time-online-and-better-protect-ourselves-from-online-threats/)。

- **PDF：**

  - 書籍檢視 (兩頁) 中的 PDF 文件顯示。 從 Microsoft Edge 版本 88 開始，使用者可以在單頁或雙頁書籍檢視中檢視 PDF 文件。 若要變更檢視，請按一下工具列中的 [頁面檢視]**** 按鈕。
  - PDF 檔案的錨定文字記事支援。 從 Microsoft Edge 版本 87 開始，使用者可以在 PDF 檔案中的任何文字片段上新增輸入的文字記事。

- **字型：**

  - 瀏覽器圖示已更新為 Fluent 設計系統。 隨著我們持續處理瀏覽器中的 Fluent Design，我們已進行變更，以讓圖示與新的 Microsoft 圖示系統對齊。 這些變更會影響我們的許多高接觸的使用者介面，包括可在我們的各種功能表中找到的索引標籤、網址列以及瀏覽和尋路圖示。
  - 改善字型轉譯。 改善文字轉譯，以提高清晰度並減少模糊。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 18 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則。

- [BasicAuthOverHttpEnabled](./microsoft-edge-policies.md#basicauthoverhttpenabled) - 允許 HTTP 的基本驗證。
- [BlockExternalExtensions](./microsoft-edge-policies.md#blockexternalextensions) - 封鎖安裝外部擴充功能。
- [InternetExplorerIntegrationLocalFileAllowed](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileallowed) - 允許在 Internet Explorer 模式中啟動本機檔案。
- [InternetExplorerIntegrationLocalFileExtensionAllowList](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) - 根據副檔名允許清單在 Internet Explorer 模式中開啟本機檔案。
- [InternetExplorerIntegrationLocalFileShowContextMenu](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileshowcontextmenu) - 顯示操作功能表以在 Internet Explorer 模式中開啟連結。
- [IntranetRedirectBehavior](./microsoft-edge-policies.md#intranetredirectbehavior) - 內部網路重新導向行為。
- [PrinterTypeDenyList](./microsoft-edge-policies.md#printertypedenylist) - 停用拒絕清單上的印表機類型。
- [ShowMicrosoftRewards](./microsoft-edge-policies.md#showmicrosoftrewards) - 顯示 Microsoft Rewards 體驗。
- [SleepingTabsEnabled](./microsoft-edge-policies.md#sleepingtabsenabled) - 設定睡眠索引標籤。
- [SleepingTabsTimeout](./microsoft-edge-policies.md#sleepingtabstimeout) - 設定睡眠索引標籤的背景索引標籤無活動逾時。
- [SleepingTabsBlockedForUrls](./microsoft-edge-policies.md#sleepingtabsblockedforurls) - 對特定網站封鎖睡眠索引標籤。
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - 啟用啟動加速。
- [TargetBlankImpliesNoOpener](./microsoft-edge-policies.md#targetblankimpliesnoopener) - 不对指向 _blank 的链接設定 window.opener。
- [UpdatePolicyOverride](./microsoft-edge-policies.md#updatepolicyoverride) - 指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。
- [VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) - 設定瀏覽器側邊上索引標籤垂直版面配置的可用性。
- [WebRtcAllowLegacyTLSProtocols](./microsoft-edge-policies.md#webrtcallowlegacytlsprotocols) - 在 WebRTC 中允許舊版 TLS/DTLS 降級。
- [WebWidgetAllowed](./microsoft-edge-policies.md#webwidgetallowed) - 啟用 Web 小工具。
- [WebWidgetIsEnabledOnStartup](./microsoft-edge-policies.md#webwidgetisenabledonstartup) - 在 Windows 啟動時允許 Web 小工具。

#### <a name="deprecated-policies"></a>取代的原則

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - 啟用主動式驗證。
- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist) - 啟用主動式驗證。
- [ProxyMode](./microsoft-edge-policies.md#proxymode) - 設定 Proxy 伺服器設定。
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl) - 設定 Proxy .pac 檔案 URL。
- [ProxyServer](./microsoft-edge-policies.md#proxyserver) - 設定 Proxy 伺服器的位址或 URL。
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容原則。

### <a name="obsoleted-policies"></a>已過時的原則

- [AllowPopsDuringPageUnload](./microsoft-edge-policies.md#allowpopupsduringpageunload) - 允許在卸載網頁期間顯示快顯視窗。
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) - 預設 Adobe Flash 設定。
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls) - 允許特定網站上的 Adobe Flash 外掛程式。
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls) - 封鎖特定網站上的 Adobe Flash 外掛程式。
- [RunAllFlashInAllowMode](./microsoft-edge-policies.md#runallflashinallowmode) - 將 Adobe Flash 內容設定延伸至所有內容。
<!--- end major 88  --->
## <a name="version-87066475-january-7"></a>版本 87.0.664.75：1 月 7 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#january-7-2021)。

## <a name="version-87066466-december-17"></a>版本 87.0.664.66：12 月 17 日

修正各種錯誤和效能問題。

## <a name="version-87066460-december-10"></a>版本 87.0.664.60：12 月 10 日

修正各種錯誤和效能問題。

## <a name="version-87066457-december-7"></a>版本 87.0.664.57：12 月 7 日

修正各種錯誤和效能問題。 穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#december-7-2020)。

## <a name="version-87066455-december-3"></a>版本 87.0.664.55：12 月 3 日

修正各種錯誤和效能問題。 下列功能已針對此版本進行更新。

- **預設會啟用 [購物] 功能**。 從 Microsoft Edge 版本 87 開始，企業使用者可以利用 Microsoft Edge 中的購物功能。 有了購物功能，Microsoft Edge 可協助使用者在線上購物時找到優待卷及更好的價格。 (優待券體驗已隨著穩定版本 87.0.664.41 推出。) 價格比較體驗現在隨著此更新提供。 此功能可使用 [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) 原則設定。 請參閱我們的[部落格](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/)和[深入了解](/microsoft-edge/privacy-whitepaper#shopping) Microsoft 購物的相關資訊。

## <a name="version-87066452-november-30"></a>版本 87.0.664.52：11 月 30 日

修正各種錯誤和效能問題。

## <a name="version-87066447-november-23"></a>版本 87.0.664.47：11 月 23 日

修正各種錯誤和效能問題。

<!-- begin major 87 --->
## <a name="version-87066441-november-19"></a>版本 87.0.664.41：11 月 19 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#november-19-2020)。

### <a name="feature-updates"></a>功能更新

- **自動將不相容網站從 Internet Explorer 重新導向至 Microsoft Edge**。 從 Microsoft Edge 87 穩定版更新開始，在 Internet Explorer 上顯示不相容訊息的公共網站，將自動重新導向至 Microsoft Edge。 若要深入了解及設定此體驗，請參閱[重新導向不相容的網站](./edge-learnmore-neededge.md)。

- **kiosk 模式隱私權功能已啟用**。 從 Microsoft Edge 版本 87 開始，有助於企業處理使用者資料隱私權的 kiosk 模式功能將會啟用。 這些功能將啟用一些體驗, 例如在退出時清除使用者資料、刪除下載的檔案，以及在指定的閒置時間後, 重設已設定的啟動體驗。 深入了解如何[設定 Microsoft Edge kiosk 模式](./microsoft-edge-configure-kiosk-mode.md)

- **依預設啟用購物功能**。 從 Microsoft Edge 版本 87 開始，企業使用者也可以透過在 Edge 中購物獲益。 利用購物功能，Microsoft Edge 可在使用者於線上購物時，協助使用者找到優待券和更優惠的價格。 我們隨著此更新提供優待券體驗，而價格比較將於 Microsoft Edge 87 近期的更新中發佈。 此功能可透過 [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) 原則設定。 請參閱我們的[部落格](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/)和[深入了解](/microsoft-edge/privacy-whitepaper#shopping) Microsoft 購物的相關資訊。

- **預設啟用 ClickOnce 部署**。 預設會在 Microsoft Edge 87 中啟用 ClickOnce，這樣可減少企業部署軟體的障礙，並更能與舊版Microsoft Edge Legacy 瀏覽器行為一致。 從 Microsoft Edge 87 開始，ClickOnceEnabled 原則的 “未設定”狀態將反映已啟用的新預設 ClickOnce 狀態 (與之前停用的預設狀態相比)。

- **企業版的新標籤頁 (NTP) 將生產力與且可自訂的工作相關的摘要內容整合在一起**。 企業版 NTP 加入Microsoft Office 365 生產力頁面, 我們提供在公司或學校帳戶登入的使用者, 有其個人化的個人化及與公司及產業相關的資料來源, 並能組織在同一個頁面中. 使用者將能夠辨識熟悉的 Office 365 內容，以及由 Bing 提供支援的商務用 Microsoft 搜尋。 此外，他們可以從組織的可用內容和模組選擇最相關的內容，以輕鬆自訂 [我的摘要]。 IT 系統管理員可以控制其組織的新聞摘要設定，包括為 Microsoft Edge 新索引標籤頁面選取的產業 (移至 Microsoft 365 系統管理中心)。 [深入了解](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **隱私權與安全性：**

  - 支援政策設定網站的 TLS Token Binding 權杖綁定。 TLS Token binding 權杖綁定可協助防止權杖被竊取攻擊，以確保無法從最初設定cookie的設備以外的其他設備重複使用。 使用 TLS 權杖綁定需設定 [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) 規定，並要求列出的網站支援這項功能。

- **鍵盤支持PDF 檔案上的螢光筆功能**. 使用者可以使用鍵盤鍵來醒目提示 PDF 中的任何文字。

- **列印:**

  - 選擇雙面列印時要翻轉的那一面。 當雙面列印時，使用者可以選擇在紙張的長邊或短邊翻轉。
  - 選擇企業的列印光柵化模式。 控制將Microsoft Edge 列印到一個 Windows 上的非PostScript 印表機。 有時需將非 PostScript 印表機上的列印工作光柵化才能正確列印。 列印選項為「完全」和「快速」。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 10 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則。

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) - 設定從 Microsoft Edge 複製的 URL 的預設貼上格式，並決定使用者是否可以使用其他格式。
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - 已啟用在 Microsoft Edge 中購物。
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) - 隱藏一次性的重新導向對話方塊和 Microsoft Edge 上的橫幅。
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) -設定位址欄編輯以給 kiosk 模式有公眾流覽體驗。
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - 當 Microsoft Edge 關閉時，刪除隨著 kiosk 工作階段下載的檔案。
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) - 啟用顯示密碼按鈕。
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) - 防止安裝瀏覽器協助程式物件 (BHO)，以將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) - 將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) - 設定語音辨識。
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) - 啟用 Microsoft Edge 中的 Web 擷取功能。

#### <a name="deprecated-policy"></a>取代的原則

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) -設定 Microsoft Edge 新增索引標籤頁面體驗。

#### <a name="obsoleted-policy"></a>淘汰的原則

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) - 在限定時間內重新啟用已取代的網頁平台功能。

<!-- end major 87 -->

## <a name="version-86062269-november-13"></a>版本 86.0.622.69：11 月 13 日

> [!IMPORTANT]
> 此更新包含已由 Chromium 小組報告為已在市面上有惡意探索問題的 [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) 以及 [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017)。

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#november-13-2020)。

## <a name="version-86062268-november-11"></a>版本 86.0.622.68：11 月 11 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#november-11-2020)

## <a name="version-86062263-november-4"></a>版本 86.0.622.63：11 月 4 日

> [!IMPORTANT]
> 此更新包含已由 Chromium 小組報告為已在市面上有惡意探索問題的 [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009)。

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#november-4-2020)。

## <a name="version-86062261-november-2"></a>版本 86.0.622.61：11 月 2 日

修正各種錯誤和效能問題。

## <a name="version-86062258-october-29"></a>版本 86.0.622.58：10 月 29 日

修正各種錯誤和效能問題。

## <a name="version-86062256-october-27"></a>版本 86.0.622.56：10 月 27 日

修正各種錯誤和效能問題。

## <a name="version-86062251-october-22"></a>版本 86.0.622.51：10 月 22 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#october-22-2020)

## <a name="version-86062248-october-20"></a>版本 86.0.622.48：10 月 20 日

修正各種錯誤和效能問題。

## <a name="version-86062243-october-15"></a>版本 86.0.622.43：10 月 15 日

修正各種錯誤和效能問題。

## <a name="version-86062238-october-9"></a>版本 86.0.622.38：10 月 9 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#october-9-2020)

### <a name="feature-updates"></a>功能更新

* **復原為上一個 Microsoft Edge 版本。** 如果最新版本的 Microsoft Edge 有問題，復原功能可讓系統管理員還原為已知良好的 Microsoft Edge 版本。 **注意：** 穩定版本 86.0.622.38 是您可以復原的第一個版本，這表示穩定版本 87 是準備好要回復的第一個版本。 [進一步了解](edge-learnmore-rollback.md)。

* **預設會在整個企業強制啟用同步。**  系統管理員可以使用 [ForceSync](./microsoft-edge-policies.md#forcesync) 原則，預設為 Azure Active Directory (Azure AD) 帳戶啟用同步。

* **在 Windows 7 和 8.1 上自動切換設定檔。** 目前在 Windows 10 版 Microsoft Edge 中提供的自動設定檔切換功能已延伸至舊版 Windows (Windows 7 和 8.1)。 如需詳細資訊，請參閱[自動設定檔切換](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)部落格文章。

* **根據預設 SameSite=Lax Cookie**。 為了改善網頁安全性和隱私權，根據預設會預設 cookie 為[SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)。 這表示 cookie 只會在第一方的上下文中傳送，對於發傳送第三方的要求將被忽略。 這項變更可能會對需要第三方資源的 cookie 才能正常運作的網站造成相容性影響。 若要允許使用這類 cookie，網頁程式開發人員可以標示 cookie，在設定 cookie 時，只要新增清楚的 `SameSite=none` 和 `Secure` 屬性，就能將該 cookie 設定並傳送到第三方上下文。 如果企業希望讓特定網站免于此變更，可以使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) 原則以達成，或可以使用 [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) 原則，以退出所有網站的變更。

* **移除 HTML5 應用程式快取 API。**  從 Microsoft Edge 版本 86 開始，可啟用離線使用網頁的舊版應用程式快取 API 會從 Microsoft Edge 中移除。 Web 開發人員應該檢閱 [WebDev 文件](https://web.dev/appcache-removal/)，以取得有關將應用程式快取 API 取代為服務工作者的資訊。  重要：您可以要求 [AppCache OriginTrial 權杖](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673)，允許網站在 Microsoft Edge 版本 90 之前繼續使用已取代的應用程式快取 API。

* **隱私權與安全性：**

  * 針對舊版 Windows 和 macOS 取代 [MetricsReportingEnabled](/DeployEdge/microsoft-edge-policies#metricsreportingenabled) 和 [SendSiteInformationToImproveServices](/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) 原則。 這些原則已在 Microsoft Edge 版本 86 中取代，並將於 Microsoft Edge 版本 89 中變得過時。<br>
這些原則會在 Windows 10 上由 [允許遙測][](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 取代，而新的 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則則用於所有其他平台。 這可讓使用者管理傳送至 Microsoft 的 Windows 7、8、8.1 和 macOS 診斷資料。
  * 安全 DNS (DNS-over-HTTPS) 支援。  從 Microsoft Edge 版本 86 開始，用來控制未受管理裝置上安全 DNS 的設定可供使用。 這些設定無法供受管理裝置上的使用者存取，但是 IT 系統管理員可以使用 [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) 群組原則來啟用或停用安全 DNS。

* **Internet Explorer 模式：** 讓使用者使用 Microsoft Edge 使用者介面 (UI) 在 Internet Explorer 模式中測試網站。 從 Microsoft Edge 版本 86 開始，系統管理員可以啟用一個 UI 選項，讓其使用者可以在 Internet Explorer 模式中載入索引標籤，以用於測試目的或做為權宜之計，直到將網站新增至網站清單 XML 為止。

* **PDF 更新：**

  * PDF 文件的目錄。 從版本 86 開始，Microsoft Edge 已新增對目錄的支援，讓使用者能輕鬆瀏覽 PDF 文件。
  * 在小型板型規格螢幕上存取所有 PDF 功能。 在使用小型螢幕的裝置上存取 Microsoft Edge PDF 閱讀程式的所有功能。
  * PDF 檔案上螢光筆的手寫筆支援。 透過此更新，使用者可以使用數位筆直接在 PDF 檔案上將文字醒目提示，就像使用實體螢光筆和紙張的方式一樣。
  * 改善 PDF 捲動。 您現在可以在瀏覽長篇的 PDF 文件時，體驗不間斷的捲動。

* **當使用者開始在 Microsoft Edge 附加元件網站上輸入搜尋查詢時，他們會看到自動完成建議。** 「自動完成」可協助使用者快速完成其搜尋查詢，而不需要輸入整個字串。 這將很有幫助，因為使用者不需要記住正確的拼寫，而他們可以從所顯示的可用選項中選擇。

* **使用群組原則將自訂影像新增至新的索引標籤頁面 (NTP)。** 從 Microsoft Edge 版本 86 開始，NTP 提供一個選項，可將預設影像以自訂使用者提供的影像取代。 群組原則也支援管理此影像屬性的功能。

* **讓自訂鍵盤快速鍵符合 VS 程式碼。** Microsoft Edge 開發工具現在支援自訂開發工具中的鍵盤快速鍵，使其符合您的編輯器/IDE。 (在 Microsoft Edge 84 中，我們新增了比對開發工具鍵盤快速鍵與 VS Code 的功能。)

* **使用下載管理員來刪除磁碟上的下載項目。** 使用者現在可以在不離開瀏覽器的情況下，從磁碟中刪除其下載的檔案。 在下載架子或下載頁面的操作功能表中，有新的 [刪除下載] 功能。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 23 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - 封鎖集錦中服務和匯出目標特定清單的存取權。
- [DefaultFileSystemReadGuardSetting](./microsoft-edge-policies.md#defaultfilesystemreadguardsetting) - 控制檔案系统 API 的讀取使用。
- [DefaultFileSystemWriteGuardSetting](./microsoft-edge-policies.md#defaultfilesystemwriteguardsetting) - 控制檔案系統 API 的寫入使用。
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - 預設的感應器設定。
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - 控制 Serial API 的使用方式。
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - 傳送關於瀏覽器使用狀況的必要和選擇性診斷資料。
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - 允許存取 Enterprise Mode Site List Manager 工具。
- [FileSystemReadAskForUrls](./microsoft-edge-policies.md#filesystemreadaskforurls) - 允許透過這些網站上的檔案系統 API 讀取存取權。
- [FileSystemReadBlockedForUrls](./microsoft-edge-policies.md#filesystemreadblockedforurls) - 封鎖透過這些網站上的檔案系統 API 讀取存取權。
- [FileSystemWriteAskForUrls](./microsoft-edge-policies.md#filesystemwriteaskforurls) - 允許這些網站上的檔案和目錄的寫入存取權。
- [FileSystemWriteBlockedForUrls](./microsoft-edge-policies.md#filesystemwriteblockedforurls) - 封鎖這些網站上的檔案和目錄的寫入存取權。
- [ForceSync](./microsoft-edge-policies.md#forcesync) - 強制同步處理瀏覽器資料，且不顯示同步同意提示。
- [InsecureFormsWarningsEnabled](./microsoft-edge-policies.md#insecureformswarningsenabled) - 啟用不安全表單的警告。
- [InternetExplorerIntegrationTestingAllowed](./microsoft-edge-policies.md#internetexplorerintegrationtestingallowed) - 允許 Internet Explorer 模式測試。
- [SpotlightExperiencesAndRecommendationsEnabled](./microsoft-edge-policies.md#spotlightexperiencesandrecommendationsenabled) - 選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知以及 Microsoft 服務的提示。
- [NewTabPageAllowedBackgroundTypes](./microsoft-edge-policies.md#newtabpageallowedbackgroundtypes) - 設定新的索引標籤頁面版面配置所允許的背景類型。
- [SaveCookiesOnExit](./microsoft-edge-policies.md#savecookiesonexit) - 在 Microsoft Edge 關閉時儲存 Cookie。
- [SensorsAllowedForUrls](./microsoft-edge-policies.md#sensorsallowedforurls) - 允許存取特定網站上的感應器。
- [SensorsBlockedForUrls](./microsoft-edge-policies.md#sensorsblockedforurls) - 封鎖存取特定網站上的感應器。
- [SerialAskForUrls](./microsoft-edge-policies.md#serialaskforurls) - 允許特定網站上的 Serial API。
- [SerialBlockedForUrls](./microsoft-edge-policies.md#serialblockedforurls) - 封鎖特定網站上的 Serial API。
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - 啟用使用者代理程式用戶端提示功能。
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - 限制保留的使用者資料快照數量，以便在緊急復原時使用。

#### <a name="deprecated-policies"></a>取代的原則

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。

#### <a name="obsoleted-policy"></a>淘汰的原則

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。

## <a name="version-85056470-october-6"></a>版本 85.0.564.70：10 月 6 日

修正各種錯誤和效能問題。

## <a name="version-85056468-october-1"></a>版本 85.0.564.68：10 月 1 日

修正各種錯誤和效能問題。

## <a name="version-85056463-september-23"></a>版本 85.0.564.63：9 月 23 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#september-23-2020)

## <a name="version-85056451-september-9"></a>版本 85.0.564.51：9 月 9 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#september-9-2020)

## <a name="version-85056444-august-31"></a>版本 85.0.564.44：8 月 31 日

修正各種錯誤和效能問題。

<!-- 85.0.564.41: August 27 -->

## <a name="version-85056441-august-27"></a>版本 85.0.564,41: 8 月 27 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#august-27-2020)

### <a name="feature-updates"></a>功能更新

- **我的最愛和設定的內部部署同步**。 您現在可以在自己的環境中，在 Active Directory 設定檔之間同步處理瀏覽器的我的最愛和設定，不需要進行雲端同步處理。

- **使用 Microsoft Edge 群組原則支援，無需確認提示即可啟動信任網站 + 無需確認即可啟動的應用程式組合。** 已添加的群組原則支援允許管理員添加受信任的網站 + 應用程式組合，無需確認提示即可啟動。 這添加了一項功能，讓管理員為其使用者設定信任通訊協定/原點組合（例如 Microsoft 365 應用程式），從而在瀏覽到包含應用協定的 URL 時禁止確認提示。

- **PDF 螢光筆工具**。 此工具可添加到 PDF 工具列中，方便醒目顯示重要文字。

- **儲存訪問 API 現可用**。 當使用者直接指示允許本來會被流覽器的當前設定阻止的儲存時，可使用此儲存訪問 API 來存取協力廠商內容中的第一方儲存。 如需詳細資訊，請參閱[儲存體存取 API](https://www.chromestatus.com/feature/5612590694662144)。

- **Microsoft Edge 集合現可使用“傳送至 OneNote” **。 所有人都期待能將集合中已收集的資訊傳送至 OneNote，從而追加資訊到更大的專案中，與他人進行協作！ 更重要的是，在 Microsoft Edge 85 中，您能夠將 Microsoft 帳戶和 Azure Active Directory 的內容傳送到 *Mac 版 Office*產品 (Word、Excel 和 OneNote)。

- **開發工具更新**。 如需以下更新的詳細資訊，請參閱 [開發工具新增功能 (Microsoft Edge 85)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools)。

   - Microsoft Edge 開發工具支援 Surface Duo 模擬。 Microsoft Edge 開發工具能夠模擬 Surface Duo，因此可測試 Web 內容在雙屏裝置上的顯示效果。 若要在開發工具中打開此實驗，請在 Windows 上按 Ctrl+Shift+M 或在 macOS 上按 Command+Shift+M 來輸入裝置模式，然後在裝置下拉式清單中選取 Surface Duo。
   - Microsoft Edge 開發工具允許鍵盤快速鍵和 VS Code 相匹配。 Microsoft Edge 開發工具支援自訂開發工具中的鍵盤快速鍵，使其匹配你的編輯器/IDE。 在 Microsoft Edge 85 中，我們添加了匹配開發工具鍵盤快速鍵和 VS Code 的功能。 此變更將有助於增加 VS Code 和開發工具之間的工作效率。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 13 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

- [AutoLaunchProtocolsFromOrigins](./microsoft-edge-policies.md#autolaunchprotocolsfromorigins) - 定義可從列出的源啟動外部應用程式的協定的清單，而無需提示用戶。
- [AutoOpenAllowedForURLs](./microsoft-edge-policies.md#autoopenallowedforurls) - AutoOpenFileTypes 可套用的 URL。
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes) - 檔案類型清單應在下載時自動開啟。
- [DefaultSearchProviderContextMenuAccessAllowed](./microsoft-edge-policies.md#defaultsearchprovidercontextmenuaccessallowed) - 允許預設搜尋提供程式中的操作功能表搜尋訪問。
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors) - 允許由本機信賴起點頒發的 SHA - 1 簽章憑證。
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](./microsoft-edge-policies.md#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告。
- [IntensiveWakeUpThrottlingEnabled](./microsoft-edge-policies.md#intensivewakeupthrottlingenabled) - 控制 IntensiveWakeUpThrottling 功能。
- [NewTabPagePrerenderEnabled](./microsoft-edge-policies.md#newtabpageprerenderenabled) - 啟用預先載入的新索引標籤頁面，以加快頁面呈現速度。
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox) - 設定新的索引標籤頁面搜尋體驗。
- [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) - 允許使用者在密碼不安全時收到警示提醒。
- [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) - 啟用 Microsoft Edge 設定檔資料的快取副本。
- [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) - 設定快取設定檔目錄。
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - 指定停用的 TLS 加密套件。

#### <a name="obsoleted-policies"></a>淘汰的原則

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載。
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- 允許 WebDriver 覆寫不相容原則。

## <a name="version-84052263-august-20"></a>版本 84.0.522.63：8 月 20 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#august-20-2020)。

## <a name="version-84052261-august-17"></a>版本 84.0.522.61：8 月 17 日

修正各種錯誤和效能問題。

## <a name="version-84052259-august-11"></a>版本 84.0.522.59：8 月 11 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#august-11-2020)

## <a name="version-84052258-august-10"></a>版本 84.0.522.58：8 月 10 日

修正各種錯誤和效能問題。

## <a name="version-84052252-august-1"></a>版本 84.0.522.52：8 月 1 日

修正各種錯誤和效能問題。

## <a name="version-84052250-july-31"></a>版本84.0.522.50：7月31日

修正各種錯誤和效能問題。

## <a name="version-84052249-july-29"></a>版本 84.0.522.49：7 月 29 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#july-29-2020)

## <a name="version-84052248-july-28"></a>版本 84.0.522.48：7 月 28 日

修正各種錯誤和效能問題。

## <a name="version-84052244-july-23"></a>版本 84.0.522.44：7 月 23 日

已修正各種錯誤和效能問題。

## <a name="version-84052240-july-16"></a>版本 84.0.522.40：7 月 16 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#july-16-2020)

### <a name="feature-updates"></a>功能更新

- 此版本的 Microsoft Edge 可提升 Internet Explorer 模式的網站清單下載時間。 在沒有快取網站清單的情況下，我們將 Internet Explorer 模式網站清單的下載延遲縮短到 0 秒 (從 60 秒等候時間往下縮短)。 如果在下載網站清單之前，Internet Explorer 模式首頁瀏覽需要延遲，我們也新增了針對此案例的群組原則支援。 如需詳細資訊，請參閱 [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) 原則。

- Microsoft Edge 現在可讓使用者在 Windows 10 上「以系統管理員身分執行」登入瀏覽器。 這可協助客戶在 Windows 伺服器上，或在遠端桌面和沙箱案例中執行 Microsoft Edge。

- Microsoft Edge 目前提供全螢幕模式的完整滑鼠支援。 現在，您可以使用滑鼠存取索引標籤、網址列及其他項目，而不需退出全螢幕模式。

- 改善線上購買。 將自訂暱稱新增至儲存的轉帳卡或信用卡。 現在您可以在線上購買時，辨別並區別您的信用卡。 設定轉帳卡或信用卡的暱稱，這樣當您使用 [自動填滿] 來選取付款方式時，就可以選擇正確的卡片。

- 預設會停用 TLS/1.0 和 TLS/1.1。  [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) 原則允許重新啟用 TLS/1.0 和 TLS/1.1。 至少到 Microsoft Edge 版本 88 都還可以使用此原則。 如需詳細資訊，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。

- 集錦改善功能：

  - 新增附註功能，可讓您針對集錦中的項目新增附註或註解。 即使您排序集錦中的項目，附註也會組成群組並持續附加到項目中。 若要嘗試這項新功能，請以滑鼠右鍵按一下項目，然後選取 [新增附註]。
  - 您可以變更集錦中的附註背景色彩。 您可以使用色彩編碼來協助您整理資訊和提高生產力。
  - 提供顯著的效能增強功能，可讓您將集錦匯出至 Excel，比起前版 Microsoft Edge 來的更省時。

- 其他 Microsoft Edge API 支援：

  - 已啟用儲存體存取 API 來進行試驗。 此功能會為家用版使用者和企業使用者啟用，並將 [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) 原則設定為 "Full"。 此功能預設會為 Microsoft Edge 穩定通道版本 85 中的所有使用者啟用。
  
    隨著隱私權對使用者的重要性日益增加，對於更嚴格的瀏覽器預設值的要求以及封鎖所有第三方儲存空間存取權等使用者選擇設定越來越普遍。 雖然這些設定可協助改善隱私權，並封鎖未知或不受信任方進行非必要的存取，但它們可能也會造成不必要的負面影響，例如封鎖使用者可能想要查看之內容的存取權 (例如社交媒體和內嵌媒體內容)。

    當使用者直接允許存取可能會由瀏覽器的目前設定封鎖的儲存體時，儲存體存取 API 會允許在第三方環境中存取第一方儲存體。 如需詳細資訊，請參閱[儲存體存取 API](https://www.chromestatus.com/feature/5612590694662144)。

  - 原生檔案系統 API，代表您可以透過原生檔案系統 API 來授與網站編輯檔案或資料夾的權限。

- PDF 改進功能：

  - PDF 的朗讀功能可讓使用者聆聽 PDF 的內容，並同時執行其他對他們而言重要的工作。 它也可協助視聽學習者專注於閱讀內容，讓學習更輕鬆。
  - 改善 PDF 檔案編輯功能。 現在您可以將對 PDF 的編輯儲存回檔案，而不需要在每次編輯 PDF 時儲存複本。

- Microsoft Edge 現在在沈浸式閱讀程式中啟用翻譯功能。 當使用者開啟沈浸式閱讀程式檢視時，會出現將頁面翻譯成所需語言的選項。

- 有多個 DevTools 更新，包括支援自訂鍵盤快速鍵以比對 VS 程式碼和以高對比檢視 DevTools。  如需詳細資訊，請參閱 [DevTools 的新功能 (Microsoft Edge 84)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools)。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 7 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - 允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態)。
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) - 設定應用程式防護容器 Proxy 的設定。
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - 要求在索引標籤瀏覽前，[企業模式網站清單] 即已可使用。
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled) - 使用 Windows Proxy 解析程式。
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection) - 針對 Internet Explorer 模式設定增強的當機偵測。
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 要降低 CPU 和耗電量，Microsoft Edge 將偵測視窗何時被其他視窗覆蓋，並將暫停工作繪製像素。
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) - 針對 [企業模式網站清單]，設定索引標籤瀏覽逾時延遲。

#### <a name="deprecated-policies"></a>過時的原則

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - 允許頁面在頁面關閉期間傳送同步 XHR 要求。
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - 判斷內建的憑證驗證程式是否將用來驗證伺服器憑證。
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。

#### <a name="obsoleted-policy"></a>已淘汰的原則

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - 強制網路程式碼在瀏覽器處理程序中執行。

<!-- End 84 -->
## <a name="version-83047864-july-13"></a>版本 83.0.478.64：7 月 13 日

修正各種錯誤和效能問題。

## <a name="version-83047861-july-7"></a>版本 83.0.478.61：7 月 7 日

修正各種錯誤和效能問題。

## <a name="version-83047858-june-30"></a>版本 83.0.478.58：6 月 30 日

修正各種錯誤和效能問題。

## <a name="version-83047856-june-24"></a>版本 83.0.478.56：6 月 24 日

修正各種錯誤和效能問題。

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#june-24-2020)

## <a name="version-83047854-june-17"></a>版本 83.0.478.54：6 月 17 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#june-17-2020)

## <a name="version-83047850-june-15"></a>版本 83.0.478.50：6 月 15 日

修正各種錯誤和效能問題。

## <a name="version-83047845-june-4"></a>版本 83.0.478.45：6 月 4 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#june-4-2020)

## <a name="version-83047844-june-1"></a>版本 83.0.478.44：6 月 1 日

修正各種錯誤和效能問題。

## <a name="version-83047837-may-21"></a>版本 83.0.478.37：5 月 21 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#may-21-2020)

### <a name="feature-updates"></a>功能更新

- Microsoft Edge 更新即將逐步推出。 從現在開始，Microsoft Edge 更新會在幾天內推出給使用者。 使我們能夠保護更多人免於進行錯誤的更新，進而改善您的更新體驗。 如果您是使用者，您將會繼續獲得流暢的自動更新。 如果組織未註冊自動更新，您將不會受到此變更影響。 若要深入了解，請參閱[漸進式更新文章](microsoft-edge-update-progressive-rollout.md)。
- Microsoft Defender SmartScreen 改善：對 Microsoft Defender SmartScreen 服務進行許多改善，例如，改善載入時針對重新導向的惡意網站的防護能力，以及最上層框架封鎖，其使用 Microsoft Defender SmartScreen 安全頁面完全取代惡意網站。 最上層框架封鎖可防止播放惡意網站的音訊和其他媒體，讓您擁有簡易且不會混淆的體驗。

- 為了回應使用者意見反應，使用者現在可以讓特定 Cookie 在瀏覽器關閉時不被自動清除。 如果有使用者不想被登出但仍想要在瀏覽器關閉時清除所有其他 Cookie 的網站，此選項就相當實用。 若要使用此功能，請移至 *edge://settings/clearBrowsingDataOnClose*，並啟用 [Cookie 與其他網站資料] 切換。

- 現在提供「自動設定檔切換」功能，以協助您更輕鬆地在不同設定檔間取得工作內容。 如果您在工作中使用多個設定檔，可以在使用您的個人設定檔時瀏覽至需要輸入公司或學校帳戶驗證的網站，藉此查看設定檔。 當我們偵測到此動作時，將提示您切換為公司設定檔來存取該網站，而不需向它進行驗證。 選擇您要切換的公司設定檔時，該網站就會在您的公司設定檔中開啟。 此設定檔切換功能可協助您將公司與個人資料分開，並協助您更輕鬆地取得工作內容。 如果您不希望該功能提示您切換設定檔，則可以選擇 [不要再問我] 選項，之後就不再提醒您。

- 集錦功能改善：
  - 您可以使用拖放功能，在不開啟集錦的情況下，將項目新增至集錦。 在拖放期間，您也可以選擇集錦清單中您要放置項目的位置。
  - 您可以將多個集錦新增至集錦，而不是一次新增一個項目。 若要新增多個項目，請選取項目，然後將它們拖曳到集錦。 或者，您也可以選取項目並以滑鼠右鍵按一下，然後挑選您需要放置項目的集錦。

- 您可以將 Microsoft Edge 視窗中的所有索引標籤新增至新的集錦，而不需要個別新增。 若要這麼做，請以滑鼠右鍵按一下任一索引標籤，然後選擇 [將所有索引標籤新增至集錦]。

- 擴充功能同步現在可供使用。 您現在可以在您所有的裝置上同步擴充功能！ 來自 Microsoft 與 Chrome 商店的擴充功能都會與 Microsoft Edge 同步。 若要使用此功能：按一下功能表列上的省略符號 (**...**)，然後選取 [設定]****。 在您的個人檔案下，按一下 [同步]**** 以查看同步選項。 在 [個人檔案/同步]**** 下，使用切換來啟用擴充功能。 您可以使用 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 群組原則來停用擴充功能的同步。

- 改善下載管理頁面上針對已封鎖不安全下載的訊息。

- 沉浸式閱讀程式的改善：
  - 我們在沉浸式閱讀程式的詞性體驗中新增了「副詞」的支援。 當您在沉浸式閱讀程式中閱讀文章時，開啟文法檢查工具，並開啟詞性中的「副詞」，即可強調頁面上的所有副詞。
  - 新增可選取網頁上任何內容，並在沉浸式閱讀器程式中開啟的功能。 這可讓使用者在所有網站上使用沉浸式閱讀程式和所有學習工具，例如「行聚焦」和「大聲朗讀」。

- Link Doctor 會在使用者誤植 URL 時，為使用者提供主機校正和搜尋查詢。 例如： <br>
使用者將「powerbi」誤植為 powerbbi.com。 Link Doctor 會建議 powerbi.com 做為修正，並建立連結以搜尋「powerbbi」，以免使用者要尋找不同內容。

- 允許使用者儲存其決定以啟動特定網站的外部通訊協定。 使用者可以設定 [ExternalProtocolDialogShowAlwaysOpenCheckbox](/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) 原則，以啟用或停用此功能。

- 使用者可以直接從 Microsoft Edge **[設定]** 將 Microsoft Edge 設為其預設瀏覽器。 這可讓使用者更輕鬆地在瀏覽器本身的內容內變更其預設瀏覽器，而不需要在作業系統設定中搜尋。 若要使用此功能，請移至 *edge://settings/defaultBrowser*，然後按一下 **[設為預設]**。

- 多個 DevTools 更新，包括新的遠端偵錯支援、UI 改善等。 如需詳細資訊，請參閱 [DevTools 的新功能 (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools)。

- MCAS (Microsoft 雲端存取安全性) 警告案例現已推出。 這可讓系統管理員設定警告，這是新的 MCAS 區塊類別，使用者可以在此覆寫 MCAS 封鎖頁面。 MDATP E5 區塊與 Microsoft Edge 中的 SmartScreen 封鎖原本即整合在一起，以獲得流暢的體驗。 這項體驗提供一個全頁的紅色區塊，其中顯示 [此網站遭到您的組織封鎖] 訊息，而不只是顯示快顯通知。

- 在頁面關閉時禁止同步 XmlHttpRequest。 在卸載網頁期間傳送的同步 XmlHttpRequests 將會被移除。 此變更可改善瀏覽器效能和可靠性，但可能會影響尚未更新的 web 應用程式，以使用更新式的 web Api，包括 sendBeacon 和擷取。 可停用此變更並允許在頁面關閉期間同步 XHR 的 [群組原則] 將可使用，直到 Microsoft Edge 88 為止。 如需詳細資訊，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 15 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AllowSurfGame](./microsoft-edge-policies.md#allowsurfgame) - 允許衝浪遊戲。
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) - 設定 Microsoft Edge 將嘗試建立權杖繫結的網站清單。
- [BingAdsSuppression](./microsoft-edge-policies.md#bingadssuppression) - 封鎖 Bing 搜尋結果中的所有廣告。
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - 判斷內建的憑證驗證程式是否將用來驗證伺服器憑證。
- [ClearCachedImagesAndFilesOnExit](./microsoft-edge-policies.md#clearcachedimagesandfilesonexit) - 當 Microsoft Edge 關閉時，清除快取的影像和檔案。
- [ConfigureShare](./microsoft-edge-policies.md#configureshare) - 設定共用體驗。
- [DeleteDataOnMigration](./microsoft-edge-policies.md#deletedataonmigration) - 移轉時刪除舊瀏覽器資料。
- [DnsOverHttpsMode](./microsoft-edge-policies.md#dnsoverhttpsmode) - 控制 DNS-over-HTTPS 模式。
- [DnsOverHttpsTemplates](./microsoft-edge-policies.md#dnsoverhttpstemplates) - 指定所需 DNS-over-HTTPS 解析程式的 URI 範本。
- [FamilySafetySettingsEnabled](./microsoft-edge-policies.md#familysafetysettingsenabled) - 允許使用者設定家長監護服務。
- [LocalProvidersEnabled](./microsoft-edge-policies.md#localprovidersenabled) - 允許來自本機提供者的建議。
- [ScrollToTextFragmentEnabled](./microsoft-edge-policies.md#scrolltotextfragmentenabled) - 啟用捲動至 URL 片段中指定的文字。
- [ScreenCaptureAllowed](./microsoft-edge-policies.md#screencaptureallowed) - 允許或拒絕螢幕擷取。
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) - 設定要從同步中除的類型清單。
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 啟用隱藏原生視窗。

#### <a name="deprecated-policy"></a>過時的原則

下列原則會持續在此版本中運作。 在未來版本中，它會變得「過時」。

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載

<!-- end 83 -->

## <a name="version-81041677-may-18"></a>版本 81.0.416.77：5 月 18 日

修正各種錯誤和效能問題。

## <a name="version-81041672-may-7"></a>版本 81.0.416.72：5 月 7 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#may-7-2020)

## <a name="version-81041668-april-29"></a>版本 81.0.416.68：4 月 29 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-29-2020)

## <a name="version-81041664-april-23"></a>版本 81.0.416.64：4 月 23 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-23-2020)

## <a name="version-81041658-april-17"></a>版本 81.0.416.58：4 月 17 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-17-2020)

## <a name="version-81041653-april-13"></a>版本 81.0.416.53：4 月 13 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-13-2020)

### <a name="feature-updates"></a>功能更新

- 新增對 Windows 資訊保護 (WIP) 的支援，WIP 可協助企業保護敏感性資料免於未經授權的揭露。 [深入了解](./microsoft-edge-security-windows-information-protection.md)。

- 集合現在可供使用。 可以按一下位址列旁邊的 [集合] 圖示來開始。 此動作會開啟 [集合] 窗格，您可以在其中建立、編輯和檢視集合。 我們根據您會在網路上執行的動作設計這些集合。 如果您是購物者、旅行者、教師或學生，則集合可協助您。 [進一步瞭解](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97)。

- 允許從 Microsoft Edge 工具列移除 (從工具列隱藏) [集合] 按鈕，以獲得一致性。

- 內部部署 Active Directory 帳戶的自動登入只會針對開啟該功能的組織。  如果使用者已使用內部部署 AD 帳戶登入，他們將可以登出該帳戶。 只有在使用者的主要帳戶是 Microsoft 帳戶或 Azure Active Directory 帳戶的情況下，使用者才會在其作業系統上使用主要帳戶自動登入。 系統管理員可以使用 ConfigureOnPremisesAccountAutoSignIn 原則，將使用內部部署 AD 帳戶自動登入啟用。

- 應用程式防護。 容器中目前提供延伸模組的支援。

- 新增訊息以在使用者瀏覽至設定為以 Internet Explorer 模式開啟的頁面時，通知使用者 Internet Explorer 未安裝。

- 更新 Microsoft Edge DevTools 中的 3D 檢視工具，加上新功能，以協助您偵錯 z 索引堆疊內容。 3D 檢視會使用色彩和堆疊顯示 DOM (文件物件模型) 深度的外觀，而 z 索引檢視可協助您區隔頁面的不同堆疊內容。 [進一步瞭解](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/)。

- 將 F12 開發工具以 10 個新語言當地語系化，讓它們符合其餘瀏覽器所使用的語言。 [進一步瞭解](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/)。

- 新增對 Dolby Vision 播放的支援。 在啟用 Dolby Vision 的 Windows 10 組建 17134 (2018 年 4 月更新) 中，網站可以顯示 Dolby Vision 內容。 看看如何從 [Netflix](https://help.netflix.com/en/node/42384) 啟用 Dolby Vision 內容。

- Microsoft Edge 現在可以識別及移除重複的我的最愛，並將相同名稱的資料夾合併。 若要存取工具，請按一下瀏覽器工具列上的星形，然後選取 [移除重複的我的最愛]。  您可以確認變更，而對您的最愛的任何更新將會在各個裝置上同步處理。

- 我們聽使用者說，很難區分使用深色佈景主題的一般瀏覽視窗與 InPrivate 視窗，因為這兩個視窗框架都是深色的。 右上角的新實體 InPrivate 藍色藥丸可協助確保使用者正在瀏覽 InPrivate。

- 在正確的瀏覽器設定檔中開啟外部連結。 從 *edge://settings/multiProfileSettings*，針對開啟的連結選取預設的設定檔，讓其在外部應用程式中開啟。

- 新增了警告，以在先前使用另一個帳戶登入之後，提醒使用該帳戶登入瀏覽器設定檔的使用者。 此警告有助於防止意外的資料合併。

- 如果您已在 Microsoft 帳戶中儲存付款卡，您可以在 Microsoft Edge 填寫付款表單時使用該資訊。 您的 Microsoft 帳戶中的卡片將會在整個桌面裝置間同步處理，且完整詳細資料會在使用雙重要素驗證 (CVC 代碼和您的 Microsoft 身分識別) 之後與網站共用。為了方便存取，您可以在驗證期間選擇在裝置上安全地儲存信用卡的複本。

- 「行聚焦」是專為希望在閱讀內容以聚焦於有限部分內容的使用者所設計。 它讓使用者能一次聚焦於第 1、3 或 5 行，並將頁面的其餘部分反灰，讓使用者閱讀而不受干擾。 使用者可以使用觸控或方向鍵來進行捲動，而焦點會相應地位移。

- Microsoft Edge 現在已與 Windows 平台 8.1 及更新版本上的 Windows 拼字檢查整合。 此整合可提供更強大的語言支援，可存取更多語言字典，並能使用 Windows 自訂字典。 當某個語言已在作業系統語言設定中新增時，使用者不需要執行進一步的動作。 同時會在 Microsoft Edge 設定中啟用語言拼字檢查切換。

- 當您使用 Microsoft Edge 開啟 PDF 文件時，使用者現在可以建立醒目提示、變更色彩，以及刪除醒目提示。 此功能有助於日後參照文件的重要部分，以及共同作業。

- 載入已針對網路最佳化的冗長 PDF 文件時，在載入其餘文件時，使用者正在瀏覽的頁面會以較快的速度 (並行) 載入。

- 現在只要按 F9 鍵，就能更輕鬆地啟動網站的沉浸式閱讀程式。

- 現在，您可以使用鍵盤快速鍵 (Ctrl + Shift + U)更輕鬆地開始「大聲朗讀」。

- 新增了 MSI 命令列參數，可讓您在安裝 Microsoft Edge 時隱藏桌面圖示建立。 下例示範如何使用這個新的參數： <br>
`MicrosoftEdgeEnterpriseX64.msi DONOTCREATEDESKTOPSHORTCUT=true`<br>
在即將推出的版本中，將提供群組原則來支援此功能。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 11 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) - 啟用 InPrivate 和來賓設定檔的環境驗證。 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) - 允許音訊沙箱執行。
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - 使用預設的查閱者原則 no-referrer-when-downgrade。
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) - 啟用全域範圍的 HTTP 驗證快取。
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) - 允許匯入延伸模組。
- [ImportCookies](./microsoft-edge-policies.md#importcookies) - 允許匯入 Cookie。
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) - 允許匯入快速鍵。
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) - 指定從 Internet Explorer 模式頁面啟動時，「頁面內」瀏覽至未設定網站的行為。
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - 設定在沒有 Azure AD 網域帳戶時，自動使用 Active Directory 網域帳戶登入。

#### <a name="policy-name-and-caption-changes"></a>原則名稱和標題變更

原則 `OmniboxMSBProviderEnabled` 變更為 [AddressBarMicrosoftSearchInBingProviderEnabled](//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - 該原則的標題為「在網址列的 Bing 建議中啟用 Microsoft Search」。

#### <a name="deprecated-policies"></a>過時的原則

下列原則會持續在此版本中運作。 在未來版本中，它們會變得「過時」。

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容。

#### <a name="resolved-issues"></a>已解決的問題

- 修正 Microsoft Edge 上的 IE 模式導致下載對話方塊持續顯示的問題 (甚至在檔案下載之後亦然)。
- 修正已在 IE 模式中觸發開啟新 IE 模式索引標籤的頁面時，Microsoft Edge 捨棄工作階段 Cookie 的問題。

## <a name="version-800361111-april-7"></a>版本 80.0.361.111：4 月 7 日

修正各種錯誤和效能問題。

## <a name="version-800361109-april-1"></a>版本 80.0.361.109：4 月 1 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-1-2020)

## <a name="version-80036169-march-19"></a>版本 80.0.361.69：3 月 19 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#march-19-2020)

## <a name="version-80036166-march-4"></a>版本 80.0.361.66：3 月 4 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#march-4-2020)

## <a name="version-80036162-february-25"></a>版本 80.0.361.62：2 月 25 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-25-2020)

## <a name="version-80036157-february-20"></a>版本 80.0.361.57：2 月 20 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-20-2020)

## <a name="version-80036156-february-19"></a>版本 80.0.361.56：2 月 19 日

修正各種錯誤和效能問題。

## <a name="version-80036154-february-14"></a>版本 80.0.361.54：2 月 14 日

### <a name="resolved-issues"></a>已解決的問題

- 修正無法將密碼、付款和 Cookie 匯入 Microsoft Edge 的問題。

## <a name="version-80036150-february-11"></a>版本 80.0.361.50：2 月 11 日

已修正各種錯誤和效能修正。

## <a name="version-80036148-february-7"></a>版本 80.0.361.48：2 月 7 日

安全性更新列於[此處](./microsoft-edge-relnotes-security.md#february-7-2020)

### <a name="feature-updates"></a>功能更新

- 新增 SmartScreen 保護，以避免下載潛在有害的應用程式。 [深入了解](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
- 新增支援 Dolby Vision 播放。
- 提供 Windows Mixed Reality 使用者在 VR 頭戴裝置上觀看 360° 影片。
- 新增 [閱讀檢視] 以增加文字間距的選項。
- 新增支援使用 Surface 手寫筆橡皮擦清除連結。
- 新增支援在編輯器模式中使用方向鍵和空格鍵，繪製意見反應螢幕擷取畫面。
- 改善螢幕擷取畫面的可靠性，讓螢幕擷取畫面在提交意見反應時，不再顯示全黑。
- 在裝置未連線至網際網路時顯示的 [本機新索引標籤] 頁面，新增深色佈景主題支援。
- 新增在瀏覽器工作階段於更新、當機等狀況之後還原時，還原安裝為應用程式之網站的功能。
- 在瀏覽器由群組原則管理時，在 PDF UI 中新增支援深色佈景主題。
- 已將 Adobe Flash 更新到版本 32.0.0.321。 [深入了解](https://helpx.adobe.com/flash-player/release-note/fp_32_air_32_release_notes.html)

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 16 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

- [AlternateErrorPagesEnabled](./microsoft-edge-policies.md#alternateerrorpagesenabled) - 找不到網頁時建議相似頁面。
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting) - 控制不安全內容例外的使用方式。
- [DNSInterceptionChecksEnabled](./microsoft-edge-policies.md#dnsinterceptionchecksenabled) - 已啟用 DNS 攔截檢查。
- [HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) - 隱藏初次執行體驗與啟動顯示畫面。
- [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) - 允許指定網站上的不安全內容。
- [InsecureContentBlockedForUrls](./microsoft-edge-policies.md#insecurecontentblockedforurls) - 封鎖指定網站上的不安全內容。
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) - 啟用預設舊版 SameSite Cookie 行為設定。
- [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) - 還原為指定網站上 Cookie 的舊版 SameSite 行為。
- [PaymentMethodQueryEnabled](./microsoft-edge-policies.md#paymentmethodqueryenabled) - 允許網站查詢可用的付款方式。
- [PersonalizationReportingEnabled](./microsoft-edge-policies.md#personalizationreportingenabled) - 透過將瀏覽歷程記錄傳送至 Microsoft，允許個人化廣告、搜尋與新聞。
- [PinningWizardAllowed](./microsoft-edge-policies.md#pinningwizardallowed) - 允許 [釘選到工作列] 精靈。
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled) - 設定 Microsoft Defender SmartScreen 來封鎖潛在有害的應用程式。
- [TotalMemoryLimitMb](./microsoft-edge-policies.md#totalmemorylimitmb) - 針對單一 Microsoft Edge 執行個體可以使用的記憶體設定 MB 限制。
- [WebAppInstallForceList](./microsoft-edge-policies.md#webappinstallforcelist) - 設定強制安裝的 Web 應用程式清單。
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebRtcLocalIpsAllowedUrls](./microsoft-edge-policies.md#webrtclocalipsallowedurls) - 透過 WebRTC 管理本機 IP 位址的暴露程度。

#### <a name="deprecated-policies"></a>過時的原則

已取代下列原則。

- [NewTabPageCompanyLogo](./microsoft-edge-policies.md#newtabpagecompanylogo) - 設定新的索引標籤頁面公司標誌。

### <a name="resolved-issues"></a>已解決的問題

- 已修正音訊在 Citrix 環境中無法運作的問題。
- 已修正 Microsoft Edge 與舊版 Microsoft Edge 並存體驗中斷舊版連結的問題。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)