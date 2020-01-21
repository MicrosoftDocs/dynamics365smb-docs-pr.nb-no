---
title: Håndtere bankkonti| Microsoft-dokumentasjon
description: Du må regelmessig avstemme bankposter med de relaterte banktransaksjonene i bankkontiene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 01/10/2020
ms.author: sgroespe
ms.openlocfilehash: 0d1a38468f5d07a1170027bc728ba16996f2b782
ms.sourcegitcommit: 2f741f442226b8be74586e355f283f365e43220f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947240"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="1d21c-103">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="1d21c-103">Reconciling Bank Accounts</span></span>
<span data-ttu-id="1d21c-104">En bankavstemming bør fullføres med jevne mellomrom for alle bankkontoene for å sikre at firmaets kontantposter er riktige.</span><span class="sxs-lookup"><span data-stu-id="1d21c-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="1d21c-105">Dette gjør du ved å sammenligne og utligne poster i de interne bankkontoene med banktransaksjoner i banken, og deretter bokføre saldoene på de interne bankkontoene for å gjøre totaler tilgjengelige for finansledere.</span><span class="sxs-lookup"><span data-stu-id="1d21c-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="1d21c-106">Bankavstemming er også en praktisk måte å oppdage og løse manglende betalinger og bokføringsfeil.</span><span class="sxs-lookup"><span data-stu-id="1d21c-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="1d21c-107">Du kan utføre oppgaven på **Bankkontoavstemming**-siden der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten.</span><span class="sxs-lookup"><span data-stu-id="1d21c-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="1d21c-108">Du kan også utføre denne oppgaven på siden **Betalingsavstemmingskladd** som en del av behandling av betalinger, som er representert i et bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="1d21c-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="1d21c-109">På begge sidene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.</span><span class="sxs-lookup"><span data-stu-id="1d21c-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="1d21c-110">I nord-amerikanske versjoner kan du også utføre bankavstemming på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="1d21c-110">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="1d21c-111">Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="1d21c-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="1d21c-112">Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="1d21c-112">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="1d21c-113">Før du kan administrere bankkontoer i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du definere hver bankkonto som et bankkort.</span><span class="sxs-lookup"><span data-stu-id="1d21c-113">Before you can manage your bank accounts within [!INCLUDE[d365fin](includes/d365fin_md.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="1d21c-114">I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="1d21c-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="1d21c-115">Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="1d21c-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="1d21c-116">Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="1d21c-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="1d21c-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="1d21c-117">To</span></span> | <span data-ttu-id="1d21c-118">Se</span><span class="sxs-lookup"><span data-stu-id="1d21c-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="1d21c-119">Du avstemmer bankkontoer som en separat oppgave på siden **Bankkontoavstemming**.</span><span class="sxs-lookup"><span data-stu-id="1d21c-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="1d21c-120">Avstemme bankkontoer</span><span class="sxs-lookup"><span data-stu-id="1d21c-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="1d21c-121">Avstemme bankkonti i forbindelse med betalingsbehandling på siden **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="1d21c-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="1d21c-122">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="1d21c-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

## <a name="see-related-training-at-microsoft-learnlearnpathsreconcile-bank-accounts-dynamics-365-business-central"></a><span data-ttu-id="1d21c-123">Se relatert opplæring på [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="1d21c-123">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="1d21c-124">Se også</span><span class="sxs-lookup"><span data-stu-id="1d21c-124">See Also</span></span>
[<span data-ttu-id="1d21c-125">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="1d21c-125">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="1d21c-126">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="1d21c-126">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="1d21c-127">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="1d21c-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="1d21c-128">[Administrere skyldige beløp](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="1d21c-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="1d21c-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d21c-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1d21c-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="1d21c-130">General Business Functionality</span></span>](ui-across-business-areas.md)
