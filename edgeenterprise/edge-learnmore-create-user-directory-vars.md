---
title: 建立 Microsoft Edge 使用者資料目錄變數
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何建立 Microsoft Edge 使用者資料目錄變數
ms.openlocfilehash: 284bef9156dc3dff1413f349eebe4e7dac854a98
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979577"
---
# <span data-ttu-id="436e7-103">建立 Microsoft Edge 使用者資料目錄變數</span><span class="sxs-lookup"><span data-stu-id="436e7-103">Create Microsoft Edge user data directory variables</span></span>

<span data-ttu-id="436e7-104">本文介紹在修改 Microsoft Edge 時如何使用資料目錄變數，而不是使用硬式編碼路徑。</span><span class="sxs-lookup"><span data-stu-id="436e7-104">This article explains how you can use data directory variables instead of using hard-coded paths when modifying Microsoft Edge.</span></span>

>[!NOTE]
><span data-ttu-id="436e7-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="436e7-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="436e7-106">路徑變數</span><span class="sxs-lookup"><span data-stu-id="436e7-106">Path variables</span></span>

<span data-ttu-id="436e7-107">用於修改資料目錄路徑的原則 (例如，設定 [UserDataDir](microsoft-edge-policies.md#userdatadir) 或 [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory) 支援變數)。</span><span class="sxs-lookup"><span data-stu-id="436e7-107">Policies for modifying data directory paths (For example, configuring the [UserDataDir](microsoft-edge-policies.md#userdatadir) or [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory) support variables.</span></span> <span data-ttu-id="436e7-108">設定這些原則時，可以使用變數來取代硬式編碼路徑。</span><span class="sxs-lookup"><span data-stu-id="436e7-108">When configuring these policies, you can use variables instead of hard-coded paths.</span></span> <span data-ttu-id="436e7-109">例如，將您的設定檔資料儲存在 Windows 的使用者本機應用程式資料下，而不是預設位置。</span><span class="sxs-lookup"><span data-stu-id="436e7-109">For example, to store your profile data under user local application data on Windows instead of the default location.</span></span> <span data-ttu-id="436e7-110">將 [UserDataDir](microsoft-edge-policies.md#userdatadir) 原則設定為 **${local_app_data}\Edge\Profile**。</span><span class="sxs-lookup"><span data-stu-id="436e7-110">Set the [UserDataDir](microsoft-edge-policies.md#userdatadir) policy to **${local_app_data}\Edge\Profile**.</span></span> <span data-ttu-id="436e7-111">在大多數 Windows 10 安裝中，此路徑解析為 *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*。</span><span class="sxs-lookup"><span data-stu-id="436e7-111">On most Windows 10 installations, this path resolves to *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*.</span></span>

>[!NOTE]
><span data-ttu-id="436e7-112">如果未設定，Microsoft Edge 使用預設目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="436e7-112">If left unset, Microsoft Edge uses default directory paths.</span></span> <span data-ttu-id="436e7-113">使用者可以使用 `--user-data-dir` 命令列旗標來覆寫預設值。</span><span class="sxs-lookup"><span data-stu-id="436e7-113">A user can use the `--user-data-dir` command-line flag to override the default.</span></span>

<span data-ttu-id="436e7-114">若要查看目前**設定檔路徑**，請開啟**關於版本**頁面 (鍵入 "edge://version")。</span><span class="sxs-lookup"><span data-stu-id="436e7-114">To view the current  **Profile path**, open the **About version** page (type "edge://version").</span></span> <span data-ttu-id="436e7-115">**設定檔路徑**遵循以下格式：*C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*。</span><span class="sxs-lookup"><span data-stu-id="436e7-115">The **Profile path** follows this format: *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*.</span></span>

### <span data-ttu-id="436e7-116">使用路徑變數的指南</span><span class="sxs-lookup"><span data-stu-id="436e7-116">Guidance for using path variables</span></span>

<span data-ttu-id="436e7-117">在使用路徑變數之前，請先查看以下指南。</span><span class="sxs-lookup"><span data-stu-id="436e7-117">Review the following guidance before using variables for paths.</span></span>

- <span data-ttu-id="436e7-118">涉及 Microsoft Edge 儲存不同資料之路徑的所有原則，都與平台相關。</span><span class="sxs-lookup"><span data-stu-id="436e7-118">All policies that involve paths where Microsoft Edge stores different data are platform dependent.</span></span> <span data-ttu-id="436e7-119">某些原則僅可用於特定平台，而其他原則可在所有平台上使用。</span><span class="sxs-lookup"><span data-stu-id="436e7-119">Some of these policies are available only on specific platforms, but others can be used on all platforms.</span></span>
- <span data-ttu-id="436e7-120">為了避免應用程式在不同場合從不同位置啟動而導致錯誤，請確保路徑是絕對的。</span><span class="sxs-lookup"><span data-stu-id="436e7-120">To avoid errors caused by applications starting from different locations on different occasions, make sure that paths are absolute.</span></span>
- <span data-ttu-id="436e7-121">每個變數只能在路徑中出現一次。</span><span class="sxs-lookup"><span data-stu-id="436e7-121">Every variable can occur only once in a path.</span></span> <span data-ttu-id="436e7-122">對於大多數變數來說，這是使用變數的唯一有意義方法，因為它們解析為絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="436e7-122">For most of them, this is the only meaningful way to use variables, because they resolve to absolute paths.</span></span>
- <span data-ttu-id="436e7-123">如果路徑不存在，幾乎所有原則都會建立該路徑 (在現有情況下如果可能)。</span><span class="sxs-lookup"><span data-stu-id="436e7-123">Almost all policies will create the path if it doesn't exist (if possible in the existing circumstances).</span></span>
- <span data-ttu-id="436e7-124">由於 Microsoft Edge 不同版本/通道處理資料夾結構的方式不同，因此在某些原則中使用網路位置可能會導致意外的結果。</span><span class="sxs-lookup"><span data-stu-id="436e7-124">Using network locations for some policies can lead to unexpected results due to differences in how different versions/channels of Microsoft Edge handle the folder structure.</span></span>

### <span data-ttu-id="436e7-125">支援的路徑變數</span><span class="sxs-lookup"><span data-stu-id="436e7-125">Supported path variables</span></span>

<span data-ttu-id="436e7-126">Microsoft Edge 支援以下路徑變數。</span><span class="sxs-lookup"><span data-stu-id="436e7-126">Microsoft Edge supports the following path variables.</span></span>

#### <span data-ttu-id="436e7-127">所有平台</span><span class="sxs-lookup"><span data-stu-id="436e7-127">All platforms</span></span>

| <span data-ttu-id="436e7-128">變數</span><span class="sxs-lookup"><span data-stu-id="436e7-128">Variable</span></span> | <span data-ttu-id="436e7-129">描述</span><span class="sxs-lookup"><span data-stu-id="436e7-129">Description</span></span> |
| --- | --- |
| **<span data-ttu-id="436e7-130">${user_name}</span><span class="sxs-lookup"><span data-stu-id="436e7-130">${user_name}</span></span>** | <span data-ttu-id="436e7-131">正在使用 Microsoft Edge 的使用者。</span><span class="sxs-lookup"><span data-stu-id="436e7-131">The user who's using Microsoft Edge.</span></span> <span data-ttu-id="436e7-132">Microsoft Edge 遵循 SUID (設定執行時的擁有者使用者 ID) 範例：*audreysmall*</span><span class="sxs-lookup"><span data-stu-id="436e7-132">Microsoft Edge respects SUIDs (Set owner User ID up on execution) Example: *audreysmall*</span></span> |
| **<span data-ttu-id="436e7-133">${machine_name}</span><span class="sxs-lookup"><span data-stu-id="436e7-133">${machine_name}</span></span>** | <span data-ttu-id="436e7-134">電腦名稱稱，可能包括網域名稱。</span><span class="sxs-lookup"><span data-stu-id="436e7-134">The machine name, possibly including the domain name.</span></span> <span data-ttu-id="436e7-135">範例：*audreysmall* or *audrey.ex.contoso.com*</span><span class="sxs-lookup"><span data-stu-id="436e7-135">Example: *audreysmall* or *audrey.ex.contoso.com*</span></span> |

#### <span data-ttu-id="436e7-136">僅限 Windows</span><span class="sxs-lookup"><span data-stu-id="436e7-136">Windows only</span></span>

| <span data-ttu-id="436e7-137">變數</span><span class="sxs-lookup"><span data-stu-id="436e7-137">Variable</span></span> | <span data-ttu-id="436e7-138">描述</span><span class="sxs-lookup"><span data-stu-id="436e7-138">Description</span></span> |
| --- | --- |
| **<span data-ttu-id="436e7-139">${documents}</span><span class="sxs-lookup"><span data-stu-id="436e7-139">${documents}</span></span>** | <span data-ttu-id="436e7-140">目前使用者的文件資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-140">The Documents folder for the current user.</span></span> <span data-ttu-id="436e7-141">範例：*C:\Users\Administrator\Documents*</span><span class="sxs-lookup"><span data-stu-id="436e7-141">Example: *C:\Users\Administrator\Documents*</span></span> |
|**<span data-ttu-id="436e7-142">${local_app_data}</span><span class="sxs-lookup"><span data-stu-id="436e7-142">${local_app_data}</span></span>** | <span data-ttu-id="436e7-143">目前使用者的 [應用程式資料] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-143">The Application Data folder for the current user.</span></span> <span data-ttu-id="436e7-144">範例：*C:\Users\Administrator\AppData\Local*</span><span class="sxs-lookup"><span data-stu-id="436e7-144">Example: *C:\Users\Administrator\AppData\Local*</span></span> |
|**<span data-ttu-id="436e7-145">${roaming_app_data}</span><span class="sxs-lookup"><span data-stu-id="436e7-145">${roaming_app_data}</span></span>** | <span data-ttu-id="436e7-146">目前使用者的 [漫遊應用程式資料] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-146">The Roamed Application Data folder for the current user.</span></span> <span data-ttu-id="436e7-147">範例：*C:\Users\Administrator\AppData\Roaming*</span><span class="sxs-lookup"><span data-stu-id="436e7-147">Example: *C:\Users\Administrator\AppData\Roaming*</span></span> |
| **<span data-ttu-id="436e7-148">${profile}</span><span class="sxs-lookup"><span data-stu-id="436e7-148">${profile}</span></span>** | <span data-ttu-id="436e7-149">目前使用者的主資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-149">The home folder for the current user.</span></span> <span data-ttu-id="436e7-150">範例：*C:\Users\Administrator*</span><span class="sxs-lookup"><span data-stu-id="436e7-150">Example: *C:\Users\Administrator*</span></span> |
| **<span data-ttu-id="436e7-151">${global_app_data}</span><span class="sxs-lookup"><span data-stu-id="436e7-151">${global_app_data}</span></span>** | <span data-ttu-id="436e7-152">系統範圍的應用程式資料資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-152">The system-wide Application Data folder.</span></span> <span data-ttu-id="436e7-153">範例：*C:\AppData*</span><span class="sxs-lookup"><span data-stu-id="436e7-153">Example: *C:\AppData*</span></span> |
| **<span data-ttu-id="436e7-154">${program_files}</span><span class="sxs-lookup"><span data-stu-id="436e7-154">${program_files}</span></span>** | <span data-ttu-id="436e7-155">目前處理序的程式檔案資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-155">The Program Files folder for the current process.</span></span> <span data-ttu-id="436e7-156">此資料夾取決於它是 32 位元還是 64 位元處理序。</span><span class="sxs-lookup"><span data-stu-id="436e7-156">This  folder  depends on whether it's a 32-bit or 64-bit process.</span></span> <span data-ttu-id="436e7-157">範例解析：*C:\Program Files (x86)*</span><span class="sxs-lookup"><span data-stu-id="436e7-157">Example resolution: *C:\Program Files (x86)*</span></span> |
| **<span data-ttu-id="436e7-158">${windows}</span><span class="sxs-lookup"><span data-stu-id="436e7-158">${windows}</span></span>** | <span data-ttu-id="436e7-159">Windows 資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-159">The Windows folder.</span></span> <span data-ttu-id="436e7-160">範例：*C:\Windows*</span><span class="sxs-lookup"><span data-stu-id="436e7-160">Example: *C:\Windows*</span></span> |
| **<span data-ttu-id="436e7-161">${client_name)</span><span class="sxs-lookup"><span data-stu-id="436e7-161">${client_name)</span></span>** | <span data-ttu-id="436e7-162">連接到 RDP 或 Citrix 工作階段的用戶端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="436e7-162">The name of the client PC connected to an RDP or Citrix session.</span></span> <span data-ttu-id="436e7-163">如果從本機工作階段使用，則此變數為空。</span><span class="sxs-lookup"><span data-stu-id="436e7-163">This variable is empty if it's used from a local session.</span></span> <span data-ttu-id="436e7-164">如果用於路徑中，請用保證不為空的項目來做為它的首碼。</span><span class="sxs-lookup"><span data-stu-id="436e7-164">If it's used in a path, prefix it with something that's guaranteed not to be empty.</span></span> <span data-ttu-id="436e7-165">範例：*C:\edge_profiles\session_${client_name}* 解析為 *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* 且 *C:\edge_profiles\session_&lt;SomePCname&gt;* 用於遠端工作階段。</span><span class="sxs-lookup"><span data-stu-id="436e7-165">Example: *C:\edge_profiles\session_${client_name}* resolves to *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* and *C:\edge_profiles\session_&lt;SomePCname&gt;* for remote sessions.</span></span> |
| **<span data-ttu-id="436e7-166">${session_name}</span><span class="sxs-lookup"><span data-stu-id="436e7-166">${session_name}</span></span>** | <span data-ttu-id="436e7-167">使用中工作階段的名稱。</span><span class="sxs-lookup"><span data-stu-id="436e7-167">The name of the active session.</span></span> <span data-ttu-id="436e7-168">使用此名稱可區分使用單一使用者設定檔的多個同時連接的遠端工作階段。</span><span class="sxs-lookup"><span data-stu-id="436e7-168">Use this name to distinguish multiple simultaneously connected remote sessions that are using a single user profile.</span></span> <span data-ttu-id="436e7-169">範例：*WinSta0 for local desktop sessions*</span><span class="sxs-lookup"><span data-stu-id="436e7-169">Example: *WinSta0 for local desktop sessions*</span></span> |

#### <span data-ttu-id="436e7-170">僅限 macOS</span><span class="sxs-lookup"><span data-stu-id="436e7-170">macOS only</span></span>

| <span data-ttu-id="436e7-171">變數</span><span class="sxs-lookup"><span data-stu-id="436e7-171">Variable</span></span> | <span data-ttu-id="436e7-172">描述</span><span class="sxs-lookup"><span data-stu-id="436e7-172">Description</span></span> |
| --- | --- |
| **<span data-ttu-id="436e7-173">${users}</span><span class="sxs-lookup"><span data-stu-id="436e7-173">${users}</span></span>** | <span data-ttu-id="436e7-174">儲存使用者設定檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-174">The folder where users' profiles are stored.</span></span> <span data-ttu-id="436e7-175">範例：*/Users*</span><span class="sxs-lookup"><span data-stu-id="436e7-175">Example: */Users*</span></span> |
| **<span data-ttu-id="436e7-176">${documents}</span><span class="sxs-lookup"><span data-stu-id="436e7-176">${documents}</span></span>** | <span data-ttu-id="436e7-177">目前使用者的文件資料夾。</span><span class="sxs-lookup"><span data-stu-id="436e7-177">The Documents folder for the current user.</span></span> <span data-ttu-id="436e7-178">範例：*/Users/audreysmall/Documents*</span><span class="sxs-lookup"><span data-stu-id="436e7-178">Example: */Users/audreysmall/Documents*</span></span> |

## <span data-ttu-id="436e7-179">內容授權</span><span class="sxs-lookup"><span data-stu-id="436e7-179">Content license</span></span>

>[!NOTE]
><span data-ttu-id="436e7-180">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="436e7-180">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms  described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="436e7-181">原始頁面可在[此處](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables)找到。</span><span class="sxs-lookup"><span data-stu-id="436e7-181">The original page can be found [here](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/><span data-ttu-id="436e7-182">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="436e7-182">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="436e7-183">請參閱</span><span class="sxs-lookup"><span data-stu-id="436e7-183">See also</span></span>

- [<span data-ttu-id="436e7-184">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="436e7-184">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)