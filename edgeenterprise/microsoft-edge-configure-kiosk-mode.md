---
title: 設定 Microsoft Edge kiosk 模式
ms.author: aguta
author: aguta
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 瞭解 Kiosk 模式功能，以及如何設定 Microsoft Edge Kiosk 模式選項。
ms.openlocfilehash: 38d94a5dfac15f810a463e43ad2fe44d51ee66c7
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642189"
---
# <a name="configure-microsoft-edge-kiosk-mode"></a>設定 Microsoft Edge kiosk 模式

本文說明如何設定供您試驗的 Microsoft Edge kiosk 模式選項。 另提供一份我們鎖定之功能的藍圖。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

> [!IMPORTANT]
> 使用[使用 kiosk 模式功能](#use-kiosk-mode-features)中的命令列引數，叫用 Windows 10 上的 Microsoft Edge kiosk 模式功能。

## <a name="overview"></a>概觀

Microsoft Edge kiosk 模式提供兩種瀏覽器鎖定體驗，組織可建立、管理以及為客戶提供最佳的體驗。 可使用的鎖定體驗如下：  

- **數位/互動式告示板**體驗 - 以全螢幕模式顯示特定網站。
- **公用瀏覽**體驗 - 可執行受限制的 Microsoft Edge 多索引標籤版本。

兩個體驗皆執行 Microsoft Edge InPrivate 工作階段，可保護使用者資料。

## <a name="set-up-microsoft-edge-kiosk-mode"></a>設定 Microsoft Edge kiosk 模式

使用 Microsoft Edge 穩定通道版本 87 可測試初始的一組 kiosk 模式功能。 您可以從 [Microsoft Edge (官方穩定通道)](https://www.microsoft.com/edge) 下載最新版本。

### <a name="kiosk-mode-supported-features"></a>kiosk 模式支援的功能

下表列出 Microsoft Edge 與舊版 Microsoft Edge 中的 kiosk 模式所支援的功能。 使用此表格做為轉換至 Microsoft Edge 的指南，方法是比較在這兩個版本的 Microsoft Edge 中支援這些功能的情況。

|功能|數位/互動式告示板|公用瀏覽|隨 Microsoft Edge 版本 (及更新版本) 提供|隨舊版 Microsoft Edge 提供|
|-|-|-|-|-|
|InPrivate 瀏覽|是|是|89|是|
|在非使用狀態時重設|是|是|89|是|
|[唯讀網址列](./microsoft-edge-policies.md#kioskaddressbareditingenabled) (原則) |否|是 |89|否|
|[結束時刪除下載](./microsoft-edge-policies.md#kioskdeletedownloadsonexit) (原則)  | 是|是 |89|否|
|F11 已封鎖 (進入/結束全螢幕) | 是 | 是 |89|是|
|F12 已封鎖 (啟動開發人員工具) | 是 | 是 |89|是|
| 支援多個索引標籤 | 否| 是|89|是|
|[允許 URL 支援](./microsoft-edge-policies.md#urlallowlist) (原則)|是|是|89|否|
|[封鎖 URL 支援](./microsoft-edge-policies.md#urlblocklist) (原則)|是|是|89|否|
|[顯示首頁按鈕](./microsoft-edge-policies.md#showhomebutton) (原則)|否|是|89|是|
|[管理我的最愛](./microsoft-edge-policies.md#managedfavorites) (原則)|否|是|89|是|
|[啟用印表機](./microsoft-edge-policies.md#printingenabled) (原則)|是|是|89|是|
|[設定新的索引標籤頁面 URL](./microsoft-edge-policies.md#newtabpagelocation) (原則)|否|是|89|是|
|結束會話按鈕 * | 否| 是|89|是|
|所有內部 Microsoft Edge URL 都會遭到封鎖，*edge://downloads* 和 *edge://print* 除外 |否|是|89|是|
| CTRL+N 封鎖 (開啟新的視窗 #) * | 是 | 是 |89|是|
| CTRL+T 已封鎖 (開啟新索引標籤) |是 | 否 |89|是|
|設定及其他 (...) 將只顯示必要的選項  |是 |是 |89|是|
|限制從瀏覽器啟動其他應用程式|是|是|90|是|
|UI 列印設定鎖定|是|是|90|是|
|[將新的索引標籤頁面設定為首頁](./microsoft-edge-policies.md#homepageisnewtabpage) (原則)|否|是|90|是|

> [!NOTE]
> 只有在指派的存取單一應用程式情況下，才能啟用後面接著 "*" 的功能。

## <a name="use-kiosk-mode-features"></a>使用 kiosk 模式功能

針對數位/互動式告示板和公開瀏覽使用下列 Windows 10 命令列選項，即可叫用 Microsoft Edge kiosk 模式功能。

### <a name="kiosk-mode-digitalinteractive-signage"></a>kiosk 模式數位/互動式告示板
 
```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen
```

### <a name="kiosk-mode-public-browsing"></a>kiosk 模式公用瀏覽：

```
msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing
```

### <a name="additional-command-line-options"></a>其他命令列選項

- **--no-first-run**：停用 Microsoft Edge 初次執行體驗。

   ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --no-first-run
  ```

  ```
  msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --no-first-run
  ```

- **--kiosk-idle-timeout-minutes=**：變更從上次使用者活動經過的時間 (以分鐘為單位)，在此時間後，Microsoft Edge kiosk 模式便重設使用者的工作階段。 將以下範例中的「值」以分鐘數取代。

   ```
   --kiosk-idle-timeout-minutes=value
   ``` 
   下列是支援的「值」：

     - 預設值 (以分鐘為單位)
       - 全螢幕 - 0 (關閉)
       - 公用瀏覽 - 5 分鐘
    - 允許的值
      - 0 - 關閉計時器
      - 1-1440 分鐘，用於重設閒置時計時器


    ```
    msedge.exe --kiosk www.contoso.com --edge-kiosk-type=fullscreen --kiosk-idle-timeout-minutes=1
   ```

   ```
   msedge.exe --kiosk www.contoso.com --edge-kiosk-type=public-browsing --kiosk-idle-timeout-minutes=1
   ```

## <a name="support-policies-for-kiosk-mode"></a>支援 kiosk 模式的原則

使用下表中所列的任何 Microsoft Edge 原則，以針對您設定的 Microsoft Edge kiosk 模式類型來加強 kiosk 體驗。 若要深入了解這些原則，請參閱 [Microsoft Edge - 瀏覽器原則參考](./microsoft-edge-policies.md)。

> [!NOTE]
> 原則設定並不限於下表所列的原則，但其他原則應經過測試，以確保 kiosk 模式功能不會受到負面影響。

|群組原則|數位/互動式告示板|公用瀏覽單一應用程式|
|--|--|--|
|[列印](./microsoft-edge-policies.md#printing-policies) | 是|是 |
|[HomePageLocation](./microsoft-edge-policies.md#homepagelocation) |否 | 是|
|[ShowHomeButton](./microsoft-edge-policies.md#showhomebutton) |否 | 是|
|[NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation) |否 |是 |
|[FavoritesBarEnabled](./microsoft-edge-policies.md#favoritesbarenabled) |否 |是 |
|[URLAllowlist](./microsoft-edge-policies.md#urlallowlist) |是 |是 |
|[URLBlocklist](./microsoft-edge-policies.md#urlblocklist) |是 | 是|
|[ManagedSearchEngines](./microsoft-edge-policies.md#managedsearchengines) |否 | 是|
|[UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed) |否 | 是|
|[VerticalTabsAllowed](./microsoft-edge-policies.md#verticaltabsallowed) | 否|是 |
|[SmartScreen 設定](./microsoft-edge-policies.md#smartscreen-settings-policies) |是 |是 |
|[EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)|是|是|

## <a name="microsoft-edge-with-assigned-access"></a>具有受指派存取權的 Microsoft Edge

### <a name="single-app-kiosk"></a>單一應用程式 kiosk

Microsoft Edge 版本 90 kiosk 模式提供廣泛的功能清單。 請參閱 Kiosk 模式支援功能一節。
透過下列 Windows 更新，您可以透過受指派的存取權單一應用程式來設定 Microsoft Edge。

|作業系統|版本|更新|
|--|--|--|
|Windows 10 | 2004 或更新版本|[KB4601382 或更新](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 或更新](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

您可以透過 [Windows 設定](/deployedge/microsoft-edge-configure-kiosk-mode#configure-using-windows-settings)和 Intune 管理 Microsoft Edge kiosk 模式受指派的存取權單一應用程式。

### <a name="multi-app-kiosk"></a>多個應用程式 Kiosk

Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於舊版 Microsoft Edge「一般瀏覽」kiosk 模式類型。 若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](/windows/configuration/lock-down-windows-10-to-specific-apps) 中的指示進行。 (Microsoft Edge 穩定通道的 AUMID 是 **MSEdge**)。

### <a name="configure-using-windows-settings"></a>使用 Windows 設定進行設定

Windows 設定是設定一或兩部單一應用程式 kiosk 裝置最簡單的方法。 使用下列步驟設定單一應用程式 kiosk 電腦。

1. 下表列出作業系統的最小系統更新。

|作業系統|版本|更新|
|--|--|--|
|Windows 10 | 2004 或更新版本|[KB4601382 或更新](https://support.microsoft.com/topic/february-24-2021-kb4601382-os-builds-19041-844-and-19042-844-preview-1a7ed2b4-017d-2644-a1e8-dd6bf14cba76) |
|Windows 10| 1909| [KB4601380 或更新](https://support.microsoft.com/topic/february-16-2021-kb4601380-os-build-18363-1411-preview-2e3c38e1-a947-1033-8006-a30f3806da18)|

2. 若要測試最新功能，您可以下載最新的 [Microsoft Edge 穩定通道](https://www.microsoft.com/edge/business/download)版本 89 或更新版本。

3. 在 kiosk 電腦上，開啟 Windows [設定]，然後在搜尋欄位中輸入 "kiosk"。 如下一個螢幕擷取畫面所示，選取 ** **[設定 kiosk (受指派的存取權)]，開啟建立 kiosk 的對話方塊。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-1-assigned-access.png" alt-text="設定有受指派存取權的 kiosk":::

4. 在 ** ** [設定 kiosk] 頁面上，按一下 ** **[開始使用]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-2-get-started.png" alt-text="Kiosk 頁面 -開始使用":::

5. 輸入名稱以建立新的 kiosk 帳戶，或從填入的下拉式清單選擇現有帳戶，然後按 ** **[下一步]。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-3-create-account.png" alt-text="Kiosk 模式 - 建立帳戶":::

6. 在** ** [選擇 kiosk 應用程式] 頁面上，選取** **[Microsoft Edge]，然後按 ** **[下一步]。

   > [!NOTE]
   > 這僅適用於 Microsoft Edge Dev、Beta 和 Stable 通道。

     :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5c-choose-a-kiosk-app.png" alt-text="Kiosk 模式顯示 - 全螢幕數位告示板":::

7. 針對以 kiosk 模式執行時 Microsoft Edge 的顯示方式，選取下列其中一個選項：

   - 數位/互動式告示板 - 執行 Microsoft Edge，以全螢幕模式顯示特定網站。
   - 公用瀏覽器 - 執行受限制的 Microsoft Edge 多索引版本。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-5a-digital-sign.png" alt-text="如何使用 kiosk - 全螢幕數位標誌":::

8. 選取 ** **[下一步]。
9. 輸入 kiosk 啟動時要載入的 URL。

   :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-6-enter-url.png" alt-text="Kiosk 模式 - 輸入 URL":::

10. 接受 5 分鐘的閒置時間預設值，或提供您自己的值。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode-7-enter-idle-time.png" alt-text="Kiosk 模式 - 輸入閒置時間":::

11. 按 ** **[下一步]。
12. 關閉 ** ** [設定] 視窗，儲存並套用您的選擇。

    :::image type="content" source="media/microsoft-edge-configure-kiosk-mode/ms-kiosk-mode--8-done.png" alt-text="kiosk 模式 - 完成設定":::

13. 從 kiosk 裝置登出，然後使用本機 kiosk 帳戶登入，以驗證設定。

## <a name="functional-limitations"></a>功能限制

隨著本預覽版 kiosk 模式的推出，我們會持續改善產品並增加新功能。

我們目前不支援下列功能，建議您關閉：

- [InPrivateModeAvailability](./microsoft-edge-policies.md#inprivatemodeavailability)
- [IsolateOrigins](./microsoft-edge-policies.md#isolateorigins)
- [ManagedFavorites](./microsoft-edge-policies.md#managedfavorites)
- [EdgeShoppingAssistantEnabled](./microsoft-edge-policies.md#edgeshoppingassistantenabled)
- [EdgeCollectionsEnabled](./microsoft-edge-policies.md#edgecollectionsenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)
- [DefaultPopupsSetting](./microsoft-edge-policies.md#defaultpopupssetting)
- [StartupBoostEnabled](./microsoft-edge-policies.md#startupboostenabled)
- [InternetExplorerIntegrationLevel](./microsoft-edge-policies.md#internetexplorerintegrationlevel)
- [Extensions](./microsoft-edge-policies.md#extensions-policies)
- [BackgroundModeEnabled](./microsoft-edge-policies.md#backgroundmodeenabled)
- [UserFeedbackAllowed](./microsoft-edge-policies.md#userfeedbackallowed)

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [規劃 Microsoft Edge 部署](deploy-edge-plan-deployment.md)
- [設定 Windows 桌面版的 kiosk 與數位招牌](/windows/configuration/kiosk-methods)
- [規劃 kiosk 模式轉換](microsoft-edge-kiosk-mode-transition-plan.md)
