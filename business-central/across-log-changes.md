---
title: Revidering av endringer
description: Du kan aktivere en brukerlogg slik at du har en logg over eventuelle endringer i data i sporede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogger.
author: edupont04
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="auditing-changes-in-business-central"></a>Revidere endringer i Business Central

En vanlig utfordring i mange forretningsadministrasjonsprogrammer er å unngå uønskede endringer i dataene. Det kan være alt fra et uriktig kundetelefonnummer til uriktig bokføring i finanspostene. Dette emnet beskriver funksjonene for å finne ut hva som er endret, hvem som endret det, og når endringen ble gjort.

## <a name="about-the-change-log"></a>Om endringsloggen

Ved hjelp av endringsloggen kan du spore alle direkte endringer som brukeren gjør i dataene i databasen. Du må angi hver tabell og hvert felt du vil at systemet skal logge. Deretter må du aktivere endringsloggen. Endringsloggen er basert på endringene som utføres på dataene i tabellene som du vil spore. På siden **Endringsloggposter** er oppføringene ordnet kronologisk og viser alle endringer som gjøres i verdiene i feltene i tabellene du angir. 

Sporing av endringer kan påvirke ytelsen, noe som kan koste deg tid, og øke størrelsen på databasen, noe som kan koste deg penger. Vurder følgende for å redusere disse kostnadene:

- Vær forsiktig når du velger tabellene og operasjonene.
- Ikke legg til poster og bokførte dokumenter. I stedet prioriterer du systemfelt som Opprettet av og Opprettingsdato.
- Ikke bruk sporings typen Alle felt. I stedet velger du Noen felt og sporer bare de viktigste feltene.

Endringsloggen deaktiveres også av hensyn til ytelsen under oppgradering av [!INCLUDE [prod_short](includes/prod_short.md)] til neste versjon. I tillegg til å gjøre oppgraderings prosessen raskere, bidrar dette også til å redusere rot i endringsloggen. Så snart oppgraderingen er fullført, begynner loggen å spore endringer igjen.

> [!Important]
> Endringer vises bare i **endringsloggpostene** etter at brukerens økt er startet på nytt, som skjer på denne måten:
>
> * Økten har utløpt og ble oppdatert.
> * Brukeren har valgt et annet selskap eller rollesenter.
> * Brukeren logget av og på igjen.

### <a name="work-with-the-change-log"></a>Arbeid med endringsloggen
Du kan aktivere eller deaktivere endringsloggen på siden **Endringsloggoppsett**. Når en bruker aktiverer eller deaktiverer endringsloggen, logges denne aktiviteten, slik at du alltid kan se hvilken bruker som deaktiverte eller aktiverte endringsloggen.

På siden **Endringsloggoppsett**, hvis du velger **Tabeller**-handlingen, kan du angi hvilke tabeller du vil spore endringer for, og hvilke endringer du vil spore. [!INCLUDE[prod_short](includes/prod_short.md)] sporer også flere systemtabeller.

> [!NOTE]
> Du kan overvåke bestemte felt for endringer, for eksempel felt som inneholder sensitive opplysninger, ved å sette opp feltovervåking. Hvis du gjør det, for å unngå redundans, vil ikke tabellen som inneholder feltet, være tilgjengelig for endringsloggoppsettet. Hvis du vil ha mer informasjon, se [Overvåke sensitive felt](across-log-changes.md#monitoring-sensitive-fields).

Når du har opprettet endringsloggen, aktivert den og endret data, kan du vise og filtrere endringene på siden **Endringsloggposter**. Hvis du vil slette postene, kan du gjøre det på siden **Slett endringsloggposter**, der du kan definere filtre basert på datoene og tidspunktene.  

## <a name="about-activity-logs"></a>Om aktivitetslogger

Fra enkelte sider i [!INCLUDE [prod_short](includes/prod_short.md)] kan du vise en aktivitetslogg som viser statusen og eventuelle feil fra filer du eksporterer fra eller importerer til [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a>Arbeid med aktivitetslogger
Informasjonen vises på **Aktivitetslogg**-siden i samsvar med konteksten den åpnes i. Du kan for eksempel åpne siden fra sidene **Oppsett av dokumentutvekslingstjeneste**, **Innkommende dokument**, **Bokført salgsfaktura**og **Bokført salgskreditnota**. Du kan tømme oversikten over loggposter eller bare fjerne oversikten over poster som er eldre enn sju dager.  

## <a name="monitoring-sensitive-fields"></a>Overvåke sensitive felt

Det å holde sensitive data sikre og private er et sentralt anliggende for de fleste bedrifter. Hvis du vil legge til et sikkerhetslag, kan du overvåke viktige felt og bli varslet via e-post når noen endrer en verdi. Det kan for eksempel hende at du vil bli varslet hvis noen endrer selskapets IBAN-nummer.

> [!NOTE]
> Sending av varsler med e-post krever at du konfigurerer e-postfunksjonen i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Sette opp feltovervåking

Du kan bruke den assisterte oppsettsveiledningen for **Endringsoppsett for overvåkingsfelt** til å angi hvilke felt du vil overvåke basert på filterkriterier, for eksempel klassifisering av datasensitivitet for feltene. Hvis du vil ha mer informasjon, kan du se [Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md). Veiledningen lar deg også angi personen som skal motta en e-postvarsling når det oppstår en endring, og e-postkontoen som skal sende e-postvarslingen. Angi både brukeren som skal varsles, og kontoen som varslingen skal sendes fra. Når du har fullført veiledningen, kan du behandle innstillinger for feltovervåking på siden **Oppsett for feltovervåking**. 

> [!NOTE]
> Når du angir e-postkontoen du vil sende varsler fra, må du legge til enten **Microsoft 365**- eller **SMTP**-kontotypen. Varsler bør sendes fra en konto som ikke er knyttet til en faktisk bruker. Du kan derfor ikke velge **Gjeldende bruker**-kontotypen. Hvis du gjør det, sendes ikke varslinger. 

Over tid vil listen over oppføringer på siden **Overvåkede feltloggposter** bli større. Hvis du vil redusere antall oppføringer, kan du opprette en oppbevaringspolicy som sletter poster etter en bestemt tidsperiode. Hvis du vil ha mer informasjon, kan du se [Definere oppbevaringspolicyer](admin-data-retention-policies.md).

Når du definerer feltovervåking eller endrer noe i oppsettet, opprettes det poster for endringene. Du kan angi om du vil vise poster som er knyttet til overvåkningsoppsettet, ved å vise eller skjule dem. 

Du kan behandle innstillinger for feltovervåking, for eksempel om du vil sende en e-postvarsling eller bare logge endringen, for hvert felt på siden **Regneark for overvåkede felt**. Siden er også der du kan legge til eller fjerne felt som skal overvåkes.

> [!NOTE]
> Når du har lagt til ett eller flere felt og starter overvåkingen, må du logge av [!INCLUDE[prod_short](includes/prod_short.md)] og på igjen for å kunne bruke innstillingene.

### <a name="work-with-field-monitoring"></a>Arbeid med feltovervåking

Oppføringer for alle endrede verdier for overvåkede felt er tilgjengelige på siden **Overvåkede feltloggposter**. Oppføring inneholder for eksempel følgende informasjon:

* Feltet som verdien ble endret for.
* De opprinnelige og nye verdiene.
* Hvem som foretok endringen, og når den ble gjort. 

Du kan undersøke en endring ytterligere ved å velge en verdi for å åpne siden den ble gjort på. Hvis du vil se en oversikt over alle postene, velger du **Feltendringsposter**.

### <a name="viewing-field-monitoring-telemetry"></a>Vise telemetri for feltovervåking

Du kan konfigurere at [!INCLUDE[prod_short](includes/prod_short.md)] sender feltovervåkingsaktivitet til en Application Insights-ressurs i Microsoft Azure. Deretter kan du bruke Azure Monitor til å opprette rapporter og konfigurere varsler for de innsamlede dataene. Hvis du vil ha mer informasjon, kan du se følgende artikler i Hjelp for utviklere og IT-eksperter for [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Overvåke og analysere telemetri – aktivere Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Analysere telemetri for feltovervåking](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a>Definere oppbevaringspolicyer

Du kan opprette oppbevaringspolicyer for å slette unødvendige data i logger etter en angitt tidsperiode. Antall poster i en logg kan for eksempel øke over tid. Ved å rydde opp i gamle poster kan du gjøre det enklere å fokusere på nyere, og sannsynligvis mer relevante poster. Hvis du vil ha mer informasjon, kan du se [Definere oppbevaringspolicyer](admin-data-retention-policies.md).

## <a name="see-also"></a>Se også

[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Sortere, søke etter og filtrere](ui-enter-criteria-filters.md)  
[Finne sider og informasjon med Fortell meg](ui-search.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definere oppbevaringspolicyer](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
