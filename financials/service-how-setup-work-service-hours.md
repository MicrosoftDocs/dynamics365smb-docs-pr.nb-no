---
title: Konfigurere arbeidstimer og servicetimer | Microsoft-dokumentasjon
description: "Du kan angi de vanlige servicearbeidstimene i selskapet. Disse servicetimene brukes til å beregne responsdatoen og -klokkeslettet for serviceordrer og -tilbud, og til å sende advarsler om responstid."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-work-hours-and-service-hours"></a><span data-ttu-id="f0c83-104">Konfigurere arbeidstimer og servicetimer</span><span class="sxs-lookup"><span data-stu-id="f0c83-104">Set Up Work Hours and Service Hours</span></span>
<span data-ttu-id="f0c83-105">Med et servicesystem kan du vanligvis spore ressurstimer og serviceordrestatus for å prognostisere arbeidsmengder og servicebehov.</span><span class="sxs-lookup"><span data-stu-id="f0c83-105">Typically, a service management system tracks resource hours and service order status in order to forecast workloads and service needs.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f0c83-106"> har innebygde verktøy du kan tilpasse for å registrere denne typen informasjon.</span><span class="sxs-lookup"><span data-stu-id="f0c83-106"> has built-in tools that you can customize to record this kind of information.</span></span>  
  
<span data-ttu-id="f0c83-107">Etter at du har angitt selskapets standard servicetimer, kan du beregne responstiden for serviceordrer eller sende advarsler eller varsler når det kommer serviceanrop.</span><span class="sxs-lookup"><span data-stu-id="f0c83-107">After you set the default service hours of your company, you can calculate response times for service orders or send warnings or alerts when service calls come in.</span></span> <span data-ttu-id="f0c83-108">Varslingsfunksjonen implementeres sammen med jobbskjemaet.</span><span class="sxs-lookup"><span data-stu-id="f0c83-108">The alert feature is implemented together with the job scheduler.</span></span>   
  
<span data-ttu-id="f0c83-109">Når du arbeider med en serviceordre, vil du oppdaterer statusen slik at du kan overvåke fremdriften.</span><span class="sxs-lookup"><span data-stu-id="f0c83-109">As you work on a service order, you will want to update it's status so that you can monitor progress.</span></span> <span data-ttu-id="f0c83-110">Serviceordrestatusen gjenspeiler reparasjonsstatusen til alle servicevarene i serviceordren.</span><span class="sxs-lookup"><span data-stu-id="f0c83-110">The service order status reflects the repair status of all the service items in the service order.</span></span> <span data-ttu-id="f0c83-111">Hvis du vil ha mer informasjon, kan du se [Forstå serviceordre- og reparasjonsstatus](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="f0c83-111">For more information, see [Understanding Service Order and Repair Status](service-order-repair-status.md).</span></span> 

## <a name="to-set-up-default-service-hours"></a><span data-ttu-id="f0c83-112">Slik definerer du Standard servicetimer</span><span class="sxs-lookup"><span data-stu-id="f0c83-112">To set up default service hours</span></span>  
<span data-ttu-id="f0c83-113">Du bruker vinduet **Standard servicetimer** til å definere selskapets normale antall servicearbeidstimer.</span><span class="sxs-lookup"><span data-stu-id="f0c83-113">You use the **Default Service Hours** window to set up the usual service working hours in your company.</span></span> <span data-ttu-id="f0c83-114">Disse servicetimene brukes til å beregne responsdatoen og -klokkeslettet for serviceordrer og -tilbud, og til å sende advarsler om responstid.</span><span class="sxs-lookup"><span data-stu-id="f0c83-114">These service hours are used to calculate the response date and time for service orders and quotes and to send response time warnings.</span></span> <span data-ttu-id="f0c83-115">Standard servicetimer brukes for servicekontrakter hvis du ikke angir spesifikke servicetimer for en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="f0c83-115">The default service hours are used for service contracts unless you specify special service hours for a contract.</span></span>  
  
1. <span data-ttu-id="f0c83-116">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Standard servicetimer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f0c83-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Default Service Hours**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0c83-117">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f0c83-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  <span data-ttu-id="f0c83-118">Hvis du lar linjene i vinduet **Standard servicetimer** stå tomme, bruker programmet 24 timer som standardverdi, som bare er gjelder for arbeidsdager fra kalenderen.</span><span class="sxs-lookup"><span data-stu-id="f0c83-118">If you leave the lines in the **Default Service Hours** window empty, the default value is 24 hours, valid only for calendar working days.</span></span>  
  
## <a name="to-set-up-work-hour-templates"></a><span data-ttu-id="f0c83-119">Definere arbeidstidsmaler</span><span class="sxs-lookup"><span data-stu-id="f0c83-119">To set up work-hour templates</span></span>
<span data-ttu-id="f0c83-120">Du kan bruke vinduet **Arbeidstidsmal** til å definere maler som inneholder vanlige arbeidstider i selskapet.</span><span class="sxs-lookup"><span data-stu-id="f0c83-120">You can use the **Work-Hour Template** window to set up templates that contain the typical working hours in your company.</span></span> <span data-ttu-id="f0c83-121">Du kan for eksempel opprette maler for heltidsteknikere og deltidsteknikere.</span><span class="sxs-lookup"><span data-stu-id="f0c83-121">For example, you can create templates for full time technicians and part time technicians.</span></span> <span data-ttu-id="f0c83-122">Du kan bruke arbeidstidsmaler når du legger til kapasitet i ressurser.</span><span class="sxs-lookup"><span data-stu-id="f0c83-122">You can use work-hour templates when you add capacity to resources.</span></span>  
  
1. <span data-ttu-id="f0c83-123">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidstidsmaler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f0c83-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Hour Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0c83-124">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f0c83-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> <span data-ttu-id="f0c83-125">Når du har angitt arbeidstimer for hver dag, beregnes verdien i feltet **Sum per uke** automatisk.</span><span class="sxs-lookup"><span data-stu-id="f0c83-125">After you enter work hours for each day, the value in the **Total per Week** field is calculated automatically.</span></span>  

## <a name="to-set-up-contract-specific-service-hours"></a><span data-ttu-id="f0c83-126">Slik definerer du kontraktsspesifikke servicetimer</span><span class="sxs-lookup"><span data-stu-id="f0c83-126">To set up contract specific service hours</span></span>  
<span data-ttu-id="f0c83-127">Du kan bruke vinduet **Servicetimer** til å definere spesifikke servicetimer timer for kunden som eier servicekontrakten.</span><span class="sxs-lookup"><span data-stu-id="f0c83-127">You can use the **Service Hours** window to set up specific service hours for the customer that owns the service contract.</span></span> <span data-ttu-id="f0c83-128">Servicetimer brukes til å beregne responsdatoen og -tiden for serviceordrer og -tilbud som hører til servicekontrakten.</span><span class="sxs-lookup"><span data-stu-id="f0c83-128">Service hours are used to calculate the response date and time for service orders and quotes that belong to the service contract.</span></span>  
  
<span data-ttu-id="f0c83-129">Hvis du ikke definerer spesifikke servicetimer for servicekontrakten, brukes standard servicetimer for servicekontraktene.</span><span class="sxs-lookup"><span data-stu-id="f0c83-129">If you do not set up specific service hours for the service contract, the default service hours for service contracts are used.</span></span>  
  
1. <span data-ttu-id="f0c83-130">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f0c83-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contracts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f0c83-131">Åpne servicekontrakten du vil definere spesifikke servicetimer for, og velg **Servicetimer**.</span><span class="sxs-lookup"><span data-stu-id="f0c83-131">Open the service contract you want to set up specific service hours for, and choose **Service Hours**.</span></span>  
4. <span data-ttu-id="f0c83-132">Hvis du vil definere servicetimer basert på standard servicetimer, velger du handlingen **Kopier std. servicetimer**.</span><span class="sxs-lookup"><span data-stu-id="f0c83-132">To set up service hours based on default service hours, choose the **Copy Default Service Hours** action.</span></span>  
5. <span data-ttu-id="f0c83-133">Rediger feltene i servicetimepostene.</span><span class="sxs-lookup"><span data-stu-id="f0c83-133">Edit the fields in the service hours entries.</span></span> <span data-ttu-id="f0c83-134">Sett inn eller slett poster for å definere servicetimer for kontrakten.</span><span class="sxs-lookup"><span data-stu-id="f0c83-134">Insert or delete entries to set up the service hours for the contract.</span></span> <span data-ttu-id="f0c83-135">Merk at feltene **Dag**, **Starttidspunkt** og **Sluttidspunkt** kreves for hver linje.</span><span class="sxs-lookup"><span data-stu-id="f0c83-135">Note that the fields **Day**, **Starting Time** and **Ending Time** are required for each line.</span></span>  
6. <span data-ttu-id="f0c83-136">Hvis du vil at servicetimene skal gjelde fra en bestemt dato, fyller du ut feltet **Startdato**.</span><span class="sxs-lookup"><span data-stu-id="f0c83-136">If you want the service hours to be valid from a specific date, fill in the **Starting Date** field.</span></span>  
7. <span data-ttu-id="f0c83-137">Hvis du vil at servicetimene skal gjelde i ferier, setter du en hake i avmerkingsboksen i feltet **Gyldig i ferier**.</span><span class="sxs-lookup"><span data-stu-id="f0c83-137">If you want the service hours to be valid on holidays, select the check box in the **Valid on Holidays** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f0c83-138">Se også</span><span class="sxs-lookup"><span data-stu-id="f0c83-138">See Also</span></span>  
[<span data-ttu-id="f0c83-139">Forstå tildelingsstatus og reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="f0c83-139">Understanding Allocation Status and Repair Status</span></span>](service-allocation-status-and-repair-status.md)  
[<span data-ttu-id="f0c83-140">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="f0c83-140">Setting Up Service Management</span></span>](service-setup-service.md)  
[<span data-ttu-id="f0c83-141">Forstå serviceordre- og reparasjonsstatus</span><span class="sxs-lookup"><span data-stu-id="f0c83-141">Understanding Service Order and Repair Status</span></span>](service-order-repair-status.md)  

