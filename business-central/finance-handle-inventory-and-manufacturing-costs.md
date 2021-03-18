---
title: Håndtere lager- og produksjonskost | Microsoft-dokumentasjon
description: Selv om mange av funksjonene for kostredegjøring er uttrykt i underliggende prosesser uten brukerhandling, for eksempel postutligning og automatisk kostjustering, er mange felt, sider og rapporter rettet inn mot brukere som direkte eller indirekte håndterer vare- eller driftskost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8d376f7acb17084ef74ce7d10ce3b848758d51fc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386527"
---
# <a name="handling-inventory-and-manufacturing-costs"></a><span data-ttu-id="18aa2-103">Håndtere lager- og produksjonskost</span><span class="sxs-lookup"><span data-stu-id="18aa2-103">Handling Inventory and Manufacturing Costs</span></span>
<span data-ttu-id="18aa2-104">Selv om mange av funksjonene for kostredegjøring er uttrykt i underliggende prosesser uten brukerhandling, for eksempel postutligning og automatisk kostjustering, er mange felt, sider og rapporter rettet inn mot brukere som direkte eller indirekte håndterer vare- eller driftskost.</span><span class="sxs-lookup"><span data-stu-id="18aa2-104">Although much of the cost accounting functionality is expressed in underlying processes with no user interaction, such as entry application and automatic cost adjustment, a number of fields, pages, and reports are aimed at users who directly or indirectly manage the cost of items or operations.</span></span>  

 <span data-ttu-id="18aa2-105">Tilordning av varegebyrer til kjøpsdokumenter er et eksempel på en indirekte kostredegjørelsesoppgave.</span><span class="sxs-lookup"><span data-stu-id="18aa2-105">Assigning item charges to purchase documents is an example of an indirect cost accounting task.</span></span> <span data-ttu-id="18aa2-106">Oppdatering av enhetskost for en monterings- eller produksjonsstykklistevare er et eksempel på en mer direkte kostredegjørelsesoppgave.</span><span class="sxs-lookup"><span data-stu-id="18aa2-106">Updating the unit cost of assembly or production BOM item is an example of a more direct cost accounting task.</span></span>  

 <span data-ttu-id="18aa2-107">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="18aa2-107">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="18aa2-108">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="18aa2-108">**To**</span></span>|<span data-ttu-id="18aa2-109">**Se**</span><span class="sxs-lookup"><span data-stu-id="18aa2-109">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="18aa2-110">Jevnlig eller automatisk oppdatere enhetskost for én eller flere varer for å videreføre eventuelle kostendringer fra inngående poster, for eksempel poster for kjøp eller produksjonsresultat, til de relaterte utgående postene, for eksempel forbruk eller overføring.</span><span class="sxs-lookup"><span data-stu-id="18aa2-110">Periodically or automatically update the unit cost of one or multiple items to forward any cost changes from inbound entries, such as those for purchases or production output, to the related outbound entries, such as consumption or transfers.</span></span>|[<span data-ttu-id="18aa2-111">Justere varekost</span><span class="sxs-lookup"><span data-stu-id="18aa2-111">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="18aa2-112">Få innsikt i dynamikken for gjennomsnittskost for å ta prisavgjørelser eller spore kostendringer som skyldes feil i dataregistreringen.</span><span class="sxs-lookup"><span data-stu-id="18aa2-112">Get insight into average cost dynamics to make pricing decisions or to track cost fluctuations caused by data entry errors.</span></span>|[<span data-ttu-id="18aa2-113">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="18aa2-113">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="18aa2-114">Opprette standardkost for en produksjonsvare ved å registrere de tre kostelementene: materialkost, kapasitetskost og underleverandørkost.</span><span class="sxs-lookup"><span data-stu-id="18aa2-114">Create a manufacturing item's standard cost by entering the three cost elements: material cost, capacity cost, and subcontractor cost.</span></span>|[<span data-ttu-id="18aa2-115">Om beregning av standardkost</span><span class="sxs-lookup"><span data-stu-id="18aa2-115">About Calculating Standard Cost</span></span>](finance-about-calculating-standard-cost.md)|  
|<span data-ttu-id="18aa2-116">Beregne enhetskost for en stykklistevare basert på enhetskost for de underliggende komponentene.</span><span class="sxs-lookup"><span data-stu-id="18aa2-116">Calculate the unit cost of a BOM item based on the unit costs of its underlying components.</span></span>|[<span data-ttu-id="18aa2-117">Arbeide med stykklister</span><span class="sxs-lookup"><span data-stu-id="18aa2-117">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|  
|<span data-ttu-id="18aa2-118">Fullføre livssyklusen for kostberegning for en produsert vare ved å justere kost og avstemme verdipostene mot Finans.</span><span class="sxs-lookup"><span data-stu-id="18aa2-118">Complete the costing life cycle of a produced item by adjusting the costs and reconciling the value entries with the general ledger.</span></span>|[<span data-ttu-id="18aa2-119">Om fullførte produksjonsordrekostnader</span><span class="sxs-lookup"><span data-stu-id="18aa2-119">About Finished Production Order Costs</span></span>](finance-about-finished-production-order-costs.md)|  
|<span data-ttu-id="18aa2-120">Endre verdien for en vare på lager eller verdien for en varepost, for eksempel en kjøpstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="18aa2-120">Change the value of an item in inventory or the value of one item ledger entry, such as a purchase transaction.</span></span>|[<span data-ttu-id="18aa2-121">Revaluere beholdning</span><span class="sxs-lookup"><span data-stu-id="18aa2-121">Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="18aa2-122">Manuelt angre en vareutligning eller utligne vareposter som er opprettet i programmet, på nytt.</span><span class="sxs-lookup"><span data-stu-id="18aa2-122">Manually undo an item application or reapply item ledger entries created by application.</span></span>|[<span data-ttu-id="18aa2-123">Fjerne varefinansposter og utligne dem på nytt</span><span class="sxs-lookup"><span data-stu-id="18aa2-123">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)|  
|<span data-ttu-id="18aa2-124">Bruk feltet **Utlignet fra-post** i varekladden til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="18aa2-124">Use the **Applies-from Entry** field in the item journal to manually create a fixed application between an inbound transaction and the original outbound transaction.</span></span>|[<span data-ttu-id="18aa2-125">Lukke åpne vareposter som er resultat av fast utligning i varekladden</span><span class="sxs-lookup"><span data-stu-id="18aa2-125">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a><span data-ttu-id="18aa2-126">Se også</span><span class="sxs-lookup"><span data-stu-id="18aa2-126">See Also</span></span>  
<span data-ttu-id="18aa2-127">[Administrere lagerkostnader](finance-manage-inventory-costs.md)
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)</span><span class="sxs-lookup"><span data-stu-id="18aa2-127">[Manage Inventory Costs](finance-manage-inventory-costs.md)
[Design Details: Inventory Costing](design-details-inventory-costing.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]