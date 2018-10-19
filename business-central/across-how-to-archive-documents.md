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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6b1b23c062fdb1c4558a292c7aa454ae24ff3c71
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="archive-documents"></a><span data-ttu-id="48a89-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="48a89-103">Archive Documents</span></span>
<span data-ttu-id="48a89-104">Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.</span><span class="sxs-lookup"><span data-stu-id="48a89-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="48a89-105">Konfigurere automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="48a89-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="48a89-106">Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="48a89-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="48a89-107">Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="48a89-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="48a89-108">Fremgangsmåten er den samme for kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="48a89-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="48a89-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="48a89-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="48a89-110">I vinduet **Generelt bokføringsoppsett** må du fylle feltene som følger:</span><span class="sxs-lookup"><span data-stu-id="48a89-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="48a89-111">Felt</span><span class="sxs-lookup"><span data-stu-id="48a89-111">Field</span></span>|<span data-ttu-id="48a89-112">Description</span><span class="sxs-lookup"><span data-stu-id="48a89-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="48a89-113">**Arkivere tilbud**</span><span class="sxs-lookup"><span data-stu-id="48a89-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="48a89-114">**Aldri** for aldri å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="48a89-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="48a89-115">**Spørsmål** for å spørre brukeren om å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="48a89-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="48a89-116">**Alltid** for å arkivere tilbud automatisk når de slettes.</span><span class="sxs-lookup"><span data-stu-id="48a89-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="48a89-117">**Arkivere rammeordrer**</span><span class="sxs-lookup"><span data-stu-id="48a89-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="48a89-118">Velg for å arkivere rammeordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="48a89-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="48a89-119">**Arkivere ordrer og best.returer**</span><span class="sxs-lookup"><span data-stu-id="48a89-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="48a89-120">Velg for å arkivere ordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="48a89-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="48a89-121">Arkivere ordrer</span><span class="sxs-lookup"><span data-stu-id="48a89-121">To archive a sales order</span></span>
<span data-ttu-id="48a89-122">Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="48a89-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="48a89-123">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="48a89-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="48a89-124">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="48a89-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48a89-125">Åpne en ordre du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="48a89-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="48a89-126">Velg handlingen **Arkiver dokument**.</span><span class="sxs-lookup"><span data-stu-id="48a89-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="48a89-127">Ordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="48a89-127">The sales order is archived.</span></span> <span data-ttu-id="48a89-128">Du kan se den i vinduet **Arkiverte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="48a89-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="48a89-129">Herfra kan du også bruke det til å opprette ordren på nytt som den ble arkivert fra.</span><span class="sxs-lookup"><span data-stu-id="48a89-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="48a89-130">Opprette en ordre fra arkivet</span><span class="sxs-lookup"><span data-stu-id="48a89-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="48a89-131">Fremgangsmåten nedenfor beskriver hvordan du oppretter en ordre på nytt.</span><span class="sxs-lookup"><span data-stu-id="48a89-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="48a89-132">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="48a89-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="48a89-133">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Arkiverte ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="48a89-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="48a89-134">Velg den arkiverte ordren som skal opprettes på nytt, og velg deretter **Gjenopprett**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="48a89-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="48a89-135">Ordren opprettes og legges til i vinduet **Ordrer**.</span><span class="sxs-lookup"><span data-stu-id="48a89-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="48a89-136">Slette arkiverte ordrer</span><span class="sxs-lookup"><span data-stu-id="48a89-136">To delete archived sales orders</span></span>
<span data-ttu-id="48a89-137">Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer.</span><span class="sxs-lookup"><span data-stu-id="48a89-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="48a89-138">Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="48a89-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="48a89-139">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Slett arkiverte ordreversjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="48a89-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="48a89-140">I vinduet **Slett arkiverte ordreversjoner** velger du de aktuelle filtrene.</span><span class="sxs-lookup"><span data-stu-id="48a89-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="48a89-141">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="48a89-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="48a89-142">Se også</span><span class="sxs-lookup"><span data-stu-id="48a89-142">See Also</span></span>
[<span data-ttu-id="48a89-143">Spore dokumentlinje</span><span class="sxs-lookup"><span data-stu-id="48a89-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="48a89-144">Salg</span><span class="sxs-lookup"><span data-stu-id="48a89-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="48a89-145">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="48a89-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="48a89-146">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="48a89-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

