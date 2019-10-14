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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9e5fe99fe822ca94758a3030659bf484f917fcaa
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308383"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="8b29a-103">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="8b29a-103">Managing Bank Accounts</span></span>
<span data-ttu-id="8b29a-104">Med jevne mellomrom må du avstemme bankposter i [!INCLUDE[d365fin](includes/d365fin_md.md)] med tilknyttede banktransaksjoner i bankkontoer i banken din, og deretter bokføre saldoen på bankkontoen din.</span><span class="sxs-lookup"><span data-stu-id="8b29a-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="8b29a-105">Du kan utføre denne oppgaven som en del av behandling av betalinger, som er representert i et bankkontoutdrag i **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="8b29a-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="8b29a-106">Alternativt kan du utføre oppgaven separat fra betalingsbehandlingen på **Bankkontoavstemming**-siden der du avstemmer bankekontoutdragslinjene i ruten til venstre med de interne bankkontopostene i den høyre ruten.</span><span class="sxs-lookup"><span data-stu-id="8b29a-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="8b29a-107">På begge sidene kan du fylle ut bankkontoutdragsinformasjon ved å importere en fil eller feed, og du kan bruke automatiske avstemmingsforslag.</span><span class="sxs-lookup"><span data-stu-id="8b29a-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="8b29a-108">I nord-amerikanske versjoner kan du også utføre bankavstemming på **Bankavstemmingsforslag**-siden, som er mer egnet for sjekker og innskudd, men tilbyr ikke import av filer med bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="8b29a-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="8b29a-109">Hvis du vil bruke denne siden i stedet for **Bankkontoavstemming**-siden, fjerner du avmerkingen for feltet **Bankavstemming med automatisk samsvar** på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="8b29a-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="8b29a-110">Hvis du vil ha mer informasjon, kan du se delen Avstemme bankkontoer under lokal funksjonalitet for USA.</span><span class="sxs-lookup"><span data-stu-id="8b29a-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="8b29a-111">Noen ganger må du overføre beløp mellom bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile overføringer i banken.</span><span class="sxs-lookup"><span data-stu-id="8b29a-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="8b29a-112">Du utfører denne oppgaven på ulike måter på siden **Finanskladd**, avhengig av valutaen for midlene.</span><span class="sxs-lookup"><span data-stu-id="8b29a-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="8b29a-113">Før du kan administrere bankkonti, må du definere hver bankkonto som et bankkort.</span><span class="sxs-lookup"><span data-stu-id="8b29a-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="8b29a-114">I tillegg må du definere elektroniske tjenester som du kan bruke for import av bankutdrag og eksport av betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="8b29a-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="8b29a-115">Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="8b29a-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="8b29a-116">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="8b29a-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="8b29a-117">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="8b29a-117">To</span></span> | <span data-ttu-id="8b29a-118">Se</span><span class="sxs-lookup"><span data-stu-id="8b29a-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="8b29a-119">Avstemme bankkonti i forbindelse med betalingsbehandling på siden **Betalingsavstemmingskladd**.</span><span class="sxs-lookup"><span data-stu-id="8b29a-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="8b29a-120">Utligne betalinger automatisk og avstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="8b29a-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="8b29a-121">Avstemme bankkonti, inkludert sjekkposter, som en separat oppgave på siden **Bankkontoavstemming**.</span><span class="sxs-lookup"><span data-stu-id="8b29a-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="8b29a-122">Avstemme bankkonti separat</span><span class="sxs-lookup"><span data-stu-id="8b29a-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="8b29a-123">Bokføre overføringer mellom bankkonti i samme eller ulike valutaer.</span><span class="sxs-lookup"><span data-stu-id="8b29a-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="8b29a-124">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="8b29a-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="8b29a-125">Se også</span><span class="sxs-lookup"><span data-stu-id="8b29a-125">See Also</span></span>
[<span data-ttu-id="8b29a-126">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="8b29a-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="8b29a-127">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="8b29a-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="8b29a-128">[Administrere skyldige beløp](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="8b29a-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="8b29a-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8b29a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="8b29a-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="8b29a-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
