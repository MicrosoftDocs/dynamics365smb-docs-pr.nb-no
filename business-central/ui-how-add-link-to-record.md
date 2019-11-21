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
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649791"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="017b7-103">Behandle vedlegg, koblinger og merknader på kort og dokumenter</span><span class="sxs-lookup"><span data-stu-id="017b7-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="017b7-104">I faktaboksen på de fleste kort og dokumenter kan du legge ved filer, legge til koblinger og skrive merknader.</span><span class="sxs-lookup"><span data-stu-id="017b7-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="017b7-105">For koblinger og merknader kan du også gjøre dette på listesiden ved først å merke den tilknyttede linjen.</span><span class="sxs-lookup"><span data-stu-id="017b7-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="017b7-106">Hvis du vil vise eller endre noen av disse vedlagte informasjonstypene, må du først åpne **Vedlegg**-kategorien i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="017b7-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="017b7-107">Nummeret bak kategoritittelen angir hvor mange vedlagte filer, koblinger eller merknader som finnes for kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="017b7-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="017b7-108">Vedlegg, koblinger og merknader forblir tilknyttet når kortet eller dokumentet behandles i andre statuser, for eksempel fra en pågående ordre til en bokført salgsfaktura.</span><span class="sxs-lookup"><span data-stu-id="017b7-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="017b7-109">Vær imidlertid oppmerksom på at ingen av vedleggstypene blir skrevet ut fra systemet, for eksempel ved utskrift eller lagring til en fil.</span><span class="sxs-lookup"><span data-stu-id="017b7-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="017b7-110">Knytte en fil til en kjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="017b7-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="017b7-111">Du kan legge ved alle typer filer, som inneholder tekst, bilder eller video, i et kort eller dokument.</span><span class="sxs-lookup"><span data-stu-id="017b7-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="017b7-112">Dette er for eksempel nyttig når du vil lagre fakturaen for en leverandør som en PDF-fil på den relaterte kjøpsfakturaen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="017b7-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="017b7-113">Filer som er knyttet til funksjonen for innkommende dokumenter, tas ikke med i kategorien **Vedlegg**. Se [Innkommende dokumenter](across-income-documents.md) for mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="017b7-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="017b7-114">Følgende fremgangsmåte er basert på en ordre.</span><span class="sxs-lookup"><span data-stu-id="017b7-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="017b7-115">Trinnene er lignende for alle andre støttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="017b7-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="017b7-116">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="017b7-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="017b7-117">Åpne salgsordren som du vil legge til en fil i.</span><span class="sxs-lookup"><span data-stu-id="017b7-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="017b7-118">Åpne fanen **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="017b7-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="017b7-119">Velg verdien bak feltet **Dokumenter**, for eksempel 0.</span><span class="sxs-lookup"><span data-stu-id="017b7-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="017b7-120">På **Vedlagte dokumenter**-siden i **Vedlegg**-feltet velger du **Velg fil**-knappen.</span><span class="sxs-lookup"><span data-stu-id="017b7-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="017b7-121">Velg en fil fra en hvilken som helst plassering, og velg deretter **Åpne**-knappen.</span><span class="sxs-lookup"><span data-stu-id="017b7-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="017b7-122">Filen er nå knyttet til kjøpsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="017b7-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="017b7-123">Legge til en kobling fra varekortet</span><span class="sxs-lookup"><span data-stu-id="017b7-123">To add a link from an item card</span></span>
<span data-ttu-id="017b7-124">Du kan legge til en kobling fra et kort eller et dokument i en hvilken som helst URL-adresse eller bane.</span><span class="sxs-lookup"><span data-stu-id="017b7-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="017b7-125">Dette er nyttig når du for eksempel vil knytte et varekort til leverandørens varekatalog.</span><span class="sxs-lookup"><span data-stu-id="017b7-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="017b7-126">Følgende fremgangsmåte er basert på et varekort.</span><span class="sxs-lookup"><span data-stu-id="017b7-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="017b7-127">Trinnene er lignende for alle andre støttede kort og dokumenter.</span><span class="sxs-lookup"><span data-stu-id="017b7-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="017b7-128">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="017b7-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="017b7-129">Velg varen du vil legge til en kobling fra, og velg deretter kategorien **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="017b7-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="017b7-130">I **Koblinger** velger du **+**-ikonet.</span><span class="sxs-lookup"><span data-stu-id="017b7-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="017b7-131">I vinduet **Koblingsadresse** angir du koblingen.</span><span class="sxs-lookup"><span data-stu-id="017b7-131">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="017b7-132">Koblingen må være en gyldig URL-adresse for Internett eller intranett.</span><span class="sxs-lookup"><span data-stu-id="017b7-132">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="017b7-133">I **Beskrivelse**-feltet angir du informasjon om koblingen.</span><span class="sxs-lookup"><span data-stu-id="017b7-133">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="017b7-134">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="017b7-134">Choose the **OK** button.</span></span>

<span data-ttu-id="017b7-135">Koblingen er nå knyttet til varekortet.</span><span class="sxs-lookup"><span data-stu-id="017b7-135">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="017b7-136">Skrive en merknad på en ordre</span><span class="sxs-lookup"><span data-stu-id="017b7-136">To write a note on a sales order</span></span>
<span data-ttu-id="017b7-137">Du kan skrive et notat på et dokument eller kort, for eksempel for å formidle spesielle instruksjoner til andre brukere av dokumentet eller kortet.</span><span class="sxs-lookup"><span data-stu-id="017b7-137">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="017b7-138">Du kan inkludere filkoblinger og URL-adresser i notater.</span><span class="sxs-lookup"><span data-stu-id="017b7-138">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="017b7-139">Merknader i kategorien **Vedlegg** er ikke knyttet til interne notatfunksjoner, som hovedsakelig brukes til å kommunisere mellom arbeidsflytbrukere.</span><span class="sxs-lookup"><span data-stu-id="017b7-139">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="017b7-140">Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="017b7-140">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="017b7-141">Følgende fremgangsmåte er basert på en ordre.</span><span class="sxs-lookup"><span data-stu-id="017b7-141">The following procedure is based on a sales order.</span></span> <span data-ttu-id="017b7-142">Trinnene er lignende for alle andre støttede dokumenter og kort.</span><span class="sxs-lookup"><span data-stu-id="017b7-142">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="017b7-143">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="017b7-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="017b7-144">Velg ordren du vil skrive en merknad på, og velg deretter kategorien **Vedlegg** i faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="017b7-144">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="017b7-145">I delen **Merknader** velger du **+**-ikonet.</span><span class="sxs-lookup"><span data-stu-id="017b7-145">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="017b7-146">I **Merknad**-feltet skriver du hva som helst, for eksempel "Dette er en hasteordre".</span><span class="sxs-lookup"><span data-stu-id="017b7-146">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="017b7-147">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="017b7-147">Choose the **OK** button.</span></span>

<span data-ttu-id="017b7-148">Merknaden er nå knyttet til ordren.</span><span class="sxs-lookup"><span data-stu-id="017b7-148">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="017b7-149">Se også</span><span class="sxs-lookup"><span data-stu-id="017b7-149">See Also</span></span>  
<span data-ttu-id="017b7-150">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="017b7-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="017b7-151">Inngående dokumenter</span><span class="sxs-lookup"><span data-stu-id="017b7-151">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="017b7-152">Konfigurere arbeidsflytvarsler</span><span class="sxs-lookup"><span data-stu-id="017b7-152">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
