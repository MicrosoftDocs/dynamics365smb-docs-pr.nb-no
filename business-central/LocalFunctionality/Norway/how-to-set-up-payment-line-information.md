---
title: Definere betalingslinjeinformasjon
description: Utbetalingskladdelinjeinformasjon for remitteringsoppdraget angis på siden Betalingsinformasjon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e0858425d573170e473702668f6bee84e6a12fc2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781703"
---
# <a name="set-up-payment-line-information"></a><span data-ttu-id="c5933-103">Definere betalingslinjeinformasjon</span><span class="sxs-lookup"><span data-stu-id="c5933-103">Set Up Payment Line Information</span></span>
<span data-ttu-id="c5933-104">Utbetalingskladdelinjeinformasjon for remitteringsoppdraget angis på siden **Betalingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="c5933-104">Payment journal line information for the remittance payment is set up on the **Payment Info** page.</span></span>  

## <a name="to-set-up-payment-line-information"></a><span data-ttu-id="c5933-105">Definere betalingslinjeinformasjon</span><span class="sxs-lookup"><span data-stu-id="c5933-105">To set up payment line information</span></span>  

1.  <span data-ttu-id="c5933-106">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-106">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c5933-107">Velg handlingen **Betalingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="c5933-107">Choose the **Payment Info** action.</span></span>  
3.  <span data-ttu-id="c5933-108">Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Generelt** på siden **Betalingsinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="c5933-108">On the **Payment Info** page, on the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c5933-109">Felt</span><span class="sxs-lookup"><span data-stu-id="c5933-109">Field</span></span>|<span data-ttu-id="c5933-110">Description</span><span class="sxs-lookup"><span data-stu-id="c5933-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c5933-111">**Remitteringskontokode**</span><span class="sxs-lookup"><span data-stu-id="c5933-111">**Remittance Account Code**</span></span>|<span data-ttu-id="c5933-112">Velg remitteringskontokoden.</span><span class="sxs-lookup"><span data-stu-id="c5933-112">Select the remittance account code.</span></span>|  
    |<span data-ttu-id="c5933-113">**Remitteringsavtalekode**</span><span class="sxs-lookup"><span data-stu-id="c5933-113">**Remittance Agreement Code**</span></span>|<span data-ttu-id="c5933-114">Angi avtalekoden som er knyttet til kontokoden.</span><span class="sxs-lookup"><span data-stu-id="c5933-114">Specify the agreement code assigned to the account code.</span></span>|  
    |<span data-ttu-id="c5933-115">**Remitteringstype**</span><span class="sxs-lookup"><span data-stu-id="c5933-115">**Remittance Type**</span></span>|<span data-ttu-id="c5933-116">Angi remitteringstypen som er tilordnet til kontokoden.</span><span class="sxs-lookup"><span data-stu-id="c5933-116">Specify the remittance type assigned to the account code.</span></span> <span data-ttu-id="c5933-117">Remitteringstyper omfatter **Innland** og **Utland**.</span><span class="sxs-lookup"><span data-stu-id="c5933-117">Remittance types include **Domestic** and **Foreign**.</span></span>|  

4.  <span data-ttu-id="c5933-118">I hurtigfanen **Innland** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c5933-118">On the **Domestic** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c5933-119">Felt</span><span class="sxs-lookup"><span data-stu-id="c5933-119">Field</span></span>|<span data-ttu-id="c5933-120">Description</span><span class="sxs-lookup"><span data-stu-id="c5933-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c5933-121">**Mottakerref. 1 - 3**</span><span class="sxs-lookup"><span data-stu-id="c5933-121">**Recipient Ref. 1 – 3**</span></span>|<span data-ttu-id="c5933-122">Angi betalingsteksten som sendes til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c5933-122">Specify the payment text which is sent to the vendor.</span></span>|  
    |<span data-ttu-id="c5933-123">**KID (kundens ID-nummer)**</span><span class="sxs-lookup"><span data-stu-id="c5933-123">**KID (Cust. id number)**</span></span>|<span data-ttu-id="c5933-124">Angi nummeret som sendes til leverandøren når betalingen skal utføres.</span><span class="sxs-lookup"><span data-stu-id="c5933-124">Specify the number sent to the vendor during payment.</span></span>|  
    |<span data-ttu-id="c5933-125">**Vårt kontonr.**</span><span class="sxs-lookup"><span data-stu-id="c5933-125">**Our Account. No.**</span></span>|<span data-ttu-id="c5933-126">Angi kontonummeret til ditt firma.</span><span class="sxs-lookup"><span data-stu-id="c5933-126">Specify the account number for your company.</span></span>|  
    |<span data-ttu-id="c5933-127">**Eksterndokumentnr.**</span><span class="sxs-lookup"><span data-stu-id="c5933-127">**External Document No.**</span></span>|<span data-ttu-id="c5933-128">Angi nummeret på det eksterne dokumentet.</span><span class="sxs-lookup"><span data-stu-id="c5933-128">Specify the number of the external document.</span></span>|  
    |<span data-ttu-id="c5933-129">**Betalingsartkode innland**</span><span class="sxs-lookup"><span data-stu-id="c5933-129">**Payment Type Code Domestic**</span></span>|<span data-ttu-id="c5933-130">Angi betalingstypekoden som er tilordnet til betalingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-130">Specify the payment type code that is assigned to the payment.</span></span>|  

    > [!NOTE]  
    >  <span data-ttu-id="c5933-131">Mottakerreferansen og KID-nummeret kan ikke angis for den samme betalingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-131">The recipient reference and the KID number cannot be entered for the same payment.</span></span> <span data-ttu-id="c5933-132">Hvis KID benyttes, er dette den eneste informasjonen som leverandøren mottar.</span><span class="sxs-lookup"><span data-stu-id="c5933-132">If the KID is used, this is the only information that the vendor receives.</span></span>  

5.  <span data-ttu-id="c5933-133">I hurtigfanen **Utland** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c5933-133">On the **Foreign** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c5933-134">Felt</span><span class="sxs-lookup"><span data-stu-id="c5933-134">Field</span></span>|<span data-ttu-id="c5933-135">Description</span><span class="sxs-lookup"><span data-stu-id="c5933-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c5933-136">**Mottakerref. utland**</span><span class="sxs-lookup"><span data-stu-id="c5933-136">**Recipient Ref. Abroad**</span></span>|<span data-ttu-id="c5933-137">Angi betalingsteksten som sendes til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c5933-137">Specify the payment text that is sent to the vendor.</span></span>|  
    |<span data-ttu-id="c5933-138">**Betalingsartkode utland**</span><span class="sxs-lookup"><span data-stu-id="c5933-138">**Payment Type Code Abroad**</span></span>|<span data-ttu-id="c5933-139">Angi betalingstypekoden som er tilordnet til betalingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-139">Specify the payment type code that is assigned to the payment.</span></span>|  
    |<span data-ttu-id="c5933-140">**Sjekk**</span><span class="sxs-lookup"><span data-stu-id="c5933-140">**Check**</span></span>|<span data-ttu-id="c5933-141">Angi om det skal utstedes en sjekk.</span><span class="sxs-lookup"><span data-stu-id="c5933-141">Specify whether a check must be issued.</span></span><br /><br /> * <br />                        <span data-ttu-id="c5933-142">**Nei** - ingen sjekk utstedes.</span><span class="sxs-lookup"><span data-stu-id="c5933-142">**No** - No check is issued.</span></span><br /><br /> <span data-ttu-id="c5933-143">\* **Sendes oppdragsgiver** - sjekken utstedes og sendes til oppdragsgiver.</span><span class="sxs-lookup"><span data-stu-id="c5933-143">\* **Send to employer** - Check is issued and sent to the employer.</span></span><br /><br /> <span data-ttu-id="c5933-144">\* **Sendes betalingsmottaker** - sjekken utstedes og sendes til betalingsmottaker.</span><span class="sxs-lookup"><span data-stu-id="c5933-144">\* **Send to beneficiary** - Check is issued and sent to the beneficiary.</span></span>|  
    |<span data-ttu-id="c5933-145">**Haster**</span><span class="sxs-lookup"><span data-stu-id="c5933-145">**Urgent**</span></span>|<span data-ttu-id="c5933-146">Velg om betalingen haster og må behandles som en hasteoverføring.</span><span class="sxs-lookup"><span data-stu-id="c5933-146">Select if the payment is urgent and should be treated as an urgent transfer.</span></span>|  
    |<span data-ttu-id="c5933-147">**Avtalt kurs**</span><span class="sxs-lookup"><span data-stu-id="c5933-147">**Agreed Exch. Rate**</span></span>|<span data-ttu-id="c5933-148">Angi valutakursen som avtales med banken.</span><span class="sxs-lookup"><span data-stu-id="c5933-148">Specify the exchange rate which the bank agrees upon.</span></span>|  
    |<span data-ttu-id="c5933-149">**Avtalt med**</span><span class="sxs-lookup"><span data-stu-id="c5933-149">**Agreed With**</span></span>|<span data-ttu-id="c5933-150">Angi hvem avtalen er inngått med, hvis det er avtalt en valutakurs.</span><span class="sxs-lookup"><span data-stu-id="c5933-150">Specify who the agreement is entered with, if an exchange rate is agreed upon.</span></span>|  
    |<span data-ttu-id="c5933-151">**Terminskontraktnr.**</span><span class="sxs-lookup"><span data-stu-id="c5933-151">**Futures Contract No.**</span></span>|<span data-ttu-id="c5933-152">Angi terminskontraktnummeret som brukes for denne betalingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-152">Specify the future contract number that is used for this payment.</span></span>|  
    |<span data-ttu-id="c5933-153">**Terminskontraktkurs**</span><span class="sxs-lookup"><span data-stu-id="c5933-153">**Futures Contract Exch. Rate**</span></span>|<span data-ttu-id="c5933-154">Angi terminskontraktkursen som brukes for denne betalingen.</span><span class="sxs-lookup"><span data-stu-id="c5933-154">Specify the future contract exchange rate that is used for this payment.</span></span>|  

6.  <span data-ttu-id="c5933-155">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5933-155">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5933-156">Se også</span><span class="sxs-lookup"><span data-stu-id="c5933-156">See Also</span></span>  
 <span data-ttu-id="c5933-157">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-157">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="c5933-158">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-158">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="c5933-159">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-159">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="c5933-160">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-160">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="c5933-161">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-161">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="c5933-162">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-162">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="c5933-163">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-163">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="c5933-164">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-164">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="c5933-165">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-165">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="c5933-166">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-166">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="c5933-167">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-167">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="c5933-168">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-168">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="c5933-169">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-169">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="c5933-170">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="c5933-170">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="c5933-171">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="c5933-171">Cancel Payments</span></span>](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]