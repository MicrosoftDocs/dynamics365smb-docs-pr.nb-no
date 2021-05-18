---
title: Overføre bankkapital
description: Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985390"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="785bc-103">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="785bc-103">Transfer Bank Funds</span></span>

<span data-ttu-id="785bc-104">Noen ganger har du behov for å overføre av et beløp fra én konto til en annen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="785bc-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="785bc-105">Hvis du vil gjøre dette, må du bokføre transaksjonen på **Finanskladd**-siden.</span><span class="sxs-lookup"><span data-stu-id="785bc-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="785bc-106">Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="785bc-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="785bc-107">Bokføre en overføring mellom bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="785bc-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="785bc-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="785bc-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="785bc-109">På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="785bc-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="785bc-110">Velg **Bankkonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="785bc-111">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="785bc-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="785bc-112">Angi beløpet som skal overføres i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="785bc-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="785bc-113">Du må deretter angi motkontoen.</span><span class="sxs-lookup"><span data-stu-id="785bc-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="785bc-114">Hvis de relevante feltene ikke vises, velger du handlingen **Vis flere kolonner** for å vise alle tilgjengelige felter.</span><span class="sxs-lookup"><span data-stu-id="785bc-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="785bc-115">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="785bc-116">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="785bc-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="785bc-117">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="785bc-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="785bc-118">Slik bokfører du en overføring mellom bankkonti med ulike valutakoder</span><span class="sxs-lookup"><span data-stu-id="785bc-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="785bc-119">Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="785bc-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="785bc-120">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="785bc-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="785bc-121">Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="785bc-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="785bc-122">På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="785bc-123">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="785bc-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="785bc-124">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen med eller uten et minustegn.</span><span class="sxs-lookup"><span data-stu-id="785bc-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="785bc-125">Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.</span><span class="sxs-lookup"><span data-stu-id="785bc-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="785bc-126">Noen selskaper foretrekker å overføre mellom konti på separate kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="785bc-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="785bc-127">Andre selskaper foretrekker å bokføre alt på én kladdelinje ved hjelp av en motkonto.</span><span class="sxs-lookup"><span data-stu-id="785bc-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="785bc-128">Kontakt den lokale eksperten hvis du ikke er sikker på hva du skal gjøre.</span><span class="sxs-lookup"><span data-stu-id="785bc-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="785bc-129">Hvis selskapet foretrekker å bruke en motkonto, setter du feltet **Motkontotype** til **Bankkonto** og feltet **Motkontonr.** til bankkontoen du vil overføre midlene til.</span><span class="sxs-lookup"><span data-stu-id="785bc-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="785bc-130">Gå deretter videre til trinn 9 eller 10.</span><span class="sxs-lookup"><span data-stu-id="785bc-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="785bc-131">Hvis selskapet foretrekker å bruke en separat kladdelinje, går du videre til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="785bc-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="785bc-132">På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="785bc-133">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="785bc-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="785bc-134">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen med eller uten et minustegn.</span><span class="sxs-lookup"><span data-stu-id="785bc-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="785bc-135">Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.</span><span class="sxs-lookup"><span data-stu-id="785bc-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="785bc-136">Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene på siden **Valutakurser**, angir du en ny kladdelinje for agio eller disagio.</span><span class="sxs-lookup"><span data-stu-id="785bc-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="785bc-137">Angi **Finanskonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="785bc-138">Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="785bc-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="785bc-139">Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn.</span><span class="sxs-lookup"><span data-stu-id="785bc-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="785bc-140">Et beløp uten et fortegn er et debetbeløp, og et beløp med et minustegn er et kreditbeløp.</span><span class="sxs-lookup"><span data-stu-id="785bc-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="785bc-141">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="785bc-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="785bc-142">Se også</span><span class="sxs-lookup"><span data-stu-id="785bc-142">See Also</span></span>

[<span data-ttu-id="785bc-143">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="785bc-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="785bc-144">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="785bc-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="785bc-145">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="785bc-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="785bc-146">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="785bc-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]