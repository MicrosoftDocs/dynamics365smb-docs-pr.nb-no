---
title: Tilbakeføre avgangsbokføring | Microsoft-dokumentasjon
description: Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cad24d75cacc290ea69f3a4488efd8dc9832a42c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787780"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="965c3-104">Tilbakeføre avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="965c3-104">Reverse Output Posting</span></span>
<span data-ttu-id="965c3-105">Det hender at avgangsbokføring må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="965c3-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="965c3-106">Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="965c3-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="965c3-107">Tilbakeføre en avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="965c3-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="965c3-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="965c3-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="965c3-109">Velg kjørselen.</span><span class="sxs-lookup"><span data-stu-id="965c3-109">Select your batch.</span></span>  
2. <span data-ttu-id="965c3-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="965c3-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="965c3-111">Hvis du vil ha mer informasjon, se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="965c3-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="965c3-112">Velg den tilknyttede vareposten i **Utligningspost**-feltet.</span><span class="sxs-lookup"><span data-stu-id="965c3-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="965c3-113">Dermed tilbakeføres kapasitets- og varepostene.</span><span class="sxs-lookup"><span data-stu-id="965c3-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="965c3-114">Bokfør tilbakeføringen ved bokføring av kladden.</span><span class="sxs-lookup"><span data-stu-id="965c3-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="965c3-115">Postene i ferdigmeldingskladden bokføres i vareposten som en oppjustering.</span><span class="sxs-lookup"><span data-stu-id="965c3-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="965c3-116">Se også</span><span class="sxs-lookup"><span data-stu-id="965c3-116">See Also</span></span>  
 <span data-ttu-id="965c3-117">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="965c3-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="965c3-118">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="965c3-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="965c3-119">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="965c3-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="965c3-120">Lager</span><span class="sxs-lookup"><span data-stu-id="965c3-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="965c3-121">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="965c3-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="965c3-122">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="965c3-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]