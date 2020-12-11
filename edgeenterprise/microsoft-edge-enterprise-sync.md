---
title: Microsoft Edge 企業版同步處理
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 12/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 企業版同步處理
ms.openlocfilehash: 791188b5d28c867d6409a4d5373ea6c1ec7e49c7
ms.sourcegitcommit: 482b2e440a62cbf974dc45ac817f9d9d187ba1b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "11205462"
---
# <span data-ttu-id="85b90-103">Microsoft Edge 企業版同步處理</span><span class="sxs-lookup"><span data-stu-id="85b90-103">Microsoft Edge Enterprise Sync</span></span>

<span data-ttu-id="85b90-104">本文介紹如何使用 Microsoft Edge 在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。</span><span class="sxs-lookup"><span data-stu-id="85b90-104">This article explains how to use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="85b90-105">除非另有說明，否則本文適用于 Microsoft Edge 版本77或更新版本。</span><span class="sxs-lookup"><span data-stu-id="85b90-105">This article applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <span data-ttu-id="85b90-106">概觀</span><span class="sxs-lookup"><span data-stu-id="85b90-106">Overview</span></span>

<span data-ttu-id="85b90-107">Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="85b90-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="85b90-108">同步支援的資料包括：</span><span class="sxs-lookup"><span data-stu-id="85b90-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="85b90-109">我的最愛</span><span class="sxs-lookup"><span data-stu-id="85b90-109">Favorites</span></span>
- <span data-ttu-id="85b90-110">密碼</span><span class="sxs-lookup"><span data-stu-id="85b90-110">Passwords</span></span>
- <span data-ttu-id="85b90-111">地址等 (表單填滿)</span><span class="sxs-lookup"><span data-stu-id="85b90-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="85b90-112">集合</span><span class="sxs-lookup"><span data-stu-id="85b90-112">Collections</span></span>
- <span data-ttu-id="85b90-113">設定</span><span class="sxs-lookup"><span data-stu-id="85b90-113">Settings</span></span>
- <span data-ttu-id="85b90-114">擴充功能</span><span class="sxs-lookup"><span data-stu-id="85b90-114">Extension</span></span>
- <span data-ttu-id="85b90-115">[開啟] 所引標籤 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="85b90-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="85b90-116">歷程記錄 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="85b90-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="85b90-117">同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。</span><span class="sxs-lookup"><span data-stu-id="85b90-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="85b90-118">將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。</span><span class="sxs-lookup"><span data-stu-id="85b90-118">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="85b90-119">必要條件</span><span class="sxs-lookup"><span data-stu-id="85b90-119">Prerequisites</span></span>

<span data-ttu-id="85b90-120">Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：</span><span class="sxs-lookup"><span data-stu-id="85b90-120">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="85b90-121">Azure AD 進階版 (P1 或 P2) </span><span class="sxs-lookup"><span data-stu-id="85b90-121">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="85b90-122">M365 商務進階版</span><span class="sxs-lookup"><span data-stu-id="85b90-122">M365 Business Premium</span></span>
- <span data-ttu-id="85b90-123">Office 365 E1 及以上版本</span><span class="sxs-lookup"><span data-stu-id="85b90-123">Office 365 E1 and above</span></span>
- <span data-ttu-id="85b90-124">Azure 資訊保護 (AIP)(P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="85b90-124">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="85b90-125">所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="85b90-125">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="85b90-126">設定 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="85b90-126">Configuring Microsoft Edge sync</span></span>

<span data-ttu-id="85b90-127">Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。</span><span class="sxs-lookup"><span data-stu-id="85b90-127">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="85b90-128">當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="85b90-128">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="85b90-129">有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。</span><span class="sxs-lookup"><span data-stu-id="85b90-129">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="85b90-130">若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) 。</span><span class="sxs-lookup"><span data-stu-id="85b90-130">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="85b90-131">如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true) PowerShell Cmdlet 來啟用 IPCv3Service。</span><span class="sxs-lookup"><span data-stu-id="85b90-131">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="85b90-132">啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。</span><span class="sxs-lookup"><span data-stu-id="85b90-132">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="85b90-133">此外，任何用來限制 Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。</span><span class="sxs-lookup"><span data-stu-id="85b90-133">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="85b90-134">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="85b90-134">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="85b90-135">新 Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。</span><span class="sxs-lookup"><span data-stu-id="85b90-135">The new Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="85b90-136">但是，新的 Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。</span><span class="sxs-lookup"><span data-stu-id="85b90-136">However, the new Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="85b90-137">有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="85b90-137">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="85b90-138">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="85b90-138">Sync group policies</span></span>

<span data-ttu-id="85b90-139">以下群組原則影響 Microsoft Edge 同步：</span><span class="sxs-lookup"><span data-stu-id="85b90-139">The following group policies impact Microsoft Edge sync:</span></span>

- <span data-ttu-id="85b90-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。</span><span class="sxs-lookup"><span data-stu-id="85b90-140">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="85b90-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。</span><span class="sxs-lookup"><span data-stu-id="85b90-141">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="85b90-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。</span><span class="sxs-lookup"><span data-stu-id="85b90-142">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="85b90-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中排除的類型清單。</span><span class="sxs-lookup"><span data-stu-id="85b90-143">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="85b90-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。</span><span class="sxs-lookup"><span data-stu-id="85b90-144">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="85b90-145">如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync)。</span><span class="sxs-lookup"><span data-stu-id="85b90-145">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="85b90-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync)：預設會開啟同步處理，且不需要使用者同意即可同步處理。</span><span class="sxs-lookup"><span data-stu-id="85b90-146">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn sync on by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="85b90-147">常見問題集</span><span class="sxs-lookup"><span data-stu-id="85b90-147">Frequently Asked Questions</span></span>

### <span data-ttu-id="85b90-148">安全性和伺服器/資料合規性</span><span class="sxs-lookup"><span data-stu-id="85b90-148">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="85b90-149">已同步的資料是否已加密？</span><span class="sxs-lookup"><span data-stu-id="85b90-149">Is the synced data encrypted?</span></span>

<span data-ttu-id="85b90-150">資料會在使用 TLS 1.2 或更高版本的傳輸中進行加密。</span><span class="sxs-lookup"><span data-stu-id="85b90-150">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="85b90-151">在 Microsoft 的服務中，所有資料類型都會在其他地方使用 AES128 來進一步加密。</span><span class="sxs-lookup"><span data-stu-id="85b90-151">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="85b90-152">除了用於 [開啟] 索引標籤和 [歷程記錄同步處理] 外的所有資料類型，在離開使用者的裝置前都會透過 [Azure 資訊保護](https://docs.microsoft.com/azure/information-protection/)管理的金鑰，另行加密。</span><span class="sxs-lookup"><span data-stu-id="85b90-152">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via [Azure Information Protection](https://docs.microsoft.com/azure/information-protection/).</span></span>

#### <span data-ttu-id="85b90-153">為什麼開啟索引標籤和歷程記錄資料有額外的用戶端加密？</span><span class="sxs-lookup"><span data-stu-id="85b90-153">Why don’t open tab and history data have additional client-side encryption?</span></span>  

<span data-ttu-id="85b90-154">為了減少使用者裝置上的資源使用率，歷程記錄資料會根據 [開啟] 索引標籤漫遊資料，在伺服器端產生。</span><span class="sxs-lookup"><span data-stu-id="85b90-154">In order to reduce resource utilization on end user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="85b90-155">此資料的用戶端加密無法進行此處理流程。</span><span class="sxs-lookup"><span data-stu-id="85b90-155">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="85b90-156">若要停用 [開啟] 索引標籤和 [歷程記錄同步]，請套用 [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) 或 [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) 原則。</span><span class="sxs-lookup"><span data-stu-id="85b90-156">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

#### <span data-ttu-id="85b90-157">租用戶系統管理員是否可以使用自己的金鑰？</span><span class="sxs-lookup"><span data-stu-id="85b90-157">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="85b90-158">是，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。</span><span class="sxs-lookup"><span data-stu-id="85b90-158">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="85b90-159">Microsoft Edge 同步資料儲存位置？</span><span class="sxs-lookup"><span data-stu-id="85b90-159">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="85b90-160">Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。</span><span class="sxs-lookup"><span data-stu-id="85b90-160">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="85b90-161">例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。</span><span class="sxs-lookup"><span data-stu-id="85b90-161">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="85b90-162">除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？</span><span class="sxs-lookup"><span data-stu-id="85b90-162">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="85b90-163">不。</span><span class="sxs-lookup"><span data-stu-id="85b90-163">No.</span></span>

#### <span data-ttu-id="85b90-164">企業同步適用的服務條款為何？</span><span class="sxs-lookup"><span data-stu-id="85b90-164">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="85b90-165">Microsoft Edge 同步處理的服務條款需遵守 Microsoft Edge 中的 Microsoft 軟體授權，可於  *edge://terms*中進行查看。</span><span class="sxs-lookup"><span data-stu-id="85b90-165">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="85b90-166">您的 Azure AD 訂閱與服務條款最終都需遵守 Microsoft 的 [線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。</span><span class="sxs-lookup"><span data-stu-id="85b90-166">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="85b90-167">Microsoft Edge 是否支援政府社群雲端 (GCC) 高合規性？</span><span class="sxs-lookup"><span data-stu-id="85b90-167">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="85b90-168">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="85b90-168">Not today.</span></span> <span data-ttu-id="85b90-169">針對 GCC High 雲端的客戶，已停用 Microsoft Edge 同步處理功能。</span><span class="sxs-lookup"><span data-stu-id="85b90-169">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

### <span data-ttu-id="85b90-170">套用同步處理</span><span class="sxs-lookup"><span data-stu-id="85b90-170">APPLYING SYNC</span></span>

#### <span data-ttu-id="85b90-171">為什麼並非所有 M365 訂閱都支援 Microsoft Edge 同步處理？</span><span class="sxs-lookup"><span data-stu-id="85b90-171">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="85b90-172">企業同步處理的方式取決於 Azure 資訊保護 (並非所有 M365 訂閱都適用)。</span><span class="sxs-lookup"><span data-stu-id="85b90-172">Enterprise sync depends on Azure Information Protection, which is not available in all M365 subscriptions.</span></span>

#### <span data-ttu-id="85b90-173">Microsoft Edge 同步會根據企業狀態漫遊嗎？</span><span class="sxs-lookup"><span data-stu-id="85b90-173">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="85b90-174">不。</span><span class="sxs-lookup"><span data-stu-id="85b90-174">No.</span></span> <span data-ttu-id="85b90-175">ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。</span><span class="sxs-lookup"><span data-stu-id="85b90-175">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="85b90-176">如需詳細資訊，請參閱 [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="85b90-176">For more information, see [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) and [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

#### <span data-ttu-id="85b90-177">Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？</span><span class="sxs-lookup"><span data-stu-id="85b90-177">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="85b90-178">目前並未計劃支援此類同步。</span><span class="sxs-lookup"><span data-stu-id="85b90-178">There are no plans to support this syncing.</span></span> <span data-ttu-id="85b90-179">如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。</span><span class="sxs-lookup"><span data-stu-id="85b90-179">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="85b90-180">Microsoft Edge 會與舊版 Microsoft Edge 進行同步處理嗎？</span><span class="sxs-lookup"><span data-stu-id="85b90-180">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="85b90-181">不，不會。</span><span class="sxs-lookup"><span data-stu-id="85b90-181">No, it won't.</span></span> <span data-ttu-id="85b90-182">我們認為連結這兩個生態系統會導致 Microsoft Edge 同步可靠性受影響。</span><span class="sxs-lookup"><span data-stu-id="85b90-182">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="85b90-183">我們將確保現有的資料移轉至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="85b90-183">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="85b90-184">使用者還可以從自己選擇的瀏覽器匯入資料。</span><span class="sxs-lookup"><span data-stu-id="85b90-184">Users will also be able to import data from browser of their choice.</span></span> <span data-ttu-id="85b90-185">這也意味著新的 Microsoft Edge 瀏覽器將不能與 IE 同步。</span><span class="sxs-lookup"><span data-stu-id="85b90-185">This also means that new Microsoft Edge browser won't have a way to sync with IE.</span></span>

### <span data-ttu-id="85b90-186">管理同步</span><span class="sxs-lookup"><span data-stu-id="85b90-186">MANAGING SYNC</span></span>

#### <span data-ttu-id="85b90-187">可以阻止我的使用者與個人租用戶進行同步嗎？</span><span class="sxs-lookup"><span data-stu-id="85b90-187">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="85b90-188">沒有直接的做法，但您可以使用 [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="85b90-188">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="85b90-189">請參閱</span><span class="sxs-lookup"><span data-stu-id="85b90-189">See also</span></span>

- [<span data-ttu-id="85b90-190">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="85b90-190">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="85b90-191">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="85b90-191">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
