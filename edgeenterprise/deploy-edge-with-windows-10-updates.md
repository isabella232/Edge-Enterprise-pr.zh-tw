---
title: 使用 Windows 10 更新部署 Microsoft Edge
ms.author: ryhecht
author: RyanHechtMSFT
manager: tinad
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 使用 Windows 10 更新部署 Microsoft Edge
ms.openlocfilehash: 9102ef37c6a5329a5cba79ed976237d7fd7e2063
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641889"
---
# <a name="deploy-microsoft-edge-with-windows-10-updates"></a><span data-ttu-id="f5a0b-103">使用 Windows 10 更新部署 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f5a0b-103">Deploy Microsoft Edge with Windows 10 updates</span></span>

<span data-ttu-id="f5a0b-104">本文為使用 Windows 10 更新部署 Microsoft Edge 的使用者提供相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-104">The article provides information for users who are deploying Microsoft Edge by using Windows 10 updates.</span></span>

## <a name="for-windows-10-release-20h2"></a><span data-ttu-id="f5a0b-105">針對 Windows 10 版本 20H2</span><span class="sxs-lookup"><span data-stu-id="f5a0b-105">For Windows 10 release 20H2</span></span>

<span data-ttu-id="f5a0b-106">Windows 10 版本 20H2 已安裝 Microsoft Edge 做為其預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-106">Windows 10 version 20H2 already has Microsoft Edge installed as its default browser.</span></span>

## <a name="for-windows-10-releases-rs4-through-20h1"></a><span data-ttu-id="f5a0b-107">Windows 10 版本 RS4 至 20H1</span><span class="sxs-lookup"><span data-stu-id="f5a0b-107">For Windows 10 releases RS4 through 20H1</span></span>

<span data-ttu-id="f5a0b-108">Windows Server Update Services (WSUS) 中具有 Windows 10 從 RS4 至 20H1 的每個版本更新，將會移除舊版 Microsoft Edge 桌面應用程式，並以 Microsoft Edge 取代它。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-108">Windows Server Update Services (WSUS) has updates for each version of Windows 10 from RS4 through 20H1 that will remove the Microsoft Edge Legacy desktop app and replace it with Microsoft Edge.</span></span> <span data-ttu-id="f5a0b-109">如需詳細資訊，請參閱[此支援文章](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c)，了解哪些 WSUS 更新適合您的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-109">For more information, see [this support article](https://support.microsoft.com/topic/update-in-wsus-for-the-new-microsoft-edge-for-windows-10-version-1809-1903-1909-and-2004-october-29-2020-b4980418-4ec4-dee7-3b17-1c6499bd127c) to find out which WSUS update is right for your Windows version.</span></span>

## <a name="for-windows-10-releases-prior-to-rs4-and-windows-7-81-and-earlier"></a><span data-ttu-id="f5a0b-110">針對早於 RS4 的 Windows 10 版本 (和 Windows 7、8.1 和更早版本)</span><span class="sxs-lookup"><span data-stu-id="f5a0b-110">For Windows 10 releases prior to RS4 (and Windows 7, 8.1, and earlier)</span></span>

<span data-ttu-id="f5a0b-111">這些版本無法透過 Windows Update 來安裝 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-111">Windows updates to install Microsoft Edge aren't available for these versions.</span></span> <span data-ttu-id="f5a0b-112">請考慮將 Microsoft Edge 部署至這些裝置的其他選項，例如 [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) 或 [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json)。</span><span class="sxs-lookup"><span data-stu-id="f5a0b-112">Consider other options for deploying Microsoft Edge to these devices such as [Configuration Manager](/configmgr/apps/deploy-use/deploy-edge?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json) or [Intune](/intune/apps/apps-windows-edge/?bc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2fbreadcrumb%2ftoc.json&toc=https%3a%2f%2fdocs.microsoft.com%2fDeployEdge%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5a0b-113">請參閱</span><span class="sxs-lookup"><span data-stu-id="f5a0b-113">See also</span></span>

- [<span data-ttu-id="f5a0b-114">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f5a0b-114">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f5a0b-115">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="f5a0b-115">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)