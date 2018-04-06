---
title: "Designdetaljer – Parti for parti | Microsoft-dokumentasjon"
description: "Lære hvordan du bruker parti for parti til å utligne ordreantall basert på behov."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 712068b5fafb8c5334bf48ddfc9242d21c0995e9
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-lot-for-lot"></a><span data-ttu-id="f01bd-103">Designdetaljer: Parti for parti</span><span class="sxs-lookup"><span data-stu-id="f01bd-103">Design Details: Lot-for-Lot</span></span>
<span data-ttu-id="f01bd-104">Prinsippet Parti for parti er det mest fleksible fordi systemet bare reagerer på faktisk behov, samt at det fungerer på forventet behov fra prognose og rammeordrer, og avklarer deretter ordreantallet basert på behovet.</span><span class="sxs-lookup"><span data-stu-id="f01bd-104">The lot-for-lot policy is the most flexible because the system only reacts on actual demand, plus it acts on anticipated demand from forecast and blanket orders and then settles the order quantity based on the demand.</span></span> <span data-ttu-id="f01bd-105">Prinsippet Parti for parti er rettet mot A- og B-varer der beholdningen kan godtas, men bør unngås.</span><span class="sxs-lookup"><span data-stu-id="f01bd-105">The lot-for-lot policy is aimed at A- and B-items where inventory can be accepted but should be avoided.</span></span>  
  
<span data-ttu-id="f01bd-106">Parti for parti-prinsippet er på mange måter lik ordreprinsippet, men det har en generell tilnærming til varer. Det kan godta antall i beholdningen, og det samler behov og tilsvarende forsyning i tidsperioder som er angitt av brukeren.</span><span class="sxs-lookup"><span data-stu-id="f01bd-106">In some ways, the lot-for-lot policy looks like the Order policy, but it has a generic approach to items; it can accept quantities in inventory, and it bundles demand and corresponding supply in time buckets defined by the user.</span></span>  
  
<span data-ttu-id="f01bd-107">Tidsperioden defineres i **Tidsperiode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f01bd-107">The time bucket is defined in the **Time Bucket** field.</span></span> <span data-ttu-id="f01bd-108">Systemet fungerer med en minste tidsperiode på én dag, siden dette er den minste tidsenheten for behovs- og forsyningshendelser i systemet (men i praksis kan tidsenheten for produksjonsordrer og komponentbehov være sekunder).</span><span class="sxs-lookup"><span data-stu-id="f01bd-108">The system works with a minimum time bucket of one day, since this is the smallest time unit of measure on demand and supply events in the system (although, in practice, the time unit of measure on production orders and component needs can be seconds).</span></span>  
  
<span data-ttu-id="f01bd-109">Tidsperioden setter også begrensninger på når en eksisterende forsyningsordre kan planlegges på nytt for å dekke et bestemt behov.</span><span class="sxs-lookup"><span data-stu-id="f01bd-109">The time bucket also sets limits on when an existing supply order should be rescheduled to meet a given demand.</span></span> <span data-ttu-id="f01bd-110">Hvis forsyningen er innenfor tidsperioden, det vil bli planlagt på nytt inn eller ut for å dekke behovet.</span><span class="sxs-lookup"><span data-stu-id="f01bd-110">If the supply lies within the time bucket, it will be rescheduled in or out to meet the demand.</span></span> <span data-ttu-id="f01bd-111">Hvis dette er tidligere, vil det føre til unødvendig oppbygging av beholdning og bør avbrytes.</span><span class="sxs-lookup"><span data-stu-id="f01bd-111">Otherwise, if it lies earlier, it will cause unnecessary build-up of inventory and should be canceled.</span></span> <span data-ttu-id="f01bd-112">Hvis det er plassert senere, vil det opprettes en ny ordre i stedet.</span><span class="sxs-lookup"><span data-stu-id="f01bd-112">If it lies later, a new supply order will be created instead.</span></span>  
  
<span data-ttu-id="f01bd-113">Med dette prinsippet er det også mulig å definere et sikkerhetslager for å kompensere for mulige svingninger i forsyning, eller for å dekke plutselig behov.</span><span class="sxs-lookup"><span data-stu-id="f01bd-113">With this policy, it is also possible to define a safety stock in order to compensate for possible fluctuations in supply, or to meet sudden demand.</span></span>  
  
<span data-ttu-id="f01bd-114">Siden forsyningsordreantallet er basert på det faktiske behovet, kan det være fornuftig å bruke ordremodifikatorer: runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor (eller kjøpsenhet for mål), reduser ordren til angitt maksimumsantall, eller reduser antallet til angitt maksimumsantall (og opprett dermed to eller flere forsyninger for å nå det totale nødvendige antallet).</span><span class="sxs-lookup"><span data-stu-id="f01bd-114">Because the supply order quantity is based on the actual demand it can make sense to use the order modifiers: round the order quantity up to meet a specified order multiple (or purchase unit of measure), increase the order to a specified minimum order quantity, or decrease the quantity to the specified maximum quantity (and thus create two or more supplies to reach the total needed quantity).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f01bd-115">Se også</span><span class="sxs-lookup"><span data-stu-id="f01bd-115">See Also</span></span>  
<span data-ttu-id="f01bd-116">[Designdetaljer: Gjenbestillingsprinsipper](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="f01bd-116">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="f01bd-117">[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="f01bd-117">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="f01bd-118">[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="f01bd-118">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="f01bd-119">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="f01bd-119">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
