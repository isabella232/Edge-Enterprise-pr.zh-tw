---
title: Microsoft Edge Update 原則文件
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/07/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge Updater 支援的所有原則的文件
ms.openlocfilehash: feb7859f062ae39e2bbfe08d8e478386defb85cf
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105567"
---
# <span data-ttu-id="b1036-103">Microsoft Edge - 更新原則</span><span class="sxs-lookup"><span data-stu-id="b1036-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="b1036-104">最新版本的 Microsoft Edge 包括以下原則，可用於控制更新 Microsoft Edge 的方式和時間。</span><span class="sxs-lookup"><span data-stu-id="b1036-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="b1036-105">如需 Microsoft Edge 中提供的其他原則的相關資訊，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="b1036-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="b1036-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <span data-ttu-id="b1036-107">可用原則</span><span class="sxs-lookup"><span data-stu-id="b1036-107">Available policies</span></span>
<span data-ttu-id="b1036-108">下表列出此版本 Microsoft Edge 提供的所有更新相關群組原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="b1036-109">使用下表中的連結，深入了解特定原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="b1036-110">應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-110">Applications</span></span>](#applications)|[<span data-ttu-id="b1036-111">喜好設定</span><span class="sxs-lookup"><span data-stu-id="b1036-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="b1036-112">Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="b1036-112">Proxy Server</span></span>](#proxy-server)|[<span data-ttu-id="b1036-113">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b1036-113">Microsoft Edge WebView</span></span>](#microsoft-edge-webview)|

### [<span data-ttu-id="b1036-114">應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-114">Applications</span></span>](#applications-policies)
|<span data-ttu-id="b1036-115">原則名稱</span><span class="sxs-lookup"><span data-stu-id="b1036-115">Policy Name</span></span>|<span data-ttu-id="b1036-116">標題</span><span class="sxs-lookup"><span data-stu-id="b1036-116">Caption</span></span>|
|-|-|
|[<span data-ttu-id="b1036-117">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-117">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="b1036-118">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-118">Allow installation default</span></span>|
|[<span data-ttu-id="b1036-119">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-119">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="b1036-120">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-120">Update policy override default</span></span>|
|[<span data-ttu-id="b1036-121">Install</span><span class="sxs-lookup"><span data-stu-id="b1036-121">Install</span></span>](#install)|<span data-ttu-id="b1036-122">允許安裝 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="b1036-122">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="b1036-123">Update</span><span class="sxs-lookup"><span data-stu-id="b1036-123">Update</span></span>](#update)|<span data-ttu-id="b1036-124">更新原則覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="b1036-124">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="b1036-125">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="b1036-125">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="b1036-126">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="b1036-126">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="b1036-127">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-127">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="b1036-128">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="b1036-128">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="b1036-129">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="b1036-129">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="b1036-130">防止在安裝時建立桌面捷徑 (每個通道)</span><span class="sxs-lookup"><span data-stu-id="b1036-130">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="b1036-131">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="b1036-131">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="b1036-132">復原至目標版本 (每個通道)</span><span class="sxs-lookup"><span data-stu-id="b1036-132">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="b1036-133">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="b1036-133">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="b1036-134">目標版本覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="b1036-134">Target version override (per channel)</span></span>|

### [<span data-ttu-id="b1036-135">喜好設定</span><span class="sxs-lookup"><span data-stu-id="b1036-135">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="b1036-136">原則名稱</span><span class="sxs-lookup"><span data-stu-id="b1036-136">Policy Name</span></span>|<span data-ttu-id="b1036-137">標題</span><span class="sxs-lookup"><span data-stu-id="b1036-137">Caption</span></span>|
|-|-|
|[<span data-ttu-id="b1036-138">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="b1036-138">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="b1036-139">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-139">Auto-update check period override</span></span>|
|[<span data-ttu-id="b1036-140">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="b1036-140">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="b1036-141">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="b1036-141">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="b1036-142">Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="b1036-142">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="b1036-143">原則名稱</span><span class="sxs-lookup"><span data-stu-id="b1036-143">Policy Name</span></span>|<span data-ttu-id="b1036-144">說明文字</span><span class="sxs-lookup"><span data-stu-id="b1036-144">Caption</span></span>|
|-|-|
|[<span data-ttu-id="b1036-145">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="b1036-145">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="b1036-146">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="b1036-146">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="b1036-147">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="b1036-147">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="b1036-148">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-148">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="b1036-149">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="b1036-149">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="b1036-150">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-150">Address or URL of proxy server</span></span>|

### [<span data-ttu-id="b1036-151">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b1036-151">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="b1036-152">原則名稱</span><span class="sxs-lookup"><span data-stu-id="b1036-152">Policy Name</span></span>|<span data-ttu-id="b1036-153">標題</span><span class="sxs-lookup"><span data-stu-id="b1036-153">Caption</span></span>|
|-|-|
|[<span data-ttu-id="b1036-154">安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-154">Install</span></span>](#install-webview)|<span data-ttu-id="b1036-155">允許安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-155">Allow installation</span></span>|
|[<span data-ttu-id="b1036-156">更新</span><span class="sxs-lookup"><span data-stu-id="b1036-156">Update</span></span>](#update-webview)|<span data-ttu-id="b1036-157">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-157">Update policy override</span></span>|

## <span data-ttu-id="b1036-158">應用程式原則</span><span class="sxs-lookup"><span data-stu-id="b1036-158">Applications policies</span></span>

[<span data-ttu-id="b1036-159">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-159">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="b1036-160">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-160">InstallDefault</span></span>
#### <span data-ttu-id="b1036-161">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-161">Allow installation default</span></span>
><span data-ttu-id="b1036-162">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-162">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-163">描述</span><span class="sxs-lookup"><span data-stu-id="b1036-163">Description</span></span>
<span data-ttu-id="b1036-164">您可以指定所有通道的預設行為，以便在加入網域的裝置上允許或封鎖 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b1036-164">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="b1036-165">您可以為特定通道啟用「[允許安裝](#install)」原則來覆寫各個通道的此原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-165">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="b1036-166">如果停用此原則，則會封鎖 Microsoft Edge 安裝。</span><span class="sxs-lookup"><span data-stu-id="b1036-166">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="b1036-167">當 '[允許安裝](#install)' 原則設定為 [尚未設定] 時，只會影響 Microsoft Edge 軟體的安裝，。</span><span class="sxs-lookup"><span data-stu-id="b1036-167">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="b1036-168">此原則不會防止 Microsoft Edge Update 執行或防止使用者透過其他方法安裝 Microsoft Edge 軟體。</span><span class="sxs-lookup"><span data-stu-id="b1036-168">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="b1036-169">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-169">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-170">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-170">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-171">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-171">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-172">GP 唯一名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-172">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="b1036-173">GP 名稱：允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-173">GP name: Allow installation default</span></span>
- <span data-ttu-id="b1036-174">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-174">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="b1036-175">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-175">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-176">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-176">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-177">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-177">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-178">值名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-178">Value Name: InstallDefault</span></span>
- <span data-ttu-id="b1036-179">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-179">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-180">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-180">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-181">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-181">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-182">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-182">UpdateDefault</span></span>
#### <span data-ttu-id="b1036-183">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-183">Update policy override default</span></span>
><span data-ttu-id="b1036-184">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-184">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-185">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-185">Description</span></span>
<span data-ttu-id="b1036-186">允許您指定所有通道的預設行為，這些通道涉及 Microsoft Edge Update 處理 Microsoft Edge 可用更新的方式。</span><span class="sxs-lookup"><span data-stu-id="b1036-186">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="b1036-187">可以透過為這些特定通道指定「[更新原則覆寫](#update)」原則來覆寫各個通道的設定。</span><span class="sxs-lookup"><span data-stu-id="b1036-187">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="b1036-188">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="b1036-188">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="b1036-189">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-189">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="b1036-190">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-190">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="b1036-191">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-191">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="b1036-192">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-192">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="b1036-193">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-193">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="b1036-194">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="b1036-194">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="b1036-195">如果不啟用和設定此原則，Microsoft Edge Update 將依照[「更新原則覆寫」](#update)原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-195">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="b1036-196">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-196">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-197">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-197">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-198">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-198">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-199">GP 唯一名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-199">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="b1036-200">GP 名稱：更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="b1036-200">GP name: Update policy override default</span></span>
- <span data-ttu-id="b1036-201">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-201">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="b1036-202">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-202">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-203">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-203">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-204">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-204">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-205">值名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-205">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="b1036-206">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-206">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-207">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-207">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="b1036-208">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-208">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-209">Install</span><span class="sxs-lookup"><span data-stu-id="b1036-209">Install</span></span>
#### <span data-ttu-id="b1036-210">允許安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-210">Allow installation</span></span>
><span data-ttu-id="b1036-211">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-211">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-212">描述</span><span class="sxs-lookup"><span data-stu-id="b1036-212">Description</span></span>
<span data-ttu-id="b1036-213">指定是否可以在加入網域的裝置上安裝 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="b1036-213">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="b1036-214">如果您為通道啟用此原則，將不會封鎖 Microsoft Edge 的安裝。</span><span class="sxs-lookup"><span data-stu-id="b1036-214">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="b1036-215">如果您為通道停用此原則，將會封鎖 Microsoft Edge 的安裝。</span><span class="sxs-lookup"><span data-stu-id="b1036-215">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="b1036-216">如果不為通道設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以安裝該 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="b1036-216">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="b1036-217">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-217">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-218">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-218">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-219">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-219">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-220">GP 唯一名稱：Install</span><span class="sxs-lookup"><span data-stu-id="b1036-220">GP unique name: Install</span></span>
- <span data-ttu-id="b1036-221">GP 名稱：允許安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-221">GP name: Allow installation</span></span>
- <span data-ttu-id="b1036-222">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="b1036-222">GP path:</span></span> 
  - <span data-ttu-id="b1036-223">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="b1036-224">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="b1036-224">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="b1036-225">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="b1036-225">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="b1036-226">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b1036-226">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="b1036-227">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-227">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-228">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-228">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-229">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-229">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-230">值名稱：</span><span class="sxs-lookup"><span data-stu-id="b1036-230">Value Name:</span></span> 
  - <span data-ttu-id="b1036-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="b1036-231">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="b1036-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="b1036-232">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="b1036-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="b1036-233">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="b1036-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="b1036-234">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="b1036-235">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-235">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-236">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-236">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-237">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-237">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-238">Update</span><span class="sxs-lookup"><span data-stu-id="b1036-238">Update</span></span>
#### <span data-ttu-id="b1036-239">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-239">Update policy override</span></span>
><span data-ttu-id="b1036-240">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-240">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-241">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-241">Description</span></span>
<span data-ttu-id="b1036-242">指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-242">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="b1036-243">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="b1036-243">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="b1036-244">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-244">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="b1036-245">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-245">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="b1036-246">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-246">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="b1036-247">(並非所有應用程式都提供此選項的介面。)</span><span class="sxs-lookup"><span data-stu-id="b1036-247">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="b1036-248">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-248">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="b1036-249">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-249">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="b1036-250">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="b1036-250">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="b1036-251">如果不啟用和設定此原則，Microsoft Edge Update 將依照「[更新原則覆寫預設值](#updatedefault)」原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-251">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="b1036-252">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406)。</span><span class="sxs-lookup"><span data-stu-id="b1036-252">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="b1036-253">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-253">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-254">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-254">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-255">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-255">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-256">GP 唯一名稱：Update</span><span class="sxs-lookup"><span data-stu-id="b1036-256">GP unique name: Update</span></span>
- <span data-ttu-id="b1036-257">GP 名稱：更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-257">GP name: Update policy override</span></span>
- <span data-ttu-id="b1036-258">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="b1036-258">GP path:</span></span> 
  - <span data-ttu-id="b1036-259">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="b1036-260">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="b1036-260">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="b1036-261">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="b1036-261">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="b1036-262">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b1036-262">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="b1036-263">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-263">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-264">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-264">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-265">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-265">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-266">值名稱：</span><span class="sxs-lookup"><span data-stu-id="b1036-266">Value Name:</span></span> 
  - <span data-ttu-id="b1036-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="b1036-267">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="b1036-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="b1036-268">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="b1036-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="b1036-269">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="b1036-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="b1036-270">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="b1036-271">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-271">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-272">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-272">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-273">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-273">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-274">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="b1036-274">Allowsxs</span></span>
#### <span data-ttu-id="b1036-275">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="b1036-275">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="b1036-276">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-276">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-277">描述</span><span class="sxs-lookup"><span data-stu-id="b1036-277">Description</span></span>
<span data-ttu-id="b1036-278">此原則允許使用者並排執行 Microsoft Edge (Edge HTML) 和 Microsoft Edge (以 Chromium 為基礎)。</span><span class="sxs-lookup"><span data-stu-id="b1036-278">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="b1036-279">如果此原則設定為 [未設定]，則在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="b1036-279">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="b1036-280">這與 [停用] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="b1036-280">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="b1036-281">[停用] 設定會封鎖並排體驗，且在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="b1036-281">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="b1036-282">這與 [未設定] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="b1036-282">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="b1036-283">當此原則 [啟用] 時，Microsoft Edge (以 Chromium 為基礎) 和 Microsoft Edge (Edge HTML) 可以在安裝 Microsoft Edge (以 Chromium 為基礎) 後並排執行。</span><span class="sxs-lookup"><span data-stu-id="b1036-283">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="b1036-284">若要使此群組原則生效，必須在 Windows Update 自動安裝 Microsoft Edge (以 Chromium 為基礎) 之前進行設定。</span><span class="sxs-lookup"><span data-stu-id="b1036-284">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="b1036-285">注意：使用者可以使用 Microsoft Edge (以 Chromium 為基礎) 封鎖程式工具組來封鎖 Microsoft Edge (以 Chromium 為基礎) 的自動更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-285">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="b1036-286">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-286">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-287">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-287">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-288">GP 唯一名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="b1036-288">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="b1036-289">GP 名稱：允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="b1036-289">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="b1036-290">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-290">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="b1036-291">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-291">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-292">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-292">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-293">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-293">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-294">值名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="b1036-294">Value Name: Allowsxs</span></span>
- <span data-ttu-id="b1036-295">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-295">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-296">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-296">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-297">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-297">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-298">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-298">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="b1036-299">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="b1036-299">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="b1036-300">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-300">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="b1036-301">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-301">Description</span></span>
<span data-ttu-id="b1036-302">在安裝 Microsoft Edge 時，可讓您針對所有通道指定建立桌面捷徑的預設行為。</span><span class="sxs-lookup"><span data-stu-id="b1036-302">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="b1036-303">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-303">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="b1036-304">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-304">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="b1036-305">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-305">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="b1036-306">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="b1036-306">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="b1036-307">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-307">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-308">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-308">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-309">GP 唯一名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-309">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="b1036-310">GP 名稱：防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="b1036-310">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="b1036-311">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="b1036-311">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="b1036-312">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-312">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-313">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-313">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-314">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-314">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-315">值名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="b1036-315">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="b1036-316">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-316">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-317">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-317">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-318">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-318">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-319">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="b1036-319">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="b1036-320">防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="b1036-320">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="b1036-321">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-321">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="b1036-322">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-322">Description</span></span>
<span data-ttu-id="b1036-323">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-323">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="b1036-324">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-324">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="b1036-325">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-325">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="b1036-326">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="b1036-326">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="b1036-327">如果您未針對通道設定此原則，[[防止在安裝時建立桌面捷徑預設](#createdesktopshortcutdefault)] 原則設定會決定在安裝 Microsoft Edge 時建立捷徑。</span><span class="sxs-lookup"><span data-stu-id="b1036-327">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="b1036-328">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-328">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-329">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-329">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-330">GP 唯一名稱：CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="b1036-330">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="b1036-331">GP 名稱：防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="b1036-331">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="b1036-332">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="b1036-332">GP path:</span></span> 
  - <span data-ttu-id="b1036-333">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="b1036-334">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="b1036-334">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="b1036-335">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="b1036-335">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="b1036-336">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b1036-336">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="b1036-337">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-337">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-338">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-338">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-339">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-339">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-340">Value Name:</span><span class="sxs-lookup"><span data-stu-id="b1036-340">Value Name:</span></span> 
  - <span data-ttu-id="b1036-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="b1036-341">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="b1036-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="b1036-342">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="b1036-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="b1036-343">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="b1036-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="b1036-344">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="b1036-345">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-345">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-346">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-346">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-347">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-347">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-348">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="b1036-348">RollbackToTargetVersion</span></span>
#### <span data-ttu-id="b1036-349">復原至目標版本</span><span class="sxs-lookup"><span data-stu-id="b1036-349">Rollback to Target version</span></span>
><span data-ttu-id="b1036-350">Microsoft Edge Update 1.3.133.3 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-350">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <span data-ttu-id="b1036-351">描述</span><span class="sxs-lookup"><span data-stu-id="b1036-351">Description</span></span>
<span data-ttu-id="b1036-352">指定 Microsoft Edge Update 應將 Microsoft Edge 的安裝復原為 '[目標版本覆寫](#targetversionprefix)' 中所示的版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-352">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="b1036-353">只有在設定 '[目標版本覆寫](#targetversionprefix)'，且將 '[更新原則覆寫](#update)' 設定為 [開啟] 狀態 (永遠允許更新、僅限自動無訊息更新、僅限手動更新) 時，此原則才會生效。</span><span class="sxs-lookup"><span data-stu-id="b1036-353">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="b1036-354">如果您停用或未設定此原則，安裝的版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會保留原樣。</span><span class="sxs-lookup"><span data-stu-id="b1036-354">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="b1036-355">如果您啟用這個原則，則目前版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會降級為目標版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-355">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="b1036-356">建議使用者安裝最新版本的 Microsoft Edge 瀏覽器，以確保最新安全性更新的保護。</span><span class="sxs-lookup"><span data-stu-id="b1036-356">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="b1036-357">復原到舊版可能會面臨已知的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="b1036-357">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="b1036-358">這項原則可做為暫時修正，以解決 Microsoft Edge 瀏覽器更新中的問題。</span><span class="sxs-lookup"><span data-stu-id="b1036-358">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="b1036-359">在暫時復原瀏覽器版本之前，建議為貴組織中的所有使用者啟用同步處理 ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032))。</span><span class="sxs-lookup"><span data-stu-id="b1036-359">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="b1036-360">如果未開啟同步，就會有瀏覽資料永久遺失的風險。</span><span class="sxs-lookup"><span data-stu-id="b1036-360">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="b1036-361">請自行承擔使用此原則的風險。</span><span class="sxs-lookup"><span data-stu-id="b1036-361">Use this policy at your own risk.</span></span>

<span data-ttu-id="b1036-362">注意：您可以在這裡檢視所有可供復原的版本[https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise)。</span><span class="sxs-lookup"><span data-stu-id="b1036-362">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="b1036-363">本原則適用於 Microsoft Edge 版本 86 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-363">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="b1036-364">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918)。</span><span class="sxs-lookup"><span data-stu-id="b1036-364">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="b1036-365">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-365">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-366">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-366">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-367">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-367">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-368">GP 唯一名稱：RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="b1036-368">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="b1036-369">GP 名稱：復原至目標版本</span><span class="sxs-lookup"><span data-stu-id="b1036-369">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="b1036-370">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="b1036-370">GP path:</span></span> 
  - <span data-ttu-id="b1036-371">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="b1036-372">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="b1036-372">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="b1036-373">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="b1036-373">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="b1036-374">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b1036-374">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="b1036-375">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-375">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-376">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-376">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-377">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-378">Value Name:</span><span class="sxs-lookup"><span data-stu-id="b1036-378">Value Name:</span></span> 
  - <span data-ttu-id="b1036-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="b1036-379">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="b1036-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="b1036-380">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="b1036-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="b1036-381">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="b1036-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="b1036-382">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="b1036-383">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-383">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-384">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-384">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-385">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-385">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-386">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="b1036-386">TargetVersionPrefix</span></span>
#### <span data-ttu-id="b1036-387">目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-387">Target version override</span></span>
><span data-ttu-id="b1036-388">Microsoft Edge Update 1.3.119.43 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-388">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="b1036-389">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-389">Description</span></span>
<span data-ttu-id="b1036-390">啟用此原則且已啟用 [自動更新] 時，Microsoft Edge 將會更新為此原則值所指定的版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-390">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="b1036-391">原則值必須是指定的 Microsoft Edge 版本，例如，83.0.499.12。</span><span class="sxs-lookup"><span data-stu-id="b1036-391">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="b1036-392">如果裝置的 Microsoft Edge 版本比指定值較新，Microsoft Edge 將會維持較新的版本，而不會降級到指定的版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-392">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="b1036-393">如果指定的版本不存在，或格式不正確，Microsoft Edge 將會維持目前的版本，而不會自動更新至未來的版本。</span><span class="sxs-lookup"><span data-stu-id="b1036-393">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="b1036-394">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707)。</span><span class="sxs-lookup"><span data-stu-id="b1036-394">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="b1036-395">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="b1036-395">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <span data-ttu-id="b1036-396">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-396">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-397">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-397">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-398">GP 唯一名稱：TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="b1036-398">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="b1036-399">GP 名稱：目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-399">GP name: Target version override</span></span>
- <span data-ttu-id="b1036-400">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="b1036-400">GP path:</span></span> 
  - <span data-ttu-id="b1036-401">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="b1036-402">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="b1036-402">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="b1036-403">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="b1036-403">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="b1036-404">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b1036-404">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="b1036-405">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-405">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-406">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-406">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-407">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-407">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-408">Value Name:</span><span class="sxs-lookup"><span data-stu-id="b1036-408">Value Name:</span></span> 
  - <span data-ttu-id="b1036-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="b1036-409">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="b1036-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="b1036-410">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="b1036-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="b1036-411">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="b1036-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="b1036-412">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="b1036-413">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1036-413">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="b1036-414">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-414">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="b1036-415">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-415">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="b1036-416">喜好設定原則</span><span class="sxs-lookup"><span data-stu-id="b1036-416">Preferences policies</span></span>

[<span data-ttu-id="b1036-417">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-417">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="b1036-418">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="b1036-418">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="b1036-419">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-419">Auto-update check period override</span></span>
><span data-ttu-id="b1036-420">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-420">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="b1036-421">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-421">Description</span></span>
<span data-ttu-id="b1036-422">如果啟用，此原則允許您設定自動更新檢查之間的最小分鐘數值。</span><span class="sxs-lookup"><span data-stu-id="b1036-422">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="b1036-423">否則，預設情況下，每 10 小時會自動檢查一次是否有更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-423">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="b1036-424">如果要停用所有自動更新檢查，請將值設定為 0 (不建議)。</span><span class="sxs-lookup"><span data-stu-id="b1036-424">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="b1036-425">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-425">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-426">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-426">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-427">GP 唯一名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="b1036-427">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="b1036-428">GP 名稱：自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-428">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="b1036-429">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="b1036-429">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="b1036-430">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-430">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-431">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-431">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-432">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-432">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-433">值名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="b1036-433">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="b1036-434">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-434">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-435">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-435">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="b1036-436">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-436">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-437">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="b1036-437">UpdatesSuppressed</span></span>
#### <span data-ttu-id="b1036-438">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="b1036-438">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="b1036-439">Microsoft Edge Update 1.3.33.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-439">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="b1036-440">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-440">Description</span></span>
<span data-ttu-id="b1036-441">如果啟用此原則，則每天從 Hour:Minute 開始，持續 Duration (分鐘) 抑制檢查更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-441">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="b1036-442">Duration 不受日光節約時間影響。</span><span class="sxs-lookup"><span data-stu-id="b1036-442">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="b1036-443">例如，如果開始時間為 22:00，Duration 為 480 分鐘，則無論日光節約時間在該期間是開始還是結束，都會抑制更新整整 8 小時。</span><span class="sxs-lookup"><span data-stu-id="b1036-443">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="b1036-444">如果停用或不設定此原則，則在任何特定期間都不會抑制更新檢查。</span><span class="sxs-lookup"><span data-stu-id="b1036-444">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="b1036-445">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-445">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-446">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-446">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-447">GP 唯一名稱：UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="b1036-447">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="b1036-448">GP 名稱：每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="b1036-448">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="b1036-449">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="b1036-449">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="b1036-450">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="b1036-450">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="b1036-451">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-451">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-452">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-452">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-453">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-453">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-454">值名稱：</span><span class="sxs-lookup"><span data-stu-id="b1036-454">Value Name:</span></span> 
  - <span data-ttu-id="b1036-455">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="b1036-455">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="b1036-456">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="b1036-456">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="b1036-457">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="b1036-457">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="b1036-458">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-458">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-459">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-459">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="b1036-460">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-460">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="b1036-461">Proxy 伺服器原則</span><span class="sxs-lookup"><span data-stu-id="b1036-461">Proxy Server policies</span></span>

[<span data-ttu-id="b1036-462">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-462">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="b1036-463">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="b1036-463">ProxyMode</span></span>
#### <span data-ttu-id="b1036-464">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="b1036-464">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="b1036-465">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-465">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="b1036-466">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-466">Description</span></span>
<span data-ttu-id="b1036-467">允許您指定 Microsoft Edge Update 使用的 Proxy 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="b1036-467">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="b1036-468">如果啟用此原則，則可以在以下 Proxy 伺服器選項之間進行選擇：</span><span class="sxs-lookup"><span data-stu-id="b1036-468">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="b1036-469">如果選擇一律不使用 Proxy 伺服器且一律直接連線，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="b1036-469">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="b1036-470">如果選擇使用系統 Proxy 設定或自動偵測 Proxy 伺服器，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="b1036-470">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="b1036-471">如果選擇固定伺服器 Proxy 模式，則可在 [[Proxy 伺服器的位址或 URL](#proxyserver)] 原則中指定其他選項。</span><span class="sxs-lookup"><span data-stu-id="b1036-471">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="b1036-472">如果選擇使用 .pac Proxy 指令碼，則必須在 [[Proxy .pac 檔案的 URL](#proxypacurl)] 原則中指定指令碼的 URL。</span><span class="sxs-lookup"><span data-stu-id="b1036-472">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="b1036-473">如果啟用此原則，則組織的使用者無法變更 Microsoft Edge Update 中的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="b1036-473">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="b1036-474">如果停用或不設定此原則，則不會設定任何 Proxy 伺服器設定，但組織中的使用者可以為 Microsoft Edge Update 選擇自己的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="b1036-474">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="b1036-475">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-475">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-476">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-476">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-477">GP 唯一名稱：ProxyMode</span><span class="sxs-lookup"><span data-stu-id="b1036-477">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="b1036-478">GP 名稱：選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="b1036-478">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="b1036-479">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="b1036-479">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="b1036-480">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-480">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-481">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-481">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-482">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-482">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-483">值名稱︰ProxyMode</span><span class="sxs-lookup"><span data-stu-id="b1036-483">Value Name: ProxyMode</span></span>
- <span data-ttu-id="b1036-484">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1036-484">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="b1036-485">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-485">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="b1036-486">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-486">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-487">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="b1036-487">ProxyPacUrl</span></span>
#### <span data-ttu-id="b1036-488">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-488">URL to a proxy .pac file</span></span>
><span data-ttu-id="b1036-489">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-489">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="b1036-490">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-490">Description</span></span>
<span data-ttu-id="b1036-491">允許您為 Proxy 自動設定 (PAC) 檔案指定 URL。</span><span class="sxs-lookup"><span data-stu-id="b1036-491">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="b1036-492">如果啟用此原則，則可以為 PAC 檔案指定 URL，以自動化 Microsoft Edge Update 選取適當 Proxy 伺服器以擷取特定網站的方式。</span><span class="sxs-lookup"><span data-stu-id="b1036-492">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="b1036-493">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-493">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="b1036-494">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-494">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="b1036-495">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-495">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-496">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-496">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-497">GP 唯一名稱：ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="b1036-497">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="b1036-498">GP 名稱：Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-498">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="b1036-499">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="b1036-499">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="b1036-500">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-500">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-501">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-501">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-502">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-502">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-503">值名稱︰ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="b1036-503">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="b1036-504">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1036-504">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="b1036-505">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-505">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="b1036-506">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-506">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-507">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="b1036-507">ProxyServer</span></span>
#### <span data-ttu-id="b1036-508">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-508">Address or URL of proxy server</span></span>
><span data-ttu-id="b1036-509">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-509">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="b1036-510">描述</span><span class="sxs-lookup"><span data-stu-id="b1036-510">Description</span></span>
<span data-ttu-id="b1036-511">允許您指定供 Microsoft Edge Update 使用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="b1036-511">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="b1036-512">如果啟用此原則，您可在組織中設定 Microsoft Edge Update 所用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="b1036-512">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="b1036-513">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中選取手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-513">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="b1036-514">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="b1036-514">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="b1036-515">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-515">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-516">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-516">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-517">GP 唯一名稱：ProxyServer</span><span class="sxs-lookup"><span data-stu-id="b1036-517">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="b1036-518">GP 名稱：Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="b1036-518">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="b1036-519">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="b1036-519">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="b1036-520">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-520">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-521">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-521">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-522">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-522">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-523">值名稱︰ProxyServer</span><span class="sxs-lookup"><span data-stu-id="b1036-523">Value Name: ProxyServer</span></span>
- <span data-ttu-id="b1036-524">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="b1036-524">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="b1036-525">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-525">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="b1036-526">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-526">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="b1036-527">Microsoft Edge WebView 原則</span><span class="sxs-lookup"><span data-stu-id="b1036-527">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="b1036-528">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-528">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="b1036-529">安裝 (WebView)</span><span class="sxs-lookup"><span data-stu-id="b1036-529">Install (WebView)</span></span>
#### <span data-ttu-id="b1036-530">允許安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-530">Allow installation</span></span>
><span data-ttu-id="b1036-531">Microsoft Edge Update 1.3.127.1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-531">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="b1036-532">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-532">Description</span></span>
<span data-ttu-id="b1036-533">可讓您指定是否可以使用 Microsoft Edge Update 來安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="b1036-533">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="b1036-534">如果您啟用此原則，使用者可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="b1036-534">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="b1036-535">如果您停用此原則，使用者無法透過 Microsoft Edge Upadte 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="b1036-535">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="b1036-536">如果不為設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="b1036-536">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="b1036-537">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-537">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-538">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-538">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-539">GP 唯一名稱：Install</span><span class="sxs-lookup"><span data-stu-id="b1036-539">GP unique name: Install</span></span>
- <span data-ttu-id="b1036-540">GP 名稱：允許安裝</span><span class="sxs-lookup"><span data-stu-id="b1036-540">GP name: Allow installation</span></span>
- <span data-ttu-id="b1036-541">GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b1036-541">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="b1036-542">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-542">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-543">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-543">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-544">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-544">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-545">Value Name:</span><span class="sxs-lookup"><span data-stu-id="b1036-545">Value Name:</span></span> 
  - <span data-ttu-id="b1036-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="b1036-546">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="b1036-547">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-547">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-548">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-548">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-549">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-549">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="b1036-550">更新 (WebView)</span><span class="sxs-lookup"><span data-stu-id="b1036-550">Update (WebView)</span></span>
#### <span data-ttu-id="b1036-551">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-551">Update policy override</span></span>
><span data-ttu-id="b1036-552">Microsoft Edge Update 1.3.127.1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="b1036-552">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <span data-ttu-id="b1036-553">說明</span><span class="sxs-lookup"><span data-stu-id="b1036-553">Description</span></span>
<span data-ttu-id="b1036-554">可讓您指定是否為 Microsoft Edge WebView 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-554">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="b1036-555">Microsoft Edge WebView 是應用程式用來顯示網路內容的元件。</span><span class="sxs-lookup"><span data-stu-id="b1036-555">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="b1036-556">預設會啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-556">Automatic updates are enabled by default.</span></span> <span data-ttu-id="b1036-557">若要停用 Microsoft Edge WebView 的自動更新，可能會導致與此元件相關的應用程式發生相容性問題。</span><span class="sxs-lookup"><span data-stu-id="b1036-557">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="b1036-558">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge WebView 更新：</span><span class="sxs-lookup"><span data-stu-id="b1036-558">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="b1036-559">永遠允許更新：會自動下載並套用更新</span><span class="sxs-lookup"><span data-stu-id="b1036-559">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="b1036-560">已停用更新：一律不下載或套用更新</span><span class="sxs-lookup"><span data-stu-id="b1036-560">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="b1036-561">如果您未啟用此原則，則會自動下載並套用更新。</span><span class="sxs-lookup"><span data-stu-id="b1036-561">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <span data-ttu-id="b1036-562">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="b1036-562">Windows information and settings</span></span>
##### <span data-ttu-id="b1036-563">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="b1036-563">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="b1036-564">GP 唯一名稱：Update</span><span class="sxs-lookup"><span data-stu-id="b1036-564">GP unique name: Update</span></span>
- <span data-ttu-id="b1036-565">GP 名稱：更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="b1036-565">GP name: Update policy override</span></span>
- <span data-ttu-id="b1036-566">GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b1036-566">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="b1036-567">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="b1036-567">GP ADMX file name: msedgeupdate.admx</span></span>
##### <span data-ttu-id="b1036-568">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="b1036-568">Windows Registry Settings</span></span>
- <span data-ttu-id="b1036-569">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="b1036-569">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="b1036-570">Value Name:</span><span class="sxs-lookup"><span data-stu-id="b1036-570">Value Name:</span></span> 
  - <span data-ttu-id="b1036-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="b1036-571">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="b1036-572">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="b1036-572">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="b1036-573">範例值：</span><span class="sxs-lookup"><span data-stu-id="b1036-573">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="b1036-574">回到頁首</span><span class="sxs-lookup"><span data-stu-id="b1036-574">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="b1036-575">請參閱</span><span class="sxs-lookup"><span data-stu-id="b1036-575">See also</span></span>
  - [<span data-ttu-id="b1036-576">設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b1036-576">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="b1036-577">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="b1036-577">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)