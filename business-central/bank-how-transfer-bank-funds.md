---
title: "Overføre bankkapital| Microsoft-dokumentasjon"
description: "Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54e8a7bf7ca8761d6317b57d45e64f9ee628f4b8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="787e3-103">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="787e3-103">Transfer Bank Funds</span></span>
<span data-ttu-id="787e3-104">Noen ganger har du behov for å overføre av et beløp fra én konto til en annen.</span><span class="sxs-lookup"><span data-stu-id="787e3-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="787e3-105">Hvis du vil gjøre dette, må du bokføre transaksjonen i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="787e3-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="787e3-106">Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="787e3-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="787e3-107">Bokføre en overføring mellom bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="787e3-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="787e3-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="787e3-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="787e3-109">På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="787e3-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="787e3-110">Velg **Bankkonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="787e3-111">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="787e3-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="787e3-112">Angi beløpet som skal overføres i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="787e3-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="787e3-113">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="787e3-114">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="787e3-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="787e3-115">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="787e3-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="787e3-116">Slik bokfører du en overføring mellom bankkonti med ulike valutakoder</span><span class="sxs-lookup"><span data-stu-id="787e3-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="787e3-117">Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="787e3-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="787e3-118">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="787e3-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="787e3-119">Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="787e3-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="787e3-120">På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="787e3-121">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="787e3-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="787e3-122">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="787e3-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="787e3-123">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="787e3-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="787e3-124">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="787e3-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="787e3-125">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="787e3-126">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="787e3-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="787e3-127">På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="787e3-128">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="787e3-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="787e3-129">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="787e3-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="787e3-130">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="787e3-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="787e3-131">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="787e3-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="787e3-132">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="787e3-133">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="787e3-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="787e3-134">Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene i vinduet **Valutakurser**, angir du en tredje linje for agio/disagio.</span><span class="sxs-lookup"><span data-stu-id="787e3-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="787e3-135">Angi **Finanskonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="787e3-136">Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="787e3-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="787e3-137">Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn for henholdsvis kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="787e3-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="787e3-138">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="787e3-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="787e3-139">Se også</span><span class="sxs-lookup"><span data-stu-id="787e3-139">See Also</span></span>
[<span data-ttu-id="787e3-140">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="787e3-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="787e3-141">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="787e3-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="787e3-142">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="787e3-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="787e3-143">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="787e3-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

