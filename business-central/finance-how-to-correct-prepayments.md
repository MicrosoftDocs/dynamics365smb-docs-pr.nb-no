---
title: Slik korrigerer du forskudd | Microsoft-dokumentasjon
description: Du kan foreta en korrigering i en ordre etter at du har bokført en forskuddsfaktura for ordren. Du kan legge til nye linjer på en ordre etter at du har utstedt et forskudd, og deretter kan du bokføre en ny forskuddsfaktura, men du kan ikke slette en linje fra en ordre etter at et forskudd er fakturert for linjen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6888db488114c306276a95fcedb4a1722637f48d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387427"
---
# <a name="correct-prepayments"></a><span data-ttu-id="e2f81-104">Korrigere forskudd</span><span class="sxs-lookup"><span data-stu-id="e2f81-104">Correct Prepayments</span></span>

<span data-ttu-id="e2f81-105">Du kan foreta en korrigering i en ordre etter at du har bokført en forskuddsfaktura for ordren.</span><span class="sxs-lookup"><span data-stu-id="e2f81-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="e2f81-106">Du kan legge til nye linjer på en ordre etter at du har utstedt et forskudd, og deretter kan du bokføre en ny forskuddsfaktura, men du kan ikke slette en linje fra en ordre etter at et forskudd er fakturert for linjen.</span><span class="sxs-lookup"><span data-stu-id="e2f81-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

> [!TIP]
> <span data-ttu-id="e2f81-107">Hvis du har bokført en forskuddsfaktura for en salgsfaktura som du deretter retter opp eller kansellerer, må du også korrigere eller kansellere forskuddet.</span><span class="sxs-lookup"><span data-stu-id="e2f81-107">If you have posted a prepayment invoice for a sales invoice that you then correct or cancel, you must correct or cancel the prepayment as well.</span></span>

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="e2f81-108">Slik korrigerer du et forskudd</span><span class="sxs-lookup"><span data-stu-id="e2f81-108">To correct a prepayment</span></span>

<span data-ttu-id="e2f81-109">Følgende fremgangsmåte viser hvordan du utsteder en forskuddskreditnota som kansellerer alle fakturerte forskudd for en ordre.</span><span class="sxs-lookup"><span data-stu-id="e2f81-109">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  

1. <span data-ttu-id="e2f81-110">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e2f81-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e2f81-111">Åpne den aktuelle ordren.</span><span class="sxs-lookup"><span data-stu-id="e2f81-111">Open the relevant sales order.</span></span>
3. <span data-ttu-id="e2f81-112">Velg **Forskuddsbetaling**, og velg deretter **Bokfør kreditnota for forskudd** eller **Bokfør og skriv ut forskuddsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="e2f81-112">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="e2f81-113">På siden **Salgskreditnota** fortsette med å korrigere de aktuelle postene, for en salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="e2f81-113">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="e2f81-114">Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="e2f81-114">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>  

    > [!NOTE]  
    > <span data-ttu-id="e2f81-115">For å redusere beløpet i **Linjebeløp**-feltet må du først øke forskuddsprosenten på linjen slik at verdien i feltet **Linjebeløp for forskudd** ikke blir lavere enn verdien i feltet **Fakturert forskuddsbeløp**.</span><span class="sxs-lookup"><span data-stu-id="e2f81-115">To reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="e2f81-116">Når du skal opprette en forskuddsfaktura for nye linjer i en salgskreditnota, velger du **Forskuddsbetaling** og velger deretter **Bokfør forskuddsfaktura** eller **Bokfør og skriv ut forskuddsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="e2f81-116">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="e2f81-117">Du kan utstede en ny forskuddsfaktura ved å øke forskuddsbeløpet på én eller flere linjer og bokføre forskuddsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="e2f81-117">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="e2f81-118">Det opprettes en ny faktura for differansen mellom forskuddsbeløpene som er fakturert, og de nye forskuddsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="e2f81-118">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e2f81-119">Se også</span><span class="sxs-lookup"><span data-stu-id="e2f81-119">See Also</span></span>

[<span data-ttu-id="e2f81-120">Fakturere forskuddsbetalinger</span><span class="sxs-lookup"><span data-stu-id="e2f81-120">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="e2f81-121">Gjennomgang: konfigurere og fakturere salgsforskudd</span><span class="sxs-lookup"><span data-stu-id="e2f81-121">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="e2f81-122">Finans</span><span class="sxs-lookup"><span data-stu-id="e2f81-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e2f81-123">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e2f81-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]