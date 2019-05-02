---
title: Designdetaljer – Tabell for planleggingstilordning | Microsoft-dokumentasjon
description: Dette emnet gir innsikt i hva som skjer når du endrer hvordan du planlegger for en vare.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 9a1661d71bd28009a0c0b83a50e27cae3c833ea7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803628"
---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="de5aa-103">Designdetaljer: Tabell for planleggingstilordning</span><span class="sxs-lookup"><span data-stu-id="de5aa-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="de5aa-104">Det må planlegges for alle varer, men det er ingen grunn til å beregne en plan for en vare med mindre det er en endring i mønsteret for behov eller forsyning siden planen sist ble beregnet.</span><span class="sxs-lookup"><span data-stu-id="de5aa-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  

<span data-ttu-id="de5aa-105">Hvis brukeren har angitt en ny ordre eller endret en eksisterende, er det grunn til å beregne planen på nytt.</span><span class="sxs-lookup"><span data-stu-id="de5aa-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="de5aa-106">Andre årsaker inkluderer en endring i prognosen eller ønsket sikkerhetslagerantall.</span><span class="sxs-lookup"><span data-stu-id="de5aa-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="de5aa-107">Endring av en stykkliste ved å legge til eller fjerne en komponent, vil mest sannsynlig indikerer en endring, men bare for komponentvaren.</span><span class="sxs-lookup"><span data-stu-id="de5aa-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  

<span data-ttu-id="de5aa-108">For flere lokasjoner foregår tildelingen på nivået for en vare per lokasjonskombinasjon.</span><span class="sxs-lookup"><span data-stu-id="de5aa-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="de5aa-109">Hvis det for eksempel er opprettet en ordre på bare én lokasjon, vil programmet tilordne varen på denne spesifikke lokasjonen for planlegging.</span><span class="sxs-lookup"><span data-stu-id="de5aa-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  

<span data-ttu-id="de5aa-110">Grunnen til å velge varer for planlegging har å gjøre med systemytelsen.</span><span class="sxs-lookup"><span data-stu-id="de5aa-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="de5aa-111">Hvis det ikke har oppstått endringer i en vares behov-/ forsyningsmønster, foreslår vil ikke planleggingssystemet foreslå handlinger som skal utføres.</span><span class="sxs-lookup"><span data-stu-id="de5aa-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="de5aa-112">Uten planleggingstilordningen måtte systemet ha utført beregningene for alle varer for å finne ut hva det skal planlegge for, og dette hadde tappet systemressursene.</span><span class="sxs-lookup"><span data-stu-id="de5aa-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  

<span data-ttu-id="de5aa-113">Tabellen **Planleggingstilordning** overvåker behovs- og forsyningshendelser og tilordner de riktige varene for planlegging.</span><span class="sxs-lookup"><span data-stu-id="de5aa-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="de5aa-114">Følgende hendelser overvåkes:</span><span class="sxs-lookup"><span data-stu-id="de5aa-114">The following events are monitored:</span></span>  

* <span data-ttu-id="de5aa-115">En ny ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="de5aa-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="de5aa-116">Endring av vare, antall, lokasjon, variant eller dato på en ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="de5aa-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="de5aa-117">Annullering av en ordre, prognose, komponent, bestilling, produksjonsordre, monteringsordre eller overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="de5aa-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="de5aa-118">Forbruk av varer som ikke er planlagt.</span><span class="sxs-lookup"><span data-stu-id="de5aa-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="de5aa-119">Avgang av varer som ikke er planlagt.</span><span class="sxs-lookup"><span data-stu-id="de5aa-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="de5aa-120">Ikke planlagte endringer på lageret.</span><span class="sxs-lookup"><span data-stu-id="de5aa-120">Unplanned changes in inventory.</span></span>  

<span data-ttu-id="de5aa-121">For disse direkteforskyvningene for forsyning/behov vedlikeholder ordresporings- og handlingsmeldingssystemet tabellen Planleggingstilordning, og angir en planleggingsårsak som en handlingsmelding.</span><span class="sxs-lookup"><span data-stu-id="de5aa-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  

<span data-ttu-id="de5aa-122">Følgende endringer i hoveddata kan også føre til en ubalanse i planleggingen:</span><span class="sxs-lookup"><span data-stu-id="de5aa-122">The following changes in master data can also cause a planning imbalance:</span></span>  

* <span data-ttu-id="de5aa-123">Endring av status til Sertifisert i produksjonsstykklistehodet (for alle varer som bruker hodet).</span><span class="sxs-lookup"><span data-stu-id="de5aa-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="de5aa-124">Slettet linje (underordnet vare).</span><span class="sxs-lookup"><span data-stu-id="de5aa-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="de5aa-125">Endring av status til Sertifisert i rutehodet (for alle varer som bruker rutingen).</span><span class="sxs-lookup"><span data-stu-id="de5aa-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="de5aa-126">Endringer i følgende varekortfelt.</span><span class="sxs-lookup"><span data-stu-id="de5aa-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="de5aa-127">Sikkerhetslagerantall eller Sikkerhetsleveringstid.</span><span class="sxs-lookup"><span data-stu-id="de5aa-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="de5aa-128">Beregning av leveringstid.</span><span class="sxs-lookup"><span data-stu-id="de5aa-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="de5aa-129">Gjenbestillingspunkt.</span><span class="sxs-lookup"><span data-stu-id="de5aa-129">Reorder Point.</span></span>  
* <span data-ttu-id="de5aa-130">Produksjonsstykklistenummer (og alle underordnede for gammel stykklistereferanse).</span><span class="sxs-lookup"><span data-stu-id="de5aa-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="de5aa-131">Rutenr.</span><span class="sxs-lookup"><span data-stu-id="de5aa-131">Routing No.</span></span>  
* <span data-ttu-id="de5aa-132">Gjenbestillingsprinsipp.</span><span class="sxs-lookup"><span data-stu-id="de5aa-132">Reordering Policy.</span></span>  

<span data-ttu-id="de5aa-133">I slike tilfeller vil en ny funksjon, Behandle planleggingstilordning, opprettholde tabellen og angir planleggingsårsaken som Bevegelse.</span><span class="sxs-lookup"><span data-stu-id="de5aa-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  

<span data-ttu-id="de5aa-134">Følgende endringer fører ikke til en planleggingstilordning:</span><span class="sxs-lookup"><span data-stu-id="de5aa-134">The following changes do not cause a planning assignment:</span></span>  

* <span data-ttu-id="de5aa-135">Kalendere</span><span class="sxs-lookup"><span data-stu-id="de5aa-135">Calendars</span></span>  
* <span data-ttu-id="de5aa-136">Andre planleggingsparametre på varekortet:</span><span class="sxs-lookup"><span data-stu-id="de5aa-136">Other planning parameters on the item card</span></span>  

<span data-ttu-id="de5aa-137">Følgende begrensninger gjelder ved beregning av MPS eller MRP:</span><span class="sxs-lookup"><span data-stu-id="de5aa-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  

* <span data-ttu-id="de5aa-138">MPS: Planleggingssystemet kontrollerer at varen har en behovsprognose eller en ordre.</span><span class="sxs-lookup"><span data-stu-id="de5aa-138">MPS: The planning system checks that the item carries a demand forecast or a sales order.</span></span> <span data-ttu-id="de5aa-139">Hvis ikke, inkluderes ikke varen i planen.</span><span class="sxs-lookup"><span data-stu-id="de5aa-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="de5aa-140">MRP: Hvis planleggingssystemet oppdager at varen etterfylles av en MPS-planleggingslinje eller MPS-forsyningsordre, blir varen utelatt fra planleggingen.</span><span class="sxs-lookup"><span data-stu-id="de5aa-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="de5aa-141">Eventuelle behov fra aktuelle komponenter er imidlertid inkludert .</span><span class="sxs-lookup"><span data-stu-id="de5aa-141">However, any demand from relevant components is included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="de5aa-142">Se også</span><span class="sxs-lookup"><span data-stu-id="de5aa-142">See Also</span></span>  
<span data-ttu-id="de5aa-143">[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="de5aa-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="de5aa-144">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="de5aa-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="de5aa-145">[Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="de5aa-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="de5aa-146">Designdetaljer: Planleggingsparametere</span><span class="sxs-lookup"><span data-stu-id="de5aa-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  