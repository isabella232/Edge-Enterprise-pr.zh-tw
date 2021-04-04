---
title: Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 04/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: 31aaad801f4632985d7fc9d043155f2eb82ed046
ms.sourcegitcommit: 21390f52f8605fe6cb0b73ca6dffacff562ada82
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "11470901"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。



- 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。
- 封存的 Microsoft Edge 穩定通道的版本資訊在[此處](microsoft-edge-relnote-archive-stable-channel.md)。

 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。

> [!NOTE]
> 針對穩定通道，更新會在一或多天內逐步推出。 若要深入了解，請參閱[適用於 Microsoft Edge 更新的漸進式推出](microsoft-edge-update-progressive-rollout.md)。

## <a name="version-89077468-april-1"></a>版本 89.0.774.68：4 月 1 日

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#april-1-2021)。

## <a name="version-89077463-march-25"></a>版本 89.0.774.63：3 月 25 日

修正各種錯誤和效能問題。

## <a name="version-89077457-march-18"></a>版本 89.0.774.57：3 月 18 日

修正各種錯誤和效能問題。

## <a name="version-89077454-march-13"></a>版本 89.0.774.54：3 月 13 日

> [!IMPORTANT]
> 此更新包含 Chromium 小組報告的 [CVE-2021-21193](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21193)，因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#march-13-2021)。

## <a name="version-89077450-march-10"></a>版本 89.0.774.50：3 月 10 日

修正各種錯誤和效能問題。

## <a name="version-89077448-march-8"></a>版本 89.0.774.48：3 月 8 日

修正各種錯誤和效能問題。

<!-- begin major 89 -->
## <a name="version-89077445-march-4"></a>版本 89.0.774.45：3 月 4 日

> [!IMPORTANT]
> 此更新包含已由 Chromium 小組報告為已在市面上有惡意探索問題的 [CVE-2021-21166](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21166)。 如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](./microsoft-edge-relnotes-security.md#march-4-2021)。

### <a name="resolved-issues"></a>解決的問題

- **工作列和開始功能表捷徑的更新和修正：**
  - 現在以滑鼠右鍵按一下開始功能表中的 Microsoft Edge 捷徑，會正確顯示當釘選 Microsoft Edge 時，可從工作列將它加以取消釘選的選項。
  - 包含將 Microsoft Edge 釘選至工作列之 [工作列設定][ ](/windows/configuration/configure-windows-10-taskbar) 的開始版面配置並不再會導致將第二個 Microsoft Edge 捷徑釘選至工作列的結果。
  - 使用 Windows 漫遊設定檔的組織在其使用者登入 Windows 時，不會再於工作列上 Microsoft Edge 圖示的地點僅看到看到空白圖示。

### <a name="feature-updates"></a>功能更新

- **Kiosk 模式可啟用其他鎖定功能**。 從 Microsoft Edge 版本 89 開始，我們在 kiosk 模式下新增了其他鎖定功能，使客戶能夠在高效和更安全的體驗中完成工作。 [進一步了解](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features)。

- **您可以透過*edge://compat*頁面在瀏覽器中使用 [企業模式] 網站清單管理員工具**。 可以使用此工具在 Microsoft Edge 上為 Internet Explorer 模式建立、編輯和匯出網站清單 XML。 可視需要透過群組原則啟用對此工具的存取。 [深入了解](./edge-ie-mode-site-list-manager.md)。

- **使用休眠索引標籤改善瀏覽器效能**。 睡眠索引標籤會透過將非作用中索引標籤置於睡眠，以釋放系統資源 (例如記憶體和 CPU)，以供使用中索引標籤或其他應用程式使用。 使用者可以防止網站進入睡眠，並設定非作用中索引標籤進入睡眠之前的時間長度。 若要讓使用者保持在流程中，您也可以透過 [啟發](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) 式來防止特定網站進入睡眠狀態，例如內部網路網站。 您可以使用群組原則來管理此功能。

- **手動重設雲端中的 Microsoft Edge 同步處理資料**。 我們正在推出一種從產品內部重設 Microsoft Edge 同步處理的方法。 這確保從 Microsoft 服務中清除您的資料，同時也解決了以前需要支援票證的某些產品問題。

- **單一非 Azure AD Microsoft Edge 設定檔使用者的所有 Windows Azure Active Directory (Azure AD) 帳戶智慧型啟用單一登入 (SSO)**。  自動為可從此功能獲得最大益處的使用者開啟此設定。 如果使用者只有一個 Microsoft Edge 設定檔 (且不是 Azure AD 或兒童模式)，則當 Microsoft Edge 啟動時，系統會自動開啟設定。 如果使用者稍後選擇使用 Azure AD 帳戶來登入不同的 Microsoft Edge 設定檔，此自動切換也會自動關閉。 使用者可以在 **設定 > 設定檔 > 設定檔喜好設定 > 允許單一登入公司或學校網站使用此設定檔** 來手動更新此功能的喜好設定。

- **PDF 檔文字選取體驗的改良功能**。 從版本 89 開始，使用者將開始在 Microsoft Edge 中開啟的 PDF 文件中取得更順暢、一致的文字選取體驗。

- **自動填寫現在支援出生日期欄位**。 現在，Microsoft Edge 透過自動填寫位址、姓名、電話號碼等資料，協助您線上填寫表單和建立帳戶時節省時間和精力。從 Microsoft Edge 版本 89 開始，我們將新增對另一可儲存及自動填寫欄位的支援—出生日期。 您可以隨時在設定檔設定中檢視、編輯和刪除此資訊。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 7 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則。

- [BrowsingDataLifetime](./microsoft-edge-policies.md#browsingdatalifetime) - 瀏覽資料存留期設定
- [MAMEnabled](./microsoft-edge-policies.md#mamenabled) - 已啟用行動裝置應用程式管理
- [DefinePreferredLanguages](./microsoft-edge-policies.md#definepreferredlanguages) - 定義網站支援語言時，網站應該顯示的慣用語言排序清單
- [ShowRecommendationsEnabled](./microsoft-edge-policies.md#showrecommendationsenabled) - 允許來自 Microsoft Edge 的建議和促銷通知
- [PrintingAllowedBackgroundGraphicsModes](./microsoft-edge-policies.md#printingallowedbackgroundgraphicsmodes) - 限制背景圖形列印模式
- [PrintingBackgroundGraphicsDefault](./microsoft-edge-policies.md#printingbackgroundgraphicsdefault) - 預設背景圖形列印模式
- [SmartActionsBlockList](./microsoft-edge-policies.md#smartactionsblocklist) - 封鎖服務清單的智慧動作

#### <a name="obsoleted-policies"></a>淘汰的原則

下列原則已過時。

- [ForceLegacyDefaultReferrerPolicy](./microsoft-edge-policies.md#forcelegacydefaultreferrerpolicy) - 使用預設的查閱者原則 no-referrer-when-downgrade
- [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告
- [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務
<!-- end major 89 -->
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
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled) - 啟用啟動提升。
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

新增了 10 個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列原則。

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

<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)