---
title: "Metoder for å feilsøke eller omgå problemer | Microsoft-dokumentasjon"
description: "Lær å omgå problemer i Accountant Hub for Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: e4f739e13123054527bf3116aec2c8c4133537e6
ms.contentlocale: nb-no
ms.lasthandoff: 04/16/2018

---
# <a name="troubleshooting-include-d365acclongincludesd365acclongmdmd"></a><span data-ttu-id="7c82d-103">Feilsøke [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c82d-103">Troubleshooting [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="7c82d-104">Registrering for [!INCLUDE [d365acc](includes/d365acc_md.md)] er enkelt og kan gjøres svært raskt.</span><span class="sxs-lookup"><span data-stu-id="7c82d-104">Signing up for [!INCLUDE [d365acc](includes/d365acc_md.md)] is easy and can be done very quickly.</span></span> <span data-ttu-id="7c82d-105">Det er også lett å legge til klienter på instrumentbordet, men denne artikkelen tar opp problemer du kan møte underveis.</span><span class="sxs-lookup"><span data-stu-id="7c82d-105">Adding clients to the dashboard is also easy, but this article addresses issues that you may have on the way.</span></span>

## <a name="what-email-address-can-i-use-with-include-d365accincludesd365accmdmd"></a><span data-ttu-id="7c82d-106">Hvilken e-postadresse kan jeg bruke med [!INCLUDE [d365acc](includes/d365acc_md.md)]?</span><span class="sxs-lookup"><span data-stu-id="7c82d-106">What email address can I use with [!INCLUDE [d365acc](includes/d365acc_md.md)]?</span></span>
<span data-ttu-id="7c82d-107">[!INCLUDE [d365acc](includes/d365acc_md.md)] krever at du bruker en e-postadresse for arbeid eller skole for å registrere deg.</span><span class="sxs-lookup"><span data-stu-id="7c82d-107">[!INCLUDE [d365acc](includes/d365acc_md.md)] requires that you use a work or school email address to sign up.</span></span> <span data-ttu-id="7c82d-108">[!INCLUDE [d365acc](includes/d365acc_md.md)] støtter ikke e-postadressene levert av e-posttjenester for forbrukere eller telekommunikasjonsleverandører.</span><span class="sxs-lookup"><span data-stu-id="7c82d-108">[!INCLUDE [d365acc](includes/d365acc_md.md)] does not support email addresses provided by consumer email services or telecommunication providers.</span></span> <span data-ttu-id="7c82d-109">Dette inkluderer outlook.com, hotmail.com, gmail.com og andre.</span><span class="sxs-lookup"><span data-stu-id="7c82d-109">This includes outlook.com, hotmail.com, gmail.com, and others.</span></span>  

<span data-ttu-id="7c82d-110">Hvis du prøver å registrere deg med en personlig e-postadresse, får du en melding om å bruke en e-postadresse for arbeid eller skole.</span><span class="sxs-lookup"><span data-stu-id="7c82d-110">If you try to sign up with a personal email address, you will get a message indicating to use a work or school email address.</span></span>  

## <a name="why-cant-i-connect-to-my-clients-data"></a><span data-ttu-id="7c82d-111">Hvorfor kan jeg ikke koble til klientens data?</span><span class="sxs-lookup"><span data-stu-id="7c82d-111">Why can't I connect to my client's data?</span></span>
<span data-ttu-id="7c82d-112">Det kan være et par årsaker, blant annet følgende:</span><span class="sxs-lookup"><span data-stu-id="7c82d-112">There can be a couple of reasons, including the following:</span></span>

- <span data-ttu-id="7c82d-113">URL-adressen i feltet **URL-adresse for klient** er ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="7c82d-113">The URL in the **Client URL** field is not valid</span></span>  

  <span data-ttu-id="7c82d-114">Gå til **Administrer klienter**, åpne klienten du ikke kan koble til, og velg deretter **Test URL-adresse for klient**.</span><span class="sxs-lookup"><span data-stu-id="7c82d-114">Go to **Manage Clients**, open the client that you cannot connect to, and then choose **Test Client URL**.</span></span>  
- <span data-ttu-id="7c82d-115">Klientens selskapet er frakoblet for øyeblikket, for eksempel hvis det blir oppgradert</span><span class="sxs-lookup"><span data-stu-id="7c82d-115">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="7c82d-116">På instrumentpanelet velger du **Verktøy**-menyelementet, og deretter **Sjekk feil**.</span><span class="sxs-lookup"><span data-stu-id="7c82d-116">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="7c82d-117">Dermed åpnes en liste med tekniske opplysninger, så du vil kanskje kontakte systemansvarlig hvis du ser feil.</span><span class="sxs-lookup"><span data-stu-id="7c82d-117">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="7c82d-118">Feilmeldingen «Serveren har avvist klientlegitimasjonen» antyder at du ikke har tilgang.</span><span class="sxs-lookup"><span data-stu-id="7c82d-118">For example, the error message "The server has rejected the client credentials" suggests that you do not have access.</span></span>  
- <span data-ttu-id="7c82d-119">Du ikke har mottatt en e-post fra klienten som inviterer dem til [!INCLUDE [d365fin](includes/d365fin_md.md)], eller du åpnet ikke koblingen i e-posten, eller du godtok ikke invitasjonen.</span><span class="sxs-lookup"><span data-stu-id="7c82d-119">You have not received an email from your client that invites them to their [!INCLUDE [d365fin](includes/d365fin_md.md)], or you did not open the link in the email, or you did not accept the invitation</span></span>

  <span data-ttu-id="7c82d-120">Du må åpne koblingen i invitasjonen og godta trinnene som legger deg til i klientens [!INCLUDE [d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7c82d-120">You must open the link in the invitation and accept the steps that adds you to your client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7c82d-121">Før det har du ikke tilgang til dataene.</span><span class="sxs-lookup"><span data-stu-id="7c82d-121">Until then, you do not have access to their data.</span></span>  
- <span data-ttu-id="7c82d-122">Du har ikke tilgang til alle selskapene i klientens [!INCLUDE [d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="7c82d-122">You do not have access to all companies in your client's [!INCLUDE [d365fin](includes/d365fin_md.md)]</span></span>

  <span data-ttu-id="7c82d-123">Klienten kan ha flere selskaper eller konsern i [!INCLUDE [d365fin](includes/d365fin_md.md)], og invitasjonen omfatter ikke alltid alle selskapene.</span><span class="sxs-lookup"><span data-stu-id="7c82d-123">Your client can have multiple business units or companies in [!INCLUDE [d365fin](includes/d365fin_md.md)], and your invitation does not always include all companies.</span></span> <span data-ttu-id="7c82d-124">Kontakt klienten for å sikre at du har tilgang til selskapene som klienten vil du skal arbeide i.</span><span class="sxs-lookup"><span data-stu-id="7c82d-124">Work with your client to make sure that you have access to the companies that the client wants you to work in.</span></span>  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a><span data-ttu-id="7c82d-125">Hvorfor oppdateres ikke dataene på instrumentbordet mitt?</span><span class="sxs-lookup"><span data-stu-id="7c82d-125">Why doesn't the data refresh in my dashboard?</span></span>
<span data-ttu-id="7c82d-126">Når du legger til en klient eller ber om en oppdatering av dataene, henter [!INCLUDE [d365acc](includes/d365acc_md.md)] dataene.</span><span class="sxs-lookup"><span data-stu-id="7c82d-126">When you add a client or request a refresh of the data, [!INCLUDE [d365acc](includes/d365acc_md.md)] fetches the data.</span></span> <span data-ttu-id="7c82d-127">Men du må oppdatere vinduet selv, for eksempel velge handlingen Vis alle selskap på nytt, oppdatere leservinduet, navigere fra instrumentbordet og deretter tilbake igjen, eller lignende.</span><span class="sxs-lookup"><span data-stu-id="7c82d-127">But you must refresh the window yourself, such as choosing the "Redisplay all companies" action, refresh the browser window, navigate away from the dashboard and then back again, or similar.</span></span> <span data-ttu-id="7c82d-128">Dette er et kjent problem som vi arbeider med å forbedre i en senere oppdatering.</span><span class="sxs-lookup"><span data-stu-id="7c82d-128">This is a known issue that we are working on improving in a later update.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c82d-129">Se også</span><span class="sxs-lookup"><span data-stu-id="7c82d-129">See Also</span></span>
<span data-ttu-id="7c82d-130">[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="7c82d-130">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="7c82d-131">[Legge til klienter på skrivebordet i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span><span class="sxs-lookup"><span data-stu-id="7c82d-131">[Add Clients to Your Dashboard in [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)</span></span>  

