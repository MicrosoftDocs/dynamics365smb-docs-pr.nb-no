---
title: Opprette arbeidsflyter fra arbeidsflytmaler | Microsoft-dokumentasjon
description: For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 407bf7cd60416a178e9ec8a5d0b154a7583e87e1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754845"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="46efc-103">Opprette arbeidsflyter fra arbeidsflytmaler</span><span class="sxs-lookup"><span data-stu-id="46efc-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="46efc-104">For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler.</span><span class="sxs-lookup"><span data-stu-id="46efc-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="46efc-105">Arbeidsflytmaler er ikke-redigerbare arbeidsflyter som finnes i den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="46efc-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="46efc-106">Kodene for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-".</span><span class="sxs-lookup"><span data-stu-id="46efc-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="46efc-107">En annen måte å raskt opprette en arbeidsflyt på er å importere en eksisterende arbeidsflyt som du har på en fil utenfor [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="46efc-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="46efc-108">Hvis du vil ha mer informasjon, kan du se [Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="46efc-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="46efc-109">På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="46efc-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="46efc-110">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="46efc-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="46efc-111">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="46efc-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="46efc-112">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="46efc-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="46efc-113">Slik oppretter du en arbeidsflyt fra arbeidsflytmaler</span><span class="sxs-lookup"><span data-stu-id="46efc-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="46efc-114">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="46efc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="46efc-115">Velg handlingen **Opprett arbeidsflyt fra mal**.</span><span class="sxs-lookup"><span data-stu-id="46efc-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="46efc-116">Siden **Arbeidsflytmaler** åpnes.</span><span class="sxs-lookup"><span data-stu-id="46efc-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="46efc-117">Velg en arbeidsflytmal, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="46efc-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="46efc-118">**Arbeidsflyt**-siden åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="46efc-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="46efc-119">Verdien i **Kode**-feltet utvides med for eksempel "-01" for å angi at dette er den første arbeidsflyten som er opprettet fra arbeidsflytmalen.</span><span class="sxs-lookup"><span data-stu-id="46efc-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="46efc-120">Fortsett med å opprette arbeidsflyten ved å redigere de arbeidsflyttrinnene eller legge til nye trinn.</span><span class="sxs-lookup"><span data-stu-id="46efc-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="46efc-121">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="46efc-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="46efc-122">Se også</span><span class="sxs-lookup"><span data-stu-id="46efc-122">See Also</span></span>  
 <span data-ttu-id="46efc-123">[Opprette arbeidsflyter](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="46efc-124">[Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="46efc-125">[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="46efc-126">[Slette arbeidsflyter](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="46efc-127">[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="46efc-128">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="46efc-129">[Bruke arbeidsflyter](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="46efc-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="46efc-130">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="46efc-130">Workflow</span></span>](across-workflow.md)   
