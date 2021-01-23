---
title: Microsoft Edge 的 PDF 閱讀程式
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Microsoft Edge 的 PDF 閱讀程式。
ms.openlocfilehash: d4d9d3efa063b9b6981d5c7cd4bc69968b56448b
ms.sourcegitcommit: f0f250190fc09964175778338a177f1240946b98
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297207"
---
# <span data-ttu-id="fcce3-103">Microsoft Edge 的 PDF 閱讀程式</span><span class="sxs-lookup"><span data-stu-id="fcce3-103">PDF reader in Microsoft Edge</span></span>

<span data-ttu-id="fcce3-104">PDF 檔案佔據我們日常生活的一大部分。</span><span class="sxs-lookup"><span data-stu-id="fcce3-104">PDF files make up a large part of our day-to-day lives.</span></span> <span data-ttu-id="fcce3-105">它們以合約和協議、電子報、表單、研究文章、履歷等的形式出現。</span><span class="sxs-lookup"><span data-stu-id="fcce3-105">They come in the form of contracts and agreements, newsletters, forms, research articles, resumes, and so on.</span></span> <span data-ttu-id="fcce3-106">這些檔案突顯了供企業使用的可靠、安全且功能強大的 PDF 閱讀程式之需求。</span><span class="sxs-lookup"><span data-stu-id="fcce3-106">These files highlight the need for a reliable, secure, and powerful PDF reader that can be adopted by Enterprises.</span></span>

<span data-ttu-id="fcce3-107">Microsoft Edge 隨附內建的 PDF 閱讀程式，可讓您開啟本機 pdf 檔案、線上 pdf 檔案，或內嵌在網頁中的 pdf 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-107">Microsoft Edge comes with a built-in PDF reader that lets you open your local pdf files, online pdf files, or pdf files embedded in web pages.</span></span> <span data-ttu-id="fcce3-108">您可以使用筆跡和醒目提示來標註這些檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-108">You can annotate these files with ink and highlighting.</span></span> <span data-ttu-id="fcce3-109">這個 PDF 閱讀程式會為使用者提供單一應用程式，以符合網頁和 PDF 文件的需求。</span><span class="sxs-lookup"><span data-stu-id="fcce3-109">This PDF reader gives users a single application to meet web page and PDF document needs.</span></span> <span data-ttu-id="fcce3-110">Microsoft Edge PDF 閱讀程式是一種安全且可靠的應用程式，可在 Windows 和 macOS 桌面平台上運作。</span><span class="sxs-lookup"><span data-stu-id="fcce3-110">The Microsoft Edge PDF reader is a secure and reliable application that works across the Windows and macOS desktop platforms.</span></span>

> [!NOTE]
> <span data-ttu-id="fcce3-111">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fcce3-111">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="fcce3-112">必要條件、支援及限制</span><span class="sxs-lookup"><span data-stu-id="fcce3-112">Prerequisites, support, and constraints</span></span>

<span data-ttu-id="fcce3-113">下表顯示支援 PDF 閱讀程式各種功能的 Microsoft Edge 頻道和版本 。</span><span class="sxs-lookup"><span data-stu-id="fcce3-113">The following table shows which channels and versions of Microsoft Edge support each PDF reader feature.</span></span>

| <span data-ttu-id="fcce3-114">功能</span><span class="sxs-lookup"><span data-stu-id="fcce3-114">Feature</span></span> | <span data-ttu-id="fcce3-115">穩定通道版本</span><span class="sxs-lookup"><span data-stu-id="fcce3-115">Stable channel version</span></span> |
|---------|------------------------|
| <span data-ttu-id="fcce3-116">檢視及列印本機、線上及內嵌的 PDF 檔案</span><span class="sxs-lookup"><span data-stu-id="fcce3-116">View and print local, online, and embedded PDF files</span></span> | <span data-ttu-id="fcce3-117">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="fcce3-117">79.0.309.71</span></span>                |
| <span data-ttu-id="fcce3-118">基本表單填寫</span><span class="sxs-lookup"><span data-stu-id="fcce3-118">Basic form filling</span></span><br><span data-ttu-id="fcce3-119">(不支援 JavaScript 表單)</span><span class="sxs-lookup"><span data-stu-id="fcce3-119">(JavaScript forms aren't supported)</span></span> | <span data-ttu-id="fcce3-120">79.0.309.71</span><span class="sxs-lookup"><span data-stu-id="fcce3-120">79.0.309.71</span></span>           |
|<span data-ttu-id="fcce3-121">目錄</span><span class="sxs-lookup"><span data-stu-id="fcce3-121">Table of contents</span></span>| <span data-ttu-id="fcce3-122">86.0.622.38</span><span class="sxs-lookup"><span data-stu-id="fcce3-122">86.0.622.38</span></span> |
| <span data-ttu-id="fcce3-123">頁面檢視</span><span class="sxs-lookup"><span data-stu-id="fcce3-123">Page view</span></span> |<span data-ttu-id="fcce3-124">目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/)通道中推廣</span><span class="sxs-lookup"><span data-stu-id="fcce3-124">Currently being promoted in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) channels</span></span> |
| <span data-ttu-id="fcce3-125">鍵盤模式瀏覽</span><span class="sxs-lookup"><span data-stu-id="fcce3-125">Caret mode browsing</span></span> |<span data-ttu-id="fcce3-126">87.0.664.41</span><span class="sxs-lookup"><span data-stu-id="fcce3-126">87.0.664.41</span></span> |
| <span data-ttu-id="fcce3-127">筆跡</span><span class="sxs-lookup"><span data-stu-id="fcce3-127">Inking</span></span>  | <span data-ttu-id="fcce3-128">80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="fcce3-128">80.0.361.48</span></span>            |
| <span data-ttu-id="fcce3-129">筆跡自訂</span><span class="sxs-lookup"><span data-stu-id="fcce3-129">Ink customization</span></span> | <span data-ttu-id="fcce3-130">83.0.478.54</span><span class="sxs-lookup"><span data-stu-id="fcce3-130">83.0.478.54</span></span>  |
| <span data-ttu-id="fcce3-131">醒目顯示</span><span class="sxs-lookup"><span data-stu-id="fcce3-131">Highlight</span></span>  | <span data-ttu-id="fcce3-132">81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="fcce3-132">81.0.416.53</span></span>         |
| <span data-ttu-id="fcce3-133">文字筆記</span><span class="sxs-lookup"><span data-stu-id="fcce3-133">Text notes</span></span> | <span data-ttu-id="fcce3-134">目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/)通道中推廣</span><span class="sxs-lookup"><span data-stu-id="fcce3-134">Currently being promoted in [Microsoft Edge Insider](https://www.microsoftedgeinsider.com/) channels</span></span> |
| <span data-ttu-id="fcce3-135">大聲朗讀</span><span class="sxs-lookup"><span data-stu-id="fcce3-135">Read aloud</span></span> | <span data-ttu-id="fcce3-136">84.0.522.63</span><span class="sxs-lookup"><span data-stu-id="fcce3-136">84.0.522.63</span></span>  |
| <span data-ttu-id="fcce3-137">檢視受 Microsoft 資訊保護 (MIP) 保護的檔案</span><span class="sxs-lookup"><span data-stu-id="fcce3-137">View Microsoft Information Protection (MIP) protected files</span></span> | <span data-ttu-id="fcce3-138">Windows 支援使用 80.0.361.48</span><span class="sxs-lookup"><span data-stu-id="fcce3-138">Windows support in 80.0.361.48</span></span><br><span data-ttu-id="fcce3-139">Mac 支援使用 81.0.416.53</span><span class="sxs-lookup"><span data-stu-id="fcce3-139">Mac support in 81.0.416.53</span></span> |
|  <span data-ttu-id="fcce3-140">檢視受資訊版權管理 (IRM) 保護的檔案</span><span class="sxs-lookup"><span data-stu-id="fcce3-140">View Information Rights Management (IRM) protected files</span></span>  | <span data-ttu-id="fcce3-141">83.0.478.37</span><span class="sxs-lookup"><span data-stu-id="fcce3-141">83.0.478.37</span></span>            |
| <span data-ttu-id="fcce3-142">檢視和驗證數位簽章</span><span class="sxs-lookup"><span data-stu-id="fcce3-142">View and validate Digital Signatures</span></span> | <span data-ttu-id="fcce3-143">在 Canary 和 Dev 通道中提供。</span><span class="sxs-lookup"><span data-stu-id="fcce3-143">Available in Canary and Dev channels.</span></span> <span data-ttu-id="fcce3-144">正在積極處理。</span><span class="sxs-lookup"><span data-stu-id="fcce3-144">Being actively worked on.</span></span> |

### <span data-ttu-id="fcce3-145">限制式</span><span class="sxs-lookup"><span data-stu-id="fcce3-145">Constraints</span></span>

<span data-ttu-id="fcce3-146">請注意以下目前 PDF 閱讀程式的限制：</span><span class="sxs-lookup"><span data-stu-id="fcce3-146">Note the following constraints for the current PDF reader:</span></span>

-  <span data-ttu-id="fcce3-147">XML 表單架構 (XFA) 是 Microsoft Edge 中不支援的舊版表單格式。</span><span class="sxs-lookup"><span data-stu-id="fcce3-147">XML Forms Architecture (XFA), is a legacy format of forms that isn't  supported in Microsoft Edge.</span></span>
-  <span data-ttu-id="fcce3-148">目前不支援之協助工具案例的相關文件，可在 [Microsoft 協助工具符合性報告](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) 的部落格中找到。</span><span class="sxs-lookup"><span data-stu-id="fcce3-148">Documentation related to Accessibility scenarios that currently aren't supported can be found on the [Microsoft Accessibility Conformance Reports](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) blog.</span></span>

## <span data-ttu-id="fcce3-149">功能</span><span class="sxs-lookup"><span data-stu-id="fcce3-149">Features</span></span>

<span data-ttu-id="fcce3-150">Microsoft Edge 內建的 PDF 閱讀程式隨附基本的閱讀和瀏覽功能，例如縮放、旋轉、符合頁面大小/寬度、跳至頁面，以及搜尋等等功能。</span><span class="sxs-lookup"><span data-stu-id="fcce3-150">The PDF reader, built into Microsoft Edge, comes with the basic reading and navigation features, as Zoom, Rotate, Fit to page/width, jump to page, and search, among others.</span></span> <span data-ttu-id="fcce3-151">透過 PDF 內容頂端的可釘選工具列即可存取這些功能。</span><span class="sxs-lookup"><span data-stu-id="fcce3-151">They can be accessed through a pin-able toolbar at the top of PDF content.</span></span> <span data-ttu-id="fcce3-152">本節提供一些重要功能的概觀。</span><span class="sxs-lookup"><span data-stu-id="fcce3-152">This section gives an overview of some important functions.</span></span> <span data-ttu-id="fcce3-153">下一個螢幕擷取畫面顯示 PDF 閱讀程式工具列。</span><span class="sxs-lookup"><span data-stu-id="fcce3-153">The next screenshot shows the PDF reader toolbar.</span></span>

![PDF 閱讀程式工具列](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <span data-ttu-id="fcce3-155">目錄</span><span class="sxs-lookup"><span data-stu-id="fcce3-155">Table of contents</span></span>

<span data-ttu-id="fcce3-156">目錄可讓使用者輕鬆瀏覽含有目錄的 PDF 文件。</span><span class="sxs-lookup"><span data-stu-id="fcce3-156">Table of contents lets users easily navigate through PDF documents that have a table of contents.</span></span> <span data-ttu-id="fcce3-157">當使用者按一下目錄圖示時，會顯示一個瀏覽窗格，其中顯示 PDF 文件中已加標籤的小節和子節的清單。</span><span class="sxs-lookup"><span data-stu-id="fcce3-157">When a user clicks the Table of contents icon, a navigation pane that  shows a list of the labeled sections and subsections in the PDF document is shown.</span></span> <span data-ttu-id="fcce3-158">然後，使用者可以按一下窗格中的任何標籤，瀏覽至文件的該小節。</span><span class="sxs-lookup"><span data-stu-id="fcce3-158">The user can then click any of the labels in the pane to navigate to that section of the document.</span></span> <span data-ttu-id="fcce3-159">窗格會在需要時維持開啟，並在使用者想要返回以閱讀文件時關閉。</span><span class="sxs-lookup"><span data-stu-id="fcce3-159">The pane stays open for as long as needed and can be closed when the user wants to go back to reading the document.</span></span> <span data-ttu-id="fcce3-160">下一個螢幕擷取畫面顯示已開啟文件的瀏覽窗格。</span><span class="sxs-lookup"><span data-stu-id="fcce3-160">The next screenshot shows the navigation pane for an open document.</span></span>

![使用目錄的 PDF 閱讀程式瀏覽](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <span data-ttu-id="fcce3-162">頁面檢視</span><span class="sxs-lookup"><span data-stu-id="fcce3-162">Page view</span></span>

<span data-ttu-id="fcce3-163">Microsoft Edge 在我們的 Dev 和 Canary 通道中支援對 PDF 文件使用不同的檢視。</span><span class="sxs-lookup"><span data-stu-id="fcce3-163">Microsoft Edge supports different views for PDF documents in our Dev and Canary channels.</span></span> <span data-ttu-id="fcce3-164">使用者可以將文件的版面配置從單一頁面檢視變更為並排顯示的兩個頁面。</span><span class="sxs-lookup"><span data-stu-id="fcce3-164">Users can change the layout of a document from a single page view to two pages that are displayed side by side.</span></span> <span data-ttu-id="fcce3-165">若要變更檢視 PDF 文件的方式，使用者可以按一下 PDF 工具列中的 [頁面檢視] 按鈕，然後選擇要使用的兩個檢視之一。</span><span class="sxs-lookup"><span data-stu-id="fcce3-165">To change how the PDF document is being viewed, users can click the Page View button in the PDF toolbar and then choose either view they want to use.</span></span> <span data-ttu-id="fcce3-166">下一個螢幕擷取畫面會顯示兩頁檢視。</span><span class="sxs-lookup"><span data-stu-id="fcce3-166">The two page view is shown in the next screenshot.</span></span>

![使用文件的兩頁檢視的 PDF 閱讀程式。](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <span data-ttu-id="fcce3-168">鍵盤模式瀏覽</span><span class="sxs-lookup"><span data-stu-id="fcce3-168">Caret mode browsing</span></span>

<span data-ttu-id="fcce3-169">於 Microsoft Edge 中開啟的 PDF 檔案中可使用鍵盤瀏覽，這表示使用者可以使用鍵盤與 PDF 檔案互動。</span><span class="sxs-lookup"><span data-stu-id="fcce3-169">Caret browsing is available for PDF files opened in Microsoft Edge, which means that users can interact with PDF files using the keyboard.</span></span> <span data-ttu-id="fcce3-170">如果使用者在瀏覽器中的任何位置按下 F7 鍵，系統會詢問他們是否要開啟鍵盤瀏覽。</span><span class="sxs-lookup"><span data-stu-id="fcce3-170">If a user presses the F7 key anywhere in the browser, they're asked if caret browsing should be turned on.</span></span> <span data-ttu-id="fcce3-171">如果啟用，就可以在瀏覽器開啟的任何內容 (無論是 PDF 檔案或網頁) 中使用鍵盤瀏覽。</span><span class="sxs-lookup"><span data-stu-id="fcce3-171">If enabled, caret browsing is available for any content opened in the browser, be it PDF files or web pages.</span></span> <span data-ttu-id="fcce3-172">當使用者再次按 F7 時，鍵盤瀏覽會關閉。</span><span class="sxs-lookup"><span data-stu-id="fcce3-172">When a user presses F7 again, caret browsing is turned off.</span></span> <span data-ttu-id="fcce3-173">當鍵盤瀏覽處於使用中狀態，且焦點位於內容上時，使用者會在 PDF 檔案中看到一個閃爍的游標。</span><span class="sxs-lookup"><span data-stu-id="fcce3-173">When caret browsing is active and the focus is on the content, users will see a blinking cursor in the PDF file.</span></span> <span data-ttu-id="fcce3-174">您也可以使用鍵盤瀏覽來瀏覽檔案，或在移動游標時按 Shift 來選取文字。</span><span class="sxs-lookup"><span data-stu-id="fcce3-174">The caret can also be used to navigate through the file, or to select text by pressing Shift while moving the cursor.</span></span> <span data-ttu-id="fcce3-175">此功能可讓使用者輕鬆地以醒目提示方式建立元素，或以連結的方式與元素互動，使用鍵盤形成欄位。</span><span class="sxs-lookup"><span data-stu-id="fcce3-175">This ability lets users easily create elements as highlights, or interact with elements as links, form fields with the keyboard.</span></span> <span data-ttu-id="fcce3-176">下一個螢幕擷取畫面顯示用於開啟鍵盤模式瀏覽的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="fcce3-176">The next screenshot shows the popup menu for turning on Caret mode browsing.</span></span>

![鍵盤模式瀏覽的 PDF 閱讀程式功能表。](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <span data-ttu-id="fcce3-178">筆跡</span><span class="sxs-lookup"><span data-stu-id="fcce3-178">Inking</span></span>

<span data-ttu-id="fcce3-179">PDF 檔案的筆跡功能可讓您輕鬆進行快速筆記，以便用於參照、簽署或填寫 PDF 表單。</span><span class="sxs-lookup"><span data-stu-id="fcce3-179">Inking on PDF files comes in handy to take quick notes for easy reference, sign, or fill out PDF forms.</span></span> <span data-ttu-id="fcce3-180">此功能現在可在 Microsoft Edge 中使用。</span><span class="sxs-lookup"><span data-stu-id="fcce3-180">This capability is now available in Microsoft Edge.</span></span> <span data-ttu-id="fcce3-181">除了筆跡 PDF 檔案，您也可以使用色彩和筆觸寬度為 PDF 檔案的不同部分引起注意。</span><span class="sxs-lookup"><span data-stu-id="fcce3-181">In addition to inking PDF files as needed, you can use color and stroke width to bring attention to different parts of the PDF file.</span></span> <span data-ttu-id="fcce3-182">下個螢幕擷取畫面顯示使用者如何將筆跡新增至 pdf 頁面。</span><span class="sxs-lookup"><span data-stu-id="fcce3-182">The next screenshot shows how a user can add inking to a pdf page.</span></span>

![將筆跡新增至 pdf 頁面](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <span data-ttu-id="fcce3-184">醒目顯示</span><span class="sxs-lookup"><span data-stu-id="fcce3-184">Highlight</span></span>

<span data-ttu-id="fcce3-185">Microsoft Edge 中的 PDF 閱讀程式隨附新增和編輯醒目提示的支援。</span><span class="sxs-lookup"><span data-stu-id="fcce3-185">PDF reader in Microsoft Edge comes with support for adding and editing highlights.</span></span> <span data-ttu-id="fcce3-186">若要建立醒目提示，使用者只需選取文字，按一下滑鼠右鍵，然後選取功能表中的 [醒目提示]，並選擇想要的色彩。</span><span class="sxs-lookup"><span data-stu-id="fcce3-186">To create a highlight, the user simply needs to select the text, right-click on it, select highlights in the menu and choose the desired color.</span></span> <span data-ttu-id="fcce3-187">您也可以使用手寫筆或鍵盤來建立醒目提示。</span><span class="sxs-lookup"><span data-stu-id="fcce3-187">Highlights can also be created using a pen, or keyboard.</span></span> <span data-ttu-id="fcce3-188">下一個螢幕擷取畫面顯示可用的醒目提示選項。</span><span class="sxs-lookup"><span data-stu-id="fcce3-188">The next screenshot shows the highlight options that are available.</span></span>

![使用 PDF 閱讀程式中的醒目提示選項](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <span data-ttu-id="fcce3-190">文字筆記</span><span class="sxs-lookup"><span data-stu-id="fcce3-190">Text notes</span></span>

<span data-ttu-id="fcce3-191">讀取 PDF 檔案時，您可以將文字筆記新增至檔案中的文字，以便日後快速參考。</span><span class="sxs-lookup"><span data-stu-id="fcce3-191">While reading a PDF file, text notes can be added to text in the file to jot down thoughts for easy reference later.</span></span>

<span data-ttu-id="fcce3-192">使用者可以新增筆記，方法是選取他們要新增筆記的文字片段，並叫用滑鼠右鍵內容功能表。</span><span class="sxs-lookup"><span data-stu-id="fcce3-192">Users can add a note by selecting the piece of text they wish to add a note for and invoking the right-click context menu.</span></span> <span data-ttu-id="fcce3-193">在功能表中選取 [新增註解]\*\*\*\* 選項，就會開啟一個文字方塊，使用者可以在其中新增其註解。</span><span class="sxs-lookup"><span data-stu-id="fcce3-193">Selecting the **Add Comment** option in the menu will open a text box where users can add their comments.</span></span> <span data-ttu-id="fcce3-194">他們可以輸入註解，然後按一下核取記號來儲存註解。</span><span class="sxs-lookup"><span data-stu-id="fcce3-194">They can type the comment and then click the check mark to save the comment.</span></span>

<span data-ttu-id="fcce3-195">新增筆記之後，系統會將選取的文字醒目提示，並且會出現註解圖示以表示註解。</span><span class="sxs-lookup"><span data-stu-id="fcce3-195">After a note is added, the selected text will be highlighted, and a comment icon will appear to indicate the comment.</span></span> <span data-ttu-id="fcce3-196">使用者可以將游標暫留在該圖示上以預覽註解，或按一下以開啟及編輯筆記。</span><span class="sxs-lookup"><span data-stu-id="fcce3-196">Users can hover over that icon to preview the comment or click on it to open and edit the note.</span></span>

<span data-ttu-id="fcce3-197">下一個螢幕擷取畫面顯示將筆記新增至醒目提示的文字。</span><span class="sxs-lookup"><span data-stu-id="fcce3-197">The next screenshot shows a note getting added to highlighted text.</span></span>

![PDF 閱讀程式將文字筆記新增至文件。](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <span data-ttu-id="fcce3-199">大聲朗讀</span><span class="sxs-lookup"><span data-stu-id="fcce3-199">Read aloud</span></span>

<span data-ttu-id="fcce3-200">PDF 的「大聲朗讀」功能為聆聽 PDF 內容增加了便利性，同時實現對使用者來說重要的其他工作。</span><span class="sxs-lookup"><span data-stu-id="fcce3-200">Read aloud for PDF adds the convenience of listening to PDF content while carrying out other tasks that may be important to users.</span></span> <span data-ttu-id="fcce3-201">這也有助於讓聽覺學習人士專注於內容，讓學習更輕鬆。</span><span class="sxs-lookup"><span data-stu-id="fcce3-201">It also helps auditory learners focus on the content, which makes learning much easier.</span></span> <span data-ttu-id="fcce3-202">下一個螢幕擷取畫面顯示大聲朗讀的範例。</span><span class="sxs-lookup"><span data-stu-id="fcce3-202">The next screenshot shows a Read aloud example.</span></span> <span data-ttu-id="fcce3-203">醒目提示會顯示目前正在朗讀的文字。</span><span class="sxs-lookup"><span data-stu-id="fcce3-203">The highlighting shows the text that is currently being read.</span></span>

![使用 PDF 閱讀程式中對大聲朗讀使用醒目提示選項](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <span data-ttu-id="fcce3-205">受保護的 PDF</span><span class="sxs-lookup"><span data-stu-id="fcce3-205">Protected PDFs</span></span>

<span data-ttu-id="fcce3-206">[Microsoft 資訊保護 (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide&preserve-view=true) 能讓使用者安全地與其他人共同作業，同時遵守貴組織的合規性原則。</span><span class="sxs-lookup"><span data-stu-id="fcce3-206">[Microsoft Information Protection (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide&preserve-view=true) enables users to collaborate with others securely, while adhering to your organization's compliance policies.</span></span> <span data-ttu-id="fcce3-207">檔案受到保護之後，使用者可對檔案執行的動作會由指派給他們的權限來決定。</span><span class="sxs-lookup"><span data-stu-id="fcce3-207">After a file is protected, the actions users can take on it are determined by the permissions assigned to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcce3-208">MIP 需要授權。</span><span class="sxs-lookup"><span data-stu-id="fcce3-208">A license is required for MIP.</span></span> <span data-ttu-id="fcce3-209">如需詳細資訊，請參閱此 [Microsoft 365 授權指引](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)。</span><span class="sxs-lookup"><span data-stu-id="fcce3-209">For more information, see this [Microsoft 365 licensing guidance](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection).</span></span>

<span data-ttu-id="fcce3-210">您可以直接在瀏覽器中開啟這些檔案，而不需要下載任何其他軟體，或安裝任何增益集。</span><span class="sxs-lookup"><span data-stu-id="fcce3-210">These files can be opened directly in the browser, without the need to download any other software, or install any add-in.</span></span> <span data-ttu-id="fcce3-211">此功能會將 MIP 所提供的安全性直接整合至瀏覽器，以提供流暢的工作流程。</span><span class="sxs-lookup"><span data-stu-id="fcce3-211">This capability integrates the security provided by MIP directly into the browser, providing a seamless workflow.</span></span>

![受保護的 PDF 文件。](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

<span data-ttu-id="fcce3-213">除了受 MIP 保護的檔案，[資訊版權管理 (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide&preserve-view=true)受保護 SharePoint 文件庫中的 PDF 檔案也可以在瀏覽器中以本機方式開啟。</span><span class="sxs-lookup"><span data-stu-id="fcce3-213">In addition to MIP protected files, PDF files in [Information Rights Management (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide&preserve-view=true) protected SharePoint libraries can also be opened natively in the browser.</span></span>

<span data-ttu-id="fcce3-214">有了 Microsoft Edge，使用者就能在本機或雲端中檢視受 MIP 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-214">With Microsoft Edge, users can view MIP protected files saved locally, or in the cloud.</span></span> <span data-ttu-id="fcce3-215">如果您已在本機儲存，可以直接在瀏覽器中開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-215">If saved locally, the file can be opened directly in the browser.</span></span> <span data-ttu-id="fcce3-216">如果檔案是從 SharePoint 雲端服務開啟 ，則使用者可能需要使用「在瀏覽器中開啟」選項。</span><span class="sxs-lookup"><span data-stu-id="fcce3-216">If the file is opened from a cloud service as SharePoint, the user may need to use the "Open in browser" option.</span></span>

<span data-ttu-id="fcce3-217">如果使用者登入 Microsoft Edge 的設定檔至少擁有該檔案的檢視權限，檔案就會在 Microsoft Edge 中開啟。</span><span class="sxs-lookup"><span data-stu-id="fcce3-217">If the profile that the user is logged into Microsoft Edge with has at least view permissions to the file, the file will open in Microsoft Edge.</span></span>

![提示儲存由 MIP 保護的 SharePoint PDF 頁面](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <span data-ttu-id="fcce3-219">檢視和驗證以憑證為基礎的數位簽章</span><span class="sxs-lookup"><span data-stu-id="fcce3-219">View and validate certificate-based digital signatures</span></span>

<span data-ttu-id="fcce3-220">在此數位世界中，建立文件中內容的真實性及擁有權變得更為重要。</span><span class="sxs-lookup"><span data-stu-id="fcce3-220">In this digital world, it becomes important to establish the authenticity and ownership of the content in the document.</span></span> <span data-ttu-id="fcce3-221">一般會在 PDF 文件中使用以憑證為基礎的數位簽章，以確保文件中的內容與作者預期的相同，且尚未變更。</span><span class="sxs-lookup"><span data-stu-id="fcce3-221">Certificate-based digital signatures are commonly used in PDF documents to ensure that the content in the document is the same as what the author intended it to be, and has not been changed.</span></span> <span data-ttu-id="fcce3-222">利用 Microsoft Edge，您就可以檢視和驗證 PDF 中憑證的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="fcce3-222">With Microsoft Edge, you can view and validate certificate digital signatures in PDFs.</span></span>

<span data-ttu-id="fcce3-223">我們正積極努力改善支援，以解決更多案例，並同樣期待收到您的意見反應。</span><span class="sxs-lookup"><span data-stu-id="fcce3-223">We’re actively working on improving the support to address more scenarios, and are looking forward for feedback about the same.</span></span>

## <span data-ttu-id="fcce3-224">協助工具</span><span class="sxs-lookup"><span data-stu-id="fcce3-224">Accessibility</span></span>

<span data-ttu-id="fcce3-225">PDF 閱讀程式隨附支援鍵盤協助工具、高對比模式，以及 支援 Windows 和 macOS 裝置的螢幕助讀程式。</span><span class="sxs-lookup"><span data-stu-id="fcce3-225">The PDF reader comes with support for Keyboard accessibility, High contrast mode, and screen reader support across Windows and macOS devices.</span></span>

### <span data-ttu-id="fcce3-226">鍵盤協助工具</span><span class="sxs-lookup"><span data-stu-id="fcce3-226">Keyboard Accessibility</span></span>

<span data-ttu-id="fcce3-227">使用者可以使用鍵盤瀏覽至文件中可與使用者互動的不同部分，例如表單欄位和醒目提示。</span><span class="sxs-lookup"><span data-stu-id="fcce3-227">Users can use navigate to different parts of the document that a user can interact with, such as form fields and highlights, using the keyboard.</span></span> <span data-ttu-id="fcce3-228">使用者也可以使用鍵盤模式來瀏覽，並利用鍵盤與 PDF 檔案互動。</span><span class="sxs-lookup"><span data-stu-id="fcce3-228">Users can also use Caret mode to navigate and interact with the PDF files using the keyboard.</span></span>

### <span data-ttu-id="fcce3-229">高對比模式</span><span class="sxs-lookup"><span data-stu-id="fcce3-229">High contrast mode</span></span>

<span data-ttu-id="fcce3-230">PDF 閱讀程式會使用作業系統層級定義的設定，在高對比模式下呈現 PDF 內容。</span><span class="sxs-lookup"><span data-stu-id="fcce3-230">PDF reader will use the settings defined at the operating system level to render PDF content in high contrast mode.</span></span>

### <span data-ttu-id="fcce3-231">支援螢幕助讀程式</span><span class="sxs-lookup"><span data-stu-id="fcce3-231">Screen reader support</span></span>

<span data-ttu-id="fcce3-232">使用者可以使用 Windows 和 Mac 電腦上的螢幕助讀程式瀏覽和讀取 PDF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-232">Users can navigate through and read PDF files using screen readers on Windows and Mac computers.</span></span>

## <span data-ttu-id="fcce3-233">安全性和可靠性</span><span class="sxs-lookup"><span data-stu-id="fcce3-233">Security and reliability</span></span>

<span data-ttu-id="fcce3-234">安全性是任何組織最重要的原則。</span><span class="sxs-lookup"><span data-stu-id="fcce3-234">Security is among the most important tenets for any organization.</span></span> <span data-ttu-id="fcce3-235">PDF 閱讀程式安全性是 Microsoft Edge 安全性設計不可或缺的一部分。</span><span class="sxs-lookup"><span data-stu-id="fcce3-235">PDF reader security is an integral part of the Microsoft Edge security design.</span></span> <span data-ttu-id="fcce3-236">從 PDF 閱讀程式最重要的兩個安全性功能之角度來看，兩個重要的安全性功能是「處理程序隔離」和「Microsoft Defender 應用程式防護」(應用程式防護)。</span><span class="sxs-lookup"><span data-stu-id="fcce3-236">Two of the most important security features From a PDF reader perspective, two important security features are process isolation and Microsoft Defender Application Guard (Application Guard).</span></span>

- <span data-ttu-id="fcce3-237">處理程序隔離。</span><span class="sxs-lookup"><span data-stu-id="fcce3-237">Process isolation.</span></span> <span data-ttu-id="fcce3-238">從不同網站開啟的 PDF 完全是處理程序隔離。</span><span class="sxs-lookup"><span data-stu-id="fcce3-238">PDFs opened from different web sites are completely process isolated.</span></span> <span data-ttu-id="fcce3-239">瀏覽器不需要與從任何網站或其他來源開啟的 PDF 檔案進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fcce3-239">The browser doesn't have to communicate with any websites, or PDF files opened from another source.</span></span> <span data-ttu-id="fcce3-240">PDF 瀏覽是安全的，不受任何計畫使用被感染的 PDF 作為攻擊面的任何威脅。</span><span class="sxs-lookup"><span data-stu-id="fcce3-240">PDF browsing is secure from any attacks that plan to use compromised PDFs as an attack surface.</span></span>

- <span data-ttu-id="fcce3-241">應用程式防護。</span><span class="sxs-lookup"><span data-stu-id="fcce3-241">Application Guard.</span></span> <span data-ttu-id="fcce3-242">使用應用程式防護，系統管理員可以設定組織信任的網站清單。</span><span class="sxs-lookup"><span data-stu-id="fcce3-242">With Application Guard, admins can set a list of sites that are trusted by their organization.</span></span> <span data-ttu-id="fcce3-243">如果使用者開啟任何其他網站，則會在單獨的應用程式防護視窗中開啟，並在自己的容器中執行。</span><span class="sxs-lookup"><span data-stu-id="fcce3-243">If users open any other sites, they are opened in a separate Application Guard window that runs in its own container.</span></span> <span data-ttu-id="fcce3-244">容器可協助保護公司網路，並防止使用者電腦上的任何資料遭盜用。</span><span class="sxs-lookup"><span data-stu-id="fcce3-244">The container helps protect the corporate network and any data on user's computer from being compromised.</span></span><br><br>
<span data-ttu-id="fcce3-245">這種保護也適用於任何已檢視的線上 PDF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcce3-245">This protection also applies to any online PDF files that are viewed.</span></span> <span data-ttu-id="fcce3-246">此外，將會儲存從應用程式防護視窗下載的任何 PDF 檔案，並在該容器中重新開啟。</span><span class="sxs-lookup"><span data-stu-id="fcce3-246">Further, any PDF files that are downloaded from an Application Guard window are stored, and when needed, re-opened in the container.</span></span> <span data-ttu-id="fcce3-247">這不僅在檔案下載時，而且在整個生命週期中都能確保環境的安全。</span><span class="sxs-lookup"><span data-stu-id="fcce3-247">This helps keeps your environment secure not just when the file is downloaded, but through its whole lifecycle.</span></span> <span data-ttu-id="fcce3-248">如需詳細資訊，請參閱 [應用程式防護](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard)。</span><span class="sxs-lookup"><span data-stu-id="fcce3-248">For more information, see [Application Guard](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard).</span></span>

### <span data-ttu-id="fcce3-249">可靠性</span><span class="sxs-lookup"><span data-stu-id="fcce3-249">Reliability</span></span>

<span data-ttu-id="fcce3-250">由於 Microsoft Edge 是以 Chromium 為基礎開發的，因此使用者預期可獲得與以 Chromium 為基礎的瀏覽器中相同的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="fcce3-250">Because Microsoft Edge is Chromium-based, users can expect the same level of reliability that they're used to seeing in other Chromium-based browsers.</span></span>

## <span data-ttu-id="fcce3-251">部署和更新 PDF 閱讀程式</span><span class="sxs-lookup"><span data-stu-id="fcce3-251">Deploy and update PDF reader</span></span>

<span data-ttu-id="fcce3-252">PDF 閱讀程式會與 Microsoft Edge 瀏覽器的其餘部分一起部署並更新。</span><span class="sxs-lookup"><span data-stu-id="fcce3-252">The PDF reader gets deployed and updated with the rest of the Microsoft Edge browser.</span></span> <span data-ttu-id="fcce3-253">若要深入了解如何部署 Microsoft Edge，請觀看[將 Microsoft Edge 部署到成百或上千個裝置](microsoft-edge-video-deploy.md)影片。</span><span class="sxs-lookup"><span data-stu-id="fcce3-253">To learn more about deploying Microsoft Edge, watch the [Deploy Microsoft Edge to hundreds or thousands of devices](microsoft-edge-video-deploy.md) video.</span></span> <span data-ttu-id="fcce3-254">您也可以在 [Microsoft Edge 文件](https://docs.microsoft.com/DeployEdge/)登陸頁面上找到更多部署資訊。</span><span class="sxs-lookup"><span data-stu-id="fcce3-254">You can also find more deployment information on the [Microsoft Edge documentation](https://docs.microsoft.com/DeployEdge/) landing page.</span></span>

> [!TIP]
> <span data-ttu-id="fcce3-255">您可以讓 Microsoft Edge 成為貴組織預設的 PDF 閱讀程式。</span><span class="sxs-lookup"><span data-stu-id="fcce3-255">You can make Microsoft Edge the default PDF reader for your organization.</span></span> <span data-ttu-id="fcce3-256">若要這樣做，[請執行下列步驟](https://docs.microsoft.com/deployedge/edge-default-browser)。</span><span class="sxs-lookup"><span data-stu-id="fcce3-256">To do this, [follow these steps](https://docs.microsoft.com/deployedge/edge-default-browser).</span></span>

## <span data-ttu-id="fcce3-257">藍圖與意見反應</span><span class="sxs-lookup"><span data-stu-id="fcce3-257">Roadmap and feedback</span></span>

<span data-ttu-id="fcce3-258">Microsoft Edge 中 PDF 閱讀程式的藍圖可在[這裡](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667)取得。</span><span class="sxs-lookup"><span data-stu-id="fcce3-258">The roadmap for PDF reader in Microsoft Edge is available [here](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667).</span></span>

<span data-ttu-id="fcce3-259">我們正在積極查看對您重要功能的意見反應。</span><span class="sxs-lookup"><span data-stu-id="fcce3-259">We're actively looking at feedback from you about the features you find important.</span></span> <span data-ttu-id="fcce3-260">歡迎您透過 [Microsoft edge UserVoice](https://microsoftedge.uservoice.com/) 和 [Microsoft Edge 測試人員](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) 論壇，將意見反應傳送給我們。</span><span class="sxs-lookup"><span data-stu-id="fcce3-260">Feel free to send us feedback through [Microsoft Edge UserVoice](https://microsoftedge.uservoice.com/) and on [Microsoft Edge Insider](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) forum.</span></span>

## <span data-ttu-id="fcce3-261">請參閱</span><span class="sxs-lookup"><span data-stu-id="fcce3-261">See also</span></span>

- [<span data-ttu-id="fcce3-262">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="fcce3-262">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fcce3-263">Microsoft 365 藍圖</span><span class="sxs-lookup"><span data-stu-id="fcce3-263">Microsoft 365 Roadmap</span></span>](https://www.microsoft.com/microsoft-365/roadmap)
- [<span data-ttu-id="fcce3-264">影片：Microsoft Edge 企業級 PDF 閱讀程式</span><span class="sxs-lookup"><span data-stu-id="fcce3-264">Video: Microsoft Edge enterprise grade PDF reader</span></span>](microsoft-edge-video-pdf-reader.md)