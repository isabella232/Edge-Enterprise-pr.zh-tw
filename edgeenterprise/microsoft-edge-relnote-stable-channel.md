---
title: Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 10/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: f15c8e1d4dcd037b0948e7309387ba3baa5d1ffa
ms.sourcegitcommit: 2bf511511f131b8497b3e162c44286c217508885
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/01/2021
ms.locfileid: "12057334"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。

- 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。
- 封存的 Microsoft Edge 穩定通道的版本資訊在[此處](microsoft-edge-relnote-archive-stable-channel.md)。

 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。

> [!NOTE]
> 針對穩定通道，更新會在一或多天內逐步推出。 若要深入了解，請參閱[適用於 Microsoft Edge 更新的漸進式推出](microsoft-edge-update-progressive-rollout.md)。
>
> Microsoft Edge Web 平台不斷演進，以改善使用者體驗、安全性和隱私權。 若要深入了解，請參閱 [Microsoft Edge 即將進行的網站相容性影響變更] (英文)(/ microsoft-edge/web-platform/site-impacting-changes)。

## <a name="version-94099238-october-1"></a>版本 94.0.992.38: 10 月 1 日

> [!Important]
> 此更新包括 Chromium 小組報告 [CVE-2021-37975](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37975) 和 [CVE-2021-37976](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37976) 的修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱[安全性更新導覽](https://msrc.microsoft.com/update-guide)

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#october-01-2021)。

## <a name="version-94099237-september-30"></a>版本 94.0.992.37：9 月 30 日

已修正各種錯誤和效能問題。

## <a name="version-94099231-september-24"></a>版本 94.0.992.31：9 月 24 日

> [!Important]
> 此更新包含 [CVE-2021-37973](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-37973) 的修正程式，Chromium 小組已回報該修正程式存在漏洞。 如需詳細資訊, 請參閱[安全性更新導覽](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#september-24-2021)。

### <a name="feature-updates"></a>功能更新

- **Microsoft Edge 已完成改為 4 週更新頻率。**  我們已針對主要版本採用新的 4 週發行週期。 請從這裡閱讀其他資訊：https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/

- **提供新「擴充穩定」選項。**  我們向受管理的企業客戶提供新「擴充穩定」選項。 「擴充穩定」選項將保留偶數修訂編號並每 8 週更新一次。 將會有每兩週一次的安全性更新。  此處提供其他資訊：https://blogs.windows.com/msedgedev/2021/07/15/opt-in-extended-stable-release-cycle/

- **改良開啟 MHTML 檔案的預設行為。**  如果啟用 IE 模式，MHTML 檔案會繼續在 IE 模式中開啟，除非 MHTML 檔案是使用 Microsoft Edge 儲存 (使用 Microsoft Edge 中的 [另存新檔] 或 [另存新頁面] 選項)。 如果檔案是從 Microsoft Edge 儲存，現在就會在 Microsoft Edge 中開啟。  此變更將修正從 Microsoft Edge 儲存時，在 IE 模式下開啟 MHTML 檔案時觀察到的呈現問題。

- **限制私人網路要求以保護內容。** 從網際網路上的頁面存取本機 (內部網路) 網路的資源需要透過 HTTPS 傳遞這些頁面。 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 如需詳細資訊，請瀏覽至 [Chrome 平台狀態項目](https://chromestatus.com/feature/5436853517811712)。 有兩種相容性原則可支援需要保留與非安全頁面相容性的案例：[InsecurePrivateNetworkRequestAllowed](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 和 [InsecurePrivateNetworkRequestAllowedForUrls](/deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls)。

- **封鎖混合內容下載。** 安全頁面只會下載託管在其他安全頁面上的檔案，如果從安全頁面啟動，則會封鎖託管在非安全 (非 HTTPS) 頁面的下載。 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 若要詳細資訊，請瀏覽至 [Google 安全性部落格項目](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html)。

- **啟用內部部署帳戶的隱含登入。** 啟用 [OnlyOnPremises1icitSigninEnabled](/deployedge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) 原則後，只會針對內部部署帳戶啟用隱含登入。  Microsoft Edge 不會嘗試隱含登入至 MSA 或 AAD 帳戶。 也會停止從內部部署帳戶升級至 AAD 帳戶。

- **新的協助工具設定頁面。**  我們已將協助工具相關設定整合在單一頁面上。 您可以在主要設定清單下找到新 edge://settings/accessibility 頁面。 您可以在這裡找到可放大網頁的設定、在焦點區域周圍顯示高可見度大綱，以及其他可協助改善網頁瀏覽體驗的設定。 我們會在未來的 Microsoft Edge 版本中繼續在此處新增設定。

***新原則***

- 
            [ApplicationGuardPassiveModeEnabled](/DeployEdge/microsoft-edge-policies#applicationguardpassivemodeenabled) 忽略應用程式防護網站清單設定，並正常瀏覽 Edge
- 
            [OnlyOnPremisesImplicitSigninEnabled](/DeployEdge/microsoft-edge-policies#onlyonpremisesimplicitsigninenabled) 只針對內部部署帳戶啟用隱含登入
- 
            [WebRtcRespectOsRoutingTableEnabled](/DeployEdge/microsoft-edge-policies#webrtcrespectosroutingtableenabled) 透過 WebRTC 建立對等連線時，啟用對 Windows 作業系統路由表規則的支援

***淘汰的原則***

- 
            [UserAgentClientHintsEnabled](/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) 啟用 User-Agent 用戶端提示功能

## <a name="version-93096152-september-16"></a>版本 93.0.961.52：9 月 16 日

>[!Important]
>此更新包括 Chromium 小組報告的 [CVE-2021-30633](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) 的修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊, 請參閱[安全性更新導覽](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於 [此處](/deployedge/microsoft-edge-relnotes-security#september-16-2021)。

## <a name="version-93096147-september-11"></a>版本 93.0.961.47: 9 月 11 日

> [!Important]
> 此更新包括 Chromium 小組報告的 [CVE-2021-30632](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30632) 的修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊, 請參閱[安全性更新導覽](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#september-11-2021)。

## <a name="version-93096144-september-9"></a>版本n 93.0.961.44: 9 月 9 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#september-09-2021)。

## <a name="version-93096138-september-2"></a>版本 93.0.961.38: 9 月 2 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#september-02-2021)。

### <a name="feature-updates"></a>功能更新

- **Microsoft Edge 中的初始喜好設定。**  Microsoft Edge 現在支援數量有限的初始喜好設定 (之前稱為主要喜好設定)。 IT 系統管理員可以在其使用者第一次執行瀏覽器之前，預設部署這些設定。 這裡提供其他資訊：[使用首次執行的初始喜好設定設定來設定 Microsoft Edge](/deployedge/initial-preferences-support-on-microsoft-edge-browser)。

- **Microsoft Edge 上的 IE 模式將支援「不合併」行為。**  針對使用者，從 IE 模式應用程式啟動新瀏覽器視窗時，視窗會處於於不同的工作階段中，類似於 IE11 中的不合併行為。 您必須調整網站清單，以設定由於「不合併」，需要防止工作階段共用的網站。 在幕後，針對 Microsoft Edge 的每個視窗，在該視窗內第一次瀏覽 IE 模式索引標籤時 (如果它是指定的其中一個「不合併」網站)，該視窗會遭鎖定到與所有其他 Microsoft Edge 視窗不同的「不合併」IE 工作階段，至少直到該視窗中的最後一個 IE 模式索引標籤關閉為止。 此行為會遵循先前的行為，其中使用者可以在不合併的情況下啟動 IE，也可以透過其他機制在不合併的情況下啟動 Microsoft Edge。  這裡提供其他資訊：[IE 模式疑難排解和常見問題集 | Microsoft Docs](/deployedge/edge-ie-mode-faq#does-ie-mode-on-microsoft-edge-support-the--nomerge--option-that-was-supported-in-internet-explorer-11-)

- **停止隱含登入的新原則。**  
            [ImplicitSignInEnabled](/deployedge/microsoft-edge-policies#implicitsigninenabled) 原則會允許系統管理員停用 Microsoft Edge 瀏覽器上的隱含登入。

- **可略過 ClickOnce 和 DirectInvoke 提示的原則。** 我們已更新我們的原則，以針對來自指定網域的指定檔案類型，啟用略過 ClickOnce 的提示和 DirectInvoke 的應用程式。 若要這樣做，您必須：

  - 啟用 [ClickOnceEnabled](/deployedge/microsoft-edge-policies#clickonceenabled) 或 [DirectInvokeEnabled](/deployedge/microsoft-edge-policies#directinvokeenabled)
  - 啟用 [AutoOpenFileTypes](/deployedge/microsoft-edge-policies#autoopenfiletypes) 原則，並設定應停用 ClickOnce 和 DirectInvoke 的特定檔案類型清單。
  - 啟用 [AutoOpenAllowedForURLs](/deployedge/microsoft-edge-policies#autoopenallowedforurls) 原則，並設定將停用 ClickOnce 和 DirectInvoke 的特定網域清單。

  注意：AutoOpenAllowedForURLs 是 AutoOpenFileTypes 的支援原則。 如果未設定 AutoOpenAllowedForURLs 且已設定 AutoOpenFileTypes，則列出的檔案類型將自動從所有 URL 開啟。

- **索引標籤群組。**  我們正在開啟索引標籤群組，其提供將索引標籤分類為使用者定義群組的功能，並幫助您更有效地尋找、切換及管理多個工作流程的索引標籤。  

- **使用垂直索引標籤時隱藏標題列。**  在垂直索引標籤中時隱藏瀏覽器的標題列，以獲得額外的一些像素。 現在，您可以前往 edge://settings/appearance，並在 [自訂工具列] 區段下選取在垂直索引標籤模式中隱藏標題列的選項。

- **透過暫留工具列的影片子母畫面 (PiP)。**  當您將游標暫留在支援的影片上時，會出現一個工具列，允許您在 PiP 視窗中觀看該影片。  請注意：這目前適用 macOS 上的 Microsoft Edge 使用者。  

- **移除 TLS 中的 3DES。 將移除對 TLS_RSA_WITH_3DES_EDE_CBC_SHA加密套件的支援。** 此變更會在 Microsoft Edge 所根據的 Chromium 專案中發生。 如需詳細資訊，請瀏覽至 [Chrome 平台狀態項目](https://chromestatus.com/feature/6678134168485888)。 此外，在 Microsoft Edge 版本 93 中，[TripleDESEnabled](/deployedge/microsoft-edge-policies#tripledesenabled) 原則將可用來支援需要保留與過時伺服器相容性的情況。 此相容性原則將在 Microsoft Edge 版本 95 中過時並停止運作。 請確定在此之前更新受影響的伺服器。

***新原則***

- 
            [AutoplayAllowlist](/DeployEdge/microsoft-edge-policies#autoplayallowlist) 允許媒體在特定的網站上自動播放
- 
            [CECPQ2Enabled](/DeployEdge/microsoft-edge-policies#cecpq2enabled) 已啟用 TLS 的 CECPQ2 後量子金鑰協定
- 
            [ConfigureViewInFileExplorer](/DeployEdge/microsoft-edge-policies#configureviewinfileexplorer) 在 Microsoft Edge 中設定適用於 SharePoint 頁面的 [在檔案總管中檢視] 功能
- 
            [DefaultJitSetting](/DeployEdge/microsoft-edge-policies#defaultjavascriptjitsetting) 控制 JavaScript JIT 的使用
- 
            [ShowPDFDefaultRecommendationsEnabled](/DeployEdge/microsoft-edge-policies#showpdfdefaultrecommendationsenabled) 允許通知將 Microsoft Edge設為預設的 PDF 閱讀程式
- 
            [FeatureFlagOverridesControl](/DeployEdge/microsoft-edge-policies#featureflagoverridescontrol) 設定使用者可覆寫功能旗標的能力
- 
            [ImplicitSignInEnabled](/DeployEdge/microsoft-edge-policies#implicitsigninenabled) 啟用隱含登入
- 
            [InternetExplorerIntegrationCloudSiteList](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationcloudsitelist) 設定企業模式雲端網站清單
- 
            [InternetExplorerIntegrationSiteListRefreshInterval](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsitelistrefreshinterval) 設定重新整理企業模式網站清單的頻率
- 
            [JavaScriptJitAllowedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitallowedforsites) 允許 JavaScript 在這些網站上使用 JIT
- 
            [JavaScriptJitBlockedForSites](/DeployEdge/microsoft-edge-policies#javascriptjitblockedforsites) 封鎖 JavaScript 以防止在這些網站上使用 JIT
- 
            [LocalBrowserDataShareEnabled](/DeployEdge/microsoft-edge-policies#localbrowserdatashareenabled) 讓 Windows 搜尋本機 Microsoft Edge 瀏覽資料
- 
            [MAUEnabled](/DeployEdge/microsoft-edge-policies#mauenabled) 一律使用 Microsoft AutoUpdate 做為 Microsoft Edge 的更新程式
- 
            [MSAWebSiteSSOUsingThisProfileAllowed](/DeployEdge/microsoft-edge-policies#msawebsitessousingthisprofileallowed) 允許使用此設定檔的單一登入 Microsoft 網站
- 
            [OneAuthAuthenticationEnforced](/DeployEdge/microsoft-edge-policies#oneauthauthenticationenforced) 已針對登入強制執行的 OneAuth 驗證流程
- 
            [PasswordGeneratorEnabled](/DeployEdge/microsoft-edge-policies#passwordgeneratorenabled) 允許使用者在線上建立帳戶時，取得強式密碼建議
- 
            [PrimaryPasswordSetting](/DeployEdge/microsoft-edge-policies#primarypasswordsetting) 設定要求使用者在使用密碼自動填寫時輸入其裝置密碼的設定
- 
            [PrintingWebpageLayout](/DeployEdge/microsoft-edge-policies#printingwebpagelayout) 設定列印版面配置
- 
            [RemoteDebuggingAllowed](/DeployEdge/microsoft-edge-policies#remotedebuggingallowed) 允許遠端偵錯
- 
            [RelaunchWindow](/DeployEdge/microsoft-edge-policies#relaunchwindow) 設定重新開機的時間間隔
- 
            [TravelAssistanceEnabled](/DeployEdge/microsoft-edge-policies#travelassistanceenabled) 啟用差旅協助
- 
            [TripleDESEnabled](/DeployEdge/microsoft-edge-policies#tripledesenabled) 在 TLS 中啟用 3DES 加密套件
- 
            [WAMAuthBelowWin10RS3Enabled](/DeployEdge/microsoft-edge-policies#wamauthbelowwin10rs3enabled) 已啟用驗證低於 Windows 10 RS3 以下的 WAM

***取代的原則***

- 
            [LegacySameSiteCookieBehaviorEnabled](/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) 啟用預設舊版 SameSite Cookie 行為設定

***淘汰的原則***

- 
            [NewTabPageSetFeedType](/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) 設定 Microsoft Edge 新增索引標籤頁面體驗

***其他變更***

- 
            [ConfigureShare](/DeployEdge/microsoft-edge-policies#configureshare) 新增 Mac 平台支援
- 
            [PasswordMonitorAllowed](/DeployEdge/microsoft-edge-policies#passwordmonitorallowed) 新增 Mac 平台支援

## <a name="version-92090284-august-26"></a>版本 92.0.902.84：8 月 26 日

已修正各種錯誤和效能問題。

## <a name="version-92090278-august-19"></a>版本 92.0.902.78：8 月 19 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#august-19-2021)。

## <a name="version-92090273-august-12"></a>版本 92.0.902.73：8 月 12 日

已修正各種錯誤和效能問題。

## <a name="version-92090267-august-5"></a>版本 92.0.902.67：8 月 5 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#august-05-2021)。

## <a name="version-92090262-july-29"></a>版本 92.0.902.62：7 月 29 日

已修正各種錯誤和效能問題。

### <a name="modified-policy"></a>已修改的原則

- AutoplayAllowed – 目前的「已停用」設定會將媒體自動播放設為「有限的」

## <a name="version-92090255-july-22"></a>版本 92.0.902.55: 7 月 22 日

穩定通道安全性更新列於 [此處](/deployedge/microsoft-edge-relnotes-security#july-22-2021)。

### <a name="feature-updates"></a>功能更新


            **使用者可以在 Microsoft Edge 上輕鬆進入 Internet Explorer 模式**。 從 Microsoft Edge 版本 92 開始，使用者可以在 Microsoft Edge 上重新載入 Internet Explorer 模式的網站，而不需要依賴獨立的 IE 11 應用程式，同時等待在企業模式網站清單中設定網站。 系統會提示使用者將網站新增到其本機網站清單，以便在接下來的 30 天內，瀏覽至 Microsoft Edge 中的相同頁面將會在 IE 模式下自動轉譯。 您可以使用 [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 原則設定此體驗，並允許存取 IE 模式進入點，而且能夠將網站新增到本機網站清單。 您可以使用 [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) 原則以調整將網站保留在本機網站清單中的天數。 請注意，Windows 10 版本 1909 需要 KB5003698 或更新版本；Windows 10 版本 2004、Windows 10 版本 20H2 或 Windows 10 版本 21H1 需要 KB5003690 或更新版本，才能提供端對端體驗。 如需詳細資訊，請參閱 [IE 模式中的本機網站清單](/deployedge/edge-ie-mode-local-site-list)。


            **MHTML 檔案將預設為在 Internet Explorer 模式下開啟**。 從 Microsoft Edge 版本 92 Stable 開始，MHTML 檔案類型將會在 Microsoft Edge (而非 Internet Explorer (IE11) 應用程式) 上自動以 Internet Explorer 模式開啟。 這是在瀏覽器中嘗試檢視 Outlook 電子郵件時最常觀察到的情況。 只有在 IE11 是此檔案類型的預設處理常式時，才能進行此變更。 如果您想要變更這項設定，可以在使用 [本指南](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 安裝 Stable 92 版更新之前執行此操作。


            **「停用開發人員模式擴充功能」警告可能會關閉 2 周的時間**。 從 Microsoft Edge 版本 92 開始，您可以選取警告對話方塊下拉式清單中的選項，將警告「停用開發人員模式延伸」延遲 2 周。


            **從工具列管理擴充功能**。 工具列上全新的擴充功能功能表將讓您輕鬆地隱藏/釘選擴充功能。 管理延伸和尋找新延伸的快速連結將使您輕鬆找到新延伸和管理現有延伸。


            **自動播放的預設值會設定為限制**。  為協助您將焦點維持在線上，我們已將自動播放媒體的預設值從 [允許] 變更為 [有限的]，從 Microsoft Edge 版本 92 開始。


            **付款方式現在會跨裝置同步處理**。 從 Microsoft Edge 版本 92 開始，您可以選擇在所有已登入的裝置上同步處理您的付款資訊。 請注意：此為受控功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。
目前此功能僅適用於美國，且僅適用於 MSA 使用者 (AAD) 


            **字型呈現的改善**。 已改善文字的呈現，以提高清晰度並減少模糊度。 請注意：此為受控功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。


            **工具列按鈕功能，例如 [我的最愛] 和 [收藏]，會記住使用者將其釘選到視窗側邊的選擇**。 現在預設為啟用，如果使用者選擇釘選工具列按鈕，它一律會以釘選狀態開啟，直到他們決定取消釘選。


            **使用者現在可以透過群組原則，'允許使用此設定檔選項單一登入公司或學校網站'**。  '允許使用此設定檔，單一登入工作或學校網站' 可讓非 AAD 設定檔得以使用電腦上存在的工作或學校認證，單一登入工作或學校網站。 對使用者來說，此選項在 [設定] -> [設定檔] -> [僅限非 AAD 設定檔的設定檔喜好設定] 中會顯示為切換開關。  您可以使用 [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 原則以設定行為。  


            **密碼健康情況** 在各帳戶間使用強大且唯一的密碼，以保持線上安全是非常重要的。 不過，這說起來容易做起來難，而且大多數使用者都有不良的密碼習慣，像是使用容易猜測的弱密碼，或重複使用跨帳戶上的相同強式密碼。

有了這個最新版本的 Microsoft Edge，使用強大且唯一密碼的工作會變得更輕鬆一些！ Microsoft Edge 現在會告訴您儲存的密碼是否夠強，並且也會指出這些密碼是否已在多個網站上使用，可協助您保持更安全的線上狀態。 您可以在 edge://settings/passwords 頁面之已儲存密碼清單中找到密碼健康情況資訊。
  

            **為您已儲存的密碼新增隱私權** 如果您使用的是與他人共用、或因為任何原因讓電腦解除鎖定的裝置，您現在可以選擇使用裝置密碼進行第二次驗證，以避免其他人存取您的網站密碼。 簡單！


            **Outlook 副檔名**。  隨時掌握您的 Microsoft Outlook 收件匣、行事曆、工作等其他功能，無需開啟新的瀏覽器視窗。  您可以在這裡取得新的 Microsoft Outlook 擴充功能：[Microsoft Outlook - Microsoft Edge 附加元件](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)


            **為了與 Chromium 開放原始碼專案保持一致，Microsoft Edge 將更新其在網頁上呈現表格的方式**。 此變更可修正已知問題，並讓 Microsoft Edge 更接近表格在網頁/其他瀏覽器中呈現的指定方式。 建議您測試環境中的重要工作流程，以檢查非預期的問題。 完整的解說程式可以在[這裡](https://docs.google.com/document/d/16PFD1GtMI9Zgwu0jtPaKZJ75Q2wyZ9EZnVbBacOfiNA/edit)取得。

### <a name="new-policies"></a>新原則

- 
            [AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 已啟用使用此設定檔單一登入公司或學校網站。
- 
            [AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) 設定自動 HTTPS
- 
            [HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) 控制無周邊模式的使用
- 
            [InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 指定是否要允許不安全的網站向較私人的網路端點提出要求
- 
            [InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) 允許列出的網站從不安全的內容對較私人的網路端點提出要求
- 
            [InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) 指定網站保留在本機 IE 模式網站清單上的天數
- 
            [InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 允許未設定的網站在 Internet Explorer 模式下重新載入
- 
            [SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) 指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用

### <a name="deprecated-policy"></a>取代的原則

- 
            [InternetExplorerIntegrationTestingAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - 允許 Internet Explorer 模式測試

### <a name="obsoleted-policy"></a>淘汰的原則

- 
            [EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) 允許由本機信賴起點頒發的 SHA-1 簽章憑證

## <a name="version-91086471-july-19"></a>版本 91.0.864.71: 7 月 19 日

> [!Important]
>此更新包括 Chromium 小組已舉報的 [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563) 修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊, 請參閱 [安全性更新導覽](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於 [此處](/deployedge/microsoft-edge-relnotes-security#july-19-2021)。

## <a name="version-91086467-july-8"></a>版本 91.0.864.67: 7 月 8 日

已修正各種錯誤和效能問題。

## <a name="version-91086464-july-2"></a>版本 91.0.864.64: 7 月 2 日

已修正各種錯誤和效能問題。

## <a name="version-91086459-june-24"></a>版本 91.0.864.59：6 月 24 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-24-2021)。

## <a name="version-91086454-june-18"></a>版本 91.0.864.54：6 月 18 日

> [!Important]
> 此更新包括 Chromium 小組已舉報的 [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554) 修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊, 請參閱 [安全性更新導覽](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-18-2021)。

## <a name="version-91086448-june-11"></a>版本 91.0.864.48：6 月 11 日

> [!Important]
>此更新包括 Chromium 小組報告 [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551) 的修正, 因為已發行的版本中有惡意探索問題。 如需詳細資訊, 請參閱 [安全性更新導覽](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-11-2021)。

## <a name="version-91086441-june-3"></a>版本 91.0.864.41：6 月 3 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-3-2021)。

## <a name="version-91086437-may-27"></a>版本 91.0.864.37：5 月 27 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#may-27-2021)。

### <a name="feature-updates"></a>功能更新

- 
            **在 Proxy 層級識別來自 Microsoft Defender 應用程式防護容器的流量**。 從 Microsoft Edge 版本 91 開始，內建支援以標記來自應用程式防護容器的流量，讓企業能夠識別它們並套用特定原則。

- 
            **支援選項，讓 [我的最愛] 從主機同步處理至 Edge 應用程式防護容器**。 從 Microsoft Edge 版本 91 開始，使用者可以選擇設定應用程式防護，將其 [我的最愛] 從主機同步處理至容器。 這可確保容器上也會出現新的 [我的最愛]。

- 
            **從 Microsoft Edge 版本 91 開始，瀏覽器會自動中斷類型下載，這些下載若在未經使用者互動的情況下啟動，且不受 SmartScreen 應用程式評價檢查支援，這些下載可能會危害您的電腦**。 使用者可以在下載項目上按一下滑鼠右鍵並選擇「保留」，以覆寫並繼續下載。 透過設定下列原則，企業系統管理員可以退出宣告此行為：
  - 
            [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警示

    如需詳細資訊，請參閱　[Microsoft Edge 安全性下載中斷](microsoft-edge-security-downloads-interruptions.md)。

- 
            **支援語音辨識 API**。 從 Microsoft Edge 版本 91 開始，將會新增對 Google.com 和類似網站的語音辨識命令 API 支援。 此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

- 
            **使用新的佈景主題色彩以個人化您的瀏覽器**。 使用設定 -> 外觀頁面上的十四種新佈景主題色彩的其中一種，將 Microsoft Edge 個人化。 您也可以從 Microsoft Edge 附加元件網站安裝自訂佈景主題。 [深入了解](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

已新增六個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：

- 
            [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) -　應用程式防護流量識別
- 
            [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - 明確允許的網路連接埠
- 
            [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - 允許匯出啟動頁面設定
- 
            [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - 讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案
- 
            [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - 允許新分頁頁面上的 Microsoft 新聞內容
- 
            [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - 允許新分頁頁面上的快速連結

#### <a name="obsoleted-policy"></a>淘汰的原則

- 
            [ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - 啟用主動式驗證
<!-- end major 91 -->

<!-- Archive from 89.0.774.45: March 4 to 90.0.818.66: May 20 ->
<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
