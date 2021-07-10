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
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641989"
---
# <a name="overview-of-the-microsoft-edge-channels"></a><span data-ttu-id="50db3-103">Microsoft Edge 通道的概觀</span><span class="sxs-lookup"><span data-stu-id="50db3-103">Overview of the Microsoft Edge channels</span></span>

<span data-ttu-id="50db3-104">下一版 Microsoft Edge 的好處之一是 Microsoft 可以定期提供新功能。</span><span class="sxs-lookup"><span data-stu-id="50db3-104">One of the benefits of the next version of Microsoft Edge is that Microsoft can provide new features on a regular basis.</span></span> <span data-ttu-id="50db3-105">但是，身為將 Microsoft Edge 部署到組織中使用者的系統管理員，您可能希望對於使用者取得這些新功能的頻率具有更多控制權。</span><span class="sxs-lookup"><span data-stu-id="50db3-105">However, as the admin who deploys Microsoft Edge to the users in your organization, you might want to have more control over how often your users get these new features.</span></span> <span data-ttu-id="50db3-106">Microsoft 為您提供了四個選項 (稱為通道) 來控制以新功能更新 Microsoft Edge 的頻率。</span><span class="sxs-lookup"><span data-stu-id="50db3-106">Microsoft provides you four options, called channels, to control how often Microsoft Edge is updated with new features.</span></span> <span data-ttu-id="50db3-107">以下是四個選項概觀。</span><span class="sxs-lookup"><span data-stu-id="50db3-107">Here's an overview of the four options.</span></span>

<span data-ttu-id="50db3-108">如需每個通道支援的資訊，請參閱：[Microsoft Edge 生命週期](/deployedge/microsoft-edge-support-lifecycle)</span><span class="sxs-lookup"><span data-stu-id="50db3-108">For more information on support for each channel read: [Microsoft Edge Lifecycle](/deployedge/microsoft-edge-support-lifecycle)</span></span>
  
> [!NOTE]
> <span data-ttu-id="50db3-109">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="50db3-109">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="channel-overview"></a><span data-ttu-id="50db3-110">通道概觀</span><span class="sxs-lookup"><span data-stu-id="50db3-110">Channel overview</span></span>

|<span data-ttu-id="50db3-111">通道</span><span class="sxs-lookup"><span data-stu-id="50db3-111">Channel</span></span>|<span data-ttu-id="50db3-112">主要用途</span><span class="sxs-lookup"><span data-stu-id="50db3-112">Primary purpose</span></span>|<span data-ttu-id="50db3-113">以新功能更新的頻率</span><span class="sxs-lookup"><span data-stu-id="50db3-113">How often updated with new features</span></span>|<span data-ttu-id="50db3-114">支援？</span><span class="sxs-lookup"><span data-stu-id="50db3-114">Supported?</span></span>|
|:---:|---|:---:|:---:|
|[<span data-ttu-id="50db3-115">Stable</span><span class="sxs-lookup"><span data-stu-id="50db3-115">Stable</span></span>](#stable-channel)|<span data-ttu-id="50db3-116">廣泛部署</span><span class="sxs-lookup"><span data-stu-id="50db3-116">Broad Deployment</span></span>|<span data-ttu-id="50db3-117">~6 週</span><span class="sxs-lookup"><span data-stu-id="50db3-117">~6 weeks</span></span>|<span data-ttu-id="50db3-118">是</span><span class="sxs-lookup"><span data-stu-id="50db3-118">Yes</span></span>|
|[<span data-ttu-id="50db3-119">Beta</span><span class="sxs-lookup"><span data-stu-id="50db3-119">Beta</span></span>](#beta-channel)|<span data-ttu-id="50db3-120">組織中的代表驗證</span><span class="sxs-lookup"><span data-stu-id="50db3-120">Representative validation in the organization</span></span>|<span data-ttu-id="50db3-121">~6 週</span><span class="sxs-lookup"><span data-stu-id="50db3-121">~6 weeks</span></span>|<span data-ttu-id="50db3-122">是</span><span class="sxs-lookup"><span data-stu-id="50db3-122">Yes</span></span>|
|[<span data-ttu-id="50db3-123">Dev</span><span class="sxs-lookup"><span data-stu-id="50db3-123">Dev</span></span>](#dev-channel)|<span data-ttu-id="50db3-124">計劃和開發</span><span class="sxs-lookup"><span data-stu-id="50db3-124">Planning and developing</span></span>|<span data-ttu-id="50db3-125">每週</span><span class="sxs-lookup"><span data-stu-id="50db3-125">Weekly</span></span>|<span data-ttu-id="50db3-126">否</span><span class="sxs-lookup"><span data-stu-id="50db3-126">No</span></span>|
|[<span data-ttu-id="50db3-127">Canary</span><span class="sxs-lookup"><span data-stu-id="50db3-127">Canary</span></span>](#canary-channel)|<span data-ttu-id="50db3-128">先進內容</span><span class="sxs-lookup"><span data-stu-id="50db3-128">Bleeding edge content</span></span>|<span data-ttu-id="50db3-129">每天</span><span class="sxs-lookup"><span data-stu-id="50db3-129">Daily</span></span>|<span data-ttu-id="50db3-130">否</span><span class="sxs-lookup"><span data-stu-id="50db3-130">No</span></span>|

<span data-ttu-id="50db3-131">您決定向使用者部署哪個更新通道取決於幾個因素，例如使用者利用了多少企業營運應用程式，以及每當使用者擁有更新版本 Microsoft Edge 時，您都需要先行測試。</span><span class="sxs-lookup"><span data-stu-id="50db3-131">Which update channel you decide to deploy to your users depends on several factors, such as how many line of business applications the user leverages and that you need to test any time they have an updated version of Microsoft Edge.</span></span> <span data-ttu-id="50db3-132">為了協助您做出決策，請檢閱以下可用於 Microsoft Edge 的四個更新通道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50db3-132">To help you make this decision, review the following information about the four update channels that are available for Microsoft Edge.</span></span>

### <a name="stable-channel"></a><span data-ttu-id="50db3-133">Stable 通道</span><span class="sxs-lookup"><span data-stu-id="50db3-133">Stable Channel</span></span>

<span data-ttu-id="50db3-134">Stable 通道用於組織中的廣泛部署，它是大多數使用者應該使用的通道。</span><span class="sxs-lookup"><span data-stu-id="50db3-134">The Stable Channel is intended for broad deployment in your organization, and it is the channel that most users should be on.</span></span> <span data-ttu-id="50db3-135">它是最穩定的通道，是之前 Beta 通道發行所提供功能集的穩定性結果。</span><span class="sxs-lookup"><span data-stu-id="50db3-135">It is the most stable of the channels and is the a result of the stabilization of the feature set available in the prior Beta Channel release.</span></span> <span data-ttu-id="50db3-136">新功能大約每 6 週發佈一次。</span><span class="sxs-lookup"><span data-stu-id="50db3-136">New features ship about every 6 weeks.</span></span> <span data-ttu-id="50db3-137">安全性和品質更新視需要發佈。</span><span class="sxs-lookup"><span data-stu-id="50db3-137">Security and quality updates ship as needed.</span></span> <span data-ttu-id="50db3-138">直到該通道的下一個發行版本可用之前，來自 Stable 通道的發行都被視為提供服務。</span><span class="sxs-lookup"><span data-stu-id="50db3-138">A release from the Stable Channel is serviced until the next release from the channel is available.</span></span>

### <a name="beta-channel"></a><span data-ttu-id="50db3-139">Beta 通道</span><span class="sxs-lookup"><span data-stu-id="50db3-139">Beta Channel</span></span>

<span data-ttu-id="50db3-140">Beta 通道用於向您組織中一組具代表性的使用者樣本進行生產環境部署。</span><span class="sxs-lookup"><span data-stu-id="50db3-140">The Beta Channel is intended for production deployment in your organization to a representative sample set of users.</span></span> <span data-ttu-id="50db3-141">它是受支援版本，並且 Beta 的每個版本都提供服務，直到此通道的下一版可用為止。</span><span class="sxs-lookup"><span data-stu-id="50db3-141">It is a supported release, and each release from Beta is serviced until the next release from this channel is available.</span></span> <span data-ttu-id="50db3-142">這是驗證您環境中的事物是否如預期運作的絕佳機會，如果您遇到問題，請先對其進行補救然後再發佈到 Stable 通道。</span><span class="sxs-lookup"><span data-stu-id="50db3-142">This is a great opportunity to validate that things work as expected in your environment, and if you encounter an issue have it remediated prior to the release going publishing to the Stable Channel.</span></span> <span data-ttu-id="50db3-143">新功能大約每 6 週發佈一次。</span><span class="sxs-lookup"><span data-stu-id="50db3-143">New features ship about every 6 weeks.</span></span> <span data-ttu-id="50db3-144">安全性和品質更新視需要發佈。</span><span class="sxs-lookup"><span data-stu-id="50db3-144">Security and quality updates ship as needed.</span></span>

### <a name="dev-channel"></a><span data-ttu-id="50db3-145">Dev 通道</span><span class="sxs-lookup"><span data-stu-id="50db3-145">Dev Channel</span></span>

<span data-ttu-id="50db3-146">Dev 通道用於協助您規劃和開發 Microsoft Edge 的最新功能，其品質高於 Canary 通道。</span><span class="sxs-lookup"><span data-stu-id="50db3-146">The Dev Channel is intended to help you plan and develop with the latest capabilities of Microsoft Edge, but with higher quality than the Canary Channel.</span></span> <span data-ttu-id="50db3-147">您可以盡早了解接下來會發生什麼事，並為下一個 Beta 版做好準備。</span><span class="sxs-lookup"><span data-stu-id="50db3-147">This is your opportunity to get an early look at what is coming next and prepare for the next Beta release.</span></span>

### <a name="canary-channel"></a><span data-ttu-id="50db3-148">Canary 通道</span><span class="sxs-lookup"><span data-stu-id="50db3-148">Canary Channel</span></span>

<span data-ttu-id="50db3-149">Canary 通道每天發佈，是所有通道中最先進的。</span><span class="sxs-lookup"><span data-stu-id="50db3-149">The Canary Channel ships daily and is the most bleeding edge of all the channels.</span></span> <span data-ttu-id="50db3-150">如果您想獲得最新的投資，它們將首先出現在這裡。</span><span class="sxs-lookup"><span data-stu-id="50db3-150">If you want access to the newest investments then they will appear here first.</span></span> <span data-ttu-id="50db3-151">由於此頻率的性質，會不斷出現問題，因此，如果您正在運用 Canary 版本，則可能需要並排安裝另一個通道。</span><span class="sxs-lookup"><span data-stu-id="50db3-151">Because of the nature of this cadence problems will arise overtime, so you may want another channel installed side by side if you are leveraging the Canary releases.</span></span>

## <a name="see-also"></a><span data-ttu-id="50db3-152">也請參閱</span><span class="sxs-lookup"><span data-stu-id="50db3-152">See also</span></span>

- [<span data-ttu-id="50db3-153">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="50db3-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="50db3-154">通道下載</span><span class="sxs-lookup"><span data-stu-id="50db3-154">Channel downloads</span></span>](https://aka.ms/EdgeEnterprise)
