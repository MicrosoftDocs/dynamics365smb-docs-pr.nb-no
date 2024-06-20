---
title: Gjennomgang – spore serie-partinumre
description: 'Dette emnet beskriver handlingene som må utføres for å forhindre salg av en defekt vare, og også spore og tilbakekalle varer når det er nødvendig.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Gjennomgang: spore serie-/partinumre

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Når det oppstår produktdefekter, må feilene identifiseres, og selskapet må unngå at påvirkede varer leveres til kunder. Hvis defekte varer allerede er levert, må du spore hvem som har mottatt dem, og om nødvendig tilbakekalle varene.  

Den første oppgaven i defekthåndtering er å undersøke hvor de defekte varene kommer fra, og hvor de ble brukt. Denne undersøkelsen er basert på historiske data og gjøres enklere ved å søke gjennom varesporingsposter på siden **Varesporing**.  

Den andre oppgaven i defekthåndtering er å avgjøre om de sporede varene er planlagt i åpne dokumenter, for eksempel ordrer eller forbrukskladder som ikke er bokført. Dette arbeidet utføres på siden **Søk etter poster**. Du kan bruke Søk etter poster-funksjonen til å søke i alle typer databaseposter.  

## Denne gjennomgangen

Denne gjennomgangen viser hvordan du identifiserer hvilke varer som er defekte, hvilken leverandør de kommer fra, og hvor de brukes, slik at du kan stoppe eller tilbakekalle disse ordrene.  

Denne gjennomgangen tar for seg følgende oppgaver:  

- Spore forbruk til opprinnelse.  
- Spore opprinnelse til forbruk.  
- Søke etter alle aktuelle poster som inneholder det sporede serie-/partinummeret.  

## Roller

Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

- Kvalitetskontrollør  
- Lagerleder  
- Ordrebehandler  
- Innkjøper  

## Forutsetninger

For å fullføre denne gjennomgangen må du gjøre følgende:  

- [!INCLUDE[prod_short](includes/prod_short.md)]-selskapet.  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## Hovedscenario

John, kvalitetskontrolløren, følger opp en ordreretur av vare 1002, Racersykkel. Kunden, Møbelhandleren A/S, klaget over at rammen hadde sprukne sveisesømmer. De tekniske kvalitetskontrollørene har bekreftet at racersykkelrammen for den returnerte sykkelen er defekt. Kvalitetskontrolløren må nå finne ut følgende:  

- Hvilke rammer som hadde feil  
- Hvilken bestilling det defekte partiet ble mottatt på  

Kvalitetskontrolløren vet, på grunnlag av informasjon fra salgsavdelingen, at den returnerte racersykkelen, vare 1002, hadde serienummeret SN1. Ved å bruke denne grunnleggende informasjonen til å finne ut hvor den ferdige racersykkelen siste ble brukt, og deretter må han søke tilbake til den tidligste opprinnelsen for å finne ut hvilket partinummer den defekte komponenten, racersykkelrammen, kom fra.  

Resultatet av denne første varesporingsoppgaven identifiserer hvilke racersykkelrammer som var defekte, og hvilken leverandør som leverte dem. Etterpå, men i samme generelle sporingsprosess, må kvalitetskontrolløren finne alle solgte racersykler med rammer fra feil parti, slik at disse ordrene kan stoppes eller tilbakekalles. Til slutt må kvalitetskontrolløren finne alle åpne dokumenter hvor det defekte partiet er i bruk slik at ingen flere transaksjoner gjøres.  

De to første oppgavene i defekthåndteringen gjøres på siden **Varesporing**. Den siste oppgaven gjøres på siden **Søk etter poster** sammen med **Varesporing**-siden.  

## Klargjøre eksempeldata

Du må opprette følgende nye varer:  

- 2000, Racersykkelramme: partispesifikk sporing, komponent for 1002  
- 1002, Racersykkel: serienummerspesifikk sporing  

Deretter må du opprette ulike kjøps-, produksjons- og salgstransaksjoner med de to varene.  

### Slik oppretter du varene  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. I feltet **Nr.** -feltet angir du **2000** og forstetter med å fylle ut følgende felt.  

    |Beskrivelse|Lagerenhet|Finans- - vare|Mva-bokføringsgruppe - vare|Bokføringsgruppe - lager|Varesporingskode|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Racersykkelramme|STK|RÅVARER|Mva.25|RÅVARER|PARTIALL|  

    > [!NOTE]  
    >  Hvis du vil angi lagerenheten, velger du **Ny**-knappen og deretter **PSC** på siden **Vareenheter**.  

4. Alle andre felt inneholder akseptable standarddata eller må ikke å fylles ut.  
5. Velg **OK**-knappen for å opprette det første nye varekortet, 2000.  
6. Velg **Ny**.  
7. I feltet **Nr.** -feltet angir du **1002** og forstetter med å fylle ut følgende felt.  

    |Beskrivelse|Lagerenhet|Finans- - vare|Mva-bokføringsgruppe - vare|Bokføringsgruppe - lager|Etterfyllingssystem|Varesporingskode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Racersykkel|STK|DETALJ|Mva.25|FERDIG|Prod.ordre|SNALL|  

    > [!NOTE]  
    >  Hvis du vil angi lagerenheten, velger du **Ny**-knappen og deretter **PSC** på siden **Vareenheter**.  

    Nå definerer du varens produksjonsoppsett.

8. Angi **1000** i feltet **Rutenr.** på hurtigfanen **Etterfylling**.  
9. Velg feltet **Prod.stykklistenr.**, og velg deretter **Avansert**.  
10. På siden **Produksjonsstykkliste - oversikt** velger du den første linjen **1000** og deretter handlingen **Rediger**.  
11. På siden **Produksjonsstykkliste** endrer du verdien i feltet **Status** til **Under utvikling**.  
12. Gå til en tom linje, og angi **2000** i **Nr.** -feltet, og angi deretter **1** i **Antall Per**-feltet.  
13. Endre verdien i **Status**-feltet tilbake til **Sertifisert**.  
14. Velg **OK**-knappen for å sette inn produksjonsstykklisten på varekortet og lukke siden **Produksjonsstykkliste**.  

    Deretter kjøper du racersykkelframmar fra Custom Metals Incorporated.  

### Kjøpe komponenter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Opprett en bestilling for leverandøren, Klubben, ved å fylle ut følgende linjefelt.  

    |Element|Antall|Partinr.|  
    |----|--------|-------|  
    |2000|10|PARTI1|  

4. Hvis du vil angi partinummeret, velger du **Varesporingslinjer**-handlingen.  
5. På siden **Varesporingslinjer** fyller du ut feltet **Partinr.** og **Antall (lagerenhet)** og lukker siden.  
6. Angi en verdi i feltet **Leverandørs fakturanr.**.  
7. Velg **Bokfør**-handlingen, velg **Motta og fakturer**-alternativet, og velg deretter **OK**-knappen.  

    Deretter kjøper du racersykkelrammer fra Coolwood Technologies.  
8. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
9. Velg handlingen **Ny**.
10. Opprett en bestilling for leverandøren, Kontorengros A/S, ved å fylle ut følgende linjefelt.  

    |Vare|Antall|Partinr.|  
    |----------|--------------|-------------|  
    |2000|11|PARTI2|  

11. Når du skal angi partinummeret, velger du hurtigfanen **Linjer**, **Linje**-gruppen og **Varesporingslinjer**-handlingen.  
12. På siden **Varesporingslinjer** fyller du ut feltet **Partinr.** og **Antall (lagerenhet)** og lukker siden.  
13. Angi en verdi i feltet **Leverandørs fakturanr.**.  
14. Velg **Bokfør**-handlingen, velg **Motta og fakturer**-alternativet, og velg deretter **OK**-knappen.  

    Deretter produserer du to racersykler, SN1 og SN2.  

### Produsere sluttvarer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitte produksjonsordrer** og velg den relaterte koblingen.  
2. Velg gruppen **Ny**.  
3. Opprett en ny frigitt produksjonsordre ved å fylle ut følgende felt.  

    |Kildenr.|Antall|Serienr.|  
    |----------|--------|----------|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4. Velg **Forny produksjonsordre**-handlingen, og velg deretter **OK** for å fylle ut linjen.  
5. Hvis du vil angi serienumre, velger du **Varesporingslinjer**-handlingen.  
6. På siden **Varesporingslinjer** fyller du ut feltet **Serienr.** og **Antall (lagerenhet)** og lukker siden.  

    Nå bokfører du forbruk av racersykkelrammer fra PARTI1.  
7. På siden **Frigitt produksjonsordre** velger du **Produksjonskladd**-handlingen.  
8. Velg forbrukslinjen for vare 2000 på siden **Produksjonskladd**, og velg **Varesporingslinjer**-handlingen.
9. På siden **Varesporingslinjer** velger du **Partinr.**-feltet, velger **PARTI1** og deretter **OK**-knappen.  
10. La alle andre standardverdier være på siden **Produksjonskladd**, og velg deretter handlingen **Bokfør**.  

    Deretter produserer du to racersykler til, SN3 og SN4.  

11. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitte produksjonsordrer** og velg den relaterte koblingen.  
12. Velg handlingen **Ny**.  
13. Opprett en ny frigitt produksjonsordre ved å fylle ut følgende felt i hodet.  

    |Kildenr.|Antall|Serienr.|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Velg handlingen **Forny produksjonsordre** for å fylle ut linjen.  
15. Når du skal angi serienumre, velger du handlingen **Varesporingslinjer** og deretter numrene på to linjer i **Serienr.**-feltet på siden **Varesporingslinjer**.  

    Nå bokfører du mer forbruk av racersykkelrammer fra PARTI1.  
16. På siden **Frigitt produksjonsordre** velger du **Produksjonskladd**-handlingen.  
17. Velg forbrukslinjen for vare 2000 på siden **Produksjonskladd**, og velg **Varesporingslinjer**-handlingen.
18. På siden **Varesporingslinjer** velger du **Partinr.**-feltet, velger **PARTI1** og deretter **OK**-knappen.  
19. La alle andre standardverdier være på siden **Produksjonskladd**, og velg deretter handlingen **Bokfør**.  

    Du har produsert fire racersykler, SN1 til SN4, og du har forbrukt fire av ti racersykkelrammer fra PARTI1, to rammer i hver produksjonsordre.  

20. Lukk produksjonskladden og produksjonsordrene.  

    Deretter selger du racersykler. Selg først racersykkelen med SN1 til Møbelhandleren A/S.  

### Selge sluttvarer

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny**-handlingen og opprett deretter en ordre ved å fylle ut feltene nedenfor.  

    |Kunde|Vare|Antall|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Møbelhandleren A/S|1002|1|SN1|  

3.  Når du skal angi serienummeret, velger du handlingen **Varesporingslinjer**, og velger deretter nummeret i **Serienr.**-feltet på siden **Varesporingslinjer**.  
4.  Velg **Bokfør**-handlingen, velg **Levere og fakturere**-alternativet, og velg deretter **OK**-knappen.  

    Nå kan du selge racersykkelen med SN2 til Kontorkomplett AS  

5.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
6.  Velg **Ny**-handlingen og opprett deretter en ordre ved å fylle ut feltene nedenfor.  

    |Kunde|Vare|Antall|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Kontorkomplett AS.|1002|1|SN2|  

7.  Når du skal angi serienummeret, velger du handlingen **Varesporingslinjer**, og velger deretter nummeret i **Serienr.**-feltet på siden **Varesporingslinjer**.  
8.  Velg **Bokfør**-handlingen, velg **Levere og fakturere**-alternativet, og velg deretter **OK**-knappen.  

    Til sist selger du noen racersykkelrammer separat. Kontorkomplett AS bestiller også fire separate racersykkelrammer for sin egen produksjonslinje.  

9. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
10. Velg **Ny**-handlingen og opprett deretter en ordre ved å fylle ut feltene nedenfor.  

    |Kunde|Vare|Antall|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Kontorkomplett AS.|2000|5|PARTI1|  

11. Når du skal angi serienummeret, velger du handlingen **Varesporingslinjer** på hurtigfanen **Linjer** i **Linje**-gruppen, og velger deretter nummeret i **Serienr.**-feltet på siden **Varesporingslinjer**.  

    > [!NOTE]  
    >  Ikke bokfør den siste ordren for fem racersykkelrammer.  

    Nå har du fullført klargjøringen av dataene som skal brukes til å vise funksjonene Varesporing og Søk etter poster.  

## Spore fra forbruk til opprinnelse

 Kvalitetskontrolløren vet, på grunnlag av informasjon fra salgsavdelingen, at den returnerte racersykkelen, vare 1002, har serienummeret SN1. Ved hjelp av denne enkle informasjonen kan han finne ut hvor den ferdige racersykkelen sist ble brukt, i dette tilfellet på følgeseddelen til Møbelhandleren A/S. Kvalitetskontrolløren må deretter søke bakover til den tidligste opprinnelsen for å bestemme hvilket partinummer den defekte racersykkelrammen kom fra og hvilken leverandør som leverte den.  

### Slik finner du ut hvilket parti den defekte rammen var i, og hvem som leverte den:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varesporing** og velg den relaterte koblingen.  
2.  Angi **SN1** i feltet **Serienr.filter** på siden **Varesporing**, og angi deretter **1002** i **Varefilter**-feltet.  
3.  Behold standardinnstillingen **Bare varesporet** i **Vis komponenter**-feltet, og behold standard sporingsmetode **Forbruk – Opprinnelse** i **Sporingsmetode**.  
4.  Velg handlingen **Spor**.  

    Merk at ett følgeseddelhode samsvarer med søkekriteriene. Før du fortsetter sporingen, kontrollerer du at leveringen inneholdt den defekte racersykkelen til Møbelhandleren A/S.  

5.  Merk sporingslinjen, og velg deretter **Vis dokument**-handlingen.  

    Fortsett å spore opprinnelsen til følgeseddelen for racersykkelen med nummeret SN1.  
6.  Klikk +-ikonet på sporingslinjene for gradvis å utvide og søke tilbake i kjeden av transaksjoner som følgeseddelen opprinnelig kommer fra.  

    Du kan spore følgende transaksjonshistorikk:  

    - Det første bokførte dokumentet bakover i kjeden av transaksjoner er avgangsbokføringen av SN1 fra den første frigitte produksjonsordren.  
    - Det neste bokførte dokumentet bakover i kjeden etter dette er forbruksbokføringen fra den første frigitte produksjonsordren. Her ser kvalitetskontrolløren at en racersykkelramme fra PARTI1 ble brukt.  
    - Det laveste bokførte dokumentet i denne kjeden er det bokførte kjøpsmottaket der racersykkelrammer med PARTI1 kom inn på lageret.  

    Kvalitetskontrolløren har nå funnet partiet med racersykkelrammer som hadde defekter, og han kan søke etter den siste sporingslinjen for å vise hvilken leverandør som leverte dem, nemlig Klubben.  

    > [!NOTE]  
    >  Ikke foreta ytterligere endringer av sporingsresultatet siden du skal bruke det i neste del.  

     Nå har du fullført første oppgave i defekthåndteringen ved å bruke **Varesporing**-siden. Kvalitetskontrolløren må nå finne ut om racersykkelrammer fra PARTI1 har vært behandlet i andre bokførte dokumenter.  

## Spore fra opprinnelse til forbruk

 Kvalitetskontrolløren har funnet ut at de defekte racersykkelrammene kom fra PARTI1. Han må nå finne eventuelle andre racersykler som har racersykkelrammer fra det defekte partiet, slik at disse syklene kan bli stoppet eller tilbakekalt.  

 Én metode for å klargjøre denne sporingsoppgaven på siden **Varesporing** er å angi PARTI1 manuelt i feltet **Partinr.filter** og 2000 i **Varefilter**-feltet. Denne gjennomgangen bruker funksjonen **Spor motsatt - fra linje**.  

### Slik finner du alt forbruk for det defekte partiet:  

1.  Merk linjen med kjøpsmottaket, siste sporingslinje, på siden **Varesporing**, og velg deretter **Spor motsatt - fra linje**.  

    Sporingsresultatet er nå basert på filtrene for sporingslinjen for kjøpsmottaket, PARTI1 og vare 2000, og resultatet er basert på sporingsmetoden **Opprinnelse - forbruk**.  

    Fortsett å utvide alle sporingslinjene hvis du vil ha en oversikt over alt forbruk for vare 2000 i PARTI1.  

2.  Velg handlingen **Utvid alle**.  

    De fire første sporingslinjene refererer til følgeseddelen for Møbelhandleren A/S, som allerede er løst. Den siste linjen angir at enda en racersykkel, SN2, ble produsert i samme frigitte produksjonsordre og deretter solgt og levert med en annen følgeseddel.  

    Kvalitetskontrolløren gir øyeblikkelig beskjed til salgsavdelingen, slik at de kan foreta en tilbakekalling av den defekte racersykkelen fra kunden, Kontorkomplett AS.  

    Samtidig kan han se ut fra de tre siste sporingslinjene at to nye varer, SN3 og SN4, er produsert basert på racersykkelrammer fra PARTI1. Han blokkerer disse sluttvarene på lageret.  

    Nå har du fullført andre oppgave i defekthåndteringen ved å bruke **Varesporing**-siden til defekthåndtering. Siden **Varesporing**-siden er basert på bare bokførte poster, må kvalitetskontrolløren gå videre til **Søk etter poster**-siden for å sikre at PARTI1 ikke brukes i dokumenter som ikke er bokført.  

## Søke etter alle poster for et serie-/partinummer

 Kvalitetskontrolløren brukte **Varesporing**-siden til å finne ut at PARTI1 inneholdt de defekte racersykkelrammene, hvem som leverte dem, og hvilken bokført transaksjon de er brukt i. Han må nå finne ut om PARTI1 finnes i noen åpne dokumenter ved å integrere fra sporingsresultatet til **Søk etter poster**-siden der han kan foreta et søk gjennom alle databaseposter.  

### Slik finner du alle forekomster av PARTI1 i poster som ikke er bokført, for eksempel åpne ordrer:  

1.  Velg den første sporingslinjen på siden **Varesporing**, kjøpsmottaket for PARTI1.  
2.  Velg handlingen **Søk etter poster**.  

    **Søk etter poster**-siden er forhåndsinnstilt med søkefiltre basert på sporingsresultatet for PARTI1. Kvalitetskontrolløren ser at de fleste postene angår dokumenter som allerede er identifisert på siden **Varesporing**. Den siste Søk etter poster-linjen av typen Produksjonsordre refererer for eksempel til de to frigitte produksjonsordrene som forbrukte racersykkelrammer fra PARTI1.  

    Den andre Søk etter poster-linjen av typen **Salgslinje** er imidlertid en dokumentlinje som ikke er bokført. Dermed blir dette undersøkt av kvalitetskontrolløren.  

3.  Merk den andre Søk etter poster-linjen, velg handlingen **Vis** for å åpne salgslinjeposten. Du kan eventuelt også velge verdien i **Antall poster**-feltet.  

    Her ser kvalitetskontrolløren én åpen salgslinje for de defekte racersykkelrammene. Han foreslår øyeblikkelig for salgsavdelingen at de kansellerer ordren og oppretter en ny produksjonsordre som er basert på racersykkelrammer uten defekter.  

 Nå har du fullført gjennomgangen av hvordan du bruker **Søk etter poster**-siden til defekthåndtering sammen med **Varesporing**-siden.  

## Se også

[Arbeide med serie- og partinumre](inventory-how-work-item-tracking.md)  
[Vare varesporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Søk etter poster](ui-find-entries.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
