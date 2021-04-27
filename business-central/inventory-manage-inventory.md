---
title: Håndtere lager | Microsoft-dokumentasjon
description: Beskriver hvordan du håndterer de fysiske produktene du handler med, for eksempel håndtering av varene på lageret.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f72ef570151babaa9bf32150c214e82374ddd0ec
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780760"
---
# <a name="inventory"></a>Lager
Du må opprette et varekort av typen **Lager** for hvert fysiske produkt du handler i. Varer du tilbyr til kunder, men ikke har på lager, kan du registrere som katalogvarer, som du kan konvertere til lagervarer når det er nødvendig. Du kan øke eller redusere antall varer på lager ved å bokføre direkte til varepostene, for eksempel etter en fysisk opptelling eller hvis du ikke registrerer kjøp.

Lagerøkning og -reduksjon registreres også når du bokfører henholdsvis salgs- og kjøpsdokumenter. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md), [Selge produkter](sales-how-sell-products.md) og [Fakturere salg](sales-how-invoice-sales.md). Overføringer mellom lokasjoner endrer lagerantallene på tvers av selskapets lagere.   

Hvis du vil ha bedre oversikt over varene og hjelp til å finne dem, kan du kategorisere varene og gi dem attributter til å søke og sortere etter.

> [!NOTE]
> Den fysiske håndteringen av varer kalles lageraktiviteter. Hvis du vil ha mer informasjon, se [Lagerstyring](warehouse-manage-warehouse.md).

Planlegging for varer for å oppfylle behovet dekkes som en del av funksjonaliteten for forsyningsplanlegging. Hvis du vil ha mer informasjon , kan du se [Planlegging](production-planning.md).  

## <a name="inventory-reconciliation"></a>Lageravstemming
Når du bokfører lagertransaksjoner, for eksempel følgesedler, kjøpsfakturaer eller lagerjusteringer, registreres endringene i varekostnader i vareverdipostene. For å gjenspeile endringen i lagerverdien i regnskapet, blir lagerkost automatisk bokført til de relaterte lagerkontoene i Finans. For hver lagertransaksjon du bokfører, bokføres de aktuelle verdiene i lagerkontoen, justeringskontoen og vareforbrukskontoen i Finans. Hvis du vil ha mer informasjon, kan du se [Avstemme lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selv om lagerkost bokføres automatisk til finans, er det fortsatt nødvendig å sikre at kostbeløpene for varer videresendes til de relaterte utgående salgstransaksjonene. Dette er særlig viktig i situasjoner der du selger varer før du fakturerer kjøpet av varene. Dette kalles kostjustering. Varekostnader justeres automatisk når du bokfører varetransaksjoner, men du kan også justere varekostnader manuelt. Hvis du vil ha mer informasjon, kan du se [Justere varekost](inventory-how-adjust-item-costs.md).  

## <a name="related-tasks"></a>Beslektede oppgaver

Tabellen nedenfor beskriver beslektede oppgaver.

|Hvis du vil |Se |
|---|----|
|Opprett varekort for lagervarer som du handler med.|[Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.|[Arbeide med stykklister](inventory-how-work-BOMs.md)|
|Hold oversikt over varer og gjør det enklere å finne og sortere varer ved å ordne dem i kategorier.|[Kategorisere varer](inventory-how-categorize-items.md)|
|Tilordne vareattributter av ulike verdityper til varene, for å gjøre det enklere for deg å sortere og finne varer.|[Arbeide med vareattributter](inventory-how-work-item-attributes.md)|
|Opprett spesielle varekort for varer som du tilbyr til kunder, men som du ikke har på lager.|[Arbeide med katalogvarer](inventory-how-work-nonstock-items.md)|
|Utfør fysisk lagertelling med sidene **Vareopptellingsordre** og **Registrering for vareopptelling**.|[Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md)|
|Du kan utføre fysisk telling, foreta negative eller positive justeringer og endre informasjon, for eksempel lokasjons- eller partinummer, i vareposter.|[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)|
|Vis tilgjengeligheten av varer per lokasjon, etter periode, ved salg eller kjøpshendelse eller ved bruk på monterings- eller produksjonsstykklister.|[Vise tilgjengeligheten av varer](inventory-how-availability-overview.md)|
|Overføre varer mellom lokasjoner med overføringsordrer for å administrere lageraktiviteter, eller med varereklassifiseringskladden.|[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)|
|Reserver lagervarer eller inngående varer for ordrer, bestillinger, serviceordrer, monteringsordrer eller produksjonsordrer.|[Reservere varer](inventory-how-to-reserve-items.md)|
|Tilordne serie- eller partinumre til en utgående eller inngående bilags- eller kladdelinje, for eksempel for å spore varer i tilfelle tilbakekallinger.|[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)|
|Sett opp en leverandørs egen beskrivelse av en vare på varekortet, slik at du raskt kan sette inn varebeskrivelser på handelsdokumenter.|[Bruke varekryssreferanser](inventory-how-use-item-cross-refs.md)|
|Finn ut hvor eventuelle serie- eller partinummer ble brukt i dets forsyningskjede, for eksempel i tilbakekallingssituasjoner.|[Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)|
|Blokker varer fra å bli lagt inn på salgs- eller bestillingslinjene eller fra å bli bokført i en transaksjon.|[Blokker varer](inventory-how-block-items.md)|
|Håndter forretningsdriften i salgskontorer, innkjøpsavdelinger eller anleggsplanleggingskontorer på tvers av flere lokasjoner.|[Arbeide med ansvarssentre](inventory-responsibility-centers.md)|
|Bruk ressurser med bestemte ferdigheter for forskjellige tjenester og servicevarer.|[Definere ressurstildeling](service-how-setup-resource-allocation.md)|

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]