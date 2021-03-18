---
title: Definere timelister og godkjenningen av dem | Microsoft-dokumentasjon
description: Du definerer timelister for å spore tiden som brukes på prosjekter, og bruk av ressurser. Dette er til hjelp ved prosjektstyring, bemanning og kapasitet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7851966211a666e6569bffa3082d05b7c3765434
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388402"
---
# <a name="set-up-time-sheets"></a><span data-ttu-id="8f0bd-103">Definere timelister</span><span class="sxs-lookup"><span data-stu-id="8f0bd-103">Set Up Time Sheets</span></span>
<span data-ttu-id="8f0bd-104">Timelister i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ukentlige intervaller på sju dager.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-104">Time sheets in [!INCLUDE[prod_short](includes/prod_short.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="8f0bd-105">Du kan bruke dem til å spore tiden som brukes på prosjekter, og du kan bruke dem til å registrere enkel registrering av ressurstid.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="8f0bd-106">Før du kan bruke timelister, må du angi hvordan du vil at de skal settes opp og konfigureres.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="8f0bd-107">Når du har definert hvordan organisasjonen vil bruke timelister, kan du angi om og hvordan timelister er godkjent.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="8f0bd-108">Avhengig av behovene i organisasjonen, kan du angi:</span><span class="sxs-lookup"><span data-stu-id="8f0bd-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="8f0bd-109">En eller flere brukere som administrator for timeliste og godkjenning for alle timelister.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="8f0bd-110">En godkjenner av timelister for hver ressurs.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="8f0bd-111">Når du har definert timelister, kan du opprette timelister for ressurser, tilordne dem til planleggingslinjer og bokføre timelistelinjer.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="8f0bd-112">Hvis du vil ha mer informasjon, kan du se [Bruke timelister](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="8f0bd-112">For more information, see [Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="8f0bd-113">Slik definerer du generell informasjon for timelister</span><span class="sxs-lookup"><span data-stu-id="8f0bd-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="8f0bd-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0bd-115">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8f0bd-116">For feltet **Timeliste etter prosjektgodkjenning** velger du ett av følgende alternativer.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="8f0bd-117">Alternativ</span><span class="sxs-lookup"><span data-stu-id="8f0bd-117">Option</span></span> | <span data-ttu-id="8f0bd-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f0bd-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8f0bd-119">**Aldri**</span><span class="sxs-lookup"><span data-stu-id="8f0bd-119">**Never**</span></span> |<span data-ttu-id="8f0bd-120">Brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet godkjenner timelisten.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="8f0bd-121">**Alltid**</span><span class="sxs-lookup"><span data-stu-id="8f0bd-121">**Always**</span></span> |<span data-ttu-id="8f0bd-122">Brukeren i feltet **Ansvarlig person** på prosjektkortet godkjenner timelisten.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="8f0bd-123">**Bare maskin**</span><span class="sxs-lookup"><span data-stu-id="8f0bd-123">**Machine Only**</span></span> |<span data-ttu-id="8f0bd-124">Hvis timelisten for maskin er knyttet til et prosjekt, godkjenner brukeren i feltet **Ansvarlig person** på prosjektkortet, timelisten.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="8f0bd-125">Hvis timelisten for maskin er knyttet til en ressurs, godkjenner brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet, timelisten.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="8f0bd-126">Slik tilordner du en timelisteadministrator</span><span class="sxs-lookup"><span data-stu-id="8f0bd-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="8f0bd-127">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f0bd-128">Legg til en ny bruker hvis brukerlisten ikke inkluderer personen som du vil skal være ansvarlig for timelisteregistrering.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="8f0bd-129">Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8f0bd-129">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>
3. <span data-ttu-id="8f0bd-130">Velg en bruker som administrator for en timeliste, og merk deretter av for **Administrator for timeliste**</span><span class="sxs-lookup"><span data-stu-id="8f0bd-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.** check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="8f0bd-131">Det anbefales at du velger bare én bruker som administrator for timelisten i et selskap.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-131">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="8f0bd-132">I den følgende fremgangsmåten setter du opp en timelisteeier og -godkjenner, der godkjenneren av timelisten er tilordnet for hver ressurs.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-132">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="8f0bd-133">Slik tilordner du en timelisteeier og -godkjenner</span><span class="sxs-lookup"><span data-stu-id="8f0bd-133">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="8f0bd-134">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="8f0bd-135">Merk ressursen du vil definere muligheten til å bruke timelister for, og merk deretter av for **Bruk timeliste**.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-135">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="8f0bd-136">Angi ID-en for eieren av timelisten i feltet **Bruker-ID for eier av timeliste:**.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-136">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="8f0bd-137">Eieren kan angi tidsbruk på en timeliste og sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-137">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="8f0bd-138">Når ressursen er en person, er denne personen vanligvis også eieren.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-138">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="8f0bd-139">Angi ID-en for godkjenneren av timelisten i feltet **Bruker-ID for godkjenner av timeliste**.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-139">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="8f0bd-140">Godkjenneren kan godkjenne, avvise eller åpne på nytt en timeliste.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-140">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="8f0bd-141">Du kan ikke endre IDen for godkjenneren av timelisten hvis det finnes timelister som ennå ikke er behandlet og som har statusen **Sendt** eller **Åpen**.</span><span class="sxs-lookup"><span data-stu-id="8f0bd-141">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f0bd-142">Se også</span><span class="sxs-lookup"><span data-stu-id="8f0bd-142">See Also</span></span>
[<span data-ttu-id="8f0bd-143">Konfigurere prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="8f0bd-143">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="8f0bd-144">Prosjektstyring</span><span class="sxs-lookup"><span data-stu-id="8f0bd-144">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="8f0bd-145">Finans</span><span class="sxs-lookup"><span data-stu-id="8f0bd-145">Finance</span></span>](finance.md)  
<span data-ttu-id="8f0bd-146">[Innkjøp](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="8f0bd-146">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="8f0bd-147">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="8f0bd-147">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="8f0bd-148">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f0bd-148">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]