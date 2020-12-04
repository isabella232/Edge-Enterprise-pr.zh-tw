---
title: 使用 .plist 設定適用於 macOS 的 Microsoft Edge
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 .plist 在 macOS 上設定 Microsoft Edge 原則設定
ms.openlocfilehash: abe110ab3589cc9276f28590273ece2d372be3b8
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194683"
---
# <span data-ttu-id="80d47-103">使用 .plist 針對 macOS 設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="80d47-103">Configure Microsoft Edge policy settings for macOS using a .plist</span></span>

<span data-ttu-id="80d47-104">本文介紹如何使用屬性清單 (.plist) 檔案，在 macOS 上設定 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="80d47-104">This article describes how to configure Microsoft Edge on macOS using a property list (.plist) file.</span></span> <span data-ttu-id="80d47-105">您將了解如何建立此檔案，然後將它部署到 Microsoft Intune。</span><span class="sxs-lookup"><span data-stu-id="80d47-105">You'll learn how to create this file and then deploy it to Microsoft Intune.</span></span>

<span data-ttu-id="80d47-106">如需詳細資訊，請參閱[關於資訊屬性清單檔案](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple 網站) 和[自訂承載資料設定](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1)。</span><span class="sxs-lookup"><span data-stu-id="80d47-106">For more information, see [About Information Property List Files](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple's website) and [Custom payload settings](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1).</span></span>

> [!NOTE]
> <span data-ttu-id="80d47-107">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="80d47-107">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="80d47-108">在 macOS 上設定 Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="80d47-108">Configure Microsoft Edge policies on macOS</span></span>

<span data-ttu-id="80d47-109">第一個步驟是建立 plist。</span><span class="sxs-lookup"><span data-stu-id="80d47-109">The first step is to create your plist.</span></span> <span data-ttu-id="80d47-110">您可以使用任何文字編輯器來建立 plist 檔，也可以使用[終端機建立組態設定檔](#create-a-configuration-profile-using-terminal)。</span><span class="sxs-lookup"><span data-stu-id="80d47-110">You can create the plist file with any text editor or you can use [Terminal to create the configuration profile](#create-a-configuration-profile-using-terminal).</span></span> <span data-ttu-id="80d47-111">不過，使用可為您設定 XML 程式碼格式的工具建立和編輯 plist 檔案會更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="80d47-111">However, it's easier to create and edit a plist file using a tool that formats the XML code for you.</span></span> <span data-ttu-id="80d47-112">*Xcode* 是一套免費的整合式開發環境，您可以從以下位置之一取得：</span><span class="sxs-lookup"><span data-stu-id="80d47-112">*Xcode* is a free integrated development environment that you can get from one of the following locations:</span></span>

- [<span data-ttu-id="80d47-113">Apple 開發人員網站</span><span class="sxs-lookup"><span data-stu-id="80d47-113">Apple developer website</span></span>](https://developer.apple.com/xcode/)
- [<span data-ttu-id="80d47-114">Mac App Store</span><span class="sxs-lookup"><span data-stu-id="80d47-114">Mac App Store</span></span>](https://apps.apple.com/app/xcode/id497799835?mt=12)

<span data-ttu-id="80d47-115">如需支援的原則及其喜好設定金鑰名稱的清單，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="80d47-115">For a list of supported policies and their preference key names, see [Microsoft Edge browser policies reference](microsoft-edge-policies.md).</span></span> <span data-ttu-id="80d47-116">在原則範本檔案 (可從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載) 中，**範例**資料夾中有一個範例 plist (*itadminexample.plist*)。</span><span class="sxs-lookup"><span data-stu-id="80d47-116">In the policy templates file, which can be downloaded from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise), there's an example plist (*itadminexample.plist*) in the **examples** folder.</span></span> <span data-ttu-id="80d47-117">範例檔案包含所有支援的資料類型，您可以自訂這些資料類型以定義原則設定。</span><span class="sxs-lookup"><span data-stu-id="80d47-117">The example file contains all supported data types that you can customize to define your policy settings.</span></span> 

<span data-ttu-id="80d47-118">建立 plist 內容後的下一步，是使用 Microsoft Edge 喜好設定網域 *com.microsoft.Edge* 來命名它。</span><span class="sxs-lookup"><span data-stu-id="80d47-118">The next step after you create the contents of your plist, is to name it using the Microsoft Edge preference domain, *com.microsoft.Edge*.</span></span> <span data-ttu-id="80d47-119">此名稱區分大小寫，不應包括您設為目標的通道，因為它適用於所有 Microsoft Edge 通道。</span><span class="sxs-lookup"><span data-stu-id="80d47-119">The name is case sensitive and should not include the channel you are targeting because it applies to all Microsoft Edge channels.</span></span> <span data-ttu-id="80d47-120">Plist 檔案名必須為 **_com.microsoft.Edge.plist_**。</span><span class="sxs-lookup"><span data-stu-id="80d47-120">The plist file name must be **_com.microsoft.Edge.plist_**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80d47-121">從組建 78.0.249.2 開始，macOS 上的所有 Microsoft Edge 通道都從 **com.microsoft.Edge** 喜好設定網域讀取。</span><span class="sxs-lookup"><span data-stu-id="80d47-121">Starting with build 78.0.249.2, all Microsoft Edge channels on macOS read from the **com.microsoft.Edge** preference domain.</span></span> <span data-ttu-id="80d47-122">所有舊版都從通道專屬網域讀取，例如 **com.microsoft.Edge.Dev** 適用於 Dev 通道。</span><span class="sxs-lookup"><span data-stu-id="80d47-122">All prior releases read from a channel specific domain, such as **com.microsoft.Edge.Dev** for Dev channel.</span></span>

<span data-ttu-id="80d47-123">最後一步是使用您偏好的 MDM 提供者 (如 Microsoft Intune) 將 plist 部署到使用者的 Mac 裝置。</span><span class="sxs-lookup"><span data-stu-id="80d47-123">The last step is to deploy your plist to your users' Mac devices using your preferred MDM provider, such as Microsoft Intune.</span></span> <span data-ttu-id="80d47-124">如需相關指示，請參閱[部署 plist](#deploy-your-plist)。</span><span class="sxs-lookup"><span data-stu-id="80d47-124">For instructions see [Deploy your plist](#deploy-your-plist).</span></span>

### <span data-ttu-id="80d47-125">使用終端機建立組態設定檔</span><span class="sxs-lookup"><span data-stu-id="80d47-125">Create a configuration profile using Terminal</span></span>

1. <span data-ttu-id="80d47-126">在終端機中，使用以下命令，以您的偏好設定在桌面建立一個適用於 Microsoft Edge 的 plist：</span><span class="sxs-lookup"><span data-stu-id="80d47-126">In Terminal, use the following command to create a plist for Microsoft Edge on your desktop with your preferred settings:</span></span>

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. <span data-ttu-id="80d47-127">將 plist 從二進位格式轉換為純文字格式：</span><span class="sxs-lookup"><span data-stu-id="80d47-127">Convert the plist from binary to plain text format:</span></span>

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

<span data-ttu-id="80d47-128">轉換檔案後，請驗證原則資料是否正確，並包含組態設定檔所需的設定。</span><span class="sxs-lookup"><span data-stu-id="80d47-128">After converting the file verify that your policy data is correct and contains the settings you want for your configuration profile.</span></span>

> [!NOTE]
> <span data-ttu-id="80d47-129">只有鍵值對應位於 plist 或 xml 檔的內容中。</span><span class="sxs-lookup"><span data-stu-id="80d47-129">Only key value pairs should be in the contents of the plist or xml file.</span></span> <span data-ttu-id="80d47-130">在將檔案上傳到 Intune 之前，請從檔案中移除所有 \<plist> 和 \<dict> 值以及 xml 標頭。</span><span class="sxs-lookup"><span data-stu-id="80d47-130">Prior to uploading your file into Intune remove all the \<plist> and \<dict> values, and xml headers from your file.</span></span> <span data-ttu-id="80d47-131">檔案應僅包含鍵值對。</span><span class="sxs-lookup"><span data-stu-id="80d47-131">The file should only contain key value pairs.</span></span>

## <span data-ttu-id="80d47-132">部署 plist</span><span class="sxs-lookup"><span data-stu-id="80d47-132">Deploy your plist</span></span>

<span data-ttu-id="80d47-133">對於 Microsoft Intune，建立以 macOS 平台為目標的新裝置組態設定檔，然後選取*喜好設定檔案*設定檔案類型。</span><span class="sxs-lookup"><span data-stu-id="80d47-133">For Microsoft Intune create a new device configuration profile targeting the macOS platform and select the *Preference file* profile type.</span></span> <span data-ttu-id="80d47-134">將 **com.microsoft.Edge** 設為目標以做為喜好設定網域名稱，並上傳您的 plist。</span><span class="sxs-lookup"><span data-stu-id="80d47-134">Target **com.microsoft.Edge** as the preference domain name and upload your plist.</span></span> <span data-ttu-id="80d47-135">如需詳細資訊，請參閱[使用 Microsoft Intune 將屬性清單檔案新增至 macOS 裝置](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos)。</span><span class="sxs-lookup"><span data-stu-id="80d47-135">For more information see [Add a property list file to macOS devices using Microsoft Intune](https://docs.microsoft.com/intune/configuration/preference-file-settings-macos).</span></span>

<span data-ttu-id="80d47-136">對於 Jamf，將 .plist 檔案上載為*自訂設定*承載。</span><span class="sxs-lookup"><span data-stu-id="80d47-136">For Jamf upload the .plist file as a *Custom Settings* payload.</span></span>

## <span data-ttu-id="80d47-137">請參閱</span><span class="sxs-lookup"><span data-stu-id="80d47-137">See also</span></span>

- [<span data-ttu-id="80d47-138">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="80d47-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="80d47-139">使用 Jamf 針對 macOS 設定</span><span class="sxs-lookup"><span data-stu-id="80d47-139">Configure for macOS with Jamf</span></span>](configure-microsoft-edge-on-mac-jamf.md)
- [<span data-ttu-id="80d47-140">進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="80d47-140">Configure for Windows</span></span>](configure-microsoft-edge.md)
- [<span data-ttu-id="80d47-141">使用 Intune 進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="80d47-141">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
