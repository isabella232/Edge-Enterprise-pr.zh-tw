---
title: 'Microsoft Edge 中的 Enterprise Site List Manager  '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 01/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '在 Microsoft Edge 中啟用和使用 Enterprise Site List Manager  '
ms.openlocfilehash: 2d10886624918c97933a841c428ea66ccf5b34c9
ms.sourcegitcommit: a6c58b19976c194299be217c58b9a99b48756fd0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "11281044"
---
# <span data-ttu-id="f4410-103">Microsoft Edge 中的 Enterprise Site List Manager </span><span class="sxs-lookup"><span data-stu-id="f4410-103">Enterprise Site List Manager in Microsoft Edge</span></span>

<span data-ttu-id="f4410-104">本文說明如何在 Microsoft Edge 中啟用存取和使用 Enterprise Site List Manager ，以建立、編輯及匯出 Internet Explorer 模式的企業網站清單。</span><span class="sxs-lookup"><span data-stu-id="f4410-104">This article explains how to enable access to and use the Enterprise Site List Manager in Microsoft Edge to create, edit and export your Enterprise Mode Site List for Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="f4410-105">本文適用於 Microsoft Edge 版本 89 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f4410-105">This article applies to Microsoft Edge version 89 or later.</span></span>

## <span data-ttu-id="f4410-106">概觀</span><span class="sxs-lookup"><span data-stu-id="f4410-106">Overview</span></span>

<span data-ttu-id="f4410-107">Enterprise Site List Manager 是[獨立企業模式網站清單管理器工具](https://www.microsoft.com/download/details.aspx?id=49974)的瀏覽器內版本，用於建立、編輯和匯出組織的網站清單。</span><span class="sxs-lookup"><span data-stu-id="f4410-107">The Enterprise Site List Manager is an in-browser version of the [standalone Enterprise Mode Site List Manager tool](https://www.microsoft.com/download/details.aspx?id=49974) that lets you create, edit, and export your organization’s site list.</span></span>

<span data-ttu-id="f4410-108">未來將透過 Microsoft Edge 中的 Enterprise Site List Manager 提供對 Internet Explorer 模式工具的改良功能。</span><span class="sxs-lookup"><span data-stu-id="f4410-108">Future improvements to the tool for Internet Explorer mode will be available through Enterprise Site List Manager in Microsoft Edge.</span></span> <span data-ttu-id="f4410-109">獨立工具將繼續在下載中心提供，但不會得到任何功能更新。</span><span class="sxs-lookup"><span data-stu-id="f4410-109">The standalone tool will continue to be available in the Download Center but won't get any feature updates.</span></span>

## <span data-ttu-id="f4410-110">啟用對 Enterprise Site List Manager 的存取</span><span class="sxs-lookup"><span data-stu-id="f4410-110">Enabling access to Enterprise Site List Manager</span></span>

<span data-ttu-id="f4410-111">您可以使用 [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) 群組原則來設定工具存取權。</span><span class="sxs-lookup"><span data-stu-id="f4410-111">You can configure access to the tool by using the [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) group policy.</span></span>

<span data-ttu-id="f4410-112">如果啟用，您的使用者將在 *edge://compat* 中的左側瀏覽窗格中看到名為「Enterprise Site List Manager」的選項。</span><span class="sxs-lookup"><span data-stu-id="f4410-112">If enabled, your users will see an option named Enterprise Site List Manager on the left navigation pane in *edge://compat*.</span></span> <span data-ttu-id="f4410-113">如果停用，使用者將不會在左側瀏覽窗格中看到 Enterprise Site List Manager 的進入點。</span><span class="sxs-lookup"><span data-stu-id="f4410-113">If Disabled, users will not see the entry point to Enterprise Site List Manager in the left navigation pane.</span></span> <span data-ttu-id="f4410-114">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="f4410-114">This is the default behavior.</span></span>

## <span data-ttu-id="f4410-115">使用 Enterprise Site List Manager</span><span class="sxs-lookup"><span data-stu-id="f4410-115">Using the Enterprise Site List Manager</span></span>

<span data-ttu-id="f4410-116">Enterprise Site List Manager 工具使用 v.2 版的結構描述。</span><span class="sxs-lookup"><span data-stu-id="f4410-116">The Enterprise Site List Manager tool uses the v.2 version of the schema.</span></span> <span data-ttu-id="f4410-117">如果您將 v.1 版的結構描述匯入 Enterprise Site List Manager (結構描述 v.2)，它會將 XML 儲存為 v.2 版的結構描述。</span><span class="sxs-lookup"><span data-stu-id="f4410-117">If you import a v.1 version schema into the Enterprise Site List Manager (schema v.2), the XML is saved into the v.2 version of the schema.</span></span>

### <span data-ttu-id="f4410-118">新增單一站台至您的網站清單</span><span class="sxs-lookup"><span data-stu-id="f4410-118">Add single sites to your site list</span></span>  

<span data-ttu-id="f4410-119">使用下列步驟將個別網站新增到您的網站清單中。</span><span class="sxs-lookup"><span data-stu-id="f4410-119">Use the following steps to add individual sites to your site list.</span></span>

> [!NOTE]
> <span data-ttu-id="f4410-120">您只能新增特定 URL，而非網際網路或內部網路區域。</span><span class="sxs-lookup"><span data-stu-id="f4410-120">You can only add specific URLs, not Internet or Intranet Zones.</span></span>

1. <span data-ttu-id="f4410-121">在 Enterprise Site List Manager 中，按一下  **[新增網站]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-121">In the Enterprise Site List Manager, click **Add a site**.</span></span>
2. <span data-ttu-id="f4410-122">在 URL 方塊中輸入要新增之網站的 URL，例如  <domain>.com 或  <domain>.com/<path> 。</span><span class="sxs-lookup"><span data-stu-id="f4410-122">Type the URL for the website you’d like to add, for example: <domain>.com or <domain>.com/<path> in the URL box.</span></span>
3. <span data-ttu-id="f4410-123">從 **[開啟位置]**  清單中選取以下選項之一：</span><span class="sxs-lookup"><span data-stu-id="f4410-123">Select one of the following options from the **Open in** list:</span></span>

   - <span data-ttu-id="f4410-124">**IE11**。</span><span class="sxs-lookup"><span data-stu-id="f4410-124">**IE11**.</span></span> <span data-ttu-id="f4410-125">在 IE11 應用程式中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-125">Opens the site in the IE11 application.</span></span>
   - <span data-ttu-id="f4410-126">**IE 模式**。</span><span class="sxs-lookup"><span data-stu-id="f4410-126">**IE mode**.</span></span> <span data-ttu-id="f4410-127">在 Microsoft Edge 上以 Internet Explorer 模式開啟網站 (如已啟用)，否則在 IE11 應用程式中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-127">Opens the site in Internet Explorer mode on Microsoft Edge if enabled and in the IE11 app otherwise.</span></span> <span data-ttu-id="f4410-128">請參閱 [Microsoft Edge 上的 Internet Explorer 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。</span><span class="sxs-lookup"><span data-stu-id="f4410-128">See [Internet Explorer mode on Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>
   - <span data-ttu-id="f4410-129">**MSEdge**。</span><span class="sxs-lookup"><span data-stu-id="f4410-129">**MSEdge**.</span></span> <span data-ttu-id="f4410-130">在 Microsoft Edge 中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-130">Opens the site in Microsoft Edge.</span></span>
   - <span data-ttu-id="f4410-131">**可設定**。</span><span class="sxs-lookup"><span data-stu-id="f4410-131">**Configurable**.</span></span> <span data-ttu-id="f4410-132">允許網站參與 IE 模式引擎判斷。</span><span class="sxs-lookup"><span data-stu-id="f4410-132">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="f4410-133">請參閲[IE 模式中可設定的網站](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)</span><span class="sxs-lookup"><span data-stu-id="f4410-133">See [Configurable sites in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)</span></span>
   - <span data-ttu-id="f4410-134">**無**。</span><span class="sxs-lookup"><span data-stu-id="f4410-134">**None**.</span></span> <span data-ttu-id="f4410-135">在使用者選擇的任何瀏覽器中開啟。</span><span class="sxs-lookup"><span data-stu-id="f4410-135">Opens in whatever browser the user chooses.</span></span>  

4. <span data-ttu-id="f4410-136">在  **[相容模式下]**，選擇下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f4410-136">Under **Compat Mode**, choose one of the following options:</span></span>

   - <span data-ttu-id="f4410-137">**IE8Enterprise**。</span><span class="sxs-lookup"><span data-stu-id="f4410-137">**IE8Enterprise**.</span></span> <span data-ttu-id="f4410-138">在 IE8 企業模式中載入網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-138">Loads the site in IE8 Enterprise Mode.</span></span>
   - <span data-ttu-id="f4410-139">**IE7Enterprise**。</span><span class="sxs-lookup"><span data-stu-id="f4410-139">**IE7Enterprise**.</span></span> <span data-ttu-id="f4410-140">在 IE7 企業模式載入網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-140">Loads the site in IE7 Enterprise Mode.</span></span>
   - <span data-ttu-id="f4410-141">**IE[x]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-141">**IE[x]**.</span></span> <span data-ttu-id="f4410-142">[x] 是文件模式的數目，而網站會以指定的文件模式載入。</span><span class="sxs-lookup"><span data-stu-id="f4410-142">Where [x] is the document mode number and the site loads in the specified document mode.</span></span>
   - <span data-ttu-id="f4410-143">**預設模式**。</span><span class="sxs-lookup"><span data-stu-id="f4410-143">**Default Mode**.</span></span> <span data-ttu-id="f4410-144">使用頁面的預設相容性模式載入網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-144">Loads the site using the default compatibility mode for the page.</span></span>

   <span data-ttu-id="f4410-145">網域內的路徑可能需要不同於網域本身的相容性模式。</span><span class="sxs-lookup"><span data-stu-id="f4410-145">The path within a domain can require a different compatibility mode from the domain itself.</span></span> <span data-ttu-id="f4410-146">例如，網域在預設的 IE11 瀏覽器中可能一切正常，但路徑可能會有問題，而需要使用企業模式。</span><span class="sxs-lookup"><span data-stu-id="f4410-146">For example, the domain might look fine in the default IE11 browser, but the path might have problems and require the use of Enterprise Mode.</span></span> <span data-ttu-id="f4410-147">如果您先前已新增網域，則仍會選取您原本選擇的相容性。</span><span class="sxs-lookup"><span data-stu-id="f4410-147">If you added the domain previously, your original compatibility choice is still selected.</span></span> <span data-ttu-id="f4410-148">不過，如果網域是新的，則會自動選取  **[IE8 企業模式]** 。</span><span class="sxs-lookup"><span data-stu-id="f4410-148">However, if the domain is new, **IE8 Enterprise Mode** is automatically selected.</span></span>

   <span data-ttu-id="f4410-149">企業模式的優先順序高於文件模式，因此已經在企業模式網站清單中的網站不會受此更新影響，而會如往常一樣以企業模式載入。</span><span class="sxs-lookup"><span data-stu-id="f4410-149">Enterprise Mode takes precedence over document modes, so sites that are already included in the Enterprise Mode site list won’t be affected by this update and will continue to load in Enterprise Mode, as usual.</span></span> <span data-ttu-id="f4410-150">如需使用文件模式的進一步詳細資訊，請參閱 [使用文件模式和企業模式網站清單修正網頁相容性問題](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list)。</span><span class="sxs-lookup"><span data-stu-id="f4410-150">For more specific information about using document modes, see [Fix web compatibility issues using document modes and the Enterprise Mode site list](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list).</span></span>

5. <span data-ttu-id="f4410-151">**[允許重新導向]** 核取方塊適用于處理伺服器端重新導向。</span><span class="sxs-lookup"><span data-stu-id="f4410-151">The **Allow Redirect** checkbox applies to the treatment of server-side redirects.</span></span> <span data-ttu-id="f4410-152">如果您勾選此方塊，伺服器端重新導向就會在 open-in 標記指定的瀏覽器中開啟。</span><span class="sxs-lookup"><span data-stu-id="f4410-152">If you check this box, server-side redirects will open in the browser specified by the open-in tag.</span></span> <span data-ttu-id="f4410-153">如需詳細資訊，請在 [此處](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes)參閱。</span><span class="sxs-lookup"><span data-stu-id="f4410-153">For more information, see [here](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes).</span></span>
6. <span data-ttu-id="f4410-154">在 [註解] 方塊中輸入 **關於網站的任何註解**。</span><span class="sxs-lookup"><span data-stu-id="f4410-154">Type any comments about the website into the **Comment** box.</span></span> <span data-ttu-id="f4410-155">系統管理員只能在此工具中查看註解，並且這些註解保留在網站清單 xml 中。</span><span class="sxs-lookup"><span data-stu-id="f4410-155">Administrators can only see comments while they’re in this tool and these comments are retained in the site list xml.</span></span>
7. <span data-ttu-id="f4410-156">按一下 **[新增]** 以將網站新增到您的網站清單。</span><span class="sxs-lookup"><span data-stu-id="f4410-156">Click **Add** to add the site to your site list.</span></span>

### <span data-ttu-id="f4410-157">將網站清單匯出到 XML</span><span class="sxs-lookup"><span data-stu-id="f4410-157">Export site list to XML</span></span>

<span data-ttu-id="f4410-158">在 Enterprise Site List Manager 中建立您的網站清單後，可以將內容匯出至企業模式 (.EMIE) 或 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="f4410-158">After you create your site list in the Enterprise Site List Manager, you can export the contents to an Enterprise Mode (.EMIE) or XML file.</span></span> 

> [!NOTE]
> <span data-ttu-id="f4410-159">此檔案包含您所有的 URL (包括您的相容性模式選項)，應儲存在安全之處。</span><span class="sxs-lookup"><span data-stu-id="f4410-159">This file includes all of your URLs, including your compatibility mode selections and should be stored somewhere safe.</span></span>

<span data-ttu-id="f4410-160">若要匯出網站清單，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f4410-160">To export the site list, follow these steps:</span></span>

1. <span data-ttu-id="f4410-161">在 Enterprise Site List Manager 中，按一下 **[匯出到 XML]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-161">In the Enterprise Site List Manager, click **Export to XML**.</span></span>
2. <span data-ttu-id="f4410-162">輸入 **版本號碼** 和 **檔案名稱**。</span><span class="sxs-lookup"><span data-stu-id="f4410-162">Enter a **Version number** and a **File name**.</span></span>
3. <span data-ttu-id="f4410-163">按一下 **[匯出]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-163">Click **Export**.</span></span>

<span data-ttu-id="f4410-164">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-164">You can save the file locally or to a network share.</span></span> <span data-ttu-id="f4410-165">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-165">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="f4410-166">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)。</span><span class="sxs-lookup"><span data-stu-id="f4410-166">For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).</span></span>

### <span data-ttu-id="f4410-167">將多個網站匯入您的網站清單</span><span class="sxs-lookup"><span data-stu-id="f4410-167">Import multiple sites to your site list</span></span>

<span data-ttu-id="f4410-168">建立 .xml 檔案後，您可以使用 **[從 XML 匯入]** 功能，將網站大量新增至編輯器。</span><span class="sxs-lookup"><span data-stu-id="f4410-168">After you create your .xml file, you can bulk add sites to the editor using **Import from XML**.</span></span>

<span data-ttu-id="f4410-169">如果您想要取代編輯器中所有的內容，請按一下省略符號 (...) ，然後選擇 **[清除清單]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-169">If you want to replace all the contents in the editor, click  the ellipsis (…) and then choose **Clear list**.</span></span> <span data-ttu-id="f4410-170">清除編輯器之後，請使用下列步驟來匯入網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-170">After you clear the editor, use the following steps to import the site.</span></span>

1. <span data-ttu-id="f4410-171">在 Enterprise Site List Manager 中，按一下 **[從 XML 匯入]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-171">In the Enterprise Site List Manager, click **Import from XML**.</span></span> 
2. <span data-ttu-id="f4410-172">按一下 **[選擇檔案]** 選取您的網站清單，將包含的網站新增到工具中。</span><span class="sxs-lookup"><span data-stu-id="f4410-172">Click **Choose file** to select your site list to add the included sites to the tool.</span></span> <span data-ttu-id="f4410-173">挑選您想要新增的網站清單，然後按一下 **[開啟]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-173">Pick the site list you want to add and then click **Open**.</span></span> <span data-ttu-id="f4410-174">支援的匯入格式為包含 Enterprise Mode Site List 的 v.2 結構描述的 .xml、.emie 或 .txt。</span><span class="sxs-lookup"><span data-stu-id="f4410-174">Supported formats for Import are .xml, .emie or .txt containing the v.2 schema for Enterprise Mode Site List.</span></span> <span data-ttu-id="f4410-175">請參閲[企業模式結構描述 v.2 指導方針](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="f4410-175">See [Enterprise Mode schema v.2 guidance](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>
3. <span data-ttu-id="f4410-176">按一下 **[載入]**  以從檔案 tp 編輯器新增網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-176">Click **Load** to add the sites from the file tp the editor.</span></span>

<span data-ttu-id="f4410-177">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-177">You can save the file locally or to a network share.</span></span> <span data-ttu-id="f4410-178">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-178">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="f4410-179">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)。</span><span class="sxs-lookup"><span data-stu-id="f4410-179">For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).</span></span>

### <span data-ttu-id="f4410-180">編輯您的網站清單中的網站</span><span class="sxs-lookup"><span data-stu-id="f4410-180">Edit sites in your site list</span></span>

 <span data-ttu-id="f4410-181">您可以在 Enterprise Site List Manager 中編輯現有網站項目的屬性。</span><span class="sxs-lookup"><span data-stu-id="f4410-181">You can edit attributes of existing site entries in the Enterprise Site List Manager.</span></span> <span data-ttu-id="f4410-182">您也可以新增、移除或刪除相關聯的註解。</span><span class="sxs-lookup"><span data-stu-id="f4410-182">You can also add, remove, or delete associated comments.</span></span>

1. <span data-ttu-id="f4410-183">在 Enterprise Site List Manager 中，按一下省略符號 (…)，然後為要編輯的 URL 選擇 **[編輯網站]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-183">In the Enterprise Site List Manager, click the ellipsis (…) and choose **Edit site** for the URL you want to edit.</span></span>
2. <span data-ttu-id="f4410-184">您可以編輯網站項目的任何屬性，但 URL 除外。</span><span class="sxs-lookup"><span data-stu-id="f4410-184">You can edit any attribute of the site entry except the URL.</span></span> <span data-ttu-id="f4410-185">完成編輯後，按一下 **[儲存]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-185">Click **Save** after you finish editing.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f4410-186">如果您想要刪除網站項目，請選擇步驟 1 中的 **[刪除網站]**。</span><span class="sxs-lookup"><span data-stu-id="f4410-186">If you want to delete a site entry, choose **Delete site** in step 1.</span></span>

3. <span data-ttu-id="f4410-187">按一下 **[匯出至 XML]**，然後儲存已更新檔案。</span><span class="sxs-lookup"><span data-stu-id="f4410-187">Click **Export to XML**, and save the updated file.</span></span>

<span data-ttu-id="f4410-188">您可以將檔案儲存在本機或網路共用位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-188">You can save the file locally or to a network share.</span></span> <span data-ttu-id="f4410-189">不過，您必須確實將它部署到您的登錄機碼中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="f4410-189">However, you must make sure you deploy it to the location specified in your registry key.</span></span> <span data-ttu-id="f4410-190">如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)。</span><span class="sxs-lookup"><span data-stu-id="f4410-190">For more information, see [Turn on Internet Explorer mode and use a site list](https://docs.microsoft.com/deployedge/edge-ie-mode-policies).</span></span>

### <span data-ttu-id="f4410-191">以 XML 格式預覽您的網站清單</span><span class="sxs-lookup"><span data-stu-id="f4410-191">Preview your site list in XML format</span></span>

<span data-ttu-id="f4410-192">匯出並儲存到網站清單位置之前，可以在編輯器中以 XML 格式預覽網站。</span><span class="sxs-lookup"><span data-stu-id="f4410-192">You can preview the sites in the editor in XML format before you export and save to your site list location.</span></span> <span data-ttu-id="f4410-193">按一下 **[XML 預覽]** ，即可在新的索引標籤中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="f4410-193">Click **XML preview** to open the file in a new tab.</span></span>

### <span data-ttu-id="f4410-194">在 Enterprise Site List Manager 中搜尋</span><span class="sxs-lookup"><span data-stu-id="f4410-194">Search in the Enterprise Site List Manager</span></span>

<span data-ttu-id="f4410-195">您可以搜尋並查看特定網站是否已出現在網站清單中，若已存在，您就不用嘗試將它重新新增。</span><span class="sxs-lookup"><span data-stu-id="f4410-195">You can search to see if a specific site already appears in your site list so you don’t try to add it again.</span></span>

<span data-ttu-id="f4410-196">若要搜尋，請在編輯器右上角的  **[依 URL 篩選網站]** 搜尋方塊中鍵入部分 URL。</span><span class="sxs-lookup"><span data-stu-id="f4410-196">To search, type part of the URL into the **Filter sites by URL** search box on the top right-hand corner of the editor.</span></span>

## <span data-ttu-id="f4410-197">請參閱</span><span class="sxs-lookup"><span data-stu-id="f4410-197">See also</span></span>

- [<span data-ttu-id="f4410-198">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f4410-198">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f4410-199">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="f4410-199">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="f4410-200">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="f4410-200">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="f4410-201">其他 Enterprise Site Discovery 資訊</span><span class="sxs-lookup"><span data-stu-id="f4410-201">Additional Enterprise Site Discovery information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)
