---
title: IE 模式常見問題集
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 適用於 IE 模式 Microsoft Edge 的常見問題集和疑難排解
ms.openlocfilehash: f5279caddb5d3dfabaf04be6bd927f7095be1fc9
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447727"
---
# <a name="ie-mode-faq"></a><span data-ttu-id="87c54-103">IE 模式常見問題集</span><span class="sxs-lookup"><span data-stu-id="87c54-103">IE mode FAQ</span></span>

<span data-ttu-id="87c54-104">本文提供 Microsoft Edge 版本 77 或更新版本的疑難排解秘訣和常見問題集。</span><span class="sxs-lookup"><span data-stu-id="87c54-104">This article provides troubleshooting tips and an FAQ for Microsoft Edge version 77 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="87c54-105">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="87c54-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>


## <a name="troubleshoot-ie-mode"></a><span data-ttu-id="87c54-106">疑難排解 IE 模式</span><span class="sxs-lookup"><span data-stu-id="87c54-106">Troubleshoot IE mode</span></span>

<span data-ttu-id="87c54-107">使用本節中的資訊來診斷和修復 IE 模式問題。</span><span class="sxs-lookup"><span data-stu-id="87c54-107">Use the information in this section to diagnose and fix IE mode problems.</span></span>

### <a name="internet-explorer-mode-diagnostic-information"></a><span data-ttu-id="87c54-108">Internet Explorer 模式診斷資訊</span><span class="sxs-lookup"><span data-stu-id="87c54-108">Internet Explorer mode diagnostic information</span></span>

<span data-ttu-id="87c54-109">您可以在 Microsoft Edge 相容性索引標籤上取得 Internet Explorer 模式診斷資訊。若要開啟此索引標籤，請移至 *edge://compat/iediagnostic*。</span><span class="sxs-lookup"><span data-stu-id="87c54-109">You can get Internet Explorer mode diagnostic information on the Microsoft Edge Compatibility tab. To open this tab, go to *edge://compat/iediagnostic*.</span></span> <span data-ttu-id="87c54-110">此頁面可能會顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="87c54-110">This page may show diagnostic messages.</span></span> <span data-ttu-id="87c54-111">本頁也提供下列類別的設定資訊：</span><span class="sxs-lookup"><span data-stu-id="87c54-111">This page also provides configuration information for the following categories:</span></span>

- <span data-ttu-id="87c54-112">**登錄機碼檢查**。</span><span class="sxs-lookup"><span data-stu-id="87c54-112">**Registry key check**.</span></span> <span data-ttu-id="87c54-113">(只有檢查失敗時才會顯示。) 檢查登錄中是否正確設定了 Internet Explorer 整合。</span><span class="sxs-lookup"><span data-stu-id="87c54-113">(Displayed only if the check fails.) Checks to see if Internet Explorer integration is set up correctly in the registry.</span></span> <span data-ttu-id="87c54-114">如果未正確設定，使用者可以按一下**修正**來解決問題。</span><span class="sxs-lookup"><span data-stu-id="87c54-114">If not, the user can click **Fix it** to resolve the problem.</span></span>
- <span data-ttu-id="87c54-115">**Internet Explorer 模式**。</span><span class="sxs-lookup"><span data-stu-id="87c54-115">**Internet Explorer mode**.</span></span> <span data-ttu-id="87c54-116">顯示所使用的 API 版本，該版本基於設定和作業系統。</span><span class="sxs-lookup"><span data-stu-id="87c54-116">Shows the API version that's used, based on the configuration and OS.</span></span> <span data-ttu-id="87c54-117">如果發生問題，可能會提示使用者安裝 **Windows Update**。</span><span class="sxs-lookup"><span data-stu-id="87c54-117">If there's a problem, the user may be prompted to install a **Windows Update**.</span></span>
- <span data-ttu-id="87c54-118">**Internet Explorer 模式**。</span><span class="sxs-lookup"><span data-stu-id="87c54-118">**Internet Explorer mode setting**.</span></span> <span data-ttu-id="87c54-119">顯示是否已啟用 Internet Explorer 模式，以及其設定方式。</span><span class="sxs-lookup"><span data-stu-id="87c54-119">Shows whether Internet Explorer mode is enabled, and how it's configured.</span></span>
- <span data-ttu-id="87c54-120">**命令列**。</span><span class="sxs-lookup"><span data-stu-id="87c54-120">**Command line**.</span></span> <span data-ttu-id="87c54-121">顯示用於啟動 Microsoft Edge 的命令列字串和參數。</span><span class="sxs-lookup"><span data-stu-id="87c54-121">Shows the command line string and switches used to start Microsoft Edge.</span></span>
- <span data-ttu-id="87c54-122">**群組原則設定**。</span><span class="sxs-lookup"><span data-stu-id="87c54-122">**Group policy settings**.</span></span> <span data-ttu-id="87c54-123">顯示是否使用群組原則設定 IE 模式，以及所套用的原則。</span><span class="sxs-lookup"><span data-stu-id="87c54-123">Shows whether IE mode is configured using group policies, and the policies that are applied.</span></span>

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a><span data-ttu-id="87c54-124">錯誤訊息：「若要在 Internet Explorer 模式中開啟此頁面，請以系統管理員權限重新安裝 Microsoft Edge。」</span><span class="sxs-lookup"><span data-stu-id="87c54-124">Error message: "To open this page in Internet Explorer mode, reinstall Microsoft Edge with administrator privileges."</span></span>

<span data-ttu-id="87c54-125">如果您沒有所有必要的 Windows Update，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="87c54-125">You may see this error if you don't have all required Windows Updates.</span></span> <span data-ttu-id="87c54-126">請參閱所需 Windows 和 Microsoft Edge 版本[關於 IE 模式](./edge-ie-mode.md)中所列的必要條件。</span><span class="sxs-lookup"><span data-stu-id="87c54-126">See the prerequisites listed in [About IE mode](./edge-ie-mode.md) for the required versions of Windows and Microsoft Edge.</span></span>

<span data-ttu-id="87c54-127">如果您已安裝所有必要的 Windows Update，您可能會在下列情況下看到此錯誤：</span><span class="sxs-lookup"><span data-stu-id="87c54-127">If you've already installed all required Windows Updates, you may see this error if:</span></span>

- <span data-ttu-id="87c54-128">您使用的是 Canary 通道，預設是在使用者層級安裝。</span><span class="sxs-lookup"><span data-stu-id="87c54-128">You're using the Canary channel, which is installed at the user level by default.</span></span>
- <span data-ttu-id="87c54-129">您使用的是 Stable、Beta 或 Dev 通道，提示提高權限時，安裝提高權限已取消。</span><span class="sxs-lookup"><span data-stu-id="87c54-129">You're using the Stable, Beta, or Dev channel, but when prompted for elevation when installing the elevation was canceled.</span></span> <span data-ttu-id="87c54-130">當您取消提高權限提示時，系統會在使用者層級繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="87c54-130">When you cancel the elevation prompt, the installation will continue at the user level.</span></span>
- <span data-ttu-id="87c54-131">Internet Explorer 11 已在 Windows 功能中停用。</span><span class="sxs-lookup"><span data-stu-id="87c54-131">Internet Explorer 11 has been disabled in Windows Features.</span></span>

<span data-ttu-id="87c54-132">可能的解決方式：</span><span class="sxs-lookup"><span data-stu-id="87c54-132">Possible solutions:</span></span>

- <span data-ttu-id="87c54-133">在系統層級執行任何通道的安裝程式：`installer.exe --system-level`。</span><span class="sxs-lookup"><span data-stu-id="87c54-133">Run the installer for any channel at the system level: `installer.exe --system-level`.</span></span>
- <span data-ttu-id="87c54-134">在 Windows 功能中啟用 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="87c54-134">Enable Internet Explorer 11 in Windows Features.</span></span>

<span data-ttu-id="87c54-135">若要檢查 Microsoft Edge 是否安裝在系統層級，請在 Microsoft Edge 網址列中鍵入 "edge://version"。</span><span class="sxs-lookup"><span data-stu-id="87c54-135">To check if Microsoft Edge is installed at the systems level, type "edge://version" in the Microsoft Edge address bar.</span></span> <span data-ttu-id="87c54-136">可執行檔路徑將顯示開頭為 *C:\Program Files* 的路徑，表示是系統安裝。</span><span class="sxs-lookup"><span data-stu-id="87c54-136">The Executable path will show a path starting with *C:\Program Files*, which indicates a system install.</span></span> <span data-ttu-id="87c54-137">如果可執行檔路徑開頭為 \*C:\Users\*，請解除安裝然後以系統管理員權限重新安裝 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="87c54-137">If the Executable path begins with \*C:\Users\*, uninstall and then reinstall Microsoft Edge with administrator privileges.</span></span>

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a><span data-ttu-id="87c54-138">錯誤訊息：「若要在 IE 模式中開啟此頁面，請嘗試重新啟動 Microsoft Edge。」</span><span class="sxs-lookup"><span data-stu-id="87c54-138">Error message: "To open this page in IE mode, try restarting Microsoft Edge."</span></span>

<span data-ttu-id="87c54-139">如果 Internet Explorer 發生未預期的錯誤，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="87c54-139">You may see this error if there was an unexpected error in Internet Explorer.</span></span> <span data-ttu-id="87c54-140">重新啟動 Microsoft Edge 通常可以修正此錯誤。</span><span class="sxs-lookup"><span data-stu-id="87c54-140">Restarting Microsoft Edge usually fixes this error.</span></span>

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a><span data-ttu-id="87c54-141">錯誤訊息：「請關閉遠端偵錯以在 IE 模式下開啟此網站，否則可能無法如預期運作。」</span><span class="sxs-lookup"><span data-stu-id="87c54-141">Error message: "Turn off remote debugging to open this site in IE mode otherwise it might not work as expected."</span></span>

<span data-ttu-id="87c54-142">如果您正在遠端偵錯，且瀏覽至設定為在 IE 模式中執行的網頁，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="87c54-142">You may see this error if you're remote debugging and navigate to a web page configured to run in IE mode.</span></span> <span data-ttu-id="87c54-143">您可以繼續，但是頁面將會使用 Microsoft Edge 轉譯。</span><span class="sxs-lookup"><span data-stu-id="87c54-143">You can continue, but the page will be rendered using Microsoft Edge.</span></span>

### <a name="error-message-error-could-not-retrieve-emie-site-list"></a><span data-ttu-id="87c54-144">錯誤訊息：「錯誤：無法擷取 EMIE 網站清單。」</span><span class="sxs-lookup"><span data-stu-id="87c54-144">Error message: "Error: Could not retrieve EMIE site list."</span></span>

<span data-ttu-id="87c54-145">您可能會在 *edge://compat/enterprise* 網頁上看到此錯誤，表示網站清單下載失敗。</span><span class="sxs-lookup"><span data-stu-id="87c54-145">You may see this error on the *edge://compat/enterprise* page indicating that the site list download failed.</span></span> <span data-ttu-id="87c54-146">從 Microsoft Edge 版本 87 開始，當使用 [BlockThirdPartyCookies](./microsoft-edge-policies.md#blockthirdpartycookies) 原則封鎖協力廠商要求的 Cookie 時，也不允許使用 HTTP 驗證。</span><span class="sxs-lookup"><span data-stu-id="87c54-146">Starting with Microsoft Edge version 87, when cookies are blocked for third party requests using the [BlockThirdPartyCookies](./microsoft-edge-policies.md#blockthirdpartycookies) policy, HTTP authentication is also disallowed.</span></span> <span data-ttu-id="87c54-147">可以使用 [CookiesAllowedForURLs](./microsoft-edge-policies.md#cookiesallowedforurls) 原則為裝載 Enterprise Mode Site List 的特定網域允許 Cookie，以確保網站清單下載成功。</span><span class="sxs-lookup"><span data-stu-id="87c54-147">You can allow cookies for the specific domain hosting your Enterprise Mode Site List using the [CookiesAllowedForURLs](./microsoft-edge-policies.md#cookiesallowedforurls) policy to ensure that site list downloads are successful.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="87c54-148">常見問題集</span><span class="sxs-lookup"><span data-stu-id="87c54-148">Frequently Asked Questions</span></span>

### <a name="will-ie-mode-replace-internet-explorer-11"></a><span data-ttu-id="87c54-149">IE 模式是否會取代 Internet Explorer 11？</span><span class="sxs-lookup"><span data-stu-id="87c54-149">Will IE mode replace Internet Explorer 11?</span></span>

<span data-ttu-id="87c54-150">我們致力於將 Internet Explorer 保持為受支援、可靠且安全的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="87c54-150">We're committed to keeping Internet Explorer a supported, reliable, and safe browser.</span></span> <span data-ttu-id="87c54-151">Internet Explorer 仍是 Windows 的元件，並遵循其安裝所在作業系統的支援週期。</span><span class="sxs-lookup"><span data-stu-id="87c54-151">Internet Explorer is still a component of Windows and follows the support lifecycle of the OS on which it's installed.</span></span> <span data-ttu-id="87c54-152">如需詳細資訊，請參閱[生命週期常見問題 – Internet Explorer](https://support.microsoft.com/help/17454/)。</span><span class="sxs-lookup"><span data-stu-id="87c54-152">For details, see [Lifecycle FAQ - Internet Explorer](https://support.microsoft.com/help/17454/).</span></span> <span data-ttu-id="87c54-153">雖然 Microsoft 繼續支援和更新 Internet Explorer，但最新的功能和平台更新僅適用於 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="87c54-153">While Microsoft continues to support and update Internet Explorer, the latest features and platform updates will only be available in Microsoft Edge.</span></span>

### <a name="can-i-use-open-with-explorer-or-view-in-file-explorer-in-sharepoint-with-ie-mode"></a><span data-ttu-id="87c54-154">我可以在 SharePoint 中搭配 IE 模式使用 [在檔案總管中開啟] 或 [在檔案總管中檢視] 嗎？</span><span class="sxs-lookup"><span data-stu-id="87c54-154">Can I use "Open with Explorer" or "View in File Explorer" in SharePoint with IE mode?</span></span>

<span data-ttu-id="87c54-155">是的，如果這在獨立式 Internet Explorer 11 中能正常運作，在 IE 模式中即能正常運作。</span><span class="sxs-lookup"><span data-stu-id="87c54-155">Yes, if this works in standalone Internet Explorer 11 it will work in IE mode.</span></span> <span data-ttu-id="87c54-156">不過，不要使用 [在檔案總管中開啟] 選項，建議用來在 SharePoint 外部管理檔案和資料夾的方法，就是[同步處理您的 SharePoint 檔案](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88)或[在 SharePoint 中移動或複製檔案](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc)。</span><span class="sxs-lookup"><span data-stu-id="87c54-156">However, rather than use the Open with Explorer option, the recommended approach to managing files and folders outside of SharePoint is to [sync your SharePoint files](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) or [move or copy files in SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).</span></span>

### <a name="does-ie-mode-on-microsoft-edge-support-the-nomerge-option-that-was-supported-in-internet-explorer-11"></a><span data-ttu-id="87c54-157">Microsoft Edge 上的 IE 模式是否支援 Internet Explorer 11中支援的 *nomerge* 選項？</span><span class="sxs-lookup"><span data-stu-id="87c54-157">Does IE mode on Microsoft Edge support the *nomerge* option that was supported in Internet Explorer 11?</span></span>

<span data-ttu-id="87c54-158">Microsoft Edge 中沒有任何明確的命令列來鏡像 *nomerge* 選項，但我們建議您使用兩種替代方法來提供此功能。</span><span class="sxs-lookup"><span data-stu-id="87c54-158">There is no explicit command line in Microsoft Edge to mirror the *nomerge* option, but there are a couple of alternatives that we recommend to provide this functionality.</span></span>

1. <span data-ttu-id="87c54-159">在 Microsoft Edge 中使用設定檔：每個設定檔對應 IE 模式頁面的不同 IE 工作模式，因此其運作方式與 *nomerge* 選項相同。</span><span class="sxs-lookup"><span data-stu-id="87c54-159">Use Profiles in Microsoft Edge - Each profile maps to a different IE session for IE mode pages, so it behaves identically to the *nomerge* option.</span></span>
2. <span data-ttu-id="87c54-160">使用 `--user-data-dir=<path>` 命令列，但每個工作模式的路徑不同。</span><span class="sxs-lookup"><span data-stu-id="87c54-160">Use the `--user-data-dir=<path>` command line, but with a different path for each session.</span></span> <span data-ttu-id="87c54-161">如有需要，您可以建立一個公用程式供使用者運行，該公用程式可以啟動 Microsoft Edge 並變更工作模式路徑。</span><span class="sxs-lookup"><span data-stu-id="87c54-161">If needed, you can create a utility for the user to run that both launches Microsoft Edge and changes the path for the session.</span></span>

<span data-ttu-id="87c54-162">如果上述選項都不適用於您的案例，請透過其中一個意見反應通道連絡我們：Microsoft 支援服務或 [TechCommunity 論壇](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)。</span><span class="sxs-lookup"><span data-stu-id="87c54-162">If neither of the above options works for your scenario, reach out through one of our feedback channels:  Microsoft support or [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise).</span></span>

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a><span data-ttu-id="87c54-163">我是否可以在 Internet Explorer 模式中將連結儲存為網頁？</span><span class="sxs-lookup"><span data-stu-id="87c54-163">Can I save links as webpages in Internet Explorer mode?</span></span>

<span data-ttu-id="87c54-164">是的，您可以在 Microsoft Edge 的 Internet Explorer 模式的操作功能表中啟用 [另存目標] 選項。</span><span class="sxs-lookup"><span data-stu-id="87c54-164">Yes, you can enable the Save Target As option in the context menu for Internet Explorer mode in Microsoft Edge.</span></span> <span data-ttu-id="87c54-165">若要這麼做，請設定位於 [電腦設定] > [系統管理範本] > [Windows 元件] > [Internet Explorer]\*\* 下的群組原則 *「允許在 Internet Explorer 模式中另存目標」*。</span><span class="sxs-lookup"><span data-stu-id="87c54-165">To do this, configure the group policy *"Allow Save Target As in Internet Explorer mode"* located at *Computer Configuration > Administrative Templates > Windows Components > Internet Explorer*.</span></span>
<span data-ttu-id="87c54-166">儲存機制的運作方式與在 Internet Explorer 中相同，而如果將目標儲存為 HTML 檔案，重新開啟該檔案就會在 Microsoft Edge 中呈現該頁面。</span><span class="sxs-lookup"><span data-stu-id="87c54-166">The save mechanism works the same as it does in Internet Explorer and if the target is saved as an html file, re-opening the file will render the page in Microsoft Edge.</span></span>
 
<span data-ttu-id="87c54-167">請注意，此功能需要下列最低版本的作業系統更新：</span><span class="sxs-lookup"><span data-stu-id="87c54-167">Note that this functionality requires the following minimum operating system updates:</span></span>
- <span data-ttu-id="87c54-168">Windows 10 版本 2004、Windows Server 版本 2004、Windows 10 版本 20H2：[KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)</span><span class="sxs-lookup"><span data-stu-id="87c54-168">Windows 10, version 2004, Windows Server version 2004, Windows 10, version 20H2 : [KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)</span></span>
- <span data-ttu-id="87c54-169">Windows 10 版本 1903、Windows 10 版本 1909、Windows Server 版本 1903：[KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)</span><span class="sxs-lookup"><span data-stu-id="87c54-169">Windows 10, version 1903, Windows 10, version 1909, Windows Server version 1903: [KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)</span></span>
- <span data-ttu-id="87c54-170">Windows 10 版本 1809、Windows Server 版本 1809、Windows Server 2019：[KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)</span><span class="sxs-lookup"><span data-stu-id="87c54-170">Windows 10, version 1809, Windows Server version 1809, Windows Server 2019: [KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)</span></span>
- <span data-ttu-id="87c54-171">Windows 10 版本 1803：[KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)</span><span class="sxs-lookup"><span data-stu-id="87c54-171">Windows 10, version 1803: [KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)</span></span>
- <span data-ttu-id="87c54-172">Windows 10 版本 1607：[KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)</span><span class="sxs-lookup"><span data-stu-id="87c54-172">Windows 10, version 1607: [KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)</span></span>
- <span data-ttu-id="87c54-173">Windows 10 版本 1507：[KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)</span><span class="sxs-lookup"><span data-stu-id="87c54-173">Windows 10, version 1507: [KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)</span></span>


## <a name="see-also"></a><span data-ttu-id="87c54-174">請參閱</span><span class="sxs-lookup"><span data-stu-id="87c54-174">See also</span></span>

- [<span data-ttu-id="87c54-175">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="87c54-175">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="87c54-176">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="87c54-176">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="87c54-177">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="87c54-177">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)