---
title: 設定適用於 Windows 的 Microsoft Edge
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 在 Windows 裝置上設定 Microsoft Edge 原則設定
ms.openlocfilehash: a5db4352e723539843a5ad80a7b067e670bced5c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641999"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows"></a><span data-ttu-id="831cb-103">在 Windows 上設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="831cb-103">Configure Microsoft Edge policy settings on Windows</span></span>

<span data-ttu-id="831cb-104">使用以下資訊，在 Windows 裝置上設定 Microsoft Edge 原則設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-104">Use the following information to configure Microsoft Edge policy settings on your Windows devices.</span></span>

> [!NOTE]
> <span data-ttu-id="831cb-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="831cb-105">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="configure-policy-settings-on-windows"></a><span data-ttu-id="831cb-106">在 Windows 上進行原則設定</span><span class="sxs-lookup"><span data-stu-id="831cb-106">Configure policy settings on Windows</span></span>

<span data-ttu-id="831cb-107">您可以使用_群組原則物件 (GPO)_ 來進行 Microsoft Edge 的原則設定，以及管理所有 Windows 版本的 Microsoft Edge Update。</span><span class="sxs-lookup"><span data-stu-id="831cb-107">You can use _group policy objects (GPO)_ to configure policy settings for Microsoft Edge and managed Microsoft Edge updates on all versions of Windows.</span></span> <span data-ttu-id="831cb-108">您也可以透過加入 Microsoft Active Directory 網域之 Windows 裝置的登錄或 Microsoft Intune 中為裝置管理註冊的 Windows 10 專業版或企業執行個體來佈建原則。</span><span class="sxs-lookup"><span data-stu-id="831cb-108">You can also provision policy through the registry for Windows devices that are joined to a Microsoft Active Directory domain, or Windows 10 Pro or Enterprise instances enrolled for device management in Microsoft Intune.</span></span> <span data-ttu-id="831cb-109">若要使用群組原則物件來設定 Microsoft Edge，請安裝_系統管理範本_，以將 Microsoft Edge 的規則和設定新增到 Active Directory 網域中的群組原則集中存放區或個別電腦上的原則定義範本資料夾，然後設定您要設定的特定原則。</span><span class="sxs-lookup"><span data-stu-id="831cb-109">To configure Microsoft Edge with group policy objects, you install _administrative templates_ that add rules and settings for Microsoft Edge to the group policy Central Store in your Active Directory domain or to the Policy Definition template folder on individual computers and then configure the specific policies you want to set.</span></span>

<span data-ttu-id="831cb-110">如果您希望在網域層級管理原則，可以使用 Active Directory 群組原則來設定 Microsoft Edge 原則設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-110">You can use Active Directory group policy to configure Microsoft Edge policy settings if you prefer to manage policy at the domain level.</span></span> <span data-ttu-id="831cb-111">這使您能夠全域管理原則設定，將不同的原則設定定位到特定 OU，或使用 WMI 篩選僅將設定套用至特定查詢傳回的使用者或電腦。</span><span class="sxs-lookup"><span data-stu-id="831cb-111">This enables you to manage policy settings globally, targeting different policy settings to specific OUs, or using WMI filters to apply settings only to users or computers returned by a particular query.</span></span> <span data-ttu-id="831cb-112">如果要在個別電腦上設定原則，則可使用目標電腦上的本機群組原則編輯器，套用僅影響本機裝置的原則設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-112">If you want to configure policy on individual computers, you can apply policy settings that only affect the local device using the Local Group Policy Editor on the target computer.</span></span>

<span data-ttu-id="831cb-113">Microsoft Edge 同時支援_強制_原則和_建議_原則。</span><span class="sxs-lookup"><span data-stu-id="831cb-113">Microsoft Edge supports both _mandatory_ and _recommended_ policies.</span></span> <span data-ttu-id="831cb-114">強制原則會覆寫使用者喜好設定並阻止使用者變更喜好設定，而建議原則提供可由使用者覆寫的預設設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-114">Mandatory policies override user preferences and prevents the user from changing it, while recommended policy provide a default setting that may be overridden by the user.</span></span> <span data-ttu-id="831cb-115">大部分原則僅是強制的；子集是強制和建議的。</span><span class="sxs-lookup"><span data-stu-id="831cb-115">Most policies are mandatory only; a subset are mandatory and recommended.</span></span> <span data-ttu-id="831cb-116">如果同時設定了兩個版本的原則，則強制設定優先。</span><span class="sxs-lookup"><span data-stu-id="831cb-116">If both versions of a policy are set, the mandatory setting takes precedence.</span></span> <span data-ttu-id="831cb-117">建議的原則只有在使用者尚未修改設定時才生效。</span><span class="sxs-lookup"><span data-stu-id="831cb-117">A recommended policy only takes effect when the user has not modified the setting.</span></span>

>[!TIP]
> <span data-ttu-id="831cb-118">您可以使用 Microsoft Intune 來設定 Microsoft Edge 原則設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-118">You can use Microsoft Intune to configure Microsoft Edge policy settings.</span></span> <span data-ttu-id="831cb-119">如需詳細資訊，請參閱[使用 Microsoft Intune 設定 Microsoft Edge](configure-edge-with-intune.md)。</span><span class="sxs-lookup"><span data-stu-id="831cb-119">For more information, see [Configure Microsoft Edge using Microsoft Intune](configure-edge-with-intune.md).</span></span>

<span data-ttu-id="831cb-120">Microsoft Edge 有兩個系統管理範本，兩種範本都可以在電腦或 Active Directory 網域層級套用：</span><span class="sxs-lookup"><span data-stu-id="831cb-120">There are two administrative templates for Microsoft Edge, both of which can be applied either at the computer or Active Directory domain level:</span></span>

- <span data-ttu-id="831cb-121">*msedge.admx*，[設定 Microsoft Edge 設定](microsoft-edge-policies.md)</span><span class="sxs-lookup"><span data-stu-id="831cb-121">*msedge.admx* to [configure Microsoft Edge settings](microsoft-edge-policies.md)</span></span>
- <span data-ttu-id="831cb-122">*msedgeupdate.admx*，[管理 Microsoft Edge Update](microsoft-edge-update-policies.md)。</span><span class="sxs-lookup"><span data-stu-id="831cb-122">*msedgeupdate.admx* to [manage Microsoft Edge updates](microsoft-edge-update-policies.md).</span></span>

<span data-ttu-id="831cb-123">若要開始使用，請下載並安裝 Microsoft Edge 系統管理範本。</span><span class="sxs-lookup"><span data-stu-id="831cb-123">To get started, download and install the Microsoft Edge administrative template.</span></span>

### <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a><span data-ttu-id="831cb-124">1. 下載並安裝 Microsoft Edge 系統管理範本</span><span class="sxs-lookup"><span data-stu-id="831cb-124">1. Download and install the Microsoft Edge administrative template</span></span>

<span data-ttu-id="831cb-125">如果要在 Active Directory 中設定 Microsoft Edge 原則設定，請將檔案下載到可從網域控制站或安裝了遠端伺服器管理工具 (RSAT) 的工作站存取的網路位置。</span><span class="sxs-lookup"><span data-stu-id="831cb-125">If you want to configure Microsoft Edge policy settings in Active Directory, download the files to a network location you can access from a domain controller or a workstation with the Remote Server Administration Tools (RSAT) installed.</span></span> <span data-ttu-id="831cb-126">若要在個別電腦上設定，只需將檔案下載到該電腦上即可。</span><span class="sxs-lookup"><span data-stu-id="831cb-126">To configure on an individual computer, simply download the files to that computer.</span></span>

<span data-ttu-id="831cb-127">將系統管理範本檔案新增到適當位置時，Microsoft Edge 原則設定可立即在群組原則編輯器中使用。</span><span class="sxs-lookup"><span data-stu-id="831cb-127">When you add the administrative template files to the appropriate location, Microsoft Edge policy settings are immediately available in the Group Policy Editor.</span></span>

<span data-ttu-id="831cb-128">移至 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (*MicrosoftEdgePolicyTemplates.cab*)，並解壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="831cb-128">Go to the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) to download the Microsoft Edge policy templates file (*MicrosoftEdgePolicyTemplates.cab*) and extract the contents.</span></span>

#### <a name="add-the-administrative-template-to-active-directory"></a><span data-ttu-id="831cb-129">將系統管理範本新增到 Active Directory</span><span class="sxs-lookup"><span data-stu-id="831cb-129">Add the administrative template to Active Directory</span></span>

1. <span data-ttu-id="831cb-130">在網域控制站或具有 RSAT 的工作站上，瀏覽到網域中任何網域控制站上的 **PolicyDefinition** 資料夾 (也稱為_集中存放區_)。</span><span class="sxs-lookup"><span data-stu-id="831cb-130">On a domain controller or workstation with RSAT, browse to the **PolicyDefinition** folder (also known as the _Central Store_) on any domain controller for your domain.</span></span> <span data-ttu-id="831cb-131">對於舊版 Windows 伺服器，您可能需要建立 PolicyDefinition 資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-131">For older versions of Windows Server, you may need to create the PolicyDefinition folder.</span></span> <span data-ttu-id="831cb-132">如需詳細資訊，請參閱[如何在 Windows 中建立及管理群組原則系統管理範本的集中存放區](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。</span><span class="sxs-lookup"><span data-stu-id="831cb-132">For more information, see [How to create and manage the Central Store for Group Policy Administrative Templates in Windows](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra).</span></span>
2. <span data-ttu-id="831cb-133">開啟 *MicrosoftEdgePolicyTemplates* 並移至 **windows** > **admx**。</span><span class="sxs-lookup"><span data-stu-id="831cb-133">Open *MicrosoftEdgePolicyTemplates* and go to **windows** > **admx**.</span></span>
3. <span data-ttu-id="831cb-134">將 *msedge.admx* 檔案複製到 PolicyDefinition 資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-134">Copy the *msedge.admx* file to the PolicyDefinition folder.</span></span> <span data-ttu-id="831cb-135">(範例：%systemroot%\sysvol\domain\policies\PolicyDefinitions)</span><span class="sxs-lookup"><span data-stu-id="831cb-135">(Example: %systemroot%\sysvol\domain\policies\PolicyDefinitions)</span></span>
4. <span data-ttu-id="831cb-136">在 *admx* 資料夾中，開啟適當的語言資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-136">In the *admx* folder, open the appropriate language folder.</span></span> <span data-ttu-id="831cb-137">例如，如果您在美國，則開啟 **en-US** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-137">For example, if you’re in the U.S., open the **en-US** folder.</span></span>
5. <span data-ttu-id="831cb-138">將 *msedge.adml* 檔案複製到 PolicyDefinition 資料夾中的相符語言資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-138">Copy the *msedge.adml* file to the matching language folder in the PolicyDefinition folder.</span></span> <span data-ttu-id="831cb-139">如果資料夾不存在，請加以建立。</span><span class="sxs-lookup"><span data-stu-id="831cb-139">Create the folder if it does not already exist.</span></span> <span data-ttu-id="831cb-140">(範例：%systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)</span><span class="sxs-lookup"><span data-stu-id="831cb-140">(Example: %systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)</span></span>
6. <span data-ttu-id="831cb-141">如果您的網域有多個網域控制站，則新的 ADMX 檔案將在下一個網域複寫間隔時複寫到它們上。</span><span class="sxs-lookup"><span data-stu-id="831cb-141">If your domain has more than one domain controller, the new ADMX files will be replicated to them at the next domain replication interval.</span></span>
7. <span data-ttu-id="831cb-142">若要確認是否正確載入檔案，請從 Windows 系統管理工具開啟**群組原則管理編輯器**並展開**電腦設定** > **原則** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="831cb-142">To confirm the files loaded correctly, open the **Group Policy Management Editor** from Windows Administrative Tools and expand **Computer Configuration** > **Policies** > **Administrative Templates** > **Microsoft Edge**.</span></span> <span data-ttu-id="831cb-143">您應該會看到一個或多個 Microsoft Edge 節點，如下所示。</span><span class="sxs-lookup"><span data-stu-id="831cb-143">You should see one or more Microsoft Edge nodes as shown below.</span></span>

    ![Microsoft Edge 原則](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### <a name="add-the-administrative-template-to-an-individual-computer"></a><span data-ttu-id="831cb-145">將系統管理範本新增到個別電腦</span><span class="sxs-lookup"><span data-stu-id="831cb-145">Add the administrative template to an individual computer</span></span>

1. <span data-ttu-id="831cb-146">在目標電腦上，開啟 *MicrosoftEdgePolicyTemplates* 並移至 **windows** > **admx**。</span><span class="sxs-lookup"><span data-stu-id="831cb-146">On the target computer, open *MicrosoftEdgePolicyTemplates* and go to **windows** > **admx**.</span></span>
2. <span data-ttu-id="831cb-147">將 *msedge.admx* 檔案複製到原則定義範本資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-147">Copy the *msedge.admx* file to your Policy Definition template folder.</span></span> <span data-ttu-id="831cb-148">(範例：C:\Windows\PolicyDefinitions)</span><span class="sxs-lookup"><span data-stu-id="831cb-148">(Example: C:\Windows\PolicyDefinitions)</span></span>
3. <span data-ttu-id="831cb-149">在 *admx* 資料夾中，開啟適當的語言資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-149">In the *admx* folder, open the appropriate language folder.</span></span> <span data-ttu-id="831cb-150">例如，如果您在美國，則開啟 **en-US** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-150">For example, if you’re in the U.S., open the **en-US** folder.</span></span>
4. <span data-ttu-id="831cb-151">將 *msedge.adml* 檔案複製到原則定義資料夾中的相符語言資料夾。</span><span class="sxs-lookup"><span data-stu-id="831cb-151">Copy the *msedge.adml* file to the matching language folder in your Policy Definition folder.</span></span> <span data-ttu-id="831cb-152">(範例：C:\Windows\PolicyDefinitions\en-US)</span><span class="sxs-lookup"><span data-stu-id="831cb-152">(Example: C:\Windows\PolicyDefinitions\en-US)</span></span>
5. <span data-ttu-id="831cb-153">若要確認是否正確載入檔案，請直接開啟本機群組原則編輯器 (Windows 鍵 + R 並輸入 gpedit.msc) 或開啟 MMC 並載入 [本機群組原則編輯器] 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="831cb-153">To confirm the files loaded correctly either open Local Group Policy Editor directly (Windows key + R and enter gpedit.msc) or open MMC and load the Local Group Policy Editor snap-in.</span></span> <span data-ttu-id="831cb-154">如果發生錯誤，通常是因為檔案位於錯誤的位置。</span><span class="sxs-lookup"><span data-stu-id="831cb-154">If an error occurs, it’s usually because the files are in an incorrect location.</span></span>

### <a name="2-set-mandatory-or-recommended-policies"></a><span data-ttu-id="831cb-155">2. 設定強制或建議原則</span><span class="sxs-lookup"><span data-stu-id="831cb-155">2. Set mandatory or recommended policies</span></span>

<span data-ttu-id="831cb-156">您可以設定強制或建議原則，以便使用群組原則編輯器為 Active Directory 和個別電腦設定 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="831cb-156">You can set mandatory or recommended policies to configure Microsoft Edge with the Group Policy Editor for both Active Directory and individual computers.</span></span> <span data-ttu-id="831cb-157">您可以透過選取適當的節點 (如下所述)，將原則設定的範圍限定為**電腦設定**或**使用者設定**。</span><span class="sxs-lookup"><span data-stu-id="831cb-157">You can scope policy settings to either the **Computer Configuration** or **User Configuration** by selecting the appropriate node as described below.</span></span>

- <span data-ttu-id="831cb-158">若要設定強制原則，請開啟群組原則編輯器並移至 (**電腦設定**或**使用者設定**) > **原則** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="831cb-158">To configure a mandatory policy, open the Group Policy Editor and go to (**Computer Configuration** or **User Configuration**) > **Policies** > **Administrative Templates** > **Microsoft Edge**.</span></span>
- <span data-ttu-id="831cb-159">若要設定建議原則，請開啟群組原則編輯器並移至 (**電腦設定**或**使用者設定**) > **原則** > **系統管理範本** > **Microsoft Edge – 預設設定 (使用者可以覆寫)**。</span><span class="sxs-lookup"><span data-stu-id="831cb-159">To configure a recommended policy, open the Group Policy Editor and go to (**Computer Configuration** or **User Configuration**) > **Policies** > **Administrative Templates** > **Microsoft Edge – Default Settings (users can override)**.</span></span>

  ![開啟群組原則編輯器](./media/configure-microsoft-edge/edge-ad-policy.png)

### <a name="3-test-your-policies"></a><span data-ttu-id="831cb-161">3. 測試您的原則</span><span class="sxs-lookup"><span data-stu-id="831cb-161">3. Test your policies</span></span>

<span data-ttu-id="831cb-162">在目標用戶端裝置上，開啟 Microsoft Edge 並瀏覽至 **edge://policy** 以查看套用的所有原則。</span><span class="sxs-lookup"><span data-stu-id="831cb-162">On a target client device, open Microsoft Edge and navigate to **edge://policy** to see all policies that are applied.</span></span> <span data-ttu-id="831cb-163">如果是在本機電腦上套用原則設定，原則應會立即顯示。</span><span class="sxs-lookup"><span data-stu-id="831cb-163">If you applied policy settings on the local computer, policies should appear immediately.</span></span> <span data-ttu-id="831cb-164">如果在進行原則設定時 Microsoft Edge 是開啟的，則可能需要關閉並重新開啟 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="831cb-164">You may need to close and reopen Microsoft Edge if it was open while you were configuring policy settings.</span></span>

![在瀏覽器中檢視設定的原則](./media/configure-microsoft-edge/edge-gpEdit.png)

<span data-ttu-id="831cb-166">對於 Active Directory 群組原則設定，原則設定會依照網域管理員定義的定期間隔傳播到網域電腦，目標電腦可能不會馬上收到原則更新。</span><span class="sxs-lookup"><span data-stu-id="831cb-166">For Active Directory group policy settings, policy settings are propagated to domain computers at a regular interval defined by your domain administrator, and target computers may not receive policy updates right away.</span></span> <span data-ttu-id="831cb-167">若要手動重新整理目標電腦上的 Active Directory 群組原則設定，請從目標電腦的命令提示字元或 PowerShell 工作階段執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="831cb-167">To manually refresh Active Directory group policy settings on a target computer, execute the following command from a command prompt or PowerShell session on the target computer:</span></span>

``` powershell
gpupdate /force
```

<span data-ttu-id="831cb-168">您可能需要關閉並重新開啟 Microsoft Edge，新原則才會出現。</span><span class="sxs-lookup"><span data-stu-id="831cb-168">You may need to close and reopen Microsoft Edge before the new policies appear.</span></span>

<span data-ttu-id="831cb-169">您還可以在目標電腦上使用 REGEDIT.exe 來檢視儲存群組原則設定的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="831cb-169">You can also use REGEDIT.exe on a target computer to view the registry settings that store group policy settings.</span></span> <span data-ttu-id="831cb-170">這些設定位於登錄路徑 **HKLM\SOFTWARE\Policies\Microsoft\Edge**。</span><span class="sxs-lookup"><span data-stu-id="831cb-170">These settings are located at the registry path **HKLM\SOFTWARE\Policies\Microsoft\Edge**.</span></span>

## <a name="see-also"></a><span data-ttu-id="831cb-171">請參閱</span><span class="sxs-lookup"><span data-stu-id="831cb-171">See also</span></span>

- [<span data-ttu-id="831cb-172">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="831cb-172">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="831cb-173">使用 Intune 進行 Windows 的設定</span><span class="sxs-lookup"><span data-stu-id="831cb-173">Configure for Windows with Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="831cb-174">進行 macOS 的設定</span><span class="sxs-lookup"><span data-stu-id="831cb-174">Configure for macOS</span></span>](configure-microsoft-edge-on-mac.md)
- [<span data-ttu-id="831cb-175">瀏覽 Microsoft Edge 企業原則</span><span class="sxs-lookup"><span data-stu-id="831cb-175">Browse Microsoft Edge Enterprise Policies</span></span>](microsoft-edge-policies.md)


