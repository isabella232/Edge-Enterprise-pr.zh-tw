---
title: 使用行動裝置管理設定 Microsoft Edge
ms.author: kvice
author: dan-wesley
manager: laurawi
ms.date: 10/25/2019
audience: ITPro
ms.topic: technical
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用行動裝置管理設定 Microsoft Edge。
ms.openlocfilehash: dda35199f653b3dfb8f20b33b068c59621222b36
ms.sourcegitcommit: 4edbe2fc2fc9a013e6a0245aba485fcc5905539b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/31/2020
ms.locfileid: "10979457"
---
# <span data-ttu-id="a8079-103">使用行動裝置管理設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8079-103">Configure Microsoft Edge using Mobile Device Management</span></span>

<span data-ttu-id="a8079-104">本文介紹如何透過 [ADMX 擷取](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)，使用[行動裝置管理 (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) 來設定 Windows 10 上的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="a8079-104">This article explains how to configure Microsoft Edge on Windows 10 using [Mobile Device Management (MDM)](https://docs.microsoft.com/windows/client-management/mdm/) by means of [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span> <span data-ttu-id="a8079-105">本文的其他內容：</span><span class="sxs-lookup"><span data-stu-id="a8079-105">This article also describes:</span></span>

- <span data-ttu-id="a8079-106">如何[為 Microsoft Edge 原則建立開放行動聯盟統一資源識別元 (OMA-URI)](#create-an-oma-uri-for-microsoft-edge-policies)。</span><span class="sxs-lookup"><span data-stu-id="a8079-106">How to [create Open Mobile Alliance Uniform Resource Identifier (OMA-URI) for Microsoft Edge policies](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>
- <span data-ttu-id="a8079-107">如何[使用 ADMX 擷取和自訂 OMA-URI 在 Intune 中設定 Microsoft Edge](#configure-microsoft-edge-in-intune-using-admx-ingestion)。</span><span class="sxs-lookup"><span data-stu-id="a8079-107">How to [configure Microsoft Edge in Intune using ADMX ingestion and custom OMA-URI](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

> [!NOTE]
> <span data-ttu-id="a8079-108">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a8079-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <span data-ttu-id="a8079-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="a8079-109">Prerequisites</span></span>

<span data-ttu-id="a8079-110">Windows 10，具有下列最低系統需求︰</span><span class="sxs-lookup"><span data-stu-id="a8079-110">Windows 10, with the following minimum system requirements:</span></span>

- <span data-ttu-id="a8079-111">Windows 10 版本 1903，需安裝 [KB4512941](https://support.microsoft.com/help/4512941/) 和 [KB4517211](https://support.microsoft.com/help/4517211/)</span><span class="sxs-lookup"><span data-stu-id="a8079-111">Windows 10, version 1903 with [KB4512941](https://support.microsoft.com/help/4512941/) and [KB4517211](https://support.microsoft.com/help/4517211/) installed</span></span>
- <span data-ttu-id="a8079-112">Windows 10 版本 1809，需安裝 [KB4512534](https://support.microsoft.com/help/4512534/) 和 [KB4520062](https://support.microsoft.com/help/4520062/)</span><span class="sxs-lookup"><span data-stu-id="a8079-112">Windows 10, version 1809 with [KB4512534](https://support.microsoft.com/help/4512534/) and [KB4520062](https://support.microsoft.com/help/4520062/) installed</span></span>
- <span data-ttu-id="a8079-113">Windows 10 版本 1803，需安裝 [KB4512509](https://support.microsoft.com/help/4512509/) 和 [KB4519978](https://support.microsoft.com/help/4519978)</span><span class="sxs-lookup"><span data-stu-id="a8079-113">Windows 10, version 1803 with [KB4512509](https://support.microsoft.com/help/4512509/) and [KB4519978](https://support.microsoft.com/help/4519978) installed</span></span>
- <span data-ttu-id="a8079-114">Windows 10 版本 1709，需安裝 [KB4516071](https://support.microsoft.com/help/4516071/) 和 [KB4520006](https://support.microsoft.com/help/4520006)</span><span class="sxs-lookup"><span data-stu-id="a8079-114">Windows 10, version 1709 with [KB4516071](https://support.microsoft.com/help/4516071/) and [KB4520006](https://support.microsoft.com/help/4520006) installed</span></span>

## <span data-ttu-id="a8079-115">概觀</span><span class="sxs-lookup"><span data-stu-id="a8079-115">Overview</span></span>

<span data-ttu-id="a8079-116">您可以使用 MDM 與偏好的企業行動管理 (EMM) 或支援 [ADMX 擷取](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)的 MDM 提供者來設定 Windows 10 上的 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="a8079-116">You can configure Microsoft Edge on Windows 10 using MDM with your preferred Enterprise Mobility Management (EMM) or MDM provider that supports [ADMX Ingestion](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration).</span></span>

<span data-ttu-id="a8079-117">使用 MDM 設定 Microsoft Edge 有兩個程序：</span><span class="sxs-lookup"><span data-stu-id="a8079-117">Configuring Microsoft Edge with MDM is a two part process:</span></span>

1. <span data-ttu-id="a8079-118">將 Microsoft Edge ADMX 檔案擷取到 EMM 或 MDM 提供者。</span><span class="sxs-lookup"><span data-stu-id="a8079-118">Ingesting the Microsoft Edge ADMX file into your EMM or MDM provider.</span></span> <span data-ttu-id="a8079-119">如需如何擷取 ADMX 檔案的指令，請洽詢您的提供者。</span><span class="sxs-lookup"><span data-stu-id="a8079-119">See your provider for instructions on how to ingest an ADMX file.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a8079-120">對於 Microsoft Intune，請參閱[使用 ADMX 擷取在 Intune 中設定 Microsoft Edge](#configure-microsoft-edge-in-intune-using-admx-ingestion)。</span><span class="sxs-lookup"><span data-stu-id="a8079-120">For Microsoft Intune, see [Configure Microsoft Edge in Intune using ADMX ingestion](#configure-microsoft-edge-in-intune-using-admx-ingestion).</span></span>

2. <span data-ttu-id="a8079-121">[為 Microsoft Edge 原則建立 OMA-URI](#create-an-oma-uri-for-microsoft-edge-policies)。</span><span class="sxs-lookup"><span data-stu-id="a8079-121">[Creating an OMA-URI for a Microsoft Edge policy](#create-an-oma-uri-for-microsoft-edge-policies).</span></span>

## <span data-ttu-id="a8079-122">為 Microsoft Edge 原則建立 OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-122">Create an OMA-URI for Microsoft Edge policies</span></span>

<span data-ttu-id="a8079-123">以下各節介紹如何建立 OMA-URI 路徑，以及如何查詢和定義用於強制和建議的瀏覽器原則的 XML 格式的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-123">The following sections describe how to create the OMA-URI path and look up and define the value in XML format for mandatory and recommended browser polices.</span></span>

<span data-ttu-id="a8079-124">在開始之前，請[從 Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (MicrosoftEdgePolicyTemplates.cab)，並解壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="a8079-124">Before you get started download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span>

<span data-ttu-id="a8079-125">定義 OMA-URI 有三個步驟：</span><span class="sxs-lookup"><span data-stu-id="a8079-125">There are three steps for defining the OMA-URI:</span></span>

1. [<span data-ttu-id="a8079-126">建立 OMA-URI 路徑</span><span class="sxs-lookup"><span data-stu-id="a8079-126">Create the OMA-URI path</span></span>](#create-the-oma-uri-path)
2. [<span data-ttu-id="a8079-127">指定 OMA-URI 資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-127">Specify the OMA-URI data type</span></span>](#specify-the-data-type)
3. [<span data-ttu-id="a8079-128">設定 OMA-URI 值</span><span class="sxs-lookup"><span data-stu-id="a8079-128">Set the OMA-URI value</span></span>](#set-the-value-for-a-browser-policy)

### <span data-ttu-id="a8079-129">建立 OMA-URI 路徑</span><span class="sxs-lookup"><span data-stu-id="a8079-129">Create the OMA-URI path</span></span>

<span data-ttu-id="a8079-130">使用以下公式作為建立 OMA-URI 路徑的指南。</span><span class="sxs-lookup"><span data-stu-id="a8079-130">Use the following formula as a guide for creating the OMA-URI paths.</span></span> <br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`* <br/><br/>

| <span data-ttu-id="a8079-131">參數</span><span class="sxs-lookup"><span data-stu-id="a8079-131">Parameter</span></span>         | <span data-ttu-id="a8079-132">描述</span><span class="sxs-lookup"><span data-stu-id="a8079-132">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| \<ADMXIngestName> | <span data-ttu-id="a8079-133">使用 "Edge" 或擷取系統管理範本時定義的內容。</span><span class="sxs-lookup"><span data-stu-id="a8079-133">Use "Edge" or what you defined when ingesting the administrative template.</span></span> <span data-ttu-id="a8079-134">例如，如果您使用 "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx"，則使用 "MicrosoftEdge"。</span><span class="sxs-lookup"><span data-stu-id="a8079-134">For example, if you used "./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftEdge/Policy/EdgeAdmx", then use "MicrosoftEdge".</span></span><br/><br/> <span data-ttu-id="a8079-135">`<ADMXIngestionName>` 必須與擷取 ADMX 檔案時使用的內容相符。</span><span class="sxs-lookup"><span data-stu-id="a8079-135">The `<ADMXIngestionName>` must match what was used when you ingested the ADMX file.</span></span> |
| \<ADMXNamespace>  | <span data-ttu-id="a8079-136">"microsoft_edge" 還是 "microsoft_edge_recommended"，取決於您設定的是強制還是建議原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-136">Either "microsoft_edge" or "microsoft_edge_recommended" depending on whether you're setting a mandatory or recommended policy.</span></span> |
| \<ADMXCategory>   | <span data-ttu-id="a8079-137">原則的 "parentCategory" 在 ADMX 檔案中定義。</span><span class="sxs-lookup"><span data-stu-id="a8079-137">The "parentCategory" of the policy is defined in the ADMX file.</span></span> <span data-ttu-id="a8079-138">如果原則未分組 (未定義 "parentCategory")，則省略 `<ADMXCategory>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-138">Omit the `<ADMXCategory>` if the policy isn't grouped (No "parentCategory" defined).</span></span> |
| \<PolicyName>     | <span data-ttu-id="a8079-139">可在[瀏覽器原則參考](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies)文章中找到原則名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-139">The policy name can be found in the [Browser policy reference](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies) article.</span></span> |

#### <span data-ttu-id="a8079-140">URI 路徑範例：</span><span class="sxs-lookup"><span data-stu-id="a8079-140">URI path example:</span></span>

<span data-ttu-id="a8079-141">在此範例中，假設 `<ADMXIngestName>` 節點名為 "Edge"，並且您正在設定強制原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-141">For this example, assume the `<ADMXIngestName>` node was named “Edge" and you're setting a mandatory policy.</span></span> <span data-ttu-id="a8079-142">URI 路徑為：</span><span class="sxs-lookup"><span data-stu-id="a8079-142">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~<ADMXCategory>/<PolicyName>`*

<span data-ttu-id="a8079-143">如果原則不在群組中 (例如，DiskCacheSize) 則移除 "`~<ADMXCategory>`"。</span><span class="sxs-lookup"><span data-stu-id="a8079-143">If the policy isn't in a group (for example, DiskCacheSize) remove "`~<ADMXCategory>`".</span></span> <span data-ttu-id="a8079-144">將 `<PolicyName>` 替換為原則名稱 DiskCacheSize。</span><span class="sxs-lookup"><span data-stu-id="a8079-144">Replace `<PolicyName>` with the name of the policy, DiskCacheSize.</span></span> <span data-ttu-id="a8079-145">URI 路徑為：</span><span class="sxs-lookup"><span data-stu-id="a8079-145">The URI path would be:</span></span><br/><br/>
*`./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`*

<span data-ttu-id="a8079-146">如果原則位於群組中，請按照以下步驟操作：</span><span class="sxs-lookup"><span data-stu-id="a8079-146">If the policy is in a group, follow these steps:</span></span>

1. <span data-ttu-id="a8079-147">使用任何 xml 編輯器開啟 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-147">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="a8079-148">搜尋要設定的原則名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-148">Search for the policy name you want to set.</span></span> <span data-ttu-id="a8079-149">例如，"ExtensionInstallForceList"。</span><span class="sxs-lookup"><span data-stu-id="a8079-149">For example, "ExtensionInstallForceList".</span></span>
3. <span data-ttu-id="a8079-150">使用 *parentCategory* 元素中 *ref* 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-150">Use the value of the *ref* attribute from the *parentCategory* element.</span></span> <span data-ttu-id="a8079-151">例如，來自 \<parentCategory ref=" Extensions"/> 的「延伸模組」。</span><span class="sxs-lookup"><span data-stu-id="a8079-151">For example, "Extensions" from \<parentCategory ref=" Extensions"/>.</span></span>
4. <span data-ttu-id="a8079-152">將 `<ADMXCategory>` 替換為建構 URI 路徑的 *ref* 屬性值。</span><span class="sxs-lookup"><span data-stu-id="a8079-152">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path.</span></span> <span data-ttu-id="a8079-153">URI 路徑為：</span><span class="sxs-lookup"><span data-stu-id="a8079-153">The URI path would be:</span></span><br/><br/>
*`/Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`*

### <span data-ttu-id="a8079-154">指定資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-154">Specify the data type</span></span>

<span data-ttu-id="a8079-155">OMA-URI 資料類型一律為 "String"。</span><span class="sxs-lookup"><span data-stu-id="a8079-155">The OMA-URI data type is always “String”.</span></span>

### <span data-ttu-id="a8079-156">設定瀏覽器原則的值</span><span class="sxs-lookup"><span data-stu-id="a8079-156">Set the value for a browser policy</span></span>

<span data-ttu-id="a8079-157">本節介紹如何為每個資料類型設定 XML 格式的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-157">This section describes how to set the value, in XML format, for each data type.</span></span> <span data-ttu-id="a8079-158">移至[瀏覽器原則參考](https://docs.microsoft.com/deployedge/microsoft-edge-policies)以查詢原則的資料類型。</span><span class="sxs-lookup"><span data-stu-id="a8079-158">Go to [Browser policy reference](https://docs.microsoft.com/deployedge/microsoft-edge-policies) to look up the data type of the policy.</span></span>

> [!NOTE]
> <span data-ttu-id="a8079-159">對於非布林資料類型，值開頭一律為 `<enabled/>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-159">For non-Boolean data types, the value always starts with `<enabled/>`.</span></span>

#### <span data-ttu-id="a8079-160">布林值資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-160">Boolean data type</span></span>

<span data-ttu-id="a8079-161">對於布林類型的原則，請使用 `<enabled/>` 或 `<disabled/>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-161">For policies that are Boolean types use `<enabled/>` or `<disabled/>`.</span></span>

#### <span data-ttu-id="a8079-162">整數資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-162">Integer data type</span></span>

<span data-ttu-id="a8079-163">值一律需開頭為 `<enabled/>` 元素，後接 `<data id="[valueName]" value="[decimal value]"/>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-163">The value always needs to start with the `<enabled/>` element followed by `<data id="[valueName]" value="[decimal value]"/>`.</span></span>

<span data-ttu-id="a8079-164">若要尋找新索引標籤頁面的值名稱和十進位值，請使用以下步驟：</span><span class="sxs-lookup"><span data-stu-id="a8079-164">To find the value name and decimal value for a new tab page, use the following steps:</span></span>

1. <span data-ttu-id="a8079-165">使用任何 xml 編輯器開啟 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-165">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="a8079-166">搜尋名稱屬性符合您要設定之原則名稱的 `<policy>` 元素。</span><span class="sxs-lookup"><span data-stu-id="a8079-166">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="a8079-167">對於 "RestoreOnStartup"，請搜尋 `name="RestoreOnStartup"`。</span><span class="sxs-lookup"><span data-stu-id="a8079-167">For "RestoreOnStartup", search for `name="RestoreOnStartup"`.</span></span>
3. <span data-ttu-id="a8079-168">在 `<elements>` 節點中，尋找您希望設定的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-168">In the `<elements>` node, find the value you want to set.</span></span>
4. <span data-ttu-id="a8079-169">使用 `<elements>` 節點中 "valueName" 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-169">Use the value in the "valueName" attribute in the `<elements>` node.</span></span> <span data-ttu-id="a8079-170">對於 "RestoreOnStartup"，"valueName" 是 "RestoreOnStartup"。</span><span class="sxs-lookup"><span data-stu-id="a8079-170">For "RestoreOnStartup" the "valueName" is "RestoreOnStartup".</span></span>
5. <span data-ttu-id="a8079-171">使用 `<decimal>` 節點中 "value" 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-171">Use the value in the "value" attribute in the `<decimal>` node.</span></span> <span data-ttu-id="a8079-172">對於 "RestoreOnStartup" 開啟新的索引標籤頁面，值為 "5"。</span><span class="sxs-lookup"><span data-stu-id="a8079-172">For "RestoreOnStartup" to open the new tab page the value is "5".</span></span>

<span data-ttu-id="a8079-173">若要在啟動時開啟新的索引標籤頁面，請使用：</span><span class="sxs-lookup"><span data-stu-id="a8079-173">To open the new tab page on startup use:</span></span><br>
`<enabled/> <data id="RestoreOnStartup" value="5"/>`

#### <span data-ttu-id="a8079-174">字串清單資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-174">List of strings data type</span></span>

<span data-ttu-id="a8079-175">值一律需開頭為 `<enabled/>` 元素，後接 `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-175">The value always needs to start with the `<enabled/>` element followed by `<data id="[listID]" value="[string 1];[string 2];[string 3]"/>`.</span></span>

> [!NOTE]
> <span data-ttu-id="a8079-176">"id=" 屬性名稱不是原則名稱，儘管在大多數情況下它與原則名稱相符。</span><span class="sxs-lookup"><span data-stu-id="a8079-176">The "id=" attribute name isn't the policy name, even though in most cases it matches the policy name.</span></span> <span data-ttu-id="a8079-177">它是 \<list> 節點識別碼屬性值，可在 ADMX 檔案中找到。</span><span class="sxs-lookup"><span data-stu-id="a8079-177">It's the \<list> node id attribute value, which is found in the ADMX file.</span></span>

<span data-ttu-id="a8079-178">若要尋找 listID 並定義封鎖 URL 的值，請按照以下步驟操作：</span><span class="sxs-lookup"><span data-stu-id="a8079-178">To find the listID and define the value to block a URL, follow these steps:</span></span>

1. <span data-ttu-id="a8079-179">使用任何 xml 編輯器開啟 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-179">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="a8079-180">搜尋名稱屬性與要設定的原則名稱相符的 `<policy>` 元素。</span><span class="sxs-lookup"><span data-stu-id="a8079-180">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="a8079-181">對於 "URLBlocklist"，搜尋 `name="URLBlocklist"`。</span><span class="sxs-lookup"><span data-stu-id="a8079-181">For "URLBlocklist", search for `name="URLBlocklist"`.</span></span>
3. <span data-ttu-id="a8079-182">使用 `<list> node for [listID]` 的 "id" 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-182">Use the value in the "id" attribute of the `<list> node for [listID]`.</span></span>
4. <span data-ttu-id="a8079-183">"value" 是由分號 (;) 分隔的 URL 清單</span><span class="sxs-lookup"><span data-stu-id="a8079-183">The "value" is a list of URLs separated by a semicolon (;)</span></span>

<span data-ttu-id="a8079-184">例如，若要封鎖對 `contoso.com` 和 `https://ssl.server.com` 的存取：</span><span class="sxs-lookup"><span data-stu-id="a8079-184">For example, to block access to `contoso.com` and `https://ssl.server.com`:</span></span><br>
`<enabled/> <data id=" URLBlocklistDesc" value="contoso.com;https://ssl.server.com"/>`

#### <span data-ttu-id="a8079-185">字典或字串資料類型</span><span class="sxs-lookup"><span data-stu-id="a8079-185">Dictionary or String data type</span></span>

<span data-ttu-id="a8079-186">值一律需開頭為 `<enabled/>`，後接 `<data id="[textID]" value="[string]"/>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-186">The value always needs to start with the `<enabled/>` followed by `<data id="[textID]" value="[string]"/>` .</span></span>

<span data-ttu-id="a8079-187">若要尋找 textID 並定義設定地區設定的值，請按照以下步驟操作：</span><span class="sxs-lookup"><span data-stu-id="a8079-187">To find the textID and define the value set the locale, follow these steps:</span></span>

1. <span data-ttu-id="a8079-188">使用任何 xml 編輯器開啟 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-188">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="a8079-189">搜尋名稱屬性與要設定的原則名稱相符的 `<policy>` 元素。</span><span class="sxs-lookup"><span data-stu-id="a8079-189">Search for the `<policy>` element where the name attribute matches the policy name you want to set.</span></span> <span data-ttu-id="a8079-190">對於 "ApplicationLocaleValue"，請搜尋 `name="ApplicationLocaleValue"`。</span><span class="sxs-lookup"><span data-stu-id="a8079-190">For "ApplicationLocaleValue", search for `name="ApplicationLocaleValue"`.</span></span>
3. <span data-ttu-id="a8079-191">使用 `[textID]` 的 `<text>` 節點 "id" 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-191">Use the value in the "id" attribute of the `<text>` node for `[textID]`.</span></span>
4. <span data-ttu-id="a8079-192">設定文化特性代碼的 "value"。</span><span class="sxs-lookup"><span data-stu-id="a8079-192">Set the "value" to the culture code.</span></span>

<span data-ttu-id="a8079-193">若要使用 "ApplicationLocaleValue" 原則將地區設定設定為 "es-US"：</span><span class="sxs-lookup"><span data-stu-id="a8079-193">To set the locale to "es-US" with the "ApplicationLocaleValue" policy:</span></span><br>
`<enabled/> <data id="ApplicationLocaleValue" value="es-US"/>`

### <span data-ttu-id="a8079-194">為建議的原則建立 OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-194">Create the OMA-URI for a recommended policies</span></span>

<span data-ttu-id="a8079-195">為建議原則定義 URI 路徑取決於您要設定的原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-195">Defining the URI path for recommended policies depends on the policy you want to configure.</span></span>

#### <span data-ttu-id="a8079-196">定義建議原則的 URI 路徑</span><span class="sxs-lookup"><span data-stu-id="a8079-196">To define the URI path for a recommended policy</span></span>

<span data-ttu-id="a8079-197">使用 URI 路徑公式 (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) 和以下步驟來定義 URI 路徑：</span><span class="sxs-lookup"><span data-stu-id="a8079-197">Use the URI path formula (*`./Device/Vendor/MSFT/Policy/Config/<ADMXIngestName>~Policy~<ADMXNamespace>~<ADMXCategory>/<PolicyName>`*) and the following steps to define the URI path:</span></span>

1. <span data-ttu-id="a8079-198">使用任何 xml 編輯器開啟 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-198">Open **msedge.admx** with any xml editor.</span></span>
2. <span data-ttu-id="a8079-199">如果要設定的原則不在群組中，請跳到步驟 4 並從路徑中移除 `~<ADMXCategory>`。</span><span class="sxs-lookup"><span data-stu-id="a8079-199">If the policy you want to configure isn't in a group, skip to step 4 and remove `~<ADMXCategory>` from the path.</span></span>
3. <span data-ttu-id="a8079-200">如果要設定的原則位於群組中：</span><span class="sxs-lookup"><span data-stu-id="a8079-200">If the policy you want to configure is in a group:</span></span>

   - <span data-ttu-id="a8079-201">若要查詢 `<ADMXCategory>`，請搜尋您要設定的原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-201">To look up the `<ADMXCategory>`, search for the policy you want to set.</span></span> <span data-ttu-id="a8079-202">搜尋時，將 "_recommended" 附加到原則名稱中。</span><span class="sxs-lookup"><span data-stu-id="a8079-202">When searching append "_recommended" to the policy name.</span></span> <span data-ttu-id="a8079-203">例如，搜尋 "RegisteredProtocolHandlers_recommended" 具有以下結果：</span><span class="sxs-lookup"><span data-stu-id="a8079-203">For example, a search for "RegisteredProtocolHandlers_recommended” has the following result:</span></span>

        ```xml
         <policy class="Both" displayName="$(string.RegisteredProtocolHandlers)" explainText="$(string.RegisteredProtocolHandlers_Explain)" key="Software\Policies\Microsoft\Edge\Recommended" name="RegisteredProtocolHandlers_recommended" presentation="$(presentation.RegisteredProtocolHandlers)">
           <parentCategory ref="ContentSettings_recommended"/>
           <supportedOn ref="SUPPORTED_WIN7_V77"/>
           <elements>
             <text id="RegisteredProtocolHandlers" maxLength="1000000" valueName="RegisteredProtocolHandlers"/>
           </elements>
         </policy>
        ```

   - <span data-ttu-id="a8079-204">從 `<parentCategory>` 元素複製 *ref* 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8079-204">Copy the value of the *ref* attribute from the `<parentCategory>` element.</span></span> <span data-ttu-id="a8079-205">對於 "ContentSettings"，請從 `<parentCategory ref=" ContentSettings_recommended"/>` 複製 "ContentSettings_recommended"。</span><span class="sxs-lookup"><span data-stu-id="a8079-205">For "ContentSettings", copy "ContentSettings_recommended" from `<parentCategory ref=" ContentSettings_recommended"/>`.</span></span>
   - <span data-ttu-id="a8079-206">將 `<ADMXCategory>` 替換為在 URI 路徑公式中建構 URI 路徑的 *ref* 屬性值。</span><span class="sxs-lookup"><span data-stu-id="a8079-206">Replace `<ADMXCategory>` with the *ref* attribute value to construct the URI path in the URI path formula.</span></span>

4. <span data-ttu-id="a8079-207">`<PolicyName>` 是原則的名稱，並附加了 "_recommended"。</span><span class="sxs-lookup"><span data-stu-id="a8079-207">The `<PolicyName>` is the name of the policy with "_recommended" appended to it.</span></span>

#### <span data-ttu-id="a8079-208">建議原則的 OMA-URI 路徑範例</span><span class="sxs-lookup"><span data-stu-id="a8079-208">OMA-URI path examples for recommended policies</span></span>

<span data-ttu-id="a8079-209">下表顯示了建議原則的 OMA-URI 路徑範例。</span><span class="sxs-lookup"><span data-stu-id="a8079-209">The following table shows examples of OMA-URI paths for recommended policies.</span></span>

|              <span data-ttu-id="a8079-210">原則</span><span class="sxs-lookup"><span data-stu-id="a8079-210">Policy</span></span>               |             <span data-ttu-id="a8079-211">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-211">OMA-URI</span></span>                      |
|-----------------------------------|------------------------------------------|
| [<span data-ttu-id="a8079-212">RegisteredProtocolHandlers</span><span class="sxs-lookup"><span data-stu-id="a8079-212">RegisteredProtocolHandlers</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#registeredprotocolhandlers)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~ContentSettings_recommended/RegisteredProtocolHandlers_recommended`                        |
| [<span data-ttu-id="a8079-213">PasswordManagerEnabled</span><span class="sxs-lookup"><span data-stu-id="a8079-213">PasswordManagerEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#passwordmanagerenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~PasswordManager_recommended/PasswordManagerEnabled_recommended`                        |
| [<span data-ttu-id="a8079-214">PrintHeaderFooter</span><span class="sxs-lookup"><span data-stu-id="a8079-214">PrintHeaderFooter</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#printheaderfooter)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Printing_recommended/PrintHeaderFooter_recommended`                        |
| [<span data-ttu-id="a8079-215">SmartScreenEnabled</span><span class="sxs-lookup"><span data-stu-id="a8079-215">SmartScreenEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#smartscreenenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~SmartScreen_recommended/SmartScreenEnabled_recommended`                        |
| [<span data-ttu-id="a8079-216">HomePageLocation</span><span class="sxs-lookup"><span data-stu-id="a8079-216">HomePageLocation</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#homepagelocation)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/HomepageLocation_recommended`                        |
| [<span data-ttu-id="a8079-217">ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="a8079-217">ShowHomeButton</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#showhomebutton)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~Startup_recommended/ShowHomeButton_recommended`                        |
| [<span data-ttu-id="a8079-218">FavoritesBarEnabled</span><span class="sxs-lookup"><span data-stu-id="a8079-218">FavoritesBarEnabled</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-policies#favoritesbarenabled)                       | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge_recommended~/FavoritesBarEnabled_recommended`                        |

### <span data-ttu-id="a8079-219">OMA-URI 範例</span><span class="sxs-lookup"><span data-stu-id="a8079-219">OMA-URI examples</span></span>

<span data-ttu-id="a8079-220">OMA-URI 範例及其 URI 路徑、類型和範例值。</span><span class="sxs-lookup"><span data-stu-id="a8079-220">OMA-URI examples with their URI path, type, and an example value.</span></span>

#### <span data-ttu-id="a8079-221">布林值資料類型範例</span><span class="sxs-lookup"><span data-stu-id="a8079-221">Boolean data type examples</span></span>

*<span data-ttu-id="a8079-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton)：</span><span class="sxs-lookup"><span data-stu-id="a8079-222">[ShowHomeButton](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ShowHomeButton):</span></span>*

| <span data-ttu-id="a8079-223">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-223">Field</span></span>   | <span data-ttu-id="a8079-224">值</span><span class="sxs-lookup"><span data-stu-id="a8079-224">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-225">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-225">Name</span></span>    | <span data-ttu-id="a8079-226">Microsoft Edge: ShowHomeButton</span><span class="sxs-lookup"><span data-stu-id="a8079-226">Microsoft Edge: ShowHomeButton</span></span>                                                       |
| <span data-ttu-id="a8079-227">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-227">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton` |
| <span data-ttu-id="a8079-228">type</span><span class="sxs-lookup"><span data-stu-id="a8079-228">type</span></span>    | <span data-ttu-id="a8079-229">String</span><span class="sxs-lookup"><span data-stu-id="a8079-229">String</span></span>                                                                               |
| <span data-ttu-id="a8079-230">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-230">Value</span></span>   | `<enabled/>`                                                                          |

*<span data-ttu-id="a8079-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled)：</span><span class="sxs-lookup"><span data-stu-id="a8079-231">[DefaultSearchProviderEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultSearchProviderEnabled):</span></span>*

| <span data-ttu-id="a8079-232">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-232">Field</span></span>   | <span data-ttu-id="a8079-233">值</span><span class="sxs-lookup"><span data-stu-id="a8079-233">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-234">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-234">Name</span></span>    | <span data-ttu-id="a8079-235">Microsoft Edge: DefaultSearchProviderEnabled</span><span class="sxs-lookup"><span data-stu-id="a8079-235">Microsoft Edge: DefaultSearchProviderEnabled</span></span>                                         |
| <span data-ttu-id="a8079-236">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-236">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~DefaultSearchProvider/DefaultSearchProviderEnabled`    |
| <span data-ttu-id="a8079-237">type</span><span class="sxs-lookup"><span data-stu-id="a8079-237">type</span></span>    | <span data-ttu-id="a8079-238">String</span><span class="sxs-lookup"><span data-stu-id="a8079-238">String</span></span>                                                                               |
| <span data-ttu-id="a8079-239">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-239">Value</span></span>   | `<disable/>`                                                                          |

### <span data-ttu-id="a8079-240">整數資料類型範例</span><span class="sxs-lookup"><span data-stu-id="a8079-240">Integer data type examples</span></span>

*<span data-ttu-id="a8079-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun)：</span><span class="sxs-lookup"><span data-stu-id="a8079-241">[AutoImportAtFirstRun](https://docs.microsoft.com/deployedge/microsoft-edge-policies#AutoImportAtFirstRun):</span></span>*

| <span data-ttu-id="a8079-242">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-242">Field</span></span>   | <span data-ttu-id="a8079-243">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-243">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-244">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-244">Name</span></span>    | <span data-ttu-id="a8079-245">Microsoft Edge: AutoImportAtFirstRun</span><span class="sxs-lookup"><span data-stu-id="a8079-245">Microsoft Edge: AutoImportAtFirstRun</span></span>                                                 |
| <span data-ttu-id="a8079-246">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-246">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/AutoImportAtFirstRun`   |
| <span data-ttu-id="a8079-247">type</span><span class="sxs-lookup"><span data-stu-id="a8079-247">type</span></span>    | <span data-ttu-id="a8079-248">String</span><span class="sxs-lookup"><span data-stu-id="a8079-248">String</span></span>                                                                               |
| <span data-ttu-id="a8079-249">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-249">Value</span></span>   | `<enabled/><data id="AutoImportAtFirstRun" value="1"/>`                             |

*<span data-ttu-id="a8079-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting)：</span><span class="sxs-lookup"><span data-stu-id="a8079-250">[DefaultImagesSetting](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DefaultImagesSetting):</span></span>*

| <span data-ttu-id="a8079-251">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-251">Field</span></span>   | <span data-ttu-id="a8079-252">值</span><span class="sxs-lookup"><span data-stu-id="a8079-252">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-253">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-253">Name</span></span>    | <span data-ttu-id="a8079-254">Microsoft Edge: DefaultImagesSetting</span><span class="sxs-lookup"><span data-stu-id="a8079-254">Microsoft Edge: DefaultImagesSetting</span></span>                                                 |
| <span data-ttu-id="a8079-255">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-255">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/DefaultImagesSetting`    |
| <span data-ttu-id="a8079-256">type</span><span class="sxs-lookup"><span data-stu-id="a8079-256">type</span></span>    | <span data-ttu-id="a8079-257">String</span><span class="sxs-lookup"><span data-stu-id="a8079-257">String</span></span>                                                                               |
| <span data-ttu-id="a8079-258">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-258">Value</span></span>   | `<enabled/><data id="DefaultImagesSetting" value="2"/>`                             |

*<span data-ttu-id="a8079-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize)：</span><span class="sxs-lookup"><span data-stu-id="a8079-259">[DiskCacheSize](https://docs.microsoft.com/deployedge/microsoft-edge-policies#DiskCacheSize):</span></span>*

| <span data-ttu-id="a8079-260">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-260">Field</span></span>   | <span data-ttu-id="a8079-261">值</span><span class="sxs-lookup"><span data-stu-id="a8079-261">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-262">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-262">Name</span></span>    | <span data-ttu-id="a8079-263">Microsoft Edge: DiskCacheSize</span><span class="sxs-lookup"><span data-stu-id="a8079-263">Microsoft Edge: DiskCacheSize</span></span>                                                        |
| <span data-ttu-id="a8079-264">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-264">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge/DiskCacheSize`        |
| <span data-ttu-id="a8079-265">type</span><span class="sxs-lookup"><span data-stu-id="a8079-265">type</span></span>    | <span data-ttu-id="a8079-266">String</span><span class="sxs-lookup"><span data-stu-id="a8079-266">String</span></span>                                                                               |
| <span data-ttu-id="a8079-267">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-267">Value</span></span>   | `<enabled/><data id="DiskCacheSize" value="1000000"/>`                               |

#### <span data-ttu-id="a8079-268">字串清單資料類型範例</span><span class="sxs-lookup"><span data-stu-id="a8079-268">List of strings data type examples</span></span>
<!--
*[NotificationsAllowedForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#NotificationsAllowedForUrls):*

| Field   | Value                                                                                |
|---------|--------------------------------------------------------------------------------------|
| Name    | Microsoft Edge: NotificationsAllowedForUrls                                          |
| OMA-URI | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ContentSettings/NotificationsAllowedForUrls`    |
| Type    | String                                                                               |
| Value   | `<enabled/><data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com"/>`<br>For multiple list items: `<data id="NotificationsAllowedForUrlsDesc" value="https://www.contoso.com;[*.]contoso.edu"/>`                               |
-->
*<span data-ttu-id="a8079-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS)：</span><span class="sxs-lookup"><span data-stu-id="a8079-269">[RestoreOnStartupURLS](https://docs.microsoft.com/deployedge/microsoft-edge-policies#RestoreOnStartupURLS):</span></span>*

| <span data-ttu-id="a8079-270">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-270">Field</span></span>   | <span data-ttu-id="a8079-271">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-271">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-272">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-272">Name</span></span>    | <span data-ttu-id="a8079-273">Microsoft Edge: RestoreOnStartupURLS</span><span class="sxs-lookup"><span data-stu-id="a8079-273">Microsoft Edge: RestoreOnStartupURLS</span></span>                                                 |
| <span data-ttu-id="a8079-274">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-274">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/RestoreOnStartupURLs`    |
| <span data-ttu-id="a8079-275">Type</span><span class="sxs-lookup"><span data-stu-id="a8079-275">Type</span></span>    | <span data-ttu-id="a8079-276">String</span><span class="sxs-lookup"><span data-stu-id="a8079-276">String</span></span>                                                                               |
| <span data-ttu-id="a8079-277">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-277">Value</span></span>   | `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com"/>`<br><span data-ttu-id="a8079-278">對於多重清單項目：</span><span class="sxs-lookup"><span data-stu-id="a8079-278">For multiple list items:</span></span> `<enabled/><data id="RestoreOnStartupURLsDesc" value="1&#xF000;http://www.bing.com&#xF000;2&#xF000;http://www.microsoft.com"/>`  |

*<span data-ttu-id="a8079-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist)：</span><span class="sxs-lookup"><span data-stu-id="a8079-279">[ExtensionInstallForcelist](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ExtensionInstallForcelist):</span></span>*

| <span data-ttu-id="a8079-280">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-280">Field</span></span>   | <span data-ttu-id="a8079-281">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-281">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-282">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-282">Name</span></span>    | <span data-ttu-id="a8079-283">Microsoft Edge: ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="a8079-283">Microsoft Edge: ExtensionInstallForcelist</span></span>                                            |
| <span data-ttu-id="a8079-284">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-284">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Extensions/ExtensionInstallForcelist`    |
| <span data-ttu-id="a8079-285">Type</span><span class="sxs-lookup"><span data-stu-id="a8079-285">Type</span></span>    | <span data-ttu-id="a8079-286">String</span><span class="sxs-lookup"><span data-stu-id="a8079-286">String</span></span>                                                                               |
| <span data-ttu-id="a8079-287">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-287">Value</span></span>   | `<enabled/><data id="ExtensionInstallForcelistDesc" value="1&#xF000;gbchcmhmhahfdphkhkmpfmihenigjmpp;https://extensionwebstorebase.edgesv.net/v1/crx"/>`                               |

#### <span data-ttu-id="a8079-288">字典和字串資料類型範例</span><span class="sxs-lookup"><span data-stu-id="a8079-288">Dictionary and String data type example</span></span>

*<span data-ttu-id="a8079-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode)：</span><span class="sxs-lookup"><span data-stu-id="a8079-289">[ProxyMode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#ProxyMode):</span></span>*

| <span data-ttu-id="a8079-290">欄位</span><span class="sxs-lookup"><span data-stu-id="a8079-290">Field</span></span>   | <span data-ttu-id="a8079-291">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-291">Value</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8079-292">Name</span><span class="sxs-lookup"><span data-stu-id="a8079-292">Name</span></span>    | <span data-ttu-id="a8079-293">Microsoft Edge: ProxyMode</span><span class="sxs-lookup"><span data-stu-id="a8079-293">Microsoft Edge: ProxyMode</span></span>                                                            |
| <span data-ttu-id="a8079-294">OMA-URI</span><span class="sxs-lookup"><span data-stu-id="a8079-294">OMA-URI</span></span> | `./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~ProxyMode/ProxyMode`  |
| <span data-ttu-id="a8079-295">Type</span><span class="sxs-lookup"><span data-stu-id="a8079-295">Type</span></span>    | <span data-ttu-id="a8079-296">String</span><span class="sxs-lookup"><span data-stu-id="a8079-296">String</span></span>                                                                               |
| <span data-ttu-id="a8079-297">Value</span><span class="sxs-lookup"><span data-stu-id="a8079-297">Value</span></span>   | `<enabled/><data id="ProxyMode" value="auto_detect"/>`                               |

## <span data-ttu-id="a8079-298">使用 ADMX 擷取在 Intune 中設定 Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a8079-298">Configure Microsoft Edge in Intune using ADMX ingestion</span></span>

<span data-ttu-id="a8079-299">使用 Microsoft Intune 設定 Microsoft Edge 的建議方法是使用系統管理範本設定檔，如[使用 Microsoft Intune 設定 Microsoft Edge 原則設定](https://docs.microsoft.com/deployedge/configure-edge-with-intune)中所述。</span><span class="sxs-lookup"><span data-stu-id="a8079-299">The recommended way to configure Microsoft Edge with Microsoft Intune is to use the Administrative Templates profile as described in [Configure Microsoft Edge policy settings with Microsoft Intune](https://docs.microsoft.com/deployedge/configure-edge-with-intune).</span></span> <span data-ttu-id="a8079-300">如果要評估 Intune 中 Microsoft Edge 系統管理範本中目前未提供的原則，則可以使用 [Intune 中 Windows 10 裝置的自訂設定](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)來設定 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="a8079-300">If you want to evaluate a policy that is currently not available in the Microsoft Edge Administrative Templates in Intune you can configure Microsoft Edge using  [custom settings for Windows 10 devices in Intune](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10).</span></span>

<span data-ttu-id="a8079-301">本節說明如何：</span><span class="sxs-lookup"><span data-stu-id="a8079-301">This section describes how to:</span></span>

1. [<span data-ttu-id="a8079-302">將 Microsoft Edge ADMX 檔案擷取至 Intune</span><span class="sxs-lookup"><span data-stu-id="a8079-302">Ingest the Microsoft Edge ADMX file into Intune</span></span>](#ingest-the-microsoft-edge-admx-file-into-intune)
2. [<span data-ttu-id="a8079-303">在 Intune 中使用自訂 OMA-URI 設定原則</span><span class="sxs-lookup"><span data-stu-id="a8079-303">Set a policy using custom OMA-URI in Intune</span></span>](#set-a-policy-using-custom-oma-uri-in-intune)

> [!IMPORTANT]
> <span data-ttu-id="a8079-304">最佳做法是，不要使用自訂 OMA-URI 設定檔和系統管理範本設定檔在 Intune 中設定相同的 Microsoft Edge 設定。</span><span class="sxs-lookup"><span data-stu-id="a8079-304">As a best practice, don’t use a custom OMA-URI profile and an Administration templates profile to configure the same Microsoft Edge setting in Intune.</span></span> <span data-ttu-id="a8079-305">如果使用自訂 OMA-URI 和系統管理範本設定檔部署同一原則，但具有不同的值，使用者會獲得不可預知的結果。</span><span class="sxs-lookup"><span data-stu-id="a8079-305">If you deploy the same policy using both a custom OMA-URI  and an Administrative template profile, but with different values, users will get unpredictable results.</span></span> <span data-ttu-id="a8079-306">在使用系統管理範本設定檔之前，我們強烈建議移除 OMA-URI 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a8079-306">We strongly recommend removing your OMA-URI profile before using an Administration templates profile.</span></span>

### <span data-ttu-id="a8079-307">將 Microsoft Edge ADMX 檔案擷取至 Intune</span><span class="sxs-lookup"><span data-stu-id="a8079-307">Ingest the Microsoft Edge ADMX file into Intune</span></span>

<span data-ttu-id="a8079-308">本節介紹如何將 Microsoft Edge 系統管理範本 (**msedge.admx** 檔案) 擷取至 Intune。</span><span class="sxs-lookup"><span data-stu-id="a8079-308">This section describes how to ingest the Microsoft Edge administrative template (**msedge.admx** file) into Intune.</span></span>

> [!WARNING]
> <span data-ttu-id="a8079-309">在擷取檔案之前，不要修改 ADMX 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8079-309">Don't modify the ADMX file before ingesting the file.</span></span>

<span data-ttu-id="a8079-310">若要擷取 ADMX 檔案，請依照下列步驟執行︰</span><span class="sxs-lookup"><span data-stu-id="a8079-310">To ingest the ADMX file, follow these steps:</span></span>

1. <span data-ttu-id="a8079-311">從 [Microsoft Edge 企業登陸頁面](https://aka.ms/EdgeEnterprise)下載 Microsoft Edge 原則範本檔案 (MicrosoftEdgePolicyTemplates.cab)，並解壓縮內容。</span><span class="sxs-lookup"><span data-stu-id="a8079-311">Download the Microsoft Edge policy templates file (MicrosoftEdgePolicyTemplates.cab) from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise) and extract the contents.</span></span> <span data-ttu-id="a8079-312">您要擷取的檔案是 **msedge.admx**。</span><span class="sxs-lookup"><span data-stu-id="a8079-312">The file that you want to ingest is **msedge.admx**.</span></span>
2. <span data-ttu-id="a8079-313">登入 [Microsoft Azure 入口網站](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="a8079-313">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
3. <span data-ttu-id="a8079-314">從_所有服務_中選取 **Intune**，或在入口網站搜尋方塊中搜尋 Intune。</span><span class="sxs-lookup"><span data-stu-id="a8079-314">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
4. <span data-ttu-id="a8079-315">從 _Microsoft Intune - 概觀_中，選取**裝置設定** | **設定檔**。</span><span class="sxs-lookup"><span data-stu-id="a8079-315">From _Microsoft Intune - Overview_, select **Device configuration** | **Profiles**.</span></span>
5. <span data-ttu-id="a8079-316">在頂端命令列上，選取 **+ 建立設定檔**。</span><span class="sxs-lookup"><span data-stu-id="a8079-316">On the top command bar, select **+ Create profile**.</span></span>

   ![建立裝置設定檔](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile.png)

6. <span data-ttu-id="a8079-318">提供以下設定檔資訊：</span><span class="sxs-lookup"><span data-stu-id="a8079-318">Provide the following profile information:</span></span>

   - <span data-ttu-id="a8079-319">**名稱**：輸入描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-319">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="a8079-320">對於此範例，為「Microsoft Edge ADMX 擷取的設定」。</span><span class="sxs-lookup"><span data-stu-id="a8079-320">For this example, "Microsoft Edge ADMX ingested configuration".</span></span>
   - <span data-ttu-id="a8079-321">**描述**：輸入設定檔的選用描述。</span><span class="sxs-lookup"><span data-stu-id="a8079-321">**Description**: Enter an optional description for the profile.</span></span>
   - <span data-ttu-id="a8079-322">**平台**：選取 [Windows 10 和更新版本]</span><span class="sxs-lookup"><span data-stu-id="a8079-322">**Platform**: Select "Windows 10 and later"</span></span>
   - <span data-ttu-id="a8079-323">**設定檔類型**：選取 [自訂]</span><span class="sxs-lookup"><span data-stu-id="a8079-323">**Profile type**: Select "Custom"</span></span>

7. <span data-ttu-id="a8079-324">在**自訂 OMA-URI 設定**上，按一下**新增**以新增 ADMX 擷取。</span><span class="sxs-lookup"><span data-stu-id="a8079-324">On **Custom OMA-URI Settings**, click **Add** to add an ADMX ingestion.</span></span>

   ![為 OMA-URI 新增擷取](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-add-omauri.png)

8. <span data-ttu-id="a8079-326">在**新增列**中提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="a8079-326">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="a8079-327">**名稱**：輸入描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-327">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="a8079-328">對於此範例，使用 "Microsoft Edge ADMX 擷取"。</span><span class="sxs-lookup"><span data-stu-id="a8079-328">For this example, use "Microsoft Edge ADMX ingestion".</span></span>
   - <span data-ttu-id="a8079-329">**描述**：輸入設定的選用描述。</span><span class="sxs-lookup"><span data-stu-id="a8079-329">**Description**: Enter an optional description for the setting.</span></span>
   - <span data-ttu-id="a8079-330">**OMA-URI**：輸入 "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span><span class="sxs-lookup"><span data-stu-id="a8079-330">**OMA-URI**: Enter "*./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/Edge/Policy/EdgeAdmx*"</span></span>
   - <span data-ttu-id="a8079-331">**資料類型**：選取 [字串]。</span><span class="sxs-lookup"><span data-stu-id="a8079-331">**Data type**: Select "String"</span></span>
   - <span data-ttu-id="a8079-332">**值**：在選取**資料類型**後，將顯示此輸入區域。</span><span class="sxs-lookup"><span data-stu-id="a8079-332">**Value**: This input area appears after you select the **Data type**.</span></span> <span data-ttu-id="a8079-333">開啟您在步驟 1 中解壓縮的 Microsoft Edge 原則範本檔案中的 msedge.admx 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8079-333">Open the msedge.admx file from the Microsoft Edge policy templates file you extracted in step 1.</span></span> <span data-ttu-id="a8079-334">複製 msedge.admx 檔案中的**所有文字**，並將其貼到以下螢幕截圖中顯示的**值**文字區域中。</span><span class="sxs-lookup"><span data-stu-id="a8079-334">Copy **ALL the text** from the msedge.admx file and paste it in the **Value** text area shown in the following screenshot.</span></span>

        ![新增 ADMX 擷取](./media/edge-cfg-with-mdm/configure-edge-intune-mdm-omauri-addrow-ingest.png)

   - <span data-ttu-id="a8079-336">按一下**確定**。</span><span class="sxs-lookup"><span data-stu-id="a8079-336">Click **OK**.</span></span>

9. <span data-ttu-id="a8079-337">在**自訂 OMA-URI 設定**上，按一下**確定**。</span><span class="sxs-lookup"><span data-stu-id="a8079-337">On **Custom OMA-URI Settings**, click **OK**.</span></span>
10. <span data-ttu-id="a8079-338">在**建立設定檔**上，按一下**建立**。</span><span class="sxs-lookup"><span data-stu-id="a8079-338">On **Create profile**, click **Create**.</span></span> <span data-ttu-id="a8079-339">下一個螢幕截圖顯示有關新建立設定檔的資訊。</span><span class="sxs-lookup"><span data-stu-id="a8079-339">The next screenshot shows information about the newly created profile.</span></span>

    ![<span data-ttu-id="a8079-340">新裝置設定檔資訊</span><span class="sxs-lookup"><span data-stu-id="a8079-340">New device profile information</span></span> ](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-create-profile-done.png)

<!--
> [!NOTE]
> You can use the preceding steps to ingest the msedgeupate.admx policy template file.
-->
### <span data-ttu-id="a8079-341">在 Intune 中使用自訂 OMA-URI 設定原則</span><span class="sxs-lookup"><span data-stu-id="a8079-341">Set a policy using custom OMA-URI in Intune</span></span>

> [!NOTE]
> <span data-ttu-id="a8079-342">在使用本節中的步驟之前，您必須先完成[將 Microsoft Edge ADMX 檔案擷取至 Intune](#ingest-the-microsoft-edge-admx-file-into-intune)中描述的步驟。</span><span class="sxs-lookup"><span data-stu-id="a8079-342">Before using the steps in this section you must complete the steps described in [Ingest the Microsoft Edge ADMX file into Intune](#ingest-the-microsoft-edge-admx-file-into-intune).</span></span>

1. <span data-ttu-id="a8079-343">登入 [Microsoft Azure 入口網站](https://portal.azure.com)。</span><span class="sxs-lookup"><span data-stu-id="a8079-343">Sign in to the [Microsoft Azure portal](https://portal.azure.com).</span></span>
2. <span data-ttu-id="a8079-344">從_所有服務_中選取 **Intune**，或在入口網站搜尋方塊中搜尋 Intune。</span><span class="sxs-lookup"><span data-stu-id="a8079-344">Select **Intune** from _All Services_, or search for Intune in the portal search box.</span></span>
3. <span data-ttu-id="a8079-345">移至 **Intune**>**裝置設定**>**設定檔**。</span><span class="sxs-lookup"><span data-stu-id="a8079-345">Go to **Intune**>**Device configuration**>**Profiles**.</span></span>
4. <span data-ttu-id="a8079-346">選取「Microsoft Edge ADMX 擷取的設定」設定檔或您用於設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-346">Select the "Microsoft Edge ADMX ingested configuration" profile or the name you used for the profile.</span></span>
5. <span data-ttu-id="a8079-347">若要新增 Microsoft Edge 原則設定，您必須開啟**自訂 OMA-URI 設定**。</span><span class="sxs-lookup"><span data-stu-id="a8079-347">To add Microsoft Edge policy settings, you have to open **Custom OMA-URI Settings**.</span></span> <span data-ttu-id="a8079-348">在**管理**下方，依序按一下**內容**和**設定**。</span><span class="sxs-lookup"><span data-stu-id="a8079-348">Under **Manage**, click **Properties**, and then click **Settings**.</span></span>

    ![設定設定檔設定](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings.png)

6. <span data-ttu-id="a8079-350">在**自訂 OMA-URI 設定**下，按一下**新增**。</span><span class="sxs-lookup"><span data-stu-id="a8079-350">On **Custom OMA-URI Settings**, click **Add**.</span></span>

    ![新增列至 OMA-URI 設定](./media/edge-cfg-with-mdm/configure-edge-mdm-intune-add-policy-settings-add-row.png)

7. <span data-ttu-id="a8079-352">在 **新增列**中提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="a8079-352">On **Add Row**, provide the following information:</span></span>

   - <span data-ttu-id="a8079-353">**名稱**：輸入描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-353">**Name**: Enter a descriptive name.</span></span> <span data-ttu-id="a8079-354">我們建議使用您要設定的原則名稱。</span><span class="sxs-lookup"><span data-stu-id="a8079-354">We suggest using the policy name you want to configure.</span></span> <span data-ttu-id="a8079-355">對於此範例，使用 "ShowHomeButton"。</span><span class="sxs-lookup"><span data-stu-id="a8079-355">For this example, use "ShowHomeButton".</span></span>
   - <span data-ttu-id="a8079-356">**描述** (選用)：輸入設定的選用描述。</span><span class="sxs-lookup"><span data-stu-id="a8079-356">**Description** (Optional): Enter a description for the setting.</span></span>
   - <span data-ttu-id="a8079-357">**OMA-URI**：輸入原則的 OMA-URI。</span><span class="sxs-lookup"><span data-stu-id="a8079-357">**OMA-URI**: Enter the OMA-URI for the policy.</span></span> <span data-ttu-id="a8079-358">使用 "ShowHomeButton" 原則作為範例，使用此字串："*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span><span class="sxs-lookup"><span data-stu-id="a8079-358">Using the for "ShowHomeButton" policy as an example, use this string: "*./Device/Vendor/MSFT/Policy/Config/Edge~Policy~microsoft_edge~Startup/ShowHomeButton*"</span></span>
   - <span data-ttu-id="a8079-359">**資料類型**：選取原則設定資料類型。</span><span class="sxs-lookup"><span data-stu-id="a8079-359">**Data type**: Select the policy settings data type.</span></span> <span data-ttu-id="a8079-360">對於 "ShowHomeButton" 原則，使用 [字串]</span><span class="sxs-lookup"><span data-stu-id="a8079-360">For the "ShowHomeButton" policy, use "String"</span></span>
   - <span data-ttu-id="a8079-361">**值**：輸入要為原則設定的設定。</span><span class="sxs-lookup"><span data-stu-id="a8079-361">**Value**: Enter the setting that you want to configure for the policy.</span></span> <span data-ttu-id="a8079-362">對於 "ShowHomeButton" 範例，輸入 "\<enabled/>"。</span><span class="sxs-lookup"><span data-stu-id="a8079-362">For "ShowHomeButton" example, enter "\<enabled/>".</span></span> <span data-ttu-id="a8079-363">下列螢幕擷取畫面顯示設定原則的設定。</span><span class="sxs-lookup"><span data-stu-id="a8079-363">The following screenshot shows the settings for configuring a policy.</span></span>

        ![新增列、自訂 OMA-URI 設定](./media/edge-cfg-with-mdm/configure-edge-mdm-custom-omauri-setting.png)

   - <span data-ttu-id="a8079-365">按一下**確定**。</span><span class="sxs-lookup"><span data-stu-id="a8079-365">Click **OK**.</span></span>

8. <span data-ttu-id="a8079-366">在**自訂 OMA-URI 設定**下，按一下**新增**。</span><span class="sxs-lookup"><span data-stu-id="a8079-366">On **Custom OMA-URI Settings**, click **OK**.</span></span>
9. <span data-ttu-id="a8079-367">在**Microsoft Edge ADMX 擷取的設定 - 內容**設定檔 (或您使用的名稱) 上，按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="a8079-367">On the "**Microsoft Edge ADMX ingested configuration - Properties**" profile (or the name you used), click **Save**.</span></span>

<span data-ttu-id="a8079-368">建立設定檔並設定屬性後，您必須[在 Microsoft Intune 中指派設定檔](https://docs.microsoft.com/intune/configuration/device-profile-assign)。</span><span class="sxs-lookup"><span data-stu-id="a8079-368">After the profile is created and the properties set, you have to [assign the profile in Microsoft Intune](https://docs.microsoft.com/intune/configuration/device-profile-assign).</span></span>

#### <span data-ttu-id="a8079-369">確認原則已設定</span><span class="sxs-lookup"><span data-stu-id="a8079-369">Confirm that the policy was set</span></span>

<span data-ttu-id="a8079-370">使用以下步驟確認 Microsoft Edge 原則是否正在使用您建立的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a8079-370">Use the following steps to confirm that the Microsoft Edge policy is using the profile you created.</span></span> <span data-ttu-id="a8079-371">(請給 Microsoft Intune 一點時間，將原則傳播到您在「Microsoft Edge ADMX 擷取的設定」設定檔範例中指派的裝置。)</span><span class="sxs-lookup"><span data-stu-id="a8079-371">(Give Microsoft Intune time to propagate the policy to a device you assigned in the "Microsoft Edge ADMX ingested configuration" profile example.)</span></span>

1. <span data-ttu-id="a8079-372">開啟 Microsoft Edge，然後移至 *edge://policy*。</span><span class="sxs-lookup"><span data-stu-id="a8079-372">Open Microsoft Edge and go to *edge://policy*.</span></span>
2. <span data-ttu-id="a8079-373">在"**原則"** 頁面上，查看是否列出了您在設定檔中設定的原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-373">On the **Policies** page, see if the policy you set in the profile is listed.</span></span>
3. <span data-ttu-id="a8079-374">如果未顯示原則，請參閱[診斷 Windows 10 中的 MDM 失敗](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10)或[疑難排解原則設定](#troubleshoot-a-policy-setting)。</span><span class="sxs-lookup"><span data-stu-id="a8079-374">If your policy isn't shown, see [Diagnose MDM failures in Windows 10](https://docs.microsoft.com/windows/client-management/mdm/diagnose-mdm-failures-in-windows-10) or [Troubleshoot a policy setting](#troubleshoot-a-policy-setting).</span></span>

#### <span data-ttu-id="a8079-375">疑難排解原則設定</span><span class="sxs-lookup"><span data-stu-id="a8079-375">Troubleshoot a policy setting</span></span>

<span data-ttu-id="a8079-376">如果 Microsoft Edge 原則未生效，請嘗試以下步驟：</span><span class="sxs-lookup"><span data-stu-id="a8079-376">If a Microsoft Edge policy isn’t taking effect, try the following steps:</span></span>

<span data-ttu-id="a8079-377">開啟目標裝置上的 *edge://policy* 頁面 (您在 Microsoft Intune 中指派設定檔的裝置) 並搜尋原則。</span><span class="sxs-lookup"><span data-stu-id="a8079-377">Open the *edge://policy* page on the target device (a device you assigned the profile to in Microsoft Intune) and search for the policy.</span></span> <span data-ttu-id="a8079-378">如果原則不在 *edge://policy* 頁面上，請嘗試以下操作：</span><span class="sxs-lookup"><span data-stu-id="a8079-378">If the policy isn’t on the *edge://policy* page, try the following:</span></span>

- <span data-ttu-id="a8079-379">檢查原則是否位於登錄中且是否正確。</span><span class="sxs-lookup"><span data-stu-id="a8079-379">Check that the policy is in the registry and is correct.</span></span> <span data-ttu-id="a8079-380">在目標裝置上開啟 Windows 10 登錄編輯程式 (**Windows 鍵 + r**，輸入「*regedit*」，然後按 **Enter**)。檢查原則是否在 *\Software\Policies\ Microsoft\Edge* 路徑中正確定義。</span><span class="sxs-lookup"><span data-stu-id="a8079-380">On the target device open the Windows 10 Registry Editor (**Windows key + r**, enter “*regedit*” and then press **Enter**.) Check that the policy is correctly defined in the *\Software\Policies\ Microsoft\Edge* path.</span></span> <span data-ttu-id="a8079-381">如果在預期路徑中找不到原則，則原則未正確推送到裝置。</span><span class="sxs-lookup"><span data-stu-id="a8079-381">If you don’t find the policy in the expected path, then the policy wasn’t pushed to the device correctly.</span></span>
- <span data-ttu-id="a8079-382">檢查 OMA-URI 路徑是否正確，並且該值是有效的 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="a8079-382">Check that the OMA-URI path is correct, and the value is a valid XML string.</span></span> <span data-ttu-id="a8079-383">如果其中任一不正確，則原則不會推送到目標裝置。</span><span class="sxs-lookup"><span data-stu-id="a8079-383">If either of these are incorrect the policy won’t be pushed to the target device.</span></span>

<span data-ttu-id="a8079-384">如需更多疑難排解祕訣，請參閱[設定 Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps)和[同步裝置](https://docs.microsoft.com/intune/remote-actions/device-sync)。</span><span class="sxs-lookup"><span data-stu-id="a8079-384">For more trouble shooting tips, see [Set up Microsoft Intune](https://docs.microsoft.com/intune/fundamentals/setup-steps) and [Sync devices](https://docs.microsoft.com/intune/remote-actions/device-sync).</span></span>

## <span data-ttu-id="a8079-385">也請參閱</span><span class="sxs-lookup"><span data-stu-id="a8079-385">See also</span></span>

- [<span data-ttu-id="a8079-386">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="a8079-386">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="a8079-387">使用 Microsoft Intune 設定 Microsoft Edge 原則設定</span><span class="sxs-lookup"><span data-stu-id="a8079-387">Configure Microsoft Edge policy settings with Microsoft Intune</span></span>](configure-edge-with-intune.md)
- [<span data-ttu-id="a8079-388">行動裝置管理</span><span class="sxs-lookup"><span data-stu-id="a8079-388">Mobile device management</span></span>](https://docs.microsoft.com/windows/client-management/mdm/)
- [<span data-ttu-id="a8079-389">使用 Intune 中 Windows 10 裝置的自訂設定</span><span class="sxs-lookup"><span data-stu-id="a8079-389">Use custom settings for Windows 10 devices in Intune</span></span>](https://docs.microsoft.com/intune/configuration/custom-settings-windows-10)
- [<span data-ttu-id="a8079-390">Win32 與傳統型橋接器應用程式原則設定</span><span class="sxs-lookup"><span data-stu-id="a8079-390">Win32 and Desktop Bridge app policy configuration</span></span>](https://docs.microsoft.com/windows/client-management/mdm/win32-and-centennial-app-policy-configuration)
- [<span data-ttu-id="a8079-391">了解 ADMX 支援的原則</span><span class="sxs-lookup"><span data-stu-id="a8079-391">Understanding ADMX-backed policies</span></span>](https://docs.microsoft.com/windows/client-management/mdm/understanding-admx-backed-policies)
