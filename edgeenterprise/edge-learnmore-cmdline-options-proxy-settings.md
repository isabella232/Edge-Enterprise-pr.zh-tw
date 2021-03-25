---
title: Microsoft Edge Proxy 設定
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '使用命令列選項來設定 Proxy 設定 '
ms.openlocfilehash: d0924f723aab6832e5b4eb70c60e1d329d3c7a9d
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447637"
---
# <a name="how-to-use-microsoft-edge-command-line-options-to-configure-proxy-settings"></a><span data-ttu-id="da711-103">如何使用 Microsoft Edge 命令列選項來設定 Proxy 設定</span><span class="sxs-lookup"><span data-stu-id="da711-103">How to use Microsoft Edge command-line options to configure proxy settings</span></span>

<span data-ttu-id="da711-104">本文介紹如何使用命令列選項來覆寫預設系統網路設定。</span><span class="sxs-lookup"><span data-stu-id="da711-104">This article describes how you can use command-line options to override the default system network settings.</span></span>

>[!NOTE]
><span data-ttu-id="da711-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="da711-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="system-network-settings"></a><span data-ttu-id="da711-106">系統網路設定</span><span class="sxs-lookup"><span data-stu-id="da711-106">System network settings</span></span>

<span data-ttu-id="da711-107">預設情況下，Microsoft Edge 網路堆疊使用系統網路設定。</span><span class="sxs-lookup"><span data-stu-id="da711-107">The Microsoft Edge network stack uses the system network settings by default.</span></span> <span data-ttu-id="da711-108">這些設定包括 *Proxy 設定*以及*憑證和私密金鑰存放區*。</span><span class="sxs-lookup"><span data-stu-id="da711-108">These settings include *proxy settings*, and *certificate and private key stores*.</span></span>

<span data-ttu-id="da711-109">在某些情況下，使用者會要求使用系統預設 Proxy 設定的替代方法。</span><span class="sxs-lookup"><span data-stu-id="da711-109">There are scenarios where users request an alternative to using the system's default proxy settings.</span></span> <span data-ttu-id="da711-110">為了支援這些方案，Microsoft Edge 支援可用於設定自訂 Proxy 設定的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="da711-110">To support these scenarios, Microsoft Edge supports command-line options that you can use to configure custom proxy settings.</span></span>

<span data-ttu-id="da711-111">這些命令列選項對應至 **Proxy 伺服器**群組中的以下原則：</span><span class="sxs-lookup"><span data-stu-id="da711-111">These command-line options correspond to the following policies in the **Proxy server** group:</span></span>

- [<span data-ttu-id="da711-112">ProxyBypassList</span><span class="sxs-lookup"><span data-stu-id="da711-112">ProxyBypassList</span></span>](./microsoft-edge-policies.md#proxybypasslist)
- [<span data-ttu-id="da711-113">ProxyMode</span><span class="sxs-lookup"><span data-stu-id="da711-113">ProxyMode</span></span>](./microsoft-edge-policies.md#proxymode)
- [<span data-ttu-id="da711-114">ProxyPacUrl</span><span class="sxs-lookup"><span data-stu-id="da711-114">ProxyPacUrl</span></span>](./microsoft-edge-policies.md#proxypacurl)
- [<span data-ttu-id="da711-115">ProxyServer</span><span class="sxs-lookup"><span data-stu-id="da711-115">ProxyServer</span></span>](./microsoft-edge-policies.md#proxyserver)
- [<span data-ttu-id="da711-116">ProxySettings</span><span class="sxs-lookup"><span data-stu-id="da711-116">ProxySettings</span></span>](./microsoft-edge-policies.md#proxysettings)

## <a name="command-line-options-for-proxy-settings"></a><span data-ttu-id="da711-117">Proxy 設定的命令列選項</span><span class="sxs-lookup"><span data-stu-id="da711-117">Command-line options for proxy settings</span></span>

<span data-ttu-id="da711-118">Microsoft Edge 支援以下與 Proxy 相關的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="da711-118">Microsoft Edge supports the following proxy-related command-line options.</span></span>

 **`--no-proxy-server`**
 
<span data-ttu-id="da711-119">告訴 Microsoft Edge 不要使用 Proxy ，即使系統設定為使用 Proxy 也是如此。</span><span class="sxs-lookup"><span data-stu-id="da711-119">Tells Microsoft Edge not to use a Proxy, even if the system is otherwise configured to use one.</span></span> <span data-ttu-id="da711-120">它會覆寫所提供的任何其他 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="da711-120">It overrides any other proxy settings that are provided.</span></span>

**`--proxy-auto-detect`**

<span data-ttu-id="da711-121">告訴 Microsoft Edge 嘗試並自動偵測您的 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="da711-121">Tells Microsoft Edge to try and automatically detect your proxy configuration.</span></span> <span data-ttu-id="da711-122">如果設定了 `--proxy-server`，則忽略此引數。</span><span class="sxs-lookup"><span data-stu-id="da711-122">This argument is ignored if `--proxy-server` is configured.</span></span>

**`--proxy-server=<scheme>=<uri>[:<port>][;...] | <uri>[:<port>] | "direct://"`**

<span data-ttu-id="da711-123">告訴 Microsoft Edge 使用自訂 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="da711-123">Tells Microsoft Edge to use a custom proxy configuration.</span></span> <span data-ttu-id="da711-124">您可以透過三種方式指定自訂 Proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="da711-124">You can specify a custom proxy configuration in three ways.</span></span>

1. <span data-ttu-id="da711-125">提供列出配置到 URL/連接埠配對的分號分隔對應清單。</span><span class="sxs-lookup"><span data-stu-id="da711-125">Provide a semicolon-separated mapping of list scheme to url/port pairs.</span></span> <span data-ttu-id="da711-126">例如，`--proxy-server="http=proxy1:8080;ftp=ftpproxy"` 告訴 Microsoft Edge 對 http URL 使用 HTTP Proxy "proxy1:8080"，對 ftp URL 使用 HTTP Proxy "ftpproxy:80"。</span><span class="sxs-lookup"><span data-stu-id="da711-126">For example, `--proxy-server="http=proxy1:8080;ftp=ftpproxy"` tells Microsoft Edge to use HTTP proxy "proxy1:8080" for http URLs and HTTP proxy "ftpproxy:80" for ftp URLs.</span></span>
2. <span data-ttu-id="da711-127">透過提供具有選用連接埠的單一 URI，適用於所有 URL。</span><span class="sxs-lookup"><span data-stu-id="da711-127">By providing a single uri with optional port to use for all URLs.</span></span> <span data-ttu-id="da711-128">例如，`--proxy-server="proxy2:8080"` 將 "proxy2:8080" 的 Proxy 用於所有流量。</span><span class="sxs-lookup"><span data-stu-id="da711-128">For example, `--proxy-server="proxy2:8080"` will use the proxy at "proxy2:8080" for all traffic.</span></span>
3. <span data-ttu-id="da711-129">透過使用特殊的 "direct://" 值。</span><span class="sxs-lookup"><span data-stu-id="da711-129">By using the special "direct://" value.</span></span> <span data-ttu-id="da711-130">例如，`--proxy-server="direct://"` 將使所有連線不使用 Proxy。</span><span class="sxs-lookup"><span data-stu-id="da711-130">For example, `--proxy-server="direct://"` will make all connections not use a proxy.</span></span> 

>[!NOTE]
><span data-ttu-id="da711-131">您可以將 Microsoft Edge 設定為嘗試使用 Proxy ，如果 Proxy 不可用，則遞補為直接連線。</span><span class="sxs-lookup"><span data-stu-id="da711-131">You can configure Microsoft Edge to try using a proxy and fallback to going direct if the proxy isn't available.</span></span> <span data-ttu-id="da711-132">例如，`--proxy-server="http://proxy2:8080,direct://`。</span><span class="sxs-lookup"><span data-stu-id="da711-132">For example, `--proxy-server="http://proxy2:8080,direct://`.</span></span>

**`--proxy-bypass-list=(<trailing_domain>|<ip-address>)[:<port>][;...]`**

<span data-ttu-id="da711-133">告訴 Microsoft Edge 繞過指定分號分隔主機清單的任何指定 Proxy。</span><span class="sxs-lookup"><span data-stu-id="da711-133">Tells Microsoft Edge to bypass any specified proxy for the specified semicolon-separated list of hosts.</span></span> <span data-ttu-id="da711-134">此旗標必須搭配 `--proxy-server` 使用。</span><span class="sxs-lookup"><span data-stu-id="da711-134">This flag must be used with `--proxy-server`.</span></span>

>[!NOTE]
><span data-ttu-id="da711-135">後置網域比對不需要 "." 分隔符號，"\*microsoft.com" 會符合 "imicrosoft.com"。</span><span class="sxs-lookup"><span data-stu-id="da711-135">Trailing-domain matching doesn't require "." separators, "\*microsoft.com" will match "imicrosoft.com".</span></span> <span data-ttu-id="da711-136">例如，`--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` 將在連接埠 8080 上對所有主機使用 Proxy 伺服器 "proxy2"，但連接埠 8080 上的 \*.microsoft.com、example.com 和 127.0.0.1 請求除外。</span><span class="sxs-lookup"><span data-stu-id="da711-136">For example, `--proxy-server="proxy2:8080" --proxy-bypass-list="*.microsoft.com;*example.com;127.0.0.1:8080"` will use the proxy server "proxy2" on port 8080 for all hosts except requests for \*.microsoft.com, example.com, and 127.0.0.1 on port 8080.</span></span> <span data-ttu-id="da711-137">在前面的範例中，imicrosoft.com 請求仍將以 Proxy 處理。</span><span class="sxs-lookup"><span data-stu-id="da711-137">In the previous example, imicrosoft.com requests will still be proxied.</span></span> <span data-ttu-id="da711-138">但是，iexample.com 請求將繞過 Proxy，因為指定了 \*example.com 而不是 \*.example.com。</span><span class="sxs-lookup"><span data-stu-id="da711-138">However, iexample.com requests will bypass the proxy because \*example.com was specified instead of \*.example.com.</span></span>

**`--proxy-pac-url=<pac-file-url>`**

<span data-ttu-id="da711-139">告訴 Microsoft Edge 在指定的 URL 使用 PAC 檔案。</span><span class="sxs-lookup"><span data-stu-id="da711-139">Tells Microsoft Edge to use the PAC file at the specified URL.</span></span> <span data-ttu-id="da711-140">例如，`--proxy-pac-url="https://wpad/proxy.pac"` 會告知 Microsoft Edge 使用 **proxy.pac** 檔案解析 URL 請求的 Proxy 資訊。</span><span class="sxs-lookup"><span data-stu-id="da711-140">For example, `--proxy-pac-url="https://wpad/proxy.pac"` tells Microsoft Edge to resolve proxy information for URL requests using the **proxy.pac** file.</span></span>

## <a name="content-license"></a><span data-ttu-id="da711-141">內容授權</span><span class="sxs-lookup"><span data-stu-id="da711-141">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="da711-142">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="da711-142">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="da711-143">原始頁面可在[此處](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett)找到。</span><span class="sxs-lookup"><span data-stu-id="da711-143">The original page can be found [here](https://www.chromium.org/developers/design-documents/network-settings#TOC-Command-line-options-for-proxy-sett).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="da711-144">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="da711-144">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="da711-145">請參閱</span><span class="sxs-lookup"><span data-stu-id="da711-145">See also</span></span>

- <span data-ttu-id="da711-146">若要查看進階組態設定和其他選項，請參閱 Chromium 開放原始碼專案中的 [Proxy 文件](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md)。</span><span class="sxs-lookup"><span data-stu-id="da711-146">To see advanced configuration settings and additional options, consult the [proxy documentation](https://chromium.googlesource.com/chromium/src/+/HEAD/net/docs/proxy.md) in the Chromium Open Source project.</span></span>
- [<span data-ttu-id="da711-147">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="da711-147">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)