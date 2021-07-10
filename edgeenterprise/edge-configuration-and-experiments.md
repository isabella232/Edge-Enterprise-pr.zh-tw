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
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641559"
---
# <a name="microsoft-edge-configurations-and-experimentation"></a><span data-ttu-id="e695a-103">Microsoft Edge 設定和實驗</span><span class="sxs-lookup"><span data-stu-id="e695a-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="e695a-104">本文介紹 Microsoft Edge 與 Experimentation and Configuration Service (ECS) 之間的互動。</span><span class="sxs-lookup"><span data-stu-id="e695a-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="e695a-105">Microsoft Edge 會與此服務通訊以請求和接收不同種類的承載。</span><span class="sxs-lookup"><span data-stu-id="e695a-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="e695a-106">這些承載包括設定、功能推出和實驗。</span><span class="sxs-lookup"><span data-stu-id="e695a-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e695a-107">確定用戶端能夠存取 `https://config.edge.skype.com`，因而能接收負載。</span><span class="sxs-lookup"><span data-stu-id="e695a-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="e695a-108">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e695a-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configurations"></a><span data-ttu-id="e695a-109">設定</span><span class="sxs-lookup"><span data-stu-id="e695a-109">Configurations</span></span>

<span data-ttu-id="e695a-110">設定是旨在確保產品良好、安全和符合隱私權的承載，旨在對所有使用者提供相同的價值 (根據平台和通道)。這可以為網域動作啟用功能標誌，也可用於在發生錯誤時停用功能標誌。</span><span class="sxs-lookup"><span data-stu-id="e695a-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <a name="controlled-feature-rollout"></a><span data-ttu-id="e695a-111">受控功能推出</span><span class="sxs-lookup"><span data-stu-id="e695a-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="e695a-112">受控功能推出 (CFR) 是緩慢增加接收功能之使用者群組大小的程序。</span><span class="sxs-lookup"><span data-stu-id="e695a-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="e695a-113">透過將新功能散佈給使用者群的隨機選取子集，可以將使用者意見反應與未使用功能的同等大小對照組進行比較，來測量該功能造成的影響。</span><span class="sxs-lookup"><span data-stu-id="e695a-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <a name="experiments"></a><span data-ttu-id="e695a-114">實驗</span><span class="sxs-lookup"><span data-stu-id="e695a-114">Experiments</span></span>

<span data-ttu-id="e695a-115">Microsoft Edge 組建具有仍在開發中或正在試驗的特性和功能。</span><span class="sxs-lookup"><span data-stu-id="e695a-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="e695a-116">實驗類似於 CFR，但使用者群組比較小，因為用於測試新概念。</span><span class="sxs-lookup"><span data-stu-id="e695a-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="e695a-117">這些功能預設為隱藏，直到功能推出或實驗完成為止。</span><span class="sxs-lookup"><span data-stu-id="e695a-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="e695a-118">實驗標誌用於啟用和停用這些功能。</span><span class="sxs-lookup"><span data-stu-id="e695a-118">Experiment flags are used to enable and disable these features.</span></span>

## <a name="about-the-ecs"></a><span data-ttu-id="e695a-119">關於 ECS</span><span class="sxs-lookup"><span data-stu-id="e695a-119">About the ECS</span></span>

<span data-ttu-id="e695a-120">在上述所有方案中，服務會將功能標誌值傳遞到瀏覽器用戶端，以便套用它們。</span><span class="sxs-lookup"><span data-stu-id="e695a-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="e695a-121">根據更新，設定會立即套用，或是在使用者重新啟動瀏覽器時套用。</span><span class="sxs-lookup"><span data-stu-id="e695a-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="e695a-122">Microsoft Edge 與此服務的互動由 [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) 原則中的設定控制。</span><span class="sxs-lookup"><span data-stu-id="e695a-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](./microsoft-edge-policies.md#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="e695a-123">您可將原則設定設定為：</span><span class="sxs-lookup"><span data-stu-id="e695a-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="e695a-124">僅擷取設定</span><span class="sxs-lookup"><span data-stu-id="e695a-124">Retrieve configurations only</span></span>
- <span data-ttu-id="e695a-125">擷取設定和實驗</span><span class="sxs-lookup"><span data-stu-id="e695a-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="e695a-126">停用與服務的通訊</span><span class="sxs-lookup"><span data-stu-id="e695a-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="e695a-127">如果停用與服務的通訊，這將影響 Microsoft 及時回應嚴重錯誤的能力。</span><span class="sxs-lookup"><span data-stu-id="e695a-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <a name="see-also"></a><span data-ttu-id="e695a-128">也請參閱</span><span class="sxs-lookup"><span data-stu-id="e695a-128">See also</span></span>

- [<span data-ttu-id="e695a-129">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="e695a-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="e695a-130">Microsoft Edge 文件登陸頁面</span><span class="sxs-lookup"><span data-stu-id="e695a-130">Microsoft Edge documentation landing page</span></span>](./index.yml)