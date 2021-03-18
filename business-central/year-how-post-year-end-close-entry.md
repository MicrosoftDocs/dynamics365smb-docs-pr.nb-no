---
title: Bokføre avslutningsposten for årsslutt
description: Beskriver hvordan du åpner kladden du angav i kjørselen Lukk resultatregnskapet, og deretter ser gjennom og bokfører avslutningsposten for årsslutt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 02/23/2021
ms.author: edupont
ms.openlocfilehash: 728a3edc1ef2200d4f28130cad6653d6b26a5b3b
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493356"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="e029a-103">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="e029a-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="e029a-104">Når du har brukt den satsvise jobben **Lukk resultatregnskapet** til å generere avslutningsposten eller -postene for årsslutt, må du åpne kladden du angav i kjørselen, og deretter se gjennom og bokføre postene.</span><span class="sxs-lookup"><span data-stu-id="e029a-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="e029a-105">Avhengig av arbeidsprosessene i organisasjonen kan du velge å lukke eller ikke lukke regnskapsperioder og regnskapsår i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e029a-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="e029a-106">Den følgende fremgangsmåten forutsetter at du har lukket regnskapsåret med alternativet *Regnskapsperioder*, generert en avslutningspost ved årsslutt ved hjelp av kjørselen **Lukk resultatregnskap**, og nå er klar til å bokføre årsavslutningsposten sammen med motregningen av poster på egenkapitalkontoen.</span><span class="sxs-lookup"><span data-stu-id="e029a-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="e029a-107">Organisasjonen din kan velge å arbeide annerledes, for eksempel ved å bokføre avslutningsposten for årsslutt som en del av avslutningen av regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="e029a-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="e029a-108">Bokføre avslutningsposten for årsslutt</span><span class="sxs-lookup"><span data-stu-id="e029a-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="e029a-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e029a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e029a-110">I **Bunkenavn**-feltet, på siden **Finanskladd**, velger du bunken som inneholder avslutningspostene.</span><span class="sxs-lookup"><span data-stu-id="e029a-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="e029a-111">Se gjennom postene.</span><span class="sxs-lookup"><span data-stu-id="e029a-111">Review the entries.</span></span>
4. <span data-ttu-id="e029a-112">Velg handlingen **Bokfør** for å bokføre kladden.</span><span class="sxs-lookup"><span data-stu-id="e029a-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="e029a-113">Det vises en feilmelding hvis feil blir oppdaget.</span><span class="sxs-lookup"><span data-stu-id="e029a-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="e029a-114">Hvis bokføringen lykkes, fjernes de bokførte postene fra kladden.</span><span class="sxs-lookup"><span data-stu-id="e029a-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="e029a-115">Når bokføringen er fullført, posteres en oppføring på hver resultatregnskapskonto, slik at saldoen blir null og årsresultatet overføres til balansen.</span><span class="sxs-lookup"><span data-stu-id="e029a-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="e029a-116">Se også</span><span class="sxs-lookup"><span data-stu-id="e029a-116">See Also</span></span>

[<span data-ttu-id="e029a-117">Lukke regnskapsperioder</span><span class="sxs-lookup"><span data-stu-id="e029a-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="e029a-118">Avslutte tablåer</span><span class="sxs-lookup"><span data-stu-id="e029a-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="e029a-119">Lukk resultatregnskapet</span><span class="sxs-lookup"><span data-stu-id="e029a-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="e029a-120">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e029a-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]