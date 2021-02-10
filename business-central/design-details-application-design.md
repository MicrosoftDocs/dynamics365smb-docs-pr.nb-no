---
title: Designdetaljer | Microsoft-dokumentasjon
description: Dette innholdet omfatter detaljert teknisk informasjon om komplekse programfunksjoner i Business Central.
author: SorenGP
documentationcenter: ''
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a2280fbeccd51d1c959aa2aa09121d728a18326f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751858"
---
# <a name="design-details"></a><span data-ttu-id="58f05-103">Designdetaljer</span><span class="sxs-lookup"><span data-stu-id="58f05-103">Design Details</span></span>
<span data-ttu-id="58f05-104">Dette innholdet omfatter detaljert teknisk informasjon om komplekse programfunksjoner i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="58f05-104">This content contains detailed technical information about complex application features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

 <span data-ttu-id="58f05-105">Innhold i designdetaljer er rettet mot implementerere, utviklere og superbrukere som trenger større innsikt for å implementere, tilpasse eller konfigurere den aktuelle funksjonen.</span><span class="sxs-lookup"><span data-stu-id="58f05-105">Design details content is aimed at implementers, developers, and super users who need deeper insight to implement, customize, or set up the features in question.</span></span>  

|<span data-ttu-id="58f05-106">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="58f05-106">**To**</span></span>|<span data-ttu-id="58f05-107">**Se**</span><span class="sxs-lookup"><span data-stu-id="58f05-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="58f05-108">Lær hvordan planleggingssystemet fungerer og hvordan du justerer algoritmene for å oppfylle krav i forskjellige miljøer.</span><span class="sxs-lookup"><span data-stu-id="58f05-108">Learn how the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="58f05-109">Designdetaljer: Forsyningsplanlegging</span><span class="sxs-lookup"><span data-stu-id="58f05-109">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|  
|<span data-ttu-id="58f05-110">Forstå mekanismene i kostmotoren, for eksempel lagermetode og kostjustering, og hvilke regnskapsprinsipper de er utformet for.</span><span class="sxs-lookup"><span data-stu-id="58f05-110">Understand mechanisms in the costing engine, such as costing method and cost adjustment, and which accounting principles they are designed for.</span></span>|[<span data-ttu-id="58f05-111">Designdetaljer: Kostberegning for beholdning</span><span class="sxs-lookup"><span data-stu-id="58f05-111">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  
|<span data-ttu-id="58f05-112">Lær mer om sentrale prinsipper bak avanserte og grunnleggende lagerfunksjoner og hvordan de integreres med andre forsyningskjedefunksjoner.</span><span class="sxs-lookup"><span data-stu-id="58f05-112">Learn about central principles behind advanced and basic warehouse features and how they integrate with other supply chain features.</span></span>|[<span data-ttu-id="58f05-113">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="58f05-113">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)|  
|<span data-ttu-id="58f05-114">Lær mer om historisk og gjeldende utformingen av varesporingsfunksjonalitet og hvordan den integreres med reservasjonssystemet, slik at serie-/partinumre inkluderes i tilgjengelighetsberegninger.</span><span class="sxs-lookup"><span data-stu-id="58f05-114">Learn about historic and the current design of item tracking functionality and how it integrates with the reservation system to include serial/lot numbers in availability calculations.</span></span>|[<span data-ttu-id="58f05-115">Designdetaljer: Varesporing</span><span class="sxs-lookup"><span data-stu-id="58f05-115">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)|  
|<span data-ttu-id="58f05-116">Finn ut mer om funksjonen for bokføring av finanskladdelinje, inkludert nye forenklinger i utformingen av kodeenhet 12.</span><span class="sxs-lookup"><span data-stu-id="58f05-116">Learn about the General Journal Posting Line feature, including recent simplifications to the design of codeunit 12.</span></span>|[<span data-ttu-id="58f05-117">Designdetaljer: Finanskladd – bokfør linje</span><span class="sxs-lookup"><span data-stu-id="58f05-117">Design Details: General Journal Post Line</span></span>](design-details-general-journal-post-line.md)|
|<span data-ttu-id="58f05-118">Finn ut mer om utformingen for lagring og bokføring av dimensjoner, inkludert kodeeksempler på hvordan du kan flytte og oppgradere dimensjonskode.</span><span class="sxs-lookup"><span data-stu-id="58f05-118">Learn about the design for storing and posting dimensions, including code examples on how to migrate and upgrade dimension code.</span></span>|[<span data-ttu-id="58f05-119">Designdetaljer: Dimensjonssettposter</span><span class="sxs-lookup"><span data-stu-id="58f05-119">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)| 

## <a name="see-also"></a><span data-ttu-id="58f05-120">Se også</span><span class="sxs-lookup"><span data-stu-id="58f05-120">See Also</span></span>  
 <span data-ttu-id="58f05-121">[Planlegging](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="58f05-121">[Planning](production-planning.md) </span></span>  
 <span data-ttu-id="58f05-122">[Administrere lagerkostnader](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="58f05-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="58f05-123">[Lagerstyring](warehouse-manage-warehouse.md) </span><span class="sxs-lookup"><span data-stu-id="58f05-123">[Warehouse Management](warehouse-manage-warehouse.md) </span></span>  
 [<span data-ttu-id="58f05-124">Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="58f05-124">Setting Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="58f05-125">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58f05-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>

 ## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
