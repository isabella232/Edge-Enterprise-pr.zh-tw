---
title: Microsoft Edge Proxy 設定
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: '使用命令列選項來設定 Proxy 設定 '
ms.openlocfilehash: d10002e5595836976a33a1b70743fe78b7987f00725546d3aae9c241d661c6eb
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724396"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a>如何使用 Microsoft Edge 命令列選項來設定 Proxy 設定

本文介紹如何使用命令列選項來覆寫預設系統網路設定。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="system-network-settings"></a>系統網路設定

預設情況下，Microsoft Edge 網路堆疊使用系統網路設定。 這些設定包括 *Proxy 設定*以及*憑證和私密金鑰存放區*。

在某些情況下，使用者會要求使用系統預設 Proxy 設定的替代方法。 為了支援這些方案，Microsoft Edge 支援可用於設定自訂 Proxy 設定的命令列選項。

這些命令列選項對應至 **Proxy 伺服器**群組中的以下原則：

- [ProxyBypassList](./microsoft-edge-policies.md#proxybypasslist)
- [ProxyMode](./microsoft-edge-policies.md#proxymode)
- [ProxyPacUrl](./microsoft-edge-policies.md#proxypacurl)
- [ProxyServer](./microsoft-edge-policies.md#proxyserver)
- [ProxySettings](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a>Proxy 設定的命令列選項

Microsoft Edge 支援以下與 Proxy 相關的命令列選項。

 **`--no-proxy-server`**
 
告訴 Microsoft Edge 不要使用 Proxy ，即使系統設定為使用 Proxy 也是如此。 它會覆寫所提供的任何其他 Proxy 設定。

**`--proxy-auto-detect`**

告訴 Microsoft Edge 嘗試並自動偵測您的 Proxy 設定。 如果設定了 `--proxy-server`，則忽略此引數。

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

告訴 Microsoft Edge 使用自訂 Proxy 設定。 您可以透過三種方式指定自訂 Proxy 設定。

1. 提供列出配置到 URL/連接埠配對的分號分隔對應清單。 例如，`--proxy-server="http=proxy1:8080;ftp=ftpproxy"` 告訴 Microsoft Edge 對 http URL 使用 HTTP Proxy "proxy1:8080"，對 ftp URL 使用 HTTP Proxy "ftpproxy:80"。
2. 透過提供具有選用連接埠的單一 URI，適用於所有 URL。 例如，`--proxy-server="proxy2:8080"` 將 "proxy2:8080" 的 Proxy 用於所有流量。
3. 透過使用特殊的 "direct://" 值。 例如，`--proxy-server="direct://"` 將使所有連線不使用 Proxy。 

>[!NOTE]
>您可以將 Microsoft Edge 設定為嘗試使用 Proxy ，如果 Proxy 不可用，則遞補為直接連線。 例如，`--proxy-server="http://proxy2:8080,direct://`。

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

告訴 Microsoft Edge 繞過指定分號分隔主機清單的任何指定 Proxy。 此旗標必須搭配 `--proxy-server` 使用。

>[!NOTE]
>後置網域比對不需要 "." 分隔符號，"\*microsoft.com" 會符合 "imicrosoft.com"。 例如，`--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` 將在連接埠 8080 上對所有主機使用 Proxy 伺服器 "proxy2"，但連接埠 8080 上的 \*.microsoft.com、example.com 和 127.0.0.1 請求除外。 在前面的範例中，imicrosoft.com 請求仍將以 Proxy 處理。 但是，iexample.com 請求將繞過 Proxy，因為指定了 \*example.com 而不是 \*.example.com。

**`--proxy-pac-url=<pac-file-url>`**

告訴 Microsoft Edge 在指定的 URL 使用 PAC 檔案。 例如，`--proxy-pac-url="https://wpad/proxy.pac"` 會告知 Microsoft Edge 使用 **proxy.pac** 檔案解析 URL 請求的 Proxy 資訊。

## <a name="content-license"></a>內容授權

> [!NOTE]
> 本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。 原始頁面可在[此處](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett)找到。
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。

## <a name="see-also"></a>請參閱

- 若要查看進階組態設定和其他選項，請參閱 Chromium 開放原始碼專案中的 [Proxy 文件](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md)。
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)