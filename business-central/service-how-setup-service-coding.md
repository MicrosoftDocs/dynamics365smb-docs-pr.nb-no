---
title: Definere koder for standardservice | Microsoft-dokumentasjon
description: Finn ut hvordan du kan definere koder for serviceaktiviteter som utføres ofte.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2db9480789e90b15e0a9d4e737817d3b8ff3b3c9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925832"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="da3d2-103">Definere standard servicekoder</span><span class="sxs-lookup"><span data-stu-id="da3d2-103">Set Up Standard Service Codes</span></span>

<span data-ttu-id="da3d2-104">Når du utfører typisk service, må du ofte opprette servicedokumenter som bruker servicelinjer som inneholder omtrent samme opplysninger.</span><span class="sxs-lookup"><span data-stu-id="da3d2-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="da3d2-105">Hvis du vil gjøre det enkelt å opprette disse linjene, kan du definere standard servicekoder som er et forhåndsdefinert sett med servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="da3d2-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="da3d2-106">Når du velger koden i et servicedokument, angis linjene automatisk.</span><span class="sxs-lookup"><span data-stu-id="da3d2-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="da3d2-107">Du kan angi så mange standard servicekoder du vil, og hver kode kan ha et ubegrenset antall servicelinjer av ulike typer, inkludert vare, ressurs, kostnad eller standardtekst, knyttet til seg.</span><span class="sxs-lookup"><span data-stu-id="da3d2-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standard text linked to it.</span></span> <span data-ttu-id="da3d2-108">Det kan opprettes servicelinjer for hver standard servicekode i korter **Standard servicekode**.</span><span class="sxs-lookup"><span data-stu-id="da3d2-108">You create service lines of each standard service code on the **Standard Service Code** card.</span></span> <span data-ttu-id="da3d2-109">Du tilordner deretter standard servicekoder til servicevaregrupper på siden **Standard servicevaregruppekoder**.</span><span class="sxs-lookup"><span data-stu-id="da3d2-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="da3d2-110">Senere, når du oppretter et servicedokument, kan du bruke handlingen **Hent standard servicekoder** for å legge til servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="da3d2-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
> <span data-ttu-id="da3d2-111">Du kan bruke samme metode for å opprette linjer i salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="da3d2-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="da3d2-112">Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="da3d2-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>  
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="da3d2-113">Slik definerer du standard servicekoder</span><span class="sxs-lookup"><span data-stu-id="da3d2-113">To set up a standard service code</span></span>

1. <span data-ttu-id="da3d2-114">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Standard servicekoder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="da3d2-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da3d2-115">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="da3d2-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="da3d2-116">Fyll ut servicelinjene som er koblet til denne servicekoden.</span><span class="sxs-lookup"><span data-stu-id="da3d2-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="da3d2-117">Slik knytter du en standard servicekode til en servicevaregruppe</span><span class="sxs-lookup"><span data-stu-id="da3d2-117">To assign a standard service code to a service item group</span></span>

1. <span data-ttu-id="da3d2-118">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicevaregrupper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="da3d2-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="da3d2-119">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="da3d2-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="da3d2-120">Fyll ut servicelinjene som er koblet til denne servicekoden.</span><span class="sxs-lookup"><span data-stu-id="da3d2-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da3d2-121">Se også</span><span class="sxs-lookup"><span data-stu-id="da3d2-121">See Also</span></span>

[<span data-ttu-id="da3d2-122">Servicebehandling</span><span class="sxs-lookup"><span data-stu-id="da3d2-122">Service Management</span></span>](service-service.md)