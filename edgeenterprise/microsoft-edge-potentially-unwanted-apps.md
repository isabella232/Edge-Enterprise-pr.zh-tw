---
title: 使用 Microsoft Edge 封鎖可能不需要的應用程式
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Microsoft Edge 封鎖可能不需要的應用程式
ms.openlocfilehash: 68cd87e85408933212c4b25baa01a9ff8d994089
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979513"
---
# <a name="protect-against-potentially-unwanted-applications-puas"></a>封鎖可能不需要的應用程式 (PUA)

本文說明如何使用 Microsoft Edge 或使用 Windows Defender 防毒程式封鎖可能不需要的應用程式 (PUA)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 80 或更新版本。

## <a name="overview"></a>概觀

可能不需要的應用程式不會被視為是病毒或惡意程式碼，但這些應用程式可能會對端點執行不利影響端點效能或使用的動作。 例如，*規避軟體*會主動嘗試規避安全性產品的偵測。 這種軟體會增加網路受到實際惡意程式碼感染的風險。 PUA 也包括聲譽不佳的應用程式。

如需將軟體分類為 PUA 的準則說明，請參閱[可能不需要的應用程式](/windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua)。

## <a name="protect-against-pua-with-microsoft-edge"></a>使用 Microsoft Edge 封鎖 PUA

Microsoft Edge (版本 80.0.361.50 或更新版本) 會封鎖 PUA 下載和相關的資源 URL。

您可以在 Microsoft Edge 中啟用 **封鎖可能不需要的應用程式**功能來設定保護。

> [!NOTE]
> [Microsoft Edge 團隊部落格文章](https://blogs.windows.com/msedgedev/2020/02/27/protecting-users-potentially-unwanted-apps/)會描述這項新功能，並解釋如何處理標籤錯誤的應用程式或如何將應用程式報告為不需要的應用程式。

### <a name="to-enable-pua-protection"></a>若要啟用 PUA 保護：

1. 在瀏覽器中開啟 [設定]****。
2. 選取 [隱私權與服務]****。
3. 在 [服務]**** 區段中，查看 [Microsoft Defender SmartScreen] **** 是否已開啟。 若未開啟，請開啟 Microsoft Defender SmartScreen。 下列螢幕擷取畫面中的範例顯示瀏覽器是由組織管理，且已開啟 Microsoft Defender SmartScreen。

   ![在 [設定] 中開啟 Microsoft Edge PUA](./media/microsoft-edge-potentially-unwanted-apps/security-pua-setup.png)

4. 在 [服務]**** 區段中，使用前面的螢幕擷取畫面中所示的切換開關開啟 [封鎖可能不需要的應用程式]****。

   > [!TIP]
   > 您可以在我們的 Windows Defender SmartScreen [示範頁面](https://demo.smartscreen.msft.net/)中進行測試，以放心地探索 PUA 防護的 URL 封鎖功能。

當 Microsoft Edge 偵測到 PUA 時，您會看到類似下一個螢幕擷取畫面所示的訊息。

   ![Microsoft Edge PUA 警告訊息](./media/microsoft-edge-potentially-unwanted-apps/security-pua-msg.png)

### <a name="to-block-against-pua-associated-urls"></a>若要封鎖與 PUA 相關的 URL

開啟 Microsoft Edge 中的 PUA 保護之後，Windows Defender SmartScreen 將會封鎖與 PUA 相關的 URL。

系統管理員可以透過多種方式來設定 Microsoft Edge 和 Windows Defender SmartScreen 如何共同作業，以避免使用者收到與 PUA 相關的 URL。 如需詳細資訊，請參閱：

- [在 Windows 上設定 Microsoft Edge 原則設定](./configure-microsoft-edge.md)
- [SmartScreen 設定](./microsoft-edge-policies.md#smartscreen-settings)
- [SmartScreenPuaEnabled 原則](./microsoft-edge-policies.md#smartscreenpuaenabled)
- [設定 Windows Defender SmartScreen](/microsoft-edge/deploy/available-policies?source=docs#configure-windows-defender-smartscreen)

系統管理員也可以自訂 Microsoft Defender 進階威脅防護 (Microsoft Defender ATP) 封鎖清單。 他們可以使用 Microsoft Defender ATP 入口網站來[建立及管理 IP 和 URL 指示器](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators#create-indicators-for-ips-and-urlsdomains-preview)。

## <a name="protect-against-pua-with-windows-defender-antivirus"></a>使用 Windows Defender 防毒軟體封鎖 PUA

[偵測並封鎖可能不需要的應用程式](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#windows-defender-antivirus)文章也說明如何設定 Windows Defender 防毒軟體以啟用 PUA 保護。 您可以使用下列任一選項設定保護：

- [Microsoft Intune](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-intune-to-configure-pua-protection)
- [Microsoft Endpoint Configuration Manager](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-configuration-manager-to-configure-pua-protection)
- [群組原則](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-group-policy-to-configure-pua-protection)
- [PowerShell Cmdlet](/windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus#use-powershell-cmdlets-to-configure-pua-protection)

當 Windows Defender 在端點上偵測到 PUA 檔案時，它會隔離該檔案，並以和一般威脅偵測相同的格式 (以 "PUA:" 開頭) 通知使用者 ([除非停用通知](/windows/security/threat-protection/windows-defender-antivirus/configure-notifications-windows-defender-antivirus))。偵測到的威脅也會顯示在 [Windows 安全性應用程式的隔離清單中](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-security-center-antivirus#detection-history)。

### <a name="pua-notifications-and-events"></a>PUA 通知與事件

系統管理員可以透過多種方式查看 PUA 事件：

- 透過 Windows 事件檢視器，但不是透過 Microsoft Endpoint Configuration Manager 或 Intune。
- 如果 PUA 偵測的電子郵件通知已開啟，則可透過電子郵件。
- 透過 [Windows Defender 防毒軟體](/windows/security/threat-protection/windows-defender-antivirus/troubleshoot-windows-defender-antivirus)事件記錄，其中 PUA 事件會記錄在事件 ID 1116 下，訊息如下：「惡意程式碼平台偵測到惡意程式碼或其他可能不需要的軟體」。

> [!NOTE]
> 使用者將會看到「Microsoft Defender SmartScreen 已經將 *.exe 封鎖為可能不需要的應用程式」。

### <a name="allow-list-an-app"></a>應用程式的允許清單

就像 Microsoft Edge 一樣，Windows Defender 防毒軟體提供了一種方法，允許錯誤封鎖的檔案或允許完成任務所需的檔案。 如果發生這種情況，您可以設定檔案允許清單。 如需詳細資訊，請參閱[如何設定 Configuration Manager 中的 Endpoint Protection](/previous-versions/system-center/system-center-2012-R2/hh508770(v=technet.10)#to-exclude-specific-files-or-folders)，了解如何排除特定檔案或資料夾。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [威脅防護](/windows/security/threat-protection/index)
- [設定行為型、啟發學習和即時保護](/windows/security/threat-protection/windows-defender-antivirus/configure-protection-features-windows-defender-antivirus)
- [新一代保護](/windows/security/threat-protection/windows-defender-antivirus/windows-defender-antivirus-in-windows-10)
- [Chromium 版 Microsoft Edge (版本 79) 的安全性基準](https://techcommunity.microsoft.com/t5/microsoft-security-baselines/security-baseline-final-for-chromium-based-microsoft-edge/ba-p/1111863)