---
title: 停用 Internet Explorer 11
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何在 Microsoft Edge 中停用 Internet Explorer 11 和使用 Internet Explorer 模式。
ms.openlocfilehash: a0486c2965b1868db67b6de1423f279905074410
ms.sourcegitcommit: f34ff11499a2b96941e704103bdd959d19e3d7e7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400603"
---
# <a name="disable-internet-explorer-11"></a>停用 Internet Explorer 11

本文說明如何在您的環境中停用 Internet Explorer 11 做為獨立瀏覽器。

## <a name="prerequisites"></a>必要條件

需要下列 Windows 更新和 Microsoft Edge 軟體：

- Windows 更新

  - Windows 10 版本 2004、Windows Server 版本 2004、Windows 10、版本 20H2：[KB4598291](https://support.microsoft.com/topic/february-2-2021-kb4598291-os-builds-19041-789-and-19042-789-preview-6a766199-a4f1-616e-1f5c-58bdc3ca5e3b) 或更新版本
  - Windows 10 版本 1909、Windows Server 版本 1909：[KB4598298](https://support.microsoft.com/topic/january-21-2021-kb4598298-os-build-18363-1350-preview-02dfd9ba-91a2-1b82-dede-42f288c02511) 或更新版本
  - Windows 10 版本 1809、Windows Server 版本 1809 和 Windows Server 2019：[KB4598296](https://support.microsoft.com/topic/january-21-2021-kb4598296-os-build-17763-1728-preview-4c0931ff-45b7-ff59-5e00-c03b5afb363d) 或更新版本
  - Windows 10 版本 1607、Windows Server 2016：[KB4601318](https://support.microsoft.com/topic/february-9-2021-kb4601318-os-build-14393-4225-c5e3de6c-e3e6-ffb5-6197-48b9ce16446e) 或更新版本
   - Windows 10 初始版本 (2015 年 7 月)：[KB4601331](https://support.microsoft.com/office/february-9-2021%e2%80%94kb4601331-os-build-10240-18842-6227d078-fef3-8d67-27e0-1882e6cb79ff?ui=en-US&rs=en-US&ad=US) 或更新版本
  - Windows 8.1：[KB4601384](https://support.microsoft.com/topic/february-9-2021-kb4601384-monthly-rollup-16bdbb75-dd4b-2910-abc5-7891c9756b96) 或更新版本
  - Windows Server 2012：[KB4601348](https://support.microsoft.com/topic/february-9-2021-kb4601348-monthly-rollup-2c338c0c-73d6-fb80-cc91-f1a86e80db0c) 或更新版本
  
- Microsoft Edge 穩定通道


## <a name="overview"></a>概觀

針對需要 Internet Explorer 11 (IE11) 之舊版相容性的組織，Microsoft Edge 上的 Internet Explorer 模式 (IE 模式) 提供流暢的單一瀏覽器體驗。 使用者可以從 Microsoft Edge 存取舊版應用程式，而不需要切換回 IE11。

設定 IE 模式之後，您可以使用群組原則來停用 IE11 作為獨立瀏覽器，**而不會影響整個組織的 IE 模式功能**。

> [!NOTE]
> 如果您需要適用於特定網站的獨立 IE11 應用程式，並想要將所有其他瀏覽器流量重新導向至 Microsoft Edge，您可以設定[將網站清單中未包含的所有網站傳送至 Microsoft Edge](https://docs.microsoft.com/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) 原則，將網站從 IE 重新導向至 Microsoft Edge。

## <a name="user-experience-after-redirecting-traffic-to-microsoft-edge"></a>將流量重新導向至 Microsoft Edge 後的使用者體驗

當您啟用 [停用 Internet Explorer 11 做為獨立瀏覽器]**** 原則後，所有 IE11 活動會重新導向至 Microsoft Edge，且使用者會擁有下列體驗：

- 系統將會移除 [開始] 功能表上的 IE11 圖示，但工作列上的圖示會保留。
- 當使用者嘗試啟動使用 IE11 的捷徑或檔案關聯時，系統將會重新導向使用者以在 Microsoft Edge 中開啟相同的檔案/URL。
- 當使用者嘗試直接以 iexplore.exe 二進位檔啟動 IE11 時，會改為啟動 Microsoft Edge。

在設定此體驗的原則時，您可以選擇為嘗試啟動 IE11 的每位使用者顯示重新導向訊息。 可將此訊息設定為 [永遠顯示] 或 [每位使用者顯示一次]。 根據預設，永遠不會顯示下一個螢幕擷取畫面中顯示的重新導向訊息。

:::image type="content" source="media/edge-ie-disable-ie11/disable-ie-redirect-msg.png" alt-text="在 Microsoft Edge 重新導向作用中時，當您嘗試開啟 IE 時，系統會提醒您。":::

如果您的 [企業模式網站清單] 包含設定為在IE11 應用程式中開啟的應用程式，並且您使用此原則停用了 IE11，則它們將在 Microsoft Edge 上以 IE 模式開啟。
> [!NOTE]
> 當網站設定為在 IE11 中開啟，且已設定停用 IE11 原則時，使用者流程會發生已知問題。 我們正在積極調查此問題。

## <a name="disable-internet-explorer-11-as-a-standalone-browser"></a>停用 Internet Explorer 11 作為獨立瀏覽器

若要使用群組原則停用 Internet Explorer 11，請遵循下列步驟：

1. 請確保您擁有必要的作業系統更新。 此步驟會直接更新您電腦上的 ADMX 檔案 (具體為 inetres.adml 和 inetres.admx)。 請注意，如果您想要更新 Central Store，您必須從具備必要更新之電腦複製 .adml 和 .admx 檔案。 如需詳細資訊，請參閱 [建立及管理 Central Store](https://docs.microsoft.com/troubleshoot/windows-client/group-policy/create-and-manage-central-store)
2. 開啟 [群組原則編輯器]。
3. 移至***電腦設定/系統管理範本/Windows 元件/Internet Explorer***。 
4. 按兩下 [停用 Internet Explorer 11 作為獨立瀏覽器] ****。
5. 選取 [啟用] ****。
6. 在 [選項] **** 下，挑選下列其中一個值：

   - **永不** 如果您不想通知使用者 IE11 已停用。
   - **永遠** 如果您想要每次從 IE11 重新導向使用者時通知使用者。
   - **每位使用者一次** 如果您只想在使用者第一次重新導向時通知使用者。

7. 按一下 [確定]  ****  或 [套用] ****  以儲存此原則設定。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [其他企業模式資訊](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
