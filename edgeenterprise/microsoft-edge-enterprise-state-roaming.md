---
title: Microsoft Edge 和企業狀態漫遊
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 和企業狀態漫遊
ms.openlocfilehash: 34ee5bf7970834a2e2211db9e2c0bc6ae99bcd6b
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11979436"
---
# <a name="microsoft-edge-and-enterprise-state-roaming"></a>Microsoft Edge 和企業狀態漫遊

本文介紹 Microsoft Edge 參與企業狀態漫遊 (ESR) 方案的情況正在發生變化，以便更好地支援跨平台和裝置同步。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="introduction"></a>簡介

使用 Windows 10，[Azure Active Directory (Azure AD)](/azure/active-directory/fundamentals/active-directory-whatis) 使用者能夠安全地將其使用者設定和應用程式設定資料同步處理至雲端。 [企業狀態漫遊 (ESR)](/azure/active-directory/devices/enterprise-state-roaming-overview) 提供使用者跨 Windows 裝置的一致體驗，並且減少設定新的裝置所需的時間。

Microsoft Edge 採用 Chromium 平台，其同步解決方案現已與 Windows 同步架構斷開連接。 這會影響 Microsoft Edge 與 ESR 方案之間的關係。

> [!IMPORTANT]
> 新的 Microsoft Edge 不參與 ESR 方案。

## <a name="whats-changing-with-microsoft-edge"></a>Microsoft Edge 有什麼變化？

使用新的 Microsoft Edge，同步解決方案不會繫結到 Windows 同步生態系統。 這使我們能夠跨所有平台 (如 Windows 7、Windows 8.1、iOS、Android 和 macOS) 提供 Microsoft Edge。 這也使我們能夠為 Windows 上的非主要帳戶提供同步。 此外，我們可以以比 Windows 更頻繁、更靈活的發行步調散發 Microsoft Edge。 (如需詳細資訊，請參閱[支援下一版 Microsoft Edge 的 Windows Update](microsoft-edge-sysupdate-windows-updates.md)。 所有這些因素都突顯，需要重新評估 Microsoft Edge 參與 ESR 方案。

ESR 被界定為 Windows 產品，承諾如何處理來自 Windows 裝置的資料，但 Microsoft Edge 同步將超出 Windows 裝置的範圍。 而且，由於資料在這些裝置之間漫遊，因此很難在 ESR 脈絡中定義 Microsoft Edge 同步方案。 為了簡化同步的工作方式和管理方式，並適應突顯的更改，我們決定從 ESR 方案中撤出 Microsoft Edge。

## <a name="does-this-mean-enterprises-will-lose-the-abilities-they-had-as-part-of-esr"></a>這是否意味著企業將失去作為 ESR 一部分的能力？

不。 Microsoft Edge 將繼續支援 ESR 提供的大部分功能。

### <a name="unified-experience-across-devices-and-new-device-configuration-time"></a>跨裝置的一致體驗和新裝置的設定時間

當使用者使用 Azure Active Directory (Azure AD 帳戶) 登入到其 Windows 裝置時，Microsoft Edge 將在初次啟動新瀏覽器時隱式繼承該身分識別。

使用者明確同意在新 Microsoft Edge 中啟用同步後，瀏覽器將同步所有瀏覽器資料，如我的最愛、密碼和歷程記錄。 這可確保跨裝置獲得一致的體驗，並縮短個人化瀏覽器所需的時間。

### <a name="separation-of-corporate-and-consumer-data"></a>分隔公司和消費者資料

組織可以控制他們的資料，消費者雲端帳戶中不會混合公司資料，企業雲端帳戶中也不會混合消費者資料。

### <a name="enhanced-security"></a>增強式安全性

資料會在離開使用者的 Windows 10 裝置之前自動加密，方法是使用 Azure 資訊保護，資料在雲端中待用時會保持加密。 所有內容在雲端中待用時會保持加密，除了命名空間，例如設定名稱。

### <a name="monitoring"></a>監視

我們將透過 Azure AD 入口網站整合，對於誰能同步處理組織中的設定以及在哪些裝置上提供更多的控制權和可見性。 此功能將在未來版本中啟用。

### <a name="management"></a>管理

管理員將能夠控制組織中哪些成員可以啟用同步。請參閱[設定 Microsoft Edge 同步](microsoft-edge-enterprise-sync.md#configure-microsoft-edge-sync)和[同步群組原則](microsoft-edge-enterprise-sync.md#sync-group-policies)。 此外，使用者可以為其每個裝置開啟/關閉同步，以及單獨切換每個資料屬性以進行同步。

### <a name="key-management"></a>金鑰管理

同步功能利用 Azure 資訊保護 (AIP) 僅保護使用者和企業管理員的同步資料。 AIP 支援 Microsoft 託管 (預設) 和自攜金鑰以進行雲端金鑰管理。 您的組織使用的雲端金鑰管理策略對 Microsoft Edge 是透明的，並且對同步功能沒有影響。

> [!IMPORTANT]
> 不支援[持有您自己的金鑰 (HYOK)](/azure/information-protection/configure-adrms-restrictions) 和 Active Directory Rights Management Services。

## <a name="summary-of-sync-attributes"></a>同步屬性摘要

以下資料屬性將在初次同步時在新版本的 Microsoft Edge 中同步：

- 我的最愛
- 密碼
- 表單填滿
- 歷程記錄
- 開啟索引標籤 (工作階段)
- 設定 (喜好設定)
- 延伸模組

前面的屬性清單與可在 Microsoft Edge 舊版中同步的屬性不同。 (有關 Microsoft Edge 舊版設定的詳細資訊，請參閱 [Windows 10 漫遊設定](/azure/active-directory/devices/enterprise-state-roaming-windows-settings-reference)。) 使用者可以使用 Microsoft Edge 設定，選擇啟用/停用這些屬性。 鑒於兩個版本 (例如歷史記錄) 之間的屬性差異，可能會要求使用者再次同意同步。

> [!NOTE]
> 與 Microsoft Edge 舊版不同，新 Microsoft Edge 不使用 Windows 認證管理員儲存密碼，因此不會將密碼與 Internet Explorer 或其他使用 Windows 認證管理員的應用程式同步。

## <a name="terms-of-service"></a>服務條款

Microsoft Edge 同步的服務條款屬於Microsoft 軟體授權，可在 Microsoft Edge 中輸入 *edge://terms* 查看。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 同步](microsoft-edge-enterprise-sync.md)