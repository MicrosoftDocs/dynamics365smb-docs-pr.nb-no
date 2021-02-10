---
title: Bruke arbeidsflyter
description: Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Finn ut mer om de ulike trinnene du må gjøre for å begynne å bruke arbeidsflyter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 375d53975bca97d16b3857056d44b9eada5cca97
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753003"
---
# <a name="using-workflows"></a><span data-ttu-id="6ba1e-104">Bruke arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="6ba1e-104">Using Workflows</span></span>
<span data-ttu-id="6ba1e-105">Du kan definere og bruke arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="6ba1e-106">Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="6ba1e-107">Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="6ba1e-108">Før du kan begynne å bruke arbeidsflyter, må du konfigurere brukere av arbeidsflyt, opprette arbeidsflytene, potensielt med foranstilt tilpasset kode, og angi hvordan brukere mottar varsler.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="6ba1e-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflyter](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="6ba1e-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6ba1e-110">Vanlige arbeidsflyttrinn er om brukere som ber om godkjenning av oppgaver og godkjennere som godkjenner eller avviser forespørsler om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="6ba1e-111">Mange emner om hvordan du bruker arbeidsflyter, refererer derfor til godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="6ba1e-112">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="6ba1e-113">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-113">**To**</span></span>|<span data-ttu-id="6ba1e-114">**Se**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6ba1e-115">Angi at en arbeidsflyt skal starte når den første innpunkthendelsen oppstår.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="6ba1e-116">Aktivere arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="6ba1e-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="6ba1e-117">Be om godkjenning for en oppgave, som godkjenner, godkjenn, avvis eller deleger godkjenning, og send eller vis godkjenningsmeldinger.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="6ba1e-118">Bruke arbeidsflyter for godkjenning</span><span class="sxs-lookup"><span data-stu-id="6ba1e-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="6ba1e-119">Opprett trinn i arbeidsflyten som forhindrer at en bestemt oppføringstype brukes før en bestemt hendelse inntreffer, for eksempel at oppføringen er godkjent.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="6ba1e-120">Begrense og tillate bruk av en post</span><span class="sxs-lookup"><span data-stu-id="6ba1e-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="6ba1e-121">Vise forekomster av arbeidsflyttrinn med statusen Fullført.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="6ba1e-122">Vise arkiverte forekomster av arbeidsflyttrinn</span><span class="sxs-lookup"><span data-stu-id="6ba1e-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="6ba1e-123">Slette en arbeidsflyt du er sikker på ikke lenger vil bli brukt.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="6ba1e-124">Slette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="6ba1e-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="6ba1e-125">Se også</span><span class="sxs-lookup"><span data-stu-id="6ba1e-125">See Also</span></span>  
<span data-ttu-id="6ba1e-126">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="6ba1e-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="6ba1e-127">[Arbeidsflyt](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="6ba1e-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="6ba1e-128">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ba1e-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
