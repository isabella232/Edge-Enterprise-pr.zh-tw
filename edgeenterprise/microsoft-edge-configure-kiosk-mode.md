---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge kiosk 模式
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297469"
---
# <span data-ttu-id="4cc30-103">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="4cc30-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="4cc30-104">本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="4cc30-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="4cc30-105">另提供一份我們鎖定之功能的藍圖。</span><span class="sxs-lookup"><span data-stu-id="4cc30-105">There's also a roadmap of features we're targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="4cc30-106">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="4cc30-107">概觀</span><span class="sxs-lookup"><span data-stu-id="4cc30-107">Overview</span></span>

<span data-ttu-id="4cc30-108">Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="4cc30-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="4cc30-109">可使用的鎖定體驗如下：</span><span class="sxs-lookup"><span data-stu-id="4cc30-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="4cc30-110">**數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="4cc30-110">**Digital/Interactive Signage** experience - Displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="4cc30-111">**公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-111">**Public-Browsing** experience - Runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="4cc30-112">兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="4cc30-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="4cc30-113">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="4cc30-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="4cc30-114">使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。</span><span class="sxs-lookup"><span data-stu-id="4cc30-114">An initial set of kiosk mode features is available to test with Microsoft Edge Stable Channel, version 87.</span></span> <span data-ttu-id="4cc30-115">您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-115">You can download the latest version from [Microsoft Edge (Official Stable Channel)](https://www.microsoft.com/edge).</span></span>

### <span data-ttu-id="4cc30-116">kiosk 模式支援的功能</span><span class="sxs-lookup"><span data-stu-id="4cc30-116">Kiosk mode supported features</span></span>

<span data-ttu-id="4cc30-117">下表列出 kiosk 模式支援的功能。</span><span class="sxs-lookup"><span data-stu-id="4cc30-117">The following table lists the features supported by kiosk mode.</span></span>

|<span data-ttu-id="4cc30-118">功能</span><span class="sxs-lookup"><span data-stu-id="4cc30-118">Feature</span></span>|<span data-ttu-id="4cc30-119">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="4cc30-119">Digital\Interactive Signage</span></span>|<span data-ttu-id="4cc30-120">公用瀏覽</span><span class="sxs-lookup"><span data-stu-id="4cc30-120">Public browsing</span></span>|<span data-ttu-id="4cc30-121">隨 Microsoft Edge 版本 (及更新版本) 提供</span><span class="sxs-lookup"><span data-stu-id="4cc30-121">Available with Microsoft Edge version (and higher)</span></span>|
|-|-|-|-|
|<span data-ttu-id="4cc30-122">InPrivate 瀏覽</span><span class="sxs-lookup"><span data-stu-id="4cc30-122">InPrivate Navigation</span></span>|<span data-ttu-id="4cc30-123">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-123">Y</span></span>|<span data-ttu-id="4cc30-124">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-124">Y</span></span>|<span data-ttu-id="4cc30-125">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-125">87</span></span>|
|<span data-ttu-id="4cc30-126">在非使用狀態時重設</span><span class="sxs-lookup"><span data-stu-id="4cc30-126">Reset on inactivity</span></span>|<span data-ttu-id="4cc30-127">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-127">Y</span></span>|<span data-ttu-id="4cc30-128">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-128">Y</span></span>|<span data-ttu-id="4cc30-129">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-129">87</span></span>|
|<span data-ttu-id="4cc30-130">[唯讀網址列](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (原則)</span><span class="sxs-lookup"><span data-stu-id="4cc30-130">[Read only address bar](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (policy)</span></span> |<span data-ttu-id="4cc30-131">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-131">N</span></span>|<span data-ttu-id="4cc30-132">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-132">Y</span></span> |<span data-ttu-id="4cc30-133">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-133">87</span></span>|
|<span data-ttu-id="4cc30-134">[結束時刪除下載](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (原則)</span><span class="sxs-lookup"><span data-stu-id="4cc30-134">[Delete downloads on exit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (policy)</span></span>  | <span data-ttu-id="4cc30-135">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-135">Y</span></span>|<span data-ttu-id="4cc30-136">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-136">Y</span></span> |<span data-ttu-id="4cc30-137">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-137">87</span></span>|
|<span data-ttu-id="4cc30-138">F11 已封鎖 (進入/結束全螢幕)</span><span class="sxs-lookup"><span data-stu-id="4cc30-138">F11 blocked (enter/exit full-screen)</span></span> | <span data-ttu-id="4cc30-139">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-139">Y</span></span> | <span data-ttu-id="4cc30-140">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-140">Y</span></span> | <span data-ttu-id="4cc30-141">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-141">87</span></span> |
|<span data-ttu-id="4cc30-142">F12 已封鎖 (啟動開發人員工具)</span><span class="sxs-lookup"><span data-stu-id="4cc30-142">F12 blocked (launch Developer Tools)</span></span> | <span data-ttu-id="4cc30-143">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-143">Y</span></span> | <span data-ttu-id="4cc30-144">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-144">Y</span></span> | <span data-ttu-id="4cc30-145">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-145">87</span></span> |
| <span data-ttu-id="4cc30-146">支援多個索引標籤</span><span class="sxs-lookup"><span data-stu-id="4cc30-146">Multi tab support</span></span> | <span data-ttu-id="4cc30-147">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-147">N</span></span>| <span data-ttu-id="4cc30-148">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-148">Y</span></span>| <span data-ttu-id="4cc30-149">87</span><span class="sxs-lookup"><span data-stu-id="4cc30-149">87</span></span>|
|<span data-ttu-id="4cc30-150">結束工作階段按鈕</span><span class="sxs-lookup"><span data-stu-id="4cc30-150">End session button</span></span> | <span data-ttu-id="4cc30-151">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-151">N</span></span>| <span data-ttu-id="4cc30-152">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-152">Y</span></span>| <span data-ttu-id="4cc30-153">88</span><span class="sxs-lookup"><span data-stu-id="4cc30-153">88</span></span>|
|<span data-ttu-id="4cc30-154">所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外</span><span class="sxs-lookup"><span data-stu-id="4cc30-154">All internal Microsoft Edge URLs are blocked, except for *edge://downloads* and *edge://print*</span></span> |<span data-ttu-id="4cc30-155">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-155">N</span></span>|<span data-ttu-id="4cc30-156">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-156">Y</span></span>|<span data-ttu-id="4cc30-157">88</span><span class="sxs-lookup"><span data-stu-id="4cc30-157">88</span></span>|
| <span data-ttu-id="4cc30-158">CTRL+N 已封鎖 (開啟新視窗)</span><span class="sxs-lookup"><span data-stu-id="4cc30-158">CTRL+N blocked (open a new window)</span></span> | <span data-ttu-id="4cc30-159">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-159">Y</span></span> | <span data-ttu-id="4cc30-160">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-160">Y</span></span> | <span data-ttu-id="4cc30-161">89</span><span class="sxs-lookup"><span data-stu-id="4cc30-161">89</span></span> |
| <span data-ttu-id="4cc30-162">CTRL+T 已封鎖 (開啟新索引標籤)</span><span class="sxs-lookup"><span data-stu-id="4cc30-162">CTRL+T blocked (open new tab)</span></span> | <span data-ttu-id="4cc30-163">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-163">N</span></span> | <span data-ttu-id="4cc30-164">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-164">Y</span></span> | <span data-ttu-id="4cc30-165">89</span><span class="sxs-lookup"><span data-stu-id="4cc30-165">89</span></span> |
|<span data-ttu-id="4cc30-166">設定及其他 (...) 將只顯示必要的選項</span><span class="sxs-lookup"><span data-stu-id="4cc30-166">Settings and more (...) will display only the required options</span></span>  |<span data-ttu-id="4cc30-167">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-167">N</span></span> |<span data-ttu-id="4cc30-168">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-168">Y</span></span> |<span data-ttu-id="4cc30-169">89</span><span class="sxs-lookup"><span data-stu-id="4cc30-169">89</span></span> |

> [!NOTE]
> <span data-ttu-id="4cc30-170">隨著 kiosk 模式的演進，提供的功能也會增加。</span><span class="sxs-lookup"><span data-stu-id="4cc30-170">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="4cc30-171">使用 kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="4cc30-171">Use kiosk mode features</span></span>

<span data-ttu-id="4cc30-172">使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能：</span><span class="sxs-lookup"><span data-stu-id="4cc30-172">Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="4cc30-173">Kiosk 模式數位/互動式告示板：</span><span class="sxs-lookup"><span data-stu-id="4cc30-173">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="4cc30-174">Kiosk 模式公用瀏覽：</span><span class="sxs-lookup"><span data-stu-id="4cc30-174">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="4cc30-175">額外命令列選項</span><span class="sxs-lookup"><span data-stu-id="4cc30-175">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="4cc30-176">：停用第一個 Microsoft Edge 執行體驗。</span><span class="sxs-lookup"><span data-stu-id="4cc30-176">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="4cc30-177">：在 Microsoft Edge kiosk 模式重設使用者的工作階段之前，變更上次使用者活動的時間 (以分鐘為單位)。</span><span class="sxs-lookup"><span data-stu-id="4cc30-177">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="4cc30-178">支援的值如下：</span><span class="sxs-lookup"><span data-stu-id="4cc30-178">The following values are supported:</span></span>

  - <span data-ttu-id="4cc30-179">預設值</span><span class="sxs-lookup"><span data-stu-id="4cc30-179">Default values</span></span>
    - <span data-ttu-id="4cc30-180">全螢幕 - 關閉</span><span class="sxs-lookup"><span data-stu-id="4cc30-180">Full screen - turned off</span></span>
    - <span data-ttu-id="4cc30-181">公用瀏覽 - 5 分鐘</span><span class="sxs-lookup"><span data-stu-id="4cc30-181">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="4cc30-182">允許的值</span><span class="sxs-lookup"><span data-stu-id="4cc30-182">Allowed values</span></span>
    - <span data-ttu-id="4cc30-183">0 - 關閉計時器</span><span class="sxs-lookup"><span data-stu-id="4cc30-183">0 - turns off the timer</span></span>
    - <span data-ttu-id="4cc30-184">1-1440 分鐘，用於重設閒置時計時器</span><span class="sxs-lookup"><span data-stu-id="4cc30-184">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="4cc30-185">支援 kiosk 模式的原則</span><span class="sxs-lookup"><span data-stu-id="4cc30-185">Support policies for kiosk mode</span></span>

<span data-ttu-id="4cc30-186">使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。</span><span class="sxs-lookup"><span data-stu-id="4cc30-186">Use any of the Microsoft Edge policies listed in the following table to enhance the kiosk experience for the Microsoft Edge kiosk mode type you configure.</span></span> <span data-ttu-id="4cc30-187">若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](https://docs.microsoft.com/deployedge/microsoft-edge-policies)。</span><span class="sxs-lookup"><span data-stu-id="4cc30-187">To learn more about these policies, see [Microsoft Edge – Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies).</span></span>

> [!NOTE]
> <span data-ttu-id="4cc30-188">原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="4cc30-188">Policy configuration isn't limited to the policies listed in the following table, however additional policies should be tested to ensure that kiosk mode functionality isn't negatively affected.</span></span>

|<span data-ttu-id="4cc30-189">群組原則</span><span class="sxs-lookup"><span data-stu-id="4cc30-189">Group policy</span></span>|<span data-ttu-id="4cc30-190">數位/互動式告示板</span><span class="sxs-lookup"><span data-stu-id="4cc30-190">Digital\Interactive signage</span></span>|<span data-ttu-id="4cc30-191">公用瀏覽單一應用程式</span><span class="sxs-lookup"><span data-stu-id="4cc30-191">Public browsing single-app</span></span>|
|--|--|--|
|[<span data-ttu-id="4cc30-192">列印</span><span class="sxs-lookup"><span data-stu-id="4cc30-192">Printing</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | <span data-ttu-id="4cc30-193">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-193">Y</span></span>|<span data-ttu-id="4cc30-194">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-194">Y</span></span> |
|[<span data-ttu-id="4cc30-195">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="4cc30-195">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |<span data-ttu-id="4cc30-196">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-196">N</span></span> | <span data-ttu-id="4cc30-197">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-197">Y</span></span>|
|[<span data-ttu-id="4cc30-198">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="4cc30-198">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |<span data-ttu-id="4cc30-199">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-199">N</span></span> | <span data-ttu-id="4cc30-200">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-200">Y</span></span>|
|[<span data-ttu-id="4cc30-201">NewTabPageLocation</span><span class="sxs-lookup"><span data-stu-id="4cc30-201">NewTabPageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |<span data-ttu-id="4cc30-202">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-202">N</span></span> |<span data-ttu-id="4cc30-203">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-203">Y</span></span> |
|[<span data-ttu-id="4cc30-204">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="4cc30-204">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |<span data-ttu-id="4cc30-205">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-205">N</span></span> |<span data-ttu-id="4cc30-206">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-206">Y</span></span> |
|[<span data-ttu-id="4cc30-207">URLAllowlist</span><span class="sxs-lookup"><span data-stu-id="4cc30-207">URLAllowlist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |<span data-ttu-id="4cc30-208">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-208">Y</span></span> |<span data-ttu-id="4cc30-209">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-209">Y</span></span> |
|[<span data-ttu-id="4cc30-210">URLBlocklist</span><span class="sxs-lookup"><span data-stu-id="4cc30-210">URLBlocklist</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |<span data-ttu-id="4cc30-211">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-211">Y</span></span> | <span data-ttu-id="4cc30-212">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-212">Y</span></span>|
|[<span data-ttu-id="4cc30-213">ManagedSearchEngines</span><span class="sxs-lookup"><span data-stu-id="4cc30-213">ManagedSearchEngines</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |<span data-ttu-id="4cc30-214">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-214">N</span></span> | <span data-ttu-id="4cc30-215">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-215">Y</span></span>|
|[<span data-ttu-id="4cc30-216">UserFeedbackAllowed</span><span class="sxs-lookup"><span data-stu-id="4cc30-216">UserFeedbackAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |<span data-ttu-id="4cc30-217">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-217">N</span></span> | <span data-ttu-id="4cc30-218">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-218">Y</span></span>|
|[<span data-ttu-id="4cc30-219">VerticalTabsAllowed</span><span class="sxs-lookup"><span data-stu-id="4cc30-219">VerticalTabsAllowed</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | <span data-ttu-id="4cc30-220">否</span><span class="sxs-lookup"><span data-stu-id="4cc30-220">N</span></span>|<span data-ttu-id="4cc30-221">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-221">Y</span></span> |
|[<span data-ttu-id="4cc30-222">SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="4cc30-222">SmartScreen settings</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |<span data-ttu-id="4cc30-223">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-223">Y</span></span> |<span data-ttu-id="4cc30-224">是</span><span class="sxs-lookup"><span data-stu-id="4cc30-224">Y</span></span> |

## <span data-ttu-id="4cc30-225">具有受指派存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4cc30-225">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="4cc30-226">單一應用程式 kiosk</span><span class="sxs-lookup"><span data-stu-id="4cc30-226">Single app kiosk</span></span>

<span data-ttu-id="4cc30-227">Microsoft Edge 目前針對單一應用程式受指派的存取權支援一組相同的舊版 Microsoft Edge kiosk 模式類型，包含下列鎖定體驗：數位/互動式告示板和公用瀏覽。</span><span class="sxs-lookup"><span data-stu-id="4cc30-227">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences: Digital/Interactive signage, and Public-browsing.</span></span>  

<span data-ttu-id="4cc30-228">您目前可使用最新的  [Windows 10 測試人員預覽版](https://insider.windows.com/) 20215 版或更新版本，以及  [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download) 87.0.644.4 版或更新版本，測試有受指派存取權的 kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="4cc30-228">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="4cc30-229">如何取得 Windows 測試人員預覽？</span><span class="sxs-lookup"><span data-stu-id="4cc30-229">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="4cc30-230">若要在電腦上安裝 Windows 10 測試人員預覽版，請依照 [開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="4cc30-230">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="4cc30-231">多個應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="4cc30-231">Multi-app kiosk</span></span>

<span data-ttu-id="4cc30-232">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="4cc30-232">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="4cc30-233">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="4cc30-233">To configure Microsoft Edge with multi-app assigned access, follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="4cc30-234">(Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。</span><span class="sxs-lookup"><span data-stu-id="4cc30-234">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="4cc30-235">使用具有受指派的存取權的 Microsoft Edge 時，您可以設定 Microsoft Edge kiosk 模式，以使用 [Microsoft Edge 瀏覽器原則](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies)來設定瀏覽體驗，進而滿足您的獨特需求。</span><span class="sxs-lookup"><span data-stu-id="4cc30-235">When using Microsoft Edge with multi-app assigned access, you can configure Microsoft Edge kiosk to use the[Microsoft Edge browser policies](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="4cc30-236">使用 Windows 設定進行設定</span><span class="sxs-lookup"><span data-stu-id="4cc30-236">Configure using Windows Settings</span></span>

<span data-ttu-id="4cc30-237">Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="4cc30-237">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="4cc30-238">使用下列步驟設定單一應用程式 kiosk 電腦。</span><span class="sxs-lookup"><span data-stu-id="4cc30-238">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="4cc30-239">安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-239">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="4cc30-240">依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="4cc30-240">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="4cc30-241">安裝最新版本的 [Microsoft Edge 穩定通道](https://www.microsoft.com/edge)版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-241">Install the latest version of [Microsoft Edge Stable channel](https://www.microsoft.com/edge), version 87 or higher.</span></span>  <span data-ttu-id="4cc30-242">若要測試最新功能，您可以下載最新的 [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-242">To test the latest features, you can download the latest [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), version 89 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="4cc30-243">由於需要裝置層級安裝，因此僅支援一個非 Canary 通道。</span><span class="sxs-lookup"><span data-stu-id="4cc30-243">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="4cc30-244">在 kiosk 電腦上，開啟 [Windows 設定]，然後在搜尋欄位中輸入「kiosk」。</span><span class="sxs-lookup"><span data-stu-id="4cc30-244">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="4cc30-245">如下一個螢幕擷取畫面所示，選取 \*\* \*\*[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4cc30-245">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. <span data-ttu-id="4cc30-247">在 \*\* ** [設定 kiosk] 頁面上，按一下 ** \*\*[開始使用]。</span><span class="sxs-lookup"><span data-stu-id="4cc30-247">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. <span data-ttu-id="4cc30-249">輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="4cc30-249">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. <span data-ttu-id="4cc30-251">在\*\* ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="4cc30-251">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4cc30-252">這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="4cc30-252">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk 模式 - 選擇應用程式":::

7. <span data-ttu-id="4cc30-254">針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="4cc30-254">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="4cc30-255">數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="4cc30-255">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="4cc30-256">公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="4cc30-256">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

8. <span data-ttu-id="4cc30-258">選取 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="4cc30-258">Select **Next**.</span></span>
9. <span data-ttu-id="4cc30-259">輸入 kiosk 啟動時要載入的 URL。</span><span class="sxs-lookup"><span data-stu-id="4cc30-259">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. <span data-ttu-id="4cc30-261">接受 5 分鐘的閒置時間預設值，或提供您自己的值。</span><span class="sxs-lookup"><span data-stu-id="4cc30-261">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. <span data-ttu-id="4cc30-263">按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="4cc30-263">Click **Next**.</span></span>
12. <span data-ttu-id="4cc30-264">關閉 \*\* \*\* [設定] 視窗，儲存並套用您的選擇。</span><span class="sxs-lookup"><span data-stu-id="4cc30-264">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. <span data-ttu-id="4cc30-266">從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。</span><span class="sxs-lookup"><span data-stu-id="4cc30-266">Sign out from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="4cc30-267">功能限制</span><span class="sxs-lookup"><span data-stu-id="4cc30-267">Functional limitations</span></span>

<span data-ttu-id="4cc30-268">隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。</span><span class="sxs-lookup"><span data-stu-id="4cc30-268">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="4cc30-269">建議您關閉：</span><span class="sxs-lookup"><span data-stu-id="4cc30-269">We recommend that you turn off:</span></span>

- [<span data-ttu-id="4cc30-270">StartupBoostEnabled</span><span class="sxs-lookup"><span data-stu-id="4cc30-270">StartupBoostEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [<span data-ttu-id="4cc30-271">InternetExplorerIntegrationLevel</span><span class="sxs-lookup"><span data-stu-id="4cc30-271">InternetExplorerIntegrationLevel</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [<span data-ttu-id="4cc30-272">Extensions</span><span class="sxs-lookup"><span data-stu-id="4cc30-272">Extensions</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [<span data-ttu-id="4cc30-273">BackgroundModeEnabled</span><span class="sxs-lookup"><span data-stu-id="4cc30-273">BackgroundModeEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## <span data-ttu-id="4cc30-274">藍圖</span><span class="sxs-lookup"><span data-stu-id="4cc30-274">Roadmap</span></span>

### <span data-ttu-id="4cc30-275">2021 年年初</span><span class="sxs-lookup"><span data-stu-id="4cc30-275">In early 2021</span></span>

<span data-ttu-id="4cc30-276">我們將增加下列支援和功能：</span><span class="sxs-lookup"><span data-stu-id="4cc30-276">We'll add the following support and features:</span></span>

- <span data-ttu-id="4cc30-277">在 Windows 10 1909 和更新版本上，具有獲指派存取權單一應用程式之 Microsoft Edge kiosk 模式的正式發行。</span><span class="sxs-lookup"><span data-stu-id="4cc30-277">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows 10 1909 and higher.</span></span>
- <span data-ttu-id="4cc30-278">與舊版 Microsoft Edge 同等的其他功能。</span><span class="sxs-lookup"><span data-stu-id="4cc30-278">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="4cc30-279">與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="4cc30-279">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>
- <span data-ttu-id="4cc30-280">將封鎖其他鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="4cc30-280">Additional keyboard shortcuts will be blocked.</span></span>
- <span data-ttu-id="4cc30-281">限制從瀏覽器啟動其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="4cc30-281">Restrict the launch of other applications from the browser.</span></span>

## <span data-ttu-id="4cc30-282">請參閱</span><span class="sxs-lookup"><span data-stu-id="4cc30-282">See also</span></span>

- [<span data-ttu-id="4cc30-283">設定 Windows 桌面版的 Kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="4cc30-283">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="4cc30-284">部署 Microsoft Edge 舊版 kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="4cc30-284">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="4cc30-285">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="4cc30-285">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="4cc30-286">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="4cc30-286">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
