---
title: Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: 99ec3764d433906dcf45e851c7bc62d4ec2483fa
ms.sourcegitcommit: 3bafa63c17f01fcec60d6297474a6a391034a8be
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/15/2021
ms.locfileid: "11271202"
---
# Microsoft Edge Beta 通道的版本資訊

這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。 這些版本資訊的封存版本可在[此處](microsoft-edge-relnote-archive-beta-channel.md)取得。

## 版本 88.0.705.45：1 月 15 日

修正各種錯誤和效能問題。

## 版本 88.0.705.41：1 月 11 日

修正各種錯誤和效能問題。

## 版本 88.0.705.29：12 月 21 日

修正各種錯誤和效能問題。

<!-- begin major 88 -->
## 版本 88.0.705.18：12 月 9 日

### 功能更新

- **取代的項目：**

  - 取代 FTP 通訊協定的支援。 已從 Microsoft Edge 移除對舊版 FTP 通訊協定的支援。 嘗試瀏覽至 FTP 連結會造成瀏覽器將作業系統導向開啟外部應用程式以處理 FTP 連結。 或者，IT 系統管理員可以設定 Microsoft Edge，以對仰賴於 FTP 通訊協定的網站使用 IE 模式。
  - 將移除對 Adobe Flash 的支援。 從 Microsoft Edge Beta 版本 88 開始，將會移除 Adobe Flash 功能和支援。 深入了解：[Adobe Flash Player 終止支援的更新 - Microsoft Edge 部落格 (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **驗證：**

  - 單一登入 (SSO) 目前可供 macOS 和下層 Windows 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用。 在 macOS 或下層 Microsoft Windows (7、8.1) 上於 Microsoft Edge 登入的使用者，現在會自動登入已設定為允許使用公司和 Microsoft 帳戶進行單一登入的網站 (例如，bing.com、office.com、msn.com、outlook.com)。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。
  - 在 macOS 上針對使用其公司帳戶驗證的網站，自動將使用者切換至其公司設定檔。 從 Microsoft Edge 版本 88 開始，我們提供功能，讓您在 macOS 上切換使用使用者的工作設定檔進行驗證的網站。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。

- 結束工作階段的 kiosk 模式選項。 「結束工作階段」按鈕現在可於 kiosk 模式公開瀏覽體驗中使用。 此功能可確保在 Microsoft Edge 關閉時，瀏覽器資料和設定隨即會刪除。 深入了解 kiosk 模式功能和藍圖，[設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)。

- **安全性及隱私權：**

  - 如果在線上洩漏中發現使用者的密碼，就會產生警示。 將對照已知遭入侵認證的儲存庫檢查使用者的密碼，並在發現相符項目時傳送警示給使用者。 若要確保安全性與隱私權，請在針對洩漏認證的資料庫檢查使用者密碼時，對其進行雜湊處理和加密。
  - 自動升級混合內容。 透過 HTTPS 提供的安全頁面可能包含會透過非安全 HTTP 提供的參考影像。 為了改善 Microsoft Edge 88 中的隱私權和安全性，將改為透過 HTTPS 來擷取這些影像。 如果無法透過 HTTPS 取得影像，將無法載入影像。
  - 依網站和最近的活動來檢視網站權限。 從 Microsoft Edge 88 開始，使用者將能更輕鬆地管理網站權限。 他們將可以依網站而不只是依權限類型檢視權限。 此外，我們新增了最近的活動區段，該區段將向使用者顯示對其網站權限的所有最近的變更。
  - 增加瀏覽器 Cookie 的控制項。 從 Microsoft Edge 88 開始，使用者可以刪除第三方 Cookie，而不會影響第一方 Cookie。 使用者也可以依據第一方或第三方篩選其 Cookie，並依名稱、Cookie 數量，以及儲存的資料數量和上次修改時間排序。

- **效能：**

  - 使用休眠索引標籤改善瀏覽器效能。 睡眠索引標籤會透過將非作用中索引標籤置於睡眠，以釋放系統資源 (例如記憶體和 CPU)，以供使用中索引標籤或其他應用程式使用。 使用者可以防止網站進入睡眠，並設定非作用中索引標籤進入睡眠之前的時間長度。 若要讓使用者保持在流程中，也有啟發學習法，可防止特定網站 (例如內部網路網站) 進入睡眠。 此功能僅限於已啟用實驗的隨機選取使用者群組。 我們打算在 Microsoft Edge 版本 89 中將 [睡眠] 索引標籤功能預設為啟用。 您可以使用群組原則來管理此功能。
  - 利用啟動提升來改善 Microsoft Edge 啟動速度。 為了改善 Microsoft Edge 啟動速度，我們開發了名為啟動提升的功能。 啟動提升利用讓 Microsoft Edge 在背景中執行，讓 Microsoft Edge 更快速啟動。 注意：此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

- **生產力：**

  - 使用垂直索引標籤來改善生產力和多工功能。 隨著水平索引標籤數量增加，網站標題會開始被截斷，而索引標籤控制項會隨著索引標籤縮減而失去。 這會中斷使用者工作流程，因為他們會用更多時間來尋找、切換和管理其索引標籤，以及用更少時間在手邊的工作上。 垂直索引標籤可讓使用者將索引標籤移至側面，在其中，垂直對齊的圖示和較長的網站標題可讓您更輕鬆地快速掃描、識別並切換到要開啟的索引標籤。
  - 自動填入生日欄位。 Microsoft Edge 已能透過自動填入使用者資料 (例如地址、名稱、電話號碼等)，來協助您節省在填入表單和線上建立帳戶時的時間和精力。Microsoft Edge 現在支援生日欄位，使用者可以儲存並自動填入。 使用者可以隨時在其設定檔設定中檢視、編輯及刪除此資訊。
  - 歷程記錄中「最近關閉的項目」的增強功能。 最近關閉的項目現在會保持來過去任何瀏覽工作階段 (而不僅僅是上一個工作階段) 的最後 25 個索引標籤和視窗。 使用者可在新的歷程記錄體驗中選取 [最近關閉的]，以查看之前開啟的所有索引標籤。
  - 預設啟用 [Your day at a glance] 功能。 從 Microsoft Edge 版本 88 開始，資訊工作者可以使用新索引標籤頁面 (NTP) 上的智慧生產力功能。 我們為使用工作或學校帳戶登入的使用者提供個人化且由 M365 Graph 支援的相關內容。 使用者可以快速瀏覽 [Your day at a glance] 模組，輕鬆追蹤他們的會議與最近的工作，以及快速啟動他們想要使用的應用程式。

- **PDF：**

  - 書籍檢視 (兩頁) 中的 PDF 文件顯示。 從 Microsoft Edge 版本 88 開始，使用者可以在單頁或雙頁書籍檢視中檢視 PDF 文件。 若要變更檢視，請按一下工具列中的 [頁面檢視]**** 按鈕。
  - PDF 檔案的錨定文字記事支援。 從 Microsoft Edge 版本 87 開始，使用者可以在 PDF 檔案中的任何文字片段上新增輸入的文字記事。
  - PDF 文件中的文字選取體驗更順暢。 對於在 Microsoft Edge 中開啟的 PDF 文件，使用者會獲得更順暢且一致的文字選取體驗。
  - 在下載列中檢視另存為 PDF 檔案的網頁。 使用者現在可以在下載列將 [另存成 PDF] 設為網頁的印表機目的地，以檢視所產生的 PDF 檔案。

- **字型：**

  - 瀏覽器圖示已更新為 Fluent 設計系統。 隨著我們持續處理瀏覽器中的 Fluent Design，我們已進行變更，以讓圖示與新的 Microsoft 圖示系統對齊。 這些變更會影響我們的許多高接觸的使用者介面，包括可在我們的各種功能表中找到的索引標籤、網址列以及瀏覽和尋路圖示。
  - 改善字型轉譯。 改善文字轉譯，以提高清晰度並減少模糊。

### 原則更新

#### 新原則

新增了 16 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列原則。

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
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) - 指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) - 設定瀏覽器側邊上索引標籤垂直版面配置的可用性。
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - 在 WebRTC 中允許舊版 TLS/DTLS 降級。

#### 取代的原則

下列原則已取代。

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - 啟用主動式驗證。
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - 啟用主動式驗證。
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - 設定 Proxy 伺服器設定。
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - 設定 Proxy .pac 檔案 URL。
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - 設定 Proxy 伺服器的位址或 URL。
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容原則。

#### 淘汰的原則

下列原則已過時。

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - 預設 Adobe Flash 設定。
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - 允許特定網站上的 Adobe Flash 外掛程式。
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - 封鎖特定網站上的 Adobe Flash 外掛程式。
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - 將 Adobe Flash 內容設定延伸至所有內容。

<!-- end major 88 -->

## 版本 87.0.664.55：12 月 3 日

修正各種錯誤和效能問題。 此版本支援下列新功能。

- **如果在線上洩漏中發現使用者的密碼，就會產生警示**。 系統會針對已知違例認證的儲存庫檢查使用者密碼，並在找到相符專案時傳送通知給使用者。 若要確保安全性與隱私權，請在針對洩漏認證的資料庫檢查使用者密碼時，對其進行雜湊處理和加密。

## 版本 87.0.664.52：11 月 30 日

修正各種錯誤和效能問題。

## 版本 87.0.664.40：11 月 18 日

修正各種錯誤和效能問題。

## 版本 87.0.664.36：11 月 16 日

修正各種錯誤和效能問題。

## 版本 87.0.664.30：11 月 9 日

修正各種錯誤和效能問題。

## 版本 87.0.664.24：11 月 2 日

修正各種錯誤和效能問題。

## 版本 87.0.664.18：10 月 26 日

修正各種錯誤和效能問題。

<!-- begin major 87 -->
## 版本 87.0.664.12：10 月 20 日

### 功能更新

- **Kiosk 模式隱私權功能已**啟用。 從 Microsoft Edge 版本 87 kiosk 模式功能開始，將會對企業的使用者資料隱私權提供協助。 這些功能將啟用一些體驗, 例如在退出時清除使用者資料、刪除下載的檔案，以及在指定的閒置時間後, 重設已設定的啟動體驗。 深入瞭解如何 [設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)
- **預設啟用 ClickOnce的 部署**。 預設會在 Microsoft Edge 87 中啟用 ClickOnce，這樣可減少企業部署軟體的障礙，並更能與舊版Microsoft Edge Legacy 瀏覽器行為一致。 從 Microsoft Edge 87 開始，ClickOnceEnabled 原則的 “未設定”狀態將反映已啟用的新預設 ClickOnce 狀態（與之前停用的預設狀態相比）。
- **企業版的新標籤頁（NTP）將生產力與且可自訂的工作相關的摘要內容整合在一起**。 企業版 NTP 加入Microsoft Office 365 生產力頁面, 我們提供在公司或學校帳戶登入的使用者, 有其個人化的個人化及與公司及產業相關的資料來源, 並能組織在同一個頁面中. 使用者將能夠識別熟悉的Microsoft Office 365 內容, 和由 Bing 所主導的Microsoft 搜尋 Microsoft Search for Business。。 此外，他們可以輕鬆地轉到自訂的＂我的摘要＂，其中包含與使用者、公司或行業相關的內容和模組，以及組織所提供的其他摘要。 [進一步瞭解](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true)。

- **隱私權與安全性：**

  - 支援政策設定網站的 TLS Token Binding 權杖綁定。 TLS Token binding 權杖綁定可協助防止權杖被竊取攻擊，以確保無法從最初設定cookie的設備以外的其他設備重複使用。 使用 TLS 權杖綁定需設定 [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) 規定，並要求列出的網站支援這項功能。

- **鍵盤支持PDF 檔案上的螢光筆功能**. 使用者可以使用鍵盤鍵來醒目提示 PDF 中的任何文字。

- **列印:**

  - 選擇雙面列印時要翻轉的那一面。 當雙面列印時，使用者可以選擇在紙張的長邊或短邊翻轉。
  - 選擇企業的列印光柵化模式。 控制將Microsoft Edge 列印到一個 Windows 上的非PostScript 印表機。 有時需將非 PostScript 印表機上的列印工作光柵化才能正確列印。 列印選項為「完全」和「快速」。

### 原則更新

#### 新原則

新增了 10 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列原則。

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) -設定從 Microsoft Edge 複製的預設貼上 Url 格式，並判斷使用者是否可以使用其他格式設定。
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) - 啟用Microsoft Edge 中的 Shopping in Microsoft Edge Enabled 。
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) -隱藏一次性重新導向對話方塊和 Microsoft Edge 標題。
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) -設定位址欄編輯以給 kiosk 模式有公眾流覽體驗。
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - Microsoft Edge 關閉時，刪除以 kiosk 會話方式下載的檔案。
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) -啟用密碼顯示按鈕。
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) -禁止安裝 BHO 以將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) -將不兼容的網站從Internet Explorer重導向到Microsoft Edge。
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) -設定語音辨識。
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) -啟用 Microsoft Edge 中的網頁擷取功能。

#### 已被取代的政策

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) -設定 Microsoft Edge 新增索引標籤頁面體驗。

#### 淘汰的原則

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) -在有限時間內重新啟用已棄用的網頁平臺功能。

<!-- end major 87 -->

## 版本 86.0.622.43：10 月 16 日

修正各種錯誤和效能問題。

## 版本 86.0.622.36：10 月 7 日

修正各種錯誤和效能問題。

## 版本 86.0.622.31：10 月 1 日

修正各種錯誤和效能問題。

## 版本 86.0.622.28：9 月 28 日

修正各種錯誤和效能問題。

## 版本 86.0.622.15：9 月 14 日

修正各種錯誤和效能問題。

## 版本 86.0.622.11：9 月 9 日

### 功能更新

* **Internet Explorer 模式：**

   * 讓使用者使用 Microsoft Edge 使用者介面 (UI) 在 Internet Explorer 模式中測試網站。 從 Microsoft Edge 版本 86 開始，系統管理員可以啟用一個 UI 選項，讓其使用者可以在 Internet Explorer 模式中載入索引標籤，以用於測試目的或做為權宜之計，直到將網站新增至網站清單 XML 為止。

* **使用下載管理員來刪除磁碟上的下載項目。** 使用者現在可以在不離開瀏覽器的情況下，從磁碟中刪除其下載的檔案。 在下載架子或下載頁面的操作功能表中，有新的 [刪除下載] 功能。

* **復原為上一個 Microsoft Edge 版本。** 如果最新版本的 Microsoft Edge 有問題，復原功能可讓系統管理員還原為已知良好的 Microsoft Edge 版本。
[進一步瞭解](edge-learnmore-rollback.md)。

* **預設會在整個企業強制啟用同步。**  系統管理員可以使用 [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) 原則，預設為 Azure Active Directory (Azure AD) 帳戶啟用同步。

* **PDF 更新：**

  * PDF 文件的目錄。 從版本 86 開始，Microsoft Edge 已新增對目錄的支援，讓使用者能輕鬆瀏覽 PDF 文件。
  * 在小型板型規格螢幕上存取所有 PDF 功能。 在使用小型螢幕的裝置上存取 Microsoft Edge PDF 閱讀程式的所有功能。
  * PDF 檔案上螢光筆的手寫筆支援。 透過此更新，使用者可以使用數位筆直接在 PDF 檔案上將文字醒目提示，就像使用實體螢光筆和紙張的方式一樣。
  * 改善 PDF 捲動。 您現在可以在瀏覽長篇的 PDF 文件時，體驗不間斷的捲動。

* **在 Windows 7、8 和 8.1 上自動切換設定檔。** 目前在 Windows 10 版 Microsoft Edge 中提供的自動設定檔切換功能已延伸至舊版 Windows (Windows 7、8 和 8.1)。 如需詳細資訊，請參閱[自動設定檔切換](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)部落格文章。

* **當使用者開始在 Microsoft Edge 附加元件網站上輸入搜尋查詢時，他們會看到自動完成建議。** 「自動完成」可協助使用者快速完成其搜尋查詢，而不需要輸入整個字串。 這將很有幫助，因為使用者不需要記住正確的拼寫，而他們可以從所顯示的可用選項中選擇。

* **移除 HTML5 應用程式快取 API。**  從 Microsoft Edge 版本 86 開始，可啟用離線使用網頁的舊版應用程式快取 API 會從 Microsoft Edge 中移除。 Web 開發人員應該檢閱 [WebDev 文件](https://web.dev/appcache-removal/)，以取得有關將應用程式快取 API 取代為服務工作者的資訊。  重要：您可以要求 [AppCache OriginTrial 權杖](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673)，允許網站在 Microsoft Edge 版本 90 之前繼續使用已取代的應用程式快取 API。

* **安全性：**

  * 安全 DNS (DNS-over-HTTPS) 支援。  從 Microsoft Edge 版本 86 開始，用來控制未受管理裝置上安全 DNS 的設定可供使用。 這些設定無法供受管理裝置上的使用者存取，但是 IT 系統管理員可以使用 [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode) 群組原則來啟用或停用安全 DNS。


* **使用群組原則將自訂影像新增至新的索引標籤頁面 (NTP)。** 從 Microsoft Edge 版本 86 開始，NTP 提供一個選項，可將預設影像以自訂使用者提供的影像取代。 群組原則也支援管理此影像屬性的功能。

* **讓自訂鍵盤快速鍵符合 VS 程式碼。** Microsoft Edge 開發工具現在支援自訂開發工具中的鍵盤快速鍵，使其符合您的編輯器/IDE。 (在 Microsoft Edge 84 中，我們新增了比對開發工具鍵盤快速鍵與 VS Code 的功能。)

* **針對舊版 Windows 和 macOS 取代 [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) 和 [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) 原則。** 這些原則已在 Microsoft Edge 版本 86 中取代，並將於 Microsoft Edge 版本 89 中變得過時。<br>
這些原則會在 Windows 10 上由 [允許遙測][](https://go.microsoft.com/fwlink/?linkid=2099569) 取代，而新的 [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) 原則則用於所有其他平台。 這可讓使用者管理傳送至 Microsoft 的 Windows 7、8、8.1 和 macOS 診斷資料。

* **根據預設 SameSite=Lax Cookie**。 為了改善網頁安全性和隱私權，根據預設會預設 cookie 為[SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)。 這表示 cookie 只會在第一方的上下文中傳送，對於發傳送第三方的要求將被忽略。 這項變更可能會對需要第三方資源的 cookie 才能正常運作的網站造成相容性影響。 若要允許使用這類 cookie，網頁程式開發人員可以標示 cookie，在設定 cookie 時，只要新增清楚的 `SameSite=none` 和 `Secure` 屬性，就能將該 cookie 設定並傳送到第三方上下文。 如果企業希望讓特定網站免于此變更，可以使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) 原則以達成，或可以使用 [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 原則，以退出所有網站的變更。

### 原則更新

#### 新原則

新增了 19 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - 封鎖集錦中服務和匯出目標特定清單的存取權。
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - 預設的感應器設定。
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - 控制 Serial API 的使用方式。
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) - 傳送關於瀏覽器使用狀況的必要和選擇性診斷資料。
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - 允許存取 Enterprise Mode Site List Manager 工具。
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
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) - 封鎖存取 URL 清單。
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) - 定義允許的 URL 清單。
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - 啟用使用者代理程式用戶端提示功能。
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - 限制保留的使用者資料快照數量，以便在緊急復原時使用。

#### 取代的原則

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。

#### 淘汰的原則

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。

#### 原則標題已變更

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - 啟用原生視窗遮蔽。

#### 原則描述已變更

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## 版本 85.0.564.41：8 月 25 日

修正各種錯誤和效能問題。

## 版本 85.0.564.40：8 月 21 日

修正各種錯誤和效能問題。

## 版本 85.0.564.36：8 月 17 日

修正各種錯誤和效能問題。

## 版本 85.0.564.30：8 月 10 日

修正各種錯誤和效能問題。

## 版本 85.0.564.23：8 月 3 日

修正各種錯誤和效能問題。

<!--- Archived to version 85.0.564.18: July 28 ---->

## 另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
