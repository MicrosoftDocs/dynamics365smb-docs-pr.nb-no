---
title: Definere det generelle lageroppsettet
description: Beskriver hvordan du definerer det generelle lageroppsettet slik at du kan styre lageret og varene.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 10344ae85edc8a63dcff1a5a5927bf2d19045810
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389402"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="0bded-103">Definere generell informasjon om lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0bded-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="0bded-104">Du angir det generelle lageroppsettet på siden **Lageroppsett**.</span><span class="sxs-lookup"><span data-stu-id="0bded-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="0bded-105">Slik definerer du generell informasjon om lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="0bded-105">To set up general inventory information</span></span>

1. <span data-ttu-id="0bded-106">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageroppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0bded-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0bded-107">På siden **Lageroppsett** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0bded-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="0bded-108">Hvis du vil ha mer informasjon om kostnadsfelt, **Automatisk kostbokføring**, **Bokf. av forventet kost i Finans** og **Standard lagermetode**, se [Avstemme lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md) og [Designdetaljer: Bokføre forventet kost](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="0bded-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="0bded-109">Hvis du vil ha mer informasjon om kostberegning generelt, se [Administrere lagerkostnader](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="0bded-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="0bded-110">Hvis du vil at inngående lagerhåndteringstid skal tas med i beregningen av ordrebekreftelse på bestillingslinjen, kan du definere den som standard for lageret, på siden **Lageroppsett**, og for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="0bded-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="0bded-111">Hvis du vil ha mer informasjon, kan du se [Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="0bded-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="0bded-112">Alternativet **Automatisk kostjustering** er aktivert som standard for å sikre at lagerverdier alltid er riktige i finans, som i sin tur holder salgs- og fortjenestestatistikk oppdatert.</span><span class="sxs-lookup"><span data-stu-id="0bded-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="0bded-113">Kostendringer fra inngående poster, for eksempel de for kjøp eller produksjonsavgang, tilordnes til de relaterte utgående postene, for eksempel salg eller overføringer.</span><span class="sxs-lookup"><span data-stu-id="0bded-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="0bded-114">Dette er nyttig for nye [!INCLUDE[prod_short](includes/prod_short.md)]-kunder og små bedrifter med relativt lave lagertransaksjonsnivåer.</span><span class="sxs-lookup"><span data-stu-id="0bded-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="0bded-115">Når virksomheten vokser og lagernivåer øker, kan imidlertid dette redusere systemets ytelse.</span><span class="sxs-lookup"><span data-stu-id="0bded-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="0bded-116">Hvis du vil minimere redusert ytelse under bokføringen, velger du et tidsalternativ for å definere hvor langt tilbake i tid fra arbeidsdatoen en inngående transaksjon kan forekomme for potensielt å utløse justering av relaterte utgående verdiposter.</span><span class="sxs-lookup"><span data-stu-id="0bded-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="0bded-117">Alternativt kan du justere kostnader manuelt ved jevne mellomrom med kjørselen Juster kostverdi – vareposter.</span><span class="sxs-lookup"><span data-stu-id="0bded-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bded-118">Se også</span><span class="sxs-lookup"><span data-stu-id="0bded-118">See Also</span></span>
[<span data-ttu-id="0bded-119">Definere lager</span><span class="sxs-lookup"><span data-stu-id="0bded-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="0bded-120">[Designdetaljer: Kostmetoder](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="0bded-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="0bded-121">Håndtere lager</span><span class="sxs-lookup"><span data-stu-id="0bded-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0bded-122">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0bded-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0bded-123">Endre hvilke funksjoner som vises</span><span class="sxs-lookup"><span data-stu-id="0bded-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="0bded-124">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0bded-124">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]