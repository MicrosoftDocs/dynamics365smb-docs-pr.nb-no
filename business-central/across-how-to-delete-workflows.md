---
title: Slette arbeidsflyter | Microsoft-dokumentasjon
description: Hvis du er sikker på at en arbeidsflyt ikke lenger er i bruk, kan du slette den. Alle forekomster av arbeidsflyttrinn som er definert i arbeidsflyten, må ha statusen **Fullført**.
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
ms.openlocfilehash: 31a92e70e044a82313b5329ed2bf007b2b809c11
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244937"
---
# <a name="delete-workflows"></a><span data-ttu-id="00c03-104">Slette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="00c03-104">Delete Workflows</span></span>
<span data-ttu-id="00c03-105">Hvis du er sikker på at en arbeidsflyt ikke lenger er i bruk, kan du slette den.</span><span class="sxs-lookup"><span data-stu-id="00c03-105">If you are certain that a workflow is no longer being used, you can delete it.</span></span> <span data-ttu-id="00c03-106">Alle forekomster av arbeidsflyttrinn som er definert i arbeidsflyten, må ha statusen **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="00c03-106">All workflow step instances that are defined in the workflow must have status **Completed**.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="00c03-107">Når du sletter en arbeidsflyt, vil all informasjon i arbeidsflyten gå tapt.</span><span class="sxs-lookup"><span data-stu-id="00c03-107">When you delete a workflow, all information in the workflow will be lost.</span></span>  

 <span data-ttu-id="00c03-108">På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="00c03-108">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="00c03-109">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="00c03-109">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="00c03-110">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="00c03-110">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="00c03-111">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="00c03-111">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-delete-a-workflow"></a><span data-ttu-id="00c03-112">Slik sletter du en arbeidsflyt:</span><span class="sxs-lookup"><span data-stu-id="00c03-112">To delete a workflow</span></span>  
1.  <span data-ttu-id="00c03-113">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="00c03-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="00c03-114">Velg arbeidsflyten du vil slette.</span><span class="sxs-lookup"><span data-stu-id="00c03-114">Select the workflow that you want to delete.</span></span>  
3.  <span data-ttu-id="00c03-115">Velg handlingen **Slett**.</span><span class="sxs-lookup"><span data-stu-id="00c03-115">Choose the **Delete** action.</span></span>  
4.  <span data-ttu-id="00c03-116">Åpne eventuelt arbeidsflyten du vil slette.</span><span class="sxs-lookup"><span data-stu-id="00c03-116">Alternatively, open the workflow that you want to delete.</span></span>  
5.  <span data-ttu-id="00c03-117">Velg **Slett**-handlingen på **Arbeidsflyt**-siden.</span><span class="sxs-lookup"><span data-stu-id="00c03-117">On the **Workflow** page, choose the **Delete** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00c03-118">Se også</span><span class="sxs-lookup"><span data-stu-id="00c03-118">See Also</span></span>  
 <span data-ttu-id="00c03-119">[Opprette arbeidsflyter](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-119">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="00c03-120">[Aktivere arbeidsflyter](across-how-to-enable-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-120">[Enable Workflows](across-how-to-enable-workflows.md) </span></span>  
 <span data-ttu-id="00c03-121">[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-121">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="00c03-122">[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-122">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="00c03-123">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-123">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="00c03-124">[Bruke arbeidsflyter](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="00c03-124">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="00c03-125">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="00c03-125">Workflow</span></span>](across-workflow.md)   
