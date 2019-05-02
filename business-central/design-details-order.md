---
title: Designdetaljer – Ordre | Microsoft-dokumentasjon
description: Dette emnet gir informasjon om ordre-til-ordre koblinger i et produser-til-ordre-miljø.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 4152dfb744215034383239ea98847fbf7b5751e9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803087"
---
# <a name="design-details-order"></a><span data-ttu-id="a873d-103">Designdetaljer: Ordre</span><span class="sxs-lookup"><span data-stu-id="a873d-103">Design Details: Order</span></span>
<span data-ttu-id="a873d-104">I et produser-til-ordre-miljø blir en vare utelukkende kjøpt eller produsert for å dekke et spesifikt behov.</span><span class="sxs-lookup"><span data-stu-id="a873d-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="a873d-105">Vanligvis er dette knyttet til A-varer, og motivasjon for å velge gjenbestillingsprinsippet Ordre kan være at behovet er sjeldent, leveringstiden er ubetydelig eller de nødvendige attributtene varierer.</span><span class="sxs-lookup"><span data-stu-id="a873d-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  

<span data-ttu-id="a873d-106">Programmet oppretter en ordre-til-ordre-kobling, som fungerer som en innledende forbindelse mellom forsyningen, en forsyningsordre eller beholdning, og behovet det skal dekke.</span><span class="sxs-lookup"><span data-stu-id="a873d-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  

<span data-ttu-id="a873d-107">I tillegg til bruk av ordrepolicy, kan ordre-til-ordre-koblingen brukes under planleggingen på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a873d-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  

* <span data-ttu-id="a873d-108">Når produksjonsprinsippet Produser til ordre brukes til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre).</span><span class="sxs-lookup"><span data-stu-id="a873d-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="a873d-109">Når funksjonen Ordreplanlegging brukes til å opprette en produksjonsordre fra en ordre.</span><span class="sxs-lookup"><span data-stu-id="a873d-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  

<span data-ttu-id="a873d-110">Selv om et produksjonsselskap anser seg selv som et miljø som produser til ordrer, kan det være best å bruke gjenbestillingsprinsippet parti for parti hvis varene er helt standard uten variasjon i attributter.</span><span class="sxs-lookup"><span data-stu-id="a873d-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="a873d-111">Resultatet blir at systemet bruker en endring i beholdningsnivået som ikke er planlagt, og akkumulerer bare ordrer med samme leveringsdato eller innenfor en angitt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="a873d-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  

## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="a873d-112">Odre-til-ordre-koblinger og tidligere forfallsdatoer</span><span class="sxs-lookup"><span data-stu-id="a873d-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="a873d-113">I motsetning til de fleste sett med forsyning/behov planlegger systemet fullstendig for koblede ordrer med forfallsdatoer som kommer før den planlagte startdatoen.</span><span class="sxs-lookup"><span data-stu-id="a873d-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="a873d-114">Forretningsårsaken til dette unntaket er at bestemte sett med behov/forsyning må synkroniseres helt frem til utførelse.</span><span class="sxs-lookup"><span data-stu-id="a873d-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="a873d-115">Hvis du vil ha mer informasjon om den frosne sonen som gjelder de fleste behovs-/forsyningstyper, kan du se [Designdetaljer: Håndtere ordrer før den planlagte startdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="a873d-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a873d-116">Se også</span><span class="sxs-lookup"><span data-stu-id="a873d-116">See Also</span></span>  
<span data-ttu-id="a873d-117">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a873d-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="a873d-118">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a873d-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="a873d-119">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a873d-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="a873d-120">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="a873d-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)