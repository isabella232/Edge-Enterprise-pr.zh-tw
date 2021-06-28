---
title: 建立 Microsoft Edge 使用者資料目錄變數
ms.author: brianalt
author: AndreaLBarr
manager: srugh
ms.date: 04/21/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何建立 Microsoft Edge 使用者資料目錄變數
ms.openlocfilehash: 5ec78f16c7e5cd43f01845f35b8473494cd0c4bf
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618059"
---
# <a name="create-microsoft-edge-user-data-directory-variables"></a>建立 Microsoft Edge 使用者資料目錄變數

本文介紹在修改 Microsoft Edge 時如何使用資料目錄變數，而不是使用硬式編碼路徑。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 77 或更新版本。
## <a name="path-variables"></a>路徑變數

用於修改資料目錄路徑的原則 (例如，設定 [UserDataDir](microsoft-edge-policies.md#userdatadir) 或 [DownloadDirectory](microsoft-edge-policies.md#downloaddirectory) 支援變數)。 設定這些原則時，可以使用變數來取代硬式編碼路徑。 例如，將您的設定檔資料儲存在 Windows 的使用者本機應用程式資料下，而不是預設位置。 將 [UserDataDir](microsoft-edge-policies.md#userdatadir) 原則設定為 **${local_app_data}\Edge\Profile**。 在大多數 Windows 10 安裝中，此路徑解析為 *C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\Profile*。

>[!NOTE]
>若要查看目前**設定檔路徑**，請開啟**關於版本**頁面 (鍵入 "edge://version")。 **設定檔路徑**遵循以下格式：*C:\Users\\&lt;Current-user&gt;\AppData\Local\Microsoft\Edge\User Data\Default*。

### <a name="guidance-for-using-path-variables"></a>使用路徑變數的指南

在使用路徑變數之前，請先查看以下指南。

- 涉及 Microsoft Edge 儲存不同資料之路徑的所有原則，都與平台相關。 某些原則僅可用於特定平台，而其他原則可在所有平台上使用。
- 為了避免應用程式在不同場合從不同位置啟動而導致錯誤，請確保路徑是絕對的。
- 每個變數只能在路徑中出現一次。 對於大多數變數來說，這是使用變數的唯一有意義方法，因為它們解析為絕對路徑。
- 如果路徑不存在，幾乎所有原則都會建立該路徑 (在現有情況下如果可能)。
- 由於 Microsoft Edge 不同版本/通道處理資料夾結構的方式不同，因此在某些原則中使用網路位置可能會導致意外的結果。

### <a name="supported-path-variables"></a>支援的路徑變數

Microsoft Edge 支援以下路徑變數。

#### <a name="all-platforms"></a>所有平台

| 變數 | 描述 |
| --- | --- |
| **${user_name}** | 正在使用 Microsoft Edge 的使用者。 Microsoft Edge 遵循 SUID (設定執行時的擁有者使用者 ID) 範例：*audreysmall* |
| **${machine_name}** | 電腦名稱稱，可能包括網域名稱。 範例：*audreysmall* or *audrey.ex.contoso.com* |

#### <a name="windows-only"></a>僅限 Windows

| 變數 | 描述 |
| --- | --- |
| **${documents}** | 目前使用者的文件資料夾。 範例：*C:\Users\Administrator\Documents* |
|**${local_app_data}** | 目前使用者的 [應用程式資料] 資料夾。 範例：*C:\Users\Administrator\AppData\Local* |
|**${roaming_app_data}** | 目前使用者的 [漫遊應用程式資料] 資料夾。 範例：*C:\Users\Administrator\AppData\Roaming* |
| **${profile}** | 目前使用者的主資料夾。 範例：*C:\Users\Administrator* |
| **${global_app_data}** | 系統範圍的應用程式資料資料夾。 範例：*C:\AppData* |
| **${program_files}** | 目前處理序的程式檔案資料夾。 此資料夾取決於它是 32 位元還是 64 位元處理序。 範例解析：*C:\Program Files (x86)* |
| **${windows}** | Windows 資料夾。 範例：*C:\Windows* |
| **${client_name)** | 連接到 RDP 或 Citrix 工作階段的用戶端電腦的名稱。 如果從本機工作階段使用，則此變數為空。 如果用於路徑中，請用保證不為空的項目來做為它的首碼。 範例：*C:\edge_profiles\session_${client_name}* 解析為 *C:\edge_profiles\session_&lt;ForlocalSessions&gt;* 且 *C:\edge_profiles\session_&lt;SomePCname&gt;* 用於遠端工作階段。 |
| **${session_name}** | 使用中工作階段的名稱。 使用此名稱可區分使用單一使用者設定檔的多個同時連接的遠端工作階段。 範例：*WinSta0 for local desktop sessions* |

#### <a name="macos-only"></a>僅限 macOS

| 變數 | 描述 |
| --- | --- |
| **${users}** | 儲存使用者設定檔的資料夾。 範例：*/Users* |
| **${documents}** | 目前使用者的文件資料夾。 範例：*/Users/audreysmall/Documents* |

## <a name="content-license"></a>內容授權

>[!NOTE]
>本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。 原始頁面可在[此處](https://www.chromium.org/administrators/policy-list-3/user-data-directory-variables)找到。
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br/>本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。
## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)