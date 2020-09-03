---
title: 在企業模式網站清單中設定網站
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定企業網站清單
ms.openlocfilehash: 969a4f6001dbe08a51c26ecf35812b101d315a59
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979579"
---
# 在企業模式網站清單中設定網站

本文說明對企業模式網站清單所做的變更，支援為 Microsoft Edge 版本 77 及更新版本設定 IE 模式。

如需有關企業模式網站清單 XML 檔案結構描述的詳細資訊，請參閱[企業模式結構描述第 2 版指導方針](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。

> [!NOTE]
> 本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。

## 更新的結構描述元素

下表描述新增到企業模式結構描述 v.2 中的 \<open-in app\> 元素：

| **元素** | **說明** |
| --- | --- |
| \<open-in app="**true**"\> | 可控制針對網站使用何種瀏覽器的子元素。 對於需要在 **IE11 中開啟**的網站，需要此元素。|

**範例：**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

下表顯示 \<open-in\> 元素的可能值：

| **值** | **說明** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | 在 IE 模式或完整 IE11 視窗中開啟網站。 若要啟用 IE 模式，請參閱[設定 IE 模式原則](https://docs.microsoft.com/deployedge/edge-ie-mode-policies)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | 在完整 IE11 視窗中開啟網站 |
| **\<open-in\>MSEdge\</open-in\>** | 在 Microsoft Edge 中開啟網站 |
| **\<open-in\>無或不指定\</open-in\>** | 在預設瀏覽器或使用者瀏覽至網站的瀏覽器中開啟網站。 |
|**\<open-in\>可設定\</open-in\>** | 允許網站參與 IE 模式引擎判斷。 若要深入了解，請參閱[了解 IE 模式中可設定的網站](edge-learnmore-configurable-sites-ie-mode.md)。  |

>[!NOTE]
> 僅當與 _'open-in' IE11_ 關聯時，才會識別屬性 app=**"true"**。 將其新增到其他 'open-in' 元素，不會變更瀏覽器行為。   

## 設定中性網站

為了讓 IE 模式正常運作，必須將驗證/單一登入伺服器明確設定為中性網站。 否則，IE 模式頁面會嘗試重新導向至 Microsoft Edge，而驗證將會失敗。

中性網站會使用瀏覽啟動的瀏覽器 - Microsoft Edge 或 IE 模式。 設定中性網站可確保使用這些驗證伺服器的所有應用程式 (新式與舊版) 會繼續運作。

您可以將 Enterprise Mode Site List Manager 工具中的 [開啟於]** 下拉式功能表設定為 [無]，或直接更新網站清單 XML，藉此來設定中性網站：

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

若要識別驗證伺服器，請使用 IE11 開發人員工具檢查來自應用程式的網路流量。 如果您需要更多時間來識別驗證伺服器，您可以設定原則，以在 IE 模式中保留所有頁面內導覽。 若要將 IE 模式的使用降至最低，請在識別並將驗證伺服器新增至網站清單之後，停用此設定。 如需詳細資訊，請參閱[設定頁面內導覽維持在 IE 模式](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)。

>[!NOTE]
   >IE 模式整合不支援企業模式結構描述 v.1。 如果目前使用結構描述 v.1 搭配 Internet Explorer 11，則必須升級到結構描述 v.2。 如需詳細資訊，請參閱[企業模式結構描述 v.2 指導方針](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [其他企業模式資訊](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)