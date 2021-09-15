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
ms.openlocfilehash: 65984daea523a7749a28d8ab6a4dd990c5fea849
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978796"
---
# <a name="reset-microsoft-edge-data-in-the-cloud"></a>重設雲端中的 Microsoft Edge 資料

本文描述用於重設您在雲端中 Microsoft Edge 資料的步驟。

> [!NOTE]
> 除非另有說明，否則本文適用於 Microsoft Edge 版本 88 或更新版本。

> [!NOTE]
> 如果您的租用戶位於 GCC Mod 環境中，您的租用戶系統管理員將需要向 Microsoft 提出支援要求以重設您的資料。

## <a name="overview"></a>概觀

在某些情況下，您會想要重設您在雲端中的 Microsoft Edge 資料。 例如，您想要同步您的資料，但 Microsoft Edge 報告無法同步資料。 或者，您可能想要確認已從 Microsoft 雲端中移除您的資料。 在這兩個情況下，Microsoft Edge 可讓您執行雲端資料重設。

## <a name="back-up-your-favorites"></a>備份我的最愛

執行重設之前，建議您備份我的最愛。 使用下列步驟以備份我的最愛。

1. 在 Microsoft Edge 中，選取 [按 Ctrl+Shift+O] > [選擇三個點] > [按匯出我的最愛 **]**。
2. 選擇您要儲存我的最愛的檔案。 您可以輸入自己的檔案名稱，或使用 Microsoft Edge 預設提供的名稱「favorites_month_day_year.html」做為檔案名稱。 例如，「favorites_07_05_21.htm」。 如果您之後需要還原我的最愛，可以透過該檔案完成。
3. 按一下 [儲存]****。

## <a name="perform-a-reset-to-fix-a-synchronization-problem"></a>執行重設以修正同步問題

如果 Microsoft Edge 報告無法同步您的資料，並建議重設資料，請執行重設以修正問題。

使用下列步驟來執行重設。

1. 首先，確認您已在您所有裝置上登出 Microsoft Edge，包括您的行動裝置，但執行重設所在裝置除外。 若要登出 Microsoft Edge，請選取 [設定] > [個人檔案] > [登出]****。登出時，請勿選取從本機裝置清除我的最愛、設定等選項。
2. 登出其他所有裝置之後，在桌面上開啟 Microsoft Edge。 選取 [設定] > [個人檔案] > [重設同步處理]****。在產生的對話方塊中，選擇在重設資料之後繼續同步，然後選取 [立即重設]****。

## <a name="perform-a-reset-to-remove-your-data-from-microsofts-cloud"></a>執行重設以將您的資料從 Microsoft 雲端中移除

如果您想要從 Microsoft 雲端移除您的資料，請使用下列步驟來執行重設。

1. 在裝置上停止同步處理，您執行重設所在的裝置除外。  在 Microsoft Edge中，選取 [設定] > [個人檔案] > [關閉同步]****。  
2. 停止同步處理後，選取 [設定] > [個人檔案] > [重設同步處理]****。在產生的對話方塊中，在重設同步處理之後，**不要**選擇在此裝置上繼續同步。選取 [重設]****。

## <a name="what-to-expect-during-and-after-a-data-reset"></a>資料重設期間及之後的預期

資料重設可能需要幾秒到幾分鐘的時間，取決於您儲存在 Microsoft 雲端中的資料量。 在某些情況下，您可能會看到一則訊息，指出該重設無法完成，並建議您再次重設。 在此情況下，請等候幾小時，然後再次嘗試重設資料。 如果您仍無法重設資料，請與 Microsoft Edge 支援人員連絡。

資料重設成功完成之後，如果您選擇在重設之後繼續同步，則會再次從您的裝置同步資料。 如果您想要從您的其他裝置進行同步，您必須重新登入這些裝置。 不過，如果您未選擇繼續同步，則您的 Microsoft Edge 資料會從雲端中移除，且您的資料將不再可同步。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 企業同步](microsoft-edge-enterprise-sync.md)
