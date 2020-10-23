---
title: Remitteringsfeil
description: Remitteringsfeil for betalinger kan oppstå ved overføring av data og etter at betalingene er sendt til banken. Begge typer feil rapporteres på siden Returfeil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 852cf8618f0ab396a208b126cdb0c2511be3ae05
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921332"
---
# <a name="remittance-errors"></a><span data-ttu-id="ed45b-104">Remitteringsfeil</span><span class="sxs-lookup"><span data-stu-id="ed45b-104">Remittance Errors</span></span>
<span data-ttu-id="ed45b-105">Remitteringsfeil for betalinger kan oppstå ved overføring av data og etter at betalingene er sendt til banken.</span><span class="sxs-lookup"><span data-stu-id="ed45b-105">Remittance errors for payments may occur when data is transferred and after payments have been sent to the bank.</span></span> <span data-ttu-id="ed45b-106">Begge typer feil rapporteres på siden **Returfeil**.</span><span class="sxs-lookup"><span data-stu-id="ed45b-106">Both kinds of errors are reported on the **Return Error** page.</span></span>  

<span data-ttu-id="ed45b-107">Remitteringssystemet håndterer alle feilkoder som kan sendes via returfiler.</span><span class="sxs-lookup"><span data-stu-id="ed45b-107">The remittance system handles all error codes which can be sent through the return files.</span></span> <span data-ttu-id="ed45b-108">Det er ikke nødvendig å utføre manuelle annulleringer av betalinger som er avvist av banken.</span><span class="sxs-lookup"><span data-stu-id="ed45b-108">It is not required to manually cancel payments rejected by the bank.</span></span>  

## <a name="types-of-errors"></a><span data-ttu-id="ed45b-109">Feiltyper</span><span class="sxs-lookup"><span data-stu-id="ed45b-109">Types of Errors</span></span>  
<span data-ttu-id="ed45b-110">Det finnes to typer remitteringsfeil:</span><span class="sxs-lookup"><span data-stu-id="ed45b-110">There are two types of remittance errors:</span></span>  

- <span data-ttu-id="ed45b-111">Overføringsfeil</span><span class="sxs-lookup"><span data-stu-id="ed45b-111">Transfer error</span></span>  
- <span data-ttu-id="ed45b-112">Avvisning</span><span class="sxs-lookup"><span data-stu-id="ed45b-112">Rejection</span></span>  

## <a name="transfer-errors"></a><span data-ttu-id="ed45b-113">Overføringsfeil</span><span class="sxs-lookup"><span data-stu-id="ed45b-113">Transfer Errors</span></span>  
<span data-ttu-id="ed45b-114">Hvis det oppstår feil under overføring, og det ikke opprettes returdata, har ikke banken mottatt betalingene.</span><span class="sxs-lookup"><span data-stu-id="ed45b-114">If errors occur during transfer and no return data is created, payments have not been received by the bank.</span></span>  

<span data-ttu-id="ed45b-115">Hvis betalingsfilen ikke kan sendes til banken, må du annullere oppdraget i remitteringssystemet.</span><span class="sxs-lookup"><span data-stu-id="ed45b-115">If the payment file cannot be sent to the bank, you must cancel the payment order in the remittance system.</span></span>  

## <a name="rejections"></a><span data-ttu-id="ed45b-116">Avslag</span><span class="sxs-lookup"><span data-stu-id="ed45b-116">Rejections</span></span>  
<span data-ttu-id="ed45b-117">Hvis det oppstår en feil eller mangler informasjon i forbindelse med en betaling som ble sendt til banken, inneholder returen en avvisning av betalingen.</span><span class="sxs-lookup"><span data-stu-id="ed45b-117">If there is an error or information is missing with a payment that was sent to the bank, the return will contain a rejection of the payment.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ed45b-118">Avvisninger kan variere fra bank til bank.</span><span class="sxs-lookup"><span data-stu-id="ed45b-118">Rejections vary from bank to bank.</span></span> <span data-ttu-id="ed45b-119">Kontakt banken din for å få informasjon om hvordan du skal håndtere avvisning av betalinger.</span><span class="sxs-lookup"><span data-stu-id="ed45b-119">Contact your bank regarding how to handle rejection of payments.</span></span>  

<span data-ttu-id="ed45b-120">Hvis betalingen avvises, vises feilkoden fra banken samt en forklaring for betalingen på siden **Ventekladd**.</span><span class="sxs-lookup"><span data-stu-id="ed45b-120">If there is a rejection, the error code from the bank and an explanation is displayed for the payment on the **Waiting Journal** page.</span></span> <span data-ttu-id="ed45b-121">Du må håndtere avvisningen, avhengig av hvordan remitteringsavtalen er satt opp.</span><span class="sxs-lookup"><span data-stu-id="ed45b-121">You will have to handle the rejection based how the remittance agreement was set up.</span></span> <span data-ttu-id="ed45b-122">Se [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="ed45b-122">For more information, see [Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed45b-123">Se også</span><span class="sxs-lookup"><span data-stu-id="ed45b-123">See Also</span></span>  
 <span data-ttu-id="ed45b-124">[Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-124">[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md) </span></span>  
 <span data-ttu-id="ed45b-125">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-125">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="ed45b-126">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-126">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="ed45b-127">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-127">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="ed45b-128">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-128">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="ed45b-129">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-129">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="ed45b-130">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-130">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="ed45b-131">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-131">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="ed45b-132">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-132">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="ed45b-133">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-133">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="ed45b-134">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-134">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="ed45b-135">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-135">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="ed45b-136">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-136">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="ed45b-137">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="ed45b-137">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="ed45b-138">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="ed45b-138">Cancel Payments</span></span>](how-to-cancel-payments.md)
