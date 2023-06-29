---
title: Designdetaljer – Balanser tilbud og etterspørsel
description: Denne artikkelen beskriver hvordan du prioriterer mål ved å balansere tilbud med etterspørsel.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a><a name="design-details-balancing-supply-and-demand"></a>Designdetaljer: Balanser tilbud og etterspørsel

Hvis du vil forstå hvordan planleggingssystemet fungerer, er det viktig å forstå de prioriterte målene:  

* Alle behov blir oppfylt av tilstrekkelig forsyning.  
* Eventuell forsyning har et formål.  

Vanligvis oppnås disse målene ved å balansere forsyning med behov.  

## <a name="supply-and-demand"></a><a name="supply-and-demand"></a>Tilbud og etterspørsel

Betegnelsen *tilbyd* gjelder alle typer positive eller inngående antall, for eksempel:

* Lager
* Innkjøp
* Montering
* Produksjon
* Inngående overføringer
* Salgsreturer  

Begrepet *etterspørsel* henviser til alle typer bruttoetterspørsler, for eksempel:

* En vare for en ordre
* En komponent for en produksjonsordre

Med [!INCLUDE [prod_short](includes/prod_short.md)] kan du også bruke mer tekniske typer etterspørsler, for eksempel negativt lager og bestillingsreturer.

For å sortere ut de mange kildene til tilbud og etterspørsel organiserer planleggingssystemet dem på to tidslinjer kalt lagerprofiler. Én profil er for etterspørselshendelser, og den andre er for tilsvarende tilbudshendelser. Hver forsyningshendelse representerer én enhet i en ordre, for eksempel:

* En ordrelinje
* En varepost
* En produksjonsordrelinje

Når du lagerprofiler lastes inn, balanseres settene med etterspørsel/tilbud for å gi en etterspørselsplan som oppfyller de angitte målene.

Lagernivåer og planleggingsparametere er andre typer tilbud og etterspørsel. Disse typene gjennomgår integrert balanse for å etterfylle varer på lager. Finn ut mer under [Designdetaljer: Håndter gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)

## <a name="the-concept-of-balancing-in-brief"></a><a name="the-concept-of-balancing-in-brief"></a>Kort om begrepet balansering

Etterspørsel kommer fra kundene dine. Tilbud er det du oppretter og fjerner for å skape balanse. Planleggingssystemet starter med etterspørselen og sporer deretter bakover til tilbudet.  

Lagerprofilene inneholder informasjon om etterspørsler og tilbud, antall og tidsberegning. Disse profilene utgjør de to sidene av balanseringsskalaen.  

Formålet med planleggingsmekanismen er å balansere tilbud og etterspørsel av en vare for å sikre at etterspørselen samsvarer med tilbudet, og å gjøre dette på en passende måte som defineres av planleggingsparameterne og -reglene.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Oversikt over balansering mellom tilbud og etterspørsel.":::

## <a name="process-orders-before-the-planning-start-date"></a><a name="process-orders-before-the-planning-start-date"></a>Behandle ordrer før den planlagte startdatoen

For å unngå at etterspørselsplanene viser urimelige forslag, planlegger ikke planleggingssystemet noe i perioden før den planlagte startdatoen. Følgende regel gjelder den perioden:

* Alle tilbud og etterspørsel før startdatoen for planleggingsperioden betraktes som en del av lageret eller levert.  

Med noen få unntak foreslår ikke planleggingssystemet endringer for forsyningsordrer i perioden eller oppretter ordresporingskoblinger for denne perioden. Følgende er unntakene fra denne regelen:  

* Lageret som er forventet å være tilgjengelig, inkludert summen av tilbud og etterspørsel i perioden, er under null.  
* Tilbakedaterte ordrer krever serie- eller partinumre.  
* Tilbud og etterspørsel-settet er koblet til et ordre-til-ordre-prinsipp. 

Hvis den første disponible beholdningen er under null, foreslår planleggingssystemet en kritisk ordre på dagen før planleggingsperioden, for å dekke antallet som mangler. Forventet og tilgjengelige lager vil derfor alltid være minst null når planlegging for den fremtidige perioden begynner. Planleggingslinjen for denne forsyningsordren har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a><a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Serie- og partinumre og ordre-til-ordre-koblinger er fritatt fra den forrige perioden

Hvis serie- eller partinumre kreves eller det finnes en ordre-til-ordre-kobling, anser planleggingssystemet regelen om forrige periode. Den inkluderer tilbakedaterte antall fra startdatoen og kan foreslå korrigerende handlinger hvis tilbud og etterspørsel ikke er synkronisert. Disse tilbud og etterspørsel-settene må samsvare for å sikre at et bestemt behov er oppfylt.

## <a name="load-inventory-profiles"></a><a name="load-inventory-profiles"></a>Laste inn lagerprofiler

For å sortere ut de mange kildene til tilbud og etterspørsel organiserer planleggingssystemet dem på to tidslinjer kalt lagerprofiler.  

Tilbud og etterspørsel med forfallsdatoer på eller etter den planlagte startdatoen lastes inn i hver lagerprofil. Når de lastes inn, sorteres tilbuds- og etterspørselstypene i henhold til generelle prioriteter, for eksempel:

* Forfallsdato
* Lavnivåkoder
* Lokasjon
* Variant

Ordreprioriteter brukes på de forskjellige typene for å oppfylle det viktigste behovet først. Finn ut mer under [Prioritering av ordrer](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Etterspørsel kan også være negativ. Behandle negativ etterspørsel som tilbud. I motsetning til vanlig etterspørsel anses imidlertid negativ etterspørsel fast etterspørsel. Planleggingssystemet kan ta det med i betraktningen, men foreslår endringer av det.  

Planleggingssystemet tar vanligvis hensyn til alle forsyningsordrer etter den planlagte startdatoen som kan endres for å dekke behovet. Etter et antall er bokført fra en forsyningsordre, kan ikke planleggingssystemet endre den. Følgende ordrer kan ikke planlegges på nytt:  

* Frigitte produksjonsordrer der forbruk eller avgang er bokført.  
* Monteringsordre der forbruk eller avgang er bokført.  
* Overføringsordrer der leveringen er bokført.  
* Bestillinger der mottaket er bokført.  

I tillegg til å laste inn tilbuds- og etterspørsels-typer, blir bestemte typer lastet inn med oppmerksomhet på spesialregler og avhengigheter. De følgende delene i denne artikkelen beskriver disse reglene og avhengighetene.  

### <a name="item-dimensions-are-separated"></a><a name="item-dimensions-are-separated"></a>Varedimensjoner atskilles

Forsyningsplanen må beregnes for hver kombinasjon av varedimensjonene, for eksempel variant og lokasjon. Bare kombinasjonene som inneholder behov og/eller forsyning må beregnes.  

Planleggingssystemet ser etter kombinasjoner i lagerprofilen. Når det finner en ny kombinasjon, oppretter det en intern kontrollpost som inneholder informasjonen om kombinasjonen. Planleggingssystemet setter inn lagerføringsenheten som kontrollpost eller ytre løkke. Derfor angis riktige planleggingsparametere i henhold til en kombinasjon av variant og lokasjon, og systemet kan fortsette til den indre løkken. 

> [!NOTE]  
> Du trenger ikke å angi en post for lagerføringsenhet når du registrerer tilbud og etterspørsel for en bestemt kombinasjon av variant og lokasjon. Hvis det ikke finnes en lagerføringsenhet for en bestemt kombinasjon, oppretter derfor [!INCLUDE [prod_short](includes/prod_short.md)] en midlertidig post for lagerføringsenhet basert på dataene fra varen. Hvis vekselbryteren **Lokasjon obligatorisk** er slått på på **siden Lageroppsett**, må du opprette en lagerføringsenhet eller slå på vekslebryteren **Komponenter ved lokasjon**. Finn ut mer under [Planlegg med eller uten lokasjoner](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a><a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Serie- og partinumre lastes inn etter spesifikasjonsnivå

Serie- og partinumre lastes inn i lagerprofiler sammen med tilbudet og etterspørselen som de er tildelt.  

Tilbuds- og etterspørselsattributter ordnes etter prioritet og spesifikasjonsnivå. Siden samsvar med serie- og partinumre gjenspeiler spesifikasjonsnivået, vil et mer spesifikt behov samsvare før et mindre spesifikt behov. Et bestemt behov kan for eksempel være et partinummer som er angitt for en salgslinje. Et mindre spesifikt behov kan være et salg fra et hvilket som helst partinummer.

> [!NOTE]  
> De eneste egne prioriteringsregler for serie- og partinummerert behov og forsyning er spesifikasjonsnivået som defineres av kombinasjonen og hvordan varesporing er konfigurert for varene.  

Under balansering anser planleggingssystemet forsyninger med serie- og partinumre som fleksible. Systemet verken øker eller planlegger slike forsyningsordrer på nytt. Det eneste unntaket er hvis de brukes i en ordre-til-ordre-relasjon. Finn ut mer under [Ordre-til-ordre-koblinger brytes aldri](#order-to-order-links-are-never-broken). Dette unntaket beskytter forsyningen mot mottak av flere, kanskje motstridende, handlingsmeldinger når den har ulike attributter. Det kan for eksempel være at forskjellige attributter er når forsyningen har en samling med forskjellige serienumre.  

En annen grunn til at serie- og partinummer er infleksible er fordi serie- og partinumre ofte tildeles sent i prosessen. Det kan være forvirrende hvis det blir foreslått endringer på dette tidspunktet.  

Balansering av serie- og partinumre overholder ikke regelen om ikke å planlegge noe før den planlagte startdatoen. Hvis tilbud og etterspørsel ikke er synkronisert, vil planleggingssystemet foreslå endringer eller foreslå nye ordrer, uavhengig av den planlagte startdatoen.  

### <a name="order-to-order-links-are-never-broken"></a><a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-koblinger brytes aldri

Når en ordre-til-ordre-vare planlegges, må den koblede forsyningen bare brukes til det den opprinnelig var ment for. Det koblede behovet må ikke dekkes av en annen tilfeldig forsyning, selv om forsyningen er tilgjengelig i tid og antall. Du kan for eksempel ikke bruke en monteringsordre som er koblet til en ordre i et monter-til-ordre-scenario, til å dekke andre behov.  

Ordre-til-ordre-behov og -forsyning må være i nøyaktig balanse. Planleggingssystemet sikrer forsyningen uten å ta hensyn til ordreskaleringsparametere, modifikatorer og antall på lager (bortsett fra antall knyttet til de koblede ordrene). Av samme årsak vil systemet foreslå å redusere overflødige forsyninger hvis det koblede behovet reduseres.  

Denne balanseringen påvirker også tidsberegningen. Det tas ikke hensyn til den begrensede horisonten som gis av tidsperioden. Forsyningen tidsplanlegges på nytt hvis tidsberegningen for behovet er endret. Avdempningstiden blir overholdt, og denne hindrer at ordre-til-ordre-forsyninger planlegges ut, med unntak av interne forsyninger for en flernivås produksjonsordre (prosjektordre).  

> [!NOTE]  
> Serie- og partinumre kan også angis i ordre-til-ordre-behov. I slike tilfeller er ikke forsyningen ufleksible, noe som vanligvis er tilfelle for serie- og partinumre. I slike tilfeller vil systemet øke eller redusere i henhold til behovsendringer. Hvis ett behov har varierende serie- og partinumre, for eksempel flere partinumre, foreslås også én forsyningsordre for hvert parti.  

> [!NOTE]  
> Prognoser skal ikke føre til oppretting av forsyningsordrer som er bundet av en ordre-til-ordre-kobling. Hvis prognosen brukes, bør den bare brukes som en generator for konkrete behov i et produksjonsmiljø.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a><a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov blir lastet inn i henhold til produksjonsordreendringer

Ved håndtering av produksjonsordrer må planleggingssystemet overvåke de nødvendige komponentene før det laster dem inn i behovsprofilen. Komponentlinjer som skyldes en endret produksjonsordre erstatter linjene i den opprinnelige ordren. Endringen sikrer at planleggingssystemet ikke dupliserer planleggingslinjer for et komponentbehov.  

### <a name="consume-safety-stock"></a><a name="consume-safety-stock"></a>Bruk sikkerhetslager

Sikkerhetslagerantallet er et behov som lastes derfor inn i lagerprofilen på den planlagte startdatoen.  

Sikkerhetslager er et lagerantall som er lagt til side for å oppfylle usikkerheter i behovet i etterfyllingslevering. Det kan imidlertid brukes til å oppfylle et behov. I dette tilfellet vil planleggingssystemet sikre at sikkerhetslageret raskt erstattes. Systemet foreslår en forsyningsordre for å etterfylle sikkerhetslagerantallet på den datoen det brukes. Planleggingslinjen viser et unntaksadvarselsikon som informerer at sikkerhetslageret er delvis eller helt forbrukt med en unntaksordre for det manglende antallet.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a><a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognosebehov blir redusert av ordrer

Behovsprognosen uttrykker forventet fremtidig behov. Når faktisk behov registreres, vanligvis som ordrer for produserte varer, forbruker det prognosen.

Selve prognosen reduseres ikke av ordrer. Prognoseantallet som brukes i planleggingsberegningen, blir imidlertid redusert med salgsordreantall før det gjenværende antallet registreres i behovsprofilen. For salg i en periode inkluderer planlegging både åpne ordrer og vareposter fra levert salg. Unntaket fra denne regelen er når de kommer fra en rammeordre.  

Du må definere en gyldig prognoseperiode. Datoen på prognoseantallet angir begynnelsen på perioden, og datoen på neste prognose angir slutten av perioden.  

Prognosen for perioder før planleggingsperioden brukes ikke, uavhengig av om den ble forbrukt. Det første prognosetallet av interesse er enten startdatoen for planlegging eller nærmeste dato til den.  

Prognosen kan være for ulike typer behov:

* Uavhengig behov, for eksempel ordrer
* Avhengig behov, for eksempel produksjonsordrekomponenter.

En vare kan ha begge typer prognoser. Under planleggingen skjer forbruket separat, først for uavhengige behov og deretter for avhengige behov.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a><a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammebestillingsbehov blir redusert av ordrer

Prognosen suppleres av rammeordrer som en måte å angi fremtidige behov fra en bestemt kunde. Som med prognosen (uspesifisert), må faktisk salg bruke den forventede etterspørselen, og det gjenværende antallet bør angi beholdningsprofilen for behov. Forbruket reduserer ikke rammebestillingsantallet.

Planleggingsberegningen inkluderer åpne ordrer som er knyttet til den bestemte rammeordrelinjen, men inkluderer ikke gyldige tidsperioder. Bokførte ordrer er heller ikke inkludert siden bokføringen allerede har redusert det utestående rammeordreantallet.

## <a name="prioritize-orders"></a><a name="prioritize-orders"></a>Prioriter ordrer

Den forespurte eller tilgjengelige datoen representerer den høyeste prioriteten i en gitt lagerføringsenhet. Dagens behov må behandles i forhold til neste ukes behov. I tillegg til denne generelle prioriteten vil planleggingssystemet imidlertid gjøre følgende forslag i henhold til ordreprioritetene:

* Hvilken type behov du må oppfylle først.
* Hvilken forsyningskilde som skal brukes før du bruker andre forsyningskilder.  

Innlastet tilbud og etterspørsel bidrar til en profil for beregnet lager i henhold til prioriteter.  

### <a name="priorities-on-the-demand-side"></a><a name="priorities-on-the-demand-side"></a>Prioriteter på behovssiden

1. Allerede levert: Varepost  
2. Bestillingsretur  
3. Ordre  
4. Serviceordre  
5. Produksjonskomponentbehov  
6. Monteringsordrelinje  
7. Utgående overføringsordre  
8. Rammeordre (som ikke allerede er brukt av tilknyttede ordrer)  
9. Prognose (som ikke allerede er brukt av andre salgsordrer)  

> [!NOTE]  
> Bestillingsreturer tas vanligvis ikke med i forsyningsplanlegging. De skal alltid reserveres fra partiet som skal returneres. Hvis den ikke er reservert, spiller bestillingsreturer en rolle i tilgjengeligheten og er høyt prioritert for å unngå at planleggingssystemet foreslår at en forsyningsordre bare skal fungere som en bestillingsretur.  

### <a name="priorities-on-the-supply-side"></a><a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden

1. Allerede på lager: Varepost (planleggingsfleksibilitet = ingen)  
2. Ordreretur (Planleggingsfleksibilitet = Ingen)  
3. Inngående overføringsordre  
4. Produksjonsordre  
5. Monteringsordre  
6. Bestilling  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a><a name="priority-related-to-the-state-of-supply-and-demand"></a>Prioritet som er knyttet til statusen for behov og forsyning

I tillegg til prioritetene fra typen forsyning og behov, er det andre ting som påvirker planleggingsfleksibiliteten. Det kan for eksempel være lageraktiviteter og statusen til følgende ordrer:

* Salg
* Kjøp
* Overfør
* Montering
* Produksjon

Statusen for disse ordrene har følgende effekter: 

1. Delvis behandlet (Planleggingsfleksibilitet = Ingen)  
2. Allerede i prosessen i lageret (planleggingsfleksibilitet = ingen)  
3. Frigitt – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)  
4. Fast planlagt produksjonsordre (planleggingsfleksibiliteten = ubegrenset)  
5. Planlagt/åpen – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)

## <a name="balancing-supply-with-demand"></a><a name="balancing-supply-with-demand"></a>Balansere behov med forsyning

Planleggingssystemet balanserer forsyning og behov ved å foreslå handlinger for å revidere forsyningsordrer som ikke er balansert. Denne balanseringen skjer for hver kombinasjon av variant og lokasjon.  

Tenk deg at alle lagerprofiler inneholder to strenger:

* En streng med behovshendelser, sortert etter dato og prioritet
* En tilsvarende streng med forsyningshendelser

Hver hendelse henviser til kildetype og identifikasjon. Reglene for balansering av varen er enkle. Samsvar av behov og forsyning kan oppstå når som helst i prosessen, på følgende måte:  

1. Det finnes verken behov eller forsyning for varen = > planleggingen er ferdig (eller skal ikke starte).  
2. Det finnes behov, men ingen forsyning = > forsyning må foreslås.  
3. Det finnes forsyning, men ikke behov for det = > forsyning må avbrytes.  
4. Både behov og forsyning finnes => spørsmål må stilles og besvares før [!INCLUDE [prod_short](includes/prod_short.md)] kan sikre at forsyningen kan oppfylle behovet.

    Hvis tidspunktet for forsyningen ikke passer, kan kanskje forsyningen planlegges på nytt som følger:  

    1. Hvis forsyningen plasseres tidligere enn behovet, kan kanskje forsyningen planlegges ut slik at beholdningen er så lavt som mulig.  
    2. Hvis forsyningen plasseres senere enn behovet, kan kanskje forsyningen planlegges fremover. Hvis ikke vil systemet foreslå ny forsyning.  
    3. Hvis forsyningen oppfyller behovet på datoen, kan planleggingssystemet undersøke om forsyningsantallet kan dekke behovet.  

    Når tidsberegningen er på plass, kan antallet for forsyning beregnes slik:  

    1. Hvis forsyningsantallet er mindre enn behovet, kan forsyningsantallet økes (eller ikke, hvis du har et prinsipp for maksimumsantall).  
    2. Hvis forsyningsantallet er større enn behovet, kan forsyningsantallet reduseres (eller ikke, hvis du har et prinsipp for minimumsantall).  

    På dette tidspunktet finnes en av disse to situasjonene:  

    1. Gjeldende behov kan dekkes, og i så fall kan det lukkes, og planlegging for neste behov kan starte.  
    2. Forsyningen har nådd maksimumet, og noe av behovsmengden er ikke dekket. I slike tilfeller kan planleggingssystemet lukke gjeldende forsyningen og fortsette til den neste.  

 Prosessen starter helt på nytt med det neste behovet og den aktuelle forsyningen eller omvendt. Gjeldende forsyning kan kanskje dekke neste behov også, eller gjeldende behov er ikke fullstendig dekket ennå.  

### <a name="rules-for-actions-for-supply-events"></a><a name="rules-for-actions-for-supply-events"></a>Regler for handlinger for forsyningshendelser

For beregninger ovenfra og ned der forsyningen må oppfylle behov, tas behovet som gitt. Det er utenfor kontrollen til planleggingssystemet. Planleggingssystemet kan imidlertid behandle forsyningssiden og vil komme med følgende forslag:

* Opprett nye forsyningsordrer
* Planlegg eksisterende ordrer på nytt eller endre antall
* Avbryt forsyningsordrer som ikke lenger er nødvendige  

Hvis du vil utelate en forsyningsordre fra planleggingsforslagene, kan du angi at den ikke har planleggingsfleksibilitet (Planleggingsfleksibilitet = ingen). Overflødig forsyning fra denne ordren brukes deretter til å dekke behovet, men ingen handling foreslås. 

All forsyning har vanligvis en planleggingsfleksibilitet som er begrenset av betingelsene i hver av de foreslåtte handlingene.  

* **Tidsplanlegg ut på nytt**: Datoen for en eksisterende forsyningsordre kan tidsplanlegges ut for å oppfylle forfallsdatoen for behovet med mindre følgende gjelder:

  * Den representerer beholdning (alltid på dag null).  
  * Den har en ordre-til-ordre som er koblet til er annet behov.  
  * Det er utenfor vinduet for ny planlegging i tidsperioden.
  * En forsyning som er nærmere, kan brukes.  
  * På den annen side kan brukeren velge ikke å planlegge på nytt fordi:
  * Forsyningsordren er knyttet til et annet behov på en tidligere dato.  
  * Den nye planleggingen som kreves, er så minimal at den er ubetydelig.  

* **Tidsplanlegg inn på nytt**: datoen for en eksisterende forsyningsordre kan tidsplanlegges inn, unntatt når følgende gjelder:

  * Den er koblet direkte til et annet behov.  
  * Det er utenfor vinduet for ny planlegging definert av tidsperioden.

> [!NOTE]  
> Når en vare planlegges ved hjelp av et gjenbestillingspunkt, kan du planlegge forsyningsordren på nytt. Dette skjer ofte i fremoverplanlagte forsyningsordrer som utløses av et gjenbestillingspunkt.

* **Øk antall**: Antallet i en eksisterende forsyningsordre kan økes for å dekke behovet, med mindre forsyningsordren er koblet direkte til et behov med en ordre-til-ordre-kobling.  

> [!NOTE]  
> Selv om du kan øke forsyningsordren, kan økningen være begrenset på grunn av et maksimumsordreantall.  

* **Reduser antall**: En eksisterende forsyningsordre med et overskudd sammenlignet med et eksisterende behov kan reduseres for å dekke behovet.  

> [!NOTE]  
> Selv om antallet kan reduseres, kan det være overskudd sammenlignet med behovet på grunn av et angitt minimumsordreantall eller en bestillingsfaktor. 

* **Avbryt**: Forsyningsordren kan avbrytes som en spesiell hendelse for handlingen for å redusere antallet, hvis den er blitt redusert til null. 
* **Ny**: Hvis det ikke finnes noen forsyningsordrer eller en eksisterende ordre ikke kan endres til å dekke det nødvendige antallet på den etterspurte forfallsdatoen for behovet, blir det foreslått en ny forsyningsordre.  

### <a name="determine-the-supply-quantity"></a><a name="determine-the-supply-quantity"></a>Fastslå forsyningsantall

Du kan definere planleggingsparametere som styrer foreslåtte antall for hver forsyningsordre.  

Når planleggingssystemet beregner antallet for en ny forsyningsordre eller antallet som skal endres i en eksisterende ordre, kan foreslåtte antallet være forskjellig fra det faktiske behovet.  

Hvis maksimumsbeholdning eller fast ordreantall som er valgt, kan det foreslåtte vareantallet økes for å oppfylle det faste antallet eller maksimumslageret. Hvis gjenbestillingsprinsippet bruker et gjenbestillingspunkt, kan antallet i det minste økes for å dekke gjenbestillingspunktet. 

Du kan endre det foreslåtte antallet i denne rekkefølgen:  

1. Ned til maks maksimumsordreantallet.  
2. Opp til det minste bestillingsantallet.  
3. Opp for oppfylle nærmeste bestillingsfaktor.

### <a name="order-tracking-links-during-planning"></a><a name="order-tracking-links-during-planning"></a>Sporingskoblinger under planlegging

For ordresporing under planlegging ordrer planleggingssystemet ordresporingskoblingene på nytt for kombinasjonene av varer, varianter og lokasjoner. Systemet ordner sporingskoblingene på nytt av følgende årsaker:

* For å bekrefte forslagene for alle behov og sikre at alle forsyningsordrer er nødvendige.  
* Ordresporingskoblingene må balanseres på nytt regelmessig.  

Ordresporingskoblinger kommer over tid i ubalanse. Koblingene kommer ut av balanse fordi hele ordresporingsnettverket ikke ordnes på nytt før en behovs- eller forsyningshendelse er lukket.

Før du balansere forsyningen ved behov, sletter planleggingssystemet alle ordresporingskoblinger. Under balanseringsprosessen, når en behovs- eller forsyningshendelse lukkes, oppretter systemet nye ordresporingskoblinger mellom behov og forsyning.  

> [!NOTE]  
> Selv om varen ikke er konfigurert for dynamisk ordresporing, vil planleggingssystemet opprette balanserte sporingskoblinger.

## <a name="close-balanced-supply-and-demand"></a><a name="close-balanced-supply-and-demand"></a>Lukk balansert tilbud og etterspørsel

Balansering av forsyning har tre mulige resultater:

* Nødvendig antall og dato for behovshendelsene er dekket, og planleggingen for dem kan lukkes. Forsyningshendelsen forblir åpen og kan være i stand til å dekke neste behov. Å holde forsyningshendelsen åpne gjør at balanseringsprosedyren kan starte på nytt med det nåværende forsyingshendelse og neste behov.  
* Forsyningsordren kan ikke endres slik at den dekker alle behov. Behovshendelsen er fortsatt åpen, med et ikke-dekket antall som kan dekkes av neste forsyningshendelse. Nåværende forsyningshendelse blir dermed lukket, og balanseringen kan starte på nytt med det nåværende behovet og neste forsyningshendelse.  
* All etterspørsel er dekket og det er ikke et neste behov (eller det er ingen behov i det hele tatt). Overskuddsforsyning kan bli redusert (eller avbrutt) og deretter lukkes. Alle andre forsyningshendelser må også avbrytes.  

Til slutt oppretter planleggingssystemet en ordresporingskoblingen mellom forsyning og behov.  

### <a name="create-the-planning-line-suggested-action"></a><a name="create-the-planning-line-suggested-action"></a>Opprett planleggingslinjen (foreslått handling)

Hvis det foreslås en handling, **Ny**, **Endre antall**, **Tidsplanlegg på nytt**, **Tidsplanlegg på nytt og endre antallet** eller **Avbryt**, for å endre forsyningsordren, oppretter planleggingssystemet en planleggingslinje i planleggingsforslaget. For ordresporing opprettes planleggingslinjen ikke bare når forsyningshendelsen er lukket, men også hvis behovshendelsen er lukket. Dette gjelder selv om forsyningshendelsen fremdeles er åpen og kan endres når neste behovshendelse behandles. Planleggingslinjen kan den endres på nytt når den er opprettet.

Hvis du vil redusere belastningen i databasen ved håndtering av produksjonsordrer, kan planleggingslinjen opprettholdes på tre nivåer:

* Opprett bare planleggingslinjen med gjeldende forfallsdato og antall, men uten ruting og komponenter.  
* Inkluder ruting: Den planlagte ruten inkluderer beregning av start- og sluttdatoer og -klokkeslett. Inkluder ruting er krevende når det gjelder databasetilgang. For å fastslå slutt- og forfallsdatoene blir det kanskje nødvendig å beregne rutingen selv om forsyningshendelsen ikke er lukket. Hvis du for eksempel bruker planlegging fremover.  
* Ta med stykklisteutfoldelse: Dette kan skje like før forsyningshendelsen lukkes.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
