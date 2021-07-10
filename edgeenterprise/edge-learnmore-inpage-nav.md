---
title: 在 Internet Explorer 模式中保留頁面內瀏覽
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 在 Internet Explorer 模式中保留頁面內瀏覽
ms.openlocfilehash: 20b18d121c3babfaacffd4a08316b25be714d95e
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641359"
---
# <a name="keep-in-page-navigation-in-internet-explorer-mode"></a>在 Internet Explorer 模式中保留頁面內瀏覽

您可以使用此原則做為臨時解決方案，強制來自 Internet Explorer 模式 (IE 模式) 網站的所有頁面內瀏覽，以維持使用 IE 模式。

頁面內瀏覽是從連結、指令碼或目前頁面上的表單開始。 也可以是先前頁面內瀏覽嘗試的伺服器端重新導向。 相反地，使用者可以使用瀏覽器控制項以多種方式啟動不在頁面內且獨立於目前頁面的瀏覽。 例如，使用網址列、[返回] 按鈕或 [我的最愛] 連結。

>[!NOTE]
>本文適用於 Microsoft Edge 版本 81 或更新版本。

## <a name="prerequisites"></a>必要條件

此原則需要下列 Windows 更新：

- Windows 10 版本 1909 & 1903、Windows Server 版本 1909 & 1903  ([KB4532695](https://support.microsoft.com/help/4532695))
- Windows 10 版本 1809、Windows Server 版本 1809、Windows Server 2019 ([KB4534321](https://support.microsoft.com/help/4534321))
- Windows 10 版本 1803 ([KB4534308](https://support.microsoft.com/help/4534308))
- Windows 10 版本 1709 ([KB4534318](https://support.microsoft.com/help/4534318))


## <a name="about-this-policy"></a>關於此原則

此原則能讓您有時間識別和設定 IE 模式網站使用的所有驗證伺服器。 不過，此原則可能會造成不一致的瀏覽體驗，而有些網站會在 IE 模式中轉譯，而有時候則以 Microsoft Edge 模式轉譯。 這取決於網站是否從 IE 模式頁面開始瀏覽。 任何未明確設定為在特定轉譯引擎開啟的網站都會受到此不一致的限制。

如果您啟用這個原則，我們建議您在識別所有驗證伺服器後將它停用，並將它們新增到網站清單以設為中性。 此動作可確保您的新式網站永遠不會在 IE 模式中意外轉譯。

## <a name="keep-in-page-navigation-in-ie-mode"></a>在 IE 模式中保持頁面內瀏覽

若要在 Internet Explorer 模式中保持自動或所有頁面內瀏覽，請按照下列步驟進行：

1. 開啟 [本機群組原則編輯器]。
2. 按一下**電腦組態** > **系統管理範本** > **Microsoft Edge**。
3. 在 [設定]**** 底下，按兩下 [指定從 Internet Explorer 模式頁面啟動時，未設定網站的「頁面內」瀏覽方式]****。

   ![頁面內原則設定](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-settings.png)

4. 選取 [已啟用]**** 

   ![啟用頁面內原則](media/edge-learnmore-inpage-nav/learnmore-in-page-nav-enable.png)

5. 從下拉式清單中選擇下列其中一個選項：

   - **預設** - 只有設定以 Internet Explorer 模式開啟的網站才會以該模式開啟。 任何未設定以 Internet Explorer 模式開啟的網站都將被重新導向回 Microsoft Edge。
   - **僅保持 Internet Explorer 模式中的自動瀏覽功能** - 如果您想要預設體驗，請使用此選項，除了所有自動瀏覽 (例如 302 重新導向) 到未設定的網站以外，都會保持 Internet Explorer 模式。
   - **在 Internet Explorer 模式中保留所有頁面流覽**  **_ (建議_*) _ - 從以 IE 模式載入的頁面到未配置的網站的流覽，所有流覽都保持為 Internet Explorer 模式。

6. 按一下 *_OK** 或 **[申請** 以儲存原則設定。

## <a name="see-also"></a>另請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
