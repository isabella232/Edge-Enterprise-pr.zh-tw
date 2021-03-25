---
title: Active Directory (AD) 使用者的內部部署同步
ms.author: scottbo
author: dan-wesley
manager: silvanam
ms.date: 02/12/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Active Directory (AD) 使用者的內部部署同步
ms.openlocfilehash: 820188db94f4ab2bc9b1ad659c22c324bcea145b
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11448047"
---
# <a name="on-premises-sync-for-active-directory-ad-users"></a><span data-ttu-id="c0b88-103">Active Directory (AD) 使用者的內部部署同步</span><span class="sxs-lookup"><span data-stu-id="c0b88-103">On-premises sync for Active Directory (AD) users</span></span>

<span data-ttu-id="c0b88-104">本文說明 Active Directory (AD) 使用者如何在不連線到 Microsoft 雲端服務的情況下，在電腦之間漫遊 Microsoft Edge 我的最愛和設定。</span><span class="sxs-lookup"><span data-stu-id="c0b88-104">This article explains how Active Directory (AD) users can roam Microsoft Edge favorites and settings between computers without connecting to Microsoft cloud services.</span></span>

> [!NOTE]
> <span data-ttu-id="c0b88-105">本文適用於 Microsoft Edge 版本 85 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c0b88-105">This article applies to Microsoft Edge version 85 or later.</span></span>

## <a name="introduction"></a><span data-ttu-id="c0b88-106">簡介</span><span class="sxs-lookup"><span data-stu-id="c0b88-106">Introduction</span></span>

<span data-ttu-id="c0b88-107">在 Microsoft Edge 中同步使用者資料，通常需要 Microsoft 帳戶或 Azure Active Directory (Azure AD) 帳戶，以及 Microsoft 雲端服務的連線。</span><span class="sxs-lookup"><span data-stu-id="c0b88-107">Syncing user data in Microsoft Edge normally requires either a Microsoft Account or an Azure Active Directory (Azure AD) account, and a connection to Microsoft cloud services.</span></span> <span data-ttu-id="c0b88-108">有了內部部署同步，Microsoft Edge 會將 Active Directory 使用者的我的最愛和設定儲存至可在不同電腦之間移動的檔案。</span><span class="sxs-lookup"><span data-stu-id="c0b88-108">With on-premises sync, Microsoft Edge saves an Active Directory user's favorites and settings to a file that can be moved between different computers.</span></span> <span data-ttu-id="c0b88-109">內部部署同步不會干擾允許該功能的這些設定檔的雲端同步。</span><span class="sxs-lookup"><span data-stu-id="c0b88-109">On-premises sync doesn't interfere with cloud syncing for those profiles that allow it.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="c0b88-110">運作方式</span><span class="sxs-lookup"><span data-stu-id="c0b88-110">How it works</span></span>

<span data-ttu-id="c0b88-111">Microsoft Edge 允許將設定檔與 Active Directory (AD) 帳戶 (其無法用於雲端同步) 建立關聯。啟用內部部署同步時，會將來自 AD 設定檔的資料儲存到名為 profile.pb 的檔案。</span><span class="sxs-lookup"><span data-stu-id="c0b88-111">Microsoft Edge allows profiles to be associated with Active Directory (AD) accounts, which can't be used with cloud sync. When on-premises sync is enabled, the data from the AD profile is saved to a file named profile.pb.</span></span> <span data-ttu-id="c0b88-112">依預設，此檔案會儲存在 *%APPDATA%/Microsoft/Edge* 中。</span><span class="sxs-lookup"><span data-stu-id="c0b88-112">By default, this file is stored in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="c0b88-113">此檔案寫入之後，可在不同的電腦之間移動該檔案，並且將在每一部電腦上讀取和寫入使用者資料。</span><span class="sxs-lookup"><span data-stu-id="c0b88-113">After this file is written, it can be moved between different computers, and user data will be read and written on each computer.</span></span> <span data-ttu-id="c0b88-114">Microsoft Edge 只會從此檔案讀取和寫入內容；系統管理員有責任確保可視需要移動檔案。</span><span class="sxs-lookup"><span data-stu-id="c0b88-114">Microsoft Edge only reads and writes from this file; it is the admin's responsibility to ensure that the file is moved as needed.</span></span>

## <a name="use-on-premises-sync"></a><span data-ttu-id="c0b88-115">使用內部部署同步</span><span class="sxs-lookup"><span data-stu-id="c0b88-115">Use on-premises sync</span></span>

<span data-ttu-id="c0b88-116">若要使用內部部署同步，您必須啟用該功能，將設定檔與 AD 帳戶建立關聯，以及選擇性地變更使用者資料的位置。</span><span class="sxs-lookup"><span data-stu-id="c0b88-116">To use on-premises sync, you have to enable it, associate a profile with an AD account, and optionally, change the location of the user data.</span></span>

### <a name="enable-on-premises-sync"></a><span data-ttu-id="c0b88-117">啟用內部部署同步</span><span class="sxs-lookup"><span data-stu-id="c0b88-117">Enable on-premises sync</span></span>

<span data-ttu-id="c0b88-118">若要在 Microsoft Edge 中啟用內部部署同步，請設定 [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) 原則。</span><span class="sxs-lookup"><span data-stu-id="c0b88-118">To enable on-premises sync in Microsoft Edge, configure the [RoamingProfileSupportEnabled](./microsoft-edge-policies.md#roamingprofilesupportenabled) policy.</span></span>

### <a name="ensure-that-a-profile-is-associated-with-an-active-directory-account"></a><span data-ttu-id="c0b88-119">確保設定檔與 Active Directory 帳戶相關聯</span><span class="sxs-lookup"><span data-stu-id="c0b88-119">Ensure that a profile is associated with an Active Directory account</span></span>

<span data-ttu-id="c0b88-120">內部部署同步僅適用與 Active Directory (AD) 帳戶相關聯的設定檔。</span><span class="sxs-lookup"><span data-stu-id="c0b88-120">On-premises sync only works with the profile associated with an Active Directory (AD) account.</span></span> <span data-ttu-id="c0b88-121">如果沒有這類設定檔，內部部署同步將無法運作。</span><span class="sxs-lookup"><span data-stu-id="c0b88-121">If no such profile exists, on-premises sync will not function.</span></span> <span data-ttu-id="c0b88-122">若要確保使用者使用 AD 帳戶登入，請設定 [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) 原則。</span><span class="sxs-lookup"><span data-stu-id="c0b88-122">To ensure that users sign on with an AD account, configure the [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) policy.</span></span> <span data-ttu-id="c0b88-123">針對內部部署的同步，Microsoft Edge 只會仰賴於 AD 來建立使用者資料的身分識別，而 Microsoft Edge 讀取和寫入內部部署資料的方式與系統管理員為 AD 使用者設定漫遊的方式之間並沒有直接的關係。</span><span class="sxs-lookup"><span data-stu-id="c0b88-123">For on-premises sync, Microsoft Edge only relies on AD to establish an identity for the user data, and there's no direct relationship between how Microsoft Edge reads and writes on-premises data to how the admin has configured roaming for an AD user.</span></span>

### <a name="change-the-location-of-the-user-data-optional"></a><span data-ttu-id="c0b88-124">變更使用者資料的位置 (選用)</span><span class="sxs-lookup"><span data-stu-id="c0b88-124">Change the location of the user data (optional)</span></span>

<span data-ttu-id="c0b88-125">依預設，使用者資料會儲存在 *%APPDATA%/Microsoft/Edge* 中名為 **profile.pb** 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="c0b88-125">By default, the user data is stored in a filed named **profile.pb** in *%APPDATA%/Microsoft/Edge*.</span></span> <span data-ttu-id="c0b88-126">若要變更此檔案的位置，請設定 [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) 原則。</span><span class="sxs-lookup"><span data-stu-id="c0b88-126">To change the location of this file, configure the [RoamingProfileLocation](./microsoft-edge-policies.md#roamingprofilelocation) policy.</span></span>

## <a name="changes-in-the-user-experience-when-on-premises-sync-is-enabled"></a><span data-ttu-id="c0b88-127">啟用內部部署同步時使用者體驗的變更</span><span class="sxs-lookup"><span data-stu-id="c0b88-127">Changes in the user experience when on-premises sync is enabled</span></span>

<span data-ttu-id="c0b88-128">啟用內部部署同步時，系統不會要求使用者啟用同步。此外，使用者無法在 [同步設定] 中關閉同步，且無法開啟內部部署同步所不支援的同步類型。</span><span class="sxs-lookup"><span data-stu-id="c0b88-128">When on-premises sync is enabled, users won't be asked to enable sync. In addition, users can't turn off sync in Sync settings, and they can't turn on sync types that aren't supported by on-premises sync.</span></span>

## <a name="on-premises-sync-usage-notes"></a><span data-ttu-id="c0b88-129">內部部署同步使用方式說明</span><span class="sxs-lookup"><span data-stu-id="c0b88-129">On-premises sync usage notes</span></span>

### <a name="running-cloud-sync-and-on-premises-sync-on-the-same-computer"></a><span data-ttu-id="c0b88-130">在相同電腦上執行雲端同步和內部部署同步</span><span class="sxs-lookup"><span data-stu-id="c0b88-130">Running cloud sync and on-premises sync on the same computer</span></span>

<span data-ttu-id="c0b88-131">內部部署同步不會干擾雲端同步。如果 Microsoft Edge 有會同步到雲端的多個 Microsoft 帳戶或 Azure Active Directory 設定檔，這些設定檔將會在啟用內部部署同步時繼續同步。</span><span class="sxs-lookup"><span data-stu-id="c0b88-131">On-premises sync doesn't interfere with cloud sync. If Microsoft Edge has multiple Microsoft Account or Azure Active Directory profiles that sync to the cloud, these profiles will continue to sync while on-premises sync is enabled.</span></span>

### <a name="running-microsoft-edge-on-more-than-one-computer-at-a-time-isnt-recommended"></a><span data-ttu-id="c0b88-132">不建議一次在多部電腦上執行 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0b88-132">Running Microsoft Edge on more than one computer at a time isn't recommended</span></span>

<span data-ttu-id="c0b88-133">由於內部部署同步的運作方式是透過在電腦之間移動使用者資料檔，因此內部部署同步並不會同步同時間工作階段之間的變更。</span><span class="sxs-lookup"><span data-stu-id="c0b88-133">Because on-premises sync works by moving a user data file between computers, on-premises sync doesn't sync changes between simultaneous sessions.</span></span> <span data-ttu-id="c0b88-134">因此，內部部署同步於一次在一部電腦上使用時最適合。</span><span class="sxs-lookup"><span data-stu-id="c0b88-134">For this reason, on-premises sync works best when used on one computer at a time.</span></span> <span data-ttu-id="c0b88-135">如果同時間有執行內部部署工作階段，任何電腦上的資料可能會在您下一次啟動瀏覽器工作階段時，意外地遭到來自另一部電腦的資料覆寫。</span><span class="sxs-lookup"><span data-stu-id="c0b88-135">If there are simultaneous on-premises sessions running, data on any of the computers may be unexpectedly overwritten by data from another computer the next time you start a browser session.</span></span>

> [!NOTE]
> <span data-ttu-id="c0b88-136">啟用內部部署同步時，Microsoft Edge 會鎖定 **profile.pb** 檔案。</span><span class="sxs-lookup"><span data-stu-id="c0b88-136">Microsoft Edge locks the **profile.pb** file when on-premises sync is enabled.</span></span> <span data-ttu-id="c0b88-137">如果使用資料夾重新導向在不同的電腦之間共用單一 **profile.pb** 檔案，則只能啟動使用該檔案的 Microsoft Edge 的一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="c0b88-137">If folder redirection is used to share a single **profile.pb** file between different computers, then only one instance of Microsoft Edge using that file can be started.</span></span>

### <a name="using-other-sync-policies-with-on-premises-sync"></a><span data-ttu-id="c0b88-138">對內部部署同步使用其他同步原則</span><span class="sxs-lookup"><span data-stu-id="c0b88-138">Using other sync policies with on-premises sync</span></span>

<span data-ttu-id="c0b88-139">如果需要，您可以使用 [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) 原則來選擇性地停用我的最愛或設定同步。</span><span class="sxs-lookup"><span data-stu-id="c0b88-139">The [SyncTypesListDisabled](./microsoft-edge-policies.md#synctypeslistdisabled) policy can be used to selectively disable either favorites or settings sync if desired.</span></span> <span data-ttu-id="c0b88-140">[SyncDisabled](./microsoft-edge-policies.md#syncdisabled) 原則對內部部署同步沒有影響。</span><span class="sxs-lookup"><span data-stu-id="c0b88-140">The [SyncDisabled](./microsoft-edge-policies.md#syncdisabled) policy has no impact on on-premises sync.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0b88-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0b88-141">See also</span></span>

- [<span data-ttu-id="c0b88-142">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="c0b88-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="c0b88-143">Microsoft Edge 和企業狀態漫遊</span><span class="sxs-lookup"><span data-stu-id="c0b88-143">Microsoft Edge and Enterprise State Roaming</span></span>](microsoft-edge-enterprise-state-roaming.md)
- [<span data-ttu-id="c0b88-144">Microsoft Edge 企業版同步處理</span><span class="sxs-lookup"><span data-stu-id="c0b88-144">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)