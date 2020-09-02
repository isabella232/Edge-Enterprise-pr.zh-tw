---
title: IE 模式常見問題集
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/27/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 適用於 IE 模式 Microsoft Edge 的常見問題集和疑難排解
ms.openlocfilehash: fcceb9eab19d667f772c593fe4f362606c1623ff
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979487"
---
# <span data-ttu-id="3f68f-103">IE 模式常見問題集</span><span class="sxs-lookup"><span data-stu-id="3f68f-103">IE mode FAQ</span></span>

<span data-ttu-id="3f68f-104">本文提供 Microsoft Edge (版本 77 或更新版本) 的疑難排解秘訣和常見問題集。</span><span class="sxs-lookup"><span data-stu-id="3f68f-104">This article provides troubleshooting tips and an FAQ for Microsoft Edge (version 77 or later).</span></span>

> [!NOTE]
> <span data-ttu-id="3f68f-105">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3f68f-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <span data-ttu-id="3f68f-106">疑難排解 IE 模式</span><span class="sxs-lookup"><span data-stu-id="3f68f-106">Troubleshoot IE mode</span></span>

<span data-ttu-id="3f68f-107">使用本節中的資訊來診斷和修復 IE 模式問題。</span><span class="sxs-lookup"><span data-stu-id="3f68f-107">Use the information in this section to diagnose and fix IE mode problems.</span></span>

### <span data-ttu-id="3f68f-108">Internet Explorer 模式診斷資訊</span><span class="sxs-lookup"><span data-stu-id="3f68f-108">Internet Explorer mode diagnostic information</span></span>

<span data-ttu-id="3f68f-109">您可以在 Microsoft Edge 相容性索引標籤上取得 Internet Explorer 模式診斷資訊。若要開啟此索引標籤，請移至 *edge://compat/iediagnostic*。</span><span class="sxs-lookup"><span data-stu-id="3f68f-109">You can get Internet Explorer mode diagnostic information on the Microsoft Edge Compatibility tab. To open this tab, go to *edge://compat/iediagnostic*.</span></span> <span data-ttu-id="3f68f-110">此頁面可能會顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="3f68f-110">This page may show diagnostic messages.</span></span> <span data-ttu-id="3f68f-111">本頁也提供下列類別的設定資訊：</span><span class="sxs-lookup"><span data-stu-id="3f68f-111">This page also provides configuration information for the following categories:</span></span>

- <span data-ttu-id="3f68f-112">**登錄機碼檢查**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-112">**Registry key check**.</span></span> <span data-ttu-id="3f68f-113">(只有檢查失敗時才會顯示。) 檢查登錄中是否正確設定了 Internet Explorer 整合。</span><span class="sxs-lookup"><span data-stu-id="3f68f-113">(Displayed only if the check fails.) Checks to see if Internet Explorer integration is set up correctly in the registry.</span></span> <span data-ttu-id="3f68f-114">如果未正確設定，使用者可以按一下**修正**來解決問題。</span><span class="sxs-lookup"><span data-stu-id="3f68f-114">If not, the user can click **Fix it** to resolve the problem.</span></span>
- <span data-ttu-id="3f68f-115">**Internet Explorer 模式**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-115">**Internet Explorer mode**.</span></span> <span data-ttu-id="3f68f-116">顯示所使用的 API 版本，該版本基於設定和作業系統。</span><span class="sxs-lookup"><span data-stu-id="3f68f-116">Shows the API version that's used, based on the configuration and OS.</span></span> <span data-ttu-id="3f68f-117">如果發生問題，可能會提示使用者安裝 **Windows Update**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-117">If there's a problem, the user may be prompted to install a **Windows Update**.</span></span>
- <span data-ttu-id="3f68f-118">**Internet Explorer 模式**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-118">**Internet Explorer mode setting**.</span></span> <span data-ttu-id="3f68f-119">顯示是否已啟用 Internet Explorer 模式，以及其設定方式。</span><span class="sxs-lookup"><span data-stu-id="3f68f-119">Shows whether Internet Explorer mode is enabled, and how it's configured.</span></span>
- <span data-ttu-id="3f68f-120">**命令列**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-120">**Command line**.</span></span> <span data-ttu-id="3f68f-121">顯示用於啟動 Microsoft Edge 的命令列字串和參數。</span><span class="sxs-lookup"><span data-stu-id="3f68f-121">Shows the command line string and switches used to start Microsoft Edge.</span></span>
- <span data-ttu-id="3f68f-122">**群組原則設定**。</span><span class="sxs-lookup"><span data-stu-id="3f68f-122">**Group policy settings**.</span></span> <span data-ttu-id="3f68f-123">顯示是否使用群組原則設定 IE 模式，以及所套用的原則。</span><span class="sxs-lookup"><span data-stu-id="3f68f-123">Shows whether IE mode is configured using group policies, and the policies that are applied.</span></span>

### <span data-ttu-id="3f68f-124">錯誤訊息：「若要在 Internet Explorer 模式中開啟此頁面，請以系統管理員權限重新安裝 Microsoft Edge。」</span><span class="sxs-lookup"><span data-stu-id="3f68f-124">Error message: "To open this page in Internet Explorer mode, reinstall Microsoft Edge with administrator privileges."</span></span>

<span data-ttu-id="3f68f-125">如果您沒有所有必要的 Windows Update，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f68f-125">You may see this error if you don't have all required Windows Updates.</span></span> <span data-ttu-id="3f68f-126">請參閱所需 Windows 和 Microsoft Edge 版本[關於 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)中所列的必要條件。</span><span class="sxs-lookup"><span data-stu-id="3f68f-126">See the prerequisites listed in [About IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode) for the required versions of Windows and Microsoft Edge.</span></span>

<span data-ttu-id="3f68f-127">如果您已安裝所有必要的 Windows Update，您可能會在下列情況下看到此錯誤：</span><span class="sxs-lookup"><span data-stu-id="3f68f-127">If you've already installed all required Windows Updates, you may see this error if:</span></span>

- <span data-ttu-id="3f68f-128">您使用的是 Canary 通道，預設是在使用者層級安裝。</span><span class="sxs-lookup"><span data-stu-id="3f68f-128">You're using the Canary channel, which is installed at the user level by default.</span></span>
- <span data-ttu-id="3f68f-129">您使用的是 Stable、Beta 或 Dev 通道，提示提高權限時，安裝提高權限已取消。</span><span class="sxs-lookup"><span data-stu-id="3f68f-129">You're using the Stable, Beta, or Dev channel, but when prompted for elevation when installing the elevation was canceled.</span></span> <span data-ttu-id="3f68f-130">當您取消提高權限提示時，系統會在使用者層級繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="3f68f-130">When you cancel the elevation prompt, the installation will continue at the user level.</span></span>
- <span data-ttu-id="3f68f-131">Internet Explorer 11 已在 Windows 功能中停用。</span><span class="sxs-lookup"><span data-stu-id="3f68f-131">Internet Explorer 11 has been disabled in Windows Features.</span></span>

<span data-ttu-id="3f68f-132">可能的解決方式：</span><span class="sxs-lookup"><span data-stu-id="3f68f-132">Possible solutions:</span></span>

- <span data-ttu-id="3f68f-133">在系統層級執行任何通道的安裝程式：`installer.exe --system-level`。</span><span class="sxs-lookup"><span data-stu-id="3f68f-133">Run the installer for any channel at the system level: `installer.exe --system-level`.</span></span>
- <span data-ttu-id="3f68f-134">在 Windows 功能中啟用 Internet Explorer 11。</span><span class="sxs-lookup"><span data-stu-id="3f68f-134">Enable Internet Explorer 11 in Windows Features.</span></span>

<span data-ttu-id="3f68f-135">若要檢查 Microsoft Edge 是否安裝在系統層級，請在 Microsoft Edge 網址列中鍵入 "edge://version"。</span><span class="sxs-lookup"><span data-stu-id="3f68f-135">To check if Microsoft Edge is installed at the systems level, type "edge://version" in the Microsoft Edge address bar.</span></span> <span data-ttu-id="3f68f-136">可執行檔路徑將顯示開頭為 *C:\Program Files* 的路徑，表示是系統安裝。</span><span class="sxs-lookup"><span data-stu-id="3f68f-136">The Executable path will show a path starting with *C:\Program Files*, which indicates a system install.</span></span> <span data-ttu-id="3f68f-137">如果可執行檔路徑開頭為 \*C:\Users\*，請解除安裝然後以系統管理員權限重新安裝 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3f68f-137">If the Executable path begins with \*C:\Users\*, uninstall and then reinstall Microsoft Edge with administrator privileges.</span></span>

### <span data-ttu-id="3f68f-138">錯誤訊息：「若要在 IE 模式中開啟此頁面，請嘗試重新啟動 Microsoft Edge。」</span><span class="sxs-lookup"><span data-stu-id="3f68f-138">Error message: "To open this page in IE mode, try restarting Microsoft Edge."</span></span>

<span data-ttu-id="3f68f-139">如果 Internet Explorer 發生未預期的錯誤，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f68f-139">You may see this error if there was an unexpected error in Internet Explorer.</span></span> <span data-ttu-id="3f68f-140">重新啟動 Microsoft Edge 通常可以修正此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f68f-140">Restarting Microsoft Edge usually fixes this error.</span></span>

### <span data-ttu-id="3f68f-141">錯誤訊息：「請關閉遠端偵錯以在 IE 模式下開啟此網站，否則可能無法如預期運作。」</span><span class="sxs-lookup"><span data-stu-id="3f68f-141">Error message: "Turn off remote debugging to open this site in IE mode otherwise it might not work as expected."</span></span>

<span data-ttu-id="3f68f-142">如果您正在遠端偵錯，且瀏覽至設定為在 IE 模式中執行的網頁，您可能會看到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="3f68f-142">You may see this error if you're remote debugging and navigate to a web page configured to run in IE mode.</span></span> <span data-ttu-id="3f68f-143">您可以繼續，但是頁面將會使用 Microsoft Edge 轉譯。</span><span class="sxs-lookup"><span data-stu-id="3f68f-143">You can continue, but the page will be rendered using Microsoft Edge.</span></span>

## <span data-ttu-id="3f68f-144">常見問題集</span><span class="sxs-lookup"><span data-stu-id="3f68f-144">Frequently Asked Questions</span></span>

### <span data-ttu-id="3f68f-145">IE 模式是否會取代 Internet Explorer 11？</span><span class="sxs-lookup"><span data-stu-id="3f68f-145">Will IE mode replace Internet Explorer 11?</span></span>

<span data-ttu-id="3f68f-146">我們致力於將 Internet Explorer 保持為受支援、可靠且安全的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="3f68f-146">We're committed to keeping Internet Explorer a supported, reliable, and safe browser.</span></span> <span data-ttu-id="3f68f-147">Internet Explorer 仍是 Windows 的元件，並遵循其安裝所在作業系統的支援週期。</span><span class="sxs-lookup"><span data-stu-id="3f68f-147">Internet Explorer is still a component of Windows and follows the support lifecycle of the OS on which it's installed.</span></span> <span data-ttu-id="3f68f-148">如需詳細資訊，請參閱[生命週期常見問題 – Internet Explorer](https://support.microsoft.com/help/17454/)。</span><span class="sxs-lookup"><span data-stu-id="3f68f-148">For details, see [Lifecycle FAQ - Internet Explorer](https://support.microsoft.com/help/17454/).</span></span> <span data-ttu-id="3f68f-149">雖然 Microsoft 繼續支援和更新 Internet Explorer，但最新的功能和平台更新僅適用於 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3f68f-149">While Microsoft continues to support and update Internet Explorer, the latest features and platform updates will only be available in Microsoft Edge.</span></span>

### <span data-ttu-id="3f68f-150">我可以在 SharePoint 中搭配 IE 模式使用 [在檔案總管中開啟] 或 [在檔案總管中檢視] 嗎？</span><span class="sxs-lookup"><span data-stu-id="3f68f-150">Can I use "Open with Explorer" or "View in File Explorer" in SharePoint with IE mode?</span></span>

<span data-ttu-id="3f68f-151">是的，如果這在獨立式 Internet Explorer 11 中能正常運作，在 IE 模式中即能正常運作。</span><span class="sxs-lookup"><span data-stu-id="3f68f-151">Yes, if this works in standalone Internet Explorer 11 it will work in IE mode.</span></span> <span data-ttu-id="3f68f-152">不過，不要使用 [在檔案總管中開啟] 選項，建議用來在 SharePoint 外部管理檔案和資料夾的方法，就是[同步處理您的 SharePoint 檔案](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88)或[在 SharePoint 中移動或複製檔案](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc)。</span><span class="sxs-lookup"><span data-stu-id="3f68f-152">However, rather than use the Open with Explorer option, the recommended approach to managing files and folders outside of SharePoint is to [sync your SharePoint files](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88) or [move or copy files in SharePoint](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc).</span></span>

### <span data-ttu-id="3f68f-153">Microsoft Edge 上的 IE 模式是否支援 Internet Explorer 11中支援的 *nomerge* 選項？</span><span class="sxs-lookup"><span data-stu-id="3f68f-153">Does IE mode on Microsoft Edge support the *nomerge* option that was supported in Internet Explorer 11?</span></span>

<span data-ttu-id="3f68f-154">Microsoft Edge 中沒有任何明確的命令列來鏡像 *nomerge* 選項，但我們建議您使用兩種替代方法來提供此功能。</span><span class="sxs-lookup"><span data-stu-id="3f68f-154">There is no explicit command line in Microsoft Edge to mirror the *nomerge* option, but there are a couple of alternatives that we recommend to provide this functionality.</span></span>

1. <span data-ttu-id="3f68f-155">在 Microsoft Edge 中使用設定檔：每個設定檔對應 IE 模式頁面的不同 IE 工作模式，因此其運作方式與 *nomerge* 選項相同。</span><span class="sxs-lookup"><span data-stu-id="3f68f-155">Use Profiles in Microsoft Edge - Each profile maps to a different IE session for IE mode pages, so it behaves identically to the *nomerge* option.</span></span>
2. <span data-ttu-id="3f68f-156">使用 `--user-data-dir=<path>` 命令列，但每個工作模式的路徑不同。</span><span class="sxs-lookup"><span data-stu-id="3f68f-156">Use the `--user-data-dir=<path>` command line, but with a different path for each session.</span></span> <span data-ttu-id="3f68f-157">如有需要，您可以建立一個公用程式供使用者運行，該公用程式可以啟動 Microsoft Edge 並變更工作模式路徑。</span><span class="sxs-lookup"><span data-stu-id="3f68f-157">If needed, you can create a utility for the user to run that both launches Microsoft Edge and changes the path for the session.</span></span>

<span data-ttu-id="3f68f-158">如果上述選項都不適用於您的案例，請透過其中一個意見反應通道聯絡我們： Microsoft 支援服務、 [TechCommunity 論壇](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)，或 [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/forums/928825-enterprise)。</span><span class="sxs-lookup"><span data-stu-id="3f68f-158">If neither of the above options works for your scenario, reach out through one of our feedback channels:  Microsoft support, [TechCommunity forum](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise), or [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/forums/928825-enterprise).</span></span>

## <span data-ttu-id="3f68f-159">請參閱</span><span class="sxs-lookup"><span data-stu-id="3f68f-159">See also</span></span>

- [<span data-ttu-id="3f68f-160">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3f68f-160">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3f68f-161">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="3f68f-161">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="3f68f-162">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="3f68f-162">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)