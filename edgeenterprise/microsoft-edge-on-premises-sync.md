---
title: Active Directory (AD) 使用者的內部部署同步
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Active Directory (AD) 使用者的內部部署同步
ms.openlocfilehash: 39d13a5d9d712ce2c086112c8de453562e037293
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617713"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a>Active Directory (AD) 使用者的內部部署同步

本文說明 Active Directory (AD) 使用者如何在不連線到 Microsoft 雲端服務的情況下，在電腦之間漫遊 Microsoft Edge 我的最愛和設定。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 85 或更新版本。

## <a name="introduction"></a>簡介

在 Microsoft Edge 中同步使用者資料，通常需要 Microsoft 帳戶或 Azure Active Directory (Azure AD) 帳戶，以及 Microsoft 雲端服務的連線。 有了內部部署同步，Microsoft Edge 會將 Active Directory 使用者的我的最愛和設定儲存至可在不同電腦之間移動的檔案。 內部部署同步不會干擾允許該功能的這些設定檔的雲端同步。

## <a name="how-it-works"></a>運作方式

Microsoft Edge 允許將設定檔與 Active Directory (AD) 帳戶 (其無法用於雲端同步) 建立關聯。啟用內部部署同步時，會將來自 AD 設定檔的資料儲存到名為 profile.pb 的檔案。 依預設，此檔案會儲存在 *%APPDATA%/Microsoft/Edge* 中。 此檔案寫入之後，可在不同的電腦之間移動該檔案，並且將在每一部電腦上讀取和寫入使用者資料。 Microsoft Edge 只會從此檔案讀取和寫入內容；系統管理員有責任確保可視需要移動檔案。

## <a name="use-on-premises-sync"></a>使用內部部署同步

若要使用內部部署同步，您必須啟用該功能，將設定檔與 AD 帳戶建立關聯，以及選擇性地變更使用者資料的位置。

### <a name="enable-on-premises-sync"></a>啟用內部部署同步

若要在 Microsoft Edge 中啟用內部部署同步，請設定 [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) 原則。

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a>確保設定檔與 Active Directory 帳戶相關聯

內部部署同步僅適用與 Active Directory (AD) 帳戶相關聯的設定檔。 如果沒有這類設定檔，內部部署同步將無法運作。 若要確保使用者使用 AD 帳戶登入，請設定 [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) 原則。 針對內部部署的同步，Microsoft Edge 只會仰賴於 AD 來建立使用者資料的身分識別，而 Microsoft Edge 讀取和寫入內部部署資料的方式與系統管理員為 AD 使用者設定漫遊的方式之間並沒有直接的關係。

### <a name="change-the-location-of-the-user-data-optional"></a>變更使用者資料的位置 (選用)

依預設，使用者資料會儲存在 *%APPDATA%/Microsoft/Edge* 中名為 **profile.pb** 的檔案中。 若要變更此檔案的位置，請設定 [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) 原則。

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a>啟用內部部署同步時使用者體驗的變更

啟用內部部署同步時，系統不會要求使用者啟用同步。此外，使用者無法在 [同步設定] 中關閉同步，且無法開啟內部部署同步所不支援的同步類型。

## <a name="on-premises-sync-usage-notes"></a>內部部署同步使用方式說明

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a>在相同電腦上執行雲端同步和內部部署同步

內部部署同步不會干擾雲端同步。如果 Microsoft Edge 有會同步到雲端的多個 Microsoft 帳戶或 Azure Active Directory 設定檔，這些設定檔將會在啟用內部部署同步時繼續同步。

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a>不建議一次在多部電腦上執行 Microsoft Edge

由於內部部署同步的運作方式是透過在電腦之間移動使用者資料檔，因此內部部署同步並不會同步同時間工作階段之間的變更。 因此，內部部署同步於一次在一部電腦上使用時最適合。 如果同時間有執行內部部署工作階段，任何電腦上的資料可能會在您下一次啟動瀏覽器工作階段時，意外地遭到來自另一部電腦的資料覆寫。

> [!NOTE]
> 啟用內部部署同步時，Microsoft Edge 會鎖定 **profile.pb** 檔案。 如果使用資料夾重新導向在不同的電腦之間共用單一 **profile.pb** 檔案，則只能啟動使用該檔案的 Microsoft Edge 的一個執行個體。

### <a name="using-other-sync-policies-with-on-premises-sync"></a>對內部部署同步使用其他同步原則

如果需要，您可以使用 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 原則來選擇性地停用我的最愛或設定同步。 [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) 原則對內部部署同步沒有影響。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 和企業狀態漫遊](microsoft-edge-enterprise-state-roaming.md)
- [Microsoft Edge 企業版同步處理](microsoft-edge-enterprise-sync.md)