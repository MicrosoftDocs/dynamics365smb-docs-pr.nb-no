---
title: Integrere med Dynamics 365 Sales | Microsoft Docs
description: Lær hvordan du klargjør Dynamics 365 Business Central for integrering med Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/30/2020
ms.author: bholtorf
ms.openlocfilehash: c42393145fc921c85570e0829c0953757981b53e
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529016"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integrere med Dynamics 365 Sales.

Selgerrollen regnes ofte som den mest synlige jobben i et konsern. Det kan imidlertid være nyttig for selgere å kunne se innover i konsernet, og se hva som skjer internt. Ved å integrere [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] kan du gi selgerne innsikt ved at de kan se informasjon i [!INCLUDE[d365fin](includes/d365fin_md.md)] når de arbeider i [!INCLUDE[crm_md](includes/crm_md.md)]. For eksempel, når du forbereder et tilbud, kan det være nyttig å vite om du har tilstrekkelig lagerbeholdning til å oppfylle ordren. Hvis du vil ha mer informasjon, kan du se [Bruke Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dette emnet beskriver prosessen med å integrere de elektroniske versjonene av [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)] via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du vil ha informasjon om lokal konfigurasjon, kan du se [Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Integrasjon via Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan også integreres med [!INCLUDE[d365fin](includes/cds_long_md.md)], som gjør det enkelt å koble til og synkronisere data med andre Dynamics 365-apper, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller til og med apper du lager selv. Hvis du integrerer for første gang, anbefales det at du gjør det via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du vil ha mer informasjon, kan du se [Integrasjon med Common Data Service](admin-common-data-service.md).

Hvis du allerede har integrert [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du fortsette å synkronisere data ved hjelp av konfigurasjonen. Hvis du imidlertid oppgraderer eller slår av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen, må du slå den på igjen ved å koble til via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Hvis du vil ha mer informasjon, kan du se [Oppgradere en integrasjon med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Når du kobler til på nytt via [!INCLUDE[d365fin](includes/cds_long_md.md)], brukes standard synkroniseringsinnstillinger, og eventuelle konfigurasjoner blir overskrevet. Standard tabelltilordninger vil for eksempel bli brukt.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrasjonsinnstillinger som er spesifikke for en [!INCLUDE[crm_md](includes/crm_md.md)]-integrering
Integrasjon med [!INCLUDE[d365fin](includes/d365fin_md.md)] skjer via [!INCLUDE[d365fin](includes/cds_long_md.md)], og det finnes mange standardinnstillinger og -enheter som tilbys av integrasjonen. I tillegg til standardinnstillingene er det noen som er spesifikke for [!INCLUDE[crm_md](includes/crm_md.md)]. De følgende avsnittene viser disse.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Tillatelser og sikkerhetsroller for brukerkontoer i Sales
Når du installerer integrasjonsløsningen, konfigureres tillatelser for integrasjonsbrukerkontoen. Hvis disse tillatelsene endres, er det mulig at du må tilbakestille dem. Dette kan du gjøre ved å installere integrasjonsløsningen på nytt ved å velge **Distribuer integreringsløsning på nytt** på siden **Konfigurasjon for Dynamics 365-tilkobling**. Følgende sikkerhetsroller distribueres:

* Integrasjonsadministrator for Dynamics 365 Business Central
* Integrasjonsbruker for Dynamics 365 Business Central
* Produkttilgjengelighetsbruker for Dynamics 365 Business Central

### <a name="connection-settings-in-the-setup-guide"></a>Tilkoblingsinnstillinger i installasjonsveiledningen
Du kan bruke en assistert oppsettsveiledning til raskt å konfigurere tilkoblingen og angi avanserte funksjoner, for eksempel kobling mellom poster.

1. Velg **Oppsett og utvidelser**, og velg deretter **Assistert oppsett**.
2. Velg **Konfigurere en Dynamics 365 Sales-tilkobling** for å starte den assisterte oppsettsveiledningen.
3. Fyll ut feltene etter behov.
4. Det finnes også avanserte innstillinger som kan forbedre sikkerheten og aktivere flere muligheter, for eksempel ordrebehandling og visning av lagernivåer. Tabellen nedenfor beskriver avanserte innstillinger.  

|Felt|Beskrivelse|
|-----|-----------|
|**Importer Dynamics 365 Sales-løsning**|Aktiver dette for å installere og konfigurere integreringsløsningen i [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic-->|
|**Publiser webtjenesten Varetilgjengelighet**|Aktiver brukere som har [!INCLUDE[crm_md](includes/crm_md.md)], til å vise tilgjengeligheten av varer (produkter) på lageret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette krever en [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkonto med tilgangsnøkkel for webtjenester. Tilordning av nøkkelen er en totrinnsprosess. I brukerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)] må du velge **Endre webtjenestenøkkel**-handlingen. I den assisterte oppsettguiden Tilkoblingsoppsett for Dynamics 365 Sales må du angi URL-adresse for webtjenesten OData for Dynamics 365 Business Central og angi [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerlegitimasjon for å få tilgang til tjenesten. Hvis du vil ha mer informasjon, kan du se [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL-adresse for webtjenesten OData for Business Central**|Hvis du aktiverer webtjenesten for visning av varedisposisjon, angis URL-adressen for webtjenesten OData for deg.|
|**Brukernavn for OData-webtjeneste for Business Central**|Navnet på [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen i [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten.|
|**Tilgangsnøkkel for OData-webtjeneste for Business Central**|Tilgangsnøkkelen for brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten. Nøkkelen tilordnes til brukeren som er valgt i feltet **Brukernavn for OData-webtjeneste for Business Central** Hvis du vil ha nøkkelen, kan du velge knappen **Oppslagsverdi** ved siden av brukernavn, velge brukeren, **Administrer** og deretter klikke på **Rediger**. På kortet velger du **Handlinger**, **Godkjenning** og deretter **Endre webtjenestenøkkel**.|
|**Aktiver ordreintegrering**|Når brukerne oppretter ordrer i [!INCLUDE[crm_md](includes/crm_md.md)] og oppfyller ordrer i [!INCLUDE[d365fin](includes/d365fin_md.md)], integreres prosessen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dette krever at du oppgir rettigheter til en systemansvarligbrukerkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Håndtere ordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Aktiver CDS-tilkobling**|Aktiver tilkoblingen til [!INCLUDE[d365fin](includes/cds_long_md.md)].|
|**Dynamics 365 SDK-versjon**|Dette er bare relevant hvis du integrerer med en lokal versjon av [!INCLUDE[crm_md](includes/crm_md.md)]. Dette er Dynamics 365 SDK-versjonen (også kalt Xrm) du bruker til å koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versjonen må være kompatibel med SDK-versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)], og er lik eller nyere enn versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Tilkoblingsinnstillinger på siden Konfigurere Microsoft Dynamics 365-tilkobling 
Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Felt|Beskrivelse|
|-----|-----------|
|**URL-adresse for Dynamics 365 Sales**|URL-adressen for [!INCLUDE[crm_md](includes/crm_md.md)]-forekomsten din. Dette gjør det mulig for brukere å åpne tilhørende poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] fra poster i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel en konto eller et produkt. [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster åpnes i [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Webtjenesten Varetilgjengelighet er aktivert**|Aktiver brukere som har [!INCLUDE[crm_md](includes/crm_md.md)], til å vise tilgjengeligheten av varer (produkter) på lageret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du aktiverer dette, må du også angi et brukernavn og en tilgangsnøkkel for [!INCLUDE[crm_md](includes/crm_md.md)] for å spørre OData-webtjeneste etter tilgjengelighet for varer (produkter). Hvis du vil ha mer informasjon, kan du se [OData-webtjenester](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL-adresse for webtjenesten OData for Dynamics 365 Business Central**|Hvis du aktiverer webtjenesten Varetilgjengelighet, angis URL-adressen for webtjenesten OData for deg. Sett dette feltet til URL-adressen til [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomsten du vil bruke.<br /><br /> For å tilbakestille feltet til standard nettadresse for [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du **Tilbakestill URL-adresse for webklient**.<br /><br /> Dette feltet er aktuelt hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen er installert i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Brukernavn for webtjenesten OData for Dynamics 365 Business Central**|Navnet på brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten.|
|**Tilgangsnøkkel for webtjenesten OData for Dynamics 365 Business Central**|Tilgangsnøkkelen for brukerkontoen som [!INCLUDE[crm_md](includes/crm_md.md)] bruker til å hente informasjon om varedisposisjonen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] via OData-webtjenesten. Nøkkelen tilordnes til brukeren som er valgt i feltet **Brukernavn for webtjenesten OData for Dynamics 365 Business Central**. Hvis du vil ha nøkkelen, kan du velge knappen **Oppslagsverdi** ved siden av brukernavn, velge brukeren, **Administrer** og deretter klikke på **Rediger**. På kortet velger du **Handlinger**, **Godkjenning** og deretter **Endre webtjenestenøkkel**.|
|**Dynamics 365 SDK-versjon**|Hvis du integrerer med en lokal versjon av [!INCLUDE[crm_md](includes/crm_md.md)], er dette Dynamics 365 SDK-pakken (også kalt Xrm) du bruker til å koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]. Versjonen du velger, må være kompatibel med SDK-versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)]. Denne versjonen må være lik eller nyere enn versjonen som brukes av [!INCLUDE[crm_md](includes/crm_md.md)].|-->

I tillegg til innstillingene ovenfor, angir du følgende innstillinger for [!INCLUDE[crm_md](includes/crm_md.md)].

|Felt|Beskrivelse|
|-----|-----|
|**Ordreintegrasjon er aktivert**|Gjør det mulig for brukerne å sende ordrer og aktiverte tilbud i [!INCLUDE[crm_md](includes/crm_md.md)] og deretter vise og behandle dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette integrerer prosessen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Opprett ordrer automatisk**|Opprett en ordre i [!INCLUDE[d365fin](includes/d365fin_md.md)] når en bruker oppretter og sender en i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Behandle salgstilbud automatisk**|Behandle et tilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)] når en bruker oppretter og aktiverer et i [!INCLUDE[crm_md](includes/crm_md.md)].|

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard Sales-enhetstilordning for synkronisering
Enhetene i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel ordrer, er integrert med tilsvarende typer enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel salgsordrer. Ved arbeid med [!INCLUDE[crm_md](includes/crm_md.md)]-data kan du lage forbindelser, kalt koblinger, mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

Tabellen nedenfor inneholder en oversikt over standardtilordning mellom enheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[d365fin](includes/d365fin_md.md)] gir.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|--------------------------------------|-----------------|--------------|
|Måleenhet|Enhetsgruppe|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Vare|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Varelager**|
|Ressurs|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-kontaktfilter: **Produkttype** er **Tjenester**|
|Kundeprisgruppe|Prisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgspris|Produktprisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Kundeprisgruppe**|
|Salgsmulighet|Salgsmulighet|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Salgsfakturahode|Fakturere|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Salgsfakturalinje|Fakturaprodukt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Ordrehode|Ordre|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Salgshodefilter: **Dokumenttype** er Ordre, **Status** er Frigitt|
|Salgsordrestatus|Salgsordrestatus|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="synchronization-rules"></a>Synkroniseringsregler
Tabellen nedenfor viser reglene som styrer synkroniseringen mellom [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette er i tillegg til reglene som er definert for Common Data Service, som også gjelder. Hvis du vil ha mer informasjon, kan du se [Standard enhetstilordning for](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Endringer i data i som ble foretatt av brukerkontoen for integrasjonen, synkroniseres ikke. Vi anbefaler derfor at du ikke endrer data mens du bruker denne kontoen. Hvis du vil ha mer informasjon, kan du se [Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Enheter|Enheter synkroniseres med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan bare være én definert enhet i enhetsgruppen.|
|Varer|Når du synkroniserer elementer med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter, oppretter [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk en prisliste i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil unngå synkroniseringsfeil, bør du ikke endre denne prislisten manuelt.|
|Ressurser|Ressurser synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produkttypen Tjeneste.|
|Kundeprisgrupper|Kundeprisgrupper synkroniseres med Sales-prislister.|
|Salgspriser|Salgsprisene som har salgstypen Kundeprisgruppe og har en definert salgskode, synkroniseres med [!INCLUDE[crm_md](includes/crm_md.md)]-prislisteslinjer|
|Salgsmuligheter|Salgsmuligheter synkroniseres med salgsmuligheter i [!INCLUDE[crm_md](includes/crm_md.md)]. Verdien Selgerkode definerer eieren av den sammenkoblede enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokførte salgsfakturaer|Bokførte salgsfakturaer synkroniseres med salgsfakturaer. Før du kan synkronisere en faktura, er det best å synkronisere alle andre enheter som kan inngå i fakturaen, fra selgere til prislister. Verdien Selgerkode i fakturaoverskriften definerer eieren av sammenkoblede enheten i Sales.|
|Ordrer|Når ordreintegrasjon er aktivert, synkroniseres ordrer i [!INCLUDE[d365fin](includes/d365fin_md.md)] som opprettes fra sendte ordrer i [!INCLUDE[crm_md](includes/crm_md.md)], med ordrer i INKLUDER SALG når de frigis. Før du synkroniserer ordrer anbefaler vi at du først synkroniserer alle enheter som er knyttet til ordren, for eksempel selgere og prislister. Feltet Selgerkode i ordreoverskriften definerer eieren av den sammenkoblede enheten i [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synkroniseringsjobber for en Sales-integrasjon
Jobbene kjøres i denne rekkefølgen for å unngå å koble avhengigheter mellom enheter. Det finnes flere jobber tilgjengelig fra Common Data Service. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. MÅLEENHET – Dynamics 365 Sales-synkroniseringsjobb  
2. RESSURS-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb  
3. VARE-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb  
4. CUSTPRCGRP-PRICE – Dynamics 365 Sales-synkroniseringsjobb.
5. SALESPRC-PRODPRICE – Dynamics 365 Sales-synkroniseringsjobb.
6. POSTEDSALESINV-INV – Dynamics 365 Sales-synkroniseringsjobb.

### <a name="default-synchronization-job-queue-entries"></a>Jobbkøposter for standard synkronisering  
Tabellen nedenfor beskriver standard synkroniseringsjobber for Sales.  

|Jobbkøpost|Beskrivelse|Retning|Tilordning for integreringstabell|Standard synkroniseringsfrekvens (minutter)|Standard hvilemodustid for inaktivitet (minutter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅLEENHET – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[d365fin](includes/d365fin_md.md)]-enheter.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|MÅLENHET|30|720<br> (12 timer)|
|RESSURS-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-ressurser.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|RESSURS-PRODUKT|30|720<br> (12 timer)|
|VARE-PRODUKT – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[d365fin](includes/d365fin_md.md)]-varer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|VARE-PRODUKT|30|1440<br> (24 timer)|
|KUNDEPRISGRUPPER-PRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-salgspriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundeprisgrupper.| |KUNDEPRISGRUPPER-SALGSPRISLISTER|30|1440<br> (24 timer)|
|SALGSPRIS-PRODUKTPRIS – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-produktpriser med [!INCLUDE[d365fin](includes/d365fin_md.md)]-salgspriser.||PRODUKTPRIS-SALGSPRIS|30|1440<br> (24 timer)|
|BOKFØRTE SALGSFAKTURAER-FAKTURAER – Dynamics 365 Sales-synkroniseringsjobb|Synkroniserer [!INCLUDE[crm_md](includes/crm_md.md)]-fakturaer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-bokførte salgsfakturaer.|Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTURAER-BOKFØRTE SALGSFAKTURAER|30|1440<br> (24 timer)|
|Kundestatistikk – Dynamics 365 Sales-synkroniseringsjobb|Oppdaterer [!INCLUDE[crm_md](includes/crm_md.md)]-konti med de nyeste [!INCLUDE[d365fin](includes/d365fin_md.md)]-kundedataene. I [!INCLUDE[crm_md](includes/crm_md.md)] vises denne informasjonen i **Business Central-kontostatistikk**-hurtigvisningsskjemaet for kontoer som er koblet til [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder.<br /><br /> Disse dataene kan også oppdateres manuelt fra hver enkelt kundepost. Hvis du vil ha mer informasjon, se [Sammenkoble og synkronisere poster manuelt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Merk:**  Denne jobbkøen er relevant bare hvis [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsløsningen er installert i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ikke i bruk|Ikke i bruk|30|Ikke i bruk| 


### <a name="note-for-on-premises-versions"></a>Merknad for lokale versjoner
> [!Note]
> Hvis du kobler en lokal versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)], og du vil konfigurere en forbindelse til en [!INCLUDE[crm_md](includes/crm_md.md)]-forekomst med en bestemt godkjenningstype, fyller du ut feltene i hurtigfanen **Detaljer for godkjenningstype**. Hvis du vil ha mer informasjon, se [Bruke tilkoblingsstrenger i XRM-verktøy for å koble til Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dette trinnet er ikke nødvendig ved tilkobling av en elektronisk versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også  
[Sette opp brukerkontoer for integrasjon med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Sette opp en tilkobling til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkronisere Business Central og [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
