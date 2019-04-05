---
title: Resultater av overføringen | Microsoft-dokumentasjon
description: Dette emnet beskriver hva som skjer når du overfører finansposter til kostposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 0e17ff5ad60014cba6ce866c9ddae848b1239167
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803260"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="078a0-103">Resultater av overføring av finansposter til kostposter</span><span class="sxs-lookup"><span data-stu-id="078a0-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="078a0-104">Under overføring av finansposter til kostposter oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] forbindelser i postene i tabellen **Finanspost**, **Kostpri.** og **Kostjournal** for å gjøre det mulig å spore forbindelsene mellom kostposter og finansposter.</span><span class="sxs-lookup"><span data-stu-id="078a0-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="078a0-105">Finansposter</span><span class="sxs-lookup"><span data-stu-id="078a0-105">General Ledger Entries</span></span>  
<span data-ttu-id="078a0-106">For hver finanspost som overføres til kostregnskap, fyller [!INCLUDE[d365fin](includes/d365fin_md.md)] ut feltet **Postnr.**-feltet for kost.</span><span class="sxs-lookup"><span data-stu-id="078a0-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="078a0-107">Kostposter</span><span class="sxs-lookup"><span data-stu-id="078a0-107">Cost Entries</span></span>  
<span data-ttu-id="078a0-108">For hver kostpost lagrer [!INCLUDE[d365fin](includes/d365fin_md.md)] postnummeret for tilsvarende finanspost i feltet **Finansløpenr.** i tabellen **Kostpri.**</span><span class="sxs-lookup"><span data-stu-id="078a0-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="078a0-109">For kombinerte kostposter lagrer [!INCLUDE[d365fin](includes/d365fin_md.md)] postnummeret på den siste finansposten, som er posten med det høyeste postnummeret.</span><span class="sxs-lookup"><span data-stu-id="078a0-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="078a0-110">Feltet **Finanskonto** i tabellen **Kostpri.**-tabellen inneholder nummeret på finanskontoen som kostposten kom fra.</span><span class="sxs-lookup"><span data-stu-id="078a0-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="078a0-111">Når det gjelder enkeltkostposter, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] bokføringsteksten fra finansposten til **Beskrivelse**-tekstfeltet.</span><span class="sxs-lookup"><span data-stu-id="078a0-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="078a0-112">Når det gjelder kombinerte poster, viser tekstfeltet at disse postene overføres som kombinerte poster.</span><span class="sxs-lookup"><span data-stu-id="078a0-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="078a0-113">For en kombinert post for oktober i 2013 kan for eksempel teksten være **Kombinerte poster, oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="078a0-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="078a0-114">Kostjournal</span><span class="sxs-lookup"><span data-stu-id="078a0-114">Cost Register</span></span>  
<span data-ttu-id="078a0-115">I **Kostjournal**-tabellen oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] en post med kildeoverføringen fra finans.</span><span class="sxs-lookup"><span data-stu-id="078a0-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="078a0-116">Posten registrerer det første og det siste løpenummeret for finanspostene som overføres, i tillegg til det første og det siste løpenummeret for kostpostene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="078a0-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="078a0-117">Se også</span><span class="sxs-lookup"><span data-stu-id="078a0-117">See Also</span></span>  
[<span data-ttu-id="078a0-118">Overføre og bokføre kostposter</span><span class="sxs-lookup"><span data-stu-id="078a0-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
