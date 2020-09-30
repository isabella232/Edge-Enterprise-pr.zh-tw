---
title: 佈建 Microsoft Edge 我的最愛
ms.author: capoon
author: dan-wesley
manager: abutcher
ms.date: 09/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 佈建 Microsoft Edge 我的最愛
ms.openlocfilehash: 94bd42573bdbc0fd1b971ded1c82e5fe152acc54
ms.sourcegitcommit: 854dd73eb168960c0eb4b483f81a8efe88806a64
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088689"
---
# <span data-ttu-id="d7343-103">佈建 Microsoft Edge 我的最愛</span><span class="sxs-lookup"><span data-stu-id="d7343-103">Provision favorites for Microsoft Edge</span></span>

<span data-ttu-id="d7343-104">依據客戶的意見反應，我們已針對佈建我的最愛進行改進。</span><span class="sxs-lookup"><span data-stu-id="d7343-104">Based on customer feedback, we've made improvements to provisioning favorites.</span></span> <span data-ttu-id="d7343-105">從 Microsoft Edge 版本 85 開始，系統管理員不再需要手動建立檔案來佈建我的最愛。</span><span class="sxs-lookup"><span data-stu-id="d7343-105">Starting with Microsoft Edge version 85, Admins no longer have to manually craft a file to provision favorites.</span></span> <span data-ttu-id="d7343-106">系統管理員可以使用 Microsoft Edge UI 新增我的最愛和資料夾，以產生可匯出至群組原則的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7343-106">Admins can add favorites and folders using the Microsoft Edge UI to generate a file that can be exported to a group policy.</span></span>

<span data-ttu-id="d7343-107">本文說明如何為貴組織佈建一組我的最愛和資料夾。</span><span class="sxs-lookup"><span data-stu-id="d7343-107">This article describes how to provision a set of favorites and folders for your organization.</span></span> <span data-ttu-id="d7343-108">您可以使用 [[設定我的最愛]](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) 原則來佈建我的最愛和資料夾。</span><span class="sxs-lookup"><span data-stu-id="d7343-108">You can use the [Configure favorites](https://docs.microsoft.com//DeployEdge/microsoft-edge-policies#configure-favorites) policy to provision favorites and folders.</span></span>

> [!NOTE]
> <span data-ttu-id="d7343-109">本文適用於 Microsoft Edge 版本 85 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d7343-109">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="d7343-110">需求和建議</span><span class="sxs-lookup"><span data-stu-id="d7343-110">Prerequisites and recommendations</span></span>

- <span data-ttu-id="d7343-111">Microsoft Edge 版本 85 隨附為群組原則安裝的適當系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="d7343-111">Microsoft Edge version 85 with the appropriate administrative template installed for group policies.</span></span>
- <span data-ttu-id="d7343-112">我們建議您在 Microsoft Edge 中使用新的設定檔來佈建這些我的最愛。</span><span class="sxs-lookup"><span data-stu-id="d7343-112">We recommend that you use a new profile in Microsoft Edge to provision these favorites.</span></span> <span data-ttu-id="d7343-113">所有與設定檔儲存的我的最愛都會包含在匯出中。</span><span class="sxs-lookup"><span data-stu-id="d7343-113">All favorites that are saved with the profile will be included in the export.</span></span>  

## <span data-ttu-id="d7343-114">佈建我的最愛與資料夾</span><span class="sxs-lookup"><span data-stu-id="d7343-114">Provision favorites and folders</span></span>

<span data-ttu-id="d7343-115">使用下列步驟為您的使用者佈建我的最愛和資料夾。</span><span class="sxs-lookup"><span data-stu-id="d7343-115">Use the following steps to provision favorites and folders for your users.</span></span>

1. <span data-ttu-id="d7343-116">移至 Microsoft Edge 網址列，然後輸入此 URL：*edge://flags/#edge-favorites-admin-export*。</span><span class="sxs-lookup"><span data-stu-id="d7343-116">Go to the Microsoft Edge address bar and type this URL: *edge://flags/#edge-favorites-admin-export*.</span></span>
2. <span data-ttu-id="d7343-117">在 **適用於系統管理員的我的最愛設定匯出** (英文) 中，從下拉式清單中挑選 **[啟用]**，然後按一下 **[重新開機]**。</span><span class="sxs-lookup"><span data-stu-id="d7343-117">Under **Favorites configuration export for administrators**, pick **Enabled** from the dropdown list and then click **Restart**.</span></span>

3. <span data-ttu-id="d7343-118">移至 *edge://favorites* 的 **[我的最愛]** 頁面，以便新增您要佈建的我的最愛和資料夾。</span><span class="sxs-lookup"><span data-stu-id="d7343-118">Go to the **Favorites** page at *edge://favorites* so you can add the favorites and folders that you want to provision.</span></span>

<!--
4. On the **Favorites bar**, click **Add folder**. The folder structure of favorites that are set in the profile you're using will be reflected in the folder you provision for your users. The next screenshot shows "Managed favorites", the folder we'll use to provision favorites.

   ![Add a folder](media/edge-learnmore-provision-favorites/provision-favorites-add-folder.png)

   > [!TIP]
   > Add existing folders that contain favorites you want to provision for your users.

5. Select "Managed favorites" and then click **Add favorite**. The next screenshot shows the favorite we've added.

   ![Add a favorite](media/edge-learnmore-provision-favorites/provision-favorites-add-favorite.png)-->

4. <span data-ttu-id="d7343-119">將我的最愛和資料夾新增完畢之後，請將它們匯出，就可以根據 **[設定我的最愛]** 原則進行使用。</span><span class="sxs-lookup"><span data-stu-id="d7343-119">When you finish adding favorites and folders you'll export them so they can be used by the **Configure favorites** policy.</span></span> <span data-ttu-id="d7343-120">移至網址列，然後流覽至 *edge://favorites*，按一下省略符號 **[...]**，然後選擇 **[匯出我的最愛設定]**。</span><span class="sxs-lookup"><span data-stu-id="d7343-120">Go to the address bar and navigate to *edge://favorites*, click the ellipsis "**…**" and choose **Export favorites configuration**.</span></span> <span data-ttu-id="d7343-121">下個螢幕畫面會顯示在佈建我的最愛時所具有的選項。</span><span class="sxs-lookup"><span data-stu-id="d7343-121">The next screenshot shows the options you have when provisioning favorites.</span></span>

   ![使用我的最愛的功能表選項。](media/edge-learnmore-provision-favorites/provision-favorites-menu-options.png)

5. <span data-ttu-id="d7343-123">在 **[匯出您的最愛設定]** 底下，您提供使用者將看到的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="d7343-123">Under **Export your favorites configuration** you provide a name for the folder that your users will see.</span></span> <span data-ttu-id="d7343-124">輸入 [資料夾] 名稱，並挑選您要使用的 [平台] 格式。</span><span class="sxs-lookup"><span data-stu-id="d7343-124">Type the Folder name and pick the Platform format you want to use.</span></span> <span data-ttu-id="d7343-125">按一下 **[複製到剪貼簿]**。</span><span class="sxs-lookup"><span data-stu-id="d7343-125">Click **Copy to clipboard**.</span></span> <span data-ttu-id="d7343-126">下個螢幕畫面會顯示資料夾名稱為 [受管理我的最愛]，且平台為 Windows。</span><span class="sxs-lookup"><span data-stu-id="d7343-126">The next screenshot shows "Managed favorites" for the folder name and the platform is Windows.</span></span>

   ![將我的最愛匯出至 Windows 資料夾的對話方塊。](media/edge-learnmore-provision-favorites/provision-favorites-export.png)

6. <span data-ttu-id="d7343-128">開啟 [群組原則編輯器]，瀏覽至 *[電腦設定]/[系統管理範本]/*，然後選取 **[設定我的最愛]**。</span><span class="sxs-lookup"><span data-stu-id="d7343-128">Open the Group Policy Editor, navigate to *Computer Configuration/Administrative Templates/* and pick **Configure Favorites**.</span></span> <span data-ttu-id="d7343-129">啟用 [設定我的最愛] 原則。</span><span class="sxs-lookup"><span data-stu-id="d7343-129">Enable the "Configure Favorites" policy.</span></span> <span data-ttu-id="d7343-130">在 **[選項:]** 底下，於 [設定我的最愛] 文字區域中貼上匯出的內容，然後按一下 **[套用]**。</span><span class="sxs-lookup"><span data-stu-id="d7343-130">Under **Options:**, paste the exported contents in the Configure favorites text area then click **Apply**.</span></span> <span data-ttu-id="d7343-131">下個螢幕畫面會顯示步驟 5 中 [受管理我的最愛] 資料夾的範例。</span><span class="sxs-lookup"><span data-stu-id="d7343-131">The next screenshot shows an example of the "Managed favorites" folder from step 5.</span></span>

   ![使用 GPEdit 啟用並設定 [設定我的最愛] 原則。](media/edge-learnmore-provision-favorites/provision-favorites-gpedit.png)

7. <span data-ttu-id="d7343-133">按一下 **[確定]** 或 **[套用]** 以儲存此原則設定。</span><span class="sxs-lookup"><span data-stu-id="d7343-133">Click **OK** or **Apply** to safe the policy settings.</span></span>

## <span data-ttu-id="d7343-134">請參閱</span><span class="sxs-lookup"><span data-stu-id="d7343-134">See also</span></span>

- [<span data-ttu-id="d7343-135">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="d7343-135">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)