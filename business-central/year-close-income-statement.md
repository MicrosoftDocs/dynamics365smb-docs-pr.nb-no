---
title: Lukke resultatregnskapskonti | Microsoft-dokumentasjon
description: "Ved årsavslutning må du kjøre kjørselen Lukk resultatregnskapet for å lukke regnskapsperiodene som utgjør regnskapsåret."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3cea438b7d3dc1b14baaf76ae1b7ff97195f2191
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="close-income-statement-accounts"></a><span data-ttu-id="3f640-103">Lukke resultatregnskapskonti</span><span class="sxs-lookup"><span data-stu-id="3f640-103">Close Income Statement Accounts</span></span>
<span data-ttu-id="3f640-104">Når et regnskapsår er over, må du lukke periodene som utgjør regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="3f640-104">When a fiscal year is over, you must close the periods that comprise it.</span></span> <span data-ttu-id="3f640-105">Hvis du vil gjøre dette, kjører du den satsvise jobben **Lukk resultatregnskapet**.</span><span class="sxs-lookup"><span data-stu-id="3f640-105">To do this, you run the **Close Income Statement** batch job.</span></span> <span data-ttu-id="3f640-106">Denne jobben overfører årets resultat til en konto i balansen og lukke resultatregnskapskontoene.</span><span class="sxs-lookup"><span data-stu-id="3f640-106">This job transfers the year's result to an account in the balance sheet and closes the income statement accounts.</span></span> <span data-ttu-id="3f640-107">Dette gjør du ved å opprette linjer i en kladd som du deretter kan bokføre.</span><span class="sxs-lookup"><span data-stu-id="3f640-107">You do this by creating lines in a journal, which you then can post.</span></span>

## <a name="to-run-the-close-income-statement-batch-job"></a><span data-ttu-id="3f640-108">Kjøre den satsvise jobben Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="3f640-108">To run the Close Income Statement batch job</span></span>
1. <span data-ttu-id="3f640-109">Avslutte regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="3f640-109">Close the fiscal year.</span></span> <span data-ttu-id="3f640-110">Regnskapsåret må avsluttes før den satsvise jobben kan kjøres.</span><span class="sxs-lookup"><span data-stu-id="3f640-110">The fiscal year must closed before the batch job can be run.</span></span> <span data-ttu-id="3f640-111">Hvis du vil ha mer informasjon, kan du se [Avslutte regnskapsperioder](year-close-account-periods.md).</span><span class="sxs-lookup"><span data-stu-id="3f640-111">For more information, see [Close Accounting Periods](year-close-account-periods.md).</span></span>
2. <span data-ttu-id="3f640-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lukk resultatregnskapet**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="3f640-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Close Income Statement**, and then choose the related link.</span></span>
3. <span data-ttu-id="3f640-113">Velg **OK** for å kjøre kjørselen.</span><span class="sxs-lookup"><span data-stu-id="3f640-113">Choose the **OK** button to run the batch job.</span></span>

## <a name="about-the-close-income-statement-batch-job"></a><span data-ttu-id="3f640-114">Den satsvise jobben Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="3f640-114">About the Close Income Statement Batch Job</span></span>
<span data-ttu-id="3f640-115">Kjørselen behandler alle finanskonti av typen Resultatregnskap og oppretter poster som utsletter deres respektive saldoer.</span><span class="sxs-lookup"><span data-stu-id="3f640-115">The batch job processes all general accounts of the income statement type and creates entries that cancel out their respective balances.</span></span> <span data-ttu-id="3f640-116">Det vil si at hver post er summen av alle finansposter på kontoen i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="3f640-116">That is, each entry is the sum of all the general ledger entries on the account in the fiscal year.</span></span> <span data-ttu-id="3f640-117">Disse nye postene plasseres i en kladd der du må angi en motkonto, konto for fri egenkapital, i balansen før du bokfører.</span><span class="sxs-lookup"><span data-stu-id="3f640-117">These new entries are placed in a journal in which you must specify a balancing account and retained earnings account in the balance sheet before you post.</span></span> <span data-ttu-id="3f640-118">Når du bokfører kladden, bokføres en post på hver resultatkonto slik at saldoen blir null og samtidig overføres årsresultatet til balansen.</span><span class="sxs-lookup"><span data-stu-id="3f640-118">When you post the journal, an entry is posted to each income statement account so that its balance becomes zero and at the same time the year's result is transferred to the balance sheet.</span></span>

<span data-ttu-id="3f640-119">Du må bokføre kladden selv.</span><span class="sxs-lookup"><span data-stu-id="3f640-119">You must post the journal yourself.</span></span> <span data-ttu-id="3f640-120">Kjørselen bokfører ikke postene automatisk, med unntak av når en tilleggsrapporteringsvaluta brukes.</span><span class="sxs-lookup"><span data-stu-id="3f640-120">The batch job does not post the entries automatically, except when an additional reporting currency is being used.</span></span> <span data-ttu-id="3f640-121">Når en tilleggsrapporteringsvaluta brukes, bokfører den satsvise jobben poster direkte mot Finans.</span><span class="sxs-lookup"><span data-stu-id="3f640-121">When an additional reporting currency is being used, the batch job posts entries directly to the general ledger.</span></span>

<span data-ttu-id="3f640-122">Datoen på linjene som kjørselen setter inn i kladden, er alltid en sluttdato for regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="3f640-122">The date on the lines that the batch job inserts in the journal is always a closing date for the fiscal year.</span></span> <span data-ttu-id="3f640-123">Avslutningsdatoen er en fiktiv dato mellom siste dag i det gamle regnskapsåret og første dag i det nye.</span><span class="sxs-lookup"><span data-stu-id="3f640-123">The closing date is a fictitious date between the last day of the old fiscal year and the first day of the new year.</span></span> <span data-ttu-id="3f640-124">Fordelen med å bokføre på en avslutningsdato er at du ivaretar riktig saldo for de ordinære datoene i regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="3f640-124">The advantage of posting on a closing date is that you maintain the correct balances for the ordinary dates of the fiscal year.</span></span>

<span data-ttu-id="3f640-125">Den satsvise jobben **Lukk resultatregnskapet** kan brukes flere ganger.</span><span class="sxs-lookup"><span data-stu-id="3f640-125">The **Close Income Statement** batch job can be used several times.</span></span> <span data-ttu-id="3f640-126">Du kan bokføre i et tidligere år, selv etter at resultatkontiene er avsluttet, hvis du kjører kjørselen på nytt.</span><span class="sxs-lookup"><span data-stu-id="3f640-126">You can post in a previous fiscal year, even after the income statement accounts have been closed, if you run the batch job again.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f640-127">Se også</span><span class="sxs-lookup"><span data-stu-id="3f640-127">See Also</span></span>
[<span data-ttu-id="3f640-128">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="3f640-128">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="3f640-129">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="3f640-129">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="3f640-130">Åpne et nytt regnskapsår</span><span class="sxs-lookup"><span data-stu-id="3f640-130">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="3f640-131">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f640-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

