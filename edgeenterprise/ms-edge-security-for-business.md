---
title: 企業的 Microsoft Edge 安全性
ms.author: collw
author: seanongit
manager: chuckf
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 企業的 Microsoft Edge 安全性
ms.openlocfilehash: d16b22b63212e3f5319b0bb7df1e457e45cd6208
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979448"
---
# <a name="microsoft-edge-security-for-your-business"></a>企業的 Microsoft Edge 安全性

Microsoft Edge 建置於 Chromium 開放原始碼專案，也就是與 Google Chrome 相同的專案，這表示它的基礎採用了同一套設計精良且經過考驗的安全性架構與設計。 Microsoft Edge 安全性的故事不會在此畫下句點。 其實，**在 Windows 10上，Microsoft Edge 比 Google Chrome 還安全**。 它內建的網路釣魚和惡意程式碼防護措施強大，而且在 Windows 10 以原生方式支援硬體隔離，因此不需要額外軟體就能達到這個安全基準。 此外，搭配 Microsoft 365 安全性與符合性服務的原生支援使用時，Microsoft Edge 可提供其他強大的安全性功能，協助防範資料遺失，優點甚至更多。 如需詳細資訊，請觀看[影片：Microsoft Edge 安全性、相容性及管理性](microsoft-edge-video-security-compatibility-manageability.md)。

讓我們了解細節，從**外部威脅**開始，接著查看**內部風險與資訊保護**。

## <a name="external-threat-protection"></a>外部威脅防護

### <a name="highest-rated-protection-against-phishing-and-malware"></a>針對網路釣魚和惡意程式碼的最高等級防護

在 Microsoft Edge 內建時，SmartScreen 會根據 NSS 實驗的獨立研究來封鎖比 Google Chrome 安全流覽更多的 [網路釣魚](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1) 和 [惡意](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW) 代碼嘗試。 使用者在線上工作時，SmartScreen 提供網站和下載的信譽檢查，而且屬於 [Microsoft Intelligent Security Graph](https://www.microsoft.com/microsoft-365/windows/intelligent-security) 的一環，可獲得 Microsoft 龐大全球資產、研究人員和合作夥伴網路產生的跡象和深入解析。 Microsoft Edge 以危險網站與下載清單的動態雲端式清單為基準執行檢查，甚至可協助您偵測及封鎖稍縱即逝的威脅。  

[使用 SmartScreen 的 Microsoft Edge](//DeployEdge/microsoft-edge-security-smartscreen) 在 [NSS Labs 的網路釣魚防護](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWASN1)測試期間封鎖了 95.5% 的網路釣魚嘗試，以及在 [NSS Labs 的惡意軟體防護](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RWANMW)測試期間封鎖了 98.5% 的惡意軟體嘗試，而相較於 Chrome 的安全瀏覽比率，其分別為 86.9% 和 86.0%。

### <a name="the-only-browser-on-windows-10-that-natively-supports-hardware-isolation"></a>Windows 10 上唯一原生支援硬體隔離的瀏覽器

Microsoft Edge 是 Windows 10 上唯一原生支援硬體隔離功能的瀏覽器。 Windows Defender 應用程式防護 (應用程式防護) 是 Windows 10 專業版或企業版的一環，會在與本機裝置和內部網路獨立的核心執行不受信任的網站。 不受信任的網站會在「容器」中執行，因此出現攻擊時，它會從其餘的公司網路進行沙箱處理。 如需詳細資訊，請參閱 [Microsoft Edge 的應用程式防護支援](./microsoft-edge-security-windows-defender-application-guard.md)。

如果您使用的是 Chrome，可利用 MDAG 擴充功能這個 Windows 10 硬體隔離。 這個擴充功能會啟動 Microsoft Edge，以利用應用程式防護的核心層級隔離。 此外，僅限 Chrome 的解決方案若要達成相似的核心層級隔離，需要有協力廠商隔離軟體。

> [!NOTE]
> Windows 10 1809 及更新版本提供應用程式防護。 Windows 10 家用版不提供應用程式防護。

## <a name="internal-risks-and-information-protection"></a>內部風險與資訊保護

### <a name="native-support-for-microsoft-365-security-without-additional-software"></a>Microsoft 365 安全性的原生支援 (無額外軟體)

除了阻擋外部威脅，IT 系統管理員也必須防範內部風險。 IT 系統管理員的優先要務，是以強有力的方式大幅保護機密的公司資料，人力分散各地時，這點格外重要。 Microsoft Edge 是唯一原生支援 Azure AD 條件式存取、Windows 資訊保護和全新 Microsoft 端點資料外洩防護 (DLP) 的瀏覽器，而且不需要額外軟體。

**Microsoft Edge 是唯一原生支援條件式存取的瀏覽器**。 [Microsoft Edge 的條件式存取支援](ms-edge-security-conditional-access.md)，讓組織的存取控制決策輕輕鬆鬆即可利用身分識別訊號。 [條件式存取](/azure/active-directory/conditional-access/overview) 是 Azure Active Directory 使用的工具，可匯集訊號，讓您做出決策及強制執行組織原則。 條件式存取是全新身分識別導向控制台的核心。 若要在 Chrome 取得條件式存取支援，需要有額外的外掛程式。

> [!NOTE]
> Azure AD 條件式存取所需的 Microsoft 365 E3 或更新版本訂閱。

**Microsoft Edge 是唯一原生支援 Windows 資訊保護 (WIP) 的瀏覽器**，可為公司資料提供保護，以協助防止使用者在 Windows 10 裝置意外洩漏。 [Microsoft Edge 的 WIP 支援](./microsoft-edge-security-windows-information-protection.md)可設定為，僅允許 IT 授權的應用程式存取公司資料。 它還提供外洩控制措施，例如剪貼簿保護、下載時加密檔案，以及防止檔案上傳到未授權的網路共用或雲端位置，提供流暢的使用者體驗。 WIP 可用於周界型設定，而且 IT 系統管理員可從這裡定義公司邊界，該邊界內的所有資料都視同公司。 Chrome 未啟用含外洩控制措施的 WIP。

> [!NOTE]
> Windows 資訊保護 (WIP) 設定需要授權 Microsoft Intune 或 Microsoft Endpoint Configuration Manager，或是使用協力廠商行動裝置管理 (MDM) 解決方案，而且這類方案可能需要額外授權。

**只有 Microsoft Edge 原生支援 Microsoft 端點資料外洩防護 (端點 DLP)**。 端點 DLP 會與 Microsoft 安全中心整合，並將資訊保護延伸至 Microsoft Edge，以協助提醒使用者無法相容的活動，並防止使用者在線上工作時遺失資料。 它可搜尋企業內符合系統管理員定義準則的機密資料，並標記這類資料，例如有信用卡號碼或政府 ID (例如社會保險號碼) 的檔案、財務資訊等。您可以將 Microsoft 資訊保護原則部署到 Microsoft 端點 DLP，而不需要另外重新配置，包括 IT 系統管理員已自訂的機密內容識別碼和原則。 這可讓 IT 系統管理員順利部署資訊保護。

若要深入了解端點 DLP 先決條件及如何進行設定，請移至 [開始使用端點資料外洩防護](/microsoft-365/compliance/endpoint-dlp-getting-started?preserve-view=true&view=o365-worldwide)。

> [!NOTE]
> Microsoft 端點資料外洩防護需要 Microsoft 365 E5 或 Microsoft 365 E5 合規性訂閱。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：Microsoft Edge 安全性、相容性及管理性](microsoft-edge-video-security-compatibility-manageability.md)