---
title: IE 模式的當地網站清單
ms.author: shisub
author: AndreaLBarr
manager: srugh
ms.date: 09/13/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 瞭解如何啟用本地網站清單及輕鬆存取 IE 模式
ms.openlocfilehash: 8130a835cd803f5cdeb50f825ccee895f35f62e3
ms.sourcegitcommit: c3d63d913eb15e7dbeb9f45b5f28fc841b46bce1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/15/2021
ms.locfileid: "12016562"
---
## <a name="local-site-list-for-ie-mode"></a>IE 模式的當地網站清單

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文說明如何在 IE 模式中設定輕鬆存取 Internet Explorer 模式 (IE) ，以及允許使用貴組織的本地網站清單。

> [!NOTE]
> 本文適用于Microsoft Edge版本 92 或更新版本。

### <a name="prerequisites"></a>必要條件

1. Windows 更新

- Windows 10版本 1909 - [KB5003698](https://support.microsoft.com/topic/june-15-2021-kb5003698-os-build-18363-1645-preview-1ecf117e-1f89-40f9-a0a5-ed5766737620)或更新版本  

- Windows 10版本 2004;Windows 10版本 20H2 Windows 10版本 21H1 – [KB5003690](https://support.microsoft.com/topic/june-21-2021-kb5003690-os-builds-19041-1081-19042-1081-and-19043-1081-preview-11a7581f-2a01-47d5-ba12-431709ee2248)或更新版本

2. Microsoft Edge版本 92 (92.0.925.0 或更新版本) 

## <a name="overview"></a>概觀

IE 模式是由模式網站清單的Enterprise提供。 當您在網站清單上識別及將網站配置為使用 IE 模式時，您的使用者不再需要等待或回到獨立 IE11 應用程式。

從版本 92 Microsoft Edge開始，重複存取未配置的*IE*模式網站會更容易。 使用者可以在 IE 模式中重載網站。 他們可以新增這些網站至其本地網站清單，以在 IE 模式中自動呈現 30 天，同時更新組織的網站清單。 當您 [的環境中停用 IE11](/deployedge/edge-ie-disable-ie11) 時，您的使用者就不再只取決於組織的網站清單。

您可以透過貴組織的群群組原則來設定此體驗。

注意：未*配置的*網站是一個需要 IE 模式，但未在 IE 模式中開啟的網站，Enterprise模式網站清單。

## <a name="local-site-list-experience"></a>本地網站清單體驗

若要啟用本地網站清單體驗，使用者可以前往 *URL* edge://settings/defaultBrowser，將允許網站在 **Internet Explorer** 模式中重載為 **Allow**。

:::image type="content" source="media/Edge-hybrid-IE-mode/internet-explorer-compatibilitiy.png" alt-text="Internet Explorer 相容性":::

>[!Note]  
>
>1. 如果您透過 *InternetExplorerIntegrationTestingAllowed policy* 啟用 IE 模式測試，會看到此設定，但除非您明確啟用 *InternetExplorerIntegrationReloadInIEModeAllowed* 政策，否則此設定會呈灰色。
>
>2. 如果 **允許在 Internet Explorer** 模式中重載網站設定為 **預設值**，如果使用者有現有的 Internet Explorer 11 使用方式，他們或許可以在 IE 模式中重載網站。  

啟用這項設定後，使用者可以選取 設定 及更多 (省略號圖示 ...) >在 Internet Explorer 模式中重載，以**IE 模式重載網站**。 當使用者以滑鼠右鍵按一下某個連結時，也可以選取 **Internet Explorer** 模式的 [重載> 定位停駐點，或在以滑鼠右鍵按一下連結時，選擇 [在新的 **Internet Explorer** 模式中開啟連結>

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-screenshot.png" alt-text="在 Internet Explorer 模式中重載":::

Internet **Explorer 模式中的重載圖示** 可以釘到工具列。 工具列按鈕可讓使用者輕鬆進入和離開 IE 模式，並透過 edge://settings/appearance URL *進行管理* 。

:::image type="content" source="media/Edge-hybrid-IE-mode/reload-in-internet-exploror-mode-icon-screenshot.png" alt-text="在 Internet Explorer 模式中重載圖示":::

>[!Note]
>如果使用者位於組織 Enterprise 模式網站清單的網站上，則顯示以 (重載或退出) Internet Explorer 模式的選項，但會以灰色顯示。

選取此選項時，網站會以 IE 模式重載。 網址欄左側會顯示 IE 模式指示器圖示，而飛出會顯示一個選項，讓使用者下次可以切換至在 Internet Explorer 模式中開啟頁面。 這會將使用者位於當地網站清單中的特定頁面新增到本地網站清單，並會在接下來 30 天內以 IE 模式自動開啟。

:::image type="content" source="media/Edge-hybrid-IE-mode/site-has-been-reloaded-in-ie-mode-screenshot.png" alt-text="此頁面以 Internet Explorer 模式開啟":::

在 IE 模式中重載網站後，「頁面內」流覽會維持在 IE 模式 (例如頁面上的連結、腳本或表單，或另一個「頁面內」流覽) 的伺服器端重新導向。  

在 IE 模式中，使用者會看到橫幅，指出他們目前位於 IE 模式、離開 IE 模式的選項，以及將 IE 模式圖示釘選到工具列 (如果尚未釘選) 。

:::image type="content" source="media/Edge-hybrid-IE-mode/ie-mode-banner-screenshot.png" alt-text="IE 模式橫幅":::

使用者可以退出宣告 IE 模式，使用橫幅上的離開按鈕、已釘選的 IE 模式圖示或 設定 等 (省略號圖示 **...) > 離開 Internet Explorer**模式，否則 Microsoft Edge 會在流覽不是「頁面內」時自動離開 IE 模式 (例如使用網址欄、返回按鈕或最愛的連結) 。

專案會保留在本地網站清單中，預設為 30 天。 我們建議您在模式網站清單中為貴組織Enterprise舊版網站。 本地網站清單可確保使用者在組織的網站清單更新時，能夠繼續其工作流程，而不會遭到干擾。 第 31 天，當使用者流覽至網站時，他們會看到橫幅，說明網站將不再在 IE 模式中載入。 使用者可以將其新增回本地網站清單 ，如果他們選擇的話。

:::image type="content" source="media/Edge-hybrid-IE-mode/page-will-no-longer-load-in-ie-mode-screenshot.png" alt-text="在 IE 模式中不會再載入頁面":::

## <a name="policies-to-configure-the-use-of-local-site-lists-for-ie-mode"></a>設定 IE 模式本地網站清單使用方式的策略

有兩個群組原則可用於在 Microsoft Edge 中設定本地網站Microsoft Edge。 這些原則如下：

### *<a name="policy-internetexplorerintegrationreloadiniemodeallowed"></a>政策：InternetExplorerIntegrationReloadInIEModeAllowed*

此政策對應至Microsoft Edge Internet Explorer 模式中允許重載網站」的設定。 您可以移至 *edge://settings/defaultbrowser* URL 來存取此設定。

- 如果您啟用此策略，使用者可以在 IE 模式中重載網站，只要選取 設定 及更多 (省略號**圖示 ... > Internet Explorer**模式重載即可。 當使用者以滑鼠右鍵按一下某個連結時，也可以選取 **Internet Explorer** 模式的 [重載> Tab，或在以滑鼠右鍵按一下連結時，選擇 [在新的 **Internet Explorer** 模式中開啟連結> 選項卡。
使用者可以選擇性地Microsoft Edge網站使用 IE 模式。 這個選項會預設為 30 天，而且可以使用 *原則 InternetExplorerIntegrationLocalSiteListExpirationDays*進行管理。

- 如果您停用此策略，則不允許使用者在 IE 模式中重載未配置的網站。

- 如果您沒有設定此政策，我們會根據最近的 Internet Explorer 11 使用方式，向使用者顯示在 IE 模式中重載未設定網站的選項。

請注意，此策略優先于您如何配置 [InternetExplorerIntegrationTestingAllowed policy，](/deployedge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) 且該策略將會停用。

### *<a name="policy-internetexplorerintegrationlocalsitelistexpirationdays"></a>原則：InternetExplorerIntegrationLocalSiteListExpirationDays*

此政策可用來調整網站在使用者的本地網站清單中保留的天數。  

- 如果您停用或不設定此策略，會使用預設值 30 天。

- 如果您啟用該政策，您必須在 0-90 天內輸入值，才能將網站保留于使用者的當地網站清單中。

如果您停用 *InternetExplorerIntegrationReloadInIEModeAllowed 政策* ，此策略將無效。

**附註：**

目前，本地網站清單不會跨裝置同步。 這項改進目前正在處理我們的待處理專案上，我們會在可用時更新。

## <a name="see-also"></a>另請參閱

停用 Internet Explorer 11 - [停用 Internet Explorer 11 |Microsoft Docs](/deployedge/edge-ie-disable-ie11)

設定 IE 模式策略 - [設定 IE 模式|Microsoft Docs](/deployedge/edge-ie-mode-policies)

