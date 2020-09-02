---
title: Microsoft Edge 的 PDF 閱讀程式
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 08/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Microsoft Edge 的 PDF 閱讀程式。
ms.openlocfilehash: c189bc08d4af0c9d5c4d9c573e0b5b7ef32a7fb3
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979603"
---
# <span data-ttu-id="82021-103">Microsoft Edge 的 PDF 閱讀程式</span><span class="sxs-lookup"><span data-stu-id="82021-103">PDF reader in Microsoft Edge</span></span>

<span data-ttu-id="82021-104">PDF 檔案是我們日常生活的一部分。</span><span class="sxs-lookup"><span data-stu-id="82021-104">PDF files make up a substantial part of our day-to-day lives.</span></span> <span data-ttu-id="82021-105">它們以合約和協議、電子報、表單、研究文章、履歷等的形式出現。</span><span class="sxs-lookup"><span data-stu-id="82021-105">They come in the form of contracts and agreements, newsletters, forms, research articles, resumes, and so on.</span></span> <span data-ttu-id="82021-106">這些檔案突顯了供企業使用的可靠、安全且功能強大的 PDF 閱讀程式之需求。</span><span class="sxs-lookup"><span data-stu-id="82021-106">These files highlight the need for a reliable, secure, and powerful PDF reader that can be adopted by Enterprises.</span></span>

<span data-ttu-id="82021-107">Microsoft Edge 隨附內建的 PDF 閱讀程式，可讓您開啟本機 pdf 檔案、線上 pdf 檔案，或內嵌在網頁中的 pdf 檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-107">Microsoft Edge comes with a built-in PDF reader that lets you open your local pdf files, online pdf files, or pdf files embedded in web pages.</span></span> <span data-ttu-id="82021-108">您可以使用筆跡和醒目提示來標註這些檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-108">You can annotate these files with ink and highlighting.</span></span> <span data-ttu-id="82021-109">這個 PDF 閱讀程式會為使用者提供單一應用程式，以符合網頁和 PDF 文件的需求。</span><span class="sxs-lookup"><span data-stu-id="82021-109">This PDF reader gives users a single application to meet web page and PDF document needs.</span></span> <span data-ttu-id="82021-110">Microsoft Edge PDF 閱讀程式是一種安全且可靠的應用程式，可在 Windows 和 macOS 桌面平台上運作。</span><span class="sxs-lookup"><span data-stu-id="82021-110">The Microsoft Edge PDF reader is a secure and reliable application that works across the Windows and macOS desktop platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="82021-111">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="82021-111">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="82021-112">必要條件、支援及限制</span><span class="sxs-lookup"><span data-stu-id="82021-112">Prerequisites, support, and constraints</span></span>

<span data-ttu-id="82021-113">下表顯示支援 PDF 閱讀程式各種功能的 Microsoft Edge 頻道和版本 。</span><span class="sxs-lookup"><span data-stu-id="82021-113">The following table shows which channels and versions of Microsoft Edge support each PDF reader feature.</span></span>

| <span data-ttu-id="82021-114">功能</span><span class="sxs-lookup"><span data-stu-id="82021-114">Feature</span></span> | <span data-ttu-id="82021-115">穩定通道版本</span><span class="sxs-lookup"><span data-stu-id="82021-115">Stable channel version</span></span> |
|---------|------------------------|
| <span data-ttu-id="82021-116">檢視及列印本機、線上及內嵌的 PDF 檔案</span><span class="sxs-lookup"><span data-stu-id="82021-116">View and print local, online, and embedded PDF files</span></span> | <span data-ttu-id="82021-117">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="82021-117">79.0.309.71</span></span>                |
| <span data-ttu-id="82021-118">基本表單填寫</span><span class="sxs-lookup"><span data-stu-id="82021-118">Basic form filling</span></span><br><span data-ttu-id="82021-119">(不支援 JavaScript 表單)</span><span class="sxs-lookup"><span data-stu-id="82021-119">(JavaScript forms aren't supported)</span></span> | <span data-ttu-id="82021-120">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="82021-120">79.0.309.71</span></span>           |
| <span data-ttu-id="82021-121">筆跡</span><span class="sxs-lookup"><span data-stu-id="82021-121">Inking</span></span>  | <span data-ttu-id="82021-122">80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="82021-122">80.0.361.48</span></span>            |
| <span data-ttu-id="82021-123">筆跡自訂</span><span class="sxs-lookup"><span data-stu-id="82021-123">Ink customization</span></span> | <span data-ttu-id="82021-124">83.0.478.54</span><span class="sxs-lookup"><span data-stu-id="82021-124">83.0.478.54</span></span>  |
| <span data-ttu-id="82021-125">醒目顯示</span><span class="sxs-lookup"><span data-stu-id="82021-125">Highlight</span></span>  | <span data-ttu-id="82021-126">81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="82021-126">81.0.416.53</span></span>         |
| <span data-ttu-id="82021-127">大聲朗讀</span><span class="sxs-lookup"><span data-stu-id="82021-127">Read Aloud</span></span> | <span data-ttu-id="82021-128">目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/) 頻道中進行推廣</span><span class="sxs-lookup"><span data-stu-id="82021-128">Currently being promoted in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) channels</span></span> |
| <span data-ttu-id="82021-129">檢視受 MIP 保護的檔案</span><span class="sxs-lookup"><span data-stu-id="82021-129">View MIP protected files</span></span> | <span data-ttu-id="82021-130">80.0.361.48 支援 Windows 版</span><span class="sxs-lookup"><span data-stu-id="82021-130">Windows support in 80.0.361.48</span></span><br><span data-ttu-id="82021-131">81.0.416.53 支援 Mac 版</span><span class="sxs-lookup"><span data-stu-id="82021-131">Mac support in 81.0.416.53</span></span> |
|  <span data-ttu-id="82021-132">檢視受 IRM 保護的檔案</span><span class="sxs-lookup"><span data-stu-id="82021-132">View IRM protected files</span></span>  | <span data-ttu-id="82021-133">83.0.478.37</span><span class="sxs-lookup"><span data-stu-id="82021-133">83.0.478.37</span></span>            |

### <span data-ttu-id="82021-134">限制式</span><span class="sxs-lookup"><span data-stu-id="82021-134">Constraints</span></span>

<span data-ttu-id="82021-135">請注意以下目前 PDF 閱讀程式的限制：</span><span class="sxs-lookup"><span data-stu-id="82021-135">Note the following constraints for the current PDF reader:</span></span>

-  <span data-ttu-id="82021-136">XML 表單架構 (XFA) 是 Microsoft Edge 中不支援的舊版表單格式。</span><span class="sxs-lookup"><span data-stu-id="82021-136">XML Forms Architecture (XFA), is a legacy format of forms that isn't  supported in Microsoft Edge.</span></span>
-  <span data-ttu-id="82021-137">目前不支援之協助工具案例的相關文件，可在 [Microsoft 協助工具符合性報告](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) 的部落格中找到。</span><span class="sxs-lookup"><span data-stu-id="82021-137">Documentation related to Accessibility scenarios that currently aren't supported can be found on the [Microsoft Accessibility Conformance Reports](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) blog.</span></span>

## <span data-ttu-id="82021-138">功能</span><span class="sxs-lookup"><span data-stu-id="82021-138">Features</span></span>

### <span data-ttu-id="82021-139">筆跡</span><span class="sxs-lookup"><span data-stu-id="82021-139">Inking</span></span>

<span data-ttu-id="82021-140">PDF 檔案的筆跡功能可讓您輕鬆進行快速筆記，以便用於參照、簽署或填寫 PDF 表單。</span><span class="sxs-lookup"><span data-stu-id="82021-140">Inking on PDF files comes in handy to take quick notes for easy reference, sign, or fill out PDF forms.</span></span> <span data-ttu-id="82021-141">此功能現在可在 Microsoft Edge 中使用。</span><span class="sxs-lookup"><span data-stu-id="82021-141">This capability is now available in Microsoft Edge.</span></span> <span data-ttu-id="82021-142">除了筆跡 PDF 檔案，您也可以使用色彩和筆觸寬度為 PDF 檔案的不同部分引起注意。</span><span class="sxs-lookup"><span data-stu-id="82021-142">In addition to inking PDF files as needed, you can use color and stroke width to bring attention to different parts of the PDF file.</span></span> <span data-ttu-id="82021-143">下個螢幕擷取畫面顯示使用者如何將筆跡新增至 pdf 頁面。</span><span class="sxs-lookup"><span data-stu-id="82021-143">The next screenshot shows how a user can add inking to a pdf page.</span></span>

<!-- SCREENSHOT -->
![將筆跡新增至 pdf 頁面](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <span data-ttu-id="82021-145">醒目顯示</span><span class="sxs-lookup"><span data-stu-id="82021-145">Highlight</span></span>

<span data-ttu-id="82021-146">Microsoft Edge 中的 PDF 閱讀程式隨附新增和編輯醒目提示的支援。</span><span class="sxs-lookup"><span data-stu-id="82021-146">PDF reader in Microsoft Edge comes with support for adding and editing highlights.</span></span> <span data-ttu-id="82021-147">若要建立醒目提示，使用者只需選取文字，按一下滑鼠右鍵，然後選取功能表中的 [醒目提示]，並選擇想要的色彩。</span><span class="sxs-lookup"><span data-stu-id="82021-147">To create a highlight, the user simply needs to select the text, right-click on it, select highlights in the menu and choose the desired color.</span></span> <span data-ttu-id="82021-148">下個螢幕擷取畫面顯示可用的醒目提示選項。</span><span class="sxs-lookup"><span data-stu-id="82021-148">The next screenshot shows the highlight options that are available.</span></span>

![使用 PDF 閱讀程式中的 [醒目提示] 選項](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <span data-ttu-id="82021-150">大聲朗讀</span><span class="sxs-lookup"><span data-stu-id="82021-150">Read Aloud</span></span>

<span data-ttu-id="82021-151">PDF 的大聲朗讀功能新增聆聽 PDF 內容的方便性，並讓使用者同時執行其他重要的工作。</span><span class="sxs-lookup"><span data-stu-id="82021-151">Read Aloud for PDF adds the convenience of listening to PDF content while carrying out other tasks that may be important to users.</span></span> <span data-ttu-id="82021-152">這也有助於讓聽覺學習人士專注於內容，讓學習更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="82021-152">It also helps auditory learners focus on the content, which makes learning much easier.</span></span> <span data-ttu-id="82021-153">下個螢幕擷取畫面顯示 [大聲朗讀] 範例。</span><span class="sxs-lookup"><span data-stu-id="82021-153">The next screenshot shows a Read Aloud example.</span></span> <span data-ttu-id="82021-154">[醒目提示] 會顯示目前正在閱讀的文字。</span><span class="sxs-lookup"><span data-stu-id="82021-154">The highlighting shows the text that is currently being read.</span></span>

![使用 PDF 閱讀程式中的 [醒目提示] 選項](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <span data-ttu-id="82021-156">受保護的 PDF</span><span class="sxs-lookup"><span data-stu-id="82021-156">Protected PDFs</span></span>

<span data-ttu-id="82021-157">[Microsoft 資訊保護 (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) 能讓使用者安全地與其他人共同作業，同時遵守貴組織的合規性原則。</span><span class="sxs-lookup"><span data-stu-id="82021-157">[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) enables users to collaborate with others securely, while adhering to your organization's compliance policies.</span></span> <span data-ttu-id="82021-158">檔案受到保護之後，使用者可對檔案執行的動作會由指派給他們的權限來決定。</span><span class="sxs-lookup"><span data-stu-id="82021-158">After a file is protected, the actions users can take on it are determined by the permissions assigned to them.</span></span>

<span data-ttu-id="82021-159">您可以直接在瀏覽器中開啟這些檔案，而不需要下載任何其他軟體，或安裝任何增益集。</span><span class="sxs-lookup"><span data-stu-id="82021-159">These files can be opened directly in the browser, without the need to download any other software, or install any add-in.</span></span> <span data-ttu-id="82021-160">這會將 MIP 所提供的安全性直接整合至瀏覽器，以提供流暢的工作流程。</span><span class="sxs-lookup"><span data-stu-id="82021-160">This integrates the security provided by MIP directly into the browser, providing a seamless workflow.</span></span>

<!-- SCREENSHOT -->
![受保護的 pdf 文件。](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

<span data-ttu-id="82021-162">除了受 MIP 保護的檔案，[資訊版權管理 (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide)受保護 SharePoint 文件庫中的 PDF 檔案也可以在瀏覽器中以本機方式開啟。</span><span class="sxs-lookup"><span data-stu-id="82021-162">In addition to MIP protected files, PDF files in [Information Rights Management (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide) protected SharePoint libraries can also be opened natively in the browser.</span></span>

<span data-ttu-id="82021-163">有了 Microsoft Edge，使用者就能在本機或雲端中檢視受 MIP 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-163">With Microsoft Edge, users can view MIP protected files saved locally, or in the cloud.</span></span> <span data-ttu-id="82021-164">如果您已在本機儲存，可以直接在瀏覽器中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-164">If saved locally, the file can be opened directly in the browser.</span></span> <span data-ttu-id="82021-165">如果檔案是從 SharePoint 雲端服務開啟 ，則使用者可能需要使用「在瀏覽器中開啟」選項。</span><span class="sxs-lookup"><span data-stu-id="82021-165">If the file is opened from a cloud service as SharePoint, the user may need to use the "Open in browser" option.</span></span>

<span data-ttu-id="82021-166">如果使用者登入 Microsoft Edge 的設定檔至少擁有該檔案的檢視權限，檔案就會在 Microsoft Edge 中開啟。</span><span class="sxs-lookup"><span data-stu-id="82021-166">If the profile that the user is logged into Microsoft Edge with has at least view permissions to the file, the file will open in Microsoft Edge.</span></span>

<!-- SCREENSHOT -->
![提示儲存由 MIP 保護的 SharePoint pdf 頁面](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## <span data-ttu-id="82021-168">協助工具</span><span class="sxs-lookup"><span data-stu-id="82021-168">Accessibility</span></span>

<span data-ttu-id="82021-169">PDF 閱讀程式隨附支援鍵盤協助工具、高對比模式，以及 支援 Windows 和 macOS 裝置的螢幕助讀程式。</span><span class="sxs-lookup"><span data-stu-id="82021-169">The PDF reader comes with support for Keyboard accessibility, High contrast mode, and screen reader support across Windows and macOS devices.</span></span>

### <span data-ttu-id="82021-170">鍵盤協助工具</span><span class="sxs-lookup"><span data-stu-id="82021-170">Keyboard Accessibility</span></span>

<span data-ttu-id="82021-171">使用者可以使用鍵盤瀏覽至文件中可與使用者互動的不同部分，例如表單欄位和醒目提示。</span><span class="sxs-lookup"><span data-stu-id="82021-171">Users can use navigate to different parts of the document that a user can interact with, such as form fields and highlights, using the keyboard.</span></span>

<!-- SCREENSHOT -->

### <span data-ttu-id="82021-172">高對比模式</span><span class="sxs-lookup"><span data-stu-id="82021-172">High contrast mode</span></span>

<span data-ttu-id="82021-173">PDF 閱讀程式會使用作業系統層級定義的設定，在高對比模式下呈現 PDF 內容。</span><span class="sxs-lookup"><span data-stu-id="82021-173">PDF reader will use the settings defined at the operating system level to render PDF content in high contrast mode.</span></span>

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### <span data-ttu-id="82021-174">支援螢幕助讀程式</span><span class="sxs-lookup"><span data-stu-id="82021-174">Screen reader support</span></span>

<span data-ttu-id="82021-175">使用者可以使用 Windows 和 Mac 電腦上的螢幕助讀程式瀏覽和讀取 PDF 檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-175">Users can navigate through and read PDF files using screen readers on Windows and Mac computers.</span></span> <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## <span data-ttu-id="82021-176">安全性和可靠性</span><span class="sxs-lookup"><span data-stu-id="82021-176">Security and reliability</span></span>

<span data-ttu-id="82021-177">安全性是任何組織最重要的原則。</span><span class="sxs-lookup"><span data-stu-id="82021-177">Security is among the most important tenets for any organization.</span></span> <span data-ttu-id="82021-178">PDF 閱讀程式安全性是 Microsoft Edge 安全性設計不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="82021-178">PDF reader security is an integral part of the Microsoft Edge security design.</span></span> <span data-ttu-id="82021-179">從 PDF 閱讀程式最重要的兩個安全性功能之角度來看，兩個重要的安全性功能是「處理程序隔離」和「Microsoft Defender 應用程式防護」(應用程式防護)。</span><span class="sxs-lookup"><span data-stu-id="82021-179">Two of the most important security features From a PDF reader perspective, two important security features are process isolation and Microsoft Defender Application Guard (Application Guard).</span></span>

- <span data-ttu-id="82021-180">處理程序隔離。</span><span class="sxs-lookup"><span data-stu-id="82021-180">Process isolation.</span></span> <span data-ttu-id="82021-181">從不同網站開啟的 PDF 完全是處理程序隔離。</span><span class="sxs-lookup"><span data-stu-id="82021-181">PDFs opened from different web sites are completely process isolated.</span></span> <span data-ttu-id="82021-182">瀏覽器不需要與從任何網站或其他來源開啟的 PDF 檔案進行通訊。</span><span class="sxs-lookup"><span data-stu-id="82021-182">The browser doesn't have to communicate with any websites, or PDF files opened from another source.</span></span> <span data-ttu-id="82021-183">PDF 瀏覽是安全的，不受任何計畫使用被感染的 PDF 作為攻擊面的任何威脅。</span><span class="sxs-lookup"><span data-stu-id="82021-183">PDF browsing is secure from any attacks that plan to use compromised PDFs as an attack surface.</span></span>

- <span data-ttu-id="82021-184">應用程式防護。</span><span class="sxs-lookup"><span data-stu-id="82021-184">Application Guard.</span></span> <span data-ttu-id="82021-185">使用應用程式防護，系統管理員可以設定組織信任的網站清單。</span><span class="sxs-lookup"><span data-stu-id="82021-185">With Application Guard, admins can set a list of sites that are trusted by their organization.</span></span> <span data-ttu-id="82021-186">如果使用者開啟任何其他網站，則會在單獨的應用程式防護視窗中開啟，並在自己的容器中執行。</span><span class="sxs-lookup"><span data-stu-id="82021-186">If users open any other sites, they are opened in a separate Application Guard window that runs in its own container.</span></span> <span data-ttu-id="82021-187">容器可協助保護公司網路，並防止使用者電腦上的任何資料遭盜用。</span><span class="sxs-lookup"><span data-stu-id="82021-187">The container helps protect the corporate network and any data on user's computer from being compromised.</span></span><br><br>
<span data-ttu-id="82021-188">這種保護也適用於任何已檢視的線上 PDF 檔案。</span><span class="sxs-lookup"><span data-stu-id="82021-188">This protection also applies to any online PDF files that are viewed.</span></span> <span data-ttu-id="82021-189">此外，將會儲存從應用程式防護視窗下載的任何 PDF 檔案，並在該容器中重新開啟。</span><span class="sxs-lookup"><span data-stu-id="82021-189">Further, any PDF files that are downloaded from an Application Guard window are stored, and when needed, re-opened in the container.</span></span> <span data-ttu-id="82021-190">這不僅在檔案下載時，而且在整個生命週期中都能確保環境的安全。</span><span class="sxs-lookup"><span data-stu-id="82021-190">This helps keeps your environment secure not just when the file is downloaded, but through its whole lifecycle.</span></span> <span data-ttu-id="82021-191">如需詳細資訊，請參閱 [應用程式防護](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard)。</span><span class="sxs-lookup"><span data-stu-id="82021-191">For more information, see [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span></span>

### <span data-ttu-id="82021-192">可靠性</span><span class="sxs-lookup"><span data-stu-id="82021-192">Reliability</span></span>

<span data-ttu-id="82021-193">由於 Microsoft Edge 是以 Chromium 為基礎開發的，因此使用者的可靠性層級與 Google Chrome 中所用的可靠性層級相同。</span><span class="sxs-lookup"><span data-stu-id="82021-193">Because Microsoft Edge is Chromium-based, users can expect the same level of reliability that they're used to seeing in Google Chrome.</span></span>

## <span data-ttu-id="82021-194">部署和更新 PDF 閱讀程式</span><span class="sxs-lookup"><span data-stu-id="82021-194">Deploy and update PDF reader</span></span>

<span data-ttu-id="82021-195">PDF 閱讀程式會與 Microsoft Edge 瀏覽器的其餘部分一起部署並更新。</span><span class="sxs-lookup"><span data-stu-id="82021-195">The PDF reader gets deployed and updated with the rest of the Microsoft Edge browser.</span></span> <span data-ttu-id="82021-196">若要深入了解如何部署 Microsoft Edge，請觀看[將 Microsoft Edge 部署到成百或上千個裝置](microsoft-edge-video-deploy.md)影片。</span><span class="sxs-lookup"><span data-stu-id="82021-196">To learn more about deploying Microsoft Edge, watch the [Deploy Microsoft Edge to hundreds or thousands of devices](microsoft-edge-video-deploy.md) video.</span></span> <span data-ttu-id="82021-197">您也可以在 [Microsoft Edge 文件](https://docs.microsoft.com/DeployEdge/)登陸頁面上找到更多部署資訊。</span><span class="sxs-lookup"><span data-stu-id="82021-197">You can also find more deployment information on the [Microsoft Edge documentation](https://docs.microsoft.com/DeployEdge/) landing page.</span></span>

> [!TIP]
> <span data-ttu-id="82021-198">您可以讓 Microsoft Edge 成為貴組織預設的 PDF 閱讀程式。</span><span class="sxs-lookup"><span data-stu-id="82021-198">You can make Microsoft Edge the default PDF reader for your organization.</span></span> <span data-ttu-id="82021-199">若要這樣做，[請執行下列步驟](https://docs.microsoft.com/deployedge/edge-default-browser)。</span><span class="sxs-lookup"><span data-stu-id="82021-199">To do this, [follow these steps](https://docs.microsoft.com/deployedge/edge-default-browser).</span></span>

## <span data-ttu-id="82021-200">藍圖與意見反應</span><span class="sxs-lookup"><span data-stu-id="82021-200">Roadmap and feedback</span></span>

<span data-ttu-id="82021-201">Microsoft Edge 的 PDF 閱讀程式藍圖可在 [此處](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667) 獲得。</span><span class="sxs-lookup"><span data-stu-id="82021-201">The roadmap for PDF Reader in Microsoft Edge is available [here](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span></span>

<span data-ttu-id="82021-202">我們正在積極查看對您重要功能的意見反應。</span><span class="sxs-lookup"><span data-stu-id="82021-202">We're actively looking at feedback from you about the features you find important.</span></span> <span data-ttu-id="82021-203">歡迎您透過 [Microsoft edge UserVoice](https://microsoftedge.uservoice.com/) 和 [Microsoft Edge 測試人員](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) 論壇，將意見反應傳送給我們。</span><span class="sxs-lookup"><span data-stu-id="82021-203">Feel free to send us feedback through [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) and on [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) forum.</span></span>

## <span data-ttu-id="82021-204">請參閱</span><span class="sxs-lookup"><span data-stu-id="82021-204">See also</span></span>

- [<span data-ttu-id="82021-205">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="82021-205">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)