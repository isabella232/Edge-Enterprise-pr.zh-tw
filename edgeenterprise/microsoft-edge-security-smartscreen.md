---
title: Microsoft Defender SmartScreen 的 Microsoft Edge 支援
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Defender SmartScreen 的 Microsoft Edge 支援
ms.openlocfilehash: 2de93b4ebe26b4a90592f7ee9143f6f775b682ce
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314686"
---
# Microsoft Defender SmartScreen 的 Microsoft Edge 支援

本文說明使用 Microsoft Defender SmartScreen 的優點，說明其運作方式，並說明如何設定此 Microsoft Edge 功能。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

Microsoft Defender SmartScreen 是一項服務，Microsoft Edge 用來在您瀏覽網頁時保護您的安全。 Microsoft Defender SmartScreen 可針對可能從事網路釣魚攻擊或嘗試透過聚焦攻擊散佈惡意程式碼的網站，協助提供一套早期警告系統。 如需詳細資訊，請觀看[影片：在 Microsoft Edge 上安全瀏覽](microsoft-edge-video-security-smartscreen.md)。

> [!NOTE]
> 在 Windows 10 版本 1703 之前，搭配瀏覽器和 Microsoft SmartScreen 篩選工具於瀏覽器之外使用時，此功能稱為「SmartScreen 篩選工具」。

## Microsoft Defender SmartScreen 的優點

Microsoft Defender SmartScreen 提供數個優點，如下列清單所述。 在 [Microsoft Defender SmartScreen 文件](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview#benefits-of-windows-defender-smartscreen)中詳細說明這些優點。 優點如下：

- 防網路釣魚和反惡意程式碼的支援
- 以信譽為基礎的 URL 和應用程式保護
- 作業系統整合
- 已改善啟發學習與診斷資料
- 透過群組原則和 Microsoft Intune 進行管理
- 封鎖與可能不需要的應用程式相關聯的 URL

## 了解 Microsoft Defender SmartScreen 如何運作

許多輸入都會造成 Microsoft Defender SmartScreen 警告。 資料會從許多來源接收，包括使用者意見反應、資料提供者和情報模型。 此資料可用於協助識別潛在惡意的內容。 Microsoft Defender SmartScreen 也會檢查下載的應用程式或應用程式安裝程式，查看是否為惡意。 在這兩個情況下，Microsoft Defender SmartScreen 會相應地警示使用者可疑的內容。

### 網站分析

Microsoft Defender SmartScreen 會透過下列方式來判斷網站是否為潛在惡意網站：

- 分析已造訪的網頁，找出可疑行為的指示。
- 對照所報告網路釣魚網站的動態清單，檢查造訪的網站。

如果 Microsoft Defender SmartScreen 認為頁面為惡意，則會顯示警告頁面，通知使用者該網站回報為不安全。 以下螢幕擷取畫面顯示當使用者嘗試開啟惡意網站時，出現的 Microsoft Defender SmartScreen 警告頁面範例。

![連結至外部網站的 Microsoft Defender SmartScreen 封鎖頁面](media/microsoft-edge-security-smartscreen/microsoft-edge-smartscreen-warning.png)

使用者可在警告訊息中選擇將網站回報為安全或不安全。 如需詳細資訊，請參閱[如何報告網站](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device#how-users-can-report-websites-as-safe-or-unsafe)。

### 檔案分析

Microsoft Defender SmartScreen 會根據許多標準 (例如下載流量、下載歷史記錄、過去的防毒結果和 URL 信譽) 判斷下載的應用程式或應用程式安裝程式是否有潛在惡意。

- 含有已知安全信譽的檔案，將會下載檔案而不出現通知。  
- 將針對含有已知惡意信譽的檔案顯示警告，讓使用者知道該檔案不安全，且已報告為惡意。 以下螢幕擷取畫面是惡意檔案的警告範例。

  ![含有惡意信譽檔案的 Microsoft Defender SmartScreen 封鎖通知](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-known-malicious.png)

- 未知的檔案則會顯示警告，讓使用者知道該下載項目沒有已知的足跡，並建議使用者注意。 以下螢幕擷取畫面是未知檔案的警告範例。

  ![含有未知信譽檔案的 Microsoft Defender SmartScreen 封鎖通知](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious.png)

並非所有未知程式都是惡意的，且未知警告是為需要的使用者提供內容和指導，特別是如果警告是非預期的。

  ![保留具有惡意信譽的檔案](media/microsoft-edge-security-smartscreen/ms-edge-smartscreen-unknown-malicious-keep.png)

不過，使用者仍然可以下載並執行應用程式，方法是按一下 [...] | [保留] | [顯示更多] | [繼續]****。

> [!TIP]
> **僅參考，這適用企業客戶。** 根據預設，Microsoft Defender SmartScreen 會讓使用者略過警告。 因為此使用者的互動可能會造成風險，建議您檢閱這些[建議的群組原則設定](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-available-settings#recommended-group-policy-and-mdm-settings-for-your-organization)。

您看到 Microsoft Defender SmartScreen 如何使用[示範網站](https://demo.smartscreen.msft.net/)回應不同的案例。

## Microsoft Defender SmartScreen 和使用者隱私權

Microsoft Defender SmartScreen 可在使用者使用信譽檢查系統來瀏覽網際網路時保護使用者。 Microsoft Edge 會將 URL 或檔案的相關資訊傳送到 Microsoft Defender SmartScreen 服務，以開始信譽檢查。 該檢查會對照已知危險的網站和檔案的動態清單來比較網站或檔案。 所有對 Microsoft Defender SmartScreen 服務要求都是以 TLS 加密的方式進行。 服務會傳回信譽檢查的結果，這可能會導致 Microsoft Edge 顯示網站或檔案的警告。 這些結果會儲存在裝置的本機上。

Microsoft Defender SmartScreen 服務會儲存信譽檢查的相關資料。 隨著新網站的發現，服務會將資料新增至已知惡意 URL 和檔案的動態資料庫。 此資料會儲存在安全的 Microsoft 伺服器上，並僅用於 Microsoft 安全性服務。 此資料永遠不會用來以任何方式識別或鎖定使用者。 清除瀏覽快取會清除所有本機儲存的 Microsoft Defender SmartScreen URL 資料。 清除下載歷史記錄將會移除有關檔案下載的任何本機儲存的 SmartScreen 資料。

如需 Microsoft Defender SmartScreen 和 Microsoft Edge 上隱私權的詳細資訊，請參閱 [Microsoft Edge 隱私權白皮書](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper#smartscreen)。

## 系統管理員的 Microsoft Defender SmartScreen 設定

系統管理員可以使用群組原則、Microsoft Intune 或行動裝置管理 (MDM) 設定來設定 Microsoft Defender SmartScreen。 根據您設定 Microsoft Defender SmartScreen 的方式，您可以向使用者顯示一個警告頁面，並且讓他們繼續移至網站，或是可以封鎖整個網站。

### 使用群組原則設定 Microsoft Defender SmartScreen

如需 SmartScreen 原則的完整清單，請參閱 [Microsoft Defender SmartScreen 設定](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreen-settings)

### 使用 MDM 設定 Microsoft Defender SmartScreen

如需詳細資訊，請參閱：

- [Microsoft Defender SmartScreen 的 Windows Intune 設定](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)
- [MDM 原則設定](https://docs.microsoft.com/mem/intune/protect/endpoint-protection-windows-10#windows-defender-smartscreen-settings)

## 使用者的 Microsoft Defender SmartScreen 設定

預設會針對 Microsoft Edge 開啟 Microsoft Defender SmartScreen。 若要關閉 Microsoft Defender SmartScreen，請移至 *edge://settings/privacy > [服務] > [Microsoft Defender SmartScreen]*。 此設定與裝置上的 Microsoft Edge 安裝相關聯的所有設定檔都是相同的。 此設定不會在裝置間同步。 此設定適用於 InPrivate 瀏覽和來賓模式。 如果裝置是使用組織設定的群組原則管理，則會在 *edge://settings/privacy* 中反映該組態。

> [!NOTE]
> 使用者可以為個別裝置設定 Microsoft Defender SmartScreen，除非群組原則或 MDM 已設定為防止它。 如需詳細資訊，請參閱[在個別裝置上設定和使用 Microsoft Defender SmartScreen](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-set-individual-device)。

## 常見問題集

### 信譽檢查系統如何運作？

當您瀏覽網頁時，Microsoft Defender SmartScreen 會將網站和下載內容分類為前幾大流量、危險或未知。 前幾大流量是 Microsoft Defender SmartScreen 判斷值得信任的熱門網站。 如果您前往標示為危險的網站，Microsoft Defender SmartScreen 會立即阻止您存取該網站。 當您前往未知網站時，Microsoft DefenderSmartScreen 會檢查其信譽，以判斷您是否應該存取該網站。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：在 Microsoft Edge 上安全瀏覽](microsoft-edge-video-security-smartscreen.md)
- [Microsoft Defender SmartScreen 概觀](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview)
- [威脅防護](https://docs.microsoft.com/windows/security/threat-protection/index)
- [防護抵禦可能不需要的應用程式](https://docs.microsoft.com/DeployEdge/microsoft-edge-potentially-unwanted-apps)