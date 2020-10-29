---
title: 企業新索引標籤頁的回溯相容性
ms.author: ruchir
author: dan-wesley
manager: vwehren
ms.date: 10/28/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 企業新索引標籤頁的回溯相容性
ms.openlocfilehash: c10671a6ec8e1ff4dcb0db3f3c085f82ae973122
ms.sourcegitcommit: af6ab070d0c09bca4a9cf505b107ed7e04839763
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/29/2020
ms.locfileid: "11144473"
---
# <span data-ttu-id="fb680-103">企業新索引標籤頁的回溯相容性</span><span class="sxs-lookup"><span data-stu-id="fb680-103">Backwards compatibility for the Enterprise New tab page</span></span>

<span data-ttu-id="fb680-104">本文將說明 [新索引標籤頁面] 的變更，以及使用者可以與 Microsoft Edge 版本 87 及更舊版本回溯相容的方式。</span><span class="sxs-lookup"><span data-stu-id="fb680-104">This article describes the change to the New tab page and how users can be backwards compatible with Microsoft Edge version 87 and earlier.</span></span>

> [!NOTE]
> <span data-ttu-id="fb680-105">本文適用於 Microsoft Edge 版本 87 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fb680-105">This article applies to Microsoft Edge version 87 or later.</span></span>

## <span data-ttu-id="fb680-106">來自單一端點的資訊摘要</span><span class="sxs-lookup"><span data-stu-id="fb680-106">Information feeds from single endpoint</span></span>

<span data-ttu-id="fb680-107">新版 [企業新索引標籤頁] 結合了透過 MSN.com 端點所提供之符合產業相關規範的 Microsoft 365 內容，以及相容的資訊摘要。</span><span class="sxs-lookup"><span data-stu-id="fb680-107">The new version of the Enterprise New tab page combines compliant Microsoft 365 content with industry relevant and compliant information feeds that are served via the MSN.com endpoint.</span></span>

> [!NOTE]
> <span data-ttu-id="fb680-108">Office 365 內容最開始使用 [Office.com](https://www.office.com) 網域所提供。</span><span class="sxs-lookup"><span data-stu-id="fb680-108">Office 365 content was originally served using the [Office.com](https://www.office.com) domain.</span></span>

<span data-ttu-id="fb680-109">如果貴組織限制存取 MSN.com 網域，強烈建議您給予使用者此 [URL](https://ntp.msn.com) 的存取權。</span><span class="sxs-lookup"><span data-stu-id="fb680-109">If access to the MSN.com domain is restricted for your organization, we strongly recommend giving users access to this [url](https://ntp.msn.com).</span></span>

<span data-ttu-id="fb680-110">如果您需要更多時間來啟用 MSN 網域的存取，我們建議您使用 [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype)，讓您為新的索引標籤頁面選擇 Microsoft News 或 Office 365 摘要體驗。</span><span class="sxs-lookup"><span data-stu-id="fb680-110">If you need more time to enable access to the MSN domain, we recommend using the [NewTabPageSetFeedType](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagesetfeedtype), that lets you choose either the Microsoft News or Office 365 feed experience for the new tab page.</span></span>

### <span data-ttu-id="fb680-111">繼續使用 Office.com</span><span class="sxs-lookup"><span data-stu-id="fb680-111">Keep using Office.com</span></span>

 <span data-ttu-id="fb680-112">您可以設定 **NewTabPageSetFeedType** 原則，以繼續使用已取代的 Office.com 網域。</span><span class="sxs-lookup"><span data-stu-id="fb680-112">You can configure the **NewTabPageSetFeedType** policy to keep using the deprecated Office.com domain.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb680-113">在 Microsoft Edge 版本 90 發行後，Office 365 所用的 **NewTabPageSetFeedType** 原則和 Office.com 網域將會停止運作。</span><span class="sxs-lookup"><span data-stu-id="fb680-113">The **NewTabPageSetFeedType** policy and the Office.com domain that serves Office 365 content will quit working when Microsoft Edge version 90 is released.</span></span>

<span data-ttu-id="fb680-114">下列原則設定會強制 [企業新索引標籤頁] 轉譯來自 Office.com 網域的 Office 文件內容。</span><span class="sxs-lookup"><span data-stu-id="fb680-114">The following policy settings will force the Enterprise New tab page to render Office document content from the Office.com domain.</span></span>

- <span data-ttu-id="fb680-115">將原則設定為 **[強制]**。</span><span class="sxs-lookup"><span data-stu-id="fb680-115">Set the policy as **Mandatory**.</span></span>
- <span data-ttu-id="fb680-116">將原則對應的值設定為 **Office (1) = Office 365 摘要體驗**。</span><span class="sxs-lookup"><span data-stu-id="fb680-116">Set the value of the policy mapping to **Office (1) = Office 365 feed experience**.</span></span>

<span data-ttu-id="fb680-117">如果無法切換為 Office.com，請與我們連絡並傳送意見反應。</span><span class="sxs-lookup"><span data-stu-id="fb680-117">If the switch to the Office.com isn't possible, reach out and send us feedback.</span></span> <span data-ttu-id="fb680-118">您也可以設定 [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation)，讓它指向貴組織所允許的端點 URL。</span><span class="sxs-lookup"><span data-stu-id="fb680-118">Another option is to configure the [NewTabPageLocation](https://docs.microsoft.com/deployedge/microsoft-edge-policies#newtabpagelocation) so it points to an endpoint URL that's allowed by your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="fb680-119">如果同時設定 **NewTabPageSetFeedType** 原則，則 **NewTabPageLocation** 有優先順序。</span><span class="sxs-lookup"><span data-stu-id="fb680-119">The **NewTabPageLocation** policy has precedence if the **NewTabPageSetFeedType** policy is also configured.</span></span>

## <span data-ttu-id="fb680-120">企業使用者現在將可透過 [我的摘要] 取得 Microsoft 新聞內容</span><span class="sxs-lookup"><span data-stu-id="fb680-120">Enterprise users will now get Microsoft news content via My Feed</span></span>

<span data-ttu-id="fb680-121">[企業新索引標籤頁] 將針對使用其 Azure Active Directory (Azure AD) 帳戶登入的使用者，以單一檢視的模式在 **[我的摘要]** 和 Office 365 內容中提供業界相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fb680-121">The Enterprise New tab page will offer industry relevant information in **My Feed** and Office 365 content in a single view for users signed in with their Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="fb680-122">針對以其 Azure Active Directory (Azure AD) 登入且在設定飛出視窗中選取 [Microsoft News] 選項的使用者，其新索引標籤頁面檢視會以 **[我的摘要]** 內容取代。</span><span class="sxs-lookup"><span data-stu-id="fb680-122">For users signed in with their Azure Active Directory (Azure AD) who selected the Microsoft News option in the settings flyout, their new tab page view will be replaced with **My Feed** content.</span></span> <span data-ttu-id="fb680-123">當他們在瀏覽器中開啟新索引標籤頁面時，頁面看起來就會像下一個螢幕擷取畫面中的範例。</span><span class="sxs-lookup"><span data-stu-id="fb680-123">When they open a new tab page in the browser it will look like the example in the next screenshot.</span></span>

![顯示來自 [我的摘要] 內容的新索引標籤頁面。](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-myfeed-view.png)

> [!NOTE]
> <span data-ttu-id="fb680-125">未使用 Azure AD 登入的使用者，會在開啟新索引標籤時繼續看到 MSN 新聞摘要。</span><span class="sxs-lookup"><span data-stu-id="fb680-125">Users who aren't signed in with Azure AD will continue to see the MSN News feed when they open a new tab.</span></span>

## <span data-ttu-id="fb680-126">頁面配置</span><span class="sxs-lookup"><span data-stu-id="fb680-126">Page layout</span></span>

<span data-ttu-id="fb680-127">當您變更了 [新索引標籤頁面]，[頁面配置] 便不需要再控制兩種特定的內容類型 (Office 365 與 Microsoft News)，因此無法使用內容切換。</span><span class="sxs-lookup"><span data-stu-id="fb680-127">With the changes to the New tab page, the Page layout no longer has to control two specific content types (Office 365 and Microsoft News), so the content toggle isn't available.</span></span> <span data-ttu-id="fb680-128">下個螢幕擷取畫面顯示 [頁面配置] 的飛出視窗。</span><span class="sxs-lookup"><span data-stu-id="fb680-128">The next screenshot shows the flyout for the Page layout.</span></span>

![[新索引標籤頁面] 的 [頁面配置] 檢視。](media/microsoft-edge-ntp-backward-compatibility/microsoft-edge-ntp-page-layout.png)

<span data-ttu-id="fb680-130">如果您想繼續存取與貴組織不相關的 Microsoft News 內容，則必須使用不同的瀏覽器設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb680-130">If you want to keep accessing Microsoft News content that isn't tied to your organization, you must use a different browser profile.</span></span> <span data-ttu-id="fb680-131">移至  *edge://settings/profiles* 並登出您的 Azure AD 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb680-131">Go to  *edge://settings/profiles* and sign out of your Azure AD profile.</span></span> <span data-ttu-id="fb680-132">此動作會顯示 [企業新索引標籤頁] 的標準檢視。</span><span class="sxs-lookup"><span data-stu-id="fb680-132">This action will bring up the  standard view for the Enterprise new tab page.</span></span> 

## <span data-ttu-id="fb680-133">請參閱</span><span class="sxs-lookup"><span data-stu-id="fb680-133">See also</span></span>

- [<span data-ttu-id="fb680-134">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="fb680-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="fb680-135">Internet Explorer 11 的企業模式</span><span class="sxs-lookup"><span data-stu-id="fb680-135">Enterprise Mode for Internet Explorer 11</span></span>](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
