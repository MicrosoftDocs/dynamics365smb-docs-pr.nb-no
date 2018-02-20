---
title: Bruke QuickBooks Migration-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Finance and Operations, Business edition."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 14e0aea700bbb46a612d8e462ace22b10faac7e2
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="the-quickbooks-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="ea7e5-103">QuickBooks Data Migration-utvidelsen for Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="ea7e5-103">The QuickBooks Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="ea7e5-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ea7e5-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ea7e5-105">Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ea7e5-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="ea7e5-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="ea7e5-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="ea7e5-107">Eksportere data fra QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="ea7e5-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="ea7e5-108">Du må ha eksportert noen eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="ea7e5-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="ea7e5-109">QuickBooks Data Migration-utvidelsen inneholder en standard tilordning av QuickBooks-data, slik at du kan bruke de eksisterende dataene til å teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="ea7e5-110">Standardtilordningen vil være tilstrekkelig i de aller fleste tilfeller, men du kan endre tilordningen i den assistert oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="ea7e5-111">I QuickBooks inneholder Fil-menyen et verktøy for å eksportere lister.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="ea7e5-112">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:</span><span class="sxs-lookup"><span data-stu-id="ea7e5-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="ea7e5-113">Kundeoversikt</span><span class="sxs-lookup"><span data-stu-id="ea7e5-113">Customer List</span></span>  
* <span data-ttu-id="ea7e5-114">Leverandøroversikt</span><span class="sxs-lookup"><span data-stu-id="ea7e5-114">Vendor List</span></span>  
* <span data-ttu-id="ea7e5-115">Vareoversikt</span><span class="sxs-lookup"><span data-stu-id="ea7e5-115">Item List</span></span>  
* <span data-ttu-id="ea7e5-116">Kontooversikt</span><span class="sxs-lookup"><span data-stu-id="ea7e5-116">Account List</span></span>  

<span data-ttu-id="ea7e5-117">De eksporterte dataene lagres som en IIF-fil som du deretter kan laste opp til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ea7e5-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="ea7e5-118">Finne QuickBooks Data Migration-utvidelsen</span><span class="sxs-lookup"><span data-stu-id="ea7e5-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="ea7e5-119">Utvidelsen Datamigrering for QuickBooks er installert og klar som en integrert del av den assisterte oppsettsveiledningen for datamigrering.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="ea7e5-120">Hvis du er klar til å komme i gang nå og har eksportert dataene fra QuickBooks, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir **Automatisk oppsett**, og velger deretter den tilknyttede koblingen.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="ea7e5-121">Velg **Overfør forretningsdata**, og følg trinnene i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="ea7e5-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea7e5-122">Se også</span><span class="sxs-lookup"><span data-stu-id="ea7e5-122">See Also</span></span>
[<span data-ttu-id="ea7e5-123">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="ea7e5-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="ea7e5-124">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ea7e5-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

