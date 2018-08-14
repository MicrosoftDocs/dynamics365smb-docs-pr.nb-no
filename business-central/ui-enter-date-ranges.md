---
title: Angi datointervaller i Business Central | Microsoft-dokumentasjon
description: "Finn ut hvordan du får en rapport til å vise data fra bestemte tidsperioder ved å bruke datointervaller i Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: nb-no
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="ce57c-103">Sette inn datointervaller</span><span class="sxs-lookup"><span data-stu-id="ce57c-103">Entering Date Ranges</span></span>
<span data-ttu-id="ce57c-104">Du kan angi filtre som inneholder en startdato og en sluttdato, for å vise bare dataene innenfor dette datointervallet eller tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="ce57c-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="ce57c-105">Særlige regler gjelder for angivelse av datointervaller.</span><span class="sxs-lookup"><span data-stu-id="ce57c-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="ce57c-106">La oss ta **Kunde - ti på topp** som eksempel:</span><span class="sxs-lookup"><span data-stu-id="ce57c-106">Let's take the **Customer Top 10** as an example:</span></span>

![Angi et datointervall på forespørselssiden for Kunde - ti på topp-listen](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="ce57c-108">Her kan du begrense rapporten til et datointervall, for eksempel de to siste ukene eller totalt seks uker, eller et hvilket som helst intervall du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="ce57c-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="ce57c-109">Du angir datointervaller ved å angi datoene og deretter bruke **..**</span><span class="sxs-lookup"><span data-stu-id="ce57c-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="ce57c-110">eller **|** til å angi intervallet.</span><span class="sxs-lookup"><span data-stu-id="ce57c-110">or **|** to set the range.</span></span> <span data-ttu-id="ce57c-111">Hvis du vil vise de ti beste kundene for de to første ukene i mai i eksemplet vårt, setter du datofilteret til *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="ce57c-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="ce57c-112">Her er noen andre eksempler:</span><span class="sxs-lookup"><span data-stu-id="ce57c-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="ce57c-113">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-113">Meaning</span></span> | <span data-ttu-id="ce57c-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ce57c-114">Example</span></span> | <span data-ttu-id="ce57c-115">Tar med poster</span><span class="sxs-lookup"><span data-stu-id="ce57c-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="ce57c-116">Lik</span><span class="sxs-lookup"><span data-stu-id="ce57c-116">Equal to</span></span>| <span data-ttu-id="ce57c-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="ce57c-117">12 15 16</span></span> |<span data-ttu-id="ce57c-118">Bare de som er bokført 15. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="ce57c-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="ce57c-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="ce57c-119">Interval</span></span>| <span data-ttu-id="ce57c-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="ce57c-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="ce57c-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="ce57c-121">..12 15 16</span></span>|<span data-ttu-id="ce57c-122">De som er bokført på datoer mellom og inkludert 15. desember 2016 og 15. januar 2017.</span><span class="sxs-lookup"><span data-stu-id="ce57c-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="ce57c-123">De som er bokført 15. desember 2016 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="ce57c-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="ce57c-124">Enten/eller</span><span class="sxs-lookup"><span data-stu-id="ce57c-124">Either/or</span></span>|<span data-ttu-id="ce57c-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="ce57c-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="ce57c-126">De som er bokført 15. eller 16. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="ce57c-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="ce57c-127">Hvis det er bokført poster begge dagene, vises alle postene.</span><span class="sxs-lookup"><span data-stu-id="ce57c-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="ce57c-128">Grunnformene kan også kombineres innbyrdes.</span><span class="sxs-lookup"><span data-stu-id="ce57c-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="ce57c-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ce57c-129">Example</span></span> | <span data-ttu-id="ce57c-130">Tar med poster</span><span class="sxs-lookup"><span data-stu-id="ce57c-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="ce57c-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="ce57c-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="ce57c-132">Poster som enten er bokført 15. desember 2016 eller på datoer mellom og inkludert 1. desember 2016 og 31. mai 2017.</span><span class="sxs-lookup"><span data-stu-id="ce57c-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="ce57c-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="ce57c-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="ce57c-134">Poster som er bokført 14. desember eller tidligere, eller poster som er bokført 30. desember eller senere, det vil si alle poster unntatt de som er bokført på datoer mellom og inkludert 15. og 29. desember.</span><span class="sxs-lookup"><span data-stu-id="ce57c-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="ce57c-135">Vær oppmerksom på at vi har brukt det amerikanske datoformatet MMDDÅÅ her.</span><span class="sxs-lookup"><span data-stu-id="ce57c-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="ce57c-136">Etter hvert som [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tilgjengelig på andre markeder, kan du bruke formatene du er vant med.</span><span class="sxs-lookup"><span data-stu-id="ce57c-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="ce57c-137">Bruke datoformler</span><span class="sxs-lookup"><span data-stu-id="ce57c-137">Using Date Formulas</span></span>
<span data-ttu-id="ce57c-138">En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer.</span><span class="sxs-lookup"><span data-stu-id="ce57c-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="ce57c-139">Du kan angi datoformler i forskjellige datoberegningsfelt og i gjentakende intervallfelt i gjentakende kladder.</span><span class="sxs-lookup"><span data-stu-id="ce57c-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="ce57c-140">Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag.</span><span class="sxs-lookup"><span data-stu-id="ce57c-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="ce57c-141">Hvis du for eksempel angir **1U**, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert.</span><span class="sxs-lookup"><span data-stu-id="ce57c-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="ce57c-142">Hvis du vil angi en periode på sju dager (én sann uke), inkludert periodens startdato, må du angi **6D** eller **1U\-1D**.</span><span class="sxs-lookup"><span data-stu-id="ce57c-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="ce57c-143">Her kommer det noen eksempler på hvordan datoformler kan brukes:</span><span class="sxs-lookup"><span data-stu-id="ce57c-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="ce57c-144">Datoformelen i gjentakelsesintervallfeltet i gjentakelseskladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="ce57c-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="ce57c-145">Datoformelen i feltet **Respittid** for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen (eller fra forfallsdato for forrige purring) før det kan opprettes en purring.</span><span class="sxs-lookup"><span data-stu-id="ce57c-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="ce57c-146">Datoformelen i feltet **Beregning av forfallsdato** angir hvordan forfallsdatoen i purringen beregnes.</span><span class="sxs-lookup"><span data-stu-id="ce57c-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="ce57c-147">Formelen for datoberegning kan inneholde opptil 20 tegn, både tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="ce57c-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="ce57c-148">Du kan bruke følgende bokstaver, som er forkortelser for tidsangivelser:</span><span class="sxs-lookup"><span data-stu-id="ce57c-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="ce57c-149">Bokstav</span><span class="sxs-lookup"><span data-stu-id="ce57c-149">Letter</span></span>  |  <span data-ttu-id="ce57c-150">Tidsspesifisering</span><span class="sxs-lookup"><span data-stu-id="ce57c-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="ce57c-151">U</span><span class="sxs-lookup"><span data-stu-id="ce57c-151">C</span></span>|<span data-ttu-id="ce57c-152">Løpende</span><span class="sxs-lookup"><span data-stu-id="ce57c-152">Current</span></span>|
|<span data-ttu-id="ce57c-153">D</span><span class="sxs-lookup"><span data-stu-id="ce57c-153">D</span></span>|<span data-ttu-id="ce57c-154">Dag\(er\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-154">Day\(s\)</span></span>|
|<span data-ttu-id="ce57c-155">V</span><span class="sxs-lookup"><span data-stu-id="ce57c-155">W</span></span>|<span data-ttu-id="ce57c-156">Uke\(r\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-156">Week\(s\)</span></span>|
|<span data-ttu-id="ce57c-157">M</span><span class="sxs-lookup"><span data-stu-id="ce57c-157">M</span></span>|<span data-ttu-id="ce57c-158">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-158">Month\(s\)</span></span>|
|<span data-ttu-id="ce57c-159">K</span><span class="sxs-lookup"><span data-stu-id="ce57c-159">Q</span></span>|<span data-ttu-id="ce57c-160">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="ce57c-161">Å</span><span class="sxs-lookup"><span data-stu-id="ce57c-161">Y</span></span>|<span data-ttu-id="ce57c-162">År\(\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-162">Year\(s\)</span></span>|

<span data-ttu-id="ce57c-163">Du kan opprette datoformler på tre måter.</span><span class="sxs-lookup"><span data-stu-id="ce57c-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="ce57c-164">Eksempelet nedenfor viser hvordan **C** brukes, for løpende, og en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="ce57c-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="ce57c-165">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="ce57c-165">Expression</span></span>  |  <span data-ttu-id="ce57c-166">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce57c-167">LU</span><span class="sxs-lookup"><span data-stu-id="ce57c-167">CW</span></span>|<span data-ttu-id="ce57c-168">Løpende uke</span><span class="sxs-lookup"><span data-stu-id="ce57c-168">Current week</span></span>|
|<span data-ttu-id="ce57c-169">NM</span><span class="sxs-lookup"><span data-stu-id="ce57c-169">CM</span></span>|<span data-ttu-id="ce57c-170">Løpende måned</span><span class="sxs-lookup"><span data-stu-id="ce57c-170">Current month</span></span>|

<span data-ttu-id="ce57c-171">Eksempelet nedenfor viser hvordan et tall og en tidsangivelse brukes.</span><span class="sxs-lookup"><span data-stu-id="ce57c-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="ce57c-172">Et tall kan ikke være større enn 9999.</span><span class="sxs-lookup"><span data-stu-id="ce57c-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="ce57c-173">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="ce57c-173">Expression</span></span>  |  <span data-ttu-id="ce57c-174">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce57c-175">10D</span><span class="sxs-lookup"><span data-stu-id="ce57c-175">10D</span></span>|<span data-ttu-id="ce57c-176">10 dager fra i dag</span><span class="sxs-lookup"><span data-stu-id="ce57c-176">10 days from today</span></span>|
|<span data-ttu-id="ce57c-177">2U</span><span class="sxs-lookup"><span data-stu-id="ce57c-177">2W</span></span>|<span data-ttu-id="ce57c-178">2 uker fra i dag</span><span class="sxs-lookup"><span data-stu-id="ce57c-178">2 weeks from today</span></span>|

<span data-ttu-id="ce57c-179">Eksempelet nedenfor viser hvordan et en tidsangivelse og et tall brukes.</span><span class="sxs-lookup"><span data-stu-id="ce57c-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="ce57c-180">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="ce57c-180">Expression</span></span>  |  <span data-ttu-id="ce57c-181">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce57c-182">D10</span><span class="sxs-lookup"><span data-stu-id="ce57c-182">D10</span></span>|<span data-ttu-id="ce57c-183">Den neste 10. dag av en måned</span><span class="sxs-lookup"><span data-stu-id="ce57c-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="ce57c-184">UD4</span><span class="sxs-lookup"><span data-stu-id="ce57c-184">WD4</span></span>|<span data-ttu-id="ce57c-185">Neste 4. dag av en uke \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="ce57c-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="ce57c-186">Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="ce57c-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="ce57c-187">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="ce57c-187">Expression</span></span>  |  <span data-ttu-id="ce57c-188">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce57c-189">LM\+10D</span><span class="sxs-lookup"><span data-stu-id="ce57c-189">CM\+10D</span></span>|<span data-ttu-id="ce57c-190">Løpende måned \+10 dager</span><span class="sxs-lookup"><span data-stu-id="ce57c-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="ce57c-191">Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="ce57c-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="ce57c-192">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="ce57c-192">Expression</span></span>  |  <span data-ttu-id="ce57c-193">Betyr</span><span class="sxs-lookup"><span data-stu-id="ce57c-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce57c-194">-1Å</span><span class="sxs-lookup"><span data-stu-id="ce57c-194">-1Y</span></span>|<span data-ttu-id="ce57c-195">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="ce57c-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="ce57c-196">Hvis plasseringen bruker en hovedkalender, tolkes datoformelen du angir, for eksempel i feltet **Leveringstid**, i henhold til arbeidsdager fra kalenderen.</span><span class="sxs-lookup"><span data-stu-id="ce57c-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="ce57c-197">For eksempel betyr **1U** sju virkedager.</span><span class="sxs-lookup"><span data-stu-id="ce57c-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce57c-198">Se også</span><span class="sxs-lookup"><span data-stu-id="ce57c-198">See Also</span></span>
<span data-ttu-id="ce57c-199">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce57c-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ce57c-200">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="ce57c-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="ce57c-201">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="ce57c-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

