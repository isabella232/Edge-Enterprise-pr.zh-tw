---
title: 使用 .plist 設定適用於 macOS 的 Microsoft Edge
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 .plist 在 macOS 上設定 Microsoft Edge 原則設定
ms.openlocfilehash: d2e604e13f0fb7f81b2fb492073eba0751407771
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978840"
---
# <a name="configure-microsoft-edge-policy-settings-for-macos-using-a-plist"></a>使用 .plist 針對 macOS 設定 Microsoft Edge 原則設定

本文介紹如何使用屬性清單 (.plist) 檔案，在 macOS 上設定 Microsoft Edge。 您將了解如何建立此檔案，然後將它部署到 Microsoft Intune。

如需詳細資訊，請參閱[關於資訊屬性清單檔案](https://developer.apple.com/library/archive/documentation/General/Reference/InfoPlistKeyReference/Articles/AboutInformationPropertyListFiles.html) (Apple 網站) 和[自訂承載資料設定](https://support.apple.com/guide/mdm/custom-mdm9abbdbe7/1/web/1)。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="configure-microsoft-edge-policies-on-macos"></a>在 macOS 上設定 Microsoft Edge 原則

第一個步驟是建立 plist。 您可以使用任何文字編輯器來建立 plist 檔，也可以使用[終端機建立組態設定檔](#create-a-configuration-profile-using-terminal)。 不過，使用可為您設定 XML 程式碼格式的工具建立和編輯 plist 檔案會更輕鬆。 *Xcode* 是一套免費的整合式開發環境，您可以從以下位置之一取得：

- [Apple 開發人員網站](https://developer.apple.com/xcode/)
- [Mac App Store](https://apps.apple.com/app/xcode/id497799835?mt=12)

如需支援的原則及其喜好設定金鑰名稱的清單，請參閱 [Microsoft Edge 瀏覽器原則參考](microsoft-edge-policies.md)。 在原則範本檔案 (可從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載) 中，**範例**資料夾中有一個範例 plist (*itadminexample.plist*)。 範例檔案包含所有支援的資料類型，您可以自訂這些資料類型以定義原則設定。 

建立 plist 內容後的下一步，是使用 Microsoft Edge 喜好設定網域 *com.microsoft.Edge* 來命名它。 此名稱區分大小寫，不應包括您設為目標的通道，因為它適用於所有 Microsoft Edge 通道。 Plist 檔案名必須為 **_com.microsoft.Edge.plist_**。

> [!IMPORTANT]
> 從組建 78.0.249.2 開始，macOS 上的所有 Microsoft Edge 通道都從 **com.microsoft.Edge** 喜好設定網域讀取。 所有舊版都從通道專屬網域讀取，例如 **com.microsoft.Edge.Dev** 適用於 Dev 通道。

最後一步是使用您偏好的 MDM 提供者 (如 Microsoft Intune) 將 plist 部署到使用者的 Mac 裝置。 如需相關指示，請參閱[部署 plist](#deploy-your-plist)。

### <a name="create-a-configuration-profile-using-terminal"></a>使用終端機建立組態設定檔

1. 在終端機中，使用以下命令，以您的偏好設定在桌面建立一個適用於 Microsoft Edge 的 plist：

   ```cmd
   /usr/bin/defaults write ~/Desktop/com.microsoft.Edge.plist RestoreOnStartup -int 1
   ```

2. 將 plist 從二進位格式轉換為純文字格式：

   ```cmd
   /usr/bin/plutil -convert xml1 ~/Desktop/com.microsoft.Edge.plist
   ```

轉換檔案後，請驗證原則資料是否正確，並包含組態設定檔所需的設定。

> [!NOTE]
> 只有鍵值對應位於 plist 或 xml 檔的內容中。 在將檔案上傳到 Intune 之前，請從檔案中移除所有 \<plist> 和 \<dict> 值以及 xml 標頭。 檔案應僅包含鍵值對。

## <a name="deploy-your-plist"></a>部署 plist

對於 Microsoft Intune，建立以 macOS 平台為目標的新裝置組態設定檔，然後選取*喜好設定檔案*設定檔案類型。 將 **com.microsoft.Edge** 設為目標以做為喜好設定網域名稱，並上傳您的 plist。 如需詳細資訊，請參閱[使用 Microsoft Intune 將屬性清單檔案新增至 macOS 裝置](/intune/configuration/preference-file-settings-macos)。

對於 Jamf，將 .plist 檔案上載為*自訂設定*承載。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [使用 Jamf 針對 macOS 設定](configure-microsoft-edge-on-mac-jamf.md)
- [進行 Windows 的設定](configure-microsoft-edge.md)
- [使用 Intune 進行 Windows 的設定](configure-edge-with-intune.md)