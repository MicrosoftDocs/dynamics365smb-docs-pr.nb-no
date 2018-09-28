---
title: "Forstå hvordan du bokfører salgsdokumenter | Microsoft-dokumentasjon"
description: "Les om de ulike bokføringsfunksjonene for å bokføre salgsdokumenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d44203f67496f2c9b04b710acdd3e88bf15d13cc
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="posting-sales"></a><span data-ttu-id="d4152-103">Bokføre salg</span><span class="sxs-lookup"><span data-stu-id="d4152-103">Posting Sales</span></span>
<span data-ttu-id="d4152-104">I **Bokføringsgruppe** i et salgsdokument, kan du velge mellom følgende bokføringsfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="d4152-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="d4152-105">**Bokfør**</span><span class="sxs-lookup"><span data-stu-id="d4152-105">**Post**</span></span>
* <span data-ttu-id="d4152-106">**Kontrollrapport**</span><span class="sxs-lookup"><span data-stu-id="d4152-106">**Test Report**</span></span>
* <span data-ttu-id="d4152-107">**Bokfør og Send**</span><span class="sxs-lookup"><span data-stu-id="d4152-107">**Post and Send**</span></span>
* <span data-ttu-id="d4152-108">**Bokfør og skriv ut**</span><span class="sxs-lookup"><span data-stu-id="d4152-108">**Post and Print**</span></span>
* <span data-ttu-id="d4152-109">**Bokfør og send e-post**</span><span class="sxs-lookup"><span data-stu-id="d4152-109">**Post and Email**</span></span>
* <span data-ttu-id="d4152-110">**Massebokfør**</span><span class="sxs-lookup"><span data-stu-id="d4152-110">**Post Batch**</span></span>
* <span data-ttu-id="d4152-111">**Forhåndsvis bokføring**</span><span class="sxs-lookup"><span data-stu-id="d4152-111">**Preview Posting**</span></span>

<span data-ttu-id="d4152-112">Når du har fylt ut alle linjene og angitt alle opplysningene i ordren, kan du bokføre den.</span><span class="sxs-lookup"><span data-stu-id="d4152-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="d4152-113">Dette oppretter en levering og en faktura.</span><span class="sxs-lookup"><span data-stu-id="d4152-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="d4152-114">Når en ordre bokføres, oppdateres kundens konto, finans og varepostene.</span><span class="sxs-lookup"><span data-stu-id="d4152-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="d4152-115">For hver ordre opprettes en salgspost i **Finanspost**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="d4152-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="d4152-116">Det opprettes også en post på leverandørens konto i **Kundepost**-tabellen, og en finanspost opprettes i den relevante kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="d4152-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="d4152-117">I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet.</span><span class="sxs-lookup"><span data-stu-id="d4152-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="d4152-118">Om en rabattpost skal bokføres, avhenger av innholdet i feltet **Rabattbokføring** i vinduet **Salgsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="d4152-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field in the **Sales & Receivables Setup** window.</span></span>

<span data-ttu-id="d4152-119">For hver ordrelinje opprettes det en varepost i tabellen **Varepost** (hvis salgslinjen inneholder varenumre), eller det opprettes en finanspost i tabellen **Finanspost** (hvis salgslinjen inneholder en finanskonto).</span><span class="sxs-lookup"><span data-stu-id="d4152-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="d4152-120">I tillegg til dette registreres alltid ordrer i tabellene **Følgeseddelhode** og **Salgsfakturahode**.</span><span class="sxs-lookup"><span data-stu-id="d4152-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="d4152-121">Når du bokfører en ordre, kan du opprette både en følgeseddel og en faktura.</span><span class="sxs-lookup"><span data-stu-id="d4152-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="d4152-122">Dette kan gjøres samtidig eller hver for seg.</span><span class="sxs-lookup"><span data-stu-id="d4152-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="d4152-123">Du kan også opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt ordrelinje før du bokfører.</span><span class="sxs-lookup"><span data-stu-id="d4152-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="d4152-124">Merk at du ikke kan opprette en faktura for noe som ikke er levert.</span><span class="sxs-lookup"><span data-stu-id="d4152-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="d4152-125">Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.</span><span class="sxs-lookup"><span data-stu-id="d4152-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="d4152-126">Når bokføringen er utført, fjernes de bokførte salgslinjene fra bestillingen.</span><span class="sxs-lookup"><span data-stu-id="d4152-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="d4152-127">En melding viser når bokføringen er gjennomført.</span><span class="sxs-lookup"><span data-stu-id="d4152-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="d4152-128">Etter dette vil du kunne se de bokførte postene i de forskjellige vinduene som inneholder bokførte poster, for eksempel vinduene **Kundeposter**, **Finansposter**, **Vareposter**, **Bokførte følgesedler** og **Bokført salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="d4152-128">After this, you will be able to see the posted entries in the various windows that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4152-129">Se også</span><span class="sxs-lookup"><span data-stu-id="d4152-129">See Also</span></span>
[<span data-ttu-id="d4152-130">Salg</span><span class="sxs-lookup"><span data-stu-id="d4152-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="d4152-131">Sende dokumenter i e-post</span><span class="sxs-lookup"><span data-stu-id="d4152-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="d4152-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d4152-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


