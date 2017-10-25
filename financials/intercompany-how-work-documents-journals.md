---
title: "Bokføre konserninterne dokumenter og kladder | Microsoft-dokumentasjon"
description: "Bruke konserninterne dokumenter til å bokføre transaksjoner med de konserninterne partnerne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: eeb070e1431d55248a762b444c2298281b0a5101
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-intercompany-documents-and-journals"></a><span data-ttu-id="a8487-103">Arbeide med konserninterne dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="a8487-103">How to: Work with Intercompany Documents and Journals</span></span>
<span data-ttu-id="a8487-104">Du bruker konserninterne dokumenter eller kladder til å bokføre transaksjoner med de konserninterne partnerne.</span><span class="sxs-lookup"><span data-stu-id="a8487-104">You use intercompany documents or journals to post transactions with your intercompany partners.</span></span> <span data-ttu-id="a8487-105">Når du bokfører et konserninternt dokument eller en kladdelinje i selskapet, opprettes det et tilsvarende dokument eller kladdelinje i den konserninterne utboksen som du kan overføre til partneren.</span><span class="sxs-lookup"><span data-stu-id="a8487-105">When you post an intercompany document or journal line in your company, a corresponding document or journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="a8487-106">Partneren kan deretter bokføre den tilsvarende transaksjonen i selskapet sitt, uten å måtte registrere dataene på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8487-106">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

<span data-ttu-id="a8487-107">For salgs-og kjøpsdokumenter sikrer den konserninterne partnerkoden på den involverte kunden eller leverandøren at alle ordrer og fakturaer som genereres i forbindelse med transaksjoner med disse selskapene, produserer tilhørende bilag i partnerselskapet, noe som fører til riktig balansering av kontoene.</span><span class="sxs-lookup"><span data-stu-id="a8487-107">For sales and purchase documents, the intercompany partner code on the involved customer or vendor ensures that all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>

<span data-ttu-id="a8487-108">For konserninterne finanskladdelinjer trenger du ikke å angi kontoene for et individuelt sett med bøker, men ganske enkelt gi identifikasjonen av partnerselskapet.</span><span class="sxs-lookup"><span data-stu-id="a8487-108">For intercompany general journal lines, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="a8487-109">Tilsvarende konserinterne finanskladdelinjer opprettes deretter i partnerselskapet, noe som fører til balansering av bøkene i begge selskapene som er involvert i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="a8487-109">Corresponding intercompany general journal lines are then created in the partner company that result in the balancing of the books of both companies involved in a transaction.</span></span>

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a><span data-ttu-id="a8487-110">Slik fyller du ut og sender en konsernintern ordre</span><span class="sxs-lookup"><span data-stu-id="a8487-110">To fill in and send an intercompany sales order</span></span>
<span data-ttu-id="a8487-111">Du kan sende ordrer, bestillinger og returordrer før bokføring.</span><span class="sxs-lookup"><span data-stu-id="a8487-111">You can send sales and purchase orders and return orders before posting.</span></span> <span data-ttu-id="a8487-112">Fakturaer og kreditnotaer kan ikke sendes før de bokført.</span><span class="sxs-lookup"><span data-stu-id="a8487-112">Invoices and credit memos cannot be sent until they are posted.</span></span>

<span data-ttu-id="a8487-113">Fremgangsmåten nedenfor beskriver hvordan du fyller ut og sender en konsernintern ordre.</span><span class="sxs-lookup"><span data-stu-id="a8487-113">The following procedure describes how to fill in and send an intercompany sales order.</span></span> <span data-ttu-id="a8487-114">Den samme fremgangsmåten gjelder for konserninterne bestillinger og returordrer og for bokførte konserninterne fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="a8487-114">The same steps apply to intercompany purchase orders and return orders, and to posted intercompany invoices and credit memos.</span></span>  

1. <span data-ttu-id="a8487-115">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a8487-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a8487-116">Velg **Ny** for å opprette en ny ordre.</span><span class="sxs-lookup"><span data-stu-id="a8487-116">Choose **New** to create a new sales order.</span></span> <span data-ttu-id="a8487-117">Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="a8487-117">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>  
3. <span data-ttu-id="a8487-118">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a8487-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="a8487-119">Kointroller at kunden er en konsernintern partner.</span><span class="sxs-lookup"><span data-stu-id="a8487-119">Make sure the customer is an intercompany partner.</span></span>
5. <span data-ttu-id="a8487-120">Hvis du vil sende ordren før du bokfører den, kan du velge **Send KI-ordre**.</span><span class="sxs-lookup"><span data-stu-id="a8487-120">To send the sales order before you post it, choose the **Send IC Sales Order** action.</span></span>

> [!NOTE]
> <span data-ttu-id="a8487-121">Hvis du utfører trinn 4, blir ordren flyttet til den konserninterne utboksen der du kan sende den senere.</span><span class="sxs-lookup"><span data-stu-id="a8487-121">If you do perform step 4, then the sales order will be moved to your intercompany outbox where you can send it later.</span></span> <span data-ttu-id="a8487-122">Hvis du vil ha mer informasjon, se [Administrere den konserninterne innboksen og utboksen](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="a8487-122">For more information, see [How to: Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="to-fill-in-and-post-an-intercompany-journal"></a><span data-ttu-id="a8487-123">Slik fyller du ut og bokfører en konsernintern kladd</span><span class="sxs-lookup"><span data-stu-id="a8487-123">To fill in and post an intercompany journal</span></span>
<span data-ttu-id="a8487-124">Når du bokfører en konsernintern kladdelinje i selskapet, opprettes det en tilsvarende kladdelinje i den konserninterne utboksen som du kan overføre til partneren.</span><span class="sxs-lookup"><span data-stu-id="a8487-124">When you post an intercompany general journal line in your company, a corresponding journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="a8487-125">Partneren kan deretter bokføre den tilsvarende transaksjonen i selskapet sitt, uten å måtte registrere dataene på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8487-125">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

1. <span data-ttu-id="a8487-126">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **KI-finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a8487-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IC General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a8487-127">Åpne den relevante kjørselen for kladden.</span><span class="sxs-lookup"><span data-stu-id="a8487-127">Open the relevant journal batch.</span></span> <span data-ttu-id="a8487-128">Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="a8487-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="a8487-129">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a8487-129">Fill in the fields as necessary.</span></span>
4. <span data-ttu-id="a8487-130">I feltet **Finanskontonr. for KI-partner** angir du nummeret til den konserninterne finanskontoen der beløpet skal bokføres i partnerens selskap.</span><span class="sxs-lookup"><span data-stu-id="a8487-130">In the **IC Partner G/L Acc. No.** field, enter the intercompany general ledger account that the amount will be posted to in your partner's company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a8487-131">Dette Feltet må fylles ut på en linje med en bankkonto eller finanskonto i feltet **Kontonr.** eller **Motkontonr.**.</span><span class="sxs-lookup"><span data-stu-id="a8487-131">This field must be filled in on a line with a bank account or general ledger account in either the **Account No.** field or the **Bal. Account No.** field.</span></span>  
5. <span data-ttu-id="a8487-132">Velg handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="a8487-132">Choose the **Post** action.</span></span>

<span data-ttu-id="a8487-133">De involverte postene bokføres i selskapet ditt, og en kladd med tilhørende poster opprettes i den konserninterne utboksen som du kan sende til partnerselskapet.</span><span class="sxs-lookup"><span data-stu-id="a8487-133">The involved entries are posted in your company and a journal with the corresponding entries are created in your intercompany outbox that you can send to your partner company.</span></span> <span data-ttu-id="a8487-134">Hvis du vil ha mer informasjon, se [Administrere den konserninterne innboksen og utboksen](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="a8487-134">For more information, see [How to: Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="a8487-135">Se også</span><span class="sxs-lookup"><span data-stu-id="a8487-135">See Also</span></span>
[<span data-ttu-id="a8487-136">Behandle konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="a8487-136">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="a8487-137">Finans</span><span class="sxs-lookup"><span data-stu-id="a8487-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="a8487-138">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="a8487-138">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="a8487-139">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="a8487-139">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="a8487-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a8487-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

