---
title: Opprette arbeidsflyter fra arbeidsflytmaler | Microsoft-dokumentasjon
description: "For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0f923c6d40093f35eb051e69ec149c3296bd0ee7
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="21119-103">Opprette arbeidsflyter fra arbeidsflytmaler</span><span class="sxs-lookup"><span data-stu-id="21119-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="21119-104">For å spare tid når du oppretter nye arbeidsflyter, kan du opprette arbeidsflyter fra arbeidsflytmaler.</span><span class="sxs-lookup"><span data-stu-id="21119-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="21119-105">Arbeidsflytmaler er ikke-redigerbare arbeidsflyter som finnes i den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="21119-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="21119-106">Kodene for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-".</span><span class="sxs-lookup"><span data-stu-id="21119-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="21119-107">En annen måte å raskt opprette en arbeidsflyt på er å importere en eksisterende arbeidsflyt som du har på en fil utenfor [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="21119-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="21119-108">Hvis du vil ha mer informasjon, kan du se [Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="21119-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="21119-109">I **Arbeidsflyt**-vinduet oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="21119-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="21119-110">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="21119-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="21119-111">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="21119-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="21119-112">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="21119-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="21119-113">Slik oppretter du en arbeidsflyt fra arbeidsflytmaler</span><span class="sxs-lookup"><span data-stu-id="21119-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="21119-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="21119-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="21119-115">Velg handlingen **Opprett arbeidsflyt fra mal**.</span><span class="sxs-lookup"><span data-stu-id="21119-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="21119-116">Vinduet **Arbeidsflytmaler** åpnes.</span><span class="sxs-lookup"><span data-stu-id="21119-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="21119-117">Velg en arbeidsflytmal, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="21119-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="21119-118">**Arbeidsflyt**-vinduet åpnes for en ny arbeidsflyt som inneholder all informasjon for den valgte malen.</span><span class="sxs-lookup"><span data-stu-id="21119-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="21119-119">Verdien i **Kode**-feltet utvides med for eksempel "-01" for å angi at dette er den første arbeidsflyten som er opprettet fra arbeidsflytmalen.</span><span class="sxs-lookup"><span data-stu-id="21119-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="21119-120">Fortsett med å opprette arbeidsflyten ved å redigere de arbeidsflyttrinnene eller legge til nye trinn.</span><span class="sxs-lookup"><span data-stu-id="21119-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="21119-121">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="21119-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="21119-122">Se også</span><span class="sxs-lookup"><span data-stu-id="21119-122">See Also</span></span>  
 <span data-ttu-id="21119-123">[Opprette arbeidsflyter](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="21119-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="21119-124">[Importere og eksportere arbeidsflyter](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="21119-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="21119-125">[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="21119-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="21119-126">[Slette arbeidsflyter](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="21119-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="21119-127">[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="21119-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="21119-128">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="21119-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="21119-129">[Bruke arbeidsflyter](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="21119-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="21119-130">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="21119-130">Workflow</span></span>](across-workflow.md)   

