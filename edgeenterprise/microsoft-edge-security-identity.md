---
title: Microsoft Edge 身分識別支援和設定
ms.author: avvaid
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 身分識別支援和設定
ms.openlocfilehash: 5829082ba52b026acd53164cce82ed04d843d53c10aaff1e1e9552cac82f06f9
ms.sourcegitcommit: d44c0997ffe40d67421312ed96e7766da947eaa0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/05/2021
ms.locfileid: "11727116"
---
# <a name="microsoft-edge-identity-support-and-configuration"></a>Microsoft Edge 身分識別支援和設定

本文介紹 Microsoft Edge 如何使用身分識別來支援同步和單一登入 (SSO) 等功能。 Microsoft Edge 支援使用 Active Directory (AD)、Azure Active Directory (Azure AD) 和 Microsoft 帳戶 (MSA) 登入。 目前 Microsoft Edge 只支援屬於全域雲端或 GCC 主權雲端的 Azure Active Directory（Azure AD）帳戶。 我們正在努力為其他主權雲端新增支援。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="browser-sign-in-and-authenticated-features"></a>瀏覽器登入和驗證功能

Microsoft Edge 支援使用 Azure AD、MSA 或網域帳戶登入瀏覽器設定檔。 登入所用的帳戶類型將決定使用者在 Microsoft Edge 中可使用何種驗證功能。 下表總結了每種帳戶類型的功能支援。

| 功能   | Azure AD Premium | Azure AD Free | 內部部署 AD DS | MSA     |
|----|------------------|---------------|----------------|---------|
| 同步 | 是 | 否 | 否 | 是 |
| SSO 搭配主要重新整理權杖 | 是 | 是 | 否 | 是 |
| 無縫 SSO | 是 | 是 | 是 | 無 |
| 整合式 Windows 驗證 | 是 | 是 | 是 | 無 |
| 企業新索引標籤頁 | 需要 O365 |   需要 O365 | 否 | 無 |
| Microsoft 搜尋 | 需要 O365 | 需要 O365 | 否 | 無 |

## <a name="how-users-can-sign-into-microsoft-edge"></a>使用者登入 Microsoft Edge 的方式

### <a name="automatic-sign-in"></a>自動登入

Microsoft Edge 使用 OS 預設帳戶來自動登入瀏覽器。 依據裝置的設定方式而定，使用者可以使用下列其中一種方法來自動登入 Microsoft Edge。

- **裝置是混合式/AAD-J：** 可在 Win10、舊版 Windows 與對應的伺服器版本上使用。
使用者會自動以其 Azure AD 帳戶登入。
- **裝置為已加入網域：** 可在 Win10、舊版 Windows 與對應的伺服器版本上使用。
根據預設，使用者將不會自動登入。 如果您想要以網域帳戶自動登入使用者，請使用 [ConfigureOnPremisesAccountAutoSignIn](./microsoft-edge-policies.md#configureonpremisesaccountautosignin) 原則。 如果您想要以 Azure AD 帳戶自動登入使用者，請考慮混合式加入您的裝置。
- **OS 預設帳戶為 MSA：** Win10 RS3 (版本 1709/組建10.0.16299) 和更新版本。 這種情況不太可能出現在企業裝置上。 不過，如果 OS 預設帳戶為 MSA，Microsoft Edge 將會使用 MSA 帳戶自動登入。

### <a name="manual-sign-in"></a>手動登入

如果使用者未能自動登入 Microsoft Edge，可以在初次執行體驗、瀏覽器設定或透過開啟身分識別飛出視窗手動登入 Microsoft Edge。

### <a name="managing-browser-sign-in"></a>管理瀏覽器登入

如果您想要管理瀏覽器登入，可以使用下列原則：

- 確保使用者在 Microsoft Edge 一直有工作設定檔。 [請參閱 NonRemovableProfileEnabled (部分機器翻譯)](./microsoft-edge-policies.md#nonremovableprofileenabled)
- 將登入限制為受信任的帳戶組。 [請參閱 RestrictSigninToPattern (英文)](./microsoft-edge-policies.md#restrictsignintopattern)
- 停用或強制瀏覽器登入。 [請參閱 BrowserSignin (英文)](./microsoft-edge-policies.md#browsersignin)

## <a name="browser-to-web-single-sign-on-sso"></a>瀏覽器至網頁單一登入 (SSO)

在某些平臺上，您可以設定 Microsoft Edge 為使用者自動登入網站。 此選項免除他們重新輸入認證的麻煩，方便存取他們的工作網站並提高其生產力。

### <a name="sso-with-primary-refresh-token-prt"></a>SSO 搭配主要重新整理權杖 (PRT)

Microsoft Edge 具有 PRT 式 SSO 原生支援，且不需要擴充。 在 Windows 10 RS3 及更新版本，如果使用者登入其瀏覽器設定檔，就會取得具有前往支援 PRT 式 SSO 網站之 PRT 機制的 SSO。

主要重新整理權杖 (PRT) 是用於在 Windows 10、iOS 和 Android 裝置上驗證的 Azure AD 金鑰。 它支援在這些裝置上使用的應用程式之間進行單一登入 (SSO)。 如需詳細資訊，請參閱[主要重新整理權杖是什麼？](/azure/active-directory/devices/concept-primary-refresh-token)。

### <a name="seamless-sso"></a>無縫 SSO

就像 PRT SSO 一樣，Microsoft Edge 有原生無縫 SSO 支援，且不需要擴充。 在 Windows 10 RS3 及更新版本，如果使用者登入其瀏覽器設定檔，就會取得具有前往支援 PRT 式 SSO 網站之 PRT 機制的 SSO。

無縫單一登入在使用者位於連接到公司網路的公司裝置上時，會自動登入使用者。 啟用後，使用者不需要輸入密碼即可登入 Azure AD。 通常甚至不需要輸入其使用者名稱。 如需詳細資訊，請參閱 [Active Directory 無縫單一登入](/azure/active-directory/hybrid/how-to-connect-sso)。

### <a name="windows-integrated-authentication-wia"></a>Windows 整合式驗證 (WIA)

Microsoft Edge 也支援在組織內部網路中針對使用瀏覽器進行其驗證的任何應用程式，進行驗證要求的 Windows 整合驗證。 所有版本的 Windows 10 和舊版 Windows 都支援這項功能。 根據預設，Microsoft Edge 會使用內部網路區域做為 WIA 的允許清單。 或者，您也可以使用 [AuthServerAllowlist](./microsoft-edge-policies.md#authserverallowlist) 原則來自訂已啟用整合式驗證的伺服器清單。 若使用 macOS，則需要此原則才能啟用整合式驗證。

若要支援 Microsoft Edge (版本 77 及更新版本) 上的 WIA 式 SSO，您可能也需要執行某些伺服器端設定。 您可能必須設定 Active Directory 同盟服務 (AD FS) 的屬性 **WiaSupportedUserAgents** 以新增適用於新版 Microsoft Edge 使用者代理程式字串的支援。 如需如何執行此動作的指示，請參閱[檢視 WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#view-wiasupporteduseragent-settings) 設定以及[變更 WIASupportedUserAgent](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia#change-wiasupporteduseragent-settings) 設定 (英文)。 下列顯示的是 Windows 10 上 Microsoft Edge 使用者代理程式字串的範例，而您可以在這裡深入了解 [Microsoft Edge UA 字串](/microsoft-edge/web-platform/user-agent-string) (英文)。 

UA 字串的以下範例適用於本文發佈時的最新 Dev 通道組建：<br> `"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3951.0 Safari/537.36 Edg/80.0.334.2"`

針對需要委派協商認證的服務，Microsoft Edge 使用 [AuthNegotiateDelegateAllowlist](./microsoft-edge-policies.md#authnegotiatedelegateallowlist) 原則支援 [限制委派]。

## <a name="additional-authentication-concepts"></a>其他驗證概念

### <a name="proactive-authentication"></a>主動式驗證

主動式驗證是對瀏覽器到網站 SSO 的最佳化，可將驗證事先載入到某些第一方網站。 如果使用者使用 Bing 做為搜尋引擎，這會改善網址列的效能。 還會提供使用者個人化和商務用 Microsoft 搜尋 (MSB) 的搜尋結果。 它可讓您允許關鍵服務的驗證，例如 Office 新索引標籤頁面。 您可以使用 [ProactiveAuthEnabled]( /deployedge/microsoft-edge-policies#proactiveauthenabled) 原則對其進行控制。

### <a name="windows-hello-credui-for-ntlm-authentication"></a>NTLM 驗證的 Windows Hello CredUI

當網站嘗試使用 NTLM 或交涉機制來登入使用者且無法使用 SSO 時，我們為使用者提供了可以使用網站共用其 OS 認證，進而得以使用 Windows Hello Cred UI 來滿足身份驗證挑戰的體驗。 Windows 10 版使用者只有在 NTLM 或交涉困難期間才會顯示此登入流程。

### <a name="sign-in-automatically-using-saved-passwords"></a>使用儲存的密碼自動登入

如果使用者在 Microsoft Edge 中儲存密碼，他們可以啟用位於具有儲存其認證的網站時即可自動登入的功能。 使用者可以流覽至 *edge://settings/passwords*來切換此功能。 如果您想要設定此功能，可以使用 [密碼管理員](./microsoft-edge-policies.md#password-manager-and-protection) 原則。

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [影片：Microsoft Edge 和身分識別](microsoft-edge-video-identity.md)
- [身分識別與存取管理](https://www.microsoft.com/security/technology/identity-access-management)
- [身分識別平台](https://developer.microsoft.com/identity)
- [具有 Azure Active Directory 的強身份識別基礎的四個步驟](/azure/active-directory/hybrid/four-steps)