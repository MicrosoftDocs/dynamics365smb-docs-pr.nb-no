---
title: Bokføre flere dokumenter samtidig | Microsoft Docs
description: I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for massebokføring, enten det er for umiddelbar bokføring eller planlagt, for eksempel på slutten av dagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: 2c04dac37b043995a9b78e2f662f9411c3cf9ae1
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782521"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="0c289-103">Bokføre flere dokumenter samtidig</span><span class="sxs-lookup"><span data-stu-id="0c289-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="0c289-104">I stedet for å bokføre enkeltdokumenter én etter én, kan du velge flere dokumenter som ikke er bokført, i en liste for umiddelbar bokføring eller massebokføring i henhold til en tidsplan, for eksempel på slutten av dagen.</span><span class="sxs-lookup"><span data-stu-id="0c289-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="0c289-105">Dette kan være nyttig hvis bare en arbeidsleder kan bokføre dokumenter som er opprettet av andre brukere, eller for å unngå problemer med systemytelse ved bokføring i arbeidstiden.</span><span class="sxs-lookup"><span data-stu-id="0c289-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="0c289-106">Bokføre flere bestillinger umiddelbart</span><span class="sxs-lookup"><span data-stu-id="0c289-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="0c289-107">Fremgangsmåten nedenfor forklarer hvordan du bokfører flere bestillinger umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="0c289-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="0c289-108">Trinnene er lignende for alle kjøps- og salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="0c289-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="0c289-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0c289-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c289-110">På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:</span><span class="sxs-lookup"><span data-stu-id="0c289-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="0c289-111">I **Nr.**</span><span class="sxs-lookup"><span data-stu-id="0c289-111">In the **No.**</span></span> <span data-ttu-id="0c289-112">-feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.</span><span class="sxs-lookup"><span data-stu-id="0c289-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="0c289-113">Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.</span><span class="sxs-lookup"><span data-stu-id="0c289-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="0c289-114">Velg handlingen **Bokføring**, og velg deretter handlingen **Bokfør**.</span><span class="sxs-lookup"><span data-stu-id="0c289-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="0c289-115">Velg **Ja** i bekreftelsesmeldingen.</span><span class="sxs-lookup"><span data-stu-id="0c289-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="0c289-116">Massebokføre flere bestillinger</span><span class="sxs-lookup"><span data-stu-id="0c289-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="0c289-117">Fremgangsmåten nedenfor forklarer hvordan du massebokfører bestillinger.</span><span class="sxs-lookup"><span data-stu-id="0c289-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="0c289-118">Trinnene er de samme for alle kjøps- og salgsdokumenter der handlingen **Massebokfør** er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="0c289-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="0c289-119">Massebokføring av dokumenter skjer i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="0c289-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="0c289-120">[!INCLUDE [prodshort](includes/prodshort.md)] Online omfatter standardjobber for bakgrunnsbokføring og massebokføring.</span><span class="sxs-lookup"><span data-stu-id="0c289-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="0c289-121">Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0c289-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="0c289-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0c289-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0c289-123">På **Bestilling**-siden fortsetter du for å velge alle bestillinger som skal bokføres:</span><span class="sxs-lookup"><span data-stu-id="0c289-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="0c289-124">I **Nr.**</span><span class="sxs-lookup"><span data-stu-id="0c289-124">In the **No.**</span></span> <span data-ttu-id="0c289-125">-feltet velger du de tre loddrette prikkene for å åpne hurtigmenyen, og deretter velger du handlingen **Velg flere**.</span><span class="sxs-lookup"><span data-stu-id="0c289-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="0c289-126">Merk av i boksen for alle linjene som representerer ordrer du vil bokføre samtidig.</span><span class="sxs-lookup"><span data-stu-id="0c289-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="0c289-127">Velg handlingen **Bokføring**, og velg deretter handlingen **Massebokfør**.</span><span class="sxs-lookup"><span data-stu-id="0c289-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="0c289-128">På siden **Bestillinger - massebokfør** fyller du ut resten av feltene.</span><span class="sxs-lookup"><span data-stu-id="0c289-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="0c289-129">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0c289-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="0c289-130">Hvis du vil vise potensielle problemer som oppstod under massebokføring av dokumenter, åpner du siden **Feilmeldingsregister**.</span><span class="sxs-lookup"><span data-stu-id="0c289-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="0c289-131">Bestillingene blir nå lagt til i en dedikert jobbkø, som definerer når dokumentene bokføres.</span><span class="sxs-lookup"><span data-stu-id="0c289-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="0c289-132">Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0c289-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="0c289-133">Hvis du velger **PDF** i feltet **Rapportutdatatype**, vil bokførte bestillinger være tilgjengelige i delen **Rapportinnboks** i rollesenteret.</span><span class="sxs-lookup"><span data-stu-id="0c289-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c289-134">Se også</span><span class="sxs-lookup"><span data-stu-id="0c289-134">See Also</span></span>

[<span data-ttu-id="0c289-135">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="0c289-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="0c289-136">Bruke jobbkøer til å planlegge oppgaver</span><span class="sxs-lookup"><span data-stu-id="0c289-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="0c289-137">Redigere bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="0c289-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="0c289-138">Korrigere eller annullere ubetalte kjøpsfakturaer</span><span class="sxs-lookup"><span data-stu-id="0c289-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="0c289-139">Finne sider og informasjon med Fortell meg</span><span class="sxs-lookup"><span data-stu-id="0c289-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="0c289-140">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c289-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
