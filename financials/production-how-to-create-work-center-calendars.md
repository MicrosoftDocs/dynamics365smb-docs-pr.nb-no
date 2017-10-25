---
title: Definere produksjonskalendere | Microsoft-dokumentasjon
description: "En arbeidssenterkalender angir virkedager og arbeidstider, skift, ferie og fravær som utgjør arbeidssenterets disponible kapasitet, målt i tid, i henhold til senterets definerte effektivitets- og kapasitetsverdier. Opprettelse og aktivering av en arbeidssenterkalender omfatter flere forhåndsoppgaver."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f42941328d49aee4e823007284fd14417866cbae
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shop-calendars"></a><span data-ttu-id="06687-104">Opprette produksjonskalendere</span><span class="sxs-lookup"><span data-stu-id="06687-104">How to: Set Up Shop Calendars</span></span>
<span data-ttu-id="06687-105">En arbeidssenter- eller maskinkalender angir virkedager/arbeidstider, skift, ferie og fravær som utgjør senterets disponible kapasitet (målt i tid) i henhold til senterets definerte effektivitets- og kapasitetsverdier.</span><span class="sxs-lookup"><span data-stu-id="06687-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="06687-106">Som grunnlag for beregning av en bestemt arbeidssenter- eller produksjonsressurskalender må du først definere en eller flere generelle produksjonskalendere.</span><span class="sxs-lookup"><span data-stu-id="06687-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="06687-107">En produksjonskalender definerer en standard arbeidsuke i henhold til starten og slutten på arbeidsdagen samt skiftarbeid.</span><span class="sxs-lookup"><span data-stu-id="06687-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="06687-108">I tillegg definerer produksjonskalenderen faste feriedager i løpet av året.</span><span class="sxs-lookup"><span data-stu-id="06687-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="06687-109">I det følgende beskrives hvordan du arbeidssenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="06687-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="06687-110">Trinnene ligner når du definerer produksjonsressurskalendere.</span><span class="sxs-lookup"><span data-stu-id="06687-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="06687-111">Slik oppretter du arbeidsskift</span><span class="sxs-lookup"><span data-stu-id="06687-111">To create work shifts</span></span>  
1.  <span data-ttu-id="06687-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="06687-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="06687-113">På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere arbeidsskiftet, for eksempel **1**.</span><span class="sxs-lookup"><span data-stu-id="06687-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="06687-114">Beskriv arbeidsskiftet i **Beskrivelse**-feltet, for eksempel **1. skift**.</span><span class="sxs-lookup"><span data-stu-id="06687-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="06687-115">Fyll eventuelt ut linjer for et andre eller tredje arbeidsskift.</span><span class="sxs-lookup"><span data-stu-id="06687-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="06687-116">Selv om arbeidssentrene ikke fungerer for andre arbeidsskift, angir du minst én arbeidsskiftkode.</span><span class="sxs-lookup"><span data-stu-id="06687-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="06687-117">Slik definerer du en produksjonskalender</span><span class="sxs-lookup"><span data-stu-id="06687-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="06687-118">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="06687-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="06687-119">På en tom linje skriver du inn nummeret i **Kode**-feltet for å identifisere produksjonskalenderen.</span><span class="sxs-lookup"><span data-stu-id="06687-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="06687-120">Beskriv produksjonskalenderen i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="06687-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="06687-121">Velg **Virkedager**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="06687-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="06687-122">I vinduet **Prod.kalender - virkedager**definerer du en fullstendig arbeidsuke med start- og sluttidspunkt for hver enkelt dag.</span><span class="sxs-lookup"><span data-stu-id="06687-122">In the **Shop Calendar Working Days** window, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="06687-123">Velg et av skiftene du har definert tidligere, i feltet **Arbeidsskiftkode**.</span><span class="sxs-lookup"><span data-stu-id="06687-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="06687-124">Legg til en linje for hver arbeidsdag og hvert skift.</span><span class="sxs-lookup"><span data-stu-id="06687-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="06687-125">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="06687-125">For example:</span></span>  

    <span data-ttu-id="06687-126">Mandag  07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="06687-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="06687-127">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="06687-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="06687-128">Hvis du trenger en produksjonskalender med to arbeidsskift, må du fylle den ut slik:</span><span class="sxs-lookup"><span data-stu-id="06687-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="06687-129">Mandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="06687-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="06687-130">Mandag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="06687-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="06687-131">Tirsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="06687-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="06687-132">Tirsdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="06687-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="06687-133">Ukedager du ikke definerer i produksjonskalenderen, for eksempel lørdag og søndag, anses ganske enkelt som fridager og har ingen verdi for disponibel kapasitet i en arbeidssenterkalender.</span><span class="sxs-lookup"><span data-stu-id="06687-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="06687-134">Når alle virkedager i en uke er definert, kan du lukke vinduet **Prod.kalender - virkedager** og fortsette med å registrere ferier.</span><span class="sxs-lookup"><span data-stu-id="06687-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** window and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="06687-135">I vinduet **Produksjonskalendere** velger du produksjonskalenderen og velger deretter **Ferie**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="06687-135">In the **Shop Calendars** window, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="06687-136">I vinduet **Prod.kalender - ferie** definerer du årets ferier ved å angi startdato/-klokkeslett, sluttidspunkt og beskrivelse av hver ferie på egne linjer, for eksempel på følgende måte.</span><span class="sxs-lookup"><span data-stu-id="06687-136">In the **Shop Calendar Holidays** window, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="06687-137">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="06687-137">For example:</span></span>  

    <span data-ttu-id="06687-138">04/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="06687-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="06687-139">05/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="06687-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="06687-140">06/07/14 0:00:00 23:59:00 Sommerferie</span><span class="sxs-lookup"><span data-stu-id="06687-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="06687-141">De definerte feriedagene har ingen disponibel kapasitet i arbeidssenterkalenderen.</span><span class="sxs-lookup"><span data-stu-id="06687-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="06687-142">Produksjonskalenderen kan nå tilordnes til et arbeidssenter for å beregne produksjonskalenderen for selve arbeidet. Denne kalenderen styrer all operasjonsplanlegging ved arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="06687-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="06687-143">Slik beregner du en arbeidssenterkalender</span><span class="sxs-lookup"><span data-stu-id="06687-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="06687-144">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Arbeidsskift**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="06687-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="06687-145">Åpne arbeidssenteret som du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="06687-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="06687-146">I feltet **Produksjonskalenderkode** velger du hvilken produksjonskalender som skal brukes som grunnlag for en arbeidssenterkalender.</span><span class="sxs-lookup"><span data-stu-id="06687-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="06687-147">Velg handlingen **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="06687-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="06687-148">I vinduet **Arbeidssenterkalender** velger du **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="06687-148">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="06687-149">Til venstre i matrisevinduet vises arbeidssentrene som er definert.</span><span class="sxs-lookup"><span data-stu-id="06687-149">The left side of the matrix window lists the work centers that are set up.</span></span> <span data-ttu-id="06687-150">Til høyre vises en kalender med verdier for disponibel kapasitet for hver virkedag i den definerte enheten, for eksempel **480** minutter.</span><span class="sxs-lookup"><span data-stu-id="06687-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="06687-151">Hver linje representerer kalenderen for ett arbeidssenter.</span><span class="sxs-lookup"><span data-stu-id="06687-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="06687-152">Du kan også vise kapasitetsverdiene for hver uke eller måned ved å endre valget i **Vis etter**-feltet i vinduet **Arbeidssenterkalender**.</span><span class="sxs-lookup"><span data-stu-id="06687-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field in the **Work Center Calendar** window.</span></span>  

    <span data-ttu-id="06687-153">Hvis du vil gjenspeile den nye produksjonskalenderen som en linje i det valgte arbeidssenteret, må den først beregnes.</span><span class="sxs-lookup"><span data-stu-id="06687-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="06687-154">Velg handlingen **Beregn**.</span><span class="sxs-lookup"><span data-stu-id="06687-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="06687-155">På hurtigfanen **Arbeidssenter** kan du angi et filter som bare beregner for ett arbeidssenter.</span><span class="sxs-lookup"><span data-stu-id="06687-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="06687-156">Hvis du ikke angir et filter, beregnes alle eksisterende arbeidssenterkalendere.</span><span class="sxs-lookup"><span data-stu-id="06687-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="06687-157">Definer start- og sluttdato for kalenderperioden som skal beregnes, for eksempel ett år fra 01.01.14 til 31.12.14.</span><span class="sxs-lookup"><span data-stu-id="06687-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="06687-158">Velg **OK**-knappen for å beregne kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="06687-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="06687-159">Kalenderposter opprettes eller oppdateres nå med visning av disponibel kapasitet for hver periode i henhold til følgende tre sett med hoveddata:</span><span class="sxs-lookup"><span data-stu-id="06687-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="06687-160">Virkedagene og skiftet som er definert i den tilordnede produksjonskalenderen.</span><span class="sxs-lookup"><span data-stu-id="06687-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="06687-161">Verdien i **Kapasitet**-feltet på arbeidssenterkortet.</span><span class="sxs-lookup"><span data-stu-id="06687-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="06687-162">Verdien i **Effektivitet**-feltet på arbeidssenterkortet.</span><span class="sxs-lookup"><span data-stu-id="06687-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="06687-163">Den beregnede arbeidssenterkalenderen definerer nå når og hvor stor kapasitet som er tilgjengelig ved dette arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="06687-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="06687-164">Dette kontrollerer den detaljerte tidsplanleggingen av operasjoner som utføres ved arbeidssenteret.</span><span class="sxs-lookup"><span data-stu-id="06687-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="06687-165">Slik registrerer du fravær ved et arbeidssenter</span><span class="sxs-lookup"><span data-stu-id="06687-165">To record work center absence</span></span>  
1.  <span data-ttu-id="06687-166">I vinduet **Arbeidssenterkalender** velger du **Vis matrise**.</span><span class="sxs-lookup"><span data-stu-id="06687-166">In the **Work Center Calendar** window, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="06687-167">I vinduet **Matrise for arbeidssenterkalender** velger du arbeidssenteret og kalenderdagen når fraværstiden skal registreres. Deretter velger du **Fravær**.</span><span class="sxs-lookup"><span data-stu-id="06687-167">In the **Work Center Calendar Matrix** window, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="06687-168">I **Fravær**-vinduet definerer du starttidspunktet, sluttidspunktet og beskrivelsen av dagens fravær.</span><span class="sxs-lookup"><span data-stu-id="06687-168">In the **Absence** window, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="06687-169">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="06687-169">For example:</span></span>  

    <span data-ttu-id="06687-170">25/01/01 08:00 10:00 Vedlikehold</span><span class="sxs-lookup"><span data-stu-id="06687-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="06687-171">Velg **Oppdater**-handlingen, og lukk deretter **Fravær**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="06687-171">Choose the **Update** action, and then close the **Absence** window.</span></span>  

<span data-ttu-id="06687-172">Kapasiteten for den valgte dagen er nå redusert med den registrerte fraværstiden.</span><span class="sxs-lookup"><span data-stu-id="06687-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06687-173">Se også</span><span class="sxs-lookup"><span data-stu-id="06687-173">See Also</span></span>  
[<span data-ttu-id="06687-174">Definere hovedkalendere</span><span class="sxs-lookup"><span data-stu-id="06687-174">How to: Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="06687-175">Konfigurere arbeidssentre og produksjonsressurser | Microsoft-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="06687-175">How to: Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="06687-176">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="06687-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="06687-177">Produksjon</span><span class="sxs-lookup"><span data-stu-id="06687-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="06687-178">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06687-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

