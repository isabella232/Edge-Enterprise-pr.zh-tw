---
title: Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 09/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: c62d540b014a47f1240d542c68ee52822719239f
ms.sourcegitcommit: 4442aa94d4ff2fef8dd6f389ec0c6823b150d04f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2021
ms.locfileid: "12053312"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Microsoft Edge Beta 通道的版本資訊

這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。 這些版本資訊的封存版本可在[此處](microsoft-edge-relnote-archive-beta-channel.md)取得。

> [!NOTE]
> Microsoft Edge Web 平台不斷演進，以改善使用者體驗、安全性和隱私權。 若要深入了解，請參閱 [Microsoft Edge 即將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes) (英文)。

## <a name="version-95010209-september-28"></a>版本 95.0.1020.9：9 月 28 日

### <a name="feature-updates"></a>功能更新

- **在檔案檔案管理器支援中SharePoint線上文件庫Microsoft Edge。**  現在，您可以在線上新式文件庫上SharePoint檔案管理器中的 View 功能。 若要顯示此體驗並適用于您的使用者，您必須啟用 Microsoft Edge 政策「在 Microsoft Edge 中設定[SharePoint](/deployedge/microsoft-edge-policies#configureviewinfileexplorer)頁面的檔案功能」，並更新您的 SharePoint Online 租使用者設定。 深入瞭解：使用檔案SharePoint檔案管理器在 Microsoft Edge[中SharePoint檔案Microsoft 365 |Microsoft Docs](/SharePoint/sharepoint-view-in-edge)。

- **內部網路區域檔案 URL 連結將在檔案Windows中開啟。**  您可以允許來自內部網路區域 HTTPS 網站的內部網路區域檔案的檔案 URL 連結，Windows檔案或目錄的檔案總管。 您可以使用 [IntranetFileLinksEnabled 策略啟用此](/deployedge/microsoft-edge-policies#intranetfilelinksenabled) 體驗。

- **下載體驗的改良功能。**  下載使用者體驗的支援正在延伸至漸進式 Web 應用程式 PWAs 和 WebView。 我們也會開始支援拖放到檔案檔案管理器和桌面。

- **從 PDF 檔離開的地方繼續。**  現在，您就能從上次關閉 PDF 檔的地方繼續閱讀。

- **當膝上型電腦進入省電模式時，效率模式可延長電池使用時間。**  當膝上型電腦進入省電模式，允許瀏覽器管理資源使用量以延長您機器的電池使用時間時，效率模式就會變成使用中。 當效率模式變成使用中、已拔除和電池不足、已拔除、永遠和永不使用時，您將有四個選項。 請注意：此為受控功能推出。 具有電池的裝置應已開啟此功能。

***新原則***

- [BrowserLegacyExtensionPointsBlockingEnabled](/DeployEdge/microsoft-edge-policies#browserlegacyextensionpointsblockingenabled) 啟用瀏覽器舊版擴充點封鎖
- [CrossOriginWebAssemblyModuleSharingEnabled](/DeployEdge/microsoft-edge-policies#crossoriginwebassemblymodulesharingenabled) 指定 WebAssembly 模組是否可以跨來源送出
- [DisplayCapturePermissionsPolicyEnabled](/DeployEdge/microsoft-edge-policies#displaycapturepermissionspolicyenabled) 指定是否已檢查或略過顯示-捕獲許可權-策略
- [InternetExplorerIntegrationWindowOpenHeightAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenheightadjustment) 設定來自 IE 模式頁面與 Edge 模式頁面之視窗與開啟高度之間的圖元調整
- [InternetExplorerIntegrationWindowOpenWidthAdjustment](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationwindowopenwidthadjustment) 設定視窗之間的圖元調整。從 IE 模式頁面與 Edge 模式頁面來源的開啟寬度
- [IntranetFileLinksEnabled](/DeployEdge/microsoft-edge-policies#intranetfilelinksenabled)允許內部網路區域檔案 URL 連結Microsoft Edge檔案檔案Windows開啟
- [ShadowStackCrashRollbackBehavior](/DeployEdge/microsoft-edge-policies#shadowstackcrashrollbackbehavior) 設定 ShadowStack 當機回收行為
- [VisualSearchEnabled](/DeployEdge/microsoft-edge-policies#visualsearchenabled) 已啟用視覺搜尋

***已過時的原則***

- [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - 允許 Internet Explorer 模式測試
- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 啟用預設舊版 SameSite Cookie 行為設定

## <a name="version-94099223-september-17"></a>版本 94.0.992.23：9 月 17 日

已修正各種錯誤和效能問題。

## <a name="version-94099219-september-13"></a>版本 94.0.992.19：9 月 13 日

已修正各種錯誤和效能問題。

## <a name="version-94099214-september-7"></a>版本 94.0.992.14：9 月 7 日

已修正各種錯誤和效能問題。

## <a name="version-9409929-september-2"></a>版本 94.0.992.9：9 月 2 日

### <a name="feature-updates"></a>功能更新

- **Microsoft Edge Beta 和穩定通道中的更新，以進入 4 周更新的步頻。**  我們會針對主要版本採用新的 4 周發行週期。 您可以在這裡閱讀有關決策的更多資訊： https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **提供新「擴充穩定」選項。**  我們向受管理的企業客戶提供新「擴充穩定」選項。 「擴充穩定」選項將保留偶數修訂編號並每 8 週更新一次。 將會有每兩週一次的安全性更新。  此處提供其他資訊：https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **改良開啟 MHTML 檔案的預設行為。**  如果啟用 IE 模式，MHTML 檔案會繼續在 IE 模式中開啟，除非 MHTML 檔案是使用 Microsoft Edge 儲存 (使用 Microsoft Edge 中的 [另存新檔] 或 [另存新頁面] 選項)。 如果檔案是從 Microsoft Edge 儲存，現在就會在 Microsoft Edge 中開啟。  此變更將修正從 Microsoft Edge 儲存時，在 IE 模式下開啟 MHTML 檔案時觀察到的呈現問題。

- **限制私人網路要求以保護內容。** 從網際網路上的頁面存取本機 (內部網路) 網路的資源需要透過 HTTPS 傳遞這些頁面。 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 如需詳細資訊，請瀏覽至 [Chrome 平台狀態項目](https://chromestatus.com/feature/5436853517811712)。 有兩種相容性原則可支援需要保留與非安全頁面相容性的案例：[InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 和 [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls)。

- **封鎖混合內容下載。** 安全頁面只會下載託管在其他安全頁面上的檔案，如果從安全頁面啟動，則會封鎖託管在非安全 (非 HTTPS) 頁面的下載。 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 若要詳細資訊，請瀏覽至 [Google 安全性部落格項目](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html)。

- **啟用內部部署帳戶的隱含登入。**   啟用 OnlyOnPremises1icitSigninEnabled 原則後，只會針對內部部署帳戶啟用隱含登入。  Microsoft Edge 不會嘗試隱含登入至 MSA 或 AAD 帳戶。 也會停止從內部部署帳戶升級至 AAD 帳戶。

- **新增到 PDF 檔的免費表單文字方塊。**  我們現在支援在 PDF 檔中新增免費的表單文字方塊，您可以使用這些文字方塊來填寫表單並新增可見的筆記。

- **輕鬆更新您的密碼。**  瀏覽器現在會直接將您帶至某個網站的變更密碼頁面，以避免手動流覽至頁面，以節省時間和按一下。 當您進入此頁面時，瀏覽器也會自動填上您現有的密碼，並建議使用強大且唯一的新密碼。  請注意：此功能目前可在數量有限的網站使用。  

- **新的協助工具設定頁面。** 我們已將協助工具相關設定整合在單一頁面上。 您可以在主要設定清單下找到新 edge://settings/accessibility 頁面。 您可以在這裡找到可放大網頁的設定、在焦點區域周圍顯示高可見度大綱，以及其他可協助改善網頁瀏覽體驗的設定。 我們會在未來的 Microsoft Edge 版本中繼續在此處新增設定。

***新原則***

- [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) 忽略應用程式防護網站清單設定，並正常瀏覽 Edge
- [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) 只針對內部部署帳戶啟用隱含登入
- [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) 透過 WebRTC 建立對等連線時，啟用對 Windows 作業系統路由表規則的支援

***淘汰的原則***

- [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) 啟用 User-Agent 用戶端提示功能

## <a name="version-93096133-august-27"></a>版本 93.0.961.33：8 月 27 日

已修正各種錯誤和效能問題。

## <a name="version-93096127-august-20"></a>版本 93.0.961.27：8 月 20 日

已修正各種錯誤和效能問題。

## <a name="version-93096124-august-18"></a>版本 93.0.961.24：8 月 18 日

已修正各種錯誤和效能問題。

## <a name="version-93096111-august-3"></a>版本 93.0.961.11：8 月 3 日

### <a name="feature-updates"></a>功能更新

- **Microsoft Edge 中的初始喜好設定。**  從 Microsoft Edge版本 93 開始，Microsoft Edge初始喜好設定，將新版部署至企業[將變得更加容易](/deployedge/initial-preferences-support-on-microsoft-edge-browser)。

- **Microsoft Edge 上的 IE 模式將支援「不合併」行為。**  從版本 93 Microsoft Edge開始，Microsoft Edge的 IE 模式會支援「無合併」。 對於使用者來說，從 IE 模式應用程式啟動新的瀏覽器視窗時，視窗會位於另一個會話中，類似 IE11 中的行為。 您必須調整網站清單，以設定需要防止會話共用的網站。 在幕後，針對 Microsoft Edge 的每個視窗，在該視窗內第一次瀏覽 IE 模式索引標籤時 (如果它是指定的其中一個「不合併」網站)，該視窗會遭鎖定到與所有其他 Microsoft Edge 視窗不同的「不合併」IE 工作階段，至少直到該視窗中的最後一個 IE 模式索引標籤關閉為止。 按一下[這裡](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--no-merge--option-that-was-supported-in-internet-explorer-11-)深入了解。

- **索引標籤群組。**  將定位停駐點分類為使用者定義群組的功能，可協助您更有效地尋找、切換及管理多個工作流程的定位字元。 若要啟用此功能，我們會從版本 93 開始開啟製表Microsoft Edge群組。

- **使用垂直索引標籤時隱藏標題列。**  在垂直索引標籤中時隱藏瀏覽器的標題列，以獲得額外的一些像素。 從 Microsoft Edge 93 開始，您可以前往 edge://settings/appearance，然後選取在垂直製表模式中隱藏標題列的選項。

- **透過暫留工具列的影片子母畫面 (PiP)。**  從 Microsoft Edge版本 93 開始，在 PiP 模式或 PiP 模式中 (圖片) 更容易。 當您將游標暫留在支援的影片上時，會出現一個工具列，允許您在 PiP 視窗中觀看該影片。  注意：這項功能目前適用于 macOS Microsoft Edge使用者。  在我們繼續向使用者推出時，請Windows回來。

- **移除 TLS 中的 3DES。**  從版本 Microsoft Edge 93 開始，系統將會移除TLS_RSA_WITH_3DES_EDE_CBC_SHA密碼套件的支援。 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 如需詳細資訊，請瀏覽至 [Chrome 平台狀態項目](https://chromestatus.com/feature/6678134168485888)。 此外，在 Microsoft Edge 版本 93 中，[TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) 原則將可用來支援需要保留與過時伺服器相容性的情況。 此相容性原則將在 Microsoft Edge 版本 95 中過時並停止運作。 請確定在此之前更新受影響的伺服器。

- **可略過 ClickOnce 和 DirectInvoke 提示的原則。**  我們已更新我們的原則，以針對來自指定網域的指定檔案類型，啟用略過 ClickOnce 的提示和 DirectInvoke 的應用程式。 若要這樣做，您必須：

  - 啟用 [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) 或 [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - 啟用 [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) 原則，並設定應停用 ClickOnce 和 DirectInvoke 的特定檔案類型清單。
  - 啟用[AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls)政策，並設定將停用 ClickOnce DirectInvoke 的特定網域清單。

  注意：AutoOpenAllowedForURLs 是 AutoOpenFileTypes 的支援原則。 如果未設定 AutoOpenAllowedForURLs 且已設定 AutoOpenFileTypes，則列出的檔案類型將自動從所有 URL 開啟。

### <a name="new-policies"></a>新原則

- [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) 允許媒體在特定的網站上自動播放
- [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) 已啟用 TLS 的 CECPQ2 後量子金鑰協定
- [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) 在 Microsoft Edge 中設定適用於 SharePoint 頁面的 [在檔案總管中檢視] 功能
- [DefaultJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) 控制 JavaScript JIT 的使用
- [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) 允許通知將 Microsoft Edge設為預設的 PDF 閱讀程式
- [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) 設定使用者可覆寫功能旗標的能力
- [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) 啟用隱含登入
- [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) 設定企業模式雲端網站清單
- [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) 設定重新整理企業模式網站清單的頻率
- [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) 允許 JavaScript 在這些網站上使用 JIT
- [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) 封鎖 JavaScript 以防止在這些網站上使用 JIT
- [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) 讓 Windows 搜尋本機 Microsoft Edge 瀏覽資料
- [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) 一律使用 Microsoft AutoUpdate 做為 Microsoft Edge 的更新程式
- [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) 允許使用此設定檔的單一登入 Microsoft 網站
- [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) 已針對登入強制執行的 OneAuth 驗證流程
- [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) 允許使用者在線上建立帳戶時，取得強式密碼建議
- [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) 設定要求使用者在使用密碼自動填寫時輸入其裝置密碼的設定
- [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) 設定列印版面配置
- [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) 允許遠端偵錯
- [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) 設定重新開機的時間間隔
- [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) 啟用差旅協助
- [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) 在 TLS 中啟用 3DES 加密套件

#### <a name="deprecated-policy"></a>取代的原則

- [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 啟用預設舊版 SameSite Cookie 行為設定

#### <a name="obsoleted-policy"></a>淘汰的原則

- [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) 設定 Microsoft Edge 新增索引標籤頁面體驗

#### <a name="additional-change"></a>其他變更

- [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) 新增 Mac 平台支援

## <a name="version-93096118-august-10"></a>版本 93.0.961.18：8 月 10 日

已修正各種錯誤和效能問題。

## <a name="version-92090262-july-29"></a>版本 92.0.902.62：7 月 29 日

已修正各種錯誤和效能問題。

## <a name="version-92090255-july-21"></a>版本 92.0.902.55：7 月 21 日

已修正各種錯誤和效能問題。

## <a name="version-92090245-july-12"></a>版本 92.0.902.45：7 月 12 日

已修正各種錯誤和效能問題。

## <a name="version-92090240-july-6"></a>版本 92.0.902.40：7 月 6 日

已修正各種錯誤和效能問題。

## <a name="version-92090222-june-21"></a>版本 92.0.902.22：6 月 21 日

### <a name="feature-updates"></a>功能更新

- **自然語言搜尋網址欄上的瀏覽器歷程記錄**。 現在，由於從網址欄搜尋自然語言，尋找您正在尋找的文章/網站變得更容易。 您可以根據頁面內容/描述/時間 (搜尋結果，例如「上周的蛋糕食譜」) 除了標題/URL 關鍵字本身符合之外。
請注意：此為受控功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

- **使用者可以在 Microsoft Edge 上輕鬆進入 Internet Explorer 模式**。 從 Microsoft Edge 版本 92 開始，使用者可以在 Microsoft Edge 上重新載入 Internet Explorer 模式的網站，而不需要依賴獨立的 IE 11 應用程式，同時等待在企業模式網站清單中設定網站。 系統會提示使用者將網站新增到其本機網站清單，以便在接下來的 30 天內，瀏覽至 Microsoft Edge 中的相同頁面將會在 IE 模式下自動轉譯。 您可以使用 *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* 原則設定此體驗，並允許存取 IE 模式進入點，而且能夠將網站新增到本機網站清單。 您可以使用 *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* 原則調整將網站保留在本機網站清單中的天數。
請注意，Windows 10 版本 1909 需要 KB5003698 或更新版本；Windows 10 版本 2004、Windows 10 版本 20H2 或 Windows 10 版本 21H1 需要 KB5003690 或更新版本，才能提供端對端體驗。

- **MHTML 檔案將預設為在 Internet Explorer 模式下開啟**。 從 Microsoft Edge 版本 92 Stable 開始，MHTML 檔案類型將會在 Microsoft Edge (而非 Internet Explorer (IE11) 應用程式) 上自動以 Internet Explorer 模式開啟。 這是在瀏覽器中嘗試檢視 Outlook 電子郵件時最常觀察到的情況。 只有在 IE11 是此檔案類型的預設處理常式時，才能進行此變更。 如果您想要變更這項設定，可以在使用[本指南](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)安裝 Stable 92 版更新之前執行此操作。

- **付款方式現在會跨裝置同步處理**。 從 Microsoft Edge 版本 92 開始，您可以選擇在所有已登入的裝置上同步處理您的付款資訊。
請注意：此為受控功能推出。 如果您沒看到這項功能，請儘快回來查看，繼續推出。

- **「停用開發人員模式擴充功能」警告可能會永久關閉**。 從 Microsoft Edge 版本 92 開始，您可以按一下 [不再顯示此訊息] 選項，以關閉警告 [停用開發人員模式擴充功能]。
請注意：此為受控功能推出。 如果您沒看到這項功能，請儘快回來查看，繼續推出。

- **從工具列管理擴充功能**。 工具列上全新的擴充功能功能表將讓您輕鬆地隱藏/釘選擴充功能。 管理延伸和尋找新延伸的快速連結將使您輕鬆找到新延伸和管理現有延伸。
請注意：此為受控功能推出。 如果您沒看到這項功能，請儘快回來查看，繼續推出。

- **自動 HTTPS**。 使用者可以選擇在可能支援這個更安全的通訊協定的網域上，將瀏覽從 HTTP 升級至 HTTPS。 此支援也可以設定為嘗試針對所有網域，透過 HTTPS 傳遞。
請注意：我們正在實驗這項功能，如果您退出宣告實驗，將不會看到此行為。

- **字型呈現的改善**。 已改善文字的呈現，以提高清晰度並減少模糊度。
請注意：此為受控功能推出。 如果您沒看到這項功能，請儘快回來查看，繼續推出。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

已新增八個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：

- [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 已啟用使用此設定檔單一登入公司或學校網站。
- [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) 設定自動 HTTPS
- [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) 控制無周邊模式的使用
- [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 指定是否要允許不安全的網站向較私人的網路端點提出要求
- [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) 允許列出的網站從不安全的內容對較私人的網路端點提出要求
- [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) 指定網站保留在本機 IE 模式網站清單上的天數
- [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 允許未設定的網站在 Internet Explorer 模式下重新載入
- [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) 指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用

#### <a name="obsoleted-policy"></a>淘汰的原則

- [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) 允許本機信賴起點核發時使用 SHA-1 簽署憑證。

## <a name="version-9209029-june-8"></a>版本 92.0.902.9：6 月 8 日

已修正各種錯誤和效能問題。

## <a name="version-91086441-june-3"></a>版本 91.0.864.41：6 月 3 日

已修正各種錯誤和效能問題。

## <a name="version-91086437-may-27"></a>版本 91.0.864.37：5 月 27 日

已修正各種錯誤和效能問題。

## <a name="version-91086436-may-26"></a>版本 91.0.864.36：5 月 26 日

已修正各種錯誤和效能問題。

## <a name="version-91086433-may-21"></a>版本 91.0.864.33：5 月 21 日

已修正各種錯誤和效能問題。

## <a name="version-91086427-may-14"></a>版本 91.0.864.27：5 月 14 日

已修正各種錯誤和效能問題。

## <a name="version-91086419-may-7"></a>版本 91.0.864.19：5 月 7 日

已修正各種錯誤和效能問題。

## <a name="version-91086415-may-3"></a>版本 91.0.864.15：5 月 3 日

已修正各種錯誤和效能問題。

## <a name="version-91086411-april-30"></a>版本 91.0.864.11：4 月 30 日

### <a name="feature-updates"></a>功能更新

- **在 Proxy 層級識別來自 Microsoft Defender 應用程式防護容器的流量**。 從 Microsoft Edge 版本 91 開始，內建支援以標記來自應用程式防護容器的流量，讓企業能夠識別它們並套用特定原則。

- **支援選項，讓 [我的最愛] 從主機同步處理至 Edge 應用程式防護容器**。 從 Microsoft Edge 版本 91 開始，使用者可以選擇設定應用程式防護，將其 [我的最愛] 從主機同步處理至容器。 這可確保容器上也會出現新的 [我的最愛]。

- **支援語音辨識 API**。 從 Microsoft Edge 版本 91 開始，將會新增對 Google.com 和類似網站的語音辨識命令 API 支援。 此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

- **使用新的佈景主題色彩以個人化您的瀏覽器**。 使用設定 -> 外觀頁面上的十四種新佈景主題色彩的其中一種，將 Microsoft Edge 個人化。 您也可以從 Microsoft Edge 附加元件網站安裝自訂佈景主題。 [深入了解](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- **中斷下載** 從 Microsoft Edge 版本 91 開始，瀏覽器會自動中斷類型下載，這些下載若在未經使用者互動的情況下啟動，且不受 SmartScreen 應用程式信譽檢查支援，這些下載可能會危害您的電腦。 使用者可以在下載項目上按一下滑鼠右鍵並選擇「保留」，以覆寫並繼續下載。
企業系統管理員可以退出宣告此行為的這兩個原則之一：
    - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名警告。如需詳細資訊，請參閱 [Microsoft Edge 安全性下載中斷](/deployedge/microsoft-edge-security-downloads-interruptions)

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

已新增六個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：

- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) -　應用程式防護流量識別
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - 明確允許的網路連接埠
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - 允許匯出啟動頁面設定
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - 讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - 允許新分頁頁面上的 Microsoft 新聞內容
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - 允許新分頁頁面上的快速連結

#### <a name="obsoleted-policy"></a>淘汰的原則

- [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - 啟用主動式驗證
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a>版本 90.0.818.46：4 月 22 日

已修正各種錯誤和效能問題。

## <a name="version-90081842-april-20"></a>版本 90.0.818.42：4 月 20 日

已修正各種錯誤和效能問題。

## <a name="version-90081841-april-16"></a>版本 90.0.818.41：4 月 16 日

已修正各種錯誤和效能問題。

## <a name="version-90081838-april-14"></a>版本 90.0.818.38：4 月 14 日

已修正各種錯誤和效能問題。

## <a name="version-90081836-april-12"></a>版本 90.0.818.36：4 月 12 日

已修正各種錯誤和效能問題。

## <a name="version-90081827-april-2"></a>版本 90.0.818.27：4 月 2 日

修正各種錯誤和效能問題。

## <a name="version-90081822-march-29"></a>版本 90.0.818.22：3 月 29 日

修正各種錯誤和效能問題。

## <a name="version-90081814-march-22"></a>版本 90.0.818.14：3 月 22 日

修正各種錯誤和效能問題。
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>版本 90.0.818.8：3 月 16 日

### <a name="feature-updates"></a>功能更新

- **單一登入 (SSO) 目前可供 macOS 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用**。 在 macOS 上，在 Microsoft Edge 上登入的使用者現在會自動進入網站，這些網站已設定為允許使用 Work 和 Microsoft 帳戶 (例如 bing.com、office.com、msn.com 和 outlook.com) 進行單一登入。

- **Kiosk 模式。** 從 Microsoft Edge 版本 90 開始，我們已鎖定 UI 列印設定，只允許已設定印表機和「列印至 PDF」選項。 我們也在受指派的存取權單一應用程式 kiosk 模式中進行了改善，以限制從瀏覽器啟動其他應用程式。 如需有關 Kiosk 模式功能的詳細資訊，請移至[這裡](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)。

- **列印：**

  - **非 PostScript 印表機的新列印點陣化模式**。 從 Microsoft Edge 版本 90 開始，系統管理員可以使用新原則來定義其使用者的列印點陣化模式。 此原則可控制 Microsoft Edge 列印至 Windows 上非 PostScript 印表機的方式。  有時需將非 PostScript 印表機上的列印工作點陣化才能正確列印。 列印選項為「完整」和「快速」。

  - **用於列印的其他頁面縮放選項**。 使用者現在能夠自訂縮放比例，同時使用其他選項列印網頁和 PDF 文件。 「符合頁面大小」選項可確保網頁或文件符合所選「紙張大小」可供列印的空間。 [實際大小] 選項可確保無論選取的 [紙張大小] 為何，列印內容的大小都不會變更。

- **生產力：**

  - **延伸自動填寫建議，以包含來自剪貼簿的地址欄位內容**。 當您按一下設定檔/地址欄位 (例如，電話、電子郵件、郵遞區號、縣/市、省/市等) 以顯示為自動填寫建議時，系統將會剖析剪貼簿內容。

  - **即使未偵測到表單或欄位，使用者也可以搜尋自動填寫建議**。 現在，如果您將您的資訊儲存在 Microsoft Edge 上，自動填寫建議將自動彈出，並幫助您在填寫表單時節省時間。 如果自動填寫遺漏表單，或您想要在通常沒有自動填寫功能的表單 (例如暫存表單) 中擷取資料，可以搜尋您使用自動填寫的資訊。

- **從功能表列的飛出視窗存取下載**。 下載會顯示在右上角，將所有作用中下載顯示在同一個位置。 此功能表可以很輕易關閉，因此使用者可以繼續瀏覽而不受干擾，且他們可以直接從工具列監視整體下載進度。 [進一步了解](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551)。


### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 7 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：

- [ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - 已啟用應用程式防護我的最愛同步處理
- [ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - 設定網站到特定來源的受管理設定值
- [PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - 列印點陣化模式
- [QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - 管理 Microsoft Edge 中的 QuickView Office 檔案功能
- [SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - 允許使用者從特定來源的 HTTPS 警告頁面繼續進行
- [WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - 啟用視窗遮蔽
- [WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - 已啟用適用於 HTTP 驗證的 Windows Hello

#### <a name="deprecated-policies"></a>取代的原則

- [NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 啟用原生視窗遮蔽
- [SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) - 已啟用最低 TLS 版本
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a>版本 89.0.774.54：3 月 13 日

修正各種錯誤和效能問題。

## <a name="version-89077450-march-10"></a>版本 89.0.774.50：3 月 10 日

修正各種錯誤和效能問題。

## <a name="version-89077448-march-8"></a>版本 89.0.774.48：3 月 8 日

修正各種錯誤和效能問題。

## <a name="version-89077445-march-3"></a>版本 89.0.774.45：3 月 3 日

修正各種錯誤和效能問題。

## <a name="version-89077439-february-26"></a>版本 89.0.774.39：2 月 26 日

修正各種錯誤和效能問題。

## <a name="version-89077434-february-22"></a>版本 89.0.774.34：2 月 22 日

修正各種錯誤和效能問題。

## <a name="version-89077427-february-12"></a>版本 89.0.774.27：2 月 12 日

修正各種錯誤和效能問題。

## <a name="version-89077423-february-8"></a>版本 89.0.774.23：2 月 8 日

修正各種錯誤和效能問題。

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
