---
title: Utligne poster i ulike valutaer | Microsoft-dokumentasjon
description: Du kan utligne poster i flere valutaer, for eksempel hvis du selger i én valuta og mottar betaling i en annen.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 846d01c98baabb8744b537292e3d8547cd3886b2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184103"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="aefaa-103">Aktivere utligning av kundeposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="aefaa-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="aefaa-104">Hvis du handler fra en leverandør i én valuta og betaler i en annen valuta, kan du utligne utbetalingen mot kjøpet.</span><span class="sxs-lookup"><span data-stu-id="aefaa-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="aefaa-105">Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du også utligne betalingen mot salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="aefaa-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="aefaa-106">Fremgangsmåten nedenfor beskriver hvordan du definerer dette for leverandørposter på siden **Kjøpsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="aefaa-106">The following procedure describes how to set this up for vendor ledger entries on the **Purchases & Payables Setup** page.</span></span> <span data-ttu-id="aefaa-107">Oppsettet er det samme for kundeposter på siden **Salgsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="aefaa-107">The setup is similar for customer ledger entries on the **Sales & Receivables Setup** page.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="aefaa-108">Aktivere utligning av leverandørposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="aefaa-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="aefaa-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="aefaa-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="aefaa-110">I feltet **Utligning mellom valuta** velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="aefaa-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="aefaa-111">Alternativ</span><span class="sxs-lookup"><span data-stu-id="aefaa-111">Option</span></span> | <span data-ttu-id="aefaa-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="aefaa-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="aefaa-113">Ingen</span><span class="sxs-lookup"><span data-stu-id="aefaa-113">None</span></span> |<span data-ttu-id="aefaa-114">Utligning mellom valutaer er ikke tillatt.</span><span class="sxs-lookup"><span data-stu-id="aefaa-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="aefaa-115">ØMU</span><span class="sxs-lookup"><span data-stu-id="aefaa-115">EMU</span></span> |<span data-ttu-id="aefaa-116">Utligning mellom ØMU-valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="aefaa-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="aefaa-117">Alle</span><span class="sxs-lookup"><span data-stu-id="aefaa-117">All</span></span> |<span data-ttu-id="aefaa-118">Utligning mellom alle valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="aefaa-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="aefaa-119">Slik konfigurerer du finanskonti for avrundingsdifferanser ved valutautligning</span><span class="sxs-lookup"><span data-stu-id="aefaa-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="aefaa-120">Hvis du vil utligne poster i ulike valutaer, må du opprette finanskontoer som du vil bokføre avrundingsdifferanser på.</span><span class="sxs-lookup"><span data-stu-id="aefaa-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="aefaa-121">Du må opprette finanskontoene før du fullfører oppgaven.</span><span class="sxs-lookup"><span data-stu-id="aefaa-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="aefaa-122">Hvis du vil ha mer informasjon, kan du se [Forstå finans og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="aefaa-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="aefaa-123">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper - kunde**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="aefaa-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aefaa-124">Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.</span><span class="sxs-lookup"><span data-stu-id="aefaa-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="aefaa-125">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper – leverandør**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="aefaa-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="aefaa-126">Angi de relevante finanskontiene der avrundingsdifferanser skal bokføres, i feltene **Debetkonto for valutaavrund.** og **Kreditkonto for valutaavrund.**.</span><span class="sxs-lookup"><span data-stu-id="aefaa-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aefaa-127">Se også</span><span class="sxs-lookup"><span data-stu-id="aefaa-127">See Also</span></span>
[<span data-ttu-id="aefaa-128">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="aefaa-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="aefaa-129">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="aefaa-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="aefaa-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aefaa-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
