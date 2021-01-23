---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 01/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge kiosk 模式
ms.openlocfilehash: be353a0e13e9234de40296a2e8dcc31b1b800f52
ms.sourcegitcommit: 8a88fd38bdb5e132e89bf17dd2b5fb72f5d1b4b9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/22/2021
ms.locfileid: "11297469"
---
# 設定 Microsoft Edge kiosk 模式

本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。 另提供一份我們鎖定之功能的藍圖。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

## 概觀

Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。 可使用的鎖定體驗如下：  

- **數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。
- **公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。

兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。

## 設定 Microsoft Edge kiosk 模式

使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。 您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。

### kiosk 模式支援的功能

下表列出 kiosk 模式支援的功能。

|功能|數位/互動式告示板|公用瀏覽|隨 Microsoft Edge 版本 (及更新版本) 提供|
|-|-|-|-|
|InPrivate 瀏覽|是|是|87|
|在非使用狀態時重設|是|是|87|
|[唯讀網址列](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (原則) |否|是 |87|
|[結束時刪除下載](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (原則)  | 是|是 |87|
|F11 已封鎖 (進入/結束全螢幕) | 是 | 是 | 87 |
|F12 已封鎖 (啟動開發人員工具) | 是 | 是 | 87 |
| 支援多個索引標籤 | 否| 是| 87|
|結束工作階段按鈕 | 否| 是| 88|
|所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外 |否|是|88|
| CTRL+N 已封鎖 (開啟新視窗) | 是 | 是 | 89 |
| CTRL+T 已封鎖 (開啟新索引標籤) | 否 | 是 | 89 |
|設定及其他 (...) 將只顯示必要的選項  |否 |是 |89 |

> [!NOTE]
> 隨著 kiosk 模式的演進，提供的功能也會增加。

## 使用 kiosk 模式功能

使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能：

- Kiosk 模式數位/互動式告示板： `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Kiosk 模式公用瀏覽： `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

### 額外命令列選項

- `--no-first-run` ：停用第一個 Microsoft Edge 執行體驗。
- `--kiosk-idle-timeout-minutes` ：在 Microsoft Edge kiosk 模式重設使用者的工作階段之前，變更上次使用者活動的時間 (以分鐘為單位)。 支援的值如下：

  - 預設值
    - 全螢幕 - 關閉
    - 公用瀏覽 - 5 分鐘
  - 允許的值
    - 0 - 關閉計時器
    - 1-1440 分鐘，用於重設閒置時計時器

## 支援 kiosk 模式的原則

使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。 若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](https://docs.microsoft.com/deployedge/microsoft-edge-policies)。

> [!NOTE]
> 原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。

|群組原則|數位/互動式告示板|公用瀏覽單一應用程式|
|--|--|--|
|[列印](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printing-policies) | 是|是 |
|[HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation) |否 | 是|
|[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton) |否 | 是|
|[NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) |否 |是 |
|[FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled) |否 |是 |
|[URLAllowlist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) |是 |是 |
|[URLBlocklist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) |是 | 是|
|[ManagedSearchEngines](https://docs.microsoft.com/deployedge/microsoft-edge-policies#managedsearchengines) |否 | 是|
|[UserFeedbackAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userfeedbackallowed) |否 | 是|
|[VerticalTabsAllowed](https://docs.microsoft.com/deployedge/microsoft-edge-policies#verticaltabsallowed) | 否|是 |
|[SmartScreen 設定](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreen-settings-policies) |是 |是 |

## 具有受指派存取權的 Microsoft Edge

### 單一應用程式 kiosk

Microsoft Edge 目前針對單一應用程式受指派的存取權支援一組相同的舊版 Microsoft Edge kiosk 模式類型，包含下列鎖定體驗：數位/互動式告示板和公用瀏覽。  

您目前可使用最新的  [Windows 10 測試人員預覽版](https://insider.windows.com/) 20215 版或更新版本，以及  [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download) 87.0.644.4 版或更新版本，測試有受指派存取權的 kiosk 模式。

**如何取得 Windows 測試人員預覽？**

若要在電腦上安裝 Windows 10 測試人員預覽版，請依照 [開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。

### 多個應用程式 Kiosk

Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。 若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。 (Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。

使用具有受指派的存取權的 Microsoft Edge 時，您可以設定 Microsoft Edge kiosk 模式，以使用 [Microsoft Edge 瀏覽器原則](https://review.docs.microsoft.com/DeployEdge/microsoft-edge-policies)來設定瀏覽體驗，進而滿足您的獨特需求。

### 使用 Windows 設定進行設定

Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。 使用下列步驟設定單一應用程式 kiosk 電腦。

1. 安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。 依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。
2. 安裝最新版本的 [Microsoft Edge 穩定通道](https://www.microsoft.com/edge)版本 87 或更新版本。  若要測試最新功能，您可以下載最新的 [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本。

   > [!IMPORTANT]
   > 由於需要裝置層級安裝，因此僅支援一個非 Canary 通道。

3. 在 kiosk 電腦上，開啟 [Windows 設定]，然後在搜尋欄位中輸入「kiosk」。 如下一個螢幕擷取畫面所示，選取 ** **[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. 在 ** ** [設定 kiosk] 頁面上，按一下 ** **[開始使用]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. 輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 ** **[下一步]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. 在** ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** **[下一步]。

   > [!NOTE]
   > 這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="Kiosk 模式 - 選擇應用程式":::

7. 針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：

   - 數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。
   - 公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

8. 選取 ** **[下一步]。
9. 輸入 kiosk 啟動時要載入的 URL。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. 接受 5 分鐘的閒置時間預設值，或提供您自己的值。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. 按 ** **[下一步]。
12. 關閉 ** ** [設定] 視窗，儲存並套用您的選擇。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. 從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。

## 功能限制

隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。

建議您關閉：

- [StartupBoostEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#startupboostenabled)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [Extensions](https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions-policies)
- [BackgroundModeEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#backgroundmodeenabled)

## 藍圖

### 2021 年年初

我們將增加下列支援和功能：

- 在 Windows 10 1909 和更新版本上，具有獲指派存取權單一應用程式之 Microsoft Edge kiosk 模式的正式發行。
- 與舊版 Microsoft Edge 同等的其他功能。
- 與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。
- 將封鎖其他鍵盤快速鍵。
- 限制從瀏覽器啟動其他應用程式。

## 請參閱

- [設定 Windows 桌面版的 Kiosk 與數位招牌](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [部署 Microsoft Edge 舊版 kiosk 模式](https://aka.ms/edgekioskmode)
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
