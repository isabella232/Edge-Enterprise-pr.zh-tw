---
title: 將 Microsoft Edge 設定為 Windows 和 macOS 中的預設瀏覽器
ms.author: brianalt
author: dan-wesley
manager: srugh
ms.date: 1/15/2020
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: 了解如何將 Microsoft Edge 設定為預設瀏覽器
ms.openlocfilehash: 9151294c34cb2252a7fb32e660c1e3d9e64b5f76
ms.sourcegitcommit: f363ceb6c42054fabc95ce8d7bca3c52d80e6a9f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2021
ms.locfileid: "11447757"
---
# <a name="set-microsoft-edge-as-the-default-browser"></a><span data-ttu-id="7bc73-103">將 Microsoft Edge 設定為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7bc73-103">Set Microsoft Edge as the default browser</span></span>

<span data-ttu-id="7bc73-104">本文說明如何將 Microsoft Edge 設定為 Windows 和 macOS 中的預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7bc73-104">This article explains how you can set Microsoft Edge as the default browser on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="7bc73-105">本文適用於 Windows 8 和 Windows 10 上的 Microsoft Edge 版本 77 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7bc73-105">This article applies to Microsoft Edge version 77 or later on Windows 8 and Windows 10.</span></span> <span data-ttu-id="7bc73-106">有關 Windows 7 和 macOS，請參閱[將 Microsoft Edge設定為預設瀏覽器](./microsoft-edge-policies.md#defaultbrowsersettingenabled)原則。</span><span class="sxs-lookup"><span data-stu-id="7bc73-106">For Windows 7 and macOS, see the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy.</span></span>

## <a name="introduction"></a><span data-ttu-id="7bc73-107">簡介</span><span class="sxs-lookup"><span data-stu-id="7bc73-107">Introduction</span></span>

<span data-ttu-id="7bc73-108">您可以使用**設定預設關聯設定檔案**群組原則或 [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 行動裝置管理設定，來將 Microsoft Edge 設定為您組織的預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7bc73-108">You can use the **Set a default associations configuration file** Group Policy or the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting to set Microsoft Edge as the default browser for your organization.</span></span>

<span data-ttu-id="7bc73-109">若要將 Microsoft Edge Stable 設定為 html 檔案、http/https 連結和 PDF 檔案的預設瀏覽器，請使用以下應用程式關聯檔案範例：</span><span class="sxs-lookup"><span data-stu-id="7bc73-109">To set Microsoft Edge Stable as the default browser for html files, http/https links, and PDF files use the following application association file example:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations> 
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="7bc73-110">若要將 Microsoft Edge Beta 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Beta"，並將 **ProgId** 設定為 "MSEdgeBHTML"。</span><span class="sxs-lookup"><span data-stu-id="7bc73-110">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="7bc73-111">若要將 Microsoft Edge Dev 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Dev"，並將 **ProgId** 設定為 "MSEdgeDHTML"。</span><span class="sxs-lookup"><span data-stu-id="7bc73-111">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>


> [!NOTE]
> <span data-ttu-id="7bc73-112">如果未在目標裝置上安裝 Microsoft Edge，則不會套用預設檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="7bc73-112">The default file associations aren't applied if Microsoft Edge isn't installed on the target device.</span></span> <span data-ttu-id="7bc73-113">在這種情況下，系統會在使用者開啟連結或 htm/html 檔案時，提示他們選取預設應用程式。</span><span class="sxs-lookup"><span data-stu-id="7bc73-113">In this scenario, users are prompted to select their default application when they open a link or a htm/html file.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-domain-joined-devices"></a><span data-ttu-id="7bc73-114">在加入網域的裝置上將 Microsoft Edge 設定為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7bc73-114">Set Microsoft Edge as the default browser on domain-joined devices</span></span>

<span data-ttu-id="7bc73-115">您可以透過設定**設定預設關聯設定檔案**群組原則，在加入網域的裝置上將 Microsoft Edge 設定為預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7bc73-115">You can set Microsoft Edge as the default browser on domain-joined devices by configuring the **Set a default associations configuration file** group policy.</span></span> <span data-ttu-id="7bc73-116">開啟這個群組原則，會要求您建立並儲存預設關聯設定檔案。</span><span class="sxs-lookup"><span data-stu-id="7bc73-116">Turning this group policy on requires you to create and store a default associations configuration file.</span></span> <span data-ttu-id="7bc73-117">此檔案儲存在本機或網路共用上。</span><span class="sxs-lookup"><span data-stu-id="7bc73-117">This file is stored locally or on a network share.</span></span> <span data-ttu-id="7bc73-118">如需有關建立這個檔案的詳細資訊，請參閱[匯出或匯入預設應用程式關聯](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)。</span><span class="sxs-lookup"><span data-stu-id="7bc73-118">For more information about creating this file, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span></span>

### <a name="to-configure-the-group-policy-for-a-default-file-type-and-protocol-associations-configuration-file"></a><span data-ttu-id="7bc73-119">若要為預設檔案類型和通訊協定關聯設定檔案設定群組原則：</span><span class="sxs-lookup"><span data-stu-id="7bc73-119">To configure the group policy for a default file type and protocol associations configuration file:</span></span>

1. <span data-ttu-id="7bc73-120">開啟群組原則編輯器，然後移至**電腦設定\系統管理範本\Windows 元件\檔案總管**。</span><span class="sxs-lookup"><span data-stu-id="7bc73-120">Open the Group Policy editor and go to the **Computer Configuration\Administrative Templates\Windows Components\File Explorer**.</span></span>
2. <span data-ttu-id="7bc73-121">選取**設定預設關聯設定檔案**。</span><span class="sxs-lookup"><span data-stu-id="7bc73-121">Select **Set a default associations configuration file**.</span></span>
3. <span data-ttu-id="7bc73-122">按一下**原則設定**，然後按一下**啟用**。</span><span class="sxs-lookup"><span data-stu-id="7bc73-122">Click **policy setting**, and then click **Enabled**.</span></span>
4. <span data-ttu-id="7bc73-123">在**選項**下輸入您預設關聯設定檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="7bc73-123">Under **Options:**, type the location to your default associations configuration file.</span></span>
5. <span data-ttu-id="7bc73-124">按一下**確定**以儲存原則設定。</span><span class="sxs-lookup"><span data-stu-id="7bc73-124">Click **OK** to save the policy settings.</span></span>

<span data-ttu-id="7bc73-125">下一個螢幕擷取畫面中的範例顯示了網路共用上名為 *appassoc.xml* 的關聯檔案，該檔案可從目標裝置存取。</span><span class="sxs-lookup"><span data-stu-id="7bc73-125">The example in the next screenshot shows an associations file named *appassoc.xml* on a network share that is accessible from the target device.</span></span>

   ![在群組原則中啟用檔案關聯](./media/edge-learnmore-make-edge-default-browser/edge-learnmore-app-associations.png)

   > [!NOTE]
   > <span data-ttu-id="7bc73-127">如果啟用了此設定，並且使用者的裝置已加入網域，則在使用者下次登入時將會處理關聯設定檔案。</span><span class="sxs-lookup"><span data-stu-id="7bc73-127">If this setting is enabled and the user's device is domain-joined, the associations configuration file is processed the next time the user signs on.</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-azure-active-directory-joined-devices"></a><span data-ttu-id="7bc73-128">在加入 Azure Active Directory 的裝置上將 Microsoft Edge 設定為預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7bc73-128">Set Microsoft Edge as the default browser on Azure Active Directory joined devices</span></span>

<span data-ttu-id="7bc73-129">若要在加入 Azure Active Directory 的裝置上將 Microsoft Edge 設定為預設瀏覽器，請使用以下應用程式關聯檔案範例並依照 [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) 行動裝置管理設定中的步驟進行。</span><span class="sxs-lookup"><span data-stu-id="7bc73-129">To set Microsoft Edge as the default browser on Azure Active Directory joined devices follow the steps in the [DefaultAssociationsConfiguration](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration) Mobile Device Management setting using the following application association file as an example.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<DefaultAssociations>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".html"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier=".htm"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="http"/>
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgeHTM" Identifier="https"/>  
  <Association ApplicationName="Microsoft Edge" ProgId="MSEdgePDF" Identifier=".pdf"/>
</DefaultAssociations>
```

> [!NOTE]
> <span data-ttu-id="7bc73-130">若要將 Microsoft Edge Beta 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Beta"，並將 **ProgId** 設定為 "MSEdgeBHTML"。</span><span class="sxs-lookup"><span data-stu-id="7bc73-130">To set Microsoft Edge Beta as the default browser, set **ApplicationName** to "Microsoft Edge Beta" and **ProgId** to "MSEdgeBHTML".</span></span> <span data-ttu-id="7bc73-131">若要將 Microsoft Edge Dev 設定為預設瀏覽器，請將 **ApplicationName** 設定為 "Microsoft Edge Dev"，並將 **ProgId** 設定為 "MSEdgeDHTML"。</span><span class="sxs-lookup"><span data-stu-id="7bc73-131">To set Microsoft Edge Dev as the default browser, set **ApplicationName** to "Microsoft Edge Dev" and **ProgId** to "MSEdgeDHTML".</span></span>

## <a name="set-microsoft-edge-as-the-default-browser-on-macos"></a><span data-ttu-id="7bc73-132">將 Microsoft Edge 設定為 macOS 中的預設瀏覽器</span><span class="sxs-lookup"><span data-stu-id="7bc73-132">Set Microsoft Edge as the default browser on macOS</span></span>

<span data-ttu-id="7bc73-133">嘗試以程式設計方式設定 macOS 的預設瀏覽器會導致向終端使用者顯示提示。</span><span class="sxs-lookup"><span data-stu-id="7bc73-133">Attempting to programmatically set the default browser on macOS causes a prompt to appear for the end user.</span></span> <span data-ttu-id="7bc73-134">此提示是 macOS 安全性功能，只有使用 AppleScript，才能使離開提示的動作自動化。</span><span class="sxs-lookup"><span data-stu-id="7bc73-134">This prompt is a macOS security feature that can only be automated away by using an AppleScript.</span></span>

<span data-ttu-id="7bc73-135">由於此限制，將 Microsoft Edge 設定為 macOS 的預設瀏覽器，有兩個主要方法可供選用。</span><span class="sxs-lookup"><span data-stu-id="7bc73-135">Because of this limitation, there are two main methods for setting Microsoft Edge as the default browser on a macOS.</span></span> <span data-ttu-id="7bc73-136">第一個選項是使用已將 Microsoft Edge 設定為預設瀏覽器的 macOS 映像來刷新裝置。</span><span class="sxs-lookup"><span data-stu-id="7bc73-136">The first option is to flash the device with an image of macOS where Microsoft Edge has already been set as the default browser.</span></span> <span data-ttu-id="7bc73-137">另一個選項是使用 [將 Microsoft Edge 設定為預設瀏覽器](./microsoft-edge-policies.md#defaultbrowsersettingenabled) 原則，此原則會提示使用者將 Microsoft Edge 設定為預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7bc73-137">The other option is to use the [Set Microsoft Edge as default browser](./microsoft-edge-policies.md#defaultbrowsersettingenabled) policy, which prompts the user to set Microsoft Edge as the default browser.</span></span>

<span data-ttu-id="7bc73-138">使用上述任一方法時，使用者仍然可以變更預設瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="7bc73-138">When using either of these methods, it is still possible for a user to change the default browser.</span></span> <span data-ttu-id="7bc73-139">這是因為基於安全理由，不可透過程式設計方式封鎖預設瀏覽器喜好設定。</span><span class="sxs-lookup"><span data-stu-id="7bc73-139">This is because for security reasons, the default browser preference can’t be blocked programmatically.</span></span> <span data-ttu-id="7bc73-140">因此，建議您部署**將 Microsoft Edge 設定為預設瀏覽器** 原則，即使您建立有 Microsoft Edge 做為預設瀏覽器的映像，也應如此。</span><span class="sxs-lookup"><span data-stu-id="7bc73-140">For this reason, we recommend that you deploy the **Set Microsoft Edge as default browser** policy even if you create an image with Microsoft Edge as the default browser.</span></span> <span data-ttu-id="7bc73-141">如果設定了此原則，而使用者下次開啟 Microsoft Edge 時，將預設瀏覽器變更為其他瀏覽器，則系統會提示他們將 Microsoft Edge 設為預設。</span><span class="sxs-lookup"><span data-stu-id="7bc73-141">If the policy is set and a user changes the default browser from Microsoft Edge the next time they open Microsoft Edge, they will be prompted to set it as the default.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bc73-142">也請參閱</span><span class="sxs-lookup"><span data-stu-id="7bc73-142">See also</span></span>

- [<span data-ttu-id="7bc73-143">規劃 Microsoft Edge 部署</span><span class="sxs-lookup"><span data-stu-id="7bc73-143">Plan your deployment of Microsoft Edge</span></span>](./deploy-edge-plan-deployment.md)
- [<span data-ttu-id="7bc73-144">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="7bc73-144">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="7bc73-145">將 Microsoft Edge 設定為預設瀏覽器 (Windows 7 和 macOS)</span><span class="sxs-lookup"><span data-stu-id="7bc73-145">Set Microsoft Edge as default browser (Windows 7 and macOS)</span></span>](./microsoft-edge-policies.md#defaultbrowsersettingenabled)
- [<span data-ttu-id="7bc73-146">Windows 10 – 如何為 IT 專業人員設定檔案關聯？</span><span class="sxs-lookup"><span data-stu-id="7bc73-146">Windows 10 – How to configure file associations for IT Pros?</span></span>](/archive/blogs/windowsinternals/windows-10-how-to-configure-file-associations-for-it-pros)
- [<span data-ttu-id="7bc73-147">匯出或匯入預設應用程式關聯</span><span class="sxs-lookup"><span data-stu-id="7bc73-147">Export or Import Default Application Associations</span></span>](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)
  - [<span data-ttu-id="7bc73-148">DISM 概觀</span><span class="sxs-lookup"><span data-stu-id="7bc73-148">DISM Overview</span></span>](/windows-hardware/manufacture/desktop/what-is-dism)
  - [<span data-ttu-id="7bc73-149">DISM - 部署映像服務與管理</span><span class="sxs-lookup"><span data-stu-id="7bc73-149">DISM - Deployment Image Servicing and Management</span></span>](/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows)