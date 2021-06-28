---
title: 什麼是 Internet Explorer 模式？
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 瞭解 Microsoft Edge 中的 Internet Explorer 模式如何提供需要 Internet Explorer 11 的網站存取權，以及存取新式網站的方式。
ms.openlocfilehash: 39f8797049ac1051d49c63c880b8436dd611d9c2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617413"
---
# <a name="what-is-internet-explorer-ie-mode"></a>什麼是 Internet Explorer (IE) 模式？

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

我們在 Microsoft Edge 中建立 Internet Explorer (IE) 模式，適用於仍然需要 Internet Explorer 11 與現有網站的回溯相容性但也需要新式瀏覽器的組織。 此功能讓組織更容易使用單一瀏覽器、舊版網頁/應用程式或新式網頁/應用程式。 本文提供在 IE 模式中使用 Microsoft Edge 的簡介。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="what-is-ie-mode"></a>什麼是 IE 模式？

Microsoft Edge 的 IE 模式可讓您輕鬆地在單一瀏覽器中使用貴組織所需的所有網站。 它針對新式網站使用整合式 Chromium 引擎，針對舊版網站使用來自 Internet Explorer 11 (IE11) 的 Trident MSHTML 引擎。

當網站在 IE 模式下載入時，IE 標誌指示器會顯示在瀏覽器列的左側。 您可按一下 IE 標誌指示器以顯示其他資訊，如下所示：

  ![IE 標誌指示器](./media/ie-mode/ie-logo-indicator1.png)

只有您專門設定 (透過原則) 的那些網站會使用 IE 模式，其他所有網站都會轉譯為新式網站。 若要讓網站使用 IE 模式，您必須：

- 使用下列其中一個原則定義的企業模式網站清單 XML，列出網站：
  - Microsoft Edge 78 或更新版本，「設定企業模式網站清單」
  - Internet Explorer，「使用企業模式 IE 網站清單」
  > [!NOTE]
  > 我們只會處理一個企業模式網站清單。 Microsoft Edge 網站清單原則優先於 Internet Explorer 網站清單原則。
- 啟用**將所有內部網路網站傳送到 Internet Explorer** 群組原則的所有內部網路網站 (Microsoft Edge 77 或更新版本)。

### <a name="ie-mode-supports-the-following-internet-explorer-functionality"></a>IE 模式支援以下 Internet Explorer 功能

- 所有文件模式和企業模式
- ActiveX 控制項 (例如 Java 或 Silverlight)
- 瀏覽器協助程式物件 
- 影響安全性區域設定和受保護模式的 Internet Explorer 設定和群組原則
- 當使用 [IEChooser](/office/dev/add-ins/testing/debug-add-ins-using-f12-developer-tools-on-windows-10) 啟動時，適用於 IE 的 F12 開發人員工具
- Microsoft Edge 延伸模組 (不支援直接與 IE 頁面內容互動的延伸模組。)

### <a name="ie-mode-doesnt-support-the-following-internet-explorer-functionality"></a>IE 模式不支援以下 Internet Explorer 功能

- Internet Explorer 工具列
- 影響瀏覽功能表的 Internet Explorer 設定和群組原則 (例如 - 搜尋引擎和首頁)。
- IE11 或 Microsoft Edge F12 開發人員工具

## <a name="prerequisites"></a>必要條件

以下必要條件適用於以 IE 模式使用 Microsoft Edge。

> [!IMPORTANT]
> 為確保成功，請安裝 Windows 和 Microsoft Edge 的最新更新。 如果不這麼做，可能會造成 IE 模式失敗。

1. 下表列出作業系統的最小系統更新。

 | 作業系統 | 版本       | 更新 |
 |------------------|---------------|---------|
 | Windows 10       | 1909 或更新版本 |         |
 | Windows 10       | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) 或更新版本 |
 | Windows Server   | 1903          | [KB4501375](https://support.microsoft.com/help/4501375/windows-10-update-kb4501375) 或更新版本 |
 | Windows 10       | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) 或更新版本 |
 | Windows Server   | 1809          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) 或更新版本 |
 | Windows Server   | 2019          | [KB4501371](https://support.microsoft.com/help/4501371/windows-10-update-kb4501371) 或更新版本 |
 | Windows 10       | 1803          | [KB4512509](https://support.microsoft.com/help/4512509/windows-10-update-kb4512509) 或更新版本 |
 | Windows 10       | 1709          | [KB4512494](https://support.microsoft.com/help/4512494/windows-10-update-kb4512494) 或更新版本 |
 | Windows 10       | 1607          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) 或更新版本 |
 | Windows Server   | 2016          | [KB4516061](https://support.microsoft.com/help/4516061/windows-10-update-kb4516061) 或更新版本 |
 | Windows 10       | 初始版本，2015 年 7 月 | [KB4520011](https://support.microsoft.com/help/4520011/windows-10-update-kb4520011) 或更新版本 |
 | Windows 8       | 8.1              | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
 | Windows Server   | 2012 R2       | [KB4507463](https://support.microsoft.com/help/4507463/july-16-2019-kb4507463-os-build-preview-of-monthly-rollup) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
 | Windows 8  | 內嵌            | 安裝 [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) 以升級到Internet Explorer 11；然後安裝 [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
 | Windows Server   | 2012           | 安裝 [KB4492872](https://support.microsoft.com/help/4492872/update-for-internet-explorer-april-16-2019) 以升級到Internet Explorer 11；然後安裝 [KB4507447](https://support.microsoft.com/help/4507447/windows-server-2012-update-kb4507447) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
 | Windows 7        |  SP1**        | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
 | Windows Server   |  2008 R2**    | [KB4507437](https://support.microsoft.com/help/4507437/windows-7-update-kb4507437) 或更新版本；或 [KB4511872](https://support.microsoft.com/help/4511872/cumulative-security-update-for-internet-explorer) 或更新版本 |
  > [!IMPORTANT]
  > ** Windows 7 和 Windows Server 2008 R2 將受 Microsoft Edge 支援，即使這些作業系統退出支援。 為了使 IE 模式在這些作業系統上得到支援，裝置將需要 [Windows 7 的延長安全性更新](https://support.microsoft.com/help/4527878/faq-about-extended-security-updates-for-windows-7)。 建議您盡快升級到受支援的作業系統，以保持安全。 延伸安全更新對 Microsoft Edge 的支援應被視為臨時橋樑，以獲得支援的作業系統狀態。

2. Microsoft Edge 系統管理範本。 如需詳細資訊，請參閱[設定 Microsoft Edge](./configure-microsoft-edge.md)。
3. 在 Windows 功能中啟用了 Internet Explorer 11。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)