---
title: 設定和疑難排解 Microsoft Edge 同步處理
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 01/22/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定和疑難排解 Microsoft Edge 同步處理
ms.openlocfilehash: 36912d2fd1c33a227ce1d4b7c912f6ef1dfdcc00
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297451"
---
# 設定和疑難排解 Microsoft Edge 同步處理

本文介紹如何設定和使用 Microsoft Edge 在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。 本文還為最常見的同步問題提供了疑難排解步驟。 它還包含用於收集疑難排解所需記錄的建議使用工具。

> [!NOTE]
> 除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。

## 概觀

Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。 同步支援的資料包括：

- 我的最愛
- 密碼
- 地址等 (表單填滿)
- 集合
- 設定
- 擴充功能
- [開啟] 所引標籤 (適用於 Microsoft Edge 版本88)
- 歷程記錄 (適用於 Microsoft Edge 版本88)

同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。

> [!NOTE]
> 將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。

## 必要條件

Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：

- Azure AD 進階版 (P1 或 P2) 
- M365 商務進階版
- Office 365 E1 及以上版本
- Azure 資訊保護 (AIP)(P1 或 P2)
- 所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)

## 同步群組原則

您可以使用以下群組原則來設定和管理 Microsoft Edge 同步處理：

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。
- [AllowDeletingBrowserHistory](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中排除的類型清單。
- [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。 如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-on-premises-sync)。
- [ForceSync]( https://docs.microsoft.com/deployedge/microsoft-edge-policies#forcesync)：依預設開啟同步處理，且不需要使用者同意同步處理。  

## 設定 Microsoft Edge 同步處理

Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。 當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。 有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。

若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](https://docs.microsoft.com/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?view=azureipps&preserve-view=true) 。 如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/get-aipserviceipcv3?view=azureipps&preserve-view=true) PowerShell Cmdlet 來啟用 IPCv3Service。

> [!CAUTION]
> 啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。 此外，任何用來限制 Microsoft Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。

## Microsoft Edge 和企業狀態漫遊 (ESR)

Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。 但是，Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。 有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。

## 疑難排解同步處理問題

本章節為最常出現的同步問題提供了疑難排解步驟。 它還包含用於收集疑難排解所需記錄的建議使用工具。

### 身分識別問題與同步處理問題

在瀏覽器中維護使用者身分識別的常見使用案例就是支援同步處理。因此，身分識別問題通常會與同步處理問題混淆。 在開始疑難排解同步處理之前，請瞭解身分識別與同步處理問題之間的差異。

在您將問題視為同步處理問題之前，請先檢查使用者是否已使用有效的帳戶登入瀏覽器。

下一個螢幕擷取畫面顯示身分識別錯誤的範例。 錯誤為「**Last Token Error, EDGE_AUTH_ERROR: 3, 54, 3ea**」，這可在 *edge://sync-internals* 的 **Credentials** 下找到：

:::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-identity-issue.png" alt-text="Last Token Error EDGE_AUTH_ERROR: 3,54, 3ea":::

### 常見的同步問題

#### 問題：無法存取 M365 或 Azure 資訊保護訂閱

您是否有先前的 M365 或 Azure 資訊保護 (AIP) 訂閱已過期，然後以新訂閱將其取代？ 如果是這樣，則租使用者識別碼已變更，且需要重設服務資料。 請參閱**密碼錯誤問題**中重置資料的說明。

#### 問題：「此帳戶無法使用同步處理」。

如果 Azure Active Directory 帳戶遇到此錯誤，或 DISABLED_BY_ADMIN 出現在 *edge://sync-internals*中，依次執行下一步驟中的步驟，直到問題得到解决。。

> [!NOTE]
> 由於此錯誤的來源通常是需要在 Azure Active Directory 租用戶中變更設定，因此這些疑難排解步驟只能由租用戶系統管理員執行，而不能由使用者執行。

1. 確認企業租使用者具有支援的 M365 訂閱。 目前提供的可用訂閱類型清單 [如下](https://docs.microsoft.com/azure/information-protection/activate-office365)。 如果租使用者沒有受支援的訂閱，他們可以單獨購買 Azure 資訊保護，或升級至其中一個支援的訂閱。
2. 如果支援的訂閱可用，請驗證租用戶是否具有可用的 Azure 資訊保護 (AIP)。 有關檢查 AIP 狀態以及在必要時啟動 AIP 的說明，請參見[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)。
3. 如果步驟 2 顯示 AIP 處於使用中，但仍無法進行同步處理，請開啟企業狀態漫遊 (ESR)。 啟用 ESR 的指示在 [這裡](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-enable)。 請注意，ESR 不需要保持開啟狀態。 如果此步驟修正了問題，您可以關閉 ESR。
4. 確認 Azure 資訊保護未透過加入原則限定範圍。 您可以使用 [AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmonboardingcontrolpolicy?view=azureipps)  PowerShell 小程式來查看是否啟用了範圍。 接下來的兩個範例顯示了一個不限範圍的設定和一個範圍設定為特定安全性群組的設定。

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


   如果已啟用範圍，則受影響的使用者應該新增至該範圍的安全性群組，或者應該移除該範圍。 在下方的範例中，上線已將 AIP 的範圍設定為指定的安全性群組，應使用 [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps) PowerShell 小程式移除該範圍。

5. 確認 IPCv3Service 已在租用戶中開啟。 [AadrmConfiguration](https://docs.microsoft.com/powershell/module/aadrm/get-aadrmconfiguration?view=azureipps) PowerShell 小程式顯示服務的狀態。

   :::image type="content" source="media/microsoft-edge-enterprise-sync-configure-and-troubleshoot/sync-scoped-cfg-example.png" alt-text="查看是否已啟用 IPCv3Service。":::

6. 如果問題未修正，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。

#### 問題：停滯在「正在設定同步處理...」或「無法連線到同步處理伺服器。 正在重試...」

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
   - [Windows 通知服務端點](https://docs.microsoft.com/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)。

5. 如果問題仍未解決，請連絡 [Microsoft Edge 支援](https://www.microsoftedgeinsider.com/support)。

### 問題：發生密碼錯誤

此錯誤可在 *edge://sync-internals* 中的 **Type info** 下看到，並且可能表示需要重設使用者的服務端資料。 下列範例顯示密碼編譯錯誤訊息：
<br>"Error:GenerateCryptoErrorsForTypes@../../components/sync/driver/data_type_manager_impl.cc:42, cryptographer error was encountered".

1. 重新啟動 Microsoft Edge 並瀏覽至 *edge://sync-internals*，然後查看 "**AAD Account Key Status**" 區段
   - "Success" in "Last MIP Result"：密碼錯誤意味著伺服器資料可能被遺失的金鑰加密。 需要重設資料才能繼續同步處理。
   - "No permissions" in "Last MIP Result"：這可能是由 Azure AD 變更或租用戶訂閱變更引起的。 需要重設資料才能繼續同步處理。
   - 其他錯誤可能意味著伺服器設定問題。
2. 如果需要重設資料，請參閱 [重設雲端中的 Microsoft Edge 資料](edge-learnmore-reset-data-in-cloud.md)。

#### 問題：「您的系統管理員已關閉同步處理。」

請確定未設定 [SyncDisabled 原則](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)。

## 常見問題集

### 安全性和伺服器/資料合規性

#### 已同步的資料是否已加密？

資料會在使用 TLS 1.2 或更高版本的傳輸中進行加密。 在 Microsoft 服務中，所有資料類型都使用 AES128 進行了額外的加密。 除了用於 [開啟] 索引標籤和 [歷程記錄同步處理] 外的所有資料類型，在離開使用者的裝置前都會透過 [Azure 資訊保護](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern)原則管理的金鑰，另行加密。

#### 為什麼[ 開啟] 索引標籤和 [歷程記錄資料] 沒有更多的用戶端加密？

爲了減少使用者裝置上的資源使用率，歷程記錄資料是根據 [開啟] 索引標籤漫遊資料在伺服器端產生的。 此資料的用戶端加密無法進行此處理流程。 若要停用 [開啟] 索引標籤和 [歷程記錄同步]，請套用 [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled) 或 [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) 原則。

#### 租用戶系統管理員是否可以使用自己的金鑰？

是，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。

#### Microsoft Edge 同步資料儲存位置？

Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。 例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。

#### 除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？

不。

#### 企業同步適用的服務條款為何？

Microsoft Edge 同步處理的服務條款需遵守 Microsoft Edge 中的 Microsoft 軟體授權，可於  *edge://terms*中進行查看。 您的 Azure AD 訂閱與服務條款最終都需遵守 Microsoft 的 [線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。

#### Microsoft Edge 是否支援政府社群雲端 (GCC) 高合規性？

尚不支援。 針對 GCC High 雲端的客戶，已停用 Microsoft Edge 同步處理功能。

### 套用同步處理

#### 為什麼並非所有 M365 訂閱都支援 Microsoft Edge 同步？

企業同步的方式取決於 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)，其並非可在所有 M365 訂閱中取得。

#### Microsoft Edge 同步是否基於企業狀態漫遊？

不。 ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。 如需詳細資訊，請參閱 [Microsoft Edge Sync](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-sync) [Microsoft Edge 和企業狀態漫遊](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-enterprise-state-roaming)。

#### Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？

目前並未計劃支援此類同步。 如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。

#### Microsoft Edge 會與舊版 Microsoft Edge 進行同步處理嗎？

不，不會。 我們認為連結這兩個生態系統會導致 Microsoft Edge 同步可靠性受影響。 我們將確保現有資料移轉至 Microsoft Edge。 使用者還可以從自己選擇的瀏覽器中匯入資料，這也意味著 Microsoft Edge 將無法與 IE 同步。

### 管理同步

#### 可以阻止我的使用者與個人租用戶進行同步嗎？

沒有直接的做法，但您可以使用 [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。

## 請參閱

- [Microsoft Edge 企業同步](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
