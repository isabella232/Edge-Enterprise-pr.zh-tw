---
title: 設定 IE 模式原則
ms.author: collw
author: AndreaLBarr
manager: srugh
ms.date: 07/23/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 設定 IE 模式原則
ms.openlocfilehash: 98d05af8769e25cfe2782a1e273f3b487afcead0
ms.sourcegitcommit: c6452a458f825dab5638db9ff31268c2dc27f8db
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/24/2021
ms.locfileid: "11677120"
---
# <a name="configure-ie-mode-policies"></a>設定 IE 模式原則

>[!Note]
> Internet Explorer 11 桌面應用程式將於 2022 年 6 月 15 日淘汰並退出支援 (如需範圍內項目的清單，[請參閱常見問題](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/internet-explorer-11-desktop-app-retirement-faq/ba-p/2366549))。 您目前使用的相同 IE11 應用程式和網站，可以在 Microsoft Edge 中以 Internet Explorer 模式開啟。 [從這裡深入了解](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/)。

本文說明如何設定 IE 模式原則。

> [!NOTE]
> 本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。

設定 IE 模式需要三個步驟：

1. [設定 Internet Explorer 整合](#configure-internet-explorer-integration)
2. [將網站從 Microsoft Edge 重新導向至 IE 模式](#redirect-sites-from-microsoft-edge-to-ie-mode)
3. (選用) [將網站從 IE 重新導向至 Microsoft Edge](#redirect-sites-from-ie-to-microsoft-edge)

    1. 如果您準備好停用 IE11 應用程式，請按照[停用 Internet Explorer 11](/deployedge/edge-ie-disable-ie11) 中的步驟進行
    2. 否則，請遵循[將網站從 IE 重新導向至 Microsoft Edge](/deployedge/edge-ie-mode-policies#redirect-sites-from-ie-to-microsoft-edge) 中的其餘步驟

> [!NOTE]
> 可透過 Intune 設定啟用 IE 模式的原則。 如需詳細資訊，請參閱[新增 Microsoft Edge 至 Microsoft Intune](/intune/apps/apps-windows-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) 和[使用 Microsoft Intune 設定 Microsoft Edge 原則](./configure-edge-with-intune.md)。

## <a name="configure-internet-explorer-integration"></a>設定 Internet Explorer 整合

您可以將 Internet Explorer 設定為直接在 Microsoft Edge 中開啟 (IE 模式)。 您也可以將 Internet Explorer 設定為使用獨立的 Internet Explorer 11 視窗開啟。 多數使用者偏好直接在 Microsoft Edge 內以 IE 模式開啟網站。

### <a name="enable-internet-explorer-integration-using-group-policy"></a>使用群組原則啟用 Internet Explorer 整合

1. 下載並使用最新的 [Microsoft Edge 原則範本](https://www.microsoft.com/en-us/edge/business/download)。
2. 開啟群組原則編輯器。
3. 按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。
4. 按兩下**設定 Internet Explorer 整合。**
5. 選取 **\[已啟用\]**。
6. 在 [選項]**** 下，將下拉式清單值設定為
   -  如果您想要在 Microsoft Edge 中以 IE 模式開啟網站，請選取 [Internet Explorer 模式]****
   -  如果您希望在獨立 Internet Explorer **11**視窗中開啟網站 (Internet Explorer 11 在 2022 年 6 月 15 日 Internet Explorer 11 桌面應用程式即將停用並結束支援之後，將不支援此選項。  在 2022 年 6 月 15 日之後，IE11 將無法再使用，此選項的行為會與 **Internet Explorer** 模式選項相同。)   
   -  如果您想要停止使用者透過 edge://flags 或透過命令列設定 Internet Explorer 模式，請選取 [無]****

   > [!NOTE]
   > 將原則設定為 [已停用]**** 表示 IE 模式已透過原則停用，但可透過 edge://flags 或命令列選項設定。
7. 按一下**確定**或**套用**儲存此原則設定。

## <a name="redirect-sites-from-microsoft-edge-to-ie-mode"></a>將網站從 Microsoft Edge 重新導向至 IE 模式

有兩個選項用於識別應在 IE 模式下開啟的網站：

- (建議) [在企業網站清單中設定網站](#configure-sites-on-the-enterprise-site-list)
- [設定所有內部網路網站](#configure-all-intranet-sites)

### <a name="configure-sites-on-the-enterprise-site-list"></a>在企業網站清單中設定網站

您可以使用以下群組原則，將特定網站設定為在 IE 模式下開啟：

- [使用企業模式 IE 網站清單](#configure-using-the-use-the-enterprise-mode-ie-website-list-policy) (Internet Explorer)
- [設定企業模式網站清單](#configure-using-the-configure-the-enterprise-mode-site-list-policy) (Microsoft Edge 版本 78 或更新版本)<br/>此原則允許您針對 Microsoft Edge 建立單獨的企業模式網站清單。 啟用此原則將覆寫 [使用企業模式 IE 網站清單] 原則中的設定，如果已啟用 [設定 Internet Explorer 整合]。 停用或不設定此原則不會影響 [設定 Internet Explorer 整合] 原則的預設行為。
    > [!NOTE]
    > 不強制設定 Microsoft Edge 原則。 許多組織會使用這項作為覆寫，讓他們以 IE 原則將目前網站清單的目標設定為所有使用者，並更輕鬆地將已更新版本的目標設定為具有 Microsoft Edge 原則的試驗使用者。

如需企業模式網站清單的詳細資訊，請參閱：

- [使用 Enterprise Mode Site List Manager](/internet-explorer/ie11-deploy-guide/use-the-enterprise-mode-site-list-manager)
- [使用檔案和 Enterprise Mode Site List Manager (結構描述 v.2) 將多個網站新增到企業模式網站清單](/internet-explorer/ie11-deploy-guide/add-multiple-sites-to-enterprise-mode-site-list-using-the-version-2-schema-and-enterprise-mode-tool)。

### <a name="configure-using-the-use-the-enterprise-mode-ie-website-list-policy"></a>使用 [使用企業模式 IE 網站清單] 原則進行設定：

IE 模式可以使用現有原則來設定 Internet Explorer 的企業網站清單，讓您建立並維護單一清單。

1. 建立或重複使用網站清單 XML
    1. 具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。
2. 開啟群組原則編輯器。
3. 按一下**使用者設定/電腦設定** > **系統管理範本** > **Windows 元件** > **Internet Explorer**。
4. 按兩下**使用企業模式 IE 網站清單**。
5. 選取 **\[已啟用\]**。
6. 在**選項**下，鍵入網站清單的位置。 您可以使用下列其中一個位置：
    - (建議) HTTPS 位置：**https**:**//iemode/sites.xml**
    - 區域網路檔案：**\\\network\shares\sites.xml**
    - 本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**
7. 按一下**確定**或**套用**儲存這些設定。

### <a name="configure-using-the-configure-the-enterprise-mode-site-list-policy"></a>使用 [設定企業模式網站清單] 原則進行設定

您也可以使用 Microsoft Edge 的個別原則來設定 IE 模式。 這個額外原則可讓您覆寫 IE 網站清單。 例如，某些組織會將生產環境網站清單的目標設定為所有使用者。 然後，您可以使用此原則將試驗網站清單部署到一小組使用者。

1. 建立或重複使用網站清單 XML
    1. 具有元素 _\<open-in\>IE11\</open-in\>_ 的所有網站現在都將在 IE 模式中開啟。
2. 開啟群組原則編輯器。
3. 按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。
4. 按兩下**設定企業模式網站清單**。
5. 選取 **\[已啟用\]**。
6. 在**選項**下，鍵入網站清單的位置。 您可以使用下列其中一個位置：
    - (建議) HTTPS 位置：**https**:**//iemode/sites.xml** <!--Trying to keep this from being an active link in MD -->
    - 區域網路檔案：**\\\network\shares\sites.xml**
    - 本機檔案：**file:///c:/Users/\<user\>/Documents/sites.xml**
7. 按一下**確定**或**套用**儲存這些設定。

### <a name="configure-all-intranet-sites"></a>設定所有內部網路網站

IE 模式可以設定為針對 [本機內部網路] 區域中的所有網站。 您可以使用企業模式網站清單從 IE 模式移除個別網站。

>[!NOTE]
>
> [本地內部網路] 區域包含明確新增的網站，但是也會使用啟發式學習法將網站指派給這個區域。 這可以包括無點主機名稱 (例如，**https**:**//payroll**)以及 Proxy 設定指令碼設定為略過 Proxy 的網站。 如果外部合作對象控制 DNS 或 Proxy，他們可能可以強制網站進入 IE 模式。

1. 開啟 [本機群組原則編輯器]。
2. 按一下**使用者設定/電腦設定** > **系統管理範本** > **Microsoft Edge**。
3. 按兩下**將所有內部網路網站傳送到 Internet Explorer**。
4. 選取**已啟用**，然後按一下**確定**或**套用**以儲存原則設定。

## <a name="redirect-sites-from-ie-to-microsoft-edge"></a>將網站從 IE 重新導向至 Microsoft Edge

您可以防止使用者針對不需要的網站使用 Internet Explorer。 如果網站不在您的網站清單上，Internet Explorer 可以自動將網站重新導向至 Microsoft Edge。

1. 開啟群組原則編輯器。
2. 按一下**使用者設定/電腦設定** > **系統管理工具** > **Windows 元件** > **Internet Explorer**。
3. 按兩下 [將未包含在企業模式網站清單中的所有網站傳送到 Microsoft Edge]****。
4. 選取 [已啟用]****
5. 按一下**確定**或**套用**儲存這些設定。
6. 按兩下 [設定用來開啟重新導向網站的 Microsoft Edge 通道]****。
7. 選取 **\[已啟用\]**。
8. 在 [選項]**** 底下，選取您要使用的通道前三個選項 - Internet Explorer 會重新導向至使用者已在該裝置上安裝的最高等級選項：
   - Microsoft Edge Stable
   - Microsoft Edge Beta 版本 77 或更新版本
   - Microsoft Edge Dev 版本 77 或更新版本
   - Microsoft Edge Canary 版本 77 或更新版本
   - Microsoft Edge 版本 45 或較舊版本
9. 按一下**確定**或**套用**儲存這些設定。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](./edge-ie-mode.md)
- [其他企業模式資訊](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
