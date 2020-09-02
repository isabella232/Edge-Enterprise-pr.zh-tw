---
title: 使用 .plist 設定適用於 macOS 的 Microsoft Edge
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 .plist 在 macOS 上設定 Microsoft Edge 原則設定
ms.openlocfilehash: 84469a4f84deeee0e47b6d8899426fa36cf345aa
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979432"
---
# <span data-ttu-id="6b1d3-103">使用 .plist 針對 macOS 設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="6b1d3-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="6b1d3-104">本文介紹如何使用屬性清單 (.plist) 檔案，在 macOS 上設定 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="6b1d3-105">您將了解如何建立此檔案，然後將它部署到 Microsoft Intune。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="6b1d3-106">如需詳細資訊，請參閱[關於資訊屬性清單檔案](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple 網站) 和[自訂承載資料設定](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="6b1d3-107">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="6b1d3-108">在 macOS 上設定 Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="6b1d3-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="6b1d3-109">第一個步驟是建立 plist。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-109">The first step is to create your plist.</span></span> <span data-ttu-id="6b1d3-110">您可以使用任何文字編輯器來建立 plist 檔，也可以使用[終端機建立組態設定檔](#create-a-configuration-profile-using-terminal)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="6b1d3-111">不過，使用可為您設定 XML 程式碼格式的工具建立和編輯 plist 檔案會更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="6b1d3-112">*Xcode* 是一套免費的整合式開發環境，您可以從以下位置之一取得：</span><span class="sxs-lookup"><span data-stu-id="6b1d3-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="6b1d3-113">Apple 開發人員網站</span><span class="sxs-lookup"><span data-stu-id="6b1d3-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="6b1d3-114">Mac App Store</span><span class="sxs-lookup"><span data-stu-id="6b1d3-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="6b1d3-115">如需支援的原則及其喜好設定金鑰名稱的清單，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="6b1d3-116">在原則範本檔案 (可從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載) 中，**範例**資料夾中有一個範例 plist (*itadminexample.plist*)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="6b1d3-117">範例檔案包含所有支援的資料類型，您可以自訂這些資料類型以定義原則設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="6b1d3-118">建立 plist 內容後的下一步，是使用 Microsoft Edge 喜好設定網域 *com.microsoft.Edge* 來命名它。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="6b1d3-119">此名稱區分大小寫，不應包括您設為目標的通道，因為它適用於所有 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="6b1d3-120">Plist 檔案名必須為 **_com.microsoft.Edge.plist_**。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="6b1d3-121">從組建 78.0.249.2 開始，macOS 上的所有 Microsoft Edge 通道都從 **com.microsoft.Edge** 喜好設定網域讀取。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="6b1d3-122">所有舊版都從通道專屬網域讀取，例如 **com.microsoft.Edge.Dev** 適用於 Dev 通道。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="6b1d3-123">最後一步是使用您偏好的 MDM 提供者 (如 Microsoft Intune) 將 plist 部署到使用者的 Mac 裝置。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="6b1d3-124">如需相關指示，請參閱[部署 plist](#deploy-your-plist)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <span data-ttu-id="6b1d3-125">使用終端機建立組態設定檔</span><span class="sxs-lookup"><span data-stu-id="6b1d3-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="6b1d3-126">在終端機中，使用以下命令，以您的偏好設定在桌面建立一個適用於 Microsoft Edge 的 plist：</span><span class="sxs-lookup"><span data-stu-id="6b1d3-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="6b1d3-127">將 plist 從二進位格式轉換為純文字格式：</span><span class="sxs-lookup"><span data-stu-id="6b1d3-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```
<span data-ttu-id="6b1d3-128">轉換檔案後，請驗證原則資料是否正確，並包含組態設定檔所需的設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="6b1d3-129">只有鍵值對應位於 plist 或 xml 檔的內容中。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="6b1d3-130">在將檔案上傳到 Intune 之前，請從檔案中移除所有 \<plist> 和 \<dict> 值以及 xml 標頭。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="6b1d3-131">檔案應僅包含鍵值對。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-131">The file should only contain key value pairs.</span></span>

## <span data-ttu-id="6b1d3-132">部署 plist</span><span class="sxs-lookup"><span data-stu-id="6b1d3-132">Deploy your plist</span></span>

<span data-ttu-id="6b1d3-133">對於 Microsoft Intune，建立以 macOS 平台為目標的新裝置組態設定檔，然後選取*喜好設定檔案*設定檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="6b1d3-134">將 **com.microsoft.Edge** 設為目標以做為喜好設定網域名稱，並上傳您的 plist。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="6b1d3-135">如需詳細資訊，請參閱[使用 Microsoft Intune 將屬性清單檔案新增至 macOS 裝置](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos)。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="6b1d3-136">對於 Jamf，將 .plist 檔案上載為*自訂設定*承載。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <span data-ttu-id="6b1d3-137">常見問題集</span><span class="sxs-lookup"><span data-stu-id="6b1d3-137">Frequently Asked Questions</span></span>

### <span data-ttu-id="6b1d3-138">是否可以將 Microsoft Edge 設定為使用主喜好設定？</span><span class="sxs-lookup"><span data-stu-id="6b1d3-138">Can Microsoft Edge be configured to use master preferences?</span></span>

<span data-ttu-id="6b1d3-139">是，您可以將 Microsoft Edge 設定為使用主喜好設定檔案。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-139">Yes, you can configure Microsoft Edge to use a master preferences file.</span></span>

<span data-ttu-id="6b1d3-140">主喜好設定檔案可讓您在部署 Microsoft Edge 時設定瀏覽器使用者設定檔的預設設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-140">A master preferences file lets you configure default settings for a browser user profile when Microsoft Edge is deployed.</span></span> <span data-ttu-id="6b1d3-141">您還可以使用主喜好設定檔案在未受裝置管理系統管理的電腦上套用設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-141">You can also use a master preferences file to apply settings on computers that aren't managed by a device management system.</span></span> <span data-ttu-id="6b1d3-142">這些設定會在使用者首次執行瀏覽器時，套用至使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-142">These settings are applied to the user’s profile the first time the user runs the browser.</span></span> <span data-ttu-id="6b1d3-143">使用者執行瀏覽器後，不會套用對主喜好設定檔案所做的變更。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-143">After the user runs the browser, changes to the master preferences file aren’t applied.</span></span> <span data-ttu-id="6b1d3-144">使用者可以從瀏覽器中的主喜好設定變更設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-144">A user can change settings from the master preferences in the browser.</span></span> <span data-ttu-id="6b1d3-145">如果要在瀏覽器首次執行後強制設定或變更設定，則必須使用原則。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-145">If you want to make a setting mandatory or change a setting after the first run of the browser, you must use a policy.</span></span>

<span data-ttu-id="6b1d3-146">主喜好設定檔案允許您自訂瀏覽器的許多不同設定和喜好設定，包括與其他以 Chromium 為基礎之瀏覽器共用且特定於 Microsoft Edge 的項目。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-146">A master preferences file lets you to customize many different settings and preferences for the browser, including those shared with other Chromium based browsers and specific to Microsoft Edge.</span></span>  <span data-ttu-id="6b1d3-147">可以使用主喜好設定檔案來設定與原則相關的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-147">Policy related preferences can be configured using the master preferences file.</span></span> <span data-ttu-id="6b1d3-148">如果設定了原則，並且存在對應的主喜好設定集，優先採用原則設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-148">In cases where a policy is set and there’s a corresponding master preference set, the policy setting takes precedence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b1d3-149">所有可用的喜好設定可能與 Microsoft Edge 術語和命名慣例不一致。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-149">All the available preferences might not be consistent with Microsoft Edge terminology and naming conventions.</span></span>  <span data-ttu-id="6b1d3-150">無法保證這些喜好設定在未來版本中可繼續如預期運作。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-150">There’s no guarantee that these preferences will continue to work as expected in future releases.</span></span> <span data-ttu-id="6b1d3-151">更新版本中可能會變更或忽略喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-151">Preferences might be changed or ignored in later versions.</span></span>

<span data-ttu-id="6b1d3-152">主喜好設定檔案是使用 JSON 標記格式化的文字檔案。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-152">A master preferences file is a text file that’s formatted using JSON markup.</span></span> <span data-ttu-id="6b1d3-153">此檔案需要新增到與 msedge.exe 可執行檔相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-153">This file needs to be added to the same directory as the msedge.exe executable.</span></span> <span data-ttu-id="6b1d3-154">對於 macOS 上的系統範圍企業部署，這通常是：「*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*」或「*/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*」。</span><span class="sxs-lookup"><span data-stu-id="6b1d3-154">For system wide enterprise deployments on macOS this is typically: “*~/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*" or "*/Library/Application Support/Microsoft/Microsoft Edge Master Preferences*”.</span></span>

## <span data-ttu-id="6b1d3-155">也請參閱</span><span class="sxs-lookup"><span data-stu-id="6b1d3-155">See also</span></span>

- [<span data-ttu-id="6b1d3-156">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="6b1d3-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="6b1d3-157">使用 Jamf 針對 macOS 設定</span><span class="sxs-lookup"><span data-stu-id="6b1d3-157">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="6b1d3-158">進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="6b1d3-158">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="6b1d3-159">使用 Intune 進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="6b1d3-159">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
