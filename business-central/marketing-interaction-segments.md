---
title: Holde rede på segmenter og relaterte samhandlinger | Microsoft-dokumentasjon
description: Finn ut hvordan du oppretter segmenter for å definere grupper med kontakter og angi samhandlinger for segmenter.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b57ae29a8825e29f5f6faaf536cb1411d74c127f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782091"
---
# <a name="manage-interactions-for-segments"></a><span data-ttu-id="4eede-103">Administrere samhandlinger for segmenter</span><span class="sxs-lookup"><span data-stu-id="4eede-103">Manage Interactions for Segments</span></span>
<span data-ttu-id="4eede-104">Siden **Segment** er en type forslag der du kan:</span><span class="sxs-lookup"><span data-stu-id="4eede-104">The **Segment** page is a type of worksheet where you can:</span></span>

* <span data-ttu-id="4eede-105">Opprette segmenter.</span><span class="sxs-lookup"><span data-stu-id="4eede-105">Create segments.</span></span>
* <span data-ttu-id="4eede-106">Lagre segmenteringskriteriene du har brukt til å velge kontakter.</span><span class="sxs-lookup"><span data-stu-id="4eede-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="4eede-107">Loggføre segmentet og registrere samhandlinger med kontaktene i segmentet.</span><span class="sxs-lookup"><span data-stu-id="4eede-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="4eede-108">Segmentering</span><span class="sxs-lookup"><span data-stu-id="4eede-108">Segmenting</span></span>
<span data-ttu-id="4eede-109">Du kan opprette segmenter på flere måter:</span><span class="sxs-lookup"><span data-stu-id="4eede-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="4eede-110">Du kan manuelt angi de kontaktene du vil ta med i segmentet på segmentlinjene.</span><span class="sxs-lookup"><span data-stu-id="4eede-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="4eede-111">Du kan velge kontakter.</span><span class="sxs-lookup"><span data-stu-id="4eede-111">You can select contacts.</span></span>
* <span data-ttu-id="4eede-112">Du kan bruke et loggført segment på nytt som grunnlag når du oppretter et nytt segment.</span><span class="sxs-lookup"><span data-stu-id="4eede-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="4eede-113">Du kan bruke lagrede segmenteringskriterier på nytt.</span><span class="sxs-lookup"><span data-stu-id="4eede-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="4eede-114">Samhandlinger</span><span class="sxs-lookup"><span data-stu-id="4eede-114">Interactions</span></span>
<span data-ttu-id="4eede-115">På **Segment**-siden kan du opprette samhandlinger for flere kontakter samtidig.</span><span class="sxs-lookup"><span data-stu-id="4eede-115">On the **Segment** page, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="4eede-116">Du kan for eksempel flette et segment med et Microsoft Word-dokument, slik at du kan sende et brev til alle kontaktene i segmentet.</span><span class="sxs-lookup"><span data-stu-id="4eede-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="4eede-117">Du kan angi opplysninger om samhandlingen for segmentet i **Segment**-hodet.</span><span class="sxs-lookup"><span data-stu-id="4eede-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="4eede-118">Du kan for eksempel angi hvilken samhandlingsmal du vil bruke for alle kontaktene, angi en beskrivelse, en korrespondansetype og så videre.</span><span class="sxs-lookup"><span data-stu-id="4eede-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="4eede-119">Du kan imidlertid endre disse opplysningene på segmentlinjen for hver enkelt kontakt, for eksempel ved å angi en annen beskrivelse for en kontakt.</span><span class="sxs-lookup"><span data-stu-id="4eede-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="4eede-120">Hvis du fletter et segment med et Microsoft Word-dokument, kan du tilpasse dokumentet som skal sendes for en eller flere kontakter i segmentet, for eksempel ved å legge til personlige merknader i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="4eede-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="4eede-121">Loggføring</span><span class="sxs-lookup"><span data-stu-id="4eede-121">Logging</span></span>
<span data-ttu-id="4eede-122">Når du velger **Logg** på **Segment**-siden, registrerer programmet samhandlingene på siden **Samhandlingspost** og loggfører segmentet.</span><span class="sxs-lookup"><span data-stu-id="4eede-122">On the **Segment** page, when you choose **Log**, the application records the interactions on the **Interaction Log Entry** page, and logs the segment.</span></span> <span data-ttu-id="4eede-123">Etter at du har loggført segmentet, finner du segmentet bare på siden **Loggførte segmenter**.</span><span class="sxs-lookup"><span data-stu-id="4eede-123">After you have logged the segment, you can only find it on the **Logged Segments** page.</span></span>

<span data-ttu-id="4eede-124">På siden **Loggførte segmenter** kan du avgjøre om du vil opprette et oppfølgingssegment som inneholder nøyaktig den samme kontakten som segmentet du har loggført.</span><span class="sxs-lookup"><span data-stu-id="4eede-124">On the **Logged Segments** page, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eede-125">Se også</span><span class="sxs-lookup"><span data-stu-id="4eede-125">See Also</span></span>
[<span data-ttu-id="4eede-126">Opprette segmenter.</span><span class="sxs-lookup"><span data-stu-id="4eede-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="4eede-127">Opprette samhandlinger for segmenter</span><span class="sxs-lookup"><span data-stu-id="4eede-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="4eede-128">Håndtere segmenter</span><span class="sxs-lookup"><span data-stu-id="4eede-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="4eede-129">Registrere samhandlinger med kontakter</span><span class="sxs-lookup"><span data-stu-id="4eede-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="4eede-130">Håndtere salgsmuligheter</span><span class="sxs-lookup"><span data-stu-id="4eede-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="4eede-131">Opprette og administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="4eede-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="4eede-132">Arbeide med Business Central</span><span class="sxs-lookup"><span data-stu-id="4eede-132">Working with Business Central</span></span>](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]