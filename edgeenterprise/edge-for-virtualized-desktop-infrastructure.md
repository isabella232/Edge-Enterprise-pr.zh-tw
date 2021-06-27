---
title: 適用於虛擬化桌面基礎結構的 Microsoft Edge
ms.author: anlake
author: AndreaLBarr
manager: collw
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 的虛擬化桌面基礎結構。
ms.openlocfilehash: eaad1b72934b336ce86d14dd8da92a6984d21914
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618063"
---
# <a name="microsoft-edge-for-virtualized-desktop-infrastructure"></a>Microsoft Edge 的虛擬化桌面基礎結構

本文說明在虛擬化環境中使用 Microsoft Edge 的需求和限制。

## <a name="what-is-vdi"></a>什麼是 VDI？

虛擬桌面基礎結構 (VDI) 是虛擬化技術，在資料中心的集中式伺服器上託管桌面作業系統和應用程式。 這可讓具有完全安全且符合規範的集中式來源的使用者獲得完全個人化的桌面體驗。

Microsoft Edge 可在這類虛擬化環境中使用，其使用方式與在本機裝置上使用的方式非常類似，同時從安全且受控制的伺服器環境執行。 視您選擇的 VDI 解決方案不同，也可能讓使用者順暢地存取內部網路應用程式和網站。

大部分的 Microsoft Edge 功能都可在 VDI 環境中都受到支援，沒有任何特殊設定。 不過，為了確保獲得最佳體驗，建議您遵循下列指引。

## <a name="platforms-certified-for-edge"></a>通過 Microsoft Edge 認證的平台

- Azure 虛擬桌面
- Citrix 虛擬應用程式和桌面 (之前稱為 XenApp 和 XenDesktop)

雖然 Microsoft Edge 小組尚未驗證其他 VDI 解決方案，但預期會支援 Edge 中最常見的工作流程。 下列提供之指引不一定適用於您選擇的解決方案。

## <a name="edge-on-vdi-performance-considerations"></a>VDI 效能考量的 Microsoft Edge

在設計 VDI 環境時，您應該仔細考慮使用者的工作流程和需求，以獲得最佳的績效和伺服器設定的限制。

Edge 建議將 Microsoft Edge 部署到 VDI 環境時，遵循下列最低需求：

- vCPU – 每個使用者 2-4 個核心
- RAM – 每個使用者 1 GB

請注意，大型複雜 Web 應用程式和擴充功能需要更多記憶體，且在設定您的環境時必須加以考慮。

## <a name="edge-on-non-persisted-vdi-environments"></a>位於非持續 VDI 環境的 Microsoft Edge

許多 VDI 解決方案都允許存取持續的環境，其中使用者獲指派一個可在工作模式之間持續的虛擬環境；而非持續環境，其中使用者獲指派數部可用電腦的其中一部 (每個工作模式可能是不同的電腦)，使用者資料不一定會在工作階段之間同步。

使用非持續環境時，通常會建立「金色影像」，用於包含所需的應用程式和設定的每個裝置。 以下是我們針對這類影像準備 Microsoft Edge 的建議。

### <a name="deploy-edge"></a>部署 Microsoft Edge

如果您目前使用 Windows 10 (版本 1803) 及更新版本，您應該將 Microsoft Edge 安裝在您的系統上。 不過，如果您使用舊版的 Windows 或想要部署 Microsoft Edge 的其他通道，建議執行下列步驟。

1. 從以下下載符合您 VDI VM 作業系統的 Microsoft Edge MSI 套件：

    - [下載商務用 Microsoft Edge - Microsoft](https://www.microsoft.com/edge/business/download)

2. 執行下列命令，將 MSI 安裝到 VDI VM：

    - `msiexec /i <path_to_msi> /qn /norestart /l*v <install_logfile_name>`

### <a name="disable-automatic-updates"></a>停用自動更新

對於非保存的電腦，最佳做法是停用自動更新並改為更新 Microsoft Edge，做法是更新「標準映射」，以確保電腦集區之間沒有版本不符的情況。

請參閱下列停用自動更新的原則：

- [更新原則覆寫預設值](/deployedge/microsoft-edge-update-policies#updatedefault)

- [更新原則覆寫](/deployedge/microsoft-edge-update-policies#update)

### <a name="profile-management"></a>設定檔管理

在非持續的設定中，請務必考慮，VM 可能無法維持工作模式之間的使用者狀態，或者使用者可能會獲指派一個他們之前從未使用的虛擬電腦，因此沒有使用者資料。

Edge 支援數種同步處理使用者資料的方法，無論使用者資料存取 Microsoft Edge的方式如何，都能使用。

### <a name="azure-ad-sync"></a>Azure AD Sync

如果您的 Azure AD 方案支援，企業同步處理是最快速且最簡單的方法，可確保 Microsoft Edge 使用者資料會同步處理至所有的使用者裝置。  

請參閱下列內容以取得要求和設定的詳細資訊。  

- [設定 Microsoft Edge 企業同步 | Microsoft Docs](/deployedge/microsoft-edge-enterprise-sync)

### <a name="on-premise-sync-for-active-directory-users"></a>Active Directory 使用者的內部部署同步

有了內部部署同步，Microsoft Edge 會將 Active Directory 使用者的我的最愛和設定儲存至可在不同電腦之間輕易移動的檔案。  

請參閱下列內容以取得要求和設定的詳細資訊。  

- [Active Directory (AD) 使用者 | Microsoft Docs 的內部部署同步](/deployedge/microsoft-edge-on-premises-sync)

### <a name="user-profile-redirection"></a>使用者設定檔重新導向  

移轉和重新導向整個使用者資料夾的解決方案有好幾種，以確保使用者內容可維持在這類非持續的環境中。 請和您的 VDI 提供者確認以決定建議的解決方案。

一些熱門解決方案包括：

- [FSLogix 概觀 - FSLogix |Microsoft Docs](/fslogix/overview)
- [如何設定 Citrix 設定檔管理](https://support.citrix.com/article/CTX222893)

另外，建議您在使用此方法時，將不必要的資料夾從備份的使用者資料夾排除，以減少使用者登入電腦和移轉設定檔時的初始載入時間。 如果是這樣，建議您將下列資料夾從您的備份排除，以減少檔案大小。

- %LocalAppData%\Microsoft\Edge\User Data\Default\Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\Code Cache
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsTopSites
- %LocalAppData%\Microsoft\Edge\User Data\Default\JumpListIconsRecentClosed

## <a name="known-issues"></a>已知問題

### <a name="microsoft-edge-crashes-in-older-versions-of-xenapp-and-xendesktop"></a>Microsoft Edge 會在舊版的 XenApp 和 XenDesktop 中當機

此問題應該會在較新的版本中減少，不過，如果您在環境中遇到此問題，您可以停用 Microsoft Edge 的 Citrix API Hooks 以解決此問題，請參閱 [如何根據每個應用程式停用 Citrix API Hooks。](https://support.citrix.com/article/CTX107825)

### <a name="degraded-performance-when-rendering-pages-with-exceptionally-large-html-tables"></a>使用超大型 HTML 表格呈現頁面時，效能會降低

下列的 Citrix 原則已知會緩慢呈現具超大型表格的 HTML 網頁 (超過 30,000 個資料列)。

- 自動鍵盤顯示
- 遠端下拉式方塊

請參閱 [行動體驗原則設定 (citrix.com) ](https://docs.citrix.com/citrix-virtual-apps-desktops/policies/reference/ica-policy-settings/mobile-experience-policy-settings.html) 以取得詳細資訊。 停用這些原則應該可以減緩此問題。

### <a name="windows-account-manager-authorization-scenarios-ie--azure-sync-fail-in-edge-when-run-as-a-citrix-seamless-application"></a>在 Microsoft Edge 中．在以 Citrix 隨選即用應用程式執行時，Windows 帳戶管理員授權案例失敗

這是 Microsoft Edge 和其他使用 WAM 的應用程式 (即 Office) 中的已知問題，因為這類案例所需的 Windows 元件在「順暢」模式下執行時並未初始化。 若要解決此問題：

- 透過遠端桌面將 Microsoft Edge 使用至 Citrix 主機，而不是做為流暢的遠端應用程式。
- 請改為使用 Azure 虛擬桌面遠端應用程式，其中有此問題的緩解措施。
