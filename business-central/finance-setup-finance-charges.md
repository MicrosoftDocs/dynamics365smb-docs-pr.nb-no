---
title: Definer rentenotabetingelser
description: Finn ut hvordan du konfigurerer Business Central slik at du kan informere kunder om tilleggsgebyrer ved å sende rentenotaer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08a2443f94efbc9920145109b4b7499a3a4e05b3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783625"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="c13c7-103">Definer rentenotabetingelser</span><span class="sxs-lookup"><span data-stu-id="c13c7-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="c13c7-104">Når en kunde ikke betaler innen forfallsdatoen, kan du beregne renter automatisk og legge dem til de forfalte beløpene på kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="c13c7-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="c13c7-105">Du kan informere kunder om tilleggsgebyr ved å sende rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="c13c7-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="c13c7-106">Du må først definere en kode som representerer de ulike måtene du vil at programmet skal beregne renter på.</span><span class="sxs-lookup"><span data-stu-id="c13c7-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="c13c7-107">Deretter kan du angi denne koden i feltet Kode for rentenotabetingelser på kundekort.</span><span class="sxs-lookup"><span data-stu-id="c13c7-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="c13c7-108">Rentenotabetingelser</span><span class="sxs-lookup"><span data-stu-id="c13c7-108">Finance charge terms</span></span>

<span data-ttu-id="c13c7-109">Du må definere rentenotabetingelser for hver rentenotaberegning og deretter tilordne betingelsene til kunden i feltet **Kode for rentenotabetingelser** på siden **Kunde**.</span><span class="sxs-lookup"><span data-stu-id="c13c7-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="c13c7-110">Renter kan beregnes ved hjelp av enten gjennomsnittlig dagssaldo eller forfalt beløp.</span><span class="sxs-lookup"><span data-stu-id="c13c7-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="c13c7-111">Gjennomsnitt daglig saldo</span><span class="sxs-lookup"><span data-stu-id="c13c7-111">Average daily balance</span></span>  
  
  <span data-ttu-id="c13c7-112">Det er tatt hensyn til hvor mange dager betalingen er forsinketl:</span><span class="sxs-lookup"><span data-stu-id="c13c7-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="c13c7-113">*Metoden Gjennomsnittlig daglig saldo* - *Rente* = *Forfalt beløp* x *(Dager forfalt / Renteperiode)* x *(Rentesats / 100)*</span><span class="sxs-lookup"><span data-stu-id="c13c7-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="c13c7-114">Forfalt saldo</span><span class="sxs-lookup"><span data-stu-id="c13c7-114">Balance due</span></span>  
  
  <span data-ttu-id="c13c7-115">Rentegebyret er en prosent av forfalt beløp:</span><span class="sxs-lookup"><span data-stu-id="c13c7-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="c13c7-116">*Forfalt saldo-metode* - *Rente* = *Forfalt beløp* x *(Rentesats / 100)*</span><span class="sxs-lookup"><span data-stu-id="c13c7-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="c13c7-117">I tillegg er hver betingelse i tabellen Rentenotatekst knyttet til en undertabell, tabellen Rentenotatekst.</span><span class="sxs-lookup"><span data-stu-id="c13c7-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="c13c7-118">For hver rentebetingelse kan du definere en start- og/eller sluttekst som kommer ut på rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="c13c7-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="c13c7-119">Definere rentenotabetingelser</span><span class="sxs-lookup"><span data-stu-id="c13c7-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="c13c7-120">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotabetingelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c13c7-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c13c7-121">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="c13c7-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="c13c7-122">Hvis du vil bruke flere kombinasjoner av rentebetingelser, definerer du en kode for hver kombinasjon.</span><span class="sxs-lookup"><span data-stu-id="c13c7-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="c13c7-123">For hver rentebetingelse kan du spesifisere individuelle betingelser, som kan inkludere tilleggsgebyrer både i NOK og i utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="c13c7-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="c13c7-124">Du kan definere tilleggsgebyrer i fremmed valuta for hver betingelse på siden **Rentenotabetingelser**.</span><span class="sxs-lookup"><span data-stu-id="c13c7-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="c13c7-125">Velg handlingen **Valutaer**.</span><span class="sxs-lookup"><span data-stu-id="c13c7-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="c13c7-126">På siden **Valuta for rentenotabeting.** definerer du en valutakode og et tilleggsgebyr for hver betingelse.</span><span class="sxs-lookup"><span data-stu-id="c13c7-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="c13c7-127">Når du oppretter renter i en utenlandsk valuta, brukes betingelsene for utenlandsk valuta du definerer her, til å opprette rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="c13c7-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="c13c7-128">Hvis det ikke er definert noen betingelser for rentenotaer i utenlandsk valuta, brukes rentenotabetingelsene for NOK som er spesifisert på siden **Rentenotabetingelser**, og deretter konverteres de til den relevante valutaen.</span><span class="sxs-lookup"><span data-stu-id="c13c7-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="c13c7-129">For hver rentenotabetingelse kan du angi tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="c13c7-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="c13c7-130">Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut siden **Rentenotatekst**.</span><span class="sxs-lookup"><span data-stu-id="c13c7-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="c13c7-131">Hvis du vil sette inn relaterte verdier automatisk i den resulterende rentenotateksten, angir du plassholderne nedenfor i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c13c7-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="c13c7-132">Plassholder</span><span class="sxs-lookup"><span data-stu-id="c13c7-132">Placeholder</span></span>|<span data-ttu-id="c13c7-133">Verdi</span><span class="sxs-lookup"><span data-stu-id="c13c7-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="c13c7-134">%1</span><span class="sxs-lookup"><span data-stu-id="c13c7-134">%1</span></span>|<span data-ttu-id="c13c7-135">Innholdet i **Bilagsdato**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-136">%2</span><span class="sxs-lookup"><span data-stu-id="c13c7-136">%2</span></span>|<span data-ttu-id="c13c7-137">Innholdet i **Forfallsdato**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-138">%3</span><span class="sxs-lookup"><span data-stu-id="c13c7-138">%3</span></span>|<span data-ttu-id="c13c7-139">Innholdet i feltet **Rentesats** på de relaterte rentenotabetingelsene</span><span class="sxs-lookup"><span data-stu-id="c13c7-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="c13c7-140">%4</span><span class="sxs-lookup"><span data-stu-id="c13c7-140">%4</span></span>|<span data-ttu-id="c13c7-141">Innholdet i **Restbeløp**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-142">%5</span><span class="sxs-lookup"><span data-stu-id="c13c7-142">%5</span></span>|<span data-ttu-id="c13c7-143">Innholdet i **Rentebeløp**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-144">%6</span><span class="sxs-lookup"><span data-stu-id="c13c7-144">%6</span></span>|<span data-ttu-id="c13c7-145">Innholdet i **Tilleggsgebyr**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-146">%7</span><span class="sxs-lookup"><span data-stu-id="c13c7-146">%7</span></span>|<span data-ttu-id="c13c7-147">Purringens totalbeløp</span><span class="sxs-lookup"><span data-stu-id="c13c7-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="c13c7-148">%8</span><span class="sxs-lookup"><span data-stu-id="c13c7-148">%8</span></span>|<span data-ttu-id="c13c7-149">Innholdet i **Valutakode**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="c13c7-150">%9</span><span class="sxs-lookup"><span data-stu-id="c13c7-150">%9</span></span>|<span data-ttu-id="c13c7-151">Innholdet i **Bokføringsdato**-feltet i rentenotahodet</span><span class="sxs-lookup"><span data-stu-id="c13c7-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="c13c7-152">Se også</span><span class="sxs-lookup"><span data-stu-id="c13c7-152">See also</span></span>

[<span data-ttu-id="c13c7-153">Innkreve utestående saldi</span><span class="sxs-lookup"><span data-stu-id="c13c7-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="c13c7-154">Definer betingelser og grader for purringer</span><span class="sxs-lookup"><span data-stu-id="c13c7-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="c13c7-155">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="c13c7-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]