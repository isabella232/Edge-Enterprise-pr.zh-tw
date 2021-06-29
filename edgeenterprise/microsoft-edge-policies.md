---
title: Microsoft Edge 瀏覽器原則文件
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/17/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge 瀏覽器支援的所有原則的 Windows 和 Mac 文件
ms.openlocfilehash: 21933e81427b84d69f6d3ead4dfc911519e65bb3
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617873"
---
# <a name="microsoft-edge---policies"></a>Microsoft Edge - 原則

最新版本的 Microsoft Edge 包含下列原則。 您可以使用這些原則來設定 Microsoft Edge 在組織中的執行方式。

如需用於控制 Microsoft Edge 更新方式和更新時機的一組額外原則的詳細資訊，請參閱 [Microsoft Edge 更新原則參考](microsoft-edge-update-policies.md)。

您可以下載 [Microsoft 安全性合規性工具組](https://www.microsoft.com/download/details.aspx?id=55319)，以取得 Microsoft Edge 的建議安全性設定基準設定。 如需詳細資訊，請參閱 [Microsoft 安全性基準部落格](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="new-policies"></a>新原則

下表列出此更新的新原則。

|名稱|標題|
|--|--|
|[AADWebSiteSSOUsingThisProfileEnabled](#aadwebsitessousingthisprofileenabled)|已啟用使用此設定檔的工作或學校網站單一登入|
|[AutomaticHttpsDefault](#automatichttpsdefault)|設定自動 HTTPS|
|[CECPQ2Enabled](#cecpq2enabled)|已啟用 TLS 的 CECPQ2 後量子金鑰協定|
|[InsecurePrivateNetworkRequestsAllowed](#insecureprivatenetworkrequestsallowed)|指定是否允許不安全的網站對較私人的網路端點提出要求|
|[InsecurePrivateNetworkRequestsAllowedForUrls](#insecureprivatenetworkrequestsallowedforurls)|允許列出的網站從不安全的內容對較私人的網路端點提出要求|
|[InternetExplorerIntegrationLocalSiteListExpirationDays](#internetexplorerintegrationlocalsitelistexpirationdays)|指定網站保留在區域 IE 模式網站清單上的天數|
|[InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed)|允許在 Internet Explorer 模式中重新載入未設置的網站|
|[LocalBrowserDataShareEnabled](#localbrowserdatashareenabled)|啟用 Windows 以搜尋當地 Microsoft Edge 瀏覽資料|
|[TripleDESEnabled](#tripledesenabled)|在 TLS 中啟用 3DES 加密套件|

## <a name="deprecated-policies"></a>取代的原則

下表列出此更新的已取代原則。

|名稱|標題|
|--|--|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|允許 Internet Explorer 模式測試 (已取代) |
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|啟用預設舊版 SameSite Cookie 行為設定 (已取代)|

## <a name="obsolete-policies"></a>過時的原則

下表列出此更新的過時原則。

|名稱|標題|
|--|--|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|設定 Microsoft Edge 新的索引標籤頁面體驗 (已過時)|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|允許 WebDriver 覆寫不相容原則 (已過時) |

## <a name="available-policies"></a>可用的原則

下表列出此版本 Microsoft Edge 提供的所有瀏覽器相關群組原則。 使用下表中的連結，深入了解特定原則。

- [應用程式防護設定](#application-guard-settings)
- [投射](#cast)
- [內容設定](#content-settings)
- [預設搜尋提供者](#default-search-provider)
- [Extensions](#extensions)
- [HTTP 驗證](#http-authentication)
- [kiosk 模式設定](#kiosk-mode-settings)
- [管理性](#manageability)
- [原生訊息](#native-messaging)
- [密碼管理員和防護](#password-manager-and-protection)
- [效能](#performance)
- [列印](#printing)
- [私人網路要求設定](#private-network-request-settings)
- [Proxy 伺服器](#proxy-server)
- [睡眠索引標籤設定](#sleeping-tabs-settings)
- [SmartScreen 設定](#smartscreen-settings)
- [啟動、首頁和新的索引標籤頁面](#startup-home-page-and-new-tab-page)
- [其他](#additional)


### [*<a name="application-guard-settings"></a>應用程式防護設定*](#application-guard-settings-policies)

|原則名稱|標題|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|應用程式防護容器 Proxy|
|[ApplicationGuardFavoritesSyncEnabled](#applicationguardfavoritessyncenabled)|已啟用應用程式防護我的最愛同步處理|
|[ApplicationGuardTrafficIdentificationEnabled](#applicationguardtrafficidentificationenabled)|應用程式防護流量識別|
### [*<a name="cast"></a>投射*](#cast-policies)

|原則名稱|標題|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|啟用 Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|在工具列中顯示投射圖示|
### [*<a name="content-settings"></a>內容設定*](#content-settings-policies)

|原則名稱|標題|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|自動選取這些網站的用戶端憑證|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|允許特定網站上的 Cookie|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|封鎖特定網站上的 Cookie|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|限制來自特定網站的 Cookie 匯入目前的工作階段|
|[DefaultCookiesSetting](#defaultcookiessetting)|設定 Cookie|
|[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting)|控制檔案系统 API 的讀取使用|
|[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting)|控制檔案系統 API 的寫入使用|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|預設地理位置設定值|
|[DefaultImagesSetting](#defaultimagessetting)|預設影像設定|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|控制不安全內容例外狀況的使用|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|預設 JavaScript 設定|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|預設通知設定|
|[DefaultPluginsSetting](#defaultpluginssetting)|預設 Adobe Flash 設定 (過時)|
|[DefaultPopupsSetting](#defaultpopupssetting)|預設快顯視窗設定|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|控制 Web 藍牙 API 的使用|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|控制 WebUSB API 的使用|
|[FileSystemReadAskForUrls](#filesystemreadaskforurls)|允許透過這些網站上的檔案系統 API 讀取存取權|
|[FileSystemReadBlockedForUrls](#filesystemreadblockedforurls)|封鎖透過這些網站上的檔案系統 API 讀取存取權|
|[FileSystemWriteAskForUrls](#filesystemwriteaskforurls)|允許這些網站上的檔案和目錄的寫入存取權|
|[FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls)|封鎖這些網站上的檔案和目錄的寫入存取權|
|[ImagesAllowedForUrls](#imagesallowedforurls)|允許這些網站上的影像|
|[ImagesBlockedForUrls](#imagesblockedforurls)|封鎖特定網站上的影像|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|允許指定網站上的不安全內容|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|封鎖指定網站上的不安全內容|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|允許特定網站上的 JavaScript|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|封鎖特定網站上的 JavaScript|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|啟用預設舊版 SameSite Cookie 行為設定 (已取代)|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|將指定網站上的 Cookie 還原至舊版 SameSite 行為|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|允許特定網站上的通知|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|封鎖特定網站上的通知|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|允許特定網站上的 Adobe Flash 外掛程式 (過時)|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|封鎖特定網站上的 Adobe Flash 外掛程式 (過時)|
|[PopupsAllowedForUrls](#popupsallowedforurls)|允許特定網站上的快顯視窗|
|[PopupsBlockedForUrls](#popupsblockedforurls)|封鎖特定網站上的快顯視窗|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|登錄通訊協定處理常式|
|[SpotlightExperiencesAndRecommendationsEnabled](#spotlightexperiencesandrecommendationsenabled)|選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知，及 [Microsoft 服務] 的提示|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|授與特定網站連線到特定 USB 裝置的存取權|
|[WebUsbAskForUrls](#webusbaskforurls)|允許特定網站上的 WebUSB|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|封鎖特定網站上的 WebUSB|
### [*<a name="default-search-provider"></a>預設搜尋提供者*](#default-search-provider-policies)

|原則名稱|標題|
|-|-|
|[DefaultSearchProviderEnabled](#defaultsearchproviderenabled)|啟用預設搜尋提供者|
|[DefaultSearchProviderEncodings](#defaultsearchproviderencodings)|預設搜尋提供者編碼|
|[DefaultSearchProviderImageURL](#defaultsearchproviderimageurl)|指定預設搜尋提供者的影像搜尋功能|
|[DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams)|使用 POST 的影像 URL 參數|
|[DefaultSearchProviderKeyword](#defaultsearchproviderkeyword)|預設搜尋提供者關鍵字|
|[DefaultSearchProviderName](#defaultsearchprovidername)|預設搜尋提供者名稱|
|[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)|預設搜尋提供者搜尋 URL|
|[DefaultSearchProviderSuggestURL](#defaultsearchprovidersuggesturl)|預設建議的搜尋提供者 URL|
|[NewTabPageSearchBox](#newtabpagesearchbox)|設定新的索引標籤頁面搜尋體驗|
### [*<a name="extensions"></a>Extensions*](#extensions-policies)

|原則名稱|標題|
|-|-|
|[BlockExternalExtensions](#blockexternalextensions)|封鎖安裝外部擴充功能|
|[ExtensionAllowedTypes](#extensionallowedtypes)|設定允許的擴充功能類型|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|允許安裝特定擴充功能|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|控制不能安裝哪些擴充功能|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|控制哪些擴充功能會以無訊息方式安裝|
|[ExtensionInstallSources](#extensioninstallsources)|設定擴充功能與使用者指令碼安裝來源|
|[ExtensionSettings](#extensionsettings)|設定擴充功能管理設定|
### [*<a name="http-authentication"></a>HTTP 驗證*](#http-authentication-policies)

|原則名稱|標題|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|允許跨來源 HTTP 驗證提示|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|指定 Microsoft Edge 可以委派使用者認證的伺服器清單|
|[AuthSchemes](#authschemes)|支援的驗證配置|
|[AuthServerAllowlist](#authserverallowlist)|設定允許驗證伺服器的清單|
|[BasicAuthOverHttpEnabled](#basicauthoverhttpenabled)|允許 HTTP 的基本驗證|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|當協調 Kerberos 驗證時停用 CNAME 查閱|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Kerberos SPN 中包含非標準連接埠|
|[NtlmV2Enabled](#ntlmv2enabled)|控制是否要啟用 NTLMv2 驗證|
|[WindowsHelloForHTTPAuthEnabled](#windowshelloforhttpauthenabled)|適用於 HTTP 驗證的 Windows Hello 已啟用|
### [*<a name="kiosk-mode-settings"></a>kiosk 模式設定*](#kiosk-mode-settings-policies)

|原則名稱|標題|
|-|-|
|[KioskAddressBarEditingEnabled](#kioskaddressbareditingenabled)|針對 kiosk 模式公開瀏覽體驗設定網址列編輯|
|[KioskDeleteDownloadsOnExit](#kioskdeletedownloadsonexit)|當 Microsoft Edge 關閉時，刪除隨著 Kiosk 工作階段下載的檔案|
### [*<a name="manageability"></a>管理性*](#manageability-policies)

|原則名稱|標題|
|-|-|
|[MAMEnabled](#mamenabled)|已啟用行動裝置應用程式管理|
### [*<a name="native-messaging"></a>原生訊息*](#native-messaging-policies)

|原則名稱|標題|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|控制使用者可以使用的原生訊息主機|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|設定原生訊息封鎖清單|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)|
### [*<a name="password-manager-and-protection"></a>密碼管理員和防護*](#password-manager-and-protection-policies)

|原則名稱|標題|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|啟用將密碼儲存到密碼管理員|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|允許使用者在密碼不安全時收到警示提醒|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|設定變更密碼 URL|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|設定密碼保護警告觸發程序|
|[PasswordRevealEnabled](#passwordrevealenabled)|啟用顯示密碼按鈕|
### [*<a name="performance"></a>效能*](#performance-policies)

|原則名稱|標題|
|-|-|
|[StartupBoostEnabled](#startupboostenabled)|啟用啟動提升|
### [*<a name="printing"></a>列印*](#printing-policies)

|原則名稱|標題|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|預設印表機選擇規則|
|[PrintHeaderFooter](#printheaderfooter)|列印頁首與頁尾|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|將系統預設的印表機設定為預設印表機|
|[PrintRasterizationMode](#printrasterizationmode)|列印點陣化模式|
|[PrinterTypeDenyList](#printertypedenylist)|停用拒絕清單上的印表機類型|
|[PrintingAllowedBackgroundGraphicsModes](#printingallowedbackgroundgraphicsmodes)|限制背景圖形列印模式|
|[PrintingBackgroundGraphicsDefault](#printingbackgroundgraphicsdefault)|預設背景圖形列印模式|
|[PrintingEnabled](#printingenabled)|啟用列印|
|[PrintingPaperSizeDefault](#printingpapersizedefault)|預設列印頁面大小|
|[UseSystemPrintDialog](#usesystemprintdialog)|使用系統列印對話方塊列印|
### [*<a name="private-network-request-settings"></a>私人網路要求設定*](#private-network-request-settings-policies)

|原則名稱|標題|
|-|-|
|[InsecurePrivateNetworkRequestsAllowed](#insecureprivatenetworkrequestsallowed)|指定是否允許不安全的網站對較私人的網路端點提出要求|
|[InsecurePrivateNetworkRequestsAllowedForUrls](#insecureprivatenetworkrequestsallowedforurls)|允許列出的網站從不安全的內容對較私人的網路端點提出要求|
### [*<a name="proxy-server"></a>Proxy 伺服器*](#proxy-server-policies)

|原則名稱|標題|
|-|-|
|[ProxyBypassList](#proxybypasslist)|設定 Proxy 略過原則 (已取代)|
|[ProxyMode](#proxymode)|設定 Proxy 伺服器設定 (已取代)|
|[ProxyPacUrl](#proxypacurl)|設定 Proxy .pac 檔案 URL (已取代)|
|[ProxyServer](#proxyserver)|設定 Proxy 伺服器的位址或 URL (已取代)|
|[ProxySettings](#proxysettings)|Proxy 設定|
### [*<a name="sleeping-tabs-settings"></a>睡眠索引標籤設定*](#sleeping-tabs-settings-policies)

|原則名稱|標題|
|-|-|
|[SleepingTabsBlockedForUrls](#sleepingtabsblockedforurls)|對特定網站封鎖睡眠索引標籤|
|[SleepingTabsEnabled](#sleepingtabsenabled)|設定睡眠索引標籤|
|[SleepingTabsTimeout](#sleepingtabstimeout)|設定睡眠索引標籤的背景索引標籤無活動逾時|
### [*<a name="smartscreen-settings"></a>SmartScreen 設定*](#smartscreen-settings-policies)

|原則名稱|標題|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|防止略過網站的 Microsoft Defender SmartScreen 提示|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|防止略過關於下載項目的 Microsoft Defender SmartScreen 警告|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單|
|[SmartScreenEnabled](#smartscreenenabled)|設定 Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式|
### [*<a name="startupcomma-home-page-and-new-tab-page"></a>啟動、首頁和新的索引標籤頁面*](#startup-home-page-and-new-tab-page-policies)

|原則名稱|標題|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|將新的索引標籤頁面設定為 [首頁]|
|[HomepageLocation](#homepagelocation)|設定首頁 URL|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|設定新索引標籤頁面版面配置所允許的背景類型|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|設定新的索引標籤頁面公司標誌 (已過時)|
|[NewTabPageContentEnabled](#newtabpagecontentenabled)|允許新分頁頁面上的 Microsoft 新聞內容|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|從新的索引標籤頁面隱藏預設熱門網站|
|[NewTabPageLocation](#newtabpagelocation)|設定新的索引標籤頁面 URL|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|設定新的索引標籤頁面快速連結|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|啟用預先載入的新索引標籤頁面，以加快頁面呈現速度|
|[NewTabPageQuickLinksEnabled](#newtabpagequicklinksenabled)|允許新分頁頁面上的快速連結|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|設定 Microsoft Edge 新的索引標籤頁面體驗 (已過時)|
|[RestoreOnStartup](#restoreonstartup)|啟動時所採取的動作|
|[RestoreOnStartupURLs](#restoreonstartupurls)|瀏覽器啟動時開啟的網站|
|[ShowHomeButton](#showhomebutton)|在工具列上顯示 [首頁] 按鈕|
### [*<a name="additional"></a>其他*](#additional-policies)

|原則名稱|標題|
|-|-|
|[AADWebSiteSSOUsingThisProfileEnabled](#aadwebsitessousingthisprofileenabled)|已啟用使用此設定檔的工作或學校網站單一登入|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|在網址列中啟用 Bing 專用 Microsoft Search 建議|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|含有干擾廣告網站的廣告設定|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|啟用刪除瀏覽器和下載歷程記錄|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|允許檔案選取項目對話方塊|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|允許在卸載網頁期間顯示快顯視窗 (已淘汰)|
|[AllowSurfGame](#allowsurfgame)|允許衝浪遊戲|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|允許頁面在頁面關閉期間傳送同步 XHR 要求 (已取代)|
|[AllowTokenBindingForUrls](#allowtokenbindingforurls)|設定 Microsoft Edge 將嘗試建立與 [權杖繫結] 連結的網站清單。|
|[AllowTrackingForUrls](#allowtrackingforurls)|設定特定網站的防止追蹤例外|
|[AlternateErrorPagesEnabled](#alternateerrorpagesenabled)|當找不到網頁時，推薦類似的頁面|
|[AlwaysOpenPdfExternally](#alwaysopenpdfexternally)|一律在外部開啟 PDF 檔案|
|[AmbientAuthenticationInPrivateModesEnabled](#ambientauthenticationinprivatemodesenabled)|針對 InPrivate 和來賓設定檔啟用環境驗證|
|[AppCacheForceEnabled](#appcacheforceenabled)|允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態) |
|[ApplicationLocaleValue](#applicationlocalevalue)|設定應用程式地區設定|
|[AudioCaptureAllowed](#audiocaptureallowed)|允許或封鎖音訊擷取|
|[AudioCaptureAllowedUrls](#audiocaptureallowedurls)|無需要求權限即可存取音訊擷取裝置的網站|
|[AudioSandboxEnabled](#audiosandboxenabled)|允許音訊沙盒執行|
|[AutoImportAtFirstRun](#autoimportatfirstrun)|在首次執行時，自動匯入其他瀏覽器的資料和設定|
|[AutoLaunchProtocolsFromOrigins](#autolaunchprotocolsfromorigins)|定義一份協定清單，可在不須提示使用者的情下，從列出的來源啟動外部應用程式|
|[AutoOpenAllowedForURLs](#autoopenallowedforurls)|URLs where AutoOpenFileTypes 可以套用 |
|[AutoOpenFileTypes](#autoopenfiletypes)|檔案類型清單應在下載時自動開啟|
|[AutofillAddressEnabled](#autofilladdressenabled)|啟用地址自動填寫|
|[AutofillCreditCardEnabled](#autofillcreditcardenabled)|啟用信用卡自動填寫|
|[AutomaticHttpsDefault](#automatichttpsdefault)|設定自動 HTTPS|
|[AutoplayAllowed](#autoplayallowed)|允許網站自動播放媒體|
|[BackgroundModeEnabled](#backgroundmodeenabled)|在 Microsoft Edge 關閉後繼續執行背景應用程式|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新|
|[BingAdsSuppression](#bingadssuppression)|封鎖 Bing 搜尋結果中的所有廣告|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|封鎖第三方 Cookie|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|啟用來賓模式|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|允許查詢瀏覽器網路時間服務|
|[BrowserSignin](#browsersignin)|瀏覽器登入設定|
|[BrowsingDataLifetime](#browsingdatalifetime)|流覽資料存留期設定|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|使用內建的 DNS 用戶端|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|決定是否使用內建的憑證驗證程式來驗證伺服器憑證 (已取代)|
|[CECPQ2Enabled](#cecpq2enabled)|已啟用 TLS 的 CECPQ2 後量子金鑰協定|
|[CertificateTransparencyEnforcementDisabledForCas](#certificatetransparencyenforcementdisabledforcas)|針對 subjectPublicKeyInfo 雜湊的清單，停用憑證透明度強化|
|[CertificateTransparencyEnforcementDisabledForLegacyCas](#certificatetransparencyenforcementdisabledforlegacycas)|停用舊版憑證授權單位清單的憑證透明度強化|
|[CertificateTransparencyEnforcementDisabledForUrls](#certificatetransparencyenforcementdisabledforurls)|停用針對特定 URL 的憑證透明度強化|
|[ClearBrowsingDataOnExit](#clearbrowsingdataonexit)|在 Microsoft Edge 關閉時清除瀏覽資料|
|[ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)|在 Microsoft Edge 關閉時清除快取的影像和檔案|
|[ClickOnceEnabled](#clickonceenabled)|允許使用者使用 ClickOnce 通訊協定開啟檔案|
|[CollectionsServicesAndExportsBlockList](#collectionsservicesandexportsblocklist)|封鎖集錦中服務和匯出目標特定清單的存取權|
|[CommandLineFlagSecurityWarningsEnabled](#commandlineflagsecuritywarningsenabled)|啟用命令列旗標的安全性警告|
|[ComponentUpdatesEnabled](#componentupdatesenabled)|啟用 Microsoft Edge 中的元件更新|
|[ConfigureDoNotTrack](#configuredonottrack)|設定不要追蹤|
|[ConfigureFriendlyURLFormat](#configurefriendlyurlformat)|設定從 Microsoft Edge 複製的 URL 預設貼上格式，並決定使用者是否可以使用其他格式|
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|設定線上文字轉語音|
|[ConfigureShare](#configureshare)|設定共用體驗|
|[CustomHelpLink](#customhelplink)|指定自訂說明連結|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS 攔截檢查已啟用|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|將 Microsoft Edge 設定為預設瀏覽器|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|允許預設搜尋提供者操作功能表搜尋存取權|
|[DefaultSensorsSetting](#defaultsensorssetting)|預設的感應器設定|
|[DefaultSerialGuardSetting](#defaultserialguardsetting)|控制 Serial API 的使用|
|[DefinePreferredLanguages](#definepreferredlanguages)|定義網站支援語言時，網站應該顯示的慣用語言的排序清單|
|[DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload)|要求在索引標籤導覽前， [企業模式網站清單] 即已可使用|
|[DeleteDataOnMigration](#deletedataonmigration)|移轉時刪除舊版瀏覽器資料|
|[DeveloperToolsAvailability](#developertoolsavailability)|控制可使用開發人員工具的位置|
|[DiagnosticData](#diagnosticdata)|傳送關於瀏覽器使用狀況的必要和選擇性診斷資料|
|[DirectInvokeEnabled](#directinvokeenabled)|允許使用者使用 DirectInvoke 通訊協定開啟檔案|
|[Disable3DAPIs](#disable3dapis)|停用 3D 圖形 API 支援|
|[DisableScreenshots](#disablescreenshots)|停用取得螢幕擷取畫面功能|
|[DiskCacheDir](#diskcachedir)|設定磁碟快取目錄|
|[DiskCacheSize](#diskcachesize)|設定磁碟快取大小，以位元組為單位|
|[DnsOverHttpsMode](#dnsoverhttpsmode)|控制 DNS-over-HTTPS 模式|
|[DnsOverHttpsTemplates](#dnsoverhttpstemplates)|指定所需的 DNS-over-HTTPS 解析程式的 URI 範本|
|[DownloadDirectory](#downloaddirectory)|設定下載目錄|
|[DownloadRestrictions](#downloadrestrictions)|允許下載限制|
|[EdgeCollectionsEnabled](#edgecollectionsenabled)|啟用集錦功能|
|[EdgeShoppingAssistantEnabled](#edgeshoppingassistantenabled)|已啟用在 Microsoft Edge 中購物|
|[EditFavoritesEnabled](#editfavoritesenabled)|允許使用者編輯我的最愛|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|在限定時間內重新啟用已過時的網頁平台功能 (過時)|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|啟用從 Microsoft 進行網域動作下載 (已過時) |
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|啟用線上 OCSP/CRL 檢查|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|允許受管擴充功能使用企業硬體平台 API|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|允許存取 Enterprise Mode Site List Manager 工具|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|控制與實驗和設定服務的通訊|
|[ExplicitlyAllowedNetworkPorts](#explicitlyallowednetworkports)|明確允許的網路連接埠|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|在外部通訊協定對話方塊中顯示「一律開啟」核取方塊|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|允許使用者設定家庭安全與兒童模式|
|[FavoritesBarEnabled](#favoritesbarenabled)|啟用我的最愛列|
|[FetchKeepaliveDurationSecondsOnShutdown](#fetchkeepalivedurationsecondsonshutdown)|擷取關機時的存留持續時間|
|[ForceBingSafeSearch](#forcebingsafesearch)|強制執行 Bing 安全搜尋|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|設定使用 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，Microsoft Edge 是否應自動選取憑證|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|啟用使用暫時設定檔|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|強制執行 Google 安全搜尋|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|使用預設的查閱者原則 no-referrer-when-downgrade (已淘汰)|
|[ForceNetworkInProcess](#forcenetworkinprocess)|強制網路程式碼在瀏覽器處理程序中執行 (已過時) |
|[ForceSync](#forcesync)|強制同步處理瀏覽器資料，且不顯示同步同意提示|
|[ForceYouTubeRestrict](#forceyoutuberestrict)|強制最小 YouTube 限制模式|
|[FullscreenAllowed](#fullscreenallowed)|允許全螢幕模式|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|啟用全域範圍的 HTTP 驗證快取|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|設定會略過 HSTS 原則檢查的名稱清單|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|可用時便使用硬體加速|
|[HeadlessModeEnabled](#headlessmodeenabled)|控制無周邊模式的使用|
|[HideFirstRunExperience](#hidefirstrunexperience)|隱藏初次執行體驗與啟動顯示畫面|
|[HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](#hideinternetexplorerredirectuxforincompatiblesitesenabled)|隱藏一次性的重新導向對話方塊和 Microsoft Edge 上的橫幅|
|[ImportAutofillFormData](#importautofillformdata)|允許匯入自動填寫表單資料|
|[ImportBrowserSettings](#importbrowsersettings)|允許匯入瀏覽器設定|
|[ImportCookies](#importcookies)|允許匯入 Cookie|
|[ImportExtensions](#importextensions)|允許匯入擴充功能|
|[ImportFavorites](#importfavorites)|允許匯入我的最愛|
|[ImportHistory](#importhistory)|允許匯入瀏覽歷程記錄|
|[ImportHomepage](#importhomepage)|允許匯入首頁設定|
|[ImportOpenTabs](#importopentabs)|允許匯入開啟的索引標籤|
|[ImportPaymentInfo](#importpaymentinfo)|允許匯入付款資訊|
|[ImportSavedPasswords](#importsavedpasswords)|允許匯入儲存的密碼|
|[ImportSearchEngine](#importsearchengine)|允許匯入搜尋引擎設定|
|[ImportShortcuts](#importshortcuts)|允許匯入捷徑|
|[ImportStartupPageSettings](#importstartuppagesettings)|允許匯入啟動程序設定|
|[InPrivateModeAvailability](#inprivatemodeavailability)|設定 InPrivate 模式可用性|
|[InsecureFormsWarningsEnabled](#insecureformswarningsenabled)|啟用不安全表單的警告|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|管理 IntensiveWakeUpThrottling 功能|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|針對 Internet Explorer 模式設定增強的當機偵測|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|設定 Internet Explorer 整合|
|[InternetExplorerIntegrationLocalFileAllowed](#internetexplorerintegrationlocalfileallowed)|允許在 Internet Explorer 模式中啟動本機檔案|
|[InternetExplorerIntegrationLocalFileExtensionAllowList](#internetexplorerintegrationlocalfileextensionallowlist)|根據副檔名允許清單在 Internet Explorer 模式中開啟本機檔案|
|[InternetExplorerIntegrationLocalFileShowContextMenu](#internetexplorerintegrationlocalfileshowcontextmenu)|顯示操作功能表以在 Internet Explorer 模式中開啟 file:// 連結|
|[InternetExplorerIntegrationLocalSiteListExpirationDays](#internetexplorerintegrationlocalsitelistexpirationdays)|指定網站保留在區域 IE 模式網站清單上的天數|
|[InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed)|允許在 Internet Explorer 模式中重新載入未設置的網站|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|設定 Enterprise Mode Site List|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式|
|[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed)|允許 Internet Explorer 模式測試 (已取代) |
|[IntranetRedirectBehavior](#intranetredirectbehavior)|內部網路重新導向行為|
|[IsolateOrigins](#isolateorigins)|為特定來源啟用網站隔離|
|[LocalBrowserDataShareEnabled](#localbrowserdatashareenabled)|啟用 Windows 以搜尋當地 Microsoft Edge 瀏覽資料|
|[LocalProvidersEnabled](#localprovidersenabled)|允許來自本機提供者的建議|
|[ManagedConfigurationPerOrigin](#managedconfigurationperorigin)|設定網站到特定來源的受管理設定值|
|[ManagedFavorites](#managedfavorites)|設定我的最愛|
|[ManagedSearchEngines](#managedsearchengines)|管理搜尋引擎|
|[MathSolverEnabled](#mathsolverenabled)|讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|同時連線到 Proxy 伺服器的最大數目|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|允許 Google Cast 連線至所有 IP 位址上的投射裝置|
|[MetricsReportingEnabled](#metricsreportingenabled)|啟用使用方式和當機相關的資料報告 (已淘汰)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|啟用原生視窗遮蔽 (已取代)|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|針對企業模式網站清單，設定索引標籤瀏覽逾時延遲|
|[NetworkPredictionOptions](#networkpredictionoptions)|啟用網路預測|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|控制不安全來源中安全性限制套用的地方|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|允許網站查詢可用的付款方式|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|將瀏覽歷程記錄、我的最愛和收藏、使用狀況及其他瀏覽資料傳送給 Microsoft，以允許個人化廣告、Microsoft Edge、搜尋、新聞和其他 Microsoft 服務|
|[PinningWizardAllowed](#pinningwizardallowed)|允許 [釘選到工作列精靈]|
|[ProactiveAuthEnabled](#proactiveauthenabled)|啟用主動式驗證 (已過時)|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|啟用全分頁促銷內容|
|[PromptForDownloadLocation](#promptfordownloadlocation)|詢問下載檔案的儲存位置|
|[QuicAllowed](#quicallowed)|允許 QUIC 通訊協定|
|[QuickViewOfficeFilesEnabled](#quickviewofficefilesenabled)|在 Microsoft Edge 中管理 QuickView Office 檔案功能|
|[RedirectSitesFromInternetExplorerPreventBHOInstall](#redirectsitesfrominternetexplorerpreventbhoinstall)|防止安裝 BHO，將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge|
|[RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode)|將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge|
|[RelaunchNotification](#relaunchnotification)|通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|設定更新通知的時間週期|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|啟用轉譯器程式碼完整性|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|指定本機信賴起點是否需要線上 OCSP/CRL 檢查|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|啟用使用 Web 服務來解決導覽錯誤|
|[RestrictSigninToPattern](#restrictsignintopattern)|限制哪些帳戶可用為 Microsoft Edge 主要帳戶|
|[RoamingProfileLocation](#roamingprofilelocation)|設定漫遊設定檔目錄|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|啟用 Microsoft Edge 設定檔資料的快取副本|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|將 Adobe Flash 內容設定延伸至所有內容 (過時)|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|允許使用者從 HTTPS 警告頁面繼續進行|
|[SSLErrorOverrideAllowedForOrigins](#sslerroroverrideallowedfororigins)|允許使用者從特定來源的 HTTPS 警告頁面繼續進行|
|[SSLVersionMin](#sslversionmin)|已啟用最小 TLS 版本 (已取代)|
|[SaveCookiesOnExit](#savecookiesonexit)|在 Microsoft Edge 關閉時儲存 Cookie|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|停用儲存瀏覽器歷程記錄|
|[ScreenCaptureAllowed](#screencaptureallowed)|允許或拒絕螢幕擷取畫面|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|啟用捲動至在 URL 片段中指定的文字|
|[SearchSuggestEnabled](#searchsuggestenabled)|啟用搜尋建議|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|不需要權限即可使用直接存取安全性金鑰證明的網站或網域|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|將所有內部網路網站傳送到 Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|傳送網站資訊以改善 Microsoft 服務 (已淘汰)|
|[SensorsAllowedForUrls](#sensorsallowedforurls)|允許存取特定網站上的感應器|
|[SensorsBlockedForUrls](#sensorsblockedforurls)|封鎖存取特定網站上的感應器|
|[SerialAskForUrls](#serialaskforurls)|允許特定網站的 Serial API|
|[SerialBlockedForUrls](#serialblockedforurls)|封鎖特定網站的 Serial API|
|[SharedArrayBufferUnrestrictedAccessAllowed](#sharedarraybufferunrestrictedaccessallowed)|指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用|
|[ShowMicrosoftRewards](#showmicrosoftrewards)|顯示 Microsoft Rewards 體驗|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|在 [我的最愛] 列中顯示 Microsoft Office 捷徑 (已取代)|
|[ShowRecommendationsEnabled](#showrecommendationsenabled)|允許來自 Microsoft Edge 的建議和促銷通知|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|啟用 Signed HTTP Exchange (SXG) 支援|
|[SitePerProcess](#siteperprocess)|為每個網站啟用網站隔離|
|[SmartActionsBlockList](#smartactionsblocklist)|封鎖服務清單的智慧型動作|
|[SpeechRecognitionEnabled](#speechrecognitionenabled)|Configure Speech Recognition|
|[SpellcheckEnabled](#spellcheckenabled)|啟用拼字檢查|
|[SpellcheckLanguage](#spellchecklanguage)|啟用特定拼字檢查語言|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|強制停用拼字檢查語言|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|針對混合內容啟用更嚴格的處理 (已過時)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|隱藏不支援的 OS 警告|
|[SyncDisabled](#syncdisabled)|透過 Microsoft 同步服務停用資料同步|
|[SyncTypesListDisabled](#synctypeslistdisabled)|設定同步服務將排除的類型清單|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|啟用適於本機信賴起點的 TLS 1.3 安全性功能 (已過時)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|指定欲停用的 TLS 加密套件|
|[TabFreezingEnabled](#tabfreezingenabled)|允許凍結背景索引標籤 (已淘汰)|
|[TargetBlankImpliesNoOpener](#targetblankimpliesnoopener)|不对指向 _blank 的链接設定 window.opener|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|啟用在瀏覽器工作管理員中結束處理程序|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|設定單一 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)|
|[TrackingPrevention](#trackingprevention)|封鎖使用者的網頁瀏覽活動追蹤|
|[TranslateEnabled](#translateenabled)|啟用翻譯|
|[TripleDESEnabled](#tripledesenabled)|在 TLS 中啟用 3DES 加密套件|
|[URLAllowlist](#urlallowlist)|定義受允許的 URL 清單|
|[URLBlocklist](#urlblocklist)|封鎖存取 URL 清單|
|[UpdatePolicyOverride](#updatepolicyoverride)|指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|啟用使用者代理程式用戶端提示功能 (已過時)|
|[UserDataDir](#userdatadir)|設定使用者資料目錄|
|[UserDataSnapshotRetentionLimit](#userdatasnapshotretentionlimit)|限制保留的使用者資料快照數量，以便在緊急復原時使用|
|[UserFeedbackAllowed](#userfeedbackallowed)|允許使用者意見反應|
|[VerticalTabsAllowed](#verticaltabsallowed)|設定瀏覽器側邊上索引標籤垂直版面配置的可用性|
|[VideoCaptureAllowed](#videocaptureallowed)|允許或封鎖視訊擷取|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|無需要求權限即可存取視訊擷取裝置的網站|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|設定 WPAD 最佳化|
|[WebAppInstallForceList](#webappinstallforcelist)|設定強制安裝 Web 應用程式的清單|
|[WebCaptureEnabled](#webcaptureenabled)|啟用 Microsoft Edge 中的 Web 擷取功能|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|在 M84 前，重新啟用 Web 元件 v0 API。|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|允許 WebDriver 覆寫不相容原則 (已過時) |
|[WebRtcAllowLegacyTLSProtocols](#webrtcallowlegacytlsprotocols)|在 WebRTC 中允許舊版 TLS/DTLS 降級 (已取代)|
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|管理由 WebRTC 暴露的本機 IP 位址|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|限制由 WebRTC 暴露的本機 IP 位址|
|[WebRtcUdpPortRange](#webrtcudpportrange)|限制 WebRTC 所使用的本機 UDP 連接埠範圍|
|[WebWidgetAllowed](#webwidgetallowed)|啟用Web 小工具|
|[WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup)|在 Windows 啟動時允許Web小工具|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|使用 Windows Proxy 解析程式 (已取代)|
|[WindowOcclusionEnabled](#windowocclusionenabled)|啟用視窗遮蔽|




  ## <a name="application-guard-settings-policies"></a>應用程式防護設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="applicationguardcontainerproxy"></a>ApplicationGuardContainerProxy

  #### <a name="application-guard-container-proxy"></a>應用程式防護容器 Proxy

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 應用程式防護的 Proxy 設定。
如果啟用此原則，則 Microsoft Edge 應用程式防護會忽略 Proxy 設定的其他來源。

如果未設定此原則，Microsoft Edge 應用程式防護會使用主機的 Proxy 設定。

此原則不會影響應用程式防護 (主機上) 以外 Microsoft Edge 的 Proxy 設定。

ProxyMode 欄位可讓您指定 Microsoft Edge 應用程式防護所使用的 Proxy 伺服器。

ProxyPacUrl 欄位是 Proxy .pac 檔案的 URL。

ProxyServer 欄位是 Proxy 伺服器的 URL。

如果選擇 'direct' 值做為 'ProxyMode'，則會忽略所有其他欄位。

如果選擇 'auto_detect' 值做為 'ProxyMode'，則會忽略所有其他欄位。

如果選擇 'fixed_servers' 值做為 'ProxyMode'，則會使用 'ProxyServer' 欄位。

如果選擇 'pac_script' 值做為 'ProxyMode'，則會使用 'ProxyPacUrl' 欄位。

如需透過雙 Proxy 識別應用程式防護流量的詳細資訊，請造訪 [https://go.microsoft.com/fwlink/?linkid=2134653](https://go.microsoft.com/fwlink/?linkid=2134653)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ApplicationGuardContainerProxy
  - GP 名稱：應用程式防護容器 Proxy
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/應用程式防護設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ApplicationGuardContainerProxy
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct",
  "ProxyPacUrl": "https://internal.site/example.pac",
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {"ProxyMode": "direct", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="applicationguardfavoritessyncenabled"></a>ApplicationGuardFavoritesSyncEnabled

  #### <a name="application-guard-favorites-sync-enabled"></a>已啟用應用程式防護我的最愛同步處理

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  此原則可讓啟用應用程式防護的 Microsoft Edge 電腦/裝置將我的最愛從主機同步處理到容器，以與我的最愛相符。

如果已設定 [ManagedFavorites](#managedfavorites) ，則這些最愛也會同步處理到容器。

如果您啟用這個原則，就會停用容器中的 [編輯我的最愛]。 因此，在容器瀏覽器的 UI 中，[新增我的最愛] 和 [新增我的最愛資料夾] 按鈕將會模糊。

如果您停用或不設定此原則，主機上的 [我的最愛] 將不會共用至容器。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： ApplicationGuardFavoritesSyncEnabled
  - GP 名稱：已啟用應用程式防護我的最愛同步處理
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/應用程式防護設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： ApplicationGuardFavoritesSyncEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="applicationguardtrafficidentificationenabled"></a>ApplicationGuardTrafficIdentificationEnabled

  #### <a name="application-guard-traffic-identification"></a>應用程式防護流量識別

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 91 或更新版本

  #### <a name="description"></a>描述

  如果您啟用或未設定此原則，應用程式防護會將額外的 HTTP 標頭 (X-MS-ApplicationGuard-Initiated) 新增至來自應用程式防護容器的所有傳出 HTTP 要求。

如果停用此原則，則額外的標頭不會新增到流量中。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱: ApplicationGuardTrafficIdentificationEnabled
  - GP 名稱: 應用程式防護流量識別
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/應用程式防護設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱: ApplicationGuardTrafficIdentificationEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="cast-policies"></a>投射原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enablemediarouter"></a>EnableMediaRouter

  #### <a name="enable-google-cast"></a>啟用 Google Cast

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用此原則以啟用 Google Cast。 使用者將可以從應用程式功能表、網頁內容功能表、已啟用投射的網站上的媒體控制項和 (如有顯示) 投射工具列圖示啟動它。

停用此原則可停用 Google Cast。

根據預設，Google Cast 將會啟用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableMediaRouter
  - GP 名稱：啟用 Google Cast
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/投射
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableMediaRouter
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableMediaRouter
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="showcasticonintoolbar"></a>ShowCastIconInToolbar

  #### <a name="show-the-cast-icon-in-the-toolbar"></a>在工具列中顯示投射圖示

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  將此原則設定為 true 即可在工具列或溢位功能表顯示投射工具列圖示。 使用者將無法移除它。

如果未設定或停用此原則，則使用者可使用圖示的關聯式功能表來釘選或移除圖示。

如果您也將 [EnableMediaRouter](#enablemediarouter) 原則設定為 false，則會忽略此原則，且不會顯示工具列圖示。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ShowCastIconInToolbar
  - GP 名稱：在工具列中顯示投射圖示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/投射
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ShowCastIconInToolbar
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ShowCastIconInToolbar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="content-settings-policies"></a>內容設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autoselectcertificateforurls"></a>AutoSelectCertificateForUrls

  #### <a name="automatically-select-client-certificates-for-these-sites"></a>自動選取這些網站的用戶端憑證

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定原則可讓您建立 URL 模式清單，以指定 Microsoft Edge 可自動選取用戶端憑證的網站。 這個值是 stringified JSON 字典的陣列，其中每個詞典都有下列兩種形式： "pattern"： "$URL _PATTERN"，"filter"： $FILTER}，其中 $URL _PATTERN 是內容設定模式。 $FILTER 會限制瀏覽器自動選取的用戶端憑證。 與篩選器無關，則只會選取符合伺服器憑證要求的憑證。

使用 $FILTER 區段的範例：

* 當 $FILTER 設為 {「發行人」： {"CN"： "$ISSUER _CN"}}，則只會選取 CommonName $ISSUER _CN 的憑證所頒發的用戶端憑證。

* 當 $FILTER 同時包含「發行人」和「主旨」區段時，只會選取符合這兩個條件的用戶端憑證。

* 當 $FILTER 中含有含有 "O" 值的「主旨」區段時，證書至少需要一個組織比指定的值相符。

* 當 $FILTER 包含含有「OU」值的「主旨」區段時，證書至少需要一個與指定的值相符的組織單位。

* 當 $FILTER 設為 [ {}] 時，不會進一步限制用戶端憑證的選取範圍。 請注意，網頁伺服器提供的篩選器仍然適用。

如果您將策略保留為取消，則任何網站都不會 autoselection。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoSelectCertificateForUrls
  - GP 名稱：自動選取這些網站的用戶端憑證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = "{\"pattern\":\"https://www.contoso.com\",\"filter\":{\"ISSUER\":{\"CN\":\"certificate issuer name\", \"L\": \"certificate issuer location\", \"O\": \"certificate issuer org\", \"OU\": \"certificate issuer org unit\"}, \"SUBJECT\":{\"CN\":\"certificate subject name\", \"L\": \"certificate subject location\", \"O\": \"certificate subject org\", \"OU\": \"certificate subject org unit\"}}}"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoSelectCertificateForUrls
  - 範例值：
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="cookiesallowedforurls"></a>CookiesAllowedForUrls

  #### <a name="allow-cookies-on-specific-sites"></a>允許特定網站上的 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義允許設定 Cookie 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需詳細資訊，請參閱 [CookiesBlockedForUrls](#cookiesblockedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 原則。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

若要避免在結束時刪除 Cookie，請設定 [SaveCookiesOnExit](#savecookiesonexit) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CookiesAllowedForUrls
  - GP 名稱：允許特定網站上的 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CookiesAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="cookiesblockedforurls"></a>CookiesBlockedForUrls

  #### <a name="block-cookies-on-specific-sites"></a>封鎖特定網站上的 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義無法設定 Cookie 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需詳細資訊，請參閱 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 原則。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CookiesBlockedForUrls
  - GP 名稱：封鎖特定網站上的 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CookiesBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="cookiessessiononlyforurls"></a>CookiesSessionOnlyForUrls

  #### <a name="limit-cookies-from-specific-websites-to-the-current-session"></a>限制來自特定網站的 Cookie 匯入目前的工作階段

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  工作階段結束 (關閉視窗) 時，會刪除由符合您所定義 URL 模式的網站建立的 Cookie。

由不符合模式的網站建立的 Cookie 會由 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或由使用者個人設定控制。 如果未設定此原則，則這也是預設行為。

您也可以使用 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesBlockedForUrls](#cookiesblockedforurls) 原則，以控制哪些網站可以建立 Cookie。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

如果將 [RestoreOnStartup](#restoreonstartup) 原則設定為從先前的工作階段還原 URL，即會忽略此原則，並為這些網站永久儲存 Cookie。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CookiesSessionOnlyForUrls
  - GP 名稱：限制來自特定網站的 Cookie 匯入目前的工作階段
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CookiesSessionOnlyForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultcookiessetting"></a>DefaultCookiesSetting

  #### <a name="configure-cookies"></a>設定 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制網站是否可在使用者的裝置上建立 Cookie。 此原則為全部或皆不 - 您可以讓所有網站建立 Cookie，或不讓任何網站建立 Cookie。 您無法使用此原則來啟用來自特定網站的 Cookie。

將原則設定為 'SessionOnly'，以在工作階段關閉時清除 Cookie。

如果未設定此原則，則會使用預設值 'AllowCookies'，且使用者可以在 Microsoft Edge 設定中變更此設定。 (如果您不希望使用者能夠變更此設定，請設定原則。)

原則選項對應：

* AllowCookies (1) = 讓所有網站建立 Cookie

* BlockCookies (2) = 不要讓任何網站建立 Cookie

* SessionOnly (4) = 在工作階段期間保留 Cookie，[SaveCookiesOnExit](#savecookiesonexit) 中所列的項目除外

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultCookiesSetting
  - GP 名稱：設定 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultCookiesSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultCookiesSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultfilesystemreadguardsetting"></a>DefaultFileSystemReadGuardSetting

  #### <a name="control-use-of-the-file-system-api-for-reading"></a>控制檔案系统 API 的讀取使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  如果將此原則設定為 3，則網站可以使用檔案系統 API 請求對主機作業系統檔案系統的讀取存取權。 如果將此原則設為2，存取權會遭到拒絕。

如果未設定此原則，網站可以要求存取權。 使用者可以變更這個設定。

原則選項對應：

* BlockFileSystemRead (2) = 不允許任何網站透過檔案系統 API 要求對檔案和目錄的讀取存取權

* BlockFileSystemRead (3) = 允許網站要求使用者透過檔案系統 API 授予對檔案和目錄的讀存取權

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultFileSystemReadGuardSetting
  - GP 名稱：控制檔案系统 API 的讀取使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DefaultFileSystemReadGuardSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultFileSystemReadGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultfilesystemwriteguardsetting"></a>DefaultFileSystemWriteGuardSetting

  #### <a name="control-use-of-the-file-system-api-for-writing"></a>控制檔案系統 API 的寫入使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  如果將此原則設定為 3，則網站可以使用檔案系統 API 請求對主機作業系統檔案系統的寫入存取權。 如果將此原則設為2，存取權會遭到拒絕。

如果未設定此原則，網站可以要求存取權。 使用者可以變更這個設定。

原則選項對應：

* BlockFileSystemWrite (2) = 不允許任何網站要求對檔案和目錄的寫入存取權

* AskFileSystemWrite (3) = 允許網站要求使用者授予對檔案和目錄的寫入存取權

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultFileSystemWriteGuardSetting
  - GP 名稱：控制檔案系统 API 的寫入使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DefaultFileSystemWriteGuardSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultFileSystmWriteGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultgeolocationsetting"></a>DefaultGeolocationSetting

  #### <a name="default-geolocation-setting"></a>預設地理位置設定值

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可追蹤使用者的實體位置。 您可以預設允許追蹤 ('AllowGeolocation')、預設拒絕 ('BlockGeolocation')，或在每次網站要求其位置時詢問使用者 ('AskGeolocation')。

如果未設定此原則，則會使用 'AskGeolocation'，且使用者可以變更此設定。

原則選項對應：

* AllowGeolocation (1) = 允許網站追蹤使用者的實體位置

* BlockGeolocation (2) = 不允許任何網站追蹤使用者的實體位置

* AskGeolocation (3) = 在網站要追蹤使用者的實體位置時詢問使用者

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultGeolocationSetting
  - GP 名稱：預設地理位置設定值
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultGeolocationSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultGeolocationSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultimagessetting"></a>DefaultImagesSetting

  #### <a name="default-images-setting"></a>預設影像設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以顯示影像。 您可以在所有網站上允許影像 ('AllowImages')，或在所有網站上封鎖影像 ('BlockImages')。

如果未設定此原則，則預設會允許顯示影像，且使用者可以變更此設定。

原則選項對應：

* AllowImages (1) = 允許所有網站顯示所有影像

* BlockImages (2) = 不允許任何網站顯示影像

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultImagesSetting
  - GP 名稱：預設影像設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultImagesSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultImagesSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultinsecurecontentsetting"></a>DefaultInsecureContentSetting

  #### <a name="control-use-of-insecure-content-exceptions"></a>控制不安全內容例外狀況的使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  允許您設定使用者是否可以新增例外，以允許特定網站的混合內容。

可以針對使用 [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) 和 [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) 原則的特定 URL 模式覆寫此原則。

如果未設定此原則，使用者將可以新增例外，以允許可封鎖的混合內容，並停用選擇性可封鎖混合內容的自動升級。

原則選項對應：

* BlockInsecureContent (2) = 不允許任何網站載入混合內容

* AllowExceptionsInsecureContent (3) = 允許使用者新增例外，以允許混合內容

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultInsecureContentSetting
  - GP 名稱：控制不安全內容例外狀況的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultInsecureContentSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultInsecureContentSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultjavascriptsetting"></a>DefaultJavaScriptSetting

  #### <a name="default-javascript-setting"></a>預設 JavaScript 設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以執行 JavaScript。 您可以為所有網站允許 ('AllowJavaScript') 或為所有網站封鎖 ('BlockJavaScript')。

如果未設定此原則，則預設為所有網站都可以執行 JavaScript，且使用者可以變更此設定。

原則選項對應：

* AllowJavaScript (1) = 允許所有網站執行 JavaScript

* BlockJavaScript (2) = 不允許任何網站執行 JavaScript

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultJavaScriptSetting
  - GP 名稱：預設 JavaScript 設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultJavaScriptSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultJavaScriptSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultnotificationssetting"></a>DefaultNotificationsSetting

  #### <a name="default-notification-setting"></a>預設通知設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以顯示桌面通知。 您可以預設允許 ('AllowNotifications')、預設拒絕 ('BlockNotifications')，或在每次網站想要顯示通知時詢問使用者 ('AskNotifications')。

如果未設定此原則，則預設為允許顯示通知，且使用者可以變更此設定。

原則選項對應：

* AllowNotifications (1) = 允許網站顯示桌面通知

* BlockNotifications (2) = 不允許任何網站顯示桌面通知

* AskNotifications (3) = 每次網站想要顯示桌面通知時詢問

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultNotificationsSetting
  - GP 名稱：預設通知設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultNotificationsSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultNotificationsSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultpluginssetting"></a>DefaultPluginsSetting

  #### <a name="default-adobe-flash-setting-obsolete"></a>預設 Adobe Flash 設定 (過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 87 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 87

  #### <a name="description"></a>描述

  由於 Microsoft Edge 不再支援 Flash，因此此原則不再有作用。

將先檢查 [PluginsAllowedForUrls](#pluginsallowedforurls) 和 [PluginsBlockedForUrls](#pluginsblockedforurls)，然後才是此原則。 選項為 'ClickToPlay' 和 'BlockPlugins'。 如果您將此原則設為 'BlockPlugins'，則所有網站皆會拒絕這個外掛程式。 'ClickToPlay' 可讓 Flash 外掛程式開始執行，但使用者可以按一下預留位置以啟動。

如果未設定此原則，則使用者可以手動變更此設定。

注意：自動播放只適用於在 [PluginsAllowedForUrls](#pluginsallowedforurls) 原則中明確列出的網域。 若要開啟所有網站的自動播放功能，請將 http://* 及 https://* 新增至 URLs 的允許清單中。

原則選項對應：

* BlockPlugins (2) = 封鎖 Adobe Flash 外掛程式

* ClickToPlay (3) = 按一下以播放

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultPluginsSetting
  - GP 名稱：預設 Adobe Flash 設定 (過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPluginsSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultPluginsSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultpopupssetting"></a>DefaultPopupsSetting

  #### <a name="default-pop-up-window-setting"></a>預設快顯視窗設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以顯示快顯視窗。 您可以在所有網站上允許 ('AllowPopups')，或在所有網站上封鎖 ('BlockPopups')。

如果未設定此原則，則預設會封鎖快顯視窗，且使用者可以變更此設定。

原則選項對應：

* AllowPopups (1) = 允許所有網站顯示快顯視窗

* BlockPopups (2) = 不允許任何網站顯示快顯視窗

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultPopupsSetting
  - GP 名稱：預設快顯視窗設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPopupsSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultPopupsSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultwebbluetoothguardsetting"></a>DefaultWebBluetoothGuardSetting

  #### <a name="control-use-of-the-web-bluetooth-api"></a>控制 Web 藍牙 API 的使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制網站是否能夠存取附近的藍牙裝置。 您可以完全封鎖或存取權或要求網站在每次想要存取藍牙裝置時詢問使用者。

如果未設定此原則，則會使用預設值 (AskWebBluetooth'，表示每次都詢問使用者)，且使用者可以變更此設定。

原則選項對應：

* BlockWebBluetooth (2) = 不允許任何網站使用 Web Bluetooth API 來要求存取藍牙裝置

* AskWebBluetooth (3) = 允許網站要求使用者授與附近藍牙裝置存取權

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultWebBluetoothGuardSetting
  - GP 名稱：控制 Web 藍牙 API 的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultWebBluetoothGuardSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultWebBluetoothGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultwebusbguardsetting"></a>DefaultWebUsbGuardSetting

  #### <a name="control-use-of-the-webusb-api"></a>控制 WebUSB API 的使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定網站是否能夠存取連接的 USB 裝置。 您可以完全封鎖存取或在每次網站想要取得連接的 USB 裝置的存取時詢問使用者。

您可以使用 [WebUsbAskForUrls](#webusbaskforurls) 和 [WebUsbBlockedForUrls](#webusbblockedforurls) 原則來針對特定 URL 模式覆寫此原則。

如果未設定此原則，則預設為網站可以詢問使用者是否可以存取連接的 USB 裝置 ('AskWebUsb')，且使用者可以變更此設定。

原則選項對應：

* BlockWebUsb (2) = 不允許任何網站透過 WebUSB API 要求存取 USB 裝置

* AskWebUsb (3) = 允許網站詢問使用者，以授與連接的 USB 裝置之存取權

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultWebUsbGuardSetting
  - GP 名稱：控制 WebUSB API 的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultWebUsbGuardSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultWebUsbGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="filesystemreadaskforurls"></a>FileSystemReadAskForUrls

  #### <a name="allow-read-access-via-the-file-system-api-on-these-sites"></a>允許透過這些網站上的檔案系統 API 讀取存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  透過設定原則，您可以列出URL模式，這些模式指定哪些網站可以要求使用者透過檔案系統 API 授予他們對主機作業系統檔案系統中的檔案或目錄的讀取存取權。

未設定原則意味著 [DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) 將套用於所有網站 (如果已設定)。 否則將套用使用者的個人設定。

URL 模式無法與 [FileSystemReadBlockedForUrls](#filesystemreadblockedforurls) 相衝突。 如果 URL 與兩者都相符，則兩個原則都不優先。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FileSystemReadAskForUrls
  - GP 名稱：允許透過這些網站上的檔案系統 API 讀取存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadAskForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FileSystemReadAskForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="filesystemreadblockedforurls"></a>FileSystemReadBlockedForUrls

  #### <a name="block-read-access-via-the-file-system-api-on-these-sites"></a>封鎖透過這些網站上的檔案系統 API 讀取存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  如果設定此原則，您可以列出URL模式，這些模式指定哪些網站可以要求使用者透過檔案系統 API 授予他們對主機作業系統檔案系統中的檔案或目錄的讀存取權。

如果您不設定此原則，[DefaultFileSystemReadGuardSetting](#defaultfilesystemreadguardsetting) 將套用於所有網站 (如果已設定)。 否則將套用使用者的個人設定。

URL 模式無法與 [FileSystemReadAskForUrls](#filesystemreadaskforurls) 相衝突。 如果 URL 與兩者都相符，則兩個原則都不優先。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FileSystemReadBlockedForUrls
  - GP 名稱：封鎖透過這些網站上的檔案系統 API 讀取存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemReadBlockedForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FileSystemReadBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="filesystemwriteaskforurls"></a>FileSystemWriteAskForUrls

  #### <a name="allow-write-access-to-files-and-directories-on-these-sites"></a>允許這些網站上的檔案和目錄的寫入存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  如果設定此原則，您可以列出URL模式，這些模式指定哪些網站可以要求使用者授予他們對主機作業系統檔案系統中的檔案或目錄的寫入取權。

如果您不設定此原則，[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) 將套用於所有網站 (如果已設定)。 否則將套用使用者的個人設定。

URL 模式無法與 [FileSystemWriteBlockedForUrls](#filesystemwriteblockedforurls) 相衝突。 如果 URL 與兩者都相符，則兩個原則都不優先。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FileSystemWriteAskForUrls
  - GP 名稱：允許這些網站上的檔案和目錄的寫入存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteAskForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FileSystemWriteAskForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="filesystemwriteblockedforurls"></a>FileSystemWriteBlockedForUrls

  #### <a name="block-write-access-to-files-and-directories-on-these-sites"></a>封鎖這些網站上的檔案和目錄的寫入存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  如果設定此原則，您可以列出URL模式，這些模式指定哪些網站不可以要求使用者授予他們對主機作業系統檔案系統中的檔案或目錄的寫入取權。

如果您不設定此原則，[DefaultFileSystemWriteGuardSetting](#defaultfilesystemwriteguardsetting) 將套用於所有網站 (如果已設定)。 否則將套用使用者的個人設定。

URL 模式無法與 [FileSystemWriteAskForUrls](#filesystemwriteaskforurls) 相衝突。 如果 URL 與兩者都相符，則兩個原則都不優先。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FileSystemWriteBlockedForUrls
  - GP 名稱：封鎖這些網站上的檔案和目錄的寫入存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\FileSystemWriteBlockedForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FileSystemWriteBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="imagesallowedforurls"></a>ImagesAllowedForUrls

  #### <a name="allow-images-on-these-sites"></a>允許這些網站上的影像

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義可顯示影像的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultImagesSetting](#defaultimagessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImagesAllowedForUrls
  - GP 名稱：允許這些網站上的影像
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImagesAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="imagesblockedforurls"></a>ImagesBlockedForUrls

  #### <a name="block-images-on-specific-sites"></a>封鎖特定網站上的影像

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義不允許顯示影像的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultImagesSetting](#defaultimagessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImagesBlockedForUrls
  - GP 名稱：封鎖特定網站上的影像
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImagesBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="insecurecontentallowedforurls"></a>InsecureContentAllowedForUrls

  #### <a name="allow-insecure-content-on-specified-sites"></a>允許指定網站上的不安全內容

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  建立 URL 模式的清單，以指定可顯示不安全混合內容 (即 HTTPS 網站上的 HTTP 內容) 的網站。

如果未設定此原則，則會封鎖可封鎖的混合內容，並升級選擇性可封鎖的混合內容。 不過，將允許使用者設定例外，以允許特定網站的不安全混合內容。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InsecureContentAllowedForUrls
  - GP 名稱：允許指定網站上的不安全內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：InsecureContentAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="insecurecontentblockedforurls"></a>InsecureContentBlockedForUrls

  #### <a name="block-insecure-content-on-specified-sites"></a>封鎖指定網站上的不安全內容

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  建立 URL 模式的清單，以指定不允許顯示可封鎖 (即使用中) 混合內容 (即 HTTPS 網站上的 HTTP 內容) 的網站，並針對它將選擇性可封鎖混合內容升級停用。

如果未設定此原則，則會封鎖可封鎖的混合內容，並升級選擇性可封鎖的混合內容。 不過，將允許使用者設定例外，以允許特定網站的不安全混合內容。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InsecureContentBlockedForUrls
  - GP 名稱：封鎖指定網站上的不安全內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：InsecureContentBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="javascriptallowedforurls"></a>JavaScriptAllowedForUrls

  #### <a name="allow-javascript-on-specific-sites"></a>允許特定網站上的 JavaScript

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義允許執行 JavaScript 的網站清單。

如果您未設定此原則 [，DefaultJavaScriptSetting](#defaultjavascriptsetting) 會套用於所有網站 (如果已設定)。 如果沒有，則會套用使用者的個人設定。

如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：JavaScriptAllowedForUrls
  - GP 名稱：允許特定網站上的 JavaScript
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：JavaScriptAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="javascriptblockedforurls"></a>JavaScriptBlockedForUrls

  #### <a name="block-javascript-on-specific-sites"></a>封鎖特定網站上的 JavaScript

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義不允許執行 JavaScript 的網站清單。

如果您未設定此原則 [，DefaultJavaScriptSetting](#defaultjavascriptsetting) 會套用於所有網站 (如果已設定)。 如果沒有，則會套用使用者的個人設定。

如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：JavaScriptBlockedForUrls
  - GP 名稱：封鎖特定網站上的 JavaScript
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：JavaScriptBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="legacysamesitecookiebehaviorenabled"></a>LegacySameSiteCookieBehaviorEnabled

  #### <a name="enable-default-legacy-samesite-cookie-behavior-setting-deprecated"></a>啟用預設舊版 SameSite Cookie 行為設定 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>說明

  此原則已過時，因為其目的只是為了提供做為短期的機制，並在發現企業與 SameSite 行為變更不相容時，給予它們更多的時間來更新其環境。

無法在 Microsoft Edge 版本 95 中使用。 如果您仍然需要舊版 Cookie 行為，請使用 [LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist) 來設定每個網域的行為。

讓您將所有 Cookie 還原為舊版 SameSite 行為。 若要還原為舊版行為，會導致沒有指定 SameSite 屬性的 cookie 視為 "SameSite = 無"，並移除「SameSite = None」 cookie 的需求，以傳送 "Secure" 屬性，並在評估兩個網站是否相同的網站時跳過方案比較。

如果您未設定此原則，cookie 的預設 SameSite 行為將視預設功能 (不含-SameSite-必須是-安全) 功能的 [Cookie]、[Schemeful 相同的網站] 功能而定。 這些功能也可由欄位試驗或相同-預設的網站-cookie 標誌 (不含相同網站的不相同的資料標記) 設定，或 edge://flags 中的 [schemeful] 網站標誌。

原則選項對應：

* DefaultToLegacySameSiteCookieBehavior (1) = 還原為所有網站上 Cookie 的舊版 SameSite 行為。

* DefaultToSameSiteByDefaultCookieBehavior (2) = 針對所有網站上 Cookie 使用預設的 SameSite 行為

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：LegacySameSiteCookieBehaviorEnabled
  - GP 名稱：啟用預設舊版 SameSite Cookie 行為設定 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：LegacySameSiteCookieBehaviorEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：LegacySameSiteCookieBehaviorEnabled
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="legacysamesitecookiebehaviorenabledfordomainlist"></a>LegacySameSiteCookieBehaviorEnabledForDomainList

  #### <a name="revert-to-legacy-samesite-behavior-for-cookies-on-specified-sites"></a>將指定網站上的 Cookie 還原至舊版 SameSite 行為

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  針對符合指定模式網域設定的 Cookie 將還原為舊版 SameSite 行為。

若要還原為舊版行為，會導致沒有指定 SameSite 屬性的 cookie 視為 "SameSite = 無"，並移除「SameSite = None」 cookie 的需求，以傳送 "Secure" 屬性，並在評估兩個網站是否相同的網站時跳過方案比較。

如果未設定此原則，則會使用全域預設值。 全域預設值也將用於您指定的模式未涵蓋的網域上的 Cookie。

在 Microsoft Edge 版本 95 推出前，全域預設值可以使用已取代的 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) 原則進行設定。 如果未設定 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)，則全域預設值會後援到其他設定來源。

請注意，您在此原則中列出的模式會被視為網域，而非 URL，因此不應指定配置或連接埠。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP 名稱：將指定網站上的 Cookie 還原至舊版 SameSite 行為
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = "www.example.com"
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：LegacySameSiteCookieBehaviorEnabledForDomainList
  - 範例值：
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="notificationsallowedforurls"></a>NotificationsAllowedForUrls

  #### <a name="allow-notifications-on-specific-sites"></a>允許特定網站上的通知

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓您建立 URL 模式的清單，以指定允許顯示通知的網站。

如果您未設定此原則，全域預設值將會套用至所有網站。 如果已設定此原則，預設值會取自　[DefaultNotificationsSetting](#defaultnotificationssetting) 原則或使用者的個人設定。 如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NotificationsAllowedForUrls
  - GP 名稱：允許特定網站上的通知
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NotificationsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="notificationsblockedforurls"></a>NotificationsBlockedForUrls

  #### <a name="block-notifications-on-specific-sites"></a>封鎖特定網站上的通知

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓您建立 URL 模式的清單，以指定不允許顯示通知的網站。

如果您未設定此原則，全域預設值將會套用至所有網站。 如果已設定此原則，預設值會取自　[DefaultNotificationsSetting](#defaultnotificationssetting) 原則或使用者的個人設定。 如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NotificationsBlockedForUrls
  - GP 名稱：封鎖特定網站上的通知
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NotificationsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="pluginsallowedforurls"></a>PluginsAllowedForUrls

  #### <a name="allow-the-adobe-flash-plug-in-on-specific-sites-obsolete"></a>允許特定網站上的 Adobe Flash 外掛程式 (過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 87 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 87

  #### <a name="description"></a>描述

  由於 Microsoft Edge 不再支援 Flash，因此此原則不再有作用。

根據 URL 的模式，定義可執行 Adobe Flash 外掛程式的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPluginsSetting](#defaultpluginssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 不過，從 M85 開始，此原則已不再支援主機使用帶有 '\*' 和 '[\*.]' 等的萬用字元。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PluginsAllowedForUrls
  - GP 名稱：允許特定網站上的 Adobe Flash 外掛程式 (過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = "http://contoso.edu:8080"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PluginsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="pluginsblockedforurls"></a>PluginsBlockedForUrls

  #### <a name="block-the-adobe-flash-plug-in-on-specific-sites-obsolete"></a>封鎖特定網站上的 Adobe Flash 外掛程式 (過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 87 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 87

  #### <a name="description"></a>描述

  由於 Microsoft Edge 不再支援 Flash，因此此原則不再有作用。

根據 URL 的模式，定義遭封鎖而無法執行 Adobe Flash 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPluginsSetting](#defaultpluginssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 不過，從 M85 開始，此原則已不再支援主機使用帶有 '\*' 和 '[\*.]' 等的萬用字元。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PluginsBlockedForUrls
  - GP 名稱：封鎖特定網站上的 Adobe Flash 外掛程式 (過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = "http://contoso.edu:8080"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PluginsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="popupsallowedforurls"></a>PopupsAllowedForUrls

  #### <a name="allow-pop-up-windows-on-specific-sites"></a>允許特定網站上的快顯視窗

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義可開啟快顯視窗的網站清單。 * 不是此原則可接受的值。

如果未設定此原則，則會對所有網站使用來自 [DefaultPopupsSetting](#defaultpopupssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PopupsAllowedForUrls
  - GP 名稱：允許特定網站上的快顯視窗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PopupsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="popupsblockedforurls"></a>PopupsBlockedForUrls

  #### <a name="block-pop-up-windows-on-specific-sites"></a>封鎖特定網站上的快顯視窗

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義遭封鎖而無法開啟快顯視窗的網站清單。 * 不是此原則可接受的值。

如果未設定此原則，則會對所有網站使用來自 [DefaultPopupsSetting](#defaultpopupssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PopupsBlockedForUrls
  - GP 名稱：封鎖特定網站上的快顯視窗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PopupsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="registeredprotocolhandlers"></a>RegisteredProtocolHandlers

  #### <a name="register-protocol-handlers"></a>登錄通訊協定處理常式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定這個原則 (僅限建議使用) 來登錄通訊協定處理常式清單。 此清單會與使用者登錄的清單合併，而且兩者皆可供使用。

登錄通訊協定處理常式：

- 將通訊協定屬性設定為配置 (例如「mailto」)
- 將 URL 屬性設定為處理「通訊協定」欄位中指定配置的應用程式之 URL 屬性。 模式可以包含「%s」預留位置，它會由已處理的 URL 取代。

使用者無法移除由此原則登錄的通訊協定處理常式。 不過，他們可以安裝新的預設通訊協定處理常式來覆寫現有的通訊協定處理常式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：否
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RegisteredProtocolHandlers
  - GP 名稱：登錄通訊協定處理常式
  - GP 路徑 (強制)：不適用
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/內容設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：不適用
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：RegisteredProtocolHandlers
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true,
    "protocol": "mailto",
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [{"default": true, "protocol": "mailto", "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RegisteredProtocolHandlers
  - 範例值：
``` xml
<key>RegisteredProtocolHandlers</key>
<array>
  <dict>
    <key>default</key>
    <true/>
    <key>protocol</key>
    <string>mailto</string>
    <key>url</key>
    <string>https://mail.contoso.com/mail/?extsrc=mailto&url=%s</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="spotlightexperiencesandrecommendationsenabled"></a>SpotlightExperiencesAndRecommendationsEnabled

  #### <a name="choose-whether-users-can-receive-customized-background-images-and-text-suggestions-notifications-and-tips-for-microsoft-services"></a>選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知，及 [Microsoft 服務] 的提示

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知，及 [Microsoft 服務] 的提示。

若您啟用或不設置此設定，精選體驗和建議便會開啟。

若您停用此設定，精選體驗和建議便會關閉。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SpotlightExperiencesAndRecommendationsEnabled
  - GP 名稱：選擇使用者是否能夠收到自訂的桌面背景影像和文字、建議、通知，及 [Microsoft 服務] 的提示。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SpotlightExperiencesAndRecommendationsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webusballowdevicesforurls"></a>WebUsbAllowDevicesForUrls

  #### <a name="grant-access-to-specific-sites-to-connect-to-specific-usb-devices"></a>授與特定網站連線到特定 USB 裝置的存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許您設定一份 URL 清單，指定哪些網站會自動獲授與權限，以存取具有指定廠商和產品識別碼的 USB 裝置。 清單中的每個項目都必須包含裝置和 URL，原則才會有效。 裝置中的每個項目都可以包含廠商識別碼和產品識別碼欄位。 省略的任何識別碼都會被視為萬用字元，並有一個例外，且該例外是不能指定產品識別碼但未同時指定廠商識別碼。 否則，原則將會無效，且會被忽略。

USB 權限模型會使用要求端網站的 URL (「要求端 URL」) 和最上層框架網站的 URL (「內嵌 URL」)，將授權授與給要求端 URL 以存取 USB 裝置。 在 iframe 中載入要求端網站時，要求端 URL 可能與內嵌 URL 不同。 因此，"urls" 欄位最多可包含兩個以逗號分隔的 URL 字串，以便分別指定要求端和內嵌 URL。 如果僅指定一個 URL，當要求端網站的 URL 與符合此 URL 時，就會授與對應的 USB 裝置的存取權，而無論內嵌狀態為何。 "urls" 中的 URL 必須是有效的 URL，否則將忽略該原則。

如果將此原則保留為未設定，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

此原則中的 URL 模式不應與透過 [WebUsbBlockedForUrls](#webusbblockedforurls) 設定的衝突。 如果發生衝突，則此原則優先於 [WebUsbBlockedForUrls](#webusbblockedforurls) 和 [WebUsbAskForUrls](#webusbaskforurls)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebUsbAllowDevicesForUrls
  - GP 名稱：授與特定網站連線到特定 USB 裝置的存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebUsbAllowDevicesForUrls
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [
  {
    "devices": [
      {
        "product_id": 5678,
        "vendor_id": 1234
      }
    ],
    "urls": [
      "https://contoso.com",
      "https://fabrikam.com"
    ]
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebUsbAllowDevicesForUrls = [{"devices": [{"product_id": 5678, "vendor_id": 1234}], "urls": ["https://contoso.com", "https://fabrikam.com"]}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebUsbAllowDevicesForUrls
  - 範例值：
``` xml
<key>WebUsbAllowDevicesForUrls</key>
<array>
  <dict>
    <key>devices</key>
    <array>
      <dict>
        <key>product_id</key>
        <integer>5678</integer>
        <key>vendor_id</key>
        <integer>1234</integer>
      </dict>
    </array>
    <key>urls</key>
    <array>
      <string>https://contoso.com</string>
      <string>https://fabrikam.com</string>
    </array>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webusbaskforurls"></a>WebUsbAskForUrls

  #### <a name="allow-webusb-on-specific-sites"></a>允許特定網站上的 WebUSB

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義可要求使用者取得 USB 裝置存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

在此原則中定義的 URL 模式不能與 [WebUsbBlockedForUrls](#webusbblockedforurls) 原則中設定的衝突，您不能同時允許和封鎖一個 URL。 如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebUsbAskForUrls
  - GP 名稱：允許特定網站上的 WebUSB
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebUsbAskForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webusbblockedforurls"></a>WebUsbBlockedForUrls

  #### <a name="block-webusb-on-specific-sites"></a>封鎖特定網站上的 WebUSB

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義無法要求使用者授與其 USB 裝置存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

在此原則中定義的 URL 模式不能與 [WebUsbAskForUrls](#webusbaskforurls) 原則中設定的衝突。 您不能同時允許和封鎖 URL。  如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebUsbBlockedForUrls
  - GP 名稱：封鎖特定網站上的 WebUSB
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebUsbBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="default-search-provider-policies"></a>預設搜尋提供者原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchproviderenabled"></a>DefaultSearchProviderEnabled

  #### <a name="enable-the-default-search-provider"></a>啟用預設搜尋提供者

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用使用預設搜尋提供者的功能。

如果啟用此原則，則使用者可以透過在網址列中輸入來搜尋字詞 (只要其輸入內容不是 URL 即可)。

您可以啟用其餘的預設搜尋原則，以指定要使用的預設搜尋提供者。 如果保留空白 (未設定) 或設定不正確，則使用者可以選擇預設提供者。

如果停用此原則，則使用者無法從網址列搜尋。

如果啟用或停用此原則，則使用者無法變更或覆寫它。

如果未設定此原則，則會啟用預設搜尋提供者，且使用者可以選擇預設搜尋提供者，並設定搜尋提供者清單。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderEnabled
  - GP 名稱：啟用預設搜尋提供者
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchproviderencodings"></a>DefaultSearchProviderEncodings

  #### <a name="default-search-provider-encodings"></a>預設搜尋提供者編碼

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定的搜尋提供者所支援的字元編碼方式。 編碼是字碼頁名稱，如 UTF-8、GB2312 和 ISO-8859-1。 這些編碼會按提供的順序進行嘗試。

此原則是選擇性的。 如果未設定，則使用預設值 UTF-8。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderEncodings
  - GP 名稱：預設搜尋提供者編碼
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended\DefaultSearchProviderEncodings
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = "UTF-8"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = "UTF-16"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = "GB2312"
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = "ISO-8859-1"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderEncodings
  - 範例值：
``` xml
<array>
  <string>UTF-8</string>
  <string>UTF-16</string>
  <string>GB2312</string>
  <string>ISO-8859-1</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchproviderimageurl"></a>DefaultSearchProviderImageURL

  #### <a name="specifies-the-search-by-image-feature-for-the-default-search-provider"></a>指定預設搜尋提供者的影像搜尋功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定要用於影像搜尋的搜尋引擎 URL。 搜尋要求會使用 GET 方法傳送。

此原則是選擇性的。 如果未設定，則影像搜尋無法使用。

將 Bing 的影像搜尋 URL 指定為：'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'。

將 Google 的影像搜尋 URL 指定為：'{google:baseURL}searchbyimage/upload'。

請參閱 [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) 原則，以完成影像搜尋的設定。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderImageURL
  - GP 名稱：指定預設搜尋提供者的影像搜尋功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderImageURL
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://search.contoso.com/searchbyimage/upload"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderImageURL
  - 範例值：
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchproviderimageurlpostparams"></a>DefaultSearchProviderImageURLPostParams

  #### <a name="parameters-for-an-image-url-that-uses-post"></a>使用 POST 的影像 URL 參數

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則，則會指定執行使用 POST 的影像搜尋時使用的參數。 原則是由以逗號分隔的名稱/值對組成。 如果值為範本參數，像是前述範例中的 {imageThumbnail}，則會被實際影像縮圖資料所取代。 僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

將 Bing 的影像搜尋 URL Post 參數指定為：'imageBin={google:imageThumbnailBase64}'。

將 Google 的影像搜尋 URL Post 參數指定為：'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'。

如果您未設定此原則，則會使用 GET 方式傳送影像搜尋要求。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderImageURLPostParams
  - GP 名稱：使用 POST 的影像 URL 參數
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderImageURLPostParams
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"content={imageThumbnail},url={imageURL},sbisrc={SearchSource}"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderImageURLPostParams
  - 範例值：
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchproviderkeyword"></a>DefaultSearchProviderKeyword

  #### <a name="default-search-provider-keyword"></a>預設搜尋提供者關鍵字

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定關鍵字，這是在網址列中用來觸發此提供者的搜尋的捷徑。

此原則是選擇性的。 如果未設定，則任何關鍵字都無法啟動搜尋提供者。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderKeyword
  - GP 名稱：預設搜尋提供者關鍵字
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderKeyword
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"mis"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderKeyword
  - 範例值：
``` xml
<string>mis</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchprovidername"></a>DefaultSearchProviderName

  #### <a name="default-search-provider-name"></a>預設搜尋提供者名稱

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定預設搜尋提供者的名稱。

如果啟用此原則，則您可以設定預設搜尋提供者的名稱。

如果未啟用此原則，或如果將它保留為空白，則會使用由搜尋 URL 指定的主機名稱。

'DefaultSearchProviderName' 應設定為與 DTBC-0008 中設定的加密搜尋提供者對應、組織核准的加密搜尋提供者。 僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderName
  - GP 名稱：預設搜尋提供者名稱
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderName
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"My Intranet Search"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderName
  - 範例值：
``` xml
<string>My Intranet Search</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchprovidersearchurl"></a>DefaultSearchProviderSearchURL

  #### <a name="default-search-provider-search-url"></a>預設搜尋提供者搜尋 URL

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定要用於預設搜尋的搜尋引擎 URL。 URL 包含字串 '{searchTerms}'，它會在查詢時以使用者搜尋的字詞取代。

將 Bing 的搜尋 URL 指定為：

'{bing:baseURL}search?q={searchTerms}'。

將 Google 的搜尋 URL 指定為：'{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'。

啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 原則時，需要此原則；如果未啟用前項原則，則會忽略此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderSearchURL
  - GP 名稱：預設搜尋提供者搜尋 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderSearchURL
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://search.contoso.com/search?q={searchTerms}"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderSearchURL
  - 範例值：
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchprovidersuggesturl"></a>DefaultSearchProviderSuggestURL

  #### <a name="default-search-provider-url-for-suggestions"></a>預設建議的搜尋提供者 URL

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定用來提供搜尋建議之搜尋引擎的 URL。 URL 包含字串 '{searchTerms}'，它會在查詢時以使用者目前輸入的文字取代。

此原則是選擇性的。 如果未設定，則使用者不會看到搜尋建議；他們會看到來自瀏覽歷程記錄和我的最愛的建議。

Bing 的建議 URL 可以指定為：

'{bing:baseURL}qbox?query={searchTerms}'。

Google 的建議 URL 可指定為：'{google:baseURL}complete/search?output=chrome&q={searchTerms}'。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderSuggestURL
  - GP 名稱：預設建議的搜尋提供者 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderSuggestURL
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://search.contoso.com/suggest?q={searchTerms}"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderSuggestURL
  - 範例值：
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagesearchbox"></a>NewTabPageSearchBox

  #### <a name="configure-the-new-tab-page-search-box-experience"></a>設定新的索引標籤頁面搜尋體驗

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  您可以設定新的索引標籤頁面搜尋方塊，使用搜尋方塊「搜尋方塊 (建議使用) 」或「位址列」來搜尋新的索引標籤。 只有當您將搜尋引擎設定為 Bing 以外的值時，才能使用此原則，只要設定下列兩種原則：[DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和[DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)。

 如果您停用或未設定此原則以及：

- 如果 [位址列] 預設搜尋引擎為 Bing，新增的索引標籤頁面會在新索引標籤上使用搜尋方塊進行搜尋。
- 如果 [位址列] 預設搜尋引擎不是 Bing，當使用者在新的索引標籤上搜尋時，系統會使用者提供其他的選項 (使用「位址列」)。


如果您啟用這個原則，並將它設定為：

- 「搜尋方塊 (建議使用) 」 ("bing") ，新增的索引標籤會在新的索引標籤上使用搜尋方塊進行搜尋。
- 「位址列」 ([重新導向]) ，新增索引標籤的搜尋 方塊會在新的索引標籤上使用 [位址] 列進行搜尋。

原則選項對應：

* bing (bing) = 搜尋方塊 (建議使用)

* 重新導向 (redirect) = 網址列

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageSearchBox
  - GP 名稱：設定新的索引標籤頁面搜尋體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageSearchBox
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"bing"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageSearchBox
  - 範例值：
``` xml
<string>bing</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="extensions-policies"></a>擴充功能原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="blockexternalextensions"></a>BlockExternalExtensions

  #### <a name="blocks-external-extensions-from-being-installed"></a>封鎖安裝外部擴充功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  控制外部擴充功能的安裝。

如果啟用此設定，則會封鎖安裝外部擴充功能。

如果停用此原則或保留未設定，則會允許安裝外部擴充功能。

外部擴充功能及其安裝會記錄在 ./microsoft-edge/extensions-chromium/developer-guide/alternate-distribution-options。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BlockExternalExtensions
  - GP 名稱：封鎖安裝外部擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BlockExternalExtensions
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BlockExternalExtensions
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensionallowedtypes"></a>ExtensionAllowedTypes

  #### <a name="configure-allowed-extension-types"></a>設定允許的擴充功能類型

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定原則會控制哪些應用程式和擴充功能可能會安裝在 Microsoft Edge 中，這些應用程式與擴充功能可以與哪些主機進行互動，以及限制執行時間存取。

如果您沒有設定此原則，則對可接受的副檔名和應用程式類型沒有任何限制。

類型不在清單中的擴充功能和應用程式將不會安裝。 每個值都應該是下列其中一個字串：

* 「擴充功能」

* 「佈景主題」

* 「user_script」

* 「hosted_app」

如需有關這些類型的詳細資訊，請參閱 Microsoft Edge 擴充功能文件。

注意：此原則也會影響使用 [ExtensionInstallForcelist](#extensioninstallforcelist)強制安裝的擴充功能和應用程式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionAllowedTypes
  - GP 名稱：設定允許的擴充功能類型
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = "hosted_app"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionAllowedTypes
  - 範例值：
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensioninstallallowlist"></a>ExtensionInstallAllowlist

  #### <a name="allow-specific-extensions-to-be-installed"></a>允許安裝特定擴充功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定此原則會指定不受此封鎖清單所規範的擴充功能。

* 的封鎖清單值表示所有的擴充功能都遭到封鎖，而使用者只能安裝允許清單中所列的擴充功能。

根據預設，會允許所有擴充功能。 不過，如果您以原則來禁止擴充功能，您可以使用此允許的擴充功能清單來變更該原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionInstallAllowlist
  - GP 名稱：允許安裝特定擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = "extension_id2"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionInstallAllowlist
  - 範例值：
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensioninstallblocklist"></a>ExtensionInstallBlocklist

  #### <a name="control-which-extensions-cannot-be-installed"></a>控制不能安裝哪些擴充功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓您指定使用者無法安裝的擴充功能。 已安裝的擴充功能若遭封鎖則會停用，使用者無法啟用它們。 停用的擴充功能從封鎖清單移除中移除後，系統會自動重新啟用該功能。

'\*' 的封鎖清單值表示所有副檔名都被封鎖，除非它們明確地列在 allowlist 中。

如果未設定此原則，使用者可以在 Microsoft Edge 中安裝任何擴充功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionInstallBlocklist
  - GP 名稱：控制不能安裝哪些擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = "extension_id1"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = "extension_id2"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionInstallBlocklist
  - 範例值：
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensioninstallforcelist"></a>ExtensionInstallForcelist

  #### <a name="control-which-extensions-are-installed-silently"></a>控制哪些擴充功能會以無訊息方式安裝

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定此原則，以指定無需使用者互動即可自動安裝的應用程式和擴充功能清單。 使用者無法解除安裝或關閉此設定。 還會針對 enterprise.deviceAttributes 和 enterprise.platformKeys 擴充功能 API 隱含授與權限。 注意：這些兩個 API 不適用於未強制安裝的應用程式和擴充功能。

如果您未設定此原則，就不會自動安裝任何應用程式或擴充功能，且使用者可以解除安裝 Microsoft Edge 中的任何應用程式。

這個原則取代 [ExtensionInstallBlocklist](#extensioninstallblocklist) 原則。 如果先前的應用程式或擴充功能已從這個清單中移除，Microsoft Edge 會自動將其解除安裝。

在 Microsoft Windows 實例上，只有當實例加入至 Microsoft Active Directory 網域且執行 Windows 10 專業版時，才能強制安裝 Microsoft Edge 附加元件網站外部的應用程式和擴充功能。

在 macOS 實例上，如果實例是透過 MDM 管理，或透過 MCX 加入至網域，才能強制安裝 Microsoft Edge 附加元件網站外部的應用程式和擴充功能。

使用者可以使用開發人員工具變更任何擴充功能的原始程式碼，這可能導致擴充功能無法正常執行。 如果這是個重要問題，請設定 DeveloperToolsDisabled 原則。

原則的每個清單項目都是包含擴充功能 ID 的字串，也可以選擇使用分號 (; ) 分隔的「更新」URL。 擴充功能 ID 是在開發人員模式 (例如，在 edge://extensions 上) 中找到的 32 個字母字串。 如果已指定，則「更新」URL 應該指向更新資訊清單 XML 文件 ( [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) )。 根據預設，會使用 Microsoft Edge 附加元件網站的更新 URL。 此原則中設定的「更新」URL 只會用於初始安裝；此擴充功能的後續更新會在擴充功能的資訊清單中使用更新 URL。

注意：此原則不適用於 InPrivate 模式。 閱讀主應用程式擴充功能 (./microsoft-edge/extensions-chromium/enterprise/hosting-and-updating)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionInstallForcelist
  - GP 名稱：控制哪些擴充功能會以無訊息方式安裝
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = "gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx"
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = "abcdefghijklmnopabcdefghijklmnop"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionInstallForcelist
  - 範例值：
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensioninstallsources"></a>ExtensionInstallSources

  #### <a name="configure-extension-and-user-script-install-sources"></a>設定擴充功能與使用者指令碼安裝來源

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  定義可安裝擴充功能和主題的 URL。

定義可直接安裝擴充和主題的 URL，而不需將套件拖放到 edge://extensions 頁面。

此清單中的每個項目都是擴充功能式比對模式 (請參閱 [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039))。 使用者可以從符合此清單中項目的任何 URL 輕鬆安裝項目。 這些模式必須同時允許 *.crx 檔案的位置，以及開始下載網頁的位置 (也就是查閱者)。 請勿將檔案存放在需要驗證的位置。

[ExtensionInstallBlocklist](#extensioninstallblocklist) 原則優先於此原則。 不會安裝封鎖清單上的任何擴充功能，即使它來自此清單上的網站。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionInstallSources
  - GP 名稱：設定擴充功能與使用者指令碼安裝來源
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = "https://corp.contoso.com/*"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionInstallSources
  - 範例值：
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="extensionsettings"></a>ExtensionSettings

  #### <a name="configure-extension-management-settings"></a>設定擴充功能管理設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定此原則會控制 Microsoft Edge 的擴充功能管理設定，包括任何由現有的擴充功能相關原則所控制的功能。 這個原則取代任何可能設定的舊版原則。

此原則只會將擴充功能 ID 或更新 URL 對應至其特定設定。 您可以針對特殊 ID "*" 設定預設組態，這將適用於此原則中不含自訂設定的所有擴充功能。 有了更新 URL，設定就會套用到擴充功能資訊清單中具有所述之精準更新 URL 的擴充功能。 若要瞭解詳細資訊，請於線上 [https://go.microsoft.com/fwlink/?linkid=2161555](https://go.microsoft.com/fwlink/?linkid=2161555) 參閱 ExtensionSettings 原則的詳細指南。

若要封鎖來自特定協力廠商商店的延伸，您只需要封鎖該商店的 update_url。 例如，如果您想要封鎖 Chrome 線上應用程式商店的延伸，您可以使用下列 JSON。

{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}}

請注意，您仍然可以使用 [ExtensionInstallForcelist](#extensioninstallforcelist) 和 [ExtensionInstallAllowlist](#extensioninstallallowlist) 來允許/強制安裝特定延伸，即使是在前一個範例中使用 JSON 來封鎖商店。

注意：對於未加入 Microsoft Active Directory 網域的 Windows 執行個體，強制安裝僅限於 Microsoft Edge 附加元件網站中所列的應用程式和擴充功能。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExtensionSettings
  - GP 名稱：設定擴充功能管理設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExtensionSettings
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {
  "*": {
    "allowed_types": [
      "hosted_app"
    ],
    "blocked_install_message": "Custom error message.",
    "blocked_permissions": [
      "downloads",
      "bookmarks"
    ],
    "install_sources": [
      "https://company-intranet/apps"
    ],
    "installation_mode": "blocked",
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ],
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ]
  },
  "abcdefghijklmnopabcdefghijklmnop": {
    "blocked_permissions": [
      "history"
    ],
    "installation_mode": "allowed",
    "minimum_version_required": "1.0.1"
  },
  "bcdefghijklmnopabcdefghijklmnopa": {
    "allowed_permissions": [
      "downloads"
    ],
    "installation_mode": "force_installed",
    "runtime_allowed_hosts": [
      "*://good.contoso.com"
    ],
    "runtime_blocked_hosts": [
      "*://*.contoso.com"
    ],
    "update_url": "https://contoso.com/update_url"
  },
  "cdefghijklmnopabcdefghijklmnopab": {
    "blocked_install_message": "Custom error message.",
    "installation_mode": "blocked"
  },
  "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {
    "blocked_install_message": "Custom error message.",
    "installation_mode": "blocked"
  },
  "fghijklmnopabcdefghijklmnopabcde": {
    "blocked_install_message": "Custom removal message.",
    "installation_mode": "removed"
  },
  "update_url:https://www.contoso.com/update.xml": {
    "allowed_permissions": [
      "downloads"
    ],
    "blocked_permissions": [
      "wallpaper"
    ],
    "installation_mode": "allowed"
  }
}
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings = {"*": {"allowed_types": ["hosted_app"], "blocked_install_message": "Custom error message.", "blocked_permissions": ["downloads", "bookmarks"], "install_sources": ["https://company-intranet/apps"], "installation_mode": "blocked", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"]}, "abcdefghijklmnopabcdefghijklmnop": {"blocked_permissions": ["history"], "installation_mode": "allowed", "minimum_version_required": "1.0.1"}, "bcdefghijklmnopabcdefghijklmnopa": {"allowed_permissions": ["downloads"], "installation_mode": "force_installed", "runtime_allowed_hosts": ["*://good.contoso.com"], "runtime_blocked_hosts": ["*://*.contoso.com"], "update_url": "https://contoso.com/update_url"}, "cdefghijklmnopabcdefghijklmnopab": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd": {"blocked_install_message": "Custom error message.", "installation_mode": "blocked"}, "fghijklmnopabcdefghijklmnopabcde": {"blocked_install_message": "Custom removal message.", "installation_mode": "removed"}, "update_url:https://www.contoso.com/update.xml": {"allowed_permissions": ["downloads"], "blocked_permissions": ["wallpaper"], "installation_mode": "allowed"}}
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExtensionSettings
  - 範例值：
``` xml
<key>ExtensionSettings</key>
<dict>
  <key>*</key>
  <dict>
    <key>allowed_types</key>
    <array>
      <string>hosted_app</string>
    </array>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>blocked_permissions</key>
    <array>
      <string>downloads</string>
      <string>bookmarks</string>
    </array>
    <key>install_sources</key>
    <array>
      <string>https://company-intranet/apps</string>
    </array>
    <key>installation_mode</key>
    <string>blocked</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
  </dict>
  <key>abcdefghijklmnopabcdefghijklmnop</key>
  <dict>
    <key>blocked_permissions</key>
    <array>
      <string>history</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
    <key>minimum_version_required</key>
    <string>1.0.1</string>
  </dict>
  <key>bcdefghijklmnopabcdefghijklmnopa</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>installation_mode</key>
    <string>force_installed</string>
    <key>runtime_allowed_hosts</key>
    <array>
      <string>*://good.contoso.com</string>
    </array>
    <key>runtime_blocked_hosts</key>
    <array>
      <string>*://*.contoso.com</string>
    </array>
    <key>update_url</key>
    <string>https://contoso.com/update_url</string>
  </dict>
  <key>cdefghijklmnopabcdefghijklmnopab</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>defghijklmnopabcdefghijklmnopabc,efghijklmnopabcdefghijklmnopabcd</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom error message.</string>
    <key>installation_mode</key>
    <string>blocked</string>
  </dict>
  <key>fghijklmnopabcdefghijklmnopabcde</key>
  <dict>
    <key>blocked_install_message</key>
    <string>Custom removal message.</string>
    <key>installation_mode</key>
    <string>removed</string>
  </dict>
  <key>update_url:https://www.contoso.com/update.xml</key>
  <dict>
    <key>allowed_permissions</key>
    <array>
      <string>downloads</string>
    </array>
    <key>blocked_permissions</key>
    <array>
      <string>wallpaper</string>
    </array>
    <key>installation_mode</key>
    <string>allowed</string>
  </dict>
</dict>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="http-authentication-policies"></a>HTTP 驗證原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowcrossoriginauthprompt"></a>AllowCrossOriginAuthPrompt

  #### <a name="allow-cross-origin-http-authentication-prompts"></a>允許跨來源 HTTP 驗證提示

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制頁面中的協力廠商影像是否可以顯示驗證提示。

通常，這會因為網路釣魚防禦而將它停用。 如果您未設定此原則，系統會停用此原則，協力廠商影像無法顯示驗證提示。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowCrossOriginAuthPrompt
  - GP 名稱：允許跨來源 HTTP 驗證提示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowCrossOriginAuthPrompt
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowCrossOriginAuthPrompt
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="authnegotiatedelegateallowlist"></a>AuthNegotiateDelegateAllowlist

  #### <a name="specifies-a-list-of-servers-that-microsoft-edge-can-delegate-user-credentials-to"></a>指定 Microsoft Edge 可以委派使用者認證的伺服器清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 可以委派的伺服器清單。

使用逗號分隔多個伺服器名稱。 允許使用萬用字元 (*)。

如果未設定此原則，Microsoft Edge 將不會委派使用者認證，即使將伺服器偵測為內部網路亦然。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AuthNegotiateDelegateAllowlist
  - GP 名稱：指定 Microsoft Edge 可以委派使用者認證的伺服器清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthNegotiateDelegateAllowlist
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"contoso.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AuthNegotiateDelegateAllowlist
  - 範例值：
``` xml
<string>contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="authschemes"></a>AuthSchemes

  #### <a name="supported-authentication-schemes"></a>支援的驗證配置

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定支援的 HTTP 驗證配置。

您可以使用這些值來設定原則：'basic'、'digest'、'ntlm' 和 'negotiate'。 使用逗號分隔多個值。

如果未設定此原則，則會使用所有四個配置。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AuthSchemes
  - GP 名稱：支援的驗證配置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthSchemes
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"basic,digest,ntlm,negotiate"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AuthSchemes
  - 範例值：
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="authserverallowlist"></a>AuthServerAllowlist

  #### <a name="configure-list-of-allowed-authentication-servers"></a>設定允許驗證伺服器的清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定要啟用整合式驗證的伺服器。 只有在 Microsoft Edge 收到來自 Proxy 或此清單中伺服器的驗證挑戰時，才會啟用整合式驗證。

使用逗號分隔多個伺服器名稱。 允許使用萬用字元 (*)。

如果未設定此原則，則 Microsoft Edge 會嘗試偵測伺服器是否在內部網路上，並在這麼做之後才會回應 IWA 要求。 如果伺服器在網際網路上，則 Microsoft Edge 會忽略來自該伺服器的 IWA 要求。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AuthServerAllowlist
  - GP 名稱：設定允許驗證伺服器的清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthServerAllowlist
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"*contoso.com,contoso.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AuthServerAllowlist
  - 範例值：
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="basicauthoverhttpenabled"></a>BasicAuthOverHttpEnabled

  #### <a name="allow-basic-authentication-for-http"></a>允許 HTTP 的基本驗證

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  如果您啟用此原則或將它保留為未設，將允許透過非安全 HTTP 接收基本驗證挑戰。

如果您停用這個原則，來自基本驗證架構的非安全 HTTP 要求會遭到封鎖，且只允許安全的 HTTPS。

如果已設定 [AuthSchemes](#authschemes) 原則，且不包含基本原則 ，則請忽略此原則設定 (且禁止使用基本原則)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： BasicAuthOverHttpEnabled
  - GP 名稱：允許 HTTP 的基本驗證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： BasicAuthOverHttpEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： BasicAuthOverHttpEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="disableauthnegotiatecnamelookup"></a>DisableAuthNegotiateCnameLookup

  #### <a name="disable-cname-lookup-when-negotiating-kerberos-authentication"></a>當協調 Kerberos 驗證時停用 CNAME 查閱

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  決定產生的 Kerberos SPN 是根據一般 DNS 名稱 (CNAME) 或是輸入的原始名稱。

如果啟用此原則，則會略過 CNAME 查閱，並使用伺服器名稱 (如輸入的內容)。

如果停用或未設定此原則，則會使用伺服器的正式名稱。  這是透過 CNAME 查閱決定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DisableAuthNegotiateCnameLookup
  - GP 名稱：當協調 Kerberos 驗證時停用 CNAME 查閱
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DisableAuthNegotiateCnameLookup
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DisableAuthNegotiateCnameLookup
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enableauthnegotiateport"></a>EnableAuthNegotiatePort

  #### <a name="include-non-standard-port-in-kerberos-spn"></a>Kerberos SPN 中包含非標準連接埠

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定產生的 Kerberos SPN 是否應包含非標準連接埠。

如果啟用此原則，且使用者在 URL 中包含非標準連接埠 (80 或 443 以外的連接埠)，則該連接埠會包含在產生的 Kerberos SPN 中。

如果未設定或停用此原則，則在任何情況下，產生的 Kerberos SPN 將不會包含連接埠。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableAuthNegotiatePort
  - GP 名稱：Kerberos SPN 中包含非標準連接埠
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableAuthNegotiatePort
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableAuthNegotiatePort
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="ntlmv2enabled"></a>NtlmV2Enabled

  #### <a name="control-whether-ntlmv2-authentication-is-enabled"></a>控制是否要啟用 NTLMv2 驗證

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制是否已啟用 NTLMv2。

所有新版的 Samba 和 Windows 伺服器均支援 NTLMv2。 您僅應為了解決回溯相容性問題而停用 NTLMv2，因為這會降低驗證的安全性。

如果未設定此原則，則預設會啟用 NTLMv2。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NtlmV2Enabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="windowshelloforhttpauthenabled"></a>WindowsHelloForHTTPAuthEnabled

  #### <a name="windows-hello-for-http-auth-enabled"></a>適用於 HTTP 驗證的 Windows Hello 已啟用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  指出是否應該使用 Windows 認證 UI 來回應 NTLM 和交涉驗證挑戰。

如果您停用此原則，則會使用基本的使用者名稱和密碼提示來回應 NTLM 和交涉挑戰。 如果您啟用或未設定此原則，將會使用 Windows 認證 UI。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WindowsHelloForHTTPAuthEnabled
  - GP 名稱：適用於 HTTP 驗證的 Windows Hello 已啟用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/HTTP 驗證
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：WindowsHelloForHTTPAuthEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="kiosk-mode-settings-policies"></a>kiosk 模式設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="kioskaddressbareditingenabled"></a>KioskAddressBarEditingEnabled

  #### <a name="configure-address-bar-editing-for-kiosk-mode-public-browsing-experience"></a>針對 kiosk 模式公開瀏覽體驗設定網址列編輯

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  此原則僅在使用公開瀏覽體驗時，才適用 Microsoft Edge kiosk 模式。

如果您啟用或未設定此原則，使用者可以在網址列中變更 URL。

如果您停用這項原則，就會防止使用者變更網址列中的 URL。

如需有關設定 kiosk 模式的詳細資訊，請參閱[https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：KioskAddressBarEditingEnabled
  - GP 名稱：針對 kiosk 模式公開瀏覽體驗設定網址列編輯
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/kiosk 模式設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：KioskAddressBarEditingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：KioskAddressBarEditingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="kioskdeletedownloadsonexit"></a>KioskDeleteDownloadsOnExit

  #### <a name="delete-files-downloaded-as-part-of-kiosk-session-when-microsoft-edge-closes"></a>當 Microsoft Edge 關閉時，刪除隨著 Kiosk 工作階段下載的檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  此原則僅適用 Microsoft Edge kiosk 模式。

如果您啟用此原則，每次 Microsoft Edge 關閉時，會刪除隨著 Kiosk 工作階段下載的檔案。

如果您停用或未設定此原則，Microsoft Edge 關閉時，不會刪除隨著 Kiosk 工作階段下載的檔案。

如需有關設定 kiosk 模式的詳細資訊，請參閱[https://go.microsoft.com/fwlink/?linkid=2137578](https://go.microsoft.com/fwlink/?linkid=2137578)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：KioskDeleteDownloadsOnExit
  - GP 名稱：當 Microsoft Edge 關閉時，刪除隨著 Kiosk 工作階段下載的檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/kiosk 模式設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：KioskDeleteDownloadsOnExit
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="manageability-policies"></a>管理性原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="mamenabled"></a>MAMEnabled

  #### <a name="mobile-app-management-enabled"></a>已啟用行動裝置應用程式管理

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 瀏覽器從 Intune 應用程式管理服務中擷取原則，然後將它們套用至使用者的設定檔。

如果您啟用或不設定此原則，則可以套用行動裝置應用程式管理 (MAM) 原則。

如果您停用此原則，Microsoft Edge 將不會與 Intune 通訊以要求 MAM 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：MAMEnabled
  - GP 名稱：已啟用行動裝置應用程式管理
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/管理性
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：MAMEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：MAMEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="native-messaging-policies"></a>原生訊息原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="nativemessagingallowlist"></a>NativeMessagingAllowlist

  #### <a name="control-which-native-messaging-hosts-users-can-use"></a>控制使用者可以使用的原生訊息主機

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定原則會指定不受此拒絕清單所規範的原生訊息主機。 * 的拒絕清單值表示除非明確允許，否則所有原生訊息郵件主機都會遭到拒絕。

根據預設，允許所有原生訊息主機。 不過，如果原生訊息主機遭到原則拒絕，系統管理員可以使用允許清單來變更該原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NativeMessagingAllowlist
  - GP 名稱：控制使用者可以使用的原生訊息主機
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = "com.native.messaging.host.name2"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NativeMessagingAllowlist
  - 範例值：
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="nativemessagingblocklist"></a>NativeMessagingBlocklist

  #### <a name="configure-native-messaging-block-list"></a>設定原生訊息封鎖清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定此原則會指定不應載入的原生訊息主機。 * 的拒絕清單值表示除非明確允許，否則所有原生訊息郵件主機都會遭到拒絕。

如果您將此原則保留為未設定，Microsoft Edge 會載入所有已安裝的原生訊息主機。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NativeMessagingBlocklist
  - GP 名稱：設定原生訊息封鎖清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = "com.native.messaging.host.name1"
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = "com.native.messaging.host.name2"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NativeMessagingBlocklist
  - 範例值：
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="nativemessaginguserlevelhosts"></a>NativeMessagingUserLevelHosts

  #### <a name="allow-user-level-native-messaging-hosts-installed-without-admin-permissions"></a>允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如果您將此原則設為 [啟用] 或保留為未設定，Microsoft Edge 可以使用在使用者層級安裝的原生訊息主機。

如果您將此原則設為 [停用]，Microsoft Edge 只能使用在系統層級安裝的這些主機。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NativeMessagingUserLevelHosts
  - GP 名稱：允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NativeMessagingUserLevelHosts
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NativeMessagingUserLevelHosts
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="password-manager-and-protection-policies"></a>密碼管理員和保護原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordmanagerenabled"></a>PasswordManagerEnabled

  #### <a name="enable-saving-passwords-to-the-password-manager"></a>啟用將密碼儲存到密碼管理員

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓 Microsoft Edge 可儲存使用者密碼。

如果啟用此原則，則使用者可以將其密碼儲存在 Microsoft Edge 中。 使用者下次瀏覽網站時，Microsoft Edge 即會自動輸入密碼。

如果停用此原則，則使用者無法儲存新的密碼，但仍然可以使用先前儲存的密碼。

如果啟用或停用此原則，則使用者無法在 Microsoft Edge 中變更或覆寫它。 如果未設定，則使用者可以儲存密碼，並關閉此功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordManagerEnabled
  - GP 名稱：啟用將密碼儲存到密碼管理員
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/密碼管理員和防護
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PasswordManagerEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PasswordManagerEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordmonitorallowed"></a>PasswordMonitorAllowed

  #### <a name="allow-users-to-be-alerted-if-their-passwords-are-found-to-be-unsafe"></a>允許使用者在密碼不安全時收到警示提醒

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 監管使用者密碼。

如果您啟用此項原則，且提供使用者同意書啟用此原則，如果任何儲存在 Microsoft Edge 中的密碼出現不安全的情形，使用者會收到警示。 Microsoft Edge 會顯示警示訊息，而此資訊也可在 [設定] > [密碼] > [密碼監視器] 中取得。

如果您停用這項原則，啟用此功能與否可不須詢問使用者的同意。 使用者的密碼不會被掃瞄，使用者也不會收到警示訊息。

如果您啟用或未設定原則，使用者可以選擇將此功能開啟或關閉。

若要深入了解 Microsoft Edge 如何發現密碼不安全，請參閱 [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

其他指導方針：

您可以將此原則同時設為建議性使用和強制性使用，但必須使用重要標註。

強制性啟用：因個人使用者同意是為特定使用者啟用此功能的預先條件，所以此原則沒有強制執行的設定。 如果將此原則設定為 [強制性啟用]，則不須變更 [設定] 中的 UI，且下列的錯誤訊息會顯示在 edge://policy。

錯誤狀態訊息範例：「忽略此原則值是因為密碼監控器須有個人使用者的同意才能開啟。 您可以要求貴組織的使用者至設定 > 設定檔 > 密碼，然後開啟此功能。」

建議性啟用：假如將此原則設為建議性使用，在設定中的 UI 即會維持在 ‘關閉’ 的狀態．但在其旁邊會顯示一個公事包的圖示，在暫留懸停時會有以下說明顯示 -「您的組織建議使用此設定適用的特定值，而您選擇了一個不同的值」

已停用強制性使用和建議性使用：這兩種狀態都能正常運作，且使用者可以看到常用的標題。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordMonitorAllowed
  - GP 名稱：允許使用者在密碼不安全時收到警示提醒
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/密碼管理員和防護
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PasswordMonitorAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordprotectionchangepasswordurl"></a>PasswordProtectionChangePasswordURL

  #### <a name="configure-the-change-password-url"></a>設定變更密碼 URL

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定變更密碼 URL (僅限 HTTP 和 HTTPS 配置)。

在瀏覽器中看到警告之後，密碼保護服務會將使用者傳送到此 URL 以變更其密碼。

如果啟用此原則，則密碼保護服務會將使用者傳送到此 URL 來變更其密碼。

如果停用或未設定此原則，則密碼保護服務不會將使用者重新導向至變更密碼 URL。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordProtectionChangePasswordURL
  - GP 名稱：設定變更密碼 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PasswordProtectionChangePasswordURL
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://contoso.com/change_password.html"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PasswordProtectionChangePasswordURL
  - 範例值：
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordprotectionloginurls"></a>PasswordProtectionLoginURLs

  #### <a name="configure-the-list-of-enterprise-login-urls-where-the-password-protection-service-should-capture-salted-hashes-of-a-password"></a>設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定企業登入 URL 的清單 (僅限 HTTP 和 HTTPS 配置)，Microsoft Edge 應在其中擷取密碼的加料雜湊，並將它用於密碼重複使用偵測。

如果啟用此原則，則密碼保護服務會在定義的 URL 上擷取密碼的指紋。

如果停用或未設定此原則，則不會擷取密碼指紋。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordProtectionLoginURLs
  - GP 名稱：設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = "https://contoso.com/login.html"
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = "https://login.contoso.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PasswordProtectionLoginURLs
  - 範例值：
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordprotectionwarningtrigger"></a>PasswordProtectionWarningTrigger

  #### <a name="configure-password-protection-warning-trigger"></a>設定密碼保護警告觸發程序

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許您控制觸發密碼保護警告的時機。 當使用者在潛在可疑網站上重複使用受保護的密碼時，密碼保護會警示使用者。

您可以使用 [PasswordProtectionLoginURLs](#passwordprotectionloginurls) 和 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) 原則來設定要保護的密碼。

免除：[PasswordProtectionLoginURLs](#passwordprotectionloginurls) 和 [PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl) 中所列的網站的密碼，以及 [SmartScreenAllowListDomains](#smartscreenallowlistdomains) 中所列網站，將不會觸發密碼保護警告。

設定為 'PasswordProtectionWarningOff'，以不顯示密碼保護警告。

設定為 'PasswordProtectionWarningOnPasswordReuse'，以在使用者於非列為允許的網站上重複使用其受保護之密碼時，顯示密碼保護警告。

如果停用或未設定此原則，則不會顯示警告觸發。

原則選項對應：

* PasswordProtectionWarningOff (0) = 密碼保護警告已關閉

* PasswordProtectionWarningOnPasswordReuse (1) = 密碼保護警告會在重新使用密碼時觸發

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordProtectionWarningTrigger
  - GP 名稱：設定密碼保護警告觸發程序
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PasswordProtectionWarningTrigger
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PasswordProtectionWarningTrigger
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="passwordrevealenabled"></a>PasswordRevealEnabled

  #### <a name="enable-password-reveal-button"></a>啟用顯示密碼按鈕

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  可讓您針對網站上的密碼輸入欄位，設定瀏覽器顯示密碼按鈕的預設顯示。

如果您啟用或未設定此原則，瀏覽器使用者設定會預設顯示該顯示密碼按鈕。

如果您停用此原則，瀏覽器使用者設定將不會顯示該顯示密碼按鈕。

針對協助工具，使用者可以從預設原則變更瀏覽器設定。

此原則只會影響瀏覽器的顯示密碼按鈕，而不會影響網站的自訂顯示按鈕。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：否
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PasswordRevealEnabled
  - GP 名稱：啟用顯示密碼按鈕
  - GP 路徑 (強制)：不適用
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/密碼管理員和防護
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：不適用
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PasswordRevealEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PasswordRevealEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="performance-policies"></a>效能策略

  [回到頁首](#microsoft-edge---policies)

  ### <a name="startupboostenabled"></a>StartupBoostEnabled

  #### <a name="enable-startup-boost"></a>啟用啟動提升

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 處理程序在 OS 登入時啟動，並在最後一個瀏覽器視窗關閉後重新開機。

如果 Microsoft Edge 以背景模式執行，瀏覽器可能不會在最後一個視窗關閉時關閉，且在視窗關閉時，瀏覽器將無法在背景模式重新啟動。 如需設定 Microsoft Edge 背景模式行為之後所發生狀況的相關資訊，請參閱 [BackgroundModeEnabled](#backgroundmodeenabled) 原則。

如果您啟用這項原則，啟動提升功能就會開啟。

如果您啟用這項原則，啟動增強功能就會關閉。

如果您未設定此原則，啟動提升功能可能會先關閉或開啟。 使用者可以在 edge://settings/system 中設定其行為。

深入瞭解啟動提升功能： [https://go.microsoft.com/fwlink/?linkid=2147018](https://go.microsoft.com/fwlink/?linkid=2147018)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： StartupBoostEnabled
  - GP 名稱：啟用啟動提升功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/效能
  - GP 路徑 (建議使用)：系統管理範本/Microsoft Edge-預設設定 (使用者可以覆寫)/Performance
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 值名稱： StartupBoostEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="printing-policies"></a>列印原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultprinterselection"></a>DefaultPrinterSelection

  #### <a name="default-printer-selection-rules"></a>預設印表機選擇規則

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  覆寫 Microsoft Edge 預設印表機選擇規則。 此原則會決定用於在 Microsoft Edge 中選取預設印表機的規則，這會在使用者第一次嘗試列印頁面時發生。

設定此原則時，Microsoft Edge 會嘗試尋找符合所有指定屬性的印表機，並將它當成預設印表機。 如果有符合條件的多個印表機，則會使用符合的第一個印表機。

如果未設定此原則，或未在逾時內找到相符的印表機，印表機會預設為內建的 PDF 印表機，或無印表機 (如果沒有 PDF 印表機)。

值會剖析為 JSON 物件，符合下列架構：{ "type": "object", "properties": { "idPattern": { "description": "用來比對印表機識別碼的規則運算式。", "type": "string" }, "namePattern": { "description": "用來比對印表機顯示名稱的規則運算式。", "type": "string" } } }

省略某個欄位表示比對所有值；例如，如果您未指定連線，則預覽列印會開始探索各種本機印表機。 規則運算式模式必須遵循 JavaScript RegExp 語法，且比對會區分大小寫。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultPrinterSelection
  - GP 名稱：預設印表機選擇規則
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPrinterSelection
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"{ \"idPattern\": \".*public\", \"namePattern\": \".*Color\" }"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultPrinterSelection
  - 範例值：
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printheaderfooter"></a>PrintHeaderFooter

  #### <a name="print-headers-and-footers"></a>列印頁首與頁尾

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在列印對話方塊中，強制開啟或關閉 [頁首及頁尾]。

如果未設定此原則，則使用者可以決定是否要列印頁首和頁尾。

如果停用此原則，則使用者無法列印頁首及頁尾。

如果啟用此原則，則使用者一律會列印頁首及頁尾。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintHeaderFooter
  - GP 名稱：列印頁首及頁尾
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/列印
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PrintHeaderFooter
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintHeaderFooter
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printpreviewusesystemdefaultprinter"></a>PrintPreviewUseSystemDefaultPrinter

  #### <a name="set-the-system-default-printer-as-the-default-printer"></a>將系統預設的印表機設定為預設印表機

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  告知 Microsoft Edge 使用 [預覽列印] 中的預設印表機，而非最近使用的印表機。

如果停用或未設定此原則，則預覽列印會將最近使用的印表機視為預設的目的地選項。

如果啟用此原則，則預覽列印會使用 OS 的系統預設印表機做為預設目的地選擇。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintPreviewUseSystemDefaultPrinter
  - GP 名稱：將系統預設的印表機設定為預設印表機
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/列印
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PrintPreviewUseSystemDefaultPrinter
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintPreviewUseSystemDefaultPrinter
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printrasterizationmode"></a>PrintRasterizationMode

  #### <a name="print-rasterization-mode"></a>列印點陣化模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  控制 Microsoft Edge 在 Windows 上的列印方式。

在 Windows 上列印至非 PostScript 印表機時，有時候列印工作需要套用點陣化，以正確列印。

如果您將這個原則設定為 [完整] 或沒有設定，Microsoft Edge 會視需要執行整頁的點陣化設定。

如果您將這個原則設定為 [快速]，Microsoft Edge 將會減少點陣化的數量，這有助於減少列印工作大小並增加列印速度。

原則選項對應：

* 完整 (0) = 整頁點陣化

* 快速 (1) = 盡可能避免點陣化

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintRasterizationMode
  - GP 名稱：列印點陣化模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：PrintRasterizationMode
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printertypedenylist"></a>PrinterTypeDenyList

  #### <a name="disable-printer-types-on-the-deny-list"></a>停用拒絕清單上的印表機類型

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  拒絕清單上的印表機類型將無法被探索到，也無法取得其功能。

將所有印表機類型放置在拒絕清單上，可有效地停用列印，因為沒有文件的列印目的地。

如果您未設定此原則，或該印表機清單為空白，則所有印表機類型均可供探索。

印表機目的地包括印表機延伸和本機印表機。 延伸印表機也稱為列印提供者目的地，並包含屬於 Microsoft Edge 延伸的任何目的地。
本機印表機也稱為本機列印目的地，並包含可供本機電腦和共用網路印表機使用的目的地。

原則選項對應：

* privet (privet) = 以 Zeroconf 為基礎 (mDNS + DNS-SD) 的通訊協定目的地

* extension (延伸) = 以延伸為基礎的目的地

* pdf (pdf) =「另存為 PDF」目的地

* local (本機) = 本機印表機目的地

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrinterTypeDenyList
  - GP 名稱：停用拒絕清單上的印表機類型
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList\1 = "local"
SOFTWARE\Policies\Microsoft\Edge\PrinterTypeDenyList\2 = "privet"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrinterTypeDenyList
  - 範例值：
``` xml
<array>
  <string>local</string>
  <string>privet</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printingallowedbackgroundgraphicsmodes"></a>PrintingAllowedBackgroundGraphicsModes

  #### <a name="restrict-background-graphics-printing-mode"></a>限制背景圖形列印模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  限制背景圖形列印模式。 如果未設定此原則，則列印背景圖形沒有限制。

原則選項對應：

* any (任何) = 允許具有與不具有背景圖形的列印

* enabled (啟用) = 只允許具有背景圖形的列印

* disabled (停用) = 只允許不含背景圖形的列印

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintingAllowedBackgroundGraphicsModes
  - GP 名稱：限制背景圖形列印模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：PrintingAllowedBackgroundGraphicsModes
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"enabled"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintingAllowedBackgroundGraphicsModes
  - 範例值：
``` xml
<string>enabled</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printingbackgroundgraphicsdefault"></a>PrintingBackgroundGraphicsDefault

  #### <a name="default-background-graphics-printing-mode"></a>預設背景圖形列印模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  覆寫 [列印背景圖形] 的 [上次使用] 設定。
如果您啟用此設定，就會啟用背景圖形列印。
如果您停用此設定，就會停用背景圖形列印。

原則選項對應：

* enabled (啟用) = 預設啟用背景圖形列印模式

* disabled (停用) = 預設停用背景圖形列印模式

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintingBackgroundGraphicsDefault
  - GP 名稱：預設背景圖形列印模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：PrintingBackgroundGraphicsDefault
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"enabled"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintingBackgroundGraphicsDefault
  - 範例值：
``` xml
<string>enabled</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printingenabled"></a>PrintingEnabled

  #### <a name="enable-printing"></a>啟用列印

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 中啟用列印，並防止使用者變更此設定。

如果啟用此原則或未設定，則使用者可以列印。

如果停用此原則，則使用者無法從 Microsoft Edge 列印。 在扳手功能表、擴充功能、JavaScript 應用程式等項目中會停用列印。 使用者仍可以從列印時會略過 Microsoft Edge 的外掛程式進行列印。 例如，某些 Adobe Flash 應用程式的內容功能表中有列印選項，而此原則並未涵蓋它。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintingEnabled
  - GP 名稱：啟用列印
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PrintingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="printingpapersizedefault"></a>PrintingPaperSizeDefault

  #### <a name="default-printing-page-size"></a>預設列印頁面大小

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  覆寫預設列印頁面大小。

如果所需紙張大小不在清單中，名稱應包含列出的其中一種格式或 [自訂]。 如果提供了 [自訂] 值則需指定 custom_size 屬性。 它以微米為單位描述所需的高度和寬度。 否則請不要指定 custom_size 屬性。 違反這些規則的原則會被忽略。

如果使用者選擇的印表機無法列印此紙張尺寸，則忽略此原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PrintingPaperSizeDefault
  - GP 名稱：預設列印頁面大小
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：PrintingPaperSizeDefault
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {
  "custom_size": {
    "height": 297000,
    "width": 210000
  },
  "name": "custom"
}
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\PrintingPaperSizeDefault = {"custom_size": {"height": 297000, "width": 210000}, "name": "custom"}
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PrintingPaperSizeDefault
  - 範例值：
``` xml
<key>PrintingPaperSizeDefault</key>
<dict>
  <key>custom_size</key>
  <dict>
    <key>height</key>
    <integer>297000</integer>
    <key>width</key>
    <integer>210000</integer>
  </dict>
  <key>name</key>
  <string>custom</string>
</dict>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="usesystemprintdialog"></a>UseSystemPrintDialog

  #### <a name="print-using-system-print-dialog"></a>使用系統列印對話方塊列印

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  顯示系統列印對話方塊，而非預覽列印。

如果啟用此原則，當使用者列印頁面時，Microsoft Edge 會開啟系統的列印對話方塊，而非內建的預覽列印。

如果未設定或停用此原則，則列印命令會觸發 Microsoft Edge 預覽列印畫面。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：UseSystemPrintDialog
  - GP 名稱：使用系統列印對話方塊列印
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UseSystemPrintDialog
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：UseSystemPrintDialog
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="private-network-request-settings-policies"></a>私人網路要求設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="insecureprivatenetworkrequestsallowed"></a>InsecurePrivateNetworkRequestsAllowed

  #### <a name="specifies-whether-to-allow-insecure-websites-to-make-requests-to-more-private-network-endpoints"></a>指定是否允許不安全的網站對較私人的網路端點提出要求

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  控制是否允許不安全的網站對較私人的網路端點提出要求。

此原則與 CORS-RFC1918 規格相關。 如需詳細資訊，請參閱https://wicg.github.io/cors-rfc1918。

網路端點比另一個端點更加私人，如果：
1) 其 IP 位址為 localhost，而另一個不是。
2) 其 IP 位址為私人，而另一個為公用。
未來，根據規格演進，此原則可能會適用于所有以私人 IP 或 localhost 導向的跨來源要求。

如果網站符合 https://developer.mozilla.org/en-US/docs/Web/Security/Secure_Contexts 中安全內容的定義，即視為安全。 否則，它將被視為不安全的內容。

當此原則未設定或設定為 false 時，從不安全內容到更私人網路端點的要求預設行為將視使用者對 BlockInsecurePrivateNetworkRequests 功能的個人設定 (可能由現場試用或命令列設定) 所決定。

當此原則設定為 true 時，允許不安全的網站對任何網路端點提出要求，但須受其他跨來源檢查。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： InsecurePrivateNetworkRequestsAllowed
  - GP 名稱：指定是否允許不安全的網站對較私人的網路端點提出要求
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/私人網路要求設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： InsecurePrivateNetworkRequestsAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： InsecurePrivateNetworkRequestsAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="insecureprivatenetworkrequestsallowedforurls"></a>InsecurePrivateNetworkRequestsAllowedForUrls

  #### <a name="allow-the-listed-sites-to-make-requests-to-more-private-network-endpoints-from-insecure-contexts"></a>允許列出的網站從不安全的內容對較私人的網路端點提出要求

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  URL 模式清單。 允許從比對來源服務之不安全網站起始的私人網路要求。

如果未設定此原則，此原則的行為會像設定為空白清單一樣。

對於此處指定的模式未涵蓋的來源，全域預設值會使用 [InsecurePrivateNetworkRequestsAllowed](#insecureprivatenetworkrequestsallowed) 原則 (如果已設定)，否則則會使用使用者的個人設定。

請注意，此原則只會影響不安全的來源，因此將忽略安全來源 (例如，https://example.com) 清單中包含的不安全來源)。

如需有效 URL 模式的詳細資訊，請造訪 [此處](/DeployEdge/edge-learnmmore-url-list-filter%20format)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： InsecurePrivateNetworkRequestsAllowedForUrls
  - GP 名稱：允許列出的網站從不安全的內容對較私人的網路端點提出要求
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/私人網路要求設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\InsecurePrivateNetworkRequestsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\InsecurePrivateNetworkRequestsAllowedForUrls\1 = "http://www.example.com:8080"
SOFTWARE\Policies\Microsoft\Edge\InsecurePrivateNetworkRequestsAllowedForUrls\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： InsecurePrivateNetworkRequestsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>http://www.example.com:8080</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="proxy-server-policies"></a>Proxy 伺服器原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proxybypasslist"></a>ProxyBypassList

  #### <a name="configure-proxy-bypass-rules-deprecated"></a>設定 Proxy 略過原則 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  不建議使用此原則，請改用[ProxySettings](#proxysettings)。 無法在 Microsoft Edge 版本91中使用。

定義 Microsoft Edge 略過任何 Proxy 的主機清單。

只有在未指定 [ProxySettings](#proxysettings) 原則，且您已選取 [ProxyMode](#proxymode) 原則中的 fixed_servers 或 pac_script，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則可以建立 Microsoft Edge 不使用 Proxy 的主機清單。

如果未設定此原則，則不會為 Microsoft Edge 略過其 Proxy 的主機建立清單。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需更詳細的範例，請移至 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProxyBypassList
  - GP 名稱：設定 Proxy 略過規則 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProxyBypassList
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://www.contoso.com, https://www.fabrikam.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProxyBypassList
  - 範例值：
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proxymode"></a>ProxyMode

  #### <a name="configure-proxy-server-settings-deprecated"></a>設定 Proxy 伺服器設定 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  不建議使用此原則，請改用[ProxySettings](#proxysettings)。 無法在 Microsoft Edge 版本91中使用。

如果您將此原則設定為啟用，您可以指定 Microsoft Edge 所使用的 Proxy 伺服器，並防止使用者變更 Proxy 設定。 Microsoft Edge 會忽略從命令列指定的所有 Proxy 相關選項。 只有在未指定 [ProxySettings](#proxysettings) 原則的情況下，才能套用原則。

如果您選擇下列其中一個選項，系統就會忽略其他選項：
  * direct = 永遠都不要使用 Proxy 伺服器，且永遠都能直接連線
  * "system" = 使用系統 Proxy 設定
  * "auto_detect" = 自動偵測 Proxy 設定

如果您選擇使用：
  * fixed_servers = 固定的 proxy 伺服器。 您可以使用 [ProxyServer](#proxyserver) 和 [ProxyBypassList](#proxybypasslist)指定更多選項。
  * pac_script = A .pac proxy 腳本。 使用 [ProxyPacUrl](#proxypacurl) 將 URL 設定為 一個Proxy .pac 檔。

如需詳細範例，請移至 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

如果未設定此原則，則使用者可以選擇其自己的 Proxy 設定。

原則選項對應：

* ProxyDisabled (direct) = 永遠不使用 Proxy

* ProxyAutoDetect (auto_detect) = 自動偵測 Proxy 設定

* ProxyPacScript (pac_script) = 使用 .pac Proxy 指令碼

* ProxyFixedServers (fixed_servers) = 使用固定的 Proxy 伺服器

* ProxyUseSystem (system) = 使用系統 Proxy 設定

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProxyMode
  - GP 名稱：設定 Proxy 伺服器設定 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyMode
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"direct"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProxyMode
  - 範例值：
``` xml
<string>direct</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proxypacurl"></a>ProxyPacUrl

  #### <a name="set-the-proxy-pac-file-url-deprecated"></a>設定 Proxy .pac 檔案 URL (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  不建議使用此原則，請改用[ProxySettings](#proxysettings)。 無法在 Microsoft Edge 版本91中使用。

指定 Proxy auto-config (PAC) 檔案的 URL。

只有在未指定 [ProxySettings](#proxysettings) 原則，且您已選取 [ProxyMode](#proxymode) 原則中的 pac_script，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則可以為 PAC 檔案指定 URL，其定義瀏覽器如何自動選擇用於擷取特定網站的適當 Proxy 伺服器。

如果停用或未設定此原則，則不會指定任何 PAC 檔案。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需詳細範例，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProxyPacUrl
  - GP 名稱：設定 Proxy .pac 檔案 URL(不建議使用)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyPacUrl
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://internal.contoso.com/example.pac"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProxyPacUrl
  - 範例值：
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proxyserver"></a>ProxyServer

  #### <a name="configure-address-or-url-of-proxy-server-deprecated"></a>設定 Proxy 伺服器的位址或 URL (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  不建議使用此原則，請改用[ProxySettings](#proxysettings)。 無法在 Microsoft Edge 版本91中使用。

指定 Proxy 伺服器的 URL。

只有在未指定 [ProxySettings](#proxysettings) 原則，且您已選取 [ProxyMode](#proxymode) 原則中的 fixed_servers，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則將對所有 URL 使用此原則設定的 Proxy 伺服器。

如果停用或未設定此原則，則使用者可以在處於此 Proxy 模式時選擇其自己的 Proxy 設定。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需更多選項和詳細範例，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProxyServer
  - GP 名稱：設定 Proxy 伺服器的位址或 URL(不建議使用)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyServer
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"123.123.123.123:8080"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProxyServer
  - 範例值：
``` xml
<string>123.123.123.123:8080</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proxysettings"></a>ProxySettings

  #### <a name="proxy-settings"></a>Proxy 設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 的 Proxy 設定。

如果啟用此原則，則 Microsoft Edge 會忽略從命令列指定的所有 Proxy 相關選項。

如果未設定此原則，則使用者可以選擇其自己的 Proxy 設定。

此原則會覆寫下列個別原則：

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

設定 [ProxySettings](#proxysettings) 原則接受下欄位:
  * ProxyMode，可讓您指定 Microsoft Edge 所使用的 proxy 伺服器，並防止使用者變更 Proxy 設定
  * ProxyPacUrl、Proxy 的 URL .pac 檔案
  * ProxyServer、Proxy 伺服器的 URL
  * ProxyBypassList，Microsoft Edge 略過的 proxy 主機清單

如果您是 ProxyMode，請選擇下列值：
  * 直接使用，永遠不會使用proxy，而忽略其他所有欄位。
  * 系統, 使用的Proxy並忽略所有其他欄位。
  * auto_detect, 忽略其他所有欄位。
  * fixed_servers 中，會使用 ProxyServer 和 ProxyBypassList 欄位。
  * pac_script 中，會使用 ProxyPacUrl 和 ProxyBypassList 欄位。

如需更詳細的範例，請移至 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProxySettings
  - GP 名稱：Proxy 設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProxySettings
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/",
  "ProxyMode": "pac_script",
  "ProxyPacUrl": "https://internal.site/example.pac",
  "ProxyServer": "123.123.123.123:8080"
}
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {"ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", "ProxyMode": "pac_script", "ProxyPacUrl": "https://internal.site/example.pac", "ProxyServer": "123.123.123.123:8080"}
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProxySettings
  - 範例值：
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>pac_script</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="sleeping-tabs-settings-policies"></a>[睡眠] 索引標籤設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sleepingtabsblockedforurls"></a>SleepingTabsBlockedForUrls

  #### <a name="block-sleeping-tabs-on-specific-sites"></a>對特定網站封鎖睡眠索引標籤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  根據 URL 模式定義不允許進入睡眠狀態的網站清單 (睡眠) 索引標籤。

如果已停用 [SleepingTabsEnabled](#sleepingtabsenabled) 原則，則不會使用此清單，且不會自動將任何網站置於睡眠。

如果未設定此原則，除非使用者的個人設定加以封鎖，否則可以將所有網站置於睡眠。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SleepingTabsBlockedForUrls
  - GP 名稱：封鎖特定網站上的 [睡眠] 索引標籤
  - GP 路徑 (強制) ： [系統管理範本]/[Microsoft Edge/睡眠] 索引標籤設定
  - (建議) 的 GP 路徑： [系統管理範本/Microsoft Edge]-預設設定 (使用者可以覆寫 [) /Sleeping] 索引標籤設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended\SleepingTabsBlockedForUrls
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SleepingTabsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SleepingTabsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sleepingtabsenabled"></a>SleepingTabsEnabled

  #### <a name="configure-sleeping-tabs"></a>設定睡眠索引標籤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您設定是否要開啟 [睡眠] 索引標籤。 [睡眠] 索引標籤會將 [空閒背景] 索引標籤置於睡眠中，以減少 CPU、電池和記憶體使用量。 Microsoft Edge 使用啟發學習法來避免將在背景中執行實用工作 (例如：顯示通知、播放音效和串流視訊) 的索引標籤置於睡眠。 預設會開啟 [睡眠] 索引標籤。

您可以設定原則 [SleepingTabsBlockedForUrls](#sleepingtabsblockedforurls)，以防止將個別網站置於睡眠。

如果您啟用此設定，就會開啟 [睡眠] 索引標籤。

如果您停用此設定，[睡眠] 索引標籤就會關閉。

如果您未設定此設定，使用者可以選擇是否要使用 [睡眠] 索引標籤。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SleepingTabsEnabled
  - GP 名稱：設定睡眠索引標籤
  - GP 路徑 (強制) ： [系統管理範本]/[Microsoft Edge/睡眠] 索引標籤設定
  - (建議) 的 GP 路徑： [系統管理範本/Microsoft Edge]-預設設定 (使用者可以覆寫 [) /Sleeping] 索引標籤設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SleepingTabsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SleepingTabsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sleepingtabstimeout"></a>SleepingTabsTimeout

  #### <a name="set-the-background-tab-inactivity-timeout-for-sleeping-tabs"></a>設定睡眠索引標籤的背景索引標籤無活動逾時

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您設定超時 (以秒為單位)，在啟用 [睡眠] 索引標籤之後，不活躍的背景索引標籤會自動進入睡眠狀態。 根據預設，此逾時為 7,200 秒 (2 小時)。

只有在啟用原則 [SleepingTabsEnabled](#sleepingtabsenabled) 或沒有設定，且使用者已啟用 [睡眠] 索引標籤設定時，才會將索引標籤自動置於 [睡眠] 中。

如果未設定此原則，則使用者可以選擇逾時值。

原則選項對應：

* 5Minutes (300) = 無活動 5 分鐘

* 15Minutes (900) = 無活動 15 分鐘

* 30Minutes (1800) = 無活動 30 分鐘

* 1Hour (3600) = 無活動 1 小時

* 2Hours (7200) = 無活動 2 小時

* 3Hours (10800) = 無活動 3 小時

* 6Hours (21600) = 無活動 6 小時

* 12Hours (43200) = 無活動 12 小時

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SleepingTabsTimeout
  - GP 名稱：設定 [睡眠] 索引標籤的 [背景] 索引標籤閒置超時
  - GP 路徑 (強制) ： [系統管理範本]/[Microsoft Edge/睡眠] 索引標籤設定
  - (建議) 的 GP 路徑： [系統管理範本/Microsoft Edge]-預設設定 (使用者可以覆寫 [) /Sleeping] 索引標籤設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SleepingTabsTimeout
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000384
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SleepingTabsTimeout
  - 範例值：
``` xml
<integer>900</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="smartscreen-settings-policies"></a>SmartScreen 設定原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="preventsmartscreenpromptoverride"></a>PreventSmartScreenPromptOverride

  #### <a name="prevent-bypassing-microsoft-defender-smartscreen-prompts-for-sites"></a>防止略過網站的 Microsoft Defender SmartScreen 提示

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您決定使用者是否可覆寫有關潛在惡意網站的 Microsoft Defender SmartScreen 警告。

如果啟用此設定，使用者就不能忽略 Microsoft Defender SmartScreen 警告，並且會封鎖使用者，使其無法繼續瀏覽網站。

如果停用或未設定此設定，則使用者可以忽略 Microsoft Defender SmartScreen 警告，並繼續瀏覽網站。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PreventSmartScreenPromptOverride
  - GP 名稱：防止略過網站的 Microsoft Defender SmartScreen 提示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PreventSmartScreenPromptOverride
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PreventSmartScreenPromptOverride
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="preventsmartscreenpromptoverrideforfiles"></a>PreventSmartScreenPromptOverrideForFiles

  #### <a name="prevent-bypassing-of-microsoft-defender-smartscreen-warnings-about-downloads"></a>防止略過關於下載項目的 Microsoft Defender SmartScreen 警告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本
  - macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  此原則可讓您判斷使用者是否可以覆寫關於未經驗證下載的 Microsoft Defender SmartScreen 警告。

如果啟用此原則，則組織中的使用者無法忽略 Microsoft Defender SmartScreen 警告，且會防止其完成未經驗證的下載。

如果停用或未設定此原則，則使用者可以忽略 Microsoft Defender SmartScreen 警告，並完成未驗證的下載。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PreventSmartScreenPromptOverrideForFiles
  - GP 名稱：防止略過關於下載項目的 Microsoft Defender SmartScreen 警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PreventSmartScreenPromptOverrideForFiles
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PreventSmartScreenPromptOverrideForFiles
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="smartscreenallowlistdomains"></a>SmartScreenAllowListDomains

  #### <a name="configure-the-list-of-domains-for-which-microsoft-defender-smartscreen-wont-trigger-warnings"></a>設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Defender SmartScreen 的信任網域清單。 這表示，如果來源 URL 符合這些網域，則 Microsoft Defender SmartScreen 不會檢查是否有潛在的惡意資源，例如網路釣魚軟體和其他惡意程式碼。
Microsoft Defender SmartScreen 下載保護服務不會檢查在這些網域上託管的下載。

如果啟用此原則，則 Microsoft Defender SmartScreen 會信任這些網域。
如果停用或未設定此原則，則會將預設的 Microsoft Defender SmartScreen 防護套用到所有資源。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。
另請注意，如果組織已啟用 Microsoft Defender 進階威脅防護，則此原則不適用。 您必須改為在 Microsoft Defender 資訊安全中心設定允許和封鎖清單。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SmartScreenAllowListDomains
  - GP 名稱：設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = "myuniversity.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SmartScreenAllowListDomains
  - 範例值：
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="smartscreenenabled"></a>SmartScreenEnabled

  #### <a name="configure-microsoft-defender-smartscreen"></a>設定 Microsoft Defender SmartScreen

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您設定是否要開啟 Microsoft Defender SmartScreen。 Microsoft Defender SmartScreen 提供警告訊息，以協助保護使用者免於遭受潛在網路釣魚詐騙和惡意軟體。 預設會開啟 Microsoft Defender SmartScreen。

如果啟用此設定，則會開啟 Microsoft Defender SmartScreen。

如果停用此設定，則會關閉 Microsoft Defender SmartScreen。

如果未設定此設定，則使用者可以選擇是否要使用 Microsoft Defender SmartScreen。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SmartScreenEnabled
  - GP 名稱：設定 Microsoft Defender SmartScreen
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SmartScreenEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="smartscreenfortrusteddownloadsenabled"></a>SmartScreenForTrustedDownloadsEnabled

  #### <a name="force-microsoft-defender-smartscreen-checks-on-downloads-from-trusted-sources"></a>強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您設定 Microsoft Defender SmartScreen 是否檢查來自信任來源的下載信譽。

如果您啟用或未設定此設定，無論來源為何，Microsoft Defender SmartScreen 都會檢查下載項目的信譽。

如果您停用此設定，Microsoft Defender SmartScreen 不會檢查從信任來源下載項目的信譽。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SmartScreenForTrustedDownloadsEnabled
  - GP 名稱：強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenForTrustedDownloadsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="smartscreenpuaenabled"></a>SmartScreenPuaEnabled

  #### <a name="configure-microsoft-defender-smartscreen-to-block-potentially-unwanted-apps"></a>設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  此原則設定可讓您設定是否要開啟封鎖潛在的垃圾應用程式以搭配 Microsoft Defender SmartScreen。 潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen 可提供警告訊息，以協助保護使用者不受廣告軟體、挖礦程式、置入軟體和其他由網站託管的低信譽應用程式。 預設會關閉潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果啟用此設定，則會開啟潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果停用此設定，則會關閉潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果未設定此設定，則使用者可以選擇是否要使用潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SmartScreenPuaEnabled
  - GP 名稱：設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenPuaEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SmartScreenPuaEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="startupcomma-home-page-and-new-tab-page-policies"></a>啟動、首頁和新的索引標籤頁面原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="homepageisnewtabpage"></a>HomepageIsNewTabPage

  #### <a name="set-the-new-tab-page-as-the-home-page"></a>將新的索引標籤頁面設定為 [首頁]

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 中的預設首頁。 您可以將首頁設定為您指定的 URL 或新的索引標籤頁面。

如果啟用此原則，則一律對首頁使用新的索引標籤頁面，且會忽略首頁 URL 位置。

如果停用此原則，除非 URL 設為 'edge://newtab'，否則使用者的首頁不會成為新的索引標籤頁面。

如果未設定，則使用者可以選擇新的索引標籤頁面是否為其首頁。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HomepageIsNewTabPage
  - GP 名稱：將新的索引標籤頁面設定為 [首頁]
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：HomepageIsNewTabPage
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HomepageIsNewTabPage
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="homepagelocation"></a>HomepageLocation

  #### <a name="configure-the-home-page-url"></a>設定首頁 URL

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 中的預設首頁 URL。

首頁是由 [首頁] 按鈕所開啟的頁面。 啟動時開啟的頁面是由 [RestoreOnStartup](#restoreonstartup) 原則所控制。

您可以在此設定 URL，或將首頁設定為開啟新的索引標籤頁面。 如果選擇開啟新的索引標籤頁面，則此原則不會有作用。

如果啟用此原則，則使用者無法變更其首頁 URL，但可以選擇使用新的索引標籤頁面做為首頁。

如果停用或未設定此原則，則使用者可以自行選擇其首頁，只要 [HomepageIsNewTabPage](#homepageisnewtabpage) 原則未啟用即可。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HomepageLocation
  - GP 名稱：設定首頁 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：HomepageLocation
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://www.contoso.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HomepageLocation
  - 範例值：
``` xml
<string>https://www.contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpageallowedbackgroundtypes"></a>NewTabPageAllowedBackgroundTypes

  #### <a name="configure-the-background-types-allowed-for-the-new-tab-page-layout"></a>設定新索引標籤頁面版面配置所允許的背景類型

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  您可以在 Microsoft Edge 中設定新索引標籤頁面版面配置所允許的背景影像類型。

如果您未設定此原則，則會啟用新索引標籤頁面上的所有背景影像類型。

原則選項對應：

* DisableImageOfTheDay (1) = 停用每日背景影像類型

* DisableCustomImage (2) = 停用自訂背景影像類型

* DisableAll (3) = 停用所有背景影像類型

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageAllowedBackgroundTypes
  - GP 名稱：設定新索引標籤頁面配置所允許的背景類型
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：NewTabPageAllowedBackgroundTypes
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageAllowedBackgroundTypes
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagecompanylogo"></a>NewTabPageCompanyLogo

  #### <a name="set-new-tab-page-company-logo-obsolete"></a>設定新的索引標籤頁面公司標誌 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 85 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - 在 Windows 和 macOS 上，版本 79 到 85

  #### <a name="description"></a>描述

  由於操作要求的變更，此原則無法按預期運作。 囙此，它已過時，不應再使用。

指定要在 Microsoft Edge 中新的索引標籤頁面上使用的公司標誌。

原則應設定為字串，以 JSON 格式表示標誌。 例如：{ "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

您可以設定此原則，方法是指定 Microsoft Edge 可以從中下載標誌的 URL，以及其加密雜湊 (SHA-256)，用來驗證下載的完整性。 標誌必須是 PNG 或 SVG 格式，且其檔案大小不能超過 16 MB。 標誌會下載並快取，每當 URL 或雜湊變更，就會重新下載標誌。 該 URL 必須未經任何驗證便可存取。

需要 'default_logo'，且它將在沒有背景影像時使用。 如果提供了 'light_logo'，則會在使用者新的索引標籤頁面有背景影像時使用。 建議使用具有透明背景的水平標誌 (靠左對齊和垂直置中)。 標誌的最小高度應為 32 像素，而長寬比從 1:1 到4:1。 'default_logo' 應對照白色/黑色背景使用適當的對比，而 'light_logo' 應對照背景影像有適當的對比。

如果啟用此原則，則 Microsoft Edge 會下載並在新的索引標籤頁面上顯示指定的標誌。 使用者無法覆寫或隱藏標誌。

如果停用或未設定此原則，則 Microsoft Edge 不會在新的索引標籤頁面上顯示公司標誌或 Microsoft 標誌。

如需判斷 SHA-256 雜湊的協助，請參閱 ./powershell/module/microsoft.powershell.utility/get-filehash。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageCompanyLogo
  - GP 名稱：設定新的索引標籤頁面公司標誌 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NewTabPageCompanyLogo
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {
  "default_logo": {
    "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29",
    "url": "https://www.contoso.com/logo.png"
  },
  "light_logo": {
    "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737",
    "url": "https://www.contoso.com/light_logo.png"
  }
}
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageCompanyLogo = {"default_logo": {"hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29", "url": "https://www.contoso.com/logo.png"}, "light_logo": {"hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737", "url": "https://www.contoso.com/light_logo.png"}}
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageCompanyLogo
  - 範例值：
``` xml
<key>NewTabPageCompanyLogo</key>
<dict>
  <key>default_logo</key>
  <dict>
    <key>hash</key>
    <string>cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29</string>
    <key>url</key>
    <string>https://www.contoso.com/logo.png</string>
  </dict>
  <key>light_logo</key>
  <dict>
    <key>hash</key>
    <string>517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737</string>
    <key>url</key>
    <string>https://www.contoso.com/light_logo.png</string>
  </dict>
</dict>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagecontentenabled"></a>NewTabPageContentEnabled

  #### <a name="allow-microsoft-news-content-on-the-new-tab-page"></a>允許新分頁頁面上的 Microsoft 新聞內容

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 91 或更新版本

  #### <a name="description"></a>描述

  如果您啟用或沒有設定此原則，Microsoft Edge 會在新的分頁頁面上顯示 Microsoft 新聞內容。 使用者可以為內容選擇不同的顯示選項，包括但不限於關閉內容、捲動時顯示內容、僅顯示標題，以及顯示的內容。 啟用此原則不會強制顯示內容 - 使用者可以繼續設定自己的偏好內容位置。

如果您停用此原則，Microsoft Edge 不會在新的分頁頁面上顯示 Microsoft 新聞內容，NTP 設定飛出視窗的內容控制項會停用並設定為 [關閉內容]。

此原則僅適用於 Microsoft Edge 的本機使用者設定檔、使用 Microsoft 帳戶所簽署的設定檔，以及使用 Active Directory 簽署的設定檔。 若要為使用 Azure Active Directory 的設定檔設定企業新索引標籤頁面，請使用 M365 系統管理入口網站。

相關的原則：[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)，[NewTabPageQuickLinksEnabled](#newtabpagequicklinksenabled)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageContentEnabled
  - GP 名稱：允許新分頁頁面上的 Microsoft 新聞內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NewTabPageContentEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageContentEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagehidedefaulttopsites"></a>NewTabPageHideDefaultTopSites

  #### <a name="hide-the-default-top-sites-from-the-new-tab-page"></a>從新的索引標籤頁面隱藏預設熱門網站

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 中從新的索引標籤頁面隱藏預設熱門網站。

如果您將此原則設定為 true，則會隱藏預設的熱門網站磚。

如果將此原則設定為 false 或未設定，則預設的熱門網站磚會保持顯示。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageHideDefaultTopSites
  - GP 名稱：從新的索引標籤頁面隱藏預設熱門網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NewTabPageHideDefaultTopSites
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageHideDefaultTopSites
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagelocation"></a>NewTabPageLocation

  #### <a name="configure-the-new-tab-page-url"></a>設定新的索引標籤頁面 URL

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定新索引標籤頁面的預設 URL。

此原則建議使用的版本目前的執行和運作，未完全符合強制的版本。

此原則會決定建立新的索引標籤時 (包括開啟新視窗時) 開啟的頁面。 如果啟動頁面已設為開啟新的索引標籤頁面，則也會影響它。

此原則不會判定在啟動時要開啟的頁面；這是由 [RestoreOnStartup](#restoreonstartup) 原則控制。 如果啟動頁面已設為開啟至新的索引標籤，則不會對首頁造成任何影響。

如果未設定此原則，則會使用預設的新的索引標籤頁面。

如果您設定此原則*以及* [NewTabPageSetFeedType](#newtabpagesetfeedtype) 原則，則此原則優先。

如果您慣用的是空白索引標籤，則 "about:blank" 是應使用的正確 URL，而非 "about://blank"。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageLocation
  - GP 名稱：設定新的索引標籤頁面 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageLocation
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://www.fabrikam.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageLocation
  - 範例值：
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagemanagedquicklinks"></a>NewTabPageManagedQuickLinks

  #### <a name="set-new-tab-page-quick-links"></a>設定新的索引標籤頁面快速連結

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  依預設，Microsoft Edge 會根據瀏覽歷程記錄，在新的索引標籤頁面上顯示來自使用者新增的捷徑和熱門網站的快速連結。 使用此原則，您可以在新的索引標籤頁面上設定最多三個快速連結磚，並以 JSON 物件表示：

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

'url' 欄位為必要欄位。'title' 和 'pinned' 為選用。 如果未提供 'title'，則會將 URL 用作預設標題。 如果未提供 'pinned'，則預設值為 false。

Microsoft Edge 會以所列的順序呈現這些項目 (由左至右)，且所有釘選的磚都會顯示在未釘選的磚前方。

如果原則設定為強制，則會忽略 'pinned' 欄位，並將所有磚釘選。 使用者無法刪除磚，且一律會出現在快速連結清單的前面。

如果原則設定為建議，則釘選的磚會保留在清單中，但使用者可以編輯和刪除它們。 未釘選的快速連結磚的行為就如同預設的熱門網站，如果其他網站的造訪頻率較高，則會將該連結推出清單之外。 透過此原則將未釘選的連結套用至現有的瀏覽器設定檔時，連結可能完全不會顯示，取決於它們相較於使用者的瀏覽歷程記錄的排名。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageManagedQuickLinks
  - GP 名稱：設定新的索引標籤頁面快速連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageManagedQuickLinks
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [
  {
    "pinned": true,
    "title": "Contoso Portal",
    "url": "https://contoso.com"
  },
  {
    "title": "Fabrikam",
    "url": "https://fabrikam.com"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\NewTabPageManagedQuickLinks = [{"pinned": true, "title": "Contoso Portal", "url": "https://contoso.com"}, {"title": "Fabrikam", "url": "https://fabrikam.com"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageManagedQuickLinks
  - 範例值：
``` xml
<key>NewTabPageManagedQuickLinks</key>
<array>
  <dict>
    <key>pinned</key>
    <true/>
    <key>title</key>
    <string>Contoso Portal</string>
    <key>url</key>
    <string>https://contoso.com</string>
  </dict>
  <dict>
    <key>title</key>
    <string>Fabrikam</string>
    <key>url</key>
    <string>https://fabrikam.com</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpageprerenderenabled"></a>NewTabPagePrerenderEnabled

  #### <a name="enable-preload-of-the-new-tab-page-for-faster-rendering"></a>啟用預先載入的新索引標籤頁面，以加快頁面呈現速度

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  若您設定此原則，將會啟用 [預先載入新增索引標籤頁面] 功能，且使用者無法變更此設定。 若您未設定此原則，將會啟用預先載入功能，且使用者可以變更此設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPagePrerenderEnabled
  - GP 名稱：啟用預先載入的新索引標籤頁面，以加快頁面呈現速度
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPagePrerenderEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPagePrerenderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagequicklinksenabled"></a>NewTabPageQuickLinksEnabled

  #### <a name="allow-quick-links-on-the-new-tab-page"></a>允許新分頁頁面上的快速連結

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 91 或更新版本

  #### <a name="description"></a>描述

  如果您啟用或沒有設定此原則，Microsoft Edge 會在新的索引標籤頁面上顯示快速連結，而且使用者可以與控制項互動，並開啟和關閉快速連結。 啟用此原則不會強制顯示快速連結 - 使用者可以繼續開啟和關閉快速連結。

如果您停用此原則，Microsoft Edge 會隱藏新分頁頁面上的快速連結，並停用 NTP 設定飛出視窗的快速連結控制項。

此原則僅適用於 Microsoft Edge 的本機使用者設定檔、使用 Microsoft 帳戶所簽署的設定檔，以及使用 Active Directory 簽署的設定檔。 若要為使用 Azure Active Directory 的設定檔設定企業新索引標籤頁面，請使用 M365 系統管理入口網站。

相關的原則：[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)，[NewTabPageContentEnabled](#newtabpagecontentenabled)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageQuickLinksEnabled
  - GP 名稱：允許新分頁頁面上的快速連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：NewTabPageQuickLinksEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定金鑰名稱：NewTabPageQuickLinksEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="newtabpagesetfeedtype"></a>NewTabPageSetFeedType

  #### <a name="configure-the-microsoft-edge-new-tab-page-experience-obsolete"></a>設定 Microsoft Edge 新的索引標籤頁面體驗 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 92 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 至 92

  #### <a name="description"></a>說明

  此原則已過時，因為新版的企業新索引標籤頁面不再需要選擇不同的內容類型。 而是可透過 Microsoft 365 系統管理中心控制向使用者顯示的內容。 若要前往 Microsoft 365 系統管理中心，請使用您的系統管理員帳戶登入 https://admin.microsoft.com。

讓您為新的索引標籤頁面選擇 Microsoft News 或 Office 365 摘要體驗。

將此原則設定為 ‘新聞’ 時，使用者會在新的索引標籤頁面上看到 Microsoft 新聞摘要體驗。

將此原則設定為 ‘Office’ 時，以 Azure Active Directory 登入瀏覽器的使用者會在新的索引標籤頁面上看到 Office 365 摘要體驗。

如果停用或未設定此原則：

- 具有 Azure Active Directory 瀏覽器登入的使用者，會獲得 Office 365 新的索引標籤頁面摘要體驗，以及標準的新的索引標籤頁面摘要體驗。

- 沒有 Azure Active Directory 瀏覽器登入的使用者將會看到標準的新的索引標籤頁面體驗。

如果您設定此原則*以及* [NewTabPageLocation](#newtabpagelocation) 原則，則 [NewTabPageLocation](#newtabpagelocation) 優先。

預設設定：已停用或未設定。

原則選項對應：

* 新聞 (0) = Microsoft 新聞摘要體驗

* Office (1) = Office 365 摘要體驗

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NewTabPageSetFeedType
  - GP 名稱：設定 Microsoft Edge 新的索引標籤頁面體驗 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageSetFeedType
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NewTabPageSetFeedType
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="restoreonstartup"></a>RestoreOnStartup

  #### <a name="action-to-take-on-startup"></a>啟動時所採取的動作

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定 Microsoft Edge 啟動時的行為。

如果想要在啟動時一律開啟新索引標籤，請選擇 'RestoreOnStartupIsNewTabPage'。

如果想要重新開啟上次 Microsoft Edge 關閉時所開啟的 URL，請選擇 'RestoreOnStartupIsLastSession'。 瀏覽工作階段將會如實還原。 請注意，此選項會停用某些依賴於工作階段或在結束時執行動作的設定 (例如，在結束時清除瀏覽資料或僅限工作階段的 Cookie)。

如果想要開啟一組特定的 URL，請選擇 'RestoreOnStartupIsURLs'。

停用此設定相當於將它保持未設定。 使用者將能夠在 Microsoft Edge 中變更它。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

原則選項對應：

* RestoreOnStartupIsNewTabPage (5) = 開啟新的索引標籤

* RestoreOnStartupIsLastSession (1) = 還原上一個工作階段

* RestoreOnStartupIsURLs (4) = 開啟 URL 清單

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RestoreOnStartup
  - GP 名稱：啟動時所採取的動作
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：RestoreOnStartup
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000004
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RestoreOnStartup
  - 範例值：
``` xml
<integer>4</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="restoreonstartupurls"></a>RestoreOnStartupURLs

  #### <a name="sites-to-open-when-the-browser-starts"></a>瀏覽器啟動時開啟的網站

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定瀏覽器啟動時自動開啟的網站清單。 如果未設定此原則，則啟動時不會開啟任何網站。

只有當您將 [RestoreOnStartup](#restoreonstartup) 原則設定為 [開啟 URL 清單] (4)時，此原則才有效。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RestoreOnStartupURLs
  - GP 名稱：瀏覽器啟動時開啟的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = "https://contoso.com"
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = "https://www.fabrikam.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RestoreOnStartupURLs
  - 範例值：
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="showhomebutton"></a>ShowHomeButton

  #### <a name="show-home-button-on-toolbar"></a>在工具列上顯示 [首頁] 按鈕

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 工具列上顯示 [首頁] 按鈕。

啟用此原則以一律顯示 [首頁] 按鈕。 停用它以一律不顯示該按鈕。

如果未設定原則，則使用者可以選擇是否要顯示首頁按鈕。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ShowHomeButton
  - GP 名稱：在工具列上顯示 [首頁] 按鈕
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ShowHomeButton
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ShowHomeButton
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## <a name="additional-policies"></a>其他原則

  [回到頁首](#microsoft-edge---policies)

  ### <a name="aadwebsitessousingthisprofileenabled"></a>AADWebSiteSSOUsingThisProfileEnabled

  #### <a name="single-sign-on-for-work-or-school-sites-using-this-profile-enabled"></a>已啟用使用此設定檔的工作或學校網站單一登入

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  '允許在工作或學校網站使用此設定檔的單一登入' 選項可讓非 AAD 設定檔使用電腦上存在的工作或學校認證，對工作或學校網站使用單一登入。 此選項在設定 -> 設定檔 ->非 AAD 設定檔的設定檔喜好設定中會顯示為切換開關。

如果停用此原則，非 AAD 設定檔將無法使用電腦上存在的其他認證來使用 SSO。 這也將確保已關閉單一非 Azure AD Microsoft Edge 設定檔使用者的所有 Windows Azure Active Directory (Azure AD) 帳戶智慧型啟用單一登入 (SSO)。

如果您啟用或不設定原則，非 AAD 設定檔將可以使用電腦上存在的其他認證來使用 SSO，而具有單一非 Azure AD Microsoft Edge 設定檔之使用者的所有 Windows Azure Active Directory (Azure AD) 帳戶的智慧型啟用單一登入 (SSO) 將繼續運作。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AADWebSiteSSOUsingThisProfileEnabled
  - GP 名稱：已啟用使用此設定檔的工作或學校網站單一登入
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AADWebSiteSSOUsingThisProfileEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AADWebSiteSSOUsingThisProfileEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="addressbarmicrosoftsearchinbingproviderenabled"></a>AddressBarMicrosoftSearchInBingProviderEnabled

  #### <a name="enable-microsoft-search-in-bing-suggestions-in-the-address-bar"></a>在網址列中啟用 Bing 專用 Microsoft Search 建議

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  讓您在使用者在網址列中輸入搜尋字串時，於網址列的建議清單中顯示相關的 Bing 專用 Microsoft Search 建議。 如果啟用或未設定此原則，則使用者可以在 Microsoft Edge 網址列建議清單中看到 Bing 專用 Microsoft Search 提供的內部結果。 若要查看 Bing 專用 Microsoft Search 結果，使用者必須使用其用於該組織的 Azure AD 帳戶登入 Microsoft Edge。
如果停用此原則，則使用者無法在 Microsoft Edge 網址列建議清單中查看內部結果。
從 Microsoft Edge 版本 89 開始，即使 Bing 不是使用者的預設搜尋提供者，仍可使用 Bing 中的 [Microsoft 搜尋] 建議。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - GP 名稱：在網址列中啟用 Bing 專用 Microsoft Search 建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="adssettingforintrusiveadssites"></a>AdsSettingForIntrusiveAdsSites

  #### <a name="ads-setting-for-sites-with-intrusive-ads"></a>含有干擾廣告網站的廣告設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  控制是否在含有干擾廣告的網站上封鎖廣告。

原則選項對應：

* AllowAds (1) = 在所有網站上允許廣告。

* BlockAds (2) = 在含有侵入式廣告的網站上封鎖廣告。 (預設值)

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AdsSettingForIntrusiveAdsSites
  - GP 名稱：含有干擾廣告網站的廣告設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AdsSettingForIntrusiveAdsSites
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AdsSettingForIntrusiveAdsSites
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowdeletingbrowserhistory"></a>AllowDeletingBrowserHistory

  #### <a name="enable-deleting-browser-and-download-history"></a>啟用刪除瀏覽器和下載歷程記錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許刪除瀏覽器歷程記錄和下載歷程記錄，並防止使用者變更此設定。

請注意，即使停用此原則，瀏覽和下載歷程記錄也不保證會保留：使用者可以直接編輯或刪除記錄資料庫檔案，而瀏覽器本身可以隨時移除 (根據到期期間) 或封存任何或所有歷程記錄項目。

如果啟用此原則或未設定，則使用者可以刪除瀏覽和下載歷程記錄。

如果停用此原則，則使用者無法刪除瀏覽和下載歷程記錄。 停用此原則會停用歷程記錄同步，並開啟索引標籤同步。

如果啟用此原則，則請勿啟用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則，因為它們全都涉及刪除資料。 如果您同時啟用這兩項，則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則優先，並且會在 Microsoft Edge 關閉時刪除所有資料，無論此原則的設定方式如何。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowDeletingBrowserHistory
  - GP 名稱：啟用刪除瀏覽器和下載歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowDeletingBrowserHistory
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowDeletingBrowserHistory
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowfileselectiondialogs"></a>AllowFileSelectionDialogs

  #### <a name="allow-file-selection-dialogs"></a>允許檔案選取項目對話方塊

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓 Microsoft Edge 顯示檔案選取對話方塊，允許存取本機檔案。

如果啟用或未設定此原則，則使用者可以正常開啟檔案選取對話方塊。

如果停用此原則，每當使用者執行會觸發檔案選取對話方塊的動作 (例如匯入我的最愛、上傳檔案或儲存連結)，即會改為顯示訊息，並假設使用者已在 [檔案選取] 對話方塊中按一下 [取消]。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowFileSelectionDialogs
  - GP 名稱：允許檔案選取項目對話方塊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowFileSelectionDialogs
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowFileSelectionDialogs
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowpopupsduringpageunload"></a>AllowPopupsDuringPageUnload

  #### <a name="allows-a-page-to-show-popups-during-its-unloading-obsolete"></a>允許在卸載網頁期間顯示快顯視窗 (已淘汰)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 87 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 至 87

  #### <a name="description"></a>描述

  此原則可讓系統管理員指定網頁可在其卸載期間顯示快顯視窗。

原則設定為已啟用時，則允許在卸載網頁期間顯示快顯視窗。

原則設為已停用或未設定時，則不允許在卸載網頁期間顯示快顯視窗。 這是基於此處的規格：(https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name)。

此原則已從 Microsoft Edge 88 中移除，如果設定，則會被忽略。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowPopupsDuringPageUnload
  - GP 名稱：允許在卸載網頁期間顯示快顯視窗 (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowPopupsDuringPageUnload
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowPopupsDuringPageUnload
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowsurfgame"></a>AllowSurfGame

  #### <a name="allow-surf-game"></a>允許衝浪遊戲

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  如果停用此原則，當裝置離線或使用者瀏覽至 edge://surf 時，使用者將無法玩衝浪遊戲。

如果啟用或未設定此原則，則使用者可以玩衝浪遊戲。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowSurfGame
  - GP 名稱：允許衝浪遊戲
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowSurfGame
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowSurfGame
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowsyncxhrinpagedismissal"></a>AllowSyncXHRInPageDismissal

  #### <a name="allow-pages-to-send-synchronous-xhr-requests-during-page-dismissal-deprecated"></a>允許頁面在頁面關閉期間傳送同步 XHR 要求 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與變更不一致，而使頁面關閉期間不允許同步 XHR 要求時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本93中使用。

此原則可讓您指定頁面可以在頁面關閉期間傳送同步 XHR 要求。

如果啟用此原則，則頁面可以在頁面關閉期間傳送同步 XHR 要求。

如果停用或未設定此原則，則不允許頁面在頁面關閉期間傳送同步 XHR 要求。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowSyncXHRInPageDismissal
  - GP 名稱：允許頁面在頁面關閉期間傳送同步 XHR 要求 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowSyncXHRInPageDismissal
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowSyncXHRInPageDismissal
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowtokenbindingforurls"></a>AllowTokenBindingForUrls

  #### <a name="configure-the-list-of-sites-for-which-microsoft-edge-will-attempt-to-establish-a-token-binding-with"></a>設定 Microsoft Edge 將嘗試建立與 [權杖繫結] 連結的網站清單。

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  為瀏覽器將嘗試與其執行權杖繫結通訊協定之網站，設定 URL 模式清單。
對於此清單上的網域，瀏覽器將會在 TLS 交握中傳送權杖繫結 ClientHello (請參閱 https://tools.ietf.org/html/rfc8472))。
如果伺服器以有效的 ServerHello 回應回覆，瀏覽器將會在後續的 HTTPS 要求中建立並傳送權杖繫結訊息。 如需詳細資訊，請參閱 https://tools.ietf.org/html/rfc8471。

如果此清單為空白，則會停用權杖繫結。

此原則僅在具備虛擬安全模式功能的 Windows 10 裝置上可用。

從 Microsoft Edge 版本 86 開始，此原則不再支援動態重新整理。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowTokenBindingForUrls
  - GP 名稱：設定 Microsoft Edge 將嘗試建立權杖繫結的網站清單。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = "mydomain.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = "[*.]mydomain2.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = "[*.].mydomain2.com"

```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="allowtrackingforurls"></a>AllowTrackingForUrls

  #### <a name="configure-tracking-prevention-exceptions-for-specific-sites"></a>設定特定網站的防止追蹤例外

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  設定要從防止追蹤中排除的 URL 模式清單。

如果設定此原則，則會將已設定 URL 模式的清單從防止追蹤中排除。

如果未設定此原則，則會對所有網站使用來自「封鎖使用者的網頁瀏覽活動追蹤」原則 (如有設定) 或使用者個人設定的全域預設值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AllowTrackingForUrls
  - GP 名稱：設定特定網站的防止追蹤例外
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AllowTrackingForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="alternateerrorpagesenabled"></a>AlternateErrorPagesEnabled

  #### <a name="suggest-similar-pages-when-a-webpage-cant-be-found"></a>當找不到網頁時，推薦類似的頁面

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 向 Web 服務發出連線，以針對連線問題 (例如 DNS 錯誤) 產生 URL 和搜尋建議。

如果啟用此原則，則會使用 Web 服務來產生 URL 並搜尋網路錯誤的建議。

如果停用此原則，則不會對 Web 服務進行呼叫，且會顯示標準錯誤頁面。

如果未設定此原則，則 Microsoft Edge 會遵守 edge://settings/privacy 的 [服務] 底下所設定的使用者喜好設定。
具體來說，使用者可以將 **[找不到網頁時，推薦類似的頁面]** 切換為開啟或關閉。 請注意，如果您已啟用此原則 (AlternateErrorPagesEnabled)，則會開啟 [找不到網頁時，推薦類似的頁面] 設定，但使用者無法使用切換來變更設定。 如果您停用此原則，則會關閉 [找不到網頁時，推薦類似的頁面] 設定，且使用者無法使用切換來變更設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AlternateErrorPagesEnabled
  - GP 名稱：找不到網頁時，推薦類似的頁面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AlternateErrorPagesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AlternateErrorPagesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="alwaysopenpdfexternally"></a>AlwaysOpenPdfExternally

  #### <a name="always-open-pdf-files-externally"></a>一律在外部開啟 PDF 檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  停用 Microsoft Edge 中的內部 PDF 檢視器。

如果啟用此原則，則 Microsoft Edge 會將 PDF 檔案視為下載項目，並讓使用者使用預設應用程式開啟。

如果 Microsoft Edge 是預設的 PDF 閱讀程式，系統不會下載 PDF 檔案，而會繼續在 Microsoft Edge 中開啟。

如果未設定或停用此原則，則 Microsoft Edge 會開啟 PDF 檔案 (除非使用者停用)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AlwaysOpenPdfExternally
  - GP 名稱：一律在外部開啟 PDF 檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AlwaysOpenPdfExternally
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AlwaysOpenPdfExternally
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="ambientauthenticationinprivatemodesenabled"></a>AmbientAuthenticationInPrivateModesEnabled

  #### <a name="enable-ambient-authentication-for-inprivate-and-guest-profiles"></a>針對 InPrivate 和來賓設定檔啟用環境驗證

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  設定此原則以允許/禁止針對 Microsoft Edge 中的 InPrivate 和來賓設定檔執行環境驗證。

當未透過 NTLM/Kerberos/交涉挑戰/回應配置提供顯式認證時，環境驗證是使用預設認證的 HTTP 驗證。

如果將原則設定為 ‘RegularOnly’，則只會允許一般工作階段的環境驗證。 不允許 InPrivate 和來賓工作階段進行環境驗證。

如果將原則設定為 ‘InPrivateAndRegular’，則會允許 InPrivate 和一般工作階段的環境驗證。 不允許來賓工作階段進行環境驗證。

如果將原則設定為 ‘GuestAndRegular’，則會允許來賓和一般工作階段的環境驗證。 不允許 InPrivate 工作階段進行環境驗證。

如果將原則設定為 ‘All’，則會允許所有工作階段的環境驗證。

請注意，一般設定檔上一律會允許進行環境驗證。

在 Microsoft Edge 版本 81 及更新版本中，如果將原則保留未設定，則僅會在一般工作階段中啟用環境驗證。

原則選項對應：

* RegularOnly (0) = 僅在一般工作階段中啟用環境驗證

* InPrivateAndRegular (1) = 在 InPrivate 和一般工作階段中啟用環境驗證

* GuestAndRegular (2) = 在來賓和一般工作階段中啟用環境驗證

* All (3) = 在一般、InPrivate 和來賓工作階段中啟用環境驗證

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AmbientAuthenticationInPrivateModesEnabled
  - GP 名稱：針對 InPrivate 和來賓設定檔啟用環境驗證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AmbientAuthenticationInPrivateModesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AmbientAuthenticationInPrivateModesEnabled
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="appcacheforceenabled"></a>AppCacheForceEnabled

  #### <a name="allows-the-appcache-feature-to-be-re-enabled-even-if-its-turned-off-by-default"></a>允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態) 

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  如果您將此原則設定為 true，系統會啟用 AppCache，即使預設值為不提供 Microsoft Edge 中的 AppCache。

如果您將此原則設為 false 或未設定，AppCache 將會依照 Microsoft Edge 的預設值決定是否啟用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AppCacheForceEnabled
  - GP 名稱：允許重新啟用 AppCache 功能 (即使此功能預設為關閉狀態) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AppCacheForceEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AppCacheForceEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="applicationlocalevalue"></a>ApplicationLocaleValue

  #### <a name="set-application-locale"></a>設定應用程式地區設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 中的應用程式地區設定，並防止使用者變更地區設定。

如果啟用此原則，則 Microsoft Edge 會使用指定的地區設定。 如果不支援所設定的地區設定，則會改用 'en-US'。

如果停用或未設定此設定，則 Microsoft Edge 會使用使用者指定偏好地區設定 (如果已設定) 或後援地區設定 'en-US'。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ApplicationLocaleValue
  - GP 名稱：設定應用程式地區設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ApplicationLocaleValue
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"en"
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="audiocaptureallowed"></a>AudioCaptureAllowed

  #### <a name="allow-or-block-audio-capture"></a>允許或封鎖音訊擷取

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許您設定是否提示使用者授與網站其音訊擷取裝置的存取權。 此原則適用於所有 URL，[AudioCaptureAllowedUrls](#audiocaptureallowedurls) 清單中設定的除外。

如果啟用此原則或未設定 (預設值)，則會提示使用者輸入音訊擷取存取權 ([AudioCaptureAllowedUrls](#audiocaptureallowedurls) 清單中的 URL 除外)。 這些列出的 URL 會獲授與存取權，且不會提示。

如果停用此原則，則不會提示使用者，且音訊擷取僅可供 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 中設定的 URL 存取。

此原則會影響所有類型的音訊輸入，而不僅僅是內建的麥克風。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AudioCaptureAllowed
  - GP 名稱：允許或封鎖音訊擷取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AudioCaptureAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AudioCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="audiocaptureallowedurls"></a>AudioCaptureAllowedUrls

  #### <a name="sites-that-can-access-audio-capture-devices-without-requesting-permission"></a>無需要求權限即可存取音訊擷取裝置的網站

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 模式指定可使用音訊擷取裝置的網站，而不詢問使用者提供權限。 此清單中的模式會對照要求端 URL 的安全性來源進行比對。 如果符合，則網站會自動獲授與音訊擷取裝置的存取權。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AudioCaptureAllowedUrls
  - GP 名稱：無需要求權限即可存取音訊擷取裝置的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AudioCaptureAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="audiosandboxenabled"></a>AudioSandboxEnabled

  #### <a name="allow-the-audio-sandbox-to-run"></a>允許音訊沙盒執行

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  此原則會控制音訊處理程序沙盒。

如果啟用此原則，則音訊處理程序會在沙盒中執行。

如果停用此原則，音訊處理程序將不在沙盒中執行，而 WebRTC 音訊處理模組將在轉譯器處理程序中執行。
這會讓使用者處於與不在沙盒中執行音訊子系統相關的安全性風險。

如果未設定此原則，則會使用音訊沙盒的預設設定，這可能會因平台而有所不同。

此原則的目的是讓企業能夠在他們使用會干擾沙盒的安全性軟體設定時，有彈性可停用音訊沙盒。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AudioSandboxEnabled
  - GP 名稱：允許音訊沙盒執行
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AudioSandboxEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AudioSandboxEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autoimportatfirstrun"></a>AutoImportAtFirstRun

  #### <a name="automatically-import-another-browsers-data-and-settings-at-first-run"></a>在首次執行時，自動匯入其他瀏覽器的資料和設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則，則來自指定瀏覽器的所有支援資料類型和設定都會在初次執行時以無訊息方式自動匯入。 在初次執行體驗期間，也會略過匯入區段。

來自舊版 Microsoft Edge 的瀏覽器資料，一律會在初次執行時以無訊息方式移轉，而無論此原則的值為何。

如果將此原則設為 'FromDefaultBrowser'，則會匯入與受管理裝置上的預設瀏覽器對應的資料類型。

如果受管理的裝置中未出現指定為此原則的值的瀏覽器，Microsoft Edge 將直接略過匯入，而不會通知使用者。

如果將此原則設定為 'DisabledAutoImport'，則會完全略過初次執行體驗的匯入部分，且 Microsoft Edge 不會自動匯入瀏覽器資料和設定。

如果將此原則設定為 'FromInternetExplorer'，則會從 Internet Explorer 匯入下列資料類型：
1. 我的最愛或書籤
2. 儲存的密碼
3. 搜尋引擎
4. 瀏覽歷程記錄
5. 首頁

如果將此原則設定為 'FromGoogleChrome'，則會從 Google Chrome 匯入下列資料類型：
1. 我的最愛
2. 儲存的密碼
3. 地址及其他資訊
4. 付款資訊
5. 瀏覽歷程記錄
6. 設定
7. 釘選和開啟的索引標籤
8. Extensions
9. Cookie

注意：如需有關從 Google Chrome 匯入之內容的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2120835](https://go.microsoft.com/fwlink/?linkid=2120835)

如果將此原則設定為 'FromSafari'，使用者資料就不再匯入到 Microsoft Edge。 這是因為在 Mac 上使用完整的磁片存取方式所致。
在 macOS Mojave 及更新版本中，Safari 資料不可能再自動匯入到 Microsoft Edge 中。

從 Microsoft Edge 版本 83 開始，如果此原則設定為 'FromMozillaFirefox'，則會從 Mozilla Firefox 匯入下列資料類型：
1. 我的最愛或書籤
2. 儲存的密碼
3. 地址及其他資訊
4. 瀏覽歷程記錄

如果您想要限制特定資料類型無法在受管理的裝置上匯入，您可以將此原則與 [ImportAutofillFormData](#importautofillformdata)、[ImportBrowserSettings](#importbrowsersettings)、[ImportFavorites](#importfavorites) 等其他原則搭配使用。

原則選項對應：

* FromDefaultBrowser (0) = 從預設瀏覽器自動匯入所有支援的資料類型和設定

* FromInternetExplorer (1) = 從 Internet Explorer 自動匯入所有支援的資料類型和設定

* FromGoogleChrome (2) = 從 Google Chrome 自動匯入所有支援的資料類型和設定

* FromSafari (3) = 從 Safari 自動匯入所有支援的資料類型和設定

* DisabledAutoImport (4) = 停用自動匯入，並略過初次執行體驗的匯入區段

* FromMozillaFirefox (5) = 從 Mozilla Firefox 自動匯入所有支援的資料類型和設定

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoImportAtFirstRun
  - GP 名稱：在首次執行時，自動匯入其他瀏覽器的資料和設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoImportAtFirstRun
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoImportAtFirstRun
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autolaunchprotocolsfromorigins"></a>AutoLaunchProtocolsFromOrigins

  #### <a name="define-a-list-of-protocols-that-can-launch-an-external-application-from-listed-origins-without-prompting-the-user"></a>定義一份協定清單，可在不須提示使用者的情下，從列出的來源啟動外部應用程式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  可讓您設定一份協定的清單，以及每個協定相關聯的 [允許的來源模式] 清單，以便在不提示使用者的情況下啟動外部應用程式。 在列出清單時，不應包含尾端分隔符號。 例如，列出「skype」，而不是「skype:」或「skype://」。

若您設定了此原則，則只有在下列情況下，才允許協定在不使用原則提示下啟動外部應用程式：

- 將協定列於

- 嘗試啟動協定的網站來源，符合此協定的 allowed_origins 清單中的其中一個原始模式。

如果其中一個條件設為 false，原則將不會省略外部通訊提示。

如果您未設定此原則，系統不會啟動任何協定。 使用者可以在每個協定/每個網站上退出提示，除非將 [ ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) 原則設為 [停用]。 此原則不會影響使用者設定的每個通訊協定/每個網站的提示。

「來源比對」模式使用類似格式，適合 [URLBlocklist](#urlblocklist) 原則，文件儲存在 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

然而，此原則的「來源比對」模式不能包含 "/path" 或 "@query" 元素。 任何含有 "/path" 或 "@query" 元素的模式都會被忽略。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoLaunchProtocolsFromOrigins
  - GP 名稱：定義一份協定清單，可從列出的來源啟動外部應用程式，且不須提示使用者
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoLaunchProtocolsFromOrigins
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [
  {
    "allowed_origins": [
      "example.com",
      "http://www.example.com:8080"
    ],
    "protocol": "spotify"
  },
  {
    "allowed_origins": [
      "https://example.com",
      "https://.mail.example.com"
    ], 
    "protocol": "msteams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "msoutlook"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\AutoLaunchProtocolsFromOrigins = [{"allowed_origins": ["example.com", "http://www.example.com:8080"], "protocol": "spotify"}, {"allowed_origins": ["https://example.com", "https://.mail.example.com"], "protocol": "msteams"}, {"allowed_origins": ["*"], "protocol": "msoutlook"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoLaunchProtocolsFromOrigins
  - 範例值：
``` xml
<key>AutoLaunchProtocolsFromOrigins</key>
<array>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>example.com</string>
      <string>http://www.example.com:8080</string>
    </array>
    <key>protocol</key>
    <string>spotify</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>https://example.com</string>
      <string>https://.mail.example.com</string>
    </array>
    <key>protocol</key>
    <string>teams</string>
  </dict>
  <dict>
    <key>allowed_origins</key>
    <array>
      <string>*</string>
    </array>
    <key>protocol</key>
    <string>outlook</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autoopenallowedforurls"></a>AutoOpenAllowedForURLs

  #### <a name="urls-where-autoopenfiletypes-can-apply"></a>URLs where AutoOpenFileTypes 可以套用 

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  適用 [AutoOpenFileTypes](#autoopenfiletypes) 的URLs 清單。 此原則不會影響使用者透過下載區設定的自動開啟值... >「永遠開啟這種類型的檔案」功能表項目。

若您將 URLs 設在此原則內，只要此 URL 屬於這個集合，且該檔案類型為 [AutoOpenFileTypes](#autoopenfiletypes)所列之一，系統會利用此原則自動開啟檔案。 如果其中一個條件為 false，則下載不會根據原則自動開啟。

若您未設定此原則，所有文件類型在 [AutoOpenFileTypes](#autoopenfiletypes) 的下載皆可自動打開。

URL 模式的格式必須依照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoOpenAllowedForURLs
  - GP 名稱：AutoOpenFileTypes 可以套用的 URLs 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)： SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = "example.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = ".exact.hostname.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoOpenAllowedForURLs
  - 範例值：
``` xml
<array>
  <string>example.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autoopenfiletypes"></a>AutoOpenFileTypes

  #### <a name="list-of-file-types-that-should-be-automatically-opened-on-download"></a>檔案類型清單應在下載時自動開啟

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  此原則設定的檔案類型清單應在下載時自動開啟。 注意：在列出檔案類型時，不應包含前置分隔符號，因此請列出 "txt"，而不是 ".txt"。

根據預設，系統會自動開啟所有 URLs 的檔案類型。 您可以使用 [AutoOpenAllowedForURLs](#autoopenallowedforurls) 原則限制可自動開啟這些檔案類型的 URLs。

應自動開啟的檔案類型，仍會受到已啟用的 Microsoft Defender SmartScreen 檢查，若未能通過檢查，系統即不會開啟這些檔案。

使用者已指定要自動開啟的檔案類型，將會在下載時持續自動開啟。 使用者仍可繼續指定其他要自動開啟的檔案類型。

若您未設定此原則，只有經使用者指定要自動開啟的檔案類型，才會在下載時持續自動開啟。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoOpenFileTypes
  - GP 名稱：檔案類型清單應在下載時自動開啟
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = "exe"
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = "txt"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoOpenFileTypes
  - 範例值：
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autofilladdressenabled"></a>AutofillAddressEnabled

  #### <a name="enable-autofill-for-addresses"></a>啟用地址自動填寫

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用自動填寫功能，並允許使用者使用先前儲存的資訊自動完成網頁表單中的地址資訊。

如果停用此原則，則自動填寫不會建議或填入地址資訊，也不會儲存使用者在瀏覽網頁時可能提交的其他地址資訊。

如果啟用此原則或未設定，則使用者可以在使用者介面中控制地址的自動填寫。

請注意，如果停用此原則，則也會停止所有網頁表單的所有活動，付款和密碼表單除外。 不會儲存更多項目，且 Microsoft Edge 將不會建議或自動填寫任何先前的項目。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutofillAddressEnabled
  - GP 名稱：啟用地址自動填寫
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AutofillAddressEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutofillAddressEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autofillcreditcardenabled"></a>AutofillCreditCardEnabled

  #### <a name="enable-autofill-for-credit-cards"></a>啟用信用卡自動填寫

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用 Microsoft Edge 的自動填寫功能，並讓使用者使用先前儲存的資訊自動完成網頁表單中的信用卡資訊。

如果停用此原則，則自動填寫不會建議或填入信用卡資訊，也不會儲存使用者在瀏覽網頁時可能提交的其他信用卡資訊。

如果啟用此原則或未設定，則使用者可以控制信用卡的自動填寫。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutofillCreditCardEnabled
  - GP 名稱：啟用信用卡自動填寫
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AutofillCreditCardEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutofillCreditCardEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="automatichttpsdefault"></a>AutomaticHttpsDefault

  #### <a name="configure-automatic-https"></a>設定自動 HTTPS

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  此原則可讓您管理 [AutomaticHttpsDefault](#automatichttpsdefault) 設定，此設定會從 HTTP 切換至 HTTPS。

此功能可強制執行更安全的連線，協助抵禦中間人攻擊，但使用者可能會遇到更多連接錯誤。

注意： 'UpgradeCapableDomains' 設定需要元件清單，如果 [ComponentUpdatesEnabled](#componentupdatesenabled) 設定為 '停用'，則將不會升級這些連接。

如果未設定此原則， 將會啟用 [AutomaticHttpsDefault](#automatichttpsdefault) ，且只會升級為可能支援 HTTPS 網域的連線。

原則選項對應：

* DisableAutomaticHttps (0) = 已停用自動 HTTPS 功能。

* UpgradeCapableDomains (1) = 在可能支援 HTTPS 的網域上，以 HTTP 傳遞的瀏覽會切換至 HTTPS。

* AlwaysUpgrade (2) = 所有透過 HTTP 傳遞的瀏覽都會切換至 HTTPS。 連線錯誤可能會更常發生。

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutomaticHttpsDefault
  - GP 名稱：設定自動 HTTPS
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AutomaticHttpsDefault
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutomaticHttpsDefault
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="autoplayallowed"></a>AutoplayAllowed

  #### <a name="allow-media-autoplay-for-websites"></a>允許網站自動播放媒體

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  此原則會設定網站的媒體自動播放原則。

預設設定 [尚未設定] 會遵守目前的媒體自動播放設定，並可讓使用者設定其自動播放設定。

設定為 [已啟用] 會將媒體自動播放設定為「允許」。  允許所有網站自動播放媒體。 使用者無法覆寫此原則。

設定設為 [已停用] 會將媒體自動播放設定為「封鎖」。  不允許任何網站自動播放媒體。 使用者無法覆寫此原則。

需要關閉索引標籤並重新開啟，此原則才能生效。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：AutoplayAllowed
  - GP 名稱：允許網站自動播放媒體
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoplayAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：AutoplayAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="backgroundmodeenabled"></a>BackgroundModeEnabled

  #### <a name="continue-running-background-apps-after-microsoft-edge-closes"></a>在 Microsoft Edge 關閉後繼續執行背景應用程式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 處理程序在 OS 登入時啟動，並持續執行直到最後一個瀏覽器視窗關閉為止。 在此案例中，背景應用程式和目前瀏覽工作階段會保持作用中，包括任何工作階段 Cookie。 開啟中的背景處理程序會在系統匣中顯示圖示，且一律能從該位置關閉。

如果啟用此原則，則會開啟背景模式。

如果停用此原則，則背景模式會關閉。

如果未設定此原則，則最初會關閉背景模式，而使用者可以在 edge://settings/system 中設定其行為。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BackgroundModeEnabled
  - GP 名稱：在 Microsoft Edge 關閉後繼續執行背景應用程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：BackgroundModeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="backgroundtemplatelistupdatesenabled"></a>BackgroundTemplateListUpdatesEnabled

  #### <a name="enables-background-updates-to-the-list-of-available-templates-for-collections-and-other-features-that-use-templates"></a>啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  讓您啟用或停用對集錦的可用範本和使用範本的其他功能的清單進行背景更新。  範本用來在您將頁面儲存到集錦時，從網頁中擷取豐富的中繼資料。

如果啟用此設定或未設定此設定，則會每隔 24 小時在背景中透過 Microsoft 服務下載可用的範本清單。

如果停用此設定，則會在需要時下載可用範本清單。 這類型的下載可能會導致集錦及其他功能的效能些微降低。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BackgroundTemplateListUpdatesEnabled
  - GP 名稱：啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BackgroundTemplateListUpdatesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BackgroundTemplateListUpdatesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="bingadssuppression"></a>BingAdsSuppression

  #### <a name="block-all-ads-on-bing-search-results"></a>封鎖 Bing 搜尋結果中的所有廣告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  在 Bing.com 上啟用無廣告的搜尋體驗

如果啟用此原則，則使用者可以在 bing.com 上搜尋，並提供無廣告的搜尋體驗。 同時，安全搜尋設定會設定為「嚴格」，而且無法由使用者變更。

如果未設定此原則，則預設體驗會在 bing.com 的搜尋結果中出現廣告。 安全搜尋會預設設為「中等」，並且可由使用者變更。

此原則僅適用由 Microsoft 識別為 EDU 租用戶的 K-12 SKU。

請參閱[https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711)，以深入了解此原則或下列案例是否適合您：

* 您有 EDU 租用戶，但原則沒有作用。

* 您的 IP allowlisted 有無廣告的免費搜尋體驗。

* 您在 Microsoft Edge 舊版中擁有無廣告的搜尋體驗，並想要升級至新版 Microsoft Edge。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BingAdsSuppression
  - GP 名稱：封鎖 Bing 搜尋結果中的所有廣告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BingAdsSuppression
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BingAdsSuppression
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="blockthirdpartycookies"></a>BlockThirdPartyCookies

  #### <a name="block-third-party-cookies"></a>封鎖第三方 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  封鎖不是來自網址列中網域的網頁元素，使其無法設定 Cookie。

如果啟用此原則，則網址列中不是來自網域的網頁元素就無法設定 Cookie

如果停用此原則，來自網址列以外網域的網頁元素可以設定 Cookie。

如果未設定此原則，則會啟用協力廠商 Cookie，但使用者可以變更此設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BlockThirdPartyCookies
  - GP 名稱：封鎖第三方 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：BlockThirdPartyCookies
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BlockThirdPartyCookies
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="browseraddprofileenabled"></a>BrowserAddProfileEnabled

  #### <a name="enable-profile-creation-from-the-identity-flyout-menu-or-the-settings-page"></a>啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者使用 [新增個人檔案]**** 選項建立新的設定檔。
如果啟用此原則或未設定，則 Microsoft Edge 會允許使用者使用 [身分識別] 飛出視窗功能表或 [設定] 頁面上的 [新增個人檔案]**** 來建立新的個人檔案。

如果停用此原則，則使用者無法從 [身分識別] 飛出視窗功能表或 [設定] 頁面新增設定檔。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BrowserAddProfileEnabled
  - GP 名稱：啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserAddProfileEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BrowserAddProfileEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="browserguestmodeenabled"></a>BrowserGuestModeEnabled

  #### <a name="enable-guest-mode"></a>啟用來賓模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用可允許在 Microsoft Edge 中使用來賓設定檔的選項。 在來賓設定檔中，瀏覽器不會從現有設定檔匯入瀏覽資料，而且會在所有來賓設定檔關閉時刪除瀏覽資料。

如果啟用此原則或未設定，則 Microsoft Edge 會讓使用者在來賓設定檔中瀏覽。

如果停用此原則，則 Microsoft Edge 不會讓使用者使用來賓設定檔瀏覽。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BrowserGuestModeEnabled
  - GP 名稱：啟用來賓模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserGuestModeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BrowserGuestModeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="browsernetworktimequeriesenabled"></a>BrowserNetworkTimeQueriesEnabled

  #### <a name="allow-queries-to-a-browser-network-time-service"></a>允許查詢瀏覽器網路時間服務

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  防止 Microsoft Edge 偶爾傳送查詢至瀏覽器網路時間服務，以擷取準確的時間戳記。

如果停用此原則，則 Microsoft Edge 將會停止將查詢傳送至瀏覽器網路時間服務。

如果啟用此原則或未設定，則 Microsoft Edge 會偶爾將查詢傳送至瀏覽器網路時間服務。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BrowserNetworkTimeQueriesEnabled
  - GP 名稱：允許查詢瀏覽器網路時間服務
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserNetworkTimeQueriesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BrowserNetworkTimeQueriesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="browsersignin"></a>BrowserSignin

  #### <a name="browser-sign-in-settings"></a>瀏覽器登入設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定使用者是否可以使用其帳戶登入 Microsoft Edge，並使用與帳戶相關的服務，例如同步和單一登入。 若要控制同步的可用性，請改用 [SyncDisabled](#syncdisabled) 原則。

如果將此原則設定為 ‘停用’，請確定也將 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 原則設定為已停用，因為 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 會停用自動登入瀏覽器設定檔的建立。 如果這兩個原則都已設定，則 Microsoft Edge 將會使用 [停用瀏覽器登入] 原則，並如同 [NonRemovableProfileEnabled](#nonremovableprofileenabled) 設為已停用般執行動作。

如果將此原則設定為 ‘啟用’，則使用者可以登入瀏覽器。 登入瀏覽器並不代表同步會預設開啟；而使用者必須另行選擇加入，才能使用此功能。

如果將此原則設定為 ‘強制’，則使用者必須登入設定檔才能使用瀏覽器。 依預設，這會允許使用者選擇是否要同步到自己的帳戶，除非由網域系統管理員或使用 [SyncDisabled](#syncdisabled) 原則停用同步。 [BrowserGuestModeEnabled](#browserguestmodeenabled) 原則的預設值設定為 false。

如果未設定此原則，則使用者可以決定是否要啟用瀏覽器登入選項，並在適合時使用該選項。

原則選項對應：

* 停用 (0) = 停用瀏覽器登入

* 啟用 (1) = 啟用瀏覽器登入

* 強制 (2) = 強制使用者登入才能使用瀏覽器

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BrowserSignin
  - GP 名稱：瀏覽器登入設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserSignin
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BrowserSignin
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="browsingdatalifetime"></a>BrowsingDataLifetime

  #### <a name="browsing-data-lifetime-settings"></a>流覽資料存留期設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 的流覽資料存留期設定。
此原則控制所選流覽資料的存留期。 如果啟用同步處理，此原則就不會有任何作用。
可用的資料類型有 'browsing_history'、'download_history'、 'cookies_and_other_site_data'、 'cached_images_and_files'、 'password_signin'、 'autofill'、'site_settings' 和 'hosted_app_data'.
Microsoft Edge 會定期移除超過「time_to_live_in_hours」的所選類型的資料。 刪除過期的資料將在瀏覽器啟動 15 秒後進行，然後在瀏覽器執行時，會每小時刪除一次。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： BrowsingDataLifetime
  - GP 名稱：流覽資料存留期設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： BrowsingDataLifetime
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\BrowsingDataLifetime = [
  {
    "data_types": [
      "browsing_history"
    ],
    "time_to_live_in_hours": 24
  },
  {
    "data_types": [
      "password_signin",
      "autofill"
    ],
    "time_to_live_in_hours": 12
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\BrowsingDataLifetime = [{"data_types": ["browsing_history"], "time_to_live_in_hours": 24}, {"data_types": ["password_signin", "autofill"], "time_to_live_in_hours": 12}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： BrowsingDataLifetime
  - 範例值：
``` xml
<key>BrowsingDataLifetime</key>
<array>
  <dict>
    <key>data_types</key>
    <array>
      <string>browsing_history</string>
    </array>
    <key>time_to_live_in_hours</key>
    <integer>24</integer>
  </dict>
  <dict>
    <key>data_types</key>
    <array>
      <string>password_signin</string>
      <string>autofill</string>
    </array>
    <key>time_to_live_in_hours</key>
    <integer>12</integer>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="builtindnsclientenabled"></a>BuiltInDnsClientEnabled

  #### <a name="use-built-in-dns-client"></a>使用內建的 DNS 用戶端

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制是否使用內建的 DNS 用戶端。

此原則會控制用來與 DNS 伺服器通訊的軟體堆疊：作業系統 DNS 用戶端或 Microsoft Edge 的內建 DNS 用戶端。 此原則不會影響使用的 DNS 伺服器：例如，如果作業系統已設定為使用企業 DNS 伺服器，則內建的 DNS 用戶端就會使用相同的伺服器。 它也不控制是否使用 DNS-over-HTTPS；Microsoft Edge 始終使用內建的解析程式來處理 DNS-over-HTTPS 要求。 請參閱 [DnsOverHttpsMode](#dnsoverhttpsmode) 原則，以取得控制 DNS-over-HTTPS 的相關資訊。

如果啟用此原則，則會使用內建的 DNS 用戶端 (如果可用)。

如果您停用此原則，則只有在使用 DNS-over-HTTPS 的情況下，才會使用內建的 DNS 用戶端。

如果您未設定此原則，則系統預設會在 macOS 和 Android 上啟用內建 DNS 用戶端 (當未啟用私人 DNS 也未啟用 VPN 時)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BuiltInDnsClientEnabled
  - GP 名稱：使用內建的 DNS 用戶端
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BuiltInDnsClientEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BuiltInDnsClientEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="builtincertificateverifierenabled"></a>BuiltinCertificateVerifierEnabled

  #### <a name="determines-whether-the-built-in-certificate-verifier-will-be-used-to-verify-server-certificates-deprecated"></a>決定是否使用內建的憑證驗證程式來驗證伺服器憑證 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  此原則已過時，因為其目的只是為了提供做為短期的機制，給予企業更多時間來更新其環境，並在發現它們與內建的認證驗證程式不相容時報告問題。

當 Mac OS X 上的舊版憑證驗證程式支援已計畫移除時，此原則無法在 Microsoft Edge 版本 92 上運作。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：BuiltinCertificateVerifierEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="cecpq2enabled"></a>CECPQ2Enabled

  #### <a name="cecpq2-post-quantum-key-agreement-enabled-for-tls"></a>已啟用 TLS 的 CECPQ2 後量子金鑰協定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 93 或更新版本

  #### <a name="description"></a>說明

  如果未設定此原則，或設定為啟用，則 Microsoft Edge 會遵循 CECPQ2 (TLS 中的後量子金鑰協定演算法) 的預設推出程式。

CECPQ2 會導致較大的 TLS 訊息，在極罕見的情況下，會觸發某些網路硬體中的錯誤。 可將此原則設定為 False，以在網路問題解決時停用 CECPQ2。

此原則是暫時方法，將在未來版本的 Microsoft Edge 中移除。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CECPQ2Enabled
  - GP 名稱：已啟用 TLS 的 CECPQ2 後量子金鑰協定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：CECPQ2Enabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CECPQ2Enabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="certificatetransparencyenforcementdisabledforcas"></a>CertificateTransparencyEnforcementDisabledForCas

  #### <a name="disable-certificate-transparency-enforcement-for-a-list-of-subjectpublickeyinfo-hashes"></a>針對 subjectPublicKeyInfo 雜湊的清單，停用憑證透明度強化

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  針對 subjectPublicKeyInfo 雜湊的清單，停用憑證透明度需求的強制執行。

此原則可讓您針對包含其中一個指定 subjectPublicKeyInfo 雜湊憑證的憑證鏈結，停用憑證透明度揭露需求。 這會允許可能以其他方式不受信任的憑證，因為它們並未公開揭露，而仍用於企業主機。

若要在設定此原則時停用認證透明度強化，則必須符合下列其中一組條件：
1. 雜湊是伺服器憑證的 subjectPublicKeyInfo。
2. 雜湊屬於 subjectPublicKeyInfo，會顯示在憑證鏈結的 CA 憑證中，該 CA 憑證是透過 X.509v3 nameConstraints 擴充功能來限制，permittedSubtrees 中會出現一或多個 directoryName nameConstraints，且 directoryName 會包含 organizationName 屬性。
3. 雜湊屬於 subjectPublicKeyInfo，會顯示在 CA 憑證中憑證鏈結中，該 CA 憑證在憑證主體中有一或多個 organizationName 屬性，而伺服器的憑證包含相同數量的 organizationName 屬性、順序相同，並具有完全相同的值。

subjectPublicKeyInfo 雜湊的指定方式是將雜湊演算法名稱、"/" 字元，以及套用至指定憑證的 DER 編碼的 subjectPublicKeyInfo 雜湊演算法的 Base64 編碼串連。 此 Base64 編碼與 SPKI 指紋的格式相同，如 RFC 7469 2.4 節中所定義。 將忽略無法辨識的雜湊演算法。 目前唯一支援的雜湊演算法是 "sha256"。

如果停用或未設定此原則，則需要透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未根據憑證透明度原則揭露的話)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForCas
  - GP 名稱：停用 subjectPublicKeyInfo 雜湊清單的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = "sha256//////////////////////w=="

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForCas
  - 範例值：
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="certificatetransparencyenforcementdisabledforlegacycas"></a>CertificateTransparencyEnforcementDisabledForLegacyCas

  #### <a name="disable-certificate-transparency-enforcement-for-a-list-of-legacy-certificate-authorities"></a>停用舊版憑證授權單位清單的憑證透明度強化

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  針對舊版憑證授權單位 (CA) 的清單，停用憑證透明度需求的強制執行。

此原則可讓您針對包含其中一個指定 subjectPublicKeyInfo 雜湊憑證的憑證鏈結，停用憑證透明度揭露需求。 這會允許可能以其他方式不受信任的憑證，因為它們並未公開揭露，而仍繼續用於企業主機。

若要停用憑證透明度強制執行，您必須將雜湊設定為會顯示在識別為舊版憑證授權單位 (CA) 的 CA 憑證中的 subjectPublicKeyInfo。 舊版 CA 是由 Microsoft Edge 所支援的一或多個作業系統所公開信任的 CA。

您可以指定 subjectPublicKeyInfo 雜湊，方法是將雜湊演算法名稱、"/" 字元，以及套用至指定憑證的 DER 編碼的 subjectPublicKeyInfo 雜湊演算法的 Base64 編碼串連。 此 Base64 編碼與 SPKI 指紋的格式相同，如 RFC 7469 2.4 節中所定義。 將忽略無法辨識的雜湊演算法。 目前唯一支援的雜湊演算法是 "sha256"。

如果未設定此原則，則需要透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未根據憑證透明度原則揭露的話)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP 名稱：停用舊版憑證授權單位清單的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = "sha256/AAAAAAAAAAAAAAAAAAAAAA=="
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = "sha256//////////////////////w=="

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForLegacyCas
  - 範例值：
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="certificatetransparencyenforcementdisabledforurls"></a>CertificateTransparencyEnforcementDisabledForUrls

  #### <a name="disable-certificate-transparency-enforcement-for-specific-urls"></a>停用針對特定 URL 的憑證透明度強化

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  針對所列的 URL，停用憑證透明度需求的強制執行。

此原則可讓您不透過憑證透明度，揭露指定 URL 中主機名稱的憑證。 這可讓您使用可能以其他方式不受信任的憑證，因為它們並正確未公開揭露，但會使得較難以偵測為這些主機錯誤核發的憑證。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。 因為憑證僅對指定的主機名稱有效，與配置、連接埠或路徑無關，因此只會考慮 URL 的主機名稱部分。 不支援萬用字元主機。

如果未設定此原則，則應該透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未揭露的話)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForUrls
  - GP 名稱：停用針對特定 URL 的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = ".contoso.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForUrls
  - 範例值：
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="clearbrowsingdataonexit"></a>ClearBrowsingDataOnExit

  #### <a name="clear-browsing-data-when-microsoft-edge-closes"></a>在 Microsoft Edge 關閉時清除瀏覽資料

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  Microsoft Edge 預設不會在關閉時清除瀏覽資料。 瀏覽資料包括在表單中輸入的資訊、密碼，甚至是造訪的網站。

如果啟用此原則，則每次關閉 Microsoft Edge 時，會刪除所有瀏覽資料。 請注意，如果啟用此原則，則它會優先於您設定的 [DefaultCookiesSetting](#defaultcookiessetting)

如果停用或未設定此原則，則使用者可以在 [設定] 中設定 [清除瀏覽資料] 選項。

如果啟用此原則，則請勿設定 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 原則，因為它們全都涉及刪除瀏覽資料。 如果設定了前述原則和此原則，則 Microsoft Edge 關閉時會刪除所有瀏覽資料，無論您如何設定 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)。

若要避免在結束時刪除 Cookie，請設定 [SaveCookiesOnExit](#savecookiesonexit) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ClearBrowsingDataOnExit
  - GP 名稱：在 Microsoft Edge 關閉時清除瀏覽資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ClearBrowsingDataOnExit
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ClearBrowsingDataOnExit
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="clearcachedimagesandfilesonexit"></a>ClearCachedImagesAndFilesOnExit

  #### <a name="clear-cached-images-and-files-when-microsoft-edge-closes"></a>在 Microsoft Edge 關閉時清除快取的影像和檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  Microsoft Edge 預設不會在關閉時清除快取的影像和檔案。

如果啟用此原則，則每次關閉 Microsoft Edge 時，會刪除快取的影像和檔案。

如果停用此原則，則使用者無法在 edge://settings/clearBrowsingDataOnClose 中設定快取影像和檔案選項。

如果未設定此原則，則使用者可以選擇是否要在結束時清除快取的影像和檔案。

如果停用此原則，則請勿啟用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則，因為它們全都涉及刪除資料。 如果您同時設定這兩項，則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則優先，並且會在 Microsoft Edge 關閉時刪除所有資料，無論 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 的設定方式如何。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ClearCachedImagesAndFilesOnExit
  - GP 名稱：在 Microsoft Edge 關閉時清除快取的影像和檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ClearCachedImagesAndFilesOnExit
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ClearCachedImagesAndFilesOnExit
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="clickonceenabled"></a>ClickOnceEnabled

  #### <a name="allow-users-to-open-files-using-the-clickonce-protocol"></a>允許使用者使用 ClickOnce 通訊協定開啟檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  允許使用者使用 ClickOnce 通訊協定開啟檔案。 ClickOnce 通訊協定會允許網站要求瀏覽器利用使用者電腦或裝置上的 ClickOnce 檔案處理常式從特定 URL 開啟檔案。

如果啟用此原則，則使用者可以使用 ClickOnce 通訊協定來開啟檔案。 此原則會覆寫 edge://flags/ 頁面中使用者的 ClickOnce 設定。

如果停用此原則，則使用者無法使用 ClickOnce 通訊協定來開啟檔案。 而是會改為使用瀏覽器將檔案儲存到檔案系統。 此原則會覆寫 edge://flags/ 頁面中使用者的 ClickOnce 設定。

如果您未設定此原則，Microsoft Edge 87 之前的使用者將無法使用 ClickOnce 通訊協定開啟檔案。 不過，他們可以利用 edge://flags/ 頁面選擇是否要啟用 ClickOnce 通訊協定的使用。 Microsoft Edge 版 本87 及更新版本的使用者可以預設使用 ClickOnce 通訊協定來開啟檔案，但可以利用 edge://flags/頁面選擇停用 ClickOnce 通訊協定。

停用 ClickOnce 可能會防止 ClickOnce 應用程式 (.application 檔案) 正常啟動。

如需 ClickOnce 的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ClickOnceEnabled
  - GP 名稱：允許使用者使用 ClickOnce 通訊協定開啟檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ClickOnceEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="collectionsservicesandexportsblocklist"></a>CollectionsServicesAndExportsBlockList

  #### <a name="block-access-to-a-specified-list-of-services-and-export-targets-in-collections"></a>封鎖集錦中服務和匯出目標特定清單的存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  列出使用者無法在 Microsoft Edge 的集錦功能中存取的特定服務和匯出目標。 這包括顯示來自 Bing 的其他資料，並將集錦匯出至 Microsoft 產品或外部合作夥伴。

如果啟用此原則，系統會封鎖與指定清單相符的服務和匯出目標。

如果未設定此原則，則對強制執行的可接受服務和匯出目標沒有限制。

原則選項對應：

* pinterest_suggestions (pinterest_suggestions) = Pinterest 建議

* collections_share (collections_share) = 共享集合

* local_pdf (local_pdf) = 將本地 PDF 以 集錦儲存到 OneDrive 

* send_word (send_word) = 將集錦傳送至 Microsoft Word

* send_excel (send_excel) = 將集錦傳送至Microsoft Excel

* send_onenote (send_onenote) = 將集錦傳送至 Microsoft OneNote

* send_pinterest (send_pinterest) = 將集錦傳送至 Pinterest

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CollectionsServicesAndExportsBlockList
  - GP 名稱：封鎖集錦中服務和匯出目標特定清單的存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = "pinterest_suggestions"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\2 = "collections_share"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\3 = "local_pdf"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\4 = "send_word"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\5 = "send_excel"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\6 = "send_onenote"
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\7 = "send_pinterest"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： CollectionsServicesAndExportsBlockList
  - 範例值：
``` xml
<array>
  <string>pinterest_suggestions</string>
  <string>collections_share</string>
  <string>local_pdf</string>
  <string>send_word</string>
  <string>send_excel</string>
  <string>send_onenote</string>
  <string>send_pinterest</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="commandlineflagsecuritywarningsenabled"></a>CommandLineFlagSecurityWarningsEnabled

  #### <a name="enable-security-warnings-for-command-line-flags"></a>啟用命令列旗標的安全性警告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  如果停用，則此原則會在 Microsoft Edge 使用可能有危險的命令列旗標啟動時防止安全性警告顯示。

如果啟用或未設定，則使用這些命令列旗標來啟動 Microsoft Edge 時，會顯示安全性警告。

例如，--disable-gpu-sandbox 旗標會產生此警告：您使用不支援的命令列旗標：--disable-gpu-sandbox。 這會造成穩定性及安全性風險。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CommandLineFlagSecurityWarningsEnabled
  - GP 名稱：啟用命令列旗標的安全性警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：CommandLineFlagSecurityWarningsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CommandLineFlagSecurityWarningsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="componentupdatesenabled"></a>ComponentUpdatesEnabled

  #### <a name="enable-component-updates-in-microsoft-edge"></a>啟用 Microsoft Edge 中的元件更新

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如果啟用或未設定此原則，則會在 Microsoft Edge 中啟用元件更新。

如果停用此原則或將它設定為 false，則會停用 Microsoft Edge 中所有元件的元件更新。

不過，有些元件會從此原則免除。 這包括不包含可執行程式碼、不會著變更瀏覽器行為，或對安全性非常重要的何元件。 也就是說，即使您停用此原則，也會套用「對安全性非常重要」的更新。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ComponentUpdatesEnabled
  - GP 名稱：啟用 Microsoft Edge 中的元件更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ComponentUpdatesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ComponentUpdatesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="configuredonottrack"></a>ConfigureDoNotTrack

  #### <a name="configure-do-not-track"></a>設定不要追蹤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定是否要將「不要追蹤」要求傳送到要求追蹤資訊的網站。 「不要追蹤」要求可讓您瀏覽的網站知道您不希望您的瀏覽活動遭到追蹤。 依預設，Microsoft Edge 不會傳送「不要追蹤」要求，但是使用者可以開啟此功能以傳送要求。

如果啟用此原則，則一律會傳送「不要追蹤」要求到要求追蹤資訊的網站。

如果停用此原則，則永遠不會傳送要求。

如果未設定此原則，則使用者可以選擇是否要傳送這些要求。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ConfigureDoNotTrack
  - GP 名稱：設定不要追蹤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureDoNotTrack
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ConfigureDoNotTrack
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="configurefriendlyurlformat"></a>ConfigureFriendlyURLFormat

  #### <a name="configure-the-default-paste-format-of-urls-copied-from-microsoft-edge-and-determine-if-additional-formats-will-be-available-to-users"></a>設定從 Microsoft Edge 複製的 URL 預設貼上格式，並決定使用者是否可以使用其他格式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本
  - macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  如果已啟用 FriendlyURLs，Microsoft Edge 將會計算 URL 的其他標記法，並將它們放在剪貼簿中。

此原則會設定當使用者在外部應用程式中，或在沒有 [貼上為] 快顯功能表項目的 Microsoft Edge 內貼上時，要貼上的格式。

如果已設定，此原則會代表使用者進行選擇。 edge://settings/shareCopyPaste 中的選項會呈現灰色，且 [貼上為] 快顯功能表中的選項將無法使用。

* 未設定 = 使用者將可以選擇其偏好的貼上格式。 根據預設，這會設定為易記的 URL 格式。 Microsoft Edge 中的 [貼上為] 功能表將可供使用。

* 1 = 不在剪貼簿中儲存其他格式。 Microsoft Edge 中不會有 [貼上] 快顯功能表項目，且唯一可貼上的格式為純文字 URL 格式。 這實際上會停用易記 URL 功能。

* 3 = 使用者會在每次貼上可接受 RTF 文字的介面時取得易記 URL。 純文字 URL 仍可用於非豐富介面。 Microsoft Edge 中將不會有 [貼上為] 功能表。

* 4 = (目前未使用)

在某些貼上目的地和/或網站中，可能無法受支援較豐富的格式。 因此，如果要設定此原則，則建議使用純文字 URL 選項。

原則選項對應：

* PlainText (1) = 純文字 URL 沒有任何額外的資訊，例如頁面標題。 這是設定此原則時的建議選項。 如需詳細資訊，請參閱描述。

* TitledHyperlink (3) = 標題的超連結：指向所複製 URL 的超連結，但其可見文字是目的地頁面的標題。 這是易記 URL 格式。

* WebPreview (4) = 即將推出。 如果設定，則行為會與「純文字 URL」相同。

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ConfigureFriendlyURLFormat
  - GP 名稱：設定從 Microsoft Edge 複製的 URL 預設貼上格式，並決定使用者是否可以使用其他格式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureFriendlyURLFormat
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000003
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 優先順序鍵名稱： ConfigureFriendlyURLFormat
  - 範例值：
``` xml
<integer>3</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="configureonpremisesaccountautosignin"></a>ConfigureOnPremisesAccountAutoSignIn

  #### <a name="configure-automatic-sign-in-with-an-active-directory-domain-account-when-there-is-no-azure-ad-domain-account"></a>設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  如果使用者的電腦已加入網域且您的環境未混合加入，則可啟用使用 Active Directory 帳戶自動登入。 如果您想要改為讓使用者以其 Azure Active Directory 帳戶自動登入，請對您的環境套用 Azure AD 加入 (如需詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) 或混合式加入 (如需詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365))。

在每次啟動時，Microsoft Edge 都會嘗試使用此原則登入，只要啟動的第一個設定檔尚未登入，或之前沒有發生自動登入。

如果 [BrowserSignin](#browsersignin) 原則設為已停用，則此原則沒有作用。

如果啟用此原則，並將其設定為 'SignInAndMakeDomainAccountNonRemovable'，則 Microsoft Edge 會自動將已加入網域電腦的使用者以其 Active Directory 帳戶登入。

如果將此原則設定為 ‘已停用’ 或未設定，則 Microsoft Edge 不會自動將已加入網域電腦的使用者以 Active Directory 帳戶登入。

從 Microsoft Edge 89 開始，如果有現有的內部部署設定檔已停用 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 原則，且電腦現在已混合加入，即 它有 Azure AD 帳戶，它會自動將內部部署設定檔升級至 Azure AD 設定檔，以取得完整的 Azure AD 同步處理功能。

原則選項對應：

* 已停用 (0) = 已停用

* SignInAndMakeDomainAccountNonRemovable (1) = 登入並將網域帳戶設為不可移除

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ConfigureOnPremisesAccountAutoSignIn
  - GP 名稱：設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureOnPremisesAccountAutoSignIn
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="configureonlinetexttospeech"></a>ConfigureOnlineTextToSpeech

  #### <a name="configure-online-text-to-speech"></a>設定線上文字轉語音

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定瀏覽器是否可以利用「線上文字轉語音」語音字型，它是 Azure 認知服務的一部分。 這些語音字型的品質高於預先安裝的系統語音字型。

如果啟用或未設定此原則，則使用 SpeechSynthesis API 的 Web 型應用程式可以使用「線上文字轉語音」語音字型。

如果停用此原則，則語音字型將無法使用。

若要深入了解此功能，請參閱這裡：SpeechSynthesis API：[https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) 認知服務：[https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ConfigureOnlineTextToSpeech
  - GP 名稱：設定線上文字轉語音
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureOnlineTextToSpeech
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ConfigureOnlineTextToSpeech
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="configureshare"></a>ConfigureShare

  #### <a name="configure-the-share-experience"></a>設定共用體驗

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  如果將此原則設定為 'ShareAllowed' (預設值)，則使用者可以從 Microsoft Edge 的 [設定及其他] 功能表存取 Windows 10 的共用體驗，以便與系統上的其他應用程式共用。

如果將此原則設定為 'ShareDisallowed'，則使用者無法存取 Windows 10 的共用體驗。 如果 [共用] 按鈕在工具列上，則也會隱藏。

原則選項對應：

* ShareAllowed (0) = 允許使用共用體驗

* ShareDisallowed (1) = 不允許使用共用體驗

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ConfigureShare
  - GP 名稱：設定共用體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureShare
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="customhelplink"></a>CustomHelpLink

  #### <a name="specify-custom-help-link"></a>指定自訂說明連結

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  為 [說明] 功能表或 F1 鍵指定連結。

如果啟用此原則，則系統管理員可以為 [說明] 功能表或 F1 鍵指定連結。

如果停用或未設定此原則，則會使用 [說明] 功能表或 F1 鍵的預設連結。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：CustomHelpLink
  - GP 名稱：指定自訂說明連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：CustomHelpLink
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://go.microsoft.com/fwlink/?linkid=2080734"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：CustomHelpLink
  - 範例值：
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="dnsinterceptionchecksenabled"></a>DNSInterceptionChecksEnabled

  #### <a name="dns-interception-checks-enabled"></a>DNS 攔截檢查已啟用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  此原則會設定可用於停用 DNS 攔截檢查的本機交換器。 這些檢查會嘗試探索瀏覽器是否位於會將未知主機名稱重新導向的 Proxy 後面。

在網路設定已知的企業環境中，可能不需要此偵測。 可以將它停用，以避免啟動時以及每個 DNS 設定變更時的額外 DNS 和 HTTP 流量。

若您啟用或未設定此原則，系統便會執行 DNS 攔截檢查。

若您停用此原則，系統便不會執行 DNS 攔截檢查。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DNSInterceptionChecksEnabled
  - GP 名稱：DNS 攔截檢查已啟用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DNSInterceptionChecksEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DNSInterceptionChecksEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultbrowsersettingenabled"></a>DefaultBrowserSettingEnabled

  #### <a name="set-microsoft-edge-as-default-browser"></a>將 Microsoft Edge 設定為預設瀏覽器

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 7 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  若您將此原則設為 True，Microsoft Edge 就會在啟動時永遠檢查是否為預設瀏覽器，如果可能，則會自動註冊。

若您將此原則設為 False，Microsoft Edge 就會停止檢查是否為預設瀏覽器，並開啟此選項的使用者控制。

如果您未設定此原則，Microsoft Edge 可讓使用者控制是否將其設為預設值，如果不是，是否顯示使用者通知。

Windows 系統管理員的注意事項：此原則只適用執行 Windows 7 的電腦。 針對較新版本的 Windows，您必須部署一個「預設應用程式關聯」檔案，讓 Microsoft Edge 成為 HTTPS 和 HTTP 通訊協定 (以及選用的 FTP 通訊協定和檔案格式，例如 .html、.htm、.pdf、.svg、.webp) 的處理常式。 如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultBrowserSettingEnabled
  - GP 名稱：將 Microsoft Edge 設定為預設瀏覽器
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultBrowserSettingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultBrowserSettingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsearchprovidercontextmenuaccessallowed"></a>DefaultSearchProviderContextMenuAccessAllowed

  #### <a name="allow-default-search-provider-context-menu-search-access"></a>允許預設搜尋提供者操作功能表搜尋存取權

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  可在操作功能表上使用預設搜尋提供者。

如果您將此原則設為停用，則依賴於預設搜尋提供者的搜尋操作功能表將無法使用，而且側邊欄搜尋也無法使用。

如果將此原則設定為啟用或未設定，則可使用預設搜尋提供者和側邊欄搜尋的操作功能表項目。

只有啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 原則時，才會套用該原則值，否則不適用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSearchProviderContextMenuAccessAllowed
  - GP 名稱：允許預設搜尋提供者操作功能表搜尋存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DefaultSearchProviderContextMenuAccessAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSearchProviderContextMenuAccessAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultsensorssetting"></a>DefaultSensorsSetting

  #### <a name="default-sensors-setting"></a>預設的感應器設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以存取及使用感應器 (例如動作和光線感應器)。 您可完全封鎖或允許網站存取感應器。

將原則設定為 1 可讓網站存取及使用感應器。 將原則設定為 2 可讓網站拒絕存取感應器。

您可以使用 [SensorsAllowedForUrls](#sensorsallowedforurls) 和 [ SensorsBlockedForUrls](#sensorsblockedforurls) 原則來針對特定 URL 模式覆寫此原則。

如果您未設定此原則，則網站可以存取及使用感應器，且使用者可以變更此設定。 這是針對 [SensorsAllowedForUrls](#sensorsallowedforurls) 和 [SensorsBlockedForUrls](#sensorsblockedforurls) 的全域預設。

原則選項對應：

* AllowSensors (1) = 允許網站存取感應器

* BlockSensors (2) = 不允許任何網站存取感應器

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSensorsSetting
  - GP 唯一名稱：預設感應器設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultSensorsSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSensorsSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="defaultserialguardsetting"></a>DefaultSerialGuardSetting

  #### <a name="control-use-of-the-serial-api"></a>控制 Serial API 的使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  設定網站是否能夠存取序列通訊埠。 您可以完全封鎖存取，或在每次網站想要存取序列通訊埠時詢問使用者。

將原則設定為3，可讓網站要求序列通訊埠的存取權。 將原則設定為 2，可拒絕存取序列通訊埠。

您可以使用 [WebUsbAskForUrls](#serialaskforurls) 和 [WebUsbBlockedForUrls](#serialblockedforurls) 原則來針對特定 URL 模式覆寫此原則。

如果未設定此原則，則預設為網站可以詢問使用者是否可以存取序列通訊埠，且使用者可以變更此設定。

原則選項對應：

* BlockSerial (2) = 不允許任何網站透過 Serial API 要求存取序列通訊埠。

* AskSerial (3) = 允許網站要求使用者同意存取序列埠

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DefaultSerialGuardSetting
  - GP 唯一名稱：控制 Serial API 的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultSerialGuardSetting
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DefaultSerialGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="definepreferredlanguages"></a>DefinePreferredLanguages

  #### <a name="define-an-ordered-list-of-preferred-languages-that-websites-should-display-in-if-the-site-supports-the-language"></a>定義網站支援語言時，網站應該顯示的慣用語言的排序清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 作為 Accept-Language 要求 HTTP 標頭的一部分傳送至網站的語言變體，並防止使用者在 Microsoft Edge 設定中新增、移除或更改慣用語言的順序。 如果使用者想要變更 Microsoft Edge 所顯示的語言，或提供翻譯頁面，將受限於此原則中設定的語言。

如果啟用此原則，網站將以其支援的清單中的第一種語言顯示，除非使用其他網站特定的邏輯來確定顯示語言。 此原則中定義的語言變體將覆寫作為 [SpellcheckLanguage](#spellchecklanguage) 原則一部分設定的語言。

如果您沒有設定或停用此原則，Microsoft Edge 會將使用者指定的慣用語言作為 Accept-Language 要求 HTTP 標頭的一部分傳送至網站。

如需有效其他語言的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2148854](https://go.microsoft.com/fwlink/?linkid=2148854)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： DefinePreferredLanguages
  - GP 名稱：定義網站支援語言時，網站應該顯示的慣用語言的排序清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： DefinePreferredLanguages
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"en-US,fr,es"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： DefinePreferredLanguages
  - 範例值：
``` xml
<string>en-US,fr,es</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="delaynavigationsforinitialsitelistdownload"></a>DelayNavigationsForInitialSiteListDownload

  #### <a name="require-that-the-enterprise-mode-site-list-is-available-before-tab-navigation"></a>要求在索引標籤導覽前， [企業模式網站清單] 即已可使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  可讓您指定是否要讓 Microsoft Edge 索引標籤等待導覽，直到連覽器已下載初始的 [企業模式網站清單]。 這項設定適用於瀏覽器首頁應在 Internet Explorer 模式中載入的情況，在啟用 IE 模式之後，首次執行瀏覽器時，這是很重要的。 如果此情況不存在，我們建議您不要啟用這項設定，因為這可能會對載入首頁的效能造成負面影響。 只有在 Microsoft Edge 沒有 [快取的] 企業模式網站清單 (例如，在啟用 IE 模式後首次執行瀏覽器時才會使用) ，才會套用此設定。

此設定會與下列內容一併執行：[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode'，並設定 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中該清單至少擁有一個項目。

此原則的超時行為可以設定為 [ NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout) 原則。

如果您將此原則設定為 'All'，當 Microsoft Edge 沒有 [企業模式網站清單] 的快取版本時，索引標籤會延遲瀏覽直到瀏覽器完成下載網站清單為止。 在 Internet Explorer 模式中，由網站清單設定為開啟的網站將會在 Internet Explorer 模式中載入，即使在瀏覽器的首次瀏覽期間也是如此。 無法在 Internet Explorer 中設定開啟的網站，像是具有 [http:]、[https:]、[file:] 或 [ftp:] 的任何網站，都不會在 Microsoft Edge 中延遲導覽和立即載入。

如果您將此原則設定為 'None' 或未設定此原則，當 Microsoft Edge 沒有 [企業模式網站清單] 的快取版本時，索引標籤會立即導覽，而不會等候瀏覽器完成下載 [企業模式網站清單]。 由網站清單設定以 Internet Explorer 模式開啟的網站，將會以 Microsoft Edge 模式開啟直到瀏覽器完成下載 [企業模式網站清單] 為止。

原則選項對應：

* None (0) = 無

* All (1) = 所有符合條件的瀏覽

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DelayNavigationsForInitialSiteListDownload
  - GP 名稱：要求在索引標籤導覽前， [企業模式網站清單] 即已可使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DelayNavigationsForInitialSiteListDownload
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="deletedataonmigration"></a>DeleteDataOnMigration

  #### <a name="delete-old-browser-data-on-migration"></a>移轉時刪除舊版瀏覽器資料

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  此原則會決定在移轉到 Microsoft Edge 版本 81 或更新版本之後，是否會刪除來自 Microsoft Edge 舊版的使用者瀏覽資料。

如果將此原則設定為 [已啟用]，則在移轉到 Microsoft Edge 版本 81 或更新版本之後，所有來自 Microsoft Edge 舊版的瀏覽資料都會被刪除。 在移轉到 Microsoft Edge 版本 81 或更新版本之前，必須先設定此原則，才能對現有的瀏覽資料有任何作用。

如果將此原則設定為 [已停用] 或未設定原則，則在移轉到 Microsoft Edge 版本 83 或更新版本之後，將不會刪除使用者瀏覽資料。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DeleteDataOnMigration
  - GP 名稱：移轉時刪除舊版瀏覽器資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DeleteDataOnMigration
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="developertoolsavailability"></a>DeveloperToolsAvailability

  #### <a name="control-where-developer-tools-can-be-used"></a>控制可使用開發人員工具的位置

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制可使用開發人員工具的位置。

如果將此原則設定為 'DeveloperToolsDisallowedForForceInstalledExtensions' (預設值)，則使用者一般可以存取開發人員工具和 JavaScript 主控台，但無法存取透過企業原則安裝的擴充功能之內容。

如果將此原則設定為 'DeveloperToolsAllowed'，則使用者可以存取所有內容中的開發人員工具和 JavaScript 主控台，包括透過企業原則安裝的擴充功能。

如果將此原則設定為 'DeveloperToolsDisallowed'，則使用者無法存取開發人員工具或檢查網站元素。 開啟開發人員工具或 JavaScript 主控台的鍵盤快速鍵和功能表或內容功能表項目會停用。

原則選項對應：

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = 在企業原則安裝的擴充功能上封鎖開發人員工具，並在其他內容中允許

* DeveloperToolsAllowed (1) = 允許使用開發人員工具

* DeveloperToolsDisallowed (2) = 不允許使用開發人員工具

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DeveloperToolsAvailability
  - GP 名稱：控制可使用開發人員工具的位置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DeveloperToolsAvailability
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DeveloperToolsAvailability
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="diagnosticdata"></a>DiagnosticData

  #### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>傳送關於瀏覽器使用狀況的必要和選擇性診斷資料

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 7 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  此原則控制傳送有關瀏覽器使用狀況的必要和選擇性診斷資料給 Microsoft。

收集必要診斷資料，確保 Microsoft Edge 安全、保持最新狀態並按期望執行。

選擇性診斷資料包含有關如何使用瀏覽器的資料、您瀏覽的網站，以及針對產品和服務改善而向 Microsoft 發送當機報告。

Windows 10 裝置不支援此原則。 若要在 Windows 10 上控制這個資料收集，IT 系統管理員必須使用 Windows 診斷資料群組原則。 這項原則會是 '允許遙測' 或 '允許診斷資料'，視 Windows 版本而定。 深入了解 Windows 10 診斷資料收集：[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

使用下列其中一個設定來設定此原則：

'Off' 關閉必要和選擇性診斷資料收集。 不建議使用此選項。

'RequiredData' 傳送必要診斷資料，但關閉選擇性診斷資料收集。 Microsoft Edge 將傳送必要診斷資料，以確保 Microsoft Edge 安全、保持最新狀態並按期望執行。

'OptionalData' 傳送選擇性診斷資料，包含瀏覽器使用狀況、造訪的網站、針對產品和服務改善而向 Microsoft 發送當機報告。

在 Windows 7 和 macOS 上，此原則控制傳送必要和選擇性診斷資料給 Microsoft。

如果未設定或停用此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

原則選項對應：

* Off (0) = 關閉 (不建議使用)

* RequiredData (1) = 必要資料

* OptionalData (2) = 選擇性資料

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DiagnosticData
  - GP名稱：傳送關於瀏覽器使用狀況的必要和選擇性診斷資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DiagnosticData
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DiagnosticData
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="directinvokeenabled"></a>DirectInvokeEnabled

  #### <a name="allow-users-to-open-files-using-the-directinvoke-protocol"></a>允許使用者使用 DirectInvoke 通訊協定開啟檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  允許使用者使用 DirectInvoke 通訊協定來開啟檔案。 DirectInvoke 通訊協定會允許網站要求瀏覽器利用使用者電腦或裝置上的特定檔案處理常式從特定 URL 開啟檔案。

如果啟用或未設定此原則，則使用者可以使用 DirectInvoke 通訊協定來開啟檔案。

如果停用此原則，則使用者無法使用 DirectInvoke 通訊協定來開啟檔案。 檔案會改為儲存到檔案系統。

注意：停用 DirectInvoke 可能會使得某些 Microsoft SharePoint Online 功能無法如預期般運作。

如需 DirectInvoke 的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DirectInvokeEnabled
  - GP 名稱：允許使用者使用 DirectInvoke 通訊協定開啟檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DirectInvokeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="disable3dapis"></a>Disable3DAPIs

  #### <a name="disable-support-for-3d-graphics-apis"></a>停用 3D 圖形 API 支援

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  防止網頁存取圖形處理器 (GPU)。 具體來說，網頁無法存取 WebGL API，且外掛程式無法使用 Pepper 3D API。

如果未設定或停用此原則，則可能會允許網頁使用 WebGL API 和外掛程式使用 Pepper 3D API。 Microsoft Edge 預設可能仍需要傳遞命令列參數，才能使用這些 API。

如果 [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) 原則設定為 false，則會忽略 'Disable3DAPIs' 原則的設定，這相當於將 'Disable3DAPIs' 原則設定為 true。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：Disable3DAPIs
  - GP 名稱：停用 3D 圖形 API 支援
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：Disable3DAPIs
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：Disable3DAPIs
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="disablescreenshots"></a>DisableScreenshots

  #### <a name="disable-taking-screenshots"></a>停用取得螢幕擷取畫面功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制使用者是否可以取得瀏覽器頁面的螢幕擷取畫面。

如果已啟用，則使用者無法使用鍵盤快速鍵或擴充功能 API 來取得螢幕擷取畫面。

如果停用或未設定此原則，則使用者可以取得螢幕擷取畫面。

請注意，此原則會控制在瀏覽器本身內取得的螢幕擷取畫面。 即使您啟用此原則，使用者仍然可以使用瀏覽器以外的一些方法 (例如使用作業系統功能或其他應用程式) 來取得螢幕擷取畫面。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DisableScreenshots
  - GP 名稱：停用取得螢幕擷取畫面功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DisableScreenshots
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DisableScreenshots
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="diskcachedir"></a>DiskCacheDir

  #### <a name="set-disk-cache-directory"></a>設定磁碟快取目錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定用來儲存快取檔案的目錄。

如果啟用此原則，則 Microsoft Edge 會使用提供的目錄，而無論使用者是否已指定 '--disk-cache-dir' 旗標。 若要避免資料遺失或其他非預期的錯誤，請勿將此原則設定為磁碟區的根目錄或用於其他用途的目錄，因為 Microsoft Edge 會管理其內容。

如需可在指定目錄和路徑時使用的變數清單，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果未設定此原則，則會使用預設的快取目錄，且使用者可以使用 '--disk-cache-dir' 命令列旗標來覆寫該預設值。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DiskCacheDir
  - GP 名稱：設定磁碟快取目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DiskCacheDir
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"${user_home}/Edge_cache"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DiskCacheDir
  - 範例值：
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="diskcachesize"></a>DiskCacheSize

  #### <a name="set-disk-cache-size-in-bytes"></a>設定磁碟快取大小，以位元組為單位

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定用來在磁碟上儲存檔案的快取大小 (以位元組為單位)。

如果啟用此原則，則 Microsoft Edge 會使用提供的快取大小，而無論使用者是否已指定 '--disk-cache-size' 旗標。 此原則中指定的值不是硬性界限，而是對快取系統的建議；低於一些 MB 的任何值都太小，並將會進位為合理的最小值。

如果將此原則的值設為 0，則會使用預設的快取大小，且使用者無法變更。

如果未設定此原則，則會使用預設大小，但使用者可以使用 '--disk-cache-size' 旗標來覆寫它。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DiskCacheSize
  - GP 名稱：設定磁碟快取大小，以位元組為單位
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DiskCacheSize
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x06400000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DiskCacheSize
  - 範例值：
``` xml
<integer>104857600</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="dnsoverhttpsmode"></a>DnsOverHttpsMode

  #### <a name="control-the-mode-of-dns-over-https"></a>控制 DNS-over-HTTPS 模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  控制 DNS-over-HTTPS 解析程式的模式。 請注意，此原則只會設定每個查詢的預設模式。 可以針對特殊類型的查詢 (例如解析 DNS-over-HTTPS 伺服器主機名稱的要求) 覆寫此模式。

"off" 模式將會停用 DNS-over-HTTPS。

如果有可用的 DNS-over-HTTPS 伺服器，且可能會在發生錯誤時後援至傳送不安全的查詢，則 "automatic" 模式會優先傳送 DNS-over-HTTPS 查詢。

"secure" 模式將只會傳送 DNS-over-HTTPS 查詢，且發生錯誤時無法解析。

如果未設定此原則，則瀏覽器可能會將 DNS-over-HTTPS 要求傳送到與使用者設定的系統解析程式關聯的解析程式。

原則選項對應：

* 關閉 (off) = 停用 DNS-over-HTTPS

* 自動 (automatic) = 啟用具有不安全遞補的 DNS-over-HTTPS

* 安全 (secure) = 啟用沒有不安全遞補的 DNS-over-HTTPS

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DnsOverHttpsMode
  - GP 名稱：控制 DNS-over-HTTPS 模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DnsOverHttpsMode
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"off"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DnsOverHttpsMode
  - 範例值：
``` xml
<string>off</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="dnsoverhttpstemplates"></a>DnsOverHttpsTemplates

  #### <a name="specify-uri-template-of-desired-dns-over-https-resolver"></a>指定所需的 DNS-over-HTTPS 解析程式的 URI 範本

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  所需的 DNS-over-HTTPS 解析程式的 URI 範本。 若要指定多個 DNS-over-HTTPS 解析程式，請以空格分隔對應的 URI 範本。

如果將 [DnsOverHttpsMode](#dnsoverhttpsmode) 設定為 "secure"，則必須設定此原則，且不能為空白。

如果將 [DnsOverHttpsMode](#dnsoverhttpsmode) 設定為 "automatic"，並設定此原則，則會使用指定的 URI 範本。 如果未設定此原則，則會使用硬式編碼對應，嘗試將使用者目前的 DNS 解析程式升級至由相同提供者所運作的 DoH 解析程式。

如果 URI 範本包含 dns 變數，對解析程式的要求將會使用 GET；否則要求會使用 POST。

將忽略格式不正確的範本。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DnsOverHttpsTemplates
  - GP 名稱：指定所需的 DNS-over-HTTPS 解析程式的 URI 範本
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DnsOverHttpsTemplates
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://dns.example.net/dns-query{?dns}"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DnsOverHttpsTemplates
  - 範例值：
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="downloaddirectory"></a>DownloadDirectory

  #### <a name="set-download-directory"></a>設定下載目錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定下載檔案時要使用的目錄。

如果啟用此原則，則 Microsoft Edge 會使用提供的目錄，而無論使用者是否已指定一個目錄或選擇要每次收到下載位置的提示。 如需可使用的變數清單，請參閱[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果停用或未設定此原則，則會使用預設的下載目錄，且使用者可以變更它。

如果設定了無效路徑，Microsoft Edge 會預設為使用者的預設下載目錄。

如果路徑指定的資料夾不存在，則下載會觸發提示，詢問使用者想要儲存其下載項目的位置。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DownloadDirectory
  - GP 名稱：設定下載目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DownloadDirectory
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"\n      Linux-based OSes (including Mac): /home/${user_name}/Downloads\n      Windows: C:\\Users\\${user_name}\\Downloads"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DownloadDirectory
  - 範例值：
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="downloadrestrictions"></a>DownloadRestrictions

  #### <a name="allow-download-restrictions"></a>允許下載限制

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定 Microsoft Edge 完全封鎖的下載項目類型，而不讓使用者覆寫安全性決策。

設定 'BlockDangerousDownloads' 以允許所有下載項目，但帶有 Microsoft Defender SmartScreen 警告的下載項目除外。

設定 'BlockPotentiallyDangerousDownloads' 以允許所有下載項目，但帶有 Microsoft Defender SmartScreen 警告的潛在危險或有害下載項目除外。

設定 'BlockAllDownloads' 以封鎖所有下載項目。

如果未設定此原則或設定 'DefaultDownloadSecurity' 選項，則下載會根據 Microsoft Defender SmartScreen 分析結果，進行一般安全性限制檢查。

請注意，這些限制適用於來自網頁內容的下載項目，以及 [下載連結] 內容功能表選項。 這些限制不適用於儲存或下載目前顯示的頁面，也不適用來自列印選項的 [另存為 PDF] 選項。

如需 Microsoft Defender SmartScreen 的詳細資訊，請參閱[https://go.microsoft.com/fwlink/?linkid=2094934](https://go.microsoft.com/fwlink/?linkid=2094934)。

原則選項對應：

* DefaultDownloadSecurity (0) = 無特殊限制

* BlockDangerousDownloads (1) = 封鎖危險的下載項目

* BlockPotentiallyDangerousDownloads (2) = 封鎖有潛在危險或有害的下載項目

* BlockAllDownloads (3) = 封鎖所有下載項目。

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：DownloadRestrictions
  - GP 名稱：允許下載限制
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DownloadRestrictions
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：DownloadRestrictions
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="edgecollectionsenabled"></a>EdgeCollectionsEnabled

  #### <a name="enable-the-collections-feature"></a>啟用集錦功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  讓您允許使用者存取集錦功能，在其中，他們可以以更有效率的方式收集、整理、共用及匯出內容，並具有 Office 整合。

如果啟用或未設定此原則，則使用者可以在 Microsoft Edge 中存取並使用集錦功能。

如果停用此原則，則使用者無法在 Microsoft Edge 中存取及使用集錦。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EdgeCollectionsEnabled
  - GP 名稱：啟用集錦功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EdgeCollectionsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EdgeCollectionsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="edgeshoppingassistantenabled"></a>EdgeShoppingAssistantEnabled

  #### <a name="shopping-in-microsoft-edge-enabled"></a>已啟用在 Microsoft Edge 中購物

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 87 或更新版本

  #### <a name="description"></a>說明

  此原則允許使用者比較他們正在尋找的產品價格，從其所在網站上取得優待券或回贈、自動申請優惠券，以及使用自動填寫資料協助，以更快速地結帳。

如果您啟用或未設定此原則，將針對零售網域自動套用價格比較、優待券、回贈和快速結帳等等購物功能。 將從伺服器擷取目前零售商的優待券和其他零售商的價格。

如果您停用此原則，將不會針對零售網域自動發現價格比較、優待券、回贈和快速結帳等等購物功能。

從版本 90.0.818.56 開始，傳訊行為會讓使用者知道購物網域有可用的優待券、回饋、價格比較或價格記錄，也會透過網址列下方的水平橫幅廣告完成。 此訊息先前是在網址列上完成。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EdgeShoppingAssistantEnabled
  - GP 名稱：已啟用在 Microsoft Edge 中購物
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：EdgeShoppingAssistantEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EdgeShoppingAssistantEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="editfavoritesenabled"></a>EditFavoritesEnabled

  #### <a name="allows-users-to-edit-favorites"></a>允許使用者編輯我的最愛

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用此原則可讓使用者新增、移除及修改我的最愛。 如果未設定此原則，則這是預設行為。

停用此原則可讓使用者無法新增、移除或修改我的最愛。 他們仍可以使用現有的我的最愛。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EditFavoritesEnabled
  - GP 名稱：允許使用者編輯我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EditFavoritesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EditFavoritesEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enabledeprecatedwebplatformfeatures"></a>EnableDeprecatedWebPlatformFeatures

  #### <a name="re-enable-deprecated-web-platform-features-for-a-limited-time-obsolete"></a>在限定時間內重新啟用已過時的網頁平台功能 (過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 86 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 86

  #### <a name="description"></a>描述

  這項原則已過時，因為現在使用私人網路頁平臺原則來管理個別網頁平臺功能 deprecations。

指定要暫時重新啟用的已過時網頁平台功能清單。

此原則可讓您在限定時間內重新啟用已過時的網頁平台功能。 功能會依字串標籤來識別。

如果未設定此原則，如果清單為空白，或如果功能不符合支援的其中一個字串標籤，則所有過時的網頁平台功能會保持停用。

雖然上述平台上支援原則本身，它要啟用的功能可能無法在這所有平台上使用。 並非所有過時的網頁平台功能都可以重新啟用。 只有下列明確列出的項目才可以重新啟用，且僅限於有限的一段時間，這會因每個功能而不同。 您可以在 https://bit.ly/blinkintents 檢閱網頁平台功能變更的背後意圖。

字串標籤的一般格式為 [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd]。

原則選項對應：

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = 啟用 ExampleDeprecatedFeature API 到 2008 年 9 月 2 日

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableDeprecatedWebPlatformFeatures
  - GP 名稱：在限定時間內重新啟用已過時的網頁平台功能 (過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = "ExampleDeprecatedFeature_EffectiveUntil20080902"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableDeprecatedWebPlatformFeatures
  - 範例值：
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enabledomainactionsdownload"></a>EnableDomainActionsDownload

  #### <a name="enable-domain-actions-download-from-microsoft-obsolete"></a>啟用從 Microsoft 進行網域動作下載 (已過時) 

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - 在 Windows 和 macOS 上，版本 77 到 84

  #### <a name="description"></a>描述

  這個原則無法使用，應避免衝突的狀態。 此原則原是用以啟用/停用網域動作清單的下載，但它並不一定能達到所需的狀態。 處理下載的實驗和設定服務擁有自己的群組原則，可設定從服務下載的內容。 請改為使用 [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) 原則。

在 Microsoft Edge 中，網域動作代表可協助瀏覽器在網路上正常運作的一系列相容性功能。

Microsoft 會基於相容性原因，保留對特定網域採取的動作清單。 例如，如果網站因為 Microsoft Edge 上的新使用者代理字串而損毀，則瀏覽器可能會覆寫網站上的使用者代理程式字串。 這些動作都是 Microsoft 嘗試解決網站擁有者的問題時的暫時性動作。

當瀏覽器啟動，然後之後定期啟動時，瀏覽器將會與包含要執行的最新相容性動作清單的實驗和設定服務連絡。 此清單會在初次擷取之後儲存在本機，以便後續的要求只會在伺服器的複本變更之後才更新該清單。

如果啟用此原則，則會繼續透過實驗和設定服務下載網域動作的清單。

如果停用此原則，則不再會透過實驗和設定服務下載網域動作的清單。

如果未設定此原則，則會繼續透過實驗和設定服務下載網域動作的清單。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableDomainActionsDownload
  - GP 名稱：啟用從 Microsoft 進行網域動作下載 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableDomainActionsDownload
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableDomainActionsDownload
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enableonlinerevocationchecks"></a>EnableOnlineRevocationChecks

  #### <a name="enable-online-ocspcrl-checks"></a>啟用線上 OCSP/CRL 檢查

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  線上撤銷檢查不會提供顯著的安全性優點，而且預設為停用。

如果啟用此原則，則 Microsoft Edge 將會執行非封鎖性失敗的線上 OCSP/CRL 檢查。 「非封鎖性失敗」表示如果無法連接撤銷伺服器，則會將憑證視為有效。

如果停用或未設定此原則，則 Microsoft Edge 不會執行線上撤銷檢查。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableOnlineRevocationChecks
  - GP 名稱：啟用線上 OCSP/CRL 檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableOnlineRevocationChecks
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableOnlineRevocationChecks
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enablesha1forlocalanchors"></a>EnableSha1ForLocalAnchors

  #### <a name="allow-certificates-signed-using-sha-1-when-issued-by-local-trust-anchors-obsolete"></a>允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 91 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 至 91

  #### <a name="description"></a>說明

  啟用此設定時，只要憑證連結接到本機安裝的根憑證，Microsoft Edge 就能以 SHA-1 簽署的憑證來保護您的連線，而這是有效的。

請注意，此原則視允許 SHA-1 簽名的作業系統 (OS) 憑證驗證堆疊而定。 如果 OS 更新變更了 SHA-1 憑證的 OS 處理，可能會導致這個原則沒有作用。  此外，此原則旨在為企業提供更多時間來擺脫 SHA-1，以做為暫時的因應措施。 這項原則將會在 2021 年中旬的 Microsoft Edge 92 中被移除。

如果您未設定此原則或將其設為 False，或將 SHA-1 憑證連結到公開信任的憑證根，Microsoft Edge 將不允許 SHA-1 簽署的憑證。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnableSha1ForLocalAnchors
  - GP 名稱：允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：EnableSha1ForLocalAnchors
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnableSha1ForLocalAnchors
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enterprisehardwareplatformapienabled"></a>EnterpriseHardwarePlatformAPIEnabled

  #### <a name="allow-managed-extensions-to-use-the-enterprise-hardware-platform-api"></a>允許受管擴充功能使用企業硬體平台 API

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  當此原則設定為已啟用時，即會允許由企業原則安裝的擴充功能，以使用企業硬體平台 API。
當此原則設定為已停用或未設定時，則不會允許任何擴充功能使用企業硬體平台 API。
此原則也適用於元件擴充功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnterpriseHardwarePlatformAPIEnabled
  - GP 名稱：允許受管擴充功能使用企業硬體平台 API
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnterpriseHardwarePlatformAPIEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：EnterpriseHardwarePlatformAPIEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="enterprisemodesitelistmanagerallowed"></a>EnterpriseModeSiteListManagerAllowed

  #### <a name="allow-access-to-the-enterprise-mode-site-list-manager-tool"></a>允許存取 Enterprise Mode Site List Manager 工具

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  可讓您設定 Enterprise Mode Site List Manager 是否可供使用者使用。

如果啟用這項原則，使用者會在 edge://compat 頁面上看到 [Enterprise Mode Site List Manager] 瀏覽按鈕，瀏覽至該工具並加以使用。

如果停用或未設定此原則，則使用者不會看到 [Enterprise Mode Site List Manager] 瀏覽按鈕，也無法使用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：EnterpriseModeSiteListManagerAllowed
  - GP 名稱：允許存取 Enterprise Mode Site List Manager 工具
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：EnterpriseModeSiteListManagerAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="exemptdomainfiletypepairsfromfiletypedownloadwarnings"></a>ExemptDomainFileTypePairsFromFileTypeDownloadWarnings

  #### <a name="disable-download-file-type-extension-based-warnings-for-specified-file-types-on-domains"></a>針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  您可以啟用此原則以建立一份檔案類型副檔名字典，及相對應的網域清單，可使這些檔案不受使用檔案類型副檔名的下載警告。 這可讓企業系統管理員封鎖與所列網域相關聯之檔案的檔案類型副檔名下載警告。 例如，如果「jnlp」副檔名與「website1.com」相關聯，使用者在從「website1.com」下載「jnlp」檔案時就不會看到警示訊息，但在從　「website2.com」下載「jnlp」檔案時就會看到下載警示訊息。

凡是檔案具有以此原則指定網域的檔案類型副檔名，仍受限於非檔案類型副檔名的安全性警告，例如混合式內容下載警示和 Microsoft Defender SmartScreen 的警示。

若您停用或未設定此原則，凡具有觸發以副檔名為依據的下載警示的檔案會向使用者顯示警示訊息。

如果啟用此原則：

* URL 模式的格式應依照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)設定。
* 輸入的檔案類型副檔名必須是小寫的 ASCII。 在列出檔案類型副檔名時，不應包含前置分隔符號，因此請列出「jnlp」，而不是「.jnlp」。

範例：

下列範例數值可以防止 [contoso.com] 網域的 [swf]、[exe] 和 [jnlp 副檔名] 的檔案類型副檔名下載警示。 它會在任何適於 exe 和 jnlp 檔案的其他網域中顯示使用者的檔案類型副檔名下載警示，但不適用於 swf 檔案。

[ { "file_extension": "jnlp", "domains": ["contoso.com"] }, { "file_extension": "exe", "domains": ["contoso.com"] }, { "file_extension": "swf", "domains": ["*"] } ]

請注意，在以上範例中，雖然所有網域中的 [swf] 檔案禁止顯示檔案類型副檔名式下載警告，但由於安全性方面的問題考量，不建議您在任何危險的檔案類型副檔名上顯示這些警告。 此範例僅顯示了執行此動作的功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP 名稱：針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {"file_extension": "jnlp", "domains": ["https://contoso.com", "contoso2.com"]}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {"file_extension": "swf", "domains": ["*"]}

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 範例值：
``` xml
<array>
  <string>{'file_extension': 'jnlp', 'domains': ['https://contoso.com', 'contoso2.com']}</string>
  <string>{'file_extension': 'swf', 'domains': ['*']}</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="experimentationandconfigurationservicecontrol"></a>ExperimentationAndConfigurationServiceControl

  #### <a name="control-communication-with-the-experimentation-and-configuration-service"></a>控制與實驗和設定服務的通訊

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 中，會使用實驗和設定服務來部署實驗和設定承載。

實驗承載是由 Microsoft 為測試和意見反應所啟用的開發功能的早期清單所組成。

設定承載包含 Microsoft 要部署到 Microsoft Edge 以最佳化使用者體驗的設定清單。 例如，設定承載可指定 Microsoft Edge 傳送要求到實驗和設定服務以取得最新承載的頻率。

此外，設定承載可能也包含基於相容性原因，要在特定網域上採取之動作的清單。 例如，如果網站因為 Microsoft Edge 上的新使用者代理字串而損毀，則瀏覽器可能會覆寫網站上的使用者代理程式字串。 這些動作都是 Microsoft 嘗試解決網站擁有者的問題時的暫時性動作。

如果將此原則設定為 'FullMode'，則會透過實驗和設定服務下載完整承載。 這同時包括實驗和設定承載。

如果將此原則設定為 'ConfigurationsOnlyMode'，則只會傳遞設定承載。

如果將此原則設定為 'RestrictedMode’，就會完全停止與實驗和設定服務的通訊。

如果未設定此原則，則在穩定和 Beta 版通道的受管理裝置上，其行為與 'ConfigurationsOnlyMode' 相同。

如果未設定此原則，則在未受管理的裝置上，其行為與 'FullMode' 相同。

原則選項對應：

* FullMode (2) = 擷取設定和實驗

* ConfigurationsOnlyMode (1) = 僅擷取設定

* RestrictedMode (0) = 停用與實驗和設定服務的通訊

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExperimentationAndConfigurationServiceControl
  - GP 名稱：控制與實驗和設定服務的通訊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExperimentationAndConfigurationServiceControl
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExperimentationAndConfigurationServiceControl
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="explicitlyallowednetworkports"></a>ExplicitlyAllowedNetworkPorts

  #### <a name="explicitly-allowed-network-ports"></a>明確允許的網路連接埠

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 91 或更新版本

  #### <a name="description"></a>說明

  此原則允許繞過 Microsoft Edge 內建的受限制連接埠清單。 埠組定義為逗號分隔清單，允許其進行連出連接。

連接埠受到限制，以防止使用 Microsoft Edge 做為利用各種網路弱點的媒介。 設定此原則可能會讓您的網路遭到攻擊。 此原則是當將封鎖連接埠上執行的服務移至標準連接埠 (例如連接埠 80 或 443) 時，錯誤碼 "ERR_UNSAFE_PORT" 的暫時解決方法。

惡意網站可以輕鬆地偵測到已設定此原則，以及哪些連接埠設定該原則，然後使用該資訊來鎖定攻擊。

將數值留白或取消設定，表示所有受限制的連接埠都會被封鎖。 透過此原則所設定的不正確埠值會被忽略，而有效的埠值仍然會繼續套用。

此原則會覆寫 "--explicitly-allowed-ports" 命令列選項。

原則選項對應：

* 554 (554) = 連接埠 554 (2021/10/15 到期)

* 10080 (10080) = 連接埠 10080 (2022/04/01 到期)

* 6566 (6566) = 連接埠 6566 (2021/10/15 到期)

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExplicitlyAllowedNetworkPorts
  - GP 名稱：明確允許的網路連接埠
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)： SOFTWARE\Policies\Microsoft\Edge\ExplicitlyAllowedNetworkPorts
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ExplicitlyAllowedNetworkPorts\1 = "10080"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExplicitlyAllowedNetworkPorts
  - 範例值：
``` xml
<array>
  <string>10080</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="externalprotocoldialogshowalwaysopencheckbox"></a>ExternalProtocolDialogShowAlwaysOpenCheckbox

  #### <a name="show-an-always-open-checkbox-in-external-protocol-dialog"></a>在外部通訊協定對話方塊中顯示「一律開啟」核取方塊

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  此原則會控制是否要在外部通訊協定啟動確認提示中顯示 [一律允許此網站開啟這類連結] 核取方塊。 這個原則只適用於 https:// 連結。

如果啟用此原則，當外部通訊協定提示顯示時，使用者可以選取 [一律允許]，以在此網站上略過該通訊協定的所有未來確認提示。

如果停用此原則，則不會顯示 [一律允許] 核取方塊。 每次呼叫外部通訊協定時，都會提示使用者進行確認。

在 Microsoft Edge 83 之前，如果您未設定此原則，則不會顯示 [永遠允許] 核取方塊。 每次呼叫外部通訊協定時，都會提示使用者進行確認。

在 Microsoft Edge 83 上，如果未設定此原則，則核取方塊可見度會由 edge://flags 中的 [啟用記憶通訊協定啟動提示喜好設定] 旗標控制

截至 Microsoft Edge 84，如果不啟用此原則，當外部通訊協定確認提示顯示時，使用者可以選取 [一律允許]，以在此網站上略過該通訊協定的所有未來確認提示。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP 名稱：在外部通訊協定對話方塊中顯示 [一律開啟] 核取方塊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="familysafetysettingsenabled"></a>FamilySafetySettingsEnabled

  #### <a name="allow-users-to-configure-family-safety-and-kids-mode"></a>允許使用者設定家庭安全與兒童模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  此原則會停用瀏覽器中的兩項家庭安全相關功能。 這會隱藏 [設定] 中的 [家庭] 頁面，且會封鎖瀏覽至 edge://settings/family。 家庭設定頁面說明使用 Microsoft Family Safety 的家庭群組提供哪些功能。 在這裡深入了解家庭安全：([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432))。 從 Microsoft Edge 90 開始，此原則也會停用兒童模式，這是一種具有自訂主題的兒童瀏覽模式，且允許需要裝置密碼才能離開的清單瀏覽。 在這裡深入了解兒童模式：([https://go.microsoft.com/fwlink/?linkid=2146910](https://go.microsoft.com/fwlink/?linkid=2146910))

如果您啟用或未設定此原則，則系統將會顯示設定中的家庭頁面，且兒童模式可供使用。

如果您停用此原則，系統將不會顯示家庭頁面，且會隱藏兒童模式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FamilySafetySettingsEnabled
  - GP 名稱：允許使用者設定家庭安全與兒童模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：FamilySafetySettingsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FamilySafetySettingsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="favoritesbarenabled"></a>FavoritesBarEnabled

  #### <a name="enable-favorites-bar"></a>啟用我的最愛列

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用或停用我的最愛列。

如果啟用此原則，則使用者會看到我的最愛列。

如果停用此原則，則使用者不會看到我的最愛列。

如果未設定此原則，則使用者可以決定是否使用我的最愛列。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FavoritesBarEnabled
  - GP 名稱：啟用我的最愛列
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：FavoritesBarEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：FavoritesBarEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="fetchkeepalivedurationsecondsonshutdown"></a>FetchKeepaliveDurationSecondsOnShutdown

  #### <a name="fetch-keepalive-duration-on-shutdown"></a>擷取關機時的存留持續時間

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  控制允許存留要求的持續時間 (秒)，以防止瀏覽器完成其關機。

如果您設定此原則，瀏覽器將在處理任何未完成的存留要求時封鎖完成關機 (請參閱 https://fetch.spec.whatwg.org/#request-keepalive-flag) 此原則所指定的最長期間。)

如果您停用或沒有設定此原則，則會使用預設值 0 秒，而在瀏覽器關閉期間，會立即取消未處理存留要求。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FetchKeepaliveDurationSecondsOnShutdown
  - GP 名稱：擷取關機時的存留持續時間
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：FetchKeepaliveDurationSecondsOnShutdown
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定金鑰名稱：FetchKeepaliveDurationSecondsOnShutdown
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcebingsafesearch"></a>ForceBingSafeSearch

  #### <a name="enforce-bing-safesearch"></a>強制執行 Bing 安全搜尋

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  確認 Bing Web 搜尋中的查詢是在將安全搜尋設定為指定值的情況下完成。 使用者無法變更此設定。

如果將此原則設定為 'BingSafeSearchNoRestrictionsMode'，則「Bing 搜尋中的安全搜尋」會後援至 bing.com 值。

如果將此原則設定為 'BingSafeSearchModerateMode'，則會在安全搜尋中使用中等設定。 中等設定會篩選成人影片和影像，但不會篩選搜尋結果中的文字。

如果將此原則設定為 'BingSafeSearchStrictMode'，則會在安全搜尋中使用嚴格設定。 嚴格設定會篩選成人文字、影像和影片。

如果停用或不設定此原則，則「Bing 搜尋中的安全搜尋」不會強制執行，而使用者可以在 bing.com 上設定他們需要的值。

原則選項對應：

* BingSafeSearchNoRestrictionsMode (0) = 不要在 Bing 中設定搜尋限制

* BingSafeSearchModerateMode (1) = 在 Bing 中設定中等搜尋限制

* BingSafeSearchStrictMode (2) = 在 Bing 中設定嚴格搜尋限制

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceBingSafeSearch
  - GP 名稱：強制執行 Bing 安全搜尋
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceBingSafeSearch
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceBingSafeSearch
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcecertificatepromptsonmultiplematches"></a>ForceCertificatePromptsOnMultipleMatches

  #### <a name="configure-whether-microsoft-edge-should-automatically-select-a-certificate-when-there-are-multiple-certificate-matches-for-a-site-configured-with-autoselectcertificateforurls"></a>設定使用 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，Microsoft Edge 是否應自動選取憑證

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  切換有多個憑證可用且使用 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 設定網站時，是否提示使用者選取憑證。 如果未針對網站設定 [AutoSelectCertificateForUrls](#autoselectcertificateforurls)，則一律會提示使用者選取憑證。

如果將此原則設定為 True，則在有多個憑證時 (且僅在此情況下)，Microsoft Edge 會提示使用者針對 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 定義的清單上的網站選取憑證。

如果將此原則設定為 False 或未設定，即使有憑證的多個相符項目，Microsoft Edge 也會自動選取憑證。 針對在 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 所定義清單中的網站，系統不會提示使用者選取憑證。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceCertificatePromptsOnMultipleMatches
  - GP 名稱：設定以 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，是否應自動選取憑證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceCertificatePromptsOnMultipleMatches
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceCertificatePromptsOnMultipleMatches
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forceephemeralprofiles"></a>ForceEphemeralProfiles

  #### <a name="enable-use-of-ephemeral-profiles"></a>啟用使用暫時設定檔

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制使用者設定檔是否切換為暫時模式。 暫時設定檔會在工作階段開始時建立，並在工作階段結束時刪除，且與使用者的原始設定檔相關聯。

如果啟用此原則，則設定檔會在暫時模式中執行。 這可讓使用者透過自己的裝置工作，而不需要將瀏覽資料儲存到這些裝置。 如果將此原則啟用為 OS 原則 (例如，在 Windows 上使用 GPO)，則它會套用至系統上的每個設定檔。

如果停用或未設定此原則，則使用者會在登入瀏覽器時取得一般的設定檔。

在暫時模式中，設定檔資料只會在該使用者工作階段期間儲存在磁碟上。 瀏覽器歷程記錄、擴充功能及其資料、Web 資料 (如 Cookie)，以及 Web 資料庫等功能，不會於瀏覽器關閉之後儲存。 這不會防止使用者手動將任何資料下載到磁碟，或是儲存頁面或列印頁面。 如果使用者已啟用同步，則會如同一般設定檔的方式，將所有資料保留在其同步帳戶中。 使用者也可以在暫時模式中使用 InPrivate 瀏覽，除非您明確地將它停用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceEphemeralProfiles
  - GP 名稱：啟用使用暫時設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceEphemeralProfiles
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceEphemeralProfiles
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcegooglesafesearch"></a>ForceGoogleSafeSearch

  #### <a name="enforce-google-safesearch"></a>強制執行 Google 安全搜尋

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  強制在 Google Web Search 中的查詢執行時將安全搜尋設為作用中，並防止使用者變更此設定。

如果啟用此原則，則 Google 搜尋中的安全搜尋一律會是作用中。

如果停用或未設定此原則，則不會在 Google 搜尋中強制執行安全搜尋。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceGoogleSafeSearch
  - GP 名稱：強制執行 Google 安全搜尋
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceGoogleSafeSearch
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceGoogleSafeSearch
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcelegacydefaultreferrerpolicy"></a>ForceLegacyDefaultReferrerPolicy

  #### <a name="use-a-default-referrer-policy-of-no-referrer-when-downgrade-obsolete"></a>使用預設的查閱者原則 no-referrer-when-downgrade (已淘汰)

  
  >已過時：此原則已過時且無法在 Microsoft Edge 88 之後運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 至 88

  #### <a name="description"></a>描述

  此原則無法運作，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與新預設的查閱者原則不一致時，可以有更多時間來更新其 Web 內容。

Microsoft Edge 的預設查閱者原則得到強化，從其目前的 no-referrer-when-downgrade 值到更安全的 strict-origin-when-cross-origin。

啟用此企業原則後，會將 Microsoft Edge 的預設查閱者原則設定為其舊值 no-referrer-when-downgrade。

此企業原則預設會停用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceLegacyDefaultReferrerPolicy
  - GP 名稱：使用預設的查閱者原則 no-referrer-when-downgrade (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceLegacyDefaultReferrerPolicy
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceLegacyDefaultReferrerPolicy
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcenetworkinprocess"></a>ForceNetworkInProcess

  #### <a name="force-networking-code-to-run-in-the-browser-process-obsolete"></a>強制網路程式碼在瀏覽器處理程序中執行 (已過時) 

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 83 及之後版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 至 83

  #### <a name="description"></a>描述

  此原則已遭取代，因為其只是一種短期機制，目的是要讓企業有更多時間可遷移到不依賴於使用網路 API 的第 3 方軟體。 建議透過 LSP 和 WIN32 API 修補來使用 Proxy 伺服器。

此原則會強制在瀏覽器處理程序中執行網路程式碼。

此原則預設為停用。 如果啟用，當網路處理程序在沙盒中執行時，使用者會面臨安全性問題。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceNetworkInProcess
  - GP 名稱：GP 名稱：強制網路程式碼在瀏覽器處理程序中執行 (已淘汰) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceNetworkInProcess
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forcesync"></a>ForceSync

  #### <a name="force-synchronization-of-browser-data-and-do-not-show-the-sync-consent-prompt"></a>強制同步處理瀏覽器資料，且不顯示同步同意提示

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  Microsoft Edge 中的強制執行資料同步處理。 這個原則也可以防止使用者關閉同步處理。

如果您未設定此原則，使用者將可以開啟或關閉同步。 如果您啟用此原則，使用者將無法關閉同步。

若要讓此原則能夠正常運作，不可設定 [BrowserSignin](#browsersignin) 原則，或必須設定為啟用。 如果將 [BrowserSignin](#browsersignin) 設為停用，則 [ForceSync](#forcesync) 將不會生效。

不可設定 [SyncDisabled](#syncdisabled)，或必須設定為 False。 如果將此原則設為 True，則 [ForceSync](#forcesync) 將不會生效。

0 = 不會自動開始同步處理及顯示同步同意 (預設值) 1 = 針對 Azure AD/Azure AD-Degraded 的使用者設定檔開啟強制同步處理，且不會顯示同步同意提示

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceSync
  - GP 唯一名稱：強制同步處理瀏覽器資料，且不顯示同步同意提示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceSync
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceSync
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="forceyoutuberestrict"></a>ForceYouTubeRestrict

  #### <a name="force-minimum-youtube-restricted-mode"></a>強制最小 YouTube 限制模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 YouTube 上強制執行最小限制模式，並防止使用者選取較不受限制的模式。

設定為 '嚴格' ，強制在 YouTube 上使用嚴格限制模式。

設定為 '中等'，強制使用者只能在 YouTube 上使用中等限制模式和嚴格限制模式。 他們無法停用限制模式。

設定為 '關閉' 或不設定此原則，以不要在 YouTube 上強制執行限制模式。 YouTube 原則等外部原則可能仍會強制執行限制模式。

原則選項對應：

* 關閉 (0) = 不要在 YouTube 上強制執行限制模式

* 中等 (1) = 強制在 YouTube 上至少使用中等限制模式

* 嚴格 (2) = 針對 YouTube 強制使用嚴格限制模式

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ForceYouTubeRestrict
  - GP 名稱：強制最小 YouTube 限制模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceYouTubeRestrict
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ForceYouTubeRestrict
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="fullscreenallowed"></a>FullscreenAllowed

  #### <a name="allow-full-screen-mode"></a>允許全螢幕模式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定全螢幕模式的可用性 - 所有 Microsoft Edge UI 都會隱藏，且只會顯示網頁內容。

如果啟用此原則或未設定，則擁有適當權限的使用者、應用程式和擴充功能即可以進入全螢幕模式。

如果停用此原則，則使用者、應用程式和擴充功能無法進入全螢幕模式。

停用全螢幕模式時，無法使用命令列在 kiosk 模式中開啟 Microsoft Edge。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：FullscreenAllowed
  - GP 名稱：允許全螢幕模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：FullscreenAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="globallyscopehttpauthcacheenabled"></a>GloballyScopeHTTPAuthCacheEnabled

  #### <a name="enable-globally-scoped-http-auth-cache"></a>啟用全域範圍的 HTTP 驗證快取

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  此原則會使用 HTTP 伺服器驗證認證來根據每個設定檔快取設定單一全域範圍。

如果停用或未設定此原則，則瀏覽器將會使用跨網站驗證的預設行為，於版本 80 開始時，將由熱門網站限定在 HTTP 伺服器驗證認證。 因此，如果兩個網站使用來自相同驗證網域的資源，就必須在這兩個網站的環境中個別提供認證。 快取的 Proxy 認證會跨網站重複使用。

如果啟用此原則，則在一個網站內容中輸入的 HTTP 驗證認證，將會自動用於另一個網站內容。

啟用此原則會使得網站遭受某種類型的跨網站攻擊，並允許跨網站追蹤使用者 (甚至是在沒有 Cookie 的情況下)，方法是使用內嵌在 URL 中的身分認證將項目新增至 HTTP 驗證快取。

此原則目的在讓基於舊版行為的企業有機會更新其登入程序，並將在未來移除。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：GloballyScopeHTTPAuthCacheEnabled
  - GP 名稱：啟用全域範圍的 HTTP 驗證快取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：GloballyScopeHTTPAuthCacheEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：GloballyScopeHTTPAuthCacheEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="gotointranetsiteforsinglewordentryinaddressbar"></a>GoToIntranetSiteForSingleWordEntryInAddressBar

  #### <a name="force-direct-intranet-site-navigation-instead-of-searching-on-single-word-entries-in-the-address-bar"></a>強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則，如果在網址列中輸入的文字是不帶標點符號的單一字詞，則網址列建議清單中最上方的自動建議結果會導覽至內部網路網站。

輸入不帶標點符號的文字時，預設的導覽會是導覽至符合所輸入文字的內部網路網站。

如果啟用此原則，網址列建議清單中的第二個自動建議結果會完全按照所輸入的單字來執行網頁搜尋，前提是此文字為不帶標點符號的單一字詞。 將使用預設的搜尋提供者，除非也啟用防止網頁搜尋的原則。

啟用此原則的兩個影響如下：

瀏覽至網站以回應一般會解析為歷程記錄項目的單一文字查詢功能將不再發生。 相反地，瀏覽器會嘗試巡覽至可能不存在組織內部網路中的內部網站。 這會導致 404 錯誤。

熱門、單一文字搜尋字詞將需要手動選取搜尋建議，才能正確執行搜尋。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP 名稱：強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="hstspolicybypasslist"></a>HSTSPolicyBypassList

  #### <a name="configure-the-list-of-names-that-will-bypass-the-hsts-policy-check"></a>設定會略過 HSTS 原則檢查的名稱清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  設定此原則會指定主機名稱清單，這些主機名稱會忽略從 http 到 https 的預先載入 HSTS 升級。

此原則只允許單一標籤主機名稱，且此原則僅適用於靜態 HSTS 預先載入項目 (例如，"app"、"new"、"search"、"play")。 此原則不會防止使用 Strict-Transport-Security 回應標頭動態要求 HSTS 升級的伺服器進行 HSTS 升級。

提供的主機名稱必須經過規範：任何 IDN 都必須轉換成其 A 標籤格式，而且所有 ASCII 字母都必須是小寫。 此原則僅適用於指定的特定單一標籤主機名稱，而非這些名稱的子網域。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HSTSPolicyBypassList
  - GP 名稱：設定會略過 HSTS 原則檢查的名稱清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = "meet"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HSTSPolicyBypassList
  - 範例值：
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="hardwareaccelerationmodeenabled"></a>HardwareAccelerationModeEnabled

  #### <a name="use-hardware-acceleration-when-available"></a>可用時便使用硬體加速

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定是否要使用硬體加速 (如果有的話)。 如果啟用此原則或未設定，除非明確封鎖 GPU 功能，否則會啟用硬體加速。

如果停用此原則，則會停用硬體加速。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HardwareAccelerationModeEnabled
  - GP 名稱：可用時便使用硬體加速
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HardwareAccelerationModeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HardwareAccelerationModeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="headlessmodeenabled"></a>HeadlessModeEnabled

  #### <a name="control-use-of-the-headless-mode"></a>控制無周邊模式的使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  此原則設定可讓您決定使用者是否可以在無周邊模式下啟動 Microsoft Edge。

如果您啟用或沒有設定此原則，Microsoft Edge 會允許使用無周邊模式。

如果您停用此原則，Microsoft Edge 會拒絕使用無周邊模式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HeadlessModeEnabled
  - GP 名稱：控制無周邊模式的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HeadlessModeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HeadlessModeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="hidefirstrunexperience"></a>HideFirstRunExperience

  #### <a name="hide-the-first-run-experience-and-splash-screen"></a>隱藏初次執行體驗與啟動顯示畫面

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則，則當使用者初次執行 Microsoft Edge 時，不會向使用者顯示初次執行體驗與啟動顯示畫面。

針對初次執行體驗中顯示的設定選項，瀏覽器將會預設為下列項目：

- 在 [新索引標籤] 頁面上，摘要類型將設定為 MSN 新聞，而版面配置為 [佈景]。

- 如果 Windows 帳戶屬於 Azure AD 或 MSA 類型，則使用者仍會自動登入 Microsoft Edge。

-預設將不會啟用同步，且系統會提示使用者選擇是否要在瀏覽器啟動時同步。 您可以使用 [ForceSync](#forcesync) 或 [SyncDisabled](#syncdisabled) 原則來設定同步和同步同意提示。

如果停用或未設定此原則，則會顯示初次執行體驗和啟動顯示畫面。

注意：在初次執行體驗中向使用者顯示的特定設定選項，也可以使用其他特定原則來管理。 您可以使用 HideFirstRunExperience 原則結合這些原則，以在受管理的裝置上設定特定的瀏覽器體驗。 其他原則中的一部分為：

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[ForceSync](#forcesync)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HideFirstRunExperience
  - GP 名稱：隱藏初次執行體驗與啟動顯示畫面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HideFirstRunExperience
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：HideFirstRunExperience
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="hideinternetexplorerredirectuxforincompatiblesitesenabled"></a>HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

  #### <a name="hide-the-one-time-redirection-dialog-and-the-banner-on-microsoft-edge"></a>隱藏一次性的重新導向對話方塊和 Microsoft Edge 上的橫幅

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  此原則可讓您選擇停用一次性重新導向對話方塊和橫幅。 啟用此原則時，使用者不會看到一次性對話方塊和橫幅。
當使用者在 Internet Explorer 上遇到不相容的網站時，系統會繼續將使用者重新導向至 Microsoft Edge，但不會匯入其瀏覽資料。

- 如果您啟用此原則，則永遠不會向使用者顯示一次性重新導向對話方塊和橫幅。 發生重新導向時，不會匯入使用者的瀏覽資料。

- 如果您停用或未設定此原則，重新導向對話方塊會在第一次重新導向時顯示，並會在從重新導向開始的工作階段，向使用者顯示持續性重新導向橫幅。 每次使用者遇到這種重新導向時，都會匯入使用者的瀏覽資料 (僅於使用者在一次性對話方塊中同意時才適用)。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - GP 名稱：隱藏一次性的重新導向對話方塊和 Microsoft Edge 上的橫幅
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HideInternetExplorerRedirectUXForIncompatibleSitesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importautofillformdata"></a>ImportAutofillFormData

  #### <a name="allow-importing-of-autofill-form-data"></a>允許匯入自動填寫表單資料

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將自動填寫表單資料匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入自動填寫資料的選項。

如果停用此原則，則自動填寫表單資料不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入自動填寫資料，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入自動填寫資料，但是使用者可以在手動匯入期間選取或清除 [自動填寫資料]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 和 Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 瀏覽器的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportAutofillFormData
  - GP 名稱：允許匯入自動填寫表單資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportAutofillFormData
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportAutofillFormData
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importbrowsersettings"></a>ImportBrowserSettings

  #### <a name="allow-importing-of-browser-settings"></a>允許匯入瀏覽器設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將瀏覽器設定匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [瀏覽器設定]**** 核取方塊。

如果停用此原則，則瀏覽器設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入瀏覽器設定，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入設定，但使用者可以在手動匯入期間選取或清除 [瀏覽器設定]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (Windows 7、8 和 10 上，以及 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportBrowserSettings
  - GP 名稱：允許匯入瀏覽器設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportBrowserSettings
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportBrowserSettings
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importcookies"></a>ImportCookies

  #### <a name="allow-importing-of-cookies"></a>允許匯入 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將 Cookie 匯入到 Microsoft Edge。

如果停用此原則，則 Cookie 不會在初次執行時匯入。

如果未設定此原則，則 Cookie 會在初次執行時匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入 Cookie。

**注意**：此原則目前會管理來自 Google Chrome (Windows 7、8 和 10 上，以及 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportCookies
  - GP 名稱：允許匯入 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportCookies
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportCookies
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importextensions"></a>ImportExtensions

  #### <a name="allow-importing-of-extensions"></a>允許匯入擴充功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將擴充功能匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [擴充功能]**** 核取方塊。

如果停用此原則，則擴充功能不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入擴充功能，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入擴充功能，但使用者可以在手動匯入期間選取或清除 [我的最愛]**** 選項。

**注意**：此原則目前只支援來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportExtensions
  - GP 名稱：允許匯入擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportExtensions
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportExtensions
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importfavorites"></a>ImportFavorites

  #### <a name="allow-importing-of-favorites"></a>允許匯入我的最愛

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將我的最愛匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [我的最愛]**** 核取方塊。

如果停用此原則，則 [我的最愛] 不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則在初次執行時匯入我的最愛，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入我的最愛，但使用者可以在手動匯入期間選取或清除 [我的最愛]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上)、Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上)，以及 Apple Safari (在 macOS 上) 瀏覽器的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportFavorites
  - GP 名稱：允許匯入我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportFavorites
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportFavorites
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importhistory"></a>ImportHistory

  #### <a name="allow-importing-of-browsing-history"></a>允許匯入瀏覽歷程記錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將瀏覽歷程記錄匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [瀏覽歷程記錄]**** 核取方塊。

如果停用此原則，則瀏覽歷程記錄資料不會在初次執行時匯入，且使用者無法手動匯入此資料。

如果未設定此原則，瀏覽歷程記錄資料會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入瀏覽歷程記錄，但使用者可以在手動匯入期間選取或清除 [歷程記錄]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及 macOS 上)、Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 以及 Apple Safari (macOS) 瀏覽器的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportHistory
  - GP 名稱：允許匯入瀏覽歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportHistory
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportHistory
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importhomepage"></a>ImportHomepage

  #### <a name="allow-importing-of-home-page-settings"></a>允許匯入首頁設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將首頁設定匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入首頁設定的選項。

如果停用此原則，則首頁設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，首頁設定會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入首頁設定，但使用者可以在手動匯入期間選取或清除 [首頁]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportHomepage
  - GP 名稱：允許匯入首頁設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ImportHomepage
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportHomepage
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importopentabs"></a>ImportOpenTabs

  #### <a name="allow-importing-of-open-tabs"></a>允許匯入開啟的索引標籤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將開啟和釘選的索引標籤匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [開啟的索引標籤]**** 核取方塊。

如果停用此原則，則開啟的索引標籤不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入開啟的索引標籤，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入開啟的索引標籤，但使用者可以在手動匯入期間選取或清除 [開啟的索引標籤]**** 選項。

**注意**：此原則目前只支援來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportOpenTabs
  - GP 名稱：允許匯入開啟的索引標籤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportOpenTabs
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportOpenTabs
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importpaymentinfo"></a>ImportPaymentInfo

  #### <a name="allow-importing-of-payment-info"></a>允許匯入付款資訊

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將付款資訊匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [付款資訊]**** 核取方塊。

如果停用此原則，則付款資訊不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，付款資訊在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入付款資訊，但使用者可以在手動匯入期間選取或清除 [付款資訊]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportPaymentInfo
  - GP 名稱：允許匯入付款資訊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportPaymentInfo
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportPaymentInfo
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importsavedpasswords"></a>ImportSavedPasswords

  #### <a name="allow-importing-of-saved-passwords"></a>允許匯入儲存的密碼

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將儲存的密碼匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入儲存的密碼的選項。

如果停用此原則，則儲存的密碼不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入密碼，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入密碼，但使用者可以在手動匯入期間選取或清除 [密碼]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及 macOS 上) 以及 Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 瀏覽器的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportSavedPasswords
  - GP 名稱：允許匯入儲存的密碼
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportSavedPasswords
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportSavedPasswords
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importsearchengine"></a>ImportSearchEngine

  #### <a name="allow-importing-of-search-engine-settings"></a>允許匯入搜尋引擎設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許使用者從其他瀏覽器將搜尋引擎設定匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取匯入搜尋引擎設定的選項。

如果停用此原則，則搜尋引擎設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，搜尋引擎設定會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入搜尋引擎設定，但使用者可以在手動匯入期間選取或清除 [搜尋引擎]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportSearchEngine
  - GP 名稱：允許匯入搜尋引擎設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportSearchEngine
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportSearchEngine
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importshortcuts"></a>ImportShortcuts

  #### <a name="allow-importing-of-shortcuts"></a>允許匯入捷徑

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  允許使用者將捷徑從其他瀏覽器匯入到 Microsoft Edge。

如果停用此原則，則捷徑不會在初次執行時匯入。

如果未設定此原則，則捷徑會在初次執行時匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入捷徑。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportShortcuts
  - GP 名稱：允許匯入捷徑
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportShortcuts
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ImportShortcuts
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="importstartuppagesettings"></a>ImportStartupPageSettings

  #### <a name="allow-importing-of-startup-page-settings"></a>允許匯入啟動程序設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 91 或更新版本

  #### <a name="description"></a>說明

  允許使用者從其他瀏覽器將啟動程序設定匯入到 Microsoft Edge。

如果啟用此原則，則會一直匯入啟動程序設定。

如果停用此原則，則啟動程序設定就不會在首次執行或手動匯入時進行。

如果未設定此原則，則啟動程序設定會于第一次執行時進行，且使用者可以選擇是否要在稍後瀏覽工作階段期間選取瀏覽器設定選項，以手動方式匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入啟動程序設定，但使用者可以在手動匯入期間選取或清除 **[瀏覽器設定]** 選項。

**注意**：此原則目前會管理來自舊版 Microsoft Edge 和 Google Chrome (在 Windows 7、8 和 10) 瀏覽器中的匯入。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ImportStartupPageSettings
  - GP 名稱：允許匯入啟動程序頁面設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportStartupPageSettings
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="inprivatemodeavailability"></a>InPrivateModeAvailability

  #### <a name="configure-inprivate-mode-availability"></a>設定 InPrivate 模式可用性

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定使用者是否可以在 Microsoft Edge 的 InPrivate 模式中開啟頁面。

如果未設定此原則，或將其設定為 '已啟用'，則使用者可以在 InPrivate 模式中開啟頁面。

將此原則設定為 '已停用'，以防止使用者使用 InPrivate 模式。

將此原則設定為 '已強制'，以一律使用 InPrivate 模式。

原則選項對應：

* 已啟用 (0) = InPrivate 模式可用

* 已停用 (1) = InPrivate 模式已停用

* 已強制 (2) = InPrivate 模式已強制執行

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InPrivateModeAvailability
  - GP 名稱：設定 InPrivate 模式可用性
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InPrivateModeAvailability
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：InPrivateModeAvailability
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="insecureformswarningsenabled"></a>InsecureFormsWarningsEnabled

  #### <a name="enable-warnings-for-insecure-forms"></a>啟用不安全表單的警告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  此原則控制了嵌入瀏覽器中安全網站 (HTTPS) 的不安全表單 (透過 HTTP 提交的表單) 處置。
如果您啟用或未設定此原則，則系統會在提交不安全表單時，顯示全頁式警告。 此外，當聚焦在表單欄位時，旁邊會出現警告泡泡，且這些表單的自動填滿功能將被停用。
如果您停用此原則，針對不安全表單的警告便不會顯示，自動填滿功能將會正常運作。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InsecureFormsWarningsEnabled
  - GP 唯一名稱：啟用不安全表單的警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InsecureFormsWarningsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： InsecureFormsWarningsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="intensivewakeupthrottlingenabled"></a>IntensiveWakeUpThrottlingEnabled

  #### <a name="control-the-intensivewakeupthrottling-feature"></a>管理 IntensiveWakeUpThrottling 功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  啟用 IntensiveWakeUpThrottling 功能時，會導致背景索引標籤中的 Javascript 計時器受到積極地節流和合併，在背景化達 5 分鐘或更久的單一頁面中運行每分鐘一次 (至多)。

這是一個符合網站標準的功能，但可能會造成某些網站的功能中斷，因為這會造成某些動作推遲多達一分鐘的時間。 不過，啟用時可造成顯著的節省 CPU 和電池損耗。 如需詳細資訊，請參閱https://bit.ly/30b1XR4。

如果啟用此原則，系統將會強制啟用此功能，而且使用者將無法覆寫這個設定。
如果停用此原則，系統將會強制停用此功能，而且使用者將無法覆寫這個設定。
若您未設定此原則，此功能將由其本身的內部邏輯所管理。 使用者可以手動設置此設定。

請注意，此原則會套用在每個轉譯過程，當轉譯過程啟動時，系統會強制執行此原則的最新值。 若要確保所有已載入的索引標籤都能收到一致的原則設定，則需完全重新開機。 使用此原則的不同值執行程式會造成危害。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：IntensiveWakeUpThrottlingEnabled
  - GP 名稱：管理 IntensiveWakeUpThrottling 功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：IntensiveWakeUpThrottlingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：IntensiveWakeUpThrottlingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationenhancedhangdetection"></a>InternetExplorerIntegrationEnhancedHangDetection

  #### <a name="configure-enhanced-hang-detection-for-internet-explorer-mode"></a>針對 Internet Explorer 模式設定增強的當機偵測

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  「加強當機偵測」是更精細的方法，可在 Internet Explorer 模式中偵測到獨立 Internet Explorer 所使用的網頁。 當檢測到網頁當機時，瀏覽器將會套用安全防護，以避免其餘的瀏覽器出現當機情形。

這項設定可讓您設定使用增強的 [當機偵測]，以防您遇到與任何網站都不相容的問題。 只有在當您在 Internet Explorer 模式 (而不是獨立 Internet Explorer) 中看到 (網站) 沒有回應等通知時，建議您停用此原則。

此設定會與下列內容一併執行：[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode'，並設定 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中該清單至少擁有一個項目。

如果將此原則設為 '已啟用' 或未設定，則在 Internet Explorer 模式中執行的網站將會使用增強的當機偵測。

如果將此原則設為 '已停用'，則會停用增強的當機偵測，而使用者可使用基本的 Internet Explorer 當機偵測行為。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

原則選項對應：

* 已停用 (0) = 已停用增強的當機偵測

* 已啟用 (1) = 啟用增強的當機偵測

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationEnhancedHangDetection
  - GP 名稱：針對 Internet Explorer 模式設定增強的當機偵測
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： InternetExplorerIntegrationEnhancedHangDetection
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationlevel"></a>InternetExplorerIntegrationLevel

  #### <a name="configure-internet-explorer-integration"></a>設定 Internet Explorer 整合

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

原則選項對應：

* None (0) = 無

* IEMode (1) = Internet Explorer 模式

* NeedIE (2) = Internet Explorer 11

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationLevel
  - GP 名稱：設定 Internet Explorer 整合
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationLevel
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationlocalfileallowed"></a>InternetExplorerIntegrationLocalFileAllowed

  #### <a name="allow-launching-of-local-files-in-internet-explorer-mode"></a>允許在 Internet Explorer 模式中啟動本機檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則可控制 --ie-mode-file-url 命令列引數的可用性，其用來在命令列上使用指定的本機檔案啟動 Microsoft Edge 並進入 Internet Explorer 模式。

此設定可結合將 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode' 運作。

如果您將此原則設定為 true，或未設定此原則，則會允許使用者將 --ie-mode-file-url 命令列引數用於在 Internet Explorer 模式中啟動本機檔案。

如果您將此原則設定為 false，則不允許使用者將 --ie-mode-file-url 命令列引數用於在 Internet Explorer 模式中啟動本機檔案。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationLocalFileAllowed
  - GP 名稱：允許在 Internet Explorer 模式中啟動本機檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationLocalFileAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationlocalfileextensionallowlist"></a>InternetExplorerIntegrationLocalFileExtensionAllowList

  #### <a name="open-local-files-in-internet-explorer-mode-file-extension-allow-list"></a>根據副檔名允許清單在 Internet Explorer 模式中開啟本機檔案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則會根據副檔名限制允許在 Internet Explorer 模式中啟動的 file:// URL。

此設定可結合將 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode' 運作。

要求在 Internet Explorer 模式中啟動某個 file:// URL 時，該 URL 的副檔名必須存在於此清單中，才能允許在 Internet Explorer 模式中啟動該 URL。 遭封鎖而無法在 Internet Explorer 模式中開啟的 URL，將改為在 Microsoft Edge 模式中開啟。

如果將此原則設定為特殊值 "*"，或未設定它，則會允許所有副檔名。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationLocalFileExtensionAllowList
  - GP 名稱：根據副檔名允許清單在 Internet Explorer 模式中開啟本機檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\1 = ".mht"
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\2 = ".pdf"
SOFTWARE\Policies\Microsoft\Edge\InternetExplorerIntegrationLocalFileExtensionAllowList\3 = ".vsdx"

```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationlocalfileshowcontextmenu"></a>InternetExplorerIntegrationLocalFileShowContextMenu

  #### <a name="show-context-menu-to-open-a-file-link-in-internet-explorer-mode"></a>顯示操作功能表以在 Internet Explorer 模式中開啟 file:// 連結

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則可控制 file:// 連結操作功能表上的 [在新的 Internet Explorer 模式索引標籤中開啟連結] 選項的可見度。

此設定可結合將 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode' 運作。

如果將此原則設定為 true，[在新的 Internet Explorer 模式索引標籤中開啟連結] 操作功能表項目將可供 file:// 連結使用。

如果將此原則設定為 false 或未設定，將不會新增該操作功能表項目。

如果 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) 原則允許使用者在 Internet Explorer 模式中重新載入網站，則除了網站清單明確為使用 Microsoft Edge 模式的網站連結之外，所有連結都可使用'以新 Internet Explorer 模式開啟連結' 操作功能表項目。 在這種情況下，如果您將這個原則設定為 true，操作功能表項目將可供 file:// 連結使用，即使是設定為使用 Microsoft Edge 模式的網站也一樣。 如果您將這個原則設定為 False 或未設定，則此原則便不會作用。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationLocalFileShowContextMenu
  - GP 名稱：顯示操作功能表以在 Internet Explorer 模式中開啟 file:// 連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationLocalFileShowContextMenu
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationlocalsitelistexpirationdays"></a>InternetExplorerIntegrationLocalSiteListExpirationDays

  #### <a name="specify-the-number-of-days-that-a-site-remains-on-the-local-ie-mode-site-list"></a>指定網站保留在區域 IE 模式網站清單上的天數

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  如果 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) 原則已啟用或尚未進行，使用者將能夠告知 Microsoft Edge 在 Internet Explorer 模式中載入特定頁面的天數。

您可以使用此設定來決定在瀏覽器中記住該設定多少天。 經過此期間之後，個別頁面將不再以 IE 模式自動載入。

如果您停用 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) ，則此原則不會有作用。

如果您停用或沒有設定此原則，則使用預設值 30 天。

如果啟用此原則，您必須在 Microsoft Edge 的使用者本地網站清單上輸入網站保留的天數。 該值可以是 0 到 90 天。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationLocalSiteListExpirationDays
  - GP 名稱：指定網站保留在區域 IE 模式網站清單上的天數
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： InternetExplorerIntegrationLocalSiteListExpirationDays
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x0000001e
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationreloadiniemodeallowed"></a>InternetExplorerIntegrationReloadInIEModeAllowed

  #### <a name="allow-unconfigured-sites-to-be-reloaded-in-internet-explorer-mode"></a>允許在 Internet Explorer 模式中重新載入未設置的網站

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 92 或更新版本

  #### <a name="description"></a>說明

  此原則允許使用者在 Microsoft Edge 中瀏覽時，在 Internet Explorer 模式中重新載入未設定的網站 (未在企業模式網站清單中進行設定)，而網站需要 Internet Explorer 的相容性。

在 Internet Explorer 模式中重新載入網站之後，「頁面內」瀏覽會保持 Internet Explorer 模式 (例如頁面上的連結、指令碼或表單，或另一個「頁面內」瀏覽的伺服器端重新導向)。 使用者可以選擇離開 Internet Explorer 模式，或者當非「頁面內」的瀏覽 (例如，使用網址列、返回按鈕或我的最愛連結) 時，Microsoft Edge 會自動離開 Internet Explorer 模式。

使用者也可以選擇性地告知 Microsoft Edge 未來使用網站的 Internet Explorer 模式。 這個選項會記住一段由 [InternetExplorerIntegrationLocalSiteListExpirationDays](#internetexplorerintegrationlocalsitelistexpirationdays) 原則管理的時間長度。

如果 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 原則設定為 'IEMode'， 然後， [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則的網站清單以使用 Microsoft Edge 的網站清單無法以 Internet Explorer 模式重新載入，且網站清單或 [SendIntranetToInternetExplorer](#sendintranettointernetexplorer) 原則所設定的網站無法從 Internet Explorer 模式退出。

如果您啟用此原則，則允許使用者在 Internet Explorer 模式中重新載入未設定的網站。

如果您停用此原則，則不允許使用者在 Internet Explorer 模式中重新載入未設定的網站。

請注意，如果您啟用此原則，它會優先于您對[InternetExplorerIntegrationTestingAllowed](#internetexplorerintegrationtestingallowed) 原則的設定，且該原則將會被停用。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationReloadInIEModeAllowed
  - GP 名稱：允許在 Internet Explorer 模式中重新載入未設置的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱： InternetExplorerIntegrationReloadInIEModeAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationsitelist"></a>InternetExplorerIntegrationSiteList

  #### <a name="configure-the-enterprise-mode-site-list"></a>設定 Enterprise Mode Site List

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationSiteList
  - GP 名稱：設定 Enterprise Mode Site List
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationSiteList
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://internal.contoso.com/sitelist.xml"
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationsiteredirect"></a>InternetExplorerIntegrationSiteRedirect

  #### <a name="specify-how-in-page-navigations-to-unconfigured-sites-behave-when-started-from-internet-explorer-mode-pages"></a>指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 81 或更新版本

  #### <a name="description"></a>描述

  「頁面內」導覽是從連結、指令碼或目前頁面上的表單開始。 也可以是先前「頁面內」導覽嘗試的伺服器端重新導向。 相反地，使用者可以使用瀏覽器控制項以多種方式啟動不在「頁面內」且獨立於目前頁面的導覽。 例如透過網址列、返回按鈕或我的最愛連結。

此設定可讓您指定是否要從 Internet Explorer 模式下載入的頁面導覽至未設定網站 (未於 Enterprise Mode Site List 中設定) 切換回 Microsoft Edge 或停留在 Internet Explorer 模式。

此設定會與下列內容一併執行：[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode'，並設定 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中該清單至少擁有一個項目。

如果停用或未設定此原則，則只有設定在 Internet Explorer 模式中開啟的網站，才會在該模式中開啟。 所有未設定在 Internet Explorer 模式中開啟的網站，將會重新導向回到 Microsoft Edge。

如果將此原則設定為 ‘預設’，只有設定為在 Internet Explorer 模式中開啟的網站，才會在該模式中開啟。 所有未設定在 Internet Explorer 模式中開啟的網站，將會重新導向回到 Microsoft Edge。

如果將此原則設定為 'AutomaticNavigationsOnly'，將會獲得預設體驗，但對未設定網站的所有自動導覽 (例如 302 重新導向) 都會保留在 Internet Explorer 模式。

如果將此原則設定為 'AllInPageNavigations'，則於 IE 模式載入到未設定網站之頁面的所有導覽，都會保留在 Internet Explorer 模式 (最不建議)。

如果 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) 原則允許使用者在 Internet Explorer 模式中重新載入網站，則使用者選擇在 Internet Explorer 模式中重新載入之未設定的網站的所有頁面內瀏覽都會保留在 Internet Explorer 模式中，無論此原則的群組原則如何進行。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

原則選項對應：

* 預設值 (0) = 預設值

* AutomaticNavigationsOnly (1) = 只保留 Internet Explorer 模式中的自動導覽

* AllInPageNavigations (2) = 保留所有 Internet Explorer 模式中的頁面內導覽

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationSiteRedirect
  - GP 名稱：指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationSiteRedirect
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="internetexplorerintegrationtestingallowed"></a>InternetExplorerIntegrationTestingAllowed

  #### <a name="allow-internet-explorer-mode-testing-deprecated"></a>允許 Internet Explorer 模式測試 (已取代) 

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 86 或更新版本

  #### <a name="description"></a>說明

  此原則已遭取代，請改為使用 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) 原則。 無法在 Microsoft Edge 版本 95 中使用。

這項原則可讓使用者透過在 Microsoft Edge 開啟 Internet Explorer 模式選項, 以 Internet Explorer 模式測試應用程式。

使用者可在＂更多工具＂功能表中，選取＂在 Internet Explorer 模式中開啟網站＂來執行此動作。

此外，使用者可以使用＂以邊緣模式開啟網站＂選項，在新式瀏覽器中測試應用程式，而不需要從網站列表中刪除應用程序 。

此設定可結合將 [InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode' 運作。

如果您啟用這個原則，則 [更多工具] 下將顯示 [以 Windows Internet Explorer 模式打開網站] 的選項。 使用者可以在這個索引標籤上，在 Internet Explorer 模式中查看他們的網站。＂其他工具＂下的＂ 以邊緣模式開啟網站＂ 以幫助在新式瀏覽器中測試網站，而不需將它們從網站清單中移除。 請注意，如果啟用 [InternetExplorerIntegrationReloadInIEModeAllowed](#internetexplorerintegrationreloadiniemodeallowed) 原則，它會優先使用，且這些選項不會顯示在 「其他工具」下。

如果您停用或未設定此原則，使用者就不會看到＂更多工具＂主選單下的＂在 Internet Explorer 模式中開啟＂ 和＂以邊緣模式開啟＂選項。 不過，使用者可以用--ie-mode-test 標誌來設定這些選項。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：InternetExplorerIntegrationTestingAllowed
  - GP 名稱：允許 Internet Explorer 模式測試 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationTestingAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="intranetredirectbehavior"></a>IntranetRedirectBehavior

  #### <a name="intranet-redirection-behavior"></a>內部網路重新導向行為

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  此原則會設定透過 DNS 攔截檢查的內部網路重新導向行為。 檢查會嘗試探索瀏覽器是否位於會將未知主機名稱重新導向的 Proxy 後面。

如果未設定此原則，瀏覽器將使用 DNS 攔截檢查和內部網路重新導向建議的預設行為。 在 M88 中，它們預設為啟用，但在未來版本中預設為停用。

[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled) 是可能也會停用 DNS 攔截檢查的相關原則。 不過，此原則是更具彈性的版本，能夠個別控制內部網路重新導向資訊列，並可能在未來擴大。
如果 [DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled) 或此原則中的一個要求停用攔截檢查，則會停用檢查。
如果 DNS 攔截檢查已由此原則停用，但 [GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar) 已啟用，則單一字詞查詢仍將導致內部網路瀏覽。

原則選項對應：

* 預設值 (0) = 使用預設瀏覽器行為。

* DisableInterceptionChecksDisableInfobar (1) = 停用 DNS 攔截檢查和 "http://intranetsite/" 資訊列。

* DisableInterceptionChecksEnableInfobar (2) = 停用 DNS 攔截檢查；允許 "http://intranetsite/" 資訊列。

* EnableInterceptionChecksEnableInfobar (3) = 允許 DNS 攔截檢查和 "http://intranetsite/" 資訊列。

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：IntranetRedirectBehavior
  - GP 名稱：內部網路重新導向行為
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：IntranetRedirectBehavior
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：IntranetRedirectBehavior
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="isolateorigins"></a>IsolateOrigins

  #### <a name="enable-site-isolation-for-specific-origins"></a>為特定來源啟用網站隔離

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  指定在隔離的進程中執行的來源。

根據預設，Microsoft Edge 會從每個網站將頁面隔離到自己的程式。 此原則會根據 Origin 而非網站，啟用更細微的隔離。 例如，指定 https://subdomain.contoso.com/ 會導致來自 https://subdomain.contoso.com/ 的頁面與來自 https://contoso.com/ 網站內其他原始來源的頁面在不同的進程中隔離。

如果您啟用此原則，以逗號分隔清單中的每個指定來源，將會在自己的處理程序中執行。

如果您停用或未設定此原則，將會以每個網站為基礎隔離頁面。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：IsolateOrigins
  - GP 名稱：為特定來源啟用網站隔離
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：IsolateOrigins
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"https://contoso.com/,https://fabrikam.com/"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：IsolateOrigins
  - 範例值：
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="localbrowserdatashareenabled"></a>LocalBrowserDataShareEnabled

  #### <a name="enable-windows-to-search-local-microsoft-edge-browsing-data"></a>啟用 Windows 以搜尋當地 Microsoft Edge 瀏覽資料

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 93 或更新版本

  #### <a name="description"></a>說明

  可讓 Windows 為儲存在使用者裝置上的 Microsoft Edge 瀏覽資料編制索引，並讓使用者直接從 Windows 功能 (例如 Windows 工作列上的搜尋方塊) 尋找並啟動先前儲存的瀏覽資料。

如果您啟用此原則或未設定，Microsoft Edge 會發佈本地瀏覽資料至 Windows 索引器。

如果您停用此原則，Microsoft Edge 將不會將資料分享給 Windows 索引器。

請注意，如果您停用此原則，Microsoft Edge 將會移除裝置上與 Windows 共用的資料，並停止共用任何新的瀏覽資料。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：LocalBrowserDataShareEnabled
  - GP 名稱：啟用 Windows 以搜尋當地 Microsoft Edge 瀏覽資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：LocalBrowserDataShareEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="localprovidersenabled"></a>LocalProvidersEnabled

  #### <a name="allow-suggestions-from-local-providers"></a>允許來自本機提供者的建議

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 的網址列和自動建議清單中，允許來自裝置上建議提供者的建議 (本機提供者)，例如我的最愛和瀏覽歷程記錄。

如果啟用此原則，則會使用來自本機提供者的建議。

如果停用此原則，則永遠不會使用來自本機提供者的建議。 將不會顯示本機歷程記錄和本機我的最愛建議。

如果未設定此原則，則會允許來自本機提供者的建議，但使用者可以使用 [設定] 切換來變更。

請注意，如果已套用停用此功能的原則，則部分功能可能無法使用。 例如，如果您啟用 [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) 原則，瀏覽歷程記錄建議將無法使用。

此原則需要將瀏覽器重新啟動，才能完成套用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：LocalProvidersEnabled
  - GP 名稱：允許來自本機提供者的建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：LocalProvidersEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：LocalProvidersEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="managedconfigurationperorigin"></a>ManagedConfigurationPerOrigin

  #### <a name="sets-managed-configuration-values-for-websites-to-specific-origins"></a>設定網站到特定來源的受管理設定值

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  設定此原則會定義指定來源的受管理設定 API 傳回值。

 受管理設定 API 是可透過 navigator.device.getManagedConfiguration() javascript 呼叫存取的機碼值設定。 此 API 僅可供透過 [WebAppInstallForceList](#webappinstallforcelist) 對應至強制安裝 Web 應用程式的來源使用。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ManagedConfigurationPerOrigin
  - GP 名稱：設定網站到特定來源的受管理設定值
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ManagedConfigurationPerOrigin
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ManagedConfigurationPerOrigin = [
  {
    "managed_configuration_hash": "asd891jedasd12ue9h",
    "managed_configuration_url": "https://static.contoso.com/configuration.json",
    "origin": "https://www.contoso.com"
  },
  {
    "managed_configuration_hash": "djio12easd89u12aws",
    "managed_configuration_url": "https://static.contoso.com/configuration2.json",
    "origin": "https://www.example.com"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedConfigurationPerOrigin = [{"managed_configuration_hash": "asd891jedasd12ue9h", "managed_configuration_url": "https://static.contoso.com/configuration.json", "origin": "https://www.contoso.com"}, {"managed_configuration_hash": "djio12easd89u12aws", "managed_configuration_url": "https://static.contoso.com/configuration2.json", "origin": "https://www.example.com"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ManagedConfigurationPerOrigin
  - 範例值：
``` xml
<key>ManagedConfigurationPerOrigin</key>
<array>
  <dict>
    <key>managed_configuration_hash</key>
    <string>asd891jedasd12ue9h</string>
    <key>managed_configuration_url</key>
    <string>https://static.contoso.com/configuration.json</string>
    <key>origin</key>
    <string>https://www.contoso.com</string>
  </dict>
  <dict>
    <key>managed_configuration_hash</key>
    <string>djio12easd89u12aws</string>
    <key>managed_configuration_url</key>
    <string>https://static.contoso.com/configuration2.json</string>
    <key>origin</key>
    <string>https://www.example.com</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="managedfavorites"></a>ManagedFavorites

  #### <a name="configure-favorites"></a>設定我的最愛

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定受管理的我的最愛清單。

該原則會建立我的最愛清單。 每個我的最愛都包含 "name" 和 "url"，這些機碼會保留我的最愛名稱及其目標。 您可以定義一個不帶 "url" 機碼但帶有一個額外的 "children" 機碼的我的最愛，藉此設定子資料夾，其中包含上面定義的我的最愛清單 (其中部分也可能是資料夾)。 Microsoft Edge 會修訂不完整的 URL，就如同透過網址列提交一般，例如 "microsoft.com" 會變成 "https://microsoft.com/"。

這些我的最愛會放在不能由使用者修改的資料夾中 (但使用者可以選擇將它從我的最愛列隱藏)。 依預設，資料夾名稱是「受管理的我的最愛」，但您可以將包含機碼 "toplevel_name" 並使用所需的資料夾名稱做為值的字典新增至我的最愛清單。

受管理我的最愛不會同步到使用者帳戶，且不能由擴充功能修改。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ManagedFavorites
  - GP 名稱：設定我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ManagedFavorites
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [
  {
    "toplevel_name": "My managed favorites folder"
  },
  {
    "name": "Microsoft",
    "url": "microsoft.com"
  },
  {
    "name": "Bing",
    "url": "bing.com"
  },
  {
    "children": [
      {
        "name": "Microsoft Edge Insiders",
        "url": "www.microsoftedgeinsider.com"
      },
      {
        "name": "Microsoft Edge",
        "url": "www.microsoft.com/windows/microsoft-edge"
      }
    ],
    "name": "Microsoft Edge links"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedFavorites = [{"toplevel_name": "My managed favorites folder"}, {"name": "Microsoft", "url": "microsoft.com"}, {"name": "Bing", "url": "bing.com"}, {"children": [{"name": "Microsoft Edge Insiders", "url": "www.microsoftedgeinsider.com"}, {"name": "Microsoft Edge", "url": "www.microsoft.com/windows/microsoft-edge"}], "name": "Microsoft Edge links"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ManagedFavorites
  - 範例值：
``` xml
<key>ManagedFavorites</key>
<array>
  <dict>
    <key>toplevel_name</key>
    <string>My managed favorites folder</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Microsoft</string>
    <key>url</key>
    <string>microsoft.com</string>
  </dict>
  <dict>
    <key>name</key>
    <string>Bing</string>
    <key>url</key>
    <string>bing.com</string>
  </dict>
  <dict>
    <key>children</key>
    <array>
      <dict>
        <key>name</key>
        <string>Microsoft Edge Insiders</string>
        <key>url</key>
        <string>www.microsoftedgeinsider.com</string>
      </dict>
      <dict>
        <key>name</key>
        <string>Microsoft Edge</string>
        <key>url</key>
        <string>www.microsoft.com/windows/microsoft-edge</string>
      </dict>
    </array>
    <key>name</key>
    <string>Microsoft Edge links</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="managedsearchengines"></a>ManagedSearchEngines

  #### <a name="manage-search-engines"></a>管理搜尋引擎

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓您設定最多 10 個搜尋引擎的清單，其中一個必須標示為預設搜尋引擎。
您不需要指定編碼。 從 Microsoft Edge 80 開始，suggest_url 和 image_search_url 參數都是選用。 選用參數 image_search_post_params (包含逗號分隔名稱/值對) 從 Microsoft Edge 80 開始提供。

從 Microsoft Edge 83 開始，您可以使用 allow_search_engine_discovery optional 選用參數來啟用搜尋引擎探索。 此參數必須是清單中的第一個項目。 如果未指定 allow_search_engine_discovery，即預設會停用搜尋引擎探索。 從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則，以允許搜尋提供者探索。 您不需要新增 allow_search_engine_discovery 選用參數。

如果啟用此原則，則使用者無法新增、移除或變更清單中的任何搜尋引擎。 使用者可以將其預設搜尋引擎設定為清單中的任何搜尋引擎。

如果停用或未設定此原則，則使用者可以視需要修改搜尋引擎清單。

如果已設定 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則，則會忽略此原則 (ManagedSearchEngines)。 使用者必須將其瀏覽器重新啟動，才能完成套用此原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ManagedSearchEngines
  - GP 名稱：管理搜尋引擎
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ManagedSearchEngines
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [
  {
    "allow_search_engine_discovery": true
  },
  {
    "is_default": true,
    "keyword": "example1.com",
    "name": "Example1",
    "search_url": "https://www.example1.com/search?q={searchTerms}",
    "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"
  },
  {
    "image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}",
    "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload",
    "keyword": "example2.com",
    "name": "Example2",
    "search_url": "https://www.example2.com/search?q={searchTerms}",
    "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"
  },
  {
    "encoding": "UTF-8",
    "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload",
    "keyword": "example3.com",
    "name": "Example3",
    "search_url": "https://www.example3.com/search?q={searchTerms}",
    "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"
  },
  {
    "keyword": "example4.com",
    "name": "Example4",
    "search_url": "https://www.example4.com/search?q={searchTerms}"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\ManagedSearchEngines = [{"allow_search_engine_discovery": true}, {"is_default": true, "keyword": "example1.com", "name": "Example1", "search_url": "https://www.example1.com/search?q={searchTerms}", "suggest_url": "https://www.example1.com/qbox?query={searchTerms}"}, {"image_search_post_params": "content={imageThumbnail},url={imageURL},sbisrc={SearchSource}", "image_search_url": "https://www.example2.com/images/detail/search?iss=sbiupload", "keyword": "example2.com", "name": "Example2", "search_url": "https://www.example2.com/search?q={searchTerms}", "suggest_url": "https://www.example2.com/qbox?query={searchTerms}"}, {"encoding": "UTF-8", "image_search_url": "https://www.example3.com/images/detail/search?iss=sbiupload", "keyword": "example3.com", "name": "Example3", "search_url": "https://www.example3.com/search?q={searchTerms}", "suggest_url": "https://www.example3.com/qbox?query={searchTerms}"}, {"keyword": "example4.com", "name": "Example4", "search_url": "https://www.example4.com/search?q={searchTerms}"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ManagedSearchEngines
  - 範例值：
``` xml
<key>ManagedSearchEngines</key>
<array>
  <dict>
    <key>allow_search_engine_discovery</key>
    <true/>
  </dict>
  <dict>
    <key>is_default</key>
    <true/>
    <key>keyword</key>
    <string>example1.com</string>
    <key>name</key>
    <string>Example1</string>
    <key>search_url</key>
    <string>https://www.example1.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example1.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>image_search_post_params</key>
    <string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
    <key>image_search_url</key>
    <string>https://www.example2.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example2.com</string>
    <key>name</key>
    <string>Example2</string>
    <key>search_url</key>
    <string>https://www.example2.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example2.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>encoding</key>
    <string>UTF-8</string>
    <key>image_search_url</key>
    <string>https://www.example3.com/images/detail/search?iss=sbiupload</string>
    <key>keyword</key>
    <string>example3.com</string>
    <key>name</key>
    <string>Example3</string>
    <key>search_url</key>
    <string>https://www.example3.com/search?q={searchTerms}</string>
    <key>suggest_url</key>
    <string>https://www.example3.com/qbox?query={searchTerms}</string>
  </dict>
  <dict>
    <key>keyword</key>
    <string>example4.com</string>
    <key>name</key>
    <string>Example4</string>
    <key>search_url</key>
    <string>https://www.example4.com/search?q={searchTerms}</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="mathsolverenabled"></a>MathSolverEnabled

  #### <a name="let-users-snip-a-math-problem-and-get-the-solution-with-a-step-by-step-explanation-in-microsoft-edge"></a>讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 91 或更新版本

  #### <a name="description"></a>說明

  此原則可讓您管理使用者是否可以使用 Microsoft Edge 中的數學規劃求解工具。

如果您啟用或未設定此原則，則使用者可以對數學問題進行一些剪取，並取得解決方案，包括 Microsoft Edge 側邊窗格中的解決方案逐步解說。

如果您停用此原則，則數學規劃求解工具將會停用，且使用者將無法使用它。

注意： 將 [ComponentUpdatesEnabled](#componentupdatesenabled) 原則設定為停用也會停用數學規劃求解元件。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：MathSolverEnabled
  - GP 名稱：讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MathSolverEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：MathSolverEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="maxconnectionsperproxy"></a>MaxConnectionsPerProxy

  #### <a name="maximum-number-of-concurrent-connections-to-the-proxy-server"></a>同時連線到 Proxy 伺服器的最大數目

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定對 Proxy 伺服器同時連線的上限。

某些 Proxy 伺服器無法處理每個用戶端的大量同時連線，您可以將此原則設定為較低的值來解決此情況。

此原則的值應低於 100，並高於 6。 預設值為 32。

某些 Web 應用程式已知會因為當機的 GET 耗用多個連線。將連線上限降低至低於 32 可能會在開啟許多這類 Web 應用程式時導致瀏覽器網路當機。

如果未設定此原則，則會使用預設值 (32)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：MaxConnectionsPerProxy
  - GP 名稱：同時連線到 Proxy 伺服器的最大數目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MaxConnectionsPerProxy
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000020
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：MaxConnectionsPerProxy
  - 範例值：
``` xml
<integer>32</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="mediaroutercastallowallips"></a>MediaRouterCastAllowAllIPs

  #### <a name="allow-google-cast-to-connect-to-cast-devices-on-all-ip-addresses"></a>允許 Google Cast 連線至所有 IP 位址上的投射裝置

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用此原則以讓 Google Cast 連線至所有 IP 位址上的投射裝置，不只是 RFC1918/RFC4193 私人位址。

停用此原則以限制 Google Cast 連線至 RFC1918/RFC4193 私人位址上的投射裝置。

如果未設定此原則，除非啟用 CastAllowAllIPs 功能，否則 Google Cast 僅會連線至 RFC1918/RFC4193 私人位址上的投射裝置。

如果 [EnableMediaRouter](#enablemediarouter) 原則為已停用，則此原則沒有作用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：MediaRouterCastAllowAllIPs
  - GP 名稱：允許 Google Cast 連線至所有 IP 位址上的投射裝置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MediaRouterCastAllowAllIPs
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：MediaRouterCastAllowAllIPs
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="metricsreportingenabled"></a>MetricsReportingEnabled

  #### <a name="enable-usage-and-crash-related-data-reporting-obsolete"></a>啟用使用方式和當機相關的資料報告 (已淘汰)

  
  >已過時：此原則已過時且無法在 Microsoft Edge 88 之後運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 88

  #### <a name="description"></a>描述

  已不再支援此原則。 它被 [DiagnosticData](#diagnosticdata) (用於 Windows 7、Windows 8 和 macOS) 取代，並允許在 Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) 上進行遙測。

此原則可將Microsoft Edge 使用方式和當機相關資料的報告傳送到 Microsoft。

啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。 停用此原則，就不會將此資料傳送到 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

在 Windows 10 上，如果未設定此原則，則 Microsoft Edge 將預設為使用 Windows 診斷資料設定。 如果啟用此原則，則僅當 Windows 診斷資料設定設為「增強」或「完整」時，Microsoft Edge 才會傳送使用狀況資料。 如果停用此原則，則 Microsoft Edge 將不會傳送使用狀況資料。 根據 Windows 診斷資料設定傳送當機相關的資料。 在這裡深入了解 Windows 診斷資料設定：[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

在 Windows 7、Windows 8 和 macOS 上，此原則會控制使用方式和當機相關資料的傳送。 如果未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

若要啟用此原則，[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 必須設定為 [已啟用]。 如果 [MetricsReportingEnabled](#metricsreportingenabled) 或 [ SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 未設定或已停用，將不會將此資料傳送到 Microsoft。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：MetricsReportingEnabled
  - GP 名稱：啟用使用方式和當機相關的資料報告 (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MetricsReportingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：MetricsReportingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="nativewindowocclusionenabled"></a>NativeWindowOcclusionEnabled

  #### <a name="enable-native-window-occlusion-deprecated"></a>啟用原生視窗遮蔽 (已取代)

  >已取代：此原則已被取代。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  此原則已被取代，請改用 '[WindowOcclusionEnabled](#windowocclusionenabled)' 原則。 無法在 Microsoft Edge 版本92中使用。

在 Microsoft Edge 中啟用原生視窗遮蔽。

如果啟用此設定，為了降低 CPU 和耗電量，Microsoft Edge 將偵測視窗何時被其他視窗覆蓋，並將暫停工作繪製像素。

如果停用此設定，則 Microsoft Edge 無法偵測某個視窗是否被其他視窗遮蓋。

如果將此原則保留為未設定，則會啟用視窗遮蔽。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NativeWindowOcclusionEnabled
  - GP 名稱：啟用原生視窗遮蔽 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NativeWindowOcclusionEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="navigationdelayforinitialsitelistdownloadtimeout"></a>NavigationDelayForInitialSiteListDownloadTimeout

  #### <a name="set-a-timeout-for-delay-of-tab-navigation-for-the-enterprise-mode-site-list"></a>針對企業模式網站清單，設定索引標籤瀏覽逾時延遲

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  可讓您設定適於 Microsoft Edge 索引標籤等候瀏覽的逾時設定 (以秒為單位) ，直到瀏覽器完成下載初始的 [企業模式網站清單] 為止。

此設定可與下列內容結合使用：將[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設為 'IEMode' 及 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中至少擁有清單中的一個項目，並將 [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) 設為「All eligible navigations」(1)。

若要下載 [企業模式網站清單]，索引標籤的等待時間不會長於此逾時設定。 如果瀏覽器在逾時設定到期時並未完成下載 [企業模式網站清單]，Microsoft Edge 索引標籤仍會繼續瀏覽。 逾時設定的數值應少於 20 秒且多於 1 秒。

若將此原則中的逾時設置設成大於 2 秒的預設值，系統會在 2 秒之後向使用者顯示資訊列。 資訊列包含可讓使用者在等候 [企業模式網站清單] 下載完成時停止等候的按鈕。

如果未設定此原則，系統將會使用逾時設置的預設值 (2 秒)。 此預設值可會在未來進行變更。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NavigationDelayForInitialSiteListDownloadTimeout
  - GP 名稱：針對 [企業模式網站清單]，設定索引標籤瀏覽逾時延遲
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NavigationDelayForInitialSiteListDownloadTimeout
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x0000000a
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="networkpredictionoptions"></a>NetworkPredictionOptions

  #### <a name="enable-network-prediction"></a>啟用網路預測

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用網路預測，並防止使用者變更此設定。

這會控制 DNS 預先擷取、TCP 和 SSL 預先連線，以及網頁的預先轉譯。

如果未設定此原則，則會啟用網路預測，但使用者可以變更它。

原則選項對應：

* NetworkPredictionAlways (0) = 預測任何網路連線上的網路動作

* NetworkPredictionWifiOnly (1) = 不支援，如果使用這個值，系統會將其視為 '預測任何網路連線上的網路動作' (0) 之設定。

* NetworkPredictionNever (2) = 不預測任何網路連線上的網路動作

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NetworkPredictionOptions
  - GP 名稱：啟用網路預測
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NetworkPredictionOptions
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：NetworkPredictionOptions
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="nonremovableprofileenabled"></a>NonRemovableProfileEnabled

  #### <a name="configure-whether-a-user-always-has-a-default-profile-automatically-signed-in-with-their-work-or-school-account"></a>設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  此原則會決定使用者是否可以移除使用使用者的公司或學校帳戶自動登入的 Microsoft Edge 設定檔。

如果啟用此原則，則會使用使用者的公司或學校帳戶在 Windows 上建立非可移除的設定檔。 無法將此設定檔登出或移除。 只有使用與 OS 登入帳戶相符的內部部署帳戶或 Azure AD 帳戶登入設定檔時，設定檔才是不可刪除的。

如果停用或未設定此原則，則在 Windows 上使用使用者的公司或學校帳戶自動登入的設定檔可由使用者登出或移除。

如果想要設定瀏覽器登入，請使用 [BrowserSignin](#browsersignin) 原則。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上取得。

從 Microsoft Edge 89 開始，如果存在已停用同步處理的現有內部部署設定檔，且電腦已加入混合式連接，它會自動將內部部署設定檔升級至 Azure AD 設定檔，並將它設為不可刪除，而不是建立新的不可刪除的 Azure AD 設定檔。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：NonRemovableProfileEnabled
  - GP 名稱：設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NonRemovableProfileEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="overridesecurityrestrictionsoninsecureorigin"></a>OverrideSecurityRestrictionsOnInsecureOrigin

  #### <a name="control-where-security-restrictions-on-insecure-origins-apply"></a>控制不安全來源中安全性限制套用的地方

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定不安全來源的安全性限制不適用的來源 (URL) 的清單或主機名稱模式 (例如 "*.contoso.com")。

此原則可讓您為無法部署 TLS 的舊版應用程式指定允許的來源，或為內部網頁開發設定分段伺服器，使得開發人員不需在分段伺服器上部署 TLS，即可測試需要安全內容的功能。 此原則也可以防止來源在 omnibox 中被標示為「不安全」。

在此原則中設定 URL 清單，與將命令列旗標 '--unsafely-treat-insecure-origin-as-secure' 設定為相同 URL 以逗號分隔的清單具有相同效果。 如果啟用此原則，則會覆寫命令列旗標。

如需有關安全內容的詳細資訊，請參閱 https://www.w3.org/TR/secure-contexts/。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：OverrideSecurityRestrictionsOnInsecureOrigin
  - GP 名稱：控制不安全來源中安全性限制套用的地方
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = "http://testserver.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = "*.contoso.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：OverrideSecurityRestrictionsOnInsecureOrigin
  - 範例值：
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="paymentmethodqueryenabled"></a>PaymentMethodQueryEnabled

  #### <a name="allow-websites-to-query-for-available-payment-methods"></a>允許網站查詢可用的付款方式

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  允許您設定網站是否可以檢查使用者是否已儲存付款條件。

如果停用此原則，使用 PaymentRequest.canMakePayment 或 PaymentRequest.hasEnrolledInstrument API 的網站會收到通知，告知沒有可用的付款方式。

如果啟用此原則或未設定此原則，則網站可以檢查使用者是否已儲存付款條件。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PaymentMethodQueryEnabled
  - GP 名稱：允許網站查詢可用的付款方式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PaymentMethodQueryEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PaymentMethodQueryEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="personalizationreportingenabled"></a>PersonalizationReportingEnabled

  #### <a name="allow-personalization-of-ads-microsoft-edge-search-news-and-other-microsoft-services-by-sending-browsing-history-favorites-and-collections-usage-and-other-browsing-data-to-microsoft"></a>將瀏覽歷程記錄、我的最愛和收藏、使用狀況及其他瀏覽資料傳送給 Microsoft，以允許個人化廣告、Microsoft Edge、搜尋、新聞和其他 Microsoft 服務

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>說明

  此原則可防止 Microsoft 收集使用者的 Microsoft Edge 瀏覽歷程記錄、我的最愛和收藏、使用狀況，以及其他用於個人化廣告、搜尋、新聞、Microsoft Edge 和其他 Microsoft 服務的瀏覽資料。

子帳戶或企業帳戶無法使用此設定。

如果停用此原則，則使用者無法變更或覆寫設定。 如果啟用或未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PersonalizationReportingEnabled
  - GP 名稱：將瀏覽歷程記錄、我的最愛和收藏、使用狀況及其他瀏覽資料傳送給 Microsoft，以允許個人化廣告、Microsoft Edge、搜尋、新聞和其他 Microsoft 服務
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PersonalizationReportingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PersonalizationReportingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="pinningwizardallowed"></a>PinningWizardAllowed

  #### <a name="allow-pin-to-taskbar-wizard"></a>允許 [釘選到工作列精靈]

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  Microsoft Edge 使用 [釘選到工作列] 精靈來協助使用者將建議的網站釘選到工作列。 [釘選到工作列] 精靈功能預設會啟用，且可供使用者透過 [設定及其他] 功能表存取。

如果啟用此原則或未設定，則使用者可以從 [設定] 和 [更多] 功能表中呼叫 [釘選到工作列] 精靈。 也可以透過通訊協定啟動來呼叫精靈。

如果停用此原則，則會停用功能表中的 [釘選到工作列] 精靈，且無法再透過通訊協定啟動來呼叫。

沒有可用來啟用或停用 [釘選到工作列] 精靈的使用者設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PinningWizardAllowed
  - GP 名稱：允許 [釘選到工作列精靈]
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PinningWizardAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="proactiveauthenabled"></a>ProactiveAuthEnabled

  #### <a name="enable-proactive-authentication-obsolete"></a>啟用主動式驗證 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 90 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 90

  #### <a name="description"></a>說明

  此原則已過時，因為它無法獨立於瀏覽器登入而運作。 版本 90 之後，它無法于 Microsoft Edge 中使用。 如果想要設定瀏覽器登入，請使用 [BrowserSignin](#browsersignin) 原則。

讓您設定是否要在 Microsoft Edge 中開啟主動式驗證。

如果啟用此原則，則 Microsoft Edge 會嘗試使用登入瀏覽器的帳戶，順暢地向網站和服務進行驗證。

如果停用此原則，則 Microsoft Edge 不會嘗試使用單一登入 (SSO) 來向網站或服務進行驗證。 企業新索引標籤頁面之類已驗證的體驗將無法運作 (例如，最近和建議的 Office 文件將無法使用)。

如果未設定此原則，則會開啟主動式驗證。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ProactiveAuthEnabled
  - GP 名稱：啟用主動式驗證 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProactiveAuthEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ProactiveAuthEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="promotionaltabsenabled"></a>PromotionalTabsEnabled

  #### <a name="enable-full-tab-promotional-content"></a>啟用全分頁促銷內容

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制全分頁促銷或教育內容的呈現。 此設定可控制能夠協助使用者登入 Microsoft Edge、選擇其預設瀏覽器，或了解產品功能的歡迎頁面的呈現方式。

如果啟用此原則 (設定為 true) 或未設定，則 Microsoft Edge 可以向使用者顯示完整的索引標籤內容，以提供產品資訊。

如果您停用此原則 (設為 false)，則 Microsoft Edge 無法向使用者顯示完整的索引標籤內容。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PromotionalTabsEnabled
  - GP 名稱：啟用全分頁促銷內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PromotionalTabsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PromotionalTabsEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="promptfordownloadlocation"></a>PromptForDownloadLocation

  #### <a name="ask-where-to-save-downloaded-files"></a>詢問下載檔案的儲存位置

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定是否要在下載之前詢問儲存檔案的位置。

如果啟用此原則，則會在下載之前詢問使用者儲存每個檔案的位置；如果未設定，則檔案會自動儲存到預設位置，而不會詢問使用者。

如果未設定此原則，則使用者將可以變更此設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：PromptForDownloadLocation
  - GP 名稱：詢問下載檔案的儲存位置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PromptForDownloadLocation
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：PromptForDownloadLocation
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="quicallowed"></a>QuicAllowed

  #### <a name="allow-quic-protocol"></a>允許 QUIC 通訊協定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許在 Microsoft Edge 中使用 QUIC 通訊協定。

如果啟用此原則或未設定，則會允許 QUIC 通訊協定。

如果停用此原則，則會封鎖 QUIC 通訊協定。

QUIC 是傳輸層網路通訊協定，可改善目前使用 TCP 的 Web 應用程式效能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：QuicAllowed
  - GP 名稱：允許 QUIC 通訊協定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：QuicAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：QuicAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="quickviewofficefilesenabled"></a>QuickViewOfficeFilesEnabled

  #### <a name="manage-quickview-office-files-capability-in-microsoft-edge"></a>在 Microsoft Edge 中管理 QuickView Office 檔案功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  可讓您設定使用者是否可以在非 OneDrive 或 SharePoint 上的網頁上查看 Office 檔案。 (範例： Word 文件、PowerPoint 簡報及 Excel 試算表)

如果您啟用或未設定此原則，則可以使用 Office Viewer 在 Microsoft Edge 中查看這些檔案，而無須下載該檔案。

如果您停用這項原則，這些檔案將會被下載以供查看。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： QuickViewOfficeFilesEnabled
  - GP 名稱：管理 Microsoft Edge 中的 QuickView Office 檔功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： QuickViewOfficeFilesEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定金鑰名稱： QuickViewOfficeFilesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="redirectsitesfrominternetexplorerpreventbhoinstall"></a>RedirectSitesFromInternetExplorerPreventBHOInstall

  #### <a name="prevent-install-of-the-bho-to-redirect-incompatible-sites-from-internet-explorer-to-microsoft-edge"></a>防止安裝 BHO，將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  此設定可讓您指定是否封鎖瀏覽器協助程式物件 (BHO) 的安裝，該物件可針對需要新式瀏覽器的網站，將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge。

如果您啟用此原則，將不會安裝 BHO。 如果已安裝，將會在下一次 Microsoft Edge 更新時解除安裝。

如果未設定或已停用此原則，則會安裝 BHO。

需要 BHO，才能讓不相容的網站發生重新導向，但發生重新導向與否，也會由 [RedirectSitesFromInternetExplorerRedirectMode](#redirectsitesfrominternetexplorerredirectmode) 所控制。

如需此原則的詳細資訊，請參閱[https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RedirectSitesFromInternetExplorerPreventBHOInstall
  - GP 名稱：防止安裝 BHO，將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RedirectSitesFromInternetExplorerPreventBHOInstall
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="redirectsitesfrominternetexplorerredirectmode"></a>RedirectSitesFromInternetExplorerRedirectMode

  #### <a name="redirect-incompatible-sites-from-internet-explorer-to-microsoft-edge"></a>將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  此設定可讓您指定 Internet Explorer 是否會將需要新式瀏覽器的網站瀏覽重新導向至 Microsoft Edge。

如果您未設定此原則或將它設定為 'Sitelist' (從 M87 開始)，Internet Explorer 會將需要新式瀏覽器的網站重新導向至 Microsoft Edge。

將網站從 Internet Explorer 重新導向至 Microsoft Edge 時，開始載入網站的 Internet Explorer 索引標籤如果沒有之前的內容，就會關閉。 否則會瀏覽至 Microsoft 說明頁面，其中會說明網站為什麼重新導向至 Microsoft Edge。

當 Microsoft Edge 啟動以從 IE 載入網站時，會向使用者顯示資訊列，說明該網站在新式瀏覽器中會有最佳效果。

如果將此原則設定為 'Disable'，Internet Explorer 不會將任何流量重新導向至 Microsoft Edge。

如需此原則的詳細資訊，請參閱[https://go.microsoft.com/fwlink/?linkid=2141715](https://go.microsoft.com/fwlink/?linkid=2141715)

原則選項對應：

* Disable (0) = 停用

* Sitelist (1) = 根據不相容的網站 sitelist 重新導向網站

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RedirectSitesFromInternetExplorerRedirectMode
  - GP 名稱：將不相容的網站從 Internet Explorer 重新導向至 Microsoft Edge
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：RedirectSitesFromInternetExplorerRedirectMode
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="relaunchnotification"></a>RelaunchNotification

  #### <a name="notify-a-user-that-a-browser-restart-is-recommended-or-required-for-pending-updates"></a>通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  通知使用者他們必須將 Microsoft Edge 重新啟動，才能套用擱置中的更新。

如果未設定此原則，則 Microsoft Edge 會在頂端功能表列的最右側加上回收圖示，提示使用者重新啟動瀏覽器以套用更新。

如果啟用此原則，並將其設定為 '建議'，則會出現重複的警告，提示使用者建議重新開機。 使用者可以關閉此警告，並將重新開機延遲。

如果將原則設定為 '必要'，會出現重複的警告，提示使用者當通知期間過後，瀏覽器將會自動重新啟動。 預設期間為七天。 您可以使用 [RelaunchNotificationPeriod](#relaunchnotificationperiod) 原則來設定此期間。

使用者的工作階段會在瀏覽器重新啟動後還原。

原則選項對應：

* 建議 (1) = 建議 - 向使用者顯示重複的提示，指出建議重新啟動

* 必要 (2) = 必要 - 向使用者顯示重複的提示，指出必須重新啟動

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RelaunchNotification
  - GP 名稱：通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RelaunchNotification
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RelaunchNotification
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="relaunchnotificationperiod"></a>RelaunchNotificationPeriod

  #### <a name="set-the-time-period-for-update-notifications"></a>設定更新通知的時間週期

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  讓您設定時間期間 (以毫秒為單位)，經過此時間後便通知使用者必須重新啟動 Microsoft Edge，才能套用擱置中的更新。

在此時間期間內，使用者將會重複收到需要更新的通知。 在 Microsoft Edge 中，經過通知期間的三分之一後，應用程式功能表會變更，以指出需要重新啟動。 此通知會在經過通知期間的三分之二後變更色彩，並在經過整個通知期間後再次變更色彩。 由 [RelaunchNotification](#relaunchnotification) 原則啟用的額外通知會遵循此相同的排程。

如果未設定，則會使用預設的 604800000 毫秒 (一週)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RelaunchNotificationPeriod
  - GP 名稱：設定更新通知的時間週期
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RelaunchNotificationPeriod
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x240c8400
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RelaunchNotificationPeriod
  - 範例值：
``` xml
<integer>604800000</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="renderercodeintegrityenabled"></a>RendererCodeIntegrityEnabled

  #### <a name="enable-renderer-code-integrity"></a>啟用轉譯器程式碼完整性

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  將原則設定為 [啟用] 或未設定，就會開啟 [轉譯器程式碼完整性]。
將原則設定為 [停用] 會對 Microsoft Edge 的安全性和穩定性造成不良的影響，因為可能會在 Microsoft Edge 轉譯器程序中載入未知和可能有害的程式碼。 只有在必須在 Microsoft Edge 轉譯器程序內執行的協力廠商軟體發生相容性問題時，才關閉原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RendererCodeIntegrityEnabled
  - GP 名稱：啟用轉譯器程式碼完整性
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RendererCodeIntegrityEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="requireonlinerevocationchecksforlocalanchors"></a>RequireOnlineRevocationChecksForLocalAnchors

  #### <a name="specify-if-online-ocspcrl-checks-are-required-for-local-trust-anchors"></a>指定本機信賴起點是否需要線上 OCSP/CRL 檢查

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制是否需要線上撤銷檢查 (OCSP/CRL 檢查)。 如果 Microsoft Edge 無法取得撤銷狀態資訊，則會將這些憑證視為已撤銷 (「封鎖性失敗」)。

如果啟用此原則，則 Microsoft Edge 一律會針對成功驗證且由本機安裝的 CA 憑證簽署的伺服器憑證執行撤銷檢查。

如果未設定或停用此原則，則 Microsoft Edge 會使用現有的線上撤銷檢查設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RequireOnlineRevocationChecksForLocalAnchors
  - GP 名稱：指定本機信賴起點是否需要線上 OCSP/CRL 檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RequireOnlineRevocationChecksForLocalAnchors
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="resolvenavigationerrorsusewebservice"></a>ResolveNavigationErrorsUseWebService

  #### <a name="enable-resolution-of-navigation-errors-using-a-web-service"></a>啟用使用 Web 服務來解決導覽錯誤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許 Microsoft Edge 向 Web 服務發出無資料連線，以便在旅館和機場 Wi-Fi 之類情況下探測網路的連線能力。

如果啟用此原則，則會使用 Web 服務來進行網路連線測試。

如果停用此原則，則 Microsoft Edge 會使用原生 API 來嘗試解決網路連線和瀏覽問題。

**注意**：除了在 Windows 8 和更新版本的 Windows 上，Microsoft Edge *一律*會使用本機 API 來解決連線問題。

如果未設定此原則，則 Microsoft Edge 會遵守 edge://settings/privacy 的 [服務] 底下所設定的使用者喜好設定。
具體來說，有一個使用者可以開啟或關閉的 [使用網頁服務協助您解決瀏覽錯誤]**** 切換。 請注意，如果已啟用此原則 (ResolveNavigationErrorsUseWebService)，[使用網頁服務協助您解決瀏覽錯誤]**** 設定會開啟，但使用者無法使用切換來變更設定。 如果已停用此原則，則 [使用網頁服務協助您解決瀏覽錯誤]**** 設定會關閉，且使用者無法使用切換來變更設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ResolveNavigationErrorsUseWebService
  - GP 名稱：啟用使用 Web 服務來解決導覽錯誤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ResolveNavigationErrorsUseWebService
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ResolveNavigationErrorsUseWebService
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="restrictsignintopattern"></a>RestrictSigninToPattern

  #### <a name="restrict-which-accounts-can-be-used-as-microsoft-edge-primary-accounts"></a>限制哪些帳戶可用為 Microsoft Edge 主要帳戶

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  決定可以將哪些帳戶設為 Microsoft Edge 中的瀏覽器主要帳戶 (在同步選擇加入流程中選取的帳戶)。

如果使用者嘗試使用不符合此模式的使用者名稱設定瀏覽器主要帳戶，則會封鎖使用者並顯示適當的錯誤訊息。 您可以使用此模式的 Perl 樣式規則運算式，將此原則設定為符合多個帳戶。 請注意，模式比對會區分大小寫。 如需使用的規則運算式規則之詳細資訊，請參閱 https://go.microsoft.com/fwlink/p/?linkid=2133903

如果未設定此原則或將它保留為空白，則使用者可以將任何帳戶設定為 Microsoft Edge 中的瀏覽器主要帳戶。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RestrictSigninToPattern
  - GP 名稱：限制哪些帳戶可用為 Microsoft Edge 主要帳戶
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RestrictSigninToPattern
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
".*@contoso.com"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RestrictSigninToPattern
  - 範例值：
``` xml
<string>.*@contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="roamingprofilelocation"></a>RoamingProfileLocation

  #### <a name="set-the-roaming-profile-directory"></a>設定漫遊設定檔目錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  設定用來儲存設定檔快取複本的目錄。

Microsoft Edge 會使用已提供的目錄，儲存設定檔的快取複本，若您在啟用此原則時同時也啟用[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)原則。 若您停用或未設定 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 原則，系統將不會使用儲存在此原則中的值。

如欲知道您可使用的變數清單，請參照[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果您並未設定此原則，系統將會使用預設的快取設定檔路徑。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RoamingProfileLocation
  - GP 名稱：設定快取設定檔目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RoamingProfileLocation
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"${roaming_app_data}\\edge-profile"
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="roamingprofilesupportenabled"></a>RoamingProfileSupportEnabled

  #### <a name="enable-using-roaming-copies-for-microsoft-edge-profile-data"></a>啟用 Microsoft Edge 設定檔資料的快取副本

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 85 或更新版本

  #### <a name="description"></a>描述

  啟用此原則以使用 Windows 上的快取設定檔。 儲存在 Microsoft Edge 設定檔 ([我的最愛] 和 [喜好設定]) 中的設定，也會儲存至 [漫遊使用者設定檔] 資料夾中儲存的檔案 (或由系統管理員透過 [RoamingProfileLocation](#roamingprofilelocation) 原則所指定的位置)。

如果您停用或未設定此原則，系統只會使用標準本機設定檔。

[SyncDisabled](#syncdisabled)只會停用雲端同步處理，而不會影響此原則。

如需使用漫遊使用者設定檔的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2150058](https://go.microsoft.com/fwlink/?linkid=2150058)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RoamingProfileSupportEnabled
  - GP 名稱：啟用 Microsoft Edge 設定檔資料的快取副本
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RoamingProfileSupportEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="runallflashinallowmode"></a>RunAllFlashInAllowMode

  #### <a name="extend-adobe-flash-content-setting-to-all-content-obsolete"></a>將 Adobe Flash 內容設定延伸至所有內容 (已過時)

  
  >已過時：此原則已過時且無法在 Microsoft Edge 88 之後運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 88

  #### <a name="description"></a>描述

  由於 Microsoft Edge 不再支援 Flash，因此此原則不再有作用。

如果啟用此原則，在內容設定中設為允許 Adobe Flash 的網站中內嵌的所有 Adobe Flash 內容 (無論是由使用者或企業原則設定) 將會執行。 這包含來自其他來源和/或小型內容的內容。

若要控制允許哪些網站執行 Adobe Flash，請參閱 [DefaultPluginsSetting](#defaultpluginssetting)、[PluginsAllowedForUrls](#pluginsallowedforurls) 和 [PluginsBlockedForUrls](#pluginsblockedforurls) 原則中的規格。

如果停用或未設定此原則，則可能會封鎖來自其他來源 (以上提及的三個原則中未指定的網站) 的 Adobe Flash 或少量內容。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：RunAllFlashInAllowMode
  - GP 名稱：將 Adobe Flash 內容設定延伸至所有內容 (過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RunAllFlashInAllowMode
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：RunAllFlashInAllowMode
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sslerroroverrideallowed"></a>SSLErrorOverrideAllowed

  #### <a name="allow-users-to-proceed-from-the-https-warning-page"></a>允許使用者從 HTTPS 警告頁面繼續進行

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  當使用者造訪含有 SSL 錯誤的網站時，Microsoft Edge 會顯示警告頁面。

如果啟用或未設定 (預設) 此原則，則使用者可以點選這些警告頁面。

如果停用此原則，則會封鎖使用者，使其無法點選任何警告頁面。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SSLErrorOverrideAllowed
  - GP 名稱：允許使用者從 HTTPS 警告頁面繼續進行
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SSLErrorOverrideAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SSLErrorOverrideAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sslerroroverrideallowedfororigins"></a>SSLErrorOverrideAllowedForOrigins

  #### <a name="allow-users-to-proceed-from-the-https-warning-page-for-specific-origins"></a>允許使用者從特定來源的 HTTPS 警告頁面繼續進行

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 90 或更新版本

  #### <a name="description"></a>描述

  當使用者造訪含有 SSL 錯誤的網站時，Microsoft Edge 會顯示警告頁面。

如果您啟用或未設定 [SSLErrorOverrideAllowed](#sslerroroverrideallowed) 原則，則此原則不會執行任何動作。

如果您停用 [SSLErrorOverrideAllowed](#sslerroroverrideallowed) 原則，則設定此原則可讓您設定網站的來源模式清單，在其中使用者可以繼續點選 SSL 錯誤頁面。 使用者無法在來源不在此清單上的 SSL 錯誤頁面上點選。

如果您未設定此原則，則 [SSLErrorOverrideAllowed](#sslerroroverrideallowed) 原則會適用所有網站。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 * 不是此原則可接受的值。 此原則只會根據來源進行比對，因此將忽略 URL 模式中的任何路徑或查詢。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SSLErrorOverrideAllowedForOrigins
  - GP 名稱：允許使用者從特定來源的 HTTPS 警告頁面繼續進行
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins\1 = "https://www.example.com"
SOFTWARE\Policies\Microsoft\Edge\SSLErrorOverrideAllowedForOrigins\2 = "[*.]example.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SSLErrorOverrideAllowedForOrigins
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sslversionmin"></a>SSLVersionMin

  #### <a name="minimum-tls-version-enabled-deprecated"></a>已啟用最小 TLS 版本 (已取代)

  >已取代：此原則已被取代。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  自版本 91 起 (大約 2021 年 5 月左右)，系統會從 Microsoft Edge 移除對隱藏 TLS 1.0/1.1 警告的支援，屆時此原則將會停止運作。

設定支援的最小 TLS 版本。 如果您未設定此原則，Microsoft Edge 將顯示 TLS 1.0 和 TLS 1.1 的錯誤，但使用者將可以略過這個錯誤。

設定時，Microsoft Edge 不會使用低於指定版本的任何 SSL/TLS 版本。 任何無法辨識的值都會被忽略。

原則選項對應：

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SSLVersionMin
  - GP 名稱：已啟用最小 TLS 版本 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SSLVersionMin
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"tls1"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SSLVersionMin
  - 範例值：
``` xml
<string>tls1</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="savecookiesonexit"></a>SaveCookiesOnExit

  #### <a name="save-cookies-when-microsoft-edge-closes"></a>在 Microsoft Edge 關閉時儲存 Cookie

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  啟用此原則時，瀏覽器關閉時，指定的 Cookie 集合不會遭到刪除。 這個原則只有在下列情況下才有效：
- 在 [設定/隱私權與服務/清除瀏覽資料] 中設定 [Cookies 及其他網站資料] 切換按鈕為關閉或
- 已啟用原則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 或
- 原則 [DefaultCookiesSetting](#defaultcookiessetting) 設定為 ‘在工作階段期間保留 Cookie’。

您可以根據 URL 模式定義要在多個工作階段之間保留 Cookie 的網站清單。

請注意：使用者仍然可以編輯 Cookie 網站清單，以新增或移除 URL。 不過，他們無法移除由系統管理員新增的 URL。

如果您啟用此原則，瀏覽器關閉時，Cookie 清單就不會被清除。

如果您停用或未設定此原則，則會使用使用者的個人設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SaveCookiesOnExit
  - GP 名稱：在 Microsoft Edge 關閉時儲存 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SaveCookiesOnExit
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="savingbrowserhistorydisabled"></a>SavingBrowserHistoryDisabled

  #### <a name="disable-saving-browser-history"></a>停用儲存瀏覽器歷程記錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  停用儲存瀏覽器歷程記錄，並防止使用者變更此設定。

如果啟用此原則，則不會儲存瀏覽歷程記錄。 這也會停用索引標籤同步。

如果停用或未設定此原則，則會儲存瀏覽歷程記錄。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SavingBrowserHistoryDisabled
  - GP 名稱：停用儲存瀏覽器歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SavingBrowserHistoryDisabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SavingBrowserHistoryDisabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="screencaptureallowed"></a>ScreenCaptureAllowed

  #### <a name="allow-or-deny-screen-capture"></a>允許或拒絕螢幕擷取畫面

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則或未設定此原則，則網頁可使用螢幕共用 API (例如 getDisplayMedia () 或桌面擷取擴充功能 API) 來進行螢幕擷取。
如果停用此原則，則對螢幕共用 API 的呼叫將會失敗。 例如，如果您正在使用網路線上會議，視訊或螢幕共用將無法運作。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ScreenCaptureAllowed
  - GP 名稱：允許或拒絕螢幕擷取畫面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ScreenCaptureAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ScreenCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="scrolltotextfragmentenabled"></a>ScrollToTextFragmentEnabled

  #### <a name="enable-scrolling-to-text-specified-in-url-fragments"></a>啟用捲動至在 URL 片段中指定的文字

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>描述

  此功能會超連結和網址列 URL 導覽以網頁上的特定文字為目標，這會在網頁載入完成之後進行捲動。

如果啟用或未設定此原則，則會啟用透過 URL 將網頁捲動至特定文字片段的功能。

如果停用此原則，則會停用透過 URL 將網頁捲動至特定文字片段的功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ScrollToTextFragmentEnabled
  - GP 名稱：啟用捲動至在 URL 片段中指定的文字
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ScrollToTextFragmentEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ScrollToTextFragmentEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="searchsuggestenabled"></a>SearchSuggestEnabled

  #### <a name="enable-search-suggestions"></a>啟用搜尋建議

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 的網址列和自動建議清單中啟用網頁搜尋建議，並防止使用者變更此原則。

如果啟用此原則，則會使用 Web 搜尋建議。

如果停用此原則，則永遠不會使用 Web 搜尋建議，不過仍會顯示本機歷程記錄和本機我的最愛建議。 如果停用此原則，則不會在對 Microsoft 的遙測中包含所輸入的字元和所造訪的 URL。

如果將此原則保留為未設定，則會啟用搜尋建議，但使用者可以變更。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SearchSuggestEnabled
  - GP 名稱：啟用搜尋建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SearchSuggestEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SearchSuggestEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="securitykeypermitattestation"></a>SecurityKeyPermitAttestation

  #### <a name="websites-or-domains-that-dont-need-permission-to-use-direct-security-key-attestation"></a>不需要權限即可使用直接存取安全性金鑰證明的網站或網域

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  指定要求來自安全性金鑰的證明憑證時，不需要明確使用者權限的網站和網域。 此外，傳送信號給安全性金鑰，指出它可以使用個別證明。 如果沒有此動作，每次網站要求安全性金鑰的證明時，即會提示使用者。

網站 (例如 https://contoso.com/some/path) 僅符合 U2F appID。 網域 (例如 contoso.com) 僅符合 webauthn RP 識別碼。 若要涵蓋特定網站的 U2F 和 webauthn API，您需要列出 appID URL 和網域。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SecurityKeyPermitAttestation
  - GP 名稱：不需要權限即可使用直接存取安全性金鑰證明的網站或網域
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = "https://contoso.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SecurityKeyPermitAttestation
  - 範例值：
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sendintranettointernetexplorer"></a>SendIntranetToInternetExplorer

  #### <a name="send-all-intranet-sites-to-internet-explorer"></a>將所有內部網路網站傳送到 Internet Explorer

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SendIntranetToInternetExplorer
  - GP 名稱：將所有內部網路網站傳送到 Internet Explorer
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SendIntranetToInternetExplorer
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sendsiteinfotoimproveservices"></a>SendSiteInfoToImproveServices

  #### <a name="send-site-information-to-improve-microsoft-services-obsolete"></a>傳送網站資訊以改善 Microsoft 服務 (已淘汰)

  
  >已過時：此原則已過時且無法在 Microsoft Edge 88 之後運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 至 88

  #### <a name="description"></a>描述

  已不再支援此原則。 它被 [DiagnosticData](#diagnosticdata) (用於 Windows 7、Windows 8 和 macOS) 取代，並允許在 Win 10 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)) 上進行遙測。

此原則允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善服務 (如搜尋)。

啟用此原則，以傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 停用此原則，以不要傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

在 Windows 10 上，如果未設定此原則，則 Microsoft Edge 將預設為使用 Windows 診斷資料設定。 如果啟用此原則，而且 Windows 診斷資料設定設為「完整」時，Microsoft Edge 將僅傳送有關在 Microsoft Edge 中所造訪網站的資訊。 如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。 深入了解 Windows 診斷資料設定：[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

在 Windows 7、Windows 8 和 macOS 上，此原則會控制所造訪網站相關資訊的傳送。 如果未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

若要啟用此原則，[MetricsReportingEnabled](#metricsreportingenabled) 必須設定為 [已啟用]。 如果 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 或 [MetricsReportingEnabled](#metricsreportingenabled) 未設定或已停用，將不會將此資料傳送到 Microsoft。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SendSiteInfoToImproveServices
  - GP 名稱：傳送網站資訊以改善 Microsoft 服務 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SendSiteInfoToImproveServices
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SendSiteInfoToImproveServices
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sensorsallowedforurls"></a>SensorsAllowedForUrls

  #### <a name="allow-access-to-sensors-on-specific-sites"></a>允許存取特定網站上的感應器

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  根據 URL 模式，定義可以存取及使用感應器 (如動作和光線感應器) 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultSensorsSetting](#defaultsensorssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

針對未符合此原則的 URL 模式，使用的優先順序依序為：[SensorsBlockedForUrls](#sensorsblockedforurls) 原則 (若符合的話)、[DefaultSensorsSetting](#defaultsensorssetting) 原則 (若有設定)、或使用者的個人設定值。

在此原則中定義的 URL 模式不能與 [SensorsBlockedForUrls](#sensorsblockedforurls) 原則中的設定相衝突。 您不能將 URL 同時設定為允許和封鎖。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SensorsAllowedForUrls
  - GP 名稱：允許存取特定網站上的感應器
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsAllowedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SensorsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sensorsblockedforurls"></a>SensorsBlockedForUrls

  #### <a name="block-access-to-sensors-on-specific-sites"></a>封鎖存取特定網站上的感應器

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  根據 URL 模式，定義不可存取感應器 (例如動作和光線感應器) 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultSensorsSetting](#defaultsensorssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

針對未符合此原則的 URL 模式，使用的優先順序依序為：[SensorsAllowedForUrls](#sensorsallowedforurls) 原則 (若符合的話)、[DefaultSensorsSetting](#defaultsensorssetting) 原則 (若有設定)、或使用者的個人設定值。

在此原則中定義的 URL 模式不能與 [SensorsAllowedForUrls](#sensorsallowedforurls) 原則中的設定相衝突。 您不能將 URL 同時設定為允許和封鎖。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SensorsBlockedForUrls
  - GP 名稱：封鎖存取特定網站上的感應器
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SensorsBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SensorsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="serialaskforurls"></a>SerialAskForUrls

  #### <a name="allow-the-serial-api-on-specific-sites"></a>允許特定網站的 Serial API

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義可要求使用者取得序列通訊埠存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultSerialGuardSetting](#defaultserialguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

針對未符合此原則的 URL 模式，使用的優先順序依序為：[SerialBlockedForUrls ](#serialblockedforurls) 原則 (若符合的話)、 [DefaultSerialGuardSetting ](#defaultserialguardsetting) 原則 (若有設定)、或使用者的個人設定值。

在此原則中定義的 URL 模式不可與 [SerialBlockedForUrls](#serialblockedforurls) 原則中的設定相衝突。 您不能將 URL 同時設定為允許和封鎖。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SerialAskForUrls
  - GP 名稱：允許特定網站的 Serial API
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialAskForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SerialAskForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="serialblockedforurls"></a>SerialBlockedForUrls

  #### <a name="block-the-serial-api-on-specific-sites"></a>封鎖特定網站的 Serial API

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義無法要求使用者授與其序列通訊埠存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultSerialGuardSetting](#defaultserialguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

針對未符合此原則的 URL 模式，使用的優先順序依序為：[SerialAskForUrls](#serialaskforurls) 原則 (若符合的話)、[DefaultSerialGuardSetting](#defaultserialguardsetting) 原則 (若有設定)、或使用者的個人設定值。

在此原則中定義的 URL 模式不能與 [SerialAskForUrls](#serialaskforurls) 原則中的設定相衝突。 您不能將 URL 同時設定為允許和封鎖。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SerialBlockedForUrls
  - GP 名稱：封鎖特定網站的 Serial API
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\SerialBlockedForUrls\2 = "[*.]contoso.edu"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SerialBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="sharedarraybufferunrestrictedaccessallowed"></a>SharedArrayBufferUnrestrictedAccessAllowed

  #### <a name="specifies-whether-sharedarraybuffers-can-be-used-in-a-non-cross-origin-isolated-context"></a>指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 91 或更新版本

  #### <a name="description"></a>說明

  指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用。  SharedArrayBuffer 是二進位資料緩衝區，可用來在共用記憶體上建立視圖。  SharedArrayBuffers 在數個熱門 CPU 中具有記憶體存取弱點。

如果啟用此原則，則允許網站使用 SharedArrayBuffers。

如果您停用或未設定此原則，則網站會防止 SharedArrayBuffers 的使用。

基於 Web 相容性考慮，使用來自 Microsoft Edge 91 以上版本的 SharedArrayBuffers 時，Microsoft Edge 將需要跨來源隔離。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SharedArrayBufferUnrestrictedAccessAllowed
  - GP 名稱：指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SharedArrayBufferUnrestrictedAccessAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SharedArrayBufferUnrestrictedAccessAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="showmicrosoftrewards"></a>ShowMicrosoftRewards

  #### <a name="show-microsoft-rewards-experiences"></a>顯示 Microsoft Rewards 體驗

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  顯示 Microsoft Rewards 體驗和通知。
如果啟用此原則：
   - 搜尋和贏得市場中的 Microsoft 帳戶使用者 (不包括 Azure AD 帳戶)，將在其 Microsoft Edge 使用者設定檔中看到 Microsoft Rewards 體驗。
   - 用來在 Microsoft Edge 設定中啟用 Microsoft Rewards 的設定，將會啟用並切換為開啟。

如果停用此原則：
   - 搜尋和贏得市場中的 Microsoft 帳戶使用者 (不包括 Azure AD 帳戶)，將不會在其 Microsoft Edge 使用者設定檔中看到 Microsoft Rewards 體驗。
   - 用來在 Microsoft Edge 設定中啟用 Microsoft Rewards 的設定，將會停用並切換為關閉。

如果未設定此原則：
   - 搜尋和贏得市場中的 Microsoft 帳戶使用者 (不包括 Azure AD 帳戶)，將在其 Microsoft Edge 使用者設定檔中看到 Microsoft Rewards 體驗。
   - 用來在 Microsoft Edge 設定中啟用 Microsoft Rewards 的設定，將會啟用並切換為開啟。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ShowMicrosoftRewards
  - GP 名稱：顯示 Microsoft Rewards 體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ShowMicrosoftRewards
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ShowMicrosoftRewards
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="showofficeshortcutinfavoritesbar"></a>ShowOfficeShortcutInFavoritesBar

  #### <a name="show-microsoft-office-shortcut-in-favorites-bar-deprecated"></a>在 [我的最愛] 列中顯示 Microsoft Office 捷徑 (已取代)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  由於操作要求的變更，此原則無法按預期運作。 此值已過時，而且不應該使用。

指定是否要在我的最愛列中加入 Office.com 的捷徑。 針對登入 Microsoft Edge 的使用者，快捷方式會將使用者帶入其 Microsoft Office app 和檔中。如果您啟用或未設定此原則，則使用者可以在 [我的最愛] 工具列內容功能表中，選擇是否要看到快速鍵。
如果您停用此原則，就不會顯示捷徑。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ShowOfficeShortcutInFavoritesBar
  - GP 名稱：在 [我的最愛] 列中顯示 Microsoft Office 捷徑 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ShowOfficeShortcutInFavoritesBar
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ShowOfficeShortcutInFavoritesBar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="showrecommendationsenabled"></a>ShowRecommendationsEnabled

  #### <a name="allow-recommendations-and-promotional-notifications-from-microsoft-edge"></a>允許來自 Microsoft Edge 的建議和促銷通知

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  此政策設定可讓您決定是否讓員工收到來自 Microsoft Edge 的建議和產品內協助通知。

如果您啟用或不設定此設定，員工會收到來自 Microsoft Edge 的建議/通知。

如果您停用這項設定，員工將不會收到來自 Microsoft Edge 的任何建議/通知。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ShowRecommendationsEnabled
  - GP 名稱：允許來自 Microsoft Edge 的建議及促銷通知
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：ShowRecommendationsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：ShowRecommendationsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="signedhttpexchangeenabled"></a>SignedHTTPExchangeEnabled

  #### <a name="enable-signed-http-exchange-sxg-support"></a>啟用 Signed HTTP Exchange (SXG) 支援

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>描述

  啟用 Signed HTTP Exchange (SXG) 的支援。

如果未設定或已啟用此原則，則 Microsoft Edge 會接受將網頁內容做為 Signed HTTP Exchange。

如果將此原則設為已停用，則無法載入 Signed HTTP Exchange。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SignedHTTPExchangeEnabled
  - GP 名稱：啟用 Signed HTTP Exchange (SXG) 支援
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SignedHTTPExchangeEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SignedHTTPExchangeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="siteperprocess"></a>SitePerProcess

  #### <a name="enable-site-isolation-for-every-site"></a>為每個網站啟用網站隔離

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  'SitePerProcess' 原則可用於防止使用者選擇退出隔離所有網站的預設行為。 請注意，您也可以使用 [IsolateOrigins](#isolateorigins) 原則來隔離其他更精細的來源。

如果啟用此原則，則使用者將無法選擇退出每個網站都是以自己的處理程序執行的預設行為。

如果您停用或未設定此原則，使用者可以選擇退出網站隔離。  (例如，使用 edge://flags 中的 [停用網站隔離] 項目。) 停用原則或未設定原則，並無法關閉網站隔離。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SitePerProcess
  - GP 名稱：為每個網站啟用網站隔離
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SitePerProcess
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SitePerProcess
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="smartactionsblocklist"></a>SmartActionsBlockList

  #### <a name="block-smart-actions-for-a-list-of-services"></a>封鎖服務清單的智慧型動作

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 89 或更新版本

  #### <a name="description"></a>說明

  列出不顯示智慧型動作的特定服務，如 PDF。 (智慧型動作是「定義」之類的動作，可在 Microsoft Edge 的完整和迷你操作功能表中使用。)

如果您啟用原則：
   - 對於與指定清單相符服務之所有設定檔，將停用迷你和完整操作功能表中的智慧型動作。
   - 對於與指定清單相符的服務，使用者將不會在文字選取的迷你和完整操作功能表中看到智慧型動作。
   - 在 Microsoft Edge 設定中，對於與指定清單相符的服務，將停用迷你和完整操作功能表中的智慧型動作。

如果停用或未設定此原則：
   - 將為所有設定檔啟用迷你和完整操作功能表中的智慧型動作。
   - 使用者將在文字選取的迷你和完整操作功能表中看到智慧型動作。
   - 在 Microsoft Edge 設定中，將啟用迷你和完整操作功能表中的智慧型動作。

原則選項對應：

* smart_actions_pdf (smart_actions_pdf) = PDF 中的智慧型動作

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SmartActionsBlockList
  - GP 名稱：封鎖服務清單的智慧型動作
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SmartActionsBlockList
  - (建議) 的路徑： SOFTWARE\Policies\Microsoft\Edge\Recommended\SmartActionsBlockList
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SmartActionsBlockList\1 = "smart_actions_pdf"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SmartActionsBlockList
  - 範例值：
``` xml
<array>
  <string>smart_actions_pdf</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="speechrecognitionenabled"></a>SpeechRecognitionEnabled

  #### <a name="configure-speech-recognition"></a>Configure Speech Recognition

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  設定網站是否可以使用 W3C Web 語音 API 來辨識使用者的語音。 Microsoft Edge 的 Web 語音 API 實施使用 Azure 認知服務，因此語音資料將離開電腦。

如果您啟用或未設定此原則，使用 Web 語音 API 的 web 型應用程式可以使用語音辨識。

如果您停用這項原則，就無法透過網頁語音 API 使用語音辨識。

若要深入了解此功能，請參閱這裡：SpeechRecognition API：[https://go.microsoft.com/fwlink/?linkid=2143388](https://go.microsoft.com/fwlink/?linkid=2143388) 認知服務：[https://go.microsoft.com/fwlink/?linkid=2143680](https://go.microsoft.com/fwlink/?linkid=2143680)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP unique name: SpeechRecognitionEnabled
  - GP name: Configure Speech Recognition
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - Value Name: SpeechRecognitionEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - Preference Key Name: SpeechRecognitionEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="spellcheckenabled"></a>SpellcheckEnabled

  #### <a name="enable-spellcheck"></a>啟用拼字檢查

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  如果啟用或未設定此原則，則使用者可以使用拼字檢查。

如果停用此原則，則使用者無法使用拼字檢查，且會停用 [SpellcheckLanguage](#spellchecklanguage) 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SpellcheckEnabled
  - GP 名稱：啟用拼字檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SpellcheckEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SpellcheckEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="spellchecklanguage"></a>SpellcheckLanguage

  #### <a name="enable-specific-spellcheck-languages"></a>啟用特定拼字檢查語言

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  啟用不同語言的拼字檢查。 將忽略您指定、無法辨識的任何語言。

如果啟用此原則，則會針對指定的語言及使用者啟用的任何語言啟用拼字檢查。

如果未設定或停用此原則，則不會對使用者的拼字檢查喜好設定進行任何變更。

如果 [SpellcheckEnabled](#spellcheckenabled) 原則為已停用，則此原則沒有作用。

如果在 'SpellcheckLanguage' 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 原則中同時包含某個語言，則會啟用該拼字檢查語言。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SpellcheckLanguage
  - GP 名稱：啟用特定拼字檢查語言
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = "es"

```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="spellchecklanguageblocklist"></a>SpellcheckLanguageBlocklist

  #### <a name="force-disable-spellcheck-languages"></a>強制停用拼字檢查語言

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 78 或更新版本

  #### <a name="description"></a>說明

  強制停用拼字檢查語言。 該清單中無法辨識的語言將會被忽略。

如果啟用此原則，則會針對指定的語言停用拼字檢查。 使用者仍可以為清單中沒有的語言啟用或停用拼字檢查。

如果未設定此原則或停用，則不會對使用者的拼字檢查喜好設定進行任何變更。

如果 [SpellcheckEnabled](#spellcheckenabled) 原則設為已停用，則此原則沒有作用。

如果在 [SpellcheckLanguage](#spellchecklanguage) 和 'SpellcheckLanguageBlocklist' 原則中同時包含某個語言，則會啟用該拼字檢查語言。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SpellcheckLanguageBlocklist
  - GP 名稱：強制停用拼字檢查語言
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = "fr"
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = "es"

```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="strictermixedcontenttreatmentenabled"></a>StricterMixedContentTreatmentEnabled

  #### <a name="enable-stricter-treatment-for-mixed-content-obsolete"></a>針對混合內容啟用更嚴格的處理 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 81 至 84

  #### <a name="description"></a>描述

  此原則無法運作，因為此原則只是要做為短期機制，用於讓企業在發現其 Web 內容與較嚴格的混合式內容處理不相容時，可以有更多時間來更新其 Web 內容。

此原則可控制在瀏覽器中處理混合式內容 (HTTPS 網站中的 HTTP 內容) 的方式。

如果將此原則設定為 true 或未設定，音訊和視訊混合內容將會自動升級為 HTTPS (也就是說，URL 將會重寫為 HTTPS，且如果資源無法透過 HTTPS 使用，也不會遞補)，且會在影像混合內容的 URL 列中顯示「不安全」警告。

如果將原則設定為 false，則會停用音訊和視訊的自動升級，且不會顯示影像的警告。

此原則不會影響音訊、視訊和影像以外的其他類型混合內容。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：StricterMixedContentTreatmentEnabled
  - GP 名稱：針對混合內容啟用更嚴格的處理 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：StricterMixedContentTreatmentEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：StricterMixedContentTreatmentEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="suppressunsupportedoswarning"></a>SuppressUnsupportedOSWarning

  #### <a name="suppress-the-unsupported-os-warning"></a>隱藏不支援的 OS 警告

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  隱藏當 Microsoft Edge 於已不再受支援的電腦或作業系統上執行時將會顯示的警告。

如果此原則為 false 或未設定，則會在這類不受支援的電腦或作業系統中顯示警告。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SuppressUnsupportedOSWarning
  - GP 名稱：隱藏不支援的 OS 警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SuppressUnsupportedOSWarning
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SuppressUnsupportedOSWarning
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="syncdisabled"></a>SyncDisabled

  #### <a name="disable-synchronization-of-data-using-microsoft-sync-services"></a>透過 Microsoft 同步服務停用資料同步

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  停用 Microsoft Edge 中的資料同步。 此原則也會防止顯示同步同意提示。

這個原則只會停用雲端同步處理，不會影響 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 原則。

如果未設定此原則或將它套用為建議，則使用者將可以開啟或關閉同步。 如果將此原則套用為強制，則使用者將無法開啟同步。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SyncDisabled
  - GP 名稱：透過 Microsoft 同步服務停用資料同步
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SyncDisabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SyncDisabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="synctypeslistdisabled"></a>SyncTypesListDisabled

  #### <a name="configure-the-list-of-types-that-are-excluded-from-synchronization"></a>設定同步服務將排除的類型清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 83 或更新版本

  #### <a name="description"></a>說明

  如果啟用此原則，則所有指定的資料類型將會從同步中排除。 此原則可用來限制上傳至 Microsoft Edge 同步服務的資料類型。

您可以針對此原則提供下列其中一個資料類型：「favorites」、「settings」、「passwords」、「addressesAndMore」、「extensions」、「history」和 「collections」。 請注意，這些資料類型名稱需區分大小寫。

使用者將無法覆寫已停用的資料類型。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：SyncTypesListDisabled
  - GP 名稱：設定同步服務將排除的類型清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = "favorites"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：SyncTypesListDisabled
  - 範例值：
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="tls13hardeningforlocalanchorsenabled"></a>TLS13HardeningForLocalAnchorsEnabled

  #### <a name="enable-a-tls-13-security-feature-for-local-trust-anchors-obsolete"></a>啟用適於本機信賴起點的 TLS 1.3 安全性功能 (已過時)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 85 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - 在 Windows 和 macOS 上，版本 81 到 85

  #### <a name="description"></a>說明

  此原則已無法運作，因為其只是一種短期機制，目的是要讓企業有更多時間升級受影響的 Proxy。

此原則會控制 TLS 1.3 中可保護連線對抗降級攻擊的安全性功能。 它是回溯相容且不會影響與相容 TLS 1.2 伺服器或 Proxy 的連線。 不過，部分舊版 TLS 攔截 Proxy 具有實作缺陷，導致它們不相容。

如果啟用此原則或未設定，則 Microsoft Edge 將會針對所有連線啟用這些安全性保護。

如果停用此原則，則 Microsoft Edge 將針對使用本機安裝的 CA 憑證進行驗證的連線，停用這些安全性保護。 針對使用公開信任的 CA 憑證進行驗證的連線，這些保護一律會啟用。

此原則可用來測試任何受影響的 Proxy，並進行升級。 受影響的 Proxy 預期會連線失敗，出現錯誤碼 ERR_TLS13_DOWNGRADE_DETECTED。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TLS13HardeningForLocalAnchorsEnabled
  - GP 名稱：針對本機信賴起點啟用 TLS 1.3 安全性功能 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TLS13HardeningForLocalAnchorsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TLS13HardeningForLocalAnchorsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="tlsciphersuitedenylist"></a>TLSCipherSuiteDenyList

  #### <a name="specify-the-tls-cipher-suites-to-disable"></a>指定欲停用的 TLS 加密套件

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 85 或更新版本

  #### <a name="description"></a>說明

  設定 TLS 連線停用的加密套件清單。

若您設定此原則設定，在建立 TLS 連線時將不會使用已設定的加密套件清單。

若您未設定此原則，瀏覽器將會自選要使用的 TLS 加密套件。

若要停用加密套件值，請將其指定為16位的十六進位值。 這些值是由 Internet Assigned Numbers Authority (IANA) 登錄所指派。

TLS 1.3 須有 TLS 1.3 加密套件 TLS_AES_128_GCM_SHA256 (0x1301) ，且不可被此原則停用。

此原則不會影響 QUIC 式連線。 您可以透過 [QuicAllowed](#quicallowed) 原則關閉 QUIC。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TLSCipherSuiteDenyList
  - GP 名稱：指定欲停用的 TLS 加密套件
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = "0x1303"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = "0xcca8"
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = "0xcca9"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TLSCipherSuiteDenyList
  - 範例值：
``` xml
<array>
  <string>0x1303</string>
  <string>0xcca8</string>
  <string>0xcca9</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="tabfreezingenabled"></a>TabFreezingEnabled

  #### <a name="allow-freezing-of-background-tabs-obsolete"></a>允許凍結背景索引標籤 (已淘汰)

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 86 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 79 至 86

  #### <a name="description"></a>描述

  此原則無法執行，請改為使用 [SleepingTabsEnabled](#sleepingtabsenabled)。

控制 Microsoft Edge 是否可以凍結在背景中至少 5 分鐘的索引標籤。

凍結索引標籤會降低 CPU、電池和記憶體使用量。 Microsoft Edge 使用啟發學習法來避免凍結在背景中執行實用工作 (例如：顯示通知、播放音效和串流視訊) 的索引標籤。

如果啟用或未設定此原則，則在背景中至少 5 分鐘的索引標籤可能會遭到凍結。

如果停用此原則，則不會凍結任何索引標籤。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TabFreezingEnabled
  - GP 名稱：允許凍結背景索引標籤 (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TabFreezingEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TabFreezingEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="targetblankimpliesnoopener"></a>TargetBlankImpliesNoOpener

  #### <a name="do-not-set-windowopener-for-links-targeting-_blank"></a>不对指向 _blank 的链接設定 window.opener

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>說明

  如果啟用或不設定此原則，則 window.opener 屬性設定為 null，除非錨點指定 rel="opener"。

如果停用此原則，則允許目標 _blank 的快顯視窗存取 (透過 JavaScript) 要求開啟快顯視窗的頁面。

此原則將在 Microsoft Edge 版本 95 中過時。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： TargetBlankImpliesNoOpener
  - GP 名稱：不对指向 _blank 的链接設定 window.opener
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱： TargetBlankImpliesNoOpener
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱： TargetBlankImpliesNoOpener
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="taskmanagerendprocessenabled"></a>TaskManagerEndProcessEnabled

  #### <a name="enable-ending-processes-in-the-browser-task-manager"></a>啟用在瀏覽器工作管理員中結束處理程序

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  如果啟用或未設定此原則，則使用者可以在瀏覽器工作管理員中結束處理程序。 如果停用此原則，則使用者無法結束處理程序，且瀏覽器工作管理員中的 [結束處理程序] 按鈕會停用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TaskManagerEndProcessEnabled
  - GP 名稱：啟用在瀏覽器工作管理員中結束處理程序
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TaskManagerEndProcessEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TaskManagerEndProcessEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="totalmemorylimitmb"></a>TotalMemoryLimitMb

  #### <a name="set-limit-on-megabytes-of-memory-a-single-microsoft-edge-instance-can-use"></a>設定單一 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>說明

  設定開始捨棄索引標籤以節省記憶體之前，單一 Microsoft Edge 執行個體可以使用的記憶體數量。 索引標籤使用的記憶體將會釋出，且在切換至該索引標籤時，必須重新載入它。

如果啟用此原則，則瀏覽器將會在超過限制之後，開始捨棄索引標籤來節省記憶體。 不過，無法保證瀏覽器一律會在限制內執行。 低於 1024 的任何值都會進位為 1024。

如果未設定此原則，則瀏覽器只會在偵測到其電腦上的實際記憶體數量不足時才嘗試儲存記憶體。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TotalMemoryLimitMb
  - GP 名稱：設定單一個 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TotalMemoryLimitMb
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000800
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TotalMemoryLimitMb
  - 範例值：
``` xml
<integer>2048</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="trackingprevention"></a>TrackingPrevention

  #### <a name="block-tracking-of-users-web-browsing-activity"></a>封鎖使用者的網頁瀏覽活動追蹤

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 78 或更新版本

  #### <a name="description"></a>說明

  讓您決定是否要封鎖網站，使其無法追蹤使用者的 Web 瀏覽活動。

如果停用此原則或未設定，則使用者可以設定自己的防止追蹤層級。

原則選項對應：

* TrackingPreventionOff (0) = 關閉 (無防止追蹤)

* TrackingPreventionBasic (1) = 基本 (封鎖有害的追蹤器，內容與廣告會進行個人化)

* TrackingPreventionBalanced (2) = 平衡 (封鎖有害的追蹤器以及來自使用者尚未造訪網站的追蹤器；內容與廣告的個人化程度較低)

* TrackingPreventionStrict (3) =嚴格 (封鎖有害的追蹤器以及來自所有網站的大部分追蹤器；內容與廣告的個人化程度最低。 網站的某些部分可能無法運作)

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TrackingPrevention
  - GP 名稱：封鎖使用者的網頁瀏覽活動追蹤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TrackingPrevention
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000002
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TrackingPrevention
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="translateenabled"></a>TranslateEnabled

  #### <a name="enable-translate"></a>啟用翻譯

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  在 Microsoft Edge 上啟用整合式 Microsoft 翻譯服務。

如果啟用此原則，則 Microsoft Edge 會透過在適當時顯示整合的翻譯飛出視窗，以及按滑鼠右鍵功能表中的翻譯選項，為使用者提供翻譯功能。

停用此原則可停用所有內建的翻譯功能。

如果未設定原則，則使用者可以選擇是否要使用翻譯功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TranslateEnabled
  - GP 名稱：啟用翻譯
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：TranslateEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TranslateEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="tripledesenabled"></a>TripleDESEnabled

  #### <a name="enable-3des-cipher-suites-in-tls"></a>在 TLS 中啟用 3DES 加密套件

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 93 或更新版本

  #### <a name="description"></a>說明

  '警告： 3DES 將 (於約 2021 年 10 月時) 從版本 95 Microsoft Edge 完全移除，屆時此原則將停止作用。

如果原則設定為 True，則會套用 TLS 中的 3DES 加密套件。 如果設定為 False，將會停用。 如果未設置原則，預設會停用 3DES 加密套件。 此原則可用來暫時保留與過期伺服器的相容性。 這是一種權宜之計，應該重新佈建服務器。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：TripleDESEnabled
  - GP 名稱：在 TLS 中啟用 3DES 加密套件
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TripleDESEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：TripleDESEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="urlallowlist"></a>URLAllowlist

  #### <a name="define-a-list-of-allowed-urls"></a>定義受允許的 URL 清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定該原則可讓您存取所列的 URL，作為 [URLBlocklist](#urlblocklist) 的例外。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。

您可以使用此原則來對限制性封鎖清單開放例外。 例如，您可以在封鎖清單中包含 '\*' 以封鎖所有要求，然後使用此原則來允許對受限的 URL 清單的存取權。 您可以使用此原則來開放特定配置、其他網域的子網域、連接埠或特定路徑的例外。

最特定的篩選會判斷是否已封鎖或允許某個 URL。 允許清單優先於封鎖清單。

此原則限制在 1000 個項目；後續的項目會被忽略。

此原則也可讓瀏覽器自動叫用註冊為通訊協定處理常式的外部應用程序，例如「tel:」或「ssh:」。

如果未設定此原則，則 [URLBlocklist](#urlblocklist) 原則的封鎖清單中沒有例外。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：URLAllowlist
  - GP 名稱：定義受允許的 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = "hosting.com/good_path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = ".exact.hostname.com"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：URLAllowlist
  - 範例值：
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/good_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="urlblocklist"></a>URLBlocklist

  #### <a name="block-access-to-a-list-of-urls"></a>封鎖存取 URL 清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 的模式，定義遭封鎖的網站清單 (您的使用者無法載入該清單)。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。

您可以在 [URLAllowlist](#urlallowlist) 原則中定義例外。 這些原則限制在 1000 個項目；後續的項目會被忽略。

請注意，不建議封鎖內部 'edge://*' URL，這可能會導致意外的錯誤。

此原則無法防止頁面透過 JavaScript 動態更新。 例如，如果您封鎖 'contoso.com/abc'，則使用者仍可能可以造訪 'contoso.com'，並按一下連結來覽 'contoso.com/abc' (只要不重新整理頁面)。

如果未設定此原則，則不會封鎖任何 URL。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：URLBlocklist
  - GP 名稱：封鎖存取 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = "contoso.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = "https://ssl.server.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = "hosting.com/bad_path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = "https://server:8080/path"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = ".exact.hostname.com"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = "file://*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = "custom_scheme:*"
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = "*"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：URLBlocklist
  - 範例值：
``` xml
<array>
  <string>contoso.com</string>
  <string>https://ssl.server.com</string>
  <string>hosting.com/bad_path</string>
  <string>https://server:8080/path</string>
  <string>.exact.hostname.com</string>
  <string>file://*</string>
  <string>custom_scheme:*</string>
  <string>*</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="updatepolicyoverride"></a>UpdatePolicyOverride

  #### <a name="specifies-how-microsoft-edge-update-handles-available-updates-from-microsoft-edge"></a>指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - macOS 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge Update：

- 僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。

- 僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。 (並非所有應用程式都提供此選項的介面。)

如果選取手動更新，請確保您使用 Microsoft AutoUpdate 定期檢查更新。

如果您未啟用並設定此原則，則 Microsoft Edge Update 會自動檢查更新。


原則選項對應：

* automatic-silent-only (僅限自動無訊息) = 僅當定期更新檢查找到更新時才套用更新。

* manual-only (僅限手動) = 僅當使用者執行手動更新檢查時才套用更新。 (並非所有應用程式都提供此選項的介面。)

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：UpdatePolicyOverride
  - 範例值：
``` xml
<string>automatic-silent-only</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="useragentclienthintsenabled"></a>UserAgentClientHintsEnabled

  #### <a name="enable-the-user-agent-client-hints-feature-deprecated"></a>啟用使用者代理程式用戶端提示功能 (已過時)

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與使用者代理程式用戶端提示功能不一致時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本 94 中使用。

啟用 [使用者代理程式用戶端提示] 功能時，會傳送提供使用者瀏覽器相關資訊 (例如瀏覽器版本) 和環境 (例如系統架構) 的細微要求標頭。

這是一項累加功能，但新的標頭可能會破壞某些網站，這些網站限制了要求可能包含某些字元。

如果您啟用或未設定此原則，則會啟用 [使用者代理程式用戶端提示] 功能。 如果您停用此原則，則無法使用此功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：UserAgentClientHintsEnabled
  - GP 名稱：啟用使用者代理程式用戶端提示功能 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：UserAgentClientHintsEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：UserAgentClientHintsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="userdatadir"></a>UserDataDir

  #### <a name="set-the-user-data-directory"></a>設定使用者資料目錄

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  設定用來儲存使用者資料的目錄。

如果啟用此原則，則 Microsoft Edge 會使用指定的目錄，而無論使用者是否已設定 '--user-data-dir' 命令列旗標。

如果未啟用此原則，則會使用預設的設定檔路徑，但使用者可以使用 '--user-data-dir' 旗標來覆寫它。 使用者可以在 edge://version/ 的「設定檔路徑」底下找到設定檔的目錄。

若要避免資料遺失或其他錯誤，請勿將此原則設定為磁碟區的根目錄或用於其他用途的目錄，因為 Microsoft Edge 會管理其內容。

如需可使用的變數清單，請參閱[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：UserDataDir
  - GP 名稱：設定使用者資料目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UserDataDir
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"${users}/${user_name}/Edge"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：UserDataDir
  - 範例值：
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="userdatasnapshotretentionlimit"></a>UserDataSnapshotRetentionLimit

  #### <a name="limits-the-number-of-user-data-snapshots-retained-for-use-in-case-of-emergency-rollback"></a>限制保留的使用者資料快照數量，以便在緊急復原時使用

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 86 或更新版本

  #### <a name="description"></a>描述

  在每個主要版本更新之後，Microsoft Edge 將會建立使用者瀏覽資料的部分內容快照，以便日後需要暫存版本復原的緊急情況。 如果在使用者有對應快照的版本中執行暫存復原，可還原快照中的資料。 這可讓使用者保留如書簽和自動填寫資料等設定。

如果您未設定此原則，採用的預設值為 3 個快照。

如果您設定了此原則，舊版快照將會視需要而被刪除，以遵守您設定的限制。 如果您將此原則設為0，則不會拍攝任何快照。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 整數

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：UserDataSnapshotRetentionLimit
  - GP 唯一名稱：限制保留的使用者資料快照數量，以便在緊急復原時使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UserDataSnapshotRetentionLimit
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000003
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="userfeedbackallowed"></a>UserFeedbackAllowed

  #### <a name="allow-user-feedback"></a>允許使用者意見反應

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  Microsoft Edge 使用 Edge 意見反應功能 (預設為啟用)，以允許使用者傳送意見反應、建議或客戶問卷調查，並報告有關瀏覽器的任何問題。 此外，使用者預設無法停用 (關閉) Microsoft Edge 意見反應功能。

如果啟用此原則或未設定，則使用者可以叫用 Microsoft Edge 意見反應。

如果停用此原則，則使用者無法叫用 Microsoft Edge 意見反應。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：UserFeedbackAllowed
  - GP 名稱：允許使用者意見反應
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UserFeedbackAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：UserFeedbackAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="verticaltabsallowed"></a>VerticalTabsAllowed

  #### <a name="configures-availability-of-a-vertical-layout-for-tabs-on-the-side-of-the-browser"></a>設定瀏覽器側邊上索引標籤垂直版面配置的可用性

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  設定使用者是否可以存取在替代的版面配置，在其中，索引標籤會在瀏覽器側邊 (而非上方) 垂直對齊。
有數個索引標籤開啟時，此版面配置可提供更好的索引標籤檢視和管理。 網站標題有更好的可見度，要一眼看到對齊的圖示更容易，並且有更多空間可用來管理及關閉索引標籤。

如果您停用此原則，則垂直索引標籤版面配置將不會以選項形式提供使用者使用。

如果您啟用或未設定此原則，索引標籤版面配置將仍位於上方，但使用者會有選項，可在側邊開啟垂直索引標籤。


  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：VerticalTabsAllowed
  - GP 名稱：設定瀏覽器側邊上索引標籤垂直版面配置的可用性
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：VerticalTabsAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：VerticalTabsAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="videocaptureallowed"></a>VideoCaptureAllowed

  #### <a name="allow-or-block-video-capture"></a>允許或封鎖視訊擷取

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  控制網站是否可以擷取視訊。

如果已啟用或未設定 (預設)，則使用者會被詢問有關所有網站的視訊擷取存取權，在 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 原則清單中已設定 URL 的這些網站除外，這些網站不需提示就會授與存取權。

如果停用此原則，則不會提示使用者，且視訊擷取僅可供 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 原則中設定的 URL 使用。

此原則會影響所有類型的視訊輸入，而不僅僅是內建的相機。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：VideoCaptureAllowed
  - GP 名稱：允許或封鎖視訊擷取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：VideoCaptureAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：VideoCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="videocaptureallowedurls"></a>VideoCaptureAllowedUrls

  #### <a name="sites-that-can-access-video-capture-devices-without-requesting-permission"></a>無需要求權限即可存取視訊擷取裝置的網站

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  根據 URL 模式指定可使用視訊擷取裝置的網站，而不詢問使用者提供權限。 此清單中的模式會對照要求端 URL 的安全性來源進行比對。 如果符合，則網站會自動獲授與視訊擷取裝置的存取權。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：VideoCaptureAllowedUrls
  - GP 名稱：無需要求權限即可存取視訊擷取裝置的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = "https://www.contoso.com/"
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = "https://[*.]contoso.edu/"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：VideoCaptureAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="wpadquickcheckenabled"></a>WPADQuickCheckEnabled

  #### <a name="set-wpad-optimization"></a>設定 WPAD 最佳化

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許您關閉 Microsoft Edge 中的 WPAD (Web Proxy AutoDiscovery) 最佳化。

如果停用此原則，則會停用 WPAD 最佳化，這會讓瀏覽器等候 DNS 型 WPAD 伺服器較長的時間。

如果啟用或未設定該原則，則會啟用 WPAD 最佳化。

無論此原則是否已啟用或如何啟用，使用者皆無法變更 WPAD 最佳化設定。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WPADQuickCheckEnabled
  - GP 名稱：設定 WPAD 最佳化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WPADQuickCheckEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WPADQuickCheckEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webappinstallforcelist"></a>WebAppInstallForceList

  #### <a name="configure-list-of-force-installed-web-apps"></a>設定強制安裝 Web 應用程式的清單

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>描述

  設定此原則以指定無需使用者互動的網頁應用程式清單，並且使用者無法卸載或關閉這些應用程式。

原則的每個清單項目都是具有強制成員的物件： url (要安裝之 web 應用程式的 URL) 

及 3 個選用的成員：
- default_launch_container (指定 Web 應用程式開啟時要使用的視窗模式，預設值為新索引標籤。)

- create_desktop_shortcut (如果要建立 Linux 和 Microsoft Windows 桌面捷徑，則為 True。)

- fallback_app_name (從 Microsoft Edge 90 開始，如果不是漸進式 Web 應用程式 (PWA)，則允許您覆寫應用程式名稱；如果是 PWA，則為暫時安裝的應用程式名稱，但需要進行驗證，安裝才能完成)

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - Dictionary

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebAppInstallForceList
  - GP 名稱：設定強制安裝 Web 應用程式的清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebAppInstallForceList
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [
  {
    "create_desktop_shortcut": true,
    "default_launch_container": "window",
    "url": "https://www.contoso.com/maps"
  },
  {
    "default_launch_container": "tab",
    "url": "https://app.contoso.edu"
  },
  {
    "default_launch_container": "window",
    "fallback_app_name": "Editor",
    "url": "https://app.contoso.com/editor"
  }
]
```

  ##### <a name="compact-example-value"></a>精簡範例值：

  ```
  SOFTWARE\Policies\Microsoft\Edge\WebAppInstallForceList = [{"create_desktop_shortcut": true, "default_launch_container": "window", "url": "https://www.contoso.com/maps"}, {"default_launch_container": "tab", "url": "https://app.contoso.edu"}, {"default_launch_container": "window", "fallback_app_name": "Editor", "url": "https://app.contoso.com/editor"}]
  ```
  

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebAppInstallForceList
  - 範例值：
``` xml
<key>WebAppInstallForceList</key>
<array>
  <dict>
    <key>create_desktop_shortcut</key>
    <true/>
    <key>default_launch_container</key>
    <string>window</string>
    <key>url</key>
    <string>https://www.contoso.com/maps</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>tab</string>
    <key>url</key>
    <string>https://app.contoso.edu</string>
  </dict>
  <dict>
    <key>default_launch_container</key>
    <string>window</string>
    <key>fallback_app_name</key>
    <string>Editor</string>
    <key>url</key>
    <string>https://app.contoso.com/editor</string>
  </dict>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webcaptureenabled"></a>WebCaptureEnabled

  #### <a name="enable-web-capture-feature-in-microsoft-edge"></a>啟用 Microsoft Edge 中的 Web 擷取功能

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  啟用 Microsoft Edge 中允許使用者擷取 Web 內容及使用筆跡工具來為擷取加上註解的 Web 擷取功能。
如果您啟用或未設定此原則，Web 擷取選項會顯示在快顯功能表、設定及更多功能表中，以及可使用鍵盤快速鍵 CTRL+SHIFT+S 取得。
如果您停用此原則，使用者將無法在 Microsoft Edge 中存取 Web 擷取功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebCaptureEnabled
  - GP 名稱：啟用 Microsoft Edge 中的 Web 擷取功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebCaptureEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebCaptureEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webcomponentsv0enabled"></a>WebComponentsV0Enabled

  #### <a name="re-enable-web-components-v0-api-until-m84-obsolete"></a>在 M84 前，重新啟用 Web 元件 v0 API。

  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - 在 Windows 和 macOS 上，版本 80 至 84

  #### <a name="description"></a>說明

  此原則無法運作，因為此原則允許您在 Microsoft Edge 版本 85 之前，選擇性地重新啟用這些功能。 Web 元件 v0 API (Shadow DOM v0、Custom Elements v0 和 HTML Imports) 已在 2018 年過時，且已預設在 Microsoft Edge 版本 M80 中開始停用。

如果將此原則設定為 True，則會為所有網站啟用網頁元件 v0 功能。

若您將此原則設定為 False 或未設定此原則，從 Microsoft Edge 版本 M80 開始，已預設停用 Web 元件 v0 功能。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebComponentsV0Enabled
  - GP 名稱：在 M84 前，重新啟用 Web 元件 v0 API (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebComponentsV0Enabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebComponentsV0Enabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webdriveroverridesincompatiblepolicies"></a>WebDriverOverridesIncompatiblePolicies

  #### <a name="allow-webdriver-to-override-incompatible-policies-obsolete"></a>允許 WebDriver 覆寫不相容原則 (已過時) 

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### <a name="supported-versions"></a>支援的版本：

  - 在 Windows 和 macOS 上，版本 77 到 84

  #### <a name="description"></a>說明

  此原則無法運作，因為 WebDriver 目前相容於所有現有原則。

此原則會允許讓 WebDriver 功能的使用者覆寫可能干擾其操作的原則。

目前此原則會停用 [SitePerProcess](#siteperprocess) 和 [IsolateOrigins](#isolateorigins) 原則。

如果已啟用此原則，WebDriver 將可以覆寫不相容的原則。
如果停用或未設定原則，則將不允許 WebDriver 覆寫不相容的原則。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebDriverOverridesIncompatiblePolicies
  - GP 名稱：允許 WebDriver 覆寫不相容原則 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebDriverOverridesIncompatiblePolicies
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebDriverOverridesIncompatiblePolicies
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webrtcallowlegacytlsprotocols"></a>WebRtcAllowLegacyTLSProtocols

  #### <a name="allow-legacy-tlsdtls-downgrade-in-webrtc-deprecated"></a>在 WebRTC 中允許舊版 TLS/DTLS 降級 (已取代)

  >已取代：此原則已被取代。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  如果您啟用此原則，則 WebRTC 對等連線可以降級至版本過時的 TLS/DTLS (DTLS 1.0、TLS 1.0 及 TLS 1.1) 通訊協定。
如果停用或不設定此原則，這些 TLS/DTLS 版本會遭停用。

此原則是暫時的，將在未來版本的 Microsoft Edge 中移除。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebRtcAllowLegacyTLSProtocols
  - GP 名稱：在 WebRTC 中允許舊版 TLS/DTLS 降級 (已取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebRtcAllowLegacyTLSProtocols
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000000
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebRtcAllowLegacyTLSProtocols
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webrtclocalipsallowedurls"></a>WebRtcLocalIpsAllowedUrls

  #### <a name="manage-exposure-of-local-ip-addressess-by-webrtc"></a>管理由 WebRTC 暴露的本機 IP 位址

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 80 或更新版本

  #### <a name="description"></a>說明

  指定應該由 WebRTC 公開本機 IP 位址的來源 (URL) 或主機名稱模式 (例如 "*contoso.com*") 的清單。

如果啟用此原則，並設定來源 (URL) 或主機名稱模式清單，當 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為啟用時，WebRTC 會在符合清單中模式的情況下公開本機 IP 位址。

如果停用或未設定此原則，且 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為已啟用，則 WebRTC 將不會公開本機 IP 位址。 本機 IP 位址會使用 mDNS 主機名稱隱藏。

如果啟用、停用或未設定此原則，且 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為已停用，則 WebRTC 將會公開本機 IP 位址。

請注意，此原則會使得系統管理員可能需要的本機 IP 位址的保護變弱。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebRtcLocalIpsAllowedUrls
  - GP 名稱：管理由 WebRTC 暴露的本機 IP 位址
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = "https://www.contoso.com"
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = "*contoso.com*"

```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebRtcLocalIpsAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webrtclocalhostiphandling"></a>WebRtcLocalhostIpHandling

  #### <a name="restrict-exposure-of-local-ip-address-by-webrtc"></a>限制由 WebRTC 暴露的本機 IP 位址

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>描述

  允許您設定 WebRTC 是否公開使用者的本機 IP 位址。

如果將此原則設定為「AllowAllInterfaces」或 「AllowPublicAndPrivateInterfaces」，則 WebRTC 會公開本機 IP 位址。

如果將此原則設定為「AllowPublicInterfaceOnly」或「DisableNonProxiedUdp」，則 WebRTC 不會公開本機 IP 位址。

如果未設定此原則，或如果停用此原則，則 WebRTC 會公開本機 IP 位址。

原則選項對應：

* AllowAllInterfaces (預設) = 允許所有介面。 這會公開本機 IP 位址。

* AllowPublicAndPrivateInterfaces (default_public_and_private_interfaces) = 允許透過 HTTP 預設路由的公用和私人介面。 這會公開本機 IP 位址。

* AllowPublicInterfaceOnly (default_public_interface_only) = 允許透過 HTTP 預設路由的公用介面。 這不會公開本機 IP 位址。

* DisableNonProxiedUdp (disable_non_proxied_udp) = 除非 Proxy 伺服器支援 UDP，否則使用 TCP。 這不會公開本機 IP 位址。

設定此原則時，請使用上述資訊。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebRtcLocalhostIpHandling
  - GP 名稱：限制由 WebRTC 暴露的本機 IP 位址
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebRtcLocalhostIpHandling
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"default"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebRtcLocalhostIpHandling
  - 範例值：
``` xml
<string>default</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webrtcudpportrange"></a>WebRtcUdpPortRange

  #### <a name="restrict-the-range-of-local-udp-ports-used-by-webrtc"></a>限制 WebRTC 所使用的本機 UDP 連接埠範圍

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 和 macOS 上，版本 77 或更新版本

  #### <a name="description"></a>說明

  將 WebRTC 所使用的 UDP 連接埠範圍限制在指定的連接埠間隔 (包括端點)。

透過設定此原則，您可以指定 WebRTC 可以使用的本機 UDP 連接埠範圍。

如果未設定此原則，或將它設定為空白字串或無效的連接埠範圍，則 WebRTC 可以使用任何可用的本機 UDP 連接埠。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 字串

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WebRtcUdpPortRange
  - GP 名稱：限制 WebRTC 所使用的本機 UDP 連接埠範圍
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebRtcUdpPortRange
  - 數值類型：REG_SZ

  ##### <a name="example-value"></a>範例值：

```
"10000-11999"
```

  #### <a name="mac-information-and-settings"></a>Mac 資訊和設定
  
  - 喜好設定機碼名稱：WebRtcUdpPortRange
  - 範例值：
``` xml
<string>10000-11999</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webwidgetallowed"></a>WebWidgetAllowed

  #### <a name="enable-the-web-widget"></a>啟用Web 小工具

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  啟用Web 小工具. 啟用後，使用者可以使用該小工具從桌面或從應用程式來搜尋網頁。 該小工具會提供搜尋方塊以顯示網頁建議，並開啟 Microsoft Edge 中的所有網頁搜尋。 搜尋方塊提供搜尋 (依照 Bing 提供的支援) 和 URL 建議。 該小工具也包含資訊摘要方塊，使用者可以在msn.com新的 Microsoft Edge 瀏覽器或視窗中點擊以看到更多資訊. 資訊摘要方塊可能包含廣告。 您可以從 Microsoft Edge 設定或 Microsoft Edge 中的＂其他工具＂功能表啟動小工具。

如果您啟用或未設定此原則：系統會自動為所有設定檔啟用Web小工具。
在 Microsoft Edge 設定中，使用者會看到啟用小工具的選項。
在 Microsoft Edge 設定中，使用者會看到功能表選項，以在 Windows 啟動時執行小工具 (自動啟動)。
如果已啟用 [WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup) 原則，則在開機時啟用小工具的選項將被打開。
如果 [WebWidgetIsEnabledOnStartup](#webwidgetisenabledonstartup) 已停用或未設定，則在開機時啟用小工具的選項將被關閉。
使用者將從 Microsoft Edge 的＂更多工具＂功能表中看到功能選項以啟動小工具。 使用者可以從＂更多工具＂啟動小工具。
您可以從系統工作列的＂離開＂選項，或從工作列關閉小工具來關閉該小工具。 如果啟用自動啟動，小工具會在系統重新開機時重新啟用。

如果您停用這個原則：所有設定檔都將停用Web小工具。
啟動 Microsoft Edge 設定小工具的選項將會停用。
在 Windows 啟動 (自動啟動) 時啟動小工具的啟用選項將會停用。
從Microsoft Edge “更多工具”的功能選單啟動 Microsoft Edge 小工具的選項將會停用。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： WebWidgetAllowed
  - GP 名稱：啟用Web小工具
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： WebWidgetAllowed
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="webwidgetisenabledonstartup"></a>WebWidgetIsEnabledOnStartup

  #### <a name="allow-the-web-widget-at-windows-startup"></a>在 Windows 啟動時允許Web小工具

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 88 或更新版本

  #### <a name="description"></a>描述

  允許網頁小工具在 Windows 啟動時開始執行。

如果您啟用：Web小工具預設會在 Windows 啟動時開始執行。
如果透過 [WebWidgetAllowed](#webwidgetallowed) 原則停用小工具，此原則就不會在 Windows 啟動時啟動小工具。

如果您停用這個原則： Web網頁小工具將不會在Windows 啟動時啟動所有配置文件。
在 Windows 啟動時啟動小工具的選項將會停用，並會在 Microsoft Edge 設定中關閉。

如果您未設定這個原則： Web網頁小工具將不會在Windows 啟動時啟動所有配置文件。
在 Windows 啟動時啟動小工具的選項將會在 Microsoft Edge 的設定中關閉。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱： WebWidgetIsEnabledOnStartup
  - GP 名稱：在 Windows 啟動時允許Web小工具
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： WebWidgetIsEnabledOnStartup
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="winhttpproxyresolverenabled"></a>WinHttpProxyResolverEnabled

  #### <a name="use-windows-proxy-resolver-deprecated"></a>使用 Windows proxy 解析程式 (已取代) 

  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 84 或更新版本

  #### <a name="description"></a>描述

  此原則已過時，因為未來版本中會有類似的功能將之取代，請參閱 https://crbug.com/1032820。

使用 Windows 解析所有瀏覽器網路的 proxy，而不是 Microsoft Edge 內建的 proxy 解析程式。 Windows proxy 解析程式可以啟用 Windows proxy 功能如 DirectAccess/NRPT。

此原則所帶來的問題如 https://crbug.com/644030 所述。 這會導致 Windows 代碼取得 PAC 檔案並執行之，包括透過 [ProxyPacUrl](#proxypacurl) 原則設定的 PAC 檔案。 由於 PAC 檔案的網路擷取是經由 Windows 而不是由 Microsoft Edge 代碼，因此像是 [DnsOverHttpsMode](#dnsoverhttpsmode) 的網路原則不適用於 PAC 檔案的網路擷取。

如果您啟用此原則，系統就會使用 Windows proxy 解析程式。

如果您停用或未設定此原則，系統將會使用 Microsoft Edge proxy 解析程式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WinHttpProxyResolverEnabled
  - GP 名稱：使用 Windows proxy 解析程式 (已取代) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WinHttpProxyResolverEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)

  ### <a name="windowocclusionenabled"></a>WindowOcclusionEnabled

  #### <a name="enable-window-occlusion"></a>啟用視窗遮蔽

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 89 或更新版本

  #### <a name="description"></a>描述

  在 Microsoft Edge 中啟用視窗遮蔽。

如果啟用此設定，為了降低 CPU 和耗電量，Microsoft Edge 將偵測視窗何時被其他視窗覆蓋，並將暫停工作繪製像素。

如果停用此設定，則 Microsoft Edge 無法偵測某個視窗是否被其他視窗遮蓋。

如果將此原則保留為未設定，則會啟用視窗隱藏偵測。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 布林值

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：WindowOcclusionEnabled
  - GP 名稱：啟用視窗遮蔽
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WindowOcclusionEnabled
  - 數值類型：REG_DWORD

  ##### <a name="example-value"></a>範例值：

```
0x00000001
```

  

  [回到頁首](#microsoft-edge---policies)


## <a name="see-also"></a>請參閱

- [設定 Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft 安全性基準部落格](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
