---
title: Angi datointervaller i Finance and Operations, Business edition | Microsoft-dokumentasjon
description: "Finn ut hvordan du får en rapport til å vise data fra bestemte tidsperioder ved å bruke datointervaller i Finance and Operations, Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0494a04e67803049df71cfefe779c831c9f31674
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="d0100-103">Sette inn datointervaller</span><span class="sxs-lookup"><span data-stu-id="d0100-103">Entering Date Ranges</span></span> 
<span data-ttu-id="d0100-104">Du kan angi filtre som inneholder en startdato og en sluttdato, for å vise bare dataene innenfor dette datointervallet eller tidsintervallet.</span><span class="sxs-lookup"><span data-stu-id="d0100-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="d0100-105">Særlige regler gjelder for angivelse av datointervaller.</span><span class="sxs-lookup"><span data-stu-id="d0100-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="d0100-106">La oss ta **Kunde - ti på topp** som eksempel:</span><span class="sxs-lookup"><span data-stu-id="d0100-106">Let's take the **Customer Top 10** as an example:</span></span>

![Angi et datointervall på forespørselssiden for Kunde - ti på topp-listen](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="d0100-108">Her kan du begrense rapporten til et datointervall, for eksempel de to siste ukene eller totalt seks uker, eller et hvilket som helst intervall du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="d0100-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="d0100-109">Du angir datointervaller ved å angi datoene og deretter bruke **..**</span><span class="sxs-lookup"><span data-stu-id="d0100-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="d0100-110">eller **|** til å angi intervallet.</span><span class="sxs-lookup"><span data-stu-id="d0100-110">or **|** to set the range.</span></span> <span data-ttu-id="d0100-111">Hvis du vil vise de ti beste kundene for de to første ukene i mai i eksemplet vårt, setter du datofilteret til *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="d0100-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="d0100-112">Her er noen andre eksempler:</span><span class="sxs-lookup"><span data-stu-id="d0100-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="d0100-113">Betyr</span><span class="sxs-lookup"><span data-stu-id="d0100-113">Meaning</span></span> | <span data-ttu-id="d0100-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d0100-114">Example</span></span> | <span data-ttu-id="d0100-115">Tar med poster</span><span class="sxs-lookup"><span data-stu-id="d0100-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="d0100-116">Lik</span><span class="sxs-lookup"><span data-stu-id="d0100-116">Equal to</span></span>| <span data-ttu-id="d0100-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="d0100-117">12 15 16</span></span> |<span data-ttu-id="d0100-118">Bare de som er bokført 15. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="d0100-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="d0100-119">Intervall</span><span class="sxs-lookup"><span data-stu-id="d0100-119">Interval</span></span>| <span data-ttu-id="d0100-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="d0100-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="d0100-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="d0100-121">..12 15 16</span></span>|<span data-ttu-id="d0100-122">De som er bokført på datoer mellom og inkludert 15. desember 2016 og 15. januar 2017.</span><span class="sxs-lookup"><span data-stu-id="d0100-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="d0100-123">De som er bokført 15. desember 2016 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="d0100-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="d0100-124">Enten/eller</span><span class="sxs-lookup"><span data-stu-id="d0100-124">Either/or</span></span>|<span data-ttu-id="d0100-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="d0100-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="d0100-126">De som er bokført 15. eller 16. desember 2016.</span><span class="sxs-lookup"><span data-stu-id="d0100-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="d0100-127">Hvis det er bokført poster begge dagene, vises alle postene.</span><span class="sxs-lookup"><span data-stu-id="d0100-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="d0100-128">Grunnformene kan også kombineres innbyrdes.</span><span class="sxs-lookup"><span data-stu-id="d0100-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="d0100-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d0100-129">Example</span></span> | <span data-ttu-id="d0100-130">Tar med poster</span><span class="sxs-lookup"><span data-stu-id="d0100-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="d0100-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="d0100-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="d0100-132">Poster som enten er bokført 15. desember 2016 eller på datoer mellom og inkludert 1. desember 2016 og 31. mai 2017.</span><span class="sxs-lookup"><span data-stu-id="d0100-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="d0100-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="d0100-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="d0100-134">Poster som er bokført 14. desember eller tidligere, eller poster som er bokført 30. desember eller senere, det vil si alle poster unntatt de som er bokført på datoer mellom og inkludert 15. og 29. desember.</span><span class="sxs-lookup"><span data-stu-id="d0100-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="d0100-135">Vær oppmerksom på at vi har brukt det amerikanske datoformatet MMDDÅÅ her.</span><span class="sxs-lookup"><span data-stu-id="d0100-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="d0100-136">Etter hvert som [!INCLUDE[d365fin](includes/d365fin_md.md)] blir tilgjengelig på andre markeder, kan du bruke formatene du er vant med.</span><span class="sxs-lookup"><span data-stu-id="d0100-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0100-137">Se også</span><span class="sxs-lookup"><span data-stu-id="d0100-137">See Also</span></span>
<span data-ttu-id="d0100-138">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0100-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d0100-139">Angi vilkår i filtre</span><span class="sxs-lookup"><span data-stu-id="d0100-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="d0100-140">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d0100-140">General Business Functionality</span></span>](ui-across-business-areas.md)

