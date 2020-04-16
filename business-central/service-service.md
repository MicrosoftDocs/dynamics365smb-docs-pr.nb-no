---
title: Servicehåndtering | Microsoft-dokumentasjon
description: Lær å bruke funksjonene som er utformet for å støtte serviceoperasjoner på verkstedet og ute hos kunder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6490ad13833c97c79c232b6433b4b2f51e51bc4f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192366"
---
# <a name="service-management"></a><span data-ttu-id="95f6d-103">Servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="95f6d-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="95f6d-104">Funksjonaliteten som er beskrevet i dette emnet og underemner, vises bare i brukergrensesnittet hvis du har **Premium**-opplevelsen.</span><span class="sxs-lookup"><span data-stu-id="95f6d-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="95f6d-105">Hvis du vil ha mer informasjon, se [Endre hvilke funksjoner som vises](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="95f6d-105">For more information, see [Change Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="95f6d-106">Det å kunne yte kontinuerlig service til kunder er viktig for alle bedrifter og kan bidra til kundetilfredshet, lojalitet og inntekt.</span><span class="sxs-lookup"><span data-stu-id="95f6d-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="95f6d-107">Det er imidlertid ikke alltid enkelt å behandle og spore service, og [!INCLUDE[d365fin](includes/d365fin_md.md)] har et sett med verktøy som kan være til hjelp.</span><span class="sxs-lookup"><span data-stu-id="95f6d-107">However, managing and tracking service is not always easy, and [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a set of tools to help.</span></span> <span data-ttu-id="95f6d-108">Disse verktøyene er utviklet for å støtte serviceoperasjoner på verkstedet og ute hos kunder og kan brukes i forretningsscenarioer som for eksempel komplekse distribusjonssystemer for kundeservice, industrielle servicemiljøer med stykklister, og fordeling av et stort antall oppgaver på serviceteknikere med behov for reservedelsstyring.</span><span class="sxs-lookup"><span data-stu-id="95f6d-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="95f6d-109">Med disse verktøyene kan du oppnå følgende:</span><span class="sxs-lookup"><span data-stu-id="95f6d-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="95f6d-110">Planlegge servicebesøk og definere serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="95f6d-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="95f6d-111">Spore reparasjonsdeler og leveranser.</span><span class="sxs-lookup"><span data-stu-id="95f6d-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="95f6d-112">Tilordne servicepersonell basert på kompetanse og tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="95f6d-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="95f6d-113">Opprett kostnadsoverslag og servicefakturaer.</span><span class="sxs-lookup"><span data-stu-id="95f6d-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="95f6d-114">I tillegg kan du standardisere koding, definere kontrakter, implementere et rabattprinsipp og opprette rutekart for servicepersonell.</span><span class="sxs-lookup"><span data-stu-id="95f6d-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="95f6d-115">Det er vanligvis to aspekter ved service: konfigurere og sette opp systemet, og bruke det til prissetting, kontrakter, ordrer, fordeling av servicepersonell, og jobbskjemaer.</span><span class="sxs-lookup"><span data-stu-id="95f6d-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="95f6d-116">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="95f6d-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="95f6d-117">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="95f6d-117">**To**</span></span>|<span data-ttu-id="95f6d-118">**Se**</span><span class="sxs-lookup"><span data-stu-id="95f6d-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="95f6d-119">Sette opp Service, inklusive feilkoder, prinsipper, standarddokumenter og maler.</span><span class="sxs-lookup"><span data-stu-id="95f6d-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="95f6d-120">Konfigurere servicehåndtering</span><span class="sxs-lookup"><span data-stu-id="95f6d-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="95f6d-121">Håndter serviceprissetting, oppretting av servicevarer og forstå hvordan du kan overvåker fremdriften.</span><span class="sxs-lookup"><span data-stu-id="95f6d-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="95f6d-122">Planlegge service</span><span class="sxs-lookup"><span data-stu-id="95f6d-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="95f6d-123">Opprett og håndter avtaler mellom deg og kundene.</span><span class="sxs-lookup"><span data-stu-id="95f6d-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="95f6d-124">Oppfylle servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="95f6d-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="95f6d-125">Gi service til kunder og fakturer serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="95f6d-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="95f6d-126">Yte service</span><span class="sxs-lookup"><span data-stu-id="95f6d-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="95f6d-127">Se også</span><span class="sxs-lookup"><span data-stu-id="95f6d-127">See Also</span></span>  
<span data-ttu-id="95f6d-128">[Håndtere fordringer](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="95f6d-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="95f6d-129">[Prosjekter](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="95f6d-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="95f6d-130">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span><span class="sxs-lookup"><span data-stu-id="95f6d-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
