---
title: Overføre bankkapital| Microsoft-dokumentasjon
description: Du kan overføre beløp fra én bankkonto til en annen, inkludert ulike valutaer, ved å bokføre transaksjonen i finanskladden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1a0ab7c2a96c278740c07ff243ad785be1d72dd4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388102"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="893fa-103">Overføre bankkapital</span><span class="sxs-lookup"><span data-stu-id="893fa-103">Transfer Bank Funds</span></span>
<span data-ttu-id="893fa-104">Noen ganger har du behov for å overføre av et beløp fra én konto til en annen i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="893fa-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="893fa-105">Hvis du vil gjøre dette, må du bokføre transaksjonen på siden **Finanskladd**.</span><span class="sxs-lookup"><span data-stu-id="893fa-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="893fa-106">Oppgaven varierer avhengig av om bankkontoene bruker samme valuta eller forskjellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="893fa-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="893fa-107">Bokføre en overføring mellom bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="893fa-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="893fa-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="893fa-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="893fa-109">På en av kladdelinjene fyller du ut feltet **Bokføringsdato** og **Bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="893fa-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="893fa-110">Velg **Bankkonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="893fa-111">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="893fa-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="893fa-112">Angi beløpet som skal overføres i feltet **Beløp**.</span><span class="sxs-lookup"><span data-stu-id="893fa-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="893fa-113">Velg handlingen **Vis flere kolonner** for å vise alle tilgjengelige felt.</span><span class="sxs-lookup"><span data-stu-id="893fa-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="893fa-114">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="893fa-115">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="893fa-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="893fa-116">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="893fa-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="893fa-117">Slik bokfører du en overføring mellom bankkonti med ulike valutakoder</span><span class="sxs-lookup"><span data-stu-id="893fa-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="893fa-118">Hvis du vil overføre midler mellom bankkonti som bruker forskjellige valutaer, må du bokføre to linjer i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="893fa-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="893fa-119">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="893fa-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="893fa-120">Opprett to kladdelinjer, og fyll ut feltene **Bokføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="893fa-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="893fa-121">På den første kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="893fa-122">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="893fa-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="893fa-123">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="893fa-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="893fa-124">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="893fa-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="893fa-125">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="893fa-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="893fa-126">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="893fa-127">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="893fa-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="893fa-128">På den andre kladdelinje angir du **Bankkonto** i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="893fa-129">I feltet **Kontonr.** velger du bankkontoen du vil overføre midler til.</span><span class="sxs-lookup"><span data-stu-id="893fa-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="893fa-130">I **Beløp**-feltet angir du beløpet i valutaen til bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="893fa-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="893fa-131">Angi kreditbeløp med minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="893fa-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="893fa-132">Angi debetbeløp uten minus som fortegn.</span><span class="sxs-lookup"><span data-stu-id="893fa-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="893fa-133">Velg **Bankkonto** i **Motkontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="893fa-134">I feltet **Motkontonr.** velger du bankkontoen du vil overføre midler fra.</span><span class="sxs-lookup"><span data-stu-id="893fa-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="893fa-135">Hvis valutakursene som brukes i kladden, ikke er de samme som valutakursene på siden **Valutakurser**, angir du en tredje linje for agio/disagio.</span><span class="sxs-lookup"><span data-stu-id="893fa-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="893fa-136">Angi **Finanskonto** i **Kontotype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="893fa-137">Angi finanskontonummeret for agio eller disagio i **Kontonr.**-feltet.</span><span class="sxs-lookup"><span data-stu-id="893fa-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="893fa-138">Angi agio eller disagio i **Beløp**-feltet med eller uten et minustegn for henholdsvis kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="893fa-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="893fa-139">Bokfør kladden.</span><span class="sxs-lookup"><span data-stu-id="893fa-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="893fa-140">Se også</span><span class="sxs-lookup"><span data-stu-id="893fa-140">See Also</span></span>
[<span data-ttu-id="893fa-141">Avstemme bankkonter</span><span class="sxs-lookup"><span data-stu-id="893fa-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="893fa-142">Konfigurere banktjenester</span><span class="sxs-lookup"><span data-stu-id="893fa-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="893fa-143">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="893fa-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="893fa-144">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="893fa-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]