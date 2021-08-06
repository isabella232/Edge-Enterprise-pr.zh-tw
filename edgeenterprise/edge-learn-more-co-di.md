---
title: Microsoft Edge 中的 ClickOnce 和 DirectInvoke
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/16/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 深入了解 Microsoft Edge 中的 ClickOnce 和 DirectInvoke。
ms.openlocfilehash: bd4d189a578f0331671cc70fc34c195693d6f5c123dfd0d83052cbc9d949f536
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724462"
---
# <a name="understand-the-clickonce-and-directinvoke-features-in-microsoft-edge"></a>了解 Microsoft Edge 中的 ClickOnce 和 DirectInvoke 功能

ClickOnce DirectInvoke 是 IE 和 Microsoft Edge提供的功能，可支援使用檔案處理常式從網站下載檔案。 雖然其具有不同的用途，但兩個功能都允許網站指定將請求下載的檔案傳遞給使用者裝置上的檔案處理常式。 ClickOnce 請求由 Windows 中的原生檔案處理常式處理。 DirectInvoke 請求由裝載該檔案之網站所指定的已註冊檔案處理常式來處理。

如需這些方法的詳細資訊，請參閱下列文章：

- [ClickOnce](/visualstudio/deployment/clickonce-security-and-deployment?view=vs-2019)
- [DirectInvoke]( https://technet.microsoft.com/learning/jj215788(v=vs.94).aspx)

> [!NOTE]
> 目前，Chromium 不提供 ClickOnce 或 DirectInvoke 的原生支援。

## <a name="overview-prerequisites-and-process"></a>概觀：必要條件和程序

若要讓 ClickOnce 和 DirectInvoke 依照設計方式運作，並能成功請求檔案處理常式，檔案處理常式必須註冊到支援 ClickOnce 或 DirectInvoke 的作業系統。 此註冊通常在安裝原始作業系統或安裝的新程式請求使用 DirectInvoke 進行更新時發生。

當網站收到需要 ClickOnce 或 DirectInvoke 的下載請求時，將發生以下動作：

- 網站請求瀏覽器使用指定的檔案處理常式。
- 瀏覽器檢查作業系統登錄以查看檔案處理常式是否已為所請求的檔案類型進行註冊。
- 如果已註冊檔案處理常式，瀏覽器將呼叫檔案處理常式並將 URL 做為引數傳遞給檔案處理常式。
- 檔案處理常式會處理 URL 並下載檔案。

  > [!NOTE]
  > URL 用於判斷檔案的來源，以及存取檔案時使用的任何參數。  例如：端點、資訊清單或中繼資料。

## <a name="use-cases"></a>使用案例

以下使用案例具有代表性。

您可以使用 ClickOnce 在裝置上輕鬆部署和更新軟體，只需最少的使用者互動。 使用者可以透過按一下網頁中的連結來安裝和執行 Windows 應用程式。 如果設定正確，ClickOnce 應用程式可以安裝程式，無需使用者為安裝程式進行設定。 例如，檔案位置、要安裝的選項等。

DirectInvoke 使用案例取決於請求 DirectInvoke 之網站的用意。 例如，Microsoft Word 的協作檔案編輯功能。 DirectInvoke 允許您下載已變更的文件部分，而不是按一下連結並下載您正在與同事和合作處理文件的整個副本。 這個策略可減少傳輸的資料量，並減少開啟文件所需的時間。  

## <a name="current-support-for-clickonce-and-directinvoke-in-microsoft-edge"></a>Microsoft Edge 中對 ClickOnce 和 DirectInvoke 的目前支援

對 ClickOnce 和 DirectInvoke 的支援：

- ClickOnce 和 DirectInvoke 全面支援所有 Windows 使用者。

  > [!NOTE]
  > 想停用 ClickOnce 支援的使用者可以移至*edge://flags/#edge-click-once* 並從下拉式清單中選取 **[停用]**。 您必須**重新啟動**瀏覽器。

- ClickOnce 和 DirectInvoke 不支援 Windows 以外的任何平台。

## <a name="clickonce-and-directinvoke-file-handling-security"></a>ClickOnce 和 DirectInvoke 檔案處理安全性

ClickOnce 和 DirectInvoke 受到 Microsoft Defender SmartScreen 的 URL 信譽掃描服務的保護。

如果 Microsoft Defender SmartScreen URL 信譽服務將 ClickOnce 或 DirectInvoke 請求標幟為不安全，則啟用 ClickOnce 或 DirectInvoke 的使用者將看到兩個快顯視窗。

第一個快顯視窗詢問使用者是否要開啟該檔案。 無論檔案被標幟為安全還是不安全，都會顯示此快顯視窗。 使用者可以**將檔案報告為不安全**、**取消**請求或按一下**開啟**以繼續。

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-clickonce-modal-1.png)

如果使用者嘗試開啟檔案，並且檔案被標幟為不安全，則會顯示第二個快顯視窗。  此快顯視窗警告使用者該檔案被標幟為不安全，並詢問他們是否確定要下載檔案。

第二個快顯視窗僅在以下情況中顯示：

- 該檔案是 ClickOnce 或 DirectInvoke 檔案
- 已啟用 ClickOnce 或 DirectInvoke
- 檔案標幟為不安全

 ![提示以開啟不安全的檔案](./media/edge-learn-more-co-di/edge-clickonce-modal-2.png)

> [!NOTE]
> 如果停用 ClickOnce 或 DirectInvoke，則請求的檔案將被視為一般下載，如果標幟為不安全，則將標記為不安全。 這與處理其他不安全下載的情況一致。

## <a name="clickonce-and-directinvoke-policies"></a>ClickOnce 和 DirectInvoke 原則

有 2 個群組原則可用於為企業使用者啟用或停用 ClickOnce 和 DirectInvoke。 這兩個原則是 [ClickOnceEnabled](./microsoft-edge-policies.md#clickonceenabled) 和 [DirectInvokeEnabled](./microsoft-edge-policies.md#directinvokeenabled)。 這兩個策略在群組原則編輯器中分別標記為 [允許使用者使用 ClickOnce 通訊協定開啟檔案] 和 [允許使用者使用 DirectInvoke 通訊協定開啟檔案]。

## <a name="clickonce-and-directinvoke-behavior"></a>ClickOnce 和 DirectInvoke 行為

以下範例顯示啟用或停用 ClickOnce 和 DirectInvoke 時的檔案處理。

### <a name="clickonce-enabled"></a>ClickOnce 已啟用

1. 使用者開啟指向請求 ClickOnce 支援之頁面的連結，並在下一個螢幕擷取畫面中收到提示。

   ![提示以開啟不安全的檔案](./media/edge-learn-more-co-di/edge-clickonce-enabled-1.png)

2. 使用者按一下**開啟**後，ClickOnce 嘗試啟動應用程式。

   ![ClickOnce 嘗試啟動應用程式](./media/edge-learn-more-co-di/edge-clickonce-enabled-launch-app.png)

3. 使用者按一下**開啟**後，瀏覽器將顯示一個快顯視窗，詢問使用者是否確定要安裝該應用程式。

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-clickonce-enabled-2.png)

   > [!NOTE]
   > ClickOnce 檔案處理常式顯示的介面、訊息和選項，將因所存取檔案的類型和設定而異。

### <a name="clickonce-disabled"></a>ClickOnce 已停用

1. 當使用者開啟指向請求 ClickOnce 支援之頁面的連結時，會在下載匣中看到一則訊息，此訊息與下一個螢幕擷取畫面中的訊息類似。

   ![檔案下載提示](./media/edge-learn-more-co-di/edge-clickonce-disabled-1.png)

### <a name="directinvoke-enabled"></a>DirectInvoke 已啟用

1. 使用者開啟指向請求 DirectInvoke 支援之頁面的連結，並在下一個螢幕擷取畫面中收到提示。

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-directinvoke-open-link-1.png)

2. 當使用者按一下**開啟**時，將開啟請求的檔案處理常式。 在此範例中，Microsoft Word 用於開啟上一個螢幕擷取畫面中顯示的文件。

   > [!NOTE]
   > DirectInvoke 檔案處理常式顯示的介面、訊息和選項，將因所存取檔案的類型和設定而異。

### <a name="directinvoke-disabled"></a>DirectInvoke 已停用

1. 當使用者開啟指向請求 DirectInvoke 支援之頁面的連結時，DirectInvoke 的行為與停用 ClickOnce 時相同。 他們將在下載匣中看到一則訊息，此訊息與下一個螢幕擷取畫面中的訊息類似。

   ![提示以開啟檔案](./media/edge-learn-more-co-di/edge-directinvoke-open-link-2.png)

## <a name="see-also"></a>也請參閱

- [ClickOnce 安全性和部署](/visualstudio/deployment/clickonce-security-and-deployment)
- [Internet Explorer 中的 DirectInvoke](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/jj215788(v=vs.85))
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)