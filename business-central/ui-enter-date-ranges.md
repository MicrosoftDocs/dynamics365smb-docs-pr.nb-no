---
title: Angi datoer og klokkeslett i Business Central | Microsoft-dokumentasjon
description: "Finn ut hvordan du angir datoer og klokkeslett, inkludert ulike produktivitetstips som snarveier, uttrykk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8717d60a8449ca300eaf9c1a5c4b137ea1a1a247
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="5d9bf-104">Arbeide med datoer og klokkeslett i kalenderen</span><span class="sxs-lookup"><span data-stu-id="5d9bf-104">Working with Calendar Dates and Times</span></span>
[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="5d9bf-105">tilbyr flere måter å angi datoer og klokkeslett på, inkludert avanserte funksjoner som fremskynder dataregistrering eller hjelper deg med å skrive sammensatte kalenderuttrykk.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="5d9bf-106">Det finnes ulike steder i programmet der du kan angi dato og klokkeslett i feltene.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="5d9bf-107">Du kan for eksempel angi leveringsdatoen på en ordre.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="5d9bf-108">Når du filtrerer lister eller rapportdata, kan du angi datoer og klokkeslett for å finne dataene du er interessert i.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="5d9bf-109">Kontrollere innstillinger for region og språk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-109">Check your region and language settings</span></span>
<span data-ttu-id="5d9bf-110">Siden [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central") angir **Region** og **Språk** som er brukt i programmet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="5d9bf-111">Disse innstillingene påvirker hvordan du angir dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="5d9bf-112">**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="5d9bf-113">For datomønstre som involverer ord, må ordene du bruker, samsvare med **Språk**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="5d9bf-114">bruker det gregorianske kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->
## <a name="entering-dates"></a><span data-ttu-id="5d9bf-115">Sette inn datoer</span><span class="sxs-lookup"><span data-stu-id="5d9bf-115">Entering Dates</span></span>
<span data-ttu-id="5d9bf-116">I et datofelt kan du angi en dato med standardformatet for regionsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="5d9bf-117">Ulike regioner kan bruke ulike skilletegn mellom dager, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="5d9bf-118">Enkelte regioner bruker for eksempel streker (mm-dd-åååå) og andre bruker skråstreker (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="5d9bf-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="5d9bf-119">Du kan imidlertid bruke alle skilletegn, også mellomrom, og datoen endres automatisk til skilletegnene som samsvarer med din region.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="5d9bf-120">Merk at ut formatet for å vise datoer i trykte rapporter eller dokumenter sendt via e-post, ikke påvirkes av ditt personlige valg av regioninnstilling.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="5d9bf-121">Hvis du vil arbeide mer effektivt med datoer og klokkeslett, kan du bruke metodene eller formatene som er beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="5d9bf-122">Plukke datoer fra kalenderen</span><span class="sxs-lookup"><span data-stu-id="5d9bf-122">Picking dates from the calendar</span></span>
<span data-ttu-id="5d9bf-123">Alle felt som viser et kalenderikonet, kan angis ved hjelp kalenderdatovelgeren.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="5d9bf-124">Aktiver kalenderikonet for å vise kalenderdatovelgeren, eller trykk Ctrl+Hjem i feltet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="5d9bf-125">![Datofelt](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="5d9bf-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="5d9bf-126">Se også [Hurtigtaster i kalenderdatovelgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="today"></a><span data-ttu-id="5d9bf-127">I dag</span><span class="sxs-lookup"><span data-stu-id="5d9bf-127">Today</span></span>
<span data-ttu-id="5d9bf-128">Skriv inn ordet for `today`, på språket som er angitt av **Språk**-innstillingen, som angir datoen til den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-128">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="5d9bf-129">I stedet for å skrive inn hele ordet kan du angi en del av ordet fra begynnelsen, som `t` eller `tod`, forutsatt at det ikke er også begynnelsen av et annet ord.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-129">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="5d9bf-130">Mønsteret dag\-uke\-årn</span><span class="sxs-lookup"><span data-stu-id="5d9bf-130">Day\-week\-year pattern</span></span>
<span data-ttu-id="5d9bf-131">Du kan angi en dato som en ukedag etterfulgt av et ukenummer og eventyelt et år.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-131">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="5d9bf-132">For eksempel `Mon25` eller `mon25` betyr mandag i uke 25.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-132">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="5d9bf-133">Hvis du ikke angir et år, brukes året i arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-133">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="5d9bf-134">I stedet for å angi hele ordet for ukedagen, kan du angi en del av ord fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-134">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="5d9bf-135">Hvis det oppstår konflikter (som med `s`, som kan være søndag), dagene evalueres i henhold til regioninnstillingen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-135">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="5d9bf-136">Inndataene vurderes først mot `workdate` og `today`, så husk dette når du forkorter.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-136">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="5d9bf-137">For eksempel `t` betyr allerede dagens, slik at det ikke betyr tirsdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-137">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="5d9bf-138">Ukenummererplanen er alltid ISO 8601, der uke 1 er uken med 4 januar i seg, eller uken med den første torsdagen i året.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-138">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="5d9bf-139">Tallmønstre</span><span class="sxs-lookup"><span data-stu-id="5d9bf-139">Digit patterns</span></span>
<span data-ttu-id="5d9bf-140">I et datofelt kan du angi to, fire, seks eller åtte tall:</span><span class="sxs-lookup"><span data-stu-id="5d9bf-140">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="5d9bf-141">Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-141">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="5d9bf-142">Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-142">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="5d9bf-143">Rekkefølgen på dag og måned avhenger av regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-143">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="5d9bf-144">Selv om dine regioninnstillingene dine har året før dag og måned, tolkes fire sifre som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-144">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="5d9bf-145">Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-145">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="current-work-date"></a><span data-ttu-id="5d9bf-146">Gjeldende arbeidsdato</span><span class="sxs-lookup"><span data-stu-id="5d9bf-146">Current work date</span></span>
<span data-ttu-id="5d9bf-147">Arbeidsdatofunksjonen lar deg registrere transaksjoner med en dato som er forskjellig fra den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-147">The work date feature allows you to record transations using a date that is different from the current date.</span></span>

<span data-ttu-id="5d9bf-148">Ordet for "arbeidsdato"på språket som er angitt av **Språk**-innstillingen setter datoen til arbeidsdatoen som er angitt i på siden [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central").</span><span class="sxs-lookup"><span data-stu-id="5d9bf-148">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="5d9bf-149">I stedet for å angi hele ordet, kan du angi en del av ord fra begynnelsen, for eksempel "a" eller "arbeid".</span><span class="sxs-lookup"><span data-stu-id="5d9bf-149">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="5d9bf-150">Hvis du ikke har definert en arbeidsdato, vil den gjeldende datoen bli brukt som arbeidsdato.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-150">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="5d9bf-151">Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-151">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="5d9bf-152">Se også [Endre grunnleggende innstillinger, for eksempel arbeidsdatoen](ui-change-basic-settings.md#work-date)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-152">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date)</span></span>

### <a name="closing-date"></a><span data-ttu-id="5d9bf-153">Lukkedato</span><span class="sxs-lookup"><span data-stu-id="5d9bf-153">Closing Date</span></span>
<span data-ttu-id="5d9bf-154">Når du avslutter et regnskapsår, kan du bruke avslutningsdatoer til å indikere at en post er en avslutningspost.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-154">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="5d9bf-155">En avslutningsdato ligger teknisk sett mellom to datoer, for eksempel mellom 31. desember og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-155">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="5d9bf-156">Hvis en dato skal være en avslutningsdato, setter du `C` rett foran datoen, for eksempel `C123101`:</span><span class="sxs-lookup"><span data-stu-id="5d9bf-156">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="5d9bf-157">Dette kan brukes sammen alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-157">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="5d9bf-158">Eksempler</span><span class="sxs-lookup"><span data-stu-id="5d9bf-158">Examples</span></span>
<span data-ttu-id="5d9bf-159">Tabellen nedenfor inneholder eksempler på datoer som bruker alle formater.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-159">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="5d9bf-160">Det antar regioninnstillinger som formaterer datoer i henhold til: **år.måned.dag.**, en uke som starter på mandag, og engelsk språk.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-160">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="5d9bf-161">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-161">**Entry**</span></span>      |<span data-ttu-id="5d9bf-162">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-162">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="5d9bf-163">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-163">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="5d9bf-164">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-164">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="5d9bf-165">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-165">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="5d9bf-166">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-166">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="5d9bf-167">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-167">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="5d9bf-168">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-168">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="5d9bf-169">arbeidsdato år.arbeidsdato måned.11.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-169">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="5d9bf-170">arbeidsdato år.11.12</span><span class="sxs-lookup"><span data-stu-id="5d9bf-170">work date year.11.12.</span></span>|
|<span data-ttu-id="5d9bf-171">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-171">`t` or `today`</span></span>|<span data-ttu-id="5d9bf-172">dagens dato</span><span class="sxs-lookup"><span data-stu-id="5d9bf-172">today's date</span></span>|
|<span data-ttu-id="5d9bf-173">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-173">`w` or `workdate`</span></span>|<span data-ttu-id="5d9bf-174">arbeidsdatoen</span><span class="sxs-lookup"><span data-stu-id="5d9bf-174">the working date</span></span>|
|<span data-ttu-id="5d9bf-175">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-175">`m` or `Monday`</span></span>|<span data-ttu-id="5d9bf-176">Mandag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="5d9bf-176">Monday of the work date week</span></span>|
|<span data-ttu-id="5d9bf-177">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-177">`tu` or `Tuesday`</span></span>|<span data-ttu-id="5d9bf-178">Tirsdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="5d9bf-178">Tuesday of the work date week</span></span>|
|<span data-ttu-id="5d9bf-179">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-179">`sa` or `Saturday`</span></span>|<span data-ttu-id="5d9bf-180">Lørdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="5d9bf-180">Saturday of the work date week</span></span>|
|<span data-ttu-id="5d9bf-181">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-181">`s` or `Sunday`</span></span>|<span data-ttu-id="5d9bf-182">Søndag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="5d9bf-182">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="5d9bf-183">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="5d9bf-183">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="5d9bf-184">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="5d9bf-184">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="5d9bf-185">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="5d9bf-185">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="5d9bf-186">Angi intervaller</span><span class="sxs-lookup"><span data-stu-id="5d9bf-186">Setting Ranges</span></span>
<span data-ttu-id="5d9bf-187">I lister, totaler eller rapporter kan du definere filtre på datoer, klokkeslett og datoer og klokkeslett som inneholder en startverdi og eventuelt en sluttverdi, for å vise bare dataene i dette intervallet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-187">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="5d9bf-188">Standardreglene gjelder for angivelse av datointervaller.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-188">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="5d9bf-189">**Betyr**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-189">**Meaning**</span></span>|<span data-ttu-id="5d9bf-190">**Eksempeluttrykk (dato)**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-190">**Sample expression (Date)**</span></span>|<span data-ttu-id="5d9bf-191">**Data som er inkludert i filteret**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-191">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="5d9bf-192">Intervall</span><span class="sxs-lookup"><span data-stu-id="5d9bf-192">Interval</span></span>|<span data-ttu-id="5d9bf-193">`12 15 00..01 15 01`  \n`..12 15 00`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-193">`12 15 00..01 15 01`  \n`..12 15 00`</span></span>|<span data-ttu-id="5d9bf-194">Poster med dato fra og med 15.12.01 til og med 15.01.00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-194">Records with dates between and including 12 15 00 and 01 15 01.</span></span>  <span data-ttu-id="5d9bf-195">\nPoster med datoer 15.12.00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-195">\nRecords with dates of 12 15 00 or earlier.</span></span>|
|<span data-ttu-id="5d9bf-196">Enten/eller</span><span class="sxs-lookup"><span data-stu-id="5d9bf-196">Either/or</span></span>|<span data-ttu-id="5d9bf-197">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-197">\`12 15 00</span></span>|<span data-ttu-id="5d9bf-198">12 16 00\`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-198">12 16 00\`</span></span>|<span data-ttu-id="5d9bf-199">Poster med datoer enten 15.12.00 eller 16.12.00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-199">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="5d9bf-200">Hvis det er poster med begge datoer på begge dager, blir alle vist.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-200">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="5d9bf-201">Kombinasjon</span><span class="sxs-lookup"><span data-stu-id="5d9bf-201">Combination</span></span>|<span data-ttu-id="5d9bf-202">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-202">\`12 15 00</span></span>|<span data-ttu-id="5d9bf-203">12 01 00..12 10 00`  \n`..12 14 00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-203">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="5d9bf-204">12 30 00..\`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-204">12 30 00..\`</span></span>|<span data-ttu-id="5d9bf-205">Poster med datoer 15.12.00 eller fra og med 01.12.00 til og med 10.12.00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-205">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="5d9bf-206">\nPoster med datoer 14.12.00 eller tidligere, eller datoer 30.12.00 eller senere, det vil si alle poster unntatt poster med datoer mellom og 15.12.00 og 29.12.00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-206">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="5d9bf-207">Du kan bruke ethvert gyldig format i datointervallfiltre.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-207">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="5d9bf-208">For eksempel `mon14 3..t 4p` brukt på en dato- og klokkeslettfelt resulterer i et filtre fra 03:00 mandag i uke 14 i det gjeldende arbeidsdatoåret, inkludert til dagens dato klokken 16:00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-208">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>


## <a name="using-date-formulas"></a><span data-ttu-id="5d9bf-209">Bruke datoformler</span><span class="sxs-lookup"><span data-stu-id="5d9bf-209">Using Date Formulas</span></span>
<span data-ttu-id="5d9bf-210">En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-210">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="5d9bf-211">Du kan angi datoformler i forskjellige datoberegningsfelt eller filtre.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-211">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="5d9bf-212">Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-212">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="5d9bf-213">Hvis du for eksempel angir `1W`, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-213">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="5d9bf-214">Hvis du vil angi en periode på sju dager \(én sann uke\), inkludert periodens startdato, må du angi `6D` eller `1W-1D`.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-214">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="5d9bf-215">Her kommer det noen eksempler på hvordan datoformler kan brukes:</span><span class="sxs-lookup"><span data-stu-id="5d9bf-215">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="5d9bf-216">Datoformelen i gjentakelsesintervallfeltet i gjentakelseskladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-216">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="5d9bf-217">Datoformelen i feltet **Respittid** for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen \(eller fra forrige purringsdato\) før det kan opprettes en purring.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-217">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="5d9bf-218">Datoformelen i feltet **Beregning av forfallsdato** angir hvordan forfallsdatoen i purringen beregnes.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-218">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="5d9bf-219">Datoformelen kan inneholde opptil 20 tegn, både tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-219">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="5d9bf-220">Du kan bruke følgende bokstaver, som er forkortelser for kalenderenheter:</span><span class="sxs-lookup"><span data-stu-id="5d9bf-220">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="5d9bf-221">Bokstav</span><span class="sxs-lookup"><span data-stu-id="5d9bf-221">Letter</span></span>  |  <span data-ttu-id="5d9bf-222">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-222">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="5d9bf-223">Løpende</span><span class="sxs-lookup"><span data-stu-id="5d9bf-223">Current</span></span>|
|`D`|<span data-ttu-id="5d9bf-224">Dag\(er\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-224">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="5d9bf-225">Uke\(r\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-225">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="5d9bf-226">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-226">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="5d9bf-227">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-227">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="5d9bf-228">År\(\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-228">Year\(s\)</span></span>|

<span data-ttu-id="5d9bf-229">Du kan opprette datoformler på tre måter.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-229">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="5d9bf-230">Eksempelet nedenfor viser hvordan `C` brukes, for løpende, og en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-230">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="5d9bf-231">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-231">Expression</span></span>  |  <span data-ttu-id="5d9bf-232">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-232">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="5d9bf-233">Løpende uke</span><span class="sxs-lookup"><span data-stu-id="5d9bf-233">Current week</span></span>|
|`CM`|<span data-ttu-id="5d9bf-234">Løpende måned</span><span class="sxs-lookup"><span data-stu-id="5d9bf-234">Current month</span></span>|

<span data-ttu-id="5d9bf-235">Eksempelet nedenfor viser hvordan et tall og en tidsangivelse brukes.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-235">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="5d9bf-236">Et tall kan ikke være større enn 9999.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-236">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="5d9bf-237">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-237">Expression</span></span>  |  <span data-ttu-id="5d9bf-238">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-238">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="5d9bf-239">10 dager fra i dag</span><span class="sxs-lookup"><span data-stu-id="5d9bf-239">10 days from today</span></span>|
|`2W`|<span data-ttu-id="5d9bf-240">2 uker fra i dag</span><span class="sxs-lookup"><span data-stu-id="5d9bf-240">2 weeks from today</span></span>|

<span data-ttu-id="5d9bf-241">Eksempelet nedenfor viser hvordan et en tidsangivelse og et tall brukes.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-241">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="5d9bf-242">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-242">Expression</span></span>  |  <span data-ttu-id="5d9bf-243">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-243">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="5d9bf-244">Den neste 10. dag av en måned</span><span class="sxs-lookup"><span data-stu-id="5d9bf-244">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="5d9bf-245">Neste 4. dag av en uke \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-245">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="5d9bf-246">Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-246">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="5d9bf-247">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-247">Expression</span></span>  |  <span data-ttu-id="5d9bf-248">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-248">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="5d9bf-249">Løpende måned \+10 dager</span><span class="sxs-lookup"><span data-stu-id="5d9bf-249">Current month \+ 10 days</span></span>|

<span data-ttu-id="5d9bf-250">Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-250">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="5d9bf-251">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="5d9bf-251">Expression</span></span>  |  <span data-ttu-id="5d9bf-252">Betyr</span><span class="sxs-lookup"><span data-stu-id="5d9bf-252">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="5d9bf-253">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="5d9bf-253">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="5d9bf-254">Hvis plasseringen bruker en hovedkalender, tolkes datoformelen du angir, for eksempel i feltet **Leveringstid**, i henhold til arbeidsdager fra kalenderen.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-254">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="5d9bf-255">For eksempel betyr `1W` sju virkedager.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-255">For example, `1W`  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="5d9bf-256">Angi klokkeslett</span><span class="sxs-lookup"><span data-stu-id="5d9bf-256">Entering Times</span></span>
<span data-ttu-id="5d9bf-257">Når du angir tidspunkt, kan du sette inn alle skilletegn (ikke mellomrom) mellom enheter, men hvis du bruker doble sifre for hver enhet opptil millisekunder, er det ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-257">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="5d9bf-258">Du trenger bare skrive de største enheter som du vil ha; resten settes til null.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-258">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="5d9bf-259">Du kan eventuelt utelate AM-PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-259">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="5d9bf-260">Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-260">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="5d9bf-261">Det antar regioninnstillinger som formaterer tidspunkt i henhold til: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-261">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="5d9bf-262">og bruker AM- og PM-indikatorer for henholdsvis "AM" og "PM".</span><span class="sxs-lookup"><span data-stu-id="5d9bf-262">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="5d9bf-263">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-263">**Entry**</span></span>      |<span data-ttu-id="5d9bf-264">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-264">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="5d9bf-265">05:23:17</span><span class="sxs-lookup"><span data-stu-id="5d9bf-265">05:23:17</span></span>|
|`5`|<span data-ttu-id="5d9bf-266">05:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-266">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="5d9bf-267">05:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-267">05:00:00</span></span>|
|`5P`|<span data-ttu-id="5d9bf-268">17:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-268">17:00:00</span></span>|
|`12`|<span data-ttu-id="5d9bf-269">12:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-269">12:00:00</span></span>|
|`12A`|<span data-ttu-id="5d9bf-270">00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-270">00:00:00</span></span>|
|`12P`|<span data-ttu-id="5d9bf-271">12:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-271">12:00:00</span></span>|
|`17`|<span data-ttu-id="5d9bf-272">17:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-272">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="5d9bf-273">05:30:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-273">05:30:00</span></span>|
|`0530`|<span data-ttu-id="5d9bf-274">05:30:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-274">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="5d9bf-275">05:30:05</span><span class="sxs-lookup"><span data-stu-id="5d9bf-275">05:30:05</span></span>|
|`053005`|<span data-ttu-id="5d9bf-276">05:30:05</span><span class="sxs-lookup"><span data-stu-id="5d9bf-276">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="5d9bf-277">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="5d9bf-277">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="5d9bf-278">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="5d9bf-278">05:30:05.05</span></span>|

<span data-ttu-id="5d9bf-279">Vær oppmerksom på at millisekunder tolkes som desimalformat.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-279">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="5d9bf-280">Derfor betyr både `3`, `30` og `300` 300 millisekunder, mens `03` betyr `30` og `003` betyr 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-280">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="5d9bf-281">Du kan ikke bruke `24:00` til å angi midnatt eller bruke en verdi som er større enn 24:00.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-281">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="5d9bf-282">Ordet for tidspunkt på språket som brukes av [!INCLUDE[d365fin](includes/d365fin_long_md.md)], evalueres etter gjeldende dato og klokkeslett på datamaskinen eller mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-282">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="5d9bf-283">Du kan angi en del av ordet, fra begynnelsen, som for eksempel `t` eller `TIM`.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-283">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="5d9bf-284">Angi kombinerte datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="5d9bf-284">Entering combined Dates and Times</span></span>
<span data-ttu-id="5d9bf-285">Når du angir dato og klokkeslett, som er en dato og klokkeslett kombinert i ett felt, må du angi et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-285">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="5d9bf-286">Datodelen kan bare inneholde mellomrom i form av det offisielle datoskilletegnet i regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-286">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="5d9bf-287">Klokkeslettet kan inneholde mellomrom rundt AM/PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-287">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="5d9bf-288">Det er også mulig å angi bare en dato i feltet for dato og klokkeslett, men det er ikke mulig å angi bare et klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-288">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="5d9bf-289">Tabellen nedenfor inneholder noen eksempler på kombinasjoner av dato/klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-289">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="5d9bf-290">Regioninnstillingene i eksemplene viser datoer i formatet dag\-måned\-år ved hjelp av AM/PM-angivelse, engelsk språk og søndag som start på uken.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-290">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="5d9bf-291">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-291">**Entry**</span></span>      |<span data-ttu-id="5d9bf-292">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-292">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="5d9bf-293">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="5d9bf-293">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="5d9bf-294">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="5d9bf-294">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="5d9bf-295">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-295">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="5d9bf-296">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-296">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="5d9bf-297">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-297">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="5d9bf-298">11\-arbeidsdatomåned\-arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-298">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="5d9bf-299">11\-12\-arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-299">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="5d9bf-300">`t` eller `today`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-300">`t` or `today`</span></span>|<span data-ttu-id="5d9bf-301">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-301">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="5d9bf-302">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-302">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="5d9bf-303">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="5d9bf-303">today's date 03:03:03</span></span>|
|<span data-ttu-id="5d9bf-304">`w` eller `workdate`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-304">`w` or `workdate`</span></span>|<span data-ttu-id="5d9bf-305">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-305">the working date 00:00:00</span></span>|
|<span data-ttu-id="5d9bf-306">`m` eller `Monday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-306">`m` or `Monday`</span></span>|<span data-ttu-id="5d9bf-307">Mandag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-307">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5d9bf-308">`tu` eller `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-308">`tu` or `Tuesday`</span></span>|<span data-ttu-id="5d9bf-309">Tirsdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-309">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5d9bf-310">`sa` eller `Saturday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-310">`sa` or `Saturday`</span></span>|<span data-ttu-id="5d9bf-311">Lørdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-311">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="5d9bf-312">`s` eller `Sunday`</span><span class="sxs-lookup"><span data-stu-id="5d9bf-312">`s` or `Sunday`</span></span>|<span data-ttu-id="5d9bf-313">Søndag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-313">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="5d9bf-314">Tirsdag i arbeidsdatouken 10:30:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-314">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="5d9bf-315">Tirsdag i arbeidsdatouken 03:03:03</span><span class="sxs-lookup"><span data-stu-id="5d9bf-315">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="5d9bf-316">Tirsdag i uke 23 i arbeidsdatoåret, gjeldende klokkeslett</span><span class="sxs-lookup"><span data-stu-id="5d9bf-316">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="5d9bf-317">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="5d9bf-317">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="5d9bf-318">I dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="5d9bf-318">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="5d9bf-319">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="5d9bf-319">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="5d9bf-320">Angi varighet</span><span class="sxs-lookup"><span data-stu-id="5d9bf-320">Entering Duration</span></span>
<span data-ttu-id="5d9bf-321">Noen av feltene i programmet representerer en varighet eller mengden som er gått, i stedet for en bestemt dato eller klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-321">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="5d9bf-322">Du angir en varighet som et tall etterfulgt av enheten.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-322">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="5d9bf-323">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-323">Here are some examples.</span></span>

|<span data-ttu-id="5d9bf-324">**Varighet**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-324">**Duration**</span></span>|<span data-ttu-id="5d9bf-325">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="5d9bf-325">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="5d9bf-326">2 timer</span><span class="sxs-lookup"><span data-stu-id="5d9bf-326">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="5d9bf-327">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5d9bf-327">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="5d9bf-328">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5d9bf-328">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="5d9bf-329">1 t 30 min</span><span class="sxs-lookup"><span data-stu-id="5d9bf-329">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="5d9bf-330">2 dager 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="5d9bf-330">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="5d9bf-331">2 dager 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="5d9bf-331">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="5d9bf-332">Du kan også angi et tall, som blir automatisk konvertert til et tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-332">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="5d9bf-333">Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-333">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="5d9bf-334">Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-334">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="5d9bf-335">Tallet `5` konverteres for eksempel til 5 timer hvis enheten er timer.</span><span class="sxs-lookup"><span data-stu-id="5d9bf-335">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="5d9bf-336">Se også</span><span class="sxs-lookup"><span data-stu-id="5d9bf-336">See Also</span></span>
<span data-ttu-id="5d9bf-337">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5d9bf-337">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5d9bf-338">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="5d9bf-338">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="5d9bf-339">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="5d9bf-339">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

