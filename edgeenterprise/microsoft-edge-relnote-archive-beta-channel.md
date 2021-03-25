---
title: 封存的 Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/17/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 封存的 Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: 3670d7225095a3f33c26e96e886e975d4bb703e0
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448017"
---
# <a name="archived-release-notes-for-microsoft-edge-beta-channel"></a>封存的 Microsoft Edge Beta 通道的版本資訊

這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。

<!-- begin major 87 -->
## <a name="version-87066412-october-20"></a>版本 87.0.664.12：10 月 20 日

### <a name="feature-updates"></a>功能更新

- **Kiosk 模式隱私權功能已**啟用。 從 Microsoft Edge 版本 87 kiosk 模式功能開始，將會對企業的使用者資料隱私權提供協助。 這些功能將啟用一些體驗, 例如在退出時清除使用者資料、刪除下載的檔案，以及在指定的閒置時間後, 重設已設定的啟動體驗。 深入瞭解如何 [設定 Microsoft Edge kiosk 模式](./microsoft-edge-configure-kiosk-mode.md)
- **預設啟用 ClickOnce的 部署**。 預設會在 Microsoft Edge 87 中啟用 ClickOnce，這樣可減少企業部署軟體的障礙，並更能與舊版Microsoft Edge Legacy 瀏覽器行為一致。 從 Microsoft Edge 87 開始，ClickOnceEnabled 原則的 “未設定”狀態將反映已啟用的新預設 ClickOnce 狀態 (與之前停用的預設狀態相比)。
- **企業版的新標籤頁 (NTP) 將生產力與且可自訂的工作相關的摘要內容整合在一起**。 企業版 NTP 加入Microsoft Office 365 生產力頁面, 我們提供在公司或學校帳戶登入的使用者, 有其個人化的個人化及與公司及產業相關的資料來源, 並能組織在同一個頁面中. 使用者將能夠識別熟悉的Microsoft Office 365 內容, 和由 Bing 所主導的Microsoft 搜尋 Microsoft Search for Business。。 此外，他們可以輕鬆地轉到自訂的＂我的摘要＂，其中包含與使用者、公司或行業相關的內容和模組，以及組織所提供的其他摘要。 [進一步瞭解](/microsoft-365/admin/manage/manage-industry-news?preserve-view=true&view=o365-worldwide)。

- **隱私權與安全性：**

  - 支援政策設定網站的 TLS Token Binding 權杖綁定。 TLS Token binding 權杖綁定可協助防止權杖被竊取攻擊，以確保無法從最初設定cookie的設備以外的其他設備重複使用。 使用 TLS 權杖綁定需設定 [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls) 規定，並要求列出的網站支援這項功能。

- **鍵盤支持PDF 檔案上的螢光筆功能**. 使用者可以使用鍵盤鍵來醒目提示 PDF 中的任何文字。

- **列印:**

  - 選擇雙面列印時要翻轉的那一面。 當雙面列印時，使用者可以選擇在紙張的長邊或短邊翻轉。
  - 選擇企業的列印光柵化模式。 控制將Microsoft Edge 列印到一個 Windows 上的非PostScript 印表機。 有時需將非 PostScript 印表機上的列印工作光柵化才能正確列印。 列印選項為「完全」和「快速」。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 10 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列原則。

- [ConfigureFriendlyURLFormat](./microsoft-edge-policies.md#configurefriendlyurlformat) -設定從 Microsoft Edge 複製的預設貼上 Url 格式，並判斷使用者是否可以使用其他格式設定。
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled) - 啟用Microsoft Edge 中的 Shopping in Microsoft Edge Enabled 。
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](./microsoft-edge-policies.md#hideinternetexplorerredirectuxforincompatiblesitesenabled) -隱藏一次性重新導向對話方塊和 Microsoft Edge 標題。
- [KioskAddressBarEditingEnabled](./microsoft-edge-policies.md#kioskaddressbareditingenabled) -設定位址欄編輯以給 kiosk 模式有公眾流覽體驗。
- [KioskDeleteDownloadsOnExit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) - Microsoft Edge 關閉時，刪除以 kiosk 會話方式下載的檔案。
- [PasswordRevealEnabled](./microsoft-edge-policies.md#passwordrevealenabled) -啟用密碼顯示按鈕。
- [RedirectSitesFromInternetExplorerPreventBHOInstall](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerpreventbhoinstall) -禁止安裝 BHO 以將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。
- [RedirectSitesFromInternetExplorerRedirectMode](./microsoft-edge-policies.md#redirectsitesfrominternetexplorerredirectmode) -將不兼容的網站從Internet Explorer重導向到Microsoft Edge。
- [SpeechRecognitionEnabled](./microsoft-edge-policies.md#speechrecognitionenabled) -設定語音辨識。
- [WebCaptureEnabled](./microsoft-edge-policies.md#webcaptureenabled) -啟用 Microsoft Edge 中的網頁擷取功能。

#### <a name="deprecated-policy"></a>已被取代的政策

[NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype) -設定 Microsoft Edge 新增索引標籤頁面體驗。

#### <a name="obsoleted-policy"></a>淘汰的原則

[EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures) -在有限時間內重新啟用已棄用的網頁平臺功能。

<!-- end major 87 -->

## <a name="version-86062243-october-16"></a>版本 86.0.622.43：10 月 16 日

修正各種錯誤和效能問題。

## <a name="version-86062236-october-7"></a>版本 86.0.622.36：10 月 7 日

修正各種錯誤和效能問題。

## <a name="version-86062231-october-1"></a>版本 86.0.622.31：10 月 1 日

修正各種錯誤和效能問題。

## <a name="version-86062228-september-28"></a>版本 86.0.622.28：9 月 28 日

修正各種錯誤和效能問題。

## <a name="version-86062215-september-14"></a>版本 86.0.622.15：9 月 14 日

修正各種錯誤和效能問題。
<!-- major 86 -->
## <a name="version-86062211-september-9"></a>版本 86.0.622.11：9 月 9 日

### <a name="feature-updates"></a>功能更新

* **Internet Explorer 模式：**

   * 讓使用者使用 Microsoft Edge 使用者介面 (UI) 在 Internet Explorer 模式中測試網站。 從 Microsoft Edge 版本 86 開始，系統管理員可以啟用一個 UI 選項，讓其使用者可以在 Internet Explorer 模式中載入索引標籤，以用於測試目的或做為權宜之計，直到將網站新增至網站清單 XML 為止。

* **使用下載管理員來刪除磁碟上的下載項目。** 使用者現在可以在不離開瀏覽器的情況下，從磁碟中刪除其下載的檔案。 在下載架子或下載頁面的操作功能表中，有新的 [刪除下載] 功能。

* **復原為上一個 Microsoft Edge 版本。** 如果最新版本的 Microsoft Edge 有問題，復原功能可讓系統管理員還原為已知良好的 Microsoft Edge 版本。
[進一步瞭解](edge-learnmore-rollback.md)。

* **預設會在整個企業強制啟用同步。**  系統管理員可以使用 [ForceSync](./microsoft-edge-policies.md#forcesync) 原則，預設為 Azure Active Directory (Azure AD) 帳戶啟用同步。

* **PDF 更新：**

  * PDF 文件的目錄。 從版本 86 開始，Microsoft Edge 已新增對目錄的支援，讓使用者能輕鬆瀏覽 PDF 文件。
  * 在小型板型規格螢幕上存取所有 PDF 功能。 在使用小型螢幕的裝置上存取 Microsoft Edge PDF 閱讀程式的所有功能。
  * PDF 檔案上螢光筆的手寫筆支援。 透過此更新，使用者可以使用數位筆直接在 PDF 檔案上將文字醒目提示，就像使用實體螢光筆和紙張的方式一樣。
  * 改善 PDF 捲動。 您現在可以在瀏覽長篇的 PDF 文件時，體驗不間斷的捲動。

* **在 Windows 7、8 和 8.1 上自動切換設定檔。** 目前在 Windows 10 版 Microsoft Edge 中提供的自動設定檔切換功能已延伸至舊版 Windows (Windows 7、8 和 8.1)。 如需詳細資訊，請參閱[自動設定檔切換](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/)部落格文章。

* **當使用者開始在 Microsoft Edge 附加元件網站上輸入搜尋查詢時，他們會看到自動完成建議。** 「自動完成」可協助使用者快速完成其搜尋查詢，而不需要輸入整個字串。 這將很有幫助，因為使用者不需要記住正確的拼寫，而他們可以從所顯示的可用選項中選擇。

* **移除 HTML5 應用程式快取 API。**  從 Microsoft Edge 版本 86 開始，可啟用離線使用網頁的舊版應用程式快取 API 會從 Microsoft Edge 中移除。 Web 開發人員應該檢閱 [WebDev 文件](https://web.dev/appcache-removal/)，以取得有關將應用程式快取 API 取代為服務工作者的資訊。  重要：您可以要求 [AppCache OriginTrial 權杖](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673)，允許網站在 Microsoft Edge 版本 90 之前繼續使用已取代的應用程式快取 API。

* **安全性：**

  * 安全 DNS (DNS-over-HTTPS) 支援。  從 Microsoft Edge 版本 86 開始，用來控制未受管理裝置上安全 DNS 的設定可供使用。 這些設定無法供受管理裝置上的使用者存取，但是 IT 系統管理員可以使用 [dnsoverhttpsmode](./microsoft-edge-policies.md#dnsoverhttpsmode) 群組原則來啟用或停用安全 DNS。


* **使用群組原則將自訂影像新增至新的索引標籤頁面 (NTP)。** 從 Microsoft Edge 版本 86 開始，NTP 提供一個選項，可將預設影像以自訂使用者提供的影像取代。 群組原則也支援管理此影像屬性的功能。

* **讓自訂鍵盤快速鍵符合 VS 程式碼。** Microsoft Edge 開發工具現在支援自訂開發工具中的鍵盤快速鍵，使其符合您的編輯器/IDE。 (在 Microsoft Edge 84 中，我們新增了比對開發工具鍵盤快速鍵與 VS Code 的功能。)

* **針對舊版 Windows 和 macOS 取代 [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) 和 [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) 原則。** 這些原則已在 Microsoft Edge 版本 86 中取代，並將於 Microsoft Edge 版本 89 中變得過時。<br>
這些原則會在 Windows 10 上由 [允許遙測][](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 取代，而新的 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則則用於所有其他平台。 這可讓使用者管理傳送至 Microsoft 的 Windows 7、8、8.1 和 macOS 診斷資料。

* **根據預設 SameSite=Lax Cookie**。 為了改善網頁安全性和隱私權，根據預設會預設 cookie 為[SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite)。 這表示 cookie 只會在第一方的上下文中傳送，對於發傳送第三方的要求將被忽略。 這項變更可能會對需要第三方資源的 cookie 才能正常運作的網站造成相容性影響。 若要允許使用這類 cookie，網頁程式開發人員可以標示 cookie，在設定 cookie 時，只要新增清楚的 `SameSite=none` 和 `Secure` 屬性，就能將該 cookie 設定並傳送到第三方上下文。 如果企業希望讓特定網站免于此變更，可以使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabledfordomainlist) 原則以達成，或可以使用 [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled) 原則，以退出所有網站的變更。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 19 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [CollectionsServicesAndExportsBlockList](./microsoft-edge-policies.md#collectionsservicesandexportsblocklist) - 封鎖集錦中服務和匯出目標特定清單的存取權。
- [DefaultSensorsSetting](./microsoft-edge-policies.md#defaultsensorssetting) - 預設的感應器設定。
- [DefaultSerialGuardSetting](./microsoft-edge-policies.md#defaultserialguardsetting) - 控制 Serial API 的使用方式。
- [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) - 傳送關於瀏覽器使用狀況的必要和選擇性診斷資料。
- [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) - 允許存取 Enterprise Mode Site List Manager 工具。
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
- [URLBlocklist](./microsoft-edge-policies.md#urlblocklist) - 封鎖存取 URL 清單。
- [URLAllowlist](./microsoft-edge-policies.md#urlallowlist) - 定義允許的 URL 清單。
- [UserAgentClientHintsEnabled](./microsoft-edge-policies.md#useragentclienthintsenabled) - 啟用使用者代理程式用戶端提示功能。
- [UserDataSnapshotRetentionLimit](./microsoft-edge-policies.md#userdatasnapshotretentionlimit) - 限制保留的使用者資料快照數量，以便在緊急復原時使用。

#### <a name="deprecated-policies"></a>取代的原則

- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。

#### <a name="obsoleted-policy"></a>淘汰的原則

[TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。

#### <a name="policy-caption-changed"></a>原則標題已變更

[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 啟用原生視窗遮蔽。

#### <a name="policy-description-changed"></a>原則描述已變更

- [AdsSettingForIntrusiveAdsSites](./microsoft-edge-policies.md#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](./microsoft-edge-policies.md#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](./microsoft-edge-policies.md#autoimportatfirstrun)
- [AutoOpenFileTypes](./microsoft-edge-policies.md#autoopenfiletypes)
- [BrowserSignin](./microsoft-edge-policies.md#browsersignin)
- [ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) 
- [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](./microsoft-edge-policies.md#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)
- [ConfigureShare](./microsoft-edge-policies.md#configureshare)
- [CookiesAllowedForUrls](./microsoft-edge-policies.md#cookiesallowedforurls)
- [CustomHelpLink](./microsoft-edge-policies.md#customhelplink)
- [DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting)
- [DefaultGeolocationSetting](./microsoft-edge-policies.md#defaultgeolocationsetting)
- [DefaultImagesSetting](./microsoft-edge-policies.md#defaultimagessetting)
- [DefaultInsecureContentSetting](./microsoft-edge-policies.md#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](./microsoft-edge-policies.md#defaultjavascriptsetting)
- [DefaultNotificationsSetting](./microsoft-edge-policies.md#defaultnotificationssetting)
- [DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [DefaultSearchProviderEnabled](./microsoft-edge-policies.md#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](./microsoft-edge-policies.md#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](./microsoft-edge-policies.md#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)
- [EnableSha1ForLocalAnchors](./microsoft-edge-policies.md#enablesha1forlocalanchors)
- [DownloadRestrictions](./microsoft-edge-policies.md#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](./microsoft-edge-policies.md#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](./microsoft-edge-policies.md#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](./microsoft-edge-policies.md#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist)
- [ForceBingSafeSearch](./microsoft-edge-policies.md#forcebingsafesearch)
- [ForceYouTubeRestrict](./microsoft-edge-policies.md#forceyoutuberestrict)
- [HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage)
- [HomepageLocation](./microsoft-edge-policies.md#homepagelocation)
- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](./microsoft-edge-policies.md#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](./microsoft-edge-policies.md#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](./microsoft-edge-policies.md#networkpredictionoptions)
- [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)
- [NewTabPageSearchBox](./microsoft-edge-policies.md#newtabpagesearchbox)
- [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](./microsoft-edge-policies.md#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](./microsoft-edge-policies.md#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](./microsoft-edge-policies.md#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](./microsoft-edge-policies.md#pluginsallowedforurls)
- [PluginsBlockedForUrls](./microsoft-edge-policies.md#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [RegisteredProtocolHandlers](./microsoft-edge-policies.md#registeredprotocolhandlers)
- [RelaunchNotification](./microsoft-edge-policies.md#relaunchnotification)
- [RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup)
- [RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls)
- [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern)
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)
- [SmartScreenAllowListDomains](./microsoft-edge-policies.md#smartscreenallowlistdomains)
- [SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](./microsoft-edge-policies.md#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)
- [TrackingPrevention](./microsoft-edge-policies.md#trackingprevention)
- [WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling)

<!-- end 86 -->

## <a name="version-85056441-august-25"></a>版本 85.0.564.41：8 月 25 日

修正各種錯誤和效能問題。

## <a name="version-85056440-august-21"></a>版本 85.0.564.40：8 月 21 日

修正各種錯誤和效能問題。

## <a name="version-85056436-august-17"></a>版本 85.0.564.36：8 月 17 日

修正各種錯誤和效能問題。

## <a name="version-85056430-august-10"></a>版本 85.0.564.30：8 月 10 日

修正各種錯誤和效能問題。

## <a name="version-85056423-august-3"></a>版本 85.0.564.23：8 月 3 日

已修正各種錯誤和效能問題。
<!-- major 85 -->
## <a name="version-85056418-july-28"></a>版本 85.0.564.18：7 月 28 日

### <a name="feature-updates"></a>功能更新

- **我的最愛和設定的內部部署同步**。 您現在可以在自己的環境中，在 Active Directory 設定檔之間同步處理瀏覽器的我的最愛和設定，不需要進行雲端同步處理。

- **使用 Microsoft Edge 群組原則支援，無需確認提示即可啟動信任網站 + 應用程式組合。** 已添加的群組原則支援允許管理員添加受信任的網站 + 應用程式組合，無需確認提示即可啟動。 這添加了一項功能，讓管理員為其使用者設定信任通訊協定/原點組合（例如 Microsoft 365 應用程式），從而在瀏覽到包含應用協定的 URL 時禁止確認提示。

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
- [TLSCipherSuiteDenyList](./microsoft-edge-policies.md#tlsciphersuitedenylist) - 指定欲停用的 TLS 加密套件。

#### <a name="obsoleted-policies"></a>已淘汰的原則

- [EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載。
- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies)- 允許 WebDriver 覆寫不相容原則。

<!--- END ---->

## <a name="version-84052235-july-9"></a>版本 84.0.522.35：7 月 9 日

修正各種錯誤和效能問題。

## <a name="version-84052228-june-26"></a>版本 84.0.522.28：6 月 26 日

修正各種錯誤和效能問題。

## <a name="version-84052226-june-24"></a>版本 84.0.522.26：6 月 24 日

修正各種錯誤和效能問題。

## <a name="version-84052220-june-15"></a>版本 84.0.522.20：6 月 15 日

修正各種錯誤和效能問題。

## <a name="version-84052215-june-8"></a>版本 84.0.522.15：6 月 8 日

修正各種錯誤和效能問題。

## <a name="version-84052211-june-2"></a>版本 84.0.522.11：6 月 2 日

### <a name="feature-updates"></a>功能更新

- 此版本的 Microsoft Edge 可提升 Internet Explorer 模式的網站清單下載時間。  在沒有快取網站清單的情況下，我們將 Internet Explorer 模式網站清單的下載延遲縮短到 0 秒 (從 60 秒等候時間往下縮短)。 如果在下載網站清單之前，Internet Explorer 模式首頁瀏覽需要延遲，我們也新增了針對此案例的群組原則支援。 如需詳細資訊，請參閱 [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) 原則。

- Microsoft Edge 現在可讓使用者在 Windows 10 上「以系統管理員身分執行」登入瀏覽器。 這可協助客戶在 Windows 伺服器上，或在遠端桌面和沙箱案例中執行 Microsoft Edge。

- Microsoft Edge 目前提供全螢幕模式的完整滑鼠支援。 現在，您可以使用滑鼠存取索引標籤、網址列及其他項目，而不需退出全螢幕模式。

- 改善線上購買。 將自訂暱稱新增至儲存的轉帳卡或信用卡。 現在您可以在線上購買時，辨別並區別您的信用卡。 設定轉帳卡或信用卡的暱稱，這樣當您使用 [自動填滿] 來選取付款方式時，就可以選擇正確的卡片。

- 預設會停用 TLS/1.0 和 TLS/1.1。 若要協助探索受影響的網站，您可以設定 *edge://flags/#display-legacy-tls-warnings* 旗標，讓 Microsoft Edge 在載入需要舊版 TLS 通訊協定的頁面時，顯示不會封鎖的「不安全」通知。 [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) 原則允許重新啟用 TLS/1.0 和 TLS/1.1。 至少到 Microsoft Edge 版本 88 都還可以使用此原則。 如需詳細資訊，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。

- 集錦改善功能：

  - 新增附註功能，可讓您針對集錦中的項目新增附註或註解。 即使您排序集錦中的項目，附註也會組成群組並持續附加到項目中。 若要嘗試這項新功能，請以滑鼠右鍵按一下項目，然後選取 [新增附註]。
  - 您可以變更集錦中的附註背景色彩。 您可以使用色彩編碼來協助您整理資訊和提高生產力。
  - 提供顯著的效能增強功能，可讓您將集錦匯出至 Excel，比起前版 Microsoft Edge 來的更省時。

- 其他 Microsoft Edge API 支援：

  - 儲存空間存取 API。 當使用者直接允許存取儲存空間時，此 API 允許在第三方情境下存取第一方儲存空間，否則將被瀏覽器的目前設定封鎖。

    隨著隱私權對使用者的重要性日益增加，對於更嚴格的瀏覽器預設值的要求以及封鎖所有第三方儲存空間存取權等使用者選擇設定越來越普遍。 雖然這些設定可協助改善隱私權，並封鎖未知或不受信任方進行非必要的存取，但它們可能也會造成不必要的負面影響，例如封鎖使用者可能想要查看之內容的存取權 (例如社交媒體和內嵌媒體內容)。

  - 原生檔案系統 API，代表您可以透過原生檔案系統 API 來授與網站編輯檔案或資料夾的權限。

- PDF 改進功能：

  - PDF 的朗讀功能可讓使用者聆聽 PDF 的內容，並同時執行其他對他們而言重要的工作。 它也可協助視聽學習者專注於閱讀內容，讓學習更輕鬆。
  - 改善 PDF 檔案編輯功能。 現在您可以將對 PDF 的編輯儲存回檔案，而不需要在每次編輯 PDF 時儲存複本。

- Microsoft Edge 現在在沈浸式閱讀程式中啟用翻譯功能。 當使用者開啟沈浸式閱讀程式檢視時，會出現將頁面翻譯成所需語言的選項。

- DevTools 支援自訂鍵盤快速鍵，以符合包括 VS 程式碼的編輯器/IDE。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 5 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

- [AppCacheForceEnabled](./microsoft-edge-policies.md#appcacheforceenabled) - 允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態)。
- [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) - 應用程式防護容器 Proxy。
- [DelayNavigationsForInitialSiteListDownload](./microsoft-edge-policies.md#delaynavigationsforinitialsitelistdownload) - 要求在索引標籤瀏覽前，[企業模式網站清單] 即已可使用。
- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 啟用隱藏原生視窗。
- [NavigationDelayForInitialSiteListDownloadTimeout](./microsoft-edge-policies.md#navigationdelayforinitialsitelistdownloadtimeout) - 針對 [企業模式網站清單]，設定索引標籤瀏覽逾時延遲。

#### <a name="deprecated-policies"></a>取代的原則

- [AllowSyncXHRInPageDismissal](./microsoft-edge-policies.md#allowsyncxhrinpagedismissal) - 允許頁面在頁面關閉期間傳送同步 XHR 要求。
- [BuiltinCertificateVerifierEnabled](./microsoft-edge-policies.md#builtincertificateverifierenabled) - 判斷內建的憑證驗證程式是否將用來驗證伺服器憑證。
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。

#### <a name="obsoleted-policy"></a>淘汰的原則

[ForceNetworkInProcess](./microsoft-edge-policies.md#forcenetworkinprocess) - 強制網路程式碼在瀏覽器處理程序中執行。

<!-- end 84 -->

## <a name="version-83047844-june-1"></a>版本 83.0.478.44：6 月 1 日

修正各種錯誤和效能問題。

## <a name="version-83047837-may-20"></a>版本 83.0.478.37：5 月 20 日

修正各種錯誤和效能問題。

## <a name="version-83047833-may-15"></a>版本 83.0.478.33：5 月 15 日

修正各種錯誤和效能問題。

## <a name="version-83047828-may-7"></a>版本 83.0.478.28：5 月 7 日

修正各種錯誤和效能問題。

## <a name="version-83047825-may-4"></a>版本 83.0.478.25：5 月 4 日

修正各種錯誤和效能問題。

## <a name="version-83047818-april-27"></a>版本 83.0.478.18：4 月 27 日

修正各種錯誤和效能問題。

## <a name="version-83047813-april-22"></a>版本 83.0.478.13：4 月 22 日

### <a name="feature-updates"></a>功能更新

- Microsoft Defender SmartScreen 改善：對 Microsoft Defender SmartScreen 服務進行許多改善，例如，改善載入時針對重新導向的惡意網站的防護能力，以及最上層框架封鎖，其使用 Microsoft Defender SmartScreen 安全頁面完全取代惡意網站。 最上層框架封鎖可防止播放惡意網站的音訊和其他媒體，讓您擁有簡易且不會混淆的體驗。

- 為了回應使用者意見反應，使用者現在可以讓特定 Cookie 在瀏覽器關閉時不被自動清除。 如果有使用者不想被登出但仍想要在瀏覽器關閉時清除所有其他 Cookie 的網站，此選項就相當實用。 若要使用此功能，請移至 *edge://settings/clearBrowsingDataOnClose*，並啟用 [Cookie 與其他網站資料] 切換。

- 現在提供「自動設定檔切換」功能，以協助您更輕鬆地在不同設定檔間取得工作內容。 如果您在工作中使用多個設定檔，可以在使用您的個人設定檔時瀏覽至需要輸入公司或學校帳戶驗證的網站，藉此查看設定檔。 當我們偵測到變更時，將提示您切換為公司設定檔來存取該網站，而不需向它進行驗證。 選擇您要切換的公司設定檔時，該網站就會在您的公司設定檔中開啟。 此設定檔切換功能可協助您將公司與個人資料分開，並協助您更輕鬆地取得工作內容。 如果您不希望該功能提示您切換設定檔，則可以選擇 [不要再問我] 選項，之後就不再提醒您。

- 集錦功能改善：
  - 您可以使用拖放功能，在不開啟集錦的情況下，將項目新增至集錦。 在拖放期間，您也可以選擇集錦清單中您要放置項目的位置。
  - 您可以將多個集錦新增至集錦，而不是一次新增一個項目。 若要新增多個項目，請選取項目，然後將它們拖曳到集錦。 或者，您也可以選取項目並以滑鼠右鍵按一下，然後挑選您需要放置項目的集錦。

- 您可以將 Microsoft Edge 視窗中的所有索引標籤新增至新的集錦，而不需要個別新增。 若要新增所有索引標籤，請以滑鼠右鍵按一下任一索引標籤，然後選擇 [將所有索引標籤新增至集錦]。

- 擴充功能同步現在可供使用。 您現在可以在您所有的裝置上同步擴充功能！ 來自 Microsoft 與 Chrome 商店的擴充功能都會與 Microsoft Edge 同步。 若要使用此功能：按一下功能表列上的省略符號 (**...**)，然後選取 [設定]****。 在您的個人檔案下，按一下 [同步]**** 以查看同步選項。 在 [個人檔案/同步]**** 下，使用切換來啟用擴充功能。 您可以使用 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 群組原則來停用擴充功能的同步。

- 改善下載管理頁面上針對已封鎖不安全下載的訊息。

- 沉浸式閱讀程式的改善：
  - 我們在沉浸式閱讀程式的詞性體驗中新增了「副詞」的支援。 當您在沉浸式閱讀程式中閱讀文章時，開啟文法檢查工具，並開啟詞性中的「副詞」，即可強調頁面上的所有副詞。
  - 新增可選取網頁上任何內容，並在沉浸式閱讀器程式中開啟的功能。 這可讓使用者在所有網站上使用沉浸式閱讀程式和所有學習工具，例如「行聚焦」和「大聲朗讀」。

- Link Doctor 會在使用者誤植 URL 時，為使用者提供主機校正和搜尋查詢。 例如： <br>
使用者將「powerbi」誤植為 powerbbi.com。 Link Doctor 會建議 powerbi.com 做為修正，並建立連結以搜尋「powerbbi」，以免使用者要尋找不同內容。

- 允許使用者儲存其決定以啟動特定網站的外部通訊協定。 使用者可以設定 [ExternalProtocolDialogShowAlwaysOpenCheckbox]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox) 原則，以啟用或停用此功能。

- 使用者可以直接從 Microsoft Edge **[設定]** 將 Microsoft Edge 設為其預設瀏覽器。 這項功能可讓使用者更輕鬆地在瀏覽器本身的內容內變更其預設瀏覽器，而不需要在作業系統設定中搜尋。 若要使用此功能，請移至 *edge://settings/defaultBrowser*，然後按一下 **[設為預設]**。

- 多個 DevTools 更新，包括新的遠端偵錯支援、UI 改善等。 如需詳細資訊，請參閱 [DevTools 的新功能 (Microsoft Edge 83)](/microsoft-edge/devtools-guide-chromium/whats-new/2020/03/devtools)。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 15 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列原則。

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

#### <a name="deprecated-policy"></a>取代的原則

下列原則會持續在此版本中運作。 在未來版本中，它會變得「過時」。

[EnableDomainActionsDownload](./microsoft-edge-policies.md#enabledomainactionsdownload) - 啟用來自 Microsoft 的網域動作下載

<!--  end 83 -->

## <a name="version-81041660-april-20"></a>版本 81.0.416.60：4 月 20 日

修正各種錯誤和效能問題。

## <a name="version-81041658-april-17"></a>版本 81.0.416.58：4 月 17 日

安全性更新。

## <a name="version-81041650-april-10"></a>版本 81.0.416.50：4 月 10 日

修正各種錯誤和效能問題。

## <a name="version-81041645-april-3"></a>版本 81.0.416.45：4 月 3 日

修正各種錯誤和效能問題。

## <a name="version-81041641-march-30"></a>版本 81.0.416.41：3 月 30 日

修正各種錯誤和效能問題。

## <a name="version-81041634-march-17"></a>版本 81.0.416.34：3 月 17 日

修正各種錯誤和效能問題。

## <a name="version-81041631-march-12"></a>版本 81.0.416.31：3 月 12 日

修正各種錯誤和效能問題。

## <a name="version-81041628-march-9"></a>版本 81.0.416.28：3 月 9 日

修正各種錯誤和效能問題。

## <a name="version-81041620-february-28"></a>版本 81.0.416.20：2 月 28 日

修正各種錯誤和效能問題。

## <a name="version-81041612-february-20"></a>版本 81.0.416.12：2 月 20 日

### <a name="feature-updates"></a>功能更新

- 集合現在可供使用。 您可以按一下位址列旁邊的 [集合] 圖示來開始。 此動作會開啟 [集合] 窗格，您可以在其中建立、編輯和檢視集合。 我們根據您會在網路上執行的動作設計這些集合。 如果您是購物者、旅行者、教師或學生，則集合可協助您。 [進一步瞭解](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/#LuDPRDUDCgdgdOVt.97)。

- 允許從 Microsoft Edge 工具列移除 (從工具列隱藏) [集合] 按鈕，以獲得一致性。

- 內部部署 Active Directory 帳戶的自動登入只會針對開啟該功能的組織。 如果使用者已使用內部部署 AD 帳戶登入，他們現在可以登出該帳戶。 現在，只有在使用者的主要帳戶是 Microsoft 帳戶或 Azure Active Directory 帳戶的情況下，使用者才會在其作業系統上使用主要帳戶自動登入。 系統管理員可以使用 ConfigureOnPremisesAccountAutoSignIn 原則，將使用內部部署 AD 帳戶自動登入啟用。

- 應用程式防護。 容器中目前提供延伸模組的支援。

- 新增訊息以在使用者瀏覽至設定為以 Internet Explorer 模式開啟的頁面時，通知使用者 Internet Explorer 未安裝。

- 更新 Microsoft Edge DevTools 中的 3D 檢視工具，加上新功能，以協助您偵錯 z 索引堆疊內容。 3D 檢視會使用色彩和堆疊顯示 DOM (文件物件模型) 深度的外觀，而 z 索引檢視可協助您區隔頁面的不同堆疊內容。 [進一步瞭解](https://blogs.windows.com/msedgedev/2020/01/23/debug-z-index-3d-view-edge-devtools/)。

- 將 F12 開發工具以 10 個新語言當地語系化，讓它們符合其餘瀏覽器所使用的語言。 [進一步瞭解](https://blogs.windows.com/msedgedev/2020/02/04/localizing-edge-devtools/)。

- 新增對 Dolby Vision 播放的支援。 在啟用 Dolby Vision 的 Windows 10 組建 17134 (2018 年 4 月更新) 中，網站可以顯示 Dolby Vision 內容。 看看如何從 [Netflix](https://help.netflix.com/en/node/42384) 啟用 Dolby Vision 內容。

- Microsoft Edge 現在可以識別及移除重複的我的最愛，並將相同名稱的資料夾合併。 若要存取工具，請按一下瀏覽器工具列上的星形，然後選取 [移除重複的我的最愛]。  您將可以確認變更，而對您的最愛的任何更新將會在各個裝置上同步處理。

- 我們聽使用者說，很難區分使用深色佈景主題的一般瀏覽視窗與 InPrivate 視窗，因為這兩個視窗框架都是深色的。 右上角的新實體 InPrivate 藍色藥丸可協助確保使用者正在瀏覽 InPrivate。

- 在正確的瀏覽器設定檔中開啟外部連結。 從 *edge://settings/multiProfileSettings*，針對開啟的連結選取預設的設定檔，讓其在外部應用程式中開啟。

- 新增了警告，以在先前使用另一個帳戶登入之後，提醒使用該帳戶登入瀏覽器設定檔的使用者。 這有助於防止意外的資料合併。

- 如果您已在 Microsoft 帳戶中儲存付款卡，您可以在 Microsoft Edge 填寫付款表單時使用該資訊。 您的 Microsoft 帳戶中的卡片將會在整個桌面裝置間同步處理，且完整詳細資料會在使用雙重要素驗證 (CVC 代碼和您的 Microsoft 身分識別) 之後與網站共用。為了方便存取，您可以在驗證期間選擇在裝置上安全地儲存信用卡的複本。

- 「行聚焦」是專為希望在閱讀內容以聚焦於有限部分內容的使用者所設計。 它讓使用者能一次聚焦於第 1、3 或 5 行，並將頁面的其餘部分反灰，讓使用者閱讀而不受干擾。 使用者可以使用觸控或方向鍵來進行捲動，而焦點會相應地位移。

- Microsoft Edge 現在已與 Windows 平台 8.1 及更新版本上的 Windows 拼字檢查整合。 此整合可提供更強大的語言支援，可存取更多語言字典，並能使用 Windows 自訂字典。 如果已在作業系統語言設定中新增某個語言，且已在 Microsoft Edge 設定中啟用語言拼字檢查切換，則使用者不需要執行其他動作。

- 當您使用 Microsoft Edge 開啟 PDF 文件時，使用者現在可以建立醒目提示、變更色彩，以及刪除醒目提示。 這有助於日後參照文件的重要部分，以及共同作業。

- 載入已針對網路最佳化的冗長 PDF 文件時，在載入其餘文件時，使用者正在瀏覽的頁面會以較快的速度 (並行) 載入。

- 現在只要按 F9 鍵，就能更輕鬆地啟動網站的沉浸式閱讀程式。

- 現在，您可以使用鍵盤快速鍵 (Ctrl + Shift + U)更輕鬆地開始「大聲朗讀」。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 12 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://aka.ms/EdgeEnterprise)下載更新的系統管理範本。 已新增下列新原則。

- [AmbientAuthenticationInPrivateModesEnabled](./microsoft-edge-policies.md#ambientauthenticationinprivatemodesenabled) - 啟用 InPrivate 和來賓設定檔的環境驗證。 
- [AudioSandboxEnabled](./microsoft-edge-policies.md#audiosandboxenabled) - 允許音訊沙箱執行。
- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - 使用預設的查閱者原則 no-referrer-when-downgrade。
- [GloballyScopeHTTPAuthCacheEnabled](./microsoft-edge-policies.md#globallyscopehttpauthcacheenabled) - 啟用全域範圍的 HTTP 驗證快取。
- [ImportExtensions](./microsoft-edge-policies.md#importextensions) - 允許匯入延伸模組。
- [ImportCookies](./microsoft-edge-policies.md#importcookies) - 允許匯入 Cookie。
- [ImportShortcuts](./microsoft-edge-policies.md#importshortcuts) - 允許匯入快速鍵。
- [InternetExplorerIntegrationSiteRedirect](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect) - 指定從 Internet Explorer 模式頁面啟動時，「頁面內」瀏覽至未設定網站的行為。
- [OmniboxMSBProviderEnabled](./microsoft-edge-policies.md#omniboxmsbproviderenabled) - 在 omnibox 中啟用 Microsoft Search for Business。 
- [StricterMixedContentTreatmentEnabled](./microsoft-edge-policies.md#strictermixedcontenttreatmentenabled) - 針對混合式內容啟用更嚴格的處理方式。
- [TLS13HardeningForLocalAnchorsEnabled](./microsoft-edge-policies.md#tls13hardeningforlocalanchorsenabled) - 針對本機信任起點啟用 TLS 1.3 安全性功能。
- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) - 設定在沒有 Azure AD 網域帳戶時，自動使用 Active Directory 網域帳戶登入。

#### <a name="deprecated-policies"></a>過時的原則

下列原則會持續在此版本中運作。 在未來版本中，它們會變得「過時」。

- [WebComponentsV0Enabled](./microsoft-edge-policies.md#webcomponentsv0enabled) - 重新啟用網頁元件 v0 API 至 M84。
- [WebDriverOverridesIncompatiblePolicies](./microsoft-edge-policies.md#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)