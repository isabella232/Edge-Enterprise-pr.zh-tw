---
title: Microsoft Edge Update 原則文件
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 06/10/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge Updater 支援的所有原則的文件
ms.openlocfilehash: d772d8dd6f60b89e9bd12a77b740e5fad699756a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979552"
---
# <span data-ttu-id="34e60-103">Microsoft Edge - 更新原則</span><span class="sxs-lookup"><span data-stu-id="34e60-103">Microsoft Edge - Update policies</span></span>
<span data-ttu-id="34e60-104">最新版本的 Microsoft Edge 包括以下原則，可用於控制更新 Microsoft Edge 的方式和時間。</span><span class="sxs-lookup"><span data-stu-id="34e60-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

           
<span data-ttu-id="34e60-105">如需 Microsoft Edge 中提供的其他原則的相關資訊，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="34e60-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="34e60-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="34e60-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="34e60-107">可用原則</span><span class="sxs-lookup"><span data-stu-id="34e60-107">Available policies</span></span>
<span data-ttu-id="34e60-108">下表列出此版本 Microsoft Edge 提供的所有更新相關群組原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="34e60-109">使用下表中的連結，深入了解特定原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-109">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="34e60-110">應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-110">Applications</span></span>](#applications)|[<span data-ttu-id="34e60-111">喜好設定</span><span class="sxs-lookup"><span data-stu-id="34e60-111">Preferences</span></span>](#preferences)|
|[<span data-ttu-id="34e60-112">Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="34e60-112">Proxy Server</span></span>](#proxy-server)||

### [<span data-ttu-id="34e60-113">應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-113">Applications</span></span>](#applications-policies)
|<span data-ttu-id="34e60-114">原則名稱</span><span class="sxs-lookup"><span data-stu-id="34e60-114">Policy Name</span></span>|<span data-ttu-id="34e60-115">標題</span><span class="sxs-lookup"><span data-stu-id="34e60-115">Caption</span></span>|
|-|-|
|[<span data-ttu-id="34e60-116">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-116">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="34e60-117">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-117">Allow installation default</span></span>|
|[<span data-ttu-id="34e60-118">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-118">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="34e60-119">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-119">Update policy override default</span></span>|
|[<span data-ttu-id="34e60-120">安裝</span><span class="sxs-lookup"><span data-stu-id="34e60-120">Install</span></span>](#install)|<span data-ttu-id="34e60-121">允許安裝 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="34e60-121">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="34e60-122">Update</span><span class="sxs-lookup"><span data-stu-id="34e60-122">Update</span></span>](#update)|<span data-ttu-id="34e60-123">更新原則覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="34e60-123">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="34e60-124">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="34e60-124">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="34e60-125">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="34e60-125">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="34e60-126">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-126">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="34e60-127">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="34e60-127">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="34e60-128">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="34e60-128">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="34e60-129">防止在安裝時建立桌面捷徑 (每個通道)</span><span class="sxs-lookup"><span data-stu-id="34e60-129">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="34e60-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="34e60-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="34e60-131">目標版本覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="34e60-131">Target version override (per channel)</span></span>|

### [<span data-ttu-id="34e60-132">喜好設定</span><span class="sxs-lookup"><span data-stu-id="34e60-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="34e60-133">原則名稱</span><span class="sxs-lookup"><span data-stu-id="34e60-133">Policy Name</span></span>|<span data-ttu-id="34e60-134">標題</span><span class="sxs-lookup"><span data-stu-id="34e60-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="34e60-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="34e60-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="34e60-136">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="34e60-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="34e60-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="34e60-138">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="34e60-138">Time period in each day to suppress auto-update check</span></span>|

### [<span data-ttu-id="34e60-139">Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="34e60-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="34e60-140">原則名稱</span><span class="sxs-lookup"><span data-stu-id="34e60-140">Policy Name</span></span>|<span data-ttu-id="34e60-141">說明文字</span><span class="sxs-lookup"><span data-stu-id="34e60-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="34e60-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="34e60-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="34e60-143">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="34e60-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="34e60-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="34e60-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="34e60-145">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="34e60-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="34e60-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="34e60-147">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-147">Address or URL of proxy server</span></span>|

                 
      
  
             
            
                  

## <span data-ttu-id="34e60-148">應用程式原則</span><span class="sxs-lookup"><span data-stu-id="34e60-148">Applications policies</span></span>

[<span data-ttu-id="34e60-149">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-149">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="34e60-150">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-150">InstallDefault</span></span>
#### <span data-ttu-id="34e60-151">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-151">Allow installation default</span></span>
><span data-ttu-id="34e60-152">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-152">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-153">說明</span><span class="sxs-lookup"><span data-stu-id="34e60-153">Description</span></span>
<span data-ttu-id="34e60-154">您可以指定所有通道的預設行為，以便在使用 Microsoft Edge 更新時允許或封鎖 Microsoft Edge 更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-154">You can specify the default behavior of all channels to allow or block Microsoft Edge updates when Microsoft Edge Update is used.</span></span>

<span data-ttu-id="34e60-155">您可以為特定通道啟用「[允許安裝](#install)」原則來覆寫各個通道的此原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-155">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="34e60-156">如果停用此原則，則封鎖透過 Microsoft Edge Update 安裝 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="34e60-156">If you disable this policy, the installation of Microsoft Edge through Microsoft Edge Update is blocked.</span></span> <span data-ttu-id="34e60-157">只有在使用者執行 Microsoft Edge Update 時，而且在使用者尚未設定「[允許安裝](#install)」原則時，才會影響 Microsoft Edge 軟體的安裝。</span><span class="sxs-lookup"><span data-stu-id="34e60-157">This only affects the installation of Microsoft Edge software only when users are running Microsoft Edge Update and when they haven't configured the '[Allow installation](#install)' policy.</span></span>

<span data-ttu-id="34e60-158">此原則不會防止 Microsoft Edge Update 執行或防止使用者透過其他方法安裝 Microsoft Edge 軟體。</span><span class="sxs-lookup"><span data-stu-id="34e60-158">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>
#### <span data-ttu-id="34e60-159">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-159">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-160">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-160">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-161">GP 唯一名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-161">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="34e60-162">GP 名稱：允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-162">GP name: Allow installation default</span></span>
- <span data-ttu-id="34e60-163">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-163">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="34e60-164">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-164">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-165">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-165">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-166">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-166">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-167">值名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-167">Value Name: InstallDefault</span></span>
- <span data-ttu-id="34e60-168">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-168">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-169">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-169">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-170">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-170">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-171">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-171">UpdateDefault</span></span>
#### <span data-ttu-id="34e60-172">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-172">Update policy override default</span></span>
><span data-ttu-id="34e60-173">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-173">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-174">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-174">Description</span></span>
<span data-ttu-id="34e60-175">允許您指定所有通道的預設行為，這些通道涉及 Microsoft Edge Update 處理 Microsoft Edge 可用更新的方式。</span><span class="sxs-lookup"><span data-stu-id="34e60-175">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="34e60-176">可以透過為這些特定通道指定「[更新原則覆寫](#update)」原則來覆寫各個通道的設定。</span><span class="sxs-lookup"><span data-stu-id="34e60-176">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="34e60-177">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="34e60-177">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="34e60-178">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-178">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="34e60-179">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-179">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="34e60-180">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-180">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="34e60-181">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-181">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="34e60-182">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-182">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="34e60-183">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="34e60-183">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="34e60-184">如果不啟用和設定此原則，Microsoft Edge Update 將依照[「更新原則覆寫」](#update)原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-184">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>
#### <span data-ttu-id="34e60-185">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-185">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-186">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-186">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-187">GP 唯一名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-187">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="34e60-188">GP 名稱：更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="34e60-188">GP name: Update policy override default</span></span>
- <span data-ttu-id="34e60-189">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-189">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="34e60-190">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-190">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-191">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-191">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-192">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-192">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-193">值名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-193">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="34e60-194">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-194">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-195">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-195">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="34e60-196">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-196">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-197">Install</span><span class="sxs-lookup"><span data-stu-id="34e60-197">Install</span></span>
#### <span data-ttu-id="34e60-198">允許安裝</span><span class="sxs-lookup"><span data-stu-id="34e60-198">Allow installation</span></span>
><span data-ttu-id="34e60-199">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-199">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-200">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-200">Description</span></span>
<span data-ttu-id="34e60-201">指定是否可以使用 Microsoft Edge Update 安裝 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="34e60-201">Specifies whether a Microsoft Edge channel can be installed using Microsoft Edge Update.</span></span>

  <span data-ttu-id="34e60-202">如果為通道啟用此原則，則使用者可以透過 Microsoft Edge Update 安裝該 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="34e60-202">If you enable this policy for a channel, users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="34e60-203">如果為通道停用此原則，則使用者無法透過 Microsoft Edge Update 安裝該 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="34e60-203">If you disable this policy for a channel, users cannot install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>

  <span data-ttu-id="34e60-204">如果不為通道設定此原則，則「[允許安裝預設值](#installdefault)」原則設定將決定使用者是否可以透過 Microsoft Edge Update 安裝該 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="34e60-204">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge through Microsoft Edge Update.</span></span>
#### <span data-ttu-id="34e60-205">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-205">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-206">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-206">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-207">GP 唯一名稱：Install</span><span class="sxs-lookup"><span data-stu-id="34e60-207">GP unique name: Install</span></span>
- <span data-ttu-id="34e60-208">GP 名稱：允許安裝</span><span class="sxs-lookup"><span data-stu-id="34e60-208">GP name: Allow installation</span></span>
- <span data-ttu-id="34e60-209">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="34e60-209">GP path:</span></span> 
  - <span data-ttu-id="34e60-210">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34e60-210">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="34e60-211">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="34e60-211">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="34e60-212">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="34e60-212">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="34e60-213">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="34e60-213">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="34e60-214">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-214">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-215">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-215">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-216">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-216">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-217">值名稱：</span><span class="sxs-lookup"><span data-stu-id="34e60-217">Value Name:</span></span> 
  - <span data-ttu-id="34e60-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="34e60-218">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="34e60-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="34e60-219">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="34e60-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="34e60-220">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="34e60-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="34e60-221">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="34e60-222">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-222">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-223">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-223">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-224">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-224">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-225">Update</span><span class="sxs-lookup"><span data-stu-id="34e60-225">Update</span></span>
#### <span data-ttu-id="34e60-226">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-226">Update policy override</span></span>
><span data-ttu-id="34e60-227">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-227">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-228">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-228">Description</span></span>
<span data-ttu-id="34e60-229">指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-229">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

  <span data-ttu-id="34e60-230">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="34e60-230">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="34e60-231">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-231">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="34e60-232">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-232">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="34e60-233">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-233">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="34e60-234">(並非所有應用程式都提供此選項的介面。)</span><span class="sxs-lookup"><span data-stu-id="34e60-234">(Not all apps provide an interface for this option.)</span></span>
   - <span data-ttu-id="34e60-235">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-235">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="34e60-236">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-236">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="34e60-237">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="34e60-237">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="34e60-238">如果不啟用和設定此原則，Microsoft Edge Update 將依照「[更新原則覆寫預設值](#updatedefault)」原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-238">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>
#### <span data-ttu-id="34e60-239">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-239">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-240">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-240">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-241">GP 唯一名稱：Update</span><span class="sxs-lookup"><span data-stu-id="34e60-241">GP unique name: Update</span></span>
- <span data-ttu-id="34e60-242">GP 名稱：更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-242">GP name: Update policy override</span></span>
- <span data-ttu-id="34e60-243">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="34e60-243">GP path:</span></span> 
  - <span data-ttu-id="34e60-244">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34e60-244">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="34e60-245">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="34e60-245">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="34e60-246">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="34e60-246">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="34e60-247">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="34e60-247">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="34e60-248">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-248">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-249">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-249">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-250">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-250">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-251">值名稱：</span><span class="sxs-lookup"><span data-stu-id="34e60-251">Value Name:</span></span> 
  - <span data-ttu-id="34e60-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="34e60-252">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="34e60-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="34e60-253">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="34e60-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="34e60-254">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="34e60-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="34e60-255">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="34e60-256">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-256">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-257">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-257">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-258">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-258">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-259">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="34e60-259">Allowsxs</span></span>
#### <span data-ttu-id="34e60-260">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="34e60-260">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="34e60-261">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-261">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-262">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-262">Description</span></span>
<span data-ttu-id="34e60-263">此原則允許使用者並排執行 Microsoft Edge (Edge HTML) 和 Microsoft Edge (以 Chromium 為基礎)。</span><span class="sxs-lookup"><span data-stu-id="34e60-263">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="34e60-264">如果此原則設定為 [未設定]，則在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="34e60-264">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="34e60-265">這與 [停用] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="34e60-265">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="34e60-266">[停用] 設定會封鎖並排體驗，且在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="34e60-266">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="34e60-267">這與 [未設定] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="34e60-267">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="34e60-268">當此原則 [啟用] 時，Microsoft Edge (以 Chromium 為基礎) 和 Microsoft Edge (Edge HTML) 可以在安裝 Microsoft Edge (以 Chromium 為基礎) 後並排執行。</span><span class="sxs-lookup"><span data-stu-id="34e60-268">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="34e60-269">若要使此群組原則生效，必須在 Windows Update 自動安裝 Microsoft Edge (以 Chromium 為基礎) 之前進行設定。</span><span class="sxs-lookup"><span data-stu-id="34e60-269">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="34e60-270">注意：使用者可以使用 Microsoft Edge (以 Chromium 為基礎) 封鎖程式工具組來封鎖 Microsoft Edge (以 Chromium 為基礎) 的自動更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-270">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <span data-ttu-id="34e60-271">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-271">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-272">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-272">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-273">GP 唯一名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="34e60-273">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="34e60-274">GP 名稱：允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="34e60-274">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="34e60-275">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-275">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="34e60-276">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-276">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-277">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-277">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-278">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-278">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-279">值名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="34e60-279">Value Name: Allowsxs</span></span>
- <span data-ttu-id="34e60-280">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-280">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-281">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-281">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-282">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-282">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-283">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-283">CreateDesktopShortcutDefault</span></span>
#### <span data-ttu-id="34e60-284">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="34e60-284">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="34e60-285">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-285">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="34e60-286">說明</span><span class="sxs-lookup"><span data-stu-id="34e60-286">Description</span></span>
<span data-ttu-id="34e60-287">在安裝 Microsoft Edge 時，可讓您針對所有通道指定建立桌面捷徑的預設行為。</span><span class="sxs-lookup"><span data-stu-id="34e60-287">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="34e60-288">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-288">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="34e60-289">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-289">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="34e60-290">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-290">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="34e60-291">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="34e60-291">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <span data-ttu-id="34e60-292">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-292">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-293">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-293">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-294">GP 唯一名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-294">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="34e60-295">GP 名稱：防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="34e60-295">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="34e60-296">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="34e60-296">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="34e60-297">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-297">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-298">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-298">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-299">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-299">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-300">值名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="34e60-300">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="34e60-301">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-301">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-302">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-302">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-303">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-303">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-304">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="34e60-304">CreateDesktopShortcut</span></span>
#### <span data-ttu-id="34e60-305">防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="34e60-305">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="34e60-306">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-306">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <span data-ttu-id="34e60-307">說明</span><span class="sxs-lookup"><span data-stu-id="34e60-307">Description</span></span>
<span data-ttu-id="34e60-308">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-308">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="34e60-309">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-309">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="34e60-310">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-310">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="34e60-311">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="34e60-311">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="34e60-312">如果您未針對通道設定此原則，[[防止在安裝時建立桌面捷徑預設](#createdesktopshortcutdefault)] 原則設定會決定在安裝 Microsoft Edge 時建立捷徑。</span><span class="sxs-lookup"><span data-stu-id="34e60-312">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <span data-ttu-id="34e60-313">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-313">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-314">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-314">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-315">GP 唯一名稱：CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="34e60-315">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="34e60-316">GP 名稱：防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="34e60-316">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="34e60-317">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="34e60-317">GP path:</span></span> 
  - <span data-ttu-id="34e60-318">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34e60-318">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="34e60-319">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="34e60-319">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="34e60-320">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="34e60-320">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="34e60-321">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="34e60-321">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="34e60-322">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-322">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-323">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-323">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-324">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-324">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-325">Value Name:</span><span class="sxs-lookup"><span data-stu-id="34e60-325">Value Name:</span></span> 
  - <span data-ttu-id="34e60-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="34e60-326">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="34e60-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="34e60-327">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="34e60-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="34e60-328">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="34e60-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="34e60-329">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="34e60-330">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-330">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-331">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-331">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="34e60-332">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-332">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-333">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="34e60-333">TargetVersionPrefix</span></span>
#### <span data-ttu-id="34e60-334">目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-334">Target version override</span></span>
><span data-ttu-id="34e60-335">Microsoft Edge Update 1.3.119.43 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-335">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <span data-ttu-id="34e60-336">說明</span><span class="sxs-lookup"><span data-stu-id="34e60-336">Description</span></span>
<span data-ttu-id="34e60-337">啟用此原則且已啟用 [自動更新] 時，Microsoft Edge 將會更新為此原則值所指定的版本。</span><span class="sxs-lookup"><span data-stu-id="34e60-337">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="34e60-338">原則值必須是指定的 Microsoft Edge 版本，例如，83.0.499.12。</span><span class="sxs-lookup"><span data-stu-id="34e60-338">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="34e60-339">如果裝置的 Microsoft Edge 版本比指定值較新，Microsoft Edge 將會維持較新的版本，而不會降級到指定的版本。</span><span class="sxs-lookup"><span data-stu-id="34e60-339">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="34e60-340">如果指定的版本不存在，或格式不正確，Microsoft Edge 將會維持目前的版本，而不會自動更新至未來的版本。</span><span class="sxs-lookup"><span data-stu-id="34e60-340">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>
#### <span data-ttu-id="34e60-341">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-341">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-342">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-342">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-343">GP 唯一名稱：TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="34e60-343">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="34e60-344">GP 名稱：目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-344">GP name: Target version override</span></span>
- <span data-ttu-id="34e60-345">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="34e60-345">GP path:</span></span> 
  - <span data-ttu-id="34e60-346">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34e60-346">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="34e60-347">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="34e60-347">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="34e60-348">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="34e60-348">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="34e60-349">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="34e60-349">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="34e60-350">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-350">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-351">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-351">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-352">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-352">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-353">Value Name:</span><span class="sxs-lookup"><span data-stu-id="34e60-353">Value Name:</span></span> 
  - <span data-ttu-id="34e60-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="34e60-354">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="34e60-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="34e60-355">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="34e60-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="34e60-356">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="34e60-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="34e60-357">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="34e60-358">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="34e60-358">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="34e60-359">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-359">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="34e60-360">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-360">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="34e60-361">喜好設定原則</span><span class="sxs-lookup"><span data-stu-id="34e60-361">Preferences policies</span></span>

[<span data-ttu-id="34e60-362">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-362">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="34e60-363">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="34e60-363">AutoUpdateCheckPeriodMinutes</span></span>
#### <span data-ttu-id="34e60-364">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-364">Auto-update check period override</span></span>
><span data-ttu-id="34e60-365">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-365">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <span data-ttu-id="34e60-366">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-366">Description</span></span>
<span data-ttu-id="34e60-367">如果啟用，此原則允許您設定自動更新檢查之間的最小分鐘數值。</span><span class="sxs-lookup"><span data-stu-id="34e60-367">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="34e60-368">否則，預設情況下，每 10 小時會自動檢查一次是否有更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-368">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="34e60-369">如果要停用所有自動更新檢查，請將值設定為 0 (不建議)。</span><span class="sxs-lookup"><span data-stu-id="34e60-369">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <span data-ttu-id="34e60-370">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-370">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-371">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-371">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-372">GP 唯一名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="34e60-372">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="34e60-373">GP 名稱：自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="34e60-373">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="34e60-374">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="34e60-374">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="34e60-375">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-375">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-376">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-376">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-377">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-377">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-378">值名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="34e60-378">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="34e60-379">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-379">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-380">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-380">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="34e60-381">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-381">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-382">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="34e60-382">UpdatesSuppressed</span></span>
#### <span data-ttu-id="34e60-383">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="34e60-383">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="34e60-384">Microsoft Edge Update 1.3.33.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-384">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <span data-ttu-id="34e60-385">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-385">Description</span></span>
<span data-ttu-id="34e60-386">如果啟用此原則，則每天從 Hour:Minute 開始，持續 Duration (分鐘) 抑制檢查更新。</span><span class="sxs-lookup"><span data-stu-id="34e60-386">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="34e60-387">Duration 不受日光節約時間影響。</span><span class="sxs-lookup"><span data-stu-id="34e60-387">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="34e60-388">例如，如果開始時間為 22:00，Duration 為 480 分鐘，則無論日光節約時間在該期間是開始還是結束，都會抑制更新整整 8 小時。</span><span class="sxs-lookup"><span data-stu-id="34e60-388">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="34e60-389">如果停用或不設定此原則，則在任何特定期間都不會抑制更新檢查。</span><span class="sxs-lookup"><span data-stu-id="34e60-389">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <span data-ttu-id="34e60-390">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-390">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-391">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-391">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-392">GP 唯一名稱：UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="34e60-392">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="34e60-393">GP 名稱：每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="34e60-393">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="34e60-394">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="34e60-394">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="34e60-395">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="34e60-395">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="34e60-396">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-396">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-397">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-397">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-398">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-398">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-399">值名稱：</span><span class="sxs-lookup"><span data-stu-id="34e60-399">Value Name:</span></span> 
  - <span data-ttu-id="34e60-400">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="34e60-400">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="34e60-401">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="34e60-401">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="34e60-402">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="34e60-402">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="34e60-403">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="34e60-403">Value Type: REG_DWORD</span></span>
##### <span data-ttu-id="34e60-404">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-404">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="34e60-405">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-405">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="34e60-406">Proxy 伺服器原則</span><span class="sxs-lookup"><span data-stu-id="34e60-406">Proxy Server policies</span></span>
  
  

[<span data-ttu-id="34e60-407">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-407">Back to top</span></span>](#microsoft-edge---update-policies)
### <span data-ttu-id="34e60-408">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="34e60-408">ProxyMode</span></span>
#### <span data-ttu-id="34e60-409">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="34e60-409">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="34e60-410">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-410">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="34e60-411">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-411">Description</span></span>
<span data-ttu-id="34e60-412">允許您指定 Microsoft Edge Update 使用的 Proxy 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="34e60-412">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="34e60-413">如果啟用此原則，則可以在以下 Proxy 伺服器選項之間進行選擇：</span><span class="sxs-lookup"><span data-stu-id="34e60-413">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="34e60-414">如果選擇一律不使用 Proxy 伺服器且一律直接連線，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="34e60-414">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="34e60-415">如果選擇使用系統 Proxy 設定或自動偵測 Proxy 伺服器，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="34e60-415">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="34e60-416">如果選擇固定伺服器 Proxy 模式，則可在 [[Proxy 伺服器的位址或 URL](#proxyserver)] 原則中指定其他選項。</span><span class="sxs-lookup"><span data-stu-id="34e60-416">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="34e60-417">如果選擇使用 .pac Proxy 指令碼，則必須在 [[Proxy .pac 檔案的 URL](#proxypacurl)] 原則中指定指令碼的 URL。</span><span class="sxs-lookup"><span data-stu-id="34e60-417">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="34e60-418">如果啟用此原則，則組織的使用者無法變更 Microsoft Edge Update 中的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="34e60-418">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="34e60-419">如果停用或不設定此原則，則不會設定任何 Proxy 伺服器設定，但組織中的使用者可以為 Microsoft Edge Update 選擇自己的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="34e60-419">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <span data-ttu-id="34e60-420">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-420">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-421">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-421">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-422">GP 唯一名稱：ProxyMode</span><span class="sxs-lookup"><span data-stu-id="34e60-422">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="34e60-423">GP 名稱：選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="34e60-423">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="34e60-424">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="34e60-424">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="34e60-425">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-425">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-426">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-426">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-427">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-427">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-428">值名稱︰ProxyMode</span><span class="sxs-lookup"><span data-stu-id="34e60-428">Value Name: ProxyMode</span></span>
- <span data-ttu-id="34e60-429">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="34e60-429">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="34e60-430">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-430">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="34e60-431">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-431">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-432">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="34e60-432">ProxyPacUrl</span></span>
#### <span data-ttu-id="34e60-433">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-433">URL to a proxy .pac file</span></span>
><span data-ttu-id="34e60-434">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-434">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="34e60-435">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-435">Description</span></span>
<span data-ttu-id="34e60-436">允許您為 Proxy 自動設定 (PAC) 檔案指定 URL。</span><span class="sxs-lookup"><span data-stu-id="34e60-436">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="34e60-437">如果啟用此原則，則可以為 PAC 檔案指定 URL，以自動化 Microsoft Edge Update 選取適當 Proxy 伺服器以擷取特定網站的方式。</span><span class="sxs-lookup"><span data-stu-id="34e60-437">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="34e60-438">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-438">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="34e60-439">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-439">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="34e60-440">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-440">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-441">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-441">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-442">GP 唯一名稱：ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="34e60-442">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="34e60-443">GP 名稱：Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-443">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="34e60-444">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="34e60-444">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="34e60-445">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-445">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-446">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-446">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-447">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-447">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-448">值名稱︰ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="34e60-448">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="34e60-449">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="34e60-449">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="34e60-450">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-450">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="34e60-451">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-451">Back to top</span></span>](#microsoft-edge---update-policies)


### <span data-ttu-id="34e60-452">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="34e60-452">ProxyServer</span></span>
#### <span data-ttu-id="34e60-453">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-453">Address or URL of proxy server</span></span>
><span data-ttu-id="34e60-454">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="34e60-454">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <span data-ttu-id="34e60-455">描述</span><span class="sxs-lookup"><span data-stu-id="34e60-455">Description</span></span>
<span data-ttu-id="34e60-456">允許您指定供 Microsoft Edge Update 使用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="34e60-456">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="34e60-457">如果啟用此原則，您可在組織中設定 Microsoft Edge Update 所用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="34e60-457">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="34e60-458">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中選取手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-458">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="34e60-459">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="34e60-459">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <span data-ttu-id="34e60-460">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="34e60-460">Windows information and settings</span></span>
##### <span data-ttu-id="34e60-461">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="34e60-461">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="34e60-462">GP 唯一名稱：ProxyServer</span><span class="sxs-lookup"><span data-stu-id="34e60-462">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="34e60-463">GP 名稱：Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="34e60-463">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="34e60-464">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="34e60-464">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="34e60-465">GP ADMX 檔案名稱：edgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="34e60-465">GP ADMX file name: edgeupdate.admx</span></span>
##### <span data-ttu-id="34e60-466">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="34e60-466">Windows Registry Settings</span></span>
- <span data-ttu-id="34e60-467">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="34e60-467">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="34e60-468">值名稱︰ProxyServer</span><span class="sxs-lookup"><span data-stu-id="34e60-468">Value Name: ProxyServer</span></span>
- <span data-ttu-id="34e60-469">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="34e60-469">Value Type: REG_SZ</span></span>
##### <span data-ttu-id="34e60-470">範例值：</span><span class="sxs-lookup"><span data-stu-id="34e60-470">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="34e60-471">回到頁首</span><span class="sxs-lookup"><span data-stu-id="34e60-471">Back to top</span></span>](#microsoft-edge---update-policies)


## <span data-ttu-id="34e60-472">請參閱</span><span class="sxs-lookup"><span data-stu-id="34e60-472">See also</span></span>
  - [<span data-ttu-id="34e60-473">設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34e60-473">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="34e60-474">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="34e60-474">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
