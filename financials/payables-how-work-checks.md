---
title: Utstede, skrive ut og kansellere sjekker | Microsoft-dokumentasjon
description: Beskriver hvordan du utsteder sjekker ved hjelp av utbetalingskladden, skriver ut sjekker og kansellerer eller viser sjekkposter i Financials.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0875164a3afee7a835346a8d4b9323dda9ebf080
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-checks"></a><span data-ttu-id="52eec-103">Arbeide med sjekker</span><span class="sxs-lookup"><span data-stu-id="52eec-103">How to: Work With Checks</span></span>
<span data-ttu-id="52eec-104">Du kan utstede elektroniske og manuelle sjekker i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="52eec-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="52eec-105">Begge metodene bruker utbetalingskladden til å utstede sjekker til leverandører.</span><span class="sxs-lookup"><span data-stu-id="52eec-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="52eec-106">Du kan også kansellere sjekker og vise sjekkposter.</span><span class="sxs-lookup"><span data-stu-id="52eec-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="52eec-107">Prosessen med å utstede sjekker foreslår utbetalinger, oppretter poster og skriver ut de maskinelle sjekkene.</span><span class="sxs-lookup"><span data-stu-id="52eec-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="52eec-108">For å være sikker på at banken bare innfrir validerte sjekker og beløp, kan du sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling.</span><span class="sxs-lookup"><span data-stu-id="52eec-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="52eec-109">Hvis du vil ha mer informasjon, kan du se [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="52eec-109">For more information, see [How to: Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="52eec-110">Skriveren må være riktig konfigurert for sjekkskjemaene, og du må definere hvilke sjekkoppsett som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="52eec-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="52eec-111">Hvis du vil ha mer informasjon, kan du se [Definere sjekkoppsett](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="52eec-111">For more information, see [How to: Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="52eec-112">Utstede sjekker</span><span class="sxs-lookup"><span data-stu-id="52eec-112">To issue checks</span></span>
1. <span data-ttu-id="52eec-113">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52eec-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="52eec-114">Fyll ut kladden med relevante betalinger, for eksempel ved hjelp av funksjonen Betalingsforslag - leverandør.</span><span class="sxs-lookup"><span data-stu-id="52eec-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="52eec-115">Hvis du vil ha mer informasjon, kan du se [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="52eec-115">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="52eec-116">I **Bankbetalingstype**-feltet på kladdelinjer for betaling som du vil gjøre med sjekker, velger du ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="52eec-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="52eec-117">**Maskinell sjekk**: Velg dette alternativet hvis du vil at programmet skal opprette og senere skrive ut en sjekk på beløpet på betalingskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="52eec-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="52eec-118">Du må skrive ut sjekkene før du kan bokføre kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="52eec-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="52eec-119">Du kan bare velge **Maskinell sjekk** hvis **Motkontotype** eller **Kontotype** er **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="52eec-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="52eec-120">**Manuell sjekk**: Velg dette alternativet hvis du manuelt har skrevet en sjekk og vil at programmet skal opprette en tilhørende sjekkpost på dette beløpet.</span><span class="sxs-lookup"><span data-stu-id="52eec-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="52eec-121">Når du bruker dette alternativet, kan du ikke skrive ut sjekker fra [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="52eec-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="52eec-122">Du kan bare velge **Manuell sjekk** hvis **Motkontotype** eller **Kontotype** er **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="52eec-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="52eec-123">Du må skrive ut maskinelle sjekker før du kan bokføre de relaterte kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="52eec-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="52eec-124">Velg **Skriv ut sjekk** for maskinelle sjekker.</span><span class="sxs-lookup"><span data-stu-id="52eec-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="52eec-125">Fyll ut feltene etter behov i vinduet **Sjekk**.</span><span class="sxs-lookup"><span data-stu-id="52eec-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="52eec-126">Velg **Skriv ut**.</span><span class="sxs-lookup"><span data-stu-id="52eec-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="52eec-127">Hvis du vil skrive ut sjekker i flere valutaer fra forskjellige bankkonti, må du utføre kjørselen **Skriv ut sjekk** separat for hver enkelt valuta og angi riktig bankkonto.</span><span class="sxs-lookup"><span data-stu-id="52eec-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="52eec-128">Kansellere utskrevne sjekker som ikke er bokført</span><span class="sxs-lookup"><span data-stu-id="52eec-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="52eec-129">Du kan kansellere ikke-bokførte sjekker etter at de er skrevet ut, ved hjelp av handlingen **Kanseller sjekk** i vinduet **Betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="52eec-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="52eec-130">I vinduet **Betalingskladd** velger du **Kanseller sjekk**, og deretter velger du hvilke sjekker som skal kanselleres.</span><span class="sxs-lookup"><span data-stu-id="52eec-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="52eec-131">Kansellere sjekker</span><span class="sxs-lookup"><span data-stu-id="52eec-131">To void checks</span></span>
<span data-ttu-id="52eec-132">Når sjekkbetaliner er bokført, kan du bare kansellere (void) sjekker fra de resulterende bankpostene.</span><span class="sxs-lookup"><span data-stu-id="52eec-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="52eec-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="52eec-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="52eec-134">Velg relevant bankkonto, velg handlingene **Rediger** og **Sjekkposter**.</span><span class="sxs-lookup"><span data-stu-id="52eec-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="52eec-135">I vinduet **Sjekkposter** velger du handlingen **Kanseller sjekk**.</span><span class="sxs-lookup"><span data-stu-id="52eec-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="52eec-136">Merk av for **Kanseller sjekk**.</span><span class="sxs-lookup"><span data-stu-id="52eec-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="52eec-137">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="52eec-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="52eec-138">Se også</span><span class="sxs-lookup"><span data-stu-id="52eec-138">See Also</span></span>
[<span data-ttu-id="52eec-139">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="52eec-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="52eec-140">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="52eec-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="52eec-141">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="52eec-141">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="52eec-142">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="52eec-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

