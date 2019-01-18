---
title: "Bokføre betalinger med SEPA Direct Debit | Microsoft-dokumentasjon"
description: "Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: d427ab28e1344ece77baaab8ceefe4043d3beaa0
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="91ff5-103">Bokføre kvitteringer for SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="91ff5-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="91ff5-104">Når en direct debit-samling er behandlet av banken din, kan du fortsette med å bokføre mottak av betalingen for de aktuelle salgsfakturaene.</span><span class="sxs-lookup"><span data-stu-id="91ff5-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="91ff5-105">Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="91ff5-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="91ff5-106">Du kan bokføre kvittering direkte fra siden **Direct Debit\-oppkrevinger** eller siden **Poster for Direct Debit-oppkreving**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-106">You can post the payment receipt directly from the **Direct Debit Collections** page or the **Direct Debit Collect. Entries** page.</span></span> <span data-ttu-id="91ff5-107">Du kan også overføre arbeidet til en annen bruker ved klargjøre de relaterte kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="91ff5-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page"></a><span data-ttu-id="91ff5-108">Slik bokfører du en kvittering for direct debit fra siden Direct Debit-samlinger</span><span class="sxs-lookup"><span data-stu-id="91ff5-108">To post a direct-debit payment receipt from the Direct Debit Collections page</span></span>  
1. <span data-ttu-id="91ff5-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Direct Debit-oppkrevinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="91ff5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91ff5-110">Velg en linje for en direct debit-samling som er eksportert til en bankfil og behandlet av banken.</span><span class="sxs-lookup"><span data-stu-id="91ff5-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="91ff5-111">Hvis du vil ha mer informasjon, kan du se [Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)</span><span class="sxs-lookup"><span data-stu-id="91ff5-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="91ff5-112">Velg handlingen **Bokfør kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="91ff5-113">På siden **Bokfør Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="91ff5-113">On the **Post Direct Debit Collection** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="91ff5-114">Felt</span><span class="sxs-lookup"><span data-stu-id="91ff5-114">Field</span></span>|<span data-ttu-id="91ff5-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="91ff5-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="91ff5-116">**Direct Debit-oppkrevingsnr.**</span><span class="sxs-lookup"><span data-stu-id="91ff5-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="91ff5-117">Angi direct debit-samlingen du vil bokføre kvittering for.</span><span class="sxs-lookup"><span data-stu-id="91ff5-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="91ff5-118">**Finanskladdemal**</span><span class="sxs-lookup"><span data-stu-id="91ff5-118">**General Journal Template**</span></span>|<span data-ttu-id="91ff5-119">Angi hvilken finanskladdemal som skal brukes til bokføring av kvitteringen, for eksempel malen for innbetalinger.</span><span class="sxs-lookup"><span data-stu-id="91ff5-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="91ff5-120">**Finanskladdenavn**</span><span class="sxs-lookup"><span data-stu-id="91ff5-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="91ff5-121">Angi hvilken finanskladd som skal brukes til bokføring av kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="91ff5-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="91ff5-122">**Opprett bare kladd**</span><span class="sxs-lookup"><span data-stu-id="91ff5-122">**Create Journal Only**</span></span>|<span data-ttu-id="91ff5-123">Merk av for dette alternativet hvis du ikke vil bokføre kvitteringen når du velger **OK**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="91ff5-124">Kvitteringen blir klargjort i den angitte kladden, og blir ikke bokført før noen bokfører de aktuelle kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="91ff5-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="91ff5-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91ff5-126">Se også</span><span class="sxs-lookup"><span data-stu-id="91ff5-126">See Also</span></span>  
 <span data-ttu-id="91ff5-127">[Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="91ff5-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="91ff5-128">Salg</span><span class="sxs-lookup"><span data-stu-id="91ff5-128">Sales</span></span>](sales-manage-sales.md)

