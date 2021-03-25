---
title: '[Microsoft Edge] 和 [Windows Defender 應用程式防護]'
ms.author: srugh
author: dan-wesley
manager: seanlyn
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 對 Microsoft Defender 應用程式防護的支援
ms.openlocfilehash: 2dc1c5b35003c7de4fa474764c46a792bf1e3439
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447167"
---
# <a name="microsoft-edge-support-for-microsoft-defender-application-guard"></a>Microsoft Edge 對 Microsoft Defender 應用程式防護的支援

本文說明 Microsoft Edge 如何支援 Microsoft Defender 應用程式防護 (應用程式防護)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="overview"></a>概觀

企業中的安全性架構師必須處理生產力與安全性之間的張力。 您可相當容易地鎖定瀏覽器，且只允許載入少數受信任的網站。 這種方法可改善整體安全性狀態，但其生產力可能會降低。 如果您降低限制以提高生產力，則會提高風險度。 這是難以達到的平衡！

在此不斷變化的威脅形勢中，我們更加難以掌握新興的威脅。 瀏覽器依舊是用戶端裝置上的主要受攻擊面，因為瀏覽器的基本任務是要讓使用者存取、下載和開啟不受信任來源中不受信任的內容。 惡意行動者不斷鑽研針對瀏覽器的新型社交工程攻擊。 安全性事件預防或偵測/回應策略無法保證 100% 安全。

所要考量的重要安全戰略就是[採用破壞方法](/office365/Enterprise/office-365-monitoring-and-testing#assume-breach-methodology)，這表示不論如何防範，都接受攻擊最少會成功一次。 此種思維需要建立防禦措施來遏制損害，以確保在此情況下公司網路和其他資源仍然受到保護。  為 Microsoft Edge 部署應用程式防護正好符合此策略。

## <a name="about-application-guard"></a>關於應用程式防護

應用程式防護專為 Windows 10 和 Microsoft Edge 設計，採用硬體隔離方法。 這種方法可讓不受信任的網站導覽在容器內啟動。 硬體隔離可協助企業保護企業網路和資料，以防使用者造訪遭入侵或惡意的網站。

企業系統管理員可定義受信任的網站、雲端資源和內部網路。 不在受信任的網站清單中的所有項目都會被視為不受信任。 這些網站會與使用者裝置上的公司網路和資料隔離。

如需詳細資訊：

- 觀看我們的影片：[使用應用程式防護的 Microsoft Edge 瀏覽器隔離](microsoft-edge-video-security-application-guard.md)
- 請閱讀[什麼是應用程式防護及其如何運作？](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview#what-is-application-guard-and-how-does-it-work)

下一個螢幕擷取畫面顯示應用程式防護的訊息範例，其中顯示使用者正在安全的空間中瀏覽。

![應用程式防護的安全瀏覽訊息](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-1.png)

## <a name="whats-new"></a>新功能

新的 Microsoft Edge 瀏覽器中的應用程式防護支援具備與舊版 Microsoft Edge 同等的功能，且包含多項改善。

### <a name="extension-support-inside-the-container"></a>容器內的延伸支援

容器內的延伸支援曾經是來自客戶的最熱門要求之一。 案例包含從想要在容器內執行廣告封鎖程式來提升瀏覽器效能，以至能夠在容器內執行自產的自訂延伸。

現在支援在容器中安裝延伸 (從 Microsoft Edge 版本 81 開始)。 可透過原則控制這項支援。 在 [ExtensionInstallForcelist](./microsoft-edge-policies.md#extensioninstallforcelist) 原則中使用的 `updateURL`，應新增為應用程式防護所用網路隔離原則中的中性資源。

有些容器支援範例包含下列案例：

- 在主機上強制安裝延伸
- 從主機移除延伸
- 主機上封鎖的延伸

> [!NOTE]
> 您也可從延伸存放區，在容器內手動安裝個別的延伸。 啟用 [允許保留][](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard#application-specific-settings) 原則後，只有手動安裝的延伸才會保留在容器中。

### <a name="identifying-application-guard-traffic-via-dual-proxy"></a>透過雙 Proxy 識別應用程式防護流量

部分企業客戶正在部署適用于特定案例的應用程式防護，以便識別來自 Microsoft Defender 應用程式防護容器的 proxy 等級網路流量。 從穩定通道版本 84 開始，Microsoft Edge 將支援雙 proxy 來滿足這一需求。 您可以使用 [ApplicationGuardContainerProxy](./microsoft-edge-policies.md#applicationguardcontainerproxy) 原則來設定此功能。

下圖顯示 Microsoft Edge 的雙 proxy 架構。

![應用程式防護的雙 proxy 架構](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-dual-proxy.png)

### <a name="diagnostic-page-for-troubleshooting"></a>用於疑難排解的診斷頁面

另一個使用者痛點就是在問題回報後，針對裝置上的應用程式防護設定進行疑難排解。 Microsoft Edge 有診斷頁面 (`edge://application-guard-internals`) 可針對使用者問題進行疑難排解。 其中一項診斷可根據使用者裝置上的設定來檢查 URL 信任。

下一個螢幕擷取畫面顯示多個索引標籤診斷頁面，以協助診斷使用者回報告的裝置問題。

![應用程式防護診斷頁面](media/microsoft-edge-security-windows-defender-application-guard/wd-application-guard-2.png)

### <a name="microsoft-edge-updates-in-the-container"></a>容器中的 Microsoft Edge 更新

容器中的舊版 Microsoft Edge 更新是 Windows OS 更新週期的一部分。 由於新版 Microsoft Edge 更新本身與 Windows OS 無關，因此不再相依於容器更新。 主機 Microsoft Edge 的通道和版本會在容器內複寫。

## <a name="prerequisites"></a>必要條件

下列需求適用於使用應用程式防護搭配 Microsoft Edge 的裝置：

- Windows 10 1809 (RS5) 及以上版本。
- 僅限 Windows 用戶端 SKU

  > [!NOTE]
  > 只有 Windows 10 專業版和 Windows 10 企業版 SKU 支援應用程式防護。

- [軟體需求](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard#software-requirements)所述的其中一個管理解決方案

## <a name="how-to-install-application-guard"></a>如何安裝應用程式防護

下列文章提供透過 Microsoft Edge 安裝、設定及測試應用程式防護所需的資訊。

- [系統需求](/windows/security/threat-protection/microsoft-defender-application-guard/reqs-md-app-guard)
- [安裝 Microsoft Defender 應用程式防護](/windows/security/threat-protection/microsoft-defender-application-guard/install-md-app-guard)
- [設定 Microsoft Defender 群組原則設定](/windows/security/threat-protection/microsoft-defender-application-guard/configure-md-app-guard)
- [測試應用程式防護](/windows/security/threat-protection/microsoft-defender-application-guard/test-scenarios-md-app-guard)

## <a name="frequently-asked-questions"></a>常見問題集

### <a name="does-application-guard-work-in-ie-mode"></a>應用程式防護是否可在 IE 模式中運作？

IE 模式支援應用程式防護功能，但我們不期望在 IE 模式中經常使用此功能。 建議針對一些受信任的內部網站部署 IE 模式，而應用程式防護只適用於不受信任的網站。 確定所有 IE 模式網站或 IP 位址也會新增至網路隔離原則，使應用程式防護將其視為受信任的資源。

### <a name="do-i-need-to-install-the-application-guard-chrome-extension"></a>我需要安裝應用程式防護 Chrome 延伸嗎？

否，Microsoft Edge 本身就支援應用程式防護功能。 事實上，應用程式防護 Chrome 延伸不是 Microsoft Edge 中支援的設定。

### <a name="are-there-any-other-platform-related-faqs"></a>是否有任何其他平台相關的常見問題集？

是。 [常見問答集─Microsoft Defender 應用程式防護](/windows/security/threat-protection/microsoft-defender-application-guard/faq-md-app-guard) 

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Defender 進階威脅防護](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [影片：使用應用程式防護的 Microsoft Edge 瀏覽器隔離](https://www.youtube.com/watch?v=zQjaRqNXMqw&t=3s)