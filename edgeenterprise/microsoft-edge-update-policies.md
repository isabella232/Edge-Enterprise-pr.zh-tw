---
title: Microsoft Edge Update 原則文件
ms.author: stmoody
author: AndreaLBarr
manager: tahills
ms.date: 07/23/2021
audience: ITPro
ms.topic: reference
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
ms.custom: ''
description: Microsoft Edge Updater 支援的所有原則的文件
ms.openlocfilehash: 9c7eca4d5bdd7c87bea141a422dce3b17f22067c
ms.sourcegitcommit: 9088e839e82d80c72460586e9af0610c6ca71b83
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675940"
---
# <a name="microsoft-edge---update-policies"></a>Microsoft Edge - 更新原則

最新版本的 Microsoft Edge 包括以下原則，可用於控制更新 Microsoft Edge 的方式和時間。

如需 Microsoft Edge 中提供的其他原則的相關資訊，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)
> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。
## <a name="available-policies"></a>可用原則
下表列出此版本 Microsoft Edge 提供的所有更新相關群組原則。 使用下表中的連結，深入了解特定原則。

|&nbsp;|&nbsp;| |**-**|-| |**[應用程式](#applications)**|[喜好設定](#preferences)| |**[Proxy 伺服器](#proxy-server)**|[Microsoft Edge WebView](#microsoft-edge-webview)|
### [<a name="applications"></a>應用程式](#applications-policies)
|原則名稱|標題|
|-|-|
|[InstallDefault](#installdefault)|允許安裝預設值|
|[UpdateDefault](#updatedefault)|更新原則覆寫預設值|
|[Install](#install)|允許安裝 (經由通道)|
|[更新](#update)|更新原則覆寫 (經由通道)|
|[Allowsxs](#allowsxs)|允許 Microsoft Edge 並排瀏覽器體驗|
|[CreateDesktopShortcutDefault](#createdesktopshortcutdefault)|防止在預設安裝時建立桌面捷徑|
|[CreateDesktopShortcut](#createdesktopshortcut)|防止在安裝時建立桌面捷徑 (每個通道)|
|[RollbackToTargetVersion](#rollbacktotargetversion)|復原至目標版本 (每個通道)|
|[TargetVersionPrefix](#targetversionprefix)|目標版本覆寫 (經由通道)|
|[UpdaterExperimentationAndConfigurationServiceControl](#UpdaterExperimentationAndConfigurationServiceControl)| 取回組組和實驗|
### [<a name="preferences"></a>喜好設定](#preferences-policies)
|原則名稱|標題|
|-|-|
|[AutoUpdateCheckPeriodMinutes](#autoupdatecheckperiodminutes)|自動更新檢查期間覆寫|
|[UpdatesSuppressed](#updatessuppressed)|每天抑制自動更新檢查的期間|

### [<a name="proxy-server"></a>Proxy 伺服器](#proxy-server-policies)
|原則名稱|說明文字|
|-|-|
|[ProxyMode](#proxymode)|選擇如何指定 Proxy 伺服器設定|
|[ProxyPacUrl](#proxypacurl)|Proxy .pac 檔案的 URL|
|[ProxyServer](#proxyserver)|Proxy 伺服器的位址或 URL|

### [<a name="microsoft-edge-webview"></a>Microsoft Edge WebView](#microsoft-edge-webview-policies)
|原則名稱|標題|
|-|-|
|[安裝](#install-webview)|允許安裝|
|[更新](#update-webview)|更新原則覆寫|

## <a name="applications-policies"></a>應用程式原則

[回到頁首](#microsoft-edge---update-policies)
### <a name="installdefault"></a>InstallDefault
#### <a name="allow-installation-default"></a>允許安裝預設值
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
您可以指定所有通道的預設行為，以便在加入網域的裝置上允許或封鎖 Microsoft Edge。

您可以為特定通道啟用「[允許安裝](#install)」原則來覆寫各個通道的此原則。

如果停用此原則，則會封鎖 Microsoft Edge 安裝。 當 '[允許安裝](#install)' 原則設定為 [尚未設定] 時，只會影響 Microsoft Edge 軟體的安裝，。

此原則不會防止 Microsoft Edge Update 執行或防止使用者透過其他方法安裝 Microsoft Edge 軟體。

這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：InstallDefault
- GP 名稱：允許安裝預設值
- GP 路徑：系統管理範本/Microsoft Edge Update/應用程式
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：InstallDefault
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="updatedefault"></a>UpdateDefault
#### <a name="update-policy-override-default"></a>更新原則覆寫預設值
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
允許您指定所有通道的預設行為，這些通道涉及 Microsoft Edge Update 處理 Microsoft Edge 可用更新的方式。 可以透過為這些特定通道指定「[更新原則覆寫](#update)」原則來覆寫各個通道的設定。

  如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：
   - 一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。
   - 僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。
   - 僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。
   - 停用更新：一律不套用更新。

  如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。 如果停用更新，請定期檢查更新，並將它們散發給使用者。

  如果不啟用和設定此原則，Microsoft Edge Update 將依照[「更新原則覆寫」](#update)原則的指定方式處理可用更新。

  這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：UpdateDefault
- GP 名稱：更新原則覆寫預設值
- GP 路徑：系統管理範本/Microsoft Edge Update/應用程式
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：UpdateDefault
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000003
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="install"></a>Install
#### <a name="allow-installation"></a>允許安裝
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
指定是否可以在加入網域的裝置上安裝 Microsoft Edge 通道。

  如果您為通道啟用此原則，將不會封鎖 Microsoft Edge 的安裝。

  如果您為通道停用此原則，將會封鎖 Microsoft Edge 的安裝。

  如果不為通道設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以安裝該 Microsoft Edge 通道。

  這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：Install
- GP 名稱：允許安裝
- GP 路徑： 
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): Install{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Install{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Install{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Install{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="update"></a>Update
#### <a name="update-policy-override"></a>更新原則覆寫
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
指定 Microsoft Edge Update 如何處理來自 Microsoft Edge 的可用更新。

如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge 更新：
  - 一律允許更新：透過定期更新檢查或手動更新檢查找到更新時，一律套用更新。
  - 僅限自動無訊息更新：僅當定期更新檢查找到更新時才套用更新。
  - 僅限手動更新：僅當使用者執行手動更新檢查時，才套用更新。 (並非所有應用程式都提供此選項的介面。)
  - 停用更新：一律不套用更新。

如果選取手動更新，請確保使用應用程式的手動更新機制 (如果可用) 定期檢查更新。 如果停用更新，請定期檢查更新，並將它們散發給使用者。

如果不啟用和設定此原則，Microsoft Edge Update 將依照「[更新原則覆寫預設值](#updatedefault)」原則的指定方式處理可用更新。

如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136406](https://go.microsoft.com/fwlink/?linkid=2136406)。

這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：Update
- GP 名稱：更新原則覆寫
- GP 路徑： 
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：
  - (Stable): Update{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): Update{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): Update{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): Update{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
always allow updates 0x00000001
Automatic silent updates only 0x00000003
manual updates only 0x00000002
updates disabled 0x00000000
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="allowsxs"></a>Allowsxs
#### <a name="allow-microsoft-edge-side-by-side-browser-experience"></a>允許 Microsoft Edge 並排瀏覽器體驗
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
此原則允許使用者並排執行 Microsoft Edge (Edge HTML) 和 Microsoft Edge (以 Chromium 為基礎)。

如果此原則設定為 [未設定]，則在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。  這與 [停用] 設定的行為相同。

[停用] 設定會封鎖並排體驗，且在安裝 Microsoft Edge (以 Chromium 為基礎) Stable 通道和 2019 年 11 月安全性更新後，Microsoft Edge (以 Chromium 為基礎) 會取代 Microsoft Edge (Edge HTML)。  這與 [未設定] 設定的行為相同。

當此原則 [啟用] 時，Microsoft Edge (以 Chromium 為基礎) 和 Microsoft Edge (Edge HTML) 可以在安裝 Microsoft Edge (以 Chromium 為基礎) 後並排執行。

若要使此群組原則生效，必須在 Windows Update 自動安裝 Microsoft Edge (以 Chromium 為基礎) 之前進行設定。 注意：使用者可以使用 Microsoft Edge (以 Chromium 為基礎) 封鎖程式工具組來封鎖 Microsoft Edge (以 Chromium 為基礎) 的自動更新。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：Allowsxs
- GP 名稱：允許 Microsoft Edge 並排瀏覽器體驗
- GP 路徑：系統管理範本/Microsoft Edge Update/應用程式
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：Allowsxs
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)

### <a name="createdesktopshortcutdefault"></a>CreateDesktopShortcutDefault
#### <a name="prevent-desktop-shortcut-creation-upon-install-default"></a>防止在預設安裝時建立桌面捷徑
>Microsoft Edge Update 1.3.128.0 和更新版本

#### <a name="description"></a>說明
在安裝 Microsoft Edge 時，可讓您針對所有通道指定建立桌面捷徑的預設行為。

  如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。
如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。
如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。
如果已安裝 Microsoft Edge，此原則就不會有任何影響。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：CreateDesktopShortcutDefault
- GP 名稱：防止在預設安裝時建立桌面捷徑
- GP 路徑：系統管理範本/Microsoft Edge Update/應用程式
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：CreateDesktopShortcutDefault
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="createdesktopshortcut"></a>CreateDesktopShortcut
#### <a name="prevent-desktop-shortcut-creation-upon-install"></a>防止在安裝時建立桌面捷徑
>Microsoft Edge Update 1.3.128.0 和更新版本

#### <a name="description"></a>說明
如果您啟用此原則，安裝 Microsoft Edge 時會建立桌面捷徑。
如果您停用此原則，安裝 Microsoft Edge 時不會建立桌面捷徑。
如果您未設定此原則，安裝過程中將會建立 Microsoft Edge 的桌面捷徑。
如果已安裝 Microsoft Edge，此原則就不會有任何影響。

  如果您未針對通道設定此原則，[[防止在安裝時建立桌面捷徑預設](#createdesktopshortcutdefault)] 原則設定會決定在安裝 Microsoft Edge 時建立捷徑。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：CreateDesktopShortcut
- GP 名稱：防止在安裝時建立桌面捷徑
- GP 路徑： 
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): CreateDesktopShortcut{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): CreateDesktopShortcut{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): CreateDesktopShortcut{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): CreateDesktopShortcut{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="rollbacktotargetversion"></a>RollbackToTargetVersion
#### <a name="rollback-to-target-version"></a>復原至目標版本
>Microsoft Edge Update 1.3.133.3 和更新版本

#### <a name="description"></a>描述
指定 Microsoft Edge Update 應將 Microsoft Edge 的安裝復原為 '[目標版本覆寫](#targetversionprefix)' 中所示的版本。

只有在設定 '[目標版本覆寫](#targetversionprefix)'，且將 '[更新原則覆寫](#update)' 設定為 [開啟] 狀態 (永遠允許更新、僅限自動無訊息更新、僅限手動更新) 時，此原則才會生效。

如果您停用或未設定此原則，安裝的版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會保留原樣。

如果您啟用這個原則，則目前版本高於 '[目標版本覆寫](#targetversionprefix)' 所指定的版本將會降級為目標版本。

建議使用者安裝最新版本的 Microsoft Edge 瀏覽器，以確保最新安全性更新的保護。 復原到舊版可能會面臨已知的安全性問題。 這項原則可做為暫時修正，以解決 Microsoft Edge 瀏覽器更新中的問題。

在暫時復原瀏覽器版本之前，建議為貴組織中的所有使用者啟用同步處理 ([https://go.microsoft.com/fwlink/?linkid=2133032](https://go.microsoft.com/fwlink/?linkid=2133032))。 如果未開啟同步，就會有瀏覽資料永久遺失的風險。 請自行承擔使用此原則的風險。

注意：您可以在這裡檢視所有可供復原的版本[https://aka.ms/EdgeEnterprise](https://aka.ms/EdgeEnterprise)。

本原則適用於 Microsoft Edge 版本 86 或更新版本。

如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2133918](https://go.microsoft.com/fwlink/?linkid=2133918)。

這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：RollbackToTargetVersion
- GP 名稱：復原至目標版本
- GP 路徑： 
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): RollbackToTargetVersion{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): RollbackToTargetVersion{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): RollbackToTargetVersion{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): RollbackToTargetVersion{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="targetversionprefix"></a>TargetVersionPrefix
#### <a name="target-version-override"></a>目標版本覆寫
>Microsoft Edge Update 1.3.119.43 和更新版本

#### <a name="description"></a>說明
啟用此原則且已啟用 [自動更新] 時，Microsoft Edge 將會更新為此原則值所指定的版本。

原則值必須是指定的 Microsoft Edge 版本，例如，83.0.499.12。

如果裝置的 Microsoft Edge 版本比指定值較新，Microsoft Edge 將會維持較新的版本，而不會降級到指定的版本。

如果指定的版本不存在，或格式不正確，Microsoft Edge 將會維持目前的版本，而不會自動更新至未來的版本。

如需相關資訊，請參閱 [https://go.microsoft.com/fwlink/?linkid=2136707](https://go.microsoft.com/fwlink/?linkid=2136707)。

這個原則只適用於已加入 Microsoft® Active Directory® 網域的 Windows 實例。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：TargetVersionPrefix
- GP 名稱：目標版本覆寫
- GP 路徑： 
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Beta
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Canary
  - 系統管理範本/Microsoft Edge Update/應用程式/Microsoft Edge Dev
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - (Stable): TargetVersionPrefix{56EB18F8-B008-4CBD-B6D2-8C97FE7E9062}
  - (Beta): TargetVersionPrefix{2CD8A007-E189-409D-A2C8-9AF4EF3C72AA}
  - (Canary): TargetVersionPrefix{65C35B14-6C1D-4122-AC46-7148CC9D6497}
  - (Dev): TargetVersionPrefix{0D50BFEC-CD6A-4F9A-964C-C7416E3ACB10}
- 值類型：REG_SZ
##### <a name="example-value"></a>範例值：
```
83.0.499.12
```
[回到頁首](#microsoft-edge---update-policies)

### <a name="updaterexperimentationandconfigurationservicecontrol"></a>UpdaterExperimentationAndConfigurationServiceControl
#### <a name="retrieve-configurations-and-experiments"></a>取回組組和實驗
>Microsoft Edge Update 1.3.145.1 及更高版本

#### <a name="description"></a>描述
在 Microsoft Edge Update，實驗與組組服務是用來部署實驗負載。

實驗有效負載包含 Microsoft 啟用測試意見回應的初期開發功能清單。

如果您啟用此策略，實驗負載會從實驗與組組服務下載。

如果您停用此策略，與實驗與組組服務的通訊會完全停止。

如果您沒有設定此策略，在受管理的裝置上，行為會與策略 '停用'相同。

如果您沒有設定此策略，在未管理裝置上的行為會與策略 '啟用'相同。

#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：UpdateExperimentationAndConfigureationServiceControl
- GP 名稱：Controle updater 與實驗與組組服務的通訊
- GP 路徑：系統管理範本/Microsoftt Edge Update/Microsoft Edge Update
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：UpdaterExperimentationAndConfigurationServiceControl
- 數值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)

## <a name="preferences-policies"></a>喜好設定原則

[回到頁首](#microsoft-edge---update-policies)
### <a name="autoupdatecheckperiodminutes"></a>AutoUpdateCheckPeriodMinutes
#### <a name="auto-update-check-period-override"></a>自動更新檢查期間覆寫
>Microsoft Edge Update 1.2.145.5 和更新版本

#### <a name="description"></a>描述
如果啟用，此原則允許您設定自動更新檢查之間的最小分鐘數值。 否則，預設情況下，每 10 小時會自動檢查一次是否有更新。

  如果要停用所有自動更新檢查，請將值設定為 0 (不建議)。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：AutoUpdateCheckPeriodMinutes
- GP 名稱：自動更新檢查期間覆寫
- GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱：AutoUpdateCheckPeriodMinutes
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000578
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="updatessuppressed"></a>UpdatesSuppressed
#### <a name="time-period-in-each-day-to-suppress-auto-update-check"></a>每天抑制自動更新檢查的期間
>Microsoft Edge Update 1.3.33.5 和更新版本

#### <a name="description"></a>描述
如果啟用此原則，則每天從 Hour:Minute 開始，持續 Duration (分鐘) 抑制檢查更新。 Duration 不受日光節約時間影響。 例如，如果開始時間為 22:00，Duration 為 480 分鐘，則無論日光節約時間在該期間是開始還是結束，都會抑制更新整整 8 小時。

  如果停用或不設定此原則，則在任何特定期間都不會抑制更新檢查。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：UpdatesSuppressed
- GP 名稱：每天抑制自動更新檢查的期間
  - Options { Hour, Minute, Duration }
- GP 路徑：系統管理範本/Microsoft Edge Update/喜好設定
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱： 
  - UpdatesSuppressedDurationMin
  - UpdatesSuppressedStartHour
  - UpdatesSuppressedStartMin
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
duration   : 0x0000003c
start hour : 0x00000001
start min  : 0x00000002
```
[回到頁首](#microsoft-edge---update-policies)

## <a name="proxy-server-policies"></a>Proxy 伺服器原則

[回到頁首](#microsoft-edge---update-policies)
### <a name="proxymode"></a>ProxyMode
#### <a name="choose-how-to-specify-proxy-server-settings"></a>選擇如何指定 Proxy 伺服器設定
>Microsoft Edge Update 1.3.21.81 和更新版本

#### <a name="description"></a>描述
允許您指定 Microsoft Edge Update 使用的 Proxy 伺服器設定。

  如果啟用此原則，則可以在以下 Proxy 伺服器選項之間進行選擇：
   - 如果選擇一律不使用 Proxy 伺服器且一律直接連線，則忽略所有其他選項。
   - 如果選擇使用系統 Proxy 設定或自動偵測 Proxy 伺服器，則忽略所有其他選項。
   - 如果選擇固定伺服器 Proxy 模式，則可在 [[Proxy 伺服器的位址或 URL](#proxyserver)] 原則中指定其他選項。
   - 如果選擇使用 .pac Proxy 指令碼，則必須在 [[Proxy .pac 檔案的 URL](#proxypacurl)] 原則中指定指令碼的 URL。

  如果啟用此原則，則組織的使用者無法變更 Microsoft Edge Update 中的 Proxy 設定。

  如果停用或不設定此原則，則不會設定任何 Proxy 伺服器設定，但組織中的使用者可以為 Microsoft Edge Update 選擇自己的 Proxy 設定。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：ProxyMode
- GP 名稱：選擇如何指定 Proxy 伺服器設定
- GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱︰ProxyMode
- 數值類型：REG_SZ
##### <a name="example-value"></a>範例值：
```
fixed_servers
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="proxypacurl"></a>ProxyPacUrl
#### <a name="url-to-a-proxy-pac-file"></a>Proxy .pac 檔案的 URL
>Microsoft Edge Update 1.3.21.81 和更新版本

#### <a name="description"></a>描述
允許您為 Proxy 自動設定 (PAC) 檔案指定 URL。

  如果啟用此原則，則可以為 PAC 檔案指定 URL，以自動化 Microsoft Edge Update 選取適當 Proxy 伺服器以擷取特定網站的方式。

  已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動 Proxy 設定時，才會套用此原則。

  如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：ProxyPacUrl
- GP 名稱：Proxy .pac 檔案的 URL
- GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱︰ProxyPacUrl
- 數值類型：REG_SZ
##### <a name="example-value"></a>範例值：
```
https://www.microsoft.com
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="proxyserver"></a>ProxyServer
#### <a name="address-or-url-of-proxy-server"></a>Proxy 伺服器的位址或 URL
>Microsoft Edge Update 1.3.21.81 和更新版本

#### <a name="description"></a>描述
允許您指定供 Microsoft Edge Update 使用的 Proxy 伺服器 URL。

  如果啟用此原則，您可在組織中設定 Microsoft Edge Update 所用的 Proxy 伺服器 URL。

  已於 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中選取手動 Proxy 設定時，才會套用此原則。

  如果您已在 [[選擇如何指定 Proxy 伺服器設定](#proxymode)] 原則中指定手動以外的其他 Proxy 設定，請勿設定此原則。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：ProxyServer
- GP 名稱：Proxy 伺服器的位址或 URL
- GP 路徑：系統管理範本/Microsoft Edge Update/Proxy 伺服器
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- 值名稱︰ProxyServer
- 數值類型：REG_SZ
##### <a name="example-value"></a>範例值：
```
https://www.microsoft.com
```
[回到頁首](#microsoft-edge---update-policies)


## <a name="microsoft-edge-webview-policies"></a>Microsoft Edge WebView 原則

[回到頁首](#microsoft-edge---update-policies)
### <a name="install-webview"></a>安裝 (WebView)
#### <a name="allow-installation"></a>允許安裝
>Microsoft Edge Update 1.3.127.1 和更新版本

#### <a name="description"></a>說明
可讓您指定是否可以使用 Microsoft Edge Update 來安裝 Microsoft Edge WebView。

  - 如果您啟用此原則，使用者可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。
  - 如果您停用此原則，使用者無法透過 Microsoft Edge Upadte 安裝 Microsoft Edge WebView。
  - 如果不為設定此原則，則 '[允許安裝預設值](#installdefault)' 原則設定將決定使用者是否可以透過 Microsoft Edge Update 安裝 Microsoft Edge WebView。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：Install
- GP 名稱：允許安裝
- GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - Install{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


### <a name="update-webview"></a>更新 (WebView)
#### <a name="update-policy-override"></a>更新原則覆寫
>Microsoft Edge Update 1.3.127.1 和更新版本

#### <a name="description"></a>說明
可讓您指定是否為 Microsoft Edge WebView 啟用自動更新。 Microsoft Edge WebView 是應用程式用來顯示網路內容的元件。
預設會啟用自動更新。 若要停用 Microsoft Edge WebView 的自動更新，可能會導致與此元件相關的應用程式發生相容性問題。

  如果啟用此原則，Microsoft Edge Update 會根據您設定以下選項的方式處理 Microsoft Edge WebView 更新：
  - 永遠允許更新：會自動下載並套用更新
  - 已停用更新：一律不下載或套用更新

  如果您未啟用此原則，則會自動下載並套用更新。
#### <a name="windows-information-and-settings"></a>Windows 資訊和設定
##### <a name="group-policy-admx-info"></a>群組原則 (ADMX) 資訊
- GP 唯一名稱：Update
- GP 名稱：更新原則覆寫
- GP 路徑：系統管理範本/Microsoft Edge Update/Microsoft Edge WebView
- GP ADMX 檔案名稱：msedgeupdate.admx
##### <a name="windows-registry-settings"></a>Windows 登錄設定
- 路徑：HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\EdgeUpdate
- Value Name: 
  - Update{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
- 值類型：REG_DWORD
##### <a name="example-value"></a>範例值：
```
0x00000001
```
[回到頁首](#microsoft-edge---update-policies)


## <a name="see-also"></a>請參閱
  - [設定 Microsoft Edge](configure-microsoft-edge.md)
  - [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
