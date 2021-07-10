---
title: 使用 System Center Configuration Manager 部署 Microsoft Edge
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 了解如何使用 System Center Configuration Manager (SCCM) 部署 Microsoft Edge。
ms.openlocfilehash: b0efa986c7f230f455d052f8e003616e081e324a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641579"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a><span data-ttu-id="825b4-103">使用 System Center Configuration Manager 部署 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="825b4-103">Deploy Microsoft Edge using System Center Configuration Manager</span></span>

<span data-ttu-id="825b4-104">本文介紹如何使用 System Center Configuration Manager (SCCM) 自動執行 Microsoft Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="825b4-104">This article shows you how to automate a Microsoft Edge deployment by using System Center Configuration Manager (SCCM).</span></span>

>[!NOTE]
><span data-ttu-id="825b4-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="825b4-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="825b4-106">在您開始前</span><span class="sxs-lookup"><span data-stu-id="825b4-106">Before you begin</span></span>

<span data-ttu-id="825b4-107">請檢閱[介紹 Configuration Manager 中的應用程式管理](/sccm/apps/understand/introduction-to-application-management)中的資訊。</span><span class="sxs-lookup"><span data-stu-id="825b4-107">Review the information in [Introduction to application management in Configuration Manager](/sccm/apps/understand/introduction-to-application-management).</span></span> <span data-ttu-id="825b4-108">此應用程式管理文章可協助您了解本文中使用的術語，並可做為準備網站以安裝應用程式的指南。</span><span class="sxs-lookup"><span data-stu-id="825b4-108">This application management article will help you understand the terminology used in this article and is a guide to preparing your site to install applications.</span></span>

<span data-ttu-id="825b4-109">從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 企業安裝檔案 (**MicrosoftEdgeDevEnterpriseX64.msi** 和/或 **MicrosoftEdgeDevEnterpriseX86.msi**)。</span><span class="sxs-lookup"><span data-stu-id="825b4-109">Download the Microsoft Edge Enterprise installation files (**MicrosoftEdgeDevEnterpriseX64.msi** and/or **MicrosoftEdgeDevEnterpriseX86.msi**) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise).</span></span>

<span data-ttu-id="825b4-110">請確保將 Microsoft Edge 安裝檔案儲存在可存取的網路位置。</span><span class="sxs-lookup"><span data-stu-id="825b4-110">Make sure you store the Microsoft Edge installation files in an accessible network location.</span></span>

## <a name="create-the-application"></a><span data-ttu-id="825b4-111">建立應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-111">Create the application</span></span>

<span data-ttu-id="825b4-112">您將使用 Configuration Manager 精靈建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-112">You'll create the application using a Configuration Manager wizard.</span></span>

### <a name="start-the-create-application-wizard-and-create-the-application"></a><span data-ttu-id="825b4-113">啟動建立應用程式精靈並建立應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-113">Start the Create Application Wizard and create the application</span></span>  

1. <span data-ttu-id="825b4-114">在 Configuration Manager 主控台中，按一下**軟體程式庫** > **應用程式管理** > **應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-114">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>  

2. <span data-ttu-id="825b4-115">在**首頁**索引標籤的**建立**群組中，按一下**建立應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-115">On the **Home** tab, in the **Create** group, click **Create Application**.</span></span> <span data-ttu-id="825b4-116">或者，在瀏覽器列的**應用程式**上按右鍵，然後按一下**建立應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-116">Or, right-click on **Applications** in the navigation bar and then click **Create Application**.</span></span>

    ![建立應用程式](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. <span data-ttu-id="825b4-118">在**建立應用程式精靈**的**一般**頁面，選取**從安裝檔案自動偵測此應用程式的相關資訊**。</span><span class="sxs-lookup"><span data-stu-id="825b4-118">On the **General** page of the **Create Application Wizard**, choose **Automatically detect information about this application from installation files**.</span></span> <span data-ttu-id="825b4-119">這將會使用從安裝 .msi 檔案中提取的資訊，在精靈中預先填入一些資訊。</span><span class="sxs-lookup"><span data-stu-id="825b4-119">This pre-populates some of the information in the wizard with information that's extracted from the installation .msi file.</span></span> <span data-ttu-id="825b4-120">提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="825b4-120">Provide the following information:</span></span>  

   - <span data-ttu-id="825b4-121">**類型**：選擇 **Windows Installer (\*.msi 檔案)**。</span><span class="sxs-lookup"><span data-stu-id="825b4-121">**Type**: Choose **Windows Installer (\*.msi file)**.</span></span>  

   - <span data-ttu-id="825b4-122">**位置**：鍵入安裝檔案 **MicrosoftEdgeDevEnterpriseX64.msi** 或 **MicrosoftEdgeDevEnterpriseX86.msi** 的位置 (或按一下**瀏覽**以選取位置)。</span><span class="sxs-lookup"><span data-stu-id="825b4-122">**Location**: Type the location (or click **Browse** to select the location) of the installation file **MicrosoftEdgeDevEnterpriseX64.msi** or **MicrosoftEdgeDevEnterpriseX86.msi**.</span></span> <span data-ttu-id="825b4-123">請注意，必須以 *\\\Server\Share\File* 格式指定位置，Configuration Manager 才能找到安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="825b4-123">Note that the location must be specified in the form *\\\Server\Share\File* for Configuration Manager to locate the installation files.</span></span>  

   <span data-ttu-id="825b4-124">您的**指定此應用程式的設定**頁面看起來會像下列範例：</span><span class="sxs-lookup"><span data-stu-id="825b4-124">Your **Specify settings for this application** page will look like the following example:</span></span>  

    ![指定此應用程式的設定](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. <span data-ttu-id="825b4-126">按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-126">Click **Next**.</span></span> <span data-ttu-id="825b4-127">在**匯入的資訊**頁面上的**詳細資料**下，您將看到有關應用程式和匯入的任何關聯檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="825b4-127">Under **Details** on the **Imported Information** page, you'll see information about the application and any associated files that were imported.</span></span> <span data-ttu-id="825b4-128">按**下一步**以繼續進行精靈。</span><span class="sxs-lookup"><span data-stu-id="825b4-128">Click **Next** to continue with the wizard.</span></span>  

    ![檢視匯入的資訊](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. <span data-ttu-id="825b4-130">在**一般資訊**頁面上，可以新增有關應用程式的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="825b4-130">On the **General Information** page, you can add more information about the application.</span></span> <span data-ttu-id="825b4-131">例如，軟體版本、系統管理員註解和發行者。</span><span class="sxs-lookup"><span data-stu-id="825b4-131">For example, Software version, Administrator comments, and Publisher.</span></span> <span data-ttu-id="825b4-132">您可以使用此資訊來協助在 Configuration Manager 主控台中排序和尋找應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-132">You can use this information to to help you sort and find the application in the Configuration Manager console.</span></span>

   <span data-ttu-id="825b4-133">您還可以使用**安裝程式**欄位指定將用於在電腦上安裝應用程式的完整命令列。</span><span class="sxs-lookup"><span data-stu-id="825b4-133">You can also use the **Installation program** field to specify the full command line that will be used to install the application on PCs.</span></span> <span data-ttu-id="825b4-134">您可以對此進行編輯以新增您自己的內容 (例如，用於自動安裝的 **/q**)。</span><span class="sxs-lookup"><span data-stu-id="825b4-134">You can edit this to add your own properties (for example, **/q** for an unattended installation).</span></span>

   <span data-ttu-id="825b4-135">以下螢幕擷取畫面顯示一個範例，其中使用了**指定此應用程式的資訊**欄位。</span><span class="sxs-lookup"><span data-stu-id="825b4-135">The following screenshot shows an example where the **Specify information about this application** fields are used.</span></span>

   ![指定應用程式中繼資料](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. <span data-ttu-id="825b4-137">按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-137">Click **Next**.</span></span>
7. <span data-ttu-id="825b4-138">在**摘要**頁面上，您可以在**詳細資訊**下確認應用程式設定，然後使用精靈完成。</span><span class="sxs-lookup"><span data-stu-id="825b4-138">On the **Summary** page, you can confirm your application settings under **Details** and then finish using the wizard.</span></span> <span data-ttu-id="825b4-139">按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-139">Click **Next**.</span></span>  

    ![應用程式設定的詳細資料](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. <span data-ttu-id="825b4-141">在**完成**頁面上，按一下**關閉**。</span><span class="sxs-lookup"><span data-stu-id="825b4-141">On the **Completion** page, click **Close**.</span></span>

    ![成功對話方塊](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

<span data-ttu-id="825b4-143">您已完成建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-143">You've finished creating the application.</span></span> <span data-ttu-id="825b4-144">使用以下步驟在 Configuration Manager 中查看它：</span><span class="sxs-lookup"><span data-stu-id="825b4-144">Use the following steps to see it in Configuration Manager:</span></span>

- <span data-ttu-id="825b4-145">選取**軟體程式庫**工作區</span><span class="sxs-lookup"><span data-stu-id="825b4-145">select the **Software Library** workspace</span></span>
- <span data-ttu-id="825b4-146">展開**應用程式管理**</span><span class="sxs-lookup"><span data-stu-id="825b4-146">expand **Application Management**</span></span>
- <span data-ttu-id="825b4-147">按一下**應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-147">click **Applications**.</span></span>

<span data-ttu-id="825b4-148">下面的螢幕擷取畫面顯示用於本文的範例。</span><span class="sxs-lookup"><span data-stu-id="825b4-148">The following screenshot shows the example used for this article.</span></span>  

![應用程式](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a><span data-ttu-id="825b4-150">變更應用程式內容和部署設定</span><span class="sxs-lookup"><span data-stu-id="825b4-150">Change application properties and deployment settings</span></span>

<span data-ttu-id="825b4-151">建立應用程式後，如有需要，可以精簡應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="825b4-151">After you create an application, you can refine the application settings if you need to.</span></span> <span data-ttu-id="825b4-152">若要查看應用程式內容：</span><span class="sxs-lookup"><span data-stu-id="825b4-152">To look at the application properties:</span></span>

- <span data-ttu-id="825b4-153">選取應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-153">select the application</span></span>
- <span data-ttu-id="825b4-154">在**首頁**>**內容**中按一下**內容**。</span><span class="sxs-lookup"><span data-stu-id="825b4-154">in **Home**>**Properties**, click **Properties**.</span></span>  

   ![設定應用程式內容](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 <span data-ttu-id="825b4-156">在 **<application name\> 應用程式內容**對話方塊中，您將看到項目的索引標籤式檢視，您可設定這些項目以變更應用程式的行為。</span><span class="sxs-lookup"><span data-stu-id="825b4-156">In the **<application name\> Application Properties** dialog page, you'll see a tabbed view of the items that you can configure to change the behavior of the application.</span></span> <span data-ttu-id="825b4-157">如需有關您可進行之設定的詳細資訊，請參閱[建立應用程式](/sccm/apps/deploy-use/create-applications)。</span><span class="sxs-lookup"><span data-stu-id="825b4-157">For more information about the settings you can configure, see [Create applications](/sccm/apps/deploy-use/create-applications).</span></span>

<span data-ttu-id="825b4-158">在此範例中，您將變更應用程式部署類型的一些內容。</span><span class="sxs-lookup"><span data-stu-id="825b4-158">For this example, you'll change some properties of the application's deployment type.</span></span> <span data-ttu-id="825b4-159">若要變更部署內容：</span><span class="sxs-lookup"><span data-stu-id="825b4-159">To change the deployment properties:</span></span>

1. <span data-ttu-id="825b4-160">按一下**部署類型**索引標籤。</span><span class="sxs-lookup"><span data-stu-id="825b4-160">Click the **Deployment Types** tab.</span></span>
2. <span data-ttu-id="825b4-161">在**部署類型**下，選取應用程式**名稱**</span><span class="sxs-lookup"><span data-stu-id="825b4-161">Under **Deployment types:**, select the application **Name**</span></span>
3. <span data-ttu-id="825b4-162">按一下**編輯**。</span><span class="sxs-lookup"><span data-stu-id="825b4-162">Click **Edit**.</span></span>

   ![編輯部署類型](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a><span data-ttu-id="825b4-164">新增需求至部署類型</span><span class="sxs-lookup"><span data-stu-id="825b4-164">Add a requirement to the deployment type</span></span>

 <span data-ttu-id="825b4-165">需求指定必須符合的條件，才可以在裝置上安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-165">Requirements specify conditions that must be met before an application is installed on a device.</span></span> <span data-ttu-id="825b4-166">您可以從內建需求中進行選擇，也可以建立自己的需求。</span><span class="sxs-lookup"><span data-stu-id="825b4-166">You can choose from built-in requirements or you can create your own.</span></span> <span data-ttu-id="825b4-167">例如，您可以新增一項需求，要求應用程式僅安裝在執行 Windows 10 **x86** 或 **x64** 的電腦上，具體取決於安裝檔案的目標處理器架構。</span><span class="sxs-lookup"><span data-stu-id="825b4-167">For example, you can add a requirement that the application will only be installed on PCs that are running Windows 10 **x86** or **x64**, depending on the installation file's target processor architecture.</span></span> <span data-ttu-id="825b4-168">在此範例中，您將指定 Windows 10 **x86**。</span><span class="sxs-lookup"><span data-stu-id="825b4-168">In this example, you'll specify Windows 10 **x86**.</span></span>

1. <span data-ttu-id="825b4-169">從剛剛開啟的部署類型內容頁面中，按一下**需求**索引標籤。</span><span class="sxs-lookup"><span data-stu-id="825b4-169">From the deployment type properties page you just opened, click the **Requirements** tab.</span></span>

2. <span data-ttu-id="825b4-170">按一下**新增**以開啟**建立需求**對話方塊。</span><span class="sxs-lookup"><span data-stu-id="825b4-170">Click **Add** to open the **Create Requirement** dialog.</span></span>

    ![建立需求](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. <span data-ttu-id="825b4-172">在**建立需求**對話方塊中，指定下列資訊：</span><span class="sxs-lookup"><span data-stu-id="825b4-172">In the **Create Requirement** dialog box, specify the following information:</span></span>

    - <span data-ttu-id="825b4-173">**類別**：**裝置**</span><span class="sxs-lookup"><span data-stu-id="825b4-173">**Category**: **Device**</span></span>  

    - <span data-ttu-id="825b4-174">**條件**：**作業系統**</span><span class="sxs-lookup"><span data-stu-id="825b4-174">**Condition**: **Operating system**</span></span>  

    - <span data-ttu-id="825b4-175">**規則類型**：**值**</span><span class="sxs-lookup"><span data-stu-id="825b4-175">**Rule type**: **Value**</span></span>  

    - <span data-ttu-id="825b4-176">**運算子**：**其中之一**</span><span class="sxs-lookup"><span data-stu-id="825b4-176">**Operator**: **One of**</span></span>  

    - <span data-ttu-id="825b4-177">從作業系統清單中，選取 **Windows 10** > **所有 Windows 10 (32 位元)**。</span><span class="sxs-lookup"><span data-stu-id="825b4-177">From the operating systems list, select **Windows 10** > **All Windows 10 (32-bit)**.</span></span>  

    <span data-ttu-id="825b4-178">完成後，對話方塊將類似於以下螢幕擷取畫面範例：</span><span class="sxs-lookup"><span data-stu-id="825b4-178">When you're finished, the dialog will look like the following screenshot example:</span></span>

    ![新增需求](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. <span data-ttu-id="825b4-180">按一下**確定**以關閉每個開啟的內容頁，然後返回 Configuration Manager 主控台中的**應用程式**清單。</span><span class="sxs-lookup"><span data-stu-id="825b4-180">Click **OK** to close each open property page and return to the **Applications** list in the Configuration Manager console.</span></span>  

## <a name="add-the-application-content-to-a-distribution-point"></a><span data-ttu-id="825b4-181">將應用程式內容新增到發佈點</span><span class="sxs-lookup"><span data-stu-id="825b4-181">Add the application content to a distribution point</span></span>  

<span data-ttu-id="825b4-182">若要將更新的應用程式部署到 PC，請確保將應用程式內容複製到發佈點。</span><span class="sxs-lookup"><span data-stu-id="825b4-182">To deploy the updated application to PCs, make sure that the application content is copied to a distribution point.</span></span> <span data-ttu-id="825b4-183">電腦會存取發佈點以安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-183">PCs access the distribution point to install the application.</span></span>  

>[!TIP]
><span data-ttu-id="825b4-184">若要深入了解 Configuration Manager 中的發佈點和內容管理，請參閱[部署和管理 System Center Configuration Manager 的內容](/sccm/core/servers/deploy/configure/deploy-and-manage-content)。</span><span class="sxs-lookup"><span data-stu-id="825b4-184">To find out more about distribution points and content management in Configuration Manager, see [Deploy and manage content for System Center Configuration Manager](/sccm/core/servers/deploy/configure/deploy-and-manage-content).</span></span>  

1. <span data-ttu-id="825b4-185">在 Configuration Manager 主控台中，按一下**軟體程式庫**。</span><span class="sxs-lookup"><span data-stu-id="825b4-185">In the Configuration Manager console, click **Software Library**.</span></span>  

2. <span data-ttu-id="825b4-186">在**軟體程式庫**工作區內，展開**應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-186">In the **Software Library** workspace, expand **Applications**.</span></span> <span data-ttu-id="825b4-187">在應用程式清單中選取您建立的應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-187">Select the application you created in the list of applications.</span></span>

3. <span data-ttu-id="825b4-188">在**部署**群組的**首頁**索引標籤中，按一下**發佈內容**。</span><span class="sxs-lookup"><span data-stu-id="825b4-188">On the **Home** tab in the **Deployment** group, click **Distribute Content**.</span></span>  

4. <span data-ttu-id="825b4-189">在**發佈內容精靈**的**一般**頁面中，檢查應用程式名稱是否正確，然後按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-189">On the **General** page of the **Distribute Content Wizard**, check that the application name is correct, and then click **Next**.</span></span>  

5. <span data-ttu-id="825b4-190">在**內容**頁面上，檢閱將要複製至發佈點的資訊，然後按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-190">On the **Content** page, review the information that will be copied to the distribution point, and then click **Next**.</span></span>  

6. <span data-ttu-id="825b4-191">在**內容目的地**頁面上，按一下**新增**以選取要在其上安裝應用程式內容的一或多個集合、發佈點或發佈點群組。</span><span class="sxs-lookup"><span data-stu-id="825b4-191">On the **Content Destination** page, click **Add** to select one or more collections, distribution points, or distribution point groups on which to install the application content.</span></span>

7. <span data-ttu-id="825b4-192">完成精靈。</span><span class="sxs-lookup"><span data-stu-id="825b4-192">Complete the wizard.</span></span>

<span data-ttu-id="825b4-193">您可以在**發佈狀態** > **內容狀態**下，從**監控**工作區檢查應用程式內容是否已成功複製到發佈點。</span><span class="sxs-lookup"><span data-stu-id="825b4-193">You can check that the application content was copied successfully to the distribution point from the **Monitoring** workspace, under **Distribution Status** > **Content Status**.</span></span>  

## <a name="deploy-the-application"></a><span data-ttu-id="825b4-194">部署應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-194">Deploy the application</span></span>  

<span data-ttu-id="825b4-195">接下來，將應用程式部署到階層中的裝置集合。</span><span class="sxs-lookup"><span data-stu-id="825b4-195">Next, deploy the application to a device collection in your hierarchy.</span></span> <span data-ttu-id="825b4-196">在此範例中，您將應用程式部署到**所有系統**裝置集合。</span><span class="sxs-lookup"><span data-stu-id="825b4-196">In this example, you deploy the application to the **All Systems** device collection.</span></span>  

>[!TIP]
><span data-ttu-id="825b4-197">請記住，由於您之前選取的需求，只有指定處理器架構的 Windows 10 電腦才會安裝該應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-197">Remember that only Windows 10 computers of the specified processor architecture will install the application because of the requirements that you selected earlier.</span></span>  

1. <span data-ttu-id="825b4-198">在 Configuration Manager 主控台中，按一下**軟體程式庫** > **應用程式管理** > **應用程式**。</span><span class="sxs-lookup"><span data-stu-id="825b4-198">In the Configuration Manager console, click **Software Library** > **Application Management** > **Applications**.</span></span>

2. <span data-ttu-id="825b4-199">在應用程式清單中，選取您稍早建立的應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-199">From the list of applications, select the application that you created earlier.</span></span> <span data-ttu-id="825b4-200">接著，在**部署**群組的**首頁**索引標籤，按一下**部署**或在應用程式上按右鍵，然後選取**部署**。</span><span class="sxs-lookup"><span data-stu-id="825b4-200">Then, on the **Home** tab in the **Deployment** group, click **Deploy**, or right-click the application and select **Deploy**.</span></span>

    ![部署應用程式](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. <span data-ttu-id="825b4-202">在**部署軟體精靈**的**一般**頁面上，按一下**瀏覽**以選取要將應用程式部署到的裝置集合。</span><span class="sxs-lookup"><span data-stu-id="825b4-202">On the **General** page of the **Deploy Software Wizard**, click **Browse** to select the device collection to which you want to deploy the application.</span></span>

    ![瀏覽至安裝檔案](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. <span data-ttu-id="825b4-204">在**內容**頁面上，檢查是否選取了希望電腦安裝應用程式的發佈點。</span><span class="sxs-lookup"><span data-stu-id="825b4-204">On the **Content** page, check that the distribution point from which you want PCs to install the application is selected.</span></span>

    ![指定發佈點](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. <span data-ttu-id="825b4-206">在**部署設定**頁面上，確保部署動作設定為**安裝**，並且部署目的設定為**必要**。</span><span class="sxs-lookup"><span data-stu-id="825b4-206">On the **Deployment Settings** page, make sure that the deployment action is set to **Install**, and the deployment purpose is set to **Required**.</span></span>

    ![進行部署設定](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    ><span data-ttu-id="825b4-208">透過將部署目的設定為**必要**，可以確保應用程式安裝在符合您所設定需求的電腦上。</span><span class="sxs-lookup"><span data-stu-id="825b4-208">By setting the deployment purpose to **Required**, you make sure that the application is installed on PCs that meet the requirements that you set.</span></span> <span data-ttu-id="825b4-209">如果將此值設定為**可用**，則使用者可以視需求從軟體中心安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-209">If you set this value to **Available**, then users can install the application on demand from Software Center.</span></span>  

6. <span data-ttu-id="825b4-210">在**排程**頁面上，可以設定何時安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-210">On the **Scheduling** page, you can configure when the application will be installed.</span></span> <span data-ttu-id="825b4-211">對於此範例，選取**在可用時間之後盡快**。</span><span class="sxs-lookup"><span data-stu-id="825b4-211">For this example, select **As soon as possible after the available time**.</span></span>

    ![排程部署](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. <span data-ttu-id="825b4-213">在**使用者經驗**頁面上，選取所需的值然後按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-213">On the **User Experience** page, select your desired values and click **Next**.</span></span>

    ![指定使用者體驗](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. <span data-ttu-id="825b4-215">指定所需的警示選項，然後按**下一步**。</span><span class="sxs-lookup"><span data-stu-id="825b4-215">Specify your desired alert options and click **Next**.</span></span>

    ![指定警示設定](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. <span data-ttu-id="825b4-217">完成精靈。</span><span class="sxs-lookup"><span data-stu-id="825b4-217">Complete the wizard.</span></span>

<span data-ttu-id="825b4-218">使用以下**監控應用程式**一節中的資訊，查看應用程式部署的狀態。</span><span class="sxs-lookup"><span data-stu-id="825b4-218">Use the information in the following **Monitor the application** section to see the status of your application deployment.</span></span>  

## <a name="monitor-the-application"></a><span data-ttu-id="825b4-219">監控應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-219">Monitor the application</span></span>

 <span data-ttu-id="825b4-220">在本節中，您將快速檢視剛剛部署之應用程式的部署狀態。</span><span class="sxs-lookup"><span data-stu-id="825b4-220">In this section, you'll take a quick look at the deployment status of the application that you just deployed.</span></span>  

### <a name="to-review-the-deployment-status"></a><span data-ttu-id="825b4-221">若要檢閱部署狀態</span><span class="sxs-lookup"><span data-stu-id="825b4-221">To review the deployment status</span></span>  

1. <span data-ttu-id="825b4-222">在 Configuration Manager 主控台中，按一下**監控** > **部署**。</span><span class="sxs-lookup"><span data-stu-id="825b4-222">In the Configuration Manager console, click **Monitoring** > **Deployments**.</span></span>  

2. <span data-ttu-id="825b4-223">從部署清單中選取應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-223">From the list of deployments, select the application.</span></span>

    ![監控部署](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. <span data-ttu-id="825b4-225">在**部署**群組的**首頁**索引標籤中，按一下**檢視狀態**。</span><span class="sxs-lookup"><span data-stu-id="825b4-225">On the **Home** tab in the **Deployment** group, click **View Status**.</span></span>  

4. <span data-ttu-id="825b4-226">選擇以下索引標籤之一，查看有關應用程式部署的更多狀態更新：</span><span class="sxs-lookup"><span data-stu-id="825b4-226">Select one of the following tabs to see more status updates about the application deployment:</span></span>  

    - <span data-ttu-id="825b4-227">**成功**：應用程式已成功安裝在指示的電腦上。</span><span class="sxs-lookup"><span data-stu-id="825b4-227">**Success**: The application installed successfully on the indicated PCs.</span></span>  

    - <span data-ttu-id="825b4-228">**進行中**：應用程式尚未完成安裝。</span><span class="sxs-lookup"><span data-stu-id="825b4-228">**In Progress**: The application has not yet finished installing.</span></span>  

    - <span data-ttu-id="825b4-229">**錯誤**：在指示的電腦上安裝應用程式時出錯。</span><span class="sxs-lookup"><span data-stu-id="825b4-229">**Error**: An error occurred installing the application on the indicated PCs.</span></span> <span data-ttu-id="825b4-230">還會顯示有關該錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="825b4-230">Further information about the error is also displayed.</span></span>  

    - <span data-ttu-id="825b4-231">**不符合需求**：未在指示的裝置上進行安裝嘗試，因為裝置不符合您設定的需求 (在此範例中，則是因為它們不在 Windows 10 上執行)。</span><span class="sxs-lookup"><span data-stu-id="825b4-231">**Requirements Not Met**: No installation attempt was made on the indicated devices because they did not meet the requirements you configured (in this example, because they do not run on Windows 10.)</span></span>

    - <span data-ttu-id="825b4-232">**不明**： Configuration Manager 無法報告部署狀態。</span><span class="sxs-lookup"><span data-stu-id="825b4-232">**Unknown**: Configuration Manager was unable to report the status of the deployment.</span></span> <span data-ttu-id="825b4-233">請稍後再回來查看。</span><span class="sxs-lookup"><span data-stu-id="825b4-233">Check back again later.</span></span>  

    >[!TIP]
    ><span data-ttu-id="825b4-234">有幾個方式可以監控應用程式部署。</span><span class="sxs-lookup"><span data-stu-id="825b4-234">There are several ways you can monitor application deployments.</span></span> <span data-ttu-id="825b4-235">如需詳細資訊，請參閱[從 System Center Configuration Manager 主控台監控應用程式](/sccm/apps/deploy-use/monitor-applications-from-the-console)。</span><span class="sxs-lookup"><span data-stu-id="825b4-235">For more information, see [Monitor applications from the System Center Configuration Manager console](/sccm/apps/deploy-use/monitor-applications-from-the-console).</span></span>  

## <a name="end-user-experience"></a><span data-ttu-id="825b4-236">使用者經驗</span><span class="sxs-lookup"><span data-stu-id="825b4-236">End-user experience</span></span>  

<span data-ttu-id="825b4-237">具有由 Configuration Manager 管理且執行指定處理器架構 Windows 10 電腦的使用者會看到一則訊息，告知必須安裝 Microsoft Edge Dev 應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-237">Users who have PCs that are managed by Configuration Manager and are running Windows 10 of the specified processor architecture, will see a message telling them that they must install the Microsoft Edge Dev application.</span></span> <span data-ttu-id="825b4-238">當他們接受此安裝選項時，就會安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="825b4-238">When they accept this installation option, the application is installed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="825b4-239">也請參閱</span><span class="sxs-lookup"><span data-stu-id="825b4-239">See also</span></span>

- [<span data-ttu-id="825b4-240">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="825b4-240">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="825b4-241">使用 System Center Configuration Manager 建立及部署應用程式</span><span class="sxs-lookup"><span data-stu-id="825b4-241">Create and deploy an application with System Center Configuration Manager</span></span>](/sccm/apps/get-started/create-and-deploy-an-application)