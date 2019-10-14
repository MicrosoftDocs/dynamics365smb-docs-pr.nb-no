---
title: Synkronisering og dataintegrering | Microsoft Docs
description: Synkroniseringen kopierer data mellom Dynamics 365 Sales-poster og Business Central-poster og holder dataene i begge systemene oppdatert.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: bbc7da12176d2a5c8ab9a2ccc153ea4053d59656
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304241"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-sales"></a>Synkronisere data i Business Central og Dynamics 365 Sales
Når du integrerer [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fastsette om du vil synkronisere dataene i bestemte felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster (for eksempel kunder, kontakter og selgere) med tilsvarende poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] (for eksempel konti, kontakter og brukere). Du kan synkronisere data fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)] eller omvendt, avhengig av posttypen. Hvis du vil ha mer informasjon, kan du se [Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering bruker følgende elementer:

* Tilordninger for integreringstabell
* Tilordninger for integreringsfelt
* Synkroniseringsregler
* Koblede poster

Når synkroniseringen er satt opp, kan du koble [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster til [!INCLUDE[crm_md](includes/crm_md.md)]-poster for å synkronisere dataene. Du kan starte en synkronisering manuelt eller basert på en plan. Tabellen nedenfor gir en oversikt over hvordan du kan synkronisere poster.  

|  Type  |  Prinsipp  |  Se  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisere på en post-per-post-basis.<br /><br /> Du kan synkronisere enkeltposter i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel en kunde, med en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-post, for eksempel en konto. Dette er vanligvis slik brukere arbeider med [!INCLUDE[crm_md](includes/crm_md.md)]-data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisere på en tabelltilordningsbasis.<br /><br /> Du kan synkronisere alle poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell med en [!INCLUDE[crm_md](includes/crm_md.md)]-enhet.|[Synkronisere individuelle tabelltilordninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisere alle endrede poster for alle tabelltilordninger.<br /><br /> Du kan synkronisere alle poster som har blitt endret i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller siden forrige synkronisering.|[Synkronisere alle endrede poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullstendig synkronisering av alle data i alle tabelltilordninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og [!INCLUDE[crm_md](includes/crm_md.md)]-enheter som er tilordnet, og opprette nye poster i målløsningen for ukoblede poster i kildeløsningen.<br /><br /> Fullstendig synkronisering synkroniserer alle data og ignorerer kobling. Vanligvis gjør du en fullstendig synkronisering når du har satt opp integrasjon og bare én av løsningene inneholder data. En fullstendig synkronisering kan også være nyttige i et demonstrasjonsmiljø.|[Kjør en full synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkronisere alle dataendringer for alle tabelltilordninger.<br /><br /> Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[crm_md](includes/crm_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen.|[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard Sales-enhetstilordning for synkronisering
Enhetene i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel kontiene, er integrert med tilsvarende typer enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel kunder. Ved arbeid med [!INCLUDE[crm_md](includes/crm_md.md)]-data kan du lage forbindelser, kalt koblinger, mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Tabellen nedenfor inneholder en oversikt over standardtilordning mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] gir.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Selger/innkjøper|Bruker|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Status** er **Nei**, **Bruker lisensiert** er **Ja**, integreringsbrukermodus er **Nei**|
|Kunde|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontofilter: **Relasjonstype** er **Kunde** og **Status** er **Aktiv**.|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Type** er **Person** og kontakten er tilordnet til et selskap. Sales-kontaktfilter: Kontakten er tilordnet et firma, og overordnet kundetype er **Konto**.|
|Valuta|Transaksjonsvaluta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Måleenhet|Enhetsgruppe|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Vare|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Varelager**|
|Ressurs|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Tjenester**|
|Kundeprisgruppe|Prisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgspris|Produktprisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Kundeprisgruppe**|
|Salgsmulighet|Salgsmulighet|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Salgsfakturahode|Fakturere|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgsfakturalinje|Fakturaprodukt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Ordrehode|Ordre|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Salgshodefilter: **Dokumenttype** er Ordre, **Status** er Frigitt|
|Salgsordrestatus|Salgsordrestatus|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Tips for administratorer: Vise enhetstilordninger
Du kan vise tilordningen mellom enhetene i [!INCLUDE[crm_md](includes/crm_md.md)] og tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)] på siden **Tilordninger for integreringstabell**, der du kan også kan bruke filtre. Du definerer tilordningen mellom feltene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og feltene i [!INCLUDE[crm_md](includes/crm_md.md)]-enhetene på siden **Tilordning for integreringsfelt**, der du kan legge til mer tilordningslogikk. Dette kan for eksempel være nyttig hvis du trenger for å feilsøke synkronisering.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Tips for utviklere: Tilordne felt i Business Central til alternativsett i Sales
Hvis du er leverandør og vil legge til alternativer i alternativsettene i [!INCLUDE[crm_md](includes/crm_md.md)], må du vite dette. Det finnes tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] som tilordnes alternativfeltene i **Konto**-enheten i [!INCLUDE[crm_md](includes/crm_md.md)]. Postene i tabellene som ikke er knyttet til alternativer i [!INCLUDE[crm_md](includes/crm_md.md)], synkroniseres ikke. Dette betyr at **Alternativ**-feltet vil være tomt i [!INCLUDE[crm_md](includes/crm_md.md)].

Tabellen nedenfor viser tilordninger fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller for **Alternativ**-feltet i **Konto**-enheten i [!INCLUDE[crm_md](includes/crm_md.md)].

|Bord|Alternativfeltet i Konto-enheten|
|----------------------|-------------------------------------------|
|Betalingsbetingelser|Betalingsbetingelser|
|Leveringsmåte|Adresse 1: Fraktvilkår|
|Transportør|Adresse 1: Leveringsmåte|

### <a name="synchronization-rules"></a>Synkroniseringsregler
Tabellen nedenfor beskriver reglene som styrer synkroniseringen mellom appene.

> [!NOTE]  
> Endringer i data i [!INCLUDE[crm_md](includes/crm_md.md)] som ble foretatt av [!INCLUDE[crm_md](includes/crm_md.md)]-brukerkontoen for tilkoblingen, synkroniseres ikke. Vi anbefaler derfor at du ikke endrer data mens du bruker denne kontoen. Hvis du vil ha mer informasjon, kan du se [Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Kunder|Før en kunde kan synkroniseres til en konto, må selgeren som er tilordnet kunden, være koblet til en bruker i [!INCLUDE[crm_md](includes/crm_md.md)]. Når du kjører KUNDER – Dynamics 365 Sales-synkroniseringsjobben, og du konfigurerer den til å opprette nye poster, må du sørge for at du synkroniserer selgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brukere før du synkroniserer kunder med [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer. <br /> <br />KUNDER – Dynamics 365 Sales-synkroniseringsjobb synkroniserer bare Sales-kontoer som har relasjonstypen Kunder.|
|Kontakter|Bare kontakter i [!INCLUDE[crm_md](includes/crm_md.md)] som er forbundet med en konto, blir opprettet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Verdien Selgerkode definerer eieren av den sammenkoblede enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Valutaer|Valutaer er koblet til transaksjonsvalutaer i [!INCLUDE[crm_md](includes/crm_md.md)] basert på ISO-kodene. Bare valutaer som har en standard ISO-kode, vil bli koblet og synkronisert med transaksjonsvalutaer.|
|Enheter|Enheter synkroniseres med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan bare være én definert enhet i enhetsgruppen.|
|Varer|Når du synkroniserer elementer med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk en prisliste i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil unngå synkroniseringsfeil, bør du ikke endre denne prislisten manuelt.|
|Selgere|Selgerne er koblet til systembrukere i [!INCLUDE[crm_md](includes/crm_md.md)]. Brukeren må være aktivert og lisensiert og kan ikke være integreringsbrukeren. Vær oppmerksom på at dette er den første tabellen som må synkroniseres fordi den brukes i kunder, kontakter, salgsmuligheter og salgsfakturaer.|
|Ressurser|Ressurser synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produkttypen Tjeneste.|
|Kundeprisgrupper|Kundeprisgrupper synkroniseres med Sales-prislister.|
|Salgspriser|Salgsprisene som har salgstypen Kundeprisgruppe og har en definert salgskode, synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-prislisteslinjer|
|Salgsmuligheter|Salgsmuligheter synkroniseres med salgsmuligheter i [!INCLUDE[crm_md](includes/crm_md.md)]. Verdien Selgerkode definerer eieren av den sammenkoblede enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokførte salgsfakturaer|Bokførte salgsfakturaer synkroniseres med salgsfakturaer. Før du kan synkronisere en faktura, er det best å synkronisere alle andre enheter som kan inngå i fakturaen, fra selgere til prislister. Verdien Selgerkode i fakturaoverskriften definerer eieren av sammenkoblede enheten i Sales.|
|Ordrer|Når ordreintegrasjon er aktivert, synkroniseres ordrer i [!INCLUDE[d365fin](includes/d365fin_md.md)] som opprettes fra sendte ordrer i [!INCLUDE[crm_md](includes/crm_md.md)], med ordrer i INKLUDER SALG når de frigis. Før du synkroniserer ordrer anbefaler vi at du først synkroniserer alle enheter som er knyttet til ordren, for eksempel selgere og prislister. Feltet Selgerkode i ordreoverskriften definerer eieren av den sammenkoblede enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|  

## <a name="see-also"></a>Se også  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
