---
title: 企業新索引標籤頁的回溯相容性
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 企業新索引標籤頁的回溯相容性
ms.openlocfilehash: e2534f9df82aa81843d7cd292ada99a4c7574a3c
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642079"
---
# <a name="backwards-compatibility-for-the-enterprise-new-tab-page"></a>企業新索引標籤頁的回溯相容性

本文將說明 [新索引標籤頁面] 的變更，以及使用者可以與 Microsoft Edge 版本 87 及更舊版本回溯相容的方式。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 87 或更新版本。

## <a name="information-feeds-from-single-endpoint"></a>來自單一端點的資訊摘要

新版 [企業新索引標籤頁] 結合了透過 MSN.com 端點所提供之符合產業相關規範的 Microsoft 365 內容，以及相容的資訊摘要。

> [!NOTE]
> Office 365 內容最開始使用 [Office.com](https://www.office.com) 網域所提供。

如果貴組織限制存取 MSN.com 網域，強烈建議您給予使用者此 [URL](https://ntp.msn.com) 的存取權。

如果您需要更多時間來啟用 MSN 網域的存取，我們建議您使用 [NewTabPageSetFeedType](./microsoft-edge-policies.md#newtabpagesetfeedtype)，讓您為新的索引標籤頁面選擇 Microsoft News 或 Office 365 摘要體驗。

### <a name="keep-using-officecom"></a>繼續使用 Office.com

 您可以設定 **NewTabPageSetFeedType** 原則，以繼續使用已取代的 Office.com 網域。

> [!IMPORTANT]
> 在 Microsoft Edge 版本 90 發行後，Office 365 所用的 **NewTabPageSetFeedType** 原則和 Office.com 網域將會停止運作。

下列原則設定會強制 [企業新索引標籤頁] 轉譯來自 Office.com 網域的 Office 文件內容。

- 將原則設定為 **[強制]**。
- 將原則對應的值設定為 **Office (1) = Office 365 摘要體驗**。

如果無法切換為 Office.com，請與我們連絡並傳送意見反應。 您也可以設定 [NewTabPageLocation](./microsoft-edge-policies.md#newtabpagelocation)，讓它指向貴組織所允許的端點 URL。

> [!NOTE]
> 如果同時設定 **NewTabPageSetFeedType** 原則，則 **NewTabPageLocation** 有優先順序。

## <a name="enterprise-users-will-now-get-microsoft-news-content-via-my-feed"></a>企業使用者現在將可透過 [我的摘要] 取得 Microsoft 新聞內容

[企業新索引標籤頁] 將針對使用其 Azure Active Directory (Azure AD) 帳戶登入的使用者，以單一檢視的模式在 **[我的摘要]** 和 Office 365 內容中提供業界相關資訊。 針對以其 Azure Active Directory (Azure AD) 登入且在設定飛出視窗中選取 [Microsoft News] 選項的使用者，其新索引標籤頁面檢視會以 **[我的摘要]** 內容取代。 當他們在瀏覽器中開啟新索引標籤頁面時，頁面看起來就會像下一個螢幕擷取畫面中的範例。

![顯示來自 [我的摘要] 內容的新索引標籤頁面。](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> 未使用 Azure AD 登入的使用者，會在開啟新索引標籤時繼續看到 MSN 新聞摘要。

## <a name="page-layout"></a>頁面配置

當您變更了 [新索引標籤頁面]，[頁面配置] 便不需要再控制兩種特定的內容類型 (Office 365 與 Microsoft News)，因此無法使用內容切換。 下個螢幕擷取畫面顯示 [頁面配置] 的飛出視窗。

![[新索引標籤頁面] 的 [頁面配置] 檢視。](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

如果您想繼續存取與貴組織不相關的 Microsoft News 內容，則必須使用不同的瀏覽器設定檔。 移至  *edge://settings/profiles* 並登出您的 Azure AD 設定檔。 此動作會顯示 [企業新索引標籤頁] 的標準檢視。 

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Internet Explorer 11 的企業模式](/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)