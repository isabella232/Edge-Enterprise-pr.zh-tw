---
title: Microsoft Edge 通道概觀
ms.author: srugh
author: RyanHechtMSFT
manager: seanlynd
ms.date: 09/23/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 通道概觀
ms.openlocfilehash: dd65d932950be90d3d9278fa41ae843335b2074d
ms.sourcegitcommit: 8e5294e82cf62abc916cfd24692f55925330d42b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/23/2021
ms.locfileid: "12037185"
---
# <a name="overview-of-the-microsoft-edge-channels"></a>Microsoft Edge 通道的概觀

下一版 Microsoft Edge 的好處之一是 Microsoft 可以定期提供新功能。 但是，身為將 Microsoft Edge 部署到組織中使用者的系統管理員，您可能希望對於使用者取得這些新功能的頻率具有更多控制權。 Microsoft 為您提供了四個選項 (稱為通道) 來控制以新功能更新 Microsoft Edge 的頻率。 以下是四個選項概觀。

如需每個通道支援的資訊，請參閱：[Microsoft Edge 生命週期](/deployedge/microsoft-edge-support-lifecycle)
  
> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="channel-overview"></a>通道概觀

|通道|主要用途|以新功能更新的頻率|支援？|
|:---:|---|:---:|:---:|
|[Stable](#stable-channel)|廣泛部署|~4 周|是|
|[擴充穩定](#extended-stable-channel)|與較長的發行週期對齊的穩定企業發行選項 |~8 周|是|
|[Beta](#beta-channel)|組織中的代表驗證|~4 周|是|
|[Dev](#dev-channel)|計劃和開發|每週|否|
|[Canary](#canary-channel)|先進內容|每天|否|

您決定要部署給使用者的更新通道取決於幾個因素，例如使用者運用的企業經營應用程式數量，以及您隨時需要測試其更新版本的 Microsoft Edge。 為了協助您做出決策，請檢閱以下可用於 Microsoft Edge 的四個更新通道的相關資訊。

### <a name="stable-channel"></a>Stable 通道

Stable 通道用於組織中的廣泛部署，它是大多數使用者應該使用的通道。 這是最穩定的通道，也是先前 Beta 通道版本中可用之功能集穩定性的結果。 新功能大約每 4 周提供一次。 安全性和品質更新視需要發佈。 直到該通道的下一個發行版本可用之前，來自 Stable 通道的發行都被視為提供服務。

### <a name="beta-channel"></a>Beta 通道

Beta 通道用於向您組織中一組具代表性的使用者樣本進行生產環境部署。 它是受支援版本，並且 Beta 的每個版本都提供服務，直到此通道的下一版可用為止。 這是驗證您環境中的事物是否如預期運作的絕佳機會，如果您遇到問題，請先對其進行補救然後再發佈到 Stable 通道。 新功能大約每 4 周提供一次。 安全性和品質更新視需要發佈。

### <a name="dev-channel"></a>Dev 通道

Dev 通道用於協助您規劃和開發 Microsoft Edge 的最新功能，其品質高於 Canary 通道。 您可以盡早了解接下來會發生什麼事，並為下一個 Beta 版做好準備。

### <a name="canary-channel"></a>Canary 通道

Canary 通道每天發佈，是所有通道中最先進的。 如果您想要存取最新的投資，這些投資會先出現在這裡。 由於這種頻次的性質，加班時會出現問題，因此如果您利用 Canary 版本，您可能會想要並排安裝另一個通道。

### <a name="extended-stable-channel"></a>擴充穩定通道

不同于我們的預覽 (Canary、Dev 和 Beta) ，擴充穩定通道無法作為個別瀏覽器應用程式使用;相反地，這是 Microsoft Edge 穩定型應用程式的企業發行選項，與穩定版) 中尋找的 4 周主要發行週期相對應 (與較長的 8 周主要發行週期 (相對應。 雖然我們建議在 4 周發行週期自動更新穩定版，但擴充穩定版的存在可更有效地為可能需要較長的時程表來測試和驗證新瀏覽器版本的組織提供服務。

Microsoft Edge 穩定版有 8 周的「擴充穩定」發行週期選項，可提供與 94 開始__ 之均勻編號發行一致的累積Microsoft Edge更新;來自奇數版本的任何功能更新，都會封裝並作為後續偶數發行版本的一部分提供。 例如，如果組織選取具有 Microsoft Edge 94 的 8 周「擴充穩定」發行週期，就會收到 Microsoft Edge 96、Microsoft Edge 98 等後續功能更新。 雖然功能更新會根據所選的發行週期以新版本版本封裝並傳遞，但重要安全性修補程式和修正程式會隨需要提供，而與選取的版本選項無關，有助於維護瀏覽器安全性。 客戶隨時都可以加入宣告擴充穩定發行選項，並將于下一個擴充穩定版中生效。

![比較穩定Microsoft Edge和擴充穩定發行週期選項的範例。](./media/microsoft-edge-channels/extended-stable-explainer.png)

#### <a name="opting-in-to-the-extended-stable-release-cadence"></a>加入宣告擴充穩定發行步頻

##### <a name="opting-in-to-extended-stable-on-windows-with-automatic-updates-recommended"></a>加入宣告使用自動更新功能Windows使用擴充穩定 (建議) 

如果您自動更新Microsoft Edge，您可以使用群組原則物件加入宣告擴充穩定發行步頻。 [請遵循本指南](/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template)，以進一步瞭解下載及安裝最新的群組原則Microsoft Edge管理範本。

1. 開啟 [本機群組原則編輯器]，然後移至 _[電腦設定] > [管理範本] > [Microsoft Edge Update] > [應用程式] > [Microsoft Edge] >_。
2. 選取 **目標通道重寫** ， **然後選取**啟用 。
3. 在 **「選項」** 下， **從 「策略** 」 下拉單中挑選 「擴充穩定」。

當擴充穩定通道的下一次更新發行時，版本號碼大於您目前安裝的裝置，Microsoft Edge會自動更新到擴充穩定通道。 上的版本 `edge://settings/help` 字串會指出您正進行不同的頻道。

> [!NOTE]
> 當擴充穩定通道有新更新，且版本號碼大於裝置 (主要或次要) 時，加入宣告擴充穩定版將會生效。 如果您執行最新版本的 Microsoft Edge 穩定版，並加入宣告擴充穩定版，它會隨著下一個修補程式或更新的 Microsoft Edge。
>
> 根據預設，Microsoft Edge不會降級本身。 如果您目前執行的是奇數版本的 Microsoft Edge 穩定版，加入宣告擴充穩定版將表示您會收到 NO 更新，直到下一個偶數Microsoft Edge發行。
>
> 如果您想要確保所有裝置都從特定版本的擴充穩定版開始，您可以將該特定版本的 Edge 穩定版部署為 MSI 且已啟用捲動功能。 例如，如果您想要從擴充穩定 94 開始，但某些裝置已經更新為穩定 95，您可以部署啟用回卷功能的 Edge 94 MSI。 若要進一步瞭解如何在啟用回卷功能時部署 Edge MSIs，請參閱 [我們的捲動指南](/DeployEdge/edge-learnmore-rollback)。

##### <a name="opting-in-to-extended-stable-on-windows-via-intune"></a>透過 Intune 加入宣告 Windows擴充穩定

Microsoft Edge系統管理範本可以從系統管理中心管理，類似于Microsoft 端點管理員群組原則物件。 請遵循[我們有關使用 Intune Microsoft Edge的指南](/mem/intune/configuration/administrative-templates-configure-edge)。 

「目標**通道重寫**」設定可在「應用程式」Microsoft Edge Update >」子__ 資料夾>Microsoft Edge找到。 應該會設定為 「**擴充穩定」** 

當擴充穩定通道的下一次更新發行時，版本號碼大於您目前安裝的裝置，Microsoft Edge會自動更新到擴充穩定通道。 上的版本 `edge://settings/help` 字串會指出您正進行不同的頻道。

##### <a name="opting-in-to-extended-stable-on-windows-via-configuration-manager"></a>透過 Configuration Manager 加入宣告 Windows擴充穩定

請參閱我們的使用 Configuration [Manager](/mem/configmgr/apps/deploy-use/deploy-edge#update-microsoft-edge)更新Microsoft Edge指南，以進一步瞭解如何同步處理及Microsoft Edge Configuration Manager 中的更新。

擴充穩定更新會發佈在 「Microsoft Edge」產品類別的軟體庫中，類似穩定版、Beta 版和 Dev 通道的現有更新。 不過，與 Beta 和 Dev 不同，Beta 和 Dev 適用于自己的瀏覽器應用程式，擴充穩定更新適用于Microsoft Edge應用程式。 因此，若要讓 Windows更新用戶端決定是否要適用穩定或延伸穩定更新，它會檢查 「目標通道重寫」群組原則的狀態。 如果未設定原則或設定為「穩定」，將會套用穩定更新。 如果設定為「擴充穩定」，將會套用擴充穩定更新。 請遵循上述指示，加入宣告使用自動更新的擴充穩定程式，以瞭解如何正確設定群組原則。 

## <a name="flighting-pre-release-channels-in-your-organization"></a>在貴組織中飛出發行前通道

「目標通道重寫」群群組原則也可以用來順暢地在貴組織中Microsoft Edge測試版通道，而使用者不需要使用第二個網頁瀏覽器應用程式。 例如，您可以針對貴組織中具有代表性的範例使用者，將「目標通道重寫」政策設定為「Beta」。 當這些使用者開啟Microsoft Edge，他們將會執行 Beta 通道發行，而不是 (穩定版，甚至不會) 。 這可提早深入瞭解下一版Microsoft Edge企業中的執行方式，並有助於驗證所有專案在環境中是否如預期運作。 如果使用者遇到任何問題，您就會收到早期訊號，並可確保在發行至穩定通道之前，他們獲得補救。 在疑難排解使用者問題時，版本字串會通知您使用者的通道是否與預設的穩定 `edge://settings/help` 通道不同。

> [!NOTE]
> 由於 Microsoft Edge 的 「Beta」和「開發人員」通道的建立，主要版本號碼大於「穩定」版本號碼，因此如果您採用 「Beta」或「開發人員」通道的更新，並想要還原為 「穩定」，Microsoft Edge[](/DeployEdge/edge-learnmore-rollback)的復原功能將會需要。 只要將「目標通道重寫」設定回穩定，表示您會收到 NO 更新，直到最新穩定發行的版本號碼大於您目前在裝置上執行的版本 Microsoft Edge。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [通道下載](https://aka.ms/EdgeEnterprise)
