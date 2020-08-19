---
title: Redigere bokførte salgs- og kjøpsdokumenter | Microsoft Docs
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre kjøpsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 07/21/2020
ms.author: sgroespe
ms.openlocfilehash: 58cbec2b697a0fdabd5749000ea94145d07fc62f
ms.sourcegitcommit: bdb6d18d512aa76d8d4f477d73ccfb284b0047fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/21/2020
ms.locfileid: "3611512"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="a5a6b-103">Redigere bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="a5a6b-103">Edit Posted Documents</span></span>

<span data-ttu-id="a5a6b-104">Noen ganger må du oppdatere et bokført dokument fordi informasjon som er relevant for dokumentet, er endret.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="a5a6b-105">I et bokført salgsdokument kan dette for eksempel være transportørens pakkesporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="a5a6b-106">På et bokført kjøpsdokument kan dette være en betalingsreferansetekst.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="a5a6b-107">Du utfører endringen i en redigerbar versjon av det opprinnelige dokumentet, angitt med "**- Oppdater**" i sidetittelen.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="a5a6b-108">Siden inneholder et delsett av feltene i det opprinnelige dokumentet, og noen av feltene kan ikke redigeres og er synlige av informasjonsårsaker.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="a5a6b-109">Funksjonaliteten er tilgjengelig for følgende dokumenter i alle støttede markeder:</span><span class="sxs-lookup"><span data-stu-id="a5a6b-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="a5a6b-110">Bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="a5a6b-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="a5a6b-111">Bokført kjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="a5a6b-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="a5a6b-112">Bokført returforsendelse</span><span class="sxs-lookup"><span data-stu-id="a5a6b-112">Posted Return Shipment</span></span>
- <span data-ttu-id="a5a6b-113">Bokført returseddel</span><span class="sxs-lookup"><span data-stu-id="a5a6b-113">Posted Return Receipt</span></span>

<span data-ttu-id="a5a6b-114">Følgende tilleggsdokumenter kan redigeres i de utvalgte landene eller områdene:</span><span class="sxs-lookup"><span data-stu-id="a5a6b-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="a5a6b-115">ES: Bokført salgsfaktura, bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="a5a6b-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="a5a6b-116">APAC: bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="a5a6b-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="a5a6b-117">RU: Bokført salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="a5a6b-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="a5a6b-118">IT: bokført overføringsseddel, bokført servicefølgeseddel</span><span class="sxs-lookup"><span data-stu-id="a5a6b-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="a5a6b-119">Slik redigerer du en bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="a5a6b-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="a5a6b-120">Nedenfor finner du informasjon om hvordan du redigerer en bokført følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="a5a6b-121">Trinnene er de samme for de andre dokumentene som støttes.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="a5a6b-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="a5a6b-123">Velg dokumentet du vil redigere, og velg deretter **Oppdater dokument**.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="a5a6b-124">Du kan eventuelt åpne dokumentet og velge handlingen.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="a5a6b-125">På siden **Bokført følgeseddel – oppdater** redigerer du **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="a5a6b-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="a5a6b-126">-feltet, for eksempel.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-126">field, for example.</span></span>
4. <span data-ttu-id="a5a6b-127">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-127">Choose the **OK** button.</span></span>

<span data-ttu-id="a5a6b-128">Den bokførte følgeseddelen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="a5a6b-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5a6b-129">Se også</span><span class="sxs-lookup"><span data-stu-id="a5a6b-129">See Also</span></span>

[<span data-ttu-id="a5a6b-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="a5a6b-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="a5a6b-131">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="a5a6b-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a5a6b-132">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="a5a6b-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="a5a6b-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a5a6b-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
