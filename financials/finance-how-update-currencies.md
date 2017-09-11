---
title: Oppdatere valutakurser | Microsoft-dokumentasjon
description: Hvis du vil bruke flere valutaer i virksomheten, kan du definere en kode for hver valuta og bruke en ekstern valutakurstjeneste, for eksempel Yahoo.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="d2ba0-103">Oppdatere valutakurser</span><span class="sxs-lookup"><span data-stu-id="d2ba0-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="d2ba0-104">Du må definere en kode for hver valuta du bruker hvis du kjøper eller selger i andre valutaer enn din lokale valuta, har kundekonti eller leverandørkonti i andre valutaer, eller registrerer finanstransaksjoner i forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="d2ba0-105">Denne funksjonen krever at opplevelsen er satt til **Løsning**.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="d2ba0-106">Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="d2ba0-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="d2ba0-107">Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="d2ba0-108">Tjenesten Yahoo-valutakurser er forhåndsinstallert og klar til å aktiveres.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="d2ba0-109">Slik konfigurerer du en valutakurstjeneste</span><span class="sxs-lookup"><span data-stu-id="d2ba0-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="d2ba0-110">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Valutakurstjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2ba0-111">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="d2ba0-112">I vinduet **Valutakurstjeneste** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="d2ba0-113">Merk av for **Aktivert** for å aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="d2ba0-114">Oppdatere valutakurser via en tjeneste</span><span class="sxs-lookup"><span data-stu-id="d2ba0-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="d2ba0-115">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Valutaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="d2ba0-116">Velg **Oppdater valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="d2ba0-117">Verdien i **Valutakurs**-feltet i **Valutaer**-vinduet oppdateres med den nyeste valutakursen.</span><span class="sxs-lookup"><span data-stu-id="d2ba0-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2ba0-118">Se også</span><span class="sxs-lookup"><span data-stu-id="d2ba0-118">See Also</span></span>
[<span data-ttu-id="d2ba0-119">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="d2ba0-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="d2ba0-120">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2ba0-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

