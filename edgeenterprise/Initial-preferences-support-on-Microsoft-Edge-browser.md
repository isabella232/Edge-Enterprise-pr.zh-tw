---
title: 瀏覽器上的初始喜好設定Microsoft Edge支援
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/27/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 瀏覽器上的初始喜好設定Microsoft Edge支援。
ms.openlocfilehash: 7a497fd2f3305b0c027a396936ef86bacbcb5b20
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978851"
---
# <a name="configure-microsoft-edge-using-initial-preferences-settings-for-the-first-run"></a>使用初次執行的 [初始喜好設定]，設定 Microsoft Edge

使用下列資訊來設定Microsoft Edge裝置上的初始喜好設定Windows設定。

> [!Note]
> 本文適用于Microsoft Edge版本 93 或更新版本。

## <a name="configure-policy-settings-on-windows"></a>在 Windows 上進行原則設定

從 Microsoft Edge 93 開始，Microsoft 支援數量有限的初始喜好設定 ，前稱「主喜好設定」，協助系統管理員設定第一次執行瀏覽器;請參閱下方支援的設定清單。  

部署時，初始喜好設定會做為受管理裝置上的預設瀏覽器設定;這些是系統管理員偏好用來做為預設值的設定，但使用者可以變更，或某些裝置無法使用這些設定，因為它們未加入 Active Directory® 網域。

部分 Intial 喜好設定範例包括預設首頁的初始設定或具有特定 URL 的定位停駐點。

喜好設定只會從initial_preferences複製一次，且在設定之後對此檔案進行的任何變更都會受到尊重。 如果設定是由 Microsoft Edge[管理](/deployedge/microsoft-edge-policies)，initial_preferences檔案中設定，則該策略一initial_preferences優先。

以下是您目前支援的喜好設定清單Microsoft Edge：

| 喜好設定類別 | 設定 |
| - | - |
| Bookmark_bar | show_apps_shortcut<br>show_managed_bookmarks<br>show_on_all_tabs |
| 書籤 | editing_enabled |
| 瀏覽器/clear_data | browsing_history<br>browsing_history_basic"<br>緩存<br>cache_basic<br>餅乾<br>download_history<br>form_data<br>密碼 |
| 歷程記錄 | browsing_history<br>緩存<br>餅乾<br>download_history<br>form_data<br>hosted_apps_data<br>密碼<br>site_settings |
| 瀏覽器 | first_run_tabs<br>dark_theme<br>show_toolbar_bookmarks_button<br>show_toolbar_collections_butto<br>show_toolbar_downloads_button<br>show_home_button<br>show_prompt_before_closing_tabs<br>show_toolbar_history_button |
| default_search_provider | [default_search_provider] 已啟用 |
| 全螢幕 | 允許 |
| 首頁 | Homepage_url |
| homepage_is_newtabpage | homepage_is_newtabpage |
| 會話 | restore_on_startup<br>startup_urls |
| Extensions | 擴充功能 ：設定 |

## <a name="1-download-an-example-initial_preferences-file"></a>1：下載檔案initial_preferences範例

若要開始使用，請從登陸頁面下載[「Microsoft Edge Enterprise」檔案](https://www.microsoft.com/edge/business/download)。 解壓縮檔案，然後開啟 `initial_preferences` 資料夾中 `examples` 的檔案。

## <a name="2-customize-and-validate-the-initial_preferences-file"></a>2：自訂及驗證initial_preferences檔案

在下載的檔案中自訂 *initial_preferences* 設定，並驗證變更，以確保 JSON 程式碼沒有錯誤。 如果您發現錯誤，請檢查該檔案的語法initial_preferences結構，** 進行修正，然後再次驗證。 在 中驗證 JSON、Online [JSON 工具](https://jsonformatter.org/)或 JSON 編輯的範例工具[Visual Studio Code。](https://code.visualstudio.com/docs/languages/json)

## <a name="3-deploy-preferences-to-users-computer"></a>3：將喜好設定部署到使用者的電腦

在*initial_preferences*瀏覽器部署的同時，將檔案部署到使用者的裝置Microsoft Edge將檔案放在裝置上的下列位置。

### <a name="windows-amd64-and-arm64"></a>Windows (AMD64 和 ARM64) 

| 通道 | Location |
| - | - |
| Stable | `"C:\Program Files (x86)\Microsoft\Edge\Application"` |
| Beta | `"C:\Program Files (x86)\Microsoft\Edge Beta\Application"` |
|Canary | `"%LOCALAPPDATA%\Microsoft\Edge SxS\Application"` |
| Dev | `"C:\Program Files (x86)\Microsoft\Edge Dev\Application"` |

**注意***：initial_preferences*檔案必須部署至與使用者電腦上msedge.exe檔案相同的Windows資料夾。  

### <a name="macos"></a>macOS

| 通道 | Location |
| - | - |
| Stable | `"~/Library/Application Support/Microsoft Edge/Microsoft Edge Initial Preferences"` |
| Beta | `“~/Library/Application Support/Microsoft Edge Beta/Microsoft Edge Initial Preferences"` |
| Canary | `“~/Library/Application Support/Microsoft Edge Canary/Microsoft Edge Initial Preferences"` |
| Dev | `"~/Library/Application Support/Microsoft Edge Dev/Microsoft Edge Initial Preferences"` |

## <a name="important-notes-msi--pkg-deployment-and-initial_preferences-interaction"></a>重要注意事項：MSI / Pkg*部署initial_preferences互動*

初始喜好設定只會在使用者initial_preferences瀏覽器之前部署該檔案時生效。  

## <a name="see-also"></a>另請參閱

- [範例 *initial_prefrences* 範本檔案](https://www.microsoft.com/edge/business/download)
