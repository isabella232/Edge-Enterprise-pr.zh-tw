---
title: Microsoft Edge 端點的允許清單
ms.author: kvice
author: dan-wesley
manager: srugh
ms.date: 06/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: medium
ms.collection: M365-modern-desktop
description: Microsoft Edge 端點的允許清單
ms.openlocfilehash: 735e18e63095405dad4fdd51d51654956b564ca7
ms.sourcegitcommit: bce02a5ce2617bb37ee5d743365d50b5fc8e4aa1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "11641329"
---
# <a name="allow-list-for-microsoft-edge-endpoints"></a>Microsoft Edge 端點的允許清單

Microsoft Edge 需要連線接到網際網路，以支援其功能。 本文識別需要新增到允許清單中的網域 URL，以確保透過防火牆和其他安全機制進行通訊。

> [!NOTE]
> 本文適用於 Microsoft Edge 版本 77 或更新版本。

## <a name="domain-urls-to-allow"></a>允許的網域 URL

允許 Microsoft Edge 的以下網域 URL。

### <a name="update-service"></a>更新服務

Microsoft Edge 用於檢查新更新的服務。

- `https://msedge.api.cdp.microsoft.com`

### <a name="experimentation-and-configuration-service"></a>實驗和設定服務

- `https://config.edge.skype.com`

### <a name="download-locations-for-microsoft-edge"></a>Microsoft Edge 的下載位置

可從初始安裝期間或更新可用時下載 Microsoft Edge 的位置。 下載位置由更新服務確定。

#### <a name="http"></a>HTTP

- `http://msedge.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.f.dl.delivery.mp.microsoft.com`
- `http://msedge.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedge.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedge.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sf.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedge.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > 為了簡化下載位置的允許清單，可以使用萬用字元： `*.dl.delivery.mp.microsoft.com`

### <a name="download-locations-for-microsoft-edge-extensions"></a>Microsoft Edge 延伸模組的下載位置

可從初始安裝期間或更新可用時下載 Microsoft Edge 延伸模組的位置。 下載位置由更新服務確定。

#### <a name="http"></a>HTTP

- `http://msedgeextensions.f.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.f.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.tlu.dl.delivery.mp.microsoft.com`
- `http://msedgeextensions.b.dl.delivery.mp.microsoft.com`

#### <a name="https"></a>HTTPS

- `https://msedgeextensions.sf.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sf.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.tlu.dl.delivery.mp.microsoft.com`
- `https://msedgeextensions.sb.dl.delivery.mp.microsoft.com`

  > [!TIP]
  > 為了簡化下載位置的允許清單，可以使用萬用字元： `*.dl.delivery.mp.microsoft.com`

### <a name="optionally-for-download-delivery-optimization"></a>可選擇下載傳遞最佳化

如需傳遞最佳化的詳細資訊，請參閱 [Windows 10 更新的傳遞最佳化](/windows/deployment/update/waas-delivery-optimization)。

- 用戶端至服務通訊：`*.do.dsp.mp.microsoft.com` (HTTP 連接埠 80，HTTPS 連接埠 443)
- 用戶端至用戶端通訊：應開啟 TCP 連接埠 7680 以供流量傳入

### <a name="sync"></a>Sync

這些端點會管理所同步資料的讀取和寫入、用於護資料的版權管理，並在新的同步資料可用時通知瀏覽器。

- Edge 同步服務端點：

  - `https://edge-enterprise.activity.windows.com`
  - `https://edge.activity.windows.com`

- Azure 資訊保護端點：

  - `https://api.aadrm.com` (適用於多數租用戶)
  - `https://api.aadrm.de` (適用於德國的租用戶)
  - `https://api.aadrm.cn` (適用於中國的租用戶)

- [Windows 通知服務端點](/windows/uwp/design/shell/tiles-and-notifications/firewall-allowlist-config)

## <a name="other-browser-support-services"></a>其他瀏覽器支援服務

為瀏覽器功能 (如追蹤保護、憑證撤銷清單和其他瀏覽器元件更新) 提供中繼資料。 提供可下載的拼字檢查字典和廣告封鎖的封鎖清單。 提供服務以支援瀏覽器功能，如集合、自動填滿和延伸模組存放區。

- `http://edge.microsoft.com/`
- `https://edge.microsoft.com/`

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 文件登陸頁面](./index.yml)
- [管理適用於 Windows 10 企業版版本 1903 的連線端點](/windows/privacy/manage-windows-1903-endpoints)