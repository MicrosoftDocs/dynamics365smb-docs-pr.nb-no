---
title: Slik blokkerer du salg til kunder
description: Hvis du må, kan du sperre en kunde fra å bli inkludert i salgsdokumenter og andre salgstransaksjoner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781741"
---
# <a name="block-customers"></a><span data-ttu-id="2e597-103">Sperre kunder</span><span class="sxs-lookup"><span data-stu-id="2e597-103">Block Customers</span></span>
<span data-ttu-id="2e597-104">Du kan sperre en kunde, for eksempel på grunn av insolvens, slik at kunden ikke kan legges til i salgsdokumenter, eller slik at ingen transaksjoner kan bokføres for kunden.</span><span class="sxs-lookup"><span data-stu-id="2e597-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="2e597-105">I tillegg til å sperre en kunde kan du angi at fordringstransaksjoner for kunden skal settes på vent i forbindelse med purringer.</span><span class="sxs-lookup"><span data-stu-id="2e597-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="2e597-106">Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="2e597-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="2e597-107">Tabellen nedenfor beskriver alternativene for å sperre kunder.</span><span class="sxs-lookup"><span data-stu-id="2e597-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="2e597-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="2e597-108">Option</span></span>|<span data-ttu-id="2e597-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2e597-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="2e597-110">**Tom**</span><span class="sxs-lookup"><span data-stu-id="2e597-110">**Blank**</span></span>|<span data-ttu-id="2e597-111">Transaksjoner er tillatt for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="2e597-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="2e597-112">**Levering**</span><span class="sxs-lookup"><span data-stu-id="2e597-112">**Ship**</span></span>|<span data-ttu-id="2e597-113">Det kan ikke opprettes nye ordrer og nye leveringer for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="2e597-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="2e597-114">Eksisterende leveringer som ennå ikke er fakturert, kan faktureres.</span><span class="sxs-lookup"><span data-stu-id="2e597-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="2e597-115">**Fakturering**</span><span class="sxs-lookup"><span data-stu-id="2e597-115">**Invoice**</span></span>|<span data-ttu-id="2e597-116">Det kan ikke opprettes nye ordrer, nye leveringer og nye fakturaer for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="2e597-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="2e597-117">Eksisterende leveringer som ennå ikke er fakturert, kan ikke faktureres.</span><span class="sxs-lookup"><span data-stu-id="2e597-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="2e597-118">Du kan fortsatt sende purringer og rentenotaer til kunden.</span><span class="sxs-lookup"><span data-stu-id="2e597-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="2e597-119">**Alle**</span><span class="sxs-lookup"><span data-stu-id="2e597-119">**All**</span></span>|<span data-ttu-id="2e597-120">Ingen transaksjoner er tillatt for denne kunden, inkludert betalinger.</span><span class="sxs-lookup"><span data-stu-id="2e597-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="2e597-121">Slik sperrer du en kunde:</span><span class="sxs-lookup"><span data-stu-id="2e597-121">To block a customer</span></span>  
1. <span data-ttu-id="2e597-122">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2e597-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="2e597-123">Velg en kunde, og velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="2e597-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="2e597-124">I **Sperret**-feltet velger du hva som skal sperres, som beskrevet i tabellen ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2e597-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e597-125">Se også</span><span class="sxs-lookup"><span data-stu-id="2e597-125">See Also</span></span>  
[<span data-ttu-id="2e597-126">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="2e597-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="2e597-127">Innkreve utestående saldi</span><span class="sxs-lookup"><span data-stu-id="2e597-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="2e597-128">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="2e597-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]