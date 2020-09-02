---
title: 適用於企業的 Microsoft Edge 復原
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 如何將 Microsoft Edge 復原到舊版
ms.openlocfilehash: 9af0881a079dd3059e567eaadb912b3d929924c4
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979517"
---
# <span data-ttu-id="d3227-103">如何將 Microsoft Edge 復原到舊版</span><span class="sxs-lookup"><span data-stu-id="d3227-103">How to roll back Microsoft Edge to a previous version</span></span>

<span data-ttu-id="d3227-104">本文將說明如何使用 [復原] 功能還原為舊版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="d3227-104">This article describes how to roll back to a previous version of Microsoft Edge using the rollback feature.</span></span>

>[!NOTE]
><span data-ttu-id="d3227-105">本文適用於 Microsoft Edge 版本 86 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="d3227-106">復原簡介</span><span class="sxs-lookup"><span data-stu-id="d3227-106">Introduction to rollback</span></span>

<span data-ttu-id="d3227-107">復原可讓您以較舊的版本取代您的 Microsoft Edge 瀏覽器版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-107">Rollback lets you replace your Microsoft Edge browser version with an earlier version.</span></span> <span data-ttu-id="d3227-108">這項功能旨在成為部署 Microsoft Edge 之企業的安全網。</span><span class="sxs-lookup"><span data-stu-id="d3227-108">This feature is designed to be a safety net for enterprises deploying Microsoft Edge.</span></span> <span data-ttu-id="d3227-109">它可讓您針對 Microsoft Edge 問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="d3227-109">It provides a way to troubleshoot issues with Microsoft Edge.</span></span> <span data-ttu-id="d3227-110">復原的好處在於能夠輕鬆快速地復原到舊版的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="d3227-110">The benefits of rollback are the ability to revert to previous browser version easily and quickly.</span></span> <span data-ttu-id="d3227-111">「復原」降低 Microsoft Edge 問題對商務運作的潛在影響。</span><span class="sxs-lookup"><span data-stu-id="d3227-111">Rollback reduces the potential impact that a Microsoft Edge issue has on business operations.</span></span>

## <span data-ttu-id="d3227-112">開始之前</span><span class="sxs-lookup"><span data-stu-id="d3227-112">Before you begin</span></span>

<span data-ttu-id="d3227-113">重要的是要瞭解如何在 Microsoft Edge 環境中安裝復原功能。</span><span class="sxs-lookup"><span data-stu-id="d3227-113">It's important to understand how the rollback feature is installed in a Microsoft Edge environment.</span></span> <span data-ttu-id="d3227-114">您可以使用兩種不同的方法來部署復原：手動使用 MSI，或使用 Microsoft Edge Update 和群組原則。</span><span class="sxs-lookup"><span data-stu-id="d3227-114">You can deploy rollback using two different methods: manually with an MSI or by using Microsoft Edge update and Group Policy.</span></span> <span data-ttu-id="d3227-115">我們也鼓勵您選擇群組原則，以便更順利地部署。</span><span class="sxs-lookup"><span data-stu-id="d3227-115">We also  encourage using a selection of Group Policies for a smoother deployment.</span></span>

### <span data-ttu-id="d3227-116">建議</span><span class="sxs-lookup"><span data-stu-id="d3227-116">Recommendations</span></span>

<span data-ttu-id="d3227-117">復原功能的目的是暫時解決您在 Microsoft Edge 瀏覽器更新中可能發生的問題。</span><span class="sxs-lookup"><span data-stu-id="d3227-117">The rollback feature is meant to be a temporary fix for issues you might find in a Microsoft Edge browser update.</span></span> <span data-ttu-id="d3227-118">建議使用者安裝最新版本的 Microsoft Edge 瀏覽器，以使用最新安全性更新提供的保護。</span><span class="sxs-lookup"><span data-stu-id="d3227-118">We recommend that users install the latest version of the Microsoft Edge browser to use the protection provided by the latest security updates.</span></span> <span data-ttu-id="d3227-119">復原到舊版可能會面臨已知的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="d3227-119">Rollback to an earlier version risks exposure to known security issues.</span></span>

<span data-ttu-id="d3227-120">在暫時復原瀏覽器版本之前，強烈建議為貴組織中的所有使用者啟用同步。</span><span class="sxs-lookup"><span data-stu-id="d3227-120">Before temporarily rolling back your browser version, we also highly recommend that you enable Sync for all the users in your organization.</span></span> <span data-ttu-id="d3227-121">如果未開啟同步，就會有瀏覽資料永久遺失的風險。</span><span class="sxs-lookup"><span data-stu-id="d3227-121">If you don't turn on Sync, there's a risk of permanent browsing data loss.</span></span> <span data-ttu-id="d3227-122">如需關於同步的詳細資訊，請參閱 [Microsoft Edge 同步](microsoft-edge-enterprise-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="d3227-122">For more information about Sync, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md).</span></span>

> [!CAUTION]
> <span data-ttu-id="d3227-123">只有在必要時才使用復原，因為始終存在資料遺失的風險。</span><span class="sxs-lookup"><span data-stu-id="d3227-123">Only use rollback when necessary, there's always the risk of data loss.</span></span>

## <span data-ttu-id="d3227-124">使用 MSI 手動啟用復原</span><span class="sxs-lookup"><span data-stu-id="d3227-124">Enable rollback manually with an MSI</span></span>

<span data-ttu-id="d3227-125">使用下列步驟，以手動方式使用 MSI 復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-125">Use the following steps to roll back manually with an MSI.</span></span>

1. <span data-ttu-id="d3227-126">停用 Microsoft Edge 更新。</span><span class="sxs-lookup"><span data-stu-id="d3227-126">Disable Microsoft Edge Updates.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d3227-127">我們建議您安裝最新的系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="d3227-127">We recommend that you install the most current Administrative templates.</span></span> <span data-ttu-id="d3227-128">如需詳細資訊，請參閱 [下載並安裝 Microsoft Edge 系統管理範本](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template)。</span><span class="sxs-lookup"><span data-stu-id="d3227-128">For more information, see [Download and install the Microsoft Edge administrative template](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template).</span></span>

   - <span data-ttu-id="d3227-129">開啟 [本機群組原則編輯器]，然後移至 *[電腦設定] > [管理範本] > [Microsoft Edge Update] > [應用程式] > [Microsoft Edge] >*。</span><span class="sxs-lookup"><span data-stu-id="d3227-129">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
   - <span data-ttu-id="d3227-130">選取 **[更新原則覆寫]**，然後選取 **[啟用]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-130">Select **Update policy override** and then select **Enabled**.</span></span>
   - <span data-ttu-id="d3227-131">在 **[選項]** 的 [原則] 下拉式清單中，挑選 **[更新已停用]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-131">Under **Options**, pick **Update disabled** from the Policy dropdown list.</span></span>

2. <span data-ttu-id="d3227-132">取得 MSI。</span><span class="sxs-lookup"><span data-stu-id="d3227-132">Get the MSI.</span></span>

   - <span data-ttu-id="d3227-133">從此處下載您想要復原至 [ ](https://www.microsoft.com/edge/business/download)的 MSI 版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-133">Download the MSI for the version you want to roll back to [from here](https://www.microsoft.com/edge/business/download).</span></span>
   - <span data-ttu-id="d3227-134">將 MSI 儲存到桌面。</span><span class="sxs-lookup"><span data-stu-id="d3227-134">Save the MSI to your desktop.</span></span>

3. <span data-ttu-id="d3227-135">執行復原命令。</span><span class="sxs-lookup"><span data-stu-id="d3227-135">Run the rollback command.</span></span>

   - <span data-ttu-id="d3227-136">使用 **以系統管理員身分執行** 開啟 Windows 命令提示字元。</span><span class="sxs-lookup"><span data-stu-id="d3227-136">Open the Windows command prompt with **Run as administrator**.</span></span>
   - <span data-ttu-id="d3227-137">輸入下列命令，其中：*C:\Users\username\Desktop\test*  是下載 MSI 的路徑，而 FileName 是 .msi 的檔案名稱：</span><span class="sxs-lookup"><span data-stu-id="d3227-137">Type the following command, where: *C:\Users\username\Desktop\test* is the path to the MSI you downloaded, and FileName is the name of the .msi file:</span></span><br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > <span data-ttu-id="d3227-138">如需有關 msiexec 的詳細資訊，請參閱 [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec)。</span><span class="sxs-lookup"><span data-stu-id="d3227-138">For more information about msiexec, see [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec).</span></span>
   - <span data-ttu-id="d3227-139">關閉並重新開啟 Microsoft Edge，以驗證復原正常運作。</span><span class="sxs-lookup"><span data-stu-id="d3227-139">Close and reopen Microsoft Edge to verify that the rollback worked.</span></span> <span data-ttu-id="d3227-140">在 **[設定和更多]** (ALT+F) 底下，移至 **[設定]** 然後選取 **[關於 Microsoft Edge]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-140">Under **Settings and more** (ALT + F), go to **Settings** and select **About Microsoft Edge**.</span></span>

## <span data-ttu-id="d3227-141">使用 Microsoft Edge Update 和群組原則啟用復原</span><span class="sxs-lookup"><span data-stu-id="d3227-141">Enable rollback with Microsoft Edge update and Group Policy</span></span>

<span data-ttu-id="d3227-142">使用下列步驟，用 Microsoft Edge Update 和群組原則啟用復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-142">Use the following steps to enable rollback with Microsoft Edge update and Group Policy.</span></span>

1. <span data-ttu-id="d3227-143">開啟 [本機群組原則編輯器]，然後移至 *[電腦設定] > [管理範本] > [Microsoft Edge Update] > [應用程式] > [Microsoft Edge] >*。</span><span class="sxs-lookup"><span data-stu-id="d3227-143">Open the local Group Policy Editor and go to *Computer Configuration>Administrative Templates>Microsoft Edge Update>Applications>Microsoft Edge>*.</span></span>
2. <span data-ttu-id="d3227-144">選取 **[復原至目標版本]**，然後選取 **[啟用]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-144">Select **Rollback to target version** and then select **Enabled**.</span></span>
3. <span data-ttu-id="d3227-145">選取 **[目標版本覆寫]**，並挑選要復原的瀏覽器版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-145">Select **Target version override** and pick the browser version you want to roll back to.</span></span>
4. <span data-ttu-id="d3227-146">選取 **[更新原則覆寫]**，然後選取 **[啟用]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-146">Select **Update policy override** and then select **Enabled**.</span></span> <span data-ttu-id="d3227-147">在 **[選項]** 的 [原則] 下拉式清單中，挑選下列其中一個選項 (**[更新已停用]** 除外)：</span><span class="sxs-lookup"><span data-stu-id="d3227-147">Under **Options**, pick one of the following options from the Policy dropdown list (except for **Update disabled**):</span></span>

   - <span data-ttu-id="d3227-148">永遠允許更新</span><span class="sxs-lookup"><span data-stu-id="d3227-148">Always allow updates</span></span>
   - <span data-ttu-id="d3227-149">僅限自動無訊息更新</span><span class="sxs-lookup"><span data-stu-id="d3227-149">Automatic silent updates only</span></span>
   - <span data-ttu-id="d3227-150">僅限手動更新</span><span class="sxs-lookup"><span data-stu-id="d3227-150">Manual updates only</span></span>  

5. <span data-ttu-id="d3227-151">下次 Microsoft Edge Update 檢查更新時，將會發生復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-151">Rollback will happen the next time Microsoft Edge Update checks for an update.</span></span>

   > [!NOTE]
   > <span data-ttu-id="d3227-152">如果要立即復原，您必須變更 Microsoft Edge Update 的輪詢間隔，或使用 MSI 啟用復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-152">If you want rollback to happen right away you have to change the Microsoft Edge Update polling interval or enable rollback using an MSI.</span></span>

### <span data-ttu-id="d3227-153">常見復原錯誤</span><span class="sxs-lookup"><span data-stu-id="d3227-153">Common rollback errors</span></span>

<span data-ttu-id="d3227-154">下列錯誤會妨礙復原：</span><span class="sxs-lookup"><span data-stu-id="d3227-154">The following errors will prevent rollback:</span></span>

- <span data-ttu-id="d3227-155">輸入不支援的目標版本</span><span class="sxs-lookup"><span data-stu-id="d3227-155">Input is an unsupported target version</span></span>
- <span data-ttu-id="d3227-156">輸入不存在的目標版本</span><span class="sxs-lookup"><span data-stu-id="d3227-156">Input is a non-existent target version</span></span>
- <span data-ttu-id="d3227-157">輸入資料格式不正確。</span><span class="sxs-lookup"><span data-stu-id="d3227-157">Input is incorrectly formatted</span></span>

### <span data-ttu-id="d3227-158">建議的群組原則</span><span class="sxs-lookup"><span data-stu-id="d3227-158">Recommended Group Policies</span></span>

<span data-ttu-id="d3227-159">強烈建議使用以下群組原則和設定來進行復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-159">The following group policies and settings are highly recommended for using rollback.</span></span>

#### <span data-ttu-id="d3227-160">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="d3227-160">Sync Group Policies</span></span>

- <span data-ttu-id="d3227-161">強制同步。</span><span class="sxs-lookup"><span data-stu-id="d3227-161">ForceSync.</span></span> <span data-ttu-id="d3227-162">將強制同步設定為啟用。</span><span class="sxs-lookup"><span data-stu-id="d3227-162">Set ForceSync to enabled.</span></span> <span data-ttu-id="d3227-163">這個原則將強制啟用所有 Azure Active Directory (Azure AD) 使用者的同步處理。</span><span class="sxs-lookup"><span data-stu-id="d3227-163">This policy will force enable Sync on all Azure Active Directory (Azure AD) users.</span></span> <span data-ttu-id="d3227-164">這個原則只適用於 Microsoft Edge 版本 86 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-164">This policy is only effective for Microsoft Edge versions 86 and later.</span></span>
- <span data-ttu-id="d3227-165">*[設定] 從 [同步處理原則] 中排除的類型清單* 允許系統管理員控制哪些資料能由使用者進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="d3227-165">The *Configure the list of the types that are excluded from synchronization policy* allows admins to control what data can be synced by users.</span></span>

#### <span data-ttu-id="d3227-166">瀏覽器重新啟動群組原則</span><span class="sxs-lookup"><span data-stu-id="d3227-166">Browser restart Group Policies</span></span>

<span data-ttu-id="d3227-167">建議您在啟用復原之後，強制為使用者重新啟動。</span><span class="sxs-lookup"><span data-stu-id="d3227-167">We recommend forcing a restart on users after rollback is enabled.</span></span>

- <span data-ttu-id="d3227-168">啟用 *[通知使用者]，建議或需要重新啟動瀏覽器，以套用擱置中的更新*。</span><span class="sxs-lookup"><span data-stu-id="d3227-168">Enable *Notify a user that a browser restart is recommended or required for pending updates*.</span></span> <span data-ttu-id="d3227-169">在 [選項] 底下，選取 **[必要]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-169">Under Options, select **Required**.</span></span>
- <span data-ttu-id="d3227-170">啟用 *[設定更新通知的時段]*，然後以毫秒設定所需的時間。</span><span class="sxs-lookup"><span data-stu-id="d3227-170">Enable *Set the time period for update notifications* and then set the desired time in milliseconds.</span></span>

## <span data-ttu-id="d3227-171">常見問題集</span><span class="sxs-lookup"><span data-stu-id="d3227-171">Frequently asked questions</span></span>

### <span data-ttu-id="d3227-172">手動 MSI 復原</span><span class="sxs-lookup"><span data-stu-id="d3227-172">Manual MSI rollback</span></span>

#### <span data-ttu-id="d3227-173">可能會發生哪些常見的 MSI 故障？</span><span class="sxs-lookup"><span data-stu-id="d3227-173">What generic MSI failures that can happen?</span></span>

1. <span data-ttu-id="d3227-174">如果已停用安裝更新群組原則，將不會發生復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-174">If the Install update group policy is disabled, rollback won't occur.</span></span>

   - <span data-ttu-id="d3227-175">若要使用復原，請確認已將安裝設為 **[啟用]**。</span><span class="sxs-lookup"><span data-stu-id="d3227-175">To use rollback, make sure Install is set to **Enabled**.</span></span> <span data-ttu-id="d3227-176">停用此原則時，會妨礙安裝 Microsoft Edge 頻道。</span><span class="sxs-lookup"><span data-stu-id="d3227-176">When this policy is disabled, it prevents Microsoft Edge channels from being installed.</span></span> <span data-ttu-id="d3227-177">如需詳細資訊，請參閱 [安裝](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install)。</span><span class="sxs-lookup"><span data-stu-id="d3227-177">For more information, see [Install](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install).</span></span>

2. <span data-ttu-id="d3227-178">如果沒有啟蒙更新，將會封鎖 Microsoft Edge 安裝，除非 *[允許 Microsoft Edge 並存瀏覽器體驗]* 已啟用。</span><span class="sxs-lookup"><span data-stu-id="d3227-178">If Enlightenment Updates aren't present, Microsoft Edge installations will be blocked unless *Allow Microsoft Edge Side by Side browser experience* is enabled.</span></span>

   - <span data-ttu-id="d3227-179">適用於 Windows 版本 1903 和 1909：如果您的上次更新在 2019 年 10 月之前，可能會遇到此問題。</span><span class="sxs-lookup"><span data-stu-id="d3227-179">For Windows versions 1903 and 1909: If your last update was before October 2019, you may have this issue.</span></span>
   - <span data-ttu-id="d3227-180">適用於 Windows 版本 1709、1803 及 1809：如果您的上次更新在 2019 年 11 月之前，可能會遇到此問題。</span><span class="sxs-lookup"><span data-stu-id="d3227-180">For Windows versions 1709, 1803, and 1809: If your last update was before November 2019, you may have this issue.</span></span><br>
<span data-ttu-id="d3227-181">如需詳細資訊，請參閱 [支援下一版 Microsoft Edge 的 Windows Update](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)。</span><span class="sxs-lookup"><span data-stu-id="d3227-181">For more information, see [Windows updates to support the next version of Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)</span></span>

#### <span data-ttu-id="d3227-182">使用 [命令提示字元] 之後，顯示下列錯誤訊息，而且復原並未發生。</span><span class="sxs-lookup"><span data-stu-id="d3227-182">The following error message was shown after using the Command Prompt and rollback didn't occur.</span></span> <span data-ttu-id="d3227-183">怎麼回事？</span><span class="sxs-lookup"><span data-stu-id="d3227-183">What's wrong?</span></span>

![復原狀態訊息](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

<span data-ttu-id="d3227-185">*ALLOWDOWNGRADE=1* 未執行。</span><span class="sxs-lookup"><span data-stu-id="d3227-185">*ALLOWDOWNGRADE=1* was not executed.</span></span>

### <span data-ttu-id="d3227-186">Microsoft Edge Update 和群組原則復原</span><span class="sxs-lookup"><span data-stu-id="d3227-186">Microsoft Edge Update and Group Policy rollback</span></span>

#### <span data-ttu-id="d3227-187">我設定 *[復原到目標版本]*、啟用 *[更新原則覆寫]*、輸入 *[目標版本覆寫]* 的預期瀏覽器版本，但瀏覽器版本不符合預期。</span><span class="sxs-lookup"><span data-stu-id="d3227-187">I set *Rollback to target version*, enabled *Update policy override*, input my desired browser version for *Target version override*, but the browser version wasn't what I expected.</span></span> <span data-ttu-id="d3227-188">怎麼回事？</span><span class="sxs-lookup"><span data-stu-id="d3227-188">What's wrong?</span></span>

<span data-ttu-id="d3227-189">以下是一些妨礙復原的常見錯誤：</span><span class="sxs-lookup"><span data-stu-id="d3227-189">Some common errors that prevent rollback are:</span></span>

- <span data-ttu-id="d3227-190">如果未設定 [復原到目標版本]，將不會執行復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-190">If Rollback to target version isn't set, rollback will not be executed.</span></span>
- <span data-ttu-id="d3227-191">[目標版本覆寫] 設定有下列其中一個問題：</span><span class="sxs-lookup"><span data-stu-id="d3227-191">There are one of the following issues with the target version override setting:</span></span>

  - <span data-ttu-id="d3227-192">[目標版本覆寫] 設定為不支援的目標版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-192">Target version override is set to an unsupported target version.</span></span>
  - <span data-ttu-id="d3227-193">[目標版本覆寫] 設定為不存在的目標版本。</span><span class="sxs-lookup"><span data-stu-id="d3227-193">Target version override is set to a non-existent target version.</span></span>
  - <span data-ttu-id="d3227-194">[目標版本覆寫] 輸入格式不正確。</span><span class="sxs-lookup"><span data-stu-id="d3227-194">Target version override input is incorrectly formatted.</span></span>

- <span data-ttu-id="d3227-195">如果 [更新原則覆寫] 設定為 [更新已停用]，Microsoft Edge Update 將不接受任何更新。</span><span class="sxs-lookup"><span data-stu-id="d3227-195">If Update policy override is set to "Updates disabled", Microsoft Edge Update won't accept any updates.</span></span> <span data-ttu-id="d3227-196">這會導致無法執行復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-196">This results in rollback not getting executed.</span></span>

### <span data-ttu-id="d3227-197">我將所有群組原則設定正確，但是復原並未執行。</span><span class="sxs-lookup"><span data-stu-id="d3227-197">I set all the group policies correctly, but rollback didn't execute.</span></span> <span data-ttu-id="d3227-198">發生了什麼事？</span><span class="sxs-lookup"><span data-stu-id="d3227-198">What happened?</span></span>

<span data-ttu-id="d3227-199">Microsoft Edge Update 尚未執行更新檢查。</span><span class="sxs-lookup"><span data-stu-id="d3227-199">Microsoft Edge Update hasn't run a check for updates yet.</span></span> <span data-ttu-id="d3227-200">預設情況下，自動更新每 10 小時會檢查一次是否有更新。</span><span class="sxs-lookup"><span data-stu-id="d3227-200">By default, auto-update checks for updates every 10 hours.</span></span> <span data-ttu-id="d3227-201">若要修正此問題，您可以變更 Microsoft Edge Update 的輪詢間隔，並使用自動更新檢查週期來覆寫群組原則。</span><span class="sxs-lookup"><span data-stu-id="d3227-201">You can fix this by changing Microsoft Edge Update's polling interval with the Auto-update check period override group policy.</span></span> <span data-ttu-id="d3227-202">如需詳細資訊，請參閱 [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) 原則。</span><span class="sxs-lookup"><span data-stu-id="d3227-202">For more information, see the [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) policy.</span></span>

### <span data-ttu-id="d3227-203">如果您是 IT 系統管理員，請遵循正確復原的所有步驟。</span><span class="sxs-lookup"><span data-stu-id="d3227-203">As an IT admin, I followed all the steps for rollback correctly.</span></span> <span data-ttu-id="d3227-204">僅自己使用者群組的一部分會復原。</span><span class="sxs-lookup"><span data-stu-id="d3227-204">Only a portion of my user group was rolled back.</span></span> <span data-ttu-id="d3227-205">為什麼其他使用者尚未復原？</span><span class="sxs-lookup"><span data-stu-id="d3227-205">Why haven't the other users been rolled back yet?</span></span>

<span data-ttu-id="d3227-206">群組原則設定尚未同步處理到所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="d3227-206">The group policy setting hasn't synced to all the clients yet.</span></span> <span data-ttu-id="d3227-207">當系統管理員設定群組原則時，用戶端不會立即收到這些設定。</span><span class="sxs-lookup"><span data-stu-id="d3227-207">When admins set a group policy, clients don't receive these settings instantaneously.</span></span>

<!--
You can update all users' group policy with the  

When admins set all users don't get this setting instantaneously 

GP Update force group policy – link to this 

-->





## <span data-ttu-id="d3227-208">請參閱</span><span class="sxs-lookup"><span data-stu-id="d3227-208">See also</span></span>

- [<span data-ttu-id="d3227-209">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="d3227-209">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
