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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fbb4e458b0e4f9068b234748a3921dbca6b3222
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300596"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="36e65-103">Redigere bokførte dokumenter</span><span class="sxs-lookup"><span data-stu-id="36e65-103">Edit Posted Documents</span></span>
<span data-ttu-id="36e65-104">Noen ganger må du oppdatere et bokført dokument fordi informasjon som er relevant for dokumentet, er endret.</span><span class="sxs-lookup"><span data-stu-id="36e65-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="36e65-105">I et bokført salgsdokument kan dette for eksempel være transportørens pakkesporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="36e65-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="36e65-106">På et bokført kjøpsdokument kan dette være en betalingsreferansetekst.</span><span class="sxs-lookup"><span data-stu-id="36e65-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="36e65-107">Du utfører endringen i en redigerbar versjon av det opprinnelige dokumentet, angitt med "**- Oppdater**" i sidetittelen.</span><span class="sxs-lookup"><span data-stu-id="36e65-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="36e65-108">Siden inneholder et delsett av feltene i det opprinnelige dokumentet, og noen av feltene kan ikke redigeres og er synlige av informasjonsårsaker.</span><span class="sxs-lookup"><span data-stu-id="36e65-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="36e65-109">Funksjonaliteten er tilgjengelig for følgende dokumenter i alle landsversjoner:</span><span class="sxs-lookup"><span data-stu-id="36e65-109">The functionality is available for the following documents in all country versions:</span></span>
- <span data-ttu-id="36e65-110">Bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="36e65-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="36e65-111">Bokført kjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="36e65-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="36e65-112">Bokført returforsendelse</span><span class="sxs-lookup"><span data-stu-id="36e65-112">Posted Return Shipment</span></span>
- <span data-ttu-id="36e65-113">Bokført returseddel</span><span class="sxs-lookup"><span data-stu-id="36e65-113">Posted Return Receipt</span></span>

<span data-ttu-id="36e65-114">Følgende tilleggsdokumenter kan redigeres i utvalgte landsversjoner:</span><span class="sxs-lookup"><span data-stu-id="36e65-114">The following additional documents can be edited in selected country versions:</span></span>
- <span data-ttu-id="36e65-115">ES: Bokført salgsfaktura, bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="36e65-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="36e65-116">APAC: bokført salgskreditnota, bokført kjøpskreditnota</span><span class="sxs-lookup"><span data-stu-id="36e65-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="36e65-117">RU: Bokført salgskreditnota</span><span class="sxs-lookup"><span data-stu-id="36e65-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="36e65-118">IT: bokført overføringsseddel, bokført servicefølgeseddel</span><span class="sxs-lookup"><span data-stu-id="36e65-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="36e65-119">Slik redigerer du en bokført følgeseddel</span><span class="sxs-lookup"><span data-stu-id="36e65-119">To edit a posted sales shipment</span></span>
<span data-ttu-id="36e65-120">Nedenfor finner du informasjon om hvordan du redigerer en bokført følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="36e65-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="36e65-121">Trinnene er de samme for de andre dokumentene som støttes.</span><span class="sxs-lookup"><span data-stu-id="36e65-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="36e65-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte følgesedler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="36e65-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="36e65-123">Velg dokumentet du vil redigere, og velg deretter **Oppdater dokument**.</span><span class="sxs-lookup"><span data-stu-id="36e65-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="36e65-124">Du kan eventuelt åpne dokumentet og velge handlingen.</span><span class="sxs-lookup"><span data-stu-id="36e65-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="36e65-125">På siden **Bokført følgeseddel – oppdater** redigerer du **Pakkesporingsnr.**</span><span class="sxs-lookup"><span data-stu-id="36e65-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="36e65-126">-feltet, for eksempel.</span><span class="sxs-lookup"><span data-stu-id="36e65-126">field, for example.</span></span>
4. <span data-ttu-id="36e65-127">Velg **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="36e65-127">Choose the **OK** button.</span></span>

<span data-ttu-id="36e65-128">Den bokførte følgeseddelen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="36e65-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="36e65-129">Se også</span><span class="sxs-lookup"><span data-stu-id="36e65-129">See Also</span></span>
[<span data-ttu-id="36e65-130">Generelle forretningsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="36e65-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="36e65-131">Innkjøp</span><span class="sxs-lookup"><span data-stu-id="36e65-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="36e65-132">Bokføre dokumenter og kladder</span><span class="sxs-lookup"><span data-stu-id="36e65-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="36e65-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="36e65-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>