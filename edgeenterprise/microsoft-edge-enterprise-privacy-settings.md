---
title: Microsoft Edge 企業隱私權設定
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge 企業隱私權設定
ms.openlocfilehash: 8ae1737cb066fd473c76f7812c875aceb3cfefb7
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447937"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a>設定 Microsoft Edge 原則以支援企業隱私權

Microsoft 致力於向企業提供必要的資訊和控制，以利於對 Microsoft Edge 中的資料收集進行選擇。

## <a name="overview"></a>概觀

當 Microsoft Edge 部署於 Windows 10 時，預設情況下是會根據使用者的 [[Windows 診斷資料設定]](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 來傳送診斷資料。

當 Microsoft Edge 部署在非 Windows 平台上時，會根據下列群組原則的設定收集診斷資料：

- (已取代) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。 此原則將在 Microsoft Edge 版本 89 中過時。
- (已取代) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。 此原則將在 Microsoft Edge 版本 89 中過時。

前途已取代的原則會在 Windows 10 上由 [允許遙測][](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 取代，而 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則則用於所有其他平台。  

## <a name="configure-policy-settings"></a>設定原則設定

開始前，請下載並使用最新的 Microsoft Edge 原則範本 (如需詳細資訊，請參閱[設定 Microsoft Edge](configure-microsoft-edge.md))。

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a>傳送關於瀏覽器使用狀況的必要和選擇性診斷資料

如果已設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則它優先於 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。

#### <a name="required-and-optional-diagnostic-data"></a>必要和選擇性診斷資料

收集必要診斷資料，以確保 Microsoft Edge 安全、保持最新且如預期執行。

選擇性診斷資料包括有關瀏覽器使用方式、瀏覽的網站和損毀報告，以協助保持 Microsoft Edge 安全、最新且如預期執行，並且用於為所有使用者改善 Microsoft Edge 和其他 Microsoft 產品及服務。

> [!NOTE]
> Windows 10 裝置不支援此原則。 若要控制 Windows 10 上的資料收集，IT 系統管理員必須使用 Windows 診斷資料群組原則。 此原則會是 [允許遙測]**** 或 [允許診斷資料]****，視 Windows 版本而定。 深入了解 [Windows 10 診斷資料收集](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。

使用下列其中一個設定來設定 **DiagnosticData**：

- 關閉 (不建議) (0) 會關閉必要和選擇性診斷資料收集。 
- 必要資料 (1) 會傳送必要診斷資料，但關閉選擇性診斷資料收集。 Microsoft Edge 將傳送確保 Microsoft Edge 安全、處於最新、安全且如預期執行所需的必要診斷資料。 
- 選擇性資料 (2) 會傳送選擇性診斷資料，其中包含有關瀏覽器使用狀況、瀏覽的網站、傳送給 Microsoft 的損毀報告的資料，以協助保持 Microsoft Edge 安全、最新且如預期執行，並且用於為所有使用者改善 Microsoft Edge 和其他 Microsoft 產品及服務。

在 Windows 7、Windows 8/8.1 和 macOS 上，此原則會控制傳送必要和選擇性診斷資料給 Microsoft。

如果未設定或停用此原則，則 Microsoft Edge 將預設為使用者的喜好設定。

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a>(已取代) 啟用使用方式和當機相關的資料報告

**MetricsReportingEnabled** 原則可將 Microsoft Edge 使用方式和當機相關資料的報告傳送給 Microsoft。

Microsoft Edge 會收集確保產品處於最新、安全且如預期執行所需的一組必要資料。 此資料包括從 Microsoft Edge 傳送有關目前資料收集同意、應用程式版本和 Microsoft Edge 安裝狀態的基本裝置連線和設定資訊。可以透過停用原則來關閉此資料收集。

啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。 停用此原則，就不會將此資料傳送到 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

當 Microsoft Edge 在 Windows 10 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。
- 如果啟用此原則，則僅當 Windows 診斷資料設定設為**增強**或**完整**時，Microsoft Edge 才會傳送使用方式資料。
  - 如果已啟用此原則，則只有在也啟用 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) 時，Microsoft Edge 才會傳送使用方式資料。
- 如果停用此原則，Microsoft Edge 將不會傳送使用方式資料。 根據 Windows 診斷資料設定傳送當機相關的資料。 [深入了解 Windows 診斷資料設定](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。

當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。
-  如果已啟用此原則，則只有在也啟用 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) 時，Microsoft Edge 才會傳送使用方式資料。

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a>(已取代) 傳送網站資訊以改善 Microsoft 服務

**SendSiteInformationToImproveServices** 原則會允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善 Microsoft 產品和服務 (如搜尋)。

啟用此原則可傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 停用此原則，就不會傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

當 Microsoft Edge 在 Windows 10 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。
- 如果啟用此原則，而且只有在 Windows 診斷資料設定設為 **[完整]** 時，Microsoft Edge 才會傳送有關造訪網站的資訊。
  - 如果已啟用此原則，則只有在也啟用 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 時，Microsoft Edge 才會傳送使用方式資料。 
- 如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。 [深入了解 Windows 診斷資料設定](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。

當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：

- 如果已啟用此原則，則只有在也啟用 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 時，Microsoft Edge 才會傳送使用方式資料。
- 如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。

## <a name="implementation-details"></a>實作詳細資料

若為非 Windows 10 裝置： 
- 如果已設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則它優先於 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。 
- 如果未設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則 Microsoft Edge 會接聽 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。  

為了讓 Windows 10 了解我們針對 Windows 診斷資料設定採用的相依性實作，下表會指出是否將 **必要**和**選擇性**診斷資料傳送給 Microsoft。

| Windows 診斷資料設定 | 必要診斷資料  | 選擇性診斷資料 |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| 安全性                        | 未傳送                                      | 未傳送                                            |
| 基本                           | 傳送                                      | 未傳送                                            |
| 增強                        | 傳送                                          | 未傳送                                            |
| 完整                            | 傳送                                          | 傳送                                                |

> [!IMPORTANT]
> 針對 Microsoft Edge 版本 86 - 88 (含)，Microsoft Edge 將支援 **MetricsReportingEnabled** 和 **SendSiteInfoToImproveServices**。 在 Microsoft Edge 版本 89 中，**MetricsReportingEnabled** 和 **SendSiteInfoToImproveServices** 將不再受支援，且會在非 Windows 10 平台上預設為 **DiagnosticData**，或 Windows 10 則為 [允許遙測]**** 原則。

## <a name="additional-privacy-policy-options"></a>其他隱私權原則選項

您可能需要考慮以下與資料隱私相關的群組原則：

- 封鎖特定網站上的 Cookie
- 封鎖第三方 Cookie
- 設定不要追蹤
- 停用 InPrivate 模式

## <a name="see-also"></a>請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 原則](microsoft-edge-policies.md)
- [Microsoft Edge 隱私權白皮書](/microsoft-edge/privacy-whitepaper)