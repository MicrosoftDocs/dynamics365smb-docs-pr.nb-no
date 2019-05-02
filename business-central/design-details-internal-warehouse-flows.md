---
title: Designdetaljer – Interne lagerflyter | Microsoft-dokumentasjon
description: Flyten av varer mellom hyller på en selskapslokasjon dreier seg i hovedsak om å plukke komponenter og plassere sluttvarer for montering eller produksjonsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten en relasjon til kildedokumenter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b728815592975091a683eb96f87b1a632da62567
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803789"
---
# <a name="design-details-internal-warehouse-flows"></a><span data-ttu-id="1dbe7-103">Designdetaljer: Interne lagerflyter</span><span class="sxs-lookup"><span data-stu-id="1dbe7-103">Design Details: Internal Warehouse Flows</span></span>
<span data-ttu-id="1dbe7-104">Flyten av varer mellom hyller på en selskapslokasjon dreier seg i hovedsak om å plukke komponenter og plassere sluttvarer for montering eller produksjonsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten en relasjon til kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-104">The flow of items between bins at a company location centers on picking components and putting away end items for assembly or production orders and ad-hoc movements, such as bin replenishments, without a relation to source documents.</span></span> <span data-ttu-id="1dbe7-105">Omfanget av og karakteren til aktivitetene som er involvert, varierer mellom grunnleggende og avanserte lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-105">The scope and nature of the involved activities vary between basic and advanced warehousing.</span></span>  

 <span data-ttu-id="1dbe7-106">Enkelte interne flyter overlapper inngående eller utgående flyter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-106">Some internal flows overlap with inbound or outbound flows.</span></span> <span data-ttu-id="1dbe7-107">Noe av denne overlappingen vises som trinn 4 og 5 i de grafiske diagrammene for henholdsvis avanserte inngående og utgående flyter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-107">Some of this overlap is shown as steps 4 and 5 in the graphical diagrams for advanced inbound and outbound flows respectively.</span></span> <span data-ttu-id="1dbe7-108">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Inngående lagerflyt](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="1dbe7-108">For more information, see [Design Details: Inbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

## <a name="internal-flows-in-basic-warehousing"></a><span data-ttu-id="1dbe7-109">Interne flyter i Grunnleggende lagerstyring</span><span class="sxs-lookup"><span data-stu-id="1dbe7-109">Internal Flows in Basic Warehousing</span></span>  
 <span data-ttu-id="1dbe7-110">I grunnleggende lageroppsett vil flyten av varer mellom hyller i selskapet være sentrert rundt plukk av komponenter og plassering av sluttvarer for produksjons- og monteringsordrer og adhocflyttinger, for eksempel etterfylling av hyller, uten relasjon til kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-110">In basic warehouse configuration, the flow of items between bins inside the company centers on picking component and putting away end items for production or assembly orders and ad-hoc movements, such as bin replenishments, without relation to source documents.</span></span>  

### <a name="flows-to-and-from-production"></a><span data-ttu-id="1dbe7-111">Flyter til og fra produksjon</span><span class="sxs-lookup"><span data-stu-id="1dbe7-111">Flows to and from Production</span></span>  
 <span data-ttu-id="1dbe7-112">Hovedintegrasjonen mellom produksjonsordrer og grunnleggende lageraktiviteter representeres av muligheten til å plukke produksjonskomponenter på siden **Lagerplukk** eller **Lagerflytting**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-112">The main integration between production orders and basic warehouse activities is represented by the ability to pick production components with the **Inventory Pick** or the **Inventory Movement** pages.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1dbe7-113">På siden **Lagerplukk** bokføres komponentforbruket sammen med plukkbokføringen.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-113">On the **Inventory Pick** page, the component consumption is posted together with the pick posting.</span></span> <span data-ttu-id="1dbe7-114">Ved hjelp av siden **Lagerflytting**, blir bare hyllejusteringer registrert, og det utføres ingen finansbokføringer for varen.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-114">By using the **Inventory Movement** page, only bin adjustments are registered, no item ledger posting occurs.</span></span>  

 <span data-ttu-id="1dbe7-115">I tillegg til komponenthåndtering representeres integreringen av muligheten til å plassere produserte varer med siden **Lagerplassering**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-115">In addition to component handling, the integration is represented by the ability to put produced items away with the **Inventory Put-away** page.</span></span>  

 <span data-ttu-id="1dbe7-116">Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjonskortet eller kortene for produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-116">The **To-Production Bin Code**, **From-Production Bin Code**, and **Open Shop Floor Bin Code** fields on the location card or the machine/work center cards define default flows to and from production areas.</span></span>  

 <span data-ttu-id="1dbe7-117">Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du se avsnittet Trekke produksjonskomponenter i lageret i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-117">For more information about how component consumption is flushed from the To-Production or Open Shop Floor bins, see the “Flushing Production Components in the Warehouse” section in this topic.</span></span>  

### <a name="flows-to-and-from-assembly"></a><span data-ttu-id="1dbe7-118">Flyter til og fra montering</span><span class="sxs-lookup"><span data-stu-id="1dbe7-118">Flows to and from Assembly</span></span>  
 <span data-ttu-id="1dbe7-119">Hovedintegrasjonen mellom monteringsordrer og grunnleggende lageraktiviteter representeres av muligheten til å flytte en monteringskomponent til monteringsområdet.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-119">The main integration between assembly orders and basic warehouse activities is represented by the ability to move assembly components to the assembly area.</span></span>  

 <span data-ttu-id="1dbe7-120">Det finnes ingen bestemt lagerfunksjonalitet for å plassere monteringsvarer, men du kan angi en standard plasseringshylle for hyllekoden i monteringsordrehodet.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-120">While no specific warehouse functionality exists for putting assembly items away, the bin code on the assembly order header may be set to a default put-away bin.</span></span> <span data-ttu-id="1dbe7-121">Bokføring av monteringsordre Funksjoner da som bokføring av en plassering.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-121">Posting the assembly order then functions like posting a put-away.</span></span> <span data-ttu-id="1dbe7-122">Lageraktiviteten som flytter monteringsvarer til lageret, kan håndteres på siden **Intern flytting** uten noen relasjon til monteringsordren.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-122">The warehouse activity to move assembly items into the warehouse can be managed on the **Internal Movement** page, with no relation to the assembly order.</span></span>  

 <span data-ttu-id="1dbe7-123">Følgende monteringsflyter finnes.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-123">The following assembly flows exist.</span></span>  

|<span data-ttu-id="1dbe7-124">Flyt</span><span class="sxs-lookup"><span data-stu-id="1dbe7-124">Flow</span></span>|<span data-ttu-id="1dbe7-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1dbe7-125">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="1dbe7-126">Monter til lager</span><span class="sxs-lookup"><span data-stu-id="1dbe7-126">Assemble-to-stock</span></span>|<span data-ttu-id="1dbe7-127">Komponentene trengs i en monteringsordre der avgangen lagres på lageret.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-127">The components are needed on an assembly order where the output is stored in the warehouse.</span></span><br /><br /> <span data-ttu-id="1dbe7-128">Denne lagerflyten håndteres på siden **Lagerflytting**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-128">This warehouse flow is managed on the **Inventory Movement** page.</span></span> <span data-ttu-id="1dbe7-129">Én hentelinje angir hvor komponentene skal hentes fra.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-129">One take line specifies where to take the components.</span></span> <span data-ttu-id="1dbe7-130">Én plasseringslinje angir hvor komponentene skal plasseres.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-130">One place line specifies where to place the components.</span></span>|  
|<span data-ttu-id="1dbe7-131">Monter til ordre</span><span class="sxs-lookup"><span data-stu-id="1dbe7-131">Assemble-to-order</span></span>|<span data-ttu-id="1dbe7-132">Komponentene trengs i en monteringsordre som er knyttet til en ordre som leveres når den solgte varen er montert.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-132">The components are needed on an assembly order that is linked to a sales order that is shipped when the sold item is assembled.</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="1dbe7-133">Hvis varer monteres til ordre, vil lagerplukk for den tilknyttede ordren deretter utløse en lagerflytting for alle involverte monteringskomponenter, ikke bare for den solgte varen som når du leverer varer på lager.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-133">If items are assembled to order, then the inventory pick of the linked sales order triggers an inventory movement for all the involved assembly components, not just for the sold item as when shipping inventory items.</span></span>  

 <span data-ttu-id="1dbe7-134">Feltene **Til-Hyllekode for montering**, **Fra-Hyllekode for montering** og **Hyllek. lev. fra m. til ordre** på lokasjonskortet definerer standardflyter til og fra monteringsområder.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-134">The **To-Assembly Bin Code**, **From-Assembly Bin Code**, and **Asm.-to-Order Shpt. Bin Code** fields on the location card define default flows to and from assembly areas.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1dbe7-135">Feltet **Hyllek. lev. fra m. til ordre** fungerer som fra-hylle for montering i monter-til-ordre-scenarier.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-135">The **Asm.-to-Order Shpt. Bin Code** field functions as the from-assembly bin in assemble-to-order scenarios.</span></span>  

### <a name="ad-hoc-movements"></a><span data-ttu-id="1dbe7-136">Adhocflyttinger</span><span class="sxs-lookup"><span data-stu-id="1dbe7-136">Ad-Hoc Movements</span></span>  
 <span data-ttu-id="1dbe7-137">I grunnleggende lagerstyring blir flytting av varer fra hylle til hylle uten relasjon til kildedokumenter, utført på siden **Intern flytting**, som fungerer sammen med siden **Lagerflytting**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-137">In basic warehousing, the movement of items from bin to bin without relation to source documents is performed on the **Internal Movement** page, which functions together with the **Inventory Movement** page.</span></span>  

 <span data-ttu-id="1dbe7-138">En metode for flytting av varer ad hoc mellom hyller, er å bokføre positive poster i feltet **Ny hyllekode** på siden **Vareoverf.kladd**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-138">Another way to move items ad hoc between bins is to post positive entries in the **New Bin Code** field on the **Item Reclass. Journal** page.</span></span>  

## <a name="internal-flows-in-advanced-warehousing"></a><span data-ttu-id="1dbe7-139">Interne flyter i Avansert lagerstyring</span><span class="sxs-lookup"><span data-stu-id="1dbe7-139">Internal Flows in Advanced Warehousing</span></span>  
 <span data-ttu-id="1dbe7-140">I avanserte lageroppsett er flyten av varer mellom hyller i selskapet sentrert rundt plukk av komponenter og plassering av sluttvarer for produksjonsordrer og plukk av komponenter for monteringsordrer.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-140">In advanced warehouse configurations, the flow of items between bins inside the company centers on picking component and putting away end items for production orders and picking components for assembly orders.</span></span> <span data-ttu-id="1dbe7-141">I tillegg oppstår interne flyter som ad hoc-flyttinger, for eksempel etterfylling av hyller, uten relasjon til kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-141">In addition, internal flows occur as ad-hoc movements, such as bin replenishments, without relation to source documents.</span></span>  

### <a name="flows-to-and-from-production"></a><span data-ttu-id="1dbe7-142">Flyter til og fra produksjon</span><span class="sxs-lookup"><span data-stu-id="1dbe7-142">Flows To and From Production</span></span>  
 <span data-ttu-id="1dbe7-143">Hovedintegrasjonen mellom produksjonsordrer og avanserte lageraktiviteter representeres av muligheten til å plukke produksjonskomponenter på **Plukk**-siden og **Plukkforslag**-siden og muligheten til å plassere produserte varer på **Intern plassering**-siden.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-143">The main integration between production orders and advanced warehouse activities is represented by the ability to pick production components, on the **Warehouse Pick** page and the **Pick Worksheet** page, and the ability to put produced items away with the **Whse. Internal-Put-away** page.</span></span>  

 <span data-ttu-id="1dbe7-144">Et annet integreringspunkt i produksjonen finnes på siden **Lagerflytting** og på siden Flytteforslag, der du kan plassere komponenter og ta produserte varer for frigitte produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-144">Another integration point in production is provided with the **Warehouse Movement** page, together with the Movement Worksheet page, which enables you to place components and take produced items for released production orders.</span></span>  

 <span data-ttu-id="1dbe7-145">Feltene **Til-Hyllekode for produksjon**, **Fra-Hyllekode for produksjon** og **Åpen prod.hyllekode** på lokasjonskortet eller kortene for produksjonsressurs/arbeidssenter definerer standardflyter til og fra produksjonsområder.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-145">The **To-Production Bin Code**, **From-Production Bin Code**, and **Open Shop Floor Bin Code** fields on the location card or the machine/work center cards define default flows to and from production areas.</span></span>  

 <span data-ttu-id="1dbe7-146">Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du se avsnittet Trekke produksjonskomponenter i lageret i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-146">For more information about how component consumption is flushed from the To-Production or Open Shop Floor Bins, see the “Flushing Production Components in the Warehouse” section in this topic.</span></span>  

### <a name="flows-to-and-from-assembly"></a><span data-ttu-id="1dbe7-147">Flyter til og fra montering</span><span class="sxs-lookup"><span data-stu-id="1dbe7-147">Flows to and from Assembly</span></span>  
 <span data-ttu-id="1dbe7-148">Hovedintegrasjonen mellom monteringsordrer og avanserte lageraktiviteter representeres av muligheten til å plukke monteringskomponenter på både **Plukk**-siden og **Plukkforslag**-siden.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-148">The main integration between assembly orders and advanced warehouse activities is represented by the ability to pick assembly components, both with the **Warehouse Pick** page and the **Pick Worksheet** page.</span></span> <span data-ttu-id="1dbe7-149">Denne funksjonaliteten fungerer nøyaktig slik som plukking av komponenter for produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-149">This functionality works just like when picking components for production orders.</span></span>  

 <span data-ttu-id="1dbe7-150">Det finnes ingen bestemt lagerfunksjonalitet for å plassere monteringsvarer, men du kan angi en standard plasseringshylle for hyllekoden i monteringsordrehodet.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-150">While no specific warehouse functionality exists for putting assembly items away, the bin code on the assembly order header may be set to a default put-away bin.</span></span> <span data-ttu-id="1dbe7-151">Bokføring av monteringsordre Funksjoner da som bokføring av en plassering.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-151">Posting the assembly order then functions like posting a put-away.</span></span> <span data-ttu-id="1dbe7-152">Lageraktiviteten som flytter monteringsvarer til lageret, kan håndteres på siden **Flytteforslag** eller siden **Intern plassering** uten noen relasjon til monteringsordren.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-152">The warehouse activity to move assembly items into the warehouse can be managed on the **Movement Worksheet** page or the **Whse. Internal Put-away** page, with no relation to the assembly order.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1dbe7-153">Hvis varer monteres til ordre, vil lagerlevering for den tilknyttede ordren deretter utløse lagerplukk for alle involverte monteringskomponenter, ikke bare for den solgte varen som når du leverer varer på lager.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-153">If items are assembled to order, then the warehouse shipment of the linked sales order triggers a warehouse pick for all the involved assembly components, not just for the sold item as when shipping inventory items.</span></span>  

 <span data-ttu-id="1dbe7-154">Feltene **Til-Hyllekode for montering** og **Fra-Hyllekode for montering** på lokasjonskortet definerer standardflyter til og fra monteringsområder.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-154">The **To-Assembly Bin Code** and **From-Assembly Bin Code** fields on the location card define default flows to and from assembly areas.</span></span>  

### <a name="ad-hoc-movements"></a><span data-ttu-id="1dbe7-155">Adhocflyttinger</span><span class="sxs-lookup"><span data-stu-id="1dbe7-155">Ad-Hoc Movements</span></span>  
 <span data-ttu-id="1dbe7-156">I avansert lagerstyring blir flytting av varer fra hylle til hylle uten relasjon til kildedokumenter, behandlet på siden **Flytteforslag** og registrert på siden Lagerflytting.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-156">In advanced warehousing, the movement of items from bin to bin without relation to source documents is managed on the **Movement Worksheet** page and registered in the Warehouse Movement page.</span></span>  

## <a name="flushing-production-components-in-the-warehouse"></a><span data-ttu-id="1dbe7-157">Trekke produksjonskomponenter i lageret</span><span class="sxs-lookup"><span data-stu-id="1dbe7-157">Flushing Production Components in the Warehouse</span></span>  
 <span data-ttu-id="1dbe7-158">Hvis det er angitt på varekortet, vil komponenter som er plukket med lagerplukk, bli bokført som forbrukte av produksjonsordren når lagerplukket registreres.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-158">If set up on the item card, components picked with warehouse picks are posted as consumed by the production order when the warehouse pick is registered.</span></span> <span data-ttu-id="1dbe7-159">Ved hjelp av trekkmetodene **Plukk + Fremover** og **Plukk + Bakover**, utløser plukkregistreringen den relaterte forbruksbokføringen henholdsvis når den første operasjonen starter, eller når den siste operasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-159">By using the **Pick + Forward** method and the **Pick + Backward** flushing method, the pick registration triggers the related consumption posting when the first operation starts or when the last operation finishes, respectively.</span></span>  

 <span data-ttu-id="1dbe7-160">Tenk deg følgende scenario basert på [!INCLUDE[d365fin](includes/d365fin_md.md)]-demonstrasjonsdatabasen, HVIT lokasjon.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-160">Consider the following scenario based on the [!INCLUDE[d365fin](includes/d365fin_md.md)] demonstration database, WHITE location.</span></span>  

 <span data-ttu-id="1dbe7-161">Det finnes en produksjonsordre for 15 STK av varen LS-100.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-161">A production order for 15 PCS of item LS-100 exists.</span></span> <span data-ttu-id="1dbe7-162">Noen av varene i komponentoversikten må trekkes manuelt i en forbrukskladd, og andre varer i oversikten kan plukkes og trekkes automatisk ved hjelp av trekkmetoden **Plukk + Bakover**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-162">Some of the items on the component list must be flushed manually in a consumption journal, and other items on the list can be picked and flushed automatically using the **Pick + Backward** flushing method.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1dbe7-163">**Plukk + fremover** fungerer bare hvis den andre operasjonen for produksjonsrutelinjen bruker en rutekoblingskode.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-163">**Pick + Forward** only works if the second production routing line operation uses a routing link code.</span></span> <span data-ttu-id="1dbe7-164">Hvis en planlagt produksjonsordre frigis, starter lagertrekk fremover for komponenter som **Plukk + Fremover** er angitt for.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-164">Releasing a planned production order initiates forward flushing of components set to **Pick + Forward**.</span></span> <span data-ttu-id="1dbe7-165">Trekking kan imidlertid ikke finne sted før plukk av komponentene er registrert, noe som igjen bare kan finne sted når ordren frigis.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-165">However, the flushing cannot take place until the pick of the components is registered, which again can only take place when the order is released.</span></span>  

 <span data-ttu-id="1dbe7-166">Fremgangsmåten nedenfor beskriver hva ulike brukere gjør, og det relaterte svaret:</span><span class="sxs-lookup"><span data-stu-id="1dbe7-166">The following steps describe the involved actions by different users and the related response:</span></span>  

1.  <span data-ttu-id="1dbe7-167">Verkstedlederen frigir produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-167">The shop floor supervisor releases the production order.</span></span> <span data-ttu-id="1dbe7-168">Varer med trekkmetoden **Fremover** og ingen rutekoblingskode, trekkes fra den åpne produksjonshylle.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-168">Items with **Forward** flushing method and no routing link code are deducted from the open shop floor bin.</span></span>  
2.  <span data-ttu-id="1dbe7-169">Verkstedlederen velger knappen **Opprett lagerplukk** på produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-169">The shop floor supervisor chooses the **Create Warehouse Pick** button on the production order.</span></span> <span data-ttu-id="1dbe7-170">Et lagerplukkdokumentet opprettet plukking for varer med trekkmetodene **Manuell**, **Plukk + Bakover** og **Plukk + Fremover**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-170">A warehouse pick document is created pick for items with **Manual**, **Pick + Backward**, and **Pick + Forward** flushing methods.</span></span> <span data-ttu-id="1dbe7-171">Disse varene plasseres i hyllen til produksjon.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-171">These items are placed in the To-Production bin.</span></span>  
3.  <span data-ttu-id="1dbe7-172">Lagerlederen tilordner plukkingene til en lagermedarbeider.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-172">The warehouse manager assigns the picks to a warehouse worker.</span></span>  
4.  <span data-ttu-id="1dbe7-173">Lagermedarbeideren plukker varene fra aktuelle hyller og plasserer dem i hyllen til produksjon eller i hyllen som er angitt i plukkingen, som kan være en arbeidssenterhylle eller produksjonsressurshylle.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-173">The warehouse worker picks the items from appropriate bins and places them in the To-Production bin or in the bin specified on the warehouse pick, which may be a work center or machine center bin.</span></span>  
5.  <span data-ttu-id="1dbe7-174">Lagermedarbeideren registrerer plukkingen.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-174">The warehouse worker registers the pick.</span></span> <span data-ttu-id="1dbe7-175">Antallet trekkes fra plukkhyllene og legges til forbrukshyllen.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-175">The quantity is subtracted from the pick bins and added to the consumption bin.</span></span> <span data-ttu-id="1dbe7-176">**Plukket ant.**-feltet oppdateres i komponentoversikten for alle plukkede varer.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-176">The **Qty. Picked** field on the component list for all picked items is updated.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1dbe7-177">Bare antallet som plukkes kan brukes.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-177">Only the quantity that is picked can be consumed.</span></span>  

6.  <span data-ttu-id="1dbe7-178">Maskinoperatøren gir produksjonssjefen beskjed om at sluttvarene er ferdige.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-178">The machine operator informs the production manager that the end items are finished.</span></span>  
7.  <span data-ttu-id="1dbe7-179">Verkstedlederen bruker forbrukskladden eller produksjonskladden til å bokføre forbruk av komponentvarer som bruker enten trekkmetoden **Manuell** eller trekkmetoden **Fremover** eller **Plukk + Fremover** sammen med rutekoblingskoder.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-179">The shop floor supervisor uses the consumption journal or production journal to post the consumption of component items that use either **Manual** flushing method or **Forward** or **Pick + Forward** flushing methods together with routing link codes.</span></span>  
8.  <span data-ttu-id="1dbe7-180">Produksjonssjefen bokfører avgangen til produksjonsordren og endrer statusen til **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-180">The production manager posts the output of the production order and changes status to **Finished**.</span></span> <span data-ttu-id="1dbe7-181">Antallet komponentvarer som bruker trekkmetoden **Bakover**, trekkes fra den åpne produksjonshyllen, og antallet komponentvarer som bruker trekkmetoden **Plukk + Bakover**, trekkes fra hyllen til produksjon.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-181">The quantity of component items that use **Backward** flushing method is deducted from the open shop floor bin, and the quantity of component items that use **Pick + Backward** flushing method is deducted from the To-Production bin.</span></span>  

 <span data-ttu-id="1dbe7-182">Illustrasjonen nedenfor viser når **Hyllekode**-feltet i komponentoversikten fylles i henhold til lokasjonsoppsettet eller oppsettet for produksjonsressurs/arbeidssenter.</span><span class="sxs-lookup"><span data-stu-id="1dbe7-182">The following illustration shows when the **Bin Code** field on the component list is filled according to your location or machine/work center setup.</span></span>  

 <span data-ttu-id="1dbe7-183">![Oversikt over når/hvordan Hyllekode-feltet fylles ut](media/binflow.png "Oversikt over når/hvordan Hyllekode-feltet fylles ut")</span><span class="sxs-lookup"><span data-stu-id="1dbe7-183">![Overview of when/how the Bin Code field is filled in](media/binflow.png "Overview of when/how the Bin Code field is filled in")</span></span>  

## <a name="see-also"></a><span data-ttu-id="1dbe7-184">Se også</span><span class="sxs-lookup"><span data-stu-id="1dbe7-184">See Also</span></span>  
 [<span data-ttu-id="1dbe7-185">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="1dbe7-185">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)