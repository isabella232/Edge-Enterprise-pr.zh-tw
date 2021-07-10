---
title: 使用 Jamf 在 macOS 上設定 Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 6/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Jamf 在 Mac 裝置上設定 Microsoft Edge 原則設定
ms.openlocfilehash: 8556a5b1d0fc01feb67fc86cb016a9ed47061b55
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641629"
---
# <a name="configure-microsoft-edge-policy-settings-on-macos-with-jamf"></a><span data-ttu-id="c6657-103">使用 Jamf 在 macOS 上設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="c6657-103">Configure Microsoft Edge policy settings on macOS with Jamf</span></span>

<span data-ttu-id="c6657-104">本文說明如何在 Jamf Pro 10.19 上使用 Microsoft Edge 原則清單檔案來設定 macOS 上的原則設定。</span><span class="sxs-lookup"><span data-stu-id="c6657-104">This article describes how to configure policy settings on macOS using a Microsoft Edge policy manifest file on Jamf Pro 10.19.</span></span>

<span data-ttu-id="c6657-105">您也可以使用屬性清單 (plist) 檔案，在 macOS 上設定 Microsoft Edge 原則設定。</span><span class="sxs-lookup"><span data-stu-id="c6657-105">You can also configure Microsoft Edge policy settings on macOS by using a property list (.plist) file.</span></span> <span data-ttu-id="c6657-106">如需詳細資訊，請參閱[使用 .plist 為 macOS 設定](configure-microsoft-edge-on-mac.md)。</span><span class="sxs-lookup"><span data-stu-id="c6657-106">For more information, see [Configure for macOS using a .plist](configure-microsoft-edge-on-mac.md)</span></span>


## <a name="prerequisites"></a><span data-ttu-id="c6657-107">必要條件</span><span class="sxs-lookup"><span data-stu-id="c6657-107">Prerequisites</span></span>

<span data-ttu-id="c6657-108">需要下列軟體：</span><span class="sxs-lookup"><span data-stu-id="c6657-108">The following software is required:</span></span>

- <span data-ttu-id="c6657-109">Microsoft Edge 穩定通道 81</span><span class="sxs-lookup"><span data-stu-id="c6657-109">Microsoft Edge Stable channel 81</span></span>
- <span data-ttu-id="c6657-110">原則範本檔案，版本 81.0.416.3</span><span class="sxs-lookup"><span data-stu-id="c6657-110">Policy Templates file, version 81.0.416.3</span></span>
- <span data-ttu-id="c6657-111">Jamf Pro，版本 10.19</span><span class="sxs-lookup"><span data-stu-id="c6657-111">Jamf Pro, Version 10.19</span></span>

## <a name="about-the-jamf-pro-application--custom-settings-menu"></a><span data-ttu-id="c6657-112">關於 Jamf Pro 應用程式與自訂設定功能表</span><span class="sxs-lookup"><span data-stu-id="c6657-112">About the Jamf Pro Application & Custom Settings menu</span></span>

<span data-ttu-id="c6657-113">Jamf Pro 10.18 之前，管理 Office 365 牽涉到手動建立 .plist 檔案。</span><span class="sxs-lookup"><span data-stu-id="c6657-113">Before Jamf Pro 10.18, managing Office 365 involved manually building a .plist file.</span></span> <span data-ttu-id="c6657-114">這是耗時的工作流程，需要強大的技術背景。</span><span class="sxs-lookup"><span data-stu-id="c6657-114">This was a time-consuming workflow that required a strong technical background.</span></span> <span data-ttu-id="c6657-115">Jamf Pro 10.18 將組態流程簡化，以消除這些障礙。</span><span class="sxs-lookup"><span data-stu-id="c6657-115">Jamf Pro 10.18 eliminated those barriers by streamlining the configuration process.</span></span> <span data-ttu-id="c6657-116">不過，IT 系統管理員只能針對 Jamf 所指定的特定應用程式和喜好設定網域使用這個新的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="c6657-116">However, IT Admins could only use this new user interface for specific applications and preference domains specified by Jamf.</span></span>

<span data-ttu-id="c6657-117">在 Jamf Pro 10.19 中，使用者可以將 JSON 資訊清單上傳為「自訂結構描述」，以鎖定任何喜好設定網域，而圖形使用者介面則會從此資訊清單產生。</span><span class="sxs-lookup"><span data-stu-id="c6657-117">In Jamf Pro 10.19, a user can upload a JSON manifest as a "custom schema" to target any preference domain, and the graphical user interface will be generated from this manifest.</span></span> <span data-ttu-id="c6657-118">建立的自訂架構會遵循 JSON 架構規格。</span><span class="sxs-lookup"><span data-stu-id="c6657-118">The custom schema that's created follows the JSON Schema specification.</span></span>

<span data-ttu-id="c6657-119">如需詳細資訊，請參閱 Jamf Pro 系統管理員指南中的[電腦組態設定檔](https://jamf.it/computer-configuration-profiles)。</span><span class="sxs-lookup"><span data-stu-id="c6657-119">For more information, see [Computer Configuration Profiles](https://jamf.it/computer-configuration-profiles) in the Jamf Pro Administrator's Guide.</span></span>

## <a name="get-the-policy-manifest-for-a-specific-version-of-microsoft-edge"></a><span data-ttu-id="c6657-120">取得特定版本 Microsoft Edge 的原則資訊清單</span><span class="sxs-lookup"><span data-stu-id="c6657-120">Get the policy manifest for a specific version of Microsoft Edge</span></span>

<span data-ttu-id="c6657-121">若要取得原則資訊清單：</span><span class="sxs-lookup"><span data-stu-id="c6657-121">To get the policy manifest:</span></span>

- <span data-ttu-id="c6657-122">移至 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)。</span><span class="sxs-lookup"><span data-stu-id="c6657-122">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="c6657-123">在 [通道/版本] 下拉式清單中，選取版本 81 或更新版本的任何通道\*\*\*\*_。</span><span class="sxs-lookup"><span data-stu-id="c6657-123">On the Channel/Version dropdown list, select **any channel with version 81 or later.**_.</span></span>
- <span data-ttu-id="c6657-124">在 [建立] 下拉式清單中，選取任何 81 組建或更新版本_\*\*\*_。</span><span class="sxs-lookup"><span data-stu-id="c6657-124">On the Build dropdown list, select any _*81 build or later.*\*_.</span></span>
- <span data-ttu-id="c6657-125">按一下 [取得原則檔案] 來下載我們的原則範本組合。</span><span class="sxs-lookup"><span data-stu-id="c6657-125">Click GET POLICY FILES to download our policy templates bundle.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c6657-126">目前，原則範本組合會以 CAB 檔案形式簽署。</span><span class="sxs-lookup"><span data-stu-id="c6657-126">Currently, the policy templates bundle is signed as a CAB file.</span></span> <span data-ttu-id="c6657-127">您需要使用協力廠商工具，例如 The Unarchiver，以在 macOS 上開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="c6657-127">You'll need to use a 3rd party tool, such as The Unarchiver to open the file on macOS.</span></span>

<span data-ttu-id="c6657-128">將 CAB 檔案解壓縮之後，將 ZIP 檔案解壓縮，並瀏覽至 "mac" 頂層目錄。</span><span class="sxs-lookup"><span data-stu-id="c6657-128">After you unpack the CAB file, unpack the ZIP file and navigate to the "mac" top level directory.</span></span> <span data-ttu-id="c6657-129">名稱為 "policy_manifest.json" 的資訊清單位於這個目錄中。</span><span class="sxs-lookup"><span data-stu-id="c6657-129">The manifest, which is named "policy_manifest.json", is in this directory.</span></span>

<span data-ttu-id="c6657-130">此資訊清單將會在從組建 81.0.416.3 開始的每個原則組合中發佈。</span><span class="sxs-lookup"><span data-stu-id="c6657-130">This manifest will be published in every policy bundle starting with build 81.0.416.3.</span></span> <span data-ttu-id="c6657-131">如果您想要在開發人員通道中測試原則，您可以使用與每個開發發行相關的資訊清單，並在 Jamf Pro 中進行測試。</span><span class="sxs-lookup"><span data-stu-id="c6657-131">If you want to test policies in the Dev channel, you can take the manifest associated with each Dev release and test it in Jamf Pro.</span></span>  

## <a name="use-the-policy-manifest-in-jamf-pro"></a><span data-ttu-id="c6657-132">在 Jamf Pro 中使用原則資訊清單</span><span class="sxs-lookup"><span data-stu-id="c6657-132">Use the policy manifest in Jamf Pro</span></span>

<span data-ttu-id="c6657-133">使用下列步驟將原則資訊清單上傳到 Jamf Pro，然後針對 macOS 建立原則設定檔。</span><span class="sxs-lookup"><span data-stu-id="c6657-133">Use the following steps to upload the policy manifest to Jamf Pro and then create a policy profile for macOS.</span></span>

1. <span data-ttu-id="c6657-134">登入 Jamf。</span><span class="sxs-lookup"><span data-stu-id="c6657-134">Sign in to Jamf.</span></span>
2. <span data-ttu-id="c6657-135">選取 [電腦]_\*\*\* 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="c6657-135">Select the _*Computer*\* tab.</span></span>
3. <span data-ttu-id="c6657-136">在 [內容管理]\*\*\*\* 底下，選取 [組態設定檔]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-136">Under **Content Management**, select **Configuration Profiles**.</span></span>
4. <span data-ttu-id="c6657-137">在 [組態設定檔]\*\*\*\* 頁面上，按一下 [+ 新增]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-137">On the **Configuration Profiles** page, click **+ New**.</span></span>

   ![在 Jamf 中新增設定檔](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. <span data-ttu-id="c6657-139">在 [新增 macOS 組態設定檔]\*\*\*\* > [選項]\*\*\*\* 中，選取 [應用程式與自訂設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-139">On **New macOS Configuration Profile**>**Options**, select **Application & Custom Settings**.</span></span>
6. <span data-ttu-id="c6657-140">在 [應用程式與自訂設定]\*\*\*\* 快顯視窗中，按一下 [設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-140">On the **Application & Custom Settings** popup window, click **Configure**.</span></span>

   ![設定應用程式與自訂設定](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. <span data-ttu-id="c6657-142">在 [應用程式與自訂設定]\*\*\*\* 區段中，設定下列螢幕擷取畫面中顯示的值。</span><span class="sxs-lookup"><span data-stu-id="c6657-142">In the **Application & Custom Settings** section, set the values shown in the following screen shot.</span></span>

   ![設定檔來源和自訂結構描述](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - <span data-ttu-id="c6657-144">針對 [建立方法]\*\*\*\*，挑選 [組態設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-144">For **Creation Method**, pick **Configure settings**.</span></span>
   - <span data-ttu-id="c6657-145">針對 [來源]\*\*\*\*，挑選 [自訂結構描述]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-145">For **Source**, pick **Custom Schema**.</span></span>
   - <span data-ttu-id="c6657-146">針對 [喜好設定網域]\*\*\*\*，提供您網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6657-146">For **Preference Domain**, provide the name of your domain.</span></span> <span data-ttu-id="c6657-147">此範例使用 *com.microsoft.Edge* 做為網域。</span><span class="sxs-lookup"><span data-stu-id="c6657-147">This example uses *com.microsoft.Edge* as the domain.</span></span>
   - <span data-ttu-id="c6657-148">在 [自訂架構]\*\*\*\* 中，貼上 "policy_manifest.json" 資訊清單檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="c6657-148">For **Custom Schema**, paste the contents of the "policy_manifest.json" manifest file.</span></span>
   - <span data-ttu-id="c6657-149">按一下 **[儲存]**。</span><span class="sxs-lookup"><span data-stu-id="c6657-149">Click **Save**.</span></span>

8. <span data-ttu-id="c6657-150">儲存設定檔後，Jamf 會顯示 [一般]\*\*\*\* 區段 (在下個螢幕擷取畫面中顯示)。</span><span class="sxs-lookup"><span data-stu-id="c6657-150">After you save the profile, Jamf displays the **General** section shown in the next screen shot.</span></span>

   ![設定一般區段](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - <span data-ttu-id="c6657-152">為設定檔提供顯示 [名稱]\*\*\*\*，以及 [描述]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-152">Provide a display **Name** for the profile and a **Description**.</span></span>
   - <span data-ttu-id="c6657-153">保留 [類別]\*\*\*\* 的預設值，也就是 [無]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-153">Keep the default setting for **Category**, which is **None**.</span></span>
   - <span data-ttu-id="c6657-154">針對 [散發方法]\*\*\*\*，選項為 [自動安裝]\*\*\*\* 或 [可在自助服務中使用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-154">For **Distribution Method**, the options are **Install Automatically** or **Make Available in Self Service**.</span></span>
   - <span data-ttu-id="c6657-155">針對 [層級]\*\*\*\*，選項為 [使用者層級]\*\*\*\* 或 [電腦層級]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-155">For **Level**, the options are **User Level** or **Computer Level**.</span></span>
   - <span data-ttu-id="c6657-156">按一下 **[儲存]**。</span><span class="sxs-lookup"><span data-stu-id="c6657-156">Click **Save**.</span></span>

9. <span data-ttu-id="c6657-157">儲存 [一般] 區段之後，Jamf 會顯示我們範例的「Microsoft Edge Beta 通道」組態設定檔。</span><span class="sxs-lookup"><span data-stu-id="c6657-157">After you save the General section, Jamf shows the "Microsoft Edge Beta Channel" configuration profile set up for our example.</span></span> <span data-ttu-id="c6657-158">在下一個螢幕擷取畫面中，請注意，您可以按一下 [編輯]\*\*\*\* 繼續處理設定檔，或如果您已完成，請按一下 [完成]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-158">In the next screen shot, note that you can keep working the profile by clicking **Edit** or if you're finished, click **Done**.</span></span>

   ![含有選項的新組態設定檔](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > <span data-ttu-id="c6657-160">您可以在儲存設定檔之後以及在另一個 Jamf 工作階段中編輯此設定檔。</span><span class="sxs-lookup"><span data-stu-id="c6657-160">You can edit this profile after it's been saved and in another Jamf session.</span></span> <span data-ttu-id="c6657-161">例如，您可能決定將 [散發方法] 變更為 [可在自助服務中使用]。</span><span class="sxs-lookup"><span data-stu-id="c6657-161">For example, you might decide to change the Distribution Method to Make Available in Self Service.</span></span>

   <span data-ttu-id="c6657-162">若要在 Microsoft Edge 穩定通道上執行追蹤編輯，或將它刪除，請選取後續的 [組態設定檔] 螢幕擷取畫面中顯示的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="c6657-162">To do a follow up edit on the Microsoft Edge Stable Channel, or delete it, select the profile name, shown in the following Configuration Profiles screen shot.</span></span>

   ![組態設定檔清單](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

<span data-ttu-id="c6657-164">建立新的組態設定檔之後，您仍需為設定檔設定**範圍**。</span><span class="sxs-lookup"><span data-stu-id="c6657-164">After you create the new configuration profile you still have to configure the **Scope** for the profile.</span></span>

### <a name="to-configure-the-scope"></a><span data-ttu-id="c6657-165">設定範圍</span><span class="sxs-lookup"><span data-stu-id="c6657-165">To configure the scope</span></span>

1. <span data-ttu-id="c6657-166">針對 [目標]\*\*\*\*，提供下列最小設定：</span><span class="sxs-lookup"><span data-stu-id="c6657-166">For **Targets**, provide the following minimum settings:</span></span>

   - <span data-ttu-id="c6657-167">目標電腦。</span><span class="sxs-lookup"><span data-stu-id="c6657-167">TARGET COMPUTERS.</span></span> <span data-ttu-id="c6657-168">選項為 [特定電腦] 或 [所有電腦]。</span><span class="sxs-lookup"><span data-stu-id="c6657-168">The options are Specific Computers or All Computers.</span></span>
   - <span data-ttu-id="c6657-169">目標使用者。</span><span class="sxs-lookup"><span data-stu-id="c6657-169">TARGET USERS.</span></span> <span data-ttu-id="c6657-170">選項為 [特定使用者] 或 [所有使用者]。</span><span class="sxs-lookup"><span data-stu-id="c6657-170">The options are Specific Users or All Users.</span></span>
   - <span data-ttu-id="c6657-171">按一下 **[儲存]**。</span><span class="sxs-lookup"><span data-stu-id="c6657-171">Click **Save**.</span></span>
2. <span data-ttu-id="c6657-172">針對 [限制]\*\*\*\*，請保留預設設定：[無]。</span><span class="sxs-lookup"><span data-stu-id="c6657-172">For **Limitations**, keep the default setting: None.</span></span> <span data-ttu-id="c6657-173">按一下 [取消]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-173">Click **Cancel**.</span></span>
3. <span data-ttu-id="c6657-174">針對 [排除]\*\*\*\*，請保留預設設定：[無]。</span><span class="sxs-lookup"><span data-stu-id="c6657-174">For **Exclusions**, keep the default setting: None.</span></span> <span data-ttu-id="c6657-175">按一下 [取消]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c6657-175">Click **Cancel**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6657-176">請參閱</span><span class="sxs-lookup"><span data-stu-id="c6657-176">See also</span></span>

- [<span data-ttu-id="c6657-177">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="c6657-177">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c6657-178">使用 Intune 針對 macOS 設定</span><span class="sxs-lookup"><span data-stu-id="c6657-178">Configure for macOS with Intune</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="c6657-179">進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="c6657-179">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="c6657-180">使用 Intune 進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="c6657-180">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
