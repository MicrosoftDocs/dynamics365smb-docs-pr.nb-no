---
title: Designdetaljer – Kostberegning for beholdning | Microsoft-dokumentasjon
description: Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8bfcf2b10d9b302c9a65b7cf27c7fb336be68617
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215981"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="27b10-103">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="27b10-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="27b10-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="27b10-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="27b10-105">Kostberegning for beholdning, også kalt kostnadsstyring, handler om å registrere og rapportere forretningsdriftskost.</span><span class="sxs-lookup"><span data-stu-id="27b10-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="27b10-106">I denne delen</span><span class="sxs-lookup"><span data-stu-id="27b10-106">In This Section</span></span>  
[<span data-ttu-id="27b10-107">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="27b10-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="27b10-108">Designdetaljer: Vareutligning</span><span class="sxs-lookup"><span data-stu-id="27b10-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="27b10-109">Designdetaljer: Kjent vareutligningsproblem</span><span class="sxs-lookup"><span data-stu-id="27b10-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="27b10-110">Designdetaljer: Kostjustering</span><span class="sxs-lookup"><span data-stu-id="27b10-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="27b10-111">Designdetaljer: Bokføringsdato på verdiposten for justering</span><span class="sxs-lookup"><span data-stu-id="27b10-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="27b10-112">Designdetaljer: Bokføre forventet kost</span><span class="sxs-lookup"><span data-stu-id="27b10-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="27b10-113">Designdetaljer: Gjennomsnittskost</span><span class="sxs-lookup"><span data-stu-id="27b10-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="27b10-114">Designdetaljer: Avvik</span><span class="sxs-lookup"><span data-stu-id="27b10-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="27b10-115">Designdetaljer: Avrunding</span><span class="sxs-lookup"><span data-stu-id="27b10-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="27b10-116">Designdetaljer: Kostkomponenter</span><span class="sxs-lookup"><span data-stu-id="27b10-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="27b10-117">Designdetaljer: Beholdningsperioder</span><span class="sxs-lookup"><span data-stu-id="27b10-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="27b10-118">Designdetaljer: Lagerbokføring</span><span class="sxs-lookup"><span data-stu-id="27b10-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="27b10-119">Designdetaljer: Bokføre produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="27b10-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="27b10-120">Designdetaljer: Bokføre monteringsordre</span><span class="sxs-lookup"><span data-stu-id="27b10-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="27b10-121">Designdetaljer: Avstemming med konti i Finans</span><span class="sxs-lookup"><span data-stu-id="27b10-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="27b10-122">Designdetaljer: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="27b10-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="27b10-123">Designdetaljer: Lagerverdisetting</span><span class="sxs-lookup"><span data-stu-id="27b10-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="27b10-124">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="27b10-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]