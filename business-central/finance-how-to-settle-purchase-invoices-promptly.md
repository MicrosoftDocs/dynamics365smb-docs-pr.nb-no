---
title: Gjøre opp kjøpsfakturaer omgående
description: Hvis du må betale leverandøren kontant eller med sjekk, kan du utføre den nødvendige bokføringen når du bokfører selve fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 60d3cf3c9e141c8df36eaca2c1975b696fdb105b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387252"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="a2d93-103">Gjøre opp kjøpsfakturaer omgående</span><span class="sxs-lookup"><span data-stu-id="a2d93-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="a2d93-104">Hvis du må betale leverandøren kontant eller med sjekk, kan du bokføre betalingen når du bokfører selve fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a2d93-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="a2d93-105">Hvis du vanligvis betaler kjøpsfakturaer kontant, med sjekk eller bankoverføring, er det lurt å definere en bestemt betalingsmåte med en motkonto, og angi denne betalingsmåten i feltet **Betalingsmåte** på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="a2d93-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="a2d93-106">Motkontonummeret settes automatisk inn i fakturahodet hver gang du oppretter en ny faktura.</span><span class="sxs-lookup"><span data-stu-id="a2d93-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="a2d93-107">Hvis du vil ha mer informasjon, kan du se [Definere betalingsmåter](finance-payment-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a2d93-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="a2d93-108">Slik gjør du opp kjøpsfakturaer omgående</span><span class="sxs-lookup"><span data-stu-id="a2d93-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="a2d93-109">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a2d93-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a2d93-110">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a2d93-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="a2d93-111">Hvis du vil betale enten med kontanter eller med giro, angir du nummeret på kassekontoen eller bankkontoen i feltet **Motkontonr.**.</span><span class="sxs-lookup"><span data-stu-id="a2d93-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="a2d93-112">Feltene **Motkontotype** og **Motkontonr.** inngår ikke i standardoppsettet for fakturahodet.</span><span class="sxs-lookup"><span data-stu-id="a2d93-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="a2d93-113">Hvis du vil bokføre betalingen av en faktura, må du kontakte en Microsoft-partner som kan legge til feltene via kode.</span><span class="sxs-lookup"><span data-stu-id="a2d93-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="a2d93-114">Denne tilpassingen er bare nødvendig hvis du ikke angir motkonti i betalingsmåtene som beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="a2d93-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2d93-115">Se også</span><span class="sxs-lookup"><span data-stu-id="a2d93-115">See Also</span></span>

[<span data-ttu-id="a2d93-116">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="a2d93-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="a2d93-117">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="a2d93-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a2d93-118">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2d93-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]