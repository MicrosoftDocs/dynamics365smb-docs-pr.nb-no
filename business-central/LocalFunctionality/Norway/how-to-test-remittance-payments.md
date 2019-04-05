---
title: Kontrollere remitteringsoppdrag
description: Etter at du har opprettet remitteringsoppdrag og generert forslag, kan du kontrollere at det ikke finnes feil i utbetalingskladdelinjene før du bokfører dem.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 86fe959c489535afe9c7e32c1b4ddf8b4f1c28b5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "826985"
---
# <a name="test-remittance-payments"></a><span data-ttu-id="09665-103">Kontrollere remitteringsoppdrag</span><span class="sxs-lookup"><span data-stu-id="09665-103">Test Remittance Payments</span></span>
<span data-ttu-id="09665-104">Etter at du har opprettet remitteringsoppdrag og generert forslag, kan du kontrollere at det ikke finnes feil i utbetalingskladdelinjene før du bokfører dem.</span><span class="sxs-lookup"><span data-stu-id="09665-104">After you have set up remittance payments and generated suggestions, you can test the payment journal lines for errors before posting them.</span></span>  

<span data-ttu-id="09665-105">Du kan bruke rapporten **Remitteringskontroll** til å kontrollere utbetalingskladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="09665-105">To test the payment journal lines, you can use the **Remittance Test** report.</span></span> <span data-ttu-id="09665-106">Denne rapporten skriver ut en oversikt over alle kladdelinjene sammen med eventuelle feil, for eksempel felt som ikke er fylt ut eller feil bankkonto.</span><span class="sxs-lookup"><span data-stu-id="09665-106">This report prints an overview of all journal lines together with any errors, such as missing fields or incorrect bank accounts.</span></span>  

<span data-ttu-id="09665-107">Hvis det skrives ut en advarsel i kontrollrapporten, kan du ikke overføre betalingene til banken før feilen er rettet opp.</span><span class="sxs-lookup"><span data-stu-id="09665-107">If a warning is printed in the test report, you cannot transfer the payments to the bank before the problem is corrected.</span></span> <span data-ttu-id="09665-108">Du bør skrive ut kontrollrapporten for å sikre at alle betalingene utføres som forventet.</span><span class="sxs-lookup"><span data-stu-id="09665-108">You should print the test report to make sure that all payments are made as expected.</span></span>  

## <a name="to-print-a-remittance-test-report"></a><span data-ttu-id="09665-109">Slik skriver du ut en remitteringskontrollrapport</span><span class="sxs-lookup"><span data-stu-id="09665-109">To print a remittance test report</span></span>  

1.  <span data-ttu-id="09665-110">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="09665-110">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="09665-111">Velg handlingen **Kontrollrapport**.</span><span class="sxs-lookup"><span data-stu-id="09665-111">Choose the **Test Report** action.</span></span>  
3.  <span data-ttu-id="09665-112">På hurtigfanen **Alternativer** velger du **Vis dimensjoner**-feltet for å skrive ut dimensjoner i kontrollrapporten.</span><span class="sxs-lookup"><span data-stu-id="09665-112">On the **Options** FastTab, select the **Show Dimensions** field to print dimensions on the test report.</span></span>  
4.  <span data-ttu-id="09665-113">Velg **Skriv ut** for å skrive ut rapporten, eller velg **Forhåndsvisning** for å vise den på skjermen.</span><span class="sxs-lookup"><span data-stu-id="09665-113">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09665-114">Se også</span><span class="sxs-lookup"><span data-stu-id="09665-114">See Also</span></span>  
 <span data-ttu-id="09665-115">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="09665-115">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="09665-116">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="09665-116">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="09665-117">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="09665-117">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="09665-118">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="09665-118">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="09665-119">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="09665-119">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="09665-120">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="09665-120">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="09665-121">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="09665-121">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="09665-122">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="09665-122">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="09665-123">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="09665-123">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="09665-124">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="09665-124">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="09665-125">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="09665-125">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="09665-126">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="09665-126">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="09665-127">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="09665-127">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="09665-128">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="09665-128">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="09665-129">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="09665-129">Cancel Payments</span></span>](how-to-cancel-payments.md)
