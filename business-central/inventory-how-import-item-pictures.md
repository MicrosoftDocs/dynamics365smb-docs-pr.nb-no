---
title: Importere mange varebilder fra en ZIP-fil | Microsoft Docs
description: Du kan importere flere varebilder på én gang. Bare gi bildefilene navn som svarer til dine varenumre, komprimer dem til en zip-fil, og bruk Importer varebilder-siden til å behandle hvilke varebilder som skal importeres.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243069"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="fee49-104">Importere flere varebilder</span><span class="sxs-lookup"><span data-stu-id="fee49-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="fee49-105">Du kan importere flere varebilder på én gang.</span><span class="sxs-lookup"><span data-stu-id="fee49-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="fee49-106">Bare gi bildefilene navn som svarer til dine varenumre, komprimer dem til en zip-fil, og bruk **Importer varebilder**-siden til å behandle hvilke varebilder som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="fee49-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="fee49-107">Alle vanlige filformater støttes.</span><span class="sxs-lookup"><span data-stu-id="fee49-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="fee49-108">Navngi bildefiler etter varenavn og klargjøre zip-filen</span><span class="sxs-lookup"><span data-stu-id="fee49-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="fee49-109">På lokasjonen der varebildene lagres, navngir du hver fil i henhold til nummeret på den tilknyttede varen.</span><span class="sxs-lookup"><span data-stu-id="fee49-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="fee49-110">Eksempel:</span><span class="sxs-lookup"><span data-stu-id="fee49-110">For example:</span></span>

    |<span data-ttu-id="fee49-111">Varenr.</span><span class="sxs-lookup"><span data-stu-id="fee49-111">Item No.</span></span>|<span data-ttu-id="fee49-112">Filnavn</span><span class="sxs-lookup"><span data-stu-id="fee49-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="fee49-113">1000</span><span class="sxs-lookup"><span data-stu-id="fee49-113">1000</span></span>|<span data-ttu-id="fee49-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="fee49-114">1000.bmp</span></span>|
    |<span data-ttu-id="fee49-115">1001</span><span class="sxs-lookup"><span data-stu-id="fee49-115">1001</span></span>|<span data-ttu-id="fee49-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="fee49-116">1001.bmp</span></span>|
    |<span data-ttu-id="fee49-117">1002</span><span class="sxs-lookup"><span data-stu-id="fee49-117">1002</span></span>|<span data-ttu-id="fee49-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="fee49-118">1002.bmp</span></span>|

2. <span data-ttu-id="fee49-119">Samle alle filer i en zip-fil.</span><span class="sxs-lookup"><span data-stu-id="fee49-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="fee49-120">For eksempel i Windows Explorer velger du filene og deretter **Send til**, **Komprimert (zippet) mappe**.</span><span class="sxs-lookup"><span data-stu-id="fee49-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="fee49-121">Importere varebilder</span><span class="sxs-lookup"><span data-stu-id="fee49-121">To import item pictures</span></span>
1. <span data-ttu-id="fee49-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageroppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="fee49-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="fee49-123">Velg handlingen **Importer varebilder**.</span><span class="sxs-lookup"><span data-stu-id="fee49-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="fee49-124">I feltet **Velg en ZIP-fil** velger du den aktuelle zip-mappen, og deretter velger du **Åpne**-knappen.</span><span class="sxs-lookup"><span data-stu-id="fee49-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="fee49-125">Det opprettes en linje for hver vare og hvert bilde som opprettes på siden **Importer varebilder**.</span><span class="sxs-lookup"><span data-stu-id="fee49-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fee49-126">For varekort som allerede har et bilde, er det merket av for **Bildet finnes allerede**.</span><span class="sxs-lookup"><span data-stu-id="fee49-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="fee49-127">Hvis du ikke vil at eksisterende bilder skal byttes ut, fjerner du merket for **Erstatt bilder**.</span><span class="sxs-lookup"><span data-stu-id="fee49-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="fee49-128">Hvis du ikke vil at individuelle eksisterende bilder skal byttes ut, kan du slette de aktuelle linjene.</span><span class="sxs-lookup"><span data-stu-id="fee49-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="fee49-129">Velg handlingen **Importer bilder**.</span><span class="sxs-lookup"><span data-stu-id="fee49-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="fee49-130">Feltet **Importer status** oppdateres for å vise om bildeimporten ble hoppet over eller fullført.</span><span class="sxs-lookup"><span data-stu-id="fee49-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="fee49-131">Se også</span><span class="sxs-lookup"><span data-stu-id="fee49-131">See Also</span></span>
[<span data-ttu-id="fee49-132">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="fee49-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="fee49-133">Opprette nummerserier</span><span class="sxs-lookup"><span data-stu-id="fee49-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="fee49-134">Lager</span><span class="sxs-lookup"><span data-stu-id="fee49-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="fee49-135">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="fee49-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="fee49-136">Salg</span><span class="sxs-lookup"><span data-stu-id="fee49-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="fee49-137">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fee49-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
