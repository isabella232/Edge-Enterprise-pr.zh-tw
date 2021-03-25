---
title: IE 模式中可設定的網站和 Microsoft Edge
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/28/2020
audience: ITPro
ms.topic: procedural
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: IE 模式中可設定的網站和 Microsoft Edge
ms.openlocfilehash: 1bffdef8c88b7a83d999b29763fcca258102ed51
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447327"
---
# <a name="learn-about-configurable-sites-in-ie-mode"></a><span data-ttu-id="f60b2-103">深入了解 IE 模式中可設定的網站</span><span class="sxs-lookup"><span data-stu-id="f60b2-103">Learn about Configurable sites in IE mode</span></span>

<span data-ttu-id="f60b2-104">本文說明了在 Microsoft Edge 中使用 IE 模式時，企業模式網站清單的 [可設定網站] 功能。</span><span class="sxs-lookup"><span data-stu-id="f60b2-104">This article explains the Configurable sites feature of the Enterprise Mode Site List when using IE mode in Microsoft Edge.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f60b2-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="f60b2-105">Prerequisites</span></span>

- <span data-ttu-id="f60b2-106">Windows 更新</span><span class="sxs-lookup"><span data-stu-id="f60b2-106">Windows updates</span></span>

  - <span data-ttu-id="f60b2-107">Windows 10 版本 1909、Windows Server 版本 1909– KB4550945  或更高版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-107">Windows 10 version 1909, Windows server version 1909 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f60b2-108">Windows 10 版本 1903、Windows Server 版本 1903– KB4550945  或更高版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-108">Windows 10 version 1903, Windows server version 1903 – KB4550945  or higher</span></span>
  - <span data-ttu-id="f60b2-109">Windows 10 版本 1809、Windows Server 版本 1809 和 Windows Server 2019：KB4550969 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-109">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4550969 or higher</span></span>
  - <span data-ttu-id="f60b2-110">Windows 10 版本 1803-KB4550944 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-110">Windows 10 version 1803 – KB4550944 or higher</span></span>
  - <span data-ttu-id="f60b2-111">Windows 10 版本1607、Windows Server 2016-KB4556826 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-111">Windows 10 version 1607, Windows Server 2016 - KB4556826 or higher</span></span>
  - <span data-ttu-id="f60b2-112">Windows 10 初始版 (2015 年 7 月 - KB4550947 或更新版本)</span><span class="sxs-lookup"><span data-stu-id="f60b2-112">Windows 10 initial version, July 2015 - KB4550947 or higher</span></span>
  - <span data-ttu-id="f60b2-113">Windows 8.1 – KB4556798 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-113">Windows 8.1 – KB4556798 or higher</span></span>

- <span data-ttu-id="f60b2-114">Microsoft Edge 版本 83 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f60b2-114">Microsoft Edge version 83 or later</span></span>
- <span data-ttu-id="f60b2-115">[IE 模式](./edge-ie-mode.md)使用企業模式網站清單設定</span><span class="sxs-lookup"><span data-stu-id="f60b2-115">[IE mode](./edge-ie-mode.md) configured with Enterprise Mode Site List</span></span>

## <a name="overview"></a><span data-ttu-id="f60b2-116">概觀</span><span class="sxs-lookup"><span data-stu-id="f60b2-116">Overview</span></span>

<span data-ttu-id="f60b2-117">在企業模式網站清單中設定 IE 模式的網站，適用于大部分舊版應用程式的環境。</span><span class="sxs-lookup"><span data-stu-id="f60b2-117">Configuring sites needing IE mode in the Enterprise Mode Site List will work well for most environments with legacy applications.</span></span> <span data-ttu-id="f60b2-118">但在某些情况下，如果不在 IE 模式中轉譯整個網域，那麼此方法不適合在 IE 模式中設定開啟網站子集。</span><span class="sxs-lookup"><span data-stu-id="f60b2-118">However, in some cases this approach isn't the best to configure a subset of sites to open in IE mode without rendering an entire domain in IE mode.</span></span> <span data-ttu-id="f60b2-119">例如，當您的環境同時包含在單個服務器上運行的新版和舊版應用程式時，且您希望能夠靈活地在 IE 模式下僅轉譯舊版應用程式，而在 Microsoft Edge 模式下轉譯其餘應用程式。</span><span class="sxs-lookup"><span data-stu-id="f60b2-119">For example, when your environment contains both modern and legacy applications running on a single server and you would like the flexibility to render only the legacy applications in IE mode and the remaining applications to render in Microsoft Edge mode.</span></span>

<span data-ttu-id="f60b2-120">解決方法是使用企業模式網站清單的 [可設定網站] 功能。</span><span class="sxs-lookup"><span data-stu-id="f60b2-120">The solution is to use the Configurable sites feature of the Enterprise Mode Site List.</span></span> <span data-ttu-id="f60b2-121">啟用此功能後，Microsoft Edge 將會允許具有「可配置」標記的網站參與 IE 模式引擎判斷。</span><span class="sxs-lookup"><span data-stu-id="f60b2-121">When the feature is enabled, Microsoft Edge will allow sites with the "configurable" tag to participate in IE mode engine determination.</span></span>

## <a name="how-configurable-sites-works"></a><span data-ttu-id="f60b2-122">[可設定網站] 的運作方式</span><span class="sxs-lookup"><span data-stu-id="f60b2-122">How Configurable sites works</span></span>

### <a name="automatic-switching-from-the-microsoft-edge-engine-to-the-ie-mode-engine"></a><span data-ttu-id="f60b2-123">從 Microsoft Edge 引擎自動切換到 IE 模式引擎</span><span class="sxs-lookup"><span data-stu-id="f60b2-123">Automatic switching from the Microsoft Edge engine to the IE mode engine</span></span>

<span data-ttu-id="f60b2-124">若要使用 [可設定網站] 功能，將需要企業模式網站清單中的一或多個網站，以具有`<open-in>Configurable</open-in>`選項。</span><span class="sxs-lookup"><span data-stu-id="f60b2-124">To use the Configurable sites feature, you'll need one or more sites in the Enterprise Mode Site List to have the `<open-in>Configurable</open-in>` option.</span></span>

<span data-ttu-id="f60b2-125">範例：</span><span class="sxs-lookup"><span data-stu-id="f60b2-125">Example:</span></span>

```
<site-list version="1">
  <site url="app.com">
    <open-in>Configurable</open-in>
  </site>
</site-list>
```

<span data-ttu-id="f60b2-126">啟用 [可設定網站] 功能時，會發生下列行為：</span><span class="sxs-lookup"><span data-stu-id="f60b2-126">When the Configurable sites feature is enabled, the following behavior occurs:</span></span>

1. <span data-ttu-id="f60b2-127">當對可設定的網站發出要求時，Microsoft Edge 會傳送 HTTP 要求標頭 “`X-InternetExplorerModeConfigurable: 1`”。</span><span class="sxs-lookup"><span data-stu-id="f60b2-127">When making a request to a Configurable site, Microsoft Edge will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`".</span></span>
2. <span data-ttu-id="f60b2-128">可設定的網站可能會傳送具有 HTTP 回應標頭 “`X-InternetExplorerMode: 1`”的重新導向回應（例如 HTTP 302） ，以要求 Microsoft Edge 在 IE 模式載入網站。</span><span class="sxs-lookup"><span data-stu-id="f60b2-128">A Configurable site may send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 1`" to request that Microsoft Edge loads the site in IE mode.</span></span>
3. <span data-ttu-id="f60b2-129">重新導向的目標（即位置**回應**標頭的值）也必須是**可設定**的或**中立**的網站，否則 IE 模式回應標頭將被忽略。</span><span class="sxs-lookup"><span data-stu-id="f60b2-129">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f60b2-130">因此重新導向的目標通常與原始的 URL 相同。</span><span class="sxs-lookup"><span data-stu-id="f60b2-130">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f60b2-131">但也不是必須如此。</span><span class="sxs-lookup"><span data-stu-id="f60b2-131">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f60b2-132">重新導向回應可根據 Microsoft Edge 重新導向的一般 HTTP 快取行為進行快取。</span><span class="sxs-lookup"><span data-stu-id="f60b2-132">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

### <a name="switching-back-from-ie-mode-engine-to-microsoft-edge-engine"></a><span data-ttu-id="f60b2-133">從 IE 模式引擎切換回 Microsoft Edge 引擎</span><span class="sxs-lookup"><span data-stu-id="f60b2-133">Switching back from IE mode engine to Microsoft Edge engine</span></span>

<span data-ttu-id="f60b2-134">啟用 Microsoft Edge 中 [可設定網站] 會自動啟用 IE 模式索引標籤中的下列行為：</span><span class="sxs-lookup"><span data-stu-id="f60b2-134">Enabling Configurable sites in Microsoft Edge automatically enables the following behaviors in IE mode tabs:</span></span>

1. <span data-ttu-id="f60b2-135">當對可設定的網站發出要求時，IE 模式索引標籤會傳送 HTTP 要求標頭 “`X-InternetExplorerModeConfigurable: 1`”，與 Microsoft Edge 索引標籤相同。</span><span class="sxs-lookup"><span data-stu-id="f60b2-135">When making a request to a Configurable site, IE mode tabs will send the HTTP request header "`X-InternetExplorerModeConfigurable: 1`", the same as Microsoft Edge tabs.</span></span>
2. <span data-ttu-id="f60b2-136">可設定的網站可能會傳送具有 HTTP 回應標頭 “`X-InternetExplorerMode: 0`”的重新導向回應（例如 HTTP 302） ，以要求導航切換回 Microsoft Edge 模式。</span><span class="sxs-lookup"><span data-stu-id="f60b2-136">A Configurable site might send a redirect response (for example, HTTP 302) with the HTTP response header "`X-InternetExplorerMode: 0`" to request that the navigation switch back to Microsoft Edge mode.</span></span>
3. <span data-ttu-id="f60b2-137">重新導向的目標（即位置**回應**標頭的值）也必須是**可設定**的或**中立**的網站，否則 IE 模式回應標頭將被忽略。</span><span class="sxs-lookup"><span data-stu-id="f60b2-137">The target of the redirect (that is, the value of the **Location** response header) must also be a **Configurable** or **Neutral** site, otherwise the IE mode response header will be ignored.</span></span> <span data-ttu-id="f60b2-138">因此重新導向的目標通常與原始的 URL 相同。</span><span class="sxs-lookup"><span data-stu-id="f60b2-138">It's expected that the target of the redirect will usually be the same as the original URL.</span></span> <span data-ttu-id="f60b2-139">但也不是必須如此。</span><span class="sxs-lookup"><span data-stu-id="f60b2-139">However, it doesn't have to be.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f60b2-140">重新導向回應可根據 Microsoft Edge 重新導向的一般 HTTP 快取行為進行快取。</span><span class="sxs-lookup"><span data-stu-id="f60b2-140">The redirect response is subject to caching according to Microsoft Edge's normal HTTP caching behavior for redirects.</span></span>

> [!TIP]
> <span data-ttu-id="f60b2-141">兩個瀏覽器引擎都將傳送相同的「`X-InternetExplorerModeConfigurable: 1`」要求標頭到可設定的網站。</span><span class="sxs-lookup"><span data-stu-id="f60b2-141">Both browser engines send the same "`X-InternetExplorerModeConfigurable: 1`" request header to Configurable sites.</span></span> <span data-ttu-id="f60b2-142">您應該使用 [使用者-代理] 要求標頭來區分來自 Microsoft Edge 模式與 IE 模式的要求，以避免當網站已載入到正確的引擎中時進行重新導向。</span><span class="sxs-lookup"><span data-stu-id="f60b2-142">You should use the User-Agent request header to distinguish between requests from Microsoft Edge mode vs. IE mode to avoid redirecting when the site is already loading in the correct engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="f60b2-143">請參閱</span><span class="sxs-lookup"><span data-stu-id="f60b2-143">See also</span></span>

- [<span data-ttu-id="f60b2-144">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="f60b2-144">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="f60b2-145">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="f60b2-145">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="f60b2-146">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f60b2-146">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)