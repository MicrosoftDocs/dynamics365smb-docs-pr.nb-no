---
title: "Slik sperrer du varer fra salg eller kjøp"
description: "I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: nb-no
ms.lasthandoff: 07/31/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="24d60-103">Blokkere varer fra salg eller kjøp</span><span class="sxs-lookup"><span data-stu-id="24d60-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="24d60-104">Du kan blokkere en vare fra å bli lagt inn på salgs- eller bestillingslinjene, og du kan blokkere den fra å bli bokført i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="24d60-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="24d60-105">Tabellen nedenfor viser hva som skjer når varer er sperret.</span><span class="sxs-lookup"><span data-stu-id="24d60-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="24d60-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="24d60-106">Option</span></span>|<span data-ttu-id="24d60-107">Description</span><span class="sxs-lookup"><span data-stu-id="24d60-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="24d60-108">**Sperret salg**</span><span class="sxs-lookup"><span data-stu-id="24d60-108">**Sales Blocked**</span></span>|<span data-ttu-id="24d60-109">Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.</span><span class="sxs-lookup"><span data-stu-id="24d60-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="24d60-110">**Innkjøp blokkert**</span><span class="sxs-lookup"><span data-stu-id="24d60-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="24d60-111">Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="24d60-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="24d60-112">**Sperret**</span><span class="sxs-lookup"><span data-stu-id="24d60-112">**Blocked**</span></span>|<span data-ttu-id="24d60-113">Du kan ikke bruke varen til noen varetransaksjon.</span><span class="sxs-lookup"><span data-stu-id="24d60-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="24d60-114">Hvis du vil ha mer informasjon om sperring av en vare for alle formål, kan du se varekortet.</span><span class="sxs-lookup"><span data-stu-id="24d60-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="24d60-115">Sperre en vare fra å legges inn på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="24d60-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="24d60-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="24d60-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="24d60-117">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.</span><span class="sxs-lookup"><span data-stu-id="24d60-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="24d60-118">Hvis du prøver å angi varen i et salgsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="24d60-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="24d60-119">Sperre en vare fra å legges inn på kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="24d60-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="24d60-120">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="24d60-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="24d60-121">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.</span><span class="sxs-lookup"><span data-stu-id="24d60-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="24d60-122">Hvis du prøver å angi varen i et kjøpsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="24d60-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="24d60-123">Sperre en vare fra å bli bokført</span><span class="sxs-lookup"><span data-stu-id="24d60-123">To block an item from being posted</span></span>
1. <span data-ttu-id="24d60-124">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="24d60-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="24d60-125">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.</span><span class="sxs-lookup"><span data-stu-id="24d60-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="24d60-126">Hvis du prøver å bokføre en transaksjonstype for varen, vil du få en feilmelding om at varen er sperret.</span><span class="sxs-lookup"><span data-stu-id="24d60-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="24d60-127">Se også</span><span class="sxs-lookup"><span data-stu-id="24d60-127">See Also</span></span>  
[<span data-ttu-id="24d60-128">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="24d60-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="24d60-129">Lager</span><span class="sxs-lookup"><span data-stu-id="24d60-129">Inventory</span></span>](inventory-manage-inventory.md)  

