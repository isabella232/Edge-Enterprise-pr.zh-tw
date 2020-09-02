---
title: Microsoft Edge URL 原則的篩選格式
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 深入了解用於 Microsoft Edge URLBlocklist 和 URLAllowlist 原則的篩選格式。
ms.openlocfilehash: 5a0eff1ca7be17fccd1087716d426b13ea302847
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979525"
---
# <span data-ttu-id="3ba88-103">URL 清單型原則的篩選格式</span><span class="sxs-lookup"><span data-stu-id="3ba88-103">Filter format for URL list-based policies</span></span>

<span data-ttu-id="3ba88-104">本文說明用於 Microsoft Edge URL 清單型原則的篩選格式 (例如 [URLBlocklist](microsoft-edge-policies.md#urlblocklist)、[URLAllowList](microsoft-edge-policies.md#urlallowlist) 和 [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) 原則)。</span><span class="sxs-lookup"><span data-stu-id="3ba88-104">This article describes the filter format used for the Microsoft Edge URL list-based policies (For example, [URLBlocklist](microsoft-edge-policies.md#urlblocklist), [URLAllowList](microsoft-edge-policies.md#urlallowlist), and [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) policies.</span></span>

> [!NOTE]
> <span data-ttu-id="3ba88-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3ba88-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="3ba88-106">篩選格式</span><span class="sxs-lookup"><span data-stu-id="3ba88-106">The filter format</span></span>

<span data-ttu-id="3ba88-107">篩選格式為：</span><span class="sxs-lookup"><span data-stu-id="3ba88-107">The filter format is:</span></span>

```
    [scheme://][.]host[:port][/path][@query]
```

<span data-ttu-id="3ba88-108">篩選格式中的欄位為：</span><span class="sxs-lookup"><span data-stu-id="3ba88-108">The fields in the filter format are:</span></span>

| <span data-ttu-id="3ba88-109">欄位</span><span class="sxs-lookup"><span data-stu-id="3ba88-109">Field</span></span> | <span data-ttu-id="3ba88-110">描述</span><span class="sxs-lookup"><span data-stu-id="3ba88-110">Description</span></span> |
| --- | --- |
| <span data-ttu-id="3ba88-111">**scheme** (*選用*)</span><span class="sxs-lookup"><span data-stu-id="3ba88-111">**scheme** (*optional*)</span></span> | <span data-ttu-id="3ba88-112">它可以是 http://、https://、ftp://、edge:// 等。</span><span class="sxs-lookup"><span data-stu-id="3ba88-112">It can be http://, https://, ftp://, edge://, etc.</span></span> |
| <span data-ttu-id="3ba88-113">**host** (*必要*)</span><span class="sxs-lookup"><span data-stu-id="3ba88-113">**host** (*required*)</span></span> | <span data-ttu-id="3ba88-114">它必須是有效的主機名稱或 IP 位址，並且您可以使用萬用字元 ("\*")。</span><span class="sxs-lookup"><span data-stu-id="3ba88-114">It must be a valid host name or IP address and you can use a wildcard ("\*").</span></span> <span data-ttu-id="3ba88-115">若要停用子網域比對，請在 **host** 之前加上一個選用的點 (".")。</span><span class="sxs-lookup"><span data-stu-id="3ba88-115">To disable subdomain matching, include an optional dot (".") before **host**.</span></span> |
| <span data-ttu-id="3ba88-116">**port** (*選用*)</span><span class="sxs-lookup"><span data-stu-id="3ba88-116">**port** (*optional*)</span></span> | <span data-ttu-id="3ba88-117">有效值範圍為 1 到 65535。</span><span class="sxs-lookup"><span data-stu-id="3ba88-117">Valid values range from 1 to 65535.</span></span> |
| <span data-ttu-id="3ba88-118">**path** (*選用*)</span><span class="sxs-lookup"><span data-stu-id="3ba88-118">**path** (*optional*)</span></span> | <span data-ttu-id="3ba88-119">您可以在路徑中使用任何字串。</span><span class="sxs-lookup"><span data-stu-id="3ba88-119">You can use any string in the path.</span></span> |
| <span data-ttu-id="3ba88-120">**query** (*選用*)</span><span class="sxs-lookup"><span data-stu-id="3ba88-120">**query** (*optional*)</span></span> | <span data-ttu-id="3ba88-121">**query** 是鍵值或僅鍵權杖，由 & 符號分隔。</span><span class="sxs-lookup"><span data-stu-id="3ba88-121">The **query** is either key-value or key-only tokens separated by an ampersand ("&").</span></span> <span data-ttu-id="3ba88-122">使用等號 ("=") 分隔鍵值權杖。</span><span class="sxs-lookup"><span data-stu-id="3ba88-122">Separate key-value tokens with an equal sign ("=").</span></span> <span data-ttu-id="3ba88-123">若要指示首碼比對，可以在 **query** 結尾使用星號 ("\*")。</span><span class="sxs-lookup"><span data-stu-id="3ba88-123">To indicate a prefix match, you can use an asterisk ("\*") at the end of the **query**.</span></span> |

## <span data-ttu-id="3ba88-124">將篩選格式與 URL 格式進行比較</span><span class="sxs-lookup"><span data-stu-id="3ba88-124">Comparing the filter format to the URL format</span></span>

<span data-ttu-id="3ba88-125">篩選格式類似於 URL 格式，但有以下差異：</span><span class="sxs-lookup"><span data-stu-id="3ba88-125">The filter format resembles the URL format, except for the following differences:</span></span>

- <span data-ttu-id="3ba88-126">如果您包含 "user:pass"，將會忽略它。</span><span class="sxs-lookup"><span data-stu-id="3ba88-126">If you include "user:pass", it will be ignored.</span></span> <span data-ttu-id="3ba88-127">例如，http://user:pass@ftp.contoso.com/pub/example.iso。</span><span class="sxs-lookup"><span data-stu-id="3ba88-127">For example, http://user:pass@ftp.contoso.com/pub/example.iso.</span></span>
- <span data-ttu-id="3ba88-128">如果包含片段識別碼 ("#")，則將忽略它和識別碼後面的所有內容。</span><span class="sxs-lookup"><span data-stu-id="3ba88-128">If you include a fragment identifier ("#"), it and everything that follows the identifier is ignored.</span></span>
- <span data-ttu-id="3ba88-129">您可以使用萬用字元 ("\*") 做為 **host**，並且可以在前面使用點 (".")。</span><span class="sxs-lookup"><span data-stu-id="3ba88-129">You can use a wildcard ("\*") as the **host** and you can prefix it with a dot (".").</span></span>
- <span data-ttu-id="3ba88-130">您可以使用正斜線 ("/") 或點 (".") 做為 **host** 的尾碼。</span><span class="sxs-lookup"><span data-stu-id="3ba88-130">You can use a forward slash ("/") or a dot (".") as a suffix for the **host**.</span></span> <span data-ttu-id="3ba88-131">在這種情況下，將忽略尾碼。</span><span class="sxs-lookup"><span data-stu-id="3ba88-131">In this case, the suffix is ignored.</span></span>

## <span data-ttu-id="3ba88-132">篩選選取準則</span><span class="sxs-lookup"><span data-stu-id="3ba88-132">Filter selection criteria</span></span>

<span data-ttu-id="3ba88-133">為 URL 選取的篩選是處理以下篩選選取規則後所找到的最具體相符項目：</span><span class="sxs-lookup"><span data-stu-id="3ba88-133">The filter selected for a URL is the most specific match found after processing the following filter selection rules:</span></span>

1. <span data-ttu-id="3ba88-134">首先選取 **host** 相符長度最長的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-134">Filters with the longest **host** match are selected first.</span></span>
2. <span data-ttu-id="3ba88-135">從所選篩選中，將丟棄任何具有不相符 scheme 或 port 的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-135">From the selected filters, any filter with a non-matching scheme or port is discarded.</span></span>
3. <span data-ttu-id="3ba88-136">從其餘篩選中，選取具有最長相符 **path** 的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-136">From the remaining filters, the filter with the longest matching **path** is selected.</span></span>
4. <span data-ttu-id="3ba88-137">從其餘篩選中，選取具有最長 query 權杖集的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-137">From the remaining filters, the filter with the longest set of query tokens is selected.</span></span> <span data-ttu-id="3ba88-138">在此步驟中，如果允許清單篩選和封鎖清單篩選具有相同的 **path** 長度和相同的 **query** 權杖數，則允許清單篩選優先於封鎖清單篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-138">At this step, the allow list filter takes precedence over the block list filter if both filters have the same **path** length and number of **query** tokens.</span></span>
5. <span data-ttu-id="3ba88-139">如果沒有剩餘有效的篩選，則從 **host** 中移除最左側的子網域，並從步驟 1 重新開始選取程序。</span><span class="sxs-lookup"><span data-stu-id="3ba88-139">If there's no valid filter remaining, then the left-most subdomain is removed from **host** and the selection process starts over at step 1.</span></span> <span data-ttu-id="3ba88-140">特殊星號 ("\*") **host** 是最後搜尋的，它會比對所有主機。</span><span class="sxs-lookup"><span data-stu-id="3ba88-140">The special asterisk ("\*") **host** is the last searched and it matches all hosts.</span></span>
6. <span data-ttu-id="3ba88-141">如果有可用篩選，它將封鎖或允許 URL 請求。</span><span class="sxs-lookup"><span data-stu-id="3ba88-141">If a filter's available, it blocks or allows the URL request.</span></span>

   >[!NOTE]
   ><span data-ttu-id="3ba88-142">如果沒有相符篩選，預設行為是允許 URL 請求。</span><span class="sxs-lookup"><span data-stu-id="3ba88-142">The default behavior is to allow the URL request if no filter is matched.</span></span>

## <span data-ttu-id="3ba88-143">篩選選取準則範例</span><span class="sxs-lookup"><span data-stu-id="3ba88-143">Example filter selection criteria</span></span>

<span data-ttu-id="3ba88-144">在此範例中，搜尋與 "https://sub.contoso.com/docs" 的相符項時，篩選選取將會：</span><span class="sxs-lookup"><span data-stu-id="3ba88-144">In this example, when searching for a match to "https://sub.contoso.com/docs" the filter selection will:</span></span>

1. <span data-ttu-id="3ba88-145">搜尋符合 "sub.contoso.com" 的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-145">Search for a filter for "sub.contoso.com".</span></span> <span data-ttu-id="3ba88-146">如果找到篩選，搜尋將移到步驟 2。</span><span class="sxs-lookup"><span data-stu-id="3ba88-146">If it finds a filter, the search moves to step 2.</span></span> <span data-ttu-id="3ba88-147">如果未找到篩選，則它再次嘗試 "contoso.com"、"com"，最後嘗試 ""。</span><span class="sxs-lookup"><span data-stu-id="3ba88-147">If a filter isn't found, then it tries again with "contoso.com", "com", and finally "".</span></span>
2. <span data-ttu-id="3ba88-148">從所選篩選中移除 **scheme** 中沒有 "http" 的任何篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-148">From the selected filters, any that don't have "http" in the **scheme** are removed.</span></span>
3. <span data-ttu-id="3ba88-149">從其餘篩選中移除任何確切連接埠號碼不是 "80" 的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-149">From the remaining filters, any that have an exact port number that isn't "80" are removed.</span></span>
4. <span data-ttu-id="3ba88-150">從其餘篩選中移除 **path** 首碼沒有 "/docs" 的任何篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-150">From the remaining filters, any that don't have "/docs" as a prefix of the **path** are removed.</span></span>
5. <span data-ttu-id="3ba88-151">從其餘篩選中，選取並套用具有最長 path 首碼的篩選。</span><span class="sxs-lookup"><span data-stu-id="3ba88-151">From the remaining filters, the filter with the longest path prefix is selected and applied.</span></span> <span data-ttu-id="3ba88-152">如果未找到篩選，則從步驟 1 重新開始選取程序。</span><span class="sxs-lookup"><span data-stu-id="3ba88-152">If a filter isn't found, the selection process starts over again at step 1.</span></span> <span data-ttu-id="3ba88-153">將使用下一個子網域重複此程序。</span><span class="sxs-lookup"><span data-stu-id="3ba88-153">The process is repeated with the next subdomain.</span></span>

### <span data-ttu-id="3ba88-154">其他篩選資訊</span><span class="sxs-lookup"><span data-stu-id="3ba88-154">Additional filter information</span></span>

<span data-ttu-id="3ba88-155">如果篩選在 **host** 前具有點 (".") 首碼，則僅篩選確切的 **host** 相符項。</span><span class="sxs-lookup"><span data-stu-id="3ba88-155">If a filter has a dot (".") prefixing the **host** then only exact **host** matches are filtered.</span></span> <span data-ttu-id="3ba88-156">例如：</span><span class="sxs-lookup"><span data-stu-id="3ba88-156">For example:</span></span>

- <span data-ttu-id="3ba88-157">"contoso.com" (無點) 將符合 "contoso.com", "www.contoso.com" 和 "sub.www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ba88-157">"contoso.com" (no dot) will match "contoso.com", "www.contoso.com", and "sub.www.contoso.com"</span></span>
- <span data-ttu-id="3ba88-158">".www.contoso.com" (帶有點首碼) 將僅符合 "www.contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ba88-158">".www.contoso.com" (with a dot prefix) will only match "www.contoso.com"</span></span>

<span data-ttu-id="3ba88-159">您可以使用標準或客戶 **schema**。</span><span class="sxs-lookup"><span data-stu-id="3ba88-159">You can use either a standard or customer **schema**.</span></span> <span data-ttu-id="3ba88-160">支援的標準 schema 包括：</span><span class="sxs-lookup"><span data-stu-id="3ba88-160">Supported standard schemas include:</span></span>

- <span data-ttu-id="3ba88-161">_about_、_blob_、_content_、_edge_、_cid_、_data_、_file_、_filesystem_、_ftp_、_gopher_、_http_、_https_、_javascript_、_mailto_、_ws_ 和 _wss_。</span><span class="sxs-lookup"><span data-stu-id="3ba88-161">_about_, _blob_, _content_, _edge_, _cid_, _data_, _file_, _filesystem_, _ftp_, _gopher_, _http_, _https_, _javascript_, _mailto_, _ws_, and _wss_.</span></span>

<span data-ttu-id="3ba88-162">任何其他 **schema** 都被視為自訂 **schema**，但只允許 _schema:\*_ 和 _schema://\*_ 模式。</span><span class="sxs-lookup"><span data-stu-id="3ba88-162">Any other **schema** is treated as a custom **schema**, but only the _schema:\*_ and _schema://\*_ patterns are allowed.</span></span> <span data-ttu-id="3ba88-163">例如：</span><span class="sxs-lookup"><span data-stu-id="3ba88-163">For example:</span></span>

- <span data-ttu-id="3ba88-164">"custom:*" 或 "custom://*" 將符合 "custom:app"</span><span class="sxs-lookup"><span data-stu-id="3ba88-164">"custom:*" or "custom://*" will match "custom:app"</span></span>
- <span data-ttu-id="3ba88-165">"custom:app" 或 "custom://app" 無效</span><span class="sxs-lookup"><span data-stu-id="3ba88-165">"custom:app" or "custom://app" are invalid</span></span>

<span data-ttu-id="3ba88-166">**schema** 和 **host** 不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3ba88-166">**schema** and **host** aren't case-sensitive.</span></span> <span data-ttu-id="3ba88-167">例如：</span><span class="sxs-lookup"><span data-stu-id="3ba88-167">For example:</span></span>

- <span data-ttu-id="3ba88-168">"http://contoso.com" 篩選符合 "HTTP://contoso.com"、"http://contoso.COM" 和 "http://contoso.com"</span><span class="sxs-lookup"><span data-stu-id="3ba88-168">"http://contoso.com" filter matches "HTTP://contoso.com", "http://contoso.COM", and "http://contoso.com"</span></span>

<span data-ttu-id="3ba88-169">**path** 和 **query** 區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3ba88-169">**path** and **query** are case-sensitive.</span></span> <span data-ttu-id="3ba88-170">例如：</span><span class="sxs-lookup"><span data-stu-id="3ba88-170">For example:</span></span>

- <span data-ttu-id="3ba88-171">"http://contoso.com/path?query=A" 篩選不符合 "http://contoso.com/Path?query=A" 或 "http://contoso.com/path?Query=A"。</span><span class="sxs-lookup"><span data-stu-id="3ba88-171">"http://contoso.com/path?query=A" filter doesn't match "http://contoso.com/Path?query=A" or "http://contoso.com/path?Query=A".</span></span> <span data-ttu-id="3ba88-172">但符合 "http://contoso.COM/path?query=A"。</span><span class="sxs-lookup"><span data-stu-id="3ba88-172">It does match "http://contoso.COM/path?query=A".</span></span>

## <span data-ttu-id="3ba88-173">內容授權</span><span class="sxs-lookup"><span data-stu-id="3ba88-173">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="3ba88-174">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="3ba88-174">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="3ba88-175">原始 [Chromium 頁面可在此處](https://www.chromium.org/administrators/url-blacklist-filter-format)找到。</span><span class="sxs-lookup"><span data-stu-id="3ba88-175">The original [Chromium page can be found here](https://www.chromium.org/administrators/url-blacklist-filter-format).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="3ba88-176">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="3ba88-176">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <span data-ttu-id="3ba88-177">請參閱</span><span class="sxs-lookup"><span data-stu-id="3ba88-177">See also</span></span>

- [<span data-ttu-id="3ba88-178">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3ba88-178">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
