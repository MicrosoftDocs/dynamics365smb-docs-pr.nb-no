---
title: Administrere samhandlinger med kontaktene dine | Microsoft-dokumentasjon
description: "Du kan administrere alle typer kommunikasjon eller samhandlinger mellom selskapet og kontaktene dine, for eksempel brev, telefonsamtaler, møter og så videre."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6fa95883e30b7912ed2b6b22f40cbcd5af339f31
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="managing-interactions-with-contacts"></a><span data-ttu-id="c16a2-103">Håndtere samhandlinger med kontakter</span><span class="sxs-lookup"><span data-stu-id="c16a2-103">Managing Interactions With Contacts</span></span>
<span data-ttu-id="c16a2-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] betraktes all slags kommunikasjon mellom selskapet og kontaktene som samhandlinger.</span><span class="sxs-lookup"><span data-stu-id="c16a2-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], interactions are all types of communications between your company and your contacts.</span></span> <span data-ttu-id="c16a2-105">Kommunikasjon kan for eksempel være per brev, telefaks, e-post, telefonsamtaler, møter og så videre.</span><span class="sxs-lookup"><span data-stu-id="c16a2-105">For example, communications can be by letter, fax, email, telephone, meetings, and so on.</span></span>

<span data-ttu-id="c16a2-106">Området for relasjonshåndtering lar deg registrere alle samhandlingene med kontaktene, slik at du kan følge opp salgs- og markedsføringskampanjene som er rettet mot kontaktene, og forbedre fremtidige forretningssamhandlinger med dem.</span><span class="sxs-lookup"><span data-stu-id="c16a2-106">The relationship management area enables you to record all the interactions you have with your contacts in order to keep track of the sales and marketing efforts you have directed at your contacts and to improve your future business interactions with them.</span></span> <span data-ttu-id="c16a2-107">Konfigurasjon av programmet til å registrere samhandlinger består av disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="c16a2-107">Setting up your application to record interactions consists of these tasks:</span></span>

* <span data-ttu-id="c16a2-108">Definere samhandlingsmaler</span><span class="sxs-lookup"><span data-stu-id="c16a2-108">Setting up interaction templates</span></span>  
* <span data-ttu-id="c16a2-109">Opprette samhandlinger på kontakter eller segmenter</span><span class="sxs-lookup"><span data-stu-id="c16a2-109">Creating interactions on contacts or segments</span></span>  
* <span data-ttu-id="c16a2-110">Vise og administrere registrerte samhandlinger</span><span class="sxs-lookup"><span data-stu-id="c16a2-110">View and manage recorded interactions</span></span>  

##  <a name="setting-up-interaction-templates"></a><span data-ttu-id="c16a2-111">Definere samhandlingsmaler</span><span class="sxs-lookup"><span data-stu-id="c16a2-111">Setting up Interaction Templates</span></span>
<span data-ttu-id="c16a2-112">Før du kan opprette og registrere samhandlinger, må du definere samhandlingsmaler.</span><span class="sxs-lookup"><span data-stu-id="c16a2-112">Before you can create and record interactions, you must set up interaction templates.</span></span> <span data-ttu-id="c16a2-113">Når du oppretter samhandlinger, må du angi hvilke samhandlingsmaler de baserer seg på.</span><span class="sxs-lookup"><span data-stu-id="c16a2-113">When creating interactions, you must specify the interaction templates they are based on.</span></span> <span data-ttu-id="c16a2-114">En samhandlingsmal en modell som definerer de grunnleggende egenskapene for en samhandling.</span><span class="sxs-lookup"><span data-stu-id="c16a2-114">An interaction template is a model that defines the basic characteristics of an interaction.</span></span>
<span data-ttu-id="c16a2-115">Du kan definere en samhandlingsmal på siden **Samhandlingsmaler**.</span><span class="sxs-lookup"><span data-stu-id="c16a2-115">You set up an interaction template on the **Interaction Templates** page.</span></span>

<span data-ttu-id="c16a2-116">Etter at du har oppgitt opplysninger om samhandlingsmalen, kan du opprette et vedlegg, for eksempel et Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="c16a2-116">After you have entered information about the interaction template, you can create an attachment, for example, a Microsoft Word document.</span></span> <span data-ttu-id="c16a2-117">Gjenta trinnene hvis du vil definere flere samhandlingsmaler.</span><span class="sxs-lookup"><span data-stu-id="c16a2-117">Repeat the steps to set up as many interaction templates as you want.</span></span>  

## <a name="creating-interactions"></a><span data-ttu-id="c16a2-118">Opprette samhandlinger</span><span class="sxs-lookup"><span data-stu-id="c16a2-118">Creating Interactions</span></span>
<span data-ttu-id="c16a2-119">Du kan registrere samhandlinger på to ulike måter:</span><span class="sxs-lookup"><span data-stu-id="c16a2-119">There are two ways of recording interactions:</span></span>

* <span data-ttu-id="c16a2-120">Du kan manuelt opprette samhandlinger som er knyttet til en enkelt kontakt eller til et segment.</span><span class="sxs-lookup"><span data-stu-id="c16a2-120">You can manually create interactions that are linked to a single contact or to a segment.</span></span> <span data-ttu-id="c16a2-121">Hvis du vil ha mer informasjon, kan du se [Opprette samhandlinger på kontakter og segmenter](marketing-how-create-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="c16a2-121">For more information, see [Create Interactions on Contacts and Segments](marketing-how-create-interactions.md).</span></span>  
* <span data-ttu-id="c16a2-122">Du kan angi at samhandlinger skal registreres automatisk når du utfører handlinger i programmet, for eksempel når du skriver ut en faktura eller et tilbud.</span><span class="sxs-lookup"><span data-stu-id="c16a2-122">You can automatically record interactions when you perform actions in the application, for example, when you print an invoice, or quote.</span></span> <span data-ttu-id="c16a2-123">Hvis du vil ha mer informasjon, kan du se [Automatisk registrere samhandlinger med kontakter](marketing-auto-record-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="c16a2-123">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="viewing-and-managing-recorded-interactions"></a><span data-ttu-id="c16a2-124">Vise og administrere registrerte samhandlinger</span><span class="sxs-lookup"><span data-stu-id="c16a2-124">Viewing and Managing Recorded Interactions</span></span>
<span data-ttu-id="c16a2-125">Du kan vise alle registrerte samhandlinger som ikke er slettet, på siden **Samhandlingsposter**.</span><span class="sxs-lookup"><span data-stu-id="c16a2-125">You can view all the recorded interactions that have not been deleted on the **Interaction Log Entries** page.</span></span> <span data-ttu-id="c16a2-126">Du kan åpne denne siden ved å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="c16a2-126">You can open this page by:</span></span>

* <span data-ttu-id="c16a2-127">Bruke **Søk etter side eller rapport**-ikonet for å søke etter **Samhandlingsposter**.</span><span class="sxs-lookup"><span data-stu-id="c16a2-127">Using the **Search for Page or Report** icon to search on **Interaction Log Entries**.</span></span>
* <span data-ttu-id="c16a2-128">Velge handlingen **Samhandlingsposter** på en kontakt eller et segment.</span><span class="sxs-lookup"><span data-stu-id="c16a2-128">Choosing the **Interaction Log Entries** action on a contact or segment.</span></span>
  <span data-ttu-id="c16a2-129">Siden **Samhandlingspost** viser hvilke samhandlinger du oppretter manuelt og hvilke samhandlinger som programmet registrerer automatisk.</span><span class="sxs-lookup"><span data-stu-id="c16a2-129">The **Interaction Log Entry** page contains the interactions you create manually and the interactions that the application records automatically.</span></span>

<span data-ttu-id="c16a2-130">På denne siden kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="c16a2-130">In this page, you can:</span></span>

* <span data-ttu-id="c16a2-131">Vise statusen til samhandlinger.</span><span class="sxs-lookup"><span data-stu-id="c16a2-131">View the status of interactions.</span></span>
* <span data-ttu-id="c16a2-132">Merke samhandlinger som annullert.</span><span class="sxs-lookup"><span data-stu-id="c16a2-132">Mark interactions as canceled.</span></span>

<span data-ttu-id="c16a2-133">Du kan slette samhandlingsposter som er annullert.</span><span class="sxs-lookup"><span data-stu-id="c16a2-133">You can delete interaction log entries that have been canceled.</span></span> <span data-ttu-id="c16a2-134">Hvis du vil slette samhandlingsposter, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Slett annullerte samhandlingsposter**, velger den relaterte koblingen og fyller ut informasjonen.</span><span class="sxs-lookup"><span data-stu-id="c16a2-134">To delete interaction log entries, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Canceled Interaction Log Entries**, and then choose the related link, and then fill in the information.</span></span>

## <a name="see-also"></a><span data-ttu-id="c16a2-135">Se også</span><span class="sxs-lookup"><span data-stu-id="c16a2-135">See Also</span></span>
[<span data-ttu-id="c16a2-136">Administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="c16a2-136">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="c16a2-137">Håndtere salgsmuligheter</span><span class="sxs-lookup"><span data-stu-id="c16a2-137">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="c16a2-138">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="c16a2-138">Working with Business Central</span></span>](ui-work-product.md)  

