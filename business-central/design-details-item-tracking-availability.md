---
title: "Designdetaljer – Varesporingstilgjengelighet | Microsoft-dokumentasjon"
description: "Sidene Varesporingslinjer og Varesporingssummering inneholder dynamisk tilgjengelighetsinformasjon for serie- eller partinumre. Hensikten med dette er å gjøre utgående dokumenter, for eksempel ordrer, klarere for brukere ved å vise dem serienumrene eller antallet partinumre som for øyeblikket er tilordnet i andre åpne dokumenter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/15/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: bbdda4378b20a50ef159f68c311fd49e68071504
ms.contentlocale: nb-no
ms.lasthandoff: 01/22/2019

---
# <a name="design-details-item-tracking-availability"></a><span data-ttu-id="baf7d-104">Designdetaljer: Varesporingstilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="baf7d-104">Design Details: Item Tracking Availability</span></span>
<span data-ttu-id="baf7d-105">Sidene **Varesporingslinjer** og **Varesporingssummering** inneholder dynamisk tilgjengelighetsinformasjon for serie- eller partinumre.</span><span class="sxs-lookup"><span data-stu-id="baf7d-105">The **Item Tracking Lines** and **Item Tracking Summary** pages provide dynamic availability information for serial or lot numbers.</span></span> <span data-ttu-id="baf7d-106">Hensikten med dette er å gjøre utgående dokumenter, for eksempel ordrer, klarere for brukere ved å vise dem serienumrene eller antallet partinumre som for øyeblikket er tilordnet i andre åpne dokumenter.</span><span class="sxs-lookup"><span data-stu-id="baf7d-106">The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.</span></span> <span data-ttu-id="baf7d-107">Dette reduserer usikkerhet som skyldes doble tildelinger og vekker tillit hos ordrebehandlere om at varesporingsnumrene og datoene de bekrefter på ikke-bokførte ordrer, kan oppfylles.</span><span class="sxs-lookup"><span data-stu-id="baf7d-107">This reduces uncertainty that is caused by double allocation and instills confidence in order processors that the item tracking numbers and dates that they are promising on unposted sales orders can be fulfilled.</span></span> <span data-ttu-id="baf7d-108">Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Side for varesporingslinjer](design-details-item-tracking-lines-window.md).</span><span class="sxs-lookup"><span data-stu-id="baf7d-108">For more information, see [Design Details: Item Tracking Lines Page](design-details-item-tracking-lines-window.md).</span></span>  

 <span data-ttu-id="baf7d-109">Når du åpner siden **Varesporingslinjer**, hentes tilgjengelighetsdata fra **Varepost**-tabellen og **Reservasjonspost**-tabellen uten noe datofilter.</span><span class="sxs-lookup"><span data-stu-id="baf7d-109">When you open the **Item Tracking Lines** page, availability data is retrieved from the **Item Ledger Entry** table and the **Reservation Entry** table, with no date filter.</span></span> <span data-ttu-id="baf7d-110">Når du velger **Serienr.**-feltet eller **Partinr.**-feltet, åpnes siden **Varesporingssummering** med et sammendrag av varesporingsinformasjonen i **Reservasjonspost**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="baf7d-110">When you choose the **Serial No.** field or the **Lot No.** field, the **Item Tracking Summary** page opens and shows a summary of the item tracking information in the **Reservation Entry** table.</span></span> <span data-ttu-id="baf7d-111">Sammendraget inneholder følgende informasjon om hvert serie- eller partinummer på varesporingslinjen:</span><span class="sxs-lookup"><span data-stu-id="baf7d-111">The summary contains the following information about each serial or lot number on the item tracking line:</span></span>  

|<span data-ttu-id="baf7d-112">Felt</span><span class="sxs-lookup"><span data-stu-id="baf7d-112">Field</span></span>|<span data-ttu-id="baf7d-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="baf7d-113">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="baf7d-114">**Antall i alt**</span><span class="sxs-lookup"><span data-stu-id="baf7d-114">**Total Quantity**</span></span>|<span data-ttu-id="baf7d-115">Det totale antallet for serie- eller partinummeret som for øyeblikket er på lager.</span><span class="sxs-lookup"><span data-stu-id="baf7d-115">The total quantity of the serial or lot number that is currently in inventory.</span></span>|  
|<span data-ttu-id="baf7d-116">**Ønsket antall i alt**</span><span class="sxs-lookup"><span data-stu-id="baf7d-116">**Total Requested Quantity**</span></span>|<span data-ttu-id="baf7d-117">Det totale antallet for serie- eller partinummeret som for øyeblikket er forespurt i alle dokumenter.</span><span class="sxs-lookup"><span data-stu-id="baf7d-117">The total quantity of the serial or lot number that is currently requested in all documents.</span></span>|  
|<span data-ttu-id="baf7d-118">**Gjeldende antall i kø**</span><span class="sxs-lookup"><span data-stu-id="baf7d-118">**Current Pending Quantity**</span></span>|<span data-ttu-id="baf7d-119">Antallet som registreres i gjeldende forekomst av siden **Varesporingslinjer**, men som ikke er lagret i databasen ennå.</span><span class="sxs-lookup"><span data-stu-id="baf7d-119">The quantity that is entered in the current instance of the **Item Tracking Lines** page but is not yet committed to the database.</span></span>|  
|<span data-ttu-id="baf7d-120">**Totalt disp. antall**</span><span class="sxs-lookup"><span data-stu-id="baf7d-120">**Total Available Quantity**</span></span>|<span data-ttu-id="baf7d-121">Antallet for serie- eller partinummeret som brukeren kan be om.</span><span class="sxs-lookup"><span data-stu-id="baf7d-121">The quantity of the serial or lot number that is available for the user to request.</span></span><br /><br /> <span data-ttu-id="baf7d-122">Dette antallet blir beregnet fra andre felt på siden, slik:</span><span class="sxs-lookup"><span data-stu-id="baf7d-122">This quantity is calculated from other fields on the page as follows:</span></span><br /><br /> <span data-ttu-id="baf7d-123">totalt antall – (ønsket antall i alt + gjeldende antall i kø).</span><span class="sxs-lookup"><span data-stu-id="baf7d-123">total quantity – (total requested quantity + current pending quantity).</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="baf7d-124">Du kan også vise informasjonen i den foregående tabellen ved å bruke funksjonen **Velg poster** på siden **Varesporingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="baf7d-124">You can also see the information in the preceding table by using the **Select Entries** function on the **Item Tracking Lines** page.</span></span>  

 <span data-ttu-id="baf7d-125">For å bevare databaseytelsen hentes tilgjengelighetsdata bare én gang fra databasen når du åpner siden **Varesporingslinjer** og når du bruker funksjonen **Oppdater tilgjengelighet** på siden.</span><span class="sxs-lookup"><span data-stu-id="baf7d-125">To preserve database performance, availability data is only retrieved once from the database when you open the **Item Tracking Lines** page and when you use the **Refresh Availability** function on the page.</span></span>  

## <a name="calculation-formula"></a><span data-ttu-id="baf7d-126">Beregningsformel</span><span class="sxs-lookup"><span data-stu-id="baf7d-126">Calculation Formula</span></span>  
 <span data-ttu-id="baf7d-127">Tilgjengeligheten av et bestemt serie- eller partinummer beregnes på følgende måte, som beskrevet i den forrige tabellen.</span><span class="sxs-lookup"><span data-stu-id="baf7d-127">As described in the preceding table, the availability of a given serial or lot number is calculated as follows.</span></span>  

 <span data-ttu-id="baf7d-128">totalt disponibelt antall = antallet på lager – (alle behov + antallet som ennå ikke er lagret i databasen)</span><span class="sxs-lookup"><span data-stu-id="baf7d-128">total available quantity = quantity in inventory – (all demands + quantity not yet committed to the database)</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="baf7d-129">Denne formelen innebærer at tilgjengelighetsberegningen for serie- eller partinumre bare tar hensyn til beholdning og ignorerer forventede mottak.</span><span class="sxs-lookup"><span data-stu-id="baf7d-129">This formula implies that the serial or lot number availability calculation considers only inventory and ignores projected receipts.</span></span> <span data-ttu-id="baf7d-130">Levering som ennå ikke er bokført på lager, påvirker derfor ikke varesporingstilgjengelighet, i motsetning til vanlig varedisposisjon der forventede mottak er inkludert.</span><span class="sxs-lookup"><span data-stu-id="baf7d-130">Accordingly, supply that is not yet posted to inventory does not affect item tracking availability, as opposed to regular item availability where projected receipts are included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="baf7d-131">Se også</span><span class="sxs-lookup"><span data-stu-id="baf7d-131">See Also</span></span>  
 [<span data-ttu-id="baf7d-132">Designdetaljer: Varesporing</span><span class="sxs-lookup"><span data-stu-id="baf7d-132">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)

