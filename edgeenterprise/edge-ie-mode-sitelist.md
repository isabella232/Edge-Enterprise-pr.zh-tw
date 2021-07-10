---
title: 企業網站設定策略
ms.author: shisub
author: shisub
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 為 Internet Explorer 模式設定企業模式網站清單的逐步指南。
ms.openlocfilehash: 72de393a5da0b4b0e2950951ae527f6ef870e110
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641809"
---
# <a name="enterprise-site-configuration-strategy"></a>企業網站設定策略

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文將說明企業模式網站清單的變更，以支援 Microsoft Edge 版本 77 及更新版本的 Internet Explorer 模式。

如需有關企業模式網站清單 XML 檔案結構描述的詳細資訊，請參閱[企業模式結構描述 v.2 指引](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a>設定策略

下列步驟是 IE 模式網站設定策略的一部分：
1. 準備您的網站清單
2. 設定中性網站
3. (選擇性) 必要時使用 Cookie 共用

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a>準備您的網站清單

如果您已經有適用於 IE11 或舊版 Microsoft Edge 的企業模式網站清單，您可以重複使用該清單來設定 IE 模式。

不過，如果您沒有網站清單，您可以使用[企業網站探索工具](/deployedge/edge-ie-mode-site-discovery)來填入網站清單。

## <a name="configure-neutral-sites"></a>設定中性網站

為了讓 IE 模式正常運作，驗證/單一登入 (SSO) 伺服器必須明確設定為中立網站。 否則，IE 模式頁面會嘗試重新導向至 Microsoft Edge，而驗證將會失敗。

中性網站會使用瀏覽啟動的瀏覽器 - Microsoft Edge 或 IE 模式。 設定中性網站可確保使用這些驗證伺服器的所有應用程式 (新式與舊版) 會繼續運作。

您可以將 Enterprise Mode Site List Manager 工具中的 [開啟於]** 下拉式功能表設定為 [無]，或直接更新網站清單 XML，藉此來設定中性網站：

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

若要識別驗證伺服器，請使用 IE11 開發人員工具檢查來自應用程式的網路流量。 如果您需要更多時間來識別您的驗證伺服器，您可以設定原則，將所有頁面內導覽保持在 IE 模式，讓您的使用者可不間斷地繼續其工作流程。 若要將 IE 模式的使用在不必要時最小化，請在識別和新增驗證伺服器至網站清單後停用此設定。 如需詳細資訊，請參閱[在 IE 模式中保持頁面內導覽](/deployedge/edge-learnmore-inpage-nav)。

>[!NOTE]
   >IE 模式整合不支援企業模式結構描述 v.1。 如果目前使用結構描述 v.1 搭配 Internet Explorer 11，則必須升級到結構描述 v.2。 如需詳細資訊，請參閱[企業模式結構描述 v.2 指引](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。

## <a name="optional-use-cookie-sharing-if-necessary"></a>(選擇性) 必要時使用 Cookie 共用

根據預設，Microsoft Edge 和 Internet Explorer 處理程序不會共用工作階段 Cookie，在某些情況下，使用 IE 模式時，這種缺少共用的情況可能不太方便。 例如，當使用者之前習慣在 IE 模式中重新驗證時，或登出 Microsoft Edge 工作階段卻不會針對重要交易登出 Internet Explorer 模式工作階段時。 在這些情況下，您可以設定 SSO 所設定的特定 Cookie，以從 Microsoft Edge 傳送至 Internet Explorer，如此一來，由於無需重新驗證，驗證體驗就會更順暢。 若需詳細資訊，請參閱[從 Microsoft Edge 共用 Cookie 到 Internet Explorer](/deployedge/edge-ie-mode-add-guidance-cookieshare)。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](./edge-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
