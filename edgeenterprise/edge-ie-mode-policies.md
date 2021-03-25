---
title: 設定 IE 模式原則
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 03/25/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 IE 模式原則
ms.openlocfilehash: e33aa57b7877d50fe6a5d9e9a888d05c366b0ef0
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447357"
---
# <a name="configure-ie-mode-policies"></a><span data-ttu-id="02a19-103">設定 IE 模式原則</span><span class="sxs-lookup"><span data-stu-id="02a19-103">Configure IE mode policies</span></span>

<span data-ttu-id="02a19-104">本文說明如何設定 IE 模式原則。</span><span class="sxs-lookup"><span data-stu-id="02a19-104">This article explains how to configure IE mode policies.</span></span>

> [!NOTE]
> <span data-ttu-id="02a19-105">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="02a19-105">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

<span data-ttu-id="02a19-106">設定 IE 模式需要三個步驟：</span><span class="sxs-lookup"><span data-stu-id="02a19-106">Configuring IE mode requires three steps:</span></span>

1. [<span data-ttu-id="02a19-107">設定 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="02a19-107">Configure Internet Explorer integration</span></span>](#configure-internet-explorer-integration)
2. [<span data-ttu-id="02a19-108">將網站從 Microsoft Edge 重新導向至 IE 模式</span><span class="sxs-lookup"><span data-stu-id="02a19-108">Redirect sites from Microsoft Edge to IE mode</span></span>](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. <span data-ttu-id="02a19-109">(選用) [將網站從 IE 重新導向至 Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span><span class="sxs-lookup"><span data-stu-id="02a19-109">(Optional) [Redirect sites from IE to Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)</span></span>

> [!NOTE]
> <span data-ttu-id="02a19-110">可透過 Intune 設定啟用 IE 模式的原則。</span><span class="sxs-lookup"><span data-stu-id="02a19-110">Policies to enable IE mode can be configured through Intune.</span></span> <span data-ttu-id="02a19-111">如需詳細資訊，請參閱[新增 Microsoft Edge 至 Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) 和[使用 Microsoft Intune 設定 Microsoft Edge 原則](./configure-edge-with-intune.md)。</span><span class="sxs-lookup"><span data-stu-id="02a19-111">For more information, see [Add Microsoft Edge to Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) and [Configure Microsoft Edge policies with Microsoft Intune](./configure-edge-with-intune.md).</span></span>

## <a name="configure-internet-explorer-integration"></a><span data-ttu-id="02a19-112">設定 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="02a19-112">Configure Internet Explorer integration</span></span>

<span data-ttu-id="02a19-113">您可以將 Internet Explorer 設定為直接在 Microsoft Edge 中開啟 (IE 模式)。</span><span class="sxs-lookup"><span data-stu-id="02a19-113">You can configure Internet Explorer to open directly within Microsoft Edge (IE mode).</span></span> <span data-ttu-id="02a19-114">您也可以將 Internet Explorer 設定為使用獨立的 Internet Explorer 11 視窗開啟。</span><span class="sxs-lookup"><span data-stu-id="02a19-114">You can also configure Internet Explorer to open with a standalone Internet Explorer 11 window.</span></span> <span data-ttu-id="02a19-115">多數使用者偏好直接在 Microsoft Edge 內以 IE 模式開啟網站。</span><span class="sxs-lookup"><span data-stu-id="02a19-115">Most users prefer when sites open directly within Microsoft Edge in IE mode.</span></span>

### <a name="enable-internet-explorer-integration-using-group-policy"></a><span data-ttu-id="02a19-116">使用群組原則啟用 Internet Explorer 整合</span><span class="sxs-lookup"><span data-stu-id="02a19-116">Enable Internet Explorer integration using Group Policy</span></span>

1. <span data-ttu-id="02a19-117">下載並使用最新的 [Microsoft Edge 原則範本](https://www.microsoft.com/en-us/edge/business/download)。</span><span class="sxs-lookup"><span data-stu-id="02a19-117">Download and use the latest [Microsoft Edge Policy Template](https://www.microsoft.com/en-us/edge/business/download).</span></span>
2. <span data-ttu-id="02a19-118">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="02a19-118">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="02a19-119">按一下**電腦組態** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="02a19-119">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="02a19-120">按兩下**設定 Internet Explorer 整合。**</span><span class="sxs-lookup"><span data-stu-id="02a19-120">Double-click **Configure Internet Explorer integration**.</span></span>
5. <span data-ttu-id="02a19-121">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="02a19-121">Select **Enabled**.</span></span>
6. <span data-ttu-id="02a19-122">在 [選項]\*\*\*\* 下，將下拉式清單值設定為</span><span class="sxs-lookup"><span data-stu-id="02a19-122">Under **Options**, set the dropdown value to</span></span> 
   -  <span data-ttu-id="02a19-123">如果您想要在 Microsoft Edge 中以 IE 模式開啟網站，請選取 [Internet Explorer 模式]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="02a19-123">**Internet Explorer mode** if you want sites to open in IE mode on Microsoft Edge</span></span>
   -  <span data-ttu-id="02a19-124">如果您想要在獨立式 Internet Explorer 11 視窗中開啟網站，請選取 [Internet Explorer 11]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="02a19-124">**Internet Explorer 11** if you want sites to open in a standalone Internet Explorer 11 window</span></span>
   -  <span data-ttu-id="02a19-125">如果您想要停止使用者透過 edge://flags 或透過命令列設定 Internet Explorer 模式，請選取 [無]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="02a19-125">**None** if you want to stop users from configuring Internet Explorer mode via edge://flags or through the command line</span></span>

   > [!NOTE]
   > <span data-ttu-id="02a19-126">將原則設定為 [已停用]\*\*\*\* 表示 IE 模式已透過原則停用，但可透過 edge://flags 或命令列選項設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-126">Setting the policy to **Disabled** implies IE mode is disabled by policy, but can be set through edge://flags or command line options.</span></span>
7. <span data-ttu-id="02a19-127">按一下**確定**或**套用**儲存此原則設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-127">Click **OK** or **Apply** to save this policy setting.</span></span>

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a><span data-ttu-id="02a19-128">將網站從 Microsoft Edge 重新導向至 IE 模式</span><span class="sxs-lookup"><span data-stu-id="02a19-128">Redirect sites from Microsoft Edge to IE mode</span></span>

<span data-ttu-id="02a19-129">有兩個選項用於識別應在 IE 模式下開啟的網站：</span><span class="sxs-lookup"><span data-stu-id="02a19-129">There are two options for identifying which sites should open in IE mode:</span></span>

- <span data-ttu-id="02a19-130">(建議) [在企業網站清單中設定網站](#configure-sites-on-the-enterprise-site-list)</span><span class="sxs-lookup"><span data-stu-id="02a19-130">(Recommended) [Configure sites on the Enterprise Site list](#configure-sites-on-the-enterprise-site-list)</span></span>
- [<span data-ttu-id="02a19-131">設定所有內部網路網站</span><span class="sxs-lookup"><span data-stu-id="02a19-131">Configure all Intranet sites</span></span>](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a><span data-ttu-id="02a19-132">在企業網站清單中設定網站</span><span class="sxs-lookup"><span data-stu-id="02a19-132">Configure sites on the Enterprise Site list</span></span>

<span data-ttu-id="02a19-133">您可以使用以下群組原則，將特定網站設定為在 IE 模式下開啟：</span><span class="sxs-lookup"><span data-stu-id="02a19-133">You can use the following group policies to configure specific sites to open in IE mode:</span></span>

- <span data-ttu-id="02a19-134">[使用企業模式 IE 網站清單](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="02a19-134">[Use the Enterprise Mode IE website list](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)</span></span>
- <span data-ttu-id="02a19-135">[設定企業模式網站清單](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge 版本 78 或更新版本)</span><span class="sxs-lookup"><span data-stu-id="02a19-135">[Configure the Enterprise Mode Site List](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge, version 78 or later)</span></span><br/><span data-ttu-id="02a19-136">此原則允許您針對 Microsoft Edge 建立單獨的企業模式網站清單。</span><span class="sxs-lookup"><span data-stu-id="02a19-136">This policy lets you create a separate Enterprise Mode Site list for Microsoft Edge.</span></span> <span data-ttu-id="02a19-137">啟用此原則將覆寫 [使用企業模式 IE 網站清單] 原則中的設定，如果已啟用 [設定 Internet Explorer 整合]。</span><span class="sxs-lookup"><span data-stu-id="02a19-137">Enabling this policy overrides the settings in the "Use the Enterprise Mode IE website list" policy, if "Configure Internet Explorer integration" is enabled.</span></span> <span data-ttu-id="02a19-138">停用或不設定此原則不會影響 [設定 Internet Explorer 整合] 原則的預設行為。</span><span class="sxs-lookup"><span data-stu-id="02a19-138">Disabling or not configuring this policy doesn't affect the default behavior of the "Configure Internet Explorer integration" policy.</span></span>
    > [!NOTE]
    > <span data-ttu-id="02a19-139">不強制設定 Microsoft Edge 原則。</span><span class="sxs-lookup"><span data-stu-id="02a19-139">It is not mandatory to configure the Microsoft Edge policy.</span></span> <span data-ttu-id="02a19-140">許多組織會使用這項作為覆寫，讓他們以 IE 原則將目前網站清單的目標設定為所有使用者，並更輕鬆地將已更新版本的目標設定為具有 Microsoft Edge 原則的試驗使用者。</span><span class="sxs-lookup"><span data-stu-id="02a19-140">Many organizations use this as an override, allowing them to target the current Site List at all users with the IE policy, and more easily target an updated version to pilot uses with the Microsoft Edge policy.</span></span>

<span data-ttu-id="02a19-141">如需企業模式網站清單的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="02a19-141">For more information about Enterprise Mode Site lists, see:</span></span>

- [<span data-ttu-id="02a19-142">使用 Enterprise Mode Site List Manager</span><span class="sxs-lookup"><span data-stu-id="02a19-142">Use the Enterprise Mode Site List Manager</span></span>](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- <span data-ttu-id="02a19-143">[使用檔案和 Enterprise Mode Site List Manager (結構描述 v.2) 將多個網站新增到企業模式網站清單](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool)。</span><span class="sxs-lookup"><span data-stu-id="02a19-143">[Add multiple sites to the Enterprise Mode site list using a file and the Enterprise Mode Site List Manager (schema v.2)](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool).</span></span>

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a><span data-ttu-id="02a19-144">使用 [使用企業模式 IE 網站清單] 原則進行設定：</span><span class="sxs-lookup"><span data-stu-id="02a19-144">Configure using the Use the Enterprise Mode IE website list policy</span></span>

<span data-ttu-id="02a19-145">IE 模式可以使用現有原則來設定 Internet Explorer 的企業網站清單，讓您建立並維護單一清單。</span><span class="sxs-lookup"><span data-stu-id="02a19-145">IE mode can use the existing policy configuring the Enterprise Site List for Internet Explorer, allowing you to create and maintain a single list.</span></span>

1. <span data-ttu-id="02a19-146">建立或重複使用網站清單 XML</span><span class="sxs-lookup"><span data-stu-id="02a19-146">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="02a19-147">具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="02a19-147">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="02a19-148">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="02a19-148">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="02a19-149">按一下**電腦設定** > **系統管理範本** > **Windows 元件** > **Internet Explorer**。</span><span class="sxs-lookup"><span data-stu-id="02a19-149">Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**.</span></span>
4. <span data-ttu-id="02a19-150">按兩下**使用企業模式 IE 網站清單**。</span><span class="sxs-lookup"><span data-stu-id="02a19-150">Double-click **Use the Enterprise Mode IE website list**.</span></span>
5. <span data-ttu-id="02a19-151">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="02a19-151">Select **Enabled**.</span></span>
6. <span data-ttu-id="02a19-152">在**選項**下，鍵入網站清單的位置。</span><span class="sxs-lookup"><span data-stu-id="02a19-152">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="02a19-153">您可以使用下列其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="02a19-153">You can use one of the following locations:</span></span>
    - <span data-ttu-id="02a19-154">(建議) HTTPS 位置：**https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-154">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span>
    - <span data-ttu-id="02a19-155">區域網路檔案：**\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-155">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="02a19-156">本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-156">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="02a19-157">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-157">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a><span data-ttu-id="02a19-158">使用 [設定企業模式網站清單] 原則進行設定</span><span class="sxs-lookup"><span data-stu-id="02a19-158">Configure using the Configure the Enterprise Mode Site List policy</span></span>

<span data-ttu-id="02a19-159">您也可以使用 Microsoft Edge 的個別原則來設定 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="02a19-159">You can also configure IE mode with a separate policy for Microsoft Edge.</span></span> <span data-ttu-id="02a19-160">這個額外原則可讓您覆寫 IE 網站清單。</span><span class="sxs-lookup"><span data-stu-id="02a19-160">This additional policy allows you to override the IE site list.</span></span> <span data-ttu-id="02a19-161">例如，某些組織會將生產環境網站清單的目標設定為所有使用者。</span><span class="sxs-lookup"><span data-stu-id="02a19-161">For example, some organizations will target the production site list to all users.</span></span> <span data-ttu-id="02a19-162">然後，您可以使用此原則將試驗網站清單部署到一小組使用者。</span><span class="sxs-lookup"><span data-stu-id="02a19-162">You can then deploy the pilot site list to a small group of users using this policy.</span></span>

1. <span data-ttu-id="02a19-163">建立或重複使用網站清單 XML</span><span class="sxs-lookup"><span data-stu-id="02a19-163">Create or reuse a Site List XML</span></span>
    1. <span data-ttu-id="02a19-164">具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="02a19-164">All sites that have the element _\<open-in\>IE11\</open-in\>_ will now open in IE mode.</span></span>
2. <span data-ttu-id="02a19-165">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="02a19-165">Open Group Policy Editor.</span></span>
3. <span data-ttu-id="02a19-166">按一下**電腦組態** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="02a19-166">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
4. <span data-ttu-id="02a19-167">按兩下**設定企業模式網站清單**。</span><span class="sxs-lookup"><span data-stu-id="02a19-167">Double-click **Configure the Enterprise Mode Site List**.</span></span>
5. <span data-ttu-id="02a19-168">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="02a19-168">Select **Enabled**.</span></span>
6. <span data-ttu-id="02a19-169">在**選項**下，鍵入網站清單的位置。</span><span class="sxs-lookup"><span data-stu-id="02a19-169">Under **Options**, type the location of website list.</span></span> <span data-ttu-id="02a19-170">您可以使用下列其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="02a19-170">You can use one of the following locations:</span></span>
    - <span data-ttu-id="02a19-171">(建議) HTTPS 位置：**https**:**//iemode/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-171">(Recommended) HTTPS location: **https**:**//iemode/sites.xml**</span></span> <!--Trying to keep this from being an active link in MD -->
    - <span data-ttu-id="02a19-172">區域網路檔案：**\\\network\shares\sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-172">Local network file: **\\\network\shares\sites.xml**</span></span>
    - <span data-ttu-id="02a19-173">本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**</span><span class="sxs-lookup"><span data-stu-id="02a19-173">Local file: **file:///c:/Users/\<user\>/Documents/sites.xml**</span></span>
7. <span data-ttu-id="02a19-174">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-174">Click **OK** or **Apply** to save these settings.</span></span>

### <a name="configure-all-intranet-sites"></a><span data-ttu-id="02a19-175">設定所有內部網路網站</span><span class="sxs-lookup"><span data-stu-id="02a19-175">Configure all intranet sites</span></span>

<span data-ttu-id="02a19-176">IE 模式可以設定為針對 [本機內部網路] 區域中的所有網站。</span><span class="sxs-lookup"><span data-stu-id="02a19-176">IE mode can be configured as for all sites in the Local Intranet zone.</span></span> <span data-ttu-id="02a19-177">您可以使用企業模式網站清單從 IE 模式移除個別網站。</span><span class="sxs-lookup"><span data-stu-id="02a19-177">You can remove individual sites from IE mode using an Enterprise Mode Site List.</span></span>

>[!NOTE]
>
> <span data-ttu-id="02a19-178">[本地內部網路] 區域包含明確新增的網站，但是也會使用啟發式學習法將網站指派給這個區域。</span><span class="sxs-lookup"><span data-stu-id="02a19-178">The Local Intranet zone contains explicitly added sites, but also assigns sites to this zone using heuristics.</span></span> <span data-ttu-id="02a19-179">這可以包括無點主機名稱 (例如，**https**:**//payroll**)以及 Proxy 設定指令碼設定為略過 Proxy 的網站。</span><span class="sxs-lookup"><span data-stu-id="02a19-179">This can include dotless host names (e.g. **https**:**//payroll**) and sites that the proxy configuration script configures to bypass the proxy.</span></span> <span data-ttu-id="02a19-180">如果外部合作對象控制 DNS 或 Proxy，他們可能可以強制網站進入 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="02a19-180">If an external party controls DNS or proxy, they could potentially force websites into IE mode.</span></span>

1. <span data-ttu-id="02a19-181">開啟 [本機群組原則編輯器]。</span><span class="sxs-lookup"><span data-stu-id="02a19-181">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="02a19-182">按一下**電腦組態** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="02a19-182">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="02a19-183">按兩下**將所有內部網路網站傳送到 Internet Explorer**。</span><span class="sxs-lookup"><span data-stu-id="02a19-183">Double-click **Send all intranet sites to Internet Explorer**.</span></span>
4. <span data-ttu-id="02a19-184">選取**已啟用**，然後按一下**確定**或**套用**以儲存原則設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-184">Select **Enabled**, and then click **OK** or **Apply** to save the policy settings.</span></span>

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a><span data-ttu-id="02a19-185">將網站從 IE 重新導向至 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="02a19-185">Redirect sites from IE to Microsoft Edge</span></span>

<span data-ttu-id="02a19-186">您可以防止使用者針對不需要的網站使用 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="02a19-186">You can prevent your users from using Internet Explorer for sites that don't need it.</span></span> <span data-ttu-id="02a19-187">如果網站不在您的網站清單上，Internet Explorer 可以自動將網站重新導向至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="02a19-187">Internet Explorer can automatically redirect sites to Microsoft Edge if they aren't on your site list.</span></span>

1. <span data-ttu-id="02a19-188">開啟群組原則編輯器。</span><span class="sxs-lookup"><span data-stu-id="02a19-188">Open Group Policy Editor.</span></span>
2. <span data-ttu-id="02a19-189">按一下 [電腦設定]\*\*\*\* >  [系統管理工具]\*\*\*\* >  [Windows 元件]\*\*\*\* >  [Internet Explorer]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="02a19-189">Click **Computer Configuration** > **Administrative Tools** > **Windows Components** > **Internet Explorer**.</span></span>
3. <span data-ttu-id="02a19-190">按兩下 [將未包含在企業模式網站清單中的所有網站傳送到 Microsoft Edge]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="02a19-190">Double-click **Send all sites not included in the Enterprise Mode Site List to Microsoft Edge.**</span></span>
4. <span data-ttu-id="02a19-191">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="02a19-191">Select **Enabled**</span></span>
5. <span data-ttu-id="02a19-192">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-192">Click **OK** or **Apply** to save these settings.</span></span>
6. <span data-ttu-id="02a19-193">按兩下 [設定用來開啟重新導向網站的 Microsoft Edge 通道]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="02a19-193">Double-click **Configure which channel of Microsoft Edge to use for opening redirected sites**.</span></span>
7. <span data-ttu-id="02a19-194">選取 **\[已啟用\]**。</span><span class="sxs-lookup"><span data-stu-id="02a19-194">Select **Enabled**.</span></span>
8. <span data-ttu-id="02a19-195">在 [選項]\*\*\*\* 底下，選取您要使用的通道前三個選項 - Internet Explorer 會重新導向至使用者已在該裝置上安裝的最高等級選項：</span><span class="sxs-lookup"><span data-stu-id="02a19-195">Under **Options**, select your top three choices for the channel to use - Internet Explorer will redirect to the highest ranked choice that the user has installed on that device:</span></span>
   - <span data-ttu-id="02a19-196">Microsoft Edge Stable</span><span class="sxs-lookup"><span data-stu-id="02a19-196">Microsoft Edge Stable</span></span>
   - <span data-ttu-id="02a19-197">Microsoft Edge Beta 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="02a19-197">Microsoft Edge Beta version 77 or later</span></span>
   - <span data-ttu-id="02a19-198">Microsoft Edge Dev 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="02a19-198">Microsoft Edge Dev version 77 or later</span></span>
   - <span data-ttu-id="02a19-199">Microsoft Edge Canary 版本 77 或更新版本</span><span class="sxs-lookup"><span data-stu-id="02a19-199">Microsoft Edge Canary version 77 or later</span></span>
   - <span data-ttu-id="02a19-200">Microsoft Edge 版本 45 或較舊版本</span><span class="sxs-lookup"><span data-stu-id="02a19-200">Microsoft Edge version 45 or earlier</span></span>
9. <span data-ttu-id="02a19-201">按一下**確定**或**套用**儲存這些設定。</span><span class="sxs-lookup"><span data-stu-id="02a19-201">Click **OK** or **Apply** to save these settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="02a19-202">請參閱</span><span class="sxs-lookup"><span data-stu-id="02a19-202">See also</span></span>

- [<span data-ttu-id="02a19-203">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="02a19-203">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="02a19-204">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="02a19-204">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="02a19-205">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="02a19-205">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)