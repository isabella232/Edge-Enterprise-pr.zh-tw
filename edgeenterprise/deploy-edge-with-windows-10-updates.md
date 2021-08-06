---
title: 使用 Windows 10 更新部署 Microsoft Edge
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Windows 10 更新部署 Microsoft Edge
ms.openlocfilehash: 8ef5bd79059f31eb368a415ccca456fcea43788aed5738ed626a476b71a7d1ad
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726176"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a>使用 Windows 10 更新部署 Microsoft Edge

本文為使用 Windows 10 更新部署 Microsoft Edge 的使用者提供相關資訊。

## <a name="for-windows-10-release-20h2"></a>針對 Windows 10 版本 20H2

Windows 10 版本 20H2 已安裝 Microsoft Edge 做為其預設瀏覽器。

## <a name="for-windows-10-releases-rs4-through-20h1"></a>Windows 10 版本 RS4 至 20H1

Windows Server Update Services (WSUS) 中具有 Windows 10 從 RS4 至 20H1 的每個版本更新，將會移除舊版 Microsoft Edge 桌面應用程式，並以 Microsoft Edge 取代它。 如需詳細資訊，請參閱[此支援文章](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c)，了解哪些 WSUS 更新適合您的 Windows 版本。

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a>針對早於 RS4 的 Windows 10 版本 (和 Windows 7、8.1 和更早版本)

這些版本無法透過 Windows Update 來安裝 Microsoft Edge。 請考慮將 Microsoft Edge 部署至這些裝置的其他選項，例如 [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) 或 [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)