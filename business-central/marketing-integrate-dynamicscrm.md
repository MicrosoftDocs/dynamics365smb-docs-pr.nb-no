---
title: Administrere kunder ved hjelp av Dynamics 365 for Sales | Microsoft-dokumentasjon
description: "Du kan bruke Dynamics 365 for Sales fra Business Central for å tilordne data og få sømløs integrasjon og synkronisering i interessent-til-kontanter-prosessen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 65466039efae2b18821fb03b6465f4c8c5e18f68
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Behandle kunder og Salg som er opprettet i Dynamics 365 for Sales
Hvis du bruker Dynamics 365 for Sales (Sales) for Customer Engagement, kan du bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] for ordrebehandling og økonomi og få sømløs integrasjon i kundeemne-til-kontanter-prosessen.

Når programmet er konfigurert til å integrere med Sales, har du tilgang til salgstall fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og motsatt vei i noen tilfeller. Denne integrasjonen gjør at du kan arbeide med og synkronisere datatyper som er felles for begge tjenester, for eksempel kunder, kontakter og salgsinformasjon, og hold dataene oppdaterte på begge lokasjoner.  

Selgeren i Sales kan for eksempel bruke prislister fra [!INCLUDE[d365fin](includes/d365fin_md.md)] når de oppretter en salgsordre. Når de legger til varen på salgsordrelinjen i Sales, kan de også se lagernivået (tilgjengelighet) av varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

I motsetning kan ordrebehandlere i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndtere de spesielle egenskapene til ordre som er automatisk eller manuelt overført fra Sales, for eksempel automatisk oppretting og bokføring av gyldige ordrelinjer for varer eller ressurser som er som angitt i Sales som varer som ikke finnes i produktkatalogen. Hvis du vil ha mer informasjon, kan du se delen "Håndtere spesielle ordredata".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integreres bare med Dynamics 365 for Sales. Andre programmer eller løsninger i Dynamics 365 som endrer standard arbeidsflyt eller datamodell i Sales, for eksempel Project Service Automation, kan bryte integrasjonen mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard Sales-enhetstilordning for synkronisering
Sales-enheter, for eksempel kontoer, er integrert med tilsvarende [!INCLUDE[d365fin](includes/d365fin_md.md)]-oppføringstyper, for eksempel kunder. For å arbeide med Sales-data setter du opp tilordninger, kalt koblinger, mellom [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og Sales-enhetsposter. For eksempel setter du opp en kobling mellom en bestemt kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)] og en tilsvarende konto i Sales.

Følgende tabeller viser [!INCLUDE[d365fin](includes/d365fin_md.md)]-posttyper (tabeller) og tilhørende Sales-enheter som har innebygd støtte for synkronisering.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Salg|Synkroniseringsretning|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Selger/innkjøper|Bruker|Sales -> Business Central|Sales-kontaktfilter: **Status** er **Nei**, **Bruker lisensiert** er **Ja**, integreringsbrukermodus er **Nei**|
|Kunde|Konto|Business Central -> Sales og Sales -> Business Central|Sales-kontofilter: **Relasjonstype** er **Kunde** og **Status** er **Aktiv**.|
|Kontakt|Kontakt|Business Central -> Sales og Sales -> Business Central|Business Central-kontaktfilter: **Type** er **Person** og kontakten er tilordnet til et firma. Sales-kontaktfilter: Kontakten er tilordnet et firma, og overordnet kundetype er **Konto**.|
|Valuta|Transaksjonsvaluta|Business Central -> Sales| |
|Måleenhet|Enhetsgruppe|Business Central -> Sales| |
|Element|Produkt|Business Central -> Sales og Sales -> Business Central|Sales-kontaktfilter: **Produkttype** er **Varelager**|
|Ressurs|Produkt|Business Central -> Sales og Sales -> Business Central|Sales-kontaktfilter: **Produkttype** er **Tjenester**|
|Kundeprisgruppe|Prisliste|Business Central -> Sales| |
|Salgspris|Produktprisliste|Business Central -> Sales|Business Central-kontaktfilter: **Salgskode** er ikke tom, **Salgstype** er **Kundeprisgruppe**|
|Salgsmulighet|Salgsmulighet|Business Central -> Sales og Sales -> Business Central| |
|Salgsfakturahode|Fakturere|Business Central -> Sales| |
|Salgsfakturalinje|Fakturaprodukt|Business Central -> Sales| |

Sales-enhetene og [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller som synkroniseres, er definert med tabelltilordningoppføringer i tabellen 5335, **Tilordning for integreringstabell**. Du kan vise tilordningene og sette opp filtre fra siden 5335, **Tilordninger for integreringstabell**. Tilordning mellom feltene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster og feltene i Sales-enheter er definert av felttilordningsoppføringene i tabellen 5336, **Tilordninger for integreringstabell** og ekstra tilordningslogikk.

### <a name="field-mapping-for-the-sales-account-option"></a>Felttilordning for alternativet Salgskonto
Tre tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] tilordnes alternativfeltene til **Konto**-enheten.   

Postene i tabellen som ikke er knyttet til alternativene som finnes i Sales utelates under synkroniseringen. Dette betyr at **Alternativ**-feltet vil være tomt i Sales.

Tabellen nedenfor viser tilordninger fra Business Central-tabeller for **Alternativ**-feltet **Konto**-enheten.

|Bord|Alternativfeltet i Konto-enhet i Sales|
|----------------------|-------------------------------------------|
|Betalingsbetingelser|Betalingsbetingelser|
|Leveringsmåte|Adresse 1: Fraktvilkår|
|Transportør|Adresse 1: Leveringsmåte|

### <a name="synchronization-rules"></a>Synkroniseringsregler
Tabellen nedenfor beskriver reglene som styrer synkroniseringen mellom Business Central-tabeller og Sales-enheter.

> [!NOTE]  
> Endringer i dataene i Sales som er utført av Sales-tilkoblingskontoen, ignoreres. Endringene synkroniseres ikke. Det anbefales derfor at du ikke endrer data ved å bruke Sales-tilkoblingskontoen.

|Bord|Regel|
|-----|----|
|Kunder|Før en kunde kan synkroniseres til en konto, må selgeren som er tilordnet kunden, være koblet til en bruker i Sales. Når du kjører KUNDER – Dynamics 365 for Sales-synkroniseringsjobben, og du konfigurerer den til å opprette nye poster, må du sørge for at du synkroniserer selgere med Sales-brukere før du synkroniserer kunder med Sales-kontoer. <br /> <br />KUNDER – Dynamics 365 for Sales-synkroniseringsjobb synkroniserer bare Sales-kontoer som har relasjonstypen Kunder.|
|Kontakter|Bare kontakter i Sales som er forbundet med en konto, blir opprettet i Business Central. Verdien Selgerkode definerer eieren av sammenkoblede enheten i Sales.|
|Valutaer|Valutaer er koblet til transaksjonsvalutaer i Sales basert på ISO-kodene. Bare valutaer som har en standard ISO-kode, vil bli koblet og synkronisert med transaksjonsvalutaer.|
|Enheter|Enheter synkroniseres med enhetsgrupper i Sales. Det kan bare være én definert enhet i enhetsgruppen.|
|Varer|Når du synkroniserer elementer med Sales-produkter, oppretter Business Central automatisk en prisliste i Sales. Hvis du vil unngå synkroniseringsfeil, bør du ikke endre denne prislisten manuelt.|
|Selgere|Selgerne er koblet til brukere i Sales. Brukeren må være aktivert og lisensiert og kan ikke være integreringsbrukeren. Vær oppmerksom på at dette er den første tabellen som må synkroniseres fordi den brukes i kunder, kontakter, salgsmuligheter og salgsfakturaer.|
|Ressurser|Ressurser synkroniseres med Sales-produkter som produkttypen Tjeneste.|
|Kundeprisgrupper|Kundeprisgrupper synkroniseres med Sales-prislister.|
|Salgspriser|Salgsprisene som har salgstypen Kundeprisgruppe og har en definert salgskode, synkroniseres med salgprislisteslinjer|
|Salgsmuligheter|Salgsmuligheter synkroniseres med salgsmuligheter i Sales. Verdien Selgerkode definerer eieren av sammenkoblede enheten i Sales.|
|Bokførte salgsfakturaer|Bokførte salgsfakturaer synkroniseres med salgsfakturaer. Før du kan synkronisere en faktura, er det best å synkronisere alle andre enheter som kan inngå i fakturaen, fra selgere til prislister. Verdien Selgerkode i fakturaoverskriften definerer eieren av sammenkoblede enheten i Sales.|

## <a name="setting-up-the-connection"></a>Definere tilkoblingen
Fra startsiden kan du få tilgang til **Tilkoblingsoppsett for Microsoft Dynamics 365** assistert oppsettguide som hjelper deg med å konfigurere tilkoblingen. Når dette er gjort, vil du ha en sømløs kobling i Sales-oppføringer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

> [!NOTE]  
>   Det følgende forklarer det assisterte oppsettet, men du kan utføre de samme oppgavene manuelt på siden **Tilkoblingsoppsett for Sales**.

Du kan velge hvilke data som skal synkroniseres mellom de to tjenestene i den assisterte oppsettguiden. Du kan også angi at du vil importere din eksisterende Sales-løsning. I så fall må du angi en administrativ brukerkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurere kontoen for import av løsning
Hvis du vil importere en eksisterende Sales-løsning, bruker oppsettguiden en administrativ konto. Angi kontoen som må være en gyldig bruker i Sales med følgende sikkerhetsroller:

* Systemansvarlig  
* Løsningstilpasser  

Hvis du vil ha mer informasjon, kan du se [Opprette brukere i Microsoft Dynamics 365 (online) og tilordne sikkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) og [Administrere brukere og tillatelser](ui-how-users-permissions.md).  

Denne kontoen brukes bare under oppsettet. Når løsningen er importert til [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke lenger nødvendig.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurere kontoen for synkronisering
Integreringen er avhengig av en delt brukerkonto. Så i Office 365-abonnementet, må du opprette et engasjert personell som skal brukes for synkronisering mellom de to tjenestene. Denne kontoen må være en gyldig bruker i Sales allerede, men du trenger ikke å tilordne sikkerhetsroller til kontoen fordi installasjonsprogrammet for TV-guiden gjør dette for deg. Du må angi denne kontoen én eller flere ganger i installasjonsveiledningen, avhengig av hvor mye synkroniseringen du vil aktivere. Hvis du vil ha mer informasjon, kan du se [Opprette brukere i Microsoft Dynamics 365 (online) og tilordne sikkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Hvis du velger å aktivere *Varedisposisjon*, må integrasjonsbrukerkontoen ha en tilgangstast for webtjenester. Dette er en totrinns ting på siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for denne brukerkontoen, må du velge knappen **Endre webtjenestenøkkel**, og i oppsettguiden for tilkobling av Sales må du angi brukeren som OData-webtjenestebrukeren.

Hvis du velger å aktivere *ordrerintegrering*, må du angi en bruker som kan håndtere denne synkroniseringen - integreringsbrukeren eller en annen brukerkonto.

### <a name="coupling-records"></a>Koblingsposter
Du kan velge å synkronisere mellom de to tjenestene i den assisterte oppsettguiden. Men senere kan du også definere synkronisering av bestemte typer data. Dette kalles *kobling*, og denne delen inneholder anbefalinger om hva du må ta i betraktning.

Hvis du vil vise Sales-kontoer som kunder i for eksempel [!INCLUDE[d365fin](includes/d365fin_md.md)], må du koble to typer poster. Det er ikke veldig komplisert - du åpner **Kundeoversikt**-siden i [!INCLUDE[d365fin](includes/d365fin_md.md)], og det er en handling i båndet for å koble disse dataene med Sales. Vil du angi hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som samsvarer med hvilke konti i Sales.

I enkelte områder avhenger funksjonaliteten av at du kobler noen bestemte sett med data før andre sett med data, som vist i følgende liste:

* Kunder og konti  
  * Koble selgere med Sales-brukere først  
* Varer og ressurser  
  * Koble målenheter med Sales-enhetsgrupper først  
* Varer og ressurspriser  
  * Koble kundeprisgrupper med Sales-priser først  

> [!NOTE]  
>   Hvis du bruker priser i utenlandsk valuta, må du kontrollere at du kobler valutaer til Sales-transaksjonsvalutaer.

Sales-salgsordrer avhenger av ekstra informasjon, for eksempel kunder, målenheter, valutaer, kundeprisgrupper, varer og/eller ressurser. For at integrasjonen med salgsordrer skal fungere sømløst, må du koble kunder, målenheter, valutaer, kundeprisgrupper, varer og/eller ressurser først.

### <a name="synchronizing-records-fully"></a>Fullstendig synkronisering av oppføringer
Til slutten av den assisterte oppsettguiden, kan du velge **Kjør full synkronisering** for å starte synkronisering av alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterte poster i den tilkoblede Sales-løsningen. På siden **Gjennomgang av full synkronisering for CRM** velger du **Start**-handlingen. Deretter synkroniseringen begynner å utføre jobber i henhold til avhengighetene. Hvis du for eksempel synkroniseres valuta poster før kundeoppføringer. Fullstendig synkronisering kan ta lang tid, og derfor kjører i bakgrunnen, slik at du kan fortsette å arbeide [!INCLUDE[d365fin](includes/d365fin_md.md)].

Hvis du vil kontrollere fremdriften for individuelle prosjekter i en fullstendig synkronisering, driller du ned til feltet **Status for jobbkøpost**, **Prosjektstatus fot Til int. tabell** eller **Prosjektstatus for Fra int. tabell** på siden **Gjennomgang av full synkronisering for CRM**.

Fra siden **Tilkoblingsoppsett for Microsoft Dynamics 365** kan du få detaljer om fullstendig synkronisering når som helst. Herfra kan du også åpne **Tilordninger for integreringstabell**-siden for å se detaljer om tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)] og i Sales-løsningen som må synkroniseres.

## <a name="handling-special-sales-order-data"></a>Håndtere spesielle ordredata
Ordrer i Sales blir automatisk overført til [!INCLUDE[d365fin](includes/d365fin_md.md)] hvis du merker av for **Opprette ordrer automatisk** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**. For slike ordrer blir **Navn**-feltet i den opprinnelige ordren overført og tilordnet feltet **Eksternt dokumentnummer** på ordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dette kan også fungere hvis den opprinnelige ordren inneholder produkter som ikke er i produktkatalogen, det vil si varer eller ressurser som ikke er registrert i et produkt. I så fall må du fylle ut feltene **Produkt som ikke er i produktkatalogen** og **Nummer på produktet som ikke er i produktkatalogen** på **Salgsoppsett**-siden, slik at alle slike ikke-registrerte produktsalg er tilordnet til en bestemt vare/ressurs for finansanalyse.

Hvis varebeskrivelsen i den opprinnelige ordren er svært lang, kan en ekstra ordrelinje av typen merknaden opprettes som har plass til hele teksten i ordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Se også
[Forbindelser](marketing-relationship-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Introduser organisasjonen og brukerne for Dynamics 365 (tilkoblet)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

