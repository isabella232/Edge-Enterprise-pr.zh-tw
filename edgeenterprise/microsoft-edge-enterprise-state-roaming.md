---
title: Microsoft Edge 和企業狀態漫遊
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 02/14/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 和企業狀態漫遊
ms.openlocfilehash: 6090ecfda2f792d49e452771943bc6348066a3d8
ms.sourcegitcommit: 90b8eab62edbed0e0a84780abd7d3854bf95c130
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "11328055"
---
# <span data-ttu-id="465cd-103">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="465cd-103">Microsoft Edge and Enterprise State Roaming</span></span>

<span data-ttu-id="465cd-104">本文介紹 Microsoft Edge 參與企業狀態漫遊 (ESR) 方案的情況正在發生變化，以便更好地支援跨平台和裝置同步。</span><span class="sxs-lookup"><span data-stu-id="465cd-104">This article explains how Microsoft Edge participation in the Enterprise State Roaming (ESR) offering is changing to better support sync across platforms and devices.</span></span>

> [!NOTE]
> <span data-ttu-id="465cd-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="465cd-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="465cd-106">簡介</span><span class="sxs-lookup"><span data-stu-id="465cd-106">Introduction</span></span>

<span data-ttu-id="465cd-107">使用 Windows 10，[Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) 使用者能夠安全地將其使用者設定和應用程式設定資料同步處理至雲端。</span><span class="sxs-lookup"><span data-stu-id="465cd-107">With Windows 10, [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-whatis) users gained the ability to securely synchronize their user settings and application settings data to the cloud.</span></span> <span data-ttu-id="465cd-108">[企業狀態漫遊 (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) 提供使用者跨 Windows 裝置的一致體驗，並且減少設定新的裝置所需的時間。</span><span class="sxs-lookup"><span data-stu-id="465cd-108">[Enterprise State Roaming (ESR)](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) provides users with a unified experience across their Windows devices and reduces the time needed for configuring a new device.</span></span>

<span data-ttu-id="465cd-109">Microsoft Edge 採用 Chromium 平台，其同步解決方案現已與 Windows 同步架構斷開連接。</span><span class="sxs-lookup"><span data-stu-id="465cd-109">As part of Microsoft Edge adopting the Chromium platform, its sync solution is now disconnected from Windows sync framework.</span></span> <span data-ttu-id="465cd-110">這會影響 Microsoft Edge 與 ESR 方案之間的關係。</span><span class="sxs-lookup"><span data-stu-id="465cd-110">This affects the relationship of Microsoft Edge to the ESR offering.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="465cd-111">新的 Microsoft Edge 不參與 ESR 方案。</span><span class="sxs-lookup"><span data-stu-id="465cd-111">The new Microsoft Edge does not participate in the ESR offering.</span></span>

## <span data-ttu-id="465cd-112">Microsoft Edge 有什麼變化？</span><span class="sxs-lookup"><span data-stu-id="465cd-112">What’s changing with Microsoft Edge?</span></span>

<span data-ttu-id="465cd-113">使用新的 Microsoft Edge，同步解決方案不會繫結到 Windows 同步生態系統。</span><span class="sxs-lookup"><span data-stu-id="465cd-113">With the new Microsoft Edge, the sync solution isn’t tied to Windows sync ecosystem.</span></span> <span data-ttu-id="465cd-114">這使我們能夠跨所有平台 (如 Windows 7、Windows 8.1、iOS、Android 和 macOS) 提供 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="465cd-114">This enables us to offer Microsoft Edge across all the platforms, such as Windows 7, Windows 8.1, iOS, Android and macOS.</span></span> <span data-ttu-id="465cd-115">這也使我們能夠為 Windows 上的非主要帳戶提供同步。</span><span class="sxs-lookup"><span data-stu-id="465cd-115">This also enables us to offer sync for non-primary accounts on Windows.</span></span> <span data-ttu-id="465cd-116">此外，我們可以以比 Windows 更頻繁、更靈活的發行步調散發 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="465cd-116">In addition, we can ship Microsoft Edge at a more frequent and flexible release cadence than Windows.</span></span> <span data-ttu-id="465cd-117">(如需詳細資訊，請參閱[支援下一版 Microsoft Edge 的 Windows Update](microsoft-edge-sysupdate-windows-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="465cd-117">(For more information, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md).</span></span> <span data-ttu-id="465cd-118">所有這些因素都突顯，需要重新評估 Microsoft Edge 參與 ESR 方案。</span><span class="sxs-lookup"><span data-stu-id="465cd-118">All these factors highlighted the need to re-assess Microsoft Edge participation in the ESR offering.</span></span>

<span data-ttu-id="465cd-119">ESR 被界定為 Windows 產品，承諾如何處理來自 Windows 裝置的資料，但 Microsoft Edge 同步將超出 Windows 裝置的範圍。</span><span class="sxs-lookup"><span data-stu-id="465cd-119">ESR is framed as a Windows product offering with promises about how data from Windows devices is handled, but Microsoft Edge sync will extend beyond Windows devices.</span></span> <span data-ttu-id="465cd-120">而且，由於資料在這些裝置之間漫遊，因此很難在 ESR 脈絡中定義 Microsoft Edge 同步方案。</span><span class="sxs-lookup"><span data-stu-id="465cd-120">And, as the data roams across these devices, it makes it difficult to define the Microsoft Edge sync offering in the context of ESR.</span></span> <span data-ttu-id="465cd-121">為了簡化同步的工作方式和管理方式，並適應突顯的更改，我們決定從 ESR 方案中撤出 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="465cd-121">To simplify how sync works and is managed, and to accommodate the changes that are highlighted, a decision was made to pull Microsoft Edge out of the ESR offering.</span></span>

## <span data-ttu-id="465cd-122">這是否意味著企業將失去作為 ESR 一部分的能力？</span><span class="sxs-lookup"><span data-stu-id="465cd-122">Does this mean Enterprises will lose the abilities they had as part of ESR?</span></span>

<span data-ttu-id="465cd-123">不。</span><span class="sxs-lookup"><span data-stu-id="465cd-123">No.</span></span> <span data-ttu-id="465cd-124">Microsoft Edge 將繼續支援 ESR 提供的大部分功能。</span><span class="sxs-lookup"><span data-stu-id="465cd-124">Microsoft Edge will continue to support most of the abilities provided in the ESR offering.</span></span>

### <span data-ttu-id="465cd-125">跨裝置的一致體驗和新裝置的設定時間</span><span class="sxs-lookup"><span data-stu-id="465cd-125">Unified experience across devices and new device configuration time</span></span>

<span data-ttu-id="465cd-126">當使用者使用 Azure Active Directory (Azure AD 帳戶) 登入到其 Windows 裝置時，Microsoft Edge 將在初次啟動新瀏覽器時隱式繼承該身分識別。</span><span class="sxs-lookup"><span data-stu-id="465cd-126">When a user is signed into their windows device with an Azure Active Directory (Azure AD account), Microsoft Edge will implicitly inherit that Identity on first launch of the new browser.</span></span>

<span data-ttu-id="465cd-127">使用者明確同意在新 Microsoft Edge 中啟用同步後，瀏覽器將同步所有瀏覽器資料，如我的最愛、密碼和歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="465cd-127">After a user has explicitly consented to turning on sync in the new Microsoft Edge, the browser will sync all the browser data, such as favorites, passwords, and history.</span></span> <span data-ttu-id="465cd-128">這可確保跨裝置獲得一致的體驗，並縮短個人化瀏覽器所需的時間。</span><span class="sxs-lookup"><span data-stu-id="465cd-128">This ensures a unified experience across devices and reduces the time needed to personalize the browser.</span></span>

### <span data-ttu-id="465cd-129">分隔公司和消費者資料</span><span class="sxs-lookup"><span data-stu-id="465cd-129">Separation of corporate and consumer data</span></span>

<span data-ttu-id="465cd-130">組織可以控制他們的資料，消費者雲端帳戶中不會混合公司資料，企業雲端帳戶中也不會混合消費者資料。</span><span class="sxs-lookup"><span data-stu-id="465cd-130">Organizations are in control of their data, and there is no mixing of corporate data in a consumer cloud account or consumer data in an enterprise cloud account.</span></span>

### <span data-ttu-id="465cd-131">增強式安全性</span><span class="sxs-lookup"><span data-stu-id="465cd-131">Enhanced security</span></span>

<span data-ttu-id="465cd-132">資料會在離開使用者的 Windows 10 裝置之前自動加密，方法是使用 Azure 資訊保護，資料在雲端中待用時會保持加密。</span><span class="sxs-lookup"><span data-stu-id="465cd-132">Data is automatically encrypted before leaving the user’s Windows 10 device by using Azure Information Protection, and data stays encrypted at rest in the cloud.</span></span> <span data-ttu-id="465cd-133">所有內容在雲端中待用時會保持加密，除了命名空間，例如設定名稱。</span><span class="sxs-lookup"><span data-stu-id="465cd-133">All content stays encrypted at rest in the cloud, except for the namespaces, like settings names.</span></span>

### <span data-ttu-id="465cd-134">監視</span><span class="sxs-lookup"><span data-stu-id="465cd-134">Monitoring</span></span>

<span data-ttu-id="465cd-135">我們將透過 Azure AD 入口網站整合，對於誰能同步處理組織中的設定以及在哪些裝置上提供更多的控制權和可見性。</span><span class="sxs-lookup"><span data-stu-id="465cd-135">We will provide control and visibility over who syncs settings in your organization and on which devices through integration with the Azure AD portal.</span></span> <span data-ttu-id="465cd-136">此功能將在未來版本中啟用。</span><span class="sxs-lookup"><span data-stu-id="465cd-136">This capability will be enabled in a future release.</span></span>

### <span data-ttu-id="465cd-137">管理</span><span class="sxs-lookup"><span data-stu-id="465cd-137">Management</span></span>

<span data-ttu-id="465cd-138">管理員將能夠控制組織中哪些成員可以啟用同步。請參閱[設定 Microsoft Edge 同步](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync)和[同步群組原則](microsoft-edge-enterprise-sync.md#sync-group-policies)。</span><span class="sxs-lookup"><span data-stu-id="465cd-138">Admins will be able to control which members in your organization can enable sync. See [Configure Microsoft Edge sync](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync) and [Sync group policies](microsoft-edge-enterprise-sync.md#sync-group-policies).</span></span> <span data-ttu-id="465cd-139">此外，使用者可以為其每個裝置開啟/關閉同步，以及單獨切換每個資料屬性以進行同步。</span><span class="sxs-lookup"><span data-stu-id="465cd-139">Additionally, users can turn sync on/off for each of their devices as well as toggle each data attribute individually for sync.</span></span>

### <span data-ttu-id="465cd-140">金鑰管理</span><span class="sxs-lookup"><span data-stu-id="465cd-140">Key management</span></span>

<span data-ttu-id="465cd-141">同步功能利用 Azure 資訊保護 (AIP) 僅保護使用者和企業管理員的同步資料。</span><span class="sxs-lookup"><span data-stu-id="465cd-141">The synchronization feature leverages Azure Information Protection (AIP) to protect the synchronized data for only the user and the enterprise admins.</span></span> <span data-ttu-id="465cd-142">AIP 支援 Microsoft 託管 (預設) 和自攜金鑰以進行雲端金鑰管理。</span><span class="sxs-lookup"><span data-stu-id="465cd-142">AIP supports both Microsoft managed (default) and bring your own key for cloud-key management.</span></span> <span data-ttu-id="465cd-143">您的組織使用的雲端金鑰管理策略對 Microsoft Edge 是透明的，並且對同步功能沒有影響。</span><span class="sxs-lookup"><span data-stu-id="465cd-143">The cloud-key management strategy your organization uses is transparent to Microsoft Edge and has no impact on the synchronization feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="465cd-144">不支援[持有您自己的金鑰 (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) 和 Active Directory Rights Management Services。</span><span class="sxs-lookup"><span data-stu-id="465cd-144">[Hold your own key (HYOK)](https://docs.microsoft.com/azure/information-protection/configure-adrms-restrictions) and the Active Directory Rights Management Service aren't supported.</span></span>

## <span data-ttu-id="465cd-145">同步屬性摘要</span><span class="sxs-lookup"><span data-stu-id="465cd-145">Summary of sync attributes</span></span>

<span data-ttu-id="465cd-146">以下資料屬性將在初次同步時在新版本的 Microsoft Edge 中同步：</span><span class="sxs-lookup"><span data-stu-id="465cd-146">The following data attributes will sync in the new version of Microsoft Edge at first launch:</span></span>

- <span data-ttu-id="465cd-147">我的最愛</span><span class="sxs-lookup"><span data-stu-id="465cd-147">Favorites</span></span>
- <span data-ttu-id="465cd-148">密碼</span><span class="sxs-lookup"><span data-stu-id="465cd-148">Passwords</span></span>
- <span data-ttu-id="465cd-149">表單填滿</span><span class="sxs-lookup"><span data-stu-id="465cd-149">Form-fill</span></span>
- <span data-ttu-id="465cd-150">歷程記錄</span><span class="sxs-lookup"><span data-stu-id="465cd-150">History</span></span>
- <span data-ttu-id="465cd-151">開啟索引標籤 (工作階段)</span><span class="sxs-lookup"><span data-stu-id="465cd-151">Open tabs (sessions)</span></span>
- <span data-ttu-id="465cd-152">設定 (喜好設定)</span><span class="sxs-lookup"><span data-stu-id="465cd-152">Settings (preferences)</span></span>
- <span data-ttu-id="465cd-153">延伸模組</span><span class="sxs-lookup"><span data-stu-id="465cd-153">Extensions</span></span>

<span data-ttu-id="465cd-154">前面的屬性清單與可在 Microsoft Edge 舊版中同步的屬性不同。</span><span class="sxs-lookup"><span data-stu-id="465cd-154">The preceding list of attributes is different than the attributes that could be synced in Microsoft Edge Legacy.</span></span> <span data-ttu-id="465cd-155">(有關 Microsoft Edge 舊版設定的詳細資訊，請參閱 [Windows 10 漫遊設定](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference)。) 使用者可以使用 Microsoft Edge 設定，選擇啟用/停用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="465cd-155">(For details about Microsoft Edge Legacy settings, see [Windows 10 roaming settings](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference).) Users can selectively enable/disable these attributes using Microsoft Edge settings.</span></span> <span data-ttu-id="465cd-156">鑒於兩個版本 (例如歷史記錄) 之間的屬性差異，可能會要求使用者再次同意同步。</span><span class="sxs-lookup"><span data-stu-id="465cd-156">Given the difference in attributes between the two versions (for example, history), users might be asked to give sync consent again.</span></span>

> [!NOTE]
> <span data-ttu-id="465cd-157">與 Microsoft Edge 舊版不同，新 Microsoft Edge 不使用 Windows 認證管理員儲存密碼，因此不會將密碼與 Internet Explorer 或其他使用 Windows 認證管理員的應用程式同步。</span><span class="sxs-lookup"><span data-stu-id="465cd-157">Unlike Microsoft Edge Legacy, the new Microsoft Edge doesn't use Windows credential Manager for passwords and as a result, won't sync passwords with Internet Explorer or other apps that use Windows Credential manager.</span></span>

## <span data-ttu-id="465cd-158">服務條款</span><span class="sxs-lookup"><span data-stu-id="465cd-158">Terms of service</span></span>

<span data-ttu-id="465cd-159">Microsoft Edge 同步的服務條款屬於Microsoft 軟體授權，可在 Microsoft Edge 中輸入 *edge://terms* 查看。</span><span class="sxs-lookup"><span data-stu-id="465cd-159">Terms of service for Microsoft Edge sync falls under the Microsoft software license viewable in Microsoft Edge at *edge://terms*.</span></span>

## <span data-ttu-id="465cd-160">請參閱</span><span class="sxs-lookup"><span data-stu-id="465cd-160">See also</span></span>

- [<span data-ttu-id="465cd-161">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="465cd-161">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="465cd-162">Microsoft Edge 同步</span><span class="sxs-lookup"><span data-stu-id="465cd-162">Microsoft Edge Sync</span></span>](microsoft-edge-enterprise-sync.md)