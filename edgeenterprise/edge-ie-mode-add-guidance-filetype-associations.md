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
ms.openlocfilehash: 9f39a3319c3e45001090dd9f0cffb3e7ce2648fb
ms.sourcegitcommit: 306582403d4272831bcac390154c7cc7041a9b7e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/21/2020
ms.locfileid: "11238190"
---
# <span data-ttu-id="8d50f-103">將副檔名與 Internet Explorer 模式建立關聯</span><span class="sxs-lookup"><span data-stu-id="8d50f-103">Associate file extensions with Internet Explorer mode</span></span>

<span data-ttu-id="8d50f-104">本文說明如何將 Microsoft Edge 與含桌面應用程式副檔名的 Internet Explorer 模式建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8d50f-104">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="8d50f-105">本文適用於 Microsoft Edge 版本 86 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8d50f-105">This article applies to Microsoft Edge version 86 or later.</span></span>

## <span data-ttu-id="8d50f-106">使用 Internet Explorer 模式的副檔名關聯指南</span><span class="sxs-lookup"><span data-stu-id="8d50f-106">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="8d50f-107">下列指示會顯示將 Microsoft Edge 與 IE 模式與 .mht 檔案類型相關聯的輸入。</span><span class="sxs-lookup"><span data-stu-id="8d50f-107">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="8d50f-108">若要設定檔案關聯，請使用下列步驟作為指南。</span><span class="sxs-lookup"><span data-stu-id="8d50f-108">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="8d50f-109">您可以使用原則來**設定預設關聯設定檔**，將特定的副檔名設定為預設在 Internet Explorer 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="8d50f-109">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="8d50f-110">如需詳細資訊，請參閱 [原則 CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)。</span><span class="sxs-lookup"><span data-stu-id="8d50f-110">For more information, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="8d50f-111">使用 Microsoft Edge 通道定義新的 ProgID，以使用 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="8d50f-111">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="8d50f-112">ProgID 包含應用程式名稱和圖示，以及 msedge.exe 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8d50f-112">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="8d50f-113">設定 Shell 更新，以傳送使用 IE 模式開啟所需的命令列。</span><span class="sxs-lookup"><span data-stu-id="8d50f-113">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="8d50f-114">最後，將 .mht 副檔名與新的 ProgID 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8d50f-114">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="8d50f-115">新增您的 ProgID 作為值名稱，並將值類型設為 REG_SZ。</span><span class="sxs-lookup"><span data-stu-id="8d50f-115">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="8d50f-116">在您設定上述範例中所述的機碼之後，您的使用者將會在 **[開啟方式]** 功能表上看到其他選項，以使用 IE 模式的 Microsoft Edge 來開啟 .mht 檔案\<channel\> 。</span><span class="sxs-lookup"><span data-stu-id="8d50f-116">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <span data-ttu-id="8d50f-117">登錄範例</span><span class="sxs-lookup"><span data-stu-id="8d50f-117">Registry Example</span></span>

<span data-ttu-id="8d50f-118">您可以將下列代碼片段儲存為 .reg 檔案，然後將其匯入到登錄檔中。</span><span class="sxs-lookup"><span data-stu-id="8d50f-118">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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
## <span data-ttu-id="8d50f-119">設定檔類型以在 Internet Explorer 模式下開啟</span><span class="sxs-lookup"><span data-stu-id="8d50f-119">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="8d50f-120">從 Microsoft Edge 88 開始，您可以使用原則[[顯示操作功能表將指定檔案類型連結設定為在 Internet Explorer 模式下開啟]](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode)，以在 Internet Explorer 模式下開啟連結。</span><span class="sxs-lookup"><span data-stu-id="8d50f-120">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#show-context-menu-to-open-a-link-in-internet-explorer-mode).</span></span> 

<span data-ttu-id="8d50f-121">透過在此原則[[在 Internet Explorer 模式下開啟本機檔案文件副檔名允許清單]](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) 中指定文件副檔名，可以定義此選項應套用的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8d50f-121">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](https://docs.microsoft.com/deployedge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <span data-ttu-id="8d50f-122">請參閱</span><span class="sxs-lookup"><span data-stu-id="8d50f-122">See also</span></span>

- [<span data-ttu-id="8d50f-123">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="8d50f-123">About IE mode</span></span>](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [<span data-ttu-id="8d50f-124">可設定的網站資訊</span><span class="sxs-lookup"><span data-stu-id="8d50f-124">Configurable sites information</span></span>](https://docs.microsoft.com/deployedge/edge-learnmore-configurable-sites-ie-mode)
- [<span data-ttu-id="8d50f-125">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="8d50f-125">Additional Enterprise Mode information</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="8d50f-126">設定檔案類型關聯</span><span class="sxs-lookup"><span data-stu-id="8d50f-126">Setting file type associations</span></span>](https://docs.microsoft.com/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="8d50f-127">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="8d50f-127">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
