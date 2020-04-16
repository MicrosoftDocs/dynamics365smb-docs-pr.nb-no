---
title: Eksportere og importere arbeidsflyter | Microsoft-dokumentasjon
description: For å overføre arbeidsflyter til andre Business Central-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2d309940d177491ce24f49884f388a5c233147fa
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188279"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="f3207-103">Importere og eksportere arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f3207-103">Export and Import Workflows</span></span>
<span data-ttu-id="f3207-104">For å overføre arbeidsflyter til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, for eksempel for å spare tid når du oppretter nye arbeidsflyter, kan du eksportere og importere arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="f3207-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="f3207-105">En annen måte å raskt opprette arbeidsflyter på er å opprette arbeidsflyter fra arbeidsflytmaler.</span><span class="sxs-lookup"><span data-stu-id="f3207-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="f3207-106">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f3207-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="f3207-107">På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene.</span><span class="sxs-lookup"><span data-stu-id="f3207-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="f3207-108">Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer.</span><span class="sxs-lookup"><span data-stu-id="f3207-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="f3207-109">Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.</span><span class="sxs-lookup"><span data-stu-id="f3207-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="f3207-110">Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f3207-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="f3207-111">Slik eksporterer du en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f3207-111">To export a workflow</span></span>  
1.  <span data-ttu-id="f3207-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f3207-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3207-113">Velg en arbeidsflyt, og velg deretter **Eksporter til fil**.</span><span class="sxs-lookup"><span data-stu-id="f3207-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="f3207-114">Velg **Lagre** på siden **Eksporter fil**.</span><span class="sxs-lookup"><span data-stu-id="f3207-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="f3207-115">På **Eksport**-siden velger du en filplassering, og deretter velger du **Lagre**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f3207-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="f3207-116">Slik importerer du en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f3207-116">To import a workflow</span></span>  
1.  <span data-ttu-id="f3207-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f3207-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3207-118">Velg handlingen **Importer fra fil**.</span><span class="sxs-lookup"><span data-stu-id="f3207-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="f3207-119">På **Import**-siden velger du XML-filen som inneholder arbeidsflyten, og deretter velger du **Åpne**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f3207-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="f3207-120">Hvis arbeidsflytkoden allerede finnes i databasen, overskrives arbeidsflyttrinnene med trinnene i den importerte arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="f3207-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3207-121">Se også</span><span class="sxs-lookup"><span data-stu-id="f3207-121">See Also</span></span>  
 <span data-ttu-id="f3207-122">[Opprette arbeidsflyter](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="f3207-123">[Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="f3207-124">[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="f3207-125">[Slette arbeidsflyter](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="f3207-126">[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="f3207-127">[Konfigurere arbeidsflyter](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="f3207-128">[Bruke arbeidsflyter](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f3207-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="f3207-129">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f3207-129">Workflow</span></span>](across-workflow.md)   
