---
title: Microsoft Edge 設定和實驗
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/20/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 設定和實驗
ms.openlocfilehash: f66da4075c33c1f375dfb593c1a1bd2b4a139833
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979490"
---
# <span data-ttu-id="59083-103">Microsoft Edge 設定和實驗</span><span class="sxs-lookup"><span data-stu-id="59083-103">Microsoft Edge configurations and experimentation</span></span>

<span data-ttu-id="59083-104">本文介紹 Microsoft Edge 與 Experimentation and Configuration Service (ECS) 之間的互動。</span><span class="sxs-lookup"><span data-stu-id="59083-104">This article describes the interaction between Microsoft Edge and the Experimentation and Configuration Service (ECS).</span></span> <span data-ttu-id="59083-105">Microsoft Edge 會與此服務通訊以請求和接收不同種類的承載。</span><span class="sxs-lookup"><span data-stu-id="59083-105">Microsoft Edge communicates with this service to request and receive different kinds of payloads.</span></span> <span data-ttu-id="59083-106">這些承載包括設定、功能推出和實驗。</span><span class="sxs-lookup"><span data-stu-id="59083-106">These payloads include configurations, feature rollouts, and experiments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59083-107">確定用戶端能夠存取 `https://config.edge.skype.com`，因而能接收負載。</span><span class="sxs-lookup"><span data-stu-id="59083-107">Make sure clients are able to access `https://config.edge.skype.com` so payloads can be received.</span></span>

> [!NOTE]
> <span data-ttu-id="59083-108">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="59083-108">This applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="59083-109">設定</span><span class="sxs-lookup"><span data-stu-id="59083-109">Configurations</span></span>

<span data-ttu-id="59083-110">設定是旨在確保產品良好、安全和符合隱私權的承載，旨在對所有使用者提供相同的價值 (根據平台和通道)。這可以為網域動作啟用功能標誌，也可用於在發生錯誤時停用功能標誌。</span><span class="sxs-lookup"><span data-stu-id="59083-110">Configurations are the payload meant to ensure product health, security, and privacy compliance, and are intended to have the same value for all the users (based on platforms and channels.) This could be to enable a feature flag for a domain action, and can also be used to disable a feature flag in the event of a bug.</span></span>

## <span data-ttu-id="59083-111">受控功能推出</span><span class="sxs-lookup"><span data-stu-id="59083-111">Controlled Feature Rollout</span></span>

<span data-ttu-id="59083-112">受控功能推出 (CFR) 是緩慢增加接收功能之使用者群組大小的程序。</span><span class="sxs-lookup"><span data-stu-id="59083-112">Controlled Feature Rollout (CFR) is a procedure for slowly increasing the size of the user group that receives a feature.</span></span> <span data-ttu-id="59083-113">透過將新功能散佈給使用者群的隨機選取子集，可以將使用者意見反應與未使用功能的同等大小對照組進行比較，來測量該功能造成的影響。</span><span class="sxs-lookup"><span data-stu-id="59083-113">By distributing a new feature to a randomly selected subset of the user population, it’s possible to compare user feedback to an equally sized control group without the feature to measure the impact of the feature.</span></span>

## <span data-ttu-id="59083-114">實驗</span><span class="sxs-lookup"><span data-stu-id="59083-114">Experiments</span></span>

<span data-ttu-id="59083-115">Microsoft Edge 組建具有仍在開發中或正在試驗的特性和功能。</span><span class="sxs-lookup"><span data-stu-id="59083-115">Microsoft Edge builds have features and functionality that are still in development or are experimental.</span></span> <span data-ttu-id="59083-116">實驗類似於 CFR，但使用者群組比較小，因為用於測試新概念。</span><span class="sxs-lookup"><span data-stu-id="59083-116">Experiments are like CFR, but the size of the user group is much smaller for testing the new concept.</span></span> <span data-ttu-id="59083-117">這些功能預設為隱藏，直到功能推出或實驗完成為止。</span><span class="sxs-lookup"><span data-stu-id="59083-117">These features are hidden by default until the feature's rolled out or the experiment's finished.</span></span> <span data-ttu-id="59083-118">實驗標誌用於啟用和停用這些功能。</span><span class="sxs-lookup"><span data-stu-id="59083-118">Experiment flags are used to enable and disable these features.</span></span>

## <span data-ttu-id="59083-119">關於 ECS</span><span class="sxs-lookup"><span data-stu-id="59083-119">About the ECS</span></span>

<span data-ttu-id="59083-120">在上述所有方案中，服務會將功能標誌值傳遞到瀏覽器用戶端，以便套用它們。</span><span class="sxs-lookup"><span data-stu-id="59083-120">In all the preceding scenarios, the service delivers the feature flag values to the browser client so they can be applied.</span></span> <span data-ttu-id="59083-121">根據更新，設定會立即套用，或是在使用者重新啟動瀏覽器時套用。</span><span class="sxs-lookup"><span data-stu-id="59083-121">Depending on the update, configurations are applied immediately or when the user restarts the browser.</span></span>

<span data-ttu-id="59083-122">Microsoft Edge 與此服務的互動由 [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) 原則中的設定控制。</span><span class="sxs-lookup"><span data-stu-id="59083-122">Microsoft Edge's interaction with this service is controlled by settings in the [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol) policy.</span></span> <span data-ttu-id="59083-123">您可將原則設定設定為：</span><span class="sxs-lookup"><span data-stu-id="59083-123">You can configure policy settings to:</span></span>

- <span data-ttu-id="59083-124">僅擷取設定</span><span class="sxs-lookup"><span data-stu-id="59083-124">Retrieve configurations only</span></span>
- <span data-ttu-id="59083-125">擷取設定和實驗</span><span class="sxs-lookup"><span data-stu-id="59083-125">Retrieve configurations and experiments</span></span>
- <span data-ttu-id="59083-126">停用與服務的通訊</span><span class="sxs-lookup"><span data-stu-id="59083-126">Disable communication with the service</span></span>

  > [!CAUTION]
  > <span data-ttu-id="59083-127">如果停用與服務的通訊，這將影響 Microsoft 及時回應嚴重錯誤的能力。</span><span class="sxs-lookup"><span data-stu-id="59083-127">If you disable communications with the service, this will affect Microsoft’s ability to respond to a severe bug in a timely manner.</span></span>

## <span data-ttu-id="59083-128">也請參閱</span><span class="sxs-lookup"><span data-stu-id="59083-128">See also</span></span>

- [<span data-ttu-id="59083-129">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="59083-129">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="59083-130">Microsoft Edge 文件登陸頁面</span><span class="sxs-lookup"><span data-stu-id="59083-130">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
