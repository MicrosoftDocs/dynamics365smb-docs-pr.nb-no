---
title: Serviceordrestatus og reparasjonsstatus
description: Feltet Status på siden Serviceordre og reparasjonsstatusen til servicevaren, som representeres av feltet Reparasjonsstatuskode på siden Serviceordre, har en bestemt forbindelse i Service. Serviceordrestatusen gjenspeiler reparasjonsstatusen til alle servicevarene i serviceordren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: b9095cbfd1b8a55f525f0a3c4dcfad6cf56fc449
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386827"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="146d7-104">Serviceordrestatus og reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="146d7-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="146d7-105">Feltet **Status** på siden **Serviceordre** og reparasjonsstatusen til servicevaren, som representeres av feltet **Reparasjonsstatuskode** på siden **Serviceordre**, har en bestemt forbindelse i Service.</span><span class="sxs-lookup"><span data-stu-id="146d7-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="146d7-106">Serviceordrestatusen gjenspeiler reparasjonsstatusen til alle servicevarene i serviceordren.</span><span class="sxs-lookup"><span data-stu-id="146d7-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="146d7-107">Disse to statusfeltene har ingen tilknytning til feltet **Frigivelsesstatus** i serviceordrehodet, som styrer hvordan lageret håndterer servicevarer.</span><span class="sxs-lookup"><span data-stu-id="146d7-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="146d7-108">Hver gang reparasjonsstatusen til en servicevare endres i en serviceordre, oppdateres ordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="146d7-109">Du må angi følgende for å vise statusen som gjenspeiler samlet reparasjonsstatus til hver enkelt servicevare:</span><span class="sxs-lookup"><span data-stu-id="146d7-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="146d7-110">Serviceordrestatusen som hver enkelt reparasjonsstatus er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="146d7-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="146d7-111">Prioritetsnivået til hvert enkelt alternativ for serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="146d7-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="146d7-112">Når du konverterer et servicetilbud til en serviceordre, endres reparasjonsstatusen til hver enkelt servicevare i ordren til **Første**, og serviceordren endres til **Ventende**.</span><span class="sxs-lookup"><span data-stu-id="146d7-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="146d7-113">Før du kan opprette serviceordrer, må du definere reparasjonsstatuser og servicestatusprioritet.</span><span class="sxs-lookup"><span data-stu-id="146d7-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="146d7-114">Hvis du vil ha mer informasjon, kan du se [Definere statuser for serviceordrer og reparasjoner](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="146d7-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="146d7-115">Angi serviceordrestatus for reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="146d7-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="146d7-116">Hver enkelt reparasjonsstatus er knyttet til en bestemt serviceordrestatus.</span><span class="sxs-lookup"><span data-stu-id="146d7-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="146d7-117">Alternativene for serviceordrestatusen er følgende:</span><span class="sxs-lookup"><span data-stu-id="146d7-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="146d7-118">**I kø**</span><span class="sxs-lookup"><span data-stu-id="146d7-118">**Pending**</span></span>
* <span data-ttu-id="146d7-119">**I arbeid**</span><span class="sxs-lookup"><span data-stu-id="146d7-119">**In Process**</span></span>
* <span data-ttu-id="146d7-120">**Avvent**</span><span class="sxs-lookup"><span data-stu-id="146d7-120">**On Hold**</span></span>
* <span data-ttu-id="146d7-121">**Ferdig**</span><span class="sxs-lookup"><span data-stu-id="146d7-121">**Finished**</span></span>

<span data-ttu-id="146d7-122">Reparasjonsstatusalternativene er følgende:</span><span class="sxs-lookup"><span data-stu-id="146d7-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="146d7-123">**Første**</span><span class="sxs-lookup"><span data-stu-id="146d7-123">**Initial**</span></span>
* <span data-ttu-id="146d7-124">**I arbeid**</span><span class="sxs-lookup"><span data-stu-id="146d7-124">**In Process**</span></span>
* <span data-ttu-id="146d7-125">**Henvist**</span><span class="sxs-lookup"><span data-stu-id="146d7-125">**Referred**</span></span>
* <span data-ttu-id="146d7-126">**Delvis vedlikeholdt**</span><span class="sxs-lookup"><span data-stu-id="146d7-126">**Partly Serviced**</span></span>
* <span data-ttu-id="146d7-127">**Tilbud ferdig**</span><span class="sxs-lookup"><span data-stu-id="146d7-127">**Quote Finished**</span></span>
* <span data-ttu-id="146d7-128">**Venter på kunde**</span><span class="sxs-lookup"><span data-stu-id="146d7-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="146d7-129">**Reservedel bestilt**</span><span class="sxs-lookup"><span data-stu-id="146d7-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="146d7-130">**Reservedel mottatt**</span><span class="sxs-lookup"><span data-stu-id="146d7-130">**Spare Part Received**</span></span>
* <span data-ttu-id="146d7-131">**Ferdig**</span><span class="sxs-lookup"><span data-stu-id="146d7-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="146d7-132">I kø</span><span class="sxs-lookup"><span data-stu-id="146d7-132">Pending</span></span>

<span data-ttu-id="146d7-133">Serviceordrestatusen **I kø** angir at servicen når som helst kan starte eller fortsette.</span><span class="sxs-lookup"><span data-stu-id="146d7-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="146d7-134">Alle de fire reparasjonsstatusalternativene **Første**, **Henvist**, **Delvis vedlikehold** og **Reservedel mottatt** kan derfor knyttes til denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="146d7-135">I arbeid</span><span class="sxs-lookup"><span data-stu-id="146d7-135">In Process</span></span>

<span data-ttu-id="146d7-136">Serviceordrestatusen **I arbeid** angir at servicen er i arbeid.</span><span class="sxs-lookup"><span data-stu-id="146d7-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="146d7-137">Begge de to reparasjonsstatusalternativene **I arbeid** og **Reservedel bestilt** kan derfor knyttes til denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="146d7-138">Hvis du kobler statusen **Reservedel bestilt** til serviceordrestatusen **I arbeid**, må du også koble statusen **Reservedel mottatt** til denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="146d7-139">Avvent</span><span class="sxs-lookup"><span data-stu-id="146d7-139">On Hold</span></span>

<span data-ttu-id="146d7-140">Serviceordrestatusen **Avvent** angir at servicen midlertidig må avventes fordi du venter på et kundesvar eller reservedeler før servicen kan påbegynnes.</span><span class="sxs-lookup"><span data-stu-id="146d7-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="146d7-141">Alle de tre reparasjonsstatusalternativene **Tilbud ferdig**, **Reservedel bestilt** og **Venter på kunde** kan derfor knyttes til denne serviceordrestatusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="146d7-142">Ferdig</span><span class="sxs-lookup"><span data-stu-id="146d7-142">Finished</span></span>

<span data-ttu-id="146d7-143">Serviceordrestatusen **Ferdig** angir at servicen er fullført.</span><span class="sxs-lookup"><span data-stu-id="146d7-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="146d7-144">Reparasjonsstatusen **Ferdig** er derfor knyttet til denne statusen.</span><span class="sxs-lookup"><span data-stu-id="146d7-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="146d7-145">Tilordne prioritet til serviceordrestatus</span><span class="sxs-lookup"><span data-stu-id="146d7-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="146d7-146">Når en reparasjonsstatus til en servicevare endres, identifiseres alternativene for serviceordrestatusen som er knyttet til de ulike reparasjonsstatusalternativene for alle servicevarene i ordren.</span><span class="sxs-lookup"><span data-stu-id="146d7-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="146d7-147">Hvis servicevarene er koblet til to eller flere alternativer for serviceordrestatus, velges serviceordrestatusalternativet med høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="146d7-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="146d7-148">Du må bestemme hvilken serviceordrestatus som inneholder de viktigste opplysningene om statusen til serviceordren, og deretter tilordne denne statusen den høyeste prioriteten og så videre.</span><span class="sxs-lookup"><span data-stu-id="146d7-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="146d7-149">Når du deretter oppretter en ny serviceordre og legger til servicevarer i den, oppdateres **Prioritet**-feltet i serviceordreoverskriften basert på prioritetene for servicevarene.</span><span class="sxs-lookup"><span data-stu-id="146d7-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="146d7-150">Eksempel</span><span class="sxs-lookup"><span data-stu-id="146d7-150">Example</span></span>

<span data-ttu-id="146d7-151">En vanlig tilordning av prioritetsnivå kan være følgende:</span><span class="sxs-lookup"><span data-stu-id="146d7-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="146d7-152">I arbeid: høy</span><span class="sxs-lookup"><span data-stu-id="146d7-152">In Process - High</span></span>  
* <span data-ttu-id="146d7-153">I kø: middels høy</span><span class="sxs-lookup"><span data-stu-id="146d7-153">Pending - Medium high</span></span>  
* <span data-ttu-id="146d7-154">Avvent: middels lav</span><span class="sxs-lookup"><span data-stu-id="146d7-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="146d7-155">Ferdig: lav</span><span class="sxs-lookup"><span data-stu-id="146d7-155">Finished - Low</span></span>  

<span data-ttu-id="146d7-156">Hvis én servicevare for eksempel har reparasjonsstatusen **Første**, knyttet til serviceordrestatusen **I kø**, en annen har reparasjonsstatusen **I arbeid**, knyttet til serviceordrestatusen **I arbeid**, og en tredje har reparasjonsstatusen **Reservedel bestilt**, knyttet til serviceordrestatusen **Avvent**, blir den endelige serviceordrestatusen **I arbeid** fordi denne har høyest prioritet.</span><span class="sxs-lookup"><span data-stu-id="146d7-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="146d7-157">Se også</span><span class="sxs-lookup"><span data-stu-id="146d7-157">See Also</span></span>

[<span data-ttu-id="146d7-158">Definere statuser for serviceordrer og reparasjoner</span><span class="sxs-lookup"><span data-stu-id="146d7-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="146d7-159">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="146d7-159">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]