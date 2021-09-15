---
title: 適用於 Microsoft Edge 穩定通道更新的漸進式套件推出
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 適用於 Microsoft Edge 穩定通道更新的漸進式套件推出
ms.openlocfilehash: bdcefdc118125d67057fa77513bd732cff6882e3
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979399"
---
# <a name="progressive-rollouts-for-microsoft-edge-stable-channel-updates"></a>適用於 Microsoft Edge 穩定通道更新的漸進式套件推出

從 Microsoft Edge 83 版本開始，我們將在幾天內逐步推出 Microsoft Edge 穩定通道的重大更新。 這可讓我們監視更新，並安全地更新整個組織的瀏覽器。

> [!NOTE]
> 本文適用於 Microsoft Edge 穩定通道 83 或更新版本。

## <a name="why-do-we-need-progressive-rollout"></a>為什麼我們需要漸進式推出？

透過密切監視更新的運行狀況並在幾天內發行更新，我們可以限制新更新可能造成的問題的影響。 在 Microsoft Edge 版本 83 中，系統會為所有 Windows 7、Windows 8 & 8.1 和 Windows 10 版 Microsoft Edge 啟用漸進式部署。 我們將儘快支援 Mac 上的 Microsoft Edge。

## <a name="how-will-the-updates-work"></a>更新將如何運作？

每次安裝 Microsoft Edge 時都會指派一個升級值。 當我們開始漸進推出時，當裝置上的值在升級值範圍內時，您將看到更新。 隨著推出的進行 (幾天內)，所有使用者最終都會獲得更新。 與沒有重大安全性修正的更新相比，具有重大安全性修復的瀏覽器更新的推出節奏更快。 這么做是為了確保對漏洞的及時提示。

## <a name="how-does-this-affect-enterprises"></a>這對企業有何影響？

Microsoft Edge 構建使用多種機制，如 Microsoft Intune、Windows Server Update Service (WSUS) 和設定管理員來散發到企業。 這些部署工具與漸進式推出的運作不同：

- 透過 Microsoft Intune 管理散發的企業會註冊為自動更新。 使用漸進式推出，所有使用者將在幾天內看到更新。
- 透過 WSUS (Windows Server Update Services) 或 設定管理員管理散發的企業不會註冊自動更新。 管理員管理並套用從開始就可用的更新。 漸進式部署不會影響這個程式。

如有任何顧慮或問題，請透過使用者意見、應用程序內的意見反應按鈕或下方的註解來分享您的寶貴意見。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
