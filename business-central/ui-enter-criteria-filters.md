---
title: Sortere, søke etter og filtrere oversikter | Microsoft-dokumentasjon
description: Økt effektivitet i oversikter ved å søke på tvers av data, sortere kolonner og forbedring av resultater ved hjelp av filtersymboler og tastatursnarveier.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 11/16/2020
ms.author: jswymer
ms.openlocfilehash: d682f9e66075348785329cd13a12c3e02d0993c4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385852"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="2b1b0-103">Sortere, søke etter og filtrere</span><span class="sxs-lookup"><span data-stu-id="2b1b0-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="2b1b0-104">Det finnes et par ting du kan gjøre som hjelper deg med å skanne, finne og begrense poster i en liste eller i en rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="2b1b0-105">Dette omfatter sortering, søk og filtrering.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="2b1b0-106">Du kan bruke noen av eller alle disse samtidig til å finne eller analysere data raskt.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="2b1b0-107">For rapporter og XML-porter kan du definere filtre som i lister for å avgrense hvilke data som skal inkluderes i rapporten eller XMLport, men du kan ikke sortere og søke.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="2b1b0-108">Når du viser dataene som fliser, kan du søke etter og bruke filtrering.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="2b1b0-109">Hvis du vil bruke hele settet med avanserte funksjoner for å sortere, søke og filtrere, velger du ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre") for å vise postene som en liste.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="2b1b0-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="2b1b0-110">Sorting</span></span>

<span data-ttu-id="2b1b0-111">Sortering gjør det enkelt å få et raskt overblikk over dataene.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="2b1b0-112">Hvis du for eksempel har mange kunder, kan du velge å sortere dem etter **Kundenr.**, **Valutakode** eller **Lands-/områdekode** for å få nødvendig oversikt.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="2b1b0-113">Hvis du vil sortere en liste, kan du:</span><span class="sxs-lookup"><span data-stu-id="2b1b0-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="2b1b0-114">velge en kolonneoverskriftstekst for å veksle mellom stigende og synkende rekkefølge, eller</span><span class="sxs-lookup"><span data-stu-id="2b1b0-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="2b1b0-115">velge rullegardinpilen i kolonneoverskriften, og deretter velge handlingen **Stigende** eller **Synkende**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="2b1b0-116">Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="2b1b0-117">Søke</span><span class="sxs-lookup"><span data-stu-id="2b1b0-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="2b1b0-118">Øverst på hver listeside er det en ![Søkeliste](media/ui-search/search-list.png "Søkeliste-ikon") **Søk**-handling som gir en rask og enkel måte å redusere postene i en oversikt på, og viser bare postene som inneholder dataene du interessert i å se på.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="2b1b0-119">For å søke velger du **Søk**-handlingen, og deretter skriver inn teksten som du søker etter, i boksen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="2b1b0-120">Du kan skrive inn bokstaver, tall og andre symboler.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="2b1b0-121">Vanligvis vil søket forsøke å samsvare tekst i alle felt.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="2b1b0-122">Det skiller ikke mellom store og små bokstaver og samsvarer tekst plassert hvor som helst i feltet, ved begynnelsen, ved slutten eller i midten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="2b1b0-123">Du kan trykke **F3** for å aktivere og deaktivere søkeboksen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="2b1b0-124">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="2b1b0-125">Søket vil ikke tilsvare verdier i bilder, BLOB-felt, FlowFilters, FlowFields og andre felt som ikke er en del av en tabell.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="2b1b0-126">Finjustere søket med filterkriterier</span><span class="sxs-lookup"><span data-stu-id="2b1b0-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="2b1b0-127">Du kan foreta et mer nøyaktig søk ved å bruke filteroperatorer, uttrykk og filterkoder.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="2b1b0-128">I motsetning til filtrering brukes disse på tvers av alle felter når de brukes i søkefeltet, noe som gjør dem mindre effektive enn filtrering.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="2b1b0-129">Hvis du vil finne bare feltverdiene som nøyaktig samsvarer med hele teksten og store/små bokstaver, setter du tekst mellom enkle anførselstegn `''` (for eksempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="2b1b0-130">Hvis du vil finne bare feltverdiene som starter med en viss tekst og store/små bokstaver, setter du `*` etter søketeksten (for eksempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="2b1b0-131">Hvis du vil finne bare feltverdiene som slutter med en viss tekst og store/små bokstaver, setter du `*` før søketeksten (for eksempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="2b1b0-132">Når du bruker `''` eller `*`, søket skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="2b1b0-133">Hvis du vil at søket ikke skal skille mellom store og små bokstaver, setter du inn `@` før teksten (for eksempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="2b1b0-134">Tabellen nedenfor inneholder eksempler som forklarer hvordan du kan bruke søket.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="2b1b0-135">Søkekriterier</span><span class="sxs-lookup"><span data-stu-id="2b1b0-135">Search Criteria</span></span>|<span data-ttu-id="2b1b0-136">Finner...</span><span class="sxs-lookup"><span data-stu-id="2b1b0-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="2b1b0-137">eller</span><span class="sxs-lookup"><span data-stu-id="2b1b0-137">or</span></span> <br />`Man`|<span data-ttu-id="2b1b0-138">Alle poster med felt som inneholder teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="2b1b0-139">For eksempel **Manchester**, **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="2b1b0-140">Alle poster med felt som inneholder bare teksten **Man**, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="2b1b0-141">Alle poster med felt som starter med teksten <b>Man</b>, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="2b1b0-142">For eksempel **Manchester**, men ikke **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="2b1b0-143">Alle poster med felt som starter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="2b1b0-144">For eksempel **Manchester** og **manuell**, men ikke **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="2b1b0-145">Alle poster som slutter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="2b1b0-146">For eksempel **Sportsman**, men ikke **Manchester** eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="2b1b0-147">Filtrering</span><span class="sxs-lookup"><span data-stu-id="2b1b0-147">Filtering</span></span>

<span data-ttu-id="2b1b0-148">Filtrering er en mer avansert og allsidig måte å kontrollere hvilke poster som tas med i en liste, rapport eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="2b1b0-149">Det finnes to viktige forskjeller mellom søking og filtrering, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="2b1b0-150">**Søke**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-150">**Searching**</span></span> | <span data-ttu-id="2b1b0-151">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="2b1b0-152">**Gjeldende felt**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-152">**Applicable Fields**</span></span> | <span data-ttu-id="2b1b0-153">Søker i alle feltene som vises på siden.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="2b1b0-154">Filtrerer ett eller flere felt hver for seg, og du kan velge fra et hvilket som helst felt i tabellen, inkludert felt som ikke vises på siden.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="2b1b0-155">**Avstemming**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-155">**Matching**</span></span> | <span data-ttu-id="2b1b0-156">Viser poster med felter som samsvarer med søketeksten, uavhengig av store/små bokstaver i teksten eller plassering av teksten i feltet.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="2b1b0-157">Viser poster der feltet samsvarer med filteret nøyaktig, og skiller mellom store/små bokstaver i teksten, med mindre spesielle filtersymboler er angitt.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="2b1b0-158">Med filtrering kan du vise poster for bestemte konti eller kunder, datoer, beløp og annen informasjon ved å angi filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="2b1b0-159">Bare poster som samsvarer med kriteriene, vises i oversikten eller inkluderes i rapporten, den satsvise jobben eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="2b1b0-160">Hvis du angir kriterier for flere felt, vises bare poster som samsvarer med alle kriteriene.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="2b1b0-161">For lister vises filtrene i en filtreringsrute som vises til venstre for listen når du aktiverer den.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="2b1b0-162">For rapporter, kjørsler og XML-porter vises filtrene direkte på forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="2b1b0-163">Filtrere med alternativfelt</span><span class="sxs-lookup"><span data-stu-id="2b1b0-163">Filtering with Option Fields</span></span>

<span data-ttu-id="2b1b0-164">Når det gjelder «vanlige» felt som inneholder data, oppsettdata eller forretningsdata, kan du angi filtre både ved å merke dataene og skrive inn filterverdier, og du kan bruke symboler til å definere avanserte filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="2b1b0-165">Hvis du vil ha mer informasjon, kan du se [Angi filterkriterier](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="2b1b0-166">For felt av typen **Alternativ** kan du imidlertid bare angi et filter ved å velge ett eller flere alternativer fra en rullegardinliste med de tilgjengelige alternativene.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="2b1b0-167">Et eksempel på et alternativfelt er feltet **Status** på siden **Salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1b0-168">Når du velger flere alternativer som filterverdi, defineres relasjonene mellom alternativene som *ELLER*.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="2b1b0-169">Hvis du for eksempel velger både avmerkingsboksen **Åpen** og **Frigitt** i filterfeltet **Status** på siden **Salgsordrer**, betyr det at salgsordrer som enten er åpne eller frigitte, vises.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="2b1b0-170">Definere filtre på oversikter</span><span class="sxs-lookup"><span data-stu-id="2b1b0-170">Setting Filters on Lists</span></span>

<span data-ttu-id="2b1b0-171">I lister kan du definere filtre ved hjelp av filtreringsruten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="2b1b0-172">Hvis du vil vise filtreringsruten for en liste, velger du rullegardinpilen ved siden av navnet på siden, og deretter velger du handlingen **Vis filterrute**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="2b1b0-173">Du kan eventuelt trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="2b1b0-174">Hvis du vil vise filtreringsruten for en kolonne på en liste, velger du rullegardinpilen, og deretter velger du handlingen **Filter**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="2b1b0-175">Du kan eventuelt trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="2b1b0-176">Filtreringsruten åpnes med den valgte kolonnen vist som et filtreringfelt i delen **Filtrer listen etter**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="2b1b0-177">Filtreringsruten viser gjeldende filtre for en liste og gjør det mulig å angi egendefinerte filtre på ett eller flere felt ved å velge handlingen **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="2b1b0-178">En filtreringsrute er inndelt i tre deler: **Visninger**, **Filtrer listen etter** og **Filtrer totaler etter**:</span><span class="sxs-lookup"><span data-stu-id="2b1b0-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="2b1b0-179">**Visninger**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-179">**Views**</span></span>

  <span data-ttu-id="2b1b0-180">Enkelte lister inkluderer delen **Visninger**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="2b1b0-181">Visninger er variasjoner av listen som er forhåndsdefinert med filtre.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="2b1b0-182">Du kan definere og lagre så mange visninger som du ønsker per liste.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="2b1b0-183">Visningene vil være tilgjengelige på alle enheter du logger på.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="2b1b0-184">Hvis du vil ha mer informasjon, kan du se [Lagre og tilpasse listevisninger](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="2b1b0-185">**Filtrer listen etter**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-185">**Filter list by**</span></span>

  <span data-ttu-id="2b1b0-186">Det er i denne inndelingen du legger til filtre på bestemte felt for å redusere antall poster som vises.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="2b1b0-187">Hvis du vil legge til et filter, velger du **+ Filter**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="2b1b0-188">Skriv deretter inn navnet på feltet du vil filtrere listen etter, eller velg et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="2b1b0-189">**Filtrer totaler etter**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-189">**Filter totals by**</span></span>

  <span data-ttu-id="2b1b0-190">Enkelte lister som viser beregnede felt, for eksempel beløp og antall, inkluderer delen **Filtrer totaler etter**, der du kan justere forskjellige dimensjoner som påvirker beregninger.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="2b1b0-191">Hvis du vil legge til et filter, velger du **+ Filter**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="2b1b0-192">Skriv deretter inn navnet på feltet du vil filtrere listen etter, eller velg et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2b1b0-193">Filtre i delen **Filtrer totaler etter** kontrolleres av FlowFilters i utformingen av siden.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="2b1b0-194">For teknisk Informasjon, se [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="2b1b0-195">Du kan angi et enkelt filter direkte i en liste ved hjelp av filtreringsruten, det vil si et filter som viser bare poster med samme verdi som i den valgte cellen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="2b1b0-196">Velg en celle i listen, velg rullegardinpilen, og velg deretter handlingen **Filtrer på denne verdien**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="2b1b0-197">Du kan eventuelt trykke på **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="2b1b0-198">Definere filtre i rapporter, kjørsler og XML-porter</span><span class="sxs-lookup"><span data-stu-id="2b1b0-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="2b1b0-199">For rapporter og XML-porter vises filtrene direkte på forespørselssiden.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="2b1b0-200">På forespørselssiden vises de sist brukte filtrene i henhold til valget i feltet **Bruk standardverdi fra**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="2b1b0-201">Hvis du vil ha mer informasjon, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="2b1b0-202">Hoveddelen for **Filter** viser standardfilterfeltene du bruker til å avgrense hvilke poster som skal tas med i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="2b1b0-203">Hvis du vil legge til et filter, velger du **+ Filter**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="2b1b0-204">Skriv deretter inn navnet på feltet du vil filtrere etter, eller velg et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="2b1b0-205">I delen **Filtrer totaler etter** kan du justere ulike dimensjoner som påvirker beregninger i rapporten eller XMLport.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="2b1b0-206">Hvis du vil legge til et filter, velger du **+ Filter**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="2b1b0-207">Skriv deretter inn navnet på feltet du vil filtrere etter, eller velg et felt fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="2b1b0-208">Angi filtervilkår</span><span class="sxs-lookup"><span data-stu-id="2b1b0-208">Entering Filter Criteria</span></span>

<span data-ttu-id="2b1b0-209">Både i filtreringsruten og på forespørselssiden angir du filterkriteriene i boksen under filterfeltet.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="2b1b0-210">Typen filterfelt bestemmer hvilke kriterier du kan angi.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="2b1b0-211">For eksempel kan filtrering av et felt som har faste verdier, gjøre at du bare kan velge mellom disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="2b1b0-212">Du finner mer informasjon om spesielle filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtersymboler](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="2b1b0-213">Kolonner som allerede har filtre, angis av ikonet ![filterikon](media/ui-search/filter-icon.png "Filter-ikon") i kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="2b1b0-214">Hvis du vil fjerne et filter, velger du rullegardinpilen, og deretter velger du handlingen **Fjern filter**.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="2b1b0-215">Raskere søk analyse av data ved hjelp av kombinasjoner av tastatursnarveier.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="2b1b0-216">Du kan for eksempel velge et felt ved å bruke **Alt+Skift+F3** for å legge til feltet i filtreringsruten, skrive inn filterkriteriene, bruke **Ctrl+Enter** til å returnere til radene, velge et annet felt og bruke **Alt+F3** til å filtrere til den verdien.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="2b1b0-217">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="2b1b0-218"><a name="FilterCriteria"> </a>Filterkriterier og -operatorer</span><span class="sxs-lookup"><span data-stu-id="2b1b0-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="2b1b0-219">Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="2b1b0-220">Men det er også et sett med spesialtegn du kan bruke som operatorer, til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="2b1b0-221">Følgende avsnitt beskriver disse symbolene og hvordan de brukes som operatorer i filtre.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="2b1b0-222">Hvis du vil ha mer informasjon om filtrering av datoer og klokkeslett, kan du se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="2b1b0-223">Det kan oppstå situasjoner der verdien du vil filtrere på, inneholder et symbol som er en operator.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="2b1b0-224">Hvis du vil ha mer informasjon om hvordan du håndterer disse situasjonene, kan du se [Filtrere etter verdier som inneholder symboler](#symbols) for å få mer informasjon om hvordan du håndterer denne situasjonen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="2b1b0-225">Hvis det er mer enn 200 operatører i ett enkelt filter, vil systemet automatisk gruppere enkelte uttrykk i parenteser `()` for å behandle det.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="2b1b0-226">Dette har ingen innvirkning på filteret eller resultatet.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="2b1b0-227">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="2b1b0-227">(..) Interval</span></span>

|<span data-ttu-id="2b1b0-228">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-228">Sample Expression</span></span>|<span data-ttu-id="2b1b0-229">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="2b1b0-230">Tall fra og med 1100 til og med 2100</span><span class="sxs-lookup"><span data-stu-id="2b1b0-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="2b1b0-231">Tall til og med 2500</span><span class="sxs-lookup"><span data-stu-id="2b1b0-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="2b1b0-232">Datoer til og med 31.12.00</span><span class="sxs-lookup"><span data-stu-id="2b1b0-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="2b1b0-233">Opplysninger for regnskapsperiode 8 og fremover</span><span class="sxs-lookup"><span data-stu-id="2b1b0-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="2b1b0-234">Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="2b1b0-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="2b1b0-235">Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid</span><span class="sxs-lookup"><span data-stu-id="2b1b0-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="2b1b0-236">Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="2b1b0-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="2b1b0-237">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="2b1b0-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="2b1b0-238">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-238">Sample Expression</span></span>|<span data-ttu-id="2b1b0-239">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="2b1b0-240">Tall med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="2b1b0-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="2b1b0-241">(<>) Ikke lik med</span><span class="sxs-lookup"><span data-stu-id="2b1b0-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="2b1b0-242">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-242">Sample Expression</span></span>|<span data-ttu-id="2b1b0-243">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="2b1b0-244">Alle tall unntatt 0</span><span class="sxs-lookup"><span data-stu-id="2b1b0-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="2b1b0-245">I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="2b1b0-246"><>A\* betyr for eksempel ikke lik noen tekst som begynner med A.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="2b1b0-247">(>) Større enn</span><span class="sxs-lookup"><span data-stu-id="2b1b0-247">(>) Greater than</span></span>  

|<span data-ttu-id="2b1b0-248">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-248">Sample Expression</span></span>|<span data-ttu-id="2b1b0-249">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="2b1b0-250">Tall som er større enn 1200</span><span class="sxs-lookup"><span data-stu-id="2b1b0-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="2b1b0-251">(>=) Større enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="2b1b0-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="2b1b0-252">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-252">Sample Expression</span></span>|<span data-ttu-id="2b1b0-253">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="2b1b0-254">Tall som er større enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="2b1b0-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="2b1b0-255">(<) Mindre enn</span><span class="sxs-lookup"><span data-stu-id="2b1b0-255">(<) Less than</span></span>  

|<span data-ttu-id="2b1b0-256">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-256">Sample Expression</span></span>|<span data-ttu-id="2b1b0-257">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="2b1b0-258">Tall som er mindre enn 1200</span><span class="sxs-lookup"><span data-stu-id="2b1b0-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="2b1b0-259">(<=) Mindre enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="2b1b0-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="2b1b0-260">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-260">Sample Expression</span></span>|<span data-ttu-id="2b1b0-261">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="2b1b0-262">Tall som er mindre enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="2b1b0-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="2b1b0-263">(&) Og</span><span class="sxs-lookup"><span data-stu-id="2b1b0-263">(&) And</span></span>  

|<span data-ttu-id="2b1b0-264">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-264">Sample Expression</span></span>|<span data-ttu-id="2b1b0-265">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="2b1b0-266">Numre som er større enn 200, men mindre enn 1 200.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="2b1b0-267">('') Finne et nøyaktig tegntreff</span><span class="sxs-lookup"><span data-stu-id="2b1b0-267">('') An exact character match</span></span>  

|<span data-ttu-id="2b1b0-268">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-268">Sample Expression</span></span>|<span data-ttu-id="2b1b0-269">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="2b1b0-270">Tekst som samsvarer nøyaktig med **man** og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="2b1b0-271">(@) Skiller ikke mellom små og store bokstaver</span><span class="sxs-lookup"><span data-stu-id="2b1b0-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="2b1b0-272">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-272">Sample Expression</span></span>|<span data-ttu-id="2b1b0-273">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="2b1b0-274">Tekst som begynner med **man** og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="2b1b0-275">(\*) Et ubegrenset antall ukjente tegn</span><span class="sxs-lookup"><span data-stu-id="2b1b0-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="2b1b0-276">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-276">Sample Expression</span></span>|<span data-ttu-id="2b1b0-277">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="2b1b0-278">Tekst som inneholder **A/S** og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="2b1b0-279">Tekst som slutter med **A/S** og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="2b1b0-280">Tekst som begynner med **A/S** og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="2b1b0-281">(?) Ett ukjent tegn</span><span class="sxs-lookup"><span data-stu-id="2b1b0-281">(?) One unknown character</span></span>  

|<span data-ttu-id="2b1b0-282">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-282">Sample Expression</span></span>|<span data-ttu-id="2b1b0-283">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="2b1b0-284">Tekst som for eksempel **Hansen** eller **Hanson**</span><span class="sxs-lookup"><span data-stu-id="2b1b0-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="2b1b0-285">Kombinerte formatuttrykk</span><span class="sxs-lookup"><span data-stu-id="2b1b0-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="2b1b0-286">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-286">Sample Expression</span></span>|<span data-ttu-id="2b1b0-287">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="2b1b0-288">Nummer 5999 og numrene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="2b1b0-289">Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="2b1b0-290">Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="2b1b0-291">Filtrere etter verdier som inneholder symboler</span><span class="sxs-lookup"><span data-stu-id="2b1b0-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="2b1b0-292">Det kan være tilfeller der feltverdier inneholder ett av følgende symboler:</span><span class="sxs-lookup"><span data-stu-id="2b1b0-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="2b1b0-293">(</span><span class="sxs-lookup"><span data-stu-id="2b1b0-293">(</span></span>
- <span data-ttu-id="2b1b0-294">)</span><span class="sxs-lookup"><span data-stu-id="2b1b0-294">)</span></span>
- =
- <span data-ttu-id="2b1b0-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="2b1b0-295">&#124;</span></span>

<span data-ttu-id="2b1b0-296">Hvis du vil filtrere etter noen av disse symbolene, plasserer du filteruttrykket i anførselstegn ('').</span><span class="sxs-lookup"><span data-stu-id="2b1b0-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="2b1b0-297">Hvis du for eksempel vil filtrere på poster som begynner med teksten *J & V*, er filteruttrykket `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="2b1b0-298">Dette kravet er ikke nødvendig for andre symboler.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="2b1b0-299"><a name="FilterTokens"> </a>Filtersymboler</span><span class="sxs-lookup"><span data-stu-id="2b1b0-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="2b1b0-300">Når du angir filterkriterier, kan du også skrive inn ord som har spesiell betydning, som kalles filtersymboler.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="2b1b0-301">Når du har angitt symbolordet, erstattes ordet av verdien eller verdiene det representerer.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="2b1b0-302">Filterkoder gjør filtreringen enklere ved å redusere behovet for å navigere til en annen side for å slå opp verdiene du vil legge til i filteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="2b1b0-303">Tabellen nedenfor beskriver noen av symbolene du kan bruke som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="2b1b0-304">Organisasjonen kan bruke egendefinerte symboler.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="2b1b0-305">Hvis du vil vite mer om det fullstendige settet med symboler du kan bruke, eller legge til flere egendefinerte symboler, kontakt systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="2b1b0-306">For teknisk informasjon, se [Legge til filtersymboler](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="2b1b0-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="2b1b0-307">(%me eller %userid) Poster som er tilordnet til deg</span><span class="sxs-lookup"><span data-stu-id="2b1b0-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="2b1b0-308">Bruk `%me` eller `%userid` når du filtrerer felt som inneholder bruker-ID-en, for eksempel feltet **Tilordnet til bruker-ID**, for å vise alle postene som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="2b1b0-309">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-309">Sample Expression</span></span>|<span data-ttu-id="2b1b0-310">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="2b1b0-311">eller</span><span class="sxs-lookup"><span data-stu-id="2b1b0-311">or</span></span><br />`%userid`|<span data-ttu-id="2b1b0-312">Poster som er knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="2b1b0-313">(%mycustomers) Kunder i Mine kunder</span><span class="sxs-lookup"><span data-stu-id="2b1b0-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="2b1b0-314">Bruk `%mycustomers` i kundens **Nummer**-felt for å vise alle postene for kunder som er inkludert i listen **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="2b1b0-315">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-315">Sample Expression</span></span>|<span data-ttu-id="2b1b0-316">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="2b1b0-317">Kunder i vinduet **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="2b1b0-318">(%myitems) Varer i Mine varer</span><span class="sxs-lookup"><span data-stu-id="2b1b0-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="2b1b0-319">Bruk `%myitems` i varens **Nummer**-felt for å vise alle postene for varer som er inkludert i listen **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="2b1b0-320">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-320">Sample Expression</span></span>|<span data-ttu-id="2b1b0-321">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="2b1b0-322">Varer i vinduet **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="2b1b0-323">(%myvendors) Leverandører i Mine leverandører</span><span class="sxs-lookup"><span data-stu-id="2b1b0-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="2b1b0-324">Bruk `%myvendors` i leverandørens **Nummer**-felt for å vise alle postene for leverandører som er inkludert i listen **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="2b1b0-325">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2b1b0-325">Sample Expression</span></span>|<span data-ttu-id="2b1b0-326">Viste poster</span><span class="sxs-lookup"><span data-stu-id="2b1b0-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="2b1b0-327">Leverandører i vinduet **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="2b1b0-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="2b1b0-328">Se også</span><span class="sxs-lookup"><span data-stu-id="2b1b0-328">See Also</span></span>

[<span data-ttu-id="2b1b0-329">Vanlige spørsmål om søk og filtrering</span><span class="sxs-lookup"><span data-stu-id="2b1b0-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="2b1b0-330">Lagre og tilpasse listevisninger</span><span class="sxs-lookup"><span data-stu-id="2b1b0-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="2b1b0-331">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2b1b0-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]