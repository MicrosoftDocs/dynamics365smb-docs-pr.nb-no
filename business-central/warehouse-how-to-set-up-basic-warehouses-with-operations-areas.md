---
title: Opprette grunnleggende lagre med operasjonsområder | Microsoft-dokumentasjon
description: 'Hvis det finnes interne operasjonsområder, for eksempel produksjon eller montering, i enkle lageroppsett der lokasjoner bruker oppsettsfeltet **Hylle obligatorisk** og muligens oppsettsfeltene **Plukk nødv.** og **Plassering nødv.**, kan du bruke tre grunnleggende lagerdokumenter til å registrere lageraktivitetene for interne operasjonsområder:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: f11719cc9488adf84bca8cd5a23d28caaa75f4bf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803444"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a><span data-ttu-id="acdd6-103">Opprette grunnleggende lagre med operasjonsområder</span><span class="sxs-lookup"><span data-stu-id="acdd6-103">Set Up Basic Warehouses with Operations Areas</span></span>
<span data-ttu-id="acdd6-104">Hvis det finnes interne operasjonsområder, for eksempel produksjon eller montering, i enkle lageroppsett der lokasjoner bruker oppsettsfeltet **Hylle obligatorisk** og muligens oppsettsfeltene **Plukk nødv.** og **Plassering nødv.**, kan du bruke følgende grunnleggende lagerdokumenter til å registrere lageraktivitetene for interne operasjonsområder:</span><span class="sxs-lookup"><span data-stu-id="acdd6-104">If internal operation areas such as production or assembly exist in basic warehouse configurations where locations use the **Bin Mandatory** setup field and possibly the **Require Pick** and **Require Put-away** setup fields, then you can use the following basic warehouse documents to record your warehouse activities for internal operation areas:</span></span>  

- <span data-ttu-id="acdd6-105">**Lagerflyttingsliste**-siden.</span><span class="sxs-lookup"><span data-stu-id="acdd6-105">**Inventory Movement** page.</span></span>  
- <span data-ttu-id="acdd6-106">**Lagreplukk**-siden.</span><span class="sxs-lookup"><span data-stu-id="acdd6-106">**Inventory Pick** page.</span></span>  
- <span data-ttu-id="acdd6-107">**Lagerplassering**-siden.</span><span class="sxs-lookup"><span data-stu-id="acdd6-107">**Inventory Put-away** page.</span></span>

> [!NOTE]
> <span data-ttu-id="acdd6-108">Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter for firma på lokasjoner der du velger disse avmerkingsboksene.</span><span class="sxs-lookup"><span data-stu-id="acdd6-108">Even though the settings are called **Require Pick** and **Require Put-away**, you can still post receipts and shipments directly from the source business documents at locations where you select these check boxes.</span></span>  

<span data-ttu-id="acdd6-109">Hvis du vil bruke disse sidene med interne operasjoner, for eksempel plukke og flytte komponenter til produksjon, må du følge noen av eller alle følgende konfigurasjonstrinn, avhengig av hvor mye kontroll du trenger:</span><span class="sxs-lookup"><span data-stu-id="acdd6-109">To use these pages with internal operations, such as to pick and move components to production, you must make some or all the following setup steps depending on how much control you need:</span></span>  

- <span data-ttu-id="acdd6-110">Aktiver dokumenter for lagerplukk, lagerflytting og lagerplassering.</span><span class="sxs-lookup"><span data-stu-id="acdd6-110">Enable the inventory pick, move, and put-away documents.</span></span>  
- <span data-ttu-id="acdd6-111">Definer standard hyllestrukturer for komponenter og sluttvarer som går til og fra operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="acdd6-111">Define default bin structures for components and end items flowing to and from operation resources.</span></span>  
- <span data-ttu-id="acdd6-112">Opprett til- og fra-hyller som er dedikert til en bestemte operasjonsressurser for å hindre at varene blir plukket for utgående dokumenter.</span><span class="sxs-lookup"><span data-stu-id="acdd6-112">Make to- and from- bins that are dedicated to specific operation resources to prevent the items from being picked for outbound documents.</span></span>

<span data-ttu-id="acdd6-113">Hyllekoder som er definert på lokasjonskort, definerer en standard lagerflyt for bestemte aktiviteter, for eksempel komponenter i en monteringsavdeling.</span><span class="sxs-lookup"><span data-stu-id="acdd6-113">Bin codes that are set up on location cards define a default warehouse flow for certain activities, such as components in an assembly department.</span></span> <span data-ttu-id="acdd6-114">Det finnes flere funksjoner for å sørge for at når varer blir plassert i en bestemt hylle, kan de ikke flyttes eller plukkes til andre aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="acdd6-114">Additional functionality exists to make sure that when items are placed in a certain bin, they cannot be moved or picked to other activities.</span></span> <span data-ttu-id="acdd6-115">Hvis du vil ha mer informasjon, kan du se [Slik oppretter du dedikerte komponenthyller](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).</span><span class="sxs-lookup"><span data-stu-id="acdd6-115">For more information, see [To create dedicated component bins](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).</span></span>

<span data-ttu-id="acdd6-116">Fremgangsmåtene nedenfor er basert på definisjon av grunnleggende lageraktiviteter rundt et produksjonsområde.</span><span class="sxs-lookup"><span data-stu-id="acdd6-116">The following procedures are based on setting up basic warehouse activities around a production area.</span></span> <span data-ttu-id="acdd6-117">Trinnene er de samme for andre operasjonsområder, for eksempel montering, service og jobber.</span><span class="sxs-lookup"><span data-stu-id="acdd6-117">The steps are similar for other operation areas, such as assembly, service management, and jobs.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="acdd6-118">I den følgende fremgangsmåten velges oppsettsfeltet **Hylle obligatorisk** som en nødvendig forutsetning fordi det regnes som grunnlaget for ethvert nivå av lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="acdd6-118">In the following procedure, the **Bin Mandatory** setup field on location cards is selected as a precondition because that is considered the foundation for any level of warehouse management.</span></span>  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a><span data-ttu-id="acdd6-119">Slik aktiverer du lagerdokumenter for interne operasjonsaktiviteter:</span><span class="sxs-lookup"><span data-stu-id="acdd6-119">To enable inventory documents for internal operation activities</span></span>  
1.  <span data-ttu-id="acdd6-120">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-121">Åpne lokasjonskortet du vil definere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-121">Open the location card you want to set up.</span></span>  
3.  <span data-ttu-id="acdd6-122">På hurtigfanen **Lager**, merker du av for **Plassering nødv.** for å indikere at når et inngående eller internt kildedokument med hyllekode frigis, kan en lagerplassering eller et lagerflyttingsdokument opprettes.</span><span class="sxs-lookup"><span data-stu-id="acdd6-122">On the **Warehouse** FastTab, select the **Require Put-away** check box to indicate that, when an inbound or internal source document with a bin code is released, an inventory put-away or an inventory movement document can be created.</span></span>  
4.  <span data-ttu-id="acdd6-123">Merk av for **Plukk nødv.** for å indikere at når det opprettes utgående eller internt kildedokument med hyllekode, må det opprettes et lagerplukk- eller en lagerflyttingsdokument.</span><span class="sxs-lookup"><span data-stu-id="acdd6-123">Select the **Require Pick** check box to indicate that when an outbound or internal source document with a bin code is created, an inventory pick or an inventory movement document must be created.</span></span>  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a><span data-ttu-id="acdd6-124">Slik definerer du en standardhyllestruktur i produksjonsområdet:</span><span class="sxs-lookup"><span data-stu-id="acdd6-124">To define a default bin structure in the production area</span></span>  
1.  <span data-ttu-id="acdd6-125">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-126">Åpne lokasjonen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-126">Open the Location you want to set up.</span></span>  
3.  <span data-ttu-id="acdd6-127">På hurtigfanen **Hyller**, i feltet **Åpen prod.hyllekode** angir du koden for hyllen i produksjonsområdet som har rikelig med komponenter maskinoperatøren kan forbruke fra uten å be om en lageraktivitet for å bringe dem til hyllen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-127">On the **Bins** FastTab, in the **Open Shop Floor Bin Code** field, enter the code of the bin in the production area with plenty of components that the machine operator can consume from without requesting a warehouse activity to bring them to the bin.</span></span> <span data-ttu-id="acdd6-128">Varer som er plassert i denne hyllen er vanligvis konfigurert for automatisk bokføring eller trekk.</span><span class="sxs-lookup"><span data-stu-id="acdd6-128">Items that are placed in this bin are typically set up for automatic posting, or flushing.</span></span> <span data-ttu-id="acdd6-129">Dette betyr at **Trekkmetode**-feltet inneholder **Fremover** eller **Bakover**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-129">This means that the **Flushing Method** field contains **Forward** or **Backward**.</span></span>  
4. <span data-ttu-id="acdd6-130">Angi koden for hyllen i feltet **Til-Hyllekode for produksjon** i produksjonsområdet der komponentene som plukkes til produksjonen på denne lokasjonen, plasseres som standard før de kan brukes.</span><span class="sxs-lookup"><span data-stu-id="acdd6-130">In the **To-Production Bin Code** field, enter the code of the bin in the production area where components that are picked for production at this location are placed by default before they can be consumed.</span></span> <span data-ttu-id="acdd6-131">Varer som er plassert i denne hyllen er vanligvis konfigurert for manuell forbruksbokføring.</span><span class="sxs-lookup"><span data-stu-id="acdd6-131">Items that are placed in this bin are typically set up for manual consumption posting.</span></span> <span data-ttu-id="acdd6-132">Dette betyr at **Trekkmetode**-feltet inneholder **Manuell** eller **Plukk + Fremover** eller **Plukk + Bakover** for lagerplukkinger og lagerflyttinger.</span><span class="sxs-lookup"><span data-stu-id="acdd6-132">This means that the **Flushing Method** field contains **Manual** or **Pick + Forward** or **Pick + Backward** for warehouse picks and inventory movements.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="acdd6-133">Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje hvilken *Hent*-hylle komponentene reduseres fra ved bokføring av forbruk.</span><span class="sxs-lookup"><span data-stu-id="acdd6-133">When you use inventory picks, the **Bin Code** field on a production order component line defines the *take* bin from where components are decreased when posting consumption.</span></span> <span data-ttu-id="acdd6-134">Når du bruker lagerflyttinger, definerer **Hyllekode**-feltet på produksjonsordrekomponentlinjer *Plasser*-hyllen i operasjonsområdet der lagermedarbeideren må plassere komponentene.</span><span class="sxs-lookup"><span data-stu-id="acdd6-134">When you use inventory movements, the **Bin Code** field on production order component lines defines the *place* bin in the operation area where the warehouse worker must place the components.</span></span>  

5. <span data-ttu-id="acdd6-135">På hurtigfanen **Hyller**, i feltet **Fra-Hyllekode for produksjon** angir du koden for hyllen i produksjonsområdet hvor ferdige varer hentes fra som standard når prosessen omfatter en lageraktivitet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-135">On the **Bins** FastTab, in the **From-Production Bin Code** field, enter the code of the bin in the production area where finished end items are taken from by default when the process involves a warehouse activity.</span></span> <span data-ttu-id="acdd6-136">I grunnleggende lageroppsett registreres aktiviteten som en lagerplassering eller lagerflytting.</span><span class="sxs-lookup"><span data-stu-id="acdd6-136">In basic warehouse configurations, the activity is recorded as an inventory put-away or an inventory movement.</span></span>  

<span data-ttu-id="acdd6-137">Nå krever produksjonsordrekomponentlinjer med standard hyllekode at komponenter som trekkes fremover plasseres her.</span><span class="sxs-lookup"><span data-stu-id="acdd6-137">Now, production order component lines with the default bin code require that forward-flushed components are placed there.</span></span> <span data-ttu-id="acdd6-138">Før komponentene forbrukes fra denne hyllen, kan imidlertid andre komponentbehov plukke eller forbruke fra denne hyllen fordi den fortsatt regnes som tilgjengelig hylleinnhold.</span><span class="sxs-lookup"><span data-stu-id="acdd6-138">However, until the components are consumed from that bin, other component demands may pick or consume from that bin because they are still considered available bin contents.</span></span> <span data-ttu-id="acdd6-139">For å sørge for at hylleinnholdet bare er tilgjengelig for komponentbehov som bruker denne hyllen til produksjon, må du velge feltet **Dedikert** på linjen for denne hyllekoden på siden **Hyller** som du åpner fra lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-139">To make sure that bin content is only available to component demand that uses that to-production bin, you must select the **Dedicated** field on the line for that bin code on the **Bins** page that you open from the location card.</span></span>

<span data-ttu-id="acdd6-140">Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til oppsettet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-140">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your setup.</span></span>  

<span data-ttu-id="acdd6-141">![Flytskjema for hylle](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="acdd6-141">![Bin flow chart](media/binflow.png "BinFlow")</span></span>    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a><span data-ttu-id="acdd6-142">Slik definerer du en standardhyllestruktur i monteringsområdet:</span><span class="sxs-lookup"><span data-stu-id="acdd6-142">To define a default bin structure in the assembly area</span></span>
<span data-ttu-id="acdd6-143">Komponenter for monteringsordrer kan ikke plukkes eller bokføres med lagerplukk.</span><span class="sxs-lookup"><span data-stu-id="acdd6-143">Components for assembly orders cannot be picked or posted with inventory picks.</span></span> <span data-ttu-id="acdd6-144">Bruk i stedet siden **Lagerflytting**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-144">Instead, use the **Inventory Movement** page.</span></span> <span data-ttu-id="acdd6-145">Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="acdd6-145">For more information, see [Move Components to an Operation Area in Basic Warehousing](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>

<span data-ttu-id="acdd6-146">Når du plukker og leverer salgslinjeantall som er montert til ordre, må du følge visse regler når du oppretter lagerplukklinjene.</span><span class="sxs-lookup"><span data-stu-id="acdd6-146">When picking and shipping sales line quantities that are assembled to the order, you must follow certain rules when creating the inventory pick lines.</span></span> <span data-ttu-id="acdd6-147">Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="acdd6-147">For more information, see the “Handling Assemble-to-Order Items in Inventory Picks” section in [Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>

<span data-ttu-id="acdd6-148">Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="acdd6-148">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a><span data-ttu-id="acdd6-149">Slik konfigurerer du at en lagerflytting opprettes automatisk når lagerplukkingen for monteringsvaren opprettes</span><span class="sxs-lookup"><span data-stu-id="acdd6-149">To set up that an inventory movement is automatically created when the inventory pick for the assembly item is created</span></span>
1. <span data-ttu-id="acdd6-150">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Monteringsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-150">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assembly Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-151">Merk av for **Opprett flyttinger automatisk**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-151">Select the **Create Movements Automatically** check box.</span></span>

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a><span data-ttu-id="acdd6-152">Slik definerer du hyllen i monteringsområdet der komponenter plasseres som standard, før de kan brukes i monteringen:</span><span class="sxs-lookup"><span data-stu-id="acdd6-152">To set up the bin in the assembly area where components are placed by default before they can be consumed in assembly</span></span>
<span data-ttu-id="acdd6-153">Verdien i dette feltet settes automatisk inn i **Hyllekode**-feltet på monteringsordrelinjer når denne lokasjonen angis i **Lokasjonskode**-feltet på monteringsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-153">The value in this field is automatically inserted in the **Bin Code** field on assembly order lines when this location is entered in the **Location Code** field on the assembly order line.</span></span>

1. <span data-ttu-id="acdd6-154">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-155">Åpne lokasjonen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-155">Open the Location you want to set up.</span></span>
3. <span data-ttu-id="acdd6-156">Fyll ut feltet **Til-Hyllekode for montering**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-156">Fill in the **To-Assembly Bin Code** field.</span></span>

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a><span data-ttu-id="acdd6-157">Slik definerer du hvilken hylle i monteringsområdet ferdige monteringsvarer bokføres til når de monteres til lager:</span><span class="sxs-lookup"><span data-stu-id="acdd6-157">To set up the bin in the assembly area where finished assembly items are posted to when they are assembled to stock</span></span>
<span data-ttu-id="acdd6-158">Verdien i dette feltet settes automatisk inn i **Hyllekode**-feltet på monteringsordrehoder når denne lokasjonskoden fylles ut i **Lokasjonskode**-feltet på monteringsordrehodet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-158">The value in this field is automatically inserted in the **Bin Code** field on assembly order headers when this location code is filled into the **Location Code** field on the assembly order header.</span></span>

<span data-ttu-id="acdd6-159">Hyllekoder som er definert på lokasjonskort, definerer en standard lagerflyt for spesifikke lageraktiviteter, for eksempel forbruk av komponenter i et monteringsområde.</span><span class="sxs-lookup"><span data-stu-id="acdd6-159">Bin codes that are set up on location cards define a default warehouse flow for specific warehouse activities, such as consumption of components in an assembly area.</span></span> <span data-ttu-id="acdd6-160">Det finnes flere funksjoner for å sørge for at når varer blir plassert i en standardhylle, kan de ikke flyttes eller plukkes til andre aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="acdd6-160">Additional functionality exists to make sure that when items are placed in a default bin, they cannot be moved or picked to other activities.</span></span>

> [!NOTE]
> <span data-ttu-id="acdd6-161">Dette oppsettet er bare mulig for lokasjoner der Hylle obligatorisk-feltet er valgt.</span><span class="sxs-lookup"><span data-stu-id="acdd6-161">This setup is only possible for locations where the Bin Mandatory field is selected.</span></span>

1. <span data-ttu-id="acdd6-162">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-162">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-163">Åpne lokasjonen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-163">Open the Location you want to set up.</span></span>
3. <span data-ttu-id="acdd6-164">Fyll ut feltet **Fra-Hyllekode for montering**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-164">Fill in the **From-Assembly Bin Code** field.</span></span>

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a><span data-ttu-id="acdd6-165">Slik definerer du hvilken hylle ferdige monteringsvarer bokføres til, når de monteres til en tilknyttet ordre:</span><span class="sxs-lookup"><span data-stu-id="acdd6-165">To set up the bin where finished assembly items are posted to when they are assembled to a linked sales order</span></span>
<span data-ttu-id="acdd6-166">Fra denne hyllen sendes monteringsvarene øyeblikkelig, via en lagerplukking, for å innfri ordren.</span><span class="sxs-lookup"><span data-stu-id="acdd6-166">From this bin, the assembly items are shipped immediately, via an inventory pick, to fulfill the sales order.</span></span>

> [!NOTE]
> <span data-ttu-id="acdd6-167">Dette feltet kan ikke brukes hvis lokasjonen er definert til å bruke lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="acdd6-167">This field cannot be used if the location is set up to use directed pick and put-away.</span></span>

<span data-ttu-id="acdd6-168">Hyllekoden kopieres fra ordrelinjen til monteringsordrehodet for å kommunisere til monteringsarbeiderne hvor de skal plassere det ferdige resultatet for å klargjøre det for levering.</span><span class="sxs-lookup"><span data-stu-id="acdd6-168">The bin code is copied from the sales order line to the assembly order header to communicate to assembly workers where to place the output to ready it for shipping.</span></span> <span data-ttu-id="acdd6-169">Det er også kopiert til lagerplukklinjen for å kommunisere til lagerarbeiderne hvor varene som skal leveres skal hentes fra.</span><span class="sxs-lookup"><span data-stu-id="acdd6-169">It is also copied to the inventory pick line to communicate to warehouse workers where to take it from to ship it.</span></span>

> [!NOTE]
> <span data-ttu-id="acdd6-170">Leveringshyllen for montering til ordre er alltid er tom.</span><span class="sxs-lookup"><span data-stu-id="acdd6-170">The Assemble-to-Order Shipment bin is always empty.</span></span> <span data-ttu-id="acdd6-171">Når du bokfører en montere-til-ordre-salgslinje, justeres først hylleinnholdet positivt i forhold til monteringsavgangen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-171">When you post an assemble-to-order sales line, then the bin content is first positively adjusted with the assembly output.</span></span> <span data-ttu-id="acdd6-172">Like etter justeres det negativt med det leverte antallet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-172">Immediately after, it is negatively adjusted with the shipped quantity.</span></span>

<span data-ttu-id="acdd6-173">Verdien i dette feltet settes automatisk inn i Hyllekode-feltet på ordrelinjer som inneholder et antall i feltet **Ant. som skal monteres til ordre**, eller hvis varen som skal selges, har **Monter til ordre** i **Etterfyllingssystem**-feltet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-173">The value in this field is automatically inserted in the Bin Code field on sales order lines that contain a quantity in the **Qty. to Assemble to Order** field or if the item to be sold has **Assemble-to-Order** in the **Replenishment System** field.</span></span>

<span data-ttu-id="acdd6-174">Hvis feltet **Hyllek. lev. fra m. til ordre** er tomt, brukes **Fra-Hyllekode for montering**-feltet i stedet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-174">If the **Asm.-to-Order Shpt. Bin Code** is blank, then the **From-Assembly Bin Code** field is used instead.</span></span> <span data-ttu-id="acdd6-175">Hvis begge oppsettsfeltene er tomme, brukes den siste brukte hyllen med innhold i **Hyllekode**-feltet på ordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="acdd6-175">If both setup fields are blank, then the last used bin with content is used in the **Bin Code** field on sales order lines.</span></span>

<span data-ttu-id="acdd6-176">Den samme hyllekoden kopieres så til **Hyllekode**-feltet på lagerplukklinjen som håndterer leveringen av montere-til-ordre-antallet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-176">The same bin code is in turn copied to the **Bin Code** field on the inventory pick line that manages the shipment of the assemble-to-order quantity.</span></span> <span data-ttu-id="acdd6-177">Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="acdd6-177">For more information, see the “Handling Assemble-to-Order Items in Inventory Picks” section in [Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>

1. <span data-ttu-id="acdd6-178">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-178">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="acdd6-179">Åpne lokasjonen du vil definere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-179">Open the Location you want to set up.</span></span>
3. <span data-ttu-id="acdd6-180">Fyll ut feltet **Hyllek. lev. fra m. til ordre**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-180">Fill in the **Asm.-to-Order Shpt. Bin Code** field.</span></span>

## <a name="to-create-dedicated-component-bins"></a><span data-ttu-id="acdd6-181">Slik oppretter du dedikerte komponenthyller:</span><span class="sxs-lookup"><span data-stu-id="acdd6-181">To create dedicated component bins</span></span>
<span data-ttu-id="acdd6-182">Du kan angi at antall i en hylle beskyttes mot å bli plukket for andre behov enn behov fra deres gjeldende formål.</span><span class="sxs-lookup"><span data-stu-id="acdd6-182">You can specify that quantities in a bin are protected from being picked for other demands than demand from their current purpose.</span></span>

<span data-ttu-id="acdd6-183">Antall i dedikerte hyller kan fremdeles reserveres.</span><span class="sxs-lookup"><span data-stu-id="acdd6-183">Quantities in dedicated bins can still be reserved.</span></span> <span data-ttu-id="acdd6-184">Antallene i dedikerte hyller er på samme måte inkludert i feltet **Totalt disp. antall** på siden **Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-184">Accordingly, the quantities in dedicated bins are included in the **Total Available Quantity** field on the **Reservation** page.</span></span>

<span data-ttu-id="acdd6-185">Et arbeidssenter er for eksempel definert med en hyllekode i feltet **Til-Hyllekode for produksjon**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-185">For example, is a work center is set up with a bin code in the **To-Production Bin Code** field.</span></span> <span data-ttu-id="acdd6-186">Produksjonsordrekomponentlinjer med den hyllekoden krever at komponenter som trekkes fremover plasseres der.</span><span class="sxs-lookup"><span data-stu-id="acdd6-186">Production order component lines with that bin code require that forward-flushed components are placed there.</span></span> <span data-ttu-id="acdd6-187">Før komponentene forbrukes fra denne hyllen, kan imidlertid andre komponentbehov plukke eller forbruke fra denne hyllen fordi den fortsatt regnes som tilgjengelig hylleinnhold.</span><span class="sxs-lookup"><span data-stu-id="acdd6-187">However, until the components are consumed from that bin, other component demands may pick or consume from that bin because they are still considered available bin contents.</span></span> <span data-ttu-id="acdd6-188">For å sørge for at hylleinnholdet bare er tilgjengelig for komponentbehov som bruker denne hyllen til produksjon, må du velge feltet **Dedikert** på linjen for denne hyllekoden på siden **Hyller** som du åpner fra lokasjonskortet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-188">To make sure that bin content is only available to component demand that uses that to-production bin, you must select the **Dedicated** field on the line for that bin code on the **Bins** page that you open from the location card.</span></span>

<span data-ttu-id="acdd6-189">Dedikering av hyller gir lignende funksjonalitet som bruk av hylletyper, som bare er tilgjengelig i avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="acdd6-189">Making a bin dedicated provides similar functionality to using bin types, which is only available in advanced warehousing.</span></span> <span data-ttu-id="acdd6-190">Hvis du vil ha mer informasjon, kan du se [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="acdd6-190">For more information, see [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>

> [!Caution]
> <span data-ttu-id="acdd6-191">Varer i dedikerte hyller er ikke beskyttet når de blir plukket og forbrukt som produksjonskomponenter med siden Lagerplukk.</span><span class="sxs-lookup"><span data-stu-id="acdd6-191">Items in dedicated bins are not protected when they are picked and consumed as production components with the Inventory Pick page.</span></span>

1.  <span data-ttu-id="acdd6-192">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-192">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span> <span data-ttu-id="acdd6-193">Velg lokasjonskortet som du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="acdd6-193">Select the location that you want to update.</span></span>  
2.  <span data-ttu-id="acdd6-194">Velg handlingen **Hyller**.</span><span class="sxs-lookup"><span data-stu-id="acdd6-194">Choose the **Bins** action.</span></span>  
3.  <span data-ttu-id="acdd6-195">Velg feltet **Dedikert** for hver hylle du vil bruke utelukkende til bestemte interne operasjoner, og hvor du vil at antallene som er plassert der skal være reservert for den interne operasjonen.</span><span class="sxs-lookup"><span data-stu-id="acdd6-195">Select the **Dedicated** field for each bin that you want to use exclusively for certain internal operations and where you want quantities to be reserved for that internal operation once placed there.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="acdd6-196">Hyllen må være tom før du kan velge eller fjerne den **Dedikert**-feltet.</span><span class="sxs-lookup"><span data-stu-id="acdd6-196">The bin must be empty before you can select or clear the **Dedicated** field.</span></span>

## <a name="see-also"></a><span data-ttu-id="acdd6-197">Se også</span><span class="sxs-lookup"><span data-stu-id="acdd6-197">See Also</span></span>  
[<span data-ttu-id="acdd6-198">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="acdd6-198">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="acdd6-199">Lager</span><span class="sxs-lookup"><span data-stu-id="acdd6-199">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="acdd6-200">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="acdd6-200">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="acdd6-201">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="acdd6-201">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="acdd6-202">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="acdd6-202">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="acdd6-203">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="acdd6-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  