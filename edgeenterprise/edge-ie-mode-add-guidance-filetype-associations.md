---
title: 將副檔名與 Internet Explorer 模式建立關聯
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 將副檔名與 Internet Explorer 模式建立關聯
ms.openlocfilehash: c027b11e426cd665cb9e6cc25b4c9f66a0c6762a
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617453"
---
# <a name="associate-file-extensions-with-internet-explorer-mode"></a><span data-ttu-id="61399-103">將副檔名與 Internet Explorer 模式建立關聯</span><span class="sxs-lookup"><span data-stu-id="61399-103">Associate file extensions with Internet Explorer mode</span></span>

>[!Note]
> <span data-ttu-id="61399-104">Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。</span><span class="sxs-lookup"><span data-stu-id="61399-104">The Internet Explorer 11 desktop application will be retired and go out of support on June 15, 2022 (for a list of what’s in scope, [see the FAQ](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549)).</span></span> <span data-ttu-id="61399-105">您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="61399-105">The same IE11 apps and sites you use today can open in Microsoft Edge with Internet Explorer mode.</span></span> <span data-ttu-id="61399-106">[從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。</span><span class="sxs-lookup"><span data-stu-id="61399-106">[Learn more here](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/).</span></span>

<span data-ttu-id="61399-107">本文說明如何將 Microsoft Edge 與含桌面應用程式副檔名的 Internet Explorer 模式建立關聯。</span><span class="sxs-lookup"><span data-stu-id="61399-107">This article explains how to associate Microsoft Edge with Internet Explorer mode with file extensions for desktop applications.</span></span>

> [!NOTE]
> <span data-ttu-id="61399-108">本文適用於 Microsoft Edge 版本 86 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="61399-108">This article applies to Microsoft Edge version 86 or later.</span></span>

## <a name="guidance-for-file-extension-association-with-internet-explorer-mode"></a><span data-ttu-id="61399-109">使用 Internet Explorer 模式的副檔名關聯指南</span><span class="sxs-lookup"><span data-stu-id="61399-109">Guidance for file extension association with Internet Explorer mode</span></span>

<span data-ttu-id="61399-110">下列指示會顯示將 Microsoft Edge 與 IE 模式與 .mht 檔案類型相關聯的輸入。</span><span class="sxs-lookup"><span data-stu-id="61399-110">The following instructions show an entry that associates Microsoft Edge with IE mode with the .mht file type.</span></span> <span data-ttu-id="61399-111">若要設定檔案關聯，請使用下列步驟作為指南。</span><span class="sxs-lookup"><span data-stu-id="61399-111">Use the following steps as a guide for setting a file association.</span></span>

> [!NOTE]
> <span data-ttu-id="61399-112">您可以使用原則來**設定預設關聯設定檔**，將特定的副檔名設定為預設在 Internet Explorer 模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="61399-112">You can set specific file extensions to open in Internet Explorer mode by default using the policy to **Set a default associations configuration file**.</span></span> <span data-ttu-id="61399-113">如需詳細資訊，請參閱 [原則 CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)。</span><span class="sxs-lookup"><span data-stu-id="61399-113">For more information, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration).</span></span>

1. <span data-ttu-id="61399-114">使用 Microsoft Edge 通道定義新的 ProgID，以使用 Internet Explorer 模式開啟。</span><span class="sxs-lookup"><span data-stu-id="61399-114">Define a new ProgID with the Microsoft Edge channel to use to open with Internet Explorer mode.</span></span> <span data-ttu-id="61399-115">ProgID 包含應用程式名稱和圖示，以及 msedge.exe 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="61399-115">The ProgID includes the application name and Icon and the full path to msedge.exe.</span></span>

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

2. <span data-ttu-id="61399-116">設定 Shell 更新，以傳送使用 IE 模式開啟所需的命令列。</span><span class="sxs-lookup"><span data-stu-id="61399-116">Configure shell updates to pass the command line needed to open with IE mode.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Classes\MSEdgeIEModeMHT\shell\open\command]
@="\"C:\\<edge_installation_dir>\\msedge.exe\" -ie-mode-file-url -- \"%1\""
```

3. <span data-ttu-id="61399-117">最後，將 .mht 副檔名與新的 ProgID 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="61399-117">Finally, associate the .mht file extension with a new ProgID.</span></span> <span data-ttu-id="61399-118">新增您的 ProgID 作為值名稱，並將值類型設為 REG_SZ。</span><span class="sxs-lookup"><span data-stu-id="61399-118">Add your ProgID as a value name, with the value type of REG_SZ.</span></span>

```markdown
[HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts\.mht\OpenWithProgids]
"MSEdgeIEModeMHT"=hex(0):
```

<span data-ttu-id="61399-119">在您設定上述範例中所述的機碼之後，您的使用者將會在 **[開啟方式]** 功能表上看到其他選項，以使用 IE 模式的 Microsoft Edge 來開啟 .mht 檔案\<channel\> 。</span><span class="sxs-lookup"><span data-stu-id="61399-119">After you set the keys described in the previous example, your users will see an additional option on the **Open with** menu to open an .mht file using Microsoft Edge \<channel\> with IE mode.</span></span>

## <a name="registry-example"></a><span data-ttu-id="61399-120">登錄範例</span><span class="sxs-lookup"><span data-stu-id="61399-120">Registry Example</span></span>

<span data-ttu-id="61399-121">您可以將下列代碼片段儲存為 .reg 檔案，然後將其匯入到登錄檔中。</span><span class="sxs-lookup"><span data-stu-id="61399-121">You can save the following code snippet as a .reg file and import it into the registry.</span></span>

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

## <a name="configuring-file-types-to-open-in-internet-explorer-mode"></a><span data-ttu-id="61399-122">設定檔類型以在 Internet Explorer 模式下開啟</span><span class="sxs-lookup"><span data-stu-id="61399-122">Configuring file types to open in Internet Explorer mode</span></span>

<span data-ttu-id="61399-123">從 Microsoft Edge 88 開始，您可以使用原則[[顯示操作功能表將指定檔案類型連結設定為在 Internet Explorer 模式下開啟]](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed)，以在 Internet Explorer 模式下開啟連結。</span><span class="sxs-lookup"><span data-stu-id="61399-123">Starting Edge 88, you can configure specific file type links to open in Internet Explorer mode using the policy [Show context menu to open links in Internet Explorer mode](./microsoft-edge-policies.md#internetexplorerintegrationreloadiniemodeallowed).</span></span>

<span data-ttu-id="61399-124">透過在此原則[[在 Internet Explorer 模式下開啟本機檔案文件副檔名允許清單]](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist) 中指定文件副檔名，可以定義此選項應套用的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="61399-124">You can define file types this option should apply to, by specifying file extensions in this policy [Open local files in Internet Explorer mode file extension allow list](./microsoft-edge-policies.md#internetexplorerintegrationlocalfileextensionallowlist).</span></span> 

## <a name="see-also"></a><span data-ttu-id="61399-125">請參閱</span><span class="sxs-lookup"><span data-stu-id="61399-125">See also</span></span>

- [<span data-ttu-id="61399-126">關於 IE 模式</span><span class="sxs-lookup"><span data-stu-id="61399-126">About IE mode</span></span>](./edge-ie-mode.md)
- [<span data-ttu-id="61399-127">可設定的網站資訊</span><span class="sxs-lookup"><span data-stu-id="61399-127">Configurable sites information</span></span>](./edge-learnmore-configurable-sites-ie-mode.md)
- [<span data-ttu-id="61399-128">其他企業模式資訊</span><span class="sxs-lookup"><span data-stu-id="61399-128">Additional Enterprise Mode information</span></span>](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [<span data-ttu-id="61399-129">設定檔案類型關聯</span><span class="sxs-lookup"><span data-stu-id="61399-129">Setting file type associations</span></span>](/windows/win32/shell/fa-file-types)
- [<span data-ttu-id="61399-130">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="61399-130">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)