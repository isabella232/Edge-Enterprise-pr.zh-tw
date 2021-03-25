---
title: 在企業模式網站清單中設定網站
ms.author: cjacks
author: cjacks
manager: saudm
ms.date: 05/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定企業網站清單
ms.openlocfilehash: 9b1943e4d50dcc770b4a634b99ecbd001d1ffbcc
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447647"
---
# <a name="configure-sites-on-the-enterprise-mode-site-list"></a><span data-ttu-id="61fe9-103">在企業模式網站清單中設定網站</span><span class="sxs-lookup"><span data-stu-id="61fe9-103">Configure Sites on the Enterprise Mode Site List</span></span>

<span data-ttu-id="61fe9-104">本文說明對企業模式網站清單所做的變更，支援為 Microsoft Edge 版本 77 及更新版本設定 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="61fe9-104">This article describes changes to the Enterprise Mode Site List that support configuring IE mode for Microsoft Edge version 77 and later.</span></span>

<span data-ttu-id="61fe9-105">如需有關企業模式網站清單 XML 檔案結構描述的詳細資訊，請參閱[企業模式結構描述第 2 版指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="61fe9-105">For more information on the schema for the Enterprise Mode Site List XML file, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

> [!NOTE]
> <span data-ttu-id="61fe9-106">本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="61fe9-106">This article applies to Microsoft Edge **Stable**, **Beta** and **Dev** Channels, version 77 or later.</span></span>

## <a name="updated-schema-elements"></a><span data-ttu-id="61fe9-107">更新的結構描述元素</span><span class="sxs-lookup"><span data-stu-id="61fe9-107">Updated schema elements</span></span>

<span data-ttu-id="61fe9-108">下表描述新增到企業模式結構描述 v.2 中的 \<open-in app\> 元素：</span><span class="sxs-lookup"><span data-stu-id="61fe9-108">The following table describes the \<open-in app\> element added to the v.2 of the Enterprise Mode schema:</span></span>

| **<span data-ttu-id="61fe9-109">元素</span><span class="sxs-lookup"><span data-stu-id="61fe9-109">Element</span></span>** | **<span data-ttu-id="61fe9-110">說明</span><span class="sxs-lookup"><span data-stu-id="61fe9-110">Description</span></span>** |
| --- | --- |
| \<open-in app="**true**"\> | <span data-ttu-id="61fe9-111">可控制針對網站使用何種瀏覽器的子元素。</span><span class="sxs-lookup"><span data-stu-id="61fe9-111">A child element that controls what browser is used for sites.</span></span> <span data-ttu-id="61fe9-112">對於需要在 **IE11 中開啟**的網站，需要此元素。</span><span class="sxs-lookup"><span data-stu-id="61fe9-112">This element is required for sites that need to **open in IE11**.</span></span>|

**<span data-ttu-id="61fe9-113">範例：</span><span class="sxs-lookup"><span data-stu-id="61fe9-113">Example:</span></span>**

``` xml
<site url="contoso.com">

  <open-in app="true">IE11</open-in>

</site>
```

<span data-ttu-id="61fe9-114">下表顯示 \<open-in\> 元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="61fe9-114">The following table shows the possible values of the \<open-in\> element:</span></span>

| **<span data-ttu-id="61fe9-115">值</span><span class="sxs-lookup"><span data-stu-id="61fe9-115">Value</span></span>** | **<span data-ttu-id="61fe9-116">說明</span><span class="sxs-lookup"><span data-stu-id="61fe9-116">Description</span></span>** |
| --- | --- |
| **\<open-in\><span data-ttu-id="61fe9-117">IE11</span><span class="sxs-lookup"><span data-stu-id="61fe9-117">IE11</span></span>\</open-in\>** | <span data-ttu-id="61fe9-118">在 IE 模式或完整 IE11 視窗中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="61fe9-118">Opens the site in IE mode or a full IE11 window.</span></span> <span data-ttu-id="61fe9-119">若要啟用 IE 模式，請參閱[設定 IE 模式原則](./edge-ie-mode-policies.md)</span><span class="sxs-lookup"><span data-stu-id="61fe9-119">To enable IE mode, see [Configure IE mode policies](./edge-ie-mode-policies.md)</span></span>|
| **\<open-in app="**true**"\><span data-ttu-id="61fe9-120">IE11</span><span class="sxs-lookup"><span data-stu-id="61fe9-120">IE11</span></span>\</open-in\>** | <span data-ttu-id="61fe9-121">在完整 IE11 視窗中開啟網站</span><span class="sxs-lookup"><span data-stu-id="61fe9-121">Opens the site in a full IE11 window</span></span> |
| **\<open-in\><span data-ttu-id="61fe9-122">MSEdge</span><span class="sxs-lookup"><span data-stu-id="61fe9-122">MSEdge</span></span>\</open-in\>** | <span data-ttu-id="61fe9-123">在 Microsoft Edge 中開啟網站</span><span class="sxs-lookup"><span data-stu-id="61fe9-123">Opens the site in Microsoft Edge</span></span> |
| **\<open-in\><span data-ttu-id="61fe9-124">無或不指定</span><span class="sxs-lookup"><span data-stu-id="61fe9-124">None or not specified</span></span>\</open-in\>** | <span data-ttu-id="61fe9-125">在預設瀏覽器或使用者瀏覽至網站的瀏覽器中開啟網站。</span><span class="sxs-lookup"><span data-stu-id="61fe9-125">Opens the site in the default browser or in the browser where the user navigated to the site.</span></span> |
|**\<open-in\><span data-ttu-id="61fe9-126">可設定</span><span class="sxs-lookup"><span data-stu-id="61fe9-126">Configurable</span></span>\</open-in\>** | <span data-ttu-id="61fe9-127">允許網站參與 IE 模式引擎判斷。</span><span class="sxs-lookup"><span data-stu-id="61fe9-127">Allows the site to participate in IE mode engine determination.</span></span> <span data-ttu-id="61fe9-128">若要深入了解，請參閱[了解 IE 模式中可設定的網站](edge-learnmore-configurable-sites-ie-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="61fe9-128">To learn more, see [Learn about Configurable sites in IE mode](edge-learnmore-configurable-sites-ie-mode.md).</span></span>  |

>[!NOTE]
> <span data-ttu-id="61fe9-129">僅當與 _'open-in' IE11_ 關聯時，才會識別屬性 app=**"true"**。</span><span class="sxs-lookup"><span data-stu-id="61fe9-129">The attribute app=**"true"** is only recognized when associated to _'open-in' IE11_.</span></span> <span data-ttu-id="61fe9-130">將其新增到其他 'open-in' 元素，不會變更瀏覽器行為。</span><span class="sxs-lookup"><span data-stu-id="61fe9-130">Adding it to the other 'open-in' elements won't change browser behavior.</span></span>   

## <a name="configure-neutral-sites"></a><span data-ttu-id="61fe9-131">設定中性網站</span><span class="sxs-lookup"><span data-stu-id="61fe9-131">Configure neutral sites</span></span>

<span data-ttu-id="61fe9-132">為了讓 IE 模式正常運作，必須將驗證/單一登入伺服器明確設定為中性網站。</span><span class="sxs-lookup"><span data-stu-id="61fe9-132">In order for IE mode to work properly, authentication / Single Sign-On servers will need to be explicitly configured as neutral sites.</span></span> <span data-ttu-id="61fe9-133">否則，IE 模式頁面會嘗試重新導向至 Microsoft Edge，而驗證將會失敗。</span><span class="sxs-lookup"><span data-stu-id="61fe9-133">Otherwise, IE mode pages will try to redirect to Microsoft Edge, and authentication will fail.</span></span>

<span data-ttu-id="61fe9-134">中性網站會使用瀏覽啟動的瀏覽器 - Microsoft Edge 或 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="61fe9-134">A neutral site will use the browser where the navigation started - either Microsoft Edge or IE mode.</span></span> <span data-ttu-id="61fe9-135">設定中性網站可確保使用這些驗證伺服器的所有應用程式 (新式與舊版) 會繼續運作。</span><span class="sxs-lookup"><span data-stu-id="61fe9-135">Configuring neutral sites ensures that all applications using these authentication servers, both modern and legacy, continue to work.</span></span>

<span data-ttu-id="61fe9-136">您可以將 Enterprise Mode Site List Manager 工具中的 [開啟於]\*\* 下拉式功能表設定為 [無]，或直接更新網站清單 XML，藉此來設定中性網站：</span><span class="sxs-lookup"><span data-stu-id="61fe9-136">You can configure neutral sites by setting the *Open In* dropdown to 'None' in the Enterprise Mode Site List Manager tool or by directly updating the site list XML:</span></span>

``` xml
<site url="login.contoso.com">
   
    <open-in>None</open-in>

</site>
```

<span data-ttu-id="61fe9-137">若要識別驗證伺服器，請使用 IE11 開發人員工具檢查來自應用程式的網路流量。</span><span class="sxs-lookup"><span data-stu-id="61fe9-137">To identify authentication servers, inspect the network traffic from an application using the IE11 Developer Tools.</span></span> <span data-ttu-id="61fe9-138">如果您需要更多時間來識別驗證伺服器，您可以設定原則，以在 IE 模式中保留所有頁面內導覽。</span><span class="sxs-lookup"><span data-stu-id="61fe9-138">If you need more time to identify your authentication servers, you can configure a policy to keep all in-page navigation in IE mode.</span></span> <span data-ttu-id="61fe9-139">若要將 IE 模式的使用降至最低，請在識別並將驗證伺服器新增至網站清單之後，停用此設定。</span><span class="sxs-lookup"><span data-stu-id="61fe9-139">To minimize the use of IE mode, disable this setting once you've identified and added your authentication servers to the site list.</span></span> <span data-ttu-id="61fe9-140">如需詳細資訊，請參閱[設定頁面內導覽維持在 IE 模式](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect)。</span><span class="sxs-lookup"><span data-stu-id="61fe9-140">For more information, see [Configure in-page navigation to remain in IE mode](./microsoft-edge-policies.md#internetexplorerintegrationsiteredirect).</span></span>

>[!NOTE]
   ><span data-ttu-id="61fe9-141">IE 模式整合不支援企業模式結構描述 v.1。</span><span class="sxs-lookup"><span data-stu-id="61fe9-141">Enterprise Mode schema v.1 isn't supported for IE mode integration.</span></span> <span data-ttu-id="61fe9-142">如果目前使用結構描述 v.1 搭配 Internet Explorer 11，則必須升級到結構描述 v.2。</span><span class="sxs-lookup"><span data-stu-id="61fe9-142">If you are currently using schema v.1 with Internet Explorer 11, you must upgrade to schema v.2.</span></span> <span data-ttu-id="61fe9-143">如需詳細資訊，請參閱[企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。</span><span class="sxs-lookup"><span data-stu-id="61fe9-143">For more information, see [Enterprise Mode schema v.2 guidance](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance).</span></span>

## <a name="see-also"></a><span data-ttu-id="61fe9-144">請參閱</span><span class="sxs-lookup"><span data-stu-id="61fe9-144">See also</span></span>

- [<span data-ttu-id="61fe9-145">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="61fe9-145">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="61fe9-146">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="61fe9-146">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="61fe9-147">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="61fe9-147">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)