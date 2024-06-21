---
title: 'Utformingsdetaljer: Sentrale begreper for planleggingssystemet'
description: Planlegging foreslår handlinger som brukeren kan utføre basert på behovs-/forsyningssituasjonen og varenes planleggingsparametere.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Utformingsdetaljer: Sentrale begreper for planleggingssystemet

Planleggingsfunksjonene er i et satsprosjekt som først velger de aktuelle varene og perioden som skal planlegges. Deretter kaller kjørselen en kodeenhet som beregner en forsyningsplan, i henhold til varens lavnivåkode (stykklisteplassering). Kodeenheten balansene tilbud-etterspørsel-sett og foreslår handlinger som brukeren skal utføres. De foreslåtte handlingene vises som linjer i planleggingsforslaget eller bestillingsforslaget.  

![Innhold på Planleggingsforslag-siden.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Innhold på Planleggingsforslag-siden")  

Planleggeren i et selskap, for eksempel en innkjøper eller en produksjonsplanlegger, antas å være brukeren av planleggingssystemet. Planleggingssystemet hjelper brukeren ved å utføre omfattende, men heller enkle, beregninger av en plan. Brukeren kan dermed konsentrere seg om å løse vanskeligere problemer, for eksempel når ting avviker fra det som er vanlig.  

Planleggingssystemet drives av forventet og faktisk kundebehov, for eksempel prognose og ordrer. Planleggingsberegninger foreslår handlinger du kan utføre når du leverer fra leverandører, montering eller produksjon eller overføringer fra andre lagre. Et eksempel på en foreslått handling kan være opprettelse av nye forsyningsordrer, for eksempel bestillinger og produksjonsordrer. Hvis det allerede finnes forsyningsordrer, kan de foreslåtte handlingene være å øke eller påskynde ordrene for å dekke endringene i behovet.  

Et annet mål med planleggingssystemet er å sikre at beholdningen ikke vokser unødvendig. Hvis behovet avtar, foreslår systemet at brukeren utsetter, reduserer antallet i eller annullerer eksisterende forsyningsordrer.  

En kodeenhet inneholder en planleggingslogikk og følgende funksjoner:

* MRP og MPS
* Beregn bevegelsesplan
* Beregn replanlegging

Forsyningsplanberegningen omfatter imidlertid forskjellige undersystemer.  

Planleggingssystemet inneholder ikke dedikert logikk for kapasitetsutjevning eller finplanlegging. Disse typene planleggingsarbeid utføres separat. Mangelen på direkte integrasjon mellom de to områdene betyr også at omfattende kapasitets- eller planendringer krever at du kjører planleggingen på nytt.  

## Planleggingsparametere

Planleggingsparametere som du angir for en vare eller varegruppe, styrer hvilke handlinger planleggingssystemet foreslår i ulike situasjoner. Definer planleggingsparametere for hver vare for å kontrollere når etterfyllingen skal gjøres, hvor mye som skal etterfylles, og hvordan etterfyllingen skal gjøres.  

Du kan også definere planleggingsparametere kan også angis for en hvilken som helst kombinasjon av vare, variant og lokasjon, ved å konfigurere en lagerføringsenhet for hver kombinasjon og deretter angi individuelle parametere. Finn ut mer under [Utformingsdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) og [Utformingsdetaljer: Planleggingsparametere](design-details-planning-parameters.md).  

## Planlegge startdato

Planleggingssystemet hjelper deg med å unngå at åpne ordrer i tidligere og foreslåtte handlinger ikke er mulige. Planlegging behandler alle datoer før startdatoen som en låst sone. Følgende regel gjelder den frosne sonen:  

* Alle tilbud og etterspørsel før startdatoen for planleggingsperioden betraktes som en del av beholdningen eller levert. Det antar med andre ord at planen for fortiden kjøres i henhold til den angitte planen. Finn ut mer under [Behandle ordrer før den planlagte startdatoen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Dynamisk sporing (utligning)

Dynamisk sporing og samtidige opprettingen av handlingsmeldinger i planleggingsforslaget er ikke en del av forsyningsplanleggingssystemet. Når et behov eller en forsyning opprettes eller endres, kobler dynamisk ordrespring behovet og antallene for å dekke det i sanntid.  

Hvis du for eksempel angir eller endrer en ordre, vil dynamisk sporing umiddelbart søke etter passende forsyning. Forsyningen kan være fra lager eller en forventet forsyningsordre (for eksempel en bestilling eller en produksjonsordre). Når det finner en forsyningskilde, kobler [!INCLUDE [prod_short](includes/prod_short.md)] til behovet og forsyningen. Du får tilgang til koblingen på sider med bare visning fra dokumentlinjene. Når forsyning ikke blir funnet, oppretter det dynamiske sporingssystemet handlingsmeldinger i planleggingsforslaget med forsyningsplanforslag.  

Dynamisk sporing hjelper deg med å vurdere om du vil godta forslag til forsyningsordrer. Fra forsyningssiden viser den behovet som opprettet forsyningen. Fra behovssiden viser den forsyningen som skal dekke behovet.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Eksempel på dynamisk sporing.":::

Finn ut mer [Utformingsdetaljer: Reservasjon, sporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).  

I selskaper med en lav vareflyt og mindre avanserte produktstrukturer kan det være nok å bruke dynamisk sporing for forsyningsplanlegging. I travle miljøer bør planleggingssystemet imidlertid brukes til å sikre at finnes en riktig balansert forsyningsplan.  

### Dynamisk sporing kontra planleggingssystemet

Det kan være vanskelig å skille mellom planleggingssystemet og dynamisk sporing. Begge funksjonene viser utdata i planleggingsforslaget ved å foreslå handlinger som planleggeren bør utføre. Utdataene blir imidlertid produser på en annen måte.  

Planleggingssystemet håndterer hele forsynings- og behovsmønsteret for en vare. Det anser alle nivåene i stykklistehierarkiet langs tidslinjen. Dynamisk sporing behandler bare situasjonen i rekkefølgen som aktiverte den. Ved balansering av behov og forsyning oppretter planleggingssystemet koblinger i en brukeraktivert satsvis modus. Dynamisk sporing oppretter koblingene automatisk når du angir et behov eller en forsyning. Når du for eksempel oppretter en ordre eller en bestilling.  

Dynamisk sporing kobler behov og forsyning når data registreres, basert på det som kommer først. Dette grunnlaget kan føre til uorden i prioriteter. Det kan for eksempel være at en ordre som er registrert først med en forfallsdato neste måned, knyttes til forsyningen i lageret. Neste ordreforfallsdato i morgen kan forårsake en handlingsmelding for å opprette en ny bestilling for å dekke den. Bildet nedenfor viser dette scenarioet.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Eksempel på sporing i forsyningsplanlegging 1.":::

Planleggingssystemet håndterer behov og forsyning for varer i en prioritert rekkefølge. Ordren prioriteres i henhold til forfallsdatoer og ordretyper. Det vil si i en først-nødvendig-første-betjent-basis. Den sletter alle sporingskoblinger som ble opprettet dynamisk, og etablerer dem på nytt i henhold til forfallsdatoprioritet. Når planleggingssystemet har kjørt, har det løst all ubalanse mellom behov og forsyning, som vist nedenfor for de samme dataene.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Eksempel på sporing i forsyningsplanlegging 2.":::  

Når du har kjørt planleggingen, inneholder ikke tabellen Handlingsmeldingspost noen handlingsmeldinger. Disse meldingene erstattes av handlingene som er foreslått i planleggingsforslaget. Finn ut mer under [Sporingskoblinger under planlegging](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## Rekkefølge og prioritet i planlegging

Sekvensen på beregningene i planen er viktig for å få prosjektet gjort innen rimelig tid. Prioriteringen av krav og ressurser spiller også en viktig rolle for å få de beste resultatene.  

Planleggingssystemet drives av behov. Varer på høyt nivå må planlegges før vare på lavt nivå, fordi de kan generere ekstra behov for varene på lavere nivå. Planlegg for eksempel detaljhandelslokasjoner før distribusjonssentre fordi detaljhandelslokasjonen kan inneholde behov fra distribusjonssenteret. På et detaljert balansenivå hvis en frigitt forsyningsordre kan dekke en ordre, skal ikke systemet opprette en ny forsyningsordre. En forsyning med et bestemt partinummer skal ikke tildeles for å dekke et generelt behov hvis et annen behov krever dette bestemte partiet.  

### Varens prioritet/lavnivåkode

Behovet for en ferdig og salgbare vare i et produksjonsmiljø, vil føre til avledede behov for komponenter som utgjør den ferdige varen. Stykklistestrukturen kontrollerer komponentstrukturen og kan dekke flere nivåer av halvferdige varer. Planlegging av en vare på ett nivå vil føre til et avledede behov for komponenter på det neste nivået. Dette hierarkiet fører til slutt til avledet behov for kjøpte varer. Planleggingssystemet planlegger for varer i prioritert rekkefølge i det samlede stykklistehierarkiet. Systemet starter med fullførte salgbare varer på øverste nivå, og fortsetter ned produktstrukturen til varer på lavere nivå (i henhold til lavnivåkoden).  

Bildet nedenfor viser rekkefølgen som [!INCLUDE [prod_short](includes/prod_short.md)] foreslår forsyningsordrer i på øverste nivå. Det antar at forslagene ble godkjent, og viser også varer på lavere nivå.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planlegge for stykklister.":::

Hvis du vil finne ut mer om produksjonshensyn, kan du gå til [Laste inn lagerprofiler](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Optimere ytelse for lavnivåberegninger

Beregninger av lavnivåkode kan påvirke systemytelsen. Hvis du vil redusere innvirkningen, kan du slå av vekslebryteren **Dynamisk beregning av lavnivåkode** på **Produksjonsoppsett**-siden. Når du gjør det, foreslår [!INCLUDE[prod_short](includes/prod_short.md)] at du oppretter en gjentakende prosjektkøpost som oppdaterer lavnivåkoder daglig. Du kan sikre at jobben vil kjøre utenom arbeidstiden ved å angi et starttidspunkt i feltet **Tidligste startdato/-klokkeslett**.

Du kan også få fart på beregninger av lavnivåkoder ved å slå på vekslebryteren **Optimaliser beregning av lavnivåkode** på siden **Produksjonsoppsett**.

> [!IMPORTANT]
> Hvis du velger å optimalisere ytelsen, vil [!INCLUDE[prod_short](includes/prod_short.md)] bruke nye beregningsmetoder til å bestemme lavnivåkoder. Hvis du har en utvidelse som er avhengig av hendelsene som brukes av de gamle beregningene, kan det hende at utvidelsen slutter å virke.

### Lokasjoner / prioritet for overføringsnivå

Selskapet med mer enn én lokasjon må kanskje planlegge individuelt for hver enkelt lokasjon. Sikkerhetslagernivået og gjenbestillingsprinsippet for en vare kan for eksempel være forskjellig på ulike lokasjoner. Du må angi planleggingsparameterne per vare og lokasjon.  

Du kan bruke lagerføringsenheter til å angi individuelle planleggingsparametere. En SKU kan betraktes som en vare på en bestemt plassering. Hvis du ikke har definert en lagerføringsenhet for lokasjonen, bruker [!INCLUDE [prod_short](includes/prod_short.md)] parameterne som er angitt på varekortet. [!INCLUDE [prod_short](includes/prod_short.md)] beregner en plan bare for aktive lokasjoner, som er der det finnes behov eller forsyning for en angitt vare.  

Alle varer kan håndteres på en hvilken som helst lokasjon, men [!INCLUDE [prod_short](includes/prod_short.md)] har en streng tilnærming til konseptet for lokasjon. En ordre for en vare på én lokasjon kan for eksempel ikke oppfylles av lager fra en annen lokasjon. Antallet på lager må først overføres til lokasjonen som er angitt i ordren.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planlegge for lagerføringsenheter.":::

Finn ut mer under [Utformingsdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md).  

### Bestillingsprioritet

I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i de neste dagene. Bortsett fra denne typen prioritet blir ulike behovs- og forsyningstyper sortert i henhold til viktighet i virksomheten for å avgjøre hvilke behov som må oppfylles først. På forsyningssiden bestemmer ordreprioriteten kilden for forsyning som skal brukes først. Finn ut mer under [Prioritering av ordrer](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Behovsprognoser og rammeordrer

Både prognoser og rammeordrer representerer forventet behov. Rammeordren, som dekker kjøp en kunde har tenkt å foreta i en bestemt tidsperiode, er med på å redusere usikkerheten ved den samlede prognosen. Rammeordren er en kundespesifikk prognose oppå den uspesifiserte prognosen som illustreres i følgende bilde.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planlegging med prognoser.":::

Finn ut mer under [Prognosebehov blir redusert av ordrer](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Planleggingstilordning

Alle varer må planlegges på nytt for når behovs- eller forsyningsmønsteret er endret siden forrige gang en plan ble beregnet. Hvis du for eksempel angir en ny ordre eller endrer en eksisterende, må du beregne planen på nytt. Andre årsaker for ny planlegging inkluderer en endring i prognosen eller sikkerhetslagerantall. Endring av en stykkliste ved å legge til eller fjerne en komponent, vil mest sannsynlig indikerer også en endring, men bare for komponentvaren.  

Planleggingssystemet overvåker slike hendelser og tilordner de riktige varene for planlegging.  

For flere lokasjoner skjer tildelingen på varenivået per lokasjonskombinasjon. Hvis det er opprettet en ordre på bare én lokasjon, vil [!INCLUDE [prod_short](includes/prod_short.md)] tildele varen på denne lokasjonen for planlegging.  

Grunnen til å velge varer for planlegging har å gjøre med systemytelsen. Hvis en vares behov-/ forsyningsmønster ikke er endret, vil ikke planleggingssystemet foreslå handlinger som skal utføres. Uten planleggingstilordningen måtte systemet ha utført beregningene for alle varer for å finne ut hva det skal planlegge for. Hvis du vil finne ut mer om årsakene for å tildele varer for planlegging, kan du gå til [Utformingsdetaljer: Tabell for planleggingstildeling](design-details-planning-assignment-table.md).  

Følgende er planleggingsalternativene som er tilgjengelige:  

* **Beregn replanlegging** beregner alle valgte varer, om det er nødvendig eller ikke.  
* **Beregn bevegelsesplan** beregner bare varene som har hatt en endring i behovs- og forsyningsmønsteret og derfor er tildelt for planlegging.  

Noen personer mener at bevegelsesplanlegging bør utføres raskt når som helst, for eksempel når ordrer registreres. Planlegging på farten kan imidlertid være forvirrende fordi dynamisk ordresporing og handlingsmeldinger også beregnes direkte. [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr sanntidskontroll for tilgjengelig for ordre. Det gir popup-advarsler når du angir ordrer og nåværende forsyningsplan ikke oppfyller behovet.  

Planleggingssystemet planlegger bare for varene du har klargjort med riktige planleggingsparametere. Hvis ikke antar det at du skal planlegge varene manuelt eller halvautomatisk ved hjelp av funksjonen for ordreplanlegging. Hvis du vil finne ut mer om automatiske planleggingsprosedyrer, kan du gå til [Utformingsdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md).  

## Varedimensjoner

Behov og forsyning kan omfatte variant- og lokasjonskoder som må respekteres når planleggingssystemet balanserer behov og forsyning.  

[!INCLUDE [prod_short](includes/prod_short.md)] behandler variant- og lokasjonskoder som varedimensjoner på en salgsordrelinje, lagerpost og så videre. Det beregner derfor en plan for hver kombinasjon av variant og lokasjon som om kombinasjonen var et eget varenummer.  

I stedet for å beregne teoretiske kombinasjoner av variant og lokasjon, beregner [!INCLUDE [prod_short](includes/prod_short.md)] kombinasjonene som faktisk finnes i databasen. Hvis du vil finne ut mer om hvordan planleggingssystemet håndterer lokasjonskoder på forespørsel, kan du gå til [Utformingsdetaljer: Behov på tom lokasjon](design-details-balancing-demand-and-supply.md)..  

## Vareattributter

Varer har ofte generelle attributter, for eksempel varenummer, variantkode, lokasjonskode og ordretype. Hver behovs- og forsyningshendelse kan imidlertid ha andre spesifikasjoner, for eksempel serie- eller partinumre. Planleggingssystemet planlegger disse attributtene på bestemte måter som avhenger av spesifikasjonsnivået deres.  

En ordre-til-ordre-kobling mellom behov og forsyning er en annen attributtype som påvirker planleggingssystemet. Finn ut mer under [Ordre-til-ordre-koblinger](#order-to-order-links).

### Bestemte attributter

Noen behovsattributter er spesifikke, og en forsyning må være identiske med hverandre.

* Serie- eller partinumre som krever bestemt program (disse attributtene kreves hvis du slår på vekslebryteren **Sporing basert på s.nr.** eller **Sporing basert på parti** på **Kort for varesporingskode**-siden for varesporingskode som brukes av varen.)  
* Koblinger til forsyningsordrer som er opprettet manuelt eller automatisk for et bestemt behov (ordre-til-ordre-koblinger).  

Planleggingssystemet bruker følgende regler for disse attributtene:  

* Behov med bestemte attributter kan bare oppfylles av forsyning med tilsvarende attributter.  
* Forsyning med bestemte attributter kan også dekke behov som ikke spesifikt krever disse attributtene.  

Hvis lager eller anslåtte forsyninger ikke kan oppfylles et behov for bestemte attributter, foreslår planleggingssystemet en ny forsyningsordre uten å ta hensyn til planleggingsparametere.  

### Ikke-spesifikke attributter

Serie- eller partinummererte varer uten et bestemt varesporingsoppsett kan ha ikke-spesifikke serie- eller partinumre. Denne typen numre kan brukes på alle serie- eller partinumre. Planleggingssystemet har større frihet til for eksempel å knytte et serialisert behov til en serialisert forsyning, vanligvis på lageret.  

Behov-forsyning med serie- eller partinumre, spesifikk eller ikke-spesifikk, er høyt prioritet og er fritatt fra den frosne sonen. De er en del av planleggingen selv om de forfaller før planleggingsstartdatoen. Finn ut mer under [Serie- og partinumre lastes inn etter spesifikasjonsnivå](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Hvis du vil finne ut mer om hvordan planleggingssystemet balanserer attributter, kan du gå til [Serie- og partinumre og ordre-til-ordre-koblinger er fritatt fra den forrige perioden](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Odre-til-ordre-koblinger

Ordre-til-ordre betyr at du kjøper, monterer eller produserer en vare for et bestemt behov. Du kan velge denne policyen på flere årsaker:

* Behovet er sjeldent.
* Leveringstiden er ikke viktig.
* Det nødvendige attributtet varierer.  

Et annet tilfelle som bruker ordre-til-ordre-koblinger når en monteringsordre knyttes til en salgsordre i et monter-til-ordre-scenario.  

Ordre-til-ordre koblinger brukes mellom behov og forsyning på fire måter:  

* Når den planlagte varen bruker gjenbestillingsprinsippet **Ordre**  
* Når du bruker produser-til-ordre-produksjonsprinsippet til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av komponenter i samme produksjonsordre)  
* Når du oppretter produksjonsordrer for ordrer med funksjonen Ordreplanlegging  
* Når du monterer en vare til en ordre (**Monteringsprinsipp** er satt til **Monter til ordre**)  

Planleggingssystemet foreslår at du bare bestille det nødvendige antallet. Kjøps-, produksjons- eller monteringsordre fortsetter å samsvare med behovet. Hvis en ordre for eksempel endres i tid eller antall, foreslår planleggingssystemet at du endrer forsyningsordren tilsvarende.  

Når det finnes ordre-til-ordre-koblinger, involverer ikke planleggingssystemet koblet forsyning eller lager i balanseringsprosessen. Planleggere kan bestemme om du skal bruke den koblede forsyningen eller et nytt behov. I siste tilfelle kan de slette forsyningsordren eller reservere den koblede forsyningen manuelt.  

Koblinger for reservasjoner og sporing brytes hvis en situasjon blir umulig. Det kan for eksempel være at når du flytter behov til en dato som er tidligere enn forsyningen. Ordre-til-ordre-koblinger tilpasses til endringer i behovet eller forsyning og stanser aldri.  

## Reservasjoner

Planleggingssystemet tar ikke med reserverte antall i beregninger. Hvis for eksempel et antall for en ordre er helt eller delvis reservert, kan du ikke bruke antallet til å dekke annet behov.

Planleggingssystemet tar med reserverte antall i anslått lagerprofil. Den må ta hensyn til alle antall for å avgjøre når gjenbestillingspunktet er passert, og hvor mange du vil endre for å nå maksimum lagernivå. Unødvendige reservasjoner kan øke risikoen for at lagernivåene bli for lave fordi planleggingslogikken ikke gjenkjenner reservert antall.  

Bildet nedenfor viser hvordan reservasjonene kan hindre planlegging.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planlegge med reservasjoner.":::

Finn ut mer [Utformingsdetaljer: Reservasjon, sporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).  

## Advarsler

Den første kolonnen i planleggingsforslaget er for advarselsfeltene. Det vises et varselsikon når du oppretter en planleggingslinje for en uvanlig situasjon.  

Forsyning på planleggingslinjer med advarsler endres vanligvis ikke i henhold til planleggingsparametere. I stedet foreslår planleggingssystemet en forsyning for å dekke det nøyaktige antallet for behovet. Systemet kan imidlertid konfigureres slik at det respekterer planleggingsparametere for planleggingslinjer med bestemte advarsler. Advarselsinformasjon vises på siden **Ikke-sporede planleggingselementer**, som også viser sporingskoblinger til ikke-ordrenettverksenheter. Det finnes tre typer advarsler:  

* Kritisk  
* Unntak  
* Viktig  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Advarsler i planleggingsforslaget.":::

### Kritisk

Kritisk-advarselen vises i to situasjoner:  

* Når beholdningen er negativ på den planlagte startdatoen  
* Når det finnes tilbakedatert forsyning eller behov  

Hvis beholdningen for en vare er negativ på den planlagte startdatoen, foreslår planleggingssystemet at det opprettes en kritisk ordre for det negative antallet, med ankomst på den planlagte startdatoen. Advarselsteksten angir startdatoen og antallet på den kritiske ordren. Finn ut mer under [Utformingsdetaljer: Håndtere forventet negativ lagerbeholdning](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Dokumentlinjer med forfallsdato før den planlagte startdatoen konsolideres til en kritisk ordre. Ordren planlegges å ankomme på den planlagte startdatoen.  

### Unntak

Unntak-advarselen vises hvis den beregnede disponible beholdningen faller under sikkerhetslagerantallet. Planleggingssystemet foreslår at det opprettes en forsyningsordre for å oppfylle behovet på forfallsdatoen. Advarselsteksten angir varens sikkerhetslagerantall og datoen da antallet ble for lavt.  

Hvis sikkerhetslagernivået er brutt, er det et unntak. Det skal ikke skje hvis gjenbestillingspunktet er riktig angitt. Finn ut mer under [Rollen til gjenbestillingspunktet](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Unntaksordreforslag bidrar til å sikre at forventet disponibel beholdning aldri er lavere enn sikkerhetslagernivået. Det foreslåtte antallet dekker sikkerhetslageret, uten å ta hensyn planleggingsparametere. I noen scenarier vurderes imidlertid ordremodifikatorer.  

> [!NOTE]  
> Planleggingssystemet kan ha forbrukt sikkerhetslageret med hensikt og etterfyller det deretter med en gang. Finn ut mer under [Forbruk sikkerhetslager](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Viktig

Tilsyn-advarselen vises i tre situasjoner:  

* Den planlagte startdatoen er tidligere enn arbeidsdatoen.  
* Planleggingslinjen foreslår at en frigitt bestilling eller produksjonsordre endres.  
* Den beregnede beholdningen overskrider overflytnivået på forfallsdatoen. Finn ut mer på [Hold deg under overflytnivået](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> På planleggingslinjer med advarsler er ikke feltet **Godta handlingsmelding** valgt fordi planleggeren må undersøke linjene før planen utføres.  

## Feillogger

På forespørselssiden **Beregn plan** kan du velge feltet **Stopp og vis første feil** for å stoppe planleggingskjøringen når den første feilen oppstår. En melding vises med informasjon om feilen. Hvis det oppstår en feil, vises planleggingsforslaget planleggingslinjer som ble behandlet før feilen oppstod.  

Hvis feltet ikke er valgt, vil den satsvise jobben **Beregn plan** fortsette til den er fullført. Feil avbryter ikke den satsvise jobben. Hvis det oppstår feil, angir en melding hvor mange varer som ble påvirket. Siden **Feillogg planlegging** gir ytterligere informasjon om feilen og koblinger til ett eller flere dokumenter eller oppsett.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Feilmeldinger i planleggingsforslaget.":::

## Planleggingsfleksibilitet

Det er ikke alltid praktisk å planlegge en eksisterende forsyningsordre. Når for eksempel produksjonen har startet eller du leier inn ekstra personer på en bestemt dag for å gjøre prosjektet. For å angi om planleggingssystemet kan endre en ordre, har alle forsyningsordrelinjer et **Planleggingsfleksibilitet**-felt med to alternativer: **Ubegrenset** eller **Ingen**. Hvis feltet er satt til **Ingen**, vil ikke planleggingssystemet prøve å endre forsyningsordrelinjen.  

Du kan manuelt velge et alternativ i feltet, men i enkelte tilfeller angis det imidlertid automatisk av [!INCLUDE [prod_short](includes/prod_short.md)]. Det at du manuelt kan angi planleggingsfleksibiliteten er viktig fordi det gjør det enkelt å tilpasse bruk av funksjonen til ulike arbeidsflyter og saker. Hvis du vil finne ut mer om hvordan dette feltet, kan du gå til [Utformingsdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md).  

## Ordreplanlegging

Det grunnleggende verktøyet for forsyningsplanlegging på **Ordreplanlegging**-siden er utviklet for manuell beslutningstaking. Den tar ikke hensyn til eventuelle planleggingsparametere, og beskrives derfor ikke ytterligere i denne artikkelen. Finn ut mer under [Planlegge for nytt behov bestilling for bestilling](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Vi anbefaler at du ikke bruker ordreplanlegging hvis selskapet allerede bruker planleggings- eller bestillingsforslag. Forsyningsordrer som opprettes ved hjelp av **Ordreplanlegging**-siden, kan endres eller slettes under automatiserte planleggingskjøringer. Disse endringene skjer fordi den automatiserte planleggingskjøringen bruker planleggingsparametere som du kanskje ikke har vurdert når du manuelt lagde planen på siden Ordreplanlegging.  

## Begrenset belastning

[!INCLUDE[prod_short](includes/prod_short.md)] viser en grov tidsplan for planlegging av rimelig bruk av ressurser. Den oppretter og vedlikeholder ikke automatisk detaljerte planer basert på prioriteter eller optimaliserings regler.  

Den tiltenkte bruken av funksjonen for kapasitetsbegrenset ressurs er som følger:

* Slik unngår du å overbelaste ressurser
* Hvis du vil sikre at kapasiteten ikke forblir tildelt, hvis den kan redusere den opphevede tiden for en produksjonsordre

Når du planlegger med kapasitetsbegrensede ressurser, sikrer [!INCLUDE [prod_short](includes/prod_short.md)] at ingen ressurser lastes over den angitte kapasiteten (kritisk belastning). Det tildeler hver operasjon til nærmeste tilgjengelige tidsluke. Hvis tidsperioden ikke er stor nok til å fullføre hele operasjonen, deler den operasjonen inn i to eller flere deler som plasseres i de nærmeste tilgjengelige tidsrommene.  

> [!NOTE]  
> I tilfeller med oppdeling av operasjon blir oppstillingstiden bare tildelt én gang fordi det antas at noe manuell justering er gjort for å optimalisere tidsplanen.  

Du kan legge til avdempingstiden til ressurser for å minimere oppdeling av operasjonen. Dette tidspunktet lar [!INCLUDE [prod_short](includes/prod_short.md)] planlegge belastningen på den siste mulige dagen ved å delvis overstige den kritiske belastnings prosenten.  

## Se også

[Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md)  
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)  
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)  
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
