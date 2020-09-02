---
title: 在 Internet Explorer 模式中保留頁面內瀏覽
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 05/01/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 在 Internet Explorer 模式中保留頁面內瀏覽
ms.openlocfilehash: 0acca9e05a0d09b02fa61d5ddd7de3f7c6cabb92
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979532"
---
# <span data-ttu-id="88990-103">在 Internet Explorer 模式中保留頁面內瀏覽</span><span class="sxs-lookup"><span data-stu-id="88990-103">Keep in-page navigation in Internet Explorer mode</span></span>

<span data-ttu-id="88990-104">您可以使用此原則做為臨時解決方案，強制來自 Internet Explorer 模式 (IE 模式) 網站的所有頁面內瀏覽，以維持使用 IE 模式。</span><span class="sxs-lookup"><span data-stu-id="88990-104">You can use this policy as a temporary solution to force all in-page navigation from Internet Explorer mode (IE mode) sites to stay in IE mode.</span></span>

<span data-ttu-id="88990-105">頁面內瀏覽是從連結、指令碼或目前頁面上的表單開始。</span><span class="sxs-lookup"><span data-stu-id="88990-105">An in-page navigation is started from a link, a script, or a form on the current page.</span></span> <span data-ttu-id="88990-106">也可以是先前頁面內瀏覽嘗試的伺服器端重新導向。</span><span class="sxs-lookup"><span data-stu-id="88990-106">It can also be a server-side redirect of a previous in-page navigation attempt.</span></span> <span data-ttu-id="88990-107">相反地，使用者可以使用瀏覽器控制項以多種方式啟動不在頁面內且獨立於目前頁面的瀏覽。</span><span class="sxs-lookup"><span data-stu-id="88990-107">Conversely, a user can start a navigation that isn't in-page that's independent of the current page in several ways by using the browser controls.</span></span> <span data-ttu-id="88990-108">例如，使用網址列、[返回] 按鈕或 [我的最愛] 連結。</span><span class="sxs-lookup"><span data-stu-id="88990-108">For example, using the address bar, the back button, or a favorite link.</span></span>

>[!NOTE]
><span data-ttu-id="88990-109">本文適用於 Microsoft Edge 版本 81 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="88990-109">This article applies to Microsoft Edge version 81 or later.</span></span>

## <span data-ttu-id="88990-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="88990-110">Prerequisites</span></span>

<span data-ttu-id="88990-111">此原則需要下列 Windows 更新：</span><span class="sxs-lookup"><span data-stu-id="88990-111">The following Windows updates are required for this policy:</span></span>

- <span data-ttu-id="88990-112">Windows 10 版本 1909 & 1903、Windows Server 版本 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span><span class="sxs-lookup"><span data-stu-id="88990-112">Windows 10 version 1909 & 1903, Windows Server version 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))</span></span>
- <span data-ttu-id="88990-113">Windows 10 版本 1809、Windows Server 版本 1809、Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span><span class="sxs-lookup"><span data-stu-id="88990-113">Windows 10 version 1809, Windows Server version 1809, Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))</span></span>
- <span data-ttu-id="88990-114">Windows 10 版本 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span><span class="sxs-lookup"><span data-stu-id="88990-114">Windows 10 version 1803 ([KB4534308](https://support.microsoft.com/help/4534308))</span></span>
- <span data-ttu-id="88990-115">Windows 10 版本 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span><span class="sxs-lookup"><span data-stu-id="88990-115">Windows 10 version 1709 ([KB4534318](https://support.microsoft.com/help/4534318))</span></span>


## <span data-ttu-id="88990-116">關於此原則</span><span class="sxs-lookup"><span data-stu-id="88990-116">About this policy</span></span>

<span data-ttu-id="88990-117">此原則能讓您有時間識別和設定 IE 模式網站使用的所有驗證伺服器。</span><span class="sxs-lookup"><span data-stu-id="88990-117">This policy gives you time to identify and configure all of the authentication servers used by your IE mode sites.</span></span> <span data-ttu-id="88990-118">不過，此原則可能會造成不一致的瀏覽體驗，而有些網站會在 IE 模式中轉譯，而有時候則以 Microsoft Edge 模式轉譯。</span><span class="sxs-lookup"><span data-stu-id="88990-118">However, this policy can result in an inconsistent browsing experience, where some sites are rendered in IE mode and at other times rendered in Microsoft Edge mode.</span></span> <span data-ttu-id="88990-119">這取決於網站是否從 IE 模式頁面開始瀏覽。</span><span class="sxs-lookup"><span data-stu-id="88990-119">This experience depends on whether the navigation to the site began from an IE mode page.</span></span> <span data-ttu-id="88990-120">任何未明確設定為在特定轉譯引擎開啟的網站都會受到此不一致的限制。</span><span class="sxs-lookup"><span data-stu-id="88990-120">Any site that isn't explicitly configured to open in a specific rendering engine will be subject to this inconsistency.</span></span>

<span data-ttu-id="88990-121">如果您啟用這個原則，我們建議您在識別所有驗證伺服器後將它停用，並將它們新增到網站清單以設為中性。</span><span class="sxs-lookup"><span data-stu-id="88990-121">If you enable this policy, we recommend that you disable it after you've identified all the authentication servers and added them to the site list as neutral.</span></span> <span data-ttu-id="88990-122">此動作可確保您的新式網站永遠不會在 IE 模式中意外轉譯。</span><span class="sxs-lookup"><span data-stu-id="88990-122">This action ensures that your modern sites never inadvertently render in IE mode.</span></span>

## <span data-ttu-id="88990-123">在 IE 模式中保持頁面內瀏覽</span><span class="sxs-lookup"><span data-stu-id="88990-123">Keep in-page navigation in IE mode</span></span>

<span data-ttu-id="88990-124">若要在 Internet Explorer 模式中保持自動或所有頁面內瀏覽，請按照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="88990-124">To keep automatic or all in-page navigation in Internet Explorer mode, follow these steps:</span></span>

1. <span data-ttu-id="88990-125">開啟 [本機群組原則編輯器]。</span><span class="sxs-lookup"><span data-stu-id="88990-125">Open Local Group Policy Editor.</span></span>
2. <span data-ttu-id="88990-126">按一下**電腦組態** > **系統管理範本** > **Microsoft Edge**。</span><span class="sxs-lookup"><span data-stu-id="88990-126">Click **Computer Configuration** > **Administrative Templates** > **Microsoft Edge**.</span></span>
3. <span data-ttu-id="88990-127">在 [設定]\*\*\*\* 底下，按兩下 [指定從 Internet Explorer 模式頁面啟動時，未設定網站的「頁面內」瀏覽方式]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="88990-127">Under **Setting**, double-click **Specify how "in-page" navigations to unconfigured sites behave when started from Internet Explorer mode pages**.</span></span>

   ![頁面內原則設定](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. <span data-ttu-id="88990-129">選取 [已啟用]\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="88990-129">Select **Enabled**</span></span> 

   ![啟用頁面內原則](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. <span data-ttu-id="88990-131">從下拉式清單中選擇下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="88990-131">Choose one of the following options from the dropdown list:</span></span>

   - <span data-ttu-id="88990-132">**預設** - 只有設定以 Internet Explorer 模式開啟的網站才會以該模式開啟。</span><span class="sxs-lookup"><span data-stu-id="88990-132">**Default** - Only sites configured to open in Internet Explorer mode will open in that mode.</span></span> <span data-ttu-id="88990-133">任何未設定以 Internet Explorer 模式開啟的網站都將被重新導向回 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="88990-133">Any site not configured to open in Internet Explorer mode will be redirected back to Microsoft Edge.</span></span>
   - <span data-ttu-id="88990-134">**僅保持 Internet Explorer 模式中的自動瀏覽功能** - 如果您想要預設體驗，請使用此選項，除了所有自動瀏覽 (例如 302 重新導向) 到未設定的網站以外，都會保持 Internet Explorer 模式。</span><span class="sxs-lookup"><span data-stu-id="88990-134">**Keep only automatic navigations in Internet Explorer mode** - Use this option if you want the default experience except that all automatic navigations (such as 302 redirects) to unconfigured sites will be kept in Internet Explorer mode.</span></span>
   - <span data-ttu-id="88990-135">**讓所有頁面內瀏覽保持在 Internet Explorer 模式** ***(最不建議)*** - 從 IE 模式載入到未設定網站之頁面的所有瀏覽，都會保持在 Internet Explorer 模式中。</span><span class="sxs-lookup"><span data-stu-id="88990-135">**Keep all in-page navigation in Internet Explorer mode** ***(Least Recommended)*** - All navigations from pages loaded in IE mode to unconfigured sites are kept in Internet Explorer mode.</span></span>

6. <span data-ttu-id="88990-136">按一下 [確定]\*\*\*\* 或 [套用]\*\*\*\* 儲存此原則設定。</span><span class="sxs-lookup"><span data-stu-id="88990-136">Click **OK** or **Apply** to save the policy settings.</span></span>

## <span data-ttu-id="88990-137">請參閱</span><span class="sxs-lookup"><span data-stu-id="88990-137">See also</span></span>

- [<span data-ttu-id="88990-138">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="88990-138">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
