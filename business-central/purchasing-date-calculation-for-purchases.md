---
title: Datoberegning for kjøp | Microsoft-dokumentasjon
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22153df1e56d274256b53d426e2dff30cad3e4bc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758595"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="b248a-104">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="b248a-104">Date Calculation for Purchases</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b248a-105">beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="b248a-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="b248a-106">Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="b248a-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="b248a-107">Hvis du angir en ønsket mottaksdato på et bestillingshode, er den beregnede bestillingsdatoen datoen bestillingen må foretas for at du skal kunne motta varene på ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="b248a-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="b248a-108">Deretter beregnes datoen da varene er tilgjengelige for plukking, og denne angis i feltet **Forventet mottaksdato**.</span><span class="sxs-lookup"><span data-stu-id="b248a-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="b248a-109">Hvis du ikke angir en ønsket mottaksdato, brukes bestillingsdatoen på linjen som utgangspunkt for beregning av datoen du kan forvente å motta varene på, samt datoen som varene er tilgjengelige for plukking på.</span><span class="sxs-lookup"><span data-stu-id="b248a-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="b248a-110">Beregne med en ønsket mottaksdato</span><span class="sxs-lookup"><span data-stu-id="b248a-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="b248a-111">Hvis det finnes en ønsket mottaksdato på bestillingslinjen, brukes denne datoen som utgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="b248a-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="b248a-112">ønsket mottaksdato - beregning av leveringstid = bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="b248a-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="b248a-113">ønsket mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato</span><span class="sxs-lookup"><span data-stu-id="b248a-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="b248a-114">Hvis du angir en ønsket mottaksdato i bestillingshodet, kopieres denne datoen til tilsvarende felt på alle linjene.</span><span class="sxs-lookup"><span data-stu-id="b248a-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="b248a-115">Du kan endre denne datoen på hvilken som helst av linjene, eller du kan fjerne datoen fra linjen.</span><span class="sxs-lookup"><span data-stu-id="b248a-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="b248a-116">Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket mottaksdato til å hente den planlagte ordredatoen, anbefaler vi at du bruker datoformler som har faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke.</span><span class="sxs-lookup"><span data-stu-id="b248a-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="b248a-117">Datoformler uten faste varigheter, for eksempel "GU" for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger.</span><span class="sxs-lookup"><span data-stu-id="b248a-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="b248a-118">Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="b248a-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="b248a-119">Beregne uten en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="b248a-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="b248a-120">Hvis du angir en bestillingslinje uten en ønsket leveringsdato, fylles feltet **Ordredato** på linjen ut med datoen i feltet **Ordredato** i bestillingshodet.</span><span class="sxs-lookup"><span data-stu-id="b248a-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="b248a-121">Dette er enten den angitte datoen eller arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b248a-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="b248a-122">Følgende datoer beregnes deretter for bestillingslinjen, med utgangspunkt i bestillingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b248a-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="b248a-123">bestillingsdato + beregning av leveringstid = planlagt mottaksdato</span><span class="sxs-lookup"><span data-stu-id="b248a-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="b248a-124">planlagt mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato</span><span class="sxs-lookup"><span data-stu-id="b248a-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="b248a-125">Hvis du endrer bestillingsdatoen på linjen, som når varene ikke er tilgjengelige hos leverandøren før på en senere dato, beregner de aktuelle datoene på linjen automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="b248a-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="b248a-126">Hvis du endrer bestillingsdatoen i hodet, så kopieres denne datoen til feltet **Ordredato** på alle linjene, og alle de aktuelle datofeltene beregnes deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="b248a-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="b248a-127">Standardverdier for beregning av leveringstid</span><span class="sxs-lookup"><span data-stu-id="b248a-127">Default values for lead time calculation</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b248a-128">bruker verdien fra feltet **Beregning av leveringstid** på bestillingslinjen for å beregne ordren og de forventede mottaksdatoene.</span><span class="sxs-lookup"><span data-stu-id="b248a-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="b248a-129">Du kan angi verdien på linjen manuelt eller la programmet bruke verdier som er definert på leverandørkortet, varekortet, lagerføringsenhetskortet eller leverandørens varekatalog.</span><span class="sxs-lookup"><span data-stu-id="b248a-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="b248a-130">Verdien for leveringstid på leverandørkortet brukes imidlertid bare hvis det ikke er angitt en leveringstid på varekortet, lagerføringsenhetskortet eller i leverandørens varekatalog for varen.</span><span class="sxs-lookup"><span data-stu-id="b248a-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="b248a-131">Dette er også den eskalerende prioritetsrekkefølgen for disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="b248a-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="b248a-132">Hvis alle er angitt, har leveringstiden fra leverandørkortet laveste prioritet, og leveringstiden fra leverandørens varekatalog har høyeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="b248a-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b248a-133">Se også</span><span class="sxs-lookup"><span data-stu-id="b248a-133">See Also</span></span>

<span data-ttu-id="b248a-134">[Beregne dato for salg](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="b248a-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="b248a-135">Beregne ordrebekreftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="b248a-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="b248a-136">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b248a-136">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
