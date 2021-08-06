---
title: 為使用者自動啟用密碼監視器
ms.author: supalsul
author:
manager: tulasim
ms.date: 07/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 為使用者自動啟用密碼監視器
ms.openlocfilehash: 19008283cb687cb903da63d74277cc0b326b91ad14e48d1e14861d765d61479a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727082"
---
# <a name="password-monitor-auto-enabled-for-users"></a>為使用者自動啟用密碼監視器

本文說明如何為選取的使用者開啟 Microsoft Edge 中的密碼監視器，並提供系統管理員用來控制監視啟用方式的步驟。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 88 或更新版本。

## <a name="introduction-benefits-and-availability"></a>簡介、優點和可用性

密碼監視器可協助 Microsoft Edge 使用者保護其線上帳戶，方法是通知使用者是否在線上洩漏中發現其任何密碼。 當不良行為者竊取協力廠商應用程式或網站的資料時，即發生線上洩漏或資料違規。 若要深入瞭解，請參閱 Microsoft 部落格上的[密碼監視器：在 Microsoft Edge 中保護密碼](https://www.microsoft.com/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/)文章。

### <a name="benefits"></a>優點

有鑑於這些線上攻擊的頻率與範圍，我們每個人都必須具備這種保護。 Microsoft Edge 具備內建功能，可安全地檢查使用者儲存的密碼對照已知受危害的密碼，並在發現相符時提醒使用者。  

## <a name="configure-group-policy-for-password-monitor"></a>設定密碼監視器的群組原則

此功能是透過 [PasswordMonitorAllowed](./microsoft-edge-policies.md#passwordmonitorallowed) 群組原則控制。

啟用原則之後，使用者仍然必須同意，才能開啟該功能。 由於功能包含使用者的敏感性和個人資料 (密碼)，因此需要取得同意。 如果使用群組原則停用該功能，使用者就無法覆寫此設定。  

## <a name="enabling-password-monitor-for-users"></a>為使用者啟用密碼監視器

啟用密碼監視器原則之後，使用者會透過不同方式來取得此功能。

- 自動啟用。 使用其公司帳戶 (Active Directory 或 Azure Active Directory) 登入並同步其密碼的使用者，將會自動啟用此功能。 在下一個螢幕擷取畫面中，使用者會看到通知，通知其該功能已開啟。

  :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-enabled-notice.png" alt-text="密碼監視器已啟用通知":::

-  取得明確同意。 未開啟密碼同步的使用者，系統會要求他們提供開啟密碼監視器的權限。 他們將在下列動作執行時收到提示：
   - 當使用者儲存新密碼時。
 
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-save-pw-prompt.png" alt-text="提示儲存密碼":::

   - 使用者使用已儲存的密碼登入瀏覽器時。
  
     :::image type="content" source="media/microsoft-edge-security-password-monitor/monitor-after-signin.png" alt-text="登入後確認提示":::
   
- 直接啟用。 使用者可以隨時移至 [設定]****  >  [密碼]****，並開啟或關閉該功能。

## <a name="user-scenarios-with-password-monitor-auto-enabled"></a>自動啟用密碼監視器的使用者案例

下表顯示自動啟用密碼監視器的案例，以及該功能如何在使用者裝置上運作。

| 案例 | 基本條件 | 影響 |
|--|--|--|
| 1 同步開啟 | 同步開啟<br>先前已啟用功能：否<br>回應同意 UI：無 | 功能會預設啟用，且瀏覽器啟動 2 分鐘後會顯示通知泡泡。<br>- 如果在此之後關閉同步，則會停用該功能。<br>- 如果在變更同步之前關閉該功能，同步將不再影響該功能。   |
| 2 同步開啟 | 同步開啟<br>先前已啟用功能：是<br>回應同意 UI：無 | 功能會與使用者選擇保持相同。  不顯示通知泡泡，對功能值的同步變更不會造成影響。|
| 3 同步關閉 | 同步關閉<br>先前已啟用功能：否<br>回應同意 UI：無 | 同步將會關閉，且功能將保持停用<br>- 在此之後的任何時間點，如果使用者開啟同步而未變更功能：功能會啟用，且在開啟同步的 2 分鐘後會顯示自動啟用通知。 <br> - 如果再次關閉同步，則會停用該功能 <br>- 如果在開啟同步之前變更了功能，同步將不會再影響密碼監視器。  |  
| 4 同步關閉 | 同步關閉<br>先前已啟用功能：是<br>回應同意 UI：無 | 功能會與使用者選擇保持相同，不會顯示通知泡泡，且對功能值的同步變更不會造成影響。  |

此外，如果使用者登入時使用的工作帳戶是由下列任何一原則所限制，就「不會」為使用者自動啟用該功能：

- 密碼監視器已停用  
- 密碼同步已停用
- 與 Microsoft 伺服器共用資料功能已停用

## <a name="frequently-asked-questions"></a>常見問題集

### <a name="how-can-password-monitor-be-disabled-for-my-organization"></a>如何為我的組織停用密碼監視器？

您可以透過以下方式，為您的組織停用密碼監視器：
- 使用 PasswordMonitorAllowed 群組原則。
- 停止同步和傳送資料到 Microsoft 伺服器。

  > [!NOTE]
  > 密碼監視器甚至能在密碼同步停用時運作，只要使用者已明確同意開啟該功能，或已自行透過 [設定] 開啟該功能即可。

### <a name="what-happens-if-a-user-for-whom-the-feature-has-been-auto-enabled-turns-password-monitor-off-via-settings"></a>如果某個使用者的該功能已自動啟用，但透過 [設定] 關閉密碼監視器，會發生什麼情況？

將採用使用者設定中的資訊，因此該使用者的功能會保持停用。 不過，系統可能會向他們再次顯示同意對話方塊，以防他們先前未曾回應同意提示。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)