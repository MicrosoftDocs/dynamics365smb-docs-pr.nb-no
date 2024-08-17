---
title: Synkronisering og dataintegrering
description: Synkroniseringen kopierer data mellom Microsoft Dataverse-tabeller og Business Central-poster og holder dataene i begge systemene oppdatert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.saerch.form: 5372_Primary
ms.service: dynamics-365-business-central
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synkronisering av data i Business Central med Microsoft Dataverse

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

### <a name="tip-for-admins-viewing-table-mappings"></a>Tips for administratorer: vise tabelltilordninger

Du kan vise tilordningen mellom tabellene i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)] på siden **Tilordninger for integreringstabell**, der du kan også kan bruke filtre. Du definerer tilordningen mellom feltene i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller og kolonnene i [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellene på siden **Tilordning for integreringsfelt**, der du kan legge til mer tilordningslogikk. Dette kan for eksempel være nyttig hvis du trenger for å feilsøke synkronisering.

## <a name="use-virtual-tables-to-get-more-data"></a>Bruke virtuelle tabeller til å hente mer data

Når du konfigurerer integreringen, kan du bruke virtuelle tabeller til å gjøre mer data tilgjengelig i [!INCLUDE[prod_short](includes/cds_long_md.md)], uten hjelp fra en utvikler.

En virtuell tabell er en tilpasset tabell som har kolonner og rader som inneholder data fra en ekstern datakilde, for eksempel [!INCLUDE [prod_short](includes/prod_short.md)]. Kolonnene og radene i en virtuell tabell ser ut som en vanlig tabell, men dataene lagres ikke i en fysisk tabell i databasen [!INCLUDE[prod_short](includes/cds_long_md.md)] . I stedet hentes dataene under kjøring.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] inneholder objekter som også kalles virtuelle tabeller. Disse tabellobjektene er ikke relatert til de virtuelle tabellene du bruker med [!INCLUDE[prod_short](includes/cds_long_md.md)].

Hvis du vil vite mer om virtuelle tabeller, går du til følgende artikler:

* [Opprett og rediger virtuelle tabeller som inneholder data fra en ekstern datakilde](/power-apps/maker/data-platform/create-edit-virtual-entities) (Power Apps-dokumentasjon)
* [Business Central Virtual Table for Microsoft Dataverse-administratorreferanse](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-admin-reference) ([!INCLUDE [prod_short](includes/prod_short.md)]-dokumentasjon)

Hvis du vil bruke virtuelle tabeller, må du installere appen **Business Central Virtual Entity** fra [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

Når du har installert appen, kan du aktivere virtuelle tabeller fra én av følgende sider i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Når du kjører den assisterte oppsettsveiledningen **Konfigurer Dataverse-tilkobling**, kan du bruke siden **Tilgjengelige virtuelle Dataverse-tabeller** til å velge flere virtuelle tabeller. Etterpå er tabellene tilgjengelige i [!INCLUDE[prod_short](includes/cds_long_md.md)] og PowerApps Maker Portal. 
* Fra sidene **Dataverse-tilkoblingsoppsett**, **Virtuelle tabeller** og **Tilgjengelige virtuelle tabeller** .  
* Fra Power App Maker Portal.

## <a name="synchronize-data-from-multiple-companies-or-environments"></a>Synkronisere data fra flere selskaper eller miljøer

Du kan synkronisere data fra flere [!INCLUDE [prod_short](includes/prod_short.md)]-selskaper eller miljøer med et [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljø. I synkroniseringsscenarier for flere selskaper er det flere ting du bør vurdere.

### <a name="set-company-ids"></a>Angi firma-IDer

Når du synkroniserer oppføringer, angir vi en selskaps-ID på [!INCLUDE[prod_short](includes/cds_long_md.md)]-enheten for å tydeliggjøre [!INCLUDE [prod_short](includes/prod_short.md)]-selskapet postene kom fra. Integreringstabelltilordninger har filterfelt for integreringstabeller som tar hensyn til selskaps-ID-en. Hvis du vil inkludere en tabelltilordning i et flerfirmaoppsett, går du til siden **Tilordning for integreringstabell** og velger **Synkronisering av flere selskaper er aktivert**. Innstillingen optimaliserer hvordan filterfelt for integreringstabeller filtrerer firma-IDer i et oppsett med flere firmaer.

For integreringstabelltilordninger som synkroniserer dokumenter, for eksempel ordrer, tilbud og salgsmuligheter, vurderer integreringen bare enheter som har firma-IDen til gjeldende [!INCLUDE [prod_short](includes/prod_short.md)]-selskap, hvis du merker av for **Synkronisering av flere firmaer**. Hvis du vil synkronisere dokumenter, for eksempel mellom Business Central og Sales, må brukere i Sales angi selskaps-IDen i dokumentene. Ellers synkroniseres ikke dokumentene.  

Hvis du merker av for alle andre integreringstabelltilordninger, fjernes filteret på firma-ID hvis du merker av for **Synkronisering av flere firmaer**. Synkroniseringen tar hensyn til relaterte enheter, uavhengig av firma-ID-en.

### <a name="specify-the-synchronization-direction"></a>Angi synkroniseringsretningen

Hvis du aktiverer støtte for flere firmaer på en tilordning av integreringstabellen, anbefaler vi at du angir retningen for tilordningen til **FromIntegration**. Hvis du angir retningen **ToIntegration** eller **Toveis**, er det lurt å bruke **Tabellfilter** og **Integreringstabellfilter** til å kontrollere hvilke enheter som synkroniseres med hvilket selskap. Det er også en god idé å bruke samsvarsbasert kobling for å unngå å opprette dupliserte poster. Hvis du vil vite mer om treffbasert kobling, går du til [Tilpass samsvarsbasert kobling](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### <a name="use-unique-numbers"></a>Bruk unike tall

Hvis nummerserien ikke garanterer at primærnøkkelverdiene er unike for hvert selskap, anbefaler vi at du bruker prefikser. Hvis du vil begynne å bruke prefikser, oppretter du en transformasjonsregel på integreringsfelttilordningen. Hvis du vil lære mer om transformasjonsregler, kan du gå til [Håndtere forskjeller i feltverdier](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## <a name="see-also"></a>Se også

[Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planlegg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
