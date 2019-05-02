---
title: Opprette og kjøre en kjørsel | Microsoft-dokumentasjon
description: Du kjører kjørsler for å behandle data og oppdatere informasjon, for eksempel for å gjøre periodiske regnskapsoppgaver eller beregninger.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 260cd7761b130bbe3748de3cc109a9f4f56c1384
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "853261"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="31bbf-103">Kjøre kjørsler</span><span class="sxs-lookup"><span data-stu-id="31bbf-103">Run Batch Jobs</span></span>
<span data-ttu-id="31bbf-104">Satsvise jobber er rutineoppgaver som behandler data bunkevis, for eksempel den satsvise jobben **Juster valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="31bbf-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="31bbf-105">Det finnes kjørsler som utfører periodiske regnskapsoppgaver, som for eksempel å avslutte resultatregnskapet på slutten av et regnskapsår.</span><span class="sxs-lookup"><span data-stu-id="31bbf-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="31bbf-106">Mange kjørsler utfører beregninger, for eksempel beregning av renteinntekter/-utgifter, justering av valutakurser og utregning av salgspris.</span><span class="sxs-lookup"><span data-stu-id="31bbf-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="31bbf-107">En satsvis jobb ligner på en rapport, bortsett fra at den satsvise jobben bruker resultatet av det den gjør til å oppdatere informasjonen direkte, i stedet for å skrive ut resultatene.</span><span class="sxs-lookup"><span data-stu-id="31bbf-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="31bbf-108">Slik kjører du en satsvis jobb</span><span class="sxs-lookup"><span data-stu-id="31bbf-108">To run a batch job</span></span>
1. <span data-ttu-id="31bbf-109">Du kan åpne forespørselssiden for den relevante kjørselen ved å velge ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi navnet på kjørselen og deretter velge den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="31bbf-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="31bbf-110">Hvis kjørselen har hurtigfanen **Alternativer**, fyller du ut feltene for å bestemme hva kjørselen skal gjøre.</span><span class="sxs-lookup"><span data-stu-id="31bbf-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="31bbf-111">Siden kan inneholde én eller flere hurtigfaner med filtre som du kan bruke til å begrense hvilke data som skal inkluderes i kjørselen.</span><span class="sxs-lookup"><span data-stu-id="31bbf-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="31bbf-112">Du kan legge inn kriterier i de foreslåtte filtrene eller legge til flere filtre.</span><span class="sxs-lookup"><span data-stu-id="31bbf-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="31bbf-113">Velg **OK** for å starte kjørselen.</span><span class="sxs-lookup"><span data-stu-id="31bbf-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="31bbf-114">Se også</span><span class="sxs-lookup"><span data-stu-id="31bbf-114">See Also</span></span>
[<span data-ttu-id="31bbf-115">Sortere, søke etter og filtrere oversikter</span><span class="sxs-lookup"><span data-stu-id="31bbf-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="31bbf-116">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="31bbf-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>