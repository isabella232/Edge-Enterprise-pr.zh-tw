---
title: 'Microsoft Edge 中的 Enterprise Site List Manager  '
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/19/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '在 Microsoft Edge 中啟用和使用 Enterprise Site List Manager  '
ms.openlocfilehash: aa468888a05753fb5b033a8b99c2f6045f4e1b12
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617403"
---
# <a name="enterprise-site-list-manager-in-microsoft-edge"></a>Microsoft Edge 中的 Enterprise Site List Manager

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文說明如何在 Microsoft Edge 中啟用存取和使用 Enterprise Site List Manager ，以建立、編輯及匯出 Internet Explorer 模式的企業網站清單。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 89 或更新版本。 

## <a name="overview"></a>概觀

Enterprise Site List Manager 是[獨立企業模式網站清單管理器工具](https://www.microsoft.com/download/details.aspx?id=49974)的瀏覽器內版本，用於建立、編輯和匯出組織的網站清單。

未來將透過 Microsoft Edge 中的 Enterprise Site List Manager 提供對 Internet Explorer 模式工具的改良功能。 獨立工具將繼續在下載中心提供，但不會得到任何功能更新。

## <a name="enabling-access-to-enterprise-site-list-manager"></a>啟用對 Enterprise Site List Manager 的存取

您可以使用 [EnterpriseModeSiteListManagerAllowed](./microsoft-edge-policies.md#enterprisemodesitelistmanagerallowed) 群組原則來設定工具存取權。

如果啟用，您的使用者將在 *edge://compat* 中的左側瀏覽窗格中看到名為「Enterprise Site List Manager」的選項。 如果停用，使用者將不會在左側瀏覽窗格中看到 Enterprise Site List Manager 的進入點。 這是預設行為。

## <a name="using-the-enterprise-site-list-manager"></a>使用 Enterprise Site List Manager

Enterprise Site List Manager 工具使用 v.2 版的結構描述。 如果您將 v.1 版的結構描述匯入 Enterprise Site List Manager (結構描述 v.2)，它會將 XML 儲存為 v.2 版的結構描述。 請參閲[企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。

### <a name="add-single-sites-to-your-site-list"></a>新增單一站台至您的網站清單  

使用下列步驟將個別網站新增到您的網站清單中。

> [!NOTE]
> 您只能新增特定 URL，而非網際網路或內部網路區域。

1. 在 Enterprise Site List Manager 中，按一下  **[新增網站]**。
2. 在 URL 方塊中輸入要新增之網站的 URL，例如  <domain>.com 或  <domain>.com/<path> 。
3. 從 **[開啟位置]**  清單中選取以下選項之一：

   - **IE11**。 在 IE11 應用程式中開啟網站。
   - **IE 模式**。 在 Microsoft Edge 上以 Internet Explorer 模式開啟網站 (如已啟用)，否則在 IE11 應用程式中開啟網站。 請參閱 [Microsoft Edge 上的 Internet Explorer 模式](./edge-ie-mode.md)。
   - **MSEdge**。 在 Microsoft Edge 中開啟網站。
   - **可設定**。 允許網站參與 IE 模式引擎判斷。 請參閲[IE 模式中可設定的網站](./edge-learnmore-configurable-sites-ie-mode.md)
   - **無**。 在使用者選擇的任何瀏覽器中開啟。  

4. 在  **[相容模式下]**，選擇下列其中一項：

   - **IE8Enterprise**。 在 IE8 企業模式中載入網站。
   - **IE7Enterprise**。 在 IE7 企業模式載入網站。
   - **IE[x]**。 [x] 是文件模式的數目，而網站會以指定的文件模式載入。
   - **預設模式**。 使用頁面的預設相容性模式載入網站。

   網域內的路徑可能需要不同於網域本身的相容性模式。 例如，網域在預設的 IE11 瀏覽器中可能一切正常，但路徑可能會有問題，而需要使用企業模式。 如果您先前已新增網域，則仍會選取您原本選擇的相容性。 不過，如果網域是新的，則會自動選取  **[IE8 企業模式]** 。

   企業模式的優先順序高於文件模式，因此已經在企業模式網站清單中的網站不會受此更新影響，而會如往常一樣以企業模式載入。 如需使用文件模式的進一步詳細資訊，請參閱 [使用文件模式和企業模式網站清單修正網頁相容性問題](/internet-explorer/ie11-deploy-guide/fix-compat-issues-with-doc-modes-and-enterprise-mode-site-list)。

5. **[允許重新導向]** 核取方塊適用于處理伺服器端重新導向。 如果您勾選此方塊，伺服器端重新導向就會在 open-in 標記指定的瀏覽器中開啟。 如需詳細資訊，請在 [此處](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance#updated-schema-attributes)參閱。
6. 在 [註解] 方塊中輸入 **關於網站的任何註解**。 系統管理員只能在此工具中查看註解，並且這些註解保留在網站清單 xml 中。
7. 按一下 **[新增]** 以將網站新增到您的網站清單。

### <a name="export-site-list-to-xml"></a>將網站清單匯出到 XML

在 Enterprise Site List Manager 中建立您的網站清單後，可以將內容匯出至企業模式 (.EMIE) 或 XML 檔案。 

> [!NOTE]
> 此檔案包含您所有的 URL (包括您的相容性模式選項)，應儲存在安全之處。

若要匯出網站清單，請遵循下列步驟：

1. 在 Enterprise Site List Manager 中，按一下 **[匯出到 XML]**。
2. 輸入 **版本號碼** 和 **檔案名稱**。
3. 按一下 **[匯出]**。

您可以將檔案儲存在本機或網路共用位置。 不過，您必須確實將它部署到您的登錄機碼中指定的位置。 如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。

### <a name="import-multiple-sites-to-your-site-list"></a>將多個網站匯入您的網站清單

建立 .xml 檔案後，您可以使用 **[從 XML 匯入]** 功能，將網站大量新增至編輯器。

如果您想要取代編輯器中所有的內容，請按一下省略符號 (...) ，然後選擇 **[清除清單]**。 清除編輯器之後，請使用下列步驟來匯入網站。

1. 在 Enterprise Site List Manager 中，按一下 **[從 XML 匯入]**。 
2. 按一下 **[選擇檔案]** 選取您的網站清單，將包含的網站新增到工具中。 挑選您想要新增的網站清單，然後按一下 **[開啟]**。 支援的匯入格式為包含 Enterprise Mode Site List 的 v.2 結構描述的 .xml、.emie 或 .txt。 請參閲[企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)。
3. 按一下 **[載入]**  以從檔案 tp 編輯器新增網站。

您可以將檔案儲存在本機或網路共用位置。 不過，您必須確實將它部署到您的登錄機碼中指定的位置。 如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。

### <a name="edit-sites-in-your-site-list"></a>編輯您的網站清單中的網站

 您可以在 Enterprise Site List Manager 中編輯現有網站項目的屬性。 您也可以新增、移除或刪除相關聯的註解。

1. 在 Enterprise Site List Manager 中，按一下省略符號 (…)，然後為要編輯的 URL 選擇 **[編輯網站]**。
2. 您可以編輯網站項目的任何屬性，但 URL 除外。 完成編輯後，按一下 **[儲存]**。

   > [!NOTE]
   > 如果您想要刪除網站項目，請選擇步驟 1 中的 **[刪除網站]**。

3. 按一下 **[匯出至 XML]**，然後儲存已更新檔案。

您可以將檔案儲存在本機或網路共用位置。 不過，您必須確實將它部署到您的登錄機碼中指定的位置。 如需詳細資訊，請參閱 [開啟 Internet Explorer 模式和使用網站清單](./edge-ie-mode-policies.md)。

### <a name="preview-your-site-list-in-xml-format"></a>以 XML 格式預覽您的網站清單

匯出並儲存到網站清單位置之前，可以在編輯器中以 XML 格式預覽網站。 按一下 **[XML 預覽]** ，即可在新的索引標籤中開啟檔案。

### <a name="search-in-the-enterprise-site-list-manager"></a>在 Enterprise Site List Manager 中搜尋

您可以搜尋並查看特定網站是否已出現在網站清單中，若已存在，您就不用嘗試將它重新新增。

若要搜尋，請在編輯器右上角的  **[依 URL 篩選網站]** 搜尋方塊中鍵入部分 URL。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](./edge-ie-mode.md)
- [企業模式結構描述 v.2 指導方針](/internet-explorer/ie11-deploy-guide/enterprise-mode-schema-version-2-guidance)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)