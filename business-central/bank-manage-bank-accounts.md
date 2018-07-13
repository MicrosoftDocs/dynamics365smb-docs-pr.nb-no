---
title: "Håndtere bankkonti| Microsoft-dokumentasjon"
description: "Du må regelmessig avstemme bankposter med de relaterte banktransaksjonene i bankkontiene."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: nb-no
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="a6ea4-103">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="a6ea4-103">Managing Bank Accounts</span></span>
<span data-ttu-id="a6ea4-104">Med jevne mellomrom må du avstemme bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med tilknyttede banktransaksjoner i bankkontoer i banken din, og deretter bokføre saldoen på bankkontoen din.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="a6ea4-105">Du kan utføre denne oppgaven som en del av behandling av betalinger, som er representert i et bankkontoutdrag i **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="a6ea4-106">Alternativt kan du utføre oppgaven separat fra betalingsbehandlingen i **Bankkontoavstemming**-vinduet der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="a6ea4-107">I begge vinduene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="a6ea4-108">I nord-amerikanske versjoner kan du også utføre bankavstemming i **Bankavstemmingsforslag**-vinduet, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="a6ea4-109">Hvis du vil bruke dette vinduet i stedet for **Bankkontoavstemming**-vinduet, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** i vinduet **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="a6ea4-110">Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="a6ea4-111">Noen ganger må du overføre beløp mellom bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile overføringer i banken.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="a6ea4-112">Du utfører denne oppgaven på ulike måter i vinduet **Finanskladd**, avhengig av valutaen for midlene.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="a6ea4-113">Før du kan administrere bankkonti, må du definere hver bankkonto som et bankkort.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="a6ea4-114">I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="a6ea4-115">Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="a6ea4-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="a6ea4-116">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="a6ea4-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="a6ea4-117">To</span></span> | <span data-ttu-id="a6ea4-118">Se</span><span class="sxs-lookup"><span data-stu-id="a6ea4-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="a6ea4-119">Avstemme bankkonti i forbindelse med betalingsbehandling i vinduet **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="a6ea4-120">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="a6ea4-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="a6ea4-121">Avstemme bankkonti, inkludert sjekkposter, som en separat oppgave i vinduet **Bankkontoavstemming**.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="a6ea4-122">Avstemme bankkonti separat</span><span class="sxs-lookup"><span data-stu-id="a6ea4-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="a6ea4-123">Bokføre overføringer mellom bankkonti i samme eller ulike valutaer.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="a6ea4-124">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="a6ea4-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="a6ea4-125">Se også</span><span class="sxs-lookup"><span data-stu-id="a6ea4-125">See Also</span></span>
[<span data-ttu-id="a6ea4-126">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="a6ea4-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="a6ea4-127">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="a6ea4-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="a6ea4-128">[Administrere skyldige beløp](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="a6ea4-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="a6ea4-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6ea4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a6ea4-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="a6ea4-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

