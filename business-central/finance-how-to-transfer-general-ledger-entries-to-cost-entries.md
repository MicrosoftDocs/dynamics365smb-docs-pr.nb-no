---
title: "Overføre finansposter til kostposter | Microsoft-dokumentasjon"
description: "Du kan overføre finansposter til kostposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 273a8c4341f621710819fd5fbc5cb8ce579c86f5
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c3b1d-103">Overføre finansposter til kostposter</span><span class="sxs-lookup"><span data-stu-id="c3b1d-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="c3b1d-104">Du kan overføre finansposter til kostposter.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="c3b1d-105">Før du kjører prosessen for overføring av finansposter til kostposter, må du klargjøre overføringen for å unngå manuell korrigeringsbokføring.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="c3b1d-106">Klargjøre overføringen</span><span class="sxs-lookup"><span data-stu-id="c3b1d-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="c3b1d-107">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kostregnskapsoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c3b1d-108">På siden **Kostregnskapsoppsett** kontrollerer du at feltet **Startdato for finansoverføring** er satt til den riktige verdien.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="c3b1d-109">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Diagram med kosttyper**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="c3b1d-110">Kontroller at feltet **Finanskto. fra/til** på siden **Kosttypekort** er riktig koblet for hver kosttype, slik at poster hentes fra finans.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="c3b1d-111">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontoplan**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="c3b1d-112">For hver relevant finanskonto på **Finanskort-siden** kontrollerer du at **Kosttypenr.**</span><span class="sxs-lookup"><span data-stu-id="c3b1d-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="c3b1d-113">-feltet er riktig tilknyttet en kostnadstype.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="c3b1d-114">Hvis du vil ha mer informasjon, kan du se [Definere kostregnskap](finance-set-up-cost-accounting.md).</span><span class="sxs-lookup"><span data-stu-id="c3b1d-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="c3b1d-115">Kontroller at alle relevante finansposter har dimensjonsverdier som svarer til et kostsenter og et kostobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="c3b1d-116">Slik overfører du finansposter til kostposter:</span><span class="sxs-lookup"><span data-stu-id="c3b1d-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="c3b1d-117">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Overfør finansposter til KR**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c3b1d-118">Velg **Ja**-knappen for å starte overføringen.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="c3b1d-119">Prosessen overfører alle finansposter som ikke allerede er overført.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="c3b1d-120">Under overføringen oppretter prosessen forbindelser i postene i tabellen **Kostpost** og i tabellen **Kostjournal**.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="c3b1d-121">Dette gjør det mulig å spore kilden til kostposter.</span><span class="sxs-lookup"><span data-stu-id="c3b1d-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3b1d-122">Se også</span><span class="sxs-lookup"><span data-stu-id="c3b1d-122">See Also</span></span>  
<span data-ttu-id="c3b1d-123">[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="c3b1d-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="c3b1d-124">Definere kostregnskap</span><span class="sxs-lookup"><span data-stu-id="c3b1d-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   

