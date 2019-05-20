---
title: Designdetaljer – Håndtere gjenbestillingsprinsipper | Microsoft-dokumentasjon
description: Oversikt over oppgaver for å definere en gjenbestillingspolicy ved forsyningsplanlegging.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 69f9f1f2f63e1d16ec1ef4980c00d21bada06166
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245783"
---
# <a name="design-details-handling-reordering-policies"></a>Designdetaljer: Håndtere gjenbestillingsprinsipper
Det må angis et gjenbestillingsprinsipp for at en vare skal kunne delta i forsyningsplanlegging. Det finnes fire gjenbestillingsprinsipper:  

* Fast gjenbest.ant.  
* Maks.ant.  
* Bestilling  
* Parti for parti  

Prinsippene Fast gjenbest.ant., og Maks.ant. som er relatert til lagerplanlegging. Selv om lagerplanlegging teknisk sett er enklere enn fremgangsmåten for balansering, må disse policyene eksistere sammen med trinnvise balansering av forsynings- og ordresporing. For å styre integrasjonen mellom dem og gi innsikt i planleggingslogikken som er involvert, finnes det strenge regler som bestemmer hvordan gjenbestillingsprinsipper skal håndteres.  

## <a name="the-role-of-the-reorder-point"></a>Rollen til gjenbestillingspunktet
I tillegg til generell balansering av tilbud og etterspørsel må systemet også overvåke lagernivåer for de berørte varene for å overholde angitte gjenbestillingsprinsipper.  

Et gjenbestillingspunkt representerer etterspørselen i løpet av leveringstiden. Når den beregnede beholdningen går under lagernivået som defineres av gjenbestillingspunktet, er det på tide å bestille mer. I mellomtiden forventes det at beholdningen gradvis reduseres og kanskje blir null (eller sikkerhetslagernivået) til etterfyllingen kommer.  

Planleggingssystemet vil foreslå en fremoverplanlagt forsyningsordre når den forventede beholdning blir lavere enn gjenbestillingspunktet.  

Gjenbestillingspunktet gjenspeiler et bestemt beholdningsnivå. Lagernivåer kan imidlertid endre seg betydelig i tidsperioden, og planleggingssystemet må derfor konstant overvåke beregnet disponibel beholdning.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Overvåke forventet lagernivå og gjenbestillingspunkt
Beholdning er en type forsyning, men for lagerplanlegging skiller planleggingssystemet mellom to lagernivåer:  

* Beregnet beholdning  
* Forventet disponibel beholdning  

### <a name="projected-inventory"></a>Beregnet lager  
I utgangspunktet er den beregnede beholdningen antallet bruttobeholdning, inkludert forsyning og behov i fortiden, selv om det ikke er bokført, når du starter planleggingen. I fremtiden blir dette et glidende beregnet beholdningsnivå som vedlikeholdes av bruttoantallene fra fremtidig forsyning og behov, fordi de innføres langs tidslinjen (reservert eller tildelt på andre måter).  

Den beregnede beholdningen brukes av planleggingssystemet til å overvåke gjenbestillingspunktet, og til å bestemme gjenbestillingsantallet når gjenbestillingsprinsippet Maks.ant. brukes.  

### <a name="projected-available-inventory"></a>Forventet disponibel beholdning  
Den forventede disponible beholdningen er delen av den beregnede beholdningen som på et gitt tidspunkt er disponibelt for å dekke behov. Den forventede disponible beholdningen brukes av planleggingsmotoren ved overvåking av sikkerhetslagernivået.  

Den forventede disponible beholdningen brukes av planleggingssystemet til å overvåke sikkerhetslagernivået, siden sikkerhetslageret alltid må være disponibelt for å dekke uventet behov.  

### <a name="time-buckets"></a>Tidsperioder  
Det er svært viktig å ha god kontroll over det beregnede lagernivået for å oppdage når gjenbestillingspunktet nås eller overskrides og for å beregne riktig ordreantall gjenbestillingsprinsippet Maks.ant. brukes.  

Som nevnt tidligere, blir forventet lagernivå beregnet ved starten av planleggingsperioden. Det er et bruttonivå som ikke tar hensyn til reservasjoner og lignende fordelinger. For å overvåke dette beholdningsnivået i løpet av planleggingssekvensen overvåker systemet de aggregerte endringene gjennom en tidsperiode. Systemet sikrer at tidsperioden er minst én dag, siden dette er den mest nøyaktige tidsenheten for en behovs- eller forsyningshendelse.  

### <a name="determining-the-projected-inventory-level"></a>Fastslå forventet beholdningsnivå  
Følgende sekvens beskriver hvordan det forventede beholdningsnivået fastsettes:  

* Når en forsyningshendelse, for eksempel en bestilling er helt planlagt, økes den beregnede beholdningen på forfallsdatoen.  
* Når en behovshendelse er fullstendig dekket, reduserer den ikke den beregnede beholdningen med en gang. I stedet bokføres en reduksjonspåminnelse, som er en intern post som inneholder dato og antall for bidrag til den beregnede beholdningen.  
* Når en påfølgende forsyningshendelse planlegges og plasseres på tidslinjen, undersøkes de bokførte reduksjonspåminnelsene enkeltvis frem til den planlagte datoen for forsyningen samtidig som den beregnede beholdningen oppdateres. Under denne prosessen kan det hende at gjenbestillingspunktnivået for påminnelsen om intern økning nås eller passeres.  
* Hvis en ny forsyningsordre blir introdusert, kontrollerer systemet om det er angitt før gjeldende forsyning. Hvis det er tilfelle, blir den nye forsyningen gjeldende forsyning og balanseringen starter på nytt.  

Nedenfor vises en grafisk illustrasjon av dette prinsippet:  

![Fastslå forventet lagernivå](media/nav_app_supply_planning_2_projected_inventory.png "Fastslå forventet lagernivå")  

1. Forsyning **Sa** med 4 (fast) lukker behov **Da** med -3.  
2. CloseDemand: Opprett en reduksjonspåminnelse med verdien -3 (vises ikke).  
3. Forsyning **Sa** lukkes med et overskudd på 1 (det finnes ikke mer behov).  

     Dermed økes det beregnede beholdningsnivået til + 4, mens den forventede **disponible** beholdningen blir -1.  

4. Den neste forsyningen **Sb** 2 (en annen ordre) er allerede plassert på tidslinjen.  
5. Systemet kontrollerer om det kommer en reduksjonspåminnelse før **Sb** (det gjør det ikke, så ingen handling utføres).  
6. Systemet lukker forsyning **Sb** (det finnes ikke mer behov), ved å A: redusere den til 0 (annullere) eller B: la den være som den er.  

     Dette øker det beregnede beholdningsnivået (A: +0 => +4 eller B: +2 = +6).  

7. Systemet foretar en sluttkontroll: Finnes det noen reduksjonspåminnelse? Ja, det er en på datoen for **Da**.  
8. Systemet legger til reduksjonspåminnelsen på -3 i det beregnede beholdningsnivået, enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. I A-tilfeller oppretter systemet en fremoverplanlagt ordre på datoen **Da**.  

     I B-tilfeller nås gjenbestillingspunktet, og det opprettes en ny ordre.

## <a name="the-role-of-the-time-bucket"></a>Rollen til tidsperioden
Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre.  

Du kan angi en tidsperiode for gjenbestillingsprinsipper som bruker et gjenbestillingspunkt. Dette sikrer at behov i samme tidsperiode akkumuleres før virkningen på den beregnede beholdningen kontrolleres, og før det kontrolleres om gjenbestillingspunktet er overskredet. Hvis gjenbestillingspunktet er overskredet, blir det planlagt en ny forsyningsordre fremover fra slutten av perioden som er angitt av tidsperioden. Tidsperiodene begynner på den planlagte startdatoen.  

Tidsperiodebegrepet gjenspeiler den manuelle fremgangsmåten for å kontrollere lagernivået hyppig i stedet for ved hver transaksjon. Brukeren må angi frekvensen (tidsperioden). Brukeren samler for eksempel inn alle behov fra én leverandør for å registrere en ukentlig ordre.  

![Eksempel på tidsperiode i planlegging](media/nav_app_supply_planning_2_reorder_cycle.png "Eksempel på tidsperiode i planlegging")  

Tidsperioden brukes vanligvis til å unngå en kaskadeeffekt. Det opprettes for eksempel en balansert rad av behov og forsyning der et tidlig behov blir avbrutt, eller det opprettes en ny. Resultatet blir at hver forsyningsordre (unntatt den siste) tidsplanlegges på nytt.

## <a name="staying-under-the-overflow-level"></a>Holde seg under overflytnivået
Når Maks.ant. og Fast gjenbest.ant. brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden. Dette betyr at planleggingssystemet kan foreslå overflødig forsyning når endring av negativt behov eller positiv forsyning skjer utenfor den angitte tidsperioden. Hvis det derfor blir foreslått en overflødig forsyning, vil planleggingssystemet beregne antallet forsyningen skal reduseres til (eller slettes) for å unngå overflødig forsyning. Dette antallet kalles "overflyt nivået." Overflyt formidles som en planleggingslinje med handlingen **Endre ant. (reduksjon)** eller **Avbryt** og følgende advarsel:  

*Viktig: Den beregnede beholdningen [xx] er høyere enn overflytnivået [xx] på forfallsdatoen [xx].*  

![Lageroverflytnivå](media/supplyplanning_2_overflow1_new.png "Lageroverflytnivå")  

###  <a name="calculating-the-overflow-level"></a>Beregne overflytnivået  
Overflytnivået beregnes på ulike måter avhengig av planleggingsoppsettet.  

#### <a name="maximum-qty-reordering-policy"></a>Gjenbestillingsprinsippet Maks.ant  
Overflytnivå = Maks. beholdning  

> [!NOTE]  
>  Hvis det finnes et minimumsordreantall, blir det lagt til som følger: Overflytnivå = Maksimumsbeholdning + Min. bestillingsantall.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Gjenbestillingsprinsippet for Fast gjenbest.ant.  
Overflytnivå = Gjenbestillingsantall + Gjenbestillingspunkt  

> [!NOTE]  
>  Hvis minimumsordreantallet er høyere enn gjenbestillingspunktet, vil dette erstatte slik: Overflytnivå = Gjenbestillingsantall + Min. bestillingsantall  

#### <a name="order-multiple"></a>Bestillingsfaktor  
Hvis det finnes en bestillingsfaktor, vil den justere overflytnivået for gjenbestillingsprinsippene Maks.ant og Fast gjenbest.ant.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>Opprette planleggingslinjen med overflytadvarsel  
Når en eksisterende forsyning fører til at den beregnede beholdningen blir høyere enn overflytnivået på slutten av en tidsperiode, opprettes en planleggingslinje. For å advare om den potensielt overflødige forsyningen vises en advarsel på planleggingslinjen, feltet **Godta handlingsmelding** er ikke valgt og handlingsmeldingen er enten Avbryt eller Endre ant.  

#### <a name="calculating-the-planning-line-quantity"></a>Beregne antall for planleggingslinjen  
Antall for planleggingslinje = Gjeldende forsyningsantall - (Beregnet beholdning – Overflytnivå)  

> [!NOTE]  
>  Som med alle advarselslinjer vil alle maksimum/minimum ordreantall eller bestillingsfaktor bli ignorert.  

#### <a name="defining-the-action-message-type"></a>Angi handlingsmeldingstype  

-   Hvis planleggingslinjeantall er større enn 0, er handlingsmeldingen Endre ant.  
-   Hvis planleggingslinjeantall er lik eller mindre enn 0, er handlingsmeldingen Avbryt  

#### <a name="composing-the-warning-message"></a>Skrive advarselsmeldingen  
Hvis det oppstår overflyt, viser siden **Ikke-sporede planleggingselementer** en advarsel med følgende informasjon:  

-   Det beregnede beholdningsnivået som utløste advarselen  
-   Det beregnede overflytnivået  
-   Forfallsdatoen for forsyningshendelsen.  

Eksempel: "Den beregnede beholdningen 120 er høyere enn overflytnivået 60 28.01.11."  

### <a name="scenario"></a>Scenario  
I dette scenariet endrer en kunde en ordre fra 70 til 40 enheter mellom to planleggingskjøringer. Overflytfunksjonen trer i kraft for å redusere kjøpet som ble foreslått for det første salgsantallet.  

#### <a name="item-setup"></a>Vareoppsett  

|Gjenbestillingsprinsipp|Maks.ant.|  
|-----------------------|------------------|  
|Maks. bestillingsantall|100|  
|Gjenbestillingspunkt|50|  
|Lager|80|  

#### <a name="situation-before-sales-decrease"></a>Situasjonen før salgsreduksjon  

|Messe|Endre ant.|Beregnet lager|  
|-----------|-----------------|-------------------------|  
|Dag én|Ingen|80|  
|Salg|-70|10|  
|Slutten av tidsperioden|Ingen|10|  
|Foreslå ny bestilling|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situasjonen etter salgsreduksjon  

|Endre|Endre ant.|Beregnet lager|  
|------------|-----------------|-------------------------|  
|Dag én|Ingen|80|  
|Salg|-40|40|  
|Kjøp|+90|130|  
|Slutten av tidsperioden|Ingen|130|  
|Foreslå å redusere bestilling<br /><br /> ordre fra 90 til 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Resulterende planleggingslinjer  
 Én planleggingslinje (advarsel) blir opprettet for å redusere kjøpet med 30 fra 90 til 60, for å holde den beregnede beholdningen på 100 i henhold til overflytnivået.  

![Planlegge i henhold til overflytnivå](media/nav_app_supply_planning_2_overflow2.png "Planlegge i henhold til overflytnivå")  

> [!NOTE]  
>  Uten overflytsfunksjonen vises det ingen advarsel hvis det beregnede beholdningsnivået er over maksimumsbeholdningen. Dette kan føre til en overflødig forsyning på 30.

## <a name="handling-projected-negative-inventory"></a>Håndtere forventet negativ lagerbeholdning
Gjenbestillingspunktet uttrykker forventet behov i løpet av leveringstiden for varen. Når gjenbestillingspunktet passeres, er det på tide å bestille mer. Det forventede beholdningsnivået må være stort nok til å dekke behovet til den nye ordren mottas. I mellomtiden håndterer sikkerhetslageret svingninger i behovet opptil et servicenivåmål.  

 Planleggingssystemet anser det derfor som en nødssituasjon hvis et fremtidig behov ikke kan betjenes fra den beregnede beholdningen, eller uttrykt i en annen måte, den beregnede beholdningen blir negativ. Systemet håndterer et slikt unntak ved å foreslå en ny forsyningsordre som dekker en del av behovet som ikke kan dekkes av lageret eller annen forsyning. Ordrestørrelsen på den nye forsyningsordren tar ikke maksimumsbeholdningen eller gjenbestillingsantallet med i betraktningen. Den tar heller ikke ordremodifikatorene Maks. bestillingsantall, Min. bestillingsantall og Bestillingsfaktor med i betraktningen. I stedet gjenspeiles den nøyaktige mangelen.  

 Planleggingslinjen for denne typen forsyningsordre har et kritisk advarselsikon, og tilleggsinformasjon gis ved oppslag for å informere brukeren om situasjonen.  

 I illustrasjonen nedenfor representerer forsyning D en kritisk bestilling for å justere for negativt lager.  

 ![Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning](media/nav_app_supply_planning_2_negative_inventory.png "Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning")  

1.  Forsyning **A**, opprinnelig beregnet beholdning, er under gjenbestillingspunktet.  
2.  Det opprettes en ny foroverplanlagt forsyning (**C**).  

     (Antall = Maks. beholdning – Forventet beholdningsnivå)  
3.  Forsyning **A** lukkes av behov **B**, som ikke er helt dekket.  

     (Behov **B** kan prøve å planlegge forsyning C i, men det vil ikke skje i henhold til tidsperiodekonseptet.)  
4.  Ny forsyning (**D**) blir opprettet for å dekke det gjenværende antallsbehovet **B**.  
5.  Behovet **B** er lukket (opprette en påminnelse til beregnet beholdning).  
6.  Den nye forsyningen **D** lukkes.  
7.  Beregnet beholdning er kontrollert. Gjenbestillingspunktet er ikke overskredet.  
8.  Forsyning **C** lukkes (det finnes ikke mer behov).  
9. Sluttkontroll: Det finnes ingen utestående påminnelser for beholdningsnivå.  

> [!NOTE]  
>  Trinn 4 viser hvordan systemet reagerer i versjoner før Microsoft Dynamics NAV 2009 SP1.  

Med dette avsluttes beskrivelsen av sentrale prinsipper vedrørende lagerplanlegging basert på gjenbestillingsprinsipper. Følgende del beskriver egenskapene til de fire gjenbestillingsprinsippene som støttes.

## <a name="reordering-policies"></a>Gjenbestillingsprinsipper
Gjenbestillingsprinsipper angir hvor mye som skal bestilles når varen må etterfylles. Det finnes fire forskjellige gjenbestillingsprinsipper.  

### <a name="fixed-reorder-qty"></a>Fast gjenbest.ant.
Prinsippet Fast gjenbest.ant. er knyttet til lagerplanlegging av vanlige C-varer (lav lagerkost, lav risiko for foreldelse og/eller mange varer). Dette prinsippet brukes vanligvis i forbindelse med et gjenbestillingspunkt som gjenspeiler forventet behov i løpet av leveringstiden for varen.  

#### <a name="calculated-per-time-bucket"></a>Beregnet per tidsperiode  
Hvis planleggingssystemet oppdager at gjenbestillingspunktet er nådd eller overskredet i en gitt tidsperiode (gjenbestillingssyklusen), over eller på gjenbestillingspunktet i begynnelsen av perioden og under eller på gjenbestillingspunktet på slutten av perioden, vil det foreslå å opprette en ny forsyningsordre med angitt bestillingsantall og planlegge det fremover fra den første datoen etter slutten av tidsperioden.  

Begrepet om periodebasert gjenbestillingspunkt reduserer antall forsyningsforslag. Dette gjenspeiler den manuelle fremgangsmåten der du ofte går gjennom lageret for å sjekke det faktiske innholdet på de ulike hyllene.  

#### <a name="creates-only-necessary-supply"></a>Oppretter bare nødvendig forsyning  
Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om forsyningen allerede er bestilt for mottak i varens leveringstid. Hvis en eksisterende forsyningsordre vil løse problemet ved å bringer det beregnede beholdningen til eller over gjenbestillingspunktet i leveringstiden, vil ikke systemet foreslå en ny forsyningsordre.  

Forsyningsordrer som utelukkende opprettes for å dekke et gjenbestillingspunkt, utelates fra vanlig forsyningsbalansering, og blir ikke på noen måte endret etterpå. Hvis en vare med gjenbestillingspunkt skal avvikles (ikke etterfylles), er det derfor tilrådelig å kontrollere utestående forsyningsordrer manuelt eller endre gjenbestillingsprinsippet for parti for parti. Da vil systemet redusere eller avbryte overflødig forsyning.  

#### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Ordremodifikatorene Min. bestillingsantall, Maks. bestillingsantall og Bestillingsfaktor skal ikke spille en stor rolle når prinsippet Fast gjenbest.ant. brukes. Planleggingssystemet tar fremdeles hensyn til disse modifikatorene, og vil redusere antallet til det angitte maksimumsordreantallet (og opprette to eller flere forsyninger for å nå totalt ordreantall), øke ordren til det angitte minimumsordreantallet, eller runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor.  

#### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om ordren er planlagt for en fridag, i henhold til kalendere som er definert i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdato. Dette kan resultere i en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller enkelte spesifikke behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.  

#### <a name="should-not-be-used-with-forecast"></a>Bør ikke brukes med prognose  
Siden det forventede behovet allerede er uttrykt i bestillingspunktnivået, er det ikke nødvendig å inkludere en prognose i planleggingen av en vare ved hjelp av et gjenbestillingspunkt. Hvis det er relevant å basere planen på en prognose, må du bruke parti for parti-prinsippet.  

#### <a name="must-not-be-used-with-reservations"></a>Må ikke brukes med reservasjoner  
Hvis brukeren har reservert et antall, for eksempel et antall på lager for fremtidig behov, vil planleggingsgrunnlaget forstyrres. Selv om det beregnede beholdningsnivået er akseptabelt i relasjon til gjenbestillingspunktet, er antallene kanskje ikke disponible. Systemet kan prøve å kompensere for dette ved å opprette unntaksordrer. Det anbefales imidlertid at Aldri angis for Reserver-feltet for varer som planlegges ved hjelp av et gjenbestillingspunkt.

### <a name="maximum-qty"></a>Maks.ant.
Maksimumsantall-prinsippet er en måte å opprettholde beholdningen på ved hjelp av et gjenbestillingspunkt.  

Alt for prinsippet Fast gjenbest.ant. gjelder også for dette prinsippet. Den eneste forskjellen er antallet i forsyningen som foreslås. Når du bruker prinsippet om maksimumsantall, defineres gjenbestillingsantallet dynamisk basert på det beregnede beholdningsnivået og varierer derfor vanligvis fra bestilling til bestilling.  

#### <a name="calculated-per-time-bucket"></a>Beregnet per tidsperiode  
Gjenbestillingsantallet fastsettes på tidspunktet (slutten av en tidsperiode) der planleggingssystemet oppdager at gjenbestillingspunktet er overskredet. Systemet måler nå avstanden fra gjeldende beregnede beholdningsnivået opp til angitt maksimal lagerbeholdning. Dette utgjør antallet som må bestilles. Systemet kontrollerer deretter om forsyning allerede er bestilt et annet sted og kommer til å mottas innen leveringstiden, og i så fall reduseres antallet i den nye forsyningsordren med antallet som allerede er bestilt.  

Systemet sikrer at den beregnede beholdningen minst når gjenbestillingspunktet, i tilfelle brukeren har glemt å angi en maksimumsbeholdning.  

#### <a name="combines-with-order-modifiers"></a>Kombineres med ordremodifikatorer  
Avhengig av oppsettet kan det være best å kombinere prinsippet for maksimumsantall med ordremodifikatorer for å sikre et minimumsordreantall, runde det opp til et heltall innkjøpsenheter, eller dele den inn i flere partier som er definert av maksimumsordreantallet.  

### <a name="combines-with-calendars"></a>Kombinerer med kalendere  
Før det blir foreslått en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer systemet om ordren er planlagt for en fridag, i henhold til kalendere som er definert i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdato. Dette kan resultere i en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller enkelte spesifikke behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.

### <a name="order"></a>Bestilling
I et produser-til-ordre-miljø blir en vare utelukkende kjøpt eller produsert for å dekke et spesifikt behov. Vanligvis er dette knyttet til A-varer, og motivasjon for å velge gjenbestillingsprinsippet Ordre kan være at behovet er sjeldent, leveringstiden er ubetydelig eller de nødvendige attributtene varierer.  

Programmet oppretter en ordre-til-ordre-kobling, som fungerer som en innledende forbindelse mellom forsyningen, en forsyningsordre eller beholdning, og behovet det skal dekke.  

I tillegg til bruk av ordrepolicy, kan ordre-til-ordre-koblingen brukes under planleggingen på følgende måter:  

* Når produksjonsprinsippet Produser til ordre brukes til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre).  
* Når funksjonen Ordreplanlegging brukes til å opprette en produksjonsordre fra en ordre.  

Selv om et produksjonsselskap anser seg selv som et miljø som produser til ordrer, kan det være best å bruke gjenbestillingsprinsippet parti for parti hvis varene er helt standard uten variasjon i attributter. Resultatet blir at systemet bruker en endring i beholdningsnivået som ikke er planlagt, og akkumulerer bare ordrer med samme leveringsdato eller innenfor en angitt tidsperiode.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Odre-til-ordre-koblinger og tidligere forfallsdatoer  
I motsetning til de fleste sett med forsyning/behov planlegger systemet fullstendig for koblede ordrer med forfallsdatoer som kommer før den planlagte startdatoen. Forretningsårsaken til dette unntaket er at bestemte sett med behov/forsyning må synkroniseres helt frem til utførelse. Hvis du vil ha mer informasjon om den frosne sonen som gjelder de fleste behovs-/forsyningstyper, kan du se [Designdetaljer: Håndtere ordrer før den planlagte startdatoen](design-details-dealing-with-orders-before-the-planning-starting-date.md).

### <a name="lot-for-lot"></a>Parti for parti
Prinsippet Parti for parti er det mest fleksible fordi systemet bare reagerer på faktisk behov, samt at det fungerer på forventet behov fra prognose og rammeordrer, og avklarer deretter ordreantallet basert på behovet. Prinsippet Parti for parti er rettet mot A- og B-varer der beholdningen kan godtas, men bør unngås.  

Parti for parti-prinsippet er på mange måter lik ordreprinsippet, men det har en generell tilnærming til varer. Det kan godta antall i beholdningen, og det samler behov og tilsvarende forsyning i tidsperioder som er angitt av brukeren.  

Tidsperioden defineres i **Tidsperiode**-feltet. Systemet fungerer med en minste tidsperiode på én dag, siden dette er den minste tidsenheten for behovs- og forsyningshendelser i systemet (men i praksis kan tidsenheten for produksjonsordrer og komponentbehov være sekunder).  

Tidsperioden setter også begrensninger på når en eksisterende forsyningsordre kan planlegges på nytt for å dekke et bestemt behov. Hvis forsyningen er innenfor tidsperioden, det vil bli planlagt på nytt inn eller ut for å dekke behovet. Hvis dette er tidligere, vil det føre til unødvendig oppbygging av beholdning og bør avbrytes. Hvis det er plassert senere, vil det opprettes en ny ordre i stedet.  

Med dette prinsippet er det også mulig å definere et sikkerhetslager for å kompensere for mulige svingninger i forsyning, eller for å dekke plutselig behov.  

Siden forsyningsordreantallet er basert på det faktiske behovet, kan det være fornuftig å bruke ordremodifikatorer: runde ordreantallet opp for å oppfylle en angitt bestillingsfaktor (eller kjøpsenhet for mål), reduser ordren til angitt maksimumsantall, eller reduser antallet til angitt maksimumsantall (og opprett dermed to eller flere forsyninger for å nå det totale nødvendige antallet).

## <a name="see-also"></a>Se også  
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)   
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
