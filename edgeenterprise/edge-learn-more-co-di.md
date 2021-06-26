---
title: Microsoft Edge 中的 ClickOnce 和 DirectInvoke
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 09/10/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 深入了解 Microsoft Edge 中的 ClickOnce 和 DirectInvoke。
ms.openlocfilehash: 528c9f39a2aa6a8b30e4ec92b6b0765fc04cb817
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617353"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a><span data-ttu-id="3ef5a-103">了解 Microsoft Edge 中的 ClickOnce 和 DirectInvoke 功能</span><span class="sxs-lookup"><span data-stu-id="3ef5a-103">Understand the ClickOnce and DirectInvoke features in Microsoft Edge</span></span>

<span data-ttu-id="3ef5a-104">ClickOnce 和 DirectInvoke 是 IE 和 Microsoft Edge (版本 45 及更早版本) 中提供的功能，支援使用檔案處理常式從網站下載檔案。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-104">ClickOnce and DirectInvoke are features available in IE and Microsoft Edge (version 45 and earlier) that support the use of a file handler to download files from a website.</span></span> <span data-ttu-id="3ef5a-105">雖然其具有不同的用途，但兩個功能都允許網站指定將請求下載的檔案傳遞給使用者裝置上的檔案處理常式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-105">Although they serve different purposes, both features let websites specify that a file requested for download is passed to a file handler on the user's device.</span></span> <span data-ttu-id="3ef5a-106">ClickOnce 請求由 Windows 中的原生檔案處理常式處理。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-106">ClickOnce requests are handled by the native file handler in Windows.</span></span> <span data-ttu-id="3ef5a-107">DirectInvoke 請求由裝載該檔案之網站所指定的已註冊檔案處理常式來處理。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-107">DirectInvoke requests are handled by a registered file handler specified by the website hosting the file.</span></span>

<span data-ttu-id="3ef5a-108">如需這些方法的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="3ef5a-108">For more information about these features, see:</span></span>

- [<span data-ttu-id="3ef5a-109">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="3ef5a-109">ClickOnce</span></span>](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [<span data-ttu-id="3ef5a-110">DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="3ef5a-110">DirectInvoke</span></span>]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> <span data-ttu-id="3ef5a-111">目前，Chromium 不提供 ClickOnce 或 DirectInvoke 的原生支援。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-111">Currently, Chromium doesn't provide native support for ClickOnce or DirectInvoke.</span></span>

## <a name="overview-prerequisites-and-process"></a><span data-ttu-id="3ef5a-112">概觀：必要條件和程序</span><span class="sxs-lookup"><span data-stu-id="3ef5a-112">Overview: prerequisites and process</span></span>

<span data-ttu-id="3ef5a-113">若要讓 ClickOnce 和 DirectInvoke 依照設計方式運作，並能成功請求檔案處理常式，檔案處理常式必須註冊到支援 ClickOnce 或 DirectInvoke 的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-113">For ClickOnce and DirectInvoke to work as designed and for the file handler to be successfully requested, the file handler must be registered to the operating system as supporting ClickOnce or DirectInvoke.</span></span> <span data-ttu-id="3ef5a-114">此註冊通常在安裝原始作業系統或安裝的新程式請求使用 DirectInvoke 進行更新時發生。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-114">This registration typically happens when the original operating system is installed or when a new program that's installed requests the ability to use DirectInvoke for updates.</span></span>

<span data-ttu-id="3ef5a-115">當網站收到需要 ClickOnce 或 DirectInvoke 的下載請求時，將發生以下動作：</span><span class="sxs-lookup"><span data-stu-id="3ef5a-115">When a website receives a download request that requires ClickOnce or DirectInvoke, the following actions happen:</span></span>

- <span data-ttu-id="3ef5a-116">網站請求瀏覽器使用指定的檔案處理常式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-116">The website requests that the browser use a specified file handler.</span></span>
- <span data-ttu-id="3ef5a-117">瀏覽器檢查作業系統登錄以查看檔案處理常式是否已為所請求的檔案類型進行註冊。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-117">The browser checks the operating system registry to see if the file handler is registered for the requested file type.</span></span>
- <span data-ttu-id="3ef5a-118">如果已註冊檔案處理常式，瀏覽器將呼叫檔案處理常式並將 URL 做為引數傳遞給檔案處理常式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-118">If the file handler is registered, the browser calls the file handler and passes the URL as an argument to the file handler.</span></span>
- <span data-ttu-id="3ef5a-119">檔案處理常式會處理 URL 並下載檔案。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-119">The file handler processes the URL and downloads the file.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3ef5a-120">URL 用於判斷檔案的來源，以及存取檔案時使用的任何參數。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-120">The URL is used to determine the source of the file, as well as any parameters to use when accessing the file.</span></span>  <span data-ttu-id="3ef5a-121">例如：端點、資訊清單或中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-121">For example: endpoints, a manifest, or metadata.</span></span>

## <a name="use-cases"></a><span data-ttu-id="3ef5a-122">使用案例</span><span class="sxs-lookup"><span data-stu-id="3ef5a-122">Use cases</span></span>

<span data-ttu-id="3ef5a-123">以下使用案例具有代表性。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-123">The following use cases are representative.</span></span>

<span data-ttu-id="3ef5a-124">您可以使用 ClickOnce 在裝置上輕鬆部署和更新軟體，只需最少的使用者互動。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-124">You can use ClickOnce to easily deploy and update software on devices with minimal user interaction.</span></span> <span data-ttu-id="3ef5a-125">使用者可以透過按一下網頁中的連結來安裝和執行 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-125">Users can install and run a Windows application by clicking a link in a web page.</span></span> <span data-ttu-id="3ef5a-126">如果設定正確，ClickOnce 應用程式可以安裝程式，無需使用者為安裝程式進行設定。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-126">If configured correctly, the ClickOnce application can install programs without having users set configurations for the installer.</span></span> <span data-ttu-id="3ef5a-127">例如，檔案位置、要安裝的選項等。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-127">For example, file locations, what options to install, and so on.</span></span>

<span data-ttu-id="3ef5a-128">DirectInvoke 使用案例取決於請求 DirectInvoke 之網站的用意。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-128">DirectInvoke use cases depend on the intent of the website requesting DirectInvoke.</span></span> <span data-ttu-id="3ef5a-129">例如，Microsoft Word 的協作檔案編輯功能。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-129">For example, the collaborative file-editing feature of Microsoft Word.</span></span> <span data-ttu-id="3ef5a-130">DirectInvoke 允許您下載已變更的文件部分，而不是按一下連結並下載您正在與同事和合作處理文件的整個副本。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-130">Instead of clicking a link and downloading the entire copy of a document you're working on with your colleagues, DirectInvoke lets you download the parts of the document that have been changed.</span></span> <span data-ttu-id="3ef5a-131">這個策略可減少傳輸的資料量，並減少開啟文件所需的時間。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-131">This strategy reduces the amount of data transferred and can reduce the time needed to open the document.</span></span>  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a><span data-ttu-id="3ef5a-132">Microsoft Edge 中對 ClickOnce 和 DirectInvoke 的目前支援</span><span class="sxs-lookup"><span data-stu-id="3ef5a-132">Current support for ClickOnce and DirectInvoke in Microsoft Edge</span></span>

<span data-ttu-id="3ef5a-133">對 ClickOnce 和 DirectInvoke 的支援：</span><span class="sxs-lookup"><span data-stu-id="3ef5a-133">Support for ClickOnce and DirectInvoke:</span></span>

- <span data-ttu-id="3ef5a-134">ClickOnce 和 DirectInvoke 全面支援所有 Windows 使用者。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-134">ClickOnce and DirectInvoke are supported out of the box for all Windows users.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3ef5a-135">想停用 ClickOnce 支援的使用者可以移至*edge://flags/#edge-click-once* 並從下拉式清單中選取 **[停用]**。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-135">Users that want to disable ClickOnce support can go to *edge://flags/#edge-click-once* and select **Disabled** from the dropdown list.</span></span> <span data-ttu-id="3ef5a-136">您必須**重新啟動**瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-136">You'll have to **Restart** the browser.</span></span>

- <span data-ttu-id="3ef5a-137">ClickOnce 和 DirectInvoke 不支援 Windows 以外的任何平台。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-137">ClickOnce and DirectInvoke aren't supported on any platforms other than Windows.</span></span>

## <a name="clickonce-and-directinvoke-file-handling-security"></a><span data-ttu-id="3ef5a-138">ClickOnce 和 DirectInvoke 檔案處理安全性</span><span class="sxs-lookup"><span data-stu-id="3ef5a-138">ClickOnce and DirectInvoke file handling security</span></span>

<span data-ttu-id="3ef5a-139">ClickOnce 和 DirectInvoke 受到 Microsoft Defender SmartScreen 的 URL 信譽掃描服務的保護。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-139">ClickOnce and DirectInvoke are protected by Microsoft Defender SmartScreen's URL reputation scanning service.</span></span>

<span data-ttu-id="3ef5a-140">如果 Microsoft Defender SmartScreen URL 信譽服務將 ClickOnce 或 DirectInvoke 請求標幟為不安全，則啟用 ClickOnce 或 DirectInvoke 的使用者將看到兩個快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-140">If a ClickOnce or a DirectInvoke request is flagged by the Microsoft Defender SmartScreen URL reputation service as unsafe, users with ClickOnce or DirectInvoke enabled will see two popups.</span></span>

<span data-ttu-id="3ef5a-141">第一個快顯視窗詢問使用者是否要開啟該檔案。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-141">The first popup asks the user if they want to open the file.</span></span> <span data-ttu-id="3ef5a-142">無論檔案被標幟為安全還是不安全，都會顯示此快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-142">This popup is displayed regardless of whether the file was flagged as safe or unsafe.</span></span> <span data-ttu-id="3ef5a-143">使用者可以**將檔案報告為不安全**、**取消**請求或按一下**開啟**以繼續。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-143">The user can **Report the file as unsafe**, **Cancel** the request, or click **Open** to continue.</span></span>

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

<span data-ttu-id="3ef5a-145">如果使用者嘗試開啟檔案，並且檔案被標幟為不安全，則會顯示第二個快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-145">If the user tries to open the file, and the file was flagged as unsafe, a second popup is displayed.</span></span>  <span data-ttu-id="3ef5a-146">此快顯視窗警告使用者該檔案被標幟為不安全，並詢問他們是否確定要下載檔案。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-146">This popup warns the user that the file was flagged as unsafe, and asks them if they're sure they want to download the file.</span></span>

<span data-ttu-id="3ef5a-147">第二個快顯視窗僅在以下情況中顯示：</span><span class="sxs-lookup"><span data-stu-id="3ef5a-147">The second popup only shows up if:</span></span>

- <span data-ttu-id="3ef5a-148">該檔案是 ClickOnce 或 DirectInvoke 檔案</span><span class="sxs-lookup"><span data-stu-id="3ef5a-148">the file is a ClickOnce or DirectInvoke file</span></span>
- <span data-ttu-id="3ef5a-149">已啟用 ClickOnce 或 DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="3ef5a-149">ClickOnce or DirectInvoke are enabled</span></span>
- <span data-ttu-id="3ef5a-150">檔案標幟為不安全</span><span class="sxs-lookup"><span data-stu-id="3ef5a-150">the file is flagged as unsafe</span></span>

 ![提示以開啟不安全的檔案](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> <span data-ttu-id="3ef5a-152">如果停用 ClickOnce 或 DirectInvoke，則請求的檔案將被視為一般下載，如果標幟為不安全，則將標記為不安全。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-152">If ClickOnce or DirectInvoke are disabled, requested files are treated as regular downloads and if flagged as unsafe, will be marked as unsafe.</span></span> <span data-ttu-id="3ef5a-153">這與處理其他不安全下載的情況一致。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-153">This is consistent with the treatment of other unsafe downloads.</span></span>

## <a name="clickonce-and-directinvoke-policies"></a><span data-ttu-id="3ef5a-154">ClickOnce 和 DirectInvoke 原則</span><span class="sxs-lookup"><span data-stu-id="3ef5a-154">ClickOnce and DirectInvoke policies</span></span>

<span data-ttu-id="3ef5a-155">有 2 個群組原則可用於為企業使用者啟用或停用 ClickOnce 和 DirectInvoke。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-155">There are two group policies that you can use to enable or disable ClickOnce and DirectInvoke for enterprise users.</span></span> <span data-ttu-id="3ef5a-156">這兩個原則是 [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) 和 [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled)。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-156">These two policies are [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) and [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled).</span></span> <span data-ttu-id="3ef5a-157">這兩個策略在群組原則編輯器中分別標記為 [允許使用者使用 ClickOnce 通訊協定開啟檔案] 和 [允許使用者使用 DirectInvoke 通訊協定開啟檔案]。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-157">These two policies are labeled in the Group Policy Editor as "Allow users to open files using the ClickOnce protocol" and "Allow users to open files using the DirectInvoke protocol" respectively.</span></span>

## <a name="clickonce-and-directinvoke-behavior"></a><span data-ttu-id="3ef5a-158">ClickOnce 和 DirectInvoke 行為</span><span class="sxs-lookup"><span data-stu-id="3ef5a-158">ClickOnce and DirectInvoke behavior</span></span>

<span data-ttu-id="3ef5a-159">以下範例顯示啟用或停用 ClickOnce 和 DirectInvoke 時的檔案處理。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-159">The following examples show file handling when ClickOnce and DirectInvoke are enabled or disabled.</span></span>

### <a name="clickonce-enabled"></a><span data-ttu-id="3ef5a-160">ClickOnce 已啟用</span><span class="sxs-lookup"><span data-stu-id="3ef5a-160">ClickOnce enabled</span></span>

1. <span data-ttu-id="3ef5a-161">使用者開啟指向請求 ClickOnce 支援之頁面的連結，並在下一個螢幕擷取畫面中收到提示。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-161">A user opens a link to a page that requests ClickOnce support and gets the prompt in the next screenshot.</span></span>

   ![提示以開啟不安全的檔案](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. <span data-ttu-id="3ef5a-163">使用者按一下**開啟**後，ClickOnce 嘗試啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-163">After the user clicks **Open**, ClickOnce attempts to launch the application.</span></span>

   ![ClickOnce 嘗試啟動應用程式](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. <span data-ttu-id="3ef5a-165">使用者按一下**開啟**後，瀏覽器將顯示一個快顯視窗，詢問使用者是否確定要安裝該應用程式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-165">After the user clicks **Open**, the browser shows a popup that asks the user if they're sure they want to install the application.</span></span>

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > <span data-ttu-id="3ef5a-167">ClickOnce 檔案處理常式顯示的介面、訊息和選項，將因所存取檔案的類型和設定而異。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-167">The interface, messaging, and options shown by the ClickOnce file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="clickonce-disabled"></a><span data-ttu-id="3ef5a-168">ClickOnce 已停用</span><span class="sxs-lookup"><span data-stu-id="3ef5a-168">ClickOnce disabled</span></span>

1. <span data-ttu-id="3ef5a-169">當使用者開啟指向請求 ClickOnce 支援之頁面的連結時，會在下載匣中看到一則訊息，此訊息與下一個螢幕擷取畫面中的訊息類似。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-169">When a user opens a link to a page that requests ClickOnce support, they will see a message in the download tray that is similar to the one in the next screenshot.</span></span>

   ![檔案下載提示](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a><span data-ttu-id="3ef5a-171">DirectInvoke 已啟用</span><span class="sxs-lookup"><span data-stu-id="3ef5a-171">DirectInvoke enabled</span></span>

1. <span data-ttu-id="3ef5a-172">使用者開啟指向請求 DirectInvoke 支援之頁面的連結，並在下一個螢幕擷取畫面中收到提示。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-172">A user opens a link to a page that requests DirectInvoke support and gets the prompt in the next screenshot.</span></span>

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. <span data-ttu-id="3ef5a-174">當使用者按一下**開啟**時，將開啟請求的檔案處理常式。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-174">When the user clicks **Open**, the requested file handler is opened.</span></span> <span data-ttu-id="3ef5a-175">在此範例中，Microsoft Word 用於開啟上一個螢幕擷取畫面中顯示的文件。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-175">In this example, Microsoft Word is used to open the document that's shown in the previous screenshot.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3ef5a-176">DirectInvoke 檔案處理常式顯示的介面、訊息和選項，將因所存取檔案的類型和設定而異。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-176">The interface, messaging, and options shown by the DirectInvoke file handler will vary depending on the type and configuration of the file that's accessed.</span></span>

### <a name="directinvoke-disabled"></a><span data-ttu-id="3ef5a-177">DirectInvoke 已停用</span><span class="sxs-lookup"><span data-stu-id="3ef5a-177">DirectInvoke disabled</span></span>

1. <span data-ttu-id="3ef5a-178">當使用者開啟指向請求 DirectInvoke 支援之頁面的連結時，DirectInvoke 的行為與停用 ClickOnce 時相同。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-178">When a user opens a link to a page that requests DirectInvoke support, DirectInvoke behaves the same as when ClickOnce is disabled.</span></span> <span data-ttu-id="3ef5a-179">他們將在下載匣中看到一則訊息，此訊息與下一個螢幕擷取畫面中的訊息類似。</span><span class="sxs-lookup"><span data-stu-id="3ef5a-179">They will see a message in the download tray that's similar to the one in the next screenshot.</span></span>

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a><span data-ttu-id="3ef5a-181">也請參閱</span><span class="sxs-lookup"><span data-stu-id="3ef5a-181">See also</span></span>

- [<span data-ttu-id="3ef5a-182">ClickOnce 安全性和部署</span><span class="sxs-lookup"><span data-stu-id="3ef5a-182">ClickOnce security and deployment</span></span>](/visualstudio/deployment/clickonce-security-and-deployment)
- [<span data-ttu-id="3ef5a-183">Internet Explorer 中的 DirectInvoke</span><span class="sxs-lookup"><span data-stu-id="3ef5a-183">DirectInvoke in Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [<span data-ttu-id="3ef5a-184">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3ef5a-184">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)