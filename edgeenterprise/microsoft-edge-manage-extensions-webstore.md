---
title: 自我裝載 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: 瞭解如何在企業中封裝和自我裝載 Microsoft Edge 擴充功能。
ms.openlocfilehash: 8b0e9ed346848f7ee9330c51f6a1c9274df89371
ms.sourcegitcommit: 8968f3107291935ed9adc84bba348d5f187eadae
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/12/2021
ms.locfileid: "11978907"
---
# <a name="self-host-microsoft-edge-extensions"></a>自我裝載 Microsoft Edge 擴充功能

本文提供封裝擴充功能以在您自己的 WebStore 上裝載的基本指引。 它也包含如何在您的組織內將擴充功能部署至裝置和使用者的指示。

## <a name="prerequisites"></a>必要條件

若要自我裝載您自己的擴充功能，您必須為擴充功能及其資訊清單檔案提供您自己的虛擬主機服務。

 下列步驟假設您已建立擴充功能、具有 XML 檔案的一些經驗、具備設定群組原則的工作知識，以及瞭解如何使用 Windows 登錄。

## <a name="publish-an-extension"></a>發佈擴充功能

發佈擴充功能之前，需要將其封裝至 CRX (Chrome 延伸) 檔案。 使用下列作為指南的步驟以將擴充功能封裝為 CRX 檔案。

1. 在 Microsoft Edge 網址列中，請移至 *edge://extensions*，並開啟 **開發人員模式** (如果尚未啟用)。
2. 在 **已安裝的擴充功能**底下，按一下 **封裝擴充功能** 以建立 CRX 檔案。
3. 使用 **封裝擴充功能** 對話方塊以尋找具有擴充功能來源的目錄。 選取目錄，然後按一下 **封裝擴充功能**。  這會建立您的 CRX 檔案和 PEM 檔案。 儲存 PEM 檔案，因為需要將擴充功能更新版本。 下一個螢幕擷取畫面顯示 **封裝擴充功能** 對話方塊，用於尋找擴充功能的根目錄。

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-pack-dialog.png" alt-text="用於尋找擴充功能的原始碼的封裝擴充功能對話方塊。":::

   > [!IMPORTANT]
   > 將 PEM 檔案儲存在安全的位置，因為它是擴充功能的金鑰，而且未來更新需要它。

4. 將 CRX 檔案拖曳到擴充功能視窗中並確定已載入該檔案。
5. 測試擴充功能，並記錄識別碼欄位 (這是 CRX 識別碼) 和版本號碼。 您稍後會需要此資訊。 下一個螢幕擷取畫面顯示具有 CRX 識別碼的測試擴充功能。

   :::image type="content" source="media/microsoft-edge-manage-extensions-webstore/manage-extensions-test-extension.png" alt-text="顯示 CRX 識別碼的擴充功能範例":::

6. 將 CRX 檔案上傳至主機，並注意要下載的 URL 位置。 這項資訊對 XML 資訊清單檔案是必須的。
7. 若要使用應用程式/擴充功能識別碼、下載 URL 和版本以建立資訊清單 XML 檔案，請定義以下欄位：  

   - **appid** - 步驟 5 的擴充功能識別碼
   - **codebase** - 步驟 6 中的 CRX 檔案下載位置
   - **版本** - 應用程式/擴充功能的版本，應符合擴充功能資訊清單中的指定版本。

   下一個程式碼片段會顯示 XML 資訊清單檔案的範例。

   ```xml
   <?xml version='1.0' encoding='UTF-8'?> 
   <gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'> 
     <app appid='ekilpdeokbpjmminmhfcgkncmmohmfeb'> 
     <updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.0' /> 
     </app> 
   </gupdate> 
   ```

   如需詳細資訊，請參閱 [Microsoft Edge 中自動更新擴充功能 - Microsoft Edge 開發](/microsoft-edge/extensions-chromium/enterprise/auto-update)。

8. 將已完成的 XML 檔案上傳至可從中下載的位置，並記錄此 URL。 當您使用群組原則安裝擴充功能時會需要此 URL。 請參閱 [發佈私人託管的擴充功能](#distribute-a-privately-hosted-extension)。

   > [!IMPORTANT]
   > 擴充功能的主機位置不需要驗證。 無論使用者裝置的可能使用位置在何處，都必須能夠存取該裝置。

## <a name="publish-updates-to-an-extension"></a>發佈更新至擴充功能

變更和測試更新的擴充功能之後，您就可以發佈它。 使用下列步驟做為發佈更新的指南。

1. 使用下列語法，將擴充功能之 manifest.JSON 檔案中的版本號碼進行變更以提升為較高的版本號碼：`"version":"versionString"`。 如果「版本」：「1.0」，之後您就可以更新為「版本」：「1.1」或任何高於「1.0」的版本號碼。
2. 更新 XML 檔案中的 `<updatecheck>`「版本」，以符合您在上一個步驟中放入資訊清單檔案中的號碼。 例如：<br>`<updatecheck codebase='https://app.somecompany.com/extensionfolder/helloworld.crx' version='1.1' />`
3. 建立包含新增變更的 CRX 檔案。 請前往 *edge://extensions* 並啟用 **開發人員模式**。
4. 按一下 **封裝擴充功能**，然後前往擴充功能來源的目錄。

   > [!IMPORTANT]
   > 使用第一次建立 CRX 檔案時產生並儲存的相同 PEM 檔案。 如果您沒有使用相同的 PEM 檔案，擴充功能的應用程式識別碼將會變更，並將更新會視為新的擴充功能。

5. 將 CRX 檔案拖放到擴充功能視窗，並確認已載入該檔案。 此作業之後，擴充功能將會停用。 若要啟用，請新增擴充模組的 CRX 識別碼至 ExtensionInstallAllowList 策略。 
6. 測試更新的擴充功能。
7. 將以更新副檔名的新檔案取代舊的 CRX 檔案和 XML 檔案。

擴充功能的變更將在下一個原則同步週期中選取。 如需更新擴充功能的詳細資訊，請參閱：[更新 URL](/microsoft-edge/extensions-chromium/enterprise/auto-update#update-url) 和 [更新資訊清單](/microsoft-edge/extensions-chromium/enterprise/auto-update#updated-manifest)。

## <a name="distribute-a-privately-hosted-extension"></a>發佈私人託管的擴充功能。

您可以共用 CRX 檔案託管位置的連結，而且一旦使用者在瀏覽器中輸入 URL，就會下載並安裝此擴充功能。 使用者可以從 edge://extensions 網頁啟用此擴充功能。 若要允許使用者安裝自我託管的擴充功能，您必須將擴充 CRX ID 新增到 [ExtensionInstallAllowList](/deployedge/microsoft-edge-policies#extensioninstallallowlist) 政策，並新增 CRX 檔案託管位置的 URL 到 [ExtensionInstallSources](/deployedge/microsoft-edge-policies#extensioninstallsources) 策略。

或者，您可以使用群組原則 [ExtensionInstallForceList](/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension) 以強制安裝擴充功能至使用者的裝置上。

您可以將這些原則套用至您所選取的使用者、裝置或兩者皆套用。 請記住，此原則更新是非即時性的，而且需要一些時間讓該原則設定生效。

## <a name="see-also"></a>另請參閱

- [管理企業中的 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions.md)
- [使用群組原則以管理 Microsoft Edge 擴充功能](microsoft-edge-manage-extensions-policies.md)
- [ExtensionSettings 原則的詳細指南](microsoft-edge-manage-extensions-ref-guide.md)
- [Microsoft Edge 擴充功能常見問題集](microsoft-edge-manage-extensions-faq.md)
- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
