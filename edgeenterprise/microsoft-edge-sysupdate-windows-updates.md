---
title: Microsoft Edge 的 Windows Update
ms.author: jtkim
author: dan-wesley
manager: srugh
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 的 Windows Update
ms.openlocfilehash: b99d3d7ed048cb829fd2328be9e4e7376334652c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642379"
---
# <a name="windows-updates-to-support-the-next-version-of-microsoft-edge"></a>支援下一版 Microsoft Edge 的 Windows Update

本文介紹 Windows 如何更新為支援下一版 Microsoft Edge。

> [!IMPORTANT]
> 請參閱 Microsoft Edge 產品小組的[部落格文章](https://aka.ms/EdgeLegacyEOS)，以了解舊版 Microsoft Edge 終止服務的相關資訊。

> [!NOTE]
> 本文適用於 Microsoft Edge 穩定通道。

## <a name="microsoft-edge-and-the-windows-release-cycle"></a>Microsoft Edge 和 Windows 發行週期

下一版 Microsoft Edge 具有更頻繁且更靈活的更新功能。 由於瀏覽器版本未繫結到 Windows 主要版本，因此將對作業系統進行變更，以確保下一版 Microsoft Edge 可無縫地適合 Windows。 如此一來，功能更新將會以約 6 週的週期釋出。 安全性與相容性更新將在必要時提供。

## <a name="updates-and-the-user-experience"></a>更新和使用者體驗

在安裝下一版 Microsoft Edge 的 Stable 通道之前，更新不會變更使用者體驗。 安裝 Microsoft Edge Beta、Dev 或 Canary 不會觸發 Windows 中的任何變更。 這些瀏覽器版本將與現有瀏覽器一起安裝。

套用所有更新「並」在系統層級安裝下一版 Microsoft Edge 的 Stable 通道時，以下變更將在系統上生效：

- 目前 Microsoft Edge 版本的所有開始功能表釘選項目、磚和捷徑都將移移至下一版 Microsoft Edge。
- 目前 Microsoft Edge 版本的所有工作列釘選項目和捷徑都將移移至下一版 Microsoft Edge。
- 下一版 Microsoft Edge 將釘選到工作列。 如果目前版本的 Microsoft Edge 已釘選，則將替換它。
- 下一版 Microsoft Edge 將新增捷徑到桌面。 如果目前版本的 Microsoft Edge 已有捷徑，則將替換它。
- 預設情況下，Microsoft Edge 控制代碼的大多數通訊協定將移移至下一版 Microsoft Edge。
- 目前 Microsoft Edge 將從作業系統中的所有 UX 介面隱藏，包括設定、所有應用程式以及任何檔案或通訊協定支援對話方塊。
- 所有對目前版本 Microsoft Edge 的嘗試啟動都將重新導向至下一版 Microsoft Edge。

  > [!NOTE]
  > 使用者層級安裝不會觸發這些行為。

隨著先前的變更，無論是否安裝了下一版 Microsoft Edge 的 Stable 通道，都會發生這些變更。

- Microsoft Edge 將解除登錄下一版 Microsoft Edge 不支援的書籍和 XML 通訊協定。 嘗試開啟這些通訊協定的使用者會看到一個對話方塊，提示他們選擇預設應用程式。 請至[下載 ePub 應用程式以繼續閱讀電子書](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fsupport.microsoft.com%2Fhelp%2F4517840&data=02%7C01%7Cv-danwes%40microsoft.com%7Cc9f8571b880549c30fcf08d72be5eaf9%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637026138803983526&sdata=qtb3DvVZQ6H%2FFXnBievkl%2B%2BngAQXwl340PcH8kRc3y4%3D&reserved=0)深入了解有關圖書支援變更。

## <a name="timeline"></a>時間表

支援所述體驗所需的變更將隨不同版本 Windows 的三個更新一起提供。

### <a name="windows-versions-1903-and-1909"></a>Windows 版本 1903 與 1909

- 選用 2019 年 7 月更新中的第一組變更，隨 2019 年 8 月安全性更新一起提供。
- 選用 2019 年 8 月更新中的第二組變更，隨 2019 年 9 月安全性更新一起提供。

  > [!NOTE]
  > 這是 Microsoft Edge 將解除登錄 XML 通訊協定的更新。

- 選用 2019 年 9 月更新中的第三組變更，隨 2019 年 10 月安全性更新一起提供。

  > [!NOTE]
  > 這是 Microsoft Edge 不再支援電子書的更新。

### <a name="windows-versions-1709-1803-and-1809"></a>Windows 版本 1709、1803 與 1809

- 選用 2019 年 8 月更新中的第一組變更，隨 2019 年 9 月安全性更新一起提供。
- 選用 2019 年 9 月更新中的第二組變更，隨 2019 年 10 月安全性更新一起提供。

  > [!NOTE]
  > 這是 Microsoft Edge 將解除登錄 XML 通訊協定的更新。

- 選用 2019 年 10 月更新中的第三組變更，隨 2019 年 11 月安全性更新一起提供。

  > [!NOTE]
  > 這是 Microsoft Edge 不再支援電子書的更新。

下表提供每組變更中特定更新的詳細資訊。

| Windows 10 | 其他資訊 | 必要下載 |
|--|--|--|
| 版本 1709 | [KB4525241](https://support.microsoft.com/help/4525241/windows-10-update-kb4525241) | [Windows 10 版本 1709 的累積更新](https://www.catalog.update.microsoft.com/Search.aspx?q=4525241) |
| 版本 1803  | [KB4525237](https://support.microsoft.com/help/4525237/windows-10-update-kb4525237) | [Windows 10 版本 1803 的累積更新](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4525237) |
| 版本 1809  | [KB4523205](https://support.microsoft.com/help/4523205/windows-10-update-kb4523205) | [Windows 10 版本 1809 的累積更新](https://www.catalog.update.microsoft.com/Search.aspx?q=4523205) |
| 版本 1903 及 1909 |[KB4517389](https://support.microsoft.com/help/4517389/windows-10-update-kb4517389)  | [Windows 10 版本 1903 和 1909 的累積更新](https://www.catalog.update.microsoft.com/Search.aspx?q=4517389) |

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 文件](./index.yml)