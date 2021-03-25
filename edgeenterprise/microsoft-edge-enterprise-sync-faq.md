---
title: Microsoft Edge 企業同步常見問題集
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 企業同步的常見問題集。
ms.openlocfilehash: e25ee985f65ee61dda5cacece73d43be7f1e6d7d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447867"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a><span data-ttu-id="0db9b-103">Microsoft Edge 企業同步常見問題集</span><span class="sxs-lookup"><span data-stu-id="0db9b-103">Microsoft Edge enterprise sync FAQ</span></span>

<span data-ttu-id="0db9b-104">本文回答有關 Microsoft Edge 版本 77 或更新版本的企業同步常見問題。</span><span class="sxs-lookup"><span data-stu-id="0db9b-104">This article answers frequently asked questions about enterprise sync for Microsoft Edge version 77 or later.</span></span>

## <a name="security-and-serverdata-compliance"></a><span data-ttu-id="0db9b-105">安全性和伺服器/資料合規性</span><span class="sxs-lookup"><span data-stu-id="0db9b-105">Security and Server/Data Compliance</span></span>

### <a name="is-the-synced-data-encrypted"></a><span data-ttu-id="0db9b-106">已同步的資料是否已加密？</span><span class="sxs-lookup"><span data-stu-id="0db9b-106">Is the synced data encrypted?</span></span>

<span data-ttu-id="0db9b-107">資料會在使用 TLS 1.2 或更高版本的傳輸中進行加密。</span><span class="sxs-lookup"><span data-stu-id="0db9b-107">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="0db9b-108">在 Microsoft 服務中，所有資料類型都使用 AES128 進行了額外的加密。</span><span class="sxs-lookup"><span data-stu-id="0db9b-108">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="0db9b-109">除了用於 [開啟] 索引標籤和 [歷程記錄同步處理] 外的所有資料類型，在離開使用者的裝置前都會透過 [Azure 資訊保護](./microsoft-edge-policies.md#restrictsignintopattern)原則管理的金鑰，另行加密。</span><span class="sxs-lookup"><span data-stu-id="0db9b-109">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a><span data-ttu-id="0db9b-110">為什麼[ 開啟] 索引標籤和 [歷程記錄資料] 沒有更多的用戶端加密？</span><span class="sxs-lookup"><span data-stu-id="0db9b-110">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="0db9b-111">爲了減少使用者裝置上的資源使用率，歷程記錄資料是根據 [開啟] 索引標籤漫遊資料在伺服器端產生的。</span><span class="sxs-lookup"><span data-stu-id="0db9b-111">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="0db9b-112">此資料的用戶端加密無法進行此處理流程。</span><span class="sxs-lookup"><span data-stu-id="0db9b-112">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="0db9b-113">若要停用 [開啟] 索引標籤和 [歷程記錄同步]，請套用 [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) 或 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 原則。</span><span class="sxs-lookup"><span data-stu-id="0db9b-113">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) or [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policies.</span></span>

### <a name="can-tenant-admins-bring-their-own-key"></a><span data-ttu-id="0db9b-114">租用戶系統管理員是否可以使用自己的金鑰？</span><span class="sxs-lookup"><span data-stu-id="0db9b-114">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="0db9b-115">是，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。</span><span class="sxs-lookup"><span data-stu-id="0db9b-115">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

### <a name="where-is-microsoft-edge-sync-data-stored"></a><span data-ttu-id="0db9b-116">Microsoft Edge 同步資料儲存位置？</span><span class="sxs-lookup"><span data-stu-id="0db9b-116">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="0db9b-117">Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。</span><span class="sxs-lookup"><span data-stu-id="0db9b-117">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="0db9b-118">例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。</span><span class="sxs-lookup"><span data-stu-id="0db9b-118">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a><span data-ttu-id="0db9b-119">除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？</span><span class="sxs-lookup"><span data-stu-id="0db9b-119">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="0db9b-120">不。</span><span class="sxs-lookup"><span data-stu-id="0db9b-120">No.</span></span>

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a><span data-ttu-id="0db9b-121">企業同步適用的服務條款為何？</span><span class="sxs-lookup"><span data-stu-id="0db9b-121">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="0db9b-122">Microsoft Edge 同步處理的服務條款需遵守 Microsoft Edge 中的 Microsoft 軟體授權，可於  *edge://terms*中進行查看。</span><span class="sxs-lookup"><span data-stu-id="0db9b-122">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="0db9b-123">您的 Azure AD 訂閱與服務條款最終都需遵守 Microsoft 的 [線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。</span><span class="sxs-lookup"><span data-stu-id="0db9b-123">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a><span data-ttu-id="0db9b-124">Microsoft Edge 是否支援政府社群雲端 (GCC) 高合規性？</span><span class="sxs-lookup"><span data-stu-id="0db9b-124">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="0db9b-125">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="0db9b-125">Not today.</span></span> <span data-ttu-id="0db9b-126">針對 GCC High 雲端的客戶，已停用 Microsoft Edge 同步處理功能。</span><span class="sxs-lookup"><span data-stu-id="0db9b-126">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

## <a name="applying-sync"></a><span data-ttu-id="0db9b-127">套用同步處理</span><span class="sxs-lookup"><span data-stu-id="0db9b-127">Applying Sync</span></span>

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a><span data-ttu-id="0db9b-128">為什麼並非所有 M365 訂閱都支援 Microsoft Edge 同步？</span><span class="sxs-lookup"><span data-stu-id="0db9b-128">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="0db9b-129">企業同步的方式取決於 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)，其並非可在所有 M365 訂閱中取得。</span><span class="sxs-lookup"><span data-stu-id="0db9b-129">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a><span data-ttu-id="0db9b-130">Microsoft Edge 同步是否基於企業狀態漫遊？</span><span class="sxs-lookup"><span data-stu-id="0db9b-130">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="0db9b-131">不。</span><span class="sxs-lookup"><span data-stu-id="0db9b-131">No.</span></span> <span data-ttu-id="0db9b-132">ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。</span><span class="sxs-lookup"><span data-stu-id="0db9b-132">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="0db9b-133">如需詳細資訊，請參閱 [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) [Microsoft Edge 和企業狀態漫遊](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming)。</span><span class="sxs-lookup"><span data-stu-id="0db9b-133">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a><span data-ttu-id="0db9b-134">Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？</span><span class="sxs-lookup"><span data-stu-id="0db9b-134">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="0db9b-135">目前並未計劃支援此類同步。</span><span class="sxs-lookup"><span data-stu-id="0db9b-135">There are no plans to support this syncing.</span></span> <span data-ttu-id="0db9b-136">如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](./edge-ie-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="0db9b-136">If you still need IE in your environment to support legacy apps, consider our [new IE mode](./edge-ie-mode.md).</span></span>

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a><span data-ttu-id="0db9b-137">Microsoft Edge 會與舊版 Microsoft Edge 進行同步處理嗎？</span><span class="sxs-lookup"><span data-stu-id="0db9b-137">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="0db9b-138">不，不會。</span><span class="sxs-lookup"><span data-stu-id="0db9b-138">No, it won't.</span></span> <span data-ttu-id="0db9b-139">我們認為連結這兩個生態系統會導致 Microsoft Edge 同步可靠性受影響。</span><span class="sxs-lookup"><span data-stu-id="0db9b-139">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="0db9b-140">我們將確保現有資料移轉至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="0db9b-140">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="0db9b-141">使用者還可以從自己選擇的瀏覽器中匯入資料，這也意味著 Microsoft Edge 將無法與 IE 同步。</span><span class="sxs-lookup"><span data-stu-id="0db9b-141">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

## <a name="managing-sync"></a><span data-ttu-id="0db9b-142">管理同步</span><span class="sxs-lookup"><span data-stu-id="0db9b-142">Managing Sync</span></span>

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a><span data-ttu-id="0db9b-143">可以阻止我的使用者與個人租用戶進行同步嗎？</span><span class="sxs-lookup"><span data-stu-id="0db9b-143">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="0db9b-144">沒有直接的做法，但您可以使用 [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="0db9b-144">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) policy.</span></span>

## <a name="see-also"></a><span data-ttu-id="0db9b-145">請參閱</span><span class="sxs-lookup"><span data-stu-id="0db9b-145">See also</span></span>

- [<span data-ttu-id="0db9b-146">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="0db9b-146">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="0db9b-147">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="0db9b-147">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="0db9b-148">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="0db9b-148">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)