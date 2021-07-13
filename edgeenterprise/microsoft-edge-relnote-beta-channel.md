---
title: Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: d5e4a4807a12cfd50cd0efaeab672361c68a1508
ms.sourcegitcommit: e3a30351b02226aa042153f17636d64a12c4518b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643939"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a>Microsoft Edge Beta 通道的版本資訊

這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。 這些版本資訊的封存版本可在[此處](microsoft-edge-relnote-archive-beta-channel.md)取得。

> [!NOTE]
> Microsoft Edge Web 平台不斷演進，以改善使用者體驗、安全性和隱私權。 若要深入了解，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。

## <a name="version-92090245-july-12"></a>版本 92.0.902.45：7 月 12 日

修正各種錯誤和效能問題。

## <a name="version-92090240-july-6"></a>版本 92.0.902.40：7 月 6 日

修正各種錯誤和效能問題。

## <a name="version-92090222-june-21"></a>版本 92.0.902.22：6 月 21 日

### <a name="feature-updates"></a>功能更新

- **自然語言搜尋網址欄上的瀏覽器歷程記錄**。 現在，由於從網址欄搜尋自然語言，尋找您正在尋找的文章/網站變得更容易。 您可以根據頁面內容/描述/時間 (尋找搜尋結果，例如「上周的蛋糕食譜」) 除了標題/URL 關鍵字本身符合之外。
請注意：這是控管功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

- **使用者可以在 Microsoft Edge 上輕鬆進入 Internet Explorer 模式**。 從 Microsoft Edge 版本 92 開始，使用者可以在 Microsoft Edge 上重新載入 Internet Explorer 模式的網站，而不需要依賴獨立的 IE 11 應用程式，同時等待在企業模式網站清單中設定網站。 系統會提示使用者將網站新增到其本機網站清單，以便在接下來的 30 天內，瀏覽至 Microsoft Edge 中的相同頁面將會在 IE 模式下自動轉譯。 您可以使用 *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* 原則設定此體驗，並允許存取 IE 模式進入點，而且能夠將網站新增到本機網站清單。 您可以使用 *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* 原則調整將網站保留在本機網站清單中的天數。
請注意，Windows 10 版本 1909 需要 KB5003698 或更新版本；Windows 10 版本 2004、Windows 10 版本 20H2 或 Windows 10 版本 21H1 需要 KB5003690 或更新版本，才能提供端對端體驗。

- **MHTML 檔案將預設為在 Internet Explorer 模式下開啟**。 從 Microsoft Edge 版本 92 Stable 開始，MHTML 檔案類型將會在 Microsoft Edge (而非 Internet Explorer (IE11) 應用程式) 上自動以 Internet Explorer 模式開啟。 這是在瀏覽器中嘗試檢視 Outlook 電子郵件時最常觀察到的情況。 只有在 IE11 是此檔案類型的預設處理常式時，才能進行此變更。 如果您想要變更這項設定，可以在使用[本指南](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)安裝 Stable 92 版更新之前執行此操作。

- **付款方式現在會跨裝置同步處理**。 從 Microsoft Edge 版本 92 開始，您可以選擇在已登入的裝置上同步處理您的付款資訊。
請注意：這是控管功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

- **「停用開發人員模式擴充功能」警告可能會永久關閉**。 從 Microsoft Edge 版本 92 開始，您可以按一下 [不再顯示此訊息] 選項，以關閉警告 [停用開發人員模式擴充功能]。
請注意：這是控管功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

- **從工具列管理擴充功能**。 工具列上全新的擴充功能功能表將讓您輕鬆地隱藏/釘選擴充功能。 管理延伸和尋找新延伸的快速連結將使您輕鬆找到新延伸和管理現有延伸。
請注意：這是控管功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

- **自動 HTTPS**。 使用者可以選擇在可能支援這個更安全的通訊協定的網域上，將瀏覽從 HTTP 升級至 HTTPS。 此支援也可以設定為嘗試針對所有網域，透過 HTTPS 傳遞。
請注意：我們正在實驗這項功能，如果您退出宣告實驗，將不會看到此行為。

- **字型呈現的改善**。 已改善文字的呈現，以提高清晰度並減少模糊度。
請注意：這是控管功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

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
