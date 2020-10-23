---
title: Microsoft Edge 企業版同步處理
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 10/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 企業版同步處理
ms.openlocfilehash: e51346d9bab83228c42a84a7a14ee45dc9b463a7
ms.sourcegitcommit: b32d8d64ae65dc5a46e47b7c34b0211097a0cc65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "11133128"
---
# <span data-ttu-id="f548d-103">Microsoft Edge 企業版同步處理</span><span class="sxs-lookup"><span data-stu-id="f548d-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="f548d-104">本文介紹如何使用 Microsoft Edge 在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。</span><span class="sxs-lookup"><span data-stu-id="f548d-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="f548d-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f548d-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="f548d-106">概觀</span><span class="sxs-lookup"><span data-stu-id="f548d-106">Overview</span></span>

<span data-ttu-id="f548d-107">Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="f548d-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="f548d-108">同步支援的資料包括：</span><span class="sxs-lookup"><span data-stu-id="f548d-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="f548d-109">我的最愛</span><span class="sxs-lookup"><span data-stu-id="f548d-109">Favorites</span></span>
- <span data-ttu-id="f548d-110">密碼</span><span class="sxs-lookup"><span data-stu-id="f548d-110">Passwords</span></span>
- <span data-ttu-id="f548d-111">地址等 (表單填滿)</span><span class="sxs-lookup"><span data-stu-id="f548d-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="f548d-112">集合</span><span class="sxs-lookup"><span data-stu-id="f548d-112">Collections</span></span>
- <span data-ttu-id="f548d-113">設定</span><span class="sxs-lookup"><span data-stu-id="f548d-113">Settings</span></span>

<span data-ttu-id="f548d-114">同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。</span><span class="sxs-lookup"><span data-stu-id="f548d-114">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="f548d-115">將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。</span><span class="sxs-lookup"><span data-stu-id="f548d-115">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="f548d-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="f548d-116">Prerequisites</span></span>

<span data-ttu-id="f548d-117">Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：</span><span class="sxs-lookup"><span data-stu-id="f548d-117">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="f548d-118">Azure AD Premium (P1 和 P2)</span><span class="sxs-lookup"><span data-stu-id="f548d-118">Azure AD Premium (P1 and P2)</span></span>
- <span data-ttu-id="f548d-119">M365 商務進階版</span><span class="sxs-lookup"><span data-stu-id="f548d-119">M365 Business Premium</span></span>
- <span data-ttu-id="f548d-120">Office 365 E1 及以上版本</span><span class="sxs-lookup"><span data-stu-id="f548d-120">Office 365 E1 and above</span></span>
- <span data-ttu-id="f548d-121">Azure 資訊保護 (AIP) (P1 和 P2)</span><span class="sxs-lookup"><span data-stu-id="f548d-121">Azure Information Protection (AIP) (P1& P2)</span></span>
- <span data-ttu-id="f548d-122">所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="f548d-122">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="f548d-123">設定 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="f548d-123">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="f548d-124">Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。</span><span class="sxs-lookup"><span data-stu-id="f548d-124">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="f548d-125">當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="f548d-125">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="f548d-126">有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。</span><span class="sxs-lookup"><span data-stu-id="f548d-126">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="f548d-127">若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) 。</span><span class="sxs-lookup"><span data-stu-id="f548d-127">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps) for those users.</span></span> <span data-ttu-id="f548d-128">如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps) PowerShell Cmdlet 來啟用 IPCv3Service。</span><span class="sxs-lookup"><span data-stu-id="f548d-128">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="f548d-129">啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。</span><span class="sxs-lookup"><span data-stu-id="f548d-129">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="f548d-130">此外，任何用來限制 Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。</span><span class="sxs-lookup"><span data-stu-id="f548d-130">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="f548d-131">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="f548d-131">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="f548d-132">新 Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。</span><span class="sxs-lookup"><span data-stu-id="f548d-132">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="f548d-133">但是，新的 Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。</span><span class="sxs-lookup"><span data-stu-id="f548d-133">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="f548d-134">有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="f548d-134">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="f548d-135">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="f548d-135">Sync group policies</span></span>

<span data-ttu-id="f548d-136">以下群組原則影響 Microsoft Edge 同步：</span><span class="sxs-lookup"><span data-stu-id="f548d-136">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="f548d-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。</span><span class="sxs-lookup"><span data-stu-id="f548d-137">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="f548d-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽歷程記錄和同步。此原則還會停用開啟索引標籤同步。</span><span class="sxs-lookup"><span data-stu-id="f548d-138">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="f548d-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中除的類型清單。</span><span class="sxs-lookup"><span data-stu-id="f548d-139">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="f548d-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。</span><span class="sxs-lookup"><span data-stu-id="f548d-140">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="f548d-141">如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync)。</span><span class="sxs-lookup"><span data-stu-id="f548d-141">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="f548d-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync)：預設會開啟同步處理，且不需要使用者同意即可同步處理。</span><span class="sxs-lookup"><span data-stu-id="f548d-142">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="f548d-143">常見問題集</span><span class="sxs-lookup"><span data-stu-id="f548d-143">Frequently Asked Questions</span></span>

### <span data-ttu-id="f548d-144">安全性和伺服器/資料合規性</span><span class="sxs-lookup"><span data-stu-id="f548d-144">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="f548d-145">已同步的資料是否已加密？</span><span class="sxs-lookup"><span data-stu-id="f548d-145">Is the synced data encrypted?</span></span> 

<span data-ttu-id="f548d-146">資料會在使用 TLS 1.2 或更高版本的傳輸中加密。</span><span class="sxs-lookup"><span data-stu-id="f548d-146">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="f548d-147">大部分的資料類型會使用 AES256 在 Microsoft 服務中進一步靜態加密。</span><span class="sxs-lookup"><span data-stu-id="f548d-147">Most data types are additionally encrypted at rest in Microsoft's service using AES256.</span></span> 

#### <span data-ttu-id="f548d-148">Microsoft Edge 同步資料儲存在哪裡？</span><span class="sxs-lookup"><span data-stu-id="f548d-148">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="f548d-149">Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。</span><span class="sxs-lookup"><span data-stu-id="f548d-149">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="f548d-150">例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。</span><span class="sxs-lookup"><span data-stu-id="f548d-150">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="f548d-151">除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？</span><span class="sxs-lookup"><span data-stu-id="f548d-151">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="f548d-152">不。</span><span class="sxs-lookup"><span data-stu-id="f548d-152">No.</span></span>

#### <span data-ttu-id="f548d-153">租用戶系統管理員是否可以使用自己的金鑰？</span><span class="sxs-lookup"><span data-stu-id="f548d-153">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="f548d-154">是的，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。</span><span class="sxs-lookup"><span data-stu-id="f548d-154">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="f548d-155">企業同步適用的服務條款為何？</span><span class="sxs-lookup"><span data-stu-id="f548d-155">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="f548d-156">服務條款與您的 Azure AD 訂閱相同。</span><span class="sxs-lookup"><span data-stu-id="f548d-156">The terms of service are the same terms as your Azure AD subscription.</span></span> <span data-ttu-id="f548d-157">所有 Azure AD 服務條款最終都需遵守 Microsoft 的[線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。</span><span class="sxs-lookup"><span data-stu-id="f548d-157">All the Azure AD terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="f548d-158">Microsoft Edge 是否支援政府社群雲端 (GCC) High 合規性？</span><span class="sxs-lookup"><span data-stu-id="f548d-158">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="f548d-159">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="f548d-159">Not today.</span></span> <span data-ttu-id="f548d-160">GCC High 是第 D 層，而 Microsoft Edge 最多支援第 C 層。</span><span class="sxs-lookup"><span data-stu-id="f548d-160">GCC High is Tier D, while Microsoft Edge supports up to Tier C.</span></span>

### <span data-ttu-id="f548d-161">套用同步</span><span class="sxs-lookup"><span data-stu-id="f548d-161">APPLYING SYNC</span></span>

#### <span data-ttu-id="f548d-162">決定留在舊版 Microsoft Edge 的企業和教育客戶會發生什麼情況？</span><span class="sxs-lookup"><span data-stu-id="f548d-162">What happens with enterprise and educational customers who decide to stay with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="f548d-163">目前版本的 Microsoft Edge 瀏覽器將繼續參與 ESR 方案。</span><span class="sxs-lookup"><span data-stu-id="f548d-163">The current version of Microsoft Edge browser will continue to participate in the ESR offering.</span></span>

#### <span data-ttu-id="f548d-164">為什麼我需要進階 Azure AD 訂閱，才能進行同步？</span><span class="sxs-lookup"><span data-stu-id="f548d-164">Why do I need a premium Azure AD subscription to sync?</span></span>

<span data-ttu-id="f548d-165">企業同步取決於 Azure 資訊保護，而這並未在所有 Azure AD 層中提供。</span><span class="sxs-lookup"><span data-stu-id="f548d-165">Enterprise sync depends on Azure Information Protection, which is not available in all Azure AD tiers.</span></span>

#### <span data-ttu-id="f548d-166">Microsoft Edge 同步會根據企業狀態漫遊嗎？</span><span class="sxs-lookup"><span data-stu-id="f548d-166">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="f548d-167">不。</span><span class="sxs-lookup"><span data-stu-id="f548d-167">No.</span></span> <span data-ttu-id="f548d-168">ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。</span><span class="sxs-lookup"><span data-stu-id="f548d-168">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="f548d-169">如需詳細資訊，請參閱 [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="f548d-169">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="f548d-170">Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？</span><span class="sxs-lookup"><span data-stu-id="f548d-170">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="f548d-171">目前並未計劃支援此類同步。</span><span class="sxs-lookup"><span data-stu-id="f548d-171">There are no plans to support this syncing.</span></span> <span data-ttu-id="f548d-172">如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。</span><span class="sxs-lookup"><span data-stu-id="f548d-172">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="f548d-173">新的 Microsoft Edge 瀏覽器將與舊版 Microsoft Edge 同步處理嗎？</span><span class="sxs-lookup"><span data-stu-id="f548d-173">Will the new Microsoft Edge browser sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="f548d-174">不，不會。</span><span class="sxs-lookup"><span data-stu-id="f548d-174">No, it won't.</span></span> <span data-ttu-id="f548d-175">我們相信，連接這兩個生態系統將導致新 Microsoft Edge 同步可靠性受影響。</span><span class="sxs-lookup"><span data-stu-id="f548d-175">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the new Microsoft Edge.</span></span> <span data-ttu-id="f548d-176">我們將確保將現有資料移轉到新的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="f548d-176">We will ensure that existing data is migrated to the new Microsoft Edge.</span></span> <span data-ttu-id="f548d-177">使用者還可以從自己選擇的瀏覽器匯入資料。</span><span class="sxs-lookup"><span data-stu-id="f548d-177">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="f548d-178">這也意味著新的 Microsoft Edge 瀏覽器將不能與 IE 同步。</span><span class="sxs-lookup"><span data-stu-id="f548d-178">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="f548d-179">管理同步</span><span class="sxs-lookup"><span data-stu-id="f548d-179">MANAGING SYNC</span></span>

#### <span data-ttu-id="f548d-180">可以阻止我的使用者與個人租用戶進行同步嗎？</span><span class="sxs-lookup"><span data-stu-id="f548d-180">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="f548d-181">沒有直接的做法，但您可以使用 [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f548d-181">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="f548d-182">請參閱</span><span class="sxs-lookup"><span data-stu-id="f548d-182">See also</span></span>

- [<span data-ttu-id="f548d-183">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f548d-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f548d-184">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="f548d-184">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
