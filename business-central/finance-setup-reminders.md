---
title: Definer betingelser og grader for purringer
description: Finn ut hvordan du konfigurerer Business Central slik at du kan sende en påminnelse til en kunde om en betaling som er forfalt, og legge gebyrer til betalingen på grunn av forsinkelsen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 06853911f5b2858fbde4ff5371971c86f2960543
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783487"
---
# <a name="set-up-reminder-terms-and-levels"></a><span data-ttu-id="fb3bb-103">Definer betingelser og grader for purringer</span><span class="sxs-lookup"><span data-stu-id="fb3bb-103">Set Up Reminder Terms and Levels</span></span>

<span data-ttu-id="fb3bb-104">Du kan bruke purringer til å minne kunder på forfalte beløp.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-104">You can use reminders to remind customers about overdue amounts.</span></span> [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a><span data-ttu-id="fb3bb-105">Purrebetingelser</span><span class="sxs-lookup"><span data-stu-id="fb3bb-105">Reminder terms</span></span>

<span data-ttu-id="fb3bb-106">Hvis kunder har forfalte betalinger, må du angi når og hvordan du vil sende purring.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-106">If customers have overdue payments, you must decide when and how to send them a reminder.</span></span> <span data-ttu-id="fb3bb-107">I tillegg vil du kanskje belaste kundekontiene med renter eller gebyr.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-107">In addition, you may want to debit their accounts for interest or fees.</span></span> <span data-ttu-id="fb3bb-108">Du kan opprette så mange purrebetingelser du vil.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-108">You can set up any number of reminder terms.</span></span>  

> [!NOTE]
> <span data-ttu-id="fb3bb-109">Hvis du vil beregne rente på forfalte betalinger, kan du gjøre det når du oppretter purringer.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-109">If you want to calculate interest on overdue payments, you can do so when you create reminders.</span></span> <span data-ttu-id="fb3bb-110">Hvis du imidlertid bare vil beregne rente og informere kundene om dette uten å sende purringer, bør du bruke [rentenotaer](finance-setup-finance-charges.md).</span><span class="sxs-lookup"><span data-stu-id="fb3bb-110">If, however, you just want to calculate interest and inform your customers about this without sending reminders, you should use [finance charge memos](finance-setup-finance-charges.md).</span></span> <span data-ttu-id="fb3bb-111">Du finner mer informasjon under [Purringer](receivables-collect-outstanding-balances.md#reminders) eller [Rentenotaer](receivables-collect-outstanding-balances.md#finance-charges).</span><span class="sxs-lookup"><span data-stu-id="fb3bb-111">For more information, see [Reminders](receivables-collect-outstanding-balances.md#reminders) or [Finance Charges](receivables-collect-outstanding-balances.md#finance-charges), respectively.</span></span>

### <a name="to-set-up-reminder-terms"></a><span data-ttu-id="fb3bb-112">Slik definerer du purrebetingelser</span><span class="sxs-lookup"><span data-stu-id="fb3bb-112">To set up reminder terms</span></span>

1. <span data-ttu-id="fb3bb-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purrebetingelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fb3bb-114">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-114">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="fb3bb-115">Hvis du vil bruke flere kombinasjoner av purrebetingelser, definerer du en kode for hver kombinasjon.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-115">To use more than one combination of reminder terms, set up a code for each one.</span></span>

## <a name="reminder-levels"></a><span data-ttu-id="fb3bb-116">Purregrader</span><span class="sxs-lookup"><span data-stu-id="fb3bb-116">Reminder levels</span></span>

<span data-ttu-id="fb3bb-117">For hver purrebetingelseskode kan du definere et ubegrenset antall purregrader.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-117">For each reminder terms code, you can define an unlimited number of reminder levels.</span></span> <span data-ttu-id="fb3bb-118">Innstillingen fra grad 1 brukes første gang det opprettes en purring for en kunde.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-118">The first time a reminder is created for a customer, the setting from level 1 is used.</span></span> <span data-ttu-id="fb3bb-119">Når purringen utstedes, registreres gradnummeret i purrepostene som opprettes og kobles til de individuelle kundepostene.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-119">When the reminder is issued, the level number is registered on the reminder entries that are created and linked to the individual customer ledger entries.</span></span> <span data-ttu-id="fb3bb-120">Hvis det er nødvendig å sende kunden en ny purring, kontrolleres alle purreposter som er koblet til åpne kundeposter, for å finne det høyeste gradnummeret.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-120">If it is necessary to remind the customer again, all reminder entries linked to open customer ledger entries are checked to locate the highest level number.</span></span> <span data-ttu-id="fb3bb-121">Betingelsene fra neste gradnummer vil deretter bli brukt i den nye purringen.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-121">The conditions from the next level number will then be used for the new reminder.</span></span>

<span data-ttu-id="fb3bb-122">Hvis du oppretter flere purringer enn du har definert grader for, brukes betingelsene for den høyeste graden.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-122">If you create more reminders than you have defined levels for, the conditions for the highest level will be used.</span></span> <span data-ttu-id="fb3bb-123">Du kan opprette så mange purringer som er tillatt i henhold til feltet **Høyeste purregrad** i purrebetingelsene.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-123">You can create as many reminders as are allowed by the **Max. No of Reminders** field in the reminder terms.</span></span>

### <a name="to-set-up-reminder-levels"></a><span data-ttu-id="fb3bb-124">Slik definerer du purregrader</span><span class="sxs-lookup"><span data-stu-id="fb3bb-124">To set up reminder levels</span></span>

1. <span data-ttu-id="fb3bb-125">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purrebetingelser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="fb3bb-126">På siden **Purrebetingelser** velger du linjen med betingelsene du vil definere grader for, og deretter velger du **Grader**.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-126">On the **Reminder Terms** page, select the line with the terms you want to set up levels for, and then choose **Levels** action.</span></span>  
3. <span data-ttu-id="fb3bb-127">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-127">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > <span data-ttu-id="fb3bb-128">Innstillingen for feltet **Beregn renter** bestemmer om renter skal vises på purringen når purringen utstedes.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-128">The setting of the **Calculate Interest** field determines if interest will appear on the reminder when the reminder is issued.</span></span> <span data-ttu-id="fb3bb-129">Feltet **Bokfør rente** på siden **Purrebetingelsene** bestemmer imidlertid om den beregnede renten skal bokføres til finans- og kundekonti.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-129">However, the **Post Interest** field in the **Reminder Terms** page determines if the calculated interest must be posted to G/L and customer accounts.</span></span>
    >
    > <span data-ttu-id="fb3bb-130">Hvis du vil angi at renter skal beregnes, velger du feletet **Beregn renter**.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-130">To indicate that interest should be calculated, choose the **Calculate Interest** field.</span></span>

    <span data-ttu-id="fb3bb-131">For hver purregrad kan du også angi tilleggsgebyr både i NOK og i utenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-131">Optionally, for each reminder level, specify additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="fb3bb-132">Du kan definere mange tilleggsgebyr i fremmed valuta for hver kode på siden **Purregrad**.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-132">You can define many additional fees in foreign currencies for each code on the **Reminder Levels** page.</span></span>  

    <span data-ttu-id="fb3bb-133">Tilleggsgebyrene kan beregnes på tre ulike måter, som er definert av verdien i feltet **Tilleggsgebyr beregningstype**.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-133">The additional fees can be calculated in three different ways that are defined by the value of the **Add. Fee Calculation Type** field.</span></span>  

    - <span data-ttu-id="fb3bb-134">**Fast**</span><span class="sxs-lookup"><span data-stu-id="fb3bb-134">**Fixed**</span></span>

        <span data-ttu-id="fb3bb-135">Gebyr beregnes basert på verdiene i feltene **Tilleggsgebyr** på linjen for selve purregraden.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-135">Fees are calculated based on the values of the **Additional Fee** fields on the line for the reminder level itself.</span></span>  
    - <span data-ttu-id="fb3bb-136">**Enkel dynamisk**</span><span class="sxs-lookup"><span data-stu-id="fb3bb-136">**Single Dynamic**</span></span>

        <span data-ttu-id="fb3bb-137">Gebyr beregnes basert på verdiene i feltene på den relevante linjen på siden **Oppsett av tilleggsgebyr** for purregraden.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-137">Fees are calculated based on the values of the fields on the relevant line in the **Additional Fee Setup** page for that reminder level.</span></span>
    - <span data-ttu-id="fb3bb-138">**Akkumulert dynamisk**</span><span class="sxs-lookup"><span data-stu-id="fb3bb-138">**Accumulated Dynamic**</span></span>

        <span data-ttu-id="fb3bb-139">Gebyr beregnes basert på verdiene i feltene på de kombinerte linjene på siden **Oppsett av tilleggsgebyr** for purregraden.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-139">Fees are calculated based on the values of the fields on the combined lines in the **Additional Fee Setup** page for that reminder level.</span></span>

4. <span data-ttu-id="fb3bb-140">Velg handlingen **Valutaer**.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-140">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="fb3bb-141">På siden **Valutaer for purregrad** definerer du en valutakode og et tilleggsgebyr for hver purregradskode og tilhørende purregradsnummer.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-141">On the **Currencies for Reminder Levels** page, define for each reminder level code and corresponding reminder level number a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="fb3bb-142">Når du oppretter purringer i en fremmed valuta, brukes betingelsene for den fremmede valutaen du definerer her, til å opprette purringer.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-142">When you create reminders in a foreign currency, the foreign currency conditions that you set up here will be used to create reminders.</span></span> <span data-ttu-id="fb3bb-143">Hvis det ikke er definert noen betingelser for purringer i fremmed valuta, brukes purrebetingelsene for NOK som er definert på siden **Purregrader**, og deretter konverteres de til den relevante valutaen.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-143">If there are no foreign currency reminder conditions set up, the LCY reminder conditions that are set up on the **Reminder Levels** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="fb3bb-144">For hver purregrad kan du spesifisere tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i purringen.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-144">For each reminder level, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the reminder.</span></span>

6. <span data-ttu-id="fb3bb-145">Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut **Purretekst**-siden.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-145">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill in the **Reminder Text** page.</span></span>
7. <span data-ttu-id="fb3bb-146">Hvis du vil sette inn beslektede verdier automatisk i den resulterende purreteksten, angir du plassholderne nedenfor i **Tekst** feltet.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-146">To automatically insert related values in the resulting reminder text, enter the following placeholders in the **Text** field .</span></span>  

    |<span data-ttu-id="fb3bb-147">Plassholder</span><span class="sxs-lookup"><span data-stu-id="fb3bb-147">Placeholder</span></span>|<span data-ttu-id="fb3bb-148">Verdi</span><span class="sxs-lookup"><span data-stu-id="fb3bb-148">Value</span></span>|  
    |-----------------|-----------|  
    |<span data-ttu-id="fb3bb-149">%1</span><span class="sxs-lookup"><span data-stu-id="fb3bb-149">%1</span></span>|<span data-ttu-id="fb3bb-150">Innholdet i **Bilagsdato**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-150">Content of the **Document Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-151">%2</span><span class="sxs-lookup"><span data-stu-id="fb3bb-151">%2</span></span>|<span data-ttu-id="fb3bb-152">Innholdet i **Forfallsdato**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-152">Content of the **Due Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-153">%3</span><span class="sxs-lookup"><span data-stu-id="fb3bb-153">%3</span></span>|<span data-ttu-id="fb3bb-154">Innholdet i feltet **Rentesats** på de relaterte rentenotabetingelsene</span><span class="sxs-lookup"><span data-stu-id="fb3bb-154">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
    |<span data-ttu-id="fb3bb-155">%4</span><span class="sxs-lookup"><span data-stu-id="fb3bb-155">%4</span></span>|<span data-ttu-id="fb3bb-156">Innholdet i **Restbeløp**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-156">Content of the **Remaining Amount** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-157">%5</span><span class="sxs-lookup"><span data-stu-id="fb3bb-157">%5</span></span>|<span data-ttu-id="fb3bb-158">Innholdet i **Rentebeløp**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-158">Content of the **Interest Amount** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-159">%6</span><span class="sxs-lookup"><span data-stu-id="fb3bb-159">%6</span></span>|<span data-ttu-id="fb3bb-160">Innholdet i **Tilleggsgebyr**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-160">Content of the **Additional Fee** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-161">%7</span><span class="sxs-lookup"><span data-stu-id="fb3bb-161">%7</span></span>|<span data-ttu-id="fb3bb-162">Purringens totalbeløp.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-162">The total amount of the reminder</span></span>|  
    |<span data-ttu-id="fb3bb-163">%8</span><span class="sxs-lookup"><span data-stu-id="fb3bb-163">%8</span></span>|<span data-ttu-id="fb3bb-164">Innholdet i **Purregrad**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-164">Content of the **Reminder Level** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-165">%9</span><span class="sxs-lookup"><span data-stu-id="fb3bb-165">%9</span></span>|<span data-ttu-id="fb3bb-166">Innholdet i **Valutakode**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-166">Content of the **Currency Code** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-167">%10</span><span class="sxs-lookup"><span data-stu-id="fb3bb-167">%10</span></span>|<span data-ttu-id="fb3bb-168">Innholdet i **Bokføringsdato**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-168">Content of the **Posting Date** field on the reminder header</span></span>|  
    |<span data-ttu-id="fb3bb-169">%11</span><span class="sxs-lookup"><span data-stu-id="fb3bb-169">%11</span></span>|<span data-ttu-id="fb3bb-170">Selskapsnavnet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-170">The company name</span></span>|  
    |<span data-ttu-id="fb3bb-171">%12</span><span class="sxs-lookup"><span data-stu-id="fb3bb-171">%12</span></span>|<span data-ttu-id="fb3bb-172">Innholdet i **Tilleggsgebyr per linje**-feltet i purrehodet</span><span class="sxs-lookup"><span data-stu-id="fb3bb-172">Content of the **Add. Fee per Line** field on the reminder header</span></span>|  

    <span data-ttu-id="fb3bb-173">Hvis du for eksempel skriver **Du skylder %9 %7, som forfaller den %2.**, vil den resulterende påminnelsen inneholde følgende tekst: **Du skylder 1 200,50 NOK, som forfaller 02-02-2014.**</span><span class="sxs-lookup"><span data-stu-id="fb3bb-173">For example, if you write **You owe %9 %7 due on %2.**, then the resulting reminder will contain the following text: **You owe USD 1.200,50 due on 02-02-2014.**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb3bb-174">Forfallsdatoen beregnes i henhold til datoformelen som du angir.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-174">The due date is calculated according to the date formula that you enter.</span></span> <span data-ttu-id="fb3bb-175">Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).</span><span class="sxs-lookup"><span data-stu-id="fb3bb-175">For more information, see [Using Date Formulas](ui-enter-date-ranges.md#using-date-formulas).</span></span>

<span data-ttu-id="fb3bb-176">Når du har definert purrebetingelsene (med tilleggsgrader og tekst), registrerer du én av kodene på hvert kundekort.</span><span class="sxs-lookup"><span data-stu-id="fb3bb-176">After you have set up the reminder terms, with additional levels and text, enter one of the codes on each of the customer cards.</span></span> <span data-ttu-id="fb3bb-177">Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="fb3bb-177">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb3bb-178">Se også</span><span class="sxs-lookup"><span data-stu-id="fb3bb-178">See also</span></span>

[<span data-ttu-id="fb3bb-179">Innkreve utestående saldi</span><span class="sxs-lookup"><span data-stu-id="fb3bb-179">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="fb3bb-180">Definer rentenotabetingelser</span><span class="sxs-lookup"><span data-stu-id="fb3bb-180">Set Up Finance Charge Terms</span></span>](finance-setup-finance-charges.md)  
[<span data-ttu-id="fb3bb-181">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="fb3bb-181">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]