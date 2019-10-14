---
title: Slik sperrer du varer fra salg eller kjøp ved salg til kunder
description: I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2b0d5b15571b7e8af1ed1dbee22859f4c131aa3
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316623"
---
# <a name="block-customers"></a><span data-ttu-id="45890-103">Sperre kunder</span><span class="sxs-lookup"><span data-stu-id="45890-103">Block Customers</span></span>
<span data-ttu-id="45890-104">Du kan sperre en kunde, for eksempel på grunn av insolvens, slik at kunden ikke kan legges til i salgsdokumenter, eller slik at ingen transaksjoner kan bokføres for kunden.</span><span class="sxs-lookup"><span data-stu-id="45890-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="45890-105">I tillegg til å sperre en kunde kan du angi at fordringstransaksjoner for kunden skal settes på vent i forbindelse med purringer.</span><span class="sxs-lookup"><span data-stu-id="45890-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="45890-106">Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="45890-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="45890-107">Tabellen nedenfor beskriver de ulike sperrealternativene.</span><span class="sxs-lookup"><span data-stu-id="45890-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="45890-108">Alternativ</span><span class="sxs-lookup"><span data-stu-id="45890-108">Option</span></span>|<span data-ttu-id="45890-109">Description</span><span class="sxs-lookup"><span data-stu-id="45890-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="45890-110">**Tom**</span><span class="sxs-lookup"><span data-stu-id="45890-110">**Blank**</span></span>|<span data-ttu-id="45890-111">Transaksjoner er tillatt for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="45890-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="45890-112">**Levering**</span><span class="sxs-lookup"><span data-stu-id="45890-112">**Ship**</span></span>|<span data-ttu-id="45890-113">Det kan ikke opprettes nye ordrer og nye leveringer for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="45890-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="45890-114">Eksisterende leveringer som ennå ikke er fakturert, kan faktureres.</span><span class="sxs-lookup"><span data-stu-id="45890-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="45890-115">**Fakturering**</span><span class="sxs-lookup"><span data-stu-id="45890-115">**Invoice**</span></span>|<span data-ttu-id="45890-116">Det kan ikke opprettes nye ordrer, nye leveringer og nye fakturaer for denne kunden.</span><span class="sxs-lookup"><span data-stu-id="45890-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="45890-117">Eksisterende leveringer som ennå ikke er fakturert, kan ikke faktureres.</span><span class="sxs-lookup"><span data-stu-id="45890-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="45890-118">**Alle**</span><span class="sxs-lookup"><span data-stu-id="45890-118">**All**</span></span>|<span data-ttu-id="45890-119">Ingen transaksjoner er tillatt for denne kunden, inkludert betalinger.</span><span class="sxs-lookup"><span data-stu-id="45890-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="45890-120">Slik sperrer du en kunde:</span><span class="sxs-lookup"><span data-stu-id="45890-120">To block a customer</span></span>  
1. <span data-ttu-id="45890-121">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="45890-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="45890-122">Velg en kunde, og velg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="45890-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="45890-123">Fyll ut feltet **Sperret** med ett av alternativene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="45890-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="45890-124">Se også</span><span class="sxs-lookup"><span data-stu-id="45890-124">See Also</span></span>  
[<span data-ttu-id="45890-125">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="45890-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="45890-126">Innkreve utestående saldi</span><span class="sxs-lookup"><span data-stu-id="45890-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="45890-127">Håndtere fordringer</span><span class="sxs-lookup"><span data-stu-id="45890-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
