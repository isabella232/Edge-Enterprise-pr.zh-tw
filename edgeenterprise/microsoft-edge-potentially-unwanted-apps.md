---
title: 使用 Microsoft Edge 封鎖可能不需要的應用程式
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 03/04/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 Microsoft Edge 封鎖可能不需要的應用程式
ms.openlocfilehash: 4e9d513c4d1144d4109064d7aa42e4ef31a59b88
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448027"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a><span data-ttu-id="30311-103">封鎖可能不需要的應用程式 (PUA)</span><span class="sxs-lookup"><span data-stu-id="30311-103">Protect against potentially unwanted applications (PUAs)</span></span>

<span data-ttu-id="30311-104">本文說明如何使用 Microsoft Edge 或使用 Windows Defender 防毒程式封鎖可能不需要的應用程式 (PUA)。</span><span class="sxs-lookup"><span data-stu-id="30311-104">This article explains how you can protect against potentially unwanted applications (PUAs) using Microsoft Edge or by using Windows Defender Antivirus.</span></span>

> [!NOTE]
> <span data-ttu-id="30311-105">本文適用於 Microsoft Edge 版本 80 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="30311-105">This article applies to Microsoft Edge version 80 or later.</span></span>

## <a name="overview"></a><span data-ttu-id="30311-106">概觀</span><span class="sxs-lookup"><span data-stu-id="30311-106">Overview</span></span>

<span data-ttu-id="30311-107">可能不需要的應用程式不會被視為是病毒或惡意程式碼，但這些應用程式可能會對端點執行不利影響端點效能或使用的動作。</span><span class="sxs-lookup"><span data-stu-id="30311-107">Potentially unwanted applications aren't considered to be viruses or malware, but these apps might perform actions on endpoints that adversely affect endpoint performance or use.</span></span> <span data-ttu-id="30311-108">例如，*規避軟體*會主動嘗試規避安全性產品的偵測。</span><span class="sxs-lookup"><span data-stu-id="30311-108">For example, *Evasion software* actively tries to evade detection by security products.</span></span> <span data-ttu-id="30311-109">這種軟體會增加網路受到實際惡意程式碼感染的風險。</span><span class="sxs-lookup"><span data-stu-id="30311-109">This kind of software can increase the risk of your network being infected with actual malware.</span></span> <span data-ttu-id="30311-110">PUA 也包括聲譽不佳的應用程式。</span><span class="sxs-lookup"><span data-stu-id="30311-110">PUA can also refer to applications that are considered to have poor reputation.</span></span>

<span data-ttu-id="30311-111">如需將軟體分類為 PUA 的準則說明，請參閱[可能不需要的應用程式](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua)。</span><span class="sxs-lookup"><span data-stu-id="30311-111">For a description of the criteria used to classify software as a PUA, see [Potentially unwanted application](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua).</span></span>

## <a name="protect-against-pua-with-microsoft-edge"></a><span data-ttu-id="30311-112">使用 Microsoft Edge 封鎖 PUA</span><span class="sxs-lookup"><span data-stu-id="30311-112">Protect against PUA with Microsoft Edge</span></span>

<span data-ttu-id="30311-113">Microsoft Edge (版本 80.0.361.50 或更新版本) 會封鎖 PUA 下載和相關的資源 URL。</span><span class="sxs-lookup"><span data-stu-id="30311-113">Microsoft Edge (version 80.0.361.50 or later) blocks PUA downloads and associated resource URLs.</span></span>

<span data-ttu-id="30311-114">您可以在 Microsoft Edge 中啟用 **封鎖可能不需要的應用程式**功能來設定保護。</span><span class="sxs-lookup"><span data-stu-id="30311-114">You can set up protection by enabling the **Block potentially unwanted apps** feature in Microsoft Edge.</span></span>

> [!NOTE]
> <span data-ttu-id="30311-115">[Microsoft Edge 團隊部落格文章](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/)會描述這項新功能，並解釋如何處理標籤錯誤的應用程式或如何將應用程式報告為不需要的應用程式。</span><span class="sxs-lookup"><span data-stu-id="30311-115">The [Microsoft Edge Team blog post](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/) describes this new feature and explains how to handle a mislabeled app or report an app as unwanted.</span></span>

### <a name="to-enable-pua-protection"></a><span data-ttu-id="30311-116">若要啟用 PUA 保護：</span><span class="sxs-lookup"><span data-stu-id="30311-116">To enable PUA protection:</span></span>

1. <span data-ttu-id="30311-117">在瀏覽器中開啟 [設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="30311-117">Open **Settings** in the browser.</span></span>
2. <span data-ttu-id="30311-118">選取 [隱私權與服務]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="30311-118">Select **Privacy and services**.</span></span>
3. <span data-ttu-id="30311-119">在 [服務]\*\*\*\* 區段中，查看 [Microsoft Defender SmartScreen] \*\*\*\* 是否已開啟。</span><span class="sxs-lookup"><span data-stu-id="30311-119">In the **Services** section, check to see that **Microsoft Defender SmartScreen** is turned on.</span></span> <span data-ttu-id="30311-120">若未開啟，請開啟 Microsoft Defender SmartScreen。</span><span class="sxs-lookup"><span data-stu-id="30311-120">If not, then turn on Microsoft Defender SmartScreen.</span></span> <span data-ttu-id="30311-121">下列螢幕擷取畫面中的範例顯示瀏覽器是由組織管理，且已開啟 Microsoft Defender SmartScreen。</span><span class="sxs-lookup"><span data-stu-id="30311-121">The example in the following screenshot shows the browser is managed by the organization and that Microsoft Defender SmartScreen is turned on.</span></span>

   ![在 [設定] 中開啟 Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. <span data-ttu-id="30311-123">在 [服務]\*\*\*\* 區段中，使用前面的螢幕擷取畫面中所示的切換開關開啟 [封鎖可能不需要的應用程式]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="30311-123">In the **Services** section, use the toggle shown in the preceding screenshot to turn on **Block potentially unwanted apps**.</span></span>

   > [!TIP]
   > <span data-ttu-id="30311-124">您可以在我們的 Windows Defender SmartScreen [示範頁面](https://demo.smartscreen.msft.net/)中進行測試，以放心地探索 PUA 防護的 URL 封鎖功能。</span><span class="sxs-lookup"><span data-stu-id="30311-124">You can safely explore the URL-blocking feature of PUA protection by testing it out on one of our Windows Defender SmartScreen [demo pages](https://demo.smartscreen.msft.net/).</span></span>

<span data-ttu-id="30311-125">當 Microsoft Edge 偵測到 PUA 時，您會看到類似下一個螢幕擷取畫面所示的訊息。</span><span class="sxs-lookup"><span data-stu-id="30311-125">When Microsoft Edge detects a PUA, you will see a message like the one in the next screenshot.</span></span>

   ![Microsoft Edge PUA 警告訊息](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a><span data-ttu-id="30311-127">若要封鎖與 PUA 相關的 URL</span><span class="sxs-lookup"><span data-stu-id="30311-127">To block against PUA-associated URLs</span></span>

<span data-ttu-id="30311-128">開啟 Microsoft Edge 中的 PUA 保護之後，Windows Defender SmartScreen 將會封鎖與 PUA 相關的 URL。</span><span class="sxs-lookup"><span data-stu-id="30311-128">After you turn on PUA protection in Microsoft Edge, Windows Defender SmartScreen will protect you from PUA-associated URLs.</span></span>

<span data-ttu-id="30311-129">系統管理員可以透過多種方式來設定 Microsoft Edge 和 Windows Defender SmartScreen 如何共同作業，以避免使用者收到與 PUA 相關的 URL。</span><span class="sxs-lookup"><span data-stu-id="30311-129">There are several ways admins can configure how Microsoft Edge and Windows Defender SmartScreen work together to protect users from PUA-associated URLs.</span></span> <span data-ttu-id="30311-130">如需詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="30311-130">For more information, see:</span></span>

- [<span data-ttu-id="30311-131">在 Windows 上設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="30311-131">Configure Microsoft Edge policy settings on Windows</span></span>](./configure-microsoft-edge.md)
- [<span data-ttu-id="30311-132">SmartScreen 設定</span><span class="sxs-lookup"><span data-stu-id="30311-132">SmartScreen settings</span></span>](./microsoft-edge-policies.md#smartscreen-settings)
- [<span data-ttu-id="30311-133">SmartScreenPuaEnabled 原則</span><span class="sxs-lookup"><span data-stu-id="30311-133">SmartScreenPuaEnabled policy</span></span>](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [<span data-ttu-id="30311-134">設定 Windows Defender SmartScreen</span><span class="sxs-lookup"><span data-stu-id="30311-134">Configure Windows Defender SmartScreen</span></span>](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

<span data-ttu-id="30311-135">系統管理員也可以自訂 Microsoft Defender 進階威脅防護 (Microsoft Defender ATP) 封鎖清單。</span><span class="sxs-lookup"><span data-stu-id="30311-135">Admins can also customize the Microsoft Defender Advanced Threat Protection (Microsoft Defender ATP) block list.</span></span> <span data-ttu-id="30311-136">他們可以使用 Microsoft Defender ATP 入口網站來[建立及管理 IP 和 URL 指示器](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview)。</span><span class="sxs-lookup"><span data-stu-id="30311-136">They can use the Microsoft Defender ATP portal to [create and manage indicators for IPs and URLs](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview).</span></span>

## <a name="protect-against-pua-with-windows-defender-antivirus"></a><span data-ttu-id="30311-137">使用 Windows Defender 防毒軟體封鎖 PUA</span><span class="sxs-lookup"><span data-stu-id="30311-137">Protect against PUA with Windows Defender Antivirus</span></span>

<span data-ttu-id="30311-138">[偵測並封鎖可能不需要的應用程式](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus)文章也說明如何設定 Windows Defender 防毒軟體以啟用 PUA 保護。</span><span class="sxs-lookup"><span data-stu-id="30311-138">The [Detect and block potentially unwanted applications](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus) article also describes how you can configure Windows Defender Antivirus to enable PUA protection.</span></span> <span data-ttu-id="30311-139">您可以使用下列任一選項設定保護：</span><span class="sxs-lookup"><span data-stu-id="30311-139">You can configure protection using any of the following options:</span></span>

- [<span data-ttu-id="30311-140">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="30311-140">Microsoft Intune</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [<span data-ttu-id="30311-141">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="30311-141">Microsoft Endpoint Configuration Manager</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [<span data-ttu-id="30311-142">群組原則</span><span class="sxs-lookup"><span data-stu-id="30311-142">Group Policy</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [<span data-ttu-id="30311-143">PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30311-143">PowerShell cmdlets</span></span>](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

<span data-ttu-id="30311-144">當 Windows Defender 在端點上偵測到 PUA 檔案時，它會隔離該檔案，並以和一般威脅偵測相同的格式 (以 "PUA:" 開頭) 通知使用者 ([除非停用通知](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus))。偵測到的威脅也會顯示在 [Windows 安全性應用程式的隔離清單中](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history)。</span><span class="sxs-lookup"><span data-stu-id="30311-144">When Windows Defender detects a PUA file on an endpoint it quarantines the file and notifies the user ([unless notifications are disabled](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus)) in the same format as a normal threat detection (prefaced with "PUA:".) Detected threats also appear in the [quarantine list in the Windows Security app](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history).</span></span>

### <a name="pua-notifications-and-events"></a><span data-ttu-id="30311-145">PUA 通知與事件</span><span class="sxs-lookup"><span data-stu-id="30311-145">PUA notifications and events</span></span>

<span data-ttu-id="30311-146">系統管理員可以透過多種方式查看 PUA 事件：</span><span class="sxs-lookup"><span data-stu-id="30311-146">There are several ways an admin can see PUA events:</span></span>

- <span data-ttu-id="30311-147">透過 Windows 事件檢視器，但不是透過 Microsoft Endpoint Configuration Manager 或 Intune。</span><span class="sxs-lookup"><span data-stu-id="30311-147">In the Windows Event Viewer, but not in Microsoft Endpoint Configuration Manager or Intune.</span></span>
- <span data-ttu-id="30311-148">如果 PUA 偵測的電子郵件通知已開啟，則可透過電子郵件。</span><span class="sxs-lookup"><span data-stu-id="30311-148">In an email if email notifications for PUA detections is turned on.</span></span>
- <span data-ttu-id="30311-149">透過 [Windows Defender 防毒軟體](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus)事件記錄，其中 PUA 事件會記錄在事件 ID 1116 下，訊息如下：「惡意程式碼平台偵測到惡意程式碼或其他可能不需要的軟體」。</span><span class="sxs-lookup"><span data-stu-id="30311-149">In [Windows Defender Antivirus](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus) event logs, where a PUA event is recorded under event ID 1116 with the message: "The antimalware platform detected malware or other potentially unwanted software."</span></span>

> [!NOTE]
> <span data-ttu-id="30311-150">使用者將會看到「Microsoft Defender SmartScreen 已經將 \*.exe 封鎖為可能不需要的應用程式」。</span><span class="sxs-lookup"><span data-stu-id="30311-150">Users will see "\*.exe has been blocked as a potentially unwanted app by Microsoft Defender SmartScreen".</span></span>

### <a name="allow-list-an-app"></a><span data-ttu-id="30311-151">應用程式的允許清單</span><span class="sxs-lookup"><span data-stu-id="30311-151">Allow-list an app</span></span>

<span data-ttu-id="30311-152">就像 Microsoft Edge 一樣，Windows Defender 防毒軟體提供了一種方法，允許錯誤封鎖的檔案或允許完成任務所需的檔案。</span><span class="sxs-lookup"><span data-stu-id="30311-152">Like Microsoft Edge, Windows Defender Antivirus provides a way to allow files that are blocked by mistake or needed to complete a task.</span></span> <span data-ttu-id="30311-153">如果發生這種情況，您可以設定檔案允許清單。</span><span class="sxs-lookup"><span data-stu-id="30311-153">If this happens you can allow-list a file.</span></span> <span data-ttu-id="30311-154">如需詳細資訊，請參閱[如何設定 Configuration Manager 中的 Endpoint Protection](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders)，了解如何排除特定檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="30311-154">For more information, see [How to Configure Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders) to learn how to exclude specific files or folders.</span></span>

## <a name="see-also"></a><span data-ttu-id="30311-155">請參閱</span><span class="sxs-lookup"><span data-stu-id="30311-155">See also</span></span>

- [<span data-ttu-id="30311-156">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="30311-156">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="30311-157">威脅防護</span><span class="sxs-lookup"><span data-stu-id="30311-157">Threat protection</span></span>](/windows/security/threat-protection/index)
- [<span data-ttu-id="30311-158">設定行為型、啟發學習和即時保護</span><span class="sxs-lookup"><span data-stu-id="30311-158">Configure behavioral, heuristic, and real-time protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [<span data-ttu-id="30311-159">新一代保護</span><span class="sxs-lookup"><span data-stu-id="30311-159">Next-generation protection</span></span>](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [<span data-ttu-id="30311-160">Chromium 版 Microsoft Edge (版本 79) 的安全性基準</span><span class="sxs-lookup"><span data-stu-id="30311-160">Security baseline for Chromium-based Microsoft Edge, version 79</span></span>](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)