---
title: Konfigurere nettleseren
description: Beskriver hvordan du konfigurerer nettlesere for å arbeide med Business Central og produkter som integreres med det.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: 17b41653b1b5934e98c82ce8a35430e7b6a5c0d0
ms.sourcegitcommit: 1aac2c5f6773151c011dc1e4069c84d79fe5bda8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839958"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="719e2-103">Konfigurere og feilsøke nettleseren for å arbeide med Business Central-nettklienten</span><span class="sxs-lookup"><span data-stu-id="719e2-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="719e2-104">Denne artikkelen forklarer hvordan du konfigurerer nettleseren slik at [!INCLUDE[web_client](includes/web_client.md)] og alle funksjonene fungerer som de skal.</span><span class="sxs-lookup"><span data-stu-id="719e2-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="719e2-105">Les denne artikkelen hvis du har problemer med å åpne [!INCLUDE[web_client](includes/web_client.md)], fordi noen problemer kan være forårsaket av innstillingene i nettleseren.</span><span class="sxs-lookup"><span data-stu-id="719e2-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="719e2-106">Artikkelen inneholder detaljer om hvordan du konfigurerer Microsoft Edge, men kravene til JavaScript, informasjonskapsler og popup-vinduer er de samme for alle nettlesere som støttes.</span><span class="sxs-lookup"><span data-stu-id="719e2-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="719e2-107">Se instruksjonene fra produsenten for andre nettlesere.</span><span class="sxs-lookup"><span data-stu-id="719e2-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="719e2-108">Bruk en nettleser som støttes</span><span class="sxs-lookup"><span data-stu-id="719e2-108">Use a supported browser</span></span>

<span data-ttu-id="719e2-109">Pass på at du bruker en av de støttede nettleserne.</span><span class="sxs-lookup"><span data-stu-id="719e2-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="719e2-110">Se [Minimumskrav for å bruke Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="719e2-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="719e2-111">Tillat JavaScript fra Business Central</span><span class="sxs-lookup"><span data-stu-id="719e2-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="719e2-112">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="719e2-112">*Problem:*</span></span>

<span data-ttu-id="719e2-113">Hvis nettleseren ikke tillater JavaScript, ser du **NotSupported/DisabledJavaScript** på adresselinjen og meldingen **HTTP-feil 404.0 – ikke funnet** når du prøver å åpne [!INCLUDE[prod_short](includes/prod_short.md)] og</span><span class="sxs-lookup"><span data-stu-id="719e2-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="719e2-114">*Løsning:*</span><span class="sxs-lookup"><span data-stu-id="719e2-114">*Fix:*</span></span>

1. <span data-ttu-id="719e2-115">I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="719e2-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="719e2-116">Gjør ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="719e2-116">Do one of the following steps.</span></span> <span data-ttu-id="719e2-117">Velg det trinnet som organisasjonen anbefaler:</span><span class="sxs-lookup"><span data-stu-id="719e2-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="719e2-118">Flytt **Tillatte**-vekslebryteren mot venstre (Av).</span><span class="sxs-lookup"><span data-stu-id="719e2-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="719e2-119">Deretter velger du **Legg til** og skriver inn adressen (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] i **Område**-boksen.</span><span class="sxs-lookup"><span data-stu-id="719e2-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="719e2-120">Velg **Legg til** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="719e2-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="719e2-121">Flytt **Tillatte**-vekslebryteren mot høyre (På).</span><span class="sxs-lookup"><span data-stu-id="719e2-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="719e2-122">Tillat informasjonskapsler fra Business Central</span><span class="sxs-lookup"><span data-stu-id="719e2-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="719e2-123">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="719e2-123">*Problem:*</span></span>

<span data-ttu-id="719e2-124">Hvis nettleseren ikke tillater informasjonskapsler, får du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="719e2-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="719e2-125">**Beklager, siden ble ikke funnet. Kontroller adressen og prøv på nytt.**</span><span class="sxs-lookup"><span data-stu-id="719e2-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="719e2-126">*Løsning:*</span><span class="sxs-lookup"><span data-stu-id="719e2-126">*Fix:*</span></span>

1. <span data-ttu-id="719e2-127">I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **Informasjonskapsler og områdedata**.</span><span class="sxs-lookup"><span data-stu-id="719e2-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="719e2-128">Flytt **Tillat områder å lagre og lese informasjonskapseldata**-vekslebryteren mot høyre (På).</span><span class="sxs-lookup"><span data-stu-id="719e2-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="719e2-129">Tillat popup-vinduer fra Business Central</span><span class="sxs-lookup"><span data-stu-id="719e2-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="719e2-130">integreres med flere produkter.</span><span class="sxs-lookup"><span data-stu-id="719e2-130">integrates with several products.</span></span> <span data-ttu-id="719e2-131">I noen tilfeller, for eksempel med Microsoft Teams, åpnes [!INCLUDE[prod_short](includes/prod_short.md)] eller popup-vinduer i produktet.</span><span class="sxs-lookup"><span data-stu-id="719e2-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="719e2-132">Denne funksjonen krever at nettleseren tillater popup-vinduer fra [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="719e2-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="719e2-133">*Problem:*</span><span class="sxs-lookup"><span data-stu-id="719e2-133">*Problem:*</span></span>

<span data-ttu-id="719e2-134">Hvis popup-vinduer for [!INCLUDE[prod_short](includes/prod_short.md)] blokkeres, får du en melding som ligner på følgende melding:</span><span class="sxs-lookup"><span data-stu-id="719e2-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="719e2-135">**Noe gikk galt. Det kan hende nettleseren blokkerer popup-vinduer som er nødvendig for Business Central.**</span><span class="sxs-lookup"><span data-stu-id="719e2-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="719e2-136">*Løsning:*</span><span class="sxs-lookup"><span data-stu-id="719e2-136">*Fix:*</span></span>

1. <span data-ttu-id="719e2-137">I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **Popup-vinduer og omdirigeringer**.</span><span class="sxs-lookup"><span data-stu-id="719e2-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="719e2-138">Flytt **Blokkert**-vekslebryteren mot høyre (På).</span><span class="sxs-lookup"><span data-stu-id="719e2-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="719e2-139">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="719e2-139">Select **Add**.</span></span> <span data-ttu-id="719e2-140">I **Område**-boksen skriver du inn `https://businesscentral.dynamics.com` og velger **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="719e2-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="719e2-141">Se også</span><span class="sxs-lookup"><span data-stu-id="719e2-141">See Also</span></span>

[<span data-ttu-id="719e2-142">Feilsøke Teams</span><span class="sxs-lookup"><span data-stu-id="719e2-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  