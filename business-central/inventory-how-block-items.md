---
title: Slik sperrer du varer fra salg eller kjøp
description: I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c98e4b893783c795a49e05ab04dc70b03161c6a
ms.sourcegitcommit: bf5f89dfaf5ad9f8f9902941cf3dac3e9f3553e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594256"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="78936-103">Blokkere varer fra salg eller kjøp</span><span class="sxs-lookup"><span data-stu-id="78936-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="78936-104">Du kan blokkere en vare fra å bli lagt inn på salgs- eller bestillingslinjene, og du kan blokkere den fra å bli bokført i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="78936-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="78936-105">Tabellen nedenfor viser hva som skjer når varer er sperret.</span><span class="sxs-lookup"><span data-stu-id="78936-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="78936-106">Alternativ</span><span class="sxs-lookup"><span data-stu-id="78936-106">Option</span></span>|<span data-ttu-id="78936-107">Description</span><span class="sxs-lookup"><span data-stu-id="78936-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="78936-108">**Sperret salg**</span><span class="sxs-lookup"><span data-stu-id="78936-108">**Sales Blocked**</span></span>|<span data-ttu-id="78936-109">Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.</span><span class="sxs-lookup"><span data-stu-id="78936-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="78936-110">**Innkjøp blokkert**</span><span class="sxs-lookup"><span data-stu-id="78936-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="78936-111">Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="78936-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="78936-112">**Sperret**</span><span class="sxs-lookup"><span data-stu-id="78936-112">**Blocked**</span></span>|<span data-ttu-id="78936-113">Du kan ikke bruke varen til noen varetransaksjon.</span><span class="sxs-lookup"><span data-stu-id="78936-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="78936-114">Sperrede varer kan returneres.</span><span class="sxs-lookup"><span data-stu-id="78936-114">Blocked items can be returned.</span></span> <span data-ttu-id="78936-115">Dette betyr at ingen av innstillingene ovenfor gjelder når varen brukes i returordrer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="78936-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="78936-116">Sperre en vare fra å legges inn på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="78936-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="78936-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="78936-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="78936-118">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.</span><span class="sxs-lookup"><span data-stu-id="78936-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="78936-119">Hvis du prøver å angi varen i et salgsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="78936-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="78936-120">Sperre en vare fra å legges inn på kjøpslinjer</span><span class="sxs-lookup"><span data-stu-id="78936-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="78936-121">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="78936-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="78936-122">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.</span><span class="sxs-lookup"><span data-stu-id="78936-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="78936-123">Hvis du prøver å angi varen i et kjøpsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.</span><span class="sxs-lookup"><span data-stu-id="78936-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="78936-124">Sperre en vare fra å bli bokført</span><span class="sxs-lookup"><span data-stu-id="78936-124">To block an item from being posted</span></span>
1. <span data-ttu-id="78936-125">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="78936-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="78936-126">Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.</span><span class="sxs-lookup"><span data-stu-id="78936-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="78936-127">Hvis du prøver å bokføre en transaksjonstype for varen, vil du få en feilmelding om at varen er sperret.</span><span class="sxs-lookup"><span data-stu-id="78936-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="78936-128">Se også</span><span class="sxs-lookup"><span data-stu-id="78936-128">See Also</span></span>  
[<span data-ttu-id="78936-129">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="78936-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="78936-130">Lager</span><span class="sxs-lookup"><span data-stu-id="78936-130">Inventory</span></span>](inventory-manage-inventory.md)  
