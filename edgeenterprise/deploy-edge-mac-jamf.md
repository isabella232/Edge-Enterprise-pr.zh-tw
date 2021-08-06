---
title: 使用 Jamf 自動執行適用於 macOS 的 Microsoft Edge 部署
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 如何使用 Jamf 自動執行適用於 macOS 的 Microsoft Edge 部署。
ms.openlocfilehash: ab860bf90aa2472dd3a0437dfc98261421c8b5467d8e2f5cb28d511f5b7b0d51
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11726260"
---
# <a name="deploy-to-macos-with-jamf"></a>使用 Jamf 部署到 macOS

本文介紹如何使用 Jamf 部署適用於 macOS 的 Microsoft Edge。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="prerequisites"></a>必要條件

開始部署 Microsoft Edge 之前，請確定符合下列必要條件：

- Microsoft Edge 安裝檔案 **MicrosoftEdgeDev-\<version\>.pkg** 位於網路上的可存取位置。 您可從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 企業安裝檔案。
- 您有 Jamf Cloud 帳戶，該帳戶具有建立安裝檔案並將其部署到電腦所需的存取和權限等級。

## <a name="to-deploy-microsoft-edge-using-jamf"></a>若要使用 Jamf 部署 Microsoft Edge：

1. 登入到 Jamf 並移至**所有設定。**

    ![開啟所有設定](./media/mac-deploy/jamf-dash-main-open-settings.png)

2. 在**所有設定**下，按一下**電腦管理**。

    ![選取電腦管理](./media/mac-deploy/jamf-all-settings-computer-mgmt.png)

3. 在**電腦管理**下，按一下**套件**。

    ![選取套件](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkgs.png)

4. 在**套件**頁面上，按一下 **+ 新增**以新增新套件。

    ![選取新增以新增套件](./media/mac-deploy/jamf-all-settings-computer-mgmt-new-pkg.png)

5. 在**新增套件**頁面上，輸入有關套件的詳細資訊，然後按一下**儲存**。 (例如，「顯示名稱」、「資訊」或「備註」。)

    ![選取儲存以儲存套件資訊](./media/mac-deploy/jamf-all-settings-computer-mgmt-save-pkg-info.png)

6. 選取功能表列上的**電腦**，然後在瀏覽器列中選取**原則**。

7. 選取 **+ 新增**以顯示**新增原則**窗格。

    ![選取新增以建立新原則](./media/mac-deploy/jamf-all-settings-computer-new-policy.png)

8. 在**選項**索引標籤上，選取**一般**。

    - 在**顯示名稱**下，輸入原則的顯示名稱。
    - 在**觸發**下，選取將觸發原則的事件。 (在上述範例中，事件為 [啟動]。)

    ![輸入部署資訊](./media/mac-deploy/jamf-all-settings-computer-cfg-policy.png)

9. 在**選項**索引標籤上，按一下**套件**。

10. 在**設定套件**快顯視窗上，按一下**設定**。

    ![設定套件](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-configure.png)

11. 您新增的套件顯示在**套件**窗格中。 按一下**新增**。 對於此範例，套件是以下螢幕擷取畫面中的 "MicrosoftEdgeBeta"。

    ![新增套件](./media/mac-deploy/jamf-all-settings-computer-policy-pkg-add-beta.png)

12. 在**新增原則**頁面上，使用下拉式清單選取原則要執行的**發佈點**和**動作**。 按一下**儲存**。 以下螢幕擷取畫面使用 [每台電腦的預設發佈點] 和 [安裝] 作為範例。

    ![選取發佈點和動作](./media/mac-deploy/jamf-all-settings-computer-mgmt-pkg-cfg-distro.png)

13. 在**新增原則**頁面上，選取**範圍**索引標籤。您可以根據電腦或使用者來管理部署範圍。 在此範例中，從**目標電腦**下拉式清單中選取**所有電腦**，然後按一下**儲存**。

    ![選取部署範圍](./media/mac-deploy/jamf-all-settings-computer-mgmt-add-target.png)

14. 此時，您可以查看 Microsoft Edge 部署原則。 如果部署選項符合您的要求，請按一下**完成**。

    ![按一下完成](./media/mac-deploy/jamf-all-settings-computer-mgmt-finish-add-deployment.png)

    > [!NOTE]
    > 您可以隨時返回部署原則以變更設定。

恭喜！ 您剛剛完成設定 Jamf 以部署適用於 macOS 的 Microsoft Edge。 當您定義的觸發條件為 true 時，套件將部署到指定的電腦。

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Jamf.com](https://www.jamf.com/)
- [將 Jamf 與 Microsoft Intune 整合](/intune/conditional-access-integrate-jamf)