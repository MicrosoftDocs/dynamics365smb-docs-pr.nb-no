---
title: Datoberegning for salg | Microsoft-dokumentasjon
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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7de382530c1872155903bfa015866cf99a9f5566
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="date-calculation-for-sales"></a><span data-ttu-id="ea543-104">Beregne dato for salg</span><span class="sxs-lookup"><span data-stu-id="ea543-104">Date Calculation for Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ea543-105">beregner automatisk hvilken dato en vare på en ordrelinje tidligst kan leveres på.</span><span class="sxs-lookup"><span data-stu-id="ea543-105"> automatically calculates the earliest possible date that an item on a sales order line can be shipped.</span></span>

<span data-ttu-id="ea543-106">Hvis en kunde har bedt om en bestemt leveringsdato, beregnes datoen varene må være tilgjengelige for plukking, for at leveringsdatoen skal kunne innfris.</span><span class="sxs-lookup"><span data-stu-id="ea543-106">If the customer has requested a specific delivery date, then the date on which the items must be available to pick to meet that delivery date is calculated.</span></span>

<span data-ttu-id="ea543-107">Hvis kunden ikke ber om en bestemt leveringsdato, beregnes datoen varene kan leveres på, fra og med den datoen varene er tilgjengelige for plukking.</span><span class="sxs-lookup"><span data-stu-id="ea543-107">If the customer does not request a specific delivery date, then the date on which the items can be delivered is calculated, starting from the date on which the items are available for picking.</span></span>

## <a name="calculating-a-requested-delivery-date"></a><span data-ttu-id="ea543-108">Beregne en ønsket leveringsdato</span><span class="sxs-lookup"><span data-stu-id="ea543-108">Calculating a Requested Delivery Date</span></span>
<span data-ttu-id="ea543-109">Hvis du angir en ønsket leveringsdato på ordren, brukes denne datoen som utgangspunkt for følgende beregninger.</span><span class="sxs-lookup"><span data-stu-id="ea543-109">If you specify a requested delivery date on the sales order line, then that date is used as the starting point for the following calculations.</span></span>

- <span data-ttu-id="ea543-110">ønsket leveringsdato - leveringstid = planlagt forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ea543-110">requested delivery date - shipping time = planned shipment date</span></span>
- <span data-ttu-id="ea543-111">planlagt forsendelsesdato - utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ea543-111">planned shipment date - outbound whse. handling time = shipment date</span></span>

<span data-ttu-id="ea543-112">Hvis varene er tilgjengelige for plukking på forsendelsesdatoen, kan salgsprosessen fortsette.</span><span class="sxs-lookup"><span data-stu-id="ea543-112">If the items are available to pick on the shipment date, then the sales process can continue.</span></span>

<span data-ttu-id="ea543-113">Hvis ikke varene er tilgjengelige for plukking på forsendelsesdatoen, vises en advarsel om at det er tomt på lager.</span><span class="sxs-lookup"><span data-stu-id="ea543-113">If the items are not available to be picked on the shipment date, then a stock-out warning is displayed.</span></span>

## <a name="calculating-the-earliest-possible-delivery-date"></a><span data-ttu-id="ea543-114">Beregne den tidligste mulige leveringsdatoen</span><span class="sxs-lookup"><span data-stu-id="ea543-114">Calculating the Earliest Possible Delivery Date</span></span>
<span data-ttu-id="ea543-115">Hvis du ikke angir en ønsket leveringsdato på ordrelinjen, eller hvis ønsket leveringsdato ikke kan innfris, beregnes datoen som varene tidligst er tilgjengelige på.</span><span class="sxs-lookup"><span data-stu-id="ea543-115">If you do not specify a requested delivery date on the sales order line, or if the requested delivery date cannot be met, then the earliest date on which that the items are available is calculated.</span></span> <span data-ttu-id="ea543-116">Denne datoen angis deretter i feltet Forsendelsesdato på linjen, og datoen du planlegger å sende og levere varene til kunden på beregnes også ved hjelp av følgende formler.</span><span class="sxs-lookup"><span data-stu-id="ea543-116">That date is then entered in the Shipment Date field on the line, and the date on which you plan to ship the items as well as the date on which they will be delivered to the customer are calculated using the following formulas.</span></span>

- <span data-ttu-id="ea543-117">forsendelsesdato + utgående lagerhåndteringstid = forsendelsesdato</span><span class="sxs-lookup"><span data-stu-id="ea543-117">shipment date + outbound whse. handling time = planned shipment date</span></span>
- <span data-ttu-id="ea543-118">planlagt forsendelsesdato + leveringstid = planlagt leveringsdato</span><span class="sxs-lookup"><span data-stu-id="ea543-118">planned shipment date + shipping time = planned delivery date</span></span>


## <a name="see-also"></a><span data-ttu-id="ea543-119">Se også</span><span class="sxs-lookup"><span data-stu-id="ea543-119">See Also</span></span>  
 <span data-ttu-id="ea543-120">[Beregne dato for kjøp](purchasing-date-calculation-for-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="ea543-120">[Date Calculation for Purchases](purchasing-date-calculation-for-purchases.md) </span></span>  
 [<span data-ttu-id="ea543-121">Beregne ordrebekreftelsesdatoer</span><span class="sxs-lookup"><span data-stu-id="ea543-121">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="ea543-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea543-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

