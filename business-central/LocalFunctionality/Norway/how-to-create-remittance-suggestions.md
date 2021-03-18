---
title: Opprette remitteringsforslag
description: Du kan opprette et remitteringsforslag slik at betalingsforslag sendes til leverandører som skal motta remitteringsoppdrag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c51c1e8d6344994290020ce8fd97b38e11b9b1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383532"
---
# <a name="create-remittance-suggestions"></a><span data-ttu-id="0dd65-103">Opprette remitteringsforslag</span><span class="sxs-lookup"><span data-stu-id="0dd65-103">Create Remittance Suggestions</span></span>
<span data-ttu-id="0dd65-104">Du kan opprette et remitteringsforslag slik at betalingsforslag sendes til leverandører som skal motta remitteringsoppdrag.</span><span class="sxs-lookup"><span data-stu-id="0dd65-104">You can create a remittance suggestion so that payment proposals are sent to vendors who are set up to receive remittance payments.</span></span> <span data-ttu-id="0dd65-105">Én betalingstransaksjon per bokføringsdato overføres til banken for hver leverandør.</span><span class="sxs-lookup"><span data-stu-id="0dd65-105">One payment transaction per posting date for each vendor is transferred to the bank.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dd65-106">Du kan unngå å opprette betalingsforslag for leverandører som remitteres når den ordinære leverandørforslagprosessen benyttes, ved å legge til et filter for **Remittering** på siden **Betalingsforslag - leverandør** og sette filteret til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="0dd65-106">To avoid creating payment suggestions for vendors who are remitted when the usual vendor suggestion process is used, add a filter for **Remittance** on the **Suggest Vendor Payments** page and set the filter to **No**.</span></span>  

## <a name="to-create-a-remittance-suggestion"></a><span data-ttu-id="0dd65-107">Slik oppretter du et remitteringsforslag:</span><span class="sxs-lookup"><span data-stu-id="0dd65-107">To create a remittance suggestion</span></span>  

1.  <span data-ttu-id="0dd65-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0dd65-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0dd65-109">Velg handlingen **Remitteringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="0dd65-109">Choose the **Remittance Suggestion** action.</span></span>  
3.  <span data-ttu-id="0dd65-110">Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Alternativer** på siden **Remitteringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="0dd65-110">On the **Suggest Remittance Payments** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="0dd65-111">Felt</span><span class="sxs-lookup"><span data-stu-id="0dd65-111">Field</span></span>|<span data-ttu-id="0dd65-112">Description</span><span class="sxs-lookup"><span data-stu-id="0dd65-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="0dd65-113">**Siste betalingsdato**</span><span class="sxs-lookup"><span data-stu-id="0dd65-113">**Last Payment Date**</span></span>|<span data-ttu-id="0dd65-114">Angi den siste betalingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="0dd65-114">Specify the last payment date.</span></span>|  
    |<span data-ttu-id="0dd65-115">**Søk etter kontantrabatter**</span><span class="sxs-lookup"><span data-stu-id="0dd65-115">**Find Payment Discounts**</span></span>|<span data-ttu-id="0dd65-116">Velg dette alternativet hvis du vil søke etter poster med kontantrabatter.</span><span class="sxs-lookup"><span data-stu-id="0dd65-116">Select if you want to search for entries where a payment discount is available.</span></span>|  
    |<span data-ttu-id="0dd65-117">**Bruk leverandørprioritet**</span><span class="sxs-lookup"><span data-stu-id="0dd65-117">**Use Vendor Priority**</span></span>|<span data-ttu-id="0dd65-118">Velg dette alternativet hvis leverandørprioritet skal brukes til å søke i poster.</span><span class="sxs-lookup"><span data-stu-id="0dd65-118">Select if the vendor priority should be used to search entries.</span></span>|  
    |<span data-ttu-id="0dd65-119">**Disponibelt beløp (NOK)**</span><span class="sxs-lookup"><span data-stu-id="0dd65-119">**Available Amount (LCY)**</span></span>|<span data-ttu-id="0dd65-120">Angi betalingene for totalsummer som er mindre enn eller lik det angitte beløpet.</span><span class="sxs-lookup"><span data-stu-id="0dd65-120">Specify the payments for total amounts that are less than or equal to the given amount.</span></span>|  
    |<span data-ttu-id="0dd65-121">**Bokføringsdato**</span><span class="sxs-lookup"><span data-stu-id="0dd65-121">**Posting Date**</span></span>|<span data-ttu-id="0dd65-122">Angi en bokføringsdato.</span><span class="sxs-lookup"><span data-stu-id="0dd65-122">Specify a posting date.</span></span>|  
    |<span data-ttu-id="0dd65-123">**Erstatt bokføringsdato med forfallsdato**</span><span class="sxs-lookup"><span data-stu-id="0dd65-123">**Replace Posting Date with Due Date**</span></span>|<span data-ttu-id="0dd65-124">Velg for å sette inn forfallsdatoen for posten som bokføringsdato for betalingene.</span><span class="sxs-lookup"><span data-stu-id="0dd65-124">Select to insert the due date of the entry as the posting date for the payments.</span></span>|  
    |<span data-ttu-id="0dd65-125">**Sjekk bilagstype**</span><span class="sxs-lookup"><span data-stu-id="0dd65-125">**Test Document Type**</span></span>|<span data-ttu-id="0dd65-126">Angi hvilke av følgende bilagstyper som skal sjekkes for betaling:</span><span class="sxs-lookup"><span data-stu-id="0dd65-126">Specify which of the following document types should be tested for payment:</span></span><br /><br /> <span data-ttu-id="0dd65-127">-   **Alle** - alle bilagstyper sjekkes.</span><span class="sxs-lookup"><span data-stu-id="0dd65-127">-   **All** - All document types are tested.</span></span><br /><span data-ttu-id="0dd65-128">-   **Faktura/kreditnota** - Bare faktura- eller kreditnotaposter sjekkes.</span><span class="sxs-lookup"><span data-stu-id="0dd65-128">-   **Invoice/Credit memo** - Only invoice or credit memo entries are tested.</span></span>|  
    |<span data-ttu-id="0dd65-129">**Bare faktura-/debetposter**</span><span class="sxs-lookup"><span data-stu-id="0dd65-129">**Invoice/Debit Vendor Ledger Entries only**</span></span>|<span data-ttu-id="0dd65-130">Velg dette for å bare betale faktura- eller debetposter.</span><span class="sxs-lookup"><span data-stu-id="0dd65-130">Select to pay only invoice or debit entries.</span></span>|  

4.  <span data-ttu-id="0dd65-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0dd65-131">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0dd65-132">Se også</span><span class="sxs-lookup"><span data-stu-id="0dd65-132">See Also</span></span>  
 <span data-ttu-id="0dd65-133">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-133">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="0dd65-134">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-134">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="0dd65-135">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-135">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="0dd65-136">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-136">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="0dd65-137">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-137">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="0dd65-138">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-138">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="0dd65-139">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-139">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="0dd65-140">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-140">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="0dd65-141">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-141">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="0dd65-142">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-142">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="0dd65-143">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-143">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="0dd65-144">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-144">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="0dd65-145">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-145">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="0dd65-146">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="0dd65-146">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="0dd65-147">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="0dd65-147">Cancel Payments</span></span>](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]