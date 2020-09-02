---
title: 規劃 Microsoft Edge 部署
ms.author: cjacks
author: appcompatguy
manager: saudm
ms.date: 04/23/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 規劃 Microsoft Edge 部署
ms.openlocfilehash: 3ac3d050578ca4f230ed7e775aefb73f11abb3c0
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979502"
---
# <span data-ttu-id="d1ca3-103">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="d1ca3-103">Plan your deployment of Microsoft Edge</span></span>

<span data-ttu-id="d1ca3-104">本文介紹了在企業環境中部署 Microsoft Edge 的建議做法。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-104">This article describes the recommended practices for deploying Microsoft Edge in an enterprise environment.</span></span>

>[!NOTE]
><span data-ttu-id="d1ca3-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="d1ca3-106">評估您現有的瀏覽器環境和瀏覽器需求</span><span class="sxs-lookup"><span data-stu-id="d1ca3-106">Evaluate your existing browser environment and browser needs</span></span>

<span data-ttu-id="d1ca3-107">花些時間瞭解您當前的瀏覽器狀態和專案願景，以確保所有專案關係人都保持一致，並朝著相同的結果努力。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-107">Take time to understand your current browser state and project vision to ensure that all project stakeholders are aligned and working towards the same result.</span></span>

<span data-ttu-id="d1ca3-108">首先定義目前狀態：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-108">Start by defining your current state:</span></span>

- <span data-ttu-id="d1ca3-109">目前在您的環境中部署了哪些瀏覽器？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-109">Which browsers are currently deployed in your environment?</span></span>
- <span data-ttu-id="d1ca3-110">哪個瀏覽器設定成預設瀏覽器？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-110">Which browser is set as the default browser?</span></span>
- <span data-ttu-id="d1ca3-111">您是否需要對某些應用程式使用 Internet Explorer？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-111">Do you need to use Internet Explorer for some of your apps?</span></span>
- <span data-ttu-id="d1ca3-112">您現在是否使用企業模式網站清單來設定 Internet Explorer？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-112">Do you use an Enterprise Mode Site List to configure Internet Explorer today?</span></span>
- <span data-ttu-id="d1ca3-113">您的環境中支援哪些作業系統平台？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-113">What OS platforms are supported in your environment?</span></span> <span data-ttu-id="d1ca3-114">(Windows 10、macOS、Windows 7、Windows Server 等等)</span><span class="sxs-lookup"><span data-stu-id="d1ca3-114">(Windows 10, macOS, Windows 7, Windows Server, etc.)</span></span>
- <span data-ttu-id="d1ca3-115">您使用哪些管理工具進行瀏覽器管理？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-115">What management tools do you use for browser management?</span></span>
- <span data-ttu-id="d1ca3-116">誰負責瀏覽器設定和管理？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-116">Who is responsible for browser configuration and management?</span></span>
- <span data-ttu-id="d1ca3-117">驗證瀏覽器相容性的程序是什麼？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-117">What is your process for validating browser compatibility?</span></span>

<span data-ttu-id="d1ca3-118">了解目前狀態後，可以確定瀏覽器部署的預期目標，同時考慮到以下事項：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-118">After you understand the current state, you can determine the desired goals for your browser deployment, taking into account the following:</span></span>

- <span data-ttu-id="d1ca3-119">是否要[將 Microsoft Edge 設定為預設瀏覽器](https://docs.microsoft.com/DeployEdge/edge-default-browser)？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-119">Do you want to [set Microsoft Edge as your default browser](https://docs.microsoft.com/DeployEdge/edge-default-browser)?</span></span>
- <span data-ttu-id="d1ca3-120">是否要隱藏舊版 Microsoft Edge，還是希望[將其保留給使用者使用](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-access-old-edge)？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-120">Do you want to hide the legacy version of Microsoft Edge, or do you want to [leave it available for users](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-access-old-edge)?</span></span>
- <span data-ttu-id="d1ca3-121">您將如何[設定 Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-121">How will you [configure Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)?</span></span>
- <span data-ttu-id="d1ca3-122">在初始部署中要設定哪些重要功能？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-122">What features are critical to configure as part of your initial deployment?</span></span>
- <span data-ttu-id="d1ca3-123">解決任何已識別的相容性或設定問題的過程是什麼？</span><span class="sxs-lookup"><span data-stu-id="d1ca3-123">What is the process for addressing any identified compatibility or configuration issues?</span></span>

<span data-ttu-id="d1ca3-124">您還應了解您感興趣的功能的**先決條件**，例如：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-124">You should also understand the **pre-requisites** for features you're interested in, such as:</span></span>

- [<span data-ttu-id="d1ca3-125">Windows Defender 應用程式防護</span><span class="sxs-lookup"><span data-stu-id="d1ca3-125">Windows Defender Application Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [<span data-ttu-id="d1ca3-126">Internet Explorer 模式</span><span class="sxs-lookup"><span data-stu-id="d1ca3-126">Internet Explorer mode</span></span>](https://docs.microsoft.com/DeployEdge/edge-ie-mode)
- [<span data-ttu-id="d1ca3-127">驗證與同步</span><span class="sxs-lookup"><span data-stu-id="d1ca3-127">Authentication and sync</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-identity)

<span data-ttu-id="d1ca3-128">有了這些答案，您已準備好規劃 Microsoft Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-128">With these answers in mind, you're ready to planning your Microsoft Edge deployment.</span></span>
<!--bookmark -->

## <span data-ttu-id="d1ca3-129">確定您的 Windows 10 裝置已準備就緒</span><span class="sxs-lookup"><span data-stu-id="d1ca3-129">Make sure your Windows 10 devices are ready</span></span>

<span data-ttu-id="d1ca3-130">Microsoft Edge 穩定通道需要自 2019 年 10 月 (或更新版本) 的最新累積更新 (LCU)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-130">The Edge Stable channel requires the Latest Cumulative Update (LCU) from October 2019 (or later).</span></span> <span data-ttu-id="d1ca3-131">如果您嘗試部署到具有舊版 LCU 的 Windows 10 裝置，安裝便會失敗。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-131">If you attempt to deploy to a Windows 10 device that has an older LCU, then the installation will fail.</span></span> <span data-ttu-id="d1ca3-132">如需部署 Microsoft Edge 前必須套用的最小 LCU 的詳細資料，請參閱[支援下一版 Microsoft Edge 的 Windows Update](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-windows-updates)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-132">For more details about the minimum LCU that must be applied before deploying Edge, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-windows-updates).</span></span>

## <span data-ttu-id="d1ca3-133">決定您的部署方法</span><span class="sxs-lookup"><span data-stu-id="d1ca3-133">Determine your deployment methodology</span></span>

<span data-ttu-id="d1ca3-134">在您了解所需的結束狀態後，您就可以開始規劃如何實現目標。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-134">After you know your desired end state, you're ready to start planning how to get there.</span></span> <span data-ttu-id="d1ca3-135">部署 Microsoft Edge 的兩種主要方式是依角色和依網站部署。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-135">The two main ways to deploy Microsoft Edge are by role, and by site.</span></span>

### <span data-ttu-id="d1ca3-136">依角色部署到終端使用者</span><span class="sxs-lookup"><span data-stu-id="d1ca3-136">Deploy to end users by role</span></span>

<span data-ttu-id="d1ca3-137">如果應用程式相容性是您主要關心的問題，並且您沒有確定要測試哪些應用程式，則可能需要考慮依角色部署到終端使用者。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-137">If app compatibility is your main concern, and you don't have a firm grasp on which apps to test, you might want to consider deploying to end users by role.</span></span> <span data-ttu-id="d1ca3-138">如此一來，對需要修改其設定以解決相容性問題的應用程式，每一波的分階段部署都能夠提供意見反應和見解。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-138">This enables each wave of a phased deployment to provide feedback and insights on apps that might need to have their configuration modified to address compatibility issues.</span></span>

### <span data-ttu-id="d1ca3-139">依網站部署到終端使用者</span><span class="sxs-lookup"><span data-stu-id="d1ca3-139">Deploy to end users by site</span></span>

<span data-ttu-id="d1ca3-140">如果頻寬是您主要關心的問題，您可能需要考慮提前進行應用程式相容性測試。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-140">If bandwidth is your primary concern, you might want to consider doing application compatibility testing up front.</span></span> <span data-ttu-id="d1ca3-141">完成測試後，依網站部署到終端使用者，以便可以利用快取對其他軟體進行傳遞最佳化。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-141">After you finish testing, deploy to end users by site so you can leverage caching other software delivery optimizations.</span></span>

## <span data-ttu-id="d1ca3-142">執行站台探索</span><span class="sxs-lookup"><span data-stu-id="d1ca3-142">Do site discovery</span></span>

<span data-ttu-id="d1ca3-143">如果您依賴於舊版 Web 應用程式，並計畫使用 Internet Explorer 模式 (大多數客戶都這樣做)，則可能需要執行一些額外的站台探索。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-143">If you have a dependency on legacy web applications, and plan to use Internet Explorer mode (which most customers do), then you probably need to do some additional site discovery.</span></span>

### <span data-ttu-id="d1ca3-144">如果您已經部署並設定舊版 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1ca3-144">If you've already deployed and configured the legacy version of Microsoft Edge</span></span>

<span data-ttu-id="d1ca3-145">如果您已將企業網站清單設定為適用於舊版 Microsoft Edge，則您的工作已基本完成！</span><span class="sxs-lookup"><span data-stu-id="d1ca3-145">If you've already configured your Enterprise Site List to work for the legacy version of Microsoft Edge, then your work is almost done!</span></span> <span data-ttu-id="d1ca3-146">您可能需要新增的一件事是中性網站。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-146">The one thing you may need to add are neutral sites.</span></span>

<span data-ttu-id="d1ca3-147">中性網站通常是提供單一登入 (SSO) 的網站。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-147">Neutral sites are typically sites that provide Single Sign-On (SSO).</span></span> <span data-ttu-id="d1ca3-148">如果從 Microsoft Edge 瀏覽到中性網站，要留在 Microsoft Edge 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-148">If you navigate to a neutral site from Microsoft Edge, then you want to stay in Microsoft Edge to authenticate.</span></span> <span data-ttu-id="d1ca3-149">如果在 Internet Explorer 模式下瀏覽到中性網站，則要保持 Internet Explorer 模式進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-149">If navigate to a neutral site in Internet Explorer mode, then you want to stay in Internet Explorer mode to authenticate.</span></span>

<span data-ttu-id="d1ca3-150">識別您使用的任何 SSO (或其他中性) 網站，並將這些網站新增到企業網站清單中。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-150">Identify any SSO (or other neutral) sites that you use and add these to your Enterprise Site List.</span></span>

### <span data-ttu-id="d1ca3-151">如果您已將 Internet Explorer 設定為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="d1ca3-151">If you've configured Internet Explorer as your default browser</span></span>

<span data-ttu-id="d1ca3-152">如果您目前僅使用 Internet Explorer，則可能不知道哪些網站已升級到現代網站標準，哪些網站仍需要 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-152">If you're currently only using Internet Explorer, you might not know which sites have upgraded to modern web standards and which still require Internet Explorer.</span></span> <span data-ttu-id="d1ca3-153">您要找到這些網站並將其新增到企業網站清單中。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-153">You want to find these sites and add them to the Enterprise Site List.</span></span> <span data-ttu-id="d1ca3-154">這可讓您僅在需要的網站上使用 Internet Explorer 模式。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-154">This lets you use Internet Explorer mode only on the sites that need it.</span></span>

> [!TIP]
> <span data-ttu-id="d1ca3-155">使用[企業網站探索](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery?redirectedfrom=MSDN)工具，發現可能需要 Internet Explorer 模式的網站。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-155">Use the [Enterprise Site Discovery](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery?redirectedfrom=MSDN) tools to discover the sites that might need Internet Explorer mode.</span></span> <span data-ttu-id="d1ca3-156">您可以在執行 Windows Internet Explorer 8 到 Internet Explorer 11 的 Windows 10、Windows 8.1 或 Windows 7 電腦上收集資料。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-156">You can collect collect data on computers running Windows Internet Explorer 8 through Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7.</span></span>

### <span data-ttu-id="d1ca3-157">分析站台探索資料</span><span class="sxs-lookup"><span data-stu-id="d1ca3-157">Analyze site discovery data</span></span>

<span data-ttu-id="d1ca3-158">收集網站資料後，我們建議採用以下 4 步驟程序來分析資料：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-158">After you've collected site data, we recommend the following 4-step process to analyze the data:</span></span>

1. <span data-ttu-id="d1ca3-159">依網域，然後依 URL 對資料進行分類。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-159">Sort the data by domain, and then by URL.</span></span>
2. <span data-ttu-id="d1ca3-160">定義「應用程式」的界限，為 Internet Explorer 模式進行設定。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-160">Define the boundaries of an "app" to configure for Internet Explorer mode.</span></span> <span data-ttu-id="d1ca3-161">您要包括定義應用程式的所有網站和 Web 控制項。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-161">You want to include all the sites and web controls that define the app.</span></span> <span data-ttu-id="d1ca3-162">但是，不要太廣泛地定義應用程式，包含任何額外的網站和控制項。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-162">But you don't want to include any extra sites and controls by defining the app too broadly.</span></span> <span data-ttu-id="d1ca3-163">某些網站可能像 "http://contoso.com/app1" 一樣簡單，某些網站可能要求您定義多個網站和頁面。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-163">Some sites may be as simple as "http://contoso.com/app1" while others may require you to define multiple sites and pages.</span></span>
3. <span data-ttu-id="d1ca3-164">測試應用程式以確認是否無法原生運作。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-164">Test the app to verify that it doesn't work natively.</span></span> <span data-ttu-id="d1ca3-165">許多網站在偵測到現代瀏覽器時會提供現代內容，並且僅在偵測到 Internet Explorer 時提供舊版內容。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-165">Many sites will offer modern content when they detect a modern browser, and only offer legacy content when they detect Internet Explorer.</span></span>
4. <span data-ttu-id="d1ca3-166">如果應用程式未通過測試，則將其新增到企業網站清單中。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-166">Add the app to your Enterprise Site list if it fails testing.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d1ca3-167">最佳做法是，對組成應用程式的所有網站分組在一起。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-167">As a best practice, group all of the sites that comprise an app.</span></span> <span data-ttu-id="d1ca3-168">如果所有網站都需要用於完成一項工作，並且它們傾向於一起更新，則表示它們應該分組在一起。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-168">If the sites all need to be used to accomplish one task, and if they tend to be updated together, that is a good indication that they should be grouped.</span></span> <span data-ttu-id="d1ca3-169">這樣，當您升級應用程式時，從 Internet Explorer 模式中刪除整個網站，並為該應用程式開始使用現代瀏覽器會更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-169">This way, when you upgrade an app, it's easier to remove the entire site from Internet Explorer mode and start using a modern browser for that app.</span></span>

## <span data-ttu-id="d1ca3-170">決定您的通道策略</span><span class="sxs-lookup"><span data-stu-id="d1ca3-170">Determine your channel strategy</span></span>

<span data-ttu-id="d1ca3-171">Microsoft Edge 在[多個通道](https://docs.microsoft.com/DeployEdge/microsoft-edge-channels)中發行。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-171">Microsoft Edge is released in [multiple channels](https://docs.microsoft.com/DeployEdge/microsoft-edge-channels).</span></span>

> [!NOTE]
> <span data-ttu-id="d1ca3-172">您可以在裝置上安裝多個通道</span><span class="sxs-lookup"><span data-stu-id="d1ca3-172">You can install more than one channel on a device</span></span>

<span data-ttu-id="d1ca3-173">穩定通道是您希望部署到大多數裝置的通道。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-173">The Stable Channel is what you will want to deploy to most devices.</span></span> <span data-ttu-id="d1ca3-174">但是，應考慮包含多個裝置和多個通道的部署策略。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-174">However, you should consider a deployment strategy that includes multiple devices and multiple channels.</span></span>

### <span data-ttu-id="d1ca3-175">多個裝置和通道</span><span class="sxs-lookup"><span data-stu-id="d1ca3-175">Multiple devices and channels</span></span>

<span data-ttu-id="d1ca3-176">我們建議將具有代表性的裝置子集設定為使用 Beta 通道。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-176">We recommend having a representative subset of devices configured to use the Beta Channel.</span></span> <span data-ttu-id="d1ca3-177">這樣，您就可以預覽即將推出的瀏覽器變更。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-177">This lets you preview upcoming changes to the browser.</span></span> <span data-ttu-id="d1ca3-178">您可以看到這些變更是否會影響終端使用者或應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-178">You can see if these changes are going to affect your end users or apps.</span></span>

<span data-ttu-id="d1ca3-179">您可能還要為某些角色 (如 Web 開發人員) 提供 Dev 通道 (甚至 Canary 通道)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-179">You might also want to make the Dev Channel (or even the Canary Channel) available to some roles, such as web developers.</span></span> <span data-ttu-id="d1ca3-180">考慮希望用更流暢和快速變化的通道來鎖定某些裝置，還是讓這些通道可供使用者選擇安裝。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-180">Consider whether you would like to target some devices with more fluid and rapidly changing channels, or simply make these channels available for users to opt to install.</span></span>

<span data-ttu-id="d1ca3-181">由於可以在裝置上安裝多個通道，因此當使用者選擇安裝發行前版本的通道時，可以降低測試的風險。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-181">Because it's possible to install multiple channels on a device, you can mitigate the risk of testing for users who have opted to install a pre-release channel.</span></span> <span data-ttu-id="d1ca3-182">例如，如果使用者正在使用 Beta 通道，並且發生問題，就可以切換到穩定通道並繼續工作。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-182">For example, if you have a user who's using the Beta Channel, and there's a problem, they can switch to the Stable Channel and continue working.</span></span> <span data-ttu-id="d1ca3-183">這不會造成障礙，直到問題得到解決。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-183">This unblocks them until the issue can be fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="d1ca3-184">如果使用者啟用同步，則其設定將跨通道同步，從而更輕鬆地在通道之間轉換。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-184">If the user enabled Sync, then their configuration will sync across channels, making it even easier to transition between channels.</span></span>

## <span data-ttu-id="d1ca3-185">定義和設定原則</span><span class="sxs-lookup"><span data-stu-id="d1ca3-185">Define and configure policies</span></span>

<span data-ttu-id="d1ca3-186">建立企業網站清單後，我們建議您識別和設定要使用 Microsoft Edge 部署的原則。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-186">After you've created your Enterprise Site List, we recommend identifying and configuring the policies that you intend to deploy with Microsoft Edge.</span></span> <span data-ttu-id="d1ca3-187">這可確保在執行測試時套用這些原則。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-187">This ensures that these policies are applied when you perform your testing.</span></span>

<span data-ttu-id="d1ca3-188">首先，考慮您希望使用者擁有的初次執行體驗。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-188">First, consider the first-run experience you want your users to have.</span></span> <span data-ttu-id="d1ca3-189">如果要從目前瀏覽器自動匯入設定，請設定 [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun) 原則。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-189">If you want to automatically import settings from the current browser, configure the policy for [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun).</span></span>

<span data-ttu-id="d1ca3-190">對於安全性原則，我們建議從 Microsoft Edge 安全性基準開始。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-190">For security policies, we recommend starting with the Microsoft Edge Security Baseline.</span></span> <span data-ttu-id="d1ca3-191">可以使用[建議的安全性基準設定](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991)或使用 [Microsoft Intune](https://docs.microsoft.com/intune/protect/security-baseline-settings-edge) 來套用安全性基準。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-191">The Security Baseline can be applied using the [recommended security configuration baseline settings](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991) or by using [Microsoft Intune](https://docs.microsoft.com/intune/protect/security-baseline-settings-edge).</span></span>

<span data-ttu-id="d1ca3-192">對於其他原則，我們建議檢閱 [Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies) 和 [Microsoft Edge 更新](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies)的原則設定。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-192">For other policies, we recommend reviewing the policy configurations for [Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies) and [Microsoft Edge Updates](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies).</span></span>

### <span data-ttu-id="d1ca3-193">定義更新策略和原則</span><span class="sxs-lookup"><span data-stu-id="d1ca3-193">Define your update strategy and policies</span></span>

<span data-ttu-id="d1ca3-194">您還要確定在部署 Microsoft Edge 後要如何執行更新：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-194">You also want to determine how you want to do updates after you deploy Microsoft Edge:</span></span>

- <span data-ttu-id="d1ca3-195">**允許 Microsoft Edge 自行更新** (預設)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-195">**Allow Microsoft Edge to update itself** (default).</span></span> <span data-ttu-id="d1ca3-196">如果選擇允許自動更新 Microsoft Edge，則 Microsoft Edge 將依您部署的通道確定的速度自動更新。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-196">If you choose to allow automatic updates of Microsoft Edge, then Microsoft Edge will automatically update itself at the pace determined by the channel(s) you deployed.</span></span>
- <span data-ttu-id="d1ca3-197">**依照您自己的步調更新 Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-197">**Update Microsoft Edge at your own pace**.</span></span> <span data-ttu-id="d1ca3-198">如果希望明確控制部署更新的時間，可以停用自動更新並自行部署 (請參閱[更新原則參考](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies))。停用自動更新後，您可以使用以下工具之一為每個通道部署更新：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-198">If you prefer to have explicit control over when updates are deployed, you can disable automatic updates and deploy it yourself (see the [Update Policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies).) After you disable automatic updates you can deploy updates for each channel using one of the following tools:</span></span>

- [<span data-ttu-id="d1ca3-199">Intune</span><span class="sxs-lookup"><span data-stu-id="d1ca3-199">Intune</span></span>](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [<span data-ttu-id="d1ca3-200">Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="d1ca3-200">Configuration Manager</span></span>](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)
- <span data-ttu-id="d1ca3-201">您選擇的部署工具。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-201">the deployment tool of your choice.</span></span>

<span data-ttu-id="d1ca3-202">無論您的更新策略如何，我們建議利用環型部署策略。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-202">Regardless of your update strategy, we recommend leveraging a ringed deployment strategy.</span></span> <span data-ttu-id="d1ca3-203">透過自動更新，這意味著具代表性的使用者樣本執行 Beta 通道，以識別通道 (將成為穩定通道) 的問題。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-203">With automatic updates, this means having a representative sample of users running the Beta Channel, to identify issues with what will become the Stable Channel.</span></span> <span data-ttu-id="d1ca3-204">使用手動更新時，這可能還包括在新的穩定通道組建發行後，對試驗群組進行其他驗證。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-204">With manual updates, this might also include additional validation of a pilot group after a new Stable Channel build is released.</span></span> <span data-ttu-id="d1ca3-205">隨後是廣泛部署。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-205">This is followed by broad deployment.</span></span>

>[!NOTE]
><span data-ttu-id="d1ca3-206">Microsoft Edge 支援僅適用於每個通道中的最新版本的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1ca3-206">Microsoft Edge support will only apply to the most recent version of Microsoft Edge in each channel</span></span>

## <span data-ttu-id="d1ca3-207">執行應用程式相容性測試</span><span class="sxs-lookup"><span data-stu-id="d1ca3-207">Do app compatibility testing</span></span>

<span data-ttu-id="d1ca3-208">Microsoft Edge 的應用程式相容性非常高 - 如此之高，Microsoft 提供了以下相容性承諾：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-208">Application compatibility for Microsoft Edge is extremely high - so high that Microsoft provides the following compatibility promises:</span></span>

1. <span data-ttu-id="d1ca3-209">如果它適用於 Microsoft Edge *版本 45 及更早版本*，也會適用於 Microsoft Edge *77 版及更高版本*。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-209">If it works on Microsoft Edge *version 45 and earlier*, it will work on Microsoft Edge *version 77 and later*.</span></span>
2. <span data-ttu-id="d1ca3-210">如果它適用於 Internet Explorer，也會適用於 Internet Explorer 模式的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-210">If it works on Internet Explorer, it will work on Microsoft Edge in Internet Explorer mode.</span></span>
3. <span data-ttu-id="d1ca3-211">如果它適用於 Google Chrome，也會適用於 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-211">If it works on Google Chrome, it will work on Microsoft Edge.</span></span>

<span data-ttu-id="d1ca3-212">如果在您的應用程式中，不符合這個承諾，我們會信守承諾，透過 [Microsoft App 保證](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure)修復它。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-212">If you have an application where we don't meet this promise, then we stand behind the promise to fix it with [Microsoft App Assure](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure).</span></span>

<span data-ttu-id="d1ca3-213">儘管有此承諾，我們知道許多組織基於合規性或風險管理的原因，必須驗證某些應用程式。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-213">Despite this promise, we know that many organizations must validate some applications for their compliance or risk management reasons.</span></span> <span data-ttu-id="d1ca3-214">儘管我們期望這非常簡單，但在應用程式測試中，有條理和嚴格是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-214">Even though we expect this to be very straightforward, it's important to be organized and rigorous in app testing.</span></span>

<span data-ttu-id="d1ca3-215">有兩種方法可以執行應用程式相容性測試：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-215">There are 2 ways to do app compatibility testing:</span></span>

1. <span data-ttu-id="d1ca3-216">實驗室測試。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-216">Lab testing.</span></span> <span data-ttu-id="d1ca3-217">應用程式在具有特定設定的嚴格控制環境中進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-217">Applications are validated in a tightly controlled environment with specific configurations.</span></span>
2. <span data-ttu-id="d1ca3-218">試驗測試。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-218">Pilot testing.</span></span> <span data-ttu-id="d1ca3-219">應用程式由數量有限的使用者在其日常工作環境中使用自己的裝置進行驗證。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-219">Applications are validated by a limited number of users in their daily work environment using their own devices.</span></span>

<span data-ttu-id="d1ca3-220">選擇最適合每個應用程式的方法，以管理風險，而不會在相容性測試中過度投資。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-220">Choose the method that is most appropriate for each app,  to manage risk without over-investing in compatibility testing.</span></span>

## <span data-ttu-id="d1ca3-221">將 Microsoft Edge 部署到試驗群組</span><span class="sxs-lookup"><span data-stu-id="d1ca3-221">Deploy Microsoft Edge to a pilot group</span></span>

<span data-ttu-id="d1ca3-222">定義原則並完成初始應用程式相容性測試後，即可部署到試驗群組。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-222">After you've defined your policies and have finished your initial app compatibility testing, you're ready to deploy to your pilot group.</span></span> <span data-ttu-id="d1ca3-223">使用以下工具之一，部署到試驗群組：</span><span class="sxs-lookup"><span data-stu-id="d1ca3-223">Deploy to your pilot group using one of the following tools:</span></span>

- <span data-ttu-id="d1ca3-224">[適用於 Windows 的Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)，或[適用於 macOS 的 Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-edge-macos?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)</span><span class="sxs-lookup"><span data-stu-id="d1ca3-224">[Microsoft Intune for Windows](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json), or [Microsoft Intune for macOS](https://docs.microsoft.com/intune/apps/apps-edge-macos?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)</span></span>
- <span data-ttu-id="d1ca3-225">[Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-225">[Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager).</span></span>
- <span data-ttu-id="d1ca3-226">另一個管理工具，下載並部署 [Microsoft Edge 的 MSI 檔案](https://www.microsoftedgeinsider.com/enterprise)。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-226">Another management tool, download and deploy the [MSI file for Microsoft Edge](https://www.microsoftedgeinsider.com/enterprise).</span></span>

## <span data-ttu-id="d1ca3-227">驗證部署</span><span class="sxs-lookup"><span data-stu-id="d1ca3-227">Validate your deployment</span></span>

<span data-ttu-id="d1ca3-228">部署試驗後，您要擷取從使用者獲得的所有意見反應。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-228">After you deploy your pilot, you want to capture all the feedback you get from your users.</span></span>

- <span data-ttu-id="d1ca3-229">擷取有關相容性的意見反應。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-229">Capture feedback on compatibility.</span></span> <span data-ttu-id="d1ca3-230">識別企業網站清單中於網站探索期間未識別的網站。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-230">Identify sites that belong on the Enterprise Site List that weren't identified during site discovery.</span></span>
- <span data-ttu-id="d1ca3-231">擷取有關原則設定的意見反應。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-231">Capture feedback on the policy configuration.</span></span> <span data-ttu-id="d1ca3-232">確保使用者可以使用關鍵功能並完成工作，同時遵循安全性準則。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-232">Ensure that users can use key features and do their work while following security guidelines.</span></span>
- <span data-ttu-id="d1ca3-233">擷取有關易用性和新功能的意見反應。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-233">Capture feedback on ease of use and new features.</span></span> <span data-ttu-id="d1ca3-234">根據使用者問題，確定應開發和提供訓練的任何領域。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-234">Identify any areas where training should be developed and delivered based on user questions.</span></span>

## <span data-ttu-id="d1ca3-235">Microsoft Edge 的廣泛部署</span><span class="sxs-lookup"><span data-stu-id="d1ca3-235">Broad deployment of Microsoft Edge</span></span>

<span data-ttu-id="d1ca3-236">完成試驗，並使用從試驗中吸取的經驗教訓更新部署計畫後，即可對所有使用者執行 Microsoft Edge 的全面部署。</span><span class="sxs-lookup"><span data-stu-id="d1ca3-236">After a finishing the pilot and updating your deployment plan with lessons learned from the pilot, you're ready to do a full deployment of Microsoft Edge to all your users.</span></span>  <span data-ttu-id="d1ca3-237">恭喜！</span><span class="sxs-lookup"><span data-stu-id="d1ca3-237">Congratulations!</span></span>

## <span data-ttu-id="d1ca3-238">請參閱</span><span class="sxs-lookup"><span data-stu-id="d1ca3-238">See also</span></span>

- [<span data-ttu-id="d1ca3-239">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="d1ca3-239">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="d1ca3-240">影片 - 部署 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d1ca3-240">Video - Deploy Microsoft Edge</span></span>](microsoft-edge-video-deploy.md)

