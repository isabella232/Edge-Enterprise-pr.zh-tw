---
title: IE 模式常見問題集
ms.author: shisub
author: dan-wesley
manager: srugh
ms.date: 03/15/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 適用於 IE 模式 Microsoft Edge 的常見問題集和疑難排解
ms.openlocfilehash: 565af265811e0e4814d82859f638ae9abcd0a014
ms.sourcegitcommit: ef30fe37d0d115af0d4402c9005f5d0d1ba54b6c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "11431810"
---
# <a name="ie-mode-faq"></a>IE 模式常見問題集

本文提供 Microsoft Edge 版本 77 或更新版本的疑難排解秘訣和常見問題集。

> [!NOTE]
> 本文適用於 Microsoft Edge **Stable**、**Beta** 和 **Dev** 通道，版本 77 或更新版本。


## <a name="troubleshoot-ie-mode"></a>疑難排解 IE 模式

使用本節中的資訊來診斷和修復 IE 模式問題。

### <a name="internet-explorer-mode-diagnostic-information"></a>Internet Explorer 模式診斷資訊

您可以在 Microsoft Edge 相容性索引標籤上取得 Internet Explorer 模式診斷資訊。若要開啟此索引標籤，請移至 *edge://compat/iediagnostic*。 此頁面可能會顯示診斷訊息。 本頁也提供下列類別的設定資訊：

- **登錄機碼檢查**。 (只有檢查失敗時才會顯示。) 檢查登錄中是否正確設定了 Internet Explorer 整合。 如果未正確設定，使用者可以按一下**修正**來解決問題。
- **Internet Explorer 模式**。 顯示所使用的 API 版本，該版本基於設定和作業系統。 如果發生問題，可能會提示使用者安裝 **Windows Update**。
- **Internet Explorer 模式**。 顯示是否已啟用 Internet Explorer 模式，以及其設定方式。
- **命令列**。 顯示用於啟動 Microsoft Edge 的命令列字串和參數。
- **群組原則設定**。 顯示是否使用群組原則設定 IE 模式，以及所套用的原則。

### <a name="error-message-to-open-this-page-in-internet-explorer-mode-reinstall-microsoft-edge-with-administrator-privileges"></a>錯誤訊息：「若要在 Internet Explorer 模式中開啟此頁面，請以系統管理員權限重新安裝 Microsoft Edge。」

如果您沒有所有必要的 Windows Update，您可能會看到此錯誤。 請參閱所需 Windows 和 Microsoft Edge 版本[關於 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)中所列的必要條件。

如果您已安裝所有必要的 Windows Update，您可能會在下列情況下看到此錯誤：

- 您使用的是 Canary 通道，預設是在使用者層級安裝。
- 您使用的是 Stable、Beta 或 Dev 通道，提示提高權限時，安裝提高權限已取消。 當您取消提高權限提示時，系統會在使用者層級繼續安裝。
- Internet Explorer 11 已在 Windows 功能中停用。

可能的解決方式：

- 在系統層級執行任何通道的安裝程式：`installer.exe --system-level`。
- 在 Windows 功能中啟用 Internet Explorer 11。

若要檢查 Microsoft Edge 是否安裝在系統層級，請在 Microsoft Edge 網址列中鍵入 "edge://version"。 可執行檔路徑將顯示開頭為 *C:\Program Files* 的路徑，表示是系統安裝。 如果可執行檔路徑開頭為 *C:\Users\*，請解除安裝然後以系統管理員權限重新安裝 Microsoft Edge。

### <a name="error-message-to-open-this-page-in-ie-mode-try-restarting-microsoft-edge"></a>錯誤訊息：「若要在 IE 模式中開啟此頁面，請嘗試重新啟動 Microsoft Edge。」

如果 Internet Explorer 發生未預期的錯誤，您可能會看到此錯誤。 重新啟動 Microsoft Edge 通常可以修正此錯誤。

### <a name="error-message-turn-off-remote-debugging-to-open-this-site-in-ie-mode-otherwise-it-might-not-work-as-expected"></a>錯誤訊息：「請關閉遠端偵錯以在 IE 模式下開啟此網站，否則可能無法如預期運作。」

如果您正在遠端偵錯，且瀏覽至設定為在 IE 模式中執行的網頁，您可能會看到此錯誤。 您可以繼續，但是頁面將會使用 Microsoft Edge 轉譯。

### <a name="error-message-error-could-not-retrieve-emie-site-list"></a>錯誤訊息：「錯誤：無法擷取 EMIE 網站清單。」

您可能會在 *edge://compat/enterprise* 網頁上看到此錯誤，表示網站清單下載失敗。 從 Microsoft Edge 版本 87 開始，當使用 [BlockThirdPartyCookies](https://docs.microsoft.com/deployedge/microsoft-edge-policies#blockthirdpartycookies) 原則封鎖協力廠商要求的 Cookie 時，也不允許使用 HTTP 驗證。 可以使用 [CookiesAllowedForURLs](https://docs.microsoft.com/deployedge/microsoft-edge-policies#cookiesallowedforurls) 原則為裝載 Enterprise Mode Site List 的特定網域允許 Cookie，以確保網站清單下載成功。

## <a name="frequently-asked-questions"></a>常見問題集

### <a name="will-ie-mode-replace-internet-explorer-11"></a>IE 模式是否會取代 Internet Explorer 11？

我們致力於將 Internet Explorer 保持為受支援、可靠且安全的瀏覽器。 Internet Explorer 仍是 Windows 的元件，並遵循其安裝所在作業系統的支援週期。 如需詳細資訊，請參閱[生命週期常見問題 – Internet Explorer](https://support.microsoft.com/help/17454/)。 雖然 Microsoft 繼續支援和更新 Internet Explorer，但最新的功能和平台更新僅適用於 Microsoft Edge。

### <a name="can-i-use-open-with-explorer-or-view-in-file-explorer-in-sharepoint-with-ie-mode"></a>我可以在 SharePoint 中搭配 IE 模式使用 [在檔案總管中開啟] 或 [在檔案總管中檢視] 嗎？

是的，如果這在獨立式 Internet Explorer 11 中能正常運作，在 IE 模式中即能正常運作。 不過，不要使用 [在檔案總管中開啟] 選項，建議用來在 SharePoint 外部管理檔案和資料夾的方法，就是[同步處理您的 SharePoint 檔案](https://support.office.com/en-us/article/sync-sharepoint-files-with-the-onedrive-sync-app-6de9ede8-5b6e-4503-80b2-6190f3354a88)或[在 SharePoint 中移動或複製檔案](https://support.office.com/en-us/article/move-or-copy-files-in-sharepoint-00e2f483-4df3-46be-a861-1f5f0c1a87bc)。

### <a name="does-ie-mode-on-microsoft-edge-support-the-nomerge-option-that-was-supported-in-internet-explorer-11"></a>Microsoft Edge 上的 IE 模式是否支援 Internet Explorer 11中支援的 *nomerge* 選項？

Microsoft Edge 中沒有任何明確的命令列來鏡像 *nomerge* 選項，但我們建議您使用兩種替代方法來提供此功能。

1. 在 Microsoft Edge 中使用設定檔：每個設定檔對應 IE 模式頁面的不同 IE 工作模式，因此其運作方式與 *nomerge* 選項相同。
2. 使用 `--user-data-dir=<path>` 命令列，但每個工作模式的路徑不同。 如有需要，您可以建立一個公用程式供使用者運行，該公用程式可以啟動 Microsoft Edge 並變更工作模式路徑。

如果上述選項都不適用於您的案例，請透過其中一個意見反應通道連絡我們：Microsoft 支援服務或 [TechCommunity 論壇](https://techcommunity.microsoft.com/t5/enterprise/bd-p/EdgeInsiderEnterprise)。

### <a name="can-i-save-links-as-webpages-in-internet-explorer-mode"></a>我是否可以在 Internet Explorer 模式中將連結儲存為網頁？

是的，您可以在 Microsoft Edge 的 Internet Explorer 模式的操作功能表中啟用 [另存目標] 選項。 若要這麼做，請設定位於 [電腦設定] > [系統管理範本] > [Windows 元件] > [Internet Explorer]** 下的群組原則 *「允許在 Internet Explorer 模式中另存目標」*。
儲存機制的運作方式與在 Internet Explorer 中相同，而如果將目標儲存為 HTML 檔案，重新開啟該檔案就會在 Microsoft Edge 中呈現該頁面。
 
請注意，此功能需要下列最低版本的作業系統更新：
- Windows 10 版本 2004、Windows Server 版本 2004、Windows 10 版本 20H2：[KB4580364](https://support.microsoft.com/help/4580364/windows-10-update-kb4580364)
- Windows 10 版本 1903、Windows 10 版本 1909、Windows Server 版本 1903：[KB4580386](https://support.microsoft.com/help/4580386/windows-10-update-kb4580386)
- Windows 10 版本 1809、Windows Server 版本 1809、Windows Server 2019：[KB4580390](https://support.microsoft.com/help/4580390/windows-10-update-kb4580390)
- Windows 10 版本 1803：[KB4586785](https://support.microsoft.com/help/4586785/windows-10-update-kb4586785)
- Windows 10 版本 1607：[KB4586830](https://support.microsoft.com/help/4586830/windows-10-update-kb4586830)
- Windows 10 版本 1507：[KB4586787](https://support.microsoft.com/help/4586787/windows-10-update-kb4586787)


## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [關於 IE 模式](https://docs.microsoft.com/deployedge/edge-ie-mode)
- [其他企業模式資訊](https://docs.microsoft.com/internet-explorer/ie11-deploy-guide/enterprise-mode-overview-for-ie11)
