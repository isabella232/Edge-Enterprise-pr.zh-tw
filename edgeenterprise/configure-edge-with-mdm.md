---
title: 使用行動裝置管理設定 Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用行動裝置管理設定 Microsoft Edge。
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979457"
---
# 使用行動裝置管理設定 Microsoft Edge

本文介紹如何透過 [ADMX 擷取](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)，使用[行動裝置管理 (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) 來設定 Windows 10 上的 Microsoft Edge。 本文的其他內容：

- 如何[為 Microsoft Edge 原則建立開放行動聯盟統一資源識別元 (OMA-URI)](#create-an-oma-uri-for-microsoft-edge-policies)。
- 如何[使用 ADMX 擷取和自訂 OMA-URI 在 Intune 中設定 Microsoft Edge](#configure-microsoft-edge-in-intune-using-admx-ingestion)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## 必要條件

Windows 10，具有下列最低系統需求︰

- Windows 10 版本 1903，需安裝 [KB4512941](https://support.microsoft.com/help/4512941/) 和 [KB4517211](https://support.microsoft.com/help/4517211/)
- Windows 10 版本 1809，需安裝 [KB4512534](https://support.microsoft.com/help/4512534/) 和 [KB4520062](https://support.microsoft.com/help/4520062/)
- Windows 10 版本 1803，需安裝 [KB4512509](https://support.microsoft.com/help/4512509/) 和 [KB4519978](https://support.microsoft.com/help/4519978)
- Windows 10 版本 1709，需安裝 [KB4516071](https://support.microsoft.com/help/4516071/) 和 [KB4520006](https://support.microsoft.com/help/4520006)

## 概觀

您可以使用 MDM 與偏好的企業行動管理 (EMM) 或支援 [ADMX 擷取](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)的 MDM 提供者來設定 Windows 10 上的 Microsoft Edge。

使用 MDM 設定 Microsoft Edge 有兩個程序：

1. 將 Microsoft Edge ADMX 檔案擷取到 EMM 或 MDM 提供者。 如需如何擷取 ADMX 檔案的指令，請洽詢您的提供者。

   > [!NOTE]
   > 對於 Microsoft Intune，請參閱[使用 ADMX 擷取在 Intune 中設定 Microsoft Edge](#configure-microsoft-edge-in-intune-using-admx-ingestion)。

2. [為 Microsoft Edge 原則建立 OMA-URI](#create-an-oma-uri-for-microsoft-edge-policies)。

## 為 Microsoft Edge 原則建立 OMA-URI

以下各節介紹如何建立 OMA-URI 路徑，以及如何查詢和定義用於強制和建議的瀏覽器原則的 XML 格式的值。

在開始之前，請[從 Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (MicrosoftEdgePolicyTemplates.cab)，並解壓縮內容。

定義 OMA-URI 有三個步驟：

1. [建立 OMA-URI 路徑](#create-the-oma-uri-path)
2. [指定 OMA-URI 資料類型](#specify-the-data-type)
3. [設定 OMA-URI 值](#set-the-value-for-a-browser-policy)

### 建立 OMA-URI 路徑

使用以下公式作為建立 OMA-URI 路徑的指南。 <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| 參數         | 描述                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | 使用 "Edge" 或擷取系統管理範本時定義的內容。 例如，如果您使用 "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx"，則使用 "MicrosoftEdge"。<br/><br/> `<ADMXIngestionName>` 必須與擷取 ADMX 檔案時使用的內容相符。 |
| \<ADMXNamespace>  | "microsoft_edge" 還是 "microsoft_edge_recommended"，取決於您設定的是強制還是建議原則。 |
| \<ADMXCategory>   | 原則的 "parentCategory" 在 ADMX 檔案中定義。 如果原則未分組 (未定義 "parentCategory")，則省略 `<ADMXCategory>`。 |
| \<PolicyName>     | 可在[瀏覽器原則參考](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies)文章中找到原則名稱。 |

#### URI 路徑範例：

在此範例中，假設 `<ADMXIngestName>` 節點名為 "Edge"，並且您正在設定強制原則。 URI 路徑為：<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

如果原則不在群組中 (例如，DiskCacheSize) 則移除 "`~<ADMXCategory>`"。 將 `<PolicyName>` 替換為原則名稱 DiskCacheSize。 URI 路徑為：<br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

如果原則位於群組中，請按照以下步驟操作：

1. 使用任何 xml 編輯器開啟 **msedge.admx**。
2. 搜尋要設定的原則名稱。 例如，"ExtensionInstallForceList"。
3. 使用 *parentCategory* 元素中 *ref* 屬性的值。 例如，來自 \<parentCategory ref=" Extensions"/> 的「延伸模組」。
4. 將 `<ADMXCategory>` 替換為建構 URI 路徑的 *ref* 屬性值。 URI 路徑為：<br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### 指定資料類型

OMA-URI 資料類型一律為 "String"。

### 設定瀏覽器原則的值

本節介紹如何為每個資料類型設定 XML 格式的值。 移至[瀏覽器原則參考](https://docs.microsoft.com/deployedge/microsoft-edge-policies)以查詢原則的資料類型。

> [!NOTE]
> 對於非布林資料類型，值開頭一律為 `<enabled/>`。

#### 布林值資料類型

對於布林類型的原則，請使用 `<enabled/>` 或 `<disabled/>`。

#### 整數資料類型

值一律需開頭為 `<enabled/>` 元素，後接 `<data id="[valueName]" value="[decimal value]"/>`。

若要尋找新索引標籤頁面的值名稱和十進位值，請使用以下步驟：

1. 使用任何 xml 編輯器開啟 **msedge.admx**。
2. 搜尋名稱屬性符合您要設定之原則名稱的 `<policy>` 元素。 對於 "RestoreOnStartup"，請搜尋 `name="RestoreOnStartup"`。
3. 在 `<elements>` 節點中，尋找您希望設定的值。
4. 使用 `<elements>` 節點中 "valueName" 屬性的值。 對於 "RestoreOnStartup"，"valueName" 是 "RestoreOnStartup"。
5. 使用 `<decimal>` 節點中 "value" 屬性的值。 對於 "RestoreOnStartup" 開啟新的索引標籤頁面，值為 "5"。

若要在啟動時開啟新的索引標籤頁面，請使用：<br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### 字串清單資料類型

值一律需開頭為 `<enabled/>` 元素，後接 `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`。

> [!NOTE]
> "id=" 屬性名稱不是原則名稱，儘管在大多數情況下它與原則名稱相符。 它是 \<list> 節點識別碼屬性值，可在 ADMX 檔案中找到。

若要尋找 listID 並定義封鎖 URL 的值，請按照以下步驟操作：

1. 使用任何 xml 編輯器開啟 **msedge.admx**。
2. 搜尋名稱屬性與要設定的原則名稱相符的 `<policy>` 元素。 對於 "URLBlocklist"，搜尋 `name="URLBlocklist"`。
3. 使用 `<list> node for [listID]` 的 "id" 屬性的值。
4. "value" 是由分號 (;) 分隔的 URL 清單

例如，若要封鎖對 `contoso.com` 和 `https://ssl.server.com` 的存取：<br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### 字典或字串資料類型

值一律需開頭為 `<enabled/>`，後接 `<data id="[textID]" value="[string]"/>`。

若要尋找 textID 並定義設定地區設定的值，請按照以下步驟操作：

1. 使用任何 xml 編輯器開啟 **msedge.admx**。
2. 搜尋名稱屬性與要設定的原則名稱相符的 `<policy>` 元素。 對於 "ApplicationLocaleValue"，請搜尋 `name="ApplicationLocaleValue"`。
3. 使用 `[textID]` 的 `<text>` 節點 "id" 屬性的值。
4. 設定文化特性代碼的 "value"。

若要使用 "ApplicationLocaleValue" 原則將地區設定設定為 "es-US"：<br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### 為建議的原則建立 OMA-URI

為建議原則定義 URI 路徑取決於您要設定的原則。

#### 定義建議原則的 URI 路徑

使用 URI 路徑公式 (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) 和以下步驟來定義 URI 路徑：

1. 使用任何 xml 編輯器開啟 **msedge.admx**。
2. 如果要設定的原則不在群組中，請跳到步驟 4 並從路徑中移除 `~<ADMXCategory>`。
3. 如果要設定的原則位於群組中：

   - 若要查詢 `<ADMXCategory>`，請搜尋您要設定的原則。 搜尋時，將 "_recommended" 附加到原則名稱中。 例如，搜尋 "RegisteredProtocolHandlers_recommended" 具有以下結果：

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - 從 `<parentCategory>` 元素複製 *ref* 屬性的值。 對於 "ContentSettings"，請從 `<parentCategory ref=" ContentSettings_recommended"/>` 複製 "ContentSettings_recommended"。
   - 將 `<ADMXCategory>` 替換為在 URI 路徑公式中建構 URI 路徑的 *ref* 屬性值。

4. `<PolicyName>` 是原則的名稱，並附加了 "_recommended"。

#### 建議原則的 OMA-URI 路徑範例

下表顯示了建議原則的 OMA-URI 路徑範例。

|              原則               |             OMA-URI                      |
|-----------------------------------|------------------------------------------|
| [RegisteredProtocolHandlers](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [PasswordManagerEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [PrintHeaderFooter](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [SmartScreenEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [HomePageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [FavoritesBarEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### OMA-URI 範例

OMA-URI 範例及其 URI 路徑、類型和範例值。

#### 布林值資料類型範例

*[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton)：*

| 欄位   | 值                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: ShowHomeButton                                                       |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| type    | String                                                                               |
| Value   | `<enabled/>`                                                                          |

*[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled)：*

| 欄位   | 值                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DefaultSearchProviderEnabled                                         |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| type    | String                                                                               |
| Value   | `<disable/>`                                                                          |

### 整數資料類型範例

*[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun)：*

| 欄位   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: AutoImportAtFirstRun                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| type    | String                                                                               |
| Value   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting)：*

| 欄位   | 值                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DefaultImagesSetting                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| type    | String                                                                               |
| Value   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize)：*

| 欄位   | 值                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: DiskCacheSize                                                        |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| type    | String                                                                               |
| Value   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### 字串清單資料類型範例
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS)：*

| 欄位   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: RestoreOnStartupURLS                                                 |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br>對於多重清單項目： `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist)：*

| 欄位   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: ExtensionInstallForcelist                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### 字典和字串資料類型範例

*[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode)：*

| 欄位   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: ProxyMode                                                            |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## 使用 ADMX 擷取在 Intune 中設定 Microsoft Edge

使用 Microsoft Intune 設定 Microsoft Edge 的建議方法是使用系統管理範本設定檔，如[使用 Microsoft Intune 設定 Microsoft Edge 原則設定](https://docs.microsoft.com/deployedge/configure-edge-with-intune)中所述。 如果要評估 Intune 中 Microsoft Edge 系統管理範本中目前未提供的原則，則可以使用 [Intune 中 Windows 10 裝置的自訂設定](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)來設定 Microsoft Edge。

本節說明如何：

1. [將 Microsoft Edge ADMX 檔案擷取至 Intune](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [在 Intune 中使用自訂 OMA-URI 設定原則](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> 最佳做法是，不要使用自訂 OMA-URI 設定檔和系統管理範本設定檔在 Intune 中設定相同的 Microsoft Edge 設定。 如果使用自訂 OMA-URI 和系統管理範本設定檔部署同一原則，但具有不同的值，使用者會獲得不可預知的結果。 在使用系統管理範本設定檔之前，我們強烈建議移除 OMA-URI 設定檔。

### 將 Microsoft Edge ADMX 檔案擷取至 Intune

本節介紹如何將 Microsoft Edge 系統管理範本 (**msedge.admx** 檔案) 擷取至 Intune。

> [!WARNING]
> 在擷取檔案之前，不要修改 ADMX 檔案。

若要擷取 ADMX 檔案，請依照下列步驟執行︰

1. 從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (MicrosoftEdgePolicyTemplates.cab)，並解壓縮內容。 您要擷取的檔案是 **msedge.admx**。
2. 登入 [Microsoft Azure 入口網站](https://portal.azure.com)。
3. 從_所有服務_中選取 **Intune**，或在入口網站搜尋方塊中搜尋 Intune。
4. 從 _Microsoft Intune - 概觀_中，選取**裝置設定** | **設定檔**。
5. 在頂端命令列上，選取 **+ 建立設定檔**。

   ![建立裝置設定檔](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. 提供以下設定檔資訊：

   - **名稱**：輸入描述性名稱。 對於此範例，為「Microsoft Edge ADMX 擷取的設定」。
   - **描述**：輸入設定檔的選用描述。
   - **平台**：選取 [Windows 10 和更新版本]
   - **設定檔類型**：選取 [自訂]

7. 在**自訂 OMA-URI 設定**上，按一下**新增**以新增 ADMX 擷取。

   ![為 OMA-URI 新增擷取](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. 在**新增列**中提供下列資訊：

   - **名稱**：輸入描述性名稱。 對於此範例，使用 "Microsoft Edge ADMX 擷取"。
   - **描述**：輸入設定的選用描述。
   - **OMA-URI**：輸入 "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"
   - **資料類型**：選取 [字串]。
   - **值**：在選取**資料類型**後，將顯示此輸入區域。 開啟您在步驟 1 中解壓縮的 Microsoft Edge 原則範本檔案中的 msedge.admx 檔案。 複製 msedge.admx 檔案中的**所有文字**，並將其貼到以下螢幕截圖中顯示的**值**文字區域中。

        ![新增 ADMX 擷取](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - 按一下**確定**。

9. 在**自訂 OMA-URI 設定**上，按一下**確定**。
10. 在**建立設定檔**上，按一下**建立**。 下一個螢幕截圖顯示有關新建立設定檔的資訊。

    ![新裝置設定檔資訊 ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### 在 Intune 中使用自訂 OMA-URI 設定原則

> [!NOTE]
> 在使用本節中的步驟之前，您必須先完成[將 Microsoft Edge ADMX 檔案擷取至 Intune](#ingest-the-microsoft-edge-admx-file-into-intune)中描述的步驟。

1. 登入 [Microsoft Azure 入口網站](https://portal.azure.com)。
2. 從_所有服務_中選取 **Intune**，或在入口網站搜尋方塊中搜尋 Intune。
3. 移至 **Intune**>**裝置設定**>**設定檔**。
4. 選取「Microsoft Edge ADMX 擷取的設定」設定檔或您用於設定檔的名稱。
5. 若要新增 Microsoft Edge 原則設定，您必須開啟**自訂 OMA-URI 設定**。 在**管理**下方，依序按一下**內容**和**設定**。

    ![設定設定檔設定](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. 在**自訂 OMA-URI 設定**下，按一下**新增**。

    ![新增列至 OMA-URI 設定](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. 在 **新增列**中提供下列資訊：

   - **名稱**：輸入描述性名稱。 我們建議使用您要設定的原則名稱。 對於此範例，使用 "ShowHomeButton"。
   - **描述** (選用)：輸入設定的選用描述。
   - **OMA-URI**：輸入原則的 OMA-URI。 使用 "ShowHomeButton" 原則作為範例，使用此字串："*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"
   - **資料類型**：選取原則設定資料類型。 對於 "ShowHomeButton" 原則，使用 [字串]
   - **值**：輸入要為原則設定的設定。 對於 "ShowHomeButton" 範例，輸入 "\<enabled/>"。 下列螢幕擷取畫面顯示設定原則的設定。

        ![新增列、自訂 OMA-URI 設定](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - 按一下**確定**。

8. 在**自訂 OMA-URI 設定**下，按一下**新增**。
9. 在**Microsoft Edge ADMX 擷取的設定 - 內容**設定檔 (或您使用的名稱) 上，按一下**儲存**。

建立設定檔並設定屬性後，您必須[在 Microsoft Intune 中指派設定檔](https://docs.microsoft.com/intune/configuration/device-profile-assign)。

#### 確認原則已設定

使用以下步驟確認 Microsoft Edge 原則是否正在使用您建立的設定檔。 (請給 Microsoft Intune 一點時間，將原則傳播到您在「Microsoft Edge ADMX 擷取的設定」設定檔範例中指派的裝置。)

1. 開啟 Microsoft Edge，然後移至 *edge://policy*。
2. 在"**原則"** 頁面上，查看是否列出了您在設定檔中設定的原則。
3. 如果未顯示原則，請參閱[診斷 Windows 10 中的 MDM 失敗](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10)或[疑難排解原則設定](#troubleshoot-a-policy-setting)。

#### 疑難排解原則設定

如果 Microsoft Edge 原則未生效，請嘗試以下步驟：

開啟目標裝置上的 *edge://policy* 頁面 (您在 Microsoft Intune 中指派設定檔的裝置) 並搜尋原則。 如果原則不在 *edge://policy* 頁面上，請嘗試以下操作：

- 檢查原則是否位於登錄中且是否正確。 在目標裝置上開啟 Windows 10 登錄編輯程式 (**Windows 鍵 + r**，輸入「*regedit*」，然後按 **Enter**)。檢查原則是否在 *\Software\Policies\ Microsoft\Edge* 路徑中正確定義。 如果在預期路徑中找不到原則，則原則未正確推送到裝置。
- 檢查 OMA-URI 路徑是否正確，並且該值是有效的 XML 字串。 如果其中任一不正確，則原則不會推送到目標裝置。

如需更多疑難排解祕訣，請參閱[設定 Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps)和[同步裝置](https://docs.microsoft.com/intune/remote-actions/device-sync)。

## 也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [使用 Microsoft Intune 設定 Microsoft Edge 原則設定](configure-edge-with-intune.md)
- [行動裝置管理](https://docs.microsoft.com/windows/client-management/mdm/)
- [使用 Intune 中 Windows 10 裝置的自訂設定](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [Win32 與傳統型橋接器應用程式原則設定](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [了解 ADMX 支援的原則](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
