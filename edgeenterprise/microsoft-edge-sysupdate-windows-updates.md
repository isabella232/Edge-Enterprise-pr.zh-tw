---
title: Microsoft Edge 的 Windows Update
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 的 Windows Update
ms.openlocfilehash: 880e5a591ee23ff852981e73fe4fc4cd815be9ad
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447147"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a><span data-ttu-id="b6d10-103">支援下一版 Microsoft Edge 的 Windows Update</span><span class="sxs-lookup"><span data-stu-id="b6d10-103">Windows updates to support the next version of Microsoft Edge</span></span>

<span data-ttu-id="b6d10-104">本文介紹 Windows 如何更新為支援下一版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b6d10-104">This article describes how Windows will be updated to support the next version of Microsoft Edge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6d10-105">請參閱 Microsoft Edge 產品小組的[部落格文章](https://aka.ms/EdgeLegacyEOS)，以了解舊版 Microsoft Edge 終止服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b6d10-105">Refer to the Microsoft Edge product team [blog post](https://aka.ms/EdgeLegacyEOS) about Microsoft Edge Legacy end of service.</span></span>

> [!NOTE]
> <span data-ttu-id="b6d10-106">本文適用於 Microsoft Edge 穩定通道。</span><span class="sxs-lookup"><span data-stu-id="b6d10-106">This article applies to the Microsoft Edge Stable channel.</span></span>

## <a name="microsoft-edge-and-the-windows-release-cycle"></a><span data-ttu-id="b6d10-107">Microsoft Edge 和 Windows 發行週期</span><span class="sxs-lookup"><span data-stu-id="b6d10-107">Microsoft Edge and the Windows release cycle</span></span>

<span data-ttu-id="b6d10-108">下一版 Microsoft Edge 具有更頻繁且更靈活的更新功能。</span><span class="sxs-lookup"><span data-stu-id="b6d10-108">The next version of Microsoft Edge features more frequent and more flexible updating capabilities.</span></span> <span data-ttu-id="b6d10-109">由於瀏覽器版本未繫結到 Windows 主要版本，因此將對作業系統進行變更，以確保下一版 Microsoft Edge 可無縫地適合 Windows。</span><span class="sxs-lookup"><span data-stu-id="b6d10-109">Because browser releases aren't bound to the Windows major releases, changes will be made to the operating system to ensure that the next version of Microsoft Edge fits seamlessly into Windows.</span></span> <span data-ttu-id="b6d10-110">如此一來，功能更新將會以約 6 週的週期釋出。</span><span class="sxs-lookup"><span data-stu-id="b6d10-110">As a result, feature updates will be released on a 6-week cycle (approximately).</span></span> <span data-ttu-id="b6d10-111">安全性與相容性更新將在必要時提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-111">Security and compatibility updates will be shipped as needed.</span></span>

## <a name="updates-and-the-user-experience"></a><span data-ttu-id="b6d10-112">更新和使用者體驗</span><span class="sxs-lookup"><span data-stu-id="b6d10-112">Updates and the user experience</span></span>

<span data-ttu-id="b6d10-113">在安裝下一版 Microsoft Edge 的 Stable 通道之前，更新不會變更使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="b6d10-113">Updates won’t change the user experience until the Stable channel of the next version of Microsoft Edge is installed.</span></span> <span data-ttu-id="b6d10-114">安裝 Microsoft Edge Beta、Dev 或 Canary 不會觸發 Windows 中的任何變更。</span><span class="sxs-lookup"><span data-stu-id="b6d10-114">Installing Microsoft Edge Beta, Dev, or Canary won’t trigger any changes in Windows.</span></span> <span data-ttu-id="b6d10-115">這些瀏覽器版本將與現有瀏覽器一起安裝。</span><span class="sxs-lookup"><span data-stu-id="b6d10-115">These browser releases will be installed alongside existing browsers.</span></span>

<span data-ttu-id="b6d10-116">套用所有更新「並」在系統層級安裝下一版 Microsoft Edge 的 Stable 通道時，以下變更將在系統上生效：</span><span class="sxs-lookup"><span data-stu-id="b6d10-116">When all the updates are applied AND the Stable channel of the next version of Microsoft Edge is installed at the system-level, the following changes will take effect on the system:</span></span>

- <span data-ttu-id="b6d10-117">目前 Microsoft Edge 版本的所有開始功能表釘選項目、磚和捷徑都將移移至下一版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b6d10-117">All start menu pins, tiles, and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="b6d10-118">目前 Microsoft Edge 版本的所有工作列釘選項目和捷徑都將移移至下一版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b6d10-118">All taskbar pins and shortcuts for the current version of Microsoft Edge will migrate to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="b6d10-119">下一版 Microsoft Edge 將釘選到工作列。</span><span class="sxs-lookup"><span data-stu-id="b6d10-119">The next version of Microsoft Edge will be pinned to the taskbar.</span></span> <span data-ttu-id="b6d10-120">如果目前版本的 Microsoft Edge 已釘選，則將替換它。</span><span class="sxs-lookup"><span data-stu-id="b6d10-120">If the current version of Microsoft Edge is already pinned, it will be replaced.</span></span>
- <span data-ttu-id="b6d10-121">下一版 Microsoft Edge 將新增捷徑到桌面。</span><span class="sxs-lookup"><span data-stu-id="b6d10-121">The next version of Microsoft Edge will add a shortcut to the desktop.</span></span> <span data-ttu-id="b6d10-122">如果目前版本的 Microsoft Edge 已有捷徑，則將替換它。</span><span class="sxs-lookup"><span data-stu-id="b6d10-122">If the current version of Microsoft Edge already has a shortcut, it will be replaced.</span></span>
- <span data-ttu-id="b6d10-123">預設情況下，Microsoft Edge 控制代碼的大多數通訊協定將移移至下一版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b6d10-123">Most protocols that Microsoft Edge handles by default will be migrated to the next version of Microsoft Edge.</span></span>
- <span data-ttu-id="b6d10-124">目前 Microsoft Edge 將從作業系統中的所有 UX 介面隱藏，包括設定、所有應用程式以及任何檔案或通訊協定支援對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b6d10-124">Current Microsoft Edge will be hidden from all UX surfaces in the OS, including settings, all apps, and any file or protocol support dialogs.</span></span>
- <span data-ttu-id="b6d10-125">所有對目前版本 Microsoft Edge 的嘗試啟動都將重新導向至下一版 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b6d10-125">All attempts to launch the current version of Microsoft Edge will redirect to the next version of Microsoft Edge.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b6d10-126">使用者層級安裝不會觸發這些行為。</span><span class="sxs-lookup"><span data-stu-id="b6d10-126">User-level installs won’t trigger these behaviors.</span></span>

<span data-ttu-id="b6d10-127">隨著先前的變更，無論是否安裝了下一版 Microsoft Edge 的 Stable 通道，都會發生這些變更。</span><span class="sxs-lookup"><span data-stu-id="b6d10-127">Along with the previous changes, there are changes that will happen regardless of whether the Stable channel of the next version of Microsoft Edge is installed.</span></span>

- <span data-ttu-id="b6d10-128">Microsoft Edge 將解除登錄下一版 Microsoft Edge 不支援的書籍和 XML 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b6d10-128">Microsoft Edge will de-register for the books and XML protocols that the next version of Microsoft Edge doesn't support.</span></span> <span data-ttu-id="b6d10-129">嘗試開啟這些通訊協定的使用者會看到一個對話方塊，提示他們選擇預設應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6d10-129">Users attempting to open these protocols will get a dialog that prompts them to choose a default app.</span></span> <span data-ttu-id="b6d10-130">請至[下載 ePub 應用程式以繼續閱讀電子書](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0)深入了解有關圖書支援變更。</span><span class="sxs-lookup"><span data-stu-id="b6d10-130">Learn more about changes to books support at [Download an ePub app to keep reading e-books](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0).</span></span>

## <a name="timeline"></a><span data-ttu-id="b6d10-131">時間表</span><span class="sxs-lookup"><span data-stu-id="b6d10-131">Timeline</span></span>

<span data-ttu-id="b6d10-132">支援所述體驗所需的變更將隨不同版本 Windows 的三個更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-132">The changes needed to support the described experience will be delivered with three updates for different versions of Windows.</span></span>

### <a name="windows-versions-1903-and-1909"></a><span data-ttu-id="b6d10-133">Windows 版本 1903 與 1909</span><span class="sxs-lookup"><span data-stu-id="b6d10-133">Windows versions 1903 and 1909</span></span>

- <span data-ttu-id="b6d10-134">選用 2019 年 7 月更新中的第一組變更，隨 2019 年 8 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-134">First set of changes in optional July 2019 update, delivered with the August 2019 security update.</span></span>
- <span data-ttu-id="b6d10-135">選用 2019 年 8 月更新中的第二組變更，隨 2019 年 9 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-135">Second set of changes in the optional August 2019 update, delivered with the September 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b6d10-136">這是 Microsoft Edge 將解除登錄 XML 通訊協定的更新。</span><span class="sxs-lookup"><span data-stu-id="b6d10-136">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="b6d10-137">選用 2019 年 9 月更新中的第三組變更，隨 2019 年 10 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-137">Third set of changes in the optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b6d10-138">這是 Microsoft Edge 不再支援電子書的更新。</span><span class="sxs-lookup"><span data-stu-id="b6d10-138">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

### <a name="windows-versions-1709-1803-and-1809"></a><span data-ttu-id="b6d10-139">Windows 版本 1709、1803 與 1809</span><span class="sxs-lookup"><span data-stu-id="b6d10-139">Windows versions 1709, 1803, and 1809</span></span>

- <span data-ttu-id="b6d10-140">選用 2019 年 8 月更新中的第一組變更，隨 2019 年 9 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-140">First set of changes in an optional August 2019 update, delivered with the September 2019 security update.</span></span>
- <span data-ttu-id="b6d10-141">選用 2019 年 9 月更新中的第二組變更，隨 2019 年 10 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-141">Second set of changes in an optional September 2019 update, delivered with the October 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b6d10-142">這是 Microsoft Edge 將解除登錄 XML 通訊協定的更新。</span><span class="sxs-lookup"><span data-stu-id="b6d10-142">This is the update where Microsoft Edge will de-register for the XML protocol.</span></span>

- <span data-ttu-id="b6d10-143">選用 2019 年 10 月更新中的第三組變更，隨 2019 年 11 月安全性更新一起提供。</span><span class="sxs-lookup"><span data-stu-id="b6d10-143">Third set of changes in an optional October 2019 update, delivered with the November 2019 security update.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b6d10-144">這是 Microsoft Edge 不再支援電子書的更新。</span><span class="sxs-lookup"><span data-stu-id="b6d10-144">This is the update where Microsoft Edge will no longer support eBooks.</span></span>

<span data-ttu-id="b6d10-145">下表提供每組變更中特定更新的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b6d10-145">The following table gives the details for specific updates in each set of changes.</span></span>

| <span data-ttu-id="b6d10-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6d10-146">Windows 10</span></span> | <span data-ttu-id="b6d10-147">其他資訊</span><span class="sxs-lookup"><span data-stu-id="b6d10-147">More Information</span></span> | <span data-ttu-id="b6d10-148">必要下載</span><span class="sxs-lookup"><span data-stu-id="b6d10-148">Required Download</span></span> |
|--|--|--|
| <span data-ttu-id="b6d10-149">版本 1709</span><span class="sxs-lookup"><span data-stu-id="b6d10-149">Version 1709</span></span> | [<span data-ttu-id="b6d10-150">KB4525241</span><span class="sxs-lookup"><span data-stu-id="b6d10-150">KB4525241</span></span>](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [<span data-ttu-id="b6d10-151">Windows 10 版本 1709 的累積更新</span><span class="sxs-lookup"><span data-stu-id="b6d10-151">Cumulative Update for Windows 10 Version 1709</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| <span data-ttu-id="b6d10-152">版本 1803</span><span class="sxs-lookup"><span data-stu-id="b6d10-152">Version 1803</span></span>  | [<span data-ttu-id="b6d10-153">KB4525237</span><span class="sxs-lookup"><span data-stu-id="b6d10-153">KB4525237</span></span>](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [<span data-ttu-id="b6d10-154">Windows 10 版本 1803 的累積更新</span><span class="sxs-lookup"><span data-stu-id="b6d10-154">Cumulative Update for Windows 10 Version 1803</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| <span data-ttu-id="b6d10-155">版本 1809</span><span class="sxs-lookup"><span data-stu-id="b6d10-155">Version 1809</span></span>  | [<span data-ttu-id="b6d10-156">KB4523205</span><span class="sxs-lookup"><span data-stu-id="b6d10-156">KB4523205</span></span>](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [<span data-ttu-id="b6d10-157">Windows 10 版本 1809 的累積更新</span><span class="sxs-lookup"><span data-stu-id="b6d10-157">Cumulative Update for Windows 10 Version 1809</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| <span data-ttu-id="b6d10-158">版本 1903 及 1909</span><span class="sxs-lookup"><span data-stu-id="b6d10-158">Version 1903 and 1909</span></span> |[<span data-ttu-id="b6d10-159">KB4517389</span><span class="sxs-lookup"><span data-stu-id="b6d10-159">KB4517389</span></span>](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [<span data-ttu-id="b6d10-160">Windows 10 版本 1903 和 1909 的累積更新</span><span class="sxs-lookup"><span data-stu-id="b6d10-160">Cumulative Update for Windows 10 Version 1903 and 1909</span></span>](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <a name="see-also"></a><span data-ttu-id="b6d10-161">也請參閱</span><span class="sxs-lookup"><span data-stu-id="b6d10-161">See also</span></span>

- [<span data-ttu-id="b6d10-162">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="b6d10-162">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="b6d10-163">Microsoft Edge 文件</span><span class="sxs-lookup"><span data-stu-id="b6d10-163">Microsoft Edge documentation</span></span>](./index.yml)