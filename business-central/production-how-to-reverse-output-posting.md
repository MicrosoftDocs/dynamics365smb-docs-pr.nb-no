---
title: Tilbakeføre avgangsbokføring | Microsoft-dokumentasjon
description: Det hender at avgangsbokføring må tilbakeføres. Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788753"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="d8c0e-104">Tilbakeføre avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="d8c0e-104">Reverse Output Posting</span></span>
<span data-ttu-id="d8c0e-105">Det hender at avgangsbokføring må tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="d8c0e-106">Et eksempel på dette er hvis det oppstår en dataregistreringsfeil, og feil antall avganger bokføres i en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="d8c0e-107">Tilbakeføre en avgangsbokføring</span><span class="sxs-lookup"><span data-stu-id="d8c0e-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="d8c0e-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ferdigmeldingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="d8c0e-109">Velg kjørselen.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-109">Select your batch.</span></span>  
2. <span data-ttu-id="d8c0e-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="d8c0e-111">Hvis du vil ha mer informasjon, se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="d8c0e-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="d8c0e-112">Velg den tilknyttede vareposten i **Utligningspost**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="d8c0e-113">Dermed tilbakeføres kapasitets- og varepostene.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="d8c0e-114">Bokfør tilbakeføringen ved bokføring av kladden.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="d8c0e-115">Postene i ferdigmeldingskladden bokføres i vareposten som en oppjustering.</span><span class="sxs-lookup"><span data-stu-id="d8c0e-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8c0e-116">Se også</span><span class="sxs-lookup"><span data-stu-id="d8c0e-116">See Also</span></span>  
 <span data-ttu-id="d8c0e-117">[Produksjon](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d8c0e-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="d8c0e-118">Definere produksjon</span><span class="sxs-lookup"><span data-stu-id="d8c0e-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="d8c0e-119">[Planlegging](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d8c0e-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="d8c0e-120">Lager</span><span class="sxs-lookup"><span data-stu-id="d8c0e-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="d8c0e-121">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d8c0e-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="d8c0e-122">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8c0e-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
