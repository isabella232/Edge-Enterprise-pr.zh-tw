---
title: Active Directory (AD) 使用者的內部部署同步
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 08/21/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Active Directory (AD) 使用者的內部部署同步
ms.openlocfilehash: 89f061072fdaa748d317ca8dc0c290893cfdfd6c
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979602"
---
# <span data-ttu-id="f0642-103">Active Directory (AD) 使用者的內部部署同步</span><span class="sxs-lookup"><span data-stu-id="f0642-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="f0642-104">本文說明 Active Directory (AD) 使用者如何在不連線到 Microsoft 雲端服務的情況下，在電腦之間漫遊 Microsoft Edge 我的最愛和設定。</span><span class="sxs-lookup"><span data-stu-id="f0642-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="f0642-105">本文適用於 Microsoft Edge 版本 85 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f0642-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <span data-ttu-id="f0642-106">簡介</span><span class="sxs-lookup"><span data-stu-id="f0642-106">Introduction</span></span>

<span data-ttu-id="f0642-107">在 Microsoft Edge 中同步使用者資料，通常需要 Microsoft 帳戶或 Azure Active Directory (Azure AD) 帳戶，以及 Microsoft 雲端服務的連線。</span><span class="sxs-lookup"><span data-stu-id="f0642-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="f0642-108">有了內部部署同步，Microsoft Edge 會將 Active Directory 使用者的我的最愛和設定儲存至可在不同電腦之間移動的檔案。</span><span class="sxs-lookup"><span data-stu-id="f0642-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="f0642-109">內部部署同步不會干擾允許該功能的這些設定檔的雲端同步。</span><span class="sxs-lookup"><span data-stu-id="f0642-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <span data-ttu-id="f0642-110">運作方式</span><span class="sxs-lookup"><span data-stu-id="f0642-110">How it works</span></span>

<span data-ttu-id="f0642-111">Microsoft Edge 允許將設定檔與 Active Directory (AD) 帳戶 (其無法用於雲端同步) 建立關聯。啟用內部部署同步時，會將來自 AD 設定檔的資料儲存到名為 profile.pb 的檔案。</span><span class="sxs-lookup"><span data-stu-id="f0642-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="f0642-112">依預設，此檔案會儲存在 *%APP_DATA%/Microsoft/Edge* 中。</span><span class="sxs-lookup"><span data-stu-id="f0642-112">By default, this file is stored in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="f0642-113">此檔案寫入之後，可在不同的電腦之間移動該檔案，並且將在每一部電腦上讀取和寫入使用者資料。</span><span class="sxs-lookup"><span data-stu-id="f0642-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span>

## <span data-ttu-id="f0642-114">使用內部部署同步</span><span class="sxs-lookup"><span data-stu-id="f0642-114">Use on-premises sync</span></span>

<span data-ttu-id="f0642-115">若要使用內部部署同步，您必須啟用該功能，將設定檔與 AD 帳戶建立關聯，以及選擇性地變更使用者資料的位置。</span><span class="sxs-lookup"><span data-stu-id="f0642-115">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <span data-ttu-id="f0642-116">啟用內部部署同步</span><span class="sxs-lookup"><span data-stu-id="f0642-116">Enable on-premises sync</span></span>

<span data-ttu-id="f0642-117">若要在 Microsoft Edge 中啟用內部部署同步，請設定 [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) 原則。</span><span class="sxs-lookup"><span data-stu-id="f0642-117">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilesupportenabled) policy.</span></span>

### <span data-ttu-id="f0642-118">確保設定檔與 Active Directory 帳戶相關聯</span><span class="sxs-lookup"><span data-stu-id="f0642-118">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="f0642-119">內部部署同步僅適用與 Active Directory (AD) 帳戶相關聯的設定檔。</span><span class="sxs-lookup"><span data-stu-id="f0642-119">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="f0642-120">如果沒有這類設定檔，內部部署同步將無法運作。</span><span class="sxs-lookup"><span data-stu-id="f0642-120">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="f0642-121">若要確保使用者使用 AD 帳戶登入，請設定 [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) 原則。</span><span class="sxs-lookup"><span data-stu-id="f0642-121">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin) policy.</span></span>

### <span data-ttu-id="f0642-122">變更使用者資料的位置 (選用)</span><span class="sxs-lookup"><span data-stu-id="f0642-122">Change the location of the user data (optional)</span></span>

<span data-ttu-id="f0642-123">依預設，使用者資料會儲存在 *%APP_DATA%/Microsoft/Edge* 中名為 **profile.pb** 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="f0642-123">By default, the user data is stored in a filed named **profile.pb** in *%APP_DATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="f0642-124">若要變更此檔案的位置，請設定 [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) 原則。</span><span class="sxs-lookup"><span data-stu-id="f0642-124">To change the location of this file, configure the [RoamingProfileLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#roamingprofilelocation) policy.</span></span>

## <span data-ttu-id="f0642-125">啟用內部部署同步時使用者體驗的變更</span><span class="sxs-lookup"><span data-stu-id="f0642-125">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="f0642-126">啟用內部部署同步時，系統不會要求使用者啟用同步。此外，使用者無法在 [同步設定] 中關閉同步，且無法開啟內部部署同步所不支援的同步類型。</span><span class="sxs-lookup"><span data-stu-id="f0642-126">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <span data-ttu-id="f0642-127">內部部署同步使用方式說明</span><span class="sxs-lookup"><span data-stu-id="f0642-127">On-premises sync usage notes</span></span>

### <span data-ttu-id="f0642-128">在相同電腦上執行雲端同步和內部部署同步</span><span class="sxs-lookup"><span data-stu-id="f0642-128">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="f0642-129">內部部署同步不會干擾雲端同步。如果 Microsoft Edge 有會同步到雲端的多個 Microsoft 帳戶或 Azure Active Directory 設定檔，這些設定檔將會在啟用內部部署同步時繼續同步。</span><span class="sxs-lookup"><span data-stu-id="f0642-129">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <span data-ttu-id="f0642-130">不建議一次在多部電腦上執行 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f0642-130">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="f0642-131">由於內部部署同步的運作方式是透過在電腦之間移動使用者資料檔，因此內部部署同步並不會同步同時間工作階段之間的變更。</span><span class="sxs-lookup"><span data-stu-id="f0642-131">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="f0642-132">因此，內部部署同步於一次在一部電腦上使用時最適合。</span><span class="sxs-lookup"><span data-stu-id="f0642-132">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="f0642-133">如果同時間有執行內部部署工作階段，任何電腦上的資料可能會在您下一次啟動瀏覽器工作階段時，意外地遭到來自另一部電腦的資料覆寫。</span><span class="sxs-lookup"><span data-stu-id="f0642-133">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="f0642-134">啟用內部部署同步時，Microsoft Edge 會鎖定 **profile.pb** 檔案。</span><span class="sxs-lookup"><span data-stu-id="f0642-134">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="f0642-135">如果使用資料夾重新導向在不同的電腦之間共用單一 **profile.pb** 檔案，則只能啟動使用該檔案的 Microsoft Edge 的一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="f0642-135">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <span data-ttu-id="f0642-136">對內部部署同步使用其他同步原則</span><span class="sxs-lookup"><span data-stu-id="f0642-136">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="f0642-137">如果需要，您可以使用 [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) 原則來選擇性地停用我的最愛或設定同步。</span><span class="sxs-lookup"><span data-stu-id="f0642-137">The [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="f0642-138">如果 [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) 原則處於作用中，則也會停用內部部署同步。</span><span class="sxs-lookup"><span data-stu-id="f0642-138">If the [SyncDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#syncdisabled) policy is active, then on-premises sync is disabled as well.</span></span>  

## <span data-ttu-id="f0642-139">請參閱</span><span class="sxs-lookup"><span data-stu-id="f0642-139">See also</span></span>

- [<span data-ttu-id="f0642-140">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="f0642-140">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="f0642-141">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="f0642-141">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="f0642-142">Microsoft Edge 企業版同步處理</span><span class="sxs-lookup"><span data-stu-id="f0642-142">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)
