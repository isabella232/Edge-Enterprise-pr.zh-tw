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
# <a name="interrupting-downloads-of-potentially-dangerous-files"></a>中斷具潛在危險的檔案下載

Microsoft Edge 的檔案類型原則元件允許檔案依據其「危險」等級分類，例如，可自由下載無害的檔案 (例如 `.txt` 檔案)，同時具潛在危險的檔案 (例如 `.dll` 檔案) 會受到更高層級的審查，以及更注重安全的使用者經驗影響。

## <a name="determining-the-danger-level-of-a-file-type"></a>判斷檔案類型的危險等級

Microsoft Edge 會從上游 Chromium 瀏覽器繼承其檔案類型策略；您可以在 [這裡](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) 檢視目前的清單內容。 在清單中，您會看到每個類型都有一個danger_level，是三個值之一：`DANGEROUS`、`NOT_DANGEROUS` 或 `ALLOW_ON_USER_GESTURE`。

前兩個很簡單：**NOT_DANGEROUS** 表示檔案可以安全下載，即使是意外下載也是如此。 **危險** 表示瀏覽器應永遠警告使用者下載可能會傷害他們的裝置。

第三個設定 **ALLOW_ON_USER_GESTURE** 是比較輕微的。 這類檔案具有潛在危險，但如果使用者要求下載，最有可能是無害的。 如果符合兩個條件，Microsoft Edge 將允許自動繼續這類下載：

1. 有一個與網路要求關聯的 [使用者手勢](https://textslashplain.com/2020/05/18/browser-basics-user-gestures/) (例如，使用者按一下下載的連結)。
2. 在最近的午夜 (即昨天或更早時間) 之前，有一個參考來源 (連結至下載的頁面) 的先前瀏覽記錄。 這表示使用者有瀏覽網站的歷程記錄。

如果使用者透過使用 **儲存連結** 做為操作功能表命令、直接在瀏覽器的網址欄中輸入下載的 URL，或 Microsoft Defender SmartScreen 指出檔案是安全的，下載也會自動繼續。

**更新：** 從版本 91 開始，Microsoft Edge會中斷缺少所需手勢的下載。

## <a name="user-experience-for-downloads-lacking-gestures"></a>下載缺少手勢的使用者體驗

如果具有潛在危險類型的下載在缺少必要手勢時開始，Microsoft Edge 會指出下載「已封鎖」。 名稱為 `Keep` 和 `Delete` 的命令可使用於...  下載項目上的選單，可讓使用者繼續或取消下載。

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/Dowload-was-blocked.png" alt-text="已封鎖下載":::

在 `edge://downloads` 頁面上，使用者會看到相同的選項：

:::image type="content" source="media/microsoft-edge-security-Download-interruptions/msg-keep-delete-option.png" alt-text="MSG 保留刪除選項":::

## <a name="enterprise-controls"></a>企業控制

雖然使用者不太可能遇到他們每天使用之網站的下載中斷，但他們可能會在很少使用的網站上遇到合法下載。 若要協助簡化企業使用者的體驗，可以使用群組原則。

企業可以使用 [ExemptDomainFileTypePairsFromFileTypeDownloadWarnings](/deployedge/microsoft-edge-policies#exemptdomainfiletypepairsfromfiletypedownloadwarnings) 以指定允許從特定網站下載而不中斷的檔案類型。 例如，下列原則允許從 contoso.com 和 woodgrovebank.com 下載 XML 檔案，從任何網站下載 MSG 檔案。

`[{"file_extension":"xml","domains":["contoso.com", "woodgrovebank.com"]},
{"file_extension":"msg", "domains": ["*"]}]`

## <a name="file-types-requiring-a-gesture"></a>需要手勢的檔案類型

最新的 [檔案類型原則](https://source.chromium.org/chromium/chromium/src/+/main:components/safe_browsing/core/resources/download_file_types.asciipb) 發行於 Chromium 原始程式碼。 截至 2021 年 5 月，在至少一個作業系統平臺上的 `ALLOW_ON_USER_GESTURE` 之 `danger_level` 檔案類型包括有：
`crx, pl, py, pyc, pyo, pyw, rb, efi, oxt, msi, msp, mst, ade, adp, mad, maf, mag, mam, maq, mar, mas, mat, mav, maw, mda, mdb, mde, mdt, mdw, mdz, accdb, accde, accdr, accda, ocx, ops, paf, pcd, pif, plg, prf, prg, pst, cpi, partial, xrm-ms, rels, svg, xml, xsl, xsd, ps1, ps1xml, ps2, ps2xml, psc1, psc2, js, jse, vb, vbe, vbs, vbscript, ws, wsc, wsf, wsh, msh, msh1, msh2, mshxml, msh1xml, msh2xml, ad, app, application, appref-ms, asp, asx, bas, bat, chi, chm, cmd, com, cpl, crt, cer, der, eml, exe, fon, fxp, hlp, htt, inf, ins, inx, isu, isp, job, lnk, mau, mht, mhtml, mmc, msc, msg, reg, rgs, scr, sct, search-ms, settingcontent-ms, shb, shs, slk, u3p, vdx, vsx, vtx, vsdx, vssx, vstx, vsdm, vssm, vstm, vsd, vsmacros, vss, vst, vsw, xnk, cdr, dart, dc42, diskcopy42, dmg, dmgpart, dvdr, dylib, img, imgpart, ndif, service, smi, sparsebundle, sparseimage, toast, udif, action, definition, wflow, caction, as, cpgz, command, mpkg, pax, workflow, xip, mobileconfig, configprofile, internetconnect, networkconnect, pkg, deb, pet, pup, rpm, slp, out, run, bash, csh, ksh, sh, shar, tcsh, desktop, dex,apk`

## <a name="danger-level-may-vary-by-operating-system"></a>危險層級可能會依作業系統而不同

檔案類型設定有時會因用戶端作業系統平臺而異。 例如， `.exe` 在 Mac 上是不具危險的，同時 `.applescript` 在 Windows 上則是無害的。
