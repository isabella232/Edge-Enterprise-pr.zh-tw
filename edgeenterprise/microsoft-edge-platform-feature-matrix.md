---
title: Microsoft Edge 功能的平台支援
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 功能的平台支援摘要
ms.openlocfilehash: 1ac512d4e9e6279ce2d6fcff5aebede0974eb5cdcf9211c957ace9f015b95010
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727466"
---
# <a name="platform-support-for-microsoft-edge-features"></a>Microsoft Edge 功能的平台支援

本文摘要說明 Microsoft Edge 功能的平台支援。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="feature-matrix-for-platforms"></a>平台的功能矩陣

下表摘要說明 Windows 和 macOS 平台的功能支援。

> [!NOTE]
> Android 和 iOS 目前並未在支援資料表中顯示，不過我們會繼續處理這項資訊，並將據此進行更新。

| 安全性功能 |Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|Azure Active Directory (Azure AD) 條件式存取|是|是|是|是|[Azure AD 條件式存取](/deployedge/ms-edge-security-conditional-access#accessing-conditional-access-protected-resources-in-microsoft-edge)|
|Microsoft Defender 應用程式防護|是 (1890+) |否|否|否|[Microsoft Defender 應用程式防護](/deployedge/microsoft-edge-security-windows-defender-application-guard) |
|Microsoft Defender SmartScreen|是|是|是|是|[Microsoft Defender SmartScreen](/deployedge/microsoft-edge-security-smartscreen) |
|Microsoft 端點 DLP|是|否|否|否|[Microsoft 端點 DLP](/deployedge/microsoft-edge-security-dlp#microsoft-endpoint-data-loss-prevention-endpoint-dlp)|
|密碼監視器|是|是|是|是|[密碼監視器](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|密碼產生器|是|是|是|是|[密碼產生器](https://blogs.windows.com/msedgedev/2021/01/21/edge-88-privacy/)|
|Windows 資訊保護 (WIP)|是 (1607+) |否|否|否|[WIP](/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)|

|身分識別功能| Win 10 | Win 8.1 | Win 7 | macOS | URL |
|--|--|--|--|--|--|
|自動登入 (混合式/AAD-J)|是|是|是|否|[混合式/AAD-J](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|自動登入 (已加入網域) |是|是|是|否|[已加入網域](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|自動登入 (作業系統預設為 MSA) |是 (1709+) |否|否|否|[MSA](/deployedge/microsoft-edge-security-identity#automatic-sign-in)|
|至網頁單一登入 (SSO) 的瀏覽器|是|是|是|是|[Browser-Web SSO](https://www.microsoft.com/microsoft-365/roadmap?featureid=66332)|
|引導式切換/「自動設定檔切換」|是|是|是|是|[在公司及家中使用多個設定檔](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|多個設定檔|是|是|是|是|[在公司及家中使用多個設定檔](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) |
|Active Directory (AD) 的內部部署同步 |是|是|是|否|[Active Directory (AD) 使用者的內部部署同步](/deployedge/microsoft-edge-on-premises-sync) |
|無縫 SSO|是 (1709+) |是|是|是|[無縫 SSO](/deployedge/microsoft-edge-security-identity#seamless-sso)|
|SSO 搭配主要重新整理權杖 (PRT)|是 (1709+) |是|是|否|[SSO 搭配 PRT](/deployedge/microsoft-edge-security-identity#sso-with-primary-refresh-token-prt)|
|Windows 整合式驗證 (WIA)|是|是|是|是* (需要原則) |[WIA](/deployedge/microsoft-edge-security-identity#windows-integrated-authentication-wia)|

|其他功能|Win 10|Win 8.1|Win 7|macOS|URL|
|--------|-------|--------|-----|-------|---|
|集合|是|是|是|是|[集合](https://blogs.windows.com/msedgedev/2019/12/09/improvements-collections-sync-microsoft-edge/) |
|企業新索引標籤頁|是|是|是|是|[新索引標籤頁](https://blogs.windows.com/msedgedev/2020/10/29/enterprise-new-tab-page-my-feed/) |
|IE 模式|是|是|是|否|[IE 模式](/deployedge/edge-ie-mode#prerequisites)|
|Kiosk 模式|是|否|否|否|[Kiosk 模式](/deployedge/microsoft-edge-configure-kiosk-mode)|
|Bing 中的 Microsoft 搜尋|是|是|是|是|[Bing 中的智慧型搜尋](https://www.microsoft.com/edge/business/intelligent-search-with-bing) |
|PDF 閱讀程式|是|是|是|是|[PDF 閱讀程式](/deployedge/microsoft-edge-pdf) |
|購物|是|是|是|是|[購物](https://techcommunity.microsoft.com/t5/articles/introducing-shopping-with-microsoft-edge/m-p/1870080) |
|[休眠] 索引標籤|是|是|是|是|[功能概觀](/deployedge/microsoft-edge-relnote-stable-channel)<br>[最新部落格文章](https://blogs.windows.com/msedgedev/2021/03/04/edge-89-performance/)<br>[群組原則](/deployedge/microsoft-edge-policies#sleeping-tabs-settings)|
|同步處理|是|是|是|是| [企業同步](/deployedge/microsoft-edge-enterprise-sync) |
|版本復原|是|是|是|否|[版本復原](/deployedge/edge-learnmore-rollback) |
|垂直索引標籤|是|是|是|是| |

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)