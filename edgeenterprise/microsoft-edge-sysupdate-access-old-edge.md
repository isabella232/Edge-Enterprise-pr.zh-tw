---
title: 存取舊版 Microsoft Edge
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 08/17/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何存取舊版 Microsoft Edge。
ms.openlocfilehash: e4733d020f3a681ded50e5a087fe086d39362201
ms.sourcegitcommit: f7f7eb69d2298b0f9779a9fd28e3c4e297ef2e05
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125515"
---
# 安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版

了解如何在安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版。

> [!NOTE]
> 本文適用於 Microsoft Edge [Stable 通道](microsoft-edge-channels.md)。

雖然大多數組織會想要將舊版 Microsoft Edge 取代為新版本，但在某些情況下，使用者可能需要存取兩個版本。 例如：

- 與使用 Microsoft Edge 的其中一個或兩個版本之使用者互動的支援人員。
- 支援使用其中一個或兩個版本的 Microsoft Edge 之客戶的開發人員。

> [!IMPORTANT]
> 不建議您在生產環境中並存執行新版 Microsoft Edge 和舊版 Microsoft Edge。 只有在需要同時測試兩個瀏覽器版本的特定情況下，才能使用這個設定。
>
> 舊版 Microsoft Edge 桌面應用程式將於 2021 年 3 月 9 日終止支援，將有利於新版 Microsoft Edge。 這表示舊版 Microsoft Edge 將不會在該日期之後收到安全性更新。 這項變更適用於所有在舊版 Microsoft Edge 桌面應用程式中執行的體驗。 [進一步瞭解](https://techcommunity.microsoft.com/t5/microsoft-365-blog/microsoft-365-apps-say-farewell-to-internet-explorer-11-and/ba-p/1591666)。

## 開始之前
> [!NOTE]
> 從 Windows 10 版本 20H2 開始已不再包含舊版 Microsoft Edge。 從 Windows 10 的這個版本開始不支援並存體驗。

本文的程序適用於已使用最新安全性更新來更新的系統。 安裝新版本 Microsoft Edge 後，將會隱藏舊版本 (Microsoft Edge 舊版)。 根據預設，所有對舊版本的嘗試啟動都會將使用者重新導向至新安裝的 Microsoft Edge。 本文說明如何在安裝 Microsoft Edge 後繼續使用舊版 Microsoft Edge。

## 快速入門：使用 Microsoft Edge Beta 通道和舊版 Microsoft Edge 並存體驗

在使用本文中的詳細指示之前，請考慮下列兩個步驟，讓您的使用者能夠並存執行舊版 Microsoft Edge 和 Microsoft Edge [Beta 頻道](microsoft-edge-channels.md)。

1. 防止 [Windows Update](https://support.microsoft.com/help/12373/windows-update-faq) 自動安裝 Microsoft Edge 的 Stable 通道。

   > [!TIP]
   > 使用[封鎖程式工具組](microsoft-edge-blocker-toolkit.md)來停用自動傳遞 Microsoft Edge。

2. 安裝新版 Microsoft Edge 的[Beta 通道](https://www.microsoft.com/edge/business/download)。

   > [!NOTE]
   > 如需有關登錄機碼設定的詳細資訊，請參閱[其他資訊](#additional-information)。

這種並存解決方案較不復雜，且需要的管理比本文所述的詳細解決方案更少。 但是，這種解決方案代表您將執行 Beta 通道，而不是 Stable 通道。

## 使用 Microsoft Edge 穩定通道和舊版 Microsoft Edge 的並存體驗

在系統層級安裝下一版 Microsoft Edge 的穩定通道，就會隱藏目前版本 (Microsoft Edge 舊版)。 如果您想要讓您的使用者在 Windows 中並存看到兩個版本的 Microsoft Edge，您可以將 **[允許 Microsoft Edge 並存瀏覽器經驗]** 群組原則設定為 **[啟用]** 來啟用此體驗。

此群組原則記錄於[此處](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)

### 若要設定並存瀏覽器體驗原則：

1. 安裝 [Microsoft Edge For Business](https://www.microsoft.com/edge/business/download) 的原則定義。

   - 挑選您想要使用的通道/組建及平台，然後按一下 [取得原則檔案]。
   - 將壓縮的檔案解壓縮。
   - 將 msedge.admx 和 msedgeupdate.admx 複製到 `C:\Windows\PolicyDefinitions` 目錄中。
   - 將 msedge.adml 和 msedgeupdate.adml (來自適當語言/地區目錄) 複製到 `C:\Windows\PolicyDefinitions\[APPROPRIATE LANGUAGE/LOCALE]` 目錄。

2. 開啟群組原則編輯器 (gpedit.msc)。
3. 在**電腦設定**下，移至*系統管理範本>Microsoft Edge Update>應用程式*。

    > [!NOTE]
    > 如果您沒有看到 *[Microsoft Edge 更新]* 資料夾，請確認步驟 1 已正確完成。

4. 在**應用程式**下，按兩下 [允許 Microsoft Edge 並排瀏覽器體驗]。 在繼續下一步之前，請參閱我們的[最佳作法指導方針](#best-practice-guidance)。

    > [!NOTE]
    > 預設情況下，此群組原則設定為 [未設定]，這將導致在安裝新版本 Microsoft Edge 後隱藏 Microsoft Edge 舊版。

5. 選取**啟用**，然後按一下**確定**。  

設定此原則會將下列登錄機碼設定為「00000001」：

- 索引鍵： `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate`
- 數值名稱： `Allowsxs`
- 數值類型: `'REG_DWORD'`

#### 最佳作法指導方針

為獲得最佳體驗，應在將新版本 Microsoft Edge 部署到使用者裝置之前，先啟用**允許 Microsoft Edge 並排瀏覽器體驗**。

如果在部署 Microsoft Edge 後才啟用群組原則，會產生以下副作用且需執行以下動作：

1. 在新版本 Microsoft Edge 的安裝程式再次執行之前，**允許 Microsoft Edge 並排瀏覽器體驗**不會生效。

   > [!NOTE]
   > 當新版本 Microsoft Edge 更新時，安裝程式可以直接或自動執行。

2. 需要將 Microsoft Edge 舊版重新釘選到 [開始] 或 [工作列]，因為部署新版本 Microsoft Edge 時已移轉釘選。
3. 為 Microsoft Edge 舊版釘選到 [開始] 或 [工作列] 的網站將移轉至新版 Microsoft Edge。

## 其他資訊

完全更新系統並安裝下一版 Microsoft Edge 的 Stable 通道後，系統將設定以下登錄機碼和值：

- 索引鍵： `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}`
- 機碼值： `BrowserReplacement`

  > [!IMPORTANT]
  > 每次更新 Microsoft Edge Stable 通道時，此機碼都會被覆寫。 我們建議的最佳做法是「不要」刪除此機碼，以允許使用者同時存取兩個版本的 Microsoft Edge。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [支援 Microsoft Edge 的 Windows 更新](microsoft-edge-sysupdate-windows-updates.md)
