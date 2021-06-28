---
title: 從 Microsoft Edge 到 Internet Explorer 共用 Cookie
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '如何從 Microsoft Edge 到 Internet Explorer 共用 Cookie '
ms.openlocfilehash: 563179852ff23142b540345222ba7e943547535d
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617463"
---
# <a name="cookie-sharing-from-microsoft-edge-to-internet-explorer"></a>從 Microsoft Edge 到 Internet Explorer 共用 Cookie

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文說明如何在使用 Internet Explorer 模式的同時，將工作階段 Cookie 設置為從 Microsoft Edge 程式共用到 Internet Explorer 程式。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

## <a name="prerequisites"></a>必要條件

- Windows 更新

  - Windows 10 版本 2004、Windows Server 版本 2004－KB4571744 或更新版本
  - Windows 10 版本 1909、Windows Server 版本 1909－KB4566116 或更新版本
  - Windows 10 版本 1903、Windows Server 版本 1903－KB4566116 或更新版本
  - Windows 10 版本 1809、Windows Server 版本 1809 和 Windows Server 2019－KB4571748 或更新版本
  - Windows 10 版本 1803－KB4577032 或更新版本

- Microsoft Edge 版本 87 或更新版本
- 使用企業模式網站清單設定 [IE 模式](./edge-ie-mode.md) 

## <a name="overview"></a>概觀

大型組織中的一般設定，是讓應用程式能夠在新式瀏覽器上使用，以連結到另一個應用程式，而這個應用程式可能設定為在工作流程中啟用單一登入（SSO）的 Internet Explorer 模式中開啟。

根據預設，Microsoft Edge 和 Internet Explorer 程式無法共用工作階段 cookie，在某些情況下可能會帶來不便。 例如，當使用者必須在 Internet Explorer 模式中重新驗證，或登出 Microsoft Edge 工作階段時，使用者並不會登出 Internet Explorer 模式工作階段。 在這些情況下，您可以將由 SSO 設置的特定 cookie 設置為從 Microsoft Edge 傳送到 Internet Explorer，驗證操作程序就會因消除了重新驗證的需要而變得更加流暢。

> [!NOTE]
> 工作階段 cookie 只能從 Microsoft Edge 共用到 Internet Explorer。 反向式共用工作階段 cookie 是不可行的（從 Internet Explorer 到 Microsoft Edge）。

## <a name="how-cookie-sharing-works"></a>Cookies 共用的運作方式

已將企業模式網站清單 XML 延展，以允許其他元素指定需要從 Microsoft Edge 工作模式與 Internet Explorer 共用的 cookie。  

在 Microsoft Edge 工作模式中，第一次建立 Internet Explorer 模式索引標籤時，所有相符的 cookie 都會共用至 Internet Explorer 工作模式。 之後，只要新增、刪除或修改符合規則的 cookie，系統就會將其新增為 Internet Explorer 工作模式的更新。 當網站清單更新時，也會重新評估該共用 cookie 集合。

### <a name="updated-schema-elements"></a>更新的結構描述元素

下表說明為了支援 cookie 共用功能而新增的 \<shared-cookie\> 元素。

| 元素| 描述 |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br>或<br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |**（必要）** 一個 \<shared-cookie\>元素至少需要一個 *網域*（適用於網域 cookie）或一個*主機*（主機專用 cookie）屬性和一個 *名稱* 屬性。<br>這些必須與 cookie 的網域和名稱完全相符。 **注意**：子域不相符。<br><br>*網域* 屬性用於網域 cookie （但允許使用前導點，但可選用）。<br>*host* 屬性適用於主機專用的 cookie（而前導點則是錯誤）。 若將這兩個都不指定或都指定將會導致錯誤。<br>* 若在 cookie 字串中指定網域，則 cookie 即為網域 cookie（透過 HTTP Set-Cookie 回應標頭或document.cookie JS AP）。 網域 cookie 適用於指定的網域和所有子網域。 * 若未在 cookie 字串中指定網域，則 cookie 即為主機專用 cookie，且只適用於其所設定的特定主機。 需要注意的是，有些類別的 URLs 像是單一文字的主機名稱（例如 http://intranetsite) 和 IP 位址（例如 http://10.0.0.1) 只可以設定主機專用的 cookie。    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | **（選用）** 可以指定 *路徑* 屬性。 如果未指定路徑屬性（或路徑屬性為空白），無論路徑為何（萬用字元規則），任何比對的網域/主機和名稱都符合該原則。<br><br>如果已指定路徑，它必須是完全相符的路徑。<br>如果 cookie 符合的規則是具有路徑，則此規則的優先順序高於不具路徑的規則。 |

#### <a name="sharing-example"></a>共用範例

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <a name="see-also"></a>請參閱

- [關於 IE 模式](./edge-ie-mode.md)
- [可設定的網站資訊](./edge-learnmore-configurable-sites-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)