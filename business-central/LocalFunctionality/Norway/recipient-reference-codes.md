---
title: Referansekoder for mottaker
description: "Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren. Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen."
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
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: b2058eaeea9c71db7a58054371d901d04bf2868a
ms.contentlocale: nb-no
ms.lasthandoff: 10/15/2018

---
# <a name="recipient-reference-codes"></a><span data-ttu-id="25a4c-104">Referansekoder for mottaker</span><span class="sxs-lookup"><span data-stu-id="25a4c-104">Recipient Reference Codes</span></span>
<span data-ttu-id="25a4c-105">Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="25a4c-105">The recipient reference code determines the message that is sent to the recipient.</span></span> <span data-ttu-id="25a4c-106">Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="25a4c-106">The code is displayed on the remittance account and is used for vendors that are paid from this account.</span></span> <span data-ttu-id="25a4c-107">Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.</span><span class="sxs-lookup"><span data-stu-id="25a4c-107">For each vendor, a special recipient reference code can be created if the general reference text is not used.</span></span>  

<span data-ttu-id="25a4c-108">Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder.</span><span class="sxs-lookup"><span data-stu-id="25a4c-108">The text in recipient reference fields can be formatted automatically with special codes.</span></span> <span data-ttu-id="25a4c-109">Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut **Betaling av faktura nr. 10000**.</span><span class="sxs-lookup"><span data-stu-id="25a4c-109">For example, if you enter **Payment of Invoice %2** in a recipient reference field, the information that will print is **Payment of Invoice 10000**.</span></span>  

<span data-ttu-id="25a4c-110">Mottakerreferansekodene blir beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="25a4c-110">The recipient reference codes are described in the following table.</span></span>  

|<span data-ttu-id="25a4c-111">**Kode**</span><span class="sxs-lookup"><span data-stu-id="25a4c-111">**Code**</span></span>|<span data-ttu-id="25a4c-112">Description</span><span class="sxs-lookup"><span data-stu-id="25a4c-112">Description</span></span>|  
|--------------|---------------------------------------|  
|<span data-ttu-id="25a4c-113">**%1**</span><span class="sxs-lookup"><span data-stu-id="25a4c-113">**%1**</span></span>|<span data-ttu-id="25a4c-114">Bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="25a4c-114">The document type.</span></span> <span data-ttu-id="25a4c-115">Enten faktura eller kreditnota.</span><span class="sxs-lookup"><span data-stu-id="25a4c-115">Either invoice or credit memo.</span></span>|  
|<span data-ttu-id="25a4c-116">**%2**</span><span class="sxs-lookup"><span data-stu-id="25a4c-116">**%2**</span></span>|<span data-ttu-id="25a4c-117">Leverandørens fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="25a4c-117">The vendor's invoice number.</span></span>|  
|<span data-ttu-id="25a4c-118">**%3**</span><span class="sxs-lookup"><span data-stu-id="25a4c-118">**%3**</span></span>|<span data-ttu-id="25a4c-119">Feltet **Vårt kontonr.** fra **Leverandørkort**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="25a4c-119">The **Our Account No.** field from the **Vendor Card** window.</span></span> <span data-ttu-id="25a4c-120">Dette er vanligvis kundenummeret som brukes av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="25a4c-120">This is usually the customer number that is used by the vendor.</span></span>|  
|<span data-ttu-id="25a4c-121">**%4**</span><span class="sxs-lookup"><span data-stu-id="25a4c-121">**%4**</span></span>|<span data-ttu-id="25a4c-122">Faktura- eller kreditnotanummeret.</span><span class="sxs-lookup"><span data-stu-id="25a4c-122">The invoice or credit memo number.</span></span>|  
|<span data-ttu-id="25a4c-123">**%5**</span><span class="sxs-lookup"><span data-stu-id="25a4c-123">**%5**</span></span>|<span data-ttu-id="25a4c-124">Beskrivelsen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="25a4c-124">The description from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="25a4c-125">**%6**</span><span class="sxs-lookup"><span data-stu-id="25a4c-125">**%6**</span></span>|<span data-ttu-id="25a4c-126">Det opprinnelige beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="25a4c-126">The original amount from the vendor ledger entries.</span></span> <span data-ttu-id="25a4c-127">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="25a4c-127">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="25a4c-128">**%7**</span><span class="sxs-lookup"><span data-stu-id="25a4c-128">**%7**</span></span>|<span data-ttu-id="25a4c-129">Det resterende beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="25a4c-129">The remaining amount from the vendor ledger entries.</span></span> <span data-ttu-id="25a4c-130">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="25a4c-130">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="25a4c-131">**%8**</span><span class="sxs-lookup"><span data-stu-id="25a4c-131">**%8**</span></span>|<span data-ttu-id="25a4c-132">Beløpet fra leverandørposten i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="25a4c-132">The local currency amount from the vendor ledger entry.</span></span> <span data-ttu-id="25a4c-133">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="25a4c-133">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="25a4c-134">**%9**</span><span class="sxs-lookup"><span data-stu-id="25a4c-134">**%9**</span></span>|<span data-ttu-id="25a4c-135">Valutakoden fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="25a4c-135">The currency code from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="25a4c-136">**%10**</span><span class="sxs-lookup"><span data-stu-id="25a4c-136">**%10**</span></span>|<span data-ttu-id="25a4c-137">Forfallsdatoen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="25a4c-137">The due date from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="25a4c-138">**%11**</span><span class="sxs-lookup"><span data-stu-id="25a4c-138">**%11**</span></span>|<span data-ttu-id="25a4c-139">Kunde ID-nummeret fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="25a4c-139">The Kunde ID number from the vendor ledger entry.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="25a4c-140">Se også</span><span class="sxs-lookup"><span data-stu-id="25a4c-140">See Also</span></span>  
 [<span data-ttu-id="25a4c-141">Angi leverandører for remittering</span><span class="sxs-lookup"><span data-stu-id="25a4c-141">Set Up Vendors for Remittance</span></span>](how-to-set-up-vendors-for-remittance.md)

