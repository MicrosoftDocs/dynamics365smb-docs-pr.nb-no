---
title: Annullere betalinger
description: Forbedringer i den norske versjonen gjør det mulig å annullere betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 557ba5f37e08122b261f0ee60a88993853d93e69
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "922306"
---
# <a name="cancel-payments"></a><span data-ttu-id="2db47-103">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="2db47-103">Cancel Payments</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="2db47-104">inneholder forbedringer i den norske versjonen, som gjør det mulig å annullere betalinger.</span><span class="sxs-lookup"><span data-stu-id="2db47-104">includes Norwegian enhancements that allow you to cancel payments.</span></span> <span data-ttu-id="2db47-105">Hvis betalingen er sendt til banken, må banken kontaktes, for å sørge for at remitteringen banken har mottatt, blir annullert.</span><span class="sxs-lookup"><span data-stu-id="2db47-105">If the payment has been sent to the bank, the bank must be contacted to cancel the remittance that they received.</span></span>  

- <span data-ttu-id="2db47-106">Et betalingsoppdrag kan annulleres hvis banken ikke mottar betalingen, og det må utføres en ny remittering.</span><span class="sxs-lookup"><span data-stu-id="2db47-106">A payment order can be canceled if the payments are not received by the bank and a new remittance must be made.</span></span> <span data-ttu-id="2db47-107">Du kan også annullere et oppdrag hvis du ikke vil overføre betalingene til banken, for eksempel hvis åpne oppdrag er feil.</span><span class="sxs-lookup"><span data-stu-id="2db47-107">You can also cancel a payment order if you do not want to transfer the payments to the bank, for example if the payments are incorrect.</span></span> <span data-ttu-id="2db47-108">Bare åpne betalingsoppdrag kan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="2db47-108">Only open payment orders can be canceled.</span></span>  

- <span data-ttu-id="2db47-109">En enkeltstående betaling kan annulleres hvis banken ikke kan behandle betalingen, og det må utføres en ny remittering.</span><span class="sxs-lookup"><span data-stu-id="2db47-109">An individual payment can be canceled if the payment cannot be processed by the bank and a new remittance has to be made.</span></span> <span data-ttu-id="2db47-110">Du kan også annullere en betaling hvis du ikke vil behandle betalingen.</span><span class="sxs-lookup"><span data-stu-id="2db47-110">You can also cancel a payment if you do not want to process the payment.</span></span> <span data-ttu-id="2db47-111">Oppgjorte betalinger kan ikke annulleres.</span><span class="sxs-lookup"><span data-stu-id="2db47-111">Settled payments cannot be canceled.</span></span>  

## <a name="to-cancel-a-payment-order"></a><span data-ttu-id="2db47-112">Slik annullerer du et oppdrag:</span><span class="sxs-lookup"><span data-stu-id="2db47-112">To cancel a payment order</span></span>  

1.  <span data-ttu-id="2db47-113">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Remitteringsoppdrag**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2db47-113">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Remittance Payment Order**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2db47-114">Velg oppdraget, velg **Eksportere**, og velg deretter handlingen **Annullere oppdrag**.</span><span class="sxs-lookup"><span data-stu-id="2db47-114">Select the payment order, choose the **Export** action, and then choose the **Cancel Payment Order** action.</span></span>  
3.  <span data-ttu-id="2db47-115">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="2db47-115">Choose the **Yes** button.</span></span>  

## <a name="to-cancel-a-payment"></a><span data-ttu-id="2db47-116">Slik annullerer du en betaling:</span><span class="sxs-lookup"><span data-stu-id="2db47-116">To cancel a payment</span></span>  

1.  <span data-ttu-id="2db47-117">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ventekladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2db47-117">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Waiting Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2db47-118">Velg betalingen, og velg deretter handlingen **Annullere betaling**.</span><span class="sxs-lookup"><span data-stu-id="2db47-118">Select the payment, and then choose the **Cancel Payment** action.</span></span>  
3.  <span data-ttu-id="2db47-119">Velg **Ja**-knappen.</span><span class="sxs-lookup"><span data-stu-id="2db47-119">Choose the **Yes** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2db47-120">Se også</span><span class="sxs-lookup"><span data-stu-id="2db47-120">See Also</span></span>  
 <span data-ttu-id="2db47-121">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-121">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="2db47-122">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-122">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="2db47-123">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-123">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="2db47-124">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-124">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="2db47-125">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-125">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="2db47-126">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-126">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="2db47-127">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-127">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="2db47-128">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-128">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="2db47-129">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-129">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="2db47-130">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-130">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="2db47-131">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-131">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="2db47-132">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-132">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="2db47-133">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-133">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="2db47-134">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="2db47-134">[Remittance Errors](remittance-errors.md) </span></span>  
 [<span data-ttu-id="2db47-135">Vise remitteringsfeilkoder</span><span class="sxs-lookup"><span data-stu-id="2db47-135">View Remittance Error Codes</span></span>](how-to-view-remittance-error-codes.md)
