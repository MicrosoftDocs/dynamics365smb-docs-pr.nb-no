---
title: Tilordne et prioritetsnivå til en leverandør | Microsoft-dokumentasjon
description: Du kan tilordne numre til leverandørene for å prioritere dem og forenkle betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1604113b255a585532677ccb47d7e68d1cc64059
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772782"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="b4935-103">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="b4935-103">Prioritize Vendors</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b4935-104">kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b4935-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="b4935-105">Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="b4935-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="b4935-106">Først må du prioritere leverandørene ved å tilordne numre til dem.</span><span class="sxs-lookup"><span data-stu-id="b4935-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="b4935-107">Slik prioriterer du leverandører</span><span class="sxs-lookup"><span data-stu-id="b4935-107">To prioritize vendors</span></span>
1. <span data-ttu-id="b4935-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="b4935-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="b4935-109">Velg den aktuelle leverandøren, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b4935-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="b4935-110">Angi et tall i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="b4935-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="b4935-111">vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="b4935-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="b4935-112">Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="b4935-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="b4935-113">Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="b4935-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="b4935-114">Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer.</span><span class="sxs-lookup"><span data-stu-id="b4935-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="b4935-115">Du kan angi et ubegrenset antall prioritetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="b4935-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4935-116">Se også</span><span class="sxs-lookup"><span data-stu-id="b4935-116">See Also</span></span>
[<span data-ttu-id="b4935-117">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="b4935-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="b4935-118">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="b4935-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="b4935-119">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4935-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]