---
title: 設定適用於 Windows 的 Microsoft Edge
ms.author: brianalt
author: kelleyvice-msft
manager: laurawi
ms.date: 06/28/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 在 Windows 裝置上設定 Microsoft Edge 原則設定
ms.openlocfilehash: a962a42c8dc40589c9275625007827ec2f76450002115a0c6d8c9e2d733df2e8
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11725242"
---
# <a name="configure-microsoft-edge-policy-settings-on-windows"></a>在 Windows 上設定 Microsoft Edge 原則設定

使用以下資訊，在 Windows 裝置上設定 Microsoft Edge 原則設定。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="configure-policy-settings-on-windows"></a>在 Windows 上進行原則設定

您可以使用_群組原則物件 (GPO)_ 來進行 Microsoft Edge 的原則設定，以及管理所有 Windows 版本的 Microsoft Edge Update。 您也可以透過加入 Microsoft Active Directory 網域之 Windows 裝置的登錄或 Microsoft Intune 中為裝置管理註冊的 Windows 10 專業版或企業執行個體來佈建原則。 若要使用群組原則物件來設定 Microsoft Edge，請安裝_系統管理範本_，以將 Microsoft Edge 的規則和設定新增到 Active Directory 網域中的群組原則集中存放區或個別電腦上的原則定義範本資料夾，然後設定您要設定的特定原則。

如果您希望在網域層級管理原則，可以使用 Active Directory 群組原則來設定 Microsoft Edge 原則設定。 這使您能夠全域管理原則設定，將不同的原則設定定位到特定 OU，或使用 WMI 篩選僅將設定套用至特定查詢傳回的使用者或電腦。 如果要在個別電腦上設定原則，則可使用目標電腦上的本機群組原則編輯器，套用僅影響本機裝置的原則設定。

Microsoft Edge 同時支援_強制_原則和_建議_原則。 強制原則會覆寫使用者喜好設定並阻止使用者變更喜好設定，而建議原則提供可由使用者覆寫的預設設定。 大部分原則僅是強制的；子集是強制和建議的。 如果同時設定了兩個版本的原則，則強制設定優先。 建議的原則只有在使用者尚未修改設定時才生效。

>[!TIP]
> 您可以使用 Microsoft Intune 來設定 Microsoft Edge 原則設定。 如需詳細資訊，請參閱[使用 Microsoft Intune 設定 Microsoft Edge](configure-edge-with-intune.md)。

Microsoft Edge 有兩個系統管理範本，兩種範本都可以在電腦或 Active Directory 網域層級套用：

- *msedge.admx*，[設定 Microsoft Edge 設定](microsoft-edge-policies.md)
- *msedgeupdate.admx*，[管理 Microsoft Edge Update](microsoft-edge-update-policies.md)。

若要開始使用，請下載並安裝 Microsoft Edge 系統管理範本。

### <a name="1-download-and-install-the-microsoft-edge-administrative-template"></a>1. 下載並安裝 Microsoft Edge 系統管理範本

如果要在 Active Directory 中設定 Microsoft Edge 原則設定，請將檔案下載到可從網域控制站或安裝了遠端伺服器管理工具 (RSAT) 的工作站存取的網路位置。 若要在個別電腦上設定，只需將檔案下載到該電腦上即可。

將系統管理範本檔案新增到適當位置時，Microsoft Edge 原則設定可立即在群組原則編輯器中使用。

移至 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (*MicrosoftEdgePolicyTemplates.cab*)，並解壓縮內容。

#### <a name="add-the-administrative-template-to-active-directory"></a>將系統管理範本新增到 Active Directory

1. 在網域控制站或具有 RSAT 的工作站上，瀏覽到網域中任何網域控制站上的 **PolicyDefinition** 資料夾 (也稱為_集中存放區_)。 對於舊版 Windows 伺服器，您可能需要建立 PolicyDefinition 資料夾。 如需詳細資訊，請參閱[如何在 Windows 中建立及管理群組原則系統管理範本的集中存放區](https://support.microsoft.com/help/3087759/how-to-create-and-manage-the-central-store-for-group-policy-administra)。
2. 開啟 *MicrosoftEdgePolicyTemplates* 並移至 **windows** > **admx**。
3. 將 *msedge.admx* 檔案複製到 PolicyDefinition 資料夾。 (範例：%systemroot%\sysvol\domain\policies\PolicyDefinitions)
4. 在 *admx* 資料夾中，開啟適當的語言資料夾。 例如，如果您在美國，則開啟 **en-US** 資料夾。
5. 將 *msedge.adml* 檔案複製到 PolicyDefinition 資料夾中的相符語言資料夾。 如果資料夾不存在，請加以建立。 (範例：%systemroot%\sysvol\domain\policies\PolicyDefinitions\EN-US)
6. 如果您的網域有多個網域控制站，則新的 ADMX 檔案將在下一個網域複寫間隔時複寫到它們上。
7. 若要確認是否正確載入檔案，請從 Windows 系統管理工具開啟**群組原則管理編輯器**並展開**電腦設定** > **原則** > **系統管理範本** > **Microsoft Edge**。 您應該會看到一個或多個 Microsoft Edge 節點，如下所示。

    ![Microsoft Edge 原則](./media/configure-microsoft-edge/edge-gpo-policies.png)

#### <a name="add-the-administrative-template-to-an-individual-computer"></a>將系統管理範本新增到個別電腦

1. 在目標電腦上，開啟 *MicrosoftEdgePolicyTemplates* 並移至 **windows** > **admx**。
2. 將 *msedge.admx* 檔案複製到原則定義範本資料夾。 (範例：C:\Windows\PolicyDefinitions)
3. 在 *admx* 資料夾中，開啟適當的語言資料夾。 例如，如果您在美國，則開啟 **en-US** 資料夾。
4. 將 *msedge.adml* 檔案複製到原則定義資料夾中的相符語言資料夾。 (範例：C:\Windows\PolicyDefinitions\en-US)
5. 若要確認是否正確載入檔案，請直接開啟本機群組原則編輯器 (Windows 鍵 + R 並輸入 gpedit.msc) 或開啟 MMC 並載入 [本機群組原則編輯器] 嵌入式管理單元。 如果發生錯誤，通常是因為檔案位於錯誤的位置。

### <a name="2-set-mandatory-or-recommended-policies"></a>2. 設定強制或建議原則

您可以設定強制或建議原則，以便使用群組原則編輯器為 Active Directory 和個別電腦設定 Microsoft Edge。 您可以透過選取適當的節點 (如下所述)，將原則設定的範圍限定為**電腦設定**或**使用者設定**。

- 若要設定強制原則，請開啟群組原則編輯器並移至 (**電腦設定**或**使用者設定**) > **原則** > **系統管理範本** > **Microsoft Edge**。
- 若要設定建議原則，請開啟群組原則編輯器並移至 (**電腦設定**或**使用者設定**) > **原則** > **系統管理範本** > **Microsoft Edge – 預設設定 (使用者可以覆寫)**。

  ![開啟群組原則編輯器](./media/configure-microsoft-edge/edge-ad-policy.png)

### <a name="3-test-your-policies"></a>3. 測試您的原則

在目標用戶端裝置上，開啟 Microsoft Edge 並瀏覽至 **edge://policy** 以查看套用的所有原則。 如果是在本機電腦上套用原則設定，原則應會立即顯示。 如果在進行原則設定時 Microsoft Edge 是開啟的，則可能需要關閉並重新開啟 Microsoft Edge。

![在瀏覽器中檢視設定的原則](./media/configure-microsoft-edge/edge-gpEdit.png)

對於 Active Directory 群組原則設定，原則設定會依照網域管理員定義的定期間隔傳播到網域電腦，目標電腦可能不會馬上收到原則更新。 若要手動重新整理目標電腦上的 Active Directory 群組原則設定，請從目標電腦的命令提示字元或 PowerShell 工作階段執行以下命令：

``` powershell
gpupdate /force
```

您可能需要關閉並重新開啟 Microsoft Edge，新原則才會出現。

您還可以在目標電腦上使用 REGEDIT.exe 來檢視儲存群組原則設定的登錄設定。 這些設定位於登錄路徑 **HKLM\SOFTWARE\Policies\Microsoft\Edge**。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [使用 Intune 進行 Windows 的設定](configure-edge-with-intune.md)
- [進行 macOS 的設定](configure-microsoft-edge-on-mac.md)
- [瀏覽 Microsoft Edge 企業原則](microsoft-edge-policies.md)


