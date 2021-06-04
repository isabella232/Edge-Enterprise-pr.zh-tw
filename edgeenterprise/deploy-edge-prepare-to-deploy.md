---
title: 您環境中的 Microsoft Edge
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 您環境中的 Microsoft Edge
ms.openlocfilehash: e1418d21ff9e541d83d5b86baf5ff25c50d2299d
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313924"
---
# 您環境中的 Microsoft Edge

本文說明如何針對舊版 Microsoft Edge 終止服務對部署 Microsoft Edge 做好準備。

根據 Microsoft Edge 產品小組的[部落格文章](https://aka.ms/EdgeLegacyEOS)，對舊版 Microsoft Edge 桌面應用程式的支援服務將於 2021 年 3 月 9 日結束。 當您套用 4 月的更新星期二 (或 "B") 發行時，它會從執行 Windows 10 RS4 至 20H1 的裝置移除舊版 Microsoft Edge，並以 Microsoft Edge 取代。

##  <a name="how-to-prepare"></a>如何準備

若要對透過 4 月的更新星期二發行在 Windows 10 RS4 到 20H1 裝置上安裝 Microsoft Edge 進行準備，建議您閱讀[規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)。

規劃部署之後，請使用下列其中一種方法來準備部署 Microsoft Edge。

- **安裝群組原則，以自訂您的 Microsoft Edge 更新方法**。 如需詳細資訊，請參閱[在 Windows 上設定 Microsoft Edge 原則設定](configure-microsoft-edge.md)，並特別注意[更新原則參考](microsoft-edge-update-policies.md)資料。 如果您在安裝 4 月的更新星期二發行之前安裝群組原則來管理您的更新，Microsoft Edge 就會立即開始採用您的原則。 如果未安裝任何群組原則，Microsoft Edge 會自動自行更新。

- **在舊版 Microsoft Edge 桌面應用程式終止服務日期 2021 年 3 月 9日之前將其移除，並部署 Microsoft Edge**。 若為 Windows 10 RS4 到 20H1，您可以使用 Windows Update 來執行此動作。 如需詳細資訊，請參閱[使用 Windows 10 更新部署 Microsoft Edge](deploy-edge-with-windows-10-updates.md)。

##  <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)