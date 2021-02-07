---
title: 規劃 Microsoft Edge 部署
ms.author: collw
author: appcompatguy
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 規劃 Microsoft Edge 部署
ms.openlocfilehash: 1b56d9874550c2002cec0577a53a3bf5766e2805
ms.sourcegitcommit: 16a92a51560fdba6f6480e4533453348f026c7ef
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "11313873"
---
# 規劃 Microsoft Edge 部署

本文介紹了在企業環境中部署 Microsoft Edge 的建議做法。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 77 或更新版本。

下列各節提供規劃 Microsoft Edge 部署的特定指南。

- [評估瀏覽器環境及需求](#evaluate-your-existing-browser-environment-and-browser-needs)
- [確定 Windows 10 裝置已準備就緒](#make-sure-your-windows-10-devices-are-ready)
- [選定部署方法](#determine-your-deployment-methodology)
- [執行站台探索](#do-site-discovery)
- [選定通道策略](#determine-your-channel-strategy)
- [識別和設定原則](#define-and-configure-policies)
- [測試應用程式相容性](#do-app-compatibility-testing)
- [Microsoft Edge 試驗](#deploy-microsoft-edge-to-a-pilot-group)
- [評估試驗](#validate-your-deployment)
- [在企業中部署 Microsoft Edge](#broad-deployment-of-microsoft-edge)

## 評估您現有的瀏覽器環境和瀏覽器需求

花些時間了解您當前的瀏覽器狀態和專案願景，以確保所有專案關係人都保持一致，並朝著相同的結果努力。

首先定義目前狀態：

- 目前在您的環境中部署了哪些瀏覽器？
- 哪個瀏覽器設定成預設瀏覽器？
- 您是否需要對某些應用程式使用 Internet Explorer？
- 您現在是否使用企業模式網站清單來設定 Internet Explorer？
- 您的環境中支援哪些作業系統平台？ (Windows 10、macOS、Windows 7、Windows Server 等等)
- 您使用哪些管理工具進行瀏覽器管理？
- 誰負責瀏覽器設定和管理？
- 驗證瀏覽器相容性的程序是什麼？

了解目前狀態後，可以確定瀏覽器部署的預期目標，同時考慮到以下事項：

- 是否要[將 Microsoft Edge 設定為預設瀏覽器](https://docs.microsoft.com/DeployEdge/edge-default-browser)？
- 您將如何[設定 Microsoft Edge](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge)？
- 在初始部署中要設定哪些重要功能？
- 解決任何已識別的相容性或設定問題的過程是什麼？

您還應了解您感興趣的功能的**先決條件**，例如：

- [Windows Defender 應用程式防護](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-application-guard/reqs-wd-app-guard)
- [Internet Explorer 模式](https://docs.microsoft.com/DeployEdge/edge-ie-mode)
- [驗證與同步](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-identity)

有了這些答案，您已準備好規劃 Microsoft Edge 部署。
<!--bookmark -->

## 確定您的 Windows 10 裝置已準備就緒

Microsoft Edge 穩定通道需要自 2019 年 10 月 (或更新版本) 起的最新累積更新 (LCU)。 如果您嘗試部署到具有舊版 LCU 的 Windows 10 裝置，安裝便會失敗。 如需部署 Microsoft Edge 前必須套用的最小 LCU 的詳細資料，請參閱[支援下一版 Microsoft Edge 的 Windows 更新](https://docs.microsoft.com/DeployEdge/microsoft-edge-sysupdate-windows-updates)。

## 決定您的部署方法

在您了解所需的結束狀態後，您就可以開始規劃如何實現目標。 部署 Microsoft Edge 的兩種主要方式是依角色和依網站部署。

### 依角色部署到終端使用者

如果應用程式相容性是您主要關心的問題，並且您沒有確定要測試哪些應用程式，則可能需要考慮依角色部署到終端使用者。 如此一來，對需要修改其設定以解決相容性問題的應用程式，每一波的分階段部署都能夠提供意見反應和見解。

### 依網站部署到終端使用者

如果頻寬是您主要關心的問題，您可能需要考慮提前進行應用程式相容性測試。 完成測試後，依網站部署到終端使用者，以便可以利用快取對其他軟體進行傳遞最佳化。

## 執行站台探索

如果您依賴於舊版 Web 應用程式，並計畫使用 Internet Explorer 模式 (大多數客戶都這樣做)，則可能需要執行一些額外的站台探索。

### 如果您已經部署並設定舊版 Microsoft Edge

如果您已將企業網站清單設定為適用於舊版 Microsoft Edge，則您的工作已基本完成！ 您可能需要新增的一件事是中性網站。

中性網站通常是提供單一登入 (SSO) 的網站。 如果從 Microsoft Edge 瀏覽到中性網站，要留在 Microsoft Edge 進行驗證。 如果在 Internet Explorer 模式下瀏覽到中性網站，則要保持 Internet Explorer 模式進行驗證。

識別您使用的任何 SSO (或其他中性) 網站，並將這些網站新增到企業網站清單中。

### 如果您已將 Internet Explorer 設定為預設瀏覽器

如果您目前僅使用 Internet Explorer，則可能不知道哪些網站已升級到現代網站標準，哪些網站仍需要 Internet Explorer。 您要找到這些網站並將其新增到企業網站清單中。 這可讓您僅在需要的網站上使用 Internet Explorer 模式。

> [!TIP]
> 使用[企業網站探索](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery?redirectedfrom=MSDN)工具，發現可能需要 Internet Explorer 模式的網站。 您可以在執行 Windows Internet Explorer 8 到 Internet Explorer 11 的 Windows 10、Windows 8.1 或 Windows 7 電腦上收集資料。

### 分析站台探索資料

收集網站資料後，我們建議採用以下 4 步驟程序來分析資料：

1. 依網域，然後依 URL 對資料進行分類。
2. 定義「應用程式」的界限，為 Internet Explorer 模式進行設定。 您要包括定義應用程式的所有網站和 Web 控制項。 但是，不要太廣泛地定義應用程式，包含任何額外的網站和控制項。 某些網站可能像 "http://contoso.com/app1" 一樣簡單，某些網站可能要求您定義多個網站和頁面。
3. 測試應用程式以確認是否無法原生運作。 許多網站在偵測到現代瀏覽器時會提供現代內容，並且僅在偵測到 Internet Explorer 時提供舊版內容。
4. 如果應用程式未通過測試，則將其新增到企業網站清單中。

   > [!NOTE]
   > 最佳做法是，對組成應用程式的所有網站分組在一起。 如果所有網站都需要用於完成一項工作，並且它們傾向於一起更新，則表示它們應該分組在一起。 這樣，當您升級應用程式時，從 Internet Explorer 模式中刪除整個網站，並為該應用程式開始使用現代瀏覽器會更輕鬆。

## 決定您的通道策略

Microsoft Edge 在[多個通道](https://docs.microsoft.com/DeployEdge/microsoft-edge-channels)中發行。

> [!NOTE]
> 您可以在裝置上安裝多個通道

穩定通道是您希望部署到大多數裝置的通道。 但是，應考慮包含多個裝置和多個通道的部署策略。

### 多個裝置和通道

我們建議將具有代表性的裝置子集設定為使用 Beta 通道。 這樣，您就可以預覽即將推出的瀏覽器變更。 您可以看到這些變更是否會影響終端使用者或應用程式。

您可能還要為某些角色 (如 Web 開發人員) 提供 Dev 通道 (甚至 Canary 通道)。 考慮希望用更流暢和快速變化的通道來鎖定某些裝置，還是讓這些通道可供使用者選擇安裝。

由於可以在裝置上安裝多個通道，因此當使用者選擇安裝發行前版本的通道時，可以降低測試的風險。 例如，如果使用者正在使用 Beta 通道，並且發生問題，就可以切換到穩定通道並繼續工作。 這不會造成障礙，直到問題得到解決。

> [!NOTE]
> 如果使用者啟用同步，則其設定將跨通道同步，從而更輕鬆地在通道之間轉換。

## 定義和設定原則

建立企業網站清單後，我們建議您識別和設定要使用 Microsoft Edge 部署的原則。 這可確保在執行測試時套用這些原則。

首先，考慮您希望使用者擁有的初次執行體驗。 如果要從目前瀏覽器自動匯入設定，請設定 [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun) 原則。

對於安全性原則，我們建議從 Microsoft Edge 安全性基準開始。 可以使用[建議的安全性基準設定](https://techcommunity.microsoft.com/t5/Microsoft-Security-Baselines/Security-baseline-DRAFT-for-Chromium-based-Microsoft-Edge/ba-p/949991)或使用 [Microsoft Intune](https://docs.microsoft.com/intune/protect/security-baseline-settings-edge) 來套用安全性基準。

對於其他原則，我們建議檢閱 [Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-policies) 和 [Microsoft Edge 更新](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies)的原則設定。

### 定義更新策略和原則

您還要確定在部署 Microsoft Edge 後要如何執行更新：

- **允許 Microsoft Edge 自行更新** (預設)。 如果選擇允許自動更新 Microsoft Edge，則 Microsoft Edge 將依您部署的通道確定的速度自動更新。
- **依照您自己的步調更新 Microsoft Edge**。 如果希望明確控制部署更新的時間，可以停用自動更新並自行部署 (請參閱[更新原則參考](https://docs.microsoft.com/DeployEdge/microsoft-edge-update-policies))。停用自動更新後，您可以使用以下工具之一為每個通道部署更新：

- [Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)
- 您選擇的部署工具。

無論您的更新策略如何，我們建議利用環型部署策略。 透過自動更新，這意味著具代表性的使用者樣本執行 Beta 通道，以識別通道 (將成為穩定通道) 的問題。 使用手動更新時，這可能還包括在新的穩定通道組建發行後，對試驗群組進行其他驗證。 隨後是廣泛部署。

>[!NOTE]
>Microsoft Edge 支援僅適用於每個通道中的最新版本的 Microsoft Edge

## 執行應用程式相容性測試

Microsoft Edge 的應用程式相容性非常高 - 如此之高，Microsoft 提供了以下相容性承諾：

1. 如果它適用於 Microsoft Edge *版本 45 及更早版本*，也會適用於 Microsoft Edge *77 版及更高版本*。
2. 如果它適用於 Internet Explorer，也會適用於 Internet Explorer 模式的 Microsoft Edge。
3. 如果它適用於 Google Chrome，也會適用於 Microsoft Edge。

如果在您的應用程式中發現不符合我們的相容性承諾，我們會信守承諾，透過 [Microsoft App 保證](https://www.microsoft.com/fasttrack/microsoft-365/desktop-app-assure)修復它。

### 內部企業營運應用程式測試

儘管我們提供相容性承諾，我們知道許多組織基於合規性或風險管理的原因，必須驗證某些應用程式。 儘管我們期望這非常簡單，但在應用程式測試中，有條理和嚴格是非常重要的。

有兩種方法可以執行應用程式相容性測試：

1. 實驗室測試。 應用程式在具有特定設定的嚴格控制環境中進行驗證。
2. 試驗測試。 應用程式由數量有限的使用者在其日常工作環境中使用自己的裝置進行驗證。

選擇最適合每個應用程式的方法，以管理風險，而不會在相容性測試中過度投資。

### 協力廠商應用程式支援

除了各自的企業營運應用程式外，許多組織會使用外部來源所提供的應用程式。 [準備好用於 Microsoft Edge](deploy-edge-ready-for-edge.md)文章包含您組織中可能正在使用的 Web 應用程式清單。 此清單提供與 Microsoft Edge 搭配使用的產品供應商支援聲明連結。

## 將 Microsoft Edge 部署到試驗群組

定義原則並完成初始應用程式相容性測試後，即可部署到試驗群組。 使用以下工具之一，部署到試驗群組：

- [適用於 Windows 的Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-windows-edge?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)，或[適用於 macOS 的 Microsoft Intune](https://docs.microsoft.com/intune/apps/apps-edge-macos?toc=https://docs.microsoft.com/DeployEdge/toc.json&bc=https://docs.microsoft.com/DeployEdge/breadcrumb/toc.json)
- [Configuration Manager](https://docs.microsoft.com/DeployEdge/deploy-edge-with-configuration-manager)。
- 另一個管理工具，下載並部署 [Microsoft Edge 的 MSI 檔案](https://www.microsoftedgeinsider.com/enterprise)。

## 驗證部署

部署試驗後，您要擷取從使用者獲得的所有意見反應。

- 擷取有關相容性的意見反應。 識別企業網站清單中於網站探索期間未識別的網站。
- 擷取有關原則設定的意見反應。 確保使用者可以使用關鍵功能並完成工作，同時遵循安全性準則。
- 擷取有關易用性和新功能的意見反應。 根據使用者問題，確定應開發和提供訓練的任何領域。

## Microsoft Edge 的廣泛部署

完成試驗，並使用從試驗中吸取的經驗教訓更新部署計畫後，即可對所有使用者執行 Microsoft Edge 的全面部署。  恭喜！

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片 - 部署 Microsoft Edge](microsoft-edge-video-deploy.md)
