---
title: 設定和疑難排解 Microsoft Edge 同步處理
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定和疑難排解 Microsoft Edge 同步處理
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297451"
---
# <span data-ttu-id="2c4b8-103">設定和疑難排解 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="2c4b8-103">Configure and troubleshoot Microsoft Edge sync</span></span>

<span data-ttu-id="2c4b8-104">本文介紹如何設定和使用 Microsoft Edge 在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-104">This article explains how to configure and use Microsoft Edge to sync your favorites, passwords, and other browser data across all your signed-in devices.</span></span> <span data-ttu-id="2c4b8-105">本文還為最常見的同步問題提供了疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-105">This article also provides troubleshooting steps for the most commonly encountered sync issues.</span></span> <span data-ttu-id="2c4b8-106">它還包含用於收集疑難排解所需記錄的建議使用工具。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-106">It also includes the recommended tools for gathering the logs needed for troubleshooting.</span></span>

> [!NOTE]
> <span data-ttu-id="2c4b8-107">除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-107">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <span data-ttu-id="2c4b8-108">概觀</span><span class="sxs-lookup"><span data-stu-id="2c4b8-108">Overview</span></span>

<span data-ttu-id="2c4b8-109">Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-109">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="2c4b8-110">同步支援的資料包括：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-110">The data supported by sync includes:</span></span>

- <span data-ttu-id="2c4b8-111">我的最愛</span><span class="sxs-lookup"><span data-stu-id="2c4b8-111">Favorites</span></span>
- <span data-ttu-id="2c4b8-112">密碼</span><span class="sxs-lookup"><span data-stu-id="2c4b8-112">Passwords</span></span>
- <span data-ttu-id="2c4b8-113">地址等 (表單填滿)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-113">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="2c4b8-114">集合</span><span class="sxs-lookup"><span data-stu-id="2c4b8-114">Collections</span></span>
- <span data-ttu-id="2c4b8-115">設定</span><span class="sxs-lookup"><span data-stu-id="2c4b8-115">Settings</span></span>
- <span data-ttu-id="2c4b8-116">擴充功能</span><span class="sxs-lookup"><span data-stu-id="2c4b8-116">Extension</span></span>
- <span data-ttu-id="2c4b8-117">[開啟] 所引標籤 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-117">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="2c4b8-118">歷程記錄 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-118">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="2c4b8-119">同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-119">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span>

> [!NOTE]
> <span data-ttu-id="2c4b8-120">將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-120">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <span data-ttu-id="2c4b8-121">必要條件</span><span class="sxs-lookup"><span data-stu-id="2c4b8-121">Prerequisites</span></span>

<span data-ttu-id="2c4b8-122">Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-122">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="2c4b8-123">Azure AD 進階版 (P1 或 P2) </span><span class="sxs-lookup"><span data-stu-id="2c4b8-123">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="2c4b8-124">M365 商務進階版</span><span class="sxs-lookup"><span data-stu-id="2c4b8-124">M365 Business Premium</span></span>
- <span data-ttu-id="2c4b8-125">Office 365 E1 及以上版本</span><span class="sxs-lookup"><span data-stu-id="2c4b8-125">Office 365 E1 and above</span></span>
- <span data-ttu-id="2c4b8-126">Azure 資訊保護 (AIP)(P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-126">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="2c4b8-127">所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-127">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <span data-ttu-id="2c4b8-128">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="2c4b8-128">Sync group policies</span></span>

<span data-ttu-id="2c4b8-129">您可以使用以下群組原則來設定和管理 Microsoft Edge 同步處理：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-129">You can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="2c4b8-130">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-130">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="2c4b8-131">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-131">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="2c4b8-132">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-132">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="2c4b8-133">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中排除的類型清單。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-133">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="2c4b8-134">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-134">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="2c4b8-135">如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-135">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="2c4b8-136">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync)：依預設開啟同步處理，且不需要使用者同意同步處理。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-136">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <span data-ttu-id="2c4b8-137">設定 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="2c4b8-137">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="2c4b8-138">Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-138">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="2c4b8-139">當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-139">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="2c4b8-140">有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-140">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="2c4b8-141">若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) 。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-141">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="2c4b8-142">如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true) PowerShell Cmdlet 來啟用 IPCv3Service。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-142">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="2c4b8-143">啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-143">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="2c4b8-144">此外，任何用來限制 Microsoft Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-144">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <span data-ttu-id="2c4b8-145">Microsoft Edge 和企業狀態漫遊 (ESR)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-145">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="2c4b8-146">Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-146">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longaer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="2c4b8-147">但是，Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-147">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="2c4b8-148">有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-148">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <span data-ttu-id="2c4b8-149">疑難排解同步處理問題</span><span class="sxs-lookup"><span data-stu-id="2c4b8-149">Troubleshoot sync issues</span></span>

<span data-ttu-id="2c4b8-150">本章節為最常出現的同步問題提供了疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-150">This section provides troubleshooting steps for the most encountered sync issues.</span></span> <span data-ttu-id="2c4b8-151">它還包含用於收集疑難排解所需記錄的建議使用工具。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-151">It also includes the recommended tools for gathering the logs needed for troubleshooting.</span></span>

### <span data-ttu-id="2c4b8-152">身分識別問題與同步處理問題</span><span class="sxs-lookup"><span data-stu-id="2c4b8-152">Identity issues versus sync issues</span></span>

<span data-ttu-id="2c4b8-153">在瀏覽器中維護使用者身分識別的常見使用案例就是支援同步處理。因此，身分識別問題通常會與同步處理問題混淆。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-153">A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues.</span></span> <span data-ttu-id="2c4b8-154">在開始疑難排解同步處理之前，請瞭解身分識別與同步處理問題之間的差異。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-154">Understand the difference between identity and sync issue before you start troubleshooting sync.</span></span>

<span data-ttu-id="2c4b8-155">在您將問題視為同步處理問題之前，請先檢查使用者是否已使用有效的帳戶登入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-155">Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.</span></span>

<span data-ttu-id="2c4b8-156">下一個螢幕擷取畫面顯示身分識別錯誤的範例。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-156">The next screenshot shows an example of an identity error.</span></span> <span data-ttu-id="2c4b8-157">錯誤為「**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**」，這可在 *edge://sync-internals* 的 **Credentials** 下找到：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-157">The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:</span></span>

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

### <span data-ttu-id="2c4b8-159">常見的同步問題</span><span class="sxs-lookup"><span data-stu-id="2c4b8-159">Common sync issues</span></span>

#### <span data-ttu-id="2c4b8-160">問題：無法存取 M365 或 Azure 資訊保護訂閱</span><span class="sxs-lookup"><span data-stu-id="2c4b8-160">Issue: Can't access M365 or Azure Information Protection subscription</span></span>

<span data-ttu-id="2c4b8-161">您是否有先前的 M365 或 Azure 資訊保護 (AIP) 訂閱已過期，然後以新訂閱將其取代？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-161">Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription?</span></span> <span data-ttu-id="2c4b8-162">如果是這樣，則租使用者識別碼已變更，且需要重設服務資料。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-162">If so, then the tenant ID has changed and the service data needs to be reset.</span></span> <span data-ttu-id="2c4b8-163">請參閱**密碼錯誤問題**中重置資料的說明。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-163">See the instructions for resetting data in the **Cryptographer error encountered** issue.</span></span>

#### <span data-ttu-id="2c4b8-164">問題：「此帳戶無法使用同步處理」。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-164">Issue: “Sync is not available for this account.”</span></span>

<span data-ttu-id="2c4b8-165">如果 Azure Active Directory 帳戶遇到此錯誤，或 DISABLED_BY_ADMIN 出現在 *edge://sync-internals*中，依次執行下一步驟中的步驟，直到問題得到解决。。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-165">If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="2c4b8-166">由於此錯誤的來源通常是需要在 Azure Active Directory 租用戶中變更設定，因此這些疑難排解步驟只能由租用戶系統管理員執行，而不能由使用者執行。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-166">Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.</span></span>

1. <span data-ttu-id="2c4b8-167">確認企業租使用者具有支援的 M365 訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-167">Verify that the enterprise tenant has a supported M365 subscription.</span></span> <span data-ttu-id="2c4b8-168">目前提供的可用訂閱類型清單 [如下](https://docs.microsoft.com/azure/information-protection/activate-office365)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-168">The current list of available subscription types is [provided here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span> <span data-ttu-id="2c4b8-169">如果租使用者沒有受支援的訂閱，他們可以單獨購買 Azure 資訊保護，或升級至其中一個支援的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-169">If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.</span></span>
2. <span data-ttu-id="2c4b8-170">如果支援的訂閱可用，請驗證租用戶是否具有可用的 Azure 資訊保護 (AIP)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-170">If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available.</span></span> <span data-ttu-id="2c4b8-171">有關檢查 AIP 狀態以及在必要時啟動 AIP 的說明，請參見[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-171">The instructions for checking the AIP status and, if necessary, activating AIP are [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>
3. <span data-ttu-id="2c4b8-172">如果步驟 2 顯示 AIP 處於使用中，但仍無法進行同步處理，請開啟企業狀態漫遊 (ESR)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-172">If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR).</span></span> <span data-ttu-id="2c4b8-173">啟用 ESR 的指示在 [這裡](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-173">The instructions for enabling ESR are [here](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span> <span data-ttu-id="2c4b8-174">請注意，ESR 不需要保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-174">Note that ESR does not need to stay on.</span></span> <span data-ttu-id="2c4b8-175">如果此步驟修正了問題，您可以關閉 ESR。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-175">You can turn off ESR if this step fixes the issue.</span></span>
4. <span data-ttu-id="2c4b8-176">確認 Azure 資訊保護未透過加入原則限定範圍。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-176">Confirm that Azure Information Protection is not scoped via an onboarding policy.</span></span> <span data-ttu-id="2c4b8-177">您可以使用 [AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell 小程式來查看是否啟用了範圍。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-177">You can use the [Get-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell applet to see if scoping is enabled.</span></span> <span data-ttu-id="2c4b8-178">接下來的兩個範例顯示了一個不限範圍的設定和一個範圍設定為特定安全性群組的設定。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-178">The next two examples show an unscoped configuration and a configuration scoped to a specific security group.</span></span>

   ```powershell
    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False 
   ```

   ```powershell

    PS C:\Work\scripts\PowerShell> Get-AadrmOnboardingControlPolicy
 
    UseRmsUserLicense SecurityGroupObjectId                Scope
    ----------------- ---------------------                -----
                False f1488a05-8196-40a6-9483-524948b90282   All
   ```


   <span data-ttu-id="2c4b8-179">如果已啟用範圍，則受影響的使用者應該新增至該範圍的安全性群組，或者應該移除該範圍。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-179">If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed.</span></span> <span data-ttu-id="2c4b8-180">在下方的範例中，上線已將 AIP 的範圍設定為指定的安全性群組，應使用 [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式移除該範圍。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-180">In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.</span></span>

5. <span data-ttu-id="2c4b8-181">確認 IPCv3Service 已在租用戶中開啟。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-181">Confirm that the IPCv3Service is turned on in the tenant.</span></span> <span data-ttu-id="2c4b8-182">[AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) PowerShell 小程式顯示服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-182">The [Get-AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="查看是否已啟用 IPCv3Service。":::

6. <span data-ttu-id="2c4b8-184">如果問題未修正，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-184">If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

#### <span data-ttu-id="2c4b8-185">問題：停滯在「正在設定同步處理...」或「無法連線到同步處理伺服器。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-185">Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server.</span></span> <span data-ttu-id="2c4b8-186">正在重試...」</span><span class="sxs-lookup"><span data-stu-id="2c4b8-186">Retrying…”</span></span>

1. <span data-ttu-id="2c4b8-187">請嘗試登出，然後再登入。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-187">Try to sign out and then sign in.</span></span>
2. <span data-ttu-id="2c4b8-188">移至 *edge://sync-internals*。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-188">Go to *edge://sync-internals*.</span></span> <span data-ttu-id="2c4b8-189">如果在「**輸入資訊**」區段下出現下列錯誤，請跳至下列問題， **發生密碼錯誤**。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-189">If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.</span></span>

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. <span data-ttu-id="2c4b8-190">請嘗試抓取伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-190">Try pinging the server endpoint.</span></span> <span data-ttu-id="2c4b8-191">用戶端的伺服器端點可在 *edge://sync-internals*中取得。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-191">The server endpoint for a client is available in *edge://sync-internals*.</span></span> <span data-ttu-id="2c4b8-192">下一個螢幕擷取畫面顯示 [**環境資訊**] 底部的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-192">The next screenshot shows endpoint information under **Environment Info**.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="端點資訊":::

4. <span data-ttu-id="2c4b8-194">如果伺服器端點為空白，或無法抓取伺服器並且環境中存在防火牆，請確認用戶端電腦可使用必要的服務端點。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-194">If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.</span></span>

   - <span data-ttu-id="2c4b8-195">Microsoft Edge 同步處理服務端點：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-195">Microsoft Edge sync service endpoints:</span></span>
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - <span data-ttu-id="2c4b8-196">Azure 資訊保護端點：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-196">Azure Information Protection endpoints:</span></span>
      - <span data-ttu-id="2c4b8-197">[https://api.aadrm.com](https://api.aadrm.com) (適用於多數租用戶)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-197">[https://api.aadrm.com](https://api.aadrm.com) (for most tenants)</span></span>
      - <span data-ttu-id="2c4b8-198">[https://api.aadrm.de](https://api.aadrm.de) (適用於德國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-198">[https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)</span></span>
      - <span data-ttu-id="2c4b8-199">[https://api.aadrm.cn](https://api.aadrm.cn) (適用於中國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="2c4b8-199">[https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)</span></span>
   - <span data-ttu-id="2c4b8-200">[Windows 通知服務端點](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-200">[Windows Notification Service endpoints](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span></span>

5. <span data-ttu-id="2c4b8-201">如果問題仍未解決，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-201">If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <span data-ttu-id="2c4b8-202">問題：發生密碼錯誤</span><span class="sxs-lookup"><span data-stu-id="2c4b8-202">Issue: Cryptographer error encountered</span></span>

<span data-ttu-id="2c4b8-203">此錯誤可在 *edge://sync-internals* 中的 **Type info** 下看到，並且可能表示需要重設使用者的服務端資料。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-203">This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset.</span></span> <span data-ttu-id="2c4b8-204">下列範例顯示密碼編譯錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="2c4b8-204">The following example shows a cryptography error message:</span></span>
<br><span data-ttu-id="2c4b8-205">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span><span class="sxs-lookup"><span data-stu-id="2c4b8-205">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span></span>

1. <span data-ttu-id="2c4b8-206">重新啟動 Microsoft Edge 並瀏覽至 *edge://sync-internals*，然後查看 "**AAD Account Key Status**" 區段</span><span class="sxs-lookup"><span data-stu-id="2c4b8-206">Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section</span></span>
   - <span data-ttu-id="2c4b8-207">"Success" in "Last MIP Result"：密碼錯誤意味著伺服器資料可能被遺失的金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-207">"Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key.</span></span> <span data-ttu-id="2c4b8-208">需要重設資料才能繼續同步處理。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-208">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="2c4b8-209">"No permissions" in "Last MIP Result"：這可能是由 Azure AD 變更或租用戶訂閱變更引起的。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-209">"No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes.</span></span> <span data-ttu-id="2c4b8-210">需要重設資料才能繼續同步處理。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-210">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="2c4b8-211">其他錯誤可能意味著伺服器設定問題。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-211">Other errors may mean server configuration issues.</span></span>
2. <span data-ttu-id="2c4b8-212">如果需要重設資料，請參閱 [重設雲端中的 Microsoft Edge 資料](edge-learnmore-reset-data-in-cloud.md)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-212">If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).</span></span>

#### <span data-ttu-id="2c4b8-213">問題：「您的系統管理員已關閉同步處理。」</span><span class="sxs-lookup"><span data-stu-id="2c4b8-213">Issue: “Sync has been turned off by your administrator.”</span></span>

<span data-ttu-id="2c4b8-214">請確定未設定 [SyncDisabled 原則](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-214">Make sure that the [SyncDisabled policy](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)  is not set.</span></span>

## <span data-ttu-id="2c4b8-215">常見問題集</span><span class="sxs-lookup"><span data-stu-id="2c4b8-215">Frequently Asked Questions</span></span>

### <span data-ttu-id="2c4b8-216">安全性和伺服器/資料合規性</span><span class="sxs-lookup"><span data-stu-id="2c4b8-216">SECURITY and SERVER/DATA COMPLIANCE</span></span>

#### <span data-ttu-id="2c4b8-217">已同步的資料是否已加密？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-217">Is the synced data encrypted?</span></span>

<span data-ttu-id="2c4b8-218">資料會在使用 TLS 1.2 或更高版本的傳輸中進行加密。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-218">The data is encrypted in transport using TLS 1.2 or greater.</span></span> <span data-ttu-id="2c4b8-219">在 Microsoft 服務中，所有資料類型都使用 AES128 進行了額外的加密。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-219">All data types are additionally encrypted at rest in Microsoft's service using AES128.</span></span> <span data-ttu-id="2c4b8-220">除了用於 [開啟] 索引標籤和 [歷程記錄同步處理] 外的所有資料類型，在離開使用者的裝置前都會透過 [Azure 資訊保護](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)原則管理的金鑰，另行加密。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-220">All data types except those used for open tab and history sync are additionally encrypted before leaving the user’s device with keys managed via the [Azure Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

#### <span data-ttu-id="2c4b8-221">為什麼[ 開啟] 索引標籤和 [歷程記錄資料] 沒有更多的用戶端加密？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-221">Why don’t open tab and history data have more client-side encryption?</span></span>

<span data-ttu-id="2c4b8-222">爲了減少使用者裝置上的資源使用率，歷程記錄資料是根據 [開啟] 索引標籤漫遊資料在伺服器端產生的。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-222">To reduce resource utilization on end-user devices, history data is generated server-side based on open tab roaming data.</span></span> <span data-ttu-id="2c4b8-223">此資料的用戶端加密無法進行此處理流程。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-223">This process would not be possible with client-side encryption of this data.</span></span> <span data-ttu-id="2c4b8-224">若要停用 [開啟] 索引標籤和 [歷程記錄同步]，請套用 [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) 或 [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) 原則。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-224">To disable open tab and history sync, apply the [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) or [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policies.</span></span>

#### <span data-ttu-id="2c4b8-225">租用戶系統管理員是否可以使用自己的金鑰？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-225">Can tenant admins bring their own key?</span></span>

<span data-ttu-id="2c4b8-226">是，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-226">Yes, through [Azure Information Protection](https://azure.microsoft.com/services/information-protection/).</span></span>

#### <span data-ttu-id="2c4b8-227">Microsoft Edge 同步資料儲存位置？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-227">Where is Microsoft Edge sync data stored?</span></span>

<span data-ttu-id="2c4b8-228">Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-228">Synced data for Azure AD accounts is stored in secure servers according to the tenant ID.</span></span> <span data-ttu-id="2c4b8-229">例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-229">For example, the data for a tenant that is registered in the United States is stored in servers geo-located for that region and uses the same storage solution as Office applications.</span></span>

#### <span data-ttu-id="2c4b8-230">除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-230">Does the data ever leave Microsoft's cloud, aside from syncing to Microsoft Edge?</span></span>

<span data-ttu-id="2c4b8-231">不。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-231">No.</span></span>

#### <span data-ttu-id="2c4b8-232">企業同步適用的服務條款為何？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-232">What terms of service does enterprise sync fall under?</span></span>

<span data-ttu-id="2c4b8-233">Microsoft Edge 同步處理的服務條款需遵守 Microsoft Edge 中的 Microsoft 軟體授權，可於  *edge://terms*中進行查看。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-233">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span> <span data-ttu-id="2c4b8-234">您的 Azure AD 訂閱與服務條款最終都需遵守 Microsoft 的 [線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-234">Your Azure AD subscription and terms of service ultimately fall under Microsoft's [Online Service Terms](https://www.microsoft.com/licensing/product-licensing/products).</span></span>

#### <span data-ttu-id="2c4b8-235">Microsoft Edge 是否支援政府社群雲端 (GCC) 高合規性？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-235">Does Microsoft Edge support Government Community Cloud (GCC) High compliance?</span></span>

<span data-ttu-id="2c4b8-236">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-236">Not today.</span></span> <span data-ttu-id="2c4b8-237">針對 GCC High 雲端的客戶，已停用 Microsoft Edge 同步處理功能。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-237">For customers in the GCC High cloud, Microsoft Edge sync is disabled.</span></span>

### <span data-ttu-id="2c4b8-238">套用同步處理</span><span class="sxs-lookup"><span data-stu-id="2c4b8-238">APPLYING SYNC</span></span>

#### <span data-ttu-id="2c4b8-239">為什麼並非所有 M365 訂閱都支援 Microsoft Edge 同步？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-239">Why isn’t Microsoft Edge sync supported in all M365 subscriptions?</span></span>

<span data-ttu-id="2c4b8-240">企業同步的方式取決於 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)，其並非可在所有 M365 訂閱中取得。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-240">Enterprise sync depends on [Azure Information Protection](https://azure.microsoft.com/services/information-protection/), which is not available in all M365 subscriptions.</span></span>

#### <span data-ttu-id="2c4b8-241">Microsoft Edge 同步是否基於企業狀態漫遊？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-241">Is Microsoft Edge sync based on Enterprise State Roaming?</span></span>

<span data-ttu-id="2c4b8-242">不。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-242">No.</span></span> <span data-ttu-id="2c4b8-243">ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-243">ESR can be used to enable sync, but Microsoft Edge sync is not a part of ESR.</span></span> <span data-ttu-id="2c4b8-244">如需詳細資訊，請參閱 [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) [Microsoft Edge 和企業狀態漫遊](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-244">For more information, see [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) and [Microsoft Edge and Enterprise State Roaming](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming).</span></span>

#### <span data-ttu-id="2c4b8-245">Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-245">Will Microsoft Edge ever support syncing between Microsoft Edge and IE?</span></span>

<span data-ttu-id="2c4b8-246">目前並未計劃支援此類同步。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-246">There are no plans to support this syncing.</span></span> <span data-ttu-id="2c4b8-247">如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-247">If you still need IE in your environment to support legacy apps, consider our [new IE mode](https://docs.microsoft.com/deployedge/edge-ie-mode).</span></span>

#### <span data-ttu-id="2c4b8-248">Microsoft Edge 會與舊版 Microsoft Edge 進行同步處理嗎？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-248">Will Microsoft Edge sync with Microsoft Edge Legacy?</span></span>

<span data-ttu-id="2c4b8-249">不，不會。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-249">No, it won't.</span></span> <span data-ttu-id="2c4b8-250">我們認為連結這兩個生態系統會導致 Microsoft Edge 同步可靠性受影響。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-250">We believe connecting these two ecosystems will lead to compromises in the reliability of sync in the Microsoft Edge.</span></span> <span data-ttu-id="2c4b8-251">我們將確保現有資料移轉至 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-251">We will ensure that existing data is migrated to the Microsoft Edge.</span></span> <span data-ttu-id="2c4b8-252">使用者還可以從自己選擇的瀏覽器中匯入資料，這也意味著 Microsoft Edge 將無法與 IE 同步。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-252">Users will also be able to import data from browser of their choice, which also means that Microsoft Edge won't have a way to sync with IE.</span></span>

### <span data-ttu-id="2c4b8-253">管理同步</span><span class="sxs-lookup"><span data-stu-id="2c4b8-253">MANAGING SYNC</span></span>

#### <span data-ttu-id="2c4b8-254">可以阻止我的使用者與個人租用戶進行同步嗎？</span><span class="sxs-lookup"><span data-stu-id="2c4b8-254">Is it possible to stop my users from syncing with a personal tenant?</span></span>

<span data-ttu-id="2c4b8-255">沒有直接的做法，但您可以使用 [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c4b8-255">Not directly, but you can determine which profiles can sign on to Microsoft Edge using the [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) policy.</span></span>

## <span data-ttu-id="2c4b8-256">請參閱</span><span class="sxs-lookup"><span data-stu-id="2c4b8-256">See also</span></span>

- [<span data-ttu-id="2c4b8-257">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="2c4b8-257">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="2c4b8-258">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="2c4b8-258">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="2c4b8-259">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="2c4b8-259">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
