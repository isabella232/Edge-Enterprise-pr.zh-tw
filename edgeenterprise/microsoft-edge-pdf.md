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
# Microsoft Edge 的 PDF 閱讀程式

PDF 檔案是我們日常生活的一部分。 它們以合約和協議、電子報、表單、研究文章、履歷等的形式出現。 這些檔案突顯了供企業使用的可靠、安全且功能強大的 PDF 閱讀程式之需求。

Microsoft Edge 隨附內建的 PDF 閱讀程式，可讓您開啟本機 pdf 檔案、線上 pdf 檔案，或內嵌在網頁中的 pdf 檔案。 您可以使用筆跡和醒目提示來標註這些檔案。 這個 PDF 閱讀程式會為使用者提供單一應用程式，以符合網頁和 PDF 文件的需求。 Microsoft Edge PDF 閱讀程式是一種安全且可靠的應用程式，可在 Windows 和 macOS 桌面平台上運作。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 必要條件、支援及限制

下表顯示支援 PDF 閱讀程式各種功能的 Microsoft Edge 頻道和版本 。

| 功能 | 穩定通道版本 |
|---------|------------------------|
| 檢視及列印本機、線上及內嵌的 PDF 檔案 | 79.0.309.71                |
| 基本表單填寫<br>(不支援 JavaScript 表單) | 79.0.309.71           |
| 筆跡  | 80.0.361.48            |
| 筆跡自訂 | 83.0.478.54  |
| 醒目顯示  | 81.0.416.53         |
| 大聲朗讀 | 目前正在 [Microsoft Edge 測試人員](https://www.microsoftedgeinsider.com/) 頻道中進行推廣 |
| 檢視受 MIP 保護的檔案 | 80.0.361.48 支援 Windows 版<br>81.0.416.53 支援 Mac 版 |
|  檢視受 IRM 保護的檔案  | 83.0.478.37            |

### 限制式

請注意以下目前 PDF 閱讀程式的限制：

-  XML 表單架構 (XFA) 是 Microsoft Edge 中不支援的舊版表單格式。
-  目前不支援之協助工具案例的相關文件，可在 [Microsoft 協助工具符合性報告](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/) 的部落格中找到。

## 功能

### 筆跡

PDF 檔案的筆跡功能可讓您輕鬆進行快速筆記，以便用於參照、簽署或填寫 PDF 表單。 此功能現在可在 Microsoft Edge 中使用。 除了筆跡 PDF 檔案，您也可以使用色彩和筆觸寬度為 PDF 檔案的不同部分引起注意。 下個螢幕擷取畫面顯示使用者如何將筆跡新增至 pdf 頁面。

<!-- SCREENSHOT -->
![將筆跡新增至 pdf 頁面](media/microsoft-edge-pdf/pdf-reader-inking.png)

### 醒目顯示

Microsoft Edge 中的 PDF 閱讀程式隨附新增和編輯醒目提示的支援。 若要建立醒目提示，使用者只需選取文字，按一下滑鼠右鍵，然後選取功能表中的 [醒目提示]，並選擇想要的色彩。 下個螢幕擷取畫面顯示可用的醒目提示選項。

![使用 PDF 閱讀程式中的 [醒目提示] 選項](media/microsoft-edge-pdf/pdf-reader-highlight.png)

### 大聲朗讀

PDF 的大聲朗讀功能新增聆聽 PDF 內容的方便性，並讓使用者同時執行其他重要的工作。 這也有助於讓聽覺學習人士專注於內容，讓學習更輕鬆。 下個螢幕擷取畫面顯示 [大聲朗讀] 範例。 [醒目提示] 會顯示目前正在閱讀的文字。

![使用 PDF 閱讀程式中的 [醒目提示] 選項](media/microsoft-edge-pdf/pdf-reader-read-aloud-example.png)

### 受保護的 PDF

[Microsoft 資訊保護 (MIP)](https://docs.microsoft.com/microsoft-365/compliance/protect-information?view=o365-worldwide) 能讓使用者安全地與其他人共同作業，同時遵守貴組織的合規性原則。 檔案受到保護之後，使用者可對檔案執行的動作會由指派給他們的權限來決定。

您可以直接在瀏覽器中開啟這些檔案，而不需要下載任何其他軟體，或安裝任何增益集。 這會將 MIP 所提供的安全性直接整合至瀏覽器，以提供流暢的工作流程。

<!-- SCREENSHOT -->
![受保護的 pdf 文件。](media/microsoft-edge-pdf/pdf-reader-protected-pdf2.png)

除了受 MIP 保護的檔案，[資訊版權管理 (IRM)](https://docs.microsoft.com/microsoft-365/compliance/set-up-irm-in-sp-admin-center?view=o365-worldwide)受保護 SharePoint 文件庫中的 PDF 檔案也可以在瀏覽器中以本機方式開啟。

有了 Microsoft Edge，使用者就能在本機或雲端中檢視受 MIP 保護的檔案。 如果您已在本機儲存，可以直接在瀏覽器中開啟檔案。 如果檔案是從 SharePoint 雲端服務開啟 ，則使用者可能需要使用「在瀏覽器中開啟」選項。

如果使用者登入 Microsoft Edge 的設定檔至少擁有該檔案的檢視權限，檔案就會在 Microsoft Edge 中開啟。

<!-- SCREENSHOT -->
![提示儲存由 MIP 保護的 SharePoint pdf 頁面](media/microsoft-edge-pdf/pdf-reader-sharepoint-irm.png)

## 協助工具

PDF 閱讀程式隨附支援鍵盤協助工具、高對比模式，以及 支援 Windows 和 macOS 裝置的螢幕助讀程式。

### 鍵盤協助工具

使用者可以使用鍵盤瀏覽至文件中可與使用者互動的不同部分，例如表單欄位和醒目提示。

<!-- SCREENSHOT -->

### 高對比模式

PDF 閱讀程式會使用作業系統層級定義的設定，在高對比模式下呈現 PDF 內容。

<!-- SCREENSHOT -->
<!--![High contrast mode for pdf file](media/microsoft-edge-pdf/pdf-reader-high-contrast.png)-->

### 支援螢幕助讀程式

使用者可以使用 Windows 和 Mac 電腦上的螢幕助讀程式瀏覽和讀取 PDF 檔案。 <!--The next screenshot shows the toolbar that users can use for audio settings when they're using the Read Aloud option in PDF reader. -->

<!-- SCREENSHOT -->
<!--
![Screen reader toolbar](media/microsoft-edge-pdf/pdf-reader-read-aloud.png) -->

## 安全性和可靠性

安全性是任何組織最重要的原則。 PDF 閱讀程式安全性是 Microsoft Edge 安全性設計不可或缺的一部分。 從 PDF 閱讀程式最重要的兩個安全性功能之角度來看，兩個重要的安全性功能是「處理程序隔離」和「Microsoft Defender 應用程式防護」(應用程式防護)。

- 處理程序隔離。 從不同網站開啟的 PDF 完全是處理程序隔離。 瀏覽器不需要與從任何網站或其他來源開啟的 PDF 檔案進行通訊。 PDF 瀏覽是安全的，不受任何計畫使用被感染的 PDF 作為攻擊面的任何威脅。

- 應用程式防護。 使用應用程式防護，系統管理員可以設定組織信任的網站清單。 如果使用者開啟任何其他網站，則會在單獨的應用程式防護視窗中開啟，並在自己的容器中執行。 容器可協助保護公司網路，並防止使用者電腦上的任何資料遭盜用。<br><br>
這種保護也適用於任何已檢視的線上 PDF 檔案。 此外，將會儲存從應用程式防護視窗下載的任何 PDF 檔案，並在該容器中重新開啟。 這不僅在檔案下載時，而且在整個生命週期中都能確保環境的安全。 如需詳細資訊，請參閱 [應用程式防護](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-defender-application-guard)。

### 可靠性

由於 Microsoft Edge 是以 Chromium 為基礎開發的，因此使用者的可靠性層級與 Google Chrome 中所用的可靠性層級相同。

## 部署和更新 PDF 閱讀程式

PDF 閱讀程式會與 Microsoft Edge 瀏覽器的其餘部分一起部署並更新。 若要深入了解如何部署 Microsoft Edge，請觀看[將 Microsoft Edge 部署到成百或上千個裝置](microsoft-edge-video-deploy.md)影片。 您也可以在 [Microsoft Edge 文件](https://docs.microsoft.com/DeployEdge/)登陸頁面上找到更多部署資訊。

> [!TIP]
> 您可以讓 Microsoft Edge 成為貴組織預設的 PDF 閱讀程式。 若要這樣做，[請執行下列步驟](https://docs.microsoft.com/deployedge/edge-default-browser)。

## 藍圖與意見反應

Microsoft Edge 的 PDF 閱讀程式藍圖可在 [此處](https://techcommunity.microsoft.com/t5/articles/roadmap-for-pdf-reader-in-microsoft-edge/m-p/1467667) 獲得。

我們正在積極查看對您重要功能的意見反應。 歡迎您透過 [Microsoft edge UserVoice](https://microsoftedge.uservoice.com/) 和 [Microsoft Edge 測試人員](https://techcommunity.microsoft.com/t5/microsoft-edge-insider/ct-p/MicrosoftEdgeInsider) 論壇，將意見反應傳送給我們。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)