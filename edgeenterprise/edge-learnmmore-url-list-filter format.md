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
# URL 清單型原則的篩選格式

本文說明用於 Microsoft Edge URL 清單型原則的篩選格式 (例如 [URLBlocklist](microsoft-edge-policies.md#urlblocklist)、[URLAllowList](microsoft-edge-policies.md#urlallowlist) 和 [CertificateTransparencyEnforcementDisabledForUrls](microsoft-edge-policies.md#certificatetransparencyenforcementdisabledforurls) 原則)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 篩選格式

篩選格式為：

```
    [scheme://][.]host[:port][/path][@query]
```

篩選格式中的欄位為：

| 欄位 | 描述 |
| --- | --- |
| **scheme** (*選用*) | 它可以是 http://、https://、ftp://、edge:// 等。 |
| **host** (*必要*) | 它必須是有效的主機名稱或 IP 位址，並且您可以使用萬用字元 ("\*")。 若要停用子網域比對，請在 **host** 之前加上一個選用的點 (".")。 |
| **port** (*選用*) | 有效值範圍為 1 到 65535。 |
| **path** (*選用*) | 您可以在路徑中使用任何字串。 |
| **query** (*選用*) | **query** 是鍵值或僅鍵權杖，由 & 符號分隔。 使用等號 ("=") 分隔鍵值權杖。 若要指示首碼比對，可以在 **query** 結尾使用星號 ("\*")。 |

## 將篩選格式與 URL 格式進行比較

篩選格式類似於 URL 格式，但有以下差異：

- 如果您包含 "user:pass"，將會忽略它。 例如，http://user:pass@ftp.contoso.com/pub/example.iso。
- 如果包含片段識別碼 ("#")，則將忽略它和識別碼後面的所有內容。
- 您可以使用萬用字元 ("*") 做為 **host**，並且可以在前面使用點 (".")。
- 您可以使用正斜線 ("/") 或點 (".") 做為 **host** 的尾碼。 在這種情況下，將忽略尾碼。

## 篩選選取準則

為 URL 選取的篩選是處理以下篩選選取規則後所找到的最具體相符項目：

1. 首先選取 **host** 相符長度最長的篩選。
2. 從所選篩選中，將丟棄任何具有不相符 scheme 或 port 的篩選。
3. 從其餘篩選中，選取具有最長相符 **path** 的篩選。
4. 從其餘篩選中，選取具有最長 query 權杖集的篩選。 在此步驟中，如果允許清單篩選和封鎖清單篩選具有相同的 **path** 長度和相同的 **query** 權杖數，則允許清單篩選優先於封鎖清單篩選。
5. 如果沒有剩餘有效的篩選，則從 **host** 中移除最左側的子網域，並從步驟 1 重新開始選取程序。 特殊星號 ("*") **host** 是最後搜尋的，它會比對所有主機。
6. 如果有可用篩選，它將封鎖或允許 URL 請求。

   >[!NOTE]
   >如果沒有相符篩選，預設行為是允許 URL 請求。

## 篩選選取準則範例

在此範例中，搜尋與 "https://sub.contoso.com/docs" 的相符項時，篩選選取將會：

1. 搜尋符合 "sub.contoso.com" 的篩選。 如果找到篩選，搜尋將移到步驟 2。 如果未找到篩選，則它再次嘗試 "contoso.com"、"com"，最後嘗試 ""。
2. 從所選篩選中移除 **scheme** 中沒有 "http" 的任何篩選。
3. 從其餘篩選中移除任何確切連接埠號碼不是 "80" 的篩選。
4. 從其餘篩選中移除 **path** 首碼沒有 "/docs" 的任何篩選。
5. 從其餘篩選中，選取並套用具有最長 path 首碼的篩選。 如果未找到篩選，則從步驟 1 重新開始選取程序。 將使用下一個子網域重複此程序。

### 其他篩選資訊

如果篩選在 **host** 前具有點 (".") 首碼，則僅篩選確切的 **host** 相符項。 例如：

- "contoso.com" (無點) 將符合 "contoso.com", "www.contoso.com" 和 "sub.www.contoso.com"
- ".www.contoso.com" (帶有點首碼) 將僅符合 "www.contoso.com"

您可以使用標準或客戶 **schema**。 支援的標準 schema 包括：

- _about_、_blob_、_content_、_edge_、_cid_、_data_、_file_、_filesystem_、_ftp_、_gopher_、_http_、_https_、_javascript_、_mailto_、_ws_ 和 _wss_。

任何其他 **schema** 都被視為自訂 **schema**，但只允許 _schema:*_ 和 _schema://*_ 模式。 例如：

- "custom:*" 或 "custom://*" 將符合 "custom:app"
- "custom:app" 或 "custom://app" 無效

**schema** 和 **host** 不區分大小寫。 例如：

- "http://contoso.com" 篩選符合 "HTTP://contoso.com"、"http://contoso.COM" 和 "http://contoso.com"

**path** 和 **query** 區分大小寫。 例如：

- "http://contoso.com/path?query=A" 篩選不符合 "http://contoso.com/Path?query=A" 或 "http://contoso.com/path?Query=A"。 但符合 "http://contoso.COM/path?query=A"。

## 內容授權

> [!NOTE]
> 本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。 原始 [Chromium 頁面可在此處](https://www.chromium.org/administrators/url-blacklist-filter-format)找到。
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
