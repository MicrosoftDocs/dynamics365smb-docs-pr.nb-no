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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: cb3556c9bd8fb893448d61c4e8f18131b96a9841
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802858"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="7b284-103">Prioritere leverandører</span><span class="sxs-lookup"><span data-stu-id="7b284-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7b284-104">kan foreslå ulike utbetalinger til leverandører, for eksempel betalinger som snart forfaller eller betalinger hvor en rabatt er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="7b284-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="7b284-105">Hvis du vil ha mer informasjon, kan du se [Betalingsforslag – leverandør](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="7b284-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="7b284-106">Først må du prioritere leverandørene ved å tilordne numre til dem.</span><span class="sxs-lookup"><span data-stu-id="7b284-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="7b284-107">Slik prioriterer du leverandører</span><span class="sxs-lookup"><span data-stu-id="7b284-107">To prioritize vendors</span></span>
1. <span data-ttu-id="7b284-108">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="7b284-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="7b284-109">Velg den aktuelle leverandøren, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="7b284-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="7b284-110">Angi et tall i feltet **Prioritet**.</span><span class="sxs-lookup"><span data-stu-id="7b284-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7b284-111">vurderer det laveste tallet, unntatt 0, til å ha høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="7b284-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="7b284-112">Hvis du for eksempel bruker 1, 2 og 3, har 1 høyeste prioritet.</span><span class="sxs-lookup"><span data-stu-id="7b284-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="7b284-113">Hvis du ikke vil prioritere en leverandør, lar du feltet **Prioritet** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="7b284-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="7b284-114">Når du deretter bruker funksjonen for betalingsforslag, vises leverandøren i oversikten etter alle leverandørene som har et prioritetsnummer.</span><span class="sxs-lookup"><span data-stu-id="7b284-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="7b284-115">Du kan angi et ubegrenset antall prioritetsnivåer.</span><span class="sxs-lookup"><span data-stu-id="7b284-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b284-116">Se også</span><span class="sxs-lookup"><span data-stu-id="7b284-116">See Also</span></span>
[<span data-ttu-id="7b284-117">Definere kjøp</span><span class="sxs-lookup"><span data-stu-id="7b284-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="7b284-118">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="7b284-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="7b284-119">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7b284-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
