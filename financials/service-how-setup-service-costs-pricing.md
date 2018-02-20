---
title: Definere priser og kostnader for servicer | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer priser og ekstra kostnader for servicer.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 151b63b0f68a6605ae5c935f2331803277766452
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-pricing-and-additional-costs-for-services"></a><span data-ttu-id="0ec8c-103">Definere priser og ekstra kostnader for servicer</span><span class="sxs-lookup"><span data-stu-id="0ec8c-103">Set Up Pricing and Additional Costs for Services</span></span>
<span data-ttu-id="0ec8c-104">Du kan bruke prissettingsfunksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å definere og tilpasse programmet slik at du bruker og justerer prissetting for servicevarer, -reparasjoner og -ordrer.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-104">You can use the [!INCLUDE[d365fin](includes/d365fin_md.md)] pricing features to set up and customize your application so that you apply and adjust pricing on service items, repairs, and orders.</span></span> <span data-ttu-id="0ec8c-105">Disse prissettingsavgjørelsene kan deretter enkelt overføres til faktureringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-105">These pricing decisions are then easily transmitted to the invoicing process.</span></span>  
  
<span data-ttu-id="0ec8c-106">Alt etter implementering kan du definere prissettingsgrupper og knytte dem til bestemte tidsperioder, kunder eller valutaer.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-106">As your implementation requires, you can set up pricing groups and map them to specific time periods, customers, or currency.</span></span> <span data-ttu-id="0ec8c-107">Du kan definere fast, minimum eller maksimum prissetting, avhengig av servicekontraktene du har med kundene.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-107">You can set up fixed, minimum, or maximum pricing, depending on the service contracts that you have with customers.</span></span> <span data-ttu-id="0ec8c-108">Når du justerer prisene, kan du vise og godkjenne endringene før de bokføres.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-108">Finally, as you adjust your prices, you can view and approve the changes before committing them to the ledger.</span></span>  

## <a name="to-set-up-a-service-price-group"></a><span data-ttu-id="0ec8c-109">Slik definerer du serviceprisgrupper</span><span class="sxs-lookup"><span data-stu-id="0ec8c-109">To set up a service price group</span></span>
<span data-ttu-id="0ec8c-110">Du kan definere grupper som inneholder servicevarer som du vil skal ha samme spesielle serviceprissetting.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-110">You can set up groups containing service items that you want to receive the same special service pricing.</span></span> <span data-ttu-id="0ec8c-111">Du tilordner serviceprisgrupper til servicevarer på servicevarelinjer.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-111">You assign service price groups to service items on service item lines.</span></span> <span data-ttu-id="0ec8c-112">Du kan dessuten tilordne serviceprisgrupper til servicevaregrupper.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-112">You can also assign service price groups to service item groups.</span></span>  

1. <span data-ttu-id="0ec8c-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceprisgrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Price Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ec8c-114">Opprett en ny serviceprisgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-114">Create a new service price group.</span></span>  
3. <span data-ttu-id="0ec8c-115">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="0ec8c-116">Velg handlingen **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-116">Choose the **Setup** action.</span></span>  
2. <span data-ttu-id="0ec8c-117">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > <span data-ttu-id="0ec8c-118">Feltene **Justeringstype** og **Beløp** fungerer sammen for å angi om justeringen gjelder et fast beløp, eller bare gjelder når den samlede serviceprisen er høyere eller lavere enn beløpet i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-118">The **Adjustment Type** and **Amount** fields work together to specify whether an adjustment concerns a fixed amount, or applies only when the total service price exceeds or is lower than the amount in the **Amount** field.</span></span>  

## <a name="to-set-up-a-service-price-adjustment-group"></a><span data-ttu-id="0ec8c-119">Slik definerer du serviceprisjusteringsgrupper</span><span class="sxs-lookup"><span data-stu-id="0ec8c-119">To set up a service price adjustment group</span></span>  
<span data-ttu-id="0ec8c-120">Du kan definere prisjusteringsgrupper for å justere serviceprissetting av servicevarer.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-120">You can set up price adjustment groups to adjust service pricing of service items.</span></span> <span data-ttu-id="0ec8c-121">Du kan for eksempel definere prisjusteringsgrupper som justerer prisen på frakt eller reservedeler.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-121">For example, you can set up price adjustment groups that adjust price of freight or spare parts.</span></span>  
  
1. <span data-ttu-id="0ec8c-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceprisgrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Price Adjustment Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ec8c-123">Opprett en ny serviceprisjusteringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-123">Create a new service price adjustment group.</span></span>  
3. <span data-ttu-id="0ec8c-124">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-124">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="0ec8c-125">Angi hvilken posttype du vil justere, i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-125">In the **Type** field, enter the type of the entry that you want to adjust.</span></span>  
  
    * <span data-ttu-id="0ec8c-126">Hvis du vil justere bare én bestemt post, kan du angi nummeret for posten i feltet **Nr.**</span><span class="sxs-lookup"><span data-stu-id="0ec8c-126">To adjust only one specific entry, enter the number of this entry in the **No.**</span></span> <span data-ttu-id="0ec8c-127">.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-127">field.</span></span> <span data-ttu-id="0ec8c-128">Hvis du lar dette feltet være tomt, vil justeringsgruppen justere alle poster av den definerte typen i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-128">When you leave this field blank, your adjustment group will adjust all entries of the type defined in the **Type** field.</span></span>  
    * <span data-ttu-id="0ec8c-129">Hvis du vil justere servicepriser relatert til bare én bestemt service, kan du fylle ut feltet **Arbeidstype**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-129">To adjust service prices related to only one specific service, fill in the **Work Type** field.</span></span> <span data-ttu-id="0ec8c-130">Hvis du lar dette feltet være tomt, blir det oversett.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-130">When you leave this field blank, it will just be ignored.</span></span>  
  
5. <span data-ttu-id="0ec8c-131">I feltet **Beskrivelse** kan du angi en kort beskrivelse av serviceprisjusteringen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-131">In the **Description** field, enter a short description of the service price adjustment.</span></span>  
6. <span data-ttu-id="0ec8c-132">Hvis du vil justere servicepriser relatert til bare én bestemt varebokføringsgruppe, fyller du ut feltet **Bokføringsgruppe - vare**.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-132">To adjust service prices related to only one specific general product posting group, fill in the **Gen. Prod. Posting Group** field.</span></span>

> [!Tip]
> <span data-ttu-id="0ec8c-133">Du kan velge **Detaljer** for å legge til tilleggsinformasjon om justeringsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-133">You can choose **Details** to add additional information about the adjustment group.</span></span> <span data-ttu-id="0ec8c-134">Du kan for eksempel definere hvilke varer som hører til en serviceprisjusteringsgruppe, og om dette er en vare, ressurs, ressursgruppe eller servicekostnad.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-134">For example, you can specify which item belongs to the service price adjustment group, and whether this is an item, a resource, a resource group, or a service charge.</span></span>  

## <a name="to-set-up-additional-costs-for-services"></a><span data-ttu-id="0ec8c-135">Definere ekstra kostnader for servicer</span><span class="sxs-lookup"><span data-stu-id="0ec8c-135">To set up additional costs for services</span></span>
<span data-ttu-id="0ec8c-136">Når du arbeider med servicevarer og serviceordrer, kan det hende du må registrere tilleggskostnader, for eksempel reiseutgifter til bestemte servicesoner eller startgebyrer.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-136">When you work with service items and service orders, you may need to register additional costs, such as travel costs to particular service zones or starting fees.</span></span> <span data-ttu-id="0ec8c-137">Når du oppretter en serviceordre, kan du sette inn disse kostnadene, og en linje av typen **Kost** legges til i ordren.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-137">When you create a service order, you can insert these costs and a line with the type **Cost** will be added to the order.</span></span> <span data-ttu-id="0ec8c-138">Hvis du vil bruke kostnaden for alle serviceordrer, kan du definere en standardkost.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-138">Alternatively, if you want to apply the cost to all service orders, you can set up a default cost.</span></span> <span data-ttu-id="0ec8c-139">For eksempel hvis du vil bruke et startgebyr.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-139">For example, if you always want to apply a starting fee.</span></span>
  
### <a name="to-set-up-service-costs"></a><span data-ttu-id="0ec8c-140">Definere servicekostnader</span><span class="sxs-lookup"><span data-stu-id="0ec8c-140">To set up service costs</span></span>
1. <span data-ttu-id="0ec8c-141">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicekostnader**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Costs**, and then choose the related link.</span></span> 
2. <span data-ttu-id="0ec8c-142">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-142">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a><span data-ttu-id="0ec8c-143">Angi en standardkost for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="0ec8c-143">To specify a default cost for service orders</span></span>
1. <span data-ttu-id="0ec8c-144">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="0ec8c-145">I feltet **Startgebyr for serviceordre** velger du den aktuelle servicekostnaden.</span><span class="sxs-lookup"><span data-stu-id="0ec8c-145">In the **Service Order Starting Fee** field, choose the appropriate service cost.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ec8c-146">Se også</span><span class="sxs-lookup"><span data-stu-id="0ec8c-146">See Also</span></span>
[<span data-ttu-id="0ec8c-147">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="0ec8c-147">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="0ec8c-148">Servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="0ec8c-148">Service Management</span></span>](service-service.md)  

