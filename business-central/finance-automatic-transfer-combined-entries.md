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
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238995"
---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="17311-105">Automatisk overføring og sammensatte poster</span><span class="sxs-lookup"><span data-stu-id="17311-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="17311-106">I kostnadsregnskap kan du overføre finansposter til en kosttype ved å bruke en kombinert bokføring.</span><span class="sxs-lookup"><span data-stu-id="17311-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="17311-107">Du kan angi om en kosttype mottar kombinerte poster i feltet **Kombiner poster** i kosttypedefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="17311-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="17311-108">Tabellen nedenfor beskriver de ulike alternativene.</span><span class="sxs-lookup"><span data-stu-id="17311-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="17311-109">Kombiner poster</span><span class="sxs-lookup"><span data-stu-id="17311-109">Combine entries</span></span>|<span data-ttu-id="17311-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="17311-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="17311-111">Ingen</span><span class="sxs-lookup"><span data-stu-id="17311-111">None</span></span>|<span data-ttu-id="17311-112">Hver finanspost overføres individuelt til tilsvarende kosttype.</span><span class="sxs-lookup"><span data-stu-id="17311-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="17311-113">Dag</span><span class="sxs-lookup"><span data-stu-id="17311-113">Day</span></span>|<span data-ttu-id="17311-114">Finansposter med samme bokføringsdato overføres som én post til tilsvarende kosttype.</span><span class="sxs-lookup"><span data-stu-id="17311-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="17311-115">Måned</span><span class="sxs-lookup"><span data-stu-id="17311-115">Month</span></span>|<span data-ttu-id="17311-116">Alle finansposter som har samme kalendermåned, overføres som én post til den tilsvarende kosttypen.</span><span class="sxs-lookup"><span data-stu-id="17311-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="17311-117">Hvis du har merket av for **Overfør automatisk fra Finans** på siden **Kostregnskapsoppsett**, oppdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] kostregnskapet etter hver bokføring i finans.</span><span class="sxs-lookup"><span data-stu-id="17311-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="17311-118">Kombinerte poster er ikke mulig.</span><span class="sxs-lookup"><span data-stu-id="17311-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="17311-119">Se også</span><span class="sxs-lookup"><span data-stu-id="17311-119">See Also</span></span>  
 <span data-ttu-id="17311-120">[Overføre og bokføre kostposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="17311-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="17311-121">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="17311-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
