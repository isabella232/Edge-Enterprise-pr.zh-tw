---
title: IE 模式中可設定的網站和 Microsoft Edge
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: IE 模式中可設定的網站和 Microsoft Edge
ms.openlocfilehash: 0248ecd394acee5773751c0685969e3d40940431
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978919"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a>深入了解 IE 模式中可設定的網站

本文說明了在 Microsoft Edge 中使用 IE 模式時，企業模式網站清單的 [可設定網站] 功能。

## <a name="prerequisites"></a>必要條件

- Windows 更新

  - Windows 10 版本 1909、Windows Server 版本 1909– KB4550945  或更高版本
  - Windows 10 版本 1903、Windows Server 版本 1903– KB4550945  或更高版本
  - Windows 10 版本 1809、Windows Server 版本 1809 和 Windows Server 2019：KB4550969 或更新版本
  - Windows 10 版本 1803-KB4550944 或更新版本
  - Windows 10 版本1607、Windows Server 2016-KB4556826 或更新版本
  - Windows 10 初始版 (2015 年 7 月 - KB4550947 或更新版本)
  - Windows 8.1 – KB4556798 或更新版本

- Microsoft Edge 版本 83 或更新版本
- [IE 模式](./edge-ie-mode.md)使用企業模式網站清單設定

## <a name="overview"></a>概觀

在企業模式網站清單中設定 IE 模式的網站，適用于大部分舊版應用程式的環境。 但在某些情况下，如果不在 IE 模式中轉譯整個網域，那麼此方法不適合在 IE 模式中設定開啟網站子集。 例如，當您的環境同時包含在單個服務器上運行的新版和舊版應用程式時，且您希望能夠靈活地在 IE 模式下僅轉譯舊版應用程式，而在 Microsoft Edge 模式下轉譯其餘應用程式。

解決方法是使用企業模式網站清單的 [可設定網站] 功能。 啟用此功能後，Microsoft Edge 將會允許具有「可配置」標記的網站參與 IE 模式引擎判斷。

## <a name="how-configurable-sites-works"></a>[可設定網站] 的運作方式

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a>從 Microsoft Edge 引擎自動切換到 IE 模式引擎

若要使用 [可設定網站] 功能，將需要企業模式網站清單中的一或多個網站，以具有`<open-in>Configurable</open-in>`選項。

範例：

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

啟用 [可設定網站] 功能時，會發生下列行為：

1. 當對可設定的網站發出要求時，Microsoft Edge 會傳送 HTTP 要求標頭 “`X-InternetExplorerModeConfigurable: 1`”。
2. 可設定的網站可能會傳送具有 HTTP 回應標頭 “`X-InternetExplorerMode: 1`”的重新導向回應（例如 HTTP 302） ，以要求 Microsoft Edge 在 IE 模式載入網站。
3. 重新導向的目標（即位置**回應**標頭的值）也必須是**可設定**的或**中立**的網站，否則 IE 模式回應標頭將被忽略。 因此重新導向的目標通常與原始的 URL 相同。 但也不是必須如此。

   > [!NOTE]
   > 重新導向回應可根據 Microsoft Edge 重新導向的一般 HTTP 快取行為進行快取。

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a>從 IE 模式引擎切換回 Microsoft Edge 引擎

啟用 Microsoft Edge 中 [可設定網站] 會自動啟用 IE 模式索引標籤中的下列行為：

1. 當對可設定的網站發出要求時，IE 模式索引標籤會傳送 HTTP 要求標頭 “`X-InternetExplorerModeConfigurable: 1`”，與 Microsoft Edge 索引標籤相同。
2. 可設定的網站可能會傳送具有 HTTP 回應標頭 “`X-InternetExplorerMode: 0`”的重新導向回應（例如 HTTP 302） ，以要求導航切換回 Microsoft Edge 模式。
3. 重新導向的目標（即位置**回應**標頭的值）也必須是**可設定**的或**中立**的網站，否則 IE 模式回應標頭將被忽略。 因此重新導向的目標通常與原始的 URL 相同。 但也不是必須如此。

   > [!NOTE]
   > 重新導向回應可根據 Microsoft Edge 重新導向的一般 HTTP 快取行為進行快取。

> [!TIP]
> 兩個瀏覽器引擎都將傳送相同的「`X-InternetExplorerModeConfigurable: 1`」要求標頭到可設定的網站。 您應該使用 [使用者-代理] 要求標頭來區分來自 Microsoft Edge 模式與 IE 模式的要求，以避免當網站已載入到正確的引擎中時進行重新導向。

## <a name="see-also"></a>請參閱

- [關於 IE 模式](./edge-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)