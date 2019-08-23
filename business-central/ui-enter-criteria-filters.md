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
ms.date: 06/13/2019
ms.author: sgroespe
ms.openlocfilehash: 5f3bab58a2387f5bf21042da782756f7b36d4792
ms.sourcegitcommit: f5050fd209b8d66722c81abe48c4c0a6f749a1f7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1740505"
---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="d7c1a-103">Sortere, søke etter og filtrere oversikter</span><span class="sxs-lookup"><span data-stu-id="d7c1a-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="d7c1a-104">Det finnes et par ting du kan gjøre som hjelper deg med å skanne, finne og begrense poster i en oversikt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="d7c1a-105">Dette omfatter sortering, søk og filtrering.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="d7c1a-106">Du kan bruke noen av eller alle disse samtidig til å finne eller analysere data raskt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="d7c1a-107">Når du viser dataene som fliser, kan du søke etter og bruke grunnleggende filtrering.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="d7c1a-108">Hvis du vil bruke hele settet med avanserte funksjoner for å sortere, søke og filtrere velger du ikonet ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste pil venstre") for å vise som en liste.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="d7c1a-109">Sortering</span><span class="sxs-lookup"><span data-stu-id="d7c1a-109">Sorting</span></span>
<span data-ttu-id="d7c1a-110">Sortering gjør det enkelt å få et raskt overblikk over dataene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="d7c1a-111">Hvis du har mange kunder, kan du for eksempel velge å sortere dem etter **Kundenr.**, **Bokføringsgruppe - kunde**, **Valutakode**, **Lands-/områdekode** eller **Mva-organisasjonsnummer** for å få nødvendig oversikt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="d7c1a-112">Hvis du vil sortere en liste, kan du enten velge en kolonneoverskriftstekst og veksle mellom stigende og synkende rekkefølge, eller velge den lille nedpilen i kolonneoverskriften og deretter velge **Stigende** eller **Synkende**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d7c1a-113">Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="d7c1a-114">Søke</span><span class="sxs-lookup"><span data-stu-id="d7c1a-114">Searching</span></span>
<!--## Searching by using the Quick Filter -->
<span data-ttu-id="d7c1a-115">Øverst på hver listeside er det et ![Søkeliste](media/ui-search/search-list.png "Søkeliste-ikon") **Søk**-ikon som gir en rask og enkel måte å redusere postene i en oversikt på, og viser bare postene som inneholder dataene du interessert i å se på.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-115">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="d7c1a-116">For å søke velger du søkeikonet og skriver inn teksten som du søker etter, i boksen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="d7c1a-117">Du kan skrive inn bokstaver, tall og andre symboler.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tuning-the-search"></a><span data-ttu-id="d7c1a-118">Finjustere søket</span><span class="sxs-lookup"><span data-stu-id="d7c1a-118">Fine-tuning the Search</span></span>
<span data-ttu-id="d7c1a-119">Vanligvis prøver Søk å samsvare teksten på tvers av alle feltene. Det skiller ikke mellom store og små bokstaver og samsvarer tekst plassert hvor som helst i feltet (ved begynnelsen, ved slutten eller i midten).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anywhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="d7c1a-120">Du kan imidlertid foreta et mer nøyaktig søk ved hjelp av følgende spesialtegn:</span><span class="sxs-lookup"><span data-stu-id="d7c1a-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="d7c1a-121">Hvis du vil finne bare feltverdiene som nøyaktig samsvarer med hele teksten og store/små bokstaver, setter du tekst mellom enkle anførselstegn `''` (for eksempel `'man'`).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="d7c1a-122">Hvis du vil finne bare feltverdiene som starter med en viss tekst og store/små bokstaver, setter du `*` etter søketeksten (for eksempel `man*`).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="d7c1a-123">Hvis du vil finne bare feltverdiene som slutter med en viss tekst og store/små bokstaver, setter du `*` før søketeksten (for eksempel `*man`).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="d7c1a-124">Når du bruker `''` eller `*`, søket skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="d7c1a-125">Hvis du vil at søket ikke skal skille mellom store og små bokstaver, setter du inn `@` før teksten (for eksempel `@man*`).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="d7c1a-126">Tabellen nedenfor inneholder eksempler som forklarer hvordan du kan bruke søket.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-126">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="d7c1a-127">Søkekriterier</span><span class="sxs-lookup"><span data-stu-id="d7c1a-127">Search Criteria</span></span>|<span data-ttu-id="d7c1a-128">Finner...</span><span class="sxs-lookup"><span data-stu-id="d7c1a-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="d7c1a-129">eller</span><span class="sxs-lookup"><span data-stu-id="d7c1a-129">or</span></span> <br />`Man`|<span data-ttu-id="d7c1a-130">Alle poster med felt som inneholder teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="d7c1a-131">For eksempel **Manchester**, **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="d7c1a-132">Alle poster med felt som inneholder bare teksten **Man**, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="d7c1a-133">Alle poster med felt som starter med teksten <b>Man</b>, og store/små bokstaver må samsvare.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="d7c1a-134">For eksempel **Manchester**, men ikke **manuell** eller **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="d7c1a-135">Alle poster med felt som starter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="d7c1a-136">For eksempel **Manchester** og **manuell**, men ikke **sportsmann**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="d7c1a-137">Alle poster som slutter med teksten **man**, uavhengig av store/små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="d7c1a-138">For eksempel **Sportsman**, men ikke **Manchester** eller **manuell**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="d7c1a-139">Du kan trykke F3 for å aktivere og deaktivere søkeboksen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="d7c1a-140">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)</span><span class="sxs-lookup"><span data-stu-id="d7c1a-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <span data-ttu-id="d7c1a-141"><a name="Filtering"> </a>Filtrering</span><span class="sxs-lookup"><span data-stu-id="d7c1a-141"><a name="Filtering"> </a>Filtering</span></span>
<span data-ttu-id="d7c1a-142">Filtrering er en mer avansert og allsidig måte for å kontrollere hvilke poster som vises i en oversikt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="d7c1a-143">Det finnes to viktige forskjeller mellom søking og filtrering, som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="d7c1a-144">**Søke**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-144">**Searching**</span></span> | <span data-ttu-id="d7c1a-145">**Filtrering**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="d7c1a-146">**Gjeldende felt**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-146">**Applicable fields**</span></span> | <span data-ttu-id="d7c1a-147">Søker i alle feltene som vises på siden.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="d7c1a-148">Filtrerer ett eller flere felt hver for seg, og du kan velge fra et hvilket som helst felt i tabellen, inkludert felt som ikke vises på siden.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="d7c1a-149">**Avstemming**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-149">**Matching**</span></span> | <span data-ttu-id="d7c1a-150">Viser poster med felt som samsvarer med søketeksten, uavhengig av store/små bokstaver eller plassering av teksten.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="d7c1a-151">Viser poster der feltet samsvarer med filteret nøyaktig, og skiller mellom store/små bokstaver, med mindre spesielle filtersymboler er angitt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="d7c1a-152">Med filtrering kan du vise poster for bestemte konti eller kunder, datoer, beløp og annen informasjon ved å angi filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="d7c1a-153">Bare poster som samsvarer med kriteriene, vises.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="d7c1a-154">Hvis du angir kriterier for flere felt, vises bare poster som samsvarer med alle kriteriene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="d7c1a-155">Arbeide i filtreringsruten</span><span class="sxs-lookup"><span data-stu-id="d7c1a-155">Working in the Filter Pane</span></span>

<span data-ttu-id="d7c1a-156">For å vise filtreringsruten kan du velge ![Filtreringsruteikon](media/open-filter-pane-icon.png "Filtreringsruteikon") øverst i oversikten eller trykke på **Skift+F3**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-156">To display the filter pane, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3**.</span></span> <span data-ttu-id="d7c1a-157">For lister i rollesenteret kan du også velge pil ned i nærheten av sidetittelen på navigasjonslinjen over listen og deretter velge **Vis filtreringsrute**, som vist her.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-157">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane** as shown here:</span></span>

<span data-ttu-id="d7c1a-158">![Vis filtreringsrute](media/open-filter-pane.png "Vis filtreringsrute")</span><span class="sxs-lookup"><span data-stu-id="d7c1a-158">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="d7c1a-159">Filtreringsruten viser gjeldende filtre for en liste og gjør det mulig å angi egendefinerte filtre på ett eller flere felt.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-159">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="d7c1a-160">Figuren nedenfor viser et eksempel på en filtreringsrute for en tilbudsliste.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-160">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="d7c1a-161">![Oversikt over filtreringsruten](media/filter-pane-overview.png "Filterikonet")</span><span class="sxs-lookup"><span data-stu-id="d7c1a-161">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="d7c1a-162">En filtreringsrute er inndelt i tre deler: **Visninger**, **Filtrer listen etter** og **Filtrer totaler etter**:</span><span class="sxs-lookup"><span data-stu-id="d7c1a-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="d7c1a-163">**Visninger**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-163">**Views**</span></span>

  <span data-ttu-id="d7c1a-164">Enkelte lister inkluderer **Visninger**-delen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="d7c1a-165">Visninger er variasjoner av listen som er forhåndsdefinert med filtre.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="d7c1a-166">Du kan bytte til en annen visning av listen ved å ganske enkelt velge en annen kobling.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="d7c1a-167">Du kan endre filtrene i en visning midlertidig, men endringene vil ikke lagres permanent.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="d7c1a-168">**Filtrer listen etter**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-168">**Filter list by**</span></span>

  <span data-ttu-id="d7c1a-169">Delen **Filtre listen etter** er der du legger til filtre på bestemte felt for å redusere antall poster som vises.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="d7c1a-170">Hvis du vil legge til et filter, velger du **+ Filter**, velger feltet du vil filtrere fra alle feltene i tabellen, og angir deretter filterkriterier i boksen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="d7c1a-171">**Filtrer totaler etter**</span><span class="sxs-lookup"><span data-stu-id="d7c1a-171">**Filter totals by**</span></span>

  <span data-ttu-id="d7c1a-172">Enkelte lister som viser beregnede felt, for eksempel beløp og antall, inkluderer delen **Filtrer totaler etter**, der du kan justere forskjellige dimensjoner som påvirker beregninger.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="d7c1a-173">For eksempel kan du raskt analysere kontoplanen ved å filtrere beløp etter en bestemt periode, eller du kan vise totalverdiene for ordrer fra et bestemt lager.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="d7c1a-174">Hvis du vil legge til et filter, velger du **+ Filter**, velger én av de forhåndsdefinerte dimensjonene, og legger deretter til filterkriteriene i boksen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d7c1a-175">Filtre i delen **Filtrer totaler etter** kontrolleres av FlowFilters i utformingen av siden.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="d7c1a-176">For teknisk Informasjon, se [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="d7c1a-177">Angi filterkriterier i filtreringsruten</span><span class="sxs-lookup"><span data-stu-id="d7c1a-177">Entering Filter Criteria in the Filter Pane</span></span>
<span data-ttu-id="d7c1a-178">Gjør ett av følgende for å velge et felt som skal filtreres:</span><span class="sxs-lookup"><span data-stu-id="d7c1a-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="d7c1a-179">I filtreringsruten, velg **+ Felt**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="d7c1a-180">Skriv inn navnet på feltet som du ønsker å filtrere, eller velg et felt fra menyen som inneholder alle feltene i tabellen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="d7c1a-181">Velg pil ned i en kolonneoverskrift, og velg deretter **Filter...**. Dette åpner filtreringsruten og legger til kolonnen i filtreringsruten.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="d7c1a-182">Du kan nå skrive inn eller velge filterkriterier i boksen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="d7c1a-183">Typen felt du filtrerer, bestemmer hvilke kriterier du kan angi.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="d7c1a-184">For eksempel kan filtrering av et felt som har faste verdier, gjøre at du bare kan velge mellom disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="d7c1a-185">Du finner mer informasjon om spesielle filtersymboler i [Filterkriterier](#FilterCriteria) og [Filtersymboler](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="d7c1a-186">Kolonner som allerede har filtre, angis av ![filterikonet](media/ui-search/filter-icon.png "filterikonet") i kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="d7c1a-187">Hvis du vil fjerne et filter, velger du kolonneoverskriven og velger deretter **Fjern Filter**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a><span data-ttu-id="d7c1a-188">Angi filterkriterier uten å bruke filtreringsruten</span><span class="sxs-lookup"><span data-stu-id="d7c1a-188">Entering Filter Criteria Without Using the Filter Pane</span></span>
<span data-ttu-id="d7c1a-189">Du kan angi enkeltfiltre direkte fra listen uten å måtte bruke filtreringsruten.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="d7c1a-190">Når et feltet er merket på en rad, kan du bruke **Alt+F3**-hurtigtasten for å vise bare poster som har samme verdi.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="d7c1a-191">Du kan deretter velge et annet felt og bruke samme hurtigast på nytt for å fortsette finjustering av filtrene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="d7c1a-192">Hvis det valgte feltet allerede filtreres, kan du fjerne dette filteret ved hjelp av **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="d7c1a-193">Raskere søk analyse av data ved hjelp av kombinasjoner av tastatursnarveier.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="d7c1a-194">Du kan for eksempel velge et felt ved å bruke**Alt+Skift+F3** for å legge til feltet i filtreringsruten, skrive inn filterkriteriene, bruke **Ctrl+Enter** til å returnere til radene, velge et annet felt og bruke **Alt+F3** til å filtrere til den verdien.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="d7c1a-195">Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](keyboard-shortcuts.md#KeyboardFilter)</span><span class="sxs-lookup"><span data-stu-id="d7c1a-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="d7c1a-196"><a name="FilterCriteria"> </a>Filterkriterier og symboler</span><span class="sxs-lookup"><span data-stu-id="d7c1a-196"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>
<span data-ttu-id="d7c1a-197">Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="d7c1a-198">I tillegg til dette kan du bruke spesielle symboler (eller operatorer) til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-198">In addition, you can use special symbols (or operators) to further filter the results.</span></span> <span data-ttu-id="d7c1a-199">Tabellene nedenfor viser hvilke symboler som kan brukes i filtre.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="d7c1a-200">For dato og klokkeslett kan du også se [Arbeide med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="d7c1a-201">Det kan være tilfeller der feltverdiene inneholder disse symbolene og du vil filtrere på dem.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="d7c1a-202">Hvis du vil gjøre dette, må du ta med filteruttrykket som inneholder symbolet, i anførselstegn ('').</span><span class="sxs-lookup"><span data-stu-id="d7c1a-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="d7c1a-203">Hvis du for eksempel vil filtrere på poster som begynner med teksten *S&R*, er filteruttrykket `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>

<span data-ttu-id="d7c1a-204">Følgende avsnitt beskriver hvordan du bruker de ulike operatorene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-204">The following sections describe how to use the different operators.</span></span>

> [!NOTE]
> <span data-ttu-id="d7c1a-205">Hvis det er mer enn 200 operatører i ett enkelt filter, vil systemet automatisk gruppere enkelte uttrykk i parenteser `()` for å behandle det.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-205">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="d7c1a-206">Dette har ingen innvirkning på filteret eller resultatet.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-206">This has no effect on the filter or the results.</span></span>  

### <a name="-interval"></a><span data-ttu-id="d7c1a-207">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="d7c1a-207">(..) Interval</span></span>

|<span data-ttu-id="d7c1a-208">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-208">Sample Expression</span></span>|<span data-ttu-id="d7c1a-209">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-209">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="d7c1a-210">Tall fra og med 1100 til og med 2100</span><span class="sxs-lookup"><span data-stu-id="d7c1a-210">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="d7c1a-211">Tall til og med 2500</span><span class="sxs-lookup"><span data-stu-id="d7c1a-211">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="d7c1a-212">Datoer til og med 31.12.00</span><span class="sxs-lookup"><span data-stu-id="d7c1a-212">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="d7c1a-213">Opplysninger for regnskapsperiode 8 og fremover</span><span class="sxs-lookup"><span data-stu-id="d7c1a-213">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="d7c1a-214">Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="d7c1a-214">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="d7c1a-215">Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid</span><span class="sxs-lookup"><span data-stu-id="d7c1a-215">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="d7c1a-216">Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="d7c1a-216">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="d7c1a-217">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="d7c1a-217">(&#124;) Either/or</span></span> 

|<span data-ttu-id="d7c1a-218">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-218">Sample Expression</span></span>|<span data-ttu-id="d7c1a-219">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-219">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="d7c1a-220">Tall med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="d7c1a-220">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="d7c1a-221">(<>) Ikke lik med</span><span class="sxs-lookup"><span data-stu-id="d7c1a-221">(<>) Not equal to</span></span>  

|<span data-ttu-id="d7c1a-222">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-222">Sample Expression</span></span>|<span data-ttu-id="d7c1a-223">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-223">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="d7c1a-224">Alle tall unntatt 0</span><span class="sxs-lookup"><span data-stu-id="d7c1a-224">All numbers except 0</span></span><br /><br /> <span data-ttu-id="d7c1a-225">I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-225">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="d7c1a-226"><>A\* betyr for eksempel ikke lik noen tekst som begynner med A.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-226">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="d7c1a-227">(>) Større enn</span><span class="sxs-lookup"><span data-stu-id="d7c1a-227">(>) Greater than</span></span>  

|<span data-ttu-id="d7c1a-228">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-228">Sample Expression</span></span>|<span data-ttu-id="d7c1a-229">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="d7c1a-230">Tall som er større enn 1200</span><span class="sxs-lookup"><span data-stu-id="d7c1a-230">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="d7c1a-231">(>=) Større enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="d7c1a-231">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="d7c1a-232">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-232">Sample Expression</span></span>|<span data-ttu-id="d7c1a-233">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-233">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="d7c1a-234">Tall som er større enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="d7c1a-234">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="d7c1a-235">(<) Mindre enn</span><span class="sxs-lookup"><span data-stu-id="d7c1a-235">(<) Less than</span></span>  

|<span data-ttu-id="d7c1a-236">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-236">Sample Expression</span></span>|<span data-ttu-id="d7c1a-237">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-237">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="d7c1a-238">Tall som er mindre enn 1200</span><span class="sxs-lookup"><span data-stu-id="d7c1a-238">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="d7c1a-239">(<=) Mindre enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="d7c1a-239">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="d7c1a-240">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-240">Sample Expression</span></span>|<span data-ttu-id="d7c1a-241">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="d7c1a-242">Tall som er mindre enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="d7c1a-242">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="d7c1a-243">(&) Og</span><span class="sxs-lookup"><span data-stu-id="d7c1a-243">(&) And</span></span>  

|<span data-ttu-id="d7c1a-244">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-244">Sample Expression</span></span>|<span data-ttu-id="d7c1a-245">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-245">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="d7c1a-246">Numre som er større enn 200, men mindre enn 1 200.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-246">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="d7c1a-247">('') Finne et nøyaktig tegntreff</span><span class="sxs-lookup"><span data-stu-id="d7c1a-247">('') An exact character match</span></span>  

|<span data-ttu-id="d7c1a-248">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-248">Sample Expression</span></span>|<span data-ttu-id="d7c1a-249">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="d7c1a-250">Tekst som samsvarer nøyaktig med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-250">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="d7c1a-251">(@) Skiller ikke mellom små og store bokstaver</span><span class="sxs-lookup"><span data-stu-id="d7c1a-251">(@) Case insensitive</span></span>  

|<span data-ttu-id="d7c1a-252">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-252">Sample Expression</span></span>|<span data-ttu-id="d7c1a-253">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="d7c1a-254">Tekst som begynner med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-254">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="d7c1a-255">(\*) Et ubegrenset antall ukjente tegn</span><span class="sxs-lookup"><span data-stu-id="d7c1a-255">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="d7c1a-256">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-256">Sample Expression</span></span>|<span data-ttu-id="d7c1a-257">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="d7c1a-258">Tekst som inneholder A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-258">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="d7c1a-259">Tekst som slutter med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-259">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="d7c1a-260">Tekst som begynner med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-260">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="d7c1a-261">Du kan ikke bruke `*` når du filtrerer på alternativfelt (opplisting), for eksempel feltet **Status** i salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-261">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="d7c1a-262">Hvis du vil angi et filter for denne typen felt, kan du angi den numeriske verdien som en parameter for filtrering.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-262">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="d7c1a-263">I feltet **Status** i en ordre som har verdiene **Åpen**, **Frigitt**, **Venter på godkjenning** og **Venter på forskudd**, må du bruke verdiene `0`, `1`, `2` og `3` for å filtrere etter disse alternativene.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-263">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="d7c1a-264">(?) Ett ukjent tegn</span><span class="sxs-lookup"><span data-stu-id="d7c1a-264">(?) One unknown character</span></span>  

|<span data-ttu-id="d7c1a-265">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-265">Sample Expression</span></span>|<span data-ttu-id="d7c1a-266">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-266">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="d7c1a-267">Tekst som for eksempel Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="d7c1a-267">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="d7c1a-268">Kombinerte formatuttrykk</span><span class="sxs-lookup"><span data-stu-id="d7c1a-268">Combined Format Expressions</span></span>  

|<span data-ttu-id="d7c1a-269">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-269">Sample Expression</span></span>|<span data-ttu-id="d7c1a-270">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-270">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="d7c1a-271">Nummer 5999 og numrene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-271">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="d7c1a-272">Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-272">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="d7c1a-273">Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-273">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="d7c1a-274"><a name="FilterTokens"> </a>Filtersymboler</span><span class="sxs-lookup"><span data-stu-id="d7c1a-274"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="d7c1a-275">Når du angir filterkriterier, kan du også skrive inn ord som har spesiell betydning, som kalles filtersymboler.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-275">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="d7c1a-276">Når du har angitt symbolordet, erstattes ordet av verdien eller verdiene det representerer.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-276">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="d7c1a-277">Dermed blir filtreringen enklere ved å redusere behovet for å navigere til en annen side for å slå opp verdiene du vil legge til i filteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-277">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="d7c1a-278">Tabellen nedenfor beskriver noen av symbolene du kan bruke som filterkriterier.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-278">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="d7c1a-279">Organisasjonen kan bruke egendefinerte symboler.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-279">Your organization may use custom tokens.</span></span> <span data-ttu-id="d7c1a-280">Hvis du vil vite mer om det fullstendige settet med symboler du kan bruke, eller legge til flere egendefinerte symboler, kontakt systemansvarlig.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-280">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="d7c1a-281">For teknisk informasjon, se [Legge til filtersymboler](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="d7c1a-281">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="d7c1a-282">(%me eller %userid) Poster som er tilordnet til deg</span><span class="sxs-lookup"><span data-stu-id="d7c1a-282">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="d7c1a-283">Bruk `%me` eller `%userid` når du filtrerer felt som inneholder bruker-ID-en, for eksempel feltet **Tilordnet til bruker-ID**, for å vise alle postene som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-283">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="d7c1a-284">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-284">Sample Expression</span></span>|<span data-ttu-id="d7c1a-285">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-285">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="d7c1a-286">eller</span><span class="sxs-lookup"><span data-stu-id="d7c1a-286">or</span></span><br />`%userid`|<span data-ttu-id="d7c1a-287">Poster som er knyttet til brukerkontoen.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-287">Records that are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="d7c1a-288">(%mycustomers) Kunder i Mine kunder</span><span class="sxs-lookup"><span data-stu-id="d7c1a-288">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="d7c1a-289">Bruk `%mycustomers` i kundens **Nummer**-felt for å vise alle postene for kunder som er inkludert i listen **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-289">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="d7c1a-290">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-290">Sample Expression</span></span>|<span data-ttu-id="d7c1a-291">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-291">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="d7c1a-292">Kunder i vinduet **Mine kunder** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-292">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="d7c1a-293">(%myitems) Varer i Mine varer</span><span class="sxs-lookup"><span data-stu-id="d7c1a-293">(%myitems) Items in My Items</span></span>

<span data-ttu-id="d7c1a-294">Bruk `%myitems` i varens **Nummer**-felt for å vise alle postene for varer som er inkludert i listen **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-294">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="d7c1a-295">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-295">Sample Expression</span></span>|<span data-ttu-id="d7c1a-296">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-296">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="d7c1a-297">Varer i vinduet **Mine varer** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-297">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="d7c1a-298">(%myvendors) Leverandører i Mine leverandører</span><span class="sxs-lookup"><span data-stu-id="d7c1a-298">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="d7c1a-299">Bruk `%myvendors` i leverandørens **Nummer**-felt for å vise alle postene for leverandører som er inkludert i listen **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-299">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="d7c1a-300">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d7c1a-300">Sample Expression</span></span>|<span data-ttu-id="d7c1a-301">Viste poster</span><span class="sxs-lookup"><span data-stu-id="d7c1a-301">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="d7c1a-302">Leverandører i vinduet **Mine leverandører** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="d7c1a-302">Vendors in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="d7c1a-303">Se også</span><span class="sxs-lookup"><span data-stu-id="d7c1a-303">See Also</span></span>
<span data-ttu-id="d7c1a-304">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d7c1a-304">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d7c1a-305">Vanlige spørsmål om søking og filtrering</span><span class="sxs-lookup"><span data-stu-id="d7c1a-305">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)
