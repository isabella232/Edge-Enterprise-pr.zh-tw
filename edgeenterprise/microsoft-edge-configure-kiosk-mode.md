---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 09/22/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge kiosk 模式
ms.openlocfilehash: d7c9df82079f8343d43ccfd312623e6e01358fa9
ms.sourcegitcommit: 858227653fc89532d1d274735f53280e27b2a8c0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/22/2020
ms.locfileid: "11072658"
---
# 設定 Microsoft Edge kiosk 模式

本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。 另外，功能藍圖也是我們的目標。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

如需 Microsoft Edge 舊版 kiosk 模式 (版本 45 和較舊版本) 的相關資訊，請參閱[部署 Microsoft Edge kiosk 模式](https://aka.ms/edgekioskmode)。

## 概觀

Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。 可使用的鎖定體驗如下：  

- 數位/互動式告示板體驗以全螢幕模式顯示特定網站。
- 公用瀏覽體驗執行受限制的 Microsoft Edge 多索引版本。

兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。

## 設定 Microsoft Edge kiosk 模式  

您現在可以使用 Microsoft Edge Canary 通道版本 87 測試最初的 kiosk 模式功能組。 您可以從[ ](https://www.microsoftedgeinsider.com/download)[Microsoft Edge Insider Channels] 頁面下載 Microsoft Edge Canary。

### Kiosk 模式功能

下列功能可供使用：

- InPrivate 瀏覽。 工作階段結束時會刪除瀏覽器資料和下載項目，保護使用者資料。
- 設定退出時刪除下載項目的原則。
- 閒置一段時間後，重設使用者工作階段。
- 初始的鎖定功能組。 可用功能如下：

  - 滑鼠快顯功能表
  - F12 開發人員工具
  - F11 退出全螢幕 (在全螢幕模式時)
  - 封鎖最初一組 *Edge://* 頁面

> [!NOTE]
> Kiosk 模式會逐漸演變，提供的功能也會增加。

### 使用 kiosk 模式功能

使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能：

- Kiosk 模式數位/互動式告示板： `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen`
- Kiosk 模式公用瀏覽： `msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing`

#### 額外命令列選項

- `--no-first-run` ：停用第一個 Microsoft Edge 執行體驗。
- `--kiosk-idle-timeout-minutes` ：在 Microsoft Edge kiosk 模式重設使用者的工作階段之前，變更上次使用者活動的時間 (以分鐘為單位)。 支援的值如下：

  - 預設值
    - 全螢幕 - 關閉
    - 公用瀏覽 - 5 分鐘
  - 允許的值
    - 0 - 關閉計時器
    - 在閒置計時器重設為 1-1440 分鐘

## 設定有受指派存取權的 kiosk 模式

您目前可使用最新的 [Windows 10 測試人員預覽版](https://insider.windows.com/) 20215 版或更新版本，以及 [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download) 87.0.644 版或更新版本，測試有受指派存取權的 kiosk 模式。

**如何取得 Windows 測試人員預覽？**

若要在電腦上安裝 Windows 10 測試人員預覽版，請依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。

### 使用 Windows 設定進行設定

Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。 使用下列步驟設定單一應用程式 kiosk 電腦。

1. 安裝最新的 Windows 10 測試人員預覽版，20215 版或更新版本。 請依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。
2. 安裝最新版的 [Microsoft Edge Dev 通道](https://www.microsoftedgeinsider.com/download)，87.0.644 版或更新版本。

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

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="Kiosk 模式 - 完成設定":::

13. 從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，驗證設定。

## 功能限制

推出這個預覽版 kiosk 模式時，我們會持續改善產品並增加新功能。

雖然 kiosk 模式目前不支援下列功能，但是下列功能正在開發中：

- 集合
- Extensions
- Internet Explorer 模式
- Windows Defender 應用程式防護 (WDAG)

## 藍圖

### 今年下半年 (2020)

我們會增加下列功能：

- 結束工作階段按鈕
- 唯讀 URL 網址列  
  - 可使用群組原則設定
  - 啟用時，使用者無法為了瀏覽其他頁面編輯網址列 URL。

- 更多鎖定功能：

  - 封鎖更多加速器 (例如，CTRL+N)
  - 「...」設定功能表只會啟用必要的選項 (例如列印、說明、意見反應和 大聲朗讀)
  - 其他 *edge://* 頁面鎖定 (例如 *edge://settings*)
  - 設定列印選項 UI
  - 將檔案總管限制為僅限下載資料夾。

### 2021 年初

我們會增加下列支援和功能：

- 在 Windows 正式發行有受指派存取權單一應用程式的 Microsoft Edge kiosk 模式。
- 與 Microsoft Edge 舊版具有其他相同功能。
- 與 Intune 整合，以使用 kiosk 模式設定檔 UX 來設定裝置。

## 請參閱

- [設定 Windows 桌面版的 Kiosk 與數位招牌](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [部署 Microsoft Edge 舊版 kiosk 模式](https://aka.ms/edgekioskmode) 
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)