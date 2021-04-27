---
title: Opprette og kjøre en kjørsel | Microsoft-dokumentasjon
description: Du kjører kjørsler for å behandle data og oppdatere informasjon, for eksempel for å gjøre periodiske regnskapsoppgaver eller beregninger.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782256"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="2228f-103">Kjøre satsvise jobber og XML-porter</span><span class="sxs-lookup"><span data-stu-id="2228f-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="2228f-104">Satsvise jobber er rutineoppgaver som behandler data bunkevis, for eksempel den satsvise jobben **Juster valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="2228f-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="2228f-105">Det finnes kjørsler som utfører periodiske regnskapsoppgaver, som for eksempel å avslutte resultatregnskapet på slutten av et regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="2228f-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="2228f-106">Mange kjørsler utfører beregninger, for eksempel beregning av renteinntekter/-utgifter, justering av valutakurser og utregning av salgspris.</span><span class="sxs-lookup"><span data-stu-id="2228f-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="2228f-107">En satsvis jobb ligner på en rapport, bortsett fra at den satsvise jobben bruker resultatet av det den gjør til å oppdatere informasjonen direkte, i stedet for å skrive ut resultatene.</span><span class="sxs-lookup"><span data-stu-id="2228f-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="2228f-108">Du kan planlegge når en kjørsel skal kjøres.</span><span class="sxs-lookup"><span data-stu-id="2228f-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="2228f-109">Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2228f-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="2228f-110">Slik kjører du en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="2228f-110">To run a batch job</span></span>
1. <span data-ttu-id="2228f-111">Hvis du vil åpne forespørselssiden for den relevante kjørselen, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir navnet på kjørselen, og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2228f-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="2228f-112">Hvis kjørselen har hurtigfanen **Alternativer**, fyller du ut feltene for å bestemme hva kjørselen skal gjøre.</span><span class="sxs-lookup"><span data-stu-id="2228f-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="2228f-113">Siden kan inneholde én eller flere hurtigfaner med filtre som du kan bruke til å begrense hvilke data som skal inkluderes i kjørselen.</span><span class="sxs-lookup"><span data-stu-id="2228f-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="2228f-114">Du kan legge inn kriterier i de foreslåtte filtrene eller legge til flere filtre.</span><span class="sxs-lookup"><span data-stu-id="2228f-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="2228f-115">Velg **OK** for å starte kjørselen.</span><span class="sxs-lookup"><span data-stu-id="2228f-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="2228f-116">Se også</span><span class="sxs-lookup"><span data-stu-id="2228f-116">See Also</span></span>
[<span data-ttu-id="2228f-117">Sortere, søke etter og filtrere oversikter</span><span class="sxs-lookup"><span data-stu-id="2228f-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="2228f-118">Bruke jobbkøer til å planlegge oppgaver</span><span class="sxs-lookup"><span data-stu-id="2228f-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="2228f-119">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2228f-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]