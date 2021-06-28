---
title: Enterprise Site Discovery 逐步指南
ms.author: collw
author: appcompatguy
manager: saudm
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 Enterprise Site Discovery 準備 IE 模式
ms.openlocfilehash: f6298b801cceeb96d9285f3597de2a6abe8ee36e
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617473"
---
# <a name="enterprise-site-discovery-step-by-step-guide"></a>Enterprise Site Discovery 逐步指南

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文提供將 Enterprise Site Discovery 與 Microsoft Endpoint Configuration Manager 搭配使用的逐步指南。

Enterprise Site Discovery 可協助您設定企業模式網站清單。 Enterprise Site Discovery 將協助您：

- 探索哪些網站使用舊版文件模式。 除非這些網站偵測新式瀏覽器並提供不同 HTML，否則可能需要使用 IE 模式。
- 探索哪些網站使用 ActiveX 控制項。 Microsoft Edge 不支援 ActiveX 控制項。 除非這些網站偵測新式瀏覽器並提供不同 HTML，否則可能需要使用 IE 模式。

> [!NOTE]
> 本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。

## <a name="prerequisites"></a>必要條件

本指南假設您已使用過 Microsoft Endpoint Configuration Manager，且已安裝下列服務和角色：

1. Microsoft Endpoint Configuration Manager
2. Microsoft SQL Server Reporting Services
3. (選用) 已設定 Configuration Manager Reporting Services 點角色

## <a name="download-enterprise-site-discovery-tools"></a>下載 Enterprise Site Discovery 工具

下載下列工具：

- [Enterprise Site Discovery 設定和組態套件](https://go.microsoft.com/fwlink/p/?LinkId=517719)
- [Microsoft 報表產生器](https://www.microsoft.com/download/details.aspx?id=53613)

## <a name="enable-enterprise-site-discovery"></a>啟用 Enterprise Site Discovery

您必須先將 WMI 類別提供者部署到裝置上，才能連線到 Windows Management Instrumentation (WMI) 來取得網站探索資料。

從 **Enterprise Site Discovery 設定和組態套件**將內容解壓縮至可用的軟體程式庫檔案共用中的資料夾。 範例：**\\\\DSL\\EnterpriseSiteDiscovery**。

接下來，在 Microsoft Endpoint Configuration Manager 中建立套件，如此[文件](/configmgr/apps/deploy-use/packages-and-programs)所述，選取下列選項：

- 在 **[套件]** 頁面上，選取 **[名稱]**，並指定名稱 **[啟用網站探索]**
- 在 **[套件]** 頁面上，選取 **[此套件包含來源檔案]**
- 在 **[套件]** 頁面上指定您解壓縮檔案的來源資料夾 (例如，**\\\\DSL\\EnterpriseSiteDiscovery**)
- 在 **[程式類型]** 頁面上，選擇 **[標準程式]**
- 在 **[標準程式]** 頁面上，輸入命令列以設定裝置上的網站探索，如下所示：
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1
  ```
  > [!NOTE]
  > 指令碼支援為 `-ZoneAllowList` 和 `-SiteAllowList` 使用命令列參數。 在這個逐步說明中，我們將透過群組原則來設定這些選項 (如下所示)。
- 在 **[標準程式]** 頁面中，選取選項以執行 **[隱藏]**。
- 在 **[標準程式]** 頁面的 **[程式可執行]** 中，選取選項 **[無論使用者是否登入]**

建立套件後，按兩下套件名稱 **[啟用網站探索]** 以查看其內容。 在 **[執行之後]** 屬性中，選取 **[Configuration Manager 重新啟動電腦]**。 裝置重新開機後，WMI 資料收集就會開始。

> [!NOTE]
> 您可以設定使用者必須重新啟動裝置所需的時間，如[用戶端設定文件](/configmgr/core/clients/deploy/about-client-settings#computer-restart)中所述。

## <a name="configure-enterprise-site-discovery-via-group-policy"></a>使用群組原則設定 Enterprise Site Discovery

啟用 Enterprise Site Discovery 後，您就可以設定要收集的資料。 請考量[此處](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery#what-data-is-collected)所述的當地法律和法規需求。

1. 開啟群組原則編輯器
2. 按一下**電腦設定** > **系統管理範本** > **Windows 元件** > **Internet Explorer** 
3. 按兩下 **[開啟網站探索 WMI 輸出]**
4. 選取 [已啟用]****
5. 按一下 **[確定]** 或 **[套用]** 儲存此原則設定

您可以限制收集網站資料的區域：

1. 按兩下 **[由區域限制網站探索輸出]**
2. 選取 [已啟用]****
3. 輸入位元遮罩，以指示要啟用網站探索的區域：
    1. 受限制的網站區域
    2. 網際網路區域
    3. 信任的網站區域
    4. 近端內部網路區域
    5. 本機電腦區域
    
    範例 1：**00010** 只會收集近端內部網路區域的資料

    範例 2：**10111** 會收集除了網際網路區域以外的所有區域的資料
4. 按一下 **[確定]** 或 **[套用]** 儲存此原則設定

您可以限制收集網站資料的網域：

1. 按兩下 **[由網域限制網站探索輸出]**
2. 選取 [已啟用]****
3. 輸入您要收集資料的網域，每行一個網域
4. 按一下 **[確定]** 或 **[套用]** 儲存此原則設定

## <a name="collect-site-discovery-data-using-configuration-manager"></a>使用 Configuration Manager 收集網站探索資料

現在，您的裝置正在產生資料，是時候在 Configuration Manager 中收集這些資料了。

1. 在 Configuration Manager 主控台中，選擇 **[管理]** > **[用戶端設定]** > **[預設用戶端設定]**
2. 在 **[首頁]** 索引標籤的 **[內容]** 群組中，選擇 **[內容]**。
3. 在 **[預設用戶端設定]** 對話方塊中，選擇 **[硬體清查]**
4. 在 **[裝置設定]** 清單中，選擇 **[設定類別]**
5. 在 **[硬體清查類別]** 對話方塊中，選擇 **[新增]**
6. 在 **[新增硬體清查類別]** 對話方塊中，按一下 **[連線]**
7. 在 **[連線到 Windows Management Instrumentation (WMI)]** 對話方塊中，輸入設定 Enterprise Site Discovery 的電腦名稱。 如果您要連線到另一部電腦，您需要具備存取 WMI 權限的認證。
8. 在 **[WMI 命名空間]** 文字方塊中，輸入 **root\cimv2\IETelemetry**
9. 選擇 **[連線]**
10. 在 **[新增硬體清查類別]** 對話方塊的 **[清查類別]** 清單中，選取 WMI 類別**IESystemINfo**、**IEUrlInfo**、和 **IECountInfo*。
11. 按一下 **[確定]** 以關閉 **[類別限定詞]** 對話方塊及其他開啟的對話方塊。

用戶端更新管理點中的設定後，系統會在下次硬體清查執行時 (預設為每七天) 報告資料。

## <a name="import-site-discovery-reports"></a>匯入網站探索報表

Enterprise Site Discovery 套件包含兩個範例報表。 一個報表使用 ActiveX 控制項顯示網站，另一個報表使用舊版文件模式顯示網站。

### <a name="configure-the-site-discovery-sample-report"></a>設定網站探索範例報表

使用下列程序建立使用三個資料來源的範例報表：使用者造訪的網站、其系統相關資訊，以及網站所使用的文件模式。 此報表可協助您識別可能依靠舊版文件模式的網站。

1. 將報表 **SCCM_Report-Site_Discovery.rdl** 複製到 Configuration Manager 伺服器。
2. 安裝 [Microsoft 報表產生器](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15)。
3. 按兩下 **SCCM_Report-Site_Discovery.rdl** 以在報表產生器中開啟報表。
4. 第一次嘗試開啟報表時，它會嘗試與建立該報表的伺服器聯繫。 當系統提示您**連接到報表伺服器**時，請按一下 **[否]**。
5. 報表開啟後，展開 **[資料來源]**，然後按兩下 **[DataSource1]**。
6. 在 **[資料來源屬性]** 視窗中，選取 **[使用內嵌在我的報表中的連線]**，然後按一下 **[建置...]** 按鈕。
7. 在 **[連線內容]** 視窗中，選取 **[伺服器名稱]**，然後輸入 Configuration Manager 伺服器的名稱。 然後，在 **[選取或輸入資料庫名稱]** 中，從下拉式清單中選取 Configuration Manager 資料庫的名稱。
8. 按一下 **[確定]** 關閉 **[連線內容]** 視窗。
9. 按一下 **[測試連線]** 以測試連線。 如果連線成功，請按一下 **[確定]** 關閉 **[資料來源屬性]** 視窗。
10. 在 **[資料來源 2]** 重複執行步驟 5 到 9。
11. 展開 **[資料集]**，然後按兩下 **[DataSet1]**。
12. 在 **[資料集屬性]** 視窗中，按一下 **[查詢:]** 文字方塊，然後使用您在步驟 7 中選取的資料庫名稱來取代 **CM_A1B**。
13. 在 **DataSet2**、**DataSet3**和 **DataSet4**重複步驟 11 到 12。
14. 在功能區的 **[首頁]** 索引標籤中，按一下 **[執行]** 按鈕來測試報表。
15. 儲存報表。
16. 關閉 Microsoft 報表產生器。
17. 將檔案重新命名為 **Site Discovery.rdl**

### <a name="configure-the-activex-sample-report"></a>設定 ActiveX 範例報告

使用下列程序建立使用單一資料來源的範例報告：使用 ActiveX 控制項的網站。 由於 Internet Explorer 是唯一支援 ActiveX 控制項的瀏覽器，因此這些網站可能需要 IE 模式。

1. 將報表 **SCCM Report Sample - ActiveX.rdl** 複製到 Configuration Manager 伺服器。
2. 安裝 [Microsoft 報表產生器](/sql/reporting-services/install-windows/install-report-builder?view=sql-server-ver15)。
3. 按兩下 **SCCM Report Sample - ActiveX.rdl** 以在報表產生器中開啟報表。
4. 第一次嘗試開啟報表時，它會嘗試與建立該報表的伺服器聯繫。 當系統提示您**連接到報表伺服器**時，請按一下 **[否]**。
5. 報表開啟後，展開 **[資料來源]**，然後按兩下 **[AutoGen__5C6358F2_4BB6_4a1b_A16E_8D96795D8602_]**。
6. 在 **[資料來源屬性]** 視窗中，選取 **[使用內嵌在我的報表中的連線]**，然後按一下 **[建置...]** 按鈕。
7. 在 **[連線內容]** 視窗中，選取 **[伺服器名稱]**，然後輸入 Configuration Manager 伺服器的名稱。 然後，在 **[選取或輸入資料庫名稱]** 中，從下拉式清單中選取 Configuration Manager 資料庫的名稱。
8. 按一下 **[確定]** 關閉 **[連線內容]** 視窗。
9. 按一下 **[測試連線]** 以測試連線。 如果連線成功，請按一下 **[確定]** 關閉 **[資料來源屬性]** 視窗。
10. 展開 **[資料集]**，然後按兩下 **[DataSet1]**。
11. 在 **[資料集屬性]** 視窗中，按一下 **[查詢:]** 文字方塊，然後使用您在步驟 7 中選取的資料庫名稱來取代 **CM_A1B**。
12. 在功能區的 **[首頁]** 索引標籤中，按一下 **[執行]** 按鈕來測試報表。
13. 儲存報表。
14. 關閉 Microsoft 報表產生器。
15. 將檔案重新命名為 **ActiveX**

### <a name="upload-configured-reports-to-microsoft-sql-server-reporting-services"></a>將已設定的報表上傳到 Microsoft SQL Server Reporting Services

設定好環境報表後，將報表上傳到報表伺服器。

1. 啟動 **Reporting Services 組態管理員**應用程式。
2. 在 **[報表伺服器連線]** 視窗中，按一下 **[連線]**，然後按一下 **[Web 入口網站身分識別]** 底下所列的 URL
3. 在開啟的瀏覽器視窗中，您應該位於 **SQL Server Reporting Services 頁面** - 按一下 SCCM 網站程式碼的 **ConfigMgr_SCCMSiteCode** 資料夾。
4. 在功能區中，將游標停留在 **[+新增]**，然後按一下 **[資料夾]** 功能表項目。
5. 輸入資料夾名稱，例如 **Enterprise Site Discovery**，然後按一下 **[建立]** 按鈕。
6. 按一下 **Enterprise Site Discovery** 資料夾。
7. 在功能區中，按一下 **[上傳]** 按鈕。
8. 選取 **[網站探索]** 報表，然後按一下 **[確定]**。
9. 在 **ActiveX** 報表重複步驟 7 與 8。

### <a name="view-reports-in-configuration-manager"></a>檢視 Configuration Manager 中的報表

現在您已自訂並上傳報表，您可以在 Configuration Manager 中檢視報表。

1. 在 Configuration Manager 主控台中，選擇 **[監視]** > **[報表]** > **[報表]** > **[Enterprise Site Discovery]**
2. 按兩下報表以檢視報表。

## <a name="disable-enterprise-site-discovery"></a>停用 Enterprise Site Discovery

資料收集完畢後，您應停用 Enterprise Site Discovery。 建立第二個套件來停用 Microsoft Endpoint Configuration Manager 中的 Enterprise Site Discovery，如此[文件](/configmgr/apps/deploy-use/packages-and-programs)所述，選取下列選項：

- 在 **[套件]** 頁面上，選取 **[名稱]**，並指定名稱 **[停用網站探索]**
- 在 **[套件]** 頁面上，選取 **[此套件包含來源檔案]**
- 在 **[套件]** 頁面上指定您解壓縮檔案的來源資料夾 (例如，**\\\\DSL\\EnterpriseSiteDiscovery**)
- 在 **[程式類型]** 頁面上，選擇 **[標準程式]**
- 在 **[標準程式]** 頁面上，輸入停用裝置上的網站探索的命令列，如下所示：
  ```dos
  powershell.exe -ExecutionPolicy Bypass .\IETelemetrySetUp-Win8.ps1 -IEFeatureOff
  ```
- 在 **[標準程式]** 頁面中，選取選項以執行 **[隱藏]**
- 在 **[標準程式]** 頁面的 **[程式可執行]** 中，選取選項 **[無論使用者是否登入]**

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](./edge-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
- [其他 Enterprise Site Discovery 資訊](/internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery)