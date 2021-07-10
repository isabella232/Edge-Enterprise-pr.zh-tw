---
title: Microsoft Edge WebView2 原則文件
ms.author: stmoody
author: dan-wesley
manager: tahills
ms.date: 06/29/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge 瀏覽器支援的所有原則的 Windows 和 Mac 文件
ms.openlocfilehash: cec4ab92257322b93072b694ceddc7ab6351b287
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642939"
---
# <a name="microsoft-edge-webview2---policies"></a>Microsoft Edge WebView2 - 原則

最新版本的 Microsoft Edge WebView2 包含下列原則。 您可以使用這些原則來設定 Microsoft Edge WebView2 在組織中的執行方式。

如需用於控制 Microsoft Edge WebView2 更新方式和更新時機的一組額外原則之詳細資訊，請參閱 [Microsoft Edge 更新原則參考](microsoft-edge-update-policies.md)。


> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

## <a name="available-policies"></a>可用原則

下表列出此版本 Microsoft Edge WebView2 提供的所有群組原則。 使用下表中的連結，深入了解特定原則。

- [載入程式重寫設定](#loader-override-settings)


### [*<a name="loader-override-settings"></a>載入程式重寫設定*](#loader-override-settings-policies)

|原則名稱|標題|
|-|-|
|[BrowserExecutableFolder](#browserexecutablefolder)|設定 [瀏覽器可執行檔] 資料夾的位置|
|[ReleaseChannelPreference](#releasechannelpreference)|設定發行通道的 [搜尋順序] 喜好設定|




  ## <a name="loader-override-settings-policies"></a>載入程式重寫設定原則

  [回到頁首](#microsoft-edge-webview2---policies)

  ### <a name="browserexecutablefolder"></a>BrowserExecutableFolder

  #### <a name="configure-the-location-of-the-browser-executable-folder"></a>設定 [瀏覽器可執行檔] 資料夾的位置

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  這項原則會在指定路徑中，將 WebView2 應用程式設定為使用 WebView2 Runtime。 該資料夾應包含下列檔案：msedgewebview2.exe、msedge.dll 等等。

若要設定資料夾路徑的值，請提供值名稱和值配對。 將 [值名稱] 設定為 [應用程式使用者模型識別碼] 或 [可執行檔名]。 您可以使用萬用字元「*」作為值名稱來套用到所有應用程式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：BrowserExecutableFolder
  - GP 名稱：設定 [瀏覽器可執行檔] 資料夾的位置
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge WebView2/載入程式重寫設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder
  - 路徑 (建議)：不適用
  - 值名稱：REG_SZ 的清單
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder = "Name: *, Value: C:\\Program Files\\Microsoft Edge WebView2 Runtime Redistributable 85.0.541.0 x64"

```

  

  [回到頁首](#microsoft-edge-webview2---policies)

  ### <a name="releasechannelpreference"></a>ReleaseChannelPreference

  #### <a name="set-the-release-channel-search-order-preference"></a>設定發行通道的 [搜尋順序] 喜好設定

  
  
  #### <a name="supported-versions"></a>支援的版本：

  - Windows 上，版本 87 或更新版本

  #### <a name="description"></a>描述

  預設通道搜尋順序為 WebView2 Runtime、Beta、Dev 和 Canary。

若要顛倒預設的搜尋順序，請將此原則設定為 1。

若要設定發行通道喜好設定的值，請提供值名稱和值配對。 將 [值名稱] 設定為 [應用程式使用者模型識別碼] 或 [可執行檔名]。 您可以使用萬用字元「*」作為值名稱來套用到所有應用程式。

  #### <a name="supported-features"></a>支援的功能：

  - 可強制執行：是
  - 可以建議：否
  - 動態原則重新整理：是

  #### <a name="data-type"></a>資料類型：

  - 字串清單

  #### <a name="windows-information-and-settings"></a>Windows 資訊和設定

  ##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊

  - GP 唯一名稱：ReleaseChannelPreference
  - GP 名稱：設定發行通道的 [搜尋順序] 喜好設定
  - GP 路徑 (強制)：系統管理範本/Microsoft Edge WebView2/載入程式重寫設定
  - GP 路徑 (建議)：不適用
  - GP ADMX 檔案名稱：MSEdgeWebView2.admx

  ##### <a name="windows-registry-settings"></a>Windows 登錄設定

  - 路徑 (強制)：SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference
  - 路徑 (建議)：不適用
  - 值名稱：REG_SZ 的清單
  - 數值類型：REG_SZ 的清單

  ##### <a name="example-value"></a>範例值：

```
SOFTWARE\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference = "Name: *, Value: 1"

```

  

  [回到頁首](#microsoft-edge-webview2---policies)


## <a name="see-also"></a>請參閱

- [設定 Microsoft Edge](configure-microsoft-edge.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft 安全性基準部落格](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/bg-p/Microsoft-Security-Baselines)