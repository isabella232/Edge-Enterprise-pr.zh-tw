---
title: Microsoft Edge 設定和實驗
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 設定和實驗
ms.openlocfilehash: 1ebfe5fc1da107aa7e9e20b629f14aff468bdd6d
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978816"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a>Microsoft Edge 設定和實驗

本文介紹 Microsoft Edge 與 Experimentation and Configuration Service (ECS) 之間的互動。 Microsoft Edge 會與此服務通訊以請求和接收不同種類的承載。 這些承載包括設定、功能推出和實驗。

> [!IMPORTANT]
> 確定用戶端能夠存取 `https://config.edge.skype.com`，因而能接收負載。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="configurations"></a>設定

設定是旨在確保產品良好、安全和符合隱私權的承載，旨在對所有使用者提供相同的價值 (根據平台和通道)。這可以為網域動作啟用功能標誌，也可用於在發生錯誤時停用功能標誌。

## <a name="controlled-feature-rollout"></a>受控功能推出

受控功能推出 (CFR) 是緩慢增加接收功能之使用者群組大小的程序。 透過將新功能散佈給使用者群的隨機選取子集，可以將使用者意見反應與未使用功能的同等大小對照組進行比較，來測量該功能造成的影響。

## <a name="experiments"></a>實驗

Microsoft Edge 組建具有仍在開發中或正在試驗的特性和功能。 實驗類似於 CFR，但使用者群組比較小，因為用於測試新概念。 這些功能預設為隱藏，直到功能推出或實驗完成為止。 實驗標誌用於啟用和停用這些功能。

## <a name="about-the-ecs"></a>關於 ECS

在上述所有方案中，服務會將功能標誌值傳遞到瀏覽器用戶端，以便套用它們。 根據更新，設定會立即套用，或是在使用者重新啟動瀏覽器時套用。

Microsoft Edge 與此服務的互動由 [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) 原則中的設定控制。 您可將原則設定設定為：

- 僅擷取設定
- 擷取設定和實驗
- 停用與服務的通訊

  > [!CAUTION]
  > 如果停用與服務的通訊，這將影響 Microsoft 及時回應嚴重錯誤的能力。

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://www.microsoftedgeinsider.com/enterprise)
- [Microsoft Edge 文件登陸頁面](./index.yml)