---
title: 存取舊版 Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何存取舊版 Microsoft Edge。
ms.openlocfilehash: e5a97a487dc6b3a45504a721e460a69103b0174e
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979563"
---
# <span data-ttu-id="3d3df-103">安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版</span><span class="sxs-lookup"><span data-stu-id="3d3df-103">Access Microsoft Edge Legacy after installing the new version of Microsoft Edge</span></span>

<span data-ttu-id="3d3df-104">了解如何在安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版。</span><span class="sxs-lookup"><span data-stu-id="3d3df-104">Learn how to access Microsoft Edge Legacy after installing the new version of Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="3d3df-105">本文適用於 Microsoft Edge [Stable 通道](microsoft-edge-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-105">This article applies to the Microsoft Edge [Stable channel](microsoft-edge-channels.md).</span></span>

<span data-ttu-id="3d3df-106">雖然大多數組織會想要將舊版 Microsoft Edge 取代為新版本，但在某些情況下，使用者可能需要存取兩個版本。</span><span class="sxs-lookup"><span data-stu-id="3d3df-106">While most organizations will want to replace Microsoft Edge Legacy with the new version, there are some situations where users will need access to both versions.</span></span> <span data-ttu-id="3d3df-107">例如：</span><span class="sxs-lookup"><span data-stu-id="3d3df-107">For example:</span></span>

- <span data-ttu-id="3d3df-108">與使用 Microsoft Edge 的其中一個或兩個版本之使用者互動的支援人員。</span><span class="sxs-lookup"><span data-stu-id="3d3df-108">Helpdesk and support staff who interact with users who are using either or both versions of Microsoft Edge.</span></span>
- <span data-ttu-id="3d3df-109">支援使用其中一個或兩個版本的 Microsoft Edge 之客戶的開發人員。</span><span class="sxs-lookup"><span data-stu-id="3d3df-109">Developers who support customers who are using either or both versions of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d3df-110">不建議您在生產環境中並存執行新版 Microsoft Edge 和舊版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-110">Running Microsoft Edge Legacy side-by-side with the new version of Microsoft Edge is not recommended for use in production.</span></span> <span data-ttu-id="3d3df-111">只有在需要同時測試兩個瀏覽器版本的特定情況下，才能使用這個設定。</span><span class="sxs-lookup"><span data-stu-id="3d3df-111">This configuration should only be used in specific cases where testing with both browser versions is required.</span></span>
>
> <span data-ttu-id="3d3df-112">舊版 Microsoft Edge 桌面應用程式將於 2021 年 3 月 9 日終止支援，將有利於新版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-112">The Microsoft Edge Legacy desktop app will reach end of support on March 9, 2021 in favor of the new Microsoft Edge.</span></span> <span data-ttu-id="3d3df-113">這表示舊版 Microsoft Edge 將不會在該日期之後收到安全性更新。</span><span class="sxs-lookup"><span data-stu-id="3d3df-113">This means that Microsoft Edge Legacy will not receive security updates after that date.</span></span> <span data-ttu-id="3d3df-114">這項變更適用於所有在舊版 Microsoft Edge 桌面應用程式中執行的體驗。</span><span class="sxs-lookup"><span data-stu-id="3d3df-114">This change is applicable to all experiences that run in the Microsoft Edge Legacy desktop app.</span></span> <span data-ttu-id="3d3df-115">[進一步瞭解](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-115">[Learn more](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666).</span></span>

## <span data-ttu-id="3d3df-116">開始之前</span><span class="sxs-lookup"><span data-stu-id="3d3df-116">Before you begin</span></span>

<span data-ttu-id="3d3df-117">本文的程序適用於已使用最新安全性更新來更新的系統。</span><span class="sxs-lookup"><span data-stu-id="3d3df-117">The procedures in this article apply to systems that have been updated with the latest security updates.</span></span> <span data-ttu-id="3d3df-118">安裝新版本 Microsoft Edge 後，將會隱藏舊版本 (Microsoft Edge 舊版)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-118">When the new version of Microsoft Edge is installed, the old version (Microsoft Edge Legacy) will be hidden.</span></span> <span data-ttu-id="3d3df-119">根據預設，所有對舊版本的嘗試啟動都會將使用者重新導向至新安裝的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-119">By default, all attempts to launch the old version will redirect the user to the newly installed version of Microsoft Edge.</span></span> <span data-ttu-id="3d3df-120">本文說明如何在安裝 Microsoft Edge 後繼續使用舊版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-120">This article describes how you can keep using Microsoft Edge Legacy after you install Microsoft Edge.</span></span>

## <span data-ttu-id="3d3df-121">快速入門：使用 Microsoft Edge Beta 通道和舊版 Microsoft Edge 並存體驗</span><span class="sxs-lookup"><span data-stu-id="3d3df-121">Quickstart: Side-by-side experience with Microsoft Edge Beta Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="3d3df-122">在使用本文中的詳細指示之前，請考慮下列兩個步驟，讓您的使用者能夠並存執行舊版 Microsoft Edge 和 Microsoft Edge [Beta 頻道](microsoft-edge-channels.md)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-122">Before using the detailed instructions in this article, consider the following two steps to let your users run Microsoft Edge Legacy and the Microsoft Edge [Beta channel](microsoft-edge-channels.md) side-by-side.</span></span>

1. <span data-ttu-id="3d3df-123">防止 [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq) 自動安裝 Microsoft Edge 的 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="3d3df-123">Prevent the automatic install of the Stable Channel of Microsoft Edge by [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq).</span></span>

   > [!TIP]
   > <span data-ttu-id="3d3df-124">使用[封鎖程式工具組](microsoft-edge-blocker-toolkit.md)來停用自動傳遞 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-124">Use the [Blocker Toolkit](microsoft-edge-blocker-toolkit.md) to disable automatic delivery of Microsoft Edge.</span></span>

2. <span data-ttu-id="3d3df-125">安裝新版 Microsoft Edge 的[Beta 通道](https://www.microsoft.com/edge/business/download)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-125">Install the [Beta channel](https://www.microsoft.com/edge/business/download) of the new version of Microsoft Edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3d3df-126">如需有關登錄機碼設定的詳細資訊，請參閱[其他資訊](#additional-information)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-126">Read [Additional information](#additional-information) for information about Registry Key settings.</span></span>

<span data-ttu-id="3d3df-127">這種並存解決方案較不復雜，且需要的管理比本文所述的詳細解決方案更少。</span><span class="sxs-lookup"><span data-stu-id="3d3df-127">This side-by-side solution is less complex and requires less management than the detailed solution described in this article.</span></span> <span data-ttu-id="3d3df-128">但是，這種解決方案代表您將執行 Beta 通道，而不是 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="3d3df-128">However, this solution does mean that you'll be running the Beta Channel rather than the Stable Channel.</span></span>

## <span data-ttu-id="3d3df-129">使用 Microsoft Edge 穩定通道和舊版 Microsoft Edge 的並存體驗</span><span class="sxs-lookup"><span data-stu-id="3d3df-129">Side-by-side experience with Microsoft Edge Stable Channel and Microsoft Edge Legacy</span></span>

<span data-ttu-id="3d3df-130">在系統層級安裝下一版 Microsoft Edge 的穩定通道，就會隱藏目前版本 (Microsoft Edge 舊版)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-130">Installing the Stable Channel of the next version of Microsoft Edge at the system-level will cause the current version (Microsoft Edge Legacy) to be hidden.</span></span> <span data-ttu-id="3d3df-131">如果您想要讓您的使用者在 Windows 中並存看到兩個版本的 Microsoft Edge，您可以將 **[允許 Microsoft Edge 並存瀏覽器經驗]** 群組原則設定為 **[啟用]** 來啟用此體驗。</span><span class="sxs-lookup"><span data-stu-id="3d3df-131">If you want to let your users see both versions of Microsoft Edge side by side in Windows, you can enable this experience by setting the **Allow Microsoft Edge Side by Side browser experience** group policy to **Enabled**.</span></span>

<span data-ttu-id="3d3df-132">此群組原則記錄於[此處](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span><span class="sxs-lookup"><span data-stu-id="3d3df-132">This group policy is documented [here](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)</span></span>

### <span data-ttu-id="3d3df-133">若要設定並存瀏覽器體驗原則：</span><span class="sxs-lookup"><span data-stu-id="3d3df-133">To set up the side-by-side browser experience policy:</span></span>

1. <span data-ttu-id="3d3df-134">安裝 [Microsoft Edge For Business](https://www.microsoft.com/edge/business/download) 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="3d3df-134">Install the Policy Definitions from [Microsoft Edge for Business](https://www.microsoft.com/edge/business/download).</span></span>

   - <span data-ttu-id="3d3df-135">挑選您想要使用的通道/組建及平台，然後按一下 [取得原則檔案]。</span><span class="sxs-lookup"><span data-stu-id="3d3df-135">Pick the CHANNEL/BUILD and PLATFORM you want to use, and then click GET POLICY FILES.</span></span>
   - <span data-ttu-id="3d3df-136">將壓縮的檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="3d3df-136">Extract the zipped files.</span></span>
   - <span data-ttu-id="3d3df-137">將 msedge.admx 和 msedgeupdate.admx 複製到 `C:\Windows\PolicyDefinitions` 目錄中。</span><span class="sxs-lookup"><span data-stu-id="3d3df-137">Copy msedge.admx and msedgeupdate.admx to the `C:\Windows\PolicyDefinitions` directory.</span></span>
   - <span data-ttu-id="3d3df-138">將 msedge.adml 和 msedgeupdate.adml (來自適當語言/地區目錄) 複製到 `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` 目錄。</span><span class="sxs-lookup"><span data-stu-id="3d3df-138">Copy msedge.adml and msedgeupdate.adml (from the appropriate language/locale directory) to the `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` directory.</span></span>

2. <span data-ttu-id="3d3df-139">開啟群組原則編輯器 (gpedit.msc)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-139">Open the Group Policy Editor (gpedit.msc).</span></span>
3. <span data-ttu-id="3d3df-140">在**電腦設定**下，移至*系統管理範本>Microsoft Edge Update>應用程式*。</span><span class="sxs-lookup"><span data-stu-id="3d3df-140">Under **Computer Configuration**, go to *Administrative Templates>Microsoft Edge Update>Applications*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d3df-141">如果您沒有看到 *[Microsoft Edge 更新]* 資料夾，請確認步驟 1 已正確完成。</span><span class="sxs-lookup"><span data-stu-id="3d3df-141">If you don't see the *Microsoft Edge Update* folder, verify that step 1 was completed correctly.</span></span>

4. <span data-ttu-id="3d3df-142">在**應用程式**下，按兩下 [允許 Microsoft Edge 並排瀏覽器體驗]。</span><span class="sxs-lookup"><span data-stu-id="3d3df-142">Under **Applications**, double-click "Allow Microsoft Edge Side by Side browser experience".</span></span> <span data-ttu-id="3d3df-143">在繼續下一步之前，請參閱我們的[最佳作法指導方針](#best-practice-guidance)。</span><span class="sxs-lookup"><span data-stu-id="3d3df-143">See our [best practice guidance](#best-practice-guidance) before continuing to the next step.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3d3df-144">預設情況下，此群組原則設定為 [未設定]，這將導致在安裝新版本 Microsoft Edge 後隱藏 Microsoft Edge 舊版。</span><span class="sxs-lookup"><span data-stu-id="3d3df-144">By default, this group policy is set to "Not configured", which results in Microsoft Edge Legacy being hidden when the new version of Microsoft Edge is installed.</span></span>

5. <span data-ttu-id="3d3df-145">選取**啟用**，然後按一下**確定**。</span><span class="sxs-lookup"><span data-stu-id="3d3df-145">Select **Enabled** and then click **OK**.</span></span>  

<span data-ttu-id="3d3df-146">設定此原則會將下列登錄機碼設定為「00000001」：</span><span class="sxs-lookup"><span data-stu-id="3d3df-146">Setting this policy will set the following Registry Key  to '00000001':</span></span>

- <span data-ttu-id="3d3df-147">索引鍵：</span><span class="sxs-lookup"><span data-stu-id="3d3df-147">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- <span data-ttu-id="3d3df-148">數值名稱：</span><span class="sxs-lookup"><span data-stu-id="3d3df-148">Value Name:</span></span> `Allowsxs`
- <span data-ttu-id="3d3df-149">數值類型:</span><span class="sxs-lookup"><span data-stu-id="3d3df-149">Value Type:</span></span> `'REG_DWORD'`

#### <span data-ttu-id="3d3df-150">最佳作法指導方針</span><span class="sxs-lookup"><span data-stu-id="3d3df-150">Best practice guidance</span></span>

<span data-ttu-id="3d3df-151">為獲得最佳體驗，應在將新版本 Microsoft Edge 部署到使用者裝置之前，先啟用**允許 Microsoft Edge 並排瀏覽器體驗**。</span><span class="sxs-lookup"><span data-stu-id="3d3df-151">For the best experience, the **Allow Microsoft Edge Side by Side browser experience** should be enabled before the new version of Microsoft Edge is deployed to your users' devices.</span></span>

<span data-ttu-id="3d3df-152">如果在部署 Microsoft Edge 後才啟用群組原則，會產生以下副作用且需執行以下動作：</span><span class="sxs-lookup"><span data-stu-id="3d3df-152">If the group policy is enabled after Microsoft Edge is deployed, there are the following side effects and required actions:</span></span>

1. <span data-ttu-id="3d3df-153">在新版本 Microsoft Edge 的安裝程式再次執行之前，**允許 Microsoft Edge 並排瀏覽器體驗**不會生效。</span><span class="sxs-lookup"><span data-stu-id="3d3df-153">**Allow Microsoft Edge Side by Side browser experience** won't take effect until after the installer for the new version of Microsoft Edge is run again.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3d3df-154">當新版本 Microsoft Edge 更新時，安裝程式可以直接或自動執行。</span><span class="sxs-lookup"><span data-stu-id="3d3df-154">The installer can be run directly or automatically when the new version of Microsoft Edge updates.</span></span>

2. <span data-ttu-id="3d3df-155">需要將 Microsoft Edge 舊版重新釘選到 [開始] 或 [工作列]，因為部署新版本 Microsoft Edge 時已移轉釘選。</span><span class="sxs-lookup"><span data-stu-id="3d3df-155">Microsoft Edge Legacy will need to be re-pinned to Start or the Taskbar because the pin is migrated when the new version of Microsoft Edge is deployed.</span></span>
3. <span data-ttu-id="3d3df-156">為 Microsoft Edge 舊版釘選到 [開始] 或 [工作列] 的網站將移轉至新版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-156">Sites that were pinned to Start or the Taskbar for Microsoft Edge Legacy will be migrated to the new version of Microsoft Edge.</span></span>

## <span data-ttu-id="3d3df-157">其他資訊</span><span class="sxs-lookup"><span data-stu-id="3d3df-157">Additional information</span></span>

<span data-ttu-id="3d3df-158">完全更新系統並安裝下一版 Microsoft Edge 的 Stable 通道後，系統將設定以下登錄機碼和值：</span><span class="sxs-lookup"><span data-stu-id="3d3df-158">After the systems are fully updated and the Stable channel of the next version of Microsoft Edge is installed, the following registry key and value is set:</span></span>

- <span data-ttu-id="3d3df-159">索引鍵：</span><span class="sxs-lookup"><span data-stu-id="3d3df-159">Key:</span></span> `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- <span data-ttu-id="3d3df-160">機碼值：</span><span class="sxs-lookup"><span data-stu-id="3d3df-160">Key value:</span></span> `BrowserReplacement`

  > [!IMPORTANT]
  > <span data-ttu-id="3d3df-161">每次更新 Microsoft Edge Stable 通道時，此機碼都會被覆寫。</span><span class="sxs-lookup"><span data-stu-id="3d3df-161">This key is over-written every time the Microsoft Edge Stable channel is updated.</span></span> <span data-ttu-id="3d3df-162">我們建議的最佳做法是「不要」刪除此機碼，以允許使用者同時存取兩個版本的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="3d3df-162">As a best practice, we recommend that you DO NOT delete this key to allow users to access both versions of Microsoft Edge.</span></span>

## <span data-ttu-id="3d3df-163">請參閱</span><span class="sxs-lookup"><span data-stu-id="3d3df-163">See also</span></span>

- [<span data-ttu-id="3d3df-164">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3d3df-164">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3d3df-165">支援 Microsoft Edge 的 Windows 更新</span><span class="sxs-lookup"><span data-stu-id="3d3df-165">Windows updates to support Microsoft Edge</span></span>](microsoft-edge-sysupdate-windows-updates.md)
