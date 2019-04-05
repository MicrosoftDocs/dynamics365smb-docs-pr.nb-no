---
title: Designdetaljer – Varesporing | Microsoft-dokumentasjon
description: Dette emnet gir en oversikt over designdetaljene for varesporing.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/12/2018
ms.author: sgroespe
ms.openlocfilehash: 1dce0ea658a2083c3d896fe6324751f63aabce06
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802587"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="dc33f-103">Designdetaljer: Varesporing</span><span class="sxs-lookup"><span data-stu-id="dc33f-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="dc33f-104">Etter hvert som flyt av varer i dagens forsyningskjede blir mer og mer komplisert, er muligheten til å holde oversikt over varer stadig viktigere for involverte selskaper.</span><span class="sxs-lookup"><span data-stu-id="dc33f-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="dc33f-105">Overvåking av en vares transaksjonsflyt er et juridisk krav i bransjer for medisinske og kjemiske produkter, men andre bedrifter vil kanskje også overvåke produkter med garantier eller utløpsdatoer av med hensyn til kundeservice.</span><span class="sxs-lookup"><span data-stu-id="dc33f-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="dc33f-106">Et varesporingssystem skal gi et selskap enkel håndtering av serie- og partinumre, og vurdering av hver unike vare: når og hvor mottatt, lagerplassering, når og hvor solgt.</span><span class="sxs-lookup"><span data-stu-id="dc33f-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="dc33f-107">har gradvis utvidet sin dekning av dette forretningsbehovet, og inneholder i dag generelle funksjoner og en solid kjerne som danner grunnlaget for utvikling av utvidelser.</span><span class="sxs-lookup"><span data-stu-id="dc33f-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="dc33f-108">I denne delen</span><span class="sxs-lookup"><span data-stu-id="dc33f-108">In This Section</span></span>  
[<span data-ttu-id="dc33f-109">Designdetaljer: Varesporingsutforming</span><span class="sxs-lookup"><span data-stu-id="dc33f-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="dc33f-110">Designdetaljer: Bokføringsstruktur for varesporing</span><span class="sxs-lookup"><span data-stu-id="dc33f-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="dc33f-111">Designdetaljer: Aktive kontra historiske varesporingsposter</span><span class="sxs-lookup"><span data-stu-id="dc33f-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="dc33f-112">Designdetaljer: Side for varesporingslinjer</span><span class="sxs-lookup"><span data-stu-id="dc33f-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="dc33f-113">Designdetaljer: Varesporingstilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="dc33f-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="dc33f-114">Designdetaljer: Varesporing og planlegging</span><span class="sxs-lookup"><span data-stu-id="dc33f-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="dc33f-115">Designdetaljer: Varesporing og reservasjoner</span><span class="sxs-lookup"><span data-stu-id="dc33f-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="dc33f-116">Designdetaljer: Varesporing på lageret</span><span class="sxs-lookup"><span data-stu-id="dc33f-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)
