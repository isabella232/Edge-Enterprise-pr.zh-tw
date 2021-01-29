---
title: 為使用者自動啟用密碼監視器
ms.author: supalsul
author: dan-wesley
manager: tulasim
ms.date: 01/26/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 為使用者自動啟用密碼監視器
ms.openlocfilehash: 2f796f0cd1bbb437f83d04a8bd59586ef7b6a982
ms.sourcegitcommit: 187203e9eaa9c48c59095b7e7d625d3081a6ba19
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/27/2021
ms.locfileid: "11304533"
---
# <span data-ttu-id="3946d-103">為使用者自動啟用密碼監視器</span><span class="sxs-lookup"><span data-stu-id="3946d-103">Password Monitor auto-enabled for users</span></span>

<span data-ttu-id="3946d-104">本文說明如何為選取的使用者開啟 Microsoft Edge 中的密碼監視器，並提供系統管理員用來控制監視啟用方式的步驟。</span><span class="sxs-lookup"><span data-stu-id="3946d-104">This article describes how Password Monitor in Microsoft Edge will be turned on for select users and gives admins the steps to control how monitoring is enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="3946d-105">本文適用於 Microsoft Edge 版本 88 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3946d-105">This article applies to Microsoft Edge version 88 or later.</span></span>

## <span data-ttu-id="3946d-106">簡介、優點和可用性</span><span class="sxs-lookup"><span data-stu-id="3946d-106">Introduction, benefits, and availability</span></span>

<span data-ttu-id="3946d-107">密碼監視器可協助 Microsoft Edge 使用者保護其線上帳戶，方法是通知使用者是否在線上洩漏中發現其任何密碼。</span><span class="sxs-lookup"><span data-stu-id="3946d-107">Password Monitor helps Microsoft Edge users protect their online accounts by informing them if any of their passwords have been found in an online leak.</span></span> <span data-ttu-id="3946d-108">當不良行為者竊取協力廠商應用程式或網站的資料時，即發生線上洩漏或資料違規。</span><span class="sxs-lookup"><span data-stu-id="3946d-108">Online leaks or data breaches happen when bad actors steal data from third-party apps or websites.</span></span> <span data-ttu-id="3946d-109">若要深入瞭解，請參閱 Microsoft 部落格上的[密碼監視器：在 Microsoft Edge 中保護密碼](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/)文章。</span><span class="sxs-lookup"><span data-stu-id="3946d-109">To learn more, see the [Password Monitor: Safeguarding passwords in Microsoft Edge](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/)  paper on the Microsoft Research Blog.</span></span>

### <span data-ttu-id="3946d-110">優點</span><span class="sxs-lookup"><span data-stu-id="3946d-110">Benefits</span></span>

<span data-ttu-id="3946d-111">有鑑於這些線上攻擊的頻率與範圍，我們每個人都必須具備這種保護。</span><span class="sxs-lookup"><span data-stu-id="3946d-111">Given the frequency and scope of these online attacks having this kind of protection has become necessary for everyone.</span></span> <span data-ttu-id="3946d-112">Microsoft Edge 具備內建功能，可安全地檢查使用者儲存的密碼對照已知受危害的密碼，並在發現相符時提醒使用者。</span><span class="sxs-lookup"><span data-stu-id="3946d-112">Microsoft Edge has the built-in ability to securely check a user's saved passwords against passwords that are known to be compromised and alerts them if a match is found.</span></span>  

### <span data-ttu-id="3946d-113">可用性</span><span class="sxs-lookup"><span data-stu-id="3946d-113">Availability</span></span>

<span data-ttu-id="3946d-114">密碼監視器在穩定通道版本 88 中提供，從 1/21 開始。</span><span class="sxs-lookup"><span data-stu-id="3946d-114">Password Monitor is available in Stable Channel version 88 starting 1/21.</span></span> <span data-ttu-id="3946d-115">推出將會是漸進式，且可能需要幾週的時間，您才會在您的 [設定]\*\*\*\*  >  [設定檔]\*\*\*\*  >  [密碼]\*\*\*\* 頁面中看到下列訊息及控制項。</span><span class="sxs-lookup"><span data-stu-id="3946d-115">The rollout will be gradual and it could take a few weeks before you will see the following message and control in your **Settings** > **Profile** > **Password** page.</span></span>

:::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enable-option.png" alt-text="啟用密碼監視器的選項":::

## <span data-ttu-id="3946d-117">設定密碼監視器的群組原則</span><span class="sxs-lookup"><span data-stu-id="3946d-117">Configure group policy for Password Monitor</span></span>

<span data-ttu-id="3946d-118">此功能是透過 [PasswordMonitorAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmonitorallowed) 群組原則控制。</span><span class="sxs-lookup"><span data-stu-id="3946d-118">This feature is controlled via the [PasswordMonitorAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmonitorallowed) group policy.</span></span>

<span data-ttu-id="3946d-119">啟用原則之後，使用者仍然必須同意，才能開啟該功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-119">After the policy is enabled, users still need to provide consent to turn on the feature.</span></span> <span data-ttu-id="3946d-120">由於功能包含使用者的敏感性和個人資料 (密碼)，因此需要取得同意。</span><span class="sxs-lookup"><span data-stu-id="3946d-120">Consent is required because the feature contains user's sensitive and personal data (passwords).</span></span> <span data-ttu-id="3946d-121">如果使用群組原則停用該功能，使用者就無法覆寫此設定。</span><span class="sxs-lookup"><span data-stu-id="3946d-121">If the feature is disabled using group policy, users can't override this setting.</span></span>  

## <span data-ttu-id="3946d-122">為使用者啟用密碼監視器</span><span class="sxs-lookup"><span data-stu-id="3946d-122">Enabling Password Monitor for users</span></span>

<span data-ttu-id="3946d-123">啟用密碼監視器原則之後，使用者會透過不同方式來取得此功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-123">After the password monitor policy is enabled, there are different ways this feature is made available to users.</span></span>

- <span data-ttu-id="3946d-124">自動啟用。</span><span class="sxs-lookup"><span data-stu-id="3946d-124">Auto-enablement.</span></span> <span data-ttu-id="3946d-125">使用其公司帳戶 (Active Directory 或 Azure Active Directory) 登入並同步其密碼的使用者，將會自動啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-125">Users that are signed-in using their work account (Active Directory or Azure Active Directory) and syncing their passwords will be auto-enabled for this feature.</span></span> <span data-ttu-id="3946d-126">在下一個螢幕擷取畫面中，使用者會看到通知，通知其該功能已開啟。</span><span class="sxs-lookup"><span data-stu-id="3946d-126">They will  see the notification in the next screenshot informing them that the feature's turned on.</span></span>

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="密碼監視器已啟用通知":::

-  <span data-ttu-id="3946d-128">取得明確同意。</span><span class="sxs-lookup"><span data-stu-id="3946d-128">Getting explicit consent.</span></span> <span data-ttu-id="3946d-129">未開啟密碼同步的使用者，系統會要求他們提供開啟密碼監視器的權限。</span><span class="sxs-lookup"><span data-stu-id="3946d-129">Users that don’t have Password Sync turned on will be asked for permission to turn on Password Monitor.</span></span> <span data-ttu-id="3946d-130">他們將在下列動作執行時收到提示：</span><span class="sxs-lookup"><span data-stu-id="3946d-130">They will be prompted when the following actions happen:</span></span>
   - <span data-ttu-id="3946d-131">當使用者儲存新密碼時。</span><span class="sxs-lookup"><span data-stu-id="3946d-131">When a user is saving a new password.</span></span>
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="提示儲存密碼":::

   - <span data-ttu-id="3946d-133">使用者使用已儲存的密碼登入瀏覽器時。</span><span class="sxs-lookup"><span data-stu-id="3946d-133">When a user has signed-in to the browser using a saved password.</span></span>
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="登入後確認提示":::
   
- <span data-ttu-id="3946d-135">直接啟用。</span><span class="sxs-lookup"><span data-stu-id="3946d-135">Direct activation.</span></span> <span data-ttu-id="3946d-136">使用者可以隨時移至 [設定]\*\*\*\*  >  [密碼]\*\*\*\*，並開啟或關閉該功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-136">Users can go to **Settings** > **Passwords** anytime and turn the feature On or Off.</span></span>

## <span data-ttu-id="3946d-137">自動啟用密碼監視器的使用者案例</span><span class="sxs-lookup"><span data-stu-id="3946d-137">User scenarios with Password Monitor auto-enabled</span></span>

<span data-ttu-id="3946d-138">下表顯示自動啟用密碼監視器的案例，以及該功能如何在使用者裝置上運作。</span><span class="sxs-lookup"><span data-stu-id="3946d-138">The following table shows scenarios where Password Monitor is auto-enabled and how it will work on user devices.</span></span>

| <span data-ttu-id="3946d-139">案例</span><span class="sxs-lookup"><span data-stu-id="3946d-139">Scenario</span></span> | <span data-ttu-id="3946d-140">基本條件</span><span class="sxs-lookup"><span data-stu-id="3946d-140">Base conditions</span></span> | <span data-ttu-id="3946d-141">影響</span><span class="sxs-lookup"><span data-stu-id="3946d-141">Impact</span></span> |
|--|--|--|
| <span data-ttu-id="3946d-142">1 同步開啟</span><span class="sxs-lookup"><span data-stu-id="3946d-142">1 with Sync on</span></span> | <span data-ttu-id="3946d-143">同步開啟</span><span class="sxs-lookup"><span data-stu-id="3946d-143">Sync ON</span></span><br><span data-ttu-id="3946d-144">先前已啟用功能：否</span><span class="sxs-lookup"><span data-stu-id="3946d-144">Feature enabled previously: No</span></span><br><span data-ttu-id="3946d-145">回應同意 UI：無</span><span class="sxs-lookup"><span data-stu-id="3946d-145">Response to Consent UI: None</span></span> | <span data-ttu-id="3946d-146">功能會預設啟用，且瀏覽器啟動 2 分鐘後會顯示通知泡泡。</span><span class="sxs-lookup"><span data-stu-id="3946d-146">Feature enabled by default and a notice bubble is shown 2 min after browser starts.</span></span><br><span data-ttu-id="3946d-147">- 如果在此之後關閉同步，則會停用該功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-147">- If sync is turned off after that, the feature is disabled.</span></span><br><span data-ttu-id="3946d-148">- 如果在變更同步之前關閉該功能，同步將不再影響該功能。</span><span class="sxs-lookup"><span data-stu-id="3946d-148">-  Feature turned off before altering sync, sync will no longer affect the feature.</span></span>   |
| <span data-ttu-id="3946d-149">2 同步開啟</span><span class="sxs-lookup"><span data-stu-id="3946d-149">2 with Sync on</span></span> | <span data-ttu-id="3946d-150">同步開啟</span><span class="sxs-lookup"><span data-stu-id="3946d-150">Sync ON</span></span><br><span data-ttu-id="3946d-151">先前已啟用功能：是</span><span class="sxs-lookup"><span data-stu-id="3946d-151">Feature enabled previously: Yes</span></span><br><span data-ttu-id="3946d-152">回應同意 UI：無</span><span class="sxs-lookup"><span data-stu-id="3946d-152">Response to Consent UI: None</span></span> | <span data-ttu-id="3946d-153">功能會與使用者選擇保持相同。</span><span class="sxs-lookup"><span data-stu-id="3946d-153">Feature stays the same as user choice.</span></span>  <span data-ttu-id="3946d-154">不顯示通知泡泡，對功能值的同步變更不會造成影響。</span><span class="sxs-lookup"><span data-stu-id="3946d-154">Notice bubble isn't shown and there's no affect of sync change on feature value.</span></span>|
| <span data-ttu-id="3946d-155">3 同步關閉</span><span class="sxs-lookup"><span data-stu-id="3946d-155">3 with Sync off</span></span> | <span data-ttu-id="3946d-156">同步關閉</span><span class="sxs-lookup"><span data-stu-id="3946d-156">Sync Off</span></span><br><span data-ttu-id="3946d-157">先前已啟用功能：否</span><span class="sxs-lookup"><span data-stu-id="3946d-157">Feature enabled previously: No</span></span><br><span data-ttu-id="3946d-158">回應同意 UI：無</span><span class="sxs-lookup"><span data-stu-id="3946d-158">Response to Consent UI: None</span></span> | <span data-ttu-id="3946d-159">同步將會關閉，且功能將保持停用</span><span class="sxs-lookup"><span data-stu-id="3946d-159">Sync will be off and the feature will stay disabled</span></span><br><span data-ttu-id="3946d-160">- 在此之後的任何時間點，如果使用者開啟同步而未變更功能：功能會啟用，且在開啟同步的 2 分鐘後會顯示自動啟用通知。</span><span class="sxs-lookup"><span data-stu-id="3946d-160">- At any point after that if user turns the sync on without altering the feature: the feature is enabled and auto-enablement notification is shown 2 minutes after Sync is turned on.</span></span> <br> <span data-ttu-id="3946d-161">- 如果再次關閉同步，則會停用該功能</span><span class="sxs-lookup"><span data-stu-id="3946d-161">- If sync is turned off again, the  feature is disabled</span></span> <br><span data-ttu-id="3946d-162">- 如果在開啟同步之前變更了功能，同步將不會再影響密碼監視器。</span><span class="sxs-lookup"><span data-stu-id="3946d-162">- If the feature is changed before turning on sync, sync will no longer affect Password Monitor.</span></span>  |  
| <span data-ttu-id="3946d-163">4 同步關閉</span><span class="sxs-lookup"><span data-stu-id="3946d-163">4 with Sync off</span></span> | <span data-ttu-id="3946d-164">同步關閉</span><span class="sxs-lookup"><span data-stu-id="3946d-164">Sync OFF</span></span><br><span data-ttu-id="3946d-165">先前已啟用功能：是</span><span class="sxs-lookup"><span data-stu-id="3946d-165">Feature enabled previously: Yes</span></span><br><span data-ttu-id="3946d-166">回應同意 UI：無</span><span class="sxs-lookup"><span data-stu-id="3946d-166">Response to Consent UI: None</span></span> | <span data-ttu-id="3946d-167">功能會與使用者選擇保持相同，不會顯示通知泡泡，且對功能值的同步變更不會造成影響。</span><span class="sxs-lookup"><span data-stu-id="3946d-167">Feature stays the same as user choice, notice bubble isn't shown, and there's no effect of sync change on the feature value.</span></span>  |

<span data-ttu-id="3946d-168">此外，如果使用者登入時使用的工作帳戶是由下列任何一原則所限制，就「不會」為使用者自動啟用該功能：</span><span class="sxs-lookup"><span data-stu-id="3946d-168">In addition, if a user is signed-in using a work account that is restricted via policies for any of the following, the feature will NOT be auto-enabled for them:</span></span>

- <span data-ttu-id="3946d-169">密碼監視器已停用</span><span class="sxs-lookup"><span data-stu-id="3946d-169">Password Monitor is disabled</span></span>  
- <span data-ttu-id="3946d-170">密碼同步已停用</span><span class="sxs-lookup"><span data-stu-id="3946d-170">Password Sync is disabled</span></span>
- <span data-ttu-id="3946d-171">與 Microsoft 伺服器共用資料功能已停用</span><span class="sxs-lookup"><span data-stu-id="3946d-171">Sharing of data with Microsoft servers is disabled</span></span>

## <span data-ttu-id="3946d-172">常見問題集</span><span class="sxs-lookup"><span data-stu-id="3946d-172">Frequently Asked Questions</span></span>

### <span data-ttu-id="3946d-173">如何為我的組織停用密碼監視器？</span><span class="sxs-lookup"><span data-stu-id="3946d-173">How can Password Monitor be disabled for my organization?</span></span>

<span data-ttu-id="3946d-174">您可以透過以下方式，為您的組織停用密碼監視器：</span><span class="sxs-lookup"><span data-stu-id="3946d-174">You can disable Password Monitor for your organization by:</span></span>
- <span data-ttu-id="3946d-175">使用 PasswordMonitorAllowed 群組原則。</span><span class="sxs-lookup"><span data-stu-id="3946d-175">Using the PasswordMonitorAllowed group policy.</span></span>
- <span data-ttu-id="3946d-176">停止同步和傳送資料到 Microsoft 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3946d-176">Stopping data from being synchronized and sent to Microsoft servers.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3946d-177">密碼監視器甚至能在密碼同步停用時運作，只要使用者已明確同意開啟該功能，或已自行透過 [設定] 開啟該功能即可。</span><span class="sxs-lookup"><span data-stu-id="3946d-177">Password Monitor can work even if Password Sync is disabled, as long as the user has given explicit consent to turn the feature On or have turned it on themselves via Settings.</span></span>

### <span data-ttu-id="3946d-178">如果某個使用者的該功能已自動啟用，但透過 [設定] 關閉密碼監視器，會發生什麼情況？</span><span class="sxs-lookup"><span data-stu-id="3946d-178">What happens if a user for whom the feature has been auto-enabled, turns Password Monitor off via Settings?</span></span>

<span data-ttu-id="3946d-179">將採用使用者設定中的資訊，因此該使用者的功能會保持停用。</span><span class="sxs-lookup"><span data-stu-id="3946d-179">The user setting is honored and the feature will remain disabled for that user.</span></span> <span data-ttu-id="3946d-180">不過，系統可能會向他們再次顯示同意對話方塊，以防他們先前未曾回應同意提示。</span><span class="sxs-lookup"><span data-stu-id="3946d-180">However, they might be shown a consent dialog again in case they've never previously responded to the consent prompt.</span></span>

## <span data-ttu-id="3946d-181">請參閱</span><span class="sxs-lookup"><span data-stu-id="3946d-181">See also</span></span>

- [<span data-ttu-id="3946d-182">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3946d-182">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)