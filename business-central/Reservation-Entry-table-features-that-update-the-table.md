---
title: Tabellen Reservasjonsinngang - Funksjoner som oppdaterer tabellen Reservasjonsinngang | Microsoft-dokumenter
description: Dette gir veiledning for å hjelpe deg med å forstå og feilsøke problemer med datainkonsekvens i tabellen Reservasjonspost.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="reservation-entry-table---introduction"></a>Tabell for reservasjonsinngang - Introduksjon

Denne tekniske hvitboken gir veiledning for å hjelpe deg med å forstå og feilsøke problemer med datainkonsekvens i tabellen *Reservasjonspost* (tabell 337) i Microsoft Dynamics NAV. Den første delen er en innføring i funksjonene som genererer eller endrer data i denne tabellen. Den dekker også flere felt i tabellen *Reservasjonspost* som er verdt å peke på i forbindelse med disse funksjonene. Den andre delen viser hvordan poster i tabellen *Reservasjonspost* genereres, slettes eller endres når overføringsordrer behandles eller planleggingsfunksjoner utføres.

Tabellen *Reservasjonspost* brukes til å håndtere og lagre informasjon om reservasjon, varesporing og ordresporing.

Ved håndtering av varesporing med delvis bokføring, fungerer tabellen sammen med tabellen *Sporingsspesifikasjon* (tabell 336). Data som brukeren angir på **siden Varesporingslinjer**, opprettes i en midlertidig versjon av tabell 336 og legges i tabell 337 og tabellen Sporingsspesifikasjon når siden lukkes.

Generelt sett avhenger dataene som genereres i tabellen *Reservasjonspost*, av hvilke funksjoner du bruker og hvilke parametere du valgte på varen kort. Disse inkluderer:

- Sporingspolicy for bestillinger
- Reservasjon politikk
- Planleggingsfunksjoner utført
- Gjenbestillings- og produksjonspolicy
- Planleggingsparametere for varen eller lagerføringsenheten kort
- Varesporingskode

## <a name="features-that-update-the-reservation-entry-table"></a>Funksjoner som oppdaterer tabellen Reservasjonspost

### <a name="order-tracking-policy"></a>Sporingspolicy for bestillinger

 **Hvis feltet Sporingsprinsipp** for en vare er satt til Ingen, Microsoft Dynamics NAV  vil det aldri opprette reservasjonsposter i *tabellen Reservasjonspost*, med mindre Nettoendringsplan eller Replanlegging, Reservasjon eller Varesporing utføres. Uten ordresporing aktivert kan du i tillegg ha reservasjonsposter når du bruker policyene Produksjon til ordre eller Montering til ordre.

Du kan vurdere å sette **sporingspolicyen** til Ingen hvis du ikke trenger å spore et behov mot en forsyning på farten, eller omvendt. Sporing av forsyning mot et behov håndteres av sporingsfunksjonaliteten eller planleggingsmotoren. Vi anbefaler ikke at du bruker ordresporing sammen med planleggingsfunksjonalitet.

Når du setter **feltet Sporingsprinsipp** til Bare sporing, Microsoft Dynamics NAV  opprettes det alltid poster i tabell 337 hver gang en ordre opprettes for varen, men **Reservasjonsstatus** i tabell 337 er ikke alltid satt til Sporing. Tenk deg følgende scenario:

> [!NOTE]  
> Arbeidsdatoen er satt til 23.01.2014 (MM/DD/ÅÅÅÅ) for alle eksempler. 
  
1. Opprett en vare med **feltet Sporingsprinsipp** satt til Bare sporing.  
1. Opprett en bestilling. Microsoft Dynamics NAV vil opprette en reservasjonspost med **reservasjonsstatusen** Overskudd, siden bestillingen ennå ikke er tildelt et behov.
1. Opprett en ordre. Microsoft Dynamics NAV vil nå opprette en ny reservasjonspost med **Reservasjonsstatus** Sporing.

 **Reservasjonsstatusen** som ble opprettet i trinn 2 vil bli oppdatert til Sporing; dette håndteres automatisk Microsoft Dynamics NAV . Dette konseptet kalles dynamisk sporing.
Ved å sette **feltet Sporingsprinsipp** for varen til Bare sporing, kan en sluttbruker bruke sporingsfunksjonen til å få en oversikt over hvilken forsyning behovet er tilordnet, og omvendt.

> [!NOTE]  
> Sporingsfunksjonalitet erstatter ikke planleggingsfunksjonalitet, som vurderer alle varer, behov og forsyninger sammen for å få til optimale planleggingsforslag for å optimalisere kundeservicenivåer og balansere lagernivåer.

### <a name="reservation-policy"></a>Reservasjon politikk

En reservasjon består av to poster *i tabellen Reservasjonsoppføring* med reservasjonsstatusen **Reservasjon**, som deler samme løpenummer. Én post har Positiv-feltet aktivert og peker på forsyningen. Den andre posten har Positiv-feltet **ikke** aktivert og peker på behovet. Feltene **Kildetype**, **Kilderef.nr.** og **Kilde-ID** markerer reservasjonen opprette en kobling mellom behov og forsyning.

Opplysningene i **feltet Kildetype** er tabellen, reservasjonsløpenummeret **.** feltet er relatert til. Hvis det for eksempel er en behovspost (negativ), kan det være tabellen Ordre *(tabell 37) eller planleggingskomponenten*  *·* (tabell 99000829).

 **Kilde-ID-feltet** inneholder IDen til dokumentet i tabellen som Kildetype refererer til.

Kilden **ref. nr.** -feltet inneholder et referansenummer for linjen, som reservasjonen **Løpenr.** er relatert til. Hvis posten er knyttet til en salgs- eller bestillingslinje, en kladdelinje eller en bestillingsforslagslinje, kopieres opplysningene i dette feltet fra linjenr **.** . Hvis den er knyttet til en post i *tabellen Varepost* (tabell 32), kopieres informasjonen i dette feltet fra løpenr **.** i tabellen *Varepost* .

Når du bruker reservasjonspolicyalternativet Alltid i kombinasjon med ordresporing, er begge vanligvis synkronisert. Når reservasjonen fjernes eller mottaksdatoen for levering flyttes fremover etter behovsforfallsdatoen, fjernes imidlertid ordresporingen. Du kan også støte på en feilmelding, der Microsoft Dynamics NAV du blir spurt om hva du skal gjøre med eksisterende reservasjoner. Dette scenariet er illustrert i følgende eksempel:

1. Opprett et nytt element kalt COMP. Angi følgende felt:
  - **Etterfyllingssystem**: Kjøp
  - **Sporingspolicy** for bestilling: Bare sporing
  - **Reserve**: Alltid
2. Opprett et annet element kalt FG. Angi følgende felt:
  - **Etterfyllingssystem**: Prod.ordre
  - **Sporingspolicy** for bestilling: Bare sporing
  - **Reserve**: Alltid
3. Opprett et annet element kalt FG. Angi følgende felt:
  - **Sak**: COMP
  - **Antall per**: 1
4. Godkjenn produksjonsstykklistenr. stykkliste FG og tilordne mot vare FG.
5. Opprett en bestilling. Angi følgende felt:
  - **Sak**: COMP
  - **Antall**: 10
  - **Stedskode**: BLÅ
  - **Forventet mottaksdato**: 24.01.2014
6. Opprett en ordre. Angi følgende felt:
  - **Forsendelsesdato**: 02/14/2014
  - **Stedskode**: BLÅ
  - **Sak**: COMP
  - **Antall**: 10

> [!NOTE]  
> Automatisk reservasjon er utført mellom bestillingen og ordren. I tillegg er det opprettet ordresporing mellom bestillingen og ordren.

7. Opprett en manuelt frigitt produksjonsordre. Angi følgende felt:
  - **Sak**: 14.02.2014
  - **Antall**: 10
  - **Sted**: BLÅ
  - **Forfallsdato**: 02/01/2014
8. Velg **Forny produksjonsordre i Prosess-gruppen i kategorien Hjem**  **.**
9. Åpne komponentlisten, og slå opp i Varekomp.

> [!NOTE]  
> Ingen reservasjon eller ordresporing opprettes av Microsoft Dynamics NAV. Årsaken er at det allerede finnes en reservasjon mot ordren som ble opprettet i trinn 6.

Anta at varen av forretningsmessige årsaker trenger varen mer presserende på den frigitte produksjonsordren som ble opprettet i trinn 7. I de følgende trinnene kansellerer vi reservasjonen fra ordren som ble opprettet i trinn 6, og legger merke til hvordan ordresporing håndteres.

10. Slå opp i ordren for Vare COMP fra trinn 6 og kansellere reservasjonen.
11. Åpne bestillingen fra trinn 5, og legg merke til at det nå opprettes ordresporing mellom bestillingen og komponenten som trengs fra den frigitte produksjonsordren.
12. Gjenopprett reservasjonen mellom komponenten som trengs fra den frigitte produksjonsordren, og forsyningen fra bestillingen i trinn 5.

> [!NOTE]  
> Reservasjonen opprettes ikke på nytt, noe som må gjøres manuelt.

13.  **Endre feltet Forventet mottaksdato** i bestillingshodet til trinn 5 fra 24.01.2014 til 02.05.2014.

Microsoft Dynamics NAV viser følgende advarsel:

   Det finnes reservasjoner for denne bestillingen. Disse reservasjonene vil bli kansellert hvis en datakonflikt skyldes denne endringen. Vil du fortsette?

14. Velg Ja. Slå opp reservasjons- og ordresporingspostene fra bestillingen.

> [!NOTE]  
> Den eksisterende reservasjonen kanselleres og må opprettes på nytt manuelt. Ordren er imidlertid dynamisk og er opprettet på nytt av Microsoft Dynamics NAV den til å eksistere mellom bestillingen og ordren. Årsaken er at behovet for den frigitte produksjonsordren (01.02.2014) er før forventet mottaksdato for forsyningen.

Dette avslutter demonstrasjonen av samspillet mellom bruk av automatiske reservasjoner og ordresporing. Eksemplene viser også hva som skjer når du endrer forfallsdatoer, og feilmeldingen som utløses når Der er en reservasjonskonflikt.

### <a name="planning-calculated"></a>Beregnet planlegging

Planlegging utført ved hjelp av ordreplanlegging, bestillingsforslaget eller planleggingsforslaget vil generere poster i tabellen *Reservasjonspost* med Reservasjonsstatus-feltet **satt** til Sporing, Reservasjon eller Overskudd. Der skal alltid være et matchende par med samme løpenr. med positiv og negativ verdi i **Antall (basis)** -feltet når statusen er Sporing eller Reservasjon.  **Kildetype-feltet** vil være behovstypen, det vil si tabell 37 for det negative antallet og en planleggingstabell, for eksempel tabell 246, for det positive antallet.  **Kilde-ID-feltet** vil være PLANLEGGING.

Hvis det gjelder ikke-allokert forsyning eller behov, Microsoft Dynamics NAV  settes Reservasjonsstatus-feltet **til** Overskudd. Du kan for eksempel ha reservasjonsstatusen Overskudd når den eksisterende beholdningen er under sikkerhetslagerantallet eller behovet er knyttet til prognosen.

 *Tabellen Ikke-sporet planleggingselement* (tabell 99000855) inneholder informasjon om ikke-sporede antall som vises når brukeren gjør et oppslag fra ordresporingssiden for å se ikke-sporede antall eller velger et advarselsikon i planleggingsforslaget. Tabellen inneholder poster som gjør rede for et ikke-sporet overskuddsantall i ordresporingsnettverket.

Disse postene genereres under planleggingskjøringen og forklarer hvor det ikke-sporede overskuddsantallet på sporingslinjene kommer fra. Dette ikke-sporede overskuddet kan komme fra:

- Produksjonsprognose
- Rammeordrer
- Sikkerhetslagerantall
- Gjenbestillingspunkt
- Maks. beholdning
- Gjenbestillingsantall
- Maks. bestillingsantall
- Min. bestillingsantall
- Bestillingsfaktor
- Avdemping (% av partistr.)

 *I tabellen Reservasjonspost*, som i ordrene Kjøp, Overføring og Produksjon, er Der feltet **Planleggingsfleksibilitet** . Dette alternativfeltet angir om forsyningen som representeres av disse forsyningsordrene, vurderes av planleggingssystemet ved beregning av handlingsmeldinger. Hvis feltet inneholder alternativet Ubegrenset, tar planleggingssystemet med linjen når handlingsmeldinger beregnes. Hvis feltet inneholder alternativet Ingen, er linjen fast og uforanderlig, og planleggingssystemet tar ikke med linjen når handlingsmeldinger beregnes. Funksjonen administreres i tabellen *Reservasjonspost* av feltet med samme navn.

### <a name="reordering-and-manufacturing-policy"></a>Gjenbestillings- og produksjonspolicy

Hvis en planleggingsfunksjon utføres for en vare som er angitt med gjenbestillingspolicyen satt til Bestilling, Microsoft Dynamics NAV  opprettes poster *i tabellen Reservasjonspost* med reservasjonsstatusen Reservasjon i stedet for Sporing.

Feltene **Kildetype** og **Kilde-ID** behandler andre gjenbestillingspolicyer på samme måte. I **Binding-feltet** i *tabellen*  Reservasjonspost Microsoft Dynamics NAV angis imidlertid Ordre-til-bestilling.

 **Feltet Bundet** fylles ut for å kontrollere forsyningsordrer som er knyttet til et bestemt behov, for eksempel produksjonsordrer som er opprettet direkte fra en ordre. Feltet viser Ordre-til-ordre når posten er knyttet spesifikt til et behov eller en forsyning (Automatisk reservasjon). Behovet kan være relatert til salgs- eller komponentbehov.

### <a name="item-tracking-and-prospect-reservation-entry"></a>Varesporing og reservasjonspost for prospekter

Reservasjonsstatusen Prospect kan opprettes i Microsoft Dynamics NAV tabellen *Reservasjonspost* når du ikke bruker noen ordrenettverksenheter, det vil si Ordresporing. På en forbrukskladdelinje tilordner du for eksempel varesporing til komponenten. Hvis varen allerede er sporet av bestillingen, Microsoft Dynamics NAV  kan det imidlertid hende at det opprettes flere reservasjonsposter for prospekt. Dette er demonstrert i EKSEMPEL 2 knyttet til overføringsordrer i den andre delen av dette dokumentet.

Når du viser eller endrer **siden Varesporingslinjer**, presenteres det samlede innholdet *i tabellen Sporingsspesifikasjon* (tabell 336) og *tabellen Reservasjonspost* i en midlertidig versjon av tabell 336. Dette sikrer at historiske og aktive varesporingsdata er tilgjengelige som ett element.

Reservasjoner faller inn i to kategorier: Ikke-spesifikke reservasjoner, der parti- og serienumre ikke er angitt på reservasjonstidspunktet, og Spesifikke reservasjoner, der du reserverer bestemte parti- eller serienumre fra lageret.

På en ikke-spesifikk reservasjon, partinummeret **.** eller **serienr.** -feltet er tomt i feltet Løpenr **.** i tabell 337 som peker på etterspørselen (for eksempel salget). På grunn av strukturen i reservasjonslogikken må Microsoft Dynamics NAV du likevel Velg bestemte vareposter å reservere mot, når du plasserer en ikke-spesifikk reservasjon for en varesporet vare på lager Microsoft Dynamics NAV .

Siden varepostene inneholder varesporingsinformasjonen, reserverer reservasjonen indirekte bestemte parti- eller serienumre, selv om brukeren ikke hadde til hensikt dette. Med sen binding Microsoft Dynamics NAV  reserverer den imidlertid fortsatt mot bestemte poster, men bruker deretter en omstokkingsmekanisme ved Microsoft Dynamics NAV bokføring.

Hvis du vil ha mer informasjon, kan du lese de Microsoft Dynamics NAV tekniske hvitbøkene som er oppført i tilleggsressursene på slutten av dette dokumentet.

### <a name="source-subtype-suppressed-action-msg-action-message-adjustment-and-disallow-cancellation-fields"></a>Feltene Kildeundertype, Undertrykt handlingsmelding, Justering av handlingsmelding og Ikke tillat annullering

Feltene Kildeundertype **,** Undertrykt handlingsmelding **,** Justering **av handlingsmelding og** Ikke tillat annullering **i tabellen** Reservasjonspost *er beskrevet i denne* delen. Scenarier er gitt for å demonstrere bruken av feltene **Undertrykt handlingsmelding**, **Justering** av handlingsmelding og **Ikke tillat annullering** . Feltet **Justering** av handlingsmelding brukes til funksjonen for sporingspolicy Sporing og handlingsmelding.  **Feltet Ikke tillat annullering** brukes for funksjonen Montering på bestilling i Microsoft Dynamics NAV 2013.

#### <a name="source-subtype"></a>Kildeundertype

 **Feltet Kildeundertype** angir hvilken kildeundertype reservasjonsposten er knyttet til. Hvis posten er knyttet til en kjøps- eller salgslinje, kopieres feltet fra **feltet Bilagstype** på linjen. Hvis den er knyttet til en kladdelinje, kopieres feltet fra **feltet Posttype** på kladdelinjen.

#### <a name="suppressed-action-msg"></a>Utelatt handlingsmelding

Den **undertrykte handlingsmeldingen.** -feltet registrerer når en eksisterende forsyning allerede er delvis behandlet, for eksempel når en bestilling allerede er delvis mottatt, eller når en produksjonsordre har forbruk bokført mot seg.

Når planlegging er utført, Microsoft Dynamics NAV  merker du dette feltet og setter **feltet Reservasjonspoststatus** til *Overskudd8. Følgende eksempel fungerer som en illustrasjon:

1. Åpne vare 80001. Angi følgende felt:
  - **Gjenbestillingspolicy**: Parti for parti
  - **Reserve**: Valgfritt
  - **Sporingspolicy** for bestilling: Ingen
2. Opprett en ordre. Angi følgende felt:
  - **Sak**: 80001
  - **Sted**: Tomt/Ingen
  - **Antall**: 10
  - **Forsendelsesdato**: 2/15/2014
3. Åpne bestillingsforslagene **og** kjør kjørselen **Beregn plan** for vare 80001.
  - **Startdato**: 01/23/2014
  - **Sluttdato**: 03/01/2014
4. Det gis et planleggingsforslag for å etterfylle antall på 10 med ny bestilling og **forfallsdato** 15.02.2014.
5. Velg **Utfør** handlingsmelding **i Funksjoner-gruppen i kategorien Handlinger** for å opprette en bestilling med **forventet mottaksdato** 15.02.2014.
6. Åpne bestillingen fra trinn 5 og sett **Antall til Motta** til 2 og bokfør bare Mottak.
7. Åpne ordren fra trinn 2 og endre **forsendelsesdatoen** til 02.10.2014.
8. Åpne bestillingsforslagene **og** kjør **Beregn plan** for vare 80001
  - **Startdato**: 01/23/2014
  - **Sluttdato**: 03/01/2014
9. Det gis et planleggingsforslag for å etterfylle antall på 8 med ny bestilling og **forfallsdato** 02.10.2014.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

Post nr. 28 i tabell 337 har reservasjonsstatus Sporing for å samsvare med den eksisterende beholdningen som er registrert i varepost 318 for 2 enheter, og det utestående behovet i Ordre-tabellen 37. Den etterfølgende post nr. 29 har også reservasjonsstatusen Sporing og knytter det gjenværende antallet på 8 enheter mellom behovet i ordretabell 37 og den foreslåtte forsyningen i tabellen 246 for bestillingsforslagslinjen.

Postnr. 30 er den eksisterende bestillingen som er delvis mottatt med antall 2. Som et resultat **er Reservasjonsstatus-feltet** Overskudd, og Microsoft Dynamics NAV setter **feltet Antall (basis)** til *8*  (gjenværende saldo) og Melding om **undertrykt handling.** -feltet er aktivert.

#### <a name="action-message-adjustment"></a>Justering av handlingsmelding

 **Feltet Justering** av handlingsmelding viser endringen på forsyningssiden i ordresporingen som oppstår når du godtar de tilhørende handlingsmeldingene. En verdi vises bare Her når funksjonene for både ordresporing og handlingsmeldinger er aktive (sporingspolicyen er satt til Sporing &; Handlingsmelding.). Verdien beregnes på bakgrunn av dataene i tabellen *Handlingsmeldingspost* (tabell 99000849). Følgende eksempel fungerer som en illustrasjon:
1. Åpne vare 80002. Angi følgende felt:
 - **Ordresporingspolicy**: Sporing og handlingsmelding
2. Opprett en ordre. Angi følgende felt:
  - **Sak**: 80002
  - **Sted**: BLÅ
  - **Antall**: 100
3. Åpne Ordreplanlegging-siden **·**, og kjør kjørselen **Beregn plan** .
4. Velg ordren fra trinn 2, og kjør kjørselen Lag **bestillinger** .
5. I ordren fra trinn 2 endrer du **Antall-feltet** fra 100 til 105.
Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.
6. Post nr. 34 har feltet **Tiltaksmelding Justering** i tabell 337 aktivert for 5 enheter med reservasjonsstatus Overskudd. Da ordren ble økt til trinn 5, Microsoft Dynamics NAV  opprettet denne reservasjonen fordi mer forsyning er nødvendig.
7.  **Åpne Planleggingsforslag-siden, og** velg **Hent handlingsmeldinger** i **Prosess-gruppen i kategorien Hjem**  **·**. Microsoft Dynamics NAV vil foreslå å øke bestillingsantallet fra 100 til 105.

#### <a name="disallow-cancellation"></a>Ikke tillat annullering

Feltet **Ikke tillat annullering** angir at reservasjonsposten representerer opprette en kobling mellom en ordrelinje og en monteringsordre. Du kan ikke slette denne reservasjonen fordi den er nødvendig for å opprettholde synkroniseringen som skjer når en vare settes sammen på bestilling. Følgende eksempel fungerer som en illustrasjon:

1. Opprett en bestilling. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Montering
  - **Monteringspolicy**: Monter-til-ordre
  - **Sporingspolicy** for bestilling: Bare sporing
2. Opprett en ny vare kalt Assemble COMP. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Kjøp
  - **Sporingspolicy** for bestilling: Bare sporing
3. Åpne vare Monter FG, og **velg Sammenstilling i gruppen Montering/produksjon i** kategorien **Naviger**  **, og velg** deretter Monteringsstykkliste. **·** Angi følgende felt i monteringsstykklisten:
  - **Type**: Vare
  - **Nr.**: Sett sammen COMP
  - **Antall per**: 1 Velg **OK-knappen** .
4. Åpne en varekladd og øk beholdningen for Sett sammen COMP til antall 10 mot lokasjonen BLÅ, og bokfør kladdelinjen.
5. Opprett en ordre. Angi følgende felt:
  - **Vare**: Monter FG
  - **Sted**: BLÅ
  - **Antall**: 1 Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

Entry No. 82 har Reservation Status Surplus som 9 enheter av Assemble Comp på lager og har ingen etterspørsel. Post nr. 84 sporer reservasjonsposter mellom behovet på samlebåndstabellen *901* og forsyningen i varepost 346.

Entry No. 86 har bindende ordre-til-bestilling med reservasjonsstatus reservasjon. I **tillegg er feltet Ikke tillat annullering** aktivert ettersom monteringspolicyen er satt som Sett sammen på bestilling for vare Monterings-FG. Til slutt settes feltet **Planleggingsfleksibilitet** til Ingen, siden Microsoft Dynamics NAV planleggingslogikken ikke kan slette reservasjonen.

#### <a name="quantity-available-to-pick-and-reservations"></a>Antall tilgjengelig for plukking og reservasjoner

Det **reserverte plukk- og leveringsantall.** Feltet i tabell 337 som finnes i versjoner før Microsoft Dynamics NAV 2013, kontrollerer varetilgjengeligheten i et administrert lager. I alle installasjoner av Microsoft Dynamics NAV lagerstyring finnes vareantall både som lagerposter og vareposter. Disse to oppføringstypene inneholder forskjellig informasjon om hvor varene finnes, og om de er tilgjengelige. Lagerposter angir disposisjonen til en vare etter hylle og hylletype, som kalles hylleinnhold. Vareposter angir varens tilgjengelighet ved reservasjon til utgående dokumenter. Det finnes en spesiell funksjonalitet i plukkalgoritmen for å beregne antallet som er tilgjengelig for plukking når hylleinnhold kombineres med reservasjoner. Plukkalgoritmen trekker fra antall som er reservert for andre utgående dokumenter, antall i eksisterende plukkdokumenter og antall som er plukket, men ennå ikke levert eller forbrukt. Resultatet vises i **feltet Disponibelt antall som skal plukkes** på **siden Plukkforslag**, der feltet beregnes dynamisk. Verdien beregnes også når en bruker oppretter lagerplukk direkte fra utgående dokumenter, for eksempel ordrer, produksjonsforbruk eller utgående overføringer.

*Tilgjengelig mengde for plukking = antall i plukkhyller - antall på plukk og flyttinger – (reservert antall i plukkhyller + reservert antall på plukk og flyttinger).*

Eksemplet nedenfor illustrerer hvordan verdien i tilgjengelig antall for plukking beregnes i Microsoft Dynamics NAV:

1. Opprett en ny vare kalt Lagervare. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Kjøp
  - **Reserve Policy**: Alltid
  - **Sporingspolicy** for bestilling: Bare sporing
2. Opprett en bestilling mot leverandør 60000. Angi følgende felt:
  - **Vare**: Lagervare
  - **Sted**: HVIT
  - **Antall**: 100
3. Frigi bestillingen, og opprett lagermottaket.
4. Bokfør lagermottaket, og registrer lagerplasseringen for antall 100.
5. Opprett en ny bestilling mot leverandør 60000. Angi følgende felt:
  - **Vare**: Lagervare
  - **Sted**: HVIT
  - **Antall**: 10
6. Frigi bestillingen, og opprett lagermottaket.
7. Bokfør KUN lagermottaket. Ikke registrer lagerplasseringen.
8. Opprett en ordre. Angi følgende felt:
  - **Vare**: Lagervare
  - **Sted**: HVIT
  - **Antall**: 10 Reservert antall settes automatisk til 10 på grunn av at reservepolicyen er satt til Alltid.
9. Opprett en ordre. Angi følgende felt:
  - **Vare**: Lagervare
  - **Sted**: HVIT
  - **Antall**: 100 Reservert antall settes automatisk til 100 på grunn av at reservepolicyen er satt til Alltid.
10. Frigi den første ordren fra trinn 8 og opprett en lagerlevering.
11. Frigi lagerleveringen, og velg Opprett plukk i **kategorien Handlinger**  **.**
Følgende feilmelding vises: *Ingenting å håndtere.*
  Årsaken er at tilgjengelig antall å plukke er null. Dette beregnes på følgende måte: Beholdningsantall = 110 Tilgjengelig mengde for plukking = 100

> [!NOTE]  
> Antall på plasserings- eller mottakshyllen kan ikke plukkes.
   
   Totalt reservert mot ordrer er 110 Antall tilgjengelig for plukking = 100 – 110 = null.

Når plasseringen registreres i trinn 7, kan du opprette lagerplukket i trinn 11. I versjoner før Microsoft Dynamics NAV 2013 har Reservert **plukk- og leveringsant.** Feltet i tabell 337 er fylt ut mot reservasjonen for antall 10.

Illustrasjonen nedenfor er hentet fra Microsoft Dynamics NAV 2009 R2.

## <a name="illustrations-using-transfer-orders-and-planning"></a>Illustrasjoner ved hjelp av overføringsordrer og planlegging

### <a name="transfer-orders"></a>Overføringsordrer

Når du bruker overføringsordrer og varen er levert, men ikke fullstendig mottatt, får du reservasjonsstatusen Overskudd i *tabellen Reservasjonspost* . Lokasjonskoden vil være overfør til-lokasjonen.

Kilden **ref. nr.** Beregnes av det siste linjeløpenummeret + linjepostnummeret for varen i den bokførte overføringsforsendelsen.

Når ordresporing er aktivert og Der ikke er behov (ordre eller forbruk), Microsoft Dynamics NAV  opprettes det to poster i tabell 337 med reservasjonsstatus Overskudd. Den *ene er mot overføringslinjetabellen* 5741 og den andre mot vareposttabellen 32.

Dette er demonstrert i det første eksemplet.

#### <a name="example-1"></a>Eksempel 1

1. Åpne elementene 80003 og 80004, og sett feltet **Sporingsprinsipp** til *Bare* sporing. La de andre feltene være standard.
2. Åpne en varekladd og øk beholdningen av disse varene til antall 10 hver mot lokasjonen RØD, og bokfør kladdelinjene.
3. Opprett en overføringsordre fra lokasjonen RED til BLUE for disse to varene: Vare 80003 på overføringsordrelinje 10000 og Vare 80004 på andre linje 20000, begge for 10 enheter.
4. Bokføre bare leveringsdelen av overføringsordren uten lagerfunksjoner.
Den bokførte overføringsforsendelsen vises i illustrasjonen nedenfor.
Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.
5. Sammenlign resultatene på den bokførte overføringsseddelen med postene i tabell 337.

Tabellen nedenfor beskriver hva som skjer i visse felt mot reservasjonsposten 40.

|Felt|Description|  
|---------------------------------|---------------------------------------|  
|**Reservasjon Status**|Overskudd som vare 80003 defineres med ordresporing, men det finnes ikke noe behov.|  
|**Lokasjonskode**|Overfør til kode plassering BLUE.|  
|**Kildetype**|Overføringslinjetabell 5741.|  
|**Kilde-ID**|Dokumentnr. av overføringsordren 1011.|
|**Kilde: ref. nr.**|Totalt linjenr. 20000 + Linjenr. 10000 mot vare 80003 = 30000.|

Forklaringen for følgende felt mot reservasjonspost 43 er som følger:

|Felt|Description|  
|---------------------------------|---------------------------------------|  
|**Reservasjon Status**|Overskudd som vare 80003 defineres med ordresporing, men det finnes ikke noe behov.|  
|**Lokasjonskode**|I transitt-lokasjon EGEN LOGG er lokasjonen der varen finnes.|  
|**Kildetype**|Varepost-tabell 32.|  
|**Kilde: ref. nr.**|Det åpne varepostnummeret 322.|

#### <a name="example-2"></a>Eksempel 2

Det neste eksemplet illustrerer hva som skjer når en komponent overføres mellom lokasjoner, men samtidig spores mellom et behovsbehov og tilgjengelig forsyning. Komponentene overføres fra lokasjonen RED til BLUE, som skal forbrukes på en frigitt produksjonsordre. Komponenten bruker Sporing, Ordreplanlegging og Varesporing.

Eksemplet uthever den oppdagede flyten i tabell 337 i forhold til feltene Reservasjonsstatus, Lokasjonskode **,** Kildetype **,** Kilde-ID, **Kilderef**.nr. **og Bindingstype** **.** **·**

1. På **siden Produksjonsoppsett** setter du feltet **Komponenter ved lokasjon** til RØDT.
2. Opprett en ny varekomponent. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Kjøp
  - **Produksjonspolicy**: Produser til lager
  - **Sporingspolicy** for bestilling: Bare sporing
  - **Varesporingskode**: LOTALL
3. Bruk varekladden til å øke lagerbeholdningen for varekomponenten mot lokasjonen RØD til 100 enheter. Angi følgende partinumre:
  - Partinummer Parti A, Antall 30
  - Partinummer Parti B, Antall 70
4. Opprett en ny vare Produsert. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Produksjon
  - **Produksjonspolicy**: Produser til lager
  - **Sporingspolicy** for bestilling: Bare sporing
5. Opprett **produksjonsstykkliste** med 1 antall per varekomponent.
6. Tilordne produksjonsstykklisten mot produsert vare.
7. Opprett en ordre. Angi følgende felt:
  - **Vare**: Produsert
  - **Sted**: BLÅ
  - **Antall**: 100
8. Velg **Planlegging** i **Plan-gruppen** i kategorien Handlinger **i** ordren for å opprette en koblet, frigitt produksjonsordre mot ordren.
9. Åpne den frigitte produksjonsordren/komponentbehovet, og legg merke til at lokasjonen er angitt som RØD.
Årsaken er at Komponenter ved **lokasjon** er RØDE i **produksjonsoppsettet**  kort.
Produsert vare henter utdataene mot lokasjonen BLÅ.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

##### <a name="reservation-entries-with-numbers-55-and-56"></a>Reservasjonsposter med nummer 55 og 56

For komponentbehovet for henholdsvis parti A og parti B opprettes sporingskoblinger fra behovet i tabell 5407 (Prod.ordrekomponent) til forsyningen i tabell 32, Varepost.  **Feltet Reservasjonsstatus** inneholder Sporing for alle fire postene for å angi at disse dynamiske sporingskoblingene mellom tilbud og etterspørsel.

Behovet i tabell 5407, Prod.ordrekomponent, er knyttet til kilde-IDen til den frigitte produksjonsordren 101006. Forsyningen i tabell 32, Varepost, er koblet til Kilderef.nr. Som er varepostnumrene 325 og 326 der enhetene finnes.

> [!NOTE]  
> **Partinr.**-feltet er tomt på behovslinjene fordi partinumrene ikke er angitt på komponentlinjene i den frigitte produksjonsordren.

##### <a name="reservation-entry-with-number-57"></a>Reservasjonsinngang med nummer 57

Fra salgsbehovet i tabell 37, Salgslinje, opprettes det en opprette en kobling for sporing av ordre til forsyningen i tabell 5406, Prod.ordrelinje. Reservasjonsstatus-feltet **inneholder** Reservasjon, og **Binding-feltet** inneholder Ordre-til-ordre. Dette skyldes at den frigitte produksjonsordren ble generert spesifikt for ordren og må forbli koblet i motsetning til sporingskoblinger med reservasjonsstatusen Sporing, som opprettes og endres dynamisk.

> [!NOTE]  
>  **Binding-feltet** kan også inneholde *Ordre-til-ordre* når Produser til ordre brukes som produksjonspolicy og/eller Ordre som gjenbestillingsprinsipp.

10. På dette punktet i scenariet overføres de 100 enhetene av komponenten fra RED-lokasjon til BLÅ-lokasjon ved hjelp av en overføringsordre.

Velg Parti A og Parti B for forsendelsen.

Bokfør det totale utestående antallet som KUN levert.

> [!NOTE]  
> Komponenter kan brukes på lokasjonen RØD, men for å illustrere flyten av reservasjonsposter overføres enhetene manuelt til lokasjonen BLÅ.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

##### <a name="reservation-entries-with-number-55-and-56"></a>Reservasjonsposter med nummer 55 og 56

Ordresporingspostene for de to partiene for komponenten som gjenspeiler behovet i tabell 5407, er endret fra reservasjonsstatusen Sporing til Overskudd. Årsaken er at forsyningene som de var knyttet til før i tabell 32, er brukt av leveringen av overføringsordren. Ekte overskudd, som i dette tilfellet gjenspeiler overflødige forsyning eller behov som forblir ikke-sporet. Det er en indikasjon på ubalanse i ordrenettverket, som vil generere en handlingsmelding fra planleggingssystemet med mindre det løses dynamisk.

##### <a name="reservation-entry-numbers-59-to-63"></a>Reservasjon Entry Numbers 59 til 63

Fordi de to partiene av komponenten er bokført på overføringsordren som levert, men ikke mottatt, er alle relaterte positive ordresporingsposter av reservasjonstypen Overskudd, noe som indikerer at de ikke er allokert til noen behov. For hvert partinummer er én post relatert til tabell 5741, Overføringslinje, og én post er relatert til vareposten på transittlokasjonen der varene nå finnes.

Tabell 5741, **Overføringslinje**, er kildetypen. **Kilde-ID** er overføringsordredokumentnummer 1012 og **kilderef.nr.** Er 20000 = 10000 + 10000 som beskrevet i eksempel 1. Lokasjonen angis som BLÅ for overfør til-lokasjonskoden.

De resterende to postene med **overskudd av reservasjonsstatus** har tabell 32, **Varepost**, som Kildetype og **Kilderef.nr.** 328 og 330, inkludert partinumrene som for øyeblikket befinner seg i transittlokasjonen UT LOGG.

11. Bokfør den utestående overføringsordren som Mottatt.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

Ordresporingspostene ligner nå på det første punktet i scenariet, før overføringsordren ble bokført som levert, bortsett fra at poster for komponenten nå har reservasjonsstatusen Overskudd i stedet for Sporing. Dette er fordi komponentbehovet fremdeles er i RED-lokasjonen, noe som gjenspeiler at **feltet Lokasjonskode** på komponentlinjen for produksjonsordren inneholder RØD som definert i **feltet Komponenter ved lokasjonsoppsett** .

Forsyningen som ble tildelt dette behovet tidligere, var overført til den blå lokasjonen og kan nå ikke spores fullstendig med mindre komponentbehovet på produksjonsordrelinjen endres til BLÅ lokasjon. Dette registreres i de to siste reservasjonspostene med partinumrene fylt ut, **Kildetype-feltet** er Tabell 32 og **Kilderef.nr.** -feltet er varepostene 333 og 334.

12. I komponentlisten som er tilordnet den frigitte produksjonsordren, endrer du lokasjonen til BLÅ for komponenten.

12. Åpne **forbrukskladden**, og kjør kjørselen **Beregn forbruk** .
Tilordne parti A antall 30 og Parti B antall 70.

Lukk Varesporing-skjemaet.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

##### <a name="reservation-entries-with-numbers-68-and-69"></a>Reservasjonsposter med nummer 68 og 69

Siden komponentbehovet er endret til BLÅ-lokasjonen, og forsyningen er tilgjengelig som vareposter på BLÅ-lokasjonen, blir alle ordresporingsposter for de to partinumrene nå fullstendig sporet, angitt av reservasjonsstatusen Sporing. Partinumrene fylles ikke ut på partinummeret **.** i forhold til behovet i tabell 5406, **Prod.ordrelinje**, siden vi ikke angav partinumre for komponenten i den frigitte produksjonsordren.

##### <a name="reservation-entries-with-numbers-70-and-71"></a>Reservasjonsposter med nummer 70 og 71

Poster med reservasjonsstatus Prospekt er generert i tabell 337. Årsaken er at begge partinumrene er tilordnet mot komponenten i forbrukskladden, men kladden er ikke bokført.

Dette fullfører delen hvordan ordresporingsposter i tabellen **Reservasjonspost** genereres, endres og slettes ved bruk av flere funksjoner i kombinasjon med overføringsordrer.

### <a name="planning-calculated-1"></a>Beregnet planlegging

Når du bruker planleggingsfunksjoner, det vil si Bestillingsforslag **,** Planleggingsforslag **eller** Ordreplanlegging **, kan reservasjonsposter i** Reservasjonspost-tabell **337 endres eller legges til, avhengig av planleggingsforslaget gitt av logikken i** . Microsoft Dynamics NAV Eksempel 3 bruker **gjenbestillingsprinsipprekkefølge** med **produksjonspolicy** Produser til-ordre for en produsert vare. Komponenten bruker **gjenbestillingsprinsippet**, Fast gjenbestillingsantall.

#### <a name="example-3"></a>Eksempel 3

1. I **produksjonsoppsettet**  er kort **er Komponent ved lokasjon** RØD fra forrige eksempel.
2. Opprett nytt overordnet Vare 70061. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Prod.ordre
  - **Produksjonspolicy**: Produser til ordre
  - **Gjenbestillingspolicy**: Bestill
  - **Reservepolicy**: Valgfritt
  - **Ordresporing**: Ingen
3. Opprett ny komponentvare 70062. Angi følgende felt:
  - **Lagerenhet: PCS**
  - Eventuelle standard bokføringsgrupper
  - **Etterfyllingssystem**: Kjøp
  - **Gjenbestillingsprinsipp**: Fast gjenbestillingsantall
  - **Reservepolicy**: Valgfritt
  - **Sporingspolicy** for bestilling: Ingen
  - **Sikkerhet Lager Antall**: 10
  - **Bestill på nytt**: 25
  - **Gjenbestillingsantall**: 50
4. Opprett en ny produksjonsstykkliste, og angi komponentvare 70062 med antall per 1.
Tilordne produksjonsstykklisten til overordnet vare 70061.
5. Opprett en ordre. Angi følgende felt:
  - **Vare**: Fast gjenbestillingsantall
  - **Sted**: RØD
  - **Antall**: 40
  - **Forsendelsesdato**: 2/15/2014
6.  **Åpne siden Planleggingsforslag**, og kjør kjørselen **Beregn regenerativ plan** .
  - **MPS/MRP**: aktivert
  - **Startdato**: 01/23/2014
  - **Sluttdato**: 03/01/2014
  - Filtrere på vare 70061 og 70062
  - Ingen prognose

Følgende planleggingsforslag er gitt.

Det første planleggingsforslaget er å opprette en ny planlagt produksjonsordre for å forsyne det utestående behovet i ordren for antall 40 av den overordnet vare 70061. Se gjennom ordresporingen, og Microsoft Dynamics NAV den utestående ordren vises. Ordresporing aktiveres når den genereres av planleggingsmotoren.

Den andre linjen er å bringe beholdningen over gjenbestillingspunktet (25). Når planleggingslogikken tar hensyn til gjenbestillingsantall (50), foreslås derfor et antall på 50 enheter. Den tredje linjen er å bringe lagerbeholdningen til sikkerhetslagernivå (10).

Den fjerde linjen er å etterfylle beholdningen når ordren leveres. På det tidspunktet er beholdningen 20 og så under gjenbestillingspunktet. Planleggingsmotoren foreslår derfor å kjøpe 50 ekstra komponenter med tanke på gjenbestillingsantall. Dette er Ikke-sporet antall, så i tabellen *Reservasjonspost* 337 merkes dette med reservasjonsstatusen Overskudd.

Statusinformasjonen i tabell 337 er vist i illustrasjonen nedenfor.

 **Reservasjonsstatus-feltet** er Reservasjon, og det opprettes en Ordre-til-bestilling-binding. Årsaken er at produksjonspolicyen for vare er Produser til ordre, og gjenbestillingspolicyen er angitt som Ordre. Hvis en av de to er satt til Bestill, vil reservasjonsstatusen være Reservasjon i stedet for Sporing, og Binding er satt til Ordre-til-ordre.

Behovet på 40 enheter mot feltet **Kilde-ID** er ordrenummer 1005 og Kildetype er *Salgslinjetabell* 37. Reservasjonsposten er i tråd med planleggingsforslaget, Kilderef. nr. 10000, Kilde-ID er PLANLEGGING, og Kildetype er *Rekvisisjonslinjetabell* 246. Så Der er en balanse mellom behovet fra ordren og forsyningen som er foreslått av planleggingsmotoren.

##### <a name="reservation-entry-numbers-73-and-74"></a>Reservasjon Entry nummer 73 og 74

Når du kjører kjørselen Beregn plan, genereres de neste fire postene med reservasjonsstatusen Sporing på grunn av innstillingen av gjenbestillingspolicyen Fast gjenbestillingsantall for komponenten. Den nødvendige forsyningen for komponentvare 70062 etterfylles av planleggingsforslagene som er gitt, Kilderef. nr. 20000 og 30000, med Kilde-ID satt til PLANLEGGING og Kildetype fra *Bestillingsforslagslinjetabell* 246. Komponentbehovet opprettes for å dekke behovet mot overordnet vare 70061 for totalt antall (grunntall) 40. Som et resultat av dette behovet er feltet **Kildeprod.ordrelinje** 10000, med Kildetype tabellen *Komponentbehov* 99000829.

Reservasjonsstatusen er ikke Overskudd, ettersom det finnes ordresporing mellom behovet for overordnet vare 70061 og forsyningen av komponentvare 70062.

##### <a name="reservation-entry-numbers-75-and-76"></a>Reservasjon Entry nummer 75 og 76

De to siste postene har reservasjonsstatusen Overskudd, siden dette er ikke-sporede antall som genereres i planleggingsforslaget i forbindelse med gjenbestillingsparameterne Gjenbestillingspunkt og Gjenbestillingsantall.

## <a name="see-also"></a>Se også
[Utformingsdetaljer: Varesporingsutforming](design-details-item-tracking-design.md)  
[Utformingsdetaljer: Balanser tilbud og etterspørsel](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger](design-details-reservation-order-tracking-and-action-messaging.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
