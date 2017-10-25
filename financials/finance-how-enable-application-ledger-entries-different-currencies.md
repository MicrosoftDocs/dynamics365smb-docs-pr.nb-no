---
title: Utligne poster i ulike valutaer | Microsoft-dokumentasjon
description: "Du kan utligne poster i flere valutaer, for eksempel hvis du selger i én valuta og mottar betaling i en annen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="30c89-103">Aktivere utligning av kundeposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="30c89-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="30c89-104">Hvis du handler fra en leverandør i én valuta og betaler i en annen valuta, kan du utligne utbetalingen mot kjøpet.</span><span class="sxs-lookup"><span data-stu-id="30c89-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="30c89-105">Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du også utligne betalingen mot salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="30c89-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="30c89-106">Fremgangsmåten nedenfor beskriver hvordan du definerer dette for leverandørposter i vinduet **Kjøpsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="30c89-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="30c89-107">Oppsettet er det samme for kundeposter i vinduet **Salgsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="30c89-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="30c89-108">Denne funksjonen krever at opplevelsen er satt til **Suite**.</span><span class="sxs-lookup"><span data-stu-id="30c89-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="30c89-109">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="30c89-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="30c89-110">Aktivere utligning av leverandørposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="30c89-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="30c89-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="30c89-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="30c89-112">I feltet **Utligning mellom valuta** velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="30c89-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="30c89-113">Alternativ</span><span class="sxs-lookup"><span data-stu-id="30c89-113">Option</span></span> | <span data-ttu-id="30c89-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="30c89-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="30c89-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="30c89-115">None</span></span> |<span data-ttu-id="30c89-116">Utligning mellom valutaer er ikke tillatt.</span><span class="sxs-lookup"><span data-stu-id="30c89-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="30c89-117">ØMU</span><span class="sxs-lookup"><span data-stu-id="30c89-117">EMU</span></span> |<span data-ttu-id="30c89-118">Utligning mellom ØMU-valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="30c89-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="30c89-119">Alle</span><span class="sxs-lookup"><span data-stu-id="30c89-119">All</span></span> |<span data-ttu-id="30c89-120">Utligning mellom alle valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="30c89-120">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="30c89-121">Slik konfigurerer du finanskonti for avrundingsdifferanser ved valutautligning</span><span class="sxs-lookup"><span data-stu-id="30c89-121">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="30c89-122">Hvis du vil utligne poster i ulike valutaer, må du opprette finanskontoer som du vil bokføre avrundingsdifferanser på.</span><span class="sxs-lookup"><span data-stu-id="30c89-122">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="30c89-123">Du må opprette finanskontoene før du fullfører oppgaven.</span><span class="sxs-lookup"><span data-stu-id="30c89-123">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="30c89-124">Hvis du vil ha mer informasjon, kan du se [Forstå finans og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="30c89-124">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span> 
  
1. <span data-ttu-id="30c89-125">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokføringsgrupper - kunde**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="30c89-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="30c89-126">Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.</span><span class="sxs-lookup"><span data-stu-id="30c89-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="30c89-127">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokføringsgrupper - leverandør**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="30c89-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="30c89-128">Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.</span><span class="sxs-lookup"><span data-stu-id="30c89-128">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="30c89-129">Se også</span><span class="sxs-lookup"><span data-stu-id="30c89-129">See Also</span></span>
[<span data-ttu-id="30c89-130">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="30c89-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="30c89-131">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="30c89-131">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="30c89-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="30c89-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

