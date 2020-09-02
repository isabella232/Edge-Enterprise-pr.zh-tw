---
title: 封鎖程式工具組用來停用自動傳遞 Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 封鎖程式工具組用來停用自動傳遞 Microsoft Edge
ms.openlocfilehash: 7563d2c94cf91a8434328699e46c75dbcfb77561
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979595"
---
# 封鎖程式工具組用來停用自動傳遞 Microsoft Edge (以 Chromium 為基礎)

本文介紹了用於停用自動傳遞和安裝 Microsoft Edge 的封鎖程式工具組。 此篇文章已於 **2020/01/09 進行更新**，並加入更多可能要求您使用封鎖程式工具組的其他資訊：於**2020/2/28** 更新內容中，將裝置準則中的 "MDM managed" 移除以便將此裝置排除在自動更新的範圍中，以及在 **2020/6/30** 更新內容中，反映出與 Windows Update 連結的所有裝置都含括在此更新內容的接收範疇之中（最快可以可於 2020/7/30 生效）。

> [!NOTE]
> 本文適用於 Microsoft Edge 穩定通道。

## 概觀

為了協助我們的客戶成為更安全且更時時維持著最新狀態，Microsoft 將會發佈 Microsoft Edge （以 Chromium 為基礎）到執行 Windows 10 版本1803 及更新版本的所有 Windows Update 連接裝置。 此過程將在 2020 年 1 月 15 日之後開始，到那時將會有更多資訊提供參考。

封鎖程式工具組適用於想要封鎖自動傳遞 Microsoft Edge 到執行 Windows 10 版本 1803 和更新版本的 Windows 更新連接裝置的組織。
透過 Windows Server Update Services (WSUS) 或 [商務用 Windows Update (WUfB)] 管理的裝置將不會含括在此自動更新的範圍清單。

**請務必注意：**

- 封鎖程式工具組不會阻止使用者從網際網路下載或外部媒體手動安裝 Microsoft Edge (以 Chromium 為基礎)。
- 透過商務用 Windows Update (WUfB) 管理更新的組織不會自動收到此更新，也不需要部署封鎖程式工具組。
- 組織在使用更新管理解決方案 (如 Windows Server Update Services (WSUS) 或 System Center Configuration Manager (SCCM)) 管理的環境中，不需要部署封鎖程式工具組。 這些組織可以使用這些產品在其環境中全面管理透過 Windows Update 和 Microsoft Update 發佈的更新的部署，包括 Microsoft Edge (以 Chromium 為基礎)。
- 此更新是獨立更新 (不是每月累積更新的一部分)，可為企業客戶提供靈活性和對部署此更新的最大控制。
- 新版 Microsoft Edge（以 Chromium 為基礎）將含括在 Windows 10 在 2020 年第二季功能更新的版本 20H2 之中。 封鎖程式工具組不會對 20H2 版本的行為或佈署造成影響。 如需有關 Windows 10 版本 20H2 的詳細資訊，請參閱[此處](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/)。

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
