---
title: Revidering av endringer
description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogger.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Revidering av endringer

En vanlig utfordring i mange forretningsadministrasjonsprogrammer er å unngå uønskede endringer i dataene. Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene. Denne artikkelen beskriver funksjonene for å finne ut hva som er endret, hvem som endret det, og når endringen ble gjort.

## Om endringsloggen

Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen. Du må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen. Endringsloggen er basert på endringene som utføres på dataene i tabellene som du vil spore. På siden **Endringsloggposter** er oppføringene ordnet kronologisk og viser alle endringer som gjøres i verdiene i feltene i tabellene du angir.

Sporing av endringer kan påvirke ytelsen, noe som kan koste deg tid, og øke størrelsen på databasen, noe som kan koste deg penger. Vurder følgende for å redusere disse kostnadene:

- Vær forsiktig når du velger tabellene og operasjonene.
- Ikke legg til poster og bokførte dokumenter. I stedet prioriterer du systemfelt som Opprettet av og Opprettingsdato.
- Ikke bruk sporingstypen **Alle felter**. Velg i stedet **Noen felter**, og spor bare de viktigste feltene.

> [!NOTE]
> Endringsloggen sporer ikke endringer for felter som bruker `autoIncrement property`. Et eksempel på et felt som bruker egenskapen, er feltet Heltall i tabellene Feilmeldinger og Mva-rapportlinje.

Endringsloggen deaktiveres også av hensyn til ytelsen under oppgradering av [!INCLUDE [prod_short](includes/prod_short.md)] til neste versjon. I tillegg til å gjøre oppgraderings prosessen raskere, vil det slå av loggen også til å redusere rot i endringsloggen. Så snart oppgraderingen er fullført, begynner loggen å spore endringer igjen.

> [!Important]
> Endringer vises bare i **endringsloggpostene** etter at brukerens økt er startet på nytt, som skjer på denne måten:
>
> - Økten har utløpt og ble oppdatert.
> - Brukeren har valgt et annet selskap eller rollesenter.
> - Brukeren logget av og på igjen.

## Definere endringsloggen

Du kan aktivere eller deaktivere endringsloggen på siden **Endringsloggoppsett**. Når du gjør det, logges aktiviteten, slik at du alltid kan se hvem som har gjort endringen.

På siden **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[prod_short](includes/prod_short.md)] sporer også flere systemtabeller.

> [!NOTE]
> Du kan overvåke bestemte felt for endringer, for eksempel felt som inneholder sensitive opplysninger, ved å sette opp feltovervåking. Hvis du gjør det, for å unngå redundans, vil ikke tabellen som inneholder feltet, være tilgjengelig for endringsloggoppsettet. Hvis du vil ha mer informasjon, kan du se [Overvåk sensitive felter](across-log-changes.md#monitor-sensitive-fields).

Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene på siden **Endringsloggposter**. Hvis du vil slette oppføringer, konfigurerer du en oppbevaringspolicy, der du kan angi filtre basert på datoer og klokkeslett. Hvis du vil finne ut mer om oppbevaringspolicyer, kan du gå til [Definer oppbevaringspolicyer](admin-data-retention-policies.md).  

## Analysere data i endringsloggen

Du kan bruke **Dataanalyse**-funksjonen til å analysere data i endringsloggen fra siden [Endringsloggposter](https://businesscentral.dynamics.com/?page=595) . Du trenger ikke å kjøre en rapport eller åpne et annet program, for eksempel Excel. Funksjonen gir en interaktiv og allsidig måte å beregne, summere og undersøke data på. I stedet for å kjøre rapporter ved hjelp av alternativer og filtre, kan du legge til flere faner som representerer forskjellige oppgaver eller visninger på dataene. Noen eksempler er "Hvem endret hvilke data, og når" eller "Data endres etter tabell/felt", eller en hvilken som helst annen visning du kan forestille deg. Hvis du vil lære mer om hvordan du bruker funksjonen **Dataanalyse**, kan du gå til [Analyser liste- og spørringsdata med analysemodus](analysis-mode.md).

### Scenarioer for ad hoc-analyse for endringslogg

De følgende avsnittene inneholder eksempler på scenarioer der analyse av endringslogg kan hjelpe deg med å overvåke viktige endringer.

| Område | Til ... | Åpne denne siden i analysemodus | Bruk disse feltene |
| ---- | ----- | ------------------------------- |------------------- |
| [Hvem endret hvilke data, og når](#example-who-changed-what-data-and-when) | Se hvem som endret hvilke data. | [Endringsloggposter](https://businesscentral.dynamics.com/?page=595) | **Bruker-ID**, **Dato og klokkeslett**, **Tabelltekst**, **Felttekst**, **Primærnøkkelverdi 2**, **Primærnøkkelverdi 3**, **Type endring**, **Gammel verdi** og **Ny verdi**. |
| [Dataendringer etter tabell/felt](#example-data-changes-by-tablefield) | Se dataendringer etter tabell/felt, og hvem som har gjort endringen. | [Endringsloggposter](https://businesscentral.dynamics.com/?page=595) | **Tabelltekst**, **Felttekst**, **Bruker-ID**, **Dato og klokkeslett**, **Primærnøkkelverdi 2**, **Primærnøkkelverdi 3**, **Type endring**, **Gammel verdi** og **Ny verdi**. |

### Eksempel: Hvem endret hvilke data, og når

Slik analyserer du Hvem endret hvilke data, og når:

1. Åpne [Endringsloggpostene](https://businesscentral.dynamics.com/?page=595)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: ikon for å aktiver analysemodus.
1. På **Kolonner**-menyen fjerner du alle kolonner (merk av i boksen ved siden av **Søk**-feltet på høyre side).
1. Dra **Bruker-ID**-feltet (hvem som gjorde det) til **Radgrupper**-området.
1. Velg nå følgende felter:
   - Hvis du vil vise når det skjedde, velger du **Dato og klokkeslett**.
   - Hvis du vil vise tabellen der det skjedde, velger du **Tabelloverskrift**. 
   - Hvis du vil vise hvilket felt, velger du **Felttekst**.
   - Hvis du vil vise feltkoden, velger du **Primærnøkkelverdi 2**. 
   - Hvis du vil vise selskapsnavnet, velger du **Primærnøkkelverdi 3**.
   - Hvis du vil vise om endringen var en innsettings-, oppdaterings- eller slettehandling, velger du **Type endring**.
   - Hvis du vil vise endringen, velger du **Gammel verdi** og **Ny verdi**.
1. Endre navnet på analysefanen til **Hvem endret hvilke data, og når** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Endringsloggposter (Hvem endret hvilke data, og når)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Eksempel: Dataendringer etter tabell/felt

Hvis du vil analysere dataendringer etter tabell/felt, gjør du følgende:

1. Åpne [Endringsloggpostene](https://businesscentral.dynamics.com/?page=595)-listen og velg :::image type="content" source="media/analysis-mode-icon.png" alt-text="Gå inn i analysemodus."::: ikon for å aktiver analysemodus.
1. På **Kolonner**-menyen fjerner du alle kolonner (merk av i boksen ved siden av **Søk**-feltet på høyre side).
1. Dra feltene **Tabelltittel** (i hvilken tabell) og **Felttittel** (i hvilket felt) til **Radgrupper**-området.
1. Velg nå følgende felter:
   - Hvis du vil vise når det skjedde, velger du **Dato og klokkeslett**
   - Hvis du vil vise hvem som har gjort endringen, velger du **Bruker-ID**.
   - Hvis du vil vise koden for feltet, velger du **Primærnøkkelverdi 2**.
   - Hvis du vil vise selskapsnavnet, velger du **Primærnøkkelverdi 3** (vanligvis selskapsnavnet), 
   - Hvis du vil vise om endringen var en innsettings-, oppdaterings- eller slettehandling, velger du **Type endring**.
   - Hvis du vil vise endringen, velger du **Gammel verdi** og **Ny verdi**.
1. Endre navnet på analysefanen til **Dataendringer etter tabell + felt** eller noe som beskriver denne analysen.

Bildet nedenfor viser resultatet av denne fremgangsmåten.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Eksempel på hvordan du utfører dataanalyse på siden Endringsloggposter (dataendringer etter tabell/felt)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Om aktivitetslogger

Fra enkelte sider i [!INCLUDE [prod_short](includes/prod_short.md)] kan du vise en aktivitetslogg som viser statusen og eventuelle feil fra filer du eksporterer fra eller importerer til [!INCLUDE [prod_short](includes/prod_short.md)].  

### Arbeid med aktivitetslogger

Informasjonen vises på **Aktivitetslogg**-siden i samsvar med konteksten den åpnes fra. Du kan for eksempel åpne siden fra sidene **Oppsett av dokumentutvekslingstjeneste**, **Innkommende dokument**, **Bokført salgsfaktura**og **Bokført salgskreditnota**. Du kan tømme oversikten over loggposter eller bare fjerne oversikten over poster som er eldre enn sju dager.  

## Overvåk sensitive felter

Det å holde sensitive data sikre og private er et sentralt anliggende for de fleste bedrifter. Hvis du vil legge til et sikkerhetslag, kan du overvåke viktige felt og motta en e-post når noen endrer en verdi. Det kan for eksempel hende at du vil bli varslet hvis noen endrer selskapets IBAN-nummer.

> [!NOTE]
> Sending av varsler med e-post krever at du konfigurerer e-postfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

### Konfigurer feltovervåking

Du kan bruke den assisterte oppsettsveiledningen for **Endringsoppsett for overvåkingsfelt** til å angi hvilke felt du vil overvåke basert på filterkriterier, for eksempel klassifisering av datasensitivitet for feltene. Hvis du vil ha mer informasjon, kan du se [Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md). Veiledningen lar deg også angi personen som skal motta en e-postvarsling når det oppstår en endring, og e-postkontoen som skal sende e-postvarslingen. Angi både brukeren som skal varsles, og kontoen som varslingen skal sendes fra. Når du har fullført veiledningen, kan du behandle innstillinger for feltovervåking på siden **Oppsett for feltovervåking**.

> [!NOTE]
> Når du angir e-postkontoen du vil sende varsler fra, må du legge til enten **Microsoft 365**- eller **SMTP**-kontotypen. Varsler bør sendes fra en konto som ikke er knyttet til en faktisk bruker. Du kan derfor ikke velge **Gjeldende bruker**-kontotypen. Hvis du gjør det, sendes ikke varslinger.

Over tid vil listen over oppføringer på siden **Overvåkede feltloggposter** bli større. Hvis du vil redusere antall oppføringer, kan du opprette en oppbevaringspolicy som sletter poster etter en bestemt tidsperiode. Hvis du vil ha mer informasjon, kan du se [Definere oppbevaringspolicyer](admin-data-retention-policies.md).

Når du definerer feltovervåking eller endrer noe i oppsettet, opprettes det poster for endringene. Du kan angi om du vil vise poster som er knyttet til overvåkningsoppsettet, ved å vise eller skjule dem.

Du kan behandle innstillinger for feltovervåking, for eksempel om du vil sende en e-postvarsling eller bare logge endringen, for hvert felt på siden **Regneark for overvåkede felt**. Siden er også der du kan legge til eller fjerne felt som skal overvåkes.

> [!NOTE]
> Når du har lagt til ett eller flere felt og starter overvåkingen, må du logge av [!INCLUDE[prod_short](includes/prod_short.md)] og på igjen for å kunne bruke innstillingene.

### Arbeid med feltovervåking

Oppføringer for alle endrede verdier for overvåkede felt er tilgjengelige på siden **Overvåkede feltloggposter**. Oppføring inneholder for eksempel følgende informasjon:

- Feltet der verdien ble endret.
- De opprinnelige og nye verdiene.
- Hvem som foretok endringen, og når den ble gjort.

Du kan undersøke en endring ytterligere ved å velge en verdi for å åpne siden den ble gjort på. Hvis du vil se en oversikt over alle postene, velger du **Feltendringsposter**.

### Vis telemetri for feltovervåking

Du kan konfigurere at [!INCLUDE[prod_short](includes/prod_short.md)] sender feltovervåkingsaktivitet til en Application Insights-ressurs i Microsoft Azure. Deretter kan du bruke Azure Monitor til å opprette rapporter og konfigurere varsler for de innsamlede dataene. Hvis du vil ha mer informasjon, kan du se følgende artikler i Hjelp for utviklere og IT-eksperter for [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Overvåke og analysere telemetri – aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Analysere telemetri for feltovervåking](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Definer oppbevaringspolicyer

Du kan opprette oppbevaringspolicyer for å slette unødvendige data i logger etter en angitt tidsperiode. Antall poster i en logg kan for eksempel øke over tid. Ved å rydde opp i gamle poster kan du gjøre det enklere å fokusere på nyere, og sannsynligvis mer relevante poster. Hvis du vil finne ut mer om oppbevaringspolicyer, kan du gå til [Definer oppbevaringspolicyer](admin-data-retention-policies.md).

## Se også

[Overvåk sensitive felter](across-log-changes.md#monitor-sensitive-fields)  
[Analysere telemetri for feltovervåking](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Definere oppbevaringspolicyer](admin-data-retention-policies.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Sorter, søk etter og filtrer](ui-enter-criteria-filters.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
