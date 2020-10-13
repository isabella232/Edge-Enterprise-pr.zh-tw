---
title: Microsoft Edge 瀏覽器原則文件
ms.author: stmoody
author: brianalt-msft
manager: tahills
ms.date: 10/08/2020
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge 瀏覽器支援的所有原則的 Windows 和 Mac 文件
ms.openlocfilehash: 56abadf907dfffec733af2456cc20db36510880b
ms.sourcegitcommit: 4e6188ade942ca6fd599a4ce1c8e0d90d3d03399
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/09/2020
ms.locfileid: "11105745"
---
# <span data-ttu-id="6bf1e-103">Microsoft Edge WebView2 - 原則</span><span class="sxs-lookup"><span data-stu-id="6bf1e-103">Microsoft Edge WebView2 - Policies</span></span>

<span data-ttu-id="6bf1e-104">最新版本的 Microsoft Edge WebView2 包含下列原則。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-104">The latest version of Microsoft Edge WebView2 includes the following policies.</span></span> <span data-ttu-id="6bf1e-105">您可以使用這些原則來設定 Microsoft Edge WebView2 在組織中的執行方式。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-105">You can use these policies to configure how Microsoft Edge WebView2 runs in your organization.</span></span>

<span data-ttu-id="6bf1e-106">如需用於控制 Microsoft Edge WebView2 更新方式和更新時機的一組額外原則之詳細資訊，請參閱 [Microsoft Edge 更新原則參考](microsoft-edge-update-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-106">For information about an additional set of policies used to control how and when Microsoft Edge WebView2 is updated, check out [Microsoft Edge update policy reference](microsoft-edge-update-policies.md).</span></span>

> [!NOTE]
> <span data-ttu-id="6bf1e-107">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-107">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="6bf1e-108">可用原則</span><span class="sxs-lookup"><span data-stu-id="6bf1e-108">Available policies</span></span>
<span data-ttu-id="6bf1e-109">下表列出此版本 Microsoft Edge WebView2 提供的所有群組原則。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-109">These tables list all of the group policies available in this release of Microsoft Edge WebView2.</span></span> <span data-ttu-id="6bf1e-110">使用下表中的連結，深入了解特定原則。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-110">Use the links in the table to get more details about specific policies.</span></span>

|||
|-|-|
|[<span data-ttu-id="6bf1e-111">載入程式重寫設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-111">Loader Override Settings</span></span>](#loader-override-settings)|

### [*<span data-ttu-id="6bf1e-112">載入程式重寫設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-112">Loader Override Settings</span></span>*](#loader-override-settings-policies)
|<span data-ttu-id="6bf1e-113">原則名稱</span><span class="sxs-lookup"><span data-stu-id="6bf1e-113">Policy Name</span></span>|<span data-ttu-id="6bf1e-114">標題</span><span class="sxs-lookup"><span data-stu-id="6bf1e-114">Caption</span></span>|
|-|-|
|[<span data-ttu-id="6bf1e-115">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6bf1e-115">browserExecutableFolder</span></span>](#browserexecutablefolder)|<span data-ttu-id="6bf1e-116">設定 [瀏覽器可執行檔] 資料夾的位置</span><span class="sxs-lookup"><span data-stu-id="6bf1e-116">Configure the location of the browser executable folder</span></span>|
|[<span data-ttu-id="6bf1e-117">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6bf1e-117">releaseChannelPreference</span></span>](#releasechannelpreference)|<span data-ttu-id="6bf1e-118">設定發行通道的 [搜尋順序] 喜好設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-118">Set the release channel search order preference</span></span>|




  ## <span data-ttu-id="6bf1e-119">載入程式重寫設定原則</span><span class="sxs-lookup"><span data-stu-id="6bf1e-119">Loader Override Settings policies</span></span>

  [<span data-ttu-id="6bf1e-120">回到頁首</span><span class="sxs-lookup"><span data-stu-id="6bf1e-120">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="6bf1e-121">browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6bf1e-121">browserExecutableFolder</span></span>
  #### <span data-ttu-id="6bf1e-122">設定 [瀏覽器可執行檔] 資料夾的位置</span><span class="sxs-lookup"><span data-stu-id="6bf1e-122">Configure the location of the browser executable folder</span></span>
  
  
  #### <span data-ttu-id="6bf1e-123">支援的版本：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-123">Supported versions:</span></span>
  - <span data-ttu-id="6bf1e-124">Windows 上，版本 87 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6bf1e-124">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="6bf1e-125">描述</span><span class="sxs-lookup"><span data-stu-id="6bf1e-125">Description</span></span>
  <span data-ttu-id="6bf1e-126">這項原則會在指定路徑中，將 WebView2 應用程式設定為使用 WebView2 Runtime。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-126">This policy configures WebView2 applications to use the WebView2 Runtime in the specified path.</span></span> <span data-ttu-id="6bf1e-127">該資料夾應包含下列檔案：msedgewebview2.exe、msedge.dll 等等。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-127">The folder should contain the following files: msedgewebview2.exe, msedge.dll, and so on.</span></span>

<span data-ttu-id="6bf1e-128">若要設定資料夾路徑的值，請提供值名稱和值配對。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-128">To set the value for the folder path, provide a Value name and Value pair.</span></span> <span data-ttu-id="6bf1e-129">將 [值名稱] 設定為 [應用程式使用者模型識別碼] 或 [可執行檔名]。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-129">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="6bf1e-130">您可以使用萬用字元「\*」作為值名稱來套用到所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-130">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="6bf1e-131">支援的功能：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-131">Supported features:</span></span>
  - <span data-ttu-id="6bf1e-132">可強制執行：是</span><span class="sxs-lookup"><span data-stu-id="6bf1e-132">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="6bf1e-133">可以建議：否</span><span class="sxs-lookup"><span data-stu-id="6bf1e-133">Can be recommended: No</span></span>
  - <span data-ttu-id="6bf1e-134">動態原則重新整理：是</span><span class="sxs-lookup"><span data-stu-id="6bf1e-134">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="6bf1e-135">Data Type:</span><span class="sxs-lookup"><span data-stu-id="6bf1e-135">Data Type:</span></span>
  - <span data-ttu-id="6bf1e-136">字串清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-136">List of strings</span></span>

  #### <span data-ttu-id="6bf1e-137">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-137">Windows information and settings</span></span>
  ##### <span data-ttu-id="6bf1e-138">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="6bf1e-138">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="6bf1e-139">GP 唯一名稱：browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6bf1e-139">GP unique name: browserExecutableFolder</span></span>
  - <span data-ttu-id="6bf1e-140">GP 名稱：設定 [瀏覽器可執行檔] 資料夾的位置</span><span class="sxs-lookup"><span data-stu-id="6bf1e-140">GP name: Configure the location of the browser executable folder</span></span>
  - <span data-ttu-id="6bf1e-141">GP 路徑 (強制)：系統管理範本/Microsoft Edge WebView2/載入程式重寫設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-141">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="6bf1e-142">GP 路徑 (建議)：不適用</span><span class="sxs-lookup"><span data-stu-id="6bf1e-142">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="6bf1e-143">GP ADMX 檔案名稱：MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="6bf1e-143">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="6bf1e-144">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-144">Windows Registry Settings</span></span>
  - <span data-ttu-id="6bf1e-145">路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span><span class="sxs-lookup"><span data-stu-id="6bf1e-145">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder</span></span>
  - <span data-ttu-id="6bf1e-146">路徑 (建議)：不適用</span><span class="sxs-lookup"><span data-stu-id="6bf1e-146">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="6bf1e-147">值名稱：REG_SZ 的清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-147">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="6bf1e-148">數值類型：REG_SZ 的清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-148">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="6bf1e-149">範例值：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-149">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\browserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```


  

  [<span data-ttu-id="6bf1e-150">回到頁首</span><span class="sxs-lookup"><span data-stu-id="6bf1e-150">Back to top</span></span>](#microsoft-edge-webview2---policies)

  ### <span data-ttu-id="6bf1e-151">releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6bf1e-151">releaseChannelPreference</span></span>
  #### <span data-ttu-id="6bf1e-152">設定發行通道的 [搜尋順序] 喜好設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-152">Set the release channel search order preference</span></span>
  
  
  #### <span data-ttu-id="6bf1e-153">支援的版本：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-153">Supported versions:</span></span>
  - <span data-ttu-id="6bf1e-154">Windows 上，版本 87 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6bf1e-154">On Windows since 87 or later</span></span>

  #### <span data-ttu-id="6bf1e-155">描述</span><span class="sxs-lookup"><span data-stu-id="6bf1e-155">Description</span></span>
  <span data-ttu-id="6bf1e-156">預設通道搜尋順序為 WebView2 Runtime、Beta、Dev 和 Canary。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-156">The default channel search order is WebView2 Runtime, Beta, Dev, and Canary.</span></span>

<span data-ttu-id="6bf1e-157">若要顛倒預設的搜尋順序，請將此原則設定為 1。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-157">To reverse the default search order, set this policy to 1.</span></span>

<span data-ttu-id="6bf1e-158">若要設定發行通道喜好設定的值，請提供值名稱和值配對。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-158">To set the value for the release channel preference, provide a Value name and Value pair.</span></span> <span data-ttu-id="6bf1e-159">將 [值名稱] 設定為 [應用程式使用者模型識別碼] 或 [可執行檔名]。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-159">Set value name to the Application User Model ID or the executable file name.</span></span> <span data-ttu-id="6bf1e-160">您可以使用萬用字元「\*」作為值名稱來套用到所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="6bf1e-160">You can use the "\*" wildcard as value name to apply to all applications.</span></span>

  #### <span data-ttu-id="6bf1e-161">支援的功能：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-161">Supported features:</span></span>
  - <span data-ttu-id="6bf1e-162">可強制執行：是</span><span class="sxs-lookup"><span data-stu-id="6bf1e-162">Can be mandatory: Yes</span></span>
  - <span data-ttu-id="6bf1e-163">可以建議：否</span><span class="sxs-lookup"><span data-stu-id="6bf1e-163">Can be recommended: No</span></span>
  - <span data-ttu-id="6bf1e-164">動態原則重新整理：是</span><span class="sxs-lookup"><span data-stu-id="6bf1e-164">Dynamic Policy Refresh: Yes</span></span>

  #### <span data-ttu-id="6bf1e-165">Data Type:</span><span class="sxs-lookup"><span data-stu-id="6bf1e-165">Data Type:</span></span>
  - <span data-ttu-id="6bf1e-166">字串清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-166">List of strings</span></span>

  #### <span data-ttu-id="6bf1e-167">Windows 資訊和設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-167">Windows information and settings</span></span>
  ##### <span data-ttu-id="6bf1e-168">群組原則 (ADMX) 資訊</span><span class="sxs-lookup"><span data-stu-id="6bf1e-168">Group Policy (ADMX) info</span></span>
  - <span data-ttu-id="6bf1e-169">GP 唯一名稱：releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6bf1e-169">GP unique name: releaseChannelPreference</span></span>
  - <span data-ttu-id="6bf1e-170">GP 名稱：設定發行通道的 [搜尋順序] 喜好設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-170">GP name: Set the release channel search order preference</span></span>
  - <span data-ttu-id="6bf1e-171">GP 路徑 (強制)：系統管理範本/Microsoft Edge WebView2/載入程式重寫設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-171">GP path (Mandatory): Administrative Templates/Microsoft Edge WebView2/Loader Override Settings</span></span>
  - <span data-ttu-id="6bf1e-172">GP 路徑 (建議)：不適用</span><span class="sxs-lookup"><span data-stu-id="6bf1e-172">GP path (Recommended): N/A</span></span>
  - <span data-ttu-id="6bf1e-173">GP ADMX 檔案名稱：MSEdgeWebView2.admx</span><span class="sxs-lookup"><span data-stu-id="6bf1e-173">GP ADMX file name: MSEdgeWebView2.admx</span></span>
  ##### <span data-ttu-id="6bf1e-174">Windows 登錄設定</span><span class="sxs-lookup"><span data-stu-id="6bf1e-174">Windows Registry Settings</span></span>
  - <span data-ttu-id="6bf1e-175">路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span><span class="sxs-lookup"><span data-stu-id="6bf1e-175">Path (Mandatory): SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference</span></span>
  - <span data-ttu-id="6bf1e-176">路徑 (建議)：不適用</span><span class="sxs-lookup"><span data-stu-id="6bf1e-176">Path (Recommended): N/A</span></span>
  - <span data-ttu-id="6bf1e-177">值名稱：REG_SZ 的清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-177">Value Name: list of REG_SZ</span></span>
  - <span data-ttu-id="6bf1e-178">數值類型：REG_SZ 的清單</span><span class="sxs-lookup"><span data-stu-id="6bf1e-178">Value Type: list of REG_SZ</span></span>
  ##### <span data-ttu-id="6bf1e-179">範例值：</span><span class="sxs-lookup"><span data-stu-id="6bf1e-179">Example value:</span></span>
```
SOFTWARE\Policies\Microsoft\Edge\WebView2\releaseChannelPreference = "Name: *, Value: 1"

```


  

  [<span data-ttu-id="6bf1e-180">回到頁首</span><span class="sxs-lookup"><span data-stu-id="6bf1e-180">Back to top</span></span>](#microsoft-edge-webview2---policies)


## <span data-ttu-id="6bf1e-181">請參閱</span><span class="sxs-lookup"><span data-stu-id="6bf1e-181">See also</span></span>
- [<span data-ttu-id="6bf1e-182">設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6bf1e-182">Configuring Microsoft Edge</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="6bf1e-183">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="6bf1e-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6bf1e-184">Microsoft 安全性基準部落格</span><span class="sxs-lookup"><span data-stu-id="6bf1e-184">Microsoft Security Baselines Blog</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)