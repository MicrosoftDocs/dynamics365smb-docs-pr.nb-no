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
ms.author: sgroespe
ms.openlocfilehash: d77592170dcf6bd05a4439a52e26e9f7f85e714c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181006"
---
# <a name="recipient-reference-codes"></a><span data-ttu-id="b2db2-104">Referansekoder for mottaker</span><span class="sxs-lookup"><span data-stu-id="b2db2-104">Recipient Reference Codes</span></span>
<span data-ttu-id="b2db2-105">Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="b2db2-105">The recipient reference code determines the message that is sent to the recipient.</span></span> <span data-ttu-id="b2db2-106">Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="b2db2-106">The code is displayed on the remittance account and is used for vendors that are paid from this account.</span></span> <span data-ttu-id="b2db2-107">Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.</span><span class="sxs-lookup"><span data-stu-id="b2db2-107">For each vendor, a special recipient reference code can be created if the general reference text is not used.</span></span>  

<span data-ttu-id="b2db2-108">Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder.</span><span class="sxs-lookup"><span data-stu-id="b2db2-108">The text in recipient reference fields can be formatted automatically with special codes.</span></span> <span data-ttu-id="b2db2-109">Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut, **Betaling av faktura nr. 10000**.</span><span class="sxs-lookup"><span data-stu-id="b2db2-109">For example, if you enter **Payment of Invoice %2** in a recipient reference field, the information that will print is **Payment of Invoice 10000**.</span></span>  

<span data-ttu-id="b2db2-110">Mottakerreferansekodene blir beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="b2db2-110">The recipient reference codes are described in the following table.</span></span>  

|<span data-ttu-id="b2db2-111">**Kode**</span><span class="sxs-lookup"><span data-stu-id="b2db2-111">**Code**</span></span>|<span data-ttu-id="b2db2-112">Description</span><span class="sxs-lookup"><span data-stu-id="b2db2-112">Description</span></span>|  
|--------------|---------------------------------------|  
|<span data-ttu-id="b2db2-113">**%1**</span><span class="sxs-lookup"><span data-stu-id="b2db2-113">**%1**</span></span>|<span data-ttu-id="b2db2-114">Bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="b2db2-114">The document type.</span></span> <span data-ttu-id="b2db2-115">Enten faktura eller kreditnota.</span><span class="sxs-lookup"><span data-stu-id="b2db2-115">Either invoice or credit memo.</span></span>|  
|<span data-ttu-id="b2db2-116">**%2**</span><span class="sxs-lookup"><span data-stu-id="b2db2-116">**%2**</span></span>|<span data-ttu-id="b2db2-117">Leverandørens fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="b2db2-117">The vendor's invoice number.</span></span>|  
|<span data-ttu-id="b2db2-118">**%3**</span><span class="sxs-lookup"><span data-stu-id="b2db2-118">**%3**</span></span>|<span data-ttu-id="b2db2-119">Feltet **Vårt kontonr.** på siden **Leverandørkort**.</span><span class="sxs-lookup"><span data-stu-id="b2db2-119">The **Our Account No.** field from the **Vendor Card** page.</span></span> <span data-ttu-id="b2db2-120">Dette er vanligvis kundenummeret som brukes av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b2db2-120">This is usually the customer number that is used by the vendor.</span></span>|  
|<span data-ttu-id="b2db2-121">**%4**</span><span class="sxs-lookup"><span data-stu-id="b2db2-121">**%4**</span></span>|<span data-ttu-id="b2db2-122">Faktura- eller kreditnotanummeret.</span><span class="sxs-lookup"><span data-stu-id="b2db2-122">The invoice or credit memo number.</span></span>|  
|<span data-ttu-id="b2db2-123">**%5**</span><span class="sxs-lookup"><span data-stu-id="b2db2-123">**%5**</span></span>|<span data-ttu-id="b2db2-124">Beskrivelsen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="b2db2-124">The description from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="b2db2-125">**%6**</span><span class="sxs-lookup"><span data-stu-id="b2db2-125">**%6**</span></span>|<span data-ttu-id="b2db2-126">Det opprinnelige beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="b2db2-126">The original amount from the vendor ledger entries.</span></span> <span data-ttu-id="b2db2-127">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="b2db2-127">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="b2db2-128">**%7**</span><span class="sxs-lookup"><span data-stu-id="b2db2-128">**%7**</span></span>|<span data-ttu-id="b2db2-129">Det resterende beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="b2db2-129">The remaining amount from the vendor ledger entries.</span></span> <span data-ttu-id="b2db2-130">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="b2db2-130">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="b2db2-131">**%8**</span><span class="sxs-lookup"><span data-stu-id="b2db2-131">**%8**</span></span>|<span data-ttu-id="b2db2-132">Beløpet fra leverandørposten i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="b2db2-132">The local currency amount from the vendor ledger entry.</span></span> <span data-ttu-id="b2db2-133">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="b2db2-133">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="b2db2-134">**%9**</span><span class="sxs-lookup"><span data-stu-id="b2db2-134">**%9**</span></span>|<span data-ttu-id="b2db2-135">Valutakoden fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="b2db2-135">The currency code from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="b2db2-136">**%10**</span><span class="sxs-lookup"><span data-stu-id="b2db2-136">**%10**</span></span>|<span data-ttu-id="b2db2-137">Forfallsdatoen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="b2db2-137">The due date from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="b2db2-138">**%11**</span><span class="sxs-lookup"><span data-stu-id="b2db2-138">**%11**</span></span>|<span data-ttu-id="b2db2-139">Kunde ID-nummeret fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="b2db2-139">The Kunde ID number from the vendor ledger entry.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b2db2-140">Se også</span><span class="sxs-lookup"><span data-stu-id="b2db2-140">See Also</span></span>  
 [<span data-ttu-id="b2db2-141">Angi leverandører for remittering</span><span class="sxs-lookup"><span data-stu-id="b2db2-141">Set Up Vendors for Remittance</span></span>](how-to-set-up-vendors-for-remittance.md)
