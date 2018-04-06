---
title: "Søke etter data og angi filterkriterier | Microsoft-dokumentasjon"
description: "Beskriver hvordan du arbeider med filtre, for eksempel hurtigfilter, for å begrense resultatene du får når du søker etter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7fd74ad235e51b1793b02e19834bdb0bd17820b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="80991-103">Søke etter, filtrere og sortere data</span><span class="sxs-lookup"><span data-stu-id="80991-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="80991-104">Det finnes et par ting du kan gjøre som hjelper deg med å finne og skanne poster i en oversikt.</span><span class="sxs-lookup"><span data-stu-id="80991-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="80991-105">Dette omfatter sortering, søk og filtrering.</span><span class="sxs-lookup"><span data-stu-id="80991-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="80991-106">Når du vil søke etter data, for eksempel kundenavn, adresser eller produktgrupper, må du angi kriterier.</span><span class="sxs-lookup"><span data-stu-id="80991-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="80991-107">I søkekriteriene kan du bruke alle tallene og bokstavene du vanligvis kan bruke i det spesifikke feltet.</span><span class="sxs-lookup"><span data-stu-id="80991-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="80991-108">I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="80991-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="80991-109">Det er to måter å søke på: bruke hurtigfilteret eller kolonnefiltre.</span><span class="sxs-lookup"><span data-stu-id="80991-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="80991-110">Sortering</span><span class="sxs-lookup"><span data-stu-id="80991-110">Sorting</span></span>
<span data-ttu-id="80991-111">Sortering gjør det enkelt å få et raskt overblikk over dataene.</span><span class="sxs-lookup"><span data-stu-id="80991-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="80991-112">Hvis du har mange kunder, kan du for eksempel velge å sortere dem etter **Kundenr.**, **Bokføringsgruppe - kunde**, **Valutakode**, **Lands-/regionkode** eller **Mva-organisasjonsnummer** for å få nødvendig oversikt.</span><span class="sxs-lookup"><span data-stu-id="80991-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="80991-113">Hvis du vil sortere en liste, kan du enten velge en kolonneoverskriftstekst og veksle mellom stigende og synkende rekkefølge, eller velge den lille nedpilen i kolonneoverskriften og deretter velge **Stigende** eller **Synkende**.</span><span class="sxs-lookup"><span data-stu-id="80991-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="80991-114">Sortering støttes ikke for bilder, BLOB-felt, FlowFilters og felt som ikke hører til i en tabell.</span><span class="sxs-lookup"><span data-stu-id="80991-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="80991-115">Søke ved hjelp av hurtigfilteret</span><span class="sxs-lookup"><span data-stu-id="80991-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="80991-116">Du kan legge til filtre på alle sider ved hjelp av hurtigfilteret.</span><span class="sxs-lookup"><span data-stu-id="80991-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="80991-117">Hurtigfilteret aktiveres ved å velge forstørrelsesikonet i øvre høyre hjørne på siden.</span><span class="sxs-lookup"><span data-stu-id="80991-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="80991-118">Denne filtreringstypen brukes for rask angivelse av kriterier.</span><span class="sxs-lookup"><span data-stu-id="80991-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="80991-119">Hurtigfilteret gjør det enkelt å filtrere data ved å skrive inn ren tekst, men gir også mange alternativer når det gjelder søkekriterier.</span><span class="sxs-lookup"><span data-stu-id="80991-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="80991-120">Virkemåten for hurtigfilteret er avhengig av om du skriver inn ren tekst eller tekst som inneholder symboler.</span><span class="sxs-lookup"><span data-stu-id="80991-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="80991-121">Hvis du skriver inn ren tekst i søkevilkåret, tolkes søkekriteriene som et søk som ikke skiller mellom store og små bokstaver og som inneholder en bestemt tekst.</span><span class="sxs-lookup"><span data-stu-id="80991-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="80991-122">Hvis du skriver inn tekst med symboler i søkekriteriene, tolkes søkekriteriene nøyaktig slik du skrev det inn, og søket skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="80991-123">Kriterier for hurtigfilter</span><span class="sxs-lookup"><span data-stu-id="80991-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="80991-124">Søkekriterier</span><span class="sxs-lookup"><span data-stu-id="80991-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="80991-125">Tolkes som ...</span><span class="sxs-lookup"><span data-stu-id="80991-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="80991-126">Returnerer ...</span><span class="sxs-lookup"><span data-stu-id="80991-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="80991-127">man</span><span class="sxs-lookup"><span data-stu-id="80991-127">man</span></span></TD>
    <TD><span data-ttu-id="80991-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="80991-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="80991-129">Alle poster som inneholder teksten <b>mann</b> og som ikke skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="80991-130">se</span><span class="sxs-lookup"><span data-stu-id="80991-130">se</span></span></TD>
    <TD><span data-ttu-id="80991-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="80991-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="80991-132">Alle poster som inneholder teksten <b>se</b> og som ikke skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="80991-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="80991-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="80991-134">Begynner med <b>Man</b>, og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="80991-135">Alle poster som starter med teksten <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="80991-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="80991-136">'man'</span><span class="sxs-lookup"><span data-stu-id="80991-136">'man'</span></span></TD>
    <TD><span data-ttu-id="80991-137">En nøyaktig tekst som skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="80991-138">Alle poster som samsvarer nøyaktig med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="80991-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="80991-139">@man\*</span><span class="sxs-lookup"><span data-stu-id="80991-139">@man\*</span></span> </TD>
    <TD><span data-ttu-id="80991-140">Begynner med, og skiller ikke mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="80991-141">Alle poster som starter med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="80991-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="80991-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="80991-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="80991-143">Slutter med, og skiller ikke mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="80991-144">Alle poster som slutter med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="80991-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="80991-145">Du kan ikke bruke et jokertegn når du filtrerer på felt for opplisting, for eksempel feltet **Status** i ordrer.</span><span class="sxs-lookup"><span data-stu-id="80991-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="80991-146">Hvis du vil angi et filter for denne typen felt, kan du angi den numeriske verdien som en parameter for filtrering.</span><span class="sxs-lookup"><span data-stu-id="80991-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="80991-147">I feltet **Status** på en ordre som har verdiene **Åpen**, **Frigitt**, **Venter på godkjenning** og **Venter på forskudd**, må du bruke verdiene **0**, **1**, **2** og **3** for å filtrere etter disse alternativene.</span><span class="sxs-lookup"><span data-stu-id="80991-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="80991-148">Søke ved hjelp av kolonnefiltre</span><span class="sxs-lookup"><span data-stu-id="80991-148">Searching by using column Filters</span></span>
<span data-ttu-id="80991-149">Du kan legge til et filter på én eller flere kolonner i listen.</span><span class="sxs-lookup"><span data-stu-id="80991-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="80991-150">Filtrering på kolonner er mer fleksibelt og avansert enn hurtigfilteret.</span><span class="sxs-lookup"><span data-stu-id="80991-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="80991-151">Slik legger du til et filter på en kolonne</span><span class="sxs-lookup"><span data-stu-id="80991-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="80991-152">Før du legger til et filter, velger du ![Vis som liste](media/ui_show_as_list_icon.png "Vis som liste, pil venstre")-ikonet for å bytte til listevisningen.</span><span class="sxs-lookup"><span data-stu-id="80991-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="80991-153">Velg den nedoverpilen i kolonneoverskriften, og deretter velger du **Filter**.</span><span class="sxs-lookup"><span data-stu-id="80991-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="80991-154">Gjør ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="80991-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="80991-155">Velg *...* ved siden av feltet for å velge en verdi i listen.</span><span class="sxs-lookup"><span data-stu-id="80991-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="80991-156">Angi filterkriterier i feltet.</span><span class="sxs-lookup"><span data-stu-id="80991-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="80991-157">Du kan se neste del for detaljer.</span><span class="sxs-lookup"><span data-stu-id="80991-157">See the next section for details.</span></span>
4. <span data-ttu-id="80991-158">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="80991-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="80991-159">Filterkriterier og symboler</span><span class="sxs-lookup"><span data-stu-id="80991-159">Filter criteria and symbols</span></span>
<span data-ttu-id="80991-160">Når du angir kriterier, kan du bruke alle tallene og bokstavene du normalt kan bruke i feltet.</span><span class="sxs-lookup"><span data-stu-id="80991-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="80991-161">I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="80991-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="80991-162">Tabellene nedenfor viser hvilke symboler som kan brukes i filtre.</span><span class="sxs-lookup"><span data-stu-id="80991-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="80991-163">Det kan være tilfeller der feltverdiene inneholder disse symbolene og du vil filtrere på dem.</span><span class="sxs-lookup"><span data-stu-id="80991-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="80991-164">Hvis du vil gjøre dette, må du ta med filteruttrykket som inneholder symbolet, i anførselstegn ('').</span><span class="sxs-lookup"><span data-stu-id="80991-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="80991-165">Hvis du for eksempel vil filtrere på poster som begynner med teksten *salg*, er filteruttrykket **salg**.</span><span class="sxs-lookup"><span data-stu-id="80991-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R\*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="80991-166">(..) Intervall</span><span class="sxs-lookup"><span data-stu-id="80991-166">(..) Interval</span></span>  
  
|<span data-ttu-id="80991-167">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-167">Sample Expression</span></span>|<span data-ttu-id="80991-168">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="80991-169">1100..2100</span></span>|<span data-ttu-id="80991-170">Tall fra og med 1100 til og med 2100</span><span class="sxs-lookup"><span data-stu-id="80991-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="80991-171">..2500</span><span class="sxs-lookup"><span data-stu-id="80991-171">..2500</span></span>|<span data-ttu-id="80991-172">Tall til og med 2500</span><span class="sxs-lookup"><span data-stu-id="80991-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="80991-173">..12 31 00</span><span class="sxs-lookup"><span data-stu-id="80991-173">..12 31 00</span></span>|<span data-ttu-id="80991-174">Datoer til og med 31.12.00</span><span class="sxs-lookup"><span data-stu-id="80991-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="80991-175">P8..</span><span class="sxs-lookup"><span data-stu-id="80991-175">P8..</span></span>|<span data-ttu-id="80991-176">Opplysninger for regnskapsperiode 8 og fremover</span><span class="sxs-lookup"><span data-stu-id="80991-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="80991-177">..23</span><span class="sxs-lookup"><span data-stu-id="80991-177">..23</span></span>|<span data-ttu-id="80991-178">Fra startdatoen til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="80991-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="80991-179">23..</span><span class="sxs-lookup"><span data-stu-id="80991-179">23..</span></span>|<span data-ttu-id="80991-180">Fra 23. i inneværende måned og inneværende år 00.00.00 til slutten av tid</span><span class="sxs-lookup"><span data-stu-id="80991-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="80991-181">22..23</span><span class="sxs-lookup"><span data-stu-id="80991-181">22..23</span></span>|<span data-ttu-id="80991-182">Fra 23. i inneværende måned og inneværende år 0.00.00 til 23. i inneværende måned og inneværende år 23.59.59</span><span class="sxs-lookup"><span data-stu-id="80991-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="80991-183">(&#124;) Enten/eller</span><span class="sxs-lookup"><span data-stu-id="80991-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="80991-184">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-184">Sample Expression</span></span>|<span data-ttu-id="80991-185">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="80991-186">1200&#124;1300</span></span>|<span data-ttu-id="80991-187">Tall med 1200 eller 1300</span><span class="sxs-lookup"><span data-stu-id="80991-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="80991-188">(<>) Ikke lik med</span><span class="sxs-lookup"><span data-stu-id="80991-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="80991-189">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-189">Sample Expression</span></span>|<span data-ttu-id="80991-190">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-191"><>0</span><span class="sxs-lookup"><span data-stu-id="80991-191"><>0</span></span>|<span data-ttu-id="80991-192">Alle tall unntatt 0</span><span class="sxs-lookup"><span data-stu-id="80991-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="80991-193">I SQL Server Option kan du kombinere dette symbolet med et jokertegnuttrykk.</span><span class="sxs-lookup"><span data-stu-id="80991-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="80991-194"><>A\* betyr for eksempel ikke lik noen tekst som begynner med A.</span><span class="sxs-lookup"><span data-stu-id="80991-194">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="80991-195">(>) Større enn</span><span class="sxs-lookup"><span data-stu-id="80991-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="80991-196">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-196">Sample Expression</span></span>|<span data-ttu-id="80991-197">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-198">>1200</span><span class="sxs-lookup"><span data-stu-id="80991-198">>1200</span></span>|<span data-ttu-id="80991-199">Tall som er større enn 1200</span><span class="sxs-lookup"><span data-stu-id="80991-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="80991-200">(>=) Større enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="80991-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="80991-201">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-201">Sample Expression</span></span>|<span data-ttu-id="80991-202">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="80991-203">>=1200</span></span>|<span data-ttu-id="80991-204">Tall som er større enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="80991-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="80991-205">(<) Mindre enn</span><span class="sxs-lookup"><span data-stu-id="80991-205">(<) Less than</span></span>  
  
|<span data-ttu-id="80991-206">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-206">Sample Expression</span></span>|<span data-ttu-id="80991-207">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-208"><1200</span><span class="sxs-lookup"><span data-stu-id="80991-208"><1200</span></span>|<span data-ttu-id="80991-209">Tall som er mindre enn 1200</span><span class="sxs-lookup"><span data-stu-id="80991-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="80991-210">(<=) Mindre enn eller lik med</span><span class="sxs-lookup"><span data-stu-id="80991-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="80991-211">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-211">Sample Expression</span></span>|<span data-ttu-id="80991-212">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="80991-213"><=1200</span></span>|<span data-ttu-id="80991-214">Tall som er mindre enn eller lik 1200</span><span class="sxs-lookup"><span data-stu-id="80991-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="80991-215">(&) Og</span><span class="sxs-lookup"><span data-stu-id="80991-215">(&) And</span></span>  
  
|<span data-ttu-id="80991-216">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-216">Sample Expression</span></span>|<span data-ttu-id="80991-217">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="80991-218">>200&<1200</span></span>|<span data-ttu-id="80991-219">Numre som er større enn 200, men mindre enn 1 200.</span><span class="sxs-lookup"><span data-stu-id="80991-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="80991-220">('') Finne et nøyaktig tegntreff</span><span class="sxs-lookup"><span data-stu-id="80991-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="80991-221">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-221">Sample Expression</span></span>|<span data-ttu-id="80991-222">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-223">'man'</span><span class="sxs-lookup"><span data-stu-id="80991-223">'man'</span></span>|<span data-ttu-id="80991-224">Tekst som samsvarer nøyaktig med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="80991-225">(@) Skiller ikke mellom små og store bokstaver</span><span class="sxs-lookup"><span data-stu-id="80991-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="80991-226">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-226">Sample Expression</span></span>|<span data-ttu-id="80991-227">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-228">@man\*</span><span class="sxs-lookup"><span data-stu-id="80991-228">@man\*</span></span>|<span data-ttu-id="80991-229">Tekst som begynner med man og skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="80991-230">(\*) Et ubegrenset antall ukjente tegn</span><span class="sxs-lookup"><span data-stu-id="80991-230">(\*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="80991-231">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-231">Sample Expression</span></span>|<span data-ttu-id="80991-232">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-233">*A/S*</span><span class="sxs-lookup"><span data-stu-id="80991-233">*Co*</span></span>|<span data-ttu-id="80991-234">Tekst som inneholder A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="80991-235">\*A/S</span><span class="sxs-lookup"><span data-stu-id="80991-235">\*Co</span></span>|<span data-ttu-id="80991-236">Tekst som slutter med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="80991-237">A/S\*</span><span class="sxs-lookup"><span data-stu-id="80991-237">Co\*</span></span>|<span data-ttu-id="80991-238">Tekst som begynner med A/S og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="80991-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="80991-239">(?) Ett ukjent tegn</span><span class="sxs-lookup"><span data-stu-id="80991-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="80991-240">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-240">Sample Expression</span></span>|<span data-ttu-id="80991-241">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-242">Hans?n</span><span class="sxs-lookup"><span data-stu-id="80991-242">Hans?n</span></span>|<span data-ttu-id="80991-243">Tekst som for eksempel Hansen eller Hanson</span><span class="sxs-lookup"><span data-stu-id="80991-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="80991-244">Kombinerte formatuttrykk</span><span class="sxs-lookup"><span data-stu-id="80991-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="80991-245">Eksempel</span><span class="sxs-lookup"><span data-stu-id="80991-245">Sample Expression</span></span>|<span data-ttu-id="80991-246">Viste poster</span><span class="sxs-lookup"><span data-stu-id="80991-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="80991-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="80991-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="80991-248">Nummer 5999 og numrene fra og med 8100 til og med 8490.</span><span class="sxs-lookup"><span data-stu-id="80991-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="80991-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="80991-249">..1299&#124;1400..</span></span>|<span data-ttu-id="80991-250">Ta med poster som har numre som er mindre enn eller lik 1299 eller nummeret 1400 eller høyere (alle numre utenom fra og med 1300 til og med 1399).</span><span class="sxs-lookup"><span data-stu-id="80991-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="80991-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="80991-251">>50&<100</span></span>|<span data-ttu-id="80991-252">Inkluder poster med numre som er større enn 50 og mindre enn 100 (det vil si tallene fra og med 51 til og med 99).</span><span class="sxs-lookup"><span data-stu-id="80991-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="80991-253">Se også</span><span class="sxs-lookup"><span data-stu-id="80991-253">See Also</span></span>
<span data-ttu-id="80991-254">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="80991-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

