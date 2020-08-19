---
title: Synkronisering og dataintegrering | Microsoft Docs
description: Synkroniseringen kopierer data mellom Common Data Service-enheter og Business Central-poster og holder dataene i begge systemene oppdatert.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 2c7b7c4175f4c17e01c114f76d0b14834e0409ae
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617707"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Synkronisere data i Business Central med Common Data Service

Når du integrerer [!INCLUDE[d365fin](includes/cds_long_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fastsette om du vil synkronisere dataene i bestemte felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster (for eksempel kunder, kontakter og selgere) med tilsvarende poster i [!INCLUDE[d365fin](includes/cds_long_md.md)] (for eksempel konti, kontakter og brukere). Du kan synkronisere data fra [!INCLUDE[d365fin](includes/cds_long_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)] eller omvendt, avhengig av posttypen. Hvis du vil ha mer informasjon, kan du se [Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering bruker følgende elementer:

* Tilordninger for integreringstabell
* Tilordninger for integreringsfelt
* Synkroniseringsregler
* Koblede poster

Når synkroniseringen er satt opp, kan du koble [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster til [!INCLUDE[d365fin](includes/cds_long_md.md)]-poster for å synkronisere dataene. Du kan starte en synkronisering manuelt eller basert på en plan. Tabellen nedenfor gir en oversikt over hvordan du kan synkronisere poster.  

|  Type  |  Prinsipp  |  Se  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisere på en post-per-post-basis.<br /><br /> Du kan synkronisere enkeltposter i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel en kunde, med en tilsvarende [!INCLUDE[d365fin](includes/cds_long_md.md)]-post, for eksempel en konto. Dette er vanligvis slik brukere arbeider med [!INCLUDE[d365fin](includes/cds_long_md.md)]-data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisere på en tabelltilordningsbasis.<br /><br /> Du kan synkronisere alle poster i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell med en [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhet.|[Synkronisere individuelle tabelltilordninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisere alle endrede poster for alle tabelltilordninger.<br /><br /> Du kan synkronisere alle poster som har blitt endret i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller siden forrige synkronisering.|[Synkronisere alle endrede poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullstendig synkronisering av alle data i alle tabelltilordninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og [!INCLUDE[d365fin](includes/cds_long_md.md)]-enheter som er tilordnet, og opprette nye poster i målløsningen for ukoblede poster i kildeløsningen.<br /><br /> Fullstendig synkronisering synkroniserer alle data og ignorerer kobling. Vanligvis gjør du en fullstendig synkronisering når du har satt opp integrasjon og bare én av løsningene inneholder data. En fullstendig synkronisering kan også være nyttige i et demonstrasjonsmiljø.|[Kjør en full synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkronisere alle dataendringer for alle tabelltilordninger.<br /><br /> Du kan synkronisere [!INCLUDE[d365fin](includes/d365fin_md.md)] med [!INCLUDE[d365fin](includes/cds_long_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen.|[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Standard enhetstilordning for synkronisering
Enhetene i [!INCLUDE[d365fin](includes/cds_long_md.md)], for eksempel kontiene, er integrert med tilsvarende typer enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel kunder. Ved arbeid med [!INCLUDE[d365fin](includes/cds_long_md.md)]-data kan du lage forbindelser, kalt koblinger, mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].

Tabellen nedenfor inneholder en oversikt over standardtilordning mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] gir.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)] | Synkroniseringsretning | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Selger/innkjøper | Bruker | [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontaktfilter: **Status** er **Nei**, **Bruker lisensiert** er **Ja**, integreringsbrukermodus er **Nei** |
| Kunde | Konto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontofilter: **Relasjonstype** er **Kunde** og **Status** er **Aktiv**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-filter: **Blokkert** er tom (kunden er ikke sperret). |
| Leverandør | Konto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontofilter: **Relasjonstype** er **Leverandør** og **Status** er **Aktiv**. [!INCLUDE[d365fin](includes/d365fin_md.md)]-filter: **Blokkert** er tom (leverandøren er ikke sperret). |
| Kontakt | Kontakt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Type** er **Person** og kontakten er tilordnet til et selskap. [!INCLUDE[d365fin](includes/cds_long_md.md)]-kontaktfilter: Kontakten er tilordnet et firma, og overordnet kundetype er **Konto**. |
| Valuta | Transaksjonsvaluta | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Tips for administratorer: Vise enhetstilordninger
Du kan vise tilordningen mellom enhetene i [!INCLUDE[d365fin](includes/cds_long_md.md)] og tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)] på siden **Tilordninger for integreringstabell**, der du kan også kan bruke filtre. Du definerer tilordningen mellom feltene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller og feltene i [!INCLUDE[d365fin](includes/cds_long_md.md)]-enhetene på siden **Tilordning for integreringsfelt**, der du kan legge til mer tilordningslogikk. Dette kan for eksempel være nyttig hvis du trenger for å feilsøke synkronisering.

## <a name="see-also"></a>Se også  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
