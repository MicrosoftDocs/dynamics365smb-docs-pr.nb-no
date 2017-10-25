---
title: "Overføre bankkapital| Microsoft-dokumentasjon"
description: "Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-transfer-bank-funds"></a><span data-ttu-id="ae260-103">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="ae260-103">How to: Transfer Bank Funds</span></span>
<span data-ttu-id="ae260-104">Noen ganger har du behov for å overføre av et beløp fra én konto til en annen.</span><span class="sxs-lookup"><span data-stu-id="ae260-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="ae260-105">Hvis du vil gjøre dette, må du bokføre transaksjonen i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="ae260-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="ae260-106">Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="ae260-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="ae260-107">Bokføre en overføring mellom bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="ae260-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="ae260-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ae260-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae260-109">På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="ae260-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ae260-110">Velg **Bankkonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ae260-111">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="ae260-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ae260-112">Angi beløpet som skal overføres i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="ae260-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="ae260-113">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="ae260-114">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="ae260-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="ae260-115">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="ae260-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="ae260-116">Slik bokfører du en overføring mellom bankkonti med ulike valutakoder</span><span class="sxs-lookup"><span data-stu-id="ae260-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="ae260-117">Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="ae260-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="ae260-118">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ae260-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="ae260-119">Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="ae260-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="ae260-120">På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="ae260-121">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="ae260-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="ae260-122">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="ae260-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="ae260-123">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="ae260-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="ae260-124">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="ae260-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="ae260-125">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="ae260-126">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="ae260-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="ae260-127">På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="ae260-128">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="ae260-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="ae260-129">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="ae260-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="ae260-130">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="ae260-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="ae260-131">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="ae260-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="ae260-132">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="ae260-133">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="ae260-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="ae260-134">Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene i vinduet **Valutakurser**, angir du en tredje linje for agio/disagio.</span><span class="sxs-lookup"><span data-stu-id="ae260-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="ae260-135">Angi **Finanskonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="ae260-136">Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae260-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="ae260-137">Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn for henholdsvis kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="ae260-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="ae260-138">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="ae260-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae260-139">Se også</span><span class="sxs-lookup"><span data-stu-id="ae260-139">See Also</span></span>
[<span data-ttu-id="ae260-140">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="ae260-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="ae260-141">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="ae260-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ae260-142">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="ae260-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ae260-143">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ae260-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

