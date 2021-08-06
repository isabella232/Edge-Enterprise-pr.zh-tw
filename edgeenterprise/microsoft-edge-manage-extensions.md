---
title: 管理企業中的 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 管理企業中的 Microsoft Edge 擴充功能
ms.openlocfilehash: 69c10bfa1e041d48f99594e6ac85dd39ba66379ca8d6d7fe12f1bdef6f3b54fe
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11724908"
---
# <a name="manage-microsoft-edge-extensions-in-the-enterprise"></a>管理企業中的 Microsoft Edge 擴充功能

本文針對在組織中管理 Microsoft Edge 擴充功能的系統管理員，提供最佳作法指導方針。 您可以使用本文中的資訊來開發管理貴組織中擴充功能的策略。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="introduction"></a>簡介

組織想要保護公司與使用者資料，並評估瀏覽器擴充功能，以確保它們安全且與企業相關。 系統管理員想要：

- 防止安裝錯誤的應用程式和擴充功能。
- 保留使用者完成工作所需的擴充功能。
- 管理使用者和公司資料的存取權。  

本文是協助系統管理員管理擴充功能系列的第一篇文章，可為使用者提供安全且有生產力的體驗。 本系列將逐步介紹不同的選項，並協助您挑選管理擴充功能的最佳方法。 本系列包含下列文章：

- [管理企業中的 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions.md)。 建立管理擴充功能的策略，並設定管理瀏覽器所需的系統管理範本。
- [使用群組原則來管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)。 使用群組原則管理擴充功能的選項。
- [建立 Web Store 以託管 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-webstore.md)。 建立和託管擴充功能。
- [適用於 Microsoft Edge 擴充功能的常見問題集](microsoft-edge-manage-extensions-faq.md)。 常見問題集。

## <a name="things-to-consider-when-managing-extensions"></a>管理擴充功能時要考慮的事

您的使用者需要存取特定應用程式、網站和擴充功能，以執行其工作，同時保護使用者和公司資料。 有效的安全性策略需要向企業提出正確的問題，以及擴充功能如何配合貴公司的需求。 需要詢問的一些關鍵問題包括：

- 我必須遵守哪些法規和合規性措施？
- 某些擴充功能是否要求過於廣泛的權限，這可能會違反我公司的資料安全性原則？
- 我的使用者裝置上儲存的使用者或公司資料有多少？

當您回答這些問題時，您可以使用 Microsoft Edge 提供的細微策略：

- 根據資料保護原則封鎖或允許使用者電腦上的擴充功能。
- 在使用者的裝置上強制安裝擴充功能，讓使用者擁有所需的生產力工具。
- 允許清單或封鎖清單的擴充功能，以允許使用者執行其工作所需的最小權限。

管理擴充功能的傳統模型會針對特定擴充功能使用允許清單和封鎖清單方法。 不過，Microsoft Edge 也讓您管理擴充功能要求的權限。 使用此模型，您可以決定要允許擴充功能在電腦和裝置上使用哪些權限，然後根據您的需求來實作允許或封鎖擴充的全域原則。  

## <a name="understand-extension-permissions"></a>了解擴充功能權限

擴充功能需要權限才能在裝置或網頁上進行變更，以正確執行。 這些存取權限稱為權限。 開發人員必須列出需要哪些權限並存取其擴充功能。 權限有兩個主要類別，而許多擴充功能需要下列兩種權限：

- 託管權限需要擴充功能列出它可檢視或修改的網頁。
- 裝置權限是擴充功能在其執行的裝置上所需的權限。

這些權限的一些範例包括：存取 USB 連接埠、儲存空間或檢視畫面，以及與原生程式通訊。  

## <a name="get-ready-to-manage-extensions"></a>準備就緒管理擴充功能

## <a name="before-you-begin"></a>開始之前

擴充功能選項假設您已為使用者管理 Microsoft Edge。 有關設定適用於 Microsoft Edge 原則的系統管理範本，請參閱：

-   [在 Windows 上設定 Microsoft Edge 原則設定](/DeployEdge/configure-microsoft-edge)
-   [使用 Intune 進行 Windows 的設定](/mem/intune/configuration/administrative-templates-configure-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
-   [使用行動裝置管理，進行 Windows 的設定](/deployedge/configure-edge-with-mdm)
-   [使用 .plist 設定 macOS](/deployedge/configure-microsoft-edge-on-mac)
-   [使用 Jamf 進行 macOS 的設定](/deployedge/configure-microsoft-edge-on-mac-jamf)

本文內容的設定步驟適用於 Windows，關於 MAC/Linux 中的對應實作，請參閱 Microsoft Edge 瀏覽器原則參考。

## <a name="decide-which-extensions-to-allow"></a>決定允許哪些擴充功能

大多數組織都應該根據權限以及有權存取的網站來管理擴充功能。 這個方法更安全、更容易管理，而且對大型組織是可調整的。  

- 封鎖/允許權限 – 可讓您根據擴充功能所需的權限來控制擴充功能。
- 執行階段封鎖主機 – 可讓您控制這些擴充功能可以存取的網站。

使用這個方法可節省時間，因為您只需要設定一次。 而使用執行階段主機原則時，您最重要的網站會受到保護。還有其他選項，例如：

-   強制安裝擴充功能 – 讓您以無訊息方式安裝擴充功能。
-   允許清單/封鎖清單 (視需要) - 決定允許安裝哪些擴充功能。

使用下列步驟做為指南，決定貴組織決定允許哪些擴充功能。

1. 建立員工電腦上所需的擴充功能清單。 在測試環境中測試擴充功能，以診斷內部應用程式的任何相容性問題。
2. 選擇需要更安全的網站。

   - 了解您需要封鎖哪些敏感性的內部網站或網域，以禁止擴充功能變更或讀取資料。  
   - 當擴展程式執行時，封鎖 API 呼叫，以防止存取這些網站。 這包括封鎖 Web 要求、讀取 Cookie、JavaScript 注入、XHR 等等。

3. 決定執行這些擴充功能所需的權限。 找出哪些權限會對使用者造成潛在風險。

   - 稽核使用者已安裝的擴充功能，並查看他們所需的權限。 您可以在擴充功能的程式碼中查看 Web App 資訊清單 JSON 檔案。 請執行下列步驟，查看擴充功能需要哪些權限：

     - 從 [Microsoft Edge 外掛程式](https://microsoftedge.microsoft.com/addons/)網站或 [Chrome 線上應用程式商店](https://chrome.google.com/webstore) 安裝擴充功能。
     - 測試擴充功能，並了解擴充功能在貴組織中運作方式。
     - 瀏覽至 *edge://extensions*，以檢閱擴充功能所需的權限。 例如，以下螢幕擷取畫面中顯示的 Microsoft Office 擴充功能會要求「讀取您的瀏覽歷程記錄」和「顯示通知」的權限。 將此擴充功能的實用性與要求的權限等級進行權衡。 核准貴組織的擴充功能後，請使用下列工具進行管理。
   :::image type="content" source="media/microsoft-edge-manage-extensions/manage-extesions-office-extension.png" alt-text="具有權限的 Microsoft Office 擴充功能。":::

   - 您也可以在貴組織中核准擴充功能之前，先驗證使用者要求的擴充功能。 擴充功能使用的一些權限可能模糊不清。 針對商務關鍵型應用程式，您可以直接與應用程式開發人員或廠商連絡，以取得擴充功能詳細資訊或查看原始程式碼。 他們應該能夠詳述擴充功能可在裝置和網站上進行的變更。
   - 檢閱宣告權限清單，該清單列出擴充功能可使用的所有權限。 從這份清單中，您可以決定要在貴組織中允許哪些權限。

4. 從您收集的資料建立主清單。此清單會包含下列資訊：

   - **必要的擴充功能**。 這份清單可以按照部門、辦公室位置或其他相關資訊來組織。
   - **擴充功能允許清單**。 具有可能封鎖但允許執行之權限的必要擴充功能。 使用者需要這些擴充功能，或透過與廠商的交談確定不會帶來風險。
   - **擴充功能封鎖清單**。 被封鎖安裝的擴充功能。 此清單中的擴充功能具有不允許執行的權限。 也包含要保持安全且不允許擴充功能存取的核心網站和網域。 之後，您可以將此封鎖清單與已有的其他清單進行比較。 您可能會發現您可以輕鬆設定目前的封鎖清單原則。

5. 向專案關係人及 IT 小組展示您的清單以取得支持。
6. 在實驗室測試新原則或在貴組織中進行小型試驗。
7. 分階段向員工推出這些新原則。 如需詳細資訊，請參閱[使用群組原則來管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)。
8. 檢閱使用者的意見反應。
9. 每月、每季或每年重複並微調程式。

在強制執行允許權限的比較基準並保護敏感性公司網站後，您可以為企業提供更多安全性，同時為使用者提供更好的體驗。 員工可能會安裝他們之前無法安裝的擴充功能，但無法在敏感性的商務網站上執行這些擴充功能。  

## <a name="see-also"></a>另請參閱

- [使用群組原則管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)
- [建立 Web Store 以託管 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-webstore.md)
- [ExtensionSettings 原則的參考指南](microsoft-edge-manage-extensions-ref-guide.md)
- [Microsoft Edge 擴充功能常見問題集](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)