---
title: 適用於虛擬化桌面基礎結構的 Microsoft Edge
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 的虛擬化桌面基礎結構。
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618063"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a><span data-ttu-id="6dc12-103">Microsoft Edge 的虛擬化桌面基礎結構</span><span class="sxs-lookup"><span data-stu-id="6dc12-103">Microsoft Edge for Virtualized Desktop Infrastructure</span></span>

<span data-ttu-id="6dc12-104">本文說明在虛擬化環境中使用 Microsoft Edge 的需求和限制。</span><span class="sxs-lookup"><span data-stu-id="6dc12-104">This article describes the requirements and limitations for using Microsoft Edge in a virtualized environment.</span></span>

## <a name="what-is-vdi"></a><span data-ttu-id="6dc12-105">什麼是 VDI？</span><span class="sxs-lookup"><span data-stu-id="6dc12-105">What is VDI?</span></span>

<span data-ttu-id="6dc12-106">虛擬桌面基礎結構 (VDI) 是虛擬化技術，在資料中心的集中式伺服器上託管桌面作業系統和應用程式。</span><span class="sxs-lookup"><span data-stu-id="6dc12-106">Virtual Desktop Infrastructure (VDI) is virtualization technology that hosts a desktop operating system and applications on a centralized server in a data center.</span></span> <span data-ttu-id="6dc12-107">這可讓具有完全安全且符合規範的集中式來源的使用者獲得完全個人化的桌面體驗。</span><span class="sxs-lookup"><span data-stu-id="6dc12-107">This enables a fully personalized desktop experience for users with a fully secured and compliant centralized source.</span></span>

<span data-ttu-id="6dc12-108">Microsoft Edge 可在這類虛擬化環境中使用，其使用方式與在本機裝置上使用的方式非常類似，同時從安全且受控制的伺服器環境執行。</span><span class="sxs-lookup"><span data-stu-id="6dc12-108">Microsoft Edge can be used in such a virtualized environment in much the same ways as it can be used on the local device, all the while running from secure and controlled server environment.</span></span> <span data-ttu-id="6dc12-109">視您選擇的 VDI 解決方案不同，也可能讓使用者順暢地存取內部網路應用程式和網站。</span><span class="sxs-lookup"><span data-stu-id="6dc12-109">Depending on your chosen VDI solution it may also be possible to give your users seamless access to intranet Applications and Sites.</span></span>

<span data-ttu-id="6dc12-110">大部分的 Microsoft Edge 功能都可在 VDI 環境中都受到支援，沒有任何特殊設定。</span><span class="sxs-lookup"><span data-stu-id="6dc12-110">Most features of Edge are supported on VDI environments without any special configuration.</span></span> <span data-ttu-id="6dc12-111">不過，為了確保獲得最佳體驗，建議您遵循下列指引。</span><span class="sxs-lookup"><span data-stu-id="6dc12-111">However, to ensure an optimal experience it’s recommended to follow the guidance below.</span></span>

## <a name="platforms-certified-for-edge"></a><span data-ttu-id="6dc12-112">通過 Microsoft Edge 認證的平台</span><span class="sxs-lookup"><span data-stu-id="6dc12-112">Platforms certified for Edge</span></span>

- <span data-ttu-id="6dc12-113">Azure 虛擬桌面</span><span class="sxs-lookup"><span data-stu-id="6dc12-113">Azure Virtual Desktop</span></span>
- <span data-ttu-id="6dc12-114">Citrix 虛擬應用程式和桌面 (之前稱為 XenApp 和 XenDesktop)</span><span class="sxs-lookup"><span data-stu-id="6dc12-114">Citrix Virtual Apps and Desktops (formerly known as XenApp and XenDesktop)</span></span>

<span data-ttu-id="6dc12-115">雖然 Microsoft Edge 小組尚未驗證其他 VDI 解決方案，但預期會支援 Edge 中最常見的工作流程。</span><span class="sxs-lookup"><span data-stu-id="6dc12-115">While other VDI solutions have not yet been verified by the Edge team, it is expected that the most common workflows in Edge should be supported.</span></span> <span data-ttu-id="6dc12-116">下列提供之指引不一定適用於您選擇的解決方案。</span><span class="sxs-lookup"><span data-stu-id="6dc12-116">Guidance provided below may or may not be applicable to your chosen solution.</span></span>

## <a name="edge-on-vdi-performance-considerations"></a><span data-ttu-id="6dc12-117">VDI 效能考量的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dc12-117">Edge on VDI performance considerations</span></span>

<span data-ttu-id="6dc12-118">在設計 VDI 環境時，您應該仔細考慮使用者的工作流程和需求，以獲得最佳的績效和伺服器設定的限制。</span><span class="sxs-lookup"><span data-stu-id="6dc12-118">When designing your VDI environment you should carefully consider the workflows and needs of your users to achieve optimal performance, as well as the limits of your server configuration.</span></span>

<span data-ttu-id="6dc12-119">Edge 建議將 Microsoft Edge 部署到 VDI 環境時，遵循下列最低需求：</span><span class="sxs-lookup"><span data-stu-id="6dc12-119">Edge recommends the following minimal requirements for deploying Edge to VDI environments:</span></span>

- <span data-ttu-id="6dc12-120">vCPU – 每個使用者 2-4 個核心</span><span class="sxs-lookup"><span data-stu-id="6dc12-120">vCPU – 2-4 Cores per User</span></span>
- <span data-ttu-id="6dc12-121">RAM – 每個使用者 1 GB</span><span class="sxs-lookup"><span data-stu-id="6dc12-121">RAM – 1 GB per User</span></span>

<span data-ttu-id="6dc12-122">請注意，大型複雜 Web 應用程式和擴充功能需要更多記憶體，且在設定您的環境時必須加以考慮。</span><span class="sxs-lookup"><span data-stu-id="6dc12-122">Please note that large complex web applications and extensions will require more memory and will have to be accounted for when configuring your environment.</span></span>

## <a name="edge-on-non-persisted-vdi-environments"></a><span data-ttu-id="6dc12-123">位於非持續 VDI 環境的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dc12-123">Edge on non-persisted VDI environments</span></span>

<span data-ttu-id="6dc12-124">許多 VDI 解決方案都允許存取持續的環境，其中使用者獲指派一個可在工作模式之間持續的虛擬環境；而非持續環境，其中使用者獲指派數部可用電腦的其中一部 (每個工作模式可能是不同的電腦)，使用者資料不一定會在工作階段之間同步。</span><span class="sxs-lookup"><span data-stu-id="6dc12-124">Many VDI solutions allow access to persisted environments, where users are assigned a virtual environment that persists between sessions, and non-persisted environments, where users are assigned to one of several available machines, possibly a different machine each session, user data may or may not sync between sessions.</span></span>

<span data-ttu-id="6dc12-125">使用非持續環境時，通常會建立「金色影像」，用於包含所需的應用程式和設定的每個裝置。</span><span class="sxs-lookup"><span data-stu-id="6dc12-125">When using a non-persisted environment, one usually creates a “golden image” which is used for each device that includes the needed apps and configurations.</span></span> <span data-ttu-id="6dc12-126">以下是我們針對這類影像準備 Microsoft Edge 的建議。</span><span class="sxs-lookup"><span data-stu-id="6dc12-126">Below are our recommendations for preparing Edge for such an image.</span></span>

### <a name="deploy-edge"></a><span data-ttu-id="6dc12-127">部署 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6dc12-127">Deploy Edge</span></span>

<span data-ttu-id="6dc12-128">如果您目前使用 Windows 10 (版本 1803) 及更新版本，您應該將 Microsoft Edge 安裝在您的系統上。</span><span class="sxs-lookup"><span data-stu-id="6dc12-128">If you are on Windows 10, version 1803 and above, you should have Microsoft Edge installed on your system.</span></span> <span data-ttu-id="6dc12-129">不過，如果您使用舊版的 Windows 或想要部署 Microsoft Edge 的其他通道，建議執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6dc12-129">However, if you are on an older version of Windows or wish to deploy a different channel of Edge, the following steps are recommended.</span></span>

1. <span data-ttu-id="6dc12-130">從以下下載符合您 VDI VM 作業系統的 Microsoft Edge MSI 套件：</span><span class="sxs-lookup"><span data-stu-id="6dc12-130">Download the Edge MSI package matching your VDI VM operating system from:</span></span>

    - [<span data-ttu-id="6dc12-131">下載商務用 Microsoft Edge - Microsoft</span><span class="sxs-lookup"><span data-stu-id="6dc12-131">Download Microsoft Edge for Business - Microsoft</span></span>](https://www.microsoft.com/edge/business/download)

2. <span data-ttu-id="6dc12-132">執行下列命令，將 MSI 安裝到 VDI VM：</span><span class="sxs-lookup"><span data-stu-id="6dc12-132">Install the MSI to the VDI VM by running the following command:</span></span>

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a><span data-ttu-id="6dc12-133">停用自動更新</span><span class="sxs-lookup"><span data-stu-id="6dc12-133">Disable automatic updates</span></span>

<span data-ttu-id="6dc12-134">對於非保存的電腦，最佳做法是停用自動更新並改為更新 Microsoft Edge，做法是更新「標準映射」，以確保電腦集區之間沒有版本不符的情況。</span><span class="sxs-lookup"><span data-stu-id="6dc12-134">For non-persisted machines it is best practice to disable automatic updates and instead update Edge by updating the “golden image” to ensure that there are no version mismatches among the pool of machines.</span></span>

<span data-ttu-id="6dc12-135">請參閱下列停用自動更新的原則：</span><span class="sxs-lookup"><span data-stu-id="6dc12-135">See the following policies for disabling automatic updates:</span></span>

- [<span data-ttu-id="6dc12-136">更新原則覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="6dc12-136">Update policy override default</span></span>](/deployedge/microsoft-edge-update-policies#updatedefault)

- [<span data-ttu-id="6dc12-137">更新原則覆寫</span><span class="sxs-lookup"><span data-stu-id="6dc12-137">Update policy override</span></span>](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a><span data-ttu-id="6dc12-138">設定檔管理</span><span class="sxs-lookup"><span data-stu-id="6dc12-138">Profile management</span></span>

<span data-ttu-id="6dc12-139">在非持續的設定中，請務必考慮，VM 可能無法維持工作模式之間的使用者狀態，或者使用者可能會獲指派一個他們之前從未使用的虛擬電腦，因此沒有使用者資料。</span><span class="sxs-lookup"><span data-stu-id="6dc12-139">On non-persisted setups it is important to consider that VMs may not maintain user state between sessions or users may be assigned a VM they have never used before and as such has none of their user data.</span></span>

<span data-ttu-id="6dc12-140">Edge 支援數種同步處理使用者資料的方法，無論使用者資料存取 Microsoft Edge的方式如何，都能使用。</span><span class="sxs-lookup"><span data-stu-id="6dc12-140">Edge supports several methods for syncing user data such that it is available regardless of how they are accessing Edge.</span></span>

### <a name="azure-ad-sync"></a><span data-ttu-id="6dc12-141">Azure AD Sync</span><span class="sxs-lookup"><span data-stu-id="6dc12-141">Azure AD Sync</span></span>

<span data-ttu-id="6dc12-142">如果您的 Azure AD 方案支援，企業同步處理是最快速且最簡單的方法，可確保 Microsoft Edge 使用者資料會同步處理至所有的使用者裝置。</span><span class="sxs-lookup"><span data-stu-id="6dc12-142">If your Azure AD plan supports it, Enterprise sync is the fastest and easiest method to ensure that Edge user data is synced to all user devices.</span></span>  

<span data-ttu-id="6dc12-143">請參閱下列內容以取得要求和設定的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6dc12-143">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="6dc12-144">設定 Microsoft Edge 企業同步 | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="6dc12-144">Configure Microsoft Edge enterprise sync | Microsoft Docs</span></span>](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a><span data-ttu-id="6dc12-145">Active Directory 使用者的內部部署同步</span><span class="sxs-lookup"><span data-stu-id="6dc12-145">On-premise Sync for Active Directory Users</span></span>

<span data-ttu-id="6dc12-146">有了內部部署同步，Microsoft Edge 會將 Active Directory 使用者的我的最愛和設定儲存至可在不同電腦之間輕易移動的檔案。</span><span class="sxs-lookup"><span data-stu-id="6dc12-146">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can easily be moved between different computers.</span></span>  

<span data-ttu-id="6dc12-147">請參閱下列內容以取得要求和設定的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6dc12-147">See the following for more information on requirements and configuration.</span></span>  

- [<span data-ttu-id="6dc12-148">Active Directory (AD) 使用者 | Microsoft Docs 的內部部署同步</span><span class="sxs-lookup"><span data-stu-id="6dc12-148">On-premises sync for Active Directory (AD) users | Microsoft Docs</span></span>](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a><span data-ttu-id="6dc12-149">使用者設定檔重新導向</span><span class="sxs-lookup"><span data-stu-id="6dc12-149">User Profile Redirection</span></span>  

<span data-ttu-id="6dc12-150">移轉和重新導向整個使用者資料夾的解決方案有好幾種，以確保使用者內容可維持在這類非持續的環境中。</span><span class="sxs-lookup"><span data-stu-id="6dc12-150">There are several solutions for migrating and redirecting the entire user folder to ensure that user context is maintained in such non-persisted environments.</span></span> <span data-ttu-id="6dc12-151">請和您的 VDI 提供者確認以決定建議的解決方案。</span><span class="sxs-lookup"><span data-stu-id="6dc12-151">Check with your VDI provider to determine the recommended solution.</span></span>

<span data-ttu-id="6dc12-152">一些熱門解決方案包括：</span><span class="sxs-lookup"><span data-stu-id="6dc12-152">Some popular solutions include:</span></span>

- [<span data-ttu-id="6dc12-153">FSLogix 概觀 - FSLogix |Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="6dc12-153">FSLogix Overview - FSLogix | Microsoft Docs</span></span>](/fslogix/overview)
- [<span data-ttu-id="6dc12-154">如何設定 Citrix 設定檔管理</span><span class="sxs-lookup"><span data-stu-id="6dc12-154">How to Configure Citrix Profile Management</span></span>](https://support.citrix.com/article/CTX222893)

<span data-ttu-id="6dc12-155">另外，建議您在使用此方法時，將不必要的資料夾從備份的使用者資料夾排除，以減少使用者登入電腦和移轉設定檔時的初始載入時間。</span><span class="sxs-lookup"><span data-stu-id="6dc12-155">It is also may be recommended that when using this method unnecessary folders be excluded from the backed-up user folder to reduce initial loading times when users are logging on to a machine and the profile is being migrated.</span></span> <span data-ttu-id="6dc12-156">如果是這樣，建議您將下列資料夾從您的備份排除，以減少檔案大小。</span><span class="sxs-lookup"><span data-stu-id="6dc12-156">If so, we recommend the following folders be excluded from your backup to reduce size.</span></span>

- <span data-ttu-id="6dc12-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span><span class="sxs-lookup"><span data-stu-id="6dc12-157">%LocalAppData%\Microsoft\Edge\User Data\Default\Cache</span></span>
- <span data-ttu-id="6dc12-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span><span class="sxs-lookup"><span data-stu-id="6dc12-158">%LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache</span></span>
- <span data-ttu-id="6dc12-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span><span class="sxs-lookup"><span data-stu-id="6dc12-159">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites</span></span>
- <span data-ttu-id="6dc12-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span><span class="sxs-lookup"><span data-stu-id="6dc12-160">%LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed</span></span>

## <a name="known-issues"></a><span data-ttu-id="6dc12-161">已知問題</span><span class="sxs-lookup"><span data-stu-id="6dc12-161">Known issues</span></span>

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a><span data-ttu-id="6dc12-162">Microsoft Edge 會在舊版的 XenApp 和 XenDesktop 中當機</span><span class="sxs-lookup"><span data-stu-id="6dc12-162">Microsoft Edge crashes in older versions of XenApp and XenDesktop</span></span>

<span data-ttu-id="6dc12-163">此問題應該會在較新的版本中減少，不過，如果您在環境中遇到此問題，您可以停用 Microsoft Edge 的 Citrix API Hooks 以解決此問題，請參閱 [如何根據每個應用程式停用 Citrix API Hooks。](https://support.citrix.com/article/CTX107825)</span><span class="sxs-lookup"><span data-stu-id="6dc12-163">This issue should be mitigated in newer versions however if you are encountering this issue in your environment, you can work around the issue by disabling Citrix API Hooks for Edge, see [How to Disable Citrix API Hooks on a Per-application Basis.](https://support.citrix.com/article/CTX107825)</span></span>

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a><span data-ttu-id="6dc12-164">使用超大型 HTML 表格呈現頁面時，效能會降低</span><span class="sxs-lookup"><span data-stu-id="6dc12-164">Degraded performance when rendering pages with exceptionally large HTML tables</span></span>

<span data-ttu-id="6dc12-165">下列的 Citrix 原則已知會緩慢呈現具超大型表格的 HTML 網頁 (超過 30,000 個資料列)。</span><span class="sxs-lookup"><span data-stu-id="6dc12-165">The following Citrix policies are known to slow rendering of html pages with very large (30,000+ row) tables.</span></span>

- <span data-ttu-id="6dc12-166">自動鍵盤顯示</span><span class="sxs-lookup"><span data-stu-id="6dc12-166">Automatic keyboard display</span></span>
- <span data-ttu-id="6dc12-167">遠端下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="6dc12-167">Remote the combo box</span></span>

<span data-ttu-id="6dc12-168">請參閱 [行動體驗原則設定 (citrix.com) ](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) 以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6dc12-168">See [Mobile experience policy settings (citrix.com)](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) for more information.</span></span> <span data-ttu-id="6dc12-169">停用這些原則應該可以減緩此問題。</span><span class="sxs-lookup"><span data-stu-id="6dc12-169">Disabling these policies should mitigate the issue.</span></span>

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a><span data-ttu-id="6dc12-170">在 Microsoft Edge 中．在以 Citrix 隨選即用應用程式執行時，Windows 帳戶管理員授權案例失敗</span><span class="sxs-lookup"><span data-stu-id="6dc12-170">Windows Account Manager authorization scenarios (i.e.  Azure sync) fail in Edge when run as a Citrix seamless application</span></span>

<span data-ttu-id="6dc12-171">這是 Microsoft Edge 和其他使用 WAM 的應用程式 (即 Office) 中的已知問題，因為這類案例所需的 Windows 元件在「順暢」模式下執行時並未初始化。</span><span class="sxs-lookup"><span data-stu-id="6dc12-171">This is a known issue in Edge and other applications that use WAM (i.e. Office) due to Windows components necessary for such scenarios not being initialized when running in the “seamless” mode.</span></span> <span data-ttu-id="6dc12-172">若要解決此問題：</span><span class="sxs-lookup"><span data-stu-id="6dc12-172">To work around this issue:</span></span>

- <span data-ttu-id="6dc12-173">透過遠端桌面將 Microsoft Edge 使用至 Citrix 主機，而不是做為流暢的遠端應用程式。</span><span class="sxs-lookup"><span data-stu-id="6dc12-173">Use Edge via a Remote Desktop to the Citrix Host instead of as a seamless remote application.</span></span>
- <span data-ttu-id="6dc12-174">請改為使用 Azure 虛擬桌面遠端應用程式，其中有此問題的緩解措施。</span><span class="sxs-lookup"><span data-stu-id="6dc12-174">Use Azure Virtual Desktop remote apps instead, which has mitigation's for this issue.</span></span>
