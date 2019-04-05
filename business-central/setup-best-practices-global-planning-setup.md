---
title: Anbefalte fremgangsmåter for globalt planleggingsoppsett | Microsoft-dokumentasjon
description: Hurtigfanen Planlegging på siden Produksjonsoppsett inneholder flere felt som definerer globale regler for forsyningsplanlegging.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d1f6333c689d6af06d68e45104020a523be7f865
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803222"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="39c8a-103">Anbefalte fremgangsmåter for oppsett: Oppsett for global planlegging</span><span class="sxs-lookup"><span data-stu-id="39c8a-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="39c8a-104">Hurtigfanen **Planlegging** på siden **Produksjonsoppsett** inneholder flere felt som definerer globale regler for forsyningsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="39c8a-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="39c8a-105">Tabellen nedenfor inneholder anbefalte fremgangsmåter for hvordan du konfigurerer valgte globale planleggingsparameterfelt.</span><span class="sxs-lookup"><span data-stu-id="39c8a-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="39c8a-106">Hvis du vil ha mer informasjon om et felt, velger du koblingen i kolonnen **Oppsettfelt**.</span><span class="sxs-lookup"><span data-stu-id="39c8a-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="39c8a-107">Oppsettfelt</span><span class="sxs-lookup"><span data-stu-id="39c8a-107">Setup field</span></span>|<span data-ttu-id="39c8a-108">Anbefalt fremgangsmåte</span><span class="sxs-lookup"><span data-stu-id="39c8a-108">Best practice</span></span>|<span data-ttu-id="39c8a-109">Merknad</span><span class="sxs-lookup"><span data-stu-id="39c8a-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="39c8a-110">Bruk prognose på lokasjoner</span><span class="sxs-lookup"><span data-stu-id="39c8a-110">Use Forecast on Locations</span></span>|<span data-ttu-id="39c8a-111">Velg dette alternativet hvis du har prognoser for bestemte plasseringer.</span><span class="sxs-lookup"><span data-stu-id="39c8a-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="39c8a-112">Komponenter ved lokasjon</span><span class="sxs-lookup"><span data-stu-id="39c8a-112">Components at Location</span></span>|<span data-ttu-id="39c8a-113">Hvis varene ikke er definert som lagerføringsenheter, velger du lokasjonskoden for hovedlageret.</span><span class="sxs-lookup"><span data-stu-id="39c8a-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="39c8a-114">Dette gjelder også hvis du bare bruker bestillingsforslaget.</span><span class="sxs-lookup"><span data-stu-id="39c8a-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="39c8a-115">Tomt overflytnivå</span><span class="sxs-lookup"><span data-stu-id="39c8a-115">Blank Overflow Level</span></span>|<span data-ttu-id="39c8a-116">Velg **Tillat standardberegning** hvis du migrerer fra Microsoft Dynamics NAV 5.0 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="39c8a-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="39c8a-117">Bruk bare hvis du vil tillate at alle eller noen av varene flyter over gjenbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="39c8a-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="39c8a-118">Standard avdempingsperiode</span><span class="sxs-lookup"><span data-stu-id="39c8a-118">Default Dampener Period</span></span>|<span data-ttu-id="39c8a-119">Velg mellom 1D og 5D.</span><span class="sxs-lookup"><span data-stu-id="39c8a-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="39c8a-120">Hvis planlegging er nytt for brukerne i [!INCLUDE[d365fin](includes/d365fin_md.md)], angir du en lengre periode.</span><span class="sxs-lookup"><span data-stu-id="39c8a-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="39c8a-121">Når brukere har satt seg bedre inn i de forskjellige årsakene til handlingsmeldinger, kan avdempingsperioden forkortes for å tillate flere endringsforslag.</span><span class="sxs-lookup"><span data-stu-id="39c8a-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="39c8a-122">Standard avdempingsantall</span><span class="sxs-lookup"><span data-stu-id="39c8a-122">Default Dampener Quantity</span></span>|<span data-ttu-id="39c8a-123">Angi mellom 5 og 20 prosent av varens partistørrelse.</span><span class="sxs-lookup"><span data-stu-id="39c8a-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="39c8a-124">Se også</span><span class="sxs-lookup"><span data-stu-id="39c8a-124">See Also</span></span>  
 <span data-ttu-id="39c8a-125">[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="39c8a-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="39c8a-126">[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="39c8a-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="39c8a-127">Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="39c8a-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="39c8a-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="39c8a-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
