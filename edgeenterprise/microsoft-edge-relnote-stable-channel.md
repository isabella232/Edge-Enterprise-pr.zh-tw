---
title: Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 11/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: fdf0a80af68259d8c36b93b072605dfa0e4893e0
ms.sourcegitcommit: 9a7ece9f4b5892ea6dc8a9b5fa5ebf71c0407f59
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182466"
---
# Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。

> [!NOTE]
> 針對穩定通道，更新會在一或多天內逐步推出。 若要深入了解，請參閱 [Microsoft Edge 更新的漸進式推出](microsoft-edge-update-progressive-rollout.md)。

<!-- begin major 87 --->
## 版本 87.0.664.41：11 月 19 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#november-19-2020)。

### 功能更新

- **自動將不相容網站從 Internet Explorer 重新導向至 Microsoft Edge**。 從 Microsoft Edge 87 穩定版更新開始，在 Internet Explorer 上顯示不相容訊息的公共網站，將自動重新導向至 Microsoft Edge。 若要深入了解及設定此體驗，請參閱[重新導向不相容的網站](https://docs.microsoft.com/deployedge/edge-learnmore-neededge)。

- **kiosk 模式隱私權功能已啟用**。 從 Microsoft Edge 版本 87 開始，有助於企業處理使用者資料隱私權的 kiosk 模式功能將會啟用。 這些功能將啟用一些體驗, 例如在退出時清除使用者資料、刪除下載的檔案，以及在指定的閒置時間後, 重設已設定的啟動體驗。 深入了解如何[設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)

- **依預設啟用購物功能**。 從 Microsoft Edge 版本 87 開始，企業使用者也可以透過在 Edge 中購物獲益。 利用購物功能，Microsoft Edge 可在使用者於線上購物時，協助使用者找到優待券和更優惠的價格。 我們隨著此更新提供優待券體驗，而價格比較將於 Microsoft Edge 87 近期的更新中發佈。 此功能可透過 [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) 原則設定。 請參閱我們的[部落格](https://blogs.windows.com/windowsexperience/2020/11/19/finish-up-that-holiday-shopping-with-new-features-from-microsoft-edge-and-bing/)和[深入了解](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#shopping) Microsoft 購物的相關資訊。

- **預設啟用 ClickOnce 部署**。 預設會在 Microsoft Edge 87 中啟用 ClickOnce，這樣可減少企業部署軟體的障礙，並更能與舊版Microsoft Edge Legacy 瀏覽器行為一致。 從 Microsoft Edge 87 開始，ClickOnceEnabled 原則的 “未設定”狀態將反映已啟用的新預設 ClickOnce 狀態（與之前停用的預設狀態相比）。

- **企業版的新標籤頁（NTP）將生產力與且可自訂的工作相關的摘要內容整合在一起**。 企業版 NTP 加入Microsoft Office 365 生產力頁面, 我們提供在公司或學校帳戶登入的使用者, 有其個人化的個人化及與公司及產業相關的資料來源, 並能組織在同一個頁面中. 使用者將能夠辨識熟悉的 Office 365 內容，以及由 Bing 提供支援的商務用 Microsoft 搜尋。 此外，他們可以從組織的可用內容和模組選擇最相關的內容，以輕鬆自訂 [我的摘要]。 IT 系統管理員可以控制其組織的新聞摘要設定，包括為 Microsoft Edge 新索引標籤頁面選取的產業 (移至 Microsoft 365 系統管理中心)。 [深入了解](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/)

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

已修正各種錯誤和效能問題。

## 版本 86.0.622.58：10 月 29 日

已修正各種錯誤和效能問題。

## 版本 86.0.622.56：10 月 27 日

已修正各種錯誤和效能問題。

## 版本 86.0.622.51：10 月 22 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-22-2020)

## 版本 86.0.622.48：10 月 20 日

已修正各種錯誤和效能問題。

## 版本 86.0.622.43：10 月 15 日

已修正各種錯誤和效能問題。

<!-- begin major 86 -->
## 版本 86.0.622.38：10 月 9 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#october-9-2020)

### 功能更新

* **復原為上一個 Microsoft Edge 版本。** 如果最新版本的 Microsoft Edge 有問題，復原功能可讓系統管理員還原為已知良好的 Microsoft Edge 版本。 **注意：** 穩定版本 86.0.622.38 是您可以復原的第一個版本，這表示穩定版本 87 是準備好要回復的第一個版本。 [深入了解](edge-learnmore-rollback.md)。

* **預設會在整個企業強制啟用同步。**  系統管理員可以使用 [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) 原則，預設為 Azure Active Directory (Azure AD) 帳戶啟用同步。

* **在 Windows 7 和 8.1 上自動切換設定檔。** 目前在 Windows 10 版 Microsoft Edge 中提供的自動設定檔切換功能已延伸至舊版 Windows (Windows 7 和 8.1)。 如需詳細資訊，請參閱[自動設定檔切換](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)部落格文章。

* **根據預設 SameSite=Lax Cookie**。 為了改善網頁安全性和隱私權，根據預設會預設 cookie 為[SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)。 這表示 cookie 只會在第一方的上下文中傳送，對於發傳送第三方的要求將被忽略。 這項變更可能會對需要第三方資源的 cookie 才能正常運作的網站造成相容性影響。 若要允許使用這類 cookie，網頁程式開發人員可以標示 cookie，在設定 cookie 時，只要新增清楚的 `SameSite=none` 和 `Secure` 屬性，就能將該 cookie 設定並傳送到第三方上下文。 如果企業希望讓特定網站免于此變更，可以使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) 原則以達成，或可以使用 [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 原則，以退出所有網站的變更。

* **移除 HTML5 應用程式快取 API。**  從 Microsoft Edge 版本 86 開始，可啟用離線使用網頁的舊版應用程式快取 API 會從 Microsoft Edge 中移除。 Web 開發人員應該檢閱 [WebDev 文件](https://web.dev/appcache-removal/)，以取得有關將應用程式快取 API 取代為服務工作者的資訊。  重要：您可以要求 [AppCache OriginTrial 權杖](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673)，允許網站在 Microsoft Edge 版本 90 之前繼續使用已取代的應用程式快取 API。

* **隱私權與安全性：**

  * **針對舊版 Windows 和 macOS 取代 [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) 和 [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) 原則。** 這些原則已在 Microsoft Edge 版本 86 中取代，並將於 Microsoft Edge 版本 89 中變得過時。<br>
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

<!-- end 86 -->
## 版本 85.0.564.70：10 月 6 日

已修正各種錯誤和效能問題。

## 版本 85.0.564.68：10 月 1 日

已修正各種錯誤和效能問題。

## 版本 85.0.564.63：9 月 23 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-23-2020)

## 版本 85.0.564.51：9 月 9 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#september-9-2020)

## 版本 85.0.564.44：8 月 31 日

已修正各種錯誤和效能問題。
<!-- begin 85 -->
## 版本 85.0.564.41：8 月 27 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-27-2020)

### 功能更新

- **我的最愛和設定的內部部署同步**。 您現在可以在自己的環境中，在 Active Directory 設定檔之間同步處理瀏覽器的我的最愛和設定，不需要進行雲端同步處理。

- **使用 Microsoft Edge 群組原則支援，無需確認提示即可啟動信任網站 + 無需確認即可啟動的應用程式組合。** 已添加的群組原則支援允許管理員添加受信任的網站 + 應用程式組合，無需確認提示即可啟動。 這添加了一項功能，讓管理員為其使用者設定信任通訊協定/原點組合（例如 Microsoft 365 應用程式），從而在瀏覽到包含應用協定的 URL 時禁止確認提示。

- **PDF 螢光筆工具**。 此工具可添加到 PDF 工具列中，方便醒目顯示重要文字。

- **儲存訪問 API 現可用**。 當使用者直接指示允許本來會被流覽器的當前設定阻止的儲存時，可使用此儲存訪問 API 來存取協力廠商內容中的第一方儲存。 如需詳細資訊，請參閱[儲存體存取 API](https://www.chromestatus.com/feature/5612590694662144)。

- **Microsoft Edge 集合現可使用“傳送至 OneNote” **。 所有人都期待能將集合中已收集的資訊傳送至 OneNote，從而追加資訊到更大的專案中，與他人進行協作！ 更重要的是，在 Microsoft Edge 85 中，您能夠將 Microsoft 帳戶和 Azure Active Directory 的內容傳送到 *Mac 版 Office*產品 (Word、Excel 和 OneNote)。

- **開發工具更新**。 如需以下更新的詳細資訊，請參閱 [開發工具新增功能 (Microsoft Edge 85)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools)。

   - Microsoft Edge 開發工具支援 Surface Duo 模擬。 Microsoft Edge 開發工具能夠模擬 Surface Duo，因此可測試 Web 內容在雙屏裝置上的顯示效果。 若要在開發工具中打開此實驗，請在 Windows 上按 Ctrl+Shift+M 或在 macOS 上按 Command+Shift+M 來輸入裝置模式，然後在裝置下拉式清單中選取 Surface Duo。
   - Microsoft Edge 開發工具允許鍵盤快速鍵和 VS Code 相匹配。 Microsoft Edge 開發工具支援自訂開發工具中的鍵盤快速鍵，使其匹配你的編輯器/IDE。 在 Microsoft Edge 85 中，我們添加了匹配開發工具鍵盤快速鍵和 VS Code 的功能。 此變更將有助於增加 VS Code 和開發工具之間的工作效率。

### 原則更新

#### 新原則

新增了 13 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

- [AutoLaunchProtocolsFromOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autolaunchprotocolsfromorigins) - 定義可從列出的源啟動外部應用程式的協定的清單，而無需提示用戶。
- [AutoOpenAllowedForURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenallowedforurls) - AutoOpenFileTypes 可套用的 URL。
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes) - 檔案類型清單應在下載時自動開啟。
- [DefaultSearchProviderContextMenuAccessAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchprovidercontextmenuaccessallowed) - 允許預設搜尋提供程式中的操作功能表搜尋訪問。
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) - 允許由本機信賴起點頒發的 SHA - 1 簽章憑證。
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告。
- [IntensiveWakeUpThrottlingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intensivewakeupthrottlingenabled) - 控制 IntensiveWakeUpThrottling 功能。
- [NewTabPagePrerenderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageprerenderenabled) - 啟用預先載入的新索引標籤頁面，以加快頁面呈現速度。
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox) - 設定新的索引標籤頁面搜尋體驗。
- [PasswordMonitorAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) - 允許使用者在密碼不安全時收到警示提醒。
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) - 啟用 Microsoft Edge 設定檔資料的快取副本。
- [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) - 設定快取設定檔目錄。
- [TLSCsipherSuiteDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tlsciphersuitedenylist) - 指定停用的 TLS 加密套件。

#### 淘汰的原則

- [EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載。
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies)- 允許 WebDriver 覆寫不相容原則。

<!--- END 85 ---->

## 版本 84.0.522.63：8 月 20 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-20-2020)。

## 版本 84.0.522.61：8 月 17 日

已修正各種錯誤和效能問題。

## 版本 84.0.522.59：8 月 11 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#august-11-2020)

## 版本 84.0.522.58：8 月 10 日

已修正各種錯誤和效能問題。

## 版本 84.0.522.52：8 月 1 日

已修正各種錯誤和效能問題。

## 版本 84.0.522.50：7 月 31 日

已修正各種錯誤和效能問題。

## 版本 84.0.522.49：7 月 29 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-29-2020)

## 版本 84.0.522.48：7 月 28 日

已修正各種錯誤和效能問題。

## 版本 84.0.522.44：7 月 23 日

已修正各種錯誤和效能問題。

<!-- begin 84 -->
## 版本 84.0.522.40：7 月 16 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#july-16-2020)

### 功能更新

- 此版本的 Microsoft Edge 可提升 Internet Explorer 模式的網站清單下載時間。 在沒有快取網站清單的情況下，我們將 Internet Explorer 模式網站清單的下載延遲縮短到 0 秒 (從 60 秒等候時間往下縮短)。 如果在下載網站清單之前，Internet Explorer 模式首頁瀏覽需要延遲，我們也新增了針對此案例的群組原則支援。 如需詳細資訊，請參閱 [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) 原則。

- Microsoft Edge 現在可讓使用者在 Windows 10 上「以系統管理員身分執行」登入瀏覽器。 這可協助客戶在 Windows 伺服器上，或在遠端桌面和沙箱案例中執行 Microsoft Edge。

- Microsoft Edge 目前提供全螢幕模式的完整滑鼠支援。 現在，您可以使用滑鼠存取索引標籤、網址列及其他項目，而不需退出全螢幕模式。

- 改善線上購買。 將自訂暱稱新增至儲存的轉帳卡或信用卡。 現在您可以在線上購買時，辨別並區別您的信用卡。 設定轉帳卡或信用卡的暱稱，這樣當您使用 [自動填滿] 來選取付款方式時，就可以選擇正確的卡片。

- 預設會停用 TLS/1.0 和 TLS/1.1。  [SSLVersionMin](https://docs.microsoft.com/deployedge/microsoft-edge-policies#sslversionmin) 原則允許重新啟用 TLS/1.0 和 TLS/1.1。 至少到 Microsoft Edge 版本 88 都還可以使用此原則。 如需詳細資訊，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes)。

- 集錦改善功能：

  - 新增附註功能，可讓您針對集錦中的項目新增附註或註解。 即使您排序集錦中的項目，附註也會組成群組並持續附加到項目中。 若要嘗試這項新功能，請以滑鼠右鍵按一下項目，然後選取 [新增附註]。
  - 您可以變更集錦中的附註背景色彩。 您可以使用色彩編碼來協助您整理資訊和提高生產力。
  - 提供顯著的效能增強功能，可讓您將集錦匯出至 Excel，比起前版 Microsoft Edge 來的更省時。

- 其他 Microsoft Edge API 支援：

  - 已啟用儲存體存取 API 來進行試驗。 此功能會為家用版使用者和企業使用者啟用，並將 [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/deployedge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) 原則設定為 "Full"。 此功能預設會為 Microsoft Edge 穩定通道版本 85 中的所有使用者啟用。
  
    隨著隱私權對使用者的重要性日益增加，對於更嚴格的瀏覽器預設值的要求以及封鎖所有第三方儲存空間存取權等使用者選擇設定越來越普遍。 雖然這些設定可協助改善隱私權，並封鎖未知或不受信任方進行非必要的存取，但它們可能也會造成不必要的負面影響，例如封鎖使用者可能想要查看之內容的存取權 (例如社交媒體和內嵌媒體內容)。

    當使用者直接允許存取可能會由瀏覽器的目前設定封鎖的儲存體時，儲存體存取 API 會允許在第三方環境中存取第一方儲存體。 如需詳細資訊，請參閱[儲存體存取 API](https://www.chromestatus.com/feature/5612590694662144)。

  - 原生檔案系統 API，代表您可以透過原生檔案系統 API 來授與網站編輯檔案或資料夾的權限。

- PDF 改進功能：

  - PDF 的朗讀功能可讓使用者聆聽 PDF 的內容，並同時執行其他對他們而言重要的工作。 它也可協助視聽學習者專注於閱讀內容，讓學習更輕鬆。
  - 改善 PDF 檔案編輯功能。 現在您可以將對 PDF 的編輯儲存回檔案，而不需要在每次編輯 PDF 時儲存複本。

- Microsoft Edge 現在在沈浸式閱讀程式中啟用翻譯功能。 當使用者開啟沈浸式閱讀程式檢視時，會出現將頁面翻譯成所需語言的選項。

- 有多個 DevTools 更新，包括支援自訂鍵盤快速鍵以比對 VS 程式碼和以高對比檢視 DevTools。  如需詳細資訊，請參閱 [DevTools 的新功能 (Microsoft Edge 84)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/05/devtools)。

### 原則更新

#### 新原則

新增了 7 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AppCacheForceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#appcacheforceenabled) - 允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態)。
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) - 設定應用程式防護容器 Proxy 的設定。
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload) - 要求在索引標籤瀏覽前，[企業模式網站清單] 即已可使用。
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled) - 使用 Windows Proxy 解析程式。
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection) - 針對 Internet Explorer 模式設定增強的當機偵測。
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - 要降低 CPU 和耗電量，Microsoft Edge 將偵測視窗何時被其他視窗覆蓋，並將暫停工作繪製像素。
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout) - 針對 [企業模式網站清單]，設定索引標籤瀏覽逾時延遲。

#### 取代的原則

- [AllowSyncXHRInPageDismissal](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsyncxhrinpagedismissal) - 允許頁面在頁面關閉期間傳送同步 XHR 要求。
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - 判斷內建的憑證驗證程式是否將用來驗證伺服器憑證。
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。

#### 淘汰的原則

[ForceNetworkInProcess](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcenetworkinprocess) - 強制網路程式碼在瀏覽器處理程序中執行。

<!-- End 84 -->
## 版本 83.0.478.64：7 月 13 日

已修正各種錯誤和效能問題。

## 版本 83.0.478.61：7 月 7 日

已修正各種錯誤和效能問題。

## 版本 83.0.478.58：6 月 30 日

已修正各種錯誤和效能問題。

## 版本 83.0.478.56：6 月 24 日

已修正各種錯誤和效能問題。

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-24-2020)

## 版本 83.0.478.54：6 月 17 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-17-2020)

## 版本 83.0.478.50：6 月 15 日

已修正各種錯誤和效能問題。

## 版本 83.0.478.45：6 月 4 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#june-4-2020)

## 版本 83.0.478.44：6 月 1 日

已修正各種錯誤和效能問題。

## 版本 83.0.478.37：5 月 21 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-21-2020)

### 功能更新

- Microsoft Edge 更新即將逐步推出。 從現在開始，Microsoft Edge 更新會在幾天內推出給使用者。 使我們能夠保護更多人免於進行錯誤的更新，進而改善您的更新體驗。 如果您是使用者，您將會繼續獲得流暢的自動更新。 如果組織未註冊自動更新，您將不會受到此變更影響。 若要深入了解，請參閱[漸進式更新文章](microsoft-edge-update-progressive-rollout.md)。
- Microsoft Defender SmartScreen 改善：對 Microsoft Defender SmartScreen 服務進行許多改善，例如，改善載入時針對重新導向的惡意網站的防護能力，以及最上層框架封鎖，其使用 Microsoft Defender SmartScreen 安全頁面完全取代惡意網站。 最上層框架封鎖可防止播放惡意網站的音訊和其他媒體，讓您擁有簡易且不會混淆的體驗。

- 為了回應使用者意見反應，使用者現在可以讓特定 Cookie 在瀏覽器關閉時不被自動清除。 如果有使用者不想被登出但仍想要在瀏覽器關閉時清除所有其他 Cookie 的網站，此選項就相當實用。 若要使用此功能，請移至 *edge://settings/clearBrowsingDataOnClose*，並啟用 [Cookie 與其他網站資料] 切換。

- 現在提供「自動設定檔切換」功能，以協助您更輕鬆地在不同設定檔間取得工作內容。 如果您在工作中使用多個設定檔，可以在使用您的個人設定檔時瀏覽至需要輸入公司或學校帳戶驗證的網站，藉此查看設定檔。 當我們偵測到此動作時，將提示您切換為公司設定檔來存取該網站，而不需向它進行驗證。 選擇您要切換的公司設定檔時，該網站就會在您的公司設定檔中開啟。 此設定檔切換功能可協助您將公司與個人資料分開，並協助您更輕鬆地取得工作內容。 如果您不希望該功能提示您切換設定檔，則可以選擇 [不要再問我] 選項，之後就不再提醒您。

- 集錦功能改善：
  - 您可以使用拖放功能，在不開啟集錦的情況下，將項目新增至集錦。 在拖放期間，您也可以選擇集錦清單中您要放置項目的位置。
  - 您可以將多個集錦新增至集錦，而不是一次新增一個項目。 若要新增多個項目，請選取項目，然後將它們拖曳到集錦。 或者，您也可以選取項目並以滑鼠右鍵按一下，然後挑選您需要放置項目的集錦。

- 您可以將 Edge 視窗中的所有索引標籤新增至新的集錦，而不需要個別新增。 若要這麼做，請以滑鼠右鍵按一下任一索引標籤，然後選擇 [將所有索引標籤新增至集錦]。

- 擴充功能同步現在可供使用。 您現在可以在您所有的裝置上同步擴充功能！ 來自 Microsoft 與 Chrome 商店的擴充功能都會與 Microsoft Edge 同步。 若要使用此功能：按一下功能表列上的省略符號 (**...**)，然後選取 [設定]****。 在您的個人檔案下，按一下 [同步]**** 以查看同步選項。 在 [個人檔案/同步]**** 下，使用切換來啟用擴充功能。 您可以使用 [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) 群組原則來停用擴充功能的同步。

- 改善下載管理頁面上針對已封鎖不安全下載的訊息。

- 沉浸式閱讀程式的改善：
  - 我們在沉浸式閱讀程式的詞性體驗中新增了「副詞」的支援。 當您在沉浸式閱讀程式中閱讀文章時，開啟文法檢查工具，並開啟詞性中的「副詞」，即可強調頁面上的所有副詞。
  - 新增可選取網頁上任何內容，並在沉浸式閱讀器程式中開啟的功能。 這可讓使用者在所有網站上使用沉浸式閱讀程式和所有學習工具，例如「行聚焦」和「大聲朗讀」。

- Link Doctor 會在使用者誤植 URL 時，為使用者提供主機校正和搜尋查詢。 例如： <br>
使用者將「powerbi」誤植為 powerbbi.com。 Link Doctor 會建議 powerbi.com 做為修正，並建立連結以搜尋「powerbbi」，以免使用者要尋找不同內容。

- 允許使用者儲存其決定以啟動特定網站的外部通訊協定。 使用者可以設定 [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) 原則，以啟用或停用此功能。

- 使用者可以直接從 Microsoft Edge **[設定]** 將 Microsoft Edge 設為其預設瀏覽器。 這可讓使用者更輕鬆地在瀏覽器本身的內容內變更其預設瀏覽器，而不需要在作業系統設定中搜尋。 若要使用此功能，請移至 *edge://settings/defaultBrowser*，然後按一下 **[設為預設]**。

- 多個 DevTools 更新，包括新的遠端偵錯支援、UI 改善等。 如需詳細資訊，請參閱 [DevTools 的新功能 (Microsoft Edge 83)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools)。

- MCAS (Microsoft 雲端存取安全性) 警告案例現已推出。 這可讓系統管理員設定警告，這是新的 MCAS 區塊類別，使用者可以在此覆寫 MCAS 封鎖頁面。 MDATP E5 區塊與 Microsoft Edge 中的 SmartScreen 封鎖原本即整合在一起，以獲得流暢的體驗。 這項體驗提供一個全頁的紅色區塊，其中顯示 [此網站遭到您的組織封鎖] 訊息，而不只是顯示快顯通知。

- 在頁面關閉時禁止同步 XmlHttpRequest。 在卸載網頁期間傳送的同步 XmlHttpRequests 將會被移除。 此變更可改善瀏覽器效能和可靠性，但可能會影響尚未更新的 Web 應用程式，以使用更新式的 Web API，包括 sendBeacon 和擷取。 可停用此變更並允許在頁面關閉期間同步 XHR 的 [群組原則] 將可使用，直到 Microsoft Edge 88 為止。 如需詳細資訊，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](https://docs.microsoft.com/microsoft-edge/web-platform/site-impacting-changes)。

### 原則更新

#### 新原則

新增了 15 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AllowSurfGame](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowsurfgame) - 允許衝浪遊戲。
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls) - 設定 Microsoft Edge 將嘗試建立權杖繫結的網站清單。
- [BingAdsSuppression](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#bingadssuppression) - 封鎖 Bing 搜尋結果中的所有廣告。
- [BuiltinCertificateVerifierEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#builtincertificateverifierenabled) - 判斷內建的憑證驗證程式是否將用來驗證伺服器憑證。
- [ClearCachedImagesAndFilesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearcachedimagesandfilesonexit) - 當 Microsoft Edge 關閉時，清除快取的影像和檔案。
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare) - 設定共用體驗。
- [DeleteDataOnMigration](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#deletedataonmigration) - 移轉時刪除舊瀏覽器資料。
- [DnsOverHttpsMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpsmode) - 控制 DNS-over-HTTPS 模式。
- [DnsOverHttpsTemplates](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsoverhttpstemplates) - 指定所需 DNS-over-HTTPS 解析程式的 URI 範本。
- [FamilySafetySettingsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#familysafetysettingsenabled) - 允許使用者設定家長監護服務。
- [LocalProvidersEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#localprovidersenabled) - 允許來自本機提供者的建議。
- [ScrollToTextFragmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#scrolltotextfragmentenabled) - 啟用捲動至 URL 片段中指定的文字。
- [ScreenCaptureAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#screencaptureallowed) - 允許或拒絕螢幕擷取。
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) - 設定要從同步中除的類型清單。
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - 啟用隱藏原生視窗。

#### 取代的原則

下列原則會持續在此版本中運作。 在未來版本中，它會變得「過時」。

[EnableDomainActionsDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載

<!-- end 83 -->

## 版本 81.0.416.77：5 月 18 日

已修正各種錯誤和效能問題。

## 版本 81.0.416.72：5 月 7 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#may-7-2020)

## 版本 81.0.416.68：4 月 29 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-29-2020)

## 版本 81.0.416.64：4 月 23 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-23-2020)

## 版本 81.0.416.58：4 月 17 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-17-2020)

## 版本 81.0.416.53：4 月 13 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-13-2020)

### 功能更新

- 新增對 Windows 資訊保護 (WIP) 的支援，WIP 可協助企業保護敏感性資料免於未經授權的揭露。 [深入了解](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection)。

- 集合現在可供使用。 可以按一下位址列旁邊的 [集合] 圖示來開始。 此動作會開啟 [集合] 窗格，您可以在其中建立、編輯和檢視集合。 我們根據您會在網路上執行的動作設計這些集合。 如果您是購物者、旅行者、教師或學生，則集合可協助您。 [深入了解](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97)。

- 允許從 Microsoft Edge 工具列移除 (從工具列隱藏) [集合] 按鈕，以獲得一致性。

- 內部部署 Active Directory 帳戶的自動登入只會針對開啟該功能的組織。  如果使用者已使用內部部署 AD 帳戶登入，他們將可以登出該帳戶。 只有在使用者的主要帳戶是 Microsoft 帳戶或 Azure Active Directory 帳戶的情況下，使用者才會在其作業系統上使用主要帳戶自動登入。 系統管理員可以使用 ConfigureOnPremisesAccountAutoSignIn 原則，將使用內部部署 AD 帳戶自動登入啟用。

- 應用程式防護。 容器中目前提供延伸模組的支援。

- 新增訊息以在使用者瀏覽至設定為以 Internet Explorer 模式開啟的頁面時，通知使用者 Internet Explorer 未安裝。

- 更新 Microsoft Edge DevTools 中的 3D 檢視工具，加上新功能，以協助您偵錯 z 索引堆疊內容。 3D 檢視會使用色彩和堆疊顯示 DOM (文件物件模型) 深度的外觀，而 z 索引檢視可協助您區隔頁面的不同堆疊內容。 [深入了解](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/)。

- 將 F12 開發工具以 10 個新語言當地語系化，讓它們符合其餘瀏覽器所使用的語言。 [深入了解](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/)。

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

### 原則更新

#### 新原則

新增了 11 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled) - 啟用 InPrivate 和來賓設定檔的環境驗證。 
- [AudioSandboxEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#audiosandboxenabled) - 允許音訊沙箱執行。
- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) - 使用預設的查閱者原則 no-referrer-when-downgrade。
- [GloballyScopeHTTPAuthCacheEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#globallyscopehttpauthcacheenabled) - 啟用全域範圍的 HTTP 驗證快取。
- [ImportExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importextensions) - 允許匯入延伸模組。
- [ImportCookies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importcookies) - 允許匯入 Cookie。
- [ImportShortcuts](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#importshortcuts) - 允許匯入快速鍵。
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect) - 指定從 Internet Explorer 模式頁面啟動時，「頁面內」瀏覽至未設定網站的行為。
- [StricterMixedContentTreatmentEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。
- [TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) - 設定在沒有 Azure AD 網域帳戶時，自動使用 Active Directory 網域帳戶登入。

#### 原則名稱和標題變更

原則 `OmniboxMSBProviderEnabled` 變更為 [AddressBarMicrosoftSearchInBingProviderEnabled](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#addressbarmicrosoftsearchinbingproviderenabled) - 該原則的標題為「在網址列的 Bing 建議中啟用 Microsoft Search」。

#### 取代的原則

下列原則會持續在此版本中運作。 在未來版本中，它們會變得「過時」。

- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容。

#### 已解決的問題

- 修正 Microsoft Edge 上的 IE 模式導致下載對話方塊持續顯示的問題 (甚至在檔案下載之後亦然)。
- 修正已在 IE 模式中觸發開啟新 IE 模式索引標籤的頁面時，Microsoft Edge 捨棄工作階段 Cookie 的問題。

## 版本 80.0.361.111：4 月 7 日

已修正各種錯誤和效能問題。

## 版本 80.0.361.109：4 月 1 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#april-1-2020)

## 版本 80.0.361.69：3 月 19 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-19-2020)

## 版本 80.0.361.66：3 月 4 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#march-4-2020)

## 版本 80.0.361.62：2 月 25 日

安全性更新列於[此處](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-25-2020)

## 版本 80.0.361.57：2 月 20 日

安全性更新列於[此處](https://docs.microsoft.com/DeployEdge/microsoft-edge-relnotes-security#february-20-2020)

## 版本 80.0.361.56：2 月 19 日

已修正各種錯誤和效能問題。

## 版本 80.0.361.54：2 月 14 日

### 已解決的問題

- 修正無法將密碼、付款和 Cookie 匯入 Microsoft Edge 的問題。

## 版本 80.0.361.50：2 月 11 日

已修正各種錯誤和效能修正。

## 版本 80.0.361.48：2 月 7 日

安全性更新列於[此處](https://docs.microsoft.com/deployedge/microsoft-edge-relnotes-security#february-7-2020)

### 功能更新

- 新增 SmartScreen 保護，以避免下載潛在有害的應用程式。 [深入了解](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus)
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

### 原則更新

#### 新原則

新增了 16 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

- [AlternateErrorPagesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#alternateerrorpagesenabled) - 找不到網頁時建議相似頁面。
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting) - 控制不安全內容例外的使用方式。
- [DNSInterceptionChecksEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#dnsinterceptionchecksenabled) - 已啟用 DNS 攔截檢查。
- [HideFirstRunExperience](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hidefirstrunexperience) - 隱藏初次執行體驗與啟動顯示畫面。
- [InsecureContentAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentallowedforurls) - 允許指定網站上的不安全內容。
- [InsecureContentBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecurecontentblockedforurls) - 封鎖指定網站上的不安全內容。
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) - 啟用預設舊版 SameSite Cookie 行為設定。
- [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) - 還原為指定網站上 Cookie 的舊版 SameSite 行為。
- [PaymentMethodQueryEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#paymentmethodqueryenabled) - 允許網站查詢可用的付款方式。
- [PersonalizationReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#personalizationreportingenabled) - 透過將瀏覽歷程記錄傳送至 Microsoft，允許個人化廣告、搜尋與新聞。
- [PinningWizardAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pinningwizardallowed) - 允許 [釘選到工作列] 精靈。
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled) - 設定 Microsoft Defender SmartScreen 來封鎖潛在有害的應用程式。
- [TotalMemoryLimitMb](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#totalmemorylimitmb) - 針對單一 Microsoft Edge 執行個體可以使用的記憶體設定 MB 限制。
- [WebAppInstallForceList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webappinstallforcelist) - 設定強制安裝的 Web 應用程式清單。
- [WebComponentsV0Enabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebRtcLocalIpsAllowedUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalipsallowedurls) - 透過 WebRTC 管理本機 IP 位址的暴露程度。

#### 取代的原則

已取代下列原則。

- [NewTabPageCompanyLogo](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagecompanylogo) - 設定新的索引標籤頁面公司標誌。

### 已解決的問題

- 已修正音訊在 Citrix 環境中無法運作的問題。
- 已修正 Microsoft Edge 與舊版 Microsoft Edge 並存體驗中斷舊版連結的問題。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
