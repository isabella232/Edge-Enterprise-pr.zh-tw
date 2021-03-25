---
title: 將副檔名與 Internet Explorer 模式建立關聯
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 12/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 將副檔名與 Internet Explorer 模式建立關聯
ms.openlocfilehash: 6c651499401757d9a58e697d1d019a7294bb5fa7
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447367"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a>將副檔名與 Internet Explorer 模式建立關聯

本文說明如何將 Microsoft Edge 與含桌面應用程式副檔名的 Internet Explorer 模式建立關聯。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 86 或更新版本。

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a>使用 Internet Explorer 模式的副檔名關聯指南

下列指示會顯示將 Microsoft Edge 與 IE 模式與 .mht 檔案類型相關聯的輸入。 若要設定檔案關聯，請使用下列步驟作為指南。

> [!NOTE]
> 您可以使用原則來**設定預設關聯設定檔**，將特定的副檔名設定為預設在 Internet Explorer 模式中開啟。 如需詳細資訊，請參閱 [原則 CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)。

1. 使用 Microsoft Edge 通道定義新的 ProgID，以使用 Internet Explorer 模式開啟。 ProgID 包含應用程式名稱和圖示，以及 msedge.exe 的完整路徑。

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""
```

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"
```

2. 設定 Shell 更新，以傳送使用 IE 模式開啟所需的命令列。

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. 最後，將 .mht 副檔名與新的 ProgID 建立關聯。 新增您的 ProgID 作為值名稱，並將值類型設為 REG_SZ。

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

在您設定上述範例中所述的機碼之後，您的使用者將會在 **[開啟方式]** 功能表上看到其他選項，以使用 IE 模式的 Microsoft Edge 來開啟 .mht 檔案\<channel\> 。

## <a name="registry-example"></a>登錄範例

您可以將下列代碼片段儲存為 .reg 檔案，然後將其匯入到登錄檔中。

```markdown
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\Application]
"ApplicationCompany"="Microsoft Corporation"
"ApplicationName"="Microsoft Edge with IE Mode"
"ApplicationIcon"="C:\\<edge_installation_dir>\\msedge.exe,4"
"AppUserModelId"=""

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\DefaultIcon]
@="C:\\<edge_installation_dir>\\msedge.exe,4"

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open]

[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""

```
## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a>設定檔類型以在 Internet Explorer 模式下開啟

從 Microsoft Edge 88 開始，您可以使用原則[[顯示操作功能表將指定檔案類型連結設定為在 Internet Explorer 模式下開啟]](./microsoft-edge-policies.md#show-context-menu-to-open-a-link-in-internet-explorer-mode)，以在 Internet Explorer 模式下開啟連結。 

透過在此原則[[在 Internet Explorer 模式下開啟本機檔案文件副檔名允許清單]](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) 中指定文件副檔名，可以定義此選項應套用的檔案類型。 

## <a name="see-also"></a>請參閱

- [關於 IE 模式](./edge-ie-mode.md)
- [可設定的網站資訊](./edge-learnmore-configurable-sites-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [設定檔案類型關聯](/windows/win32/shell/fa-file-types)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)