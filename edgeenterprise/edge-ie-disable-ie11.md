---
title: 停用 Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 了解如何在 Microsoft Edge 中停用 Internet Explorer 11 和使用 Internet Explorer 模式。
ms.openlocfilehash: b70da0ff7437d1f5e70cec40e31211046a66205a
ms.sourcegitcommit: 2a00571483e1d169b2b3b59f4fce43262f460a9a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643748"
---
# <a name="disable-internet-explorer-11"></a><span data-ttu-id="dacec-103">停用 Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="dacec-103">Disable Internet Explorer 11</span></span>

>[!Note]
> <span data-ttu-id="dacec-104">Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。</span><span class="sxs-lookup"><span data-stu-id="dacec-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="dacec-105">您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="dacec-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="dacec-106">[從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。</span><span class="sxs-lookup"><span data-stu-id="dacec-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="dacec-107">本文說明如何在您的環境中停用 Internet Explorer 11 做為獨立瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="dacec-107">This article describes how to disable Internet Explorer 11 as a standalone browser in your environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dacec-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="dacec-108">Prerequisites</span></span>

<span data-ttu-id="dacec-109">需要下列 Windows 更新和 Microsoft Edge 軟體：</span><span class="sxs-lookup"><span data-stu-id="dacec-109">The following Windows updates and Microsoft Edge software are required:</span></span>

- <span data-ttu-id="dacec-110">Windows 更新</span><span class="sxs-lookup"><span data-stu-id="dacec-110">Windows updates</span></span>

  - <span data-ttu-id="dacec-111">Windows 10版本 21H1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="dacec-111">Windows 10, version 21H1 or later</span></span>
  - <span data-ttu-id="dacec-112">Windows 10版本 2004;Windows伺服器版本 2004;Windows 10版本 20H2;Windows伺服器版本[20H2：KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b)或更新版本</span><span class="sxs-lookup"><span data-stu-id="dacec-112">Windows 10, version 2004; Windows Server version 2004; Windows 10, version 20H2; Windows Server version 20H2: [KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) or later</span></span>
  - <span data-ttu-id="dacec-113">Windows 10版本[1909：KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511)或更新版本</span><span class="sxs-lookup"><span data-stu-id="dacec-113">Windows 10 version 1909: [KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) or later</span></span>
  - <span data-ttu-id="dacec-114">WindowsServer 2019;Windows 10 企業版 2019 [LTSC：KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d)或更新版</span><span class="sxs-lookup"><span data-stu-id="dacec-114">Windows Server 2019; Windows 10 Enterprise 2019 LTSC: [KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) or later</span></span>
  - <span data-ttu-id="dacec-115">Windows Server 2016;[Windows 10 企業版 2016 長期維護：KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e)或更新專案</span><span class="sxs-lookup"><span data-stu-id="dacec-115">Windows Server 2016; Windows 10 Enterprise 2016 LTSB: [KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) or later</span></span>
  - <span data-ttu-id="dacec-116">[Windows 10 企業版 2015 長期維護：KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US)或更新專案</span><span class="sxs-lookup"><span data-stu-id="dacec-116">Windows 10 Enterprise 2015 LTSB: [KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) or later</span></span>
  - <span data-ttu-id="dacec-117">Windows 8.1;Windows Server 2012[R2：KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96)或更新專案</span><span class="sxs-lookup"><span data-stu-id="dacec-117">Windows 8.1; Windows Server 2012 R2: [KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) or later</span></span>
  - <span data-ttu-id="dacec-118">Windows Server 2012：[KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) 或更新版本</span><span class="sxs-lookup"><span data-stu-id="dacec-118">Windows Server 2012: [KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) or later</span></span>
  
- <span data-ttu-id="dacec-119">Microsoft Edge 穩定通道</span><span class="sxs-lookup"><span data-stu-id="dacec-119">Microsoft Edge Stable Channel</span></span>


## <a name="overview"></a><span data-ttu-id="dacec-120">概觀</span><span class="sxs-lookup"><span data-stu-id="dacec-120">Overview</span></span>

<span data-ttu-id="dacec-121">針對需要 Internet Explorer 11 (IE11) 之舊版相容性的組織，Microsoft Edge 上的 Internet Explorer 模式 (IE 模式) 提供流暢的單一瀏覽器體驗。</span><span class="sxs-lookup"><span data-stu-id="dacec-121">For organizations that require Internet Explorer 11 (IE11) for legacy compatibility, Internet Explorer mode (IE mode) on Microsoft Edge provides a seamless, single browser experience.</span></span> <span data-ttu-id="dacec-122">使用者可以從 Microsoft Edge 存取舊版應用程式，而不需要切換回 IE11。</span><span class="sxs-lookup"><span data-stu-id="dacec-122">Users can access legacy applications from within Microsoft Edge without having to switch back to IE11.</span></span>

<span data-ttu-id="dacec-123">設定 IE 模式之後，您可以使用群組原則來停用 IE11 作為獨立瀏覽器，**而不會影響整個組織的 IE 模式功能**。</span><span class="sxs-lookup"><span data-stu-id="dacec-123">After you configure IE mode, you can disable IE11 as a standalone browser **without affecting IE mode functionality** across your organization using group policy.</span></span>

> [!NOTE]
> <span data-ttu-id="dacec-124">如果您需要適用於特定網站的獨立 IE11 應用程式，並想要將所有其他瀏覽器流量重新導向至 Microsoft Edge，您可以設定[將網站清單中未包含的所有網站傳送至 Microsoft Edge](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) 原則，將網站從 IE 重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="dacec-124">If you need the standalone IE11 app for specific sites, and want to redirect all other browser traffic to Microsoft Edge, you can configure the [Send all sites not included in the site list to Microsoft Edge](./edge-ie-mode-policies.md#redirect-sites-from-ie-to-microsoft-edge) policy to redirect sites from IE to Microsoft Edge.</span></span>

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a><span data-ttu-id="dacec-125">將流量重新導向至 Microsoft Edge 後的使用者體驗</span><span class="sxs-lookup"><span data-stu-id="dacec-125">User experience after redirecting traffic to Microsoft Edge</span></span>

<span data-ttu-id="dacec-126">當您啟用 [停用 Internet Explorer 11 做為獨立瀏覽器]\*\*\*\* 原則後，所有 IE11 活動會重新導向至 Microsoft Edge，且使用者會擁有下列體驗：</span><span class="sxs-lookup"><span data-stu-id="dacec-126">When you enable the **Disable Internet Explorer 11 as a standalone browser** policy, all IE11 activity is redirected to Microsoft Edge and users have the following experience:</span></span>

- <span data-ttu-id="dacec-127">系統將會移除 [開始] 功能表上的 IE11 圖示，但工作列上的圖示會保留。</span><span class="sxs-lookup"><span data-stu-id="dacec-127">The IE11 icon on the Start Menu will be removed, but the one on the taskbar will remain.</span></span>
- <span data-ttu-id="dacec-128">當使用者嘗試啟動使用 IE11 的捷徑或檔案關聯時，系統將會重新導向使用者以在 Microsoft Edge 中開啟相同的檔案/URL。</span><span class="sxs-lookup"><span data-stu-id="dacec-128">When users try to launch shortcuts or file associations that use IE11, they will be redirected to open the same file/URL in Microsoft Edge.</span></span>
- <span data-ttu-id="dacec-129">當使用者嘗試直接以 iexplore.exe 二進位檔啟動 IE11 時，會改為啟動 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="dacec-129">When users try to launch IE11 by directly invoking the iexplore.exe binary, Microsoft Edge will launch instead.</span></span>

<span data-ttu-id="dacec-130">在設定此體驗的原則時，您可以選擇為嘗試啟動 IE11 的每位使用者顯示重新導向訊息。</span><span class="sxs-lookup"><span data-stu-id="dacec-130">As part of setting the policy for this experience, you can optionally show a redirect message for each user who tries to launch IE11.</span></span> <span data-ttu-id="dacec-131">可將此訊息設定為 [永遠顯示] 或 [每位使用者顯示一次]。</span><span class="sxs-lookup"><span data-stu-id="dacec-131">This message can be set to display "Always" or "Once per user".</span></span> <span data-ttu-id="dacec-132">根據預設，永遠不會顯示下一個螢幕擷取畫面中顯示的重新導向訊息。</span><span class="sxs-lookup"><span data-stu-id="dacec-132">By default, the redirect message shown in the next screenshot is never shown.</span></span>

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="在 Microsoft Edge 重新導向作用中時，當您嘗試開啟 IE 時，系統會提醒您。":::

<span data-ttu-id="dacec-134">如果您的 [企業模式網站清單] 包含設定為在IE11 應用程式中開啟的應用程式，並且您使用此原則停用了 IE11，則它們將在 Microsoft Edge 上以 IE 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="dacec-134">If your Enterprise Mode Site List contains applications that are configured to open in the IE11 app and you disable IE11 with this policy, they will open in IE mode on Microsoft Edge.</span></span>
> [!NOTE]
> <span data-ttu-id="dacec-135">當網站設定為在 IE11 應用程式中開啟，且已設定停用 IE11 原則時，使用者流程會發生已知問題。</span><span class="sxs-lookup"><span data-stu-id="dacec-135">There was a known issue with the user flow when a site is configured to open in the IE11 application and the disable IE11 policy is set.</span></span> <span data-ttu-id="dacec-136">此問題已在 Microsoft Edge 版本 91.0.840.0 或更新版本中修正。</span><span class="sxs-lookup"><span data-stu-id="dacec-136">The issue has been fixed in Microsoft Edge versions 91.0.840.0 or later.</span></span>

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a><span data-ttu-id="dacec-137">停用 Internet Explorer 11 作為獨立瀏覽器</span><span class="sxs-lookup"><span data-stu-id="dacec-137">Disable Internet Explorer 11 as a standalone browser</span></span>

<span data-ttu-id="dacec-138">若要使用群組原則停用 Internet Explorer 11，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="dacec-138">To disable Internet Explorer 11 using group policy, follow these steps:</span></span>

1. <span data-ttu-id="dacec-139">請確保您擁有必要的作業系統更新。</span><span class="sxs-lookup"><span data-stu-id="dacec-139">Ensure you have the pre-requisite operating system updates.</span></span> <span data-ttu-id="dacec-140">此步驟會直接更新您電腦上的 ADMX 檔案 (具體為 inetres.adml 和 inetres.admx)。</span><span class="sxs-lookup"><span data-stu-id="dacec-140">This step will update the ADMX files on your machine directly (specifically inetres.adml and inetres.admx).</span></span> <span data-ttu-id="dacec-141">請注意，如果您想要更新 Central Store，您必須從具備必要更新之電腦複製 .adml 和 .admx 檔案。</span><span class="sxs-lookup"><span data-stu-id="dacec-141">Please note that if you want to update your Central Store, you will need to copy over the .adml and .admx files from a machine that has the pre-requisite updates.</span></span> <span data-ttu-id="dacec-142">如需詳細資訊，請參閱 [建立及管理 Central Store](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span><span class="sxs-lookup"><span data-stu-id="dacec-142">For more information, see [Create and manage Central Store](/troubleshoot/windows-client/group-policy/create-and-manage-central-store)</span></span>
2. <span data-ttu-id="dacec-143">開啟 [群組原則編輯器]。</span><span class="sxs-lookup"><span data-stu-id="dacec-143">Open the Group Policy Editor.</span></span>
3. <span data-ttu-id="dacec-144">移至***電腦設定/系統管理範本/Windows 元件/Internet Explorer***。</span><span class="sxs-lookup"><span data-stu-id="dacec-144">Go to ***Computer Configuration/Administrative Templates/Windows Components/Internet Explorer***.</span></span> 
4. <span data-ttu-id="dacec-145">按兩下 [停用 Internet Explorer 11 作為獨立瀏覽器] \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="dacec-145">Double-click **Disable Internet Explorer 11 as a standalone browser**.</span></span>
5. <span data-ttu-id="dacec-146">選取 [啟用] \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="dacec-146">Select **Enabled**.</span></span>
6. <span data-ttu-id="dacec-147">在 [選項] \*\*\*\* 下，挑選下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="dacec-147">Under **Options**, pick one of the following values:</span></span>

   - <span data-ttu-id="dacec-148">**永不** 如果您不想通知使用者 IE11 已停用。</span><span class="sxs-lookup"><span data-stu-id="dacec-148">**Never** if you don’t want to notify users that IE11 is disabled.</span></span>
   - <span data-ttu-id="dacec-149">**永遠** 如果您想要每次從 IE11 重新導向使用者時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="dacec-149">**Always** if you want to notify users every time they're redirected from IE11.</span></span>
   - <span data-ttu-id="dacec-150">**每位使用者一次** 如果您只想在使用者第一次重新導向時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="dacec-150">**Once per user** if you want to notify users only the first time they are redirected.</span></span>

7. <span data-ttu-id="dacec-151">按一下 [確定]  \*\*\*\*  或 [套用] \*\*\*\*  以儲存此原則設定。</span><span class="sxs-lookup"><span data-stu-id="dacec-151">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="dacec-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dacec-152">See also</span></span>

- [<span data-ttu-id="dacec-153">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="dacec-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="dacec-154">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="dacec-154">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="dacec-155">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="dacec-155">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
