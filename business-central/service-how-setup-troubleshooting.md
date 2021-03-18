---
title: Definere feilsøkingsprosesser | Microsoft-dokumentasjon
description: Finn ut hvordan du konfigurerer prosessene som kan hjelpe kundeservicerepresentanter med å identifisere og løse problemer med servicevarer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, troubleshoot, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7fdbc30e20e7d5a8feeb17a97ccdee3688fa7607
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380409"
---
# <a name="setting-up-troubleshooting-for-service-items"></a><span data-ttu-id="25f35-103">Definere feilsøking av servicevarer</span><span class="sxs-lookup"><span data-stu-id="25f35-103">Setting Up Troubleshooting for Service Items</span></span>
<span data-ttu-id="25f35-104">Du kan definere retningslinjer for feilsøking for teknikere som bidrar til å løse problemer ved service.</span><span class="sxs-lookup"><span data-stu-id="25f35-104">You can set up troubleshooting guidelines that help technicians solve problems when providing service.</span></span> <span data-ttu-id="25f35-105">Retningslinjene kan for eksempel være en oversikt over trinn for å utføre en reparasjon eller en serie med spørsmål å stille om varene.</span><span class="sxs-lookup"><span data-stu-id="25f35-105">For example, guidelines might be a list of steps to perform a repair, or a series of questions to ask about the items.</span></span> <span data-ttu-id="25f35-106">Når du har definert retningslinjene for feilsøking, kan du tilordne dem til servicevaregrupper, servicevarer eller varer.</span><span class="sxs-lookup"><span data-stu-id="25f35-106">After you set up troubleshooting guidelines, you can assign them to service item groups, service items, and items.</span></span> <span data-ttu-id="25f35-107">Det finnes et arvehierarki for retningslinjer.</span><span class="sxs-lookup"><span data-stu-id="25f35-107">There is an inheritance hierarchy for guidelines.</span></span> <span data-ttu-id="25f35-108">Hvis du tilordner dem til en servicevaregruppe, vil varene i gruppen arver retningslinjene med mindre du angir dem for varene.</span><span class="sxs-lookup"><span data-stu-id="25f35-108">If you assign them to a service item group, the items included in the group will inherit the guidelines unless you specify them for the items.</span></span> <span data-ttu-id="25f35-109">På samme måte arver servicevarer retningslinjene fra varer.</span><span class="sxs-lookup"><span data-stu-id="25f35-109">Similarly, service items will inherit guidelines from items.</span></span>  

## <a name="to-set-up-troubleshooting-guidelines"></a><span data-ttu-id="25f35-110">Slik definerer du retningslinjer for feilsøking</span><span class="sxs-lookup"><span data-stu-id="25f35-110">To set up troubleshooting guidelines</span></span>
1. <span data-ttu-id="25f35-111">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Feilsøking**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="25f35-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Troubleshooting**, and then choose the related link.</span></span>  
2. <span data-ttu-id="25f35-112">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="25f35-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-troubleshooting-guidelines-to-items-service-items-or-service-item-groups"></a><span data-ttu-id="25f35-113">Tilordne retningslinjer for feilsøking til varer, servicevarer eller servicevaregrupper.</span><span class="sxs-lookup"><span data-stu-id="25f35-113">To assign troubleshooting guidelines to items, service items, or service item groups</span></span>
1. <span data-ttu-id="25f35-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, **Servicevarer** eller **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="25f35-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, **Service Items**, or **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="25f35-115">Velg den aktuelle enheten, og velg deretter handlingen **Feilsøking**.</span><span class="sxs-lookup"><span data-stu-id="25f35-115">Choose the relevant entity, and then choose the **Troubleshooting** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="25f35-116">Se også</span><span class="sxs-lookup"><span data-stu-id="25f35-116">See Also</span></span>
[<span data-ttu-id="25f35-117">Servicebehandling</span><span class="sxs-lookup"><span data-stu-id="25f35-117">Service Management</span></span>](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]