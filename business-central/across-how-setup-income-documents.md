---
title: Konfigurere inngående dokumenter| Microsoft-dokumentasjon
description: Bruke funksjonen Inngående dokumenter til å opprette elektroniske dokumenter, behandle OCR-oppgaver, importere fakturaer og konvertere bildefiler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 00bfa89376a361bedc71ba76630906d761989ead
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384602"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="a5435-103">Konfigurere inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="a5435-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="a5435-104">Hvis du oppretter finanskladdelinjer fra innkommende dokumentposter, må du angi hvilken kladdemal og kladd som skal brukes på siden **Oppsett for inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="a5435-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="a5435-105">Hvis du ikke vil at brukerne skal opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre dokumentene først er godkjent, må du definere arbeidsflytgodkjennere.</span><span class="sxs-lookup"><span data-stu-id="a5435-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="a5435-106">Hvis du vil gjøre om PDF- og bildefiler til elektroniske dokumenter som du kan konvertere til, for eksempel kjøpsfakturaer i [!INCLUDE[prod_short](includes/prod_short.md)], må du først sette opp OCR-funksjonen og aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a5435-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[prod_short](includes/prod_short.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="a5435-107">Velg en tjenestepakke som passer for organisasjonen og/eller landet/området.</span><span class="sxs-lookup"><span data-stu-id="a5435-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="a5435-108">Du kan også opprette poster manuelt for å representere de eksterne dokumentene.</span><span class="sxs-lookup"><span data-stu-id="a5435-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="a5435-109">Når funksjonen for inngående dokumenter er konfigurert, kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="a5435-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="a5435-110">De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="a5435-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="a5435-111">Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="a5435-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="a5435-112">Slik konfigurerer du funksjonen for inngående dokumenter:</span><span class="sxs-lookup"><span data-stu-id="a5435-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="a5435-113">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a5435-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a5435-114">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a5435-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="a5435-115">Som en del av oppsettet må du bestemme om du vil kreve godkjenning av innkommende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="a5435-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="a5435-116">Hvis du vil kreve godkjenning, må du definere godkjennere og arbeidsflyter for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a5435-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="a5435-117">Hvis organisasjonen ikke vil kreve godkjenning, kan du hoppe over neste del.</span><span class="sxs-lookup"><span data-stu-id="a5435-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="a5435-118">Hvis du bruker en tjeneste til å konvertere PDF-eller bildefiler som representerer inn kommende dokumenter, må du konfigurere det.</span><span class="sxs-lookup"><span data-stu-id="a5435-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="a5435-119">Hvis ikke kan du også hoppe over den delen.</span><span class="sxs-lookup"><span data-stu-id="a5435-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="a5435-120">Slik definerer du godkjennere av inngående dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="a5435-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="a5435-121">Du kan eventuelt definere en godkjenningsprosess for innkommende dokumenter.</span><span class="sxs-lookup"><span data-stu-id="a5435-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="a5435-122">Godkjennere av innkommende dokumenter må konfigureres som brukere av arbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a5435-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="a5435-123">Før du kan opprette arbeidsflyter som omfatter godkjenningstrinn, må du definere arbeidsflytbrukerne som er involvert i godkjenningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="a5435-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="a5435-124">På siden **Brukeroppsett for godkjenning** angir du også beløpsgrenser for bestemte typer forespørsler og definerer stedfortredende godkjennere som godkjenningsforespørsler delegeres til når den opprinnelige godkjenneren er borte.</span><span class="sxs-lookup"><span data-stu-id="a5435-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="a5435-125">Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="a5435-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="a5435-126">Slik definerer du en OCR-tjeneste:</span><span class="sxs-lookup"><span data-stu-id="a5435-126">To set up an OCR service</span></span>

1. <span data-ttu-id="a5435-127">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for OCR-tjeneste**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a5435-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="a5435-128">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="a5435-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="a5435-129">Påloggingsdataene krypteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="a5435-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="a5435-130">Hvis du vil ha mer informasjon, kan du se [Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).</span><span class="sxs-lookup"><span data-stu-id="a5435-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5435-131">Se også</span><span class="sxs-lookup"><span data-stu-id="a5435-131">See Also</span></span>

[<span data-ttu-id="a5435-132">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="a5435-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="a5435-133">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="a5435-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="a5435-134">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="a5435-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a5435-135">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5435-135">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]