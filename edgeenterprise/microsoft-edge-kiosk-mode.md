---
title: Microsoft Edge kiosk 模式
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge kiosk 模式
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979600"
---
# Microsoft Edge kiosk 模式

本文概述 Microsoft Edge (版本 77 或更新版本) kiosk 模式選項。 同時也涵蓋繼續使用 Microsoft Edge 舊版 kiosk 模式 (版本 45 和較舊版本) 所需具備的條件。

如需 Microsoft Edge 舊版 kiosk 模式 (版本 45 和較舊版本) 的相關資訊，請參閱[部署 Microsoft Edge kiosk 模式](https://aka.ms/edgekioskmode)。

## 具有受指派的存取權的 Microsoft Edge

Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於 Microsoft Edge 舊版「正常瀏覽」kiosk 模式類型。 若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)中的指示進行。 Microsoft Edge Stable 通道的 AUMID 是 **MSEdge**。

使用具有受指派的存取權的 Microsoft Edge 時，您可以使用 [Microsoft Edge 瀏覽器原則](microsoft-edge-policies.md)來設定瀏覽體驗，以滿足您的獨特要求。

目前 Microsoft Edge 不支援與單一應用程式受指派的存取權相同的 Microsoft Edge 舊版 kiosk 模式類型，以及多應用程式受指派的存取權中的「公用瀏覽」kiosk 模式類型。 如果您需要適用於單一應用程式受指派的存取權 kiosk 裝置的瀏覽器，我們建議您使用 [Microsoft Edge 舊版 kiosk 模式](https://aka.ms/edgekioskmode)或 [Microsoft Kiosk 瀏覽器應用程式](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab)。 

## Microsoft Edge “--kiosk” 命令列參數

您可以使用 “`--kiosk`” 命令列參數在 kiosk 模式下啟動 Microsoft Edge。 這將在停用全螢幕鍵盤快速鍵 (F11) 時以全螢幕開啟瀏覽器。 若要完成這項操作，請建立一個快速鍵，將目標設定為：<br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> "`--kiosk`" 參數不會阻止使用者存取 Windows 鍵盤快速鍵，也不會阻止其他應用程式執行。 若要完成這種控制類型，請考慮使用 [AppLocker 建立 Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) 和[鍵盤篩選器](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter)。

若要退出 kiosk 模式並關閉瀏覽器，請使用 alt+F4。

## 支援 Microsoft Edge 舊版 kiosk 模式

安裝新版本的 Microsoft Edge Stable 通道時，會隱藏 Microsoft Edge 舊版，並將所有啟動 Microsoft Edge 舊版的嘗試重新導向到新版本。 如需以下相關資訊：

- Windows Update 需求，請參閱[支援下一版 Microsoft Edge 的 Windows Update](microsoft-edge-sysupdate-windows-updates.md) 
- 安裝 Microsoft Edge 後存取 Microsoft Edge 舊版，請參閱[安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版](microsoft-edge-sysupdate-access-old-edge.md)
 
若要繼續在 kiosk 裝置上使用 Microsoft Edge 舊版 kiosk 模式，請採取以下動作之一： 

- 如果您計畫安裝 Microsoft Edge Stable 通道、希望允許安裝它，或是已在 kiosk 裝置上安裝它，請部署 Microsoft Edge [允許 Microsoft Edge 並排瀏覽器體驗](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)原則。
- 若要防止 Microsoft Edge Stable 通道安裝在您的 kiosk 裝置上，請部署適用於 Stable 通道的 Microsoft Edge [允許安裝預設值](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default)原則或考慮使用[封鎖程式工具組用來停用自動傳遞 Microsoft Edge](microsoft-edge-blocker-toolkit.md)。 

## 也請參閱

- [設定 Windows 桌面版的 Kiosk 與數位招牌](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [部署 Microsoft Edge 舊版 kiosk 模式](https://aka.ms/edgekioskmode) 
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
