---
title: 中斷具潛在危險的檔案下載
ms.author: kvice
author: AndreaLBarr
manager: srugh
ms.date: 05/20/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 中斷具潛在危險的檔案下載
ms.openlocfilehash: 6239fd766c9e10d070188133a84ec0d7ce42a882
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618084"
---
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a><span data-ttu-id="b2a83-103">中斷具潛在危險的檔案下載</span><span class="sxs-lookup"><span data-stu-id="b2a83-103">Interrupting Downloads of Potentially Dangerous Files</span></span>

<span data-ttu-id="b2a83-104">Microsoft Edge 的檔案類型原則元件允許檔案依據其「危險」等級分類，例如，可自由下載無害的檔案 (例如 `.txt` 檔案)，同時具潛在危險的檔案 (例如 `.dll` 檔案) 會受到更高層級的審查，以及更注重安全的使用者經驗影響。</span><span class="sxs-lookup"><span data-stu-id="b2a83-104">Microsoft Edge’s File Type Policies component allows files to be classified by their level of “dangerousness”, such that harmless files (e.g. `.txt` files) can be downloaded freely, whilst potentially-dangerous files (e.g. `.dll` files) are subjected to a higher degree of vetting and a more security-conscious user-experience.</span></span>

## <a name="determining-the-danger-level-of-a-file-type"></a><span data-ttu-id="b2a83-105">判斷檔案類型的危險等級</span><span class="sxs-lookup"><span data-stu-id="b2a83-105">Determining the Danger Level of a File Type</span></span>

<span data-ttu-id="b2a83-106">Microsoft Edge 會從上游 Chromium 瀏覽器繼承其檔案類型策略；您可以在 [這裡](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) 檢視目前的清單內容。</span><span class="sxs-lookup"><span data-stu-id="b2a83-106">Microsoft Edge inherits its file type policies from the upstream Chromium browser; you can view the current contents of the list [here](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb).</span></span> <span data-ttu-id="b2a83-107">在清單中，您會看到每個類型都有一個danger_level，是三個值之一：`DANGEROUS`、`NOT_DANGEROUS` 或 `ALLOW_ON_USER_GESTURE`。</span><span class="sxs-lookup"><span data-stu-id="b2a83-107">Within the list, you’ll see that each type has a danger_level, which is one of three values: `DANGEROUS`, `NOT_DANGEROUS`, or `ALLOW_ON_USER_GESTURE`.</span></span>

<span data-ttu-id="b2a83-108">前兩個很簡單：**NOT_DANGEROUS** 表示檔案可以安全下載，即使是意外下載也是如此。</span><span class="sxs-lookup"><span data-stu-id="b2a83-108">The first two are simple: **NOT_DANGEROUS** means that the file is safe to download, even if the download was accidental.</span></span> <span data-ttu-id="b2a83-109">**危險** 表示瀏覽器應永遠警告使用者下載可能會傷害他們的裝置。</span><span class="sxs-lookup"><span data-stu-id="b2a83-109">**DANGEROUS** means that the browser should always warn the user that the download may harm their device.</span></span>

<span data-ttu-id="b2a83-110">第三個設定 **ALLOW_ON_USER_GESTURE** 是比較輕微的。</span><span class="sxs-lookup"><span data-stu-id="b2a83-110">The third setting **ALLOW_ON_USER_GESTURE** is more subtle.</span></span> <span data-ttu-id="b2a83-111">這類檔案具有潛在危險，但如果使用者要求下載，最有可能是無害的。</span><span class="sxs-lookup"><span data-stu-id="b2a83-111">Such files are potentially dangerous, but most likely harmless if the user requested the download.</span></span> <span data-ttu-id="b2a83-112">如果符合兩個條件，Microsoft Edge 將允許自動繼續這類下載：</span><span class="sxs-lookup"><span data-stu-id="b2a83-112">Microsoft Edge will allow such downloads to proceed automatically if two conditions are met:</span></span>

1. <span data-ttu-id="b2a83-113">有一個與網路要求關聯的 [使用者手勢](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) (例如，使用者按一下下載的連結)。</span><span class="sxs-lookup"><span data-stu-id="b2a83-113">There is a [user gesture](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) associated with the network request that initiated the download (e.g., the user clicked a link to the download).</span></span>
2. <span data-ttu-id="b2a83-114">在最近的午夜 (即昨天或更早時間) 之前，有一個參考來源 (連結至下載的頁面) 的先前瀏覽記錄。</span><span class="sxs-lookup"><span data-stu-id="b2a83-114">There is a recorded prior visit to the referring origin (the page linking to the download) prior to the most recent midnight (i.e., yesterday or earlier).</span></span> <span data-ttu-id="b2a83-115">這表示使用者有瀏覽網站的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="b2a83-115">This implies that the user has a history of visiting the site.</span></span>

<span data-ttu-id="b2a83-116">如果使用者透過使用 **儲存連結** 做為操作功能表命令、直接在瀏覽器的網址欄中輸入下載的 URL，或 Microsoft Defender SmartScreen 指出檔案是安全的，下載也會自動繼續。</span><span class="sxs-lookup"><span data-stu-id="b2a83-116">The download will also proceed automatically if the user explicitly initiated it by using the **Save link as** context menu command, entered the download’s URL directly into the browser’s address bar, or if Microsoft Defender SmartScreen indicated that the file is safe.</span></span>

<span data-ttu-id="b2a83-117">**更新：** 從版本 91 開始，Microsoft Edge會中斷缺少所需手勢的下載。</span><span class="sxs-lookup"><span data-stu-id="b2a83-117">**Update:** Starting in version 91, Microsoft Edge will interrupt downloads that lack the required gesture.</span></span>

## <a name="user-experience-for-downloads-lacking-gestures"></a><span data-ttu-id="b2a83-118">下載缺少手勢的使用者體驗</span><span class="sxs-lookup"><span data-stu-id="b2a83-118">User Experience for Downloads Lacking Gestures</span></span>

<span data-ttu-id="b2a83-119">如果具有潛在危險類型的下載在缺少必要手勢時開始，Microsoft Edge 會指出下載「已封鎖」。</span><span class="sxs-lookup"><span data-stu-id="b2a83-119">If a download for a potentially dangerous type starts without the required gesture, Microsoft Edge states that the download “was blocked”.</span></span> <span data-ttu-id="b2a83-120">名稱為 `Keep` 和 `Delete` 的命令可使用於... </span><span class="sxs-lookup"><span data-stu-id="b2a83-120">Commands named `Keep` and `Delete` are available from the …</span></span> <span data-ttu-id="b2a83-121">下載項目上的選單，可讓使用者繼續或取消下載。</span><span class="sxs-lookup"><span data-stu-id="b2a83-121">menu on the download item to allow the user to continue or cancel the download.</span></span>

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="已封鎖下載":::

<span data-ttu-id="b2a83-123">在 `edge://downloads` 頁面上，使用者會看到相同的選項：</span><span class="sxs-lookup"><span data-stu-id="b2a83-123">On the `edge://downloads`, page, the user will see the same options:</span></span>

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="MSG 保留刪除選項":::

## <a name="enterprise-controls"></a><span data-ttu-id="b2a83-125">企業控制</span><span class="sxs-lookup"><span data-stu-id="b2a83-125">Enterprise Controls</span></span>

<span data-ttu-id="b2a83-126">雖然使用者不太可能遇到他們每天使用之網站的下載中斷，但他們可能會在很少使用的網站上遇到合法下載。</span><span class="sxs-lookup"><span data-stu-id="b2a83-126">While users are unlikely to encounter download interruptions for sites they use every day, they might encounter them for legitimate downloads on sites that they use rarely.</span></span> <span data-ttu-id="b2a83-127">若要協助簡化企業使用者的體驗，可以使用群組原則。</span><span class="sxs-lookup"><span data-stu-id="b2a83-127">To help streamline the user-experience for Enterprises, a Group Policy is available.</span></span>

<span data-ttu-id="b2a83-128">企業可以使用 [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) 以指定允許從特定網站下載而不中斷的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b2a83-128">Enterprises can use [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) to specify the filetypes that are allowed to download from specific sites without interruption.</span></span> <span data-ttu-id="b2a83-129">例如，下列原則允許從 contoso.com 和 woodgrovebank.com 下載 XML 檔案，從任何網站下載 MSG 檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a83-129">For instance, the following policy allows XML files to download from contoso.com and woodgrovebank.com without interruption, and MSG files to download from any site.</span></span>

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a><span data-ttu-id="b2a83-130">需要手勢的檔案類型</span><span class="sxs-lookup"><span data-stu-id="b2a83-130">File Types Requiring a Gesture</span></span>

<span data-ttu-id="b2a83-131">最新的 [檔案類型原則](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) 發行於 Chromium 原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="b2a83-131">The latest [file types policies](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) are published in the Chromium source code.</span></span> <span data-ttu-id="b2a83-132">截至 2021 年 5 月，在至少一個作業系統平臺上的 `ALLOW_ON_USER_GESTURE` 之 `danger_level` 檔案類型包括有：</span><span class="sxs-lookup"><span data-stu-id="b2a83-132">As of May 2021, file types with a `danger_level` of `ALLOW_ON_USER_GESTURE` on at least one OS platform include:</span></span>
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a><span data-ttu-id="b2a83-133">危險層級可能會依作業系統而不同</span><span class="sxs-lookup"><span data-stu-id="b2a83-133">Danger Level May Vary By Operating System</span></span>

<span data-ttu-id="b2a83-134">檔案類型設定有時會因用戶端作業系統平臺而異。</span><span class="sxs-lookup"><span data-stu-id="b2a83-134">File type settings sometimes vary depending on the client OS platform.</span></span> <span data-ttu-id="b2a83-135">例如， `.exe` 在 Mac 上是不具危險的，同時 `.applescript` 在 Windows 上則是無害的。</span><span class="sxs-lookup"><span data-stu-id="b2a83-135">For instance, an `.exe` is not dangerous on a Mac, while an `.applescript` is harmless on Windows.</span></span>
