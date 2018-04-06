---
title: Opprette poster for innkommende dokumenter | Microsoft-dokumentasjon
description: "Du kan opprette poster for inngående dokumenter, for eksempel e-fakturaer, og behandle OCR-oppgaver, e-handel og dokumentutveksling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 444dabfdcfbf91eb81e281f6f6b4b9f3b184462d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="create-incoming-document-records"></a><span data-ttu-id="cfa69-103">Opprette innkommende dokumentposter</span><span class="sxs-lookup"><span data-stu-id="cfa69-103">Create Incoming Document Records</span></span>
<span data-ttu-id="cfa69-104">I vinduet **Inngående dokumenter** kan du bruke forskjellige funksjoner til å se gjennom utgiftskvitteringer, behandle OCR-oppgaver og konvertere inngående dokumentfiler, manuelt eller automatisk, til de aktuelle dokumentene eller kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="cfa69-104">In the **Incoming Documents** window, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="cfa69-105">De eksterne filene kan tilknyttes på et hvilket som helst tidspunkt i prosessen, inkludert bokførte dokumenter og resulterende leverandør, kunde- og finansposter.</span><span class="sxs-lookup"><span data-stu-id="cfa69-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="cfa69-106">For å registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] må du først opprette eller fullføre en innkommende dokumentpost.</span><span class="sxs-lookup"><span data-stu-id="cfa69-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="cfa69-107">Du kan gjøre dette manuelt, eller du kan ta et bilde av det eksterne dokumentet og deretter opprette den inngående dokumentposten med bildefilen som vedlegg.</span><span class="sxs-lookup"><span data-stu-id="cfa69-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="cfa69-108">Før du kan bruke funksjonen for inngående dokumenter, må du utføre den nødvendige konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="cfa69-109">Hvis du vil ha mer informasjon, kan du se [Konfigurere inngående dokumenter](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="cfa69-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="cfa69-110">Slik godkjenner eller avviser du et innkommende dokument</span><span class="sxs-lookup"><span data-stu-id="cfa69-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="cfa69-111">Hvis du vil tillate brukere å opprette fakturaer eller finanskladdelinjer fra innkommende dokumentposter med mindre de er godkjent, kan du definere godkjennere som må godkjenne postene før de kan behandles.</span><span class="sxs-lookup"><span data-stu-id="cfa69-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="cfa69-112">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="cfa69-113">Velg linjen med dokumentet som du vil godkjenne eller avvise, og velg deretter handlingen **Godkjenn** eller **Avvis**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="cfa69-114">Hvis du godkjenner den inngående dokumentposten, merkes det av for **Frigitt** på linjen for det inngående dokumentet.</span><span class="sxs-lookup"><span data-stu-id="cfa69-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="cfa69-115">Brukeren som for eksempel er ansvarlig for å opprette kjøpsfakturaer, kan fortsette å behandle posten.</span><span class="sxs-lookup"><span data-stu-id="cfa69-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="cfa69-116">Slik oppretter du en innkommende dokumentpost ved å ta et bilde</span><span class="sxs-lookup"><span data-stu-id="cfa69-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="cfa69-117">Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienter.</span><span class="sxs-lookup"><span data-stu-id="cfa69-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="cfa69-118">I appfeltet velger du **Opprett innkommende dokument fra kamera**-flisen, og gå deretter til trinn 4.</span><span class="sxs-lookup"><span data-stu-id="cfa69-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="cfa69-119">Alternativt kan du velge Alternativer-knappen i appfeltet, velge **Innkommende dokumenter**, og deretter velge **Alle**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="cfa69-120">I vinduet **Inngående dokumenter** velger du ellipseknappen, og deretter velger du **Opprett fra kamera**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-120">In the **Incoming Documents** window, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="cfa69-121">Kameraet på tavle-PC-en eller telefon er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cfa69-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="cfa69-122">Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="cfa69-123">En ny innkommende dokumentpost opprettes med bildet vedlagt.</span><span class="sxs-lookup"><span data-stu-id="cfa69-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="cfa69-124">Slik legger du ved et bilde i en innkommende dokumentpost ved å ta et bilde</span><span class="sxs-lookup"><span data-stu-id="cfa69-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="cfa69-125">Fremgangsmåten nedenfor gjelder bare for nettbrett og telefoner med [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienter.</span><span class="sxs-lookup"><span data-stu-id="cfa69-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="cfa69-126">Velg Alternativer-knappen i appfeltet, velg **Innkommende dokumenter**, og velg deretter **Alle**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="cfa69-127">Åpne kortet for en eksisterende innkommende dokumentpost.</span><span class="sxs-lookup"><span data-stu-id="cfa69-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="cfa69-128">I vinduet **Inngående dokument** velger du ellipseknappen, og deretter velger du **Legg ved bilde fra kamera**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-128">In the **Incoming Document** window, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="cfa69-129">Kameraet på tavle-PC-en eller telefon er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cfa69-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="cfa69-130">Ta et bilde av et dokument, for eksempel et kjøpsmottak, som du vil behandle som et innkommende dokument, og velg deretter **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="cfa69-131">Bildet legges ved den innkommende dokumentposten.</span><span class="sxs-lookup"><span data-stu-id="cfa69-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="cfa69-132">Slik oppretter du en innkommende dokumentpost manuelt:</span><span class="sxs-lookup"><span data-stu-id="cfa69-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="cfa69-133">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Inngående dokumenter**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="cfa69-134">Velg handlingen **Opprett fra fil**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="cfa69-135">I **Sett inn fil**-vinduet velger du en fil og deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-135">In the **Insert File** window, select a file, and then choose **Open**.</span></span> <span data-ttu-id="cfa69-136">Filen legges ved automatisk.</span><span class="sxs-lookup"><span data-stu-id="cfa69-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="cfa69-137">Du kan også velge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="cfa69-138">Hvis du vil legge ved en fil, velger du handlingen **Legg ved fil**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="cfa69-139">I vinduet **Sett inn fil** velger du filen som representerer det innkommende dokumentet, og deretter velger du **Åpne**- knappen.</span><span class="sxs-lookup"><span data-stu-id="cfa69-139">In the **Insert File** window, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="cfa69-140">Fyll ut feltene etter behov i vinduet **Inngående dokument**.</span><span class="sxs-lookup"><span data-stu-id="cfa69-140">In the **Incoming Document** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="cfa69-141">Se også</span><span class="sxs-lookup"><span data-stu-id="cfa69-141">See Also</span></span>
[<span data-ttu-id="cfa69-142">Behandle inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="cfa69-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="cfa69-143">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="cfa69-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="cfa69-144">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="cfa69-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="cfa69-145">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cfa69-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

