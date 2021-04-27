---
title: Datoberegning for salg | Microsoft-dokumentasjon
description: Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 49bc91d049ee6c2357323ed4e88f66116322d276
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778900"
---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="e4ff2-104">Beregne dato for salg</span><span class="sxs-lookup"><span data-stu-id="e4ff2-104">Date Calculation for Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e4ff2-105">beregner automatisk hvilken dato en vare på en ordrelinje tidligst kan leveres på.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-105">automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="e4ff2-106">Hvis en kunde har bedt om en bestemt leveringsdato, beregnes datoen varene må være tilgjengelige for plukking, for at leveringsdatoen skal kunne innfris.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="e4ff2-107">Hvis kunden ikke ber om en bestemt leveringsdato, beregnes datoen varene kan leveres på, fra og med den datoen varene er tilgjengelige for plukking.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="e4ff2-108">Beregne en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="e4ff2-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="e4ff2-109">Hvis du angir en ønsket leveringsdato på ordren, blir denne datoen som utgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-109">If you specify a requested delivery date on the sales order line, that date becomes the starting point for the following calculations.</span></span>

- <span data-ttu-id="e4ff2-110">ønsket leveringsdato - leveringstid = planlagt forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="e4ff2-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="e4ff2-111">planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="e4ff2-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="e4ff2-112">Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span> <span data-ttu-id="e4ff2-113">Hvis ikke, vises en advarsel om tomt lager.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-113">Otherwise, a stock-out warning is displayed.</span></span>

> [!Note]
> <span data-ttu-id="e4ff2-114">Hvis prosessen er basert på beregning bakover, for eksempel hvis du bruker ønsket leveringsdato til å hente den planlagte forsendelsesdatoen, anbefaler vi at du bruker datoformler som har faste varigheter, for eksempel "5D" i fem dager eller "1U" for én uke.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-114">If your process is based on backward calculation, for example, if you use the requested delivery date to get the planned shipment date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="e4ff2-115">Datoformler uten faste varigheter, for eksempel "GU" for gjeldende uke eller GM for gjeldende måned, kan resultere i feil datoberegninger.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-115">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="e4ff2-116">Hvis du vil ha mer informasjon om datoformler, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="e4ff2-116">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="e4ff2-117">Beregne den tidligste mulige leveringsdatoen</span><span class="sxs-lookup"><span data-stu-id="e4ff2-117">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="e4ff2-118">Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-118">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="e4ff2-119">Denne datoen angis deretter i feltet Forsendelsesdato på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende formler.</span><span class="sxs-lookup"><span data-stu-id="e4ff2-119">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="e4ff2-120">forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="e4ff2-120">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="e4ff2-121">planlagt forsendelsesdato + leveringstid = planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="e4ff2-121">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="e4ff2-122">Se også</span><span class="sxs-lookup"><span data-stu-id="e4ff2-122">See Also</span></span>  
 <span data-ttu-id="e4ff2-123">[Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="e4ff2-123">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="e4ff2-124">Beregne ordrebekreftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="e4ff2-124">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="e4ff2-125">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4ff2-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]