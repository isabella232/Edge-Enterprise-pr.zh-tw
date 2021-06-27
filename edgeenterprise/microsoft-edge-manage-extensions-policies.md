---
title: 使用群組原則管理 Microsoft Edge 擴充功能
ms.author: aspoddar
author: AndreaLBarr
manager: balajek
ms.date: 06/09/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 在企業中使用群組原則管理 Microsoft Edge 擴充功能
ms.openlocfilehash: a633b036c1733716dfb257b4711bca57bd6721f0
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618073"
---
# <a name="use-group-policies-to-manage-microsoft-edge-extensions"></a><span data-ttu-id="da18d-103">使用群組原則管理 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-103">Use group policies to manage Microsoft Edge extensions</span></span>

<span data-ttu-id="da18d-104">本文將說明使用群組原則管理擴充功能的選項和步驟。</span><span class="sxs-lookup"><span data-stu-id="da18d-104">This article describes the options and steps for managing extensions by using group policies.</span></span> <span data-ttu-id="da18d-105">這些選項假設您已經為使用者管理 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="da18d-105">These options  assume that you already have Microsoft Edge managed for your users.</span></span> <span data-ttu-id="da18d-106">如果您尚未設定要為使用者管理的 Microsoft Edge，請遵循下列連結立即進行。</span><span class="sxs-lookup"><span data-stu-id="da18d-106">If you have not already set up Microsoft Edge to be managed for your users please follow the below link to do so now.</span></span>

- [<span data-ttu-id="da18d-107">在企業中管理 Microsoft Edge 的擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-107">Manage Microsoft Edge extensions in the enterprise</span></span>](/deployedge/microsoft-edge-manage-extensions)

> [!NOTE]
> <span data-ttu-id="da18d-108">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="da18d-108">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="block-extensions-based-on-their-permissions"></a><span data-ttu-id="da18d-109">根據擴充功能的權限封鎖擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-109">Block extensions based on their permissions</span></span>

<span data-ttu-id="da18d-110">您可以使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則，根據權限來控制使用者可以安裝的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-110">You can control what extensions your users can install based on permissions using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span> <span data-ttu-id="da18d-111">如果已安裝的擴充功能需要的權限已遭封鎖，就不會執行該擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-111">If an installed extension needs a permission that’s blocked, it just won't run.</span></span> <span data-ttu-id="da18d-112">不會移除擴充功能，只會停用。</span><span class="sxs-lookup"><span data-stu-id="da18d-112">The extension isn't removed, just disabled.</span></span>

> [!NOTE]
> <span data-ttu-id="da18d-113">只能在擴充功能設定原則內設定遭封鎖的權限設定。</span><span class="sxs-lookup"><span data-stu-id="da18d-113">The blocked permissions setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="da18d-114">使用下列步驟做為封鎖擴充功能的指南。</span><span class="sxs-lookup"><span data-stu-id="da18d-114">Use the following steps as a guide for blocking an extension.</span></span>

1. <span data-ttu-id="da18d-115">開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]\*\*\*\*，然後選取 [設定擴充功能管理設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-115">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**  and then select **Configure extension management settings**.</span></span>
2. <span data-ttu-id="da18d-116">啟用該原則，然後使用壓縮的 JSON 字串輸入您想要允許或封鎖的權限。</span><span class="sxs-lookup"><span data-stu-id="da18d-116">Enable the policy, then enter the permissions that you want allowed or blocked, by using a JSON string that gets compressed.</span></span> <span data-ttu-id="da18d-117">下一個螢幕擷取畫面顯示如何封鎖使用 "usb" 權限的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-117">The next screenshot shows how to block an extension that uses the permission "usb".</span></span>

    :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-1.png" alt-text="設定群組原則以封鎖擴充功能。":::

<span data-ttu-id="da18d-119">下列範例顯示 JSON 以封鎖任何需要使用權限 "usb" 及其壓縮字串的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-119">The following example shows the JSON to block any extension that needs the use of permission "usb" and its compressed string.</span></span>

### <a name="json-example"></a><span data-ttu-id="da18d-120">JSON 範例</span><span class="sxs-lookup"><span data-stu-id="da18d-120">JSON example</span></span>

   ```json
   { 
        "*": { 
             "blocked_permissions": ["usb"] 
        } 
   } 
   ```

   ```json
   {"*":{"blocked_permissions":["usb"]}} 
   ```

   > [!NOTE]
   > <span data-ttu-id="da18d-121">若要封鎖所有使用該權限的擴充功能，請使用星號作為擴充功能識別碼，如上一個範例所示。</span><span class="sxs-lookup"><span data-stu-id="da18d-121">To block all extensions that use the permission, use an asterisk for the extension ID, as shown in the previous example.</span></span> <span data-ttu-id="da18d-122">如果您指定一個擴充識別碼，原則只會套用至該擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-122">If you specify one extension ID, the policy will only apply to that extension.</span></span> <span data-ttu-id="da18d-123">您可以封鎖多個擴充功能，但這些擴充功能必須是個別項目。</span><span class="sxs-lookup"><span data-stu-id="da18d-123">You can block more than one, but they need to be separate entries.</span></span>

## <a name="prevent-extensions-from-altering-web-pages"></a><span data-ttu-id="da18d-124">防止擴充功能變更網頁</span><span class="sxs-lookup"><span data-stu-id="da18d-124">Prevent extensions from altering web pages</span></span>

<span data-ttu-id="da18d-125">此設定可防止擴充功能讀取及變更來自敏感網站和網域的資料。</span><span class="sxs-lookup"><span data-stu-id="da18d-125">This setting prevents extensions from reading and changing  data from sensitive websites and domains.</span></span> <span data-ttu-id="da18d-126">封鎖不想要的動作是透過封鎖以下動作來完成：指令碼插入您的網站、讀取 Cookie 或進行網路要求修改。</span><span class="sxs-lookup"><span data-stu-id="da18d-126">Blocking unwanted actions is done by blocking actions such as script injection into your websites, reading the cookies, or making web-request modifications.</span></span> <span data-ttu-id="da18d-127">此設定不會阻止使用者安裝或移除擴充功能，只會防止擴充功能變更指定的網站。</span><span class="sxs-lookup"><span data-stu-id="da18d-127">This setting doesn’t prevent your users from installing or removing extensions, it only prevents extensions from altering the specified websites.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="da18d-128">只能在擴充功能設定原則內設定執行階段允許/封鎖主機設定。</span><span class="sxs-lookup"><span data-stu-id="da18d-128">The Runtime allowed/blocked hosts setting can only be set within the extension settings policy.</span></span>  

<span data-ttu-id="da18d-129">您可以在 ExtensionSettings 原則中設定下列設定，以防止 (或允許) 變更網站或網域：</span><span class="sxs-lookup"><span data-stu-id="da18d-129">You can configure the following settings in the ExtensionSettings policy to prevent (or allow) alterations of websites or domains:</span></span>

- <span data-ttu-id="da18d-130">**Runtime_blocked_hosts**。</span><span class="sxs-lookup"><span data-stu-id="da18d-130">**Runtime_blocked_hosts**.</span></span> <span data-ttu-id="da18d-131">此設定會阻止擴充功能進行變更，或從您指定的網站讀取資料。</span><span class="sxs-lookup"><span data-stu-id="da18d-131">This setting blocks extensions from making changes or reading data from the websites you specify.</span></span>
- <span data-ttu-id="da18d-132">**Runtime_allowed_hosts**。</span><span class="sxs-lookup"><span data-stu-id="da18d-132">**Runtime_allowed_hosts**.</span></span> <span data-ttu-id="da18d-133">此設定可允許擴充功能進行變更，或從您指定的網站讀取資料。</span><span class="sxs-lookup"><span data-stu-id="da18d-133">This setting allows extensions to make changes or read data from the websites you specify.</span></span> <span data-ttu-id="da18d-134">以下格式用於在原則的 JSON 字串中指定您的網站：</span><span class="sxs-lookup"><span data-stu-id="da18d-134">The following format is used for specifying your site(s) in the JSON string in the policy:</span></span>

  ```json
  [http|https|ftp|*]://[subdomain|*].[hostname|*].[eTLD|*] [http|https|ftp|*],
  ```

  > [!NOTE]
  > `[hostname|*], and [eTLD|*]` <span data-ttu-id="da18d-135">區段為必要項目，但 `[subdomain|*]` 區段為選用。</span><span class="sxs-lookup"><span data-stu-id="da18d-135">sections are required, but `[subdomain|*]` section is optional.</span></span>

<span data-ttu-id="da18d-136">下表顯示有效的主機模式和相符模式的範例。</span><span class="sxs-lookup"><span data-stu-id="da18d-136">The following table shows examples of valid host patterns and matching patterns.</span></span>

|<span data-ttu-id="da18d-137">有效的主機模式</span><span class="sxs-lookup"><span data-stu-id="da18d-137">Valid host patterns</span></span>|<span data-ttu-id="da18d-138">相符項目</span><span class="sxs-lookup"><span data-stu-id="da18d-138">Matches</span></span>|<span data-ttu-id="da18d-139">不相符</span><span class="sxs-lookup"><span data-stu-id="da18d-139">Doesn't match</span></span>|
|--|--|--|
|  `*://*.example.*` | `http://example.com`<br>`https://test.example.co.uk`   | `https://example.microsoft.com`<br>`http://example.microsoft.co.uk`  |
| `http://example.*` | `http://example.com`<br>`http://example.ly` | `https://example.com`<br>`http://test.example.com`   |
| `http://example.com`   | `http://example.com` | `https://example.com`<br>`http://test.example.co.uk` |
| `*://*`   | <span data-ttu-id="da18d-140">所有 URL</span><span class="sxs-lookup"><span data-stu-id="da18d-140">All URLs</span></span>  |   |

<span data-ttu-id="da18d-141">使用下列步驟做為封鎖或允許擴充功能存取網站或網域的指南。</span><span class="sxs-lookup"><span data-stu-id="da18d-141">Use the following steps as a guide to block or allow extensions to access a website or domain.</span></span>

1. <span data-ttu-id="da18d-142">開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]\*\*\*\*，然後選取 [設定擴充功能管理設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-142">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions**, and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="da18d-143">啟用該原則，然後輸入您想要允許或封鎖的權限，將權限壓縮為單一 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="da18d-143">Enable the policy, then enter the permissions that you want allowed or blocked, compressing the permissions to a single JSON string.</span></span>

<span data-ttu-id="da18d-144">下列範例顯示如何封鎖主機名稱上的擴充功能，以及如何封鎖同一個網域上的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-144">The following examples show how to block extensions on a hostname and how to block extensions on the same domain.</span></span>

### <a name="json-example-to-block-hostname"></a><span data-ttu-id="da18d-145">封鎖主機名稱的 JSON 範例</span><span class="sxs-lookup"><span data-stu-id="da18d-145">JSON example to block hostname</span></span>

<span data-ttu-id="da18d-146">此範例顯示 JSON 和壓縮的 JSON 字串，以封鎖任何擴充功能，禁止其存取 `www.microsoft.com` 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="da18d-146">This example shows the JSON and compressed JSON string to block any extension from accessing the `www.microsoft.com` hostname.</span></span>

```json
{ 
    "*":{ 
            "runtime_blocked_hosts":["www.microsoft.com"] 
    } 
} 
```

```json
{"*":{"runtime_blocked_hosts":["www.microsoft.com"]}} 
```

> [!NOTE]
> <span data-ttu-id="da18d-147">若要封鎖所有擴充功能存取網頁，請使用星號作為擴充功能識別碼，如上一個範例所示。</span><span class="sxs-lookup"><span data-stu-id="da18d-147">To block all extensions from accessing a webpage, use an asterisk for the extension ID, as shown in the previous example.</span></span>  <span data-ttu-id="da18d-148">如果您指定一個擴充識別碼而不指定星號，原則只會套用至該擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-148">If you specify one extension ID instead of an asterisk, the policy will only apply to that extension.</span></span> <span data-ttu-id="da18d-149">您可以封鎖多個擴充功能，但這些擴充功能必須是個別項目。</span><span class="sxs-lookup"><span data-stu-id="da18d-149">You can block more than one extension, but they need to be separate entries.</span></span>

### <a name="json-example-to-block-extensions-on-same-domain"></a><span data-ttu-id="da18d-150">JSON 範例，可封鎖相同網域上的擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-150">JSON example to block extensions on same domain</span></span>

<span data-ttu-id="da18d-151">此範例顯示 JSON 和壓縮的 JSON 字串，以封鎖特定擴充功能在相同網域 "importantwebsite" 上執行。</span><span class="sxs-lookup"><span data-stu-id="da18d-151">This example shows the JSON and compressed JSON string to block specific extensions from running on the same domain, "importantwebsite".</span></span>

```json
{ 
    "aapbdbdomjkkjkaonfhkkikfgjllcleb": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    }, 
    "bfbmjmiodbnnpllbbbfblcplfjjepjdn": { 
        "runtime_blocked_hosts": ["*://*.importantwebsite"] 
    } 
} 
```

```json
{"aapbdbdomjkkjkaonfhkkikfgjllcleb": {"runtime_blocked_hosts": ["*://,*.importantwebsite"]},"bfbmjmiodbnnpllbbbfblcplfjjepjdn": {"runtime_blocked_hosts": ["*://*.importantwebsite"]}} 
```

## <a name="allow-or-block-extensions-in-group-policy"></a><span data-ttu-id="da18d-152">在群組原則中允許或封鎖擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-152">Allow or block extensions in group policy</span></span>

<span data-ttu-id="da18d-153">您可以使用 [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) 和 [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) 原則來控制要封鎖或允許的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-153">You can use the [ExtensionInstallBlocklist](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist) and [ExtensionInstallAllowlist](/DeployEdge/microsoft-edge-policies#extensioninstallallowlist) policies to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="da18d-154">使用下列步驟做為指南，以允許所有擴充功能，除了您想要封鎖的擴充功能之外。</span><span class="sxs-lookup"><span data-stu-id="da18d-154">Use the following steps as a guide to allow all extensions except those you want to block.</span></span>

1. <span data-ttu-id="da18d-155">開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]\*\*\*\*，然後選取 [控制不能安裝哪些擴充程式]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-155">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Control which extensions cannot be installed**.</span></span>
2. <span data-ttu-id="da18d-156">選取 [啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-156">Select **Enabled**.</span></span>
3. <span data-ttu-id="da18d-157">按一下 [顯示]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-157">Click **Show**.</span></span>
4. <span data-ttu-id="da18d-158">輸入要封鎖之擴充功能的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="da18d-158">Enter the app ID of the extensions that you want to block.</span></span> <span data-ttu-id="da18d-159">新增多個應用程式識別碼時，請針對每個識別碼使用個別列。</span><span class="sxs-lookup"><span data-stu-id="da18d-159">When adding multiple app ID’s use a separate row for each ID.</span></span>
5. <span data-ttu-id="da18d-160">若要封鎖所有擴充功能，請將 **\*** 輸入該原則，以防止安裝任何擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-160">To block all extensions, type **\*** into the policy to prevent any extensions from being installed.</span></span> <span data-ttu-id="da18d-161">您可以結合 [允許特定安裝擴充功能] 原則來使用這項功能，以只允許安裝特定擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-161">You can use this in conjunction with the "Allow specific extensions to be installed" policy to only allow certain extensions to be installed.</span></span> <span data-ttu-id="da18d-162">下一個螢幕擷取畫面顯示將根據提供的應用程式識別碼封鎖的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-162">The next screenshot shows an extension that will be blocked based on the app ID that's provided.</span></span>

   :::image type="content" source="media/microsoft-edge-manage-extensions-policies/manage-extensions-gp-block-2.png" alt-text="使用應用程式識別碼封鎖擴充功能。":::

   > [!TIP]
   > <span data-ttu-id="da18d-164">如果您找不到擴充功能的應用程式識別碼，請查詢 Microsoft Edge 附加元件網站中的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-164">If you can’t find the app ID of an extension, look at the extension in the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="da18d-165">找到特定的擴充功能，您將在 omnibox 的 URL 結尾看到應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="da18d-165">Find the specific extension and you will see the app ID at the end of the URL in the omnibox.</span></span>

> [!NOTE]
> <span data-ttu-id="da18d-166">您可以在使用者電腦上安裝的封鎖清單中新增擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-166">You can add an extension to the blocklist that’s already installed on a user’s computer.</span></span> <span data-ttu-id="da18d-167">這將停用擴充功能，並防止使用者重新啟用它。</span><span class="sxs-lookup"><span data-stu-id="da18d-167">This will disable the extension and prevent the user from re-enabling it.</span></span> <span data-ttu-id="da18d-168">不會解除安裝擴充功能，只會停用。</span><span class="sxs-lookup"><span data-stu-id="da18d-168">It won't be uninstalled, just disabled.</span></span>

## <a name="force-install-an-extension"></a><span data-ttu-id="da18d-169">強制安裝擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-169">Force-install an extension</span></span>

<span data-ttu-id="da18d-170">使用 [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) 原則來控制要封鎖或允許的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-170">Use the [ExtensionInstallForcelist](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist) policy to control which extensions are blocked or allowed.</span></span> <span data-ttu-id="da18d-171">使用下列步驟做為強制安裝擴充功能的指南。</span><span class="sxs-lookup"><span data-stu-id="da18d-171">Use the following steps as a guide to force-install an extension.</span></span>

1. <span data-ttu-id="da18d-172">在 [群組原則編輯器] 中，移至 [系統管理範本 > Microsoft Edge > 擴充功能]\*\*\*\*，然後選取 [控制哪些擴充功能會默默地安裝]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-172">In the Group Policy Editor, go to **Administrative Templates> Microsoft Edge >  Extensions >** and then select **Control which extensions are installed silently**.</span></span>
2. <span data-ttu-id="da18d-173">選取 [啟用]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-173">Select **Enabled**.</span></span>  
3. <span data-ttu-id="da18d-174">按一下 [顯示]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-174">Click **Show**.</span></span>
4. <span data-ttu-id="da18d-175">輸入要強制安裝的擴充功能的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="da18d-175">Enter the app ID or IDs of the extension or extensions you want to force-install.</span></span>  

<span data-ttu-id="da18d-176">擴充功能將自動安裝，不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="da18d-176">The extension will be installed silently with no need for user interaction.</span></span> <span data-ttu-id="da18d-177">使用者也將無法解除安裝或停用擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-177">The user also won’t be able to uninstall or disable the extension.</span></span> <span data-ttu-id="da18d-178">此設定會覆寫任何已啟用的封鎖清單原則。</span><span class="sxs-lookup"><span data-stu-id="da18d-178">This setting will overwrite over any blocklist policy that’s enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="da18d-179">對於在 Chrome線上應用程式商店中託管的擴充功能，請使用字串，例如：`pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`。</span><span class="sxs-lookup"><span data-stu-id="da18d-179">For extensions hosted in the Chrome web store use a string such as: `pckdojakecnhhplcgfflhndiffaohfah;https://clients2.google.com/service/update2/crx`.</span></span>

## <a name="block-extensions-from-a-specific-store-or-update-url"></a><span data-ttu-id="da18d-180">封鎖來自特定商店或更新 URL 的擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-180">Block extensions from a specific store or update URL</span></span>

<span data-ttu-id="da18d-181">若要封鎖來自特定商店或 URL 的擴充功能，您只需要使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則封鎖該商店的 *update_url* 即可。</span><span class="sxs-lookup"><span data-stu-id="da18d-181">To block extensions from a particular store or URL, you only need to block the *update_url* for that store using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

<span data-ttu-id="da18d-182">使用下列步驟做為指南，以封鎖來自特定商店或 URL 的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="da18d-182">Use the following steps as a guide to block extensions from an particular store or URL.</span></span>

1. <span data-ttu-id="da18d-183">開啟 [群組原則管理編輯器]，然後前往 [系統管理範本 > Microsoft Edge > 擴充功能]\*\*\*\*，然後選取 [設定擴充功能管理設定]\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="da18d-183">Open the group policy management editor and go to **Administrative Templates > Microsoft Edge > Extensions >** and then select **Configure extension management settings**.</span></span>  
2. <span data-ttu-id="da18d-184">啟用該原則，然後輸入您想要允許或封鎖的權限，將權限壓縮為單一 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="da18d-184">Enable the policy, then enter the permissions that you want allowed or blocked, compressing it to a single JSON string.</span></span>

<span data-ttu-id="da18d-185">下一個範例顯示 JSON 和壓縮的 JSON 字串，以使用其更新 URL (`https://clients2.google.com/service/update2/crx`) 封鎖 Chrome 線上應用程式商店。</span><span class="sxs-lookup"><span data-stu-id="da18d-185">The next example shows the JSON and compressed JSON string to block from the Chrome Web Store using its update URL (`https://clients2.google.com/service/update2/crx`).</span></span>

### <a name="json-example-for-blocking-on-update-url"></a><span data-ttu-id="da18d-186">封鎖更新 URL 的 JSON 範例</span><span class="sxs-lookup"><span data-stu-id="da18d-186">JSON example for blocking on update URL</span></span>

```json
{ 
"update_url:https://clients2.google.com/service/update2/crx":{ 
                                                             " installation_mode":"blocked" 
                                                             } 
} 
```

```json
{"update_url:https://clients2.google.com/service/update2/crx":{"installation_mode":"blocked"}} 
```

> [!NOTE]
> <span data-ttu-id="da18d-187">您仍然可以使用 **ExtensionInstallForceList** 和 **ExtensionInstallAllowList** 來允許/強制安裝特定擴充功能，即使是在前一個範例中已使用 JSON 來封鎖商店。</span><span class="sxs-lookup"><span data-stu-id="da18d-187">You can still use **ExtensionInstallForceList** and **ExtensionInstallAllowList** to allow/force install specific extensions even if the store is blocked using the JSON in the previous example.</span></span>

## <a name="see-also"></a><span data-ttu-id="da18d-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da18d-188">See also</span></span>

- [<span data-ttu-id="da18d-189">在企業中管理 Microsoft Edge 的擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-189">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="da18d-190">建立線上應用程式商店以託管 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="da18d-190">Create a web store to host Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-webstore.md)
- [<span data-ttu-id="da18d-191">ExtensionSettings 原則的參考指南</span><span class="sxs-lookup"><span data-stu-id="da18d-191">Reference guide for the ExtensionSettings policy</span></span>](microsoft-edge-manage-extensions-ref-guide.md)
- [<span data-ttu-id="da18d-192">Microsoft Edge 擴充功能常見問題集</span><span class="sxs-lookup"><span data-stu-id="da18d-192">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="da18d-193">Microsoft Edge 企業版登陸頁面</span><span class="sxs-lookup"><span data-stu-id="da18d-193">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
