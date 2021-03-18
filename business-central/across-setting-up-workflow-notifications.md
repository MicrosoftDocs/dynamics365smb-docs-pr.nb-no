---
title: Arbeidsflytvarslinger
description: Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren. I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: d11a391a7fd91f6a094dfae9f8908ba4314b357a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378951"
---
# <a name="workflow-notifications"></a><span data-ttu-id="37a8b-106">Arbeidsflytvarslinger</span><span class="sxs-lookup"><span data-stu-id="37a8b-106">Workflow Notifications</span></span>

<span data-ttu-id="37a8b-107">Konfigurere arbeidsflytene slik at de automatisk varsler brukere når de må det må utføres handlinger for et trinn i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="37a8b-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="37a8b-108">Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med.</span><span class="sxs-lookup"><span data-stu-id="37a8b-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="37a8b-109">I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren.</span><span class="sxs-lookup"><span data-stu-id="37a8b-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="37a8b-110">I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten.</span><span class="sxs-lookup"><span data-stu-id="37a8b-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="37a8b-111">Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning.</span><span class="sxs-lookup"><span data-stu-id="37a8b-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="37a8b-112">Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="37a8b-113">Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter varsler som e-post og interne merknader.</span><span class="sxs-lookup"><span data-stu-id="37a8b-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="37a8b-114">Alle arbeidsflytvarsler sendes via en jobbkø.</span><span class="sxs-lookup"><span data-stu-id="37a8b-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="37a8b-115">Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler, og at det er merket av for **Start automatisk fra server**.</span><span class="sxs-lookup"><span data-stu-id="37a8b-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="37a8b-116">Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="37a8b-117">Konfigurer varslinger</span><span class="sxs-lookup"><span data-stu-id="37a8b-117">Set up notifications</span></span>

<span data-ttu-id="37a8b-118">Du kan definere ulike aspekter ved arbeidsflytvarsler på følgende steder:</span><span class="sxs-lookup"><span data-stu-id="37a8b-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="37a8b-119">Godkjenner-varsling</span><span class="sxs-lookup"><span data-stu-id="37a8b-119">Approver notification</span></span>

    <span data-ttu-id="37a8b-120">For arbeidsflyter for godkjenning angir du mottakerne av arbeidsflytvarsler ved å fylle en linje på siden **Brukeroppsett for godkjenning** for hver bruker som tar del i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="37a8b-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="37a8b-121">Hvis for eksempel bruker 2 er angitt i **Godkjenner-ID**-feltet på linjen for bruker 1, sendes varselet om godkjenningsforespørsel til bruker 1.</span><span class="sxs-lookup"><span data-stu-id="37a8b-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="37a8b-122">Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="37a8b-123">Tidsplaner for varsling</span><span class="sxs-lookup"><span data-stu-id="37a8b-123">Notification schedules</span></span>

    <span data-ttu-id="37a8b-124">Du kan angi når og hvordan brukere skal motta arbeidsflytvarsler, ved å fylle ut siden **Tidsplan for varsling** for hver arbeidsflytbruker.</span><span class="sxs-lookup"><span data-stu-id="37a8b-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="37a8b-125">Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="37a8b-126">Tilpass e-postvarslingene</span><span class="sxs-lookup"><span data-stu-id="37a8b-126">Customize the email notifications</span></span>

    <span data-ttu-id="37a8b-127">Hvis du vil, kan du tilpasse innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="37a8b-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="37a8b-128">Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="37a8b-129">Svaralternativer</span><span class="sxs-lookup"><span data-stu-id="37a8b-129">Response options</span></span>

    <span data-ttu-id="37a8b-130">Du definerer det bestemte innholdet og reglene for et arbeidsflytvarsel når du oppretter den aktuelle arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="37a8b-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="37a8b-131">Dette gjør du ved å velge alternativer på siden **Alternativer for arbeidsflytsvar** for arbeidsflytsvaret som representerer varslingen.</span><span class="sxs-lookup"><span data-stu-id="37a8b-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="37a8b-132">Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="37a8b-133">Varsle avsender</span><span class="sxs-lookup"><span data-stu-id="37a8b-133">Notify sender</span></span>

    <span data-ttu-id="37a8b-134">For arbeidsflyter for godkjenning legger du til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist.</span><span class="sxs-lookup"><span data-stu-id="37a8b-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="37a8b-135">Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="37a8b-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="37a8b-136">Se også</span><span class="sxs-lookup"><span data-stu-id="37a8b-136">See Also</span></span>

[<span data-ttu-id="37a8b-137">Konfigurere godkjenningsbrukere</span><span class="sxs-lookup"><span data-stu-id="37a8b-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="37a8b-138">Konfigurere arbeidsflytbrukere</span><span class="sxs-lookup"><span data-stu-id="37a8b-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="37a8b-139">Angi når og hvor du kan motta varsler</span><span class="sxs-lookup"><span data-stu-id="37a8b-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="37a8b-140">Opprette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="37a8b-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="37a8b-141">Opprette og endre et egendefinert rapportoppsett</span><span class="sxs-lookup"><span data-stu-id="37a8b-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="37a8b-142">Bruke jobbkøer til å planlegge oppgaver</span><span class="sxs-lookup"><span data-stu-id="37a8b-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="37a8b-143">Konfigurere e-post</span><span class="sxs-lookup"><span data-stu-id="37a8b-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="37a8b-144">Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning</span><span class="sxs-lookup"><span data-stu-id="37a8b-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="37a8b-145">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="37a8b-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]