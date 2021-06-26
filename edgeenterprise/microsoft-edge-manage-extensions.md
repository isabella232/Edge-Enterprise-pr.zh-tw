---
title: 管理企業中的 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 04/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 管理企業中的 Microsoft Edge 擴充功能
ms.openlocfilehash: c123deaed638004b380308fd0d29b40b132dbfd5
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618067"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a><span data-ttu-id="196fe-103">管理企業中的 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="196fe-103">Manage Microsoft Edge extensions in the enterprise</span></span>

<span data-ttu-id="196fe-104">本文針對在組織中管理 Microsoft Edge 擴充功能的系統管理員，提供最佳作法指導方針。</span><span class="sxs-lookup"><span data-stu-id="196fe-104">This article provides best practice guidance for admins who are managing Microsoft Edge extensions in their organizations.</span></span> <span data-ttu-id="196fe-105">您可以使用本文中的資訊來開發管理貴組織中擴充功能的策略。</span><span class="sxs-lookup"><span data-stu-id="196fe-105">You can use the information in this article to develop a strategy for managing extensions in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="196fe-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="196fe-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="introduction"></a><span data-ttu-id="196fe-107">簡介</span><span class="sxs-lookup"><span data-stu-id="196fe-107">Introduction</span></span>

<span data-ttu-id="196fe-108">組織想要保護公司與使用者資料，並評估瀏覽器擴充功能，以確保它們安全且與企業相關。</span><span class="sxs-lookup"><span data-stu-id="196fe-108">Organizations want to protect corporate and user data and evaluate browser extensions to ensure that they’re safe and relevant to their enterprise.</span></span> <span data-ttu-id="196fe-109">系統管理員想要：</span><span class="sxs-lookup"><span data-stu-id="196fe-109">Admins want to:</span></span>

- <span data-ttu-id="196fe-110">防止安裝錯誤的應用程式和擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-110">Prevent bad apps and extensions from being installed.</span></span>
- <span data-ttu-id="196fe-111">保留使用者完成工作所需的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-111">Keep extensions that users need to do their job.</span></span>
- <span data-ttu-id="196fe-112">管理使用者和公司資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="196fe-112">Manage access to user and company data.</span></span>  

<span data-ttu-id="196fe-113">本文是協助系統管理員管理擴充功能系列的第一篇文章，可為使用者提供安全且有生產力的體驗。</span><span class="sxs-lookup"><span data-stu-id="196fe-113">This article is the first in a series that that helps admins manage extensions to provide a safe and productive experience for their users.</span></span> <span data-ttu-id="196fe-114">本系列將逐步介紹不同的選項，並協助您挑選管理擴充功能的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="196fe-114">This series walks through the different options and helps you pick the best method for managing extensions.</span></span> <span data-ttu-id="196fe-115">本系列包含下列文章：</span><span class="sxs-lookup"><span data-stu-id="196fe-115">The series consists of the following articles:</span></span>

- <span data-ttu-id="196fe-116">[管理企業中的 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="196fe-116">[Manage Microsoft Edge extensions in the enterprise](microsoft-edge-manage-extensions.md).</span></span> <span data-ttu-id="196fe-117">建立管理擴充功能的策略，並設定管理瀏覽器所需的系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="196fe-117">Create a strategy to manage extensions and set up administrative templates required for managing the browser.</span></span>
- <span data-ttu-id="196fe-118">[使用群組原則來管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="196fe-118">[Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md).</span></span> <span data-ttu-id="196fe-119">使用群組原則管理擴充功能的選項。</span><span class="sxs-lookup"><span data-stu-id="196fe-119">Options using group policies to manage extensions.</span></span>
- <span data-ttu-id="196fe-120">[建立 Web Store 以託管 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-webstore.md)。</span><span class="sxs-lookup"><span data-stu-id="196fe-120">[Create a web store to host Microsoft Edge extensions](microsoft-edge-manage-extensions-webstore.md).</span></span> <span data-ttu-id="196fe-121">建立和託管擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-121">Create and host extensions.</span></span>
- <span data-ttu-id="196fe-122">[適用於 Microsoft Edge 擴充功能的常見問題集](microsoft-edge-manage-extensions-faq.md)。</span><span class="sxs-lookup"><span data-stu-id="196fe-122">[FAQ for Microsoft Edge Extensions](microsoft-edge-manage-extensions-faq.md).</span></span> <span data-ttu-id="196fe-123">常見問題集。</span><span class="sxs-lookup"><span data-stu-id="196fe-123">Frequently Asked Questions.</span></span>

## <a name="things-to-consider-when-managing-extensions"></a><span data-ttu-id="196fe-124">管理擴充功能時要考慮的事</span><span class="sxs-lookup"><span data-stu-id="196fe-124">Things to consider when managing extensions</span></span>

<span data-ttu-id="196fe-125">您的使用者需要存取特定應用程式、網站和擴充功能，以執行其工作，同時保護使用者和公司資料。</span><span class="sxs-lookup"><span data-stu-id="196fe-125">Your users need access to certain apps, sites, and extensions to do their jobs while at the same time protecting users and company data.</span></span> <span data-ttu-id="196fe-126">有效的安全性策略需要向企業提出正確的問題，以及擴充功能如何配合貴公司的需求。</span><span class="sxs-lookup"><span data-stu-id="196fe-126">An effective security strategy involves asking the right questions for your enterprise and how extensions can fit your company’s needs.</span></span> <span data-ttu-id="196fe-127">需要詢問的一些關鍵問題包括：</span><span class="sxs-lookup"><span data-stu-id="196fe-127">Some of the key questions to ask are:</span></span>

- <span data-ttu-id="196fe-128">我必須遵守哪些法規和合規性措施？</span><span class="sxs-lookup"><span data-stu-id="196fe-128">What regulations and compliance measures do I need to adhere to?</span></span>
- <span data-ttu-id="196fe-129">某些擴充功能是否要求過於廣泛的權限，這可能會違反我公司的資料安全性原則？</span><span class="sxs-lookup"><span data-stu-id="196fe-129">Do some extensions ask for overly broad permissions, which could go against my company’s data security policies?</span></span>
- <span data-ttu-id="196fe-130">我的使用者裝置上儲存的使用者或公司資料有多少？</span><span class="sxs-lookup"><span data-stu-id="196fe-130">How much user or corporate data is stored on my users’ devices?</span></span>

<span data-ttu-id="196fe-131">當您回答這些問題時，您可以使用 Microsoft Edge 提供的細微策略：</span><span class="sxs-lookup"><span data-stu-id="196fe-131">As you answer these questions, you can use the granular policies that Microsoft Edge provides to:</span></span>

- <span data-ttu-id="196fe-132">根據資料保護原則封鎖或允許使用者電腦上的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-132">Block or allow extensions on users’ computers based on your data protection policies.</span></span>
- <span data-ttu-id="196fe-133">在使用者的裝置上強制安裝擴充功能，讓使用者擁有所需的生產力工具。</span><span class="sxs-lookup"><span data-stu-id="196fe-133">Force-install extensions on your users' devices so they have tools that they need to be productive.</span></span>
- <span data-ttu-id="196fe-134">允許清單或封鎖清單的擴充功能，以允許使用者執行其工作所需的最小權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-134">Allowlist or blocklist extensions to allow the least amount of rights needed for your users to do their  work.</span></span>

<span data-ttu-id="196fe-135">管理擴充功能的傳統模型會針對特定擴充功能使用允許清單和封鎖清單方法。</span><span class="sxs-lookup"><span data-stu-id="196fe-135">The traditional model for managing extensions uses the allowlist and blocklist approach for specific extensions.</span></span> <span data-ttu-id="196fe-136">不過，Microsoft Edge 也讓您管理擴充功能要求的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-136">However, Microsoft Edge also lets you manage the permissions requested by extensions.</span></span> <span data-ttu-id="196fe-137">使用此模型，您可以決定要允許擴充功能在電腦和裝置上使用哪些權限，然後根據您的需求來實作允許或封鎖擴充的全域原則。</span><span class="sxs-lookup"><span data-stu-id="196fe-137">Using this model, you can decide which rights and permissions you want to allow extensions to use on your computers and devices, and then implement a global policy that allows or block extensions based on your requirements.</span></span>  

## <a name="understand-extension-permissions"></a><span data-ttu-id="196fe-138">了解擴充功能權限</span><span class="sxs-lookup"><span data-stu-id="196fe-138">Understand extension permissions</span></span>

<span data-ttu-id="196fe-139">擴充功能需要權限才能在裝置或網頁上進行變更，以正確執行。</span><span class="sxs-lookup"><span data-stu-id="196fe-139">Extensions can require rights to make changes on a device or a web page to run properly.</span></span> <span data-ttu-id="196fe-140">這些存取權限稱為權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-140">These rights are called permissions.</span></span> <span data-ttu-id="196fe-141">開發人員必須列出需要哪些權限並存取其擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-141">Developers must list what rights and access their extensions need.</span></span> <span data-ttu-id="196fe-142">權限有兩個主要類別，而許多擴充功能需要下列兩種權限：</span><span class="sxs-lookup"><span data-stu-id="196fe-142">There are two main categories for permissions, and many extensions need both of the following permissions:</span></span>

- <span data-ttu-id="196fe-143">託管權限需要擴充功能列出它可檢視或修改的網頁。</span><span class="sxs-lookup"><span data-stu-id="196fe-143">Host permissions require the extension to list webpages it may view or modify.</span></span>
- <span data-ttu-id="196fe-144">裝置權限是擴充功能在其執行的裝置上所需的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-144">Device permissions are the rights needed by an extension on the device where it’s running.</span></span>

<span data-ttu-id="196fe-145">這些權限的一些範例包括：存取 USB 連接埠、儲存空間或檢視畫面，以及與原生程式通訊。</span><span class="sxs-lookup"><span data-stu-id="196fe-145">Some examples of these permissions are: access to a USB port, storage or viewing screen, and communicating with native programs.</span></span>  

## <a name="get-ready-to-manage-extensions"></a><span data-ttu-id="196fe-146">準備就緒管理擴充功能</span><span class="sxs-lookup"><span data-stu-id="196fe-146">Get ready to manage extensions</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="196fe-147">開始之前</span><span class="sxs-lookup"><span data-stu-id="196fe-147">Before you begin</span></span>

<span data-ttu-id="196fe-148">擴充功能選項假設您已為使用者管理 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="196fe-148">The extensions options assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="196fe-149">有關設定適用於 Microsoft Edge 原則的系統管理範本，請參閱：</span><span class="sxs-lookup"><span data-stu-id="196fe-149">For more information about setting up administrative templates for Microsoft Edge policies, see:</span></span>

-   [<span data-ttu-id="196fe-150">在 Windows 上設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="196fe-150">Configure Microsoft Edge policy settings on Windows</span></span>](/DeployEdge/configure-microsoft-edge)
-   [<span data-ttu-id="196fe-151">使用 Intune 進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="196fe-151">Configure for Windows with Intune</span></span>](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [<span data-ttu-id="196fe-152">使用行動裝置管理，進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="196fe-152">Configure for Windows with Mobile Device Management</span></span>](/deployedge/configure-edge-with-mdm)
-   [<span data-ttu-id="196fe-153">使用 .plist 設定 macOS</span><span class="sxs-lookup"><span data-stu-id="196fe-153">Configure for macOS using a .plist</span></span>](/deployedge/configure-microsoft-edge-on-mac)
-   [<span data-ttu-id="196fe-154">使用 Jamf 進行 macOS 的設定</span><span class="sxs-lookup"><span data-stu-id="196fe-154">Configure for macOS with Jamf</span></span>](/deployedge/configure-microsoft-edge-on-mac-jamf)

<span data-ttu-id="196fe-155">本文內容的設定步驟適用於 Windows，關於 MAC/Linux 中的對應實作，請參閱 Microsoft Edge 瀏覽器原則參考。</span><span class="sxs-lookup"><span data-stu-id="196fe-155">The configuration steps in this article are for Windows, for the corresponding implementation in MAC/Linux, see the Microsoft Edge browser policy reference.</span></span>

## <a name="decide-which-extensions-to-allow"></a><span data-ttu-id="196fe-156">決定允許哪些擴充功能</span><span class="sxs-lookup"><span data-stu-id="196fe-156">Decide which extensions to allow</span></span>

<span data-ttu-id="196fe-157">大多數組織都應該根據權限以及有權存取的網站來管理擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-157">Most organizations should manage extensions by their permissions and what websites they have access to.</span></span> <span data-ttu-id="196fe-158">這個方法更安全、更容易管理，而且對大型組織是可調整的。</span><span class="sxs-lookup"><span data-stu-id="196fe-158">This method is more secure, easier to manage, and is scalable for large organizations.</span></span>  

- <span data-ttu-id="196fe-159">封鎖/允許權限 – 可讓您根據擴充功能所需的權限來控制擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-159">Blocked/allowed permissions – Lets you control extensions by the permissions they need.</span></span>
- <span data-ttu-id="196fe-160">執行階段封鎖主機 – 可讓您控制這些擴充功能可以存取的網站。</span><span class="sxs-lookup"><span data-stu-id="196fe-160">Runtime block hosts – Lets you to control what websites these extensions can access.</span></span>

<span data-ttu-id="196fe-161">使用這個方法可節省時間，因為您只需要設定一次。</span><span class="sxs-lookup"><span data-stu-id="196fe-161">Using this approach saves time because you only need to set these once.</span></span> <span data-ttu-id="196fe-162">而使用執行階段主機原則時，您最重要的網站會受到保護。還有其他選項，例如：</span><span class="sxs-lookup"><span data-stu-id="196fe-162">And with the run-time hosts policy, your most important sites will be protected.There are other options as well such as:</span></span>

-   <span data-ttu-id="196fe-163">強制安裝擴充功能 – 讓您以無訊息方式安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-163">Force install extensions – Lets you install extensions silently.</span></span>
-   <span data-ttu-id="196fe-164">允許清單/封鎖清單 (視需要) - 決定允許安裝哪些擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-164">Allowlist/blocklist (if required) – Decide what extensions are allowed to be installed.</span></span>

<span data-ttu-id="196fe-165">使用下列步驟做為指南，決定貴組織決定允許哪些擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-165">Use the following steps as a guide to decide which extensions to allow in your organization.</span></span>

1. <span data-ttu-id="196fe-166">建立員工電腦上所需的擴充功能清單。</span><span class="sxs-lookup"><span data-stu-id="196fe-166">Create a list of which extensions employees need on their computers.</span></span> <span data-ttu-id="196fe-167">在測試環境中測試擴充功能，以診斷內部應用程式的任何相容性問題。</span><span class="sxs-lookup"><span data-stu-id="196fe-167">Test the extensions in a test environment to diagnose any compatibility issues with internal apps.</span></span>
2. <span data-ttu-id="196fe-168">選擇需要更安全的網站。</span><span class="sxs-lookup"><span data-stu-id="196fe-168">Choose which sites need to be more secure.</span></span>

   - <span data-ttu-id="196fe-169">了解您需要封鎖哪些敏感性的內部網站或網域，以禁止擴充功能變更或讀取資料。</span><span class="sxs-lookup"><span data-stu-id="196fe-169">Find out which sensitive internal websites or domains you need to block extensions from making changes to or reading data from.</span></span>  
   - <span data-ttu-id="196fe-170">當擴展程式執行時，封鎖 API 呼叫，以防止存取這些網站。</span><span class="sxs-lookup"><span data-stu-id="196fe-170">Prevent access to these sites by blocking the API calls when the extension is run.</span></span> <span data-ttu-id="196fe-171">這包括封鎖 Web 要求、讀取 Cookie、JavaScript 注入、XHR 等等。</span><span class="sxs-lookup"><span data-stu-id="196fe-171">This includes blocking web requests, reading cookies, JavaScript injection, XHR, and so on.</span></span>

3. <span data-ttu-id="196fe-172">決定執行這些擴充功能所需的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-172">Determine which permissions are required for these extensions to run.</span></span> <span data-ttu-id="196fe-173">找出哪些權限會對使用者造成潛在風險。</span><span class="sxs-lookup"><span data-stu-id="196fe-173">Identify which permissions pose potential risks to your users.</span></span>

   - <span data-ttu-id="196fe-174">稽核使用者已安裝的擴充功能，並查看他們所需的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-174">Audit the extensions your users have installed and see what permissions they need.</span></span> <span data-ttu-id="196fe-175">您可以在擴充功能的程式碼中查看 Web App 資訊清單 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="196fe-175">You can look at the web app manifest JSON file in the code of the extension.</span></span> <span data-ttu-id="196fe-176">請執行下列步驟，查看擴充功能需要哪些權限：</span><span class="sxs-lookup"><span data-stu-id="196fe-176">Take the following steps to see what rights the extension needs:</span></span>

     - <span data-ttu-id="196fe-177">從 [Microsoft Edge 外掛程式](https://microsoftedge.microsoft.com/addons/)網站或 [Chrome 線上應用程式商店](https://chrome.google.com/webstore) 安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-177">Install the extension from the [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/) website or the [Chrome Web Store](https://chrome.google.com/webstore).</span></span>
     - <span data-ttu-id="196fe-178">測試擴充功能，並了解擴充功能在貴組織中運作方式。</span><span class="sxs-lookup"><span data-stu-id="196fe-178">Test the extension and understand how it works in your organization.</span></span>
     - <span data-ttu-id="196fe-179">瀏覽至 *edge://extensions*，以檢閱擴充功能所需的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-179">Review the permissions that the extension requires by navigating to *edge://extensions*.</span></span> <span data-ttu-id="196fe-180">例如，以下螢幕擷取畫面中顯示的 Microsoft Office 擴充功能會要求「讀取您的瀏覽歷程記錄」和「顯示通知」的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-180">For example, the Microsoft Office extension shown in the next screenshot requests the permissions "Read your browsing history" and "Display notifications".</span></span> <span data-ttu-id="196fe-181">將此擴充功能的實用性與要求的權限等級進行權衡。</span><span class="sxs-lookup"><span data-stu-id="196fe-181">Weigh the usefulness of this extension against the level of permissions it requests.</span></span> <span data-ttu-id="196fe-182">核准貴組織的擴充功能後，請使用下列工具進行管理。</span><span class="sxs-lookup"><span data-stu-id="196fe-182">After you approve an extension for your organization, manage it using the following tools.</span></span>
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="具有權限的 Microsoft Office 擴充功能。":::

   - <span data-ttu-id="196fe-184">您也可以在貴組織中核准擴充功能之前，先驗證使用者要求的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-184">You can also validate the extensions requested by users in your organization before approving them in the organization.</span></span> <span data-ttu-id="196fe-185">擴充功能使用的一些權限可能模糊不清。</span><span class="sxs-lookup"><span data-stu-id="196fe-185">Some of the permissions that extensions use can be vague.</span></span> <span data-ttu-id="196fe-186">針對商務關鍵型應用程式，您可以直接與應用程式開發人員或廠商連絡，以取得擴充功能詳細資訊或查看原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="196fe-186">For business-critical apps, you can reach out to the app developer or vendor directly to get more information about the extension or look at the source code.</span></span> <span data-ttu-id="196fe-187">他們應該能夠詳述擴充功能可在裝置和網站上進行的變更。</span><span class="sxs-lookup"><span data-stu-id="196fe-187">They should be able to detail the changes that the extension can make on devices and websites.</span></span>
   - <span data-ttu-id="196fe-188">檢閱宣告權限清單，該清單列出擴充功能可使用的所有權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-188">Review the Declare Permissions list, which lists all permissions an extension can use.</span></span> <span data-ttu-id="196fe-189">從這份清單中，您可以決定要在貴組織中允許哪些權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-189">From this list, you can decide which permissions you want to allow in your organization.</span></span>

4. <span data-ttu-id="196fe-190">從您收集的資料建立主清單。此清單會包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="196fe-190">Create a master list from the data you collected.This list will include the following information:</span></span>

   - <span data-ttu-id="196fe-191">**必要的擴充功能**。</span><span class="sxs-lookup"><span data-stu-id="196fe-191">**Required extensions**.</span></span> <span data-ttu-id="196fe-192">這份清單可以按照部門、辦公室位置或其他相關資訊來組織。</span><span class="sxs-lookup"><span data-stu-id="196fe-192">This list could be organized by department, office location, or other relevant information.</span></span>
   - <span data-ttu-id="196fe-193">**擴充功能允許清單**。</span><span class="sxs-lookup"><span data-stu-id="196fe-193">**Extension Allowlist**.</span></span> <span data-ttu-id="196fe-194">具有可能封鎖但允許執行之權限的必要擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-194">Required extensions with permissions that may be blocked but will be allowed to run.</span></span> <span data-ttu-id="196fe-195">使用者需要這些擴充功能，或透過與廠商的交談確定不會帶來風險。</span><span class="sxs-lookup"><span data-stu-id="196fe-195">These extensions are needed by your users or are determined to not be a risk through conversations with the vendor.</span></span>
   - <span data-ttu-id="196fe-196">**擴充功能封鎖清單**。</span><span class="sxs-lookup"><span data-stu-id="196fe-196">**Extension Blocklist**.</span></span> <span data-ttu-id="196fe-197">被封鎖安裝的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-197">Extensions that are blocked from installation.</span></span> <span data-ttu-id="196fe-198">此清單中的擴充功能具有不允許執行的權限。</span><span class="sxs-lookup"><span data-stu-id="196fe-198">The extensions in this list have the permissions that aren’t allowed to run.</span></span> <span data-ttu-id="196fe-199">也包含要保持安全且不允許擴充功能存取的核心網站和網域。</span><span class="sxs-lookup"><span data-stu-id="196fe-199">Also include the core sites and domains to be kept secure and not allowed extension access.</span></span> <span data-ttu-id="196fe-200">之後，您可以將此封鎖清單與已有的其他清單進行比較。</span><span class="sxs-lookup"><span data-stu-id="196fe-200">Later you can compare this blocklist to others you already have in place.</span></span> <span data-ttu-id="196fe-201">您可能會發現您可以輕鬆設定目前的封鎖清單原則。</span><span class="sxs-lookup"><span data-stu-id="196fe-201">You might find that you can relax your current blocklist policies.</span></span>

5. <span data-ttu-id="196fe-202">向專案關係人及 IT 小組展示您的清單以取得支持。</span><span class="sxs-lookup"><span data-stu-id="196fe-202">Present your list to your stakeholders and the IT team to get buy in.</span></span>
6. <span data-ttu-id="196fe-203">在實驗室測試新原則或在貴組織中進行小型試驗。</span><span class="sxs-lookup"><span data-stu-id="196fe-203">Test out the new policy in your lab or with a small pilot in your organization.</span></span>
7. <span data-ttu-id="196fe-204">分階段向員工推出這些新原則。</span><span class="sxs-lookup"><span data-stu-id="196fe-204">Roll out these new sets of policies to employees in phases.</span></span> <span data-ttu-id="196fe-205">如需詳細資訊，請參閱[使用群組原則來管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="196fe-205">For more information, see [Use group policies to manage Microsoft Edge extensions](microsoft-edge-manage-extensions-policies.md).</span></span>
8. <span data-ttu-id="196fe-206">檢閱使用者的意見反應。</span><span class="sxs-lookup"><span data-stu-id="196fe-206">Review feedback from your users.</span></span>
9. <span data-ttu-id="196fe-207">每月、每季或每年重複並微調程式。</span><span class="sxs-lookup"><span data-stu-id="196fe-207">Repeat and fine-tune the process monthly, quarterly, or yearly.</span></span>

<span data-ttu-id="196fe-208">在強制執行允許權限的比較基準並保護敏感性公司網站後，您可以為企業提供更多安全性，同時為使用者提供更好的體驗。</span><span class="sxs-lookup"><span data-stu-id="196fe-208">With your baseline of allowed permissions enforced and sensitive corporate sites protected, you can provide your enterprise with more security while providing a better experience for users.</span></span> <span data-ttu-id="196fe-209">員工可能會安裝他們之前無法安裝的擴充功能，但無法在敏感性的商務網站上執行這些擴充功能。</span><span class="sxs-lookup"><span data-stu-id="196fe-209">Staff might install extensions that they couldn't before, but not run them on sensitive business sites.</span></span>  

## <a name="see-also"></a><span data-ttu-id="196fe-210">另請參閱</span><span class="sxs-lookup"><span data-stu-id="196fe-210">See also</span></span>

- [<span data-ttu-id="196fe-211">使用群組原則管理 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="196fe-211">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="196fe-212">建立 Web Store 以託管 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="196fe-212">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="196fe-213">ExtensionSettings 原則的參考指南</span><span class="sxs-lookup"><span data-stu-id="196fe-213">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="196fe-214">Microsoft Edge 擴充功能常見問題集</span><span class="sxs-lookup"><span data-stu-id="196fe-214">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="196fe-215">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="196fe-215">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)