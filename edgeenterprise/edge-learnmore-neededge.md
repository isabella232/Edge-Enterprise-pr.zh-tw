---
title: 針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge
ms.openlocfilehash: ce9e8dabdff25cc3ba375746ec82ddd78b6d7694
ms.sourcegitcommit: cf991cc4bd2e70169902cbda9ddc870d70e31ca2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120518"
---
# <span data-ttu-id="bcf58-103">針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bcf58-103">Redirection from Internet Explorer to Microsoft Edge for compatibility with modern web sites</span></span>

> [!NOTE]
> <span data-ttu-id="bcf58-104">本文適用於 Microsoft Edge Stable 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bcf58-104">This article applies to Microsoft Edge Stable version 87 or later.</span></span>

## <span data-ttu-id="bcf58-105">概觀</span><span class="sxs-lookup"><span data-stu-id="bcf58-105">Overview</span></span>

<span data-ttu-id="bcf58-106">許多新式網站的設計與 Internet Explorer 不相容。</span><span class="sxs-lookup"><span data-stu-id="bcf58-106">Many modern websites have designs that are incompatible with Internet Explorer.</span></span> <span data-ttu-id="bcf58-107">每當 Internet Explorer 使用者造訪不相容的公用網站時，系統會顯示訊息，告訴他們該網站與其瀏覽器不相容，他們需要手動切換到不同的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="bcf58-107">Whenever an Internet Explorer user visits an incompatible public site, they get a message that tells them the site is incompatible with their browser, and they need to manually switch to a different browser.</span></span>

<span data-ttu-id="bcf58-108">需要手動切換到不同的瀏覽器變更是從 Microsoft Edge Stable 版本 87 開始。</span><span class="sxs-lookup"><span data-stu-id="bcf58-108">The need to  manually switch to a different browser changes starting with Microsoft Edge Stable version 87.</span></span>

<span data-ttu-id="bcf58-109">當使用者前往與 Internet Explorer 不相容的網站時，系統會自動將使用者重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="bcf58-109">When a user goes to a site that is incompatible with Internet Explorer, they will be automatically redirected to Microsoft Edge.</span></span> <span data-ttu-id="bcf58-110">本文說明重新導向的使用者體驗，以及用來設定或停用自動重新導向的群組原則。</span><span class="sxs-lookup"><span data-stu-id="bcf58-110">This article describes the user experience for redirection and the group policies that are used to configure or disable automatic redirection.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf58-111">Microsoft 會維護已知與 Internet Explorer 不相容的所有網站清單。</span><span class="sxs-lookup"><span data-stu-id="bcf58-111">Microsoft maintains a list of all sites that are known to be incompatible with Internet Explorer.</span></span>

## <span data-ttu-id="bcf58-112">重新導向體驗</span><span class="sxs-lookup"><span data-stu-id="bcf58-112">Redirection experience</span></span>

<span data-ttu-id="bcf58-113">一旦重新導向至 Microsoft Edge，即會在下一個螢幕擷取畫面中向使用者顯示一次性對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bcf58-113">On redirection to Microsoft Edge, users are shown the one-time dialog in the next screenshot.</span></span> <span data-ttu-id="bcf58-114">此對話方塊會說明什麼將使用者重新導向，並提示使用者同意將瀏覽資料和喜好設定從 Internet Explorer 複製到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="bcf58-114">This dialog explains why they're getting redirected and prompts for consent to copy their browsing data and preferences from Internet Explorer to Microsoft Edge.</span></span> <span data-ttu-id="bcf58-115">將會匯入以下瀏覽資料：我的最愛、密碼、搜尋引擎、開啟的索引標籤、設定、Cookie 和首頁。</span><span class="sxs-lookup"><span data-stu-id="bcf58-115">The following browsing data will be imported: Favorites, Passwords, Search engines, open tabs, History, settings, cookies, and the Home Page.</span></span>

![瀏覽通知和提示以匯入資料和喜好設定。](media/edge-learnmore-neededge/neededge-dialog1.png)

<span data-ttu-id="bcf58-117">即使他們未透過勾選 [永遠從 Internet Explorer 取得我的瀏覽資料和喜好設定] 來表示同意，他們也可以按一下 [繼續瀏覽] \*\*\*\* 以繼續進行其工作階段。</span><span class="sxs-lookup"><span data-stu-id="bcf58-117">Even if they don't give their consent by checking "Always bring over my browsing data and preferences from Internet Explorer", they can click **Continue browsing** to continue their session.</span></span>

<span data-ttu-id="bcf58-118">最後，在下一個螢幕擷取畫面中顯示的網站不相容橫幅，會在每次重新導向時顯示在網址列下方。</span><span class="sxs-lookup"><span data-stu-id="bcf58-118">Finally, a website incompatibility banner, shown in the next screenshot, appears below the address bar for every redirection.</span></span>

![有關新式網站的通知，並提示您將 Microsoft Edge 設定為預設瀏覽器或探索 Microsoft Edge。](media/edge-learnmore-neededge/neededge-banner.png)

<span data-ttu-id="bcf58-120">網站不相容橫幅：</span><span class="sxs-lookup"><span data-stu-id="bcf58-120">The website incompatibility banner:</span></span>

- <span data-ttu-id="bcf58-121">鼓勵使用者切換到 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bcf58-121">encourages the user to switch to Microsoft Edge</span></span>
- <span data-ttu-id="bcf58-122">將 Microsoft Edge 設定為預設瀏覽器的選項</span><span class="sxs-lookup"><span data-stu-id="bcf58-122">offers to make Microsoft Edge as the default browser</span></span>
- <span data-ttu-id="bcf58-123">讓使用者選擇探索 Microsoft Edge 的選項</span><span class="sxs-lookup"><span data-stu-id="bcf58-123">gives the user the option to explore Microsoft Edge</span></span>

<span data-ttu-id="bcf58-124">將網站從 Internet Explorer 重新導向至 Microsoft Edge 時，開始載入網站的 Internet Explorer 索引標籤如果沒有之前的內容，就會關閉。</span><span class="sxs-lookup"><span data-stu-id="bcf58-124">When a site is redirected from Internet Explorer to Microsoft Edge, the Internet Explorer tab that started loading the site is closed if it had no prior content.</span></span> <span data-ttu-id="bcf58-125">否則，使用中的索引標籤檢視會移至 Microsoft  [支援](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) 頁面，在其中會說明為什麼將網站重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="bcf58-125">Otherwise, the active tab view goes to a  Microsoft [support](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) page that explains why the site was redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf58-126">在重新導向之後，使用者可以返回，對不在 Internet Explorer 不相容性清單中的網站使用 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="bcf58-126">After a redirection users can go back to using Internet Explorer for sites that are not on the Internet Explorer incompatibility list.</span></span>  

## <span data-ttu-id="bcf58-127">設定重新導向至 Microsoft Edge 的原則</span><span class="sxs-lookup"><span data-stu-id="bcf58-127">Policies to configure redirection to Microsoft Edge</span></span>

> [!NOTE]
> <span data-ttu-id="bcf58-128">這些原則於 2020 年 10 月 26 日之前，以 ADMX 檔案更新的形式提供，並將於 2020 年 11 月 9 日在 Intune 中提供。</span><span class="sxs-lookup"><span data-stu-id="bcf58-128">These policies will be available as ADMX file updates by October 26, 2020 and will be available in Intune by November 9, 2020.</span></span>

<span data-ttu-id="bcf58-129">必須設定三個群群組原則，才能啟用對 Microsoft Edge 的自動重新導向。</span><span class="sxs-lookup"><span data-stu-id="bcf58-129">Three group policies must be configured to enable automatic redirection to Microsoft Edge.</span></span> <span data-ttu-id="bcf58-130">這些原則如下：</span><span class="sxs-lookup"><span data-stu-id="bcf58-130">These policies are:</span></span>

- <span data-ttu-id="bcf58-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="bcf58-131">RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>
- <span data-ttu-id="bcf58-132">RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="bcf58-132">RedirectSitesFromInternetExplorerRedirectMode</span></span>
- <span data-ttu-id="bcf58-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="bcf58-133">HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

### <span data-ttu-id="bcf58-134">原則：RedirectSitesFromInternetExplorerPreventBHOInstall</span><span class="sxs-lookup"><span data-stu-id="bcf58-134">Policy: RedirectSitesFromInternetExplorerPreventBHOInstall</span></span>

<span data-ttu-id="bcf58-135">從 Internet Explorer 重新導向至 Microsoft Edge 需要一個名為 "IEtoEdge BHO" 的 Internet Explorer 瀏覽器協助程式物件 (BHO)。</span><span class="sxs-lookup"><span data-stu-id="bcf58-135">Redirection from Internet Explorer to Microsoft Edge requires an Internet Explorer Browser Helper Object (BHO) named "IEtoEdge BHO".</span></span> <span data-ttu-id="bcf58-136">**RedirectSitesFromInternetExplorerPreventBHOInstall** 原則會控制是否安裝此 BHO。</span><span class="sxs-lookup"><span data-stu-id="bcf58-136">The **RedirectSitesFromInternetExplorerPreventBHOInstall** policy controls whether or not this BHO is installed.</span></span>  

- <span data-ttu-id="bcf58-137">如果您啟用此原則，將不會安裝重新導向所需的 BHO，且您的使用者將繼續在 Internet Explorer 上看到特定網站的不相容訊息。</span><span class="sxs-lookup"><span data-stu-id="bcf58-137">If you enable this policy, the BHO required for redirection will not be installed and your users will continue to see incompatibility messages for certain websites on Internet Explorer.</span></span> <span data-ttu-id="bcf58-138">如果已安裝 BHO，則會在下一次更新 Microsoft Edge Stable 通道時將它解除安裝。</span><span class="sxs-lookup"><span data-stu-id="bcf58-138">If the BHO is already installed, it will be uninstalled the next time the Microsoft Edge Stable channel is updated.</span></span>
- <span data-ttu-id="bcf58-139">如果您停用或未設定此原則，則會安裝 BHO。</span><span class="sxs-lookup"><span data-stu-id="bcf58-139">If you disable or don't configure this policy, the BHO will be installed.</span></span> <span data-ttu-id="bcf58-140">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="bcf58-140">This is the default behavior.</span></span>

<span data-ttu-id="bcf58-141">除了需要 BHO 之外，還有對 **RedirectSitesFromInternetExplorerRedirectMode** 的相依性，必須將其設定為 "Sitelist" 或「未設定」。</span><span class="sxs-lookup"><span data-stu-id="bcf58-141">In addition to needing the BHO, there is a dependency on the **RedirectSitesFromInternetExplorerRedirectMode**, which needs to be set to "Sitelist" or "Not Configured".</span></span>

### <span data-ttu-id="bcf58-142">原則：RedirectSitesFromInternetExplorerRedirectMode</span><span class="sxs-lookup"><span data-stu-id="bcf58-142">Policy: RedirectSitesFromInternetExplorerRedirectMode</span></span>

 <span data-ttu-id="bcf58-143">此原則對應於 Microsoft Edge 中的 [預設瀏覽器]\*\*\*\* 設定：[在 Microsoft Edge 中以 Internet Explorer 開啟網站]。</span><span class="sxs-lookup"><span data-stu-id="bcf58-143">This policy corresponds to the Microsoft Edge **Default browser** setting "Let Internet Explorer open sites in Microsoft Edge".</span></span> <span data-ttu-id="bcf58-144">您可以移至 *edge://settings/defaultbrowser* URL 來存取此設定。</span><span class="sxs-lookup"><span data-stu-id="bcf58-144">You can access this setting by going to the *edge://settings/defaultbrowser* URL.</span></span>  

- <span data-ttu-id="bcf58-145">如果您未設定此原則或將它設定為 "Sitelist"，Internet Explorer 會將不相容的網站重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="bcf58-145">If you don't configure this policy or set it to "Sitelist", Internet Explorer will redirect incompatible sites to Microsoft Edge.</span></span> <span data-ttu-id="bcf58-146">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="bcf58-146">This is the default behavior.</span></span>
- <span data-ttu-id="bcf58-147">如果您停用此原則，則不會將不相容的網站重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="bcf58-147">If you disable this policy, incompatible sites aren't redirected to Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf58-148">如果您所使用的個人裝置不是由組織管理，則會在 [Internet Explorer 相容性]\*\*\*\* 下看到另一個名為 [允許在 Internet Explorer 模式中載入網站] 的設定。</span><span class="sxs-lookup"><span data-stu-id="bcf58-148">If you're on a personal device that isn't  managed by your organization, you'll see another setting named "Allow sites to be loaded in Internet Explorer mode" under **Internet Explorer compatibility**.</span></span>
>
><span data-ttu-id="bcf58-149">如果您所使用的是加入網域或註冊行動裝置管理 (MDM) 的裝置，就不會看到此選項。</span><span class="sxs-lookup"><span data-stu-id="bcf58-149">If you're on a domain joined or Mobile Device Management (MDM) enrolled device, you won't see this option.</span></span>
>
> <span data-ttu-id="bcf58-150">相反地，如果您想要讓使用者在 Internet Explorer 模式中載入網站，您可以透過設定原則 [允許在 Internet Explorer 模式中重新載入網站][](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing) 來完成。</span><span class="sxs-lookup"><span data-stu-id="bcf58-150">Instead, if you want to let your users load sites in Internet Explorer mode, you can do so by configuring the policy [Allow Internet Explorer mode testing](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing).</span></span>

### <span data-ttu-id="bcf58-151">原則：HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span><span class="sxs-lookup"><span data-stu-id="bcf58-151">Policy: HideInternetExplorerRedirectUXForIncompatibleSitesEnabled</span></span>

<span data-ttu-id="bcf58-152">此原則會設定將不相容網站重新導向至 Microsoft Edge 的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="bcf58-152">This policy configures the user experience for incompatible site redirection to Microsoft Edge.</span></span>  

- <span data-ttu-id="bcf58-153">如果您啟用此原則，使用者就不會看到一次性的重新導向對話方塊和重新導向橫幅。</span><span class="sxs-lookup"><span data-stu-id="bcf58-153">If you enable this policy, users never see the one-time redirection dialog and the redirection banner.</span></span> <span data-ttu-id="bcf58-154">不會匯入任何瀏覽器資料或使用者喜好設定。</span><span class="sxs-lookup"><span data-stu-id="bcf58-154">No browser data or user preferences are imported.</span></span>
- <span data-ttu-id="bcf58-155">如果您停用或不設定此原則，重新導向對話方塊會在第一次重新導向時顯示，並會針對從重新導向開始的工作階段顯示持續性重新導向橫幅。</span><span class="sxs-lookup"><span data-stu-id="bcf58-155">If you disable or don't configure this policy, the redirection dialog will be shown on the first redirection and the persistent redirection banner will be shown for sessions that start with a redirection.</span></span>

  > [!NOTE]
  > <span data-ttu-id="bcf58-156">使用者每次發生新的重新導向時，都會匯入使用者瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="bcf58-156">User browsing data will be imported every time a user encounters a new redirection.</span></span> <span data-ttu-id="bcf58-157">不過，此動作只會在使用者於一次性重新導向對話方塊中同意匯入時才會發生。</span><span class="sxs-lookup"><span data-stu-id="bcf58-157">However, this only happens if the user consented to the import on the one-time redirection dialog.</span></span>

## <span data-ttu-id="bcf58-158">停用重新導向至 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bcf58-158">Disable redirection to Microsoft Edge</span></span>

<span data-ttu-id="bcf58-159">如果您想要在更新至 Microsoft Edge Stable 版本 87「之前」停用重新導向，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="bcf58-159">If you want to disable redirection BEFORE updating to Microsoft Edge Stable version 87, use the following step:</span></span>

1. <span data-ttu-id="bcf58-160">將 **RedirectSitesFromInternetExplorerRedirectMode** 原則設定為 [已啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bcf58-160">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Enabled**.</span></span> <span data-ttu-id="bcf58-161">原則生效後，此設定就會停止重新導向。</span><span class="sxs-lookup"><span data-stu-id="bcf58-161">This setting will stop redirecting as soon as the policy takes effect.</span></span>

<span data-ttu-id="bcf58-162">如果您想要在更新至 Microsoft Edge Stable 版本 87「之後」停用重新導向，請使用下列步驟：</span><span class="sxs-lookup"><span data-stu-id="bcf58-162">If you want to disable redirection AFTER updating to Microsoft Edge Stable version 87, use the following steps:</span></span>

1. <span data-ttu-id="bcf58-163">將 **RedirectSitesFromInternetExplorerRedirectMode** 原則設定為 [已停用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bcf58-163">Set the **RedirectSitesFromInternetExplorerRedirectMode** policy to **Disabled**.</span></span> <span data-ttu-id="bcf58-164">原則生效後，此設定就會停止重新導向。</span><span class="sxs-lookup"><span data-stu-id="bcf58-164">This setting will stop redirecting as soon as the policy takes effect.</span></span>
2. <span data-ttu-id="bcf58-165">將 **RedirectSitesFromInternetExplorerPreventBHOInstall** 原則設定為 [已啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="bcf58-165">Set the **RedirectSitesFromInternetExplorerPreventBHOInstall** policy to **Enabled**.</span></span> <span data-ttu-id="bcf58-166">這會在下一次 Microsoft Edge 更新之後解除安裝 BHO。</span><span class="sxs-lookup"><span data-stu-id="bcf58-166">This will uninstall the BHO after the next Microsoft Edge update.</span></span>

## <span data-ttu-id="bcf58-167">請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf58-167">See also</span></span>

- [<span data-ttu-id="bcf58-168">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="bcf58-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="bcf58-169">Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="bcf58-169">Microsoft Edge Policies</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies)