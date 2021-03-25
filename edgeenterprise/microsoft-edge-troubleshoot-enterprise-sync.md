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
# <a name="diagnose-and-fix-microsoft-edge-sync-issues"></a>診斷並修正 Microsoft Edge 同步處理問題

本文針對 Azure Active Directory (Azure AD) 環境中最常遇到的同步處理問題提供疑難排解指導方針。 它還包含用於收集疑難排解同步處理問題所需的記錄建議使用工具。

如果使用者遇到跨裝置同步處理瀏覽器資料的問題，可以嘗試 [重設同步處理](edge-learnmore-reset-data-in-cloud.md)。如果還是無法解決問題，系統管理員或支援人員可以使用下列指導方針以修正同步處理問題。

> [!NOTE]
> 除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="identity-issues-versus-sync-issues"></a>身分識別問題與同步處理問題

開始之前，瞭解身分識別問題與同步處理問題之間的差異非常重要。 在瀏覽器中維護使用者身分識別的常見使用案例就是支援同步處理。因此，身分識別問題通常會與同步處理問題混淆。 在開始疑難排解同步處理之前，請瞭解身分識別與同步處理問題之間的差異。

在您將問題視為同步處理問題之前，請先檢查使用者是否已使用有效的帳戶登入瀏覽器。

下一個螢幕擷取畫面顯示身分識別錯誤的範例。 錯誤為「**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**」，這可在 *edge://sync-internals* 的 **Credentials** 下找到：

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

## <a name="common-sync-issues"></a>常見的同步問題

### <a name="issue-cant-access-m365-or-azure-information-protection-subscription"></a>問題：無法存取 M365 或 Azure 資訊保護訂閱

您是否有先前的 M365 或 Azure 資訊保護 (AIP) 訂閱已過期，然後以新訂閱將其取代？ 如果是這樣，則租使用者識別碼已變更，且需要重設服務資料。 請參閱**密碼錯誤問題**中重置資料的說明。

### <a name="issue-sync-is-not-available-for-this-account"></a>問題：「此帳戶無法使用同步處理」。

如果 Azure Active Directory 帳戶遇到此錯誤，或 DISABLED_BY_ADMIN 出現在 *edge://sync-internals*中，依次執行下一步驟中的步驟，直到問題得到解决。。

> [!NOTE]
> 由於此錯誤的來源通常是需要在 Azure Active Directory 租用戶中變更設定，因此這些疑難排解步驟只能由租用戶系統管理員執行，而不能由使用者執行。

1. 確認企業租使用者具有支援的 M365 訂閱。 目前提供的可用訂閱類型清單 [如下](/azure/information-protection/activate-office365)。 如果租使用者沒有受支援的訂閱，他們可以單獨購買 Azure 資訊保護，或升級至其中一個支援的訂閱。
2. 如果支援的訂閱可用，請驗證租用戶是否具有可用的 Azure 資訊保護 (AIP)。 有關檢查 AIP 狀態以及在必要時啟動 AIP 的說明，請參見[此處](/azure/information-protection/activate-office365)。
3. 如果步驟 2 顯示 AIP 處於使用中，但仍無法進行同步處理，請開啟企業狀態漫遊 (ESR)。 啟用 ESR 的指示在 [這裡](/azure/active-directory/devices/enterprise-state-roaming-enable)。 請注意，ESR 不需要保持開啟狀態。 如果此步驟修正了問題，您可以關閉 ESR。
4. 確認 Azure 資訊保護未透過加入原則限定範圍。 您可以使用 [AadrmOnboardingControlPolicy](/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式來查看是否啟用了範圍。 接下來的兩個範例顯示了一個不限範圍的設定和一個範圍設定為特定安全性群組的設定。

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

   如果已啟用範圍，則受影響的使用者應該新增至該範圍的安全性群組，或者應該移除該範圍。 在下方的範例中，上線已將 AIP 的範圍設定為指定的安全性群組，應使用 [Set-AadrmOnboardingControlPolicy](/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式移除該範圍。

5. 確認 IPCv3Service 已在租用戶中開啟。 [AadrmConfiguration](/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) PowerShell 小程式顯示服務的狀態。

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="查看是否已啟用 IPCv3Service。":::

6. 如果問題未修正，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。

### <a name="issue-stuck-at-setting-up-sync-or-couldnt-connect-to-the-sync-server-retrying"></a>問題：停滯在「正在設定同步處理...」或「無法連線到同步處理伺服器。 正在重試...」

1. 請嘗試登出，然後再登入。
2. 移至 *edge://sync-internals*。 如果在「**輸入資訊**」區段下出現下列錯誤，請跳至下列問題， **發生密碼錯誤**。

   `"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered"`

3. 請嘗試抓取伺服器端點。 用戶端的伺服器端點可在 *edge://sync-internals*中取得。 下一個螢幕擷取畫面顯示 [**環境資訊**] 底部的端點資訊。

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-endpoint-info.png" alt-text="端點資訊":::

4. 如果伺服器端點為空白，或無法抓取伺服器並且環境中存在防火牆，請確認用戶端電腦可使用必要的服務端點。

   - Microsoft Edge 同步處理服務端點：
     - [https://edge-enterprise.activity.windows.com](https://edge-enterprise.activity.windows.com)
     - [https://edge.activity.windows.com](https://edge.activity.windows.com)
    - Azure 資訊保護端點：
      - [https://api.aadrm.com](https://api.aadrm.com) (適用於多數租用戶)
      - [https://api.aadrm.de](https://api.aadrm.de) (適用於德國的租用戶)
      - [https://api.aadrm.cn](https://api.aadrm.cn) (適用於中國的租用戶)
   - [Windows 通知服務端點](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)。

5. 如果問題仍未解決，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。

### <a name="issue-cryptographer-error-encountered"></a>問題：發生密碼錯誤

此錯誤可在 *edge://sync-internals* 中的 **Type info** 下看到，並且可能表示需要重設使用者的服務端資料。 下列範例顯示密碼編譯錯誤訊息：
<br>"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".

1. 重新啟動 Microsoft Edge 並瀏覽至 *edge://sync-internals*，然後查看 "**AAD Account Key Status**" 區段
   - "Success" in "Last MIP Result"：密碼錯誤意味著伺服器資料可能被遺失的金鑰加密。 需要重設資料才能繼續同步處理。
   - "No permissions" in "Last MIP Result"：這可能是由 Azure AD 變更或租用戶訂閱變更引起的。 需要重設資料才能繼續同步處理。
   - 其他錯誤可能意味著伺服器設定問題。
2. 如果需要重設資料，請參閱 [重設雲端中的 Microsoft Edge 資料](edge-learnmore-reset-data-in-cloud.md)。

### <a name="issue-sync-has-been-turned-off-by-your-administrator"></a>問題：「您的系統管理員已關閉同步處理。」

請確定未設定 [SyncDisabled 原則](./microsoft-edge-policies.md#syncdisabled)。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業同步](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)