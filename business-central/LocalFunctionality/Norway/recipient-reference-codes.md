---
title: Referansekoder for mottaker
description: Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren. Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 5d6e8d8ab985ded26a159a7e02713f26d298b3ec
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777897"
---
# <a name="recipient-reference-codes"></a><span data-ttu-id="ffd43-104">Referansekoder for mottaker</span><span class="sxs-lookup"><span data-stu-id="ffd43-104">Recipient Reference Codes</span></span>
<span data-ttu-id="ffd43-105">Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="ffd43-105">The recipient reference code determines the message that is sent to the recipient.</span></span> <span data-ttu-id="ffd43-106">Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="ffd43-106">The code is displayed on the remittance account and is used for vendors that are paid from this account.</span></span> <span data-ttu-id="ffd43-107">Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.</span><span class="sxs-lookup"><span data-stu-id="ffd43-107">For each vendor, a special recipient reference code can be created if the general reference text is not used.</span></span>  

<span data-ttu-id="ffd43-108">Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder.</span><span class="sxs-lookup"><span data-stu-id="ffd43-108">The text in recipient reference fields can be formatted automatically with special codes.</span></span> <span data-ttu-id="ffd43-109">Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut, **Betaling av faktura nr. 10000**.</span><span class="sxs-lookup"><span data-stu-id="ffd43-109">For example, if you enter **Payment of Invoice %2** in a recipient reference field, the information that will print is **Payment of Invoice 10000**.</span></span>  

<span data-ttu-id="ffd43-110">Mottakerreferansekodene blir beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ffd43-110">The recipient reference codes are described in the following table.</span></span>  

|<span data-ttu-id="ffd43-111">**Kode**</span><span class="sxs-lookup"><span data-stu-id="ffd43-111">**Code**</span></span>|<span data-ttu-id="ffd43-112">Description</span><span class="sxs-lookup"><span data-stu-id="ffd43-112">Description</span></span>|  
|--------------|---------------------------------------|  
|<span data-ttu-id="ffd43-113">**%1**</span><span class="sxs-lookup"><span data-stu-id="ffd43-113">**%1**</span></span>|<span data-ttu-id="ffd43-114">Bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="ffd43-114">The document type.</span></span> <span data-ttu-id="ffd43-115">Enten faktura eller kreditnota.</span><span class="sxs-lookup"><span data-stu-id="ffd43-115">Either invoice or credit memo.</span></span>|  
|<span data-ttu-id="ffd43-116">**%2**</span><span class="sxs-lookup"><span data-stu-id="ffd43-116">**%2**</span></span>|<span data-ttu-id="ffd43-117">Leverandørens fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="ffd43-117">The vendor's invoice number.</span></span>|  
|<span data-ttu-id="ffd43-118">**%3**</span><span class="sxs-lookup"><span data-stu-id="ffd43-118">**%3**</span></span>|<span data-ttu-id="ffd43-119">Feltet **Vårt kontonr.** på siden **Leverandørkort**.</span><span class="sxs-lookup"><span data-stu-id="ffd43-119">The **Our Account No.** field from the **Vendor Card** page.</span></span> <span data-ttu-id="ffd43-120">Dette er vanligvis kundenummeret som brukes av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="ffd43-120">This is usually the customer number that is used by the vendor.</span></span>|  
|<span data-ttu-id="ffd43-121">**%4**</span><span class="sxs-lookup"><span data-stu-id="ffd43-121">**%4**</span></span>|<span data-ttu-id="ffd43-122">Faktura- eller kreditnotanummeret.</span><span class="sxs-lookup"><span data-stu-id="ffd43-122">The invoice or credit memo number.</span></span>|  
|<span data-ttu-id="ffd43-123">**%5**</span><span class="sxs-lookup"><span data-stu-id="ffd43-123">**%5**</span></span>|<span data-ttu-id="ffd43-124">Beskrivelsen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="ffd43-124">The description from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="ffd43-125">**%6**</span><span class="sxs-lookup"><span data-stu-id="ffd43-125">**%6**</span></span>|<span data-ttu-id="ffd43-126">Det opprinnelige beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="ffd43-126">The original amount from the vendor ledger entries.</span></span> <span data-ttu-id="ffd43-127">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="ffd43-127">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="ffd43-128">**%7**</span><span class="sxs-lookup"><span data-stu-id="ffd43-128">**%7**</span></span>|<span data-ttu-id="ffd43-129">Det resterende beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="ffd43-129">The remaining amount from the vendor ledger entries.</span></span> <span data-ttu-id="ffd43-130">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="ffd43-130">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="ffd43-131">**%8**</span><span class="sxs-lookup"><span data-stu-id="ffd43-131">**%8**</span></span>|<span data-ttu-id="ffd43-132">Beløpet fra leverandørposten i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="ffd43-132">The local currency amount from the vendor ledger entry.</span></span> <span data-ttu-id="ffd43-133">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="ffd43-133">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="ffd43-134">**%9**</span><span class="sxs-lookup"><span data-stu-id="ffd43-134">**%9**</span></span>|<span data-ttu-id="ffd43-135">Valutakoden fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="ffd43-135">The currency code from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="ffd43-136">**%10**</span><span class="sxs-lookup"><span data-stu-id="ffd43-136">**%10**</span></span>|<span data-ttu-id="ffd43-137">Forfallsdatoen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="ffd43-137">The due date from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="ffd43-138">**%11**</span><span class="sxs-lookup"><span data-stu-id="ffd43-138">**%11**</span></span>|<span data-ttu-id="ffd43-139">Kunde ID-nummeret fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="ffd43-139">The Kunde ID number from the vendor ledger entry.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="ffd43-140">Se også</span><span class="sxs-lookup"><span data-stu-id="ffd43-140">See Also</span></span>  
 [<span data-ttu-id="ffd43-141">Angi leverandører for remittering</span><span class="sxs-lookup"><span data-stu-id="ffd43-141">Set Up Vendors for Remittance</span></span>](how-to-set-up-vendors-for-remittance.md)
