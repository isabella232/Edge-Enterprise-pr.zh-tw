---
title: Microsoft Edge 端點的允許清單
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 端點的允許清單
ms.openlocfilehash: 48a3a72e5af3744516e3b72d02b5254ad2e0504a
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133118"
---
# <span data-ttu-id="9adbe-103">Microsoft Edge 端點的允許清單</span><span class="sxs-lookup"><span data-stu-id="9adbe-103">Allow list for Microsoft Edge endpoints</span></span>

<span data-ttu-id="9adbe-104">Microsoft Edge 需要連線接到網際網路，以支援其功能。</span><span class="sxs-lookup"><span data-stu-id="9adbe-104">Microsoft Edge requires connectivity to the Internet to support its features.</span></span> <span data-ttu-id="9adbe-105">本文識別需要新增到允許清單中的網域 URL，以確保透過防火牆和其他安全機制進行通訊。</span><span class="sxs-lookup"><span data-stu-id="9adbe-105">This article identifies the domain URLs that you need to add to the Allow list to ensure communications through firewalls and other security mechanisms.</span></span>

> [!NOTE]
> <span data-ttu-id="9adbe-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9adbe-106">This applies  to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="9adbe-107">允許的網域 URL</span><span class="sxs-lookup"><span data-stu-id="9adbe-107">Domain URLs to allow</span></span>

<span data-ttu-id="9adbe-108">允許 Microsoft Edge 的以下網域 URL。</span><span class="sxs-lookup"><span data-stu-id="9adbe-108">Allow the following domain URLs for Microsoft Edge.</span></span>

### <span data-ttu-id="9adbe-109">更新服務</span><span class="sxs-lookup"><span data-stu-id="9adbe-109">Update Service</span></span>

<span data-ttu-id="9adbe-110">Microsoft Edge 用於檢查新更新的服務。</span><span class="sxs-lookup"><span data-stu-id="9adbe-110">The service that Microsoft Edge uses to check for new updates.</span></span>

- `https://msedge.api.cdp.microsoft.com`

### <span data-ttu-id="9adbe-111">實驗和設定服務</span><span class="sxs-lookup"><span data-stu-id="9adbe-111">Experimentation and Configuration service</span></span>

- `https://config.edge.skype.com`

### <span data-ttu-id="9adbe-112">Microsoft Edge 的下載位置</span><span class="sxs-lookup"><span data-stu-id="9adbe-112">Download locations for Microsoft Edge</span></span>

<span data-ttu-id="9adbe-113">可從初始安裝期間或更新可用時下載 Microsoft Edge 的位置。</span><span class="sxs-lookup"><span data-stu-id="9adbe-113">Locations Microsoft Edge can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="9adbe-114">下載位置由更新服務確定。</span><span class="sxs-lookup"><span data-stu-id="9adbe-114">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="9adbe-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="9adbe-115">HTTP</span></span>

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="9adbe-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9adbe-116">HTTPS</span></span>

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="9adbe-117">為了簡化下載位置的允許清單，可以使用萬用字元：</span><span class="sxs-lookup"><span data-stu-id="9adbe-117">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="9adbe-118">Microsoft Edge 延伸模組的下載位置</span><span class="sxs-lookup"><span data-stu-id="9adbe-118">Download locations for Microsoft Edge Extensions</span></span>

<span data-ttu-id="9adbe-119">可從初始安裝期間或更新可用時下載 Microsoft Edge 延伸模組的位置。</span><span class="sxs-lookup"><span data-stu-id="9adbe-119">Locations Microsoft Edge Extensions can be downloaded from during an initial install or when an update is available.</span></span> <span data-ttu-id="9adbe-120">下載位置由更新服務確定。</span><span class="sxs-lookup"><span data-stu-id="9adbe-120">The download location is determined by the Update Service.</span></span>

#### <span data-ttu-id="9adbe-121">HTTP</span><span class="sxs-lookup"><span data-stu-id="9adbe-121">HTTP</span></span>

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <span data-ttu-id="9adbe-122">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9adbe-122">HTTPS</span></span>

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > <span data-ttu-id="9adbe-123">為了簡化下載位置的允許清單，可以使用萬用字元：</span><span class="sxs-lookup"><span data-stu-id="9adbe-123">To simplify the allow list for download locations a wild card can be used:</span></span> `*.dl.delivery.mp.microsoft.com`

### <span data-ttu-id="9adbe-124">可選擇下載傳遞最佳化</span><span class="sxs-lookup"><span data-stu-id="9adbe-124">Optionally for Download Delivery Optimization</span></span>

<span data-ttu-id="9adbe-125">如需傳遞最佳化的詳細資訊，請參閱 [Windows 10 更新的傳遞最佳化](https://aka.ms/waas-do)。</span><span class="sxs-lookup"><span data-stu-id="9adbe-125">For information about delivery optimization, see [Delivery Optimization for Windows 10 updates](https://aka.ms/waas-do).</span></span>

- <span data-ttu-id="9adbe-126">用戶端至服務通訊：`*.do.dsp.mp.microsoft.com` (HTTP 連接埠 80，HTTPS 連接埠 443)</span><span class="sxs-lookup"><span data-stu-id="9adbe-126">Client to Service communication: `*.do.dsp.mp.microsoft.com` (HTTP Port 80, HTTPS Port 443)</span></span>
- <span data-ttu-id="9adbe-127">用戶端至用戶端通訊：應開啟 TCP 連接埠 7680 以供流量傳入</span><span class="sxs-lookup"><span data-stu-id="9adbe-127">Client to Client communication: TCP port 7680 should be open for inbound traffic</span></span>

### <span data-ttu-id="9adbe-128">Sync</span><span class="sxs-lookup"><span data-stu-id="9adbe-128">Sync</span></span>

<span data-ttu-id="9adbe-129">這些端點會管理所同步資料的讀取和寫入、用於護資料的版權管理，並在新的同步資料可用時通知瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="9adbe-129">These endpoints manage the reading and writing of synced data, rights management for secure data, and notifying the browser when new sync data is available.</span></span>

- <span data-ttu-id="9adbe-130">Edge 同步服務端點：</span><span class="sxs-lookup"><span data-stu-id="9adbe-130">Edge sync service endpoints:</span></span>

  - `https://enterprise.edge.activity.windows.com`
  - `https://edge.activity.windows.com`

- <span data-ttu-id="9adbe-131">Azure 資訊保護端點：</span><span class="sxs-lookup"><span data-stu-id="9adbe-131">Azure Information Protection endpoints:</span></span>

  - `https://api.aadrm.com` <span data-ttu-id="9adbe-132">(適用於多數租用戶)</span><span class="sxs-lookup"><span data-stu-id="9adbe-132">(for most tenants)</span></span>
  - `https://api.aadrm.de` <span data-ttu-id="9adbe-133">(適用於德國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="9adbe-133">(for tenants in Germany)</span></span>
  - `https://api.aadrm.cn` <span data-ttu-id="9adbe-134">(適用於中國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="9adbe-134">(for tenants in China)</span></span>

- [<span data-ttu-id="9adbe-135">Windows 通知服務端點</span><span class="sxs-lookup"><span data-stu-id="9adbe-135">Windows Notification Service endpoints</span></span>](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <span data-ttu-id="9adbe-136">其他瀏覽器支援服務</span><span class="sxs-lookup"><span data-stu-id="9adbe-136">Other browser support services</span></span>

<span data-ttu-id="9adbe-137">為瀏覽器功能 (如追蹤保護、憑證撤銷清單和其他瀏覽器元件更新) 提供中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9adbe-137">Provide metadata for browser features such as tracking protection, certificate revocation lists, and other browser component updates.</span></span> <span data-ttu-id="9adbe-138">提供可下載的拼字檢查字典和廣告封鎖的封鎖清單。</span><span class="sxs-lookup"><span data-stu-id="9adbe-138">Provide downloadable spellcheck dictionaries and ad-blocking block lists.</span></span> <span data-ttu-id="9adbe-139">提供服務以支援瀏覽器功能，如集合、自動填滿和延伸模組存放區。</span><span class="sxs-lookup"><span data-stu-id="9adbe-139">Provide services to support browser features such as collections, autofill, and extension store.</span></span>

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <span data-ttu-id="9adbe-140">請參閱</span><span class="sxs-lookup"><span data-stu-id="9adbe-140">See also</span></span>

- [<span data-ttu-id="9adbe-141">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9adbe-141">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9adbe-142">Microsoft Edge 文件登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9adbe-142">Microsoft Edge documentation landing page</span></span>](https://docs.microsoft.com/DeployEdge/)
- [<span data-ttu-id="9adbe-143">管理適用於 Windows 10 企業版版本 1903 的連線端點</span><span class="sxs-lookup"><span data-stu-id="9adbe-143">Manage connection endpoints for Windows 10 Enterprise, version 1903</span></span>](https://docs.microsoft.com/windows/privacy/manage-windows-1903-endpoints)
