---
title: Bokføringsdato på verdiposter
description: Lær hvordan kjørselen Juster kostverdi - vareposter identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215106"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="77703-103">Designdetaljer: Bokføringsdato på verdiposten for justering</span><span class="sxs-lookup"><span data-stu-id="77703-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="77703-104">Denne artikkelen gir en beskrivelse av funksjonen for kostberegning av beholdning i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="77703-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="77703-105">Denne artikkelen beskriver hvordan kjørselen **Juster kostverdi - vareposter** identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.</span><span class="sxs-lookup"><span data-stu-id="77703-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="77703-106">Først gjennomgås begrepet om prosessen, hvordan kjørselen identifiserer og tilordner bokføringsdatoen til verdiposten som skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="77703-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="77703-107">Deretter formidler vi noen scenarier som vi i støtteteamet møter på med jevne mellomrom, og til slutt er det en oppsummering av begrepene.</span><span class="sxs-lookup"><span data-stu-id="77703-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="77703-108">Begrepet</span><span class="sxs-lookup"><span data-stu-id="77703-108">The Concept</span></span>  
<span data-ttu-id="77703-109">Kjørselen **Juster kostverdi – vareposter** tilordner en bokføringsdato til verdiposten den skal opprette, på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="77703-109">The **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="77703-110">Først er bokføringsdatoen for posten som skal opprettes, samme dato som posten den justerer</span><span class="sxs-lookup"><span data-stu-id="77703-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="77703-111">Bokføringsdatoen valideres mot lagerperioder og/eller finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="77703-112">Tilordning av bokføringsdato: Hvis opprinnelig bokføringsdato ikke er innenfor tillatt datointervall for bokføring, tilordner kjørselen en tillatt bokføringsdato fra finansoppsett eller lagerperiode.</span><span class="sxs-lookup"><span data-stu-id="77703-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="77703-113">Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, tilordnes den seneste datoen av de to til verdiposten for justering.</span><span class="sxs-lookup"><span data-stu-id="77703-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="77703-114">La oss se på prosessen ved hjelp av et praktisk eksempel.</span><span class="sxs-lookup"><span data-stu-id="77703-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="77703-115">Anta at vi har en varepost for salg.</span><span class="sxs-lookup"><span data-stu-id="77703-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="77703-116">Varen ble levert 5. september 2013, og den ble fakturert dagen etter.</span><span class="sxs-lookup"><span data-stu-id="77703-116">The item was shipped on September 5, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="77703-117">![Status for vareposter i scenariet](media/helene/TechArticleAdjustcost1.png "Status for vareposter i scenariet")</span><span class="sxs-lookup"><span data-stu-id="77703-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="77703-118">Den første verdiposten (379) nedenfor representerer leveringen og har samme bokføringsdato som den overordnede vareposten.</span><span class="sxs-lookup"><span data-stu-id="77703-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="77703-119">Den andre verdiposten (381) representerer fakturaen.</span><span class="sxs-lookup"><span data-stu-id="77703-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="77703-120">Den tredje verdiposten (391) er en justering av faktureringsverdiposten (381)</span><span class="sxs-lookup"><span data-stu-id="77703-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="77703-121">![Status for verdiposter i scenariet](media/helene/TechArticleAdjustcost2.png "Status for verdiposter i scenariet")</span><span class="sxs-lookup"><span data-stu-id="77703-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="77703-122">Trinn 1: Verdiposten for justering som skal opprettes, tildeles samme bokføringsdato som posten den justerer, som vist ovenfor ved verdipost 391.</span><span class="sxs-lookup"><span data-stu-id="77703-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="77703-123">Trinn 2: Validering av opprinnelig tilordnet bokføringsdato.</span><span class="sxs-lookup"><span data-stu-id="77703-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="77703-124">**Juster kostverdi - vareposter**-kjørselen bestemmer om den første bokføringsdatoen for verdiposten for justering er innenfor tillatt datointervall for bokføring basert på lagerperioder og/eller finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="77703-125">La oss gå gjennom salget som er angitt ovenfor, ved å legge til oppsett for tillatt bokføringsdatointervall.</span><span class="sxs-lookup"><span data-stu-id="77703-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="77703-126">Lagerperioder:</span><span class="sxs-lookup"><span data-stu-id="77703-126">Inventory Periods:</span></span>  

<span data-ttu-id="77703-127">![Lagerperioder i scenariet](media/helene/TechArticleAdjustcost3.png "Lagerperioder i scenariet")</span><span class="sxs-lookup"><span data-stu-id="77703-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="77703-128">Den første tillatte bokføringsdatoen er den første dagen i den første åpne perioden.</span><span class="sxs-lookup"><span data-stu-id="77703-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="77703-129">1. september 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-129">September 1, 2013.</span></span>  

 <span data-ttu-id="77703-130">Finansoppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-130">General Ledger Setup:</span></span>  

<span data-ttu-id="77703-131">![Finansoppsett i scenariet](media/helene/TechArticleAdjustcost4.png "Finansoppsett i scenariet")</span><span class="sxs-lookup"><span data-stu-id="77703-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="77703-132">Første tillatte bokføringsdato er datoen som er angitt i feltet Bokf. tillatt fra: 10. september 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-132">First allowed posting date is the date stated in field Allow Posting From: September 10, 2013.</span></span>  

 <span data-ttu-id="77703-133">Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, definerer den seneste datoen av de to det tillatte bokføringsdatointervallet.</span><span class="sxs-lookup"><span data-stu-id="77703-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="77703-134">Trinn 3: Tilordning av en tillatt bokføringsdato.</span><span class="sxs-lookup"><span data-stu-id="77703-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="77703-135">Første tilordnede bokføringsdato var 6. september, som vist i trinn 1.</span><span class="sxs-lookup"><span data-stu-id="77703-135">The initial assigned Posting Date was September 6 as illustrated in step 1.</span></span> <span data-ttu-id="77703-136">Men i det andre trinnet identifiserer kjørselen Juster kostverdi – vareposter at den tidligste tillatte bokføringsdatoen er 10. september, og dermed tilordnes 10. september til verdiposten for justeringsposten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="77703-136">However, in the second step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10 and thereby assigns September 10 to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="77703-137">![Status for verdiposter i scenariet 2](media/helene/TechArticleAdjustcost5.png "Status for verdiposter i scenariet 2")</span><span class="sxs-lookup"><span data-stu-id="77703-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="77703-138">Vi har nå sett på begrepet om å tilordne bokføringsdatoer til verdiposter som opprettes av kjørselen Juster kostverdi - vareposter.</span><span class="sxs-lookup"><span data-stu-id="77703-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="77703-139">La oss fortsette å se på noen scenarioer som vi i støtteteamet møter på fra tid til annen knyttet til tilordnede bokføringsdatoer i kjørselen Juster kostverdi – vareposter og relaterte oppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="77703-140">Scenarier</span><span class="sxs-lookup"><span data-stu-id="77703-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="77703-141">Scenario I: Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer ...</span><span class="sxs-lookup"><span data-stu-id="77703-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="77703-142">Dette er en situasjon der en bruker får denne feilmeldingen når kjørselen Juster kostverdi - vareposter er kjørt.</span><span class="sxs-lookup"><span data-stu-id="77703-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="77703-143">I forrige del der vi beskrev begrepet om tilordning av bokføringsdatoer, var kjørselen Juster kostverdi - vareposter ment å opprette en verdipost med bokføringsdato 10. september.</span><span class="sxs-lookup"><span data-stu-id="77703-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="77703-144">![Feilmelding om bokføringsdato](media/helene/TechArticleAdjustcost6.png "Feilmelding om bokføringsdato")</span><span class="sxs-lookup"><span data-stu-id="77703-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="77703-145">Vi følge opp med brukeroppsettet:</span><span class="sxs-lookup"><span data-stu-id="77703-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="77703-146">![Oppsett av brukerens tillatte bokføringsdatoer](media/helene/TechArticleAdjustcost7.png "Oppsett av brukerens tillatte bokføringsdatoer")</span><span class="sxs-lookup"><span data-stu-id="77703-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="77703-147">Brukeren i dette tilfellet har et tillatt bokføringstidsrom fra 11. september til 30. september, og kan dermed ikke bokføre justeringsverdiposten med bokføringsdato 10. september.</span><span class="sxs-lookup"><span data-stu-id="77703-147">The user in this case has an allowed posting date range from September 11 to September 30 and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="77703-148">![Oversikt over involvert oppsett for bokføringsdato](media/helene/TechArticleAdjustcost8.png "Oversikt over involvert oppsett for bokføringsdato")</span><span class="sxs-lookup"><span data-stu-id="77703-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="77703-149">Kunnskapsbaseartikkel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver flere scenarioer knyttet til den nevnte feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="77703-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses more scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="77703-150">Scenario II: Bokføringsdato på verdipost for justering kontra bokføringsdato på post som forårsaker justeringen, for eksempel revaluering eller varegebyr.</span><span class="sxs-lookup"><span data-stu-id="77703-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="77703-151">Revalueringsscenario:</span><span class="sxs-lookup"><span data-stu-id="77703-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="77703-152">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="77703-152">Prerequisites:</span></span>  

 <span data-ttu-id="77703-153">Lageroppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-153">Inventory setup:</span></span>  

-   <span data-ttu-id="77703-154">Automatisk kostbokføring = Ja</span><span class="sxs-lookup"><span data-stu-id="77703-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="77703-155">Automatisk kostjustering = Alltid</span><span class="sxs-lookup"><span data-stu-id="77703-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="77703-156">Beregn.type for gj.snittskost = vare</span><span class="sxs-lookup"><span data-stu-id="77703-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="77703-157">Gjennomsnittskostperiode = Dag</span><span class="sxs-lookup"><span data-stu-id="77703-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="77703-158">Finansoppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="77703-159">Bokf. tillatt fra = 1. januar 2014</span><span class="sxs-lookup"><span data-stu-id="77703-159">Allow Posting From = January 1, 2014</span></span>  

-   <span data-ttu-id="77703-160">Bokf. tillatt til = tom</span><span class="sxs-lookup"><span data-stu-id="77703-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="77703-161">Brukeroppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-161">User Setup:</span></span>  

-   <span data-ttu-id="77703-162">Bokf. tillatt fra = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-162">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="77703-163">Bokf. tillatt til = tom</span><span class="sxs-lookup"><span data-stu-id="77703-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="77703-164">Slik tester du scenarioet:</span><span class="sxs-lookup"><span data-stu-id="77703-164">To test the scenario</span></span>  

1.  <span data-ttu-id="77703-165">Opprett varen TEST:</span><span class="sxs-lookup"><span data-stu-id="77703-165">Create item TEST:</span></span>  

     <span data-ttu-id="77703-166">Lagerenhet = STK</span><span class="sxs-lookup"><span data-stu-id="77703-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="77703-167">Lagermetode = Gjennomsnitt</span><span class="sxs-lookup"><span data-stu-id="77703-167">Costing Method = Average</span></span>  

     <span data-ttu-id="77703-168">Velg valgfrie bokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="77703-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="77703-169">Åpne varekladden, og opprett og bokfør en linje på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="77703-169">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="77703-170">Bokføringsdato = 15. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-170">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="77703-171">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="77703-171">Item = TEST</span></span>  

     <span data-ttu-id="77703-172">Posttype = Kjøp</span><span class="sxs-lookup"><span data-stu-id="77703-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="77703-173">Antall = 100</span><span class="sxs-lookup"><span data-stu-id="77703-173">Quantity = 100</span></span>  

     <span data-ttu-id="77703-174">Enhetsbeløp = 10</span><span class="sxs-lookup"><span data-stu-id="77703-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="77703-175">Åpne varekladden, og opprett og bokfør en linje på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="77703-175">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="77703-176">Dato = 20. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-176">Date = December 20, 2013</span></span>  

     <span data-ttu-id="77703-177">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="77703-177">Item = TEST</span></span>  

     <span data-ttu-id="77703-178">Posttype = Nedjustering</span><span class="sxs-lookup"><span data-stu-id="77703-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="77703-179">Antall = 2</span><span class="sxs-lookup"><span data-stu-id="77703-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="77703-180">Åpne varekladden, og opprett og bokfør en linje på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="77703-180">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="77703-181">Dato = 15. januar 2014</span><span class="sxs-lookup"><span data-stu-id="77703-181">Date = January 15, 2014</span></span>  

     <span data-ttu-id="77703-182">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="77703-182">Item = TEST</span></span>  

     <span data-ttu-id="77703-183">Posttype = Nedjustering</span><span class="sxs-lookup"><span data-stu-id="77703-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="77703-184">Antall = 3</span><span class="sxs-lookup"><span data-stu-id="77703-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="77703-185">Åpne revalueringskladden, og opprett og bokfør en linje på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="77703-185">Open Revaluation Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="77703-186">Vare = TEST</span><span class="sxs-lookup"><span data-stu-id="77703-186">Item = TEST</span></span>  

     <span data-ttu-id="77703-187">Utligningspost = velg kjøpspost bokført i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="77703-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="77703-188">Bokføringsdatoen for revalueringen blir lik posten den justerer.</span><span class="sxs-lookup"><span data-stu-id="77703-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="77703-189">Enhetskost (revaluert) = 40</span><span class="sxs-lookup"><span data-stu-id="77703-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="77703-190">Følgende vareposter og verdiposter er bokført:</span><span class="sxs-lookup"><span data-stu-id="77703-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="77703-191">![Oversikt over resulterende finans- og vareposter 1](media/helene/TechArticleAdjustcost9.png "Oversikt over resulterende finans- og vareposter 1")</span><span class="sxs-lookup"><span data-stu-id="77703-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="77703-192">![Oversikt over resulterende finans- og vareposter 2](media/helene/TechArticleAdjustcost10.png "Oversikt over resulterende finans- og vareposter 2")</span><span class="sxs-lookup"><span data-stu-id="77703-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="77703-193">Juster kostverdi – vareposter-kjørselen har gjenkjent en endring i kost og justert nedjusteringene.</span><span class="sxs-lookup"><span data-stu-id="77703-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="77703-194">**Gjennomgang av bokføringsdatoer på opprettede verdiposter for justering:** Den tidligste tillatte bokføringsdatoen som kjørselen Juster kostverdi - vareposter må relateres til, er 1. januar 2014, som angitt i Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="77703-195">**Nedjustering i trinn 3:** Tilordnet bokføringsdato er 1. januar, angitt i finansoppsettet.</span><span class="sxs-lookup"><span data-stu-id="77703-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1, provided by General Ledger Setup.</span></span> <span data-ttu-id="77703-196">Bokføringsdatoen for verdiposten i området for justering er 20. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="77703-197">I henhold til Finansoppsett er ikke datoen innenfor det tillatte datointervallet for bokføring.</span><span class="sxs-lookup"><span data-stu-id="77703-197">According to General Ledger Setup, the date is not within allowed posting date range.</span></span> <span data-ttu-id="77703-198">Derfor tilordnes bokføringsdatoen som er angitt i feltet Bokf. tillatt fra i finansoppsettet, til verdiposten for justering.</span><span class="sxs-lookup"><span data-stu-id="77703-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="77703-199">**Nedjustering i trinn 4:** Tilordnet bokføringsdato er 15. januar.</span><span class="sxs-lookup"><span data-stu-id="77703-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15.</span></span> <span data-ttu-id="77703-200">Verdiposten i området for justering har bokføringsdatoen 15. januar, som er innenfor det tillatte bokføringsdatointervallet i henhold til Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-200">The Value Entry in scope of adjustment has Posting Date January 15, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="77703-201">Justeringen foretatt for nedjusteringen i trinn 3 fører til diskusjon.</span><span class="sxs-lookup"><span data-stu-id="77703-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="77703-202">Den beste bokføringsdatoen for verdiposten for justering ville vært 20. desember eller i det minste i desember siden revalueringen som forårsaker endringen i vareforbruk, ble bokført i desember.</span><span class="sxs-lookup"><span data-stu-id="77703-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20 or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="77703-203">For å oppnå justering i desember for nedjusteringen i trinn 3, må feltet Bokf. tillatt fra i Finansoppsett angi en dato i desember.</span><span class="sxs-lookup"><span data-stu-id="77703-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="77703-204">**Konklusjon:**</span><span class="sxs-lookup"><span data-stu-id="77703-204">**Conclusion:**</span></span>  

 <span data-ttu-id="77703-205">Med erfaringene fra dette scenarioet, når du skal vurdere det best egnede oppsettet for tillatt bokføringsdatointervall for et selskap, kan du vurdere følgende informasjon: Såfremt du tillater endringer i lagerverdien kan bokføres i en periode, desember i dette tilfellet, må oppsettet som selskapet bruker for tillatt bokføringsdatoområde, justeres i henhold til denne beslutningen.</span><span class="sxs-lookup"><span data-stu-id="77703-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, you might want to consider the following information: As long as you allow changes in inventory value to be posted in a period, December in this case, the setup that the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="77703-206">Bokf. tillatt fra i finansoppsettet, som angir 1. desember, ville tillatt at revalueringen i desember kunne overføres til påvirkede utgående poster i samme periode.</span><span class="sxs-lookup"><span data-stu-id="77703-206">The Allow Posting From in the General Ledger Setup, stating December 1, would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="77703-207">Brukergrupper som ikke kan bokføre i desember, men i januar, som sannsynligvis var ment å være begrenset av finansoppsettet i dette scenarioet, bør i stedet løses via brukeroppsettet.</span><span class="sxs-lookup"><span data-stu-id="77703-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="77703-208">Varegebyrscenario:</span><span class="sxs-lookup"><span data-stu-id="77703-208">Item charge scenario:</span></span>  
 <span data-ttu-id="77703-209">Forutsetninger:</span><span class="sxs-lookup"><span data-stu-id="77703-209">Prerequisites:</span></span>  

 <span data-ttu-id="77703-210">Lageroppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-210">Inventory setup:</span></span>  

-   <span data-ttu-id="77703-211">Automatisk kostbokføring = Ja</span><span class="sxs-lookup"><span data-stu-id="77703-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="77703-212">Automatisk kostjustering = Alltid</span><span class="sxs-lookup"><span data-stu-id="77703-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="77703-213">Beregn.type for gj.snittskost = vare</span><span class="sxs-lookup"><span data-stu-id="77703-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="77703-214">Gjennomsnittskostperiode = Dag</span><span class="sxs-lookup"><span data-stu-id="77703-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="77703-215">Finansoppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="77703-216">Bokf. tillatt fra = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-216">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="77703-217">Bokf. tillatt til = tom</span><span class="sxs-lookup"><span data-stu-id="77703-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="77703-218">Brukeroppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-218">User Setup:</span></span>  

-   <span data-ttu-id="77703-219">Bokf. tillatt fra = 1. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-219">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="77703-220">Bokf. tillatt til = tom</span><span class="sxs-lookup"><span data-stu-id="77703-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="77703-221">Slik tester du scenarioet</span><span class="sxs-lookup"><span data-stu-id="77703-221">To test the scenario</span></span>  

1.  <span data-ttu-id="77703-222">Opprett varegebyr:</span><span class="sxs-lookup"><span data-stu-id="77703-222">Create item charge:</span></span>  

     <span data-ttu-id="77703-223">Lagerenhet = STK</span><span class="sxs-lookup"><span data-stu-id="77703-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="77703-224">Lagermetode = Gjennomsnitt</span><span class="sxs-lookup"><span data-stu-id="77703-224">Costing Method = Average</span></span>  

     <span data-ttu-id="77703-225">Velg valgfrie bokføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="77703-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="77703-226">Opprett ny bestilling</span><span class="sxs-lookup"><span data-stu-id="77703-226">Create new purchase order</span></span>  

     <span data-ttu-id="77703-227">Kjøp fra-leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="77703-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="77703-228">Bokføringsdato = 15. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-228">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="77703-229">Leverandørs fakturanr.: 1234</span><span class="sxs-lookup"><span data-stu-id="77703-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="77703-230">På bestillingslinjen:</span><span class="sxs-lookup"><span data-stu-id="77703-230">On the purchase order line:</span></span>  

     <span data-ttu-id="77703-231">Vare = GEBYR</span><span class="sxs-lookup"><span data-stu-id="77703-231">Item = CHARGE</span></span>  

     <span data-ttu-id="77703-232">Antall = 1</span><span class="sxs-lookup"><span data-stu-id="77703-232">Quantity = 1</span></span>  

     <span data-ttu-id="77703-233">Direkte enhetskost = 100</span><span class="sxs-lookup"><span data-stu-id="77703-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="77703-234">Bokfør mottak og faktura.</span><span class="sxs-lookup"><span data-stu-id="77703-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="77703-235">Opprett ny ordre:</span><span class="sxs-lookup"><span data-stu-id="77703-235">Create new sales order:</span></span>  

     <span data-ttu-id="77703-236">Salg til-kundenr.: 10000</span><span class="sxs-lookup"><span data-stu-id="77703-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="77703-237">Bokføringsdato = 16. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-237">Posting Date = December 16, 2013</span></span>  

     <span data-ttu-id="77703-238">På ordrelinjen:</span><span class="sxs-lookup"><span data-stu-id="77703-238">On the sales order line:</span></span>  

     <span data-ttu-id="77703-239">Vare = GEBYR</span><span class="sxs-lookup"><span data-stu-id="77703-239">Item = CHARGE</span></span>  

     <span data-ttu-id="77703-240">Antall = 1</span><span class="sxs-lookup"><span data-stu-id="77703-240">Quantity = 1</span></span>  

     <span data-ttu-id="77703-241">Salgspris = 135</span><span class="sxs-lookup"><span data-stu-id="77703-241">Unit Price = 135</span></span>  

     <span data-ttu-id="77703-242">Bokfør levering og faktura.</span><span class="sxs-lookup"><span data-stu-id="77703-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="77703-243">Finansoppsett:</span><span class="sxs-lookup"><span data-stu-id="77703-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="77703-244">Bokf. tillatt fra = 1. januar 2014</span><span class="sxs-lookup"><span data-stu-id="77703-244">Allow Posting From = January 1, 2014</span></span>  

     <span data-ttu-id="77703-245">Bokf. tillatt til = tom</span><span class="sxs-lookup"><span data-stu-id="77703-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="77703-246">Opprett ny bestilling:</span><span class="sxs-lookup"><span data-stu-id="77703-246">Create new purchase order:</span></span>  

     <span data-ttu-id="77703-247">Kjøp fra-leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="77703-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="77703-248">Bokføringsdato = 2. januar 2014</span><span class="sxs-lookup"><span data-stu-id="77703-248">Posting Date = January 2, 2014</span></span>  

     <span data-ttu-id="77703-249">Leverandørs fakturanr.: 2345</span><span class="sxs-lookup"><span data-stu-id="77703-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="77703-250">På bestillingslinjen:</span><span class="sxs-lookup"><span data-stu-id="77703-250">On the purchase order line:</span></span>  

     <span data-ttu-id="77703-251">Varegebyr = NC-FRAKT</span><span class="sxs-lookup"><span data-stu-id="77703-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="77703-252">Antall = 1</span><span class="sxs-lookup"><span data-stu-id="77703-252">Quantity = 1</span></span>  

     <span data-ttu-id="77703-253">Direkte enhetskost = 3</span><span class="sxs-lookup"><span data-stu-id="77703-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="77703-254">Tilordne varegebyr til kjøpsmottak fra trinn 2.</span><span class="sxs-lookup"><span data-stu-id="77703-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="77703-255">Bokfør mottak og faktura.</span><span class="sxs-lookup"><span data-stu-id="77703-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="77703-256">![Oversikt over resulterende finans- og vareposter 3](media/helene/TechArticleAdjustcost11.png "Oversikt over resulterende finans- og vareposter 3")</span><span class="sxs-lookup"><span data-stu-id="77703-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="77703-257">På arbeidsdatoen 3. januar kommer en kjøpsfaktura som inneholder et ekstra varegebyr for kjøpet som ble gjort i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="77703-257">On work date January 3, a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="77703-258">Denne fakturaen har bilagsdato 30. desember, og bokføres derfor med bokføringsdatoen 30. desember 2013.</span><span class="sxs-lookup"><span data-stu-id="77703-258">This invoice has document date December 30 and is therefore posted with Posting Date December 30, 2013.</span></span>  

     <span data-ttu-id="77703-259">Opprett ny bestilling:</span><span class="sxs-lookup"><span data-stu-id="77703-259">Create new purchase order:</span></span>  

     <span data-ttu-id="77703-260">Kjøp fra-leverandørnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="77703-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="77703-261">Bokføringsdato = 30. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-261">Posting Date = December 30, 2013</span></span>  

     <span data-ttu-id="77703-262">Leverandørs fakturanr.: 3456</span><span class="sxs-lookup"><span data-stu-id="77703-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="77703-263">På bestillingslinjen:</span><span class="sxs-lookup"><span data-stu-id="77703-263">On the purchase order line:</span></span>  

     <span data-ttu-id="77703-264">Varegebyr = NC-FRAKT</span><span class="sxs-lookup"><span data-stu-id="77703-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="77703-265">Antall = 1</span><span class="sxs-lookup"><span data-stu-id="77703-265">Quantity = 1</span></span>  

     <span data-ttu-id="77703-266">Direkte enhetskost = 2</span><span class="sxs-lookup"><span data-stu-id="77703-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="77703-267">Tilordne varegebyr til kjøpsmottak fra trinn 2</span><span class="sxs-lookup"><span data-stu-id="77703-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="77703-268">Bokfør mottak og faktura.</span><span class="sxs-lookup"><span data-stu-id="77703-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="77703-269">![Oversikt over resulterende finans- og vareposter 4](media/helene/TechArticleAdjustcost12.png "Oversikt over resulterende finans- og vareposter 4")</span><span class="sxs-lookup"><span data-stu-id="77703-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="77703-270">Lagerverdisettingsrapporten skrives ut per 31. desember 2013</span><span class="sxs-lookup"><span data-stu-id="77703-270">Inventory Valuation report is printed as of Date December 31 , 2013</span></span>  

<span data-ttu-id="77703-271">![Innholdet i rapporten Lagerverdisetting](media/helene/TechArticleAdjustcost13.png "Innholdet i rapporten Lagerverdisetting")</span><span class="sxs-lookup"><span data-stu-id="77703-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="77703-272">**Sammendrag av scenarioet:**</span><span class="sxs-lookup"><span data-stu-id="77703-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="77703-273">Det beskrevne scenarioet ender opp med en lagerverdisettingsrapport som viser antall = 0 når verdien = 2.</span><span class="sxs-lookup"><span data-stu-id="77703-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="77703-274">Varegebyret som ble bokført i trinn 11, er del av lagerøkningsverdien i desember, mens lagerreduksjonen i samme periode påvirkes ikke.</span><span class="sxs-lookup"><span data-stu-id="77703-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="77703-275">At Finansoppsett angir Bokf. tillatt fra 1. januar var nyttig for det første varegebyret.</span><span class="sxs-lookup"><span data-stu-id="77703-275">Having the General Ledger Setup stating Allow Posting From January 1 was a good thing for the first Item charge.</span></span> <span data-ttu-id="77703-276">Kostnadene ved lagerøkning og -reduksjon ble registrert i samme periode.</span><span class="sxs-lookup"><span data-stu-id="77703-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="77703-277">For det andre varegebyret derimot, fører finansoppsettet til at endringen i vareforbruk føres på perioden etter.</span><span class="sxs-lookup"><span data-stu-id="77703-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="77703-278">**Konklusjon:**</span><span class="sxs-lookup"><span data-stu-id="77703-278">**Conclusion:**</span></span>  

 <span data-ttu-id="77703-279">Det er utfordrende å få lagerverdisettingsrapporten til å vise antall = 0 når verdien <> 0.</span><span class="sxs-lookup"><span data-stu-id="77703-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="77703-280">I dette tilfellet er det også vanskeligere å uttrykke optimale innstillinger når du har kjøpsfakturaer som kommer på samme dag, men på forskjellige perioder eller regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="77703-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="77703-281">Kryssing til et nytt regnskapsår krever vanligvis noe planlegging, og som en del av innsikten fra Juster kostverdi - vareposter-prosessen må føring av vareforbruk vurderes.</span><span class="sxs-lookup"><span data-stu-id="77703-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="77703-282">I dette scenarioet kunne ett alternativ ha vært å angi en dato i desember for noen flere dager i feltet Bokf. tillatt fra i Finansoppsett, og utsette bokføringen av det første varegebyret, slik at alle kostnader for forrige periode/regnskapsår føres for perioden de tilhører først, og kjøre kjørselen Juster kostverdi - vareposter, og deretter flytte den tillatte bokføringsdatoen til den nye perioden\/regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="77703-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="77703-283">Det første varegebyret med bokføringsdato 2. januar kunne deretter bli bokført.</span><span class="sxs-lookup"><span data-stu-id="77703-283">The first item charge with posting date January 2 could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="77703-284">Historikk for kjørselen Juster kostverdi - vareposter</span><span class="sxs-lookup"><span data-stu-id="77703-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="77703-285">Nedenfor finner du et sammendrag av begrepet om tilordning av bokføringsdatoer til verdiposter for justering med kjørselen Juster kostverdi – vareposter.</span><span class="sxs-lookup"><span data-stu-id="77703-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job.</span></span>  

### <a name="about-the-request-form-posting-date"></a><span data-ttu-id="77703-286">Om forespørselsskjemaet Bokføringsdato:</span><span class="sxs-lookup"><span data-stu-id="77703-286">About the request form posting date:</span></span>  
 <span data-ttu-id="77703-287">Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Juster kostverdi - vareposter.</span><span class="sxs-lookup"><span data-stu-id="77703-287">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="77703-288">Kjørselen kjører gjennom alle nødvendige endringer og oppretter verdiposter med bokføringsdatoen for verdiposten den justerer.</span><span class="sxs-lookup"><span data-stu-id="77703-288">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="77703-289">Hvis bokføringsdatoen ikke er innenfor tillatt datointervall for bokføring, brukes bokføringsdatoen i feltet Bokf. tillatt fra i finansoppsettet, eller hvis lagerperiodene brukes, brukes den seneste datoen av de to.</span><span class="sxs-lookup"><span data-stu-id="77703-289">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="77703-290">Se beskrevet begrep ovenfor.</span><span class="sxs-lookup"><span data-stu-id="77703-290">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="77703-291">Historikk for kjørselen Bokfør lagerkost i Finans</span><span class="sxs-lookup"><span data-stu-id="77703-291">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="77703-292">Kjørselen Bokfør lagerkost i Finans er nært knyttet til kjørselen Juster kostverdi – vareposter, og er grunnen til at denne kjørselen oppsummeres og formidles her også.</span><span class="sxs-lookup"><span data-stu-id="77703-292">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  
 
<span data-ttu-id="77703-293">![Faktiske kostnader og forventede kostnader](media/helene/TechArticleAdjustcost14.png "Faktiske kostnader og forventede kostnader")</span><span class="sxs-lookup"><span data-stu-id="77703-293">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="about-the-posting-date"></a><span data-ttu-id="77703-294">Om bokføringsdatoen</span><span class="sxs-lookup"><span data-stu-id="77703-294">About the posting date</span></span>
 <span data-ttu-id="77703-295">Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Bokfør lagerkost i Finans.</span><span class="sxs-lookup"><span data-stu-id="77703-295">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="77703-296">Finansposten opprettes med samme bokføringsdato som den relaterte verdiposten.</span><span class="sxs-lookup"><span data-stu-id="77703-296">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="77703-297">For å fullføre kjørselen må det tillatte bokføringsdatointervallet tillate bokføringsdatoen for den opprettede finansposten.</span><span class="sxs-lookup"><span data-stu-id="77703-297">In order to complete the batch job, the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="77703-298">Hvis ikke, må det tillatte bokføringsdatointervallet midlertidig åpnes på nytt ved å endre eller fjerne datoene i feltet Bokf. tillatt fra og Tillat bokf. til i Finansoppsett.</span><span class="sxs-lookup"><span data-stu-id="77703-298">If not, the allowed posting date range must be temporarily reopened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="77703-299">For å unngå avstemmingsproblemer må bokføringsdato for finansposten svare til bokføringsdatoen for verdiposten.</span><span class="sxs-lookup"><span data-stu-id="77703-299">To avoid reconciliation issues, it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="77703-300">Kjørselen søker gjennom tabell 5811 - Bokfør verdipost i Finans for å identifisere verdipostene innenfor området for bokføring i Finans.</span><span class="sxs-lookup"><span data-stu-id="77703-300">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="77703-301">Tabellen tømmes når du har utført kjørselen.</span><span class="sxs-lookup"><span data-stu-id="77703-301">After a successful run, the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="77703-302">Se også</span><span class="sxs-lookup"><span data-stu-id="77703-302">See Also</span></span>  
[<span data-ttu-id="77703-303">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="77703-303">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="77703-304">Designdetaljer: Vareutligning</span><span class="sxs-lookup"><span data-stu-id="77703-304">Design Details: Item Application</span></span>](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
