---
title: 有關企業中的 Edge 的常見問題集
ms.author: jwhit
author: jwhit-MSFT
manager: laurawi
ms.date: 11/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 有關在企業中部署 Microsoft Edge 的常見問題集
ms.openlocfilehash: e689967cbad950e2969535bad0dd63d5d7081798
ms.sourcegitcommit: 12827458f6217f443128e826c1d18d36d401d03b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154318"
---
# 有關企業中的 Microsoft Edge 的常見問題集

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 如何知道我的 Microsoft Edge 是什麼版本？

按一下 Microsoft Edge 右上角的省略符號圖示 (**…**)，再按一下**設定**。 選取**關於 Microsoft Edge** 以查看 Microsoft Edge 版本。

## Internet Explorer 11 會繼續收到更新嗎？

我們致力於將 Internet Explorer 保持為受支援、可靠且安全的瀏覽器。 Internet Explorer 仍是 Windows 的元件，並遵循其安裝所在作業系統的支援週期。 如需詳細資訊，請參閱[生命週期常見問題 – Internet Explorer](https://support.microsoft.com/help/17454/)。 雖然我們會繼續支援和更新 Internet Explorer，但最新的功能和平台更新僅適用於 Microsoft Edge。

## 嘗試新版本時，是否可以並排執行目前版本的 Microsoft Edge (Microsoft Edge 舊版)？

可以。 2020 年 1 月 15 日之後，新版本 Microsoft Edge (以 Chromium 為基礎) 將散發到執行 Windows 10 版本 1803 或更新版本的家用版和專業版裝置。 加入網域的裝置將從此自動更新中排除。 如需詳細資訊，請參閱 [Microsoft Edge Update 概觀](https://docs.microsoft.com/deployedge/microsoft-edge-blocker-toolkit#overview)。 在評估 Microsoft Edge 的下一個版本時，可以並排安裝 Microsoft Edge 舊版。 如需詳細資訊，請參閱[如何存取舊版 Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)。 此外，每個新的 Microsoft Edge 通道也支援並排安裝。 如需詳細資訊，請參閱 [Microsoft Edge 通道的概觀](https://docs.microsoft.com/deployedge/microsoft-edge-channels)。

## Microsoft Edge (以 Chromium 為基礎) 是否支援 ActiveX 控制項或 BHO (例如 Silverlight 或 Java)？

不。 Microsoft Edge 不支援 ActiveX 控制項和 BHO (例如 Silverlight 或 Java)。 不過，如果您執行使用 ActiveX 控制項的 Web 應用程式、BHO 或 Internet Explorer 11 上的傳統文件模式，可以將它們設定為在 Microsoft Edge 的 IE 模式中執行。 如需詳細資訊，請參閱[在 Microsoft Edge 上設定 IE 模式](https://docs.microsoft.com/DeployEdge/edge-ie-mode)。

## 我的最愛能否從目前版本的 Microsoft Edge 移植，還是必須重新新增？

目前，Microsoft Edge 支援從現有安裝的 Microsoft Edge、Chrome、Internet Explorer 和 Firefox (在 Win10 上) 匯入。 匯入時支援以下設定：書籤、歷史記錄、密碼和自動填寫 (付款、地址和通用表單)。 您可以選擇從 [初次執行體驗] 或是從瀏覽器設定匯入。  

## Stable、Beta、Dev 和 Canary 通道/組建之間的區別是什麼？

下一版 Microsoft Edge 的 Stable 通道是我們所提供最穩定的預覽通道，具有以企業為中心的功能，可供您在整個組織中[試用和評估](https://aka.ms/EdgeEnterprise)。 Beta 通道可讓您向一組具代表性的使用者驗證下一個穩定版本。 Stable 和 Beta 通道大約每六週更新一次。 Dev 和 Canary 通道分別持續每週和每天更新。 離線安裝程式 (MSI 和 PKG 檔案) 僅適用於穩定、Beta 和 Dev 通道。 如需詳細資訊，請參閱 [Microsoft Edge 通道的概觀](https://docs.microsoft.com/deployedge/microsoft-edge-channels)。

## 新版本 Microsoft Edge 提供哪些擴充功能支援？

Microsoft Edge 支援 [Microsoft Edge Insider Addons](https://go.microsoft.com/fwlink/?linkid=2081222) 和 [Chrome 線上應用程式商店](https://go.microsoft.com/fwlink/?linkid=2072338)的擴充功能。

## 你們是否支援行動裝置管理 (MDM) 和 Microsoft Intune？

是。 現已支援使用 Microsoft Intune 和行動裝置管理 (MDM) 來設定 Windows 10 上的 Microsoft Edge。 如需詳細資訊，請參閱[使用 Microsoft Intune 設定 Microsoft Edge](configure-edge-with-intune.md)以及[使用行動裝置管理設定 Microsoft Edge](configure-edge-with-mdm.md)。

## WSUS 是否支援新 Microsoft Edge 的初始部署？

是。 [[Microsoft Update Catalog]](https://www.catalog.update.microsoft.com/Search.aspx?q=the%20new%20microsoft%20edge%20for%20windows) 中的套件可用於經 WSUS 進行的新版 Microsoft Edge 初始部署。 在初始部署之後，系統預設的設定為自動更新。 如需詳細資訊，請參閱 [WSUS 更新，適用於 Windows 10 版 (版本為 1809、1903、1909 和 2004：2020 年 10 月 29 日) 的新版 Microsoft Edge](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge)。

手動更新可以透過設定管理工具完成，例如 [ConfigMgr](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)。

## 請參閱

- [Microsoft Edge 文件登陸頁面](https://docs.microsoft.com/DeployEdge/)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
