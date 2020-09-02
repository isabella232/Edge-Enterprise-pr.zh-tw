---
title: Microsoft Edge 安全性概觀
ms.author: srugh
author: srugh
manager: seanlyn
ms.date: 04/29/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 部署 Microsoft Edge 安全性的概觀
ms.openlocfilehash: f22f2dcbace00cd535d201950c2af488c708525b
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979616"
---
# <span data-ttu-id="9d911-103">Microsoft Edge 安全性概觀</span><span class="sxs-lookup"><span data-stu-id="9d911-103">Overview of Microsoft Edge security</span></span>
  
<span data-ttu-id="9d911-104">企業的 IT 管理員需保護企業網路和裝置免受惡意攻擊，並防止未經授權的存取和洩露公司資料，同時仍需面臨大量現有和新興的安全挑戰。</span><span class="sxs-lookup"><span data-stu-id="9d911-104">IT admins in the enterprise are constantly facing a myriad of existing and emerging security challenges while protecting the corporate network and devices from malicious attacks and preventing unauthorized access and leaks of corporate data.</span></span> <span data-ttu-id="9d911-105">Microsoft Edge 提供數種原生內建的獨特功能，可協助應對這些挑戰。</span><span class="sxs-lookup"><span data-stu-id="9d911-105">Microsoft Edge provides several natively built, unique capabilities that help address these challenges.</span></span>

> [!NOTE]
> <span data-ttu-id="9d911-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9d911-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="9d911-107">條件式存取</span><span class="sxs-lookup"><span data-stu-id="9d911-107">Conditional Access</span></span>

<span data-ttu-id="9d911-108">提到管理雲端資源時，雲端安全的一個關鍵面向是身分識別和存取權。</span><span class="sxs-lookup"><span data-stu-id="9d911-108">A key aspect of cloud security is identity and access when it comes to managing your cloud resources.</span></span> <span data-ttu-id="9d911-109">在行動優先、雲端優先的世界中，使用者可以從任何位置使用各種裝置和應用程式存取組織的資源。</span><span class="sxs-lookup"><span data-stu-id="9d911-109">In a mobile-first, cloud-first world, users can access your organization's resources using a variety of devices and apps from anywhere.</span></span> <span data-ttu-id="9d911-110">因此，僅關注何人可以存取資源是不夠的。</span><span class="sxs-lookup"><span data-stu-id="9d911-110">As a result of this, just focusing on who can access a resource is not sufficient.</span></span> <span data-ttu-id="9d911-111">您還需要考慮存取資源的方式。</span><span class="sxs-lookup"><span data-stu-id="9d911-111">You also need to factor in how a resource is accessed.</span></span> <span data-ttu-id="9d911-112">Azure Active Directory (Azure AD) 條件式存取可協助您掌握安全性和生產力之間的平衡。</span><span class="sxs-lookup"><span data-stu-id="9d911-112">Azure Active Directory (Azure AD) Conditional Access helps you master the balance between security and productivity.</span></span>

### <span data-ttu-id="9d911-113">在 Microsoft Edge 中存取受條件式存取保護的資源</span><span class="sxs-lookup"><span data-stu-id="9d911-113">Accessing Conditional Access protected resources in Microsoft Edge</span></span>

<span data-ttu-id="9d911-114">Microsoft Edge 原生支援 Azure AD 條件式存取。</span><span class="sxs-lookup"><span data-stu-id="9d911-114">Microsoft Edge natively supports Azure AD Conditional Access.</span></span> <span data-ttu-id="9d911-115">無需另外安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="9d911-115">There's no need to install a separate extension.</span></span> <span data-ttu-id="9d911-116">當您使用企業 Azure AD 認證登入 Microsoft Edge 設定檔時，Microsoft Edge 允許無縫存取受條件式存取保護的企業雲端資源。</span><span class="sxs-lookup"><span data-stu-id="9d911-116">When you're signed into a Microsoft Edge profile with enterprise Azure AD credentials, Microsoft Edge allows seamless access to enterprise cloud resources protected using Conditional Access.</span></span>

<span data-ttu-id="9d911-117">在相容裝置上，存取資源的身分識別應與設定檔上的身分識別相符。</span><span class="sxs-lookup"><span data-stu-id="9d911-117">On a compliant device, the identity accessing the resource should match the identity on the profile.</span></span>  <span data-ttu-id="9d911-118">否則，您會看到一則類似於下一個螢幕擷取畫面中顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="9d911-118">If it doesn't, you'll see a message like the one in the next screenshot.</span></span> <span data-ttu-id="9d911-119">在螢幕擷取畫面範例中，"testadmin@evostsoneboxtest.com" 是存取資源所需的登入帳戶。</span><span class="sxs-lookup"><span data-stu-id="9d911-119">In the screenshot example, "testadmin@evostsoneboxtest.com" is the sign-in account needed to access the resource.</span></span>

![瀏覽器中的條件式存取訊息](./media/edge-security/microsoft-edge-security-conditional-access.png)

<span data-ttu-id="9d911-121">若要繼續，您必須切換到所需的設定檔 (如果有) 或建立具有相符身分識別的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d911-121">To continue, you have to switch to the required profile (if you have one) or create a profile with matching identity.</span></span>

<span data-ttu-id="9d911-122">若要登入並使用您的設定檔，請按一下瀏覽器右上角的帳戶圖片。</span><span class="sxs-lookup"><span data-stu-id="9d911-122">To sign in and work with your profile, click the account picture in the top right corner of the browser.</span></span> <span data-ttu-id="9d911-123">您可以使用下拉式功能表來︰</span><span class="sxs-lookup"><span data-stu-id="9d911-123">You can use the dropdown menu to:</span></span>

- <span data-ttu-id="9d911-124">選取其他設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d911-124">Select another profile.</span></span> <span data-ttu-id="9d911-125">按一下設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9d911-125">Click the profile name.</span></span>
- <span data-ttu-id="9d911-126">建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d911-126">Create a profile.</span></span> <span data-ttu-id="9d911-127">按一下**新增設定檔**。</span><span class="sxs-lookup"><span data-stu-id="9d911-127">Click **Add a profile**.</span></span>
- <span data-ttu-id="9d911-128">管理您的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9d911-128">Manage your profiles.</span></span> <span data-ttu-id="9d911-129">按一下**管理設定檔設定**。</span><span class="sxs-lookup"><span data-stu-id="9d911-129">Click **Manage profile settings**.</span></span>

<span data-ttu-id="9d911-130">此支援適用於所有平台，包括所有受支援的 Windows 和 macOS 版本。</span><span class="sxs-lookup"><span data-stu-id="9d911-130">This support is available across all platforms, including all supported versions of Windows and macOS.</span></span>

### <span data-ttu-id="9d911-131">如何在 Azure Active Directory 中部署條件式存取</span><span class="sxs-lookup"><span data-stu-id="9d911-131">How to deploy Conditional Access in Azure Active Directory</span></span>

<span data-ttu-id="9d911-132">[部署條件式存取](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access)提供可協助在 Azure Active Directory 中部署條件式存取的詳細指南。</span><span class="sxs-lookup"><span data-stu-id="9d911-132">[Deploy Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/plan-conditional-access) provides a detailed guide to help deploy Conditional Access in Azure Active Directory.</span></span>

## <span data-ttu-id="9d911-133">請參閱</span><span class="sxs-lookup"><span data-stu-id="9d911-133">See also</span></span>

- [<span data-ttu-id="9d911-134">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="9d911-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="9d911-135">影片：安全性、相容性及管理性</span><span class="sxs-lookup"><span data-stu-id="9d911-135">Video: Security, compatibility, and manageability</span></span>](/microsoft-edge-video-security-compatibility-manageability.md)
