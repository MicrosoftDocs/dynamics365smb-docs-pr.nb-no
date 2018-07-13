---
title: "Konfigurere inngående dokumenter| Microsoft-dokumentasjon"
description: "Bruke funksjonen Inngående dokumenter til å opprette elektroniske dokumenter, behandle OCR-oppgaver, importere fakturaer og konvertere bildefiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: ea5673f341954960852de33cb94ee5722c8dbe26
ms.contentlocale: nb-no
ms.lasthandoff: 06/11/2018

---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="0a207-103">Konfigurere inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="0a207-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="0a207-104">Hvis du oppretter finanskladdelinjer fra innkommende dokumentposter, må du angi hvilken kladdemal og kladd som skal brukes i vinduet **Oppsett for inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="0a207-104">If you create general journal lines from incoming document records, you must specify in the **Incoming Documents Setup** window which journal template and batch to use.</span></span>

<span data-ttu-id="0a207-105">Hvis du ikke vil at brukerne skal opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre dokumentene først er godkjent, må du definere godkjennere i vinduet **Godkjennere for inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="0a207-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers in the **Incoming Document Approvers** window.</span></span>

<span data-ttu-id="0a207-106">Hvis du vil gjøre om PDF- og bildefiler til elektroniske dokumenter som du kan konvertere til, for eksempel kjøpsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du først sette opp OCR-funksjonen og aktivere tjenesten.</span><span class="sxs-lookup"><span data-stu-id="0a207-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="0a207-107">Når funksjonen for inngående dokumenter er konfigurert, kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="0a207-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="0a207-108">De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="0a207-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="0a207-109">Hvis du vil ha mer informasjon, kan du se [Behandle inngående dokumenter](across-process-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="0a207-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="0a207-110">Slik konfigurerer du funksjonen for inngående dokumenter:</span><span class="sxs-lookup"><span data-stu-id="0a207-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="0a207-111">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0a207-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a207-112">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0a207-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="0a207-113">Slik definerer du godkjennere av inngående dokumentposter:</span><span class="sxs-lookup"><span data-stu-id="0a207-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="0a207-114">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett for inngående dokumenter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0a207-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a207-115">I vinduet **Oppsett for inngående dokumenter** velger du handlingen **Godkjennere**.</span><span class="sxs-lookup"><span data-stu-id="0a207-115">In the **Incoming Documents Setup** window, choose the **Approvers** action.</span></span>

    <span data-ttu-id="0a207-116">Vinduet **Godkjennere for inngående dokumenter** viser alle brukerne som er definert i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0a207-116">The **Incoming Document Approvers** window shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="0a207-117">Velg én eller flere brukere som kan godkjenne et innkommende dokument før det kan opprettes en relatert dokument- eller kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="0a207-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="0a207-118">Når godkjennere er definert i vinduet **Godkjennere for inngående dokumenter**, er det bare disse brukerne som kan godkjenne et inngående dokument hvis det er merket av for **Krev godkjenning for opprettelse** i vinduet **Oppsett for inngående dokumenter**.</span><span class="sxs-lookup"><span data-stu-id="0a207-118">When approvers have been set up in the **Incoming Document Approvers** window, only those users can approve an incoming document if the **Require Approval To Create** check box in the **Incoming Documents Setup** window is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0a207-119">Dette godkjenningsoppsettet er ikke relatert til arbeidsflyter for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="0a207-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="0a207-120">Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="0a207-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="0a207-121">Slik definerer du en OCR-tjeneste:</span><span class="sxs-lookup"><span data-stu-id="0a207-121">To set up an OCR service</span></span>
1. <span data-ttu-id="0a207-122">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett for OCR-tjeneste**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0a207-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="0a207-123">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="0a207-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="0a207-124">Påloggingsdataene krypteres automatisk.</span><span class="sxs-lookup"><span data-stu-id="0a207-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a207-125">Se også</span><span class="sxs-lookup"><span data-stu-id="0a207-125">See Also</span></span>
[<span data-ttu-id="0a207-126">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="0a207-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="0a207-127">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="0a207-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0a207-128">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="0a207-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0a207-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a207-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

