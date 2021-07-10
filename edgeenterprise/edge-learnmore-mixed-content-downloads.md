---
title: Microsoft Edge 和混合式內容下載
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 和混合式內容下載
ms.openlocfilehash: 4871b23145d365e814c5cf1cac7699044f3da35e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11642139"
---
# <a name="learn-about-microsoft-edge-and-mixed-content-downloads"></a>了解 Microsoft Edge 和混合式內容下載

本文說明混合式內容下載以及 Microsoft Edge 的處理方式。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 85 或更新版本。

## <a name="what-are-mixed-content-downloads"></a>什麼是混合式內容下載？

當您從透過安全 HTTPS 連線載入的 HTML 頁面開始下載時，就會發生混合式內容下載，但有下列其中一種情況存在：

- 一或多個下載位置的重新導向是透過不安全的 HTTP 連線所載入。
- 最終的下載位置是透過不安全的 HTTP 連線所載入。

上述任一案例會因為使用安全的 HTTPS 來提出要求而成為混合式內容，而且 HTTP 與 HTTPS 內容均涉及最終下載目的地。 新式瀏覽器會顯示有關此內容類型的警告，向使用者表明：即使存取的原始頁面很安全，也可能不安全地傳輸此下載。

## <a name="download-warnings-and-user-options"></a>下載警告和使用者選項

下載警告可確保使用者知道正在下載的檔案可能會遭到網路上的惡意攻擊者讀取。 此警告可讓使用者做出知情決策來決定是否下載檔案。

在 Microsoft Edge 中，混合式內容下載會遭到封鎖，但是使用者可以視需要覆寫和下載檔案。 從 Microsoft Edge 版本 85 開始，Microsoft Edge 打算開始封鎖混合式內容的可執行檔下載，而在未來的版本中將會封鎖不同的檔案類型。

> [!NOTE]
> 此功能的部署可能視發行排程和使用者意見反應而有所變動。

<!-- The schedule of the block for different filetypes is to be determined and may be impacted by usage data and user feedback. -->

在下載列中，封鎖警告訊息看起來就像下一個螢幕擷取畫面中的範例。

 ![下載匣中的混合式內容警告](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-tray-warning.png)

在下載頁面上，封鎖警告看起來就像以下螢幕擷取畫面範例：

 ![混合式內容覆寫提示](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-page-warning.png)

如果使用者決定要保留下載，系統會提示他們確認其動作。 下一個螢幕擷取畫面顯示此確認提示的範例。

 ![Internet Explorer 模式](./media/edge-learnmore-mixed-content-downloads/edge-mixed-content-download-override.png)

## <a name="supporting-policies"></a>支援原則

如果企業想要排除特定網站的混合式內容封鎖，可以使用 [InsecureContentAllowedForUrls](./microsoft-edge-policies.md#insecurecontentallowedforurls) 原則執行此操作。

## <a name="content-license"></a>內容授權

> [!NOTE]
> 本頁的某些部分是根據 Chromium.org 創造和分享的作品加以修改，並根據[創用 CC 姓名標示 4.0 國際版本授權條款](http://creativecommons.org/licenses/by/4.0/)中所述條款加以使用。 原始頁面可在[此處](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content)找到。
  
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />本作品根據<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">創用 CC 姓名標示 4.0 國際版本授權條款</a>獲得授權。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)