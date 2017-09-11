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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="a0308-103">Aktivere utligning av kundeposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="a0308-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="a0308-104">Hvis du handler fra en leverandør i én valuta og betaler i en annen valuta, kan du utligne utbetalingen mot kjøpet.</span><span class="sxs-lookup"><span data-stu-id="a0308-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="a0308-105">Hvis du selger til en kunde i én valuta og mottar betaling i en annen valuta, kan du også utligne betalingen mot salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="a0308-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="a0308-106">Fremgangsmåten nedenfor beskriver hvordan du definerer dette for leverandørposter i vinduet **Kjøpsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a0308-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="a0308-107">Oppsettet er det samme for kundeposter i vinduet **Salgsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a0308-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="a0308-108">Denne funksjonen krever at opplevelsen er satt til **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="a0308-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="a0308-109">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="a0308-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="a0308-110">Aktivere utligning av leverandørposter i forskjellige valutaer</span><span class="sxs-lookup"><span data-stu-id="a0308-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="a0308-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a0308-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0308-112">I feltet **Utligning mellom valuta** velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="a0308-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="a0308-113">Alternativ</span><span class="sxs-lookup"><span data-stu-id="a0308-113">Option</span></span> | <span data-ttu-id="a0308-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a0308-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="a0308-115">Ingen</span><span class="sxs-lookup"><span data-stu-id="a0308-115">None</span></span> |<span data-ttu-id="a0308-116">Utligning mellom valutaer er ikke tillatt.</span><span class="sxs-lookup"><span data-stu-id="a0308-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="a0308-117">ØMU</span><span class="sxs-lookup"><span data-stu-id="a0308-117">EMU</span></span> |<span data-ttu-id="a0308-118">Utligning mellom ØMU-valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="a0308-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="a0308-119">Alle</span><span class="sxs-lookup"><span data-stu-id="a0308-119">All</span></span> |<span data-ttu-id="a0308-120">Utligning mellom alle valutaer er tillatt.</span><span class="sxs-lookup"><span data-stu-id="a0308-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a0308-121">Se også</span><span class="sxs-lookup"><span data-stu-id="a0308-121">See Also</span></span>
[<span data-ttu-id="a0308-122">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="a0308-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="a0308-123">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="a0308-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="a0308-124">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0308-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

