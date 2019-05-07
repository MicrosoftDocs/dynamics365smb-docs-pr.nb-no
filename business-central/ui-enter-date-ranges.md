---
title: Angi datoer og klokkeslett i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du angir datoer og klokkeslett, inkludert ulike produktivitetstips som snarveier, uttrykk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: c7e80edfd796056176d37ad12a56c76e64bb44e6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "932981"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="b925c-104">Arbeide med datoer og klokkeslett i kalenderen</span><span class="sxs-lookup"><span data-stu-id="b925c-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="b925c-105">tilbyr flere måter å angi datoer og klokkeslett på, inkludert avanserte funksjoner som fremskynder dataregistrering eller hjelper deg med å skrive sammensatte kalenderuttrykk.</span><span class="sxs-lookup"><span data-stu-id="b925c-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="b925c-106">Det finnes ulike steder i programmet der du kan angi dato og klokkeslett i feltene.</span><span class="sxs-lookup"><span data-stu-id="b925c-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="b925c-107">Du kan for eksempel angi leveringsdatoen på en ordre.</span><span class="sxs-lookup"><span data-stu-id="b925c-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="b925c-108">Når du filtrerer lister eller rapportdata, kan du angi datoer og klokkeslett for å finne dataene du er interessert i.</span><span class="sxs-lookup"><span data-stu-id="b925c-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="b925c-109">Kontrollere innstillinger for region og språk</span><span class="sxs-lookup"><span data-stu-id="b925c-109">Check your region and language settings</span></span>

<span data-ttu-id="b925c-110">Siden [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central") angir **Region** og **Språk** som er brukt i programmet.</span><span class="sxs-lookup"><span data-stu-id="b925c-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="b925c-111">Disse innstillingene påvirker hvordan du angir dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b925c-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="b925c-112">**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres.</span><span class="sxs-lookup"><span data-stu-id="b925c-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="b925c-113">For datomønstre som involverer ord, må ordene du bruker, samsvare med **Språk**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="b925c-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="b925c-114">bruker det gregorianske kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="b925c-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="b925c-115">Sette inn datoer</span><span class="sxs-lookup"><span data-stu-id="b925c-115">Entering Dates</span></span>

<span data-ttu-id="b925c-116">I et datofelt kan du angi en dato med standardformatet for regionsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="b925c-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="b925c-117">Ulike regioner kan bruke ulike skilletegn mellom dager, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="b925c-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="b925c-118">Enkelte regioner bruker for eksempel streker (mm-dd-åååå) og andre bruker skråstreker (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="b925c-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="b925c-119">Du kan imidlertid bruke alle skilletegn, også mellomrom, og datoen endres automatisk til skilletegnene som samsvarer med din region.</span><span class="sxs-lookup"><span data-stu-id="b925c-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="b925c-120">Merk at ut formatet for å vise datoer i trykte rapporter eller dokumenter sendt via e-post, ikke påvirkes av ditt personlige valg av regioninnstilling.</span><span class="sxs-lookup"><span data-stu-id="b925c-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="b925c-121">Hvis du vil arbeide mer effektivt med datoer og klokkeslett, kan du bruke metodene eller formatene som er beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b925c-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="b925c-122">Plukke datoer fra kalenderen</span><span class="sxs-lookup"><span data-stu-id="b925c-122">Picking dates from the calendar</span></span>

<span data-ttu-id="b925c-123">Alle felt som viser et kalenderikonet, kan angis ved hjelp kalenderdatovelgeren.</span><span class="sxs-lookup"><span data-stu-id="b925c-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="b925c-124">Aktiver kalenderikonet for å vise kalenderdatovelgeren, eller trykk Ctrl+Hjem i feltet.</span><span class="sxs-lookup"><span data-stu-id="b925c-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="b925c-125">![Datofelt](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="b925c-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="b925c-126">Se også [Hurtigtaster i kalenderdatovelgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="b925c-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="b925c-127">Mønsteret dag\-uke\-årn</span><span class="sxs-lookup"><span data-stu-id="b925c-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="b925c-128">Du kan angi en dato som en ukedag etterfulgt av et ukenummer og eventyelt et år.</span><span class="sxs-lookup"><span data-stu-id="b925c-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="b925c-129">For eksempel `Mon25` eller `mon25` betyr mandag i uke 25.</span><span class="sxs-lookup"><span data-stu-id="b925c-129">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="b925c-130">Hvis du ikke angir et år, brukes året i arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b925c-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="b925c-131">I stedet for å angi hele ordet for ukedagen, kan du angi en del av ord fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="b925c-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="b925c-132">Hvis det oppstår konflikter (som med `s`, som kan være søndag), dagene evalueres i henhold til regioninnstillingen.</span><span class="sxs-lookup"><span data-stu-id="b925c-132">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="b925c-133">Inndataene vurderes først mot `workdate` og `today`, så husk dette når du forkorter.</span><span class="sxs-lookup"><span data-stu-id="b925c-133">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="b925c-134">For eksempel `t` betyr allerede dagens, slik at det ikke betyr tirsdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="b925c-134">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="b925c-135">Ukenummererplanen er alltid ISO 8601, der uke 1 er uken med 4 januar i seg, eller uken med den første torsdagen i året.</span><span class="sxs-lookup"><span data-stu-id="b925c-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="b925c-136">Tallmønstre</span><span class="sxs-lookup"><span data-stu-id="b925c-136">Digit patterns</span></span>

<span data-ttu-id="b925c-137">I et datofelt kan du angi to, fire, seks eller åtte tall:</span><span class="sxs-lookup"><span data-stu-id="b925c-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="b925c-138">Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="b925c-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="b925c-139">Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="b925c-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="b925c-140">Rekkefølgen på dag og måned avhenger av regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="b925c-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="b925c-141">Selv om dine regioninnstillingene dine har året før dag og måned, tolkes fire sifre som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="b925c-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="b925c-142">Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.</span><span class="sxs-lookup"><span data-stu-id="b925c-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="b925c-143">I dag</span><span class="sxs-lookup"><span data-stu-id="b925c-143">Today</span></span>

<span data-ttu-id="b925c-144">Skriv inn ordet for `today`, på språket som er angitt av **Språk**-innstillingen, som angir datoen til den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="b925c-144">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="b925c-145">I stedet for å skrive inn hele ordet kan du angi en del av ordet fra begynnelsen, som `t` eller `tod`, forutsatt at det ikke er også begynnelsen av et annet ord.</span><span class="sxs-lookup"><span data-stu-id="b925c-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="b925c-146">Periode</span><span class="sxs-lookup"><span data-stu-id="b925c-146">Period</span></span>

<span data-ttu-id="b925c-147">For å filtrere på en bestemt regnskapsperiode, angi bokstaven `p` eller ordet `period` i datofeltet, etterfulgt av et nummer som identifiserer regnskapsperioden, som `p2` eller `period4`.</span><span class="sxs-lookup"><span data-stu-id="b925c-147">To filter on a specific accounting period, in a date field enter the letter `p`, or the word `period`, followed by a number that identifies the accounting period, like `p2` or `period4`.</span></span> <span data-ttu-id="b925c-148">Regnskapsperioden er relativ til regnskapsåret for gjeldende arbeidsdato som er angitt i ditt rollesenter.</span><span class="sxs-lookup"><span data-stu-id="b925c-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="b925c-149">Hvis for eksempel arbeidsdatoen er **21/03/20**, filtreres `p1` eller bare `p` på den første regnskapsperioden i regnskapsåret 2020 (som for eksempel `01/01/20..01/31/20`).</span><span class="sxs-lookup"><span data-stu-id="b925c-149">For example, if the work date is **03/21/20**, then `p1`, or just `p`, filters on the first accounting period of the fiscal year 2020 (such as `01/01/20..01/31/20`).</span></span> <span data-ttu-id="b925c-150">`p15` filtrerer på den femtende regnskapsperioden fra starten av regnskapsåret 2020 (for eksempel `03/01/21..03/31/21`).</span><span class="sxs-lookup"><span data-stu-id="b925c-150">`p15` filters on the fifteenth accounting period from the start of fiscal year 2020 (such as `03/01/21..03/31/21`).</span></span> 

<span data-ttu-id="b925c-151">Regnskapsperioden er definert på **Regnskapsperioder**-siden.</span><span class="sxs-lookup"><span data-stu-id="b925c-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="b925c-152">Hvis du vil vise eller endre regnskapsperiodene, åpner du siden [her](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="b925c-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="b925c-153">Gjeldende arbeidsdato</span><span class="sxs-lookup"><span data-stu-id="b925c-153">Current work date</span></span>

<span data-ttu-id="b925c-154">Arbeidsdatofunksjonen lar deg registrere transaksjoner med en dato som er forskjellig fra den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="b925c-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="b925c-155">Ordet for "arbeidsdato"på språket som er angitt av **Språk**-innstillingen setter datoen til arbeidsdatoen som er angitt i på siden [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central").</span><span class="sxs-lookup"><span data-stu-id="b925c-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="b925c-156">I stedet for å angi hele ordet, kan du angi en del av ord fra begynnelsen, for eksempel "a" eller "arbeid".</span><span class="sxs-lookup"><span data-stu-id="b925c-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="b925c-157">Hvis du ikke har definert en arbeidsdato, vil den gjeldende datoen bli brukt som arbeidsdato.</span><span class="sxs-lookup"><span data-stu-id="b925c-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="b925c-158">Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b925c-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="b925c-159">Se også [Endre grunnleggende innstillinger, for eksempel arbeidsdatoen](ui-change-basic-settings.md#work-date)</span><span class="sxs-lookup"><span data-stu-id="b925c-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="b925c-160">Lukkedato</span><span class="sxs-lookup"><span data-stu-id="b925c-160">Closing Date</span></span>

<span data-ttu-id="b925c-161">Når du avslutter et regnskapsår, kan du bruke avslutningsdatoer til å indikere at en post er en avslutningspost.</span><span class="sxs-lookup"><span data-stu-id="b925c-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="b925c-162">En avslutningsdato ligger teknisk sett mellom to datoer, for eksempel mellom 31. desember og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="b925c-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="b925c-163">Hvis en dato skal være en avslutningsdato, setter du `C` rett foran datoen, for eksempel `C123101`:</span><span class="sxs-lookup"><span data-stu-id="b925c-163">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="b925c-164">Dette kan brukes sammen alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="b925c-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="b925c-165">Eksempler</span><span class="sxs-lookup"><span data-stu-id="b925c-165">Examples</span></span>

<span data-ttu-id="b925c-166">Tabellen nedenfor inneholder eksempler på datoer som bruker alle formater.</span><span class="sxs-lookup"><span data-stu-id="b925c-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="b925c-167">Det antar regioninnstillinger som formaterer datoer i henhold til: **år.måned.dag.**, en uke som starter på mandag, og engelsk språk.</span><span class="sxs-lookup"><span data-stu-id="b925c-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="b925c-168">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="b925c-168">**Entry**</span></span>      |<span data-ttu-id="b925c-169">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="b925c-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="b925c-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-170">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="b925c-171">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-171">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="b925c-172">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-172">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="b925c-173">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-173">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="b925c-174">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-174">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="b925c-175">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="b925c-175">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="b925c-176">arbeidsdato år.arbeidsdato måned.11.</span><span class="sxs-lookup"><span data-stu-id="b925c-176">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="b925c-177">arbeidsdato år.11.12</span><span class="sxs-lookup"><span data-stu-id="b925c-177">work date year.11.12.</span></span>|
|<span data-ttu-id="b925c-178">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="b925c-178">`t` or `today`</span></span>|<span data-ttu-id="b925c-179">dagens dato</span><span class="sxs-lookup"><span data-stu-id="b925c-179">today's date</span></span>|
|`p4`|<span data-ttu-id="b925c-180">datointervall som inneholder den fjerde regnskapsperioden, for eksempel `04/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="b925c-180">date range that includes the fourth accounting period, such as `04/01/20..04/30/20`</span></span>|
|<span data-ttu-id="b925c-181">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="b925c-181">`w` or `workdate`</span></span>|<span data-ttu-id="b925c-182">arbeidsdatoen</span><span class="sxs-lookup"><span data-stu-id="b925c-182">the working date</span></span>|
|<span data-ttu-id="b925c-183">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="b925c-183">`m` or `Monday`</span></span>|<span data-ttu-id="b925c-184">Mandag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="b925c-184">Monday of the work date week</span></span>|
|<span data-ttu-id="b925c-185">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="b925c-185">`tu` or `Tuesday`</span></span>|<span data-ttu-id="b925c-186">Tirsdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="b925c-186">Tuesday of the work date week</span></span>|
|<span data-ttu-id="b925c-187">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="b925c-187">`sa` or `Saturday`</span></span>|<span data-ttu-id="b925c-188">Lørdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="b925c-188">Saturday of the work date week</span></span>|
|<span data-ttu-id="b925c-189">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="b925c-189">`s` or `Sunday`</span></span>|<span data-ttu-id="b925c-190">Søndag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="b925c-190">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="b925c-191">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="b925c-191">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="b925c-192">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="b925c-192">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="b925c-193">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="b925c-193">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="b925c-194">Angi intervaller</span><span class="sxs-lookup"><span data-stu-id="b925c-194">Setting Ranges</span></span>

<span data-ttu-id="b925c-195">I lister, totaler eller rapporter kan du definere filtre på datoer, klokkeslett og datoer og klokkeslett som inneholder en startverdi og eventuelt en sluttverdi, for å vise bare dataene i dette intervallet.</span><span class="sxs-lookup"><span data-stu-id="b925c-195">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="b925c-196">Standardreglene gjelder for angivelse av datointervaller.</span><span class="sxs-lookup"><span data-stu-id="b925c-196">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="b925c-197">**Betyr**</span><span class="sxs-lookup"><span data-stu-id="b925c-197">**Meaning**</span></span>|<span data-ttu-id="b925c-198">**Eksempeluttrykk (dato)**</span><span class="sxs-lookup"><span data-stu-id="b925c-198">**Sample expression (Date)**</span></span>|<span data-ttu-id="b925c-199">**Data som er inkludert i filteret**</span><span class="sxs-lookup"><span data-stu-id="b925c-199">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="b925c-200">Intervall</span><span class="sxs-lookup"><span data-stu-id="b925c-200">Interval</span></span>|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|<span data-ttu-id="b925c-201">Poster med dato fra og med 15.12.01 til og med 15.01.00.</span><span class="sxs-lookup"><span data-stu-id="b925c-201">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="b925c-202">Poster med datoer 15.12.00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="b925c-202">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="b925c-203">Datointervall som inneholder den andre, tredje eller fjerde regnskapsperioden, for eksempel `01/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="b925c-203">Date range that includes the second, third, and fourth accounting periods, such as `01/01/20..04/30/20`.</span></span>|
|<span data-ttu-id="b925c-204">Enten/eller</span><span class="sxs-lookup"><span data-stu-id="b925c-204">Either/or</span></span>|`12 15 00|12 16 00`|<span data-ttu-id="b925c-205">Poster med datoer enten 15.12.00 eller 16.12.00.</span><span class="sxs-lookup"><span data-stu-id="b925c-205">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="b925c-206">Hvis det er poster med begge datoer på begge dager, blir alle vist.</span><span class="sxs-lookup"><span data-stu-id="b925c-206">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="b925c-207">Kombinasjon</span><span class="sxs-lookup"><span data-stu-id="b925c-207">Combination</span></span>|<span data-ttu-id="b925c-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span><span class="sxs-lookup"><span data-stu-id="b925c-208">`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00..`</span></span>|<span data-ttu-id="b925c-209">Poster med datoer 15.12.00 eller fra og med 01.12.00 til og med 10.12.00.</span><span class="sxs-lookup"><span data-stu-id="b925c-209">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="b925c-210">\nPoster med datoer 14.12.00 eller tidligere, eller datoer 30.12.00 eller senere, det vil si alle poster unntatt poster med datoer mellom og 15.12.00 og 29.12.00.</span><span class="sxs-lookup"><span data-stu-id="b925c-210">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="b925c-211">Du kan bruke ethvert gyldig format i datointervallfiltre.</span><span class="sxs-lookup"><span data-stu-id="b925c-211">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="b925c-212">For eksempel `mon14 3..t 4p` brukt på en dato- og klokkeslettfelt resulterer i et filtre fra 03:00 mandag i uke 14 i det gjeldende arbeidsdatoåret, inkludert til dagens dato klokken 16:00.</span><span class="sxs-lookup"><span data-stu-id="b925c-212">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="b925c-213">Bruke datoformler</span><span class="sxs-lookup"><span data-stu-id="b925c-213">Using Date Formulas</span></span>
<span data-ttu-id="b925c-214">En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer.</span><span class="sxs-lookup"><span data-stu-id="b925c-214">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="b925c-215">Du kan angi datoformler i forskjellige datoberegningsfelt eller filtre.</span><span class="sxs-lookup"><span data-stu-id="b925c-215">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="b925c-216">Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag.</span><span class="sxs-lookup"><span data-stu-id="b925c-216">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="b925c-217">Hvis du for eksempel angir `1W`, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert.</span><span class="sxs-lookup"><span data-stu-id="b925c-217">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="b925c-218">Hvis du vil angi en periode på sju dager \(én sann uke\), inkludert periodens startdato, må du angi `6D` eller `1W-1D`.</span><span class="sxs-lookup"><span data-stu-id="b925c-218">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="b925c-219">Her kommer det noen eksempler på hvordan datoformler kan brukes:</span><span class="sxs-lookup"><span data-stu-id="b925c-219">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="b925c-220">Datoformelen i gjentakelsesintervallfeltet i gjentakelseskladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="b925c-220">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="b925c-221">Datoformelen i feltet **Respittid** for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen \(eller fra forrige purringsdato\) før det kan opprettes en purring.</span><span class="sxs-lookup"><span data-stu-id="b925c-221">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="b925c-222">Datoformelen i feltet **Beregning av forfallsdato** angir hvordan forfallsdatoen i purringen beregnes.</span><span class="sxs-lookup"><span data-stu-id="b925c-222">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="b925c-223">Datoformelen kan inneholde opptil 20 tegn, både tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="b925c-223">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="b925c-224">Du kan bruke følgende bokstaver, som er forkortelser for kalenderenheter:</span><span class="sxs-lookup"><span data-stu-id="b925c-224">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="b925c-225">Bokstav</span><span class="sxs-lookup"><span data-stu-id="b925c-225">Letter</span></span>  |  <span data-ttu-id="b925c-226">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-226">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="b925c-227">Løpende</span><span class="sxs-lookup"><span data-stu-id="b925c-227">Current</span></span>|
|`D`|<span data-ttu-id="b925c-228">Dag\(er\)</span><span class="sxs-lookup"><span data-stu-id="b925c-228">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="b925c-229">Uke\(r\)</span><span class="sxs-lookup"><span data-stu-id="b925c-229">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="b925c-230">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="b925c-230">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="b925c-231">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="b925c-231">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="b925c-232">År\(\)</span><span class="sxs-lookup"><span data-stu-id="b925c-232">Year\(s\)</span></span>|

<span data-ttu-id="b925c-233">Du kan opprette datoformler på tre måter.</span><span class="sxs-lookup"><span data-stu-id="b925c-233">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="b925c-234">Eksempelet nedenfor viser hvordan `C` brukes, for løpende, og en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="b925c-234">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="b925c-235">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="b925c-235">Expression</span></span>  |  <span data-ttu-id="b925c-236">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-236">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="b925c-237">Løpende uke</span><span class="sxs-lookup"><span data-stu-id="b925c-237">Current week</span></span>|
|`CM`|<span data-ttu-id="b925c-238">Løpende måned</span><span class="sxs-lookup"><span data-stu-id="b925c-238">Current month</span></span>|

<span data-ttu-id="b925c-239">Eksempelet nedenfor viser hvordan et tall og en tidsangivelse brukes.</span><span class="sxs-lookup"><span data-stu-id="b925c-239">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="b925c-240">Et tall kan ikke være større enn 9999.</span><span class="sxs-lookup"><span data-stu-id="b925c-240">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="b925c-241">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="b925c-241">Expression</span></span>  |  <span data-ttu-id="b925c-242">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-242">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="b925c-243">10 dager fra i dag</span><span class="sxs-lookup"><span data-stu-id="b925c-243">10 days from today</span></span>|
|`2W`|<span data-ttu-id="b925c-244">2 uker fra i dag</span><span class="sxs-lookup"><span data-stu-id="b925c-244">2 weeks from today</span></span>|

<span data-ttu-id="b925c-245">Eksempelet nedenfor viser hvordan et en tidsangivelse og et tall brukes.</span><span class="sxs-lookup"><span data-stu-id="b925c-245">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="b925c-246">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="b925c-246">Expression</span></span>  |  <span data-ttu-id="b925c-247">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-247">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="b925c-248">Den neste 10. dag av en måned</span><span class="sxs-lookup"><span data-stu-id="b925c-248">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="b925c-249">Neste 4. dag av en uke \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="b925c-249">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="b925c-250">Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="b925c-250">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="b925c-251">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="b925c-251">Expression</span></span>  |  <span data-ttu-id="b925c-252">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-252">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="b925c-253">Løpende måned \+10 dager</span><span class="sxs-lookup"><span data-stu-id="b925c-253">Current month \+ 10 days</span></span>|

<span data-ttu-id="b925c-254">Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="b925c-254">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="b925c-255">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="b925c-255">Expression</span></span>  |  <span data-ttu-id="b925c-256">Betyr</span><span class="sxs-lookup"><span data-stu-id="b925c-256">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="b925c-257">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="b925c-257">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="b925c-258">Hvis plasseringen bruker en hovedkalender, tolkes datoformelen du angir, for eksempel i feltet **Leveringstid**, i henhold til arbeidsdager fra kalenderen.</span><span class="sxs-lookup"><span data-stu-id="b925c-258">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="b925c-259">For eksempel betyr `1W` sju virkedager.</span><span class="sxs-lookup"><span data-stu-id="b925c-259">For example, `1W`  means seven working days.</span></span>
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a><span data-ttu-id="b925c-260">Angi klokkeslett</span><span class="sxs-lookup"><span data-stu-id="b925c-260">Entering Times</span></span>
<span data-ttu-id="b925c-261">Når du angir tidspunkt, kan du sette inn alle skilletegn (ikke mellomrom) mellom enheter, men hvis du bruker doble sifre for hver enhet opptil millisekunder, er det ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b925c-261">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="b925c-262">Du trenger bare skrive de største enheter som du vil ha; resten settes til null.</span><span class="sxs-lookup"><span data-stu-id="b925c-262">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="b925c-263">Du kan eventuelt utelate AM-PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="b925c-263">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="b925c-264">Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="b925c-264">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="b925c-265">Det antar regioninnstillinger som formaterer tidspunkt i henhold til: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="b925c-265">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="b925c-266">og bruker AM- og PM-indikatorer for henholdsvis "AM" og "PM".</span><span class="sxs-lookup"><span data-stu-id="b925c-266">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="b925c-267">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="b925c-267">**Entry**</span></span>      |<span data-ttu-id="b925c-268">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="b925c-268">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="b925c-269">05:23:17</span><span class="sxs-lookup"><span data-stu-id="b925c-269">05:23:17</span></span>|
|`5`|<span data-ttu-id="b925c-270">05:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-270">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="b925c-271">05:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-271">05:00:00</span></span>|
|`5P`|<span data-ttu-id="b925c-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-272">17:00:00</span></span>|
|`12`|<span data-ttu-id="b925c-273">12:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-273">12:00:00</span></span>|
|`12A`|<span data-ttu-id="b925c-274">00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-274">00:00:00</span></span>|
|`12P`|<span data-ttu-id="b925c-275">12:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-275">12:00:00</span></span>|
|`17`|<span data-ttu-id="b925c-276">17:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-276">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="b925c-277">05:30:00</span><span class="sxs-lookup"><span data-stu-id="b925c-277">05:30:00</span></span>|
|`0530`|<span data-ttu-id="b925c-278">05:30:00</span><span class="sxs-lookup"><span data-stu-id="b925c-278">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="b925c-279">05:30:05</span><span class="sxs-lookup"><span data-stu-id="b925c-279">05:30:05</span></span>|
|`053005`|<span data-ttu-id="b925c-280">05:30:05</span><span class="sxs-lookup"><span data-stu-id="b925c-280">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="b925c-281">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="b925c-281">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="b925c-282">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="b925c-282">05:30:05.05</span></span>|

<span data-ttu-id="b925c-283">Vær oppmerksom på at millisekunder tolkes som desimalformat.</span><span class="sxs-lookup"><span data-stu-id="b925c-283">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="b925c-284">Derfor betyr både `3`, `30` og `300` 300 millisekunder, mens `03` betyr `30` og `003` betyr 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="b925c-284">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="b925c-285">Du kan ikke bruke `24:00` til å angi midnatt eller bruke en verdi som er større enn 24:00.</span><span class="sxs-lookup"><span data-stu-id="b925c-285">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="b925c-286">Ordet for tidspunkt på språket som brukes av [!INCLUDE[d365fin](includes/d365fin_long_md.md)], evalueres etter gjeldende dato og klokkeslett på datamaskinen eller mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="b925c-286">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="b925c-287">Du kan angi en del av ordet, fra begynnelsen, som for eksempel `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="b925c-287">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="b925c-288">Angi kombinerte datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="b925c-288">Entering combined Dates and Times</span></span>
<span data-ttu-id="b925c-289">Når du angir dato og klokkeslett, som er en dato og klokkeslett kombinert i ett felt, må du angi et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="b925c-289">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="b925c-290">Datodelen kan bare inneholde mellomrom i form av det offisielle datoskilletegnet i regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="b925c-290">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="b925c-291">Klokkeslettet kan inneholde mellomrom rundt AM/PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="b925c-291">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="b925c-292">Det er også mulig å angi bare en dato i feltet for dato og klokkeslett, men det er ikke mulig å angi bare et klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b925c-292">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="b925c-293">Tabellen nedenfor inneholder noen eksempler på kombinasjoner av dato/klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b925c-293">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="b925c-294">Regioninnstillingene i eksemplene viser datoer i formatet dag\-måned\-år ved hjelp av AM/PM-angivelse, engelsk språk og søndag som start på uken.</span><span class="sxs-lookup"><span data-stu-id="b925c-294">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="b925c-295">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="b925c-295">**Entry**</span></span>      |<span data-ttu-id="b925c-296">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="b925c-296">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="b925c-297">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="b925c-297">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="b925c-298">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="b925c-298">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="b925c-299">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-299">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="b925c-300">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-300">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="b925c-301">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-301">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="b925c-302">11\-arbeidsdatomåned\-arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-302">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="b925c-303">11\-12\-arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-303">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="b925c-304">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="b925c-304">`t` or `today`</span></span>|<span data-ttu-id="b925c-305">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-305">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="b925c-306">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="b925c-306">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="b925c-307">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="b925c-307">today's date 03:03:03</span></span>|
|<span data-ttu-id="b925c-308">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="b925c-308">`w` or `workdate`</span></span>|<span data-ttu-id="b925c-309">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="b925c-309">the working date 00:00:00</span></span>|
|<span data-ttu-id="b925c-310">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="b925c-310">`m` or `Monday`</span></span>|<span data-ttu-id="b925c-311">Mandag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-311">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="b925c-312">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="b925c-312">`tu` or `Tuesday`</span></span>|<span data-ttu-id="b925c-313">Tirsdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-313">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="b925c-314">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="b925c-314">`sa` or `Saturday`</span></span>|<span data-ttu-id="b925c-315">Lørdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-315">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="b925c-316">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="b925c-316">`s` or `Sunday`</span></span>|<span data-ttu-id="b925c-317">Søndag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-317">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="b925c-318">Tirsdag i arbeidsdatouken 10:30:00</span><span class="sxs-lookup"><span data-stu-id="b925c-318">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="b925c-319">Tirsdag i arbeidsdatouken 03:03:03</span><span class="sxs-lookup"><span data-stu-id="b925c-319">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="b925c-320">Tirsdag i uke 23 i arbeidsdatoåret, gjeldende klokkeslett</span><span class="sxs-lookup"><span data-stu-id="b925c-320">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="b925c-321">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="b925c-321">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="b925c-322">I dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="b925c-322">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="b925c-323">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="b925c-323">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="b925c-324">Angi varighet</span><span class="sxs-lookup"><span data-stu-id="b925c-324">Entering Duration</span></span>
<span data-ttu-id="b925c-325">Noen av feltene i programmet representerer en varighet eller mengden som er gått, i stedet for en bestemt dato eller klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b925c-325">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="b925c-326">Du angir en varighet som et tall etterfulgt av enheten.</span><span class="sxs-lookup"><span data-stu-id="b925c-326">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="b925c-327">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="b925c-327">Here are some examples.</span></span>

|<span data-ttu-id="b925c-328">**Varighet**</span><span class="sxs-lookup"><span data-stu-id="b925c-328">**Duration**</span></span>|<span data-ttu-id="b925c-329">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="b925c-329">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="b925c-330">2 timer</span><span class="sxs-lookup"><span data-stu-id="b925c-330">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="b925c-331">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="b925c-331">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="b925c-332">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="b925c-332">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="b925c-333">1 t 30 min</span><span class="sxs-lookup"><span data-stu-id="b925c-333">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="b925c-334">2 dager 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="b925c-334">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="b925c-335">2 dager 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="b925c-335">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="b925c-336">Du kan også angi et tall, som blir automatisk konvertert til et tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="b925c-336">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="b925c-337">Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.</span><span class="sxs-lookup"><span data-stu-id="b925c-337">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="b925c-338">Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.</span><span class="sxs-lookup"><span data-stu-id="b925c-338">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="b925c-339">Tallet `5` konverteres for eksempel til 5 timer hvis enheten er timer.</span><span class="sxs-lookup"><span data-stu-id="b925c-339">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="b925c-340">Se også</span><span class="sxs-lookup"><span data-stu-id="b925c-340">See Also</span></span>
<span data-ttu-id="b925c-341">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b925c-341">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b925c-342">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="b925c-342">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="b925c-343">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="b925c-343">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
