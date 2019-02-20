---
title: Oppdatere valutakurser | Microsoft-dokumentasjon
description: Hvis du vil bruke flere valutaer i virksomheten, kan du definere en kode for hver valuta og bruke en ekstern valutakurstjeneste.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: nb-no
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="baebf-103">Oppdatere valutakurser</span><span class="sxs-lookup"><span data-stu-id="baebf-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="baebf-104">Ettersom selskaper har drift i stadig flere land/regioner, blir det også stadig viktigere at de kan handle i og rapportere økonomien i mer enn én valuta.</span><span class="sxs-lookup"><span data-stu-id="baebf-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="baebf-105">Du må definere en kode for hver valuta du bruker hvis du kjøper eller selger i andre valutaer enn din lokale valuta, har kundekonti eller leverandørkonti i andre valutaer, eller registrerer finanstransaksjoner i forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="baebf-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="baebf-106">Finans er definert til å bruke den lokale valutaen (NOK), men du kan definere at den skal bruke en annen valuta med en gjeldende valutakurs.</span><span class="sxs-lookup"><span data-stu-id="baebf-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="baebf-107">Når du angir en ny valuta som en såkalt tilleggsrapporteringsvaluta, registrerer [!INCLUDE[d365fin](includes/d365fin_md.md)] beløp automatisk i både NOK og denne tilleggsrapporteringsvalutaen i alle finansposter og andre poster, for eksempel mva-poster.</span><span class="sxs-lookup"><span data-stu-id="baebf-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="baebf-108">Hvis du vil ha mer informasjon, se [Sette opp en tilleggsrapporteringsvaluta](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="baebf-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="baebf-109">Justere valutakurser</span><span class="sxs-lookup"><span data-stu-id="baebf-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="baebf-110">Ettersom valutakursene varierer konstant, må tilleggsvalutaangivelser i systemet justeres jevnlig.</span><span class="sxs-lookup"><span data-stu-id="baebf-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="baebf-111">Hvis disse justeringene ikke utføres, kan beløp som er regnet om fra utenlandske valutaer (eller tilleggsvalutaer) og bokført i NOK i Finans, være villedende.</span><span class="sxs-lookup"><span data-stu-id="baebf-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="baebf-112">I tillegg må daglige poster som bokføres før en daglig valutakurs angis i programmet, oppdateres etter at informasjonen om den daglige valutakursen er angitt.</span><span class="sxs-lookup"><span data-stu-id="baebf-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="baebf-113">Kjørselen Juster valutakurser brukes til å justere valutakursene for bokførte kunde-, leverandør- og bankkontoposter.</span><span class="sxs-lookup"><span data-stu-id="baebf-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="baebf-114">Den kan også oppdatere tilleggsrapporteringsvalutabeløp i finansposter.</span><span class="sxs-lookup"><span data-stu-id="baebf-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="baebf-115">Slik konfigurerer du en valutakurstjeneste</span><span class="sxs-lookup"><span data-stu-id="baebf-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="baebf-116">Du kan bruke en ekstern tjeneste for å holde valutakurser oppdatert, for eksempel FloatRates.</span><span class="sxs-lookup"><span data-stu-id="baebf-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="baebf-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutakurstjenester**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="baebf-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="baebf-118">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="baebf-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="baebf-119">På siden **Valutakurstjeneste** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="baebf-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="baebf-120">Merk av for **Aktivert** for å aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="baebf-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="baebf-121">Oppdatere valutakurser via en tjeneste</span><span class="sxs-lookup"><span data-stu-id="baebf-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="baebf-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Valutaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="baebf-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="baebf-123">Velg **Oppdater valutakurser**.</span><span class="sxs-lookup"><span data-stu-id="baebf-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="baebf-124">Verdien i **Valutakurs**-feltet på **Valutaer**-siden oppdateres med den nyeste valutakursen.</span><span class="sxs-lookup"><span data-stu-id="baebf-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="baebf-125">Se også</span><span class="sxs-lookup"><span data-stu-id="baebf-125">See Also</span></span>
[<span data-ttu-id="baebf-126">Definere en tilleggsrapporteringsvaluta</span><span class="sxs-lookup"><span data-stu-id="baebf-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="baebf-127">Avslutte år og perioder</span><span class="sxs-lookup"><span data-stu-id="baebf-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="baebf-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="baebf-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

