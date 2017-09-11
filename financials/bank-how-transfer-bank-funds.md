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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 20661cce60bc9007adb9767388bf5af6f9c3acb9
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-transfer-bank-funds"></a><span data-ttu-id="79f7c-103">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="79f7c-103">How to: Transfer Bank Funds</span></span>
<span data-ttu-id="79f7c-104">Noen ganger har du behov for å overføre av et beløp fra én konto til en annen.</span><span class="sxs-lookup"><span data-stu-id="79f7c-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="79f7c-105">Hvis du vil gjøre dette, må du bokføre transaksjonen i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="79f7c-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="79f7c-106">Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="79f7c-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="79f7c-107">Bokføre en overføring mellom bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="79f7c-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="79f7c-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="79f7c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="79f7c-109">På en av kladdelinjene fyller du ut **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="79f7c-109">On a journal line, fill in the **Posting Date** and **Document No.**</span></span> <span data-ttu-id="79f7c-110">-feltene.</span><span class="sxs-lookup"><span data-stu-id="79f7c-110">fields.</span></span>
3. <span data-ttu-id="79f7c-111">Velg **Bankkonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-111">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="79f7c-112">I **Kontonummer**</span><span class="sxs-lookup"><span data-stu-id="79f7c-112">In the **Account No.**</span></span> <span data-ttu-id="79f7c-113">-feltet velger du banken du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="79f7c-113">field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="79f7c-114">Angi beløpet som skal overføres i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="79f7c-114">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="79f7c-115">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="79f7c-116">I **Motkontonr.**</span><span class="sxs-lookup"><span data-stu-id="79f7c-116">In the **Bal. Account No.**</span></span> <span data-ttu-id="79f7c-117">-feltet velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="79f7c-117">field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="79f7c-118">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="79f7c-118">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="79f7c-119">Slik bokfører du en overføring mellom bankkonti med ulike valutakoder</span><span class="sxs-lookup"><span data-stu-id="79f7c-119">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="79f7c-120">Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="79f7c-120">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="79f7c-121">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="79f7c-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="79f7c-122">Opprett to kladdelinjer, og fyll ut **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="79f7c-122">Create two journal lines, and fill in the **Posting Date** and **Document No.**</span></span> <span data-ttu-id="79f7c-123">-feltene.</span><span class="sxs-lookup"><span data-stu-id="79f7c-123">fields.</span></span>
3. <span data-ttu-id="79f7c-124">På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-124">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="79f7c-125">I **Kontonummer**</span><span class="sxs-lookup"><span data-stu-id="79f7c-125">In the **Account No.**</span></span> <span data-ttu-id="79f7c-126">-feltet velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="79f7c-126">field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="79f7c-127">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="79f7c-127">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="79f7c-128">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="79f7c-128">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="79f7c-129">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="79f7c-129">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="79f7c-130">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-130">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="79f7c-131">I **Motkontonr.**</span><span class="sxs-lookup"><span data-stu-id="79f7c-131">In the **Bal. Account No.**</span></span> <span data-ttu-id="79f7c-132">-feltet velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="79f7c-132">field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="79f7c-133">På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-133">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="79f7c-134">I **Kontonummer**</span><span class="sxs-lookup"><span data-stu-id="79f7c-134">In the **Account No.**</span></span> <span data-ttu-id="79f7c-135">-feltet velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="79f7c-135">field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="79f7c-136">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="79f7c-136">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="79f7c-137">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="79f7c-137">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="79f7c-138">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="79f7c-138">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="79f7c-139">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-139">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="79f7c-140">I **Motkontonr.**</span><span class="sxs-lookup"><span data-stu-id="79f7c-140">In the **Bal. Account No.**</span></span> <span data-ttu-id="79f7c-141">-feltet velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="79f7c-141">field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="79f7c-142">Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene i vinduet **Valutakurser**, angir du en tredje linje for agio/disagio.</span><span class="sxs-lookup"><span data-stu-id="79f7c-142">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="79f7c-143">Angi **Finanskonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-143">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="79f7c-144">Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-144">Enter the G/L account number for exchange rate gain or loss in the **Account No.**</span></span> <span data-ttu-id="79f7c-145">.</span><span class="sxs-lookup"><span data-stu-id="79f7c-145">field.</span></span> <span data-ttu-id="79f7c-146">Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn for henholdsvis kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="79f7c-146">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="79f7c-147">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="79f7c-147">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="79f7c-148">Se også</span><span class="sxs-lookup"><span data-stu-id="79f7c-148">See Also</span></span>
[<span data-ttu-id="79f7c-149">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="79f7c-149">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="79f7c-150">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="79f7c-150">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="79f7c-151">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="79f7c-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="79f7c-152">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79f7c-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

