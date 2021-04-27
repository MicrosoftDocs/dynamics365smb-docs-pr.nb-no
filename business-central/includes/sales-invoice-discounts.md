---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778650"
---
<span data-ttu-id="ccb3a-101">Når alle varene er registrert som salgslinjer, kan du beregne fakturarabatten for hele salgsdokumentet ved å velge handlingen **Beregn fakturarabatt**.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-101">When all the items have been entered as lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="ccb3a-102">Rabatten beregnes basert på alle linjene i salgsdokumentet for varer, forutsatt at det står **Ja** i feltet **Tillat fakturarabatt** på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="ccb3a-103">Dette er standardinnstillingen for varer.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-103">This is the default setting for items.</span></span> <span data-ttu-id="ccb3a-104">Linjer med for eksempel varegebyrer tas ikke med i beregningen av fakturarabatten.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="ccb3a-105">Hvis du vil bruke en rabatt på slike linjer, må du angi feltet **Linjerabatt-%** på de aktuelle linjene.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="ccb3a-106">Hvis **Beregn fakturarabatt**-feltet er valgt på siden **Oppsett av kunde- og leverandørkonto**, beregnes fakturarabatten automatisk når du gjør et av følgende på et salgsdokument:</span><span class="sxs-lookup"><span data-stu-id="ccb3a-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="ccb3a-107">Vis statistikk</span><span class="sxs-lookup"><span data-stu-id="ccb3a-107">View statistics</span></span>
> * <span data-ttu-id="ccb3a-108">Vis en testrapport</span><span class="sxs-lookup"><span data-stu-id="ccb3a-108">View a test report</span></span>
> * <span data-ttu-id="ccb3a-109">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="ccb3a-109">Print</span></span>
> * <span data-ttu-id="ccb3a-110">Post</span><span class="sxs-lookup"><span data-stu-id="ccb3a-110">Post</span></span>

<span data-ttu-id="ccb3a-111">Fakturarabattbetingelsene for en kunde er definert på siden **Kundefakturarabatter** for kunden.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="ccb3a-112">Valutakoden på salgsdokumentet brukes til å finne betingelsene for fakturarabatt i den aktuelle valutaen.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="ccb3a-113">Hvis fakturarabattene ikke er definert i fremmed valuta, er fakturarabattbetingelsene definert på siden **Kundefakturarabatt** med beløpene i lokal valuta, og valutakursen på bokføringsdatoen i salgsdokumentet til å beregne fakturarabatten i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="ccb3a-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
