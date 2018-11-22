---
title: "Elektroniske betalinger til leverandører i Norge"
description: "Forbedringer i den norske versjonen inkluderer automatisk betaling til leverandører."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: fda1ce632f44230eb6d6a9b7045f087e5abffff8
ms.contentlocale: nb-no
ms.lasthandoff: 10/15/2018

---
# <a name="electronic-payments-to-vendors-in-norway"></a><span data-ttu-id="502b9-103">Elektroniske betalinger til leverandører i Norge</span><span class="sxs-lookup"><span data-stu-id="502b9-103">Electronic Payments to Vendors in Norway</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="502b9-104">inkluderer forbedringer i den norske versjonen for automatisk betaling til leverandører.</span><span class="sxs-lookup"><span data-stu-id="502b9-104">includes Norwegian enhancements for automatically making payments to vendors.</span></span> <span data-ttu-id="502b9-105">Dette reduserer sjansen for at feil skal oppstå på grunn av manuell registrering av data.</span><span class="sxs-lookup"><span data-stu-id="502b9-105">This reduces errors that occur from manual data entry.</span></span> <span data-ttu-id="502b9-106">Denne funksjonaliteten kan brukes til å utføre følgende operasjoner:</span><span class="sxs-lookup"><span data-stu-id="502b9-106">You can use this functionality to perform the following operations:</span></span>  

- <span data-ttu-id="502b9-107">Søke etter fakturaer som er forfalt, basert på ulike kriterier.</span><span class="sxs-lookup"><span data-stu-id="502b9-107">Search invoices that are due based on different conditions.</span></span>  
- <span data-ttu-id="502b9-108">Sende betalinger til banken.</span><span class="sxs-lookup"><span data-stu-id="502b9-108">Send payments to the bank.</span></span>  
- <span data-ttu-id="502b9-109">Motta meldinger fra banken om status for betalinger.</span><span class="sxs-lookup"><span data-stu-id="502b9-109">Receive messages from the bank on the status of payments.</span></span>  
- <span data-ttu-id="502b9-110">Motta informasjon om betalte transaksjoner som skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="502b9-110">Receive paid transaction information to be posted.</span></span>  

<span data-ttu-id="502b9-111">Du kan utføre elektroniske betalinger i følgende formater:</span><span class="sxs-lookup"><span data-stu-id="502b9-111">You can make electronic payments using the following formats:</span></span>  

- <span data-ttu-id="502b9-112">TelePay</span><span class="sxs-lookup"><span data-stu-id="502b9-112">TelePay</span></span>  
- <span data-ttu-id="502b9-113">Remitteringsoppdrag</span><span class="sxs-lookup"><span data-stu-id="502b9-113">Remittance payment</span></span>  

## <a name="electronic-payment-process"></a><span data-ttu-id="502b9-114">Elektronisk betalingsprosess</span><span class="sxs-lookup"><span data-stu-id="502b9-114">Electronic Payment Process</span></span>  
<span data-ttu-id="502b9-115">Elektroniske betalinger behandles på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="502b9-115">The following steps show how electronic payments are processed:</span></span>  

1.  <span data-ttu-id="502b9-116">Betalingsforslaget kjøres i den elektroniske betalingsfunksjonen og overføres til banken ved hjelp av bankens programvare.</span><span class="sxs-lookup"><span data-stu-id="502b9-116">The payment proposal is run in the electronic payments feature and transferred to the bank by using the bank’s software.</span></span>  
2.  <span data-ttu-id="502b9-117">Bankens programvare mottar betalingene og overfører dem til banken.</span><span class="sxs-lookup"><span data-stu-id="502b9-117">The bank's software receives the payments and transfers payments to the bank.</span></span>  
3.  <span data-ttu-id="502b9-118">Banken mottar betalingene og sender den første mottaksreturen til [!INCLUDE[d365fin](../../includes/d365fin_md.md)] via bankens programvare.</span><span class="sxs-lookup"><span data-stu-id="502b9-118">The bank receives the payments and sends the first-time return receipt to [!INCLUDE[d365fin](../../includes/d365fin_md.md)] using the bank's software.</span></span>  
4.  <span data-ttu-id="502b9-119">Banken utfører betalingene og sender avregningsreturen (andre mottaksretur) til [!INCLUDE[d365fin](../../includes/d365fin_md.md)] via bankens programvare, hvor betalingene bokføres.</span><span class="sxs-lookup"><span data-stu-id="502b9-119">The bank executes the payments and sends the settlement return (second-time return receipt) to [!INCLUDE[d365fin](../../includes/d365fin_md.md)] using the bank's software where the payments are posted.</span></span>  

## <a name="vendor-payment-requirements"></a><span data-ttu-id="502b9-120">Krav til leverandørbetalinger</span><span class="sxs-lookup"><span data-stu-id="502b9-120">Vendor Payment Requirements</span></span>  
<span data-ttu-id="502b9-121">Hvis betalingstransaksjonene ikke oppfyller kravene, vises en feilmelding, og du kan ikke opprette en betalingsfil for overføringer til banken.</span><span class="sxs-lookup"><span data-stu-id="502b9-121">If the payment transactions do not fulfill the requirements, an error message appears and you cannot create a payment file for transfers to the bank.</span></span> <span data-ttu-id="502b9-122">Følgende kriterier må oppfylles ved når du behandler betalinger til leverandører:</span><span class="sxs-lookup"><span data-stu-id="502b9-122">The following criteria must be met when you process payments to vendors:</span></span>  

- <span data-ttu-id="502b9-123">Betalingstransaksjonen må være positiv eller null.</span><span class="sxs-lookup"><span data-stu-id="502b9-123">The payment transaction must be positive or zero.</span></span> <span data-ttu-id="502b9-124">En betalingstransaksjon må overføre et positivt beløp (eller null) til betalingsmottakeren.</span><span class="sxs-lookup"><span data-stu-id="502b9-124">A payment transaction must transfer a positive amount (or zero) to the payment receiver.</span></span> <span data-ttu-id="502b9-125">Dette betyr at når en kreditnota skal trekkes fra, må fakturaen i samme betalingstransaksjon lyde på det samme eller et høyere beløp.</span><span class="sxs-lookup"><span data-stu-id="502b9-125">This means that deducting a credit memo requires an invoice with the same or higher amount in the same payment transaction.</span></span> <span data-ttu-id="502b9-126">Det er ikke mulig å trekke fra penger på leverandørens konto.</span><span class="sxs-lookup"><span data-stu-id="502b9-126">Money cannot be deducted from the vendor's account.</span></span>  

- <span data-ttu-id="502b9-127">Det må anvendes en kreditnota sammen med fakturaen.</span><span class="sxs-lookup"><span data-stu-id="502b9-127">A credit memo must be applied with the invoice.</span></span> <span data-ttu-id="502b9-128">En kreditnota inneholder vanligvis ikke en Kunde-ID (KID).</span><span class="sxs-lookup"><span data-stu-id="502b9-128">Generally a credit memo does not contain a Kunde ID (KID).</span></span> <span data-ttu-id="502b9-129">Du kan ikke betale en kreditnota i en betalingstransaksjon med fakturaer som inneholder et KID-nummer.</span><span class="sxs-lookup"><span data-stu-id="502b9-129">You cannot pay a credit memo in a payment transaction with invoices that contain a KID.</span></span> <span data-ttu-id="502b9-130">Årsaken er at betalinger vanligvis deles opp i transaksjoner med eller uten KID-nummer.</span><span class="sxs-lookup"><span data-stu-id="502b9-130">This is because payments are usually split into transactions with or without a KID.</span></span> <span data-ttu-id="502b9-131">Det betyr at hvis en kreditnota uten KID-nummer betales sammen med en faktura i samme betalingstransaksjon, må fakturaen betales uten KID-nummer, og mottakerreferansenummeret må brukes i stedet.</span><span class="sxs-lookup"><span data-stu-id="502b9-131">This means that if a credit memo without a KID is paid with an invoice in the same payment transaction, the invoice must be paid without a KID, and the recipient reference number must be used instead.</span></span>  

- <span data-ttu-id="502b9-132">Hvis fakturaen og kreditnotaen betales i samme betalingstransaksjon, må betalingen finne sted på samme dato, i samme valuta og med samme valutakurs.</span><span class="sxs-lookup"><span data-stu-id="502b9-132">If the invoice and credit memo are paid in the same payment transaction, the payment must occur on the same date using the same currency and exchange rate.</span></span>  

## <a name="see-also"></a><span data-ttu-id="502b9-133">Se også</span><span class="sxs-lookup"><span data-stu-id="502b9-133">See Also</span></span>  
 <span data-ttu-id="502b9-134">[Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-134">[Norway Local Functionality](norway-local-functionality.md) </span></span>  
 <span data-ttu-id="502b9-135">[Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-135">[Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md) </span></span>  
 <span data-ttu-id="502b9-136">[Opprette remitteringskontoer](how-to-create-remittance-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-136">[Create Remittance Accounts](how-to-create-remittance-accounts.md) </span></span>  
 <span data-ttu-id="502b9-137">[Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-137">[Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md) </span></span>  
 <span data-ttu-id="502b9-138">[Mottakerreferansekoder](recipient-reference-codes.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-138">[Recipient Reference Codes](recipient-reference-codes.md) </span></span>  
 <span data-ttu-id="502b9-139">[Opprette remitteringsforslag](how-to-create-remittance-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-139">[Create Remittance Suggestions](how-to-create-remittance-suggestions.md) </span></span>  
 <span data-ttu-id="502b9-140">[Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-140">[Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md) </span></span>  
 <span data-ttu-id="502b9-141">[Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-141">[Set Up Payment Line Information](how-to-set-up-payment-line-information.md) </span></span>  
 <span data-ttu-id="502b9-142">[Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-142">[Test Remittance Payments](how-to-test-remittance-payments.md) </span></span>  
 <span data-ttu-id="502b9-143">[Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-143">[Export Remittance Payments](how-to-export-remittance-payments.md) </span></span>  
 <span data-ttu-id="502b9-144">[Typer betalingsreturfiler](types-of-payment-returns-files.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-144">[Types of Payment Returns Files](types-of-payment-returns-files.md) </span></span>  
 <span data-ttu-id="502b9-145">[Importere betalingsreturdata](how-to-import-payment-return-data.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-145">[Import Payment Return Data](how-to-import-payment-return-data.md) </span></span>  
 <span data-ttu-id="502b9-146">[Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-146">[Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md) </span></span>  
 <span data-ttu-id="502b9-147">[Remitteringsfeil](remittance-errors.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-147">[Remittance Errors](remittance-errors.md) </span></span>  
 <span data-ttu-id="502b9-148">[Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md) </span><span class="sxs-lookup"><span data-stu-id="502b9-148">[View Remittance Error Codes](how-to-view-remittance-error-codes.md) </span></span>  
 [<span data-ttu-id="502b9-149">Annullere betalinger</span><span class="sxs-lookup"><span data-stu-id="502b9-149">Cancel Payments</span></span>](how-to-cancel-payments.md)
