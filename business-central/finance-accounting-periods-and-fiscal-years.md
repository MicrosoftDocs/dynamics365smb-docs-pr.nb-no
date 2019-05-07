---
title: Arbeide med regnskapsperioder og regnskapsår | Microsoft-dokumentasjon
description: Lær hvordan du arbeider med regnskapsperioder for å definere når bedriften rapporterer økonomiske resultater.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 50df903e664f98f038a82c646dd3bd9c2f5ef479
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "936627"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a><span data-ttu-id="56867-103">Arbeide med regnskapsperioder og regnskapsår</span><span class="sxs-lookup"><span data-stu-id="56867-103">Working with Accounting Periods and Fiscal Years</span></span>
<span data-ttu-id="56867-104">Regnskapsperioder, som også kalles rapporteringsperioder, er tidsperioder som en bedrift eller organisasjon rapporterer økonomiske resultater for, for eksempel ved å generere resultatregnskapet eller balansen.</span><span class="sxs-lookup"><span data-stu-id="56867-104">Accounting periods, which are also known as reporting periods, are periods of time for which a company or organization reports financial performance, for example, by generating their income statement or balance sheet.</span></span> <span data-ttu-id="56867-105">Vanligvis viser regnskapsperioder til selskapets regnskapsår, som kan inneholde flere regnskapsperioder, for eksempel måneder eller kvartal.</span><span class="sxs-lookup"><span data-stu-id="56867-105">Typically, accounting periods refer to the company's fiscal year, which can contain several accounting periods, such as months or quarters.</span></span>

<span data-ttu-id="56867-106">I mange selskaper samsvarer ikke regnskapsåret med kalenderåret.</span><span class="sxs-lookup"><span data-stu-id="56867-106">For many companies the fiscal year does not align with the calendar year.</span></span> <span data-ttu-id="56867-107">Regnskapsåret kan for eksempel slutte 30. juni i stedet for 31. desember.</span><span class="sxs-lookup"><span data-stu-id="56867-107">For example, the fiscal year might end on June 30th rather than December 31st.</span></span> <span data-ttu-id="56867-108">For nyopprettede selskaper kan regnskapsåret faktisk være lenger enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="56867-108">For newly created companies, the fiscal might actually be longer than 12 months.</span></span> 

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="56867-109">krever bare regnskapsperioder hvis du vil lukke et resultatregnskap eller kjøre datakomprimeringsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="56867-109">only requires accounting periods only if you want to close an income statement, or run data compression tasks.</span></span> 

<span data-ttu-id="56867-110">Du kan bruke regnskapsperioder i rapportering.</span><span class="sxs-lookup"><span data-stu-id="56867-110">You can use accounting periods in reporting.</span></span> <span data-ttu-id="56867-111">For eksempel når du går gjennom bokførte poster på siden **Saldo/Budsjett** der rapporteringsintervallet kan angis.</span><span class="sxs-lookup"><span data-stu-id="56867-111">For example, when you are reviewing posted entries on the **Balance/Budget** page where the reporting interval can be specified.</span></span> <span data-ttu-id="56867-112">Ett av alternativene du kan angi er å rapportere etter regnskapsperiode.</span><span class="sxs-lookup"><span data-stu-id="56867-112">One of the options you may specify to report by accounting period.</span></span> <span data-ttu-id="56867-113">Du kan også lage et kontoskjema som sammenligner resultater for ulike regnskapsperioder.</span><span class="sxs-lookup"><span data-stu-id="56867-113">You can also build an account schedule that compares results for different accounting periods.</span></span>

## <a name="creating-a-new-fiscal-year"></a><span data-ttu-id="56867-114">Opprette et nytt regnskapsår</span><span class="sxs-lookup"><span data-stu-id="56867-114">Creating a new fiscal year</span></span>
<span data-ttu-id="56867-115">Du kan masseopprette regnskapsperioder ved å bruke **Opprett regnskapsår**-kjørselen eller manuelt.</span><span class="sxs-lookup"><span data-stu-id="56867-115">You can create accounting periods in bulk, by using eh **Create Fiscal Year** batch job, or manually.</span></span>

### <a name="how-to-create-accounting-periods-in-bulk"></a><span data-ttu-id="56867-116">Slik masseoppretter du regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="56867-116">How to create accounting periods in-bulk</span></span>
<span data-ttu-id="56867-117">Bruk **Opprett regnskapsår**-kjørselen til å dele et regnskapsår inn i like lange perioder.</span><span class="sxs-lookup"><span data-stu-id="56867-117">Use the **Create Fiscal Year** batch job to divide a fiscal year into periods of equal length.</span></span>  

1. <span data-ttu-id="56867-118">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="56867-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="56867-119">Velg handlingen **Opprett år**.</span><span class="sxs-lookup"><span data-stu-id="56867-119">Choose the **Create Year** action.</span></span>  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. <span data-ttu-id="56867-120">I **Startdato**-feltet angir du datoen som regnskapsåret starter på.</span><span class="sxs-lookup"><span data-stu-id="56867-120">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span>  
4. <span data-ttu-id="56867-121">I **Antall perioder**-feltet angir du antall regnskapsperioder som regnskapsåret skal deles inn i.</span><span class="sxs-lookup"><span data-stu-id="56867-121">In the **No. of Periods** field, enter the number of accounting periods to divide the fiscal year into.</span></span> <span data-ttu-id="56867-122">Det kan være opptil 365 perioder i et år.</span><span class="sxs-lookup"><span data-stu-id="56867-122">There can be up to 365 periods in a year.</span></span>  
5. <span data-ttu-id="56867-123">I feltet **Periodelengde** angir du en varighet for hver periode.</span><span class="sxs-lookup"><span data-stu-id="56867-123">In the **Period Length** field, enter a duration for each period.</span></span> <span data-ttu-id="56867-124">For eksempel 1M for én måned, 1K for ett kvartal og 1Å for ett år.</span><span class="sxs-lookup"><span data-stu-id="56867-124">For example, 1M for one month, 1Q for one quarter, and 1Y for one year.</span></span>  
6. <span data-ttu-id="56867-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="56867-125">Choose **OK**.</span></span>  

### <a name="how-to-create-accounting-periods-manually"></a><span data-ttu-id="56867-126">Slik oppretter du regnskapsperioder manuelt</span><span class="sxs-lookup"><span data-stu-id="56867-126">How to create accounting periods manually</span></span>
<span data-ttu-id="56867-127">Hvis regnskapsperiodene i regnskapsåret har forskjellig varighet, som 4-4-5-kalenderen i detaljhandel, kan du opprette det manuelt.</span><span class="sxs-lookup"><span data-stu-id="56867-127">If the accounting periods in your fiscal year have different durations, like the 4-4-5 calendar used in retail, you can manually set it up.</span></span>  
  
1. <span data-ttu-id="56867-128">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="56867-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="56867-129">I **Startdato**-feltet angir du datoen som regnskapsåret starter på.</span><span class="sxs-lookup"><span data-stu-id="56867-129">In the **Starting Date** field, enter the date on which the fiscal year starts.</span></span> <span data-ttu-id="56867-130">Feltet **Navn** vil vise navnet på måneden.</span><span class="sxs-lookup"><span data-stu-id="56867-130">The **Name** field will show the name of the month.</span></span>  
3. <span data-ttu-id="56867-131">Merk av for **Nytt regnskapsår** for å angi at dette er den første perioden i året.</span><span class="sxs-lookup"><span data-stu-id="56867-131">Choose the **New Fiscal Year** check box to indicate that this is the first period in the year.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="56867-132">bruker denne perioden for å finne ut hvilke perioder som skal lukkes ved årsslutt.</span><span class="sxs-lookup"><span data-stu-id="56867-132">will use this period to determine which periods to close at year-end.</span></span>
4. <span data-ttu-id="56867-133">Gjenta trinn 2 og 3 for hver gjenværende periode.</span><span class="sxs-lookup"><span data-stu-id="56867-133">Repeat steps 2 and 3 for each remaining period.</span></span>  

## <a name="closing-a-fiscal-year"></a><span data-ttu-id="56867-134">Lukke et regnskapsår</span><span class="sxs-lookup"><span data-stu-id="56867-134">Closing a Fiscal Year</span></span>
<span data-ttu-id="56867-135">Lukking av regnskapsåret er en av oppgavene for lukking av tablåene.</span><span class="sxs-lookup"><span data-stu-id="56867-135">Closing the fiscal year is one of the tasks for closing the books.</span></span> <span data-ttu-id="56867-136">Når du har lukket regnskapsåret, er det merket av for **Lukket** og **Dato låst** for alle periodene i året.</span><span class="sxs-lookup"><span data-stu-id="56867-136">After you close a fiscal year, the **Closed** and **Date Locked** check boxes are selected for all periods in the year.</span></span> <span data-ttu-id="56867-137">Du kan ikke åpne et år på nytt eller fjerne avmerkingene.</span><span class="sxs-lookup"><span data-stu-id="56867-137">You cannot reopen a year or clear the check boxes.</span></span>

> [!NOTE]  
>  <span data-ttu-id="56867-138">Du må alltid ha minst ett åpent regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="56867-138">You must always have at least one open fiscal year.</span></span> <span data-ttu-id="56867-139">Når du lukker et år, må du kontrollere at et nytt år er opprettet.</span><span class="sxs-lookup"><span data-stu-id="56867-139">When closing a year, ensure that a new year has been created.</span></span> <span data-ttu-id="56867-140">Legg også merke til at etter du lukker ett år, er det ikke mulig å endre startdatoen for det etterfølgende året.</span><span class="sxs-lookup"><span data-stu-id="56867-140">Also, note that after you close one year, you cannot change the starting date of the following year.</span></span>

1. <span data-ttu-id="56867-141">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Regnskapsperioder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="56867-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="56867-142">Velg handlingen **Lukk år**.</span><span class="sxs-lookup"><span data-stu-id="56867-142">Choose the **Close Year** action.</span></span>  

## <a name="posting-entries-to-a-closed-fiscal-year"></a><span data-ttu-id="56867-143">Bokføre poster i et lukket regnskapsår</span><span class="sxs-lookup"><span data-stu-id="56867-143">Posting Entries to a Closed Fiscal Year</span></span>
<span data-ttu-id="56867-144">Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det.</span><span class="sxs-lookup"><span data-stu-id="56867-144">Although a fiscal year is closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="56867-145">Når du gjør dette, blir postene merket som bokført i et avsluttet regnskapsår, og det merkes av for feltet **Etterpost**.</span><span class="sxs-lookup"><span data-stu-id="56867-145">When you do, the entries are marked as posted to a closed fiscal year and the **Prior Year Entry** check box is selected.</span></span> <span data-ttu-id="56867-146">Som standard vises ikke avmerkingsboksen på siden, men du kan legge den til.</span><span class="sxs-lookup"><span data-stu-id="56867-146">By default, the check box is not displayed on the page, but you can add it.</span></span> <span data-ttu-id="56867-147">Neste trinn er å lukke resultatregnskapskontoene og overføre årsresultatene til en konto i balansen.</span><span class="sxs-lookup"><span data-stu-id="56867-147">The next steps are to close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="56867-148">Gjenta disse trinnene hver gang du bokfører poster til et lukket regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="56867-148">Repeat these steps each time you post entries to a closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="56867-149">Se også</span><span class="sxs-lookup"><span data-stu-id="56867-149">See Also</span></span>
[<span data-ttu-id="56867-150">Lukke tablåene</span><span class="sxs-lookup"><span data-stu-id="56867-150">Closing the Books</span></span>](year-close-books.md)  
[<span data-ttu-id="56867-151">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="56867-151">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="56867-152">Arbeide med kontoskjemaer</span><span class="sxs-lookup"><span data-stu-id="56867-152">How to Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
  





