---
title: 使用 Jamf 在 macOS 上設定 Microsoft Edge
ms.author: brianalt
author: dan-wesley
manager: laurawi
ms.date: 11/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 Jamf 在 Mac 裝置上設定 Microsoft Edge 原則設定
ms.openlocfilehash: 1859d9fb1fd3ea8ff6908c41f75df21a8b338769
ms.sourcegitcommit: ed6a5afabf909df87bec48671c4c47bcdfaeb7bc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/02/2020
ms.locfileid: "11194711"
---
# 使用 Jamf 在 macOS 上設定 Microsoft Edge 原則設定

本文說明如何在 Jamf Pro 10.19 上使用 Microsoft Edge 原則清單檔案來設定 macOS 上的原則設定。

您也可以使用屬性清單 (plist) 檔案，在 macOS 上設定 Microsoft Edge 原則設定。 如需詳細資訊，請參閱[使用 .plist 為 macOS 設定](configure-microsoft-edge-on-mac.md)。


##  <a name="prerequisites"></a>必要條件

需要下列軟體：

- Microsoft Edge 穩定通道 81
- 原則範本檔案，版本 81.0.416.3
- Jamf Pro，版本 10.19

##  <a name="about-the-jamf-pro-application-&-custom-settings-menu"></a>關於 Jamf Pro 應用程式與自訂設定功能表

Jamf Pro 10.18 之前，管理 Office 365 牽涉到手動建立 .plist 檔案。 這是耗時的工作流程，需要強大的技術背景。 Jamf Pro 10.18 將組態流程簡化，以消除這些障礙。 不過，IT 系統管理員只能針對 Jamf 所指定的特定應用程式和喜好設定網域使用這個新的使用者介面。

在 Jamf Pro 10.19 中，使用者可以將 JSON 資訊清單上傳為「自訂結構描述」，以鎖定任何喜好設定網域，而圖形使用者介面則會從此資訊清單產生。 建立的自訂架構會遵循 JSON 架構規格。

如需詳細資訊，請參閱 Jamf Pro 系統管理員指南中的[電腦組態設定檔](https://jamf.it/computer-configuration-profiles)。

##  <a name="get-the-policy-manifest-for-a-specific-version-of-microsoft-edge"></a>取得特定版本 Microsoft Edge 的原則資訊清單

若要取得原則資訊清單：

- 移至 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)。
- 在 [通道/版本] 下拉式清單中，選取版本 81 或更新版本的任何通道****_。
- 在 [建立] 下拉式清單中，選取任何 81 組建或更新版本_***_。
- 按一下 [取得原則檔案] 來下載我們的原則範本組合。

  > [!NOTE]
  > 目前，原則範本組合會以 CAB 檔案形式簽署。 您需要使用協力廠商工具，例如 The Unarchiver，以在 macOS 上開啟檔案。

將 CAB 檔案解壓縮之後，將 ZIP 檔案解壓縮，並瀏覽至 "mac" 頂層目錄。 名稱為 "policy_manifest.json" 的資訊清單位於這個目錄中。

此資訊清單將會在從組建 81.0.416.3 開始的每個原則組合中發佈。 如果您想要在開發人員通道中測試原則，您可以使用與每個開發發行相關的資訊清單，並在 Jamf Pro 中進行測試。  

##  <a name="use-the-policy-manifest-in-jamf-pro"></a>在 Jamf Pro 中使用原則資訊清單

使用下列步驟將原則資訊清單上傳到 Jamf Pro，然後針對 macOS 建立原則設定檔。

1. 登入 Jamf。
2. 選取 [電腦]_*** 索引標籤。
3. 在 [內容管理]**** 底下，選取 [組態設定檔]****。
4. 在 [組態設定檔]**** 頁面上，按一下 [+ 新增]****。

   ![在 Jamf 中新增設定檔](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles.png)

5. 在 [新增 macOS 組態設定檔]**** > [選項]**** 中，選取 [應用程式與自訂設定]****。
6. 在 [應用程式與自訂設定]**** 快顯視窗中，按一下 [設定]****。

   ![設定應用程式與自訂設定](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom.png)

7. 在 [應用程式與自訂設定]**** 區段中，設定下列螢幕擷取畫面中顯示的值。

   ![設定檔來源和自訂結構描述](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-schema.png)

   - 針對 [建立方法]****，挑選 [組態設定]****。
   - 針對 [來源]****，挑選 [自訂結構描述]****。
   - 針對 [喜好設定網域]****，提供您網域的名稱。 此範例使用 *com.microsoft.Edge* 做為網域。
   - 在 [自訂架構]**** 中，貼上 "policy_manifest.json" 資訊清單檔案的內容。
   - 按一下 **[儲存]**。

8. 儲存設定檔後，Jamf 會顯示 [一般]**** 區段 (在下個螢幕擷取畫面中顯示)。

   ![設定一般區段](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-app-and-custom-general-setting.png)

   - 為設定檔提供顯示 [名稱]****，以及 [描述]****。
   - 保留 [類別]**** 的預設值，也就是 [無]****。
   - 針對 [散發方法]****，選項為 [自動安裝]**** 或 [可在自助服務中使用]****。
   - 針對 [層級]****，選項為 [使用者層級]**** 或 [電腦層級]****。
   - 按一下 **[儲存]**。

9. 儲存 [一般] 區段之後，Jamf 會顯示我們範例的「Microsoft Edge Beta 通道」組態設定檔。 在下一個螢幕擷取畫面中，請注意，您可以按一下 [編輯]**** 繼續處理設定檔，或如果您已完成，請按一下 [完成]****。

   ![含有選項的新組態設定檔](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel.png)

   > [!NOTE]
   > 您可以在儲存設定檔之後以及在另一個 Jamf 工作階段中編輯此設定檔。 例如，您可能決定將 [散發方法] 變更為 [可在自助服務中使用]。

   若要在 Microsoft Edge 穩定通道上執行追蹤編輯，或將它刪除，請選取後續的 [組態設定檔] 螢幕擷取畫面中顯示的設定檔名稱。

   ![組態設定檔清單](media/configure-microsoft-edge-on-mac-jamf/configure-macos-jamf-configuration-profiles-beta-channel-done.png)

建立新的組態設定檔之後，您仍需為設定檔設定**範圍**。

###  <a name="to-configure-the-scope"></a>設定範圍

1. 針對 [目標]****，提供下列最小設定：

   - 目標電腦。 選項為 [特定電腦] 或 [所有電腦]。
   - 目標使用者。 選項為 [特定使用者] 或 [所有使用者]。
   - 按一下 **[儲存]**。
2. 針對 [限制]****，請保留預設設定：[無]。 按一下 [取消]****。
3. 針對 [排除]****，請保留預設設定：[無]。 按一下 [取消]****。

##  <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [使用 Intune 針對 macOS 設定](configure-microsoft-edge-on-mac.md)
- [進行 Windows 的設定](configure-microsoft-edge.md)
- [使用 Intune 進行 Windows 的設定](configure-edge-with-intune.md)
