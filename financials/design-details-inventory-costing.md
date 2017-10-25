---
title: "Designdetaljer – Kostberegning for beholdning | Microsoft-dokumentasjon"
description: Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i [!INCLUDE[d365fin](includes/d365fin_md.md)].
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 38a37a6fb1e3b8a58fd28b3d8e678b93a110683b
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="d085e-103">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="d085e-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="d085e-104">Denne dokumentasjonen gir et detaljert teknisk innblikk i begrepene og prinsippene som brukes i funksjonene for kostberegning for beholdning i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d085e-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d085e-105">Kostberegning for beholdning, også kalt kostnadsstyring, handler om å registrere og rapportere forretningsdriftskost.</span><span class="sxs-lookup"><span data-stu-id="d085e-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="d085e-106">I denne delen</span><span class="sxs-lookup"><span data-stu-id="d085e-106">In This Section</span></span>  
[<span data-ttu-id="d085e-107">Designdetaljer: Kostmetoder</span><span class="sxs-lookup"><span data-stu-id="d085e-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="d085e-108">Designdetaljer: Vareutligning</span><span class="sxs-lookup"><span data-stu-id="d085e-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="d085e-109">Designdetaljer: Kostjustering</span><span class="sxs-lookup"><span data-stu-id="d085e-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="d085e-110">Designdetaljer: Bokføre forventet kost</span><span class="sxs-lookup"><span data-stu-id="d085e-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="d085e-111">Designdetaljer: Gjennomsnittskost</span><span class="sxs-lookup"><span data-stu-id="d085e-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="d085e-112">Designdetaljer: Avvik</span><span class="sxs-lookup"><span data-stu-id="d085e-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="d085e-113">Designdetaljer: Avrunding</span><span class="sxs-lookup"><span data-stu-id="d085e-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="d085e-114">Designdetaljer: Kostkomponenter</span><span class="sxs-lookup"><span data-stu-id="d085e-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="d085e-115">Designdetaljer: Beholdningsperioder</span><span class="sxs-lookup"><span data-stu-id="d085e-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="d085e-116">Designdetaljer: Lagerbokføring</span><span class="sxs-lookup"><span data-stu-id="d085e-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="d085e-117">Designdetaljer: Bokføre produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="d085e-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="d085e-118">Designdetaljer: Bokføre monteringsordre</span><span class="sxs-lookup"><span data-stu-id="d085e-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="d085e-119">Designdetaljer: Avstemming med konti i Finans</span><span class="sxs-lookup"><span data-stu-id="d085e-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="d085e-120">Designdetaljer: Konti i Finans</span><span class="sxs-lookup"><span data-stu-id="d085e-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="d085e-121">Designdetaljer: Revaluering</span><span class="sxs-lookup"><span data-stu-id="d085e-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

