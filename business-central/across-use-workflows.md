---
title: Bruke arbeidsflyter | Microsoft-dokumentasjon
description: Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.
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
ms.openlocfilehash: e5dee76fa49d66d72c7e20cb9ff5eead63cf37aa
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "928349"
---
# <a name="using-workflows"></a><span data-ttu-id="f3ab4-105">Bruke arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f3ab4-105">Using Workflows</span></span>
<span data-ttu-id="f3ab4-106">Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="f3ab4-107">Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="f3ab4-108">Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="f3ab4-109">Før du kan begynne å bruke arbeidsflyter, må du konfigurere brukere av arbeidsflyt, opprette arbeidsflytene, potensielt med foranstilt tilpasset kode, og angi hvordan brukere mottar varsler.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="f3ab4-110">Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflyter](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f3ab4-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f3ab4-111">Vanlige arbeidsflyttrinn er om brukere som ber om godkjenning av oppgaver og godkjennere som godkjenner eller avviser forespørsler om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="f3ab4-112">Mange emner om hvordan du bruker arbeidsflyter, refererer derfor til godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="f3ab4-113">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="f3ab4-114">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="f3ab4-114">**To**</span></span>|<span data-ttu-id="f3ab4-115">**Se**</span><span class="sxs-lookup"><span data-stu-id="f3ab4-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="f3ab4-116">Angi at en arbeidsflyt skal starte når den første innpunkthendelsen oppstår.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="f3ab4-117">Aktivere arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f3ab4-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="f3ab4-118">Be om godkjenning for en oppgave, som godkjenner, godkjenn, avvis eller deleger godkjenning, og send eller vis godkjenningsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="f3ab4-119">Bruke arbeidsflyter for godkjenning</span><span class="sxs-lookup"><span data-stu-id="f3ab4-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="f3ab4-120">Opprett trinn i arbeidsflyten som forhindrer at en bestemt oppføringstype brukes før en bestemt hendelse inntreffer, for eksempel at oppføringen er godkjent.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="f3ab4-121">Begrense og tillate bruk av en post</span><span class="sxs-lookup"><span data-stu-id="f3ab4-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="f3ab4-122">Vise forekomster av arbeidsflyttrinn med statusen Fullført.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="f3ab4-123">Vise arkiverte forekomster av arbeidsflyttrinn</span><span class="sxs-lookup"><span data-stu-id="f3ab4-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="f3ab4-124">Slette en arbeidsflyt du er sikker på ikke lenger vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="f3ab4-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="f3ab4-125">Slette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f3ab4-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="f3ab4-126">Se også</span><span class="sxs-lookup"><span data-stu-id="f3ab4-126">See Also</span></span>  
<span data-ttu-id="f3ab4-127">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f3ab4-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="f3ab4-128">[Arbeidsflyt](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f3ab4-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="f3ab4-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3ab4-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
