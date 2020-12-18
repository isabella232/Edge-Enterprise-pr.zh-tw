---
title: 封鎖程式工具組用來停用自動傳遞 Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 12/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 封鎖程式工具組用來停用自動傳遞 Microsoft Edge
ms.openlocfilehash: 9fb97d2dfec4822f8ce76dc3e37b85118c6572ad
ms.sourcegitcommit: 606282995b466a968bab40c16005a6653323c763
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229614"
---
# 封鎖程式工具組用來停用自動傳遞 Microsoft Edge (以 Chromium 為基礎)

本文介紹了用於停用自動傳遞和安裝 Microsoft Edge 的封鎖程式工具組。

我們已在本文中進行下列更新：

- **2020 年 01 月 09 日**，包含可能會要求您使用封鎖程式工具組的裝置相關資訊。
- **2020 年 2 月 28 日**，將「MDM 管理」從裝置準則中移除，以便從此自動更新中排除
- **2020 年 6 月 30 日** ，反映出與 Windows Update 連結的所有裝置都含括在此更新內容的接收範疇之中 (最快可以可於 2020 年 7 月 30 日生效)
- **2020 年 10 月 12 日** 說明在版本 20H2 之前的情況，通常會忽略封鎖程式工具組的設定

> [!NOTE]
> 本文適用於 Microsoft Edge 穩定通道。

## 概觀

為了協助我們的客戶成為更安全且更時時維持著最新狀態，Microsoft 將會發佈 Microsoft Edge （以 Chromium 為基礎）到執行 Windows 10 版本1803 及更新版本的所有 Windows Update 連接裝置。 此過程將在 2020 年 1 月 15 日之後開始，到那時將會有更多資訊提供參考。

封鎖程式工具組適用於想要封鎖自動傳遞 Microsoft Edge 到執行 Windows 10 版本 1803 和更新版本的 Windows 更新連接裝置的組織。 Windows Server Update Services (WSUS) 或商務用 Windows Update (WUfB) 管理的裝置將會從此自動 Windows 更新中排除，但可能會透過其組織收到新的 Microsoft Edge (以 Chromium 為基礎)。

**請務必注意：**

- 封鎖程式工具組不會阻止使用者從網際網路下載或外部媒體手動安裝 Microsoft Edge (以 Chromium 為基礎)。
- 透過商務用 Windows Update (WUfB) 管理更新的組織不會自動收到此更新，也不需要部署封鎖程式工具組。
- 組織在使用更新管理解決方案 (如 Windows Server Update Services (WSUS) 或 System Center Configuration Manager (SCCM)) 管理的環境中，不需要部署封鎖程式工具組。 他們可以使用這些產品，透過 Windows Update 和 Microsoft Update 來全面管理已發佈的更新，包括在 [全新 Microsoft Edge 中的 WSUS 更新](https://support.microsoft.com/help/4584642/update-in-wsus-for-the-new-microsoft-edge)(在其環境內)。
- 此更新是獨立更新 (不是每月累積更新的一部分)，可為企業客戶提供靈活性和對部署此更新的最大控制。
- 新版 Microsoft Edge (以 Chromium 為基礎) 是包含在 2020 下半年的 Windows 10 版本 20H2 功能更新中。 封鎖程式工具組不會對 20H2 版本的行為或佈署造成影響。 如需有關 Windows 10 版本 20H2 的詳細資訊，請參閱[此處](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/)。

可以從 [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe) 下載封鎖程式工具組可執行檔。

### 工具組元件

此工具組包括下列元件：

- 可執行封鎖程式指令碼 (.CMD)
- 群組原則系統管理範本 (.ADMX 和 .ADML)

### 支援的作業系統

Windows 10 版本 1803 及更新版本。

## 封鎖程式指令碼

該指令碼建立一個登錄機碼，並將關聯的值設定為封鎖或解除封鎖 (取決於使用的命令列選項) 自動在本機電腦或遠端目的電腦上 Microsoft Edge (以 Chromium 為基礎) 的傳遞。

**登錄機碼：** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**機碼值名稱：** `DoNotUpdateToEdgeWithChromium`

| 值                | 結果                         |
|----------------------|--------------------------------|
| *機碼未定義* | *不會*封鎖散發。 |
| 0                    | *不會*封鎖散發。 |
| 1                    | 會封鎖散發。       |

指令碼有下列命令列語法：<br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### 電腦名稱

`<machine name>` 參數是選擇性的。 如果未指定，則在本機電腦上執行該動作。 否則，透過 `REG` 命令的遠端登錄功能存取遠端電腦。 如果由於安全性權限而無法存取遠端登錄，或者找不到遠端電腦，則會從 `REG` 命令傳回錯誤訊息。

### 切換

指令碼使用的切換是互斥的，並且只對給定命令中的第一個有效切換執行操作。 指令碼可以在同一台電腦上執行多次。

| 切換       | 描述                              |
|--------------|------------------------------------------|
| `/B`         | 會封鎖散發                      |
| `/U`         | 會解除封鎖散發                    |
| `/H` 或 `/?` | 顯示以下摘要說明：<br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## 群組原則系統管理範本 (.ADMX 和 .ADML 檔案)

群組原則系統管理範本 (.ADMX 和 .ADML 檔案) 允許系統管理員匯入新的群組原則設定，以封鎖或解除封鎖將 Microsoft Edge (以 Chromium 為基礎) 自動傳遞到其群組原則環境，並使用群組原則在其環境中的系統中集中執行動作。

執行 Windows 10 RS3 企業版/教育版以及 RS4 和更高版本的使用者將在以下路徑下看到原則：

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

此設定僅做為電腦設定可用；沒有每個使用者設定。

> [!IMPORTANT]
> 此登錄設定不儲存在原則機碼中，並被視為*喜好設定*。 因此，如果已刪除實作該設定的群組原則物件，或者原則設定為**未設定**，則該設定將保留。 若要使用群組原則解除封鎖 Microsoft Edge (以 Chromium 為基礎) 的散發，將原則設定為**禁用**。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://www.microsoftedgeinsider.com/enterprise)
- [支援 Microsoft Edge 的 Windows 更新](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [如何存取舊版 Microsoft Edge](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
