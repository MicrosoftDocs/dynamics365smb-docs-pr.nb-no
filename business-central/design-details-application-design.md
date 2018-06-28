---
title: Designdetaljer | Microsoft-dokumentasjon
description: Dette innholdet omfatter detaljert teknisk informasjon om komplekse programfunksjoner i Business Central.
author: SorenGP
documentationcenter: 
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 8397edc9454adcd8e619d8f43cd81b6a2c058d99
ms.contentlocale: nb-no
ms.lasthandoff: 06/28/2018

---
# <a name="design-details"></a><span data-ttu-id="6cd65-103">Designdetaljer</span><span class="sxs-lookup"><span data-stu-id="6cd65-103">Design Details</span></span>
<span data-ttu-id="6cd65-104">Dette innholdet omfatter detaljert teknisk informasjon om komplekse programfunksjoner i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6cd65-104">This content contains detailed technical information about complex application features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

 <span data-ttu-id="6cd65-105">Innhold i designdetaljer er rettet mot implementerere, utviklere og superbrukere som trenger større innsikt for å implementere, tilpasse eller konfigurere den aktuelle funksjonen.</span><span class="sxs-lookup"><span data-stu-id="6cd65-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="6cd65-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="6cd65-106">**To**</span></span>|<span data-ttu-id="6cd65-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="6cd65-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="6cd65-108">Finn ut mer om utformingen for lagring og bokføring av dimensjoner, inkludert kodeeksempler på hvordan du kan flytte og oppgradere dimensjonskode.</span><span class="sxs-lookup"><span data-stu-id="6cd65-108">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="6cd65-109">Designdetaljer: Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="6cd65-109">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)|  
|<span data-ttu-id="6cd65-110">Lær hvordan planleggingssystemet fungerer og hvordan du justerer algoritmene for å oppfylle krav i forskjellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="6cd65-110">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="6cd65-111">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="6cd65-111">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="6cd65-112">Forstå mekanismene i kostmotoren, for eksempel lagermetode og kostjustering, og hvilke regnskapsprinsipper de er utformet for.</span><span class="sxs-lookup"><span data-stu-id="6cd65-112">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="6cd65-113">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="6cd65-113">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="6cd65-114">Lær mer om sentrale prinsipper bak avanserte og grunnleggende lagerfunksjoner og hvordan de integreres med andre forsyningskjedefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="6cd65-114">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="6cd65-115">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="6cd65-115">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="6cd65-116">Lær mer om historisk og gjeldende utformingen av varesporingsfunksjonalitet og hvordan den integreres med reservasjonssystemet, slik at serie-/partinumre inkluderes i tilgjengelighetsberegninger.</span><span class="sxs-lookup"><span data-stu-id="6cd65-116">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="6cd65-117">Designdetaljer: Varesporing</span><span class="sxs-lookup"><span data-stu-id="6cd65-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="6cd65-118">Finn ut mer om funksjonen for bokføring av finanskladdelinje, inkludert nye forenklinger i utformingen av kodeenhet 12.</span><span class="sxs-lookup"><span data-stu-id="6cd65-118">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="6cd65-119">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="6cd65-119">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|  

## <a name="see-also"></a><span data-ttu-id="6cd65-120">Se også</span><span class="sxs-lookup"><span data-stu-id="6cd65-120">See Also</span></span>  
 <span data-ttu-id="6cd65-121">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="6cd65-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="6cd65-122">[Administrere lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="6cd65-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="6cd65-123">[Lagerstyring](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="6cd65-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="6cd65-124">Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="6cd65-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="6cd65-125">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6cd65-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
  

