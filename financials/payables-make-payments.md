---
title: "Oversikt over oppgaver for å behandle betalinger til leverandører | Microsoft-dokumentasjon"
description: "Gir en oversikt over oppgavene for å behandle betalinger til leverandører eller kreditorer, inkludert bokføring av betalingslinjene og oversikt over forfalt saldo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="3eec1-103">Foreta betalinger</span><span class="sxs-lookup"><span data-stu-id="3eec1-103">Make Payments</span></span>
<span data-ttu-id="3eec1-104">Når du foretar betalinger til leverandører, kan du bokføre de relaterte betalingslinjene i vinduet **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="3eec1-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="3eec1-105">Du kan bruke funksjonen **Betalingsforslag – leverandør** til å finne betalinger som har forfalt.</span><span class="sxs-lookup"><span data-stu-id="3eec1-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="3eec1-106">Du kan også bruker rapporten **Leverandør – forfallsoversikt** til å få oversikt over betalinger som har forfalt.</span><span class="sxs-lookup"><span data-stu-id="3eec1-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="3eec1-107">Fra betalingskladden kan du skrive ut maskinelle sjekker eller registrere når sjekker skrives.</span><span class="sxs-lookup"><span data-stu-id="3eec1-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="3eec1-108">Hvis du velger **Maskinell sjekk** i feltet **Bankbetalingstype**, må eventuelle linjer som representerer sjekker skrives ut før betalingskladden kan bokføres.</span><span class="sxs-lookup"><span data-stu-id="3eec1-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="3eec1-109">Når betalingene er bokført, kan du eksportere dem til en bankfil for opplasting til banken for behandling.</span><span class="sxs-lookup"><span data-stu-id="3eec1-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="3eec1-110">Når betalingene er foretatt i banken, må du utligne dem på deres tilknyttede åpne leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="3eec1-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="3eec1-111">Du kan gjøre dette manuelt eller ved å importere en bankkontoutdragsfil og utligne betalingene automatisk.</span><span class="sxs-lookup"><span data-stu-id="3eec1-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="3eec1-112">Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="3eec1-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="3eec1-113">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="3eec1-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="3eec1-114">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="3eec1-114">To</span></span> | <span data-ttu-id="3eec1-115">Se</span><span class="sxs-lookup"><span data-stu-id="3eec1-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="3eec1-116">Bruke en funksjon til å foreslå leverandørbetalinger i henhold til valgte kriterier som forfallsdato, rabatt arbeidstillatelse og din likviditet.</span><span class="sxs-lookup"><span data-stu-id="3eec1-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="3eec1-117">Foreslå leverandørbetalinger</span><span class="sxs-lookup"><span data-stu-id="3eec1-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="3eec1-118">Utstede sjekker for betalinger, enten som utskrifter eller maskinelle sjekker.</span><span class="sxs-lookup"><span data-stu-id="3eec1-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="3eec1-119">Kansellere sjekker før eller etter bokføring.</span><span class="sxs-lookup"><span data-stu-id="3eec1-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="3eec1-120">Arbeide med sjekker</span><span class="sxs-lookup"><span data-stu-id="3eec1-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="3eec1-121">Du kan sørge for at at banken bare fjerner validerte sjekker og beløp ved å sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling.</span><span class="sxs-lookup"><span data-stu-id="3eec1-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="3eec1-122">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="3eec1-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="3eec1-123">Eksporter betalinger fra vinduet **Utbetalingskladd** til en bankfil som du laster opp til banken for behandling, inkludert EFT (elektronisk pengeoverføring) i Nord-Amerika.</span><span class="sxs-lookup"><span data-stu-id="3eec1-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="3eec1-124">Fremgangsmåte: Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="3eec1-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="3eec1-125">Se også</span><span class="sxs-lookup"><span data-stu-id="3eec1-125">See Also</span></span>
[<span data-ttu-id="3eec1-126">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="3eec1-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="3eec1-127">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="3eec1-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="3eec1-128">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="3eec1-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="3eec1-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3eec1-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

