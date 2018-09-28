---
title: Arbeidsflyt | Microsoft-dokumentasjon
description: "Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7a7782fcb51eb9078cb62c4892814cd178518332
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="workflow"></a><span data-ttu-id="040e5-105">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="040e5-105">Workflow</span></span>
<span data-ttu-id="040e5-106">Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="040e5-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="040e5-107">Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver.</span><span class="sxs-lookup"><span data-stu-id="040e5-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="040e5-108">Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="040e5-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="040e5-109">I **Arbeidsflyt**-vinduet oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="040e5-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="040e5-110">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="040e5-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="040e5-111">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="040e5-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="040e5-112">Standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] omfatter en rekke forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="040e5-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="040e5-113">Koden for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-".</span><span class="sxs-lookup"><span data-stu-id="040e5-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="040e5-114">Hvis du vil ha mer informasjon, kan du se listen over arbeidsflytmaler i vinduet Arbeidsflytmaler.</span><span class="sxs-lookup"><span data-stu-id="040e5-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="040e5-115">Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, må en Microsoft-partner implementere dem ved å tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="040e5-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="040e5-116">Hvis du vil ha mer informasjon, kan du se [Gjennomgang: Implementering av nye arbeidsflythendelser og svar](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) i hjelpen for utviklere og IT-eksperter.</span><span class="sxs-lookup"><span data-stu-id="040e5-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="040e5-117">Arbeidsflyter kan også startes fra Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="040e5-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="040e5-118">Hvis du vil ha mer informasjon, se [Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="040e5-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="040e5-119">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="040e5-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="040e5-120">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="040e5-120">**To**</span></span>|<span data-ttu-id="040e5-121">**Se**</span><span class="sxs-lookup"><span data-stu-id="040e5-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="040e5-122">Definer arbeidsflytbrukere, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="040e5-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="040e5-123">For nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="040e5-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="040e5-124">Konfigurere arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="040e5-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="040e5-125">Aktiver arbeidsflyter, handle på arbeidsflytvarsler, inkludert forespørselsgodkjenninger, og godkjenn forespørsler om å utføre et arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="040e5-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="040e5-126">Arkiver og slett arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="040e5-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="040e5-127">Bruke arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="040e5-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="040e5-128">Se også</span><span class="sxs-lookup"><span data-stu-id="040e5-128">See Also</span></span>  
[<span data-ttu-id="040e5-129">Salg</span><span class="sxs-lookup"><span data-stu-id="040e5-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="040e5-130">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="040e5-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="040e5-131">Administrere prosjekter</span><span class="sxs-lookup"><span data-stu-id="040e5-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="040e5-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="040e5-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

