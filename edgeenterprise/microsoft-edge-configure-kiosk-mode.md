---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 04/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Kiosk 模式功能，以及如何設定 Microsoft Edge Kiosk 模式選項。
ms.openlocfilehash: 20cb32c0cd27ad6d7437ed8ae0440560f3ed71b2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617853"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a><span data-ttu-id="1b83b-103">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="1b83b-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="1b83b-104">本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="1b83b-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="1b83b-105">另提供一份我們鎖定之功能的藍圖。</span><span class="sxs-lookup"><span data-stu-id="1b83b-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="1b83b-106">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1b83b-106">This article applies to Microsoft Edge version 87 or later.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b83b-107">使用[使用 kiosk 模式功能](#use-kiosk-mode-features)中的命令列引數，叫用 Windows 10 上的 Microsoft Edge kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-107">Invoke Microsoft Edge kiosk mode features on Windows 10 using the command line arguments provided in [Use kiosk mode features](#use-kiosk-mode-features).</span></span>

## <a name="overview"></a><span data-ttu-id="1b83b-108">概觀</span><span class="sxs-lookup"><span data-stu-id="1b83b-108">Overview</span></span>

<span data-ttu-id="1b83b-109">Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="1b83b-109">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="1b83b-110">可使用的鎖定體驗如下：</span><span class="sxs-lookup"><span data-stu-id="1b83b-110">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="1b83b-111">**數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="1b83b-111">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="1b83b-112">**公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。</span><span class="sxs-lookup"><span data-stu-id="1b83b-112">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="1b83b-113">兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="1b83b-113">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <a name="set-up-microsoft-edge-kiosk-mode"></a><span data-ttu-id="1b83b-114">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="1b83b-114">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="1b83b-115">使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-115">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="1b83b-116">您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。</span><span class="sxs-lookup"><span data-stu-id="1b83b-116">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <a name="kiosk-mode-supported-features"></a><span data-ttu-id="1b83b-117">kiosk 模式支援的功能</span><span class="sxs-lookup"><span data-stu-id="1b83b-117">Kiosk mode supported features</span></span>

<span data-ttu-id="1b83b-118">下表列出 Microsoft Edge 與舊版 Microsoft Edge 中的 kiosk 模式所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-118">The following table lists the features supported by kiosk mode in Microsoft Edge and Microsoft Edge Legacy.</span></span> <span data-ttu-id="1b83b-119">使用此表格做為轉換至 Microsoft Edge 的指南，方法是比較在這兩個版本的 Microsoft Edge 中支援這些功能的情況。</span><span class="sxs-lookup"><span data-stu-id="1b83b-119">Use this table as a guide to transitioning to Microsoft Edge by comparing how these features are supported in both versions of Microsoft Edge.</span></span>

|<span data-ttu-id="1b83b-120">功能</span><span class="sxs-lookup"><span data-stu-id="1b83b-120">Feature</span></span>|<span data-ttu-id="1b83b-121">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="1b83b-121">Digital\Interactive Signage</span></span>|<span data-ttu-id="1b83b-122">公用瀏覽</span><span class="sxs-lookup"><span data-stu-id="1b83b-122">Public browsing</span></span>|<span data-ttu-id="1b83b-123">隨 Microsoft Edge 版本 (及更新版本) 提供</span><span class="sxs-lookup"><span data-stu-id="1b83b-123">Available with Microsoft Edge version (and higher)</span></span>|<span data-ttu-id="1b83b-124">隨舊版 Microsoft Edge 提供</span><span class="sxs-lookup"><span data-stu-id="1b83b-124">Available with Microsoft Edge Legacy</span></span>|
|-|-|-|-|-|
|<span data-ttu-id="1b83b-125">InPrivate 瀏覽</span><span class="sxs-lookup"><span data-stu-id="1b83b-125">InPrivate Navigation</span></span>|<span data-ttu-id="1b83b-126">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-126">Y</span></span>|<span data-ttu-id="1b83b-127">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-127">Y</span></span>|<span data-ttu-id="1b83b-128">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-128">89</span></span>|<span data-ttu-id="1b83b-129">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-129">Y</span></span>|
|<span data-ttu-id="1b83b-130">在非使用狀態時重設</span><span class="sxs-lookup"><span data-stu-id="1b83b-130">Reset on inactivity</span></span>|<span data-ttu-id="1b83b-131">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-131">Y</span></span>|<span data-ttu-id="1b83b-132">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-132">Y</span></span>|<span data-ttu-id="1b83b-133">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-133">89</span></span>|<span data-ttu-id="1b83b-134">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-134">Y</span></span>|
|<span data-ttu-id="1b83b-135">[唯讀網址列](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-135">[Read only address bar](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="1b83b-136">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-136">N</span></span>|<span data-ttu-id="1b83b-137">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-137">Y</span></span> |<span data-ttu-id="1b83b-138">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-138">89</span></span>|<span data-ttu-id="1b83b-139">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-139">N</span></span>|
|<span data-ttu-id="1b83b-140">[結束時刪除下載](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-140">[Delete downloads on exit](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="1b83b-141">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-141">Y</span></span>|<span data-ttu-id="1b83b-142">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-142">Y</span></span> |<span data-ttu-id="1b83b-143">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-143">89</span></span>|<span data-ttu-id="1b83b-144">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-144">N</span></span>|
|<span data-ttu-id="1b83b-145">F11 已封鎖 (進入/結束全螢幕)</span><span class="sxs-lookup"><span data-stu-id="1b83b-145">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="1b83b-146">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-146">Y</span></span> | <span data-ttu-id="1b83b-147">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-147">Y</span></span> |<span data-ttu-id="1b83b-148">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-148">89</span></span>|<span data-ttu-id="1b83b-149">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-149">Y</span></span>|
|<span data-ttu-id="1b83b-150">F12 已封鎖 (啟動開發人員工具)</span><span class="sxs-lookup"><span data-stu-id="1b83b-150">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="1b83b-151">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-151">Y</span></span> | <span data-ttu-id="1b83b-152">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-152">Y</span></span> |<span data-ttu-id="1b83b-153">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-153">89</span></span>|<span data-ttu-id="1b83b-154">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-154">Y</span></span>|
| <span data-ttu-id="1b83b-155">支援多個索引標籤</span><span class="sxs-lookup"><span data-stu-id="1b83b-155">Multi tab support</span></span> | <span data-ttu-id="1b83b-156">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-156">N</span></span>| <span data-ttu-id="1b83b-157">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-157">Y</span></span>|<span data-ttu-id="1b83b-158">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-158">89</span></span>|<span data-ttu-id="1b83b-159">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-159">Y</span></span>|
|<span data-ttu-id="1b83b-160">[允許 URL 支援](./microsoft-edge-policies.md#urlallowlist) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-160">[Allow URL support](./microsoft-edge-policies.md#urlallowlist) (policy)</span></span>|<span data-ttu-id="1b83b-161">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-161">Y</span></span>|<span data-ttu-id="1b83b-162">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-162">Y</span></span>|<span data-ttu-id="1b83b-163">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-163">89</span></span>|<span data-ttu-id="1b83b-164">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-164">N</span></span>|
|<span data-ttu-id="1b83b-165">[封鎖 URL 支援](./microsoft-edge-policies.md#urlblocklist) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-165">[Block URL support](./microsoft-edge-policies.md#urlblocklist) (policy)</span></span>|<span data-ttu-id="1b83b-166">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-166">Y</span></span>|<span data-ttu-id="1b83b-167">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-167">Y</span></span>|<span data-ttu-id="1b83b-168">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-168">89</span></span>|<span data-ttu-id="1b83b-169">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-169">N</span></span>|
|<span data-ttu-id="1b83b-170">[顯示首頁按鈕](./microsoft-edge-policies.md#showhomebutton) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-170">[Show home button](./microsoft-edge-policies.md#showhomebutton) (policy)</span></span>|<span data-ttu-id="1b83b-171">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-171">N</span></span>|<span data-ttu-id="1b83b-172">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-172">Y</span></span>|<span data-ttu-id="1b83b-173">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-173">89</span></span>|<span data-ttu-id="1b83b-174">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-174">Y</span></span>|
|<span data-ttu-id="1b83b-175">[管理我的最愛](./microsoft-edge-policies.md#managedfavorites) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-175">[Manage favorites](./microsoft-edge-policies.md#managedfavorites) (policy)</span></span>|<span data-ttu-id="1b83b-176">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-176">N</span></span>|<span data-ttu-id="1b83b-177">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-177">Y</span></span>|<span data-ttu-id="1b83b-178">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-178">89</span></span>|<span data-ttu-id="1b83b-179">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-179">Y</span></span>|
|<span data-ttu-id="1b83b-180">[啟用印表機](./microsoft-edge-policies.md#printingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-180">[Enable printer](./microsoft-edge-policies.md#printingenabled) (policy)</span></span>|<span data-ttu-id="1b83b-181">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-181">Y</span></span>|<span data-ttu-id="1b83b-182">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-182">Y</span></span>|<span data-ttu-id="1b83b-183">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-183">89</span></span>|<span data-ttu-id="1b83b-184">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-184">Y</span></span>|
|<span data-ttu-id="1b83b-185">[設定新的索引標籤頁面 URL](./microsoft-edge-policies.md#newtabpagelocation) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-185">[Configure the new tab page URL](./microsoft-edge-policies.md#newtabpagelocation) (policy)</span></span>|<span data-ttu-id="1b83b-186">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-186">N</span></span>|<span data-ttu-id="1b83b-187">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-187">Y</span></span>|<span data-ttu-id="1b83b-188">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-188">89</span></span>|<span data-ttu-id="1b83b-189">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-189">Y</span></span>|
|<span data-ttu-id="1b83b-190">結束會話按鈕 \*</span><span class="sxs-lookup"><span data-stu-id="1b83b-190">End session button \*</span></span> | <span data-ttu-id="1b83b-191">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-191">N</span></span>| <span data-ttu-id="1b83b-192">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-192">Y</span></span>|<span data-ttu-id="1b83b-193">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-193">89</span></span>|<span data-ttu-id="1b83b-194">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-194">Y</span></span>|
|<span data-ttu-id="1b83b-195">所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外</span><span class="sxs-lookup"><span data-stu-id="1b83b-195">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="1b83b-196">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-196">N</span></span>|<span data-ttu-id="1b83b-197">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-197">Y</span></span>|<span data-ttu-id="1b83b-198">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-198">89</span></span>|<span data-ttu-id="1b83b-199">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-199">Y</span></span>|
| <span data-ttu-id="1b83b-200">CTRL+N 封鎖 (開啟新的視窗 #) \*</span><span class="sxs-lookup"><span data-stu-id="1b83b-200">CTRL+N blocked (open a new window) \*</span></span> | <span data-ttu-id="1b83b-201">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-201">Y</span></span> | <span data-ttu-id="1b83b-202">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-202">Y</span></span> |<span data-ttu-id="1b83b-203">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-203">89</span></span>|<span data-ttu-id="1b83b-204">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-204">Y</span></span>|
| <span data-ttu-id="1b83b-205">CTRL+T 已封鎖 (開啟新索引標籤)</span><span class="sxs-lookup"><span data-stu-id="1b83b-205">CTRL+T blocked (open new tab)</span></span> |<span data-ttu-id="1b83b-206">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-206">Y</span></span> | <span data-ttu-id="1b83b-207">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-207">N</span></span> |<span data-ttu-id="1b83b-208">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-208">89</span></span>|<span data-ttu-id="1b83b-209">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-209">Y</span></span>|
|<span data-ttu-id="1b83b-210">設定及其他 (...) 將只顯示必要的選項</span><span class="sxs-lookup"><span data-stu-id="1b83b-210">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="1b83b-211">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-211">Y</span></span> |<span data-ttu-id="1b83b-212">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-212">Y</span></span> |<span data-ttu-id="1b83b-213">89</span><span class="sxs-lookup"><span data-stu-id="1b83b-213">89</span></span>|<span data-ttu-id="1b83b-214">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-214">Y</span></span>|
|<span data-ttu-id="1b83b-215">限制從瀏覽器啟動其他應用程式</span><span class="sxs-lookup"><span data-stu-id="1b83b-215">Restrict the launch of other applications from the browser</span></span>|<span data-ttu-id="1b83b-216">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-216">Y</span></span>|<span data-ttu-id="1b83b-217">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-217">Y</span></span>|<span data-ttu-id="1b83b-218">90</span><span class="sxs-lookup"><span data-stu-id="1b83b-218">90</span></span>|<span data-ttu-id="1b83b-219">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-219">Y</span></span>|
|<span data-ttu-id="1b83b-220">UI 列印設定鎖定</span><span class="sxs-lookup"><span data-stu-id="1b83b-220">UI print settings lockdown</span></span>|<span data-ttu-id="1b83b-221">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-221">Y</span></span>|<span data-ttu-id="1b83b-222">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-222">Y</span></span>|<span data-ttu-id="1b83b-223">90</span><span class="sxs-lookup"><span data-stu-id="1b83b-223">90</span></span>|<span data-ttu-id="1b83b-224">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-224">Y</span></span>|
|<span data-ttu-id="1b83b-225">[將新的索引標籤頁面設定為首頁](./microsoft-edge-policies.md#homepageisnewtabpage) (原則)</span><span class="sxs-lookup"><span data-stu-id="1b83b-225">[Set the new tab page as the home page](./microsoft-edge-policies.md#homepageisnewtabpage) (policy)</span></span>|<span data-ttu-id="1b83b-226">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-226">N</span></span>|<span data-ttu-id="1b83b-227">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-227">Y</span></span>|<span data-ttu-id="1b83b-228">90</span><span class="sxs-lookup"><span data-stu-id="1b83b-228">90</span></span>|<span data-ttu-id="1b83b-229">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-229">Y</span></span>|

> [!NOTE]
> <span data-ttu-id="1b83b-230">只有在指派的存取單一應用程式情況下，才能啟用後面接著 "\*" 的功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-230">Features followed by "\*" are only enabled in an assigned access single app scenario.</span></span>

## <a name="use-kiosk-mode-features"></a><span data-ttu-id="1b83b-231">使用 kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="1b83b-231">Use kiosk mode features</span></span>

<span data-ttu-id="1b83b-232">針對數位/互動式告示板和公開瀏覽使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-232">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options for Digital/Interactive signage and Public browsing.</span></span>

### <a name="kiosk-mode-digitalinteractive-signage"></a><span data-ttu-id="1b83b-233">kiosk 模式數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="1b83b-233">Kiosk mode Digital/Interactive signage</span></span>
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a><span data-ttu-id="1b83b-234">kiosk 模式公用瀏覽：</span><span class="sxs-lookup"><span data-stu-id="1b83b-234">Kiosk mode Public browsing</span></span>

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a><span data-ttu-id="1b83b-235">其他命令列選項</span><span class="sxs-lookup"><span data-stu-id="1b83b-235">Additional command line options</span></span>

- <span data-ttu-id="1b83b-236">**--no-first-run**：停用 Microsoft Edge 初次執行體驗。</span><span class="sxs-lookup"><span data-stu-id="1b83b-236">**--no-first-run**: Disable the first Microsoft Edge run experience.</span></span>

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- <span data-ttu-id="1b83b-237">**--kiosk-idle-timeout-minutes=**：變更從上次使用者活動經過的時間 (以分鐘為單位)，在此時間後，Microsoft Edge kiosk 模式便重設使用者的工作階段。</span><span class="sxs-lookup"><span data-stu-id="1b83b-237">**--kiosk-idle-timeout-minutes=**: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="1b83b-238">將以下範例中的「值」以分鐘數取代。</span><span class="sxs-lookup"><span data-stu-id="1b83b-238">Replace "value" in the next example with the number of minutes.</span></span>

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   <span data-ttu-id="1b83b-239">下列是支援的「值」：</span><span class="sxs-lookup"><span data-stu-id="1b83b-239">The following "values" are supported:</span></span>

     - <span data-ttu-id="1b83b-240">預設值 (以分鐘為單位)</span><span class="sxs-lookup"><span data-stu-id="1b83b-240">Default values (in minutes)</span></span>
       - <span data-ttu-id="1b83b-241">全螢幕 - 0 (關閉)</span><span class="sxs-lookup"><span data-stu-id="1b83b-241">Full screen - 0 (turned off)</span></span>
       - <span data-ttu-id="1b83b-242">公用瀏覽 - 5 分鐘</span><span class="sxs-lookup"><span data-stu-id="1b83b-242">Public browsing - 5 minutes</span></span>
    - <span data-ttu-id="1b83b-243">允許的值</span><span class="sxs-lookup"><span data-stu-id="1b83b-243">Allowed values</span></span>
      - <span data-ttu-id="1b83b-244">0 - 關閉計時器</span><span class="sxs-lookup"><span data-stu-id="1b83b-244">0 - turns off the timer</span></span>
      - <span data-ttu-id="1b83b-245">1-1440 分鐘，用於重設閒置時計時器</span><span class="sxs-lookup"><span data-stu-id="1b83b-245">1-1440 minutes for reset on idle timer</span></span>


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a><span data-ttu-id="1b83b-246">支援 kiosk 模式的原則</span><span class="sxs-lookup"><span data-stu-id="1b83b-246">Support policies for kiosk mode</span></span>

<span data-ttu-id="1b83b-247">使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。</span><span class="sxs-lookup"><span data-stu-id="1b83b-247">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="1b83b-248">若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](./microsoft-edge-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="1b83b-248">To learn more about these policies, see [Microsoft Edge – Browser policy reference](./microsoft-edge-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1b83b-249">原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="1b83b-249">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="1b83b-250">群組原則</span><span class="sxs-lookup"><span data-stu-id="1b83b-250">Group policy</span></span>|<span data-ttu-id="1b83b-251">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="1b83b-251">Digital\Interactive signage</span></span>|<span data-ttu-id="1b83b-252">公用瀏覽單一應用程式</span><span class="sxs-lookup"><span data-stu-id="1b83b-252">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="1b83b-253">列印</span><span class="sxs-lookup"><span data-stu-id="1b83b-253">Printing</span></span>](./microsoft-edge-policies.md#printing-policies) | <span data-ttu-id="1b83b-254">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-254">Y</span></span>|<span data-ttu-id="1b83b-255">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-255">Y</span></span> |
|[<span data-ttu-id="1b83b-256">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="1b83b-256">HomePageLocation</span></span>](./microsoft-edge-policies.md#homepagelocation) |<span data-ttu-id="1b83b-257">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-257">N</span></span> | <span data-ttu-id="1b83b-258">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-258">Y</span></span>|
|[<span data-ttu-id="1b83b-259">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="1b83b-259">ShowHomeButton</span></span>](./microsoft-edge-policies.md#showhomebutton) |<span data-ttu-id="1b83b-260">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-260">N</span></span> | <span data-ttu-id="1b83b-261">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-261">Y</span></span>|
|[<span data-ttu-id="1b83b-262">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="1b83b-262">NewTabPageLocation</span></span>](./microsoft-edge-policies.md#newtabpagelocation) |<span data-ttu-id="1b83b-263">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-263">N</span></span> |<span data-ttu-id="1b83b-264">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-264">Y</span></span> |
|[<span data-ttu-id="1b83b-265">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-265">FavoritesBarEnabled</span></span>](./microsoft-edge-policies.md#favoritesbarenabled) |<span data-ttu-id="1b83b-266">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-266">N</span></span> |<span data-ttu-id="1b83b-267">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-267">Y</span></span> |
|[<span data-ttu-id="1b83b-268">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="1b83b-268">URLAllowlist</span></span>](./microsoft-edge-policies.md#urlallowlist) |<span data-ttu-id="1b83b-269">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-269">Y</span></span> |<span data-ttu-id="1b83b-270">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-270">Y</span></span> |
|[<span data-ttu-id="1b83b-271">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="1b83b-271">URLBlocklist</span></span>](./microsoft-edge-policies.md#urlblocklist) |<span data-ttu-id="1b83b-272">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-272">Y</span></span> | <span data-ttu-id="1b83b-273">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-273">Y</span></span>|
|[<span data-ttu-id="1b83b-274">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="1b83b-274">ManagedSearchEngines</span></span>](./microsoft-edge-policies.md#managedsearchengines) |<span data-ttu-id="1b83b-275">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-275">N</span></span> | <span data-ttu-id="1b83b-276">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-276">Y</span></span>|
|[<span data-ttu-id="1b83b-277">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="1b83b-277">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed) |<span data-ttu-id="1b83b-278">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-278">N</span></span> | <span data-ttu-id="1b83b-279">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-279">Y</span></span>|
|[<span data-ttu-id="1b83b-280">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="1b83b-280">VerticalTabsAllowed</span></span>](./microsoft-edge-policies.md#verticaltabsallowed) | <span data-ttu-id="1b83b-281">否</span><span class="sxs-lookup"><span data-stu-id="1b83b-281">N</span></span>|<span data-ttu-id="1b83b-282">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-282">Y</span></span> |
|[<span data-ttu-id="1b83b-283">SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="1b83b-283">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings-policies) |<span data-ttu-id="1b83b-284">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-284">Y</span></span> |<span data-ttu-id="1b83b-285">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-285">Y</span></span> |
|[<span data-ttu-id="1b83b-286">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-286">EdgeCollectionsEnabled</span></span>](./microsoft-edge-policies.md#edgecollectionsenabled)|<span data-ttu-id="1b83b-287">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-287">Y</span></span>|<span data-ttu-id="1b83b-288">是</span><span class="sxs-lookup"><span data-stu-id="1b83b-288">Y</span></span>|

## <a name="microsoft-edge-with-assigned-access"></a><span data-ttu-id="1b83b-289">具有受指派存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b83b-289">Microsoft Edge with assigned access</span></span>

### <a name="single-app-kiosk"></a><span data-ttu-id="1b83b-290">單一應用程式 kiosk</span><span class="sxs-lookup"><span data-stu-id="1b83b-290">Single app kiosk</span></span>

<span data-ttu-id="1b83b-291">Microsoft Edge 版本 90 kiosk 模式提供廣泛的功能清單。</span><span class="sxs-lookup"><span data-stu-id="1b83b-291">Microsoft Edge version 90 kiosk mode offers an extensive list of features.</span></span> <span data-ttu-id="1b83b-292">請參閱 Kiosk 模式支援功能一節。</span><span class="sxs-lookup"><span data-stu-id="1b83b-292">See the section of Kiosk mode supported features.</span></span>
<span data-ttu-id="1b83b-293">透過下列 Windows 更新，您可以透過受指派的存取權單一應用程式來設定 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="1b83b-293">With the following Windows updates you can configure Microsoft Edge via assigned access single app.</span></span>

|<span data-ttu-id="1b83b-294">作業系統</span><span class="sxs-lookup"><span data-stu-id="1b83b-294">Operating System</span></span>|<span data-ttu-id="1b83b-295">版本</span><span class="sxs-lookup"><span data-stu-id="1b83b-295">Version</span></span>|<span data-ttu-id="1b83b-296">更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-296">Updates</span></span>|
|--|--|--|
|<span data-ttu-id="1b83b-297">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1b83b-297">Windows 10</span></span> | <span data-ttu-id="1b83b-298">2004 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b83b-298">2004 or later</span></span>|[<span data-ttu-id="1b83b-299">KB4601382 或更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-299">KB4601382 or later</span></span>](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|<span data-ttu-id="1b83b-300">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1b83b-300">Windows 10</span></span>| <span data-ttu-id="1b83b-301">1909</span><span class="sxs-lookup"><span data-stu-id="1b83b-301">1909</span></span>| [<span data-ttu-id="1b83b-302">KB4601380 或更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-302">KB4601380 or later</span></span>](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

<span data-ttu-id="1b83b-303">您可以透過 [Windows 設定](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings)和 Intune 管理 Microsoft Edge kiosk 模式受指派的存取權單一應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b83b-303">You can manage Microsoft Edge kiosk mode assigned access single app via [Windows Settings](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings) and Intune.</span></span>

### <a name="multi-app-kiosk"></a><span data-ttu-id="1b83b-304">多個應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="1b83b-304">Multi-app kiosk</span></span>

<span data-ttu-id="1b83b-305">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="1b83b-305">Microsoft Edge can be run with [multi-app assigned access](/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="1b83b-306">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="1b83b-306">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="1b83b-307">(Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。</span><span class="sxs-lookup"><span data-stu-id="1b83b-307">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

### <a name="configure-using-windows-settings"></a><span data-ttu-id="1b83b-308">使用 Windows 設定進行設定</span><span class="sxs-lookup"><span data-stu-id="1b83b-308">Configure using Windows Settings</span></span>

<span data-ttu-id="1b83b-309">Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="1b83b-309">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="1b83b-310">使用下列步驟設定單一應用程式 kiosk 電腦。</span><span class="sxs-lookup"><span data-stu-id="1b83b-310">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="1b83b-311">下表列出作業系統的最小系統更新。</span><span class="sxs-lookup"><span data-stu-id="1b83b-311">The minimum system updates for the operating systems listed in the next table.</span></span>

|<span data-ttu-id="1b83b-312">作業系統</span><span class="sxs-lookup"><span data-stu-id="1b83b-312">Operating System</span></span>|<span data-ttu-id="1b83b-313">版本</span><span class="sxs-lookup"><span data-stu-id="1b83b-313">Version</span></span>|<span data-ttu-id="1b83b-314">更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-314">Updates</span></span>|
|--|--|--|
|<span data-ttu-id="1b83b-315">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1b83b-315">Windows 10</span></span> | <span data-ttu-id="1b83b-316">2004 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1b83b-316">2004 or later</span></span>|[<span data-ttu-id="1b83b-317">KB4601382 或更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-317">KB4601382 or later</span></span>](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|<span data-ttu-id="1b83b-318">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1b83b-318">Windows 10</span></span>| <span data-ttu-id="1b83b-319">1909</span><span class="sxs-lookup"><span data-stu-id="1b83b-319">1909</span></span>| [<span data-ttu-id="1b83b-320">KB4601380 或更新</span><span class="sxs-lookup"><span data-stu-id="1b83b-320">KB4601380 or later</span></span>](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. <span data-ttu-id="1b83b-321">若要測試最新功能，您可以下載最新的 [Microsoft Edge 穩定通道](https://www.microsoft.com/edge/business/download)版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1b83b-321">To test the latest features, you can download the latest [Microsoft Edge Stable channel](https://www.microsoft.com/edge/business/download), version 89 or higher.</span></span>

3. <span data-ttu-id="1b83b-322">在 kiosk 電腦上，開啟 Windows [設定]，然後在搜尋欄位中輸入 "kiosk"。</span><span class="sxs-lookup"><span data-stu-id="1b83b-322">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="1b83b-323">如下一個螢幕擷取畫面所示，選取 \*\* \*\*[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="1b83b-323">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. <span data-ttu-id="1b83b-325">在 \*\* ** [設定 kiosk] 頁面上，按一下 ** \*\*[開始使用]。</span><span class="sxs-lookup"><span data-stu-id="1b83b-325">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. <span data-ttu-id="1b83b-327">輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="1b83b-327">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. <span data-ttu-id="1b83b-329">在\*\* ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="1b83b-329">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="1b83b-330">這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="1b83b-330">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

7. <span data-ttu-id="1b83b-332">針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="1b83b-332">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="1b83b-333">數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="1b83b-333">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="1b83b-334">公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="1b83b-334">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="如何使用 kiosk - 全螢幕數位標誌":::

8. <span data-ttu-id="1b83b-336">選取 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="1b83b-336">Select **Next**.</span></span>
9. <span data-ttu-id="1b83b-337">輸入 kiosk 啟動時要載入的 URL。</span><span class="sxs-lookup"><span data-stu-id="1b83b-337">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. <span data-ttu-id="1b83b-339">接受 5 分鐘的閒置時間預設值，或提供您自己的值。</span><span class="sxs-lookup"><span data-stu-id="1b83b-339">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. <span data-ttu-id="1b83b-341">按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="1b83b-341">Click **Next**.</span></span>
12. <span data-ttu-id="1b83b-342">關閉 \*\* \*\* [設定] 視窗，儲存並套用您的選擇。</span><span class="sxs-lookup"><span data-stu-id="1b83b-342">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. <span data-ttu-id="1b83b-344">從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。</span><span class="sxs-lookup"><span data-stu-id="1b83b-344">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <a name="functional-limitations"></a><span data-ttu-id="1b83b-345">功能限制</span><span class="sxs-lookup"><span data-stu-id="1b83b-345">Functional limitations</span></span>

<span data-ttu-id="1b83b-346">隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。</span><span class="sxs-lookup"><span data-stu-id="1b83b-346">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="1b83b-347">我們目前不支援下列功能，建議您關閉：</span><span class="sxs-lookup"><span data-stu-id="1b83b-347">We currently don't support the following features and recommend that you turn off:</span></span>

- [<span data-ttu-id="1b83b-348">InPrivateModeAvailability</span><span class="sxs-lookup"><span data-stu-id="1b83b-348">InPrivateModeAvailability</span></span>](./microsoft-edge-policies.md#inprivatemodeavailability)
- [<span data-ttu-id="1b83b-349">IsolateOrigins</span><span class="sxs-lookup"><span data-stu-id="1b83b-349">IsolateOrigins</span></span>](./microsoft-edge-policies.md#isolateorigins)
- [<span data-ttu-id="1b83b-350">ManagedFavorites</span><span class="sxs-lookup"><span data-stu-id="1b83b-350">ManagedFavorites</span></span>](./microsoft-edge-policies.md#managedfavorites)
- [<span data-ttu-id="1b83b-351">EdgeShoppingAssistantEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-351">EdgeShoppingAssistantEnabled</span></span>](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [<span data-ttu-id="1b83b-352">EdgeCollectionsEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-352">EdgeCollectionsEnabled</span></span>](./microsoft-edge-policies.md#edgecollectionsenabled)
- [<span data-ttu-id="1b83b-353">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="1b83b-353">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed)
- [<span data-ttu-id="1b83b-354">DefaultPopupsSetting</span><span class="sxs-lookup"><span data-stu-id="1b83b-354">DefaultPopupsSetting</span></span>](./microsoft-edge-policies.md#defaultpopupssetting)
- [<span data-ttu-id="1b83b-355">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-355">StartupBoostEnabled</span></span>](./microsoft-edge-policies.md#startupboostenabled)
- [<span data-ttu-id="1b83b-356">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="1b83b-356">InternetExplorerIntegrationLevel</span></span>](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [<span data-ttu-id="1b83b-357">Extensions</span><span class="sxs-lookup"><span data-stu-id="1b83b-357">Extensions</span></span>](./microsoft-edge-policies.md#extensions-policies)
- [<span data-ttu-id="1b83b-358">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="1b83b-358">BackgroundModeEnabled</span></span>](./microsoft-edge-policies.md#backgroundmodeenabled)
- [<span data-ttu-id="1b83b-359">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="1b83b-359">UserFeedbackAllowed</span></span>](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a><span data-ttu-id="1b83b-360">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b83b-360">See also</span></span>

- [<span data-ttu-id="1b83b-361">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="1b83b-361">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="1b83b-362">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="1b83b-362">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="1b83b-363">設定 Windows 桌面版的 kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="1b83b-363">Configure kiosks and digital signs on Windows desktop editions</span></span>](/windows/configuration/kiosk-methods)
- [<span data-ttu-id="1b83b-364">規劃 kiosk 模式轉換</span><span class="sxs-lookup"><span data-stu-id="1b83b-364">Plan your kiosk mode transition</span></span>](microsoft-edge-kiosk-mode-transition-plan.md)
