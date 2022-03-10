---
title: Synkronisering og dataintegrering | Microsoft Docs
description: Synkroniseringen kopierer data mellom Microsoft Dataverse-tabeller og Business Central-poster og holder dataene i begge systemene oppdatert.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Dataverse, integration, sync, synchronize, mapping
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: ceef56f1b951b5c9f1621d463276ec1d22c44da4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148827"
---
# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synkronisere data i Business Central med Microsoft Dataverse


Når du integrerer [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)], kan du fastsette om du vil synkronisere dataene i bestemte felter i [!INCLUDE[prod_short](includes/prod_short.md)] (for eksempel kunder, kontakter og selgere) med tilsvarende rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] (for eksempel konti, kontakter og brukere). Du kan synkronisere data fra [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)] eller omvendt, avhengig av radtypen. Hvis du vil ha mer informasjon, kan du se [Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering bruker følgende elementer:

* Tilordninger for integreringstabell
* Tilordninger for integreringsfelt
* Synkroniseringsregler
* Koblede poster

Når synkroniseringen er satt opp, kan du koble [!INCLUDE[prod_short](includes/prod_short.md)]-poster til [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader for å synkronisere dataene. Du kan starte en synkronisering manuelt eller basert på en plan. Tabellen nedenfor gir en oversikt over hvordan du kan synkronisere rader.  

|  Type  |  Prinsipp  |  Se  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisere på en rad-per-rad-basis.<br /><br /> Du kan synkronisere enkeltposter i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel en kunde, med en tilsvarende [!INCLUDE[prod_short](includes/cds_long_md.md)]-rad, for eksempel en konto. Dette er vanligvis slik brukere arbeider med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data i [!INCLUDE[prod_short](includes/prod_short.md)].|[Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisere på en tabelltilordningsbasis.<br /><br /> Du kan synkronisere alle poster i en [!INCLUDE[prod_short](includes/prod_short.md)]-tabell med en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabell.|[Synkronisere individuelle tabelltilordninger](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisere alle endrede poster for alle tabelltilordninger.<br /><br /> Du kan synkronisere alle poster som har blitt endret i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller siden forrige synkronisering.|[Synkronisere alle endrede poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullstendig synkronisering av alle data i alle tabelltilordninger.<br /><br /> Du kan synkronisere alle data i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabeller som er tilordnet, og opprette nye poster eller rader i målløsningen for ukoblede poster i kildeløsningen.<br /><br /> Fullstendig synkronisering synkroniserer alle data og ignorerer kobling. Vanligvis gjør du en fullstendig synkronisering når du har satt opp integrasjon og bare én av løsningene inneholder data. En fullstendig synkronisering kan også være nyttige i et demonstrasjonsmiljø.|[Kjør en full synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Planlagt synkronisering|Synkronisere alle dataendringer for alle tabelltilordninger.<br /><br /> Du kan synkronisere [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] på planlagte intervaller ved å definere jobber i jobbkøen.|[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> Synkroniseringen mellom [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] er basert på den planlagte kjøringen av prosjektkøpostene og garanterer ikke sanntidsdatakonsekvens mellom to tjenester. For sanntidsdatakonsekvens bør du utforske [virtuelle Business Central-tabeller](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) eller Business Central-API-er.   


## <a name="standard-table-mapping-for-synchronization"></a>Standard tabelltilordning for synkronisering
Tabellene i [!INCLUDE[prod_short](includes/cds_long_md.md)], for eksempel kontiene, er integrert med tilsvarende typer tabeller i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel kunder. Ved arbeid med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data kan du lage forbindelser, kalt koblinger, mellom tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

Tabellen nedenfor inneholder en oversikt over standardtilordning mellom tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Du kan tilbakestille konfigurasjonsendringer i integrasjonstabell og felttilordninger til standardinnstillingene ved å velge tilordninger, og deretter velge **Bruk standard synkroniseringsoppsett**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkroniseringsretning | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Selger/innkjøper | Bruker | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontaktfilter: **Status** er **Nei**, **Bruker lisensiert** er **Ja**, integreringsbrukermodus er **Nei** |
| Kunde | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontofilter: **Relasjonstype** er **Kunde** og **Status** er **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Blokkert** er tom (kunden er ikke sperret). |
| Leverandør | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontofilter: **Relasjonstype** er **Leverandør** og **Status** er **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)]-filter: **Blokkert** er tom (leverandøren er ikke sperret). |
| Kontakt | Kontakt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Type** er **Person** og kontakten er tilordnet til et selskap. [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontaktfilter: Kontakten er tilordnet et firma, og overordnet kundetype er **Kunde**. |
| Valuta | Transaksjonsvaluta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> **Dataverse**-handlingene er ikke tilgjengelige på sider, for eksempel Kundekort-siden, for poster som ikke tar hensyn til tabellfilteret i integrasjonstabelltilordningen.

### <a name="tip-for-admins-viewing-table-mappings"></a>Tips for administratorer: Vise tabelltilordninger
Du kan vise tilordningen mellom tabellene i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] på siden **Tilordninger for integreringstabell**, der du kan også kan bruke filtre. Du definerer tilordningen mellom feltene i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og kolonnene i [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellene på siden **Tilordning for integreringsfelt**, der du kan legge til mer tilordningslogikk. Dette kan for eksempel være nyttig hvis du trenger for å feilsøke synkronisering.

## <a name="see-also"></a>Se også  
[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
