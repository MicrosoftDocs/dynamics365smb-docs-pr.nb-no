---
title: Opprette en forespørsel for å be om et tilbud | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde og selge produkter under visse betingelser.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 416c5a4e4376932c16a1496f2db2b0c79307d22b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772622"
---
# <a name="request-quotes"></a><span data-ttu-id="cb976-103">Be om tilbud</span><span class="sxs-lookup"><span data-stu-id="cb976-103">Request Quotes</span></span>
<span data-ttu-id="cb976-104">En forespørsel kan brukes som et foreløpig utkast til en bestilling, og bestillingen kan deretter konverteres til en bestilling eller ordre.</span><span class="sxs-lookup"><span data-stu-id="cb976-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="cb976-105">Slik oppretter du en forespørsel</span><span class="sxs-lookup"><span data-stu-id="cb976-105">To create a purchase quote</span></span>
1. <span data-ttu-id="cb976-106">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forespørsler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cb976-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="cb976-107">Opprett et nytt dokument, på samme måte som du oppretter en bestilling.</span><span class="sxs-lookup"><span data-stu-id="cb976-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="cb976-108">Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="cb976-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="cb976-109">Slik konverterer du en forespørsel til en bestilling</span><span class="sxs-lookup"><span data-stu-id="cb976-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="cb976-110">Når du har godtatt leverandørtilbudet, kan du konvertere det til en kjøpsfaktura eller ordre for å behandle kjøpet.</span><span class="sxs-lookup"><span data-stu-id="cb976-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="cb976-111">Åpne en forespørsel som er klar til å konverteres, og velg handlingen **Lag ordre**.</span><span class="sxs-lookup"><span data-stu-id="cb976-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="cb976-112">Forespørselen er fjernet fra databasen.</span><span class="sxs-lookup"><span data-stu-id="cb976-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="cb976-113">Det opprettes en kjøpsfaktura eller bestilling basert på informasjonen i forespørselen der du kan behandle kjøpet.</span><span class="sxs-lookup"><span data-stu-id="cb976-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="cb976-114">I feltet **Tilbudsnr.** på kjøpsfakturaen eller bestillingen kan du se nummeret på forespørselen den ble laget fra.</span><span class="sxs-lookup"><span data-stu-id="cb976-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb976-115">Se også</span><span class="sxs-lookup"><span data-stu-id="cb976-115">See Also</span></span>
[<span data-ttu-id="cb976-116">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="cb976-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="cb976-117">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="cb976-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="cb976-118">Sende dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="cb976-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="cb976-119">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb976-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]