---
title: "Tilbakeføre avgangsbokføring | Microsoft-dokumentasjon"
description: "Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a><span data-ttu-id="33950-104">Tilbakeføre avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="33950-104">How to: Reverse Output Posting</span></span>
<span data-ttu-id="33950-105">Det hender at avgangsbokføring må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="33950-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="33950-106">Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="33950-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="33950-107">Tilbakeføre en avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="33950-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="33950-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="33950-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="33950-109">Velg kjørselen.</span><span class="sxs-lookup"><span data-stu-id="33950-109">Select your batch.</span></span>  
2. <span data-ttu-id="33950-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="33950-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="33950-111">Hvis du vil ha mer informasjon, se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="33950-111">For more information, see [How to: Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="33950-112">Velg den tilknyttede vareposten i **Utligningspost**-feltet.</span><span class="sxs-lookup"><span data-stu-id="33950-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="33950-113">Dermed tilbakeføres kapasitets- og varepostene.</span><span class="sxs-lookup"><span data-stu-id="33950-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="33950-114">Bokfør tilbakeføringen ved bokføring av kladden.</span><span class="sxs-lookup"><span data-stu-id="33950-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="33950-115">Postene i ferdigmeldingskladden bokføres i vareposten som en oppjustering.</span><span class="sxs-lookup"><span data-stu-id="33950-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33950-116">Se også</span><span class="sxs-lookup"><span data-stu-id="33950-116">See Also</span></span>  
 <span data-ttu-id="33950-117">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="33950-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="33950-118">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="33950-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="33950-119">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="33950-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="33950-120">Lager</span><span class="sxs-lookup"><span data-stu-id="33950-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="33950-121">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="33950-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="33950-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33950-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

