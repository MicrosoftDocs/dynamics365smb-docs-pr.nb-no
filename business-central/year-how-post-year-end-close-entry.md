---
title: "Se gjennom og bokføre avslutningsposten for årsslutt | Microsoft-dokumentasjon"
description: "Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: cd555cc389ff7d9e306645475ef042f7ee9bc934
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="cb1d0-103">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="cb1d0-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="cb1d0-104">Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="cb1d0-105">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="cb1d0-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="cb1d0-106">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="cb1d0-107">I **Bunkenavn**-feltet, på siden **Finanskladd**, velger du bunken som inneholder avslutningspostene.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="cb1d0-108">Se gjennom postene.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-108">Review the entries.</span></span>
4. <span data-ttu-id="cb1d0-109">Velg handlingen **Bokfør** for å bokføre kladden.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="cb1d0-110">Det vises en feilmelding hvis feil blir oppdaget.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="cb1d0-111">Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="cb1d0-112">Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.</span><span class="sxs-lookup"><span data-stu-id="cb1d0-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb1d0-113">Se også</span><span class="sxs-lookup"><span data-stu-id="cb1d0-113">See Also</span></span>
[<span data-ttu-id="cb1d0-114">Lukke regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="cb1d0-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="cb1d0-115">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="cb1d0-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="cb1d0-116">Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="cb1d0-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="cb1d0-117">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb1d0-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

