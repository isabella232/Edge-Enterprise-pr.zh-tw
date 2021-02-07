---
title: 規劃 kiosk 模式轉換
ms.author: aguta
author: aguta
manager: srugh
ms.date: 02/05/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 規劃 kiosk 模式轉換
ms.openlocfilehash: 3a438c6dd71d9e1f0e644d24e3b1d1d60b099e8e
ms.sourcegitcommit: b1d49b229c47dc1d99e1b677d75aad38b3334ed6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "11314233"
---
# 規劃 kiosk 模式轉換

本文提供有關如何將您的 kiosk 從舊版 Microsoft Edge 轉換至 Microsoft Edge 的指導方針。  

> [!NOTE]
> 本文適用於 Microsoft Edge 穩定、Beta 和 Dev 通道，版本 87 或更新版本。

> [!IMPORTANT]
> 當舊版 Microsoft Edge 的支援服務於 2021 年 3 月 9 日終止時，將隨著 4 月的 Windows Update 將其移除並以 Microsoft Edge on Chromium 取代。 如需詳細資訊，請移至[此部落格文章](https://aka.ms/EdgeLegacyEOS)。 若要繼續使用您的瀏覽器型 kiosk 案例，您需要在 4 月的 Windows Update 向您的裝置釋出之前安裝 Microsoft Edge on Chromium，並設定 kiosk 模式。

## kiosk 設定步驟

若要在 Microsoft Edge 中設定 kiosk，請使用下列步驟做為指南。

**步驟 1：對照已釋出 (及即將到來) 的 kiosk 模式功能評估您的需求。** 下表列出 Microsoft Edge on Chromium 與舊版 Microsoft Edge 中的 kiosk 模式所支援的功能。 使用此表格做為轉換至 Microsoft Edge 的指南，方法是比較在這兩個版本的 Microsoft Edge 中支援這些功能的情況。

|功能|數位/互動式告示板|公用瀏覽|隨 Microsoft Edge 版本 (及更新版本) 提供|隨舊版 Microsoft Edge 提供|
|-|-|-|-|-|
|InPrivate 瀏覽|是|是|89|是|
|在非使用狀態時重設|是|是|89|是|
|[唯讀網址列](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) (原則) |否|是 |89|否|
|[結束時刪除下載](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) (原則)  | 是|是 |89|否|
|F11 已封鎖 (進入/結束全螢幕) | 是 | 是 | 89 |是|
|F12 已封鎖 (啟動開發人員工具) | 是 | 是 | 89 |是|
| 支援多個索引標籤 | 否| 是| 89|是|
|[允許 URL 支援](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlallowlist) (原則)|是|是|89|否|
|[封鎖 URL 支援](https://docs.microsoft.com/deployedge/microsoft-edge-policies#urlblocklist) (原則)|是|是|89|否|
|[顯示首頁按鈕](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showhomebutton) (原則)|否|是|89|是|
|[管理我的最愛](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#managedfavorites) (原則)|否|是|89|是|
|[啟用印表機](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printingenabled) (原則)|是|是|89|是|
|[設定新的索引標籤頁面 URL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation) (原則)|否|是||是|
|結束工作階段按鈕 | 否| 是| 89|是|
|所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外 |否|是|89|是|
| CTRL+N 已封鎖 (開啟新視窗) | 是 | 是 | 89 |是|
| CTRL+T 已封鎖 (開啟新索引標籤) |是 | 是 | 89 |是|
|設定及其他 (...) 將只顯示必要的選項  |是 |是 |89 |是|
|限制從瀏覽器啟動其他應用程式|是|是|90/91|是|
|UI 列印設定鎖定|是|是|90/91|是|
|[將新的索引標籤頁面設定為首頁](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepageisnewtabpage) (原則)|-|-|待決定|是|

> [!NOTE]
> 如需 Microsoft Edge 發行排程的相關資訊，請參閱 [Microsoft Edge 發行排程](microsoft-edge-release-schedule.md)。

**步驟 2：在 Microsoft Edge 中測試新 kiosk。** 建議您在 Microsoft Edge 中測試 kiosk 模式。 若要快速且輕鬆地測試 kiosk 模式，您可以使用 Windows [設定] 來設定受指派存取權的單一應用程式，如下所述。

1. 安裝最新的 Windows 10 測試人員預覽版本 20215 或更新版本。 依照[開始使用 Windows 10 測試人員預覽版](https://docs.microsoft.com/windows-insider/get-started)中的指示進行。
2. 安裝最新版本的 [Microsoft Edge 穩定通道](https://www.microsoft.com/edge)版本 87 或更新版本。  若要測試最新功能，您可以下載最新的 [Microsoft Edge Beta 通道](https://www.microsoftedgeinsider.com/download)版本 89 或更新版本。

   > [!IMPORTANT]
   > 由於需要裝置層級安裝，因此不支援 Canary 通道。

3. 在 kiosk 電腦上，開啟 Windows [設定]，然後在搜尋欄位中輸入 "kiosk"。 如下一個螢幕擷取畫面所示，選取 ** **[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. 在 ** ** [設定 kiosk] 頁面上，按一下 ** **[開始使用]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. 輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 ** **[下一步]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. 在 [選擇 kiosk 應用程式]****  頁面上，選取 [Microsoft Edge]****，然後按 [下一步] ****。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-4-pick-app.png" alt-text="kiosk 模式 - 選擇應用程式":::

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

**步驟 3：開發轉換計畫。** 根據您的測試和組織需求，建議您開發轉換計畫，並於舊版 Microsoft Edge 的支援服務於 2021 年 3 月 9 日結束之前，移至 Microsoft Edge on Chromium。

## 需要重新建立現有 kiosk 模式的其他案例

如果您更新至 Windows 10 版本 20H2，則會安裝 Microsoft Edge on Chromium，並且會隱藏舊版 Microsoft Edge。 在此情況中，您必須在 Microsoft Edge on Chromium 中再次設定 kiosk 模式。

## 如何取得協助

kiosk 模式可能是您日常業務的重要部分，因此我們想要協助您讓此轉換盡可能順暢，並協助您避免中斷。 如果您的企業需要協助轉換到 Microsoft Edge on Chromium：

- Microsoft 提供[支援服務](https://support.serviceshub.microsoft.com/supportforbusiness/create?sapId=a77ee9b7-b6b6-aa08-d7b9-887ebe228207)。 
- 如果客戶擁有 150 個或更多個 Windows 10 企業版基座，就可以免費使用 [FastTrack 支援](https://www.microsoft.com/fasttrack/microsoft-365/microsoft-edge?rtc=1)。
- 如果您遇到網站或應用程式相容性問題，就能使用[應用裝置保證](https://www.microsoft.com/en-us/fasttrack/microsoft-365/app-assure)。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [新的 Microsoft Edge 會隨著 4 月的 Windows 10 更新星期二發行取代舊版 Microsoft Edge](https://techcommunity.microsoft.com/t5/microsoft-365-blog/new-microsoft-edge-to-replace-microsoft-edge-legacy-with-april-s/ba-p/2114224)