---
title: Microsoft Edge 的 PDF 閱讀程式
ms.author: adigan
author: dan-wesley
manager: balajek
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Microsoft Edge 的 PDF 閱讀程式。
ms.openlocfilehash: 342f6702ff0da3305c037112555549b0d5503d3c
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447837"
---
# <a name="pdf-reader-in-microsoft-edge"></a>Microsoft Edge 的 PDF 閱讀程式

PDF 檔案佔據我們日常生活的一大部分。 它們以合約和協議、電子報、表單、研究文章、履歷等的形式出現。 這些檔案突顯了供企業使用的可靠、安全且功能強大的 PDF 閱讀程式之需求。

Microsoft Edge 隨附內建的 PDF 閱讀程式，可讓您開啟本機 pdf 檔案、線上 pdf 檔案，或內嵌在網頁中的 pdf 檔案。 您可以使用筆跡和醒目提示來標註這些檔案。 這個 PDF 閱讀程式會為使用者提供單一應用程式，以符合網頁和 PDF 文件的需求。 Microsoft Edge PDF 閱讀程式是一種安全且可靠的應用程式，可在 Windows 和 macOS 桌面平台上運作。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="prerequisites-support-and-constraints"></a>必要條件、支援及限制

下表顯示支援 PDF 閱讀程式各種功能的 Microsoft Edge 頻道和版本 。

| 功能 | 穩定通道版本 |
|---------|------------------------|
| 檢視及列印本機、線上及內嵌的 PDF 檔案 | 79.0.309.71                |
| 基本表單填寫<br>(不支援 JavaScript 表單) | 79.0.309.71           |
|目錄| 86.0.622.38 |
| 頁面檢視 |目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/)通道中推廣 |
| 鍵盤模式瀏覽 |87.0.664.41 |
| 筆跡  | 80.0.361.48            |
| 筆跡自訂 | 83.0.478.54  |
| 醒目顯示  | 81.0.416.53         |
| 文字筆記 | 目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/)通道中推廣 |
| 大聲朗讀 | 84.0.522.63  |
| 檢視受 Microsoft 資訊保護 (MIP) 保護的檔案 | Windows 支援使用 80.0.361.48<br>Mac 支援使用 81.0.416.53 |
|  檢視受資訊版權管理 (IRM) 保護的檔案  | 83.0.478.37            |
| 檢視和驗證數位簽章 | 在 Canary 和 Dev 通道中提供。 正在積極處理。 |

### <a name="constraints"></a>限制式

請注意以下目前 PDF 閱讀程式的限制：

-  XML 表單架構 (XFA) 是 Microsoft Edge 中不支援的舊版表單格式。
-  目前不支援之協助工具案例的相關文件，可在 [Microsoft 協助工具符合性報告](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) 的部落格中找到。

## <a name="features"></a>功能

Microsoft Edge 內建的 PDF 閱讀程式隨附基本的閱讀和瀏覽功能，例如縮放、旋轉、符合頁面大小/寬度、跳至頁面，以及搜尋等等功能。 透過 PDF 內容頂端的可釘選工具列即可存取這些功能。 本節提供一些重要功能的概觀。 下一個螢幕擷取畫面顯示 PDF 閱讀程式工具列。

![PDF 閱讀程式工具列](media/microsoft-edge-pdf/pdf-reader-toolbar.png)

### <a name="table-of-contents"></a>目錄

目錄可讓使用者輕鬆瀏覽含有目錄的 PDF 文件。 當使用者按一下目錄圖示時，會顯示一個瀏覽窗格，其中顯示 PDF 文件中已加標籤的小節和子節的清單。 然後，使用者可以按一下窗格中的任何標籤，瀏覽至文件的該小節。 窗格會在需要時維持開啟，並在使用者想要返回以閱讀文件時關閉。 下一個螢幕擷取畫面顯示已開啟文件的瀏覽窗格。

![使用目錄的 PDF 閱讀程式瀏覽](media/microsoft-edge-pdf/pdf-reader-toc.png)

### <a name="page-view"></a>頁面檢視

Microsoft Edge 在我們的 Dev 和 Canary 通道中支援對 PDF 文件使用不同的檢視。 使用者可以將文件的版面配置從單一頁面檢視變更為並排顯示的兩個頁面。 若要變更檢視 PDF 文件的方式，使用者可以按一下 PDF 工具列中的 [頁面檢視] 按鈕，然後選擇要使用的兩個檢視之一。 下一個螢幕擷取畫面會顯示兩頁檢視。

![使用文件的兩頁檢視的 PDF 閱讀程式。](media/microsoft-edge-pdf/pdf-reader-page-view.png)

### <a name="caret-mode-browsing"></a>鍵盤模式瀏覽

於 Microsoft Edge 中開啟的 PDF 檔案中可使用鍵盤瀏覽，這表示使用者可以使用鍵盤與 PDF 檔案互動。 如果使用者在瀏覽器中的任何位置按下 F7 鍵，系統會詢問他們是否要開啟鍵盤瀏覽。 如果啟用，就可以在瀏覽器開啟的任何內容 (無論是 PDF 檔案或網頁) 中使用鍵盤瀏覽。 當使用者再次按 F7 時，鍵盤瀏覽會關閉。 當鍵盤瀏覽處於使用中狀態，且焦點位於內容上時，使用者會在 PDF 檔案中看到一個閃爍的游標。 您也可以使用鍵盤瀏覽來瀏覽檔案，或在移動游標時按 Shift 來選取文字。 此功能可讓使用者輕鬆地以醒目提示方式建立元素，或以連結的方式與元素互動，使用鍵盤形成欄位。 下一個螢幕擷取畫面顯示用於開啟鍵盤模式瀏覽的快顯功能表。

![鍵盤模式瀏覽的 PDF 閱讀程式功能表。](media/microsoft-edge-pdf/pdf-reader-caret-mode.png)

### <a name="inking"></a>筆跡

PDF 檔案的筆跡功能可讓您輕鬆進行快速筆記，以便用於參照、簽署或填寫 PDF 表單。 此功能現在可在 Microsoft Edge 中使用。 除了筆跡 PDF 檔案，您也可以使用色彩和筆觸寬度為 PDF 檔案的不同部分引起注意。 下個螢幕擷取畫面顯示使用者如何將筆跡新增至 pdf 頁面。

![將筆跡新增至 pdf 頁面](media/microsoft-edge-pdf/pdf-reader-inking.png)

### <a name="highlight"></a>醒目顯示

Microsoft Edge 中的 PDF 閱讀程式隨附新增和編輯醒目提示的支援。 若要建立醒目提示，使用者只需選取文字，按一下滑鼠右鍵，然後選取功能表中的 [醒目提示]，並選擇想要的色彩。 您也可以使用手寫筆或鍵盤來建立醒目提示。 下一個螢幕擷取畫面顯示可用的醒目提示選項。

![使用 PDF 閱讀程式中的醒目提示選項](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### <a name="text-notes"></a>文字筆記

讀取 PDF 檔案時，您可以將文字筆記新增至檔案中的文字，以便日後快速參考。

使用者可以新增筆記，方法是選取他們要新增筆記的文字片段，並叫用滑鼠右鍵內容功能表。 在功能表中選取 [新增註解]**** 選項，就會開啟一個文字方塊，使用者可以在其中新增其註解。 他們可以輸入註解，然後按一下核取記號來儲存註解。

新增筆記之後，系統會將選取的文字醒目提示，並且會出現註解圖示以表示註解。 使用者可以將游標暫留在該圖示上以預覽註解，或按一下以開啟及編輯筆記。

下一個螢幕擷取畫面顯示將筆記新增至醒目提示的文字。

![PDF 閱讀程式將文字筆記新增至文件。](media/microsoft-edge-pdf/pdf-reader-text-note.png)

### <a name="read-aloud"></a>大聲朗讀

PDF 的「大聲朗讀」功能為聆聽 PDF 內容增加了便利性，同時實現對使用者來說重要的其他工作。 這也有助於讓聽覺學習人士專注於內容，讓學習更輕鬆。 下一個螢幕擷取畫面顯示大聲朗讀的範例。 醒目提示會顯示目前正在朗讀的文字。

![使用 PDF 閱讀程式中對大聲朗讀使用醒目提示選項](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### <a name="protected-pdfs"></a>受保護的 PDF

[Microsoft 資訊保護 (MIP)](/microsoft-365/compliance/protect-information?preserve-view=true&view=o365-worldwide) 能讓使用者安全地與其他人共同作業，同時遵守貴組織的合規性原則。 檔案受到保護之後，使用者可對檔案執行的動作會由指派給他們的權限來決定。

> [!IMPORTANT]
> MIP 需要授權。 如需詳細資訊，請參閱此 [Microsoft 365 授權指引](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#information-protection)。

您可以直接在瀏覽器中開啟這些檔案，而不需要下載任何其他軟體，或安裝任何增益集。 此功能會將 MIP 所提供的安全性直接整合至瀏覽器，以提供流暢的工作流程。

![受保護的 PDF 文件。](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

除了受 MIP 保護的檔案，[資訊版權管理 (IRM)](/microsoft-365/compliance/set-up-irm-in-sp-admin-center?preserve-view=true&view=o365-worldwide)受保護 SharePoint 文件庫中的 PDF 檔案也可以在瀏覽器中以本機方式開啟。

有了 Microsoft Edge，使用者就能在本機或雲端中檢視受 MIP 保護的檔案。 如果您已在本機儲存，可以直接在瀏覽器中開啟檔案。 如果檔案是從 SharePoint 雲端服務開啟 ，則使用者可能需要使用「在瀏覽器中開啟」選項。

如果使用者登入 Microsoft Edge 的設定檔至少擁有該檔案的檢視權限，檔案就會在 Microsoft Edge 中開啟。

![提示儲存由 MIP 保護的 SharePoint PDF 頁面](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

### <a name="view-and-validate-certificate-based-digital-signatures"></a>檢視和驗證以憑證為基礎的數位簽章

在此數位世界中，建立文件中內容的真實性及擁有權變得更為重要。 一般會在 PDF 文件中使用以憑證為基礎的數位簽章，以確保文件中的內容與作者預期的相同，且尚未變更。 利用 Microsoft Edge，您就可以檢視和驗證 PDF 中憑證的數位簽章。

我們正積極努力改善支援，以解決更多案例，並同樣期待收到您的意見反應。

## <a name="accessibility"></a>協助工具

PDF 閱讀程式隨附支援鍵盤協助工具、高對比模式，以及 支援 Windows 和 macOS 裝置的螢幕助讀程式。

### <a name="keyboard-accessibility"></a>鍵盤協助工具

使用者可以使用鍵盤瀏覽至文件中可與使用者互動的不同部分，例如表單欄位和醒目提示。 使用者也可以使用鍵盤模式來瀏覽，並利用鍵盤與 PDF 檔案互動。

### <a name="high-contrast-mode"></a>高對比模式

PDF 閱讀程式會使用作業系統層級定義的設定，在高對比模式下呈現 PDF 內容。

### <a name="screen-reader-support"></a>支援螢幕助讀程式

使用者可以使用 Windows 和 Mac 電腦上的螢幕助讀程式瀏覽和讀取 PDF 檔案。

## <a name="security-and-reliability"></a>安全性和可靠性

安全性是任何組織最重要的原則。 PDF 閱讀程式安全性是 Microsoft Edge 安全性設計不可或缺的一部分。 從 PDF 閱讀程式最重要的兩個安全性功能之角度來看，兩個重要的安全性功能是「處理程序隔離」和「Microsoft Defender 應用程式防護」(應用程式防護)。

- 處理程序隔離。 從不同網站開啟的 PDF 完全是處理程序隔離。 瀏覽器不需要與從任何網站或其他來源開啟的 PDF 檔案進行通訊。 PDF 瀏覽是安全的，不受任何計畫使用被感染的 PDF 作為攻擊面的任何威脅。

- 應用程式防護。 使用應用程式防護，系統管理員可以設定組織信任的網站清單。 如果使用者開啟任何其他網站，則會在單獨的應用程式防護視窗中開啟，並在自己的容器中執行。 容器可協助保護公司網路，並防止使用者電腦上的任何資料遭盜用。<br><br>
這種保護也適用於任何已檢視的線上 PDF 檔案。 此外，將會儲存從應用程式防護視窗下載的任何 PDF 檔案，並在該容器中重新開啟。 這不僅在檔案下載時，而且在整個生命週期中都能確保環境的安全。 如需詳細資訊，請參閱 [應用程式防護](./microsoft-edge-security-windows-defender-application-guard.md)。

### <a name="reliability"></a>可靠性

由於 Microsoft Edge 是以 Chromium 為基礎開發的，因此使用者預期可獲得與以 Chromium 為基礎的瀏覽器中相同的可靠性層級。

## <a name="deploy-and-update-pdf-reader"></a>部署和更新 PDF 閱讀程式

PDF 閱讀程式會與 Microsoft Edge 瀏覽器的其餘部分一起部署並更新。 若要深入了解如何部署 Microsoft Edge，請觀看[將 Microsoft Edge 部署到成百或上千個裝置](microsoft-edge-video-deploy.md)影片。 您也可以在 [Microsoft Edge 文件](./index.yml)登陸頁面上找到更多部署資訊。

> [!TIP]
> 您可以讓 Microsoft Edge 成為貴組織預設的 PDF 閱讀程式。 若要這樣做，[請執行下列步驟](./edge-default-browser.md)。

## <a name="roadmap-and-feedback"></a>藍圖與意見反應

Microsoft Edge 中 PDF 閱讀程式的藍圖可在[這裡](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667)取得。

我們正在積極查看您對重要功能的意見反應。 歡迎隨時透過 [Microsoft Edge 測試人員](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider)論壇傳送意見反應給我們。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft 365 藍圖](https://www.microsoft.com/microsoft-365/roadmap)
- [影片：Microsoft Edge 企業級 PDF 閱讀程式](microsoft-edge-video-pdf-reader.md)