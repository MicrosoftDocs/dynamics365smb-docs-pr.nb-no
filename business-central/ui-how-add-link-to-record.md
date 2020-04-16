---
title: Legge til vedlegg, koblinger og merknader i poster | Microsoft Docs
description: Legg til en hyperkobling i et dokument eller et webområde til en bestemt post, for eksempel en kunde eller et dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c5d9dcc46e05cef21961e20008227a1a35b737af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193881"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="094e4-103">Behandle vedlegg, koblinger og merknader på kort og dokumenter</span><span class="sxs-lookup"><span data-stu-id="094e4-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="094e4-104">I faktaboksen på de fleste kort og dokumenter kan du legge ved filer, legge til koblinger og skrive merknader.</span><span class="sxs-lookup"><span data-stu-id="094e4-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="094e4-105">For koblinger og merknader kan du også gjøre dette på listesiden ved først å merke den tilknyttede linjen.</span><span class="sxs-lookup"><span data-stu-id="094e4-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="094e4-106">Hvis du vil vise eller endre noen av disse vedlagte informasjonstypene, må du først åpne **Vedlegg**-kategorien i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="094e4-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="094e4-107">Nummeret bak kategoritittelen angir hvor mange vedlagte filer, koblinger eller merknader som finnes for kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="094e4-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="094e4-108">Vedlegg, koblinger og merknader forblir tilknyttet når kortet eller dokumentet behandles i andre statuser, for eksempel fra en pågående ordre til en bokført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="094e4-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="094e4-109">Ingen av vedleggstypene blir imidlertid skrevet ut fra systemet, for eksempel ved utskrift eller lagring til en fil.</span><span class="sxs-lookup"><span data-stu-id="094e4-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="094e4-110">Når du delvis sender og fakturerer en ordre eller bestilling, blir vedlegget bare knyttet til den endelige fakturaen for den ordren.</span><span class="sxs-lookup"><span data-stu-id="094e4-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="094e4-111">På samme måte, når du fakturerer ved hjelp av Periodiseringer-funksjonen, knyttes vedlegget bare til finanspostene for bilaget, men ikke for periodiseringspostene.</span><span class="sxs-lookup"><span data-stu-id="094e4-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="094e4-112">Knytte en fil til en kjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="094e4-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="094e4-113">Du kan legge ved alle typer filer, som inneholder tekst, bilder eller video, i et kort eller dokument.</span><span class="sxs-lookup"><span data-stu-id="094e4-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="094e4-114">Dette er for eksempel nyttig når du vil lagre fakturaen for en leverandør som en PDF-fil på den relaterte kjøpsfakturaen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="094e4-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="094e4-115">Filer som er knyttet til funksjonen for innkommende dokumenter, tas ikke med i kategorien **Vedlegg**. Se [Innkommende dokumenter](across-income-documents.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="094e4-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="094e4-116">Følgende fremgangsmåte er basert på en kjøpsfaktura.</span><span class="sxs-lookup"><span data-stu-id="094e4-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="094e4-117">Trinnene er lignende for alle andre støttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="094e4-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="094e4-118">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="094e4-119">Åpne salgsordren som du vil legge til en fil i.</span><span class="sxs-lookup"><span data-stu-id="094e4-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="094e4-120">Åpne fanen **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="094e4-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="094e4-121">Velg verdien bak feltet **Dokumenter**, for eksempel 0.</span><span class="sxs-lookup"><span data-stu-id="094e4-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="094e4-122">På **Vedlagte dokumenter**-siden i **Vedlegg**-feltet velger du **Velg fil**-knappen.</span><span class="sxs-lookup"><span data-stu-id="094e4-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="094e4-123">Velg en fil fra en hvilken som helst plassering, og velg deretter **Åpne**-knappen.</span><span class="sxs-lookup"><span data-stu-id="094e4-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="094e4-124">Filen er nå knyttet til kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="094e4-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="094e4-125">Slik lagrer du et dokument som et PDF-vedlegg</span><span class="sxs-lookup"><span data-stu-id="094e4-125">To save a document as a PDF attachment</span></span>
<span data-ttu-id="094e4-126">Når du skal lagre et dokument som en fil, kan du bruke handlingen **Legg ved som PDF** til å lagre gjeldende dokumentinnhold som en PDF-fil som er knyttet til faktaboksen for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="094e4-126">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="094e4-127">Dette er for eksempel nyttig når dokumenter følger flere trinn i en prosess, for eksempel en salgsprosess eller en godkjenningsarbeidsflyt, og du vil referere til en utskrift av forrige trinn.</span><span class="sxs-lookup"><span data-stu-id="094e4-127">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="094e4-128">Følgende fremgangsmåte er basert på en ordre.</span><span class="sxs-lookup"><span data-stu-id="094e4-128">The following procedure is based on a sales order.</span></span> <span data-ttu-id="094e4-129">Trinnene er de samme for alle støttede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="094e4-129">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="094e4-130">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="094e4-131">Velg en ordre, og velg deretter handlingen **Legg ved som PDF**.</span><span class="sxs-lookup"><span data-stu-id="094e4-131">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="094e4-132">En PDF-fil med gjeldende ordreinnhold legges til i fanen **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="094e4-132">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span> 

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="094e4-133">Legge til en kobling fra varekortet</span><span class="sxs-lookup"><span data-stu-id="094e4-133">To add a link from an item card</span></span>
<span data-ttu-id="094e4-134">Du kan legge til en kobling fra et kort eller et dokument i en hvilken som helst URL-adresse eller bane.</span><span class="sxs-lookup"><span data-stu-id="094e4-134">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="094e4-135">Dette er nyttig når du for eksempel vil knytte et varekort til leverandørens varekatalog.</span><span class="sxs-lookup"><span data-stu-id="094e4-135">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="094e4-136">Følgende fremgangsmåte er basert på et varekort.</span><span class="sxs-lookup"><span data-stu-id="094e4-136">The following procedure is based on an item card.</span></span> <span data-ttu-id="094e4-137">Trinnene er lignende for alle andre støttede kort og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="094e4-137">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="094e4-138">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="094e4-139">Velg varen du vil legge til en kobling fra, og velg deretter kategorien **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="094e4-139">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="094e4-140">I **Koblinger** velger du **+**-ikonet.</span><span class="sxs-lookup"><span data-stu-id="094e4-140">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="094e4-141">I vinduet **Koblingsadresse** angir du koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-141">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="094e4-142">Koblingen må være en gyldig URL-adresse for Internett eller intranett.</span><span class="sxs-lookup"><span data-stu-id="094e4-142">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="094e4-143">I **Beskrivelse**-feltet angir du informasjon om koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-143">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="094e4-144">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="094e4-144">Choose the **OK** button.</span></span>

<span data-ttu-id="094e4-145">Koblingen er nå knyttet til varekortet.</span><span class="sxs-lookup"><span data-stu-id="094e4-145">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="094e4-146">Skrive en merknad på en ordre</span><span class="sxs-lookup"><span data-stu-id="094e4-146">To write a note on a sales order</span></span>
<span data-ttu-id="094e4-147">Du kan skrive et notat på et dokument eller kort, for eksempel for å formidle spesielle instruksjoner til andre brukere av dokumentet eller kortet.</span><span class="sxs-lookup"><span data-stu-id="094e4-147">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="094e4-148">Du kan inkludere filkoblinger og URL-adresser i notater.</span><span class="sxs-lookup"><span data-stu-id="094e4-148">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="094e4-149">Merknader i kategorien **Vedlegg** er ikke knyttet til interne notatfunksjoner, som hovedsakelig brukes til å kommunisere mellom arbeidsflytbrukere.</span><span class="sxs-lookup"><span data-stu-id="094e4-149">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="094e4-150">Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="094e4-150">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="094e4-151">Følgende fremgangsmåte er basert på en ordre.</span><span class="sxs-lookup"><span data-stu-id="094e4-151">The following procedure is based on a sales order.</span></span> <span data-ttu-id="094e4-152">Trinnene er lignende for alle andre støttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="094e4-152">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="094e4-153">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="094e4-153">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="094e4-154">Velg ordren du vil skrive en merknad på, og velg deretter kategorien **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="094e4-154">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="094e4-155">I delen **Merknader** velger du **+**-ikonet.</span><span class="sxs-lookup"><span data-stu-id="094e4-155">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="094e4-156">I **Merknad**-feltet skriver du hva som helst, for eksempel "Dette er en hasteordre".</span><span class="sxs-lookup"><span data-stu-id="094e4-156">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="094e4-157">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="094e4-157">Choose the **OK** button.</span></span>

<span data-ttu-id="094e4-158">Merknaden er nå knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="094e4-158">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="094e4-159">Se også</span><span class="sxs-lookup"><span data-stu-id="094e4-159">See Also</span></span>  
<span data-ttu-id="094e4-160">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="094e4-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="094e4-161">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="094e4-161">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="094e4-162">Konfigurere arbeidsflytvarsler</span><span class="sxs-lookup"><span data-stu-id="094e4-162">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
