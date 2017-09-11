---
title: "Oversikt over oppgaver for å behandle leverandørgjeld | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å behandle leverandørgjeld, for eksempel betale kreditorer eller utligne utgående betalinger mot poster for å lukke fakturaer eller kreditnotaer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9684a91268927a4f1f4d249fef019c8f6ac00325
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="managing-payables"></a><span data-ttu-id="dec28-103">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="dec28-103">Managing Payables</span></span>
<span data-ttu-id="dec28-104">En stor del av administrasjon av skyldige beløp består av å betale dine leverandører.</span><span class="sxs-lookup"><span data-stu-id="dec28-104">A big part of managing accounts payable is paying your vendors.</span></span> <span data-ttu-id="dec28-105">Du kan bruke funksjoner til å legge til betalingslinjer for forfalte kjøpsfakturaer i vinduet **Utbetalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="dec28-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="dec28-106">Du kan sende transaksjoner til banken din ved å eksportere flere betalingskladdelinjer til en fil og deretter laste opp filen til banken.</span><span class="sxs-lookup"><span data-stu-id="dec28-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="dec28-107">Du kan også betale med sjekk, inkludert å overføre sjekker som elektroniske betalinger.</span><span class="sxs-lookup"><span data-stu-id="dec28-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="dec28-108">En annen vanlig oppgave er å utligne utgående betalinger mot deres relaterte leverandørposter for å kunne lukke de beslektede kjøpsfakturaene eller kjøpskreditnotaene som betalt.</span><span class="sxs-lookup"><span data-stu-id="dec28-108">Another typical task is to apply outgoing payments to their related vendor ledger entries in order to close purchase invoices or purchase credit memos as paid.</span></span> <span data-ttu-id="dec28-109">Du kan gjøre dette i vinduet **Betalingsavstemmingskladd** ved å importere en bankkontoutdragsfil for hurtig å registrere betalinger.</span><span class="sxs-lookup"><span data-stu-id="dec28-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="dec28-110">Betaling brukes til å åpne kunde- eller kundepostoppføringer ved å sammenligne betalingstekst for oppføringsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="dec28-110">The payments are applied to open vendor or customer ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="dec28-111">Det finnes ulike måter å se gjennom og endre treff før du bokfører kladden.</span><span class="sxs-lookup"><span data-stu-id="dec28-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="dec28-112">Du kan velge å lukke alle åpne bankposter relatert til de utlignede postene når du bokfører kladden.</span><span class="sxs-lookup"><span data-stu-id="dec28-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="dec28-113">Bankkontoen avstemmes automatisk når alle betalinger er utlignet.</span><span class="sxs-lookup"><span data-stu-id="dec28-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="dec28-114">Du kan også bruke utgående betalinger manuelt i vinduet **Betalingskladd** eller fra de relaterte leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="dec28-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor ledger entries.</span></span>

<span data-ttu-id="dec28-115">Tabellen nedenfor beskriver en sekvens av oppgaver i leverandørgjeld, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="dec28-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="dec28-116">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="dec28-116">To</span></span> | <span data-ttu-id="dec28-117">Se</span><span class="sxs-lookup"><span data-stu-id="dec28-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="dec28-118">Generere forfalte leverandørbetalinger prioritert i henhold til kontantrabatter og forfalte straffegebyrer.</span><span class="sxs-lookup"><span data-stu-id="dec28-118">Generate due vendor payments prioritized according to payment discounts and overdue penalties.</span></span> <span data-ttu-id="dec28-119">Du kan også eksportere betalingene til en bankfil ved bokføring.</span><span class="sxs-lookup"><span data-stu-id="dec28-119">Optionally, export the payments to a bank file when posting.</span></span> |[<span data-ttu-id="dec28-120">Foreta betalinger</span><span class="sxs-lookup"><span data-stu-id="dec28-120">Make Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="dec28-121">Utligne leverandørbetalinger automatisk på ubetalte kjøpsfakturaer ved å importere en bankkontoutdragsfil.</span><span class="sxs-lookup"><span data-stu-id="dec28-121">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="dec28-122">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="dec28-122">Apply Payments Automatically and Reconcile Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="dec28-123">Utligne leverandørbetalinger på ubetalte fakturaer manuelt.</span><span class="sxs-lookup"><span data-stu-id="dec28-123">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="dec28-124">Avstemme leverandørbetalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="dec28-124">How to: Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="dec28-125">Sikre riktig lagerverdisetting ved å tilordne ekstra varekost, for eksempel frakt, fysisk håndtering, forsikring og transport, som du pådrar deg ved innkjøp.</span><span class="sxs-lookup"><span data-stu-id="dec28-125">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="dec28-126">Bruke varegebyr til å gjøre rede for ekstra handelskostnader</span><span class="sxs-lookup"><span data-stu-id="dec28-126">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="dec28-127">Se også</span><span class="sxs-lookup"><span data-stu-id="dec28-127">See Also</span></span>
[<span data-ttu-id="dec28-128">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="dec28-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="dec28-129">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="dec28-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="dec28-130">Bruke varegebyr til å gjøre rede for ekstra handelskostnader</span><span class="sxs-lookup"><span data-stu-id="dec28-130">How to: Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="dec28-131">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="dec28-131">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="dec28-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dec28-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

