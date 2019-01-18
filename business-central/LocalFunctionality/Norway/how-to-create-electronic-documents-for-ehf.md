---
title: Opprette elektroniske dokumenter for EHF
description: "Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a12b81a85e36e516dd458ff541e06b7523ea1981
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="create-electronic-documents-for-ehf"></a><span data-ttu-id="44d32-103">Opprette elektroniske dokumenter for EHF</span><span class="sxs-lookup"><span data-stu-id="44d32-103">Create Electronic Documents for EHF</span></span>
<span data-ttu-id="44d32-104">Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk.</span><span class="sxs-lookup"><span data-stu-id="44d32-104">When you sell goods or services to a customer in the public sector, you must submit documents electronically.</span></span>  <span data-ttu-id="44d32-105">I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du opprette elektroniske dokumenter for fakturaer, kreditnotaer, purringer og rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="44d32-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create electronic documents for invoices, credit memos, reminders, and finance charge memos.</span></span> <span data-ttu-id="44d32-106">Før du kan opprette elektroniske dokumenter, må du angi filplasseringen og opplysninger om kundene.</span><span class="sxs-lookup"><span data-stu-id="44d32-106">Before you can create the electronic documents, you must have set up file locations and information about the customers.</span></span> <span data-ttu-id="44d32-107">Hvis du vil ha mer informasjon, kan du se [Sette opp EHF](how-to-set-up-ehf.md) og [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md).</span><span class="sxs-lookup"><span data-stu-id="44d32-107">For more information, see [Set Up EHF](how-to-set-up-ehf.md) and [Set Up Customers for EHF](how-to-set-up-customers-for-ehf.md).</span></span>

<span data-ttu-id="44d32-108">Du kan bare opprette elektroniske dokumenter etter at et dokument er bokført eller utstedt.</span><span class="sxs-lookup"><span data-stu-id="44d32-108">Electronic documents can only be created after a document has been posted or issued.</span></span> <span data-ttu-id="44d32-109">Følgende fremgangsmåte viser hvordan du bokfører en salgsfaktura med nødvendig informasjon og deretter oppretter en elektronisk salgsfaktura, men de samme trinnene gjelder også for salgskreditnotaer, purringer, rentenotaer, servicefakturaer og servicekreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="44d32-109">The following procedures describe how to post a sales invoice with the required information and then create an electronic sales invoice, but the same steps also apply to sales credit memos, reminders, finance charge memos, service invoices, and service credit memos.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="44d32-110">Summen av linjene i et eksportert elektronisk dokument gjenspeiler ikke fakturaavrunding, selv om det er aktivert.</span><span class="sxs-lookup"><span data-stu-id="44d32-110">The sum of lines in an exported electronic document will not reflect invoice rounding, even if it is enabled.</span></span> <span data-ttu-id="44d32-111">I stedet summerer [!INCLUDE[d365fin](../../includes/d365fin_md.md)] linjene uten avrunding.</span><span class="sxs-lookup"><span data-stu-id="44d32-111">Instead, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] sums the lines without rounding.</span></span>  

## <a name="to-post-a-sales-invoice"></a><span data-ttu-id="44d32-112">Slik bokfører du en salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="44d32-112">To post a sales invoice</span></span>  

1.  <span data-ttu-id="44d32-113">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="44d32-113">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="44d32-114">Velg salgsfakturaen du vil bokføre, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="44d32-114">Select the sales invoice that you want to post, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="44d32-115">På **Generelt**-hurtigfanen kontrollerer du at disse feltene inneholder verdier:</span><span class="sxs-lookup"><span data-stu-id="44d32-115">On the **General** FastTab, make sure that the following fields contain values:</span></span>  

    - <span data-ttu-id="44d32-116">**Eksterndokumentnr.**</span><span class="sxs-lookup"><span data-stu-id="44d32-116">**External Document No.**</span></span>  
    - <span data-ttu-id="44d32-117">**Deres referanse**</span><span class="sxs-lookup"><span data-stu-id="44d32-117">**Your Reference**</span></span>  

    <span data-ttu-id="44d32-118">**Eksterndokumentnr.**-feltet viser dokumentnummeret som kunden har oppgitt.</span><span class="sxs-lookup"><span data-stu-id="44d32-118">The **External Document No.** field contains the document number that the customer provided.</span></span>  

4.  <span data-ttu-id="44d32-119">På **Fakturering**-hurtigfanen kontrollerer du at disse feltene inneholder verdier:</span><span class="sxs-lookup"><span data-stu-id="44d32-119">On the **Invoicing** FastTab, make sure that the following fields have values:</span></span>  

    - <span data-ttu-id="44d32-120">**GLN-nr.**</span><span class="sxs-lookup"><span data-stu-id="44d32-120">**GLN No.**</span></span>  
    - <span data-ttu-id="44d32-121">**Kontokode**</span><span class="sxs-lookup"><span data-stu-id="44d32-121">**Account Code**</span></span>  
    - <span data-ttu-id="44d32-122">**Faktura til-kundenr.**</span><span class="sxs-lookup"><span data-stu-id="44d32-122">**Bill-to Customer**</span></span>  
    - <span data-ttu-id="44d32-123">**Forsendelsesdato**</span><span class="sxs-lookup"><span data-stu-id="44d32-123">**Shipment Date**</span></span>  

    <span data-ttu-id="44d32-124">Merk av for **E-faktura**.</span><span class="sxs-lookup"><span data-stu-id="44d32-124">Select the **E-Invoice** check box.</span></span>  

    <span data-ttu-id="44d32-125">Standardverdien i feltet **Forsendelsesdato** er bokføringsdatoen for dokumentet.</span><span class="sxs-lookup"><span data-stu-id="44d32-125">The default value of the **Shipment Date** field is the posting date of the document.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="44d32-126">For purringer og rentenotaer er feltet **GLN-nr.**, **Kontokode** og **E-faktura** på **Bokføring**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="44d32-126">For reminders and finance charge memos, the **GLN No.**, **Account Code**, and **E-Invoice** fields are on the **Posting** FastTab.</span></span>  

5.  <span data-ttu-id="44d32-127">Velg handlingen **Bokfør** for å bokføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="44d32-127">Choose the **Post** action to post the invoice.</span></span>  

## <a name="to-create-an-electronic-sales-invoice"></a><span data-ttu-id="44d32-128">Slik oppretter du en elektronisk salgsfaktura:</span><span class="sxs-lookup"><span data-stu-id="44d32-128">To create an electronic sales invoice</span></span>  

1.  <span data-ttu-id="44d32-129">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="44d32-129">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Sales Invoices**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="44d32-130">Velg den aktuelle salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="44d32-130">Select the relevant sales invoice.</span></span>  
3.  <span data-ttu-id="44d32-131">Velg handlingen **Opprett elektronisk faktura**.</span><span class="sxs-lookup"><span data-stu-id="44d32-131">Choose the **Create Electronic Invoice** action.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="44d32-132">Du må merke av for **E-faktura** på fakturaen hvis du vil opprette en elektronisk faktura.</span><span class="sxs-lookup"><span data-stu-id="44d32-132">The **E-Invoice** check box must be selected on the invoice in order to create an electronic invoice.</span></span>  

4.  <span data-ttu-id="44d32-133">Hvis du vil, kan du angi flere filtre på kjørselssiden **Opprett elektroniske fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="44d32-133">Optionally, in the **Create Electronic Invoices** batch job page, set additional filters.</span></span>  
5.  <span data-ttu-id="44d32-134">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="44d32-134">Choose the **OK** button.</span></span>  

<span data-ttu-id="44d32-135">En XML-fil opprettes og lagres på lokasjonen som er definert på **Salgsoppsett**-siden.</span><span class="sxs-lookup"><span data-stu-id="44d32-135">An XML file is created and stored at the location that was defined on the **Sales & Receivables Setup** page.</span></span> <span data-ttu-id="44d32-136">Du kan nå sende dokumentet til kunden.</span><span class="sxs-lookup"><span data-stu-id="44d32-136">You can now submit the document to the customer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44d32-137">Se også</span><span class="sxs-lookup"><span data-stu-id="44d32-137">See Also</span></span>  
 [<span data-ttu-id="44d32-138">EHF – Elektronisk fakturering i Norge</span><span class="sxs-lookup"><span data-stu-id="44d32-138">EHF Electronic Invoicing in Norway</span></span>](ehf-electronic-invoicing-in-norway.md)

