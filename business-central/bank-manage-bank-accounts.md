---
title: Håndtere bankkonti| Microsoft-dokumentasjon
description: Du må regelmessig avstemme bankposter med de relaterte banktransaksjonene i bankkontiene.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c36e906c87cb17acb85d8cde32fdc51ee501469d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381734"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="aee2b-103">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="aee2b-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="aee2b-104">En bankavstemming bør fullføres med jevne mellomrom for alle bankkontoene for å sikre at firmaets kontantposter er riktige.</span><span class="sxs-lookup"><span data-stu-id="aee2b-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="aee2b-105">Dette gjør du ved å sammenligne og utligne poster i de interne bankkontoene med banktransaksjoner i banken, og deretter bokføre saldoene på de interne bankkontoene for å gjøre totaler tilgjengelige for finansledere.</span><span class="sxs-lookup"><span data-stu-id="aee2b-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="aee2b-106">Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.</span><span class="sxs-lookup"><span data-stu-id="aee2b-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="aee2b-107">Du kan utføre oppgaven på **Bankkontoavstemming**-siden der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten.</span><span class="sxs-lookup"><span data-stu-id="aee2b-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="aee2b-108">Du kan også utføre denne oppgaven på siden **Betalingsavstemmingskladd** som en del av behandling av betalinger, som er representert i et bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="aee2b-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="aee2b-109">På begge sidene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.</span><span class="sxs-lookup"><span data-stu-id="aee2b-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="aee2b-110">I nord-amerikanske versjoner kan du også utføre bankavstemming på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="aee2b-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="aee2b-111">Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="aee2b-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="aee2b-112">Hvis du vil ha mer informasjon, kan du se delen [Avstemme bankkontoer](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under lokal funksjonalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="aee2b-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="aee2b-113">Før du kan administrere bankkontoer i [!INCLUDE[prod_short](includes/prod_short.md)], må du definere hver bankkonto som et bankkort.</span><span class="sxs-lookup"><span data-stu-id="aee2b-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="aee2b-114">I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="aee2b-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="aee2b-115">Hvis du vil ha mer informasjon, kan du se [Konfigurere banktjenester](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="aee2b-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="aee2b-116">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="aee2b-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="aee2b-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="aee2b-117">To</span></span> | <span data-ttu-id="aee2b-118">Se</span><span class="sxs-lookup"><span data-stu-id="aee2b-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="aee2b-119">Du avstemmer bankkontoer som en separat oppgave på siden **Bankkontoavstemming**.</span><span class="sxs-lookup"><span data-stu-id="aee2b-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="aee2b-120">Avstemme bankkontoer</span><span class="sxs-lookup"><span data-stu-id="aee2b-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="aee2b-121">Avstemme bankkonti i forbindelse med betalingsbehandling på siden **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="aee2b-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="aee2b-122">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="aee2b-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="aee2b-123">Bruk bankavstemming til å kontrollere at bøkene er oppdaterte, og ikke bokføre avstemmingen før du er fornøyd med den.</span><span class="sxs-lookup"><span data-stu-id="aee2b-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="aee2b-124">Se relatert opplæring på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="aee2b-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="aee2b-125">Se også</span><span class="sxs-lookup"><span data-stu-id="aee2b-125">See Also</span></span>

[<span data-ttu-id="aee2b-126">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="aee2b-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="aee2b-127">Avstemme bankkontoer</span><span class="sxs-lookup"><span data-stu-id="aee2b-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="aee2b-128">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="aee2b-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="aee2b-129">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="aee2b-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="aee2b-130">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="aee2b-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="aee2b-131">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="aee2b-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="aee2b-132">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aee2b-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="aee2b-133">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="aee2b-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]