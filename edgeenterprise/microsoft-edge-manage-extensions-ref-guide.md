---
title: ExtensionSettings 原則的詳細指南
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 ExtensionSettings 原則設定 Microsoft Edge 擴充功能的詳細參考指南。
ms.openlocfilehash: 3660910a252377efe8dff47dec8f811ecdd2018e
ms.sourcegitcommit: b67ebf9a68205407f5eaec343cb0722cfdd17396
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/04/2021
ms.locfileid: "12061102"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a>ExtensionSettings 原則的詳細指南

Microsoft Edge 提供多種管理擴充功能的方法。 一般的方法就是使用 JSON 字串在 Windows 群組原則編輯器或 Windows 登錄中，在單一位置使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則設定多個策原則。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="before-you-begin"></a>開始之前

您可以決定是否要在這裡設定所有擴充功能管理設定，或透過其他原則設定這些控制項。
  
ExtensionSettings 原則可以覆寫您設定在群組原則中其他位置的其他原則，包括下列原則：

- [ExtensionAllowedTypes](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ExtensionInstallSources](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a>ExtensionSettings 原則欄位

此原則可以控制設定，例如更新 URL、可從其中下載擴充功能進行初次安裝，以及封鎖權限，或不允許執行哪些權限。 下表說明可用的原則欄位。

| &nbsp; | 說明 |
|--|--|
| **allowed_types** | 只能用來設定預設設定 *。 指定允許使用者在 Microsoft Edge 上安裝的應用程式或擴充功能。 該值是字串清單，每個字串應該為下列其中一種類型：「extension」、「theme」、「user_script」和「hosted_app」。   |
| **blocked_install_message**| 如果您封鎖使用者安裝特定擴充功能，您可以指定自訂訊息，如果使用者嘗試安裝，該訊息會在瀏覽器中顯示。<br>將文字附加到 Microsoft Edge 外掛程式網站上顯示的一般錯誤訊息文字。 例如，您可以告訴使用者如何與 IT 部門連絡，或特定擴充功能無法使用的原因。 訊息最多 1,000 個字元。   |
|**blocked_permissions**  | 防止使用者安裝及執行要求貴組織不允許之特定 API 權限的擴充功能。 例如，您可以封鎖存取 Cookie 的擴充功能。 如果擴充功能需要您封鎖的權限，使用者無法安裝擴充功能。 如果使用者先前已安裝擴充功能，它將不再載入。 如果擴充功能包含封鎖的權限為選擇性需求，它會如往常一樣安裝。 接著，當擴充功能執行時，系統會自動拒絕封鎖的權限。<br>有關可用權限的清單，請參閱[宣告權限](/microsoft-edge/extensions-chromium/enterprise/declare-permissions)。   |
| **installation_mode**| 控制您指定的擴充功能是否及如何新增到 Microsoft Edge。 您可以將安裝模式設定為下列其中一個選項：<br>- allowed：使用者可以安裝擴充功能。 如果未定義安裝模式，則此設定為預設值。<br>- blocked：使用者無法安裝擴充功能。<br>- force_installed：自動安裝擴充功能，而不需要使用者互動。 使用者無法移除擴充功能。 您也需要使用 update_url 定義擴充功能下載位置。 **注意**：此設定無法使用 *，因為Microsoft Edge 無法知道要自動安裝哪個擴充功能。<br>- normal_installed：自動安裝擴充功能，而不需要使用者互動。 使用者可以停用此功能。 您也需要使用 update_url 定義擴充功能下載位置。 **注意**：此設定無法使用 *，因為Microsoft Edge 無法知道要自動安裝哪個擴充功能。<br>- removed：使用者無法安裝擴充功能。 如果使用者先前已安裝擴充功能，Microsoft Edge 會將其移除。 |  |
| **install_sources** | 只能用來設定預設設定 *。 指定允許安裝擴充模組的 URL。 這些模式必須同時允許 *.crx 檔案的位置，以及開始下載網頁的位置 (查閱者)。 有關 URL 模式範例，請參閱[符合模式](/microsoft-edge/extensions-chromium/enterprise/match-patterns)。  |
| **minimum_version_required** |Microsoft Edge 停用擴充功能，包括強制安裝的擴充功能，其版本比指定的最低版本還要舊。<br>版本字串的格式與擴充功能資訊清單中使用的格式相同。     |
| **update_url** | 僅適用於  force_installed and normal_installed。 指定 Microsoft Edge 擴充功能的下載位置。 如果擴充功能是託管在 Microsoft Edge 外掛程式網站中，請使用此位置：`https://edge.microsoft.com/extensionwebstorebase/v1/crx`。<br>Microsoft Edge 會使用您為初始擴充安裝指定的 URL。 對於後續的擴充功能更新，Microsoft Edge 的擴充功能資訊清單中使用該 URL。   |
| **runtime_allowed_hosts**| 允許擴充功能與指定的網站互動，即使它們也是在 runtime_blocked_hosts 中定義。 您可以指定最多 100 個項目。 系統會捨棄額外的項目。<br>主機模式格式與 [符合模式](/microsoft-edge/extensions-chromium/enterprise/match-patterns)類似， 但無法定義路徑。 例如：<br>- *://*.example.com<br>- *://example。*—支援 eTLD 萬用字元     |
| **runtime_blocked_hosts**| 防止擴充功能與您指定的網站互動或修改。 修改包括封鎖 JavaScript 注入、Cookie 存取，以及 Web 要求修改。<br>您可以指定最多 100 個項目。 系統會捨棄額外的項目。<br>主機模式格式與符合模式類似，但無法定義路徑。 例如：<br>- *://*.example.com<br>- *://example。*—支援 eTLD 萬用字元   |
| **override_update_url**| 可從 Edge 93 使用<br>如果設定為 `true` ，Edge 會使用 ExtensionSettings 策略或 ExtensionInstallForcelist 策略中指定的更新 URL，以用於後續的擴充更新。<br>如果未設定或設定為 ，Edge 會使用副檔名清單中指定的 URL `false` 進行更新。|
| **toolbar_state**| 可從 Edge 94 使用<br>此策略設定可讓您強制顯示工具列已安裝的擴充功能。 預設狀態適用于 `default_shown` 所有擴充功能。 此設定可能遵循下列狀態<br>-`force_shown`：您可以選擇強制在工具列上顯示已安裝的擴充功能。 使用者將無法從工具列中隱藏特定的擴充圖示。<br>-`default_hidden`：在此狀態中，副檔名會從安裝時工具列中隱藏。 如有必要，使用者可以在工具列上顯示它們。<br>-`default_shown`：這是瀏覽器上所有已安裝的擴充模組的聽障設定。

以下為全域範圍 * (允許) ： 

- blocked_permissions
- installation_mode - 只有'封鎖'、'允許'或'已移除'在此範圍內是有效的值。
- runtime_blocked_hosts
- blocked_install_message
- allowed_types
- runtime_allowed_hosts
- install_sources

這些是個別擴充範圍中允許的按鍵： 

- blocked_permissions
- minimum_version_required
- blocked_install_message
- toolbar_state (Edge 94) 
- installation_mode `"blocked"` - `"allowed"` `"removed"` 、、、及 `"force_installed"` `"normal_installed"` 為可能的值。
- runtime_allowed_hosts
- update_url
- override_update_url
- runtime_blocked_hosts
- toolbar_state

這些是更新 URL 範圍中允許的按鍵： 

- blocked_permissions
- installation_mode - 僅 `"blocked"` ， `"allowed"` `"removed"` 或在此範圍中是有效的值。

## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a>在 Windows 群組原則編輯器中使用 JSON 字串進行設定

使用 GPO 使用擴充功能設定原則的步驟假設您已針對 Microsoft Edge 原則匯入 ADM/ADMX。

1. 開啟群組原則編輯器，然後前往 **[Microsoft Edge] > [擴充功能] > [設定擴充功能管理設定原則]**。
2. 啟用該原則，並在文字方塊中輸入其精簡的 JavaScript 物件標記法 (JSON) 資料做為一行，沒有分行符號。
3. 若要驗證該原則，並精簡成單行，請使用 JSON 壓縮工具。

### <a name="properly-format-json-for-the-extension-settings-policy"></a>正確設定 JSON 擴充功能設定原則的格式

您必須了解此原則的兩個部分：預設範圍和個別範圍。 預設範圍是包含所有的擴充功能，而沒有自己的範圍。 個別範圍只會套用該擴充功能。  

預設範圍是由星號 (*) 識別。 下一個範例會定義預設範圍和個別擴充功能範圍。

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

擴充功能只會從一個範圍取得其設定。 如果該擴充功能有個別的擴充功能範圍，這些會是套用到該擴充功能的設定。 如果沒有個別的擴充範圍，則擴充功能會使用預設範圍。  

下一個 JSON 範例會封鎖任何擴充功能在 `.example.com` 上執行，並封鎖任何需要 「USB」權限的擴充功能。

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**精簡 JSON**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a>其他一些 JSON 擴充功能設定的範例

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a>使用 installation_mode 屬性來允許和封鎖擴充功能

- 使用者可以安裝所有擴充功能 - 這是預設設定 

  `{ "*": {"installation_mode": "allowed" }}`
- 使用者無法安裝任何擴充功能。  

  `{ "*": {"installation_mode": "blocked" }}`

- 指定在安裝被封鎖時要顯示的自訂訊息。

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a>使用 installation_mode 屬性強制安裝擴充功能

當使用 installation_mode 做為「force_installed」時，系統會自動安裝擴充功能，而不需要使用者互動。 使用者無法停用或移除擴充功能。 如果已安裝「標準」或「強制」擴充功能，**，update_url** 欄位也必須定義。 此欄位指向可安裝擴充功能的位置。 針對 **update_url** 欄位，請使用下列位置：

- 如果您下載的擴充功能是託管在 Microsoft Edge 外掛程式市集，請使用 [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx)。
- 如果您下載的擴充功能是託管在 Chrome 線上應用程式商店，請使用 [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx)。
- 如果您是在您自己的伺服器上託管擴充功能，請使用 Microsoft Edge 可下載的已封裝擴充功能 (.crx 檔案) 之 URL。 JSON 範例：

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
在上例中，如果您改為使用「normal_installed」而不是「force_installed」，系統會自動安裝擴充功能，而不需要使用者互動，但可以停用擴充功能。  

   > [!TIP]
   > 正確格式化 JSON 字串可能相當棘手。 在實作原則之前，請使用 JSON 檢查程式。 或者，試用最新版本的[擴充功能設定產生工具](https://microsoft.github.io/edge-extension-settings-generator/minimal)

## <a name="configure-using-the-windows-registry"></a>使用 Windows 登錄進行設定

ExtensionSettings 原則應寫入此機碼下的登錄：

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> 您可以使用 HKCU 而非 HKLM。 對等路徑可以使用群組原則物件 (GPO) 進行設定。  

針對 Microsoft Edge，所有設定都會在此機碼下開始：

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

下一個要建立的機碼是個別範圍的擴充功能識別碼或預設範圍的星號 (*)。 例如，您可以使用下列位置套用到 Google Hangouts 的設定：

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

針對套用到預設範圍的設定，請使用這個位置：

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

不同的設定會要求不同的格式，視其為字串或字串陣列而不同。 陣列值需要 [＂value＂]。 字串值可以以目前格式輸入。 下列清單顯示哪些設定是陣列或字串：

- Installation_mode = 字串
- update_url = 字串
- blocked_permissions = 字串陣列
- allowed_permissions = 字串陣列
- minimum_version_required = 字串
- runtime_blocked_hosts = 字串陣列
- runtime_allowed_hosts = 字串陣列
- blocked_install_message = 字串


## <a name="see-also"></a>另請參閱

- [管理企業中的 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions.md)
- [使用群組原則管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)
- [Microsoft Edge 擴充功能常見問題集](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
