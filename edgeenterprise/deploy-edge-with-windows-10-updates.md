---
title: 使用 Windows 10 更新部署 Microsoft Edge
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 Windows 10 更新部署 Microsoft Edge
ms.openlocfilehash: a000e3426792df79d1450c838b7848be10d6b0ca
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313923"
---
# 使用 Windows 10 更新部署 Microsoft Edge

本文為使用 Windows 10 更新部署 Microsoft Edge 的使用者提供相關資訊。

## 針對 Windows 10 版本 20H2

Windows 10 版本 20H2 已安裝 Microsoft Edge 做為其預設瀏覽器。

## Windows 10 版本 RS4 至 20H1

Windows Server Update Services (WSUS) 中具有 Windows 10 從 RS4 至 20H1 的每個版本更新，將會移除舊版 Microsoft Edge 桌面應用程式，並以 Microsoft Edge 取代它。 如需詳細資訊，請參閱[此支援文章](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c)，了解哪些 WSUS 更新適合您的 Windows 版本。

## 針對早於 RS4 的 Windows 10 版本 (和 Windows 7、8.1 和更早版本)

這些版本無法透過 Windows Update 來安裝 Microsoft Edge。 請考慮將 Microsoft Edge 部署至這些裝置的其他選項，例如 [Configuration Manager](https://docs.microsoft.com/configmgr/apps/deploy-use/deploy-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json) 或 [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge/?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)