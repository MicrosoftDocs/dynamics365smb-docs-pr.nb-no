---
title: Typer betalingsreturfiler
description: 'Forbedringer i den norske versjonen omfatter to typer importerbare betalingsreturfiler:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 55b2a6672e1c447655d19a49b071b4a9dc23cbaf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921326"
---
# <a name="types-of-payment-returns-files"></a><span data-ttu-id="0af4e-103">Typer betalingsreturfiler</span><span class="sxs-lookup"><span data-stu-id="0af4e-103">Types of Payment Returns Files</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="0af4e-104">omfatter to typer importerbare betalingsreturfiler:</span><span class="sxs-lookup"><span data-stu-id="0af4e-104">includes two types of payment return files that can be imported:</span></span>  

- <span data-ttu-id="0af4e-105">Mottaksreturer</span><span class="sxs-lookup"><span data-stu-id="0af4e-105">Receipt returns</span></span>  
- <span data-ttu-id="0af4e-106">Avregningsreturer</span><span class="sxs-lookup"><span data-stu-id="0af4e-106">Settlement returns</span></span>  

<span data-ttu-id="0af4e-107">Du kan også velge å ikke bruke returfiler ved å velge feltet **Returfiler brukes ikke** i **remitteringsavtalen**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0af4e-107">You can also choose to not use return files by selecting the **Return File Is Not In Use** field in the **Remittance Agreement** table.</span></span> <span data-ttu-id="0af4e-108">Se [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="0af4e-108">For more information, see [Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md).</span></span>  

## <a name="receipt-returns"></a><span data-ttu-id="0af4e-109">Mottaksreturer</span><span class="sxs-lookup"><span data-stu-id="0af4e-109">Receipt Returns</span></span>  
<span data-ttu-id="0af4e-110">Mottaksreturen mottas fra banken etter at du har sendt remitteringsfilen til banken.</span><span class="sxs-lookup"><span data-stu-id="0af4e-110">The receipt return is received from the bank after you have sent the remittance file to the bank.</span></span> <span data-ttu-id="0af4e-111">Når data leses inn, vises informasjon om hvor mange fakturaer som blir korrekt mottatt og hvor mange som mottas med feilmelding.</span><span class="sxs-lookup"><span data-stu-id="0af4e-111">When data is imported, information about the number of invoices that are received correctly and the number that are received with error is displayed.</span></span> <span data-ttu-id="0af4e-112">Når du har importert en mottaksretur, blir statusen for betalingene i vinduet **Ventekladd** satt til **Godkjent**.</span><span class="sxs-lookup"><span data-stu-id="0af4e-112">After you import a receipt return, the status of the payments in the **Waiting Journal** table is set to **Approved**.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0af4e-113">Du kan også motta en avvist retur fra banken.</span><span class="sxs-lookup"><span data-stu-id="0af4e-113">You may also receive a rejected return from the bank.</span></span> <span data-ttu-id="0af4e-114">Hvis remitteringen avvises, mottar du ingen avregningsretur.</span><span class="sxs-lookup"><span data-stu-id="0af4e-114">If the remittance is rejected, the settlement return will not be received.</span></span>  

## <a name="settlement-returns"></a><span data-ttu-id="0af4e-115">Avregningsreturer</span><span class="sxs-lookup"><span data-stu-id="0af4e-115">Settlement Returns</span></span>  
<span data-ttu-id="0af4e-116">Avregningsreturen mottas fra banken etter at betalingen er utført.</span><span class="sxs-lookup"><span data-stu-id="0af4e-116">The settlement return is received from the bank after the payment is executed.</span></span> <span data-ttu-id="0af4e-117">Når dataene leses inn, vises informasjon om antall oppgjorte fakturaer.</span><span class="sxs-lookup"><span data-stu-id="0af4e-117">When data is imported, information about the number of settled invoices is displayed.</span></span>  

<span data-ttu-id="0af4e-118">Følgende skjer når avregningsreturen leses inn:</span><span class="sxs-lookup"><span data-stu-id="0af4e-118">The following occurs when the settlement return is imported:</span></span>  

- <span data-ttu-id="0af4e-119">Betalingsstatusen i tabellen **Ventekladd** settes til **Avregnet**.</span><span class="sxs-lookup"><span data-stu-id="0af4e-119">Payment status in the **Waiting Journal** table is set to **Settled**.</span></span>  
- <span data-ttu-id="0af4e-120">Da overføres informasjon fra siden **Ventekladd** til utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="0af4e-120">Information will be transferred from the **Waiting Journal** page to the payment journal.</span></span>  
- <span data-ttu-id="0af4e-121">Det opprettes en motkonto for hver transaksjon.</span><span class="sxs-lookup"><span data-stu-id="0af4e-121">A balancing account will be created for each transaction.</span></span>  
- <span data-ttu-id="0af4e-122">Det settes inn bilagsnumre for hver transaksjon.</span><span class="sxs-lookup"><span data-stu-id="0af4e-122">Document numbers will be inserted for each transaction.</span></span>  

## <a name="exchange-rates-by-settlement"></a><span data-ttu-id="0af4e-123">Valutakurser ved oppgjør</span><span class="sxs-lookup"><span data-stu-id="0af4e-123">Exchange Rates by Settlement</span></span>  
<span data-ttu-id="0af4e-124">Ved oppgjør håndteres valutakurser på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="0af4e-124">For a payment, the exchange rates are managed in the following ways:</span></span>  

- <span data-ttu-id="0af4e-125">Betaling fra en konto i lokal valuta - Hvis en betaling i en annen valuta utføres fra en konto i NOK, flagger banken avregningsreturen med en advarsel om hvilken vekslingskurs som benyttes mellom NOK og valutaen som benyttes for betalingen.</span><span class="sxs-lookup"><span data-stu-id="0af4e-125">Payment from an account in local currency - If a payment in another currency is from an account in LCY, the bank will flag the settlement return with a warning about the exchange rate between LCY and the currency that is used as payment.</span></span>  

- <span data-ttu-id="0af4e-126">Betaling fra en valutakonto - Hvis betalingen utføres fra en valutakonto, benyttes vekslingskursen for denne valutaen og NOK.</span><span class="sxs-lookup"><span data-stu-id="0af4e-126">Payment from a currency account - If payment is made from a currency account, the exchange rate for this currency and LCY is used.</span></span> <span data-ttu-id="0af4e-127">Dette fordi banken ikke informerer systemet om valutakursen.</span><span class="sxs-lookup"><span data-stu-id="0af4e-127">This is because the bank does not inform the system about the exchange rate.</span></span>  

## <a name="warnings-on-settlement-returns"></a><span data-ttu-id="0af4e-128">Advarsler i avregningsreturer</span><span class="sxs-lookup"><span data-stu-id="0af4e-128">Warnings on Settlement Returns</span></span>  
<span data-ttu-id="0af4e-129">Det kan forekomme advarsler når avregningsreturen leses inn.</span><span class="sxs-lookup"><span data-stu-id="0af4e-129">When the settlement return is imported, warnings can occur.</span></span> <span data-ttu-id="0af4e-130">Innbetalingskladdelinjer med advarsler er merket med et symbol.</span><span class="sxs-lookup"><span data-stu-id="0af4e-130">Payment journal lines with warnings are marked with a symbol.</span></span> <span data-ttu-id="0af4e-131">Hvis du vil vite mer om advarselen, kan du åpne siden **Avregningsopplysninger**.</span><span class="sxs-lookup"><span data-stu-id="0af4e-131">To view the information about the warning, you can open the **Settlement Info** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0af4e-132">Se også</span><span class="sxs-lookup"><span data-stu-id="0af4e-132">See Also</span></span>  
 <span data-ttu-id="0af4e-133">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-133">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="0af4e-134">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-134">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="0af4e-135">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-135">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="0af4e-136">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-136">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="0af4e-137">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-137">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="0af4e-138">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-138">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="0af4e-139">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-139">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="0af4e-140">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-140">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="0af4e-141">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-141">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="0af4e-142">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-142">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="0af4e-143">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-143">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="0af4e-144">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-144">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="0af4e-145">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-145">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="0af4e-146">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="0af4e-146">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="0af4e-147">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="0af4e-147">Cancel Payments</span></span>](how-to-cancel-payments.md)
