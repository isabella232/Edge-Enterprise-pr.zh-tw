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
# <span data-ttu-id="a4c28-103">設定 Microsoft Edge 原則以支援企業隱私權</span><span class="sxs-lookup"><span data-stu-id="a4c28-103">Configure Microsoft Edge policies to support enterprise privacy</span></span>

<span data-ttu-id="a4c28-104">Microsoft 致力於向企業提供必要的資訊和控制，以利於對 Microsoft Edge 中的資料收集進行選擇。</span><span class="sxs-lookup"><span data-stu-id="a4c28-104">Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.</span></span>

## <span data-ttu-id="a4c28-105">概觀</span><span class="sxs-lookup"><span data-stu-id="a4c28-105">Overview</span></span>

<span data-ttu-id="a4c28-106">根據預設，部署在非 Windows 平台的 Microsoft Edge 不會傳送診斷資料或網站資訊至 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-106">By default, Microsoft Edge deployed on non-Windows platforms doesn't send diagnostic data or site information to Microsoft.</span></span> <span data-ttu-id="a4c28-107">當 Microsoft Edge 部署於 Windows 10 時，預設情況下是會根據使用者的 [[Windows 診斷資料設定]](https://go.microsoft.com/fwlink/?linkid=2099569) 來傳送診斷資料。</span><span class="sxs-lookup"><span data-stu-id="a4c28-107">When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="a4c28-108">您也可以使用以下群組原則，設定 Microsoft Edge 如何處理組織的資料收集：</span><span class="sxs-lookup"><span data-stu-id="a4c28-108">You can also configure how Microsoft Edge handles data collection for your organization with the following group policies:</span></span>

- <span data-ttu-id="a4c28-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。</span><span class="sxs-lookup"><span data-stu-id="a4c28-109">[MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.</span></span>
- <span data-ttu-id="a4c28-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。</span><span class="sxs-lookup"><span data-stu-id="a4c28-110">[SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.</span></span>

## <span data-ttu-id="a4c28-111">設定原則設定</span><span class="sxs-lookup"><span data-stu-id="a4c28-111">Configure policy settings</span></span>

<span data-ttu-id="a4c28-112">開始前，請下載並使用最新的 Microsoft Edge 原則範本 (如需詳細資訊，請參閱[設定 Microsoft Edge](configure-microsoft-edge.md))。</span><span class="sxs-lookup"><span data-stu-id="a4c28-112">Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)</span></span>

### <span data-ttu-id="a4c28-113">啟用使用方式和當機相關的資料報告</span><span class="sxs-lookup"><span data-stu-id="a4c28-113">Enable usage and crash-related data reporting</span></span>

<span data-ttu-id="a4c28-114">此原則可將Microsoft Edge 使用方式和當機相關資料的報告傳送到 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-114">This policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.</span></span>

<span data-ttu-id="a4c28-115">Microsoft Edge 會收集一組必要的資料，以確保產品處於最新狀態、安全無虞且運作正常。</span><span class="sxs-lookup"><span data-stu-id="a4c28-115">Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing properly.</span></span> <span data-ttu-id="a4c28-116">此資料包括從 Microsoft Edge 傳送有關目前資料收集同意、應用程式版本和 Microsoft Edge 安裝狀態的基本裝置連線和設定資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c28-116">This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge.</span></span><span data-ttu-id="a4c28-117">可以透過停用原則來關閉此資料收集。</span><span class="sxs-lookup"><span data-stu-id="a4c28-117"> This data collection can be turned off by disabling the policy.</span></span>

<span data-ttu-id="a4c28-118">啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-118">Enable this policy to send reporting of usage and crash-related data to Microsoft.</span></span> <span data-ttu-id="a4c28-119">停用此原則，就不會將此資料傳送到 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-119">Disable this policy to not send the data to Microsoft.</span></span> <span data-ttu-id="a4c28-120">在這兩種情況下，使用者都無法變更或覆寫設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-120">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="a4c28-121">當 Microsoft Edge 在 Windows 10 上執行時：</span><span class="sxs-lookup"><span data-stu-id="a4c28-121">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="a4c28-122">如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-122">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="a4c28-123">如果啟用此原則，則僅當 Windows 診斷資料設定設為**增強**或**完整**時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="a4c28-123">If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.</span></span>
- <span data-ttu-id="a4c28-124">如果停用此原則，Microsoft Edge 將不會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="a4c28-124">If this policy is disabled, Microsoft Edge will not send usage data.</span></span> <span data-ttu-id="a4c28-125">根據 Windows 診斷資料設定傳送當機相關的資料。</span><span class="sxs-lookup"><span data-stu-id="a4c28-125">Crash-related data is sent based on the Windows Diagnostic data setting.</span></span> <span data-ttu-id="a4c28-126">[深入了解 Windows 診斷資料設定](https://go.microsoft.com/fwlink/?linkid=2099569)。</span><span class="sxs-lookup"><span data-stu-id="a4c28-126">[Learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="a4c28-127">當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：</span><span class="sxs-lookup"><span data-stu-id="a4c28-127">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="a4c28-128">如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-128">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

### <span data-ttu-id="a4c28-129">傳送網站資訊以改善 Microsoft 服務</span><span class="sxs-lookup"><span data-stu-id="a4c28-129">Send site information to improve Microsoft services</span></span>

<span data-ttu-id="a4c28-130">此原則允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善 Microsoft 產品和服務 (如搜尋)。</span><span class="sxs-lookup"><span data-stu-id="a4c28-130">This policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.</span></span>

<span data-ttu-id="a4c28-131">啟用此原則可傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-131">Enable this policy to send information about websites visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="a4c28-132">停用此原則，就不會傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4c28-132">Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="a4c28-133">在這兩種情況下，使用者都無法變更或覆寫設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-133">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="a4c28-134">當 Microsoft Edge 在 Windows 10 上執行時：</span><span class="sxs-lookup"><span data-stu-id="a4c28-134">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="a4c28-135">如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-135">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="a4c28-136">如果啟用此原則，而且只有在 Windows 診斷資料設定設為 **[完整]** 時，Microsoft Edge 才會傳送有關造訪網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c28-136">If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.</span></span>
- <span data-ttu-id="a4c28-137">如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c28-137">If this policy is disabled, Microsoft Edge will not send info about websites visited.</span></span> <span data-ttu-id="a4c28-138">[深入了解 Windows 診斷資料設定](https://go.microsoft.com/fwlink/?linkid=2099569)。</span><span class="sxs-lookup"><span data-stu-id="a4c28-138">To [learn more about Windows Diagnostic data settings](https://go.microsoft.com/fwlink/?linkid=2099569).</span></span>

<span data-ttu-id="a4c28-139">當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：</span><span class="sxs-lookup"><span data-stu-id="a4c28-139">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="a4c28-140">如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-140">If this policy isn't configured, Microsoft Edge will default to the user's preference.</span></span>

## <span data-ttu-id="a4c28-141">實作詳細資料</span><span class="sxs-lookup"><span data-stu-id="a4c28-141">Implementation details</span></span>

<span data-ttu-id="a4c28-142">對於 Windows 10，若要了解我們對 Windows 診斷資料設定上相依性的實作，，下表描述了**啟用使用方式和當機相關的資料報告**以及**傳送網站資訊以改善 Microsoft 服務**未設定時的設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-142">For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table describes our configuration if **Enable usage and crash-related data reporting** and **Send site information to improve Microsoft services** were not configured.</span></span>

| <span data-ttu-id="a4c28-143">Windows 診斷資料設定</span><span class="sxs-lookup"><span data-stu-id="a4c28-143">Windows Diagnostic data setting</span></span> | <span data-ttu-id="a4c28-144">啟用使用方式和當機相關的資料報告</span><span class="sxs-lookup"><span data-stu-id="a4c28-144">Enable usage and crash-related data reporting</span></span> | <span data-ttu-id="a4c28-145">傳送網站資訊以改善 Microsoft 服務</span><span class="sxs-lookup"><span data-stu-id="a4c28-145">Send site information to improve Microsoft services</span></span> |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="a4c28-146">安全性</span><span class="sxs-lookup"><span data-stu-id="a4c28-146">Security</span></span>                        | <span data-ttu-id="a4c28-147">未傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-147">Not sent</span></span>                                      | <span data-ttu-id="a4c28-148">未傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-148">Not sent</span></span>                                            |
| <span data-ttu-id="a4c28-149">基本</span><span class="sxs-lookup"><span data-stu-id="a4c28-149">Basic</span></span>                           | <span data-ttu-id="a4c28-150">未傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-150">Not sent</span></span>                                      | <span data-ttu-id="a4c28-151">未傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-151">Not sent</span></span>                                            |
| <span data-ttu-id="a4c28-152">增強</span><span class="sxs-lookup"><span data-stu-id="a4c28-152">Enhanced</span></span>                        | <span data-ttu-id="a4c28-153">傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-153">Sent</span></span>                                          | <span data-ttu-id="a4c28-154">未傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-154">Not sent</span></span>                                            |
| <span data-ttu-id="a4c28-155">完整</span><span class="sxs-lookup"><span data-stu-id="a4c28-155">Full</span></span>                            | <span data-ttu-id="a4c28-156">傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-156">Sent</span></span>                                          | <span data-ttu-id="a4c28-157">傳送</span><span class="sxs-lookup"><span data-stu-id="a4c28-157">Sent</span></span>                                                |

<span data-ttu-id="a4c28-158">如果您的 Windows 10 設定是根據之前表格的設定錯誤，我們將回復為較小的資料收集設定。</span><span class="sxs-lookup"><span data-stu-id="a4c28-158">If your configurations for Windows 10 are misconfigured in accordance with the preceding table, we will fall back to the lesser data collection setting.</span></span>

<span data-ttu-id="a4c28-159">例如：</span><span class="sxs-lookup"><span data-stu-id="a4c28-159">For example:</span></span>

- <span data-ttu-id="a4c28-160">設定 [啟用使用方式和當機相關的資料報告] 原則為 **[啟用]**，但是 Windows 診斷資料設定是設為 **[基本]**。</span><span class="sxs-lookup"><span data-stu-id="a4c28-160">You set the "Enable usage and crash-related data reporting" policy to **Enabled** but the Windows Diagnostic data setting is set to **Basic**.</span></span> <span data-ttu-id="a4c28-161">我們不會傳送使用方式和與當機相關的資料。</span><span class="sxs-lookup"><span data-stu-id="a4c28-161">We won't send usage and crash-related data.</span></span>
- <span data-ttu-id="a4c28-162">設定 [傳送網站資訊以改善 Microsoft 服務] 原則為 **[停用]**，但是 Windows 診斷資料設定是設為 **[完整]**。則我們不會傳送有關造訪問網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c28-162">You set the "Send site information to improve Microsoft services" policy to **Disabled** but the Windows Diagnostic data setting is set to **Full**.</span></span> <span data-ttu-id="a4c28-163">我們不會傳送有關造訪網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4c28-163">We won't send information about the sites that are visited.</span></span>

<span data-ttu-id="a4c28-164">之前設定的正確實作是設定 [啟用使用方式和當機相關的資料報告] 原則為 **[啟用]**，並設定 Windows 診斷資料設定是設為 **[增強]** 或 **[完整]**。</span><span class="sxs-lookup"><span data-stu-id="a4c28-164">The correct implementation for the previous settings is to set the "Enable usage and crash-related data reporting" policy to **Enabled** and set the Windows Diagnostic data setting to **Enhanced** or **Full**.</span></span>

## <span data-ttu-id="a4c28-165">其他隱私權原則選項</span><span class="sxs-lookup"><span data-stu-id="a4c28-165">Additional privacy policy options</span></span>

<span data-ttu-id="a4c28-166">您可能需要考慮以下與資料隱私相關的群組原則：</span><span class="sxs-lookup"><span data-stu-id="a4c28-166">You may want to consider the following group policies related to data privacy:</span></span>

- <span data-ttu-id="a4c28-167">封鎖特定網站上的 Cookie</span><span class="sxs-lookup"><span data-stu-id="a4c28-167">Block cookies on specific sites</span></span>
- <span data-ttu-id="a4c28-168">封鎖第三方 Cookie</span><span class="sxs-lookup"><span data-stu-id="a4c28-168">Block third-party cookies</span></span>
- <span data-ttu-id="a4c28-169">設定不要追蹤</span><span class="sxs-lookup"><span data-stu-id="a4c28-169">Configure Do Not Track</span></span>
- <span data-ttu-id="a4c28-170">停用 InPrivate 模式</span><span class="sxs-lookup"><span data-stu-id="a4c28-170">Disable InPrivate mode</span></span>

## <span data-ttu-id="a4c28-171">也請參閱</span><span class="sxs-lookup"><span data-stu-id="a4c28-171">See also</span></span>

- [<span data-ttu-id="a4c28-172">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="a4c28-172">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a4c28-173">Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="a4c28-173">Microsoft Edge policies</span></span>](microsoft-edge-policies.md)
- [<span data-ttu-id="a4c28-174">Microsoft Edge 隱私權白皮書</span><span class="sxs-lookup"><span data-stu-id="a4c28-174">Microsoft Edge Privacy Whitepaper</span></span>](https://docs.microsoft.com/microsoft-edge/privacy-whitepaper)
