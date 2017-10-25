---
title: "Opprette en forespørsel for å be om et tilbud fra leverandøren | Microsoft-dokumentasjon"
description: "Beskriver hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde og selge produkter under visse betingelser."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: fe51ade7a46ab7a8fdf77419a0098ac47fe2e5d1
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-request-quotes"></a><span data-ttu-id="4f832-103">Be om tilbud</span><span class="sxs-lookup"><span data-stu-id="4f832-103">How to: Request Quotes</span></span>
<span data-ttu-id="4f832-104">En forespørsel kan brukes som et foreløpig utkast til en bestilling, og bestillingen kan deretter konverteres til en bestilling eller ordre.</span><span class="sxs-lookup"><span data-stu-id="4f832-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or a order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="4f832-105">Slik oppretter du en forespørsel</span><span class="sxs-lookup"><span data-stu-id="4f832-105">To create a purchase quote</span></span>
1. <span data-ttu-id="4f832-106">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Forespørsler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4f832-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="4f832-107">Opprett et nytt dokument, på samme måte som du oppretter en bestilling.</span><span class="sxs-lookup"><span data-stu-id="4f832-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="4f832-108">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="4f832-108">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="4f832-109">Slik konverterer du en forespørsel til en bestilling</span><span class="sxs-lookup"><span data-stu-id="4f832-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="4f832-110">Når du har godtatt leverandørtilbudet, kan du konvertere det til en kjøpsfaktura eller ordre for å behandle kjøpet.</span><span class="sxs-lookup"><span data-stu-id="4f832-110">When you have accepted the vendors quote, you can convert it to a purchase invoice or ordfer to process the purchase.</span></span>

1. <span data-ttu-id="4f832-111">Åpne en forespørsel som er klar til å konverteres, og velg handlingen **Lag ordre**.</span><span class="sxs-lookup"><span data-stu-id="4f832-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="4f832-112">Forespørselen er fjernet fra databasen.</span><span class="sxs-lookup"><span data-stu-id="4f832-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="4f832-113">Det opprettes en kjøpsfaktura eller ordre basert på informasjonen i forespørselen der du kan behandle kjøpet.</span><span class="sxs-lookup"><span data-stu-id="4f832-113">A purchase invoice or a sales order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="4f832-114">I feltet **Tilbudsnr.** på kjøpsfakturaen eller bestillingen kan du se nummeret på forespørselen den ble laget fra.</span><span class="sxs-lookup"><span data-stu-id="4f832-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f832-115">Se også</span><span class="sxs-lookup"><span data-stu-id="4f832-115">See Also</span></span>
[<span data-ttu-id="4f832-116">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4f832-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4f832-117">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="4f832-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="4f832-118">Sende dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="4f832-118">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="4f832-119">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4f832-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

