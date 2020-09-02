---
title: Microsoft Edge 瀏覽器原則文件
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 08/12/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge 瀏覽器支援的所有原則的 Windows 和 Mac 文件
ms.openlocfilehash: 8b514b1c1cbcaf64e8c44497522c368f71e7a0a0
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979615"
---
# Microsoft Edge - 原則
最新版本的 Microsoft Edge 包含下列原則。 您可以使用這些原則來設定 Microsoft Edge 在組織中的執行方式。

如需用於控制 Microsoft Edge 更新方式和更新時機的一組額外原則的詳細資訊，請參閱 [Microsoft Edge 更新原則參考](microsoft-edge-update-policies.md)。

您可以下載 [Microsoft 安全性合規性工具組](https://www.microsoft.com/download/details.aspx?id=55319)，以取得 Microsoft Edge 的建議安全性設定基準設定。 如需詳細資訊，請參閱 [Microsoft 安全性基準部落格](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 可用原則
下表列出此版本 Microsoft Edge 提供的所有瀏覽器相關群組原則。 使用下表中的連結，深入了解特定原則。

|||
|-|-|
|[應用程式防護設定](#application-guard-settings)|[投射](#cast)|
|[內容設定](#content-settings)|[預設搜尋提供者](#default-search-provider)|
|[Extensions](#extensions)|[HTTP 驗證](#http-authentication)|
|[原生訊息](#native-messaging)|[密碼管理員和防護](#password-manager-and-protection)|
|[列印](#printing)|[Proxy 伺服器](#proxy-server)|
|[SmartScreen 設定](#smartscreen-settings)|[啟動、首頁和新的索引標籤頁面](#startup-home-page-and-new-tab-page)|
|[其他](#additional)|

### [*應用程式防護設定*](#application-guard-settings-policies)
|原則名稱|標題|
|-|-|
|[ApplicationGuardContainerProxy](#applicationguardcontainerproxy)|應用程式防護容器 Proxy|
### [*投射*](#cast-policies)
|原則名稱|標題|
|-|-|
|[EnableMediaRouter](#enablemediarouter)|啟用 Google Cast|
|[ShowCastIconInToolbar](#showcasticonintoolbar)|在工具列中顯示投射圖示|
### [*內容設定*](#content-settings-policies)
|原則名稱|標題|
|-|-|
|[AutoSelectCertificateForUrls](#autoselectcertificateforurls)|自動選取這些網站的用戶端憑證|
|[CookiesAllowedForUrls](#cookiesallowedforurls)|允許特定網站上的 Cookie|
|[CookiesBlockedForUrls](#cookiesblockedforurls)|封鎖特定網站上的 Cookie|
|[CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)|限制來自特定網站的 Cookie 匯入目前的工作階段|
|[DefaultCookiesSetting](#defaultcookiessetting)|設定 Cookie|
|[DefaultGeolocationSetting](#defaultgeolocationsetting)|預設地理位置設定值|
|[DefaultImagesSetting](#defaultimagessetting)|預設影像設定|
|[DefaultInsecureContentSetting](#defaultinsecurecontentsetting)|控制不安全內容例外狀況的使用|
|[DefaultJavaScriptSetting](#defaultjavascriptsetting)|預設 JavaScript 設定|
|[DefaultNotificationsSetting](#defaultnotificationssetting)|預設通知設定|
|[DefaultPluginsSetting](#defaultpluginssetting)|預設 Adobe Flash 設定|
|[DefaultPopupsSetting](#defaultpopupssetting)|預設快顯視窗設定|
|[DefaultWebBluetoothGuardSetting](#defaultwebbluetoothguardsetting)|控制 Web 藍牙 API 的使用|
|[DefaultWebUsbGuardSetting](#defaultwebusbguardsetting)|控制 WebUSB API 的使用|
|[ImagesAllowedForUrls](#imagesallowedforurls)|允許這些網站上的影像|
|[ImagesBlockedForUrls](#imagesblockedforurls)|封鎖特定網站上的影像|
|[InsecureContentAllowedForUrls](#insecurecontentallowedforurls)|允許指定網站上的不安全內容|
|[InsecureContentBlockedForUrls](#insecurecontentblockedforurls)|封鎖指定網站上的不安全內容|
|[JavaScriptAllowedForUrls](#javascriptallowedforurls)|允許特定網站上的 JavaScript|
|[JavaScriptBlockedForUrls](#javascriptblockedforurls)|封鎖特定網站上的 JavaScript|
|[LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)|啟用預設舊版 SameSite Cookie 行為設定|
|[LegacySameSiteCookieBehaviorEnabledForDomainList](#legacysamesitecookiebehaviorenabledfordomainlist)|將指定網站上的 Cookie 還原至舊版 SameSite 行為|
|[NotificationsAllowedForUrls](#notificationsallowedforurls)|允許特定網站上的通知|
|[NotificationsBlockedForUrls](#notificationsblockedforurls)|封鎖特定網站上的通知|
|[PluginsAllowedForUrls](#pluginsallowedforurls)|允許特定網站上的 Adobe Flash 外掛程式|
|[PluginsBlockedForUrls](#pluginsblockedforurls)|封鎖特定網站上的 Adobe Flash 外掛程式|
|[PopupsAllowedForUrls](#popupsallowedforurls)|允許特定網站上的快顯視窗|
|[PopupsBlockedForUrls](#popupsblockedforurls)|封鎖特定網站上的快顯視窗|
|[RegisteredProtocolHandlers](#registeredprotocolhandlers)|登錄通訊協定處理常式|
|[WebUsbAllowDevicesForUrls](#webusballowdevicesforurls)|授與特定網站連線到特定 USB 裝置的存取權|
|[WebUsbAskForUrls](#webusbaskforurls)|允許特定網站上的 WebUSB|
|[WebUsbBlockedForUrls](#webusbblockedforurls)|封鎖特定網站上的 WebUSB|
### [*預設搜尋提供者*](#default-search-provider-policies)
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
### [*Extensions*](#extensions-policies)
|原則名稱|標題|
|-|-|
|[ExtensionAllowedTypes](#extensionallowedtypes)|設定允許的擴充功能類型|
|[ExtensionInstallAllowlist](#extensioninstallallowlist)|允許安裝特定擴充功能|
|[ExtensionInstallBlocklist](#extensioninstallblocklist)|控制不能安裝哪些擴充功能|
|[ExtensionInstallForcelist](#extensioninstallforcelist)|控制哪些擴充功能會以無訊息方式安裝|
|[ExtensionInstallSources](#extensioninstallsources)|設定擴充功能與使用者指令碼安裝來源|
|[ExtensionSettings](#extensionsettings)|設定擴充功能管理設定|
### [*HTTP 驗證*](#http-authentication-policies)
|原則名稱|標題|
|-|-|
|[AllowCrossOriginAuthPrompt](#allowcrossoriginauthprompt)|允許跨原始來源 HTTP 基本驗證提示|
|[AuthNegotiateDelegateAllowlist](#authnegotiatedelegateallowlist)|指定 Microsoft Edge 可以委派使用者認證的伺服器清單|
|[AuthSchemes](#authschemes)|支援的驗證配置|
|[AuthServerAllowlist](#authserverallowlist)|設定允許驗證伺服器的清單|
|[DisableAuthNegotiateCnameLookup](#disableauthnegotiatecnamelookup)|當協調 Kerberos 驗證時停用 CNAME 查閱|
|[EnableAuthNegotiatePort](#enableauthnegotiateport)|Kerberos SPN 中包含非標準連接埠|
|[NtlmV2Enabled](#ntlmv2enabled)|控制是否要啟用 NTLMv2 驗證|
### [*原生訊息*](#native-messaging-policies)
|原則名稱|標題|
|-|-|
|[NativeMessagingAllowlist](#nativemessagingallowlist)|控制使用者可以使用的原生訊息主機|
|[NativeMessagingBlocklist](#nativemessagingblocklist)|設定原生訊息封鎖清單|
|[NativeMessagingUserLevelHosts](#nativemessaginguserlevelhosts)|允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)|
### [*密碼管理員和防護*](#password-manager-and-protection-policies)
|原則名稱|標題|
|-|-|
|[PasswordManagerEnabled](#passwordmanagerenabled)|啟用將密碼儲存到密碼管理員|
|[PasswordMonitorAllowed](#passwordmonitorallowed)|允許使用者在密碼不安全時收到警示提醒|
|[PasswordProtectionChangePasswordURL](#passwordprotectionchangepasswordurl)|設定變更密碼 URL|
|[PasswordProtectionLoginURLs](#passwordprotectionloginurls)|設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單|
|[PasswordProtectionWarningTrigger](#passwordprotectionwarningtrigger)|設定密碼保護警告觸發程序|
### [*列印*](#printing-policies)
|原則名稱|標題|
|-|-|
|[DefaultPrinterSelection](#defaultprinterselection)|預設印表機選擇規則|
|[PrintHeaderFooter](#printheaderfooter)|列印頁首與頁尾|
|[PrintPreviewUseSystemDefaultPrinter](#printpreviewusesystemdefaultprinter)|將系統預設的印表機設定為預設印表機|
|[PrintingEnabled](#printingenabled)|啟用列印|
|[UseSystemPrintDialog](#usesystemprintdialog)|使用系統列印對話方塊列印|
### [*Proxy 伺服器*](#proxy-server-policies)
|原則名稱|標題|
|-|-|
|[ProxyBypassList](#proxybypasslist)|設定 Proxy 許可規則|
|[ProxyMode](#proxymode)|設定 Proxy 伺服器設定|
|[ProxyPacUrl](#proxypacurl)|設定 Proxy .pac 檔案 URL|
|[ProxyServer](#proxyserver)|設定 Proxy 伺服器的位址或 URL|
|[ProxySettings](#proxysettings)|Proxy 設定|
### [*SmartScreen 設定*](#smartscreen-settings-policies)
|原則名稱|標題|
|-|-|
|[PreventSmartScreenPromptOverride](#preventsmartscreenpromptoverride)|防止略過網站的 Microsoft Defender SmartScreen 提示|
|[PreventSmartScreenPromptOverrideForFiles](#preventsmartscreenpromptoverrideforfiles)|防止略過關於下載項目的 Microsoft Defender SmartScreen 警告|
|[SmartScreenAllowListDomains](#smartscreenallowlistdomains)|設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單|
|[SmartScreenEnabled](#smartscreenenabled)|設定 Microsoft Defender SmartScreen|
|[SmartScreenForTrustedDownloadsEnabled](#smartscreenfortrusteddownloadsenabled)|強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目|
|[SmartScreenPuaEnabled](#smartscreenpuaenabled)|設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式|
### [*啟動、首頁和新的索引標籤頁面*](#startup-home-page-and-new-tab-page-policies)
|原則名稱|標題|
|-|-|
|[HomepageIsNewTabPage](#homepageisnewtabpage)|將新的索引標籤頁面設定為 [首頁]|
|[HomepageLocation](#homepagelocation)|設定首頁 URL|
|[NewTabPageAllowedBackgroundTypes](#newtabpageallowedbackgroundtypes)|設定新索引標籤頁面版面配置所允許的背景類型|
|[NewTabPageCompanyLogo](#newtabpagecompanylogo)|設定新的索引標籤頁面公司標誌 (已過時)|
|[NewTabPageHideDefaultTopSites](#newtabpagehidedefaulttopsites)|從新的索引標籤頁面隱藏預設熱門網站|
|[NewTabPageLocation](#newtabpagelocation)|設定新的索引標籤頁面 URL|
|[NewTabPageManagedQuickLinks](#newtabpagemanagedquicklinks)|設定新的索引標籤頁面快速連結|
|[NewTabPagePrerenderEnabled](#newtabpageprerenderenabled)|啟用預先載入的新索引標籤頁面，以加快頁面呈現速度|
|[NewTabPageSetFeedType](#newtabpagesetfeedtype)|設定 Microsoft Edge 新的索引標籤頁面體驗|
|[RestoreOnStartup](#restoreonstartup)|啟動時所採取的動作|
|[RestoreOnStartupURLs](#restoreonstartupurls)|瀏覽器啟動時開啟的網站|
|[ShowHomeButton](#showhomebutton)|在工具列上顯示 [首頁] 按鈕|
### [*其他*](#additional-policies)
|原則名稱|標題|
|-|-|
|[AddressBarMicrosoftSearchInBingProviderEnabled](#addressbarmicrosoftsearchinbingproviderenabled)|在網址列中啟用 Bing 專用 Microsoft Search 建議|
|[AdsSettingForIntrusiveAdsSites](#adssettingforintrusiveadssites)|含有干擾廣告網站的廣告設定|
|[AllowDeletingBrowserHistory](#allowdeletingbrowserhistory)|啟用刪除瀏覽器和下載歷程記錄|
|[AllowFileSelectionDialogs](#allowfileselectiondialogs)|允許檔案選取項目對話方塊|
|[AllowPopupsDuringPageUnload](#allowpopupsduringpageunload)|允許在卸載網頁期間顯示快顯視窗|
|[AllowSurfGame](#allowsurfgame)|允許衝浪遊戲|
|[AllowSyncXHRInPageDismissal](#allowsyncxhrinpagedismissal)|允許頁面在頁面關閉期間傳送同步 XHR 要求 (已淘汰)|
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
|[AutoplayAllowed](#autoplayallowed)|允許網站自動播放媒體|
|[BackgroundModeEnabled](#backgroundmodeenabled)|在 Microsoft Edge 關閉後繼續執行背景應用程式|
|[BackgroundTemplateListUpdatesEnabled](#backgroundtemplatelistupdatesenabled)|啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新|
|[BingAdsSuppression](#bingadssuppression)|封鎖 Bing 搜尋結果中的所有廣告|
|[BlockThirdPartyCookies](#blockthirdpartycookies)|封鎖第三方 Cookie|
|[BrowserAddProfileEnabled](#browseraddprofileenabled)|啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔|
|[BrowserGuestModeEnabled](#browserguestmodeenabled)|啟用來賓模式|
|[BrowserNetworkTimeQueriesEnabled](#browsernetworktimequeriesenabled)|允許查詢瀏覽器網路時間服務|
|[BrowserSignin](#browsersignin)|瀏覽器登入設定|
|[BuiltInDnsClientEnabled](#builtindnsclientenabled)|使用內建的 DNS 用戶端|
|[BuiltinCertificateVerifierEnabled](#builtincertificateverifierenabled)|決定是否使用內建的憑證驗證程式來驗證伺服器憑證 (已淘汰)|
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
|[ConfigureOnPremisesAccountAutoSignIn](#configureonpremisesaccountautosignin)|設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入|
|[ConfigureOnlineTextToSpeech](#configureonlinetexttospeech)|設定線上文字轉語音|
|[ConfigureShare](#configureshare)|設定共用體驗|
|[CustomHelpLink](#customhelplink)|指定自訂說明連結|
|[DNSInterceptionChecksEnabled](#dnsinterceptionchecksenabled)|DNS 攔截檢查已啟用|
|[DefaultBrowserSettingEnabled](#defaultbrowsersettingenabled)|將 Microsoft Edge 設定為預設瀏覽器|
|[DefaultSearchProviderContextMenuAccessAllowed](#defaultsearchprovidercontextmenuaccessallowed)|允許預設搜尋提供者操作功能表搜尋存取權|
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
|[EditFavoritesEnabled](#editfavoritesenabled)|允許使用者編輯我的最愛|
|[EnableDeprecatedWebPlatformFeatures](#enabledeprecatedwebplatformfeatures)|在限定時間內重新啟用已過時的網頁平台功能|
|[EnableDomainActionsDownload](#enabledomainactionsdownload)|啟用從 Microsoft 進行網域動作下載 (已過時) |
|[EnableOnlineRevocationChecks](#enableonlinerevocationchecks)|啟用線上 OCSP/CRL 檢查|
|[EnableSha1ForLocalAnchors](#enablesha1forlocalanchors)|允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)|
|[EnterpriseHardwarePlatformAPIEnabled](#enterprisehardwareplatformapienabled)|允許受管擴充功能使用企業硬體平台 API|
|[EnterpriseModeSiteListManagerAllowed](#enterprisemodesitelistmanagerallowed)|允許存取 Enterprise Mode Site List Manager 工具|
|[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](#exemptdomainfiletypepairsfromfiletypedownloadwarnings)|針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告|
|[ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol)|控制與實驗和設定服務的通訊|
|[ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox)|在外部通訊協定對話方塊中顯示「一律開啟」核取方塊|
|[FamilySafetySettingsEnabled](#familysafetysettingsenabled)|允許使用者設定家長監護服務|
|[FavoritesBarEnabled](#favoritesbarenabled)|啟用我的最愛列|
|[ForceBingSafeSearch](#forcebingsafesearch)|強制執行 Bing 安全搜尋|
|[ForceCertificatePromptsOnMultipleMatches](#forcecertificatepromptsonmultiplematches)|設定使用 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，Microsoft Edge 是否應自動選取憑證|
|[ForceEphemeralProfiles](#forceephemeralprofiles)|啟用使用暫時設定檔|
|[ForceGoogleSafeSearch](#forcegooglesafesearch)|強制執行 Google 安全搜尋|
|[ForceLegacyDefaultReferrerPolicy](#forcelegacydefaultreferrerpolicy)|使用預設的查閱者原則－當降級且無查閱者時 (已被取代)。|
|[ForceNetworkInProcess](#forcenetworkinprocess)|強制網路程式碼在瀏覽器處理程序中執行 (已過時) |
|[ForceYouTubeRestrict](#forceyoutuberestrict)|強制最小 YouTube 限制模式|
|[FullscreenAllowed](#fullscreenallowed)|允許全螢幕模式|
|[GloballyScopeHTTPAuthCacheEnabled](#globallyscopehttpauthcacheenabled)|啟用全域範圍的 HTTP 驗證快取|
|[GoToIntranetSiteForSingleWordEntryInAddressBar](#gotointranetsiteforsinglewordentryinaddressbar)|強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目|
|[HSTSPolicyBypassList](#hstspolicybypasslist)|設定會略過 HSTS 原則檢查的名稱清單|
|[HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled)|可用時便使用硬體加速|
|[HideFirstRunExperience](#hidefirstrunexperience)|隱藏初次執行體驗與啟動顯示畫面|
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
|[InPrivateModeAvailability](#inprivatemodeavailability)|設定 InPrivate 模式可用性|
|[IntensiveWakeUpThrottlingEnabled](#intensivewakeupthrottlingenabled)|管理 IntensiveWakeUpThrottling 功能|
|[InternetExplorerIntegrationEnhancedHangDetection](#internetexplorerintegrationenhancedhangdetection)|針對 Internet Explorer 模式設定增強的當機偵測|
|[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel)|設定 Internet Explorer 整合|
|[InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist)|設定 Enterprise Mode Site List|
|[InternetExplorerIntegrationSiteRedirect](#internetexplorerintegrationsiteredirect)|指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式|
|[IsolateOrigins](#isolateorigins)|為特定來源啟用網站隔離|
|[LocalProvidersEnabled](#localprovidersenabled)|允許來自本地提供者的建議|
|[ManagedFavorites](#managedfavorites)|設定我的最愛|
|[ManagedSearchEngines](#managedsearchengines)|管理搜尋引擎|
|[MaxConnectionsPerProxy](#maxconnectionsperproxy)|同時連線到 Proxy 伺服器的最大數目|
|[MediaRouterCastAllowAllIPs](#mediaroutercastallowallips)|允許 Google Cast 連線至所有 IP 位址上的投射裝置|
|[MetricsReportingEnabled](#metricsreportingenabled)|啟用使用方式和當機相關的資料報告 (已過時)|
|[NativeWindowOcclusionEnabled](#nativewindowocclusionenabled)|啟用原生視窗遮蔽|
|[NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout)|針對企業模式網站清單，設定索引標籤瀏覽逾時延遲|
|[NetworkPredictionOptions](#networkpredictionoptions)|啟用網路預測|
|[NonRemovableProfileEnabled](#nonremovableprofileenabled)|設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔|
|[OverrideSecurityRestrictionsOnInsecureOrigin](#overridesecurityrestrictionsoninsecureorigin)|控制不安全來源中安全性限制套用的地方|
|[PaymentMethodQueryEnabled](#paymentmethodqueryenabled)|允許網站查詢可用的付款方式|
|[PersonalizationReportingEnabled](#personalizationreportingenabled)|透過傳送瀏覽歷程記錄至 Microsoft，允許廣告、搜尋及新聞個人化|
|[PinningWizardAllowed](#pinningwizardallowed)|允許 [釘選到工作列精靈]|
|[ProactiveAuthEnabled](#proactiveauthenabled)|啟用主動式驗證|
|[PromotionalTabsEnabled](#promotionaltabsenabled)|啟用全分頁促銷內容|
|[PromptForDownloadLocation](#promptfordownloadlocation)|詢問下載檔案的儲存位置|
|[QuicAllowed](#quicallowed)|允許 QUIC 通訊協定|
|[RelaunchNotification](#relaunchnotification)|通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新|
|[RelaunchNotificationPeriod](#relaunchnotificationperiod)|設定更新通知的時間週期|
|[RendererCodeIntegrityEnabled](#renderercodeintegrityenabled)|啟用轉譯器程式碼完整性|
|[RequireOnlineRevocationChecksForLocalAnchors](#requireonlinerevocationchecksforlocalanchors)|指定本機信賴起點是否需要線上 OCSP/CRL 檢查|
|[ResolveNavigationErrorsUseWebService](#resolvenavigationerrorsusewebservice)|啟用使用 Web 服務來解決導覽錯誤|
|[RestrictSigninToPattern](#restrictsignintopattern)|限制哪些帳戶可用為 Microsoft Edge 主要帳戶|
|[RoamingProfileLocation](#roamingprofilelocation)|設定漫遊設定檔目錄|
|[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)|啟用 Microsoft Edge 設定檔資料的快取副本|
|[RunAllFlashInAllowMode](#runallflashinallowmode)|將 Adobe Flash 內容設定延伸至所有內容|
|[SSLErrorOverrideAllowed](#sslerroroverrideallowed)|允許使用者從 HTTPS 警告頁面繼續進行|
|[SSLVersionMin](#sslversionmin)|已啟用最低 TLS 版本|
|[SaveCookiesOnExit](#savecookiesonexit)|在 Microsoft Edge 關閉時儲存 Cookie|
|[SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled)|停用儲存瀏覽器歷程記錄|
|[ScreenCaptureAllowed](#screencaptureallowed)|允許或拒絕螢幕擷取畫面|
|[ScrollToTextFragmentEnabled](#scrolltotextfragmentenabled)|啟用捲動至在 URL 片段中指定的文字|
|[SearchSuggestEnabled](#searchsuggestenabled)|啟用搜尋建議|
|[SecurityKeyPermitAttestation](#securitykeypermitattestation)|不需要權限即可使用直接存取安全性金鑰證明的網站或網域|
|[SendIntranetToInternetExplorer](#sendintranettointernetexplorer)|將所有內部網路網站傳送到 Internet Explorer|
|[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices)|傳送網站資訊以改善 Microsoft 服務 (已過時)|
|[ShowOfficeShortcutInFavoritesBar](#showofficeshortcutinfavoritesbar)|在 [我的最愛] 列中顯示 Microsoft Office 捷徑|
|[SignedHTTPExchangeEnabled](#signedhttpexchangeenabled)|啟用 Signed HTTP Exchange (SXG) 支援|
|[SitePerProcess](#siteperprocess)|為每個網站啟用網站隔離|
|[SpellcheckEnabled](#spellcheckenabled)|啟用拼字檢查|
|[SpellcheckLanguage](#spellchecklanguage)|啟用特定拼字檢查語言|
|[SpellcheckLanguageBlocklist](#spellchecklanguageblocklist)|強制停用拼字檢查語言|
|[StricterMixedContentTreatmentEnabled](#strictermixedcontenttreatmentenabled)|針對混合內容啟用更嚴格的處理 (已淘汰)|
|[SuppressUnsupportedOSWarning](#suppressunsupportedoswarning)|隱藏不支援的 OS 警告|
|[SyncDisabled](#syncdisabled)|透過 Microsoft 同步服務停用資料同步|
|[SyncTypesListDisabled](#synctypeslistdisabled)|設定同步服務將排除的類型清單|
|[TLS13HardeningForLocalAnchorsEnabled](#tls13hardeningforlocalanchorsenabled)|啟用適於本機信賴起點的 TLS 1.3 安全性功能 (已過時)|
|[TLSCipherSuiteDenyList](#tlsciphersuitedenylist)|指定欲停用的 TLS 加密套件|
|[TabFreezingEnabled](#tabfreezingenabled)|允許凍結背景索引標籤|
|[TaskManagerEndProcessEnabled](#taskmanagerendprocessenabled)|啟用在瀏覽器工作管理員中結束處理程序|
|[TotalMemoryLimitMb](#totalmemorylimitmb)|設定單一 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)|
|[TrackingPrevention](#trackingprevention)|封鎖使用者的網頁瀏覽活動追蹤|
|[TranslateEnabled](#translateenabled)|啟用翻譯|
|[URLAllowlist](#urlallowlist)|定義受允許的 URL 清單|
|[URLBlocklist](#urlblocklist)|封鎖存取 URL 清單|
|[UserAgentClientHintsEnabled](#useragentclienthintsenabled)|啟用使用者代理程式用戶端提示功能 (已過時)|
|[UserDataDir](#userdatadir)|設定使用者資料目錄|
|[UserFeedbackAllowed](#userfeedbackallowed)|允許使用者意見反應|
|[VideoCaptureAllowed](#videocaptureallowed)|允許或封鎖視訊擷取|
|[VideoCaptureAllowedUrls](#videocaptureallowedurls)|無需要求權限即可存取視訊擷取裝置的網站|
|[WPADQuickCheckEnabled](#wpadquickcheckenabled)|設定 WPAD 最佳化|
|[WebAppInstallForceList](#webappinstallforcelist)|設定強制安裝 Web 應用程式的清單|
|[WebComponentsV0Enabled](#webcomponentsv0enabled)|在 M84 前，重新啟用 Web 元件 v0 API。|
|[WebDriverOverridesIncompatiblePolicies](#webdriveroverridesincompatiblepolicies)|允許 WebDriver 覆寫不相容原則 (已過時) |
|[WebRtcLocalIpsAllowedUrls](#webrtclocalipsallowedurls)|管理由 WebRTC 暴露的本機 IP 位址|
|[WebRtcLocalhostIpHandling](#webrtclocalhostiphandling)|限制由 WebRTC 暴露的本機 IP 位址|
|[WebRtcUdpPortRange](#webrtcudpportrange)|限制 WebRTC 所使用的本機 UDP 連接埠範圍|
|[WinHttpProxyResolverEnabled](#winhttpproxyresolverenabled)|使用 Windows proxy 解析程式 (已過時) |




  ## 應用程式防護設定原則

  [回到頁首](#microsoft-edge---policies)

  ### ApplicationGuardContainerProxy
  #### 應用程式防護容器 Proxy
  
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ApplicationGuardContainerProxy
  - GP 名稱：應用程式防護容器 Proxy
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/應用程式防護設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ApplicationGuardContainerProxy
  - 值類型：REG_SZ
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ApplicationGuardContainerProxy = {
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  

  [回到頁首](#microsoft-edge---policies)

  ## 投射原則

  [回到頁首](#microsoft-edge---policies)

  ### EnableMediaRouter
  #### 啟用 Google Cast
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用此原則以啟用 Google Cast。 使用者將可以從應用程式功能表、網頁內容功能表、已啟用投射的網站上的媒體控制項和 (如有顯示) 投射工具列圖示啟動它。

停用此原則可停用 Google Cast。

根據預設，Google Cast 將會啟用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableMediaRouter
  - GP 名稱：啟用 Google Cast
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/投射
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableMediaRouter
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableMediaRouter
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ShowCastIconInToolbar
  #### 在工具列中顯示投射圖示
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  將此原則設定為 true 即可在工具列或溢位功能表顯示投射工具列圖示。 使用者將無法移除它。

如果未設定或停用此原則，則使用者可使用圖示的關聯式功能表來釘選或移除圖示。

如果您也將 [EnableMediaRouter](#enablemediarouter) 原則設定為 false，則會忽略此原則，且不會顯示工具列圖示。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ShowCastIconInToolbar
  - GP 名稱：在工具列中顯示投射圖示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/投射
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ShowCastIconInToolbar
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ShowCastIconInToolbar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 內容設定原則

  [回到頁首](#microsoft-edge---policies)

  ### AutoSelectCertificateForUrls
  #### 自動選取這些網站的用戶端憑證
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 模式指定網站清單，Microsoft Edge 應為其自動選擇用戶端憑證 (如果網站要求)。

該值必須是 JSON 字典字串化的陣列。 每個字典的格式必須為 { "pattern": "$URL_PATTERN", "filter" : $FILTER }，其中 $URL_PATTERN 是內容設定模式。 $FILTER 會限制瀏覽器要自動選擇哪個用戶端憑證。 與篩選器無關，僅選擇與伺服器憑證要求相符的憑證。 例如，如果 $FILTER 的格式為{ "ISSUER": { "CN": "$ISSUER_CN" } }，則僅選擇由具有 CommonName $ISSUER_CN 的憑證所發佈的用戶端憑證。 如果 $FILTER 包含 "ISSUER" 和 "SUBJECT" 部分，用戶端憑證必須同時滿足兩個要選擇的條件。 如果 $FILTER 指定一個組織 ("O")，則憑證必須具有至少一個與要選擇的指定值相符的組織。 如果 $FILTER 指定組織單位 ("OU")，則憑證必須具有至少一個與要選擇的指定值相符的組織單位。 如果 $FILTER 為空字典 {}，則用戶端憑證的選擇沒有任何其他限制。

如果未設定此原則，則所有網站皆不會進行自動選擇。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoSelectCertificateForUrls
  - GP 名稱：自動選取這些網站的用戶端憑證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AutoSelectCertificateForUrls\1 = {"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutoSelectCertificateForUrls
  - 範例值：
``` xml
<array>
  <string>{"pattern":"https://www.contoso.com","filter":{"ISSUER":{"CN":"certificate issuer name", "L": "certificate issuer location", "O": "certificate issuer org", "OU": "certificate issuer org unit"}, "SUBJECT":{"CN":"certificate subject name", "L": "certificate subject location", "O": "certificate subject org", "OU": "certificate subject org unit"}}}</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CookiesAllowedForUrls
  #### 允許特定網站上的 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義允許設定 Cookie 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需詳細資訊，請參閱 [CookiesBlockedForUrls](#cookiesblockedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 原則。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- CookiesAllowedForUrls

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

若要避免在結束時刪除 Cookie，請設定 [SaveCookiesOnExit](#savecookiesonexit) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CookiesAllowedForUrls
  - GP 名稱：允許特定網站上的 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\CookiesAllowedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CookiesAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CookiesBlockedForUrls
  #### 封鎖特定網站上的 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義無法設定 Cookie 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需詳細資訊，請參閱 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls) 原則。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- CookiesBlockedForUrls

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- [CookiesSessionOnlyForUrls](#cookiessessiononlyforurls)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CookiesBlockedForUrls
  - GP 名稱：封鎖特定網站上的 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\CookiesBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CookiesBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CookiesSessionOnlyForUrls
  #### 限制來自特定網站的 Cookie 匯入目前的工作階段
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  工作階段結束 (關閉視窗) 時，會刪除由符合您所定義 URL 模式的網站建立的 Cookie。

由不符合模式的網站建立的 Cookie 會由 [DefaultCookiesSetting](#defaultcookiessetting) 原則 (如有設定) 或由使用者個人設定控制。 如果未設定此原則，則這也是預設行為。

如果 Microsoft Edge 正以背景模式執行，當最後一個視窗關閉時，則工作階段可能會停止執行，這表示視窗關閉時將不會清除 Cookie。 如需將 Microsoft Edge 設定在背景模式中執行時會發生之情況的詳細資訊，請參閱 [BackgroundModeEnabled](#backgroundmodeenabled) 原則。

您也可以使用 [CookiesAllowedForUrls](#cookiesallowedforurls) 和 [CookiesBlockedForUrls](#cookiesblockedforurls) 原則，以控制哪些網站可以建立 Cookie。

請注意，這三個原則之間不可有衝突的 URL 模式設定：

- [CookiesBlockedForUrls](#cookiesblockedforurls)

- [CookiesAllowedForUrls](#cookiesallowedforurls)

- CookiesSessionOnlyForUrls

如果將 [RestoreOnStartup](#restoreonstartup) 原則設定為從先前的工作階段還原 URL，即會忽略此原則，並為這些網站永久儲存 Cookie。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CookiesSessionOnlyForUrls
  - GP 名稱：限制來自特定網站的 Cookie 匯入目前的工作階段
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\CookiesSessionOnlyForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CookiesSessionOnlyForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultCookiesSetting
  #### 設定 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制網站是否可在使用者的裝置上建立 Cookie。 此原則為全部或皆不 - 您可以讓所有網站建立 Cookie，或不讓任何網站建立 Cookie。 您無法使用此原則來啟用來自特定網站的 Cookie。

將原則設定為 'SessionOnly'，以在工作階段關閉時清除 Cookie。 如果 Microsoft Edge 正以背景模式執行，當最後一個視窗關閉時，則工作階段可能會停止執行，這表示視窗關閉時將不會清除 Cookie。 如需將 Microsoft Edge 設定在背景模式中執行時會發生之情況的詳細資訊，請參閱 [BackgroundModeEnabled](#backgroundmodeenabled) 原則。

如果未設定此原則，則會使用預設值 'AllowCookies'，且使用者可以在 Microsoft Edge 設定中變更此設定。 (如果您不希望使用者能夠變更此設定，請設定原則。)

原則選項對應：

* AllowCookies (1) = 讓所有網站建立 Cookie

* BlockCookies (2) = 不要讓任何網站建立 Cookie

* SessionOnly (4) = 在工作階段期間保留 Cookie，[SaveCookiesOnExit](#savecookiesonexit) 中所列的項目除外

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultCookiesSetting
  - GP 名稱：設定 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultCookiesSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultCookiesSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultGeolocationSetting
  #### 預設地理位置設定值
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否可追蹤使用者的實體位置。 您可以預設允許追蹤 ('AllowGeolocation')、預設拒絕 ('BlockGeolocation')，或在每次網站要求其位置時詢問使用者 ('AskGeolocation')。

如果未設定此原則，則會使用 'AskGeolocation'，且使用者可以變更此設定。

原則選項對應：

* AllowGeolocation (1) = 允許網站追蹤使用者的實體位置

* BlockGeolocation (2) = 不允許任何網站追蹤使用者的實體位置

* AskGeolocation (3) = 在網站要追蹤使用者的實體位置時詢問使用者

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultGeolocationSetting
  - GP 名稱：預設地理位置設定值
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultGeolocationSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultGeolocationSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultImagesSetting
  #### 預設影像設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否可以顯示影像。 您可以在所有網站上允許影像 ('AllowImages')，或在所有網站上封鎖影像 ('BlockImages')。

如果未設定此原則，則預設會允許顯示影像，且使用者可以變更此設定。

原則選項對應：

* AllowImages (1) = 允許所有網站顯示所有影像

* BlockImages (2) = 不允許任何網站顯示影像

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultImagesSetting
  - GP 名稱：預設影像設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultImagesSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultImagesSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultInsecureContentSetting
  #### 控制不安全內容例外狀況的使用
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  允許您設定使用者是否可以新增例外，以允許特定網站的混合內容。

可以針對使用 [InsecureContentAllowedForUrls](#insecurecontentallowedforurls) 和 [InsecureContentBlockedForUrls](#insecurecontentblockedforurls) 原則的特定 URL 模式覆寫此原則。

如果未設定此原則，使用者將可以新增例外，以允許可封鎖的混合內容，並停用選擇性可封鎖混合內容的自動升級。

原則選項對應：

* BlockInsecureContent (2) = 不允許任何網站載入混合內容

* AllowExceptionsInsecureContent (3) = 允許使用者新增例外，以允許混合內容

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultInsecureContentSetting
  - GP 名稱：控制不安全內容例外狀況的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultInsecureContentSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultInsecureContentSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultJavaScriptSetting
  #### 預設 JavaScript 設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否可以執行 JavaScript。 您可以為所有網站允許 ('AllowJavaScript') 或為所有網站封鎖 ('BlockJavaScript')。

如果未設定此原則，則預設為所有網站都可以執行 JavaScript，且使用者可以變更此設定。

原則選項對應：

* AllowJavaScript (1) = 允許所有網站執行 JavaScript

* BlockJavaScript (2) = 不允許任何網站執行 JavaScript

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultJavaScriptSetting
  - GP 名稱：預設 JavaScript 設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultJavaScriptSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultJavaScriptSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultNotificationsSetting
  #### 預設通知設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否可以顯示桌面通知。 您可以預設允許 ('AllowNotifications')、預設拒絕 ('BlockNotifications')，或在每次網站想要顯示通知時詢問使用者 ('AskNotifications')。

如果未設定此原則，則預設為允許顯示通知，且使用者可以變更此設定。

原則選項對應：

* AllowNotifications (1) = 允許網站顯示桌面通知

* BlockNotifications (2) = 不允許任何網站顯示桌面通知

* AskNotifications (3) = 每次網站想要顯示桌面通知時詢問

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultNotificationsSetting
  - GP 名稱：預設通知設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultNotificationsSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultNotificationsSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultPluginsSetting
  #### 預設 Adobe Flash 設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  判定 [PluginsAllowedForUrls](#pluginsallowedforurls) 或 [PluginsBlockedForUrls](#pluginsblockedforurls) 中未涵蓋的網站是否可自動執行 Adobe Flash 外掛程式。 您可以選取 'BlockPlugins' 以在所有網站上封鎖 Adobe Flash；或者也可以選取 'ClickToPlay' 以讓 Adobe Flash 執行，但要求使用者按一下預留位置來啟動它。 在任何情況下，[PluginsAllowedForUrls](#pluginsallowedforurls) 和 [PluginsBlockedForUrls](#pluginsblockedforurls) 原則優先於 'DefaultPluginsSetting'。

只有在 [PluginsAllowedForUrls](#pluginsallowedforurls) 原則中明確列出的網域才會允許自動播放。 如果想要為所有網站啟用自動播放功能，請考慮將 http://* 和 https://* 新增至此清單中。

如果未設定此原則，則使用者可以手動變更此設定。

之前的 '1' 選項會設定 allow-all，但此功能現在僅由 [PluginsAllowedForUrls](#pluginsallowedforurls) 原則處理。  使用 '1' 的現有原則將會以 'ClickToPlay' 模式運作。

原則選項對應：

* BlockPlugins (2) = 封鎖 Adobe Flash 外掛程式

* ClickToPlay (3) = 按一下以播放

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultPluginsSetting
  - GP 名稱：預設 Adobe Flash 設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPluginsSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultPluginsSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultPopupsSetting
  #### 預設快顯視窗設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否可以顯示快顯視窗。 您可以在所有網站上允許 ('AllowPopups')，或在所有網站上封鎖 ('BlockPopups')。

如果未設定此原則，則預設會封鎖快顯視窗，且使用者可以變更此設定。

原則選項對應：

* AllowPopups (1) = 允許所有網站顯示快顯視窗

* BlockPopups (2) = 不允許任何網站顯示快顯視窗

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultPopupsSetting
  - GP 名稱：預設快顯視窗設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPopupsSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultPopupsSetting
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultWebBluetoothGuardSetting
  #### 控制 Web 藍牙 API 的使用
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制網站是否能夠存取附近的藍牙裝置。 您可以完全封鎖或存取權或要求網站在每次想要存取藍牙裝置時詢問使用者。

如果未設定此原則，則會使用預設值 (AskWebBluetooth'，表示每次都詢問使用者)，且使用者可以變更此設定。

原則選項對應：

* BlockWebBluetooth (2) = 不允許任何網站使用 Web Bluetooth API 來要求存取藍牙裝置

* AskWebBluetooth (3) = 允許網站要求使用者授與附近藍牙裝置存取權

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultWebBluetoothGuardSetting
  - GP 名稱：控制 Web 藍牙 API 的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultWebBluetoothGuardSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultWebBluetoothGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultWebUsbGuardSetting
  #### 控制 WebUSB API 的使用
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定網站是否能夠存取連接的 USB 裝置。 您可以完全封鎖存取或在每次網站想要取得連接的 USB 裝置的存取時詢問使用者。

您可以使用 [WebUsbAskForUrls](#webusbaskforurls) 和 [WebUsbBlockedForUrls](#webusbblockedforurls) 原則來針對特定 URL 模式覆寫此原則。

如果未設定此原則，則預設為網站可以詢問使用者是否可以存取連接的 USB 裝置 ('AskWebUsb')，且使用者可以變更此設定。

原則選項對應：

* BlockWebUsb (2) = 不允許任何網站透過 WebUSB API 要求存取 USB 裝置

* AskWebUsb (3) = 允許網站詢問使用者，以授與連接的 USB 裝置之存取權

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultWebUsbGuardSetting
  - GP 名稱：控制 WebUSB API 的使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultWebUsbGuardSetting
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultWebUsbGuardSetting
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImagesAllowedForUrls
  #### 允許這些網站上的影像
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義可顯示影像的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultImagesSetting](#defaultimagessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImagesAllowedForUrls
  - GP 名稱：允許這些網站上的影像
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\ImagesAllowedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImagesAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImagesBlockedForUrls
  #### 封鎖特定網站上的影像
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義不允許顯示影像的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultImagesSetting](#defaultimagessetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImagesBlockedForUrls
  - GP 名稱：封鎖特定網站上的影像
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\ImagesBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImagesBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### InsecureContentAllowedForUrls
  #### 允許指定網站上的不安全內容
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  建立 URL 模式的清單，以指定可顯示不安全混合內容 (即 HTTPS 網站上的 HTTP 內容) 的網站。

如果未設定此原則，則會封鎖可封鎖的混合內容，並升級選擇性可封鎖的混合內容。 不過，將允許使用者設定例外，以允許特定網站的不安全混合內容。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InsecureContentAllowedForUrls
  - GP 名稱：允許指定網站上的不安全內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\1 = https://www.example.com
SOFTWARE\Policies\Microsoft\Edge\InsecureContentAllowedForUrls\2 = [*.]example.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：InsecureContentAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### InsecureContentBlockedForUrls
  #### 封鎖指定網站上的不安全內容
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  建立 URL 模式的清單，以指定不允許顯示可封鎖 (即使用中) 混合內容 (即 HTTPS 網站上的 HTTP 內容) 的網站，並針對它將選擇性可封鎖混合內容升級停用。

如果未設定此原則，則會封鎖可封鎖的混合內容，並升級選擇性可封鎖的混合內容。 不過，將允許使用者設定例外，以允許特定網站的不安全混合內容。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InsecureContentBlockedForUrls
  - GP 名稱：封鎖指定網站上的不安全內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\1 = https://www.example.com
SOFTWARE\Policies\Microsoft\Edge\InsecureContentBlockedForUrls\2 = [*.]example.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：InsecureContentBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### JavaScriptAllowedForUrls
  #### 允許特定網站上的 JavaScript
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義允許執行 JavaScript 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：JavaScriptAllowedForUrls
  - GP 名稱：允許特定網站上的 JavaScript
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\JavaScriptAllowedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：JavaScriptAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### JavaScriptBlockedForUrls
  #### 封鎖特定網站上的 JavaScript
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義不允許執行 JavaScript 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultJavaScriptSetting](#defaultjavascriptsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：JavaScriptBlockedForUrls
  - GP 名稱：封鎖特定網站上的 JavaScript
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\JavaScriptBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：JavaScriptBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabled
  #### 啟用預設舊版 SameSite Cookie 行為設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  讓您將所有 Cookie 還原為舊版 SameSite 行為。 還原為舊版行為會導致未指定 SameSite 屬性的 Cookie 被視為 "SameSite=None"，並移除 "SameSite=None" Cookie 傳輸 "Secure" 屬性的需求。

如果未設定此原則，則未指定 SameSite 屬性的 Cookie 的預設行為，將取決於 SameSite-by-default 功能的其他設定來源。 此功能可能是由現場試驗或在 edge://flags 中啟用 same-site-by-default-cookies 旗標而設定。

原則選項對應：

* DefaultToLegacySameSiteCookieBehavior (1) = 還原為所有網站上 Cookie 的舊版 SameSite 行為。

* DefaultToSameSiteByDefaultCookieBehavior (2) = 針對所有網站上 Cookie 使用預設的 SameSite 行為

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：LegacySameSiteCookieBehaviorEnabled
  - GP 名稱：啟用預設舊版 SameSite Cookie 行為設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：LegacySameSiteCookieBehaviorEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：LegacySameSiteCookieBehaviorEnabled
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### LegacySameSiteCookieBehaviorEnabledForDomainList
  #### 將指定網站上的 Cookie 還原至舊版 SameSite 行為
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  針對符合指定模式網域設定的 Cookie 將還原為舊版 SameSite 行為。

還原為舊版行為會導致未指定 SameSite 屬性的 Cookie 被視為 "SameSite=None"，並移除 "SameSite=None" Cookie 傳輸 "Secure" 屬性的需求。

如果未設定此原則，則會使用全域預設值。 全域預設值也將用於您指定的模式未涵蓋的網域上的 Cookie。

全域預設值可以使用 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled) 原則進行設定。 如果未設定 [LegacySameSiteCookieBehaviorEnabled](#legacysamesitecookiebehaviorenabled)，則全域預設值會後援到其他設定來源。

請注意，您在此原則中列出的模式會被視為網域，而非 URL，因此不應指定配置或連接埠。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：LegacySameSiteCookieBehaviorEnabledForDomainList
  - GP 名稱：將指定網站上的 Cookie 還原至舊版 SameSite 行為
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\1 = www.example.com
SOFTWARE\Policies\Microsoft\Edge\LegacySameSiteCookieBehaviorEnabledForDomainList\2 = [*.]example.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：LegacySameSiteCookieBehaviorEnabledForDomainList
  - 範例值：
``` xml
<array>
  <string>www.example.com</string>
  <string>[*.]example.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NotificationsAllowedForUrls
  #### 允許特定網站上的通知
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓您建立 URL 模式的清單，以指定允許顯示通知的網站。

如果您未設定此原則，全域預設值將會套用至所有網站。 如果已設定此原則，預設值會取自　[DefaultNotificationsSetting](#defaultnotificationssetting) 原則或使用者的個人設定。 如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NotificationsAllowedForUrls
  - GP 名稱：允許特定網站上的通知
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\NotificationsAllowedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NotificationsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NotificationsBlockedForUrls
  #### 封鎖特定網站上的通知
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓您建立 URL 模式的清單，以指定不允許顯示通知的網站。

如果您未設定此原則，全域預設值將會套用至所有網站。 如果已設定此原則，預設值會取自　[DefaultNotificationsSetting](#defaultnotificationssetting) 原則或使用者的個人設定。 如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NotificationsBlockedForUrls
  - GP 名稱：封鎖特定網站上的通知
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\NotificationsBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NotificationsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PluginsAllowedForUrls
  #### 允許特定網站上的 Adobe Flash 外掛程式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義可執行 Adobe Flash 外掛程式的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPluginsSetting](#defaultpluginssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 不過，從 M85 開始，此原則已不再支援主機使用帶有 ‘*' 和 '[*.]’ 等的萬用字元。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PluginsAllowedForUrls
  - GP 名稱：允許特定網站上的 Adobe Flash 外掛程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls\2 = http://contoso.edu:8080

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PluginsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PluginsBlockedForUrls
  #### 封鎖特定網站上的 Adobe Flash 外掛程式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義遭封鎖而無法執行 Adobe Flash 的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPluginsSetting](#defaultpluginssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。 不過，從 M85 開始，此原則已不再支援主機使用帶有 ‘*' 和 '[*.]’ 等的萬用字元。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PluginsBlockedForUrls
  - GP 名稱：封鎖特定網站上的 Adobe Flash 外掛程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\PluginsBlockedForUrls\2 = http://contoso.edu:8080

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PluginsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>http://contoso.edu:8080</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PopupsAllowedForUrls
  #### 允許特定網站上的快顯視窗
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義可開啟快顯視窗的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPopupsSetting](#defaultpopupssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PopupsAllowedForUrls
  - GP 名稱：允許特定網站上的快顯視窗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\PopupsAllowedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PopupsAllowedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PopupsBlockedForUrls
  #### 封鎖特定網站上的快顯視窗
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義遭封鎖而無法開啟快顯視窗的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultPopupsSetting](#defaultpopupssetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PopupsBlockedForUrls
  - GP 名稱：封鎖特定網站上的快顯視窗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\PopupsBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PopupsBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RegisteredProtocolHandlers
  #### 登錄通訊協定處理常式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定這個原則 (僅限建議使用) 來登錄通訊協定處理常式清單。 此清單會與使用者登錄的清單合併，而且兩者皆可供使用。

登錄通訊協定處理常式：

- 將通訊協定屬性設定為配置 (例如「mailto」)
- 將 URL 屬性設定為處理「通訊協定」欄位中指定配置的應用程式之 URL 屬性。 模式可以包含「%s」預留位置，它會由已處理的 URL 取代。

使用者無法移除由此原則登錄的通訊協定處理常式。 不過，他們可以安裝新的預設通訊協定處理常式來覆寫現有的通訊協定處理常式。

  #### 支援的功能：
  - 可強制執行：否
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RegisteredProtocolHandlers
  - GP 名稱：登錄通訊協定處理常式
  - GP 路徑 (強制)：不適用
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/內容設定
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：不適用
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：RegisteredProtocolHandlers
  - 值類型：REG_SZ
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\RegisteredProtocolHandlers = [
  {
    "default": true, 
    "protocol": "mailto", 
    "url": "https://mail.contoso.com/mail/?extsrc=mailto&url=%s"
  }
]
```


  #### Mac 資訊和設定
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

  ### WebUsbAllowDevicesForUrls
  #### 授與特定網站連線到特定 USB 裝置的存取權
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許您設定一份 URL 清單，指定哪些網站會自動獲授與權限，以存取具有指定廠商和產品識別碼的 USB 裝置。 清單中的每個項目都必須包含裝置和 URL，原則才會有效。 裝置中的每個項目都可以包含廠商識別碼和產品識別碼欄位。 省略的任何識別碼都會被視為萬用字元，並有一個例外，且該例外是不能指定產品識別碼但未同時指定廠商識別碼。 否則，原則將會無效，且會被忽略。

USB 權限模型會使用要求端網站的 URL (「要求端 URL」) 和最上層框架網站的 URL (「內嵌 URL」)，將授權授與給要求端 URL 以存取 USB 裝置。 在 iframe 中載入要求端網站時，要求端 URL 可能與內嵌 URL 不同。 因此，"urls" 欄位最多可包含兩個以逗號分隔的 URL 字串，以便分別指定要求端和內嵌 URL。 如果僅指定一個 URL，當要求端網站的 URL 與符合此 URL 時，就會授與對應的 USB 裝置的存取權，而無論內嵌狀態為何。 "urls" 中的 URL 必須是有效的 URL，否則將忽略該原則。

如果將此原則保留為未設定，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

此原則中的 URL 模式不應與透過 [WebUsbBlockedForUrls](#webusbblockedforurls) 設定的衝突。 如果發生衝突，則此原則優先於 [WebUsbBlockedForUrls](#webusbblockedforurls) 和 [WebUsbAskForUrls](#webusbaskforurls)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebUsbAllowDevicesForUrls
  - GP 名稱：授與特定網站連線到特定 USB 裝置的存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebUsbAllowDevicesForUrls
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ### WebUsbAskForUrls
  #### 允許特定網站上的 WebUSB
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義可要求使用者取得 USB 裝置存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

在此原則中定義的 URL 模式不能與 [WebUsbBlockedForUrls](#webusbblockedforurls) 原則中設定的衝突，您不能同時允許和封鎖一個 URL。 如需有效 URL 模式的詳細資訊，請參照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebUsbAskForUrls
  - GP 名稱：允許特定網站上的 WebUSB
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\WebUsbAskForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebUsbAskForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebUsbBlockedForUrls
  #### 封鎖特定網站上的 WebUSB
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義無法要求使用者授與其 USB 裝置存取權的網站清單。

如果未設定此原則，則會對所有網站使用來自 [DefaultWebUsbGuardSetting](#defaultwebusbguardsetting) 原則 (如有設定) 或使用者個人設定的全域預設值。

在此原則中定義的 URL 模式不能與 [WebUsbAskForUrls](#webusbaskforurls) 原則中設定的衝突。 您不能同時允許和封鎖 URL。  如需有效 URL 模式的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebUsbBlockedForUrls
  - GP 名稱：封鎖特定網站上的 WebUSB
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/內容設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\WebUsbBlockedForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebUsbBlockedForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 預設搜尋提供者原則

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderEnabled
  #### 啟用預設搜尋提供者
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用使用預設搜尋提供者的功能。

如果啟用此原則，則使用者可以透過在網址列中輸入來搜尋字詞 (只要其輸入內容不是 URL 即可)。

您可以啟用其餘的預設搜尋原則，以指定要使用的預設搜尋提供者。 如果保留空白 (未設定) 或設定不正確，則使用者可以選擇預設提供者。

如果停用此原則，則使用者無法從網址列搜尋。

如果啟用或停用此原則，則使用者無法變更或覆寫它。

如果未設定此原則，則會啟用預設搜尋提供者，且使用者可以選擇預設搜尋提供者，並設定搜尋提供者清單。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderEnabled
  - GP 名稱：啟用預設搜尋提供者
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderEncodings
  #### 預設搜尋提供者編碼
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定的搜尋提供者所支援的字元編碼方式。 編碼是字碼頁名稱，如 UTF-8、GB2312 和 ISO-8859-1。 這些編碼會按提供的順序進行嘗試。

此原則是選擇性的。 如果未設定，則使用預設值 UTF-8。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderEncodings
  - GP 名稱：預設搜尋提供者編碼
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended\DefaultSearchProviderEncodings
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\1 = UTF-8
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\2 = UTF-16
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\3 = GB2312
SOFTWARE\Policies\Microsoft\Edge\DefaultSearchProviderEncodings\4 = ISO-8859-1

```


  #### Mac 資訊和設定
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

  ### DefaultSearchProviderImageURL
  #### 指定預設搜尋提供者的影像搜尋功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要用於影像搜尋的搜尋引擎 URL。 搜尋要求會使用 GET 方法傳送。

此原則是選擇性的。 如果未設定，則影像搜尋無法使用。

將 Bing 的影像搜尋 URL 指定為：'{bing:baseURL}images/detail/search?iss=sbiupload&FORM=ANCMS1#enterInsights'。

將 Google 的影像搜尋 URL 指定為：'{google:baseURL}searchbyimage/upload'。

請參閱 [DefaultSearchProviderImageURLPostParams](#defaultsearchproviderimageurlpostparams) 原則，以完成影像搜尋的設定。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderImageURL
  - GP 名稱：指定預設搜尋提供者的影像搜尋功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderImageURL
  - 值類型：REG_SZ
  ##### 範例值：
```
https://search.contoso.com/searchbyimage/upload
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderImageURL
  - 範例值：
``` xml
<string>https://search.contoso.com/searchbyimage/upload</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderImageURLPostParams
  #### 使用 POST 的影像 URL 參數
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  如果啟用此原則，則會指定執行使用 POST 的影像搜尋時使用的參數。 原則是由以逗號分隔的名稱/值對組成。 如果值為範本參數，像是前述範例中的 {imageThumbnail}，則會被實際影像縮圖資料所取代。 僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

將 Bing 的影像搜尋 URL Post 參數指定為：'imageBin={google:imageThumbnailBase64}'。

將 Google 的影像搜尋 URL Post 參數指定為：'encoded_image={google:imageThumbnail},image_url={google:imageURL},sbisrc={google:imageSearchSource},original_width={google:imageOriginalWidth},original_height={google:imageOriginalHeight}'。

如果您未設定此原則，則會使用 GET 方式傳送影像搜尋要求。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderImageURLPostParams
  - GP 名稱：使用 POST 的影像 URL 參數
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderImageURLPostParams
  - 值類型：REG_SZ
  ##### 範例值：
```
content={imageThumbnail},url={imageURL},sbisrc={SearchSource}
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderImageURLPostParams
  - 範例值：
``` xml
<string>content={imageThumbnail},url={imageURL},sbisrc={SearchSource}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderKeyword
  #### 預設搜尋提供者關鍵字
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定關鍵字，這是在網址列中用來觸發此提供者的搜尋的捷徑。

此原則是選擇性的。 如果未設定，則任何關鍵字都無法啟動搜尋提供者。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderKeyword
  - GP 名稱：預設搜尋提供者關鍵字
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderKeyword
  - 值類型：REG_SZ
  ##### 範例值：
```
mis
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderKeyword
  - 範例值：
``` xml
<string>mis</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderName
  #### 預設搜尋提供者名稱
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定預設搜尋提供者的名稱。

如果啟用此原則，則您可以設定預設搜尋提供者的名稱。

如果未啟用此原則，或如果將它保留為空白，則會使用由搜尋 URL 指定的主機名稱。

'DefaultSearchProviderName' 應設定為與 DTBC-0008 中設定的加密搜尋提供者對應、組織核准的加密搜尋提供者。 僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderName
  - GP 名稱：預設搜尋提供者名稱
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderName
  - 值類型：REG_SZ
  ##### 範例值：
```
My Intranet Search
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderName
  - 範例值：
``` xml
<string>My Intranet Search</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderSearchURL
  #### 預設搜尋提供者搜尋 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要用於預設搜尋的搜尋引擎 URL。 URL 包含字串 '{searchTerms}'，它會在查詢時以使用者搜尋的字詞取代。

將 Bing 的搜尋 URL 指定為：

'{bing:baseURL}search?q={searchTerms}'。

將 Google 的搜尋 URL 指定為：'{google:baseURL}search?q={searchTerms}&{google:RLZ}{google:originalQueryForSuggestion}{google:assistedQueryStats}{google:searchFieldtrialParameter}{google:searchClient}{google:sourceId}ie={inputEncoding}'。

啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 原則時，需要此原則；如果未啟用前項原則，則會忽略此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderSearchURL
  - GP 名稱：預設搜尋提供者搜尋 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderSearchURL
  - 值類型：REG_SZ
  ##### 範例值：
```
https://search.contoso.com/search?q={searchTerms}
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderSearchURL
  - 範例值：
``` xml
<string>https://search.contoso.com/search?q={searchTerms}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderSuggestURL
  #### 預設建議的搜尋提供者 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定用來提供搜尋建議之搜尋引擎的 URL。 URL 包含字串 '{searchTerms}'，它會在查詢時以使用者目前輸入的文字取代。

此原則是選擇性的。 如果未設定，則使用者不會看到搜尋建議；他們會看到來自瀏覽歷程記錄和我的最愛的建議。

Bing 的建議 URL 可以指定為：

'{bing:baseURL}qbox?query={searchTerms}'。

Google 的建議 URL 可指定為：'{google:baseURL}complete/search?output=chrome&q={searchTerms}'。

僅在啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則時，才會套用此原則。

從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則。 如果使用者已設定預設搜尋提供者，由這個建議原則設定的預設搜尋提供者就不會新增到可讓使用者選擇的搜尋提供者清單中。 如果這是您想要的行為，請使用 [ManagedSearchEngines](#managedsearchengines) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderSuggestURL
  - GP 名稱：預設建議的搜尋提供者 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DefaultSearchProviderSuggestURL
  - 值類型：REG_SZ
  ##### 範例值：
```
https://search.contoso.com/suggest?q={searchTerms}
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderSuggestURL
  - 範例值：
``` xml
<string>https://search.contoso.com/suggest?q={searchTerms}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageSearchBox
  #### 設定新的索引標籤頁面搜尋體驗
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageSearchBox
  - GP 名稱：設定新的索引標籤頁面搜尋體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/預設搜尋提供者
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/預設搜尋提供者
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageSearchBox
  - 值類型：REG_SZ
  ##### 範例值：
```
bing
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPageSearchBox
  - 範例值：
``` xml
<string>bing</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 擴充功能原則

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionAllowedTypes
  #### 設定允許的擴充功能類型
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制可以安裝的擴充功能類型，並限制執行階段存取。

此設定會定義允許的擴充功能類型，以及其可以與哪些主機進行互動。 該值是字串清單，其中的每個應該為下列其中一項："extension"、"theme"、"user_script" 和 "hosted_app"。 如需有關這些類型的詳細資訊，請參閱 Microsoft Edge 擴充功能文件。

請注意，此原則也會影響使用 [ExtensionInstallForcelist](#extensioninstallforcelist) 原則強制安裝的擴充功能。

如果啟用此原則，則只會安裝符合清單中類型的擴充功能。

如果未設定此原則，則對強制執行的可接受擴充功能類型沒有限制。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionAllowedTypes
  - GP 名稱：設定允許的擴充功能類型
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionAllowedTypes\1 = hosted_app

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExtensionAllowedTypes
  - 範例值：
``` xml
<array>
  <string>hosted_app</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionInstallAllowlist
  #### 允許安裝特定擴充功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  預設會允許所有擴充功能。 不過，如果您將 'ExtensionInstallBlockList' 原則設定為 "*" 以封鎖所有擴充功能，則使用者只能安裝此原則中定義的擴充功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionInstallAllowlist
  - GP 名稱：允許安裝特定擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\1 = extension_id1
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallAllowlist\2 = extension_id2

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExtensionInstallAllowlist
  - 範例值：
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionInstallBlocklist
  #### 控制不能安裝哪些擴充功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  列出使用者「無法」在 Microsoft Edge 中安裝的特定擴充功能。 部署此原則時，此清單上先前安裝的任何擴充功能都將停用，而且使用者將無法啟用它們。 如果您從封鎖的擴充功能清單中移除某個項目，則會在先前安裝該擴充功能的任何位置自動重新啟用它。

使用 "*" 可封鎖未在允許清單中明確列出的所有擴充功能。

如果未設定此原則，則使用者可以在 Microsoft Edge 中安裝任何擴充功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionInstallBlocklist
  - GP 名稱：控制不能安裝哪些擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\1 = extension_id1
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallBlocklist\2 = extension_id2

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExtensionInstallBlocklist
  - 範例值：
``` xml
<array>
  <string>extension_id1</string>
  <string>extension_id2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionInstallForcelist
  #### 控制哪些擴充功能會以無訊息方式安裝
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定以無訊息方式安裝、不需使用者互動且使用者無法解除安裝或停用 (「強制安裝」) 的擴充功能。 擴充功能所要求的權限都是隱含授與，無需使用者互動，包括未來版本的擴充功能所要求的任何額外權限。 此外，還會針對 enterprise.deviceAttributes 和 enterprise.platformKeys 擴充功能 API 授與權限。 (這兩個 API 僅適用強制安裝的擴充功能。)

此原則優先於可能會衝突的 [ExtensionInstallBlocklist](#extensioninstallblocklist) 原則。 將擴充功能從強制安裝清單中去除，Microsoft Edge 會自動將其解除安裝。

對於未加入 Microsoft Active Directory 網域的 Windows 裝置，強制安裝僅限於 Microsoft Store 中提供的擴充功能。

請注意，使用者可以使用開發人員工具來修改任何擴充功能的原始程式碼，而這可能會使得擴充功能的功能失常。 如果這是問題，請設定 [DeveloperToolsAvailability](#developertoolsavailability) 原則。

使用下列格式將擴充功能新增至清單：

[extensionID];[updateURL]

- extensionID - 在開發人員模式中，可於 edge://extensions 中找到的 32 個字母字串。

- updateURL (選用) 是應用程式或擴充功能的更新資訊清單 XML 文件位址，如 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) 中所述。 如果您想要從 Chrome 線上應用程式 Microsoft Store 安裝擴充功能，請提供 Chrome 線上應用程式 Microsoft Store 的更新 URL https://clients2.google.com/service/update2/crx。 請注意，此原則中設定的更新 URL 只適用於初始安裝；擴充功能的後續更新會使用在擴充功能資訊清單中指出的更新 URL。 如果您沒有設定 updateURL，系統會假定此擴充功能是存放在 Microsoft Store，並使用下列的更新 URL (https://edge.microsoft.com/extensionwebstorebase/v1/crx)。

例如，gggmmkjegpiggikcnhidnjjhmicpibll;https://edge.microsoft.com/extensionwebstorebase/v1/crx 會透過 Microsoft Store "update" URL 安裝 Microsoft Online 應用程式。 如需有關裝載擴充功能的詳細資訊，請參閱：[https://go.microsoft.com/fwlink/?linkid=2095044](https://go.microsoft.com/fwlink/?linkid=2095044)。

如果未設定此原則，則不會自動安裝任何擴充功能，且使用者可以在 Microsoft Edge 中解除安裝任何擴充功能。

請注意，此原則不適用 InPrivate 模式。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionInstallForcelist
  - GP 名稱：控制哪些擴充功能會以無訊息方式安裝
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\1 = gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallForcelist\2 = abcdefghijklmnopabcdefghijklmnop

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExtensionInstallForcelist
  - 範例值：
``` xml
<array>
  <string>gbchcmhmhahfdphkhkmpfmihenigjmpp;https://edge.microsoft.com/extensionwebstorebase/v1/crx</string>
  <string>abcdefghijklmnopabcdefghijklmnop</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionInstallSources
  #### 設定擴充功能與使用者指令碼安裝來源
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  定義可安裝擴充功能和主題的 URL。

依預設，使用者必須針對要安裝的每個擴充功能或指令碼下載 *.crx 檔案，然後將它拖曳到 Microsoft Edge 設定頁面。 此原則可讓特定 URL 為使用者安裝擴充功能或指令碼。

此清單中的每個項目都是擴充功能式比對模式 (請參閱 [https://go.microsoft.com/fwlink/?linkid=2095039](https://go.microsoft.com/fwlink/?linkid=2095039))。 使用者可以從符合此清單中項目的任何 URL 輕鬆安裝項目。 這些模式必須同時允許 *.crx 檔案的位置，以及開始下載網頁的位置 (也就是查閱者)。

[ExtensionInstallBlocklist](#extensioninstallblocklist) 原則優先於此原則。 不會安裝封鎖清單上的任何擴充功能，即使它來自此清單上的網站。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionInstallSources
  - GP 名稱：設定擴充功能與使用者指令碼安裝來源
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExtensionInstallSources\1 = https://corp.contoso.com/*

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExtensionInstallSources
  - 範例值：
``` xml
<array>
  <string>https://corp.contoso.com/*</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExtensionSettings
  #### 設定擴充功能管理設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 的擴充功能管理設定。

此原則可控制多個設定，包括由任何現有擴充功能相關原則所控制的設定。 此原則會覆寫任何舊版原則 (如果同時設定)。

此原則會將擴充功能識別碼或更新 URL 與其設定對應。 利用擴充功能識別碼，設定只會套用至指定的擴充功能。 設定特殊識別碼 "*" 的預設設定，以將它套用至此原則中未特別列出的所有擴充功能。 利用更新 URL，設定會套用至具有此擴充功能的資訊清單中陳述的確切更新 URL 的所有擴充功能，如 [https://go.microsoft.com/fwlink/?linkid=2095043](https://go.microsoft.com/fwlink/?linkid=2095043) 中所述。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExtensionSettings
  - GP 名稱：設定擴充功能管理設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/擴充功能
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExtensionSettings
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ## HTTP 驗證原則

  [回到頁首](#microsoft-edge---policies)

  ### AllowCrossOriginAuthPrompt
  #### 允許跨原始來源 HTTP 基本驗證提示
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制頁面上的協力廠商子內容是否能夠開啟 [HTTP 基本驗證] 對話方塊。

通常，這會因為網路釣魚防禦而將它停用。 如果未設定此原則，則會停用此原則，且協力廠商子內容無法開啟 [HTTP 基本驗證] 對話方塊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowCrossOriginAuthPrompt
  - GP 名稱：允許跨原始來源 HTTP 基本驗證提示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowCrossOriginAuthPrompt
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowCrossOriginAuthPrompt
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AuthNegotiateDelegateAllowlist
  #### 指定 Microsoft Edge 可以委派使用者認證的伺服器清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 可以委派的伺服器清單。

使用逗號分隔多個伺服器名稱。 允許使用萬用字元 (*)。

如果未設定此原則，Microsoft Edge 將不會委派使用者認證，即使將伺服器偵測為內部網路亦然。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AuthNegotiateDelegateAllowlist
  - GP 名稱：指定 Microsoft Edge 可以委派使用者認證的伺服器清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthNegotiateDelegateAllowlist
  - 值類型：REG_SZ
  ##### 範例值：
```
contoso.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AuthNegotiateDelegateAllowlist
  - 範例值：
``` xml
<string>contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AuthSchemes
  #### 支援的驗證配置
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定支援的 HTTP 驗證配置。

您可以使用這些值來設定原則：'basic'、'digest'、'ntlm' 和 'negotiate'。 使用逗號分隔多個值。

如果未設定此原則，則會使用所有四個配置。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AuthSchemes
  - GP 名稱：支援的驗證配置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthSchemes
  - 值類型：REG_SZ
  ##### 範例值：
```
basic,digest,ntlm,negotiate
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AuthSchemes
  - 範例值：
``` xml
<string>basic,digest,ntlm,negotiate</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AuthServerAllowlist
  #### 設定允許驗證伺服器的清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要啟用整合式驗證的伺服器。 只有在 Microsoft Edge 收到來自 Proxy 或此清單中伺服器的驗證挑戰時，才會啟用整合式驗證。

使用逗號分隔多個伺服器名稱。 允許使用萬用字元 (*)。

如果未設定此原則，則 Microsoft Edge 會嘗試偵測伺服器是否在內部網路上，並在這麼做之後才會回應 IWA 要求。 如果伺服器在網際網路上，則 Microsoft Edge 會忽略來自該伺服器的 IWA 要求。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AuthServerAllowlist
  - GP 名稱：設定允許驗證伺服器的清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AuthServerAllowlist
  - 值類型：REG_SZ
  ##### 範例值：
```
*contoso.com,contoso.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AuthServerAllowlist
  - 範例值：
``` xml
<string>*contoso.com,contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DisableAuthNegotiateCnameLookup
  #### 當協調 Kerberos 驗證時停用 CNAME 查閱
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  決定產生的 Kerberos SPN 是根據一般 DNS 名稱 (CNAME) 或是輸入的原始名稱。

如果啟用此原則，則會略過 CNAME 查閱，並使用伺服器名稱 (如輸入的內容)。

如果停用或未設定此原則，則會使用伺服器的正式名稱。  這是透過 CNAME 查閱決定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DisableAuthNegotiateCnameLookup
  - GP 名稱：當協調 Kerberos 驗證時停用 CNAME 查閱
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DisableAuthNegotiateCnameLookup
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DisableAuthNegotiateCnameLookup
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnableAuthNegotiatePort
  #### Kerberos SPN 中包含非標準連接埠
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定產生的 Kerberos SPN 是否應包含非標準連接埠。

如果啟用此原則，且使用者在 URL 中包含非標準連接埠 (80 或 443 以外的連接埠)，則該連接埠會包含在產生的 Kerberos SPN 中。

如果未設定或停用此原則，則在任何情況下，產生的 Kerberos SPN 將不會包含連接埠。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableAuthNegotiatePort
  - GP 名稱：Kerberos SPN 中包含非標準連接埠
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/HTTP 驗證
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableAuthNegotiatePort
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableAuthNegotiatePort
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NtlmV2Enabled
  #### 控制是否要啟用 NTLMv2 驗證
  
  
  #### 支援的版本：
  - macOS 上，版本 77 或更新版本

  #### 說明
  控制是否已啟用 NTLMv2。

所有新版的 Samba 和 Windows 伺服器均支援 NTLMv2。 您僅應為了解決回溯相容性問題而停用 NTLMv2，因為這會降低驗證的安全性。

如果未設定此原則，則預設會啟用 NTLMv2。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  

  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NtlmV2Enabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 原生訊息原則

  [回到頁首](#microsoft-edge---policies)

  ### NativeMessagingAllowlist
  #### 控制使用者可以使用的原生訊息主機
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  列出使用者可在 Microsoft Edge 中使用的特定原生訊息主機。

預設會允許所有原生訊息主機。 如果將 [NativeMessagingBlocklist](#nativemessagingblocklist) 原則設定為 *，則會封鎖所有原生訊息主機，且只會載入此處所列的原生訊息主機。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NativeMessagingAllowlist
  - GP 名稱：控制使用者可以使用的原生訊息主機
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\1 = com.native.messaging.host.name1
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingAllowlist\2 = com.native.messaging.host.name2

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NativeMessagingAllowlist
  - 範例值：
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NativeMessagingBlocklist
  #### 設定原生訊息封鎖清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定不應使用的原生訊息主機。

使用 "*" 以封鎖所有原生訊息主機，除非它們明確列在允許清單中。

如果未設定此原則，則 Microsoft Edge 會載入所有安裝的原生訊息主機。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NativeMessagingBlocklist
  - GP 名稱：設定原生訊息封鎖清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\1 = com.native.messaging.host.name1
SOFTWARE\Policies\Microsoft\Edge\NativeMessagingBlocklist\2 = com.native.messaging.host.name2

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NativeMessagingBlocklist
  - 範例值：
``` xml
<array>
  <string>com.native.messaging.host.name1</string>
  <string>com.native.messaging.host.name2</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NativeMessagingUserLevelHosts
  #### 允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用原生訊息主機的使用者層級安裝。

如果停用此原則，則 Microsoft Edge 只會使用在系統層級上安裝的原生訊息主機。

如果未設定此原則，依預設，Microsoft Edge 將允許使用使用者層級的原生訊息主機。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NativeMessagingUserLevelHosts
  - GP 名稱：允許使用者層級原生訊息主機 (安裝時不需要系統管理員權限)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/原生訊息
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NativeMessagingUserLevelHosts
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NativeMessagingUserLevelHosts
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 密碼管理員和保護原則

  [回到頁首](#microsoft-edge---policies)

  ### PasswordManagerEnabled
  #### 啟用將密碼儲存到密碼管理員
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓 Microsoft Edge 可儲存使用者密碼。

如果啟用此原則，則使用者可以將其密碼儲存在 Microsoft Edge 中。 使用者下次瀏覽網站時，Microsoft Edge 即會自動輸入密碼。

如果停用此原則，則使用者無法儲存新的密碼，但仍然可以使用先前儲存的密碼。

如果啟用或停用此原則，則使用者無法在 Microsoft Edge 中變更或覆寫它。 如果未設定，則使用者可以儲存密碼，並關閉此功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PasswordManagerEnabled
  - GP 名稱：啟用將密碼儲存到密碼管理員
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/密碼管理員和防護
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PasswordManagerEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PasswordManagerEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PasswordMonitorAllowed
  #### 允許使用者在密碼不安全時收到警示提醒
  
  
  #### 支援的版本：
  - Windows 上，版本 85 或更新版本

  #### 說明
  允許 Microsoft Edge 監管使用者密碼。

如果您啟用此項原則，且提供使用者同意書啟用此原則，如果任何儲存在 Microsoft Edge 中的密碼出現不安全的情形，使用者會收到警示。 Microsoft Edge 會顯示警示訊息，而此資訊也可在 [設定] > [密碼] > [密碼監視器] 中取得。

如果您停用這項原則，啟用此功能與否可不須詢問使用者的同意。 使用者的密碼不會被掃瞄，使用者也不會收到警示訊息。

如果您啟用或未設定原則，使用者可以選擇將此功能開啟或關閉。

若要深入瞭解 Microsoft Edge 如何發現密碼不安全，請參閱 [https://go.microsoft.com/fwlink/?linkid=2133833](https://go.microsoft.com/fwlink/?linkid=2133833)

其他指導方針：

您可以將此原則同時設為建議性使用和強制性使用，但必須使用重要標註。

強制性啟用：因個人使用者同意是為特定使用者啟用此功能的預先條件，所以此原則沒有強制執行的設定。 如果將此原則設定為 [強制性啟用]，則不須變更 [設定] 中的 UI，且下列的錯誤訊息會顯示在 edge://policy。

錯誤狀態訊息範例：「忽略此原則值是因為密碼監控器須有個人使用者的同意才能開啟。 您可以要求貴組織的使用者至設定 > 設定檔 > 密碼，然後開啟此功能。」

建議性啟用：假如將此原則設為建議性使用，在設定中的 UI 即會維持在 ‘關閉’ 的狀態．但在其旁邊會顯示一個公事包的圖示，在暫留懸停時會有以下說明顯示 -「您的組織建議使用此設定適用的特定值，而您選擇了一個不同的值」

已停用強制性使用和建議性使用：這兩種狀態都能正常運作，且使用者可以看到常用的標題。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PasswordMonitorAllowed
  - GP 名稱：允許使用者在密碼不安全時收到警示提醒
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/密碼管理員和防護
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PasswordMonitorAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  
  
   
 
 
   
  

  [回到頁首](#microsoft-edge---policies)

  ### PasswordProtectionChangePasswordURL
  #### 設定變更密碼 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定變更密碼 URL (僅限 HTTP 和 HTTPS 配置)。

在瀏覽器中看到警告之後，密碼保護服務會將使用者傳送到此 URL 以變更其密碼。

如果啟用此原則，則密碼保護服務會將使用者傳送到此 URL 來變更其密碼。

如果停用或未設定此原則，則密碼保護服務不會將使用者重新導向至變更密碼 URL。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PasswordProtectionChangePasswordURL
  - GP 名稱：設定變更密碼 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PasswordProtectionChangePasswordURL
  - 值類型：REG_SZ
  ##### 範例值：
```
https://contoso.com/change_password.html
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PasswordProtectionChangePasswordURL
  - 範例值：
``` xml
<string>https://contoso.com/change_password.html</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PasswordProtectionLoginURLs
  #### 設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定企業登入 URL 的清單 (僅限 HTTP 和 HTTPS 配置)，Microsoft Edge 應在其中擷取密碼的加料雜湊，並將它用於密碼重複使用偵測。

如果啟用此原則，則密碼保護服務會在定義的 URL 上擷取密碼的指紋。

如果停用或未設定此原則，則不會擷取密碼指紋。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PasswordProtectionLoginURLs
  - GP 名稱：設定密碼保護服務應擷取密碼加料雜湊的企業登入 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\1 = https://contoso.com/login.html
SOFTWARE\Policies\Microsoft\Edge\PasswordProtectionLoginURLs\2 = https://login.contoso.com

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PasswordProtectionLoginURLs
  - 範例值：
``` xml
<array>
  <string>https://contoso.com/login.html</string>
  <string>https://login.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PasswordProtectionWarningTrigger
  #### 設定密碼保護警告觸發程序
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PasswordProtectionWarningTrigger
  - GP 名稱：設定密碼保護警告觸發程序
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/密碼管理員和防護
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PasswordProtectionWarningTrigger
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PasswordProtectionWarningTrigger
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 列印原則

  [回到頁首](#microsoft-edge---policies)

  ### DefaultPrinterSelection
  #### 預設印表機選擇規則
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  覆寫 Microsoft Edge 預設印表機選擇規則。 此原則會決定用於在 Microsoft Edge 中選取預設印表機的規則，這會在使用者第一次嘗試列印頁面時發生。

設定此原則時，Microsoft Edge 會嘗試尋找符合所有指定屬性的印表機，並將它當成預設印表機。 如果有符合條件的多個印表機，則會使用符合的第一個印表機。

如果未設定此原則，或未在逾時內找到相符的印表機，印表機會預設為內建的 PDF 印表機，或無印表機 (如果沒有 PDF 印表機)。

值會剖析為 JSON 物件，符合下列架構：{ "type": "object", "properties": { "idPattern": { "description": "用來比對印表機識別碼的規則運算式。", "type": "string" }, "namePattern": { "description": "用來比對印表機顯示名稱的規則運算式。", "type": "string" } } }

省略某個欄位表示比對所有值；例如，如果您未指定連線，則預覽列印會開始探索各種本機印表機。 規則運算式模式必須遵循 JavaScript RegExp 語法，且比對會區分大小寫。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultPrinterSelection
  - GP 名稱：預設印表機選擇規則
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultPrinterSelection
  - 值類型：REG_SZ
  ##### 範例值：
```
{ "idPattern": ".*public", "namePattern": ".*Color" }
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultPrinterSelection
  - 範例值：
``` xml
<string>{ "idPattern": ".*public", "namePattern": ".*Color" }</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PrintHeaderFooter
  #### 列印頁首與頁尾
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在列印對話方塊中，強制開啟或關閉 [頁首及頁尾]。

如果未設定此原則，則使用者可以決定是否要列印頁首和頁尾。

如果停用此原則，則使用者無法列印頁首及頁尾。

如果啟用此原則，則使用者一律會列印頁首及頁尾。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PrintHeaderFooter
  - GP 名稱：列印頁首及頁尾
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/列印
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PrintHeaderFooter
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PrintHeaderFooter
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PrintPreviewUseSystemDefaultPrinter
  #### 將系統預設的印表機設定為預設印表機
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  告知 Microsoft Edge 使用 [預覽列印] 中的預設印表機，而非最近使用的印表機。

如果停用或未設定此原則，則預覽列印會將最近使用的印表機視為預設的目的地選項。

如果啟用此原則，則預覽列印會使用 OS 的系統預設印表機做為預設目的地選擇。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PrintPreviewUseSystemDefaultPrinter
  - GP 名稱：將系統預設的印表機設定為預設印表機
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/列印
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：PrintPreviewUseSystemDefaultPrinter
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PrintPreviewUseSystemDefaultPrinter
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PrintingEnabled
  #### 啟用列印
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 Microsoft Edge 中啟用列印，並防止使用者變更此設定。

如果啟用此原則或未設定，則使用者可以列印。

如果停用此原則，則使用者無法從 Microsoft Edge 列印。 在扳手功能表、擴充功能、JavaScript 應用程式等項目中會停用列印。 使用者仍可以從列印時會略過 Microsoft Edge 的外掛程式進行列印。 例如，某些 Adobe Flash 應用程式的內容功能表中有列印選項，而此原則並未涵蓋它。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PrintingEnabled
  - GP 名稱：啟用列印
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PrintingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PrintingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### UseSystemPrintDialog
  #### 使用系統列印對話方塊列印
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  顯示系統列印對話方塊，而非預覽列印。

如果啟用此原則，當使用者列印頁面時，Microsoft Edge 會開啟系統的列印對話方塊，而非內建的預覽列印。

如果未設定或停用此原則，則列印命令會觸發 Microsoft Edge 預覽列印畫面。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：UseSystemPrintDialog
  - GP 名稱：使用系統列印對話方塊列印
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/列印
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UseSystemPrintDialog
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：UseSystemPrintDialog
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## Proxy 伺服器原則

  [回到頁首](#microsoft-edge---policies)

  ### ProxyBypassList
  #### 設定 Proxy 許可規則
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  定義 Microsoft Edge 略過任何 Proxy 的主機清單。

只有當您在 [ProxyMode](#proxymode) 原則中選取 [使用固定的 Proxy 伺服器] 時，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則可以建立 Microsoft Edge 不使用 Proxy 的主機清單。

如果未設定此原則，則不會為 Microsoft Edge 略過其 Proxy 的主機建立清單。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需更詳細的範例，請移至 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProxyBypassList
  - GP 名稱：設定 Proxy 許可規則
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProxyBypassList
  - 值類型：REG_SZ
  ##### 範例值：
```
https://www.contoso.com, https://www.fabrikam.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProxyBypassList
  - 範例值：
``` xml
<string>https://www.contoso.com, https://www.fabrikam.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ProxyMode
  #### 設定 Proxy 伺服器設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定 Microsoft Edge 所使用的 Proxy 伺服器設定。 如果啟用此原則，則使用者無法變更 Proxy 設定。

如果選擇一律不使用 Proxy 伺服器且一律直接連線，則會忽略所有其他選項。

如果選擇使用系統 Proxy 設定，則會忽略所有其他選項。

如果選擇自動偵測 Proxy 伺服器，則會忽略所有其他選項。

如果選擇固定伺服器 Proxy 模式，則可以在 [ProxyServer](#proxyserver) 和「逗點分隔的 Proxy 許可規則清單」中指定更多選項。

如果選擇使用 .pac Proxy 指令碼，則必須在 [Proxy .pac 檔案的 URL] 中指定指令碼的 URL。

如需詳細範例，請移至 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

如果啟用此原則，則 Microsoft Edge 會忽略從命令列指定的所有 Proxy 相關選項。

如果未設定此原則，則使用者可以選擇其自己的 Proxy 設定。

原則選項對應：

* ProxyDisabled (direct) = 永遠不使用 Proxy

* ProxyAutoDetect (auto_detect) = 自動偵測 Proxy 設定

* ProxyPacScript (pac_script) = 使用 .pac Proxy 指令碼

* ProxyFixedServers (fixed_servers) = 使用固定的 Proxy 伺服器

* ProxyUseSystem (system) = 使用系統 Proxy 設定

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProxyMode
  - GP 名稱：設定 Proxy 伺服器設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyMode
  - 值類型：REG_SZ
  ##### 範例值：
```
direct
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProxyMode
  - 範例值：
``` xml
<string>direct</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ProxyPacUrl
  #### 設定 Proxy .pac 檔案 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定 Proxy auto-config (PAC) 檔案的 URL。

只有當您在 [ProxyMode](#proxymode) 原則中選取 [使用 .pac Proxy 指令碼] 時，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則可以為 PAC 檔案指定 URL，其定義瀏覽器如何自動選擇用於擷取特定網站的適當 Proxy 伺服器。

如果停用或未設定此原則，則不會指定任何 PAC 檔案。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需詳細範例，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProxyPacUrl
  - GP 名稱：設定 Proxy .pac 檔案 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyPacUrl
  - 值類型：REG_SZ
  ##### 範例值：
```
https://internal.contoso.com/example.pac
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProxyPacUrl
  - 範例值：
``` xml
<string>https://internal.contoso.com/example.pac</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ProxyServer
  #### 設定 Proxy 伺服器的位址或 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定 Proxy 伺服器的 URL。

只有當您在 [ProxyMode](#proxymode) 原則中選取 [使用固定的 Proxy 伺服器] 時，才會套用此原則。 如果已選取用於設定 Proxy 原則的任何其他模式，請勿啟用或設定此原則。

如果啟用此原則，則將對所有 URL 使用此原則設定的 Proxy 伺服器。

如果停用或未設定此原則，則使用者可以在處於此 Proxy 模式時選擇其自己的 Proxy 設定。 如果已指定用於設定 Proxy 原則的任何其他方法，請將此原則保留為未設定。

如需更多選項和詳細範例，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094936](https://go.microsoft.com/fwlink/?linkid=2094936)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProxyServer
  - GP 名稱：設定 Proxy 伺服器的位址或 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱︰ProxyServer
  - 值類型：REG_SZ
  ##### 範例值：
```
123.123.123.123:8080
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProxyServer
  - 範例值：
``` xml
<string>123.123.123.123:8080</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ProxySettings
  #### Proxy 設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 的 Proxy 設定。

如果啟用此原則，則 Microsoft Edge 會忽略從命令列指定的所有 Proxy 相關選項。

如果未設定此原則，則使用者可以選擇其自己的 Proxy 設定。

此原則會覆寫下列個別原則：

[ProxyMode](#proxymode)
[ProxyPacUrl](#proxypacurl)
[ProxyServer](#proxyserver)
[ProxyBypassList](#proxybypasslist)

ProxyMode 欄位可讓您指定 Microsoft Edge 所使用的 Proxy 伺服器，並防止使用者變更 Proxy 設定。

ProxyPacUrl 欄位是 Proxy .pac 檔案的 URL。

ProxyServer 欄位是 Proxy 伺服器的 URL。

ProxyBypassList 欄位是 Microsoft Edge 略過的 Proxy 主機清單。

如果選擇 'direct' 值做為 'ProxyMode'，則永遠不會使用 Proxy，並忽略所有其他欄位。

如果選擇 'system' 值做為 'ProxyMode'，則會使用系統的 Proxy，並忽略所有其他欄位。

如果選擇 'auto_detect' 值做為 'ProxyMode'，則會忽略所有其他欄位。

如果選擇 'fixed_server' 值做為 'ProxyMode'，則會使用 'ProxyServer' 和 'ProxyBypassList' 欄位。

如果選擇 'pac_script' 值做為 'ProxyMode'，則會使用 'ProxyPacUrl' 和 'ProxyBypassList' 欄位。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProxySettings
  - GP 名稱：Proxy 設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/Proxy 伺服器
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProxySettings
  - 值類型：REG_SZ
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ProxySettings = {
  "ProxyBypassList": "https://www.example1.com,https://www.example2.com,https://internalsite/", 
  "ProxyMode": "direct", 
  "ProxyPacUrl": "https://internal.site/example.pac", 
  "ProxyServer": "123.123.123.123:8080"
}
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProxySettings
  - 範例值：
``` xml
<key>ProxySettings</key>
<dict>
  <key>ProxyBypassList</key>
  <string>https://www.example1.com,https://www.example2.com,https://internalsite/</string>
  <key>ProxyMode</key>
  <string>direct</string>
  <key>ProxyPacUrl</key>
  <string>https://internal.site/example.pac</string>
  <key>ProxyServer</key>
  <string>123.123.123.123:8080</string>
</dict>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## SmartScreen 設定原則

  [回到頁首](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverride
  #### 防止略過網站的 Microsoft Defender SmartScreen 提示
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  此原則設定可讓您決定使用者是否可覆寫有關潛在惡意網站的 Microsoft Defender SmartScreen 警告。

如果啟用此設定，使用者就不能忽略 Microsoft Defender SmartScreen 警告，並且會封鎖使用者，使其無法繼續瀏覽網站。

如果停用或未設定此設定，則使用者可以忽略 Microsoft Defender SmartScreen 警告，並繼續瀏覽網站。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PreventSmartScreenPromptOverride
  - GP 名稱：防止略過網站的 Microsoft Defender SmartScreen 提示
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PreventSmartScreenPromptOverride
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PreventSmartScreenPromptOverride
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PreventSmartScreenPromptOverrideForFiles
  #### 防止略過關於下載項目的 Microsoft Defender SmartScreen 警告
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本
  - macOS 上，版本 79 或更新版本

  #### 說明
  此原則可讓您判斷使用者是否可以覆寫關於未經驗證下載的 Microsoft Defender SmartScreen 警告。

如果啟用此原則，則組織中的使用者無法忽略 Microsoft Defender SmartScreen 警告，且會防止其完成未經驗證的下載。

如果停用或未設定此原則，則使用者可以忽略 Microsoft Defender SmartScreen 警告，並完成未驗證的下載。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PreventSmartScreenPromptOverrideForFiles
  - GP 名稱：防止略過關於下載項目的 Microsoft Defender SmartScreen 警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PreventSmartScreenPromptOverrideForFiles
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PreventSmartScreenPromptOverrideForFiles
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SmartScreenAllowListDomains
  #### 設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Defender SmartScreen 的信任網域清單。 這表示，如果來源 URL 符合這些網域，則 Microsoft Defender SmartScreen 不會檢查是否有潛在的惡意資源，例如網路釣魚軟體和其他惡意程式碼。
Microsoft Defender SmartScreen 下載保護服務不會檢查在這些網域上託管的下載。

如果啟用此原則，則 Microsoft Defender SmartScreen 會信任這些網域。
如果停用或未設定此原則，則會將預設的 Microsoft Defender SmartScreen 防護套用到所有資源。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。
另請注意，如果組織已啟用 Microsoft Defender 進階威脅防護，則此原則不適用。 您必須改為在 Microsoft Defender 資訊安全中心設定允許和封鎖清單。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SmartScreenAllowListDomains
  - GP 名稱：設定 Microsoft Defender SmartScreen 篩選工具將不會觸發警告的網域清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\1 = mydomain.com
SOFTWARE\Policies\Microsoft\Edge\SmartScreenAllowListDomains\2 = myuniversity.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SmartScreenAllowListDomains
  - 範例值：
``` xml
<array>
  <string>mydomain.com</string>
  <string>myuniversity.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SmartScreenEnabled
  #### 設定 Microsoft Defender SmartScreen
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  此原則設定可讓您設定是否要開啟 Microsoft Defender SmartScreen。 Microsoft Defender SmartScreen 提供警告訊息，以協助保護使用者免於遭受潛在網路釣魚詐騙和惡意軟體。 預設會開啟 Microsoft Defender SmartScreen。

如果啟用此設定，則會開啟 Microsoft Defender SmartScreen。

如果停用此設定，則會關閉 Microsoft Defender SmartScreen。

如果未設定此設定，則使用者可以選擇是否要使用 Microsoft Defender SmartScreen。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SmartScreenEnabled
  - GP 名稱：設定 Microsoft Defender SmartScreen
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SmartScreenEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SmartScreenForTrustedDownloadsEnabled
  #### 強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  此原則設定可讓您設定 Microsoft Defender SmartScreen 是否檢查來自信任來源的下載信譽。

如果您啟用或未設定此設定，無論來源為何，Microsoft Defender SmartScreen 都會檢查下載項目的信譽。

如果您停用此設定，Microsoft Defender SmartScreen 不會檢查從信任來源下載項目的信譽。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SmartScreenForTrustedDownloadsEnabled
  - GP 名稱：強制 Microsoft Defender SmartScreen 檢查來自信任來源的下載項目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenForTrustedDownloadsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### SmartScreenPuaEnabled
  #### 設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  此原則設定可讓您設定是否要開啟封鎖潛在的垃圾應用程式以搭配 Microsoft Defender SmartScreen。 潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen 可提供警告訊息，以協助保護使用者不受廣告軟體、挖礦程式、置入軟體和其他由網站託管的低信譽應用程式。 預設會關閉潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果啟用此設定，則會開啟潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果停用此設定，則會關閉潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

如果未設定此設定，則使用者可以選擇是否要使用潛在的垃圾應用程式封鎖搭配 Microsoft Defender SmartScreen。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SmartScreenPuaEnabled
  - GP 名稱：設定 Microsoft Defender SmartScreen 以封鎖潛在的垃圾應用程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/SmartScreen 設定
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/SmartScreen 設定
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SmartScreenPuaEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SmartScreenPuaEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 啟動、首頁和新的索引標籤頁面原則

  [回到頁首](#microsoft-edge---policies)

  ### HomepageIsNewTabPage
  #### 將新的索引標籤頁面設定為 [首頁]
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 中的預設首頁。 您可以將首頁設定為您指定的 URL 或新的索引標籤頁面。

如果啟用此原則，則一律對首頁使用新的索引標籤頁面，且會忽略首頁 URL 位置。

如果停用此原則，除非 URL 設為 'edge://newtab'，否則使用者的首頁不會成為新的索引標籤頁面。

如果未設定，則使用者可以選擇新的索引標籤頁面是否為其首頁。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：HomepageIsNewTabPage
  - GP 名稱：將新的索引標籤頁面設定為 [首頁]
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：HomepageIsNewTabPage
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：HomepageIsNewTabPage
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### HomepageLocation
  #### 設定首頁 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 中的預設首頁 URL。

首頁是由 [首頁] 按鈕所開啟的頁面。 啟動時開啟的頁面是由 [RestoreOnStartup](#restoreonstartup) 原則所控制。

您可以在此設定 URL，或將首頁設定為開啟新的索引標籤頁面。 如果選擇開啟新的索引標籤頁面，則此原則不會有作用。

如果啟用此原則，則使用者無法變更其首頁 URL，但可以選擇使用新的索引標籤頁面做為首頁。

如果停用或未設定此原則，則使用者可以自行選擇其首頁，只要 [HomepageIsNewTabPage](#homepageisnewtabpage) 原則未啟用即可。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：HomepageLocation
  - GP 名稱：設定首頁 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：HomepageLocation
  - 值類型：REG_SZ
  ##### 範例值：
```
https://www.contoso.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：HomepageLocation
  - 範例值：
``` xml
<string>https://www.contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageAllowedBackgroundTypes
  #### 設定新索引標籤頁面版面配置所允許的背景類型
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  您可以在 Microsoft Edge 中設定新索引標籤頁面版面配置所允許的背景影像類型。

如果您未設定此原則，則會啟用新索引標籤頁面上的所有背景影像類型。

                                           

                                            

                                          

原則選項對應：

* DisableImageOfTheDay (1) = 停用每日背景影像類型

* DisableCustomImage (2) = 停用自訂背景影像類型

* DisableAll (3) = 停用所有背景影像類型

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageAllowedBackgroundTypes
  - GP 名稱：設定新索引標籤頁面配置所允許的背景類型
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：NewTabPageAllowedBackgroundTypes
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPageAllowedBackgroundTypes
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageCompanyLogo
  #### 設定新的索引標籤頁面公司標誌 (已過時)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  此原則已遭取代，是因為它的運作效能不如預期，建議您不要使用此原則。 無法在 Microsoft Edge 版本 86 中使用。

指定要在 Microsoft Edge 中新的索引標籤頁面上使用的公司標誌。

原則應設定為字串，以 JSON 格式表示標誌。 例如：{ "default_logo": { "url": "https://www.contoso.com/logo.png", "hash": "cd0aa9856147b6c5b4ff2b7dfee5da20aa38253099ef1b4a64aced233c9afe29" }, "light_logo": { "url": "https://www.contoso.com/light_logo.png", "hash": "517d286edb416bb2625ccfcba9de78296e90da8e32330d4c9c8275c4c1c33737" } }

您可以設定此原則，方法是指定 Microsoft Edge 可以從中下載標誌的 URL，以及其加密雜湊 (SHA-256)，用來驗證下載的完整性。 標誌必須是 PNG 或 SVG 格式，且其檔案大小不能超過 16 MB。 標誌會下載並快取，每當 URL 或雜湊變更，就會重新下載標誌。 該 URL 必須未經任何驗證便可存取。

需要 'default_logo'，且它將在沒有背景影像時使用。 如果提供了 'light_logo'，則會在使用者新的索引標籤頁面有背景影像時使用。 建議使用具有透明背景的水平標誌 (靠左對齊和垂直置中)。 標誌的最小高度應為 32 像素，而長寬比從 1:1 到4:1。 'default_logo' 應對照白色/黑色背景使用適當的對比，而 'light_logo' 應對照背景影像有適當的對比。

如果啟用此原則，則 Microsoft Edge 會下載並在新的索引標籤頁面上顯示指定的標誌。 使用者無法覆寫或隱藏標誌。

如果停用或未設定此原則，則 Microsoft Edge 不會在新的索引標籤頁面上顯示公司標誌或 Microsoft 標誌。

如需有關判定 SHA-256 雜湊的說明，請參閱 https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/get-filehash。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageCompanyLogo
  - GP 名稱：設定新的索引標籤頁面公司標誌 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NewTabPageCompanyLogo
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ### NewTabPageHideDefaultTopSites
  #### 從新的索引標籤頁面隱藏預設熱門網站
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 Microsoft Edge 中從新的索引標籤頁面隱藏預設熱門網站。

如果您將此原則設定為 true，則會隱藏預設的熱門網站磚。

如果將此原則設定為 false 或未設定，則預設的熱門網站磚會保持顯示。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageHideDefaultTopSites
  - GP 名稱：從新的索引標籤頁面隱藏預設熱門網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NewTabPageHideDefaultTopSites
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPageHideDefaultTopSites
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageLocation
  #### 設定新的索引標籤頁面 URL
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定新的索引標籤頁面的預設 URL。

此原則會決定建立新的索引標籤時開啟的頁面 (包括開啟新視窗時)。 如果啟動頁面已設為開啟新的索引標籤頁面，則也會影響它。

此原則不會判定在啟動時要開啟的頁面；這是由 [RestoreOnStartup](#restoreonstartup) 原則控制。 如果啟動頁面已設為開啟至新的索引標籤，則不會對首頁造成任何影響。

如果未設定此原則，則會使用預設的新的索引標籤頁面。

如果您設定此原則*以及* [NewTabPageSetFeedType](#newtabpagesetfeedtype) 原則，則此原則優先。

如果提供的 URL 無效，新的索引標籤會開啟 about://blank。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageLocation
  - GP 名稱：設定新的索引標籤頁面 URL
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageLocation
  - 值類型：REG_SZ
  ##### 範例值：
```
https://www.fabrikam.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPageLocation
  - 範例值：
``` xml
<string>https://www.fabrikam.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageManagedQuickLinks
  #### 設定新的索引標籤頁面快速連結
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  依預設，Microsoft Edge 會根據瀏覽歷程記錄，在新的索引標籤頁面上顯示來自使用者新增的捷徑和熱門網站的快速連結。 使用此原則，您可以在新的索引標籤頁面上設定最多三個快速連結磚，並以 JSON 物件表示：

[ { "url": "https://www.contoso.com", "title": "Contoso Portal", "pinned": true/false }, ... ]

'url' 欄位為必要欄位。'title' 和 'pinned' 為選用。 如果未提供 'title'，則會將 URL 用作預設標題。 如果未提供 'pinned'，則預設值為 false。

Microsoft Edge 會以所列的順序呈現這些項目 (由左至右)，且所有釘選的磚都會顯示在未釘選的磚前方。

如果原則設定為強制，則會忽略 'pinned' 欄位，並將所有磚釘選。 使用者無法刪除磚，且一律會出現在快速連結清單的前面。

如果原則設定為建議，則釘選的磚會保留在清單中，但使用者可以編輯和刪除它們。 未釘選的快速連結磚的行為就如同預設的熱門網站，如果其他網站的造訪頻率較高，則會將該連結推出清單之外。 透過此原則將未釘選的連結套用至現有的瀏覽器設定檔時，連結可能完全不會顯示，取決於它們相較於使用者的瀏覽歷程記錄的排名。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageManagedQuickLinks
  - GP 名稱：設定新的索引標籤頁面快速連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageManagedQuickLinks
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ### NewTabPagePrerenderEnabled
  #### 啟用預先載入的新索引標籤頁面，以加快頁面呈現速度
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  若您設定此原則，將會啟用 [預先載入新增索引標籤頁面] 功能，且使用者無法變更此設定。 若您未設定此原則，將會啟用預先載入功能，且使用者可以變更此設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPagePrerenderEnabled
  - GP 名稱：啟用預先載入的新索引標籤頁面，以加快頁面呈現速度
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPagePrerenderEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPagePrerenderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NewTabPageSetFeedType
  #### 設定 Microsoft Edge 新的索引標籤頁面體驗
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NewTabPageSetFeedType
  - GP 名稱：設定 Microsoft Edge 新的索引標籤頁面體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NewTabPageSetFeedType
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NewTabPageSetFeedType
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RestoreOnStartup
  #### 啟動時所採取的動作
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RestoreOnStartup
  - GP 名稱：啟動時所採取的動作
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：RestoreOnStartup
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000004
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RestoreOnStartup
  - 範例值：
``` xml
<integer>4</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RestoreOnStartupURLs
  #### 瀏覽器啟動時開啟的網站
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定瀏覽器啟動時自動開啟的網站清單。 如果未設定此原則，則啟動時不會開啟任何網站。

只有當您將 [RestoreOnStartup](#restoreonstartup) 原則設定為 [開啟 URL 清單] (4)時，此原則才有效。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RestoreOnStartupURLs
  - GP 名稱：瀏覽器啟動時開啟的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended\RestoreOnStartupURLs
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\1 = https://contoso.com
SOFTWARE\Policies\Microsoft\Edge\RestoreOnStartupURLs\2 = https://www.fabrikam.com

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RestoreOnStartupURLs
  - 範例值：
``` xml
<array>
  <string>https://contoso.com</string>
  <string>https://www.fabrikam.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ShowHomeButton
  #### 在工具列上顯示 [首頁] 按鈕
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 Microsoft Edge 工具列上顯示 [首頁] 按鈕。

啟用此原則以一律顯示 [首頁] 按鈕。 停用它以一律不顯示該按鈕。

如果未設定原則，則使用者可以選擇是否要顯示首頁按鈕。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ShowHomeButton
  - GP 名稱：在工具列上顯示 [首頁] 按鈕
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/啟動、首頁和新的索引標籤頁面
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/啟動、首頁和新的索引標籤頁面
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ShowHomeButton
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ShowHomeButton
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ## 其他原則

  [回到頁首](#microsoft-edge---policies)

  ### AddressBarMicrosoftSearchInBingProviderEnabled
  #### 在網址列中啟用 Bing 專用 Microsoft Search 建議
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  讓您在使用者在網址列中輸入搜尋字串時，於網址列的建議清單中顯示相關的 Bing 專用 Microsoft Search 建議。 如果啟用或未設定此原則，則使用者可以在 Microsoft Edge 網址列建議清單中看到 Bing 專用 Microsoft Search 提供的內部結果。 若要查看 Bing 專用 Microsoft Search 結果，使用者必須使用其用於該組織的 Azure AD 帳戶登入 Microsoft Edge。
如果停用此原則，則使用者無法在 Microsoft Edge 網址列建議清單中查看內部結果。
如果已啟用會強制使用預設搜尋提供者 ([DefaultSearchProviderEnabled](#defaultsearchproviderenabled)、[DefaultSearchProviderName](#defaultsearchprovidername) 和 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl)) 的原則，且所指定的搜尋提供者不是 Bing，則不適用此原則，在網址列的建議清單中也不會有 Bing 專用 Microsoft Search 建議。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - GP 名稱：在網址列中啟用 Bing 專用 Microsoft Search 建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AddressBarMicrosoftSearchInBingProviderEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AdsSettingForIntrusiveAdsSites
  #### 含有干擾廣告網站的廣告設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  控制是否在含有干擾廣告的網站上封鎖廣告。

原則選項對應：

* AllowAds (1) = 在所有網站上允許廣告。

* BlockAds (2) = 在含有侵入式廣告的網站上封鎖廣告。 (預設值)

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AdsSettingForIntrusiveAdsSites
  - GP 名稱：含有干擾廣告網站的廣告設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AdsSettingForIntrusiveAdsSites
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AdsSettingForIntrusiveAdsSites
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowDeletingBrowserHistory
  #### 啟用刪除瀏覽器和下載歷程記錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許刪除瀏覽器歷程記錄和下載歷程記錄，並防止使用者變更此設定。

請注意，即使停用此原則，瀏覽和下載歷程記錄也不保證會保留：使用者可以直接編輯或刪除記錄資料庫檔案，而瀏覽器本身可以隨時移除 (根據到期期間) 或封存任何或所有歷程記錄項目。

如果啟用此原則或未設定，則使用者可以刪除瀏覽和下載歷程記錄。

如果停用此原則，則使用者無法刪除瀏覽和下載歷程記錄。

如果啟用此原則，則請勿啟用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則，因為它們全都涉及刪除資料。 如果您同時啟用這兩項，則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則優先，並且會在 Microsoft Edge 關閉時刪除所有資料，無論此原則的設定方式如何。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowDeletingBrowserHistory
  - GP 名稱：啟用刪除瀏覽器和下載歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowDeletingBrowserHistory
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowDeletingBrowserHistory
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowFileSelectionDialogs
  #### 允許檔案選取項目對話方塊
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓 Microsoft Edge 顯示檔案選取對話方塊，允許存取本機檔案。

如果啟用或未設定此原則，則使用者可以正常開啟檔案選取對話方塊。

如果停用此原則，每當使用者執行會觸發檔案選取對話方塊的動作 (例如匯入我的最愛、上傳檔案或儲存連結)，即會改為顯示訊息，並假設使用者已在 [檔案選取] 對話方塊中按一下 [取消]。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowFileSelectionDialogs
  - GP 名稱：允許檔案選取項目對話方塊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowFileSelectionDialogs
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowFileSelectionDialogs
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowPopupsDuringPageUnload
  #### 允許在卸載網頁期間顯示快顯視窗
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  此原則可讓系統管理員指定網頁可在其卸載期間顯示快顯視窗。

原則設定為已啟用時，則允許在卸載網頁期間顯示快顯視窗。

原則設為已停用或未設定時，則不允許在卸載網頁期間顯示快顯視窗。 這是基於此處的規格：(https://html.spec.whatwg.org/#apis-for-creating-and-navigating-browsing-contexts-by-name)。

此原則未來會移除。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowPopupsDuringPageUnload
  - GP 名稱：允許在卸載網頁期間顯示快顯視窗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowPopupsDuringPageUnload
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowPopupsDuringPageUnload
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowSurfGame
  #### 允許衝浪遊戲
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  如果停用此原則，當裝置離線或使用者瀏覽至 edge://surf 時，使用者將無法玩衝浪遊戲。

如果啟用或未設定此原則，則使用者可以玩衝浪遊戲。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowSurfGame
  - GP 名稱：允許衝浪遊戲
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowSurfGame
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowSurfGame
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowSyncXHRInPageDismissal
  #### 允許頁面在頁面關閉期間傳送同步 XHR 要求 (已淘汰)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與變更不一致，而使頁面關閉期間不允許同步 XHR 要求時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本 88 中使用。

此原則可讓您指定頁面可以在頁面關閉期間傳送同步 XHR 要求。

如果啟用此原則，則頁面可以在頁面關閉期間傳送同步 XHR 要求。

如果停用或未設定此原則，則不允許頁面在頁面關閉期間傳送同步 XHR 要求。

  

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowSyncXHRInPageDismissal
  - GP 名稱：允許頁面在頁面關閉期間傳送同步 XHR 要求 (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AllowSyncXHRInPageDismissal
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowSyncXHRInPageDismissal
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AllowTokenBindingForUrls
  #### 設定 Microsoft Edge 將嘗試建立與 [權杖繫結] 連結的網站清單。
  
  
  #### 支援的版本：
  - Windows 上，版本 83 或更新版本

  #### 說明
  為瀏覽器將嘗試與其執行權杖繫結通訊協定之網站，設定 URL 模式清單。
對於此清單上的網域，瀏覽器將會在 TLS 交握中傳送權杖繫結 ClientHello (請參閱 https://tools.ietf.org/html/rfc8472))。
如果伺服器以有效的 ServerHello 回應回覆，瀏覽器將會在後續的 HTTPS 要求中建立並傳送權杖繫結訊息。 如需詳細資訊，請參閱 https://tools.ietf.org/html/rfc8471。

如果此清單為空白，則會停用權杖繫結。

此原則僅在具備虛擬安全模式功能的 Windows 10 裝置上可用。

從 Microsoft Edge 版本 86 開始，此原則不再支援動態重新整理。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowTokenBindingForUrls
  - GP 名稱：設定 Microsoft Edge 將嘗試建立權杖繫結的網站清單。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\1 = mydomain.com
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\2 = [*.]mydomain2.com
SOFTWARE\Policies\Microsoft\Edge\AllowTokenBindingForUrls\3 = [*.].mydomain2.com

```


  

  [回到頁首](#microsoft-edge---policies)

  ### AllowTrackingForUrls
  #### 設定特定網站的防止追蹤例外
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  設定要從防止追蹤中排除的 URL 模式清單。

如果設定此原則，則會將已設定 URL 模式的清單從防止追蹤中排除。

如果未設定此原則，則會對所有網站使用來自「封鎖使用者的網頁瀏覽活動追蹤」原則 (如有設定) 或使用者個人設定的全域預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AllowTrackingForUrls
  - GP 名稱：設定特定網站的防止追蹤例外
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\AllowTrackingForUrls\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AllowTrackingForUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AlternateErrorPagesEnabled
  #### 當找不到網頁時，推薦類似的頁面
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  允許 Microsoft Edge 向 Web 服務發出連線，以針對連線問題 (例如 DNS 錯誤) 產生 URL 和搜尋建議。

如果啟用此原則，則會使用 Web 服務來產生 URL 並搜尋網路錯誤的建議。

如果停用此原則，則不會對 Web 服務進行呼叫，且會顯示標準錯誤頁面。

如果未設定此原則，則 Microsoft Edge 會遵守 edge://settings/privacy 的 [服務] 底下所設定的使用者喜好設定。
具體來說，使用者可以將 **[找不到網頁時，推薦類似的頁面]** 切換為開啟或關閉。 請注意，如果您已啟用此原則 (AlternateErrorPagesEnabled)，則會開啟 [找不到網頁時，推薦類似的頁面] 設定，但使用者無法使用切換來變更設定。 如果您停用此原則，則會關閉 [找不到網頁時，推薦類似的頁面] 設定，且使用者無法使用切換來變更設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AlternateErrorPagesEnabled
  - GP 名稱：找不到網頁時，推薦類似的頁面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AlternateErrorPagesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AlternateErrorPagesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AlwaysOpenPdfExternally
  #### 一律在外部開啟 PDF 檔案
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  停用 Microsoft Edge 中的內部 PDF 檢視器。

如果啟用此原則，則 Microsoft Edge 會將 PDF 檔案視為下載項目，並讓使用者使用預設應用程式開啟。

如果未設定或停用此原則，則 Microsoft Edge 會開啟 PDF 檔案 (除非使用者停用)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AlwaysOpenPdfExternally
  - GP 名稱：一律在外部開啟 PDF 檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AlwaysOpenPdfExternally
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AlwaysOpenPdfExternally
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AmbientAuthenticationInPrivateModesEnabled
  #### 針對 InPrivate 和來賓設定檔啟用環境驗證
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AmbientAuthenticationInPrivateModesEnabled
  - GP 名稱：針對 InPrivate 和來賓設定檔啟用環境驗證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AmbientAuthenticationInPrivateModesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AmbientAuthenticationInPrivateModesEnabled
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AppCacheForceEnabled
  #### 允許重新啟用 AppCache 功能 (即使此功能預設為關閉的狀態) 
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 84 或更新版本

  #### 說明
  如果您將此原則設定為 true，系統會啟用 AppCache，即使預設值為不提供 Microsoft Edge 中的 AppCache。

如果您將此原則設為 false 或未設定，AppCache 將會依照 Microsoft Edge 的預設值決定是否啟用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AppCacheForceEnabled
  - GP 名稱：允許重新啟用 AppCache 功能 (即使此功能預設為關閉狀態) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AppCacheForceEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AppCacheForceEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ApplicationLocaleValue
  #### 設定應用程式地區設定
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  設定 Microsoft Edge 中的應用程式地區設定，並防止使用者變更地區設定。

如果啟用此原則，則 Microsoft Edge 會使用指定的地區設定。 如果不支援所設定的地區設定，則會改用 'en-US'。

如果停用或未設定此設定，則 Microsoft Edge 會使用使用者指定偏好地區設定 (如果已設定) 或後援地區設定 'en-US'。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ApplicationLocaleValue
  - GP 名稱：設定應用程式地區設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ApplicationLocaleValue
  - 值類型：REG_SZ
  ##### 範例值：
```
en
```


  

  [回到頁首](#microsoft-edge---policies)

  ### AudioCaptureAllowed
  #### 允許或封鎖音訊擷取
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許您設定是否提示使用者授與網站其音訊擷取裝置的存取權。 此原則適用於所有 URL，[AudioCaptureAllowedUrls](#audiocaptureallowedurls) 清單中設定的除外。

如果啟用此原則或未設定 (預設值)，則會提示使用者輸入音訊擷取存取權 ([AudioCaptureAllowedUrls](#audiocaptureallowedurls) 清單中的 URL 除外)。 這些列出的 URL 會獲授與存取權，且不會提示。

如果停用此原則，則不會提示使用者，且音訊擷取僅可供 [AudioCaptureAllowedUrls](#audiocaptureallowedurls) 中設定的 URL 存取。

此原則會影響所有類型的音訊輸入，而不僅僅是內建的麥克風。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AudioCaptureAllowed
  - GP 名稱：允許或封鎖音訊擷取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AudioCaptureAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AudioCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AudioCaptureAllowedUrls
  #### 無需要求權限即可存取音訊擷取裝置的網站
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 模式指定可使用音訊擷取裝置的網站，而不詢問使用者提供權限。 此清單中的模式會對照要求端 URL 的安全性來源進行比對。 如果符合，則網站會自動獲授與音訊擷取裝置的存取權。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AudioCaptureAllowedUrls
  - GP 名稱：無需要求權限即可存取音訊擷取裝置的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\1 = https://www.contoso.com/
SOFTWARE\Policies\Microsoft\Edge\AudioCaptureAllowedUrls\2 = https://[*.]contoso.edu/

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AudioCaptureAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AudioSandboxEnabled
  #### 允許音訊沙盒執行
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  此原則會控制音訊處理程序沙盒。

如果啟用此原則，則音訊處理程序會在沙盒中執行。

如果停用此原則，音訊處理程序將不在沙盒中執行，而 WebRTC 音訊處理模組將在轉譯器處理程序中執行。
這會讓使用者處於與不在沙盒中執行音訊子系統相關的安全性風險。

如果未設定此原則，則會使用音訊沙盒的預設設定，這可能會因平台而有所不同。

此原則的目的是讓企業能夠在他們使用會干擾沙盒的安全性軟體設定時，有彈性可停用音訊沙盒。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AudioSandboxEnabled
  - GP 名稱：允許音訊沙盒執行
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AudioSandboxEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AudioSandboxEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AutoImportAtFirstRun
  #### 在首次執行時，自動匯入其他瀏覽器的資料和設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoImportAtFirstRun
  - GP 名稱：在首次執行時，自動匯入其他瀏覽器的資料和設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoImportAtFirstRun
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutoImportAtFirstRun
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AutoLaunchProtocolsFromOrigins
  #### 定義一份協定清單，可在不須提示使用者的情下，從列出的來源啟動外部應用程式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  可讓您設定一份協定的清單，以及每個協定相關聯的 [允許的來源模式] 清單，以便在不提示使用者的情況下啟動外部應用程式。 在列出清單時，不應包含尾端分隔符號。 例如，列出「skype」，而不是「skype:」或「skype://」。

若您設定了此原則，則只有在下列情況下，才允許協定在不使用原則提示下啟動外部應用程式：

- 將協定列於

- 嘗試啟動協定的網站來源，符合此協定的 allowed_origins 清單中的其中一個原始模式。

如果其中一個條件設為 false，原則將不會省略外部通訊提示。

如果您未設定此原則，系統不會啟動任何協定。 使用者可以在每個協定/每個網站上退出提示，除非將 [ ExternalProtocolDialogShowAlwaysOpenCheckbox](#externalprotocoldialogshowalwaysopencheckbox) 原則設為 [停用]。 此原則不會影響使用者設定的每個通訊協定/每個網站的提示。

「來源比對」模式使用類似格式，適合 [URLBlocklist](#urlblocklist) 原則，文件儲存在 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)。

然而，此原則的「來源比對」模式不能包含 "/path" 或 "@query" 元素。 任何含有 "/path" 或 "@query" 元素的模式都會被忽略。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoLaunchProtocolsFromOrigins
  - GP 名稱：定義一份協定清單，可從列出的來源啟動外部應用程式，且不須提示使用者
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoLaunchProtocolsFromOrigins
  - 值類型：REG_SZ
  ##### 範例值：
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
    "protocol": "teams"
  }, 
  {
    "allowed_origins": [
      "*"
    ], 
    "protocol": "outlook"
  }
]
```


  #### Mac 資訊和設定
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

  ### AutoOpenAllowedForURLs
  #### URLs where AutoOpenFileTypes 可以套用 
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  適用 [AutoOpenFileTypes](#autoopenfiletypes) 的URLs 清單。 此原則不會影響使用者透過下載區設定的自動開啟值... >「永遠開啟這種類型的檔案」功能表項目。

若您將 URLs 設在此原則內，只要此 URL 屬於這個集合，且該檔案類型為 [AutoOpenFileTypes](#autoopenfiletypes)所列之一，系統會利用此原則自動開啟檔案。 如果其中一個條件為 false，則下載不會根據原則自動開啟。

若您未設定此原則，所有文件類型在 [AutoOpenFileTypes](#autoopenfiletypes) 的下載皆可自動打開。

URL 模式的格式必須依照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoOpenAllowedForURLs
  - GP 名稱：AutoOpenFileTypes 可以套用的 URLs 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)： SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\1 = example.com
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\2 = https://ssl.server.com
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\3 = hosting.com/good_path
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\4 = https://server:8080/path
SOFTWARE\Policies\Microsoft\Edge\AutoOpenAllowedForURLs\5 = .exact.hostname.com

```


  #### Mac 資訊和設定
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

  ### AutoOpenFileTypes
  #### 檔案類型清單應在下載時自動開啟
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  此原則設定的檔案類型清單應在下載時自動開啟。 注意：在列出檔案類型時，不應包含前置分隔符號，因此請列出 "txt"，而不是 ".txt"。

根據預設，系統會自動開啟所有 URLs 的檔案類型。 您可以使用 [AutoOpenAllowedForURLs](#autoopenallowedforurls) 原則限制可自動開啟這些檔案類型的 URLs。

應自動開啟的檔案類型，仍會受到已啟用的 Microsoft Defender SmartScreen 檢查，若未能通過檢查，系統即不會開啟這些檔案。

使用者已指定要自動開啟的檔案類型，將會在下載時持續自動開啟。 使用者仍可繼續指定其他要自動開啟的檔案類型。

若您未設定此原則，只有經使用者指定要自動開啟的檔案類型，才會在下載時持續自動開啟。

                                                                                                                                                                                                           

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoOpenFileTypes
  - GP 名稱：檔案類型清單應在下載時自動開啟
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\1 = exe
SOFTWARE\Policies\Microsoft\Edge\AutoOpenFileTypes\2 = txt

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutoOpenFileTypes
  - 範例值：
``` xml
<array>
  <string>exe</string>
  <string>txt</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AutofillAddressEnabled
  #### 啟用地址自動填寫
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用自動填寫功能，並允許使用者使用先前儲存的資訊自動完成網頁表單中的地址資訊。

如果停用此原則，則自動填寫不會建議或填入地址資訊，也不會儲存使用者在瀏覽網頁時可能提交的其他地址資訊。

如果啟用此原則或未設定，則使用者可以在使用者介面中控制地址的自動填寫。

請注意，如果停用此原則，則也會停止所有網頁表單的所有活動，付款和密碼表單除外。 不會儲存更多項目，且 Microsoft Edge 將不會建議或自動填寫任何先前的項目。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutofillAddressEnabled
  - GP 名稱：啟用地址自動填寫
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AutofillAddressEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutofillAddressEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AutofillCreditCardEnabled
  #### 啟用信用卡自動填寫
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用 Microsoft Edge 的自動填寫功能，並讓使用者使用先前儲存的資訊自動完成網頁表單中的信用卡資訊。

如果停用此原則，則自動填寫不會建議或填入信用卡資訊，也不會儲存使用者在瀏覽網頁時可能提交的其他信用卡資訊。

如果啟用此原則或未設定，則使用者可以控制信用卡的自動填寫。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutofillCreditCardEnabled
  - GP 名稱：啟用信用卡自動填寫
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：AutofillCreditCardEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutofillCreditCardEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### AutoplayAllowed
  #### 允許網站自動播放媒體
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  此原則會設定網站的媒體自動播放原則。

預設設定 [尚未設定] 會遵守目前的媒體自動播放設定，並可讓使用者設定其自動播放設定。

設定為 [已啟用] 會將媒體自動播放設定為「允許」。  允許所有網站自動播放媒體。 使用者無法覆寫此原則。

設定設為 [已停用] 會將媒體自動播放設定為「封鎖」。  不允許任何網站自動播放媒體。 使用者無法覆寫此原則。

需要關閉索引標籤並重新開啟，此原則才能生效。


  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：AutoplayAllowed
  - GP 名稱：允許網站自動播放媒體
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：AutoplayAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：AutoplayAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BackgroundModeEnabled
  #### 在 Microsoft Edge 關閉後繼續執行背景應用程式
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  允許 Microsoft Edge 處理程序在 OS 登入時啟動，並持續執行直到最後一個瀏覽器視窗關閉為止。 在此案例中，背景應用程式和目前瀏覽工作階段會保持作用中，包括任何工作階段 Cookie。 開啟中的背景處理程序會在系統匣中顯示圖示，且一律能從該位置關閉。

如果啟用此原則，則會開啟背景模式。

如果停用此原則，則背景模式會關閉。

如果未設定此原則，則最初會關閉背景模式，而使用者可以在 edge://settings/system 中設定其行為。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BackgroundModeEnabled
  - GP 名稱：在 Microsoft Edge 關閉後繼續執行背景應用程式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：BackgroundModeEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### BackgroundTemplateListUpdatesEnabled
  #### 啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  讓您啟用或停用對集錦的可用範本和使用範本的其他功能的清單進行背景更新。  範本用來在您將頁面儲存到集錦時，從網頁中擷取豐富的中繼資料。

如果啟用此設定或未設定此設定，則會每隔 24 小時在背景中透過 Microsoft 服務下載可用的範本清單。

如果停用此設定，則會在需要時下載可用範本清單。 這類型的下載可能會導致集錦及其他功能的效能些微降低。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BackgroundTemplateListUpdatesEnabled
  - GP 名稱：啟用對集錦的可用範本和使用範本的其他功能的清單進行背景更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BackgroundTemplateListUpdatesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BackgroundTemplateListUpdatesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BingAdsSuppression
  #### 封鎖 Bing 搜尋結果中的所有廣告
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  在 Bing.com 上啟用無廣告的搜尋體驗

如果啟用此原則，則使用者可以在 bing.com 上搜尋，並提供無廣告的搜尋體驗。 同時，安全搜尋設定會設定為「嚴格」，而且無法由使用者變更。

如果未設定此原則，則預設體驗會在 bing.com 的搜尋結果中出現廣告。 安全搜尋會預設設為「中等」，並且可由使用者變更。

此原則僅適用由 Microsoft 識別為 EDU 租用戶的 K-12 SKU。

請參閱[https://go.microsoft.com/fwlink/?linkid=2119711](https://go.microsoft.com/fwlink/?linkid=2119711)，以深入了解此原則或下列案例是否適合您：

* 您有 EDU 租用戶，但原則沒有作用。

* 您將您的 IP 加入白名單，以獲得無廣告的搜尋體驗。

* 您在 Microsoft Edge 舊版中擁有無廣告的搜尋體驗，並想要升級至新版 Microsoft Edge。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BingAdsSuppression
  - GP 名稱：封鎖 Bing 搜尋結果中的所有廣告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BingAdsSuppression
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BingAdsSuppression
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BlockThirdPartyCookies
  #### 封鎖第三方 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  封鎖不是來自網址列中網域的網頁元素，使其無法設定 Cookie。

如果啟用此原則，則網址列中不是來自網域的網頁元素就無法設定 Cookie

如果停用此原則，來自網址列以外網域的網頁元素可以設定 Cookie。

如果未設定此原則，則會啟用協力廠商 Cookie，但使用者可以變更此設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BlockThirdPartyCookies
  - GP 名稱：封鎖第三方 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：BlockThirdPartyCookies
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BlockThirdPartyCookies
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BrowserAddProfileEnabled
  #### 啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者使用 [新增個人檔案]**** 選項建立新的設定檔。
如果啟用此原則或未設定，則 Microsoft Edge 會允許使用者使用 [身分識別] 飛出視窗功能表或 [設定] 頁面上的 [新增個人檔案]**** 來建立新的個人檔案。

如果停用此原則，則使用者無法從 [身分識別] 飛出視窗功能表或 [設定] 頁面新增設定檔。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BrowserAddProfileEnabled
  - GP 名稱：啟用從 [身分識別] 飛出視窗功能表或 [設定] 頁面建立設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserAddProfileEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BrowserAddProfileEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BrowserGuestModeEnabled
  #### 啟用來賓模式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用可允許在 Microsoft Edge 中使用來賓設定檔的選項。 在來賓設定檔中，瀏覽器不會從現有設定檔匯入瀏覽資料，而且會在所有來賓設定檔關閉時刪除瀏覽資料。

如果啟用此原則或未設定，則 Microsoft Edge 會讓使用者在來賓設定檔中瀏覽。

如果停用此原則，則 Microsoft Edge 不會讓使用者使用來賓設定檔瀏覽。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BrowserGuestModeEnabled
  - GP 名稱：啟用來賓模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserGuestModeEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BrowserGuestModeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BrowserNetworkTimeQueriesEnabled
  #### 允許查詢瀏覽器網路時間服務
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  防止 Microsoft Edge 偶爾傳送查詢至瀏覽器網路時間服務，以擷取準確的時間戳記。

如果停用此原則，則 Microsoft Edge 將會停止將查詢傳送至瀏覽器網路時間服務。

如果啟用此原則或未設定，則 Microsoft Edge 會偶爾將查詢傳送至瀏覽器網路時間服務。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BrowserNetworkTimeQueriesEnabled
  - GP 名稱：允許查詢瀏覽器網路時間服務
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserNetworkTimeQueriesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BrowserNetworkTimeQueriesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BrowserSignin
  #### 瀏覽器登入設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BrowserSignin
  - GP 名稱：瀏覽器登入設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BrowserSignin
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BrowserSignin
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BuiltInDnsClientEnabled
  #### 使用內建的 DNS 用戶端
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制是否使用內建的 DNS 用戶端。

這不會影響所使用的 DNS 伺服器；只有用來與它們通訊的軟體堆疊。 例如，如果作業系統設定為使用企業 DNS 伺服器，則內建 DNS 用戶端將會使用相同的伺服器。 不過，內建的 DNS 用戶端可能會使用更現代的 DNS 相關通訊協定 (例如 DNS-over-TLS)，以不同的方式來為伺服器定址。

如果啟用此原則，則會使用內建的 DNS 用戶端 (如果可用)。

如果停用此原則，則永遠不會使用用戶端。

如果未設定此原則，則內建的 DNS 用戶端預設會在 MacOS 上啟用，且使用者可以透過編輯 edge://flags 或指定命令列旗標來變更是否使用內建的 DNS 用戶端。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：BuiltInDnsClientEnabled
  - GP 名稱：使用內建的 DNS 用戶端
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：BuiltInDnsClientEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BuiltInDnsClientEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### BuiltinCertificateVerifierEnabled
  #### 決定是否使用內建的憑證驗證程式來驗證伺服器憑證 (已淘汰)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - macOS 上，版本 83 或更新版本

  #### 說明
  此原則已過時，因為其目的只是為了提供做為短期的機制，給予企業更多時間來更新其環境，並在發現它們與內建的認證驗證程式不相容時報告問題。
 
  

  

當 Mac OS X 上的舊版憑證驗證程式支援已計畫移除時，此原則無法在 Microsoft Edge 版本 87 上運作。


  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  

  #### Mac 資訊和設定
  - 喜好設定機碼名稱：BuiltinCertificateVerifierEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForCas
  #### 針對 subjectPublicKeyInfo 雜湊的清單，停用憑證透明度強化
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  針對 subjectPublicKeyInfo 雜湊的清單，停用憑證透明度需求的強制執行。

此原則可讓您針對包含其中一個指定 subjectPublicKeyInfo 雜湊憑證的憑證鏈結，停用憑證透明度揭露需求。 這會允許可能以其他方式不受信任的憑證，因為它們並未公開揭露，而仍用於企業主機。

若要在設定此原則時停用認證透明度強化，則必須符合下列其中一組條件：
1. 雜湊是伺服器憑證的 subjectPublicKeyInfo。
2. 雜湊屬於 subjectPublicKeyInfo，會顯示在憑證鏈結的 CA 憑證中，該 CA 憑證是透過 X.509v3 nameConstraints 擴充功能來限制，permittedSubtrees 中會出現一或多個 directoryName nameConstraints，且 directoryName 會包含 organizationName 屬性。
3. 雜湊屬於 subjectPublicKeyInfo，會顯示在 CA 憑證中憑證鏈結中，該 CA 憑證在憑證主體中有一或多個 organizationName 屬性，而伺服器的憑證包含相同數量的 organizationName 屬性、順序相同，並具有完全相同的值。

subjectPublicKeyInfo 雜湊的指定方式是將雜湊演算法名稱、"/" 字元，以及套用至指定憑證的 DER 編碼的 subjectPublicKeyInfo 雜湊演算法的 Base64 編碼串連。 此 Base64 編碼與 SPKI 指紋的格式相同，如 RFC 7469 2.4 節中所定義。 將忽略無法辨識的雜湊演算法。 目前唯一支援的雜湊演算法是 "sha256"。

如果停用或未設定此原則，則需要透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未根據憑證透明度原則揭露的話)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForCas
  - GP 名稱：停用 subjectPublicKeyInfo 雜湊清單的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\1 = sha256/AAAAAAAAAAAAAAAAAAAAAA==
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForCas\2 = sha256//////////////////////w==

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForCas
  - 範例值：
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForLegacyCas
  #### 停用舊版憑證授權單位清單的憑證透明度強化
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  針對舊版憑證授權單位 (CA) 的清單，停用憑證透明度需求的強制執行。

此原則可讓您針對包含其中一個指定 subjectPublicKeyInfo 雜湊憑證的憑證鏈結，停用憑證透明度揭露需求。 這會允許可能以其他方式不受信任的憑證，因為它們並未公開揭露，而仍繼續用於企業主機。

若要停用憑證透明度強制執行，您必須將雜湊設定為會顯示在識別為舊版憑證授權單位 (CA) 的 CA 憑證中的 subjectPublicKeyInfo。 舊版 CA 是由 Microsoft Edge 所支援的一或多個作業系統所公開信任的 CA。

您可以指定 subjectPublicKeyInfo 雜湊，方法是將雜湊演算法名稱、"/" 字元，以及套用至指定憑證的 DER 編碼的 subjectPublicKeyInfo 雜湊演算法的 Base64 編碼串連。 此 Base64 編碼與 SPKI 指紋的格式相同，如 RFC 7469 2.4 節中所定義。 將忽略無法辨識的雜湊演算法。 目前唯一支援的雜湊演算法是 "sha256"。

如果未設定此原則，則需要透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未根據憑證透明度原則揭露的話)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForLegacyCas
  - GP 名稱：停用舊版憑證授權單位清單的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\1 = sha256/AAAAAAAAAAAAAAAAAAAAAA==
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForLegacyCas\2 = sha256//////////////////////w==

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForLegacyCas
  - 範例值：
``` xml
<array>
  <string>sha256/AAAAAAAAAAAAAAAAAAAAAA==</string>
  <string>sha256//////////////////////w==</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CertificateTransparencyEnforcementDisabledForUrls
  #### 停用針對特定 URL 的憑證透明度強化
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  針對所列的 URL，停用憑證透明度需求的強制執行。

此原則可讓您不透過憑證透明度，揭露指定 URL 中主機名稱的憑證。 這可讓您使用可能以其他方式不受信任的憑證，因為它們並正確未公開揭露，但會使得較難以偵測為這些主機錯誤核發的憑證。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。 因為憑證僅對指定的主機名稱有效，與配置、連接埠或路徑無關，因此只會考慮 URL 的主機名稱部分。 不支援萬用字元主機。

如果未設定此原則，則應該透過憑證透明度揭露的任何憑證都將被視為不受信任 (如果未揭露的話)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CertificateTransparencyEnforcementDisabledForUrls
  - GP 名稱：停用針對特定 URL 的憑證透明度強化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\1 = contoso.com
SOFTWARE\Policies\Microsoft\Edge\CertificateTransparencyEnforcementDisabledForUrls\2 = .contoso.com

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CertificateTransparencyEnforcementDisabledForUrls
  - 範例值：
``` xml
<array>
  <string>contoso.com</string>
  <string>.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ClearBrowsingDataOnExit
  #### 在 Microsoft Edge 關閉時清除瀏覽資料
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  Microsoft Edge 預設不會在關閉時清除瀏覽資料。 瀏覽資料包括在表單中輸入的資訊、密碼，甚至是造訪的網站。

如果啟用此原則，則每次關閉 Microsoft Edge 時，會刪除所有瀏覽資料。 請注意，如果啟用此原則，則它會優先於您設定的 [DefaultCookiesSetting](#defaultcookiessetting)

如果停用或未設定此原則，則使用者可以在 [設定] 中設定 [清除瀏覽資料] 選項。

如果啟用此原則，則請勿設定 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 原則，因為它們全都涉及刪除瀏覽資料。 如果設定了前述原則和此原則，則 Microsoft Edge 關閉時會刪除所有瀏覽資料，無論您如何設定 [AllowDeletingBrowserHistory](#allowdeletingbrowserhistory) 或 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit)。

若要避免在結束時刪除 Cookie，請設定 [SaveCookiesOnExit](#savecookiesonexit) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ClearBrowsingDataOnExit
  - GP 名稱：在 Microsoft Edge 關閉時清除瀏覽資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ClearBrowsingDataOnExit
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ClearBrowsingDataOnExit
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ClearCachedImagesAndFilesOnExit
  #### 在 Microsoft Edge 關閉時清除快取的影像和檔案
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  Microsoft Edge 預設不會在關閉時清除快取的影像和檔案。

如果啟用此原則，則每次關閉 Microsoft Edge 時，會刪除快取的影像和檔案。

如果停用此原則，則使用者無法在 edge://settings/clearBrowsingDataOnClose 中設定快取影像和檔案選項。

如果未設定此原則，則使用者可以選擇是否要在結束時清除快取的影像和檔案。

如果停用此原則，則請勿啟用 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則，因為它們全都涉及刪除資料。 如果您同時設定這兩項，則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 原則優先，並且會在 Microsoft Edge 關閉時刪除所有資料，無論 [ClearCachedImagesAndFilesOnExit](#clearcachedimagesandfilesonexit) 的設定方式如何。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ClearCachedImagesAndFilesOnExit
  - GP 名稱：在 Microsoft Edge 關閉時清除快取的影像和檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ClearCachedImagesAndFilesOnExit
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ClearCachedImagesAndFilesOnExit
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ClickOnceEnabled
  #### 允許使用者使用 ClickOnce 通訊協定開啟檔案
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  允許使用者使用 ClickOnce 通訊協定開啟檔案。 ClickOnce 通訊協定會允許網站要求瀏覽器利用使用者電腦或裝置上的 ClickOnce 檔案處理常式從特定 URL 開啟檔案。

如果啟用此原則，則使用者可以使用 ClickOnce 通訊協定來開啟檔案。 此原則會覆寫 edge://flags/ 頁面中使用者的 ClickOnce 設定。

如果停用此原則，則使用者無法使用 ClickOnce 通訊協定來開啟檔案。 而是會改為使用瀏覽器將檔案儲存到檔案系統。 此原則會覆寫 edge://flags/ 頁面中使用者的 ClickOnce 設定。

如果您未設定此原則，Microsoft Edge 87 之前的使用者將無法使用 ClickOnce 通訊協定開啟檔案。 不過，他們可以利用 edge://flags/ 頁面選擇是否要啟用 ClickOnce 通訊協定的使用。 Microsoft Edge 版 本87 及更新版本的使用者可以預設使用 ClickOnce 通訊協定來開啟檔案，但可以利用 edge://flags/頁面選擇停用 ClickOnce 通訊協定。

停用 ClickOnce 可能會防止 ClickOnce 應用程式 (.application 檔案) 正常啟動。

如需 ClickOnce 的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099880](https://go.microsoft.com/fwlink/?linkid=2099880)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ClickOnceEnabled
  - GP 名稱：允許使用者使用 ClickOnce 通訊協定開啟檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ClickOnceEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### CollectionsServicesAndExportsBlockList
  #### 封鎖集錦中服務和匯出目標特定清單的存取權
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 86 或更新版本

  #### 說明
  列出使用者無法在 Microsoft Edge 的集錦功能中存取的特定服務和匯出目標。 這包括顯示來自 Bing 的其他資料，並將集錦匯出至 Microsoft 產品或外部合作夥伴。

如果啟用此原則，系統會封鎖與指定清單相符的服務和匯出目標。

如果未設定此原則，則對強制執行的可接受服務和匯出目標沒有限制。

                                                     

原則選項對應：

* pinterest_suggestions (pinterest_suggestions) = Pinterest 建議

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CollectionsServicesAndExportsBlockList
  - GP 名稱：封鎖集錦中服務和匯出目標特定清單的存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\CollectionsServicesAndExportsBlockList\1 = pinterest_suggestions

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱： CollectionsServicesAndExportsBlockList
  - 範例值：
``` xml
<array>
  <string>pinterest_suggestions</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### CommandLineFlagSecurityWarningsEnabled
  #### 啟用命令列旗標的安全性警告
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  如果停用，則此原則會在 Microsoft Edge 使用可能有危險的命令列旗標啟動時防止安全性警告顯示。

如果啟用或未設定，則使用這些命令列旗標來啟動 Microsoft Edge 時，會顯示安全性警告。

例如，--disable-gpu-sandbox 旗標會產生此警告：您使用不支援的命令列旗標：--disable-gpu-sandbox。 這會造成穩定性及安全性風險。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CommandLineFlagSecurityWarningsEnabled
  - GP 名稱：啟用命令列旗標的安全性警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：CommandLineFlagSecurityWarningsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CommandLineFlagSecurityWarningsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ComponentUpdatesEnabled
  #### 啟用 Microsoft Edge 中的元件更新
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  如果啟用或未設定此原則，則會在 Microsoft Edge 中啟用元件更新。

如果停用此原則或將它設定為 false，則會停用 Microsoft Edge 中所有元件的元件更新。

不過，有些元件會從此原則免除。 這包括不包含可執行程式碼、不會著變更瀏覽器行為，或對安全性非常重要的何元件。 也就是說，即使您停用此原則，也會套用「對安全性非常重要」的更新。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ComponentUpdatesEnabled
  - GP 名稱：啟用 Microsoft Edge 中的元件更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ComponentUpdatesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ComponentUpdatesEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ConfigureDoNotTrack
  #### 設定不要追蹤
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定是否要將「不要追蹤」要求傳送到要求追蹤資訊的網站。 「不要追蹤」要求可讓您瀏覽的網站知道您不希望您的瀏覽活動遭到追蹤。 依預設，Microsoft Edge 不會傳送「不要追蹤」要求，但是使用者可以開啟此功能以傳送要求。

如果啟用此原則，則一律會傳送「不要追蹤」要求到要求追蹤資訊的網站。

如果停用此原則，則永遠不會傳送要求。

如果未設定此原則，則使用者可以選擇是否要傳送這些要求。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ConfigureDoNotTrack
  - GP 名稱：設定不要追蹤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureDoNotTrack
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ConfigureDoNotTrack
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ConfigureOnPremisesAccountAutoSignIn
  #### 設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入
  
  
  #### 支援的版本：
  - Windows 上，版本 81 或更新版本

  #### 說明
  如果使用者的電腦已加入網域且您的環境未混合加入，則可啟用使用 Active Directory 帳戶自動登入。 如果您想要改為讓使用者以其 Azure Active Directory 帳戶自動登入，請對您的環境套用 Azure AD 加入 (如需詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2118197](https://go.microsoft.com/fwlink/?linkid=2118197)) 或混合式加入 (如需詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2118365](https://go.microsoft.com/fwlink/?linkid=2118365))。

如果 [BrowserSignin](#browsersignin) 原則設為已停用，則此原則沒有作用。

如果啟用此原則，並將其設定為 'SignInAndMakeDomainAccountNonRemovable'，則 Microsoft Edge 會自動將已加入網域電腦的使用者以其 Active Directory 帳戶登入。

如果將此原則設定為 ‘已停用’ 或未設定，則 Microsoft Edge 不會自動將已加入網域電腦的使用者以 Active Directory 帳戶登入。

原則選項對應：

* 已停用 (0) = 已停用

* SignInAndMakeDomainAccountNonRemovable (1) = 登入並將網域帳戶設為不可移除

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ConfigureOnPremisesAccountAutoSignIn
  - GP 名稱：設定當沒有 Azure AD 網域帳戶時，使用 Active Directory 網域帳戶自動登入
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureOnPremisesAccountAutoSignIn
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### ConfigureOnlineTextToSpeech
  #### 設定線上文字轉語音
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定瀏覽器是否可以利用「線上文字轉語音」語音字型，它是 Azure 認知服務的一部分。 這些語音字型的品質高於預先安裝的系統語音字型。

如果啟用或未設定此原則，則使用 SpeechSynthesis API 的 Web 型應用程式可以使用「線上文字轉語音」語音字型。

如果停用此原則，則語音字型將無法使用。

若要深入了解此功能，請參閱這裡：SpeechSynthesis API：[https://go.microsoft.com/fwlink/?linkid=2110038](https://go.microsoft.com/fwlink/?linkid=2110038) 認知服務：[https://go.microsoft.com/fwlink/?linkid=2110141](https://go.microsoft.com/fwlink/?linkid=2110141)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ConfigureOnlineTextToSpeech
  - GP 名稱：設定線上文字轉語音
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureOnlineTextToSpeech
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ConfigureOnlineTextToSpeech
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ConfigureShare
  #### 設定共用體驗
  
  
  #### 支援的版本：
  - Windows 上，版本 83 或更新版本

  #### 說明
  如果將此原則設定為 'ShareAllowed' (預設值)，則使用者可以從 Microsoft Edge 的 [設定及其他] 功能表存取 Windows 10 的共用體驗，以便與系統上的其他應用程式共用。

如果將此原則設定為 'ShareDisallowed'，則使用者無法存取 Windows 10 的共用體驗。 如果 [共用] 按鈕在工具列上，則也會隱藏。

原則選項對應：

* ShareAllowed (0) = 允許使用共用體驗

* ShareDisallowed (1) = 不允許使用共用體驗

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ConfigureShare
  - GP 名稱：設定共用體驗
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ConfigureShare
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### CustomHelpLink
  #### 指定自訂說明連結
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  為 [說明] 功能表或 F1 鍵指定連結。

如果啟用此原則，則系統管理員可以為 [說明] 功能表或 F1 鍵指定連結。

如果停用或未設定此原則，則會使用 [說明] 功能表或 F1 鍵的預設連結。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：CustomHelpLink
  - GP 名稱：指定自訂說明連結
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：CustomHelpLink
  - 值類型：REG_SZ
  ##### 範例值：
```
https://go.microsoft.com/fwlink/?linkid=2080734
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：CustomHelpLink
  - 範例值：
``` xml
<string>https://go.microsoft.com/fwlink/?linkid=2080734</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DNSInterceptionChecksEnabled
  #### DNS 攔截檢查已啟用
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  此原則會設定可用於停用 DNS 攔截檢查的本機交換器。 這些檢查會嘗試探索瀏覽器是否位於會將未知主機名稱重新導向的 Proxy 後面。

在網路設定已知的企業環境中，可能不需要此偵測。 可以將它停用，以避免啟動時以及每個 DNS 設定變更時的額外 DNS 和 HTTP 流量。

若您啟用或未設定此原則，系統便會執行 DNS 攔截檢查。

若您停用此原則，系統便不會執行 DNS 攔截檢查。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DNSInterceptionChecksEnabled
  - GP 名稱：DNS 攔截檢查已啟用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DNSInterceptionChecksEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DNSInterceptionChecksEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultBrowserSettingEnabled
  #### 將 Microsoft Edge 設定為預設瀏覽器
  
  
  #### 支援的版本：
  - Windows 7 和 macOS 上，版本 77 或更新版本

  #### 說明
      

  若您將此原則設為 True，Microsoft Edge 就會在啟動時永遠檢查是否為預設瀏覽器，如果可能，則會自動註冊。

若您將此原則設為 False，Microsoft Edge 就會停止檢查是否為預設瀏覽器，並開啟此選項的使用者控制。

如果您未設定此原則，Microsoft Edge 可讓使用者控制是否將其設為預設值，如果不是，是否顯示使用者通知。

Windows 系統管理員的注意事項：此原則只適用執行 Windows 7 的電腦。 針對較新版本的 Windows，您必須部署一個「預設應用程式關聯」檔案，讓 Microsoft Edge 成為 HTTPS 和 HTTP 通訊協定 (以及選用的 FTP 通訊協定和檔案格式，例如 .html、.htm、.pdf、.svg、.webp) 的處理常式。 如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2094932](https://go.microsoft.com/fwlink/?linkid=2094932)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultBrowserSettingEnabled
  - GP 名稱：將 Microsoft Edge 設定為預設瀏覽器
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DefaultBrowserSettingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultBrowserSettingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DefaultSearchProviderContextMenuAccessAllowed
  #### 允許預設搜尋提供者操作功能表搜尋存取權
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  可在操作功能表上使用預設搜尋提供者。

如果您將此原則設為停用，則依賴於預設搜尋提供者的搜尋操作功能表將無法使用，而且側邊欄搜尋也無法使用。

如果將此原則設定為啟用或未設定，則可使用預設搜尋提供者和側邊欄搜尋的操作功能表項目。

只有啟用 [DefaultSearchProviderEnabled](#defaultsearchproviderenabled) 原則時，才會套用該原則值，否則不適用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DefaultSearchProviderContextMenuAccessAllowed
  - GP 名稱：允許預設搜尋提供者操作功能表搜尋存取權
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DefaultSearchProviderContextMenuAccessAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DefaultSearchProviderContextMenuAccessAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DelayNavigationsForInitialSiteListDownload
  #### 要求在索引標籤導覽前， [企業模式網站清單] 即已可使用
  
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
  可讓您指定是否要讓 Microsoft Edge 索引標籤等待導覽，直到連覽器已下載初始的 [企業模式網站清單]。 這項設定適用於瀏覽器首頁應在 Internet Explorer 模式中載入的情況，在啟用 IE 模式之後，首次執行瀏覽器時，這是很重要的。 如果此情況不存在，我們建議您不要啟用這項設定，因為這可能會對載入首頁的效能造成負面影響。 只有在 Microsoft Edge 沒有 [快取的] 企業模式網站清單 (例如，在啟用 IE 模式後首次執行瀏覽器時才會使用) ，才會套用此設定。

此設定會與下列內容一併執行：[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode'，並設定 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中該清單至少擁有一個項目。

此原則的超時行為可以設定為 [ NavigationDelayForInitialSiteListDownloadTimeout](#navigationdelayforinitialsitelistdownloadtimeout) 原則。

如果您將此原則設定為 'All'，當 Microsoft Edge 沒有 [企業模式網站清單] 的快取版本時，索引標籤會延遲瀏覽直到瀏覽器完成下載網站清單為止。 在 Internet Explorer 模式中，由網站清單設定為開啟的網站將會在 Internet Explorer 模式中載入，即使在瀏覽器的首次瀏覽期間也是如此。 無法在 Internet Explorer 中設定開啟的網站，像是具有 [http:]、[https:]、[file:] 或 [ftp:] 的任何網站，都不會在 Microsoft Edge 中延遲導覽和立即載入。

如果您將此原則設定為 'None' 或未設定此原則，當 Microsoft Edge 沒有 [企業模式網站清單] 的快取版本時，索引標籤會立即導覽，而不會等候瀏覽器完成下載 [企業模式網站清單]。 由網站清單設定以 Internet Explorer 模式開啟的網站，將會以 Microsoft Edge 模式開啟直到瀏覽器完成下載 [企業模式網站清單] 為止。

原則選項對應：

* None (0) = 無

* All (1) = 所有符合條件的瀏覽

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DelayNavigationsForInitialSiteListDownload
  - GP 名稱：要求在索引標籤導覽前， [企業模式網站清單] 即已可使用
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DelayNavigationsForInitialSiteListDownload
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### DeleteDataOnMigration
  #### 移轉時刪除舊版瀏覽器資料
  
  
  #### 支援的版本：
  - Windows 上，版本 83 或更新版本

  #### 說明
  此原則會決定在移轉到 Microsoft Edge 版本 81 或更新版本之後，是否會刪除來自 Microsoft Edge 舊版的使用者瀏覽資料。

如果將此原則設定為 [已啟用]，則在移轉到 Microsoft Edge 版本 81 或更新版本之後，所有來自 Microsoft Edge 舊版的瀏覽資料都會被刪除。 在移轉到 Microsoft Edge 版本 81 或更新版本之前，必須先設定此原則，才能對現有的瀏覽資料有任何作用。

如果將此原則設定為 [已停用] 或未設定原則，則在移轉到 Microsoft Edge 版本 83 或更新版本之後，將不會刪除使用者瀏覽資料。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DeleteDataOnMigration
  - GP 名稱：移轉時刪除舊版瀏覽器資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DeleteDataOnMigration
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### DeveloperToolsAvailability
  #### 控制可使用開發人員工具的位置
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制可使用開發人員工具的位置。

如果將此原則設定為 'DeveloperToolsDisallowedForForceInstalledExtensions' (預設值)，則使用者一般可以存取開發人員工具和 JavaScript 主控台，但無法存取透過企業原則安裝的擴充功能之內容。

如果將此原則設定為 'DeveloperToolsAllowed'，則使用者可以存取所有內容中的開發人員工具和 JavaScript 主控台，包括透過企業原則安裝的擴充功能。

如果將此原則設定為 'DeveloperToolsDisallowed'，則使用者無法存取開發人員工具或檢查網站元素。 開啟開發人員工具或 JavaScript 主控台的鍵盤快速鍵和功能表或內容功能表項目會停用。

原則選項對應：

* DeveloperToolsDisallowedForForceInstalledExtensions (0) = 在企業原則安裝的擴充功能上封鎖開發人員工具，並在其他內容中允許

* DeveloperToolsAllowed (1) = 允許使用開發人員工具

* DeveloperToolsDisallowed (2) = 不允許使用開發人員工具

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DeveloperToolsAvailability
  - GP 名稱：控制可使用開發人員工具的位置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DeveloperToolsAvailability
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DeveloperToolsAvailability
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DiagnosticData
  #### 傳送關於瀏覽器使用狀況的必要和選擇性診斷資料
  
  
  #### 支援的版本：
  - Windows 7 和 macOS 上，版本 86 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DiagnosticData
  - GP名稱：傳送關於瀏覽器使用狀況的必要和選擇性診斷資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：DiagnosticData
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DiagnosticData
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DirectInvokeEnabled
  #### 允許使用者使用 DirectInvoke 通訊協定開啟檔案
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  允許使用者使用 DirectInvoke 通訊協定來開啟檔案。 DirectInvoke 通訊協定會允許網站要求瀏覽器利用使用者電腦或裝置上的特定檔案處理常式從特定 URL 開啟檔案。

如果啟用或未設定此原則，則使用者可以使用 DirectInvoke 通訊協定來開啟檔案。

如果停用此原則，則使用者無法使用 DirectInvoke 通訊協定來開啟檔案。 檔案會改為儲存到檔案系統。

注意：停用 DirectInvoke 可能會使得某些 Microsoft SharePoint Online 功能無法如預期般運作。

如需 DirectInvoke 的詳細資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2103872](https://go.microsoft.com/fwlink/?linkid=2103872) 和 [https://go.microsoft.com/fwlink/?linkid=2099871](https://go.microsoft.com/fwlink/?linkid=2099871)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DirectInvokeEnabled
  - GP 名稱：允許使用者使用 DirectInvoke 通訊協定開啟檔案
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DirectInvokeEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### Disable3DAPIs
  #### 停用 3D 圖形 API 支援
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  防止網頁存取圖形處理器 (GPU)。 具體來說，網頁無法存取 WebGL API，且外掛程式無法使用 Pepper 3D API。

如果未設定或停用此原則，則可能會允許網頁使用 WebGL API 和外掛程式使用 Pepper 3D API。 Microsoft Edge 預設可能仍需要傳遞命令列參數，才能使用這些 API。

如果 [HardwareAccelerationModeEnabled](#hardwareaccelerationmodeenabled) 原則設定為 false，則會忽略 'Disable3DAPIs' 原則的設定，這相當於將 'Disable3DAPIs' 原則設定為 true。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：Disable3DAPIs
  - GP 名稱：停用 3D 圖形 API 支援
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：Disable3DAPIs
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：Disable3DAPIs
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DisableScreenshots
  #### 停用取得螢幕擷取畫面功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制使用者是否可以取得瀏覽器頁面的螢幕擷取畫面。

如果已啟用，則使用者無法使用鍵盤快速鍵或擴充功能 API 來取得螢幕擷取畫面。

如果停用或未設定此原則，則使用者可以取得螢幕擷取畫面。

請注意，此原則會控制在瀏覽器本身內取得的螢幕擷取畫面。 即使您啟用此原則，使用者仍然可以使用瀏覽器以外的一些方法 (例如使用作業系統功能或其他應用程式) 來取得螢幕擷取畫面。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DisableScreenshots
  - GP 名稱：停用取得螢幕擷取畫面功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DisableScreenshots
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DisableScreenshots
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DiskCacheDir
  #### 設定磁碟快取目錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定用來儲存快取檔案的目錄。

如果啟用此原則，則 Microsoft Edge 會使用提供的目錄，而無論使用者是否已指定 '--disk-cache-dir' 旗標。 若要避免資料遺失或其他非預期的錯誤，請勿將此原則設定為磁碟區的根目錄或用於其他用途的目錄，因為 Microsoft Edge 會管理其內容。

如需可在指定目錄和路徑時使用的變數清單，請參閱 [https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果未設定此原則，則會使用預設的快取目錄，且使用者可以使用 '--disk-cache-dir' 命令列旗標來覆寫該預設值。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DiskCacheDir
  - GP 名稱：設定磁碟快取目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DiskCacheDir
  - 值類型：REG_SZ
  ##### 範例值：
```
${user_home}/Edge_cache
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DiskCacheDir
  - 範例值：
``` xml
<string>${user_home}/Edge_cache</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DiskCacheSize
  #### 設定磁碟快取大小，以位元組為單位
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定用來在磁碟上儲存檔案的快取大小 (以位元組為單位)。

如果啟用此原則，則 Microsoft Edge 會使用提供的快取大小，而無論使用者是否已指定 '--disk-cache-size' 旗標。 此原則中指定的值不是硬性界限，而是對快取系統的建議；低於一些 MB 的任何值都太小，並將會進位為合理的最小值。

如果將此原則的值設為 0，則會使用預設的快取大小，且使用者無法變更。

如果未設定此原則，則會使用預設大小，但使用者可以使用 '--disk-cache-size' 旗標來覆寫它。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DiskCacheSize
  - GP 名稱：設定磁碟快取大小，以位元組為單位
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DiskCacheSize
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x06400000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DiskCacheSize
  - 範例值：
``` xml
<integer>104857600</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DnsOverHttpsMode
  #### 控制 DNS-over-HTTPS 模式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DnsOverHttpsMode
  - GP 名稱：控制 DNS-over-HTTPS 模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DnsOverHttpsMode
  - 值類型：REG_SZ
  ##### 範例值：
```
off
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DnsOverHttpsMode
  - 範例值：
``` xml
<string>off</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DnsOverHttpsTemplates
  #### 指定所需的 DNS-over-HTTPS 解析程式的 URI 範本
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  所需的 DNS-over-HTTPS 解析程式的 URI 範本。 若要指定多個 DNS-over-HTTPS 解析程式，請以空格分隔對應的 URI 範本。

如果將 [DnsOverHttpsMode](#dnsoverhttpsmode) 設定為 "secure"，則必須設定此原則，且不能為空白。

如果將 [DnsOverHttpsMode](#dnsoverhttpsmode) 設定為 "automatic"，並設定此原則，則會使用指定的 URI 範本。 如果未設定此原則，則會使用硬式編碼對應，嘗試將使用者目前的 DNS 解析程式升級至由相同提供者所運作的 DoH 解析程式。

如果 URI 範本包含 dns 變數，對解析程式的要求將會使用 GET；否則要求會使用 POST。

將忽略格式不正確的範本。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DnsOverHttpsTemplates
  - GP 名稱：指定所需的 DNS-over-HTTPS 解析程式的 URI 範本
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：DnsOverHttpsTemplates
  - 值類型：REG_SZ
  ##### 範例值：
```
https://dns.example.net/dns-query{?dns}
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DnsOverHttpsTemplates
  - 範例值：
``` xml
<string>https://dns.example.net/dns-query{?dns}</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DownloadDirectory
  #### 設定下載目錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定下載檔案時要使用的目錄。

如果啟用此原則，則 Microsoft Edge 會使用提供的目錄，而無論使用者是否已指定一個目錄或選擇要每次收到下載位置的提示。 如需可使用的變數清單，請參閱[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果停用或未設定此原則，則會使用預設的下載目錄，且使用者可以變更它。

如果設定了無效路徑，Microsoft Edge 會預設為使用者的預設下載目錄。

如果路徑指定的資料夾不存在，則下載會觸發提示，詢問使用者想要儲存其下載項目的位置。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DownloadDirectory
  - GP 名稱：設定下載目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DownloadDirectory
  - 值類型：REG_SZ
  ##### 範例值：
```

      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DownloadDirectory
  - 範例值：
``` xml
<string>
      Linux-based OSes (including Mac): /home/${user_name}/Downloads
      Windows: C:\Users\${user_name}\Downloads</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### DownloadRestrictions
  #### 允許下載限制
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：DownloadRestrictions
  - GP 名稱：允許下載限制
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：DownloadRestrictions
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：DownloadRestrictions
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EdgeCollectionsEnabled
  #### 啟用集錦功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  讓您允許使用者存取集錦功能，在其中，他們可以以更有效率的方式收集、整理、共用及匯出內容，並具有 Office 整合。

如果啟用或未設定此原則，則使用者可以在 Microsoft Edge 中存取並使用集錦功能。

如果停用此原則，則使用者無法在 Microsoft Edge 中存取及使用集錦。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EdgeCollectionsEnabled
  - GP 名稱：啟用集錦功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EdgeCollectionsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EdgeCollectionsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EditFavoritesEnabled
  #### 允許使用者編輯我的最愛
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用此原則可讓使用者新增、移除及修改我的最愛。 如果未設定此原則，則這是預設行為。

停用此原則可讓使用者無法新增、移除或修改我的最愛。 他們仍可以使用現有的我的最愛。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EditFavoritesEnabled
  - GP 名稱：允許使用者編輯我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EditFavoritesEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EditFavoritesEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnableDeprecatedWebPlatformFeatures
  #### 在限定時間內重新啟用已過時的網頁平台功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要暫時重新啟用的已過時網頁平台功能清單。

此原則可讓您在限定時間內重新啟用已過時的網頁平台功能。 功能會依字串標籤來識別。

如果未設定此原則，如果清單為空白，或如果功能不符合支援的其中一個字串標籤，則所有過時的網頁平台功能會保持停用。

雖然上述平台上支援原則本身，它要啟用的功能可能無法在這所有平台上使用。 並非所有過時的網頁平台功能都可以重新啟用。 只有下列明確列出的項目才可以重新啟用，且僅限於有限的一段時間，這會因每個功能而不同。 您可以在 https://bit.ly/blinkintents 檢閱網頁平台功能變更的背後意圖。

字串標籤的一般格式為 [DeprecatedFeatureName]_EffectiveUntil[yyyymmdd]。

原則選項對應：

* ExampleDeprecatedFeature (ExampleDeprecatedFeature_EffectiveUntil20080902) = 啟用 ExampleDeprecatedFeature API 到 2008 年 9 月 2 日

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableDeprecatedWebPlatformFeatures
  - GP 名稱：在限定時間內重新啟用已過時的網頁平台功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\EnableDeprecatedWebPlatformFeatures\1 = ExampleDeprecatedFeature_EffectiveUntil20080902

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableDeprecatedWebPlatformFeatures
  - 範例值：
``` xml
<array>
  <string>ExampleDeprecatedFeature_EffectiveUntil20080902</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnableDomainActionsDownload
  #### 啟用從 Microsoft 進行網域動作下載 (已過時) 
                       
        
  
  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### 支援的版本：
  - 在 Windows 和 macOS 上，版本 77 到 84

  #### 說明
  這個原則無法使用，應避免衝突的狀態。 此原則原是用以啟用/停用網域動作清單的下載，但它並不一定能達到所需的狀態。 處理下載的實驗和設定服務擁有自己的群組原則，可設定從服務下載的內容。 請改為使用 [ExperimentationAndConfigurationServiceControl](#experimentationandconfigurationservicecontrol) 原則。

在 Microsoft Edge 中，網域動作代表可協助瀏覽器在網路上正常運作的一系列相容性功能。

Microsoft 會基於相容性原因，保留對特定網域採取的動作清單。 例如，如果網站因為 Microsoft Edge 上的新使用者代理字串而損毀，則瀏覽器可能會覆寫網站上的使用者代理程式字串。 這些動作都是 Microsoft 嘗試解決網站擁有者的問題時的暫時性動作。

當瀏覽器啟動，然後之後定期啟動時，瀏覽器將會與包含要執行的最新相容性動作清單的實驗和設定服務連絡。 此清單會在初次擷取之後儲存在本機，以便後續的要求只會在伺服器的複本變更之後才更新該清單。

如果啟用此原則，則會繼續透過實驗和設定服務下載網域動作的清單。

如果停用此原則，則不再會透過實驗和設定服務下載網域動作的清單。

如果未設定此原則，則會繼續透過實驗和設定服務下載網域動作的清單。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableDomainActionsDownload
  - GP 名稱：啟用從 Microsoft 進行網域動作下載 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableDomainActionsDownload
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableDomainActionsDownload
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnableOnlineRevocationChecks
  #### 啟用線上 OCSP/CRL 檢查
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  線上撤銷檢查不會提供顯著的安全性優點，而且預設為停用。

如果啟用此原則，則 Microsoft Edge 將會執行非封鎖性失敗的線上 OCSP/CRL 檢查。 「非封鎖性失敗」表示如果無法連接撤銷伺服器，則會將憑證視為有效。

如果停用或未設定此原則，則 Microsoft Edge 不會執行線上撤銷檢查。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableOnlineRevocationChecks
  - GP 名稱：啟用線上 OCSP/CRL 檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnableOnlineRevocationChecks
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableOnlineRevocationChecks
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnableSha1ForLocalAnchors
  #### 允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  啟用此設定時，只要憑證連結接到本機安裝的根憑證，Microsoft Edge 就能以 SHA-1 簽署的憑證來保護您的連線，而這是有效的。

請注意，此原則視允許 SHA-1 簽名的作業系統 (OS) 憑證驗證堆疊而定。 如果 OS 更新變更了 SHA-1 憑證的 OS 處理，可能會導致這個原則沒有作用。  此外，此原則旨在為企業提供更多時間來擺脫 SHA-1，以做為暫時的因應措施。 這項原則將會在 2021 年中旬的 Microsoft Edge 92 中被移除。

如果您未設定此原則或將其設為 False，或將 SHA-1 憑證連結到公開信任的憑證根，Microsoft Edge 將不允許 SHA-1 簽署的憑證。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnableSha1ForLocalAnchors
  - GP 名稱：允許由本機信賴起點頒發的 SHA-1 簽章憑證 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：EnableSha1ForLocalAnchors
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnableSha1ForLocalAnchors
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnterpriseHardwarePlatformAPIEnabled
  #### 允許受管擴充功能使用企業硬體平台 API
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  當此原則設定為已啟用時，即會允許由企業原則安裝的擴充功能，以使用企業硬體平台 API。
當此原則設定為已停用或未設定時，則不會允許任何擴充功能使用企業硬體平台 API。
此原則也適用於元件擴充功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnterpriseHardwarePlatformAPIEnabled
  - GP 名稱：允許受管擴充功能使用企業硬體平台 API
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：EnterpriseHardwarePlatformAPIEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：EnterpriseHardwarePlatformAPIEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### EnterpriseModeSiteListManagerAllowed
  #### 允許存取 Enterprise Mode Site List Manager 工具
  
  
  #### 支援的版本：
  - Windows 上，版本 86 或更新版本

  #### 說明
  可讓您設定 Enterprise Mode Site List Manager 是否可供使用者使用。

如果啟用這項原則，使用者會在 edge://compat 頁面上看到 [Enterprise Mode Site List Manager] 瀏覽按鈕，瀏覽至該工具並加以使用。

如果停用或未設定此原則，則使用者不會看到 [Enterprise Mode Site List Manager] 瀏覽按鈕，也無法使用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：EnterpriseModeSiteListManagerAllowed
  - GP 名稱：允許存取 Enterprise Mode Site List Manager 工具
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：EnterpriseModeSiteListManagerAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  #### 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  您可以啟用此原則以建立一份檔案類型副檔名字典，及相對應的網域清單，可使這些檔案不受使用檔案類型副檔名的下載警告。 這可讓企業系統管理員封鎖與所列網域相關聯之檔案的檔案類型副檔名下載警告。 例如，如果「jnlp」副檔名與「website1.com」相關聯，使用者在從「website1.com」下載「jnlp」檔案時就不會看到警示訊息，但在從　「website2.com」下載「jnlp」檔案時就會看到下載警示訊息。

凡是檔案具有以此原則指定網域的檔案類型副檔名，仍受限於非檔案類型副檔名的安全性警告，例如混合式內容下載警示和 Microsoft Defender SmartScreen 的警示。

若您停用或未設定此原則，凡具有觸發以副檔名為依據的下載警示的檔案會向使用者顯示警示訊息。

如果您啟用這個原則：

* URL 模式的格式應依照 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322)設定。
* 輸入的檔案類型副檔名必須是小寫的 ASCII。 在列出檔案類型副檔名時，不應包含前置分隔符號，因此請列出「jnlp」，而不是「.jnlp」。

範例：

下列範例數值可以防止 [contoso.com] 網域的 [swf]、[exe] 和 [jnlp 副檔名] 的檔案類型副檔名下載警示。 它會在任何適於 exe 和 jnlp 檔案的其他網域中顯示使用者的檔案類型副檔名下載警示，但不適用於 swf 檔案。

[ { "file_extension": "jnlp", "domains": ["contoso.com"] }, { "file_extension": "exe", "domains": ["contoso.com"] }, { "file_extension": "swf", "domains": ["*"] } ]

請注意，在以上範例中，雖然所有網域中的 [swf] 檔案禁止顯示檔案類型副檔名式下載警告，但由於安全性方面的問題考量，不建議您在任何危險的檔案類型副檔名上顯示這些警告。 此範例僅顯示了執行此動作的功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - GP 名稱：針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\1 = {'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}
SOFTWARE\Policies\Microsoft\Edge\ExemptDomainFileTypePairsFromFileTypeDownloadWarnings\2 = {'domains': ['*'], 'file_extension': 'swf'}

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExemptDomainFileTypePairsFromFileTypeDownloadWarnings
  - 範例值：
``` xml
<array>
  <string>{'domains': ['https://contoso.com', 'contoso2.com'], 'file_extension': 'jnlp'}</string>
  <string>{'domains': ['*'], 'file_extension': 'swf'}</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExperimentationAndConfigurationServiceControl
  #### 控制與實驗和設定服務的通訊
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExperimentationAndConfigurationServiceControl
  - GP 名稱：控制與實驗和設定服務的通訊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExperimentationAndConfigurationServiceControl
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExperimentationAndConfigurationServiceControl
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ExternalProtocolDialogShowAlwaysOpenCheckbox
  #### 在外部通訊協定對話方塊中顯示「一律開啟」核取方塊
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  此原則會控制是否要在外部通訊協定啟動確認提示中顯示 [一律允許此網站開啟這類連結] 核取方塊。 這個原則只適用於 https:// 連結。

如果啟用此原則，當外部通訊協定提示顯示時，使用者可以選取 [一律允許]，以在此網站上略過該通訊協定的所有未來確認提示。

如果停用此原則，則不會顯示 [一律允許] 核取方塊。 每次呼叫外部通訊協定時，都會提示使用者進行確認。

在 Microsoft Edge 83 之前，如果您未設定此原則，則不會顯示 [永遠允許] 核取方塊。 每次呼叫外部通訊協定時，都會提示使用者進行確認。

在 Microsoft Edge 83 上，如果未設定此原則，則核取方塊可見度會由 edge://flags 中的 [啟用記憶通訊協定啟動提示喜好設定] 旗標控制

截至 Microsoft Edge 84，如果不啟用此原則，當外部通訊協定確認提示顯示時，使用者可以選取 [一律允許]，以在此網站上略過該通訊協定的所有未來確認提示。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - GP 名稱：在外部通訊協定對話方塊中顯示 [一律開啟] 核取方塊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ExternalProtocolDialogShowAlwaysOpenCheckbox
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### FamilySafetySettingsEnabled
  #### 允許使用者設定家長監護服務
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  此原則會停用並在 [設定] 中完全隱藏 [家長監護服務] 頁面。 瀏覽至 edge://settings/familysafety 也會遭到封鎖。 [家長監護服務] 頁面會說明哪些功能可供家庭群組使用，以及如何加入家庭群組。 在這裡深入了解家長監護服務：([https://go.microsoft.com/fwlink/?linkid=2098432](https://go.microsoft.com/fwlink/?linkid=2098432))。

如果啟用此原則或未設定，則會顯示「家長監護服務」頁面。

如果停用此原則，則不會顯示家長監護服務頁面。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：FamilySafetySettingsEnabled
  - GP 名稱：允許使用者設定家長監護服務
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：FamilySafetySettingsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：FamilySafetySettingsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### FavoritesBarEnabled
  #### 啟用我的最愛列
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用或停用我的最愛列。

如果啟用此原則，則使用者會看到我的最愛列。

如果停用此原則，則使用者不會看到我的最愛列。

如果未設定此原則，則使用者可以決定是否使用我的最愛列。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：FavoritesBarEnabled
  - GP 名稱：啟用我的最愛列
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：FavoritesBarEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：FavoritesBarEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceBingSafeSearch
  #### 強制執行 Bing 安全搜尋
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceBingSafeSearch
  - GP 名稱：強制執行 Bing 安全搜尋
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceBingSafeSearch
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceBingSafeSearch
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceCertificatePromptsOnMultipleMatches
  #### 設定使用 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，Microsoft Edge 是否應自動選取憑證
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  切換有多個憑證可用且使用 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 設定網站時，是否提示使用者選取憑證。 如果未針對網站設定 [AutoSelectCertificateForUrls](#autoselectcertificateforurls)，則一律會提示使用者選取憑證。

如果將此原則設定為 True，則在有多個憑證時 (且僅在此情況下)，Microsoft Edge 會提示使用者針對 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 定義的清單上的網站選取憑證。

如果將此原則設定為 False 或未設定，即使有憑證的多個相符項目，Microsoft Edge 也會自動選取憑證。 針對在 [AutoSelectCertificateForUrls](#autoselectcertificateforurls) 所定義清單中的網站，系統不會提示使用者選取憑證。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceCertificatePromptsOnMultipleMatches
  - GP 名稱：設定以 "AutoSelectCertificateForUrls" 設定的網站有多個憑證相符時，是否應自動選取憑證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceCertificatePromptsOnMultipleMatches
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceCertificatePromptsOnMultipleMatches
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceEphemeralProfiles
  #### 啟用使用暫時設定檔
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制使用者設定檔是否切換為暫時模式。 暫時設定檔會在工作階段開始時建立，並在工作階段結束時刪除，且與使用者的原始設定檔相關聯。

如果啟用此原則，則設定檔會在暫時模式中執行。 這可讓使用者透過自己的裝置工作，而不需要將瀏覽資料儲存到這些裝置。 如果將此原則啟用為 OS 原則 (例如，在 Windows 上使用 GPO)，則它會套用至系統上的每個設定檔。

如果停用或未設定此原則，則使用者會在登入瀏覽器時取得一般的設定檔。

在暫時模式中，設定檔資料只會在該使用者工作階段期間儲存在磁碟上。 瀏覽器歷程記錄、擴充功能及其資料、Web 資料 (如 Cookie)，以及 Web 資料庫等功能，不會於瀏覽器關閉之後儲存。 這不會防止使用者手動將任何資料下載到磁碟，或是儲存頁面或列印頁面。 如果使用者已啟用同步，則會如同一般設定檔的方式，將所有資料保留在其同步帳戶中。 使用者也可以在暫時模式中使用 InPrivate 瀏覽，除非您明確地將它停用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceEphemeralProfiles
  - GP 名稱：啟用使用暫時設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceEphemeralProfiles
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceEphemeralProfiles
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceGoogleSafeSearch
  #### 強制執行 Google 安全搜尋
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  強制在 Google Web Search 中的查詢執行時將安全搜尋設為作用中，並防止使用者變更此設定。

如果啟用此原則，則 Google 搜尋中的安全搜尋一律會是作用中。

如果停用或未設定此原則，則不會在 Google 搜尋中強制執行安全搜尋。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceGoogleSafeSearch
  - GP 名稱：強制執行 Google 安全搜尋
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceGoogleSafeSearch
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceGoogleSafeSearch
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceLegacyDefaultReferrerPolicy
  #### 使用預設的查閱者原則－當降級且無查閱者時 (已被取代)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與目前預設的查閱者原則不一致時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本 86 中使用。

Microsoft Edge 的預設查閱者原則正在強化，透過逐步推出，從其目前的 no-referrer-when-downgrade 值到更安全的 strict-origin-when-cross-origin。

推出之前，此企業原則將不會有任何影響。 在推出之後，啟用此企業原則時，會將 Microsoft Edge 的預設查閱者原則設定為其舊值 no-referrer-when-downgrade。

此企業原則預設會停用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceLegacyDefaultReferrerPolicy
  - GP 名稱：使用預設的查閱者原則－當降級且無查閱者時 (已被取代)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceLegacyDefaultReferrerPolicy
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceLegacyDefaultReferrerPolicy
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ForceNetworkInProcess
  #### 強制網路程式碼在瀏覽器處理程序中執行 (已過時) 
                       
        
  
  
  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 83 及之後版本中運作。
  #### 支援的版本：
  - Windows 上，版本 78 至 83

  #### 說明
  此原則已遭取代，因為其只是一種短期機制，目的是要讓企業有更多時間可遷移到不依賴於使用網路 API 的第 3 方軟體。 建議透過 LSP 和 WIN32 API 修補來使用 Proxy 伺服器。

此原則會強制在瀏覽器處理程序中執行網路程式碼。

此原則預設為停用。 如果啟用，當網路處理程序在沙盒中執行時，使用者會面臨安全性問題。


 

  
  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceNetworkInProcess
  - GP 名稱：GP 名稱：強制網路程式碼在瀏覽器處理程序中執行 (已淘汰) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceNetworkInProcess
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### ForceYouTubeRestrict
  #### 強制最小 YouTube 限制模式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 YouTube 上強制執行最小限制模式，並防止使用者選取較不受限制的模式。

設定為 '嚴格' ，強制在 YouTube 上使用嚴格限制模式。

設定為 '中等'，強制使用者只能在 YouTube 上使用中等限制模式和嚴格限制模式。 他們無法停用限制模式。

設定為 '關閉' 或不設定此原則，以不要在 YouTube 上強制執行限制模式。 YouTube 原則等外部原則可能仍會強制執行限制模式。

原則選項對應：

* 關閉 (0) = 不要在 YouTube 上強制執行限制模式

* 中等 (1) = 強制在 YouTube 上至少使用中等限制模式

* 嚴格 (2) = 針對 YouTube 強制使用嚴格限制模式

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ForceYouTubeRestrict
  - GP 名稱：強制最小 YouTube 限制模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ForceYouTubeRestrict
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ForceYouTubeRestrict
  - 範例值：
``` xml
<integer>0</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### FullscreenAllowed
  #### 允許全螢幕模式
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  設定全螢幕模式的可用性 - 所有 Microsoft Edge UI 都會隱藏，且只會顯示網頁內容。

如果啟用此原則或未設定，則擁有適當權限的使用者、應用程式和擴充功能即可以進入全螢幕模式。

如果停用此原則，則使用者、應用程式和擴充功能無法進入全螢幕模式。

停用全螢幕模式時，無法使用命令列在 kiosk 模式中開啟 Microsoft Edge。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：FullscreenAllowed
  - GP 名稱：允許全螢幕模式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：FullscreenAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### GloballyScopeHTTPAuthCacheEnabled
  #### 啟用全域範圍的 HTTP 驗證快取
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  此原則會使用 HTTP 伺服器驗證認證來根據每個設定檔快取設定單一全域範圍。

如果停用或未設定此原則，則瀏覽器將會使用跨網站驗證的預設行為，於版本 80 開始時，將由熱門網站限定在 HTTP 伺服器驗證認證。 因此，如果兩個網站使用來自相同驗證網域的資源，就必須在這兩個網站的環境中個別提供認證。 快取的 Proxy 認證會跨網站重複使用。

如果啟用此原則，則在一個網站內容中輸入的 HTTP 驗證認證，將會自動用於另一個網站內容。

啟用此原則會使得網站遭受某種類型的跨網站攻擊，並允許跨網站追蹤使用者 (甚至是在沒有 Cookie 的情況下)，方法是使用內嵌在 URL 中的身分認證將項目新增至 HTTP 驗證快取。

此原則目的在讓基於舊版行為的企業有機會更新其登入程序，並將在未來移除。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：GloballyScopeHTTPAuthCacheEnabled
  - GP 名稱：啟用全域範圍的 HTTP 驗證快取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：GloballyScopeHTTPAuthCacheEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：GloballyScopeHTTPAuthCacheEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### GoToIntranetSiteForSingleWordEntryInAddressBar
  #### 強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  如果啟用此原則，如果在網址列中輸入的文字是不帶標點符號的單一字詞，則網址列建議清單中最上方的自動建議結果會導覽至內部網路網站。

輸入不帶標點符號的文字時，預設的導覽會是導覽至符合所輸入文字的內部網路網站。

如果啟用此原則，網址列建議清單中的第二個自動建議結果會完全按照所輸入的單字來執行網頁搜尋，前提是此文字為不帶標點符號的單一字詞。 將使用預設的搜尋提供者，除非也啟用防止網頁搜尋的原則。

啟用此原則的兩個影響如下：

瀏覽至網站以回應一般會解析為歷程記錄項目的單一文字查詢功能將不再發生。 相反地，瀏覽器會嘗試巡覽至可能不存在組織內部網路中的內部網站。 這會導致 404 錯誤。

熱門、單一文字搜尋字詞將需要手動選取搜尋建議，才能正確執行搜尋。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - GP 名稱：強制直接進行內部網路網站導覽，而非在網址列中搜尋單字項目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：GoToIntranetSiteForSingleWordEntryInAddressBar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### HSTSPolicyBypassList
  #### 設定會略過 HSTS 原則檢查的名稱清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  在此清單中指定的主機名稱將從可能會將要求從 "http://" 升級為 "https://" 的 HSTS 原則檢查中免除。 此原則中僅允許單一標籤的主機名稱。 主機名稱必須是正式的。 任何 IDN 都必須轉換成其 A 標籤格式，且所有 ASCII 字母都必須是小寫。 此原則僅適用指定的特定主機名稱；不會套用到清單中名稱的子網域。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：HSTSPolicyBypassList
  - GP 名稱：設定會略過 HSTS 原則檢查的名稱清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\HSTSPolicyBypassList\1 = meet

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：HSTSPolicyBypassList
  - 範例值：
``` xml
<array>
  <string>meet</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### HardwareAccelerationModeEnabled
  #### 可用時便使用硬體加速
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定使用硬體加速 (如果有的話)。 如果啟用此原則或未設定，除非明確封鎖 GPU 功能，否則會啟用硬體加速。

如果停用此原則，則會停用硬體加速。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：HardwareAccelerationModeEnabled
  - GP 名稱：可用時便使用硬體加速
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HardwareAccelerationModeEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：HardwareAccelerationModeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### HideFirstRunExperience
  #### 隱藏初次執行體驗與啟動顯示畫面
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  如果啟用此原則，則當使用者初次執行 Microsoft Edge 時，不會向使用者顯示初次執行體驗與啟動顯示畫面。

針對初次執行體驗中顯示的設定選項，瀏覽器將會預設為下列項目：

- 在 [新索引標籤] 頁面上，摘要類型將設定為 MSN 新聞，而版面配置為 [佈景]。

- 如果 Windows 帳戶屬於 Azure AD 或 MSA 類型，則使用者仍會自動登入 Microsoft Edge。

- 預設不會啟用同步，且使用者將可以從同步設定開啟同步。

如果停用或未設定此原則，則會顯示初次執行體驗和啟動顯示畫面。

注意：在初次執行體驗中向使用者顯示的特定設定選項，也可以使用其他特定原則來管理。 您可以使用 HideFirstRunExperience 原則結合這些原則，以在受管理的裝置上設定特定的瀏覽器體驗。 其他原則中的一部分為：

-[AutoImportAtFirstRun](#autoimportatfirstrun)

-[NewTabPageLocation](#newtabpagelocation)

-[NewTabPageSetFeedType](#newtabpagesetfeedtype)

-[SyncDisabled](#syncdisabled)

-[BrowserSignin](#browsersignin)

-[NonRemovableProfileEnabled](#nonremovableprofileenabled)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：HideFirstRunExperience
  - GP 名稱：隱藏初次執行體驗與啟動顯示畫面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：HideFirstRunExperience
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：HideFirstRunExperience
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportAutofillFormData
  #### 允許匯入自動填寫表單資料
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將自動填寫表單資料匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入自動填寫資料的選項。

如果停用此原則，則自動填寫表單資料不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入自動填寫資料，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入自動填寫資料，但是使用者可以在手動匯入期間選取或清除 [自動填寫資料]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 和 Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 瀏覽器的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportAutofillFormData
  - GP 名稱：允許匯入自動填寫表單資料
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportAutofillFormData
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportAutofillFormData
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportBrowserSettings
  #### 允許匯入瀏覽器設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將瀏覽器設定匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [瀏覽器設定]**** 核取方塊。

如果停用此原則，則瀏覽器設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入瀏覽器設定，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入設定，但使用者可以在手動匯入期間選取或清除 [瀏覽器設定]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (Windows 7、8 和 10 上，以及 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportBrowserSettings
  - GP 名稱：允許匯入瀏覽器設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportBrowserSettings
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportBrowserSettings
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportCookies
  #### 允許匯入 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將 Cookie 匯入到 Microsoft Edge。

如果停用此原則，則 Cookie 不會在初次執行時匯入。

如果未設定此原則，則 Cookie 會在初次執行時匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入 Cookie。

**注意**：此原則目前會管理來自 Google Chrome (Windows 7、8 和 10 上，以及 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportCookies
  - GP 名稱：允許匯入 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportCookies
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportCookies
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportExtensions
  #### 允許匯入擴充功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將擴充功能匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [擴充功能]**** 核取方塊。

如果停用此原則，則擴充功能不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入擴充功能，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入擴充功能，但使用者可以在手動匯入期間選取或清除 [我的最愛]**** 選項。

**注意**：此原則目前只支援來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportExtensions
  - GP 名稱：允許匯入擴充功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportExtensions
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportExtensions
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportFavorites
  #### 允許匯入我的最愛
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將我的最愛匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [我的最愛]**** 核取方塊。

如果停用此原則，則 [我的最愛] 不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則在初次執行時匯入我的最愛，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入我的最愛，但使用者可以在手動匯入期間選取或清除 [我的最愛]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上)、Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上)，以及 Apple Safari (在 macOS 上) 瀏覽器的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportFavorites
  - GP 名稱：允許匯入我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportFavorites
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportFavorites
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportHistory
  #### 允許匯入瀏覽歷程記錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將瀏覽歷程記錄匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [瀏覽歷程記錄]**** 核取方塊。

如果停用此原則，則瀏覽歷程記錄資料不會在初次執行時匯入，且使用者無法手動匯入此資料。

如果未設定此原則，瀏覽歷程記錄資料會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入瀏覽歷程記錄，但使用者可以在手動匯入期間選取或清除 [歷程記錄]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及 macOS 上)、Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 以及 Apple Safari (macOS) 瀏覽器的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportHistory
  - GP 名稱：允許匯入瀏覽歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportHistory
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportHistory
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportHomepage
  #### 允許匯入首頁設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將首頁設定匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入首頁設定的選項。

如果停用此原則，則首頁設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，首頁設定會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入首頁設定，但使用者可以在手動匯入期間選取或清除 [首頁]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportHomepage
  - GP 名稱：允許匯入首頁設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ImportHomepage
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportHomepage
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportOpenTabs
  #### 允許匯入開啟的索引標籤
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將開啟和釘選的索引標籤匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [開啟的索引標籤]**** 核取方塊。

如果停用此原則，則開啟的索引標籤不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入開啟的索引標籤，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入開啟的索引標籤，但使用者可以在手動匯入期間選取或清除 [開啟的索引標籤]**** 選項。

**注意**：此原則目前只支援來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportOpenTabs
  - GP 名稱：允許匯入開啟的索引標籤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportOpenTabs
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportOpenTabs
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportPaymentInfo
  #### 允許匯入付款資訊
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將付款資訊匯入到 Microsoft Edge。

如果啟用此原則，[匯入瀏覽器資料]**** 對話方塊中會自動選取 [付款資訊]**** 核取方塊。

如果停用此原則，則付款資訊不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，付款資訊在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入付款資訊，但使用者可以在手動匯入期間選取或清除 [付款資訊]**** 選項。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportPaymentInfo
  - GP 名稱：允許匯入付款資訊
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportPaymentInfo
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportPaymentInfo
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportSavedPasswords
  #### 允許匯入儲存的密碼
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將儲存的密碼匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取手動匯入儲存的密碼的選項。

如果停用此原則，則儲存的密碼不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，則會在初次執行時匯入密碼，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入它們。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入密碼，但使用者可以在手動匯入期間選取或清除 [密碼]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上)、Google Chrome (在 Windows 7、8 和 10 上，以及 macOS 上) 以及 Mozilla Firefox (在 Windows 7、8 和 10 上，以及在 macOS 上) 瀏覽器的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportSavedPasswords
  - GP 名稱：允許匯入儲存的密碼
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportSavedPasswords
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportSavedPasswords
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportSearchEngine
  #### 允許匯入搜尋引擎設定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許使用者從其他瀏覽器將搜尋引擎設定匯入到 Microsoft Edge。

如果啟用此原則，則會自動選取匯入搜尋引擎設定的選項。

如果停用此原則，則搜尋引擎設定不會在初次執行時匯入，且使用者無法手動匯入。

如果未設定此原則，搜尋引擎設定會在初次執行時匯入，且使用者可以選擇是否要在之後的瀏覽工作階段期間手動匯入此資料。

您可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入搜尋引擎設定，但使用者可以在手動匯入期間選取或清除 [搜尋引擎]**** 選項。

**注意**：此原則目前會管理來自 Internet Explorer (在 Windows 7、8 和 10 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportSearchEngine
  - GP 名稱：允許匯入搜尋引擎設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportSearchEngine
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportSearchEngine
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ImportShortcuts
  #### 允許匯入捷徑
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  允許使用者將捷徑從其他瀏覽器匯入到 Microsoft Edge。

如果停用此原則，則捷徑不會在初次執行時匯入。

如果未設定此原則，則捷徑會在初次執行時匯入。

您也可以將此原則設定為建議。 這表示 Microsoft Edge 會在初次執行時匯入捷徑。

**注意**：此原則目前會管理來自 Google Chrome (在 Windows 7、8 和 10 上，以及在 macOS 上) 的匯入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ImportShortcuts
  - GP 名稱：允許匯入捷徑
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ImportShortcuts
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ImportShortcuts
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### InPrivateModeAvailability
  #### 設定 InPrivate 模式可用性
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定使用者是否可以在 Microsoft Edge 的 InPrivate 模式中開啟頁面。

如果未設定此原則，或將其設定為 '已啟用'，則使用者可以在 InPrivate 模式中開啟頁面。

將此原則設定為 '已停用'，以防止使用者使用 InPrivate 模式。

將此原則設定為 '已強制'，以一律使用 InPrivate 模式。

原則選項對應：

* 已啟用 (0) = InPrivate 模式可用

* 已停用 (1) = InPrivate 模式已停用

* 已強制 (2) = InPrivate 模式已強制執行

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InPrivateModeAvailability
  - GP 名稱：設定 InPrivate 模式可用性
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InPrivateModeAvailability
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：InPrivateModeAvailability
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### IntensiveWakeUpThrottlingEnabled
  #### 管理 IntensiveWakeUpThrottling 功能
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  啟用 IntensiveWakeUpThrottling 功能時，會導致背景索引標籤中的 Javascript 計時器受到積極地節流和合併，在背景化達 5 分鐘或更久的單一頁面中運行每分鐘一次 (至多)。

這是一個符合網站標準的功能，但可能會造成某些網站的功能中斷，因為這會造成某些動作推遲多達一分鐘的時間。 不過，啟用時可造成顯著的節省 CPU 和電池損耗。 如需詳細資訊，請參閱https://bit.ly/30b1XR4。

如果啟用此原則，系統將會強制啟用此功能，而且使用者將無法覆寫這個設定。
如果停用此原則，系統將會強制停用此功能，而且使用者將無法覆寫這個設定。
若您未設定此原則，此功能將由其本身的內部邏輯所管理。 使用者可以手動設置此設定。

請注意，此原則會套用在每個轉譯過程，當轉譯過程啟動時，系統會強制執行此原則的最新值。 若要確保所有已載入的索引標籤都能收到一致的原則設定，則需完全重新開機。 使用此原則的不同值執行程式會造成危害。


  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：IntensiveWakeUpThrottlingEnabled
  - GP 名稱：管理 IntensiveWakeUpThrottling 功能
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：IntensiveWakeUpThrottlingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：IntensiveWakeUpThrottlingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### InternetExplorerIntegrationEnhancedHangDetection
  #### 針對 Internet Explorer 模式設定增強的當機偵測
  
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InternetExplorerIntegrationEnhancedHangDetection
  - GP 名稱：針對 Internet Explorer 模式設定增強的當機偵測
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱： InternetExplorerIntegrationEnhancedHangDetection
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### InternetExplorerIntegrationLevel
  #### 設定 Internet Explorer 整合
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

原則選項對應：

* None (0) = 無

* IEMode (1) = Internet Explorer 模式

* NeedIE (2) = Internet Explorer 11

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InternetExplorerIntegrationLevel
  - GP 名稱：設定 Internet Explorer 整合
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationLevel
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteList
  #### 設定 Enterprise Mode Site List
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InternetExplorerIntegrationSiteList
  - GP 名稱：設定 Enterprise Mode Site List
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationSiteList
  - 值類型：REG_SZ
  ##### 範例值：
```
https://internal.contoso.com/sitelist.xml
```


  

  [回到頁首](#microsoft-edge---policies)

  ### InternetExplorerIntegrationSiteRedirect
  #### 指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式
  
  
  #### 支援的版本：
  - Windows 上，版本 81 或更新版本

  #### 說明
  「頁面內」導覽是從連結、指令碼或目前頁面上的表單開始。 也可以是先前「頁面內」導覽嘗試的伺服器端重新導向。 相反地，使用者可以使用瀏覽器控制項以多種方式啟動不在「頁面內」且獨立於目前頁面的導覽。 例如透過網址列、返回按鈕或我的最愛連結。

此設定可讓您指定是否要從 Internet Explorer 模式下載入的頁面導覽至未設定網站 (未於 Enterprise Mode Site List 中設定) 切換回 Microsoft Edge 或停留在 Internet Explorer 模式。

此設定會與下列內容一併執行：[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設定為 'IEMode'，並設定 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中該清單至少擁有一個項目。

如果停用或未設定此原則，則只有設定在 Internet Explorer 模式中開啟的網站，才會在該模式中開啟。 所有未設定在 Internet Explorer 模式中開啟的網站，將會重新導向回到 Microsoft Edge。

如果將此原則設定為 ‘預設’，只有設定為在 Internet Explorer 模式中開啟的網站，才會在該模式中開啟。 所有未設定在 Internet Explorer 模式中開啟的網站，將會重新導向回到 Microsoft Edge。

如果將此原則設定為 'AutomaticNavigationsOnly'，將會獲得預設體驗，但對未設定網站的所有自動導覽 (例如 302 重新導向) 都會保留在 Internet Explorer 模式。

如果將此原則設定為 'AllInPageNavigations'，則於 IE 模式載入到未設定網站之頁面的所有導覽，都會保留在 Internet Explorer 模式 (最不建議)。

若要深入了解 Internet Explorer 模式，請參閱 [https://go.microsoft.com/fwlink/?linkid=2105106](https://go.microsoft.com/fwlink/?linkid=2105106)

原則選項對應：
  

* 預設值 (0) = 預設值

* AutomaticNavigationsOnly (1) = 只保留 Internet Explorer 模式中的自動導覽

* AllInPageNavigations (2) = 保留所有 Internet Explorer 模式中的頁面內導覽

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：InternetExplorerIntegrationSiteRedirect
  - GP 名稱：指定從 Internet Explorer 模式頁面啟動時，「頁面內」導覽至未設定網站的方式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：InternetExplorerIntegrationSiteRedirect
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### IsolateOrigins
  #### 為特定來源啟用網站隔離
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要在隔離中於其自己的處理程序中執行的來源。
此原則也會隔離由子網域所指定的來源，例如，指定 https://contoso.com/ 會導致 https://foo.contoso.com/ 隨著 https://contoso.com/ 網站中的一部分隔離。
如果已啟用原則，以逗號分隔清單中的每個指定來源，將會在自己的處理程序中執行。
如果停用此原則，則會同時停用 'IsolateOrigins' 和 'SitePerProcess' 功能。 使用者仍然可以透過命令列旗標手動啟用 'IsolateOrigins' 原則。
如果未設定此原則，則使用者可以變更此設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：IsolateOrigins
  - GP 名稱：為特定來源啟用網站隔離
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：IsolateOrigins
  - 值類型：REG_SZ
  ##### 範例值：
```
https://contoso.com/,https://fabrikam.com/
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：IsolateOrigins
  - 範例值：
``` xml
<string>https://contoso.com/,https://fabrikam.com/</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### LocalProvidersEnabled
  #### 允許來自本地提供者的建議
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  在 Microsoft Edge 的網址列和自動建議清單中，允許來自裝置上建議提供者的建議 (本機提供者)，例如我的最愛和瀏覽歷程記錄。

如果啟用此原則，則會使用來自本機提供者的建議。

如果停用此原則，則永遠不會使用來自本機提供者的建議。 將不會顯示本機歷程記錄和本機我的最愛建議。

如果未設定此原則，則會允許來自本機提供者的建議，但使用者可以使用 [設定] 切換來變更。

請注意，如果已套用停用此功能的原則，則部分功能可能無法使用。 例如，如果您啟用 [SavingBrowserHistoryDisabled](#savingbrowserhistorydisabled) 原則，瀏覽歷程記錄建議將無法使用。

此原則需要將瀏覽器重新啟動，才能完成套用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：LocalProvidersEnabled
  - GP 名稱：允許來自本地提供者的建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：LocalProvidersEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：LocalProvidersEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ManagedFavorites
  #### 設定我的最愛
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定受管理的我的最愛清單。

該原則會建立我的最愛清單。 每個我的最愛都包含 "name" 和 "url"，這些機碼會保留我的最愛名稱及其目標。 您可以定義一個不帶 "url" 機碼但帶有一個額外的 "children" 機碼的我的最愛，藉此設定子資料夾，其中包含上面定義的我的最愛清單 (其中部分也可能是資料夾)。 Microsoft Edge 會修訂不完整的 URL，就如同透過網址列提交一般，例如 "microsoft.com" 會變成 "https://microsoft.com/"。

這些我的最愛會放在不能由使用者修改的資料夾中 (但使用者可以選擇將它從我的最愛列隱藏)。 依預設，資料夾名稱是「受管理的我的最愛」，但您可以將包含機碼 "toplevel_name" 並使用所需的資料夾名稱做為值的字典新增至我的最愛清單。

受管理我的最愛不會同步到使用者帳戶，且不能由擴充功能修改。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ManagedFavorites
  - GP 名稱：設定我的最愛
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ManagedFavorites
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ### ManagedSearchEngines
  #### 管理搜尋引擎
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓您設定最多 10 個搜尋引擎的清單，其中一個必須標示為預設搜尋引擎。
您不需要指定編碼。 從 Microsoft Edge 80 開始，suggest_url 和 image_search_url 參數都是選用。 選用參數 image_search_post_params (包含逗號分隔名稱/值對) 從 Microsoft Edge 80 開始提供。

從 Microsoft Edge 83 開始，您可以使用 allow_search_engine_discovery optional 選用參數來啟用搜尋引擎探索。 此參數必須是清單中的第一個項目。 如果未指定 allow_search_engine_discovery，即預設會停用搜尋引擎探索。 從 Microsoft Edge 84 開始，您可以將此原則設定為建議的原則，以允許搜尋提供者探索。 您不需要新增 allow_search_engine_discovery 選用參數。

如果啟用此原則，則使用者無法新增、移除或變更清單中的任何搜尋引擎。 使用者可以將其預設搜尋引擎設定為清單中的任何搜尋引擎。

如果停用或未設定此原則，則使用者可以視需要修改搜尋引擎清單。

如果已設定 [DefaultSearchProviderSearchURL](#defaultsearchprovidersearchurl) 原則，則會忽略此原則 (ManagedSearchEngines)。 使用者必須將其瀏覽器重新啟動，才能完成套用此原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ManagedSearchEngines
  - GP 名稱：管理搜尋引擎
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ManagedSearchEngines
  - 值類型：REG_SZ
  ##### 範例值：
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


  #### Mac 資訊和設定
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

  ### MaxConnectionsPerProxy
  #### 同時連線到 Proxy 伺服器的最大數目
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定對 Proxy 伺服器同時連線的上限。

某些 Proxy 伺服器無法處理每個用戶端的大量同時連線，您可以將此原則設定為較低的值來解決此情況。

此原則的值應低於 100，並高於 6。 預設值為 32。

某些 Web 應用程式已知會因為當機的 GET 耗用多個連線。將連線上限降低至低於 32 可能會在開啟許多這類 Web 應用程式時導致瀏覽器網路當機。

如果未設定此原則，則會使用預設值 (32)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：MaxConnectionsPerProxy
  - GP 名稱：同時連線到 Proxy 伺服器的最大數目
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MaxConnectionsPerProxy
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000020
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：MaxConnectionsPerProxy
  - 範例值：
``` xml
<integer>32</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### MediaRouterCastAllowAllIPs
  #### 允許 Google Cast 連線至所有 IP 位址上的投射裝置
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用此原則以讓 Google Cast 連線至所有 IP 位址上的投射裝置，不只是 RFC1918/RFC4193 私人位址。

停用此原則以限制 Google Cast 連線至 RFC1918/RFC4193 私人位址上的投射裝置。

如果未設定此原則，除非啟用 CastAllowAllIPs 功能，否則 Google Cast 僅會連線至 RFC1918/RFC4193 私人位址上的投射裝置。

如果 [EnableMediaRouter](#enablemediarouter) 原則為已停用，則此原則沒有作用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：MediaRouterCastAllowAllIPs
  - GP 名稱：允許 Google Cast 連線至所有 IP 位址上的投射裝置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MediaRouterCastAllowAllIPs
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：MediaRouterCastAllowAllIPs
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### MetricsReportingEnabled
  #### 啟用使用方式和當機相關的資料報告 (已過時)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
   
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  此原則已被取代。 目前支援，但將在 Microsoft Edge 版本 89 中過時。 這個原則會由新原則取代：Windows 7、Windows 8 和 macOS 的 [DiagnosticData](#diagnosticdata)。 這項原則會由 Win 10 上的允許遙測取代 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))。

此原則可將Microsoft Edge 使用方式和當機相關資料的報告傳送到 Microsoft。

啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。 停用此原則，就不會將此資料傳送到 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

在 Windows 10 上，如果未設定此原則，則 Microsoft Edge 將預設為使用 Windows 診斷資料設定。 如果啟用此原則，則僅當 Windows 診斷資料設定設為「增強」或「完整」時，Microsoft Edge 才會傳送使用狀況資料。 如果停用此原則，則 Microsoft Edge 將不會傳送使用狀況資料。 根據 Windows 診斷資料設定傳送當機相關的資料。 在這裡深入了解 Windows 診斷資料設定：[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

在 Windows 7、Windows 8 和 macOS 上，此原則會控制使用方式和當機相關資料的傳送。 如果未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

若要啟用此原則，[SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 必須設定為 [已啟用]。 如果 [MetricsReportingEnabled](#metricsreportingenabled) 或 [ SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 未設定或已停用，將不會將此資料傳送到 Microsoft。
                                                                                                                                                                                

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上或者透過 MDM 管理或透過 MCX 加入網域的 macOS 執行個體上取得。

  
  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：MetricsReportingEnabled
  - GP 名稱：啟用使用方式和當機相關的資料報告 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：MetricsReportingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：MetricsReportingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NativeWindowOcclusionEnabled
  #### 啟用原生視窗遮蔽
  
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
  在 Microsoft Edge 中啟用原生視窗遮蔽。

如果啟用此設定，為了降低 CPU 和耗電量，Microsoft Edge 將偵測視窗何時被其他視窗覆蓋，並將暫停工作繪製像素。

如果停用此設定，則 Microsoft Edge 無法偵測某個視窗是否被其他視窗遮蓋。

如果將此原則保留為未設定，則會啟用視窗隱藏偵測。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NativeWindowOcclusionEnabled
  - GP 名稱：啟用原生視窗遮蔽
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NativeWindowOcclusionEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### NavigationDelayForInitialSiteListDownloadTimeout
  #### 針對企業模式網站清單，設定索引標籤瀏覽逾時延遲
  
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
  可讓您設定適於 Microsoft Edge 索引標籤等候瀏覽的逾時設定 (以秒為單位) ，直到瀏覽器完成下載初始的 [企業模式網站清單] 為止。

此設定可與下列內容結合使用：將[InternetExplorerIntegrationLevel](#internetexplorerintegrationlevel) 設為 'IEMode' 及 [InternetExplorerIntegrationSiteList](#internetexplorerintegrationsitelist) 原則，其中至少擁有清單中的一個項目，並將 [DelayNavigationsForInitialSiteListDownload](#delaynavigationsforinitialsitelistdownload) 設為「All eligible navigations」(1)。

若要下載 [企業模式網站清單]，索引標籤的等待時間不會長於此逾時設定。 如果瀏覽器在逾時設定到期時並未完成下載 [企業模式網站清單]，Microsoft Edge 索引標籤仍會繼續瀏覽。 逾時設定的數值應少於 20 秒且多於 1 秒。

若將此原則中的逾時設置設成大於 2 秒的預設值，系統會在 2 秒之後向使用者顯示資訊列。 資訊列包含可讓使用者在等候 [企業模式網站清單] 下載完成時停止等候的按鈕。

如果未設定此原則，系統將會使用逾時設置的預設值 (2 秒)。 此預設值可會在未來進行變更。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NavigationDelayForInitialSiteListDownloadTimeout
  - GP 名稱：針對 [企業模式網站清單]，設定索引標籤瀏覽逾時延遲
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NavigationDelayForInitialSiteListDownloadTimeout
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x0000000a
```


  

  [回到頁首](#microsoft-edge---policies)

  ### NetworkPredictionOptions
  #### 啟用網路預測
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  啟用網路預測，並防止使用者變更此設定。

這會控制 DNS 預先擷取、TCP 和 SSL 預先連線，以及網頁的預先轉譯。

如果未設定此原則，則會啟用網路預測，但使用者可以變更它。

原則選項對應：

* NetworkPredictionAlways (0) = 預測任何網路連線上的網路動作

* NetworkPredictionWifiOnly (1) = 不支援，如果使用這個值，系統會將其視為 '預測任何網路連線上的網路動作' (0) 之設定。

* NetworkPredictionNever (2) = 不預測任何網路連線上的網路動作

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NetworkPredictionOptions
  - GP 名稱：啟用網路預測
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：NetworkPredictionOptions
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：NetworkPredictionOptions
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### NonRemovableProfileEnabled
  #### 設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  此原則會決定使用者是否可以移除使用使用者的公司或學校帳戶自動登入的 Microsoft Edge 設定檔。

如果啟用此原則，則會使用使用者的公司或學校帳戶在 Windows 上建立非可移除的設定檔。 無法將此設定檔登出或移除。

如果停用或未設定此原則，則在 Windows 上使用使用者的公司或學校帳戶自動登入的設定檔可由使用者登出或移除。

如果想要設定瀏覽器登入，請使用 [BrowserSignin](#browsersignin) 原則。

此原則僅可在已加入 Microsoft Active Directory 網域的 Windows 執行個體上、已註冊裝置管理的 Windows 10 專業版或企業版執行個體上取得。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：NonRemovableProfileEnabled
  - GP 名稱：設定使用者是否一律擁有其公司或學校帳戶自動登入的預設設定檔
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：NonRemovableProfileEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  


 
   
 

   
  

   

   

  
 
  
 

  
   

   
  
   
   
  
   
 
   
   
   
  
 
 
   
 
   


  
  
   
 
 
   
  

 
  [回到頁首](#microsoft-edge---policies)

  ### OverrideSecurityRestrictionsOnInsecureOrigin
  #### 控制不安全來源中安全性限制套用的地方
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定不安全來源的安全性限制不適用的來源 (URL) 的清單或主機名稱模式 (例如 "*.contoso.com")。

此原則可讓您為無法部署 TLS 的舊版應用程式指定允許的來源，或為內部網頁開發設定分段伺服器，使得開發人員不需在分段伺服器上部署 TLS，即可測試需要安全內容的功能。 此原則也可以防止來源在 omnibox 中被標示為「不安全」。

在此原則中設定 URL 清單，與將命令列旗標 '--unsafely-treat-insecure-origin-as-secure' 設定為相同 URL 以逗號分隔的清單具有相同效果。 如果啟用此原則，則會覆寫命令列旗標。

如需有關安全內容的詳細資訊，請參閱 https://www.w3.org/TR/secure-contexts/。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：OverrideSecurityRestrictionsOnInsecureOrigin
  - GP 名稱：控制不安全來源中安全性限制套用的地方
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\1 = http://testserver.contoso.com/
SOFTWARE\Policies\Microsoft\Edge\OverrideSecurityRestrictionsOnInsecureOrigin\2 = *.contoso.com

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：OverrideSecurityRestrictionsOnInsecureOrigin
  - 範例值：
``` xml
<array>
  <string>http://testserver.contoso.com/</string>
  <string>*.contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PaymentMethodQueryEnabled
  #### 允許網站查詢可用的付款方式
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  允許您設定網站是否可以檢查使用者是否已儲存付款條件。

如果停用此原則，使用 PaymentRequest.canMakePayment 或 PaymentRequest.hasEnrolledInstrument API 的網站會收到通知，告知沒有可用的付款方式。

如果啟用此原則或未設定此原則，則網站可以檢查使用者是否已儲存付款條件。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PaymentMethodQueryEnabled
  - GP 名稱：允許網站查詢可用的付款方式
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PaymentMethodQueryEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PaymentMethodQueryEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PersonalizationReportingEnabled
  #### 透過傳送瀏覽歷程記錄至 Microsoft，允許廣告、搜尋及新聞個人化
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  此原則可防止 Microsoft 收集使用者的 Microsoft Edge 瀏覽歷程記錄，以用於個人化廣告、搜尋、新聞及其他 Microsoft 服務。

只有擁有 Microsoft 帳戶的使用者才能使用此設定。 子帳戶或企業帳戶無法使用此設定。

如果停用此原則，則使用者無法變更或覆寫設定。 如果啟用或未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PersonalizationReportingEnabled
  - GP 名稱：透過傳送瀏覽歷程記錄至 Microsoft，允許廣告、搜尋及新聞個人化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PersonalizationReportingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PersonalizationReportingEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PinningWizardAllowed
  #### 允許 [釘選到工作列精靈]
  
  
  #### 支援的版本：
  - Windows 上，版本 80 或更新版本

  #### 說明
  Microsoft Edge 使用 [釘選到工作列] 精靈來協助使用者將建議的網站釘選到工作列。 [釘選到工作列] 精靈功能預設會啟用，且可供使用者透過 [設定及其他] 功能表存取。

如果啟用此原則或未設定，則使用者可以從 [設定] 和 [更多] 功能表中呼叫 [釘選到工作列] 精靈。 也可以透過通訊協定啟動來呼叫精靈。

如果停用此原則，則會停用功能表中的 [釘選到工作列] 精靈，且無法再透過通訊協定啟動來呼叫。

沒有可用來啟用或停用 [釘選到工作列] 精靈的使用者設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PinningWizardAllowed
  - GP 名稱：允許 [釘選到工作列精靈]
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PinningWizardAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### ProactiveAuthEnabled
  #### 啟用主動式驗證
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓您設定是否要開啟主動式驗證。

如果啟用此原則，則 Microsoft Edge 會嘗試使用 Microsoft 服務主動驗證登入使用者的身分。 Microsoft Edge 會定期檢查線上服務，以取得包含控管如何執行此動作之設定的更新資訊清單。

如果停用此原則，則 Microsoft Edge 不會嘗試使用 Microsoft 服務主動驗證登入使用者的身分。 Microsoft Edge 不再會檢查線上服務是否有包含用於執行此動作之設定的更新資訊清單。

如果未設定此原則，則會開啟主動式驗證。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ProactiveAuthEnabled
  - GP 名稱：啟用主動式驗證
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ProactiveAuthEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ProactiveAuthEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PromotionalTabsEnabled
  #### 啟用全分頁促銷內容
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制全分頁促銷或教育內容的呈現。 此設定可控制能夠協助使用者登入 Microsoft Edge、選擇其預設瀏覽器，或了解產品功能的歡迎頁面的呈現方式。

如果啟用此原則 (設定為 true) 或未設定，則 Microsoft Edge 可以向使用者顯示完整的索引標籤內容，以提供產品資訊。

如果您停用此原則 (設為 false)，則 Microsoft Edge 無法向使用者顯示完整的索引標籤內容。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PromotionalTabsEnabled
  - GP 名稱：啟用全分頁促銷內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PromotionalTabsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PromotionalTabsEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### PromptForDownloadLocation
  #### 詢問下載檔案的儲存位置
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定是否要在下載之前詢問儲存檔案的位置。

如果啟用此原則，則會在下載之前詢問使用者儲存每個檔案的位置；如果未設定，則檔案會自動儲存到預設位置，而不會詢問使用者。

如果未設定此原則，則使用者將可以變更此設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：PromptForDownloadLocation
  - GP 名稱：詢問下載檔案的儲存位置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：PromptForDownloadLocation
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：PromptForDownloadLocation
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### QuicAllowed
  #### 允許 QUIC 通訊協定
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許在 Microsoft Edge 中使用 QUIC 通訊協定。

如果啟用此原則或未設定，則會允許 QUIC 通訊協定。

如果停用此原則，則會封鎖 QUIC 通訊協定。

QUIC 是傳輸層網路通訊協定，可改善目前使用 TCP 的 Web 應用程式效能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：QuicAllowed
  - GP 名稱：允許 QUIC 通訊協定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：QuicAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：QuicAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RelaunchNotification
  #### 通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  通知使用者他們必須將 Microsoft Edge 重新啟動，才能套用擱置中的更新。

如果未設定此原則，則 Microsoft Edge 會在頂端功能表列的最右側加上回收圖示，提示使用者重新啟動瀏覽器以套用更新。

如果啟用此原則，並將其設定為 '建議'，則會出現重複的警告，提示使用者建議重新開機。 使用者可以關閉此警告，並將重新開機延遲。

如果將原則設定為 '必要'，會出現重複的警告，提示使用者當通知期間過後，瀏覽器將會自動重新啟動。 預設期間為七天。 您可以使用 [RelaunchNotificationPeriod](#relaunchnotificationperiod) 原則來設定此期間。

使用者的工作階段會在瀏覽器重新啟動後還原。

原則選項對應：

* 建議 (1) = 建議 - 向使用者顯示重複的提示，指出建議重新啟動

* 必要 (2) = 必要 - 向使用者顯示重複的提示，指出必須重新啟動

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RelaunchNotification
  - GP 名稱：通知使用者建議或需要重新啟動瀏覽器，以套用擱置中的更新
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RelaunchNotification
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RelaunchNotification
  - 範例值：
``` xml
<integer>1</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RelaunchNotificationPeriod
  #### 設定更新通知的時間週期
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  讓您設定時間期間 (以毫秒為單位)，經過此時間後便通知使用者必須重新啟動 Microsoft Edge，才能套用擱置中的更新。

在此時間期間內，使用者將會重複收到需要更新的通知。 在 Microsoft Edge 中，經過通知期間的三分之一後，應用程式功能表會變更，以指出需要重新啟動。 此通知會在經過通知期間的三分之二後變更色彩，並在經過整個通知期間後再次變更色彩。 由 [RelaunchNotification](#relaunchnotification) 原則啟用的額外通知會遵循此相同的排程。

如果未設定，則會使用預設的 604800000 毫秒 (一週)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RelaunchNotificationPeriod
  - GP 名稱：設定更新通知的時間週期
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RelaunchNotificationPeriod
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x240c8400
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RelaunchNotificationPeriod
  - 範例值：
``` xml
<integer>604800000</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RendererCodeIntegrityEnabled
  #### 啟用轉譯器程式碼完整性
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  如果啟用或未設定此原則，則會啟用轉譯器程式碼完整性。 只有當必須在 Microsoft Edge 的轉譯器處理程序內執行的協力廠商軟體發生的相容性問題時，才應該停用此原則。

停用此原則會對 Microsoft Edge 的安全性和穩定性造成不利影響，因為會允許未知且可能有害的程式碼在 Microsoft Edge 的轉譯器處理程序內載入。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RendererCodeIntegrityEnabled
  - GP 名稱：啟用轉譯器程式碼完整性
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RendererCodeIntegrityEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### RequireOnlineRevocationChecksForLocalAnchors
  #### 指定本機信賴起點是否需要線上 OCSP/CRL 檢查
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  控制是否需要線上撤銷檢查 (OCSP/CRL 檢查)。 如果 Microsoft Edge 無法取得撤銷狀態資訊，則會將這些憑證視為已撤銷 (「封鎖性失敗」)。

如果啟用此原則，則 Microsoft Edge 一律會針對成功驗證且由本機安裝的 CA 憑證簽署的伺服器憑證執行撤銷檢查。

如果未設定或停用此原則，則 Microsoft Edge 會使用現有的線上撤銷檢查設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RequireOnlineRevocationChecksForLocalAnchors
  - GP 名稱：指定本機信賴起點是否需要線上 OCSP/CRL 檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RequireOnlineRevocationChecksForLocalAnchors
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  

  [回到頁首](#microsoft-edge---policies)

  ### ResolveNavigationErrorsUseWebService
  #### 啟用使用 Web 服務來解決導覽錯誤
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許 Microsoft Edge 向 Web 服務發出無資料連線，以便在旅館和機場 Wi-Fi 之類情況下探測網路的連線能力。

如果啟用此原則，則會使用 Web 服務來進行網路連線測試。

如果停用此原則，則 Microsoft Edge 會使用原生 API 來嘗試解決網路連線和瀏覽問題。

**注意**：除了在 Windows 8 和更新版本的 Windows 上，Microsoft Edge *一律*會使用本機 API 來解決連線問題。

如果未設定此原則，則 Microsoft Edge 會遵守 edge://settings/privacy 的 [服務] 底下所設定的使用者喜好設定。
具體來說，有一個使用者可以開啟或關閉的 [使用網頁服務協助您解決瀏覽錯誤]**** 切換。 請注意，如果已啟用此原則 (ResolveNavigationErrorsUseWebService)，[使用網頁服務協助您解決瀏覽錯誤]**** 設定會開啟，但使用者無法使用切換來變更設定。 如果已停用此原則，則 [使用網頁服務協助您解決瀏覽錯誤]**** 設定會關閉，且使用者無法使用切換來變更設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ResolveNavigationErrorsUseWebService
  - GP 名稱：啟用使用 Web 服務來解決導覽錯誤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：ResolveNavigationErrorsUseWebService
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ResolveNavigationErrorsUseWebService
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RestrictSigninToPattern
  #### 限制哪些帳戶可用為 Microsoft Edge 主要帳戶
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  決定可以將哪些帳戶設為 Microsoft Edge 中的瀏覽器主要帳戶 (在同步選擇加入流程中選取的帳戶)。

如果使用者嘗試使用不符合此模式的使用者名稱設定瀏覽器主要帳戶，則會封鎖使用者並顯示適當的錯誤訊息。 您可以使用此模式的 Perl 樣式規則運算式，將此原則設定為符合多個帳戶。 請注意，模式比對會區分大小寫。 如需使用的規則運算式規則之詳細資訊，請參閱 https://go.microsoft.com/fwlink/p/?linkid=2133903

如果未設定此原則或將它保留為空白，則使用者可以將任何帳戶設定為 Microsoft Edge 中的瀏覽器主要帳戶。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RestrictSigninToPattern
  - GP 名稱：限制哪些帳戶可用為 Microsoft Edge 主要帳戶
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RestrictSigninToPattern
  - 值類型：REG_SZ
  ##### 範例值：
```
.*@contoso.com
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RestrictSigninToPattern
  - 範例值：
``` xml
<string>.*@contoso.com</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### RoamingProfileLocation
  #### 設定漫遊設定檔目錄
  
  
  #### 支援的版本：
  - Windows 上，版本 85 或更新版本

  #### 說明
  設定用來儲存設定檔快取複本的目錄。

Microsoft Edge 會使用已提供的目錄，儲存設定檔的快取複本，若您在啟用此原則時同時也啟用[RoamingProfileSupportEnabled](#roamingprofilesupportenabled)原則。 若您停用或未設定 [RoamingProfileSupportEnabled](#roamingprofilesupportenabled) 原則，系統將不會使用儲存在此原則中的值。

如欲知道您可使用的變數清單，請參照[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

如果您並未設定此原則，系統將會使用預設的快取設定檔路徑。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RoamingProfileLocation
  - GP 名稱：設定快取設定檔目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RoamingProfileLocation
  - 值類型：REG_SZ
  ##### 範例值：
```
${roaming_app_data}\edge-profile
```


           
              
      
    
             
   
  

  [回到頁首](#microsoft-edge---policies)

  ### RoamingProfileSupportEnabled
  #### 啟用 Microsoft Edge 設定檔資料的快取副本
  
  
  #### 支援的版本：
  - Windows 上，版本 85 或更新版本

  #### 說明
  啟用此原則以使用 Windows 上的快取設定檔。 儲存在 Microsoft Edge 設定檔 ([我的最愛] 和 [喜好設定]) 中的設定，也會儲存至 [漫遊使用者設定檔] 資料夾中儲存的檔案 (或由系統管理員透過 [RoamingProfileLocation](#roamingprofilelocation) 原則所指定的位置)。

如果您停用或未設定此原則，系統只會使用標準本機設定檔。

[SyncDisabled](#syncdisabled) 原則會停用所有資料同步處理、覆寫原則。

如需使用漫遊使用者設定檔的詳細資訊，請參閱 https://docs.microsoft.com/windows-server/storage/folder-redirection/deploy-roaming-user-profiles。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RoamingProfileSupportEnabled
  - GP 名稱：啟用 Microsoft Edge 設定檔資料的快取副本
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RoamingProfileSupportEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


           
              
      
    
    
   
  

  [回到頁首](#microsoft-edge---policies)

  ### RunAllFlashInAllowMode
  #### 將 Adobe Flash 內容設定延伸至所有內容
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  如果啟用此原則，在內容設定中設為允許 Adobe Flash 的網站中內嵌的所有 Adobe Flash 內容 (無論是由使用者或企業原則設定) 將會執行。 這包含來自其他來源和/或小型內容的內容。

若要控制允許哪些網站執行 Adobe Flash，請參閱 [DefaultPluginsSetting](#defaultpluginssetting)、[PluginsAllowedForUrls](#pluginsallowedforurls) 和 [PluginsBlockedForUrls](#pluginsblockedforurls) 原則中的規格。

如果停用或未設定此原則，則可能會封鎖來自其他來源 (以上提及的三個原則中未指定的網站) 的 Adobe Flash 或少量內容。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：RunAllFlashInAllowMode
  - GP 名稱：將 Adobe Flash 內容設定延伸至所有內容
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：RunAllFlashInAllowMode
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：RunAllFlashInAllowMode
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SSLErrorOverrideAllowed
  #### 允許使用者從 HTTPS 警告頁面繼續進行
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  當使用者造訪含有 SSL 錯誤的網站時，Microsoft Edge 會顯示警告頁面。

如果啟用或未設定 (預設) 此原則，則使用者可以點選這些警告頁面。

如果停用此原則，則會封鎖使用者，使其無法點選任何警告頁面。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SSLErrorOverrideAllowed
  - GP 名稱：允許使用者從 HTTPS 警告頁面繼續進行
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SSLErrorOverrideAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SSLErrorOverrideAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SSLVersionMin
  #### 已啟用最低 TLS 版本
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定支援的最低 SSL 版本。 如果未設定此原則，則 Microsoft Edge 會使用預設的最低版本，TLS 1.0。

如果啟用此原則，則可以將最低版本設定為下列其中一個值：'TLSv1'、'TLSv1.1' 或 'TLSv1.2'。 設定時，Microsoft Edge 不會使用低於指定版本的任何 SSL/TLS 版本。 任何無法辨識的值都會被忽略。

原則選項對應：

* TLSv1 (tls1) = TLS 1.0

* TLSv1.1 (tls1.1) = TLS 1.1

* TLSv1.2 (tls1.2) = TLS 1.2

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SSLVersionMin
  - GP 名稱：已啟用最低 TLS 版本
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SSLVersionMin
  - 值類型：REG_SZ
  ##### 範例值：
```
tls1
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SSLVersionMin
  - 範例值：
``` xml
<string>tls1</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SaveCookiesOnExit
  #### 在 Microsoft Edge 關閉時儲存 Cookie
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 86 或更新版本

  #### 說明
  啟用此原則時，瀏覽器關閉時，指定的 Cookie 集合不會遭到刪除。 這個原則只有在下列情況下才有效：
- 在 [設定/隱私權與服務/清除瀏覽資料] 中設定 [Cookies 及其他網站資料] 切換按鈕為關閉或
- 已啟用原則 [ClearBrowsingDataOnExit](#clearbrowsingdataonexit) 或
- 原則 [DefaultCookiesSetting](#defaultcookiessetting) 設定為 ‘在工作階段期間保留 Cookie’。

您可以根據 URL 模式定義要在多個工作階段之間保留 Cookie 的網站清單。

請注意：使用者仍然可以編輯 Cookie 網站清單，以新增或移除 URL。 不過，他們無法移除由系統管理員新增的 URL。

如果您啟用此原則，瀏覽器關閉時，Cookie 清單就不會被清除。

如果您停用或未設定此原則，則會使用使用者的個人設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SaveCookiesOnExit
  - GP 名稱：在 Microsoft Edge 關閉時儲存 Cookie
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\SaveCookiesOnExit\2 = [*.]contoso.edu

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SaveCookiesOnExit
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>[*.]contoso.edu</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SavingBrowserHistoryDisabled
  #### 停用儲存瀏覽器歷程記錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  停用儲存瀏覽器歷程記錄，並防止使用者變更此設定。

如果啟用此原則，則不會儲存瀏覽歷程記錄。 這也會停用索引標籤同步。

如果停用或未設定此原則，則會儲存瀏覽歷程記錄。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SavingBrowserHistoryDisabled
  - GP 名稱：停用儲存瀏覽器歷程記錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SavingBrowserHistoryDisabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SavingBrowserHistoryDisabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ScreenCaptureAllowed
  #### 允許或拒絕螢幕擷取畫面
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  如果啟用此原則或未設定此原則，則網頁可使用螢幕共用 API (例如 getDisplayMedia () 或桌面擷取擴充功能 API) 來進行螢幕擷取。
如果停用此原則，則對螢幕共用 API 的呼叫將會失敗。 例如，如果您正在使用網路線上會議，視訊或螢幕共用將無法運作。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ScreenCaptureAllowed
  - GP 名稱：允許或拒絕螢幕擷取畫面
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ScreenCaptureAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ScreenCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ScrollToTextFragmentEnabled
  #### 啟用捲動至在 URL 片段中指定的文字
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  此功能會超連結和網址列 URL 導覽以網頁上的特定文字為目標，這會在網頁載入完成之後進行捲動。

如果啟用或未設定此原則，則會啟用透過 URL 將網頁捲動至特定文字片段的功能。

如果停用此原則，則會停用透過 URL 將網頁捲動至特定文字片段的功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ScrollToTextFragmentEnabled
  - GP 名稱：啟用捲動至在 URL 片段中指定的文字
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ScrollToTextFragmentEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ScrollToTextFragmentEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SearchSuggestEnabled
  #### 啟用搜尋建議
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 Microsoft Edge 的網址列和自動建議清單中啟用網頁搜尋建議，並防止使用者變更此原則。

如果啟用此原則，則會使用 Web 搜尋建議。

如果停用此原則，則永遠不會使用 Web 搜尋建議，不過仍會顯示本機歷程記錄和本機我的最愛建議。 如果停用此原則，則不會在對 Microsoft 的遙測中包含所輸入的字元和所造訪的 URL。

如果將此原則保留為未設定，則會啟用搜尋建議，但使用者可以變更。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SearchSuggestEnabled
  - GP 名稱：啟用搜尋建議
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SearchSuggestEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SearchSuggestEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SecurityKeyPermitAttestation
  #### 不需要權限即可使用直接存取安全性金鑰證明的網站或網域
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定要求來自安全性金鑰的證明憑證時，不需要明確使用者權限的網站和網域。 此外，傳送信號給安全性金鑰，指出它可以使用個別證明。 如果沒有此動作，每次網站要求安全性金鑰的證明時，即會提示使用者。

網站 (例如 https://contoso.com/some/path) 僅符合 U2F appID。 網域 (例如 contoso.com) 僅符合 webauthn RP 識別碼。 若要涵蓋特定網站的 U2F 和 webauthn API，您需要列出 appID URL 和網域。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SecurityKeyPermitAttestation
  - GP 名稱：不需要權限即可使用直接存取安全性金鑰證明的網站或網域
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SecurityKeyPermitAttestation\1 = https://contoso.com

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SecurityKeyPermitAttestation
  - 範例值：
``` xml
<array>
  <string>https://contoso.com</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SendIntranetToInternetExplorer
  #### 將所有內部網路網站傳送到 Internet Explorer
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  如需有關設定 Internet Explorer 模式的最佳體驗的指導方針，請參閱[https://go.microsoft.com/fwlink/?linkid=2094210](https://go.microsoft.com/fwlink/?linkid=2094210)

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SendIntranetToInternetExplorer
  - GP 名稱：將所有內部網路網站傳送到 Internet Explorer
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SendIntranetToInternetExplorer
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)

  ### SendSiteInfoToImproveServices
  #### 傳送網站資訊以改善 Microsoft 服務 (已過時)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
   
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  此原則已被取代。 目前支援，但將在 Microsoft Edge 版本 89 中過時。 這個原則會由新原則取代：Windows 7、Windows 8 和 macOS 的 [DiagnosticData](#diagnosticdata)。 這項原則會由 Win 10 上的允許遙測取代 ([https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569))。

此原則允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善服務 (如搜尋)。

   
啟用此原則，以傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 停用此原則，以不要傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

在 Windows 10 上，如果未設定此原則，則 Microsoft Edge 將預設為使用 Windows 診斷資料設定。 如果啟用此原則，而且 Windows 診斷資料設定設為「完整」時，Microsoft Edge 將僅傳送有關在 Microsoft Edge 中所造訪網站的資訊。 如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。 深入了解 Windows 診斷資料設定：[https://go.microsoft.com/fwlink/?linkid=2099569](https://go.microsoft.com/fwlink/?linkid=2099569)

在 Windows 7、Windows 8 和 macOS 上，此原則會控制所造訪網站相關資訊的傳送。 如果未設定此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

若要啟用此原則，[MetricsReportingEnabled](#metricsreportingenabled) 必須設定為 [已啟用]。 如果 [SendSiteInfoToImproveServices](#sendsiteinfotoimproveservices) 或 [MetricsReportingEnabled](#metricsreportingenabled) 未設定或已停用，將不會將此資料傳送到 Microsoft。
                                                                                                                                                                            

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SendSiteInfoToImproveServices
  - GP 名稱：傳送網站資訊以改善 Microsoft 服務 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SendSiteInfoToImproveServices
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SendSiteInfoToImproveServices
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### ShowOfficeShortcutInFavoritesBar
  #### 在 [我的最愛] 列中顯示 Microsoft Office 捷徑
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  指定是否要在我的最愛列中加入 Office.com 的捷徑。 針對登入 Microsoft Edge 的使用者，捷徑會帶使用者前往其 Microsoft Office 應用程式和文件。

如果啟用或未設定此原則，則使用者可以透過變更我的最愛工具列內容功能表中的切換，來選擇是否要查看捷徑。

如果停用原則，就不會顯示捷徑。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：ShowOfficeShortcutInFavoritesBar
  - GP 名稱：在 [我的最愛] 列中顯示 Microsoft Office 捷徑
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：ShowOfficeShortcutInFavoritesBar
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：ShowOfficeShortcutInFavoritesBar
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SignedHTTPExchangeEnabled
  #### 啟用 Signed HTTP Exchange (SXG) 支援
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  啟用 Signed HTTP Exchange (SXG) 的支援。

如果未設定或已啟用此原則，則 Microsoft Edge 會接受將網頁內容做為 Signed HTTP Exchange。

如果將此原則設為已停用，則無法載入 Signed HTTP Exchange。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SignedHTTPExchangeEnabled
  - GP 名稱：啟用 Signed HTTP Exchange (SXG) 支援
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SignedHTTPExchangeEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SignedHTTPExchangeEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SitePerProcess
  #### 為每個網站啟用網站隔離
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  
'SitePerProcess' 原則可用於防止使用者選擇退出隔離所有網站的預設行為。 請注意，您也可以使用 [IsolateOrigins](#isolateorigins) 原則來隔離其他更精細的來源。
如果啟用此原則，則使用者將無法選擇退出每個網站都是以自己的處理程序執行的預設行為。
如果您停用或未設定此原則，使用者可以選擇退出網站隔離。  (例如，使用 edge://flags 中的 [停用網站隔離] 項目。) 停用原則或未設定原則，並無法關閉網站隔離。


  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SitePerProcess
  - GP 名稱：為每個網站啟用網站隔離
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SitePerProcess
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SitePerProcess
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SpellcheckEnabled
  #### 啟用拼字檢查
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  如果啟用或未設定此原則，則使用者可以使用拼字檢查。

如果停用此原則，則使用者無法使用拼字檢查，且會停用 [SpellcheckLanguage](#spellchecklanguage) 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SpellcheckEnabled
  - GP 名稱：啟用拼字檢查
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SpellcheckEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SpellcheckEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SpellcheckLanguage
  #### 啟用特定拼字檢查語言
  
  
  #### 支援的版本：
  - Windows 上，版本 77 或更新版本

  #### 說明
  啟用不同語言的拼字檢查。 將忽略您指定、無法辨識的任何語言。

如果啟用此原則，則會針對指定的語言及使用者啟用的任何語言啟用拼字檢查。

如果未設定或停用此原則，則不會對使用者的拼字檢查喜好設定進行任何變更。

如果 [SpellcheckEnabled](#spellcheckenabled) 原則為已停用，則此原則沒有作用。

如果在 'SpellcheckLanguage' 和 [SpellcheckLanguageBlocklist](#spellchecklanguageblocklist) 原則中同時包含某個語言，則會啟用該拼字檢查語言。

支援的語言為：af、bg、ca、cs、cy、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SpellcheckLanguage
  - GP 名稱：啟用特定拼字檢查語言
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\1 = fr
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguage\2 = es

```


  

  [回到頁首](#microsoft-edge---policies)

  ### SpellcheckLanguageBlocklist
  #### 強制停用拼字檢查語言
  
  
  #### 支援的版本：
  - Windows 上，版本 78 或更新版本

  #### 說明
  強制停用拼字檢查語言。 該清單中無法辨識的語言將會被忽略。

如果啟用此原則，則會針對指定的語言停用拼字檢查。 使用者仍可以為清單中沒有的語言啟用或停用拼字檢查。

如果未設定此原則或停用，則不會對使用者的拼字檢查喜好設定進行任何變更。

如果 [SpellcheckEnabled](#spellcheckenabled) 原則設為已停用，則此原則沒有作用。

如果在 [SpellcheckLanguage](#spellchecklanguage) 和 'SpellcheckLanguageBlocklist' 原則中同時包含某個語言，則會啟用該拼字檢查語言。

目前支援的語言為：af、bg、ca、cs、da、de、el、en-AU、en-CA、en-GB、en-US、es、es-419、es-AR、es-ES、es-MX、es-US、et、fa、fo、fr、he、hi、hr、hu、id、it、ko、lt、lv、nb、nl、pl、pt-BR、pt-PT、ro、ru、sh、sk、sl、sq、sr、sv、ta、tg、tr、uk、vi。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SpellcheckLanguageBlocklist
  - GP 名稱：強制停用拼字檢查語言
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\1 = fr
SOFTWARE\Policies\Microsoft\Edge\SpellcheckLanguageBlocklist\2 = es

```


  

  [回到頁首](#microsoft-edge---policies)

  ### StricterMixedContentTreatmentEnabled
  #### 針對混合內容啟用更嚴格的處理 (已淘汰)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 81 或更新版本

  #### 說明
  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與嚴格混合內容的處理不一致時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本 85 中使用。

此原則可控制在瀏覽器中處理混合內容 (HTTPS 網站中的 HTTP 內容) 的方式。

如果將此原則設定為 true 或未設定，音訊和視訊混合內容將會自動升級為 HTTPS (也就是說，URL 將會重寫為 HTTPS，且如果資源無法透過 HTTPS 使用，也不會遞補)，且會在影像混合內容的 URL 列中顯示「不安全」警告。

如果將原則設定為 false，則會停用音訊和視訊的自動升級，且不會顯示影像的警告。

此原則不會影響音訊、視訊和影像以外的其他類型混合內容。


  
  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：StricterMixedContentTreatmentEnabled
  - GP 名稱：針對混合內容啟用更嚴格的處理 (已淘汰)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：StricterMixedContentTreatmentEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：StricterMixedContentTreatmentEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SuppressUnsupportedOSWarning
  #### 隱藏不支援的 OS 警告
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  隱藏當 Microsoft Edge 於已不再受支援的電腦或作業系統上執行時將會顯示的警告。

如果此原則為 false 或未設定，則會在這類不受支援的電腦或作業系統中顯示警告。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SuppressUnsupportedOSWarning
  - GP 名稱：隱藏不支援的 OS 警告
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：SuppressUnsupportedOSWarning
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SuppressUnsupportedOSWarning
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SyncDisabled
  #### 透過 Microsoft 同步服務停用資料同步
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  停用 Microsoft Edge 中的資料同步。 此原則也會防止顯示同步同意提示。


 
如果未設定此原則或將它套用為建議，則使用者將可以開啟或關閉同步。 如果將此原則套用為強制，則使用者將無法開啟同步。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SyncDisabled
  - GP 名稱：透過 Microsoft 同步服務停用資料同步
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：SyncDisabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SyncDisabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### SyncTypesListDisabled
  #### 設定同步服務將排除的類型清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 83 或更新版本

  #### 說明
  如果啟用此原則，則所有指定的資料類型將會從同步中排除。 此原則可用來限制上傳至 Microsoft Edge 同步服務的資料類型。

您可以針對此原則提供下列其中一個資料類型：「favorites」、「settings」、「passwords」、「addressesAndMore」、「extensions」、「history」和 「collections」。 請注意，這些資料類型名稱需區分大小寫。

使用者將無法覆寫已停用的資料類型。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：SyncTypesListDisabled
  - GP 名稱：設定同步服務將排除的類型清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\SyncTypesListDisabled\1 = favorites

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：SyncTypesListDisabled
  - 範例值：
``` xml
<array>
  <string>favorites</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TLS13HardeningForLocalAnchorsEnabled
  #### 啟用適於本機信賴起點的 TLS 1.3 安全性功能 (已過時)
  
  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 85 及之後的版本中運作。
  #### 支援的版本：
  - 在 Windows 和 macOS 上，版本 81 到 85

  #### 說明
  此原則已無法運作，因為其只是一種短期機制，目的是要讓企業有更多時間升級受影響的 Proxy。

此原則會控制 TLS 1.3 中可保護連線對抗降級攻擊的安全性功能。 它是回溯相容且不會影響與相容 TLS 1.2 伺服器或 Proxy 的連線。 不過，部分舊版 TLS 攔截 Proxy 具有實作缺陷，導致它們不相容。

如果啟用此原則或未設定，則 Microsoft Edge 將會針對所有連線啟用這些安全性保護。

如果停用此原則，則 Microsoft Edge 將針對使用本機安裝的 CA 憑證進行驗證的連線，停用這些安全性保護。 針對使用公開信任的 CA 憑證進行驗證的連線，這些保護一律會啟用。

                                                                                                                                                                                                                                                      

                                                                                                                                                                                                             

此原則可用來測試任何受影響的 Proxy，並進行升級。 受影響的 Proxy 預期會連線失敗，出現錯誤碼 ERR_TLS13_DOWNGRADE_DETECTED。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TLS13HardeningForLocalAnchorsEnabled
  - GP 名稱：針對本機信賴起點啟用 TLS 1.3 安全性功能 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TLS13HardeningForLocalAnchorsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TLS13HardeningForLocalAnchorsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TLSCipherSuiteDenyList
  #### 指定欲停用的 TLS 加密套件
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 85 或更新版本

  #### 說明
  設定 TLS 連線停用的加密套件清單。

若您設定此原則設定，在建立 TLS 連線時將不會使用已設定的加密套件清單。

若您未設定此原則，瀏覽器將會自選要使用的 TLS 加密套件。

若要停用加密套件值，請將其指定為16位的十六進位值。 這些值是由 Internet Assigned Numbers Authority (IANA) 登錄所指派。

TLS 1.3 須有 TLS 1.3 加密套件 TLS_AES_128_GCM_SHA256 (0x1301) ，且不可被此原則停用。

此原則不會影響 QUIC 式連線。 您可以透過 [QuicAllowed](#quicallowed) 原則關閉 QUIC。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TLSCipherSuiteDenyList
  - GP 名稱：指定欲停用的 TLS 加密套件
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\1 = 0x1303
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\2 = 0xcca8
SOFTWARE\Policies\Microsoft\Edge\TLSCipherSuiteDenyList\3 = 0xcca9

```


  #### Mac 資訊和設定
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

  ### TabFreezingEnabled
  #### 允許凍結背景索引標籤
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 79 或更新版本

  #### 說明
  控制 Microsoft Edge 是否可以凍結在背景中至少 5 分鐘的索引標籤。

凍結索引標籤會降低 CPU、電池和記憶體使用量。 Microsoft Edge 使用啟發學習法來避免凍結在背景中執行實用工作 (例如：顯示通知、播放音效和串流視訊) 的索引標籤。

如果啟用或未設定此原則，則在背景中至少 5 分鐘的索引標籤可能會遭到凍結。

如果停用此原則，則不會凍結任何索引標籤。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TabFreezingEnabled
  - GP 名稱：允許凍結背景索引標籤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TabFreezingEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TabFreezingEnabled
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TaskManagerEndProcessEnabled
  #### 啟用在瀏覽器工作管理員中結束處理程序
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  如果啟用或未設定此原則，則使用者可以在瀏覽器工作管理員中結束處理程序。 如果停用此原則，則使用者無法結束處理程序，且瀏覽器工作管理員中的 [結束處理程序] 按鈕會停用。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TaskManagerEndProcessEnabled
  - GP 名稱：啟用在瀏覽器工作管理員中結束處理程序
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TaskManagerEndProcessEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TaskManagerEndProcessEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TotalMemoryLimitMb
  #### 設定單一 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  設定開始捨棄索引標籤以節省記憶體之前，單一 Microsoft Edge 執行個體可以使用的記憶體數量。 索引標籤使用的記憶體將會釋出，且在切換至該索引標籤時，必須重新載入它。

如果啟用此原則，則瀏覽器將會在超過限制之後，開始捨棄索引標籤來節省記憶體。 不過，無法保證瀏覽器一律會在限制內執行。 低於 1024 的任何值都會進位為 1024。

如果未設定此原則，則瀏覽器只會在偵測到其電腦上的實際記憶體數量不足時才嘗試儲存記憶體。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TotalMemoryLimitMb
  - GP 名稱：設定單一個 Microsoft Edge 執行個體可以使用的記憶體容量限制 (MB)。
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TotalMemoryLimitMb
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000800
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TotalMemoryLimitMb
  - 範例值：
``` xml
<integer>2048</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TrackingPrevention
  #### 封鎖使用者的網頁瀏覽活動追蹤
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 78 或更新版本

  #### 說明
  讓您決定是否要封鎖網站，使其無法追蹤使用者的 Web 瀏覽活動。

如果停用此原則或未設定，則使用者可以設定自己的防止追蹤層級。

原則選項對應：
   
 

* TrackingPreventionOff (0) = 關閉 (無防止追蹤)

* TrackingPreventionBasic (1) = 基本 (封鎖有害的追蹤器，內容與廣告會進行個人化)

* TrackingPreventionBalanced (2) = 平衡 (封鎖有害的追蹤器以及來自使用者尚未造訪網站的追蹤器；內容與廣告的個人化程度較低)

* TrackingPreventionStrict (3) =嚴格 (封鎖有害的追蹤器以及來自所有網站的大部分追蹤器；內容與廣告的個人化程度最低。 網站的某些部分可能無法運作)

設定此原則時，請使用上述資訊。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 整數

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TrackingPrevention
  - GP 名稱：封鎖使用者的網頁瀏覽活動追蹤
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：TrackingPrevention
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000002
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TrackingPrevention
  - 範例值：
``` xml
<integer>2</integer>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### TranslateEnabled
  #### 啟用翻譯
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  在 Microsoft Edge 上啟用整合式 Microsoft 翻譯服務。

如果啟用此原則，則 Microsoft Edge 會透過在適當時顯示整合的翻譯飛出視窗，以及按滑鼠右鍵功能表中的翻譯選項，為使用者提供翻譯功能。

停用此原則可停用所有內建的翻譯功能。

如果未設定原則，則使用者可以選擇是否要使用翻譯功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：是
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：TranslateEnabled
  - GP 名稱：啟用翻譯
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：系統管理範本/Microsoft Edge - 預設設定 (使用者可以覆寫)/
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：SOFTWARE\Policies\Microsoft\Edge\Recommended
  - 數值名稱：TranslateEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：TranslateEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### URLAllowlist
  #### 定義受允許的 URL 清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許存取所列的 URL，做為 URL 封鎖清單的例外。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。

您可以使用此原則來對限制性封鎖清單開放例外。 例如，您可以在封鎖清單中包含 '*' 以封鎖所有要求，然後使用此原則來允許對受限的 URL 清單的存取權。 您可以使用此原則來開放特定配置、其他網域的子網域、連接埠或特定路徑的例外。

最特定的篩選會判斷是否已封鎖或允許某個 URL。 允許清單優先於封鎖清單。

此原則限制在 1000 個項目；後續的項目會被忽略。

此原則也可讓瀏覽器自動叫用註冊為通訊協定處理常式的外部應用程序，例如「tel:」或「ssh:」。

如果未設定此原則，則 [URLBlocklist](#urlblocklist) 原則的封鎖清單中沒有例外。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：URLAllowlist
  - GP 名稱：定義受允許的 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\URLAllowlist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\1 = contoso.com
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\2 = https://ssl.server.com
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\3 = hosting.com/good_path
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\4 = https://server:8080/path
SOFTWARE\Policies\Microsoft\Edge\URLAllowlist\5 = .exact.hostname.com

```


  #### Mac 資訊和設定
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

  ### URLBlocklist
  #### 封鎖存取 URL 清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 的模式，定義遭封鎖的網站清單 (您的使用者無法載入該清單)。

根據 [https://go.microsoft.com/fwlink/?linkid=2095322](https://go.microsoft.com/fwlink/?linkid=2095322) 來設定 URL 模式的格式。

您可以在 [URLAllowlist](#urlallowlist) 原則中定義例外。 這些原則限制在 1000 個項目；後續的項目會被忽略。

請注意，不建議封鎖內部 'edge://*' URL，這可能會導致意外的錯誤。

此原則無法防止頁面透過 JavaScript 動態更新。 例如，如果您封鎖 'contoso.com/abc'，則使用者仍可能可以造訪 'contoso.com'，並按一下連結來覽 'contoso.com/abc' (只要不重新整理頁面)。

如果未設定此原則，則不會封鎖任何 URL。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：URLBlocklist
  - GP 名稱：封鎖存取 URL 清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\URLBlocklist
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\1 = contoso.com
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\2 = https://ssl.server.com
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\3 = hosting.com/bad_path
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\4 = https://server:8080/path
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\5 = .exact.hostname.com
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\6 = file://*
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\7 = custom_scheme:*
SOFTWARE\Policies\Microsoft\Edge\URLBlocklist\8 = *

```


  #### Mac 資訊和設定
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

  ### UserAgentClientHintsEnabled
  #### 啟用使用者代理程式用戶端提示功能 (已過時)
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 86 或更新版本

  #### 說明
  此原則已遭取代，因為此原則只是一個短期機制，用於讓企業在發現其 Web 內容與使用者代理程式用戶端提示功能不一致時，可以有更多時間來更新其 Web 內容。 無法在 Microsoft Edge 版本 89 中使用。

啟用 [使用者代理程式用戶端提示] 功能時，會傳送提供使用者瀏覽器相關資訊 (例如瀏覽器版本) 和環境 (例如系統架構) 的細微要求標頭。

這是一項累加功能，但新的標頭可能會破壞某些網站，這些網站限制了要求可能包含某些字元。

如果您啟用或未設定此原則，則會啟用 [使用者代理程式用戶端提示] 功能。 如果您停用此原則，則無法使用此功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：UserAgentClientHintsEnabled
  - GP 名稱：啟用使用者代理程式用戶端提示功能 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 值名稱：UserAgentClientHintsEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：UserAgentClientHintsEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### UserDataDir
  #### 設定使用者資料目錄
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  設定用來儲存使用者資料的目錄。

如果啟用此原則，則 Microsoft Edge 會使用指定的目錄，而無論使用者是否已設定 '--user-data-dir' 命令列旗標。

如果未啟用此原則，則會使用預設的設定檔路徑，但使用者可以使用 '--user-data-dir' 旗標來覆寫它。 使用者可以在 edge://version/ 的「設定檔路徑」底下找到設定檔的目錄。

若要避免資料遺失或其他錯誤，請勿將此原則設定為磁碟區的根目錄或用於其他用途的目錄，因為 Microsoft Edge 會管理其內容。

如需可使用的變數清單，請參閱[https://go.microsoft.com/fwlink/?linkid=2095041](https://go.microsoft.com/fwlink/?linkid=2095041)。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：UserDataDir
  - GP 名稱：設定使用者資料目錄
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UserDataDir
  - 值類型：REG_SZ
  ##### 範例值：
```
${users}/${user_name}/Edge
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：UserDataDir
  - 範例值：
``` xml
<string>${users}/${user_name}/Edge</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### UserFeedbackAllowed
  #### 允許使用者意見反應
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  Microsoft Edge 使用 Edge 意見反應功能 (預設為啟用)，以允許使用者傳送意見反應、建議或客戶問卷調查，並報告有關瀏覽器的任何問題。 此外，使用者預設無法停用 (關閉) Edge 意見反應功能。

如果啟用此原則或未設定，則使用者可以叫用 Edge 意見反應。

如果停用此原則，則使用者無法叫用 Edge 意見反應。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：UserFeedbackAllowed
  - GP 名稱：允許使用者意見反應
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：UserFeedbackAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：UserFeedbackAllowed
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### VideoCaptureAllowed
  #### 允許或封鎖視訊擷取
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  控制網站是否可以擷取視訊。

如果已啟用或未設定 (預設)，則使用者會被詢問有關所有網站的視訊擷取存取權，在 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 原則清單中已設定 URL 的這些網站除外，這些網站不需提示就會授與存取權。

如果停用此原則，則不會提示使用者，且視訊擷取僅可供 [VideoCaptureAllowedUrls](#videocaptureallowedurls) 原則中設定的 URL 使用。

此原則會影響所有類型的視訊輸入，而不僅僅是內建的相機。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：VideoCaptureAllowed
  - GP 名稱：允許或封鎖視訊擷取
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：VideoCaptureAllowed
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000000
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：VideoCaptureAllowed
  - 範例值：
``` xml
<false/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### VideoCaptureAllowedUrls
  #### 無需要求權限即可存取視訊擷取裝置的網站
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  根據 URL 模式指定可使用視訊擷取裝置的網站，而不詢問使用者提供權限。 此清單中的模式會對照要求端 URL 的安全性來源進行比對。 如果符合，則網站會自動獲授與視訊擷取裝置的存取權。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：VideoCaptureAllowedUrls
  - GP 名稱：無需要求權限即可存取視訊擷取裝置的網站
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\1 = https://www.contoso.com/
SOFTWARE\Policies\Microsoft\Edge\VideoCaptureAllowedUrls\2 = https://[*.]contoso.edu/

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：VideoCaptureAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com/</string>
  <string>https://[*.]contoso.edu/</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WPADQuickCheckEnabled
  #### 設定 WPAD 最佳化
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  允許您關閉 Microsoft Edge 中的 WPAD (Web Proxy AutoDiscovery) 最佳化。

如果停用此原則，則會停用 WPAD 最佳化，這會讓瀏覽器等候 DNS 型 WPAD 伺服器較長的時間。

如果啟用或未設定該原則，則會啟用 WPAD 最佳化。

無論此原則是否已啟用或如何啟用，使用者皆無法變更 WPAD 最佳化設定。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WPADQuickCheckEnabled
  - GP 名稱：設定 WPAD 最佳化
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WPADQuickCheckEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WPADQuickCheckEnabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebAppInstallForceList
  #### 設定強制安裝 Web 應用程式的清單
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  指定以無訊息方式安裝、不需使用者互動且無法由使用者解除安裝或停用的網站清單。

原則中的每個清單項目都是含有下列成員的物件：
  - "url"，這是強制項目。 "url" 應該是要安裝之 Web 應用程式的 URL。

選用成員的值如下：
  - "launch_container" 應該是 "window" 或 "tab"，以指出 Web 應用程式安裝後將如何開啟。
  - 如果應該在 Windows 上建立桌面捷徑，則 "create_desktop_shortcut" 應為 true。

如果省略 "default_launch_container"，則應用程式預設會在索引標籤中開啟。 無論 "default_launch_container" 的值如何，使用者都可以變更應用程式將在其中開啟的容器。 如果省略 "create_desktop_shortcuts"，則不會建立任何桌面捷徑。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### Data Type:
  - Dictionary

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebAppInstallForceList
  - GP 名稱：設定強制安裝 Web 應用程式的清單
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebAppInstallForceList
  - 值類型：REG_SZ
  ##### 範例值：
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
  }
]
```


  #### Mac 資訊和設定
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
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebComponentsV0Enabled
  #### 在 M84 前，重新啟用 Web 元件 v0 API。
                       
        
  
  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### 支援的版本：
  - 在 Windows 和 macOS 上，版本 80 至 84

  #### 說明
  此原則無法運作，因為此原則允許您在 Microsoft Edge 版本 85 之前，選擇性地重新啟用這些功能。 Web 元件 v0 API (Shadow DOM v0、Custom Elements v0 和 HTML Imports) 已在 2018 年過時，且已預設在 Microsoft Edge 版本 M80 中開始停用。

如果將此原則設定為 True，則會為所有網站啟用網頁元件 v0 功能。

若您將此原則設定為 False 或未設定此原則，從 Microsoft Edge 版本 M80 開始，已預設停用 Web 元件 v0 功能。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebComponentsV0Enabled
  - GP 名稱：在 M84 前，重新啟用 Web 元件 v0 API (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebComponentsV0Enabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebComponentsV0Enabled
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebDriverOverridesIncompatiblePolicies
  #### 允許 WebDriver 覆寫不相容原則 (已過時) 
                       
        
  
  
  >已過時：此原則已過時，且無法在 Microsoft Edge 版本 84 及之後的版本中運作。
  #### 支援的版本：
  - 在 Windows 和 macOS 上，版本 77 到 84

  #### 說明
  
  
此原則無法運作，因為 WebDriver 目前相容於所有現有原則。

此原則會允許讓 WebDriver 功能的使用者覆寫可能干擾其操作的原則。

目前此原則會停用 [SitePerProcess](#siteperprocess) 和 [IsolateOrigins](#isolateorigins) 原則。

如果已啟用此原則，WebDriver 將可以覆寫不相容的原則。
如果停用或未設定原則，則將不允許 WebDriver 覆寫不相容的原則。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebDriverOverridesIncompatiblePolicies
  - GP 名稱：允許 WebDriver 覆寫不相容原則 (已過時)
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebDriverOverridesIncompatiblePolicies
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebDriverOverridesIncompatiblePolicies
  - 範例值：
``` xml
<true/>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebRtcLocalIpsAllowedUrls
  #### 管理由 WebRTC 暴露的本機 IP 位址
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 80 或更新版本

  #### 說明
  指定應該由 WebRTC 公開本機 IP 位址的來源 (URL) 或主機名稱模式 (例如 "*contoso.com*") 的清單。

如果啟用此原則，並設定來源 (URL) 或主機名稱模式清單，當 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為啟用時，WebRTC 會在符合清單中模式的情況下公開本機 IP 位址。

如果停用或未設定此原則，且 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為已啟用，則 WebRTC 將不會公開本機 IP 位址。 本機 IP 位址會使用 mDNS 主機名稱隱藏。

如果啟用、停用或未設定此原則，且 edge://flags/#enable-webrtc-hide-local-ips-with-mdns 為已停用，則 WebRTC 將會公開本機 IP 位址。

請注意，此原則會使得系統管理員可能需要的本機 IP 位址的保護變弱。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串清單

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebRtcLocalIpsAllowedUrls
  - GP 名稱：管理由 WebRTC 暴露的本機 IP 位址
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls
  - 路徑 (建議)：不適用
  - 數值名稱：1、2、3、...
  - 數值類型：REG_SZ 的清單
  ##### 範例值：
```
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\1 = https://www.contoso.com
SOFTWARE\Policies\Microsoft\Edge\WebRtcLocalIpsAllowedUrls\2 = *contoso.com*

```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebRtcLocalIpsAllowedUrls
  - 範例值：
``` xml
<array>
  <string>https://www.contoso.com</string>
  <string>*contoso.com*</string>
</array>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebRtcLocalhostIpHandling
  #### 限制由 WebRTC 暴露的本機 IP 位址
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
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

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebRtcLocalhostIpHandling
  - GP 名稱：限制由 WebRTC 暴露的本機 IP 位址
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebRtcLocalhostIpHandling
  - 值類型：REG_SZ
  ##### 範例值：
```
default
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebRtcLocalhostIpHandling
  - 範例值：
``` xml
<string>default</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WebRtcUdpPortRange
  #### 限制 WebRTC 所使用的本機 UDP 連接埠範圍
  
  
  #### 支援的版本：
  - Windows 和 macOS 上，版本 77 或更新版本

  #### 說明
  將 WebRTC 所使用的 UDP 連接埠範圍限制在指定的連接埠間隔 (包括端點)。

透過設定此原則，您可以指定 WebRTC 可以使用的本機 UDP 連接埠範圍。

如果未設定此原則，或將它設定為空白字串或無效的連接埠範圍，則 WebRTC 可以使用任何可用的本機 UDP 連接埠。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 字串

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WebRtcUdpPortRange
  - GP 名稱：限制 WebRTC 所使用的本機 UDP 連接埠範圍
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WebRtcUdpPortRange
  - 值類型：REG_SZ
  ##### 範例值：
```
10000-11999
```


  #### Mac 資訊和設定
  - 喜好設定機碼名稱：WebRtcUdpPortRange
  - 範例值：
``` xml
<string>10000-11999</string>
```
  

  [回到頁首](#microsoft-edge---policies)

  ### WinHttpProxyResolverEnabled
  #### 使用 Windows proxy 解析程式 (已過時) 
  >已過時：此原則已過時。 目前支援，但將在未來版本中過時。
  
  #### 支援的版本：
  - Windows 上，版本 84 或更新版本

  #### 說明
  此原則已遭取代，因為此原則會被未來版本中的類似功能取代，請參閱https://crbug.com/1032820。 無法在 Microsoft Edge 版本 87 中使用。

使用 Windows 解析所有瀏覽器網路的 proxy，而不是 Microsoft Edge 內建的 proxy 解析程式。 Windows proxy 解析程式可以啟用 Windows proxy 功能如 DirectAccess/NRPT。

此原則所帶來的問題如述 https://crbug.com/644030。 這會導致 Windows 代碼取得 PAC 檔案並執行之，包括透過 [ProxyPacUrl](#proxypacurl) 原則設定的 PAC 檔案。 由於 PAC 檔案的網路擷取是經由 Windows 而不是由 Microsoft Edge 代碼，因此像是 [DnsOverHttpsMode](#dnsoverhttpsmode) 的網路原則不適用於 PAC 檔案的網路擷取。

如果您啟用此原則，系統就會使用 Windows proxy 解析程式。

如果您停用或未設定此原則，系統將會使用 Microsoft Edge proxy 解析程式。

  #### 支援的功能：
  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：否 - 需要重新啟動瀏覽器

  #### Data Type:
  - 布林值

  #### Windows 資訊和設定
  ##### 群組原則 (ADMX) 資訊
  - GP 唯一名稱：WinHttpProxyResolverEnabled
  - GP 名稱：使用 Windows proxy 解析程式 (已過時) 
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge/
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdge.admx
  ##### Windows 登錄設定
  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge
  - 路徑 (建議)：不適用
  - 數值名稱：WinHttpProxyResolverEnabled
  - 值類型：REG_DWORD
  ##### 範例值：
```
0x00000001
```


  

  [回到頁首](#microsoft-edge---policies)


## 請參閱
- [設定 Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft 安全性基準部落格](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)
