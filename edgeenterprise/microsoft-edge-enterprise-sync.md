---
title: Microsoft Edge 企業版同步處理
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/03/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 企業版同步處理
ms.openlocfilehash: a6d01356db478871a7c6b386bbb731b32dc4739a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979587"
---
# Microsoft Edge 企業版同步處理

本文介紹如何使用 Microsoft Edge 在所有登入裝置上同步處理我的最愛、密碼和其他瀏覽器資料。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 概觀

Microsoft Edge 同步可讓使用者跨所有登入裝置存取其瀏覽資料。 同步支援的資料包括：

- 我的最愛
- 密碼
- 地址等 (表單填滿)
- 集合
- 設定

同步功能透過使用者同意啟用，使用者可以為上面列出的每種資料類型開啟或關閉同步。

> [!NOTE]
> 將上載其他裝置連線和設定資料 (如裝置名稱、品牌和型號) 以支援同步功能。

## 必要條件

目前 Azure Active Directory (Azure AD) 帳戶的 Microsoft Edge 同步適用於以下訂閱：

- Azure AD Premium (P1 和 P2)
- M365 商務進階版
- Office 365 E3 及以上
- Azure 資訊保護 (AIP) (P1 和 P2)
- 所有 EDU 訂閱 (O365 A1 或以上、M365 A1 或以上，或 Azure 資訊保護 P1 或 P2 (學生或教職員))

> [!NOTE]
> 同步相依於 Azure 資訊保護 (AIP) 提供的保護服務，以保護同步資料。 此服務目前可用於上述訂閱。 若要查看具有 AIP 的 SKU 的完整清單，請參閱[資訊保護定價](https://azure.microsoft.com/pricing/details/information-protection/)。

## Microsoft Edge 同步的設定選項

以下設定選項可用於啟用 Microsoft Edge 同步：

- Azure 資訊保護 (AIP)
- Azure AD 企業狀態漫遊 (ESR)

如果停用 AIP 和 ESR，使用者將看到一條錯誤訊息，指示其帳戶無法進行同步。

### Azure 資訊保護 (AIP)

如果為租用戶啟用了 Azure 資訊保護 (AIP) 服務，則無論使用何種授權，所有使用者都可以同步 Microsoft Edge 資料。 有關如何解啟用 AIP 的指示，可以在[此處](https://docs.microsoft.com/azure/information-protection/activate-office365)找到。

若要限制同步到某組使用者，可以為這些使用者啟用 [AADRM 上線控制原則](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)。 如果在確保所有必要的使用者都已上線後仍無法使用同步處理，請確定使用 [Get-AIPServiceIPCv3](https://docs.microsoft.com/powershell/module/aipservice/Get-AipServiceIPCv3?view=azureipps) PowerShell Cmdlet 來啟用 IPCv3Service。

> [!CAUTION]
> 啟用 Azure 資訊保護也會限制其他使用 AIP 應用程式的存取，例如 Microsoft Word 或 Microsoft Outlook。

### Azure AD 企業狀態漫遊 (ESR)

如果為任何使用者或租用戶啟用了 Azure Active Directory [企業狀態漫遊](https://docs.microsoft.com/azure/active-directory/devices/enterprise-state-roaming-overview) (ESR) 功能，則無論上線控制原則設定如何，他們都可以使用 Microsoft Edge 同步功能。

## Microsoft Edge 和企業狀態漫遊

新 Microsoft Edge 是一個跨平台應用程式，提供跨其所有裝置同步使用者資料的擴展範圍，並且不再是 Azure AD 企業狀態漫遊的一部分。 但是，新的 Microsoft Edge 將履行 ESR 的資料保護承諾，例如自攜金鑰的能力。 有關詳細資訊，請參閱 [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。

## 同步群組原則

以下群組原則影響 Microsoft Edge 同步：

- [SyncDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#syncdisabled)：完全停用同步。
- [SavingBrowserHistoryDisabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#savingbrowserhistorydisabled)：停用儲存瀏覽歷程記錄和同步。此原則還會停用開啟索引標籤同步。
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)：設定要從同步中除的類型清單。

## 常見問題集

### 安全性和伺服器/資料合規性

#### 已同步的資料是否已加密？ 

資料在傳輸時會使用 TLS 1.2 或更高版本加密，此外，資料在 Microsoft 服務存放時則使用 AES256 加密。

#### Microsoft Edge 同步資料儲存在哪裡？

Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。 例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。

#### 除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？

不。

#### 租用戶系統管理員是否可以使用自己的金鑰？

是的，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。

#### 企業同步適用的服務條款為何？

服務條款與您的 Azure AD 訂閱相同。 所有 Azure AD 服務條款最終都需遵守 Microsoft 的[線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。

#### Microsoft Edge 是否支援政府社群雲端 (GCC) High 合規性？

尚不支援。 GCC High 是第 D 層，而 Microsoft Edge 最多支援第 C 層。

### 套用同步

#### 決定留在舊版 Microsoft Edge 的企業和教育客戶會發生什麼情況？

目前版本的 Microsoft Edge 瀏覽器將繼續參與 ESR 方案。

#### 為什麼我需要進階 Azure AD 訂閱，才能進行同步？

企業同步取決於 Azure 資訊保護，而這並未在所有 Azure AD 層中提供。

#### Microsoft Edge 同步會根據企業狀態漫遊嗎？

不。 ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。 如需詳細資訊，請參閱 [Microsoft Edge Sync](microsoft-edge-enterprise-sync.md) [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)。

#### Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？

目前並未計劃支援此類同步。 如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)。

#### 新的 Microsoft Edge 瀏覽器將與舊版 Microsoft Edge 同步處理嗎？

不，不會。 我們相信，連接這兩個生態系統將導致新 Microsoft Edge 同步可靠性受影響。 我們將確保將現有資料移轉到新的 Microsoft Edge。 使用者還可以從自己選擇的瀏覽器匯入資料。 這也意味著新的 Microsoft Edge 瀏覽器將不能與 IE 同步。

### 管理同步

#### 可以阻止我的使用者與個人租用戶進行同步嗎？

沒有直接的做法，但您可以使用 [RestrictSigninToPattern](https://docs.microsoft.com/deployedge/microsoft-edge-policies#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
