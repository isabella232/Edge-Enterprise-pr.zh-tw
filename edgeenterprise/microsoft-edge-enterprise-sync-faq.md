---
title: Microsoft Edge 企業同步常見問題集
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 企業同步的常見問題集。
ms.openlocfilehash: a13e1f02f6e871004d45f81159d5cf0a3397b6ad
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979423"
---
# <a name="microsoft-edge-enterprise-sync-faq"></a>Microsoft Edge 企業同步常見問題集

本文回答有關 Microsoft Edge 版本 77 或更新版本的企業同步常見問題。

## <a name="security-and-serverdata-compliance"></a>安全性和伺服器/資料合規性

### <a name="is-the-synced-data-encrypted"></a>已同步的資料是否已加密？

資料會在使用 TLS 1.2 或更高版本的傳輸中進行加密。 在 Microsoft 服務中，所有資料類型都使用 AES128 進行了額外的加密。 除了用於 [開啟] 索引標籤和 [歷程記錄同步處理] 外的所有資料類型，在離開使用者的裝置前都會透過 [Azure 資訊保護](./microsoft-edge-policies.md#restrictsignintopattern)原則管理的金鑰，另行加密。

### <a name="why-dont-open-tab-and-history-data-have-more-client-side-encryption"></a>為什麼[ 開啟] 索引標籤和 [歷程記錄資料] 沒有更多的用戶端加密？

爲了減少使用者裝置上的資源使用率，歷程記錄資料是根據 [開啟] 索引標籤漫遊資料在伺服器端產生的。 此資料的用戶端加密無法進行此處理流程。 若要停用 [開啟] 索引標籤和 [歷程記錄同步]，請套用 [SavingBrowserHistoryDisabled](./microsoft-edge-policies.md#savingbrowserhistorydisabled) 或 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 原則。

### <a name="can-tenant-admins-bring-their-own-key"></a>租用戶系統管理員是否可以使用自己的金鑰？

是，透過 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)。

### <a name="where-is-microsoft-edge-sync-data-stored"></a>Microsoft Edge 同步資料儲存位置？

Azure AD 帳戶的同步資料根據租用戶 ID 儲存在安全伺服器中。 例如，在美國註冊的租用戶的資料儲存在位於該區域的伺服器中，並利用 Office 應用程式使用的相同儲存解決方案。

### <a name="does-the-data-ever-leave-microsofts-cloud-aside-from-syncing-to-microsoft-edge"></a>除了同步到 Microsoft Edge 以外，資料是否曾經離開 Microsoft 的雲端？

不。

### <a name="what-terms-of-service-does-enterprise-sync-fall-under"></a>企業同步適用的服務條款為何？

Microsoft Edge 同步處理的服務條款需遵守 Microsoft Edge 中的 Microsoft 軟體授權，可於  *edge://terms*中進行查看。 您的 Azure AD 訂閱與服務條款最終都需遵守 Microsoft 的 [線上服務條款](https://www.microsoft.com/licensing/product-licensing/products)。

### <a name="does-microsoft-edge-support-government-community-cloud-gcc-high-compliance"></a>Microsoft Edge 是否支援政府社群雲端 (GCC) 高合規性？

尚不支援。 針對 GCC High 雲端的客戶，已停用 Microsoft Edge 同步處理功能。

## <a name="applying-sync"></a>套用同步處理

### <a name="why-isnt-microsoft-edge-sync-supported-in-all-m365-subscriptions"></a>為什麼並非所有 M365 訂閱都支援 Microsoft Edge 同步？

企業同步的方式取決於 [Azure 資訊保護](https://azure.microsoft.com/services/information-protection/)，其並非可在所有 M365 訂閱中取得。

### <a name="is-microsoft-edge-sync-based-on-enterprise-state-roaming"></a>Microsoft Edge 同步是否基於企業狀態漫遊？

不。 ESR 可用來啟用同步，但 Microsoft Edge 同步不屬於 ESR。 如需詳細資訊，請參閱 [Microsoft Edge Sync](/DeployEdge/microsoft-edge-enterprise-sync) [Microsoft Edge 和企業狀態漫遊](/DeployEdge/microsoft-edge-enterprise-state-roaming)。

### <a name="will-microsoft-edge-ever-support-syncing-between-microsoft-edge-and-ie"></a>Microsoft Edge 是否會支援在 Microsoft Edge 與 IE 之間同步？

目前並未計劃支援此類同步。 如果在您的環境中仍然需要 IE 來支援舊版應用程式，請考慮使用我們的[全新 IE 模式](./edge-ie-mode.md)。

### <a name="will-microsoft-edge-sync-with-microsoft-edge-legacy"></a>Microsoft Edge 會與舊版 Microsoft Edge 進行同步處理嗎？

不，不會。 我們認為連結這兩個生態系統會導致 Microsoft Edge 同步可靠性受影響。 我們將確保現有資料移轉至 Microsoft Edge。 使用者還可以從自己選擇的瀏覽器中匯入資料，這也意味著 Microsoft Edge 將無法與 IE 同步。

## <a name="managing-sync"></a>管理同步

### <a name="is-it-possible-to-stop-my-users-from-syncing-with-a-personal-tenant"></a>可以阻止我的使用者與個人租用戶進行同步嗎？

沒有直接的做法，但您可以使用 [RestrictSigninToPattern](./microsoft-edge-policies.md#restrictsignintopattern) 原則來決定可以登入 Microsoft Edge 的設定檔。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業同步](microsoft-edge-enterprise-sync.md)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)