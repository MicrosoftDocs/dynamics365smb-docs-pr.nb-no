---
title: Behandle leverandørgjeld | Microsoft-dokumentasjon
description: Oversikt over hvordan du behandler leverandørgjeld, inkludert leverandørbetalinger, kreditorer, gjeld og forfalt saldo.
services: project-madeira
documentationcenter: ''
author: bholtorf
manager: edupont
editor: ''
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: abf7e9cf01c8d394a022e384584e32e78c754639
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802691"
---
# <a name="managing-payables"></a><span data-ttu-id="a975f-103">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="a975f-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a975f-104">har det du trenger for å effektivt administrere leverandører.</span><span class="sxs-lookup"><span data-stu-id="a975f-104">has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="a975f-105">Betalinger</span><span class="sxs-lookup"><span data-stu-id="a975f-105">Payments</span></span>
<span data-ttu-id="a975f-106">Det er enkelt å prioritere betalinger, vurdere straffer for forfalte betalinger og håndtere rabatter for tidlige betalinger.</span><span class="sxs-lookup"><span data-stu-id="a975f-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="a975f-107">Du kan registrere betalinger i en finanskladd og deretter skrive ut sjekker før bokføring av utbetalingskladden.</span><span class="sxs-lookup"><span data-stu-id="a975f-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="a975f-108">Du kan utligne betalinger mot lukkede fakturaer når du bokfører betalingen, eller etter at du har bokført betalingen.</span><span class="sxs-lookup"><span data-stu-id="a975f-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="a975f-109">**Utligningsmetode** angitt for leverandøren (på **leverandørkortet**) bestemmer om du utligner betalingen manuelt eller automatisk.</span><span class="sxs-lookup"><span data-stu-id="a975f-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="a975f-110">Du kan alltid utligne transaksjoner manuelt.</span><span class="sxs-lookup"><span data-stu-id="a975f-110">You can always apply transactions manually.</span></span> <span data-ttu-id="a975f-111">Hvis utligningsmetoden for leverandøren er **Saldo** og du ikke angir et dokument som betalingen skal utlignes mot, vil betalingen imidlertid bli utlignet mot den eldste åpne posten for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="a975f-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="a975f-112">Betalingsforslag - leverandør</span><span class="sxs-lookup"><span data-stu-id="a975f-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a975f-113">kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="a975f-113">can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="a975f-114">Betalingsforslaget kan ta hensyn til et beløp du angir som tilgjengelige betalingsbeløp og berettigelse til kontantrabatter.</span><span class="sxs-lookup"><span data-stu-id="a975f-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="a975f-115">Utstede sjekker</span><span class="sxs-lookup"><span data-stu-id="a975f-115">Issue Checks</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="a975f-116">lar deg utstede sjekker til leverandører manuelt og elektronisk.</span><span class="sxs-lookup"><span data-stu-id="a975f-116">lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="a975f-117">Du kan gjøre begge deler på **Utbetalingskladder**-siden, der du kan kansellere sjekker og vise sjekkposter.</span><span class="sxs-lookup"><span data-stu-id="a975f-117">You do both on the **Payment Journals** page, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="a975f-118">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="a975f-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="a975f-119">Når du er klar til betale en leverandør, kan du fra siden **Betalingskladd** eksportere en fil med betalingsinformasjonen fra kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="a975f-119">When you are ready to pay a vendor, from the **Payment Journal** page you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="a975f-120">Du kan deretter laste opp filen til nettbanken for å behandle pengeoverføringene.</span><span class="sxs-lookup"><span data-stu-id="a975f-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="a975f-121">Hvis du ikke vil bokføre en utbetalingskladdelinje for en eksportert betaling, for eksempel fordi du venter på at banken skal bekrefte transaksjonen, kan du bare slette kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="a975f-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="a975f-122">Når du senere oppretter en utbetalingskladdelinje for å betale restbeløpet på fakturaen, viser feltet **Totalt eksportert beløp** hvor mye av betalingsbeløpet som allerede er eksportert.</span><span class="sxs-lookup"><span data-stu-id="a975f-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="a975f-123">Du kan også finne detaljert informasjon om det eksporterte totalbeløpet ved å velge knappen **Poster i kredittoverføringsreg.**</span><span class="sxs-lookup"><span data-stu-id="a975f-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="a975f-124">Hvis du venter med å bokføre innbetalinger til etter at banken bekrefter at den har behandlet transaksjoner, er det to måter å unngå utilsiktet eksport av betalinger for åpne dokumenter:</span><span class="sxs-lookup"><span data-stu-id="a975f-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="a975f-125">I en betalingskladd med foreslåtte betalingslinjer kan du sortere etter kolonnen **Lest ut til betalingsfil** eller **Totalt eksportert beløp**, og deretter slette betalingsforslag for åpne fakturaer som allerede er betalt og du ikke ønsker å betale.</span><span class="sxs-lookup"><span data-stu-id="a975f-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="a975f-126">**Merk:** Det kan være du må legge til disse kolonnene i oversikten.</span><span class="sxs-lookup"><span data-stu-id="a975f-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="a975f-127">Hvis du vil ha mer informasjon, se [Tilpasse arbeidsområdet ](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="a975f-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="a975f-128">Du kan også merke av for **Hopp over eksporterte betalinger** i kjørselen **Betalingsforslag - leverandør**, der du angir hvilke betalinger som skal inkluderes i utbetalingskladden, hvis du ikke vil sette inn kladdelinjer for betalinger som allerede er eksportert.</span><span class="sxs-lookup"><span data-stu-id="a975f-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="a975f-129">Se også</span><span class="sxs-lookup"><span data-stu-id="a975f-129">See Also</span></span>
[<span data-ttu-id="a975f-130">Betalingsmåter</span><span class="sxs-lookup"><span data-stu-id="a975f-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="a975f-131">Finans</span><span class="sxs-lookup"><span data-stu-id="a975f-131">Finance</span></span>](finance.md)  
<span data-ttu-id="a975f-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a975f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
