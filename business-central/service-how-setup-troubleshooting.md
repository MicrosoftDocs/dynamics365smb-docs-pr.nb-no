---
title: Definere feilsøkingsprosesser | Microsoft-dokumentasjon
description: Finn ut hvordan du konfigurerer prosessene som kan hjelpe kundeservicerepresentanter med å identifisere og løse problemer med servicevarer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 24a4fa9811547acfd3372d3eaf7de7b9f1882c7d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803043"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="11f29-103">Definere feilsøking av servicevarer</span><span class="sxs-lookup"><span data-stu-id="11f29-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="11f29-104">Du kan definere retningslinjer for feilsøking for teknikere som bidrar til å løse problemer ved service.</span><span class="sxs-lookup"><span data-stu-id="11f29-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="11f29-105">Retningslinjene kan for eksempel være en oversikt over trinn for å utføre en reparasjon eller en serie med spørsmål å stille om varene.</span><span class="sxs-lookup"><span data-stu-id="11f29-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="11f29-106">Når du har definert retningslinjene for feilsøking, kan du tilordne dem til servicevaregrupper, servicevarer eller varer.</span><span class="sxs-lookup"><span data-stu-id="11f29-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="11f29-107">Det finnes et arvehierarki for retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="11f29-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="11f29-108">Hvis du tilordner dem til en servicevaregruppe, vil varene i gruppen arver retningslinjene med mindre du angir dem for varene.</span><span class="sxs-lookup"><span data-stu-id="11f29-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="11f29-109">På samme måte arver servicevarer retningslinjene fra varer.</span><span class="sxs-lookup"><span data-stu-id="11f29-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="11f29-110">Slik definerer du retningslinjer for feilsøking</span><span class="sxs-lookup"><span data-stu-id="11f29-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="11f29-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feilsøking**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="11f29-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="11f29-112">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="11f29-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="11f29-113">Tilordne retningslinjer for feilsøking til varer, servicevarer eller servicevaregrupper.</span><span class="sxs-lookup"><span data-stu-id="11f29-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="11f29-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, **Servicevarer** eller **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="11f29-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="11f29-115">Velg den aktuelle enheten, og velg deretter handlingen **Feilsøking**.</span><span class="sxs-lookup"><span data-stu-id="11f29-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11f29-116">Se også</span><span class="sxs-lookup"><span data-stu-id="11f29-116">See Also</span></span>
[<span data-ttu-id="11f29-117">Servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="11f29-117">Service Management</span></span>](service-service.md)