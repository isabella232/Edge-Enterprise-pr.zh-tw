---
title: Microsoft Edge 和混合式內容下載
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 04/30/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 和混合式內容下載
ms.openlocfilehash: a81c44754865b2303320bfe87346c7f7533e6133
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617303"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a><span data-ttu-id="4d120-103">了解 Microsoft Edge 和混合式內容下載</span><span class="sxs-lookup"><span data-stu-id="4d120-103">Learn about Microsoft Edge and mixed content downloads</span></span>

<span data-ttu-id="4d120-104">本文說明混合式內容下載以及 Microsoft Edge 的處理方式。</span><span class="sxs-lookup"><span data-stu-id="4d120-104">This article explains mixed content downloads and how Microsoft Edge handles them.</span></span>

>[!NOTE]
><span data-ttu-id="4d120-105">本文適用於 Microsoft Edge 版本 85 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4d120-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="what-are-mixed-content-downloads"></a><span data-ttu-id="4d120-106">什麼是混合式內容下載？</span><span class="sxs-lookup"><span data-stu-id="4d120-106">What are mixed content downloads?</span></span>

<span data-ttu-id="4d120-107">當您從透過安全 HTTPS 連線載入的 HTML 頁面開始下載時，就會發生混合式內容下載，但有下列其中一種情況存在：</span><span class="sxs-lookup"><span data-stu-id="4d120-107">A mixed content download happens when you start a download from an HTML page that was loaded over a secure HTTPS connection, but one of the following conditions exists:</span></span>

- <span data-ttu-id="4d120-108">一或多個下載位置的重新導向是透過不安全的 HTTP 連線所載入。</span><span class="sxs-lookup"><span data-stu-id="4d120-108">One or more of the download location's redirects was loaded over an insecure HTTP connection.</span></span>
- <span data-ttu-id="4d120-109">最終的下載位置是透過不安全的 HTTP 連線所載入。</span><span class="sxs-lookup"><span data-stu-id="4d120-109">The final download location was loaded over an insecure HTTP connection.</span></span>

<span data-ttu-id="4d120-110">上述任一案例會因為使用安全的 HTTPS 來提出要求而成為混合式內容，而且 HTTP 與 HTTPS 內容均涉及最終下載目的地。</span><span class="sxs-lookup"><span data-stu-id="4d120-110">Either scenario is a mixed content because the request was made using secure HTTPS and both HTTP and HTTPS content are involved in reaching the final download destination.</span></span> <span data-ttu-id="4d120-111">新式瀏覽器會顯示有關此內容類型的警告，向使用者表明：即使存取的原始頁面很安全，也可能不安全地傳輸此下載。</span><span class="sxs-lookup"><span data-stu-id="4d120-111">Modern browsers display warnings about this type of content to indicate to the user that this download may be transferred insecurely even though the original page accessed was secure.</span></span>

## <a name="download-warnings-and-user-options"></a><span data-ttu-id="4d120-112">下載警告和使用者選項</span><span class="sxs-lookup"><span data-stu-id="4d120-112">Download warnings and user options</span></span>

<span data-ttu-id="4d120-113">下載警告可確保使用者知道正在下載的檔案可能會遭到網路上的惡意攻擊者讀取。</span><span class="sxs-lookup"><span data-stu-id="4d120-113">The download warning ensures that users know that the file they're downloading could be read by malicious attackers on their network.</span></span> <span data-ttu-id="4d120-114">此警告可讓使用者做出知情決策來決定是否下載檔案。</span><span class="sxs-lookup"><span data-stu-id="4d120-114">This warning lets a user make an informed decision on whether to download the file.</span></span>

<span data-ttu-id="4d120-115">在 Microsoft Edge 中，混合式內容下載會遭到封鎖，但是使用者可以視需要覆寫和下載檔案。</span><span class="sxs-lookup"><span data-stu-id="4d120-115">In Microsoft Edge, mixed content downloads will be blocked but users can override and download the file if they want to.</span></span> <span data-ttu-id="4d120-116">從 Microsoft Edge 版本 85 開始，Microsoft Edge 打算開始封鎖混合式內容的可執行檔下載，而在未來的版本中將會封鎖不同的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="4d120-116">Microsoft Edge plans on starting to block mixed content executable file downloads starting with Microsoft Edge version 85 and will block different filetypes in future releases.</span></span>

> [!NOTE]
> <span data-ttu-id="4d120-117">此功能的部署可能視發行排程和使用者意見反應而有所變動。</span><span class="sxs-lookup"><span data-stu-id="4d120-117">Deployment of this feature is subject to change based on release schedule and user feedback.</span></span>

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

<span data-ttu-id="4d120-118">在下載列中，封鎖警告訊息看起來就像下一個螢幕擷取畫面中的範例。</span><span class="sxs-lookup"><span data-stu-id="4d120-118">In the download shelf, the block warning message looks like the example in the next screenshot.</span></span>

 ![下載匣中的混合式內容警告](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

<span data-ttu-id="4d120-120">在下載頁面上，封鎖警告看起來就像以下螢幕擷取畫面範例：</span><span class="sxs-lookup"><span data-stu-id="4d120-120">On the download page, the block warning looks like the following screenshot example:</span></span>

 ![混合式內容覆寫提示](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

<span data-ttu-id="4d120-122">如果使用者決定要保留下載，系統會提示他們確認其動作。</span><span class="sxs-lookup"><span data-stu-id="4d120-122">If a user decides to keep the download, they are prompted to confirm their action.</span></span> <span data-ttu-id="4d120-123">下一個螢幕擷取畫面顯示此確認提示的範例。</span><span class="sxs-lookup"><span data-stu-id="4d120-123">The next screenshot shows an example of this confirmation prompt.</span></span>

 ![Internet Explorer 模式](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a><span data-ttu-id="4d120-125">支援原則</span><span class="sxs-lookup"><span data-stu-id="4d120-125">Supporting policies</span></span>

<span data-ttu-id="4d120-126">如果企業想要排除特定網站的混合式內容封鎖，可以使用 [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) 原則執行此操作。</span><span class="sxs-lookup"><span data-stu-id="4d120-126">Enterprises that want to exclude mixed content blocking from specific websites can use the [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) policy to do so.</span></span>

## <a name="content-license"></a><span data-ttu-id="4d120-127">內容授權</span><span class="sxs-lookup"><span data-stu-id="4d120-127">Content license</span></span>

> [!NOTE]
> <span data-ttu-id="4d120-128">本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。</span><span class="sxs-lookup"><span data-stu-id="4d120-128">Portions of this page are modifications based on work created and shared by Chromium.org and used according to terms described in the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).</span></span> <span data-ttu-id="4d120-129">原始頁面可在[此處](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content)找到。</span><span class="sxs-lookup"><span data-stu-id="4d120-129">The original page can be found [here](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content).</span></span>
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span data-ttu-id="4d120-130">本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。</span><span class="sxs-lookup"><span data-stu-id="4d120-130">This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d120-131">請參閱</span><span class="sxs-lookup"><span data-stu-id="4d120-131">See also</span></span>

- [<span data-ttu-id="4d120-132">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="4d120-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)