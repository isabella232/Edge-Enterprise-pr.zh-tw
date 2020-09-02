---
title: Microsoft Edge kiosk 模式
ms.author: brianalt
author: brianalt
manager: seanlynd
ms.date: 01/16/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge kiosk 模式
ms.openlocfilehash: 7a690820752b5361349bf394055a737bd8175215
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979600"
---
# <span data-ttu-id="6d8f1-103">Microsoft Edge kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="6d8f1-103">Microsoft Edge kiosk mode</span></span>

<span data-ttu-id="6d8f1-104">本文概述 Microsoft Edge (版本 77 或更新版本) kiosk 模式選項。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-104">This article provides an overview of the Microsoft Edge (version 77 or later) kiosk mode options.</span></span> <span data-ttu-id="6d8f1-105">同時也涵蓋繼續使用 Microsoft Edge 舊版 kiosk 模式 (版本 45 和較舊版本) 所需具備的條件。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-105">It also covers what's required to continue using Microsoft Edge Legacy kiosk mode (version 45 and earlier.)</span></span>

<span data-ttu-id="6d8f1-106">如需 Microsoft Edge 舊版 kiosk 模式 (版本 45 和較舊版本) 的相關資訊，請參閱[部署 Microsoft Edge kiosk 模式](https://aka.ms/edgekioskmode)。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-106">For information about Microsoft Edge Legacy kiosk mode (version 45 and earlier) see [Deploy Microsoft Edge kiosk mode](https://aka.ms/edgekioskmode).</span></span>

## <span data-ttu-id="6d8f1-107">具有受指派的存取權的 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6d8f1-107">Microsoft Edge with assigned access</span></span>

<span data-ttu-id="6d8f1-108">Microsoft Edge 可以在 Windows 10 上以[多應用程式受指派的存取權](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)執行，這相當於 Microsoft Edge 舊版「正常瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-108">Microsoft Edge can be run with [multi-app assigned access](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps) on Windows 10, which is the equivalent of Microsoft Edge Legacy "Normal browsing” kiosk mode type.</span></span> <span data-ttu-id="6d8f1-109">若要設定具有多應用程式受指派存取權的 Microsoft Edge，請按照如何[設定多個應用程式 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps)中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-109">To configure Microsoft Edge with multi-app assigned access follow the instructions on how to [Set up a multi-app kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-to-specific-apps).</span></span> <span data-ttu-id="6d8f1-110">Microsoft Edge Stable 通道的 AUMID 是 **MSEdge**。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-110">The AUMID for the Microsoft Edge Stable channel is **MSEdge**.</span></span>

<span data-ttu-id="6d8f1-111">使用具有受指派的存取權的 Microsoft Edge 時，您可以使用 [Microsoft Edge 瀏覽器原則](microsoft-edge-policies.md)來設定瀏覽體驗，以滿足您的獨特要求。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-111">When using Microsoft Edge with multi-app assigned access you can use the [Microsoft Edge browser policies](microsoft-edge-policies.md) to configure the browsing experience to meet your unique requirements.</span></span>

<span data-ttu-id="6d8f1-112">目前 Microsoft Edge 不支援與單一應用程式受指派的存取權相同的 Microsoft Edge 舊版 kiosk 模式類型，以及多應用程式受指派的存取權中的「公用瀏覽」kiosk 模式類型。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-112">Today Microsoft Edge does not support the same Microsoft Edge Legacy kiosk mode types for single-app assigned access and the "Public browsing" kiosk mode type in multi-app assigned access.</span></span> <span data-ttu-id="6d8f1-113">如果您需要適用於單一應用程式受指派的存取權 kiosk 裝置的瀏覽器，我們建議您使用 [Microsoft Edge 舊版 kiosk 模式](https://aka.ms/edgekioskmode)或 [Microsoft Kiosk 瀏覽器應用程式](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab)。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-113">If you need a browser for your single-app assigned access kiosk device, we recommend using [Microsoft Edge Legacy kiosk mode](https://aka.ms/edgekioskmode) or the [Microsoft Kiosk Browser app](https://www.microsoft.com/p/kiosk-browser/9ngb5s5xg2kp?activetab=pivot:overviewtab).</span></span> 

## <span data-ttu-id="6d8f1-114">Microsoft Edge “--kiosk” 命令列參數</span><span class="sxs-lookup"><span data-stu-id="6d8f1-114">Microsoft Edge “--kiosk” command line parameter</span></span>

<span data-ttu-id="6d8f1-115">您可以使用 “`--kiosk`” 命令列參數在 kiosk 模式下啟動 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-115">You can launch Microsoft Edge in kiosk mode using the “`--kiosk`” command line parameter.</span></span> <span data-ttu-id="6d8f1-116">這將在停用全螢幕鍵盤快速鍵 (F11) 時以全螢幕開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-116">This opens the browser in full screen with the full screen keyboard shortcut disabled (F11).</span></span> <span data-ttu-id="6d8f1-117">若要完成這項操作，請建立一個快速鍵，將目標設定為：</span><span class="sxs-lookup"><span data-stu-id="6d8f1-117">To accomplish this, create a shortcut with the target set to:</span></span><br>
*`"<local path>\msedge.exe" --kiosk http://bing.com`*

> [!NOTE]
> <span data-ttu-id="6d8f1-118">"`--kiosk`" 參數不會阻止使用者存取 Windows 鍵盤快速鍵，也不會阻止其他應用程式執行。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-118">The "`--kiosk`" parameter will not prevent the user from accessing Windows keyboard shortcuts and will not prevent other applications from running.</span></span> <span data-ttu-id="6d8f1-119">若要完成這種控制類型，請考慮使用 [AppLocker 建立 Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) 和[鍵盤篩選器](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter)。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-119">To accomplish this type of control, consider using [AppLocker to create a Windows 10 kiosk](https://docs.microsoft.com/windows/configuration/lock-down-windows-10-applocker) and [Keyboard Filter](https://docs.microsoft.com/windows-hardware/customize/enterprise/keyboardfilter).</span></span>

<span data-ttu-id="6d8f1-120">若要退出 kiosk 模式並關閉瀏覽器，請使用 alt+F4。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-120">To exit kiosk mode and close the browser use alt+F4.</span></span>

## <span data-ttu-id="6d8f1-121">支援 Microsoft Edge 舊版 kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="6d8f1-121">Support for Microsoft Edge Legacy kiosk mode</span></span>

<span data-ttu-id="6d8f1-122">安裝新版本的 Microsoft Edge Stable 通道時，會隱藏 Microsoft Edge 舊版，並將所有啟動 Microsoft Edge 舊版的嘗試重新導向到新版本。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-122">When the new version of Microsoft Edge Stable channel is installed, Microsoft Edge Legacy is hidden and all attempts to launch Microsoft Edge Legacy are redirected to the new version.</span></span> <span data-ttu-id="6d8f1-123">如需以下相關資訊：</span><span class="sxs-lookup"><span data-stu-id="6d8f1-123">For information about:</span></span>

- <span data-ttu-id="6d8f1-124">Windows Update 需求，請參閱[支援下一版 Microsoft Edge 的 Windows Update](microsoft-edge-sysupdate-windows-updates.md)</span><span class="sxs-lookup"><span data-stu-id="6d8f1-124">Windows update requirements, see [Windows updates to support the next version of Microsoft Edge](microsoft-edge-sysupdate-windows-updates.md)</span></span> 
- <span data-ttu-id="6d8f1-125">安裝 Microsoft Edge 後存取 Microsoft Edge 舊版，請參閱[安裝新版本 Microsoft Edge 後存取 Microsoft Edge 舊版](microsoft-edge-sysupdate-access-old-edge.md)</span><span class="sxs-lookup"><span data-stu-id="6d8f1-125">Accessing Microsoft Edge Legacy after installing Microsoft Edge,  see [Access Microsoft Edge Legacy after installing the new version of Microsoft Edge](microsoft-edge-sysupdate-access-old-edge.md)</span></span>
 
<span data-ttu-id="6d8f1-126">若要繼續在 kiosk 裝置上使用 Microsoft Edge 舊版 kiosk 模式，請採取以下動作之一：</span><span class="sxs-lookup"><span data-stu-id="6d8f1-126">To continue using Microsoft Edge Legacy kiosk mode on your kiosk devices take one of the following actions:</span></span> 

- <span data-ttu-id="6d8f1-127">如果您計畫安裝 Microsoft Edge Stable 通道、希望允許安裝它，或是已在 kiosk 裝置上安裝它，請部署 Microsoft Edge [允許 Microsoft Edge 並排瀏覽器體驗](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs)原則。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-127">If you plan to install Microsoft Edge Stable channel, want to allow it to be installed, or if it's already installed on your kiosk device deploy the Microsoft Edge [Allow Microsoft Edge Side by Side browser experience](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allowsxs) policy.</span></span>
- <span data-ttu-id="6d8f1-128">若要防止 Microsoft Edge Stable 通道安裝在您的 kiosk 裝置上，請部署適用於 Stable 通道的 Microsoft Edge [允許安裝預設值](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default)原則或考慮使用[封鎖程式工具組用來停用自動傳遞 Microsoft Edge](microsoft-edge-blocker-toolkit.md)。</span><span class="sxs-lookup"><span data-stu-id="6d8f1-128">To prevent Microsoft Edge Stable channel from being installed on your kiosk devices deploy the Microsoft Edge [Allow installation default](https://docs.microsoft.com/deployedge/microsoft-edge-update-policies#allow-installation-default) policy for Stable channel or consider using the [Blocker toolkit to disable automatic delivery of Microsoft Edge](microsoft-edge-blocker-toolkit.md).</span></span> 

## <span data-ttu-id="6d8f1-129">也請參閱</span><span class="sxs-lookup"><span data-stu-id="6d8f1-129">See also</span></span>

- [<span data-ttu-id="6d8f1-130">設定 Windows 桌面版的 Kiosk 與數位招牌</span><span class="sxs-lookup"><span data-stu-id="6d8f1-130">Configure kiosks and digital signs on Windows desktop editions</span></span>](https://docs.microsoft.com/windows/configuration/kiosk-methods)
- [<span data-ttu-id="6d8f1-131">部署 Microsoft Edge 舊版 kiosk 模式</span><span class="sxs-lookup"><span data-stu-id="6d8f1-131">Deploy Microsoft Edge Legacy kiosk mode</span></span>](https://aka.ms/edgekioskmode) 
- [<span data-ttu-id="6d8f1-132">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="6d8f1-132">Plan your deployment of Microsoft Edge</span></span>](deploy-edge-plan-deployment.md)
- [<span data-ttu-id="6d8f1-133">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="6d8f1-133">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
