---
title: "Definere hvilke inngående dokumenter som skal vises | Microsoft-dokumentasjon"
description: "Du kan justere standardvisningen for inngående dokumenter, for eksempel e-fakturaer, for å få bedre oversikt over behandlede og ubehandlede poster."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="93993-103">Håndtere mange inngående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="93993-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="93993-104">Når du oppretter eller behandle inngående dokumentposter, kan antall linjer i vinduet **Inngående dokumenter** øke så mye at du mister oversikten.</span><span class="sxs-lookup"><span data-stu-id="93993-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="93993-105">Derfor kan du sette inngående dokumentposter til Behandlet for å fjerne dem fra standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="93993-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="93993-106">Når du velger handlingen **Vis alle**, kan du vise både behandlede og ubehandlede poster.</span><span class="sxs-lookup"><span data-stu-id="93993-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="93993-107">Du kan ikke redigere informasjon, legge ved filer eller utføre andre prosesser på inngående dokumentposter som er satt til Behandlet.</span><span class="sxs-lookup"><span data-stu-id="93993-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="93993-108">Først må du sette det til Ubehandlet.</span><span class="sxs-lookup"><span data-stu-id="93993-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="93993-109">Det merkes automatisk av for **Behandlet** på inngående dokumentposter som har blitt behandlet, men du kan også merke av for eller fjerne merket manuelt.</span><span class="sxs-lookup"><span data-stu-id="93993-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="93993-110">Avhengig av forretningsprosessen, kan en inngående dokumentpost behandles når et relatert dokument er opprettet for det eller en fil er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="93993-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="93993-111">Når du åpner vinduet **Inngående dokumenter** med handlingen **Mine inngående dokumenter** i rollesenteret, vises bare ubehandlede inngående dokumentposter som standard.</span><span class="sxs-lookup"><span data-stu-id="93993-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="93993-112">I dette emnet kalles dette "standardvisningen".</span><span class="sxs-lookup"><span data-stu-id="93993-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="93993-113">Fjerne inngående dokumentposter fra standardvisningen</span><span class="sxs-lookup"><span data-stu-id="93993-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="93993-114">I vinduet **Inngående dokumenter** velger du én eller flere linjer for inngående dokumentposter som du vil fjerne fra standardvisning.</span><span class="sxs-lookup"><span data-stu-id="93993-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="93993-115">Velg handlingen **Satt til Behandlet**.</span><span class="sxs-lookup"><span data-stu-id="93993-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="93993-116">Inngående dokumentposter fjernes fra standardvisningen, og det merkes av for **Behandlet** på linjene.</span><span class="sxs-lookup"><span data-stu-id="93993-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="93993-117">Du kan også utføre denne handlingen for hver enkelt post i vinduet **Kort for inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="93993-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="93993-118">Vise alle inngående dokumentposter</span><span class="sxs-lookup"><span data-stu-id="93993-118">To view all incoming document records</span></span>
1. <span data-ttu-id="93993-119">I vinduet **Inngående dokumenter** velger du handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="93993-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="93993-120">Alle inngående dokumentposter vises, inkludert dem som det ikke er merket av for **Behandlet**.</span><span class="sxs-lookup"><span data-stu-id="93993-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="93993-121">Legge til inngående dokumentposter i standardvisningen</span><span class="sxs-lookup"><span data-stu-id="93993-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="93993-122">I vinduet **Inngående dokumenter** velger du handlingen **Vis alle**.</span><span class="sxs-lookup"><span data-stu-id="93993-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="93993-123">Velg én eller flere linjer for inngående dokumentposter som du vil skal vises i standardvisningen.</span><span class="sxs-lookup"><span data-stu-id="93993-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="93993-124">Velg handlingen **Satt til Ubehandlet**.</span><span class="sxs-lookup"><span data-stu-id="93993-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="93993-125">Du kan også utføre denne handlingen for hver enkelt post i vinduet **Kort for inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="93993-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="93993-126">Se også</span><span class="sxs-lookup"><span data-stu-id="93993-126">See Also</span></span>
[<span data-ttu-id="93993-127">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="93993-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="93993-128">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="93993-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="93993-129">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="93993-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="93993-130">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93993-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

