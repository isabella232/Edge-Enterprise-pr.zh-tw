---
title: 設定 Microsoft Edge 企業同步
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 管理員和使用者選項，用於使 Microsoft Edge 同步處理我的最愛、密碼和其他瀏覽器資料。
ms.openlocfilehash: bfaa1db297093d0b0655a8d217aefcd59d11ac5e
ms.sourcegitcommit: 86e0de9b27ad4297a6d5a57c866d7ef4fc7bb0cd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "11400137"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="20f13-103">設定 Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="20f13-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="20f13-104">本文介紹系統管理員如何將 Microsoft Edge 設定為在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。</span><span class="sxs-lookup"><span data-stu-id="20f13-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.</span></span>

> [!NOTE]
> <span data-ttu-id="20f13-105">除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="20f13-105">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="20f13-106">概觀</span><span class="sxs-lookup"><span data-stu-id="20f13-106">Overview</span></span>

<span data-ttu-id="20f13-107">Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="20f13-107">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="20f13-108">同步支援的資料包括：</span><span class="sxs-lookup"><span data-stu-id="20f13-108">The data supported by sync includes:</span></span>

- <span data-ttu-id="20f13-109">我的最愛</span><span class="sxs-lookup"><span data-stu-id="20f13-109">Favorites</span></span>
- <span data-ttu-id="20f13-110">密碼</span><span class="sxs-lookup"><span data-stu-id="20f13-110">Passwords</span></span>
- <span data-ttu-id="20f13-111">地址等 (表單填滿)</span><span class="sxs-lookup"><span data-stu-id="20f13-111">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="20f13-112">集合</span><span class="sxs-lookup"><span data-stu-id="20f13-112">Collections</span></span>
- <span data-ttu-id="20f13-113">設定</span><span class="sxs-lookup"><span data-stu-id="20f13-113">Settings</span></span>
- <span data-ttu-id="20f13-114">擴充功能</span><span class="sxs-lookup"><span data-stu-id="20f13-114">Extension</span></span>
- <span data-ttu-id="20f13-115">[開啟] 所引標籤 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="20f13-115">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="20f13-116">歷程記錄 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="20f13-116">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="20f13-117">同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。</span><span class="sxs-lookup"><span data-stu-id="20f13-117">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="20f13-118">如果使用者遇到同步處理問題，他們可能需要在 **設定** > **設定檔** > **重設同步處理**中重設同步處理。</span><span class="sxs-lookup"><span data-stu-id="20f13-118">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="20f13-119">將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。</span><span class="sxs-lookup"><span data-stu-id="20f13-119">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="20f13-120">必要條件</span><span class="sxs-lookup"><span data-stu-id="20f13-120">Prerequisites</span></span>

<span data-ttu-id="20f13-121">Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：</span><span class="sxs-lookup"><span data-stu-id="20f13-121">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="20f13-122">Azure AD 進階版 (P1 或 P2) </span><span class="sxs-lookup"><span data-stu-id="20f13-122">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="20f13-123">M365 商務進階版</span><span class="sxs-lookup"><span data-stu-id="20f13-123">M365 Business Premium</span></span>
- <span data-ttu-id="20f13-124">Office 365 E1 及以上版本</span><span class="sxs-lookup"><span data-stu-id="20f13-124">Office 365 E1 and above</span></span>
- <span data-ttu-id="20f13-125">Azure 資訊保護 (AIP)(P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="20f13-125">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="20f13-126">所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="20f13-126">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="20f13-127">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="20f13-127">Sync group policies</span></span>

<span data-ttu-id="20f13-128">系統管理員可以使用以下群組原則來設定和管理 Microsoft Edge 同步處理：</span><span class="sxs-lookup"><span data-stu-id="20f13-128">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="20f13-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。</span><span class="sxs-lookup"><span data-stu-id="20f13-129">[SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="20f13-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。</span><span class="sxs-lookup"><span data-stu-id="20f13-130">[SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="20f13-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。</span><span class="sxs-lookup"><span data-stu-id="20f13-131">[AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="20f13-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中排除的類型清單。</span><span class="sxs-lookup"><span data-stu-id="20f13-132">[SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="20f13-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。</span><span class="sxs-lookup"><span data-stu-id="20f13-133">[RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="20f13-134">如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync)。</span><span class="sxs-lookup"><span data-stu-id="20f13-134">For more information, see [On-premises sync for Active Directory (AD) users](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync).</span></span>
- <span data-ttu-id="20f13-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync)：依預設開啟同步處理，且不需要使用者同意同步處理。</span><span class="sxs-lookup"><span data-stu-id="20f13-135">[ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="20f13-136">設定 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="20f13-136">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="20f13-137">Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。</span><span class="sxs-lookup"><span data-stu-id="20f13-137">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="20f13-138">當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="20f13-138">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="20f13-139">有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。</span><span class="sxs-lookup"><span data-stu-id="20f13-139">Instructions on how to enable AIP can be found [here](https://docs.microsoft.com/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="20f13-140">若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) 。</span><span class="sxs-lookup"><span data-stu-id="20f13-140">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) for those users.</span></span> <span data-ttu-id="20f13-141">如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true) PowerShell Cmdlet 來啟用 IPCv3Service。</span><span class="sxs-lookup"><span data-stu-id="20f13-141">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="20f13-142">啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。</span><span class="sxs-lookup"><span data-stu-id="20f13-142">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="20f13-143">此外，任何用來限制 Microsoft Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。</span><span class="sxs-lookup"><span data-stu-id="20f13-143">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="20f13-144">Microsoft Edge 和企業狀態漫遊 (ESR)</span><span class="sxs-lookup"><span data-stu-id="20f13-144">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="20f13-145">Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。</span><span class="sxs-lookup"><span data-stu-id="20f13-145">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="20f13-146">但是，Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。</span><span class="sxs-lookup"><span data-stu-id="20f13-146">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="20f13-147">有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="20f13-147">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="20f13-148">也請參閱</span><span class="sxs-lookup"><span data-stu-id="20f13-148">See also</span></span>

- [<span data-ttu-id="20f13-149">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="20f13-149">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="20f13-150">診斷並修正 Microsoft Edge 同步處理問題</span><span class="sxs-lookup"><span data-stu-id="20f13-150">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="20f13-151">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="20f13-151">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="20f13-152">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="20f13-152">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
