---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Kiosk 模式功能，以及如何設定 Microsoft Edge Kiosk 模式選項。
ms.openlocfilehash: 9f2ce26f2c505ba3fc9e2e05b057e5d5df8257fe
ms.sourcegitcommit: 8da3a4de1a14514014b6d7b103ba79f2ace48044
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "11388551"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a><span data-ttu-id="b5b03-103">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="b5b03-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="b5b03-104">本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="b5b03-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="b5b03-105">另提供一份我們鎖定之功能的藍圖。</span><span class="sxs-lookup"><span data-stu-id="b5b03-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="b5b03-106">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="b5b03-107">概觀</span><span class="sxs-lookup"><span data-stu-id="b5b03-107">Overview</span></span>

<span data-ttu-id="b5b03-108">Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="b5b03-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="b5b03-109">可使用的鎖定體驗如下：</span><span class="sxs-lookup"><span data-stu-id="b5b03-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="b5b03-110">**數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="b5b03-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="b5b03-111">**公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="b5b03-112">兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="b5b03-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <a name="set-up-microsoft-edge-kiosk-mode"></a><span data-ttu-id="b5b03-113">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="b5b03-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="b5b03-114">使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="b5b03-115">您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <a name="kiosk-mode-supported-features"></a><span data-ttu-id="b5b03-116">kiosk 模式支援的功能</span><span class="sxs-lookup"><span data-stu-id="b5b03-116">Kiosk mode supported features</span></span>

<span data-ttu-id="b5b03-117">下表列出 Microsoft Edge 與舊版 Microsoft Edge 中的 kiosk 模式所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-117">The following table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy.</span></span> <span data-ttu-id="b5b03-118">使用此表格做為轉換至 Microsoft Edge 的指南，方法是比較在這兩個版本的 Microsoft Edge 中支援這些功能的情況。</span><span class="sxs-lookup"><span data-stu-id="b5b03-118">Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both versions of Microsoft Edge.</span></span>

|<span data-ttu-id="b5b03-119">功能</span><span class="sxs-lookup"><span data-stu-id="b5b03-119">Feature</span></span>|<span data-ttu-id="b5b03-120">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="b5b03-120">Digital\Interactive Signage</span></span>|<span data-ttu-id="b5b03-121">公用瀏覽</span><span class="sxs-lookup"><span data-stu-id="b5b03-121">Public browsing</span></span>|<span data-ttu-id="b5b03-122">隨 Microsoft Edge 版本 (及更新版本) 提供</span><span class="sxs-lookup"><span data-stu-id="b5b03-122">Available with Microsoft Edge version (and higher)</span></span>|<span data-ttu-id="b5b03-123">隨舊版 Microsoft Edge 提供</span><span class="sxs-lookup"><span data-stu-id="b5b03-123">Available with Microsoft Edge Legacy</span></span>|
|-|-|-|-|-|
|<span data-ttu-id="b5b03-124">InPrivate 瀏覽</span><span class="sxs-lookup"><span data-stu-id="b5b03-124">InPrivate Navigation</span></span>|<span data-ttu-id="b5b03-125">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-125">Y</span></span>|<span data-ttu-id="b5b03-126">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-126">Y</span></span>|<span data-ttu-id="b5b03-127">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-127">89</span></span>|<span data-ttu-id="b5b03-128">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-128">Y</span></span>|
|<span data-ttu-id="b5b03-129">在非使用狀態時重設</span><span class="sxs-lookup"><span data-stu-id="b5b03-129">Reset on inactivity</span></span>|<span data-ttu-id="b5b03-130">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-130">Y</span></span>|<span data-ttu-id="b5b03-131">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-131">Y</span></span>|<span data-ttu-id="b5b03-132">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-132">89</span></span>|<span data-ttu-id="b5b03-133">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-133">Y</span></span>|
|<span data-ttu-id="b5b03-134">[唯讀網址列](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-134">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="b5b03-135">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-135">N</span></span>|<span data-ttu-id="b5b03-136">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-136">Y</span></span> |<span data-ttu-id="b5b03-137">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-137">89</span></span>|<span data-ttu-id="b5b03-138">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-138">N</span></span>|
|<span data-ttu-id="b5b03-139">[結束時刪除下載](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-139">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="b5b03-140">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-140">Y</span></span>|<span data-ttu-id="b5b03-141">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-141">Y</span></span> |<span data-ttu-id="b5b03-142">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-142">89</span></span>|<span data-ttu-id="b5b03-143">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-143">N</span></span>|
|<span data-ttu-id="b5b03-144">F11 已封鎖 (進入/結束全螢幕)</span><span class="sxs-lookup"><span data-stu-id="b5b03-144">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="b5b03-145">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-145">Y</span></span> | <span data-ttu-id="b5b03-146">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-146">Y</span></span> | <span data-ttu-id="b5b03-147">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-147">89</span></span> |<span data-ttu-id="b5b03-148">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-148">Y</span></span>|
|<span data-ttu-id="b5b03-149">F12 已封鎖 (啟動開發人員工具)</span><span class="sxs-lookup"><span data-stu-id="b5b03-149">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="b5b03-150">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-150">Y</span></span> | <span data-ttu-id="b5b03-151">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-151">Y</span></span> | <span data-ttu-id="b5b03-152">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-152">89</span></span> |<span data-ttu-id="b5b03-153">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-153">Y</span></span>|
| <span data-ttu-id="b5b03-154">支援多個索引標籤</span><span class="sxs-lookup"><span data-stu-id="b5b03-154">Multi tab support</span></span> | <span data-ttu-id="b5b03-155">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-155">N</span></span>| <span data-ttu-id="b5b03-156">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-156">Y</span></span>| <span data-ttu-id="b5b03-157">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-157">89</span></span>|<span data-ttu-id="b5b03-158">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-158">Y</span></span>|
|<span data-ttu-id="b5b03-159">[允許 URL 支援](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-159">[Allow URL support](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (policy)</span></span>|<span data-ttu-id="b5b03-160">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-160">Y</span></span>|<span data-ttu-id="b5b03-161">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-161">Y</span></span>|<span data-ttu-id="b5b03-162">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-162">89</span></span>|<span data-ttu-id="b5b03-163">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-163">N</span></span>|
|<span data-ttu-id="b5b03-164">[封鎖 URL 支援](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-164">[Block URL support](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (policy)</span></span>|<span data-ttu-id="b5b03-165">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-165">Y</span></span>|<span data-ttu-id="b5b03-166">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-166">Y</span></span>|<span data-ttu-id="b5b03-167">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-167">89</span></span>|<span data-ttu-id="b5b03-168">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-168">N</span></span>|
|<span data-ttu-id="b5b03-169">[顯示首頁按鈕](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-169">[Show home button](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (policy)</span></span>|<span data-ttu-id="b5b03-170">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-170">N</span></span>|<span data-ttu-id="b5b03-171">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-171">Y</span></span>|<span data-ttu-id="b5b03-172">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-172">89</span></span>|<span data-ttu-id="b5b03-173">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-173">Y</span></span>|
|<span data-ttu-id="b5b03-174">[管理我的最愛](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-174">[Manage favorites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (policy)</span></span>|<span data-ttu-id="b5b03-175">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-175">N</span></span>|<span data-ttu-id="b5b03-176">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-176">Y</span></span>|<span data-ttu-id="b5b03-177">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-177">89</span></span>|<span data-ttu-id="b5b03-178">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-178">Y</span></span>|
|<span data-ttu-id="b5b03-179">[啟用印表機](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-179">[Enable printer](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (policy)</span></span>|<span data-ttu-id="b5b03-180">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-180">Y</span></span>|<span data-ttu-id="b5b03-181">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-181">Y</span></span>|<span data-ttu-id="b5b03-182">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-182">89</span></span>|<span data-ttu-id="b5b03-183">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-183">Y</span></span>|
|<span data-ttu-id="b5b03-184">[設定新的索引標籤頁面 URL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-184">[Configure the new tab page URL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (policy)</span></span>|<span data-ttu-id="b5b03-185">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-185">N</span></span>|<span data-ttu-id="b5b03-186">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-186">Y</span></span>||<span data-ttu-id="b5b03-187">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-187">Y</span></span>|
|<span data-ttu-id="b5b03-188">結束會話按鈕 \*</span><span class="sxs-lookup"><span data-stu-id="b5b03-188">End session button \*</span></span> | <span data-ttu-id="b5b03-189">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-189">N</span></span>| <span data-ttu-id="b5b03-190">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-190">Y</span></span>| <span data-ttu-id="b5b03-191">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-191">89</span></span>|<span data-ttu-id="b5b03-192">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-192">Y</span></span>|
|<span data-ttu-id="b5b03-193">所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外</span><span class="sxs-lookup"><span data-stu-id="b5b03-193">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="b5b03-194">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-194">N</span></span>|<span data-ttu-id="b5b03-195">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-195">Y</span></span>|<span data-ttu-id="b5b03-196">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-196">89</span></span>|<span data-ttu-id="b5b03-197">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-197">Y</span></span>|
| <span data-ttu-id="b5b03-198">CTRL+N 封鎖 (開啟新的視窗 #) \*</span><span class="sxs-lookup"><span data-stu-id="b5b03-198">CTRL+N blocked (open a new window) \*</span></span> | <span data-ttu-id="b5b03-199">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-199">Y</span></span> | <span data-ttu-id="b5b03-200">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-200">Y</span></span> | <span data-ttu-id="b5b03-201">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-201">89</span></span> |<span data-ttu-id="b5b03-202">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-202">Y</span></span>|
| <span data-ttu-id="b5b03-203">CTRL+T 已封鎖 (開啟新索引標籤)</span><span class="sxs-lookup"><span data-stu-id="b5b03-203">CTRL+T blocked (open new tab)</span></span> |<span data-ttu-id="b5b03-204">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-204">Y</span></span> | <span data-ttu-id="b5b03-205">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-205">N</span></span> | <span data-ttu-id="b5b03-206">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-206">89</span></span> |<span data-ttu-id="b5b03-207">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-207">Y</span></span>|
|<span data-ttu-id="b5b03-208">設定及其他 (...) 將只顯示必要的選項</span><span class="sxs-lookup"><span data-stu-id="b5b03-208">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="b5b03-209">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-209">Y</span></span> |<span data-ttu-id="b5b03-210">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-210">Y</span></span> |<span data-ttu-id="b5b03-211">89</span><span class="sxs-lookup"><span data-stu-id="b5b03-211">89</span></span> |<span data-ttu-id="b5b03-212">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-212">Y</span></span>|
|<span data-ttu-id="b5b03-213">限制從瀏覽器啟動其他應用程式</span><span class="sxs-lookup"><span data-stu-id="b5b03-213">Restrict the launch of other applications from the browser</span></span>|<span data-ttu-id="b5b03-214">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-214">Y</span></span>|<span data-ttu-id="b5b03-215">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-215">Y</span></span>|<span data-ttu-id="b5b03-216">90/91</span><span class="sxs-lookup"><span data-stu-id="b5b03-216">90/91</span></span>|<span data-ttu-id="b5b03-217">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-217">Y</span></span>|
|<span data-ttu-id="b5b03-218">UI 列印設定鎖定</span><span class="sxs-lookup"><span data-stu-id="b5b03-218">UI print settings lockdown</span></span>|<span data-ttu-id="b5b03-219">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-219">Y</span></span>|<span data-ttu-id="b5b03-220">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-220">Y</span></span>|<span data-ttu-id="b5b03-221">90/91</span><span class="sxs-lookup"><span data-stu-id="b5b03-221">90/91</span></span>|<span data-ttu-id="b5b03-222">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-222">Y</span></span>|
|<span data-ttu-id="b5b03-223">[將新的索引標籤頁面設定為首頁](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (原則)</span><span class="sxs-lookup"><span data-stu-id="b5b03-223">[Set the new tab page as the home page](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (policy)</span></span>|-|-|<span data-ttu-id="b5b03-224">待決定</span><span class="sxs-lookup"><span data-stu-id="b5b03-224">TBD</span></span>|<span data-ttu-id="b5b03-225">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-225">Y</span></span>|

> [!NOTE]
> <span data-ttu-id="b5b03-226">只有在指派的存取單一應用程式情況下，才能啟用後面接著 "\*" 的功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-226">Features followed by "\*" are only enabled in an assigned access single app scenario.</span></span>

## <a name="use-kiosk-mode-features"></a><span data-ttu-id="b5b03-227">使用 kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="b5b03-227">Use kiosk mode features</span></span>

<span data-ttu-id="b5b03-228">針對數位/互動式告示板和公開瀏覽使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-228">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options for Digital/Interactive signage and Public browsing.</span></span>

### <a name="kiosk-mode-digitalinteractive-signage"></a><span data-ttu-id="b5b03-229">kiosk 模式數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="b5b03-229">Kiosk mode Digital/Interactive signage</span></span>
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a><span data-ttu-id="b5b03-230">kiosk 模式公用瀏覽：</span><span class="sxs-lookup"><span data-stu-id="b5b03-230">Kiosk mode Public browsing</span></span>

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a><span data-ttu-id="b5b03-231">其他命令列選項</span><span class="sxs-lookup"><span data-stu-id="b5b03-231">Additional command line options</span></span>

- <span data-ttu-id="b5b03-232">**--no-first-run**：停用 Microsoft Edge 初次執行體驗。</span><span class="sxs-lookup"><span data-stu-id="b5b03-232">**--no-first-run**: Disable the first Microsoft Edge run experience.</span></span>

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- <span data-ttu-id="b5b03-233">**--kiosk-idle-timeout-minutes=**：變更從上次使用者活動經過的時間 (以分鐘為單位)，在此時間後，Microsoft Edge kiosk 模式便重設使用者的工作階段。</span><span class="sxs-lookup"><span data-stu-id="b5b03-233">**--kiosk-idle-timeout-minutes=**: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="b5b03-234">將以下範例中的「值」以分鐘數取代。</span><span class="sxs-lookup"><span data-stu-id="b5b03-234">Replace "value" in the next example with the number of minutes.</span></span>

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   <span data-ttu-id="b5b03-235">下列是支援的「值」：</span><span class="sxs-lookup"><span data-stu-id="b5b03-235">The following "values" are supported:</span></span>

     - <span data-ttu-id="b5b03-236">預設值 (以分鐘為單位)</span><span class="sxs-lookup"><span data-stu-id="b5b03-236">Default values (in minutes)</span></span>
       - <span data-ttu-id="b5b03-237">全螢幕 - 0 (關閉)</span><span class="sxs-lookup"><span data-stu-id="b5b03-237">Full screen - 0 (turned off)</span></span>
       - <span data-ttu-id="b5b03-238">公用瀏覽 - 5 分鐘</span><span class="sxs-lookup"><span data-stu-id="b5b03-238">Public browsing - 5 minutes</span></span>
    - <span data-ttu-id="b5b03-239">允許的值</span><span class="sxs-lookup"><span data-stu-id="b5b03-239">Allowed values</span></span>
      - <span data-ttu-id="b5b03-240">0 - 關閉計時器</span><span class="sxs-lookup"><span data-stu-id="b5b03-240">0 - turns off the timer</span></span>
      - <span data-ttu-id="b5b03-241">1-1440 分鐘，用於重設閒置時計時器</span><span class="sxs-lookup"><span data-stu-id="b5b03-241">1-1440 minutes for reset on idle timer</span></span>


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a><span data-ttu-id="b5b03-242">支援 kiosk 模式的原則</span><span class="sxs-lookup"><span data-stu-id="b5b03-242">Support policies for kiosk mode</span></span>

<span data-ttu-id="b5b03-243">使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。</span><span class="sxs-lookup"><span data-stu-id="b5b03-243">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="b5b03-244">若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](https://docs.microsoft.com/deployedge/microsoft-edge-policies)。</span><span class="sxs-lookup"><span data-stu-id="b5b03-244">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="b5b03-245">原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="b5b03-245">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="b5b03-246">群組原則</span><span class="sxs-lookup"><span data-stu-id="b5b03-246">Group policy</span></span>|<span data-ttu-id="b5b03-247">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="b5b03-247">Digital\Interactive signage</span></span>|<span data-ttu-id="b5b03-248">公用瀏覽單一應用程式</span><span class="sxs-lookup"><span data-stu-id="b5b03-248">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="b5b03-249">列印</span><span class="sxs-lookup"><span data-stu-id="b5b03-249">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="b5b03-250">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-250">Y</span></span>|<span data-ttu-id="b5b03-251">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-251">Y</span></span> |
|[<span data-ttu-id="b5b03-252">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="b5b03-252">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="b5b03-253">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-253">N</span></span> | <span data-ttu-id="b5b03-254">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-254">Y</span></span>|
|[<span data-ttu-id="b5b03-255">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="b5b03-255">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="b5b03-256">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-256">N</span></span> | <span data-ttu-id="b5b03-257">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-257">Y</span></span>|
|[<span data-ttu-id="b5b03-258">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="b5b03-258">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="b5b03-259">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-259">N</span></span> |<span data-ttu-id="b5b03-260">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-260">Y</span></span> |
|[<span data-ttu-id="b5b03-261">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-261">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="b5b03-262">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-262">N</span></span> |<span data-ttu-id="b5b03-263">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-263">Y</span></span> |
|[<span data-ttu-id="b5b03-264">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="b5b03-264">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="b5b03-265">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-265">Y</span></span> |<span data-ttu-id="b5b03-266">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-266">Y</span></span> |
|[<span data-ttu-id="b5b03-267">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="b5b03-267">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="b5b03-268">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-268">Y</span></span> | <span data-ttu-id="b5b03-269">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-269">Y</span></span>|
|[<span data-ttu-id="b5b03-270">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="b5b03-270">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="b5b03-271">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-271">N</span></span> | <span data-ttu-id="b5b03-272">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-272">Y</span></span>|
|[<span data-ttu-id="b5b03-273">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="b5b03-273">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="b5b03-274">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-274">N</span></span> | <span data-ttu-id="b5b03-275">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-275">Y</span></span>|
|[<span data-ttu-id="b5b03-276">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="b5b03-276">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="b5b03-277">否</span><span class="sxs-lookup"><span data-stu-id="b5b03-277">N</span></span>|<span data-ttu-id="b5b03-278">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-278">Y</span></span> |
|[<span data-ttu-id="b5b03-279">SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="b5b03-279">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="b5b03-280">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-280">Y</span></span> |<span data-ttu-id="b5b03-281">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-281">Y</span></span> |
|[<span data-ttu-id="b5b03-282">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-282">EdgeCollectionsEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)|<span data-ttu-id="b5b03-283">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-283">Y</span></span>|<span data-ttu-id="b5b03-284">是</span><span class="sxs-lookup"><span data-stu-id="b5b03-284">Y</span></span>|

## <a name="microsoft-edge-with-assigned-access"></a><span data-ttu-id="b5b03-285">具有受指派存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b5b03-285">Microsoft Edge with assigned access</span></span>

### <a name="single-app-kiosk"></a><span data-ttu-id="b5b03-286">單一應用程式 kiosk</span><span class="sxs-lookup"><span data-stu-id="b5b03-286">Single app kiosk</span></span>

<span data-ttu-id="b5b03-287">Microsoft Edge 目前針對單一應用程式受指派的存取權支援一組相同的舊版 Microsoft Edge kiosk 模式類型，包含下列鎖定體驗：數位/互動式告示板和公用瀏覽。</span><span class="sxs-lookup"><span data-stu-id="b5b03-287">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="b5b03-288">您目前可使用最新的  [Windows 10 測試人員預覽版](https://insider.windows.com/)版本 20215 或更新版本，以及  [Microsoft Edge Beta 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本，測試具有受指派存取權單一應用程式的 Microsoft Edge kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="b5b03-288">Microsoft Edge kiosk mode with assigned access single app is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

**<span data-ttu-id="b5b03-289">如何取得 Windows 測試人員預覽？</span><span class="sxs-lookup"><span data-stu-id="b5b03-289">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="b5b03-290">若要在電腦上安裝 Windows 10 測試人員預覽版，請依照 [開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="b5b03-290">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <a name="multi-app-kiosk"></a><span data-ttu-id="b5b03-291">多個應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="b5b03-291">Multi-app kiosk</span></span>

<span data-ttu-id="b5b03-292">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="b5b03-292">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="b5b03-293">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="b5b03-293">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="b5b03-294">(Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。</span><span class="sxs-lookup"><span data-stu-id="b5b03-294">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="b5b03-295">使用具有受指派的存取權的 Microsoft Edge 時，您可以設定 Microsoft Edge kiosk 模式，以使用 [Microsoft Edge 瀏覽器原則](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies)來設定瀏覽體驗，進而滿足您的獨特需求。</span><span class="sxs-lookup"><span data-stu-id="b5b03-295">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <a name="configure-using-windows-settings"></a><span data-ttu-id="b5b03-296">使用 Windows 設定進行設定</span><span class="sxs-lookup"><span data-stu-id="b5b03-296">Configure using Windows Settings</span></span>

<span data-ttu-id="b5b03-297">Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="b5b03-297">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="b5b03-298">使用下列步驟設定單一應用程式 kiosk 電腦。</span><span class="sxs-lookup"><span data-stu-id="b5b03-298">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="b5b03-299">安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-299">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="b5b03-300">依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="b5b03-300">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="b5b03-301">若要測試最新功能，您可以下載最新的 [Microsoft Edge Beta 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-301">To test the latest features, you can download the latest [Microsoft Edge Beta channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>
3. <span data-ttu-id="b5b03-302">在 kiosk 電腦上，開啟 Windows [設定]，然後在搜尋欄位中輸入 "kiosk"。</span><span class="sxs-lookup"><span data-stu-id="b5b03-302">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="b5b03-303">如下一個螢幕擷取畫面所示，選取 \*\* \*\*[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b5b03-303">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. <span data-ttu-id="b5b03-305">在 \*\* ** [設定 kiosk] 頁面上，按一下 ** \*\*[開始使用]。</span><span class="sxs-lookup"><span data-stu-id="b5b03-305">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. <span data-ttu-id="b5b03-307">輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="b5b03-307">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. <span data-ttu-id="b5b03-309">在\*\* ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="b5b03-309">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="b5b03-310">這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="b5b03-310">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk 模式 - 選擇應用程式":::

7. <span data-ttu-id="b5b03-312">針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="b5b03-312">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="b5b03-313">數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="b5b03-313">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="b5b03-314">公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="b5b03-314">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

8. <span data-ttu-id="b5b03-316">選取 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="b5b03-316">Select **Next**.</span></span>
9. <span data-ttu-id="b5b03-317">輸入 kiosk 啟動時要載入的 URL。</span><span class="sxs-lookup"><span data-stu-id="b5b03-317">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. <span data-ttu-id="b5b03-319">接受 5 分鐘的閒置時間預設值，或提供您自己的值。</span><span class="sxs-lookup"><span data-stu-id="b5b03-319">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. <span data-ttu-id="b5b03-321">按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="b5b03-321">Click **Next**.</span></span>
12. <span data-ttu-id="b5b03-322">關閉 \*\* \*\* [設定] 視窗，儲存並套用您的選擇。</span><span class="sxs-lookup"><span data-stu-id="b5b03-322">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. <span data-ttu-id="b5b03-324">從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。</span><span class="sxs-lookup"><span data-stu-id="b5b03-324">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <a name="functional-limitations"></a><span data-ttu-id="b5b03-325">功能限制</span><span class="sxs-lookup"><span data-stu-id="b5b03-325">Functional limitations</span></span>

<span data-ttu-id="b5b03-326">隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-326">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="b5b03-327">建議您關閉：</span><span class="sxs-lookup"><span data-stu-id="b5b03-327">We recommend that you turn off:</span></span>

- [<span data-ttu-id="b5b03-328">InPrivateModeAvailability</span><span class="sxs-lookup"><span data-stu-id="b5b03-328">InPrivateModeAvailability</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#inprivatemodeavailability)
- [<span data-ttu-id="b5b03-329">IsolateOrigins</span><span class="sxs-lookup"><span data-stu-id="b5b03-329">IsolateOrigins</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#isolateorigins)
- [<span data-ttu-id="b5b03-330">ManagedFavorites</span><span class="sxs-lookup"><span data-stu-id="b5b03-330">ManagedFavorites</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedfavorites)
- [<span data-ttu-id="b5b03-331">EdgeShoppingAssistantEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-331">EdgeShoppingAssistantEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgeshoppingassistantenabled)
- [<span data-ttu-id="b5b03-332">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-332">EdgeCollectionsEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#edgecollectionsenabled)
- [<span data-ttu-id="b5b03-333">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="b5b03-333">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed)
- [<span data-ttu-id="b5b03-334">DefaultPopupsSetting</span><span class="sxs-lookup"><span data-stu-id="b5b03-334">DefaultPopupsSetting</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#defaultpopupssetting)
- [<span data-ttu-id="b5b03-335">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-335">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="b5b03-336">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="b5b03-336">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="b5b03-337">Extensions</span><span class="sxs-lookup"><span data-stu-id="b5b03-337">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="b5b03-338">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="b5b03-338">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <a name="roadmap"></a><span data-ttu-id="b5b03-339">藍圖</span><span class="sxs-lookup"><span data-stu-id="b5b03-339">Roadmap</span></span>

### <a name="in-early-2021"></a><span data-ttu-id="b5b03-340">2021 年年初</span><span class="sxs-lookup"><span data-stu-id="b5b03-340">In early 2021</span></span>

<span data-ttu-id="b5b03-341">我們將增加下列支援和功能：</span><span class="sxs-lookup"><span data-stu-id="b5b03-341">We'll add the following support and features:</span></span>

- <span data-ttu-id="b5b03-342">在 Windows 10 1909 和更新版本上，具有獲指派存取權單一應用程式之 Microsoft Edge kiosk 模式的正式發行。</span><span class="sxs-lookup"><span data-stu-id="b5b03-342">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="b5b03-343">與舊版 Microsoft Edge 同等的其他功能。</span><span class="sxs-lookup"><span data-stu-id="b5b03-343">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="b5b03-344">與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b5b03-344">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="b5b03-345">限制從瀏覽器啟動其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="b5b03-345">Restrict the launch of other applications from the browser.</span></span>
- <span data-ttu-id="b5b03-346">UI 列印設定鎖定。</span><span class="sxs-lookup"><span data-stu-id="b5b03-346">UI print settings lockdown.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5b03-347">請參閱</span><span class="sxs-lookup"><span data-stu-id="b5b03-347">See also</span></span>

- [<span data-ttu-id="b5b03-348">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="b5b03-348">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="b5b03-349">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="b5b03-349">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="b5b03-350">設定 Windows 桌面版的 kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="b5b03-350">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="b5b03-351">規劃 kiosk 模式轉換</span><span class="sxs-lookup"><span data-stu-id="b5b03-351">Plan your kiosk mode transition</span></span>](microsoft-edge-kiosk-mode-transition-plan.md)
