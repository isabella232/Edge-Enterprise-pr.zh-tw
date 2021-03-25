---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 03/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Kiosk 模式功能，以及如何設定 Microsoft Edge Kiosk 模式選項。
ms.openlocfilehash: 9d76bfcaebeaf56e627a401cc4f0375bce9d17a3
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448127"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a><span data-ttu-id="9e59a-103">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="9e59a-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="9e59a-104">本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="9e59a-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="9e59a-105">另提供一份我們鎖定之功能的藍圖。</span><span class="sxs-lookup"><span data-stu-id="9e59a-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="9e59a-106">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-106">This article applies to Microsoft Edge version 87 or later.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e59a-107">使用[使用 kiosk 模式功能](#use-kiosk-mode-features)中的命令列引數，叫用 Windows 10 上的 Microsoft Edge kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-107">Invoke Microsoft Edge kiosk mode features on Windows 10 using the command line arguments provided in [Use kiosk mode features](#use-kiosk-mode-features).</span></span>

## <a name="overview"></a><span data-ttu-id="9e59a-108">概觀</span><span class="sxs-lookup"><span data-stu-id="9e59a-108">Overview</span></span>

<span data-ttu-id="9e59a-109">Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="9e59a-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="9e59a-110">可使用的鎖定體驗如下：</span><span class="sxs-lookup"><span data-stu-id="9e59a-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="9e59a-111">**數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="9e59a-111">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="9e59a-112">**公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-112">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="9e59a-113">兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="9e59a-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <a name="set-up-microsoft-edge-kiosk-mode"></a><span data-ttu-id="9e59a-114">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="9e59a-114">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="9e59a-115">使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-115">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="9e59a-116">您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-116">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <a name="kiosk-mode-supported-features"></a><span data-ttu-id="9e59a-117">kiosk 模式支援的功能</span><span class="sxs-lookup"><span data-stu-id="9e59a-117">Kiosk mode supported features</span></span>

<span data-ttu-id="9e59a-118">下表列出 Microsoft Edge 與舊版 Microsoft Edge 中的 kiosk 模式所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-118">The following table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy.</span></span> <span data-ttu-id="9e59a-119">使用此表格做為轉換至 Microsoft Edge 的指南，方法是比較在這兩個版本的 Microsoft Edge 中支援這些功能的情況。</span><span class="sxs-lookup"><span data-stu-id="9e59a-119">Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both versions of Microsoft Edge.</span></span>

|<span data-ttu-id="9e59a-120">功能</span><span class="sxs-lookup"><span data-stu-id="9e59a-120">Feature</span></span>|<span data-ttu-id="9e59a-121">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="9e59a-121">Digital\Interactive Signage</span></span>|<span data-ttu-id="9e59a-122">公用瀏覽</span><span class="sxs-lookup"><span data-stu-id="9e59a-122">Public browsing</span></span>|<span data-ttu-id="9e59a-123">隨 Microsoft Edge 版本 (及更新版本) 提供</span><span class="sxs-lookup"><span data-stu-id="9e59a-123">Available with Microsoft Edge version (and higher)</span></span>|<span data-ttu-id="9e59a-124">隨舊版 Microsoft Edge 提供</span><span class="sxs-lookup"><span data-stu-id="9e59a-124">Available with Microsoft Edge Legacy</span></span>|
|-|-|-|-|-|
|<span data-ttu-id="9e59a-125">InPrivate 瀏覽</span><span class="sxs-lookup"><span data-stu-id="9e59a-125">InPrivate Navigation</span></span>|<span data-ttu-id="9e59a-126">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-126">Y</span></span>|<span data-ttu-id="9e59a-127">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-127">Y</span></span>|<span data-ttu-id="9e59a-128">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-128">89</span></span>|<span data-ttu-id="9e59a-129">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-129">Y</span></span>|
|<span data-ttu-id="9e59a-130">在非使用狀態時重設</span><span class="sxs-lookup"><span data-stu-id="9e59a-130">Reset on inactivity</span></span>|<span data-ttu-id="9e59a-131">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-131">Y</span></span>|<span data-ttu-id="9e59a-132">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-132">Y</span></span>|<span data-ttu-id="9e59a-133">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-133">89</span></span>|<span data-ttu-id="9e59a-134">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-134">Y</span></span>|
|<span data-ttu-id="9e59a-135">[唯讀網址列](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-135">[Read only address bar](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="9e59a-136">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-136">N</span></span>|<span data-ttu-id="9e59a-137">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-137">Y</span></span> |<span data-ttu-id="9e59a-138">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-138">89</span></span>|<span data-ttu-id="9e59a-139">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-139">N</span></span>|
|<span data-ttu-id="9e59a-140">[結束時刪除下載](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-140">[Delete downloads on exit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="9e59a-141">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-141">Y</span></span>|<span data-ttu-id="9e59a-142">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-142">Y</span></span> |<span data-ttu-id="9e59a-143">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-143">89</span></span>|<span data-ttu-id="9e59a-144">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-144">N</span></span>|
|<span data-ttu-id="9e59a-145">F11 已封鎖 (進入/結束全螢幕)</span><span class="sxs-lookup"><span data-stu-id="9e59a-145">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="9e59a-146">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-146">Y</span></span> | <span data-ttu-id="9e59a-147">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-147">Y</span></span> | <span data-ttu-id="9e59a-148">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-148">89</span></span> |<span data-ttu-id="9e59a-149">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-149">Y</span></span>|
|<span data-ttu-id="9e59a-150">F12 已封鎖 (啟動開發人員工具)</span><span class="sxs-lookup"><span data-stu-id="9e59a-150">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="9e59a-151">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-151">Y</span></span> | <span data-ttu-id="9e59a-152">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-152">Y</span></span> | <span data-ttu-id="9e59a-153">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-153">89</span></span> |<span data-ttu-id="9e59a-154">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-154">Y</span></span>|
| <span data-ttu-id="9e59a-155">支援多個索引標籤</span><span class="sxs-lookup"><span data-stu-id="9e59a-155">Multi tab support</span></span> | <span data-ttu-id="9e59a-156">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-156">N</span></span>| <span data-ttu-id="9e59a-157">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-157">Y</span></span>| <span data-ttu-id="9e59a-158">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-158">89</span></span>|<span data-ttu-id="9e59a-159">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-159">Y</span></span>|
|<span data-ttu-id="9e59a-160">[允許 URL 支援](./microsoft-edge-policies.md#urlallowlist) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-160">[Allow URL support](./microsoft-edge-policies.md#urlallowlist) (policy)</span></span>|<span data-ttu-id="9e59a-161">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-161">Y</span></span>|<span data-ttu-id="9e59a-162">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-162">Y</span></span>|<span data-ttu-id="9e59a-163">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-163">89</span></span>|<span data-ttu-id="9e59a-164">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-164">N</span></span>|
|<span data-ttu-id="9e59a-165">[封鎖 URL 支援](./microsoft-edge-policies.md#urlblocklist) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-165">[Block URL support](./microsoft-edge-policies.md#urlblocklist) (policy)</span></span>|<span data-ttu-id="9e59a-166">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-166">Y</span></span>|<span data-ttu-id="9e59a-167">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-167">Y</span></span>|<span data-ttu-id="9e59a-168">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-168">89</span></span>|<span data-ttu-id="9e59a-169">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-169">N</span></span>|
|<span data-ttu-id="9e59a-170">[顯示首頁按鈕](./microsoft-edge-policies.md#showhomebutton) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-170">[Show home button](./microsoft-edge-policies.md#showhomebutton) (policy)</span></span>|<span data-ttu-id="9e59a-171">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-171">N</span></span>|<span data-ttu-id="9e59a-172">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-172">Y</span></span>|<span data-ttu-id="9e59a-173">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-173">89</span></span>|<span data-ttu-id="9e59a-174">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-174">Y</span></span>|
|<span data-ttu-id="9e59a-175">[管理我的最愛](./microsoft-edge-policies.md#managedfavorites) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-175">[Manage favorites](./microsoft-edge-policies.md#managedfavorites) (policy)</span></span>|<span data-ttu-id="9e59a-176">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-176">N</span></span>|<span data-ttu-id="9e59a-177">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-177">Y</span></span>|<span data-ttu-id="9e59a-178">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-178">89</span></span>|<span data-ttu-id="9e59a-179">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-179">Y</span></span>|
|<span data-ttu-id="9e59a-180">[啟用印表機](./microsoft-edge-policies.md#printingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-180">[Enable printer](./microsoft-edge-policies.md#printingenabled) (policy)</span></span>|<span data-ttu-id="9e59a-181">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-181">Y</span></span>|<span data-ttu-id="9e59a-182">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-182">Y</span></span>|<span data-ttu-id="9e59a-183">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-183">89</span></span>|<span data-ttu-id="9e59a-184">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-184">Y</span></span>|
|<span data-ttu-id="9e59a-185">[設定新的索引標籤頁面 URL](./microsoft-edge-policies.md#newtabpagelocation) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-185">[Configure the new tab page URL](./microsoft-edge-policies.md#newtabpagelocation) (policy)</span></span>|<span data-ttu-id="9e59a-186">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-186">N</span></span>|<span data-ttu-id="9e59a-187">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-187">Y</span></span>||<span data-ttu-id="9e59a-188">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-188">Y</span></span>|
|<span data-ttu-id="9e59a-189">結束會話按鈕 \*</span><span class="sxs-lookup"><span data-stu-id="9e59a-189">End session button \*</span></span> | <span data-ttu-id="9e59a-190">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-190">N</span></span>| <span data-ttu-id="9e59a-191">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-191">Y</span></span>| <span data-ttu-id="9e59a-192">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-192">89</span></span>|<span data-ttu-id="9e59a-193">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-193">Y</span></span>|
|<span data-ttu-id="9e59a-194">所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外</span><span class="sxs-lookup"><span data-stu-id="9e59a-194">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="9e59a-195">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-195">N</span></span>|<span data-ttu-id="9e59a-196">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-196">Y</span></span>|<span data-ttu-id="9e59a-197">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-197">89</span></span>|<span data-ttu-id="9e59a-198">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-198">Y</span></span>|
| <span data-ttu-id="9e59a-199">CTRL+N 封鎖 (開啟新的視窗 #) \*</span><span class="sxs-lookup"><span data-stu-id="9e59a-199">CTRL+N blocked (open a new window) \*</span></span> | <span data-ttu-id="9e59a-200">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-200">Y</span></span> | <span data-ttu-id="9e59a-201">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-201">Y</span></span> | <span data-ttu-id="9e59a-202">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-202">89</span></span> |<span data-ttu-id="9e59a-203">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-203">Y</span></span>|
| <span data-ttu-id="9e59a-204">CTRL+T 已封鎖 (開啟新索引標籤)</span><span class="sxs-lookup"><span data-stu-id="9e59a-204">CTRL+T blocked (open new tab)</span></span> |<span data-ttu-id="9e59a-205">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-205">Y</span></span> | <span data-ttu-id="9e59a-206">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-206">N</span></span> | <span data-ttu-id="9e59a-207">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-207">89</span></span> |<span data-ttu-id="9e59a-208">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-208">Y</span></span>|
|<span data-ttu-id="9e59a-209">設定及其他 (...) 將只顯示必要的選項</span><span class="sxs-lookup"><span data-stu-id="9e59a-209">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="9e59a-210">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-210">Y</span></span> |<span data-ttu-id="9e59a-211">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-211">Y</span></span> |<span data-ttu-id="9e59a-212">89</span><span class="sxs-lookup"><span data-stu-id="9e59a-212">89</span></span> |<span data-ttu-id="9e59a-213">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-213">Y</span></span>|
|<span data-ttu-id="9e59a-214">限制從瀏覽器啟動其他應用程式</span><span class="sxs-lookup"><span data-stu-id="9e59a-214">Restrict the launch of other applications from the browser</span></span>|<span data-ttu-id="9e59a-215">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-215">Y</span></span>|<span data-ttu-id="9e59a-216">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-216">Y</span></span>|<span data-ttu-id="9e59a-217">90/91</span><span class="sxs-lookup"><span data-stu-id="9e59a-217">90/91</span></span>|<span data-ttu-id="9e59a-218">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-218">Y</span></span>|
|<span data-ttu-id="9e59a-219">UI 列印設定鎖定</span><span class="sxs-lookup"><span data-stu-id="9e59a-219">UI print settings lockdown</span></span>|<span data-ttu-id="9e59a-220">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-220">Y</span></span>|<span data-ttu-id="9e59a-221">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-221">Y</span></span>|<span data-ttu-id="9e59a-222">90/91</span><span class="sxs-lookup"><span data-stu-id="9e59a-222">90/91</span></span>|<span data-ttu-id="9e59a-223">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-223">Y</span></span>|
|<span data-ttu-id="9e59a-224">[將新的索引標籤頁面設定為首頁](./microsoft-edge-policies.md#homepageisnewtabpage) (原則)</span><span class="sxs-lookup"><span data-stu-id="9e59a-224">[Set the new tab page as the home page](./microsoft-edge-policies.md#homepageisnewtabpage) (policy)</span></span>|-|-|<span data-ttu-id="9e59a-225">待決定</span><span class="sxs-lookup"><span data-stu-id="9e59a-225">TBD</span></span>|<span data-ttu-id="9e59a-226">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-226">Y</span></span>|

> [!NOTE]
> <span data-ttu-id="9e59a-227">只有在指派的存取單一應用程式情況下，才能啟用後面接著 "\*" 的功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-227">Features followed by "\*" are only enabled in an assigned access single app scenario.</span></span>

## <a name="use-kiosk-mode-features"></a><span data-ttu-id="9e59a-228">使用 kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="9e59a-228">Use kiosk mode features</span></span>

<span data-ttu-id="9e59a-229">針對數位/互動式告示板和公開瀏覽使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-229">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options for Digital/Interactive signage and Public browsing.</span></span>

### <a name="kiosk-mode-digitalinteractive-signage"></a><span data-ttu-id="9e59a-230">kiosk 模式數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="9e59a-230">Kiosk mode Digital/Interactive signage</span></span>
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a><span data-ttu-id="9e59a-231">kiosk 模式公用瀏覽：</span><span class="sxs-lookup"><span data-stu-id="9e59a-231">Kiosk mode Public browsing</span></span>

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a><span data-ttu-id="9e59a-232">其他命令列選項</span><span class="sxs-lookup"><span data-stu-id="9e59a-232">Additional command line options</span></span>

- <span data-ttu-id="9e59a-233">**--no-first-run**：停用 Microsoft Edge 初次執行體驗。</span><span class="sxs-lookup"><span data-stu-id="9e59a-233">**--no-first-run**: Disable the first Microsoft Edge run experience.</span></span>

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- <span data-ttu-id="9e59a-234">**--kiosk-idle-timeout-minutes=**：變更從上次使用者活動經過的時間 (以分鐘為單位)，在此時間後，Microsoft Edge kiosk 模式便重設使用者的工作階段。</span><span class="sxs-lookup"><span data-stu-id="9e59a-234">**--kiosk-idle-timeout-minutes=**: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="9e59a-235">將以下範例中的「值」以分鐘數取代。</span><span class="sxs-lookup"><span data-stu-id="9e59a-235">Replace "value" in the next example with the number of minutes.</span></span>

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   <span data-ttu-id="9e59a-236">下列是支援的「值」：</span><span class="sxs-lookup"><span data-stu-id="9e59a-236">The following "values" are supported:</span></span>

     - <span data-ttu-id="9e59a-237">預設值 (以分鐘為單位)</span><span class="sxs-lookup"><span data-stu-id="9e59a-237">Default values (in minutes)</span></span>
       - <span data-ttu-id="9e59a-238">全螢幕 - 0 (關閉)</span><span class="sxs-lookup"><span data-stu-id="9e59a-238">Full screen - 0 (turned off)</span></span>
       - <span data-ttu-id="9e59a-239">公用瀏覽 - 5 分鐘</span><span class="sxs-lookup"><span data-stu-id="9e59a-239">Public browsing - 5 minutes</span></span>
    - <span data-ttu-id="9e59a-240">允許的值</span><span class="sxs-lookup"><span data-stu-id="9e59a-240">Allowed values</span></span>
      - <span data-ttu-id="9e59a-241">0 - 關閉計時器</span><span class="sxs-lookup"><span data-stu-id="9e59a-241">0 - turns off the timer</span></span>
      - <span data-ttu-id="9e59a-242">1-1440 分鐘，用於重設閒置時計時器</span><span class="sxs-lookup"><span data-stu-id="9e59a-242">1-1440 minutes for reset on idle timer</span></span>


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a><span data-ttu-id="9e59a-243">支援 kiosk 模式的原則</span><span class="sxs-lookup"><span data-stu-id="9e59a-243">Support policies for kiosk mode</span></span>

<span data-ttu-id="9e59a-244">使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。</span><span class="sxs-lookup"><span data-stu-id="9e59a-244">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="9e59a-245">若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](./microsoft-edge-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="9e59a-245">To learn more about these policies, see [Microsoft Edge – Browser policy reference](./microsoft-edge-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9e59a-246">原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="9e59a-246">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="9e59a-247">群組原則</span><span class="sxs-lookup"><span data-stu-id="9e59a-247">Group policy</span></span>|<span data-ttu-id="9e59a-248">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="9e59a-248">Digital\Interactive signage</span></span>|<span data-ttu-id="9e59a-249">公用瀏覽單一應用程式</span><span class="sxs-lookup"><span data-stu-id="9e59a-249">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="9e59a-250">列印</span><span class="sxs-lookup"><span data-stu-id="9e59a-250">Printing</span></span>](./microsoft-edge-policies.md#printing-policies) | <span data-ttu-id="9e59a-251">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-251">Y</span></span>|<span data-ttu-id="9e59a-252">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-252">Y</span></span> |
|[<span data-ttu-id="9e59a-253">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="9e59a-253">HomePageLocation</span></span>](./microsoft-edge-policies.md#homepagelocation) |<span data-ttu-id="9e59a-254">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-254">N</span></span> | <span data-ttu-id="9e59a-255">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-255">Y</span></span>|
|[<span data-ttu-id="9e59a-256">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="9e59a-256">ShowHomeButton</span></span>](./microsoft-edge-policies.md#showhomebutton) |<span data-ttu-id="9e59a-257">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-257">N</span></span> | <span data-ttu-id="9e59a-258">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-258">Y</span></span>|
|[<span data-ttu-id="9e59a-259">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="9e59a-259">NewTabPageLocation</span></span>](./microsoft-edge-policies.md#newtabpagelocation) |<span data-ttu-id="9e59a-260">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-260">N</span></span> |<span data-ttu-id="9e59a-261">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-261">Y</span></span> |
|[<span data-ttu-id="9e59a-262">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-262">FavoritesBarEnabled</span></span>](./microsoft-edge-policies.md#favoritesbarenabled) |<span data-ttu-id="9e59a-263">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-263">N</span></span> |<span data-ttu-id="9e59a-264">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-264">Y</span></span> |
|[<span data-ttu-id="9e59a-265">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="9e59a-265">URLAllowlist</span></span>](./microsoft-edge-policies.md#urlallowlist) |<span data-ttu-id="9e59a-266">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-266">Y</span></span> |<span data-ttu-id="9e59a-267">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-267">Y</span></span> |
|[<span data-ttu-id="9e59a-268">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="9e59a-268">URLBlocklist</span></span>](./microsoft-edge-policies.md#urlblocklist) |<span data-ttu-id="9e59a-269">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-269">Y</span></span> | <span data-ttu-id="9e59a-270">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-270">Y</span></span>|
|[<span data-ttu-id="9e59a-271">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="9e59a-271">ManagedSearchEngines</span></span>](./microsoft-edge-policies.md#managedsearchengines) |<span data-ttu-id="9e59a-272">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-272">N</span></span> | <span data-ttu-id="9e59a-273">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-273">Y</span></span>|
|[<span data-ttu-id="9e59a-274">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="9e59a-274">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed) |<span data-ttu-id="9e59a-275">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-275">N</span></span> | <span data-ttu-id="9e59a-276">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-276">Y</span></span>|
|[<span data-ttu-id="9e59a-277">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="9e59a-277">VerticalTabsAllowed</span></span>](./microsoft-edge-policies.md#verticaltabsallowed) | <span data-ttu-id="9e59a-278">否</span><span class="sxs-lookup"><span data-stu-id="9e59a-278">N</span></span>|<span data-ttu-id="9e59a-279">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-279">Y</span></span> |
|[<span data-ttu-id="9e59a-280">SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="9e59a-280">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings-policies) |<span data-ttu-id="9e59a-281">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-281">Y</span></span> |<span data-ttu-id="9e59a-282">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-282">Y</span></span> |
|[<span data-ttu-id="9e59a-283">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-283">EdgeCollectionsEnabled</span></span>](./microsoft-edge-policies.md#edgecollectionsenabled)|<span data-ttu-id="9e59a-284">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-284">Y</span></span>|<span data-ttu-id="9e59a-285">是</span><span class="sxs-lookup"><span data-stu-id="9e59a-285">Y</span></span>|

## <a name="microsoft-edge-with-assigned-access"></a><span data-ttu-id="9e59a-286">具有受指派存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9e59a-286">Microsoft Edge with assigned access</span></span>

### <a name="single-app-kiosk"></a><span data-ttu-id="9e59a-287">單一應用程式 kiosk</span><span class="sxs-lookup"><span data-stu-id="9e59a-287">Single app kiosk</span></span>

<span data-ttu-id="9e59a-288">Microsoft Edge 目前針對單一應用程式受指派的存取權支援一組相同的舊版 Microsoft Edge kiosk 模式類型，包含下列鎖定體驗：數位/互動式告示板和公用瀏覽。</span><span class="sxs-lookup"><span data-stu-id="9e59a-288">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="9e59a-289">您目前可使用最新的  [Windows 10 測試人員預覽版](https://insider.windows.com/)版本 20215 或更新版本，以及  [Microsoft Edge Beta 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本，測試具有受指派存取權單一應用程式的 Microsoft Edge kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="9e59a-289">Microsoft Edge kiosk mode with assigned access single app is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Beta Channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

**<span data-ttu-id="9e59a-290">如何取得 Windows 測試人員預覽？</span><span class="sxs-lookup"><span data-stu-id="9e59a-290">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="9e59a-291">若要在電腦上安裝 Windows 10 測試人員預覽版，請依照 [開始使用 Windows 10 測試人員預覽版](/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="9e59a-291">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](/windows-insider/get-started).</span></span>

### <a name="multi-app-kiosk"></a><span data-ttu-id="9e59a-292">多個應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="9e59a-292">Multi-app kiosk</span></span>

<span data-ttu-id="9e59a-293">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="9e59a-293">Microsoft Edge can be run with [multi-app assigned access](/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="9e59a-294">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="9e59a-294">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="9e59a-295">(Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。</span><span class="sxs-lookup"><span data-stu-id="9e59a-295">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="9e59a-296">使用具有受指派的存取權的 Microsoft Edge 時，您可以設定 Microsoft Edge kiosk 模式，以使用 [Microsoft Edge 瀏覽器原則](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies)來設定瀏覽體驗，進而滿足您的獨特需求。</span><span class="sxs-lookup"><span data-stu-id="9e59a-296">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <a name="configure-using-windows-settings"></a><span data-ttu-id="9e59a-297">使用 Windows 設定進行設定</span><span class="sxs-lookup"><span data-stu-id="9e59a-297">Configure using Windows Settings</span></span>

<span data-ttu-id="9e59a-298">Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="9e59a-298">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="9e59a-299">使用下列步驟設定單一應用程式 kiosk 電腦。</span><span class="sxs-lookup"><span data-stu-id="9e59a-299">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="9e59a-300">安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-300">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="9e59a-301">依照[開始使用 Windows 10 測試人員預覽版](/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="9e59a-301">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](/windows-insider/get-started).</span></span>
2. <span data-ttu-id="9e59a-302">若要測試最新功能，您可以下載最新的 [Microsoft Edge Beta 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-302">To test the latest features, you can download the latest [Microsoft Edge Beta channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>
3. <span data-ttu-id="9e59a-303">在 kiosk 電腦上，開啟 Windows [設定]，然後在搜尋欄位中輸入 "kiosk"。</span><span class="sxs-lookup"><span data-stu-id="9e59a-303">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="9e59a-304">如下一個螢幕擷取畫面所示，選取 \*\* \*\*[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9e59a-304">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. <span data-ttu-id="9e59a-306">在 \*\* ** [設定 kiosk] 頁面上，按一下 ** \*\*[開始使用]。</span><span class="sxs-lookup"><span data-stu-id="9e59a-306">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. <span data-ttu-id="9e59a-308">輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="9e59a-308">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. <span data-ttu-id="9e59a-310">在\*\* ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="9e59a-310">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9e59a-311">這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="9e59a-311">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk 模式 - 選擇應用程式":::

7. <span data-ttu-id="9e59a-313">針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="9e59a-313">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="9e59a-314">數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="9e59a-314">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="9e59a-315">公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="9e59a-315">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

8. <span data-ttu-id="9e59a-317">選取 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="9e59a-317">Select **Next**.</span></span>
9. <span data-ttu-id="9e59a-318">輸入 kiosk 啟動時要載入的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e59a-318">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. <span data-ttu-id="9e59a-320">接受 5 分鐘的閒置時間預設值，或提供您自己的值。</span><span class="sxs-lookup"><span data-stu-id="9e59a-320">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. <span data-ttu-id="9e59a-322">按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="9e59a-322">Click **Next**.</span></span>
12. <span data-ttu-id="9e59a-323">關閉 \*\* \*\* [設定] 視窗，儲存並套用您的選擇。</span><span class="sxs-lookup"><span data-stu-id="9e59a-323">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. <span data-ttu-id="9e59a-325">從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。</span><span class="sxs-lookup"><span data-stu-id="9e59a-325">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <a name="functional-limitations"></a><span data-ttu-id="9e59a-326">功能限制</span><span class="sxs-lookup"><span data-stu-id="9e59a-326">Functional limitations</span></span>

<span data-ttu-id="9e59a-327">隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-327">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="9e59a-328">我們目前不支援下列功能，建議您關閉：</span><span class="sxs-lookup"><span data-stu-id="9e59a-328">We currently don't support the following features and recommend that you turn off:</span></span>

- [<span data-ttu-id="9e59a-329">InPrivateModeAvailability</span><span class="sxs-lookup"><span data-stu-id="9e59a-329">InPrivateModeAvailability</span></span>](./microsoft-edge-policies.md#inprivatemodeavailability)
- [<span data-ttu-id="9e59a-330">IsolateOrigins</span><span class="sxs-lookup"><span data-stu-id="9e59a-330">IsolateOrigins</span></span>](./microsoft-edge-policies.md#isolateorigins)
- [<span data-ttu-id="9e59a-331">ManagedFavorites</span><span class="sxs-lookup"><span data-stu-id="9e59a-331">ManagedFavorites</span></span>](./microsoft-edge-policies.md#managedfavorites)
- [<span data-ttu-id="9e59a-332">EdgeShoppingAssistantEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-332">EdgeShoppingAssistantEnabled</span></span>](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [<span data-ttu-id="9e59a-333">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-333">EdgeCollectionsEnabled</span></span>](./microsoft-edge-policies.md#edgecollectionsenabled)
- [<span data-ttu-id="9e59a-334">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="9e59a-334">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed)
- [<span data-ttu-id="9e59a-335">DefaultPopupsSetting</span><span class="sxs-lookup"><span data-stu-id="9e59a-335">DefaultPopupsSetting</span></span>](./microsoft-edge-policies.md#defaultpopupssetting)
- [<span data-ttu-id="9e59a-336">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-336">StartupBoostEnabled</span></span>](./microsoft-edge-policies.md#startupboostenabled)
- [<span data-ttu-id="9e59a-337">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="9e59a-337">InternetExplorerIntegrationLevel</span></span>](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [<span data-ttu-id="9e59a-338">Extensions</span><span class="sxs-lookup"><span data-stu-id="9e59a-338">Extensions</span></span>](./microsoft-edge-policies.md#extensions-policies)
- [<span data-ttu-id="9e59a-339">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="9e59a-339">BackgroundModeEnabled</span></span>](./microsoft-edge-policies.md#backgroundmodeenabled)
- [<span data-ttu-id="9e59a-340">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="9e59a-340">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="roadmap"></a><span data-ttu-id="9e59a-341">藍圖</span><span class="sxs-lookup"><span data-stu-id="9e59a-341">Roadmap</span></span>

### <a name="in-early-2021"></a><span data-ttu-id="9e59a-342">2021 年年初</span><span class="sxs-lookup"><span data-stu-id="9e59a-342">In early 2021</span></span>

<span data-ttu-id="9e59a-343">我們將增加下列支援和功能：</span><span class="sxs-lookup"><span data-stu-id="9e59a-343">We'll add the following support and features:</span></span>

- <span data-ttu-id="9e59a-344">在 Windows 10 1909 和更新版本上，具有獲指派存取權單一應用程式之 Microsoft Edge kiosk 模式的正式發行。</span><span class="sxs-lookup"><span data-stu-id="9e59a-344">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="9e59a-345">與舊版 Microsoft Edge 同等的其他功能。</span><span class="sxs-lookup"><span data-stu-id="9e59a-345">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="9e59a-346">與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="9e59a-346">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="9e59a-347">限制從瀏覽器啟動其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="9e59a-347">Restrict the launch of other applications from the browser.</span></span>
- <span data-ttu-id="9e59a-348">UI 列印設定鎖定。</span><span class="sxs-lookup"><span data-stu-id="9e59a-348">UI print settings lockdown.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e59a-349">請參閱</span><span class="sxs-lookup"><span data-stu-id="9e59a-349">See also</span></span>

- [<span data-ttu-id="9e59a-350">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9e59a-350">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9e59a-351">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="9e59a-351">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="9e59a-352">設定 Windows 桌面版的 kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="9e59a-352">Configure kiosks and digital signs on Windows desktop editions</span></span>](/windows/configuration/kiosk-methods)
- [<span data-ttu-id="9e59a-353">規劃 kiosk 模式轉換</span><span class="sxs-lookup"><span data-stu-id="9e59a-353">Plan your kiosk mode transition</span></span>](microsoft-edge-kiosk-mode-transition-plan.md)