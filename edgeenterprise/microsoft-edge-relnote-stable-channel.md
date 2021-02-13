---
title: Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 02/11/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: 82c03b918f8407eaa4b7f6b91a7a6fc1d3e2dc9b
ms.sourcegitcommit: 543259647f221de88e67d47984617091f9c75cfc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "11326996"
---
# Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。

- 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。
- 封存的 Microsoft Edge 穩定通道的版本資訊在[此處](microsoft-edge-relnote-archive-stable-channel.md)。

 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。

> [!NOTE]
> 針對穩定通道，更新會在一或多天內逐步推出。 若要深入了解，請參閱 [Microsoft Edge 更新的漸進式推出](microsoft-edge-update-progressive-rollout.md)。

## 版本 88.0.705.68：2 月 11 日

修正各種錯誤和效能問題。

## 版本 88.0.705.63：2 月 5 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-5-2021)。 此更新包含 Chromium 小組報告的 [CVE-2021-21148](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21148)，因為已發行的版本中有惡意探索問題。

## 版本 88.0.705.62：2 月 4 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#February-4-2021)。

修正各種錯誤和效能問題。

## 版本 88.0.705.56：1 月 28 日

已修正各種錯誤和效能問題。

## 版本 88.0.705.53：1 月 26 日

已修正各種錯誤和效能問題。

## 版本 88.0.705.50：1 月 21 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-21-2021)。

<!--- begin major 88  --->
### 功能更新

- **取代的項目：**

  - 取代 FTP 通訊協定的支援。 已從 Microsoft Edge 移除對舊版 FTP 通訊協定的支援。 嘗試瀏覽至 FTP 連結會造成瀏覽器將作業系統導向開啟外部應用程式以處理 FTP 連結。 或者，IT 系統管理員可以設定 Microsoft Edge，以對仰賴於 FTP 通訊協定的網站使用 IE 模式。
  - 將移除對 Adobe Flash 的支援。 從 Microsoft Edge Beta 版本 88 開始，將會移除 Adobe Flash 功能和支援。 深入了解：[Adobe Flash Player 終止支援的更新 - Microsoft Edge 部落格 (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **驗證：**

  - 單一登入 (SSO) 目前可供下層 Windows 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用。 在下層 Microsoft Windows (7、8.1) 上於 Microsoft Edge 登入的使用者，現在會自動登入已設定為允許使用公司和 Microsoft 帳戶進行單一登入的網站 (例如，bing.com、office.com、msn.com、outlook.com)。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。
  
  - 在採用非 Azure AD Microsoft Edge 設定檔的系統上，使用任何 Windows Azure Active Directory (Azure AD) 帳戶單一登入 (SSO) 至公司網站。 您可以針對未使用公司/學校帳戶登入且並非來賓或私密瀏覽的任何設定檔啟用此功能，並允許在使用該設定檔的作業系統上使用任何登入的公司/學校帳戶。 此功能可在 [設定]****  >  [設定檔]****  >  [設定檔喜好設定]****  >  [對使用此設定檔的公司或學校網站允許單一登入]**** 中設定。
  
    > [!NOTE]
    > 「使用 Microsoft Edge 設定檔的所有 Windows 帳戶的單一登入 (SSO)」是 1 月 21 日版本資訊的更新。

- **結束工作階段的 kiosk 模式選項**。 「結束工作階段」按鈕現在可於 kiosk 模式公開瀏覽體驗中使用。 此功能可確保在 Microsoft Edge 關閉時，瀏覽器資料和設定隨即會刪除。 深入了解 kiosk 模式功能和藍圖，[設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)。

- **安全性及隱私權：**

  - 如果在線上洩漏中發現使用者的密碼，就會產生警示。 將對照已知遭入侵認證的儲存庫檢查使用者的密碼，並在發現相符項目時傳送警示給使用者。 若要確保安全性與隱私權，請在針對洩漏認證的資料庫檢查使用者密碼時，對其進行雜湊處理和加密。
  - 自動升級混合內容。 透過 HTTPS 提供的安全頁面可能包含會透過非安全 HTTP 提供的參考影像。 為了改善 Microsoft Edge 88 中的隱私權和安全性，將改為透過 HTTPS 來擷取這些影像。 如果無法透過 HTTPS 取得影像，將無法載入影像。
  - 依網站和最近的活動來檢視網站權限。 從 Microsoft Edge 88 開始，使用者將能更輕鬆地管理網站權限。 他們將可以依網站而不只是依權限類型檢視權限。 此外，我們新增了最近的活動區段，該區段將向使用者顯示對其網站權限的所有最近的變更。
  - 增加瀏覽器 Cookie 的控制項。 從 Microsoft Edge 88 開始，使用者可以刪除第三方 Cookie，而不會影響第一方 Cookie。 使用者也可以依據第一方或第三方篩選其 Cookie，並依名稱、Cookie 數量，以及儲存的資料數量和上次修改時間排序。

- **密碼：**

  - 密碼產生器。 Microsoft Edge 提供內建的強式密碼產生器，可在註冊新帳戶或變更現有密碼時使用。 只要在密碼欄位中尋找瀏覽器建議的密碼下拉式清單，系統就會在選取時自動將其儲存到瀏覽器並跨裝置同步，方便日後使用。
  - 密碼監視器。 當您儲存至瀏覽器的密碼與洩漏認證清單中顯示的密碼一樣時，Microsoft Edge 會通知您並提示您更新密碼。 密碼監視器會代表您掃描相符項目，且預設為啟用。
  - 編輯密碼。 現在，您可以直接在 Microsoft Edge 設定中編輯已儲存的密碼。 每次 Microsoft Edge 更新密碼之後，都可以透過在 [設定] 中編輯儲存的項目輕鬆地將儲存的舊密碼替換為新密碼。 

- **利用啟動提昇來改善 Microsoft Edge 啟動速度**。 為了改善 Microsoft Edge 啟動速度，我們開發了名為啟動提升的功能。 啟動提升利用讓 Microsoft Edge 在背景中執行，讓 Microsoft Edge 更快速啟動。 注意：此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

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

### 原則更新

#### 新原則

新增了 18 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則。

- [BasicAuthOverHttpEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#basicauthoverhttpenabled) - 允許 HTTP 的基本驗證。
- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions) - 封鎖安裝外部擴充功能。
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed) - 允許在 Internet Explorer 模式中啟動本機檔案。
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) - 根據副檔名允許清單在 Internet Explorer 模式中開啟本機檔案。
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu) - 顯示操作功能表以在 Internet Explorer 模式中開啟連結。
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior) - 內部網路重新導向行為。
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist) - 停用拒絕清單上的印表機類型。
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards) - 顯示 Microsoft Rewards 體驗。
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled) - 設定睡眠索引標籤。
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) - 設定睡眠索引標籤的背景索引標籤無活動逾時。
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls) - 對特定網站封鎖睡眠索引標籤。
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled) - 啟用啟動提升。
- [TargetBlankImpliesNoOpener](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#targetblankimpliesnoopener) - 不对指向 _blank 的链接設定 window.opener。
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) - 指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) - 設定瀏覽器側邊上索引標籤垂直版面配置的可用性。
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - 在 WebRTC 中允許舊版 TLS/DTLS 降級。
- [WebWidgetAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetallowed) - 啟用 Web 小工具。
- [WebWidgetIsEnabledOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webwidgetisenabledonstartup) - 在 Windows 啟動時允許 Web 小工具。

#### 取代的原則

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - 啟用主動式驗證。
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - 啟用主動式驗證。
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - 設定 Proxy 伺服器設定。
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - 設定 Proxy .pac 檔案 URL。
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - 設定 Proxy 伺服器的位址或 URL。
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容原則。

### 已過時的原則

- [AllowPopsDuringPageUnload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowpopupsduringpageunload) - 允許在卸載網頁期間顯示快顯視窗。
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - 預設 Adobe Flash 設定。
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - 允許特定網站上的 Adobe Flash 外掛程式。
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - 封鎖特定網站上的 Adobe Flash 外掛程式。
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - 將 Adobe Flash 內容設定延伸至所有內容。
<!--- end major 88  --->
## 版本 87.0.664.75：1 月 7 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#january-7-2021)。

## 版本 87.0.664.66：12 月 17 日

修正各種錯誤和效能問題。

## 版本 87.0.664.60：12 月 10 日

修正各種錯誤和效能問題。

## 版本 87.0.664.57：12 月 7 日

修正各種錯誤和效能問題。 安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#december-7-2020)。

## 版本 87.0.664.55：12 月 3 日

修正各種錯誤和效能問題。 下列功能已針對此版本進行更新。

- **預設會啟用 [購物] 功能**。 從 Microsoft Edge 版本 87 開始，企業使用者可以利用 Microsoft Edge 中的購物功能。 有了購物功能，Microsoft Edge 可協助使用者在線上購物時找到優待卷及更好的價格。 (優待券體驗已隨著穩定版本 87.0.664.41 推出。) 價格比較體驗現在隨著此更新提供。 此功能可使用 [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled) 原則設定。 請參閱我們的[部落格](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/)和[深入了解](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) Microsoft 購物的相關資訊。

## 版本 87.0.664.52：11 月 30 日

修正各種錯誤和效能問題。

## 版本 87.0.664.47：11 月 23 日

修正各種錯誤和效能問題。

<!-- begin major 87 --->
## 版本 87.0.664.41：11 月 19 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020)。

### 功能更新

- **自動將不相容網站從 Internet Explorer 重新導向至 Microsoft Edge**。 從 Microsoft Edge 87 穩定版更新開始，在 Internet Explorer 上顯示不相容訊息的公共網站，將自動重新導向至 Microsoft Edge。 若要深入了解及設定此體驗，請參閱[重新導向不相容的網站](https://docs.microsoft.com/deployedge/edge-learnmore-neededge)。

- **kiosk 模式隱私權功能已啟用**。 從 Microsoft Edge 版本 87 開始，有助於企業處理使用者資料隱私權的 kiosk 模式功能將會啟用。 這些功能將啟用一些體驗, 例如在退出時清除使用者資料、刪除下載的檔案，以及在指定的閒置時間後, 重設已設定的啟動體驗。 深入了解如何[設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **依預設啟用購物功能**。 從 Microsoft Edge 版本 87 開始，企業使用者也可以透過在 Edge 中購物獲益。 利用購物功能，Microsoft Edge 可在使用者於線上購物時，協助使用者找到優待券和更優惠的價格。 我們隨著此更新提供優待券體驗，而價格比較將於 Microsoft Edge 87 近期的更新中發佈。 此功能可透過 [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) 原則設定。 請參閱我們的[部落格](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/)和[深入了解](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) Microsoft 購物的相關資訊。

- **預設啟用 ClickOnce 部署**。 預設會在 Microsoft Edge 87 中啟用 ClickOnce，這樣可減少企業部署軟體的障礙，並更能與舊版Microsoft Edge Legacy 瀏覽器行為一致。 從 Microsoft Edge 87 開始，ClickOnceEnabled 原則的 “未設定”狀態將反映已啟用的新預設 ClickOnce 狀態 (與之前停用的預設狀態相比)。

- **企業版的新標籤頁 (NTP) 將生產力與且可自訂的工作相關的摘要內容整合在一起**。 企業版 NTP 加入Microsoft Office 365 生產力頁面, 我們提供在公司或學校帳戶登入的使用者, 有其個人化的個人化及與公司及產業相關的資料來源, 並能組織在同一個頁面中. 使用者將能夠辨識熟悉的 Office 365 內容，以及由 Bing 提供支援的商務用 Microsoft 搜尋。 此外，他們可以從組織的可用內容和模組選擇最相關的內容，以輕鬆自訂 [我的摘要]。 IT 系統管理員可以控制其組織的新聞摘要設定，包括為 Microsoft Edge 新索引標籤頁面選取的產業 (移至 Microsoft 365 系統管理中心)。 [深入了解](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

- **隱私權與安全性：**

  - 支援政策設定網站的 TLS Token Binding 權杖綁定。 TLS Token binding 權杖綁定可協助防止權杖被竊取攻擊，以確保無法從最初設定cookie的設備以外的其他設備重複使用。 使用 TLS 權杖綁定需設定 [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) 規定，並要求列出的網站支援這項功能。

- **鍵盤支持PDF 檔案上的螢光筆功能**. 使用者可以使用鍵盤鍵來醒目提示 PDF 中的任何文字。

- **列印:**

  - 選擇雙面列印時要翻轉的那一面。 當雙面列印時，使用者可以選擇在紙張的長邊或短邊翻轉。
  - 選擇企業的列印光柵化模式。 控制將Microsoft Edge 列印到一個 Windows 上的非PostScript 印表機。 有時需將非 PostScript 印表機上的列印工作光柵化才能正確列印。 列印選項為「完全」和「快速」。

### 原則更新

#### 新原則

新增了 10 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則。

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) - 設定從 Microsoft Edge 複製的 URL 的預設貼上格式，並決定使用者是否可以使用其他格式。
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) - 已啟用在 Microsoft Edge 中購物。
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) - 隱藏一次性的重新導向對話方塊和 Microsoft Edge 上的橫幅。
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) -設定位址欄編輯以給 kiosk 模式有公眾流覽體驗。
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - 當 Microsoft Edge 關閉時，刪除隨著 kiosk 工作階段下載的檔案。
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) - 啟用顯示密碼按鈕。
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) - 防止安裝瀏覽器協助程式物件 (BHO)，以將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) - 將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - 設定語音辨識。
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - 啟用 Microsoft Edge 中的 Web 擷取功能。

#### 取代的原則

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) -設定 Microsoft Edge 新增索引標籤頁面體驗。

#### 淘汰的原則

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - 在限定時間內重新啟用已取代的網頁平台功能。

<!-- end major 87 -->

## 版本 86.0.622.69：11 月 13 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-13-2020)。 此更新包含 Chromium 小組所報告的 [CVE-2020-16013](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16013) 和 [CVE-2020-16017](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16017)，因為已發行的版本中有惡意探索問題。

## 版本 86.0.622.68：11 月 11 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-11-2020)

## 版本 86.0.622.63：11 月 4 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-4-2020)。 此更新包含 Chromium 小組報告的 [CVE-2020-16009](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-16009)，因為已發行的版本中有惡意探索問題。

## 版本 86.0.622.61：11 月 2 日

修正各種錯誤和效能問題。

## 版本 86.0.622.58：10 月 29 日

修正各種錯誤和效能問題。

## 版本 86.0.622.56：10 月 27 日

修正各種錯誤和效能問題。

## 版本 86.0.622.51：10 月 22 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## 版本 86.0.622.48：10 月 20 日

修正各種錯誤和效能問題。

## 版本 86.0.622.43：10 月 15 日

修正各種錯誤和效能問題。

<!-- begin major 86 -->
## 版本 86.0.622.38：10 月 9 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020)

### 功能更新

* **復原為上一個 Microsoft Edge 版本。** 如果最新版本的 Microsoft Edge 有問題，復原功能可讓系統管理員還原為已知良好的 Microsoft Edge 版本。 **注意：** 穩定版本 86.0.622.38 是您可以復原的第一個版本，這表示穩定版本 87 是準備好要回復的第一個版本。 [進一步瞭解](edge-learnmore-rollback.md)。

* **預設會在整個企業強制啟用同步。**  系統管理員可以使用 [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) 原則，預設為 Azure Active Directory (Azure AD) 帳戶啟用同步。

* **在 Windows 7 和 8.1 上自動切換設定檔。** 目前在 Windows 10 版 Microsoft Edge 中提供的自動設定檔切換功能已延伸至舊版 Windows (Windows 7 和 8.1)。 如需詳細資訊，請參閱[自動設定檔切換](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)部落格文章。

* **根據預設 SameSite=Lax Cookie**。 為了改善網頁安全性和隱私權，根據預設會預設 cookie 為[SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)。 這表示 cookie 只會在第一方的上下文中傳送，對於發傳送第三方的要求將被忽略。 這項變更可能會對需要第三方資源的 cookie 才能正常運作的網站造成相容性影響。 若要允許使用這類 cookie，網頁程式開發人員可以標示 cookie，在設定 cookie 時，只要新增清楚的 `SameSite=none` 和 `Secure` 屬性，就能將該 cookie 設定並傳送到第三方上下文。 如果企業希望讓特定網站免于此變更，可以使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) 原則以達成，或可以使用 [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 原則，以退出所有網站的變更。

* **移除 HTML5 應用程式快取 API。**  從 Microsoft Edge 版本 86 開始，可啟用離線使用網頁的舊版應用程式快取 API 會從 Microsoft Edge 中移除。 Web 開發人員應該檢閱 [WebDev 文件](https://web.dev/appcache-removal/)，以取得有關將應用程式快取 API 取代為服務工作者的資訊。  重要：您可以要求 [AppCache OriginTrial 權杖](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673)，允許網站在 Microsoft Edge 版本 90 之前繼續使用已取代的應用程式快取 API。

* **隱私權與安全性：**

  * 針對舊版 Windows 和 macOS 取代 [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) 和 [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) 原則。 這些原則已在 Microsoft Edge 版本 86 中取代，並將於 Microsoft Edge 版本 89 中變得過時。<br>
這些原則會在 Windows 10 上由 [允許遙測][](https://go.microsoft.com/fwlink/?linkid=2099569) 取代，而新的 [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) 原則則用於所有其他平台。 這可讓使用者管理傳送至 Microsoft 的 Windows 7、8、8.1 和 macOS 診斷資料。
  * 安全 DNS (DNS-over-HTTPS) 支援。  從 Microsoft Edge 版本 86 開始，用來控制未受管理裝置上安全 DNS 的設定可供使用。 這些設定無法供受管理裝置上的使用者存取，但是 IT 系統管理員可以使用 [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode) 群組原則來啟用或停用安全 DNS。

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

### 原則更新

#### 新原則

新增了 23 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - 封鎖集錦中服務和匯出目標特定清單的存取權。
- [DefaultFileSystemReadGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemreadguardsetting) - 控制檔案系统 API 的讀取使用。
- [DefaultFileSystemWriteGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultfilesystemwriteguardsetting) - 控制檔案系統 API 的寫入使用。
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - 預設的感應器設定。
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - 控制 Serial API 的使用方式。
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) - 傳送關於瀏覽器使用狀況的必要和選擇性診斷資料。
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - 允許存取 Enterprise Mode Site List Manager 工具。
- [FileSystemReadAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadaskforurls) - 允許透過這些網站上的檔案系統 API 讀取存取權。
- [FileSystemReadBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemreadblockedforurls) - 封鎖透過這些網站上的檔案系統 API 讀取存取權。
- [FileSystemWriteAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteaskforurls) - 允許這些網站上的檔案和目錄的寫入存取權。
- [FileSystemWriteBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#filesystemwriteblockedforurls) - 封鎖這些網站上的檔案和目錄的寫入存取權。
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) - 強制同步處理瀏覽器資料，且不顯示同步同意提示。
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) - 啟用不安全表單的警告。
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - 允許 Internet Explorer 模式測試。
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) - 選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知以及 Microsoft 服務的提示。
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) - 設定新的索引標籤頁面版面配置所允許的背景類型。
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) - 在 Microsoft Edge 關閉時儲存 Cookie。
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) - 允許存取特定網站上的感應器。
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) - 封鎖存取特定網站上的感應器。
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) - 允許特定網站上的 Serial API。
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) - 封鎖特定網站上的 Serial API。
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - 啟用使用者代理程式用戶端提示功能。
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - 限制保留的使用者資料快照數量，以便在緊急復原時使用。

#### 取代的原則

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。

#### 淘汰的原則

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。

## 版本 85.0.564.70：10 月 6 日

修正各種錯誤和效能問題。

## 版本 85.0.564.68：10 月 1 日

修正各種錯誤和效能問題。

## 版本 85.0.564.63：9 月 23 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## 版本 85.0.564.51：9 月 9 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## 版本 85.0.564.44：8 月 31 日

修正各種錯誤和效能問題。

<!-- 85.0.564.41: August 27 -->
<!-- Archived to version 84.0.522.40: July 16 -->

## 另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
