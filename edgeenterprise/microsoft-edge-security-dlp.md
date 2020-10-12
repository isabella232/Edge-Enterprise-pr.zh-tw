---
title: Microsoft Edge 中的資料外洩防護
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 10/08/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 中的資料外洩防護 (DLP)
ms.openlocfilehash: 59c1b68c0526a49a2ee30283893707852514828d
ms.sourcegitcommit: 2af303fc97e8493024e2359fa2e8be162ab95a59
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104604"
---
# Microsoft Edge 中的資料外洩防護 (DLP)

資料外洩防護 (DLP) 是一種技術系統，可識別並保護敏感性企業資料不遭到未經授權的披露。 若要遵守商務標準和行業法規，組織必須保護敏感性資訊，並防止未經授權的披露。 敏感性資訊包括財務資料或個人身分識別資訊 (PII)，例如信用卡號碼、社會安全號碼或健康記錄等諸多其他項目。

遠端工作已提升對 DLP 使用的著重度。 隨著在裝置上逐漸增多的個人及工作活動之使用，企業可能面臨在工作場所以外未經授權共用公司資料的風險。

這種使用者活動混合也已分散到多個裝置，在這種情況下，資料會隨著各種公用網路和私人網路之使用，在個人和公司裝置間移動。 最終結果會增加披露敏感性資料的風險。

Microsoft Edge 本身支援兩種不同的 DLP 解決方案： Microsoft Endpoint DLP 和 Windows 資訊保護 (WIP)。

## Microsoft Endpoint DLP

Microsoft Endpoint DLP 是使用現代化概念 (例如以資料為中心的防護) 的新一代 DLP。 它內建於 Windows 10 和 Microsoft Edge，因此不需要在裝置上安裝其他代理程式或外掛程式。 若要深入瞭解 Endpoint DLP，請參閱 [瞭解 Microsoft 365 Endpoint 資料外洩防護](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 85 或更新版本。

Microsoft Edge 強制執行系統管理員設定的敏感性檔案和記錄非合規活動的稽核事件之原則。

在執行 Windows 10 的裝置上，您可以在執行稽核和管理的使用者活動包括下列活動：

- 檔案上傳：防止將敏感性檔案上傳到未經授權的雲端位置。 接下來的3個螢幕擷取畫面會顯示使用者嘗試將敏感性資料檔案放到其本機儲存區的順序。
- 剪貼簿保護：防止敏感性資料從檔案中移除。
- 列印保護：防止敏感性檔案被列印。
- 儲存至 USB/網路：防止將敏感性檔案儲存至可移動 USB 儲存區或未經授權的網路位置。

如需有關您可以稽核和管理之使用者活動的詳細資訊，請參閱 [您可以監視並採取行動的 Endpoint 活動](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on)。

## Windows 資訊保護

請參閱 [Windows 資訊保護的 支援](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection)，其中描述 Microsoft Edge 如何支援 Windows 資訊保護 (WIP)。 您可以在下列各節中深入瞭解系統需求、優點和支援功能：

- [系統需求](https://docs.microsoft.com/deployedge/:microsoft-edge-security-windows-information-protection#system-requirements)
- [Windows 資訊保護的優點](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [Microsoft Edge 支援的 WIP 功能](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## 請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：資料外洩防護 - Microsoft Edge](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [資料外洩防護概觀](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide)
- [使用 Windows 資訊保護來保護您的企業資料](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
