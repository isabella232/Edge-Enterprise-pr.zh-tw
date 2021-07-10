---
title: 設定 Microsoft Edge 企業同步
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 管理員和使用者選項，用於使 Microsoft Edge 同步處理我的最愛、密碼和其他瀏覽器資料。
ms.openlocfilehash: 5e3813664d3942e84d38e4ae1b4fd17e41049cda
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642819"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a><span data-ttu-id="1d40b-103">設定 Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="1d40b-103">Configure Microsoft Edge enterprise sync</span></span>

<span data-ttu-id="1d40b-104">本文說明系統管理員如何設定 Microsoft Edge，在所有已登入的裝置上同步處理使用者的我的最愛、密碼和其他瀏覽器資料。如果您不是系統管理員，請瀏覽本文，了解如何跨裝置登入和同步 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="1d40b-104">This article explains how admins can configure Microsoft Edge to sync user favorites, passwords, and other browser data across all signed-in devices.If you are not an admin, please visit this article for how to sign-in and sync Microsoft Edge across devices.</span></span> <span data-ttu-id="1d40b-105">[登入以跨裝置同步 Microsoft Edge](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674)。</span><span class="sxs-lookup"><span data-stu-id="1d40b-105">[Sign in to sync Microsoft Edge across devices](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674).</span></span>

> [!NOTE]
> <span data-ttu-id="1d40b-106">除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1d40b-106">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="overview"></a><span data-ttu-id="1d40b-107">概觀</span><span class="sxs-lookup"><span data-stu-id="1d40b-107">Overview</span></span>

<span data-ttu-id="1d40b-108">Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。</span><span class="sxs-lookup"><span data-stu-id="1d40b-108">Microsoft Edge sync enables users to access their browsing data across all their signed-in devices.</span></span> <span data-ttu-id="1d40b-109">同步支援的資料包括：</span><span class="sxs-lookup"><span data-stu-id="1d40b-109">The data supported by sync includes:</span></span>

- <span data-ttu-id="1d40b-110">我的最愛</span><span class="sxs-lookup"><span data-stu-id="1d40b-110">Favorites</span></span>
- <span data-ttu-id="1d40b-111">密碼</span><span class="sxs-lookup"><span data-stu-id="1d40b-111">Passwords</span></span>
- <span data-ttu-id="1d40b-112">地址等 (表單填滿)</span><span class="sxs-lookup"><span data-stu-id="1d40b-112">Addresses and more (form-fill)</span></span>
- <span data-ttu-id="1d40b-113">集合</span><span class="sxs-lookup"><span data-stu-id="1d40b-113">Collections</span></span>
- <span data-ttu-id="1d40b-114">設定</span><span class="sxs-lookup"><span data-stu-id="1d40b-114">Settings</span></span>
- <span data-ttu-id="1d40b-115">擴充功能</span><span class="sxs-lookup"><span data-stu-id="1d40b-115">Extension</span></span>
- <span data-ttu-id="1d40b-116">[開啟] 所引標籤 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="1d40b-116">Open tabs (available in Microsoft Edge version 88)</span></span>
- <span data-ttu-id="1d40b-117">歷程記錄 (適用於 Microsoft Edge 版本88)</span><span class="sxs-lookup"><span data-stu-id="1d40b-117">History (available in Microsoft Edge version 88)</span></span>

<span data-ttu-id="1d40b-118">同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。</span><span class="sxs-lookup"><span data-stu-id="1d40b-118">Sync functionality is enabled via user consent and users can turn sync on or off for each of the data types listed above.</span></span> <span data-ttu-id="1d40b-119">如果使用者遇到同步處理問題，他們可能需要在 **設定** > **設定檔** > **重設同步處理**中重設同步處理。</span><span class="sxs-lookup"><span data-stu-id="1d40b-119">If a user is experiencing a sync issue they might need to reset sync in **Settings** > **Profiles** > **Reset sync**.</span></span>

> [!NOTE]
> <span data-ttu-id="1d40b-120">將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。</span><span class="sxs-lookup"><span data-stu-id="1d40b-120">Additional device connectivity and configuration data (such as device name, make and model) is uploaded to support sync functionality.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1d40b-121">必要條件</span><span class="sxs-lookup"><span data-stu-id="1d40b-121">Prerequisites</span></span>

<span data-ttu-id="1d40b-122">Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：</span><span class="sxs-lookup"><span data-stu-id="1d40b-122">Microsoft Edge sync for Azure Active Directory (Azure AD) accounts is available for any of the following subscriptions:</span></span>

- <span data-ttu-id="1d40b-123">Azure AD 進階版 (P1 或 P2) </span><span class="sxs-lookup"><span data-stu-id="1d40b-123">Azure AD Premium (P1 or P2)</span></span>
- <span data-ttu-id="1d40b-124">M365 商務進階版</span><span class="sxs-lookup"><span data-stu-id="1d40b-124">M365 Business Premium</span></span>
- <span data-ttu-id="1d40b-125">Office 365 E1 及以上版本</span><span class="sxs-lookup"><span data-stu-id="1d40b-125">Office 365 E1 and above</span></span>
- <span data-ttu-id="1d40b-126">Azure 資訊保護 (AIP)(P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="1d40b-126">Azure Information Protection (AIP) (P1 or P2)</span></span>
- <span data-ttu-id="1d40b-127">所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)</span><span class="sxs-lookup"><span data-stu-id="1d40b-127">All EDU subscriptions (Microsoft Apps for Students or Faculty, Exchange Online for Students or Faculty, O365 A1 or above, M365 A1 or above, or Azure Information Protection P1 or P2 for Students or Faculty)</span></span>

## <a name="sync-group-policies"></a><span data-ttu-id="1d40b-128">同步群組原則</span><span class="sxs-lookup"><span data-stu-id="1d40b-128">Sync group policies</span></span>

<span data-ttu-id="1d40b-129">系統管理員可以使用以下群組原則來設定和管理 Microsoft Edge 同步處理：</span><span class="sxs-lookup"><span data-stu-id="1d40b-129">Admins can use the following group policies to configure and manage Microsoft Edge sync:</span></span>

- <span data-ttu-id="1d40b-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled)：完全停用同步。</span><span class="sxs-lookup"><span data-stu-id="1d40b-130">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled): Disables sync completely.</span></span>
- <span data-ttu-id="1d40b-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。</span><span class="sxs-lookup"><span data-stu-id="1d40b-131">[SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled): Disables saving browsing history and sync. This policy also disables open-tabs sync.</span></span>
- <span data-ttu-id="1d40b-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。</span><span class="sxs-lookup"><span data-stu-id="1d40b-132">[AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory): When this policy is set to disabled, history sync will also be disabled.</span></span>
- <span data-ttu-id="1d40b-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)：設定要從同步中排除的類型清單。</span><span class="sxs-lookup"><span data-stu-id="1d40b-133">[SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled): Configure the list of types that are excluded from synchronization.</span></span>
- <span data-ttu-id="1d40b-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。</span><span class="sxs-lookup"><span data-stu-id="1d40b-134">[RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled): Allow Active Directory (AD) profiles to use on-premises storage.</span></span> <span data-ttu-id="1d40b-135">如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](./microsoft-edge-on-premises-sync.md)。</span><span class="sxs-lookup"><span data-stu-id="1d40b-135">For more information, see [On-premises sync for Active Directory (AD) users](./microsoft-edge-on-premises-sync.md).</span></span>
- <span data-ttu-id="1d40b-136">[ForceSync](/deployedge/microsoft-edge-policies#forcesync)：依預設開啟同步處理，且不需要使用者同意同步處理。</span><span class="sxs-lookup"><span data-stu-id="1d40b-136">[ForceSync](/deployedge/microsoft-edge-policies#forcesync): Turn on sync by default and do not require user consent to sync.</span></span>  

## <a name="configure-microsoft-edge-sync"></a><span data-ttu-id="1d40b-137">設定 Microsoft Edge 同步處理</span><span class="sxs-lookup"><span data-stu-id="1d40b-137">Configure Microsoft Edge sync</span></span>

<span data-ttu-id="1d40b-138">Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。</span><span class="sxs-lookup"><span data-stu-id="1d40b-138">Configuration options for Microsoft Edge sync are available through the Azure Information Protection (AIP) service.</span></span> <span data-ttu-id="1d40b-139">當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="1d40b-139">When AIP is enabled for a tenant, all users can sync Microsoft Edge data, regardless of licensing.</span></span> <span data-ttu-id="1d40b-140">有關如何解啟用 AIP 的指示，可以在[此處](/azure/information-protection/activate-office365)找到。</span><span class="sxs-lookup"><span data-stu-id="1d40b-140">Instructions on how to enable AIP can be found [here](/azure/information-protection/activate-office365).</span></span>

<span data-ttu-id="1d40b-141">若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) 。</span><span class="sxs-lookup"><span data-stu-id="1d40b-141">To restrict sync to certain set of users, you can enable the [AIP onboarding control policy](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) for those users.</span></span> <span data-ttu-id="1d40b-142">如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell Cmdlet 來啟用 IPCv3Service。</span><span class="sxs-lookup"><span data-stu-id="1d40b-142">If sync is still not available after ensuring that all necessary users are onboarded, ensure that the IPCv3Service is enabled using the [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps)  PowerShell cmdlet.</span></span>

> [!CAUTION]
> <span data-ttu-id="1d40b-143">啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。</span><span class="sxs-lookup"><span data-stu-id="1d40b-143">Activating Azure Information Protection will also allow other applications, such as Microsoft Word or Microsoft Outlook, to protect content with AIP.</span></span> <span data-ttu-id="1d40b-144">此外，任何用來限制 Microsoft Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。</span><span class="sxs-lookup"><span data-stu-id="1d40b-144">In addition, any onboarding control policy used to restrict Edge sync will also restrict other applications from protecting content using AIP.</span></span>

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a><span data-ttu-id="1d40b-145">Microsoft Edge 和企業狀態漫遊 (ESR)</span><span class="sxs-lookup"><span data-stu-id="1d40b-145">Microsoft Edge and Enterprise State Roaming (ESR)</span></span>

<span data-ttu-id="1d40b-146">Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。</span><span class="sxs-lookup"><span data-stu-id="1d40b-146">Microsoft Edge is a cross-platform application with an expanded scope for syncing user data across all their devices and is no longer a part of Azure AD Enterprise State Roaming.</span></span> <span data-ttu-id="1d40b-147">但是，Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。</span><span class="sxs-lookup"><span data-stu-id="1d40b-147">However, the Microsoft Edge will fulfill the data protection promises of ESR, such as the ability to bring your own key.</span></span> <span data-ttu-id="1d40b-148">有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。</span><span class="sxs-lookup"><span data-stu-id="1d40b-148">For more information, see [Microsoft Edge and Enterprise State Roaming](microsoft-edge-enterprise-state-roaming.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1d40b-149">也請參閱</span><span class="sxs-lookup"><span data-stu-id="1d40b-149">See also</span></span>

- [<span data-ttu-id="1d40b-150">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="1d40b-150">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="1d40b-151">診斷並修正 Microsoft Edge 同步處理問題</span><span class="sxs-lookup"><span data-stu-id="1d40b-151">Diagnose and fix Microsoft Edge sync issues</span></span>](microsoft-edge-troubleshoot-enterprise-sync.md)
- [<span data-ttu-id="1d40b-152">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="1d40b-152">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="1d40b-153">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="1d40b-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)