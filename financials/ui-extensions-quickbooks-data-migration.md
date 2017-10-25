---
title: Bruke QuickBooks Migration-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4775c945a7721b8f4e52a187840a585396611e47
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="c1a43-103">Utvidelsen QuickBooks Data Migration for Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="c1a43-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="c1a43-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks Desktop til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1a43-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks Desktop to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c1a43-105">Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1a43-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="c1a43-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="c1a43-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="c1a43-107">Eksportere data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="c1a43-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="c1a43-108">Du må ha eksportert noen eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="c1a43-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="c1a43-109">QuickBooks Data Migration-utvidelsen inneholder en standard tilordning av QuickBooks-data, slik at du kan bruke de eksisterende dataene til å teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="c1a43-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="c1a43-110">Standardtilordningen vil være tilstrekkelig i de aller fleste tilfeller, men du kan endre tilordningen i den assistert oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="c1a43-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="c1a43-111">I QuickBooks inneholder Fil-menyen et verktøy for å eksportere lister.</span><span class="sxs-lookup"><span data-stu-id="c1a43-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="c1a43-112">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:</span><span class="sxs-lookup"><span data-stu-id="c1a43-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="c1a43-113">Kundeoversikt</span><span class="sxs-lookup"><span data-stu-id="c1a43-113">Customer List</span></span>  
* <span data-ttu-id="c1a43-114">Leverandøroversikt</span><span class="sxs-lookup"><span data-stu-id="c1a43-114">Vendor List</span></span>  
* <span data-ttu-id="c1a43-115">Vareoversikt</span><span class="sxs-lookup"><span data-stu-id="c1a43-115">Item List</span></span>  
* <span data-ttu-id="c1a43-116">Kontooversikt</span><span class="sxs-lookup"><span data-stu-id="c1a43-116">Account List</span></span>  

<span data-ttu-id="c1a43-117">De eksporterte dataene lagres som en IIF-fil som du deretter kan laste opp til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1a43-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="c1a43-118">Finne QuickBooks Data Migration-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="c1a43-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="c1a43-119">Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering.</span><span class="sxs-lookup"><span data-stu-id="c1a43-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="c1a43-120">Hvis du er klar til å komme i gang nå og har eksportert dataene fra QuickBooks, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angir **Automatisk oppsett**, og velger deretter den tilknyttede koblingen.</span><span class="sxs-lookup"><span data-stu-id="c1a43-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="c1a43-121">Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="c1a43-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c1a43-122">Se også</span><span class="sxs-lookup"><span data-stu-id="c1a43-122">See Also</span></span>
[<span data-ttu-id="c1a43-123">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="c1a43-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="c1a43-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c1a43-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

