---
title: Optimalisering av Outlook for innboks for virksomheten
description: Lær om ting du kan gjøre for å forbedre opplevelsen med innboksen for virksomhet i Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064859"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="9f30c-103">Optimalisering av Outlook for innboks for virksomheten</span><span class="sxs-lookup"><span data-stu-id="9f30c-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="9f30c-104">Denne artikkelen beskriver ting du kan gjøre for å få den best mulige opplevelsen med innboksen for virksomhet i Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="9f30c-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="9f30c-105">Oppdater Outlook</span><span class="sxs-lookup"><span data-stu-id="9f30c-105">Update Outlook</span></span>

<span data-ttu-id="9f30c-106">Oppdat til Outlook, versjon 2012 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="9f30c-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="9f30c-107">Hvis du ikke kan oppdatere Outlook til versjon 2012 eller nyere, må du kontrollere at du minst oppdaterer til versjon 1905.</span><span class="sxs-lookup"><span data-stu-id="9f30c-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="9f30c-108">Dette forhindrer at Outlook-tillegget kan kjøre ved å bruke eldre Internet Explorer-komponenter</span><span class="sxs-lookup"><span data-stu-id="9f30c-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="9f30c-109">Slik kontrollerer du versjonen til Outlook</span><span class="sxs-lookup"><span data-stu-id="9f30c-109">How to check your version of Outlook</span></span>

<span data-ttu-id="9f30c-110">Hvis du bruker Office 2019 eller Microsoft 365, følger du denne veiledningen fra Microsofts kundestøtte for å kontrollere hvilken Outlook-versjon du har:</span><span class="sxs-lookup"><span data-stu-id="9f30c-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="9f30c-111">Om Office: Hvilken versjon av Office bruker jeg?</span><span class="sxs-lookup"><span data-stu-id="9f30c-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="9f30c-112">Slik oppdaterer du Outlook</span><span class="sxs-lookup"><span data-stu-id="9f30c-112">How to update Outlook</span></span>

<span data-ttu-id="9f30c-113">Hvis du vil oppdatere Outlook til den nyeste versjonen, følger du veiledningen fra Microsofts kundestøtte eller kontakter administratoren:</span><span class="sxs-lookup"><span data-stu-id="9f30c-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="9f30c-114">Installer Office-oppdateringer</span><span class="sxs-lookup"><span data-stu-id="9f30c-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="9f30c-115">Installer Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="9f30c-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="9f30c-116">Kontroller at Microsoft Edge WebView2 er installert på enheten.</span><span class="sxs-lookup"><span data-stu-id="9f30c-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="9f30c-117">Slik kontrollerer du om Microsoft Edge WebView2 er installert</span><span class="sxs-lookup"><span data-stu-id="9f30c-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="9f30c-118">Hvis du vil kontrollere om du har Microsoft Edge WebView2 installert på en datamaskin, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="9f30c-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="9f30c-119">Fra Start-menyen:</span><span class="sxs-lookup"><span data-stu-id="9f30c-119">From Start menu:</span></span>

1. <span data-ttu-id="9f30c-120">Velg **Start** ![Windows Start](media/windows-start-icon.png "Windows Start-ikon") > **Innstillinger** ![Windows-innstillinger](media/windows-settings-icon.png "Ikon for Windows-innstillinger") > **Apper og funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="9f30c-121">Skriv inn **WebView2** i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="9f30c-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="9f30c-122">Hvis Microsoft Edge WebView2 er installert, vises en oppføring kalt **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="9f30c-123">Fra kontrollpanel:</span><span class="sxs-lookup"><span data-stu-id="9f30c-123">From Control Panel:</span></span>

1. <span data-ttu-id="9f30c-124">Skriv inn **Kontrollpanel** i søkefeltet ved siden av **Start** ![Windows Start](media/windows-start-icon.png "Windows Start-ikon"), og velg deretter resultatet.</span><span class="sxs-lookup"><span data-stu-id="9f30c-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="9f30c-125">Velg **Programmer** > **Programmer og funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="9f30c-126">Skriv inn **WebView2** i søkefeltet.</span><span class="sxs-lookup"><span data-stu-id="9f30c-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="9f30c-127">Hvis Microsoft Edge WebView2 er installert, vises en oppføring kalt **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="9f30c-128">Slik installerer du Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="9f30c-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="9f30c-129">Gå til [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/) i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="9f30c-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="9f30c-130">Velg **Last ned**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-130">Choose **Download**.</span></span>
3. <span data-ttu-id="9f30c-131">Angi **Velg arkitektur** for å samsvare med systemet ditt.</span><span class="sxs-lookup"><span data-stu-id="9f30c-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="9f30c-132">Velg **Last ned**.</span><span class="sxs-lookup"><span data-stu-id="9f30c-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="9f30c-133">Det kan hende at organisasjonen har begrensninger for hvilke komponenter som kan installeres på enheten.</span><span class="sxs-lookup"><span data-stu-id="9f30c-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="9f30c-134">Kontakt systemansvarlig for å få hjelp.</span><span class="sxs-lookup"><span data-stu-id="9f30c-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="9f30c-135">Bruk en nettleser som støttes</span><span class="sxs-lookup"><span data-stu-id="9f30c-135">Use a supported browser</span></span>

<span data-ttu-id="9f30c-136">Du bør vurdere å bruke Outlook for nettet i en av nettleserne som støttes av Business Central.</span><span class="sxs-lookup"><span data-stu-id="9f30c-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="9f30c-137">Hvis du vil se en liste over nettlesere som støttes, kan du se [Minimumskrav for bruk av Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="9f30c-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="9f30c-138">Se også</span><span class="sxs-lookup"><span data-stu-id="9f30c-138">See Also</span></span>

[<span data-ttu-id="9f30c-139">Bli klar til å gjøre forretninger</span><span class="sxs-lookup"><span data-stu-id="9f30c-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="9f30c-140">Få Business Central på mobilenheten</span><span class="sxs-lookup"><span data-stu-id="9f30c-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="9f30c-141">Send dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="9f30c-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="9f30c-142">Finans</span><span class="sxs-lookup"><span data-stu-id="9f30c-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="9f30c-143">Salg</span><span class="sxs-lookup"><span data-stu-id="9f30c-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="9f30c-144">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="9f30c-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="9f30c-145">Minimumskrav for Outlook</span><span class="sxs-lookup"><span data-stu-id="9f30c-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="9f30c-146">Bruke tillegg i Outlook på Internett</span><span class="sxs-lookup"><span data-stu-id="9f30c-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]