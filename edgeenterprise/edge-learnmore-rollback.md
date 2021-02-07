---
title: 適用於企業的 Microsoft Edge 復原
ms.author: v-danwes
author: dan-wesley
manager: srugh
ms.date: 02/04/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 如何將 Microsoft Edge 復原到舊版
ms.openlocfilehash: 2059ea04bf8ec3a03266fe95599ea3b515b78c12
ms.sourcegitcommit: c290b0b0fa6b7d7f94dcdfdda91302da733326ec
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314566"
---
# 如何將 Microsoft Edge 復原到舊版

本文將說明如何使用 [復原] 功能還原為舊版 Microsoft Edge。 若要深入了解此功能，請觀看[影片：Microsoft Edge 版本復原](microsoft-edge-video-version-rollback.md)。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 86 或更新版本。

## 復原簡介

復原可讓您以較舊的版本取代您的 Microsoft Edge 瀏覽器版本。 這項功能旨在成為部署 Microsoft Edge 之企業的安全網。 它可讓您針對 Microsoft Edge 問題進行疑難排解。 復原的好處在於能夠輕鬆快速地復原到舊版的瀏覽器。 「復原」降低 Microsoft Edge 問題對商務運作的潛在影響。

## 開始之前

重要的是要了解如何在 Microsoft Edge 環境中安裝復原功能。 您可以使用兩種不同的方法來部署復原：手動使用 MSI，或使用 Microsoft Edge Update 和群組原則。 我們也鼓勵您使用精選的群組原則，以便更順利地部署。

### 建議

復原功能的目的是暫時解決您在 Microsoft Edge 瀏覽器更新中可能發生的問題。 建議使用者安裝最新版本的 Microsoft Edge 瀏覽器，以使用最新安全性更新提供的保護。 復原到舊版可能會面臨已知的安全性問題。

在暫時復原瀏覽器版本之前，強烈建議為貴組織中的所有使用者啟用同步。 如果未開啟同步，就會有瀏覽資料永久遺失的風險。 如需關於同步的詳細資訊，請參閱 [Microsoft Edge 同步](microsoft-edge-enterprise-sync.md)。

> [!CAUTION]
> 只有在必要時才使用復原，因為始終存在資料遺失的風險。

## 使用 MSI 手動啟用復原

使用下列步驟，以手動方式使用 MSI 復原。

1. 停用 Microsoft Edge 更新。

   > [!NOTE]
   > 我們建議您安裝最新的系統管理範本。 如需詳細資訊，請參閱 [下載並安裝 Microsoft Edge 系統管理範本](https://docs.microsoft.com/DeployEdge/configure-microsoft-edge#1-download-and-install-the-microsoft-edge-administrative-template)。

   - 開啟 [本機群組原則編輯器]，然後移至 *[電腦設定] > [管理範本] > [Microsoft Edge Update] > [應用程式] > [Microsoft Edge] >*。
   - 選取 **[更新原則覆寫]**，然後選取 **[啟用]**。
   - 在 **[選項]** 的 [原則] 下拉式清單中，挑選 **[更新已停用]**。

2. 取得 MSI。

   - 從此處下載您想要復原至 [ ](https://www.microsoft.com/edge/business/download)的 MSI 版本。
   - 將 MSI 儲存到桌面。

3. 執行復原命令。

   - 使用 **以系統管理員身分執行** 開啟 Windows 命令提示字元。
   - 輸入下列命令，其中：*C:\Users\username\Desktop\test*  是下載 MSI 的路徑，而 FileName 是 .msi 的檔案名稱：<br>
 `C:\Users\username\Desktop\test>msiexec /I FileName.msi /qn ALLOWDOWNGRADE=1`<br>
     > [!NOTE]
     > 如需有關 msiexec 的詳細資訊，請參閱 [msiexec](https://docs.microsoft.com/windows-server/administration/windows-commands/msiexec)。
   - 關閉並重新開啟 Microsoft Edge，以驗證復原正常運作。 在 **[設定和更多]** (ALT+F) 底下，移至 **[設定]** 然後選取 **[關於 Microsoft Edge]**。

## 使用 Microsoft Edge Update 和群組原則啟用復原

使用下列步驟，用 Microsoft Edge Update 和群組原則啟用復原。

1. 開啟 [本機群組原則編輯器]，然後移至 *[電腦設定] > [管理範本] > [Microsoft Edge Update] > [應用程式] > [Microsoft Edge] >*。
2. 選取 **[復原至目標版本]**，然後選取 **[啟用]**。
3. 選取 **[目標版本覆寫]**，並挑選要復原的瀏覽器版本。
4. 選取 **[更新原則覆寫]**，然後選取 **[啟用]**。 在 **[選項]** 的 [原則] 下拉式清單中，挑選下列其中一個選項 (**[更新已停用]** 除外)：

   - 永遠允許更新
   - 僅限自動無訊息更新

     > [!NOTE]
     > 若要強制執行群組原則更新，請在 Windows 系統管理員 [命令提示] 處輸入 `gpupdate /force` (以系統管理員身分執行)。

5. 按一下**確定**以儲存原則設定。 下次 Microsoft Edge Update 檢查更新時，將會發生復原。 如果要盡快更新，您可以變更 Microsoft Edge Update 的輪詢間隔，或使用 MSI 啟用復原。

### 常見復原錯誤

下列錯誤會妨礙復原：

- 輸入不支援的目標版本
- 輸入不存在的目標版本
- 輸入資料格式不正確。

### 建議的群組原則

強烈建議使用以下群組原則和設定來進行復原。

#### 同步群組原則

- 強制同步。 將強制同步設定為啟用。 這個原則將強制啟用所有 Azure Active Directory (Azure AD) 使用者的同步處理。 這個原則只適用於 Microsoft Edge 版本 86 及更新版本。
- *[設定] 從 [同步處理原則] 中排除的類型清單* 允許系統管理員控制哪些資料能由使用者進行同步處理。

#### 瀏覽器重新啟動群組原則

建議您在啟用復原之後，強制為使用者重新啟動。

- 啟用 *[通知使用者]，建議或需要重新啟動瀏覽器，以套用擱置中的更新*。 在 [選項] 底下，選取 **[必要]**。
- 啟用 *[設定更新通知的時段]*，然後以毫秒設定所需的時間。

## 快照

快照是 [使用者資料] 資料夾的版本戳複本。 在版本升級期間，會建立舊版本的快照，並儲存在 [快照] 資料夾中。 復原之後，會將與版本相符的快照複製到新的 [使用者資料] 資料夾，並從 [快照] 資料夾中刪除。 如果降級時，沒有與版本相符的快照，復原將會依靠 [同步處理] 以將使用者資料填入新的 Microsoft Edge 版本中。

[UserDataSnapshotRetentionLimit](https://docs.microsoft.com/deployedge/microsoft-edge-policies#userdatasnapshotretentionlimit) 群組原則可讓您設定在特定時間內可保留的快照數目限制。 根據預設，會保留三個快照。 您可以將此原則設定為保留 0-5 個快照。

## 常見問題集

### 手動 MSI 復原

#### 可能會發生哪些常見的 MSI 故障？

1. 如果已停用安裝更新群組原則，將不會發生復原。

   - 若要使用復原，請確認已將安裝設為 **[啟用]**。 停用此原則時，會妨礙安裝 Microsoft Edge 頻道。 如需詳細資訊，請參閱 [安裝](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#install)。

2. 如果沒有啟蒙更新，將會封鎖 Microsoft Edge 安裝，除非 *[允許 Microsoft Edge 並存瀏覽器體驗]* 已啟用。

   - 適用於 Windows 版本 1903 和 1909：如果您的上次更新在 2019 年 10 月之前，可能會遇到此問題。
   - 適用於 Windows 版本 1709、1803 及 1809：如果您的上次更新在 2019 年 11 月之前，可能會遇到此問題。<br>
如需詳細資訊，請參閱 [支援下一版 Microsoft Edge 的 Windows Update](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)。

#### 使用 [命令提示字元] 之後，顯示下列錯誤訊息，而且復原並未發生。 怎麼回事？

![復原狀態訊息](./media/edge-learnmore-rollback/edge-rollback-cmd-flag-error.png)

*ALLOWDOWNGRADE=1* 未執行。

### Microsoft Edge Update 和群組原則復原

#### 我設定 *[復原到目標版本]*、啟用 *[更新原則覆寫]*、輸入 *[目標版本覆寫]* 的預期瀏覽器版本，但瀏覽器版本不符合預期。 怎麼回事？

以下是一些妨礙復原的常見錯誤：

- 如果未設定 [復原到目標版本]，將不會執行復原。
- [目標版本覆寫] 設定有下列其中一個問題：

  - [目標版本覆寫] 設定為不支援的目標版本。
  - [目標版本覆寫] 設定為不存在的目標版本。
  - [目標版本覆寫] 輸入格式不正確。

- 如果 [更新原則覆寫] 設定為 [更新已停用]，Microsoft Edge Update 將不接受任何更新，且不會執行復原。

### 我將所有群組原則設定正確，但是復原並未執行。 發生了什麼事？

Microsoft Edge Update 尚未執行更新檢查。 預設情況下，自動更新每 10 小時會檢查一次是否有更新。 若要修正此問題，您可以使用 [自動更新檢查期間覆寫] 群組原則，以變更 Microsoft Edge Update 的輪詢間隔。 如需詳細資訊，請參閱 [AutoUpdateCheckPeriodMinutes](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#autoupdatecheckperiodminutes) 原則。

### 如果您是 IT 系統管理員，請遵循正確復原的所有步驟。 僅自己使用者群組的一部分會復原。 為什麼其他使用者尚未復原？

群組原則設定尚未同步處理到所有用戶端。 當系統管理員設定群組原則時，用戶端不會立即收到這些設定。 您可以 [[強制遠端群組原則更新]](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/jj134201(v=ws.11))。

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：Microsoft Edge 版本復原](microsoft-edge-video-version-rollback.md)
