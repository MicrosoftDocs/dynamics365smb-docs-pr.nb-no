---
title: Arbeide med lagerperioder | Microsoft-dokumentasjon
description: Du kan kontrollere tidsrammen som brukere kan bokføre endringer i lageret, ved å definere lagerperioder.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1aae1d32b86000ea8a5f867f1ee4c07d8bc1ff09
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803527"
---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="82bae-103">Arbeide med lagerperioder</span><span class="sxs-lookup"><span data-stu-id="82bae-103">Work with Inventory Periods</span></span>
<span data-ttu-id="82bae-104">Lagerperioder er tidsperioder som du kan bokføre lagerendringer i.</span><span class="sxs-lookup"><span data-stu-id="82bae-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="82bae-105">En lagerperiode defineres av datoen den slutter på, eller sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="82bae-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="82bae-106">En lagerperiode defineres av datoen den slutter på, eller sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="82bae-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="82bae-107">Du kan ikke bokføre eventuelle nye verdier til lageret før sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="82bae-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="82bae-108">Hvis du har åpne vareposter i en lukket periode, det vil si positivt antall som ennå ikke er utlignet mot utgående transaksjoner, kan du fortsatt utligne utgående antall mot disse postene, selv om perioden er lukket.</span><span class="sxs-lookup"><span data-stu-id="82bae-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="82bae-109">De følgende delene handler om hvordan du kan:</span><span class="sxs-lookup"><span data-stu-id="82bae-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="82bae-110">Opprett lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="82bae-110">Create inventory periods.</span></span>  
* <span data-ttu-id="82bae-111">Lukk lagerperioder.</span><span class="sxs-lookup"><span data-stu-id="82bae-111">Close inventory periods.</span></span>  
* <span data-ttu-id="82bae-112">Åpne lagerperioder på nytt.</span><span class="sxs-lookup"><span data-stu-id="82bae-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="82bae-113">Slik oppretter du en lagerperiode</span><span class="sxs-lookup"><span data-stu-id="82bae-113">To create an inventory period</span></span>  
1. <span data-ttu-id="82bae-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="82bae-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="82bae-115">Opprett en ny linje.</span><span class="sxs-lookup"><span data-stu-id="82bae-115">Create a new line.</span></span>  
3. <span data-ttu-id="82bae-116">Angi den siste datoen i lagerperioden du vil definere, i **Sluttdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="82bae-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="82bae-117">Når perioden er lukket, kan du ikke bokføre lagerendringer før denne datoen.</span><span class="sxs-lookup"><span data-stu-id="82bae-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="82bae-118">Skriv inn et beskrivende navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="82bae-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="82bae-119">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="82bae-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="82bae-120">Lukke lagerperioder</span><span class="sxs-lookup"><span data-stu-id="82bae-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="82bae-121">**Lukket**-feltet angir om lagerperioden er lukket eller ikke for lagerverdiendringer.</span><span class="sxs-lookup"><span data-stu-id="82bae-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="82bae-122">Du kan ikke redigere dette feltet.</span><span class="sxs-lookup"><span data-stu-id="82bae-122">You cannot edit this field.</span></span>  

<span data-ttu-id="82bae-123">Du kan lukke en hvilken som helst lagerperiode gitt at følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="82bae-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="82bae-124">Det er ingen utgående vareposter, det vil si negativ beholdning, i perioden.</span><span class="sxs-lookup"><span data-stu-id="82bae-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="82bae-125">Kostbeløpet for alle varer er justert ved hjelp av kjørselen **Juster kostverdi - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="82bae-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="82bae-126">Dette betyr at alle utgående transaksjonsantall, for eksempel de fra ordrer, utgående overføringer, salgsfakturaer, bestillingsreturer eller kjøpskreditnotaer, må utlignes mot eksisterende antall på lageret.</span><span class="sxs-lookup"><span data-stu-id="82bae-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="82bae-127">Slik lukker du en lagerperiode:</span><span class="sxs-lookup"><span data-stu-id="82bae-127">To close an inventory period</span></span>  
1. <span data-ttu-id="82bae-128">Før du lukker en lagerperiode, kjører du den satsvise jobben **Juster kostverdi – vareposter** for å sikre at alle kostjusteringer er bokført.</span><span class="sxs-lookup"><span data-stu-id="82bae-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="82bae-129">I fanebladet **Handlinger**, under **Funksjoner** velger du **Juster kostverdi - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="82bae-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="82bae-130">Kjør rapporten **Lukk lagerperiode - test** for å fastslå om det er noen åpne utgående vareposter i lagerperioden eller varer som kost ikke er justert for ennå.</span><span class="sxs-lookup"><span data-stu-id="82bae-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="82bae-131">Velg **Lukk lagerperiode - test**.</span><span class="sxs-lookup"><span data-stu-id="82bae-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="82bae-132">Kjør kjørselen **Bokfør lagerkost i Finans** for å sikre at all kost bokføres i Finans.</span><span class="sxs-lookup"><span data-stu-id="82bae-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="82bae-133">Velg handlingen **Bokfør lager i Finans**.</span><span class="sxs-lookup"><span data-stu-id="82bae-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="82bae-134">På siden **Lagerperioder** velger du lagerperioden du vil lukke.</span><span class="sxs-lookup"><span data-stu-id="82bae-134">On the **Inventory Periods** page, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="82bae-135">Velg **Lukk periode**.</span><span class="sxs-lookup"><span data-stu-id="82bae-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="82bae-136">Når lagerperioden er lukket, kan du ikke bokføre lagerendringer før sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="82bae-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="82bae-137">Du må justere kostbeløpet for alle varer med kjørselen **Juster kostverdi - vareposter** før du lukker lagerperioden.</span><span class="sxs-lookup"><span data-stu-id="82bae-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="82bae-138">Velg **Ja** for å bekrefte at du vil lukke perioden, eller velg **Nei** hvis du ikke vil lukke den.</span><span class="sxs-lookup"><span data-stu-id="82bae-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="82bae-139">Lagerperioden lukkes og en bekreftelsesmelding vises når prosessen er ferdig.</span><span class="sxs-lookup"><span data-stu-id="82bae-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="82bae-140">Åpne lagerperioder på nytt</span><span class="sxs-lookup"><span data-stu-id="82bae-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="82bae-141">Når du har lukket lagerperioden, kan du ikke slette den.</span><span class="sxs-lookup"><span data-stu-id="82bae-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="82bae-142">Du kan imidlertid åpne den på nytt hvis du vil tillate bokføring før sluttdatoen i lagerperioden.</span><span class="sxs-lookup"><span data-stu-id="82bae-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="82bae-143">Hvis du åpner en periode på nytt, åpnes også alle lagerperioder med sluttdatoer som er senere enn perioden du åpner på nytt.</span><span class="sxs-lookup"><span data-stu-id="82bae-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="82bae-144">Åpne en lagerperiode på nytt</span><span class="sxs-lookup"><span data-stu-id="82bae-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="82bae-145">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="82bae-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="82bae-146">Velg lagerperioden du vil åpne på nytt.</span><span class="sxs-lookup"><span data-stu-id="82bae-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="82bae-147">Velg **Åpne periode på nytt**.</span><span class="sxs-lookup"><span data-stu-id="82bae-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="82bae-148">Bekreft at du vil åpne perioden på nytt.</span><span class="sxs-lookup"><span data-stu-id="82bae-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="82bae-149">Alle lagerperioder med sluttdatoer som er senere enn perioden du valgte, åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="82bae-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82bae-150">Se også</span><span class="sxs-lookup"><span data-stu-id="82bae-150">See Also</span></span>  
[<span data-ttu-id="82bae-151">Designdetaljer: Beholdningsperioder</span><span class="sxs-lookup"><span data-stu-id="82bae-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="82bae-152">Finans</span><span class="sxs-lookup"><span data-stu-id="82bae-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="82bae-153">Lager</span><span class="sxs-lookup"><span data-stu-id="82bae-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="82bae-154">Arbeide med Financials</span><span class="sxs-lookup"><span data-stu-id="82bae-154">Working with Financials</span></span>](ui-work-product.md)