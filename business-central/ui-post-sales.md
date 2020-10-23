---
title: Bokføre salgsdokumenter | Microsoft Docs
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre salgsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5ca69a35aac0ba61591dfdfd71d739726e2fb62f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910133"
---
# <a name="posting-sales"></a><span data-ttu-id="780ce-103">Bokføre salg</span><span class="sxs-lookup"><span data-stu-id="780ce-103">Posting Sales</span></span>

<span data-ttu-id="780ce-104">I menyen **Bokføring** i et salgsdokument kan du velge mellom følgende bokføringsfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="780ce-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="780ce-105">**Bokfør**</span><span class="sxs-lookup"><span data-stu-id="780ce-105">**Post**</span></span>
* <span data-ttu-id="780ce-106">**Bokfør og ny**</span><span class="sxs-lookup"><span data-stu-id="780ce-106">**Post and New**</span></span>
* <span data-ttu-id="780ce-107">**Bokfør og Send**</span><span class="sxs-lookup"><span data-stu-id="780ce-107">**Post and Send**</span></span>
* <span data-ttu-id="780ce-108">**Forhåndsvis bokføring**</span><span class="sxs-lookup"><span data-stu-id="780ce-108">**Preview Posting**</span></span>
* <span data-ttu-id="780ce-109">**Fakturakladd**</span><span class="sxs-lookup"><span data-stu-id="780ce-109">**Draft Invoice**</span></span>
* <span data-ttu-id="780ce-110">**Proformafaktura**</span><span class="sxs-lookup"><span data-stu-id="780ce-110">**Pro Forma Invoice**</span></span>
* <span data-ttu-id="780ce-111">**Kontrollrapport**</span><span class="sxs-lookup"><span data-stu-id="780ce-111">**Test Report**</span></span>

<span data-ttu-id="780ce-112">Når du har fylt ut alle linjene og angitt alle opplysningene i ordren, kan du bokføre den.</span><span class="sxs-lookup"><span data-stu-id="780ce-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="780ce-113">Dette oppretter en levering og en faktura.</span><span class="sxs-lookup"><span data-stu-id="780ce-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="780ce-114">Når en ordre bokføres, oppdateres kundens konto, finans og varepostene.</span><span class="sxs-lookup"><span data-stu-id="780ce-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="780ce-115">For hver ordre opprettes en salgspost i **Finanspost**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="780ce-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="780ce-116">Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="780ce-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="780ce-117">I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet.</span><span class="sxs-lookup"><span data-stu-id="780ce-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="780ce-118">Om en rabattpost skal bokføres, avhenger av innholdet i feltet **Rabattbokføring** på **Salgsoppsett**-siden.</span><span class="sxs-lookup"><span data-stu-id="780ce-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="780ce-119">For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto).</span><span class="sxs-lookup"><span data-stu-id="780ce-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="780ce-120">I tillegg til dette registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.</span><span class="sxs-lookup"><span data-stu-id="780ce-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="780ce-121">Når du bokfører en ordre, kan du opprette både en følgeseddel og en faktura.</span><span class="sxs-lookup"><span data-stu-id="780ce-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="780ce-122">Dette kan gjøres samtidig eller hver for seg.</span><span class="sxs-lookup"><span data-stu-id="780ce-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="780ce-123">Du kan også opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt ordrelinje før du bokfører.</span><span class="sxs-lookup"><span data-stu-id="780ce-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="780ce-124">Merk at du ikke kan opprette en faktura for noe som ikke er levert.</span><span class="sxs-lookup"><span data-stu-id="780ce-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="780ce-125">Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.</span><span class="sxs-lookup"><span data-stu-id="780ce-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="780ce-126">Du kan enten bokføre eller bokføre og sende.</span><span class="sxs-lookup"><span data-stu-id="780ce-126">You can either post, or post and send.</span></span> <span data-ttu-id="780ce-127">Hvis du velger å bokføre og sende, genereres en PDF-fil som du deretter kan sende.</span><span class="sxs-lookup"><span data-stu-id="780ce-127">If you choose to post and send, a PDF file is generated that you can then send.</span></span> <span data-ttu-id="780ce-128">Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig.</span><span class="sxs-lookup"><span data-stu-id="780ce-128">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span> <span data-ttu-id="780ce-129">Hvis du vil ha mer informasjon, se [Bokføre flere dokumenter samtidig](ui-batch-posting.md).</span><span class="sxs-lookup"><span data-stu-id="780ce-129">For more information, see [Post Multiple Documents at the Same Time](ui-batch-posting.md).</span></span>

## <a name="viewing-ledger-entries"></a><span data-ttu-id="780ce-130">Vise poster</span><span class="sxs-lookup"><span data-stu-id="780ce-130">Viewing Ledger Entries</span></span>

<span data-ttu-id="780ce-131">Når bokføringen er utført, fjernes de bokførte salgslinjene fra bestillingen.</span><span class="sxs-lookup"><span data-stu-id="780ce-131">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="780ce-132">En melding viser når bokføringen er gjennomført.</span><span class="sxs-lookup"><span data-stu-id="780ce-132">A message tells you when the posting is completed.</span></span> <span data-ttu-id="780ce-133">Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Bokførte følgesedler** og **Bokført salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="780ce-133">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="780ce-134">I de fleste tilfeller kan du åpne poster fra det berørte kortet eller dokumentet.</span><span class="sxs-lookup"><span data-stu-id="780ce-134">In most cases, you can open ledger entries from the affected card or document.</span></span> <span data-ttu-id="780ce-135">På siden **Kundekort** velger du for eksempel handlingen **Poster**.</span><span class="sxs-lookup"><span data-stu-id="780ce-135">For example, on the **Customer Card** page, choose the **Ledger Entries** action.</span></span>

## <a name="editing-ledger-entries"></a><span data-ttu-id="780ce-136">Redigere poster</span><span class="sxs-lookup"><span data-stu-id="780ce-136">Editing Ledger Entries</span></span>

<span data-ttu-id="780ce-137">Du kan redigere bestemte felt på bokførte kjøpsdokumenter, for eksempel **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="780ce-137">You can edit certain fields on posted purchase documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="780ce-138">-feltet.</span><span class="sxs-lookup"><span data-stu-id="780ce-138">field.</span></span> <span data-ttu-id="780ce-139">Hvis du vil ha mer informasjon, kan du se [Redigere bokførte dokumenter](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="780ce-139">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span> <span data-ttu-id="780ce-140">Hvis du vil ha mer kritiske felt som påvirker revisjonssporingen, må du tilbakeføre eller angre bokføringen.</span><span class="sxs-lookup"><span data-stu-id="780ce-140">For more critical fields that affect the auditing trail, you must reverse or undo posting.</span></span> <span data-ttu-id="780ce-141">Hvis du vil ha mer informasjon, kan du se [Tilbakeføre kladdebokføringer og angre mottak/leveringer](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="780ce-141">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="780ce-142">Se relatert opplæring på [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="780ce-142">See Related Training at [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="780ce-143">Se også</span><span class="sxs-lookup"><span data-stu-id="780ce-143">See Also</span></span>

[<span data-ttu-id="780ce-144">Salg</span><span class="sxs-lookup"><span data-stu-id="780ce-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="780ce-145">Bokføre flere dokumenter samtidig</span><span class="sxs-lookup"><span data-stu-id="780ce-145">Post Multiple Documents at the Same Time</span></span>](ui-batch-posting.md)  
[<span data-ttu-id="780ce-146">Redigere bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="780ce-146">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="780ce-147">Sende dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="780ce-147">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="780ce-148">Korrigere eller annullere ubetalte salgsfakturaer</span><span class="sxs-lookup"><span data-stu-id="780ce-148">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="780ce-149">Finne sider og informasjon med Fortell meg</span><span class="sxs-lookup"><span data-stu-id="780ce-149">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="780ce-150">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="780ce-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
