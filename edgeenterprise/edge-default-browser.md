---
title: 將 Microsoft Edge 設定為 Windows 和 macOS 中的預設瀏覽器
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 了解如何將 Microsoft Edge 設定為預設瀏覽器
ms.openlocfilehash: 191d7835a0c4aacfc2fde409c57622ff5a351926
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978943"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a>將 Microsoft Edge 設定為預設瀏覽器

本文說明如何將 Microsoft Edge 設定為 Windows 和 macOS 中的預設瀏覽器。

> [!NOTE]
> 本文適用於 Windows 8 和 Windows 10 上的 Microsoft Edge 版本 77 或更新版本。 有關 Windows 7 和 macOS，請參閱[將 Microsoft Edge設定為預設瀏覽器](./microsoft-edge-policies.md#defaultbrowsersettingenabled)原則。

## <a name="introduction"></a>簡介

您可以使用**設定預設關聯設定檔案**群組原則或 [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 行動裝置管理設定，來將 Microsoft Edge 設定為您組織的預設瀏覽器。

若要將 Microsoft Edge Stable 設定為 html 檔案、http/https 連結和 PDF 檔案的預設瀏覽器，請使用以下應用程式關聯檔案範例：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> 若要將 Microsoft Edge Beta 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Beta"，並將 **ProgId** 設定為 "MSEdgeBHTML"。 若要將 Microsoft Edge Dev 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Dev"，並將 **ProgId** 設定為 "MSEdgeDHTML"。


> [!NOTE]
> 如果未在目標裝置上安裝 Microsoft Edge，則不會套用預設檔案關聯。 在這種情況下，系統會在使用者開啟連結或 htm/html 檔案時，提示他們選取預設應用程式。

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a>在加入網域的裝置上將 Microsoft Edge 設定為預設瀏覽器

您可以透過設定**設定預設關聯設定檔案**群組原則，在加入網域的裝置上將 Microsoft Edge 設定為預設瀏覽器。 開啟這個群組原則，會要求您建立並儲存預設關聯設定檔案。 此檔案儲存在本機或網路共用上。 如需有關建立這個檔案的詳細資訊，請參閱[匯出或匯入預設應用程式關聯](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)。

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a>若要為預設檔案類型和通訊協定關聯設定檔案設定群組原則：

1. 開啟群組原則編輯器，然後移至**電腦設定\系統管理範本\Windows 元件\檔案總管**。
2. 選取**設定預設關聯設定檔案**。
3. 按一下**原則設定**，然後按一下**啟用**。
4. 在**選項**下輸入您預設關聯設定檔案的位置。
5. 按一下**確定**以儲存原則設定。

下一個螢幕擷取畫面中的範例顯示了網路共用上名為 *appassoc.xml* 的關聯檔案，該檔案可從目標裝置存取。

   ![在群組原則中啟用檔案關聯](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > 如果啟用了此設定，並且使用者的裝置已加入網域，則在使用者下次登入時將會處理關聯設定檔案。

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a>在加入 Azure Active Directory 的裝置上將 Microsoft Edge 設定為預設瀏覽器

若要在加入 Azure Active Directory 的裝置上將 Microsoft Edge 設定為預設瀏覽器，請使用以下應用程式關聯檔案範例並依照 [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 行動裝置管理設定中的步驟進行。

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> 若要將 Microsoft Edge Beta 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Beta"，並將 **ProgId** 設定為 "MSEdgeBHTML"。 若要將 Microsoft Edge Dev 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Dev"，並將 **ProgId** 設定為 "MSEdgeDHTML"。

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a>將 Microsoft Edge 設定為 macOS 中的預設瀏覽器

嘗試以程式設計方式設定 macOS 的預設瀏覽器會導致向終端使用者顯示提示。 此提示是 macOS 安全性功能，只有使用 AppleScript，才能使離開提示的動作自動化。

由於此限制，將 Microsoft Edge 設定為 macOS 的預設瀏覽器，有兩個主要方法可供選用。 第一個選項是使用已將 Microsoft Edge 設定為預設瀏覽器的 macOS 映像來刷新裝置。 另一個選項是使用 [將 Microsoft Edge 設定為預設瀏覽器](./microsoft-edge-policies.md#defaultbrowsersettingenabled) 原則，此原則會提示使用者將 Microsoft Edge 設定為預設瀏覽器。

使用上述任一方法時，使用者仍然可以變更預設瀏覽器。 這是因為基於安全理由，不可透過程式設計方式封鎖預設瀏覽器喜好設定。 因此，建議您部署**將 Microsoft Edge 設定為預設瀏覽器** 原則，即使您建立有 Microsoft Edge 做為預設瀏覽器的映像，也應如此。 如果設定了此原則，而使用者下次開啟 Microsoft Edge 時，將預設瀏覽器變更為其他瀏覽器，則系統會提示他們將 Microsoft Edge 設為預設。

## <a name="see-also"></a>也請參閱

- [規劃 Microsoft Edge 部署](./deploy-edge-plan-deployment.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [將 Microsoft Edge 設定為預設瀏覽器 (Windows 7 和 macOS)](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [Windows 10 – 如何為 IT 專業人員設定檔案關聯？](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [匯出或匯入預設應用程式關聯](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [DISM 概觀](/windows-hardware/manufacture/desktop/what-is-dism)
  - [DISM - 部署映像服務與管理](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)