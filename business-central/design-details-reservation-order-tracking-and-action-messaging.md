---
title: 'Designdetaljer - Reservasjon, ordresporing og handlingsmeldinger | Microsoft-dokumentasjon'
description: Reservasjonssystemet er omfattende og inneholder de beslektede og parallelle funksjonene i sporing og handlingsmeldingssystemet.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, replenishment, reordering'
ms.date: 06/08/2021
ms.author: edupont
---
# Designdetaljer: Reservasjon, ordresporing og handlingsmeldinger
Reservasjonssystemet er omfattende og inneholder de beslektede og parallelle funksjonene i sporing og handlingsmeldingssystemet.  

 I kjernen av reservasjonssystemet er koblingen av en behovspost og en tilsvarende forsyningspost, enten ved hjelp av reservasjon eller sporing. En reservasjon er en brukergenerert kobling, og en ordresporingspost er en systemgenerert kobling. Et vareantall som er angitt i reservasjonssystemet, blir reservert eller bestilling sporet, men ikke begge deler samtidig. Hvordan systemer bruker en vare, avhenger av hvordan varen konfigureres.  

 Reservasjonssystemet fungerer sammen med planleggingssystemet ved å opprette handlingsmeldinger på planleggingslinjer under planleggingskjøringer. En handlingsmelding kan betegnes som et tillegg til en ordre ordresporingspost. Handlingsmeldinger er et praktisk verktøy for planlegging av effektiv forsyning uavhengig av om de er opprettet dynamisk i ordresporingen eller under planleggingskjøringen.  

> [!NOTE]  
>  Reserverte antall ignoreres av planleggingssystemet, det vil si at den harde koblingen som opprettes mellom forsyning og behov, ikke kan endres gjennom planlegging.  

 Reservasjonssystemet danner også det strukturelle grunnlaget for varesporingssystemet. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing](design-details-item-tracking.md).  

 <!--For more detailed information about how the reservation system works, see the _Reservation Entry Table_ white paper on [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).  -->

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Reservasjon  
 En reservasjon er en fast kobling som knytter sammen et bestemt behov og en bestemt forsyning. Denne koblingen påvirker den påfølgende lagertransaksjonen direkte og sikrer riktig utligning av vareposter for kostnadsformål. En reservasjon overstyrer standard lagermetode for en vare. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Varesporing](design-details-item-tracking.md).  

 **Reservasjon**-siden er tilgjengelig fra alle ordrelinjer av typene behov og forsyning. På denne siden kan brukere angi hvilken behovs- eller forsyningspost som det skal opprettes en reservasjonskobling til. Reservasjonen består av to poster med samme postnummer. Én post har et minustegn og peker til behovet. Den andre posten har et positivt fortegn og peker mot forsyningen. Disse postene lagres i **Reservasjonspost**-tabellen med statusverdien **Reservasjon**. Brukeren kan vise alle reservasjonene på **Reservasjonsposter**-siden.  

### Forskyvning i reservasjoner  
 Reservasjoner foretas mot disponibelt vareantall. Disponibelt beregnes i hovedsak slik:  

 disponibelt antall = beholdning + tidsplanlagte mottak - bruttobehov  

 Tabellen nedenfor viser detaljene for ordrenettverksenhetene som er en del av tilgjengelighetsberegningen.  

||Felt i T27|Kildetabell|Tabellfilter|Kildefelt|  
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

### Manuell reservasjon  
 Når en bruker oppretter en reservasjon med hensikt, får brukeren fullt eierskap over og ansvar for disse varene. Dette betyr at brukeren også må endre eller kansellere reservasjonen manuelt. Slike manuelle endringer kan føre til automatisk endring av de involverte reservasjonene.  

 Tabellen nedenfor viser hvilke endringer som kan oppstå, og når de kan oppstå:  

|Brukerhandling|Systemreaksjon|  
|-----------------|---------------------|  
|Redusere antallet som er reservert|De tilknyttede antallsfeltene oppdateres.|  
|Endre datofelt|De tilknyttede datofeltene oppdateres.<br /><br /> **Obs!** Hvis forfallsdatoen på en forespørsel endres til komme før leveringsdato eller forfallsdato for forsyningen, avbrytes reservasjonen.|  
|Slette ordren|Reservasjonen kanselleres.|  
|Endre lokasjon, hylle, variant, serienummer eller partinummer|Reservasjonen kanselleres.|  

> [!NOTE]  
>  Funksjonen for sen binding kan også brukes til å endre reservasjoner uten å informere brukeren, ved å stokke om på ikke-spesifikke reservasjoner av serie- eller partinumre. Hvis du vil ha mer informasjon, kan du se Designdetaljer: Varesporing og reservasjoner.  

### Automatiske reservasjoner  
 Varekortet kan defineres slik at det alltid reserveres automatisk fra behov, for eksempel ordrer. I slike tilfeller utførers en reservasjon mot beholdning, bestillinger, monteringsordrer og produksjonsordrer. Det utstedes en advarsel hvis forsyningen ikke er tilstrekkelig.  

 I tillegg reserveres varer automatisk av forskjellige planleggingsfunksjoner for å holde et behov knyttet til en bestemt forsyning. Sporingspostene for slike planleggingskoblinger inneholder **Reservasjon** i **Reservasjonsstatus**-feltet i **Reservasjonspost**-tabellen. Det opprettes automatiske reserveringer i følgende situasjoner:  

-   En produksjonsordrer på flere nivåer der **Produksjonsprinsipp**-feltet for involverte overordnede og underordnede elementene er satt til **Produser til ordre**. Planleggingssystemet oppretter reservasjoner mellom den overordnede produksjonsordren og de underliggende produksjonsordrene for å sikre at de behandles sammen. En slik reservasjonsbinding overstyrer varens standard lagermetode og utligningsmetode.  

-   En produksjon, montering eller bestilling der feltet **Gjenbestillingsprinsipp** for den aktuelle varen er satt til **Bestilling**. Planleggingssystemet oppretter reservasjoner mellom behovet og den planlagte forsyningen for å sikre at den bestemte forsyningen opprettes. Hvis du vil ha mer informasjon, kan du se [Ordre](design-details-handling-reordering-policies.md#order).  

-   En produksjonsordre blir opprettet fra en ordre med **Ordreplanlegging**-funksjonen knyttet til ordren med en automatisk reservasjon.  

-   En monteringsordre opprettes automatisk for en salgsordrelinje for å oppfylle antallet i feltet **($ T_37_900 Qty. to Assemble to Order $)**. Denne automatiske reservasjonen knytter sammen salgsbehovet og monteringsforsyningen, slik at ordrebehandlere kan tilpasse og bekrefte monteringsvaren til kunden direkte. I tillegg kobler reservasjonen monteringsavgangen til ordrelinjen gjennom til leveringsaktiviteten som oppfyller kundeordren.  

 I tilfeller der forsyning eller behov ikke er tildelt, tilordner planleggingssystemet automatisk reserveringsstatusen av typen **Overskudd**. Dette kan være et resultat av behov som skyldes prognoseantall eller brukerdefinerte planleggingsparametere. Dette er legitimt overskudd, som systemet gjenkjenner, og det utløser ingen handlingsmeldinger. Overskudd kan også være ekte, overflødig forsyning eller behov som fortsatt ikke spores. Dette er en indikasjon på en ubalanse i ordrenettverket, som gjør at systemet utsteder handlingsmeldinger. Vær oppmerksom på at en handlingsmelding som foreslår en endring i antallet alltid refererer til typen **Overskudd**. Hvis du vil ha mer informasjon, kan du se avsnittet Eksempel: Sporing i salg, produksjon og overføringer i dette emnet.  

 Automatiske reservasjoner som opprettes under planleggingskjøringen håndteres på følgende måter:  

-   De utlignes mot vareantall som er en del av tilgjengelighetsberegningen, slik som manuelle reservasjoner. Hvis du vil ha mer informasjon, kan du se delen Forskyvning i reservasjoner i dette emnet.  

-   De tas med og eventuelt endres i påfølgende planleggingskjøringer, i motsetning til manuelt reserverte varer.  

## Sporing  
 Sporing lar planleggeren opprettholde en gyldig leveringsplan ved å gi en oversikt over motregning mellom behov og forsyning i ordrenettverket. Sporingspostene fungerer som grunnlaget for opprettelse av dynamiske handlingsmeldinger og planleggingslinjeforslag under planleggingskjøringer.  

> [!NOTE]  
>  Sporingssystemet utligner tilgjengelig beholdning etter hvert som ordrer registreres i ordrenettverket. Dette betyr at systemet ikke prioriterer ordrer som kanskje haster mer med hensyn til forfallsdatoen. Det er derfor opp til logikken i planleggingssystemet eller kunnskapen til planleggeren å omorganisere disse prioritetene på en meningsfylt måte.  

> [!NOTE]  
>  Sporingsprinsipp og funksjonen Hent handlingsmelding ikke er integrert med Prosjekter. Dette betyr at behov som er knyttet til et prosjekt, ikke spores automatisk. Siden det ikke spores, kan det føre til at bruken av en eksisterende etterfylling med prosjektinformasjon spores til et annet behov, for eksempel en ordre. Derfor kan det oppstå situasjoner der informasjon om disponibel beholdning ikke er synkronisert.  

### Ordrenettverket  
 Sporingssystemet er basert på prinsippet om at ordrenettverket alltid må være i balanse, der alle behov som går inn i systemet, blir utlignet med en tilsvarende forsyning, og omvendt. Systemet sørger for dette ved å identifisere logiske koblinger mellom alle behovs- og forsyningsposter i ordrenettverket.  

 Dette prinsippet betyr at en endring i behov fører til en tilsvarende ubalanse på forsyningssiden i ordrenettverket. I motsetning vil en endring i forsyning fører til en tilsvarende ubalanse på behovssiden i ordrenettverket. I virkeligheten er ordrenettverket i en tilstand av konstant endring når brukere skrive inn, endrer og sletter ordrer. Sporing behandler ordrer dynamisk ved å reagere på en endringer når den registreres i systemet og blir en del av ordrenettverket. Så snart nye ordresporingsposter er opprettet, er ordrenettverket i balanse, men bare til neste endring skjer.  

 For å øke gjennomsiktigheten til beregninger i planleggingssystemet, vises ikke-sporede antall på siden **Ikke-sporede planleggingselementer**. Disse antallene representerer differansen i antall mellom kjent behov og foreslått forsyning. Hver linje på siden refererer til årsaken for det overflødige antallet , for eksempel **Rammebestilling**, **Sikkerhetslagernivå**, **Fast gjenbest.ant**, **Minimum bestillingsantall**, **Avrunding** eller **Avdemping**.  

### Forskyvning i ordresporing  
 I motsetning til reservasjoner som bare kan utføres mot tilgjengelig antall, er sporing mulig mot alle ordrenettverksenheter som er en del av beregningen av planleggingssystemet beregning av nettobehov. Nettobehovet beregnes som følger:  

 Nettobehov = Bruttobehov + Gjenbestillingspunkt - Tidsplanlagte mottak - Planlagte mottak - Beregnet disponibel saldo  

> [!NOTE]  
>  Behov som er knyttet til prognoser eller planleggingsparametere blir ikke sporet.  

### Eksempel: Sporing i salg, produksjon og overføringer  
 Følgende scenario viser hvilke sporingsposter som opprettes i **Reservasjonspost**-tabellen som resultat av ulike ordrenettverksendringer.  

 Anta bruk av følgende data for to varer som er konfigurert for sporing.  

|Vare 1|Name|Komponent|
|-|-|-|
||Disponibelt|100 enheter i VEST lokasjon<br /><br />- 30 enheter av PARTIA<br />- 70 enheter av PARTIB|  
|Vare 2|Name|Produsert vare|
||Produksjonsstykkliste|1 antall per Komponent|  
||Behov|Salg for 100 enheter i ØST lokasjon|  
||Forsyning|Frigitt produksjonsordre (generert med **Ordreplanlegging**-funksjonen for salg av 100 enheter)|  

På **Produksjonsoppsett**-siden er **Komponenter ved lokasjon**-feltet angitt til **RØD**.

 Følgende sporingsposter finnes i **Reservasjonspost**-tabellen basert på dataene i tabellen.  

 ![Første eksempel på ordresporingsposter i tabellen Reservasjonspost.](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")  

### Løpenummer 8 og 9  
 Det opprettes sporingskoblinger for komponentbehov for henholdsvis PARTIA og PARTIB, fra behovet i tabell 5407, **Prod.ordrekomponent**, til forsyningen i tabell 32, **Varepost**. **Reservasjonsstatus**-feltet inneholder **Sporing** for å angi at disse postene er dynamiske sporingskoblinger mellom forsyning og behov.  

> [!NOTE]  
>  **Partinr.**-feltet er tomt på behovslinjene fordi partinumrene ikke er angitt på komponentlinjene i den frigitte produksjonsordren.  

### Løpenummer 10  
 Fra salgsbehov i tabell 37, **Salgslinje**, opprettes en sporingskobling til forsyning i tabell 5406, **Prod.ordrelinje**. **Reservasjonsstatus**-feltet inneholder **Reservasjon**, og **Bundet til**-feltet inneholder **Ordre-til-ordre**. Dette er fordi den frigitte produksjonsordren ble spesifikt generert for ordren og må forbli tilknyttet, i motsetning til sporingskoblinger med reservasjonsstatusen **Sporing**, som opprettes og endres dynamisk. Hvis du vil ha mer informasjon, kan du se delen Automatiske reservasjoner i dette emnet.  

 På dette tidspunktet i scenariet overføres de 100 enhetene av PARTIA og PARTIB til ØST lokasjon av en overføringsordre.  

> [!NOTE]  
>  Bare overføringsordren bokføres nå, ikke mottak.  

 Følgende ordresporingsposter finnes nå i tabellen **Reservasjonspost**.  

 ![Andre eksempel på ordresporingsposter i tabellen Reservasjonspost.](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")  

### Løpenummer 8 og 9  
 Sporingsposter for de to komponentpartiene som gjenspeiler behov i tabell 5407, blir endret fra reservasjonsstatusen **Sporing** til **Overskudd**. Årsaken er at forsyningene som de var knyttet til før i tabell 32, er brukt av leveringen av overføringsordren.  

 Ekte overskudd, som i dette tilfellet gjenspeiler overflødige forsyning eller behov som forblir ikke-sporet. Dette er en indikasjon på ubalanse i ordrenettverket, som vil generere en handlingsmelding av planleggingssystemet med mindre det løses dynamisk.  

### Løpenummer 12 til 16  
 Siden de to partiene av komponenten bokføres på overføringsordren som levert, men ikke mottatt, er alle relaterte positive ordresporingsposter av reservasjonstypen **Overskudd**, som angir at de ikke er tilordnet til alle behov. For hver partinummer er én relatert til tabell 5741, **Overføringslinje**, og én post er relatert til vareposten på transittlokasjonen der varene finnes nå.  

 På dette tidspunktet i scenariet blir overføringsordren bokført som mottatt for komponenter fra ØST til VEST lokasjon.  

 Følgende ordresporingsposter finnes nå i tabellen **Reservasjonspost**.  

 ![Tredje eksempel på ordresporingsposter i tabellen Reservasjonspost.](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")  

 Sporingspostene ligner nå på det første punktet i scenariet, før overføringsordren ble bokført som bare levert, bortsett fra at postene for komponenten nå har reservasjonsstatusen **Overskudd**. Dette er fordi komponentbehovet fortsatt er i VEST lokasjon, som gjenspeiler at **Lokasjonskode**-feltet på produksjonsordrekomponentlinjen inneholder **VEST**, som definert i oppsettfeltet **Komponenter ved lokasjon**. Forsyningen som ble tildelt til dette behovet tidligere, er overført til ØST lokasjon og kan ikke nå spores fullstendig med mindre komponentbehovet på produksjonsordrelinjen endres til ØST lokasjon.  

 På dette tidspunktet i scenariet blir **Lokasjonskode** på produksjonsordrelinjen satt til **ØST**. På siden **Varesporingslinjer** vil i tillegg de 30 enhetene med PARTIA og de 70 enhetene i PARTIB bli tilordnet produksjonsordrelinjen.  

 Følgende ordresporingsposter finnes nå i tabellen **Reservasjonspost**.  

 ![Fjerde eksempel på ordresporingsposter i tabellen Reservasjonspost.](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")  

### Løpenummer 21 og 22  
 Siden komponentbehovet er endret til ØST lokasjon og forsyningen er tilgjengelig som vareposter i ØST lokasjon, blir nå alle sporingsposter for de to partinumrene fullstendig sporet, som angitt av reservasjonsstatusen **Sporing**.  

 **Partinr.**-feltet er nå fylt ut i sporingsposten for tabell 5407 fordi partinumrene ble tilordnet til produksjonsordrekomponentlinjene.  

 Hvis du vil se flere eksempler på ordresporingsposter i tabellen **Reservasjonspost**, kan du se hvitboken Tabellen Reservasjonspost på [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (krever pålogging).

## Handlingsmeldingssystem  
 Når sporingssystemet oppdager en ubalanse i ordrenettverket, oppretter det automatisk en handlingsmelding for å varsle brukeren. Handlingsmeldinger er systemgenererte kall for brukerhandling som angir detaljer om ubalansen og forslag om hvordan du gjenoppretter balansen for ordrenettverket. De vises som planleggingslinjer på **Planleggingsforslag**-siden når du velger **Hent handlingsmeldinger**. Handlingsmeldinger vises dessuten på planleggingslinjer som er generert av planleggingskjøringen, for å gjenspeile planleggingssystemets forslag om hvordan balansen kan gjenopprettes i ordrenettverket. I begge tilfeller kjøres forslagene i ordrenettverket når du velger **Utfør handlingsmelding**.  

 En handlingsmelding behandler ett stykklistenivå om gangen. Hvis brukeren godtar handlingsmeldingen, kan dette føre til flere handlingsmeldinger på neste stykklistenivå.  

 Tabellen nedenfor viser handlingsmeldingene som finnes.  

|Handlingsmelding|Description|  
|--------------------|---------------------------------------|  
|**Endre ant.**|Endrer antallet i en eksisterende forsyningsordre for å dekke endret eller nytt behov.|  
|**Tidsplanlegg på nytt**|Tidsplanlegger forfallsdatoen i en eksisterende ordre på nytt.|  
|**Resched. & Chg. Qty.**|Tidsplanlegger forfallsdatoen på nytt og endrer antallet i en eksisterende ordre.|  
|**Ny**|Oppretter en ny bestilling hvis behovet ikke kan oppfylles av de tidligere handlingsmeldingene.|  
|**Kanseller**|Kansellerer en eksisterende ordre.|  

 Sporingssystemet prøver alltid å løse en ubalanse i det eksisterende ordrenettverket. Hvis dette ikke er mulig, utstedes det en handlingsmelding for å opprette en ny ordre. Følgende er en prioritert liste som ordresporingenssystemet bruker når det avgjør hvordan balansen skal gjenopprettes. Hvis et ekstra behov er ankommet ordrenettverket, forsøker systemet å spore en ordren via følgende kontroller:  

1.  Se etter eventuell overflødig forsyning i eksisterende ordresporingspost for dette behovet.  
2.  Se etter planlagte og tidsplanlagte mottak sortert etter mottaksdato. Den senest mulige datoen velges.  
3.  Se etter tilgjengelige beholdning.  
4.  Kontroller om det finnes en forsyningsordre i gjeldende sporingspost. Hvis dette er tilfelle, utsteder systemet en handlingsmelding av typen **Endre** for å øke ordren.  
5.  Pass på at det ikke finnes en forsyningsordre i gjeldende sporingspost. Hvis dette er tilfelle, utsteder systemet en handlingsmelding av typen **Ny** for å opprette en ny ordre.  

 Et åpent behov passerer gjennom listen og forskyver tilgjengelig forsyning på hvert punkt. Eventuelle gjenværende behov dekkes alltid med sjekk 4 eller 5.  

 Hvis det oppstår en reduksjon i behovsmengden, prøve sporingssystemet å løse ubalansen ved å utføre de forrige kontrollene i omvendt rekkefølge. Dette betyr at eksisterende handlingsmeldinger om nødvendig kan endres eller til og med slettes. Sporingssystemet viser alltid det endelige resultatet av beregningene for brukeren.  

## Sporing og planlegging  
 Når planleggingssystemet kjører, sletter det alle eksisterende sporingsposter og handlingsmeldingsposter og gjenoppretter dem som planleggingslinjeforslag i samsvar med par med forsyning/behov og prioriteter. Når planleggingskjøringen er ferdig, er ordrenettverket i balanse.  

### Planleggingssystemet kontra sporing og handlingsmeldinger  
 Følgende sammenligning viser forskjellene mellom metodene som brukes av planleggingssystemet til å opprette forslag til planleggingslinjer, og metodene som brukes av sporingssystemet til å opprette sporingsposter og handlingsmeldinger.  

-   Planleggingssystemet håndterer hele forsynings- og behovsmønsteret for en bestemt vare, mens sporing håndterer ordren som aktiverte det.  

-   Planleggingssystemet håndterer alle nivåer i stykklistehierarkiet, mens sporing håndterer ett stykklistenivå om gangen.  

-   Planleggingssystemet oppretter koblinger mellom behov og forsyning i henhold til den prioriterte forfallsdatoen. Sporing oppretter koblinger mellom behov og forsyning i henhold til rekkefølgen for ordreregistreringen.  

-   Planleggingssystemet tar planleggingsparametere med i betraktning, mens sporing ikke gjør det.  

-   Planleggingssystemet oppretter koblinger i en brukeraktivert satsvis modus når det balanserer behov og forsyning, mens sporing oppretter koblingene automatisk og dynamisk mens brukeren registrerer ordrer.  

## Se også  
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
