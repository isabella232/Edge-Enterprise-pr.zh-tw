---
title: 設定 IE 模式原則
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 設定 IE 模式原則
ms.openlocfilehash: 57d0db97a96baf361f88ca8ec90812373440c3d8
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641469"
---
# <a name="configure-ie-mode-policies"></a><span data-ttu-id="ab062-103">設定 IE 模式原則</span><span class="sxs-lookup"><span data-stu-id="ab062-103">Configure IE mode policies</span></span>

>[!Note]
> <span data-ttu-id="ab062-104">Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。</span><span class="sxs-lookup"><span data-stu-id="ab062-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="ab062-105">您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="ab062-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="ab062-106">[從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。</span><span class="sxs-lookup"><span data-stu-id="ab062-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="ab062-107">本文說明如何設定 IE 模式原則。</span><span class="sxs-lookup"><span data-stu-id="ab062-107">This article explains how to configure IE mode policies.</span></span>

> [!NOTE]
> <span data-ttu-id="ab062-108">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ab062-108">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

<span data-ttu-id="ab062-109">設定 IE 模式需要三個步驟：</span><span class="sxs-lookup"><span data-stu-id="ab062-109">Configuring IE mode requires three steps:</span></span>

1. [<span data-ttu-id="ab062-110">設定 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="ab062-110">Configure Internet Explorer integration</span></span>](#configure-internet-explorer-integration)
2. [<span data-ttu-id="ab062-111">將網站從 Microsoft Edge 重新導向至 IE 模式</span><span class="sxs-lookup"><span data-stu-id="ab062-111">Redirect sites from Microsoft Edge to IE mode</span></span>](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. <span data-ttu-id="ab062-112">(選用) [將網站從 IE 重新導向至 Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="ab062-112">(Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span></span>

    1. <span data-ttu-id="ab062-113">如果您準備好停用 IE11 應用程式，請按照[停用 Internet Explorer 11](/deployedge/edge-ie-disable-ie11) 中的步驟進行</span><span class="sxs-lookup"><span data-stu-id="ab062-113">If you are ready to disable the IE11 app, follow the steps in [Disable Internet Explorer 11](/deployedge/edge-ie-disable-ie11)</span></span>
    2. <span data-ttu-id="ab062-114">否則，請遵循[將網站從 IE 重新導向至 Microsoft Edge](/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) 中的其餘步驟</span><span class="sxs-lookup"><span data-stu-id="ab062-114">Otherwise,  follow the rest of the steps in [Redirect sites from IE to Microsoft Edge](/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge)</span></span>

> [!NOTE]
> <span data-ttu-id="ab062-115">可透過 Intune 設定啟用 IE 模式的原則。</span><span class="sxs-lookup"><span data-stu-id="ab062-115">Policies to enable IE mode can be configured through Intune.</span></span> <span data-ttu-id="ab062-116">如需詳細資訊，請參閱[新增 Microsoft Edge 至 Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) 和[使用 Microsoft Intune 設定 Microsoft Edge 原則](./configure-edge-with-intune.md)。</span><span class="sxs-lookup"><span data-stu-id="ab062-116">For more information, see [Add Microsoft Edge to Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) and [Configure Microsoft Edge policies with Microsoft Intune](./configure-edge-with-intune.md).</span></span>

## <a name="configure-internet-explorer-integration"></a><span data-ttu-id="ab062-117">設定 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="ab062-117">Configure Internet Explorer integration</span></span>

<span data-ttu-id="ab062-118">您可以將 Internet Explorer 設定為直接在 Microsoft Edge 中開啟 (IE 模式)。</span><span class="sxs-lookup"><span data-stu-id="ab062-118">You can configure Internet Explorer to open directly within Microsoft Edge (IE mode).</span></span> <span data-ttu-id="ab062-119">您也可以將 Internet Explorer 設定為使用獨立的 Internet Explorer 11 視窗開啟。</span><span class="sxs-lookup"><span data-stu-id="ab062-119">You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window.</span></span> <span data-ttu-id="ab062-120">多數使用者偏好直接在 Microsoft Edge 內以 IE 模式開啟網站。</span><span class="sxs-lookup"><span data-stu-id="ab062-120">Most users prefer when sites open directly within Microsoft Edge in IE mode.</span></span>

### <a name="enable-internet-explorer-integration-using-group-policy"></a><span data-ttu-id="ab062-121">使用群組原則啟用 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="ab062-121">Enable Internet Explorer integration using Group Policy</span></span>

1. <span data-ttu-id="ab062-122">下載並使用最新的 [Microsoft Edge 原則範本](https://www.microsoft.com/en-us/edge/business/download)。</span><span class="sxs-lookup"><span data-stu-id="ab062-122">Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).</span></span>
2. <span data-ttu-id="ab062-123">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="ab062-123">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab062-124">按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="ab062-124">Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="ab062-125">按兩下**設定 Internet Explorer 整合。**</span><span class="sxs-lookup"><span data-stu-id="ab062-125">Double-click **Configure Internet Explorer integration**.</span></span>
5. <span data-ttu-id="ab062-126">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="ab062-126">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab062-127">在 [選項]\*\*\*\* 下，將下拉式清單值設定為</span><span class="sxs-lookup"><span data-stu-id="ab062-127">Under **Options**, set the dropdown value to</span></span> 
   -  <span data-ttu-id="ab062-128">如果您想要在 Microsoft Edge 中以 IE 模式開啟網站，請選取 [Internet Explorer 模式]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab062-128">**Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge</span></span>
   -  <span data-ttu-id="ab062-129">如果您想要在獨立式 Internet Explorer 11 視窗中開啟網站，請選取 [Internet Explorer 11]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab062-129">**Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window</span></span>
   -  <span data-ttu-id="ab062-130">如果您想要停止使用者透過 edge://flags 或透過命令列設定 Internet Explorer 模式，請選取 [無]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab062-130">**None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line</span></span>

   > [!NOTE]
   > <span data-ttu-id="ab062-131">將原則設定為 [已停用]\*\*\*\* 表示 IE 模式已透過原則停用，但可透過 edge://flags 或命令列選項設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-131">Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.</span></span>
7. <span data-ttu-id="ab062-132">按一下**確定**或**套用**儲存此原則設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-132">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a><span data-ttu-id="ab062-133">將網站從 Microsoft Edge 重新導向至 IE 模式</span><span class="sxs-lookup"><span data-stu-id="ab062-133">Redirect sites from Microsoft Edge to IE mode</span></span>

<span data-ttu-id="ab062-134">有兩個選項用於識別應在 IE 模式下開啟的網站：</span><span class="sxs-lookup"><span data-stu-id="ab062-134">There are two options for identifying which sites should open in IE mode:</span></span>

- <span data-ttu-id="ab062-135">(建議) [在企業網站清單中設定網站](#configure-sites-on-the-enterprise-site-list)</span><span class="sxs-lookup"><span data-stu-id="ab062-135">(Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)</span></span>
- [<span data-ttu-id="ab062-136">設定所有內部網路網站</span><span class="sxs-lookup"><span data-stu-id="ab062-136">Configure all Intranet sites</span></span>](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a><span data-ttu-id="ab062-137">在企業網站清單中設定網站</span><span class="sxs-lookup"><span data-stu-id="ab062-137">Configure sites on the Enterprise Site list</span></span>

<span data-ttu-id="ab062-138">您可以使用以下群組原則，將特定網站設定為在 IE 模式下開啟：</span><span class="sxs-lookup"><span data-stu-id="ab062-138">You can use the following group policies to configure specific sites to open in IE mode:</span></span>

- <span data-ttu-id="ab062-139">[使用企業模式 IE 網站清單](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="ab062-139">[Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span></span>
- <span data-ttu-id="ab062-140">[設定企業模式網站清單](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge 版本 78 或更新版本)</span><span class="sxs-lookup"><span data-stu-id="ab062-140">[Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)</span></span><br/><span data-ttu-id="ab062-141">此原則允許您針對 Microsoft Edge 建立單獨的企業模式網站清單。</span><span class="sxs-lookup"><span data-stu-id="ab062-141">This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge.</span></span> <span data-ttu-id="ab062-142">啟用此原則將覆寫 [使用企業模式 IE 網站清單] 原則中的設定，如果已啟用 [設定 Internet Explorer 整合]。</span><span class="sxs-lookup"><span data-stu-id="ab062-142">Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled.</span></span> <span data-ttu-id="ab062-143">停用或不設定此原則不會影響 [設定 Internet Explorer 整合] 原則的預設行為。</span><span class="sxs-lookup"><span data-stu-id="ab062-143">Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ab062-144">不強制設定 Microsoft Edge 原則。</span><span class="sxs-lookup"><span data-stu-id="ab062-144">It is not mandatory to configure the Microsoft Edge policy.</span></span> <span data-ttu-id="ab062-145">許多組織會使用這項作為覆寫，讓他們以 IE 原則將目前網站清單的目標設定為所有使用者，並更輕鬆地將已更新版本的目標設定為具有 Microsoft Edge 原則的試驗使用者。</span><span class="sxs-lookup"><span data-stu-id="ab062-145">Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.</span></span>

<span data-ttu-id="ab062-146">如需企業模式網站清單的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="ab062-146">For more information about Enterprise Mode Site lists, see:</span></span>

- [<span data-ttu-id="ab062-147">使用 Enterprise Mode Site List Manager</span><span class="sxs-lookup"><span data-stu-id="ab062-147">Use the Enterprise Mode Site List Manager</span></span>](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- <span data-ttu-id="ab062-148">[使用檔案和 Enterprise Mode Site List Manager (結構描述 v.2) 將多個網站新增到企業模式網站清單](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool)。</span><span class="sxs-lookup"><span data-stu-id="ab062-148">[Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span></span>

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a><span data-ttu-id="ab062-149">使用 [使用企業模式 IE 網站清單] 原則進行設定：</span><span class="sxs-lookup"><span data-stu-id="ab062-149">Configure using the Use the Enterprise Mode IE website list policy</span></span>

<span data-ttu-id="ab062-150">IE 模式可以使用現有原則來設定 Internet Explorer 的企業網站清單，讓您建立並維護單一清單。</span><span class="sxs-lookup"><span data-stu-id="ab062-150">IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.</span></span>

1. <span data-ttu-id="ab062-151">建立或重複使用網站清單 XML</span><span class="sxs-lookup"><span data-stu-id="ab062-151">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="ab062-152">具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="ab062-152">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="ab062-153">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="ab062-153">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab062-154">按一下**使用者設定/電腦設定** > **系統管理範本** > **Windows 元件** > **Internet Explorer**。</span><span class="sxs-lookup"><span data-stu-id="ab062-154">Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.</span></span>
4. <span data-ttu-id="ab062-155">按兩下**使用企業模式 IE 網站清單**。</span><span class="sxs-lookup"><span data-stu-id="ab062-155">Double-click **Use the Enterprise Mode IE website list**.</span></span>
5. <span data-ttu-id="ab062-156">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="ab062-156">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab062-157">在**選項**下，鍵入網站清單的位置。</span><span class="sxs-lookup"><span data-stu-id="ab062-157">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="ab062-158">您可以使用下列其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="ab062-158">You can use one of the following locations:</span></span>
    - <span data-ttu-id="ab062-159">(建議) HTTPS 位置：**https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-159">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span>
    - <span data-ttu-id="ab062-160">區域網路檔案：**\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-160">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="ab062-161">本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-161">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="ab062-162">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-162">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a><span data-ttu-id="ab062-163">使用 [設定企業模式網站清單] 原則進行設定</span><span class="sxs-lookup"><span data-stu-id="ab062-163">Configure using the Configure the Enterprise Mode Site List policy</span></span>

<span data-ttu-id="ab062-164">您也可以使用 Microsoft Edge 的個別原則來設定 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="ab062-164">You can also configure IE mode with a separate policy for Microsoft Edge.</span></span> <span data-ttu-id="ab062-165">這個額外原則可讓您覆寫 IE 網站清單。</span><span class="sxs-lookup"><span data-stu-id="ab062-165">This additional policy allows you to override the IE site list.</span></span> <span data-ttu-id="ab062-166">例如，某些組織會將生產環境網站清單的目標設定為所有使用者。</span><span class="sxs-lookup"><span data-stu-id="ab062-166">For example, some organizations will target the production site list to all users.</span></span> <span data-ttu-id="ab062-167">然後，您可以使用此原則將試驗網站清單部署到一小組使用者。</span><span class="sxs-lookup"><span data-stu-id="ab062-167">You can then deploy the pilot site list to a small group of users using this policy.</span></span>

1. <span data-ttu-id="ab062-168">建立或重複使用網站清單 XML</span><span class="sxs-lookup"><span data-stu-id="ab062-168">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="ab062-169">具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="ab062-169">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="ab062-170">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="ab062-170">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="ab062-171">按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="ab062-171">Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="ab062-172">按兩下**設定企業模式網站清單**。</span><span class="sxs-lookup"><span data-stu-id="ab062-172">Double-click **Configure the Enterprise Mode Site List**.</span></span>
5. <span data-ttu-id="ab062-173">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="ab062-173">Select **Enabled**.</span></span>
6. <span data-ttu-id="ab062-174">在**選項**下，鍵入網站清單的位置。</span><span class="sxs-lookup"><span data-stu-id="ab062-174">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="ab062-175">您可以使用下列其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="ab062-175">You can use one of the following locations:</span></span>
    - <span data-ttu-id="ab062-176">(建議) HTTPS 位置：**https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-176">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span> <!--Trying to keep this from being an active link in MD -->
    - <span data-ttu-id="ab062-177">區域網路檔案：**\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-177">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="ab062-178">本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="ab062-178">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="ab062-179">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-179">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-all-intranet-sites"></a><span data-ttu-id="ab062-180">設定所有內部網路網站</span><span class="sxs-lookup"><span data-stu-id="ab062-180">Configure all intranet sites</span></span>

<span data-ttu-id="ab062-181">IE 模式可以設定為針對 [本機內部網路] 區域中的所有網站。</span><span class="sxs-lookup"><span data-stu-id="ab062-181">IE mode can be configured as for all sites in the Local Intranet zone.</span></span> <span data-ttu-id="ab062-182">您可以使用企業模式網站清單從 IE 模式移除個別網站。</span><span class="sxs-lookup"><span data-stu-id="ab062-182">You can remove individual sites from IE mode using an Enterprise Mode Site List.</span></span>

>[!NOTE]
>
> <span data-ttu-id="ab062-183">[本地內部網路] 區域包含明確新增的網站，但是也會使用啟發式學習法將網站指派給這個區域。</span><span class="sxs-lookup"><span data-stu-id="ab062-183">The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics.</span></span> <span data-ttu-id="ab062-184">這可以包括無點主機名稱 (例如，**https**:**//payroll**)以及 Proxy 設定指令碼設定為略過 Proxy 的網站。</span><span class="sxs-lookup"><span data-stu-id="ab062-184">This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy.</span></span> <span data-ttu-id="ab062-185">如果外部合作對象控制 DNS 或 Proxy，他們可能可以強制網站進入 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="ab062-185">If an external party controls DNS or proxy, they could potentially force websites into IE mode.</span></span>

1. <span data-ttu-id="ab062-186">開啟 [本機群組原則編輯器]。</span><span class="sxs-lookup"><span data-stu-id="ab062-186">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="ab062-187">按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="ab062-187">Click **User Configuration/Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="ab062-188">按兩下**將所有內部網路網站傳送到 Internet Explorer**。</span><span class="sxs-lookup"><span data-stu-id="ab062-188">Double-click **Send all intranet sites to Internet Explorer**.</span></span>
4. <span data-ttu-id="ab062-189">選取**已啟用**，然後按一下**確定**或**套用**以儲存原則設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-189">Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.</span></span>

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a><span data-ttu-id="ab062-190">將網站從 IE 重新導向至 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ab062-190">Redirect sites from IE to Microsoft Edge</span></span>

<span data-ttu-id="ab062-191">您可以防止使用者針對不需要的網站使用 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="ab062-191">You can prevent your users from using Internet Explorer for sites that don't need it.</span></span> <span data-ttu-id="ab062-192">如果網站不在您的網站清單上，Internet Explorer 可以自動將網站重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="ab062-192">Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.</span></span>

1. <span data-ttu-id="ab062-193">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="ab062-193">Open Group Policy Editor.</span></span>
2. <span data-ttu-id="ab062-194">按一下**使用者設定/電腦設定** > **系統管理工具** > **Windows 元件** > **Internet Explorer**。</span><span class="sxs-lookup"><span data-stu-id="ab062-194">Click **User Configuration/Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.</span></span>
3. <span data-ttu-id="ab062-195">按兩下 [將未包含在企業模式網站清單中的所有網站傳送到 Microsoft Edge]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ab062-195">Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**</span></span>
4. <span data-ttu-id="ab062-196">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ab062-196">Select **Enabled**</span></span>
5. <span data-ttu-id="ab062-197">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-197">Click **OK** or **Apply** to save these settings.</span></span>
6. <span data-ttu-id="ab062-198">按兩下 [設定用來開啟重新導向網站的 Microsoft Edge 通道]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ab062-198">Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.</span></span>
7. <span data-ttu-id="ab062-199">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="ab062-199">Select **Enabled**.</span></span>
8. <span data-ttu-id="ab062-200">在 [選項]\*\*\*\* 底下，選取您要使用的通道前三個選項 - Internet Explorer 會重新導向至使用者已在該裝置上安裝的最高等級選項：</span><span class="sxs-lookup"><span data-stu-id="ab062-200">Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:</span></span>
   - <span data-ttu-id="ab062-201">Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="ab062-201">Microsoft Edge Stable</span></span>
   - <span data-ttu-id="ab062-202">Microsoft Edge Beta 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ab062-202">Microsoft Edge Beta version 77 or later</span></span>
   - <span data-ttu-id="ab062-203">Microsoft Edge Dev 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ab062-203">Microsoft Edge Dev version 77 or later</span></span>
   - <span data-ttu-id="ab062-204">Microsoft Edge Canary 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ab062-204">Microsoft Edge Canary version 77 or later</span></span>
   - <span data-ttu-id="ab062-205">Microsoft Edge 版本 45 或較舊版本</span><span class="sxs-lookup"><span data-stu-id="ab062-205">Microsoft Edge version 45 or earlier</span></span>
9. <span data-ttu-id="ab062-206">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="ab062-206">Click **OK** or **Apply** to save these settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab062-207">請參閱</span><span class="sxs-lookup"><span data-stu-id="ab062-207">See also</span></span>

- [<span data-ttu-id="ab062-208">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="ab062-208">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="ab062-209">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="ab062-209">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="ab062-210">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="ab062-210">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)