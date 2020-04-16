---
title: Bruke kjørselen Betalingsforslag - leverandør | Microsoft-dokumentasjon
description: Du kan angi innstillinger for leverandørbetaling for å få forslag for betalinger som snart forfaller, eller der en rabatt er tilgjengelig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4f146894489cd1292558916068758e4b3c9c15fb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190254"
---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="f7741-103">Betalingsforslag - leverandør</span><span class="sxs-lookup"><span data-stu-id="f7741-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="f7741-104">På siden **Utbetalingskladd** kan du bruke kjørselen **Betalingsforslag – leverandør** til å foreslå betalingslinjer.</span><span class="sxs-lookup"><span data-stu-id="f7741-104">On the **Payment Journal** page, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="f7741-105">Linjer for betalinger som forfaller snart, eller betalinger der kontantrabatt er tilgjengelig, foreslås basert på innstillingene.</span><span class="sxs-lookup"><span data-stu-id="f7741-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="f7741-106">Hvis du vil dra nytte fullstendig av betalingsforslag, må du prioritere leverandørene først.</span><span class="sxs-lookup"><span data-stu-id="f7741-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="f7741-107">Hvis du vil ha mer informasjon, kan du se [Prioritere leverandører](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="f7741-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f7741-108">Leverandørposter som er merket med **Avvent** tas ikke med i kjørselen.</span><span class="sxs-lookup"><span data-stu-id="f7741-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="f7741-109">Hvis du vil dra nytte av kontantrabatter og har angitt et disponibelt beløp, brukes beløpet til følgende:</span><span class="sxs-lookup"><span data-stu-id="f7741-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="f7741-110">Prioriterte forfalte leverandørposter først i prioritetsrekkefølge.</span><span class="sxs-lookup"><span data-stu-id="f7741-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="f7741-111">Forfalte leverandørposter som ikke er prioritert.</span><span class="sxs-lookup"><span data-stu-id="f7741-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="f7741-112">Åpne leverandørposter som kvalifiserer for kontantrabatter, sortert etter leverandørnummer.</span><span class="sxs-lookup"><span data-stu-id="f7741-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="f7741-113">Bruke funksjonen Betalingsforslag - leverandør</span><span class="sxs-lookup"><span data-stu-id="f7741-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="f7741-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f7741-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f7741-115">Åpne den aktuelle kladden, og velg deretter handlingen **Betalingsforslag - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="f7741-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="f7741-116">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f7741-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="f7741-117">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7741-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="f7741-118">Sette inn forfallsdato som bokføringsdato på betalingskladdelinjer</span><span class="sxs-lookup"><span data-stu-id="f7741-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="f7741-119">Når du bruker kjørselen **Betalingsforslag - leverandør** til å opprette betalingslinjer for leverandørene, kan du fylle ut to spesialfelt for å sikre at de genererte linjene bruker forfallsdatoen til å beregne bokføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f7741-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="f7741-120">Disse feltene er **Beregn bokføringsdato fra forfallsdato for utligningsbilag** og **Forskyvning av forfallsdato for utligningsbilag**.</span><span class="sxs-lookup"><span data-stu-id="f7741-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="f7741-121">Du kan ikke bruke feltet **Beregn bokføringsdato fra forfallsdato for utligningsbilag** sammen med feltet **Søk etter kontantrabatter** eller feltet **Summer per leverandør**.</span><span class="sxs-lookup"><span data-stu-id="f7741-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="f7741-122">Hvis bokføringsdatoen er basert på forfallsdatoen, kan det hende at enkelte kontantrabatter ikke beregnes på riktig måte, fordi bokføringsdatoen er etter kontantrabattdatoen.</span><span class="sxs-lookup"><span data-stu-id="f7741-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="f7741-123">Hvis den beregnede bokføringsdatoen er passert, vil bokføringsdatoen også bli flyttet til arbeidsdatoen og det vil vises en advarsel.</span><span class="sxs-lookup"><span data-stu-id="f7741-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="f7741-124">Du kan også opprette betalingslinjer manuelt ved å bruke forfallsdatoen til å beregne bokføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="f7741-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="f7741-125">Når du bruker leverandørposter, kan du bruke den **Beregn bokføringsdato** til å oppdatere bokføringsdatoen på kladdelinjen med forfallsdatoen for den tilknyttede kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="f7741-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="f7741-126">Hvis du vil ha mer informasjon, kan du se [Utligne kjøpstransaksjoner manuelt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="f7741-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f7741-127">Hvis kjøpsfakturaen er forfalt, vil bokføringsdatoen bli satt til arbeidsdatoen, og skriftfargen på linjen blir rød.</span><span class="sxs-lookup"><span data-stu-id="f7741-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7741-128">Se også</span><span class="sxs-lookup"><span data-stu-id="f7741-128">See Also</span></span>
[<span data-ttu-id="f7741-129">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="f7741-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="f7741-130">Utføre betalinger</span><span class="sxs-lookup"><span data-stu-id="f7741-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="f7741-131">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="f7741-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="f7741-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7741-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
