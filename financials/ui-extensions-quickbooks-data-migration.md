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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: fdda803b7cc2f93ae4d7353be28282dc60d904d8
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-business-edition"></a><span data-ttu-id="50975-103">Utvidelsen Datamigrering for QuickBooks for Dynamics 365 Business edition</span><span class="sxs-lookup"><span data-stu-id="50975-103">The QuickBooks Data Migration Extension for Dynamics 365 Business edition</span></span>
<span data-ttu-id="50975-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50975-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="50975-105">Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50975-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="50975-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="50975-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="50975-107">Eksportere data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="50975-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="50975-108">Du må ha eksportert noen eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="50975-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="50975-109">QuickBooks Data Migration-utvidelsen inneholder en standard tilordning av QuickBooks-data, slik at du kan bruke de eksisterende dataene til å teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="50975-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="50975-110">Standardtilordningen vil være tilstrekkelig i de aller fleste tilfeller, men du kan endre tilordningen i den assistert oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="50975-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="50975-111">I QuickBooks inneholder Fil-menyen et verktøy for å eksportere lister.</span><span class="sxs-lookup"><span data-stu-id="50975-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="50975-112">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:</span><span class="sxs-lookup"><span data-stu-id="50975-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="50975-113">Kundeoversikt</span><span class="sxs-lookup"><span data-stu-id="50975-113">Customer List</span></span>  
* <span data-ttu-id="50975-114">Leverandøroversikt</span><span class="sxs-lookup"><span data-stu-id="50975-114">Vendor List</span></span>  
* <span data-ttu-id="50975-115">Vareoversikt</span><span class="sxs-lookup"><span data-stu-id="50975-115">Item List</span></span>  
* <span data-ttu-id="50975-116">Kontooversikt</span><span class="sxs-lookup"><span data-stu-id="50975-116">Account List</span></span>  

<span data-ttu-id="50975-117">De eksporterte dataene lagres som en IIF-fil som du deretter kan laste opp til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="50975-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="50975-118">Finne QuickBooks Data Migration-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="50975-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="50975-119">Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering.</span><span class="sxs-lookup"><span data-stu-id="50975-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="50975-120">Hvis du er klar til å komme i gang nå og har eksportert dataene fra QuickBooks, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir **Automatisk oppsett**, og velger deretter den tilknyttede koblingen.</span><span class="sxs-lookup"><span data-stu-id="50975-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="50975-121">Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="50975-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="50975-122">Se også</span><span class="sxs-lookup"><span data-stu-id="50975-122">See Also</span></span>
[<span data-ttu-id="50975-123">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="50975-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="50975-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="50975-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

