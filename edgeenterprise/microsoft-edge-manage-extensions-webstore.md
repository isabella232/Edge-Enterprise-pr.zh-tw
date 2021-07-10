---
title: 自我裝載 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 瞭解如何在企業中封裝和自我裝載 Microsoft Edge 擴充功能。
ms.openlocfilehash: aef4438212829006e39572fa938462f13721c580
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642869"
---
# <a name="self-host-microsoft-edge-extensions"></a><span data-ttu-id="f641e-103">自我裝載 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="f641e-103">Self-host Microsoft Edge extensions</span></span>

<span data-ttu-id="f641e-104">本文提供封裝擴充功能以在您自己的 WebStore 上裝載的基本指引。</span><span class="sxs-lookup"><span data-stu-id="f641e-104">This article provides basic guidance for packaging an extension to host on your own webstore.</span></span> <span data-ttu-id="f641e-105">它也包含如何在您的組織內將擴充功能部署至裝置和使用者的指示。</span><span class="sxs-lookup"><span data-stu-id="f641e-105">It also includes instructions on how to deploy extensions to devices and users in your organization.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f641e-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="f641e-106">Prerequisites</span></span>

<span data-ttu-id="f641e-107">若要自我裝載您自己的擴充功能，您必須為擴充功能及其資訊清單檔案提供您自己的虛擬主機服務。</span><span class="sxs-lookup"><span data-stu-id="f641e-107">To self-host your own extensions, you will need to provide your own web hosting services for the extensions and their manifest files.</span></span>

 <span data-ttu-id="f641e-108">下列步驟假設您已建立擴充功能、具有 XML 檔案的一些經驗、具備設定群組原則的工作知識，以及瞭解如何使用 Windows 登錄。</span><span class="sxs-lookup"><span data-stu-id="f641e-108">The following steps assume that you’ve already created your extension, have some experience with XML files, have a working knowledge of configuring group policy, and know how to use the Windows registry.</span></span>

## <a name="publish-an-extension"></a><span data-ttu-id="f641e-109">發佈擴充功能</span><span class="sxs-lookup"><span data-stu-id="f641e-109">Publish an extension</span></span>

<span data-ttu-id="f641e-110">發佈擴充功能之前，需要將其封裝至 CRX (Chrome 延伸) 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-110">Before you publish an extension it needs to be packed into a CRX (Chrome extension) file.</span></span> <span data-ttu-id="f641e-111">使用下列作為指南的步驟以將擴充功能封裝為 CRX 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-111">Use the following steps as a guide to packing an extension as a CRX file.</span></span>

1. <span data-ttu-id="f641e-112">在 Microsoft Edge 網址列中，請移至 *edge://extensions*，並開啟 **開發人員模式** (如果尚未啟用)。</span><span class="sxs-lookup"><span data-stu-id="f641e-112">In the Microsoft Edge address bar, go to *edge://extensions* and turn on **Developer mode** if it’s not already enabled.</span></span>
2. <span data-ttu-id="f641e-113">在 **已安裝的擴充功能**底下，按一下 **封裝擴充功能** 以建立 CRX 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-113">Under **Installed extensions**, click **Pack Extension** to create the CRX file.</span></span>
3. <span data-ttu-id="f641e-114">使用 **封裝擴充功能** 對話方塊以尋找具有擴充功能來源的目錄。</span><span class="sxs-lookup"><span data-stu-id="f641e-114">Use the **Pack extension** dialog to find the directory that has the source for the extension.</span></span> <span data-ttu-id="f641e-115">選取目錄，然後按一下 **封裝擴充功能**。</span><span class="sxs-lookup"><span data-stu-id="f641e-115">Select the directory and then click **Pack extension**.</span></span>  <span data-ttu-id="f641e-116">這會建立您的 CRX 檔案和 PEM 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-116">This will create your CRX file, along with a PEM file.</span></span> <span data-ttu-id="f641e-117">儲存 PEM 檔案，因為需要將擴充功能更新版本。</span><span class="sxs-lookup"><span data-stu-id="f641e-117">Save the PEM file because it’s needed for making version updates to the extension.</span></span> <span data-ttu-id="f641e-118">下一個螢幕擷取畫面顯示 **封裝擴充功能** 對話方塊，用於尋找擴充功能的根目錄。</span><span class="sxs-lookup"><span data-stu-id="f641e-118">The next screenshot shows the **Pack extension** dialog for locating the root directory of the extension.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="用於尋找擴充功能的原始碼的封裝擴充功能對話方塊。":::

   > [!IMPORTANT]
   > <span data-ttu-id="f641e-120">將 PEM 檔案儲存在安全的位置，因為它是擴充功能的金鑰，而且未來更新需要它。</span><span class="sxs-lookup"><span data-stu-id="f641e-120">Store the PEM file in a safe location because it’s the key for the extension and it’s needed for future updates.</span></span>

4. <span data-ttu-id="f641e-121">將 CRX 檔案拖曳到擴充功能視窗中並確定已載入該檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-121">Drag the CRX file into your extensions window and make sure that it loads.</span></span>
5. <span data-ttu-id="f641e-122">測試擴充功能，並記錄識別碼欄位 (這是 CRX 識別碼) 和版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f641e-122">Test the extension and take note of the ID field (this is the CRX ID) and version number.</span></span> <span data-ttu-id="f641e-123">您稍後會需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="f641e-123">You’ll need this information later.</span></span> <span data-ttu-id="f641e-124">下一個螢幕擷取畫面顯示具有 CRX 識別碼的測試擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-124">The next screenshot shows a test extension with its CRX ID.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="顯示 CRX 識別碼的擴充功能範例":::

6. <span data-ttu-id="f641e-126">將 CRX 檔案上傳至主機，並注意要下載的 URL 位置。</span><span class="sxs-lookup"><span data-stu-id="f641e-126">Upload the the CRX file to the host and note the URL of the location it will be downloaded from.</span></span> <span data-ttu-id="f641e-127">這項資訊對 XML 資訊清單檔案是必須的。</span><span class="sxs-lookup"><span data-stu-id="f641e-127">This information is needed for the XML manifest file.</span></span>
7. <span data-ttu-id="f641e-128">若要使用應用程式/擴充功能識別碼、下載 URL 和版本以建立資訊清單 XML 檔案，請定義以下欄位：</span><span class="sxs-lookup"><span data-stu-id="f641e-128">To create a manifest XML file with the app/extension ID, download URL, and version, define the following fields:</span></span>  

   - <span data-ttu-id="f641e-129">**appid** - 步驟 5 的擴充功能識別碼</span><span class="sxs-lookup"><span data-stu-id="f641e-129">**appid** - The extension ID from step 5</span></span>
   - <span data-ttu-id="f641e-130">**codebase** - 步驟 6 中的 CRX 檔案下載位置</span><span class="sxs-lookup"><span data-stu-id="f641e-130">**codebase** - The download location for the CRX file from step 6</span></span>
   - <span data-ttu-id="f641e-131">**版本** - 應用程式/擴充功能的版本，應符合擴充功能資訊清單中的指定版本。</span><span class="sxs-lookup"><span data-stu-id="f641e-131">**version** - The version of the app/extension, which should match the version specified in the manifest of the extension.</span></span>

   <span data-ttu-id="f641e-132">下一個程式碼片段會顯示 XML 資訊清單檔案的範例。</span><span class="sxs-lookup"><span data-stu-id="f641e-132">The next code snippet shows an example of an XML manifest file.</span></span>

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   <span data-ttu-id="f641e-133">如需詳細資訊，請參閱 [Microsoft Edge 中自動更新擴充功能 - Microsoft Edge 開發](/microsoft-edge/extensions-chromium/enterprise/auto-update)。</span><span class="sxs-lookup"><span data-stu-id="f641e-133">For more information, see [Auto-update extensions in Microsoft Edge - Microsoft Edge Development](/microsoft-edge/extensions-chromium/enterprise/auto-update).</span></span>

8. <span data-ttu-id="f641e-134">將已完成的 XML 檔案上傳至可從中下載的位置，並記錄此 URL。</span><span class="sxs-lookup"><span data-stu-id="f641e-134">Upload the completed XML file to a location where it can be downloaded from, noting the URL.</span></span> <span data-ttu-id="f641e-135">當您使用群組原則安裝擴充功能時會需要此 URL。</span><span class="sxs-lookup"><span data-stu-id="f641e-135">This URL will be needed when you install the extension using a group policy.</span></span> <span data-ttu-id="f641e-136">請參閱 [發佈私人託管的擴充功能](#distribute-a-privately-hosted-extension)。</span><span class="sxs-lookup"><span data-stu-id="f641e-136">See [Distribute a privately hosted extension](#distribute-a-privately-hosted-extension).</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="f641e-137">擴充功能的主機位置不需要驗證。</span><span class="sxs-lookup"><span data-stu-id="f641e-137">The hosting location for the extension doesn’t need authentication.</span></span> <span data-ttu-id="f641e-138">無論使用者裝置的可能使用位置在何處，都必須能夠存取該裝置。</span><span class="sxs-lookup"><span data-stu-id="f641e-138">It needs to be accessible by user devices wherever they might be used.</span></span>

## <a name="publish-updates-to-an-extension"></a><span data-ttu-id="f641e-139">發佈更新至擴充功能</span><span class="sxs-lookup"><span data-stu-id="f641e-139">Publish updates to an extension</span></span>

<span data-ttu-id="f641e-140">變更和測試更新的擴充功能之後，您就可以發佈它。</span><span class="sxs-lookup"><span data-stu-id="f641e-140">After you change and test the updated extension you can publish it.</span></span> <span data-ttu-id="f641e-141">使用下列步驟做為發佈更新的指南。</span><span class="sxs-lookup"><span data-stu-id="f641e-141">Use the following steps as a guide for publishing an update.</span></span>

1. <span data-ttu-id="f641e-142">使用下列語法，將擴充功能之 manifest.JSON 檔案中的版本號碼進行變更以提升為較高的版本號碼：`"version":"versionString"`。</span><span class="sxs-lookup"><span data-stu-id="f641e-142">Change the version number in your extension's manifest.JSON file to a higher number using the following syntax: `"version":"versionString"`.</span></span> <span data-ttu-id="f641e-143">如果「版本」：「1.0」，之後您就可以更新為「版本」：「1.1」或任何高於「1.0」的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f641e-143">If the "version":"1.0", then you can update to "version":"1.1" or any number higher than "1.0".</span></span>
2. <span data-ttu-id="f641e-144">更新 XML 檔案中的 `<updatecheck>`「版本」，以符合您在上一個步驟中放入資訊清單檔案中的號碼。</span><span class="sxs-lookup"><span data-stu-id="f641e-144">Update the "version" of `<updatecheck>` in the XML file to match the number that you put in the manifest file in the previous step.</span></span> <span data-ttu-id="f641e-145">例如：</span><span class="sxs-lookup"><span data-stu-id="f641e-145">For example:</span></span><br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. <span data-ttu-id="f641e-146">建立包含新增變更的 CRX 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-146">Create a CRX file that includes the new changes.</span></span> <span data-ttu-id="f641e-147">請前往 *edge://extensions* 並啟用 **開發人員模式**。</span><span class="sxs-lookup"><span data-stu-id="f641e-147">Go to *edge://extensions* and enable **Developer mode**.</span></span>
4. <span data-ttu-id="f641e-148">按一下 **封裝擴充功能**，然後前往擴充功能來源的目錄。</span><span class="sxs-lookup"><span data-stu-id="f641e-148">Click **Pack extension** and go to the directory for the extension source.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="f641e-149">使用第一次建立 CRX 檔案時產生並儲存的相同 PEM 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-149">Use the same PEM file that was generated and saved the first time the CRX file was created.</span></span> <span data-ttu-id="f641e-150">如果您沒有使用相同的 PEM 檔案，擴充功能的應用程式識別碼將會變更，並將更新會視為新的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-150">If you don't use the same PEM file the app ID of the extension will change and the update will be treated as a new extension.</span></span>

5. <span data-ttu-id="f641e-151">將 CRX 檔案拖放到擴充功能視窗，並確認已載入該檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-151">Drag and drop the CRX file into the extensions window and verify that it loads.</span></span>
6. <span data-ttu-id="f641e-152">測試更新的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-152">Test the updated extension.</span></span>
7. <span data-ttu-id="f641e-153">將以更新副檔名的新檔案取代舊的 CRX 檔案和 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="f641e-153">Replace the old CRX file and XML file with the new files for the updated extension.</span></span>

<span data-ttu-id="f641e-154">擴充功能的變更將在下一個原則同步週期中選取。</span><span class="sxs-lookup"><span data-stu-id="f641e-154">The extension's changes will be picked up during the next policy sync cycle.</span></span> <span data-ttu-id="f641e-155">如需更新擴充功能的詳細資訊，請參閱：[更新 URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) 和 [更新資訊清單](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest)。</span><span class="sxs-lookup"><span data-stu-id="f641e-155">For more information about updating extensions, see: [Update URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) and [Update manifest](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest).</span></span>

## <a name="distribute-a-privately-hosted-extension"></a><span data-ttu-id="f641e-156">發佈私人託管的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-156">Distribute a privately hosted extension</span></span>

<span data-ttu-id="f641e-157">您可以共用 CRX 檔案託管位置的連結，而且一旦使用者在瀏覽器中輸入 URL，就會下載並安裝此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-157">You can share the link of the location where the CRX file is hosted, and as soon as users enter the URL in their browser the extension will be downloaded and installed.</span></span> <span data-ttu-id="f641e-158">使用者可以從 edge://extensions 網頁啟用此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="f641e-158">Users can enable the extension from the edge://extensions page.</span></span> <span data-ttu-id="f641e-159">若要允許使用者安裝自我裝載的擴充功能，您必須將擴充功能 CRX ID 新增到 [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) 原則。</span><span class="sxs-lookup"><span data-stu-id="f641e-159">To allow users to install self-hosted extensions, you need to add the extension CRX IDs to the [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) policy.</span></span>

<span data-ttu-id="f641e-160">或者，您可以使用群組原則 [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) 以強制安裝擴充功能至使用者的裝置上。</span><span class="sxs-lookup"><span data-stu-id="f641e-160">Alternatively, you can use group policy [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) to Force-install an extension on your users’ devices.</span></span>

<span data-ttu-id="f641e-161">您可以將這些原則套用至您所選取的使用者、裝置或兩者皆套用。</span><span class="sxs-lookup"><span data-stu-id="f641e-161">You can apply these policies to your selected users, devices, or both.</span></span> <span data-ttu-id="f641e-162">請記住，此原則更新是非即時性的，而且需要一些時間讓該原則設定生效。</span><span class="sxs-lookup"><span data-stu-id="f641e-162">Remember though that policy updates are not instantaneous, and it will take time for the policy settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="f641e-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f641e-163">See also</span></span>

- [<span data-ttu-id="f641e-164">管理企業中的 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="f641e-164">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="f641e-165">使用群組原則以管理 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="f641e-165">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="f641e-166">ExtensionSettings 原則的詳細指南</span><span class="sxs-lookup"><span data-stu-id="f641e-166">Detailed guide to the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="f641e-167">Microsoft Edge 擴充功能常見問題集</span><span class="sxs-lookup"><span data-stu-id="f641e-167">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="f641e-168">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f641e-168">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
