---
title: Designdetaljer – Sentrale begreper for planleggingssystemet | Microsoft-dokumentasjon
description: Planleggingsfunksjonene er i en kjørsel som først velger de aktuelle varene og perioden som skal planlegges, og foreslår deretter mulige handlinger som brukeren kan utføre i henhold til etterspørsels-/tilbudssituasjonen og varens planleggingsparametere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b809743aa25aee409b9a71ca98da77ea64b58fb1
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076517"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Designdetaljer: Sentrale begreper for planleggingssystemet
Planleggingsfunksjonene er i en kjørsel som først velger de aktuelle varene og perioden som skal planlegges. Deretter kaller kjørselen en kodeenhet i henhold til lavnivåkoden (stykklisteposisjonen) for hver vare. Kodeenheten beregner en forsyningsplan ved å balansere sett med behov/forsyning, og foreslår mulige handlinger for brukeren. De foreslåtte handlingene vises som linjer i planleggingsforslaget eller bestillingsforslaget.  

![Innhold på Planleggingsforslag-siden](media/NAV_APP_supply_planning_1_planning_worksheet.png "Innhold på Planleggingsforslag-siden")  

Planleggeren i et selskap, for eksempel en innkjøper eller en produksjonsplanlegger, antas å være brukeren av planleggingssystemet. Planleggingssystemet hjelper brukeren ved å utføre omfattende, men heller enkle, beregninger av en plan. Brukeren kan dermed konsentrere seg om å løse vanskeligere problemer, for eksempel når ting avviker fra det som er vanlig.  

Planleggingssystemet drives av forventet og faktisk kundebehov, for eksempel prognose og ordrer. Når planleggingsberegningen kjøres, foreslår programmet bestemte handlinger som brukeren kan utføre, vedrørende mulig forsyning fra leverandører, monterings- eller produksjonsavdelinger, eller overføringer fra andre lagre. Disse foreslåtte handlingene kan være opprettelse av nye forsyningsordrer, for eksempel bestillinger og produksjonsordrer. Hvis det allerede finnes forsyningsordrer, kan de foreslåtte handlingene være å øke eller påskynde ordrene for å dekke endringene i behovet.  

Et annet mål med planleggingssystemet er å sikre at beholdningen ikke vokser unødvendig. Hvis behovet avtar, foreslår systemet at brukeren utsetter, reduserer antallet i eller annullerer eksisterende forsyningsordrer.  

MRP og MPS, Beregn bevegelsesplan og Beregn replanlegging er alle funksjoner i én kodeenhet som inneholder planleggingslogikken. Forsyningsplanberegningen omfatter imidlertid forskjellige undersystemer.  

Vær oppmerksom på at planleggingssystemet ikke inneholder dedikert logikk for kapasitetsutjevning eller finplanlegging. Derfor utføres slikt planleggingsarbeid som en egen disiplin. Mangelen på direkte integrasjon mellom de to områdene betyr også at omfattende kapasitets- eller planendringer gjør at planleggingen må kjøres på nytt.  

## <a name="planning-parameters"></a>Planleggingsparametere  
Planleggingsparametre som brukeren angir for en vare eller varegruppe, styrer hvilke handlinger planleggingssystemet foreslår i ulike situasjoner. Planleggingsparameterne defineres på hvert varekort for å kontrollere når etterfyllingen skal gjøres, hvor mye som skal etterfylles, og hvordan etterfyllingen skal gjøres.  

Planleggingsparametre kan også angis for en hvilken som helst kombinasjon av vare, variant og lokasjon, ved å konfigurere en lagerføringsenhet (LFE) for hver nødvendig kombinasjon og deretter angi individuelle parametere.  

Hvis du vil ha mer informasjon, se [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md) og [Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Planlegge startdato  
For å unngå en forsyningsplan som innholder åpne ordrer i fortiden og foreslår potensielt umulige handlinger, behandler planleggingssystemet alle datoer før den planlagte startdatoen som en frossen sone der følgende spesialregel gjelder:  

Alle tilbud og etterspørsel før startdatoen for planleggingsperioden blir betraktet som en del av beholdningen eller levert.  

Det antar med andre ord at planen for fortiden utførtes i henhold til den angitte planen.  

Hvis du vil ha mer informasjon, kan du se [Håndtere ordrer før den planlagte startdatoen](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynamisk sporing (utligning)  
Dynamisk sporing, med den samtidige opprettingen av handlingsmeldinger i planleggingsforslaget, er ikke en del av forsyningsplanleggingssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Denne funksjonen knytter sammen behovene og antallene som kan dekke dem, i sanntid, hver gang et nytt behov eller en ny forsyning opprettes eller endres.  

Hvis brukeren for eksempel angir eller endrer en ordre, vil det dynamisk ordresporingssystemet umiddelbart søke etter en passende forsyning til å dekke behovet. Dette kan være fra lager eller en forventet forsyningsordre (for eksempel en bestilling eller en produksjonsordre). Når en forsyningskilde blir funnet, oppretter systemet en kobling mellom behovet og forsyningen og viser koblingen på visningssider som kan åpnes fra de aktuelle dokumentlinjene. Når riktig forsyning ikke blir funnet, oppretter det dynamiske sporingssystemet handlingsmeldinger i planleggingsforslaget med forsyningsplanforslag som gjenspeiler den dynamiske balanseringen. Det dynamiske systemet for ordresporing tilbyr et svært enkel planleggingssystem som kan være nyttig for planleggere og andre roller i den interne forsyningskjeden.  

Tilsvarende kan dynamisk sporing betraktes som et verktøy som hjelper brukeren med å vurdere forslag til forsyningsordre skal godtas. Fra forsyningssiden kan en bruker se hvilke behov som har opprettet forsyning, og fra behovssiden hvilken forsyning som skal dekke behovet.  

![Eksempel på dynamisk sporing](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Eksempel på dynamisk sporing")  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).  

I selskaper med en lav vareflyt og mindre avanserte produktstrukturer kan det være tilstrekkelig å bruke dynamisk sporing som det primære middelet for forsyningsplanlegging. I travle miljøer bør planleggingssystemet imidlertid brukes til å sikre at det alltid finnes en riktig balansert forsyningsplan.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamisk sporing kontra planleggingssystemet  
Det kan være vanskelig å skille mellom planleggingssystemet og dynamisk sporing med et raskt blikk. Begge funksjonene viser utdata i planleggingsforslaget ved å foreslå handlinger som planleggeren bør utføre. Utdataene blir imidlertid produser på en annen måte.  

Planleggingssystemet håndterer hele forsynings- og behovsmønsteret for en vare gjennom alle nivåer i stykklistehierarkiet langs tidslinjen, mens dynamisk sporing bare håndterer situasjonen for ordren som aktiverte det. Når planleggingssystemet balanserer behov og forsyning, oppretter det koblinger i en brukeraktivert satsvis modus, mens Dynamisk sporing oppretter koblingene automatisk og på sparket, hver gang brukeren registrerer et behov eller en forsyning i programmet, for eksempel en ordre eller bestilling.  

Dynamisk sporing oppretter koblinger mellom behov og forsyning når data registreres, basert på det som kommer først. Dette kan føre til litt uorden i prioriteter. En ordre som angis først og som har forfallsdato neste måned, kan for eksempel være koblet til forsyning på lager, mens den neste ordren som forfaller i morgen, kan føre til en handlingsmelding om å opprette en ny bestilling for å dekke den, som vist nedenfor.  

![Eksempel på sporing i forsyningsplanlegging 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Eksempel på sporing i forsyningsplanlegging 1")  

I motsetning håndterer planleggingssystemet alle behov og forsyning for en bestemt vare, i prioritert rekkefølge i henhold til forfallsdato og ordretyper, det vil si basert på det som kommer først. Den sletter alle sporingskoblinger som ble opprettet dynamisk, og etablerer dem på nytt i henhold til forfallsdatoprioritet. Når planleggingssystemet har kjørt, har det løst all ubalanse mellom behov og forsyning, som vist nedenfor for de samme dataene.  

![Eksempel på sporing i forsyningsplanlegging 2](media/NAV_APP_supply_planning_1_planning_graph.png "Eksempel på sporing i forsyningsplanlegging 2")  

Etter planleggingskjøringen lagres ingen handlingsmeldinger i tabellen Handlingsmeldingspost fordi de har blitt erstattet av de foreslåtte handlingene i planleggingsforslaget  

Hvis du vil ha mer informasjon, kan du se sporingskoblinger under Planlegging i [Balansere forsyning med behov](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand).  

## <a name="sequence-and-priority-in-planning"></a>Rekkefølge og prioritet i planlegging  
Når du oppretter en plan, er rekkefølgen beregningene gjøres i, viktig for å få jobben gjort innen rimelig tid. I tillegg spiller prioritering av krav og ressurser en viktig rolle for å oppnå de beste resultatene.  

Planleggingssystemet i [!INCLUDE[d365fin](includes/d365fin_md.md)] drives av behov. Varer på høyt nivå må planlegges før vare på lavt nivå, fordi planen for varer på høyt nivå kan generere ekstra behov for varene på lavere nivå. Dette betyr for eksempel at detaljhandelslokasjoner må planlegges før distribusjonssentre, fordi planen for en detaljhandelslokasjon kan inneholde flere behov fra distribusjonssenteret. På et detaljert balansenivå betyr dette også at en ordre ikke skal utløse en ny forsyningsordre hvis det en allerede utgitt forsyningsordre kan dekke ordren. En forsyning fra et bestemt partinummer skal ikke tilordnes for å dekke et generelt behov hvis et annen behov krever dette bestemte partiet.  

### <a name="item-priority--low-level-code"></a>Varens prioritet/lavnivåkode  
Behovet for en ferdig og salgbare vare i et produksjonsmiljø, vil føre til avledede behov for komponenter som utgjør den ferdige varen. Stykklistestrukturen kontrollerer komponentstrukturen og kan dekke flere nivåer av halvferdige varer. Planlegging av en vare på ett nivå vil føre til et avledede behov for komponenter på det neste nivået og så videre. Dette fører til slutt til avledet behov for kjøpte varer. Planleggingssystemet planlegger derfor for varer i rangeringsrekkefølgen i det totale stykklistehierarkiet. Systemet starter på øverste nivå med en ferdig vare som kan selges, og fortsetter nedover gjennom produktstrukturen til varene på lavere nivåer (i henhold til lavnivåkode).  

![Planlegge for stykklister](media/NAV_APP_supply_planning_1_BOM_planning.png "Planlegge for stykklister")  

Figurene illustrerer i hvilken rekkefølge systemet lager forslag til forsyningsordrer på øverste nivå og, forutsatt at brukeren godtar disse forslagene, for alle varene på lavere nivå også.  

Du finner mer informasjon om produksjonshensyn i [Laste inn lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

### <a name="locations--transfer-level-priority"></a>Lokasjoner / prioritet for overføringsnivå  
Firmaer som driver virksomhet på mer enn ett sted må kanskje planlegge individuelt for hver enkelt lokasjon. Sikkerhetslagernivået og gjenbestillingsprinsippet for en vare kan for eksempel være forskjellig på ulike lokasjoner. I slike tilfeller må planleggingsparameterne angis per vare og per lokasjon.  

Dette støttes med bruk av LFEer, der individuelle planleggingsparametere kan angis på LFE-nivået. En SKU kan betraktes som en vare på en bestemt plassering. Hvis brukeren ikke har angitt LFE for denne lokasjonen, vil programmet bruke standardparametere som er angitt på varekortet. Programmet beregner en plan bare for aktive lokasjoner, som er der det finnes behov eller forsyning for den angitte varen.  

I prinsippet kan en vare håndteres på en hvilken som helst lokasjon, men programmets tilnærming til lokasjonskonseptet er ganske streng. En ordre på én lokasjon kan for eksempel ikke oppfylles av et antall på lager på en annen lokasjon. Antallet på lager må først overføres til lokasjonen som er angitt i ordren.  

![Planlegge for lagerføringsenheter](media/NAV_APP_supply_planning_1_SKU_planning.png "Planlegge for lagerføringsenheter")  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md).  

### <a name="order-priority"></a>Bestillingsprioritet  
I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i de neste dagene. Bortsett fra denne typen prioritet blir ulike behovs- og forsyningstyper sortert i henhold til viktighet i virksomheten for å avgjøre hvilke behov som må oppfylles før andre behov oppfylles. På forsyningssiden vil ordreprioriteten vise hvilken forsyningskilde som skal brukes før bruk av andre forsyningskilder.  

Hvis du vil ha mer informasjon, kan du se [Prioritere ordrer](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Behovsprognoser og rammeordrer  
Både prognoser og rammeordrer representerer forventet behov. Rammeordren, som dekker kjøp en kunde har tenkt å foreta i en bestemt tidsperiode, er med på å redusere usikkerheten ved den samlede prognosen. Rammeordren er en kundespesifikk prognose oppå den uspesifiserte prognosen som illustreres nedenfor.  

![Planlegging med prognoser](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planlegging med prognoser")  

Hvis du vil ha mer informasjon, kan du se delen Prognosebehov blir redusert av ordrer i [Laste inn lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Planleggingstilordning  
Det må planlegges for alle varer, men det er ingen grunn til å beregne en plan for en vare med mindre det er en endring i mønsteret for behov eller forsyning siden planen sist ble beregnet.  

Hvis brukeren har angitt en ny ordre eller endret en eksisterende, er det grunn til å beregne planen på nytt. Andre årsaker inkluderer en endring i prognosen eller ønsket sikkerhetslagerantall. Endring av en stykkliste ved å legge til eller fjerne en komponent, vil mest sannsynlig indikerer en endring, men bare for komponentvaren.  

Planleggingssystemet overvåker slike hendelser og tilordner de riktige varene for planlegging.  

For flere lokasjoner foregår tildelingen på nivået for en vare per lokasjonskombinasjon. Hvis det for eksempel er opprettet en ordre på bare én lokasjon, vil programmet tilordne varen på denne spesifikke lokasjonen for planlegging.  

Grunnen til å velge varer for planlegging har å gjøre med systemytelsen. Hvis det ikke har oppstått endringer i en vares behov-/ forsyningsmønster, foreslår vil ikke planleggingssystemet foreslå handlinger som skal utføres. Uten planleggingstilordningen måtte systemet ha utført beregningene for alle varer for å finne ut hva det skal planlegge for, og dette hadde tappet systemressursene.  

Den fullstendige listen over grunner til å tilordne en vare for planlegging finnes i [Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md).  

Planleggingsalternativene i [!INCLUDE[d365fin](includes/d365fin_md.md)] er:  

-   Beregn replanlegging – beregner alle valgte varer, om det er nødvendig eller ikke.  
-   Beregn bevegelsesplan – beregner bare de valgte varene som har hatt endringer i behovs-/forsyningsmønsteret og derfor er tilordnet for planlegging.  

Noen brukere mener at bevegelsesplanlegging bør utføres raskt når som helst, for eksempel når ordrer registreres. Dette kan imidlertid være forvirrende fordi dynamisk ordresporing og handlingsmeldinger også beregnes direkte. I tillegg har [!INCLUDE[d365fin](includes/d365fin_md.md)] tilgjengelig for ordre (ATP)/kontroll i sanntid, noe som gir popup-advarsler når du registrerer salgsordrer hvis behovet ikke kan oppfylles i henhold til gjeldende forsyningsplan.  

I tillegg til disse vurderingene planlegger planleggingssystemet bare for varer der brukeren har klargjort med riktige planleggingsparametere. Hvis ikke, antas det at brukeren skal planlegge varene manuelt eller halvautomatisk ved hjelp av funksjonen for ordreplanlegging.  

Hvis du vil ha mer informasjon om automatiske planleggingsprosedyrer, kan du se [Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Varedimensjoner  
Behov og forsyning kan omfatte variant- og lokasjonskoder som må respekteres når planleggingssystemet balanserer behov og forsyning.  

Systemet behandler variant- og lokasjonskoder som varedimensjoner på en salgsordrelinje, lagerpost og så videre. Det beregner derfor en plan for hver kombinasjon av variant og lokasjon som om kombinasjonen var et eget varenummer.  

I stedet for å beregne teoretiske kombinasjoner av variant og lokasjon, beregner programmet kombinasjonene som faktisk finnes i databasen.  

Hvis du vil ha mer informasjon om hvordan planleggingssystemet håndterer lokasjonskoder på forespørsel, kan du se [Designdetaljer: Behov på tom lokasjon](design-details-balancing-demand-and-supply.md)..  

## <a name="item-attributes"></a>Vareattributter  
I tillegg til generell varedimensjoner, for eksempel varenummer, variantkode, lokasjonskode og ordretype, kan hver hendelses og forsyningshendelse inneholde tilleggsspesifikasjoner i form av serie-/partinumre. Planleggingssystemet planlegger disse attributtene på bestemte måter som avhenger av spesifikasjonsnivået deres.  

En ordre-til-ordre-kobling mellom behov og forsyning er en annen attributtype som påvirker planleggingssystemet.  

### <a name="specific-attributes"></a>Bestemte attributter  
Enkelte attributter på forespørsel er spesifikke og må samsvare nøyaktig med en tilsvarende forsyning. Følgende to bestemte attributter finnes:  

-   Etterspørsel etter serie-/partinumre som krever bestemt program (avmerkingsboksen **Sporing basert på s.nr.** eller **Sporing basert på parti** er merket av på **Kort for varesporingskode**-siden for varesporingskode som brukes av elementet.)  
-   Koblinger til forsyningsordrer som er opprettet manuelt eller automatisk for et bestemt behov (ordre-til-ordre-koblinger).  

Planleggingssystemet bruker følgende regler for disse attributtene:  

-   Behov med bestemte attributter kan bare oppfylles av forsyning med tilsvarende attributter.  
-   Forsyning med bestemte attributter kan også dekke behov som ikke spesifikt ber om disse attributtene.  

Hvis et behov for bestemte attributter ikke kan oppfylles av lager eller forventede forsyninger, vil planleggingssystemet foreslå en ny forsyningsordre for å dekke dette bestemte behov uten hensyn til planleggingsparametere.  

### <a name="non-specific-attributes"></a>Ikke-spesifikke attributter  
Serie-/partinummererte varer uten et bestemt varesporingsoppsett kan ha serie-/partinumre som ikke trenger å utlignes mot nøyaktig samme serie-/partinummer, men kan utlignes mot et hvilket som helst serie-/partinummer. Dette gir planleggingssystemet større frihet til for eksempel å knytte et serialisert behov til en serialisert forsyning, vanligvis på lageret.  

Behov/forsyning med serie-/partinumre, spesifikke eller ikke-spesifikke, anses som høy prioritet og er derfor er unntatt fra den frosne sonen, noe som betyr at de blir en del av planleggingen selv om de er forfalt før den planlagte startdatoen.  

Hvis du vil ha mer informasjon, kan du se avsnittet Serie-/partinumre lastes inn etter spesifikasjonsnivå i [Laste inn lagerprofiler](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Hvis du vil ha mer informasjon om hvordan planleggingssystemet balanserer attributter, kan du se [Serie-/partinumre og ordre-til-ordre-koblinger er fritatt fra den frosne sonen](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Odre-til-ordre-koblinger  
Ordre-til-ordre-innkjøp betyr at en vare utelukkende blir kjøpt, montert eller produsert for å dekke et spesifikt behov. Vanligvis er dette knyttet til A-varer, og motivasjon for å velge dette prinsippet kan være at behovet er sjeldent, leveringstiden er ubetydelig eller de nødvendige attributtene varierer.  

Et annet spesialtilfelle som bruker ordre-til-ordre-koblinger når en monteringsordre knyttes til en salgsordre i et monter-til-ordre-scenario.  

Ordre-til-ordre koblinger brukes mellom behov og forsyning på fire måter:  

-   Når den planlagte varen bruker gjenbestillingsprinsippet Ordre.  
-   Når produksjonsprinsippet Produser til ordre brukes til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre).  
-   Når produksjonsordrer opprettes for ordrer med funksjonen Ordreplanlegging.  
-   Når en vare monteres til en ordre. (Monteringsprinsippet er satt til å montere til ordre.  

I slike tilfeller vil planleggingssystemet bare foreslå å bestille det nødvendige antallet. Når opprettet, vil kjøps-, produksjons- eller monteringsordre fortsatt samsvarer med det tilsvarende behovet. Hvis en ordre for eksempel endres i tid eller antall, foreslår planleggingssystemet at tilsvarende forsyningsordre endres tilsvarende.  

Når det finnes ordre-til-ordre-koblinger, involverer ikke planleggingssystemet koblet forsyning eller lager i balanseringsprosessen. Det er opp til brukeren å vurdere om den tilknyttede forsyningen skal brukes til å dekke et annet eller nytt behov, og i slike tilfeller må forsyningsordren slettes eller den tilknyttede forsyningen må reserveres manuelt.  

Reservasjoner og sporingskoblinger brytes hvis en situasjon blir umulig, for eksempel hvis behovet flyttes til en dato som kommer før forsyningen. Ordre-til-ordre-kobling tilpasses imidlertid eventuelle endringer i det aktuelle behovet eller forsyningen, og dermed blir koblingen aldri brutt.  

## <a name="reservations"></a>Reservasjoner  
Planleggingssystemet tar ikke med reserverte antall i beregningen. Hvis en ordre er helt eller delvis reservert mot antallet på lageret, kan for eksempel ikke det reserverte antallet på lageret brukes til å dekke andre behov. Planleggingssystemet tar ikke med dette settet med behov/forsyning i beregningen.  

Planleggingssystemet vil imidlertid fremdeles inkludere reservert antall i profilen for beregnet beholdning, fordi alle antall må tas i betraktning når du fastslår både når gjenbestillingspunktet er overskredet, og hvor mange som må gjenbestilles for å oppnå og ikke overskride maksimumsnivået for beholdningen. Unødvendige reservasjoner vil derfor føre til økt risiko for at lagernivåene bli for lave fordi planleggingslogikken ikke gjenkjenner reservert antall.  

Illustrasjonen nedenfor viser hvordan reservasjoner kan hindre den mest gjennomførbare planen.  

![Planlegge med reservasjoner](media/NAV_APP_supply_planning_1_reservations.png "Planlegge med reservasjoner")  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Advarsler  
Den første kolonnen i planleggingsforslaget er for advarselsfeltene. Når en planleggingslinje opprettes for en uvanlig situasjon, vises et advarselsikon i dette feltet. Brukeren kan klikke ikonet for å få mer informasjon.  

Forsyning på planleggingslinjer med advarsler blir vanligvis ikke endret i henhold til planleggingsparametere. I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden. Systemet kan imidlertid konfigureres slik at det respekterer visse planleggingsparametere for planleggingslinjer med bestemte advarsler. Hvis du vil ha mer informasjon, kan du se beskrivelsen av disse alternativene for kjørselen **Beregn plan - planl.forslag**. og **Beregn plan - best.forslag** henholdsvis.  

Advarselsinformasjon vises på siden **Ikke-sporede planleggingselementer**, som også brukes til å vise sporingskoblinger til ikke-ordrenettverksenheter. Følgende typer advarsler finnes:  

-   Kritisk  
-   Unntak  
-   Viktig  

![Advarsler i planleggingsforslaget](media/NAV_APP_supply_planning_1_warnings.png "Advarsler i planleggingsforslaget")  

### <a name="emergency"></a>Kritisk  
Kritisk-advarselen vises i to situasjoner:  

-   Når beholdningen er negativ på den planlagte startdatoen.  
-   Når det finnes tilbakedatert forsyning eller behov.  

Hvis beholdningen for en vare er negativ på den planlagte startdatoen, foreslår planleggingssystemet at det opprettes en kritisk ordre for det negative antallet, med ankomst på den planlagte startdatoen. Advarselsteksten angir startdatoen og antallet på den kritiske ordren. Hvis du vil ha mer informasjon, se [Håndtere forventet negativ lagerbeholdning](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Dokumentlinjer med forfallsdato før den planlagte startdatoen konsolideres til én kritisk ordre for varen, med ankomst på den planlagte startdatoen.  

### <a name="exception"></a>Unntak  
Unntak-advarselen vises hvis den beregnede disponible beholdningen faller under sikkerhetslagerantallet. Planleggingssystemet foreslår at det opprettes en forsyningsordre for å oppfylle behovet på forfallsdatoen. Advarselsteksten angir varens sikkerhetslagerantall og datoen da antallet ble for lavt.  

Et for lavt sikkerhetslagernivå anses for å være et unntak fordi det ikke skal forekomme hvis gjenbestillingspunktet er riktig angitt. Hvis du vil ha mer informasjon, se [Rollen til gjenbestillingspunktet](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Unntaksordreforslag sikrer vanligvis at forventet disponibel beholdning aldri er lavere enn sikkerhetslagernivået. Dette betyr at det foreslåtte antallet er akkurat nok til å dekke sikkerhetslageret, uten å ta hensyn planleggingsparametre. I noen scenarier vurderes imidlertid ordremodifikatorer.  

> [!NOTE]  
>  Planleggingssystemet kan ha forbrukt sikkerhetslageret med hensikt og etterfyller det deretter med en gang. Hvis du vil ha mer informasjon, se [Sikkerhetslager kan forbrukes](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Viktig  
Tilsyn-advarselen vises i tre situasjoner:  

-   Den planlagte startdatoen er tidligere enn arbeidsdatoen.  
-   Planleggingslinjen foreslår at en frigitt bestilling eller produksjonsordre endres.  
-   Den beregnede beholdningen overskrider overflytnivået på forfallsdatoen. Hvis du vil ha mer informasjon, se [Holde seg under overflytnivået](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  På planleggingslinjer med advarsler er ikke feltet **Godta handlingsmelding** valgt, fordi planleggeren må undersøke disse linjene ytterligere før planen utføres.  

## <a name="error-logs"></a>Feillogger  
På forespørselssiden Beregn plan kan brukeren velge feltet **Stopp og vis første feil** for å stoppe planleggingskjøringen når den første feilen oppstår. Samtidig vises en melding med informasjon om feilen. Hvis det oppstår en feil, vises bare feilfrie planleggingslinjer som ble behandlet før feilen oppstod, i planleggingsforslaget.  

Hvis feltet ikke er valgt, vil den satsvise jobben Beregn plan fortsette til den er fullført. Feil avbryter ikke den satsvise jobben. Hvis det oppstår feil, vises en melding når kjørselen er fullført, med informasjon om hvor mange varer som er berørt av feil. Siden **Feillogg planlegging** åpnes deretter med ytterligere informasjon om feilen og koblinger til ett eller flere dokumenter eller oppsettkort som er berørt.  

![Feilmeldinger i planleggingsforslaget](media/NAV_APP_supply_planning_1_error_log.png "Feilmeldinger i planleggingsforslaget")  

## <a name="planning-flexibility"></a>Planleggingsfleksibilitet  
Det er ikke alltid praktisk å planlegge en eksisterende forsyningsordre, for eksempel når produksjonen har startet eller ekstra folk ansettes på en bestemt dag for å gjøre jobben. For å angi om en eksisterende ordre kan endres av planleggingssystemet, har alle forsyningsordrelinjer et Planleggingsfleksibilitet-felt med to alternativer: Ubegrenset eller Ingen. Hvis feltet er satt til Ingen, vil ikke planleggingssystemet prøve å endre forsyningsordrelinjen.  

Feltet kan angis manuelt av brukeren, men i enkelte tilfeller angis det automatisk av systemet. Det at planleggingsfleksibilitet kan angis manuelt av brukeren, er viktig, fordi det gjør det enkelt å tilpasse bruk av funksjonen til ulike arbeidsflyter og saker.  

Du finner mer informasjon om hvordan dette feltet brukes i [Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Bestillingsplanlegging  
Det grunnleggende verktøyet for forsyningsplanlegging på **Ordreplanlegging**-siden er utviklet for manuell beslutningstaking. Den tar ikke hensyn til eventuelle planleggingsparametre, og beskrives derfor ikke ytterligere i dette dokumentet. Hvis du vil ha mer informasjon om funksjonen Ordreplanlegging, kan du se Hjelp i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Det anbefales ikke å bruke ordreplanlegging hvis selskapet allerede bruker planleggings- eller bestillingsforslag. Forsyningsordrer som opprettes ved hjelp av **Ordreplanlegging**-siden, kan endres eller slettes under automatiserte planleggingskjøringer. Dette er fordi den automatiserte planleggingskjøringen bruker planleggingsparametere, og brukeren som laget den manuelle planen på Ordreplanlegging-siden, tar kanskje ikke disse med i beregningen.  

##  <a name="finite-loading"></a>Begrenset belastning  
[!INCLUDE[d365fin](includes/d365fin_md.md)] er et standard ERP-system, ikke et ordrefordelings- eller produksjonskontrollsystem. Det planlegger for en gjennomførbar utnyttelse av ressurser ved å tilby en grov tidsplan, men det blir ikke automatisk opprettet og vedlikeholdt detaljerte tidsplaner basert på prioriteringer eller regler for optimalisering.  

Den tiltenkte bruken av funksjonen Kapasitetsbegrenset ressurs er 1) for å unngå overbelastning av bestemte ressurser, og 2) for å sikre at all kapasitet fordeles hvis den kan øke gjennomløpstiden til en produksjonsordre. Funksjonen omfatter ikke muligheter eller alternativer for å prioritere eller optimalisere operasjoner, som vanligvis finnes i et fordelingssystem. Dette kan imidlertid gi en grov kapasitetsinformasjon som er nyttig til å identifisere flaskehalser og for å unngå overbelastning av ressurser.  

Når du planlegger med kapasitetsbegrensede ressurser, sikrer systemet at ingen ressurser lastes over den angitte kapasiteten (kritisk belastning). Dette gjøres ved å tilordne hver operasjon til nærmeste tilgjengelige tidsluke. Hvis tidsperioden ikke er stor nok til å fullføre hele operasjonen, vil operasjonen bli delt inn i to eller flere deler som plasseres i de nærmeste tilgjengelige tidsrommene.  

> [!NOTE]  
>  I tilfeller med oppdeling av operasjon blir oppstillingstiden bare tilordnet én gang fordi det antas at noe manuell justering er gjort for å optimalisere tidsplanen.  

Avdempingstiden kan legges til ressurser for å minimere oppdeling av operasjonen. Dette gjør at systemet kan planlegge belastning på den aller siste dagen ved å overskride den kritiske belastningsprosenten litt hvis dette kan redusere antall delte operasjoner.  

Dermed har du fått en oversikt over sentrale begreper som har å gjøre med forsyningsplanlegging i [!INCLUDE[d365fin](includes/d365fin_md.md)]. De følgende delene tar for seg disse begrepene i større detalj og plasserer dem i sammenheng med de viktigste fremgangsmåtene for planlegging, balansering av behov og forsyning samt bruk av gjenbestillingsprinsipper.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Overføringer i planlegging](design-details-transfers-in-planning.md)   
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)   
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)
