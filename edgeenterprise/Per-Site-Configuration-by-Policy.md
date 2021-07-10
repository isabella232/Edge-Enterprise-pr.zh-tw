---
title: '依原則的每一網站設定 '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: '依原則的每一網站設定 '
ms.openlocfilehash: 4f1bf9a421f0098ba8105e78f77ac4af62530239
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641689"
---
# <a name="persite-configuration-by-policy"></a><span data-ttu-id="17dd6-103">依原則的每一網站設定</span><span class="sxs-lookup"><span data-stu-id="17dd6-103">PerSite Configuration by Policy</span></span>

## <a name="introduction-browsers-as-decision-makers"></a><span data-ttu-id="17dd6-104">簡介：瀏覽器做為決策者</span><span class="sxs-lookup"><span data-stu-id="17dd6-104">Introduction: Browsers as Decision Makers</span></span>

<span data-ttu-id="17dd6-105">隨著每個頁面載入的一部分，瀏覽器會進行許多決策，其中包括：特定 API 應該可供使用嗎？</span><span class="sxs-lookup"><span data-stu-id="17dd6-105">As a part of every page load, browsers make many decisions — should a particular API be available?</span></span> <span data-ttu-id="17dd6-106">應該允許資源載入嗎？</span><span class="sxs-lookup"><span data-stu-id="17dd6-106">Should a resource load be permitted?</span></span> <span data-ttu-id="17dd6-107">應該允許指令碼執行嗎？</span><span class="sxs-lookup"><span data-stu-id="17dd6-107">Should script be allowed to run?</span></span> <span data-ttu-id="17dd6-108">清單太長。</span><span class="sxs-lookup"><span data-stu-id="17dd6-108">The list is long.</span></span>

<span data-ttu-id="17dd6-109">在大部分情況下，決策是由兩個輸入所控管：使用者設定，以及進行決策的頁面 URL。</span><span class="sxs-lookup"><span data-stu-id="17dd6-109">In most cases, decisions are governed by two inputs: a user setting, and the URL of the page for which the decision is being made.</span></span>

<span data-ttu-id="17dd6-110">在舊版 Internet Explorer Web 平台中，這些決策都稱為  [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29)，而網際網路控制台內的企業群組原則和使用者設定會控制瀏覽器處理每個決策的方式。</span><span class="sxs-lookup"><span data-stu-id="17dd6-110">In the legacy Internet Explorer web platform, each of these decisions was called an [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29), and Enterprise Group Policy and user settings inside the Internet Control Panel controlled how the browser would handle each decision.</span></span>  

<span data-ttu-id="17dd6-111">在 Microsoft Edge 中，多數的每一網站權限是由使用簡單語法 (具有有限萬用字元支援) 表達的設定和原則所控制。</span><span class="sxs-lookup"><span data-stu-id="17dd6-111">In the Microsoft Edge, most per-site permissions are controlled by settings and policies expressed using a simple syntax with limited wild carding support.</span></span> <span data-ttu-id="17dd6-112">Windows 安全性區域仍只能用於少量的設定決策。</span><span class="sxs-lookup"><span data-stu-id="17dd6-112">Windows Security Zones are still used only for a small number of configuration decisions.</span></span>

## <a name="background-windows-security-zones"></a><span data-ttu-id="17dd6-113">背景：Windows 安全性區域</span><span class="sxs-lookup"><span data-stu-id="17dd6-113">Background: Windows Security Zones</span></span>

<span data-ttu-id="17dd6-114">為了簡化使用者或其系統管理員的設定，舊版平台將網站分類為五個不同的 **安全性區域**：本機電腦、近端內部網路、信任的網站、網際網路和限制的網站。</span><span class="sxs-lookup"><span data-stu-id="17dd6-114">To simplify configuration for the user or their administrator, the legacy platform classified sites into five different **Security Zones:** Local Machine, Local Intranet, Trusted, Internet, and Restricted Sites.</span></span>

<span data-ttu-id="17dd6-115">做出決策時，瀏覽器會先將網站對應至區域，然後查閱該區域的 URLAction 的設定，以決定該執行的動作。</span><span class="sxs-lookup"><span data-stu-id="17dd6-115">When making a decision, the browser would first map the website to a Zone, then consult the setting for that URLAction for that Zone to decide what to do.</span></span> <span data-ttu-id="17dd6-116">合理的預設值 (例如「自動滿足來自我的內部網路的驗證挑戰」) 表示多數使用者不需要變更任何預設值的設定。</span><span class="sxs-lookup"><span data-stu-id="17dd6-116">Reasonable defaults like “Automatically satisfy authentication challenges from my Intranet” meant that most users never needed to change any settings away from their defaults.</span></span>

<span data-ttu-id="17dd6-117">使用者可以使用網際網路控制台將特定網站指派給區域，並設定每個區域的權限結果。</span><span class="sxs-lookup"><span data-stu-id="17dd6-117">Users can use the Internet Control Panel to assign specific sites to Zones and to configure the permission results for each zone.</span></span> <span data-ttu-id="17dd6-118">在受管理環境中，系統管理員可以使用群組原則來為區域指派特定網站 (透過「指派網站到區域清單」原則)，並以每個區域為基礎指定 URLActions 的設定。</span><span class="sxs-lookup"><span data-stu-id="17dd6-118">In managed environments, administrators can use Group Policy to assign specific sites to Zones (via “Site to Zone Assignment List” policy) and specify the settings for URLActions on a per-zone basis.</span></span> <span data-ttu-id="17dd6-119">除了手動管理網站或將使用者網站指派至區域之外，其他啟發學習法可以 [將網站指派給近端內部網路區域](/archive/blogs/ieinternals/the-intranet-zone)。</span><span class="sxs-lookup"><span data-stu-id="17dd6-119">Beyond manual administrative or user assignment of sites to Zones, additional heuristics could [assign sites to the Local Intranet Zone](/archive/blogs/ieinternals/the-intranet-zone).</span></span> <span data-ttu-id="17dd6-120">特別是，無點的主機名稱 (例如 `http://payroll`) 為指派給內部網路區域。</span><span class="sxs-lookup"><span data-stu-id="17dd6-120">In particular, dotless host names (e.g. `http://payroll`) were assigned to the Intranet Zone.</span></span> <span data-ttu-id="17dd6-121">如果使用 Proxy 設定指令碼，設定為略過 Proxy 的任何網站都會對應至內部網路區域。</span><span class="sxs-lookup"><span data-stu-id="17dd6-121">If a Proxy Configuration script was used, any sites configured to bypass the proxy would be mapped to the Intranet Zone.</span></span>

<span data-ttu-id="17dd6-122">舊版 Microsoft Edge 繼承了其前身 Internet Explorer 的區域架構，並有一些簡化的變更：</span><span class="sxs-lookup"><span data-stu-id="17dd6-122">Microsoft Edge Legacy inherited the Zones architecture from its Internet Explorer predecessor with a few simplifying changes:</span></span>

- <span data-ttu-id="17dd6-123">Windows 的五個內建區域已減少為三個：網際網路 (網際網路)、信任 (內部網路+信任) 和本機電腦。</span><span class="sxs-lookup"><span data-stu-id="17dd6-123">Windows’ five built-in Zones were collapsed to three: Internet (Internet), Trusted (Intranet+Trusted), and Local Computer.</span></span> <span data-ttu-id="17dd6-124">已移除「限制的網站」區域。</span><span class="sxs-lookup"><span data-stu-id="17dd6-124">The Restricted Sites Zone was removed.</span></span>

- <span data-ttu-id="17dd6-125">區域到 URLAction 的對應已硬式編碼到瀏覽器，忽略網際網路控制台中的群組原則和設定。</span><span class="sxs-lookup"><span data-stu-id="17dd6-125">Zone to URLAction mappings were hardcoded into the browser, ignoring Group Policies and settings in the Internet Control Panel.</span></span>

## <a name="per-site-permissions-in-the-microsoft-edge"></a><span data-ttu-id="17dd6-126">Microsoft Edge 中的每一網站權限</span><span class="sxs-lookup"><span data-stu-id="17dd6-126">Per-Site Permissions in the Microsoft Edge</span></span>

<span data-ttu-id="17dd6-127">與其前身不同，新版 Microsoft Edge 對 Windows 安全性區域的使用非常有限。</span><span class="sxs-lookup"><span data-stu-id="17dd6-127">Unlike its predecessors, the new Microsoft Edge makes very limited use of Windows Security Zones.</span></span> <span data-ttu-id="17dd6-128">相反地，透過 [原則](/deployedge/microsoft-edge-policies)為系統管理員提供每一網站設定的多數權限和功能，都依賴於  [URL 篩選格式](/DeployEdge/edge-learnmmore-url-list-filter%20format)中的規則清單。</span><span class="sxs-lookup"><span data-stu-id="17dd6-128">Instead, most permissions and features that offer administrators per-site configuration via [policy](/deployedge/microsoft-edge-policies) rely on lists of rules in the [URL Filter Format](/DeployEdge/edge-learnmmore-url-list-filter%20format).</span></span>

<span data-ttu-id="17dd6-129">當使用者開啟 <code>edge://settings/content/siteDetails?site=https://example.com</code>時，他們會找到一長串設定參數的清單和各種權限的清單。</span><span class="sxs-lookup"><span data-stu-id="17dd6-129">When end-users open <code>edge://settings/content/siteDetails?site=https://example.com</code>, they’ll find a long list of configuration switches and lists for various permissions.</span></span> <span data-ttu-id="17dd6-130">使用者很少會直接使用設定頁面，而是在使用各種小工具瀏覽時進行選擇，並在 **頁面資訊** 下拉式清單 (當您按一下網址列中的鎖定圖示時會出現) 或透過網址列右側的各種提示或按鈕進行切換。</span><span class="sxs-lookup"><span data-stu-id="17dd6-130">Users rarely use the Settings Page directly, instead making choices while browsing using various widgets and toggles in the **Page Info** dropdown (which appears when you click the lock icon in the address bar) or via various prompts or buttons at the right-edge of the address bar.</span></span>

<span data-ttu-id="17dd6-131">企業可以使用群組原則，來為控制瀏覽器行為的個別原則佈建網站清單。</span><span class="sxs-lookup"><span data-stu-id="17dd6-131">Enterprises can use Group Policy to provision site lists for individual policies that control the browser’s behavior.</span></span> <span data-ttu-id="17dd6-132">若要尋找這些原則，只要開啟  [Microsoft Edge 群組原則文件](/deployedge/microsoft-edge-policies) 並搜尋 ForUrls \*\*\*\* ，即可尋找會根據所載入網站的 URL 來允許和封鎖行為的原則。</span><span class="sxs-lookup"><span data-stu-id="17dd6-132">To find these policies, simply open the [Microsoft Edge Group Policy documentation](/deployedge/microsoft-edge-policies) and search for **ForUrls** to find the policies that allow and block behavior based on the loaded site’s URL.</span></span> <span data-ttu-id="17dd6-133">大部分相關設定會在 [內容設定的群組原則](/deployedge/microsoft-edge-policies#content-settings)區段中列出。</span><span class="sxs-lookup"><span data-stu-id="17dd6-133">Most of the relevant settings are listed within the [Group Policy for Content Settings](/deployedge/microsoft-edge-policies#content-settings) section.</span></span>

<span data-ttu-id="17dd6-134">也有一些原則 (其名稱包含 **預設**) 可控制指定設定的預設行為。</span><span class="sxs-lookup"><span data-stu-id="17dd6-134">There are also a number of policies (whose names contain **Default**) that control the default behavior for a given setting.</span></span>

<span data-ttu-id="17dd6-135">許多設定非常模糊 (WebSerial、WebMIDI)，而且通常沒有理由變更預設值 (影像) 的設定。</span><span class="sxs-lookup"><span data-stu-id="17dd6-135">Many of the settings are very obscure (WebSerial, WebMIDI) and there’s very often no reason to change a setting away from the default (Images).</span></span>

## <a name="common-questions"></a><span data-ttu-id="17dd6-136">常見問題</span><span class="sxs-lookup"><span data-stu-id="17dd6-136">Common Questions</span></span>

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a><span data-ttu-id="17dd6-137">問：URL 篩選格式可比對網站的 IP 位址嗎？</span><span class="sxs-lookup"><span data-stu-id="17dd6-137">Q: Can the URL Filter Format match on a site’s IP address?</span></span>

<span data-ttu-id="17dd6-138">否，格式不支援指定允許和封鎖清單的 IP 範圍。</span><span class="sxs-lookup"><span data-stu-id="17dd6-138">No, the format does not support specifying an IP-range for allow and block lists.</span></span> <span data-ttu-id="17dd6-139">它確實支援指定個別 IP  **常值**，但只有在使用者使用上述常值 (例如  <http://127.0.0.1/>) 瀏覽至網站時，才會考慮這類規則。</span><span class="sxs-lookup"><span data-stu-id="17dd6-139">It does support specification of individual IP **literals**, but such rules are only respected if the user navigates to the site using said literal (e.g. <http://127.0.0.1/>).</span></span> <span data-ttu-id="17dd6-140">如果使用主機名稱 (<http://localhost>)，即使主機的解析 IP 符合篩選列出的 IP，也不會考慮 IP 常值規則。</span><span class="sxs-lookup"><span data-stu-id="17dd6-140">If a hostname is used (<http://localhost>), the IP Literal rule will not be respected even though the resolved IP of the host matches the filter-listed IP.</span></span>

## <a name="q-can-url-filters-matchjustdotless-host-names"></a><span data-ttu-id="17dd6-141">問：URL 篩選能夠僅比對無點的主機名稱嗎？</span><span class="sxs-lookup"><span data-stu-id="17dd6-141">Q: Can URL Filters match just dotless host names?</span></span>

<span data-ttu-id="17dd6-142">否。</span><span class="sxs-lookup"><span data-stu-id="17dd6-142">No.</span></span> <span data-ttu-id="17dd6-143">您必須個別列出每個需要的主機名稱，例如 (`https://payroll`、`https://stock`、`https://who` 等)。</span><span class="sxs-lookup"><span data-stu-id="17dd6-143">You must individually list each desired hostname, e.g. (`https://payroll`, `https://stock`, `https://who`, etc).</span></span>

<span data-ttu-id="17dd6-144">如果您足夠有前瞻性，而可以建立內部網路的結構，使得主機名稱格式為：</span><span class="sxs-lookup"><span data-stu-id="17dd6-144">If you were forward-thinking enough to structure your intranet such that your host names are of the form:</span></span>

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

<span data-ttu-id="17dd6-145">恭喜！您已實作最佳作法。</span><span class="sxs-lookup"><span data-stu-id="17dd6-145">Congratulations, you’ve implemented a best practice.</span></span> <span data-ttu-id="17dd6-146">您可以使用 \**_.contoso-intranet.com_* 專案來設定每個想要的政策，整個   內部網路都會加入。</span><span class="sxs-lookup"><span data-stu-id="17dd6-146">You can configure each desired policy with a \**_.contoso-intranet.com_* entry and your entire Intranet will be opted in.</span></span>

## <a name="use-of-security-zones-inthe-microsoft-edge"></a><span data-ttu-id="17dd6-147">使用 Microsoft Edge 中的安全性區域</span><span class="sxs-lookup"><span data-stu-id="17dd6-147">Use of Security Zones in the Microsoft Edge</span></span>

<span data-ttu-id="17dd6-148">雖然 Microsoft Edge 主要仰賴於使用 URL 篩選格式的個別原則，但它預設會持續在少數位置使用 Windows 的安全性區域，以簡化過去仰賴區域設定的企業內部署。</span><span class="sxs-lookup"><span data-stu-id="17dd6-148">While Microsoft Edge mostly relies upon individual policies using the URL Filter format, it continues to use Windows’ Security Zones by default in a small number of places in order to simplify deployment within Enterprises that have historically relied upon Zones configuration.</span></span> <span data-ttu-id="17dd6-149">下列行為是由區域原則控制：</span><span class="sxs-lookup"><span data-stu-id="17dd6-149">The following behaviors are controlled by Zone policy:</span></span>

1. <span data-ttu-id="17dd6-150">決定是否要自動釋出 Windows 整合式驗證 (Kerberos/NTLM) 認證時</span><span class="sxs-lookup"><span data-stu-id="17dd6-150">When deciding whether to release Windows Integrated Authentication (Kerberos/NTLM) credentials automatically</span></span>

2. <span data-ttu-id="17dd6-151">決定如何處理檔案下載時</span><span class="sxs-lookup"><span data-stu-id="17dd6-151">When deciding how to handle File Downloads</span></span>

3. <span data-ttu-id="17dd6-152">針對 Internet Explorer 模式</span><span class="sxs-lookup"><span data-stu-id="17dd6-152">For Internet Explorer Mode</span></span>

## <a name="credential-release"></a><span data-ttu-id="17dd6-153">釋出認證</span><span class="sxs-lookup"><span data-stu-id="17dd6-153">Credential Release</span></span>

<span data-ttu-id="17dd6-154">依預設，Microsoft Edge 會評估 URLACTION_CREDENTIALS_USE 以決定是否自動使用 Windows 整合式驗證，或是使用者應該改為看到手動驗證提示。</span><span class="sxs-lookup"><span data-stu-id="17dd6-154">By default, Microsoft Edge will evaluate URLACTION_CREDENTIALS_USE to decide whether Windows Integrated Authentication is used automatically, or the user should instead see a manual authentication prompt.</span></span> <span data-ttu-id="17dd6-155">設定 [AuthServerAllowlist 網站清單原則](/deployedge/microsoft-edge-policies#authserverallowlist)，將防止查閱區域原則。</span><span class="sxs-lookup"><span data-stu-id="17dd6-155">Configuring an [AuthServerAllowlist site list policy](/deployedge/microsoft-edge-policies#authserverallowlist) will prevent Zone Policy from being consulted.</span></span>

## <a name="file-downloads"></a><span data-ttu-id="17dd6-156">檔案下載</span><span class="sxs-lookup"><span data-stu-id="17dd6-156">File Downloads</span></span>

<span data-ttu-id="17dd6-157">從網際網路區域下載的檔案，會記錄其檔案下載來源的證據 (稱為[網路標記](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/))。</span><span class="sxs-lookup"><span data-stu-id="17dd6-157">Evidence about the origins of a file download (the so-called “[Mark of the Web](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/) is recorded for files downloaded from the Internet Zone.</span></span> <span data-ttu-id="17dd6-158">在決定如何處理檔案時，其他應用程式 (例如 Windows Shell、Microsoft Office 等) 可能會考慮此來源證據。</span><span class="sxs-lookup"><span data-stu-id="17dd6-158">Other applications (e.g. the Windows Shell, Microsoft Office, etc) may take this origin evidence into account when deciding how to handle a file.</span></span>

<span data-ttu-id="17dd6-159">如果 Windows 安全性區域原則設定為停用「啟動應用程式及不安全的檔案」設定，Microsoft Edge 下載管理員將會封鎖來自該區域中網站的檔案下載，並加上備註：「無法下載 - 已封鎖」。</span><span class="sxs-lookup"><span data-stu-id="17dd6-159">If the Windows Security Zone policy is configured to Disable the setting Launching applications and unsafe files, the Microsoft Edge download manager will block file downloads from sites in that Zone with a note: “Couldn’t download – Blocked.”</span></span>  

## <a name="ie-mode"></a><span data-ttu-id="17dd6-160">IE 模式</span><span class="sxs-lookup"><span data-stu-id="17dd6-160">IE mode</span></span>

<span data-ttu-id="17dd6-161">IE 模式可設定為 [以 IE 模式開啟所有內部網路網站](/deployedge/edge-ie-mode#configure-all-intranet-sites)。</span><span class="sxs-lookup"><span data-stu-id="17dd6-161">IE mode can be configured to [open all Intranet sites in IE mode](/deployedge/edge-ie-mode#configure-all-intranet-sites).</span></span> <span data-ttu-id="17dd6-162">使用此設定時，Edge 會在決定是否應該在 IE 模式中開啟時評估 URL 的區域。</span><span class="sxs-lookup"><span data-stu-id="17dd6-162">When in this configuration, Edge evaluates the Zone of a URL when deciding whether or not it should open in IE mode.</span></span> <span data-ttu-id="17dd6-163">除了此初始決策之外，IE 模式索引標籤會實際執行 Internet Explorer，因此，其會評估每個原則決策的區域設定，正如同 Internet Explorer 本身所做的一般。</span><span class="sxs-lookup"><span data-stu-id="17dd6-163">Beyond this initial decision, IE mode tabs are really running Internet Explorer, and as a consequence they evaluate Zones settings for every policy decision just as Internet Explorer itself did.</span></span>

## <a name="summary"></a><span data-ttu-id="17dd6-164">摘要</span><span class="sxs-lookup"><span data-stu-id="17dd6-164">Summary</span></span>

<span data-ttu-id="17dd6-165">在大部分情況下，可以將 Microsoft Edge 設定保留為其預設值。</span><span class="sxs-lookup"><span data-stu-id="17dd6-165">In most cases, Microsoft Edge settings can be left at their defaults.</span></span> <span data-ttu-id="17dd6-166">想要變更所有網站或特定網站預設值的系統管理員，可以使用適當的群組原則來指定網站清單或預設行為。</span><span class="sxs-lookup"><span data-stu-id="17dd6-166">Administrators who wish to change the defaults for all sites or specific sites can use the appropriate Group Policies to specify Site Lists or default behaviors.</span></span> <span data-ttu-id="17dd6-167">在少數情況下 (認證釋出、檔案下載和 IE 模式)，系統管理員會透過設定 Windows 安全性區域設定，以繼續控制行為。</span><span class="sxs-lookup"><span data-stu-id="17dd6-167">In a handful of cases (credential release, file download, and IE mode), administrators will continue to control behavior by configuring Windows Security Zones settings.</span></span>
