---
title: EHF – Elektronisk fakturering i Norge
description: Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8c83e68c269b335122c3717b30b1a0d74c2dbad8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771000"
---
# <a name="ehf-electronic-invoicing-in-norway"></a><span data-ttu-id="32d0c-103">EHF – Elektronisk fakturering i Norge</span><span class="sxs-lookup"><span data-stu-id="32d0c-103">EHF Electronic Invoicing in Norway</span></span>
<span data-ttu-id="32d0c-104">Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language).</span><span class="sxs-lookup"><span data-stu-id="32d0c-104">Companies must send sales invoices and credit memos to the Norwegian public sector electronically in the Elektronisk Handelsformat (EHF) based on Universal Business Language (UBL).</span></span> <span data-ttu-id="32d0c-105">Hvis et selskap ikke sender dokumentene elektronisk, kan myndighetene nekte betaling.</span><span class="sxs-lookup"><span data-stu-id="32d0c-105">If a company does not send these documents electronically, the authorities can deny payment.</span></span> <span data-ttu-id="32d0c-106">Standardformatet som støttes for elektronisk utveksling mellom parter, er formatet Ehandel.no.</span><span class="sxs-lookup"><span data-stu-id="32d0c-106">The standard supported format for electronic exchange between parties is the Ehandel.no format.</span></span> <span data-ttu-id="32d0c-107">Hvis du vil ha mer informasjon om EHF elektronisk fakturering, kan du se [Anskaffelser.no](https://www.anskaffelser.no).</span><span class="sxs-lookup"><span data-stu-id="32d0c-107">For more information on EHF electronic invoicing, see [Anskaffelser.no](https://www.anskaffelser.no).</span></span>  

## <a name="implementation-in-prod_short"></a><span data-ttu-id="32d0c-108">Implementering i [!INCLUDE[prod_short](../../includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="32d0c-108">Implementation in [!INCLUDE[prod_short](../../includes/prod_short.md)]</span></span>  
<span data-ttu-id="32d0c-109">Fra januar 2019 vil kravene for å sende elektroniske fakturaer være basert på PEPPOL BIS Billing 3.0-standarden.</span><span class="sxs-lookup"><span data-stu-id="32d0c-109">From January, 2019, the requirements for sending electronic invoices are based on the PEPPOL BIS Billing 3.0 standard.</span></span> <span data-ttu-id="32d0c-110">Hvis du vil ha mer informasjon, kan du se siden [EHF Billing 3.0](https://test-vefa.difi.no/ehf/g3/billing-3.0/norway/) fra Direktoratet for forvaltning og ikt.</span><span class="sxs-lookup"><span data-stu-id="32d0c-110">For more information, see the [EHF Billing 3.0](https://test-vefa.difi.no/ehf/g3/billing-3.0/norway/) page from the Agency of Public Management and eGovernment.</span></span> <span data-ttu-id="32d0c-111">Selskaper som allerede sender elektroniske dokumenter i før-2019-format, kan fortsette å gjøre dette i 2019.</span><span class="sxs-lookup"><span data-stu-id="32d0c-111">Companies that are already sending electronic documents in the pre-2019 format can continue to do so during 2019.</span></span>

<span data-ttu-id="32d0c-112">Hvis du vil sende dokumenter elektronisk, må du tilordne EAN-lokasjonsnumre (European Article Numbering) og kontokoder til de aktuelle kundene på **Kundekort**-siden.</span><span class="sxs-lookup"><span data-stu-id="32d0c-112">To send documents electronically, you must assign European Article Numbering (EAN) location numbers and account codes to the relevant customers on the **Customer Card** page.</span></span> <span data-ttu-id="32d0c-113">Du finner mer informasjon under [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md).</span><span class="sxs-lookup"><span data-stu-id="32d0c-113">For more information, see [Set Up Customers for EHF](how-to-set-up-customers-for-ehf.md).</span></span> <span data-ttu-id="32d0c-114">Disse numrene inkluderes når du oppretter, bokfører eller utsteder dokumenter.</span><span class="sxs-lookup"><span data-stu-id="32d0c-114">These numbers are included when you create, post, or issue documents.</span></span> <span data-ttu-id="32d0c-115">Nå dokumentene bokføres eller utstedes, kan du opprette elektroniske versjoner som sendes til kunder.</span><span class="sxs-lookup"><span data-stu-id="32d0c-115">After documents are posted or issued, you can create electronic versions to send to customers.</span></span>  

[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="32d0c-116">eksporterer enkelte elektroniske dokumenter i EHF versjon 3.0, som bruker UBL versjon 2.1.</span><span class="sxs-lookup"><span data-stu-id="32d0c-116">exports certain electronic documents in EHF version 3.0, which uses UBL version 2.1.</span></span> <span data-ttu-id="32d0c-117">Du kan sende følgende typer dokumenter:</span><span class="sxs-lookup"><span data-stu-id="32d0c-117">You can submit the following types of documents:</span></span>  

- <span data-ttu-id="32d0c-118">Salgs- og servicefakturaer</span><span class="sxs-lookup"><span data-stu-id="32d0c-118">Sales and service invoices</span></span>
- <span data-ttu-id="32d0c-119">Salgs- og servicekreditnotaer</span><span class="sxs-lookup"><span data-stu-id="32d0c-119">Sales and service credit memos</span></span>

[!INCLUDE[prod_short](../../includes/prod_short.md)] <span data-ttu-id="32d0c-120">eksporterer andre elektroniske dokumenter i versjon 1.6, som bruker UBL versjon 2.0.</span><span class="sxs-lookup"><span data-stu-id="32d0c-120">exports other electronic documents in version 1.6, which uses UBL version 2.0.</span></span> <span data-ttu-id="32d0c-121">Du kan sende følgende typer dokumenter:</span><span class="sxs-lookup"><span data-stu-id="32d0c-121">You can submit the following types of documents:</span></span>  

- <span data-ttu-id="32d0c-122">Rentenota</span><span class="sxs-lookup"><span data-stu-id="32d0c-122">Finance charge memo</span></span>  
- <span data-ttu-id="32d0c-123">Purring</span><span class="sxs-lookup"><span data-stu-id="32d0c-123">Reminder</span></span>  

<span data-ttu-id="32d0c-124">Du kan angi hvor du skal lagre elektroniske dokumenter, på siden **Salgsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="32d0c-124">You can specify where to store electronic documents on the **Sales & Receivables Setup** page.</span></span> <span data-ttu-id="32d0c-125">Du kan også bruke [dokumentutvekslingsfunksjonaliteten](../../across-how-to-set-up-electronic-document-sending-and-receiving.md) til å generere og sende dem.</span><span class="sxs-lookup"><span data-stu-id="32d0c-125">You can also use the [Document Exchange functionality](../../across-how-to-set-up-electronic-document-sending-and-receiving.md) to generate and send them.</span></span>

## <a name="vat-treatment"></a><span data-ttu-id="32d0c-126">Mva-justering</span><span class="sxs-lookup"><span data-stu-id="32d0c-126">VAT Treatment</span></span>  
<span data-ttu-id="32d0c-127">Mva-prosenter og transaksjonstypen bestemmer mva-typen som eksporteres i det elektroniske dokumentet.</span><span class="sxs-lookup"><span data-stu-id="32d0c-127">VAT percentages and the type of transaction determine the VAT Type that is exported in the electronic document.</span></span>  

|<span data-ttu-id="32d0c-128">XML</span><span class="sxs-lookup"><span data-stu-id="32d0c-128">XML</span></span>|<span data-ttu-id="32d0c-129">Type</span><span class="sxs-lookup"><span data-stu-id="32d0c-129">Type</span></span>| 
|---------|----------|  
|<span data-ttu-id="32d0c-130">S</span><span class="sxs-lookup"><span data-stu-id="32d0c-130">S</span></span>|<span data-ttu-id="32d0c-131">Utgående mva, vanlige sats</span><span class="sxs-lookup"><span data-stu-id="32d0c-131">Outgoing VAT, ordinary rate</span></span>|
|<span data-ttu-id="32d0c-132">H</span><span class="sxs-lookup"><span data-stu-id="32d0c-132">H</span></span>|<span data-ttu-id="32d0c-133">Utgående mva, redusert sats – matvarer og drikkevarer</span><span class="sxs-lookup"><span data-stu-id="32d0c-133">Outgoing VAT, reduced rate – food and beverage</span></span>|
|<span data-ttu-id="32d0c-134">R</span><span class="sxs-lookup"><span data-stu-id="32d0c-134">R</span></span>|<span data-ttu-id="32d0c-135">Utgående mva, redusert sats – rå fisk</span><span class="sxs-lookup"><span data-stu-id="32d0c-135">Outgoing VAT, reduced rate – raw fish</span></span>|
|<span data-ttu-id="32d0c-136">AA</span><span class="sxs-lookup"><span data-stu-id="32d0c-136">AA</span></span>|<span data-ttu-id="32d0c-137">Utgående mva, lav sats</span><span class="sxs-lookup"><span data-stu-id="32d0c-137">Outgoing VAT, low rate</span></span>|
|<span data-ttu-id="32d0c-138">AE</span><span class="sxs-lookup"><span data-stu-id="32d0c-138">AE</span></span>|<span data-ttu-id="32d0c-139">Snudd avregning</span><span class="sxs-lookup"><span data-stu-id="32d0c-139">VAT Reverse Charge</span></span>|
|<span data-ttu-id="32d0c-140">L</span><span class="sxs-lookup"><span data-stu-id="32d0c-140">L</span></span>|<span data-ttu-id="32d0c-141">Kanariøyene, generell indirekte mva</span><span class="sxs-lookup"><span data-stu-id="32d0c-141">Canary Islands general indirect tax</span></span>|
|<span data-ttu-id="32d0c-142">M</span><span class="sxs-lookup"><span data-stu-id="32d0c-142">M</span></span>|<span data-ttu-id="32d0c-143">Mva for produksjon, tjenester og import for Ceuta og Melilla</span><span class="sxs-lookup"><span data-stu-id="32d0c-143">Tax for production, services and importation in Ceuta and Melilla</span></span>|
|<span data-ttu-id="32d0c-144">G</span><span class="sxs-lookup"><span data-stu-id="32d0c-144">G</span></span>|<span data-ttu-id="32d0c-145">Gratis eksportvare, avgift betales ikke</span><span class="sxs-lookup"><span data-stu-id="32d0c-145">Free export item, tax not charged</span></span>|
|<span data-ttu-id="32d0c-146">O</span><span class="sxs-lookup"><span data-stu-id="32d0c-146">O</span></span>|<span data-ttu-id="32d0c-147">Tjenester utenfor området for mva</span><span class="sxs-lookup"><span data-stu-id="32d0c-147">Services outside scope of tax</span></span>|
|<span data-ttu-id="32d0c-148">Ø</span><span class="sxs-lookup"><span data-stu-id="32d0c-148">E</span></span>|<span data-ttu-id="32d0c-149">Mva-fritak</span><span class="sxs-lookup"><span data-stu-id="32d0c-149">VAT Exempt</span></span>|
|<span data-ttu-id="32d0c-150">Z</span><span class="sxs-lookup"><span data-stu-id="32d0c-150">Z</span></span>|<span data-ttu-id="32d0c-151">Mva-fritak (varer og tjenester som ikke omfattes av mva-bestemmelsene)</span><span class="sxs-lookup"><span data-stu-id="32d0c-151">VAT Exempt (goods and services not included in the VAT regulations)</span></span>|
|<span data-ttu-id="32d0c-152">K</span><span class="sxs-lookup"><span data-stu-id="32d0c-152">K</span></span>|<span data-ttu-id="32d0c-153">Mva-fritak for intra-EU-levering av varer og tjenester</span><span class="sxs-lookup"><span data-stu-id="32d0c-153">VAT exempt for EEA intra-community supply of goods and services</span></span>|

## <a name="vat-scheme"></a><span data-ttu-id="32d0c-154">MVA-skjema</span><span class="sxs-lookup"><span data-stu-id="32d0c-154">VAT Scheme</span></span>
<span data-ttu-id="32d0c-155">Kontroller at du har definert den riktige verdien i feltet **Mva-skjema** på siden **Land/regioner**.</span><span class="sxs-lookup"><span data-stu-id="32d0c-155">Make sure you set up the correct value in the **VAT Scheme** field on the **Countries/Regions** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="32d0c-156">Se også</span><span class="sxs-lookup"><span data-stu-id="32d0c-156">See Also</span></span>  
[<span data-ttu-id="32d0c-157">Sette opp kunder for EHF</span><span class="sxs-lookup"><span data-stu-id="32d0c-157">Set Up Customers for EHF</span></span>](how-to-set-up-customers-for-ehf.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]