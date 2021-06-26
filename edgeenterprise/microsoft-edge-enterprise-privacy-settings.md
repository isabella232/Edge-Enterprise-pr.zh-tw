---
title: Microsoft Edge 企業隱私權設定
ms.author: collw
author: dan-wesley
manager: srugh
ms.date: 09/09/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 設定 Microsoft Edge 企業隱私權設定
ms.openlocfilehash: 9af3ce14b9ee717d4c64fa3b920e8c63224613e6
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11617773"
---
# <a name="configure-microsoft-edge-policies-to-support-enterprise-privacy"></a><span data-ttu-id="35768-103">設定 Microsoft Edge 原則以支援企業隱私權</span><span class="sxs-lookup"><span data-stu-id="35768-103">Configure Microsoft Edge policies to support enterprise privacy</span></span>

<span data-ttu-id="35768-104">Microsoft 致力於向企業提供必要的資訊和控制，以利於對 Microsoft Edge 中的資料收集進行選擇。</span><span class="sxs-lookup"><span data-stu-id="35768-104">Microsoft is committed to providing enterprises with the information and controls needed to make choices about data collection in Microsoft Edge.</span></span>

## <a name="overview"></a><span data-ttu-id="35768-105">概觀</span><span class="sxs-lookup"><span data-stu-id="35768-105">Overview</span></span>

<span data-ttu-id="35768-106">當 Microsoft Edge 部署於 Windows 10 時，預設情況下是會根據使用者的 [[Windows 診斷資料設定]](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 來傳送診斷資料。</span><span class="sxs-lookup"><span data-stu-id="35768-106">When Microsoft Edge is deployed on Windows 10, the default is to send diagnostic data based on the users' [Windows Diagnostic data setting](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).</span></span>

<span data-ttu-id="35768-107">當 Microsoft Edge 部署在非 Windows 平台上時，會根據下列群組原則的設定收集診斷資料：</span><span class="sxs-lookup"><span data-stu-id="35768-107">When Microsoft Edge is deployed on non-Windows platforms, diagnostic data is collected according to the settings of the following group policies:</span></span>

- <span data-ttu-id="35768-108">(已取代) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - 啟用使用方式和當機相關的資料報告。</span><span class="sxs-lookup"><span data-stu-id="35768-108">(DEPRECATED) [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) - Enable usage and crash-related data reporting.</span></span> <span data-ttu-id="35768-109">此原則將在 Microsoft Edge 版本 89 中過時。</span><span class="sxs-lookup"><span data-stu-id="35768-109">This policy will be obsolete in Microsoft Edge version 89.</span></span>
- <span data-ttu-id="35768-110">(已取代) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - 傳送網站資訊以改善 Microsoft 服務。</span><span class="sxs-lookup"><span data-stu-id="35768-110">(DEPRECATED) [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.</span></span> <span data-ttu-id="35768-111">此原則將在 Microsoft Edge 版本 89 中過時。</span><span class="sxs-lookup"><span data-stu-id="35768-111">This policy will be obsolete in Microsoft Edge version 89.</span></span>

<span data-ttu-id="35768-112">前途已取代的原則會在 Windows 10 上由 [允許遙測][](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) 取代，而 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則則用於所有其他平台。</span><span class="sxs-lookup"><span data-stu-id="35768-112">The preceding deprecated policies are replaced by [Allow Telemetry](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) on Windows 10, and [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy for all other platforms.</span></span>  

## <a name="configure-policy-settings"></a><span data-ttu-id="35768-113">設定原則設定</span><span class="sxs-lookup"><span data-stu-id="35768-113">Configure policy settings</span></span>

<span data-ttu-id="35768-114">開始前，請下載並使用最新的 Microsoft Edge 原則範本 (如需詳細資訊，請參閱[設定 Microsoft Edge](configure-microsoft-edge.md))。</span><span class="sxs-lookup"><span data-stu-id="35768-114">Before you begin, download and use the latest Microsoft Edge Policy Template (For more information, see [Configure Microsoft Edge](configure-microsoft-edge.md).)</span></span>

### <a name="send-required-and-optional-diagnostic-data-about-browser-usage"></a><span data-ttu-id="35768-115">傳送關於瀏覽器使用狀況的必要和選擇性診斷資料</span><span class="sxs-lookup"><span data-stu-id="35768-115">Send required and optional diagnostic data about browser usage</span></span>

<span data-ttu-id="35768-116">如果已設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則它優先於 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。</span><span class="sxs-lookup"><span data-stu-id="35768-116">If the [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy is configured, it takes precedence over [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).</span></span>

#### <a name="required-and-optional-diagnostic-data"></a><span data-ttu-id="35768-117">必要和選擇性診斷資料</span><span class="sxs-lookup"><span data-stu-id="35768-117">Required and optional diagnostic data</span></span>

<span data-ttu-id="35768-118">收集必要診斷資料，以確保 Microsoft Edge 安全、保持最新且如預期執行。</span><span class="sxs-lookup"><span data-stu-id="35768-118">Required diagnostic data is collected to keep Microsoft Edge secure, up to date and performing as expected.</span></span>

<span data-ttu-id="35768-119">選擇性診斷資料包括有關瀏覽器使用方式、瀏覽的網站和損毀報告，以協助保持 Microsoft Edge 安全、最新且如預期執行，並且用於為所有使用者改善 Microsoft Edge 和其他 Microsoft 產品及服務。</span><span class="sxs-lookup"><span data-stu-id="35768-119">Optional diagnostic data includes data about how you use the browser, websites you visit and crash reports to help keep Microsoft Edge secure, up to date, and performing as expected and is used to improve Microsoft Edge and other Microsoft products and services for all users.</span></span>

> [!NOTE]
> <span data-ttu-id="35768-120">Windows 10 裝置不支援此原則。</span><span class="sxs-lookup"><span data-stu-id="35768-120">This policy isn't supported on Windows 10 devices.</span></span> <span data-ttu-id="35768-121">若要控制 Windows 10 上的資料收集，IT 系統管理員必須使用 Windows 診斷資料群組原則。</span><span class="sxs-lookup"><span data-stu-id="35768-121">To control data collection on Windows 10, IT admins must use the Windows diagnostic data group policy.</span></span> <span data-ttu-id="35768-122">此原則會是 [允許遙測]\*\*\*\* 或 [允許診斷資料]\*\*\*\*，視 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="35768-122">This policy will either be to **Allow Telemetry** or to **Allow Diagnostic Data**, depending on the version of Windows.</span></span> <span data-ttu-id="35768-123">深入了解 [Windows 10 診斷資料收集](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。</span><span class="sxs-lookup"><span data-stu-id="35768-123">Learn more about [Windows 10 diagnostic data collection](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).</span></span>

<span data-ttu-id="35768-124">使用下列其中一個設定來設定 **DiagnosticData**：</span><span class="sxs-lookup"><span data-stu-id="35768-124">Use one of the following settings to configure **DiagnosticData**:</span></span>

- <span data-ttu-id="35768-125">關閉 (不建議) (0) 會關閉必要和選擇性診斷資料收集。</span><span class="sxs-lookup"><span data-stu-id="35768-125">Off (Not recommended) (0) turns off required and optional diagnostic data collection.</span></span> 
- <span data-ttu-id="35768-126">必要資料 (1) 會傳送必要診斷資料，但關閉選擇性診斷資料收集。</span><span class="sxs-lookup"><span data-stu-id="35768-126">Required data (1) sends required diagnostic data but turns off optional diagnostic data collection.</span></span> <span data-ttu-id="35768-127">Microsoft Edge 將傳送確保 Microsoft Edge 安全、處於最新、安全且如預期執行所需的必要診斷資料。</span><span class="sxs-lookup"><span data-stu-id="35768-127">Microsoft Edge will send required diagnostic data necessary to keep Microsoft Edge secure, up to date and performing as expected.</span></span> 
- <span data-ttu-id="35768-128">選擇性資料 (2) 會傳送選擇性診斷資料，其中包含有關瀏覽器使用狀況、瀏覽的網站、傳送給 Microsoft 的損毀報告的資料，以協助保持 Microsoft Edge 安全、最新且如預期執行，並且用於為所有使用者改善 Microsoft Edge 和其他 Microsoft 產品及服務。</span><span class="sxs-lookup"><span data-stu-id="35768-128">Optional data (2) sends optional diagnostic data includes data about browser usage, websites that are visited, crash reports sent to Microsoft to help keep Microsoft Edge secure, up to date, and performing as expected and is used to improve Microsoft Edge and other Microsoft products and services for all users.</span></span>

<span data-ttu-id="35768-129">在 Windows 7、Windows 8/8.1 和 macOS 上，此原則會控制傳送必要和選擇性診斷資料給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-129">On Windows 7, Windows 8/8.1, and macOS, this policy controls sending required and optional data to Microsoft.</span></span>

<span data-ttu-id="35768-130">如果未設定或停用此原則，則 Microsoft Edge 將預設為使用者的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="35768-130">If you don't configure this policy or disable it Microsoft Edge will default to the user's preference.</span></span>

### <a name="deprecated-enable-usage-and-crash-related-data-reporting"></a><span data-ttu-id="35768-131">(已取代) 啟用使用方式和當機相關的資料報告</span><span class="sxs-lookup"><span data-stu-id="35768-131">(DEPRECATED) Enable usage and crash-related data reporting</span></span>

<span data-ttu-id="35768-132">**MetricsReportingEnabled** 原則可將 Microsoft Edge 使用方式和當機相關資料的報告傳送給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-132">The **MetricsReportingEnabled** policy enables reporting of usage and crash-related data about Microsoft Edge to Microsoft.</span></span>

<span data-ttu-id="35768-133">Microsoft Edge 會收集確保產品處於最新、安全且如預期執行所需的一組必要資料。</span><span class="sxs-lookup"><span data-stu-id="35768-133">Microsoft Edge collects a set of required data that's necessary to keep the product up to date, secure, and performing as expected.</span></span> <span data-ttu-id="35768-134">此資料包括從 Microsoft Edge 傳送有關目前資料收集同意、應用程式版本和 Microsoft Edge 安裝狀態的基本裝置連線和設定資訊。</span><span class="sxs-lookup"><span data-stu-id="35768-134">This data includes basic device connectivity and configuration information from Microsoft Edge about the current data collection consent, app version, and installation state about your installation of Microsoft Edge.</span></span><span data-ttu-id="35768-135">可以透過停用原則來關閉此資料收集。</span><span class="sxs-lookup"><span data-stu-id="35768-135"> This data collection can be turned off by disabling the policy.</span></span>

<span data-ttu-id="35768-136">啟用此原則，將使用方式和當機相關資料的報告傳送到 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-136">Enable this policy to send reporting of usage and crash-related data to Microsoft.</span></span> <span data-ttu-id="35768-137">停用此原則，就不會將此資料傳送到 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-137">Disable this policy to not send the data to Microsoft.</span></span> <span data-ttu-id="35768-138">在這兩種情況下，使用者都無法變更或覆寫設定。</span><span class="sxs-lookup"><span data-stu-id="35768-138">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="35768-139">當 Microsoft Edge 在 Windows 10 上執行時：</span><span class="sxs-lookup"><span data-stu-id="35768-139">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="35768-140">如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。</span><span class="sxs-lookup"><span data-stu-id="35768-140">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="35768-141">如果啟用此原則，則僅當 Windows 診斷資料設定設為**增強**或**完整**時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-141">If this policy is enabled, Microsoft Edge will only send usage data if the Windows Diagnostic data setting is set to **Enhanced** or **Full**.</span></span>
  - <span data-ttu-id="35768-142">如果已啟用此原則，則只有在也啟用 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) 時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-142">If this policy is enabled, Microsoft Edge will only send usage data if [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) is also enabled.</span></span>
- <span data-ttu-id="35768-143">如果停用此原則，Microsoft Edge 將不會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-143">If this policy is disabled, Microsoft Edge will not send usage data.</span></span> <span data-ttu-id="35768-144">根據 Windows 診斷資料設定傳送當機相關的資料。</span><span class="sxs-lookup"><span data-stu-id="35768-144">Crash-related data is sent based on the Windows Diagnostic data setting.</span></span> <span data-ttu-id="35768-145">[深入了解 Windows 診斷資料設定](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。</span><span class="sxs-lookup"><span data-stu-id="35768-145">[Learn more about Windows Diagnostic data settings](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).</span></span>

<span data-ttu-id="35768-146">當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：</span><span class="sxs-lookup"><span data-stu-id="35768-146">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="35768-147">如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="35768-147">If this policy isn't configured, Microsoft Edge defaults to the user's preference.</span></span>
-  <span data-ttu-id="35768-148">如果已啟用此原則，則只有在也啟用 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) 時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-148">If this policy is enabled, Microsoft Edge will only send usage data if [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices) is also enabled.</span></span>

### <a name="deprecated-send-site-information-to-improve-microsoft-services"></a><span data-ttu-id="35768-149">(已取代) 傳送網站資訊以改善 Microsoft 服務</span><span class="sxs-lookup"><span data-stu-id="35768-149">(DEPRECATED) Send site information to improve Microsoft services</span></span>

<span data-ttu-id="35768-150">**SendSiteInformationToImproveServices** 原則會允許傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft，以改善 Microsoft 產品和服務 (如搜尋)。</span><span class="sxs-lookup"><span data-stu-id="35768-150">The  **SendSiteInformationToImproveServices** policy enables sending information about websites visited in Microsoft Edge to Microsoft to improve Microsoft products and services such as search.</span></span>

<span data-ttu-id="35768-151">啟用此原則可傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-151">Enable this policy to send information about websites visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="35768-152">停用此原則，就不會傳送有關使用 Microsoft Edge 造訪網站的資訊給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-152">Disable this policy to not send information about the websites that are visited in Microsoft Edge to Microsoft.</span></span> <span data-ttu-id="35768-153">在這兩種情況下，使用者都無法變更或覆寫設定。</span><span class="sxs-lookup"><span data-stu-id="35768-153">In both cases, users can't change or override the setting.</span></span>

<span data-ttu-id="35768-154">當 Microsoft Edge 在 Windows 10 上執行時：</span><span class="sxs-lookup"><span data-stu-id="35768-154">When Microsoft Edge is running on Windows 10:</span></span>

- <span data-ttu-id="35768-155">如果未設定此原則，Microsoft Edge 將預設為 Windows 診斷資料設定。</span><span class="sxs-lookup"><span data-stu-id="35768-155">If this policy isn't configured, Microsoft Edge will default to the Windows diagnostic data setting.</span></span>
- <span data-ttu-id="35768-156">如果啟用此原則，而且只有在 Windows 診斷資料設定設為 **[完整]** 時，Microsoft Edge 才會傳送有關造訪網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="35768-156">If this policy is enabled, Microsoft Edge will only send information about the websites that are visited if the Windows Diagnostic data setting is set to **Full**.</span></span>
  - <span data-ttu-id="35768-157">如果已啟用此原則，則只有在也啟用 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-157">If this policy is enabled, Microsoft Edge will only send usage data if [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) is also enabled.</span></span> 
- <span data-ttu-id="35768-158">如果停用此原則，Microsoft Edge 將不會傳送有關造訪網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="35768-158">If this policy is disabled, Microsoft Edge will not send info about websites visited.</span></span> <span data-ttu-id="35768-159">[深入了解 Windows 診斷資料設定](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。</span><span class="sxs-lookup"><span data-stu-id="35768-159">To [learn more about Windows Diagnostic data settings](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).</span></span>

<span data-ttu-id="35768-160">當 Microsoft Edge 在 Windows 7、8 及 macOS 上執行時：</span><span class="sxs-lookup"><span data-stu-id="35768-160">When Microsoft Edge is running on Windows 7, 8, and macOS:</span></span>

- <span data-ttu-id="35768-161">如果已啟用此原則，則只有在也啟用 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 時，Microsoft Edge 才會傳送使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="35768-161">If this policy is enabled, Microsoft Edge will only send usage data if [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) is also enabled.</span></span>
- <span data-ttu-id="35768-162">如果未設定此原則，Microsoft Edge 將預設為使用者的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="35768-162">If this policy isn't configured, Microsoft Edge defaults to the user's preference.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="35768-163">實作詳細資料</span><span class="sxs-lookup"><span data-stu-id="35768-163">Implementation details</span></span>

<span data-ttu-id="35768-164">若為非 Windows 10 裝置：</span><span class="sxs-lookup"><span data-stu-id="35768-164">For non-Windows 10 devices:</span></span> 
- <span data-ttu-id="35768-165">如果已設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則它優先於 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。</span><span class="sxs-lookup"><span data-stu-id="35768-165">If [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy is configured, it takes precedence over [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).</span></span> 
- <span data-ttu-id="35768-166">如果未設定 [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) 原則，則 Microsoft Edge 會接聽 [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) 和 [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices)。</span><span class="sxs-lookup"><span data-stu-id="35768-166">If [DiagnosticData](./microsoft-edge-policies.md#diagnosticdata) policy isn't configured, Microsoft Edge listens to [MetricsReportingEnabled](./microsoft-edge-policies.md#metricsreportingenabled) and [SendSiteInfoToImproveServices](./microsoft-edge-policies.md#sendsiteinfotoimproveservices).</span></span>  

<span data-ttu-id="35768-167">為了讓 Windows 10 了解我們針對 Windows 診斷資料設定採用的相依性實作，下表會指出是否將 **必要**和**選擇性**診斷資料傳送給 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35768-167">For Windows 10 to understand our implementation with the dependency on the Windows Diagnostic data setting, the following table identifies whether **Required** and **Optional** diagnostic data is sent to Microsoft.</span></span>

| <span data-ttu-id="35768-168">Windows 診斷資料設定</span><span class="sxs-lookup"><span data-stu-id="35768-168">Windows Diagnostic data setting</span></span> | <span data-ttu-id="35768-169">必要診斷資料</span><span class="sxs-lookup"><span data-stu-id="35768-169">Required diagnostic data</span></span>  | <span data-ttu-id="35768-170">選擇性診斷資料</span><span class="sxs-lookup"><span data-stu-id="35768-170">Optional diagnostic data</span></span> |
|---------------------------------|-----------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="35768-171">安全性</span><span class="sxs-lookup"><span data-stu-id="35768-171">Security</span></span>                        | <span data-ttu-id="35768-172">未傳送</span><span class="sxs-lookup"><span data-stu-id="35768-172">Not sent</span></span>                                      | <span data-ttu-id="35768-173">未傳送</span><span class="sxs-lookup"><span data-stu-id="35768-173">Not sent</span></span>                                            |
| <span data-ttu-id="35768-174">基本</span><span class="sxs-lookup"><span data-stu-id="35768-174">Basic</span></span>                           | <span data-ttu-id="35768-175">傳送</span><span class="sxs-lookup"><span data-stu-id="35768-175">Sent</span></span>                                      | <span data-ttu-id="35768-176">未傳送</span><span class="sxs-lookup"><span data-stu-id="35768-176">Not sent</span></span>                                            |
| <span data-ttu-id="35768-177">增強</span><span class="sxs-lookup"><span data-stu-id="35768-177">Enhanced</span></span>                        | <span data-ttu-id="35768-178">傳送</span><span class="sxs-lookup"><span data-stu-id="35768-178">Sent</span></span>                                          | <span data-ttu-id="35768-179">未傳送</span><span class="sxs-lookup"><span data-stu-id="35768-179">Not sent</span></span>                                            |
| <span data-ttu-id="35768-180">完整</span><span class="sxs-lookup"><span data-stu-id="35768-180">Full</span></span>                            | <span data-ttu-id="35768-181">傳送</span><span class="sxs-lookup"><span data-stu-id="35768-181">Sent</span></span>                                          | <span data-ttu-id="35768-182">傳送</span><span class="sxs-lookup"><span data-stu-id="35768-182">Sent</span></span>                                                |

> [!IMPORTANT]
> <span data-ttu-id="35768-183">針對 Microsoft Edge 版本 86 - 88 (含)，Microsoft Edge 將支援 **MetricsReportingEnabled** 和 **SendSiteInfoToImproveServices**。</span><span class="sxs-lookup"><span data-stu-id="35768-183">Microsoft Edge will support **MetricsReportingEnabled** and **SendSiteInfoToImproveServices** for Microsoft Edge versions 86 – 88 inclusive.</span></span> <span data-ttu-id="35768-184">在 Microsoft Edge 版本 89 中，**MetricsReportingEnabled** 和 **SendSiteInfoToImproveServices** 將不再受支援，且會在非 Windows 10 平台上預設為 **DiagnosticData**，或 Windows 10 則為 [允許遙測]\*\*\*\* 原則。</span><span class="sxs-lookup"><span data-stu-id="35768-184">In Microsoft Edge version 89, **MetricsReportingEnabled** and **SendSiteInfoToImproveServices** will no longer be supported and will default to **DiagnosticData** on non-Windows 10 platforms or the **Allow Telemetry** policy for Windows 10.</span></span>

## <a name="additional-privacy-policy-options"></a><span data-ttu-id="35768-185">其他隱私權原則選項</span><span class="sxs-lookup"><span data-stu-id="35768-185">Additional privacy policy options</span></span>

<span data-ttu-id="35768-186">您可能需要考慮以下與資料隱私相關的群組原則：</span><span class="sxs-lookup"><span data-stu-id="35768-186">You may want to consider the following group policies related to data privacy:</span></span>

- <span data-ttu-id="35768-187">封鎖特定網站上的 Cookie</span><span class="sxs-lookup"><span data-stu-id="35768-187">Block cookies on specific sites</span></span>
- <span data-ttu-id="35768-188">封鎖第三方 Cookie</span><span class="sxs-lookup"><span data-stu-id="35768-188">Block third-party cookies</span></span>
- <span data-ttu-id="35768-189">設定不要追蹤</span><span class="sxs-lookup"><span data-stu-id="35768-189">Configure Do Not Track</span></span>
- <span data-ttu-id="35768-190">停用 InPrivate 模式</span><span class="sxs-lookup"><span data-stu-id="35768-190">Disable InPrivate mode</span></span>

## <a name="see-also"></a><span data-ttu-id="35768-191">請參閱</span><span class="sxs-lookup"><span data-stu-id="35768-191">See also</span></span>

- [<span data-ttu-id="35768-192">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="35768-192">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="35768-193">Microsoft Edge 原則</span><span class="sxs-lookup"><span data-stu-id="35768-193">Microsoft Edge policies</span></span>](microsoft-edge-policies.md)
- [<span data-ttu-id="35768-194">Microsoft Edge 隱私權白皮書</span><span class="sxs-lookup"><span data-stu-id="35768-194">Microsoft Edge Privacy Whitepaper</span></span>](/microsoft-edge/privacy-whitepaper)