---
title: Microsoft Edge Beta 通道的版本資訊
ms.author: aguta
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge Beta 通道的版本資訊
ms.openlocfilehash: 1115c8d7822fef7e3784a465d5d4ddfd7b6bd6b1
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643159"
---
# <a name="release-notes-for-microsoft-edge-beta-channel"></a><span data-ttu-id="d9b2a-103">Microsoft Edge Beta 通道的版本資訊</span><span class="sxs-lookup"><span data-stu-id="d9b2a-103">Release notes for Microsoft Edge Beta Channel</span></span>

<span data-ttu-id="d9b2a-104">這些版本資訊提供 Microsoft Edge Beta 通道中包含的新功能和非安全性更新的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-104">These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel.</span></span> <span data-ttu-id="d9b2a-105">這些版本資訊的封存版本可在[此處](microsoft-edge-relnote-archive-beta-channel.md)取得。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-105">Archived versions of these release notes are available [here](microsoft-edge-relnote-archive-beta-channel.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d9b2a-106">Microsoft Edge Web 平台不斷演進，以改善使用者體驗、安全性和隱私權。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-106">Microsoft Edge Web Platform constantly evolves to improve user experience, security, and privacy.</span></span> <span data-ttu-id="d9b2a-107">若要深入了解，請參閱 [Microsoft Edge 將進行的網站相容性影響變更](/microsoft-edge/web-platform/site-impacting-changes)。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-107">To learn more, see [Site compatibility-impacting changes coming to Microsoft Edge](/microsoft-edge/web-platform/site-impacting-changes).</span></span>

## <a name="version-92090222-june-21"></a><span data-ttu-id="d9b2a-108">版本 92.0.902.22：6 月 21 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-108">Version 92.0.902.22: June 21</span></span>

### <a name="feature-updates"></a><span data-ttu-id="d9b2a-109">功能更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-109">Feature updates</span></span>

- <span data-ttu-id="d9b2a-110">**使用者可以在 Microsoft Edge 上輕鬆進入 Internet Explorer 模式**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-110">**Users can easily get to Internet Explorer mode on Microsoft Edge**.</span></span> <span data-ttu-id="d9b2a-111">從 Microsoft Edge 版本 92 開始，使用者可以在 Microsoft Edge 上重新載入 Internet Explorer 模式的網站，而不需要依賴獨立的 IE 11 應用程式，同時等待在企業模式網站清單中設定網站。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-111">Starting with Microsoft Edge version 92, users can reload a site in Internet Explorer mode on Microsoft Edge instead of relying on the standalone IE 11 application while waiting for a site to be configured in the Enterprise Mode Site List.</span></span> <span data-ttu-id="d9b2a-112">系統會提示使用者將網站新增到其本機網站清單，以便在接下來的 30 天內，瀏覽至 Microsoft Edge 中的相同頁面將會在 IE 模式下自動轉譯。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-112">Users will be prompted to add the site to their local site list such that navigating to the same page in Microsoft Edge will automatically render in IE mode for the next 30 days.</span></span> <span data-ttu-id="d9b2a-113">您可以使用 *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* 原則設定此體驗，並允許存取 IE 模式進入點，而且能夠將網站新增到本機網站清單。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-113">You can use the *[InternetExplorerIntegrationReloadInIEModeAllowed](/deployedge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed)* policy to configure this experience and allow access to the IE mode entry points as well as the ability to add sites to the local site list.</span></span> <span data-ttu-id="d9b2a-114">您可以使用 *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* 原則調整將網站保留在本機網站清單中的天數。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-114">You can use the *[InternetExplorerIntegrationLocalSiteListExpirationDays](/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays)* policy to adjust the number of days to keep sites on the local site list.</span></span>
<span data-ttu-id="d9b2a-115">請注意，Windows 10 版本 1909 需要 KB5003698 或更新版本；Windows 10 版本 2004、Windows 10 版本 20H2 或 Windows 10 版本 21H1 需要 KB5003690 或更新版本，才能提供端對端體驗。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-115">Note that KB5003698 or later is required for Windows 10, version 1909; or KB5003690 or later is required for Windows 10, version 2004, Windows 10, version 20H2, or Windows 10, version 21H1 for the end-to-end experience.</span></span>

- <span data-ttu-id="d9b2a-116">**MHTML 檔案將預設為在 Internet Explorer 模式下開啟**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-116">**MHTML files will default to opening in Internet Explorer mode**.</span></span> <span data-ttu-id="d9b2a-117">從 Microsoft Edge 版本 92 Stable 開始，MHTML 檔案類型將會在 Microsoft Edge (而非 Internet Explorer (IE11) 應用程式) 上自動以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-117">Starting in Microsoft Edge version 92 Stable, MHTML file types will automatically open in Internet Explorer mode on Microsoft Edge instead of the Internet Explorer (IE11) application.</span></span> <span data-ttu-id="d9b2a-118">這是在瀏覽器中嘗試檢視 Outlook 電子郵件時最常觀察到的情況。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-118">This is most commonly observed while trying to view Outlook emails in a browser.</span></span> <span data-ttu-id="d9b2a-119">只有在 IE11 是此檔案類型的預設處理常式時，才能進行此變更。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-119">This change will occur only if IE11 is the default handler for this file type.</span></span> <span data-ttu-id="d9b2a-120">如果您想要變更這項設定，可以在使用[本指南](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)安裝 Stable 92 版更新之前執行此操作。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-120">If you'd prefer to change this, you can do so prior to installing the Stable version 92 update using [this guidance](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

- <span data-ttu-id="d9b2a-121">**付款方式現在會跨裝置同步處理**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-121">**Payment instruments are now synced across devices**.</span></span> <span data-ttu-id="d9b2a-122">從 Microsoft Edge 版本 92 開始，您可以選擇在已登入的裝置上同步處理您的付款資訊。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-122">Beginning with Microsoft Edge version 92, you have the option to synchronize your payment information across your signed in devices.</span></span>
<span data-ttu-id="d9b2a-123">請注意：這是受控功能推出，我們目前為 50%。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-123">Please note: this is a Controlled Feature Rollout and we are currently at 50%.</span></span> <span data-ttu-id="d9b2a-124">如果您看不到此功能，請在我們繼續推出時儘快回來查看。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-124">If you don’t see this feature, please check back shortly as we continue our rollout.</span></span>

- <span data-ttu-id="d9b2a-125">**「停用開發人員模式擴充功能」警告可能會永久關閉**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-125">**"Disable developer mode extensions" warning can be permanently dismissed**.</span></span> <span data-ttu-id="d9b2a-126">從 Microsoft Edge 版本 92 開始，您可以按一下 [不再顯示此訊息] 選項，以關閉警告 [停用開發人員模式擴充功能]。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-126">Beginning with Microsoft Edge version 92, you can turn off the warning "Disable developer mode extensions" by clicking on the 'Don't show this again' option.</span></span>
<span data-ttu-id="d9b2a-127">請注意：這是受控功能推出，我們目前為 25%。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-127">Please note: this is a Controlled Feature Rollout and we are currently at 25%.</span></span> <span data-ttu-id="d9b2a-128">如果您看不到此功能，請在我們繼續推出時儘快回來查看。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-128">If you don’t see this feature, please check back shortly as we continue our rollout.</span></span>

- <span data-ttu-id="d9b2a-129">**從工具列管理擴充功能**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-129">**Manage your extensions right from the toolbar**.</span></span> <span data-ttu-id="d9b2a-130">工具列上全新的擴充功能功能表將讓您輕鬆地隱藏/釘選擴充功能。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-130">The all-new extensions menu on the toolbar will allow you to hide/pin extensions easily.</span></span> <span data-ttu-id="d9b2a-131">管理延伸和尋找新延伸的快速連結將使您輕鬆找到新延伸和管理現有延伸。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-131">The quick links to manage extensions and find new extensions will make it easy for you to find new extensions and manage your existing ones.</span></span>
<span data-ttu-id="d9b2a-132">請注意：這是受控功能推出，我們目前為 25%。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-132">Please note: this is a Controlled Feature Rollout and we are currently at 25%.</span></span> <span data-ttu-id="d9b2a-133">如果您看不到此功能，請在我們繼續推出時儘快回來查看。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-133">If you don’t see this feature, please check back shortly as we continue our rollout.</span></span>

- <span data-ttu-id="d9b2a-134">**自動 HTTPS**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-134">**Automatic HTTPS**.</span></span> <span data-ttu-id="d9b2a-135">使用者可以選擇在可能支援這個更安全的通訊協定的網域上，將瀏覽從 HTTP 升級至 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-135">Users will have the option to upgrade navigation from HTTP to HTTPS on domains likely to support this more secure protocol.</span></span> <span data-ttu-id="d9b2a-136">此支援也可以設定為嘗試針對所有網域，透過 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-136">This support can also be configured to attempt delivery over HTTPS for all domains.</span></span>
<span data-ttu-id="d9b2a-137">請注意：我們正在實驗這項功能，如果您退出宣告實驗，將不會看到此行為。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-137">Please note: we are experimenting with this feature and this behavior won’t be seen if you have opted out of experiments.</span></span>

- <span data-ttu-id="d9b2a-138">**字型呈現的改善**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-138">**Improvements to font rendering**.</span></span> <span data-ttu-id="d9b2a-139">已改善文字的呈現，以提高清晰度並減少模糊度。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-139">Improvements have been made to the rendering of text to improve clarity and reduce blurriness.</span></span>
<span data-ttu-id="d9b2a-140">請注意：這是受控功能推出，我們目前為 25%。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-140">Please note: this is a Controlled Feature Rollout and we are currently at 25%.</span></span> <span data-ttu-id="d9b2a-141">如果您看不到此功能，請在我們繼續推出時儘快回來查看。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-141">If you don’t see this feature, please check back shortly as we continue our rollout.</span></span>

### <a name="policy-updates"></a><span data-ttu-id="d9b2a-142">原則更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-142">Policy updates</span></span>

#### <a name="new-policies"></a><span data-ttu-id="d9b2a-143">新原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-143">New policies</span></span>

<span data-ttu-id="d9b2a-144">已新增八個新原則。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-144">Eight new policies were added.</span></span> <span data-ttu-id="d9b2a-145">從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-145">Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download).</span></span> <span data-ttu-id="d9b2a-146">已新增下列新原則：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-146">The following new policies were added:</span></span>

- <span data-ttu-id="d9b2a-147">[AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) 已啟用使用此設定檔單一登入公司或學校網站。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-147">[AADWebSiteSSOUsingThisProfileEnabled](/DeployEdge/microsoft-edge-policies#aadwebsitessousingthisprofileenabled) Single sign-on for work or school sites using this profile enabled.</span></span>
- <span data-ttu-id="d9b2a-148">[AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) 設定自動 HTTPS</span><span class="sxs-lookup"><span data-stu-id="d9b2a-148">[AutomaticHttpsDefault](/DeployEdge/microsoft-edge-policies#automatichttpsdefault) Configure Automatic HTTPS</span></span>
- <span data-ttu-id="d9b2a-149">[HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) 控制無周邊模式的使用</span><span class="sxs-lookup"><span data-stu-id="d9b2a-149">[HeadlessModeEnabled](/DeployEdge/microsoft-edge-policies#headlessmodeenabled) Control use of the Headless Mode</span></span>
- <span data-ttu-id="d9b2a-150">[InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed) 指定是否要允許不安全的網站向較私人的網路端點提出要求</span><span class="sxs-lookup"><span data-stu-id="d9b2a-150">[InsecurePrivateNetworkRequestsAllowed](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed)Specifies whether to allow insecure websites to make requests to more-private network endpoints</span></span>
- <span data-ttu-id="d9b2a-151">[InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) 允許列出的網站從不安全的內容對較私人的網路端點提出要求</span><span class="sxs-lookup"><span data-stu-id="d9b2a-151">[InsecurePrivateNetworkRequestsAllowedForUrls](/DeployEdge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls) Allow the listed sites to make requests to more-private network endpoints from insecure contexts</span></span>
- <span data-ttu-id="d9b2a-152">[InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) 指定網站保留在本機 IE 模式網站清單上的天數</span><span class="sxs-lookup"><span data-stu-id="d9b2a-152">[InternetExplorerIntegrationLocalSiteListExpirationDays](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalsitelistexpirationdays) Specify the number of days that a site remains on the local IE mode site list</span></span>
- <span data-ttu-id="d9b2a-153">[InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) 允許未設定的網站在 Internet Explorer 模式下重新載入</span><span class="sxs-lookup"><span data-stu-id="d9b2a-153">[InternetExplorerIntegrationReloadInIEModeAllowed](/DeployEdge/microsoft-edge-policies#internetexplorerintegrationreloadiniemodeallowed) Allow unconfigured sites to be reloaded in Internet Explorer mode</span></span>
- <span data-ttu-id="d9b2a-154">[SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) 指定 SharedArrayBuffers 是否可以在非跨來源隔離內容中使用</span><span class="sxs-lookup"><span data-stu-id="d9b2a-154">[SharedArrayBufferUnrestrictedAccessAllowed](/DeployEdge/microsoft-edge-policies#sharedarraybufferunrestrictedaccessallowed) Specifies whether SharedArrayBuffers can be used in a non cross-origin-isolated context</span></span>

#### <a name="obsoleted-policy"></a><span data-ttu-id="d9b2a-155">淘汰的原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-155">Obsoleted Policy</span></span>

- <span data-ttu-id="d9b2a-156">[EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) 允許本機信賴起點核發時使用 SHA-1 簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-156">[EnableSha1ForLocalAnchors](/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors) Allow certificates signed using SHA-1 when issued by local trust anchors.</span></span>


## <a name="version-9209029-june-8"></a><span data-ttu-id="d9b2a-157">版本 92.0.902.9：6 月 8 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-157">Version 92.0.902.9: June 8</span></span>

<span data-ttu-id="d9b2a-158">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-158">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086441-june-3"></a><span data-ttu-id="d9b2a-159">版本 91.0.864.41：6 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-159">Version 91.0.864.41: June 3</span></span>

<span data-ttu-id="d9b2a-160">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-160">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086437-may-27"></a><span data-ttu-id="d9b2a-161">版本 91.0.864.37：5 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-161">Version 91.0.864.37: May 27</span></span>

<span data-ttu-id="d9b2a-162">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-162">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086436-may-26"></a><span data-ttu-id="d9b2a-163">版本 91.0.864.36：5 月 26 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-163">Version 91.0.864.36: May 26</span></span>

<span data-ttu-id="d9b2a-164">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-164">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086433-may-21"></a><span data-ttu-id="d9b2a-165">版本 91.0.864.33：5 月 21 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-165">Version 91.0.864.33: May 21</span></span>

<span data-ttu-id="d9b2a-166">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-166">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086427-may-14"></a><span data-ttu-id="d9b2a-167">版本 91.0.864.27：5 月 14 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-167">Version 91.0.864.27: May 14</span></span>

<span data-ttu-id="d9b2a-168">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-168">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086419-may-7"></a><span data-ttu-id="d9b2a-169">版本 91.0.864.19：5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-169">Version 91.0.864.19: May 7</span></span>

<span data-ttu-id="d9b2a-170">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-170">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086415-may-3"></a><span data-ttu-id="d9b2a-171">版本 91.0.864.15：5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-171">Version 91.0.864.15: May 3</span></span>

<span data-ttu-id="d9b2a-172">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-172">Fixed various bugs and performance issues.</span></span>

## <a name="version-91086411-april-30"></a><span data-ttu-id="d9b2a-173">版本 91.0.864.11：4 月 30 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-173">Version 91.0.864.11: April 30</span></span>

### <a name="feature-updates"></a><span data-ttu-id="d9b2a-174">功能更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-174">Feature updates</span></span>

- <span data-ttu-id="d9b2a-175">**在 Proxy 層級識別來自 Microsoft Defender 應用程式防護容器的流量**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-175">**Identify network traffic originating from Microsoft Defender Application Guard containers at the proxy level**.</span></span> <span data-ttu-id="d9b2a-176">從 Microsoft Edge 版本 91 開始，內建支援以標記來自應用程式防護容器的流量，讓企業能夠識別它們並套用特定原則。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-176">Starting with Microsoft Edge version 91, there’s built in support to tag network traffic originating from Application Guard containers, allowing enterprises to identify them and apply specific policies.</span></span>

- <span data-ttu-id="d9b2a-177">**支援選項，讓 [我的最愛] 從主機同步處理至 Edge 應用程式防護容器**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-177">**Support option to allow synchronizing Favorites from the host to the Edge Application Guard container**.</span></span> <span data-ttu-id="d9b2a-178">從 Microsoft Edge 版本 91 開始，使用者可以選擇設定應用程式防護，將其 [我的最愛] 從主機同步處理至容器。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-178">Starting with Microsoft Edge version 91, users have the option to configure Application Guard to synchronize their favorites from the host to the container.</span></span> <span data-ttu-id="d9b2a-179">這可確保容器上也會出現新的 [我的最愛]。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-179">This ensures new favorites appear on the container as well.</span></span>

- <span data-ttu-id="d9b2a-180">**支援語音辨識 API**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-180">**Support for Speech Recognition APIs**.</span></span> <span data-ttu-id="d9b2a-181">從 Microsoft Edge 版本 91 開始，將會新增對 Google.com 和類似網站的語音辨識命令 API 支援。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-181">Starting with Microsoft Edge version 91, API support for speech recognition commands on Google.com and similar sites will be added.</span></span> <span data-ttu-id="d9b2a-182">此功能僅限於已啟用試驗的隨機選取使用者群組。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-182">This feature is limited to a randomly selected group of users who have enabled experimentation.</span></span> <span data-ttu-id="d9b2a-183">這些使用者會向功能小組提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-183">These users are giving feedback to the feature team.</span></span>

- <span data-ttu-id="d9b2a-184">**使用新的佈景主題色彩以個人化您的瀏覽器**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-184">**Personalize your browser with new theme colors**.</span></span> <span data-ttu-id="d9b2a-185">使用設定 -> 外觀頁面上的十四種新佈景主題色彩的其中一種，將 Microsoft Edge 個人化。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-185">Make Microsoft Edge your own with one of the fourteen new theme colors on the Settings -> Appearance page.</span></span> <span data-ttu-id="d9b2a-186">您也可以從 Microsoft Edge 附加元件網站安裝自訂佈景主題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-186">You can also install custom themes from the Microsoft Edge Add-on site.</span></span> [<span data-ttu-id="d9b2a-187">深入了解</span><span class="sxs-lookup"><span data-stu-id="d9b2a-187">Learn more</span></span>](https://techcommunity.microsoft.com/t5/articles/make-microsoft-edge-your-own-with-themes/m-p/2083165)

- <span data-ttu-id="d9b2a-188">**中斷下載** 從 Microsoft Edge 版本 91 開始，瀏覽器會自動中斷類型下載，這些下載若在未經使用者互動的情況下啟動，且不受 SmartScreen 應用程式信譽檢查支援，這些下載可能會危害您的電腦。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-188">**Interrupt Downloads** Starting with Microsoft Edge version 91 the browser will automatically interrupt downloads of types which could harm your computer if those downloads are started without a user interaction and are not supported by SmartScreen Application Reputation check.</span></span> <span data-ttu-id="d9b2a-189">使用者可以在下載項目上按一下滑鼠右鍵並選擇「保留」，以覆寫並繼續下載。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-189">Users may override and continue to download by right clicking and choosing “Keep” on the download item.</span></span>
<span data-ttu-id="d9b2a-190">企業系統管理員可以退出宣告此行為的這兩個原則之一：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-190">Enterprise administrators may opt out of this behavior one of these two policies:</span></span>
    - <span data-ttu-id="d9b2a-191">[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - 針對網域中的指定檔案類型，停用下載檔案類型副檔名警告。如需詳細資訊，請參閱 [Microsoft Edge 安全性下載中斷](/deployedge/microsoft-edge-security-downloads-interruptions)</span><span class="sxs-lookup"><span data-stu-id="d9b2a-191">[ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) - Disable download file type extension-based warnings for specified file types on domains For more information, see [Microsoft Edge Security downloads interruptions](/deployedge/microsoft-edge-security-downloads-interruptions)</span></span>

### <a name="policy-updates"></a><span data-ttu-id="d9b2a-192">原則更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-192">Policy updates</span></span>

#### <a name="new-policies"></a><span data-ttu-id="d9b2a-193">新原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-193">New policies</span></span>

<span data-ttu-id="d9b2a-194">已新增六個新原則。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-194">Six new policies were added.</span></span> <span data-ttu-id="d9b2a-195">從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-195">Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download).</span></span> <span data-ttu-id="d9b2a-196">已新增下列新原則：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-196">The following new policies were added:</span></span>

- <span data-ttu-id="d9b2a-197">[ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) -　應用程式防護流量識別</span><span class="sxs-lookup"><span data-stu-id="d9b2a-197">[ApplicationGuardTrafficIdentificationEnabled](/DeployEdge/microsoft-edge-policies#applicationguardtrafficidentificationenabled) - Application Guard Traffic Identification</span></span>
- <span data-ttu-id="d9b2a-198">[ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - 明確允許的網路連接埠</span><span class="sxs-lookup"><span data-stu-id="d9b2a-198">[ExplicitlyAllowedNetworkPorts](/DeployEdge/microsoft-edge-policies#explicitlyallowednetworkports) - Explicitly allowed network ports</span></span>
- <span data-ttu-id="d9b2a-199">[ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - 允許匯出啟動頁面設定</span><span class="sxs-lookup"><span data-stu-id="d9b2a-199">[ImportStartupPageSettings](/DeployEdge/microsoft-edge-policies#importstartuppagesettings) - Allow importing of startup page settings</span></span>
- <span data-ttu-id="d9b2a-200">[MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - 讓使用者在 Microsoft Edge 中以逐步解說來刪除數學問題並取得解決方案</span><span class="sxs-lookup"><span data-stu-id="d9b2a-200">[MathSolverEnabled](/DeployEdge/microsoft-edge-policies#mathsolverenabled) - Let users snip a Math problem and get the solution with a step-by-step explanation in Microsoft Edge</span></span>
- <span data-ttu-id="d9b2a-201">[NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - 允許新分頁頁面上的 Microsoft 新聞內容</span><span class="sxs-lookup"><span data-stu-id="d9b2a-201">[NewTabPageContentEnabled](/DeployEdge/microsoft-edge-policies#newtabpagecontentenabled) - Allow Microsoft News content on the new tab page</span></span>
- <span data-ttu-id="d9b2a-202">[NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - 允許新分頁頁面上的快速連結</span><span class="sxs-lookup"><span data-stu-id="d9b2a-202">[NewTabPageQuickLinksEnabled](/DeployEdge/microsoft-edge-policies#newtabpagequicklinksenabled) - Allow quick links on the new tab page</span></span>

#### <a name="obsoleted-policy"></a><span data-ttu-id="d9b2a-203">淘汰的原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-203">Obsoleted Policy</span></span>

- <span data-ttu-id="d9b2a-204">[ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - 啟用主動式驗證</span><span class="sxs-lookup"><span data-stu-id="d9b2a-204">[ProactiveAuthEnabled](./microsoft-edge-policies.md#proactiveauthenabled) - Enable Proactive Authentication</span></span>
<!-- end major 91 -->

## <a name="version-90081846-april-22"></a><span data-ttu-id="d9b2a-205">版本 90.0.818.46：4 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-205">Version 90.0.818.46: April 22</span></span>

<span data-ttu-id="d9b2a-206">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-206">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081842-april-20"></a><span data-ttu-id="d9b2a-207">版本 90.0.818.42：4 月 20 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-207">Version 90.0.818.42: April 20</span></span>

<span data-ttu-id="d9b2a-208">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-208">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081841-april-16"></a><span data-ttu-id="d9b2a-209">版本 90.0.818.41：4 月 16 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-209">Version 90.0.818.41: April 16</span></span>

<span data-ttu-id="d9b2a-210">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-210">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081838-april-14"></a><span data-ttu-id="d9b2a-211">版本 90.0.818.38：4 月 14 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-211">Version 90.0.818.38: April 14</span></span>

<span data-ttu-id="d9b2a-212">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-212">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081836-april-12"></a><span data-ttu-id="d9b2a-213">版本 90.0.818.36：4 月 12 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-213">Version 90.0.818.36: April 12</span></span>

<span data-ttu-id="d9b2a-214">已修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-214">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081827-april-2"></a><span data-ttu-id="d9b2a-215">版本 90.0.818.27：4 月 2 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-215">Version 90.0.818.27: April 2</span></span>

<span data-ttu-id="d9b2a-216">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-216">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081822-march-29"></a><span data-ttu-id="d9b2a-217">版本 90.0.818.22：3 月 29 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-217">Version 90.0.818.22: March 29</span></span>

<span data-ttu-id="d9b2a-218">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-218">Fixed various bugs and performance issues.</span></span>

## <a name="version-90081814-march-22"></a><span data-ttu-id="d9b2a-219">版本 90.0.818.14：3 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-219">Version 90.0.818.14: March 22</span></span>

<span data-ttu-id="d9b2a-220">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-220">Fixed various bugs and performance issues.</span></span>
<!-- begin major 90 -->
## <a name="version-9008188-march-16"></a><span data-ttu-id="d9b2a-221">版本 90.0.818.8：3 月 16 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-221">Version 90.0.818.8: March 16</span></span>

### <a name="feature-updates"></a><span data-ttu-id="d9b2a-222">功能更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-222">Feature updates</span></span>

- <span data-ttu-id="d9b2a-223">**單一登入 (SSO) 目前可供 macOS 上的 Azure Active Directory (Azure AD) 帳戶和 Microsoft 帳戶 (MSA) 使用**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-223">**Single Sign On (SSO) is now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS**.</span></span> <span data-ttu-id="d9b2a-224">在 macOS 上，在 Microsoft Edge 上登入的使用者現在會自動進入網站，這些網站已設定為允許使用 Work 和 Microsoft 帳戶 (例如 bing.com、office.com、msn.com 和 outlook.com) 進行單一登入。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-224">A user signed in on Microsoft Edge on macOS will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (for example, bing.com, office.com, msn.com, and outlook.com).</span></span>

- **<span data-ttu-id="d9b2a-225">Kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-225">Kiosk mode.</span></span>** <span data-ttu-id="d9b2a-226">從 Microsoft Edge 版本 90 開始，我們已鎖定 UI 列印設定，只允許已設定印表機和「列印至 PDF」選項。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-226">Starting with Microsoft Edge version 90, we have locked down the UI print settings to only allow the configured printers and “Print to PDF” options.</span></span> <span data-ttu-id="d9b2a-227">我們也在受指派的存取權單一應用程式 kiosk 模式中進行了改善，以限制從瀏覽器啟動其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-227">We have also done improvements within the assigned access single app kiosk mode to restrict the launch of other applications from the browser.</span></span> <span data-ttu-id="d9b2a-228">如需有關 Kiosk 模式功能的詳細資訊，請移至[這裡](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features)。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-228">For more information about the kiosk mode features please go [here](/deployedge/microsoft-edge-configure-kiosk-mode#kiosk-mode-supported-features).</span></span>

- **<span data-ttu-id="d9b2a-229">列印：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-229">Printing:</span></span>**

  - <span data-ttu-id="d9b2a-230">**非 PostScript 印表機的新列印點陣化模式**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-230">**New print rasterization mode for non-PostScript printers**.</span></span> <span data-ttu-id="d9b2a-231">從 Microsoft Edge 版本 90 開始，系統管理員可以使用新原則來定義其使用者的列印點陣化模式。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-231">Starting with Microsoft Edge version 90, Admins can use a new policy to define print rasterization mode for their users.</span></span> <span data-ttu-id="d9b2a-232">此原則可控制 Microsoft Edge 列印至 Windows 上非 PostScript 印表機的方式。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-232">This policy  controls how Microsoft Edge prints to non-PostScript printers on Windows.</span></span>  <span data-ttu-id="d9b2a-233">有時需將非 PostScript 印表機上的列印工作點陣化才能正確列印。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-233">Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly.</span></span> <span data-ttu-id="d9b2a-234">列印選項為「完整」和「快速」。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-234">The print options are Full and Fast.</span></span>

  - <span data-ttu-id="d9b2a-235">**用於列印的其他頁面縮放選項**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-235">**Additional page scaling options for printing**.</span></span> <span data-ttu-id="d9b2a-236">使用者現在能夠自訂縮放比例，同時使用其他選項列印網頁和 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-236">Users are now able to customize scaling while printing webpages and PDF documents using additional options.</span></span> <span data-ttu-id="d9b2a-237">「符合頁面大小」選項可確保網頁或文件符合所選「紙張大小」可供列印的空間。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-237">The "Fit to Page" option ensures that the webpage or document is fit into the space available in the selected "Paper size" for printing.</span></span> <span data-ttu-id="d9b2a-238">[實際大小] 選項可確保無論選取的 [紙張大小] 為何，列印內容的大小都不會變更。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-238">The "Actual size" option ensures that there are no changes in the size of the contents being printed regardless of the selected "Paper size".</span></span>

- **<span data-ttu-id="d9b2a-239">生產力：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-239">Productivity:</span></span>**

  - <span data-ttu-id="d9b2a-240">**延伸自動填寫建議，以包含來自剪貼簿的地址欄位內容**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-240">**Autofill suggestions are extended to include address fields content from clipboard**.</span></span> <span data-ttu-id="d9b2a-241">當您按一下設定檔/地址欄位 (例如，電話、電子郵件、郵遞區號、縣/市、省/市等) 以顯示為自動填寫建議時，系統將會剖析剪貼簿內容。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-241">Clipboard content is parsed when you click on a profile/address field (for example, phone, email, zip code, city, state, etc.) to show as autofill suggestions.</span></span>

  - <span data-ttu-id="d9b2a-242">**即使未偵測到表單或欄位，使用者也可以搜尋自動填寫建議**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-242">**Users can search for autofill suggestions even if a form or field isn’t detected**.</span></span> <span data-ttu-id="d9b2a-243">現在，如果您將您的資訊儲存在 Microsoft Edge 上，自動填寫建議將自動彈出，並幫助您在填寫表單時節省時間。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-243">Today if you have your information saved on Microsoft Edge, autofill suggestions pop up automatically and help you save time while filling out forms.</span></span> <span data-ttu-id="d9b2a-244">如果自動填寫遺漏表單，或您想要在通常沒有自動填寫功能的表單 (例如暫存表單) 中擷取資料，可以搜尋您使用自動填寫的資訊。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-244">In cases where autofill misses a form, or if you want to fetch data in forms that don't typically have autofill (like temporary forms), you can search for your information using autofill.</span></span>

- <span data-ttu-id="d9b2a-245">**從功能表列的飛出視窗存取下載**。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-245">**Access downloads from a flyout in the menu bar**.</span></span> <span data-ttu-id="d9b2a-246">下載會顯示在右上角，將所有作用中下載顯示在同一個位置。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-246">Downloads will appear in the top-right corner with all the active downloads in one place.</span></span> <span data-ttu-id="d9b2a-247">此功能表可以很輕易關閉，因此使用者可以繼續瀏覽而不受干擾，且他們可以直接從工具列監視整體下載進度。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-247">This menu is easily dismissible so users can continue browsing uninterrupted, and they can monitor overall download progress right from the toolbar.</span></span> <span data-ttu-id="d9b2a-248">[進一步了解](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551)。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-248">[Learn more](https://techcommunity.microsoft.com/t5/articles/introducing-the-new-downloads-experience/m-p/2111551).</span></span>


### <a name="policy-updates"></a><span data-ttu-id="d9b2a-249">原則更新</span><span class="sxs-lookup"><span data-stu-id="d9b2a-249">Policy updates</span></span>

#### <a name="new-policies"></a><span data-ttu-id="d9b2a-250">新原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-250">New policies</span></span>

<span data-ttu-id="d9b2a-251">新增了 7 個原則。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-251">Seven new policies were added.</span></span> <span data-ttu-id="d9b2a-252">從 [Microsoft Edge 企業版登陸頁面](https://www.microsoft.com/edge/business/download)下載更新的系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-252">Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download).</span></span> <span data-ttu-id="d9b2a-253">已新增下列新原則：</span><span class="sxs-lookup"><span data-stu-id="d9b2a-253">The following new policies were added:</span></span>

- <span data-ttu-id="d9b2a-254">[ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - 已啟用應用程式防護我的最愛同步處理</span><span class="sxs-lookup"><span data-stu-id="d9b2a-254">[ApplicationGuardFavoritesSyncEnabled](./microsoft-edge-policies.md#applicationguardfavoritessyncenabled) - Application Guard Favorites Sync Enabled</span></span>
- <span data-ttu-id="d9b2a-255">[ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - 設定網站到特定來源的受管理設定值</span><span class="sxs-lookup"><span data-stu-id="d9b2a-255">[ManagedConfigurationPerOrigin](./microsoft-edge-policies.md#managedconfigurationperorigin) - Sets managed configuration values for websites to specific origins</span></span>
- <span data-ttu-id="d9b2a-256">[PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - 列印點陣化模式</span><span class="sxs-lookup"><span data-stu-id="d9b2a-256">[PrintRasterizationMode](./microsoft-edge-policies.md#printrasterizationmode) - Print Rasterization Mode</span></span>
- <span data-ttu-id="d9b2a-257">[QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - 管理 Microsoft Edge 中的 QuickView Office 檔案功能</span><span class="sxs-lookup"><span data-stu-id="d9b2a-257">[QuickViewOfficeFilesEnabled](./microsoft-edge-policies.md#quickviewofficefilesenabled) - Manage QuickView Office files capability in Microsoft Edge</span></span>
- <span data-ttu-id="d9b2a-258">[SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - 允許使用者從特定來源的 HTTPS 警告頁面繼續進行</span><span class="sxs-lookup"><span data-stu-id="d9b2a-258">[SSLErrorOverrideAllowedForOrigins](./microsoft-edge-policies.md#sslerroroverrideallowedfororigins) - Allow users to proceed from the HTTPS warning page for specific origins</span></span>
- <span data-ttu-id="d9b2a-259">[WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - 啟用視窗遮蔽</span><span class="sxs-lookup"><span data-stu-id="d9b2a-259">[WindowOcclusionEnabled](./microsoft-edge-policies.md#windowocclusionenabled) - Enable Window Occlusion</span></span>
- <span data-ttu-id="d9b2a-260">[WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - 已啟用適用於 HTTP 驗證的 Windows Hello</span><span class="sxs-lookup"><span data-stu-id="d9b2a-260">[WindowsHelloForHTTPAuthEnabled](./microsoft-edge-policies.md#windowshelloforhttpauthenabled) - Windows Hello For HTTP Auth Enabled</span></span>

#### <a name="deprecated-policies"></a><span data-ttu-id="d9b2a-261">取代的原則</span><span class="sxs-lookup"><span data-stu-id="d9b2a-261">Deprecated policies</span></span>

- <span data-ttu-id="d9b2a-262">[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - 啟用原生視窗遮蔽</span><span class="sxs-lookup"><span data-stu-id="d9b2a-262">[NativeWindowOcclusionEnabled](./microsoft-edge-policies.md#nativewindowocclusionenabled) - Enable Native Window Occlusion</span></span>
- <span data-ttu-id="d9b2a-263">[SSLVersionMin](./microsoft-edge-policies.md#sslversionmin) - 已啟用最低 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="d9b2a-263">[SSLVersionMin](./microsoft-edge-policies.md#sslversionmin)- Minimum TLS version enabled</span></span>
<!-- end major 90 -->

## <a name="version-89077454-march-13"></a><span data-ttu-id="d9b2a-264">版本 89.0.774.54：3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-264">Version 89.0.774.54: March 13</span></span>

<span data-ttu-id="d9b2a-265">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-265">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077450-march-10"></a><span data-ttu-id="d9b2a-266">版本 89.0.774.50：3 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-266">Version 89.0.774.50: March 10</span></span>

<span data-ttu-id="d9b2a-267">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-267">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077448-march-8"></a><span data-ttu-id="d9b2a-268">版本 89.0.774.48：3 月 8 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-268">Version 89.0.774.48: March 8</span></span>

<span data-ttu-id="d9b2a-269">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-269">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077445-march-3"></a><span data-ttu-id="d9b2a-270">版本 89.0.774.45：3 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-270">Version 89.0.774.45: March 3</span></span>

<span data-ttu-id="d9b2a-271">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-271">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077439-february-26"></a><span data-ttu-id="d9b2a-272">版本 89.0.774.39：2 月 26 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-272">Version 89.0.774.39: February 26</span></span>

<span data-ttu-id="d9b2a-273">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-273">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077434-february-22"></a><span data-ttu-id="d9b2a-274">版本 89.0.774.34：2 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-274">Version 89.0.774.34: February 22</span></span>

<span data-ttu-id="d9b2a-275">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-275">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077427-february-12"></a><span data-ttu-id="d9b2a-276">版本 89.0.774.27：2 月 12 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-276">Version 89.0.774.27: February 12</span></span>

<span data-ttu-id="d9b2a-277">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-277">Fixed various bugs and performance issues.</span></span>

## <a name="version-89077423-february-8"></a><span data-ttu-id="d9b2a-278">版本 89.0.774.23：2 月 8 日</span><span class="sxs-lookup"><span data-stu-id="d9b2a-278">Version 89.0.774.23: February 8</span></span>

<span data-ttu-id="d9b2a-279">修正各種錯誤和效能問題。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-279">Fixed various bugs and performance issues.</span></span>

<!-- begin major 89 -->

<!--- Archived from Version 87.0.664.18: October 26 to to version 89.0.774.18: February 3 ---->
<!--- Archived from Version 87.0.664.12: October 20 to to version 86.0.622.15: September 14 ---->
<!--- Archived to version 86.0.622.11: September 9 ---->
<!--- Archived to version 85.0.564.18: July 28 ---->

## <a name="see-also"></a><span data-ttu-id="d9b2a-280">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9b2a-280">See also</span></span>

- [<span data-ttu-id="d9b2a-281">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="d9b2a-281">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
