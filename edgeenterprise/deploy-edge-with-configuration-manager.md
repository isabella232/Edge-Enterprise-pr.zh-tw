---
title: 使用 System Center Configuration Manager 部署 Microsoft Edge
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 06/08/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何使用 System Center Configuration Manager (SCCM) 部署 Microsoft Edge。
ms.openlocfilehash: b403c8924a0f970aaadff2e1b20ebd05c0641a96
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617543"
---
# <a name="deploy-microsoft-edge-using-system-center-configuration-manager"></a>使用 System Center Configuration Manager 部署 Microsoft Edge

本文介紹如何使用 System Center Configuration Manager (SCCM) 自動執行 Microsoft Edge 部署。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="before-you-begin"></a>在您開始前

請檢閱[介紹 Configuration Manager 中的應用程式管理](/sccm/apps/understand/introduction-to-application-management)中的資訊。 此應用程式管理文章可協助您了解本文中使用的術語，並可做為準備網站以安裝應用程式的指南。

從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 企業安裝檔案 (**MicrosoftEdgeDevEnterpriseX64.msi** 和/或 **MicrosoftEdgeDevEnterpriseX86.msi**)。

請確保將 Microsoft Edge 安裝檔案儲存在可存取的網路位置。

## <a name="create-the-application"></a>建立應用程式

您將使用 Configuration Manager 精靈建立應用程式。

### <a name="start-the-create-application-wizard-and-create-the-application"></a>啟動建立應用程式精靈並建立應用程式  

1. 在 Configuration Manager 主控台中，按一下**軟體程式庫** > **應用程式管理** > **應用程式**。  

2. 在**首頁**索引標籤的**建立**群組中，按一下**建立應用程式**。 或者，在瀏覽器列的**應用程式**上按右鍵，然後按一下**建立應用程式**。

    ![建立應用程式](./media/edge-ent-deployment-sccm/edge-ent-create-app-1.png)

3. 在**建立應用程式精靈**的**一般**頁面，選取**從安裝檔案自動偵測此應用程式的相關資訊**。 這將會使用從安裝 .msi 檔案中提取的資訊，在精靈中預先填入一些資訊。 提供下列資訊：  

   - **類型**：選擇 **Windows Installer (\*.msi 檔案)**。  

   - **位置**：鍵入安裝檔案 **MicrosoftEdgeDevEnterpriseX64.msi** 或 **MicrosoftEdgeDevEnterpriseX86.msi** 的位置 (或按一下**瀏覽**以選取位置)。 請注意，必須以 *\\\Server\Share\File* 格式指定位置，Configuration Manager 才能找到安裝檔案。  

   您的**指定此應用程式的設定**頁面看起來會像下列範例：  

    ![指定此應用程式的設定](./media/edge-ent-deployment-sccm/edge-ent-create-app-2.png)

4. 按**下一步**。 在**匯入的資訊**頁面上的**詳細資料**下，您將看到有關應用程式和匯入的任何關聯檔案的資訊。 按**下一步**以繼續進行精靈。  

    ![檢視匯入的資訊](./media/edge-ent-deployment-sccm/edge-ent-create-app-3.png)

5. 在**一般資訊**頁面上，可以新增有關應用程式的詳細資訊。 例如，軟體版本、系統管理員註解和發行者。 您可以使用此資訊來協助在 Configuration Manager 主控台中排序和尋找應用程式。

   您還可以使用**安裝程式**欄位指定將用於在電腦上安裝應用程式的完整命令列。 您可以對此進行編輯以新增您自己的內容 (例如，用於自動安裝的 **/q**)。

   以下螢幕擷取畫面顯示一個範例，其中使用了**指定此應用程式的資訊**欄位。

   ![指定應用程式中繼資料](./media/edge-ent-deployment-sccm/edge-ent-create-app-5.png)

6. 按**下一步**。
7. 在**摘要**頁面上，您可以在**詳細資訊**下確認應用程式設定，然後使用精靈完成。 按**下一步**。  

    ![應用程式設定的詳細資料](./media/edge-ent-deployment-sccm/edge-ent-create-app-6.png)

8. 在**完成**頁面上，按一下**關閉**。

    ![成功對話方塊](./media/edge-ent-deployment-sccm/edge-ent-create-app-7.png)

您已完成建立應用程式。 使用以下步驟在 Configuration Manager 中查看它：

- 選取**軟體程式庫**工作區
- 展開**應用程式管理**
- 按一下**應用程式**。

下面的螢幕擷取畫面顯示用於本文的範例。  

![應用程式](./media/edge-ent-deployment-sccm/edge-ent-create-app-8.png)

## <a name="change-application-properties-and-deployment-settings"></a>變更應用程式內容和部署設定

建立應用程式後，如有需要，可以精簡應用程式設定。 若要查看應用程式內容：

- 選取應用程式
- 在**首頁**>**內容**中按一下**內容**。  

   ![設定應用程式內容](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-1.png)

 在 **<application name\> 應用程式內容**對話方塊中，您將看到項目的索引標籤式檢視，您可設定這些項目以變更應用程式的行為。 如需有關您可進行之設定的詳細資訊，請參閱[建立應用程式](/sccm/apps/deploy-use/create-applications)。

在此範例中，您將變更應用程式部署類型的一些內容。 若要變更部署內容：

1. 按一下**部署類型**索引標籤。
2. 在**部署類型**下，選取應用程式**名稱**
3. 按一下**編輯**。

   ![編輯部署類型](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-2.png)

### <a name="add-a-requirement-to-the-deployment-type"></a>新增需求至部署類型

 需求指定必須符合的條件，才可以在裝置上安裝應用程式。 您可以從內建需求中進行選擇，也可以建立自己的需求。 例如，您可以新增一項需求，要求應用程式僅安裝在執行 Windows 10 **x86** 或 **x64** 的電腦上，具體取決於安裝檔案的目標處理器架構。 在此範例中，您將指定 Windows 10 **x86**。

1. 從剛剛開啟的部署類型內容頁面中，按一下**需求**索引標籤。

2. 按一下**新增**以開啟**建立需求**對話方塊。

    ![建立需求](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-3.png)

3. 在**建立需求**對話方塊中，指定下列資訊：

    - **類別**：**裝置**  

    - **條件**：**作業系統**  

    - **規則類型**：**值**  

    - **運算子**：**其中之一**  

    - 從作業系統清單中，選取 **Windows 10** > **所有 Windows 10 (32 位元)**。  

    完成後，對話方塊將類似於以下螢幕擷取畫面範例：

    ![新增需求](./media/edge-ent-deployment-sccm/edge-ent-create-app-req-4.png)

4. 按一下**確定**以關閉每個開啟的內容頁，然後返回 Configuration Manager 主控台中的**應用程式**清單。  

## <a name="add-the-application-content-to-a-distribution-point"></a>將應用程式內容新增到發佈點  

若要將更新的應用程式部署到 PC，請確保將應用程式內容複製到發佈點。 電腦會存取發佈點以安裝應用程式。  

>[!TIP]
>若要深入了解 Configuration Manager 中的發佈點和內容管理，請參閱[部署和管理 System Center Configuration Manager 的內容](/sccm/core/servers/deploy/configure/deploy-and-manage-content)。  

1. 在 Configuration Manager 主控台中，按一下**軟體程式庫**。  

2. 在**軟體程式庫**工作區內，展開**應用程式**。 在應用程式清單中選取您建立的應用程式。

3. 在**部署**群組的**首頁**索引標籤中，按一下**發佈內容**。  

4. 在**發佈內容精靈**的**一般**頁面中，檢查應用程式名稱是否正確，然後按**下一步**。  

5. 在**內容**頁面上，檢閱將要複製至發佈點的資訊，然後按**下一步**。  

6. 在**內容目的地**頁面上，按一下**新增**以選取要在其上安裝應用程式內容的一或多個集合、發佈點或發佈點群組。

7. 完成精靈。

您可以在**發佈狀態** > **內容狀態**下，從**監控**工作區檢查應用程式內容是否已成功複製到發佈點。  

## <a name="deploy-the-application"></a>部署應用程式  

接下來，將應用程式部署到階層中的裝置集合。 在此範例中，您將應用程式部署到**所有系統**裝置集合。  

>[!TIP]
>請記住，由於您之前選取的需求，只有指定處理器架構的 Windows 10 電腦才會安裝該應用程式。  

1. 在 Configuration Manager 主控台中，按一下**軟體程式庫** > **應用程式管理** > **應用程式**。

2. 在應用程式清單中，選取您稍早建立的應用程式。 接著，在**部署**群組的**首頁**索引標籤，按一下**部署**或在應用程式上按右鍵，然後選取**部署**。

    ![部署應用程式](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-1.png)

3. 在**部署軟體精靈**的**一般**頁面上，按一下**瀏覽**以選取要將應用程式部署到的裝置集合。

    ![瀏覽至安裝檔案](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-2.png)

4. 在**內容**頁面上，檢查是否選取了希望電腦安裝應用程式的發佈點。

    ![指定發佈點](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-6.png)

5. 在**部署設定**頁面上，確保部署動作設定為**安裝**，並且部署目的設定為**必要**。

    ![進行部署設定](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-8.png)

    >[!TIP]
    >透過將部署目的設定為**必要**，可以確保應用程式安裝在符合您所設定需求的電腦上。 如果將此值設定為**可用**，則使用者可以視需求從軟體中心安裝應用程式。  

6. 在**排程**頁面上，可以設定何時安裝應用程式。 對於此範例，選取**在可用時間之後盡快**。

    ![排程部署](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-9.png)

7. 在**使用者經驗**頁面上，選取所需的值然後按**下一步**。

    ![指定使用者體驗](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-10.png)

8. 指定所需的警示選項，然後按**下一步**。

    ![指定警示設定](./media/edge-ent-deployment-sccm/edge-ent-deploy-app-11.png)

9. 完成精靈。

使用以下**監控應用程式**一節中的資訊，查看應用程式部署的狀態。  

## <a name="monitor-the-application"></a>監控應用程式

 在本節中，您將快速檢視剛剛部署之應用程式的部署狀態。  

### <a name="to-review-the-deployment-status"></a>若要檢閱部署狀態  

1. 在 Configuration Manager 主控台中，按一下**監控** > **部署**。  

2. 從部署清單中選取應用程式。

    ![監控部署](./media/edge-ent-deployment-sccm/edge-ent-monitor-deployment.png)

3. 在**部署**群組的**首頁**索引標籤中，按一下**檢視狀態**。  

4. 選擇以下索引標籤之一，查看有關應用程式部署的更多狀態更新：  

    - **成功**：應用程式已成功安裝在指示的電腦上。  

    - **進行中**：應用程式尚未完成安裝。  

    - **錯誤**：在指示的電腦上安裝應用程式時出錯。 還會顯示有關該錯誤的詳細資訊。  

    - **不符合需求**：未在指示的裝置上進行安裝嘗試，因為裝置不符合您設定的需求 (在此範例中，則是因為它們不在 Windows 10 上執行)。

    - **不明**： Configuration Manager 無法報告部署狀態。 請稍後再回來查看。  

    >[!TIP]
    >有幾個方式可以監控應用程式部署。 如需詳細資訊，請參閱[從 System Center Configuration Manager 主控台監控應用程式](/sccm/apps/deploy-use/monitor-applications-from-the-console)。  

## <a name="end-user-experience"></a>使用者經驗  

具有由 Configuration Manager 管理且執行指定處理器架構 Windows 10 電腦的使用者會看到一則訊息，告知必須安裝 Microsoft Edge Dev 應用程式。 當他們接受此安裝選項時，就會安裝應用程式。  

## <a name="see-also"></a>也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [使用 System Center Configuration Manager 建立及部署應用程式](/sccm/apps/get-started/create-and-deploy-an-application)