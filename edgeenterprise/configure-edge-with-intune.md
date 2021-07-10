---
title: 使用 Microsoft Intune 設定適用於 Windows 的 Microsoft Edge 原則設定
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Microsoft Intune 設定適用於 Windows 的 Microsoft Edge 原則設定。
ms.openlocfilehash: adcd80f68250a9694b9bbaa21fb7941ebcbaf15a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641669"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a><span data-ttu-id="3ae98-103">使用 Microsoft Intune 設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="3ae98-103">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>

<span data-ttu-id="3ae98-104">本文說明如何使用 Microsoft Intune 設定適用於 Windows 10 的 Microsoft Edge 原則設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-104">This article explains how to configure Microsoft Edge policy settings for Windows 10 using Microsoft Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="3ae98-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3ae98-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="3ae98-106">您可以透過將裝置組態設定檔新增到 Microsoft Intune 來設定 Microsoft Edge 原則和設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-106">You can configure Microsoft Edge policies and settings by adding a device configuration profile to Microsoft Intune.</span></span> <span data-ttu-id="3ae98-107">使用 Intune 管理和實施原則，等同於在使用者裝置上使用 Active Directory 群組原則或設定本機群組原則物件 (GPO) 設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-107">Using Intune to manage and enforce policies is equivalent to using Active Directory Group Policy or configuring local Group Policy Object (GPO) settings on user devices.</span></span>

<span data-ttu-id="3ae98-108">如需使用 Microsoft Intune 管理 Microsoft Edge 原則的詳細資訊，您可閱讀[透過搭配 Microsoft Intune 使用 Microsoft Edge 來管理 Web 存取](/intune/manage-microsoft-edge)，但請記住，此連結文章特定於 Microsoft Edge 版本 45 及更早版本，因此可能包含不適用於 Microsoft Edge 企業版 77 及更新版本的資訊和參考。</span><span class="sxs-lookup"><span data-stu-id="3ae98-108">For more information about managing Microsoft Edge policies with Microsoft Intune, you can read [Manage web access by using Microsoft Edge with Microsoft Intune](/intune/manage-microsoft-edge), but keep in mind that the linked article is specific to Microsoft Edge version 45 and earlier and therefore may contain information and references that don't apply to Microsoft Edge Enterprise version 77 and later.</span></span>

> [!TIP]
> <span data-ttu-id="3ae98-109">如需如何使用 Microsoft Intune 在 macOS 上設定 Microsoft Edge 的相關資訊，請參閱[進行 macOS 的設定](configure-microsoft-edge-on-mac.md)。</span><span class="sxs-lookup"><span data-stu-id="3ae98-109">For information on how to configure Microsoft Edge on macOS using Microsoft Intune, see [Configure for macOS](configure-microsoft-edge-on-mac.md).</span></span>

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a><span data-ttu-id="3ae98-110">建立設定檔以在 Microsoft Edge 中管理 Windows 10 的設定</span><span class="sxs-lookup"><span data-stu-id="3ae98-110">Create a profile to manage settings in Microsoft Edge for Windows 10</span></span>

<span data-ttu-id="3ae98-111">在 Microsoft Intune 中使用系統管理範本，您可以使用雲端管理 Windows 10 裝置上的 Microsoft Edge 群組原則。</span><span class="sxs-lookup"><span data-stu-id="3ae98-111">Using Administrative Templates in Microsoft Intune, you can manage Microsoft Edge group policies on your Windows 10 devices using the cloud.</span></span> <span data-ttu-id="3ae98-112">本節將協助您建立範本以設定 Microsoft Edge 專屬的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-112">This section will help you create a template to configure Microsoft Edge-specific application settings.</span></span> <span data-ttu-id="3ae98-113">建立範本時，它會建立裝置組態設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ae98-113">When you create the template, it creates a device configuration profile.</span></span> <span data-ttu-id="3ae98-114">然後，您可以將此設定檔指派或部署到組織中的 Windows 10 裝置。</span><span class="sxs-lookup"><span data-stu-id="3ae98-114">You can then assign or deploy this profile to Windows 10 devices in your organization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3ae98-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="3ae98-115">Prerequisites</span></span>

- <span data-ttu-id="3ae98-116">Windows 10，具有下列最低系統需求︰</span><span class="sxs-lookup"><span data-stu-id="3ae98-116">Windows 10 with the following minimum system requirements:</span></span>
  - <span data-ttu-id="3ae98-117">Windows 10 版本 1909</span><span class="sxs-lookup"><span data-stu-id="3ae98-117">Windows 10, version 1909</span></span>
  - <span data-ttu-id="3ae98-118">Windows 10 版本 1903，需安裝 [KB4512941](https://support.microsoft.com/kb/4512941)</span><span class="sxs-lookup"><span data-stu-id="3ae98-118">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/kb/4512941) installed</span></span>
  - <span data-ttu-id="3ae98-119">Windows 10 版本 1809，需安裝 [KB4512534](https://support.microsoft.com/kb/4512534)</span><span class="sxs-lookup"><span data-stu-id="3ae98-119">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/kb/4512534) installed</span></span>
  - <span data-ttu-id="3ae98-120">Windows 10 版本 1803，需安裝 [KB4512509](https://support.microsoft.com/kb/4512509)</span><span class="sxs-lookup"><span data-stu-id="3ae98-120">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/kb/4512509) installed</span></span>
  - <span data-ttu-id="3ae98-121">Windows 10 版本 1709，需安裝 [KB4516071](https://support.microsoft.com/kb/4516071)</span><span class="sxs-lookup"><span data-stu-id="3ae98-121">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/kb/4516071) installed</span></span>

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a><span data-ttu-id="3ae98-122">使用 [系統管理範本] 建立 Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="3ae98-122">Use Administrative Templates to create a policy for Microsoft Edge</span></span>

<span data-ttu-id="3ae98-123">此程序利用 Intune 內建的系統管理範本 (您可能熟悉的群組原則)。</span><span class="sxs-lookup"><span data-stu-id="3ae98-123">This procedure leverages Administrative templates (which you might be familiar with from Group Policy) that are built into Intune.</span></span> <span data-ttu-id="3ae98-124">您可以使用這些範本來建立 Microsoft Edge 原則，方法是從預先設定的清單中選取 [設定]。</span><span class="sxs-lookup"><span data-stu-id="3ae98-124">You can use these templates to create a policy for Microsoft Edge by selecting settings from a pre-configured list.</span></span>

1. <span data-ttu-id="3ae98-125">登入 [Microsoft 端點管理員](https://endpoint.microsoft.com/) 入口網站。</span><span class="sxs-lookup"><span data-stu-id="3ae98-125">Sign in to the [Microsoft Endpoint Manager](https://endpoint.microsoft.com/) portal.</span></span>
2. <span data-ttu-id="3ae98-126">在左側瀏覽窗格中，選取 **[裝置]**。</span><span class="sxs-lookup"><span data-stu-id="3ae98-126">Select **Devices** in the left-hand navigation pane.</span></span>
3. <span data-ttu-id="3ae98-127">從 **[裝置]** | **概述**中，選取 **[組態設定檔]** (在 [原則] 標題下)。</span><span class="sxs-lookup"><span data-stu-id="3ae98-127">From **Devices** | **Overview**, select **Configuration Profiles** (under Policy heading).</span></span>
4. <span data-ttu-id="3ae98-128">在頂端命令列上，選取**建立設定檔**。</span><span class="sxs-lookup"><span data-stu-id="3ae98-128">On the top command bar, select **Create profile**.</span></span>
5. <span data-ttu-id="3ae98-129">在 **[平台]** 下方的下拉式清單中，選取 **[Windows 10 及更新版本]**。</span><span class="sxs-lookup"><span data-stu-id="3ae98-129">In the drop-down list below **Platform**, select **Windows 10 and later**.</span></span>
6. <span data-ttu-id="3ae98-130">在 **[設定檔]** 下方的下拉式清單中，選取 **[系統管理範本]**，然後按一下 **[建立]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ae98-130">In the drop-down list below **Profile**, select **Administrative Templates** and then click the **Create** button.</span></span> <span data-ttu-id="3ae98-131">下個螢幕擷取畫面顯示可選取 [平台] 和 [設定檔] 類型的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="3ae98-131">The next screenshot shows the drop-down lists to select the platform and type of profile.</span></span>

    ![選取 [平台] 和 [設定檔] 類型](./media/configure-edge-with-intune/create-profile-platform.png)

7. <span data-ttu-id="3ae98-133">在 **[基本資料]** 索引標籤，輸入描述性 **[名稱]**，例如 [Microsoft Edge 原則]。</span><span class="sxs-lookup"><span data-stu-id="3ae98-133">On the **Basics** tab, enter a descriptive **Name**, such as Microsoft Edge Policy.</span></span> <span data-ttu-id="3ae98-134">選擇性輸入原則的 **描述**。</span><span class="sxs-lookup"><span data-stu-id="3ae98-134">Optionally, enter a  **Description** for the policy.</span></span>
<span data-ttu-id="3ae98-135">下個螢幕擷取畫面顯示 **[基本資料]** 索引標籤的表單，而且功能表列會顯示後續步驟 (索引標籤呈現灰色) 來建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ae98-135">The next screenshot shows the form for the **Basics** tab and the menu bar shows the next steps (as grayed out tabs) to create the profile.</span></span>

   ![輸入 [名稱和描述]](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. <span data-ttu-id="3ae98-137">選取 **\[下一步\]**。</span><span class="sxs-lookup"><span data-stu-id="3ae98-137">Select **Next**.</span></span>
9. <span data-ttu-id="3ae98-138">在 **[組態設定]** 索引標籤上，選取下列其中一個位置中的 [Microsoft Edge] 資料夾：</span><span class="sxs-lookup"><span data-stu-id="3ae98-138">On the **Configuration settings** tab, select the Microsoft Edge folder in one of the following locations:</span></span>

   - <span data-ttu-id="3ae98-139">在 [電腦設定] 資料夾下方</span><span class="sxs-lookup"><span data-stu-id="3ae98-139">below the Computer Configuration folder</span></span>
   - <span data-ttu-id="3ae98-140">在 [使用者設定] 資料夾下方。</span><span class="sxs-lookup"><span data-stu-id="3ae98-140">below the User Configuration folder.</span></span>

   <span data-ttu-id="3ae98-141">將會在右側窗格中顯示適用於 Microsoft Edge 的設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-141">The available settings for Microsoft Edge will be shown on the right pane.</span></span> <span data-ttu-id="3ae98-142">例如，下列螢幕擷取畫面所示的*電腦設定/Microsoft Edge/允許下載限制*。</span><span class="sxs-lookup"><span data-stu-id="3ae98-142">For example, *Computer Configuration/Microsoft Edge/Allow download restrictions* shown in the following screenshot.</span></span>

   ![[組態設定] 索引標籤](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > <span data-ttu-id="3ae98-144">如需 Microsoft Edge 所有可用設定的最完整和最新之清單，請參閱 [Microsoft Edge – 原則](./microsoft-edge-policies.md) 和 [Microsoft Edge – 更新原則](./microsoft-edge-update-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="3ae98-144">See [Microsoft Edge – Policies](./microsoft-edge-policies.md) and [Microsoft Edge – Update policies](./microsoft-edge-update-policies.md) for the most complete and up to date list of all the available settings for Microsoft Edge.</span></span>

10. <span data-ttu-id="3ae98-145">使用搜尋欄位 (「搜尋以篩選項目...」) 來尋找您要設定的特定設定。</span><span class="sxs-lookup"><span data-stu-id="3ae98-145">Use the search field ("Search to filter items ...") to find a specific setting you want to configure.</span></span> <span data-ttu-id="3ae98-146">在此範例中，搜尋字串為「首頁」。</span><span class="sxs-lookup"><span data-stu-id="3ae98-146">In this example, the search string is "home page".</span></span> <span data-ttu-id="3ae98-147">下個螢幕擷取畫面顯示搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="3ae98-147">The next screenshot shows the search results.</span></span>

    ![搜尋結果](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. <span data-ttu-id="3ae98-149">當您找到想要設定的設定之後，請選取它以顯示您可以設定的值。</span><span class="sxs-lookup"><span data-stu-id="3ae98-149">After you find the setting you intend to configure, select it to expose the values you can set.</span></span> <span data-ttu-id="3ae98-150">在下個螢幕擷取畫面中，我們選取 [設定首頁 URL] 做為範例。</span><span class="sxs-lookup"><span data-stu-id="3ae98-150">In the next screenshot, we selected "Configure the home page URL" as an example.</span></span>

    ![設定首頁 URL 原則](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. <span data-ttu-id="3ae98-152">啟用原則，並輸入首頁 URL 的值，如上個螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ae98-152">Enable the policy and enter a value for the Home page URL, as shown in the previous screenshot.</span></span>

13. <span data-ttu-id="3ae98-153">按一下 \[確定\] \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="3ae98-153">Click **OK**.</span></span> <span data-ttu-id="3ae98-154">[狀態] 欄位應顯示為 [已啟用]，如下方螢幕擷取畫面範例所示。</span><span class="sxs-lookup"><span data-stu-id="3ae98-154">The settings "State" column should appear as "Enabled", as shown in the following screenshot example.</span></span>

    ![設定狀態已啟用](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. <span data-ttu-id="3ae98-156">按一下 **\[下一步\]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ae98-156">Click the **Next** button.</span></span>

15. <span data-ttu-id="3ae98-157">如果需要，請在 **[範圍標籤]** 索引標籤上，新增一個範圍標籤，否則請按一下 **[下一個]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ae98-157">On the **Scope tags** tab, add a Scope tag if wanted, otherwise click the **Next** button.</span></span>

16. <span data-ttu-id="3ae98-158">在 **[指派]** 索引標籤上，按一下 **[+ 選取要包含的群組]** 將此原則指派給 Azure Active Directory (Azure AD) 群組，其中包含想要接收此原則設定的裝置或使用者。</span><span class="sxs-lookup"><span data-stu-id="3ae98-158">On the **Assignments** tab, click **+ Select groups to include** to assign this policy to the Azure Active Directory (Azure AD) group that contains the devices or the users that you want to receive this policy setting.</span></span> <span data-ttu-id="3ae98-159">請參閱 [在 Microsoft Intune 中指派使用者和裝置設定檔](/intune/device-profile-assign)，以了解如何將設定檔指派給 Azure AD 使用者或裝置群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ae98-159">See [Assign user and device profiles in Microsoft Intune](/intune/device-profile-assign) for information about how to assign the profile to your Azure AD user or device groups.</span></span>

    ![選取要包含的群組](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. <span data-ttu-id="3ae98-161">按一下 **\[下一步\]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ae98-161">Click the **Next** button.</span></span>

18. <span data-ttu-id="3ae98-162">在 **[檢閱 + 建立]** 索引標籤上，檢閱變更摘要以確保其正確無誤，然後按一下 **[建立]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3ae98-162">On the **Review + create** tab, review the summary of your changes to ensure it's correct and then click the **Create** button.</span></span>

19. <span data-ttu-id="3ae98-163">新建立的原則 (Microsoft Edge 原則) 會顯示在下方螢幕擷取畫面中。</span><span class="sxs-lookup"><span data-stu-id="3ae98-163">The newly created policy (Microsoft Edge Policy) is shown in the following screenshot.</span></span>

    ![選取要包含的群組](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

<span data-ttu-id="3ae98-165">如需 Windows 10 設定檔的詳細資訊，請參閱[在 Microsoft Intune 中使用 Windows 10 範本設定群組原則設定](/intune/administrative-templates-windows)。</span><span class="sxs-lookup"><span data-stu-id="3ae98-165">For more information about Windows 10 profiles, see [Use Windows 10 templates to configure group policy settings in Microsoft Intune](/intune/administrative-templates-windows).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ae98-166">也請參閱</span><span class="sxs-lookup"><span data-stu-id="3ae98-166">See also</span></span>

- [<span data-ttu-id="3ae98-167">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="3ae98-167">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="3ae98-168">透過搭配 Microsoft Intune 使用 Microsoft Edge 來管理 Web 存取</span><span class="sxs-lookup"><span data-stu-id="3ae98-168">Manage web access by using Microsoft Edge with Microsoft Intune</span></span>](/intune/manage-microsoft-edge)
- [<span data-ttu-id="3ae98-169">使用 Windows 10 範本在 Microsoft Intune 中設定群組原則設定</span><span class="sxs-lookup"><span data-stu-id="3ae98-169">Use Windows 10 templates to configure group policy settings in Microsoft Intune</span></span>](/intune/administrative-templates-windows)
- [<span data-ttu-id="3ae98-170">使用 Microsoft Intune 部署 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3ae98-170">Deploy Microsoft Edge using Microsoft Intune</span></span>](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)