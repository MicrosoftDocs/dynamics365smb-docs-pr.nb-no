---
title: Designdetaljer – Balansere behov og forsyning
description: For å forstå hvordan planleggingssystemet fungerer, er det nødvendig å forstå de prioriterte målene i planleggingssystemet oppnådd ved å balansere behov med etterspørsel..
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 8ff08e03196aac03a9e57519f47a37e284e8c9ff
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442513"
---
# <a name="design-details-balancing-demand-and-supply"></a>Designdetaljer: Balansere behov og forsyning
For å forstå hvordan planleggingssystemet fungerer, er det nødvendig å forstå de prioriterte målene i planleggingssystemet, og det viktigste er å sikre at følgende oppfylles:  

- Alle behov blir oppfylt av tilstrekkelig forsyning.  
- Eventuell forsyning har et formål.  

 Vanligvis oppnås disse målene ved å balansere forsyning med behov.  

## <a name="demand-and-supply"></a>Behov og forsyning
 Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel ordre- og komponentbehov fra en produksjonsordre. I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.  

  Forsyning er den vanlige betegnelsen som brukes om alle typer positive eller inngående antall, for eksempel beholdning, kjøp, montering, produksjon eller inngående overføringer. I tillegg kan en ordreretur også representere forsyning.  

  For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler. Én profil inneholder behovshendelser, og den andre inneholder tilsvarende forsyningshendelser. Hver hendelse representerer én ordrenettverksenhet, for eksempel en salgsordrelinje, en varepost eller en produksjonsordrelinje.  

  Når du beholdningsprofiler lastes inn, balanseres de ulike settene med behov/forsyning for å gi en forsyningsplan som oppfyller de angitte målene.  

  Planleggingsparametre og lagernivåer er henholdsvis andre typer behov og forsyning som gjennomgå integrert balansering for å etterfylle lagervarer. Hvis du vil ha mer informasjon, se [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Kort om begrepet balansering
  Behovet er gitt av selskapets kunder. Forsyning er det selskapet kan opprette og fjerne for å skape balanse. Planleggingssystemet starter med det uavhengige behovet og sporer deretter bakover til forsyningen.  

   Beholdningsprofilene brukes til å lagre informasjon om behov og forsyninger, antall og tidsberegning. Disse profilene utgjør i hovedsak de to sidene av balanseringsskalaen.  

   Formålet med planleggingsmekanismen er å utligne behovet for og forsyningen av en vare for å sikre at forsyningen samsvarer med behovet, og å gjøre dette på en passende måte som defineres av planleggingsparameterne og -reglene.  

   ![Oversikt over balansering mellom forsyningen og behov.](media/nav_app_supply_planning_2_balancing.png "Oversikt over balansering mellom forsyningen og behov")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Håndtere ordrer før den planlagte startdatoen
For å unngå at en leveringsplan viser umulige og dermed ubrukelige forslag, regner planleggingssystemet perioden frem til den planlagte startdatoen som en frossen sone der ingenting er planlagt. Følgende regel gjelder den frosne sonen:  

Alle tilbud og etterspørsel før startdatoen for planleggingsperioden blir betraktet som en del av beholdningen eller levert.  

Planleggingssystemet vil derfor ikke, med noen få unntak, foreslå endringer for forsyningsordrer i den frosne sonen, og ingen koblinger for ordresporing opprettes eller vedlikeholdes for denne perioden.  

Unntakene fra denne regelen er som følger:  

   * Hvis forventet disponibel beholdning, inkludert summen av forsyning og behov i den frosne sonen, er under null.  
   * Hvis serie-/partinumre er nødvendige på tilbakedaterte ordre(r).  
   * Hvis forsyningsbehovsettet er koblet til et ordre-til-ordre-prinsipp.  

Hvis den første disponible beholdningen er under null, foreslår planleggingssystemet en kritisk ordre på dagen før planleggingsperioden, for å dekke antallet som mangler. Forventet og tilgjengelige beholdning vil derfor alltid være minst null når planlegging for den fremtidige perioden begynner. Planleggingslinjen for denne forsyningsordren har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/partinumre og ordre-til-ordre-koblinger er fritatt fra den frosne sonen  
   Hvis serie-/partinumre er nødvendige eller det finnes en ordre-til-ordre-kobling, vil planleggingssystemet se bort fra den frosne sonen og inkludere slike antall som er tilbakedaterte fra startdatoen og potensielt foreslå korrigerende handlinger hvis behov og forsyning ikke er synkronisert. Forretningsårsaken til dette prinsippet er at slike bestemte sett med behov/forsyning må samsvare for å sikre at dette bestemte behovet dekkes.

## <a name="loading-the-inventory-profiles"></a>Laste inn lagerprofiler
For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler.  

De vanlige typene behov og forsyning med forfallsdatoer på eller etter den planlagte startdatoen lastes inn i hver beholdningsprofil. Når de er lastet inn, sorteres de ulike behovs og forsyningstypene i henhold til generelle prioriteter, for eksempel forfallsdato, lavnivåkoder, lokasjon og variant. I tillegg brukes ordreprioriteter på de forskjellige typene for å sikre at det viktigste behovet oppfylles først. Hvis du vil ha mer informasjon, kan du se [Prioritere ordrer](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Behov kan også være negative, som nevnt tidligere. Dette betyr at det må behandles som forsyning. I motsetning til vanlige typer forsyning regnes imidlertid negativt behov som fast forsyning. Planleggingssystemet kan ta det med i betraktningen, men foreslår ingen endringer av det.  

Planleggingssystemet tar vanligvis hensyn til alle forsyningsordrer etter den planlagte startdatoen som kan endres for å dekke behovet. Så snart et antall er bokført fra en ordre, kan den imidlertid ikke lenger endres av planleggingssystemet. Følgende forskjellige ordrer kan derfor ikke planlegges på nytt:  

- Frigitte produksjonsordrer der forbruk eller avgang er bokført.  
- Monteringsordre der forbruk eller avgang er bokført.  
- Overføringsordrer der leveringen er bokført.  
- Bestillinger der mottaket er bokført.  

I tillegg til å laste inn behovs- og forsyningstyper, blir bestemte typer lastet inn med oppmerksomhet på spesialregler og avhengigheter som er beskrevet nedenfor.  

### <a name="item-dimensions-are-separated"></a>Varedimensjoner atskilles  
Forsyningsplanen må beregnes per kombinasjon av varedimensjonene, for eksempel variant og lokasjon. Det er imidlertid ingen grunn til å beregne teoretisk kombinasjoner. Bare kombinasjonene som inneholder behov og/eller forsyning må beregnes.  

Planleggingssystemet kontrollerer dette ved å kjøre gjennom beholdningsprofilen. Når det blir funnet en ny kombinasjon, oppretter programmet en intern kontrollpost som inneholder den faktiske kombinasjonsinformasjonen. Programmet setter inn LFEen som kontrollpost eller ytre løkke. Derfor angis riktige planleggingsparametre i henhold til en kombinasjon av variant og lokasjon, og programmet kan fortsette til den indre løkken.  

> [!NOTE]  
>  Programmet krever ikke at brukerne angir en LFE-post når de registrerer behov og/eller forsyning for en bestemt kombinasjon av variant og lokasjon. Hvis det ikke finnes en LFE for en bestemt kombinasjon, oppretter derfor programmet sin egen midlertidige LFE-post basert på varekortdataene. Hvis Lokasjon obligatorisk er satt til Ja på siden Lageroppsett, må du opprette en SKU, eller Komponenter ved lokasjon må være satt til Ja. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Behov på tom lokasjon](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/partinumre lastes inn etter spesifikasjonsnivå  
Attributter i form av serie-/ partinumre lastes inn i lagerprofiler sammen med behovet og forsyningen som de er tilordnet.  

Behovs- og forsyningsattributter ordnes etter prioritet og spesifikasjonsnivå. Siden treff for serie-/partinumre gjenspeiler spesifikasjonsnivået, vil mer spesifikke behov, for eksempel et partinummer valgt spesielt for en salgslinje, søke samsvar før mindre spesifikke behov, for eksempel et salg fra et hvilken som helst valgt partinummer.  

> [!NOTE]  
>  Det finnes ingen egne prioriteringsregler for serie-/partinummerert behov og forsyning utenom spesifikasjonsnivået som defineres av kombinasjonen av serie- og partinumre for dem og varesporingsoppsettet for de involverte varene.  

Under balansering betrakter planleggingssystemet forsyning med serie-/partinumre som ufleksibel, og vil ikke prøve å øke eller planlegge slike forsyningsordrer på nytt (med mindre de brukes i en ordre for ordre-relasjon). Se Ordre-til-ordre-koblinger brytes aldri). Dette beskytter forsyningen mot mottak av flere, kanskje motstridende, handlingsmeldinger når en forsyning har ulike attributter, for eksempel en samling med ulike serienumre.  

En annen årsak til at serie-/partinummerert forsyning ikke er fleksible, et at serie-/partinumre vanligvis tilordnes så sent i prosessen at det kan være forvirrende hvis det foreslås endringer.  

Balanseringen av serie-/partinumre tar ikke hensyn til den *frosne sonen*. Hvis behov og forsyning ikke er synkronisert, vil planleggingssystemet foreslå endringer eller foreslå nye ordrer, uavhengig av den planlagte startdatoen.  

### <a name="order-to-order-links-are-never-broken"></a>Ordre-til-ordre-koblinger brytes aldri  
Når en ordre-til-ordre-vare planlegges, kan ikke den koblede forsyningen brukes til noe annet behov enn det den opprinnelig var ment for. Det koblede behovet må ikke dekkes av en annen tilfeldig forsyning, selv om den er tilgjengelig i tid og antall i den aktuelle situasjonen. En monteringsordre som er koblet til en ordre i et monter-til-ordre-scenario, kan for eksempel ikke brukes til å dekke andre behov.  

Ordre-til-ordre-behov og -forsyning må være i nøyaktig balanse. Planleggingssystemet sikrer forsyningen under alle omstendigheter uten å ta hensyn til ordreskaleringsparametere, modifikatorer og antall på lager (bortsett fra antall knyttet til de koblede ordrene). Av samme årsak vil systemet foreslå å redusere overflødige forsyninger hvis det koblede behovet reduseres.  

Denne balanseringen påvirker også tidsberegningen. Det tas ikke hensyn til den begrensede horisonten som gis av tidsperioden. Forsyningen tidsplanlegges på nytt hvis tidsberegningen for behovet er endret. Avdempningstiden blir overholdt, og denne hindrer at ordre-til-ordre-forsyninger planlegges ut, med unntak av interne forsyninger for en flernivås produksjonsordre (prosjektordre).  

> [!NOTE]  
>  Serie-/partinumre kan også angis i ordre-til-ordre-behov. I slike tilfeller betraktes ikke forsyningen som ufleksible som standard, noe som vanligvis er tilfelle for serie-/partinumre. I slike tilfeller vil systemet øke/redusere i henhold til behovsendringer. Hvis ett behov har varierende serie-/partinumre tall, for eksempel flere partinumre, foreslås også én forsyningsordre per parti.  

> [!NOTE]  
>  Prognoser skal ikke føre til oppretting av forsyningsordrer som er bundet av en ordre-til-ordre-kobling. Hvis prognosen brukes, bør den bare brukes som en generator for konkrete behov i et produksjonsmiljø.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Komponentbehov blir lastet inn i henhold til produksjonsordreendringer  
Ved håndtering av produksjonsordrer må planleggingssystemet overvåke de nødvendige komponentene før det laster dem inn i behovsprofilen. Komponentlinjer som skyldes en endret produksjonsordre erstatter linjene i den opprinnelige ordren. Dette betyr at planleggingssystemet sikrer at planleggingslinjer for komponentbehov aldri blir duplisert.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Sikkerhetslager kan forbrukes  
Sikkerhetslagerantallet er først og fremst en behovstype og lastes derfor inn i beholdningsprofilen på den planlagte startdatoen.  

Sikkerhetslager er et lagerantall som er lagt til side for å kompensere for usikkerheter i behovet i etterfyllingsleveringstiden. Dette kan imidlertid brukes hvis det er nødvendig å ta fra det å oppfylle et behov. I slike tilfeller sikrer planleggingssystemet at sikkerhetslageret raskt erstattes, ved å foreslå en forsyningsordre for å etterfylle sikkerhetslagerantallet på datoen den forbrukes. Denne planleggingslinjen viser et unntaksadvarselsikon som informerer planleggeren om at sikkerhetslageret er delvis eller helt forbrukt med en unntaksordre for det manglende antallet.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognosebehov blir redusert av ordrer  
Behovsprognosen uttrykker forventet fremtidig behov. Når faktisk behov registreres, vanligvis som ordrer for produserte varer, forbruker det prognosen.  

Selve prognosen reduseres faktisk ikke av ordrer. Den forblir den samme. Prognoseantallet som brukes i planleggingsberegningen, blir imidlertid redusert (med salgsordreantall) før det gjenværende antallet, hvis det finnes, registreres i beholdningsprofilen for behov. Når planleggingssystemet undersøker faktisk salg i en periode, blir både åpne ordrer og vareposter fra leverte salg tatt med, med mindre de er avledet fra en rammeordre.  

Det kreves at en bruker angir en gyldig prognoseperioden. Datoen på prognoseantallet angir begynnelsen på perioden, og datoen på neste prognose angir slutten av perioden.  

Prognosen for perioder før planleggingsperioden brukes ikke, uavhengig av om den ble forbrukt eller ikke. Det første prognosetallet av interesse er enten samme dato som den planlagte startdatoen eller nærmeste dato før den planlagte startdatoen.  

Prognosen kan være for uavhengig behov, for eksempel ordrer, eller avhengig behov, for eksempel produksjonsordrekomponenter (modulprognose). En vare kan ha begge typer prognoser. Under planleggingen foregår forbruket separat, først for uavhengige behov og deretter for avhengige behov.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Rammebestillingsbehov blir redusert av ordrer  
Prognosen suppleres av rammeordren som et middel for å angi fremtidige behov fra en bestemt kunde. Som med prognosen (uspesifisert), må faktisk salg bruke den forventede etterspørselen, og det gjenværende antallet bør angi beholdningsprofilen for behov. Forbruket reduserer ikke rammebestillingen.  

Planleggingsberegningen tar hensyn til åpne ordrer som er knyttet til den bestemte rammeordrelinjen, men tar ikke hensyn til gyldige tidsperioder. Det tas heller ikke hensyn til bokførte ordrer, siden bokføringen allerede har redusert det utestående rammeordreantallet.

## <a name="prioritizing-orders"></a>Prioritere ordrer
I en gitt LFE representerer ønsket eller tilgjengelig dato den høyeste prioriteten. Behovet i dag bør håndteres før behovet i neste uke. I tillegg til denne generelle prioriteten vil planleggingssystemet også foreslå hvilken type behov som må være oppfylt før andre behov oppfylles. Det vil foreslå hvilken forsyningskilde som skal brukes før du bruker andre forsyningskilder. Dette gjøres i henhold til ordreprioriteter.  

Innlastet behov og forsyning bidrar til en profil for den beregnede beholdningen i henhold til følgende prioriteter:  

### <a name="priorities-on-the-demand-side"></a>Prioriteter på behovssiden  
1. Allerede levert: Varepost  
2. Bestillingsretur  
3. Ordre  
4. Serviceordre  
5. Produksjonskomponentbehov  
6. Monteringsordrelinje  
7. Utgående overføringsordre  
8. Rammebestilling (som ikke allerede er brukt av tilknyttede salgsordrer)  
9. Prognose (som ikke allerede er brukt av andre salgsordrer)  

> [!NOTE]  
>  Bestillingsreturer tas vanligvis ikke med i forsyningsplanlegging. De skal alltid reserveres fra partiet som skal returneres. Hvis den ikke er reservert, spiller bestillingsreturer en rolle i tilgjengeligheten og er høyt prioritert for å unngå at planleggingssystemet foreslår at en forsyningsordre bare skal fungere som en bestillingsretur.  

### <a name="priorities-on-the-supply-side"></a>Prioriteter på forsyningssiden  
1. Allerede på lager: Varepost (planleggingsfleksibilitet = ingen)  
2. Ordreretur (Planleggingsfleksibilitet = Ingen)  
3. Inngående overføringsordre  
4. Produksjonsordre  
5. Monteringsordre  
6. Bestilling  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioritet som er knyttet til statusen for behov og forsyning  
I tillegg til prioriteter som er angitt av behov og forsyning, definerer den nåværende ordretilstanden i utføringsprosessen, en prioritet. Lageraktiviteter har for eksempel innvirkning, og det tas hensyn til statusen for salgs-, kjøps-, overførings-, monterings- og produksjonsordrer:  

1. Delvis behandlet (Planleggingsfleksibilitet = Ingen)  
2. Allerede i prosessen i lageret (planleggingsfleksibilitet = ingen)  
3. Frigitt – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)  
4. Fast planlagt produksjonsordre (planleggingsfleksibiliteten = ubegrenset)  
5. Planlagt/åpen – alle ordretyper (Planleggingsfleksibilitet = Ubegrenset)

## <a name="balancing-supply-with-demand"></a>Balansere behov med forsyning
Kjernen i planleggingssystemet omfatter balansering av behov og forsyning ved å foreslå brukerhandlinger som endrer forsyningsordrene hvis det oppstår ubalanse. Dette skjer per kombinasjon av variant og lokasjon.  

Tenk deg at hver lagerprofil inneholder en streng med behovshendelser (sortert etter dato og prioritet) og en tilsvarende streng for forsyningshendelser. Hver hendelse refererer tilbake til kildetype og identifikasjon. Reglene for utligning av varen er enkle. Fire forekomster av tilsvarende behov og forsyning kan oppstå når som helst i prosessen:  

1. Det finnes verken behov eller forsyning for varen = > planleggingen er ferdig (eller skal ikke starte).  
2. Det finnes behov, men ingen forsyning = > forsyning må foreslås.  
3. Det finnes forsyning, men ikke behov for det = > forsyning må avbrytes.  
4. Både behov og forsyning finnes => spørsmål må stilles og besvares før systemet kan sikre at behovet kan dekkes og forsyningen er tilstrekkelig.  

    Hvis tidspunktet for forsyningen ikke passer, kan kanskje forsyningen planlegges på nytt som følger:  

    1.  Hvis forsyningen plasseres tidligere enn behovet, kan kanskje forsyningen planlegges ut slik at beholdningen er så lavt som mulig.  
    2.  Hvis forsyningen plasseres senere enn behovet, kan kanskje forsyningen planlegges inn. Hvis ikke vil systemet foreslå ny forsyning.  
    3.  Hvis forsyningen oppfyller behovet på datoen, kan planleggingssystemet fortsette å undersøke om forsyningsantallet kan dekke behovet.  

    Når tidsberegningen er på plass, kan det tilstrekkelig antallet som skal leveres, beregnes slik:  

    1.  Hvis forsyningsantallet er mindre enn behovet, kan det hende at forsyningsantallet kan reduseres (eller ikke, hvis det er begrenset av et prinsipp for maksimumsantall).  
    2.  Hvis forsyningsantallet er større enn behovet, kan det hende at forsyningsantallet kan reduseres (eller ikke, hvis det er begrenset av et prinsipp for minimumsantall).  

    På dette tidspunktet finnes en av disse to situasjonene:  

    1.  Gjeldende behov kan dekkes, og i så fall kan det lukkes, og planlegging for neste behov kan starte.  
    2.  Forsyningen har nådd maksimumet, og noe av behovsmengden er ikke dekket. I slike tilfeller kan planleggingssystemet lukke gjeldende forsyningen og fortsette til den neste.  

 Prosessen starter helt på nytt med det neste behovet og den aktuelle forsyningen eller omvendt. Gjeldende forsyning kan kanskje dekke neste behov også, eller gjeldende behov er ikke fullstendig dekket ennå.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regler vedrørende handlinger for forsyningshendelser  
Når planleggingssystemet utfører en beregning ovenfra og nedover der forsyning må dekke behov, tas behovet som gitt, det vil si at planleggingssystemet ikke kan kontrollere det. Forsyningssiden kan Imidlertid administreres. Planleggingssystemet foreslår derfor å opprette nye forsyningsordrer, tidsplanlegge eksisterende på nytt og/eller endre ordreantallet. Hvis en eksisterende forsyningsordre blir overflødige foreslår planleggingssystemet at brukeren avbryter den.  

Hvis brukeren vil utelate en eksisterende forsyningsordre fra planleggingsforslagene, kan det angis at den ikke har planleggingsfleksibilitet (Planleggingsfleksibilitet = ingen). Overflødig forsyning fra denne ordren brukes deretter til å dekke behovet, men ingen handling foreslås.  

All forsyning har vanligvis en planleggingsfleksibilitet som er begrenset av betingelsene i hver av de foreslåtte handlingene.  

-   **Tidsplanlegg ut på nytt**: Datoen for en eksisterende forsyningsordre kan tidsplanlegges ut for å oppfylle forfallsdatoen for behovet med mindre følgende gjelder:  

    -   Den representerer beholdning (alltid på dag null).  
    -   Den har en ordre-til-ordre som er koblet til er annet behov.  
    -   Dette ligger utenfor siden for å planlegge på nytt, som angitt av tidsperioden.  
    -   En forsyning som er nærmere, kan brukes.  
    -   På den annen side kan brukeren velge ikke å planlegge på nytt fordi:  
    -   Forsyningsordren er allerede knyttet til et annet behov på en tidligere dato.  
    -   Den nye planleggingen som kreves, er så minimal at brukeren synes den er ubetydelig.  

-   **Tidsplanlegg inn på nytt**: datoen for en eksisterende forsyningsordre kan tidsplanlegges inn, unntatt når følgende gjelder:  

    -   Den er koblet direkte til et annet behov.  
    -   Dette ligger utenfor siden for å planlegge på nytt, som angitt av tidsperioden.  

> [!NOTE]  
>  Når en vare planlegges ved hjelp av et gjenbestillingspunkt, kan forsyningsordren alltid om nødvendig tidsplanlegges inn. Dette er vanlig i fremoverplanlagte forsyningsordrer som utløses av et gjenbestillingspunkt.  

-   **Øk antall**: Antallet i en eksisterende forsyningsordre kan økes for å dekke behovet, med mindre forsyningsordren er koblet direkte til et behov med en ordre-til-ordre-kobling.  

> [!NOTE]  
>  Selv om det er mulig å øke forsyningsordren, kan det være begrenset på grunn av et maksimumsordreantall.  

-   **Reduser antall**: En eksisterende forsyningsordre med et overskudd sammenlignet med et eksisterende behov kan reduseres for å dekke behovet.  

> [!NOTE]  
>  Selv om antallet kan reduseres, kan det fortsatt være noen overskudd sammenlignet med behovet på grunn av et angitt minimumsordreantall eller en bestillingsfaktor.  

-   **Avbryt**: Forsyningsordren kan avbrytes som en spesiell hendelse for handlingen for å redusere antallet, hvis den er blitt redusert til null.  
-   **Ny**: Hvis det ikke allerede finnes en forsyningsordre eller en eksisterende ikke kan endres til å dekke det nødvendige antallet på den etterspurte forfallsdatoen, blir det foreslått en ny forsyningsordre.  

### <a name="determining-the-supply-quantity"></a>Fastslå forsyningsantall  
Planleggingsparametre angitt av brukeren, styrer foreslåtte antall for hver ordre.  

Når planleggingssystemet beregner antallet for en ny forsyningsordre eller det endrede antallet i en eksisterende, kan foreslåtte antallet være forskjellig fra antallet det faktisk er behov for.  

Hvis maksimumsbeholdning eller fast ordreantall som er valgt, kan det foreslåtte vareantallet økes for å oppfylle det faste antallet eller maksimumsbeholdningen. Hvis gjenbestillingsprinsippet bruker et gjenbestillingspunkt, kan antallet i det minste økes for å dekke gjenbestillingspunktet.  

 Du kan endre det foreslåtte antallet i denne rekkefølgen:  

1. Ned til maks maksimumsordreantallet (hvis det finnes).  
2. Opp til det minste bestillingsantallet.  
3. Opp for oppfylle nærmeste bestillingsfaktor. (Dette kan bryte med maksimumsordreantallet ved feile innstillinger.)  

### <a name="order-tracking-links-during-planning"></a>Sporingskoblinger under planlegging  
Når det gjelder sporing under planleggingen, er det viktig å nevne at planleggingssystemet ordner de dynamisk opprettede sporingskoblingene for vare-/variant-/lokasjonskombinasjoner.  

Det er to årsaker til dette:  

-   Planleggingssystemet må kunne justere forslagene, slik at alle behov dekkes, og at ingen forsyningsordrer er overflødige.  
-   Sporingskoblinger som er opprettet dynamisk må balanseres på nytt regelmessig.  

Over tid kommer dynamiske sporingskoblinger ut av balanse fordi hele ordrensporingsnettverket ikke endres på nytt før en behovs- eller forsyningshendelse faktisk er lukket.  

Før du balansere forsyningen ved behov, slettes alle eksisterende sporingskoblinger. Når en en behovs- eller forsyningshendelse deretter lukkes under balanseringsprosessen, oppretter det nye sporingskoblinger mellom behov og forsyning.  

> [!NOTE]  
>  Selv om varen ikke er konfigurert for dynamisk ordresporing, vil det planlagte systemet opprette balanserte sporingskoblinger, som beskrevet ovenfor.
## <a name="closing-demand-and-supply"></a>Lukke behov og forsyning
Når balanseringsprosessene for forsyning er utført, er det tre mulige sluttsituasjoner:  

* Nødvendig antall og dato for behovshendelsene er dekket, og planleggingen for dem kan lukkes. Forsyningshendelsen er fortsatt åpen og kan kanskje dekke neste behov, slik at balanseringsprosessen kan starte på nytt med den gjeldende forsyningshendelsen og neste behov.  
* Forsyningsordren kan ikke endres slik at den dekker alle behov. Behovshendelsen er fortsatt åpen, med et ikke-dekket antall som kan dekkes av neste forsyningshendelse. Gjeldende forsyningshendelse blir dermed lukket, slik at balanseringen kan starte på nytt med det gjeldende behovet og neste forsyningshendelse.  
* All etterspørsel er dekket. Det er ingen etterfølgende etterspørsel (eller det er ingen etterspørsel i det hele tatt). Hvis det finnes overskuddsforsyning, kan den reduseres (eller avbrytes) og deretter lukkes. Det kan hende det finnes flere forsyningshendelser videre i kjeden, og de må også avbrytes.  

Til slutt oppretter planleggingssystemet en ordresporingskoblingen mellom forsyning og behov.  

### <a name="creating-the-planning-line-suggested-action"></a>Opprette planleggingslinjen (foreslått handling)  
Hvis det foreslås en handling, Ny, Endre antall, Tidsplanlegg på nytt, Tidsplanlegg på nytt og endre antallet eller Avbryt, for å endre forsyningsordren, oppretter planleggingssystemet en planleggingslinje i planleggingsforslaget. Planleggingslinjen opprettes på grunn av ordresporing, ikke bare når forsyningshendelsen lukkes, men også hvis behovshendelsen lukkes, selv om forsyningshendelsen fremdeles er åpen og kan endres når neste behovshendelse behandles. Dette betyr at når planleggingslinjen først opprettes, kan den endres på nytt.  

Du kan minimere databasetilgang ved håndtering av produksjonsordrer ved å vedlikeholde planleggingslinjen på tre nivåer og samtidig prøve å utføre det minst krevende vedlikeholdsnivået:  

* Opprett bare planleggingslinjen med gjeldende forfallsdato og antall, men uten ruting og komponenter.  
* Inkluder ruting: Den planlagte ruten settes opp, herunder beregning av start- og sluttdatoer og -klokkeslett. Dette er krevende når det gjelder databasetilgang. For å fastslå slutt- og forfallsdatoene blir det kanskje nødvendig å beregne dette selv om forsyningshendelsen ikke er lukket (når det gjelder planlegging fremover).  
* Ta med stykklisteutfoldelse: Dette kan vente til like før forsyningshendelsen lukkes.  

Med dette avsluttes beskrivelsene av hvordan behov og forsyning lastes, prioriteres og balanseres av planleggingssystemet. I integrering med denne aktiviteten for forsyningsplanlegging, må systemet sikre at nødvendig lagernivå opprettholdes for hver planlagt vare i henhold til sine gjenbestillingsprinsippene.

## <a name="see-also"></a>Se også  
 [Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]