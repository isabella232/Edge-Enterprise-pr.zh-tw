---
title: '[Microsoft Edge] 和 [Windows Defender 應用程式防護]'
ms.author: srugh
author: AndreaLBarr
manager: seanlyn
ms.date: 05/06/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 對 Microsoft Defender 應用程式防護的支援
ms.openlocfilehash: 7374810eb19ada298963817844e52184c0271a8c
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617993"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a><span data-ttu-id="19a2f-103">Microsoft Edge 對 Microsoft Defender 應用程式防護的支援</span><span class="sxs-lookup"><span data-stu-id="19a2f-103">Microsoft Edge support for Microsoft Defender Application Guard</span></span>

<span data-ttu-id="19a2f-104">本文說明 Microsoft Edge 如何支援 Microsoft Defender 應用程式防護 (應用程式防護)。</span><span class="sxs-lookup"><span data-stu-id="19a2f-104">This article describes how Microsoft Edge supports Microsoft Defender Application Guard (Application Guard).</span></span>

> [!NOTE]
> <span data-ttu-id="19a2f-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="19a2f-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="19a2f-106">概觀</span><span class="sxs-lookup"><span data-stu-id="19a2f-106">Overview</span></span>

<span data-ttu-id="19a2f-107">企業中的安全性架構師必須處理生產力與安全性之間的張力。</span><span class="sxs-lookup"><span data-stu-id="19a2f-107">Security architects in the enterprise must deal with the tension that exists between productivity and security.</span></span> <span data-ttu-id="19a2f-108">您可相當容易地鎖定瀏覽器，且只允許載入少數受信任的網站。</span><span class="sxs-lookup"><span data-stu-id="19a2f-108">It's relatively easy to lock down a browser and only allow a handful of trusted sites to load.</span></span> <span data-ttu-id="19a2f-109">這種方法可改善整體安全性狀態，但其生產力可能會降低。</span><span class="sxs-lookup"><span data-stu-id="19a2f-109">This approach will improve the overall security posture but is arguably less productive.</span></span> <span data-ttu-id="19a2f-110">如果您降低限制以提高生產力，則會提高風險度。</span><span class="sxs-lookup"><span data-stu-id="19a2f-110">If you make it less restrictive to improve productivity, you increase the risk profile.</span></span> <span data-ttu-id="19a2f-111">這是難以達到的平衡！</span><span class="sxs-lookup"><span data-stu-id="19a2f-111">It's a hard balance to strike!</span></span>

<span data-ttu-id="19a2f-112">在此不斷變化的威脅形勢中，我們更加難以掌握新興的威脅。</span><span class="sxs-lookup"><span data-stu-id="19a2f-112">It's even harder to keep up with new emerging threats in this constantly changing threat landscape.</span></span> <span data-ttu-id="19a2f-113">瀏覽器依舊是用戶端裝置上的主要受攻擊面，因為瀏覽器的基本任務是要讓使用者存取、下載和開啟不受信任來源中不受信任的內容。</span><span class="sxs-lookup"><span data-stu-id="19a2f-113">Browsers remain the primary attack surface on client devices because the browser's basic job is to let users access, download, and open untrusted content from untrusted sources.</span></span> <span data-ttu-id="19a2f-114">惡意行動者不斷鑽研針對瀏覽器的新型社交工程攻擊。</span><span class="sxs-lookup"><span data-stu-id="19a2f-114">Malicious actors are constantly working to social engineer new forms of attacks against the browser.</span></span> <span data-ttu-id="19a2f-115">安全性事件預防或偵測/回應策略無法保證 100% 安全。</span><span class="sxs-lookup"><span data-stu-id="19a2f-115">Security incident prevention or detection/response strategies can't guarantee 100% safety.</span></span>

<span data-ttu-id="19a2f-116">所要考量的重要安全戰略就是[採用破壞方法](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology)，這表示不論如何防範，都接受攻擊最少會成功一次。</span><span class="sxs-lookup"><span data-stu-id="19a2f-116">A key security strategy to consider is the [Assume Breach Methodology](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), which means there's an acceptance that an attack is going to succeed at least once regardless of efforts to prevent it.</span></span> <span data-ttu-id="19a2f-117">此種思維需要建立防禦措施來遏制損害，以確保在此情況下公司網路和其他資源仍然受到保護。</span><span class="sxs-lookup"><span data-stu-id="19a2f-117">This mindset requires building defenses to contain the damage, which ensures that corporate network and other resources remain protected in this scenario.</span></span>  <span data-ttu-id="19a2f-118">為 Microsoft Edge 部署應用程式防護正好符合此策略。</span><span class="sxs-lookup"><span data-stu-id="19a2f-118">Deploying Application Guard for Microsoft Edge fits right into this strategy.</span></span>

## <a name="about-application-guard"></a><span data-ttu-id="19a2f-119">關於應用程式防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-119">About Application Guard</span></span>

<span data-ttu-id="19a2f-120">應用程式防護專為 Windows 10 和 Microsoft Edge 設計，採用硬體隔離方法。</span><span class="sxs-lookup"><span data-stu-id="19a2f-120">Designed for Windows 10 and Microsoft Edge, Application Guard uses a hardware isolation approach.</span></span> <span data-ttu-id="19a2f-121">這種方法可讓不受信任的網站導覽在容器內啟動。</span><span class="sxs-lookup"><span data-stu-id="19a2f-121">This approach lets untrusted site navigation launch inside a container.</span></span> <span data-ttu-id="19a2f-122">硬體隔離可協助企業保護企業網路和資料，以防使用者造訪遭入侵或惡意的網站。</span><span class="sxs-lookup"><span data-stu-id="19a2f-122">Hardware isolation helps enterprises safeguard their corporate network and data in case users visit a site that is compromised or is malicious.</span></span>

<span data-ttu-id="19a2f-123">企業系統管理員可定義受信任的網站、雲端資源和內部網路。</span><span class="sxs-lookup"><span data-stu-id="19a2f-123">The enterprise administrator defines what are trusted sites, cloud resources, and internal networks.</span></span> <span data-ttu-id="19a2f-124">不在受信任的網站清單中的所有項目都會被視為不受信任。</span><span class="sxs-lookup"><span data-stu-id="19a2f-124">Everything that's not in the trusted sites list is considered untrusted.</span></span> <span data-ttu-id="19a2f-125">這些網站會與使用者裝置上的公司網路和資料隔離。</span><span class="sxs-lookup"><span data-stu-id="19a2f-125">These sites are isolated from the corporate network and data on the user's device.</span></span>

<span data-ttu-id="19a2f-126">如需詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="19a2f-126">For more information:</span></span>

- <span data-ttu-id="19a2f-127">觀看我們的影片：[使用應用程式防護的 Microsoft Edge 瀏覽器隔離](microsoft-edge-video-security-application-guard.md)</span><span class="sxs-lookup"><span data-stu-id="19a2f-127">watch our video [Microsoft Edge browser isolation using Application Guard](microsoft-edge-video-security-application-guard.md)</span></span>
- <span data-ttu-id="19a2f-128">請閱讀[什麼是應用程式防護及其如何運作？](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)</span><span class="sxs-lookup"><span data-stu-id="19a2f-128">read [What is Application Guard and how does it work?](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)</span></span>

<span data-ttu-id="19a2f-129">下一個螢幕擷取畫面顯示應用程式防護的訊息範例，其中顯示使用者正在安全的空間中瀏覽。</span><span class="sxs-lookup"><span data-stu-id="19a2f-129">The next screenshot shows an example of Application Guard's message showing that the user is browsing in a safe space.</span></span>

![應用程式防護的安全瀏覽訊息](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a><span data-ttu-id="19a2f-131">新功能</span><span class="sxs-lookup"><span data-stu-id="19a2f-131">What's new</span></span>

<span data-ttu-id="19a2f-132">新的 Microsoft Edge 瀏覽器中的應用程式防護支援具備與舊版 Microsoft Edge 同等的功能，且包含多項改善。</span><span class="sxs-lookup"><span data-stu-id="19a2f-132">Application Guard support in the new Microsoft Edge  browser has functional parity with Microsoft Edge Legacy and includes several improvements.</span></span>

### <a name="favorites-synchronizing-from-the-host-to-the-container"></a><span data-ttu-id="19a2f-133">將 [我的最愛] 從主機同步處理至容器</span><span class="sxs-lookup"><span data-stu-id="19a2f-133">Favorites synchronizing from the host to the container</span></span>

<span data-ttu-id="19a2f-134">我們的部分客戶一直要求在應用程式防護中的主機瀏覽器和容器之間同步 [我的最愛]。</span><span class="sxs-lookup"><span data-stu-id="19a2f-134">Some of our customers have been asking for favorites sync between the host browser and the container in Application Guard.</span></span> <span data-ttu-id="19a2f-135">從 Microsoft Edge 91 開始，使用者現在可以選擇設定應用程式防護，以將 [我的最愛] 從主機同步處理至容器。</span><span class="sxs-lookup"><span data-stu-id="19a2f-135">Starting from Microsoft Edge 91, users now have the option to configure Application Guard to synchronize their favorites from the host to the container.</span></span> <span data-ttu-id="19a2f-136">這可確保容器上也會出現新的 [我的最愛]。</span><span class="sxs-lookup"><span data-stu-id="19a2f-136">This ensures new favorites appear on the container as well.</span></span>

<span data-ttu-id="19a2f-137">可透過原則控制這項支援。</span><span class="sxs-lookup"><span data-stu-id="19a2f-137">This support can be controlled via policy.</span></span> <span data-ttu-id="19a2f-138">您可以更新 Edge 原則 [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) 以啟用或停用 [我的最愛] 同步處理。</span><span class="sxs-lookup"><span data-stu-id="19a2f-138">You can update the Edge policy [ApplicationGuardFavoritesSyncEnabled](/deployedge/microsoft-edge-policies#applicationguardfavoritessyncenabled) to enable or disable favorites sync.</span></span>

> [!Note]
> <span data-ttu-id="19a2f-139">基於安全性考量，[我的最愛] 同步處理僅能從主機同步處理到容器，且不能為相反的方式。</span><span class="sxs-lookup"><span data-stu-id="19a2f-139">For security reasons, favorites sync is only possible from the host to the container and not the other way around.</span></span> <span data-ttu-id="19a2f-140">若要確保跨主機和容器的 [我的最愛] 整合清單，我們已停用容器內的 [我的最愛] 管理。</span><span class="sxs-lookup"><span data-stu-id="19a2f-140">To ensure a unified list of favorites across the host and the container, we have disabled favorites management inside the container.</span></span>

### <a name="identify-network-traffic-originating-from-the-container"></a><span data-ttu-id="19a2f-141">識別源自容器的流量</span><span class="sxs-lookup"><span data-stu-id="19a2f-141">Identify network traffic originating from the container</span></span>

<span data-ttu-id="19a2f-142">數個客戶正在特定組態中使用 WDAG，以便識別來自容器的流量。</span><span class="sxs-lookup"><span data-stu-id="19a2f-142">Several customers are using WDAG in a specific configuration where they want to identify network traffic coming from the container.</span></span> <span data-ttu-id="19a2f-143">此情況的其中一些案例為：</span><span class="sxs-lookup"><span data-stu-id="19a2f-143">Some of the scenarios for this are:</span></span>

- <span data-ttu-id="19a2f-144">若要限制僅存取少數的未受信任網站</span><span class="sxs-lookup"><span data-stu-id="19a2f-144">To restrict access to only a handful of untrusted sites</span></span>
- <span data-ttu-id="19a2f-145">若允許僅從容器存取網際網路</span><span class="sxs-lookup"><span data-stu-id="19a2f-145">To allow internet access from the container only</span></span>

<span data-ttu-id="19a2f-146">從 Microsoft Edge 版本 91 開始，內建支援以標記來自應用程式防護容器的流量，讓企業能夠使用 proxy 以篩選出流量及套用特定原則。</span><span class="sxs-lookup"><span data-stu-id="19a2f-146">Starting with Microsoft Edge version 91, there’s built in support to tag network traffic originating from Application Guard containers, allowing enterprises to use proxy to filter out traffic and apply specific policies.</span></span> <span data-ttu-id="19a2f-147">您可以使用標頭以識別哪些流量是透過容器或主機使用 [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled)。</span><span class="sxs-lookup"><span data-stu-id="19a2f-147">You can use the header to identify which traffic is through the container or the host using [ApplicationGuardTrafficIdentificationEnabled](/deployedge/microsoft-edge-policies#applicationguardtrafficidentificationenabled).</span></span>

### <a name="extension-support-inside-the-container"></a><span data-ttu-id="19a2f-148">容器內的延伸支援</span><span class="sxs-lookup"><span data-stu-id="19a2f-148">Extension support inside the container</span></span>

<span data-ttu-id="19a2f-149">容器內的延伸支援曾經是來自客戶的最熱門要求之一。</span><span class="sxs-lookup"><span data-stu-id="19a2f-149">Extension support inside the container has been one of the top requests from the customers.</span></span> <span data-ttu-id="19a2f-150">案例包含從想要在容器內執行廣告封鎖程式來提升瀏覽器效能，以至能夠在容器內執行自產的自訂延伸。</span><span class="sxs-lookup"><span data-stu-id="19a2f-150">Scenarios ranged from wanting to run ad-blockers inside the container to boost browser performance to having the ability to run custom home-grown extensions inside the container.</span></span>

<span data-ttu-id="19a2f-151">現在支援在容器中安裝延伸 (從 Microsoft Edge 版本 81 開始)。</span><span class="sxs-lookup"><span data-stu-id="19a2f-151">Extension installs in the container is now supported, starting from Microsoft Edge version 81.</span></span> <span data-ttu-id="19a2f-152">可透過原則控制這項支援。</span><span class="sxs-lookup"><span data-stu-id="19a2f-152">This support can be controlled via policy.</span></span> <span data-ttu-id="19a2f-153">在 [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) 原則中使用的 `updateURL`，應新增為應用程式防護所用網路隔離原則中的中性資源。</span><span class="sxs-lookup"><span data-stu-id="19a2f-153">The `updateURL` that gets used in [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) policy should be added as Neutral Resources in the Network Isolation policies used by Application Guard.</span></span>

<span data-ttu-id="19a2f-154">有些容器支援範例包含下列案例：</span><span class="sxs-lookup"><span data-stu-id="19a2f-154">Some examples of container support include the following scenarios:</span></span>

- <span data-ttu-id="19a2f-155">在主機上強制安裝延伸</span><span class="sxs-lookup"><span data-stu-id="19a2f-155">Force installs of an extension on the host</span></span>
- <span data-ttu-id="19a2f-156">從主機移除延伸</span><span class="sxs-lookup"><span data-stu-id="19a2f-156">Removing an extension from the host</span></span>
- <span data-ttu-id="19a2f-157">主機上封鎖的延伸</span><span class="sxs-lookup"><span data-stu-id="19a2f-157">Extensions blocked on the host</span></span>

> [!NOTE]
> <span data-ttu-id="19a2f-158">您也可從延伸存放區，在容器內手動安裝個別的延伸。</span><span class="sxs-lookup"><span data-stu-id="19a2f-158">It's also possible to manually install individual extensions inside the container from the extension store.</span></span> <span data-ttu-id="19a2f-159">啟用 [允許保留][](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) 原則後，只有手動安裝的延伸才會保留在容器中。</span><span class="sxs-lookup"><span data-stu-id="19a2f-159">Manually installed extensions will only persist in the container when [Allow Persistence](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) policy is enabled.</span></span>

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a><span data-ttu-id="19a2f-160">透過雙 Proxy 識別應用程式防護流量</span><span class="sxs-lookup"><span data-stu-id="19a2f-160">Identifying Application Guard traffic via Dual Proxy</span></span>

<span data-ttu-id="19a2f-161">部分企業客戶正在部署適用于特定案例的應用程式防護，以便識別來自 Microsoft Defender 應用程式防護容器的 proxy 等級網路流量。</span><span class="sxs-lookup"><span data-stu-id="19a2f-161">Some enterprise customers are deploying Application Guard with a specific use case where they need to identify web traffic coming out of a Microsoft Defender Application Guard container at the proxy level.</span></span> <span data-ttu-id="19a2f-162">從穩定通道版本 84 開始，Microsoft Edge 將支援雙 proxy 來滿足這一需求。</span><span class="sxs-lookup"><span data-stu-id="19a2f-162">Starting with Stable Channel version 84, Microsoft Edge will support dual proxy to address this requirement.</span></span> <span data-ttu-id="19a2f-163">您可以使用 [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) 原則來設定此功能。</span><span class="sxs-lookup"><span data-stu-id="19a2f-163">You can configure this functionality using the [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) policy.</span></span>

<span data-ttu-id="19a2f-164">下圖顯示 Microsoft Edge 的雙 proxy 架構。</span><span class="sxs-lookup"><span data-stu-id="19a2f-164">The following drawing shows the dual proxy architecture for Microsoft Edge.</span></span>

![應用程式防護的雙 proxy 架構](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a><span data-ttu-id="19a2f-166">用於疑難排解的診斷頁面</span><span class="sxs-lookup"><span data-stu-id="19a2f-166">Diagnostic page for troubleshooting</span></span>

<span data-ttu-id="19a2f-167">另一個使用者痛點就是在問題回報後，針對裝置上的應用程式防護設定進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="19a2f-167">Another user pain point is troubleshooting the Application Guard configuration on a device when a problem is reported.</span></span> <span data-ttu-id="19a2f-168">Microsoft Edge 有診斷頁面 (`edge://application-guard-internals`) 可針對使用者問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="19a2f-168">Microsoft Edge has a diagnostics page (`edge://application-guard-internals`) to troubleshoot user issues.</span></span> <span data-ttu-id="19a2f-169">其中一項診斷可根據使用者裝置上的設定來檢查 URL 信任。</span><span class="sxs-lookup"><span data-stu-id="19a2f-169">One of these diagnostics is being able to check the URL trust based on the configuration on the user's device.</span></span>

<span data-ttu-id="19a2f-170">下一個螢幕擷取畫面顯示多個索引標籤診斷頁面，以協助診斷使用者回報告的裝置問題。</span><span class="sxs-lookup"><span data-stu-id="19a2f-170">The next screenshot shows a multiple tab diagnostics page to help diagnose user reported issues on the device.</span></span>

![應用程式防護診斷頁面](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a><span data-ttu-id="19a2f-172">容器中的 Microsoft Edge 更新</span><span class="sxs-lookup"><span data-stu-id="19a2f-172">Microsoft Edge updates in the container</span></span>

<span data-ttu-id="19a2f-173">容器中的舊版 Microsoft Edge 更新是 Windows OS 更新週期的一部分。</span><span class="sxs-lookup"><span data-stu-id="19a2f-173">Microsoft Edge Legacy updates in the container are part of the Windows OS update cycle.</span></span> <span data-ttu-id="19a2f-174">由於新版 Microsoft Edge 更新本身與 Windows OS 無關，因此不再相依於容器更新。</span><span class="sxs-lookup"><span data-stu-id="19a2f-174">Because the new version of Microsoft Edge updates itself independent of the Windows OS, there is no longer any dependency on container updates.</span></span> <span data-ttu-id="19a2f-175">主機 Microsoft Edge 的通道和版本會在容器內複寫。</span><span class="sxs-lookup"><span data-stu-id="19a2f-175">The channel and version of the host Microsoft Edge is replicated inside the container.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="19a2f-176">必要條件</span><span class="sxs-lookup"><span data-stu-id="19a2f-176">Prerequisites</span></span>

<span data-ttu-id="19a2f-177">下列需求適用於使用應用程式防護搭配 Microsoft Edge 的裝置：</span><span class="sxs-lookup"><span data-stu-id="19a2f-177">The following  requirements apply to devices using Application Guard with Microsoft Edge:</span></span>

- <span data-ttu-id="19a2f-178">Windows 10 1809 (RS5) 及以上版本。</span><span class="sxs-lookup"><span data-stu-id="19a2f-178">Windows 10 1809 (RS5) and above.</span></span>
- <span data-ttu-id="19a2f-179">僅限 Windows 用戶端 SKU</span><span class="sxs-lookup"><span data-stu-id="19a2f-179">Only Windows client SKUs</span></span>

  > [!NOTE]
  > <span data-ttu-id="19a2f-180">只有 Windows 10 專業版和 Windows 10 企業版 SKU 支援應用程式防護。</span><span class="sxs-lookup"><span data-stu-id="19a2f-180">Application Guard is only supported on Windows 10 Pro and Windows 10 Enterprise SKUs.</span></span>

- <span data-ttu-id="19a2f-181">[軟體需求](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)所述的其中一個管理解決方案</span><span class="sxs-lookup"><span data-stu-id="19a2f-181">One of the management solutions described in [Software requirements](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)</span></span>

## <a name="how-to-install-application-guard"></a><span data-ttu-id="19a2f-182">如何安裝應用程式防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-182">How to install Application Guard</span></span>

<span data-ttu-id="19a2f-183">下列文章提供透過 Microsoft Edge 安裝、設定及測試應用程式防護所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="19a2f-183">The following articles provide the information you need to install, configure, and test Application Guard with Microsoft Edge.</span></span>

- [<span data-ttu-id="19a2f-184">系統需求</span><span class="sxs-lookup"><span data-stu-id="19a2f-184">System requirements</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [<span data-ttu-id="19a2f-185">安裝 Microsoft Defender 應用程式防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-185">Install Microsoft Defender Application Guard</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [<span data-ttu-id="19a2f-186">設定 Microsoft Defender 群組原則設定</span><span class="sxs-lookup"><span data-stu-id="19a2f-186">Configure Microsoft Defender group policy settings</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [<span data-ttu-id="19a2f-187">測試應用程式防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-187">Test Application Guard</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a><span data-ttu-id="19a2f-188">常見問題集</span><span class="sxs-lookup"><span data-stu-id="19a2f-188">Frequently Asked Questions</span></span>

### <a name="does-application-guard-work-in-ie-mode"></a><span data-ttu-id="19a2f-189">應用程式防護是否可在 IE 模式中運作？</span><span class="sxs-lookup"><span data-stu-id="19a2f-189">Does Application Guard work in IE mode?</span></span>

<span data-ttu-id="19a2f-190">IE 模式支援應用程式防護功能，但我們不期望在 IE 模式中經常使用此功能。</span><span class="sxs-lookup"><span data-stu-id="19a2f-190">IE mode supports Application Guard functionality, but we don't anticipate much use of this feature in IE Mode.</span></span> <span data-ttu-id="19a2f-191">建議針對一些受信任的內部網站部署 IE 模式，而應用程式防護只適用於不受信任的網站。</span><span class="sxs-lookup"><span data-stu-id="19a2f-191">IE mode is recommended to be deployed for a list of trusted internal sites, and Application Guard is for untrusted sites only.</span></span> <span data-ttu-id="19a2f-192">確定所有 IE 模式網站或 IP 位址也會新增至網路隔離原則，使應用程式防護將其視為受信任的資源。</span><span class="sxs-lookup"><span data-stu-id="19a2f-192">Make sure all the IE mode sites or IP addresses are also added to the Network Isolation policy to be considered as trusted resource by Application Guard.</span></span>

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a><span data-ttu-id="19a2f-193">我需要安裝應用程式防護 Chrome 延伸嗎？</span><span class="sxs-lookup"><span data-stu-id="19a2f-193">Do I need to install the Application Guard Chrome extension?</span></span>

<span data-ttu-id="19a2f-194">否，Microsoft Edge 本身就支援應用程式防護功能。</span><span class="sxs-lookup"><span data-stu-id="19a2f-194">No, the Application Guard feature is natively supported in Microsoft Edge.</span></span> <span data-ttu-id="19a2f-195">事實上，應用程式防護 Chrome 延伸不是 Microsoft Edge 中支援的設定。</span><span class="sxs-lookup"><span data-stu-id="19a2f-195">In fact, the Application Guard Chrome extension isn't a supported configuration in Microsoft Edge.</span></span>

### <a name="are-there-any-other-platform-related-faqs"></a><span data-ttu-id="19a2f-196">是否有任何其他平台相關的常見問題集？</span><span class="sxs-lookup"><span data-stu-id="19a2f-196">Are there any other platform related FAQs?</span></span>

<span data-ttu-id="19a2f-197">是。</span><span class="sxs-lookup"><span data-stu-id="19a2f-197">Yes.</span></span> [<span data-ttu-id="19a2f-198">常見問答集─Microsoft Defender 應用程式防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-198">Frequently asked questions - Microsoft Defender Application Guard</span></span>](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a><span data-ttu-id="19a2f-199">請參閱</span><span class="sxs-lookup"><span data-stu-id="19a2f-199">See also</span></span>

- [<span data-ttu-id="19a2f-200">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="19a2f-200">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="19a2f-201">Microsoft Defender 進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="19a2f-201">Microsoft Defender Advanced Threat Protection</span></span>](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="19a2f-202">影片：使用應用程式防護的 Microsoft Edge 瀏覽器隔離</span><span class="sxs-lookup"><span data-stu-id="19a2f-202">Video: Microsoft Edge browser isolation using Application Guard</span></span>](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)