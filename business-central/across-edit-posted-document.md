---
title: Redigere bokførte salgs- og kjøpsdokumenter | Microsoft Docs
description: Lær om de forskjellige bokføringsfunksjonene for å bokføre kjøpsdokumenter og hvordan du kan oppdatere bokførte dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ef23d98aaeeb63c17e836fd25b547703787264da
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776200"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="c136f-103">Redigere bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="c136f-103">Edit Posted Documents</span></span>

<span data-ttu-id="c136f-104">Noen ganger må du oppdatere et bokført dokument fordi informasjon som er relevant for dokumentet, er endret.</span><span class="sxs-lookup"><span data-stu-id="c136f-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="c136f-105">I et bokført salgsdokument kan dette for eksempel være transportørens pakkesporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="c136f-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="c136f-106">På et bokført kjøpsdokument kan dette være en betalingsreferansetekst.</span><span class="sxs-lookup"><span data-stu-id="c136f-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="c136f-107">Du utfører endringen i en redigerbar versjon av det opprinnelige dokumentet, angitt med "**- Oppdater**" i sidetittelen.</span><span class="sxs-lookup"><span data-stu-id="c136f-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="c136f-108">Siden inneholder et delsett av feltene i det opprinnelige dokumentet, og noen av feltene kan ikke redigeres og er synlige av informasjonsårsaker.</span><span class="sxs-lookup"><span data-stu-id="c136f-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="c136f-109">Funksjonaliteten er tilgjengelig for følgende dokumenter i alle støttede markeder:</span><span class="sxs-lookup"><span data-stu-id="c136f-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="c136f-110">Bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="c136f-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="c136f-111">Bokført kjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="c136f-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="c136f-112">Bokført returforsendelse</span><span class="sxs-lookup"><span data-stu-id="c136f-112">Posted Return Shipment</span></span>
- <span data-ttu-id="c136f-113">Bokført returseddel</span><span class="sxs-lookup"><span data-stu-id="c136f-113">Posted Return Receipt</span></span>

<span data-ttu-id="c136f-114">Følgende tilleggsdokumenter kan redigeres i de utvalgte landene eller områdene:</span><span class="sxs-lookup"><span data-stu-id="c136f-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="c136f-115">ES: Bokført salgsfaktura, bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="c136f-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="c136f-116">APAC: bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="c136f-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="c136f-117">RU: Bokført salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="c136f-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="c136f-118">IT: bokført overføringsseddel, bokført servicefølgeseddel</span><span class="sxs-lookup"><span data-stu-id="c136f-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="c136f-119">Slik redigerer du en bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="c136f-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="c136f-120">Nedenfor finner du informasjon om hvordan du redigerer en bokført følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="c136f-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="c136f-121">Trinnene er de samme for de andre dokumentene som støttes.</span><span class="sxs-lookup"><span data-stu-id="c136f-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="c136f-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c136f-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="c136f-123">Velg dokumentet du vil redigere, og velg deretter **Oppdater dokument**.</span><span class="sxs-lookup"><span data-stu-id="c136f-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="c136f-124">Du kan eventuelt åpne dokumentet og velge handlingen.</span><span class="sxs-lookup"><span data-stu-id="c136f-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="c136f-125">På siden **Bokført følgeseddel – oppdater** redigerer du **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="c136f-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="c136f-126">-feltet, for eksempel.</span><span class="sxs-lookup"><span data-stu-id="c136f-126">field, for example.</span></span>
4. <span data-ttu-id="c136f-127">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="c136f-127">Choose the **OK** button.</span></span>

<span data-ttu-id="c136f-128">Den bokførte følgeseddelen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="c136f-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="c136f-129">Se også</span><span class="sxs-lookup"><span data-stu-id="c136f-129">See Also</span></span>

[<span data-ttu-id="c136f-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="c136f-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="c136f-131">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="c136f-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c136f-132">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="c136f-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="c136f-133">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c136f-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]