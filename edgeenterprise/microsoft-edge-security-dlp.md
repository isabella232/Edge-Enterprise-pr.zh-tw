---
title: Microsoft Edge 中的資料外洩防護
ms.author: archandr
author: dan-wesley
manager: seanlynd
ms.date: 03/01/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: Microsoft Edge 中的資料外洩防護 (DLP)
ms.openlocfilehash: f25e1fa7a610645f6ca0ca10cbcfc69ae8689b7a
ms.sourcegitcommit: f14286edec59ee9183bdf38c15fc890881efd64f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "11384981"
---
# <a name="data-loss-prevention-dlp-in-microsoft-edge"></a><span data-ttu-id="39b2c-103">Microsoft Edge 中的資料外洩防護 (DLP)</span><span class="sxs-lookup"><span data-stu-id="39b2c-103">Data Loss Prevention (DLP) in Microsoft Edge</span></span>

<span data-ttu-id="39b2c-104">資料外洩防護 (DLP) 是一種技術系統，可識別並保護敏感性企業資料不遭到未經授權的披露。</span><span class="sxs-lookup"><span data-stu-id="39b2c-104">Data loss prevention (DLP) is a system of technologies that identify and safeguard sensitive enterprise data from unauthorized disclosure.</span></span> <span data-ttu-id="39b2c-105">若要遵守商務標準和行業法規，組織必須保護敏感性資訊，並防止未經授權的披露。</span><span class="sxs-lookup"><span data-stu-id="39b2c-105">To comply with business standards and industry regulations, organizations must protect sensitive information and prevent its unauthorized disclosure.</span></span> <span data-ttu-id="39b2c-106">敏感性資訊包括財務資料或個人身分識別資訊 (PII)，例如信用卡號碼、社會安全號碼或健康記錄等諸多其他項目。</span><span class="sxs-lookup"><span data-stu-id="39b2c-106">Sensitive information includes financial data or personally identifiable information (PII) such as credit card numbers, social security numbers, or health records, among many other things.</span></span>

<span data-ttu-id="39b2c-107">遠端工作已提升對 DLP 使用的著重度。</span><span class="sxs-lookup"><span data-stu-id="39b2c-107">Remote work has increased the emphasis on using DLP.</span></span> <span data-ttu-id="39b2c-108">隨著在裝置上逐漸增多的個人及工作活動之使用，企業可能面臨在工作場所以外未經授權共用公司資料的風險。</span><span class="sxs-lookup"><span data-stu-id="39b2c-108">With the growing use of personal and work activities on devices, enterprises are seeing an increased risk of unauthorized sharing of corporate data outside the workplace.</span></span>

<span data-ttu-id="39b2c-109">這種使用者活動混合也已分散到多個裝置，在這種情況下，資料會隨著各種公用網路和私人網路之使用，在個人和公司裝置間移動。</span><span class="sxs-lookup"><span data-stu-id="39b2c-109">This blending of user activities has spread to devices as well, where data is moved between personal and corporate devices over a variety of public and private networks.</span></span> <span data-ttu-id="39b2c-110">最終結果會增加披露敏感性資料的風險。</span><span class="sxs-lookup"><span data-stu-id="39b2c-110">The net result is a dramatically increased risk of exposing sensitive data.</span></span>

<span data-ttu-id="39b2c-111">Microsoft Edge 本身支援兩種不同的 DLP 解決方案： Microsoft 端點 DLP 和 Windows 資訊保護 (WIP)。</span><span class="sxs-lookup"><span data-stu-id="39b2c-111">Microsoft Edge natively supports two different DLP solutions, Microsoft Endpoint DLP and Windows Information Protection (WIP).</span></span>

## <a name="microsoft-endpoint-data-loss-prevention-endpoint-dlp"></a><span data-ttu-id="39b2c-112">Microsoft 端點資料遺失防護 (端點 DLP)</span><span class="sxs-lookup"><span data-stu-id="39b2c-112">Microsoft Endpoint data loss prevention (Endpoint DLP)</span></span>

<span data-ttu-id="39b2c-113">Microsoft 端點 DLP 使用先進概念 (例如以資料為中心的保護) 的新一代資料外洩防護。</span><span class="sxs-lookup"><span data-stu-id="39b2c-113">Microsoft Endpoint DLP is the next generation of data loss prevention using modern concepts such as data-centric protection.</span></span> <span data-ttu-id="39b2c-114">它內建於 Windows 10 和 Microsoft Edge，因此裝置上不需要其他的代理程式或外掛程式。</span><span class="sxs-lookup"><span data-stu-id="39b2c-114">It's built-in to Windows 10 and Microsoft Edge so it doesn't need additional agents or plugins on the device.</span></span>

> [!NOTE]
> <span data-ttu-id="39b2c-115">這適用於 Microsoft Edge 版本 85 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="39b2c-115">This applies to Microsoft Edge version 85 or later.</span></span>

<span data-ttu-id="39b2c-116">若要深入了解端點 DLP，請使用下列資源：</span><span class="sxs-lookup"><span data-stu-id="39b2c-116">To learn more about Endpoint DLP, use the following resources:</span></span>

- [<span data-ttu-id="39b2c-117">影片：Microsoft Edge 和資料外洩防護 (DLP)</span><span class="sxs-lookup"><span data-stu-id="39b2c-117">Video: Microsoft Edge and Data loss prevention (DLP)</span></span>](microsoft-edge-video-security-dlp.md)
- [<span data-ttu-id="39b2c-118">了解 Microsoft 365 端點資料外洩防護</span><span class="sxs-lookup"><span data-stu-id="39b2c-118">Learn about Microsoft 365 Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="39b2c-119">開始使用端點資料外洩防護</span><span class="sxs-lookup"><span data-stu-id="39b2c-119">Get started with Endpoint data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-getting-started?view=o365-worldwide&preserve-view=true)

<span data-ttu-id="39b2c-120">Microsoft Edge 強制執行系統管理員設定的敏感性檔案和記錄非合規活動的稽核事件之原則。</span><span class="sxs-lookup"><span data-stu-id="39b2c-120">Microsoft Edge enforces admin configured policies for sensitive files and records audit events for non-compliant activities.</span></span>

<span data-ttu-id="39b2c-121">在執行 Windows 10 的裝置上，您可以在執行稽核和管理的使用者活動包括下列活動：</span><span class="sxs-lookup"><span data-stu-id="39b2c-121">Some of the user activities that you can audit and manage on devices running Windows 10 include the following activities:</span></span>

- <span data-ttu-id="39b2c-122">檔案上傳：防止將敏感性檔案上傳到未經授權的雲端位置。</span><span class="sxs-lookup"><span data-stu-id="39b2c-122">File Upload: Protect sensitive file upload to unauthorized cloud locations.</span></span> <!-- The next 3 screenshots show a sequence where a user tries to drop a sensitive data file on to their local storage.-->
- <span data-ttu-id="39b2c-123">剪貼簿保護：防止從檔案複製敏感性資料。</span><span class="sxs-lookup"><span data-stu-id="39b2c-123">Clipboard Protection: Protect sensitive data from being copied out of the file.</span></span>
- <span data-ttu-id="39b2c-124">列印保護：防止敏感性檔案被列印。</span><span class="sxs-lookup"><span data-stu-id="39b2c-124">Print Protection: Protect sensitive file from being printed.</span></span>
- <span data-ttu-id="39b2c-125">儲存至 USB/網路：防止將敏感性檔案儲存至可移動 USB 儲存區或未經授權的網路位置。</span><span class="sxs-lookup"><span data-stu-id="39b2c-125">Save to USB/Network: Protect sensitive file from being saved to removable USB storage or unauthorized network locations.</span></span>

<span data-ttu-id="39b2c-126">如需有關您可以稽核和管理之使用者活動的詳細資訊，請參閱 [您可以監視並採取行動的 Endpoint 活動](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="39b2c-126">For more detailed information about user activities you can audit and manage, see [Endpoint activities you can monitor and take action on](https://docs.microsoft.com/microsoft-365/compliance/endpoint-dlp-learn-about?view=o365-worldwide#endpoint-activities-you-can-monitor-and-take-action-on&preserve-view=true).</span></span>

## <a name="windows-information-protection"></a><span data-ttu-id="39b2c-127">Windows 資訊保護</span><span class="sxs-lookup"><span data-stu-id="39b2c-127">Windows Information Protection</span></span>

<span data-ttu-id="39b2c-128">請參閱 [Windows 資訊保護的 支援](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection)，其中描述 Microsoft Edge 如何支援 Windows 資訊保護 (WIP)。</span><span class="sxs-lookup"><span data-stu-id="39b2c-128">Check out [Support for Windows Information Protection](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection), which describes how Microsoft Edge supports Windows Information Protection (WIP).</span></span> <span data-ttu-id="39b2c-129">您可以在下列各節中深入了解系統需求、優點和支援功能：</span><span class="sxs-lookup"><span data-stu-id="39b2c-129">You can learn moe about system requirements, benefits, and supported features in the following sections:</span></span>

- [<span data-ttu-id="39b2c-130">系統需求</span><span class="sxs-lookup"><span data-stu-id="39b2c-130">System Requirements</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#system-requirements)
- [<span data-ttu-id="39b2c-131">Windows 資訊保護的優點</span><span class="sxs-lookup"><span data-stu-id="39b2c-131">Windows Information Protection Benefits</span></span>](https://docs.microsoft.com/deployedge/microsoft-edge-security-windows-information-protection#windows-information-protection-benefits)
- [<span data-ttu-id="39b2c-132">Microsoft Edge 支援的 WIP 功能</span><span class="sxs-lookup"><span data-stu-id="39b2c-132">WIP features supported in Microsoft Edge</span></span>](https://docs.microsoft.com/DeployEdge/microsoft-edge-security-windows-information-protection#wip-features-supported-in-microsoft-edge)

## <a name="see-also"></a><span data-ttu-id="39b2c-133">請參閱</span><span class="sxs-lookup"><span data-stu-id="39b2c-133">See also</span></span>

- [<span data-ttu-id="39b2c-134">Microsoft Edge 企業登陸頁面</span><span class="sxs-lookup"><span data-stu-id="39b2c-134">Microsoft Edge Enterprise landing page</span></span>](https://aka.ms/EdgeEnterprise)
- [<span data-ttu-id="39b2c-135">影片：資料外洩防護 - Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="39b2c-135">Video: Data loss prevention - Microsoft Edge</span></span>](https://www.youtube.com/watch?v=dLD04U9eTqg)
- [<span data-ttu-id="39b2c-136">資料外洩防護概觀</span><span class="sxs-lookup"><span data-stu-id="39b2c-136">Overview of data loss prevention</span></span>](https://docs.microsoft.com/microsoft-365/compliance/data-loss-prevention-policies?view=o365-worldwide&preserve-view=true)
- [<span data-ttu-id="39b2c-137">使用 Windows 資訊保護來保護您的企業資料</span><span class="sxs-lookup"><span data-stu-id="39b2c-137">Protect your enterprise data using Windows Information Protection</span></span>](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip)
