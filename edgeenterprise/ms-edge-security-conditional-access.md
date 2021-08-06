---
title: Microsoft Edge 和條件式存取
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 和條件式存取
ms.openlocfilehash: bee6aa73e078037adf28af05755bd0a74b30a65b5122eeca16fb7f6c2af1ae4a
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726708"
---
# <a name="microsoft-edge-and-conditional-access"></a>Microsoft Edge 和條件式存取
  
本文將說明 Microsoft Edge 如何支援條件式存取，並說明如何存取由條件存取保護的資源。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

提到管理雲端資源時，雲端安全的一個關鍵面向是身分識別和存取權。 在行動優先、雲端優先的世界中，使用者可以從任何位置使用各種裝置和應用程式存取組織的資源。 因此，僅關注何人可以存取資源是不夠的。 您還需要考慮存取資源的方式。 Azure Active Directory (Azure AD) 條件式存取可協助您掌握安全性和生產力之間的平衡。

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a>在 Microsoft Edge 中存取受條件式存取保護的資源

Microsoft Edge 原生支援 Azure AD 條件式存取。 無需另外安裝擴充功能。 當您使用企業 Azure AD 認證登入 Microsoft Edge 設定檔時，Microsoft Edge 允許無縫存取受條件式存取保護的企業雲端資源。

在相容裝置上，存取資源的身分識別應與設定檔上的身分識別相符。  否則，您會看到一則類似於下一個螢幕擷取畫面中顯示的訊息。 在螢幕擷取畫面範例中，"testadmin@evostsoneboxtest.com" 是存取資源所需的登入帳戶。

![瀏覽器中的條件式存取訊息](./media/edge-security/microsoft-edge-security-conditional-access.png)

若要繼續，您必須切換到所需的設定檔 (如果有) 或建立具有相符身分識別的設定檔。

若要登入並使用您的設定檔，請按一下瀏覽器右上角的帳戶圖片。 您可以使用下拉式功能表來︰

- 選取其他設定檔。 按一下設定檔名稱。
- 建立設定檔。 按一下**新增設定檔**。
- 管理您的設定檔。 按一下**管理設定檔設定**。

此支援適用於所有平台，包括所有受支援的 Windows 和 macOS 版本。

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a>如何在 Azure Active Directory 中部署條件式存取

[部署條件式存取](/azure/active-directory/conditional-access/plan-conditional-access)提供可協助在 Azure Active Directory 中部署條件式存取的詳細指南。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：安全性、相容性及管理性](/microsoft-edge-video-security-compatibility-manageability.md)