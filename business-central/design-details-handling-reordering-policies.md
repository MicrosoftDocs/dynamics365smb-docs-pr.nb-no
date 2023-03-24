---
title: Designdetaljer – Håndtere gjenbestillingsprinsipper
description: Denne artikkelen gir en oversikt over gjenbestillingsprinsippene du kan bruke i forsyningsplanlegging.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/24/2023
ms.custom: bap-template
---
# Designdetaljer: Håndtere gjenbestillingsprinsipper

Hvis du vil ta med en vare i forsyningsplanleggingen, må du angi et gjenbestillingsprinsipp på siden **Varekort**. Følgende gjenbestillingsprinsipper er tilgjengelige:  

* Fast gjenbest.ant.  
* Maks.ant.  
* Bestilling  
* Parti for parti  

Prinsippene **Fast gjenbest.ant.** og **Maks.ant.** som er relatert til lagerplanlegging. Disse policyene finnes i tillegg til den trinn vise fordelingen av forsynings- og ordresporing.  

## Rollen til gjenbestillingspunktet

Et gjenbestillingspunkt representerer etterspørselen i løpet av leveringstiden. Når beholdningen er beregnet til å gå under lagernivået som defineres av gjenbestillingspunktet, er det på tide å bestille mer. Lageret reduseres gradvis til etterfyllingen ankommer. Den kan nå være null eller sikkerhetslagernivået. Planleggingssystemet foreslår en fremoverplanlagt forsyningsordre når den forventede beholdning blir lavere enn gjenbestillingspunktet.  

Lagernivåer kan flyttes betydelig i tidsperioden. Derfor vil planleggingssystemet overvåke disponibel beholdning kontinuerlig.

## Overvåking av forventet lagernivå og gjenbestillingspunkt

Beholdning er en type forsyning, men for lagerplanlegging skiller planleggingssystemet mellom to lagernivåer:  

* Beregnet beholdning  
* Forventet disponibel beholdning  

### Beregnet beholdning  

Ved starten av planleggingsprosessen er anslått beholdning brutto lagerantall. Bruttoantallet inkluderer bokført og ikke-bokført forsyning og behov i fortiden. Dette antallet blir et anslått beholdningsnivå som bruttoantall fra fremtidige forsyninger og behov opprettholder. Fremtidig forsyning og behov blir innført langs tidslinjen, enten de reserveres eller fordeles på andre måter.  

Planleggingssystemet bruker anslått lager til å overvåke gjenbestillingspunktet, og til å bestemme gjenbestillingsantallet når gjenbestillingsprinsippet **Maks.ant.** brukes.  

### Forventet disponibel beholdning  

Forventet disponibelt beholdningen er beholdningen som er tilgjengelig for å oppfylle behovet på et gitt tidspunkt. Planleggingssystemet bruker forventet disponibel beholdning ved overvåking av sikkerhetslagernivået. Sikkerhetslager må alltid være tilgjengelig for uventet behov.  

### Tidsperioder  

Forventet beholdning er viktig for å oppdaget når gjenbestillingspunktet nås eller overskrides og for å beregne riktig ordreantall gjenbestillingsprinsippet **Maks.ant.** brukes.  

Forventet lagernivå beregnes ved starten av planleggingsperioden. Det er et bruttonivå som ikke tar hensyn til reservasjoner eller andre tildelinger. For å overvåke dette beholdningsnivået i løpet av planleggingssekvensen overvåker planleggingssystemet de aggregerte endringene gjennom en tidsperiode. Den perioden kalles en *tidsperiode*. Hvis du vil finne ut mer om tidsperioder, går du til [Tidsperioder](#time-buckets). Planleggingssystemet sikrer at tidsperioden er minst én dag. Én dag er minste tidsenhet for behovs- eller forsyningshendelser.  

### Fastslå forventet beholdningsnivå  

Følgende sekvens beskriver hvordan planleggingssystemet fastslår det forventede beholdningsnivået:  

* Når en forsyningshendelse er fullstendig planlagt, for eksempel en bestilling, økes den beregnede beholdningen på hendelsens forfallsdato.  
* Når en behovshendelse er fullstendig dekket, reduserer den ikke den beregnede beholdningen med en gang. I stedet bokføres en reduksjonspåminnelse, som er en intern post som inneholder dato og antall for tillegget til den beregnede beholdningen.  
* Når en senere forsyningshendelse planlegges og legges til på tidslinjen, undersøker systemet bokførte reduksjonspåminnelser én etter én til den planlagte datoen for forsyningen. Under denne prosessen kan det hende at gjenbestillingspunktnivået for påminnelsen om intern økning nås eller passeres.  
* Hvis en ny forsyningsordre blir introdusert, kontrollerer det om det er angitt før nåværende forsyning. Hvis det er tilfelle, blir den nye forsyningen gjeldende forsyning og balanseringen starter på nytt.  

Bildet nedenfor viser dette prinsippet.  

![Fastslå forventet beholdningsnivå.](media/nav_app_supply_planning_2_projected_inventory.png "Fastslå forventet beholdningsnivå")  

1. Forsyning **Sa** med 4 (fast) lukker behov **Da** med -3.  
2. CloseDemand: Opprett en reduksjonspåminnelse med verdien -3 (vises ikke).  
3. Forsyning **Sa** lukkes med et overskudd på 1 (det finnes ikke mer behov).  

     Forventet lagernivå øker til + 4, mens den forventede **disponible** beholdningen blir -1.  

4. Den neste forsyningen **Sb** 2 (en annen ordre) er allerede plassert på tidslinjen.  
5. Planleggingssystemet kontrollerer for en reduksjonspåminnelse før **Sb** (i dette eksempelet er det ikke det så ingen handling utføres).  
6. Planleggingssystemet lukker forsyning **Sb** (det finnes ikke mer behov), ved å A: redusere den til 0 (annullere) eller B: la den være som den er.  

     Foreslått lagernivå øker (A: +0 => +4 eller B: +2 = +6).  

7. Planleggingssystemet foretar en endelig sjekk. Er det noen lavere påminnelse? Ja, det er en på datoen for **Da**.  
8. Planleggingssystemet legger til reduksjonspåminnelsen på -3 i det beregnede beholdningsnivået, enten A: +4 -3 = 1 eller B: +6 -3 = +3.  
9. for A oppretter planleggingssystemet en fremoverplanlagt ordre på datoen **Da**. For B nås gjenbestillingspunktet, og det opprettes en ny ordre.

## Rollen til tidsperioden

Formålet med tidsperioden er å samle inn behovshendelser i tidsrammen for å opprette en felles forsyningsordre.  

Du kan angi en tidsperiode for gjenbestillingsprinsipper som bruker et gjenbestillingspunkt. Tids perioder bidrar til å sikre at behov innenfor samme tidsperiode akkumuleres. Deretter kontrollerer systemet om forventet beholdning og om gjenbestillingspunktet er sendt.

Hvis du går over gjenbestillingspunktet, planlegger systemet fremover en ny forsyningsordre fra slutten av tidsperioden. Tidsperioder begynner på den planlagte startdatoen.  

Tidsperiodebegrepet gjenspeiler den manuelle fremgangsmåten for å kontrollere lagernivået hyppig i stedet for ved hver transaksjon. Du definerer frekvensen (tidsperioden). Du kan for eksempel samle inn alle behov fra en leverandør for å registrere en ukentlig ordre.  

![Eksempel på tidsperiode i planlegging.](media/nav_app_supply_planning_2_reorder_cycle.png "Eksempel på tidsperiode i planlegging")  

Tidsperioder brukes ofte til å unngå en kaskadeeffekt. Det opprettes for eksempel en balansert rad av behov og forsyning der et tidlig behov blir avbrutt, eller det opprettes en ny. Resultatet blir at hver forsyningsordre (unntatt den siste) tidsplanlegges på nytt.

## Hold deg under overflytnivået

Når gjenbestillingsprinsippene **Maks.ant.** og **Fast gjenbest.ant.** brukes, fokuserer planleggingssystemet bare på den beregnede beholdningen i den angitte tidsperioden. Det kan foreslå ekstra forsyning når negativt behov eller positive forsyningsendringer skjer utenfor tidsperioden. For ekstra forsyning beregner planleggingssystemet antallet du bør redusere forsyningen for. Dette antallet kalles "overflyt nivået." Overflyten er tilgjengelig som en planleggingslinje med handlingen **Endre ant. (reduksjon)** eller **Avbryt** og følgende advarsel:  

* Viktig: Den beregnede beholdningen [xx] er høyere enn overflytnivået [xx] på forfallsdatoen [xx].*  

![Lageroverflytnivå.](media/supplyplanning_2_overflow1_new.png "Lageroverflytnivå")  

### Beregn overflytnivået  

Overflytnivået beregnes på ulike måter avhengig av gjenbestillingsprinsippet.  

#### Maks.ant.

Overflytnivå = maks. beholdning  

> [!NOTE]  
> Hvis du bruker et minimums ordreantall, legges det til på følgende måte:
>
> overflytnivå = maksimum beholdning + minimum ordreantall.  

#### Fast gjenbest.ant.  

overflytnivå = gjenbestillingsantall + gjenbestillingspunkt  

> [!NOTE]  
> Hvis minimum ordreantall er høyere enn gjenbestillingspunktet, erstattes det på følgende måte:
>
> overflytnivå = gjenbestillingsantall + minimum gjenbestillingsantall  

#### Bestillingsfaktor  

Hvis det finnes en bestillingsfaktor, justerer den overflytnivået for gjenbestillingsprinsippene Maks.ant og Fast gjenbest.ant.  

### Opprett planleggingslinje med en overflytadvarsel  

En planleggingslinje opprettes når en eksisterende forsyning fører til at den beregnede beholdningen blir høyere enn overflytnivået på slutten av en tidsperiode. For å advare om den ekstra forsyningen vises en advarsel på planleggingslinjen, feltet **Godta handlingsmelding** er ikke valgt og handlingsmeldingen er enten **Avbryt** eller **Endre ant.**  

#### Beregn antall for planleggingslinjen  

Antallet på en planleggingslinje beregnes som følger:

antall for planleggingslinje = nåværende forsyningsantall - (beregnet beholdning – overflytnivå)  

> [!NOTE]  
> For sAs med alle advarselslinjer blir alle maksimum og minimum ordreantall og bestillingsfaktor ignorert.  

#### Angi handlingsmeldingstypen  

* Hvis planleggingslinjeantall er større enn 0, er handlingsmeldingen **Endre ant.**  
* Hvis planleggingslinjeantall er lik eller mindre enn 0, er handlingsmeldingen **Avbryt**  

#### Skriv advarselsmeldingen  

Hvis det oppstår overflyt, viser siden **Ikke-sporede planleggingselementer** en advarsel med følgende informasjon:  

* Det beregnede beholdningsnivået som utløste advarselen  
* Det beregnede overflytnivået  
* Forfallsdatoen for forsyningshendelsen  

Eksempel: "Den beregnede beholdningen 120 er høyere enn overflytnivået 60 den 28.01.23"  

### Eksempelscenario  

I dette scenariet endrer en kunde en ordre fra 70 til 40 enheter mellom to planleggingskjøringer. Overflytfunksjonen reduserer kjøpet som ble foreslått for det første salgsantallet.  

#### Vareoppsett  

|Gjenbestillingsprinsipp|Maks.ant.|  
|-----------------------|------------------|  
|Maks. bestillingsantall|100|  
|Gjenbestillingspunkt|50|  
|Lager|80|  

#### Situasjonen før salgsreduksjon  

|Hendelse|Endre ant.|Beregnet lager|  
|-----------|-----------------|-------------------------|  
|Dag én|Ingen|80|  
|Salg|-70|10|  
|Slutten av tidsperioden|Ingen|10|  
|Foreslå ny bestilling|+90|100|  

#### Situasjonen etter salgsreduksjon  

|Endre|Endre ant.|Beregnet lager|  
|------------|-----------------|-------------------------|  
|Dag én|Ingen|80|  
|Salg|-40|40|  
|Kjøp|+90|130|  
|Slutten av tidsperioden|Ingen|130|  
|Foreslå å redusere bestilling<br><br> ordre fra 90 til 60|-30|100|  

#### Resulterende planleggingslinjer  

Systemet oppretter en advarselsplanleggingslinje (advarsel) for å redusere kjøpet med 30, fra 90 til 60, for å holde den beregnede beholdningen på 100 i henhold til overflytnivået.  

![Planlegge i henhold til overflytnivå.](media/nav_app_supply_planning_2_overflow2.png "Planlegge i henhold til overflytnivå")  

> [!NOTE]  
> Uten overflytsfunksjonen vises det ingen advarsel hvis det beregnede beholdningsnivået er over maksimum, som kan føre til en ekstra forsyning på 30.

## Håndter forventet negativ lagerbeholdning

Gjenbestillingspunktet uttrykker forventet behov i løpet av leveringstiden for varen. Det forventede beholdningsnivået må være stort nok til å dekke behovet til den nye ordren mottas. I mellomtiden håndterer sikkerhetslageret svingninger i behovet opptil et servicenivåmål.  

Planleggingssystemet anser det som et nødstilfelle hvis et fremtidig behov ikke kan leveres fra det prosjekterte lageret. Eller uttrykt på en annen måte at den prosjekterte beholdningen blir negativ. Systemet foreslår at du oppretter en ny forsyningsordre for å dekke ikke oppfylt del av behovet. Størrelsen på den nye forsyningsordren tar ikke hensyn til maksimumsbeholdningen eller gjenbestillingsantallet eller følgende ordreendringer:

* Maks. bestillingsantall
* Min. bestillingsantall
* Bestillingsfaktor 

I stedet gjenspeiles den nøyaktige mangelen.  

Planleggingslinjen for denne typen forsyningsordren viser et **kritisk** advarselsikon, og oppgi tilleggsinformasjon om situasjonen.  

I bildet nedenfor representerer forsyning D en kritisk bestilling for å justere for negativt lager.  

![Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning.](media/nav_app_supply_planning_2_negative_inventory.png "Forslag til planlegging av nødsituasjoner for å unngå negativ beholdning")  

1. Forsyning **A**, opprinnelig beregnet beholdning, er under gjenbestillingspunktet.  
2. Det opprettes en ny foroverplanlagt forsyning (**C**).  

     (antall = maks. beholdning – forventet beholdningsnivå)  
3. Forsyning **A** lukkes av behov **B**, som ikke er helt dekket.  

     (Behov **B** kan prøve å planlegge forsyning C i, men tidsperioden forhindrer det.)  
4. Ny forsyning (**D**) blir opprettet for å dekke det gjenværende antallsbehovet **B**.  
5. Behovet **B** er lukket (opprette en påminnelse til beregnet beholdning).  
6. Den nye forsyningen **D** lukkes.  
7. Forventet lager kontrolleres. Gjenbestillingspunktet er ikke overskredet.  
8. Forsyning **C** lukkes (det finnes ikke mer behov).  
9. Siste sjekk. Det finnes ingen utestående påminnelser for beholdningsnivå.  

Følgende del beskriver egenskapene til de fire gjenbestillingsprinsippene som støttes.

## Gjenbestillingsprinsipper

Gjenbestillingsprinsipper angir hvor mye som skal bestilles når varen må etterfylles. Det finnes fire forskjellige gjenbestillingsprinsipper.  

### Fast gjenbestillingsantall

Prinsippet Fast gjenbest.ant. brukes vanligvis til lagerplanlegging for varer med følgende egenskaper:

* Lav lagerkostnad
* Lav risiko for foreldelse
* Lite antall varer

Bruk dette prinsippet vanligvis i forbindelse med et gjenbestillingspunkt som gjenspeiler forventet behov i løpet av varens leveringstid.  

#### Beregnet per tidsperiode  

Hvis du når eller krysser ved gjenbestillingspunktet i en tidsperiode (gjenbestillingssyklus), foreslår systemet to handlinger:

* Opprett en ny forsyningsordre for gjenbestillingsantallet
* Fremoverplanlegg ordren fra den første datoen etter slutten på tidsperioden  

Tidsperiodebasert gjenbestillingspunkt reduserer antall forsyningsforslag. Den gjenspeiler en prosess med å kontrollere manuelt til faktisk innhold i hyller i lageret.  

#### Oppretter bare nødvendig forsyning  

Før det foreslås en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer planleggingssystemet følgende forsyning:

* Om forsyningen allerede er bestilt
* Om du forventer å motta forsyningen innenfor varens leveringstid

Systemet foreslår ikke en ny forsyningsordre hvis en forsyning bringer det beregnede beholdningen til gjenbestillingspunktet i leveringstiden.  

Forsyningsordrer som utelukkende opprettes for å dekke et gjenbestillingspunkt, utelates fra forsyningsbalansering, og blir ikke endret etterpå. Hvis du vil sette opp en vare som har et gjenbestillingspunkt, kan du se gjennom de utestående forsyningsordrene manuelt eller endre gjenbestillingsprinsippet til **Parti for parti**. Systemet vil redusere eller avbryte ekstra forsyning.  

#### Kombineres med ordreendringer  

Ordremodifikatorene Min. bestillingsantall, Maks. bestillingsantall og Bestillingsfaktor skal ikke spille en stor rolle når du bruker prinsippet Fast gjenbest.ant. Planleggingssystemet tar imidlertid dem med i betraktning:

* Reduser antallet til det angitte maks. bestillingsantallet (og opprett to eller flere forsyninger for å nå det totale ordreantallet)
* Øk ordren til det angitte minimumsordreantallet
* Avrunder ordreantallet slik at det oppfyller en bestemt bestilling flere  

#### Kombinerer med kalendere  

Før du foreslår en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer planleggingssystemet om ordren er planlagt for en fridag. Den bruker de kalendere du angir i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdag. Flytting av datoen kan føre til en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller et bestemt behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.  

#### Skal ikke brukes med prognoser  

Siden det forventede behovet allerede er uttrykt i bestillingspunktnivået, er det ikke nødvendig å inkludere en prognose i planleggingen. Hvis det er relevant å basere planen på en prognose, må du bruke **Parti for parti**-prinsippet.  

#### Må ikke brukes med reservasjoner  

Hvis du har reservert et antall, for eksempel et antall på lager for fremtidig behov, forstyrrer du kanskje planleggingsgrunnlaget. Selv om det beregnede beholdningsnivået er akseptabelt i relasjon til gjenbestillingspunktet, er antallene kanskje ikke disponible. Systemet kan forsøke å kompensere ved å opprette unntaksordrer. Vi anbefaler imidlertid at **Reserver**-feltet er satt til **Aldri** på varer som er planlagt med et gjenbestillingspunkt.

### Maksimumsantall

Maksimumsantall-prinsippet er en måte å opprettholde beholdningen på ved hjelp av et gjenbestillingspunkt.  

Alt for prinsippet Fast gjenbest.ant. gjelder også for dette prinsippet. Den eneste forskjellen er antallet i forsyningen som foreslås. Når du bruker prinsippet om maksimumsantall, defineres gjenbestillingsantallet dynamisk basert på det beregnede beholdningsnivået. Derfor er den vanligvis forskjellig fra ordre til ordre.  

#### Beregn per tidsperiode

Når gjenbestillingspunktet er nådd eller du skal krysse gjenbestillingspunktet, bestemmer systemet gjenbestillingsantallet på slutten av en tidsperiode. Det måler avstanden mellom nåværende beregnede beholdningsnivået og angitt maksimal lagerbeholdning for å fastslå antallet i ordren. Systemet kontrollerer deretter:

* Om forsyningen allerede er bestilt
* Om du forventer å motta forsyningen innenfor varens leveringstid

I så fall vil systemet redusere antallet i den nye forsyningsordren med antallene som allerede er bestilt.  

Hvis du ikke angir et maksimum lagerantall, sikrer planleggingssystemet at den forventede beholdningen når gjenbestillingsantallet.

#### Kombiner med ordremodifikatorer

Avhengig av oppsettet kan det være best å kombinere policyen for maksimumsantall med ordremodifikatorer: 

* Slik sikrer du et minimums bestillingsantall
* Avrund antallet til et heltall med innkjøpsenhetens målenhet
* Del antallet i partier som definert av maksimumsordreantallet  

### Kombiner med kalendere

Før du foreslår en ny forsyningsordre for å oppfylle et gjenbestillingspunkt, kontrollerer planleggingssystemet om ordren er planlagt for en fridag. Den bruker de kalendere du angir i feltet **Hovedkalenderkode** på sidene **Selskapsopplysninger** og **Lokasjonskort**.  

Hvis den planlagte datoen er en fridag, flytter planleggingssystemet ordren fremover til nærmeste arbeidsdag. Flytting av datoen kan føre til en ordre som oppfyller et gjenbestillingspunkt, men som ikke oppfyller et bestemt behov. For slike ubalanserte behov oppretter planleggingssystemet en ekstra forsyning.

### Bestilling

I et produser-til-ordre-miljø blir en vare kjøpt eller produsert for å dekke et spesifikt behov. Ordregjenbestillingsprinsippet brukes vanligvis for varer med følgende egenskaper

* Behovet er sjeldent
* Leveringstiden er ikke viktig
* Nødvendige attributter varierer  

[!INCLUDE [prod_short](includes/prod_short.md)] oppretter en ordre-til-ordre-kobling, som fungerer som en innledende forbindelse mellom forsyningen (en forsyningsordre eller beholdning) og behovet. Du kan utligne koblingen ordre-til-ordre under planlegging på følgende måter:  

* Når du bruker produksjonsprinsippet Produser til ordre til å opprette produksjonsordrer med flere nivåer eller av prosjekttypen (produksjon av nødvendige komponenter i samme produksjonsordre)  
* Når du bruker ordreplanlegging til å opprette en produksjonsordre fra en ordre  

> [!TIP]
> Hvis vareattributtene ikke varierer, kan det være best å bruke et Parti for parti-gjenbestillingsprinsipp. Resultatet blir at systemet bruker en endring i beholdningsnivået som ikke er planlagt, og akkumulerer bare ordrer med samme leveringsdato eller innenfor en angitt tidsperiode.  

#### Odre-til-ordre-koblinger og tidligere forfallsdatoer

I motsetning til de fleste sett med forsyning/behov planlegger systemet fullstendig for koblede ordrer med forfallsdatoer som kommer før den planlagte startdatoen. Årsaken til dette unntaket er at bestemte sett med behov/forsyning må synkroniseres. Hvis du vil finne ut mer om den frosne sonen som gjelder de fleste behovs-/forsyningstyper, går du til [Håndtere ordrer før den planlagte startdatoen](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### Parti for parti

Parti for parti-prinsippet er den mest fleksible fordi systemet bare reagerer på faktisk behov på nytt. Det virker på forventet behov fra prognose og rammeordrer, og utligner ordreantallet på bakgrunn av behovet. Prinsippet er ment for varer der beholdningen kan godtas, men bør unngås.  

På noen måter ligner Parti-for-parti-prinsippet på ordrepolicyen, men den har en generisk tilnærming til varer. Den kan godta antall i beholdningen, og det pakker behov og forsyning i tidsperiodene du definerer.  

Du angir tidsperioden i feltet **Tidsperiode** på siden **Varekort**. Den minste tidsperiodens varighet er én dag fordi det er den minste tidsenhetsbetegnelsen på forespørsels- og forsyningshendelser i [!INCLUDE [prod_short](includes/prod_short.md)].  

Tidsperioden begrenses også når du skal planlegge en forsyningsordre på nytt for å oppfylle et gitt behov. Forsyningen innenfor tidsperioden planlegges på nytt inn eller ut for å dekke behovet. Tidligere forsyning vil føre til ekstra lager, og du bør avbryte den. Opprett en ny forsyningsordre for å få en senere forsyning.  

Med denne policyen kan du angi et sikkerhetslager for å kompensere for endringer i forsyningen eller for å dekke et plutselig behov.  

Ettersom forsyningsordreantallet er basert på det faktiske behovet, kan det være fornuftig å bruke ordremodifiseringer:

* Avrund ordreantallet for å oppfylle en ordre med flere (eller kjøpsenhet)
* Øk ordren til et angitte minimumsordreantall
* Reduser antallet til det angitte maks. bestillingsantallet (og opprett dermed to eller flere forsyninger for å nå det totale nødvendige ordreantallet)

## Se også  

[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)  
[Designdetaljer: Tabell for planleggingstilordning](design-details-planning-assignment-table.md)  
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]