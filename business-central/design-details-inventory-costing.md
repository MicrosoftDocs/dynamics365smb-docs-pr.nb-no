---
title: Designdetaljer – Kostberegning for beholdning | Microsoft-dokumentasjon
description: Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 97aa9dc23397403b74fc8f1c65d302733ab3301c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751483"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="0c08d-103">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="0c08d-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="0c08d-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0c08d-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="0c08d-105">Kostberegning for beholdning, også kalt kostnadsstyring, handler om å registrere og rapportere forretningsdriftskost.</span><span class="sxs-lookup"><span data-stu-id="0c08d-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0c08d-106">I denne delen</span><span class="sxs-lookup"><span data-stu-id="0c08d-106">In This Section</span></span>  
[<span data-ttu-id="0c08d-107">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="0c08d-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="0c08d-108">Designdetaljer: Vareutligning</span><span class="sxs-lookup"><span data-stu-id="0c08d-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="0c08d-109">Designdetaljer: Kjent vareutligningsproblem</span><span class="sxs-lookup"><span data-stu-id="0c08d-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="0c08d-110">Designdetaljer: Kostjustering</span><span class="sxs-lookup"><span data-stu-id="0c08d-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="0c08d-111">Designdetaljer: Bokføringsdato på verdiposten for justering</span><span class="sxs-lookup"><span data-stu-id="0c08d-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="0c08d-112">Designdetaljer: Bokføre forventet kost</span><span class="sxs-lookup"><span data-stu-id="0c08d-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="0c08d-113">Designdetaljer: Gjennomsnittskost</span><span class="sxs-lookup"><span data-stu-id="0c08d-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="0c08d-114">Designdetaljer: Avvik</span><span class="sxs-lookup"><span data-stu-id="0c08d-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="0c08d-115">Designdetaljer: Avrunding</span><span class="sxs-lookup"><span data-stu-id="0c08d-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="0c08d-116">Designdetaljer: Kostkomponenter</span><span class="sxs-lookup"><span data-stu-id="0c08d-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="0c08d-117">Designdetaljer: Beholdningsperioder</span><span class="sxs-lookup"><span data-stu-id="0c08d-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="0c08d-118">Designdetaljer: Lagerbokføring</span><span class="sxs-lookup"><span data-stu-id="0c08d-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="0c08d-119">Designdetaljer: Bokføre produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="0c08d-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="0c08d-120">Designdetaljer: Bokføre monteringsordre</span><span class="sxs-lookup"><span data-stu-id="0c08d-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="0c08d-121">Designdetaljer: Avstemming med konti i Finans</span><span class="sxs-lookup"><span data-stu-id="0c08d-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="0c08d-122">Designdetaljer: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="0c08d-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="0c08d-123">Designdetaljer: Lagerverdisetting</span><span class="sxs-lookup"><span data-stu-id="0c08d-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="0c08d-124">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="0c08d-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
