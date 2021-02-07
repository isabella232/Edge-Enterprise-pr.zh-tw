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
# <span data-ttu-id="f53cb-103">您環境中的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f53cb-103">Microsoft Edge in your environment</span></span>

<span data-ttu-id="f53cb-104">本文說明如何針對舊版 Microsoft Edge 終止服務對部署 Microsoft Edge 做好準備。</span><span class="sxs-lookup"><span data-stu-id="f53cb-104">This article describes how to prepare to deploy Microsoft Edge when Microsoft Edge Legacy reaches its end of service.</span></span>

<span data-ttu-id="f53cb-105">根據 Microsoft Edge 產品小組的[部落格文章](https://aka.ms/EdgeLegacyEOS)，對舊版 Microsoft Edge 桌面應用程式的支援服務將於 2021 年 3 月 9 日結束。</span><span class="sxs-lookup"><span data-stu-id="f53cb-105">As per the Microsoft Edge Product Team’s [blog post](https://aka.ms/EdgeLegacyEOS), support for the Microsoft Edge Legacy desktop application will end on March 9, 2021.</span></span> <span data-ttu-id="f53cb-106">當您套用 4 月的更新星期二 (或 "B") 發行時，它會從執行 Windows 10 RS4 至 20H1 的裝置移除舊版 Microsoft Edge，並以 Microsoft Edge 取代。</span><span class="sxs-lookup"><span data-stu-id="f53cb-106">When you apply the Update Tuesday (or "B") release in April, it will remove Microsoft Edge Legacy from devices running Windows 10 RS4 through 20H1 and replace it with Microsoft Edge.</span></span>

## <span data-ttu-id="f53cb-107">如何準備</span><span class="sxs-lookup"><span data-stu-id="f53cb-107">How to Prepare</span></span>

<span data-ttu-id="f53cb-108">若要對透過 4 月的更新星期二發行在 Windows 10 RS4 到 20H1 裝置上安裝 Microsoft Edge 進行準備，建議您閱讀[規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="f53cb-108">To prepare for Microsoft Edge being installed on Windows 10 RS4 through 20H1 devices with the Update Tuesday release in April, we recommend reading [Plan your deployment of Microsoft Edge](deploy-edge-plan-deployment.md).</span></span>

<span data-ttu-id="f53cb-109">規劃部署之後，請使用下列其中一種方法來準備部署 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="f53cb-109">After you plan your deployment, use one of the following approaches to prepare to deploy Microsoft Edge.</span></span>

- <span data-ttu-id="f53cb-110">**安裝群組原則，以自訂您的 Microsoft Edge 更新方法**。</span><span class="sxs-lookup"><span data-stu-id="f53cb-110">**Install group policies to customize your Microsoft Edge update approach**.</span></span> <span data-ttu-id="f53cb-111">如需詳細資訊，請參閱[在 Windows 上設定 Microsoft Edge 原則設定](configure-microsoft-edge.md)，並特別注意[更新原則參考](microsoft-edge-update-policies.md)資料。</span><span class="sxs-lookup"><span data-stu-id="f53cb-111">For more information, see [Configure Microsoft Edge policy settings on Windows](configure-microsoft-edge.md), and pay special attention to the [Update Policy reference](microsoft-edge-update-policies.md) material.</span></span> <span data-ttu-id="f53cb-112">如果您在安裝 4 月的更新星期二發行之前安裝群組原則來管理您的更新，Microsoft Edge 就會立即開始採用您的原則。</span><span class="sxs-lookup"><span data-stu-id="f53cb-112">If you install group policies to manage your updates before installing April’s Update Tuesday release, Microsoft Edge will immediately start respecting your policy.</span></span> <span data-ttu-id="f53cb-113">如果未安裝任何群組原則，Microsoft Edge 會自動自行更新。</span><span class="sxs-lookup"><span data-stu-id="f53cb-113">If there isn't any installed group policy, Microsoft Edge will automatically update itself.</span></span>

- <span data-ttu-id="f53cb-114">**在舊版 Microsoft Edge 桌面應用程式終止服務日期 2021 年 3 月 9日之前將其移除，並部署 Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="f53cb-114">**Remove the Microsoft Edge Legacy desktop application before its end of service date of March 9, 2021 and deploy Microsoft Edge**.</span></span> <span data-ttu-id="f53cb-115">若為 Windows 10 RS4 到 20H1，您可以使用 Windows Update 來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="f53cb-115">For Windows 10 RS4 through 20H1, you can do this by using Windows Updates.</span></span> <span data-ttu-id="f53cb-116">如需詳細資訊，請參閱[使用 Windows 10 更新部署 Microsoft Edge](deploy-edge-with-windows-10-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="f53cb-116">For more information, see [Deploy Microsoft Edge with Windows 10 updates](deploy-edge-with-windows-10-updates.md).</span></span>

## <span data-ttu-id="f53cb-117">請參閱</span><span class="sxs-lookup"><span data-stu-id="f53cb-117">See also</span></span>

- [<span data-ttu-id="f53cb-118">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f53cb-118">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f53cb-119">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="f53cb-119">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)