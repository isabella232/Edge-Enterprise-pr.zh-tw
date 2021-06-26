---
title: '依原則的每一網站設定 '
ms.author: collw
author: AndreaLBarr
manager: laurawi
ms.date: 05/03/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: '依原則的每一網站設定 '
ms.openlocfilehash: 6bba2c9b1d691c338a3146ef246de9f94e262a03
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618064"
---
# <a name="persite-configuration-by-policy"></a>依原則的每一網站設定

## <a name="introduction-browsers-as-decision-makers"></a>簡介：瀏覽器做為決策者

隨著每個頁面載入的一部分，瀏覽器會進行許多決策，其中包括：特定 API 應該可供使用嗎？ 應該允許資源載入嗎？ 應該允許指令碼執行嗎？ 清單太長。

在大部分情況下，決策是由兩個輸入所控管：使用者設定，以及進行決策的頁面 URL。

在舊版 Internet Explorer Web 平台中，這些決策都稱為  [URLAction](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178%28v%3dvs.85%29)，而網際網路控制台內的企業群組原則和使用者設定會控制瀏覽器處理每個決策的方式。  

在 Microsoft Edge 中，多數的每一網站權限是由使用簡單語法 (具有有限萬用字元支援) 表達的設定和原則所控制。 Windows 安全性區域仍只能用於少量的設定決策。

## <a name="background-windows-security-zones"></a>背景：Windows 安全性區域

為了簡化使用者或其系統管理員的設定，舊版平台將網站分類為五個不同的 **安全性區域**：本機電腦、近端內部網路、信任的網站、網際網路和限制的網站。

做出決策時，瀏覽器會先將網站對應至區域，然後查閱該區域的 URLAction 的設定，以決定該執行的動作。 合理的預設值 (例如「自動滿足來自我的內部網路的驗證挑戰」) 表示多數使用者不需要變更任何預設值的設定。

使用者可以使用網際網路控制台將特定網站指派給區域，並設定每個區域的權限結果。 在受管理環境中，系統管理員可以使用群組原則來為區域指派特定網站 (透過「指派網站到區域清單」原則)，並以每個區域為基礎指定 URLActions 的設定。 除了手動管理網站或將使用者網站指派至區域之外，其他啟發學習法可以 [將網站指派給近端內部網路區域](/archive/blogs/ieinternals/the-intranet-zone)。 特別是，無點的主機名稱 (例如 `http://payroll`) 為指派給內部網路區域。 如果使用 Proxy 設定指令碼，設定為略過 Proxy 的任何網站都會對應至內部網路區域。

舊版 Microsoft Edge 繼承了其前身 Internet Explorer 的區域架構，並有一些簡化的變更：

- Windows 的五個內建區域已減少為三個：網際網路 (網際網路)、信任 (內部網路+信任) 和本機電腦。 已移除「限制的網站」區域。

- 區域到 URLAction 的對應已硬式編碼到瀏覽器，忽略網際網路控制台中的群組原則和設定。

## <a name="per-site-permissions-in-the-microsoft-edge"></a>Microsoft Edge 中的每一網站權限

與其前身不同，新版 Microsoft Edge 對 Windows 安全性區域的使用非常有限。 相反地，透過 [原則](/deployedge/microsoft-edge-policies)為系統管理員提供每一網站設定的多數權限和功能，都依賴於  [URL 篩選格式](/DeployEdge/edge-learnmmore-url-list-filter%20format)中的規則清單。

當使用者開啟 <code>edge://settings/content/siteDetails?site=https://example.com</code>時，他們會找到一長串設定參數的清單和各種權限的清單。 使用者很少會直接使用設定頁面，而是在使用各種小工具瀏覽時進行選擇，並在 **頁面資訊** 下拉式清單 (當您按一下網址列中的鎖定圖示時會出現) 或透過網址列右側的各種提示或按鈕進行切換。

企業可以使用群組原則，來為控制瀏覽器行為的個別原則佈建網站清單。 若要尋找這些原則，只要開啟  [Microsoft Edge 群組原則文件](/deployedge/microsoft-edge-policies) 並搜尋 ForUrls **** ，即可尋找會根據所載入網站的 URL 來允許和封鎖行為的原則。 大部分相關設定會在 [內容設定的群組原則](/deployedge/microsoft-edge-policies#content-settings)區段中列出。

也有一些原則 (其名稱包含 **預設**) 可控制指定設定的預設行為。

許多設定非常模糊 (WebSerial、WebMIDI)，而且通常沒有理由變更預設值 (影像) 的設定。

## <a name="common-questions"></a>常見問題

## <a name="q-can-the-url-filter-format-match-on-a-sites-ip-address"></a>問：URL 篩選格式可比對網站的 IP 位址嗎？

否，格式不支援指定允許和封鎖清單的 IP 範圍。 它確實支援指定個別 IP  **常值**，但只有在使用者使用上述常值 (例如  <http://127.0.0.1/>) 瀏覽至網站時，才會考慮這類規則。 如果使用主機名稱 (<http://localhost>)，即使主機的解析 IP 符合篩選列出的 IP，也不會考慮 IP 常值規則。

## <a name="q-can-url-filters-matchjustdotless-host-names"></a>問：URL 篩選能夠僅比對無點的主機名稱嗎？

否。 您必須個別列出每個需要的主機名稱，例如 (`https://payroll`、`https://stock`、`https://who` 等)。

如果您足夠有前瞻性，而可以建立內部網路的結構，使得主機名稱格式為：

- <div style="display: inline">`https://payroll.contoso-intranet.com`</div>

- <div style="display: inline">`https://timecard.contoso-intranet.com`</div>

- <div style="display: inline">`https://sharepoint.contoso-intranet.com`</div>

恭喜！您已實作最佳作法。 您可以使用 ***.contoso-intranet.com** 項目來設定每個想要的原則，而您的整個內部網路將會加入。

## <a name="use-of-security-zones-inthe-microsoft-edge"></a>使用 Microsoft Edge 中的安全性區域

雖然 Microsoft Edge 主要仰賴於使用 URL 篩選格式的個別原則，但它預設會持續在少數位置使用 Windows 的安全性區域，以簡化過去仰賴區域設定的企業內部署。 下列行為是由區域原則控制：

1. 決定是否要自動釋出 Windows 整合式驗證 (Kerberos/NTLM) 認證時

2. 決定如何處理檔案下載時

3. 針對 Internet Explorer 模式

## <a name="credential-release"></a>釋出認證

依預設，Microsoft Edge 會評估 URLACTION_CREDENTIALS_USE 以決定是否自動使用 Windows 整合式驗證，或是使用者應該改為看到手動驗證提示。 設定 [AuthServerAllowlist 網站清單原則](/deployedge/microsoft-edge-policies#authserverallowlist)，將防止查閱區域原則。

## <a name="file-downloads"></a>檔案下載

從網際網路區域下載的檔案，會記錄其檔案下載來源的證據 (稱為[網路標記](https://textslashplain.com/2016/04/04/downloads-and-the-mark-of-the-web/))。 在決定如何處理檔案時，其他應用程式 (例如 Windows Shell、Microsoft Office 等) 可能會考慮此來源證據。

如果 Windows 安全性區域原則設定為停用「啟動應用程式及不安全的檔案」設定，Microsoft Edge 下載管理員將會封鎖來自該區域中網站的檔案下載，並加上備註：「無法下載 - 已封鎖」。  

## <a name="ie-mode"></a>IE 模式

IE 模式可設定為 [以 IE 模式開啟所有內部網路網站](/deployedge/edge-ie-mode#configure-all-intranet-sites)。 使用此設定時，Edge 會在決定是否應該在 IE 模式中開啟時評估 URL 的區域。 除了此初始決策之外，IE 模式索引標籤會實際執行 Internet Explorer，因此，其會評估每個原則決策的區域設定，正如同 Internet Explorer 本身所做的一般。

## <a name="summary"></a>摘要

在大部分情況下，可以將 Microsoft Edge 設定保留為其預設值。 想要變更所有網站或特定網站預設值的系統管理員，可以使用適當的群組原則來指定網站清單或預設行為。 在少數情況下 (認證釋出、檔案下載和 IE 模式)，系統管理員會透過設定 Windows 安全性區域設定，以繼續控制行為。
