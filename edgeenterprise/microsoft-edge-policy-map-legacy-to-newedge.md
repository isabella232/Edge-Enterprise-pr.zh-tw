---
title: Microsoft Edge 舊版與 Microsoft Edge 的原則對應
ms.author: brianalt
author: brianalt
manager: srugh
ms.date: 02/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 舊版與 Microsoft Edge 的原則對應
ms.openlocfilehash: f0ce58f3876bf9f02691d7d6bf2a7c7d1944fd24
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447997"
---
# <a name="microsoft-edge-legacy-to-microsoft-edge-policy-mapping"></a>Microsoft Edge 舊版與 Microsoft Edge 的原則對應

本文將 Microsoft Edge 舊版 (版本 45 及更舊版本) 的群組原則 (GP) 和行動裝置管理 (MDM) 設定對應到相關的 Microsoft Edge 版本 80 原則。 如需 Google Chrome 原則，請參閱 [Google Chrome 與 Microsoft Edge 的原則對應](microsoft-edge-policy-map-chrome-to-newedge.md)文章。

> [!NOTE]
> 以下提供的對應旨在協助您進行 Microsoft Edge 版本 80 的初始部署。 如需最新原則的最終清單，請參閱：
> - [瀏覽器原則參考](microsoft-edge-policies.md)
> - [更新原則參考](microsoft-edge-update-policies.md)

## <a name="microsoft-edge-legacy-to-microsoft-edge-policy-map"></a>Microsoft Edge 舊版與 Microsoft Edge 的原則對應

|Microsoft Edge 舊版 GP|Microsoft Edge 舊版 MDM|Microsoft Edge 原則 <br> 和 GP 名稱|
|-|-|-|
|[允許共用書籍資料夾](/microsoft-edge/deploy/available-policies#allow-a-shared-books-folder)|[UseSharedFolderForBooks](/windows/client-management/mdm/policy-csp-browser#browser-usesharedfolderforbooks)|不適用|
|[允許網址列下拉式清單建議](/microsoft-edge/deploy/available-policies#allow-address-bar-drop-down-list-suggestions)|[AllowAddressBarDropdown](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)|[SearchSuggestEnabled](./microsoft-edge-policies.md#searchsuggestenabled) <br> 啟用搜尋建議|
|[允許 Adobe Flash](/microsoft-edge/deploy/available-policies#allow-adobe-flash)|[AllowFlash](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)|[DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) <br> 預設 Adobe Flash 設定|
|[允許在結束時清除瀏覽資料](/microsoft-edge/deploy/available-policies#allow-clearing-browsing-data-on-exit)|[ClearBrowsingDataOnExit](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)|[ClearBrowsingDataOnExit](./microsoft-edge-policies.md#clearbrowsingdataonexit) <br> 在 Microsoft Edge 關閉時清除瀏覽資料|
|[允許書籍媒體櫃的設定更新](/microsoft-edge/deploy/available-policies#allow-configuration-updates-for-the-books-library)|[AllowConfigurationUpdateForBooksLibrary](/windows/client-management/mdm/policy-csp-browser#browser-allowconfigurationupdateforbookslibrary)|不適用|
|[允許 Cortana](/microsoft-edge/deploy/available-policies#allow-cortana)|[AllowCortana](/windows/client-management/mdm/policy-csp-browser#browser-allowcortana)|不適用|
|[允許開發人員工具](/microsoft-edge/deploy/available-policies#allow-developer-tools)|[AllowDeveloperTools](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)|[DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability) <br> 控制可使用開發人員工具的位置|
|[允許 [書籍] 索引標籤的延伸遙測](/microsoft-edge/deploy/available-policies#allow-extended-telemetry-for-the-books-tab)|[EnableExtendedBooksTelemetry](/windows/client-management/mdm/policy-csp-browser#browser-enableextendedbookstelemetry)|不適用|
|[允許擴充功能](/microsoft-edge/deploy/available-policies#allow-extensions)|[AllowExtensions](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)|[ExtensionInstallBlockList](./microsoft-edge-policies.md#extensioninstallblocklist) <br> 控制無法安裝的延伸 <br/><br/>_若要封鎖所有延伸，請使用 "*"_|
|[允許全螢幕模式](/microsoft-edge/deploy/group-policies/browser-settings-management-gp#allow-fullscreen-mode)|[AllowFullscreen](/windows/client-management/mdm/policy-csp-browser#browser-allowfullscreen)|[FullscreenAllowed](./microsoft-edge-policies.md#fullscreenallowed) <br> 允許全螢幕模式|
|[允許 Microsoft 相容性清單](/microsoft-edge/deploy/available-policies#allow-microsoft-compatibility-list)|[AllowMicrosoftCompatibilityList](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)|不適用|
|[允許 Microsoft Edge 在 Windows 啟動時、系統處於閒置狀態時，以及每次關閉 Microsoft Edge 時預啟動](/microsoft-edge/deploy/group-policies/prelaunch-preload-gp#allow-microsoft-edge-to-load-the-start-and-new-tab-page-at-windows-startup-and-each-time-microsoft-edge-is-closed)|[AllowPrelaunch](/windows/client-management/mdm/policy-csp-browser#browser-allowprelaunch)|不適用|
|[允許 Microsoft Edge 在 Windows 啟動時及每次關閉 Microsoft Edge 時啟動及載入 [開始] 和 [新索引標籤] 頁面](/microsoft-edge/deploy/group-policies/prelaunch-preload-gp#allow-microsoft-edge-to-load-the-start-and-new-tab-page-at-windows-startup-and-each-time-microsoft-edge-is-closed)|[AllowTabPreloading](/windows/client-management/mdm/policy-csp-browser#browser-allowtabpreloading)|[BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled) <br> 在關閉 Microsoft Edge 後繼續執行背景應用程式|
|[允許列印](/microsoft-edge/deploy/group-policies/browser-settings-management-gp#allow-printing)|[AllowPrinting](/windows/client-management/mdm/policy-csp-browser#browser-allowprinting)|[PrintingEnabled](./microsoft-edge-policies.md#printingenabled) <br> 啟用列印|
|[允許儲存歷史記錄](/microsoft-edge/deploy/group-policies/browser-settings-management-gp#allow-saving-history)|[AllowSavingHistory](/windows/client-management/mdm/policy-csp-browser#browser-allowsavinghistory)|[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) <br> 停用儲存瀏覽器歷史記錄|
|[允許搜索引擎自訂](/microsoft-edge/deploy/available-policies#allow-search-engine-customization)|[AllowSearchEngineCustomization](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)|[請參閱預設搜尋提供者原則](./microsoft-edge-policies.md#default-search-provider)|
|[允許延伸側載](/microsoft-edge/deploy/group-policies/extensions-management-gp#allow-sideloading-of-extensions)|[AllowSideloadingExtensions](/windows/client-management/mdm/policy-csp-browser#browser-allowsideloadingextensions)|[ExtensionInstallBlocklist](./microsoft-edge-policies.md#extensioninstallblocklist)<br/>控制無法安裝的延伸<br/>或 [DeveloperToolsAvailability](./microsoft-edge-policies.md#developertoolsavailability)<br/>控制可使用開發人員工具的位置|
|[允許在新索引標籤上顯示網頁內容](/microsoft-edge/deploy/available-policies#allow-web-content-on-new-tab-page)|[AllowWebContentOnNewTabPage](/windows/client-management/mdm/policy-csp-browser#browser-allowwebcontentonnewtabpage)|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) <br> 設定新索引標籤頁面 URL|
|[在 Microsoft Edge 中一律顯示書籍媒體櫃](/microsoft-edge/deploy/available-policies#always-show-the-books-library-in-microsoft-edge)|[AlwaysEnableBooksLibrary](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)|不適用|
|[設定額外的搜索引擎](/microsoft-edge/deploy/available-policies#configure-additional-search-engines)|[ConfigureAdditionalSearchEngines](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)|[請參閱預設搜尋提供者原則](./microsoft-edge-policies.md#default-search-provider)|
|[設定自動填入](/microsoft-edge/deploy/available-policies#configure-autofill)|[AllowAutofill](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)|[AutofillAddressEnabled](./microsoft-edge-policies.md#autofilladdressenabled) <br> 啟用位址自動填寫|
|[設定 Cookie](/microsoft-edge/deploy/group-policies/security-privacy-management-gp#configure-cookies)|[AllowCookies](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)|[DefaultCookiesSetting](./microsoft-edge-policies.md#defaultcookiessetting) <br> 設定 Cookie|
|[設定不要追蹤](/microsoft-edge/deploy/available-policies#configure-do-not-track)|[AllowDoNotTrack](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)|[ConfigureDoNotTrack](./microsoft-edge-policies.md#configuredonottrack) <br> 設定不要追蹤|
|[設定我的最愛列](/microsoft-edge/deploy/group-policies/favorites-management-gp#configure-favorites-bar)|[ConfigureFavoritesBar](/windows/client-management/mdm/policy-csp-browser#browser-configurefavoritesbar)|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) <br> 啟用我的最愛列|
|[設定首頁按鈕](/microsoft-edge/deploy/group-policies/home-button-gp#configure-home-button)|[ConfigureHomeButton](/windows/client-management/mdm/policy-csp-browser#browser-configurehomebutton)|[HomepageIsNewTabPage](./microsoft-edge-policies.md#homepageisnewtabpage) <br> 將新索引標籤頁面設為首頁|
|[設定 Kiosk 模式](/windows/client-management/mdm/policy-csp-browser#browser-configurekioskmode)|[ConfigureKioskMode](/windows/client-management/mdm/policy-csp-browser#browser-configurekioskmode)|不適用|
|[在閒置逾時後設定 Kiosk 重設](/windows/client-management/mdm/policy-csp-browser#browser-configurekioskresetafteridletimeout)|[ConfigureKioskResetAfterIdleTimeout](/windows/client-management/mdm/policy-csp-browser#browser-configurekioskresetafteridletimeout)|不適用|
|[設定 Microsoft Edge 的開啟方式](/microsoft-edge/deploy/group-policies/start-pages-gp#configure-open-microsoft-edge-with)|[ConfigureOpenEdgeWith](/windows/client-management/mdm/policy-csp-browser#browser-configureopenedgewith)|[RestoreOnStartup](./microsoft-edge-policies.md#restoreonstartup) <br> 啟動時要採取的動作|
|[設定密碼管理員](/microsoft-edge/deploy/available-policies#configure-password-manager)|[AllowPasswordManager](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)|[PasswordManagerEnabled](./microsoft-edge-policies.md#passwordmanagerenabled) <br> 啟用將密碼儲存到密碼管理員|
|[設定快顯封鎖程式](/microsoft-edge/deploy/available-policies#configure-pop-up-blocker)|[AllowPopups](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)|[DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting) <br> 預設快顯視窗設定|
|[設定網址列中的搜尋建議](/microsoft-edge/deploy/available-policies#configure-search-suggestions-in-address-bar)|[AllowSearchSuggestionsinAddressBar](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)|[請參閱預設搜尋提供者原則](./microsoft-edge-policies.md#default-search-provider)|
|[設定起始畫面](/microsoft-edge/deploy/available-policies#configure-start-pages)|[首頁](/windows/client-management/mdm/policy-csp-browser#browser-homepages)|[RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls) <br> 瀏覽器啟動時要開啟的網站|
|[設定 Adobe Flash 隨選即用設定](/microsoft-edge/deploy/available-policies#configure-the-adobe-flash-click-to-run-setting)|[AllowFlashClickToRun](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)|[DefaultPluginsSetting](./microsoft-edge-policies.md#defaultpluginssetting) <br> 預設 Adobe Flash 設定|
|[設定 Enterprise Mode Site List](/microsoft-edge/deploy/available-policies#configure-the-enterprise-mode-site-list)|[EnterpriseModeSiteList](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)|[InternetExplorerIntegrationSiteList](./microsoft-edge-policies.md#internetexplorerintegrationsitelist) <br> 設定 Enterprise Mode Site List|
|[設定 Windows Defender SmartScreen](/microsoft-edge/deploy/available-policies#configure-windows-defender-smartscreen)|[AllowSmartScreen](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)|[SmartScreenEnabled](./microsoft-edge-policies.md#smartscreenenabled) <br> 設定 Microsoft Defender SmartScreen|
|[停用對起始畫面的鎖定](/microsoft-edge/deploy/available-policies#disable-lockdown-of-start-pages)|[DisableLockdownOfStartPages](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)|[RestoreOnStartupURLs](./microsoft-edge-policies.md#restoreonstartupurls) <br> 瀏覽器啟動時要開啟的網站 (建議的版本)|
|[不會同步](/microsoft-edge/deploy/available-policies#do-not-sync)|[AllowSyncMySettings](/windows/client-management/mdm/policy-csp-browser#browser-allowsyncmysettings)|[SyncDisabled](./microsoft-edge-policies.md#syncdisabled) <br> 使用 Microsoft 同步處理服務停用資料同步處理|
|[不要同步瀏覽器設定](/microsoft-edge/deploy/available-policies#do-not-sync-browser-settings)|[DoNotSyncBrowserSettings](/windows/client-management/mdm/policy-csp-experience#experience-donotsyncbrowsersetting)|不適用|
|[同步處理 Internet Explorer 與 Microsoft Edge 之間的我的最愛](/microsoft-edge/deploy/available-policies#keep-favorites-in-sync-between-internet-explorer-and-microsoft-edge)|[SyncFavoritesBetweenIEAndMicrosoftEdge](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)|不適用|
|[防止存取 about:flags 頁面](/microsoft-edge/deploy/available-policies#prevent-access-to-the-aboutflags-page)|[PreventAccessToAboutFlagsInMicrosoftEdge](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) <br> 封鎖 URL 清單的存取權 <br/><br/>_設為 “edge://flags”。 我們不建議使用此原則封鎖 edge://* 頁面，因為這可能會導致非預期的結果。_|
|[防止略過檔案的 Windows Defender SmartScreen 提示](/microsoft-edge/deploy/available-policies#prevent-bypassing-windows-defender-smartscreen-prompts-for-files)|[PreventSmartScreenPromptOverrideForFiles](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)|[PreventSmartScreenPromptOverrideForFiles](./microsoft-edge-policies.md#preventsmartscreenpromptoverrideforfiles) <br> 防止略過關於下載的 Microsoft Defender SmartScreen 警告|
|[防止略過網站的 Windows Defender SmartScreen 提示](/microsoft-edge/deploy/available-policies#prevent-bypassing-windows-defender-smartscreen-prompts-for-sites)|[PreventSmartScreenPromptOverride](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)|[PreventSmartScreenPromptOverride](./microsoft-edge-policies.md#preventsmartscreenpromptoverride) <br> 防止略過網站的 Microsoft Defender SmartScreen 提示|
|[防止憑證錯誤覆寫](/microsoft-edge/deploy/group-policies/security-privacy-management-gp#prevent-certificate-error-overrides)|[PreventCertErrorOverrides](/windows/client-management/mdm/policy-csp-browser#browser-preventcerterroroverrides)|[SSLErrorOverrideAllowed](./microsoft-edge-policies.md#sslerroroverrideallowed) <br> 允許使用者從 HTTPS 警告頁面繼續進行|
|[防止變更 Microsoft Edge 的我的最愛](/microsoft-edge/deploy/available-policies#prevent-changes-to-favorites-on-microsoft-edge)|[LockdownFavorites](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)|[EditFavoritesEnabled](./microsoft-edge-policies.md#editfavoritesenabled) <br> 允許使用者編輯我的最愛|
|[防止 Microsoft Edge 於釘選網站到開始畫面時收集動態磚資訊](/microsoft-edge/deploy/available-policies#prevent-microsoft-edge-from-gathering-live-tile-information-when-pinning-a-site-to-start)|[PreventLiveTileDataCollection](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)|不適用|
|[防止 Microsoft Edge 開啟 [首次執行] 網頁](/microsoft-edge/deploy/available-policies#prevent-the-first-run-webpage-from-opening-on-microsoft-edge)|[PreventFirstRunPage](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)|[HideFirstRunExperience](./microsoft-edge-policies.md#hidefirstrunexperience) <br> 隱藏初次執行體驗與啟動顯示畫面|
|[防止關閉所需的延伸](/microsoft-edge/deploy/group-policies/extensions-management-gp#prevent-turning-off-required-extensions)|[PreventTurningOffRequiredExtensions](/windows/client-management/mdm/policy-csp-browser#browser-preventturningoffrequiredextensions)|[ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) <br> 控制自動安裝的延伸|
|[防止使用者開啟瀏覽器同步處理](/microsoft-edge/deploy/available-policies#prevent-users-from-turning-on-browser-syncing)|[PreventUsersFromTurningOnBrowserSyncing](/windows/client-management/mdm/policy-csp-experience#experience-preventusersfromturningonbrowsersyncing)|不適用|
|[避免針對 WebRTC 使用 Localhost IP 位址](/microsoft-edge/deploy/available-policies#prevent-using-localhost-ip-address-for-webrtc)|[PreventUsingLocalHostIPAddressForWebRTC](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)|[WebRtcLocalhostIpHandling](./microsoft-edge-policies.md#webrtclocalhostiphandling) <br> 限制由 WebRTC 暴露本機 IP 位址|
|[佈建我的最愛](/microsoft-edge/deploy/available-policies#provision-favorites)|[ProvisionFavorites](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)|[ManagedFavorites](./microsoft-edge-policies.md#managedfavorites) <br> 設定我的最愛|
|[將所有內部網路網站傳送到 Internet Explorer 11](/microsoft-edge/deploy/available-policies#send-all-intranet-sites-to-internet-explorer-11)|[SendIntranetTraffictoInternetExplorer](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)|[SendIntranetToInternetExplorer](./microsoft-edge-policies.md#sendintranettointernetexplorer) <br> 將所有內部網路網站傳送到 Internet Explorer|
|[設定預設搜尋引擎](/microsoft-edge/deploy/available-policies#set-default-search-engine)|[SetDefaultSearchEngine](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)|[請參閱預設搜尋提供者原則](./microsoft-edge-policies.md#default-search-provider)|
|[設定首頁按鈕 URL](/microsoft-edge/deploy/group-policies/home-button-gp#set-home-button-url)|[SetHomeButtonURL](/windows/client-management/mdm/policy-csp-browser#browser-sethomebuttonurl)|[HomepageLocation](./microsoft-edge-policies.md#homepagelocation) <br> 設定首頁 URL|
|[設定新索引標籤頁面 URL](/microsoft-edge/deploy/group-policies/new-tab-page-settings-gp#set-new-tab-page-url)|[SetNewTabPageURL](/windows/client-management/mdm/policy-csp-browser#browser-setnewtabpageurl)|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) <br> 設定新索引標籤頁面 URL|
|[在 Internet Explorer 中開啟網站時顯示訊息](/microsoft-edge/deploy/available-policies#show-message-when-opening-sites-in-internet-explorer)|[ShowMessageWhenOpeningSitesInInternetExplorer](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)|不適用|
|[解除鎖定首頁按鈕](/microsoft-edge/deploy/group-policies/home-button-gp#unlock-home-button)|[UnlockHomeButton](/windows/client-management/mdm/policy-csp-browser#browser-unlockhomebutton)|[ShowHomeButton ](./microsoft-edge-policies.md#showhomebutton) <br> 在工具列上顯示 [首頁] 按鈕 (建議的版本)|


## <a name="see-also"></a>請參閱
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [設定 Microsoft Edge](configure-microsoft-edge.md)
-   [瀏覽器原則參考](microsoft-edge-policies.md)