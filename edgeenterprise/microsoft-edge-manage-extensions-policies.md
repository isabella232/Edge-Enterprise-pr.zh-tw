---
title: 使用群組原則管理 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 在企業中使用群組原則管理 Microsoft Edge 擴充功能
ms.openlocfilehash: dad239a448ec1f0ebef60c7072bfaad5c3baed57
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979393"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a>使用群組原則管理 Microsoft Edge 擴充功能

本文將說明使用群組原則管理擴充功能的選項和步驟。 這些選項假設您已經為使用者管理 Microsoft Edge。 如果您尚未設定要為使用者管理的 Microsoft Edge，請遵循下列連結立即進行。

- [在企業中管理 Microsoft Edge 的擴充功能](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="block-extensions-based-on-their-permissions"></a>根據擴充功能的權限封鎖擴充功能

您可以使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則，根據權限來控制使用者可以安裝的擴充功能。 如果已安裝的擴充功能需要的權限已遭封鎖，就不會執行該擴充功能。 不會移除擴充功能，只會停用。

> [!NOTE]
> 只能在擴充功能設定原則內設定遭封鎖的權限設定。  

使用下列步驟做為封鎖擴充功能的指南。

1. 開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]****，然後選取 [設定擴充功能管理設定]****。
2. 啟用該原則，然後使用壓縮的 JSON 字串輸入您想要允許或封鎖的權限。 下一個螢幕擷取畫面顯示如何封鎖使用 "usb" 權限的擴充功能。

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="設定群組原則以封鎖擴充功能。":::

下列範例顯示 JSON 以封鎖任何需要使用權限 "usb" 及其壓縮字串的擴充功能。

### <a name="json-example"></a>JSON 範例

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > 若要封鎖所有使用該權限的擴充功能，請使用星號作為擴充功能識別碼，如上一個範例所示。 如果您指定一個擴充識別碼，原則只會套用至該擴充功能。 您可以封鎖多個擴充功能，但這些擴充功能必須是個別項目。

## <a name="prevent-extensions-from-altering-web-pages"></a>防止擴充功能變更網頁

此設定可防止擴充功能讀取及變更來自敏感網站和網域的資料。 封鎖不想要的動作是透過封鎖以下動作來完成：指令碼插入您的網站、讀取 Cookie 或進行網路要求修改。 此設定不會阻止使用者安裝或移除擴充功能，只會防止擴充功能變更指定的網站。 
  
> [!NOTE]
> 只能在擴充功能設定原則內設定執行階段允許/封鎖主機設定。  

您可以在 ExtensionSettings 原則中設定下列設定，以防止 (或允許) 變更網站或網域：

- **Runtime_blocked_hosts**。 此設定會阻止擴充功能進行變更，或從您指定的網站讀取資料。
- **Runtime_allowed_hosts**。 此設定可允許擴充功能進行變更，或從您指定的網站讀取資料。 以下格式用於在原則的 JSON 字串中指定您的網站：

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` 區段為必要項目，但 `[subdomain|*]` 區段為選用。

下表顯示有效的主機模式和相符模式的範例。

|有效的主機模式|相符項目|不相符|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | 所有 URL  |   |

使用下列步驟做為封鎖或允許擴充功能存取網站或網域的指南。

1. 開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]****，然後選取 [設定擴充功能管理設定]****。  
2. 啟用該原則，然後輸入您想要允許或封鎖的權限，將權限壓縮為單一 JSON 字串。

下列範例顯示如何封鎖主機名稱上的擴充功能，以及如何封鎖同一個網域上的擴充功能。

### <a name="json-example-to-block-hostname"></a>封鎖主機名稱的 JSON 範例

此範例顯示 JSON 和壓縮的 JSON 字串，以封鎖任何擴充功能，禁止其存取 `www.microsoft.com` 主機名稱。

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> 若要封鎖所有擴充功能存取網頁，請使用星號作為擴充功能識別碼，如上一個範例所示。  如果您指定一個擴充識別碼而不指定星號，原則只會套用至該擴充功能。 您可以封鎖多個擴充功能，但這些擴充功能必須是個別項目。

### <a name="json-example-to-block-extensions-on-same-domain"></a>JSON 範例，可封鎖相同網域上的擴充功能

此範例顯示 JSON 和壓縮的 JSON 字串，以封鎖特定擴充功能在相同網域 "importantwebsite" 上執行。

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a>在群組原則中允許或封鎖擴充功能

您可以使用 [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) 和 [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) 原則來控制要封鎖或允許的擴充功能。 使用下列步驟做為指南，以允許所有擴充功能，除了您想要封鎖的擴充功能之外。

1. 開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]****，然後選取 [控制不能安裝哪些擴充程式]****。
2. 選取 [啟用]****。
3. 按一下 [顯示]****。
4. 輸入要封鎖之擴充功能的應用程式識別碼。 新增多個應用程式識別碼時，請針對每個識別碼使用個別列。
5. 若要封鎖所有擴充功能，請將 **\*** 輸入該原則，以防止安裝任何擴充功能。 您可以結合 [允許特定安裝擴充功能] 原則來使用這項功能，以只允許安裝特定擴充功能。 下一個螢幕擷取畫面顯示將根據提供的應用程式識別碼封鎖的擴充功能。

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="使用應用程式識別碼封鎖擴充功能。":::

   > [!TIP]
   > 如果您找不到擴充功能的應用程式識別碼，請查詢 Microsoft Edge 附加元件網站中的擴充功能。 找到特定的擴充功能，您將在 omnibox 的 URL 結尾看到應用程式識別碼。

> [!NOTE]
> 您可以在使用者電腦上安裝的封鎖清單中新增擴充功能。 這將停用擴充功能，並防止使用者重新啟用它。 不會解除安裝擴充功能，只會停用。

## <a name="force-install-an-extension"></a>強制安裝擴充功能

使用 [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) 原則來控制要封鎖或允許的擴充功能。 使用下列步驟做為強制安裝擴充功能的指南。

1. 在 [群組原則編輯器] 中，移至 [系統管理範本 > Microsoft Edge > 擴充功能]****，然後選取 [控制哪些擴充功能會默默地安裝]****。
2. 選取 [啟用]****。  
3. 按一下 [顯示]****。
4. 輸入要強制安裝的擴充功能的應用程式識別碼。  

擴充功能將自動安裝，不需要使用者介入。 使用者也將無法解除安裝或停用擴充功能。 此設定會覆寫任何已啟用的封鎖清單原則。

> [!NOTE]
> 對於在 Chrome線上應用程式商店中託管的擴充功能，請使用字串，例如：`pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`。

## <a name="block-extensions-from-a-specific-store-or-update-url"></a>封鎖來自特定商店或更新 URL 的擴充功能

若要封鎖來自特定商店或 URL 的擴充功能，您只需要使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則封鎖該商店的 *update_url* 即可。

使用下列步驟做為指南，以封鎖來自特定商店或 URL 的擴充功能。

1. 開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]****，然後選取 [設定擴充功能管理設定]****。  
2. 啟用該原則，然後輸入您想要允許或封鎖的權限，將權限壓縮為單一 JSON 字串。

下一個範例顯示 JSON 和壓縮的 JSON 字串，以使用其更新 URL (`https://clients2.google.com/service/update2/crx`) 封鎖 Chrome 線上應用程式商店。

### <a name="json-example-for-blocking-on-update-url"></a>封鎖更新 URL 的 JSON 範例

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> 您仍然可以使用 **ExtensionInstallForceList** 和 **ExtensionInstallAllowList** 來允許/強制安裝特定擴充功能，即使是在前一個範例中已使用 JSON 來封鎖商店。

## <a name="see-also"></a>另請參閱

- [在企業中管理 Microsoft Edge 的擴充功能](microsoft-edge-manage-extensions.md)
- [建立線上應用程式商店以託管 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-webstore.md)
- [ExtensionSettings 原則的參考指南](microsoft-edge-manage-extensions-ref-guide.md)
- [Microsoft Edge 擴充功能常見問題集](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
