---
title: Definere koder for standardservice | Microsoft-dokumentasjon
description: Finn ut hvordan du kan definere koder for serviceaktiviteter som utføres ofte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 494a3dd93906a8a9d663455f7410d27c9fc34eb9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778225"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="4a92b-103">Definere standard servicekoder</span><span class="sxs-lookup"><span data-stu-id="4a92b-103">Set Up Standard Service Codes</span></span>

<span data-ttu-id="4a92b-104">Når du utfører typisk service, må du ofte opprette servicedokumenter som bruker servicelinjer som inneholder omtrent samme opplysninger.</span><span class="sxs-lookup"><span data-stu-id="4a92b-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="4a92b-105">Hvis du vil gjøre det enkelt å opprette disse linjene, kan du definere standard servicekoder som er et forhåndsdefinert sett med servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="4a92b-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="4a92b-106">Når du velger koden i et servicedokument, angis linjene automatisk.</span><span class="sxs-lookup"><span data-stu-id="4a92b-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="4a92b-107">Du kan angi så mange standard servicekoder du vil, og hver kode kan ha et ubegrenset antall servicelinjer av ulike typer, inkludert vare, ressurs, kostnad eller standardtekst, knyttet til seg.</span><span class="sxs-lookup"><span data-stu-id="4a92b-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standard text linked to it.</span></span> <span data-ttu-id="4a92b-108">Det kan opprettes servicelinjer for hver standard servicekode i korter **Standard servicekode**.</span><span class="sxs-lookup"><span data-stu-id="4a92b-108">You create service lines of each standard service code on the **Standard Service Code** card.</span></span> <span data-ttu-id="4a92b-109">Du tilordner deretter standard servicekoder til servicevaregrupper på siden **Standard servicevaregruppekoder**.</span><span class="sxs-lookup"><span data-stu-id="4a92b-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="4a92b-110">Senere, når du oppretter et servicedokument, kan du bruke handlingen **Hent standard servicekoder** for å legge til servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="4a92b-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
> <span data-ttu-id="4a92b-111">Du kan bruke samme metode for å opprette linjer i salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="4a92b-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="4a92b-112">Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="4a92b-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="4a92b-113">Slik definerer du standard servicekoder</span><span class="sxs-lookup"><span data-stu-id="4a92b-113">To set up a standard service code</span></span>

1. <span data-ttu-id="4a92b-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Standard servicekoder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4a92b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4a92b-115">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4a92b-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="4a92b-116">Fyll ut servicelinjene som er koblet til denne servicekoden.</span><span class="sxs-lookup"><span data-stu-id="4a92b-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="4a92b-117">Slik knytter du en standard servicekode til en servicevaregruppe</span><span class="sxs-lookup"><span data-stu-id="4a92b-117">To assign a standard service code to a service item group</span></span>

1. <span data-ttu-id="4a92b-118">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="4a92b-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4a92b-119">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="4a92b-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="4a92b-120">Fyll ut servicelinjene som er koblet til denne servicekoden.</span><span class="sxs-lookup"><span data-stu-id="4a92b-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a92b-121">Se også</span><span class="sxs-lookup"><span data-stu-id="4a92b-121">See Also</span></span>

[<span data-ttu-id="4a92b-122">Servicebehandling</span><span class="sxs-lookup"><span data-stu-id="4a92b-122">Service Management</span></span>](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]