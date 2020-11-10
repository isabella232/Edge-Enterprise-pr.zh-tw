---
title: 從 Microsoft Edge 到 Internet Explorer 共用 Cookie
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 11/05/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '如何從 Microsoft Edge 到 Internet Explorer 共用 Cookie '
ms.openlocfilehash: 5740a4ce31a240573b9106e7a20a5c44688aca0a
ms.sourcegitcommit: 2024629929044e2dcf146674058c1d6312c32e9a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "11157537"
---
# <span data-ttu-id="9361a-103">從 Microsoft Edge 到 Internet Explorer 共用 Cookie</span><span class="sxs-lookup"><span data-stu-id="9361a-103">Cookie sharing from Microsoft Edge to Internet Explorer</span></span>

<span data-ttu-id="9361a-104">本文說明如何在使用 Internet Explorer 模式的同時，將工作階段 Cookie 設置為從 Microsoft Edge 程式共用到 Internet Explorer 程式。</span><span class="sxs-lookup"><span data-stu-id="9361a-104">This article explains explains how to configure session cookie sharing from a Microsoft Edge process to Internet Explorer process, while using Internet Explorer mode.</span></span>

> [!NOTE]
> <span data-ttu-id="9361a-105">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9361a-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="9361a-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="9361a-106">Prerequisites</span></span>

- <span data-ttu-id="9361a-107">Windows 更新</span><span class="sxs-lookup"><span data-stu-id="9361a-107">Windows updates</span></span>

  - <span data-ttu-id="9361a-108">Windows 10 版本 2004、Windows Server 版本 2004－KB4571744 或更高版本</span><span class="sxs-lookup"><span data-stu-id="9361a-108">Windows 10 version 2004, Windows server version 2004 - KB4571744 or higher</span></span>
  - <span data-ttu-id="9361a-109">Windows 10 版本 1909、Windows Server 版本 1909－KB4566116 或更高版本</span><span class="sxs-lookup"><span data-stu-id="9361a-109">Windows 10 version 1909, Windows server version 1909 – KB4566116 or higher</span></span>
  - <span data-ttu-id="9361a-110">Windows 10 版本 1903、Windows Server 版本 1903－KB4566116 或更高版本</span><span class="sxs-lookup"><span data-stu-id="9361a-110">Windows 10 version 1903, Windows server version 1903 – KB4566116 or higher</span></span>
  - <span data-ttu-id="9361a-111">Windows 10 版本 1809、Windows Server 版本 1809 和 Windows Server 2019－KB4571748 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9361a-111">Windows 10 version 1809, Windows Server version 1809, and Windows Server 2019 - KB4571748 or higher</span></span>
  - <span data-ttu-id="9361a-112">Windows 10 版本 1803－KB4577032 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9361a-112">Windows 10 version 1803 – KB4577032 or higher</span></span>

- <span data-ttu-id="9361a-113">Microsoft Edge 版本 87 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9361a-113">Microsoft Edge version 87 or later</span></span>
- <span data-ttu-id="9361a-114">使用企業模式網站清單設定 [IE 模式](https://aka.ms/iemodeonedge) </span><span class="sxs-lookup"><span data-stu-id="9361a-114">[IE mode](https://aka.ms/iemodeonedge) configured with Enterprise Mode Site List</span></span>

## <span data-ttu-id="9361a-115">概觀</span><span class="sxs-lookup"><span data-stu-id="9361a-115">Overview</span></span>

<span data-ttu-id="9361a-116">大型組織中的一般設定，是讓應用程式能夠在新式瀏覽器上使用，以連結到另一個應用程式，而這個應用程式可能設定為在工作流程中啟用單一登入（SSO）的 Internet Explorer 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="9361a-116">A common configuration in large organizations is to have an application that works on a modern browser link to another application, which might be configured to open in Internet Explorer mode with Single Sign On (SSO) enabled as part of the workflow.</span></span>

<span data-ttu-id="9361a-117">根據預設，Microsoft Edge 和 Internet Explorer 程式無法共用工作階段 cookie，在某些情況下可能會帶來不便。</span><span class="sxs-lookup"><span data-stu-id="9361a-117">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this can be inconvenient in some cases.</span></span> <span data-ttu-id="9361a-118">例如，當使用者必須在 Internet Explorer 模式中重新驗證，或登出 Microsoft Edge 工作階段時，使用者並不會登出 Internet Explorer 模式工作階段。</span><span class="sxs-lookup"><span data-stu-id="9361a-118">For example, when a user has to re-authenticate in Internet Explorer mode or when signing out of an Microsoft Edge session doesn’t sign out of the Internet Explorer mode session.</span></span> <span data-ttu-id="9361a-119">在這些情況下，您可以將由 SSO 設置的特定 cookie 設置為從 Microsoft Edge 傳送到 Internet Explorer，驗證操作程序就會因消除了重新驗證的需要而變得更加流暢。</span><span class="sxs-lookup"><span data-stu-id="9361a-119">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to re-authenticate.</span></span>

> [!NOTE]
> <span data-ttu-id="9361a-120">工作階段 cookie 只能從 Microsoft Edge 共用到 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="9361a-120">Session cookies can only be shared from Microsoft Edge to Internet Explorer.</span></span> <span data-ttu-id="9361a-121">反向式共用工作階段 cookie 是不可行的（從 Internet Explorer 到 Microsoft Edge）。</span><span class="sxs-lookup"><span data-stu-id="9361a-121">Sharing session cookies in reverse (from Internet Explorer to Microsoft Edge) isn't possible.</span></span>

## <span data-ttu-id="9361a-122">Cookies 共用的運作方式</span><span class="sxs-lookup"><span data-stu-id="9361a-122">How cookie sharing works</span></span>

<span data-ttu-id="9361a-123">已將企業模式網站清單 XML 延展，以允許其他元素指定需要從 Microsoft Edge 工作模式與 Internet Explorer 共用的 cookie。</span><span class="sxs-lookup"><span data-stu-id="9361a-123">The Enterprise Mode site list XML has been extended to allow additional elements to specify cookies that need to be shared from a Microsoft Edge session with Internet Explorer.</span></span>  

<span data-ttu-id="9361a-124">在 Microsoft Edge 工作模式中，第一次建立 Internet Explorer 模式索引標籤時，所有相符的 cookie 都會共用至 Internet Explorer 工作模式。</span><span class="sxs-lookup"><span data-stu-id="9361a-124">The first time an Internet Explorer mode tab is created in a Microsoft Edge session, all matching cookies are shared to the Internet Explorer session.</span></span> <span data-ttu-id="9361a-125">之後，只要新增、刪除或修改符合規則的 cookie，系統就會將其新增為 Internet Explorer 工作模式的更新。</span><span class="sxs-lookup"><span data-stu-id="9361a-125">Subsequently, any time a cookie that matches a rule is added, deleted, or modified it is sent as an update to the Internet Explorer session.</span></span> <span data-ttu-id="9361a-126">當網站清單更新時，也會重新評估該共用 cookie 集合。</span><span class="sxs-lookup"><span data-stu-id="9361a-126">The set of shared cookies is also re-evaluated when the site list is updated.</span></span>

### <span data-ttu-id="9361a-127">更新的結構描述元素</span><span class="sxs-lookup"><span data-stu-id="9361a-127">Updated schema elements</span></span>

<span data-ttu-id="9361a-128">下表說明為了支援 cookie 共用功能而新增的 \<shared-cookie\> 元素。</span><span class="sxs-lookup"><span data-stu-id="9361a-128">The following table describes the \<shared-cookie\> element added to support the cookie sharing feature.</span></span>

| <span data-ttu-id="9361a-129">元素</span><span class="sxs-lookup"><span data-stu-id="9361a-129">Element</span></span>| <span data-ttu-id="9361a-130">描述</span><span class="sxs-lookup"><span data-stu-id="9361a-130">Description</span></span> |
|-|-|
| \<shared-cookie **domain**=".contoso.com" **name**="cookie1"\>\</shared-cookie\><br><br><span data-ttu-id="9361a-131">或</span><span class="sxs-lookup"><span data-stu-id="9361a-131">OR</span></span><br><br>\<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2"\>\</shared-cookie\>   |<span data-ttu-id="9361a-132">**（必要）** 一個 \<shared-cookie\>元素至少需要一個 *網域*（適用於網域 cookie）或一個*主機*（主機專用 cookie）屬性和一個 *名稱* 屬性。</span><span class="sxs-lookup"><span data-stu-id="9361a-132">**(Required)** A \<shared-cookie\> element requires, at minimum, a *domain* (for domain cookies) or a *host* (for host-only cookies) attribute and a *name* attribute.</span></span><br><span data-ttu-id="9361a-133">這些必須與 cookie 的網域和名稱完全相符。</span><span class="sxs-lookup"><span data-stu-id="9361a-133">These must be exact matches to the cookie's domain and name respectively.</span></span> <span data-ttu-id="9361a-134">**注意**：子域不相符。</span><span class="sxs-lookup"><span data-stu-id="9361a-134">**Note** that subdomains do not match.</span></span><br><br><span data-ttu-id="9361a-135">*網域* 屬性用於網域 cookie （但允許使用前導點，但可選用）。</span><span class="sxs-lookup"><span data-stu-id="9361a-135">The *domain* attribute is used for domain cookies (and a leading dot is allowed but optional).</span></span><br><span data-ttu-id="9361a-136">*host* 屬性適用於主機專用的 cookie（而前導點則是錯誤）。</span><span class="sxs-lookup"><span data-stu-id="9361a-136">The *host* attribute is used for host-only cookies (and a leading dot is an error).</span></span> <span data-ttu-id="9361a-137">若將這兩個都不指定或都指定將會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="9361a-137">Specifying neither or both will result in an error.</span></span><br><span data-ttu-id="9361a-138">\* 若在 cookie 字串中指定網域，則 cookie 即為網域 cookie（透過 HTTP Set-Cookie 回應標頭或document.cookie JS AP）。</span><span class="sxs-lookup"><span data-stu-id="9361a-138">\* A cookie is a domain cookie if a domain was specified in the cookie string (via HTTP Set-Cookie response header or document.cookie JS API).</span></span> <span data-ttu-id="9361a-139">網域 cookie 適用於指定的網域和所有子網域。</span><span class="sxs-lookup"><span data-stu-id="9361a-139">A domain cookie applies to the specified domain and all subdomains.</span></span> <span data-ttu-id="9361a-140">\* 若未在 cookie 字串中指定網域，則 cookie 即為主機專用 cookie，且只適用於其所設定的特定主機。</span><span class="sxs-lookup"><span data-stu-id="9361a-140">If a domain was not specified in the cookie string, the cookie is a host-only cookie and only applies to the specific host that it was set for.</span></span> <span data-ttu-id="9361a-141">需要注意的是，有些類別的 URLs 像是單一文字的主機名稱（例如 http://intranetsite) 和 IP 位址（例如 http://10.0.0.1) 只可以設定主機專用的 cookie。</span><span class="sxs-lookup"><span data-stu-id="9361a-141">Note that some classes of URLs such as single-word hostnames (e.g. http://intranetsite) and IP addresses (e.g. http://10.0.0.1) can only set host-only cookies.</span></span>    |
| \<shared-cookie **host**="subdomain.contoso.com" **name**="cookie2" **path**="/a/b/c"\>\</shared-cookie\>  | <span data-ttu-id="9361a-142">**（選用）** 可以指定 *路徑* 屬性。</span><span class="sxs-lookup"><span data-stu-id="9361a-142">**(Optional)** A *path* attribute may be specified.</span></span> <span data-ttu-id="9361a-143">如果未指定路徑屬性（或路徑屬性為空白），無論路徑為何（萬用字元規則），任何比對的網域/主機和名稱都符合該原則。</span><span class="sxs-lookup"><span data-stu-id="9361a-143">If no path attribute is specified (or if the path attribute is empty), any cookies matching domain/host and name match the policy, regardless of path (wildcard rule).</span></span><br><br><span data-ttu-id="9361a-144">如果已指定路徑，它必須是完全相符的路徑。</span><span class="sxs-lookup"><span data-stu-id="9361a-144">If a path is specified, it must be an exact match.</span></span><br><span data-ttu-id="9361a-145">如果 cookie 符合的規則是具有路徑，則此規則的優先順序高於不具路徑的規則。</span><span class="sxs-lookup"><span data-stu-id="9361a-145">If a cookie matches a rule with a path, that takes precedence over a rule without a path.</span></span> |

#### <span data-ttu-id="9361a-146">共用範例</span><span class="sxs-lookup"><span data-stu-id="9361a-146">Sharing example</span></span>

```xml
<site-list version="1">
<shared-cookie domain=".contoso.com" name="cookie1"></shared-cookie> 
<shared-cookie host="subdomain.contoso.com" name="cookie2" path="/a/b/c">
</shared-cookie>
</site-list>
```

## <span data-ttu-id="9361a-147">請參閱</span><span class="sxs-lookup"><span data-stu-id="9361a-147">See also</span></span>

- [<span data-ttu-id="9361a-148">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="9361a-148">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="9361a-149">可設定的網站資訊</span><span class="sxs-lookup"><span data-stu-id="9361a-149">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="9361a-150">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="9361a-150">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="9361a-151">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9361a-151">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
