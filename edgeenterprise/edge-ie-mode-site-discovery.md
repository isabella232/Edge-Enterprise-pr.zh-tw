---
title: Enterprise Site Discovery 逐步指南
ms.author: collw
author: appcompatguy
manager: saudm
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 Enterprise Site Discovery 準備 IE 模式
ms.openlocfilehash: f6298b801cceeb96d9285f3597de2a6abe8ee36e
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617473"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a><span data-ttu-id="792e5-103">Enterprise Site Discovery 逐步指南</span><span class="sxs-lookup"><span data-stu-id="792e5-103">Enterprise Site Discovery Step-by-Step Guide</span></span>

>[!Note]
> <span data-ttu-id="792e5-104">Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。</span><span class="sxs-lookup"><span data-stu-id="792e5-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="792e5-105">您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="792e5-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="792e5-106">[從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。</span><span class="sxs-lookup"><span data-stu-id="792e5-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="792e5-107">本文提供將 Enterprise Site Discovery 與 Microsoft Endpoint Configuration Manager 搭配使用的逐步指南。</span><span class="sxs-lookup"><span data-stu-id="792e5-107">This article provides a step-by-step guide to using Enterprise Site Discovery with Microsoft Endpoint Configuration Manager.</span></span>

<span data-ttu-id="792e5-108">Enterprise Site Discovery 可協助您設定企業模式網站清單。</span><span class="sxs-lookup"><span data-stu-id="792e5-108">Enterprise Site Discovery can help you configure your Enterprise Mode Site List.</span></span> <span data-ttu-id="792e5-109">Enterprise Site Discovery 將協助您：</span><span class="sxs-lookup"><span data-stu-id="792e5-109">Enterprise Site Discovery will help you:</span></span>

- <span data-ttu-id="792e5-110">探索哪些網站使用舊版文件模式。</span><span class="sxs-lookup"><span data-stu-id="792e5-110">Discover which sites are using legacy document modes.</span></span> <span data-ttu-id="792e5-111">除非這些網站偵測新式瀏覽器並提供不同 HTML，否則可能需要使用 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="792e5-111">Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.</span></span>
- <span data-ttu-id="792e5-112">探索哪些網站使用 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="792e5-112">Discover which sites are using ActiveX controls.</span></span> <span data-ttu-id="792e5-113">Microsoft Edge 不支援 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="792e5-113">Microsoft Edge doesn't support ActiveX controls.</span></span> <span data-ttu-id="792e5-114">除非這些網站偵測新式瀏覽器並提供不同 HTML，否則可能需要使用 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="792e5-114">Unless these sites are detecting modern browsers and providing different HTML, they probably need to use IE mode.</span></span>

> [!NOTE]
> <span data-ttu-id="792e5-115">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="792e5-115">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="792e5-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="792e5-116">Prerequisites</span></span>

<span data-ttu-id="792e5-117">本指南假設您已使用過 Microsoft Endpoint Configuration Manager，且已安裝下列服務和角色：</span><span class="sxs-lookup"><span data-stu-id="792e5-117">This guide assumes you're experienced with using Microsoft Endpoint Configuration Manager and have the following services and roles installed:</span></span>

1. <span data-ttu-id="792e5-118">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="792e5-118">Microsoft Endpoint Configuration Manager</span></span>
2. <span data-ttu-id="792e5-119">Microsoft SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="792e5-119">Microsoft SQL Server Reporting Services</span></span>
3. <span data-ttu-id="792e5-120">(選用) 已設定 Configuration Manager Reporting Services 點角色</span><span class="sxs-lookup"><span data-stu-id="792e5-120">(Optional) Configuration Manager Reporting Services Point Role configured</span></span>

## <a name="download-enterprise-site-discovery-tools"></a><span data-ttu-id="792e5-121">下載 Enterprise Site Discovery 工具</span><span class="sxs-lookup"><span data-stu-id="792e5-121">Download Enterprise Site Discovery Tools</span></span>

<span data-ttu-id="792e5-122">下載下列工具：</span><span class="sxs-lookup"><span data-stu-id="792e5-122">Download the following tools:</span></span>

- [<span data-ttu-id="792e5-123">Enterprise Site Discovery 設定和組態套件</span><span class="sxs-lookup"><span data-stu-id="792e5-123">Enterprise Site Discovery Setup and Configuration Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [<span data-ttu-id="792e5-124">Microsoft 報表產生器</span><span class="sxs-lookup"><span data-stu-id="792e5-124">Microsoft Report Builder</span></span>](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a><span data-ttu-id="792e5-125">啟用 Enterprise Site Discovery</span><span class="sxs-lookup"><span data-stu-id="792e5-125">Enable Enterprise Site Discovery</span></span>

<span data-ttu-id="792e5-126">您必須先將 WMI 類別提供者部署到裝置上，才能連線到 Windows Management Instrumentation (WMI) 來取得網站探索資料。</span><span class="sxs-lookup"><span data-stu-id="792e5-126">Before you can connect to Windows Management Instrumentation (WMI) to retrieve site discovery data, you must first deploy the WMI class provider to the device.</span></span>

<span data-ttu-id="792e5-127">從 **Enterprise Site Discovery 設定和組態套件**將內容解壓縮至可用的軟體程式庫檔案共用中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="792e5-127">From the **Enterprise Site Discovery Setup and Configuration Package**, extract the contents to a folder in your definitive software library file share.</span></span> <span data-ttu-id="792e5-128">範例：**\\\\DSL\\EnterpriseSiteDiscovery**。</span><span class="sxs-lookup"><span data-stu-id="792e5-128">Example: **\\\\DSL\\EnterpriseSiteDiscovery**.</span></span>

<span data-ttu-id="792e5-129">接下來，在 Microsoft Endpoint Configuration Manager 中建立套件，如此[文件](/configmgr/apps/deploy-use/packages-and-programs)所述，選取下列選項：</span><span class="sxs-lookup"><span data-stu-id="792e5-129">Next, create a package in Microsoft Endpoint Configuration Manager, as described in the [documentation](/configmgr/apps/deploy-use/packages-and-programs), selecting the following options:</span></span>

- <span data-ttu-id="792e5-130">在 **[套件]** 頁面上，選取 **[名稱]**，並指定名稱 **[啟用網站探索]**</span><span class="sxs-lookup"><span data-stu-id="792e5-130">On the **Package** page, select **Name** and specify the name **Enable Site Discovery**</span></span>
- <span data-ttu-id="792e5-131">在 **[套件]** 頁面上，選取 **[此套件包含來源檔案]**</span><span class="sxs-lookup"><span data-stu-id="792e5-131">On the **Package** page, select **This package contains source files**</span></span>
- <span data-ttu-id="792e5-132">在 **[套件]** 頁面上指定您解壓縮檔案的來源資料夾 (例如，**\\\\DSL\\EnterpriseSiteDiscovery**)</span><span class="sxs-lookup"><span data-stu-id="792e5-132">On the **Package** page, specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**)</span></span>
- <span data-ttu-id="792e5-133">在 **[程式類型]** 頁面上，選擇 **[標準程式]**</span><span class="sxs-lookup"><span data-stu-id="792e5-133">On the **Program Type** page, choose **Standard Program**</span></span>
- <span data-ttu-id="792e5-134">在 **[標準程式]** 頁面上，輸入命令列以設定裝置上的網站探索，如下所示：</span><span class="sxs-lookup"><span data-stu-id="792e5-134">On the **Standard Program** page, enter the command line to configure Site Discovery on the device as follows:</span></span>
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > <span data-ttu-id="792e5-135">指令碼支援為 `-ZoneAllowList` 和 `-SiteAllowList` 使用命令列參數。</span><span class="sxs-lookup"><span data-stu-id="792e5-135">The script supports using command line switches for `-ZoneAllowList` and `-SiteAllowList`.</span></span> <span data-ttu-id="792e5-136">在這個逐步說明中，我們將透過群組原則來設定這些選項 (如下所示)。</span><span class="sxs-lookup"><span data-stu-id="792e5-136">For this step-by-step, we will configure these options via group policy (below).</span></span>
- <span data-ttu-id="792e5-137">在 **[標準程式]** 頁面中，選取選項以執行 **[隱藏]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-137">On the **Standard Program** page, select the option to run **Hidden**.</span></span>
- <span data-ttu-id="792e5-138">在 **[標準程式]** 頁面的 **[程式可執行]** 中，選取選項 **[無論使用者是否登入]**</span><span class="sxs-lookup"><span data-stu-id="792e5-138">On the **Standard Program** page, under **Program can run**, select the option **Whether or not a user is logged in**</span></span>

<span data-ttu-id="792e5-139">建立套件後，按兩下套件名稱 **[啟用網站探索]** 以查看其內容。</span><span class="sxs-lookup"><span data-stu-id="792e5-139">After creating the package, double-click on the package name **Enable Site Discovery** to view its properties.</span></span> <span data-ttu-id="792e5-140">在 **[執行之後]** 屬性中，選取 **[Configuration Manager 重新啟動電腦]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-140">In the **After running** property, select **Configuration manager restarts computer**.</span></span> <span data-ttu-id="792e5-141">裝置重新開機後，WMI 資料收集就會開始。</span><span class="sxs-lookup"><span data-stu-id="792e5-141">WMI data collection will begin after the devices reboot.</span></span>

> [!NOTE]
> <span data-ttu-id="792e5-142">您可以設定使用者必須重新啟動裝置所需的時間，如[用戶端設定文件](/configmgr/core/clients/deploy/about-client-settings#computer-restart)中所述。</span><span class="sxs-lookup"><span data-stu-id="792e5-142">You can configure the amount of time a user has to restart the device as described in the [client settings documentation](/configmgr/core/clients/deploy/about-client-settings#computer-restart).</span></span>

## <a name="configure-enterprise-site-discovery-via-group-policy"></a><span data-ttu-id="792e5-143">使用群組原則設定 Enterprise Site Discovery</span><span class="sxs-lookup"><span data-stu-id="792e5-143">Configure Enterprise Site Discovery via Group Policy</span></span>

<span data-ttu-id="792e5-144">啟用 Enterprise Site Discovery 後，您就可以設定要收集的資料。</span><span class="sxs-lookup"><span data-stu-id="792e5-144">With Enterprise Site Discovery enabled, you can configure what data you'll collect.</span></span> <span data-ttu-id="792e5-145">請考量[此處](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected)所述的當地法律和法規需求。</span><span class="sxs-lookup"><span data-stu-id="792e5-145">Consider local laws and regulatory requirements as described [here](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected).</span></span>

1. <span data-ttu-id="792e5-146">開啟群組原則編輯器</span><span class="sxs-lookup"><span data-stu-id="792e5-146">Open Group Policy Editor</span></span>
2. <span data-ttu-id="792e5-147">按一下**電腦設定** > **系統管理範本** > **Windows 元件** > **Internet Explorer**</span><span class="sxs-lookup"><span data-stu-id="792e5-147">Click **Computer Configuration** > **Administrative Templates** > **Windows Components** > **Internet Explorer**</span></span> 
3. <span data-ttu-id="792e5-148">按兩下 **[開啟網站探索 WMI 輸出]**</span><span class="sxs-lookup"><span data-stu-id="792e5-148">Double-click **Turn on Site Discovery WMI output**</span></span>
4. <span data-ttu-id="792e5-149">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="792e5-149">Select **Enabled**</span></span>
5. <span data-ttu-id="792e5-150">按一下 **[確定]** 或 **[套用]** 儲存此原則設定</span><span class="sxs-lookup"><span data-stu-id="792e5-150">Click **OK** or **Apply** to save this policy setting</span></span>

<span data-ttu-id="792e5-151">您可以限制收集網站資料的區域：</span><span class="sxs-lookup"><span data-stu-id="792e5-151">You can limit the zones in which you collect site data:</span></span>

1. <span data-ttu-id="792e5-152">按兩下 **[由區域限制網站探索輸出]**</span><span class="sxs-lookup"><span data-stu-id="792e5-152">Double-click **Limit Site Discovery output by Zone**</span></span>
2. <span data-ttu-id="792e5-153">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="792e5-153">Select **Enabled**</span></span>
3. <span data-ttu-id="792e5-154">輸入位元遮罩，以指示要啟用網站探索的區域：</span><span class="sxs-lookup"><span data-stu-id="792e5-154">Enter a bitmask indicating which zones to enable site discover for:</span></span>
    1. <span data-ttu-id="792e5-155">受限制的網站區域</span><span class="sxs-lookup"><span data-stu-id="792e5-155">Restricted Sites zone</span></span>
    2. <span data-ttu-id="792e5-156">網際網路區域</span><span class="sxs-lookup"><span data-stu-id="792e5-156">Internet zone</span></span>
    3. <span data-ttu-id="792e5-157">信任的網站區域</span><span class="sxs-lookup"><span data-stu-id="792e5-157">Trusted Sites zone</span></span>
    4. <span data-ttu-id="792e5-158">近端內部網路區域</span><span class="sxs-lookup"><span data-stu-id="792e5-158">Local Intranet zone</span></span>
    5. <span data-ttu-id="792e5-159">本機電腦區域</span><span class="sxs-lookup"><span data-stu-id="792e5-159">Local Machine zone</span></span>
    
    <span data-ttu-id="792e5-160">範例 1：**00010** 只會收集近端內部網路區域的資料</span><span class="sxs-lookup"><span data-stu-id="792e5-160">Example 1: **00010** will collect data only for the Local Intranet zone</span></span>

    <span data-ttu-id="792e5-161">範例 2：**10111** 會收集除了網際網路區域以外的所有區域的資料</span><span class="sxs-lookup"><span data-stu-id="792e5-161">Example 2: **10111** will collect data for all zones except the Internet zone</span></span>
4. <span data-ttu-id="792e5-162">按一下 **[確定]** 或 **[套用]** 儲存此原則設定</span><span class="sxs-lookup"><span data-stu-id="792e5-162">Click **OK** or **Apply** to save this policy setting</span></span>

<span data-ttu-id="792e5-163">您可以限制收集網站資料的網域：</span><span class="sxs-lookup"><span data-stu-id="792e5-163">You can limit the domains for which you collect site data:</span></span>

1. <span data-ttu-id="792e5-164">按兩下 **[由網域限制網站探索輸出]**</span><span class="sxs-lookup"><span data-stu-id="792e5-164">Double-click **Limit Site Discovery output by domain**</span></span>
2. <span data-ttu-id="792e5-165">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="792e5-165">Select **Enabled**</span></span>
3. <span data-ttu-id="792e5-166">輸入您要收集資料的網域，每行一個網域</span><span class="sxs-lookup"><span data-stu-id="792e5-166">Enter the domains you want to collect data for, one domain per line</span></span>
4. <span data-ttu-id="792e5-167">按一下 **[確定]** 或 **[套用]** 儲存此原則設定</span><span class="sxs-lookup"><span data-stu-id="792e5-167">Click **OK** or **Apply** to save this policy setting</span></span>

## <a name="collect-site-discovery-data-using-configuration-manager"></a><span data-ttu-id="792e5-168">使用 Configuration Manager 收集網站探索資料</span><span class="sxs-lookup"><span data-stu-id="792e5-168">Collect Site Discovery data using Configuration Manager</span></span>

<span data-ttu-id="792e5-169">現在，您的裝置正在產生資料，是時候在 Configuration Manager 中收集這些資料了。</span><span class="sxs-lookup"><span data-stu-id="792e5-169">Now that your devices are generating data, it's time to collect this data in Configuration Manager.</span></span>

1. <span data-ttu-id="792e5-170">在 Configuration Manager 主控台中，選擇 **[管理]** > **[用戶端設定]** > **[預設用戶端設定]**</span><span class="sxs-lookup"><span data-stu-id="792e5-170">In the Configuration Manager console, choose **Administration** > **Client Settings** > **Default Client Settings**</span></span>
2. <span data-ttu-id="792e5-171">在 **[首頁]** 索引標籤的 **[內容]** 群組中，選擇 **[內容]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-171">On the **Home** tab, in the **Properties** group, choose **Properties**</span></span>
3. <span data-ttu-id="792e5-172">在 **[預設用戶端設定]** 對話方塊中，選擇 **[硬體清查]**</span><span class="sxs-lookup"><span data-stu-id="792e5-172">In the **Default Client Settings** dialog box, choose **Hardware Inventory**</span></span>
4. <span data-ttu-id="792e5-173">在 **[裝置設定]** 清單中，選擇 **[設定類別]**</span><span class="sxs-lookup"><span data-stu-id="792e5-173">In the **Device Settings** list, choose **Set Classes**</span></span>
5. <span data-ttu-id="792e5-174">在 **[硬體清查類別]** 對話方塊中，選擇 **[新增]**</span><span class="sxs-lookup"><span data-stu-id="792e5-174">In the **Hardware Inventory Classes** dialog box, choose **Add**</span></span>
6. <span data-ttu-id="792e5-175">在 **[新增硬體清查類別]** 對話方塊中，按一下 **[連線]**</span><span class="sxs-lookup"><span data-stu-id="792e5-175">In the **Add Hardware Inventory Class** dialog box, click **Connect**</span></span>
7. <span data-ttu-id="792e5-176">在 **[連線到 Windows Management Instrumentation (WMI)]** 對話方塊中，輸入設定 Enterprise Site Discovery 的電腦名稱。</span><span class="sxs-lookup"><span data-stu-id="792e5-176">In the **Connect to Windows Management Instrumentation (WMI)** dialog box, enter the name of a computer where Enterprise Site Discovery is configured.</span></span> <span data-ttu-id="792e5-177">如果您要連線到另一部電腦，您需要具備存取 WMI 權限的認證。</span><span class="sxs-lookup"><span data-stu-id="792e5-177">If you're connecting to another computer, you'll need credentials with permission to access WMI.</span></span>
8. <span data-ttu-id="792e5-178">在 **[WMI 命名空間]** 文字方塊中，輸入 **root\cimv2\IETelemetry**</span><span class="sxs-lookup"><span data-stu-id="792e5-178">In the **WMI Namespace** text box, enter **root\cimv2\IETelemetry**</span></span>
9. <span data-ttu-id="792e5-179">選擇 **[連線]**</span><span class="sxs-lookup"><span data-stu-id="792e5-179">Choose **Connect**</span></span>
10. <span data-ttu-id="792e5-180">在 **[新增硬體清查類別]** 對話方塊的 **[清查類別]** 清單中，選取 WMI 類別**IESystemINfo**、**IEUrlInfo**、和 \**IECountInfo*。</span><span class="sxs-lookup"><span data-stu-id="792e5-180">In the **Add Hardware Inventory Class** dialog box, in the **Inventory classes** list, select the WMI classes **IESystemINfo**, **IEUrlInfo**, and \**IECountInfo*.</span></span>
11. <span data-ttu-id="792e5-181">按一下 **[確定]** 以關閉 **[類別限定詞]** 對話方塊及其他開啟的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="792e5-181">Click **OK** to close the **Class qualifiers** dialog box and the other open dialogs.</span></span>

<span data-ttu-id="792e5-182">用戶端更新管理點中的設定後，系統會在下次硬體清查執行時 (預設為每七天) 報告資料。</span><span class="sxs-lookup"><span data-stu-id="792e5-182">After the client updates settings from the management point, data will be reported when the next hardware inventory runs (by default every seven days).</span></span>

## <a name="import-site-discovery-reports"></a><span data-ttu-id="792e5-183">匯入網站探索報表</span><span class="sxs-lookup"><span data-stu-id="792e5-183">Import Site Discovery reports</span></span>

<span data-ttu-id="792e5-184">Enterprise Site Discovery 套件包含兩個範例報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-184">The Enterprise Site Discovery package includes two sample reports.</span></span> <span data-ttu-id="792e5-185">一個報表使用 ActiveX 控制項顯示網站，另一個報表使用舊版文件模式顯示網站。</span><span class="sxs-lookup"><span data-stu-id="792e5-185">One report shows sites using ActiveX controls, and another shows sites using legacy document modes.</span></span>

### <a name="configure-the-site-discovery-sample-report"></a><span data-ttu-id="792e5-186">設定網站探索範例報表</span><span class="sxs-lookup"><span data-stu-id="792e5-186">Configure the Site Discovery sample report</span></span>

<span data-ttu-id="792e5-187">使用下列程序建立使用三個資料來源的範例報表：使用者造訪的網站、其系統相關資訊，以及網站所使用的文件模式。</span><span class="sxs-lookup"><span data-stu-id="792e5-187">Use the following procedure to create a sample report that uses three data sources: the sites a user visits, information about their system, and the document modes used by the sites.</span></span> <span data-ttu-id="792e5-188">此報表可協助您識別可能依靠舊版文件模式的網站。</span><span class="sxs-lookup"><span data-stu-id="792e5-188">This report helps you identify sites that may depend on legacy document modes.</span></span>

1. <span data-ttu-id="792e5-189">將報表 **SCCM_Report-Site_Discovery.rdl** 複製到 Configuration Manager 伺服器。</span><span class="sxs-lookup"><span data-stu-id="792e5-189">Copy the report **SCCM_Report-Site_Discovery.rdl** to your Configuration Manager server.</span></span>
2. <span data-ttu-id="792e5-190">安裝 [Microsoft 報表產生器](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15)。</span><span class="sxs-lookup"><span data-stu-id="792e5-190">Install [Microsoft Report Builder](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).</span></span>
3. <span data-ttu-id="792e5-191">按兩下 **SCCM_Report-Site_Discovery.rdl** 以在報表產生器中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-191">Double-click **SCCM_Report-Site_Discovery.rdl** to open the report in Report Builder.</span></span>
4. <span data-ttu-id="792e5-192">第一次嘗試開啟報表時，它會嘗試與建立該報表的伺服器聯繫。</span><span class="sxs-lookup"><span data-stu-id="792e5-192">The first time you try to open the report, it will try to contact the server where it was created.</span></span> <span data-ttu-id="792e5-193">當系統提示您**連接到報表伺服器**時，請按一下 **[否]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-193">When prompted to **Connect to Report Server**, click **No**.</span></span>
5. <span data-ttu-id="792e5-194">報表開啟後，展開 **[資料來源]**，然後按兩下 **[DataSource1]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-194">After the report opens, expand **Data Sources** and double-click **DataSource1**.</span></span>
6. <span data-ttu-id="792e5-195">在 **[資料來源屬性]** 視窗中，選取 **[使用內嵌在我的報表中的連線]**，然後按一下 **[建置...]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="792e5-195">In the **Data Source Properties** window, select **Use a connection embedded in my report** and then click the **Build...** button.</span></span>
7. <span data-ttu-id="792e5-196">在 **[連線內容]** 視窗中，選取 **[伺服器名稱]**，然後輸入 Configuration Manager 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="792e5-196">In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server.</span></span> <span data-ttu-id="792e5-197">然後，在 **[選取或輸入資料庫名稱]** 中，從下拉式清單中選取 Configuration Manager 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="792e5-197">Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.</span></span>
8. <span data-ttu-id="792e5-198">按一下 **[確定]** 關閉 **[連線內容]** 視窗。</span><span class="sxs-lookup"><span data-stu-id="792e5-198">Click **OK** to close the **Connection Properties** window.</span></span>
9. <span data-ttu-id="792e5-199">按一下 **[測試連線]** 以測試連線。</span><span class="sxs-lookup"><span data-stu-id="792e5-199">Click **Test Connection** to test the connection.</span></span> <span data-ttu-id="792e5-200">如果連線成功，請按一下 **[確定]** 關閉 **[資料來源屬性]** 視窗。</span><span class="sxs-lookup"><span data-stu-id="792e5-200">If the connection is successful, click **OK** to close the **Data Source Properties** window.</span></span>
10. <span data-ttu-id="792e5-201">在 **[資料來源 2]** 重複執行步驟 5 到 9。</span><span class="sxs-lookup"><span data-stu-id="792e5-201">Repeat Steps 5 through 9 for **Data Source 2**.</span></span>
11. <span data-ttu-id="792e5-202">展開 **[資料集]**，然後按兩下 **[DataSet1]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-202">Expand **Datasets** and double-click **DataSet1**.</span></span>
12. <span data-ttu-id="792e5-203">在 **[資料集屬性]** 視窗中，按一下 **[查詢:]** 文字方塊，然後使用您在步驟 7 中選取的資料庫名稱來取代 **CM_A1B**。</span><span class="sxs-lookup"><span data-stu-id="792e5-203">In the **Dataset Properties** window, click in the **Query:** textbox and replace **USE CM_A1B** with the database name you selected in Step 7.</span></span>
13. <span data-ttu-id="792e5-204">在 **DataSet2**、**DataSet3**和 **DataSet4**重複步驟 11 到 12。</span><span class="sxs-lookup"><span data-stu-id="792e5-204">Repeat steps 11 through 12 for **DataSet2**, **DataSet3**, and **DataSet4**.</span></span>
14. <span data-ttu-id="792e5-205">在功能區的 **[首頁]** 索引標籤中，按一下 **[執行]** 按鈕來測試報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-205">In the **Home** tab of the ribbon, click the **Run** button to test the report.</span></span>
15. <span data-ttu-id="792e5-206">儲存報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-206">Save the report.</span></span>
16. <span data-ttu-id="792e5-207">關閉 Microsoft 報表產生器。</span><span class="sxs-lookup"><span data-stu-id="792e5-207">Close Microsoft Report Builder.</span></span>
17. <span data-ttu-id="792e5-208">將檔案重新命名為 **Site Discovery.rdl**</span><span class="sxs-lookup"><span data-stu-id="792e5-208">Rename the file to **Site Discovery.rdl**</span></span>

### <a name="configure-the-activex-sample-report"></a><span data-ttu-id="792e5-209">設定 ActiveX 範例報告</span><span class="sxs-lookup"><span data-stu-id="792e5-209">Configure the ActiveX sample report</span></span>

<span data-ttu-id="792e5-210">使用下列程序建立使用單一資料來源的範例報告：使用 ActiveX 控制項的網站。</span><span class="sxs-lookup"><span data-stu-id="792e5-210">Use the following procedure to create a sample report that uses one data source: the sites that are using ActiveX controls.</span></span> <span data-ttu-id="792e5-211">由於 Internet Explorer 是唯一支援 ActiveX 控制項的瀏覽器，因此這些網站可能需要 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="792e5-211">Since Internet Explorer is the only browser that support ActiveX controls, these sites may require IE mode.</span></span>

1. <span data-ttu-id="792e5-212">將報表 **SCCM Report Sample - ActiveX.rdl** 複製到 Configuration Manager 伺服器。</span><span class="sxs-lookup"><span data-stu-id="792e5-212">Copy the report **SCCM Report Sample - ActiveX.rdl** to your Configuration Manager server.</span></span>
2. <span data-ttu-id="792e5-213">安裝 [Microsoft 報表產生器](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15)。</span><span class="sxs-lookup"><span data-stu-id="792e5-213">Install [Microsoft Report Builder](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15).</span></span>
3. <span data-ttu-id="792e5-214">按兩下 **SCCM Report Sample - ActiveX.rdl** 以在報表產生器中開啟報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-214">Double-click **SCCM Report Sample - ActiveX.rdl** to open the report in Report Builder.</span></span>
4. <span data-ttu-id="792e5-215">第一次嘗試開啟報表時，它會嘗試與建立該報表的伺服器聯繫。</span><span class="sxs-lookup"><span data-stu-id="792e5-215">The first time you try to open the report, it will try to contact the server where it was created.</span></span> <span data-ttu-id="792e5-216">當系統提示您**連接到報表伺服器**時，請按一下 **[否]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-216">When prompted to **Connect to Report Server**, click **No**.</span></span>
5. <span data-ttu-id="792e5-217">報表開啟後，展開 **[資料來源]**，然後按兩下 **[AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-217">After the report opens, expand **Data Sources** and double-click **AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_**.</span></span>
6. <span data-ttu-id="792e5-218">在 **[資料來源屬性]** 視窗中，選取 **[使用內嵌在我的報表中的連線]**，然後按一下 **[建置...]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="792e5-218">In the **Data Source Properties** window, select **Use a connection embedded in my report** and then click the **Build...** button.</span></span>
7. <span data-ttu-id="792e5-219">在 **[連線內容]** 視窗中，選取 **[伺服器名稱]**，然後輸入 Configuration Manager 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="792e5-219">In the **Connection Properties** window, select **Server Name** and enter the name of the Configuration Manager server.</span></span> <span data-ttu-id="792e5-220">然後，在 **[選取或輸入資料庫名稱]** 中，從下拉式清單中選取 Configuration Manager 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="792e5-220">Then, in **Select or enter a database name** select the name of the Configuration Manager database from the dropdown list.</span></span>
8. <span data-ttu-id="792e5-221">按一下 **[確定]** 關閉 **[連線內容]** 視窗。</span><span class="sxs-lookup"><span data-stu-id="792e5-221">Click **OK** to close the **Connection Properties** window.</span></span>
9. <span data-ttu-id="792e5-222">按一下 **[測試連線]** 以測試連線。</span><span class="sxs-lookup"><span data-stu-id="792e5-222">Click **Test Connection** to test the connection.</span></span> <span data-ttu-id="792e5-223">如果連線成功，請按一下 **[確定]** 關閉 **[資料來源屬性]** 視窗。</span><span class="sxs-lookup"><span data-stu-id="792e5-223">If the connection is successful, click **OK** to close the **Data Source Properties** window.</span></span>
10. <span data-ttu-id="792e5-224">展開 **[資料集]**，然後按兩下 **[DataSet1]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-224">Expand **Datasets** and double-click **DataSet1**.</span></span>
11. <span data-ttu-id="792e5-225">在 **[資料集屬性]** 視窗中，按一下 **[查詢:]** 文字方塊，然後使用您在步驟 7 中選取的資料庫名稱來取代 **CM_A1B**。</span><span class="sxs-lookup"><span data-stu-id="792e5-225">In the **Dataset Properties** window, click in the **Query:** textbox and replace **USE CM_A1B** with the database name you selected in Step 7.</span></span>
12. <span data-ttu-id="792e5-226">在功能區的 **[首頁]** 索引標籤中，按一下 **[執行]** 按鈕來測試報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-226">In the **Home** tab of the ribbon, click the **Run** button to test the report.</span></span>
13. <span data-ttu-id="792e5-227">儲存報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-227">Save the report.</span></span>
14. <span data-ttu-id="792e5-228">關閉 Microsoft 報表產生器。</span><span class="sxs-lookup"><span data-stu-id="792e5-228">Close Microsoft Report Builder.</span></span>
15. <span data-ttu-id="792e5-229">將檔案重新命名為 **ActiveX**</span><span class="sxs-lookup"><span data-stu-id="792e5-229">Rename the file to **ActiveX**</span></span>

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a><span data-ttu-id="792e5-230">將已設定的報表上傳到 Microsoft SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="792e5-230">Upload configured reports to Microsoft SQL Server Reporting Services</span></span>

<span data-ttu-id="792e5-231">設定好環境報表後，將報表上傳到報表伺服器。</span><span class="sxs-lookup"><span data-stu-id="792e5-231">After you've configured the reports for your environment, upload them to the reporting server.</span></span>

1. <span data-ttu-id="792e5-232">啟動 **Reporting Services 組態管理員**應用程式。</span><span class="sxs-lookup"><span data-stu-id="792e5-232">Launch the **Reporting Services Configuration Manager** application.</span></span>
2. <span data-ttu-id="792e5-233">在 **[報表伺服器連線]** 視窗中，按一下 **[連線]**，然後按一下 **[Web 入口網站身分識別]** 底下所列的 URL</span><span class="sxs-lookup"><span data-stu-id="792e5-233">In the **Report Server Connection** window, click **Connect** and then click on the URL listed under **Web Portal Site Identification**</span></span>
3. <span data-ttu-id="792e5-234">在開啟的瀏覽器視窗中，您應該位於 **SQL Server Reporting Services 頁面** - 按一下 SCCM 網站程式碼的 **ConfigMgr_SCCMSiteCode** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="792e5-234">In the browser window that opens, you should be on the **SQL Server Reporting Services Page** - click the **ConfigMgr_SCCMSiteCode** folder for your SCCM Site Code.</span></span>
4. <span data-ttu-id="792e5-235">在功能區中，將游標停留在 **[+新增]**，然後按一下 **[資料夾]** 功能表項目。</span><span class="sxs-lookup"><span data-stu-id="792e5-235">In the ribbon, hover over **+New** and click the **Folder** menu item.</span></span>
5. <span data-ttu-id="792e5-236">輸入資料夾名稱，例如 **Enterprise Site Discovery**，然後按一下 **[建立]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="792e5-236">Enter a folder name, such as **Enterprise Site Discovery**, and then click the **Create** button.</span></span>
6. <span data-ttu-id="792e5-237">按一下 **Enterprise Site Discovery** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="792e5-237">Click on the **Enterprise Site Discovery** folder.</span></span>
7. <span data-ttu-id="792e5-238">在功能區中，按一下 **[上傳]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="792e5-238">In the ribbon, click the **Upload** button.</span></span>
8. <span data-ttu-id="792e5-239">選取 **[網站探索]** 報表，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="792e5-239">Select the **Site Discovery** report, and click **OK**.</span></span>
9. <span data-ttu-id="792e5-240">在 **ActiveX** 報表重複步驟 7 與 8。</span><span class="sxs-lookup"><span data-stu-id="792e5-240">Repeat steps 7 and 8 for the **ActiveX** report.</span></span>

### <a name="view-reports-in-configuration-manager"></a><span data-ttu-id="792e5-241">檢視 Configuration Manager 中的報表</span><span class="sxs-lookup"><span data-stu-id="792e5-241">View reports in Configuration Manager</span></span>

<span data-ttu-id="792e5-242">現在您已自訂並上傳報表，您可以在 Configuration Manager 中檢視報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-242">Now that you've customized and uploaded the reports, you can view them in Configuration Manager.</span></span>

1. <span data-ttu-id="792e5-243">在 Configuration Manager 主控台中，選擇 **[監視]** > **[報表]** > **[報表]** > **[Enterprise Site Discovery]**</span><span class="sxs-lookup"><span data-stu-id="792e5-243">In the Configuration Manager console, choose **Monitoring** > **Reporting** > **Reports** > **Enterprise Site Discovery**</span></span>
2. <span data-ttu-id="792e5-244">按兩下報表以檢視報表。</span><span class="sxs-lookup"><span data-stu-id="792e5-244">Double-click on a report to view it.</span></span>

## <a name="disable-enterprise-site-discovery"></a><span data-ttu-id="792e5-245">停用 Enterprise Site Discovery</span><span class="sxs-lookup"><span data-stu-id="792e5-245">Disable Enterprise Site Discovery</span></span>

<span data-ttu-id="792e5-246">資料收集完畢後，您應停用 Enterprise Site Discovery。</span><span class="sxs-lookup"><span data-stu-id="792e5-246">When you're finished collecting data, you should disable Enterprise Site Discovery.</span></span> <span data-ttu-id="792e5-247">建立第二個套件來停用 Microsoft Endpoint Configuration Manager 中的 Enterprise Site Discovery，如此[文件](/configmgr/apps/deploy-use/packages-and-programs)所述，選取下列選項：</span><span class="sxs-lookup"><span data-stu-id="792e5-247">Create a second package to disable Enterprise Site Discovery in Microsoft Endpoint Configuration Manager, as described in the [documentation](/configmgr/apps/deploy-use/packages-and-programs), selecting the following options:</span></span>

- <span data-ttu-id="792e5-248">在 **[套件]** 頁面上，選取 **[名稱]**，並指定名稱 **[停用網站探索]**</span><span class="sxs-lookup"><span data-stu-id="792e5-248">On the **Package** page, select **Name** and specify the name **Disable Site Discovery**</span></span>
- <span data-ttu-id="792e5-249">在 **[套件]** 頁面上，選取 **[此套件包含來源檔案]**</span><span class="sxs-lookup"><span data-stu-id="792e5-249">On the **Package** page, select **This package contains source files**</span></span>
- <span data-ttu-id="792e5-250">在 **[套件]** 頁面上指定您解壓縮檔案的來源資料夾 (例如，**\\\\DSL\\EnterpriseSiteDiscovery**)</span><span class="sxs-lookup"><span data-stu-id="792e5-250">On the **Package** page, specify the source folder you extracted the files to (for example, **\\\\DSL\\EnterpriseSiteDiscovery**)</span></span>
- <span data-ttu-id="792e5-251">在 **[程式類型]** 頁面上，選擇 **[標準程式]**</span><span class="sxs-lookup"><span data-stu-id="792e5-251">On the **Program Type** page, choose **Standard Program**</span></span>
- <span data-ttu-id="792e5-252">在 **[標準程式]** 頁面上，輸入停用裝置上的網站探索的命令列，如下所示：</span><span class="sxs-lookup"><span data-stu-id="792e5-252">On the **Standard Program** page, enter the command line that will disable Site Discovery on the device as follows:</span></span>
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- <span data-ttu-id="792e5-253">在 **[標準程式]** 頁面中，選取選項以執行 **[隱藏]**</span><span class="sxs-lookup"><span data-stu-id="792e5-253">On the **Standard Program** page, select the option to run **Hidden**</span></span>
- <span data-ttu-id="792e5-254">在 **[標準程式]** 頁面的 **[程式可執行]** 中，選取選項 **[無論使用者是否登入]**</span><span class="sxs-lookup"><span data-stu-id="792e5-254">On the **Standard Program** page, under **Program can run**, select the option **Whether or not a user is logged in**</span></span>

## <a name="see-also"></a><span data-ttu-id="792e5-255">請參閱</span><span class="sxs-lookup"><span data-stu-id="792e5-255">See also</span></span>

- [<span data-ttu-id="792e5-256">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="792e5-256">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="792e5-257">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="792e5-257">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="792e5-258">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="792e5-258">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="792e5-259">其他 Enterprise Site Discovery 資訊</span><span class="sxs-lookup"><span data-stu-id="792e5-259">Additional Enterprise Site Discovery information</span></span>](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)