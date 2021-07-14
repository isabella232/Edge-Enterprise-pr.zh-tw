---
title: 重設 Microsoft Edge 資料
ms.author: collw
author: dan-wesley
manager: silvanam
ms.date: 07/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 如何重設雲端中的 Microsoft Edge 資料
ms.openlocfilehash: dc6c0ae1b1bc31228e9b9b1de315a19e99149134
ms.sourcegitcommit: 2a00571483e1d169b2b3b59f4fce43262f460a9a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2021
ms.locfileid: "11643738"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a><span data-ttu-id="7a1fb-103">重設雲端中的 Microsoft Edge 資料</span><span class="sxs-lookup"><span data-stu-id="7a1fb-103">Reset Microsoft Edge data in the cloud</span></span>

<span data-ttu-id="7a1fb-104">本文描述用於重設您在雲端中 Microsoft Edge 資料的步驟。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-104">This article describes the steps for resetting your Microsoft Edge data in the cloud.</span></span>

> [!NOTE]
> <span data-ttu-id="7a1fb-105">除非另有說明，否則本文適用於 Microsoft Edge 版本 88 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-105">This article applies to Microsoft Edge version 88 or later unless otherwise noted.</span></span>

> [!NOTE]
> <span data-ttu-id="7a1fb-106">如果您的租用戶位於 GCC Mod 環境中，您的租用戶系統管理員將需要向 Microsoft 提出支援要求以重設您的資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-106">If your tenant is in a GCC Mod environment, your tenant admin will need to file a support request with Microsoft to reset your data.</span></span>

## <a name="overview"></a><span data-ttu-id="7a1fb-107">概觀</span><span class="sxs-lookup"><span data-stu-id="7a1fb-107">Overview</span></span>

<span data-ttu-id="7a1fb-108">在某些情況下，您會想要重設您在雲端中的 Microsoft Edge 資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-108">There are situations in which you want to reset your Microsoft Edge data in the cloud.</span></span> <span data-ttu-id="7a1fb-109">例如，您想要同步您的資料，但 Microsoft Edge 報告無法同步資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-109">For example,  you want to synchronize your data, but Microsoft Edge reports that it is unable to synchronize the data.</span></span> <span data-ttu-id="7a1fb-110">或者，您可能想要確認已從 Microsoft 雲端中移除您的資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-110">Or you might want to make sure that your data is removed from Microsoft’s cloud.</span></span> <span data-ttu-id="7a1fb-111">在這兩個情況下，Microsoft Edge 可讓您執行雲端資料重設。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-111">In both cases, Microsoft Edge lets you perform a cloud data reset.</span></span>

## <a name="back-up-your-favorites"></a><span data-ttu-id="7a1fb-112">備份我的最愛</span><span class="sxs-lookup"><span data-stu-id="7a1fb-112">Back up your favorites</span></span>

<span data-ttu-id="7a1fb-113">執行重設之前，建議您備份我的最愛。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-113">Before performing a reset, we recommend that you back up your favorites.</span></span> <span data-ttu-id="7a1fb-114">使用下列步驟以備份我的最愛。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-114">Use the following steps to back up your favorites.</span></span>

1. <span data-ttu-id="7a1fb-115">在 Microsoft Edge 右上角，選取 **設定和其他 > 我的最愛 > 其他選項 > 匯出我的最愛**。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-115">In the upper-right corner of Microsoft Edge, select **Settings and more > Favorites > More options > Export favorites**.</span></span>
2. <span data-ttu-id="7a1fb-116">選擇您要儲存我的最愛的檔案。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-116">Choose the file to where you want to save your favorites.</span></span> <span data-ttu-id="7a1fb-117">您可以輸入自己的檔案名稱，或使用 Microsoft Edge 預設提供的名稱 "favorites_month_day_year.html" 做為檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-117">You can type your own filename or use the name that Microsoft Edge provides by default,  "favorites_month_day_year.html" as a filename.</span></span> <span data-ttu-id="7a1fb-118">例如，"favorites_12_17_20.html"。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-118">For example, "favorites_12_17_20.html".</span></span> <span data-ttu-id="7a1fb-119">如果您之後需要還原我的最愛，可以透過該檔案完成。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-119">If you need to restore your favorites later, you can do so from that file.</span></span>
3. <span data-ttu-id="7a1fb-120">按一下 [儲存]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-120">Click **Save**.</span></span>

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a><span data-ttu-id="7a1fb-121">執行重設以修正同步問題</span><span class="sxs-lookup"><span data-stu-id="7a1fb-121">Perform a reset to fix a synchronization problem</span></span>

<span data-ttu-id="7a1fb-122">如果 Microsoft Edge 報告無法同步您的資料，並建議重設資料，請執行重設以修正問題。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-122">If Microsoft Edge reports that it can't synchronize your data and suggests resetting your data, perform a reset to fix the problem.</span></span>

<span data-ttu-id="7a1fb-123">使用下列步驟來執行重設。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-123">Use the following steps to do a reset.</span></span>

1. <span data-ttu-id="7a1fb-124">首先，確認您已在您所有裝置上登出 Microsoft Edge，包括您的行動裝置，但執行重設所在裝置除外。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-124">First, make sure that you’re signed out of Microsoft Edge on all your devices, including your mobile devices, except the device you are performing the reset on.</span></span> <span data-ttu-id="7a1fb-125">若要登出 Microsoft Edge，請在 Microsoft Edge 的右下角，選取 **[設定及其他] > [設定] > [登出]**。登出時，請勿選取從本機裝置清除我的最愛、設定等選項。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-125">To sign out of Microsoft Edge, in the upper-right corner of Microsoft Edge select **Settings and more > Settings > Sign out**. When signing out, do not select the option to clear favorites, settings, and etc. from your local device.</span></span>
2. <span data-ttu-id="7a1fb-126">登出所有其他裝置之後，請開啟桌面上的 Microsoft Edge。在 Microsoft Edge 的右上角設定 **其他 > 重設同步處理**。在產生的對話方塊中，選擇以重設資料後繼續同步處理，然後選取 **重設**。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-126">After you sign out of all your other devices, open Microsoft Edge on your desktop.In the upper-right corner of Microsoft Edge **Select Settings and more > Sync > Reset sync**. In the resulting dialog box, choose to resume sync after resetting data, and then select **Reset**.</span></span>

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a><span data-ttu-id="7a1fb-127">執行重設以將您的資料從 Microsoft 雲端中移除</span><span class="sxs-lookup"><span data-stu-id="7a1fb-127">Perform a reset to remove your data from Microsoft’s cloud</span></span>

<span data-ttu-id="7a1fb-128">如果您想要從 Microsoft 雲端移除您的資料，請使用下列步驟來執行重設。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-128">If you want to remove your data from Microsoft’s cloud, use the following steps to do a reset.</span></span>

1. <span data-ttu-id="7a1fb-129">在裝置上停止同步，您執行重設所在的裝置除外。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-129">Stop synchronization on devices except the device you are performing the reset on.</span></span>  <span data-ttu-id="7a1fb-130">在 Microsof Edge 的右上角，選取 **設定和其他 > 設定 > 同步> 關閉同步**。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-130">In the upper-right corner of Microsoft Edge, select **Settings and more > Settings > Sync > Turn off sync**.</span></span>  
2. <span data-ttu-id="7a1fb-131">停止同步之後，在 Microsof Edge 的右上角，請選取 [設定及其他]\*\*\*\* > [同步] > [重設同步]\*\*\*\*。在產生的對話方塊中，不要選擇在重設資料之後繼續同步。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-131">After you stop synchronization, in the upper-right corner of Microsoft Edge select **Settings and more > Sync > Reset sync**. In the resulting dialog box, **do not** choose to resume sync after resetting data.</span></span> <span data-ttu-id="7a1fb-132">選取 [重設]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-132">Select **Reset**.</span></span>

## <a name="what-to-expect-during-and-after-a-data-reset"></a><span data-ttu-id="7a1fb-133">資料重設期間及之後的預期</span><span class="sxs-lookup"><span data-stu-id="7a1fb-133">What to expect during and after a data reset</span></span>

<span data-ttu-id="7a1fb-134">資料重設可能需要幾秒到幾分鐘的時間，取決於您儲存在 Microsoft 雲端中的資料量。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-134">A data reset can take from a few seconds to a few minutes, depending on how much data you have stored in Microsoft’s cloud.</span></span> <span data-ttu-id="7a1fb-135">在某些情況下，您可能會看到一則訊息，指出該重設無法完成，並建議您再次重設。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-135">In some cases, you might see a message saying that a reset could not be completed and a suggestion to reset again.</span></span> <span data-ttu-id="7a1fb-136">在此情況下，請等候幾小時，然後再次嘗試重設資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-136">In this case, wait a few hours and try to reset the data again.</span></span> <span data-ttu-id="7a1fb-137">如果您仍無法重設資料，請與 Microsoft Edge 支援人員連絡。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-137">If you are still unable to reset your data, contact Microsoft Edge Support.</span></span>

<span data-ttu-id="7a1fb-138">資料重設成功完成之後，如果您選擇在重設之後繼續同步，則會再次從您的裝置同步資料。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-138">After a data reset has been successfully completed, data will once again synchronize from your device if you chose to resume sync after the reset.</span></span> <span data-ttu-id="7a1fb-139">如果您想要從您的其他裝置進行同步，您必須重新登入這些裝置。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-139">You will need to sign back in on your other devices if you want to sync from those devices.</span></span> <span data-ttu-id="7a1fb-140">不過，如果您未選擇繼續同步，則您的 Microsoft Edge 資料會從雲端中移除，且您的資料將不再可同步。</span><span class="sxs-lookup"><span data-stu-id="7a1fb-140">However, if you didn’t choose to resume sync, then your Microsoft Edge data is removed from the cloud and your data will no longer synchronize.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a1fb-141">請參閱</span><span class="sxs-lookup"><span data-stu-id="7a1fb-141">See also</span></span>

- [<span data-ttu-id="7a1fb-142">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="7a1fb-142">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="7a1fb-143">Microsoft Edge 企業同步</span><span class="sxs-lookup"><span data-stu-id="7a1fb-143">Microsoft Edge Enterprise Sync</span></span>](microsoft-edge-enterprise-sync.md)