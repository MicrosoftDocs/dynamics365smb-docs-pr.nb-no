---
title: "Designdetaljer – Kostberegning for beholdning | Microsoft-dokumentasjon"
description: Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 2ee8988a89e4bd01683a6945e66e08ab9608af2e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="d8bf3-103">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="d8bf3-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="d8bf3-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d8bf3-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d8bf3-105">Kostberegning for beholdning, også kalt kostnadsstyring, handler om å registrere og rapportere forretningsdriftskost.</span><span class="sxs-lookup"><span data-stu-id="d8bf3-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d8bf3-106">I denne delen</span><span class="sxs-lookup"><span data-stu-id="d8bf3-106">In This Section</span></span>  
[<span data-ttu-id="d8bf3-107">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="d8bf3-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="d8bf3-108">Designdetaljer: Vareutligning</span><span class="sxs-lookup"><span data-stu-id="d8bf3-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="d8bf3-109">Designdetaljer: Kjent vareutligningsproblem</span><span class="sxs-lookup"><span data-stu-id="d8bf3-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="d8bf3-110">Designdetaljer: Kostjustering</span><span class="sxs-lookup"><span data-stu-id="d8bf3-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="d8bf3-111">Designdetaljer: Bokføringsdato på verdiposten for justering</span><span class="sxs-lookup"><span data-stu-id="d8bf3-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="d8bf3-112">Designdetaljer: Bokføre forventet kost</span><span class="sxs-lookup"><span data-stu-id="d8bf3-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="d8bf3-113">Designdetaljer: Gjennomsnittskost</span><span class="sxs-lookup"><span data-stu-id="d8bf3-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="d8bf3-114">Designdetaljer: Avvik</span><span class="sxs-lookup"><span data-stu-id="d8bf3-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="d8bf3-115">Designdetaljer: Avrunding</span><span class="sxs-lookup"><span data-stu-id="d8bf3-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="d8bf3-116">Designdetaljer: Kostkomponenter</span><span class="sxs-lookup"><span data-stu-id="d8bf3-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="d8bf3-117">Designdetaljer: Beholdningsperioder</span><span class="sxs-lookup"><span data-stu-id="d8bf3-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="d8bf3-118">Designdetaljer: Lagerbokføring</span><span class="sxs-lookup"><span data-stu-id="d8bf3-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="d8bf3-119">Designdetaljer: Bokføre produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="d8bf3-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="d8bf3-120">Designdetaljer: Bokføre monteringsordre</span><span class="sxs-lookup"><span data-stu-id="d8bf3-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="d8bf3-121">Designdetaljer: Avstemming med konti i Finans</span><span class="sxs-lookup"><span data-stu-id="d8bf3-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="d8bf3-122">Designdetaljer: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="d8bf3-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="d8bf3-123">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="d8bf3-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

