---
title: Tildeling tabellene og feltene som skal synkroniseres
description: Lær hvordan du kan tilordne tabeller og felt for å synkronisere data mellom Business Central og Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 08/07/2024
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Tildeling tabellene og feltene som skal synkroniseres

Det grunnleggende for å synkronisere data er å tilordne tabeller og felter i [!INCLUDE[prod_short](includes/prod_short.md)] med tabeller og kolonner i [!INCLUDE[prod_short](includes/cds_long_md.md)] slik at de kan utveksle data. Tilordning skjer gjennom integrasjonstabeller.

## <a name="mapping-integration-tables"></a>Tilordne integrasjonstabeller

En integrasjonstabell er en tabell i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen som representerer en tabell, for eksempel en konto, i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integrasjonstabeller inneholder felt som samsvarer med kolonnene i tabellen [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integrasjonstabellen Konto kobler for eksempel til Kontoer-tabellen i [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Det må være en integrasjonstabelltilordning for hver tabell i [!INCLUDE[cds_short_md](includes/cds_short_md.md)] som du vil synkronisere med data i [!INCLUDE[prod_short](includes/prod_short.md)].

Når du oppretter tilkoblingen mellom appene, definerer [!INCLUDE[prod_short](includes/prod_short.md)] enkelte standardtilordninger. Du kan endre tabelltilordningene hvis du vil. Hvis du vil ha mer informasjon, kan du se [Standard tabelltilordning for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Hvis du har endret standardtilordningene og vil tilbakestille endringene, går du til siden **Tilordninger for integreringstabell** og velger **Bruk standard synkroniseringsoppsett**.

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[prod_short](includes/prod_short.md)], er integrasjonstabelltilordningene lagret i tabellen 5335 Tilordninger for integreringstabell, der du kan vise og redigere tilordningene. Avanserte tilordninger og synkroniseringsregler er definert i codeunit 5341.

> [!TIP]
> Når en sammenkoblet post endres, synkroniserer [!INCLUDE [prod_short](includes/prod_short.md)] dataene automatisk med Dataverse. Automatisk synkronisering er nyttig i de fleste tilfeller. Oftere endringer i store mengder sammenkoblede poster i en tabell kan imidlertid redusere datasynkroniseringen.
>
> Hvis du vil unngå lav ytelse, kan du aktivere eller deaktivere hendelsesbasert datasynkronisering for en tabell på siden **Tildelinger for integreringstabell**. Som standard er hendelsesbasert synkronisering aktivert, slik at eksisterende integrasjon ikke påvirkes. Systemansvarlig kan aktivere eller deaktivere den for bestemte tabeller.

### <a name="add-table-and-field-mappings-to-existing-integration-tables"></a>Legge til tabell- og felttilordninger i eksisterende integreringstabeller

På siden **integreringstabell Tilordninger** kan du bruke handlingen Ny tabelltilknytning til å legge til nye tabelltilordninger i integreringstabeller. Handlingen starter det assisterte oppsettet **Opprett nye integreringstilordninger** hjelpelinje, som hjelper deg med å konfigurere nye integreringstabell- og felttilordninger.

Med hjelpelinje kan du tilordne tabellene sammen [!INCLUDE [prod_short](includes/prod_short.md)] med eksisterende integreringstabeller Dataverse. Du kan også angi Dataverse tabellens unike identifikator i **integreringstabell Navn på unik** identifikator og **integreringstabell Endret ved feltnavn**, som er nødvendige for at datasynkronisering skal fungere.

> [!NOTE]
> Oppslaget i Tabell-kolonnen viser alle [!INCLUDE [prod_short](includes/prod_short.md)] tabeller, inkludert egendefinerte tabeller, som ennå ikke er tilordnet. Den ekskluderer de som allerede finnes på integreringstabell Tilordninger-siden. Oppslaget i den integreringstabell kolonnen viser bare Dataverse tabeller (AL proxy-tabeller) som er en del av standardintegrasjoner. Hvis du vil legge til flere eller egendefinerte Dataverse tabeller, trenger du hjelp fra en utvikler til å opprette og distribuere dem via en utvidelse.

Handlingen Avansert åpner flere tabelltilknytning innstillinger du kan konfigurere. I Avansert-delen **kan** **du angi filtre for**  Tabellfilter-feltet [!INCLUDE [prod_short](includes/prod_short.md)]. Bruk integreringstabell **Filter-feltet** for data som Dataverse skal vurderes ved datasynkronisering sammen med kodene for konfigurasjonsmalen i **Table Config. Malkode** og **Int. Tbl. Config. Kode** for å forhåndsutfylle manglende data når nye data kommer fra et av programmene.

Med hjelpelinje kan du også angi hvilke felt du vil at de nye tildeling skal inneholde. Du kan sammenligne et [!INCLUDE [prod_short](includes/prod_short.md)] felt i Feltnavn-kolonnen **med** et Dataverse feltnavn i kolonnen Navn **på** integreringsfelt. Du kan også angi en **retning**, om feltet alltid har samme verdi i **kolonnen Konstant**, og om valideringer eller transformasjoner må brukes under felt tildeling.

> [!NOTE]
> Hvis du vil redusere feil, filtrerer oppslaget for **integreringstabell Felt-kolonnen** til en liste over tilgjengelige felt. Hvis du vil tilordne felt som filtrene ikke inkluderer, trenger du hjelp fra en utvikler.
>
> * Felt må være aktivert.
> * Du kan ikke bruke hjelpelinje til å tilordne FlowField- og FlowFilter-felt.
> * Du kan bare tilordne felt av typen BigInteger, boolsk, Code, Date, DateFormula, DateTime, Decimal, Duration, GUID, Heltall, Tilvalg og Tekst.

> [!TIP]
> Du kan også legge til nye felttilordninger i eksisterende integreringstabell tilordninger via **listesiden Tilordninger** for integreringsfelt, som du får tilgang til ved å velge **Felt** på **siden integreringstabell Tilordninger** .
>
> Velg Nytt **felt tildeling**  for å åpne feltet tildeling trinn i **det assisterte oppsettet Opprett nye integreringstilordninger** hjelpelinje, og fortsett deretter som beskrevet i denne artikkelen.

Nye felttilordninger du legger til i et eksisterende tabelltilknytning, er i tilstanden Deaktivert. Du kan velge **Rediger liste** for å aktivere dem senere.

### <a name="synchronization-rules"></a>Synkroniseringsregler

En integreringstabelltilordning inneholder også regler som styrer hvordan integrasjonssynkroniseringsjobber synkroniserer poster i en [!INCLUDE[prod_short](includes/prod_short.md)]-tabell og en tabell i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Gå til [Synkroniseringsregler](#synchronization-rules) for eksempler på regler for integrering med Sales.

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategier for automatisk løsing av konflikter

Det kan enkelt oppstå datakonflikter når forretningsapplikasjoner utveksler data fortløpende. Det kan for eksempel hende at noen sletter eller endrer en rad i ett av programmene, eller begge deler. Hvis du vil redusere antall konflikter du må løse manuelt, kan du angi løsningsstrategier og [!INCLUDE[prod_short](includes/prod_short.md)] vil løse konflikter automatisk i henhold til reglene i strategiene.

Integrasjonstabelltilordninger omfatter regler som styrer hvordan synkroniseringsjobber synkroniserer poster. På siden **Tilordning for integreringstabell** i kolonnene **Løs slettekonflikter** og **Løs oppdateringskonflikter** kan du angi hvordan [!INCLUDE[prod_short](includes/prod_short.md)] skal løse konflikter som oppstår fordi poster ble slettet i tabeller i én eller den andre forretningsapplikasjonen, eller oppdatert i begge. 

I kolonnen **Løs slettekonflikter** kan du velge at [!INCLUDE[prod_short](includes/prod_short.md)] gjenoppretter automatisk slettede poster, fjerner koblingen mellom postene, eller ikke gjøre noe. Hvis du ikke gjør noe, må du løse konflikter manuelt. 

I kolonnen **Løs oppdateringskonflikter** kan du velge at [!INCLUDE[prod_short](includes/prod_short.md)] sender en dataoppdatering automatisk til integreringstabellen når du sender data til [!INCLUDE[prod_short](includes/cds_long_md.md)], eller henter en dataoppdatering fra integreringstabellen ved henting av data fra [!INCLUDE[prod_short](includes/cds_long_md.md)], eller ikke gjøre noe. Hvis du ikke gjør noe, må du løse konflikter manuelt.

Når du har angitt strategien, kan du velge handlingen **Prøv alle på nytt** på siden **Feil ved synkronisering av koblede data** for å løse konflikter automatisk.

## <a name="mapping-integration-fields"></a>Tildel integreringsfelter

Tilordning av tabeller er bare det første trinnet. Du må også tilordne feltene i tabellene. Integreringsfelttilordninger kobler felt i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller med tilsvarende kolonner i [!INCLUDE[prod_short](includes/cds_long_md.md)], og avgjør om data skal synkroniseres i hver tabell. Standard tabelltilordning som [!INCLUDE[prod_short](includes/prod_short.md)] sørger for, inneholder felttilordninger, men du kan endre dem hvis du vil. Hvis du vil ha mer informasjon, kan du se [Vise tabelltilordninger](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Hvis du bruker en lokal versjon av [!INCLUDE[prod_short](includes/prod_short.md)], defineres tilordninger for integreringsfelt i tabell 5336 Tilordning for integreringsfelt.

Du kan tilordne feltene manuelt, eller du kan automatisere prosessen ved å tilordne flere felter på samme tid basert på kriterier for å sammenligne verdiene. Hvis du vil ha mer informasjon, kan du se [Slik kobler du flere poster basert på feltverdisamsvar](admin-how-to-couple-and-synchronize-records-manually.md).

### <a name="handle-differences-in-field-values"></a>Håndter forskjeller i feltverdier

Noen ganger er verdiene i feltene du vil tilordne, forskjellige. I [!INCLUDE[crm_md](includes/crm_md.md)] er språkkoden for USA for eksempel "U.S.", men i [!INCLUDE[prod_short](includes/prod_short.md)] er den "US". Det betyr at du må transformere verdien når du synkroniserer data. Dette skjer gjennom transformeringsregler som du definerer for feltene. Du definerer transformeringsregler på siden **Tilordninger for integreringstabell** ved å velge **Tilordning** og deretter **Felt**. Forhåndsdefinerte regler er angitt, men du kan også opprette dine egne. Hvis du vil ha mer informasjon, kan du se [Transformeringsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handle-missing-option-values"></a>Håndter manglende alternativverdier

[!INCLUDE[prod_short](includes/cds_long_md.md)] inneholder tre kolonner som formidler verdier du kan tilordne til [!INCLUDE[prod_short](includes/prod_short.md)]-felt av typen **Alternativ** for automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilordnede alternativer, og de manglende alternativene legges til i den relaterte [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og legges til i systemtabellen **Tilordning av CDS-alternativ** for å håndteres manuelt senere. Det kan for eksempel være å legge til de manglende alternativene i hvert produkt og deretter oppdatere tilordningen. Hvis du vil ha mer informasjon, kan du se [Håndtere manglende alternativverdier](admin-cds-missing-option-values.md).

## <a name="couple-records"></a>Koble poster

Kobling kobler rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] til poster i [!INCLUDE[prod_short](includes/prod_short.md)]. Kontoer i [!INCLUDE[prod_short](includes/cds_long_md.md)] er for eksempel vanligvis koblet sammen med kunder i [!INCLUDE[prod_short](includes/prod_short.md)]. Kobling av poster gir følgende fordeler:

* Det gjør synkronisering mulig.
* Brukere kan åpne poster eller rader i én forretningsapp fra den andre. Dette krever at appene allerede er integrert.

Koblinger kan settes opp automatisk ved hjelp av synkroniseringsjobber eller manuelt ved å redigere posten i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Synkronisere data i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) og [Sammenkoble og synkronisere poster manuelt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filter-records-and-rows"></a>Filtrer poster og rader

Hvis du ikke vil synkronisere alle radene for en bestemt tabell i [!INCLUDE[prod_short](includes/cds_long_md.md)] eller tabell i [!INCLUDE[prod_short](includes/prod_short.md)], kan du sette opp filtre for å begrense dataene som synkroniseres. Du definerer filtrene på siden **Tilordninger for integreringstabell**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2. For å filtrere [!INCLUDE[prod_short](includes/prod_short.md)]-postene angir du **Tabellfilter**-feltet.  
3. For å filtrere [!INCLUDE[prod_short](includes/cds_long_md.md)]-radene angir du **Integreringstabellfilter**-feltet.  

## <a name="create-new-records"></a>Opprett nye poster

Som standard vil bare poster i [!INCLUDE[prod_short](includes/prod_short.md)] og rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] som er koblet, synkroniseres av integreringssynkroniseringsjobbene. Du kan definere tabelltilordninger slik at nye poster eller rader opprettes i målet (for eksempel [!INCLUDE[prod_short](includes/prod_short.md)]) for hver rad i kilden (for eksempel [!INCLUDE[prod_short](includes/cds_long_md.md)]) som ikke allerede er koblet.  

SELGERE – Dynamics 365 Sales-synkroniseringsjobben bruker for eksempel tabelltilordningen SELGERE. Synkroniseringsjobben kopierer data fra brukere i [!INCLUDE[prod_short](includes/cds_long_md.md)] til selgere i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du setter opp tabelltilordningen til å opprette nye poster, for hver bruker i [!INCLUDE[prod_short](includes/cds_long_md.md)] som ikke er allerede koblet til en selger i [!INCLUDE[prod_short](includes/prod_short.md)], opprettes en ny selgerrad i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-create-new-records-during-synchronization"></a>Slik oppretter du nye poster under synkronisering

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2. I tabelltilordningsoppføringen i listen fjerner du **Synkroniser bare koblede poster**-feltet.  

## <a name="use-configuration-templates-on-table-mappings"></a>Bruk konfigurasjonsmaler på tabelltildelinger

Du kan tilordne konfigurasjonsmaler til tabelltilordninger til bruk for nye poster eller rader som er opprettet i [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)]. For hver tabelltilordning kan du angi en konfigurasjonsmal som skal brukes for nye [!INCLUDE[prod_short](includes/prod_short.md)]-poster, og en annen mal for å bruke nye [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader.  

Hvis du installerer standard synkroniseringsoppsett, vil to konfigurasjonsmaler vanligvis bli opprettet automatisk og brukes på tabelltilordningen for [!INCLUDE[prod_short](includes/prod_short.md)]-kunder og [!INCLUDE[crm_md](includes/crm_md.md)]-kontoer: **CDSCUST** og **CDSACCOUNT**.  

* **CDSCUST** oppretter og synkroniserer nye kunder i [!INCLUDE[prod_short](includes/prod_short.md)] basert på kontoer i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Opprett denne malen ved å kopiere en eksisterende konfigurasjonsmal for kunder. **CDSCUST** opprettes bare hvis det finnes en eksisterende konfigurasjonsmal og **Valutakoden** -feltet i malen er tomt. Hvis et felt i konfigurasjonsmalen inneholder en verdi, brukes verdien i stedet for verdien i den tilordnede kolonnen for [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontoen. Hvis **Land/region**-kolonnen i en [!INCLUDE[prod_short](includes/cds_long_md.md)]-konto inneholder *USA*, og **Land/region**-feltet i konfigurasjonsmalen er **GB**, brukes **GB** som **Land/region** for den opprettede kunden i [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** oppretter og synkroniserer nye kontoer i [!INCLUDE[prod_short](includes/cds_long_md.md)] basert på en konto i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Angi konfigurasjonsmaler på en tabelltilordning

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Tilordninger for integreringstabell**, og velg deretter den relaterte koblingen.
2. I tabelltilordningsposten i listen angir du **Malkode for konfigurasjon av tabell**-feltet, velger du konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Sett **Malkode for konfigurasjon av int.tab.**-feltet til konfigurasjonsmalen som skal brukes for nye poster i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Se også

[Om integrering av Dynamics 365 Business Central med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Synkronisere Business Central og [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Planlegge en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
