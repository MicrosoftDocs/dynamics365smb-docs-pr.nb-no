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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 22984af4c0fcdf4d61c39c2dfe170adb9641e915
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921328"
---
# <a name="recipient-reference-codes"></a><span data-ttu-id="07309-104">Referansekoder for mottaker</span><span class="sxs-lookup"><span data-stu-id="07309-104">Recipient Reference Codes</span></span>
<span data-ttu-id="07309-105">Mottakerreferansekoden bestemmer hvilken melding som skal sendes til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="07309-105">The recipient reference code determines the message that is sent to the recipient.</span></span> <span data-ttu-id="07309-106">Koden vises i remitteringskontoen, og brukes for leverandører som betales fra denne kontoen.</span><span class="sxs-lookup"><span data-stu-id="07309-106">The code is displayed on the remittance account and is used for vendors that are paid from this account.</span></span> <span data-ttu-id="07309-107">Det kan opprettes en egen mottakerreferansekode for hver leverandør hvis den generelle referanseteksten ikke benyttes.</span><span class="sxs-lookup"><span data-stu-id="07309-107">For each vendor, a special recipient reference code can be created if the general reference text is not used.</span></span>  

<span data-ttu-id="07309-108">Teksten i mottakerreferansefeltene kan formateres automatisk ved hjelp av spesielle koder.</span><span class="sxs-lookup"><span data-stu-id="07309-108">The text in recipient reference fields can be formatted automatically with special codes.</span></span> <span data-ttu-id="07309-109">Hvis du for eksempel angir **Betaling av faktura nr. %2** i et mottakerreferansefelt, blir informasjonen som skrives ut, **Betaling av faktura nr. 10000**.</span><span class="sxs-lookup"><span data-stu-id="07309-109">For example, if you enter **Payment of Invoice %2** in a recipient reference field, the information that will print is **Payment of Invoice 10000**.</span></span>  

<span data-ttu-id="07309-110">Mottakerreferansekodene blir beskrevet i tabellen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="07309-110">The recipient reference codes are described in the following table.</span></span>  

|<span data-ttu-id="07309-111">**Kode**</span><span class="sxs-lookup"><span data-stu-id="07309-111">**Code**</span></span>|<span data-ttu-id="07309-112">Description</span><span class="sxs-lookup"><span data-stu-id="07309-112">Description</span></span>|  
|--------------|---------------------------------------|  
|<span data-ttu-id="07309-113">**%1**</span><span class="sxs-lookup"><span data-stu-id="07309-113">**%1**</span></span>|<span data-ttu-id="07309-114">Bilagstypen.</span><span class="sxs-lookup"><span data-stu-id="07309-114">The document type.</span></span> <span data-ttu-id="07309-115">Enten faktura eller kreditnota.</span><span class="sxs-lookup"><span data-stu-id="07309-115">Either invoice or credit memo.</span></span>|  
|<span data-ttu-id="07309-116">**%2**</span><span class="sxs-lookup"><span data-stu-id="07309-116">**%2**</span></span>|<span data-ttu-id="07309-117">Leverandørens fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="07309-117">The vendor's invoice number.</span></span>|  
|<span data-ttu-id="07309-118">**%3**</span><span class="sxs-lookup"><span data-stu-id="07309-118">**%3**</span></span>|<span data-ttu-id="07309-119">Feltet **Vårt kontonr.** på siden **Leverandørkort**.</span><span class="sxs-lookup"><span data-stu-id="07309-119">The **Our Account No.** field from the **Vendor Card** page.</span></span> <span data-ttu-id="07309-120">Dette er vanligvis kundenummeret som brukes av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="07309-120">This is usually the customer number that is used by the vendor.</span></span>|  
|<span data-ttu-id="07309-121">**%4**</span><span class="sxs-lookup"><span data-stu-id="07309-121">**%4**</span></span>|<span data-ttu-id="07309-122">Faktura- eller kreditnotanummeret.</span><span class="sxs-lookup"><span data-stu-id="07309-122">The invoice or credit memo number.</span></span>|  
|<span data-ttu-id="07309-123">**%5**</span><span class="sxs-lookup"><span data-stu-id="07309-123">**%5**</span></span>|<span data-ttu-id="07309-124">Beskrivelsen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="07309-124">The description from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="07309-125">**%6**</span><span class="sxs-lookup"><span data-stu-id="07309-125">**%6**</span></span>|<span data-ttu-id="07309-126">Det opprinnelige beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="07309-126">The original amount from the vendor ledger entries.</span></span> <span data-ttu-id="07309-127">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="07309-127">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="07309-128">**%7**</span><span class="sxs-lookup"><span data-stu-id="07309-128">**%7**</span></span>|<span data-ttu-id="07309-129">Det resterende beløpet fra leverandørpostene.</span><span class="sxs-lookup"><span data-stu-id="07309-129">The remaining amount from the vendor ledger entries.</span></span> <span data-ttu-id="07309-130">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="07309-130">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="07309-131">**%8**</span><span class="sxs-lookup"><span data-stu-id="07309-131">**%8**</span></span>|<span data-ttu-id="07309-132">Beløpet fra leverandørposten i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="07309-132">The local currency amount from the vendor ledger entry.</span></span> <span data-ttu-id="07309-133">Beløpet vises med positivt fortegn.</span><span class="sxs-lookup"><span data-stu-id="07309-133">The amount is shown as positive.</span></span>|  
|<span data-ttu-id="07309-134">**%9**</span><span class="sxs-lookup"><span data-stu-id="07309-134">**%9**</span></span>|<span data-ttu-id="07309-135">Valutakoden fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="07309-135">The currency code from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="07309-136">**%10**</span><span class="sxs-lookup"><span data-stu-id="07309-136">**%10**</span></span>|<span data-ttu-id="07309-137">Forfallsdatoen fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="07309-137">The due date from the vendor ledger entry.</span></span>|  
|<span data-ttu-id="07309-138">**%11**</span><span class="sxs-lookup"><span data-stu-id="07309-138">**%11**</span></span>|<span data-ttu-id="07309-139">Kunde ID-nummeret fra leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="07309-139">The Kunde ID number from the vendor ledger entry.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="07309-140">Se også</span><span class="sxs-lookup"><span data-stu-id="07309-140">See Also</span></span>  
 [<span data-ttu-id="07309-141">Angi leverandører for remittering</span><span class="sxs-lookup"><span data-stu-id="07309-141">Set Up Vendors for Remittance</span></span>](how-to-set-up-vendors-for-remittance.md)
