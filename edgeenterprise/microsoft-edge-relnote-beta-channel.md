---
title: Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 03/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: f2fde765cffcc546a2bd64d931c58e7a460d260c
ms.sourcegitcommit: 50bf27680754f4cfde4112e5e618d862c2919ac3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/23/2021
ms.locfileid: "11445242"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Microsoft Edge Beta 通道的版本資訊

這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。 這些版本資訊的封存版本可在[此處](microsoft-edge-relnote-archive-beta-channel.md)取得。

> [!NOTE]
> 我們已更新 Microsoft Edge Beta [版本 89.0.774.18：2 月 3 日](#version-89077418-february-3)版本資訊，以反映已推出的功能。

## <a name="version-90081814-march-22"></a>版本 90.0.818.14：3 月 22 日

修正各種錯誤和效能問題。
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a>版本 90.0.818.8：3 月 16 日

### <a name="feature-updates"></a>功能更新

- **單一登入 (SSO) 目前可供 macOS 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用**。 在 macOS 上，在 Microsoft Edge 上登入的使用者現在會自動進入網站，這些網站已設定為允許使用 Work 和 Microsoft 帳戶 (例如 bing.com、office.com、msn.com 和 outlook.com) 進行單一登入。

- **列印：**

  - **非 PostScript 印表機的新列印點陣化模式**。 從 Microsoft Edge 版本 90 開始，系統管理員可以使用新原則來定義其使用者的列印點陣化模式。 此原則可控制 Microsoft Edge 列印至 Windows 上非 PostScript 印表機的方式。  有時需將非 PostScript 印表機上的列印工作點陣化才能正確列印。 列印選項為「完整」和「快速」。

  - **用於列印的其他頁面縮放選項**。 使用者現在能夠自訂縮放比例，同時使用其他選項列印網頁和 PDF 文件。 「符合頁面大小」選項可確保網頁或文件符合所選「紙張大小」可供列印的空間。 [實際大小] 選項可確保無論選取的 [紙張大小] 為何，列印內容的大小都不會變更。

- **生產力：**

  - **延伸自動填寫建議，以包含來自剪貼簿的地址欄位內容**。 當您按一下設定檔/地址欄位 (例如，電話、電子郵件、郵遞區號、縣/市、省/市等) 以顯示為自動填寫建議時，系統將會剖析剪貼簿內容。

  - **即使未偵測到表單或欄位，使用者也可以搜尋自動填寫建議**。 現在，如果您將您的資訊儲存在 Microsoft Edge 上，自動填寫建議將自動彈出，並幫助您在填寫表單時節省時間。 如果自動填寫遺漏表單，或您想要在通常沒有自動填寫的表單 (例如暫存表單) 中擷取資料，您可以搜尋您使用自動填寫的資訊。

- **從功能表列的飛出視窗存取下載**。 下載會顯示在右上角，將所有作用中下載顯示在同一個位置。 此功能表可以很輕易關閉，因此使用者可以繼續瀏覽而不受干擾，且他們可以直接從工具列監視整體下載進度。 [進一步了解](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551)。

- **字型呈現的改善**。 從 Microsoft Edge 版本 90 開始，我們改善了文字的呈現，以改善清晰度並減少模糊度。 部分字型呈現改善將在 Beta 版本 90 中推出，但預設會停用。


### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

新增了 7 個原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：

- [ApplicationGuardFavoritesSyncEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) - 已啟用應用程式防護我的最愛同步處理
- [ManagedConfigurationPerOrigin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) - 設定網站到特定來源的受管理設定值
- [PrintRasterizationMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printrasterizationmode) - 列印點陣化模式
- [QuickViewOfficeFilesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - 管理 Microsoft Edge 中的 QuickView Office 檔案功能
- [SSLErrorOverrideAllowedForOrigins](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - 允許使用者從特定來源的 HTTPS 警告頁面繼續進行
- [WindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - 啟用視窗遮蔽
- [WindowsHelloForHTTPAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - 已啟用適用於 HTTP 驗證的 Windows Hello

#### <a name="deprecated-policies"></a>取代的原則

- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - 啟用原生視窗遮蔽
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin) - 已啟用最低 TLS 版本
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
## <a name="version-89077418-february-3"></a>版本 89.0.774.18：2 月 3 日

### <a name="feature-updates"></a>功能更新

- **Kiosk 模式可啟用其他鎖定功能**。 從 Microsoft Edge 版本 89 開始，我們在 kiosk 模式下新增了其他鎖定功能，使客戶能夠在高效和更安全的體驗中完成工作。 [進一步了解](microsoft-edge-configure-kiosk-mode.md#kiosk-mode-supported-features)。

- **您可以透過*edge://compat*頁面在瀏覽器中使用 [企業模式] 網站清單管理員工具**。 可以使用此工具在 Microsoft Edge 上為 Internet Explorer 模式建立、編輯和匯出網站清單 XML。 可視需要透過群組原則啟用對此工具的存取。 [深入了解](https://docs.microsoft.com/deployedge/edge-ie-mode-site-list-manager)。

- **使用休眠索引標籤改善瀏覽器效能**。 睡眠索引標籤會透過將非作用中索引標籤置於睡眠，以釋放系統資源 (例如記憶體和 CPU)，以供使用中索引標籤或其他應用程式使用。 使用者可以防止網站進入睡眠，並設定非作用中索引標籤進入睡眠之前的時間長度。 若要讓使用者保持在流程中，您也可以透過 [啟發](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) 式來防止特定網站進入睡眠狀態，例如內部網路網站。 您可以使用群組原則來管理此功能。

  > [!NOTE]
  > 「使用休眠索引標籤改善瀏覽器效能」是主要版本89.0.774.18 的 2 月 3 日版本更新。

- **手動重設雲端中的 Microsoft Edge 同步處理資料**。 我們正在推出一種從產品內部重設 Microsoft Edge 同步處理的方法。 這確保從 Microsoft 服務中清除您的資料，同時也解決了以前需要支援票證的某些產品問題。

- **PDF 檔中的文字選取體驗的改良功能**。 從版本 89 開始，使用者將開始在 Microsoft Edge 中開啟的 PDF 文件中取得更順暢、一致的文字選取體驗。

- **自動填寫現在支援出生日期欄位**。 現在，Microsoft Edge 透過自動填寫位址、姓名、電話號碼等資料，協助您線上填寫表單和建立帳戶時節省時間和精力。從 Microsoft Edge 版本 89 開始，我們將新增對另一可儲存及自動填寫欄位的支援—出生日期。 您可以隨時在設定檔設定中檢視、編輯和刪除此資訊。

- **在 [位址列]、[歷程記錄] 搜尋頁面和 [歷程記錄中心] 上，都支援自然語言搜尋**。 從 Microsoft Edge 版本 89 開始，使用網址列、歷程記錄頁面和歷程記錄中樞上的自然語言搜尋使尋找文章/網站更容易。 除了標題/URL 關鍵字相符項目之外，使用者還可以搜尋以前檢視過的頁面內容/描述/時間 (如「上週的蛋糕食譜」)。 此功能僅限於已啟用實驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

- [BrowsingDataLifetime](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsingdatalifetime) - 瀏覽資料存留期設定
- [MAMEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#mamenabled) - 已啟用行動裝置應用程式管理
- [DefinePreferredLanguages](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#definepreferredlanguages) - 定義網站支援語言時，網站應該顯示的慣用語言的排序清單
- [ShowRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showrecommendationsenabled) - 允許來自 Microsoft Edge 的建議和促銷通知
- [PrintingAllowedBackgroundGraphicsModes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingallowedbackgroundgraphicsmodes) - 限制背景圖形列印模式
- [PrintingBackgroundGraphicsDefault](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printingbackgroundgraphicsdefault)- 預設背景圖形列印模式
- [SmartActionsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartactionsblocklist)- 封鎖服務清單的智慧型動作

#### <a name="obsoleted-policies"></a>已淘汰的原則

- [ForceLegacyDefaultReferrerPolicy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcelegacydefaultreferrerpolicy) - 使用預設的查閱者原則 no-referrer-when-downgrade
- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務
<!-- end major 89 -->

## <a name="version-88070556-january-29"></a>版本 88.0.705.56：1 月 29 日

修正各種錯誤和效能問題。

## <a name="version-88070549-january-20"></a>版本 88.0.705.49：1 月 20 日

修正各種錯誤和效能問題。

## <a name="version-88070545-january-15"></a>版本 88.0.705.45：1 月 15 日

修正各種錯誤和效能問題。

## <a name="version-88070541-january-11"></a>版本 88.0.705.41：1 月 11 日

修正各種錯誤和效能問題。

## <a name="version-88070529-december-21"></a>版本 88.0.705.29：12 月 21 日

修正各種錯誤和效能問題。

<!-- begin major 88 -->
## <a name="version-88070518-december-9"></a>版本 88.0.705.18：12 月 9 日

### <a name="feature-updates"></a>功能更新

- **取代的項目：**

  - 取代 FTP 通訊協定的支援。 已從 Microsoft Edge 移除對舊版 FTP 通訊協定的支援。 嘗試瀏覽至 FTP 連結會造成瀏覽器將作業系統導向開啟外部應用程式以處理 FTP 連結。 或者，IT 系統管理員可以設定 Microsoft Edge，以對仰賴於 FTP 通訊協定的網站使用 IE 模式。
  - 將移除對 Adobe Flash 的支援。 從 Microsoft Edge Beta 版本 88 開始，將會移除 Adobe Flash 功能和支援。 深入了解：[Adobe Flash Player 終止支援的更新 - Microsoft Edge 部落格 (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **驗證：**

  - 單一登入 (SSO) 目前可供 macOS 和下層 Windows 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用。 在 macOS 或下層 Microsoft Windows (7、8.1) 上於 Microsoft Edge 登入的使用者，現在會自動登入已設定為允許使用公司和 Microsoft 帳戶進行單一登入的網站 (例如，bing.com、office.com、msn.com、outlook.com)。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。
  - 在 macOS 上針對使用其公司帳戶驗證的網站，自動將使用者切換至其公司設定檔。 從 Microsoft Edge 版本 88 開始，我們提供功能，讓您在 macOS 上切換使用使用者的工作設定檔進行驗證的網站。<br>注意：如果使用者在早於 Microsoft Edge 88 的版本中登入 Microsoft Edge 以使用此功能，則使用者可能需要登出，然後再重新登入。

- **結束工作階段的 kiosk 模式選項**。 「結束工作階段」按鈕現在可於 kiosk 模式公開瀏覽體驗中使用。 此功能可確保在 Microsoft Edge 關閉時，瀏覽器資料和設定隨即會刪除。 深入了解 kiosk 模式功能和藍圖，[設定 Microsoft Edge kiosk 模式](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)。

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

### <a name="policy-updates"></a>原則更新

#### <a name="new-policies"></a>新原則

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

#### <a name="deprecated-policies"></a>取代的原則

下列原則已取代。

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - 啟用主動式驗證。
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - 啟用主動式驗證。
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - 設定 Proxy 伺服器設定。
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - 設定 Proxy .pac 檔案 URL。
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - 設定 Proxy 伺服器的位址或 URL。
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - 允許 WebDriver 覆寫不相容原則。

#### <a name="obsoleted-policies"></a>淘汰的原則

下列原則已過時。

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - 預設 Adobe Flash 設定。
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - 允許特定網站上的 Adobe Flash 外掛程式。
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - 封鎖特定網站上的 Adobe Flash 外掛程式。
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - 將 Adobe Flash 內容設定延伸至所有內容。

<!-- end major 88 -->

## <a name="version-87066455-december-3"></a>版本 87.0.664.55：12 月 3 日

修正各種錯誤和效能問題。 此版本支援下列新功能。

- **如果在線上洩漏中發現使用者的密碼，就會產生警示**。 系統會針對已知違例認證的儲存庫檢查使用者密碼，並在找到相符專案時傳送通知給使用者。 若要確保安全性與隱私權，請在針對洩漏認證的資料庫檢查使用者密碼時，對其進行雜湊處理和加密。

## <a name="version-87066452-november-30"></a>版本 87.0.664.52：11 月 30 日

修正各種錯誤和效能問題。

## <a name="version-87066440-november-18"></a>版本 87.0.664.40：11 月 18 日

修正各種錯誤和效能問題。

## <a name="version-87066436-november-16"></a>版本 87.0.664.36：11 月 16 日

修正各種錯誤和效能問題。

## <a name="version-87066430-november-9"></a>版本 87.0.664.30：11 月 9 日

修正各種錯誤和效能問題。

## <a name="version-87066424-november-2"></a>版本 87.0.664.24：11 月 2 日

修正各種錯誤和效能問題。

## <a name="version-87066418-october-26"></a>版本 87.0.664.18：10 月 26 日

修正各種錯誤和效能問題。

<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
