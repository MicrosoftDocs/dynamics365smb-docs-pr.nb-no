---
title: Referansekoder for mottaker
description: Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren. Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 73814b4010111845dc1a58308183d09958ea133a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382797"
---
# <a name="recipient-reference-codes"></a><span data-ttu-id="22c39-104">Referansekoder for mottaker</span><span class="sxs-lookup"><span data-stu-id="22c39-104">Recipient Reference Codes</span></span>
<span data-ttu-id="22c39-105">Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="22c39-105">The recipient reference code determines the message that is sent to the recipient.</span></span> <span data-ttu-id="22c39-106">Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="22c39-106">The code is displayed on the remittance account and is used for vendors that are paid from this account.</span></span> <span data-ttu-id="22c39-107">Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.</span><span class="sxs-lookup"><span data-stu-id="22c39-107">For each vendor, a special recipient reference code can be created if the general reference text is not used.</span></span>  

<span data-ttu-id="22c39-108">Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder.</span><span class="sxs-lookup"><span data-stu-id="22c39-108">The text in recipient reference fields can be formatted automatically with special codes.</span></span> <span data-ttu-id="22c39-109">Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut, **Betaling av faktura nr. 10000**.</span><span class="sxs-lookup"><span data-stu-id="22c39-109">For example, if you enter **Payment of Invoice %2** in a recipient reference field, the information that will print is **Payment of Invoice 10000**.</span></span>  

<span data-ttu-id="22c39-110">Mottakerreferansekodene blir beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="22c39-110">The recipient reference codes are described in the following table.</span></span>  

|<span data-ttu-id="22c39-111">**Kode**</span><span class="sxs-lookup"><span data-stu-id="22c39-111">**Code**</span></span>|<span data-ttu-id="22c39-112">Description</span><span class="sxs-lookup"><span data-stu-id="22c39-112">Description</span></span>|  
|--------------|---------------------------------------|  
|<span data-ttu-id="22c39-113">**%1**</span><span class="sxs-lookup"><span data-stu-id="22c39-113">**%1**</span></span>|<span data-ttu-id="22c39-114">Bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="22c39-114">The document type.</span></span> <span data-ttu-id="22c39-115">Enten faktura eller kreditnota.</span><span class="sxs-lookup"><span data-stu-id="22c39-115">Either invoice or credit memo.</span></span>|  
|<span data-ttu-id="22c39-116">**%2**</span><span class="sxs-lookup"><span data-stu-id="22c39-116">**%2**</span></span>|<span data-ttu-id="22c39-117">Leverandørens fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="22c39-117">The vendor's invoice number.</span></span>|  
|<span data-ttu-id="22c39-118">**%3**</span><span class="sxs-lookup"><span data-stu-id="22c39-118">**%3**</span></span>|<span data-ttu-id="22c39-119">Feltet **Vårt kontonr.** på siden **Leverandørkort**.</span><span class="sxs-lookup"><span data-stu-id="22c39-119">The **Our Account No.** field from the **Vendor Card** page.</span></span> <span data-ttu-id="22c39-120">Dette er vanligvis kundenummeret som brukes av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="22c39-120">This is usually the customer number that is used by the vendor.</span></span>|  
|<span data-ttu-id="22c39-121">**%4**</span><span class="sxs-lookup"><span data-stu-id="22c39-121">**%4**</span></span>|<span data-ttu-id="22c39-122">Faktura- eller kreditnotanummeret.</span><span class="sxs-lookup"><span data-stu-id="22c39-122">The invoice or credit memo number.</span></span>|  
|<span data-ttu-id="22c39-123">**%5**</span><span class="sxs-lookup"><span data-stu-id="22c39-123">**%5**</span></span>|<span data-ttu-id="22c39-124">Beskrivelsen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="22c39-124">The description from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="22c39-125">**%6**</span><span class="sxs-lookup"><span data-stu-id="22c39-125">**%6**</span></span>|<span data-ttu-id="22c39-126">Det opprinnelige beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="22c39-126">The original amount from the vendor ledger entries.</span></span> <span data-ttu-id="22c39-127">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="22c39-127">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="22c39-128">**%7**</span><span class="sxs-lookup"><span data-stu-id="22c39-128">**%7**</span></span>|<span data-ttu-id="22c39-129">Det resterende beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="22c39-129">The remaining amount from the vendor ledger entries.</span></span> <span data-ttu-id="22c39-130">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="22c39-130">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="22c39-131">**%8**</span><span class="sxs-lookup"><span data-stu-id="22c39-131">**%8**</span></span>|<span data-ttu-id="22c39-132">Beløpet fra leverandørposten i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="22c39-132">The local currency amount from the vendor ledger entry.</span></span> <span data-ttu-id="22c39-133">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="22c39-133">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="22c39-134">**%9**</span><span class="sxs-lookup"><span data-stu-id="22c39-134">**%9**</span></span>|<span data-ttu-id="22c39-135">Valutakoden fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="22c39-135">The currency code from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="22c39-136">**%10**</span><span class="sxs-lookup"><span data-stu-id="22c39-136">**%10**</span></span>|<span data-ttu-id="22c39-137">Forfallsdatoen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="22c39-137">The due date from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="22c39-138">**%11**</span><span class="sxs-lookup"><span data-stu-id="22c39-138">**%11**</span></span>|<span data-ttu-id="22c39-139">Kunde ID-nummeret fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="22c39-139">The Kunde ID number from the vendor ledger entry.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="22c39-140">Se også</span><span class="sxs-lookup"><span data-stu-id="22c39-140">See Also</span></span>  
 [<span data-ttu-id="22c39-141">Angi leverandører for remittering</span><span class="sxs-lookup"><span data-stu-id="22c39-141">Set Up Vendors for Remittance</span></span>](how-to-set-up-vendors-for-remittance.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]