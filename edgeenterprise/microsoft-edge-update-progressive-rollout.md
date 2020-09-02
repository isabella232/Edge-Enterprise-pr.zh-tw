---
title: 適用於 Microsoft Edge 穩定通道更新的漸進式套件推出
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 05/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 適用於 Microsoft Edge 穩定通道更新的漸進式套件推出
ms.openlocfilehash: 5b0d2f58318b10538d0470b644d346b5b9b9489b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979550"
---
# <span data-ttu-id="73638-103">適用於 Microsoft Edge 穩定通道更新的漸進式套件推出</span><span class="sxs-lookup"><span data-stu-id="73638-103">Progressive rollouts for Microsoft Edge Stable channel updates</span></span>

<span data-ttu-id="73638-104">從 Microsoft Edge 83 版本開始，我們將在幾天內逐步推出 Microsoft Edge 穩定通道的重大更新。</span><span class="sxs-lookup"><span data-stu-id="73638-104">Starting with Microsoft Edge 83 release, we will perform gradual rollouts of major updates to Microsoft Edge Stable channel over the span of a few days.</span></span> <span data-ttu-id="73638-105">這可讓我們監視更新，並安全地更新整個組織的瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="73638-105">This progressive rollout allows us to monitor upgrades and safely update the browser across the organization.</span></span>

> [!NOTE]
> <span data-ttu-id="73638-106">本文適用於 Microsoft Edge 穩定通道 83 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="73638-106">This applies to Microsoft Edge Stable channel version 83 or later.</span></span>

## <span data-ttu-id="73638-107">為什麼我們需要漸進式推出？</span><span class="sxs-lookup"><span data-stu-id="73638-107">Why do we need progressive rollout?</span></span>

<span data-ttu-id="73638-108">透過密切監視更新的運行狀況並在幾天內發行更新，我們可以限制新更新可能造成的問題的影響。</span><span class="sxs-lookup"><span data-stu-id="73638-108">By monitoring the health of our updates closely and rolling out the updates over the course of several days, we can limit the impact of issues that might occur with the new update.</span></span> <span data-ttu-id="73638-109">在 Microsoft Edge 版本 83 中，系統會為所有 Windows 7、Windows 8 & 8.1 和 Windows 10 版 Microsoft Edge 啟用漸進式部署。</span><span class="sxs-lookup"><span data-stu-id="73638-109">With Microsoft Edge release 83, Progressive Rollouts will be enabled for all Windows 7, Windows 8 & 8.1, and Windows 10 versions of Microsoft Edge.</span></span> <span data-ttu-id="73638-110">我們將儘快支援 Mac 上的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="73638-110">We will support Microsoft Edge on Mac as soon as it is ready.</span></span>

## <span data-ttu-id="73638-111">更新將如何運作？</span><span class="sxs-lookup"><span data-stu-id="73638-111">How will the updates work?</span></span>

<span data-ttu-id="73638-112">每次安裝 Microsoft Edge 時都會指派一個升級值。</span><span class="sxs-lookup"><span data-stu-id="73638-112">Each installation of Microsoft Edge is assigned an upgrade value.</span></span> <span data-ttu-id="73638-113">當我們開始漸進推出時，當裝置上的值在升級值範圍內時，您將看到更新。</span><span class="sxs-lookup"><span data-stu-id="73638-113">When we start rolling out incrementally, you'll see the update when the value on your device falls within the upgrade value range.</span></span> <span data-ttu-id="73638-114">隨著推出的進行 (幾天內)，所有使用者最終都會獲得更新。</span><span class="sxs-lookup"><span data-stu-id="73638-114">As the rollout progresses (within a few days), all users will eventually get the update.</span></span> <span data-ttu-id="73638-115">與沒有重大安全性修正的更新相比，具有重大安全性修復的瀏覽器更新的推出節奏更快。</span><span class="sxs-lookup"><span data-stu-id="73638-115">Browser updates with critical security fixes will have a faster rollout cadence than updates that don't have critical security fixes.</span></span> <span data-ttu-id="73638-116">這么做是為了確保對漏洞的及時提示。</span><span class="sxs-lookup"><span data-stu-id="73638-116">This is done to ensure prompt protection from vulnerabilities.</span></span>

## <span data-ttu-id="73638-117">這對企業有何影響？</span><span class="sxs-lookup"><span data-stu-id="73638-117">How does this affect enterprises?</span></span>

<span data-ttu-id="73638-118">Microsoft Edge 構建使用多種機制，如 Microsoft Intune、Windows Server Update Service (WSUS) 和設定管理員來散發到企業。</span><span class="sxs-lookup"><span data-stu-id="73638-118">Microsoft Edge artifacts are distributed to enterprises using multiple mechanisms such as Microsoft Intune, Windows Server Update Service (WSUS), and Configuration Manager.</span></span> <span data-ttu-id="73638-119">這些部署工具與漸進式推出的運作不同：</span><span class="sxs-lookup"><span data-stu-id="73638-119">These deployment tools behave differently with respect to Progressive Rollout:</span></span>

- <span data-ttu-id="73638-120">透過 Microsoft Intune 管理散發的企業會註冊為自動更新。</span><span class="sxs-lookup"><span data-stu-id="73638-120">Enterprises that manage distribution via Microsoft Intune are registered for auto-updates.</span></span> <span data-ttu-id="73638-121">使用漸進式推出，所有使用者將在幾天內看到更新。</span><span class="sxs-lookup"><span data-stu-id="73638-121">Progressive Rollout is used, and all the users will see an update in a few days.</span></span>
- <span data-ttu-id="73638-122">透過 WSUS (Windows Server Update Services) 或 設定管理員管理散發的企業不會註冊自動更新。</span><span class="sxs-lookup"><span data-stu-id="73638-122">Enterprises that manage distribution through WSUS (Windows Server Update Services) or Configuration Manager are not registered for auto-updates.</span></span> <span data-ttu-id="73638-123">管理員管理並套用從開始就可用的更新。</span><span class="sxs-lookup"><span data-stu-id="73638-123">Administrators manage and apply the updates that will be available from the start.</span></span> <span data-ttu-id="73638-124">漸進式部署不會影響這個程式。</span><span class="sxs-lookup"><span data-stu-id="73638-124">Progressive Rollout does not affect this process.</span></span>

<span data-ttu-id="73638-125">如有任何顧慮或問題，請透過使用者意見、應用程序內的意見反應按鈕或下方的註解來分享您的寶貴意見。</span><span class="sxs-lookup"><span data-stu-id="73638-125">Please share your valuable feedback through user voice, the in-application feedback button, or below in the comments if you have any concerns or questions.</span></span>

## <span data-ttu-id="73638-126">請參閱</span><span class="sxs-lookup"><span data-stu-id="73638-126">See also</span></span>

- [<span data-ttu-id="73638-127">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="73638-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
