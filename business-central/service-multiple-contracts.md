---
title: Flere kontrakter | Microsoft-dokumentasjon
description: Avhengig av servicenivåavtalene du har med kunden, må du kanskje behandle en servicevare på flere enn én servicekontrakt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6410f1b96aa1c1f8251738184db07aba0d94c4b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915288"
---
# <a name="multiple-contracts"></a><span data-ttu-id="85775-103">Flere kontrakter</span><span class="sxs-lookup"><span data-stu-id="85775-103">Multiple Contracts</span></span>
<span data-ttu-id="85775-104">Avhengig av servicenivåavtalene du har med kunden, må du kanskje behandle en servicevare på flere enn én servicekontrakt.</span><span class="sxs-lookup"><span data-stu-id="85775-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="85775-105">Ved å behandle en servicevare for flere kontrakter, kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="85775-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="85775-106">Utstede forskjellige kontrakter for samme servicevare.</span><span class="sxs-lookup"><span data-stu-id="85775-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="85775-107">Foreta service på deler separat.</span><span class="sxs-lookup"><span data-stu-id="85775-107">Service parts separately.</span></span>  
* <span data-ttu-id="85775-108">Vurder forskjellig kompetanse som kreves for å foreta service på forskjellige deler av en servicevare, for eksempel mekaniske komponenter og programvare.</span><span class="sxs-lookup"><span data-stu-id="85775-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="85775-109">Angi forskjellige responstider og -frekvenser for service på forskjellige deler av servicevaren.</span><span class="sxs-lookup"><span data-stu-id="85775-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="85775-110">Gå i gang med forskjellige aktiviteter som må utføres på en servicevare, når servicevaren krever forskjellige typer service, til forskjellige tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="85775-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="85775-111">Velg og tilordne et riktig kontraktnummer til en servicevarelinje når du oppretter en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="85775-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="85775-112">Behandle relevant finansiell informasjon om servicevarer og servicenivåavtaler.</span><span class="sxs-lookup"><span data-stu-id="85775-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="85775-113">Vurder følgende eksempler for bruk av flerkontraktsfunksjonalitet:</span><span class="sxs-lookup"><span data-stu-id="85775-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="85775-114">Opprette flere kontrakter per servicevare</span><span class="sxs-lookup"><span data-stu-id="85775-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="85775-115">Du kan opprette en servicekontrakt eller et kontrakttilbud manuelt for servicevarer som allerede er registrert i ikke-avbrutte kontrakter som tilhører av samme kunde.</span><span class="sxs-lookup"><span data-stu-id="85775-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="85775-116">Følg vanlig fremgangsmåte for opprettelse av servicekontrakter og servicekontrakttilbud når du skal gjøre dette.</span><span class="sxs-lookup"><span data-stu-id="85775-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="85775-117">Hvis du vil ha mer informasjon, kan du se [Arbeide med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="85775-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="85775-118">Når du legger til en servicevare på en kontraktlinje som er registrert i andre servicekontrakter eller kontrakttilbud, vises en advarsel som sier at servicevaren allerede tilhører én eller flere servicekontrakter eller kontrakttilbud.</span><span class="sxs-lookup"><span data-stu-id="85775-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="85775-119">Hvis du bekrefter denne meldingen, kopieres alle aktuelle servicevareopplysninger til en nyopprettet kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="85775-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="85775-120">Kopiere dokumenter</span><span class="sxs-lookup"><span data-stu-id="85775-120">Copying Documents</span></span>  
<span data-ttu-id="85775-121">Du kan automatisk opprette en servicekontrakt eller et kontrakttilbud for servicevarer som allerede er registrert i andre servicekontrakter eller kontrakttilbud, ved å bruke handlingen **Kopier fra dokument**.</span><span class="sxs-lookup"><span data-stu-id="85775-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy from Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="85775-122">Opprette serviceordrer for flere kontrakter</span><span class="sxs-lookup"><span data-stu-id="85775-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="85775-123">Du kan manuelt opprette en serviceordre for en servicevare som er registrert i flere aktive kontrakter.</span><span class="sxs-lookup"><span data-stu-id="85775-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="85775-124">En servicekontrakt er aktiv hvis den er undertegnet og ikke er utgått.</span><span class="sxs-lookup"><span data-stu-id="85775-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85775-125">Se også</span><span class="sxs-lookup"><span data-stu-id="85775-125">See Also</span></span>  
[<span data-ttu-id="85775-126">Oppfylle servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="85775-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="85775-127">Opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="85775-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
