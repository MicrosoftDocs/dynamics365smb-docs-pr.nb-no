---
title: Angi datoer og klokkeslett i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du angir datoer og klokkeslett, inkludert ulike produktivitetstips som snarveier, uttrykk og områder. Filtrer lister eller rapporter ned til en bestemt dato eller tidsperioder.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ff34a7a8a1086b41d2df2a75955017fc82866fb6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194406"
---
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="66600-104">Arbeide med datoer og klokkeslett i kalenderen</span><span class="sxs-lookup"><span data-stu-id="66600-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="66600-105">tilbyr flere måter å angi datoer og klokkeslett på, inkludert avanserte funksjoner som fremskynder dataregistrering eller hjelper deg med å skrive sammensatte kalenderuttrykk.</span><span class="sxs-lookup"><span data-stu-id="66600-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="66600-106">Det finnes ulike steder i programmet der du kan angi dato og klokkeslett i feltene.</span><span class="sxs-lookup"><span data-stu-id="66600-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="66600-107">Du kan for eksempel angi leveringsdatoen på en ordre.</span><span class="sxs-lookup"><span data-stu-id="66600-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="66600-108">Når du filtrerer lister eller rapportdata, kan du angi datoer og klokkeslett for å finne dataene du er interessert i.</span><span class="sxs-lookup"><span data-stu-id="66600-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="66600-109">Kontrollere innstillinger for region og språk</span><span class="sxs-lookup"><span data-stu-id="66600-109">Check your region and language settings</span></span>
<span data-ttu-id="66600-110">Siden **Mine innstillinger** angir **Område** og **Språk** du bruker i programmet.</span><span class="sxs-lookup"><span data-stu-id="66600-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="66600-111">Disse innstillingene påvirker hvordan du angir dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="66600-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="66600-112">**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres.</span><span class="sxs-lookup"><span data-stu-id="66600-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="66600-113">For datomønstre som involverer ord, må ordene du bruker, samsvare med **Språk**-innstillingen.</span><span class="sxs-lookup"><span data-stu-id="66600-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="66600-114">bruker det gregorianske kalendersystemet.</span><span class="sxs-lookup"><span data-stu-id="66600-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="66600-115">Sette inn datoer</span><span class="sxs-lookup"><span data-stu-id="66600-115">Entering Dates</span></span>

<span data-ttu-id="66600-116">I et datofelt kan du angi en dato med standardformatet for regionsinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="66600-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="66600-117">Ulike regioner kan bruke ulike skilletegn mellom dager, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="66600-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="66600-118">Enkelte regioner bruker for eksempel streker (mm-dd-åååå) og andre bruker skråstreker (mm/dd/åååå).</span><span class="sxs-lookup"><span data-stu-id="66600-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="66600-119">Du kan imidlertid bruke alle skilletegn, også mellomrom, og datoen endres automatisk til skilletegnene som samsvarer med din region.</span><span class="sxs-lookup"><span data-stu-id="66600-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="66600-120">Merk at ut formatet for å vise datoer i trykte rapporter eller dokumenter sendt via e-post, ikke påvirkes av ditt personlige valg av regioninnstilling.</span><span class="sxs-lookup"><span data-stu-id="66600-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="66600-121">Hvis du vil arbeide mer effektivt med datoer og klokkeslett, kan du bruke metodene eller formatene som er beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="66600-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="66600-122">Plukke datoer fra kalenderen</span><span class="sxs-lookup"><span data-stu-id="66600-122">Picking dates from the calendar</span></span>

<span data-ttu-id="66600-123">Alle felt som viser et kalenderikonet, kan angis ved hjelp kalenderdatovelgeren.</span><span class="sxs-lookup"><span data-stu-id="66600-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="66600-124">Aktiver kalenderikonet for å vise kalenderdatovelgeren, eller trykk Ctrl+Hjem i feltet.</span><span class="sxs-lookup"><span data-stu-id="66600-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="66600-125">![Datofelt](media/ui-date-field.png "Eksempel på et datofelt")</span><span class="sxs-lookup"><span data-stu-id="66600-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="66600-126">Se også [Hurtigtaster i kalenderdatovelgeren](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="66600-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="66600-127">Mønsteret dag\-uke\-årn</span><span class="sxs-lookup"><span data-stu-id="66600-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="66600-128">Du kan angi en dato som en ukedag etterfulgt av et ukenummer og eventyelt et år.</span><span class="sxs-lookup"><span data-stu-id="66600-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="66600-129">For eksempel Man25 eller man25 betyr mandag i uke 25.</span><span class="sxs-lookup"><span data-stu-id="66600-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="66600-130">Hvis du ikke angir et år, brukes året i arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="66600-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="66600-131">I stedet for å angi hele ordet for ukedagen, kan du angi en del av ord fra begynnelsen.</span><span class="sxs-lookup"><span data-stu-id="66600-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="66600-132">Hvis det oppstår konflikter (som med t som kan være tirsdag eller torsdag), evalueres dagene i henhold til regioninnstillingen.</span><span class="sxs-lookup"><span data-stu-id="66600-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="66600-133">Inndataene vurderes først mot arbeidsdato samt i dag, så husk dette når du forkorter.</span><span class="sxs-lookup"><span data-stu-id="66600-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="66600-134">For eksempel t betyr allerede dagens, og kan dermed ikke bety tirsdag eller torsdag.</span><span class="sxs-lookup"><span data-stu-id="66600-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="66600-135">Ukenummererplanen er alltid ISO 8601, der uke 1 er uken med 4 januar i seg, eller uken med den første torsdagen i året.</span><span class="sxs-lookup"><span data-stu-id="66600-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="66600-136">Tallmønstre</span><span class="sxs-lookup"><span data-stu-id="66600-136">Digit patterns</span></span>

<span data-ttu-id="66600-137">I et datofelt kan du angi to, fire, seks eller åtte tall:</span><span class="sxs-lookup"><span data-stu-id="66600-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="66600-138">Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="66600-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="66600-139">Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="66600-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="66600-140">Rekkefølgen på dag og måned avhenger av regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="66600-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="66600-141">Selv om dine regioninnstillingene dine har året før dag og måned, tolkes fire sifre som dagen og måneden.</span><span class="sxs-lookup"><span data-stu-id="66600-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="66600-142">Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.</span><span class="sxs-lookup"><span data-stu-id="66600-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="66600-143">I dag</span><span class="sxs-lookup"><span data-stu-id="66600-143">Today</span></span>

<span data-ttu-id="66600-144">Skriv inn ordet for i dag, på språket som er angitt av **Språk**-innstillingen, som angir datoen til den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="66600-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="66600-145">I stedet for å skrive inn hele ordet kan du angi en del av ordet fra begynnelsen, som t eller ida, forutsatt at det ikke er også begynnelsen av et annet ord.</span><span class="sxs-lookup"><span data-stu-id="66600-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="66600-146">Periode</span><span class="sxs-lookup"><span data-stu-id="66600-146">Period</span></span>

<span data-ttu-id="66600-147">For å filtrere på en bestemt regnskapsperiode, angi bokstaven p eller ordet periode i datofeltet, etterfulgt av et nummer som identifiserer regnskapsperioden, som p2 eller periode4.</span><span class="sxs-lookup"><span data-stu-id="66600-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="66600-148">Regnskapsperioden er relativ til regnskapsåret for gjeldende arbeidsdato som er angitt i ditt rollesenter.</span><span class="sxs-lookup"><span data-stu-id="66600-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="66600-149">Hvis for eksempel arbeidsdatoen er **21.03.20**, filtreres p1 eller bare p på den første regnskapsperioden i regnskapsåret 2020 (for eksempel 01.01.20–31.01/20).</span><span class="sxs-lookup"><span data-stu-id="66600-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="66600-150">p15 filtrerer på den femtende regnskapsperioden fra starten av regnskapsåret 2020 (for eksempel 01.03.21–31.03.20).</span><span class="sxs-lookup"><span data-stu-id="66600-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="66600-151">Regnskapsperioden er definert på **Regnskapsperioder**-siden.</span><span class="sxs-lookup"><span data-stu-id="66600-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="66600-152">Hvis du vil vise eller endre regnskapsperiodene, åpner du siden [her](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="66600-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="66600-153">Gjeldende arbeidsdato</span><span class="sxs-lookup"><span data-stu-id="66600-153">Current work date</span></span>

<span data-ttu-id="66600-154">Arbeidsdatofunksjonen lar deg registrere transaksjoner med en dato som er forskjellig fra den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="66600-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="66600-155">Ordet for "arbeidsdato" på språket som er angitt av **Språk**-innstillingen, setter datoen til arbeidsdatoen som er angitt på siden **Mine innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="66600-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="66600-156">I stedet for å angi hele ordet, kan du angi en del av ord fra begynnelsen, for eksempel "a" eller "arbeid".</span><span class="sxs-lookup"><span data-stu-id="66600-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="66600-157">Hvis du ikke har definert en arbeidsdato, vil den gjeldende datoen bli brukt som arbeidsdato.</span><span class="sxs-lookup"><span data-stu-id="66600-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="66600-158">Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="66600-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="66600-159">Se også [Endre grunnleggende innstillinger, for eksempel arbeidsdatoen](ui-change-basic-settings.md#work-date)</span><span class="sxs-lookup"><span data-stu-id="66600-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="66600-160">Avslutningsdato</span><span class="sxs-lookup"><span data-stu-id="66600-160">Closing Date</span></span>

<span data-ttu-id="66600-161">Når du avslutter et regnskapsår, kan du bruke avslutningsdatoer til å indikere at en post er en avslutningspost.</span><span class="sxs-lookup"><span data-stu-id="66600-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="66600-162">En avslutningsdato ligger teknisk sett mellom to datoer, for eksempel mellom 31. desember og 1. januar.</span><span class="sxs-lookup"><span data-stu-id="66600-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="66600-163">Hvis en dato skal være en avslutningsdato, setter du A rett foran datoen, for eksempel A123101.</span><span class="sxs-lookup"><span data-stu-id="66600-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="66600-164">Dette kan brukes sammen alle datomønstre.</span><span class="sxs-lookup"><span data-stu-id="66600-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="66600-165">Eksempler</span><span class="sxs-lookup"><span data-stu-id="66600-165">Examples</span></span>

<span data-ttu-id="66600-166">Tabellen nedenfor inneholder eksempler på datoer som bruker alle formater.</span><span class="sxs-lookup"><span data-stu-id="66600-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="66600-167">Det antar regioninnstillinger som formaterer datoer i henhold til: **år.måned.dag.**, en uke som starter på mandag, og engelsk språk.</span><span class="sxs-lookup"><span data-stu-id="66600-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="66600-168">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="66600-168">**Entry**</span></span>      |<span data-ttu-id="66600-169">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="66600-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="66600-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="66600-170">2018.12.31.</span></span>|<span data-ttu-id="66600-171">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-171">2018.12.31.</span></span>|
|<span data-ttu-id="66600-172">181231</span><span class="sxs-lookup"><span data-stu-id="66600-172">181231</span></span>|<span data-ttu-id="66600-173">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-173">2018.12.31.</span></span>|
|<span data-ttu-id="66600-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="66600-174">18.12.31.</span></span>|<span data-ttu-id="66600-175">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-175">2018.12.31.</span></span>|
|<span data-ttu-id="66600-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="66600-176">18.12.31.</span></span>|<span data-ttu-id="66600-177">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-177">2018.12.31.</span></span>|
|<span data-ttu-id="66600-178">20181231</span><span class="sxs-lookup"><span data-stu-id="66600-178">20181231</span></span>|<span data-ttu-id="66600-179">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-179">2018.12.31.</span></span>|
|<span data-ttu-id="66600-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="66600-180">18/12,31</span></span>|<span data-ttu-id="66600-181">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="66600-181">2018.12.31.</span></span>|
|<span data-ttu-id="66600-182">11</span><span class="sxs-lookup"><span data-stu-id="66600-182">11</span></span>|<span data-ttu-id="66600-183">11.arbeidsdato måned.arbeidsdato år.</span><span class="sxs-lookup"><span data-stu-id="66600-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="66600-184">1112</span><span class="sxs-lookup"><span data-stu-id="66600-184">1112</span></span>|<span data-ttu-id="66600-185">12.11.arbeidsdato år.</span><span class="sxs-lookup"><span data-stu-id="66600-185">work date year.11.12.</span></span>|
|<span data-ttu-id="66600-186">d eller i dag</span><span class="sxs-lookup"><span data-stu-id="66600-186">t or today</span></span>|<span data-ttu-id="66600-187">dagens dato</span><span class="sxs-lookup"><span data-stu-id="66600-187">today's date</span></span>|
|<span data-ttu-id="66600-188">p4</span><span class="sxs-lookup"><span data-stu-id="66600-188">p4</span></span>|<span data-ttu-id="66600-189">datointervall som inneholder den fjerde regnskapsperioden, for eksempel 01.04.20–30.04.20</span><span class="sxs-lookup"><span data-stu-id="66600-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="66600-190">a eller arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="66600-190">w or workdate</span></span>|<span data-ttu-id="66600-191">arbeidsdatoen</span><span class="sxs-lookup"><span data-stu-id="66600-191">the working date</span></span>|
|<span data-ttu-id="66600-192">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="66600-192">m or Monday</span></span>|<span data-ttu-id="66600-193">Mandag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="66600-193">Monday of the work date week</span></span>|
|<span data-ttu-id="66600-194">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="66600-194">tu or Tuesday</span></span>|<span data-ttu-id="66600-195">Tirsdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="66600-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="66600-196">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="66600-196">sa or Saturday</span></span>|<span data-ttu-id="66600-197">Lørdag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="66600-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="66600-198">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="66600-198">s or Sunday</span></span>|<span data-ttu-id="66600-199">Søndag i arbeidsdatouken</span><span class="sxs-lookup"><span data-stu-id="66600-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="66600-200">t23</span><span class="sxs-lookup"><span data-stu-id="66600-200">t23</span></span>|<span data-ttu-id="66600-201">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="66600-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="66600-202">t 23</span><span class="sxs-lookup"><span data-stu-id="66600-202">t 23</span></span>|<span data-ttu-id="66600-203">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="66600-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="66600-204">t-1</span><span class="sxs-lookup"><span data-stu-id="66600-204">t-1</span></span>|<span data-ttu-id="66600-205">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="66600-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="66600-206">Angi intervaller</span><span class="sxs-lookup"><span data-stu-id="66600-206">Setting Ranges</span></span>

<span data-ttu-id="66600-207">I lister, totaler eller rapporter kan du definere filtre på datoer, klokkeslett og datoer og klokkeslett som inneholder en startverdi og eventuelt en sluttverdi, for å vise bare dataene i dette intervallet.</span><span class="sxs-lookup"><span data-stu-id="66600-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="66600-208">Standardreglene gjelder for angivelse av datointervaller.</span><span class="sxs-lookup"><span data-stu-id="66600-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="66600-209">**Betyr**</span><span class="sxs-lookup"><span data-stu-id="66600-209">**Meaning**</span></span>|<span data-ttu-id="66600-210">**Eksempeluttrykk (dato)**</span><span class="sxs-lookup"><span data-stu-id="66600-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="66600-211">**Data som er inkludert i filteret**</span><span class="sxs-lookup"><span data-stu-id="66600-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="66600-212">Intervall</span><span class="sxs-lookup"><span data-stu-id="66600-212">Interval</span></span>|<span data-ttu-id="66600-213">15.12.00..15.01.01</span><span class="sxs-lookup"><span data-stu-id="66600-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="66600-214">..15.12.00</span><span class="sxs-lookup"><span data-stu-id="66600-214">..12 15 00</span></span><br /><br /><span data-ttu-id="66600-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="66600-215">p1..p4</span></span>|<span data-ttu-id="66600-216">Poster med dato fra og med 15.12.00 til og med 15.01.01.</span><span class="sxs-lookup"><span data-stu-id="66600-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="66600-217">Poster med datoer 15.12.00 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="66600-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="66600-218">Datointervall som inneholder den andre, tredje eller fjerde regnskapsperioden, for eksempel 01.01.20–30.04.20.</span><span class="sxs-lookup"><span data-stu-id="66600-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="66600-219">Enten/eller</span><span class="sxs-lookup"><span data-stu-id="66600-219">Either/or</span></span>|<span data-ttu-id="66600-220">12 15 00\|12 16 00</span><span class="sxs-lookup"><span data-stu-id="66600-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="66600-221">Poster med datoer enten 15.12.00 eller 16.12.00.</span><span class="sxs-lookup"><span data-stu-id="66600-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="66600-222">Hvis det er poster med begge datoer på begge dager, blir alle vist.</span><span class="sxs-lookup"><span data-stu-id="66600-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="66600-223">Kombinasjon</span><span class="sxs-lookup"><span data-stu-id="66600-223">Combination</span></span>|<span data-ttu-id="66600-224">12 15 00\|12 01 00..12 10 00</span><span class="sxs-lookup"><span data-stu-id="66600-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="66600-225">..12 14 00\|12 30 00..</span><span class="sxs-lookup"><span data-stu-id="66600-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="66600-226">Poster med datoer 15.12.00 eller fra og med 01.12.00 til og med 10.12.00.</span><span class="sxs-lookup"><span data-stu-id="66600-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="66600-227">Poster med datoer 14.12.00 eller tidligere, eller datoer 30.12.00 eller senere, det vil si alle poster unntatt poster med datoer mellom og 15.12.00 og 29.12.00.</span><span class="sxs-lookup"><span data-stu-id="66600-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="66600-228">Du kan bruke ethvert gyldig format i datointervallfiltre.</span><span class="sxs-lookup"><span data-stu-id="66600-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="66600-229">For eksempel man14 3..t 4p brukt på en dato- og klokkeslettfelt resulterer i et filter fra 03:00 mandag i uke 14 i det gjeldende arbeidsdatoåret, inkludert til dagens dato klokken 16:00.</span><span class="sxs-lookup"><span data-stu-id="66600-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="66600-230">Bruke datoformler</span><span class="sxs-lookup"><span data-stu-id="66600-230">Using Date Formulas</span></span>
<span data-ttu-id="66600-231">En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer.</span><span class="sxs-lookup"><span data-stu-id="66600-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="66600-232">Du kan angi datoformler i forskjellige datoberegningsfelt eller filtre.</span><span class="sxs-lookup"><span data-stu-id="66600-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="66600-233">Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag.</span><span class="sxs-lookup"><span data-stu-id="66600-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="66600-234">Hvis du for eksempel angir 1U, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert.</span><span class="sxs-lookup"><span data-stu-id="66600-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="66600-235">Hvis du vil angi en periode på sju dager \(én sann uke\), inkludert periodens startdato, må du angi 6D eller 1U-1D.</span><span class="sxs-lookup"><span data-stu-id="66600-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="66600-236">Her kommer det noen eksempler på hvordan datoformler kan brukes:</span><span class="sxs-lookup"><span data-stu-id="66600-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="66600-237">Datoformelen i det gjentakende intervallfeltet i gjentakende kladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="66600-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="66600-238">Datoformelen i feltet **Respittid** for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen \(eller fra forrige purringsdato\) før det kan opprettes en purring.</span><span class="sxs-lookup"><span data-stu-id="66600-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="66600-239">Datoformelen i feltet **Beregning av forfallsdato** angir hvordan forfallsdatoen i purringen beregnes.</span><span class="sxs-lookup"><span data-stu-id="66600-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="66600-240">Datoformelen kan inneholde opptil 20 tegn, både tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66600-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="66600-241">Du kan bruke følgende bokstaver, som er forkortelser for kalenderenheter:</span><span class="sxs-lookup"><span data-stu-id="66600-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="66600-242">Bokstav</span><span class="sxs-lookup"><span data-stu-id="66600-242">Letter</span></span>  |  <span data-ttu-id="66600-243">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="66600-244">L</span><span class="sxs-lookup"><span data-stu-id="66600-244">C</span></span>|<span data-ttu-id="66600-245">Løpende</span><span class="sxs-lookup"><span data-stu-id="66600-245">Current</span></span>|
|<span data-ttu-id="66600-246">D</span><span class="sxs-lookup"><span data-stu-id="66600-246">D</span></span>|<span data-ttu-id="66600-247">Dag\(er\)</span><span class="sxs-lookup"><span data-stu-id="66600-247">Day\(s\)</span></span>|
|<span data-ttu-id="66600-248">U</span><span class="sxs-lookup"><span data-stu-id="66600-248">W</span></span>|<span data-ttu-id="66600-249">Uke\(r\)</span><span class="sxs-lookup"><span data-stu-id="66600-249">Week\(s\)</span></span>|
|<span data-ttu-id="66600-250">M</span><span class="sxs-lookup"><span data-stu-id="66600-250">M</span></span>|<span data-ttu-id="66600-251">Måned\(er\)</span><span class="sxs-lookup"><span data-stu-id="66600-251">Month\(s\)</span></span>|
|<span data-ttu-id="66600-252">K</span><span class="sxs-lookup"><span data-stu-id="66600-252">Q</span></span>|<span data-ttu-id="66600-253">Kvartal\(er\)</span><span class="sxs-lookup"><span data-stu-id="66600-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="66600-254">Å</span><span class="sxs-lookup"><span data-stu-id="66600-254">Y</span></span>|<span data-ttu-id="66600-255">År\(\)</span><span class="sxs-lookup"><span data-stu-id="66600-255">Year\(s\)</span></span>|

<span data-ttu-id="66600-256">Du kan opprette datoformler på tre måter.</span><span class="sxs-lookup"><span data-stu-id="66600-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="66600-257">Eksempelet nedenfor viser hvordan L brukes, for løpende, og en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="66600-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="66600-258">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="66600-258">Expression</span></span>  |  <span data-ttu-id="66600-259">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="66600-260">LU</span><span class="sxs-lookup"><span data-stu-id="66600-260">CW</span></span>|<span data-ttu-id="66600-261">Løpende uke</span><span class="sxs-lookup"><span data-stu-id="66600-261">Current week</span></span>|
|<span data-ttu-id="66600-262">LM</span><span class="sxs-lookup"><span data-stu-id="66600-262">CM</span></span>|<span data-ttu-id="66600-263">Løpende måned</span><span class="sxs-lookup"><span data-stu-id="66600-263">Current month</span></span>|

<span data-ttu-id="66600-264">Eksempelet nedenfor viser hvordan et tall og en tidsangivelse brukes.</span><span class="sxs-lookup"><span data-stu-id="66600-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="66600-265">Et tall kan ikke være større enn 9999.</span><span class="sxs-lookup"><span data-stu-id="66600-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="66600-266">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="66600-266">Expression</span></span>  |  <span data-ttu-id="66600-267">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="66600-268">10D</span><span class="sxs-lookup"><span data-stu-id="66600-268">10D</span></span>|<span data-ttu-id="66600-269">10 dager fra i dag</span><span class="sxs-lookup"><span data-stu-id="66600-269">10 days from today</span></span>|
|<span data-ttu-id="66600-270">2U</span><span class="sxs-lookup"><span data-stu-id="66600-270">2W</span></span>|<span data-ttu-id="66600-271">2 uker fra i dag</span><span class="sxs-lookup"><span data-stu-id="66600-271">2 weeks from today</span></span>|

<span data-ttu-id="66600-272">Eksempelet nedenfor viser hvordan et en tidsangivelse og et tall brukes.</span><span class="sxs-lookup"><span data-stu-id="66600-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="66600-273">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="66600-273">Expression</span></span>  |  <span data-ttu-id="66600-274">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="66600-275">D10</span><span class="sxs-lookup"><span data-stu-id="66600-275">D10</span></span>|<span data-ttu-id="66600-276">Den neste 10. dag av en måned</span><span class="sxs-lookup"><span data-stu-id="66600-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="66600-277">UD4</span><span class="sxs-lookup"><span data-stu-id="66600-277">WD4</span></span>|<span data-ttu-id="66600-278">Neste 4. dag av en uke \(torsdag\)</span><span class="sxs-lookup"><span data-stu-id="66600-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="66600-279">Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="66600-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="66600-280">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="66600-280">Expression</span></span>  |  <span data-ttu-id="66600-281">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="66600-282">LM+10D</span><span class="sxs-lookup"><span data-stu-id="66600-282">CM+10D</span></span>|<span data-ttu-id="66600-283">Løpende måned \+10 dager</span><span class="sxs-lookup"><span data-stu-id="66600-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="66600-284">Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="66600-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="66600-285">Uttrykk</span><span class="sxs-lookup"><span data-stu-id="66600-285">Expression</span></span>  |  <span data-ttu-id="66600-286">Betyr</span><span class="sxs-lookup"><span data-stu-id="66600-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="66600-287">-1Å</span><span class="sxs-lookup"><span data-stu-id="66600-287">-1Y</span></span>|<span data-ttu-id="66600-288">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="66600-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="66600-289">Hvis plasseringen bruker en hovedkalender, tolkes datoformelen du angir, for eksempel i feltet **Leveringstid**, i henhold til arbeidsdager fra kalenderen.</span><span class="sxs-lookup"><span data-stu-id="66600-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="66600-290">For eksempel betyr 1U sju virkedager.</span><span class="sxs-lookup"><span data-stu-id="66600-290">For example, 1W  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="66600-291">Angi klokkeslett</span><span class="sxs-lookup"><span data-stu-id="66600-291">Entering Times</span></span>
<span data-ttu-id="66600-292">Når du angir tidspunkt, kan du sette inn alle skilletegn (ikke mellomrom) mellom enheter, men hvis du bruker doble sifre for hver enhet opptil millisekunder, er det ikke nødvendig.</span><span class="sxs-lookup"><span data-stu-id="66600-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="66600-293">Du trenger bare skrive de største enheter som du vil ha; resten settes til null.</span><span class="sxs-lookup"><span data-stu-id="66600-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="66600-294">Du kan eventuelt utelate AM-PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="66600-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="66600-295">Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="66600-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="66600-296">Det antar regioninnstillinger som formaterer tidspunkt i henhold til: **Timer:Minutter:Sekunder.Millisekunder.**</span><span class="sxs-lookup"><span data-stu-id="66600-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="66600-297">og bruker AM- og PM-indikatorer for henholdsvis "AM" og "PM".</span><span class="sxs-lookup"><span data-stu-id="66600-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="66600-298">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="66600-298">**Entry**</span></span>      |<span data-ttu-id="66600-299">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="66600-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="66600-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="66600-300">05:23:17</span></span>|<span data-ttu-id="66600-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="66600-301">05:23:17</span></span>|
|<span data-ttu-id="66600-302">5</span><span class="sxs-lookup"><span data-stu-id="66600-302">5</span></span>|<span data-ttu-id="66600-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-303">05:00:00</span></span>|
|<span data-ttu-id="66600-304">5AM</span><span class="sxs-lookup"><span data-stu-id="66600-304">5AM</span></span>|<span data-ttu-id="66600-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-305">05:00:00</span></span>|
|<span data-ttu-id="66600-306">5P</span><span class="sxs-lookup"><span data-stu-id="66600-306">5P</span></span>|<span data-ttu-id="66600-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-307">17:00:00</span></span>|
|<span data-ttu-id="66600-308">12</span><span class="sxs-lookup"><span data-stu-id="66600-308">12</span></span>|<span data-ttu-id="66600-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-309">12:00:00</span></span>|
|<span data-ttu-id="66600-310">12A</span><span class="sxs-lookup"><span data-stu-id="66600-310">12A</span></span>|<span data-ttu-id="66600-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-311">00:00:00</span></span>|
|<span data-ttu-id="66600-312">12P</span><span class="sxs-lookup"><span data-stu-id="66600-312">12P</span></span>|<span data-ttu-id="66600-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-313">12:00:00</span></span>|
|<span data-ttu-id="66600-314">17</span><span class="sxs-lookup"><span data-stu-id="66600-314">17</span></span>|<span data-ttu-id="66600-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-315">17:00:00</span></span>|
|<span data-ttu-id="66600-316">5:30</span><span class="sxs-lookup"><span data-stu-id="66600-316">5:30</span></span>|<span data-ttu-id="66600-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="66600-317">05:30:00</span></span>|
|<span data-ttu-id="66600-318">0530</span><span class="sxs-lookup"><span data-stu-id="66600-318">0530</span></span>|<span data-ttu-id="66600-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="66600-319">05:30:00</span></span>|
|<span data-ttu-id="66600-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="66600-320">5:30:5</span></span>|<span data-ttu-id="66600-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="66600-321">05:30:05</span></span>|
|<span data-ttu-id="66600-322">053005</span><span class="sxs-lookup"><span data-stu-id="66600-322">053005</span></span>|<span data-ttu-id="66600-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="66600-323">05:30:05</span></span>|
|<span data-ttu-id="66600-324">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="66600-324">5:30:5,50</span></span>|<span data-ttu-id="66600-325">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="66600-325">05:30:05.5</span></span>|
|<span data-ttu-id="66600-326">053005050</span><span class="sxs-lookup"><span data-stu-id="66600-326">053005050</span></span>|<span data-ttu-id="66600-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="66600-327">05:30:05.05</span></span>|

<span data-ttu-id="66600-328">Vær oppmerksom på at millisekunder tolkes som desimalformat.</span><span class="sxs-lookup"><span data-stu-id="66600-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="66600-329">Derfor betyr både 3, 30 og 300 altså 300 millisekunder, mens 03 betyr 30 og 003 betyr 3 millisekunder.</span><span class="sxs-lookup"><span data-stu-id="66600-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="66600-330">Du kan ikke bruke 24:00 til å angi midnatt eller bruke en verdi som er større enn 24:00.</span><span class="sxs-lookup"><span data-stu-id="66600-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="66600-331">Ordet for tidspunkt på språket som brukes av [!INCLUDE[d365fin](includes/d365fin_long_md.md)], evalueres etter gjeldende dato og klokkeslett på datamaskinen eller mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="66600-331">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="66600-332">Du kan angi en del av ordet, fra begynnelsen, som for eksempel t eller TIM.</span><span class="sxs-lookup"><span data-stu-id="66600-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="66600-333">Angi kombinerte datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="66600-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="66600-334">Når du angir dato og klokkeslett, som er en dato og klokkeslett kombinert i ett felt, må du angi et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="66600-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="66600-335">Datodelen kan bare inneholde mellomrom i form av det offisielle datoskilletegnet i regioninnstillingene.</span><span class="sxs-lookup"><span data-stu-id="66600-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="66600-336">Klokkeslettet kan inneholde mellomrom rundt AM/PM-indikatoren.</span><span class="sxs-lookup"><span data-stu-id="66600-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="66600-337">Det er også mulig å angi bare en dato i feltet for dato og klokkeslett, men det er ikke mulig å angi bare et klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="66600-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="66600-338">Tabellen nedenfor inneholder noen eksempler på kombinasjoner av dato/klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="66600-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="66600-339">Regioninnstillingene i eksemplene viser datoer i formatet dag\-måned\-år ved hjelp av AM/PM-angivelse, engelsk språk og søndag som start på uken.</span><span class="sxs-lookup"><span data-stu-id="66600-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="66600-340">**Angivelse**</span><span class="sxs-lookup"><span data-stu-id="66600-340">**Entry**</span></span>      |<span data-ttu-id="66600-341">**Tolkning**</span><span class="sxs-lookup"><span data-stu-id="66600-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="66600-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="66600-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="66600-343">08.01.2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="66600-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="66600-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="66600-344">131202 132455</span></span>|<span data-ttu-id="66600-345">13.12.2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="66600-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="66600-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="66600-346">1-12-02 10</span></span>|<span data-ttu-id="66600-347">01.12.2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="66600-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="66600-348">1.12.02 5</span></span>|<span data-ttu-id="66600-349">01.12.2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="66600-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="66600-350">1.12.02</span></span>|<span data-ttu-id="66600-351">01.12.2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="66600-352">11 12</span><span class="sxs-lookup"><span data-stu-id="66600-352">11 12</span></span>|<span data-ttu-id="66600-353">11.arbeidsdatomåned.arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="66600-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="66600-354">1112 12</span></span>|<span data-ttu-id="66600-355">11.12.arbeidsdatoår 12:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="66600-356">d eller i dag</span><span class="sxs-lookup"><span data-stu-id="66600-356">t or today</span></span>|<span data-ttu-id="66600-357">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="66600-358">k 10.30</span><span class="sxs-lookup"><span data-stu-id="66600-358">t 10:30</span></span>|<span data-ttu-id="66600-359">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="66600-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="66600-360">k 3.3.3</span><span class="sxs-lookup"><span data-stu-id="66600-360">t 3:3:3</span></span>|<span data-ttu-id="66600-361">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="66600-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="66600-362">a eller arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="66600-362">w or workdate</span></span>|<span data-ttu-id="66600-363">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="66600-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="66600-364">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="66600-364">m or Monday</span></span>|<span data-ttu-id="66600-365">Mandag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="66600-366">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="66600-366">tu or Tuesday</span></span>|<span data-ttu-id="66600-367">Tirsdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="66600-368">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="66600-368">sa or Saturday</span></span>|<span data-ttu-id="66600-369">Lørdag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="66600-370">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="66600-370">s or Sunday</span></span>|<span data-ttu-id="66600-371">Søndag i arbeidsdatouken 00:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="66600-372">ti 10.30</span><span class="sxs-lookup"><span data-stu-id="66600-372">tu 10:30</span></span>|<span data-ttu-id="66600-373">Tirsdag i arbeidsdatouken 10:30:00</span><span class="sxs-lookup"><span data-stu-id="66600-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="66600-374">ti 3.3.3</span><span class="sxs-lookup"><span data-stu-id="66600-374">tu 3:3:3</span></span>|<span data-ttu-id="66600-375">Tirsdag i arbeidsdatouken 03:03:03</span><span class="sxs-lookup"><span data-stu-id="66600-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="66600-376">t23 t</span><span class="sxs-lookup"><span data-stu-id="66600-376">t23 t</span></span>|<span data-ttu-id="66600-377">Tirsdag i uke 23 i arbeidsdatoåret, gjeldende klokkeslett</span><span class="sxs-lookup"><span data-stu-id="66600-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="66600-378">t23</span><span class="sxs-lookup"><span data-stu-id="66600-378">t23</span></span>|<span data-ttu-id="66600-379">Tirsdag i uke 23 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="66600-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="66600-380">t 23</span><span class="sxs-lookup"><span data-stu-id="66600-380">t 23</span></span>|<span data-ttu-id="66600-381">I dag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="66600-381">Today 23:00:00</span></span>|
|<span data-ttu-id="66600-382">t-1</span><span class="sxs-lookup"><span data-stu-id="66600-382">t-1</span></span>|<span data-ttu-id="66600-383">Tirsdag i uke 1 i arbeidsdatoåret</span><span class="sxs-lookup"><span data-stu-id="66600-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="66600-384">Angi varighet</span><span class="sxs-lookup"><span data-stu-id="66600-384">Entering Duration</span></span>
<span data-ttu-id="66600-385">Noen av feltene i programmet representerer en varighet eller mengden som er gått, i stedet for en bestemt dato eller klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="66600-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="66600-386">Du angir en varighet som et tall etterfulgt av enheten.</span><span class="sxs-lookup"><span data-stu-id="66600-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="66600-387">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="66600-387">Here are some examples.</span></span>

|<span data-ttu-id="66600-388">**Varighet**</span><span class="sxs-lookup"><span data-stu-id="66600-388">**Duration**</span></span>|<span data-ttu-id="66600-389">**Enhet**</span><span class="sxs-lookup"><span data-stu-id="66600-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="66600-390">2t</span><span class="sxs-lookup"><span data-stu-id="66600-390">2h</span></span>|<span data-ttu-id="66600-391">2 timer</span><span class="sxs-lookup"><span data-stu-id="66600-391">2 hrs</span></span>|
|<span data-ttu-id="66600-392">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="66600-392">6h 30 m</span></span>|<span data-ttu-id="66600-393">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="66600-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="66600-394">6,5t</span><span class="sxs-lookup"><span data-stu-id="66600-394">6.5h</span></span>|<span data-ttu-id="66600-395">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="66600-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="66600-396">90m</span><span class="sxs-lookup"><span data-stu-id="66600-396">90m</span></span>|<span data-ttu-id="66600-397">1 t 30 min</span><span class="sxs-lookup"><span data-stu-id="66600-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="66600-398">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="66600-398">2d 6h 30m</span></span>|<span data-ttu-id="66600-399">2 dager 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="66600-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="66600-400">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="66600-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="66600-401">2 dager 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="66600-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="66600-402">Du kan også angi et tall, som blir automatisk konvertert til et tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="66600-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="66600-403">Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.</span><span class="sxs-lookup"><span data-stu-id="66600-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="66600-404">Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.</span><span class="sxs-lookup"><span data-stu-id="66600-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="66600-405">Tallet 5 konverteres for eksempel til 5 timer hvis enheten er timer.</span><span class="sxs-lookup"><span data-stu-id="66600-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="66600-406">Se også</span><span class="sxs-lookup"><span data-stu-id="66600-406">See Also</span></span>
<span data-ttu-id="66600-407">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66600-407">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="66600-408">Beregne dato for kjøp</span><span class="sxs-lookup"><span data-stu-id="66600-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="66600-409">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="66600-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
