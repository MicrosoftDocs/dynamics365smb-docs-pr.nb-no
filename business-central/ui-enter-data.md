---
title: Skrive inn data i felt | Microsoft-dokumentasjon
description: "Det er mange generelle funksjoner du kan bruke til å skrive inn data raskt og enkelt. De generelle funksjonene for å skrive inn data beskrives i dette emnet."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a><span data-ttu-id="afd6a-104">Skrive inn data</span><span class="sxs-lookup"><span data-stu-id="afd6a-104">Entering Data</span></span>
<span data-ttu-id="afd6a-105">Det er mange generelle funksjoner du kan bruke til å skrive inn data raskt og enkelt.</span><span class="sxs-lookup"><span data-stu-id="afd6a-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="afd6a-106">De generelle funksjonene for å skrive inn data beskrives i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="afd6a-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="afd6a-107">Eksemplene i denne artikkelen bruker demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="afd6a-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="afd6a-108">Obligatoriske felt</span><span class="sxs-lookup"><span data-stu-id="afd6a-108">Mandatory Fields</span></span>
<span data-ttu-id="afd6a-109">Når du angir data på sider, merkes bestemte felt med en rød stjerne.</span><span class="sxs-lookup"><span data-stu-id="afd6a-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="afd6a-110">Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="afd6a-111">Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden.</span><span class="sxs-lookup"><span data-stu-id="afd6a-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="afd6a-112">Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.</span><span class="sxs-lookup"><span data-stu-id="afd6a-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="afd6a-113">Finne data mens du skriver</span><span class="sxs-lookup"><span data-stu-id="afd6a-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="afd6a-114">Når du begynner å skrive inn tegn i et felt, åpnes en rullegardinliste med mulige feltverdier.</span><span class="sxs-lookup"><span data-stu-id="afd6a-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="afd6a-115">Innholdet i listen endres etter hvert som du skriver inn flere tegn, og du kan velge ønsket verdi når den vises.</span><span class="sxs-lookup"><span data-stu-id="afd6a-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="afd6a-116">Mange felt har en pil-ned-knapp som du kan velge.</span><span class="sxs-lookup"><span data-stu-id="afd6a-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="afd6a-117">Du velger pilen for å få frem en liste over data som kan settes inn i feltet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="afd6a-118">Knappen har to funksjoner, avhengig av felttype:</span><span class="sxs-lookup"><span data-stu-id="afd6a-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="afd6a-119">Oppslag - viser informasjon fra en annen tabell som du kan sette inn i feltet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="afd6a-120">Du kan velge én datadel om gangen.</span><span class="sxs-lookup"><span data-stu-id="afd6a-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="afd6a-121">Rullegardin - viser settet med alternativer som finnes for feltet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="afd6a-122">Du kan bare velge ett av alternativene.</span><span class="sxs-lookup"><span data-stu-id="afd6a-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="afd6a-123">Angi antall ved beregning</span><span class="sxs-lookup"><span data-stu-id="afd6a-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="afd6a-124">Når du setter inn tall i antallfelt, for eksempel **Antall**-feltet på en varekladdlinje, kan du angi formelen i stedet for summen.</span><span class="sxs-lookup"><span data-stu-id="afd6a-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="afd6a-125">Eksempler</span><span class="sxs-lookup"><span data-stu-id="afd6a-125">Examples</span></span>  

-   <span data-ttu-id="afd6a-126">Hvis du skriver inn 19+19, beregnes feltet til 38.</span><span class="sxs-lookup"><span data-stu-id="afd6a-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="afd6a-127">Hvis du skriver inn 41-9, beregnes feltet til 32.</span><span class="sxs-lookup"><span data-stu-id="afd6a-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="afd6a-128">Hvis du skriver inn 12\*4, beregnes feltet til 48.</span><span class="sxs-lookup"><span data-stu-id="afd6a-128">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="afd6a-129">Hvis du skriver inn 12/4, beregnes feltet til 3.</span><span class="sxs-lookup"><span data-stu-id="afd6a-129">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="afd6a-130">Skrive inn negative tall</span><span class="sxs-lookup"><span data-stu-id="afd6a-130">Entering Negative Numbers</span></span>
<span data-ttu-id="afd6a-131">Du kan angi negative tall på to måter.</span><span class="sxs-lookup"><span data-stu-id="afd6a-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="afd6a-132">Tallet -20,5 kan angis som:</span><span class="sxs-lookup"><span data-stu-id="afd6a-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="afd6a-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="afd6a-133">-20.5</span></span>  

    <span data-ttu-id="afd6a-134">eller</span><span class="sxs-lookup"><span data-stu-id="afd6a-134">or</span></span>
-   <span data-ttu-id="afd6a-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="afd6a-135">20.5-</span></span>  

 <span data-ttu-id="afd6a-136">I begge tilfeller registreres beløpet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="afd6a-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="afd6a-137">Hvis det siste tegnet i uttrykket er en **++** eller en **--**, blir hele uttrykket registrert med dette tegnet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="afd6a-138">Eksempel: **10-20+** resulterer i 10 og ikke -10.</span><span class="sxs-lookup"><span data-stu-id="afd6a-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="afd6a-139">Angi datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="afd6a-139">Entering Dates and Times</span></span>
<span data-ttu-id="afd6a-140">Du kan sette inn datoer og klokkeslett i alle felt som er spesifikt tilordnet til datoer (datofelt).</span><span class="sxs-lookup"><span data-stu-id="afd6a-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="afd6a-141">Datoene kan skrives inn med eller uten skilletegn.</span><span class="sxs-lookup"><span data-stu-id="afd6a-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="afd6a-142">Hvordan du angir dato og klokkeslett på, avhenger av dine **Område**-innstillinger.</span><span class="sxs-lookup"><span data-stu-id="afd6a-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="afd6a-143">Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="afd6a-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="afd6a-144">Sette inn datoer</span><span class="sxs-lookup"><span data-stu-id="afd6a-144">Entering Dates</span></span>  
 <span data-ttu-id="afd6a-145">I et datofelt kan du angi to, fire, seks eller åtte tall:</span><span class="sxs-lookup"><span data-stu-id="afd6a-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="afd6a-146">Hvis du bare skriver inn to tall, tolkes disse som dagen, og måneden og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="afd6a-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="afd6a-147">Hvis du skriver inn fire tall, tolkes disse som dagen og måneden, og året for arbeidsdatoen legges til.</span><span class="sxs-lookup"><span data-stu-id="afd6a-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="afd6a-148">Hvis datoen du vil angi ligger i intervallet 01.01.1930 til og med 31.12.2029, kan du angi året med to eller fire sifre.</span><span class="sxs-lookup"><span data-stu-id="afd6a-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="afd6a-149">Du kan også angi en dato som en ukedag etterfulgt av et ukenummer og, hvis du vil, et år (for eksempel Man25 eller man25 betyr mandag i uke 25).</span><span class="sxs-lookup"><span data-stu-id="afd6a-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="afd6a-150">I stedet for å skrive inn en bestemt dato, kan du skrive inn én av to koder.</span><span class="sxs-lookup"><span data-stu-id="afd6a-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="afd6a-151"> - kode</span><span class="sxs-lookup"><span data-stu-id="afd6a-151">Code</span></span>|<span data-ttu-id="afd6a-152">Resultat</span><span class="sxs-lookup"><span data-stu-id="afd6a-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="afd6a-153">i</span><span class="sxs-lookup"><span data-stu-id="afd6a-153">t</span></span>|<span data-ttu-id="afd6a-154">Dette er dagens dato (systemdatoen for datamaskinen).</span><span class="sxs-lookup"><span data-stu-id="afd6a-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="afd6a-155">a</span><span class="sxs-lookup"><span data-stu-id="afd6a-155">w</span></span>|<span data-ttu-id="afd6a-156">Dette er arbeidsdatoen som er satt opp i programmet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="afd6a-157">Du kan endre arbeidsdatoen ved å se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="afd6a-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="afd6a-158">Hvis du har mange transaksjoner å utføre på en dato som ikke er dagens dato, er det en fordel å bruke arbeidsdatoen.</span><span class="sxs-lookup"><span data-stu-id="afd6a-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="afd6a-159">Angi klokkeslett</span><span class="sxs-lookup"><span data-stu-id="afd6a-159">Entering Times</span></span>  
 <span data-ttu-id="afd6a-160">Et vilkårlig skilletegn kan settes inn mellom tidsinndelingene, men det er ikke obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="afd6a-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="afd6a-161">Du behøver ikke å skrive inn minutter eller sekunder.</span><span class="sxs-lookup"><span data-stu-id="afd6a-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="afd6a-162">Tabellen nedenfor viser en oversikt over ulike måter å angi tidsinnstillinger på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="afd6a-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="afd6a-163">Angivelse</span><span class="sxs-lookup"><span data-stu-id="afd6a-163">Entry</span></span>|<span data-ttu-id="afd6a-164">Tolkning</span><span class="sxs-lookup"><span data-stu-id="afd6a-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="afd6a-165">5</span><span class="sxs-lookup"><span data-stu-id="afd6a-165">5</span></span>|<span data-ttu-id="afd6a-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-166">05:00:00</span></span>|  
|<span data-ttu-id="afd6a-167">5:30</span><span class="sxs-lookup"><span data-stu-id="afd6a-167">5:30</span></span>|<span data-ttu-id="afd6a-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-168">05:30:00</span></span>|  
|<span data-ttu-id="afd6a-169">0530</span><span class="sxs-lookup"><span data-stu-id="afd6a-169">0530</span></span>|<span data-ttu-id="afd6a-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-170">05:30:00</span></span>|  
|<span data-ttu-id="afd6a-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="afd6a-171">5:30:5</span></span>|<span data-ttu-id="afd6a-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="afd6a-172">05:30:05</span></span>|  
|<span data-ttu-id="afd6a-173">053005</span><span class="sxs-lookup"><span data-stu-id="afd6a-173">053005</span></span>|<span data-ttu-id="afd6a-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="afd6a-174">05:30:05</span></span>|  
|<span data-ttu-id="afd6a-175">5:30:5,50</span><span class="sxs-lookup"><span data-stu-id="afd6a-175">5:30:5,50</span></span>|<span data-ttu-id="afd6a-176">05:30:05.5</span><span class="sxs-lookup"><span data-stu-id="afd6a-176">05:30:05.5</span></span>|  
|<span data-ttu-id="afd6a-177">053005050</span><span class="sxs-lookup"><span data-stu-id="afd6a-177">053005050</span></span>|<span data-ttu-id="afd6a-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="afd6a-178">05:30:05.05</span></span>|  

 <span data-ttu-id="afd6a-179">Du må angi to sifre for hver tidsenhet dersom du ikke setter inn et skilletegn.</span><span class="sxs-lookup"><span data-stu-id="afd6a-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="afd6a-180">Angi datoer og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="afd6a-180">Entering Datetimes</span></span>  
 <span data-ttu-id="afd6a-181">Når du angir dato og klokkeslett, må du sette inn et mellomrom mellom datoen og klokkeslettet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="afd6a-182">Tabellen nedenfor viser de forskjellige måtene du kan angi dato og klokkeslett på, og hvordan de tolkes.</span><span class="sxs-lookup"><span data-stu-id="afd6a-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="afd6a-183">Post</span><span class="sxs-lookup"><span data-stu-id="afd6a-183">Entry</span></span>|<span data-ttu-id="afd6a-184">Tolkning</span><span class="sxs-lookup"><span data-stu-id="afd6a-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="afd6a-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="afd6a-185">131202 132455</span></span>|<span data-ttu-id="afd6a-186">13.12.02 13.24.55</span><span class="sxs-lookup"><span data-stu-id="afd6a-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="afd6a-187">1.12.02 10</span><span class="sxs-lookup"><span data-stu-id="afd6a-187">1-12-02 10</span></span>|<span data-ttu-id="afd6a-188">01.12.02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="afd6a-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="afd6a-189">1.12.02 5</span></span>|<span data-ttu-id="afd6a-190">12.01.02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="afd6a-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="afd6a-191">1.12.02</span></span>|<span data-ttu-id="afd6a-192">01.12.02 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-193">11 12</span><span class="sxs-lookup"><span data-stu-id="afd6a-193">11 12</span></span>|<span data-ttu-id="afd6a-194">11 - inneværende måned - inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="afd6a-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="afd6a-195">1112 12</span></span>|<span data-ttu-id="afd6a-196">11-12 - inneværende år 12.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="afd6a-197">i eller i dag</span><span class="sxs-lookup"><span data-stu-id="afd6a-197">t or today</span></span>|<span data-ttu-id="afd6a-198">dagens dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-199">i klokkeslett</span><span class="sxs-lookup"><span data-stu-id="afd6a-199">t time</span></span>|<span data-ttu-id="afd6a-200">dagens dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="afd6a-200">today's date actual time</span></span>|  
|<span data-ttu-id="afd6a-201">i 10.30</span><span class="sxs-lookup"><span data-stu-id="afd6a-201">t 10:30</span></span>|<span data-ttu-id="afd6a-202">dagens dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="afd6a-203">i 3.3.3</span><span class="sxs-lookup"><span data-stu-id="afd6a-203">t 3:3:3</span></span>|<span data-ttu-id="afd6a-204">dagens dato 03.03.03</span><span class="sxs-lookup"><span data-stu-id="afd6a-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="afd6a-205">a eller arbeidsdag</span><span class="sxs-lookup"><span data-stu-id="afd6a-205">w or workdate</span></span>|<span data-ttu-id="afd6a-206">arbeidsdatoen 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-207">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="afd6a-207">m or Monday</span></span>|<span data-ttu-id="afd6a-208">mandag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-209">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="afd6a-209">tu or Tuesday</span></span>|<span data-ttu-id="afd6a-210">tirsdag i inneværende uke 00:00:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-211">o eller onsdag</span><span class="sxs-lookup"><span data-stu-id="afd6a-211">we or Wednesday</span></span>|<span data-ttu-id="afd6a-212">onsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-213">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="afd6a-213">th or Thursday</span></span>|<span data-ttu-id="afd6a-214">torsdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-215">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="afd6a-215">f or Friday</span></span>|<span data-ttu-id="afd6a-216">fredag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-217">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="afd6a-217">s or Saturday</span></span>|<span data-ttu-id="afd6a-218">lørdag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-219">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="afd6a-219">su or Sunday</span></span>|<span data-ttu-id="afd6a-220">søndag i inneværende uke 00.00.00</span><span class="sxs-lookup"><span data-stu-id="afd6a-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="afd6a-221">ti 10.30</span><span class="sxs-lookup"><span data-stu-id="afd6a-221">tu 10:30</span></span>|<span data-ttu-id="afd6a-222">tirsdag i inneværende uke 10:30:00</span><span class="sxs-lookup"><span data-stu-id="afd6a-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="afd6a-223">ti 3.3.3</span><span class="sxs-lookup"><span data-stu-id="afd6a-223">tu 3:3:3</span></span>|<span data-ttu-id="afd6a-224">tirsdag i inneværende uke 03.03.03</span><span class="sxs-lookup"><span data-stu-id="afd6a-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="afd6a-225">Angi varighet</span><span class="sxs-lookup"><span data-stu-id="afd6a-225">Entering Duration</span></span>  
 <span data-ttu-id="afd6a-226">Du angir en varighet som et tall etterfulgt av enheten.</span><span class="sxs-lookup"><span data-stu-id="afd6a-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="afd6a-227">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="afd6a-227">Here are some examples.</span></span>  

|<span data-ttu-id="afd6a-228">Varighet</span><span class="sxs-lookup"><span data-stu-id="afd6a-228">Duration</span></span>|<span data-ttu-id="afd6a-229">Enhtet**</span><span class="sxs-lookup"><span data-stu-id="afd6a-229">Unit of measure**</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="afd6a-230">2t</span><span class="sxs-lookup"><span data-stu-id="afd6a-230">2h</span></span>|<span data-ttu-id="afd6a-231">2 timer</span><span class="sxs-lookup"><span data-stu-id="afd6a-231">2 hrs</span></span>|  
|<span data-ttu-id="afd6a-232">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="afd6a-232">6h 30 m</span></span>|<span data-ttu-id="afd6a-233">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="afd6a-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="afd6a-234">6,5t</span><span class="sxs-lookup"><span data-stu-id="afd6a-234">6.5h</span></span>|<span data-ttu-id="afd6a-235">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="afd6a-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="afd6a-236">90m</span><span class="sxs-lookup"><span data-stu-id="afd6a-236">90m</span></span>|<span data-ttu-id="afd6a-237">1 t 30 min</span><span class="sxs-lookup"><span data-stu-id="afd6a-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="afd6a-238">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="afd6a-238">2d 6h 30m</span></span>|<span data-ttu-id="afd6a-239">2 dager 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="afd6a-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="afd6a-240">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="afd6a-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="afd6a-241">2 dager 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="afd6a-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="afd6a-242">Du kan også angi et tall, og det blir automatisk konvertert til et tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="afd6a-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="afd6a-243">Tallet du angir, konverteres i henhold til standardenheten som er angitt for feltet Varighet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="afd6a-244">Hvis du vil se hvilken enhet som er brukt i et varighetsfelt, kan du angi et tall og se hvilken enhet programmet er konvertert det til.</span><span class="sxs-lookup"><span data-stu-id="afd6a-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="afd6a-245">Tallet 5 konverteres til 5 timer hvis enheten er timer.</span><span class="sxs-lookup"><span data-stu-id="afd6a-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="afd6a-246">Bruke datoformler</span><span class="sxs-lookup"><span data-stu-id="afd6a-246">Using Date Formulas</span></span>  
 <span data-ttu-id="afd6a-247">En datoformel er en kort, forkortet kombinasjon av bokstaver og tall som angir hvordan det skal beregne datoer.</span><span class="sxs-lookup"><span data-stu-id="afd6a-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="afd6a-248">Du kan angi datoformler i forskjellige datoberegningsfelt og i gjentakende intervallfelt i gjentakende kladder.</span><span class="sxs-lookup"><span data-stu-id="afd6a-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="afd6a-249">Én dag tas med automatisk i alle datoformelfelt for å angi at perioden starter i dag.</span><span class="sxs-lookup"><span data-stu-id="afd6a-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="afd6a-250">Hvis du for eksempel angir 1U, blir perioden på samme måte faktisk åtte dager fordi dagens dato er inkludert.</span><span class="sxs-lookup"><span data-stu-id="afd6a-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="afd6a-251">Hvis du vil angi en periode på sju dager (én sann uke), inkludert periodens startdato, må du angi 6D eller 1U-1D.</span><span class="sxs-lookup"><span data-stu-id="afd6a-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="afd6a-252">Her kommer det noen eksempler på hvordan datoformler kan brukes:</span><span class="sxs-lookup"><span data-stu-id="afd6a-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="afd6a-253">Datoformelen i det gjentakende intervallfeltet i gjentakende kladder bestemmer hvor ofte posten på kladdelinjen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="afd6a-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="afd6a-254">Datoformelen i feltet Respittid for en bestemt purringsgrad angir hvor lang tid som må gå fra forfallsdatoen (eller fra forrige purringsdato) før det kan opprettes en purring.</span><span class="sxs-lookup"><span data-stu-id="afd6a-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="afd6a-255">Datoformelen i feltet Beregning av forfallsdato angir hvordan forfallsdatoen i purringen beregnes.</span><span class="sxs-lookup"><span data-stu-id="afd6a-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="afd6a-256">Formelen for datoberegning kan inneholde opptil 20 tegn, både tall og bokstaver.</span><span class="sxs-lookup"><span data-stu-id="afd6a-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="afd6a-257">Du kan bruke følgende bokstaver, som er forkortelser for tidsangivelser:</span><span class="sxs-lookup"><span data-stu-id="afd6a-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-258">L</span><span class="sxs-lookup"><span data-stu-id="afd6a-258">C</span></span>|<span data-ttu-id="afd6a-259">Løpende</span><span class="sxs-lookup"><span data-stu-id="afd6a-259">Current</span></span>|  
|<span data-ttu-id="afd6a-260">D</span><span class="sxs-lookup"><span data-stu-id="afd6a-260">D</span></span>|<span data-ttu-id="afd6a-261">Dag(er)</span><span class="sxs-lookup"><span data-stu-id="afd6a-261">Day(s)</span></span>|  
|<span data-ttu-id="afd6a-262">U</span><span class="sxs-lookup"><span data-stu-id="afd6a-262">W</span></span>|<span data-ttu-id="afd6a-263">Uke(r)</span><span class="sxs-lookup"><span data-stu-id="afd6a-263">Week(s)</span></span>|  
|<span data-ttu-id="afd6a-264">M</span><span class="sxs-lookup"><span data-stu-id="afd6a-264">M</span></span>|<span data-ttu-id="afd6a-265">Måned(er)</span><span class="sxs-lookup"><span data-stu-id="afd6a-265">Month(s)</span></span>|  
|<span data-ttu-id="afd6a-266">K</span><span class="sxs-lookup"><span data-stu-id="afd6a-266">Q</span></span>|<span data-ttu-id="afd6a-267">Kvartal(er)</span><span class="sxs-lookup"><span data-stu-id="afd6a-267">Quarter(s)</span></span>|  
|<span data-ttu-id="afd6a-268">Å</span><span class="sxs-lookup"><span data-stu-id="afd6a-268">Y</span></span>|<span data-ttu-id="afd6a-269">År</span><span class="sxs-lookup"><span data-stu-id="afd6a-269">Year(s)</span></span>|  

 <span data-ttu-id="afd6a-270">Du kan opprette datoformler på tre måter.</span><span class="sxs-lookup"><span data-stu-id="afd6a-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="afd6a-271">Eksempelet nedenfor viser løpende pluss en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="afd6a-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-272">LU</span><span class="sxs-lookup"><span data-stu-id="afd6a-272">CW</span></span>|<span data-ttu-id="afd6a-273">Løpende uke</span><span class="sxs-lookup"><span data-stu-id="afd6a-273">Current week</span></span>|  
|<span data-ttu-id="afd6a-274">LM</span><span class="sxs-lookup"><span data-stu-id="afd6a-274">CM</span></span>|<span data-ttu-id="afd6a-275">Løpende måned</span><span class="sxs-lookup"><span data-stu-id="afd6a-275">Current month</span></span>|  

 <span data-ttu-id="afd6a-276">Eksempelet nedenfor viser et tall og en tidsangivelse.</span><span class="sxs-lookup"><span data-stu-id="afd6a-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="afd6a-277">Et tall kan ikke være større enn 9999.</span><span class="sxs-lookup"><span data-stu-id="afd6a-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-278">10D</span><span class="sxs-lookup"><span data-stu-id="afd6a-278">10D</span></span>|<span data-ttu-id="afd6a-279">10 dager fra i dag</span><span class="sxs-lookup"><span data-stu-id="afd6a-279">10 days from today</span></span>|  
|<span data-ttu-id="afd6a-280">2U</span><span class="sxs-lookup"><span data-stu-id="afd6a-280">2W</span></span>|<span data-ttu-id="afd6a-281">2 uker fra i dag</span><span class="sxs-lookup"><span data-stu-id="afd6a-281">2 weeks from today</span></span>|  

 <span data-ttu-id="afd6a-282">Eksempelet nedenfor viser en tidsangivelse og et tall.</span><span class="sxs-lookup"><span data-stu-id="afd6a-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-283">D10</span><span class="sxs-lookup"><span data-stu-id="afd6a-283">D10</span></span>|<span data-ttu-id="afd6a-284">Den neste 10. dag av en måned</span><span class="sxs-lookup"><span data-stu-id="afd6a-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="afd6a-285">UD4</span><span class="sxs-lookup"><span data-stu-id="afd6a-285">WD4</span></span>|<span data-ttu-id="afd6a-286">Neste 4. dag av en uke (torsdag)</span><span class="sxs-lookup"><span data-stu-id="afd6a-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="afd6a-287">Eksempelet nedenfor viser hvordan du kan kombinere disse tre formlene hvis du trenger det.</span><span class="sxs-lookup"><span data-stu-id="afd6a-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-288">LM+10D</span><span class="sxs-lookup"><span data-stu-id="afd6a-288">CM+10D</span></span>|<span data-ttu-id="afd6a-289">Løpende måned + 10 dager</span><span class="sxs-lookup"><span data-stu-id="afd6a-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="afd6a-290">Følgende eksempel viser hvordan du kan bruke minus-tegn til å indikere en dato i fortiden.</span><span class="sxs-lookup"><span data-stu-id="afd6a-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="afd6a-291">-1Å</span><span class="sxs-lookup"><span data-stu-id="afd6a-291">-1Y</span></span>|<span data-ttu-id="afd6a-292">1 år siden fra i dag</span><span class="sxs-lookup"><span data-stu-id="afd6a-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="afd6a-293">Se også</span><span class="sxs-lookup"><span data-stu-id="afd6a-293">See Also</span></span>  
 [<span data-ttu-id="afd6a-294">Søke etter, filtrere og sortere data</span><span class="sxs-lookup"><span data-stu-id="afd6a-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="afd6a-295">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="afd6a-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

