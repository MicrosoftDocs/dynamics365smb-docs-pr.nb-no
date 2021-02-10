---
title: Arkivere salgs- og kjøpsdokumenter | Microsoft-dokumentasjon
description: Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c7f7da76bdea02f640bdb0ffaf5f1b8da16494cf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754870"
---
# <a name="archive-documents"></a><span data-ttu-id="786dd-103">Arkivere dokumenter</span><span class="sxs-lookup"><span data-stu-id="786dd-103">Archive Documents</span></span>
<span data-ttu-id="786dd-104">Du kan arkivere ordrer, bestillinger, tilbud, ordrereturer og rammebestillinger, for eksempel fordi du vil lagre en kopi av et dokument til bruk senere.</span><span class="sxs-lookup"><span data-stu-id="786dd-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, for example because you want to save a copy of a document for reuse later.</span></span> <span data-ttu-id="786dd-105">Du arkivere et salgs- eller kjøpsdokument flere ganger og lagre en annen arkiverte versjon hver gang.</span><span class="sxs-lookup"><span data-stu-id="786dd-105">You can archive a sales or purchase document several times, saving a different archived version each time.</span></span>

<span data-ttu-id="786dd-106">For arkiverte dokumenter der originalen fortsatt finnes og ikke er bokført, kan du bruke funksjonen **Gjenopprett** til å overskrive originalen med den arkiverte versjonen av dokumentet.</span><span class="sxs-lookup"><span data-stu-id="786dd-106">For archived documents where the original still exists and is not posted, you can use the **Restore** function to overwrite the original with the archived version of the document.</span></span> <span data-ttu-id="786dd-107">Dette er nyttig hvis du trenger å gjenopprette innholdet i et dokument til en tidligere tilstand.</span><span class="sxs-lookup"><span data-stu-id="786dd-107">This is practical if you need to restore the contents of a document to an earlier state.</span></span>

<span data-ttu-id="786dd-108">For arkiverte dokumenter der originalen er slettet, kan du bare bruke innholdet på nytt ved å kopiere dataene, for eksempel med funksjonen **Kopier fra dokument**.</span><span class="sxs-lookup"><span data-stu-id="786dd-108">For archived documents where the original is deleted, you can only reuse the content by copying the data, for example with the **Copy from Document** function.</span></span>   

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="786dd-109">Konfigurere automatisk dokumentarkivering</span><span class="sxs-lookup"><span data-stu-id="786dd-109">To set up automatic document archiving</span></span>  
<span data-ttu-id="786dd-110">Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.</span><span class="sxs-lookup"><span data-stu-id="786dd-110">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="786dd-111">Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="786dd-111">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="786dd-112">Fremgangsmåten er den samme for kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="786dd-112">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="786dd-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="786dd-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="786dd-114">På siden **Generelt bokføringsoppsett** må du fylle ut følgende felt.</span><span class="sxs-lookup"><span data-stu-id="786dd-114">On the **Sales & Receivables Setup** page, fill in the fields as follows.</span></span>

|<span data-ttu-id="786dd-115">Felt</span><span class="sxs-lookup"><span data-stu-id="786dd-115">Field</span></span>|<span data-ttu-id="786dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="786dd-116">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="786dd-117">**Arkivere tilbud**</span><span class="sxs-lookup"><span data-stu-id="786dd-117">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="786dd-118">**Aldri** for aldri å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="786dd-118">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="786dd-119">**Spørsmål** for å spørre brukeren om å arkivere tilbud når de slettes.</span><span class="sxs-lookup"><span data-stu-id="786dd-119">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="786dd-120">**Alltid** for å arkivere tilbud automatisk når de slettes.</span><span class="sxs-lookup"><span data-stu-id="786dd-120">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="786dd-121">**Arkivere rammeordrer**</span><span class="sxs-lookup"><span data-stu-id="786dd-121">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="786dd-122">Velg for å arkivere rammeordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="786dd-122">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="786dd-123">**Arkivere ordrer og best.returer**</span><span class="sxs-lookup"><span data-stu-id="786dd-123">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="786dd-124">Velg for å arkivere ordrer automatisk hver gang de slettes.</span><span class="sxs-lookup"><span data-stu-id="786dd-124">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="786dd-125">Arkivere ordrer</span><span class="sxs-lookup"><span data-stu-id="786dd-125">To archive a sales order</span></span>
<span data-ttu-id="786dd-126">Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer.</span><span class="sxs-lookup"><span data-stu-id="786dd-126">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="786dd-127">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="786dd-127">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="786dd-128">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="786dd-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="786dd-129">Åpne en ordre du vil arkivere.</span><span class="sxs-lookup"><span data-stu-id="786dd-129">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="786dd-130">Velg handlingen **Arkiver dokument**.</span><span class="sxs-lookup"><span data-stu-id="786dd-130">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="786dd-131">Ordren arkiveres.</span><span class="sxs-lookup"><span data-stu-id="786dd-131">The sales order is archived.</span></span> <span data-ttu-id="786dd-132">Du kan se den på siden **Arkiverte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="786dd-132">You can view it on the **Archived Sales Orders** page.</span></span>

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a><span data-ttu-id="786dd-133">Slik gjenoppretter du salgordrer som ikke er bokført, fra arkivet</span><span class="sxs-lookup"><span data-stu-id="786dd-133">To restore a non-posted sales order from the archive</span></span>
<span data-ttu-id="786dd-134">Følgende fremgangsmåte beskriver hvordan du tar innholdet i en arkivert ordre tilbake den opprinnelige ordren.</span><span class="sxs-lookup"><span data-stu-id="786dd-134">The following procedure describes how to bring the contents of an archived sales order back to the original sales order.</span></span> <span data-ttu-id="786dd-135">Dette er bare mulig når det opprinnelige dokumentet ikke er bokført.</span><span class="sxs-lookup"><span data-stu-id="786dd-135">This is only possible when the original document has not been posted.</span></span> <span data-ttu-id="786dd-136">Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.</span><span class="sxs-lookup"><span data-stu-id="786dd-136">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1. <span data-ttu-id="786dd-137">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arkiverte ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="786dd-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="786dd-138">Velg den arkiverte ordren, eller versjonen av den, som du vil gjenopprette, og velg deretter **Gjenopprett**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="786dd-138">Select the archived sales order, or version of it, that you want to restore, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="786dd-139">Innholdet i den opprinnelige ordren erstattes med den valgte arkiverte versjonen.</span><span class="sxs-lookup"><span data-stu-id="786dd-139">The contents of the original sales order is replaced with that of the selected archived version.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="786dd-140">Slette arkiverte ordrer</span><span class="sxs-lookup"><span data-stu-id="786dd-140">To delete archived sales orders</span></span>
<span data-ttu-id="786dd-141">Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer.</span><span class="sxs-lookup"><span data-stu-id="786dd-141">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="786dd-142">Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="786dd-142">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="786dd-143">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett arkiverte ordreversjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="786dd-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="786dd-144">På siden **Slett arkiverte ordreversjoner** velger du de aktuelle filtrene.</span><span class="sxs-lookup"><span data-stu-id="786dd-144">On the **Delete Archived Sales Order Versions** page, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="786dd-145">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="786dd-145">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="786dd-146">Se også</span><span class="sxs-lookup"><span data-stu-id="786dd-146">See Also</span></span>
[<span data-ttu-id="786dd-147">Spore dokumentlinje</span><span class="sxs-lookup"><span data-stu-id="786dd-147">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="786dd-148">Salg</span><span class="sxs-lookup"><span data-stu-id="786dd-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="786dd-149">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="786dd-149">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="786dd-150">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="786dd-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
