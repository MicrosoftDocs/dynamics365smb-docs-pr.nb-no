---
title: Definere urealisert merverdiavgift | Microsoft-dokumentasjon
description: "Hvis du bruker kontantbasert regnskap, kan du angi hvordan urealisert MVA for salg og innkjøp skal håndteres."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c22e17c931fcb262abe2d2059af89ec6f930ecb5
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a><span data-ttu-id="53d04-103">Definere urealisert merverdiavgift for kontantbasert regnskap</span><span class="sxs-lookup"><span data-stu-id="53d04-103">Set Up Unrealized VAT for Cash-Based Accounting</span></span>
<span data-ttu-id="53d04-104">Hvis du bruker metoder for kontantbasert regnskap, kan du definere [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] for å håndtere urealisert MVA.</span><span class="sxs-lookup"><span data-stu-id="53d04-104">If you're using cash-based accounting methods, you can set up [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] to handle unrealized VAT.</span></span>

## <a name="use-general-ledger-accounts-for-unrealized-vat"></a><span data-ttu-id="53d04-105">Bruke finanskonti for urealisert MVA</span><span class="sxs-lookup"><span data-stu-id="53d04-105">Use general ledger accounts for unrealized VAT</span></span>
<span data-ttu-id="53d04-106">Du kan beregne og bokføre mva-beløp til en midlertidig finanskonto når fakturaen bokføres, og deretter bokføre den til den riktige finanskontoen og inkludere den i mva-oppgaver når den faktiske betalingen av fakturaen bokføres.</span><span class="sxs-lookup"><span data-stu-id="53d04-106">You can choose to have VAT amounts calculated and posted to a temporary general ledger account when an invoice is posted, and then posted to the correct general ledger account and included in VAT statements when the actual payment of the invoice is posted.</span></span> <span data-ttu-id="53d04-107">Før du kan gjøre dette, må du fullføre mva.-bokføringsoppsettet.</span><span class="sxs-lookup"><span data-stu-id="53d04-107">Before you can do this, you must complete the VAT posting setup.</span></span>

<span data-ttu-id="53d04-108">Hvis du vil bruke konti for urealisert MVA, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="53d04-108">To use accounts for unrealized VAT, follow these steps:</span></span>
1. <span data-ttu-id="53d04-109">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), og angi **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="53d04-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, and enter **General Ledger Setup**.</span></span> 
2. <span data-ttu-id="53d04-110">På siden **Finansoppsett** på hurtigfanen **Generelt** velger du **Vis mer** og merker deretter av for **Urealisert MVA**.</span><span class="sxs-lookup"><span data-stu-id="53d04-110">On the **General Ledger Setup** page, on the **General** FastTab, choose **Show More**, and then choose the **Unrealized VAT** check box.</span></span>
3. <span data-ttu-id="53d04-111">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="53d04-111">Close the page.</span></span>
4. <span data-ttu-id="53d04-112">Velg ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), og angir **Mva-bokføringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="53d04-112">choose the **Search for Page or Report** icon ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon"), and enter **VAT Posting Setup**.</span></span> 
5. <span data-ttu-id="53d04-113">På siden **Mva-bokføringsoppsett** velger du Mva-bokføringsgruppen, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="53d04-113">On the **VAT Posting Setup** page, choose the VAT posting group, and then choose **Edit**.</span></span> 
6. <span data-ttu-id="53d04-114">I feltet **Urealisert mva-type** velger du et alternativ for å angi hvordan betalinger skal knyttes til fakturabeløpet (ekskl. mva) og selve mva-beløpet, og hvordan mva-beløp skal overføres fra en urealisert mva-konto til en (realisert) mva-konto.</span><span class="sxs-lookup"><span data-stu-id="53d04-114">In the **Unrealized VAT Type** field, choose an option to specify how to allocate payments to the invoice amount (excluding VAT) and the VAT amount itself, and how to transfer VAT amounts from the unrealized VAT account to the realized account.</span></span> <span data-ttu-id="53d04-115">Tabellen nedenfor beskriver alternativene.</span><span class="sxs-lookup"><span data-stu-id="53d04-115">The following table describes the options.</span></span>

| <span data-ttu-id="53d04-116">Alternativ</span><span class="sxs-lookup"><span data-stu-id="53d04-116">Option</span></span> | <span data-ttu-id="53d04-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="53d04-117">Description</span></span> |
| --- | --- |
| <span data-ttu-id="53d04-118">Tom</span><span class="sxs-lookup"><span data-stu-id="53d04-118">Blank</span></span> | <span data-ttu-id="53d04-119">Velg dette alternativet hvis du ikke vil bruke funksjonen for urealisert MVA.</span><span class="sxs-lookup"><span data-stu-id="53d04-119">Choose this option if you don't want to use the unrealized VAT feature.</span></span> |
| <span data-ttu-id="53d04-120">Prosent</span><span class="sxs-lookup"><span data-stu-id="53d04-120">Percentage</span></span> | <span data-ttu-id="53d04-121">Betalinger dekker både MVA og fakturabeløpet i forhold til prosenten av den totale fakturaen.</span><span class="sxs-lookup"><span data-stu-id="53d04-121">Payments covers both VAT and the invoice amount in proportion to the payment's percentage of the remaining invoice amount.</span></span> <span data-ttu-id="53d04-122">Det betalte MVA-beløpet blir overført fra konto for urealisert MVA til kontoen for realisert MVA.</span><span class="sxs-lookup"><span data-stu-id="53d04-122">The paid VAT amount is transferred from the unrealized VAT account to the realized VAT account.</span></span> |
| <span data-ttu-id="53d04-123">Første</span><span class="sxs-lookup"><span data-stu-id="53d04-123">First</span></span> | <span data-ttu-id="53d04-124">Betalinger dekker mva først og deretter fakturabeløp.</span><span class="sxs-lookup"><span data-stu-id="53d04-124">Payments cover VAT first and then invoice amounts.</span></span> <span data-ttu-id="53d04-125">I dette feltet vil beløpet som er overført fra den urealiserte mva-kontoen til mva-kontoen, være likt betalingsbeløpet til hele mva. er betalt.</span><span class="sxs-lookup"><span data-stu-id="53d04-125">In this case, the amount transferred from the unrealized VAT account to the VAT account will equal the amount of the payment until the total VAT has been paid.</span></span> |
| <span data-ttu-id="53d04-126">Siste</span><span class="sxs-lookup"><span data-stu-id="53d04-126">Last</span></span> | <span data-ttu-id="53d04-127">Betalinger dekker fakturabeløpet først og deretter mva.</span><span class="sxs-lookup"><span data-stu-id="53d04-127">Payments cover the invoice amount first and then VAT.</span></span> <span data-ttu-id="53d04-128">I dette tilfellet blir ingen beløp overført fra kontoen for urealisert mva. til mva-kontoen før det totale fakturabeløpet, eksklusive MVA, er betalt.</span><span class="sxs-lookup"><span data-stu-id="53d04-128">In this case, no amount will be transferred from the unrealized VAT account to the VAT account until the total amount of the invoice, excluding VAT, has been paid.</span></span> |
| <span data-ttu-id="53d04-129">Først (fullt betalt)</span><span class="sxs-lookup"><span data-stu-id="53d04-129">First (Fully Paid)</span></span> | <span data-ttu-id="53d04-130">Betalinger dekker MVA først (som alternativet _Først_), men ingen beløp vil bli overført til MVA-kontoen før hele MVA-beløpet er betalt.</span><span class="sxs-lookup"><span data-stu-id="53d04-130">Payments will cover VAT first (like the _First_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |
| <span data-ttu-id="53d04-131">Siste (fullt betalt)</span><span class="sxs-lookup"><span data-stu-id="53d04-131">Last (Fully Paid)</span></span> | <span data-ttu-id="53d04-132">Betalinger dekker først fakturabeløpet (som alternativet _Siste_), men ingen beløp vil bli overført til MVA-kontoen før hele MVA-beløpet er betalt.</span><span class="sxs-lookup"><span data-stu-id="53d04-132">Payments will cover invoice amount first (like the _Last_ option), but no amount will be transferred to the VAT account until the full amount of VAT has been paid.</span></span> |

6. <span data-ttu-id="53d04-133">I feltet **Konto for ureal. utgående mva.** velger du kontoen for urealisert utgående mva.</span><span class="sxs-lookup"><span data-stu-id="53d04-133">In the **Sales VAT Unreal. Account** field, choose the account for unrealized sales VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="53d04-134">Mva-beløpet bokføres på denne kontoen, der det blir værende til kundens betaling er bokført.</span><span class="sxs-lookup"><span data-stu-id="53d04-134">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="53d04-135">Beløpet overføres deretter til finanskontoen for utgående mva.</span><span class="sxs-lookup"><span data-stu-id="53d04-135">The amount is then transferred to the account for sales VAT.</span></span>
7. <span data-ttu-id="53d04-136">I feltet **Konto for ureal. inngående mva.** angir du finanskontoen for urealisert inngående mva.</span><span class="sxs-lookup"><span data-stu-id="53d04-136">In the **Purch. VAT Unreal. Account** field, enter the general ledger count for unrealized purchase VAT.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="53d04-137">Mva-beløpet bokføres på denne kontoen, der det blir værende til kundens betaling er bokført.</span><span class="sxs-lookup"><span data-stu-id="53d04-137">The VAT amount will be posted to this account, and stay there until the customer payment is posted.</span></span> <span data-ttu-id="53d04-138">Beløpet overføres deretter til finanskontoen for utgående mva.</span><span class="sxs-lookup"><span data-stu-id="53d04-138">The amount is then transferred to the account for sales VAT.</span></span>

## <a name="see-also"></a><span data-ttu-id="53d04-139">Se også</span><span class="sxs-lookup"><span data-stu-id="53d04-139">See Also</span></span>
[<span data-ttu-id="53d04-140">Definere merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="53d04-140">Setting Up Value Added Tax</span></span>](finance-setup-vat.md)
