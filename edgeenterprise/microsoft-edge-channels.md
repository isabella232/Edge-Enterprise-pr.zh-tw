---
title: Microsoft Edge 通道概觀
ms.author: srugh
author: srugh
manager: seanlynd
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 通道概觀
ms.openlocfilehash: 7d1fb72b458569cb4e4c6f44a6d89be7f65984df
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979442"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Microsoft Edge 通道的概觀

下一版 Microsoft Edge 的好處之一是 Microsoft 可以定期提供新功能。 但是，身為將 Microsoft Edge 部署到組織中使用者的系統管理員，您可能希望對於使用者取得這些新功能的頻率具有更多控制權。 Microsoft 為您提供了四個選項 (稱為通道) 來控制以新功能更新 Microsoft Edge 的頻率。 以下是四個選項概觀。

如需每個通道支援的資訊，請參閱：[Microsoft Edge 生命週期](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="channel-overview"></a>通道概觀

|通道|主要用途|以新功能更新的頻率|支援？|
|:---:|---|:---:|:---:|
|[Stable](#stable-channel)|廣泛部署|~6 週|是|
|[Beta](#beta-channel)|組織中的代表驗證|~6 週|是|
|[Dev](#dev-channel)|計劃和開發|每週|否|
|[Canary](#canary-channel)|先進內容|每天|否|

您決定向使用者部署哪個更新通道取決於幾個因素，例如使用者利用了多少企業營運應用程式，以及每當使用者擁有更新版本 Microsoft Edge 時，您都需要先行測試。 為了協助您做出決策，請檢閱以下可用於 Microsoft Edge 的四個更新通道的相關資訊。

### <a name="stable-channel"></a>Stable 通道

Stable 通道用於組織中的廣泛部署，它是大多數使用者應該使用的通道。 它是最穩定的通道，是之前 Beta 通道發行所提供功能集的穩定性結果。 新功能大約每 6 週發佈一次。 安全性和品質更新視需要發佈。 直到該通道的下一個發行版本可用之前，來自 Stable 通道的發行都被視為提供服務。

### <a name="beta-channel"></a>Beta 通道

Beta 通道用於向您組織中一組具代表性的使用者樣本進行生產環境部署。 它是受支援版本，並且 Beta 的每個版本都提供服務，直到此通道的下一版可用為止。 這是驗證您環境中的事物是否如預期運作的絕佳機會，如果您遇到問題，請先對其進行補救然後再發佈到 Stable 通道。 新功能大約每 6 週發佈一次。 安全性和品質更新視需要發佈。

### <a name="dev-channel"></a>Dev 通道

Dev 通道用於協助您規劃和開發 Microsoft Edge 的最新功能，其品質高於 Canary 通道。 您可以盡早了解接下來會發生什麼事，並為下一個 Beta 版做好準備。

### <a name="canary-channel"></a>Canary 通道

Canary 通道每天發佈，是所有通道中最先進的。 如果您想獲得最新的投資，它們將首先出現在這裡。 由於此頻率的性質，會不斷出現問題，因此，如果您正在運用 Canary 版本，則可能需要並排安裝另一個通道。

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [通道下載](https://aka.ms/EdgeEnterprise)
