---
title: Microsoft Edge Update 原則文件
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge Updater 支援的所有原則的文件
ms.openlocfilehash: a9808981acad544042c6e0ccb59ff755a670c848
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642319"
---
# <a name="microsoft-edge---update-policies"></a><span data-ttu-id="04318-103">Microsoft Edge - 更新原則</span><span class="sxs-lookup"><span data-stu-id="04318-103">Microsoft Edge - Update policies</span></span>

<span data-ttu-id="04318-104">最新版本的 Microsoft Edge 包括以下原則，可用於控制更新 Microsoft Edge 的方式和時間。</span><span class="sxs-lookup"><span data-stu-id="04318-104">The latest version of Microsoft Edge includes the following policies that you can use to control how and when Microsoft Edge is updated.</span></span>

<span data-ttu-id="04318-105">如需 Microsoft Edge 中提供的其他原則的相關資訊，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="04318-105">For information about other policies available in Microsoft Edge, check out [Microsoft Edge browser policy reference](microsoft-edge-policies.md)</span></span>
> [!NOTE]
> <span data-ttu-id="04318-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="04318-106">This article applies to Microsoft Edge version 77 or later.</span></span>
## <a name="available-policies"></a><span data-ttu-id="04318-107">可用原則</span><span class="sxs-lookup"><span data-stu-id="04318-107">Available policies</span></span>
<span data-ttu-id="04318-108">下表列出此版本 Microsoft Edge 提供的所有更新相關群組原則。</span><span class="sxs-lookup"><span data-stu-id="04318-108">These tables lists all of the update-related group policies available in this release of Microsoft Edge.</span></span> <span data-ttu-id="04318-109">使用下表中的連結，深入了解特定原則。</span><span class="sxs-lookup"><span data-stu-id="04318-109">Use the links in the table to get more details about specific policies.</span></span>

<span data-ttu-id="04318-110">|&nbsp;|&nbsp;| |**-**|-| |**[應用程式](#applications)**|[喜好設定](#preferences)| |**[Proxy 伺服器](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span><span class="sxs-lookup"><span data-stu-id="04318-110">|&nbsp;|&nbsp;| |**-**|-| |**[Applications](#applications)**|[Preferences](#preferences)| |**[Proxy Server](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|</span></span>
### [<a name="applications"></a><span data-ttu-id="04318-111">應用程式</span><span class="sxs-lookup"><span data-stu-id="04318-111">Applications</span></span>](#applications-policies)
|<span data-ttu-id="04318-112">原則名稱</span><span class="sxs-lookup"><span data-stu-id="04318-112">Policy Name</span></span>|<span data-ttu-id="04318-113">標題</span><span class="sxs-lookup"><span data-stu-id="04318-113">Caption</span></span>|
|-|-|
|[<span data-ttu-id="04318-114">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="04318-114">InstallDefault</span></span>](#installdefault)|<span data-ttu-id="04318-115">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="04318-115">Allow installation default</span></span>|
|[<span data-ttu-id="04318-116">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="04318-116">UpdateDefault</span></span>](#updatedefault)|<span data-ttu-id="04318-117">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="04318-117">Update policy override default</span></span>|
|[<span data-ttu-id="04318-118">Install</span><span class="sxs-lookup"><span data-stu-id="04318-118">Install</span></span>](#install)|<span data-ttu-id="04318-119">允許安裝 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="04318-119">Allow installation (per channel)</span></span>|
|[<span data-ttu-id="04318-120">Update</span><span class="sxs-lookup"><span data-stu-id="04318-120">Update</span></span>](#update)|<span data-ttu-id="04318-121">更新原則覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="04318-121">Update policy override (per channel)</span></span>|
|[<span data-ttu-id="04318-122">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="04318-122">Allowsxs</span></span>](#allowsxs)|<span data-ttu-id="04318-123">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="04318-123">Allow Microsoft Edge Side by Side browser experience</span></span>|
|[<span data-ttu-id="04318-124">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="04318-124">CreateDesktopShortcutDefault</span></span>](#createdesktopshortcutdefault)|<span data-ttu-id="04318-125">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="04318-125">Prevent Desktop Shortcut creation upon install default</span></span>|
|[<span data-ttu-id="04318-126">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="04318-126">CreateDesktopShortcut</span></span>](#createdesktopshortcut)|<span data-ttu-id="04318-127">防止在安裝時建立桌面捷徑 (每個通道)</span><span class="sxs-lookup"><span data-stu-id="04318-127">Prevent Desktop Shortcut creation upon install (per channel)</span></span>|
|[<span data-ttu-id="04318-128">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="04318-128">RollbackToTargetVersion</span></span>](#rollbacktotargetversion)|<span data-ttu-id="04318-129">復原至目標版本 (每個通道)</span><span class="sxs-lookup"><span data-stu-id="04318-129">Rollback to Target version (per channel)</span></span>|
|[<span data-ttu-id="04318-130">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="04318-130">TargetVersionPrefix</span></span>](#targetversionprefix)|<span data-ttu-id="04318-131">目標版本覆寫 (經由通道)</span><span class="sxs-lookup"><span data-stu-id="04318-131">Target version override (per channel)</span></span>|

### [<a name="preferences"></a><span data-ttu-id="04318-132">喜好設定</span><span class="sxs-lookup"><span data-stu-id="04318-132">Preferences</span></span>](#preferences-policies)
|<span data-ttu-id="04318-133">原則名稱</span><span class="sxs-lookup"><span data-stu-id="04318-133">Policy Name</span></span>|<span data-ttu-id="04318-134">標題</span><span class="sxs-lookup"><span data-stu-id="04318-134">Caption</span></span>|
|-|-|
|[<span data-ttu-id="04318-135">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="04318-135">AutoUpdateCheckPeriodMinutes</span></span>](#autoupdatecheckperiodminutes)|<span data-ttu-id="04318-136">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-136">Auto-update check period override</span></span>|
|[<span data-ttu-id="04318-137">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="04318-137">UpdatesSuppressed</span></span>](#updatessuppressed)|<span data-ttu-id="04318-138">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="04318-138">Time period in each day to suppress auto-update check</span></span>|

### [<a name="proxy-server"></a><span data-ttu-id="04318-139">Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="04318-139">Proxy Server</span></span>](#proxy-server-policies)
|<span data-ttu-id="04318-140">原則名稱</span><span class="sxs-lookup"><span data-stu-id="04318-140">Policy Name</span></span>|<span data-ttu-id="04318-141">說明文字</span><span class="sxs-lookup"><span data-stu-id="04318-141">Caption</span></span>|
|-|-|
|[<span data-ttu-id="04318-142">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="04318-142">ProxyMode</span></span>](#proxymode)|<span data-ttu-id="04318-143">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="04318-143">Choose how to specify proxy server settings</span></span>|
|[<span data-ttu-id="04318-144">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="04318-144">ProxyPacUrl</span></span>](#proxypacurl)|<span data-ttu-id="04318-145">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="04318-145">URL to a proxy .pac file</span></span>|
|[<span data-ttu-id="04318-146">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="04318-146">ProxyServer</span></span>](#proxyserver)|<span data-ttu-id="04318-147">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="04318-147">Address or URL of proxy server</span></span>|

### [<a name="microsoft-edge-webview"></a><span data-ttu-id="04318-148">Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="04318-148">Microsoft Edge WebView</span></span>](#microsoft-edge-webview-policies)
|<span data-ttu-id="04318-149">原則名稱</span><span class="sxs-lookup"><span data-stu-id="04318-149">Policy Name</span></span>|<span data-ttu-id="04318-150">標題</span><span class="sxs-lookup"><span data-stu-id="04318-150">Caption</span></span>|
|-|-|
|[<span data-ttu-id="04318-151">安裝</span><span class="sxs-lookup"><span data-stu-id="04318-151">Install</span></span>](#install-webview)|<span data-ttu-id="04318-152">允許安裝</span><span class="sxs-lookup"><span data-stu-id="04318-152">Allow installation</span></span>|
|[<span data-ttu-id="04318-153">更新</span><span class="sxs-lookup"><span data-stu-id="04318-153">Update</span></span>](#update-webview)|<span data-ttu-id="04318-154">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-154">Update policy override</span></span>|

## <a name="applications-policies"></a><span data-ttu-id="04318-155">應用程式原則</span><span class="sxs-lookup"><span data-stu-id="04318-155">Applications policies</span></span>

[<span data-ttu-id="04318-156">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-156">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="installdefault"></a><span data-ttu-id="04318-157">InstallDefault</span><span class="sxs-lookup"><span data-stu-id="04318-157">InstallDefault</span></span>
#### <a name="allow-installation-default"></a><span data-ttu-id="04318-158">允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="04318-158">Allow installation default</span></span>
><span data-ttu-id="04318-159">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-159">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-160">描述</span><span class="sxs-lookup"><span data-stu-id="04318-160">Description</span></span>
<span data-ttu-id="04318-161">您可以指定所有通道的預設行為，以便在加入網域的裝置上允許或封鎖 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="04318-161">You can specify the default behavior of all channels to allow or block Microsoft Edge on domain-joined devices.</span></span>

<span data-ttu-id="04318-162">您可以為特定通道啟用「[允許安裝](#install)」原則來覆寫各個通道的此原則。</span><span class="sxs-lookup"><span data-stu-id="04318-162">You can override this policy for individual channels by enabling the '[Allow installation](#install)' policy for specific channels.</span></span>

<span data-ttu-id="04318-163">如果停用此原則，則會封鎖 Microsoft Edge 安裝。</span><span class="sxs-lookup"><span data-stu-id="04318-163">If you disable this policy, the installation of Microsoft Edge is blocked.</span></span> <span data-ttu-id="04318-164">當 '[允許安裝](#install)' 原則設定為 [尚未設定] 時，只會影響 Microsoft Edge 軟體的安裝，。</span><span class="sxs-lookup"><span data-stu-id="04318-164">This only affects the installation of Microsoft Edge software when the '[Allow installation](#install)' policy is set to Not Configured.</span></span>

<span data-ttu-id="04318-165">此原則不會防止 Microsoft Edge Update 執行或防止使用者透過其他方法安裝 Microsoft Edge 軟體。</span><span class="sxs-lookup"><span data-stu-id="04318-165">This policy doesn't prevent Microsoft Edge Update from running or prevent users from installing Microsoft Edge software using other methods.</span></span>

<span data-ttu-id="04318-166">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-166">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-167">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-167">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-168">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-168">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-169">GP 唯一名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="04318-169">GP unique name: InstallDefault</span></span>
- <span data-ttu-id="04318-170">GP 名稱：允許安裝預設值</span><span class="sxs-lookup"><span data-stu-id="04318-170">GP name: Allow installation default</span></span>
- <span data-ttu-id="04318-171">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="04318-171">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="04318-172">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-172">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-173">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-173">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-174">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-174">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-175">值名稱：InstallDefault</span><span class="sxs-lookup"><span data-stu-id="04318-175">Value Name: InstallDefault</span></span>
- <span data-ttu-id="04318-176">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-176">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-177">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-177">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-178">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-178">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatedefault"></a><span data-ttu-id="04318-179">UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="04318-179">UpdateDefault</span></span>
#### <a name="update-policy-override-default"></a><span data-ttu-id="04318-180">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="04318-180">Update policy override default</span></span>
><span data-ttu-id="04318-181">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-181">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-182">描述</span><span class="sxs-lookup"><span data-stu-id="04318-182">Description</span></span>
<span data-ttu-id="04318-183">允許您指定所有通道的預設行為，這些通道涉及 Microsoft Edge Update 處理 Microsoft Edge 可用更新的方式。</span><span class="sxs-lookup"><span data-stu-id="04318-183">Lets you specify the default behavior for all channels concerning the way Microsoft Edge Update handles available updates for Microsoft Edge.</span></span> <span data-ttu-id="04318-184">可以透過為這些特定通道指定「[更新原則覆寫](#update)」原則來覆寫各個通道的設定。</span><span class="sxs-lookup"><span data-stu-id="04318-184">Can be overridden for individual channels by specifying the '[Update policy override](#update)' policy for those specific channels.</span></span>

  <span data-ttu-id="04318-185">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="04318-185">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
   - <span data-ttu-id="04318-186">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-186">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
   - <span data-ttu-id="04318-187">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-187">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
   - <span data-ttu-id="04318-188">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-188">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span>
   - <span data-ttu-id="04318-189">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-189">Updates disabled: Updates are never applied.</span></span>

  <span data-ttu-id="04318-190">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="04318-190">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="04318-191">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="04318-191">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

  <span data-ttu-id="04318-192">如果不啟用和設定此原則，Microsoft Edge Update 將依照[「更新原則覆寫」](#update)原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-192">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override](#update)' policy.</span></span>

  <span data-ttu-id="04318-193">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-193">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-194">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-194">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-195">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-195">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-196">GP 唯一名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="04318-196">GP unique name: UpdateDefault</span></span>
- <span data-ttu-id="04318-197">GP 名稱：更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="04318-197">GP name: Update policy override default</span></span>
- <span data-ttu-id="04318-198">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="04318-198">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="04318-199">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-199">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-200">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-200">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-201">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-201">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-202">值名稱：UpdateDefault</span><span class="sxs-lookup"><span data-stu-id="04318-202">Value Name: UpdateDefault</span></span>
- <span data-ttu-id="04318-203">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-203">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-204">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-204">Example value:</span></span>
```
0x00000003
```
[<span data-ttu-id="04318-205">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-205">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="install"></a><span data-ttu-id="04318-206">Install</span><span class="sxs-lookup"><span data-stu-id="04318-206">Install</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="04318-207">允許安裝</span><span class="sxs-lookup"><span data-stu-id="04318-207">Allow installation</span></span>
><span data-ttu-id="04318-208">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-208">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-209">描述</span><span class="sxs-lookup"><span data-stu-id="04318-209">Description</span></span>
<span data-ttu-id="04318-210">指定是否可以在加入網域的裝置上安裝 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="04318-210">Specifies whether a Microsoft Edge channel can be installed on domain-joined devices.</span></span>

  <span data-ttu-id="04318-211">如果您為通道啟用此原則，將不會封鎖 Microsoft Edge 的安裝。</span><span class="sxs-lookup"><span data-stu-id="04318-211">If you enable this policy for a channel, Microsoft Edge will not be blocked from installation.</span></span>

  <span data-ttu-id="04318-212">如果您為通道停用此原則，將會封鎖 Microsoft Edge 的安裝。</span><span class="sxs-lookup"><span data-stu-id="04318-212">If you disable this policy for a channel, Microsoft Edge will be blocked from installation.</span></span>

  <span data-ttu-id="04318-213">如果不為通道設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以安裝該 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="04318-213">If you don't configure this policy for a channel, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install that channel of Microsoft Edge.</span></span>

  <span data-ttu-id="04318-214">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-214">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-215">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-215">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-216">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-216">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-217">GP 唯一名稱：Install</span><span class="sxs-lookup"><span data-stu-id="04318-217">GP unique name: Install</span></span>
- <span data-ttu-id="04318-218">GP 名稱：允許安裝</span><span class="sxs-lookup"><span data-stu-id="04318-218">GP name: Allow installation</span></span>
- <span data-ttu-id="04318-219">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="04318-219">GP path:</span></span> 
  - <span data-ttu-id="04318-220">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-220">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="04318-221">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="04318-221">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="04318-222">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="04318-222">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="04318-223">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="04318-223">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="04318-224">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-224">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-225">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-225">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-226">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-226">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-227">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-227">Value Name:</span></span> 
  - <span data-ttu-id="04318-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="04318-228">(Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="04318-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="04318-229">(Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="04318-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="04318-230">(Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="04318-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="04318-231">(Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="04318-232">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-232">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-233">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-233">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-234">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-234">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update"></a><span data-ttu-id="04318-235">Update</span><span class="sxs-lookup"><span data-stu-id="04318-235">Update</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="04318-236">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-236">Update policy override</span></span>
><span data-ttu-id="04318-237">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-237">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-238">描述</span><span class="sxs-lookup"><span data-stu-id="04318-238">Description</span></span>
<span data-ttu-id="04318-239">指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-239">Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.</span></span>

<span data-ttu-id="04318-240">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：</span><span class="sxs-lookup"><span data-stu-id="04318-240">If you enable this policy, Microsoft Edge Update handles Microsoft Edge updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="04318-241">一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-241">Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.</span></span>
  - <span data-ttu-id="04318-242">僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-242">Automatic silent updates only: Updates are applied only when they're found by the periodic update check.</span></span>
  - <span data-ttu-id="04318-243">僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-243">Manual updates only: Updates are applied only when the user runs a manual update check.</span></span> <span data-ttu-id="04318-244">(並非所有應用程式都提供此選項的介面。)</span><span class="sxs-lookup"><span data-stu-id="04318-244">(Not all apps provide an interface for this option.)</span></span>
  - <span data-ttu-id="04318-245">停用更新：一律不套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-245">Updates disabled: Updates are never applied.</span></span>

<span data-ttu-id="04318-246">如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。</span><span class="sxs-lookup"><span data-stu-id="04318-246">If you select manual updates, make sure you periodically check for updates by using the app's manual update mechanism, if available.</span></span> <span data-ttu-id="04318-247">如果停用更新，請定期檢查更新，並將它們散發給使用者。</span><span class="sxs-lookup"><span data-stu-id="04318-247">If you disable updates, periodically check for updates, and distribute them to users.</span></span>

<span data-ttu-id="04318-248">如果不啟用和設定此原則，Microsoft Edge Update 將依照「[更新原則覆寫預設值](#updatedefault)」原則的指定方式處理可用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-248">If you don't enable and configure this policy, Microsoft Edge Update handles available updates as specified by the '[Update policy override default](#updatedefault)' policy.</span></span>

<span data-ttu-id="04318-249">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406)。</span><span class="sxs-lookup"><span data-stu-id="04318-249">See [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406) for more information.</span></span>

<span data-ttu-id="04318-250">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-250">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-251">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-251">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-252">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-252">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-253">GP 唯一名稱：Update</span><span class="sxs-lookup"><span data-stu-id="04318-253">GP unique name: Update</span></span>
- <span data-ttu-id="04318-254">GP 名稱：更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-254">GP name: Update policy override</span></span>
- <span data-ttu-id="04318-255">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="04318-255">GP path:</span></span> 
  - <span data-ttu-id="04318-256">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-256">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="04318-257">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="04318-257">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="04318-258">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="04318-258">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="04318-259">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="04318-259">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="04318-260">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-260">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-261">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-261">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-262">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-262">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-263">值名稱：</span><span class="sxs-lookup"><span data-stu-id="04318-263">Value Name:</span></span> 
  - <span data-ttu-id="04318-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="04318-264">(Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="04318-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="04318-265">(Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="04318-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="04318-266">(Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="04318-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="04318-267">(Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="04318-268">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-268">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-269">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-269">Example value:</span></span>
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[<span data-ttu-id="04318-270">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-270">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="allowsxs"></a><span data-ttu-id="04318-271">Allowsxs</span><span class="sxs-lookup"><span data-stu-id="04318-271">Allowsxs</span></span>
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a><span data-ttu-id="04318-272">允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="04318-272">Allow Microsoft Edge Side by Side browser experience</span></span>
><span data-ttu-id="04318-273">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-273">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-274">描述</span><span class="sxs-lookup"><span data-stu-id="04318-274">Description</span></span>
<span data-ttu-id="04318-275">此原則允許使用者並排執行 Microsoft Edge (Edge HTML) 和 Microsoft Edge (以 Chromium 為基礎)。</span><span class="sxs-lookup"><span data-stu-id="04318-275">This policy lets a user run Microsoft Edge (Edge HTML) and Microsoft Edge (Chromium-based) side-by-side.</span></span>

<span data-ttu-id="04318-276">如果此原則設定為 [未設定]，則在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="04318-276">If this policy is set to “Not configured”, Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="04318-277">這與 [停用] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="04318-277">This is the same behavior as the “Disabled” setting.</span></span>

<span data-ttu-id="04318-278">[停用] 設定會封鎖並排體驗，且在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。</span><span class="sxs-lookup"><span data-stu-id="04318-278">The “Disabled” setting blocks a side-by-side experience and Microsoft Edge (Chromium-based) will replace Microsoft Edge (Edge HTML) after the Microsoft Edge (Chromium-based) stable channel and the November 2019 security updates are installed.</span></span>  <span data-ttu-id="04318-279">這與 [未設定] 設定的行為相同。</span><span class="sxs-lookup"><span data-stu-id="04318-279">This is the same behavior as the “Not Configured” setting.</span></span>

<span data-ttu-id="04318-280">當此原則 [啟用] 時，Microsoft Edge (以 Chromium 為基礎) 和 Microsoft Edge (Edge HTML) 可以在安裝 Microsoft Edge (以 Chromium 為基礎) 後並排執行。</span><span class="sxs-lookup"><span data-stu-id="04318-280">When this policy is “Enabled”, Microsoft Edge (Chromium-based) and Microsoft Edge (Edge HTML) can run side-by-side after Microsoft Edge (Chromium-based) is installed.</span></span>

<span data-ttu-id="04318-281">若要使此群組原則生效，必須在 Windows Update 自動安裝 Microsoft Edge (以 Chromium 為基礎) 之前進行設定。</span><span class="sxs-lookup"><span data-stu-id="04318-281">For this group policy to take affect, it must be configured before the automatic install of Microsoft Edge (Chromium-based) by Windows Update.</span></span> <span data-ttu-id="04318-282">注意：使用者可以使用 Microsoft Edge (以 Chromium 為基礎) 封鎖程式工具組來封鎖 Microsoft Edge (以 Chromium 為基礎) 的自動更新。</span><span class="sxs-lookup"><span data-stu-id="04318-282">Note: A user can block the automatic update of Microsoft Edge (Chromium-based) by using the Microsoft Edge (Chromium-based) Blocker Toolkit.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-283">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-283">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-284">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-284">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-285">GP 唯一名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="04318-285">GP unique name: Allowsxs</span></span>
- <span data-ttu-id="04318-286">GP 名稱：允許 Microsoft Edge 並排瀏覽器體驗</span><span class="sxs-lookup"><span data-stu-id="04318-286">GP name: Allow Microsoft Edge Side by Side browser experience</span></span>
- <span data-ttu-id="04318-287">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="04318-287">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="04318-288">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-288">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-289">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-289">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-290">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-290">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-291">值名稱：Allowsxs</span><span class="sxs-lookup"><span data-stu-id="04318-291">Value Name: Allowsxs</span></span>
- <span data-ttu-id="04318-292">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-292">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-293">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-293">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-294">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-294">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcutdefault"></a><span data-ttu-id="04318-295">CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="04318-295">CreateDesktopShortcutDefault</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a><span data-ttu-id="04318-296">防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="04318-296">Prevent Desktop Shortcut creation upon install default</span></span>
><span data-ttu-id="04318-297">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-297">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-298">說明</span><span class="sxs-lookup"><span data-stu-id="04318-298">Description</span></span>
<span data-ttu-id="04318-299">在安裝 Microsoft Edge 時，可讓您針對所有通道指定建立桌面捷徑的預設行為。</span><span class="sxs-lookup"><span data-stu-id="04318-299">Lets you specify the default behavior for all channels for creating a desktop shortcut when Microsoft Edge is installed.</span></span>

  <span data-ttu-id="04318-300">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-300">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="04318-301">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-301">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="04318-302">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-302">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="04318-303">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="04318-303">If Microsoft Edge is already installed, this policy will have no effect.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-304">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-304">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-305">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-305">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-306">GP 唯一名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="04318-306">GP unique name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="04318-307">GP 名稱：防止在預設安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="04318-307">GP name: Prevent Desktop Shortcut creation upon install default</span></span>
- <span data-ttu-id="04318-308">GP 路徑：系統管理範本/Microsoft Edge Update/應用程式</span><span class="sxs-lookup"><span data-stu-id="04318-308">GP path: Administrative Templates/Microsoft Edge Update/Applications</span></span>
- <span data-ttu-id="04318-309">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-309">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-310">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-310">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-311">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-311">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-312">值名稱：CreateDesktopShortcutDefault</span><span class="sxs-lookup"><span data-stu-id="04318-312">Value Name: CreateDesktopShortcutDefault</span></span>
- <span data-ttu-id="04318-313">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-313">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-314">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-314">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-315">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-315">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a><span data-ttu-id="04318-316">CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="04318-316">CreateDesktopShortcut</span></span>
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a><span data-ttu-id="04318-317">防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="04318-317">Prevent Desktop Shortcut creation upon install</span></span>
><span data-ttu-id="04318-318">Microsoft Edge Update 1.3.128.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-318">Microsoft Edge Update 1.3.128.0 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-319">說明</span><span class="sxs-lookup"><span data-stu-id="04318-319">Description</span></span>
<span data-ttu-id="04318-320">如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-320">If you enable this policy a desktop shortcut is created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="04318-321">如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-321">If you disable this policy, no desktop shortcut will be created when Microsoft Edge is installed.</span></span>
<span data-ttu-id="04318-322">如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-322">If you don’t configure this policy a desktop shortcut to Microsoft Edge will be created during installation.</span></span>
<span data-ttu-id="04318-323">如果已安裝 Microsoft Edge，此原則就不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="04318-323">If Microsoft Edge is already installed, this policy will have no effect.</span></span>

  <span data-ttu-id="04318-324">如果您未針對通道設定此原則，[[防止在安裝時建立桌面捷徑預設](#createdesktopshortcutdefault)] 原則設定會決定在安裝 Microsoft Edge 時建立捷徑。</span><span class="sxs-lookup"><span data-stu-id="04318-324">If you don't configure this policy for a channel, the '[Prevent Desktop Shortcut creation upon install default](#createdesktopshortcutdefault)' policy configuration determines shortcut creation when Microsoft Edge is installed.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-325">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-325">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-326">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-326">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-327">GP 唯一名稱：CreateDesktopShortcut</span><span class="sxs-lookup"><span data-stu-id="04318-327">GP unique name: CreateDesktopShortcut</span></span>
- <span data-ttu-id="04318-328">GP 名稱：防止在安裝時建立桌面捷徑</span><span class="sxs-lookup"><span data-stu-id="04318-328">GP name: Prevent Desktop Shortcut creation upon install</span></span>
- <span data-ttu-id="04318-329">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="04318-329">GP path:</span></span> 
  - <span data-ttu-id="04318-330">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-330">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="04318-331">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="04318-331">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="04318-332">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="04318-332">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="04318-333">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="04318-333">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="04318-334">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-334">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-335">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-335">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-336">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-336">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-337">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-337">Value Name:</span></span> 
  - <span data-ttu-id="04318-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="04318-338">(Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="04318-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="04318-339">(Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="04318-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="04318-340">(Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="04318-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="04318-341">(Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="04318-342">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-342">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-343">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-343">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-344">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-344">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a><span data-ttu-id="04318-345">RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="04318-345">RollbackToTargetVersion</span></span>
#### <a name="rollback-to-target-version"></a><span data-ttu-id="04318-346">復原至目標版本</span><span class="sxs-lookup"><span data-stu-id="04318-346">Rollback to Target version</span></span>
><span data-ttu-id="04318-347">Microsoft Edge Update 1.3.133.3 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-347">Microsoft Edge Update 1.3.133.3 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-348">描述</span><span class="sxs-lookup"><span data-stu-id="04318-348">Description</span></span>
<span data-ttu-id="04318-349">指定 Microsoft Edge Update 應將 Microsoft Edge 的安裝復原為 '[目標版本覆寫](#targetversionprefix)' 中所示的版本。</span><span class="sxs-lookup"><span data-stu-id="04318-349">Specifies that Microsoft Edge Update should rollback installations of Microsoft Edge to the version indicated in '[Target version override](#targetversionprefix)'.</span></span>

<span data-ttu-id="04318-350">只有在設定 '[目標版本覆寫](#targetversionprefix)'，且將 '[更新原則覆寫](#update)' 設定為 [開啟] 狀態 (永遠允許更新、僅限自動無訊息更新、僅限手動更新) 時，此原則才會生效。</span><span class="sxs-lookup"><span data-stu-id="04318-350">This policy has no effect unless '[Target version override](#targetversionprefix)' is set and '[Update policy override](#update)' is set to one of the ON states (Always allow updates, Automatic silent updates only, Manual updates only).</span></span>

<span data-ttu-id="04318-351">如果您停用或未設定此原則，安裝的版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會保留原樣。</span><span class="sxs-lookup"><span data-stu-id="04318-351">If you disable this policy or don't configure it, installs that have a version higher than that specified by '[Target version override](#targetversionprefix)' will be left as-is.</span></span>

<span data-ttu-id="04318-352">如果您啟用這個原則，則目前版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會降級為目標版本。</span><span class="sxs-lookup"><span data-stu-id="04318-352">If you enable this policy, installs that have a current version higher than specified by the '[Target version override](#targetversionprefix)' will be downgraded to the target version.</span></span>

<span data-ttu-id="04318-353">建議使用者安裝最新版本的 Microsoft Edge 瀏覽器，以確保最新安全性更新的保護。</span><span class="sxs-lookup"><span data-stu-id="04318-353">We recommend that users install the latest version of the Microsoft Edge browser to ensure protection by the latest security updates.</span></span> <span data-ttu-id="04318-354">復原到舊版可能會面臨已知的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="04318-354">Rollback to an earlier version risks exposure to known security issues.</span></span> <span data-ttu-id="04318-355">這項原則可做為暫時修正，以解決 Microsoft Edge 瀏覽器更新中的問題。</span><span class="sxs-lookup"><span data-stu-id="04318-355">This policy is meant to be used as a temporary fix to address issues in a Microsoft Edge browser update.</span></span>

<span data-ttu-id="04318-356">在暫時復原瀏覽器版本之前，建議為貴組織中的所有使用者啟用同步處理 ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032))。</span><span class="sxs-lookup"><span data-stu-id="04318-356">Before temporarily rolling back your browser version, we recommend that you turn on Sync ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032)) for all users in your organization.</span></span> <span data-ttu-id="04318-357">如果未開啟同步，就會有瀏覽資料永久遺失的風險。</span><span class="sxs-lookup"><span data-stu-id="04318-357">If you don't turn on Sync, there is a risk of permanent browsing data loss.</span></span> <span data-ttu-id="04318-358">請自行承擔使用此原則的風險。</span><span class="sxs-lookup"><span data-stu-id="04318-358">Use this policy at your own risk.</span></span>

<span data-ttu-id="04318-359">注意：您可以在這裡檢視所有可供復原的版本[https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise)。</span><span class="sxs-lookup"><span data-stu-id="04318-359">Note: All versions available for rollback can be viewed here [https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="04318-360">本原則適用於 Microsoft Edge 版本 86 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="04318-360">This policy applies to Microsoft Edge version 86 or later.</span></span>

<span data-ttu-id="04318-361">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918)。</span><span class="sxs-lookup"><span data-stu-id="04318-361">See [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918) for more information.</span></span>

<span data-ttu-id="04318-362">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-362">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-363">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-363">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-364">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-364">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-365">GP 唯一名稱：RollbackToTargetVersion</span><span class="sxs-lookup"><span data-stu-id="04318-365">GP unique name: RollbackToTargetVersion</span></span>
- <span data-ttu-id="04318-366">GP 名稱：復原至目標版本</span><span class="sxs-lookup"><span data-stu-id="04318-366">GP name: Rollback to Target version</span></span>
- <span data-ttu-id="04318-367">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="04318-367">GP path:</span></span> 
  - <span data-ttu-id="04318-368">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-368">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="04318-369">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="04318-369">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="04318-370">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="04318-370">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="04318-371">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="04318-371">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="04318-372">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-372">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-373">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-373">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-374">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-374">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-375">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-375">Value Name:</span></span> 
  - <span data-ttu-id="04318-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="04318-376">(Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="04318-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="04318-377">(Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="04318-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="04318-378">(Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="04318-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="04318-379">(Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="04318-380">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-380">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-381">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-381">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-382">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-382">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a><span data-ttu-id="04318-383">TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="04318-383">TargetVersionPrefix</span></span>
#### <a name="target-version-override"></a><span data-ttu-id="04318-384">目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-384">Target version override</span></span>
><span data-ttu-id="04318-385">Microsoft Edge Update 1.3.119.43 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-385">Microsoft Edge Update 1.3.119.43 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-386">說明</span><span class="sxs-lookup"><span data-stu-id="04318-386">Description</span></span>
<span data-ttu-id="04318-387">啟用此原則且已啟用 [自動更新] 時，Microsoft Edge 將會更新為此原則值所指定的版本。</span><span class="sxs-lookup"><span data-stu-id="04318-387">When this policy is enabled, and auto-update is enabled, Microsoft Edge will be updated to the version specified by this policy value.</span></span>

<span data-ttu-id="04318-388">原則值必須是指定的 Microsoft Edge 版本，例如，83.0.499.12。</span><span class="sxs-lookup"><span data-stu-id="04318-388">The policy value must be a specific Microsoft Edge version, e.g. 83.0.499.12.</span></span>

<span data-ttu-id="04318-389">如果裝置的 Microsoft Edge 版本比指定值較新，Microsoft Edge 將會維持較新的版本，而不會降級到指定的版本。</span><span class="sxs-lookup"><span data-stu-id="04318-389">If a device has newer version of Microsoft Edge than the value specified, Microsoft Edge will remain on the newer version and not downgrade to the specified version.</span></span>

<span data-ttu-id="04318-390">如果指定的版本不存在，或格式不正確，Microsoft Edge 將會維持目前的版本，而不會自動更新至未來的版本。</span><span class="sxs-lookup"><span data-stu-id="04318-390">If the specified version does not exist, or is improperly formatted, then Microsoft Edge will remain on its current version and not update to future versions automatically.</span></span>

<span data-ttu-id="04318-391">如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707)。</span><span class="sxs-lookup"><span data-stu-id="04318-391">See [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707) for more information.</span></span>

<span data-ttu-id="04318-392">這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。</span><span class="sxs-lookup"><span data-stu-id="04318-392">This policy is available only on Windows instances that are joined to a Microsoft® Active Directory® domain.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-393">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-393">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-394">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-394">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-395">GP 唯一名稱：TargetVersionPrefix</span><span class="sxs-lookup"><span data-stu-id="04318-395">GP unique name: TargetVersionPrefix</span></span>
- <span data-ttu-id="04318-396">GP 名稱：目標版本覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-396">GP name: Target version override</span></span>
- <span data-ttu-id="04318-397">GP 路徑：</span><span class="sxs-lookup"><span data-stu-id="04318-397">GP path:</span></span> 
  - <span data-ttu-id="04318-398">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-398">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge</span></span>
  - <span data-ttu-id="04318-399">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta</span><span class="sxs-lookup"><span data-stu-id="04318-399">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Beta</span></span>
  - <span data-ttu-id="04318-400">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary</span><span class="sxs-lookup"><span data-stu-id="04318-400">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Canary</span></span>
  - <span data-ttu-id="04318-401">系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="04318-401">Administrative Templates/Microsoft Edge Update/Applications/Microsoft Edge Dev</span></span>
- <span data-ttu-id="04318-402">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-402">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-403">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-403">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-404">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-404">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-405">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-405">Value Name:</span></span> 
  - <span data-ttu-id="04318-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span><span class="sxs-lookup"><span data-stu-id="04318-406">(Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}</span></span>
  - <span data-ttu-id="04318-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span><span class="sxs-lookup"><span data-stu-id="04318-407">(Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}</span></span>
  - <span data-ttu-id="04318-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span><span class="sxs-lookup"><span data-stu-id="04318-408">(Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}</span></span>
  - <span data-ttu-id="04318-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span><span class="sxs-lookup"><span data-stu-id="04318-409">(Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}</span></span>
- <span data-ttu-id="04318-410">值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="04318-410">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-411">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-411">Example value:</span></span>
```
83.0.499.12
```
[<span data-ttu-id="04318-412">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-412">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="preferences-policies"></a><span data-ttu-id="04318-413">喜好設定原則</span><span class="sxs-lookup"><span data-stu-id="04318-413">Preferences policies</span></span>

[<span data-ttu-id="04318-414">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-414">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a><span data-ttu-id="04318-415">AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="04318-415">AutoUpdateCheckPeriodMinutes</span></span>
#### <a name="auto-update-check-period-override"></a><span data-ttu-id="04318-416">自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-416">Auto-update check period override</span></span>
><span data-ttu-id="04318-417">Microsoft Edge Update 1.2.145.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-417">Microsoft Edge Update 1.2.145.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-418">描述</span><span class="sxs-lookup"><span data-stu-id="04318-418">Description</span></span>
<span data-ttu-id="04318-419">如果啟用，此原則允許您設定自動更新檢查之間的最小分鐘數值。</span><span class="sxs-lookup"><span data-stu-id="04318-419">If enabled, this policy lets you set a value for the minimum number of minutes between automatic update checks.</span></span> <span data-ttu-id="04318-420">否則，預設情況下，每 10 小時會自動檢查一次是否有更新。</span><span class="sxs-lookup"><span data-stu-id="04318-420">Otherwise, by default, auto-update checks for updates every 10 hours.</span></span>

  <span data-ttu-id="04318-421">如果要停用所有自動更新檢查，請將值設定為 0 (不建議)。</span><span class="sxs-lookup"><span data-stu-id="04318-421">If you want to disable all auto-update checks, set the value to 0 (not recommended).</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-422">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-422">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-423">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-423">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-424">GP 唯一名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="04318-424">GP unique name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="04318-425">GP 名稱：自動更新檢查期間覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-425">GP name: Auto-update check period override</span></span>
- <span data-ttu-id="04318-426">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="04318-426">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="04318-427">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-427">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-428">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-428">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-429">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-429">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-430">值名稱：AutoUpdateCheckPeriodMinutes</span><span class="sxs-lookup"><span data-stu-id="04318-430">Value Name: AutoUpdateCheckPeriodMinutes</span></span>
- <span data-ttu-id="04318-431">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-431">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-432">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-432">Example value:</span></span>
```
0x00000578
```
[<span data-ttu-id="04318-433">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-433">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a><span data-ttu-id="04318-434">UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="04318-434">UpdatesSuppressed</span></span>
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a><span data-ttu-id="04318-435">每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="04318-435">Time period in each day to suppress auto-update check</span></span>
><span data-ttu-id="04318-436">Microsoft Edge Update 1.3.33.5 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-436">Microsoft Edge Update 1.3.33.5 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-437">描述</span><span class="sxs-lookup"><span data-stu-id="04318-437">Description</span></span>
<span data-ttu-id="04318-438">如果啟用此原則，則每天從 Hour:Minute 開始，持續 Duration (分鐘) 抑制檢查更新。</span><span class="sxs-lookup"><span data-stu-id="04318-438">If you enable this policy, update checks are suppressed each day starting at Hour:Minute for a period of Duration (in minutes).</span></span> <span data-ttu-id="04318-439">Duration 不受日光節約時間影響。</span><span class="sxs-lookup"><span data-stu-id="04318-439">Duration isn't affected by daylight saving time.</span></span> <span data-ttu-id="04318-440">例如，如果開始時間為 22:00，Duration 為 480 分鐘，則無論日光節約時間在該期間是開始還是結束，都會抑制更新整整 8 小時。</span><span class="sxs-lookup"><span data-stu-id="04318-440">For example, if the start time is 22:00 and the duration is 480 minutes, updates will be suppressed for exactly 8 hours, regardless of whether daylight saving time starts or ends during this period.</span></span>

  <span data-ttu-id="04318-441">如果停用或不設定此原則，則在任何特定期間都不會抑制更新檢查。</span><span class="sxs-lookup"><span data-stu-id="04318-441">If you disable or don't configure this policy, update checks aren't suppressed during any specific period.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-442">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-442">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-443">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-443">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-444">GP 唯一名稱：UpdatesSuppressed</span><span class="sxs-lookup"><span data-stu-id="04318-444">GP unique name: UpdatesSuppressed</span></span>
- <span data-ttu-id="04318-445">GP 名稱：每天抑制自動更新檢查的期間</span><span class="sxs-lookup"><span data-stu-id="04318-445">GP name: Time period in each day to suppress auto-update check</span></span>
  - <span data-ttu-id="04318-446">Options { Hour, Minute, Duration }</span><span class="sxs-lookup"><span data-stu-id="04318-446">Options { Hour, Minute, Duration }</span></span>
- <span data-ttu-id="04318-447">GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定</span><span class="sxs-lookup"><span data-stu-id="04318-447">GP path: Administrative Templates/Microsoft Edge Update/Preferences</span></span>
- <span data-ttu-id="04318-448">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-448">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-449">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-449">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-450">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-450">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-451">值名稱：</span><span class="sxs-lookup"><span data-stu-id="04318-451">Value Name:</span></span> 
  - <span data-ttu-id="04318-452">UpdatesSuppressedDurationMin</span><span class="sxs-lookup"><span data-stu-id="04318-452">UpdatesSuppressedDurationMin</span></span>
  - <span data-ttu-id="04318-453">UpdatesSuppressedStartHour</span><span class="sxs-lookup"><span data-stu-id="04318-453">UpdatesSuppressedStartHour</span></span>
  - <span data-ttu-id="04318-454">UpdatesSuppressedStartMin</span><span class="sxs-lookup"><span data-stu-id="04318-454">UpdatesSuppressedStartMin</span></span>
- <span data-ttu-id="04318-455">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-455">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-456">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-456">Example value:</span></span>
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[<span data-ttu-id="04318-457">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-457">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="proxy-server-policies"></a><span data-ttu-id="04318-458">Proxy 伺服器原則</span><span class="sxs-lookup"><span data-stu-id="04318-458">Proxy Server policies</span></span>

[<span data-ttu-id="04318-459">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-459">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="proxymode"></a><span data-ttu-id="04318-460">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="04318-460">ProxyMode</span></span>
#### <a name="choose-how-to-specify-proxy-server-settings"></a><span data-ttu-id="04318-461">選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="04318-461">Choose how to specify proxy server settings</span></span>
><span data-ttu-id="04318-462">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-462">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-463">描述</span><span class="sxs-lookup"><span data-stu-id="04318-463">Description</span></span>
<span data-ttu-id="04318-464">允許您指定 Microsoft Edge Update 使用的 Proxy 伺服器設定。</span><span class="sxs-lookup"><span data-stu-id="04318-464">Allows you to specify the proxy server settings that are used by Microsoft Edge Update.</span></span>

  <span data-ttu-id="04318-465">如果啟用此原則，則可以在以下 Proxy 伺服器選項之間進行選擇：</span><span class="sxs-lookup"><span data-stu-id="04318-465">If you enable this policy, you can choose between the following proxy server options:</span></span>
   - <span data-ttu-id="04318-466">如果選擇一律不使用 Proxy 伺服器且一律直接連線，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="04318-466">If you choose to never use a proxy server and always connect directly, all other options are ignored.</span></span>
   - <span data-ttu-id="04318-467">如果選擇使用系統 Proxy 設定或自動偵測 Proxy 伺服器，則忽略所有其他選項。</span><span class="sxs-lookup"><span data-stu-id="04318-467">If you choose to use system proxy settings or auto-detect the proxy server, all other options are ignored.</span></span>
   - <span data-ttu-id="04318-468">如果選擇固定伺服器 Proxy 模式，則可在 [[Proxy 伺服器的位址或 URL](#proxyserver)] 原則中指定其他選項。</span><span class="sxs-lookup"><span data-stu-id="04318-468">If you choose fixed server proxy mode, you can specify further options in '[Address or URL of proxy server](#proxyserver)' policy.</span></span>
   - <span data-ttu-id="04318-469">如果選擇使用 .pac Proxy 指令碼，則必須在 [[Proxy .pac 檔案的 URL](#proxypacurl)] 原則中指定指令碼的 URL。</span><span class="sxs-lookup"><span data-stu-id="04318-469">If you choose to use a .pac proxy script, you must specify the URL for the script in '[URL to a proxy .pac file](#proxypacurl)' policy.</span></span>

  <span data-ttu-id="04318-470">如果啟用此原則，則組織的使用者無法變更 Microsoft Edge Update 中的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="04318-470">If you enable this policy, users in your organization can't change the proxy settings in Microsoft Edge Update.</span></span>

  <span data-ttu-id="04318-471">如果停用或不設定此原則，則不會設定任何 Proxy 伺服器設定，但組織中的使用者可以為 Microsoft Edge Update 選擇自己的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="04318-471">If you disable or don't configure this policy, no proxy server settings are configured, but users in your organization can choose their own proxy settings for Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-472">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-472">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-473">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-473">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-474">GP 唯一名稱：ProxyMode</span><span class="sxs-lookup"><span data-stu-id="04318-474">GP unique name: ProxyMode</span></span>
- <span data-ttu-id="04318-475">GP 名稱：選擇如何指定 Proxy 伺服器設定</span><span class="sxs-lookup"><span data-stu-id="04318-475">GP name: Choose how to specify proxy server settings</span></span>
- <span data-ttu-id="04318-476">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="04318-476">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="04318-477">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-477">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-478">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-478">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-479">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-479">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-480">值名稱︰ProxyMode</span><span class="sxs-lookup"><span data-stu-id="04318-480">Value Name: ProxyMode</span></span>
- <span data-ttu-id="04318-481">數值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="04318-481">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-482">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-482">Example value:</span></span>
```
fixed_servers
```
[<span data-ttu-id="04318-483">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-483">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a><span data-ttu-id="04318-484">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="04318-484">ProxyPacUrl</span></span>
#### <a name="url-to-a-proxy-pac-file"></a><span data-ttu-id="04318-485">Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="04318-485">URL to a proxy .pac file</span></span>
><span data-ttu-id="04318-486">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-486">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-487">描述</span><span class="sxs-lookup"><span data-stu-id="04318-487">Description</span></span>
<span data-ttu-id="04318-488">允許您為 Proxy 自動設定 (PAC) 檔案指定 URL。</span><span class="sxs-lookup"><span data-stu-id="04318-488">Allows you to specify a URL for a proxy auto-config (PAC) file.</span></span>

  <span data-ttu-id="04318-489">如果啟用此原則，則可以為 PAC 檔案指定 URL，以自動化 Microsoft Edge Update 選取適當 Proxy 伺服器以擷取特定網站的方式。</span><span class="sxs-lookup"><span data-stu-id="04318-489">If you enable this policy, you can specify a URL for a PAC file to automate how Microsoft Edge Update selects the appropriate proxy server for fetching a particular website.</span></span>

  <span data-ttu-id="04318-490">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="04318-490">This policy is applied only if you have specified manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="04318-491">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="04318-491">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-492">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-492">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-493">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-493">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-494">GP 唯一名稱：ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="04318-494">GP unique name: ProxyPacUrl</span></span>
- <span data-ttu-id="04318-495">GP 名稱：Proxy .pac 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="04318-495">GP name: URL to a proxy .pac file</span></span>
- <span data-ttu-id="04318-496">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="04318-496">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="04318-497">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-497">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-498">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-498">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-499">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-499">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-500">值名稱︰ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="04318-500">Value Name: ProxyPacUrl</span></span>
- <span data-ttu-id="04318-501">數值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="04318-501">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-502">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-502">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="04318-503">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-503">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="proxyserver"></a><span data-ttu-id="04318-504">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="04318-504">ProxyServer</span></span>
#### <a name="address-or-url-of-proxy-server"></a><span data-ttu-id="04318-505">Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="04318-505">Address or URL of proxy server</span></span>
><span data-ttu-id="04318-506">Microsoft Edge Update 1.3.21.81 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-506">Microsoft Edge Update 1.3.21.81 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-507">描述</span><span class="sxs-lookup"><span data-stu-id="04318-507">Description</span></span>
<span data-ttu-id="04318-508">允許您指定供 Microsoft Edge Update 使用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="04318-508">Allows you to specify the URL of the proxy server for Microsoft Edge Update to use.</span></span>

  <span data-ttu-id="04318-509">如果啟用此原則，您可在組織中設定 Microsoft Edge Update 所用的 Proxy 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="04318-509">If you enable this policy, you can set the proxy server URL used by Microsoft Edge Update in your organization.</span></span>

  <span data-ttu-id="04318-510">已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中選取手動 Proxy 設定時，才會套用此原則。</span><span class="sxs-lookup"><span data-stu-id="04318-510">This policy is applied only if you have selected manual proxy settings in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>

  <span data-ttu-id="04318-511">如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。</span><span class="sxs-lookup"><span data-stu-id="04318-511">Don't configure this policy if you have selected a proxy setting other than manual in the '[Choose how to specify proxy server settings](#proxymode)' policy.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-512">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-512">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-513">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-513">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-514">GP 唯一名稱：ProxyServer</span><span class="sxs-lookup"><span data-stu-id="04318-514">GP unique name: ProxyServer</span></span>
- <span data-ttu-id="04318-515">GP 名稱：Proxy 伺服器的位址或 URL</span><span class="sxs-lookup"><span data-stu-id="04318-515">GP name: Address or URL of proxy server</span></span>
- <span data-ttu-id="04318-516">GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器</span><span class="sxs-lookup"><span data-stu-id="04318-516">GP path: Administrative Templates/Microsoft Edge Update/Proxy Server</span></span>
- <span data-ttu-id="04318-517">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-517">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-518">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-518">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-519">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-519">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-520">值名稱︰ProxyServer</span><span class="sxs-lookup"><span data-stu-id="04318-520">Value Name: ProxyServer</span></span>
- <span data-ttu-id="04318-521">數值類型：REG_SZ</span><span class="sxs-lookup"><span data-stu-id="04318-521">Value Type: REG_SZ</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-522">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-522">Example value:</span></span>
```
https://www.microsoft.com
```
[<span data-ttu-id="04318-523">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-523">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a><span data-ttu-id="04318-524">Microsoft Edge WebView 原則</span><span class="sxs-lookup"><span data-stu-id="04318-524">Microsoft Edge WebView policies</span></span>

[<span data-ttu-id="04318-525">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-525">Back to top</span></span>](#microsoft-edge---update-policies)
### <a name="install-webview"></a><span data-ttu-id="04318-526">安裝 (WebView)</span><span class="sxs-lookup"><span data-stu-id="04318-526">Install (WebView)</span></span>
#### <a name="allow-installation"></a><span data-ttu-id="04318-527">允許安裝</span><span class="sxs-lookup"><span data-stu-id="04318-527">Allow installation</span></span>
><span data-ttu-id="04318-528">Microsoft Edge Update 1.3.127.1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-528">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-529">說明</span><span class="sxs-lookup"><span data-stu-id="04318-529">Description</span></span>
<span data-ttu-id="04318-530">可讓您指定是否可以使用 Microsoft Edge Update 來安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="04318-530">Lets you specify whether Microsoft Edge WebView can be installed using Microsoft Edge Update.</span></span>

  - <span data-ttu-id="04318-531">如果您啟用此原則，使用者可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="04318-531">If you enable this policy, users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="04318-532">如果您停用此原則，使用者無法透過 Microsoft Edge Upadte 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="04318-532">If you disable this policy, users cannot install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
  - <span data-ttu-id="04318-533">如果不為設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。</span><span class="sxs-lookup"><span data-stu-id="04318-533">If you don't configure this policy, the '[Allow installation default](#installdefault)' policy configuration determines whether users can install Microsoft Edge WebView through Microsoft Edge Update.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-534">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-534">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-535">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-535">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-536">GP 唯一名稱：Install</span><span class="sxs-lookup"><span data-stu-id="04318-536">GP unique name: Install</span></span>
- <span data-ttu-id="04318-537">GP 名稱：允許安裝</span><span class="sxs-lookup"><span data-stu-id="04318-537">GP name: Allow installation</span></span>
- <span data-ttu-id="04318-538">GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="04318-538">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="04318-539">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-539">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-540">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-540">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-541">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-541">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-542">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-542">Value Name:</span></span> 
  - <span data-ttu-id="04318-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="04318-543">Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="04318-544">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-544">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-545">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-545">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-546">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-546">Back to top</span></span>](#microsoft-edge---update-policies)


### <a name="update-webview"></a><span data-ttu-id="04318-547">更新 (WebView)</span><span class="sxs-lookup"><span data-stu-id="04318-547">Update (WebView)</span></span>
#### <a name="update-policy-override"></a><span data-ttu-id="04318-548">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-548">Update policy override</span></span>
><span data-ttu-id="04318-549">Microsoft Edge Update 1.3.127.1 和更新版本</span><span class="sxs-lookup"><span data-stu-id="04318-549">Microsoft Edge Update 1.3.127.1 and later</span></span>

#### <a name="description"></a><span data-ttu-id="04318-550">說明</span><span class="sxs-lookup"><span data-stu-id="04318-550">Description</span></span>
<span data-ttu-id="04318-551">可讓您指定是否為 Microsoft Edge WebView 啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="04318-551">Lets you specify whether or not automatic updates are enabled for Microsoft Edge WebView.</span></span> <span data-ttu-id="04318-552">Microsoft Edge WebView 是應用程式用來顯示網路內容的元件。</span><span class="sxs-lookup"><span data-stu-id="04318-552">Microsoft Edge WebView is a component used by applications to display web content.</span></span>
<span data-ttu-id="04318-553">預設會啟用自動更新。</span><span class="sxs-lookup"><span data-stu-id="04318-553">Automatic updates are enabled by default.</span></span> <span data-ttu-id="04318-554">若要停用 Microsoft Edge WebView 的自動更新，可能會導致與此元件相關的應用程式發生相容性問題。</span><span class="sxs-lookup"><span data-stu-id="04318-554">Disabling automatic updates for Microsoft Edge WebView might cause compatibility issues with applications that depend on this component.</span></span>

  <span data-ttu-id="04318-555">如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge WebView 更新：</span><span class="sxs-lookup"><span data-stu-id="04318-555">If you enable this policy, Microsoft Edge Update handles Microsoft Edge WebView updates according to how you configure the following options:</span></span>
  - <span data-ttu-id="04318-556">永遠允許更新：會自動下載並套用更新</span><span class="sxs-lookup"><span data-stu-id="04318-556">Always allow updates: Updates are automatically downloaded and applied</span></span>
  - <span data-ttu-id="04318-557">已停用更新：一律不下載或套用更新</span><span class="sxs-lookup"><span data-stu-id="04318-557">Updates disabled: Updates are never downloaded or applied</span></span>

  <span data-ttu-id="04318-558">如果您未啟用此原則，則會自動下載並套用更新。</span><span class="sxs-lookup"><span data-stu-id="04318-558">If you don't enable this policy, updates are automatically downloaded and applied.</span></span>
#### <a name="windows-information-and-settings"></a><span data-ttu-id="04318-559">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="04318-559">Windows information and settings</span></span>
##### <a name="group-policy-admx-info"></a><span data-ttu-id="04318-560">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="04318-560">Group Policy (ADMX) info</span></span>
- <span data-ttu-id="04318-561">GP 唯一名稱：Update</span><span class="sxs-lookup"><span data-stu-id="04318-561">GP unique name: Update</span></span>
- <span data-ttu-id="04318-562">GP 名稱：更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="04318-562">GP name: Update policy override</span></span>
- <span data-ttu-id="04318-563">GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="04318-563">GP path: Administrative Templates/Microsoft Edge Update/Microsoft Edge WebView</span></span>
- <span data-ttu-id="04318-564">GP ADMX 檔案名稱：msedgeupdate.admx</span><span class="sxs-lookup"><span data-stu-id="04318-564">GP ADMX file name: msedgeupdate.admx</span></span>
##### <a name="windows-registry-settings"></a><span data-ttu-id="04318-565">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="04318-565">Windows Registry Settings</span></span>
- <span data-ttu-id="04318-566">路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span><span class="sxs-lookup"><span data-stu-id="04318-566">Path: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate</span></span>
- <span data-ttu-id="04318-567">Value Name:</span><span class="sxs-lookup"><span data-stu-id="04318-567">Value Name:</span></span> 
  - <span data-ttu-id="04318-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span><span class="sxs-lookup"><span data-stu-id="04318-568">Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}</span></span>
- <span data-ttu-id="04318-569">值類型：REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="04318-569">Value Type: REG_DWORD</span></span>
##### <a name="example-value"></a><span data-ttu-id="04318-570">範例值：</span><span class="sxs-lookup"><span data-stu-id="04318-570">Example value:</span></span>
```
0x00000001
```
[<span data-ttu-id="04318-571">回到頁首</span><span class="sxs-lookup"><span data-stu-id="04318-571">Back to top</span></span>](#microsoft-edge---update-policies)


## <a name="see-also"></a><span data-ttu-id="04318-572">請參閱</span><span class="sxs-lookup"><span data-stu-id="04318-572">See also</span></span>
  - [<span data-ttu-id="04318-573">設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04318-573">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
  - [<span data-ttu-id="04318-574">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="04318-574">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
