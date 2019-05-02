---
title: Designdetaljer – Varesporing i lageret | Microsoft-dokumentasjon
description: Håndtering av serie- og partinumre er hovedsakelig en lageroppgave, og derfor har alle inngående og utgående lagerdokumenter standard funksjonalitet for tilordning og valg av varesporingsnumre. Siden reservasjonssystemet er basert på vareposter, blir imidlertid ikke lageraktivitetsdokumenter som registrerer bare lagerposter, støttet fullstendig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 01/15/2019
ms.author: sgroespe
ms.openlocfilehash: e780dba122374bd80e48ca6bbc74b7540e034ac6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802500"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="1af85-104">Designdetaljer: Varesporing på lageret</span><span class="sxs-lookup"><span data-stu-id="1af85-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="1af85-105">Håndtering av serie- og partinumre er hovedsakelig en lageroppgave, og derfor har alle inngående og utgående lagerdokumenter standard funksjonalitet for tilordning og valg av varesporingsnumre.</span><span class="sxs-lookup"><span data-stu-id="1af85-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="1af85-106">Siden reservasjonssystemet er basert på vareposter, blir imidlertid ikke lageraktivitetsdokumenter som registrerer bare lagerposter, støttet fullstendig.</span><span class="sxs-lookup"><span data-stu-id="1af85-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="1af85-107">Siden reservasjoner og varesporingsnumre bare kan behandles på lokasjonsnivå og ikke på hylle/ og sonenivå, kan ikke siden **Varesporingslinjer** åpnes fra lageraktivitetsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1af85-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="1af85-108">Det samme gjelder for **Reservasjon**-siden.</span><span class="sxs-lookup"><span data-stu-id="1af85-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="1af85-109">Etter at et serie- eller partinummer er lagt til en vare på lagerlokasjonen, kan de flyttes og omklassifiseres fritt i lageret ved hjelp av en uavhengig struktur for varesporings som ikke er relatert til reservasjonssystemet.</span><span class="sxs-lookup"><span data-stu-id="1af85-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="1af85-110">Du har direkte tilgang til feltene **Serienr.** og **Partinr.** på lagerdokumentlinjer.</span><span class="sxs-lookup"><span data-stu-id="1af85-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="1af85-111">Når serie- eller partinummeret senere er med i utgående bokføring, synkroniseres det med reservasjonssystemet som en del av vanlig hyllejustering.</span><span class="sxs-lookup"><span data-stu-id="1af85-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="1af85-112">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Integrasjon med lagerbeholdning](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="1af85-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="1af85-113">Reservasjonssystemet tar imidlertid hensyn til lageraktiviteter ved beregning av tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="1af85-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="1af85-114">Varer som for eksempel er tildelt plukkinger eller registrert som plukket, kan ikke reserveres.</span><span class="sxs-lookup"><span data-stu-id="1af85-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="1af85-115">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="1af85-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1af85-116">Se også</span><span class="sxs-lookup"><span data-stu-id="1af85-116">See Also</span></span>  
[<span data-ttu-id="1af85-117">Designdetaljer: Varesporing</span><span class="sxs-lookup"><span data-stu-id="1af85-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="1af85-118">Designdetaljer: Integrasjon med lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="1af85-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="1af85-119">Designdetaljer: Tilgjengelighet i lageret</span><span class="sxs-lookup"><span data-stu-id="1af85-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="1af85-120">Designdetaljer: Varesporingsutforming</span><span class="sxs-lookup"><span data-stu-id="1af85-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)