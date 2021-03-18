---
title: Kontrollere remitteringsoppdrag
description: Etter at du har opprettet remitteringsoppdrag og generert forslag, kan du kontrollere at det ikke finnes feil i utbetalingskladdelinjene før du bokfører dem.
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
ms.openlocfilehash: 8f0b6aa1afaf2a67902f23111fbb9f165d935613
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383516"
---
# <a name="test-remittance-payments"></a><span data-ttu-id="d6a2c-103">Kontrollere remitteringsoppdrag</span><span class="sxs-lookup"><span data-stu-id="d6a2c-103">Test Remittance Payments</span></span>
<span data-ttu-id="d6a2c-104">Etter at du har opprettet remitteringsoppdrag og generert forslag, kan du kontrollere at det ikke finnes feil i utbetalingskladdelinjene før du bokfører dem.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-104">After you have set up remittance payments and generated suggestions, you can test the payment journal lines for errors before posting them.</span></span>  

<span data-ttu-id="d6a2c-105">Du kan bruke rapporten **Remitteringskontroll** til å kontrollere utbetalingskladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-105">To test the payment journal lines, you can use the **Remittance Test** report.</span></span> <span data-ttu-id="d6a2c-106">Denne rapporten skriver ut en oversikt over alle kladdelinjene sammen med eventuelle feil, for eksempel felt som ikke er fylt ut eller feil bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-106">This report prints an overview of all journal lines together with any errors, such as missing fields or incorrect bank accounts.</span></span>  

<span data-ttu-id="d6a2c-107">Hvis det skrives ut en advarsel i kontrollrapporten, kan du ikke overføre betalingene til banken før feilen er rettet opp.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-107">If a warning is printed in the test report, you cannot transfer the payments to the bank before the problem is corrected.</span></span> <span data-ttu-id="d6a2c-108">Du bør skrive ut kontrollrapporten for å sikre at alle betalingene utføres som forventet.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-108">You should print the test report to make sure that all payments are made as expected.</span></span>  

## <a name="to-print-a-remittance-test-report"></a><span data-ttu-id="d6a2c-109">Slik skriver du ut en remitteringskontrollrapport</span><span class="sxs-lookup"><span data-stu-id="d6a2c-109">To print a remittance test report</span></span>  

1.  <span data-ttu-id="d6a2c-110">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d6a2c-111">Velg handlingen **Kontrollrapport**.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-111">Choose the **Test Report** action.</span></span>  
3.  <span data-ttu-id="d6a2c-112">På hurtigfanen **Alternativer** velger du **Vis dimensjoner**-feltet for å skrive ut dimensjoner i kontrollrapporten.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-112">On the **Options** FastTab, select the **Show Dimensions** field to print dimensions on the test report.</span></span>  
4.  <span data-ttu-id="d6a2c-113">Velg **Skriv ut** for å skrive ut rapporten, eller velg **Forhåndsvisning** for å vise den på skjermen.</span><span class="sxs-lookup"><span data-stu-id="d6a2c-113">Choose the **Print** button to print the report or choose the **Preview** button to view it on the screen.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6a2c-114">Se også</span><span class="sxs-lookup"><span data-stu-id="d6a2c-114">See Also</span></span>  
 <span data-ttu-id="d6a2c-115">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-115">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="d6a2c-116">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-116">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="d6a2c-117">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-117">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="d6a2c-118">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-118">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="d6a2c-119">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-119">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="d6a2c-120">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-120">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="d6a2c-121">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-121">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="d6a2c-122">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-122">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="d6a2c-123">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-123">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="d6a2c-124">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-124">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="d6a2c-125">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-125">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="d6a2c-126">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-126">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="d6a2c-127">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-127">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="d6a2c-128">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="d6a2c-128">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="d6a2c-129">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="d6a2c-129">Cancel Payments</span></span>](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]