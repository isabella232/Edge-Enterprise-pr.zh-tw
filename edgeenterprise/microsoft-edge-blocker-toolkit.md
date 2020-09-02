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
# <span data-ttu-id="4b68f-103">封鎖程式工具組用來停用自動傳遞 Microsoft Edge (以 Chromium 為基礎)</span><span class="sxs-lookup"><span data-stu-id="4b68f-103">Blocker Toolkit to disable automatic delivery of Microsoft Edge (Chromium-based)</span></span>

<span data-ttu-id="4b68f-104">本文介紹了用於停用自動傳遞和安裝 Microsoft Edge 的封鎖程式工具組。</span><span class="sxs-lookup"><span data-stu-id="4b68f-104">This article describes the Blocker Toolkit for disabling automatic delivery and installation of Microsoft Edge.</span></span> <span data-ttu-id="4b68f-105">此篇文章已於 **2020/01/09 進行更新**，並加入更多可能要求您使用封鎖程式工具組的其他資訊：於**2020/2/28** 更新內容中，將裝置準則中的 "MDM managed" 移除以便將此裝置排除在自動更新的範圍中，以及在 **2020/6/30** 更新內容中，反映出與 Windows Update 連結的所有裝置都含括在此更新內容的接收範疇之中（最快可以可於 2020/7/30 生效）。</span><span class="sxs-lookup"><span data-stu-id="4b68f-105">This article was updated on **01/09/2020** with more information about devices that might require you to use the Blocker Toolkit, on **2/28/2020** to remove "MDM managed" from the criteria of devices to be excluded from this automatic update, and on **6/30/2020** to reflect that all Windows Update connected devices are in scope to receive this update (effective no sooner than 7/30/2020).</span></span>

> [!NOTE]
> <span data-ttu-id="4b68f-106">本文適用於 Microsoft Edge 穩定通道。</span><span class="sxs-lookup"><span data-stu-id="4b68f-106">This applies to Microsoft Edge Stable channel.</span></span>

## <span data-ttu-id="4b68f-107">概觀</span><span class="sxs-lookup"><span data-stu-id="4b68f-107">Overview</span></span>

<span data-ttu-id="4b68f-108">為了協助我們的客戶成為更安全且更時時維持著最新狀態，Microsoft 將會發佈 Microsoft Edge （以 Chromium 為基礎）到執行 Windows 10 版本1803 及更新版本的所有 Windows Update 連接裝置。</span><span class="sxs-lookup"><span data-stu-id="4b68f-108">To help our customers become more secure and up-to-date, Microsoft will distribute Microsoft Edge (Chromium-based) to all Windows Update-connected devices running Windows 10 version 1803 and newer.</span></span> <span data-ttu-id="4b68f-109">此過程將在 2020 年 1 月 15 日之後開始，到那時將會有更多資訊提供參考。</span><span class="sxs-lookup"><span data-stu-id="4b68f-109">This process will start after January 15, 2020 and more information will be available on that date.</span></span>

<span data-ttu-id="4b68f-110">封鎖程式工具組適用於想要封鎖自動傳遞 Microsoft Edge 到執行 Windows 10 版本 1803 和更新版本的 Windows 更新連接裝置的組織。</span><span class="sxs-lookup"><span data-stu-id="4b68f-110">The Blocker Toolkit is intended for organizations that would like to block automatic delivery of Microsoft Edge (Chromium-based) to Windows Updated-connected devices running Windows 10 version 1803 and newer.</span></span>
<span data-ttu-id="4b68f-111">透過 Windows Server Update Services (WSUS) 或 [商務用 Windows Update (WUfB)] 管理的裝置將不會含括在此自動更新的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="4b68f-111">Devices that are Windows Server Update Services (WSUS) or Windows Update for Business (WUfB) managed will be excluded from this automatic update.</span></span>

**<span data-ttu-id="4b68f-112">請務必注意：</span><span class="sxs-lookup"><span data-stu-id="4b68f-112">It's important to note that:</span></span>**

- <span data-ttu-id="4b68f-113">封鎖程式工具組不會阻止使用者從網際網路下載或外部媒體手動安裝 Microsoft Edge (以 Chromium 為基礎)。</span><span class="sxs-lookup"><span data-stu-id="4b68f-113">The Blocker Toolkit will not prevent users from manually installing Microsoft Edge (Chromium-based) from Internet download, or from external media.</span></span>
- <span data-ttu-id="4b68f-114">透過商務用 Windows Update (WUfB) 管理更新的組織不會自動收到此更新，也不需要部署封鎖程式工具組。</span><span class="sxs-lookup"><span data-stu-id="4b68f-114">Organizations with updates managed through Windows Update for Business (WUfB) will not automatically receive this update and do not need to deploy the blocker toolkit.</span></span>
- <span data-ttu-id="4b68f-115">組織在使用更新管理解決方案 (如 Windows Server Update Services (WSUS) 或 System Center Configuration Manager (SCCM)) 管理的環境中，不需要部署封鎖程式工具組。</span><span class="sxs-lookup"><span data-stu-id="4b68f-115">Organizations with environments managed with an update management solution such as Windows Server Update Services (WSUS) or System Center Configuration Manager (SCCM) do not have to deploy the Blocker Toolkit.</span></span> <span data-ttu-id="4b68f-116">這些組織可以使用這些產品在其環境中全面管理透過 Windows Update 和 Microsoft Update 發佈的更新的部署，包括 Microsoft Edge (以 Chromium 為基礎)。</span><span class="sxs-lookup"><span data-stu-id="4b68f-116">They can use those products to fully manage deployment of updates released through Windows Update and Microsoft Update, including Microsoft Edge (Chromium-based), within their environment.</span></span>
- <span data-ttu-id="4b68f-117">此更新是獨立更新 (不是每月累積更新的一部分)，可為企業客戶提供靈活性和對部署此更新的最大控制。</span><span class="sxs-lookup"><span data-stu-id="4b68f-117">This update is a stand-alone update (not part of the monthly cumulative update) to give Enterprise customers flexibility and maximum control over deploying this update.</span></span>
- <span data-ttu-id="4b68f-118">新版 Microsoft Edge（以 Chromium 為基礎）將含括在 Windows 10 在 2020 年第二季功能更新的版本 20H2 之中。</span><span class="sxs-lookup"><span data-stu-id="4b68f-118">The new Microsoft Edge (Chromium-based) will be included as part of the Windows 10, version 20H2 feature update in the second half of 2020.</span></span> <span data-ttu-id="4b68f-119">封鎖程式工具組不會對 20H2 版本的行為或佈署造成影響。</span><span class="sxs-lookup"><span data-stu-id="4b68f-119">The Blocker toolkit does not impact 20H2 behaviors or deployment.</span></span> <span data-ttu-id="4b68f-120">如需有關 Windows 10 版本 20H2 的詳細資訊，請參閱[此處](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/)。</span><span class="sxs-lookup"><span data-stu-id="4b68f-120">See more information about Windows 10, version 20H2 [here](https://blogs.windows.com/windowsexperience/2020/06/16/whats-next-for-windows-10-updates/).</span></span>

<span data-ttu-id="4b68f-121">可以從 [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe) 下載封鎖程式工具組可執行檔。</span><span class="sxs-lookup"><span data-stu-id="4b68f-121">You can download the Blocker Toolkit executable file from [https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe](https://msedgeblockertoolkit.blob.core.windows.net/blockertoolkit/MicrosoftEdgeChromiumBlockerToolkit.exe).</span></span>

### <span data-ttu-id="4b68f-122">工具組元件</span><span class="sxs-lookup"><span data-stu-id="4b68f-122">Toolkit components</span></span>

<span data-ttu-id="4b68f-123">此工具組包括下列元件：</span><span class="sxs-lookup"><span data-stu-id="4b68f-123">This toolkit contains the following components:</span></span>

- <span data-ttu-id="4b68f-124">可執行封鎖程式指令碼 (.CMD)</span><span class="sxs-lookup"><span data-stu-id="4b68f-124">Executable blocker script (.CMD)</span></span>
- <span data-ttu-id="4b68f-125">群組原則系統管理範本 (.ADMX 和 .ADML)</span><span class="sxs-lookup"><span data-stu-id="4b68f-125">Group Policy Administrative Template (.ADMX and .ADML)</span></span>

### <span data-ttu-id="4b68f-126">支援的作業系統</span><span class="sxs-lookup"><span data-stu-id="4b68f-126">Supported Operating Systems</span></span>

<span data-ttu-id="4b68f-127">Windows 10 版本 1803 及更新版本。</span><span class="sxs-lookup"><span data-stu-id="4b68f-127">Windows 10 version 1803 and newer.</span></span>

## <span data-ttu-id="4b68f-128">封鎖程式指令碼</span><span class="sxs-lookup"><span data-stu-id="4b68f-128">Blocker script</span></span>

<span data-ttu-id="4b68f-129">該指令碼建立一個登錄機碼，並將關聯的值設定為封鎖或解除封鎖 (取決於使用的命令列選項) 自動在本機電腦或遠端目的電腦上 Microsoft Edge (以 Chromium 為基礎) 的傳遞。</span><span class="sxs-lookup"><span data-stu-id="4b68f-129">The script creates a registry key and sets the associated value to block or unblock (depending on the command-line option used) automatic delivery of Microsoft Edge (Chromium-based) on either the local machine or a remote target machine.</span></span>

**<span data-ttu-id="4b68f-130">登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="4b68f-130">Registry key:</span></span>** `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate`<br>
**<span data-ttu-id="4b68f-131">機碼值名稱：</span><span class="sxs-lookup"><span data-stu-id="4b68f-131">Key value name:</span></span>** `DoNotUpdateToEdgeWithChromium`

| <span data-ttu-id="4b68f-132">值</span><span class="sxs-lookup"><span data-stu-id="4b68f-132">Value</span></span>                | <span data-ttu-id="4b68f-133">結果</span><span class="sxs-lookup"><span data-stu-id="4b68f-133">Result</span></span>                         |
|----------------------|--------------------------------|
| *<span data-ttu-id="4b68f-134">機碼未定義</span><span class="sxs-lookup"><span data-stu-id="4b68f-134">Key is not defined</span></span>* | <span data-ttu-id="4b68f-135">*不會*封鎖散發。</span><span class="sxs-lookup"><span data-stu-id="4b68f-135">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4b68f-136">0</span><span class="sxs-lookup"><span data-stu-id="4b68f-136">0</span></span>                    | <span data-ttu-id="4b68f-137">*不會*封鎖散發。</span><span class="sxs-lookup"><span data-stu-id="4b68f-137">Distribution is *not* blocked.</span></span> |
| <span data-ttu-id="4b68f-138">1</span><span class="sxs-lookup"><span data-stu-id="4b68f-138">1</span></span>                    | <span data-ttu-id="4b68f-139">會封鎖散發。</span><span class="sxs-lookup"><span data-stu-id="4b68f-139">Distribution is blocked.</span></span>       |

<span data-ttu-id="4b68f-140">指令碼有下列命令列語法：</span><span class="sxs-lookup"><span data-stu-id="4b68f-140">The script has the following command-line syntax:</span></span><br>
`EdgeChromium_Blocker.cmd [<machine name>] [/B] [/U] [/H]`

### <span data-ttu-id="4b68f-141">電腦名稱</span><span class="sxs-lookup"><span data-stu-id="4b68f-141">Machine name</span></span>

<span data-ttu-id="4b68f-142">`<machine name>` 參數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="4b68f-142">The `<machine name>` parameter is optional.</span></span> <span data-ttu-id="4b68f-143">如果未指定，則在本機電腦上執行該動作。</span><span class="sxs-lookup"><span data-stu-id="4b68f-143">If not specified, the action is performed on the local machine.</span></span> <span data-ttu-id="4b68f-144">否則，透過 `REG` 命令的遠端登錄功能存取遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="4b68f-144">Otherwise, the remote machine is accessed through the remote registry capabilities of the `REG` command.</span></span> <span data-ttu-id="4b68f-145">如果由於安全性權限而無法存取遠端登錄，或者找不到遠端電腦，則會從 `REG` 命令傳回錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4b68f-145">If the remote registry can't be accessed due to security permissions or the remote machine can't be found, an error message is returned from the `REG` command.</span></span>

### <span data-ttu-id="4b68f-146">切換</span><span class="sxs-lookup"><span data-stu-id="4b68f-146">Switches</span></span>

<span data-ttu-id="4b68f-147">指令碼使用的切換是互斥的，並且只對給定命令中的第一個有效切換執行操作。</span><span class="sxs-lookup"><span data-stu-id="4b68f-147">Switches used by the script are mutually exclusive and only the first valid switch from a given command is acted on.</span></span> <span data-ttu-id="4b68f-148">指令碼可以在同一台電腦上執行多次。</span><span class="sxs-lookup"><span data-stu-id="4b68f-148">The script can be run multiple times on the same machine.</span></span>

| <span data-ttu-id="4b68f-149">切換</span><span class="sxs-lookup"><span data-stu-id="4b68f-149">Switch</span></span>       | <span data-ttu-id="4b68f-150">描述</span><span class="sxs-lookup"><span data-stu-id="4b68f-150">Description</span></span>                              |
|--------------|------------------------------------------|
| `/B`         | <span data-ttu-id="4b68f-151">會封鎖散發</span><span class="sxs-lookup"><span data-stu-id="4b68f-151">Blocks distribution</span></span>                      |
| `/U`         | <span data-ttu-id="4b68f-152">會解除封鎖散發</span><span class="sxs-lookup"><span data-stu-id="4b68f-152">Unblocks distribution</span></span>                    |
| `/H` <span data-ttu-id="4b68f-153">或</span><span class="sxs-lookup"><span data-stu-id="4b68f-153">or</span></span> `/?` | <span data-ttu-id="4b68f-154">顯示以下摘要說明：</span><span class="sxs-lookup"><span data-stu-id="4b68f-154">Displays the following summary help:</span></span><br>`This tool can be used to remotely block or unblock the delivery of Microsoft Edge (Chromium-based) through Automatic Updates.`<br> `Usage:`<br>`EdgeChromium_Blocker.cmd [<machine name>] [/B][/U][/H]`<br>`B = Block Microsoft Edge (Chromium-based) deployment`<br>`U = Allow Microsoft Edge (Chromium-based) deployment`<br>`H = Help`<br>`Examples:`<br>`EdgeChromium_Blocker.cmd mymachine /B (blocks delivery on machine "mymachine")`<br>`EdgeChromium_Blocker.cmd /U (unblocks delivery on the local machine)`<br> |

## <span data-ttu-id="4b68f-155">群組原則系統管理範本 (.ADMX 和 .ADML 檔案)</span><span class="sxs-lookup"><span data-stu-id="4b68f-155">Group Policy Administrative Template (.ADMX and .ADML files)</span></span>

<span data-ttu-id="4b68f-156">群組原則系統管理範本 (.ADMX 和 .ADML 檔案) 允許系統管理員匯入新的群組原則設定，以封鎖或解除封鎖將 Microsoft Edge (以 Chromium 為基礎) 自動傳遞到其群組原則環境，並使用群組原則在其環境中的系統中集中執行動作。</span><span class="sxs-lookup"><span data-stu-id="4b68f-156">The Group Policy Administrative Template (.ADMX  and .ADML files) allows administrators to import the new Group Policy settings to block or unblock automatic delivery of Microsoft Edge (Chromium-based) into their Group Policy environment, and use Group Policy to centrally execute the action across systems in their environment.</span></span>

<span data-ttu-id="4b68f-157">執行 Windows 10 RS3 企業版/教育版以及 RS4 和更高版本的使用者將在以下路徑下看到原則：</span><span class="sxs-lookup"><span data-stu-id="4b68f-157">Users running Windows 10 RS3 Enterprise/EDU and RS4 and newer, will see the policy under the following path:</span></span>

```
/Computer Configuration  
  /Administrative Templates
    /Classic Administrative Templates
      /Windows Components
        /Windows Update  
          /Microsoft Edge (Chromium-based) Blockers  
```

<span data-ttu-id="4b68f-158">此設定僅做為電腦設定可用；沒有每個使用者設定。</span><span class="sxs-lookup"><span data-stu-id="4b68f-158">This setting is available only as a Computer setting; there is no Per-User setting.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b68f-159">此登錄設定不儲存在原則機碼中，並被視為*喜好設定*。</span><span class="sxs-lookup"><span data-stu-id="4b68f-159">This registry setting isn't stored in a policies key and is considered a *preference*.</span></span> <span data-ttu-id="4b68f-160">因此，如果已刪除實作該設定的群組原則物件，或者原則設定為**未設定**，則該設定將保留。</span><span class="sxs-lookup"><span data-stu-id="4b68f-160">Therefore, if the Group Policy Object that implements the setting is ever removed or the policy is set to **Not Configured**, the setting will remain.</span></span> <span data-ttu-id="4b68f-161">若要使用群組原則解除封鎖 Microsoft Edge (以 Chromium 為基礎) 的散發，將原則設定為**禁用**。</span><span class="sxs-lookup"><span data-stu-id="4b68f-161">To unblock distribution of Microsoft Edge (Chromium-based) by using Group Policy, set the policy to **Disabled**.</span></span>

## <span data-ttu-id="4b68f-162">請參閱</span><span class="sxs-lookup"><span data-stu-id="4b68f-162">See also</span></span>

- [<span data-ttu-id="4b68f-163">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="4b68f-163">Microsoft Edge Enterprise landing page</span></span>](https://www.microsoftedgeinsider.com/enterprise)
- [<span data-ttu-id="4b68f-164">支援 Microsoft Edge 的 Windows 更新</span><span class="sxs-lookup"><span data-stu-id="4b68f-164">Windows updates to support Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-windows-updates)
- [<span data-ttu-id="4b68f-165">如何存取舊版 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4b68f-165">How to access the old version of Microsoft Edge</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-sysupdate-access-old-edge)
