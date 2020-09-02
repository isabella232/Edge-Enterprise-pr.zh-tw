---
title: Microsoft Edge 企業隱私權設定
ms.author: likravit
author: dan-wesley
manager: srugh
ms.date: 05/26/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge 企業隱私權設定
ms.openlocfilehash: 2b7a33087ae5110c53d18b3192486d4ae62fa540
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979588"
---
# 設定 Microsoft Edge 原則以支援企業隱私權

Microsoft 致力於向企業提供必要的資訊和控制，以利於對 Microsoft Edge 中的資料收集進行選擇。

## 概觀

根據預設，部署在非 Windows 平台的 Microsoft Edge 不會傳送診斷資料或網站資訊至 Microsoft。 當 Microsoft Edge 部署於 Windows 10 時，預設情況下是會根據使用者的 [[Windows 診斷資料設定]](https://go.microsoft.com/fwlink/?linkid=2099569) 來傳送診斷資料。

您也可以使用以下群組原則，設定 Microsoft Edge 如何處理組織的資料收集：

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。

## 設定原則設定

開始前，請下載並使用最新的 Microsoft Edge 原則範本 (如需詳細資訊，請參閱[設定 Microsoft Edge](configure-microsoft-edge.md))。

### 啟用使用方式和當機相關的資料報告

此原則可將Microsoft Edge 使用方式和當機相關資料的報告傳送到 Microsoft。

Microsoft Edge 會收集一組必要的資料，以確保產品處於最新狀態、安全無虞且運作正常。 此資料包括從 Microsoft Edge 傳送有關目前資料收集同意、應用程式版本和 Microsoft Edge 安裝狀態的基本裝置連線和設定資訊。可以透過停用原則來關閉此資料收集。

啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。 停用此原則，就不會將此資料傳送到 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

當 Microsoft Edge 在 Windows 10 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。
- 如果啟用此原則，則僅當 Windows 診斷資料設定設為**增強**或**完整**時，Microsoft Edge 才會傳送使用方式資料。
- 如果停用此原則，Microsoft Edge 將不會傳送使用方式資料。 根據 Windows 診斷資料設定傳送當機相關的資料。 [深入了解 Windows 診斷資料設定](https://go.microsoft.com/fwlink/?linkid=2099569)。

當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。

### 傳送網站資訊以改善 Microsoft 服務

此原則允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善 Microsoft 產品和服務 (如搜尋)。

啟用此原則可傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 停用此原則，就不會傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。 在這兩種情況下，使用者都無法變更或覆寫設定。

當 Microsoft Edge 在 Windows 10 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。
- 如果啟用此原則，而且只有在 Windows 診斷資料設定設為 **[完整]** 時，Microsoft Edge 才會傳送有關造訪網站的資訊。
- 如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。 [深入了解 Windows 診斷資料設定](https://go.microsoft.com/fwlink/?linkid=2099569)。

當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：

- 如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。

## 實作詳細資料

對於 Windows 10，若要了解我們對 Windows 診斷資料設定上相依性的實作，，下表描述了**啟用使用方式和當機相關的資料報告**以及**傳送網站資訊以改善 Microsoft 服務**未設定時的設定。

| Windows 診斷資料設定 | 啟用使用方式和當機相關的資料報告 | 傳送網站資訊以改善 Microsoft 服務 |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| 安全性                        | 未傳送                                      | 未傳送                                            |
| 基本                           | 未傳送                                      | 未傳送                                            |
| 增強                        | 傳送                                          | 未傳送                                            |
| 完整                            | 傳送                                          | 傳送                                                |

如果您的 Windows 10 設定是根據之前表格的設定錯誤，我們將回復為較小的資料收集設定。

例如：

- 設定 [啟用使用方式和當機相關的資料報告] 原則為 **[啟用]**，但是 Windows 診斷資料設定是設為 **[基本]**。 我們不會傳送使用方式和與當機相關的資料。
- 設定 [傳送網站資訊以改善 Microsoft 服務] 原則為 **[停用]**，但是 Windows 診斷資料設定是設為 **[完整]**。則我們不會傳送有關造訪問網站的資訊。 我們不會傳送有關造訪網站的資訊。

之前設定的正確實作是設定 [啟用使用方式和當機相關的資料報告] 原則為 **[啟用]**，並設定 Windows 診斷資料設定是設為 **[增強]** 或 **[完整]**。

## 其他隱私權原則選項

您可能需要考慮以下與資料隱私相關的群組原則：

- 封鎖特定網站上的 Cookie
- 封鎖第三方 Cookie
- 設定不要追蹤
- 停用 InPrivate 模式

## 也請參閱

- [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)
- [Microsoft Edge 原則](microsoft-edge-policies.md)
- [Microsoft Edge 隱私權白皮書](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
