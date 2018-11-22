---
title: Definere gjentakelsesordrer
description: "Når du har opprettet en gjentakelsesgruppe, kan du definere gjentakelsesordrer for rammeordren ved å legge til gruppen i ordren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: 6a4b7e839be68151eaeb73d6003739f9bb30e60e
ms.contentlocale: nb-no
ms.lasthandoff: 10/15/2018

---
# <a name="set-up-recurring-orders"></a><span data-ttu-id="c22ab-103">Definere gjentakelsesordrer</span><span class="sxs-lookup"><span data-stu-id="c22ab-103">Set Up Recurring Orders</span></span>
<span data-ttu-id="c22ab-104">Når du har opprettet en gjentakelsesgruppe, kan du definere gjentakelsesordrer for rammeordren ved å legge til gruppen i ordren.</span><span class="sxs-lookup"><span data-stu-id="c22ab-104">After you create a recurring group, you can set up recurring orders on the blanket sales order by adding the group to the order.</span></span> <span data-ttu-id="c22ab-105">Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](how-to-set-up-recurring-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c22ab-105">For more information, see [Create Blanket Sales Orders](how-to-set-up-recurring-groups.md).</span></span>  

## <a name="to-set-up-a-recurring-order"></a><span data-ttu-id="c22ab-106">Slik definerer du en gjentakelsesordre</span><span class="sxs-lookup"><span data-stu-id="c22ab-106">To set up a recurring order</span></span>  

1.  <span data-ttu-id="c22ab-107">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Rammeordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c22ab-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c22ab-108">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c22ab-108">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="c22ab-109">I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c22ab-109">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c22ab-110">Felt</span><span class="sxs-lookup"><span data-stu-id="c22ab-110">Field</span></span>|<span data-ttu-id="c22ab-111">Description</span><span class="sxs-lookup"><span data-stu-id="c22ab-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c22ab-112">**Ordredato**</span><span class="sxs-lookup"><span data-stu-id="c22ab-112">**Order Date**</span></span>|<span data-ttu-id="c22ab-113">Angi ordredatoen.</span><span class="sxs-lookup"><span data-stu-id="c22ab-113">Enter the order date.</span></span> <span data-ttu-id="c22ab-114">Ordredatoen benytter du når du oppretter nye gjentakelsesordrer.</span><span class="sxs-lookup"><span data-stu-id="c22ab-114">The order date is used when you create new recurring orders.</span></span> <span data-ttu-id="c22ab-115">Ordrer med en ordredato som faller på behandlingsdatoen eller tidligere, blir behandlet.</span><span class="sxs-lookup"><span data-stu-id="c22ab-115">Orders with an order date on or before the processing date are processed.</span></span>|  
    |<span data-ttu-id="c22ab-116">**Kode for gjentakelsesgruppe**</span><span class="sxs-lookup"><span data-stu-id="c22ab-116">**Recurring Group Code**</span></span>|<span data-ttu-id="c22ab-117">Angi koden for gjentakelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="c22ab-117">Enter the recurring group code for the recurring group.</span></span> <span data-ttu-id="c22ab-118">Hvis en rammeordre inneholder en gjentakelsesgruppekode, er rammeordren tilgjengelig som en gjentakelsesordre.</span><span class="sxs-lookup"><span data-stu-id="c22ab-118">When a blanket order contains a recurring group code, the blanket order is available as a recurring order.</span></span>|  

4.  <span data-ttu-id="c22ab-119">I hurtigfanen **Linjer** fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="c22ab-119">On the **Lines** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c22ab-120">Felt</span><span class="sxs-lookup"><span data-stu-id="c22ab-120">Field</span></span>|<span data-ttu-id="c22ab-121">Description</span><span class="sxs-lookup"><span data-stu-id="c22ab-121">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c22ab-122">**Antall**</span><span class="sxs-lookup"><span data-stu-id="c22ab-122">**Quantity**</span></span>|<span data-ttu-id="c22ab-123">Angi antall for rammeordren.</span><span class="sxs-lookup"><span data-stu-id="c22ab-123">Enter the quantity for the blanket order.</span></span>|  
    |<span data-ttu-id="c22ab-124">**Levere (antall)**</span><span class="sxs-lookup"><span data-stu-id="c22ab-124">**Qty. to Ship**</span></span>|<span data-ttu-id="c22ab-125">Angi antallet som skal leveres.</span><span class="sxs-lookup"><span data-stu-id="c22ab-125">Enter the quantity to ship.</span></span> <span data-ttu-id="c22ab-126">Dette antallet benyttes når du oppretter nye ordrer som gjentakelsesordrer.</span><span class="sxs-lookup"><span data-stu-id="c22ab-126">This quantity is used when you create new orders as recurring orders.</span></span>|  

5.  <span data-ttu-id="c22ab-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="c22ab-127">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c22ab-128">Se også</span><span class="sxs-lookup"><span data-stu-id="c22ab-128">See Also</span></span>  
 <span data-ttu-id="c22ab-129">[Gjentakelsesordrer](recurring-orders.md) </span><span class="sxs-lookup"><span data-stu-id="c22ab-129">[Recurring Orders](recurring-orders.md) </span></span>  
 <span data-ttu-id="c22ab-130">[Opprette gjentakelsesgrupper](how-to-set-up-recurring-groups.md) </span><span class="sxs-lookup"><span data-stu-id="c22ab-130">[Set Up Recurring Groups](how-to-set-up-recurring-groups.md) </span></span>  
 <span data-ttu-id="c22ab-131">[Opprett gjentakelsesordrer](how-to-create-recurring-orders.md) </span><span class="sxs-lookup"><span data-stu-id="c22ab-131">[Create Recurring Orders](how-to-create-recurring-orders.md) </span></span>  
 [<span data-ttu-id="c22ab-132">Arbeide med rammeordrer</span><span class="sxs-lookup"><span data-stu-id="c22ab-132">Work with Blanket Sales Orders</span></span>](../../sales-how-to-create-blanket-sales-orders.md)
