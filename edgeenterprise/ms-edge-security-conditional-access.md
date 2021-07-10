---
title: Microsoft Edge 和條件式存取
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 和條件式存取
ms.openlocfilehash: 27d93627f8a86ad821a00d6d78b7db352e9e557a
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642849"
---
# <a name="microsoft-edge-and-conditional-access"></a><span data-ttu-id="8d8bb-103">Microsoft Edge 和條件式存取</span><span class="sxs-lookup"><span data-stu-id="8d8bb-103">Microsoft Edge and Conditional Access</span></span>
  
<span data-ttu-id="8d8bb-104">本文將說明 Microsoft Edge 如何支援條件式存取，並說明如何存取由條件存取保護的資源。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-104">This article describes how Microsoft Edge supports Conditional Access, and how to access resources protected by Conditional Access.</span></span>

> [!NOTE]
> <span data-ttu-id="8d8bb-105">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-105">This article applies to Microsoft Edge version 77 or later.</span></span>

<span data-ttu-id="8d8bb-106">提到管理雲端資源時，雲端安全的一個關鍵面向是身分識別和存取權。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-106">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="8d8bb-107">在行動優先、雲端優先的世界中，使用者可以從任何位置使用各種裝置和應用程式存取組織的資源。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-107">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="8d8bb-108">因此，僅關注何人可以存取資源是不夠的。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-108">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="8d8bb-109">您還需要考慮存取資源的方式。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-109">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="8d8bb-110">Azure Active Directory (Azure AD) 條件式存取可協助您掌握安全性和生產力之間的平衡。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-110">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

## <a name="accessing-conditional-access-protected-resources-in-microsoft-edge"></a><span data-ttu-id="8d8bb-111">在 Microsoft Edge 中存取受條件式存取保護的資源</span><span class="sxs-lookup"><span data-stu-id="8d8bb-111">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="8d8bb-112">Microsoft Edge 原生支援 Azure AD 條件式存取。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-112">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="8d8bb-113">無需另外安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-113">There's no need to install a separate extension.</span></span> <span data-ttu-id="8d8bb-114">當您使用企業 Azure AD 認證登入 Microsoft Edge 設定檔時，Microsoft Edge 允許無縫存取受條件式存取保護的企業雲端資源。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-114">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="8d8bb-115">在相容裝置上，存取資源的身分識別應與設定檔上的身分識別相符。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-115">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="8d8bb-116">否則，您會看到一則類似於下一個螢幕擷取畫面中顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-116">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="8d8bb-117">在螢幕擷取畫面範例中，"testadmin@evostsoneboxtest.com" 是存取資源所需的登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-117">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![瀏覽器中的條件式存取訊息](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="8d8bb-119">若要繼續，您必須切換到所需的設定檔 (如果有) 或建立具有相符身分識別的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-119">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="8d8bb-120">若要登入並使用您的設定檔，請按一下瀏覽器右上角的帳戶圖片。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-120">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="8d8bb-121">您可以使用下拉式功能表來︰</span><span class="sxs-lookup"><span data-stu-id="8d8bb-121">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="8d8bb-122">選取其他設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-122">Select another profile.</span></span> <span data-ttu-id="8d8bb-123">按一下設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-123">Click the profile name.</span></span>
- <span data-ttu-id="8d8bb-124">建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-124">Create a profile.</span></span> <span data-ttu-id="8d8bb-125">按一下**新增設定檔**。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-125">Click **Add a profile**.</span></span>
- <span data-ttu-id="8d8bb-126">管理您的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-126">Manage your profiles.</span></span> <span data-ttu-id="8d8bb-127">按一下**管理設定檔設定**。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-127">Click **Manage profile settings**.</span></span>

<span data-ttu-id="8d8bb-128">此支援適用於所有平台，包括所有受支援的 Windows 和 macOS 版本。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-128">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <a name="how-to-deploy-conditional-access-in-azure-active-directory"></a><span data-ttu-id="8d8bb-129">如何在 Azure Active Directory 中部署條件式存取</span><span class="sxs-lookup"><span data-stu-id="8d8bb-129">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="8d8bb-130">[部署條件式存取](/azure/active-directory/conditional-access/plan-conditional-access)提供可協助在 Azure Active Directory 中部署條件式存取的詳細指南。</span><span class="sxs-lookup"><span data-stu-id="8d8bb-130">[Deploy Conditional Access](/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d8bb-131">請參閱</span><span class="sxs-lookup"><span data-stu-id="8d8bb-131">See also</span></span>

- [<span data-ttu-id="8d8bb-132">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="8d8bb-132">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="8d8bb-133">影片：安全性、相容性及管理性</span><span class="sxs-lookup"><span data-stu-id="8d8bb-133">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)