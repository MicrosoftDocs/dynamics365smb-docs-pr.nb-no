---
title: Se gjennom og bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon
description: Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ca92d9535a9a15d46d93de6febdfd169c3d7d17a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755545"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="71bb4-103">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="71bb4-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="71bb4-104">Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.</span><span class="sxs-lookup"><span data-stu-id="71bb4-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="71bb4-105">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="71bb4-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="71bb4-106">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="71bb4-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="71bb4-107">I **Bunkenavn**-feltet, på siden **Finanskladd**, velger du bunken som inneholder avslutningspostene.</span><span class="sxs-lookup"><span data-stu-id="71bb4-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="71bb4-108">Se gjennom postene.</span><span class="sxs-lookup"><span data-stu-id="71bb4-108">Review the entries.</span></span>
4. <span data-ttu-id="71bb4-109">Velg handlingen **Bokfør** for å bokføre kladden.</span><span class="sxs-lookup"><span data-stu-id="71bb4-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="71bb4-110">Det vises en feilmelding hvis feil blir oppdaget.</span><span class="sxs-lookup"><span data-stu-id="71bb4-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="71bb4-111">Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden.</span><span class="sxs-lookup"><span data-stu-id="71bb4-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="71bb4-112">Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.</span><span class="sxs-lookup"><span data-stu-id="71bb4-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="71bb4-113">Se også</span><span class="sxs-lookup"><span data-stu-id="71bb4-113">See Also</span></span>
[<span data-ttu-id="71bb4-114">Lukke regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="71bb4-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="71bb4-115">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="71bb4-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="71bb4-116">Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="71bb4-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="71bb4-117">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71bb4-117">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
