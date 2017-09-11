---
title: "Definere søkekriterier i filtre | Microsoft-dokumentasjon"
description: "Beskriver hvordan du arbeider med filtre, for eksempel hurtigfilter, for å begrense resultatene du får når du søker etter data."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="f8c3c-103">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="f8c3c-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="f8c3c-104">Når du vil søke etter data, for eksempel kundenavn, adresser eller produktgrupper, må du angi kriterier.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="f8c3c-105">I søkekriteriene kan du bruke alle tallene og bokstavene du vanligvis kan bruke i det spesifikke feltet.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="f8c3c-106">I tillegg til dette kan du bruke spesielle symboler til å filtrere resultatene ytterligere.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="f8c3c-107">Søke ved hjelp av hurtigfilteret</span><span class="sxs-lookup"><span data-stu-id="f8c3c-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="f8c3c-108">Du kan legge til filtre på alle sider ved hjelp av hurtigfilteret.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="f8c3c-109">Hurtigfilteret aktiveres ved å velge forstørrelsesikonet i øvre høyre hjørne på siden.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="f8c3c-110">Denne filtreringstypen brukes for rask angivelse av kriterier.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="f8c3c-111">Hurtigfilteret gjør det enkelt å filtrere data ved å skrive inn ren tekst, men gir også mange alternativer når det gjelder søkekriterier.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="f8c3c-112">Virkemåten for hurtigfilteret er avhengig av om du skriver inn ren tekst eller tekst som inneholder symboler.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="f8c3c-113">Hvis du skriver inn ren tekst i søkevilkåret, tolkes søkekriteriene som et søk som ikke skiller mellom store og små bokstaver og som inneholder en bestemt tekst.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="f8c3c-114">Hvis du skriver inn tekst med symboler i søkekriteriene, tolkes søkekriteriene nøyaktig slik du skrev det inn, og søket skiller mellom store og små bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="f8c3c-115">Kriterier for hurtigfilter</span><span class="sxs-lookup"><span data-stu-id="f8c3c-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="f8c3c-116">Søkekriterier</span><span class="sxs-lookup"><span data-stu-id="f8c3c-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="f8c3c-117">Tolkes som ...</span><span class="sxs-lookup"><span data-stu-id="f8c3c-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="f8c3c-118">Returnerer ...</span><span class="sxs-lookup"><span data-stu-id="f8c3c-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="f8c3c-119">man</span><span class="sxs-lookup"><span data-stu-id="f8c3c-119">man</span></span></TD>
    <TD><span data-ttu-id="f8c3c-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="f8c3c-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="f8c3c-121">Alle poster som inneholder teksten <b>mann</b> og som ikke skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="f8c3c-122">se</span><span class="sxs-lookup"><span data-stu-id="f8c3c-122">se</span></span></TD>
    <TD><span data-ttu-id="f8c3c-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="f8c3c-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="f8c3c-124">Alle poster som inneholder teksten <b>se</b> og som ikke skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="f8c3c-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="f8c3c-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="f8c3c-126">Begynner med <b>Man</b>, og skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="f8c3c-127">Alle poster som starter med teksten <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="f8c3c-128">'man'</span><span class="sxs-lookup"><span data-stu-id="f8c3c-128">'man'</span></span></TD>
    <TD><span data-ttu-id="f8c3c-129">En nøyaktig tekst som skiller mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="f8c3c-130">Alle poster som samsvarer nøyaktig med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="f8c3c-131">@man*</span><span class="sxs-lookup"><span data-stu-id="f8c3c-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="f8c3c-132">Begynner med, og skiller ikke mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="f8c3c-133">Alle poster som starter med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="f8c3c-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="f8c3c-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="f8c3c-135">Slutter med, og skiller ikke mellom små og store bokstaver.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="f8c3c-136">Alle poster som slutter med <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="f8c3c-137">Du kan ikke bruke et jokertegn når du filtrerer på felt for opplisting, for eksempel feltet **Status** i ordrer.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="f8c3c-138">Hvis du vil angi et filter for denne typen felt, kan du angi den numeriske verdien som en parameter for filtrering.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="f8c3c-139">I feltet **Status** på en ordre som har verdiene **Åpen**, **Frigitt**, **Venter på godkjenning** og **Venter på forskudd**, må du bruke verdiene **0**, **1**, **2** og **3** for å filtrere etter disse alternativene.</span><span class="sxs-lookup"><span data-stu-id="f8c3c-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8c3c-140">Se også</span><span class="sxs-lookup"><span data-stu-id="f8c3c-140">See Also</span></span>
<span data-ttu-id="f8c3c-141">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8c3c-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

