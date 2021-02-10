---
title: Definere produksjonskalendere | Microsoft-dokumentasjon
description: En arbeidssenterkalender angir virkedager og arbeidstider, skift, ferie og fravær som utgjør arbeidssenterets disponible kapasitet, målt i tid, i henhold til senterets definerte effektivitets- og kapasitetsverdier. Opprettelse og aktivering av en arbeidssenterkalender omfatter flere forhåndsoppgaver.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 127ae5af7533c4a6b8b77f2ed88fe90e4453966e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759320"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="a6d80-104">Definere produksjonskalendere</span><span class="sxs-lookup"><span data-stu-id="a6d80-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="a6d80-105">En arbeidssenter- eller maskinkalender angir virkedager/arbeidstider, skift, ferie og fravær som utgjør senterets disponible kapasitet (målt i tid) i henhold til senterets definerte effektivitets- og kapasitetsverdier.</span><span class="sxs-lookup"><span data-stu-id="a6d80-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="a6d80-106">Som grunnlag for beregning av en bestemt arbeidssenter- eller produksjonsressurskalender må du først definere en eller flere generelle produksjonskalendere.</span><span class="sxs-lookup"><span data-stu-id="a6d80-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="a6d80-107">En produksjonskalender definerer en standard arbeidsuke i henhold til starten og slutten på arbeidsdagen samt skiftarbeid.</span><span class="sxs-lookup"><span data-stu-id="a6d80-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="a6d80-108">I tillegg definerer produksjonskalenderen faste feriedager i løpet av året.</span><span class="sxs-lookup"><span data-stu-id="a6d80-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="a6d80-109">I det følgende beskrives hvordan du arbeidssenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="a6d80-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="a6d80-110">Trinnene ligner når du definerer produksjonsressurskalendere.</span><span class="sxs-lookup"><span data-stu-id="a6d80-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="a6d80-111">Slik oppretter du arbeidsskift</span><span class="sxs-lookup"><span data-stu-id="a6d80-111">To create work shifts</span></span>  
1.  <span data-ttu-id="a6d80-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6d80-113">På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere arbeidsskiftet, for eksempel **1**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="a6d80-114">Beskriv arbeidsskiftet i **Beskrivelse**-feltet, for eksempel **1. skift**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="a6d80-115">Fyll eventuelt ut linjer for et andre eller tredje arbeidsskift.</span><span class="sxs-lookup"><span data-stu-id="a6d80-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="a6d80-116">Selv om arbeidssentrene ikke fungerer for andre arbeidsskift, angir du minst én arbeidsskiftkode.</span><span class="sxs-lookup"><span data-stu-id="a6d80-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="a6d80-117">Slik definerer du en produksjonskalender</span><span class="sxs-lookup"><span data-stu-id="a6d80-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="a6d80-118">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonskalendere**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a6d80-119">På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere produksjonskalenderen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="a6d80-120">Beskriv produksjonskalenderen i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a6d80-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="a6d80-121">Velg **Virkedager**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="a6d80-122">På siden **Prod.kalender - virkedager** definerer du en fullstendig arbeidsuke med start- og sluttidspunkt for hver enkelt dag.</span><span class="sxs-lookup"><span data-stu-id="a6d80-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="a6d80-123">Velg et av skiftene du har definert tidligere, i feltet **Arbeidsskiftkode**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="a6d80-124">Legg til en linje for hver arbeidsdag og hvert skift.</span><span class="sxs-lookup"><span data-stu-id="a6d80-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="a6d80-125">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="a6d80-125">For example:</span></span>  

    <span data-ttu-id="a6d80-126">Mandag  07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="a6d80-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="a6d80-127">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="a6d80-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="a6d80-128">Hvis du trenger en produksjonskalender med to arbeidsskift, må du fylle den ut slik:</span><span class="sxs-lookup"><span data-stu-id="a6d80-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="a6d80-129">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="a6d80-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="a6d80-130">Mandag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="a6d80-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="a6d80-131">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="a6d80-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="a6d80-132">Tirsdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="a6d80-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="a6d80-133">Ukedager du ikke definerer i produksjonskalenderen, for eksempel lørdag og søndag, anses ganske enkelt som fridager og har ingen verdi for disponibel kapasitet i en arbeidssenterkalender.</span><span class="sxs-lookup"><span data-stu-id="a6d80-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="a6d80-134">Når alle virkedager i en uke er definert, kan du lukke siden **Prod.kalender - virkedager** og fortsette med å registrere ferie.</span><span class="sxs-lookup"><span data-stu-id="a6d80-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="a6d80-135">På siden **Produksjonskalendere** velger du produksjonskalenderen og velger deretter **Ferie**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="a6d80-136">På siden **Prod.kalender - ferie** definerer du årets ferier ved å angi startdato/-klokkeslett, sluttidspunkt og beskrivelse av hver ferie på egne linjer, for eksempel på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="a6d80-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="a6d80-137">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="a6d80-137">For example:</span></span>  

    <span data-ttu-id="a6d80-138">04/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="a6d80-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="a6d80-139">05/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="a6d80-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="a6d80-140">06/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="a6d80-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="a6d80-141">De definerte feriedagene har ingen disponibel kapasitet i arbeidssenterkalenderen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="a6d80-142">Produksjonskalenderen kan nå tilordnes til et arbeidssenter for å beregne produksjonskalenderen for selve arbeidet. Denne kalenderen styrer all operasjonsplanlegging ved arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="a6d80-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="a6d80-143">Slik beregner du en arbeidssenterkalender</span><span class="sxs-lookup"><span data-stu-id="a6d80-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="a6d80-144">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidssentre**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="a6d80-145">Åpne arbeidssenteret som du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="a6d80-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="a6d80-146">I feltet **Produksjonskalenderkode** velger du hvilken produksjonskalender som skal brukes som grunnlag for en arbeidssenterkalender.</span><span class="sxs-lookup"><span data-stu-id="a6d80-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="a6d80-147">Velg handlingen **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="a6d80-148">På siden **Arbeidssenterkalender** velger du **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="a6d80-149">Til venstre på matrisesiden vises arbeidssentrene som er definert.</span><span class="sxs-lookup"><span data-stu-id="a6d80-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="a6d80-150">Til høyre vises en kalender med verdier for disponibel kapasitet for hver virkedag i den definerte enheten, for eksempel **480** minutter.</span><span class="sxs-lookup"><span data-stu-id="a6d80-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="a6d80-151">Hver linje representerer kalenderen for ett arbeidssenter.</span><span class="sxs-lookup"><span data-stu-id="a6d80-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a6d80-152">Du kan også vise kapasitetsverdiene for hver uke eller måned ved å endre valget i **Vis etter**-feltet på siden **Arbeidssenterkalender**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="a6d80-153">Hvis du vil gjenspeile den nye produksjonskalenderen som en linje i det valgte arbeidssenteret, må den først beregnes.</span><span class="sxs-lookup"><span data-stu-id="a6d80-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="a6d80-154">Velg handlingen **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="a6d80-155">På hurtigfanen **Arbeidssenter** kan du angi et filter som bare beregner for ett arbeidssenter.</span><span class="sxs-lookup"><span data-stu-id="a6d80-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="a6d80-156">Hvis du ikke angir et filter, beregnes alle eksisterende arbeidssenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="a6d80-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="a6d80-157">Definer start- og sluttdato for kalenderperioden som skal beregnes, for eksempel ett år fra 01.01.14 til 31.12.14.</span><span class="sxs-lookup"><span data-stu-id="a6d80-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="a6d80-158">Velg **OK**-knappen for å beregne kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="a6d80-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="a6d80-159">Kalenderposter opprettes eller oppdateres nå med visning av disponibel kapasitet for hver periode i henhold til følgende tre sett med hoveddata:</span><span class="sxs-lookup"><span data-stu-id="a6d80-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="a6d80-160">Virkedagene og skiftet som er definert i den tilordnede produksjonskalenderen.</span><span class="sxs-lookup"><span data-stu-id="a6d80-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="a6d80-161">Verdien i **Kapasitet**-feltet på arbeidssenterkortet.</span><span class="sxs-lookup"><span data-stu-id="a6d80-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="a6d80-162">Verdien i **Effektivitet**-feltet på arbeidssenterkortet.</span><span class="sxs-lookup"><span data-stu-id="a6d80-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="a6d80-163">Den beregnede arbeidssenterkalenderen definerer nå når og hvor stor kapasitet som er tilgjengelig ved dette arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="a6d80-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="a6d80-164">Dette kontrollerer den detaljerte tidsplanleggingen av operasjoner som utføres ved arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="a6d80-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="a6d80-165">Slik registrerer du fravær ved et arbeidssenter</span><span class="sxs-lookup"><span data-stu-id="a6d80-165">To record work center absence</span></span>  
1.  <span data-ttu-id="a6d80-166">På siden **Arbeidssenterkalender** velger du **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="a6d80-167">På siden **Matrise for arbeidssenterkalender** velger du arbeidssenteret og kalenderdagen når fraværstiden skal registreres. Deretter velger du **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="a6d80-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="a6d80-168">På **Fravær**-siden definerer du starttidspunktet, sluttidspunktet og beskrivelsen av dagens fravær.</span><span class="sxs-lookup"><span data-stu-id="a6d80-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="a6d80-169">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="a6d80-169">For example:</span></span>  

    <span data-ttu-id="a6d80-170">25/01/01 08:00 10:00 Vedlikehold</span><span class="sxs-lookup"><span data-stu-id="a6d80-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="a6d80-171">Velg **Oppdater**-handlingen, og lukk deretter **Fravær**-siden.</span><span class="sxs-lookup"><span data-stu-id="a6d80-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="a6d80-172">Kapasiteten for den valgte dagen er nå redusert med den registrerte fraværstiden.</span><span class="sxs-lookup"><span data-stu-id="a6d80-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a6d80-173">Se også</span><span class="sxs-lookup"><span data-stu-id="a6d80-173">See Also</span></span>  
[<span data-ttu-id="a6d80-174">Definere hovedkalendere</span><span class="sxs-lookup"><span data-stu-id="a6d80-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="a6d80-175">Konfigurere arbeidssentre og produksjonsressurser</span><span class="sxs-lookup"><span data-stu-id="a6d80-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="a6d80-176">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="a6d80-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="a6d80-177">Produksjon</span><span class="sxs-lookup"><span data-stu-id="a6d80-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="a6d80-178">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6d80-178">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
