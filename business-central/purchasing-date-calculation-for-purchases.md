---
title: "Datoberegning for kjøp | Microsoft-dokumentasjon"
description: "Programmet beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato. Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8224f609dd110cd9f5d01d33d8e207f0c4aef6e0
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="e5705-104">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="e5705-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e5705-105"> beregner automatisk datoen du må bestille en vare på for å ha den på lager på en bestemt dato.</span><span class="sxs-lookup"><span data-stu-id="e5705-105"> automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="e5705-106">Dette er datoen da du kan forvente at varer som ble bestilt på en bestemt dato, vil være tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="e5705-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="e5705-107">Hvis du angir en ønsket mottaksdato på et bestillingshode, er den beregnede bestillingsdatoen datoen bestillingen må foretas for at du skal kunne motta varene på ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="e5705-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="e5705-108">Deretter beregnes datoen da varene er tilgjengelige for plukking, og denne angis i feltet **Forventet mottaksdato**.</span><span class="sxs-lookup"><span data-stu-id="e5705-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="e5705-109">Hvis du ikke angir en ønsket mottaksdato, brukes bestillingsdatoen på linjen som utgangspunkt for beregning av datoen du kan forvente å motta varene på, samt datoen som varene er tilgjengelige for plukking på.</span><span class="sxs-lookup"><span data-stu-id="e5705-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="e5705-110">Beregne med en ønsket mottaksdato</span><span class="sxs-lookup"><span data-stu-id="e5705-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="e5705-111">Hvis det finnes en ønsket mottaksdato på bestillingslinjen, brukes denne datoen som utgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="e5705-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="e5705-112">ønsket mottaksdato - beregning av leveringstid = bestillingsdato</span><span class="sxs-lookup"><span data-stu-id="e5705-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="e5705-113">ønsket mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato</span><span class="sxs-lookup"><span data-stu-id="e5705-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="e5705-114">Hvis du angir en ønsket mottaksdato i bestillingshodet, kopieres denne datoen til tilsvarende felt på alle linjene.</span><span class="sxs-lookup"><span data-stu-id="e5705-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="e5705-115">Du kan endre denne datoen på hvilken som helst av linjene, eller du kan fjerne datoen fra linjen.</span><span class="sxs-lookup"><span data-stu-id="e5705-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="e5705-116">Beregne uten en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="e5705-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="e5705-117">Hvis du angir en bestillingslinje uten en ønsket leveringsdato, fylles feltet **Ordredato** på linjen ut med datoen i feltet **Ordredato** i bestillingshodet.</span><span class="sxs-lookup"><span data-stu-id="e5705-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="e5705-118">Dette er enten den angitte datoen eller arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e5705-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="e5705-119">Følgende datoer beregnes deretter for bestillingslinjen, med utgangspunkt i bestillingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="e5705-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="e5705-120">bestillingsdato + beregning av leveringstid = planlagt mottaksdato</span><span class="sxs-lookup"><span data-stu-id="e5705-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="e5705-121">planlagt mottaksdato + inngående lagerhåndteringstid + sikkerhetsleveringstid = forventet mottaksdato</span><span class="sxs-lookup"><span data-stu-id="e5705-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="e5705-122">Hvis du endrer bestillingsdatoen på linjen, som når varene ikke er tilgjengelige hos leverandøren før på en senere dato, beregner de aktuelle datoene på linjen automatisk på nytt.</span><span class="sxs-lookup"><span data-stu-id="e5705-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="e5705-123">Hvis du endrer bestillingsdatoen i hodet, så kopieres denne datoen til feltet **Ordredato** på alle linjene, og alle de aktuelle datofeltene beregnes deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="e5705-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e5705-124">Se også</span><span class="sxs-lookup"><span data-stu-id="e5705-124">See Also</span></span>  
 <span data-ttu-id="e5705-125">[Beregne dato for salg](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="e5705-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="e5705-126">Beregne ordrebekreftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="e5705-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="e5705-127">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e5705-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

