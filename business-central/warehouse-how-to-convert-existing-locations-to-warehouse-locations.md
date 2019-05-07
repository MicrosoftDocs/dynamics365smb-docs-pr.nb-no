---
title: Konvertere eksisterende lokasjoner til lagerlokasjoner | Microsoft-dokumentasjon
description: Du kan definere at en eksisterende lokasjon skal bruke soner og hyller, og at den skal fungere som en lagerlokasjon.
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
ms.openlocfilehash: 9996dce18755a48be903fabdfcb381a5d6ee5398
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2019
ms.locfileid: "939203"
---
# <a name="convert-existing-locations-to-warehouse-locations"></a><span data-ttu-id="56659-103">Konvertere eksisterende lokasjoner til lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="56659-103">Convert Existing Locations to Warehouse Locations</span></span>
<span data-ttu-id="56659-104">Du kan definere at en eksisterende lokasjon skal bruke soner og hyller, og at den skal fungere som en lagerlokasjon.</span><span class="sxs-lookup"><span data-stu-id="56659-104">You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.</span></span>  

<span data-ttu-id="56659-105">Kjørselen for å aktivere en lokasjon for lageroperasjoner oppretter startlagerposter for lagerjusteringshyllen for alle varer som har lager på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="56659-105">The batch job to enable a location for warehouse operation creates initial warehouse entries for the warehouse adjustment bin for all items that have inventory in the location.</span></span> <span data-ttu-id="56659-106">Disse startpostene balanseres når vareopptellingsposter for lageret registreres etter at kjørselen er utført.</span><span class="sxs-lookup"><span data-stu-id="56659-106">These initial entries will be balanced when warehouse physical inventory entries are entered after the batch job is run.</span></span>  

<span data-ttu-id="56659-107">Du kan opprette soner og hyller før eller etter konverteringen.</span><span class="sxs-lookup"><span data-stu-id="56659-107">You can create zones and bins either before or after the conversion.</span></span> <span data-ttu-id="56659-108">Den eneste hyllen du må opprette før konverteringen, er hyllen som skal brukes som fremtidig justeringshylle.</span><span class="sxs-lookup"><span data-stu-id="56659-108">The only bin that you must create before the conversion is the one that is to be used as the future adjustment bin.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="56659-109">Når du skal tømme all negativ beholdning og eventuelle åpne lagerdokumenter før du konverterer lokasjonen for lagerhåndtering, kjører du en rapport for å identifisere varene med negativ beholdning og åpne lagerdokumenter for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="56659-109">To clear all negative inventory and any open warehouse documents before you convert the location for warehouse handling, run a report to identify the items with negative inventory and open warehouse documents for the location.</span></span> <span data-ttu-id="56659-110">Du finner mer informasjon under Kontroll for negativ beholdning.</span><span class="sxs-lookup"><span data-stu-id="56659-110">For more information, see Check on Negative Inventory.</span></span>  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><span data-ttu-id="56659-111">Slik definerer du en eksisterende lokasjon som lagerlokasjon</span><span class="sxs-lookup"><span data-stu-id="56659-111">To enable an existing location to operate as a warehouse location</span></span>  
1.  <span data-ttu-id="56659-112">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett lagerlokasjon**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="56659-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Warehouse Location**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="56659-113">Angi lokasjonen du vil aktivere for lagerbehandling, i **Lokasjonskode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="56659-113">In the **Location Code** field, specify the location that you want to enable for warehouse processing.</span></span>  
3.  <span data-ttu-id="56659-114">Angi hyllen i lokasjonen der usynkroniserte lagerposter lagres, i feltet **Hyllekode for justering**.</span><span class="sxs-lookup"><span data-stu-id="56659-114">In the **Adjustment Bin Code** field, specify the bin at the location where unsynchronized warehouse entries are stored.</span></span> <span data-ttu-id="56659-115">Hvis du vil ha mer informasjon, kan du se [Slik synkroniserer du de justerte lagerpostene med de tilhørende varepostene](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).</span><span class="sxs-lookup"><span data-stu-id="56659-115">For more information, see the [To synchronize the adjusted warehouse entries with the related item ledger entries](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).</span></span>  

    <span data-ttu-id="56659-116">Når du bruker åpne vareposter for den angitte lokasjonen, opprettes det lagerkladdelinjer som summerer alle kombinasjoner av Varenr, Variantkode, Enhetskode og om nødvendig Partinr. og Serienr, i varepostene.</span><span class="sxs-lookup"><span data-stu-id="56659-116">Using the open item ledger entries for the specified location, warehouse journal lines are created that sum up every combination of Item No., Variant Code, Unit of Measure Code, and, if necessary, Lot No. and Serial No. in the item ledger entries.</span></span> <span data-ttu-id="56659-117">Lagerkladdelinjene blir deretter bokført.</span><span class="sxs-lookup"><span data-stu-id="56659-117">The warehouse journal lines are then posted.</span></span> <span data-ttu-id="56659-118">Under bokføringen opprettes det lagerposter som plasserer lageret i lagerjusteringshyllen.</span><span class="sxs-lookup"><span data-stu-id="56659-118">This posting creates warehouse entries that place the inventory in the warehouse adjustment bin.</span></span> <span data-ttu-id="56659-119">**Hyllekode for justering** på lokasjonskortet angis også.</span><span class="sxs-lookup"><span data-stu-id="56659-119">The **Adjustment Bin Code** on the location card is also set.</span></span>  

4.  <span data-ttu-id="56659-120">Hvis du vil se hvilke varer som ble lagt til i justeringshyllen under kjørselen, kan du kjøre rapporten **Lagerjustering - hylle**.</span><span class="sxs-lookup"><span data-stu-id="56659-120">To see which items were added to the adjustment bin during the batch job, run the **Warehouse Adjustment Bin** report.</span></span>  
5.  <span data-ttu-id="56659-121">Når den satsvise jobben **Opprett lagerlokasjon** er fullført, må du utføre og bokføre en vareopptelling for lageret.</span><span class="sxs-lookup"><span data-stu-id="56659-121">When the **Create Warehouse Location** batch job has completed, perform and post a warehouse physical inventory.</span></span> <span data-ttu-id="56659-122">Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)</span><span class="sxs-lookup"><span data-stu-id="56659-122">For more information, see [Count, Adjust, and Reclassify Inventory Using Journals](inventory-how-count-adjust-reclassify.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="56659-123">Det anbefales at du utfører kjørselen **Opprett lagerlokasjon** når den ikke påvirker den daglige driften i systemet.</span><span class="sxs-lookup"><span data-stu-id="56659-123">It is recommended that you run the **Create Warehouse Location** batch job at a time when it will not impact the daily work in the system.</span></span> <span data-ttu-id="56659-124">Kjørselen behandler hver post i tabellen **Varepost**, og hvis det finnes et stort antall vareposter, kan det hende jobben tar flere timer.</span><span class="sxs-lookup"><span data-stu-id="56659-124">This job processes each entry in the **Item Ledger Entry** table, and if there are a large number of item ledger entries, the job can last several hours.</span></span>  

 <span data-ttu-id="56659-125">Du må åpne på nytt og frigi eventuelle kildedokumenter som ble delvis mottatt eller delvis levert før konverteringen, for lokasjonene som ikke brukte lagerstyringsdokumenter før konverteringen.</span><span class="sxs-lookup"><span data-stu-id="56659-125">For those locations that did not use warehouse management documents before the conversion, you must re-open and release any source documents that were partially received or partially shipped before the conversion.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56659-126">Se også</span><span class="sxs-lookup"><span data-stu-id="56659-126">See Also</span></span>  
[<span data-ttu-id="56659-127">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="56659-127">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="56659-128">Lager</span><span class="sxs-lookup"><span data-stu-id="56659-128">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="56659-129">[Definere lagerstyring](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="56659-129">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="56659-130">[Monteringsstyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="56659-130">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="56659-131">Designdetaljer: Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="56659-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="56659-132">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56659-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
