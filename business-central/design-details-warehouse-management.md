---
title: Administrer lageraktiviteter
description: I tillegg til mottak og leveringer støtter Business Central en rekke interne lageraktiviteter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/13/2023
ms.custom: bap-template
---

# Oversikt over lagerstyring

Det er to ting som er viktige for alle virksomheter som fysisk flytter varer inn og ut av lageret:

* De har en oversikt over lagernivåer og vareplassering i lageret.
* De kan raskt og enkelt motta, plukke og levere varer.

For å hjelpe bedrifter med å oppnå disse tingene legger lagerfunksjoner i [!INCLUDE[prod_short](includes/prod_short.md)] til følgende funksjoner i lagerstyring:

* Hyller
* Lagerleveringer
* Lagerplukk
* Flytteforslag

Implementer disse funksjonene i ulike kombinasjoner for å skreddersy lagerprosessene for bedriften. Gjør det mulig å øke kompleksiteten etter hvert som selskapet vokser og prosessene endres.

## Oversikt over ulike konfigurasjonsalternativer

Du kan konfigurere lagerfunksjoner på ulike måter. Det er viktig at du velger alternativene som forbedrer prosessene uten å forårsake indirekte kostnader. Tabellen nedenfor gir en oversikt over typiske konfigurasjoner for å håndtere fysiske varer.

|Kompleksitetsnivå|Description|Innstillinger|Hyllekode|Eksempel på inngående flyt|Eksempel på utgående flyt|Eksempel på intern flyt|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen dedikert lageraktivitet.|Bokfør fra ordrer og kladder.||Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Bestilling|Ordre| Produksjonsordre -> Forbrukskladd|  
|Grunnleggende|Konsolidert mottak/levering for flere ordrer.|**Mottak nødv.**<br>**Levering nødv.**|Valgfritt. Kontrollert av vekslebryteren Hyllekode er obligatorisk|Bestillinger -> Lagermottak|Ordre -> Lagerlevering|Samme som ovenfor.|
|Grunnleggende|Ordre for ordre.|Plukk nødv. eller Mottak nødv. </br><br/> **Obs**! Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter på lokasjoner der du velger disse avmerkingsboksene.|Valgfritt. Kontrollert av vekslebryteren **Hyllekode er obligatorisk**.|Bestilling -> Lagerplassering|Ordre -> Lagerplukk|Produksjonsordre-> Lagerplukk|
|Avansert|Konsolidert mottak/levering for flere ordrer.<br /><br />Konsoliderte plukk-/plasseringsaktiviteter for flere kildedokumenter.|Mottak nødv. + Plukk nødv.</br> Forsendelse nødv. + Plukk nødv.|Valgfritt. Kontrollert av vekslebryteren Hyllekode er obligatorisk|Bestillinger -> lagermottak -> lagerplassering|Ordrer -> lagerleveringer -> plukkforslag -> lagerplukk| Produksjonsordre -> Plukkforslag -> Lagerplukk -> Forbrukskladd|
|Avansert|Samme som over + lagerstyringsaktiviteter|Lagerstyring (avhengig av vekslebrytere aktiveres automatisk)|Obligatorisk|Samme som ovenfor.|Samme som ovenfor.| Produksjonsordre -> Plukkforslag -> Lagerplukk Forbrukskladd|

Kompleksiteten øker med størrelsen på organisasjonen og hvor mange avdelinger og personer som er involvert. En prosess kan være enkel, for eksempel når den samme personen oppretter og bokfører et salgsdokument. Prosesser kan også være mer komplekse og involvere flere trinn og personer. Følgende trinn er et eksempel på en mer komplisert prosess:

1. En ordrebehandler oppretter en ordre.
1. En lagersjef oppretter plukkinstruksjoner.
1. En lagermedarbeider fullfører flyten ved å bokføre lagerleveringen.

Kompleksiteten påvirkes også av dokumenttypene du bruker i lageraktivitetene. Du kan for eksempel bruke lagermottaks- og lagerplasseringsdokumenter for inngående flyt, men bruke lagerplukkdokumenter for utgående flyt.

En annen faktor som påvirker kompleksiteten, er hvordan det fysiske lageret er representert i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Modellering av det fysiske lageret](#modeling-the-physical-warehouse).

## Modellering av det fysiske lageret

Du har flere alternativer for å representere det virkelige oppsettet av lageret i [!INCLUDE[prod_short](includes/prod_short.md)]. Valgene bestemmer hvordan du arbeider med lagerfunksjoner.

Plasseringen av varer kan være hyller og lokasjoner, og det finnes fordeler og ulemper for hvert alternativ.

### Lokasjoner og hyller

Du må ha minst én lokasjon for å kunne håndtere fysiske varer. Du kan bruke flere lokasjoner eller bruke hyller for å modellere lageret og organisasjonsstrukturen.

Lokasjoner er vanligvis den beste måten å organisere operasjoner på på tvers av geografiske områder. I noen tilfeller vil du imidlertid kanskje opprette flere lokasjoner som befinner seg på samme sted. Bruk av lokasjonene har følgende fordeler:

* Gi tilgang ved hjelp av sidene **Lagermedarbeider** og **Ansvarssentre** .
* Definer kalendere, ruter og inngående og utgående håndteringstider for datoberegning og planlegging. Finn ut mer under [Om planleggingsfunksjonaliteten](production-about-planning-functionality.md).
* Angi standarddimensjoner og bruke ulike lagerbokføringsoppsett.
* Konfigurer planleggingsparametere. Finn ut mer under [Planleggingsparametere](production-about-planning-functionality.md#planning-parameters).  
* Bruk forskjellige lagerfunksjoner for hver lokasjon.

### Hyller

Hvis du alltid lagrer en vare på samme sted, kan du bruke feltet **Hyllenr.** på sidene **Varekort** eller **Lagerføringsenhetskort**. Dette feltet kan være et grunnleggende manuelt lagringssystem i miljøer uten hyller. Verdien i feltet kopieres fra varekortet til dokumentlinjene og -rapportene, men det er bare til informasjon. Verdien brukes ikke i lageraktiviteter eller tilgjengelighetsberegninger.

Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer:

* En eller flere faste hyller for en vare.
* Hyller for bestemte operasjoner, for eksempel en leveringshylle eller en produksjonsavgangshylle.
* Hyllekapasitet og vektbegrensninger (bare for lagerstyring).
* Hyllerangering (bare for lagerstyring).

## Vanlig arbeidsflyt for lager

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|I en enkel flyt på en ordre-for-ordre-basis, bruker du en lagerplassering for å registrere mottak av varer på lokasjoner, inkludert overmottak. Hvis du konsoliderer flere ordrer i mottaket, bruker du et lagermottak.|[Inngående flyt](design-details-inbound-warehouse-flow.md)|
|Registrer leveringen av varer fra lagerlokasjoner. Bruk en lagerplukk på ordre-for-ordre-basis. Hvis du konsoliderer flere ordrer i leveringen, bruker du et lagerlevering.|[Utgående flyt](design-details-outbound-warehouse-flow.md)|
|Håndter varer innenfor lagerlokasjonen. Når du for eksempel flytter komponenter til produksjon eller utfører en vareopptelling.|[Intern flyt](design-details-internal-warehouse-flows.md)|

Definer lagerprosessene som passer til din virksomhet. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

## Terminologi relatert til lagerstyring

### Kompleksitetsnivåer

Vi bruker termene «enkel» og «avansert» til å skille mellom kompleksitetsnivåer. Denne enkle differensieringen dekker flere kompleksitetsnivåer i lokasjonsoppsett, der hvert nivå støttes av ulike lagerdokumenter. Det mest avanserte nivået for lagerstyring kalles «Lagerstyring». Hvis du vil bruke lagerstyring for en lokasjon, må du aktivere **Lagerstyring** på siden **Lokasjonskort**.

### Lagerflyter

* Inngående flyt – Flytt varer på lagerlokasjonen og gjør dem tilgjengelig, for eksempel innkjøp og inngående overføringer.
* Utgående flyt – plukk og lever varer til kunder eller andre lokasjoner.
* Intern flyt – håndter varer innenfor en lokasjon. Flytt for eksempel komponenter til produksjon eller utfør vareopptelling.

### Grunnleggende dokumenter  

Følgende dokumenter brukes i enkle lagerflyter.

* Lagerplassering
* Lagerplukk
* Lagerflytting
* Varekladd
* Varereklassifiseringskladd

### Avanserte dokumenter  

Følgende dokumenter brukes i avanserte lagerflyter.

* Lagermottak
* Plasseringsforslag
* Plassering
* Plukkforslag
* Plukk
* Flytteforslag
* Lagerflytting
* Intern lagerplukk
* Intern lagerplassering
* Hylleoppretting
* Hylleinnholdopprett. - forslag
* Lagervarekladd
* Varereklassifiseringskladd for lager

### Sider og innstillinger

Denne delen beskriver begrepene bak nøkkelsidene og innstillingene for lagerstyring.

#### Hyller og hylleinnhold

En hylle er en lagringsenhet som er utformet for å inneholde atskilte deler. Dette er den minste beholderenheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Vareantall i hyller kalles *hylleinnhold*. Et oppslag fra **Vare**-feltet eller **Hyllekode**-feltet på en hvilken som helst lagerrelatert dokumentlinjen viser beregnet tilgjengeligheten for varen på hyllen.  

Hylleinnhold kan være **Fast**, **Dedikert** eller **Standard** for å angi hvordan hylleinnholdet skal brukes. Hyller med ingen av disse egenskapene kalles *flytende* hyller.  

En fast hylle kan inneholde elementer som er tilordnet til hyllekoden. Egenskapen Fast hylle sikrer at hylleinnholdet ikke forsvinner selv om hyllen tømmes. Du kan velge hyllen igjen så snart innholdet er etterfylt.  

En dedikert hylle inneholder hylleinnhold som bare kan plukkes for dedikert ressurs som bruker hyllen. Det kan for eksempel være en produksjonsressurs. Annet ikke-plukkinnhold, for eksempel antall utgående på en leveringsbokføring, kan brukes fra en dedikert hylle. Bare hylleinnhold som **Opprett plukk**-algoritmen tar hensyn til er beskyttet i en dedikert hylle.  

[!INCLUDE [prod_short](includes/prod_short.md)] bruker hylleegenskap **Standard** til å foreslå hyller for lageraktiviteter. På lokasjoner som bruker lagerstyring, brukes ikke Standard-hylleegenskapen. På steder der det kreves hyller, angir egenskapen hvor varer skal plasseres i inngående flyter. I utgående flyter angir egenskapen hvor varer skal plukkes fra.  

> [!NOTE]  
> Hvis utgående varer er plassert i flere hyller, blir varer først plukket fra ikke-standard hyllene for å tømme dette hylleinnholdet, og deretter blir resten av varene plukket fra standardhyllen.  

Du kan bare ha én standardhylle per vare per lokasjon.  

#### Hylletype

Lokasjoner som bruker lagerstyring, kan bruke hylletyper. Hylletyper styrer aktivitetene du tillater for en hylle. 

Følgende hylletyper er tilgjengelige:  

|Hylletype|Beskrivelse|  
|------------------|---------------------------------------|  
|MOTTA|Varer som er mottatt, men ikke plassert.|  
|SHIP|Varer som er plukket for lagerleveringslinjer, men som ikke er bokført som levert.|  
|PUT AWAY|Vanligvis varer som skal lagres i store enheter, men som du ikke vil opprette tilgang til for plukking. Disse hyllene brukes ikke til plukking, enten for produksjonsordrer eller leveringer, så bruken av disse kan være begrenset. Denne typen hylle er nyttig når du kjøper et stort antall varer. Hyllene må alltid ha en lav hylleprioritering, slik at varer med høyere prioriterte PLASSPLUKK-hyller plasseres først. Etterfyll denne typen hylle regelmessig slik at varene er tilgjengelige i PLASSPLUKK- eller PLUKK-hylletyper.|  
|PLUKK|Varer som bare skal brukes til plukk. Du kan bare bruke flyttinger til å etterfylle disse hyllene, ikke plasseringer.|  
|PUTPICK|Varer i hyller som er foreslått både for plasseringer og plukk. Hyller av denne typen har forskjellige hylleprioriteringer. Sett opp masselagringshyllene med lavere hylleprioriteringer enn vanlige plukkhyller eller hyller i forhåndsplukkingsområder.|  
|KK|Denne hyllen brukes til lagerjusteringer hvis du angir denne hyllen på lokasjonskortet i feltet **Hyllekode for justering**. Du kan også sette opp hyller av denne typen for defekte varer og varer som blir kontrollert. Du kan flytte varer til denne typen hylle hvis du vil gjøre dem utilgjengelig for den vanlige vareflyten. **Obs!** I motsetning til alle andre hylletyper er det ikke merket av for noen av varehåndteringsalternativene for **KK**-hylletypen som standard. Innholdet du plasserer i en KK-hylle, er utelukket fra vareflyter.|  

Du kan velge å bruke alle de åtte mulige hylletypene i lageret, eller du kan velge å bruke bare hylletypene MOTTAK, PLASSPLUKK, LEVERING og KK. Med disse fire hylletypene kan det gis forslag som støtter flyten, og du kan registrere beholdningsavvik.
Med unntak av typene PLUKK, PLASSPLUKK og PLASSERING, definerer hylletypen hvilken type aktivitet som er tillatt for en hylle. Du kan for eksempel bare bruke en MOTTAK-hylletype til å motta varer eller plukke varene fra.  

> [!NOTE]  
> Du må bruke flyttinger til å flytte varer for MOTTAK- og KK-hyller. På samme måte kan du bruke flyttinger til å flytte varer fra LEVER- og KK-hyller.  

#### Hylleprioritering

I avanserte lagerstyring kan du automatisere og optimalisere hvordan du samler inn varer på plassering og plukkforslag ved rangering av hyllene. Varene foreslås for plukking og plasseringer basert på hylleprioritet.

Plasseringsprosesser er optimalisert i henhold til hylleprioriteringen ved å foreslå høyt prioriterte hyller før lavt prioriterte hyller. Plukkprosessen foreslår varer fra hylleinnhold med høy hylleprioritering først. Hylleetterfylling foreslår fra lavere hyller før høyere prioriterte hyller.  

Hylleprioritering og hylleinnhold er de grunnleggende egenskapene som veileder lagermedarbeidere i lageret.  

#### Hylleoppsett

I avansert lagerstyring kan du angi følgende kapasitetsverdier når du skal styre hvordan og i hvilke hyller du lagrer varer:

* Antall
* Totalt kubikkinnhold
* Vekt  

Du kan tildele en grunnleggende enhet (UOM) til varer. En grunnleggende UOM kan være stykk, paller, liter, gram eller esker. Du kan også opprette større UOM-er basert på grunnleggende UOM. Hvis for eksempel stykk er en grunnleggende UOM, kan en pall være lik 16 stykker.  

Hvis en vare har mer enn én UOM, angir du maksimumsantallet for hver UOM på varekortet. Hvis du håndterer en vare i stykker og paller, må feltet **Maks. ant.** på siden **Hylleinnhold** for denne varen også være i stykker og paller. Hvis ikke blir ikke det tillatte antallet for hyllen beregnet på riktig måte.  

Før du angir begrensninger for kapasitet for hylleinnhold på en hylle, må du kontrollere at varens enhet og dimensjoner er angitt på varen.  

> [!NOTE]  
> Du kan bare bruke flere UOM.er på lokasjoner som bruker lagerstyring. I alle andre konfigurasjoner kan du bruke hylleinnhold i grunnleggende UOM. Antallet konverteres til grunnenhet for alle transaksjoner med UOM som er større enn varens grunnleggende UOM.  

#### Sone

I avanserte lagerstyring kan hyller grupperes i soner for å styre hvordan arbeidsflyten er i lageraktiviteter for lokasjoner.  

En sone kan være en mottakssone eller en lagringssone, og hver sone kan bestå av én eller flere hyller.  

De fleste egenskapene som er tildelt til en sone, tildeles til hyllene som er opprettet for sonen.  

#### Lagerklasse

I avansert lagerstyring kan du tildele lagerklassekoder til følgende enheter: 

* Varer
* Hyller
* Soner

Lagerklasser kontrollerer hvor varene skal lagres. Du kan dele opp en sone i flere lagerklasser. Du kan for eksempel lagre varer i mottakssonen som frosset, farlige eller en annen klasse.

Når du arbeider med lagerklasser og en standard mottaks-/leveringshylle, må du velge de aktuelle hyllene på lagermottaks- og lagerfølgeseddellinjene manuelt.  

I inngående flyter utheves lagerklassekoden bare på innkommende linjer der vareklassekoden ikke samsvarer med standard mottakshylle. Hvis riktige standardhyller ikke tildeles, kan ikke antallet mottas.  

#### Lokasjon

En lokasjon er en fysisk struktur eller et sted der lager mottas, lagres og leveres. En lokasjon kan være et lager, en servicebil, utstillingsrom, anlegg eller et område på et anlegg. Lageret er ofte organisert i hyller og soner.

#### Først utløpt, først ut (FEFO)

Hvis du merker av for **Plukk i henhold til FEFO** for hurtigfanen **Hylleprinsipp** på siden **Lokasjonskort**, blir varesporede varer plukket på lokasjonen i henhold til utløpsdatoen. Varene med de tidligste utløpsdatoene plukkes først.  

Lageraktiviteter i alle plukke- og flyttedokumenter sorteres i henhold til FEFO, med mindre varene har fått tilordnet serie- eller partinumre. Hvis noen, men ikke alle, av antallet på linjen er tilordnet vare- eller partinumre, brukes FEFO til å sortere det gjenstående antallet.  

Når det plukkes etter FEFO, samles varer som utløper først, i en midlertidig varesporingsliste basert på utløpsdato. Hvis to varer har samme utløpsdato, blir varen med lavest parti- eller serienummer valgt først. Hvis parti- eller serienumrene er like, blir varen som ble registrert først, valgt først. Standardkriterier for å velge varer i plukkhyller, for eksempel Hylleprioritering eller Anbrekk, brukes på den midlertidige FEFO-varesporingslisten.  

#### Plasseringsmal

Plasseringsmalen angir et sett med prioriterte regler som gjelder når du oppretter plasseringer. En plasseringsmal kan for eksempel kreve at du plasserer varer på en hylle med hylleinnhold med samme enhet. Hvis en lignende hylle med tilstrekkelig kapasitet ikke blir funnet, må varen plasseres i en tom hylle. Du tildeler en plasseringsmal til en vare og en lokasjon.  

## Se også

[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
