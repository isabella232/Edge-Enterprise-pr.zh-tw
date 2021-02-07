---
title: Microsoft Defender SmartScreen 的 Microsoft Edge 支援
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Defender SmartScreen 的 Microsoft Edge 支援
ms.openlocfilehash: 2de93b4ebe26b4a90592f7ee9143f6f775b682ce
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314686"
---
# <span data-ttu-id="c8f27-103">Microsoft Defender SmartScreen 的 Microsoft Edge 支援</span><span class="sxs-lookup"><span data-stu-id="c8f27-103">Microsoft Edge support for Microsoft Defender SmartScreen</span></span>

<span data-ttu-id="c8f27-104">本文說明使用 Microsoft Defender SmartScreen 的優點，說明其運作方式，並說明如何設定此 Microsoft Edge 功能。</span><span class="sxs-lookup"><span data-stu-id="c8f27-104">This article describes the benefits of using Microsoft Defender SmartScreen, explains how it works, and describes how to configure this Microsoft Edge feature.</span></span>

> [!NOTE]
> <span data-ttu-id="c8f27-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c8f27-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="c8f27-106">Microsoft Defender SmartScreen 是一項服務，Microsoft Edge 用來在您瀏覽網頁時保護您的安全。</span><span class="sxs-lookup"><span data-stu-id="c8f27-106">Microsoft Defender SmartScreen is a service that Microsoft Edge uses to keep you safe while you browse the web.</span></span> <span data-ttu-id="c8f27-107">Microsoft Defender SmartScreen 可針對可能從事網路釣魚攻擊或嘗試透過聚焦攻擊散佈惡意程式碼的網站，協助提供一套早期警告系統。</span><span class="sxs-lookup"><span data-stu-id="c8f27-107">Microsoft Defender SmartScreen provides an early warning system against websites that might engage in phishing attacks or attempt to distribute malware through a focused attack.</span></span> <span data-ttu-id="c8f27-108">如需詳細資訊，請觀看[影片：在 Microsoft Edge 上安全瀏覽](microsoft-edge-video-security-smartscreen.md)。</span><span class="sxs-lookup"><span data-stu-id="c8f27-108">For more information, watch [Video: Secure browsing on Microsoft Edge](microsoft-edge-video-security-smartscreen.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c8f27-109">在 Windows 10 版本 1703 之前，搭配瀏覽器和 Microsoft SmartScreen 篩選工具於瀏覽器之外使用時，此功能稱為「SmartScreen 篩選工具」。</span><span class="sxs-lookup"><span data-stu-id="c8f27-109">Before Windows 10, version 1703, this feature was called the SmartScreen filter when used within the browser and Microsoft SmartScreen when used outside of the browser.</span></span>

## <span data-ttu-id="c8f27-110">Microsoft Defender SmartScreen 的優點</span><span class="sxs-lookup"><span data-stu-id="c8f27-110">The benefits of Microsoft Defender SmartScreen</span></span>

<span data-ttu-id="c8f27-111">Microsoft Defender SmartScreen 提供數個優點，如下列清單所述。</span><span class="sxs-lookup"><span data-stu-id="c8f27-111">Microsoft Defender SmartScreen provides several benefits, which are summarized in the following list.</span></span> <span data-ttu-id="c8f27-112">在 [Microsoft Defender SmartScreen 文件](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen)中詳細說明這些優點。</span><span class="sxs-lookup"><span data-stu-id="c8f27-112">These benefits are described in detail in the [Microsoft Defender SmartScreen documentation](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen).</span></span> <span data-ttu-id="c8f27-113">優點如下：</span><span class="sxs-lookup"><span data-stu-id="c8f27-113">The benefits are:</span></span>

- <span data-ttu-id="c8f27-114">防網路釣魚和反惡意程式碼的支援</span><span class="sxs-lookup"><span data-stu-id="c8f27-114">Anti-phishing and anti-malware support</span></span>
- <span data-ttu-id="c8f27-115">以信譽為基礎的 URL 和應用程式保護</span><span class="sxs-lookup"><span data-stu-id="c8f27-115">Reputation-based URL and app protection</span></span>
- <span data-ttu-id="c8f27-116">作業系統整合</span><span class="sxs-lookup"><span data-stu-id="c8f27-116">Operating system integration</span></span>
- <span data-ttu-id="c8f27-117">已改善啟發學習與診斷資料</span><span class="sxs-lookup"><span data-stu-id="c8f27-117">Improved heuristics and diagnostic data</span></span>
- <span data-ttu-id="c8f27-118">透過群組原則和 Microsoft Intune 進行管理</span><span class="sxs-lookup"><span data-stu-id="c8f27-118">Management through Group Policy and Microsoft Intune</span></span>
- <span data-ttu-id="c8f27-119">封鎖與可能不需要的應用程式相關聯的 URL</span><span class="sxs-lookup"><span data-stu-id="c8f27-119">Blocking URLs associated with potentially unwanted applications</span></span>

## <span data-ttu-id="c8f27-120">了解 Microsoft Defender SmartScreen 如何運作</span><span class="sxs-lookup"><span data-stu-id="c8f27-120">Understand how Microsoft Defender SmartScreen works</span></span>

<span data-ttu-id="c8f27-121">許多輸入都會造成 Microsoft Defender SmartScreen 警告。</span><span class="sxs-lookup"><span data-stu-id="c8f27-121">A number of inputs contribute to Microsoft Defender SmartScreen warnings.</span></span> <span data-ttu-id="c8f27-122">資料會從許多來源接收，包括使用者意見反應、資料提供者和情報模型。</span><span class="sxs-lookup"><span data-stu-id="c8f27-122">Data is received from many sources, including user feedback, data providers, and intelligence models.</span></span> <span data-ttu-id="c8f27-123">此資料可用於協助識別潛在惡意的內容。</span><span class="sxs-lookup"><span data-stu-id="c8f27-123">This data is used to help identify potentially malicious content.</span></span> <span data-ttu-id="c8f27-124">Microsoft Defender SmartScreen 也會檢查下載的應用程式或應用程式安裝程式，查看是否為惡意。</span><span class="sxs-lookup"><span data-stu-id="c8f27-124">Microsoft Defender SmartScreen also checks downloaded apps or app installers to see if they're malicious.</span></span> <span data-ttu-id="c8f27-125">在這兩個情況下，Microsoft Defender SmartScreen 會相應地警示使用者可疑的內容。</span><span class="sxs-lookup"><span data-stu-id="c8f27-125">In both scenarios, Microsoft Defender SmartScreen warns users appropriately about suspicious content.</span></span>

### <span data-ttu-id="c8f27-126">網站分析</span><span class="sxs-lookup"><span data-stu-id="c8f27-126">Site analysis</span></span>

<span data-ttu-id="c8f27-127">Microsoft Defender SmartScreen 會透過下列方式來判斷網站是否為潛在惡意網站：</span><span class="sxs-lookup"><span data-stu-id="c8f27-127">Microsoft Defender SmartScreen determines whether a site is potentially malicious by:</span></span>

- <span data-ttu-id="c8f27-128">分析已造訪的網頁，找出可疑行為的指示。</span><span class="sxs-lookup"><span data-stu-id="c8f27-128">Analyzing visited webpages for indications of suspicious behavior.</span></span>
- <span data-ttu-id="c8f27-129">對照所報告網路釣魚網站的動態清單，檢查造訪的網站。</span><span class="sxs-lookup"><span data-stu-id="c8f27-129">Checking the visited sites against a dynamic record of reported phishing sites.</span></span>

<span data-ttu-id="c8f27-130">如果 Microsoft Defender SmartScreen 認為頁面為惡意，則會顯示警告頁面，通知使用者該網站回報為不安全。</span><span class="sxs-lookup"><span data-stu-id="c8f27-130">If Microsoft Defender SmartScreen determines that a page is malicious, it will show a warning page to notify the user that that site is reported as unsafe.</span></span> <span data-ttu-id="c8f27-131">以下螢幕擷取畫面顯示當使用者嘗試開啟惡意網站時，出現的 Microsoft Defender SmartScreen 警告頁面範例。</span><span class="sxs-lookup"><span data-stu-id="c8f27-131">The next screenshot shows an example of a Microsoft Defender SmartScreen warning page when a user tries to open a malicious website.</span></span>

![連結至外部網站的 Microsoft Defender SmartScreen 封鎖頁面](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

<span data-ttu-id="c8f27-133">使用者可在警告訊息中選擇將網站回報為安全或不安全。</span><span class="sxs-lookup"><span data-stu-id="c8f27-133">Users are given the option of reporting a site as safe or unsafe within the warning message.</span></span> <span data-ttu-id="c8f27-134">如需詳細資訊，請參閱[如何報告網站](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe)。</span><span class="sxs-lookup"><span data-stu-id="c8f27-134">For more information, see [how to report a site](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe).</span></span>

### <span data-ttu-id="c8f27-135">檔案分析</span><span class="sxs-lookup"><span data-stu-id="c8f27-135">File analysis</span></span>

<span data-ttu-id="c8f27-136">Microsoft Defender SmartScreen 會根據許多標準 (例如下載流量、下載歷史記錄、過去的防毒結果和 URL 信譽) 判斷下載的應用程式或應用程式安裝程式是否有潛在惡意。</span><span class="sxs-lookup"><span data-stu-id="c8f27-136">Microsoft Defender SmartScreen determines whether a downloaded app or app installer is potentially malicious based on many criteria, such as download traffic, download history, past anti-virus results, and URL reputation.</span></span>

- <span data-ttu-id="c8f27-137">含有已知安全信譽的檔案，將會下載檔案而不出現通知。</span><span class="sxs-lookup"><span data-stu-id="c8f27-137">Files with a known safe reputation will download without any notification.</span></span>  
- <span data-ttu-id="c8f27-138">將針對含有已知惡意信譽的檔案顯示警告，讓使用者知道該檔案不安全，且已報告為惡意。</span><span class="sxs-lookup"><span data-stu-id="c8f27-138">Files with a known malicious reputation show a warning to let the user know that the file is unsafe and has been reported as malicious.</span></span> <span data-ttu-id="c8f27-139">以下螢幕擷取畫面是惡意檔案的警告範例。</span><span class="sxs-lookup"><span data-stu-id="c8f27-139">The next screenshot is an example of a warning for a malicious file.</span></span>

  ![含有惡意信譽檔案的 Microsoft Defender SmartScreen 封鎖通知](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- <span data-ttu-id="c8f27-141">未知的檔案則會顯示警告，讓使用者知道該下載項目沒有已知的足跡，並建議使用者注意。</span><span class="sxs-lookup"><span data-stu-id="c8f27-141">Files that are unknown show a warning to let the user know that the download doesn't have a known footprint and advise caution.</span></span> <span data-ttu-id="c8f27-142">以下螢幕擷取畫面是未知檔案的警告範例。</span><span class="sxs-lookup"><span data-stu-id="c8f27-142">The next screenshot is an example of a warning for an unknown file.</span></span>

  ![含有未知信譽檔案的 Microsoft Defender SmartScreen 封鎖通知](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

<span data-ttu-id="c8f27-144">並非所有未知程式都是惡意的，且未知警告是為需要的使用者提供內容和指導，特別是如果警告是非預期的。</span><span class="sxs-lookup"><span data-stu-id="c8f27-144">Not all unknown programs are malicious, and the unknown warning is intended to provide context and guidance for users who need it, especially if the warning is unexpected.</span></span>

  ![保留具有惡意信譽的檔案](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

<span data-ttu-id="c8f27-146">不過，使用者仍然可以下載並執行應用程式，方法是按一下 [...] | [保留] | [顯示更多] | [繼續]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="c8f27-146">However, users can still download and run the application by clicking **... | Keep | Show More | Keep anyway**.</span></span>

> [!TIP]
> **<span data-ttu-id="c8f27-147">僅參考，這適用企業客戶。</span><span class="sxs-lookup"><span data-stu-id="c8f27-147">FYI for Enterprise Customers.</span></span>** <span data-ttu-id="c8f27-148">根據預設，Microsoft Defender SmartScreen 會讓使用者略過警告。</span><span class="sxs-lookup"><span data-stu-id="c8f27-148">By default, Microsoft Defender SmartScreen lets users bypass warnings.</span></span> <span data-ttu-id="c8f27-149">因為此使用者的互動可能會造成風險，建議您檢閱這些[建議的群組原則設定](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization)。</span><span class="sxs-lookup"><span data-stu-id="c8f27-149">Because this user interaction is potentially risky, we recommend that you review these [recommended group policy settings](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization).</span></span>

<span data-ttu-id="c8f27-150">您看到 Microsoft Defender SmartScreen 如何使用[示範網站](https://demo.smartscreen.msft.net/)回應不同的案例。</span><span class="sxs-lookup"><span data-stu-id="c8f27-150">You see how Microsoft Defender SmartScreen responds to different scenarios using our [demo site](https://demo.smartscreen.msft.net/).</span></span>

## <span data-ttu-id="c8f27-151">Microsoft Defender SmartScreen 和使用者隱私權</span><span class="sxs-lookup"><span data-stu-id="c8f27-151">Microsoft Defender SmartScreen and user privacy</span></span>

<span data-ttu-id="c8f27-152">Microsoft Defender SmartScreen 可在使用者使用信譽檢查系統來瀏覽網際網路時保護使用者。</span><span class="sxs-lookup"><span data-stu-id="c8f27-152">Microsoft Defender SmartScreen protects users while they browse the Internet by using a reputation check system.</span></span> <span data-ttu-id="c8f27-153">Microsoft Edge 會將 URL 或檔案的相關資訊傳送到 Microsoft Defender SmartScreen 服務，以開始信譽檢查。</span><span class="sxs-lookup"><span data-stu-id="c8f27-153">Microsoft Edge passes relevant information about the URL or file to the Microsoft Defender SmartScreen service to start the reputation check.</span></span> <span data-ttu-id="c8f27-154">該檢查會對照已知危險的網站和檔案的動態清單來比較網站或檔案。</span><span class="sxs-lookup"><span data-stu-id="c8f27-154">The check compares the website or file against dynamic lists of sites and files that are known to be dangerous.</span></span> <span data-ttu-id="c8f27-155">所有對 Microsoft Defender SmartScreen 服務要求都是以 TLS 加密的方式進行。</span><span class="sxs-lookup"><span data-stu-id="c8f27-155">All requests to the Microsoft Defender SmartScreen service are made with TLS encryption.</span></span> <span data-ttu-id="c8f27-156">服務會傳回信譽檢查的結果，這可能會導致 Microsoft Edge 顯示網站或檔案的警告。</span><span class="sxs-lookup"><span data-stu-id="c8f27-156">The service returns the results of the reputation check, which might lead to Microsoft Edge showing a warning for the site or file.</span></span> <span data-ttu-id="c8f27-157">這些結果會儲存在裝置的本機上。</span><span class="sxs-lookup"><span data-stu-id="c8f27-157">These results are stored locally on the device.</span></span>

<span data-ttu-id="c8f27-158">Microsoft Defender SmartScreen 服務會儲存信譽檢查的相關資料。</span><span class="sxs-lookup"><span data-stu-id="c8f27-158">The Microsoft Defender SmartScreen service stores data about reputation checks.</span></span> <span data-ttu-id="c8f27-159">隨著新網站的發現，服務會將資料新增至已知惡意 URL 和檔案的動態資料庫。</span><span class="sxs-lookup"><span data-stu-id="c8f27-159">As new sites are identified, the service adds to a dynamic database of known malicious URLs and files.</span></span> <span data-ttu-id="c8f27-160">此資料會儲存在安全的 Microsoft 伺服器上，並僅用於 Microsoft 安全性服務。</span><span class="sxs-lookup"><span data-stu-id="c8f27-160">This data is stored on secure Microsoft servers and is only used for Microsoft security services.</span></span> <span data-ttu-id="c8f27-161">此資料永遠不會用來以任何方式識別或鎖定使用者。</span><span class="sxs-lookup"><span data-stu-id="c8f27-161">This data will never be used to identify or target users in any way.</span></span> <span data-ttu-id="c8f27-162">清除瀏覽快取會清除所有本機儲存的 Microsoft Defender SmartScreen URL 資料。</span><span class="sxs-lookup"><span data-stu-id="c8f27-162">Clearing browsing cache clears all locally stored Microsoft Defender SmartScreen URL data.</span></span> <span data-ttu-id="c8f27-163">清除下載歷史記錄將會移除有關檔案下載的任何本機儲存的 SmartScreen 資料。</span><span class="sxs-lookup"><span data-stu-id="c8f27-163">Clearing download history will remove any locally stored SmartScreen data about file downloads.</span></span>

<span data-ttu-id="c8f27-164">如需 Microsoft Defender SmartScreen 和 Microsoft Edge 上隱私權的詳細資訊，請參閱 [Microsoft Edge 隱私權白皮書](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#smartscreen)。</span><span class="sxs-lookup"><span data-stu-id="c8f27-164">For more information about Microsoft Defender SmartScreen and privacy on Microsoft Edge, read the [Microsoft Edge Privacy Whitepaper](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#smartscreen).</span></span>

## <span data-ttu-id="c8f27-165">系統管理員的 Microsoft Defender SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="c8f27-165">Microsoft Defender SmartScreen setup for admins</span></span>

<span data-ttu-id="c8f27-166">系統管理員可以使用群組原則、Microsoft Intune 或行動裝置管理 (MDM) 設定來設定 Microsoft Defender SmartScreen。</span><span class="sxs-lookup"><span data-stu-id="c8f27-166">Admins can configure Microsoft Defender SmartScreen using Group Policy, Microsoft Intune, or mobile device management (MDM) settings.</span></span> <span data-ttu-id="c8f27-167">根據您設定 Microsoft Defender SmartScreen 的方式，您可以向使用者顯示一個警告頁面，並且讓他們繼續移至網站，或是可以封鎖整個網站。</span><span class="sxs-lookup"><span data-stu-id="c8f27-167">Based on how you set up Microsoft Defender SmartScreen, you can show users a warning page and let them continue to the site or block the site entirely.</span></span>

### <span data-ttu-id="c8f27-168">使用群組原則設定 Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="c8f27-168">Microsoft Defender SmartScreen set up using Group Policy</span></span>

<span data-ttu-id="c8f27-169">如需 SmartScreen 原則的完整清單，請參閱 [Microsoft Defender SmartScreen 設定](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)</span><span class="sxs-lookup"><span data-stu-id="c8f27-169">For a complete list of SmartScreen policies, see [Microsoft Defender SmartScreen settings](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)</span></span>

### <span data-ttu-id="c8f27-170">使用 MDM 設定 Microsoft Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="c8f27-170">Microsoft Defender SmartScreen set up using MDM</span></span>

<span data-ttu-id="c8f27-171">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="c8f27-171">For more information, see:</span></span>

- [<span data-ttu-id="c8f27-172">Microsoft Defender SmartScreen 的 Windows Intune 設定</span><span class="sxs-lookup"><span data-stu-id="c8f27-172">Windows Intune settings for Microsoft Defender SmartScreen</span></span>](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [<span data-ttu-id="c8f27-173">MDM 原則設定</span><span class="sxs-lookup"><span data-stu-id="c8f27-173">MDM policy settings</span></span>](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## <span data-ttu-id="c8f27-174">使用者的 Microsoft Defender SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="c8f27-174">Microsoft Defender SmartScreen setup for users</span></span>

<span data-ttu-id="c8f27-175">預設會針對 Microsoft Edge 開啟 Microsoft Defender SmartScreen。</span><span class="sxs-lookup"><span data-stu-id="c8f27-175">Microsoft Defender SmartScreen is turned on by default for Microsoft Edge.</span></span> <span data-ttu-id="c8f27-176">若要關閉 Microsoft Defender SmartScreen，請移至 *edge://settings/privacy > [服務] > [Microsoft Defender SmartScreen]*。</span><span class="sxs-lookup"><span data-stu-id="c8f27-176">To turn off Microsoft Defender SmartScreen, go to *edge://settings/privacy > Services > Microsoft Defender SmartScreen*.</span></span> <span data-ttu-id="c8f27-177">此設定與裝置上的 Microsoft Edge 安裝相關聯的所有設定檔都是相同的。</span><span class="sxs-lookup"><span data-stu-id="c8f27-177">This setting is the same for all profiles associated with the installation of Microsoft Edge on a device.</span></span> <span data-ttu-id="c8f27-178">此設定不會在裝置間同步。</span><span class="sxs-lookup"><span data-stu-id="c8f27-178">This setting is not synced across devices.</span></span> <span data-ttu-id="c8f27-179">此設定適用於 InPrivate 瀏覽和來賓模式。</span><span class="sxs-lookup"><span data-stu-id="c8f27-179">The setting applies to InPrivate browsing and Guest mode.</span></span> <span data-ttu-id="c8f27-180">如果裝置是使用組織設定的群組原則管理，則會在 *edge://settings/privacy* 中反映該組態。</span><span class="sxs-lookup"><span data-stu-id="c8f27-180">If a device is managed with group policies set by an organization, this configuration will be reflected in *edge://settings/privacy*.</span></span>

> [!NOTE]
> <span data-ttu-id="c8f27-181">使用者可以為個別裝置設定 Microsoft Defender SmartScreen，除非群組原則或 MDM 已設定為防止它。</span><span class="sxs-lookup"><span data-stu-id="c8f27-181">Users can set up Microsoft Defender SmartScreen for an individual device unless Group Policy or MDM is configured to prevent it.</span></span> <span data-ttu-id="c8f27-182">如需詳細資訊，請參閱[在個別裝置上設定和使用 Microsoft Defender SmartScreen](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device)。</span><span class="sxs-lookup"><span data-stu-id="c8f27-182">For more information, see [set up and use Microsoft Defender SmartScreen on individual devices](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device).</span></span>

## <span data-ttu-id="c8f27-183">常見問題集</span><span class="sxs-lookup"><span data-stu-id="c8f27-183">Frequently asked questions</span></span>

### <span data-ttu-id="c8f27-184">信譽檢查系統如何運作？</span><span class="sxs-lookup"><span data-stu-id="c8f27-184">How does the reputation check system work?</span></span>

<span data-ttu-id="c8f27-185">當您瀏覽網頁時，Microsoft Defender SmartScreen 會將網站和下載內容分類為前幾大流量、危險或未知。</span><span class="sxs-lookup"><span data-stu-id="c8f27-185">As you browse the web, Microsoft Defender SmartScreen categorizes websites and downloads as top traffic, dangerous, or unknown.</span></span> <span data-ttu-id="c8f27-186">前幾大流量是 Microsoft Defender SmartScreen 判斷值得信任的熱門網站。</span><span class="sxs-lookup"><span data-stu-id="c8f27-186">Top traffic is popular sites that Microsoft Defender SmartScreen has determined are trustworthy.</span></span> <span data-ttu-id="c8f27-187">如果您前往標示為危險的網站，Microsoft Defender SmartScreen 會立即阻止您存取該網站。</span><span class="sxs-lookup"><span data-stu-id="c8f27-187">If you go to a site marked as dangerous, Microsoft Defender SmartScreen immediately blocks you from accessing the site.</span></span> <span data-ttu-id="c8f27-188">當您前往未知網站時，Microsoft DefenderSmartScreen 會檢查其信譽，以判斷您是否應該存取該網站。</span><span class="sxs-lookup"><span data-stu-id="c8f27-188">When you go to an unknown site, Microsoft DefenderSmartScreen checks its reputation to determine if you should access the site.</span></span>

## <span data-ttu-id="c8f27-189">請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f27-189">See also</span></span>

- [<span data-ttu-id="c8f27-190">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="c8f27-190">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c8f27-191">影片：在 Microsoft Edge 上安全瀏覽</span><span class="sxs-lookup"><span data-stu-id="c8f27-191">Video: Secure browsing on Microsoft Edge</span></span>](microsoft-edge-video-security-smartscreen.md)
- [<span data-ttu-id="c8f27-192">Microsoft Defender SmartScreen 概觀</span><span class="sxs-lookup"><span data-stu-id="c8f27-192">Microsoft Defender SmartScreen Overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [<span data-ttu-id="c8f27-193">威脅防護</span><span class="sxs-lookup"><span data-stu-id="c8f27-193">Threat protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/index)
- [<span data-ttu-id="c8f27-194">防護抵禦可能不需要的應用程式</span><span class="sxs-lookup"><span data-stu-id="c8f27-194">Protect against potentially unwanted applications</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-potentially-unwanted-apps)