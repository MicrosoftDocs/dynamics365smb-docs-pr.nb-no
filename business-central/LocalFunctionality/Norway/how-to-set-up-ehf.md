---
title: Sette opp EHF
description: Du må definere en lokasjon for lagring av EHF-filer (Elektronisk Handelsformat) når du oppretter elektroniske dokumenter, for eksempel fakturaer og kreditnotaer. Du må også definere betalingsmåter og definere aktuelle kunder for EHF.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 594e0263a754dfc07b01e8e8948e47e3fff21676
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241649"
---
# <a name="set-up-ehf"></a><span data-ttu-id="f3bac-104">Angi EHF</span><span class="sxs-lookup"><span data-stu-id="f3bac-104">Set Up EHF</span></span>
<span data-ttu-id="f3bac-105">Du må definere en lokasjon for lagring av EHF-filer (Elektronisk Handelsformat) når du oppretter elektroniske dokumenter, for eksempel fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-105">You must define a location for storing Elektronisk Handelsformat (EHF) files when you create electronic documents such as invoices or credit memos.</span></span> <span data-ttu-id="f3bac-106">Du må også definere betalingsmåter og definere aktuelle kunder for EHF.</span><span class="sxs-lookup"><span data-stu-id="f3bac-106">You must also define payment methods and set up relevant customers for EHF.</span></span>  

## <a name="to-set-up-ehf-file-locations-for-sales-and-receivables"></a><span data-ttu-id="f3bac-107">Slik definerer du EHF-filplasseringer for salg:</span><span class="sxs-lookup"><span data-stu-id="f3bac-107">To set up EHF file locations for sales and receivables</span></span>  

1.  <span data-ttu-id="f3bac-108">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f3bac-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3bac-109">På siden **Salgsoppsett**-vinduet på **E-faktura**-hurtigfanen i **Utdatabaner**-delen, fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f3bac-109">On the **Sales & Receivables Setup** page, on the **E-Invoice** FastTab, in the **Output Paths** section, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f3bac-110">Felt</span><span class="sxs-lookup"><span data-stu-id="f3bac-110">Field</span></span>|<span data-ttu-id="f3bac-111">Description</span><span class="sxs-lookup"><span data-stu-id="f3bac-111">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f3bac-112">**Fakturabane**</span><span class="sxs-lookup"><span data-stu-id="f3bac-112">**Invoice Path**</span></span>|<span data-ttu-id="f3bac-113">Banen til og navnet på mappen der du vil lagre EHF-filene for salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-113">The path and name of the folder where you want to store the EHF files for sales invoices.</span></span>|  
    |<span data-ttu-id="f3bac-114">**Kreditnotabane**</span><span class="sxs-lookup"><span data-stu-id="f3bac-114">**Cr. Memo Path**</span></span>|<span data-ttu-id="f3bac-115">Banen til og navnet på mappen der du vil lagre EHF-filene for salgskreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-115">The path and name of the folder where you want to store the EHF files for sales credit memos.</span></span>|  
    |<span data-ttu-id="f3bac-116">**E-faktura - purrebane**</span><span class="sxs-lookup"><span data-stu-id="f3bac-116">**E-Invoice Reminder Path**</span></span>|<span data-ttu-id="f3bac-117">Banen til og navnet på mappen der du vil lagre EHF-filene for purringer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-117">The path and name of the folder where you want to store the EHF files for reminders.</span></span>|  
    |<span data-ttu-id="f3bac-118">**E-faktura - rentenotabane**</span><span class="sxs-lookup"><span data-stu-id="f3bac-118">**E-Invoice Fin. Charge Path**</span></span>|<span data-ttu-id="f3bac-119">Banen til og navnet på mappen der du vil lagre EHF-filene for rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-119">The path and name of the folder where you want to store the EHF files for finance charge memos.</span></span>|  

3.  <span data-ttu-id="f3bac-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3bac-120">Choose the **OK** button.</span></span>  

## <a name="to-set-up-ehf-file-locations-for-service-management"></a><span data-ttu-id="f3bac-121">Slik definerer du EHF-filplasseringer for servicestyring:</span><span class="sxs-lookup"><span data-stu-id="f3bac-121">To set up EHF file locations for service management</span></span>  

1.  <span data-ttu-id="f3bac-122">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="f3bac-122">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Mgt. Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3bac-123">På **Serviceoppsett**-siden på **E-faktura**-hurtigfanen i **Utdatabaner**-delen, fyller du ut feltene som beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="f3bac-123">On the **Service Mgt. Setup** page, on the **E-Invoice** FastTab, in the **Output Paths** section, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f3bac-124">Felt</span><span class="sxs-lookup"><span data-stu-id="f3bac-124">Field</span></span>|<span data-ttu-id="f3bac-125">Description</span><span class="sxs-lookup"><span data-stu-id="f3bac-125">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f3bac-126">**E-faktura - servicefakturabane**</span><span class="sxs-lookup"><span data-stu-id="f3bac-126">**E-Invoice Service Invoice Path**</span></span>|<span data-ttu-id="f3bac-127">Banen til og navnet på mappen der du vil lagre EHF-filene for servicefakturaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-127">The path and name of the folder where you want to store the EHF files for service invoices.</span></span>|  
    |<span data-ttu-id="f3bac-128">**E-faktura - salgskreditnotabane (service)**</span><span class="sxs-lookup"><span data-stu-id="f3bac-128">**E-Invoice Serv. Cr. Memo Path**</span></span>|<span data-ttu-id="f3bac-129">Banen til og navnet på mappen der du vil lagre EHF-filene for servicekreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="f3bac-129">The path and name of the folder where you want to store the EHF files for service credit memos.</span></span>|  

3.  <span data-ttu-id="f3bac-130">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3bac-130">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3bac-131">Se også</span><span class="sxs-lookup"><span data-stu-id="f3bac-131">See Also</span></span>  
 <span data-ttu-id="f3bac-132">[Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md) </span><span class="sxs-lookup"><span data-stu-id="f3bac-132">[Set Up Customers for EHF](how-to-set-up-customers-for-ehf.md) </span></span>  
 [<span data-ttu-id="f3bac-133">EHF – Elektronisk fakturering i Norge</span><span class="sxs-lookup"><span data-stu-id="f3bac-133">EHF Electronic Invoicing in Norway</span></span>](ehf-electronic-invoicing-in-norway.md)
