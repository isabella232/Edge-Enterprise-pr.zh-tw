---
title: Microsoft Edge 對 Windows 資訊保護的支援
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2029
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 對 Windows 資訊保護的支援
ms.openlocfilehash: 53564d6089e84969501ac4802cf96dbdb1b24361
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642239"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a><span data-ttu-id="2c9ff-103">Microsoft Edge 對 Windows 資訊保護 (WIP) 的支援</span><span class="sxs-lookup"><span data-stu-id="2c9ff-103">Microsoft Edge support for Windows Information Protection (WIP)</span></span>

<span data-ttu-id="2c9ff-104">本文說明 Microsoft Edge 如何支援 Windows 資訊保護 (WIP)。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-104">This article describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span>

> [!NOTE]
> <span data-ttu-id="2c9ff-105">本文適用於 Microsoft Edge 版本 81 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-105">This applies to Microsoft Edge version 81 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="2c9ff-106">概觀</span><span class="sxs-lookup"><span data-stu-id="2c9ff-106">Overview</span></span>

<span data-ttu-id="2c9ff-107">Windows 資訊保護 (WIP) 是 Windows 10 的功能，可協助保護企業資料免於受到未經授權或意外的洩露。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-107">Windows Information Protection (WIP) is a Windows 10 feature that helps protect enterprise data from unauthorized or accidental disclosure.</span></span> <span data-ttu-id="2c9ff-108">隨著遠端工作的增加，在工作場所以外共用公司資料的風險也增加了。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-108">With the rise of remote work, there's an increased risk of sharing corporate data outside the workplace.</span></span> <span data-ttu-id="2c9ff-109">當公司裝置上存在個人活動和工作活動時，這種風險就會增加。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-109">This risk increases when personal activities and work activities occur on corporate devices.</span></span>

<span data-ttu-id="2c9ff-110">Microsoft Edge 支援使用 WIP 來協助保護 Web 環境中的內容，因為使用者通常是在 Web 環境中共用和散布內容。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-110">Microsoft Edge supports WIP to help protect content in a web environment where users often share and distribute content.</span></span>

### <a name="system-requirements"></a><span data-ttu-id="2c9ff-111">系統需求</span><span class="sxs-lookup"><span data-stu-id="2c9ff-111">System requirements</span></span>

<span data-ttu-id="2c9ff-112">下列需求適用於企業中使用 WIP 的裝置：</span><span class="sxs-lookup"><span data-stu-id="2c9ff-112">The follow requirements apply to devices using WIP in the enterprise:</span></span>

- <span data-ttu-id="2c9ff-113">Windows 10 (版本 1607) 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2c9ff-113">Windows 10, version 1607 or later</span></span>
- <span data-ttu-id="2c9ff-114">僅限 Windows 用戶端 SKU</span><span class="sxs-lookup"><span data-stu-id="2c9ff-114">Only Windows client SKUs</span></span>
- <span data-ttu-id="2c9ff-115">[WIP 必要條件](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)所述的其中一個管理解決方案</span><span class="sxs-lookup"><span data-stu-id="2c9ff-115">One of the management solutions described in [WIP prerequisites](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)</span></span>

### <a name="windows-information-protection-benefits"></a><span data-ttu-id="2c9ff-116">Windows 資訊保護的優點</span><span class="sxs-lookup"><span data-stu-id="2c9ff-116">Windows Information Protection benefits</span></span>

<span data-ttu-id="2c9ff-117">WIP 有下列優點：</span><span class="sxs-lookup"><span data-stu-id="2c9ff-117">WIP provides the following benefits:</span></span>

- <span data-ttu-id="2c9ff-118">清楚區分個人和公司資料，而不需要員工切換環境或應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-118">Obvious separation between personal and corporate data, without requiring employees to switch environments or apps.</span></span>
- <span data-ttu-id="2c9ff-119">為現有的商務應用程式組合提供額外的資料保護，而不需要更新應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-119">Additional data protection for existing line-of-business apps without a need to update the apps.</span></span>
- <span data-ttu-id="2c9ff-120">可從遠端抹除 Intune 行動裝置管理 (MDM) 註冊裝置上的公司資料，且不會影響個人資料。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-120">The ability to remote wipes corporate data from Intune Mobile Device Management (MDM) enrolled devices while leaving personal data unaffected.</span></span> 
- <span data-ttu-id="2c9ff-121">針對追蹤問題和補救動作 (例如使用者的合規性訓練) 的稽核報告。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-121">Audit reports for tracking issues and for remedial actions such as compliance training for users.</span></span>
- <span data-ttu-id="2c9ff-122">與您現有的管理系統整合，以設定、部署、管理 WIP。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-122">Integration with your existing management system to configure, deploy, and manage WIP.</span></span> <span data-ttu-id="2c9ff-123">例如 Microsoft Intune、Microsoft Endpoint 設定管理員、或是您目前的行動裝置管理 (MDM) 系統。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-123">Some examples are Microsoft Intune, Microsoft Endpoint Configuration Manager, or your current mobile device management (MDM) system.</span></span>

## <a name="wip-policy-and-protection-modes"></a><span data-ttu-id="2c9ff-124">WIP 原則和保護模式</span><span class="sxs-lookup"><span data-stu-id="2c9ff-124">WIP policy and protection modes</span></span>

<span data-ttu-id="2c9ff-125">使用原則，您可以設定下表所述的四種保護模式。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-125">Using policies, you can configure the four protection modes described in the following table.</span></span> <span data-ttu-id="2c9ff-126">如需詳細資訊，請參閱 [WIP 保護模式](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes)。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-126">For more information, see [WIP-protection modes](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes).</span></span>

| <span data-ttu-id="2c9ff-127">模式</span><span class="sxs-lookup"><span data-stu-id="2c9ff-127">Mode</span></span> | <span data-ttu-id="2c9ff-128">描述</span><span class="sxs-lookup"><span data-stu-id="2c9ff-128">Description</span></span> |
|------|-------------|
| <span data-ttu-id="2c9ff-129">封鎖</span><span class="sxs-lookup"><span data-stu-id="2c9ff-129">Block</span></span> | <span data-ttu-id="2c9ff-130">WIP 會尋找不適當的資料共用做法，並阻止員工完成該動作。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-130">WIP looks for inappropriate data sharing practices and stops the employee from completing the action.</span></span> <span data-ttu-id="2c9ff-131">此搜尋可包含將企業資訊共用至非企業保護的應用程式，以及在應用程式之間共用企業資料，或嘗試在組織網路以外的地方進行共用。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-131">This search can include sharing enterprise data to non-enterprise-protected apps in addition to sharing enterprise data between apps or attempting to share outside of your organization's network.</span></span> |
| <span data-ttu-id="2c9ff-132">允許覆寫</span><span class="sxs-lookup"><span data-stu-id="2c9ff-132">Allow Overrides</span></span> | <span data-ttu-id="2c9ff-133">WIP 會尋找不適當的資料共用，並在員工做出可能不安全的事情時，對該員工發出警告。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-133">WIP looks for inappropriate data sharing, warning employees if they do something deemed potentially unsafe.</span></span> <span data-ttu-id="2c9ff-134">不過，此管理模式允許員工覆寫原則並共用資料，同時將該動作記錄到您的稽核記錄中。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-134">However, this management mode lets the employee override the policy and share the data, logging the action to your audit log.</span></span> |
| <span data-ttu-id="2c9ff-135">無訊息</span><span class="sxs-lookup"><span data-stu-id="2c9ff-135">Silent</span></span> | <span data-ttu-id="2c9ff-136">WIP 會以無訊息方式執行、記錄不適當的資料共用，但在處於允許覆寫模式時，不會阻止任何提示員工進行互動的動作。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-136">WIP runs silently, logging inappropriate data sharing, without stopping anything that would have been prompted for employee interaction while in Allow Overrides mode.</span></span> <span data-ttu-id="2c9ff-137">不允許的動作 (例如，不適當地嘗試存取網路資源或 WIP 所保護資料的應用程式) 仍會遭到阻止。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-137">Unallowed actions, like apps inappropriately trying to access a network resource or WIP-protected data, are still stopped.</span></span> |
| <span data-ttu-id="2c9ff-138">關閉</span><span class="sxs-lookup"><span data-stu-id="2c9ff-138">Off</span></span> | <span data-ttu-id="2c9ff-139">WIP 會關閉，且不會協助保護或稽核您的資料。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-139">WIP is turned off and doesn't help to protect or audit your data.</span></span> <span data-ttu-id="2c9ff-140">關閉 WIP 之後，會嘗試在本機連接的磁碟機上將任何有 WIP 標記的檔案解密。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-140">After you turn off WIP, an attempt is made to decrypt any WIP-tagged files on the locally attached drives.</span></span> <span data-ttu-id="2c9ff-141">如果您重新開啟 WIP 保護，之前的解密和原則資訊並不會自動重新套用。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-141">Your previous decryption and policy info isn't automatically reapplied if you turn WIP protection back on.</span></span>
 |

## <a name="wip-features-supported-in-microsoft-edge"></a><span data-ttu-id="2c9ff-142">Microsoft Edge 支援的 WIP 功能</span><span class="sxs-lookup"><span data-stu-id="2c9ff-142">WIP features supported in Microsoft Edge</span></span>

<span data-ttu-id="2c9ff-143">從 Microsoft Edge 版本 81 開始，支援下列功能：</span><span class="sxs-lookup"><span data-stu-id="2c9ff-143">Starting with Microsoft Edge version 81, the following features are supported:</span></span>

- <span data-ttu-id="2c9ff-144">用網址列上的公事包圖示來表示工作網站。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-144">Work sites will be indicated by a briefcase icon on the address bar.</span></span>  
- <span data-ttu-id="2c9ff-145">從工作位置下載的檔案會自動加密。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-145">Files downloaded from a work location are automatically encrypted.</span></span>
- <span data-ttu-id="2c9ff-146">將工作檔案上傳到非工作位置時，強制執行無訊息/封鎖/覆寫。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-146">Silent/Block/Override enforcement for work file uploads to non-work locations.</span></span>  
- <span data-ttu-id="2c9ff-147">拖放檔案時強制執行無訊息/封鎖/覆寫。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-147">Silent/Block/Override enforcement for file Drag & Drop actions.</span></span>
- <span data-ttu-id="2c9ff-148">執行剪貼簿動作時，強制執行無訊息/封鎖/覆寫。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-148">Silent/Block/Override enforcement for Clipboard actions.</span></span>
- <span data-ttu-id="2c9ff-149">從非工作設定檔瀏覽到工作位置，會自動重新導向至工作設定檔 (與 Azure AD 身分識別關聯)。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-149">Browsing to work locations from non-work profiles automatically redirects to the Work Profile (associated with the Azure AD Identity.)</span></span>
- <span data-ttu-id="2c9ff-150">IE 模式支援完整的 WIP 功能。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-150">IE Mode supports full WIP functionality.</span></span>

## <a name="working-with-wip-in-microsoft-edge"></a><span data-ttu-id="2c9ff-151">在 Microsoft Edge 中使用 WIP</span><span class="sxs-lookup"><span data-stu-id="2c9ff-151">Working with WIP in Microsoft Edge</span></span>

<span data-ttu-id="2c9ff-152">啟用 Microsoft Edge 的 WIP 支援之後，使用者將會看到正在存取工作相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-152">After WIP support is enabled for Microsoft Edge, users will see when work-related information is accessed.</span></span> <span data-ttu-id="2c9ff-153">下個螢幕擷取畫面的網址列中顯示公事包圖示，指出正透過瀏覽器存取工作相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-153">The next screenshot shows the briefcase icon in the address bar, indicating that work-related information is accessed via the browser.</span></span>

 ![標示為「工作」網站的網址列指示器](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

<span data-ttu-id="2c9ff-155">Microsoft Edge 可讓使用者在未核准的網站中共用受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-155">Microsoft Edge gives users the ability to share protected content in an unapproved website.</span></span> <span data-ttu-id="2c9ff-156">下個螢幕擷取畫面中顯示的 Microsoft Edge 提示，提醒使用者將允許在未獲核准的網站中使用受保護內容。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-156">The next screenshot shows the Microsoft Edge prompt that allows a user to use protected content in an unapproved website.</span></span>

 ![提示受保護的內容覆寫](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a><span data-ttu-id="2c9ff-158">設定原則以支援 WIP</span><span class="sxs-lookup"><span data-stu-id="2c9ff-158">Configure policies to support WIP</span></span>

<span data-ttu-id="2c9ff-159">在 Microsoft Edge 中使用 WIP 需要具備工作設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-159">Using WIP with Microsoft Edge requires the presence of a work profile.</span></span>

### <a name="ensure-the-presence-of-a-work-profile"></a><span data-ttu-id="2c9ff-160">確定有工作設定檔</span><span class="sxs-lookup"><span data-stu-id="2c9ff-160">Ensure the presence of a work profile</span></span>

<span data-ttu-id="2c9ff-161">在混合式聯結的電腦上，Microsoft Edge 會自動以 Azure Active Directory (Azure AD) 帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-161">On hybrid joined machines, Microsoft Edge is automatically signed in with the Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="2c9ff-162">為了確保使用者沒有移除 WIP 需要的這個設定檔，請設定下列原則：</span><span class="sxs-lookup"><span data-stu-id="2c9ff-162">To make sure that users don't remove this profile, which is needed for WIP, configure the following policy:</span></span>

- [<span data-ttu-id="2c9ff-163">NonRemovableProfileEnabled</span><span class="sxs-lookup"><span data-stu-id="2c9ff-163">NonRemovableProfileEnabled</span></span>](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> <span data-ttu-id="2c9ff-164">如果您的環境不是混合式聯結，您可以使用下列指示進行混合式聯結： [規劃混合式 Azure Active Directory 聯結的實作](/azure/active-directory/devices/hybrid-azuread-join-plan)。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-164">If your environment isn't hybrid joined, you can hybrid join using these instructions: [Plan your hybrid Azure Active Directory join implementation](/azure/active-directory/devices/hybrid-azuread-join-plan).</span></span>

<span data-ttu-id="2c9ff-165">如果混合式聯結不可行，您可以使用內部部署的 Active Directory 帳戶來允許 Microsoft Edge 以使用者網域帳戶自動建立特別工作設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-165">If hybrid joining isn't an option, you can use on-prem Active Directory accounts to allow Microsoft Edge to auto create a special work profile with the users' domain accounts.</span></span> <span data-ttu-id="2c9ff-166">請注意，內部部署帳戶可能不能使用 Azure AD 的所有功能，例如雲端同步處理、Office NTP 等。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-166">Note that on-premises accounts may not receive all of Azure AD's features, such as cloud sync, Office NTP, and so on.)</span></span>

#### <a name="active-directory-ad-accounts"></a><span data-ttu-id="2c9ff-167">Active Directory (AD) 帳戶</span><span class="sxs-lookup"><span data-stu-id="2c9ff-167">Active Directory (AD) accounts</span></span>

<span data-ttu-id="2c9ff-168">您必須為 AD 帳戶設定下列原則，好讓 Microsoft Edge 自動建立特別工作設定檔。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-168">For AD accounts, you must configure the following policy to have the Microsoft Edge auto create a special work profile.</span></span>

- [<span data-ttu-id="2c9ff-169">ConfigureOnPremisesAccountAutoSignIn</span><span class="sxs-lookup"><span data-stu-id="2c9ff-169">ConfigureOnPremisesAccountAutoSignIn</span></span>](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a><span data-ttu-id="2c9ff-170">適用於 WIP 的 Windows 原則</span><span class="sxs-lookup"><span data-stu-id="2c9ff-170">Windows policies for WIP</span></span>

<span data-ttu-id="2c9ff-171">您可以使用 Windows 原則來設定 WIP。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-171">You can configure WIP using Windows policies.</span></span> <span data-ttu-id="2c9ff-172">如需詳細資訊，請參閱[使用 Microsoft Intune 建立和部署 WIP 原則](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-172">For more information, see [Create and deploy WIP policies using Microsoft Intune](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2c9ff-173">常見問題集</span><span class="sxs-lookup"><span data-stu-id="2c9ff-173">Frequently Asked Questions</span></span>

### <a name="how-do-i-resolve-error-code--2147024540"></a><span data-ttu-id="2c9ff-174">如何解決錯誤碼 -2147024540？</span><span class="sxs-lookup"><span data-stu-id="2c9ff-174">How do I resolve Error Code -2147024540?</span></span>

<span data-ttu-id="2c9ff-175">此錯誤碼對應於以下 Windows 資訊保護錯誤：*ERROR_EDP_POLICY_DENIES_OPERATION：Windows 資訊保護原則封鎖了請求的操作。如需詳細資訊，請連絡您的系統管理員*。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-175">This error code corresponds to the following Windows Information Protection error: *ERROR_EDP_POLICY_DENIES_OPERATION: The requested operation was blocked by Windows Information Protection policy. For more information, contact your system administrator.*</span></span>

<span data-ttu-id="2c9ff-176">當組織啟用 Windows 資訊保護 (WIP) 以僅允許使用已核准應用程式的使用者存取公司資源時，Microsoft Edge 會顯示此錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-176">Microsoft Edge shows this error when the organization has enabled Windows Information Protection (WIP) to only allow users with approved applications to access corporate resources.</span></span> <span data-ttu-id="2c9ff-177">在這種情況下，由於 Microsoft Edge 不在已核准的應用程式清單中，管理員必須更新 WIP 原則以授予對 Microsoft Edge 的存取權限。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-177">In this case because Microsoft Edge isn't on the approved applications list, the admin will have to update the WIP policies to grant access to Microsoft Edge.</span></span>

<span data-ttu-id="2c9ff-178">下列螢幕擷取畫面顯示如何使用 Microsoft Intune 將 Microsoft Edge 新增為可供 WIP 使用的應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-178">The following screenshot shows how the Microsoft Intune is used to add Microsoft Edge as an allowed app for WIP.</span></span>

 ![將 Microsoft Edge 新增為 WIP 應用程式的 Intune 對話方塊](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

<span data-ttu-id="2c9ff-180">如果您並非使用 Microsoft Intune，請下載 [WIP 企業 AppLocker 原則](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip)檔案並套用檔案中的原則更新。</span><span class="sxs-lookup"><span data-stu-id="2c9ff-180">If you're not using Microsoft Intune, download and apply the policy update in the [WIP Enterprise AppLocker Policy](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip) file.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c9ff-181">請參閱</span><span class="sxs-lookup"><span data-stu-id="2c9ff-181">See also</span></span>

- [<span data-ttu-id="2c9ff-182">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="2c9ff-182">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise) 
- [<span data-ttu-id="2c9ff-183">使用 Windows 資訊保護保護企業資料</span><span class="sxs-lookup"><span data-stu-id="2c9ff-183">Protect enterprise data using Windows Information Protection</span></span>](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)