---
title: Definere lageransatte | Microsoft-dokumentasjon
description: Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til én standardlokasjon og eventuelt flere ikke-standardlokasjoner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ee03696db25242145232f11da58729b51d65654e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925325"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="422d8-103">Definere lageransatte</span><span class="sxs-lookup"><span data-stu-id="422d8-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="422d8-104">Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til én standardlokasjon og eventuelt flere ikke-standardlokasjoner.</span><span class="sxs-lookup"><span data-stu-id="422d8-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="422d8-105">Dette brukeroppsettet filtrerer alle lageraktiviteter i databasen etter den ansattes lokasjon slik at den ansatte bare kan utføre lageraktivitetene i standardlokasjonen.</span><span class="sxs-lookup"><span data-stu-id="422d8-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="422d8-106">En bruker kan tilordnes til flere ikke-standardlokasjoner som den ansatte kan vise aktivitetslinjer for, men ikke utføre aktiviteter for.</span><span class="sxs-lookup"><span data-stu-id="422d8-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="422d8-107">Slik definerer du lageransatte</span><span class="sxs-lookup"><span data-stu-id="422d8-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="422d8-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageransatte**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="422d8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="422d8-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="422d8-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="422d8-110">Velg **Bruker-ID**-feltet, og velg deretter brukeren som skal legges til som lageransatt.</span><span class="sxs-lookup"><span data-stu-id="422d8-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="422d8-111">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="422d8-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="422d8-112">I feltet **Lokasjonskode** skriver du inn koden for lokasjonen der brukeren skal arbeide.</span><span class="sxs-lookup"><span data-stu-id="422d8-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="422d8-113">Merk av for **Standard** for å definere lokasjonen som den eneste lokasjonen der den ansatte kan utføre lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="422d8-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="422d8-114">Gjenta disse trinnene for å tilordne andre ansatte til lokasjoner, eller for å tilordne ikke-standardlokasjoner til eksisterende lageransatte.</span><span class="sxs-lookup"><span data-stu-id="422d8-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="422d8-115">Se også</span><span class="sxs-lookup"><span data-stu-id="422d8-115">See Also</span></span>  
[<span data-ttu-id="422d8-116">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="422d8-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="422d8-117">Lager</span><span class="sxs-lookup"><span data-stu-id="422d8-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="422d8-118">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="422d8-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="422d8-119">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="422d8-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="422d8-120">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="422d8-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="422d8-121">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="422d8-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
