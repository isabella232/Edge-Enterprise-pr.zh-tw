---
title: ExtensionSettings 原則的詳細指南
ms.author: aspoddar
author: dan-wesley
manager: balajek
ms.date: 03/31/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 使用 ExtensionSettings 原則設定 Microsoft Edge 擴充功能的詳細參考指南。
ms.openlocfilehash: 89ff329d6e209a4e658907385ec24fd0d2f1d1c2
ms.sourcegitcommit: 4192328ee585bc32a9be528766b8a5a98e046c8e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/25/2021
ms.locfileid: "11618072"
---
# <a name="detailed-guide-to-the-extensionsettings-policy"></a><span data-ttu-id="38e36-103">ExtensionSettings 原則的詳細指南</span><span class="sxs-lookup"><span data-stu-id="38e36-103">Detailed guide to the ExtensionSettings policy</span></span>

<span data-ttu-id="38e36-104">Microsoft Edge 提供多種管理擴充功能的方法。</span><span class="sxs-lookup"><span data-stu-id="38e36-104">Microsoft Edge offers multiple ways to manage extensions.</span></span> <span data-ttu-id="38e36-105">一般的方法就是使用 JSON 字串在 Windows 群組原則編輯器或 Windows 登錄中，在單一位置使用 [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) 原則設定多個策原則。</span><span class="sxs-lookup"><span data-stu-id="38e36-105">A common way is to set multiple policies in one place with a JSON string in the Windows Group Policy Editor or in the Windows Registry using the [ExtensionSettings](/deployedge/microsoft-edge-policies#extensionsettings) policy.</span></span>

> [!NOTE]
> <span data-ttu-id="38e36-106">本文適用於 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="38e36-106">This article applies to Microsoft Edge version 77 or later.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="38e36-107">開始之前</span><span class="sxs-lookup"><span data-stu-id="38e36-107">Before you begin</span></span>

<span data-ttu-id="38e36-108">您可以決定是否要在這裡設定所有擴充功能管理設定，或透過其他原則設定這些控制項。</span><span class="sxs-lookup"><span data-stu-id="38e36-108">You decide if you want to set all extension management settings here or set these controls through other policies.</span></span>
  
<span data-ttu-id="38e36-109">ExtensionSettings 原則可以覆寫您設定在群組原則中其他位置的其他原則，包括下列原則：</span><span class="sxs-lookup"><span data-stu-id="38e36-109">The ExtensionSettings policy can overwrite other policies that you've set elsewhere in group policy, including the following policies:</span></span>

- [<span data-ttu-id="38e36-110">ExtensionAllowedTypes</span><span class="sxs-lookup"><span data-stu-id="38e36-110">ExtensionAllowedTypes</span></span>](/DeployEdge/microsoft-edge-policies#extensionallowedtypes)
- [<span data-ttu-id="38e36-111">ExtensionInstallBlocklist</span><span class="sxs-lookup"><span data-stu-id="38e36-111">ExtensionInstallBlocklist</span></span>](/DeployEdge/microsoft-edge-policies#extensioninstallblocklist)
- [<span data-ttu-id="38e36-112">ExtensionInstallForcelist</span><span class="sxs-lookup"><span data-stu-id="38e36-112">ExtensionInstallForcelist</span></span>](/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [<span data-ttu-id="38e36-113">ExtensionInstallSources</span><span class="sxs-lookup"><span data-stu-id="38e36-113">ExtensionInstallSources</span></span>](/DeployEdge/microsoft-edge-policies#extensioninstallsources)
- [<span data-ttu-id="38e36-114">ExtensionInstallAllowlist</span><span class="sxs-lookup"><span data-stu-id="38e36-114">ExtensionInstallAllowlist</span></span>](/DeployEdge/microsoft-edge-policies#extensioninstallsources)

## <a name="extensionsettings-policy-fields"></a><span data-ttu-id="38e36-115">ExtensionSettings 原則欄位</span><span class="sxs-lookup"><span data-stu-id="38e36-115">ExtensionSettings policy fields</span></span>

<span data-ttu-id="38e36-116">此原則可以控制設定，例如更新 URL、可從其中下載擴充功能進行初次安裝，以及封鎖權限，或不允許執行哪些權限。</span><span class="sxs-lookup"><span data-stu-id="38e36-116">This policy can control settings such as Update URL, where the extension will be downloaded from for initial install, and Blocked permissions, or which permissions aren't allowed to run.</span></span> <span data-ttu-id="38e36-117">下表說明可用的原則欄位。</span><span class="sxs-lookup"><span data-stu-id="38e36-117">The available policy fields are described in the following table.</span></span>

| &nbsp; | <span data-ttu-id="38e36-118">說明</span><span class="sxs-lookup"><span data-stu-id="38e36-118">Description</span></span> |
|--|--|
| **<span data-ttu-id="38e36-119">allowed_types</span><span class="sxs-lookup"><span data-stu-id="38e36-119">allowed_types</span></span>** | <span data-ttu-id="38e36-120">只能用來設定預設設定 \*。</span><span class="sxs-lookup"><span data-stu-id="38e36-120">Can only be used to configure the default configuration, \*.</span></span> <span data-ttu-id="38e36-121">指定允許使用者在 Microsoft Edge 上安裝的應用程式或擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-121">Specifies what types of app or extension users are allowed to install on Microsoft Edge.</span></span> <span data-ttu-id="38e36-122">該值是字串清單，每個字串應該為下列其中一種類型：「extension」、「theme」、「user_script」和「hosted_app」。</span><span class="sxs-lookup"><span data-stu-id="38e36-122">The value is a list of strings, each of which should be one of the following types: "extension", "theme", "user_script", and "hosted_app"</span></span>   |
| **<span data-ttu-id="38e36-123">blocked_install_message</span><span class="sxs-lookup"><span data-stu-id="38e36-123">blocked_install_message</span></span>**| <span data-ttu-id="38e36-124">如果您封鎖使用者安裝特定擴充功能，您可以指定自訂訊息，如果使用者嘗試安裝，該訊息會在瀏覽器中顯示。</span><span class="sxs-lookup"><span data-stu-id="38e36-124">If you block users from installing certain extensions, you can specify a custom message to display in the browser if users try to install them.</span></span><br><span data-ttu-id="38e36-125">將文字附加到 Microsoft Edge 外掛程式網站上顯示的一般錯誤訊息文字。</span><span class="sxs-lookup"><span data-stu-id="38e36-125">Append text to the generic error message that is displayed on the Microsoft Edge Add-ons website.</span></span> <span data-ttu-id="38e36-126">例如，您可以告訴使用者如何與 IT 部門連絡，或特定擴充功能無法使用的原因。</span><span class="sxs-lookup"><span data-stu-id="38e36-126">For example, you can tell users how to contact their IT department or why a particular extension is unavailable.</span></span> <span data-ttu-id="38e36-127">訊息最多 1,000 個字元。</span><span class="sxs-lookup"><span data-stu-id="38e36-127">The message can be up to 1,000 characters long.</span></span>   |
|**<span data-ttu-id="38e36-128">blocked_permissions</span><span class="sxs-lookup"><span data-stu-id="38e36-128">blocked_permissions</span></span>**  | <span data-ttu-id="38e36-129">防止使用者安裝及執行要求貴組織不允許之特定 API 權限的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-129">Prevents users from installing and running extensions that request certain API permissions that your organization doesn’t allow.</span></span> <span data-ttu-id="38e36-130">例如，您可以封鎖存取 Cookie 的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-130">For example, you can block extensions that access cookies.</span></span> <span data-ttu-id="38e36-131">如果擴充功能需要您封鎖的權限，使用者無法安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-131">If an extension requires a permission that you blocked, the user can’t install it.</span></span> <span data-ttu-id="38e36-132">如果使用者先前已安裝擴充功能，它將不再載入。</span><span class="sxs-lookup"><span data-stu-id="38e36-132">If users previously installed the extension, it will no longer load.</span></span> <span data-ttu-id="38e36-133">如果擴充功能包含封鎖的權限為選擇性需求，它會如往常一樣安裝。</span><span class="sxs-lookup"><span data-stu-id="38e36-133">If an extension contains a blocked permission as an optional requirement, it installs as usual.</span></span> <span data-ttu-id="38e36-134">接著，當擴充功能執行時，系統會自動拒絕封鎖的權限。</span><span class="sxs-lookup"><span data-stu-id="38e36-134">Then, while the extension is running, blocked permissions are automatically declined.</span></span><br><span data-ttu-id="38e36-135">有關可用權限的清單，請參閱[宣告權限](/microsoft-edge/extensions-chromium/enterprise/declare-permissions)。</span><span class="sxs-lookup"><span data-stu-id="38e36-135">For a list of available permissions, see [declare permissions](/microsoft-edge/extensions-chromium/enterprise/declare-permissions).</span></span>   |
| **<span data-ttu-id="38e36-136">installation_mode</span><span class="sxs-lookup"><span data-stu-id="38e36-136">installation_mode</span></span>**| <span data-ttu-id="38e36-137">控制您指定的擴充功能是否及如何新增到 Microsoft Edge。</span><span class="sxs-lookup"><span data-stu-id="38e36-137">Controls if and how extensions that you specify are added to Microsoft Edge.</span></span> <span data-ttu-id="38e36-138">您可以將安裝模式設定為下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="38e36-138">You can set the installation mode to one of the following options:</span></span><br><span data-ttu-id="38e36-139">- allowed：使用者可以安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-139">- allowed: Users can install the extension.</span></span> <span data-ttu-id="38e36-140">如果未定義安裝模式，則此設定為預設值。</span><span class="sxs-lookup"><span data-stu-id="38e36-140">If no installation mode is defined, this setting is the default.</span></span><br><span data-ttu-id="38e36-141">- blocked：使用者無法安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-141">- blocked: Users can’t install the extension.</span></span><br><span data-ttu-id="38e36-142">- force_installed：自動安裝擴充功能，而不需要使用者互動。</span><span class="sxs-lookup"><span data-stu-id="38e36-142">- force_installed: Automatically install the extension without user interaction.</span></span> <span data-ttu-id="38e36-143">使用者無法移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-143">Users can’t remove it.</span></span> <span data-ttu-id="38e36-144">您也需要使用 update_url 定義擴充功能下載位置。</span><span class="sxs-lookup"><span data-stu-id="38e36-144">You also need to define the extension download location using update_url.</span></span> <span data-ttu-id="38e36-145">**注意**：此設定無法使用 \*，因為Microsoft Edge 無法知道要自動安裝哪個擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-145">**Note**: You can’t use this setting with \* because Microsoft Edge wouldn't know which extension to automatically install.</span></span><br><span data-ttu-id="38e36-146">- normal_installed：自動安裝擴充功能，而不需要使用者互動。</span><span class="sxs-lookup"><span data-stu-id="38e36-146">- normal_installed: Automatically install the extension without user interaction.</span></span> <span data-ttu-id="38e36-147">使用者可以停用此功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-147">Users can disable it.</span></span> <span data-ttu-id="38e36-148">您也需要使用 update_url 定義擴充功能下載位置。</span><span class="sxs-lookup"><span data-stu-id="38e36-148">You also need to define the extension download location using update_url.</span></span> <span data-ttu-id="38e36-149">**注意**：此設定無法使用 \*，因為Microsoft Edge 無法知道要自動安裝哪個擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-149">**Note**: You can’t use this setting with \* because Microsoft Edge wouldn't know which extension to automatically install.</span></span><br><span data-ttu-id="38e36-150">- removed：使用者無法安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-150">- removed: Users can’t install the extension.</span></span> <span data-ttu-id="38e36-151">如果使用者先前已安裝擴充功能，Microsoft Edge 會將其移除。</span><span class="sxs-lookup"><span data-stu-id="38e36-151">If users previously installed the extension, Microsoft Edge removes it.</span></span> |  |
| **<span data-ttu-id="38e36-152">install_sources</span><span class="sxs-lookup"><span data-stu-id="38e36-152">install_sources</span></span>** | <span data-ttu-id="38e36-153">只能用來設定預設設定 \*。</span><span class="sxs-lookup"><span data-stu-id="38e36-153">Can be used only to configure the default configuration, \*.</span></span> <span data-ttu-id="38e36-154">指定允許安裝擴充模組的 URL。</span><span class="sxs-lookup"><span data-stu-id="38e36-154">Specifies which URLs are allowed to install extensions.</span></span> <span data-ttu-id="38e36-155">這些模式必須同時允許 \*.crx 檔案的位置，以及開始下載網頁的位置 (查閱者)。</span><span class="sxs-lookup"><span data-stu-id="38e36-155">Both the location of the \*.crx file and the page where the download is started from (the referrer) must be allowed by these patterns.</span></span> <span data-ttu-id="38e36-156">有關 URL 模式範例，請參閱[符合模式](/microsoft-edge/extensions-chromium/enterprise/match-patterns)。</span><span class="sxs-lookup"><span data-stu-id="38e36-156">For URL pattern examples, see the [match patterns](/microsoft-edge/extensions-chromium/enterprise/match-patterns).</span></span>  |
| **<span data-ttu-id="38e36-157">minimum_version_required</span><span class="sxs-lookup"><span data-stu-id="38e36-157">minimum_version_required</span></span>** |<span data-ttu-id="38e36-158">Microsoft Edge 停用擴充功能，包括強制安裝的擴充功能，其版本比指定的最低版本還要舊。</span><span class="sxs-lookup"><span data-stu-id="38e36-158">Microsoft Edge disables extensions, including force-installed extensions, with a version older than the specified minimum version.</span></span><br><span data-ttu-id="38e36-159">版本字串的格式與擴充功能資訊清單中使用的格式相同。</span><span class="sxs-lookup"><span data-stu-id="38e36-159">The format of the version string is the same as the one used in the extension manifest.</span></span>     |
| **<span data-ttu-id="38e36-160">update_url</span><span class="sxs-lookup"><span data-stu-id="38e36-160">update_url</span></span>** | <span data-ttu-id="38e36-161">僅適用於  force_installed and normal_installed。</span><span class="sxs-lookup"><span data-stu-id="38e36-161">Only applies to force_installed and normal_installed.</span></span> <span data-ttu-id="38e36-162">指定 Microsoft Edge 擴充功能的下載位置。</span><span class="sxs-lookup"><span data-stu-id="38e36-162">Specifies where Microsoft Edge should download an extension from.</span></span> <span data-ttu-id="38e36-163">如果擴充功能是託管在 Microsoft Edge 外掛程式網站中，請使用此位置：`https://edge.microsoft.com/extensionwebstorebase/v1/crx`。</span><span class="sxs-lookup"><span data-stu-id="38e36-163">If the extension is hosted in the Microsoft Edge Add-ons website, use this location: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span><br><span data-ttu-id="38e36-164">Microsoft Edge 會使用您為初始擴充安裝指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="38e36-164">Microsoft Edge uses the URL that you specify for the initial extension installation.</span></span> <span data-ttu-id="38e36-165">對於後續的擴充功能更新，Microsoft Edge 的擴充功能資訊清單中使用該 URL。</span><span class="sxs-lookup"><span data-stu-id="38e36-165">For subsequent extension updates, Microsoft Edge uses the URL in the extension's manifest.</span></span>   |
| **<span data-ttu-id="38e36-166">runtime_allowed_hosts</span><span class="sxs-lookup"><span data-stu-id="38e36-166">runtime_allowed_hosts</span></span>**| <span data-ttu-id="38e36-167">允許擴充功能與指定的網站互動，即使它們也是在 runtime_blocked_hosts 中定義。</span><span class="sxs-lookup"><span data-stu-id="38e36-167">Allows extensions to interact with specified websites, even if they’re also defined in runtime_blocked_hosts.</span></span> <span data-ttu-id="38e36-168">您可以指定最多 100 個項目。</span><span class="sxs-lookup"><span data-stu-id="38e36-168">You can specify up to 100 entries.</span></span> <span data-ttu-id="38e36-169">系統會捨棄額外的項目。</span><span class="sxs-lookup"><span data-stu-id="38e36-169">Extra entries are discarded.</span></span><br><span data-ttu-id="38e36-170">主機模式格式與 [符合模式](/microsoft-edge/extensions-chromium/enterprise/match-patterns)類似， 但無法定義路徑。</span><span class="sxs-lookup"><span data-stu-id="38e36-170">The host pattern format is similar to [match patterns](/microsoft-edge/extensions-chromium/enterprise/match-patterns) except you can’t define the path.</span></span> <span data-ttu-id="38e36-171">例如：</span><span class="sxs-lookup"><span data-stu-id="38e36-171">For example:</span></span><br><span data-ttu-id="38e36-172">- *://*.example.com</span><span class="sxs-lookup"><span data-stu-id="38e36-172">- *://*.example.com</span></span><br><span data-ttu-id="38e36-173">- *://example。*—支援 eTLD 萬用字元</span><span class="sxs-lookup"><span data-stu-id="38e36-173">- *://example.*—eTLD wildcards are supported</span></span>     |
| **<span data-ttu-id="38e36-174">runtime_blocked_hosts</span><span class="sxs-lookup"><span data-stu-id="38e36-174">runtime_blocked_hosts</span></span>**| <span data-ttu-id="38e36-175">防止擴充功能與您指定的網站互動或修改。</span><span class="sxs-lookup"><span data-stu-id="38e36-175">Prevent extensions from interacting with or modifying websites that you specify.</span></span> <span data-ttu-id="38e36-176">修改包括封鎖 JavaScript 注入、Cookie 存取，以及 Web 要求修改。</span><span class="sxs-lookup"><span data-stu-id="38e36-176">Modifications include blocking JavaScript injection, cookie access, and web-request modifications.</span></span><br><span data-ttu-id="38e36-177">您可以指定最多 100 個項目。</span><span class="sxs-lookup"><span data-stu-id="38e36-177">You can specify up to 100 entries.</span></span> <span data-ttu-id="38e36-178">系統會捨棄額外的項目。</span><span class="sxs-lookup"><span data-stu-id="38e36-178">Extra entries are discarded.</span></span><br><span data-ttu-id="38e36-179">主機模式格式與符合模式類似，但無法定義路徑。</span><span class="sxs-lookup"><span data-stu-id="38e36-179">The host pattern format is similar to match patterns except you can’t define the path.</span></span> <span data-ttu-id="38e36-180">例如：</span><span class="sxs-lookup"><span data-stu-id="38e36-180">For example:</span></span><br><span data-ttu-id="38e36-181">- *://*.example.com</span><span class="sxs-lookup"><span data-stu-id="38e36-181">- *://*.example.com</span></span><br><span data-ttu-id="38e36-182">- *://example。*—支援 eTLD 萬用字元</span><span class="sxs-lookup"><span data-stu-id="38e36-182">- *://example.*—eTLD wildcards are supported</span></span>   |


## <a name="configure-using-a-json-string-in-windows-group-policy-editor"></a><span data-ttu-id="38e36-183">在 Windows 群組原則編輯器中使用 JSON 字串進行設定</span><span class="sxs-lookup"><span data-stu-id="38e36-183">Configure using a JSON string in Windows Group Policy Editor</span></span>

<span data-ttu-id="38e36-184">使用 GPO 使用擴充功能設定原則的步驟假設您已針對 Microsoft Edge 原則匯入 ADM/ADMX。</span><span class="sxs-lookup"><span data-stu-id="38e36-184">The steps to use the extension settings policy using GPO assume that you've already imported the ADM/ADMX for Microsoft Edge Policies.</span></span>

1. <span data-ttu-id="38e36-185">開啟群組原則編輯器，然後前往 **[Microsoft Edge] > [擴充功能] > [設定擴充功能管理設定原則]**。</span><span class="sxs-lookup"><span data-stu-id="38e36-185">Open the group policy editor and go to go to **Microsoft Edge > Extensions > Configure extension management setting policy**.</span></span>
2. <span data-ttu-id="38e36-186">啟用該原則，並在文字方塊中輸入其精簡的 JavaScript 物件標記法 (JSON) 資料做為一行，沒有分行符號。</span><span class="sxs-lookup"><span data-stu-id="38e36-186">Enable the policy and enter its compact JavaScript Object Notation (JSON) data in the text box as a single line with no line breaks.</span></span>
3. <span data-ttu-id="38e36-187">若要驗證該原則，並精簡成單行，請使用 JSON 壓縮工具。</span><span class="sxs-lookup"><span data-stu-id="38e36-187">To validate the policy and compact it into a single line, use a JSON compression tool.</span></span>

### <a name="properly-format-json-for-the-extension-settings-policy"></a><span data-ttu-id="38e36-188">正確設定 JSON 擴充功能設定原則的格式</span><span class="sxs-lookup"><span data-stu-id="38e36-188">Properly format JSON for the extension settings policy</span></span>

<span data-ttu-id="38e36-189">您必須了解此原則的兩個部分：預設範圍和個別範圍。</span><span class="sxs-lookup"><span data-stu-id="38e36-189">You need to understand the two parts to this policy — the default scope and the individual scope.</span></span> <span data-ttu-id="38e36-190">預設範圍是包含所有的擴充功能，而沒有自己的範圍。</span><span class="sxs-lookup"><span data-stu-id="38e36-190">The default scope is a catch-all for extensions without their own scope.</span></span> <span data-ttu-id="38e36-191">個別範圍只會套用該擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-191">The individual scope is applied to that extension only.</span></span>  

<span data-ttu-id="38e36-192">預設範圍是由星號 (\*) 識別。</span><span class="sxs-lookup"><span data-stu-id="38e36-192">The default scope is identified by the asterisk (\*).</span></span> <span data-ttu-id="38e36-193">下一個範例會定義預設範圍和個別擴充功能範圍。</span><span class="sxs-lookup"><span data-stu-id="38e36-193">The next example defines a default scope and an individual extension scope.</span></span>

```json
{ 
   “*”: {}, 
   “nckgahadagoaajjgafhacjanaoiihapd”: {} 
} 
```

<span data-ttu-id="38e36-194">擴充功能只會從一個範圍取得其設定。</span><span class="sxs-lookup"><span data-stu-id="38e36-194">An extension will only get its settings from one scope.</span></span> <span data-ttu-id="38e36-195">如果該擴充功能有個別的擴充功能範圍，這些會是套用到該擴充功能的設定。</span><span class="sxs-lookup"><span data-stu-id="38e36-195">If there’s an individual extension scope for that extension, those will be the settings that apply to that extension.</span></span> <span data-ttu-id="38e36-196">如果沒有個別的擴充範圍，則擴充功能會使用預設範圍。</span><span class="sxs-lookup"><span data-stu-id="38e36-196">If no individual extension scope exists, then the extension will use the default scope.</span></span>  

<span data-ttu-id="38e36-197">下一個 JSON 範例會封鎖任何擴充功能在 `.example.com` 上執行，並封鎖任何需要 「USB」權限的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-197">The next JSON example blocks any extension from running on `.example.com` and blocks any extension that requires the permission "USB".</span></span>

```json
{ 
  "*": { 
    "runtime_blocked_hosts": ["*://*.example.com"], 
    "blocked_permissions": ["usb"] 
  } 
} 
```

**<span data-ttu-id="38e36-198">精簡 JSON</span><span class="sxs-lookup"><span data-stu-id="38e36-198">Compact JSON</span></span>**

```json
{"*":{"runtime_blocked_hosts":["*://*.example.com"],"blocked_permissions":["usb"]}} 
```

### <a name="a-few-more-json-examples-for-extension-settings"></a><span data-ttu-id="38e36-199">其他一些 JSON 擴充功能設定的範例</span><span class="sxs-lookup"><span data-stu-id="38e36-199">A few more JSON examples for extension settings</span></span>

#### <a name="using-installation_mode-property-to-allow-and-block-extensions"></a><span data-ttu-id="38e36-200">使用 installation_mode 屬性來允許和封鎖擴充功能</span><span class="sxs-lookup"><span data-stu-id="38e36-200">Using installation_mode property to allow and block extensions</span></span>

- <span data-ttu-id="38e36-201">使用者可以安裝所有擴充功能 - 這是預設設定</span><span class="sxs-lookup"><span data-stu-id="38e36-201">User can install all extensions - this is the default setting</span></span> 

  `{ "*": {"installation_mode": "allowed" }}`
- <span data-ttu-id="38e36-202">使用者無法安裝任何擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-202">User can’t install any extensions.</span></span>  

  `{ "*": {"installation_mode": "blocked" }}`

- <span data-ttu-id="38e36-203">指定在安裝被封鎖時要顯示的自訂訊息。</span><span class="sxs-lookup"><span data-stu-id="38e36-203">Specify a custom message to display when installation is blocked.</span></span>

   `{"*": {"blocked_install_message": ["Call IT(408 - 555 - 1234) for an exception"]}}`

#### <a name="using-installation_mode-property-to-force-install-extensions"></a><span data-ttu-id="38e36-204">使用 installation_mode 屬性強制安裝擴充功能</span><span class="sxs-lookup"><span data-stu-id="38e36-204">Using installation_mode property to force install extensions</span></span>

<span data-ttu-id="38e36-205">當使用 installation_mode 做為「force_installed」時，系統會自動安裝擴充功能，而不需要使用者互動。</span><span class="sxs-lookup"><span data-stu-id="38e36-205">When using installation_mode as "force_installed", the extension is automatically installed without user interaction.</span></span> <span data-ttu-id="38e36-206">使用者無法停用或移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-206">A user can’t disable or remove the extension.</span></span> <span data-ttu-id="38e36-207">如果已安裝「標準」或「強制」擴充功能，**，update_url** 欄位也必須定義。</span><span class="sxs-lookup"><span data-stu-id="38e36-207">If an extension is "normal" or "force" installed, the **update_url** field must also be defined.</span></span> <span data-ttu-id="38e36-208">此欄位指向可安裝擴充功能的位置。</span><span class="sxs-lookup"><span data-stu-id="38e36-208">This field points to the location where the extension can be installed from.</span></span> <span data-ttu-id="38e36-209">針對 **update_url** 欄位，請使用下列位置：</span><span class="sxs-lookup"><span data-stu-id="38e36-209">Use the following locations for the **update_url** field:</span></span>

- <span data-ttu-id="38e36-210">如果您下載的擴充功能是託管在 Microsoft Edge 外掛程式市集，請使用 [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx)。</span><span class="sxs-lookup"><span data-stu-id="38e36-210">If the extension you’re downloading is hosted on the Microsoft Edge Add-ons store, use [https://edge.microsoft.com/extensionwebstorebase/v1/crx](https://edge.microsoft.com/extensionwebstorebase/v1/crx).</span></span>
- <span data-ttu-id="38e36-211">如果您下載的擴充功能是託管在 Chrome 線上應用程式商店，請使用 [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx)。</span><span class="sxs-lookup"><span data-stu-id="38e36-211">If the extension you’re downloading is hosted on the Chrome Web Store, use [https://clients2.google.com/service/update2/crx](https://clients2.google.com/service/update2/crx).</span></span>
- <span data-ttu-id="38e36-212">如果您是在您自己的伺服器上託管擴充功能，請使用 Microsoft Edge 可下載的已封裝擴充功能 (.crx 檔案) 之 URL。</span><span class="sxs-lookup"><span data-stu-id="38e36-212">If you’re hosting the extension on your own server, use the URL where Microsoft Edge can download the packed extension (.crx file).</span></span> <span data-ttu-id="38e36-213">JSON 範例：</span><span class="sxs-lookup"><span data-stu-id="38e36-213">JSON example:</span></span>

   `{"nckgahadagoaajjgafhacjanaoiihapd": {"installation_mode": "force_installed","update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"}}`
  
<span data-ttu-id="38e36-214">在上例中，如果您改為使用「normal_installed」而不是「force_installed」，系統會自動安裝擴充功能，而不需要使用者互動，但可以停用擴充功能。</span><span class="sxs-lookup"><span data-stu-id="38e36-214">In the above example Instead of "force_installed", if you use "normal_installed", then the extension is automatically installed without user interaction, but they can disable the extension.</span></span>  

   > [!TIP]
   > <span data-ttu-id="38e36-215">正確格式化 JSON 字串可能相當棘手。</span><span class="sxs-lookup"><span data-stu-id="38e36-215">Formatting a JSON string correctly can be tricky.</span></span> <span data-ttu-id="38e36-216">在實作原則之前，請使用 JSON 檢查程式。</span><span class="sxs-lookup"><span data-stu-id="38e36-216">Use a JSON checker before implementing the policy.</span></span> <span data-ttu-id="38e36-217">或者，試用最新版本的[擴充功能設定產生工具](https://microsoft.github.io/edge-extension-settings-generator/minimal)</span><span class="sxs-lookup"><span data-stu-id="38e36-217">Or try the early version of [Extension Settings Generator Tool](https://microsoft.github.io/edge-extension-settings-generator/minimal)</span></span>

## <a name="configure-using-the-windows-registry"></a><span data-ttu-id="38e36-218">使用 Windows 登錄進行設定</span><span class="sxs-lookup"><span data-stu-id="38e36-218">Configure using the Windows Registry</span></span>

<span data-ttu-id="38e36-219">ExtensionSettings 原則應寫入此機碼下的登錄：</span><span class="sxs-lookup"><span data-stu-id="38e36-219">The ExtensionSettings policy should be written to the registry under this key:</span></span>

`HKLM\Software\Policies\Microsoft\Edge\`

> [!NOTE]
> <span data-ttu-id="38e36-220">您可以使用 HKCU 而非 HKLM。</span><span class="sxs-lookup"><span data-stu-id="38e36-220">It’s possible to use HKCU instead of HKLM.</span></span> <span data-ttu-id="38e36-221">對等路徑可以使用群組原則物件 (GPO) 進行設定。</span><span class="sxs-lookup"><span data-stu-id="38e36-221">The equivalent path can be configured with Group Policy Object (GPO).</span></span>  

<span data-ttu-id="38e36-222">針對 Microsoft Edge，所有設定都會在此機碼下開始：</span><span class="sxs-lookup"><span data-stu-id="38e36-222">For Microsoft Edge, all settings will start under this key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\`

<span data-ttu-id="38e36-223">下一個要建立的機碼是個別範圍的擴充功能識別碼或預設範圍的星號 (\*)。</span><span class="sxs-lookup"><span data-stu-id="38e36-223">The next key that you will create is either the Extension ID for individual scope or an asterisk (\*) for the Default Scope.</span></span> <span data-ttu-id="38e36-224">例如，您可以使用下列位置套用到 Google Hangouts 的設定：</span><span class="sxs-lookup"><span data-stu-id="38e36-224">For example, you'd use the following location for settings that apply to Google Hangouts:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\nckgahadagoaajjgafhacjanaoiihapd`

<span data-ttu-id="38e36-225">針對套用到預設範圍的設定，請使用這個位置：</span><span class="sxs-lookup"><span data-stu-id="38e36-225">For settings that apply to the Default Scope, use this location:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\ExtensionSettings\*`

<span data-ttu-id="38e36-226">不同的設定會要求不同的格式，視其為字串或字串陣列而不同。</span><span class="sxs-lookup"><span data-stu-id="38e36-226">Different settings will require different formats, depending on whether they are a string or an array of strings.</span></span> <span data-ttu-id="38e36-227">陣列值需要 [＂value＂]。</span><span class="sxs-lookup"><span data-stu-id="38e36-227">Array values require [＂value＂].</span></span> <span data-ttu-id="38e36-228">字串值可以以目前格式輸入。</span><span class="sxs-lookup"><span data-stu-id="38e36-228">String values can be entered as is.</span></span> <span data-ttu-id="38e36-229">下列清單顯示哪些設定是陣列或字串：</span><span class="sxs-lookup"><span data-stu-id="38e36-229">The following list shows which settings are arrays or strings:</span></span>

- <span data-ttu-id="38e36-230">Installation_mode = 字串</span><span class="sxs-lookup"><span data-stu-id="38e36-230">Installation_mode = String</span></span>
- <span data-ttu-id="38e36-231">update_url = 字串</span><span class="sxs-lookup"><span data-stu-id="38e36-231">update_url = String</span></span>
- <span data-ttu-id="38e36-232">blocked_permissions = 字串陣列</span><span class="sxs-lookup"><span data-stu-id="38e36-232">blocked_permissions = Array of strings</span></span>
- <span data-ttu-id="38e36-233">allowed_permissions = 字串陣列</span><span class="sxs-lookup"><span data-stu-id="38e36-233">allowed_permissions = Array of Strings</span></span>
- <span data-ttu-id="38e36-234">minimum_version_required = 字串</span><span class="sxs-lookup"><span data-stu-id="38e36-234">minimum_version_required = String</span></span>
- <span data-ttu-id="38e36-235">runtime_blocked_hosts = 字串陣列</span><span class="sxs-lookup"><span data-stu-id="38e36-235">runtime_blocked_hosts = Array of strings</span></span>
- <span data-ttu-id="38e36-236">runtime_allowed_hosts = 字串陣列</span><span class="sxs-lookup"><span data-stu-id="38e36-236">runtime_allowed_hosts = Array of Strings</span></span>
- <span data-ttu-id="38e36-237">blocked_install_message = 字串</span><span class="sxs-lookup"><span data-stu-id="38e36-237">blocked_install_message = String</span></span>


## <a name="see-also"></a><span data-ttu-id="38e36-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38e36-238">See also</span></span>

- [<span data-ttu-id="38e36-239">管理企業中的 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="38e36-239">Manage Microsoft Edge extensions in the enterprise</span></span>](microsoft-edge-manage-extensions.md)
- [<span data-ttu-id="38e36-240">使用群組原則管理 Microsoft Edge 擴充功能</span><span class="sxs-lookup"><span data-stu-id="38e36-240">Use group policies to manage Microsoft Edge extensions</span></span>](microsoft-edge-manage-extensions-policies.md)
- [<span data-ttu-id="38e36-241">Microsoft Edge 擴充功能常見問題集</span><span class="sxs-lookup"><span data-stu-id="38e36-241">FAQ for Microsoft Edge Extensions</span></span>](microsoft-edge-manage-extensions-faq.md)
- [<span data-ttu-id="38e36-242">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="38e36-242">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
