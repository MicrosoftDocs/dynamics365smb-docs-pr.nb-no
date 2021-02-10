---
title: Automatisk samlet oppbryting med lagerstyring og plukk | Microsoft-dokumentasjon
description: For lokasjoner som bruker lagerstyring kan du bryte opp en større enhet til mindre enheter når det oppretter lagerinstruksjoner som oppfyller behovene fra kildedokumenter, produksjonsordrer eller interne plukk og plasseringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8d3ce697bb627bcc8acebc2392fe86b6af4b370b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759970"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="2d553-103">Aktivere automatisk samlet oppbryting med lagerstyring og plukk</span><span class="sxs-lookup"><span data-stu-id="2d553-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="2d553-104">For lokasjoner som bruker lagerstyring kan [!INCLUDE[prod_short](includes/prod_short.md)] i enkelte situasjoner utføre automatisk anbrekk, det vil si konvertere en større enhet til mindre enheter når det oppretter lagerinstruksjoner som oppfyller behovene fra kildedokumenter, produksjonsordrer eller interne plukk og plasseringer.</span><span class="sxs-lookup"><span data-stu-id="2d553-104">For locations that use directed put-away and pick, [!INCLUDE[prod_short](includes/prod_short.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="2d553-105">Anbrekk betyr også noen ganger å samle mindre enheter, hvis det er nødvendig for å imøtekomme utgående forespørsler. Det vil si å konvertere de større enhetene i kildedokumentet eller produksjonsordren til de mindre enhetene som er tilgjengelig i lageret.</span><span class="sxs-lookup"><span data-stu-id="2d553-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="2d553-106">Anbrekk i plukkinger</span><span class="sxs-lookup"><span data-stu-id="2d553-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="2d553-107">Hvis du vil lagre varer i flere enheter og vil tillate at de kombineres automatisk etter behov i plukkprosessen, merker du av for **Tillat anbrekk** på lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="2d553-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="2d553-108">Når det skal utføres en oppgave, ser programmet automatisk etter en vare i samme enhet.</span><span class="sxs-lookup"><span data-stu-id="2d553-108">To fulfill a task, application automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="2d553-109">Hvis det ikke kan finne denne varetypen, og du har valgt dette feltet, vil programmet foreslå at du kan konvertere en større enhet til den enheten som er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="2d553-109">But if it cannot find this form of the item, and this field is selected, application will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="2d553-110">Hvis systemet bare kan finne mindre enheter, vil det foreslå at du kan samle varer for å oppfylle antallet i følgeseddelen eller produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="2d553-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="2d553-111">I virkeligheten konverterer det den store enheten i kildedokumentet til mindre enheter for plukking.</span><span class="sxs-lookup"><span data-stu-id="2d553-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="2d553-112">Anbrekk i plasseringer</span><span class="sxs-lookup"><span data-stu-id="2d553-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="2d553-113">I plasseringen foreslår programmet automatisk Plasser-handlingslinjer i plasseringsenheten, for eksempel stykkevis, selv om varene ankommer i en annen enhet.</span><span class="sxs-lookup"><span data-stu-id="2d553-113">In the warehouse put-away, application automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="2d553-114">Anbrekk i flyttinger</span><span class="sxs-lookup"><span data-stu-id="2d553-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="2d553-115">Programmet utfører også automatisk anbrekk i etterfyllingsflyttinger hvis **Tillat anbrekk**-feltet er valgt på hurtigfanen **Alternativer** på siden **Beregn etterfylling av hylle**.</span><span class="sxs-lookup"><span data-stu-id="2d553-115">The application also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="2d553-116">Du kan vise resultatene av prosessen med konvertering fra én enhet til en annen som midlertidige anbrekkslinjer i plasserings-, plukk- eller flytteinstruksjonen.</span><span class="sxs-lookup"><span data-stu-id="2d553-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d553-117">Hvis du velger feltet **Anbrekksfilter** i lagerinstruksjonshodet, vil programmet skjule anbrekkslinjene når den større enheten skal brukes helt.</span><span class="sxs-lookup"><span data-stu-id="2d553-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, application will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="2d553-118">Hvis en pall for eksempel har 12 stykker, og du skal bruke alle 12, vil plukkingen be deg ta 1 pall i stedet for 12 stykker.</span><span class="sxs-lookup"><span data-stu-id="2d553-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="2d553-119">Hvis du imidlertid bare skal plukke 9 stykker, skjules ikke anbrekkslinjen, selv om du har valgt **Anbrekksfilter**-feltet, fordi du må sette de resterende tre stykkene et eller annet sted i lageret.</span><span class="sxs-lookup"><span data-stu-id="2d553-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2d553-120">Hvis du vil at enhetene skal fungere optimalt i lageret, også i forbindelse med anbrekksfunksjonaliteten, bør du prøve følgende der det er mulig:</span><span class="sxs-lookup"><span data-stu-id="2d553-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="2d553-121">Definer den grunnleggende vareenheten til den minste enheten du forventer å håndtere i lagerprosessene.</span><span class="sxs-lookup"><span data-stu-id="2d553-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="2d553-122">Definer de alternative vareenhetene som multiplum av den grunnleggende enheten.</span><span class="sxs-lookup"><span data-stu-id="2d553-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d553-123">Se også</span><span class="sxs-lookup"><span data-stu-id="2d553-123">See Also</span></span>  
[<span data-ttu-id="2d553-124">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="2d553-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2d553-125">Lager</span><span class="sxs-lookup"><span data-stu-id="2d553-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2d553-126">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2d553-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2d553-127">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2d553-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2d553-128">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="2d553-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2d553-129">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2d553-129">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
