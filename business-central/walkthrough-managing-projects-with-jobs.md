---
title: Gjennomgang – administrere prosjekter med prosjekter
description: 'Denne gjennomgangen gir deg en innføring i prosjektstyringsfunksjonene i prosjekter, slik at du kan planlegge bruken av selskapets ressurser og mer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Gjennomgang: prosjektstyring

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

I denne gjennomgangen får du en innføring i prosjektstyringsfunksjoner. Prosjekter brukes til å estimere forbruket av selskapets ressurser og til å holde rede på de ulike kostbeløpene som er knyttet til ressursene i et bestemt prosjekt. Prosjekter omfatter forbruk av ansattes arbeidstid, maskindriftstid, lagervarer og andre typer forbruk som det kan hende du vil spore etter som et prosjekt går fremover.  

 Denne gjennomgangen tar for seg oppsett av et nytt prosjekt i tillegg til noen vanlige oppgaver, for eksempel håndtering av faste priser, betaling i avdrag, bokføring av fakturaer fra prosjekter og kopiering av prosjekter.  

## Denne gjennomgangen

 Denne gjennomgangen viser følgende oppgaver:  

### Definere et prosjekt

 Opprettelse av et prosjekt blir enkelt når du har definert budsjettstrukturen for prosjekter. Denne gjennomgangen omhandler følgende prosedyrer:  

- Opprett prosjektoppgavelinjer og planleggingslinjer.  
- Opprett prosjektspesifikke priser for varer, ressurser og finanskonti.  
- Fakturering fra et prosjekt.  

### Håndtere faste priser

 Du kan håndtere faste priser og priser på tjenester og varer som er avtalt med kunder på forhånd. I denne gjennomgangen kan du gjøre følgende:  

- Vise hvordan kontraktverdier og fakturaverdier fastsettes.  
- Tillate ekstra arbeid i estimatet som ikke er fakturert.  

### Kopiere et prosjekt

 Denne delen av gjennomgangen fokuserer på hvordan du kopierer deler av et prosjekt eller hele prosjektet for å redusere manuell registrering av data og forbedre korrektheten. Det inkluderer følgende:  

- Kopiering av deler av et prosjekt til et nytt prosjekt.  
- Kopiering av prosjektspesifikke priser.  
- Kopiering av planleggingslinjer  

### Foreta betaling i avdrag

 Når et stort, kostbart prosjekt varer lenge, gjør kunden ofte en avtale med selskapet om å betale i avdrag. Dette scenariet viser hvordan du definerer betaling i avdrag, og tar for seg følgende:  

- Opprette betaling i avdrag for et prosjekt.  
- Fakturering av kunder  
- Redegjørelse for bruk i et prosjekt konfigurert for betaling i avdrag.  

## Roller

 Denne gjennomgangen omfatter oppgaver for følgende roller:  

- Prosjektleder  
- Medlem i prosjektgruppen  

## Forutsetninger

 Før du kan utføre oppgavene i gjennomgangen, må du gjøre følgende:  

- Installer CRONUS-demonstrasjonsdatabasen.
- Opprett eksempeldata ved å bruke fremgangsmåten i neste del.  

## Hovedscenario

Denne gjennomgangen fokuserer på CRONUS, et design- og konsulentfirma som designer og innreder nye infrastrukturer, for eksempel konferanserom og kontorer, med møbler, tilbehør og reoler. Mesteparten av arbeidet er prosjektorientert. Prakash, prosjektleder hos CRONUS, bruker prosjekter til å få en oversikt over alle pågående oppgaver som CRONUS har startet, samt ferdige oppgaver. Prakash er vanligvis den som setter opp avtaler med kunder og legger inn kjernen i prosjektet, som er oppgave- og planleggingslinjer i tillegg til priser, inn [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash synes det er enkelt å opprette, vedlikeholde og gå gjennom informasjon. Prakash liker også hvordan [!INCLUDE[prod_short](includes/prod_short.md)] gjør det mulig å kopiere prosjekter og betale i avdrag.

 Tricia, som er medlem i prosjektgruppen og rapporterer til Florian, har ansvaret for den daglige overvåkingen av prosjektet. Tricia registrerer sitt eget arbeid i tillegg til arbeidet utført av teknikere i hver oppgave, registrerer varene de har brukt, og påløpte kostbeløp.  

## Klargjøre eksempeldata

 Hvis du vil forberede denne gjennomgangen, må du legge til Tricia som en ny ressurs.  

### Slik klargjør du eksempeldataene:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.  
2. Velg **Ny**-handlingen for å opprette et nytt ressurskort.  
3. Skriv inn følgende informasjon på hurtigfanen **Generelt**:  

    - **Nr.**: **Marie**  
    - **Navn**: **Marie**  
    - **Skriv inn**: **person**  

4. Velg feltet **Lagerenhet**, og velg **Ny**-handlingen for å åpne siden **Ressursenhet**. Velg **Time** i **Kode**-feltet.  
5. Skriv inn følgende informasjon på hurtigfanen **Fakturering**:  

    - **Direkte enhetskost**: **5**  
    - **Indirekte kost-%**: **4**  
    - **Enhetskost**: **10**  
    - **Bokføringsgruppe - vare**: **Service**  
    - **Mva-bokføringsgruppe – vare**: **mva 25**  

6. Lukk siden.

I neste fremgangsmåte kan du opprette en prosjektkladd for Tricia for å bokføre forbruket.  

### Slik oppretter du en prosjektkladd  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder** og velg den relaterte koblingen.  
2. Velg **Bunkenavn**-feltet på **Prosjektkladd**-siden. Siden **Prosjektkladder** åpnes.  
3. Velg **Ny**-handlingen for å opprette en ny linje med følgende informasjon:  

    - **Navn**: **Marie**  
    - **Beskrivelse**: **Marie**  
    - **Nr.serie**: **PKLD-GEN**  

4. Velg **OK**-knappen for å lagre endringene.

## Definere et prosjekt

 I dette scenariet har CRONUS fått i oppdrag av en kunde, Progressive Home Furnishings, å designe et konferanserom og en spisesal. Kunden er basert i USA, og prosjektet krever spesialprogramvare. Prosjektlederen inngår en avtale med kunden og oppretter et prosjekt som er i tråd med avtalen.  

### Slik definerer du et prosjekt  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
2. Velg **Ny**-handlingen for å opprette et nytt kort.  
3. Skriv inn følgende informasjon på hurtigfanen **Generelt**:  

    - **Beskrivelse**: **Rådgivning om oppsett av konferanserom**  
    - **Faktura til-kundenr.**: **01445544**  

4. Skriv inn følgende informasjon på hurtigfanen **Bokføring**:  

    - **Status**: **Planlegging**  
    - **Prosjektbokføringsgruppe**: **Definere**  
    - **VIA-metode**: **Kostverdi**  

5. Skriv inn dagens dato i feltene **Sluttdato** og **Startdato** på hurtigfanen **Varighet**. Disse datoene er til hjelp ved valutaomregning når prosjektet faktureres.  
6. På hurtigfanen **Utenrikshandel** setter du valutakoden til **USD**. Hvis du velger USD i feltet **Valutakode for faktura**, faktureres prosjektet i amerikanske dollar og planlegges bare i den lokale valutaen til CRONUS.  

 +Du kan tilpasse prissettingen for kunder per prosjekt, avhengig av avtalene du har definert. I neste fremgangsmåte angir prosjektlederen en kostpris for Maries tid, angir pris for programvaren som kreves, og legger til i reisekostnadene at kunden har godtatt å betale.  

### Slik tilpasser du prising:  

1. Fra **Prosjektkort**, velg **Ressurs**-handlingen.  
2. Skriv inn følgende informasjon på siden **Ressurspriser for prosjekt**:  

    - **Kode**: **Marie**  
    - **Enhetspris**: **20**  

3. Lukk siden.  
4. Velg handlingen **Vare**.  
5. Angi følgende informasjon og tilpasset pris på siden **Varepriser for prosjekt**:  

    1. **Varenr.**: **80201 (Grafikkprogram)**  
    2. **Enhetspris**: **200**  

6. Lukk siden.  
7. Velg **Finanskonto**-handlingen.  
8. På siden **Finanskontopriser for prosjekt** skriver du inn følgende informasjon og reisekostnadene, som kunden har godtatt å betale kost pluss 25 prosent for:  

    1. **Finanskonto**: **8430 (Reise)**  
    2. **Enhetskostfaktor**: **1,25**  

9. Lukk siden.  

 De siste trinnene for konfigurasjon av et prosjekt er å legge til prosjektoppgavene og planleggingslinjene som inngår i hver oppgave. Planleggingslinjene fastsetter hva som faktureres til kunden.  

### Slik legger du til prosjektoppgaver  

1.  Velg **handlingen** Prosjektaktivitetslinjer **på Prosjekt-kortet** for det nye prosjektet.  
2.  Tabellen nedenfor beskriver informasjonen som du bør angi i feltene.  

    |Prosjektoppgavenr.|Description|Prosjektoppgavetype|  
    |------------------|---------------------------------------|-------------------|  
    |1 000|Konsultasjon om oppsett av rom|Fra-sum|  
    |1010|Konsultasjonsmøte med kunden|Konto|  
    |1020|Utvikling|Konto|  
    |1090|Konsultasjon totalt|Til-sum|  

3.  Hvis du vil vise at noen oppgaver er underkategorier av andre oppgaver, velger du handlingen **Rykk inn prosjektoppgaver**.  

 En planleggingslinje kan være én av følgende typer:  

- **Budsjett**: Lagt til i tidsplanen, men ikke fakturert.  
- **Fakturerbar**: Fakturert, men ikke lagt til i tidsplanen.  
- **Både Budsjett og Fakturerbar**: Faktureres og legges til i tidsplanen.  

 I denne gjennomgangen bruker prosjektlederen **Både Budsjett og Fakturerbar**. De oppretter tre planleggingslinjer for oppgave 1010 og to planleggingslinjer for oppgave 1020.  

### Slik oppretter du planleggingslinjer:  

1. Velg linje 1010 og velg deretter handlingen **Prosjektplanleggingslinjer**.  

2. Opprett planleggingslinjer med følgende informasjon:  

    | Linje | Linjetype | Planleggingsdato  | Type        | Antall   | Antall | Enhetspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både Budsjett og Fakturerbar | (dagens dato) | Ressurs | Marie | 40        |     |
    | 2    | Både Budsjett og Fakturerbar | (dagens dato) | Ressurs | Egil | 40        |     |
    | 3    | Både Budsjett og Fakturerbar | (dagens dato) | Finanskonto | 8430 (reise) | 2 | 400    |

     Lukk siden. Totalene oppdateres på siden **Prosjektoppgavelinjer**.  
3. Velg linje 1020 og velg deretter handlingen **Prosjektplanleggingslinjer**. Angi følgende informasjon:  

    | Linje | Linjetype | Planleggingsdato  | Type        | Antall   | Antall | Enhetspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både Budsjett og Fakturerbar | (dagens dato) | Ressurs | Marie | 80        |     |
    | 2    | Både Budsjett og Fakturerbar | (dagens dato) | Vare | 80201 (grafikkprogram) | 1 |     |

4. Lukk siden. Totalene oppdateres på siden **Prosjektoppgavelinjer**.  

## Beregne gjenstående forbruk

 Tricia, medlemmet i prosjektgruppen, har arbeidet på prosjektet en stund og vil registrere timene og forbruket. Tricia har ikke arbeidet flere timer enn det som ble avtalt med kunden på forhånd. Tricia bruker kjørselen **Beregn gjenstående forbruk** til å beregne gjenstående forbruk i en prosjektkladd. For hver oppgave beregner kjørselen differansen mellom planlagt forbruk av varer, ressurser og finansutgifter og det faktiske forbruket som er bokført i prosjektposter. Det gjenstående forbruket vises deretter i prosjektkladden, som hun kan bokføre det fra.  

### Slik beregner du gjenstående forbruk:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder** og velg den relaterte koblingen.  
2. Åpne oversikten **Prosjektkladd** i **Bunkenavn**-feltet på siden **Prosjektkladd**. Velg prosjektkladden **Tricia**.  
3. Velg handlingen **Beregn gjenstående forbruk**.  
4. På siden **Beregn gjenstående forbruk for prosjekt**, på hurtigfanen **Prosjektoppgave**, velg feltet **Prosjektnr.** og det aktuelle prosjektnummeret, vanligvis J00010.  
5. Skriv inn **J00001** i feltet **Bilagsnr.** på hurtigfanen **Alternativer**. Dette gjør det enklere å spore bokføringen senere.  
6. Angi dagens dato som bokføringsdato.  
7. Velg **OK**-knappen. Dermed genereres prosjektkladdelinjer basert på planleggingslinjene som Prakash opprettet.  
8. Velg **OK**-knappen på bekreftelsessiden. De genererte linjene legges til i prosjektkladden.  
9. Kontroller at alle bilagsnumrene er J00001, og velg deretter **Bokfør**-handlingen. Velg **Ja** for å bekrefte bokføringen.  

Linjene er nå bokført.  

## Opprette og bokføre en prosjektsalgsfaktura

 Nå kan Marie opprette en ny faktura for hele prosjektet eller for deler av et prosjekt. Marie kan også knytte fakturaen til en annen faktura for samme kunde for det samme prosjektet. I dette tilfellet fakturerer Tricia for hele prosjektet fordi prosjektet nå er fullført.  

### Slik oppretter du en prosjektsalgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg prosjektet du opprettet tidligere, og velg deretter handlingen Opprett salgsfaktura **for** prosjekt.  
3.  På hurtigfanen **Prosjektoppgave** tømmer du eventuelle filtre på **Prosjektoppgavenr.** for å fakturere prosjektet. I feltet **Prosjektnr.** velger du det aktuelle prosjektet.  
4.  Fyll ut bokføringsdatoen og definer om du vil opprette én faktura per oppgave eller én enkelt faktura for alle oppgaver, på hurtigfanen **Alternativer**.  
5.  Velg **OK**-knappen for å opprette fakturaen, og velg deretter **OK**-knappen på bekreftelsessiden.  

 Etter at Tricia har opprettet fakturaen, kan hun f.eks. få tilgang til den fra rollesenteret **Ordrebehandler**. 

### Slik bokfører du en ny salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2.  Åpne fakturaen for kundenr. 01445544. Nå kan du se informasjonen som ble registrert på planleggingslinjene.  
3.  Velg handlingen **Bokfør**. Velg **Ja** for å bekrefte bokføringen.  

### Slik viser du den bokførte fakturaen:  

1.  Åpne prosjektet, og velg deretter handlingen **Prosjektplanleggingslinjer** .  
2.  Velg en planleggingslinje som er fakturert, og velg deretter handlingen **Salgsfaktura/kreditnota**.
3. På **siden Prosjektfakturaer** velger du handlingen **Åpne salgsfaktura/kreditnota** .  

 Tricia har et spørsmål om prisene, kostnadene og fortjenesten som er relevante for dette prosjektet, så Tricia får tilgang til denne informasjonen på **Statistikk-siden** .  

### For å åpne statistikksiden  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Statistikk**. Du kan se detaljert informasjon om prosjektpriser, kostnader og fortjeneste i både lokal og utenlandsk valuta.  
3.  Velg Lukk-knappen **for** å lukke Prosjektstatistikk-siden **·** .  

## Håndtere faste priser

 CRONUS har fått i oppdrag å sette opp konferanserom. Som prosjektleder ønsker Florian en god oversikt over oppgavene som kreves for prosjektet, med tilhørende budsjetterte og påløpte kostnader for hver oppgave. I tillegg ønsker Prakash å vite den totale kontraktsprisen for prosjektet og beløpet som er fakturert til dette punktet. De har kommet til enighet med kunden om fast pris på prosjektet.  

### Slik håndterer du faste priser i prosjekter  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
2. Velg Guildford-prosjektnummeret **·**, og velg deretter handlingen **Prosjektoppgavelinjer** .  
3. Velg linje 1120, og høyreklikk beløpet i feltet **Budsjett (kostbeløp)** og velg **Drilldown**.  

     Ved å gå gjennom prosjektplanleggingslinjene er det bestemt at Prakash også trenger Tricia i 30 timer på dette trinnet i prosjektet. Prakash avtaler en fast pris med kunden.  

4. På siden **Prosjektoppgavelinjer** velger du linje 1120, og deretter velger du handlingen **Prosjektplanleggingslinjer**. Opprett en planleggingslinje med følgende informasjon:  

    | Linje | Linjetype | Type        | Antall   | Antall |
    |------|-----------|-------------|-------|----------|
    | 1    | Både Budsjett og Fakturerbar  | Ressurs | Marie | 30 |

     Lukk siden.  
5. Høyreklikk feltet **Budsjett (kostbeløp)**, og velg **Drilldown** på nytt på siden **Prosjektoppgavelinjer**. Vis endringene av estimatet. Du ser at de 30 timene er lagt til i estimatet.  
6. Lukk sidene.  

Etter å ha blitt lagt til i tidsplanen for denne oppgavelinjen, arbeider Marie 25 timer på prosjektet og registrerer disse timene i prosjektkladden.  

### Slik angir du timer i en prosjektkladd  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder** og velg den relaterte koblingen.  
2. Skriv inn følgende informasjon på en ny linje:  

    - **Linjetype**: **(tom)**  
    - **Bokføringsdato**: **(dagens dato)**  
    - **Bilagsnr.**: **J00002**  
    - **Prosjektnr.**: **Tremøbler AS**  
    - **Prosjektoppgavenr.**: **1120**  
    - **Type**: **Ressurs**  
    - **Nr.**: **Marie**  
    - **Antall**: **25**  

3. Velg handlingen **Bokfør**.  

     Noen få dager senere arbeider Tricia for ytterligere 10 timer på prosjektet og har nå arbeidet 35 timer totalt. Siden avtalen gjelder for 30 timer med kunden, blir kunden bare belastet for 5 av disse timene. Tricia legger til de ekstra fem timene hun arbeidet, manuelt i timeplanen.  

4. Velg handlingen **Beregn gjenstående forbruk** på siden **Prosjektkladd**.  
5. Angi følgende informasjon på hurtigfanen **Alternativer** på siden **Beregn gjenstående forbruk for prosjekt**:  

    - **Bilagsnr.**: **J00003**  
    - **Bokføringsdato**: **(dagens dato)**  

6. På hurtigfanen **Prosjektoppgave** angir du følgende informasjon:  

    - **Prosjektnr.**: **Tremøbler AS**  
    - **Prosjektoppgavenr.**: **1120**  

7. Velg **OK**-knappen for å kjøre beregningen.

    Det gjenstår fem timers arbeid for Marie. **Linjetype**-feltet er tomt, noe som betyr at det bare er forbruket som gjenstår å bli bokført, siden arbeidet allerede er planlagt.  

8. Opprett en ny linje med følgende informasjon i **Prosjektkladd**-vinduet: Kontroller at begge prosjektnumrene er sekvensielle med de du allerede har brukt:  

    - **Linjetype**: **Budsjett**  
    - **Prosjektnr.**: **Tremøbler AS**  
    - **Prosjektoppgavenr.**: **1120**  
    - **Type**: **Ressurs**  
    - **Nr.**: **Marie**  
    - **Antall**: **5**  

     Estimatkostbeløpene og estimatprisene oppdateres ved hjelp av linjetypen **Budsjett** uten å oppdatere kontraktkostbeløpene og kontraktprisene som er fakturert til kunden.  

9. Velg handlingen **Bokfør**. Velg **OK**-knappen for å lukke siden.  
10. Åpne **prosjektlisten** .  
11. Velg jobben TREM, og velg deretter linje 1120 i delen **Prosjektoppgavelinjer**, og høyreklikk deretter beløpet i feltet **Budsjett (kostbeløp)**. Velg **Drilldown** for å vise informasjonen.  

     Endringer blir automatisk lagt inn på linjen for prosjektoppgavenr. 1120. Fem ekstra timer arbeid av Tricia er lagt til i totalkostnaden for planlagt arbeid i tidsplanen.  

12. Velg **Lukk**-knappen for å lukke siden.  
13. Høyreklikk beløpet i feltet **Kontrakt (kostbeløp)**, og velg **Drilldown** for å vise informasjonen.  

I kontraktens salgsbeløp er bare de opprinnelig avtalte 30 timene tatt med siden dette er det som ble avtalt med kunden.  

## Kopiere prosjekter

Florian har inngått en avtale med en kunde, Møbelhandleren A/S, om å foreta oppsett av 10 konferanserom. Avtalen ligner et tidligere prosjekt. Derfor vil det spare tid å kopiere det tidligere prosjektet.  

På **siden Kopier prosjekt** kan du velge prosjektet og aktivitetslinjene du vil kopiere. Du kan også kopiere kildeprosjektpostene, som gjør at det opprettes planleggingslinjer basert på faktisk forbruk, eller du kan kopiere planleggingslinjene fra kildeprosjektet, slik at de opprinnelige planleggingslinjene kopieres til det nye prosjektet. Deretter kan du velge hvilken planleggingslinjetype eller postlinjetype du vil inkludere, og velge bare det som er relevant for det nye prosjektet. Til slutt kan du velge prosjektet du vil kopiere til, og angi om priser og antall også skal kopieres.  

### Slik kopierer du et prosjekt  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  **Velg handlingen Ny** for å opprette et nytt prosjekt. Angi følgende informasjon:  

    - **Beskrivelse**: **Oppsett av ti konferanserom**  
    - **Faktura til-kundenr.**: **20000**  

3. Velg handlingen **Kopier prosjektoppgaver fra**.  
4. Angi følgende på siden **Kopier prosjektoppgaver**:  

    - **Prosjektnr.**: **Tremøbler AS**  
    - **Prosjektoppgavenr. fra**: **1000**  
    - **Kilde**: **Prosjektplanleggingslinjer**  
    - **Inkl. planleggingslinjetype**: **Budsjett + Fakturerbar**  
    - **Til prosjektnr.**: **Tremøbler AS Oppsett av ti konferanserom**  
    - Velg feltene **Kopier dimensjoner** og **Kopier mengde**.  

5.  **Velg OK-knappen** for å kopiere prosjektet, og velg **deretter OK-knappen** for å lukke bekreftelsessiden.  

Ved å sammenligne priser, prosjektaktivitetslinjer og prosjektplanleggingslinjer for de to prosjektene, kan du se at informasjonen ble kopiert.  

## Foreta betaling i avdrag

CRONUS har nettopp fått et stort prosjekt som kommer til å ta et år å fullføre. Siden mange ressurser må avsettes, setter prosjektlederen opp kontrakten slik at kunden betaler en del av prisen på forskudd, en del når prosjektet er halvveis fullført, og den siste delen når prosjektet er fullført.  

### Slik konfigurerer du et nytt budsjett  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. Velg **Ny**-handlingen på siden **Kontoplan** for å opprette et nytt kort.  
3. Angi følgende informasjon på kortet **Ny finanskonto**:  

    - **Nr.**: **40255**  
    - **Navn**: **Prosjektbetaling**  

4. I hurtigfanen **Bokføring** i feltet **Bokføringsgruppe - vare** velger du **Tjenester**. Lukk siden.  
5. Velg **Nr. 40255 Prosjektbetaling** på siden **Kontoplan**, og velg deretter **Innrykk kontoplan**-handlingen. Velg **Ja** for å bekrefte.  

Fremgangsmåtene nedenfor viser hvordan du oppretter et nytt prosjekt, angir priser og deretter definerer betaling i avdrag. Du kan opprette spesifikke prosjektlinjer som er reservert for betalingen i avdrag, på prosjektoppgavelinjene. Alt fullført arbeid på prosjektet som legges til i tidsplanen, angis på forbrukslinjene. Linjetypen er **Fakturerbar** for hver betalingsoppgavelinje på planleggingslinjene, som betyr at kunden blir fakturert. Angi en ny linje for avdraget. På forbruksoppgavelinjen kan du angi informasjonen for varene og ressursene som er brukt i dette prosjektet, noe som vil øke tidsplanen, for eksempel ansattes timer og varer som er brukt i prosjektet.  

### Slik foretar du betaling i avdrag:  

1. Opprett et nytt prosjekt.  
2. Fyll inn følgende informasjon på det nye **Project-kortet** :  

    - **Beskrivelse**: **Ny innredning av resepsjon**  
    - **Faktura til-kundenr.**: **30000**  
    - **Prosjektbokføringsgruppe**: **Definere**  
    - **VIA-metode**: **Kostverdi**  

3. På prosjektkortet velger du handlingen **Priser**, og deretter velger du handlingen **Ressurs**. Angi følgende informasjon:  

    - **Kode**: **Marie**  
    - **Enhetspris**: **10**  

     Lukk siden.  

4. Legg **til prosjektaktivitetslinjer i** Oppgaver-delen **på Prosjekt-kortet**, som beskrevet i tabellen nedenfor:  

    | Linje | Prosjektoppgavenr. | Description          | Prosjektoppgavetype |
    |------|--------------|----------------------|---------------|
    | 1    | 1 000         | Betalingsavdrag | Bokføring       |
    | 2    | 2000         | Bruk                | Bokføring       |
    | 3    | 3 000         | Betaling - Halvveis     | Konto       |
    | 4    | 4000         | Betaling - fullføring | Bokføring       |

5. Velg oppgave 1000, og velg deretter handlingen **Prosjektplanleggingslinjer**.  

6. Opprett en planleggingslinje med følgende informasjon:  

    | Linje | Linjetype | Planleggingsdato  | Type        | Antall   | Antall | Enhetspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (dagens dato) | Finanskonto | 40255 | 1        | 5000       |

     Lukk siden.  

7. Velg oppgave 2000, og velg deretter handlingen **Prosjektplanleggingslinjer**.  

8. Opprett en planleggingslinje med følgende informasjon:

    | Linje | Linjetype | Planleggingsdato  | Type     | Antall    | Antall |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budsjett    | (dagens dato) | Ressurs | Marie | 120      |
    | 2    | Budsjett    | (dagens dato) | Element     | 70104  | 10       |

     Lukk siden. På siden **Prosjektoppgavelinjer** kan du se at estimatbeløpene har blitt oppdatert.  

9. Velg oppgave 32000, og velg deretter handlingen **Prosjektplanleggingslinjer**.  

10. Opprett en planleggingslinje med følgende informasjon:

    | Linje | Linjetype | Planleggingsdato   | Type        | Antall   | Antall | Enhetspris |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (en fremtidig dato) | Finanskonto | 40255 | 1        | 5000       |

     Lukk siden.  

11. Opprett en lignende planleggingslinjepost for prosjektoppgave 4000.  

 Nå som oppgave- og planleggingslinjene er registrert, oppretter Florian en faktura for den første betalingen. Prakash gjør dette fra prosjektoppgavelinjene for å sikre at fakturaen bare inneholder linjene for den første betalingen. Du kan åpne ordren fra planleggingslinjene eller oppgavelinjene.  

### Slik oppretter du en faktura:  

1.  På siden **Prosjektoppgavelinjer** velger du linje 1000, og deretter velger du handlingen **Opprett salgsfaktura**.  
2.  Angi dagens dato som bokføringsdato på siden **Opprett salgsfaktura**, angi **Per oppgave**, og klikk **OK** for å opprette en faktura med standardinformasjon. Velg **OK**-knappen for å lukke bekreftelsessiden.  
3.  Velg handlingen **Salgsfaktura/kreditnota**. I salgsfakturaen kan du se at det bare er avdraget som er tatt med i fakturaen. Du kan nå sende denne til kunden som avtalt.  

## Neste trinn

 Denne gjennomgangen har ledet deg gjennom noen av de grunnleggende trinnene for å arbeide med prosjekter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du har lært om hvordan du oppretter et nytt prosjekt, hvordan du kopierer et prosjekt og hvordan du håndterer betalinger. Du har også sett en demonstrasjon av hvordan du sporer timer og oppretter fakturaer.  

## Se også

 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
 [Konfigurer prosjektstyring](projects-setup-projects.md)  
 [Bruk ressurser](projects-how-use-resources.md)  
 [Overvåke fremdrift og prestasjon](projects-how-monitor-progress-performance.md)  
 [Fakturere prosjekter](projects-how-invoice-jobs.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
