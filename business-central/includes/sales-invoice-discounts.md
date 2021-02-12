---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035791"
---
<span data-ttu-id="ff785-101">Når alle varene er registrert på ordrelinjene, kan du beregne fakturarabatten for hele salgsdokumentet ved å velge handlingen **Beregn fakturarabatt**.</span><span class="sxs-lookup"><span data-stu-id="ff785-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="ff785-102">Hvis **Beregn fakturarabatt**-feltet er valgt i vinduet **Oppsett av kunde- og leverandørkonto**, beregnes fakturarabatten automatisk når du gjør et av følgende på et salgsdokument:</span><span class="sxs-lookup"><span data-stu-id="ff785-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="ff785-103">Vis statistikk</span><span class="sxs-lookup"><span data-stu-id="ff785-103">View statistics</span></span>
* <span data-ttu-id="ff785-104">Vis en testrapport</span><span class="sxs-lookup"><span data-stu-id="ff785-104">View a test report</span></span>
* <span data-ttu-id="ff785-105">Skriv ut</span><span class="sxs-lookup"><span data-stu-id="ff785-105">Print</span></span>
* <span data-ttu-id="ff785-106">Post</span><span class="sxs-lookup"><span data-stu-id="ff785-106">Post</span></span>

<span data-ttu-id="ff785-107">Rabatten fordeles på alle linjene i salgsdokumentet for varer, forutsatt at det står **Ja** i feltet **Tillat fakturarabatt** på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="ff785-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="ff785-108">Dette er standardinnstillingen for varer.</span><span class="sxs-lookup"><span data-stu-id="ff785-108">This is the default setting for items.</span></span>

<span data-ttu-id="ff785-109">Fakturarabattbetingelsene er definert på siden **Kundefakturarabatter** til å beregne fakturarabatt.</span><span class="sxs-lookup"><span data-stu-id="ff785-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="ff785-110">Valutakoden på salgsdokumentet brukes til å finne betingelsene for fakturarabatt i den aktuelle valutaen.</span><span class="sxs-lookup"><span data-stu-id="ff785-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="ff785-111">Hvis fakturarabattene ikke er definert i fremmed valuta, er fakturarabattbetingelsene definert på siden **Kundefakturarabatt** med beløpene i lokal valuta, og valutakursen på bokføringsdatoen i salgsdokumentet til å beregne fakturarabatten i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="ff785-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
