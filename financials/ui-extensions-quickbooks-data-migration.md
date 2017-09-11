---
title: Bruke QuickBooks Migration-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker utvidelsen til å importere kunder, leverandører, varer og konti fra QuickBooks Desktop til Dynamics 365 for Financials."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="70fd7-103">Utvidelsen QuickBooks Data Migration for Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="70fd7-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="70fd7-104">Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra QuickBooks til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="70fd7-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="70fd7-105">Hvis virksomheten din bruker QuickBooks i dag, kan du eksportere relevant informasjon og deretter åpner en assistert oppsettsveiledning for å laste opp data til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="70fd7-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="70fd7-106">Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="70fd7-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="70fd7-107">Eksportere data fra QuickBooks</span><span class="sxs-lookup"><span data-stu-id="70fd7-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="70fd7-108">Du må ha eksportert noen eller alle eksisterende kunder, leverandører, lagervarer og konti til en IIF-fil (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="70fd7-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="70fd7-109">QuickBooks Data Migration-utvidelsen inneholder en standard tilordning av QuickBooks-data, slik at du kan bruke de eksisterende dataene til å teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet.</span><span class="sxs-lookup"><span data-stu-id="70fd7-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="70fd7-110">Standardtilordningen vil være tilstrekkelig i de aller fleste tilfeller, men du kan endre tilordningen i den assistert oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="70fd7-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="70fd7-111">I QuickBooks inneholder Fil-menyen et verktøy for å eksportere lister.</span><span class="sxs-lookup"><span data-stu-id="70fd7-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="70fd7-112">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende lister:</span><span class="sxs-lookup"><span data-stu-id="70fd7-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="70fd7-113">Kundeoversikt</span><span class="sxs-lookup"><span data-stu-id="70fd7-113">Customer List</span></span>  
* <span data-ttu-id="70fd7-114">Leverandøroversikt</span><span class="sxs-lookup"><span data-stu-id="70fd7-114">Vendor List</span></span>  
* <span data-ttu-id="70fd7-115">Vareoversikt</span><span class="sxs-lookup"><span data-stu-id="70fd7-115">Item List</span></span>  
* <span data-ttu-id="70fd7-116">Kontooversikt</span><span class="sxs-lookup"><span data-stu-id="70fd7-116">Account List</span></span>  

<span data-ttu-id="70fd7-117">De eksporterte dataene lagres som en IIF-fil som du deretter kan laste opp til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="70fd7-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="70fd7-118">Se også</span><span class="sxs-lookup"><span data-stu-id="70fd7-118">See Also</span></span>
[<span data-ttu-id="70fd7-119">Importere forretningsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="70fd7-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="70fd7-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="70fd7-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

