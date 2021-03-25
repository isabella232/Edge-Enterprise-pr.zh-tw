---
title: 診斷並修正 Microsoft Edge 同步處理問題
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 03/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 系統管理員可用於疑難排解及修正常見企業同步處理問題的指導方針和工具
ms.openlocfilehash: 49fb0c5fc555e4f7ad4c728477387e931a5fbb5f
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447157"
---
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a><span data-ttu-id="7d1d1-103">診斷並修正 Microsoft Edge 同步處理問題</span><span class="sxs-lookup"><span data-stu-id="7d1d1-103">Diagnose and fix Microsoft Edge sync issues</span></span>

<span data-ttu-id="7d1d1-104">本文針對 Azure Active Directory (Azure AD) 環境中最常遇到的同步處理問題提供疑難排解指導方針。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-104">This article provides troubleshooting guidance for the most commonly encountered sync issues in an Azure Active Directory (Azure AD) environment.</span></span> <span data-ttu-id="7d1d1-105">它還包含用於收集疑難排解同步處理問題所需的記錄建議使用工具。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-105">It also includes the recommended tools for gathering the logs needed for troubleshooting a sync issue.</span></span>

<span data-ttu-id="7d1d1-106">如果使用者遇到跨裝置同步處理瀏覽器資料的問題，可以嘗試 [重設同步處理](edge-learnmore-reset-data-in-cloud.md)。如果還是無法解決問題，系統管理員或支援人員可以使用下列指導方針以修正同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-106">If a user is experiencing an issue syncing browser data across their devices they can try [resetting sync](edge-learnmore-reset-data-in-cloud.md). If this doesn't work, admins or support staff can use the following guidance to fix a sync issue.</span></span>

> [!NOTE]
> <span data-ttu-id="7d1d1-107">除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-107">Applies to Microsoft Edge version 77 or later unless otherwise noted.</span></span>

## <a name="identity-issues-versus-sync-issues"></a><span data-ttu-id="7d1d1-108">身分識別問題與同步處理問題</span><span class="sxs-lookup"><span data-stu-id="7d1d1-108">Identity issues versus sync issues</span></span>

<span data-ttu-id="7d1d1-109">開始之前，瞭解身分識別問題與同步處理問題之間的差異非常重要。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-109">Before you begin it's important to understand the difference between identity issues and sync issues.</span></span> <span data-ttu-id="7d1d1-110">在瀏覽器中維護使用者身分識別的常見使用案例就是支援同步處理。因此，身分識別問題通常會與同步處理問題混淆。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-110">A popular use case for maintaining user identity in the browser is to support sync. For this reason, identity issues are frequently confused with sync issues.</span></span> <span data-ttu-id="7d1d1-111">在開始疑難排解同步處理之前，請瞭解身分識別與同步處理問題之間的差異。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-111">Understand the difference between identity and sync issue before you start troubleshooting sync.</span></span>

<span data-ttu-id="7d1d1-112">在您將問題視為同步處理問題之前，請先檢查使用者是否已使用有效的帳戶登入瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-112">Before you treat an issue as a sync issue, check to see if the user is signed into the browser with a valid account.</span></span>

<span data-ttu-id="7d1d1-113">下一個螢幕擷取畫面顯示身分識別錯誤的範例。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-113">The next screenshot shows an example of an identity error.</span></span> <span data-ttu-id="7d1d1-114">錯誤為「**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**」，這可在 *edge://sync-internals* 的 **Credentials** 下找到：</span><span class="sxs-lookup"><span data-stu-id="7d1d1-114">The error is "**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**", which is found in *edge://sync-internals* under **Credentials**:</span></span>

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a><span data-ttu-id="7d1d1-116">常見的同步問題</span><span class="sxs-lookup"><span data-stu-id="7d1d1-116">Common sync issues</span></span>

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a><span data-ttu-id="7d1d1-117">問題：無法存取 M365 或 Azure 資訊保護訂閱</span><span class="sxs-lookup"><span data-stu-id="7d1d1-117">Issue: Can't access M365 or Azure Information Protection subscription</span></span>

<span data-ttu-id="7d1d1-118">您是否有先前的 M365 或 Azure 資訊保護 (AIP) 訂閱已過期，然後以新訂閱將其取代？</span><span class="sxs-lookup"><span data-stu-id="7d1d1-118">Do you have a previous M365 or Azure Information Protection (AIP) subscription that expired and then replaced with a new subscription?</span></span> <span data-ttu-id="7d1d1-119">如果是這樣，則租使用者識別碼已變更，且需要重設服務資料。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-119">If so, then the tenant ID has changed and the service data needs to be reset.</span></span> <span data-ttu-id="7d1d1-120">請參閱**密碼錯誤問題**中重置資料的說明。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-120">See the instructions for resetting data in the **Cryptographer error encountered** issue.</span></span>

### <a name="issue-sync-is-not-available-for-this-account"></a><span data-ttu-id="7d1d1-121">問題：「此帳戶無法使用同步處理」。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-121">Issue: “Sync is not available for this account.”</span></span>

<span data-ttu-id="7d1d1-122">如果 Azure Active Directory 帳戶遇到此錯誤，或 DISABLED_BY_ADMIN 出現在 *edge://sync-internals*中，依次執行下一步驟中的步驟，直到問題得到解决。。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-122">If this error is encountered for an Azure Active Directory account, or if DISABLED_BY_ADMIN appears in *edge://sync-internals*, follow the steps in the next procedure sequentially until the problem is fixed.</span></span>

> [!NOTE]
> <span data-ttu-id="7d1d1-123">由於此錯誤的來源通常是需要在 Azure Active Directory 租用戶中變更設定，因此這些疑難排解步驟只能由租用戶系統管理員執行，而不能由使用者執行。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-123">Because the source of this error is usually requires a configuration change in an Azure Active Directory tenant, these troubleshooting steps can only performed by a tenant admin and not by end users.</span></span>

1. <span data-ttu-id="7d1d1-124">確認企業租使用者具有支援的 M365 訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-124">Verify that the enterprise tenant has a supported M365 subscription.</span></span> <span data-ttu-id="7d1d1-125">目前提供的可用訂閱類型清單 [如下](/azure/information-protection/activate-office365)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-125">The current list of available subscription types is [provided here](/azure/information-protection/activate-office365).</span></span> <span data-ttu-id="7d1d1-126">如果租使用者沒有受支援的訂閱，他們可以單獨購買 Azure 資訊保護，或升級至其中一個支援的訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-126">If the tenant doesn't have a supported subscription, they can either purchase Azure Information Protection separately, or upgrade to one of the supported subscriptions.</span></span>
2. <span data-ttu-id="7d1d1-127">如果支援的訂閱可用，請驗證租用戶是否具有可用的 Azure 資訊保護 (AIP)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-127">If a supported subscription is available, verify that the tenant has Azure Information Protection (AIP) available.</span></span> <span data-ttu-id="7d1d1-128">有關檢查 AIP 狀態以及在必要時啟動 AIP 的說明，請參見[此處](/azure/information-protection/activate-office365)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-128">The instructions for checking the AIP status and, if necessary, activating AIP are [here](/azure/information-protection/activate-office365).</span></span>
3. <span data-ttu-id="7d1d1-129">如果步驟 2 顯示 AIP 處於使用中，但仍無法進行同步處理，請開啟企業狀態漫遊 (ESR)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-129">If step 2 shows that AIP is active but sync still doesn't work, turn on Enterprise State Roaming (ESR).</span></span> <span data-ttu-id="7d1d1-130">啟用 ESR 的指示在 [這裡](/azure/active-directory/devices/enterprise-state-roaming-enable)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-130">The instructions for enabling ESR are [here](/azure/active-directory/devices/enterprise-state-roaming-enable).</span></span> <span data-ttu-id="7d1d1-131">請注意，ESR 不需要保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-131">Note that ESR does not need to stay on.</span></span> <span data-ttu-id="7d1d1-132">如果此步驟修正了問題，您可以關閉 ESR。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-132">You can turn off ESR if this step fixes the issue.</span></span>
4. <span data-ttu-id="7d1d1-133">確認 Azure 資訊保護未透過加入原則限定範圍。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-133">Confirm that Azure Information Protection is not scoped via an onboarding policy.</span></span> <span data-ttu-id="7d1d1-134">您可以使用 [AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式來查看是否啟用了範圍。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-134">You can use the [Get-AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet to see if scoping is enabled.</span></span> <span data-ttu-id="7d1d1-135">接下來的兩個範例顯示了一個不限範圍的設定和一個範圍設定為特定安全性群組的設定。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-135">The next two examples show an unscoped configuration and a configuration scoped to a specific security group.</span></span>

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

   <span data-ttu-id="7d1d1-136">如果已啟用範圍，則受影響的使用者應該新增至該範圍的安全性群組，或者應該移除該範圍。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-136">If scoping is enabled, the affected user should either be added to the security group for the scope, or the scope should be removed.</span></span> <span data-ttu-id="7d1d1-137">在下方的範例中，上線已將 AIP 的範圍設定為指定的安全性群組，應使用 [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式移除該範圍。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-137">In the example below, onboarding has scoped AIP to the indicated security group and the scoping should be removed with the [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell applet.</span></span>

5. <span data-ttu-id="7d1d1-138">確認 IPCv3Service 已在租用戶中開啟。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-138">Confirm that the IPCv3Service is turned on in the tenant.</span></span> <span data-ttu-id="7d1d1-139">[AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) PowerShell 小程式顯示服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-139">The [Get-AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps)  PowerShell applet shows the status of the service.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="查看是否已啟用 IPCv3Service。":::

6. <span data-ttu-id="7d1d1-141">如果問題未修正，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-141">If the issue isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a><span data-ttu-id="7d1d1-142">問題：停滯在「正在設定同步處理...」或「無法連線到同步處理伺服器。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-142">Issue: Stuck at "Setting up sync..." or “Couldn’t connect to the sync server.</span></span> <span data-ttu-id="7d1d1-143">正在重試...」</span><span class="sxs-lookup"><span data-stu-id="7d1d1-143">Retrying…”</span></span>

1. <span data-ttu-id="7d1d1-144">請嘗試登出，然後再登入。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-144">Try to sign out and then sign in.</span></span>
2. <span data-ttu-id="7d1d1-145">移至 *edge://sync-internals*。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-145">Go to *edge://sync-internals*.</span></span> <span data-ttu-id="7d1d1-146">如果在「**輸入資訊**」區段下出現下列錯誤，請跳至下列問題， **發生密碼錯誤**。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-146">If under the "**Type info**" section the following error is present, then  skip to the following issue, **Cryptographer error encountered**.</span></span>

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. <span data-ttu-id="7d1d1-147">請嘗試抓取伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-147">Try pinging the server endpoint.</span></span> <span data-ttu-id="7d1d1-148">用戶端的伺服器端點可在 *edge://sync-internals*中取得。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-148">The server endpoint for a client is available in *edge://sync-internals*.</span></span> <span data-ttu-id="7d1d1-149">下一個螢幕擷取畫面顯示 [**環境資訊**] 底部的端點資訊。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-149">The next screenshot shows endpoint information under **Environment Info**.</span></span>

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="端點資訊":::

4. <span data-ttu-id="7d1d1-151">如果伺服器端點為空白，或無法抓取伺服器並且環境中存在防火牆，請確認用戶端電腦可使用必要的服務端點。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-151">If the server endpoint is empty, or if server cannot be pinged and a firewall is present in the environment, confirm that the necessary service endpoints are available to the client computer.</span></span>

   - <span data-ttu-id="7d1d1-152">Microsoft Edge 同步處理服務端點：</span><span class="sxs-lookup"><span data-stu-id="7d1d1-152">Microsoft Edge sync service endpoints:</span></span>
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - <span data-ttu-id="7d1d1-153">Azure 資訊保護端點：</span><span class="sxs-lookup"><span data-stu-id="7d1d1-153">Azure Information Protection endpoints:</span></span>
      - <span data-ttu-id="7d1d1-154">[https://api.aadrm.com](https://api.aadrm.com) (適用於多數租用戶)</span><span class="sxs-lookup"><span data-stu-id="7d1d1-154">[https://api.aadrm.com](https://api.aadrm.com) (for most tenants)</span></span>
      - <span data-ttu-id="7d1d1-155">[https://api.aadrm.de](https://api.aadrm.de) (適用於德國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="7d1d1-155">[https://api.aadrm.de](https://api.aadrm.de) (for tenants in Germany)</span></span>
      - <span data-ttu-id="7d1d1-156">[https://api.aadrm.cn](https://api.aadrm.cn) (適用於中國的租用戶)</span><span class="sxs-lookup"><span data-stu-id="7d1d1-156">[https://api.aadrm.cn](https://api.aadrm.cn) (for tenants in China)</span></span>
   - <span data-ttu-id="7d1d1-157">[Windows 通知服務端點](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-157">[Windows Notification Service endpoints](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config).</span></span>

5. <span data-ttu-id="7d1d1-158">如果問題仍未解決，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-158">If the issue still isn't fixed, contact [Microsoft Edge support](https://www.microsoftedgeinsider.com/support).</span></span>

### <a name="issue-cryptographer-error-encountered"></a><span data-ttu-id="7d1d1-159">問題：發生密碼錯誤</span><span class="sxs-lookup"><span data-stu-id="7d1d1-159">Issue: Cryptographer error encountered</span></span>

<span data-ttu-id="7d1d1-160">此錯誤可在 *edge://sync-internals* 中的 **Type info** 下看到，並且可能表示需要重設使用者的服務端資料。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-160">This error is visible under **Type info** in *edge://sync-internals* and may mean that the user's service side data needs to be reset.</span></span> <span data-ttu-id="7d1d1-161">下列範例顯示密碼編譯錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="7d1d1-161">The following example shows a cryptography error message:</span></span>
<br><span data-ttu-id="7d1d1-162">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span><span class="sxs-lookup"><span data-stu-id="7d1d1-162">"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".</span></span>

1. <span data-ttu-id="7d1d1-163">重新啟動 Microsoft Edge 並瀏覽至 *edge://sync-internals*，然後查看 "**AAD Account Key Status**" 區段</span><span class="sxs-lookup"><span data-stu-id="7d1d1-163">Restart Microsoft Edge and navigate to *edge://sync-internals* and check the “**AAD Account Key Status**” section</span></span>
   - <span data-ttu-id="7d1d1-164">"Success" in "Last MIP Result"：密碼錯誤意味著伺服器資料可能被遺失的金鑰加密。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-164">"Success" in "Last MIP Result": the cryptographer error means server data might be encrypted with a lost key.</span></span> <span data-ttu-id="7d1d1-165">需要重設資料才能繼續同步處理。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-165">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="7d1d1-166">"No permissions" in "Last MIP Result"：這可能是由 Azure AD 變更或租用戶訂閱變更引起的。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-166">"No permissions" in "Last MIP Result": It is possibly caused by an Azure AD change or tenant subscription changes.</span></span> <span data-ttu-id="7d1d1-167">需要重設資料才能繼續同步處理。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-167">Data reset is needed to resume sync.</span></span>
   - <span data-ttu-id="7d1d1-168">其他錯誤可能意味著伺服器設定問題。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-168">Other errors may mean server configuration issues.</span></span>
2. <span data-ttu-id="7d1d1-169">如果需要重設資料，請參閱 [重設雲端中的 Microsoft Edge 資料](edge-learnmore-reset-data-in-cloud.md)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-169">If data reset is needed, see [Reset Microsoft Edge data in the cloud](edge-learnmore-reset-data-in-cloud.md).</span></span>

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a><span data-ttu-id="7d1d1-170">問題：「您的系統管理員已關閉同步處理。」</span><span class="sxs-lookup"><span data-stu-id="7d1d1-170">Issue: “Sync has been turned off by your administrator.”</span></span>

<span data-ttu-id="7d1d1-171">請確定未設定 [SyncDisabled 原則](./microsoft-edge-policies.md#syncdisabled)。</span><span class="sxs-lookup"><span data-stu-id="7d1d1-171">Make sure that the [SyncDisabled policy](./microsoft-edge-policies.md#syncdisabled)  is not set.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d1d1-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d1d1-172">See also</span></span>

- [<span data-ttu-id="7d1d1-173">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="7d1d1-173">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
- [<span data-ttu-id="7d1d1-174">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="7d1d1-174">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="7d1d1-175">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="7d1d1-175">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)