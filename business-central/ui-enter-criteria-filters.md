---
title: Sortere, søke etter og filtrere oversikter | Microsoft-dokumentasjon
description: Økt effektivitet i oversikter ved å søke på tvers av data, sortere kolonner og forbedring av resultater ved hjelp av effektive filtersymboler og tastatursnarveier.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5c67ea33937ded164626e4c403522a7dc1f3dca0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912574"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="66618-103">Sortere, søke etter og filtrere</span><span class="sxs-lookup"><span data-stu-id="66618-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="66618-104">Det finnes et par ting du kan gjøre som hjelper deg med å skanne, finne og begrense poster i en liste eller i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="66618-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="66618-105">Dette omfatter sortering, søk og filtrering.</span><span class="sxs-lookup"><span data-stu-id="66618-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="66618-106">Du kan bruke noen av eller alle disse samtidig til å finne eller analysere data raskt.</span><span class="sxs-lookup"><span data-stu-id="66618-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="66618-107">For rapporter og XML-porter kan du definere filtre som i lister for å avgrense hvilke data som skal inkluderes i rapporten eller XMLport, men du kan ikke sortere og søke.</span><span class="sxs-lookup"><span data-stu-id="66618-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you cannot sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="66618-108">Når du viser dataene som fliser, kan du søke etter og bruke grunnleggende filtrering.</span><span class="sxs-lookup"><span data-stu-id="66618-108">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="66618-109">Hvis du vil bruke hele settet med avanserte funksjoner for å sortere, søke og filtrere, velger du ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre") for å vise postene som en liste.</span><span class="sxs-lookup"><span data-stu-id="66618-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="66618-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="66618-110">Sorting</span></span>

<span data-ttu-id="66618-111">Sortering gjør det enkelt å få et raskt overblikk over dataene.</span><span class="sxs-lookup"><span data-stu-id="66618-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="66618-112">Hvis du har mange kunder, kan du for eksempel velge å sortere dem etter **Kundenr.**, **Bokføringsgruppe - kunde**, **Valutakode**, **Lands-/områdekode** eller **Mva-organisasjonsnummer** for å få nødvendig oversikt.</span><span class="sxs-lookup"><span data-stu-id="66618-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="66618-113">Hvis du vil sortere en liste, kan du enten velge en kolonneoverskriftstekst og veksle mellom stigende og synkende rekkefølge, eller velge nedpilen i kolonneoverskriften og deretter velge handlingen **Stigende** eller **Synkende**.</span><span class="sxs-lookup"><span data-stu-id="66618-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the drop-down arrow in the column heading, and then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="66618-114">Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.</span><span class="sxs-lookup"><span data-stu-id="66618-114">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="66618-115">Søke</span><span class="sxs-lookup"><span data-stu-id="66618-115">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="66618-116">Øverst på hver listeside er det en ![Søkeliste](media/ui-search/search-list.png "Søkeliste-ikon") **Søk**-handling som gir en rask og enkel måte å redusere postene i en oversikt på, og viser bare postene som inneholder dataene du interessert i å se på.</span><span class="sxs-lookup"><span data-stu-id="66618-116">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="66618-117">For å søke velger du **Søk**-handlingen, og deretter skriver inn teksten som du søker etter, i boksen.</span><span class="sxs-lookup"><span data-stu-id="66618-117">To search, simply choose the **Search** action, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="66618-118">Du kan skrive inn bokstaver, tall og andre symboler.</span><span class="sxs-lookup"><span data-stu-id="66618-118">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tuning-the-search"></a><span data-ttu-id="66618-119">Finjustere søket</span><span class="sxs-lookup"><span data-stu-id="66618-119">Fine-tuning the Search</span></span>

<span data-ttu-id="66618-120">Vanligvis vil søket forsøke å samsvare tekst i alle felt.</span><span class="sxs-lookup"><span data-stu-id="66618-120">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="66618-121">Det skiller ikke mellom store og små bokstaver og samsvarer tekst plassert hvor som helst i feltet, ved begynnelsen, ved slutten eller i midten.</span><span class="sxs-lookup"><span data-stu-id="66618-121">It does not distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

<span data-ttu-id="66618-122">Du kan imidlertid foreta et mer nøyaktig søk ved hjelp av spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="66618-122">However, you can make a more exact search by using special characters.</span></span>

- <span data-ttu-id="66618-123">Hvis du vil finne bare feltverdiene som nøyaktig samsvarer med hele teksten og store/små bokstaver, setter du tekst mellom enkle anførselstegn `''` (for eksempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="66618-123">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="66618-124">Hvis du vil finne bare feltverdiene som starter med en viss tekst og store/små bokstaver, setter du `*` etter søketeksten (for eksempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="66618-124">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="66618-125">Hvis du vil finne bare feltverdiene som slutter med en viss tekst og store/små bokstaver, setter du `*` før søketeksten (for eksempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="66618-125">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="66618-126">Når du bruker `''` eller `*`, søket skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-126">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="66618-127">Hvis du vil at søket ikke skal skille mellom store og små bokstaver, setter du inn `@` før teksten (for eksempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="66618-127">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="66618-128">Tabellen nedenfor inneholder eksempler som forklarer hvordan du kan bruke søket.</span><span class="sxs-lookup"><span data-stu-id="66618-128">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="66618-129">Søkekriterier</span><span class="sxs-lookup"><span data-stu-id="66618-129">Search Criteria</span></span>|<span data-ttu-id="66618-130">Finner...</span><span class="sxs-lookup"><span data-stu-id="66618-130">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="66618-131">eller</span><span class="sxs-lookup"><span data-stu-id="66618-131">or</span></span> <br />`Man`|<span data-ttu-id="66618-132">Alle poster med felt som inneholder teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-132">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="66618-133">For eksempel **Manchester**, **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="66618-133">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="66618-134">Alle poster med felt som inneholder bare teksten **Man**, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="66618-134">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="66618-135">Alle poster med felt som starter med teksten <b>Man</b>, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="66618-135">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="66618-136">For eksempel **Manchester**, men ikke **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="66618-136">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="66618-137">Alle poster med felt som starter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-137">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="66618-138">For eksempel **Manchester** og **manuell**, men ikke **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="66618-138">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="66618-139">Alle poster som slutter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-139">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="66618-140">For eksempel **Sportsman**, men ikke **Manchester** eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="66618-140">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="66618-141">Du kan trykke **F3** for å aktivere og deaktivere søkeboksen.</span><span class="sxs-lookup"><span data-stu-id="66618-141">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="66618-142">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)</span><span class="sxs-lookup"><span data-stu-id="66618-142">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="66618-143">Søket vil ikke tilsvare verdier i bilder, BLOB-felt, FlowFilters, FlowFields og andre felt som ikke er en del av en tabell.</span><span class="sxs-lookup"><span data-stu-id="66618-143">Search will not match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that are not part of a table.</span></span>

## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="66618-144">Filtrering</span><span class="sxs-lookup"><span data-stu-id="66618-144">Filtering</span></span>

<span data-ttu-id="66618-145">Filtrering er en mer avansert og allsidig måte å kontrollere hvilke poster som vises i en liste eller inkluderes i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="66618-145">Filtering provides a more advanced and versatile way of controlling which records display on a list or include in a report or XMLport.</span></span> <span data-ttu-id="66618-146">Det finnes to viktige forskjeller mellom søking og filtrering, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="66618-146">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="66618-147">**Søke**</span><span class="sxs-lookup"><span data-stu-id="66618-147">**Searching**</span></span> | <span data-ttu-id="66618-148">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="66618-148">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="66618-149">**Gjeldende felt**</span><span class="sxs-lookup"><span data-stu-id="66618-149">**Applicable Fields**</span></span> | <span data-ttu-id="66618-150">Søker i alle feltene som vises på siden.</span><span class="sxs-lookup"><span data-stu-id="66618-150">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="66618-151">Filtrerer ett eller flere felt hver for seg, og du kan velge fra et hvilket som helst felt i tabellen, inkludert felt som ikke vises på siden.</span><span class="sxs-lookup"><span data-stu-id="66618-151">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="66618-152">**Avstemming**</span><span class="sxs-lookup"><span data-stu-id="66618-152">**Matching**</span></span> | <span data-ttu-id="66618-153">Viser poster med felt som samsvarer med søketeksten, uavhengig av store/små bokstaver eller plassering av teksten.</span><span class="sxs-lookup"><span data-stu-id="66618-153">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="66618-154">Viser poster der feltet samsvarer med filteret nøyaktig, og skiller mellom store/små bokstaver, med mindre spesielle filtersymboler er angitt.</span><span class="sxs-lookup"><span data-stu-id="66618-154">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="66618-155">Med filtrering kan du vise poster for bestemte konti eller kunder, datoer, beløp og annen informasjon ved å angi filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="66618-155">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="66618-156">Bare poster som samsvarer med kriteriene, vises i oversikten eller inkluderes i rapporten, den satsvise jobben eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="66618-156">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="66618-157">Hvis du angir kriterier for flere felt, vises bare poster som samsvarer med alle kriteriene.</span><span class="sxs-lookup"><span data-stu-id="66618-157">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="66618-158">For lister vises filtrene i en filtreringsrute som vises til venstre for listen når du aktiverer den.</span><span class="sxs-lookup"><span data-stu-id="66618-158">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="66618-159">For rapporter, kjørsler og XML-porter vises filtrene direkte på forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="66618-159">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="66618-160">Filtrere med alternativfelt</span><span class="sxs-lookup"><span data-stu-id="66618-160">Filtering with Option Fields</span></span>

<span data-ttu-id="66618-161">Når det gjelder "vanlige" felt som inneholder data, oppsettdata eller forretningsdata, kan du angi filtre både ved å merke dataene og skrive inn filterverdier, og du kan bruke symboler til å definere avanserte filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="66618-161">For "ordinary" fields that hold data, setup date or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="66618-162">Hvis du vil ha mer informasjon, kan du se [Angi filterkriterier](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="66618-162">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="66618-163">For felt av typen **Alternativ** kan du imidlertid bare angi et filter ved å velge ett eller flere alternativer fra en rullegardinliste med de tilgjengelige alternativene.</span><span class="sxs-lookup"><span data-stu-id="66618-163">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="66618-164">Et eksempel på et alternativfelt er feltet **Status** på siden **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="66618-164">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="66618-165">Når du velger flere alternativer som filterverdi, defineres relasjonene mellom alternativene som *ELLER*.</span><span class="sxs-lookup"><span data-stu-id="66618-165">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="66618-166">Hvis du for eksempel velger både avmerkingsboksen **Åpen** og **Frigitt** i filterfeltet **Status** på siden **Salgsordrer**, betyr det at salgsordrer som enten er åpne eller frigitte, vises.</span><span class="sxs-lookup"><span data-stu-id="66618-166">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="66618-167">Definere filtre på oversikter</span><span class="sxs-lookup"><span data-stu-id="66618-167">Setting Filters on Lists</span></span>

<span data-ttu-id="66618-168">I lister kan du definere filtre ved hjelp av filtreringsruten.</span><span class="sxs-lookup"><span data-stu-id="66618-168">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="66618-169">Hvis du vil vise filtreringsruten for en liste, velger du rullegardinpilen ved siden av navnet på siden, og deretter velger du handlingen **Vis filterrute**.</span><span class="sxs-lookup"><span data-stu-id="66618-169">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="66618-170">Du kan eventuelt trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="66618-170">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="66618-171">Hvis du vil vise filtreringsruten for en kolonne på en liste, velger du rullegardinpilen, og deretter velger du handlingen **Filter**.</span><span class="sxs-lookup"><span data-stu-id="66618-171">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="66618-172">Du kan eventuelt trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="66618-172">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="66618-173">Filtreringsruten åpnes med den valgte kolonnen vist som et filtreringfelt i delen **Filtrer listen etter**.</span><span class="sxs-lookup"><span data-stu-id="66618-173">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="66618-174">Filtreringsruten viser gjeldende filtre for en liste og gjør det mulig å angi egendefinerte filtre på ett eller flere felt ved å velge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="66618-174">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="66618-175">En filtreringsrute er inndelt i tre deler: **Visninger**, **Filtrer listen etter** og **Filtrer totaler etter**:</span><span class="sxs-lookup"><span data-stu-id="66618-175">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="66618-176">**Visninger**</span><span class="sxs-lookup"><span data-stu-id="66618-176">**Views**</span></span>

  <span data-ttu-id="66618-177">Enkelte lister inkluderer delen **Visninger**.</span><span class="sxs-lookup"><span data-stu-id="66618-177">Some lists include the **Views** section.</span></span> <span data-ttu-id="66618-178">Visninger er variasjoner av listen som er forhåndsdefinert med filtre.</span><span class="sxs-lookup"><span data-stu-id="66618-178">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="66618-179">Du kan definere og lagre så mange visninger du vil, per liste, og visningene vil være tilgjengelige på alle enheter du logger på.</span><span class="sxs-lookup"><span data-stu-id="66618-179">You can define and save as many views as you want per list, and the views will be available to you on any device you sign into.</span></span> <span data-ttu-id="66618-180">Hvis du vil ha mer informasjon, kan du se [Lagre og tilpasse listevisninger](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="66618-180">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="66618-181">**Filtrer listen etter**</span><span class="sxs-lookup"><span data-stu-id="66618-181">**Filter list by**</span></span>

  <span data-ttu-id="66618-182">Det er her du legger til filtre på bestemte felt for å redusere antall poster som vises.</span><span class="sxs-lookup"><span data-stu-id="66618-182">This is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="66618-183">Hvis du vil legge til et filter, velger du handlingen **+ Filter**, skriver inn navnet på feltet du vil filtrere listen etter, eller velger et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="66618-183">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="66618-184">**Filtrer totaler etter**</span><span class="sxs-lookup"><span data-stu-id="66618-184">**Filter totals by**</span></span>

  <span data-ttu-id="66618-185">Enkelte lister som viser beregnede felt, for eksempel beløp og antall, inkluderer delen **Filtrer totaler etter**, der du kan justere forskjellige dimensjoner som påvirker beregninger.</span><span class="sxs-lookup"><span data-stu-id="66618-185">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="66618-186">Hvis du vil legge til et filter, velger du handlingen **+ Filter**, skriver inn navnet på feltet du vil filtrere listen etter, eller velger et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="66618-186">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter the list by, or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="66618-187">Filtre i delen **Filtrer totaler etter** kontrolleres av FlowFilters i utformingen av siden.</span><span class="sxs-lookup"><span data-stu-id="66618-187">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="66618-188">For teknisk Informasjon, se [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="66618-188">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="66618-189">Du kan angi et enkelt filter direkte i en liste ved hjelp av filtreringsruten, det vil si et filter som viser bare poster med samme verdi som i den valgte cellen.</span><span class="sxs-lookup"><span data-stu-id="66618-189">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="66618-190">Velg en celle i listen, velg rullegardinpilen, og velg deretter handlingen **Filtrer på denne verdien**.</span><span class="sxs-lookup"><span data-stu-id="66618-190">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="66618-191">Du kan eventuelt trykke på **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="66618-191">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="66618-192">Definere filtre i rapporter, kjørsler og XML-porter</span><span class="sxs-lookup"><span data-stu-id="66618-192">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="66618-193">For rapporter og XML-porter vises filtrene direkte på forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="66618-193">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="66618-194">På forespørselssiden vises de sist brukte filtrene i henhold til valget i feltet **Bruk standardverdi fra**.</span><span class="sxs-lookup"><span data-stu-id="66618-194">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="66618-195">Hvis du vil ha mer informasjon, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="66618-195">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="66618-196">Hoveddelen for **Filter** viser standardfilterfeltene du bruker til å avgrense hvilke poster som skal tas med i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="66618-196">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="66618-197">Hvis du vil legge til et filter, velger du handlingen **+ Filter**, skriver inn navnet på feltet du vil filtrere etter, eller velger et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="66618-197">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="66618-198">I delen **Filtrer totaler etter** kan du justere ulike dimensjoner som påvirker beregninger i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="66618-198">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="66618-199">Hvis du vil legge til et filter, velger du handlingen **+ Filter**, skriver inn navnet på feltet du vil filtrere etter, eller velger et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="66618-199">To add a filter, choose the **+ Filter** action, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="66618-200">Angi filtervilkår</span><span class="sxs-lookup"><span data-stu-id="66618-200">Entering Filter Criteria</span></span>

<span data-ttu-id="66618-201">Både i filtreringsruten og på forespørselssiden angir du filterkriteriene i boksen under filterfeltet.</span><span class="sxs-lookup"><span data-stu-id="66618-201">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="66618-202">Typen filterfelt bestemmer hvilke kriterier du kan angi.</span><span class="sxs-lookup"><span data-stu-id="66618-202">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="66618-203">For eksempel kan filtrering av et felt som har faste verdier, gjøre at du bare kan velge mellom disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="66618-203">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="66618-204">Du finner mer informasjon om spesielle filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtersymboler](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="66618-204">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="66618-205">Kolonner som allerede har filtre, angis av ikonet ![filterikon](media/ui-search/filter-icon.png "Filter-ikon") i kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="66618-205">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="66618-206">Hvis du vil fjerne et filter, velger du rullegardinpilen, og deretter velger du handlingen **Fjern filter**.</span><span class="sxs-lookup"><span data-stu-id="66618-206">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="66618-207">Raskere søk analyse av data ved hjelp av kombinasjoner av tastatursnarveier.</span><span class="sxs-lookup"><span data-stu-id="66618-207">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="66618-208">Du kan for eksempel velge et felt ved å bruke **Alt+Skift+F3** for å legge til feltet i filtreringsruten, skrive inn filterkriteriene, bruke **Ctrl+Enter** til å returnere til radene, velge et annet felt og bruke **Alt+F3** til å filtrere til den verdien.</span><span class="sxs-lookup"><span data-stu-id="66618-208">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="66618-209">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)</span><span class="sxs-lookup"><span data-stu-id="66618-209">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-symbols"></a><span data-ttu-id="66618-210"><a name="FilterCriteria"> </a>Filterkriterier og symboler</span><span class="sxs-lookup"><span data-stu-id="66618-210"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>

<span data-ttu-id="66618-211">Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet.</span><span class="sxs-lookup"><span data-stu-id="66618-211">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="66618-212">I tillegg til dette kan du bruke spesielle symboler (eller operatorer) til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="66618-212">In addition, you can use special symbols (or operators) to further filter the results.</span></span> <span data-ttu-id="66618-213">Tabellene nedenfor viser hvilke symboler som kan brukes i filtre.</span><span class="sxs-lookup"><span data-stu-id="66618-213">The following tables show the symbols that can be used in filters.</span></span> <span data-ttu-id="66618-214">For dato og klokkeslett kan du også se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="66618-214">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="66618-215">Det kan være tilfeller der feltverdiene inneholder disse symbolene og du vil filtrere på dem.</span><span class="sxs-lookup"><span data-stu-id="66618-215">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="66618-216">Hvis du vil gjøre dette, må du ta med filteruttrykket som inneholder symbolet, i anførselstegn ('').</span><span class="sxs-lookup"><span data-stu-id="66618-216">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="66618-217">Hvis du for eksempel vil filtrere på poster som begynner med teksten *S&R*, er filteruttrykket `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="66618-217">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>

<span data-ttu-id="66618-218">Følgende avsnitt beskriver hvordan du bruker de ulike operatorene.</span><span class="sxs-lookup"><span data-stu-id="66618-218">The following sections describe how to use the different operators.</span></span>

> [!NOTE]
> <span data-ttu-id="66618-219">Hvis det er mer enn 200 operatører i ett enkelt filter, vil systemet automatisk gruppere enkelte uttrykk i parenteser `()` for å behandle det.</span><span class="sxs-lookup"><span data-stu-id="66618-219">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="66618-220">Dette har ingen innvirkning på filteret eller resultatet.</span><span class="sxs-lookup"><span data-stu-id="66618-220">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="66618-221">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="66618-221">(..) Interval</span></span>

|<span data-ttu-id="66618-222">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-222">Sample Expression</span></span>|<span data-ttu-id="66618-223">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-223">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="66618-224">Tall fra og med 1100 til og med 2100</span><span class="sxs-lookup"><span data-stu-id="66618-224">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="66618-225">Tall til og med 2500</span><span class="sxs-lookup"><span data-stu-id="66618-225">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="66618-226">Datoer til og med 31.12.00</span><span class="sxs-lookup"><span data-stu-id="66618-226">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="66618-227">Opplysninger for regnskapsperiode 8 og fremover</span><span class="sxs-lookup"><span data-stu-id="66618-227">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="66618-228">Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="66618-228">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="66618-229">Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid</span><span class="sxs-lookup"><span data-stu-id="66618-229">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="66618-230">Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="66618-230">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="66618-231">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="66618-231">(&#124;) Either/or</span></span>

|<span data-ttu-id="66618-232">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-232">Sample Expression</span></span>|<span data-ttu-id="66618-233">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-233">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="66618-234">Tall med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="66618-234">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="66618-235">(<>) Ikke lik med</span><span class="sxs-lookup"><span data-stu-id="66618-235">(<>) Not equal to</span></span>  

|<span data-ttu-id="66618-236">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-236">Sample Expression</span></span>|<span data-ttu-id="66618-237">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-237">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="66618-238">Alle tall unntatt 0</span><span class="sxs-lookup"><span data-stu-id="66618-238">All numbers except 0</span></span><br /><br /> <span data-ttu-id="66618-239">I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk.</span><span class="sxs-lookup"><span data-stu-id="66618-239">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="66618-240"><>A\* betyr for eksempel ikke lik noen tekst som begynner med A.</span><span class="sxs-lookup"><span data-stu-id="66618-240">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="66618-241">(>) Større enn</span><span class="sxs-lookup"><span data-stu-id="66618-241">(>) Greater than</span></span>  

|<span data-ttu-id="66618-242">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-242">Sample Expression</span></span>|<span data-ttu-id="66618-243">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="66618-244">Tall som er større enn 1200</span><span class="sxs-lookup"><span data-stu-id="66618-244">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="66618-245">(>=) Større enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="66618-245">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="66618-246">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-246">Sample Expression</span></span>|<span data-ttu-id="66618-247">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-247">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="66618-248">Tall som er større enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="66618-248">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="66618-249">(<) Mindre enn</span><span class="sxs-lookup"><span data-stu-id="66618-249">(<) Less than</span></span>  

|<span data-ttu-id="66618-250">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-250">Sample Expression</span></span>|<span data-ttu-id="66618-251">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-251">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="66618-252">Tall som er mindre enn 1200</span><span class="sxs-lookup"><span data-stu-id="66618-252">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="66618-253">(<=) Mindre enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="66618-253">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="66618-254">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-254">Sample Expression</span></span>|<span data-ttu-id="66618-255">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-255">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="66618-256">Tall som er mindre enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="66618-256">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="66618-257">(&) Og</span><span class="sxs-lookup"><span data-stu-id="66618-257">(&) And</span></span>  

|<span data-ttu-id="66618-258">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-258">Sample Expression</span></span>|<span data-ttu-id="66618-259">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-259">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="66618-260">Numre som er større enn 200, men mindre enn 1 200.</span><span class="sxs-lookup"><span data-stu-id="66618-260">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="66618-261">('') Finne et nøyaktig tegntreff</span><span class="sxs-lookup"><span data-stu-id="66618-261">('') An exact character match</span></span>  

|<span data-ttu-id="66618-262">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-262">Sample Expression</span></span>|<span data-ttu-id="66618-263">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-263">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="66618-264">Tekst som samsvarer nøyaktig med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-264">Text that matches man exactly and is case sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="66618-265">(@) Skiller ikke mellom små og store bokstaver</span><span class="sxs-lookup"><span data-stu-id="66618-265">(@) Case insensitive</span></span>  

|<span data-ttu-id="66618-266">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-266">Sample Expression</span></span>|<span data-ttu-id="66618-267">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-267">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="66618-268">Tekst som begynner med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-268">Text that starts with man and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="66618-269">(\*) Et ubegrenset antall ukjente tegn</span><span class="sxs-lookup"><span data-stu-id="66618-269">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="66618-270">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-270">Sample Expression</span></span>|<span data-ttu-id="66618-271">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-271">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="66618-272">Tekst som inneholder A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-272">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="66618-273">Tekst som slutter med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-273">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="66618-274">Tekst som begynner med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="66618-274">Text that begins with "Co" and is case sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="66618-275">(?) Ett ukjent tegn</span><span class="sxs-lookup"><span data-stu-id="66618-275">(?) One unknown character</span></span>  

|<span data-ttu-id="66618-276">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-276">Sample Expression</span></span>|<span data-ttu-id="66618-277">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="66618-278">Tekst som for eksempel Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="66618-278">Text such as Hansen or Hanson</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="66618-279">Kombinerte formatuttrykk</span><span class="sxs-lookup"><span data-stu-id="66618-279">Combined Format Expressions</span></span>  

|<span data-ttu-id="66618-280">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-280">Sample Expression</span></span>|<span data-ttu-id="66618-281">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-281">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="66618-282">Nummer 5999 og numrene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="66618-282">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="66618-283">Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="66618-283">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="66618-284">Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="66618-284">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filter-tokens"></a><span data-ttu-id="66618-285"><a name="FilterTokens"> </a>Filtersymboler</span><span class="sxs-lookup"><span data-stu-id="66618-285"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="66618-286">Når du angir filterkriterier, kan du også skrive inn ord som har spesiell betydning, som kalles filtersymboler.</span><span class="sxs-lookup"><span data-stu-id="66618-286">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="66618-287">Når du har angitt symbolordet, erstattes ordet av verdien eller verdiene det representerer.</span><span class="sxs-lookup"><span data-stu-id="66618-287">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="66618-288">Dermed blir filtreringen enklere ved å redusere behovet for å navigere til en annen side for å slå opp verdiene du vil legge til i filteret.</span><span class="sxs-lookup"><span data-stu-id="66618-288">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="66618-289">Tabellen nedenfor beskriver noen av symbolene du kan bruke som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="66618-289">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="66618-290">Organisasjonen kan bruke egendefinerte symboler.</span><span class="sxs-lookup"><span data-stu-id="66618-290">Your organization may use custom tokens.</span></span> <span data-ttu-id="66618-291">Hvis du vil vite mer om det fullstendige settet med symboler du kan bruke, eller legge til flere egendefinerte symboler, kontakt systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="66618-291">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="66618-292">For teknisk informasjon, se [Legge til filtersymboler](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="66618-292">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="66618-293">(%me eller %userid) Poster som er tilordnet til deg</span><span class="sxs-lookup"><span data-stu-id="66618-293">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="66618-294">Bruk `%me` eller `%userid` når du filtrerer felt som inneholder bruker-ID-en, for eksempel feltet **Tilordnet til bruker-ID**, for å vise alle postene som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="66618-294">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="66618-295">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-295">Sample Expression</span></span>|<span data-ttu-id="66618-296">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-296">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="66618-297">eller</span><span class="sxs-lookup"><span data-stu-id="66618-297">or</span></span><br />`%userid`|<span data-ttu-id="66618-298">Poster som er knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="66618-298">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="66618-299">(%mycustomers) Kunder i Mine kunder</span><span class="sxs-lookup"><span data-stu-id="66618-299">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="66618-300">Bruk `%mycustomers` i kundens **Nummer**-felt for å vise alle postene for kunder som er inkludert i listen **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-300">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="66618-301">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-301">Sample Expression</span></span>|<span data-ttu-id="66618-302">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-302">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="66618-303">Kunder i vinduet **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-303">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="66618-304">(%myitems) Varer i Mine varer</span><span class="sxs-lookup"><span data-stu-id="66618-304">(%myitems) Items in My Items</span></span>

<span data-ttu-id="66618-305">Bruk `%myitems` i varens **Nummer**-felt for å vise alle postene for varer som er inkludert i listen **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-305">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="66618-306">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-306">Sample Expression</span></span>|<span data-ttu-id="66618-307">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-307">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="66618-308">Varer i vinduet **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-308">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="66618-309">(%myvendors) Leverandører i Mine leverandører</span><span class="sxs-lookup"><span data-stu-id="66618-309">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="66618-310">Bruk `%myvendors` i leverandørens **Nummer**-felt for å vise alle postene for leverandører som er inkludert i listen **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-310">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="66618-311">Eksempel</span><span class="sxs-lookup"><span data-stu-id="66618-311">Sample Expression</span></span>|<span data-ttu-id="66618-312">Viste poster</span><span class="sxs-lookup"><span data-stu-id="66618-312">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="66618-313">Leverandører i vinduet **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="66618-313">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="66618-314">Se også</span><span class="sxs-lookup"><span data-stu-id="66618-314">See Also</span></span>

[<span data-ttu-id="66618-315">Vanlige spørsmål om søk og filtrering</span><span class="sxs-lookup"><span data-stu-id="66618-315">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="66618-316">Lagre og tilpasse listevisninger</span><span class="sxs-lookup"><span data-stu-id="66618-316">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="66618-317">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66618-317">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
