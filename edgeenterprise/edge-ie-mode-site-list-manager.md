---
title: 'Microsoft Edge 中的 Enterprise Site List Manager  '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: '在 Microsoft Edge 中啟用和使用 Enterprise Site List Manager  '
ms.openlocfilehash: add635a17d05cb4be94e710fd99ab480b992a579
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641419"
---
# <a name="enterprise-site-list-manager-in-microsoft-edge"></a><span data-ttu-id="03b54-103">Microsoft Edge 中的 Enterprise Site List Manager</span><span class="sxs-lookup"><span data-stu-id="03b54-103">Enterprise Site List Manager in Microsoft Edge</span></span>

>[!Note]
> <span data-ttu-id="03b54-104">Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。</span><span class="sxs-lookup"><span data-stu-id="03b54-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="03b54-105">您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="03b54-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="03b54-106">[從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。</span><span class="sxs-lookup"><span data-stu-id="03b54-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="03b54-107">本文說明如何在 Microsoft Edge 中啟用存取和使用 Enterprise Site List Manager ，以建立、編輯及匯出 Internet Explorer 模式的企業網站清單。</span><span class="sxs-lookup"><span data-stu-id="03b54-107">This article explains how to enable access to and use the Enterprise Site List Manager in Microsoft Edge to create, edit and export your Enterprise Mode Site List for Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="03b54-108">本文適用於 Microsoft Edge 版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="03b54-108">This article applies to Microsoft Edge version 89 or later.</span></span> 

## <a name="overview"></a><span data-ttu-id="03b54-109">概觀</span><span class="sxs-lookup"><span data-stu-id="03b54-109">Overview</span></span>

<span data-ttu-id="03b54-110">Enterprise Site List Manager 是[獨立企業模式網站清單管理器工具](https://www.microsoft.com/download/details.aspx?id=49974)的瀏覽器內版本，用於建立、編輯和匯出組織的網站清單。</span><span class="sxs-lookup"><span data-stu-id="03b54-110">The Enterprise Site List Manager is an in-browser version of the [standalone Enterprise Mode Site List Manager tool](https://www.microsoft.com/download/details.aspx?id=49974) that lets you create, edit, and export your organization’s site list.</span></span>

<span data-ttu-id="03b54-111">未來將透過 Microsoft Edge 中的 Enterprise Site List Manager 提供對 Internet Explorer 模式工具的改良功能。</span><span class="sxs-lookup"><span data-stu-id="03b54-111">Future improvements to the tool for Internet Explorer mode will be available through Enterprise Site List Manager in Microsoft Edge.</span></span> <span data-ttu-id="03b54-112">獨立工具將繼續在下載中心提供，但不會得到任何功能更新。</span><span class="sxs-lookup"><span data-stu-id="03b54-112">The standalone tool will continue to be available in the Download Center but won't get any feature updates.</span></span>

## <a name="enabling-access-to-enterprise-site-list-manager"></a><span data-ttu-id="03b54-113">啟用對 Enterprise Site List Manager 的存取</span><span class="sxs-lookup"><span data-stu-id="03b54-113">Enabling access to Enterprise Site List Manager</span></span>

<span data-ttu-id="03b54-114">您可以使用 [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) 群組原則來設定工具存取權。</span><span class="sxs-lookup"><span data-stu-id="03b54-114">You can configure access to the tool by using the [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) group policy.</span></span>

<span data-ttu-id="03b54-115">如果啟用，您的使用者將在 *edge://compat* 中的左側瀏覽窗格中看到名為「Enterprise Site List Manager」的選項。</span><span class="sxs-lookup"><span data-stu-id="03b54-115">If enabled, your users will see an option named Enterprise Site List Manager on the left navigation pane in *edge://compat*.</span></span> <span data-ttu-id="03b54-116">如果停用，使用者將不會在左側瀏覽窗格中看到 Enterprise Site List Manager 的進入點。</span><span class="sxs-lookup"><span data-stu-id="03b54-116">If disabled, users will not see the entry point to Enterprise Site List Manager in the left navigation pane.</span></span> <span data-ttu-id="03b54-117">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="03b54-117">This is the default behavior.</span></span>

## <a name="using-the-enterprise-site-list-manager"></a><span data-ttu-id="03b54-118">使用 Enterprise Site List Manager</span><span class="sxs-lookup"><span data-stu-id="03b54-118">Using the Enterprise Site List Manager</span></span>

<span data-ttu-id="03b54-119">Enterprise Site List Manager 工具使用 v.2 版的結構描述。</span><span class="sxs-lookup"><span data-stu-id="03b54-119">The Enterprise Site List Manager tool uses the v.2 version of the schema.</span></span> <span data-ttu-id="03b54-120">如果您將 v.1 版的結構描述匯入 Enterprise Site List Manager (結構描述 v.2)，它會將 XML 儲存為 v.2 版的結構描述。</span><span class="sxs-lookup"><span data-stu-id="03b54-120">If you import a v.1 version schema into the Enterprise Site List Manager (schema v.2), the XML is saved into the v.2 version of the schema.</span></span> <span data-ttu-id="03b54-121">請參閲[企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="03b54-121">See [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

### <a name="add-single-sites-to-your-site-list"></a><span data-ttu-id="03b54-122">新增單一站台至您的網站清單</span><span class="sxs-lookup"><span data-stu-id="03b54-122">Add single sites to your site list</span></span>  

<span data-ttu-id="03b54-123">使用下列步驟將個別網站新增到您的網站清單中。</span><span class="sxs-lookup"><span data-stu-id="03b54-123">Use the following steps to add individual sites to your site list.</span></span>

> [!NOTE]
> <span data-ttu-id="03b54-124">您只能新增特定 URL，而非網際網路或內部網路區域。</span><span class="sxs-lookup"><span data-stu-id="03b54-124">You can only add specific URLs, not Internet or Intranet Zones.</span></span>

1. <span data-ttu-id="03b54-125">在 Enterprise Site List Manager 中，按一下  **[新增網站]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-125">In the Enterprise Site List Manager, click **Add a site**.</span></span>
2. <span data-ttu-id="03b54-126">在 URL 方塊中輸入要新增之網站的 URL，例如  <domain>.com 或  <domain>.com/<path> 。</span><span class="sxs-lookup"><span data-stu-id="03b54-126">Type the URL for the website you’d like to add, for example: <domain>.com or <domain>.com/<path> in the URL box.</span></span>
3. <span data-ttu-id="03b54-127">從 **[開啟位置]**  清單中選取以下選項之一：</span><span class="sxs-lookup"><span data-stu-id="03b54-127">Select one of the following options from the **Open in** list:</span></span>

   - <span data-ttu-id="03b54-128">**IE11**。</span><span class="sxs-lookup"><span data-stu-id="03b54-128">**IE11**.</span></span> <span data-ttu-id="03b54-129">在 IE11 應用程式中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-129">Opens the site in the IE11 application.</span></span>
   - <span data-ttu-id="03b54-130">**IE 模式**。</span><span class="sxs-lookup"><span data-stu-id="03b54-130">**IE mode**.</span></span> <span data-ttu-id="03b54-131">在 Microsoft Edge 上以 Internet Explorer 模式開啟網站 (如已啟用)，否則在 IE11 應用程式中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-131">Opens the site in Internet Explorer mode on Microsoft Edge if enabled and in the IE11 app otherwise.</span></span> <span data-ttu-id="03b54-132">請參閱 [Microsoft Edge 上的 Internet Explorer 模式](./edge-ie-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="03b54-132">See [Internet Explorer mode on Microsoft Edge](./edge-ie-mode.md).</span></span>
   - <span data-ttu-id="03b54-133">**MSEdge**。</span><span class="sxs-lookup"><span data-stu-id="03b54-133">**MSEdge**.</span></span> <span data-ttu-id="03b54-134">在 Microsoft Edge 中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-134">Opens the site in Microsoft Edge.</span></span>
   - <span data-ttu-id="03b54-135">**可設定**。</span><span class="sxs-lookup"><span data-stu-id="03b54-135">**Configurable**.</span></span> <span data-ttu-id="03b54-136">允許網站參與 IE 模式引擎判斷。</span><span class="sxs-lookup"><span data-stu-id="03b54-136">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="03b54-137">請參閲[IE 模式中可設定的網站](./edge-learnmore-configurable-sites-ie-mode.md)</span><span class="sxs-lookup"><span data-stu-id="03b54-137">See [Configurable sites in IE mode](./edge-learnmore-configurable-sites-ie-mode.md)</span></span>
   - <span data-ttu-id="03b54-138">**無**。</span><span class="sxs-lookup"><span data-stu-id="03b54-138">**None**.</span></span> <span data-ttu-id="03b54-139">在使用者選擇的任何瀏覽器中開啟。</span><span class="sxs-lookup"><span data-stu-id="03b54-139">Opens in whatever browser the user chooses.</span></span>  

4. <span data-ttu-id="03b54-140">在  **[相容模式下]**，選擇下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="03b54-140">Under **Compat Mode**, choose one of the following options:</span></span>

   - <span data-ttu-id="03b54-141">**IE8Enterprise**。</span><span class="sxs-lookup"><span data-stu-id="03b54-141">**IE8Enterprise**.</span></span> <span data-ttu-id="03b54-142">在 IE8 企業模式中載入網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-142">Loads the site in IE8 Enterprise Mode.</span></span>
   - <span data-ttu-id="03b54-143">**IE7Enterprise**。</span><span class="sxs-lookup"><span data-stu-id="03b54-143">**IE7Enterprise**.</span></span> <span data-ttu-id="03b54-144">在 IE7 企業模式載入網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-144">Loads the site in IE7 Enterprise Mode.</span></span>
   - <span data-ttu-id="03b54-145">**IE[x]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-145">**IE[x]**.</span></span> <span data-ttu-id="03b54-146">[x] 是文件模式的數目，而網站會以指定的文件模式載入。</span><span class="sxs-lookup"><span data-stu-id="03b54-146">Where [x] is the document mode number and the site loads in the specified document mode.</span></span>
   - <span data-ttu-id="03b54-147">**預設模式**。</span><span class="sxs-lookup"><span data-stu-id="03b54-147">**Default Mode**.</span></span> <span data-ttu-id="03b54-148">使用頁面的預設相容性模式載入網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-148">Loads the site using the default compatibility mode for the page.</span></span>

   <span data-ttu-id="03b54-149">網域內的路徑可能需要不同於網域本身的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="03b54-149">The path within a domain can require a different compatibility mode from the domain itself.</span></span> <span data-ttu-id="03b54-150">例如，網域在預設的 IE11 瀏覽器中可能一切正常，但路徑可能會有問題，而需要使用企業模式。</span><span class="sxs-lookup"><span data-stu-id="03b54-150">For example, the domain might look fine in the default IE11 browser, but the path might have problems and require the use of Enterprise Mode.</span></span> <span data-ttu-id="03b54-151">如果您先前已新增網域，則仍會選取您原本選擇的相容性。</span><span class="sxs-lookup"><span data-stu-id="03b54-151">If you added the domain previously, your original compatibility choice is still selected.</span></span> <span data-ttu-id="03b54-152">不過，如果網域是新的，則會自動選取  **[IE8 企業模式]** 。</span><span class="sxs-lookup"><span data-stu-id="03b54-152">However, if the domain is new, **IE8 Enterprise Mode** is automatically selected.</span></span>

   <span data-ttu-id="03b54-153">企業模式的優先順序高於文件模式，因此已經在企業模式網站清單中的網站不會受此更新影響，而會如往常一樣以企業模式載入。</span><span class="sxs-lookup"><span data-stu-id="03b54-153">Enterprise Mode takes precedence over document modes, so sites that are already included in the Enterprise Mode site list won’t be affected by this update and will continue to load in Enterprise Mode, as usual.</span></span> <span data-ttu-id="03b54-154">如需使用文件模式的進一步詳細資訊，請參閱 [使用文件模式和企業模式網站清單修正網頁相容性問題](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list)。</span><span class="sxs-lookup"><span data-stu-id="03b54-154">For more specific information about using document modes, see [Fix web compatibility issues using document modes and the Enterprise Mode site list](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).</span></span>

5. <span data-ttu-id="03b54-155">**[允許重新導向]** 核取方塊適用于處理伺服器端重新導向。</span><span class="sxs-lookup"><span data-stu-id="03b54-155">The **Allow Redirect** checkbox applies to the treatment of server-side redirects.</span></span> <span data-ttu-id="03b54-156">如果您勾選此方塊，伺服器端重新導向就會在 open-in 標記指定的瀏覽器中開啟。</span><span class="sxs-lookup"><span data-stu-id="03b54-156">If you check this box, server-side redirects will open in the browser specified by the open-in tag.</span></span> <span data-ttu-id="03b54-157">如需詳細資訊，請在 [此處](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes)參閱。</span><span class="sxs-lookup"><span data-stu-id="03b54-157">For more information, see [here](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).</span></span>
6. <span data-ttu-id="03b54-158">在 [註解] 方塊中輸入 **關於網站的任何註解**。</span><span class="sxs-lookup"><span data-stu-id="03b54-158">Type any comments about the website into the **Comment** box.</span></span> <span data-ttu-id="03b54-159">系統管理員只能在此工具中查看註解，並且這些註解保留在網站清單 xml 中。</span><span class="sxs-lookup"><span data-stu-id="03b54-159">Administrators can only see comments while they’re in this tool and these comments are retained in the site list xml.</span></span>
7. <span data-ttu-id="03b54-160">按一下 **[新增]** 以將網站新增到您的網站清單。</span><span class="sxs-lookup"><span data-stu-id="03b54-160">Click **Add** to add the site to your site list.</span></span>

### <a name="export-site-list-to-xml"></a><span data-ttu-id="03b54-161">將網站清單匯出到 XML</span><span class="sxs-lookup"><span data-stu-id="03b54-161">Export site list to XML</span></span>

<span data-ttu-id="03b54-162">在 Enterprise Site List Manager 中建立您的網站清單後，可以將內容匯出至企業模式 (.EMIE) 或 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="03b54-162">After you create your site list in the Enterprise Site List Manager, you can export the contents to an Enterprise Mode (.EMIE) or XML file.</span></span> 

> [!NOTE]
> <span data-ttu-id="03b54-163">此檔案包含您所有的 URL (包括您的相容性模式選項)，應儲存在安全之處。</span><span class="sxs-lookup"><span data-stu-id="03b54-163">This file includes all of your URLs, including your compatibility mode selections and should be stored somewhere safe.</span></span>

<span data-ttu-id="03b54-164">若要匯出網站清單，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="03b54-164">To export the site list, follow these steps:</span></span>

1. <span data-ttu-id="03b54-165">在 Enterprise Site List Manager 中，按一下 **[匯出到 XML]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-165">In the Enterprise Site List Manager, click **Export to XML**.</span></span>
2. <span data-ttu-id="03b54-166">輸入 **版本號碼** 和 **檔案名稱**。</span><span class="sxs-lookup"><span data-stu-id="03b54-166">Enter a **Version number** and a **File name**.</span></span>
3. <span data-ttu-id="03b54-167">按一下 **[匯出]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-167">Click **Export**.</span></span>

<span data-ttu-id="03b54-168">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-168">You can save the file locally or to a network share.</span></span> <span data-ttu-id="03b54-169">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-169">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="03b54-170">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="03b54-170">For more information, see [Turn on Internet Explorer mode and use a site list](./edge-ie-mode-policies.md).</span></span>

### <a name="import-multiple-sites-to-your-site-list"></a><span data-ttu-id="03b54-171">將多個網站匯入您的網站清單</span><span class="sxs-lookup"><span data-stu-id="03b54-171">Import multiple sites to your site list</span></span>

<span data-ttu-id="03b54-172">建立 .xml 檔案後，您可以使用 **[從 XML 匯入]** 功能，將網站大量新增至編輯器。</span><span class="sxs-lookup"><span data-stu-id="03b54-172">After you create your .xml file, you can bulk add sites to the editor using **Import from XML**.</span></span>

<span data-ttu-id="03b54-173">如果您想要取代編輯器中所有的內容，請按一下省略符號 (...) ，然後選擇 **[清除清單]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-173">If you want to replace all the contents in the editor, click  the ellipsis (…) and then choose **Clear list**.</span></span> <span data-ttu-id="03b54-174">清除編輯器之後，請使用下列步驟來匯入網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-174">After you clear the editor, use the following steps to import the site.</span></span>

1. <span data-ttu-id="03b54-175">在 Enterprise Site List Manager 中，按一下 **[從 XML 匯入]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-175">In the Enterprise Site List Manager, click **Import from XML**.</span></span> 
2. <span data-ttu-id="03b54-176">按一下 **[選擇檔案]** 選取您的網站清單，將包含的網站新增到工具中。</span><span class="sxs-lookup"><span data-stu-id="03b54-176">Click **Choose file** to select your site list to add the included sites to the tool.</span></span> <span data-ttu-id="03b54-177">挑選您想要新增的網站清單，然後按一下 **[開啟]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-177">Pick the site list you want to add and then click **Open**.</span></span> <span data-ttu-id="03b54-178">支援的匯入格式為包含 Enterprise Mode Site List 的 v.2 結構描述的 .xml、.emie 或 .txt。</span><span class="sxs-lookup"><span data-stu-id="03b54-178">Supported formats for Import are .xml, .emie or .txt containing the v.2 schema for Enterprise Mode Site List.</span></span> <span data-ttu-id="03b54-179">請參閲[企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="03b54-179">See [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>
3. <span data-ttu-id="03b54-180">按一下 **[載入]**  以從檔案 tp 編輯器新增網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-180">Click **Load** to add the sites from the file tp the editor.</span></span>

<span data-ttu-id="03b54-181">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-181">You can save the file locally or to a network share.</span></span> <span data-ttu-id="03b54-182">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-182">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="03b54-183">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="03b54-183">For more information, see [Turn on Internet Explorer mode and use a site list](./edge-ie-mode-policies.md).</span></span>

### <a name="edit-sites-in-your-site-list"></a><span data-ttu-id="03b54-184">編輯您的網站清單中的網站</span><span class="sxs-lookup"><span data-stu-id="03b54-184">Edit sites in your site list</span></span>

 <span data-ttu-id="03b54-185">您可以在 Enterprise Site List Manager 中編輯現有網站項目的屬性。</span><span class="sxs-lookup"><span data-stu-id="03b54-185">You can edit attributes of existing site entries in the Enterprise Site List Manager.</span></span> <span data-ttu-id="03b54-186">您也可以新增、移除或刪除相關聯的註解。</span><span class="sxs-lookup"><span data-stu-id="03b54-186">You can also add, remove, or delete associated comments.</span></span>

1. <span data-ttu-id="03b54-187">在 Enterprise Site List Manager 中，按一下省略符號 (…)，然後為要編輯的 URL 選擇 **[編輯網站]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-187">In the Enterprise Site List Manager, click the ellipsis (…) and choose **Edit site** for the URL you want to edit.</span></span>
2. <span data-ttu-id="03b54-188">您可以編輯網站項目的任何屬性，但 URL 除外。</span><span class="sxs-lookup"><span data-stu-id="03b54-188">You can edit any attribute of the site entry except the URL.</span></span> <span data-ttu-id="03b54-189">完成編輯後，按一下 **[儲存]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-189">Click **Save** after you finish editing.</span></span>

   > [!NOTE]
   > <span data-ttu-id="03b54-190">如果您想要刪除網站項目，請選擇步驟 1 中的 **[刪除網站]**。</span><span class="sxs-lookup"><span data-stu-id="03b54-190">If you want to delete a site entry, choose **Delete site** in step 1.</span></span>

3. <span data-ttu-id="03b54-191">按一下 **[匯出至 XML]**，然後儲存已更新檔案。</span><span class="sxs-lookup"><span data-stu-id="03b54-191">Click **Export to XML**, and save the updated file.</span></span>

<span data-ttu-id="03b54-192">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-192">You can save the file locally or to a network share.</span></span> <span data-ttu-id="03b54-193">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="03b54-193">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="03b54-194">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="03b54-194">For more information, see [Turn on Internet Explorer mode and use a site list](./edge-ie-mode-policies.md).</span></span>

### <a name="preview-your-site-list-in-xml-format"></a><span data-ttu-id="03b54-195">以 XML 格式預覽您的網站清單</span><span class="sxs-lookup"><span data-stu-id="03b54-195">Preview your site list in XML format</span></span>

<span data-ttu-id="03b54-196">匯出並儲存到網站清單位置之前，可以在編輯器中以 XML 格式預覽網站。</span><span class="sxs-lookup"><span data-stu-id="03b54-196">You can preview the sites in the editor in XML format before you export and save to your site list location.</span></span> <span data-ttu-id="03b54-197">按一下 **[XML 預覽]** ，即可在新的索引標籤中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="03b54-197">Click **XML preview** to open the file in a new tab.</span></span>

### <a name="search-in-the-enterprise-site-list-manager"></a><span data-ttu-id="03b54-198">在 Enterprise Site List Manager 中搜尋</span><span class="sxs-lookup"><span data-stu-id="03b54-198">Search in the Enterprise Site List Manager</span></span>

<span data-ttu-id="03b54-199">您可以搜尋並查看特定網站是否已出現在網站清單中，若已存在，您就不用嘗試將它重新新增。</span><span class="sxs-lookup"><span data-stu-id="03b54-199">You can search to see if a specific site already appears in your site list so you don’t try to add it again.</span></span>

<span data-ttu-id="03b54-200">若要搜尋，請在編輯器右上角的  **[依 URL 篩選網站]** 搜尋方塊中鍵入部分 URL。</span><span class="sxs-lookup"><span data-stu-id="03b54-200">To search, type part of the URL into the **Filter sites by URL** search box on the top right-hand corner of the editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="03b54-201">請參閱</span><span class="sxs-lookup"><span data-stu-id="03b54-201">See also</span></span>

- [<span data-ttu-id="03b54-202">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="03b54-202">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="03b54-203">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="03b54-203">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="03b54-204">企業模式結構描述 v.2 指導方針</span><span class="sxs-lookup"><span data-stu-id="03b54-204">Enterprise Mode schema v.2 guidance</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [<span data-ttu-id="03b54-205">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="03b54-205">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)