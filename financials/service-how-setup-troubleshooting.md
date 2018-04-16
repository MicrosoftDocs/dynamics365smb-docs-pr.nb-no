---
title: "Definere feilsøkingsprosesser | Microsoft-dokumentasjon"
description: "Finn ut hvordan du konfigurerer prosessene som kan hjelpe kundeservicerepresentanter med å identifisere og løse problemer med servicevarer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 14b7dddf1415e06df5e27f063447de633167b81f
ms.contentlocale: nb-no
ms.lasthandoff: 04/16/2018

---

# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="a7254-103">Definere feilsøking av servicevarer</span><span class="sxs-lookup"><span data-stu-id="a7254-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="a7254-104">Du kan definere retningslinjer for feilsøking for teknikere som bidrar til å løse problemer ved service.</span><span class="sxs-lookup"><span data-stu-id="a7254-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="a7254-105">Retningslinjene kan for eksempel være en oversikt over trinn for å utføre en reparasjon eller en serie med spørsmål å stille om varene.</span><span class="sxs-lookup"><span data-stu-id="a7254-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="a7254-106">Når du har definert retningslinjene for feilsøking, kan du tilordne dem til servicevaregrupper, servicevarer eller varer.</span><span class="sxs-lookup"><span data-stu-id="a7254-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="a7254-107">Det finnes et arvehierarki for retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="a7254-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="a7254-108">Hvis du tilordner dem til en servicevaregruppe, vil varene i gruppen arver retningslinjene med mindre du angir dem for varene.</span><span class="sxs-lookup"><span data-stu-id="a7254-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="a7254-109">På samme måte arver servicevarer retningslinjene fra varer.</span><span class="sxs-lookup"><span data-stu-id="a7254-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="a7254-110">Slik definerer du retningslinjer for feilsøking</span><span class="sxs-lookup"><span data-stu-id="a7254-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="a7254-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Feilsøking**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a7254-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a7254-112">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a7254-112">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="a7254-113">Tilordne retningslinjer for feilsøking til varer, servicevarer eller servicevaregrupper.</span><span class="sxs-lookup"><span data-stu-id="a7254-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="a7254-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, **Servicevarer** eller **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a7254-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a7254-115">Velg den aktuelle enheten, og velg deretter handlingen **Feilsøking**.</span><span class="sxs-lookup"><span data-stu-id="a7254-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7254-116">Se også</span><span class="sxs-lookup"><span data-stu-id="a7254-116">See Also</span></span>
[<span data-ttu-id="a7254-117">Servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="a7254-117">Service Management</span></span>](service-service.md)
