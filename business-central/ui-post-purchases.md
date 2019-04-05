---
title: Forstå hvordan du bokfører kjøpsdokumenter | Microsoft-dokumentasjon
description: Les om de ulike bokføringsfunksjonene for å bokføre kjøpsdokumenter.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 5f3c709e6e2588fe7cf409e44291d331acc09432
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802544"
---
# <a name="posting-purchases"></a><span data-ttu-id="4c214-103">Bokføre kjøp</span><span class="sxs-lookup"><span data-stu-id="4c214-103">Posting Purchases</span></span>
<span data-ttu-id="4c214-104">I **Bokføringsgruppe** i et kjøpsdokument, kan du velge mellom følgende bokføringsfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="4c214-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="4c214-105">**Bokfør**</span><span class="sxs-lookup"><span data-stu-id="4c214-105">**Post**</span></span>
* <span data-ttu-id="4c214-106">**Forhåndsvis bokføring**</span><span class="sxs-lookup"><span data-stu-id="4c214-106">**Preview Posting**</span></span>
* <span data-ttu-id="4c214-107">**Bokfør og skriv ut**</span><span class="sxs-lookup"><span data-stu-id="4c214-107">**Post and Print**</span></span>
* <span data-ttu-id="4c214-108">**Kontrollrapport**</span><span class="sxs-lookup"><span data-stu-id="4c214-108">**Test Report**</span></span>
* <span data-ttu-id="4c214-109">**Massebokfør**</span><span class="sxs-lookup"><span data-stu-id="4c214-109">**Post Batch**</span></span>

<span data-ttu-id="4c214-110">Når du har fylt ut alle linjene og angitt alle opplysningene i bestillingen, kan du bokføre den. Det vil si at du oppretter et mottak og en faktura.</span><span class="sxs-lookup"><span data-stu-id="4c214-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="4c214-111">Når en bestilling bokføres, oppdateres leverandørens konto, finans og varepostene.</span><span class="sxs-lookup"><span data-stu-id="4c214-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="4c214-112">For hver bestilling opprettes det en kjøpspost i **Finanspost**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4c214-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="4c214-113">Det opprettes også en post på leverandørens konto i **Leverandørpost**-tabellen, og en finanspost opprettes i den relevante samlekontoen.</span><span class="sxs-lookup"><span data-stu-id="4c214-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="4c214-114">I tillegg kan bokføring av bestillingen resultere i en mva-post og en finanspost for rabattbeløpet.</span><span class="sxs-lookup"><span data-stu-id="4c214-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="4c214-115">Om en rabattpost skal bokføres, avhenger av innholdet i feltet  **Rabattbokføring** på siden **Kjøpsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="4c214-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Purchases & Payables Setup** page.</span></span>

<span data-ttu-id="4c214-116">For hver bestillingslinje opprettes det en varepost i tabellen **Varepost** (hvis bestillingslinjen inneholder varenumre), eller en finanspost i tabellen **Finanspost** (hvis bestillingslinjen inneholder en finanskonto).</span><span class="sxs-lookup"><span data-stu-id="4c214-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="4c214-117">I tillegg registreres alltid bestillinger i tabellene **Mottakshode** og **Kjøpsfakturahode**.</span><span class="sxs-lookup"><span data-stu-id="4c214-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="4c214-118">Før du starter bokføringen, kan du skrive ut en kontrollrapport som viser alle opplysningene i bestillingen, samt eventuelle feil.</span><span class="sxs-lookup"><span data-stu-id="4c214-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="4c214-119">Hvis du vil skrive ut rapporten, velger du **Bokføring** og deretter **Kontrollrapport**.</span><span class="sxs-lookup"><span data-stu-id="4c214-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="4c214-120">Når du bokfører en bestilling, kan du opprette både et mottak og en faktura.</span><span class="sxs-lookup"><span data-stu-id="4c214-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="4c214-121">Dette kan gjøres samtidig, eller hver for seg.</span><span class="sxs-lookup"><span data-stu-id="4c214-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="4c214-122">Du kan også opprette et delvis mottak og en delfaktura ved å fylle ut feltene **Motta (antall)** og **Fakturer (antall)** på de enkelte bestillingsordrelinjene før du bokfører.</span><span class="sxs-lookup"><span data-stu-id="4c214-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="4c214-123">Legg merke til at du ikke kan opprette en faktura for noe som ikke er mottatt.</span><span class="sxs-lookup"><span data-stu-id="4c214-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="4c214-124">Det vil si at for å kunne fakturere, må du på forhånd ha registrert et mottak, eller du må velge å motta og fakturere samtidig.</span><span class="sxs-lookup"><span data-stu-id="4c214-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="4c214-125">Du kan enten bokføre eller bokføre og skrive ut.</span><span class="sxs-lookup"><span data-stu-id="4c214-125">You can either post, or post and print.</span></span> <span data-ttu-id="4c214-126">Hvis du velger å bokføre og skrive ut, skrives det ut en rapport når ordren bokføres.</span><span class="sxs-lookup"><span data-stu-id="4c214-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="4c214-127">Du kan også velge funksjonen **Massebokfør** for å bokføre flere bestillinger samtidig.</span><span class="sxs-lookup"><span data-stu-id="4c214-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="4c214-128">Når bokføringen er utført, fjernes de bokførte kjøpslinjene fra bestillingen.</span><span class="sxs-lookup"><span data-stu-id="4c214-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="4c214-129">En melding viser når bokføringen er gjennomført.</span><span class="sxs-lookup"><span data-stu-id="4c214-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="4c214-130">Etter dette vil du kunne se de bokførte postene på de forskjellige sidene som inneholder bokførte poster, for eksempel sidene **Kundeposter**, **Finansposter**, **Vareposter**, **Kjøpsmottak** og **Bokførte kjøpsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="4c214-130">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c214-131">Se også</span><span class="sxs-lookup"><span data-stu-id="4c214-131">See Also</span></span>
[<span data-ttu-id="4c214-132">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="4c214-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="4c214-133">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="4c214-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="4c214-134">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4c214-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

