---
title: "Se gjennom og bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon"
description: "Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 78039e9387866ce17ff3be5a2ff509545e8439d2
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="410a2-103">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="410a2-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="410a2-104">Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.</span><span class="sxs-lookup"><span data-stu-id="410a2-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="410a2-105">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="410a2-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="410a2-106">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="410a2-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="410a2-107">I **Bunkenavn**-feltet i vinduet **Finanskladd**, velger du bunken som inneholder avslutningspostene.</span><span class="sxs-lookup"><span data-stu-id="410a2-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="410a2-108">Se gjennom postene.</span><span class="sxs-lookup"><span data-stu-id="410a2-108">Review the entries.</span></span>
4. <span data-ttu-id="410a2-109">Velg handlingen **Bokfør** for å bokføre kladden.</span><span class="sxs-lookup"><span data-stu-id="410a2-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="410a2-110">Det vises en feilmelding hvis feil blir oppdaget.</span><span class="sxs-lookup"><span data-stu-id="410a2-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="410a2-111">Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden.</span><span class="sxs-lookup"><span data-stu-id="410a2-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="410a2-112">Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.</span><span class="sxs-lookup"><span data-stu-id="410a2-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="410a2-113">Se også</span><span class="sxs-lookup"><span data-stu-id="410a2-113">See Also</span></span>
[<span data-ttu-id="410a2-114">Lukke regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="410a2-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="410a2-115">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="410a2-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="410a2-116">Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="410a2-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="410a2-117">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="410a2-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

