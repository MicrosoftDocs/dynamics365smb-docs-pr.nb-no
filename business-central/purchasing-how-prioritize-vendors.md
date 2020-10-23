---
title: Tilordne et prioritetsnivå til en leverandør | Microsoft-dokumentasjon
description: Du kan tilordne numre til leverandørene for å prioritere dem og forenkle betalingsforslag i Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 177fb324e39a59abbfc1b50e6ceaa34d4ae06f56
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926900"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="e9184-103">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="e9184-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e9184-104">kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e9184-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="e9184-105">Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="e9184-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="e9184-106">Først må du prioritere leverandørene ved å tilordne numre til dem.</span><span class="sxs-lookup"><span data-stu-id="e9184-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="e9184-107">Slik prioriterer du leverandører</span><span class="sxs-lookup"><span data-stu-id="e9184-107">To prioritize vendors</span></span>
1. <span data-ttu-id="e9184-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e9184-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="e9184-109">Velg den aktuelle leverandøren, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="e9184-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="e9184-110">Angi et tall i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="e9184-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="e9184-111">vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="e9184-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="e9184-112">Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="e9184-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="e9184-113">Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="e9184-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="e9184-114">Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer.</span><span class="sxs-lookup"><span data-stu-id="e9184-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="e9184-115">Du kan angi et ubegrenset antall prioritetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="e9184-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9184-116">Se også</span><span class="sxs-lookup"><span data-stu-id="e9184-116">See Also</span></span>
[<span data-ttu-id="e9184-117">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="e9184-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="e9184-118">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="e9184-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="e9184-119">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9184-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
