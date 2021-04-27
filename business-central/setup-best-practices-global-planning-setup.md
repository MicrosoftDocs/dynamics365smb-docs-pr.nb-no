---
title: Anbefalte fremgangsmåter for globalt planleggingsoppsett | Microsoft-dokumentasjon
description: Hurtigfanen Planlegging på siden Produksjonsoppsett inneholder flere felt som definerer globale regler for forsyningsplanlegging.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c91bde42378992ef1c1e9613fb94d9bac2d4f57c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785351"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="e8d99-103">Anbefalte fremgangsmåter for oppsett: Oppsett for global planlegging</span><span class="sxs-lookup"><span data-stu-id="e8d99-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="e8d99-104">Hurtigfanen **Planlegging** på siden **Produksjonsoppsett** inneholder flere felt som definerer globale regler for forsyningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="e8d99-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="e8d99-105">Tabellen nedenfor inneholder anbefalte fremgangsmåter for hvordan du konfigurerer valgte globale planleggingsparameterfelt.</span><span class="sxs-lookup"><span data-stu-id="e8d99-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="e8d99-106">Hvis du vil ha mer informasjon om et felt, velger du koblingen i kolonnen **Oppsettfelt**.</span><span class="sxs-lookup"><span data-stu-id="e8d99-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="e8d99-107">Oppsettfelt</span><span class="sxs-lookup"><span data-stu-id="e8d99-107">Setup field</span></span>|<span data-ttu-id="e8d99-108">Anbefalt fremgangsmåte</span><span class="sxs-lookup"><span data-stu-id="e8d99-108">Best practice</span></span>|<span data-ttu-id="e8d99-109">Merknad</span><span class="sxs-lookup"><span data-stu-id="e8d99-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="e8d99-110">Bruk prognose på lokasjoner</span><span class="sxs-lookup"><span data-stu-id="e8d99-110">Use Forecast on Locations</span></span>|<span data-ttu-id="e8d99-111">Velg dette alternativet hvis du har prognoser for bestemte plasseringer.</span><span class="sxs-lookup"><span data-stu-id="e8d99-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="e8d99-112">Komponenter ved lokasjon</span><span class="sxs-lookup"><span data-stu-id="e8d99-112">Components at Location</span></span>|<span data-ttu-id="e8d99-113">Hvis varene ikke er definert som lagerføringsenheter, velger du lokasjonskoden for hovedlageret.</span><span class="sxs-lookup"><span data-stu-id="e8d99-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="e8d99-114">Dette gjelder også hvis du bare bruker bestillingsforslaget.</span><span class="sxs-lookup"><span data-stu-id="e8d99-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="e8d99-115">Tomt overflytnivå</span><span class="sxs-lookup"><span data-stu-id="e8d99-115">Blank Overflow Level</span></span>|<span data-ttu-id="e8d99-116">Velg **Tillat standardberegning** hvis du migrerer fra Microsoft Dynamics NAV 5.0 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="e8d99-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="e8d99-117">Bruk bare hvis du vil tillate at alle eller noen av varene flyter over gjenbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="e8d99-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="e8d99-118">Standard avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="e8d99-118">Default Dampener Period</span></span>|<span data-ttu-id="e8d99-119">Velg mellom 1D og 5D.</span><span class="sxs-lookup"><span data-stu-id="e8d99-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="e8d99-120">Hvis planlegging er nytt for brukerne i [!INCLUDE[prod_short](includes/prod_short.md)], angir du en lengre periode.</span><span class="sxs-lookup"><span data-stu-id="e8d99-120">If new to planning in [!INCLUDE[prod_short](includes/prod_short.md)], then set a longer period.</span></span>|<span data-ttu-id="e8d99-121">Når brukere har satt seg bedre inn i de forskjellige årsakene til handlingsmeldinger, kan avdempingsperioden forkortes for å tillate flere endringsforslag.</span><span class="sxs-lookup"><span data-stu-id="e8d99-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="e8d99-122">Standard avdempingsantall %</span><span class="sxs-lookup"><span data-stu-id="e8d99-122">Default Dampener Quantity %</span></span>|<span data-ttu-id="e8d99-123">Angi mellom 5 og 20 prosent av varens partistørrelse.</span><span class="sxs-lookup"><span data-stu-id="e8d99-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="e8d99-124">Se også</span><span class="sxs-lookup"><span data-stu-id="e8d99-124">See Also</span></span>  
 <span data-ttu-id="e8d99-125">[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e8d99-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="e8d99-126">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="e8d99-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="e8d99-127">Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="e8d99-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="e8d99-128">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e8d99-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]