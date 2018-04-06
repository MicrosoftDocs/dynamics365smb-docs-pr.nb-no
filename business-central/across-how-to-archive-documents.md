---
title: "Arkivere salgs- og kjøpsdokumenter | Microsoft-dokumentasjon"
description: "Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a><span data-ttu-id="0df9d-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="0df9d-103">Archive Documents</span></span>
<span data-ttu-id="0df9d-104">Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.</span><span class="sxs-lookup"><span data-stu-id="0df9d-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="0df9d-105">Konfigurere automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="0df9d-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="0df9d-106">Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="0df9d-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="0df9d-107">Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0df9d-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="0df9d-108">Fremgangsmåten er den samme for kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0df9d-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="0df9d-109">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0df9d-110">I vinduet **Generelt bokføringsoppsett** må du fylle feltene som følger:</span><span class="sxs-lookup"><span data-stu-id="0df9d-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="0df9d-111">Felt</span><span class="sxs-lookup"><span data-stu-id="0df9d-111">Field</span></span>|<span data-ttu-id="0df9d-112">Description</span><span class="sxs-lookup"><span data-stu-id="0df9d-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="0df9d-113">**Arkivere tilbud**</span><span class="sxs-lookup"><span data-stu-id="0df9d-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="0df9d-114">**Aldri** for aldri å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="0df9d-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="0df9d-115">**Spørsmål** for å spørre brukeren om å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="0df9d-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="0df9d-116">**Alltid** for å arkivere tilbud automatisk når de slettes.</span><span class="sxs-lookup"><span data-stu-id="0df9d-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="0df9d-117">**Arkivere rammeordrer**</span><span class="sxs-lookup"><span data-stu-id="0df9d-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="0df9d-118">Velg for å arkivere rammeordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="0df9d-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="0df9d-119">**Arkivere ordrer og best.returer**</span><span class="sxs-lookup"><span data-stu-id="0df9d-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="0df9d-120">Velg for å arkivere ordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="0df9d-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="0df9d-121">Arkivere ordrer</span><span class="sxs-lookup"><span data-stu-id="0df9d-121">To archive a sales order</span></span>
<span data-ttu-id="0df9d-122">Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="0df9d-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="0df9d-123">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="0df9d-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="0df9d-124">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0df9d-125">Åpne en ordre du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="0df9d-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="0df9d-126">Velg handlingen **Arkiver dokument**.</span><span class="sxs-lookup"><span data-stu-id="0df9d-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="0df9d-127">Ordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="0df9d-127">The sales order is archived.</span></span> <span data-ttu-id="0df9d-128">Du kan se den i vinduet **Arkiverte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="0df9d-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="0df9d-129">Herfra kan du også bruke det til å opprette ordren på nytt som den ble arkivert fra.</span><span class="sxs-lookup"><span data-stu-id="0df9d-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="0df9d-130">Opprette en ordre fra arkivet</span><span class="sxs-lookup"><span data-stu-id="0df9d-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="0df9d-131">Fremgangsmåten nedenfor beskriver hvordan du oppretter en ordre på nytt.</span><span class="sxs-lookup"><span data-stu-id="0df9d-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="0df9d-132">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="0df9d-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="0df9d-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arkiverte ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="0df9d-134">Velg den arkiverte ordren som skal opprettes på nytt, og velg deretter **Gjenopprett**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="0df9d-135">Ordren opprettes og legges til i vinduet **Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="0df9d-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="0df9d-136">Slette arkiverte ordrer</span><span class="sxs-lookup"><span data-stu-id="0df9d-136">To delete archived sales orders</span></span>
<span data-ttu-id="0df9d-137">Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer.</span><span class="sxs-lookup"><span data-stu-id="0df9d-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="0df9d-138">Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0df9d-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="0df9d-139">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Slett arkiverte ordreversjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0df9d-140">I vinduet **Slett arkiverte ordreversjoner** velger du de aktuelle filtrene.</span><span class="sxs-lookup"><span data-stu-id="0df9d-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="0df9d-141">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0df9d-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="0df9d-142">Se også</span><span class="sxs-lookup"><span data-stu-id="0df9d-142">See Also</span></span>
[<span data-ttu-id="0df9d-143">Spore dokumentlinje</span><span class="sxs-lookup"><span data-stu-id="0df9d-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="0df9d-144">Salg</span><span class="sxs-lookup"><span data-stu-id="0df9d-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0df9d-145">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0df9d-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="0df9d-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0df9d-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

