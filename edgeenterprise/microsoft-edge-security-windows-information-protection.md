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
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979334"
---
# <a name="microsoft-edge-support-for-windows-information-protection-wip"></a>Microsoft Edge 對 Windows 資訊保護 (WIP) 的支援

本文說明 Microsoft Edge 如何支援 Windows 資訊保護 (WIP)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 81 或更新版本。

## <a name="overview"></a>概觀

Windows 資訊保護 (WIP) 是 Windows 10 的功能，可協助保護企業資料免於受到未經授權或意外的洩露。 隨著遠端工作的增加，在工作場所以外共用公司資料的風險也增加了。 當公司裝置上存在個人活動和工作活動時，這種風險就會增加。

Microsoft Edge 支援使用 WIP 來協助保護 Web 環境中的內容，因為使用者通常是在 Web 環境中共用和散布內容。

### <a name="system-requirements"></a>系統需求

下列需求適用於企業中使用 WIP 的裝置：

- Windows 10 (版本 1607) 或更新版本
- 僅限 Windows 用戶端 SKU
- [WIP 必要條件](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#prerequisites)所述的其中一個管理解決方案

### <a name="windows-information-protection-benefits"></a>Windows 資訊保護的優點

WIP 有下列優點：

- 清楚區分個人和公司資料，而不需要員工切換環境或應用程式。
- 為現有的商務應用程式組合提供額外的資料保護，而不需要更新應用程式。
- 可從遠端抹除 Intune 行動裝置管理 (MDM) 註冊裝置上的公司資料，且不會影響個人資料。 
- 針對追蹤問題和補救動作 (例如使用者的合規性訓練) 的稽核報告。
- 與您現有的管理系統整合，以設定、部署、管理 WIP。 例如 Microsoft Intune、Microsoft Endpoint 設定管理員、或是您目前的行動裝置管理 (MDM) 系統。

## <a name="wip-policy-and-protection-modes"></a>WIP 原則和保護模式

使用原則，您可以設定下表所述的四種保護模式。 如需詳細資訊，請參閱 [WIP 保護模式](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip#wip-protection-modes)。

| 模式 | 說明 |
|------|-------------|
| 封鎖 | WIP 會尋找不適當的資料共用做法，並阻止員工完成該動作。 此搜尋可包含將企業資訊共用至非企業保護的應用程式，以及在應用程式之間共用企業資料，或嘗試在組織網路以外的地方進行共用。 |
| 允許覆寫 | WIP 會尋找不適當的資料共用，並在員工做出可能不安全的事情時，對該員工發出警告。 不過，此管理模式允許員工覆寫原則並共用資料，同時將該動作記錄到您的稽核記錄中。 |
| 無訊息 | WIP 會以無訊息方式執行、記錄不適當的資料共用，但在處於允許覆寫模式時，不會阻止任何提示員工進行互動的動作。 不允許的動作 (例如，不適當地嘗試存取網路資源或 WIP 所保護資料的應用程式) 仍會遭到阻止。 |
| 關閉 | WIP 會關閉，且不會協助保護或稽核您的資料。 關閉 WIP 之後，會嘗試在本機連接的磁碟機上將任何有 WIP 標記的檔案解密。 如果您重新開啟 WIP 保護，之前的解密和原則資訊並不會自動重新套用。
 |

## <a name="wip-features-supported-in-microsoft-edge"></a>Microsoft Edge 支援的 WIP 功能

從 Microsoft Edge 版本 81 開始，支援下列功能：

- 用網址列上的公事包圖示來表示工作網站。  
- 從工作位置下載的檔案會自動加密。
- 將工作檔案上傳到非工作位置時，強制執行無訊息/封鎖/覆寫。  
- 拖放檔案時強制執行無訊息/封鎖/覆寫。
- 執行剪貼簿動作時，強制執行無訊息/封鎖/覆寫。
- 從非工作設定檔瀏覽到工作位置，會自動重新導向至工作設定檔 (與 Azure AD 身分識別關聯)。
- IE 模式支援完整的 WIP 功能。

## <a name="working-with-wip-in-microsoft-edge"></a>在 Microsoft Edge 中使用 WIP

啟用 Microsoft Edge 的 WIP 支援之後，使用者將會看到正在存取工作相關資訊。 下個螢幕擷取畫面的網址列中顯示公事包圖示，指出正透過瀏覽器存取工作相關資訊。

 ![標示為「工作」網站的網址列指示器](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-notify.png)

Microsoft Edge 可讓使用者在未核准的網站中共用受保護的內容。 下個螢幕擷取畫面中顯示的 Microsoft Edge 提示，提醒使用者將允許在未獲核准的網站中使用受保護內容。

 ![提示受保護的內容覆寫](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-override.png)

## <a name="configure-policies-to-support-wip"></a>設定原則以支援 WIP

在 Microsoft Edge 中使用 WIP 需要具備工作設定檔。

### <a name="ensure-the-presence-of-a-work-profile"></a>確定有工作設定檔

在混合式聯結的電腦上，Microsoft Edge 會自動以 Azure Active Directory (Azure AD) 帳戶登入。 為了確保使用者沒有移除 WIP 需要的這個設定檔，請設定下列原則：

- [NonRemovableProfileEnabled](./microsoft-edge-policies.md#nonremovableprofileenabled)

> [!NOTE]
> 如果您的環境不是混合式聯結，您可以使用下列指示進行混合式聯結： [規劃混合式 Azure Active Directory 聯結的實作](/azure/active-directory/devices/hybrid-azuread-join-plan)。

如果混合式聯結不可行，您可以使用內部部署的 Active Directory 帳戶來允許 Microsoft Edge 以使用者網域帳戶自動建立特別工作設定檔。 請注意，內部部署帳戶可能不能使用 Azure AD 的所有功能，例如雲端同步處理、Office NTP 等。

#### <a name="active-directory-ad-accounts"></a>Active Directory (AD) 帳戶

您必須為 AD 帳戶設定下列原則，好讓 Microsoft Edge 自動建立特別工作設定檔。

- [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin)

### <a name="windows-policies-for-wip"></a>適用於 WIP 的 Windows 原則

您可以使用 Windows 原則來設定 WIP。 如需詳細資訊，請參閱[使用 Microsoft Intune 建立和部署 WIP 原則](/windows/security/information-protection/windows-information-protection/overview-create-wip-policy)。

## <a name="frequently-asked-questions"></a>常見問題集

### <a name="how-do-i-resolve-error-code--2147024540"></a>如何解決錯誤碼 -2147024540？

此錯誤碼對應於以下 Windows 資訊保護錯誤：*ERROR_EDP_POLICY_DENIES_OPERATION：Windows 資訊保護原則封鎖了請求的操作。如需詳細資訊，請連絡您的系統管理員*。

當組織啟用 Windows 資訊保護 (WIP) 以僅允許使用已核准應用程式的使用者存取公司資源時，Microsoft Edge 會顯示此錯誤。 在這種情況下，由於 Microsoft Edge 不在已核准的應用程式清單中，管理員必須更新 WIP 原則以授予對 Microsoft Edge 的存取權限。

下列螢幕擷取畫面顯示如何使用 Microsoft Intune 將 Microsoft Edge 新增為可供 WIP 使用的應用程式。

 ![將 Microsoft Edge 新增為 WIP 應用程式的 Intune 對話方塊](./media/microsoft-edge-security-windows-information-protection/microsoft-edge-wip-exemption.png)

如果您並非使用 Microsoft Intune，請下載 [WIP 企業 AppLocker 原則](https://download.microsoft.com/download/8/9/9/8995d820-065c-4ab1-aa2a-9d6dc0cd7ffa/MsEdge%20-%20WIP%20Enterprise%20AppLocker%20Policy%20Files.zip)檔案並套用檔案中的原則更新。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise) 
- [使用 Windows 資訊保護保護企業資料](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)