---
title: 設定 Microsoft Edge 企業同步
ms.author: collw
author: AndreaLBarr
manager: silvanam
ms.date: 09/07/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 管理員和使用者選項，用於使 Microsoft Edge 同步處理我的最愛、密碼和其他瀏覽器資料。
ms.openlocfilehash: 5caec237eebcd18a83b8f32d638ace2fa2914e38
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979412"
---
# <a name="configure-microsoft-edge-enterprise-sync"></a>設定 Microsoft Edge 企業同步

本文說明系統管理員如何設定 Microsoft Edge，在所有已登入的裝置上同步處理使用者的我的最愛、密碼和其他瀏覽器資料。如果您不是系統管理員，請瀏覽本文，了解如何跨裝置登入和同步 Microsoft Edge。 
            [登入以跨裝置同步 Microsoft Edge](https://support.microsoft.com/microsoft-edge/sign-in-to-sync-microsoft-edge-across-devices-e6ffa79b-ed52-aa32-47e2-5d5597fe4674)。

> [!NOTE]
> 除非另有說明，否則適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="overview"></a>概觀

Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。 同步支援的資料包括：

- 我的最愛
- 密碼
- 地址等 (表單填滿)
- 集合
- 設定
- 擴充功能
- [開啟] 所引標籤 (適用於 Microsoft Edge 版本88)
- 歷程記錄 (適用於 Microsoft Edge 版本88)

同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。 如果使用者遇到同步處理問題，他們可能需要在 **設定** > **設定檔** > **重設同步處理**中重設同步處理。

> [!NOTE]
> 將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。

## <a name="prerequisites"></a>必要條件

Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下任何訂閱：

- Azure AD 進階版 (P1 或 P2) 
- M365 商務進階版、商務標準版或商務基本版
- Office 365 E1 及以上版本
- Azure 資訊保護 (AIP)(P1 或 P2)
- 所有 EDU 訂閱 (適用於學生或教職員的 Microsoft Apps、適用於學生或教職員的 Exchange Online、O365 A1 或以上、M365 A1 或以上或適用於學生或教職員的 Azure 資訊保護 P1 或 P2)

## <a name="sync-group-policies"></a>同步群組原則

系統管理員可以使用以下群組原則來設定和管理 Microsoft Edge 同步處理：

- 
            [SyncDisabled](./microsoft-edge-policies.md#syncdisabled)：完全停用同步。
- 
            [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled)：停用儲存瀏覽 [歷程記錄和同步處理]。此原則還會停用 [開啟] 索引標籤同步。
- 
            [AllowDeletingBrowserHistory](./microsoft-edge-policies.md#allowdeletingbrowserhistory)：當此原則設定為 [停用] 時，也會停用 [歷程記錄同步處理]。
- 
            [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled)：設定要從同步中排除的類型清單。
- 
            [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled)：允許 Active Directory (AD) 設定檔使用內部部署儲存體。 如需詳細資訊，請參閱[ 適用於 Active Directory (AD) 使用者的內部部署同步](./microsoft-edge-on-premises-sync.md)。
- 
            [ForceSync](/deployedge/microsoft-edge-policies#forcesync)：依預設開啟同步處理，且不需要使用者同意同步處理。  

## <a name="configure-microsoft-edge-sync"></a>設定 Microsoft Edge 同步處理

Microsoft Edge 同步處理的設定選項可透過 Azure 資訊保護 (AIP) 服務取得。 當為租用戶啟用 AIP，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。 有關如何解啟用 AIP 的指示，可以在[此處](/azure/information-protection/activate-office365)找到。

若要限制同步到某組使用者，可以為這些使用者啟用 [AIP 上線控制原則](/powershell/module/aipservice/set-aipserviceonboardingcontrolpolicy?preserve-view=true&view=azureipps) 。 如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](/powershell/module/aipservice/get-aipserviceipcv3?preserve-view=true&view=azureipps) PowerShell Cmdlet 來啟用 IPCv3Service。

> [!CAUTION]
> 啟用 Azure 資訊保護也會允許其他應用程式 (例如 Microsoft Word 或 Microsoft Outlook) 使用 AIP 來保護內容。 此外，任何用來限制 Microsoft Edge 同步處理的上線控制原則，也會使用 AIP 限制其他應用程式來保護內容。

## <a name="microsoft-edge-and-enterprise-state-roaming-esr"></a>Microsoft Edge 和企業狀態漫遊 (ESR)

Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。 但是，Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。 有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業同步](microsoft-edge-enterprise-sync.md)
- [診斷並修正 Microsoft Edge 同步處理問題](microsoft-edge-troubleshoot-enterprise-sync.md)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)