---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 10/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge kiosk 模式
ms.openlocfilehash: 799b3dd4b7fc96f0b8e5cb718bca98fd4f38ec15
ms.sourcegitcommit: 78905f66f4a6590a57c8f2bf808af92106b62996
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094860"
---
# <span data-ttu-id="59efa-103">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="59efa-103">Configure Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="59efa-104">本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="59efa-104">This article describes how to configure Microsoft Edge kiosk mode options that you can pilot.</span></span> <span data-ttu-id="59efa-105">另外，功能藍圖也是我們的目標。</span><span class="sxs-lookup"><span data-stu-id="59efa-105">There's also a roadmap of features we are targeting.</span></span>

> [!NOTE]
> <span data-ttu-id="59efa-106">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="59efa-106">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="59efa-107">概觀</span><span class="sxs-lookup"><span data-stu-id="59efa-107">Overview</span></span>

<span data-ttu-id="59efa-108">Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。</span><span class="sxs-lookup"><span data-stu-id="59efa-108">Microsoft Edge kiosk mode offers two lockdown experiences of the browser so organizations can create, manage, and provide the best experience for their customers.</span></span> <span data-ttu-id="59efa-109">可使用的鎖定體驗如下：</span><span class="sxs-lookup"><span data-stu-id="59efa-109">The following lockdown experiences are available:</span></span>  

- <span data-ttu-id="59efa-110">數位/互動式告示板體驗以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="59efa-110">The Digital/Interactive signage experience displays a specific site in full-screen mode.</span></span>
- <span data-ttu-id="59efa-111">公用瀏覽體驗執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="59efa-111">The public-browsing experience runs a limited multi-tab version of Microsoft Edge.</span></span>

<span data-ttu-id="59efa-112">兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="59efa-112">Both experiences are running a Microsoft Edge InPrivate session, which protects user data.</span></span>

## <span data-ttu-id="59efa-113">設定 Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="59efa-113">Set up Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="59efa-114">您現在可以使用 Microsoft Edge Canary 通道版本 87 測試最初的 kiosk 模式功能組。</span><span class="sxs-lookup"><span data-stu-id="59efa-114">An initial set of kiosk mode features are now available to test with Microsoft Edge Canary Channel, version 87.</span></span> <span data-ttu-id="59efa-115">您可以從[ ](https://www.microsoftedgeinsider.com/download)[Microsoft Edge Insider Channels] 頁面下載 Microsoft Edge Canary。</span><span class="sxs-lookup"><span data-stu-id="59efa-115">You can download Microsoft Edge Canary from the [Microsoft Edge Insider Channels](https://www.microsoftedgeinsider.com/download) page.</span></span>

### <span data-ttu-id="59efa-116">Kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="59efa-116">Kiosk mode features</span></span>

<span data-ttu-id="59efa-117">下列功能可供使用：</span><span class="sxs-lookup"><span data-stu-id="59efa-117">The following features are available:</span></span>

- <span data-ttu-id="59efa-118">InPrivate 導覽在工作階段結束時會刪除瀏覽器資料和下載項目，保護使用者資料。</span><span class="sxs-lookup"><span data-stu-id="59efa-118">InPrivate navigation protects user data by deleting browser data and downloads when the session ends.</span></span>
- <span data-ttu-id="59efa-119">設定結束時刪除下載項目的原則。</span><span class="sxs-lookup"><span data-stu-id="59efa-119">A policy to configure Delete downloads on exit.</span></span>
- <span data-ttu-id="59efa-120">重設使用者工作階段在閒置一段時間後的選項。</span><span class="sxs-lookup"><span data-stu-id="59efa-120">The option to reset a user session after a certain period of inactivity.</span></span>
- <span data-ttu-id="59efa-121">一組初始的鎖定功能。</span><span class="sxs-lookup"><span data-stu-id="59efa-121">An initial set of lockdown functionality.</span></span> <span data-ttu-id="59efa-122">可用功能如下：</span><span class="sxs-lookup"><span data-stu-id="59efa-122">The following functions are available:</span></span>

  - <span data-ttu-id="59efa-123">滑鼠快顯功能表</span><span class="sxs-lookup"><span data-stu-id="59efa-123">Mouse context menu</span></span>
  - <span data-ttu-id="59efa-124">F12 開發人員工具</span><span class="sxs-lookup"><span data-stu-id="59efa-124">F12 Developer Tools</span></span>
  - <span data-ttu-id="59efa-125">F11 退出全螢幕 (在全螢幕模式時)</span><span class="sxs-lookup"><span data-stu-id="59efa-125">F11 Exit full screen (while in full screen mode)</span></span>
  - <span data-ttu-id="59efa-126">封鎖最初一組 *Edge://* 頁面</span><span class="sxs-lookup"><span data-stu-id="59efa-126">Blocking of the initial set of *Edge://* pages</span></span>

> [!NOTE]
> <span data-ttu-id="59efa-127">Kiosk 模式會逐漸演變，提供的功能也會增加。</span><span class="sxs-lookup"><span data-stu-id="59efa-127">As kiosk mode evolves, more features will be available.</span></span>

## <span data-ttu-id="59efa-128">使用 kiosk 模式功能</span><span class="sxs-lookup"><span data-stu-id="59efa-128">Use kiosk mode features</span></span>

<span data-ttu-id="59efa-129">使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能：</span><span class="sxs-lookup"><span data-stu-id="59efa-129">You can invoke Microsoft Edge kiosk mode features can be invoked with the following Windows 10 command line options:</span></span>

- <span data-ttu-id="59efa-130">Kiosk 模式數位/互動式告示板：</span><span class="sxs-lookup"><span data-stu-id="59efa-130">Kiosk mode Digital/Interactive signage:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- <span data-ttu-id="59efa-131">Kiosk 模式公用瀏覽：</span><span class="sxs-lookup"><span data-stu-id="59efa-131">Kiosk mode public browsing:</span></span> `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### <span data-ttu-id="59efa-132">額外命令列選項</span><span class="sxs-lookup"><span data-stu-id="59efa-132">Additional command line options</span></span>

- `--no-first-run` <span data-ttu-id="59efa-133">：停用第一個 Microsoft Edge 執行體驗。</span><span class="sxs-lookup"><span data-stu-id="59efa-133">: Disable the first Microsoft Edge run experience.</span></span>
- `--kiosk-idle-timeout-minutes` <span data-ttu-id="59efa-134">：在 Microsoft Edge kiosk 模式重設使用者的工作階段之前，變更上次使用者活動的時間 (以分鐘為單位)。</span><span class="sxs-lookup"><span data-stu-id="59efa-134">: Change the time (in minutes) from the last user activity before Microsoft Edge kiosk mode resets the user's session.</span></span> <span data-ttu-id="59efa-135">支援的值如下：</span><span class="sxs-lookup"><span data-stu-id="59efa-135">The following values are supported:</span></span>

  - <span data-ttu-id="59efa-136">預設值</span><span class="sxs-lookup"><span data-stu-id="59efa-136">Default values</span></span>
    - <span data-ttu-id="59efa-137">全螢幕 - 關閉</span><span class="sxs-lookup"><span data-stu-id="59efa-137">Full screen - turned off</span></span>
    - <span data-ttu-id="59efa-138">公用瀏覽 - 5 分鐘</span><span class="sxs-lookup"><span data-stu-id="59efa-138">Public browsing - 5 minutes</span></span>
  - <span data-ttu-id="59efa-139">允許的值</span><span class="sxs-lookup"><span data-stu-id="59efa-139">Allowed values</span></span>
    - <span data-ttu-id="59efa-140">0 - 關閉計時器</span><span class="sxs-lookup"><span data-stu-id="59efa-140">0 - turns off the timer</span></span>
    - <span data-ttu-id="59efa-141">在閒置計時器重設為 1-1440 分鐘</span><span class="sxs-lookup"><span data-stu-id="59efa-141">1-1440 minutes for reset on idle timer</span></span>

## <span data-ttu-id="59efa-142">具有受指派的存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="59efa-142">Microsoft Edge with assigned access</span></span>

### <span data-ttu-id="59efa-143">單一應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="59efa-143">Single app kiosk</span></span>

<span data-ttu-id="59efa-144">Microsoft Edge 目前針對單一應用程式受指派的存權支援一組相同的舊版 Microsoft Edge kiosk 模式類型，包含下列鎖定體驗、數位/互動式告示板和公用瀏覽。</span><span class="sxs-lookup"><span data-stu-id="59efa-144">Microsoft Edge currently supports a subset of the same Microsoft Edge Legacy kiosk mode types for single-app assigned access with the following lockdown experiences, Digital/Interactive signage and Public-browsing.</span></span>  

<span data-ttu-id="59efa-145">您目前可使用最新的  [Windows 10 測試人員預覽版](https://insider.windows.com/) 20215 版或更新版本，以及  [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download) 87.0.644.4 版或更新版本，測試有受指派存取權的 kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="59efa-145">Kiosk mode with assigned access is currently available for testing with the latest [Windows 10 Insider Preview Build](https://insider.windows.com/), version 20215 or higher, and with the [Microsoft Edge Dev Channel](https://www.microsoftedgeinsider.com/download), version 87.0.644.4 or higher.</span></span>

**<span data-ttu-id="59efa-146">如何取得 Windows 測試人員預覽？</span><span class="sxs-lookup"><span data-stu-id="59efa-146">How do I get the Windows Insiders preview?</span></span>**

<span data-ttu-id="59efa-147">若要在電腦上安裝 Windows 10 測試人員預覽版，請依照 [開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="59efa-147">To install a Windows 10 Insider Preview Build on a PC, follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>

### <span data-ttu-id="59efa-148">多個應用程式 Kiosk</span><span class="sxs-lookup"><span data-stu-id="59efa-148">Multi-app kiosk</span></span>

<span data-ttu-id="59efa-149">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="59efa-149">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing" kiosk mode type.</span></span> <span data-ttu-id="59efa-150">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="59efa-150">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="59efa-151">(Microsoft Edge Stable 通道的 AUMID 是 **MSEdge**)。</span><span class="sxs-lookup"><span data-stu-id="59efa-151">(The AUMID for the Microsoft Edge Stable channel is **MSEdge**).</span></span>

<span data-ttu-id="59efa-152">設定 Microsoft Edge kiosk 模式 使用具有受指派的存取權的 Microsoft Edge 時，您可以使用 [Microsoft Edge 瀏覽器原則](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies)來設定瀏覽體驗，以滿足您的獨特要求。</span><span class="sxs-lookup"><span data-stu-id="59efa-152">Configure Microsoft Edge kiosk mode When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](https://review.docs.microsoft.com/en-us/DeployEdge/microsoft-edge-policies) to configure the browsing experience to meet your unique requirements.</span></span>

### <span data-ttu-id="59efa-153">使用 Windows 設定進行設定</span><span class="sxs-lookup"><span data-stu-id="59efa-153">Configure using Windows Settings</span></span>

<span data-ttu-id="59efa-154">Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="59efa-154">Windows Settings is the simplest way to set up one or two single-app kiosk devices.</span></span> <span data-ttu-id="59efa-155">使用下列步驟設定單一應用程式 kiosk 電腦。</span><span class="sxs-lookup"><span data-stu-id="59efa-155">Use the following steps to set up a single-app kiosk computer.</span></span>

1. <span data-ttu-id="59efa-156">安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="59efa-156">Install the latest Windows 10 Insider Preview, version 20215 or higher.</span></span> <span data-ttu-id="59efa-157">請依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="59efa-157">Follow the instructions in [Getting started with Windows 10 Insider Preview Builds](https://docs.microsoft.com/windows-insider/get-started).</span></span>
2. <span data-ttu-id="59efa-158">安裝最新版的 [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download)，87.0.644.4 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="59efa-158">Install the latest version of [Microsoft Edge Dev channel](https://www.microsoftedgeinsider.com/download), 87.0.644.4 or higher.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="59efa-159">由於需要裝置層級安裝，因此僅支援一個非 Canary 通道。</span><span class="sxs-lookup"><span data-stu-id="59efa-159">Because a device level installation is required, only a non-Canary channel is supported.</span></span>

3. <span data-ttu-id="59efa-160">在 kiosk 電腦上，開啟 [Windows 設定]，然後在搜尋欄位中輸入「kiosk」。</span><span class="sxs-lookup"><span data-stu-id="59efa-160">On the kiosk computer, open Windows Settings, and type "kiosk" in the search field.</span></span> <span data-ttu-id="59efa-161">如下一個螢幕擷取畫面所示，選取 \*\* \*\*[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="59efa-161">Select  **Set up a kiosk (assigned access)**, shown in the next screenshot to open the dialog for creating the kiosk.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. <span data-ttu-id="59efa-163">在 \*\* ** [設定 kiosk] 頁面上，按一下 ** \*\*[開始使用]。</span><span class="sxs-lookup"><span data-stu-id="59efa-163">On the **Set up a kiosk** page, click **Get started**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="設定有受指派存取權的 kiosk":::

5. <span data-ttu-id="59efa-165">輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="59efa-165">Type a name to create a new kiosk account or choose an existing account from the populated dropdown list and then click **Next**.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="設定有受指派存取權的 kiosk":::

6. <span data-ttu-id="59efa-167">在\*\* ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="59efa-167">On the **Choose a kiosk app** page, select **Microsoft Edge** and then click **Next**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="59efa-168">這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="59efa-168">This only applies to Microsoft Edge Dev, Beta, and Stable channels.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="設定有受指派存取權的 kiosk":::

7. <span data-ttu-id="59efa-170">針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="59efa-170">Pick one of the following options for how Microsoft Edge displays when running in kiosk mode:</span></span>

   - <span data-ttu-id="59efa-171">數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。</span><span class="sxs-lookup"><span data-stu-id="59efa-171">Digital/Interactive signage - Displays a specific site in full-screen mode, running Microsoft Edge.</span></span>
   - <span data-ttu-id="59efa-172">公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。</span><span class="sxs-lookup"><span data-stu-id="59efa-172">Public browser - Runs a limited multi-tab version of Microsoft Edge.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="設定有受指派存取權的 kiosk":::

8. <span data-ttu-id="59efa-174">選取 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="59efa-174">Select **Next**.</span></span>
9. <span data-ttu-id="59efa-175">輸入 kiosk 啟動時要載入的 URL。</span><span class="sxs-lookup"><span data-stu-id="59efa-175">Type the URL to load when the kiosk launches.</span></span>

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="設定有受指派存取權的 kiosk":::

10. <span data-ttu-id="59efa-177">接受 5 分鐘的閒置時間預設值，或提供您自己的值。</span><span class="sxs-lookup"><span data-stu-id="59efa-177">Accept the default value of 5 minutes for the idle time or provide a value of your own.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="設定有受指派存取權的 kiosk":::

11. <span data-ttu-id="59efa-179">按 \*\* \*\*[下一步]。</span><span class="sxs-lookup"><span data-stu-id="59efa-179">Click **Next**.</span></span>
12. <span data-ttu-id="59efa-180">關閉 \*\* \*\* [設定] 視窗，儲存並套用您的選擇。</span><span class="sxs-lookup"><span data-stu-id="59efa-180">Close the **Settings** window to save and apply your choices.</span></span>

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="設定有受指派存取權的 kiosk":::

13. <span data-ttu-id="59efa-182">從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，驗證設定。</span><span class="sxs-lookup"><span data-stu-id="59efa-182">Sign off from the kiosk device and sign in with the local kiosk account to validate the configuration.</span></span>

## <span data-ttu-id="59efa-183">功能限制</span><span class="sxs-lookup"><span data-stu-id="59efa-183">Functional limitations</span></span>

<span data-ttu-id="59efa-184">推出這個預覽版 kiosk 模式時，我們會持續改善產品並增加新功能。</span><span class="sxs-lookup"><span data-stu-id="59efa-184">With the release of this preview version of kiosk mode we're continuing work on improving the product and adding new features.</span></span>

<span data-ttu-id="59efa-185">雖然 kiosk 模式目前不支援下列功能，但是下列功能正在開發中：</span><span class="sxs-lookup"><span data-stu-id="59efa-185">Although kiosk mode doesn't currently support the following functionality, work is underway on the following features:</span></span>

- <span data-ttu-id="59efa-186">集合</span><span class="sxs-lookup"><span data-stu-id="59efa-186">Collections</span></span>
- <span data-ttu-id="59efa-187">Extensions</span><span class="sxs-lookup"><span data-stu-id="59efa-187">Extensions</span></span>
- <span data-ttu-id="59efa-188">Internet Explorer 模式</span><span class="sxs-lookup"><span data-stu-id="59efa-188">Internet Explorer mode</span></span>
- <span data-ttu-id="59efa-189">Windows Defender 應用程式防護 (WDAG)</span><span class="sxs-lookup"><span data-stu-id="59efa-189">Windows Defender Application Guard (WDAG)</span></span>

## <span data-ttu-id="59efa-190">藍圖</span><span class="sxs-lookup"><span data-stu-id="59efa-190">Roadmap</span></span>

### <span data-ttu-id="59efa-191">今年下半年 (2020)</span><span class="sxs-lookup"><span data-stu-id="59efa-191">Later this year (2020)</span></span>

<span data-ttu-id="59efa-192">我們會增加下列功能：</span><span class="sxs-lookup"><span data-stu-id="59efa-192">We'll add the following features:</span></span>

- <span data-ttu-id="59efa-193">結束工作階段按鈕</span><span class="sxs-lookup"><span data-stu-id="59efa-193">End session button</span></span>
- <span data-ttu-id="59efa-194">唯讀網址列</span><span class="sxs-lookup"><span data-stu-id="59efa-194">Read only address bar</span></span>  
  - <span data-ttu-id="59efa-195">可使用群組原則設定</span><span class="sxs-lookup"><span data-stu-id="59efa-195">Configurable with group policy</span></span>
  - <span data-ttu-id="59efa-196">啟用時，使用者無法編輯網址列和瀏覽其他頁面。</span><span class="sxs-lookup"><span data-stu-id="59efa-196">When enabled, users will be prevented from editing the address bar and navigating to another page.</span></span>

- <span data-ttu-id="59efa-197">更多鎖定功能：</span><span class="sxs-lookup"><span data-stu-id="59efa-197">More lockdown functions:</span></span>

  - <span data-ttu-id="59efa-198">封鎖更多加速器 (例如，CTRL+N)</span><span class="sxs-lookup"><span data-stu-id="59efa-198">Additional accelerators will be blocked (for example, CTRL+N)</span></span>
  - <span data-ttu-id="59efa-199">「...」設定功能表只會啟用必要的選項 (例如列印、說明、意見反應和 大聲朗讀)</span><span class="sxs-lookup"><span data-stu-id="59efa-199">The "…" settings menu will enable only required options (for example, Print, Help,  Feedback, and Read aloud)</span></span>
  - <span data-ttu-id="59efa-200">其他 *edge://* 頁面鎖定 (例如 *edge://settings*)</span><span class="sxs-lookup"><span data-stu-id="59efa-200">Additional *edge://* pages lockdown (for example, *edge://settings*)</span></span>
  - <span data-ttu-id="59efa-201">設定列印選項 UI</span><span class="sxs-lookup"><span data-stu-id="59efa-201">Configure print options UI</span></span>
  - <span data-ttu-id="59efa-202">將檔案總管限制為僅限下載資料夾。</span><span class="sxs-lookup"><span data-stu-id="59efa-202">Limiting file explorer to the download folder only.</span></span>

### <span data-ttu-id="59efa-203">2021 年初</span><span class="sxs-lookup"><span data-stu-id="59efa-203">In early 2021</span></span>

<span data-ttu-id="59efa-204">我們會增加下列支援和功能：</span><span class="sxs-lookup"><span data-stu-id="59efa-204">We'll add the following support and features:</span></span>

- <span data-ttu-id="59efa-205">在 Windows 正式發行有受指派存取權單一應用程式的 Microsoft Edge kiosk 模式。</span><span class="sxs-lookup"><span data-stu-id="59efa-205">General availability of Microsoft Edge kiosk mode with assigned access single app on Windows.</span></span>
- <span data-ttu-id="59efa-206">與 Microsoft Edge 舊版具有其他相同功能。</span><span class="sxs-lookup"><span data-stu-id="59efa-206">Additional features for parity with Microsoft Edge Legacy.</span></span>
- <span data-ttu-id="59efa-207">與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。</span><span class="sxs-lookup"><span data-stu-id="59efa-207">Integration with Intune to configure devices using kiosk mode profile UX.</span></span>

## <span data-ttu-id="59efa-208">請參閱</span><span class="sxs-lookup"><span data-stu-id="59efa-208">See also</span></span>

- [<span data-ttu-id="59efa-209">設定 Windows 桌面版的 Kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="59efa-209">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="59efa-210">部署 Microsoft Edge 舊版 kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="59efa-210">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode)
- [<span data-ttu-id="59efa-211">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="59efa-211">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="59efa-212">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="59efa-212">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
