---
title: '[Microsoft Edge] 和 [Windows Defender 應用程式防護]'
ms.author: srugh
author: dan-wesley
manager: seanlyn
ms.date: 06/19/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 對 Microsoft Defender 應用程式防護的支援。
ms.openlocfilehash: 7bd2efd35e0cd65c524a17a88f659e9b3838233f
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979618"
---
# <span data-ttu-id="4bf03-103">Microsoft Edge 對 Microsoft Defender 應用程式防護的支援。</span><span class="sxs-lookup"><span data-stu-id="4bf03-103">Microsoft Edge support for Microsoft Defender Application Guard</span></span>

<span data-ttu-id="4bf03-104">本文說明 Microsoft Edge 如何支援 Microsoft Defender 應用程式防護 (應用程式防護)。</span><span class="sxs-lookup"><span data-stu-id="4bf03-104">This article describes how Microsoft Edge supports Microsoft Defender Application Guard (Application Guard).</span></span>

> [!NOTE]
> <span data-ttu-id="4bf03-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4bf03-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="4bf03-106">概觀</span><span class="sxs-lookup"><span data-stu-id="4bf03-106">Overview</span></span>

<span data-ttu-id="4bf03-107">企業中的安全性架構師必須處理生產力與安全性之間的張力。</span><span class="sxs-lookup"><span data-stu-id="4bf03-107">Security architects in the enterprise must deal with the tension that exists between productivity and security.</span></span> <span data-ttu-id="4bf03-108">您可相當容易地鎖定瀏覽器，且只允許載入少數受信任的網站。</span><span class="sxs-lookup"><span data-stu-id="4bf03-108">It's relatively easy to lock down a browser and only allow a handful of trusted sites to load.</span></span> <span data-ttu-id="4bf03-109">這種方法可改善整體安全性狀態，但其生產力可能會降低。</span><span class="sxs-lookup"><span data-stu-id="4bf03-109">This approach will improve the overall security posture but is arguably less productive.</span></span> <span data-ttu-id="4bf03-110">如果您降低限制以提高生產力，則會提高風險度。</span><span class="sxs-lookup"><span data-stu-id="4bf03-110">If you make it less restrictive to improve productivity, you increase the risk profile.</span></span> <span data-ttu-id="4bf03-111">這是難以達到的平衡！</span><span class="sxs-lookup"><span data-stu-id="4bf03-111">It's a hard balance to strike!</span></span>

<span data-ttu-id="4bf03-112">在此不斷變化的威脅形勢中，我們更加難以掌握新興的威脅。</span><span class="sxs-lookup"><span data-stu-id="4bf03-112">It's even harder to keep up with new emerging threats in this constantly changing threat landscape.</span></span> <span data-ttu-id="4bf03-113">瀏覽器依舊是用戶端裝置上的主要受攻擊面，因為瀏覽器的基本任務是要讓使用者存取、下載和開啟不受信任來源中不受信任的內容。</span><span class="sxs-lookup"><span data-stu-id="4bf03-113">Browsers remain the primary attack surface on client devices because the browser's basic job is to let users access, download, and open untrusted content from untrusted sources.</span></span> <span data-ttu-id="4bf03-114">惡意行動者不斷鑽研針對瀏覽器的新型社交工程攻擊。</span><span class="sxs-lookup"><span data-stu-id="4bf03-114">Malicious actors are constantly working to social engineer new forms of attacks against the browser.</span></span> <span data-ttu-id="4bf03-115">安全性事件預防或偵測/回應策略無法保證 100% 安全。</span><span class="sxs-lookup"><span data-stu-id="4bf03-115">Security incident prevention or detection/response strategies can't guarantee 100% safety.</span></span>

<span data-ttu-id="4bf03-116">所要考量的重要安全戰略就是[採用破壞方法](https://docs.microsoft.com/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology)，這表示不論如何防範，都接受攻擊最少會成功一次。</span><span class="sxs-lookup"><span data-stu-id="4bf03-116">A key security strategy to consider is the [Assume Breach Methodology](https://docs.microsoft.com/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology), which means there's an acceptance that an attack is going to succeed at least once regardless of efforts to prevent it.</span></span> <span data-ttu-id="4bf03-117">此種思維需要建立防禦措施來遏制損害，以確保在此情況下公司網路和其他資源仍然受到保護。</span><span class="sxs-lookup"><span data-stu-id="4bf03-117">This mindset requires building defenses to contain the damage, which ensures that corporate network and other resources remain protected in this scenario.</span></span>  <span data-ttu-id="4bf03-118">為 Microsoft Edge 部署應用程式防護正好符合此策略。</span><span class="sxs-lookup"><span data-stu-id="4bf03-118">Deploying Application Guard for Microsoft Edge fits right into this strategy.</span></span>

## <span data-ttu-id="4bf03-119">關於應用程式防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-119">About Application Guard</span></span>

<span data-ttu-id="4bf03-120">應用程式防護專為 Windows 10 和 Microsoft Edge 設計，採用硬體隔離方法。</span><span class="sxs-lookup"><span data-stu-id="4bf03-120">Designed for Windows 10 and Microsoft Edge, Application Guard uses a hardware isolation approach.</span></span> <span data-ttu-id="4bf03-121">這種方法可讓不受信任的網站導覽在容器內啟動。</span><span class="sxs-lookup"><span data-stu-id="4bf03-121">This approach lets untrusted site navigation launch inside a container.</span></span> <span data-ttu-id="4bf03-122">硬體隔離可協助企業保護企業網路和資料，以防使用者造訪遭入侵或惡意的網站。</span><span class="sxs-lookup"><span data-stu-id="4bf03-122">Hardware isolation helps enterprises safeguard their corporate network and data in case users visit a site that is compromised or is malicious.</span></span>

<span data-ttu-id="4bf03-123">企業系統管理員可定義受信任的網站、雲端資源和內部網路。</span><span class="sxs-lookup"><span data-stu-id="4bf03-123">The enterprise administrator defines what are trusted sites, cloud resources, and internal networks.</span></span> <span data-ttu-id="4bf03-124">不在受信任的網站清單中的所有項目都會被視為不受信任。</span><span class="sxs-lookup"><span data-stu-id="4bf03-124">Everything that's not in the trusted sites list is considered untrusted.</span></span> <span data-ttu-id="4bf03-125">這些網站會與使用者裝置上的公司網路和資料隔離。</span><span class="sxs-lookup"><span data-stu-id="4bf03-125">These sites are isolated from the corporate network and data on the user's device.</span></span>

<span data-ttu-id="4bf03-126">如需詳細資訊，請參閱[什麼是應用程式防護？如何運作？](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)。</span><span class="sxs-lookup"><span data-stu-id="4bf03-126">For more information, see [What is Application Guard and how does it work?](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work).</span></span>

<span data-ttu-id="4bf03-127">下一個螢幕擷取畫面顯示應用程式防護的訊息範例，其中顯示使用者正在安全的空間中瀏覽。</span><span class="sxs-lookup"><span data-stu-id="4bf03-127">The next screenshot shows an example of Application Guard's message showing that the user is browsing in a safe space.</span></span>

![應用程式防護的安全瀏覽訊息](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <span data-ttu-id="4bf03-129">新功能</span><span class="sxs-lookup"><span data-stu-id="4bf03-129">What's new</span></span>

<span data-ttu-id="4bf03-130">新的 Microsoft Edge 瀏覽器中的應用程式防護支援具備與舊版 Microsoft Edge 同等的功能，且包含多項改善。</span><span class="sxs-lookup"><span data-stu-id="4bf03-130">Application Guard support in the new Microsoft Edge  browser has functional parity with Microsoft Edge Legacy and includes several improvements.</span></span>

### <span data-ttu-id="4bf03-131">容器內的延伸支援</span><span class="sxs-lookup"><span data-stu-id="4bf03-131">Extension support inside the container</span></span>

<span data-ttu-id="4bf03-132">容器內的延伸支援曾經是來自客戶的最熱門要求之一。</span><span class="sxs-lookup"><span data-stu-id="4bf03-132">Extension support inside the container has been one of the top requests from the customers.</span></span> <span data-ttu-id="4bf03-133">案例包含從想要在容器內執行廣告封鎖程式來提升瀏覽器效能，以至能夠在容器內執行自產的自訂延伸。</span><span class="sxs-lookup"><span data-stu-id="4bf03-133">Scenarios ranged from wanting to run ad-blockers inside the container to boost browser performance to having the ability to run custom home-grown extensions inside the container.</span></span>

<span data-ttu-id="4bf03-134">現在支援在容器中安裝延伸 (從 Microsoft Edge 版本 81 開始)。</span><span class="sxs-lookup"><span data-stu-id="4bf03-134">Extension installs in the container is now supported, starting from Microsoft Edge version 81.</span></span> <span data-ttu-id="4bf03-135">可透過原則控制這項支援。</span><span class="sxs-lookup"><span data-stu-id="4bf03-135">This support can be controlled via policy.</span></span> <span data-ttu-id="4bf03-136">在 [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) 原則中使用的 `updateURL`，應新增為應用程式防護所用網路隔離原則中的中性資源。</span><span class="sxs-lookup"><span data-stu-id="4bf03-136">The `updateURL` that gets used in [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy should be added as Neutral Resources in the Network Isolation policies used by Application Guard.</span></span>

<span data-ttu-id="4bf03-137">有些容器支援範例包含下列案例：</span><span class="sxs-lookup"><span data-stu-id="4bf03-137">Some examples of container support include the following scenarios:</span></span>

- <span data-ttu-id="4bf03-138">在主機上強制安裝延伸</span><span class="sxs-lookup"><span data-stu-id="4bf03-138">Force installs of an extension on the host</span></span>
- <span data-ttu-id="4bf03-139">從主機移除延伸</span><span class="sxs-lookup"><span data-stu-id="4bf03-139">Removing an extension from the host</span></span>
- <span data-ttu-id="4bf03-140">主機上封鎖的延伸</span><span class="sxs-lookup"><span data-stu-id="4bf03-140">Extensions blocked on the host</span></span>

> [!NOTE]
> <span data-ttu-id="4bf03-141">您也可從延伸存放區，在容器內手動安裝個別的延伸。</span><span class="sxs-lookup"><span data-stu-id="4bf03-141">It's also possible to manually install individual extensions inside the container from the extension store.</span></span> <span data-ttu-id="4bf03-142">啟用 [允許保留][](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) 原則後，只有手動安裝的延伸才會保留在容器中。</span><span class="sxs-lookup"><span data-stu-id="4bf03-142">Manually installed extensions will only persist in the container when [Allow Persistence](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) policy is enabled.</span></span>

### <span data-ttu-id="4bf03-143">透過雙 Proxy 識別應用程式防護流量</span><span class="sxs-lookup"><span data-stu-id="4bf03-143">Identifying Application Guard traffic via Dual Proxy</span></span>

<span data-ttu-id="4bf03-144">部分企業客戶正在部署適用于特定案例的應用程式防護，以便識別來自 Microsoft Defender 應用程式防護容器的 proxy 等級網路流量。</span><span class="sxs-lookup"><span data-stu-id="4bf03-144">Some enterprise customers are deploying Application Guard with a specific use case where they need to identify web traffic coming out of a Microsoft Defender Application Guard container at the proxy level.</span></span> <span data-ttu-id="4bf03-145">從穩定通道版本 84 開始，Microsoft Edge 將支援雙 proxy 來滿足這一需求。</span><span class="sxs-lookup"><span data-stu-id="4bf03-145">Starting with Stable Channel version 84, Microsoft Edge will support dual proxy to address this requirement.</span></span> <span data-ttu-id="4bf03-146">您可以使用 [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) 原則來設定此功能。</span><span class="sxs-lookup"><span data-stu-id="4bf03-146">You can configure this functionality using the [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy) policy.</span></span>

<span data-ttu-id="4bf03-147">下圖顯示 Microsoft Edge 的雙 proxy 架構。</span><span class="sxs-lookup"><span data-stu-id="4bf03-147">The following drawing shows the dual proxy architecture for Microsoft Edge.</span></span>

![應用程式防護的雙 proxy 架構](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <span data-ttu-id="4bf03-149">用於疑難排解的診斷頁面</span><span class="sxs-lookup"><span data-stu-id="4bf03-149">Diagnostic page for troubleshooting</span></span>

<span data-ttu-id="4bf03-150">另一個使用者痛點就是在問題回報後，針對裝置上的應用程式防護設定進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="4bf03-150">Another user pain point is troubleshooting the Application Guard configuration on a device when a problem is reported.</span></span> <span data-ttu-id="4bf03-151">Microsoft Edge 有診斷頁面 (`edge://application-guard-internals`) 可針對使用者問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="4bf03-151">Microsoft Edge has a diagnostics page (`edge://application-guard-internals`) to troubleshoot user issues.</span></span> <span data-ttu-id="4bf03-152">其中一項診斷可根據使用者裝置上的設定來檢查 URL 信任。</span><span class="sxs-lookup"><span data-stu-id="4bf03-152">One of these diagnostics is being able to check the URL trust based on the configuration on the user's device.</span></span>

<span data-ttu-id="4bf03-153">下一個螢幕擷取畫面顯示多個索引標籤診斷頁面，以協助診斷使用者回報告的裝置問題。</span><span class="sxs-lookup"><span data-stu-id="4bf03-153">The next screenshot shows a multiple tab diagnostics page to help diagnose user reported issues on the device.</span></span>

![應用程式防護診斷頁面](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <span data-ttu-id="4bf03-155">容器中的 Microsoft Edge 更新</span><span class="sxs-lookup"><span data-stu-id="4bf03-155">Microsoft Edge updates in the container</span></span>

<span data-ttu-id="4bf03-156">容器中的舊版 Microsoft Edge 更新是 Windows OS 更新週期的一部分。</span><span class="sxs-lookup"><span data-stu-id="4bf03-156">Microsoft Edge Legacy updates in the container are part of the Windows OS update cycle.</span></span> <span data-ttu-id="4bf03-157">由於新版 Microsoft Edge 更新本身與 Windows OS 無關，因此不再相依於容器更新。</span><span class="sxs-lookup"><span data-stu-id="4bf03-157">Because the new version of Microsoft Edge updates itself independent of the Windows OS, there is no longer any dependency on container updates.</span></span> <span data-ttu-id="4bf03-158">主機 Microsoft Edge 的通道和版本會在容器內複寫。</span><span class="sxs-lookup"><span data-stu-id="4bf03-158">The channel and version of the host Microsoft Edge is replicated inside the container.</span></span>

## <span data-ttu-id="4bf03-159">必要條件</span><span class="sxs-lookup"><span data-stu-id="4bf03-159">Prerequisites</span></span>

<span data-ttu-id="4bf03-160">下列需求適用於使用應用程式防護搭配 Microsoft Edge 的裝置：</span><span class="sxs-lookup"><span data-stu-id="4bf03-160">The following  requirements apply to devices using Application Guard with Microsoft Edge:</span></span>

- <span data-ttu-id="4bf03-161">Windows 10 1809 (RS5) 及以上版本。</span><span class="sxs-lookup"><span data-stu-id="4bf03-161">Windows 10 1809 (RS5) and above.</span></span>
- <span data-ttu-id="4bf03-162">僅限 Windows 用戶端 SKU</span><span class="sxs-lookup"><span data-stu-id="4bf03-162">Only Windows client SKUs</span></span>

  > [!NOTE]
  > <span data-ttu-id="4bf03-163">只有 Windows 10 專業版和 Windows 10 企業版 SKU 支援應用程式防護。</span><span class="sxs-lookup"><span data-stu-id="4bf03-163">Application Guard is only supported on Windows 10 Pro and Windows 10 Enterprise SKUs.</span></span>

- <span data-ttu-id="4bf03-164">[軟體需求](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)所述的其中一個管理解決方案</span><span class="sxs-lookup"><span data-stu-id="4bf03-164">One of the management solutions described in [Software requirements](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)</span></span>

## <span data-ttu-id="4bf03-165">如何安裝應用程式防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-165">How to install Application Guard</span></span>

<span data-ttu-id="4bf03-166">下列文章提供透過 Microsoft Edge 安裝、設定及測試應用程式防護所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="4bf03-166">The following articles provide the information you need to install, configure, and test Application Guard with Microsoft Edge.</span></span>

- [<span data-ttu-id="4bf03-167">系統需求</span><span class="sxs-lookup"><span data-stu-id="4bf03-167">System requirements</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [<span data-ttu-id="4bf03-168">安裝 Microsoft Defender 應用程式防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-168">Install Microsoft Defender Application Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [<span data-ttu-id="4bf03-169">設定 Microsoft Defender 群組原則設定</span><span class="sxs-lookup"><span data-stu-id="4bf03-169">Configure Microsoft Defender group policy settings</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [<span data-ttu-id="4bf03-170">測試應用程式防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-170">Test Application Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <span data-ttu-id="4bf03-171">常見問題集</span><span class="sxs-lookup"><span data-stu-id="4bf03-171">Frequently Asked Questions</span></span>

### <span data-ttu-id="4bf03-172">應用程式防護是否可在 IE 模式中運作？</span><span class="sxs-lookup"><span data-stu-id="4bf03-172">Does Application Guard work in IE Mode?</span></span>

<span data-ttu-id="4bf03-173">IE 模式支援應用程式防護功能，但我們不期望在 IE 模式中經常使用此功能。</span><span class="sxs-lookup"><span data-stu-id="4bf03-173">IE Mode supports Application Guard functionality, but we don't anticipate much use of this feature in IE Mode.</span></span> <span data-ttu-id="4bf03-174">建議針對一些受信任的內部網站部署 IE 模式，而應用程式防護只適用於不受信任的網站。</span><span class="sxs-lookup"><span data-stu-id="4bf03-174">IE Mode is recommended to be deployed for a list of trusted internal sites, and Application Guard is for untrusted sites only.</span></span> <span data-ttu-id="4bf03-175">確定所有 IE 模式網站或 IP 位址也會新增至網路隔離原則，使應用程式防護將其視為受信任的資源。</span><span class="sxs-lookup"><span data-stu-id="4bf03-175">Make sure all the IE mode sites or IP addresses are also added to the Network Isolation policy to be considered as trusted resource by Application Guard.</span></span>

### <span data-ttu-id="4bf03-176">我需要安裝應用程式防護 Chrome 延伸嗎？</span><span class="sxs-lookup"><span data-stu-id="4bf03-176">Do I need to install the Application Guard Chrome extension?</span></span>

<span data-ttu-id="4bf03-177">否，Microsoft Edge 本身就支援應用程式防護功能。</span><span class="sxs-lookup"><span data-stu-id="4bf03-177">No, the Application Guard feature is natively supported in Microsoft Edge.</span></span> <span data-ttu-id="4bf03-178">事實上，應用程式防護 Chrome 延伸不是 Microsoft Edge 中支援的設定。</span><span class="sxs-lookup"><span data-stu-id="4bf03-178">In fact, the Application Guard Chrome extension isn't a supported configuration in Microsoft Edge.</span></span>

### <span data-ttu-id="4bf03-179">是否有任何其他平台相關的常見問題集？</span><span class="sxs-lookup"><span data-stu-id="4bf03-179">Are there any other platform related FAQs?</span></span>

<span data-ttu-id="4bf03-180">是。</span><span class="sxs-lookup"><span data-stu-id="4bf03-180">Yes.</span></span> [<span data-ttu-id="4bf03-181">常見問答集─Microsoft Defender 應用程式防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-181">Frequently asked questions - Microsoft Defender Application Guard</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <span data-ttu-id="4bf03-182">請參閱</span><span class="sxs-lookup"><span data-stu-id="4bf03-182">See also</span></span>

- [<span data-ttu-id="4bf03-183">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="4bf03-183">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="4bf03-184">安全性概觀</span><span class="sxs-lookup"><span data-stu-id="4bf03-184">Security overview</span></span>](security-overview.md)
- [<span data-ttu-id="4bf03-185">Microsoft Defender 進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="4bf03-185">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
