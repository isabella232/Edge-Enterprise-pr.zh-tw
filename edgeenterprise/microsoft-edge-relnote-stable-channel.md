---
title: Microsoft Edge 穩定通道的版本資訊
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 07/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 穩定通道的版本資訊
ms.openlocfilehash: 02d4f2fc96215902000d30f37b589ea126496e47
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/23/2021
ms.locfileid: "11676060"
---
# <a name="release-notes-for-microsoft-edge-stable-channel"></a>Microsoft Edge 穩定通道的版本資訊

這些版本資訊提供 Microsoft Edge 穩定通道中包含的新功能和非安全性更新的相關資訊。

- 所有安全性更新列於[此處](microsoft-edge-relnotes-security.md)。
- 封存的 Microsoft Edge 穩定通道的版本資訊在[此處](microsoft-edge-relnote-archive-stable-channel.md)。

 若要了解 Microsoft Edge 通道，請參閱 [Microsoft Edge 通道概觀](microsoft-edge-channels.md)。

> [!NOTE]
> 針對穩定通道，更新會在一或多天內逐步推出。 若要深入了解，請參閱[適用於 Microsoft Edge 更新的漸進式推出](microsoft-edge-update-progressive-rollout.md)。
>
> Microsoft Edge Web 平台不斷演進，以改善使用者體驗、安全性和隱私權。 若要深入了解，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。

## <a name="version-92090255-july-22"></a>版本 92.0.902.55: 7 月 22 日

穩定通道安全性更新列於 [此處](/deployedge/microsoft-edge-relnotes-security#july-22-2021)。

### <a name="feature-updates"></a>功能更新

**使用者可以在 Microsoft Edge 上輕鬆進入 Internet Explorer 模式**。 從 Microsoft Edge 版本 92 開始，使用者可以在 Microsoft Edge 上重新載入 Internet Explorer 模式的網站，而不需要依賴獨立的 IE 11 應用程式，同時等待在企業模式網站清單中設定網站。 系統會提示使用者將網站新增到其本機網站清單，以便在接下來的 30 天內，瀏覽至 Microsoft Edge 中的相同頁面將會在 IE 模式下自動轉譯。 您可以使用 [InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 原則設定此體驗，並允許存取 IE 模式進入點，而且能夠將網站新增到本機網站清單。 您可以使用 [InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationday) 原則以調整將網站保留在本機網站清單中的天數。 請注意，Windows 10 版本 1909 需要 KB5003698 或更新版本；Windows 10 版本 2004、Windows 10 版本 20H2 或 Windows 10 版本 21H1 需要 KB5003690 或更新版本，才能提供端對端體驗。

**MHTML 檔案將預設為在 Internet Explorer 模式下開啟**。 從 Microsoft Edge 版本 92 Stable 開始，MHTML 檔案類型將會在 Microsoft Edge (而非 Internet Explorer (IE11) 應用程式) 上自動以 Internet Explorer 模式開啟。 這是在瀏覽器中嘗試檢視 Outlook 電子郵件時最常觀察到的情況。 只有在 IE11 是此檔案類型的預設處理常式時，才能進行此變更。 如果您想要變更這項設定，可以在使用 [本指南](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 安裝 Stable 92 版更新之前執行此操作。

**「停用開發人員模式擴充功能」警告可能會永久關閉**。 從 Microsoft Edge 版本 92 開始，您可以按一下 [不再顯示此訊息] 選項，以關閉警告 [停用開發人員模式擴充功能]。

**從工具列管理擴充功能**。 工具列上全新的擴充功能功能表將讓您輕鬆地隱藏/釘選擴充功能。 管理延伸和尋找新延伸的快速連結將使您輕鬆找到新延伸和管理現有延伸。

**自動播放的預設值會設為 [有限的]**。  為協助您將焦點維持在線上，我們已將自動播放媒體的預設值從 [允許] 變更為 [有限的]，從 Microsoft Edge 版本 92 開始。

**付款方式現在會跨裝置同步處理**。 從 Microsoft Edge 版本 92 開始，您可以選擇在所有已登入的裝置上同步處理您的付款資訊。 請注意：此為受控功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。
目前此功能僅適用於美國，且僅適用於 MSA 使用者 (AAD) 

**字型呈現的改善**。 已改善文字的呈現，以提高清晰度並減少模糊度。 請注意：此為受控功能推出。 如果您看不到此功能，請在我們繼續推出時儘快回來查看。

**工具列按鈕功能，例如 [我的最愛] 和 [收藏]，會記住使用者將其釘選到視窗側邊的選擇**。 現在預設為啟用，如果使用者選擇釘選工具列按鈕，它一律會以釘選狀態開啟，直到他們決定取消釘選。

**使用者現在可以透過群組原則，'允許使用此設定檔選項單一登入公司或學校網站'**。  '允許使用此設定檔，單一登入工作或學校網站' 可讓非 AAD 設定檔得以使用電腦上存在的工作或學校認證，單一登入工作或學校網站。 對使用者來說，此選項在 [設定] -> [設定檔] -> [僅限非 AAD 設定檔的設定檔喜好設定] 中會顯示為切換開關。  您可以使用 [AADWebSiteSSOUsingThisProfileEnabled](/deployedge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 原則以設定行為。  

**密碼健康情況** 在各帳戶間使用強大且唯一的密碼，以保持線上安全是非常重要的。 不過，這說起來容易做起來難，而且大多數使用者都有不良的密碼習慣，像是使用容易猜測的弱密碼，或重複使用跨帳戶上的相同強式密碼。

有了這個最新版本的 Microsoft Edge，使用強大且唯一密碼的工作會變得更輕鬆一些！ Microsoft Edge 現在會告訴您儲存的密碼是否夠強，並且也會指出這些密碼是否已在多個網站上使用，可協助您保持更安全的線上狀態。 您可以在 edge://settings/passwords 頁面之已儲存密碼清單中找到密碼健康情況資訊。
  
**為您已儲存的密碼新增隱私權** 如果您使用的是與他人共用、或因為任何原因讓電腦解除鎖定的裝置，您現在可以選擇使用裝置密碼進行第二次驗證，以避免其他人存取您的網站密碼。 簡單！

**Outlook 副檔名**。  隨時掌握您的 Microsoft Outlook 收件匣、行事曆、工作等其他功能，無需開啟新的瀏覽器視窗。  您可以在這裡取得新的 Microsoft Outlook 擴充功能：[Microsoft Outlook - Microsoft Edge 附加元件](https://microsoftedge.microsoft.com/addons/detail/microsoft-outlook/kkpalkknhlklpbflpcpkepmmbnmfailf?hl=en-US)

### <a name="new-policies"></a>新原則

- [AADWebSiteSSOUsingThisProfileEnabled](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 已啟用使用此設定檔單一登入公司或學校網站。
- [AutomaticHttpsDefault](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#automatichttpsdefault) 設定自動 HTTPS
- [HeadlessModeEnabled](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#headlessmodeenabled) 控制無周邊模式的使用
- [InsecurePrivateNetworkRequestsAllowed](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 指定是否要允許不安全的網站向較私人的網路端點提出要求
- [InsecurePrivateNetworkRequestsAllowedForUrls](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) 允許列出的網站從不安全的內容對較私人的網路端點提出要求
- [InternetExplorerIntegrationLocalSiteListExpirationDays](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) 指定網站保留在本機 IE 模式網站清單上的天數
- [InternetExplorerIntegrationReloadInIEModeAllowed](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 允許未設定的網站在 Internet Explorer 模式下重新載入
- [SharedArrayBufferUnrestrictedAccessAllowed](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) 指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用

### <a name="deprecated-policy"></a>取代的原則

- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - 允許 Internet Explorer 模式測試

### <a name="obsoleted-policy"></a>淘汰的原則

- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/en-US/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) 允許由本機信賴起點頒發的 SHA-1 簽章憑證

## <a name="version-91086471-july-19"></a>版本 91.0.864.71: 7 月 19 日

> [!Important]
>此更新包含 Chromium 小組報告的 [CVE-2021-30563](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30563)，因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱 [安全性更新指南](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於 [此處](/deployedge/microsoft-edge-relnotes-security#july-19-2021)。

## <a name="version-91086467-july-8"></a>版本 91.0.864.67: 7 月 8 日

已修正各種錯誤和效能問題。

## <a name="version-91086464-july-2"></a>版本 91.0.864.64: 7 月 2 日

已修正各種錯誤和效能問題。

## <a name="version-91086459-june-24"></a>版本 91.0.864.59：6 月 24 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-24-2021)。

## <a name="version-91086454-june-18"></a>版本 91.0.864.54：6 月 18 日

> [!Important]
> 此更新包含 Chromium 小組報告的 [CVE-2021-30554](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30554)，因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-18-2021)。

## <a name="version-91086448-june-11"></a>版本 91.0.864.48：6 月 11 日

> [!Important]
>此更新包含 Chromium 小組報告的 [CVE-2021-30551](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-30551)，因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide/vulnerability/ADV200002)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-11-2021)。

## <a name="version-91086441-june-3"></a>版本 91.0.864.41：6 月 3 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#june-3-2021)。

## <a name="version-91086437-may-27"></a>版本 91.0.864.37：5 月 27 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#may-27-2021)。

### <a name="feature-updates"></a>功能更新

- **在 Proxy 層級識別來自 Microsoft Defender 應用程式防護容器的流量**。 從 Microsoft Edge 版本 91 開始，內建支援以標記來自應用程式防護容器的流量，讓企業能夠識別它們並套用特定原則。

- **支援選項，讓 [我的最愛] 從主機同步處理至 Edge 應用程式防護容器**。 從 Microsoft Edge 版本 91 開始，使用者可以選擇設定應用程式防護，將其 [我的最愛] 從主機同步處理至容器。 這可確保容器上也會出現新的 [我的最愛]。

- **從 Microsoft Edge 版本 91 開始，瀏覽器會自動中斷類型下載，這些下載若在未經使用者互動的情況下啟動，且不受 SmartScreen 應用程式評價檢查支援，這些下載可能會危害您的電腦**。 使用者可以在下載項目上按一下滑鼠右鍵並選擇「保留」，以覆寫並繼續下載。 透過設定下列原則，企業系統管理員可以退出宣告此行為：
  - [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings.md) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警示

    如需詳細資訊，請參閱　[Microsoft Edge 安全性下載中斷](microsoft-edge-security-downloads-interruptions.md)。

- **支援語音辨識 API**。 從 Microsoft Edge 版本 91 開始，將會新增對 Google.com 和類似網站的語音辨識命令 API 支援。 此功能僅限於已啟用試驗的隨機選取使用者群組。 這些使用者會向功能小組提供意見反應。

- **使用新的佈景主題色彩以個人化您的瀏覽器**。 使用設定 -> 外觀頁面上的十四種新佈景主題色彩的其中一種，將 Microsoft Edge 個人化。 您也可以從 Microsoft Edge 附加元件網站安裝自訂佈景主題。 [深入了解](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

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

## <a name="version-90081866-may-20"></a>版本 90.0.818.66：5 月 20 日

修正各種錯誤和效能問題。

## <a name="version-90081862-may-13"></a>版本 90.0.818.62：5 月 13 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#may-13-2021)。

## <a name="version-90081856-may-6"></a>版本 90.0.818.56：5 月 6 日

修正各種錯誤和效能問題。

## <a name="version-90081851-april-29"></a>版本 90.0.818.51：4 月 29 日

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#april-29-2021)。

## <a name="version-90081849-april-26"></a>版本 90.0.818.49：4 月 26 日

修正各種錯誤和效能問題。

## <a name="version-90081846-april-22"></a>版本 90.0.818.46：4 月 22 日 ##

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#april-22-2021)。

## <a name="version-90081842-april-19"></a>版本 90.0.818.42：4 月 19 日

修正各種錯誤和效能問題。

## <a name="version-90081841-april-16"></a>版本 90.0.818.41：4 月 16 日 ##

> [!Important]
>此更新包含 Chromium 小組報告的 [CVE-2021-21224](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21224)，因為已發行的版本中有惡意探索問題。 如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#april-16-2021)。

## <a name="version-90081839-april-15"></a>版本 90.0.818.39：4 月 15 日 ##

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#april-15-2021)。

## <a name="feature-updates"></a>功能更新 ##

-    **單一登入 (SSO) 目前可供 macOS 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用。** 在 macOS 上，在 Microsoft Edge 上登入的使用者現在會自動進入網站，這些網站已設定為允許使用 Work 和 Microsoft 帳戶 (例如 bing.com、office.com、msn.com 和 outlook.com) 進行單一登入。

- **Kiosk 模式。** 從 Microsoft Edge 版本 90 開始，我們已鎖定 UI 列印設定，只允許已設定印表機和「列印至 PDF」選項。 我們也在受指派的存取權單一應用程式 kiosk 模式中進行了改善，以限制從瀏覽器啟動其他應用程式。 如需 kiosk 模式功能詳細資訊，請移至 [這裡](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)。

- **中斷下載** 從 Microsoft Edge 版本 91 開始，瀏覽器會自動中斷類型下載，這些下載若在未經使用者互動的情況下啟動，且不受 SmartScreen 應用程式信譽檢查支援，這些下載可能會危害您的電腦。 使用者可以在下載項目上按一下滑鼠右鍵並選擇「保留」，以覆寫並繼續下載。
企業系統管理員可以退出宣告此行為的這兩個原則之一：
- [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名-警告。如需詳細資訊，請參閱 [Microsoft Edge 安全性下載中斷](/deployedge/microsoft-edge-security-downloads-interruptions)

- **列印**：

    - **非 PostScript 印表機的新列印點陣化模式。** 從 Microsoft Edge 版本 90 開始，系統管理員可以使用新原則以定義其使用者的列印點陣化模式。 此原則可控制 Microsoft Edge 列印至 Windows 上非 PostScript 印表機的方式。 有時需將非 PostScript 印表機上的列印工作點陣化才能正確列印。 列印選項為「完整」和「快速」。
    
  - **列印的其他頁面縮放選項。** 使用者現在能夠自訂縮放比例，同時使用其他選項列印網頁和 PDF 文件。 「符合頁面大小」選項可確保網頁或文件符合所選「紙張大小」可供列印的空間。 [實際大小] 選項可確保無論選取的 [紙張大小] 為何，列印內容的大小都不會變更。

-   **生產力：**

    -   **延伸自動填寫建議，以包含剪貼簿中的地址欄位內容。** 當您按一下設定檔/地址欄位 (例如，電話、電子郵件、郵遞區號、縣/市、省/市等) 以顯示為自動填寫建議時，系統將會剖析剪貼簿內容。

    -   **即使未偵測到表單或欄位，使用者也可以搜尋自動填寫建議。** 現在，如果您將您的資訊儲存在 Microsoft Edge 上，自動填寫建議將自動彈出，並幫助您在填寫表單時節省時間。 如果自動填寫遺漏表單，或您想要在通常沒有自動填寫的表單 (例如暫存表單) 中擷取資料，您可以搜尋您使用自動填寫的資訊。

-   **從功能表列的飛出視窗存取下載。** 下載會顯示在右上角，將所有作用中下載顯示在同一個位置。 此功能表可以很輕易關閉，因此使用者可以繼續瀏覽而不受干擾，且他們可以直接從工具列監視整體下載進度。 [進一步了解](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551)。

-   **字型呈現的改善。** 從 Microsoft Edge 版本 90 開始，我們改善了文字的呈現，以改善清晰度並減少模糊度。 部分字型呈現改善將在 Beta 版本 90 中推出，但預設為停用。

- **兒童模式。** 我們已更新此政策，因此當啟用該原則時，除了家長監護服務之外，兒童模式功能會遭到停用。 有關兒童模式 [這裡](https://go.microsoft.com/fwlink/?linkid=2146910)

## <a name="policy-updates"></a>原則更新

## <a name="new-policies"></a>新原則

已新增八個新原則。 從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。 已新增下列新原則：
-   [ApplicationGuardFavoritesSyncEnabled](/DeployEdge/microsoft-edge-policies#applicationguardfavoritessyncenabled) - 已啟用應用程式防護我的最愛同步處理
- [ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) 應用程式防護流量識別
- [ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) 明確允許的網路連接埠
- [ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) 允許匯出啟動頁面設定
- [MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) 讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案
- [NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) 允許新分頁頁面上的 Microsoft 新聞內容
- [NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) 允許新分頁頁面上的快速連結
-   [FetchKeepaliveDurationSOnShutdown](/DeployEdge/microsoft-edge-policies#fetchkeepalivedurationsecondsonshutdown) 擷取關機時的存留持續時間
-   [ManagedConfigurationPerOrigin](/DeployEdge/microsoft-edge-policies#managedconfigurationperorigin) 設定網站到特定來源的受管理設定值
-   [PrintRasterizationMode](/DeployEdge/microsoft-edge-policies#printrasterizationmode) - 列印點陣化模式
-   [QuickViewOfficeFilesEnabled](/DeployEdge/microsoft-edge-policies#quickviewofficefilesenabled) - 管理 Microsoft Edge 中的 QuickView Office 檔案功能
-   [SSLErrorOverrideAllowedForOrigins](/DeployEdge/microsoft-edge-policies#sslerroroverrideallowedfororigins) - 允許使用者從特定來源的 HTTPS 警告頁面繼續進行
-   [WindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#windowocclusionenabled) - 啟用視窗遮蔽
-   [WindowsHelloForHTTPAuthEnabled](/DeployEdge/microsoft-edge-policies#windowshelloforhttpauthenabled) - 已啟用適用於 HTTP 驗證的 Windows Hello

## <a name="deprecated-policies"></a>過時的原則

- [ProactiveAuthEnabled](/DeployEdge/microsoft-edge-policies#proactiveauthenabled) 啟用主動式驗證
-   [NativeWindowOcclusionEnabled](/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - 啟用原生視窗遮蔽
-   [SSLVersionMin](/DeployEdge/microsoft-edge-policies#sslversionmin) - 已啟用最低 TLS 版本

## <a name="version-89077477-april-14"></a>版本 89.0.774.77：4 月 14 日

> [!Important]
>此更新包含 Chromium 小組報告的 [CVE-2021-21206](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21206) 和 [CVE-2021-21220](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-21220)，因為已發行的版本中有惡意探索問題。  如需詳細資訊，請參閱[安全性更新指南](https://msrc.microsoft.com/update-guide)。

穩定通道安全性更新列於[此處](/deployedge/microsoft-edge-relnotes-security#april-14-2021)。

## <a name="version-89077476-april-12"></a>版本 89.0.774.76：4 月 12 日

修正各種錯誤和效能問題。

## <a name="version-89077475-april-8"></a>版本 89.0.774.75：4 月 8 日

修正各種錯誤和效能問題。

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

<!-- Archive from 86.0.622.43: October 15 to beta 88.0.705.81: February 25  ->
<!-- Archive from 86.0.622.38-october-9 to beta 86.0.62.215-september-14  ->
<!-- Archived to version 84.0.522.40: July 16 -->

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
