---
title: Håndtere lager
description: 'Denne artikkelen beskriver hvordan du administrerer de fysiske produktene du handler med, ved å opprette et lagervarekort.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.forms: '5804, 2106, 5823, 5751, 5750, 772, 5829, 5828, 513, 304, 40, 38, 167, 117, 5827, 9223, 158, 354, 9152, 286, 5754, 5402, 209, 297, 298, 99000782'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Håndter lager

Du må opprette et varekort av typen **Lager** for hvert fysiske produkt du handler i. Varer du tilbyr til kunder, men ikke har på lager, kan du registrere som katalogvarer, som du kan konvertere til lagervarer når det er nødvendig. Du kan øke eller redusere antall varer på lager ved å bokføre direkte til varepostene, for eksempel etter en fysisk opptelling eller hvis du ikke registrerer kjøp.

Lagerøkning og -reduksjon registreres også når du bokfører henholdsvis salgs- og kjøpsdokumenter. Finn ut mer under [Registrer kjøp](purchasing-how-record-purchases.md), [Selg produkter](sales-how-sell-products.md) og [Fakturer salg](sales-how-invoice-sales.md). Overføringer mellom lokasjoner endrer lagerantallene på tvers av selskapets lagre.

Hvis du vil ha bedre oversikt over varene og hjelp til å finne dem, kan du kategorisere varene og gi dem attributter til å søke og sortere etter.

> [!NOTE]
> Den fysiske håndteringen av varer kalles lageraktiviteter. Finn ut mer under [Oversikt over lagerstyring](design-details-warehouse-management.md).

Planlegging for varer for å oppfylle behovet dekkes som en del av funksjonaliteten for forsyningsplanlegging. Finn ut mer under [Planlegging](production-planning.md).  

## Lageranalyse

Denne delen beskriver analyseverktøyene du kan bruke til å få innsikt i lagerdata.

| Til ... | Se |
| --- | --- |
| Finn ut mer om muligheter for analyse av lagerdata. | [Oversikt over salgsanalyse](inventory-analytics-overview.md) |
| Utfør ad hoc-analyse av lagerdata direkte på listesider og spørringer. | [Ad hoc-analyse av lagerdata](ad-hoc-analysis-inventory.md) |
| Utforsk innebygde lagerrapporter. | [Innebygd beholdnings- og lagerrapporter](inventory-WMS-reports.md) |

## Lageravstemming

Når du bokfører lagertransaksjoner, for eksempel følgesedler, kjøpsfakturaer eller lagerjusteringer, registreres endringene i varekostnader i vareverdipostene. For å gjenspeile endringen i lagerverdien i regnskapet, blir lagerkost automatisk bokført til de relaterte lagerkontoene i Finans. For hver lagertransaksjon du bokfører, bokføres de aktuelle verdiene i lagerkontoen, justeringskontoen og vareforbrukskontoen i Finans. Finn ut mer under [Avstem lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selv om lagerkost bokføres automatisk til finans, er det fortsatt nødvendig å sikre at kostbeløpene for varer videresendes til de relaterte utgående salgstransaksjonene. Dette er særlig viktig i situasjoner der du selger varer før du fakturerer kjøpet av varene. Dette kalles kostjustering. Varekostnader justeres automatisk når du bokfører varetransaksjoner, men du kan også justere varekostnader manuelt. Finn ut mer under [Juster varekost](inventory-how-adjust-item-costs.md).  

## Beslektede oppgaver

Tabellen nedenfor beskriver beslektede oppgaver.

|Til |Se |
|---|----|
|Opprett varekort for lagervarer som du handler med.|[Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.|[Arbeide med stykklister](inventory-how-work-BOMs.md)|
|Hold oversikt over varer og gjør det enklere å finne og sortere varer ved å ordne dem i kategorier.|[Kategorisere varer](inventory-how-categorize-items.md)|
|Tilordne vareattributter av ulike verdityper til varene, for å gjøre det enklere for deg å sortere og finne varer.|[Arbeid med vareattributter](inventory-how-work-item-attributes.md)|
|Opprett spesielle varekort for varer som du tilbyr til kunder, men som du ikke har på lager.|[Arbeide med katalogvarer](inventory-how-work-nonstock-items.md)|
|Utfør fysisk lagertelling med sidene **Vareopptellingsordre** og **Registrering for vareopptelling**.|[Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md)|
|Du kan utføre fysisk telling, foreta negative eller positive justeringer og endre informasjon, for eksempel lokasjons- eller partinummer, i vareposter.|[Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)|
|Vis tilgjengeligheten av varer per lokasjon, etter periode, ved salg eller kjøpshendelse eller ved bruk på monterings- eller produksjonsstykklister.|[Vis tilgjengeligheten av varer](inventory-how-availability-overview.md)|
|Overføre varer mellom lokasjoner ved å bruke overføringsordrer for å administrere lageraktiviteter, eller med varereklassifiseringskladden.|[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)|
|Reserver lagervarer eller inngående varer for ordrer, bestillinger, serviceordrer, monteringsordrer, overføringsordrer eller produksjonsordrer.|[Reservere varer](inventory-how-to-reserve-items.md)|
|Definer varesporing slik at du kan spore vareserienumre, for eksempel når du må spore varer på grunn av tilbakekallinger.|[Konfigurer varesporing med serie-, parti- og pakkenumre](inventory-how-setup-item-tracking.md)|
|Tilordne serienumre eller partinumre til alle utgående eller inngående dokumenter eller kladdelinjer.|[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)|
|Finn ut hvor eventuelle serie- eller partinummer ble brukt i dets forsyningskjede, for eksempel i tilbakekallingssituasjoner.|[Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)|
|Sett opp en leverandørs egen beskrivelse av en vare på varekortet, slik at du raskt kan sette inn varebeskrivelser på handelsdokumenter.|[Bruk varereferanser](inventory-how-use-item-cross-refs.md)|
|Blokker varer fra å bli lagt inn på salgs- eller bestillingslinjene eller fra å bli bokført i en transaksjon.|[Blokker varer](inventory-how-block-items.md)|
|Håndter forretningsdriften i salgskontorer, innkjøpsavdelinger eller anleggsplanleggingskontorer på tvers av flere lokasjoner.|[Arbeide med ansvarssentre](inventory-responsibility-centers.md)|
|Bruk ressurser med bestemte funksjoner for forskjellige tjenester og servicevarer.|[Konfigurer ressurstildeling](service-how-setup-resource-allocation.md)|

## Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)    
[Innkjøp](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Generelle forretningsfunksjoner](ui-across-business-areas.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
