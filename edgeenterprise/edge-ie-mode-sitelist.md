---
title: 企業網站設定策略
ms.author: shisub
author: shisub
manager: srugh
ms.date: 03/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 為 Internet Explorer 模式設定企業模式網站清單的逐步指南。
ms.openlocfilehash: 1d0b80950439fce77513413c3f5d1143538487d1
ms.sourcegitcommit: 93851b83dc11422924646a04a9e0f60ff2554af7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/01/2021
ms.locfileid: "11470151"
---
# <a name="enterprise-site-configuration-strategy"></a><span data-ttu-id="be312-103">企業網站設定策略</span><span class="sxs-lookup"><span data-stu-id="be312-103">Enterprise site configuration strategy</span></span>

<span data-ttu-id="be312-104">本文將說明企業模式網站清單的變更，以支援 Microsoft Edge 版本 77 及更新版本的 Internet Explorer 模式。</span><span class="sxs-lookup"><span data-stu-id="be312-104">This article describes changes to the Enterprise Mode Site List to support Internet Explorer mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="be312-105">如需有關企業模式網站清單 XML 檔案結構描述的詳細資訊，請參閱[企業模式結構描述 v.2 指引](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="be312-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="be312-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="be312-106">This article applies to Microsoft Edge version 77 or later.</span></span>
<!--
## Updated schema elements

The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:

| **Element** | **Description** |
| --- | --- |
| \<open-in app="**true**"\> | A child element that controls what browser is used for sites. This element is required for sites that need to **open in IE11**.|

**Example:**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

The following table shows the possible values of the \<open-in\> element:

| **Value** | **Description** |
| --- | --- |
| **\<open-in\>IE11\</open-in\>** | Opens the site in IE mode or a full IE11 window. To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)|
| **\<open-in app="**true**"\>IE11\</open-in\>** | Opens the site in a full IE11 window |
| **\<open-in\>MSEdge\</open-in\>** | Opens the site in Microsoft Edge |
| **\<open-in\>None or not specified\</open-in\>** | Opens the site in the default browser or in the browser where the user navigated to the site. |
|**\<open-in\>Configurable\</open-in\>** | Allows the site to participate in IE mode engine determination. To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).  |

>[!NOTE]
> The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_. Adding it to the other 'open-in' elements won't change browser behavior.   -->

## <a name="configuration-strategy"></a><span data-ttu-id="be312-107">設定策略</span><span class="sxs-lookup"><span data-stu-id="be312-107">Configuration strategy</span></span>

<span data-ttu-id="be312-108">下列步驟是 IE 模式網站設定策略的一部分：</span><span class="sxs-lookup"><span data-stu-id="be312-108">The following steps are part of a site configuration strategy for IE mode:</span></span>
1. <span data-ttu-id="be312-109">準備您的網站清單</span><span class="sxs-lookup"><span data-stu-id="be312-109">Prepare your site list</span></span>
2. <span data-ttu-id="be312-110">設定中性網站</span><span class="sxs-lookup"><span data-stu-id="be312-110">Configure neutral sites</span></span>
3. <span data-ttu-id="be312-111">(選擇性) 必要時使用 Cookie 共用</span><span class="sxs-lookup"><span data-stu-id="be312-111">(Optional) Use cookie sharing if necessary</span></span>

<!--
Step 1.  – if you don’t have one use Site Discovery Step-by-Step
Step 2 – Neutral sites + sticky mode
        Use more examples and explain sticky mode better
Step 3 – If that doesn’t cover your needs, then use Cookie sharing -->

## <a name="prepare-your-site-list"></a><span data-ttu-id="be312-112">準備您的網站清單</span><span class="sxs-lookup"><span data-stu-id="be312-112">Prepare your site list</span></span>

<span data-ttu-id="be312-113">如果您已經有適用於 IE11 或舊版 Microsoft Edge 的企業模式網站清單，您可以重複使用該清單來設定 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="be312-113">If you already have an Enterprise Mode site list for IE11 or Microsoft Edge Legacy, you can reuse it to configure IE mode.</span></span>

<span data-ttu-id="be312-114">不過，如果您沒有網站清單，您可以使用[企業網站探索工具](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery)來填入網站清單。</span><span class="sxs-lookup"><span data-stu-id="be312-114">However, if you don't have a site list, you can use the [Enterprise Site Discovery tool](https://docs.microsoft.com/deployedge/edge-ie-mode-site-discovery) to populate your site list.</span></span>

## <a name="configure-neutral-sites"></a><span data-ttu-id="be312-115">設定中性網站</span><span class="sxs-lookup"><span data-stu-id="be312-115">Configure neutral sites</span></span>

<span data-ttu-id="be312-116">為了讓 IE 模式正常運作，驗證/單一登入 (SSO) 伺服器必須明確設定為中立網站。</span><span class="sxs-lookup"><span data-stu-id="be312-116">In order for IE mode to work properly, authentication / Single Sign-On (SSO) servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="be312-117">否則，IE 模式頁面會嘗試重新導向至 Microsoft Edge，而驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="be312-117">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="be312-118">中性網站會使用瀏覽啟動的瀏覽器 - Microsoft Edge 或 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="be312-118">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="be312-119">設定中性網站可確保使用這些驗證伺服器的所有應用程式 (新式與舊版) 會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="be312-119">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="be312-120">您可以將 Enterprise Mode Site List Manager 工具中的 [開啟於]\*\* 下拉式功能表設定為 [無]，或直接更新網站清單 XML，藉此來設定中性網站：</span><span class="sxs-lookup"><span data-stu-id="be312-120">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="be312-121">若要識別驗證伺服器，請使用 IE11 開發人員工具檢查來自應用程式的網路流量。</span><span class="sxs-lookup"><span data-stu-id="be312-121">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="be312-122">如果您需要更多時間來識別您的驗證伺服器，您可以設定原則，將所有頁面內導覽保持在 IE 模式，讓您的使用者可不間斷地繼續其工作流程。</span><span class="sxs-lookup"><span data-stu-id="be312-122">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigations in IE mode to allow your users to continue their workflows uninterrupted.</span></span> <span data-ttu-id="be312-123">若要將 IE 模式的使用在不必要時最小化，請在識別和新增驗證伺服器至網站清單後停用此設定。</span><span class="sxs-lookup"><span data-stu-id="be312-123">To minimize the use of IE mode when unnecessary, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="be312-124">如需詳細資訊，請參閱[在 IE 模式中保持頁面內導覽](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav)。</span><span class="sxs-lookup"><span data-stu-id="be312-124">For more information, see [Keep in-page navigation in IE mode](https://docs.microsoft.com/deployedge/edge-learnmore-inpage-nav).</span></span>

>[!NOTE]
   ><span data-ttu-id="be312-125">IE 模式整合不支援企業模式結構描述 v.1。</span><span class="sxs-lookup"><span data-stu-id="be312-125">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="be312-126">如果目前使用結構描述 v.1 搭配 Internet Explorer 11，則必須升級到結構描述 v.2。</span><span class="sxs-lookup"><span data-stu-id="be312-126">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="be312-127">如需詳細資訊，請參閱[企業模式結構描述 v.2 指引](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="be312-127">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="optional-use-cookie-sharing-if-necessary"></a><span data-ttu-id="be312-128">(選擇性) 必要時使用 Cookie 共用</span><span class="sxs-lookup"><span data-stu-id="be312-128">(Optional) Use cookie sharing if necessary</span></span>

<span data-ttu-id="be312-129">根據預設，Microsoft Edge 和 Internet Explorer 處理程序不會共用工作階段 Cookie，在某些情況下，使用 IE 模式時，這種缺少共用的情況可能不太方便。</span><span class="sxs-lookup"><span data-stu-id="be312-129">By default, the Microsoft Edge and Internet Explorer processes don't share session cookies, and this lack of sharing can be inconvenient in some cases while using IE mode.</span></span> <span data-ttu-id="be312-130">例如，當使用者之前習慣在 IE 模式中重新驗證時，或登出 Microsoft Edge 工作階段卻不會針對重要交易登出 Internet Explorer 模式工作階段時。</span><span class="sxs-lookup"><span data-stu-id="be312-130">For example, when a user has to reauthenticate in IE mode when previously they are accustomed to doing so or when signing out of a Microsoft Edge session doesn’t sign out of the Internet Explorer mode session for critical transactions.</span></span> <span data-ttu-id="be312-131">在這些情況下，您可以設定 SSO 所設定的特定 Cookie，以從 Microsoft Edge 傳送至 Internet Explorer，如此一來，由於無需重新驗證，驗證體驗就會更順暢。</span><span class="sxs-lookup"><span data-stu-id="be312-131">In these scenarios, you can configure specific cookies set by SSO to be sent from Microsoft Edge to Internet Explorer so the authentication experience becomes more seamless by eliminating the need to reauthenticate.</span></span> <span data-ttu-id="be312-132">若需詳細資訊，請參閱[從 Microsoft Edge 共用 Cookie 到 Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare)。</span><span class="sxs-lookup"><span data-stu-id="be312-132">For more information, see [Cookie sharing from Microsoft Edge to Internet Explorer](https://docs.microsoft.com/deployedge/edge-ie-mode-add-guidance-cookieshare).</span></span>

## <a name="see-also"></a><span data-ttu-id="be312-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be312-133">See also</span></span>

- [<span data-ttu-id="be312-134">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="be312-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="be312-135">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="be312-135">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="be312-136">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="be312-136">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
