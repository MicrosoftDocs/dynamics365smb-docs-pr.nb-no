---
title: Definere statuser for serviceordrer og reparasjoner | Microsoft-dokumentasjon
description: Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cb6ba334d4584d6e3ead25606a612686258eae9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776819"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="1fa03-103">Definere statuser for serviceordrer og reparasjoner</span><span class="sxs-lookup"><span data-stu-id="1fa03-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="1fa03-104">Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="1fa03-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="1fa03-105">Du må definerer minst ni alternativer for reparasjonsstatus som identifiserer situasjoner eller handlinger som er iverksatt under vedlikehold av servicevarer.</span><span class="sxs-lookup"><span data-stu-id="1fa03-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="1fa03-106">Du kan angi prioritetsnivå for alternativene for serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="1fa03-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="1fa03-107">De fire prioritetene er **Høy**, **Middels høy**, **Middels lav** og **Lav**.</span><span class="sxs-lookup"><span data-stu-id="1fa03-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="1fa03-108">Når du endrer reparasjonsstatusen til en servicevare i en serviceordre, oppdateres serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="1fa03-109">Reparasjonsstatusen til hver enkelt servicevare er knyttet til serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="1fa03-110">Hvis servicevarene er koblet til to eller flere alternativer for serviceordrestatus, velges serviceordrestatusen med høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="1fa03-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="1fa03-111">Før du kan definere en reparasjonsstatus, må du definere servicestatusprioritet.</span><span class="sxs-lookup"><span data-stu-id="1fa03-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="1fa03-112">Slik definerer du servicestatusprioritet</span><span class="sxs-lookup"><span data-stu-id="1fa03-112">To set up service status priorities</span></span>

1. <span data-ttu-id="1fa03-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrestatus**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1fa03-114">Velg serviceordrestatusen du vil angi en prioritet for.</span><span class="sxs-lookup"><span data-stu-id="1fa03-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="1fa03-115">I feltet **Prioritet** velger du prioriteten du vil ha for denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="1fa03-116">Gjenta trinnene 2 og 3 til du har angitt prioriteten for hvert enkelt av de fire statusalternativene: **Venter**, **I arbeid**, **Ferdig** og **Avvent**.</span><span class="sxs-lookup"><span data-stu-id="1fa03-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="1fa03-117">Slik definerer du reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="1fa03-117">To set up a repair status</span></span>

1. <span data-ttu-id="1fa03-118">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Reparasjonsstatus**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="1fa03-119">Opprett en ny reparasjonsstatus.</span><span class="sxs-lookup"><span data-stu-id="1fa03-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="1fa03-120">Fyll ut feltene **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="1fa03-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="1fa03-121">I **Serviceordrestatus**-feltet velger du ordrestatusen å knytte reparasjonsstatusen til.</span><span class="sxs-lookup"><span data-stu-id="1fa03-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="1fa03-122">**Prioritet**-feltet viser prioriteten til serviceordrestatusen du har valgt.</span><span class="sxs-lookup"><span data-stu-id="1fa03-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="1fa03-123">Velg en reparasjonsstatus.</span><span class="sxs-lookup"><span data-stu-id="1fa03-123">Choose a repair status.</span></span> <span data-ttu-id="1fa03-124">Du kan bare velge én.</span><span class="sxs-lookup"><span data-stu-id="1fa03-124">You can choose only one.</span></span> <span data-ttu-id="1fa03-125">En reparasjonsstatus kan ikke kobles til mer enn ett reparasjonsstatusalternativ.</span><span class="sxs-lookup"><span data-stu-id="1fa03-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="1fa03-126">Velg feltet **Bokføring tillatt** hvis du vil kunne bokføre serviceordrer som omfatter servicevarer, med reparasjonsstatusen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="1fa03-127">Merk av for **I kø-status tillatt** for å tillate manuell endring av alternativet for serviceordrestatusen til alternativet **I kø** i serviceordrer som omfatter servicevarer med denne reparasjonsstatusen.</span><span class="sxs-lookup"><span data-stu-id="1fa03-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="1fa03-128">Merk av for **I arbeid-status tillatt**, **Ferdig-status tillatt** og **Avvent-status tillatt** på samme måte.</span><span class="sxs-lookup"><span data-stu-id="1fa03-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="1fa03-129">Gjenta disse trinnene for hvert enkelt alternativ for reparasjonsstatusen du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="1fa03-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa03-130">Se også</span><span class="sxs-lookup"><span data-stu-id="1fa03-130">See Also</span></span>

[<span data-ttu-id="1fa03-131">Serviceordrestatus og reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="1fa03-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="1fa03-132">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="1fa03-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]