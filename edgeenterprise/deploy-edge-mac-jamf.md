---
title: 使用 Jamf 自動執行適用於 macOS 的 Microsoft Edge 部署
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 09/30/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 如何使用 Jamf 自動執行適用於 macOS 的 Microsoft Edge 部署。
ms.openlocfilehash: 3065e4f02dbfed70b887a60b1cf076335dbff19a
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979419"
---
# <span data-ttu-id="b707c-103">使用 Jamf 部署到 macOS</span><span class="sxs-lookup"><span data-stu-id="b707c-103">Deploy to macOS with Jamf</span></span>

<span data-ttu-id="b707c-104">本文介紹如何使用 Jamf 部署適用於 macOS 的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b707c-104">This article describes how to deploy Microsoft Edge for macOS using Jamf.</span></span>

> [!NOTE]
> <span data-ttu-id="b707c-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b707c-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="b707c-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="b707c-106">Prerequisites</span></span>

<span data-ttu-id="b707c-107">開始部署 Microsoft Edge 之前，請確定符合下列必要條件：</span><span class="sxs-lookup"><span data-stu-id="b707c-107">Before you deploy Microsoft Edge, make sure you meet the following prerequisites:</span></span>

- <span data-ttu-id="b707c-108">Microsoft Edge 安裝檔案 **MicrosoftEdgeDev-\<version\>.pkg** 位於網路上的可存取位置。</span><span class="sxs-lookup"><span data-stu-id="b707c-108">The Microsoft Edge installation file,  **MicrosoftEdgeDev-\<version\>.pkg** is in an accessible location on your network.</span></span> <span data-ttu-id="b707c-109">您可從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 企業安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="b707c-109">You can download the Microsoft Edge Enterprise installation files from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>
- <span data-ttu-id="b707c-110">您有 Jamf Cloud 帳戶，該帳戶具有建立安裝檔案並將其部署到電腦所需的存取和權限等級。</span><span class="sxs-lookup"><span data-stu-id="b707c-110">You have a Jamf Cloud account with the level of access and privileges needed to create and deploy installation files to computers.</span></span>

## <span data-ttu-id="b707c-111">若要使用 Jamf 部署 Microsoft Edge：</span><span class="sxs-lookup"><span data-stu-id="b707c-111">To deploy Microsoft Edge using Jamf:</span></span>

1. <span data-ttu-id="b707c-112">登入到 Jamf 並移至**所有設定。**</span><span class="sxs-lookup"><span data-stu-id="b707c-112">Sign on to Jamf and go to **All Settings**.</span></span>

    ![開啟所有設定](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. <span data-ttu-id="b707c-114">在**所有設定**下，按一下**電腦管理**。</span><span class="sxs-lookup"><span data-stu-id="b707c-114">Under **All Settings**, click **Computer Management**.</span></span>

    ![選取電腦管理](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. <span data-ttu-id="b707c-116">在**電腦管理**下，按一下**套件**。</span><span class="sxs-lookup"><span data-stu-id="b707c-116">Under **Computer Management**, click **Packages**.</span></span>

    ![選取套件](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. <span data-ttu-id="b707c-118">在**套件**頁面上，按一下 **+ 新增**以新增新套件。</span><span class="sxs-lookup"><span data-stu-id="b707c-118">On the **Packages** page, click **+ New** to add a new package.</span></span>

    ![選取新增以新增套件](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. <span data-ttu-id="b707c-120">在**新增套件**頁面上，輸入有關套件的詳細資訊，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="b707c-120">On the **New Package** page, enter the details about the package and then click **Save**.</span></span> <span data-ttu-id="b707c-121">(例如，「顯示名稱」、「資訊」或「備註」。)</span><span class="sxs-lookup"><span data-stu-id="b707c-121">(For example, DISPLAY NAME, INFO, or NOTES.)</span></span>

    ![選取儲存以儲存套件資訊](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. <span data-ttu-id="b707c-123">選取功能表列上的**電腦**，然後在瀏覽器列中選取**原則**。</span><span class="sxs-lookup"><span data-stu-id="b707c-123">Select **Computers** on the menu bar, and then select **Policies** in the navigation bar.</span></span>

7. <span data-ttu-id="b707c-124">選取 **+ 新增**以顯示**新增原則**窗格。</span><span class="sxs-lookup"><span data-stu-id="b707c-124">Select **+ New** to display the **New Policy** pane.</span></span>

    ![選取新增以建立新原則](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. <span data-ttu-id="b707c-126">在**選項**索引標籤上，選取**一般**。</span><span class="sxs-lookup"><span data-stu-id="b707c-126">On the **Options** tab, select **General**.</span></span>

    - <span data-ttu-id="b707c-127">在**顯示名稱**下，輸入原則的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b707c-127">Under **DISPLAY NAME**, enter the display name for the policy.</span></span>
    - <span data-ttu-id="b707c-128">在**觸發**下，選取將觸發原則的事件。</span><span class="sxs-lookup"><span data-stu-id="b707c-128">Under **Trigger**, select the event that will trigger the policy.</span></span> <span data-ttu-id="b707c-129">(在上述範例中，事件為 [啟動]。)</span><span class="sxs-lookup"><span data-stu-id="b707c-129">(In the following example, the event is Startup.)</span></span>

    ![輸入部署資訊](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. <span data-ttu-id="b707c-131">在**選項**索引標籤上，按一下**套件**。</span><span class="sxs-lookup"><span data-stu-id="b707c-131">On the **Options** tab, click **Packages**.</span></span>

10. <span data-ttu-id="b707c-132">在**設定套件**快顯視窗上，按一下**設定**。</span><span class="sxs-lookup"><span data-stu-id="b707c-132">On the **Configure Packages** popup, click **Configure**.</span></span>

    ![設定套件](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. <span data-ttu-id="b707c-134">您新增的套件顯示在**套件**窗格中。</span><span class="sxs-lookup"><span data-stu-id="b707c-134">The package that you added shows on the **Packages** pane.</span></span> <span data-ttu-id="b707c-135">按一下**新增**。</span><span class="sxs-lookup"><span data-stu-id="b707c-135">Click **Add**.</span></span> <span data-ttu-id="b707c-136">對於此範例，套件是以下螢幕擷取畫面中的 "MicrosoftEdgeBeta"。</span><span class="sxs-lookup"><span data-stu-id="b707c-136">For this example, the package is "MicrosoftEdgeBeta" in the following screenshot.</span></span>

    ![新增套件](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. <span data-ttu-id="b707c-138">在**新增原則**頁面上，使用下拉式清單選取原則要執行的**發佈點**和**動作**。</span><span class="sxs-lookup"><span data-stu-id="b707c-138">On the **New Policy** page, uUse the drop-down lists to select the **DISTRIBUTION POINT** and **ACTION** to take for the policy.</span></span> <span data-ttu-id="b707c-139">按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="b707c-139">Click **Save**.</span></span> <span data-ttu-id="b707c-140">以下螢幕擷取畫面使用 [每台電腦的預設發佈點] 和 [安裝] 作為範例。</span><span class="sxs-lookup"><span data-stu-id="b707c-140">The following screenshot uses "Each computer's default distribution point" and "Install" as an example.</span></span>

    ![選取發佈點和動作](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. <span data-ttu-id="b707c-142">在**新增原則**頁面上，選取**範圍**索引標籤。您可以根據電腦或使用者來管理部署範圍。</span><span class="sxs-lookup"><span data-stu-id="b707c-142">On the **New Policy** page, select the **Scope** tab. You can manage the scope of the deployment based on computers or users.</span></span> <span data-ttu-id="b707c-143">在此範例中，從**目標電腦**下拉式清單中選取**所有電腦**，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="b707c-143">For this example, select **All Computers** from the **TARGET COMPUTERS** drop-down list and then click **Save**.</span></span>

    ![選取部署範圍](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. <span data-ttu-id="b707c-145">此時，您可以查看 Microsoft Edge 部署原則。</span><span class="sxs-lookup"><span data-stu-id="b707c-145">At this point you can review the Microsoft Edge deployment policy.</span></span> <span data-ttu-id="b707c-146">如果部署選項符合您的要求，請按一下**完成**。</span><span class="sxs-lookup"><span data-stu-id="b707c-146">If the deployment options meet your requirements, click **Done**.</span></span>

    ![按一下完成](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > <span data-ttu-id="b707c-148">您可以隨時返回部署原則以變更設定。</span><span class="sxs-lookup"><span data-stu-id="b707c-148">You can return to a deployment policy at any time to change settings.</span></span>

<span data-ttu-id="b707c-149">恭喜！</span><span class="sxs-lookup"><span data-stu-id="b707c-149">Congratulations!</span></span> <span data-ttu-id="b707c-150">您剛剛完成設定 Jamf 以部署適用於 macOS 的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="b707c-150">You’ve just finished configuring Jamf to deploy Microsoft Edge for macOS.</span></span> <span data-ttu-id="b707c-151">當您定義的觸發條件為 true 時，套件將部署到指定的電腦。</span><span class="sxs-lookup"><span data-stu-id="b707c-151">When the trigger condition you defined is true, the package will get deployed to the computers you specified.</span></span>

## <span data-ttu-id="b707c-152">也請參閱</span><span class="sxs-lookup"><span data-stu-id="b707c-152">See also</span></span>

- [<span data-ttu-id="b707c-153">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="b707c-153">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="b707c-154">Jamf.com</span><span class="sxs-lookup"><span data-stu-id="b707c-154">Jamf.com</span></span>](https://www.jamf.com/)
- [<span data-ttu-id="b707c-155">將 Jamf 與 Microsoft Intune 整合</span><span class="sxs-lookup"><span data-stu-id="b707c-155">Integrate Jamf with Microsoft Intune</span></span>](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)
