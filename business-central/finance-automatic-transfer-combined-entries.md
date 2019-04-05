---
title: Automatisk overføring og sammensatte poster | Microsoft-dokumentasjon
description: I kostnadsregnskap kan du overføre finansposter til en kosttype ved å bruke en kombinert bokføring. Du kan angi om en kosttype mottar kombinerte poster i feltet **Kombiner poster** i kosttypedefinisjonen. Tabellen nedenfor beskriver de ulike alternativene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802579"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="e9201-105">Automatisk overføring og sammensatte poster</span><span class="sxs-lookup"><span data-stu-id="e9201-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="e9201-106">I kostnadsregnskap kan du overføre finansposter til en kosttype ved å bruke en kombinert bokføring.</span><span class="sxs-lookup"><span data-stu-id="e9201-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="e9201-107">Du kan angi om en kosttype mottar kombinerte poster i feltet **Kombiner poster** i kosttypedefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="e9201-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="e9201-108">Tabellen nedenfor beskriver de ulike alternativene.</span><span class="sxs-lookup"><span data-stu-id="e9201-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="e9201-109">Kombiner poster</span><span class="sxs-lookup"><span data-stu-id="e9201-109">Combine entries</span></span>|<span data-ttu-id="e9201-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e9201-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="e9201-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9201-111">None</span></span>|<span data-ttu-id="e9201-112">Hver finanspost overføres individuelt til tilsvarende kosttype.</span><span class="sxs-lookup"><span data-stu-id="e9201-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="e9201-113">Dag</span><span class="sxs-lookup"><span data-stu-id="e9201-113">Day</span></span>|<span data-ttu-id="e9201-114">Finansposter med samme bokføringsdato overføres som én post til tilsvarende kosttype.</span><span class="sxs-lookup"><span data-stu-id="e9201-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="e9201-115">Måned</span><span class="sxs-lookup"><span data-stu-id="e9201-115">Month</span></span>|<span data-ttu-id="e9201-116">Alle finansposter som har samme kalendermåned, overføres som én post til den tilsvarende kosttypen.</span><span class="sxs-lookup"><span data-stu-id="e9201-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="e9201-117">Hvis du har merket av for **Overfør automatisk fra Finans** på siden **Kostregnskapsoppsett**, oppdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] kostregnskapet etter hver bokføring i finans.</span><span class="sxs-lookup"><span data-stu-id="e9201-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="e9201-118">Kombinerte poster er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="e9201-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9201-119">Se også</span><span class="sxs-lookup"><span data-stu-id="e9201-119">See Also</span></span>  
 <span data-ttu-id="e9201-120">[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="e9201-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="e9201-121">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9201-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
