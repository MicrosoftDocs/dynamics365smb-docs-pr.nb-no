---
title: Arbeidsflyt | Microsoft-dokumentasjon
description: Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 38092f364d1dee1f34d8aa0c0858ac1bc04d829b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378801"
---
# <a name="workflows-in-dynamics-365-business-central"></a><span data-ttu-id="d1415-105">Arbeidsflyter i Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="d1415-105">Workflows in Dynamics 365 Business Central</span></span>

<span data-ttu-id="d1415-106">Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="d1415-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="d1415-107">Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver.</span><span class="sxs-lookup"><span data-stu-id="d1415-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="d1415-108">Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="d1415-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="d1415-109">På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="d1415-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d1415-110">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="d1415-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d1415-111">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="d1415-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="d1415-112">Standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] omfatter en rekke forhåndskonfigurerte arbeidsflyter representert av arbeidsflytmaler som du kan kopiere for å opprette arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="d1415-112">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="d1415-113">Koden for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-".</span><span class="sxs-lookup"><span data-stu-id="d1415-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="d1415-114">Hvis du vil ha mer informasjon, kan du se listen over arbeidsflytmaler på siden Arbeidsflytmaler.</span><span class="sxs-lookup"><span data-stu-id="d1415-114">For more information, see the list of workflow templates in the Workflow Templates page.</span></span>  

 <span data-ttu-id="d1415-115">Hvis et forretningsscenario krever en arbeidsflythendelse eller et arbeidsflytsvar som ikke støttes, kan du bruke Power Automate eller samarbeide med en Microsoft-partner for å tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="d1415-115">If a business scenario requires a workflow event or response that is not supported, you can either use Power Automate or work with a Microsoft partner to customize the application code.</span></span> <span data-ttu-id="d1415-116">Hvis du vil ha mer informasjon, kan du se [Bruke [!INCLUDE[prod_short](includes/prod_short.md)] i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d1415-116">For more information, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>

<span data-ttu-id="d1415-117">Alle arbeidsflytmaler du oppretter med Power Automate, legges til i listen over arbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d1415-117">Any workflow template that you create with Power Automate is added to the list of workflow templates within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d1415-118">Hvis du vil ha mer informasjon, se [Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="d1415-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="d1415-119">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="d1415-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="d1415-120">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="d1415-120">**To**</span></span>|<span data-ttu-id="d1415-121">**Se**</span><span class="sxs-lookup"><span data-stu-id="d1415-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="d1415-122">Definer arbeidsflytbrukere, angi hvordan brukere skal varsles, og opprett nye arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="d1415-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="d1415-123">For nye arbeidsflyter for scenarier som ikke støttes, kan du implementere nødvendige arbeidsflytelementer ved å tilpasse programkoden.</span><span class="sxs-lookup"><span data-stu-id="d1415-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="d1415-124">Konfigurere arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="d1415-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="d1415-125">Aktiver arbeidsflyter, handle på arbeidsflytvarsler, inkludert forespørselsgodkjenninger, og godkjenn forespørsler om å utføre et arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="d1415-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="d1415-126">Arkiver og slett arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="d1415-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="d1415-127">Bruke arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="d1415-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="d1415-128">Se også</span><span class="sxs-lookup"><span data-stu-id="d1415-128">See Also</span></span>

[<span data-ttu-id="d1415-129">Salg</span><span class="sxs-lookup"><span data-stu-id="d1415-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d1415-130">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="d1415-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="d1415-131">Administrere prosjekter</span><span class="sxs-lookup"><span data-stu-id="d1415-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="d1415-132">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1415-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]