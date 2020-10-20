---
title: 針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge
ms.author: laannade
author: dan-wesley
manager: ratetali
ms.date: 10/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge
ms.openlocfilehash: ce9e8dabdff25cc3ba375746ec82ddd78b6d7694
ms.sourcegitcommit: cf991cc4bd2e70169902cbda9ddc870d70e31ca2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120518"
---
# 針對與新式網站的相容性，從 Internet Explorer 重新導向至 Microsoft Edge

> [!NOTE]
> 本文適用於 Microsoft Edge Stable 版本 87 或更新版本。

## 概觀

許多新式網站的設計與 Internet Explorer 不相容。 每當 Internet Explorer 使用者造訪不相容的公用網站時，系統會顯示訊息，告訴他們該網站與其瀏覽器不相容，他們需要手動切換到不同的瀏覽器。

需要手動切換到不同的瀏覽器變更是從 Microsoft Edge Stable 版本 87 開始。

當使用者前往與 Internet Explorer 不相容的網站時，系統會自動將使用者重新導向至 Microsoft Edge。 本文說明重新導向的使用者體驗，以及用來設定或停用自動重新導向的群組原則。

> [!NOTE]
> Microsoft 會維護已知與 Internet Explorer 不相容的所有網站清單。

## 重新導向體驗

一旦重新導向至 Microsoft Edge，即會在下一個螢幕擷取畫面中向使用者顯示一次性對話方塊。 此對話方塊會說明什麼將使用者重新導向，並提示使用者同意將瀏覽資料和喜好設定從 Internet Explorer 複製到 Microsoft Edge。 將會匯入以下瀏覽資料：我的最愛、密碼、搜尋引擎、開啟的索引標籤、設定、Cookie 和首頁。

![瀏覽通知和提示以匯入資料和喜好設定。](media/edge-learnmore-neededge/neededge-dialog1.png)

即使他們未透過勾選 [永遠從 Internet Explorer 取得我的瀏覽資料和喜好設定] 來表示同意，他們也可以按一下 [繼續瀏覽] **** 以繼續進行其工作階段。

最後，在下一個螢幕擷取畫面中顯示的網站不相容橫幅，會在每次重新導向時顯示在網址列下方。

![有關新式網站的通知，並提示您將 Microsoft Edge 設定為預設瀏覽器或探索 Microsoft Edge。](media/edge-learnmore-neededge/neededge-banner.png)

網站不相容橫幅：

- 鼓勵使用者切換到 Microsoft Edge
- 將 Microsoft Edge 設定為預設瀏覽器的選項
- 讓使用者選擇探索 Microsoft Edge 的選項

將網站從 Internet Explorer 重新導向至 Microsoft Edge 時，開始載入網站的 Internet Explorer 索引標籤如果沒有之前的內容，就會關閉。 否則，使用中的索引標籤檢視會移至 Microsoft  [支援](https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554?ui=en-US&rs=en-US&ad=US) 頁面，在其中會說明為什麼將網站重新導向至 Microsoft Edge。

> [!NOTE]
> 在重新導向之後，使用者可以返回，對不在 Internet Explorer 不相容性清單中的網站使用 Internet Explorer。  

## 設定重新導向至 Microsoft Edge 的原則

> [!NOTE]
> 這些原則於 2020 年 10 月 26 日之前，以 ADMX 檔案更新的形式提供，並將於 2020 年 11 月 9 日在 Intune 中提供。

必須設定三個群群組原則，才能啟用對 Microsoft Edge 的自動重新導向。 這些原則如下：

- RedirectSitesFromInternetExplorerPreventBHOInstall
- RedirectSitesFromInternetExplorerRedirectMode
- HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

### 原則：RedirectSitesFromInternetExplorerPreventBHOInstall

從 Internet Explorer 重新導向至 Microsoft Edge 需要一個名為 "IEtoEdge BHO" 的 Internet Explorer 瀏覽器協助程式物件 (BHO)。 **RedirectSitesFromInternetExplorerPreventBHOInstall** 原則會控制是否安裝此 BHO。  

- 如果您啟用此原則，將不會安裝重新導向所需的 BHO，且您的使用者將繼續在 Internet Explorer 上看到特定網站的不相容訊息。 如果已安裝 BHO，則會在下一次更新 Microsoft Edge Stable 通道時將它解除安裝。
- 如果您停用或未設定此原則，則會安裝 BHO。 這是預設行為。

除了需要 BHO 之外，還有對 **RedirectSitesFromInternetExplorerRedirectMode** 的相依性，必須將其設定為 "Sitelist" 或「未設定」。

### 原則：RedirectSitesFromInternetExplorerRedirectMode

 此原則對應於 Microsoft Edge 中的 [預設瀏覽器]**** 設定：[在 Microsoft Edge 中以 Internet Explorer 開啟網站]。 您可以移至 *edge://settings/defaultbrowser* URL 來存取此設定。  

- 如果您未設定此原則或將它設定為 "Sitelist"，Internet Explorer 會將不相容的網站重新導向至 Microsoft Edge。 這是預設行為。
- 如果您停用此原則，則不會將不相容的網站重新導向至 Microsoft Edge。

> [!NOTE]
> 如果您所使用的個人裝置不是由組織管理，則會在 [Internet Explorer 相容性]**** 下看到另一個名為 [允許在 Internet Explorer 模式中載入網站] 的設定。
>
>如果您所使用的是加入網域或註冊行動裝置管理 (MDM) 的裝置，就不會看到此選項。
>
> 相反地，如果您想要讓使用者在 Internet Explorer 模式中載入網站，您可以透過設定原則 [允許在 Internet Explorer 模式中重新載入網站][](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allow-internet-explorer-mode-testing) 來完成。

### 原則：HideInternetExplorerRedirectUXForIncompatibleSitesEnabled

此原則會設定將不相容網站重新導向至 Microsoft Edge 的使用者體驗。  

- 如果您啟用此原則，使用者就不會看到一次性的重新導向對話方塊和重新導向橫幅。 不會匯入任何瀏覽器資料或使用者喜好設定。
- 如果您停用或不設定此原則，重新導向對話方塊會在第一次重新導向時顯示，並會針對從重新導向開始的工作階段顯示持續性重新導向橫幅。

  > [!NOTE]
  > 使用者每次發生新的重新導向時，都會匯入使用者瀏覽資料。 不過，此動作只會在使用者於一次性重新導向對話方塊中同意匯入時才會發生。

## 停用重新導向至 Microsoft Edge

如果您想要在更新至 Microsoft Edge Stable 版本 87「之前」停用重新導向，請使用下列步驟：

1. 將 **RedirectSitesFromInternetExplorerRedirectMode** 原則設定為 [已啟用]****。 原則生效後，此設定就會停止重新導向。

如果您想要在更新至 Microsoft Edge Stable 版本 87「之後」停用重新導向，請使用下列步驟：

1. 將 **RedirectSitesFromInternetExplorerRedirectMode** 原則設定為 [已停用]****。 原則生效後，此設定就會停止重新導向。
2. 將 **RedirectSitesFromInternetExplorerPreventBHOInstall** 原則設定為 [已啟用]****。 這會在下一次 Microsoft Edge 更新之後解除安裝 BHO。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 原則](https://docs.microsoft.com/deployedge/microsoft-edge-policies)