---
title: Definere statuser for serviceordrer og reparasjoner | Microsoft-dokumentasjon
description: Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 64afbccba0573445902efdaf3c3919dacdb40e8c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "928419"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="c230d-103">Definere statuser for serviceordrer og reparasjoner</span><span class="sxs-lookup"><span data-stu-id="c230d-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="c230d-104">Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="c230d-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="c230d-105">Du må definerer minst ni alternativer for reparasjonsstatus som identifiserer situasjoner eller handlinger som er iverksatt under vedlikehold av servicevarer.</span><span class="sxs-lookup"><span data-stu-id="c230d-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="c230d-106">Du kan angi prioritetsnivå for alternativene for serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="c230d-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="c230d-107">De fire prioritetene er Høy, Middels høy, Middels lav og Lav.</span><span class="sxs-lookup"><span data-stu-id="c230d-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  

<span data-ttu-id="c230d-108">Når du endrer reparasjonsstatusen til en servicevare i en serviceordre, oppdateres serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="c230d-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="c230d-109">Reparasjonsstatusen til hver enkelt servicevare er knyttet til serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="c230d-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="c230d-110">Hvis servicevarene er koblet til to eller flere alternativer for serviceordrestatus, velges serviceordrestatusen med høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="c230d-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="c230d-111">Slik definerer du reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="c230d-111">To set up a repair status</span></span>  
1. <span data-ttu-id="c230d-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Reparasjonsstatus**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c230d-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="c230d-113">Opprett en ny reparasjonsstatus.</span><span class="sxs-lookup"><span data-stu-id="c230d-113">Create a new repair status.</span></span>  
3. <span data-ttu-id="c230d-114">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="c230d-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="c230d-115">I **Serviceordrestatus**-feltet velger du ordrestatusen å knytte reparasjonsstatusen til.</span><span class="sxs-lookup"><span data-stu-id="c230d-115">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="c230d-116">**Prioritet**-feltet viser prioriteten til serviceordrestatusen du har valgt.</span><span class="sxs-lookup"><span data-stu-id="c230d-116">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="c230d-117">Velg en reparasjonsstatus.</span><span class="sxs-lookup"><span data-stu-id="c230d-117">Choose a repair status.</span></span> <span data-ttu-id="c230d-118">Du kan bare velge én.</span><span class="sxs-lookup"><span data-stu-id="c230d-118">You can choose only one.</span></span>  
6. <span data-ttu-id="c230d-119">Velg feltet **Bokføring tillatt** hvis du vil kunne bokføre serviceordrer som omfatter servicevarer, med reparasjonsstatusen.</span><span class="sxs-lookup"><span data-stu-id="c230d-119">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="c230d-120">Merk av for **I kø-status tillatt** for å tillate manuell endring av alternativet for serviceordrestatusen til alternativet **I kø** i serviceordrer som omfatter servicevarer med denne reparasjonsstatusen.</span><span class="sxs-lookup"><span data-stu-id="c230d-120">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="c230d-121">Merk av for **I arbeid-status tillatt**, **Ferdig-status tillatt**og **Avvent-status tillatt**på samme måte.</span><span class="sxs-lookup"><span data-stu-id="c230d-121">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="c230d-122">Slik definerer du servicestatusprioritet</span><span class="sxs-lookup"><span data-stu-id="c230d-122">To set up service status priorities</span></span>  
1. <span data-ttu-id="c230d-123">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrestatus**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c230d-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c230d-124">Velg serviceordrestatusen du vil angi en prioritet for.</span><span class="sxs-lookup"><span data-stu-id="c230d-124">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="c230d-125">I feltet **Prioritet** velger du prioriteten du vil ha for denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="c230d-125">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="c230d-126">Gjenta dette trinnet for hver status.</span><span class="sxs-lookup"><span data-stu-id="c230d-126">Repeat this step for each status.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c230d-127">Se også</span><span class="sxs-lookup"><span data-stu-id="c230d-127">See Also</span></span>  
[<span data-ttu-id="c230d-128">Serviceordrestatus og reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="c230d-128">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="c230d-129">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="c230d-129">Setting Up Service Management</span></span>](service-setup-service.md)  
