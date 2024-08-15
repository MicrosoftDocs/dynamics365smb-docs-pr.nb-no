---
title: 'Designdetaljer – reservasjon, ordresporing og handlingsmeldinger | Microsoft-dokumenter'
description: Reservasjonssystemet er omfattende og inneholder de beslektede og parallelle funksjonene i sporing og handlingsmeldingssystemet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 07/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-reservation-order-tracking-and-action-messaging"></a>Designdetaljer: reservasjon, ordresporing og handlingsmeldinger

Reservasjonssystemet er omfattende og inneholder de beslektede og parallelle funksjonene i sporing og handlingsmeldingssystemet.  

Kjernen i reservasjonssystemet er koblingen av en behovspost og en tilhørende forsyningspost, enten via reservasjon eller ordresporing. En reservasjon er en brukergenerert kobling, og en ordresporingspost er en systemgenerert kobling. Et vareantall som er angitt i reservasjonssystemet, blir reservert eller bestilling sporet, men ikke begge deler samtidig. Hvordan systemene håndterer en vare, avhenger av hvordan varen er satt opp.  

Reservasjonssystemet fungerer sammen med planleggingssystemet ved å opprette handlingsmeldinger på planleggingslinjer under planleggingskjøringer. En handlingsmelding kan betegnes som et tillegg til en ordre ordresporingspost. Handlingsmeldinger er et praktisk verktøy for planlegging av effektiv forsyning uavhengig av om de er opprettet dynamisk i ordresporingen eller under planleggingskjøringen.  

> [!NOTE]  
> Reserverte antall ignoreres av planleggingssystemet, det vil si at den harde koblingen som opprettes mellom forsyning og behov, ikke kan endres gjennom planlegging.  

 Reservasjonssystemet danner også det strukturelle grunnlaget for varesporingssystemet. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->
<!--
> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]
-->

## <a name="reservation"></a>Reservasjon

 En reservasjon er en fast kobling som knytter sammen et bestemt behov og en bestemt forsyning. Denne koblingen påvirker den påfølgende lagertransaksjonen direkte og sikrer riktig utligning av vareposter for kostnadsformål. En reservasjon overstyrer standard lagermetode for en vare. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing](design-details-item-tracking.md).  

 **Reservasjon**-siden er tilgjengelig fra alle ordrelinjer av typene behov og forsyning. På denne siden kan brukere angi hvilken behovs- eller forsyningspost som det skal opprettes en reservasjonskobling til. Reservasjonen består av to poster med samme postnummer. Én post har et minustegn og peker til behovet. Den andre posten har et positivt fortegn og peker mot forsyningen. Disse postene lagres i tabellen *Reservasjonspost* med statusverdien *Reservasjon*. Brukeren kan vise alle reservasjonene på **Reservasjonsposter**-siden.  

### <a name="offsetting-in-reservations"></a>Forskyvning i reservasjoner

 Reservasjoner foretas mot disponibelt vareantall. Disponibelt beregnes i hovedsak slik:  

 `available quantity = inventory + scheduled receipts - gross requirements`

 Tabellen nedenfor viser detaljene for ordrenettverksenhetene som er en del av tilgjengelighetsberegningen.  

||Felt i T27-element|Kildetabell|Tabellfilter|Kildefelt|  
|-|------------------|------------------|------------------|------------------|  
|**Lager**|Lager|Varepost|I/T|Antall|  
|**Tidsplanlagte mottak**|Fast planl. ordremott. (ant.)|Prod.ordrelinje|= Fast planlagt|Restlager (ant.)|  
|**Tidsplanlagte mottak**|Tilh. ordremottak (ant.)|Prod.ordrelinje|= Frigitt|Restlager (ant.)|  
|**Tidsplanlagte mottak**|Ant. på monteringsordre|Monteringshode|= Ordre|Restlager (ant.)|  
|**Tidsplanlagte mottak**|Antall i bestilling|Bestillingslinje|= Ordre|Restantall (lagerenhet)|  
|**Tidsplanlagte mottak**|Overf.ordremottak (ant.)|Overføringslinje|I/T|Restantall|  
|**Bruttobehov**|Antall i ordre|Salgslinje|= Ordre|Restantall (lagerenhet)|  
|**Bruttobehov**|Planlagt behov (ant.)|Prod.ordrekomponent|<>Simulert|Restlager (ant.)|  
|**Bruttobehov**|Ant. på monteringskomponent|Monteringslinje|= Ordre|Restlager (ant.)|  
|**Bruttobehov**|Overf.ordreseddel (ant.)|Overføringslinje|I/T|Restantall|  

 Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Tilgjengelighet i lageret](design-details-availability-in-the-warehouse.md).  

### <a name="manual-reservation"></a>Manuell reservasjon

Når en bruker oppretter en reservasjon med hensikt, får brukeren fullt eierskap over og ansvar for disse varene. Dette betyr at brukeren også må endre eller kansellere reservasjonen manuelt. Slike manuelle endringer kan føre til automatisk endring av de involverte reservasjonene.  

Tabellen nedenfor viser når og hvilke endringer som kan oppstå:  

|Brukerhandling|Systemreaksjon|  
|-----------------|---------------------|  
|Redusere antallet som er reservert|De tilknyttede antallsfeltene oppdateres.|  
|Endre datofelt|De tilknyttede datofeltene oppdateres.<br /><br /> **Obs!** Hvis forfallsdatoen på en forespørsel endres til komme før leveringsdato eller forfallsdato for forsyningen, avbrytes reservasjonen.|  
|Slette ordren|Reservasjonen kanselleres.|  
|Endre lokasjon, hylle, variant, serienummer eller partinummer|Reservasjonen kanselleres.|  

> [!NOTE]  
> Funksjonen for sen binding kan også brukes til å endre reservasjoner uten å informere brukeren, ved å stokke om på ikke-spesifikke reservasjoner av serie- eller partinumre. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md).  

### <a name="automatic-reservations"></a>Automatiske reservasjoner

 Varekortet kan defineres slik at det alltid reserveres automatisk fra behov, for eksempel ordrer. I slike tilfeller utførers en reservasjon mot beholdning, bestillinger, monteringsordrer og produksjonsordrer. Det utstedes en advarsel hvis forsyningen ikke er tilstrekkelig.  

 I tillegg reserveres varer automatisk av forskjellige planleggingsfunksjoner for å holde et behov knyttet til en bestemt forsyning. Ordresporingspostene for slike planleggingskoblinger inneholder **Reservasjon** i **feltet Reservasjonsstatus** i tabellen *Reservasjonspost* . Det opprettes automatiske reserveringer i følgende situasjoner:  

- En produksjonsordrer på flere nivåer der **Produksjonsprinsipp**-feltet for involverte overordnede og underordnede elementene er satt til **Produser til ordre**. Planleggingssystemet oppretter reservasjoner mellom den overordnet produksjonsordren og de underliggende produksjonsordrene for å sikre at de behandles sammen. En slik reservasjonsbinding overstyrer varens standard lagermetode og utligningsmetode.  

- En produksjon, montering eller bestilling der feltet **Gjenbestillingsprinsipp** for den aktuelle varen er satt til **Bestilling**. Planleggingssystemet oppretter reservasjoner mellom behovet og den planlagte forsyningen for å sikre at den bestemte forsyningen opprettes. Hvis du vil ha mer informasjon, kan du se [Ordre](design-details-handling-reordering-policies.md#order).  

- En produksjonsordre blir opprettet fra en ordre med **Ordreplanlegging**-funksjonen knyttet til ordren med en automatisk reservasjon.  

- En monteringsordre som opprettes automatisk for en ordrelinje for å oppfylle antallet i **feltet Antall som skal monteres på ordre** . Denne automatiske reservasjonen knytter sammen salgsbehovet og monteringsforsyningen, slik at ordrebehandlere kan tilpasse og bekrefte monteringsvaren til kunden direkte. I tillegg kobler reservasjonen monteringsavgangen til ordrelinjen gjennom til leveringsaktiviteten som oppfyller kundeordren.  

Hvis forsyning eller behov ikke er tildelt, tilordner planleggingssystemet automatisk en reservasjonsstatus av typen **Overskudd**. Dette kan være et resultat av behov som skyldes prognoseantall eller brukerdefinerte planleggingsparametere. Dette er legitimt overskudd, som systemet gjenkjenner, og det gir ikke opphav til handlingsmeldinger. Overskudd kan også være ekte, overflødig forsyning eller behov som fortsatt ikke spores. Dette er en indikasjon på en ubalanse i ordrenettverket, som gjør at systemet utsteder handlingsmeldinger. Vær oppmerksom på at en handlingsmelding som foreslår en endring i antallet alltid refererer til typen **Overskudd**. Hvis du vil ha mer informasjon, kan du [se delen Eksempel: Sporing av ordrer i delen Salg, Produksjon og Overføringer](#example-order-tracking-in-sales-production-and-transfers) i denne artikkelen.  

Automatiske reservasjoner som opprettes under planleggingskjøringen håndteres på følgende måter:  

- De brukes mot vareantall som er en del av tilgjengelighetsberegningen, og det samme gjelder manuelle reservasjoner. Hvis du vil ha mer informasjon, kan du se delen "Motregning i reservasjoner" i denne artikkelen.  

- De inkluderes og kan endres i etterfølgende planleggingskjøringer, i motsetning til manuelt reserverte varer.  

## <a name="order-tracking"></a>Sporing

Sporing lar planleggeren opprettholde en gyldig leveringsplan ved å gi en oversikt over motregning mellom behov og forsyning i ordrenettverket. Sporingspostene fungerer som grunnlaget for opprettelse av dynamiske handlingsmeldinger og planleggingslinjeforslag under planleggingskjøringer.  

> [!NOTE]  
> Sporingssystemet utligner tilgjengelig beholdning etter hvert som ordrer registreres i ordrenettverket. Dette betyr at systemet ikke prioriterer ordrer som kanskje haster mer med hensyn til forfallsdatoen. Det er derfor opp til logikken i planleggingssystemet eller kunnskapen til planleggeren å omorganisere disse prioritetene på en meningsfylt måte.  

> [!NOTE]  
> Ordresporingspolicyen og funksjonen Hent handlingsmeldinger er ikke integrert med prosjekter. Dette betyr at behov som er knyttet til et prosjekt, ikke spores automatisk. Siden det ikke spores, kan det føre til at bruken av en eksisterende etterfylling med prosjektinformasjon spores til et annet behov, for eksempel en ordre. Derfor kan det oppstå situasjoner der informasjon om disponibel beholdning ikke er synkronisert.  

### <a name="the-order-network"></a>Ordrenettverket

Sporingssystemet er basert på prinsippet om at ordrenettverket alltid må være i balanse, der alle behov som går inn i systemet, blir utlignet med en tilsvarende forsyning, og omvendt. Systemet sørger for dette ved å identifisere logiske koblinger mellom alle behovs- og forsyningsposter i ordrenettverket.  

Dette prinsippet betyr at en endring i behov fører til en tilsvarende ubalanse på forsyningssiden i ordrenettverket. I motsetning vil en endring i forsyning fører til en tilsvarende ubalanse på behovssiden i ordrenettverket. I virkeligheten er ordrenettverket i en tilstand av konstant endring når brukere skrive inn, endrer og sletter ordrer. Sporing behandler ordrer dynamisk ved å reagere på en endringer når den registreres i systemet og blir en del av ordrenettverket. Så snart nye ordresporingsposter er opprettet, er ordrenettverket i balanse, men bare til neste endring skjer.  

For å øke gjennomsiktigheten til beregninger i planleggingssystemet, vises ikke-sporede antall på siden **Ikke-sporede planleggingselementer**. Disse antallene representerer differansen i antall mellom kjent behov og foreslått forsyning. Hver linje på siden refererer til årsaken for det overflødige antallet , for eksempel **Rammebestilling**, **Sikkerhetslagernivå**, **Fast gjenbest.ant**, **Minimum bestillingsantall**, **Avrunding** eller **Avdemping**.  

### <a name="offsetting-in-order-tracking"></a>Forskyvning i sporing

I motsetning til reservasjoner som bare kan utføres mot tilgjengelig antall, er sporing mulig mot alle ordrenettverksenheter som er en del av beregningen av planleggingssystemet beregning av nettobehov. Nettobehovet beregnes som følger:  

`net requirements = gross requirements + reorder point - scheduled receipts - planned receipts - projected available balance`  

> [!NOTE]  
> Behov som er knyttet til prognoser eller planleggingsparametere blir ikke sporet.  

### <a name="example-order-tracking-in-sales-production-and-transfers"></a>Eksempel: Sporing i salg, produksjon og overføringer

Følgende scenario viser hvilke ordresporingsposter som opprettes i tabellen *Reservasjonspost* som følge av ulike endringer i ordrenettverket.  

Anta bruk av følgende data for to varer som er konfigurert for sporing.  

|Element|Parameter|Detalj|
|-|-|-|
|Vare 1|Name|Komponent|
||Disponibelt|100 enheter i EAST plassering<br /><br />- 30 enheter av PARTIA<br />- 70 enheter av PARTIB|  
|Vare 2|Name|Produsert vare|
||Produksjonsstykkliste|1 antall per komponent|  
||Behov|Salg for 100 enheter på WEST lokasjon|  
||Forsyning|Frigitt produksjonsordre (generert med *funksjonen Ordreplanlegging* for salg av 100 enheter)|  

På **siden Produksjonsoppsett** er feltet **Komponenter ved lokasjon** satt til *ØST*.

Følgende ordresporingsposter finnes i tabellen *Reservasjonspost*, basert på dataene i tabellen.  

<!--![First example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  -->
**Reservasjon oppføringer**

|Oppføringsnr.|Positiv|Varenr.|Lokasjonskode|Antall|Reservasjonsstatus|Description|Partinr.|Kildetype|Kilde-ID|Bundet til|  
|--------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ØST|-70|Sporing|Komponent|-|5407|101004|-|
|8|Ja|KOMPONENT|ØST|70|Sporing|Komponent|LOTB|32|-|-| 
|9|-|KOMPONENT|ØST|-30|Sporing|Komponent|-|5407|1001004|-| 
|9|Ja|KOMPONENT|ØST|30|Sporing|Komponent|LOTA|32|-|-| 
|10|-|PRODUSERT VARE|VEST|-100|Reservasjon|Produsert vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUSERT VARE|VEST|100|Reservasjon|Produsert vare|-|5406|101004|Ordre-til-ordre|


#### <a name="entry-numbers-8-and-9"></a>Løpenumre 8 og 9

For komponentbehovet for henholdsvis LOTA og LOTB opprettes sporingskoblinger fra behovet i tabell 5407, *Prod.ordrekomponent*, til forsyningen i tabell 32, *Varepost*.  **Feltet Reservasjonsstatus** inneholder *Sporing* for å angi at disse postene er dynamiske sporingskoblinger mellom tilbud og etterspørsel.  

> [!NOTE]  
> **Partinr.**-feltet er tomt på behovslinjene fordi partinumrene ikke er angitt på komponentlinjene i den frigitte produksjonsordren.  

#### <a name="entry-number-10"></a>Løpenummer 10

Fra salgsbehovet i tabell 37 *Salgslinjer* opprettes det en ordresporings opprette en kobling til forsyningen i tabell 5406,Prod.ordrelinje *·*. Reservasjonsstatus-feltet inneholder Reservasjon **, og** Binding-feltet *inneholder* Ordre-til-ordre **.**  *·* Dette skyldes at den frigitte produksjonsordren ble generert spesifikt for ordren og må forbli koblet i motsetning til sporingskoblinger med reservasjonsstatusen Sporing, som opprettes og endres dynamisk. Hvis du vil ha mer informasjon, kan du [se delen Automatiske reservasjoner](#automatic-reservations) i denne artikkelen.  

 På dette punktet i scenariet overføres de 100 enhetene av LOTA og LOTB til WEST-lokasjonen via en overføringsordre.  

> [!NOTE]  
> Bare overføringsordren bokføres nå, ikke mottak.  

 Nå finnes følgende ordresporingsposter i tabellen *Reservasjonspost* .  

<!-- ![Second example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  -->
**Reservasjon oppføringer**

|Oppføringsnr.|Positiv|Varenr.|Lokasjonskode|Antall|Reservasjonsstatus|Description|Partinr.|Kildetype|Kilde-ID|Bundet til|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|9|-|KOMPONENT|ØST|-30|Overskudd|Komponent|-|5407|1001004|-| 
|10|-|PRODUSERT VARE|VEST|-100|Reservasjon|Produsert vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUSERT VARE|VEST|100|Reservasjon|Produsert vare|-|5406|101004|Ordre-til-ordre|
|12|Ja|KOMPONENT|VEST|70|Overskudd|Komponent|LOTB|5741|1011|-| 
|14|Ja|KOMPONENT|VEST|30|Overskudd|Komponent|LOTA|5741|1011|-| 
|15|Ja|KOMPONENT|UT. LOGG.|70|Overskudd|Komponent|LOTB|32|-|-| 
|16|Ja|KOMPONENT|UT. LOGG.|30|Overskudd|Komponent|LOTA|32|-|-| 

#### <a name="entry-numbers-8-and-9-1"></a>Løpenumre 8 og 9

Ordresporingspostene for de to partiene for komponenten som gjenspeiler behovet i tabell 5407, er endret fra reservasjonsstatusen *Sporing til* Overskudd *·*. Årsaken er at forsyningene som de var knyttet til før i tabell 32, er brukt av leveringen av overføringsordren.  

Ekte overskudd, som i dette tilfellet gjenspeiler overflødige forsyning eller behov som forblir ikke-sporet. Det er en indikasjon på ubalanse i ordrenettverket, som vil generere en handlingsmelding fra planleggingssystemet med mindre det løses dynamisk.  

#### <a name="entry-numbers-12-to-16"></a>Løpenumre 12 til 16

Fordi de to partiene av komponenten er bokført på overføringsordren som levert, men ikke mottatt, er alle relaterte positive ordresporingsposter av reservasjonstypen *Overskudd*, noe som indikerer at de ikke er allokert til noen behov. For hvert partinummer er én post relatert til tabell 5741, *overføringslinje*, og én post er relatert til vareposten på transittlokasjonen der varene nå finnes.  

På dette punktet i scenariet bokføres overføringsordren for komponentene fra *ØST* til VEST *som* mottatt.  

Nå finnes følgende ordresporingsposter i tabellen *Reservasjonspost* .  

<!-- ![Third example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3") -->
 **Reservasjon oppføringer**

|Oppføringsnr.|Positiv|Varenr.|Lokasjonskode|Antall|Reservasjonsstatus|Description|Partinr.|Kildetype|Kilde-ID|Bundet til|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|8|-|KOMPONENT|ØST|-70|Overskudd|Komponent|-|5407|101004|-| 
|9|-|KOMPONENT|ØST|-30|Overskudd|Komponent|-|5407|1001004|-|
|10|-|PRODUSERT VARE|VEST|-100|Reservasjon|Produsert vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUSERT VARE|VEST|100|Reservasjon|Produsert vare|-|5406|101004|Ordre-til-ordre|
|17|Ja|KOMPONENT|VEST|70|Overskudd|Komponent|LOTB|32|-|-| 
|18|Ja|KOMPONENT|VEST|30|Overskudd|Komponent|LOTA|32|-|-| 

Ordresporingspostene ligner nå på det første punktet i scenariet, før overføringsordren ble bokført som levert, bortsett fra at poster for komponenten nå har reservasjonsstatusen *Overskudd*. Dette er fordi komponentbehovet fremdeles er på ØST-lokasjonen *, noe som gjenspeiler at* feltet Lokasjonskode **på komponentlinjen for produksjonsordren inneholder** ØST *som oppsett i* feltet Komponenter ved lokasjon **.**  Forsyningen som ble tildelt dette behovet tidligere, er overført til *WEST-lokasjon* og kan nå ikke spores fullstendig med mindre komponentbehovet på produksjonsordrelinjen endres til *WEST-lokasjon* .  

På dette punktet i scenariet **er lokasjonskoden** på komponentlinjen for produksjonsordren satt til *Vest*. På **siden Varesporingslinjer** tilordnes i tillegg de 30 enhetene i LOTA og de 70 enhetene av LOTB til produksjonsordrekomponentlinjen.  

Nå finnes følgende ordresporingsposter i tabellen *Reservasjonspost* .  

<!-- ![Fourth example of order tracking entries in Reservation Entry table.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")   -->
 **Reservasjon oppføringer**

|Oppføringsnr.|Positiv|Varenr.|Lokasjonskode|Antall|Reservasjonsstatus|Description|Partinr.|Kildetype|Kilde-ID|Bundet til|  
|---------|--------|--------|-------------|--------|------------------|-----------|-------|-----------|---------|-------| 
|10|-|PRODUSERT VARE|VEST|-100|Reservasjon|Produsert vare|-|37|1001|Ordre-til-ordre|
|10|Ja|PRODUSERT VARE|VEST|100|Reservasjon|Produsert vare|-|5406|101004|Ordre-til-ordre|
|21|-|KOMPONENT|VEST|-70|Sporing|Komponent|LOTB|5407|101004|-| 
|21|Ja|KOMPONENT|VEST|70|Sporing|Komponent|LOTB|32|-|-| 
|22|-|KOMPONENT|VEST|-30|Sporing|Komponent|LOTA|5407|1001004|-| 
|22|Ja|KOMPONENT|VEST|30|Sporing|Komponent|LOTA|32|-|-| 

#### <a name="entry-numbers-21-and-22"></a>Løpenumre 21 og 22

Siden komponentbehovet er endret til *VEST-lokasjon*, og forsyningen er tilgjengelig som vareposter på *VEST-lokasjonen*, blir alle ordresporingsposter for de to partinumrene nå fullstendig sporet, angitt av reservasjonsstatusen *Sporing*.  

**Partinr.**-feltet er nå fylt ut i sporingsposten for tabell 5407 fordi partinumrene ble tilordnet til produksjonsordrekomponentlinjene.  

## <a name="action-messaging"></a>Handlingsmeldinger

Når sporingssystemet oppdager en ubalanse i ordrenettverket, oppretter det automatisk en handlingsmelding for å varsle brukeren. Handlingsmeldinger er systemgenererte kall for brukerhandling som angir detaljer om ubalansen og forslag om hvordan du gjenoppretter balansen for ordrenettverket. De vises som planleggingslinjer på **siden Planleggingsforslag når du velger** handlingen Hent **handlingsmeldinger** . Handlingsmeldinger vises dessuten på planleggingslinjer som er generert av planleggingskjøringen, for å gjenspeile planleggingssystemets forslag om hvordan balansen kan gjenopprettes i ordrenettverket. I begge tilfeller kjøres forslagene på ordrenettverket når du velger **handlingen Utfør handlingsmelding** .  

En handlingsmelding behandler ett stykklistenivå om gangen. Hvis brukeren godtar handlingsmeldingen, kan dette føre til flere handlingsmeldinger på neste stykklistenivå.  

Tabellen nedenfor viser handlingsmeldingene som finnes.  

|Handlingsmelding|Description|  
|--------------------|---------------------------------------|  
|**Endre ant.**|Endrer antallet i en eksisterende forsyningsordre for å dekke endret eller nytt behov.|  
|**Tidsplanlegg på nytt**|Tidsplanlegger forfallsdatoen i en eksisterende ordre på nytt.|  
|**Resched. & Chg. Qty.**|Tidsplanlegger forfallsdatoen på nytt og endrer antallet i en eksisterende ordre.|  
|**Ny**|Oppretter en ny ordre hvis behovet ikke kan oppfylles av noen av de tidligere handlingsmeldingene.|  
|**Avbryt**|Kansellerer en eksisterende ordre.|  

Sporingssystemet prøver alltid å løse en ubalanse i det eksisterende ordrenettverket. Hvis dette ikke er mulig, utsteder det en handlingsmelding for å opprette en ny ordre. Følgende er en prioritert liste som ordresporingenssystemet bruker når det avgjør hvordan balansen skal gjenopprettes. Hvis et ekstra behov er ankommet ordrenettverket, forsøker systemet å spore en ordren via følgende kontroller:  

1. Se etter eventuell overflødig forsyning i eksisterende ordresporingspost for dette behovet.  
2. Se etter planlagte og tidsplanlagte mottak sortert etter mottaksdato. Den senest mulige datoen velges.  
3. Se etter tilgjengelige beholdning.  
4. Kontroller om det finnes en forsyningsordre i gjeldende sporingspost. I så fall utsteder systemet en handlingsmelding av typen *Endre* for å øke ordren.  
5. Pass på at det ikke finnes en forsyningsordre i gjeldende sporingspost. I så fall utsteder systemet en handlingsmelding av typen *Ny* for å opprette en ny ordre.  

Et åpent behov passerer gjennom listen og forskyver tilgjengelig forsyning på hvert punkt. Eventuelle gjenværende behov dekkes alltid med sjekk 4 eller 5.  

Hvis det oppstår en reduksjon i behovsmengden, prøve sporingssystemet å løse ubalansen ved å utføre de forrige kontrollene i omvendt rekkefølge. Dette betyr at eksisterende handlingsmeldinger om nødvendig kan endres eller til og med slettes. Sporingssystemet viser alltid det endelige resultatet av beregningene for brukeren.  

## <a name="order-tracking-and-planning"></a>Sporing og planlegging

Når planleggingssystemet kjører, sletter det alle eksisterende sporingsposter og handlingsmeldingsposter og gjenoppretter dem som planleggingslinjeforslag i samsvar med par med forsyning/behov og prioriteter. Når planleggingskjøringen er ferdig, er ordrenettverket i balanse.  

### <a name="planning-system-versus-order-tracking-and-action-messaging"></a>Planleggingssystem kontra sporing og handlingsmeldinger

 Følgende sammenligning viser forskjellene mellom metodene som brukes av planleggingssystemet til å opprette forslag til planleggingslinjer, og metodene som brukes av sporingssystemet til å opprette sporingsposter og handlingsmeldinger.  

- Planleggingssystemet håndterer hele forsynings- og behovsmønsteret for en bestemt vare, mens sporing håndterer ordren som aktiverte det.  

- Planleggingssystemet håndterer alle nivåer i stykklistehierarkiet, mens sporing håndterer ett stykklistenivå om gangen.  

- Planleggingssystemet oppretter koblinger mellom behov og forsyning i henhold til den prioriterte forfallsdatoen. Sporing oppretter koblinger mellom behov og forsyning i henhold til rekkefølgen for ordreregistreringen.  

- Planleggingssystemet tar hensyn til planleggingsparametere, mens ordresporing ikke gjør det.  

- Planleggingssystemet oppretter koblinger i en brukeraktivert satsvis modus når det balanserer behov og forsyning, mens sporing oppretter koblingene automatisk og dynamisk mens brukeren registrerer ordrer.  

## <a name="see-also"></a>Se også

[Utformingsdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
