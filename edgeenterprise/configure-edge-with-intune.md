---
title: 使用 Microsoft Intune 設定適用於 Windows 的 Microsoft Edge 原則設定
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Microsoft Intune 設定適用於 Windows 的 Microsoft Edge 原則設定。
ms.openlocfilehash: 63eb29018bf4ec9c5a32d11b215f422e150383c9
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978858"
---
# <a name="configure-microsoft-edge-policy-settings-with-microsoft-intune"></a>使用 Microsoft Intune 設定 Microsoft Edge 原則設定

本文說明如何使用 Microsoft Intune 設定適用於 Windows 10 的 Microsoft Edge 原則設定。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

您可以透過將裝置組態設定檔新增到 Microsoft Intune 來設定 Microsoft Edge 原則和設定。 使用 Intune 管理和實施原則，等同於在使用者裝置上使用 Active Directory 群組原則或設定本機群組原則物件 (GPO) 設定。

如需使用 Microsoft Intune 管理 Microsoft Edge 原則的詳細資訊，您可閱讀[透過搭配 Microsoft Intune 使用 Microsoft Edge 來管理 Web 存取](/intune/manage-microsoft-edge)，但請記住，此連結文章特定於 Microsoft Edge 版本 45 及更早版本，因此可能包含不適用於 Microsoft Edge 企業版 77 及更新版本的資訊和參考。

> [!TIP]
> 如需如何使用 Microsoft Intune 在 macOS 上設定 Microsoft Edge 的相關資訊，請參閱[進行 macOS 的設定](configure-microsoft-edge-on-mac.md)。

## <a name="create-a-profile-to-manage-settings-in-microsoft-edge-for-windows-10"></a>建立設定檔以在 Microsoft Edge 中管理 Windows 10 的設定

在 Microsoft Intune 中使用系統管理範本，您可以使用雲端管理 Windows 10 裝置上的 Microsoft Edge 群組原則。 本節將協助您建立範本以設定 Microsoft Edge 專屬的應用程式設定。 建立範本時，它會建立裝置組態設定檔。 然後，您可以將此設定檔指派或部署到組織中的 Windows 10 裝置。

### <a name="prerequisites"></a>必要條件

- Windows 10，具有下列最低系統需求︰
  - Windows 10 版本 1909
  - Windows 10 版本 1903，需安裝 [KB4512941](https://support.microsoft.com/kb/4512941)
  - Windows 10 版本 1809，需安裝 [KB4512534](https://support.microsoft.com/kb/4512534)
  - Windows 10 版本 1803，需安裝 [KB4512509](https://support.microsoft.com/kb/4512509)
  - Windows 10 版本 1709，需安裝 [KB4516071](https://support.microsoft.com/kb/4516071)

### <a name="use-administrative-templates-to-create-a-policy-for-microsoft-edge"></a>使用 [系統管理範本] 建立 Microsoft Edge 原則

此程序利用 Intune 內建的系統管理範本 (您可能熟悉的群組原則)。 您可以使用這些範本來建立 Microsoft Edge 原則，方法是從預先設定的清單中選取 [設定]。

1. 登入 [Microsoft 端點管理員](https://endpoint.microsoft.com/) 入口網站。
2. 在左側瀏覽窗格中，選取 **[裝置]**。
3. 從 **[裝置]** | **概述**中，選取 **[組態設定檔]** (在 [原則] 標題下)。
4. 在頂端命令列上，選取**建立設定檔**。
5. 在 **[平台]** 下方的下拉式清單中，選取 **[Windows 10 及更新版本]**。
6. 在配置檔案類型下方的下拉式 **清單中，** 選取 **範本**。
7. 在 [ **範本名稱下**， **選取系統管理範本** ，然後按一下建立 **按鈕** 。 下個螢幕擷取畫面顯示可選取 [平台] 和 [設定檔] 類型的下拉式清單。

    ![選取 [平台] 和 [設定檔] 類型](./media/configure-edge-with-intune/create-profile-platform.png)

7. 在 **[基本資料]** 索引標籤，輸入描述性 **[名稱]**，例如 [Microsoft Edge 原則]。 選擇性輸入原則的 **描述**。
下個螢幕擷取畫面顯示 **[基本資料]** 索引標籤的表單，而且功能表列會顯示後續步驟 (索引標籤呈現灰色) 來建立設定檔。

   ![輸入 [名稱和描述]](./media/configure-edge-with-intune/create-profile-basics-tab.png)

8. 選取 **\[下一步\]**。
9. 在 **[組態設定]** 索引標籤上，選取下列其中一個位置中的 [Microsoft Edge] 資料夾：

   - 在 [電腦設定] 資料夾下方
   - 在 [使用者設定] 資料夾下方。

   將會在右側窗格中顯示適用於 Microsoft Edge 的設定。 例如，下列螢幕擷取畫面所示的*電腦設定/Microsoft Edge/允許下載限制*。

   ![[組態設定] 索引標籤](./media/configure-edge-with-intune/create-profile-configuration-settings-tab.png)

   > [!NOTE]
   > 如需 Microsoft Edge 所有可用設定的最完整和最新之清單，請參閱 [Microsoft Edge – 原則](./microsoft-edge-policies.md) 和 [Microsoft Edge – 更新原則](./microsoft-edge-update-policies.md)。

10. 使用搜尋欄位 (「搜尋以篩選項目...」) 來尋找您要設定的特定設定。 在此範例中，搜尋字串為「首頁」。 下個螢幕擷取畫面顯示搜尋結果。

    ![搜尋結果](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-search.png)

11. 當您找到想要設定的設定之後，請選取它以顯示您可以設定的值。 在下個螢幕擷取畫面中，我們選取 [設定首頁 URL] 做為範例。

    ![設定首頁 URL 原則](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-edit-pol.png)

12. 啟用原則，並輸入首頁 URL 的值，如上個螢幕擷取畫面所示。

13. 按一下 \[確定\] ****。 [狀態] 欄位應顯示為 [已啟用]，如下方螢幕擷取畫面範例所示。

    ![設定狀態已啟用](./media/configure-edge-with-intune/create-profile-configuration-settings-tab-set-enabled.png)

14. 按一下 **\[下一步\]** 按鈕。

15. 如果需要，請在 **[範圍標籤]** 索引標籤上，新增一個範圍標籤，否則請按一下 **[下一個]** 按鈕。

16. 在 **[指派]** 索引標籤上，按一下 **[+ 選取要包含的群組]** 將此原則指派給 Azure Active Directory (Azure AD) 群組，其中包含想要接收此原則設定的裝置或使用者。 請參閱 [在 Microsoft Intune 中指派使用者和裝置設定檔](/intune/device-profile-assign)，以了解如何將設定檔指派給 Azure AD 使用者或裝置群組的相關資訊。

    ![選取要包含的群組](./media/configure-edge-with-intune/create-profile-assignments-tab.png)

17. 按一下 **\[下一步\]** 按鈕。

18. 在 **[檢閱 + 建立]** 索引標籤上，檢閱變更摘要以確保其正確無誤，然後按一下 **[建立]** 按鈕。

19. 新建立的原則 (Microsoft Edge 原則) 會顯示在下方螢幕擷取畫面中。

    ![選取要包含的群組](./media/configure-edge-with-intune/create-profile-new-policy-finished.png)

如需 Windows 10 設定檔的詳細資訊，請參閱[在 Microsoft Intune 中使用 Windows 10 範本設定群組原則設定](/intune/administrative-templates-windows)。

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [透過搭配 Microsoft Intune 使用 Microsoft Edge 來管理 Web 存取](/intune/manage-microsoft-edge)
- [使用 Windows 10 範本在 Microsoft Intune 中設定群組原則設定](/intune/administrative-templates-windows)
- [使用 Microsoft Intune 部署 Microsoft Edge](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)
