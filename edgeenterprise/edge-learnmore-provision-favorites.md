---
title: 佈建 Microsoft Edge 我的最愛
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 佈建 Microsoft Edge 我的最愛
ms.openlocfilehash: 2d75e9c22a8aa9cc70d8b96c280934137396620a
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978795"
---
# <a name="provision-favorites-for-microsoft-edge"></a>佈建 Microsoft Edge 我的最愛

依據客戶的意見反應，我們已針對佈建我的最愛進行改進。 從 Microsoft Edge 版本 85 開始，系統管理員不再需要手動建立檔案來佈建我的最愛。 系統管理員可以使用 Microsoft Edge UI 新增我的最愛和資料夾，以產生可匯出至群組原則的檔案。

本文說明如何為貴組織佈建一組我的最愛和資料夾。 您可以使用 [[設定我的最愛]](//DeployEdge/microsoft-edge-policies#configure-favorites) 原則來佈建我的最愛和資料夾。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 85 或更新版本。

## <a name="prerequisites-and-recommendations"></a>需求和建議

- Microsoft Edge 版本 85 隨附為群組原則安裝的適當系統管理範本。
- 我們建議您在 Microsoft Edge 中使用新的設定檔來佈建這些我的最愛。 所有與設定檔儲存的我的最愛都會包含在匯出中。  

## <a name="provision-favorites-and-folders"></a>佈建我的最愛與資料夾

使用下列步驟為您的使用者佈建我的最愛和資料夾。

1. 移至 Microsoft Edge 網址列，然後輸入此 URL：*edge://flags/#edge-favorites-admin-export*。
2. 在 **適用於系統管理員的我的最愛設定匯出** (英文) 中，從下拉式清單中挑選 **[啟用]**，然後按一下 **[重新開機]**。

3. 移至 *edge://favorites* 的 **[我的最愛]** 頁面，以便新增您要佈建的我的最愛和資料夾。

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. 將我的最愛和資料夾新增完畢之後，請將它們匯出，就可以根據 **[設定我的最愛]** 原則進行使用。 移至網址列，然後流覽至 *edge://favorites*，按一下省略符號 **[...]**，然後選擇 **[匯出我的最愛設定]**。 下個螢幕畫面會顯示在佈建我的最愛時所具有的選項。

   ![使用我的最愛的功能表選項。](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. 在 **[匯出您的最愛設定]** 底下，您提供使用者將看到的資料夾名稱。 輸入 [資料夾] 名稱，並挑選您要使用的 [平台] 格式。 按一下 **[複製到剪貼簿]**。 下個螢幕畫面會顯示資料夾名稱為 [受管理我的最愛]，且平台為 Windows。

   ![將我的最愛匯出至 Windows 資料夾的對話方塊。](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. 開啟 [群組原則編輯器]，瀏覽至 *[電腦設定]/[系統管理範本]/*，然後選取 **[設定我的最愛]**。 啟用 [設定我的最愛] 原則。 在 **[選項:]** 底下，於 [設定我的最愛] 文字區域中貼上匯出的內容，然後按一下 **[套用]**。 下個螢幕畫面會顯示步驟 5 中 [受管理我的最愛] 資料夾的範例。

   ![使用 GPEdit 啟用並設定 [設定我的最愛] 原則。](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. 按一下 **[確定]** 或 **[套用]** 以儲存此原則設定。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)