---
title: Gjennomgang – Administrere prosjekter med underordnede prosjekter | Microsoft-dokumentasjon
description: I denne gjennomgangen får du en innføring i prosjektstyringsfunksjoner i prosjekter. Prosjeker brukes til å estimere forbruket av selskapets ressurser og til å holde rede på de ulike kostbeløpene som er knyttet til ressursene i et bestemt prosjekt. Prosjekter omfatter forbruk av ansattes arbeidstid, maskindriftstid, lagervarer og andre typer forbruk som det kan hende du vil spore etter som et prosjekt går fremover.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 05f45c0c7041771a63dc7b7c7a6b61512d67af2a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760070"
---
# <a name="walkthrough-managing-projects-with-jobs"></a>Gjennomgang: prosjektstyring

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

I denne gjennomgangen får du en innføring i prosjektstyringsfunksjoner i prosjekter. Prosjeker brukes til å estimere forbruket av selskapets ressurser og til å holde rede på de ulike kostbeløpene som er knyttet til ressursene i et bestemt prosjekt. Prosjekter omfatter forbruk av ansattes arbeidstid, maskindriftstid, lagervarer og andre typer forbruk som det kan hende du vil spore etter som et prosjekt går fremover.  

 Denne gjennomgangen tar for seg oppsett av et nytt prosjekt i tillegg til noen vanlige oppgaver, for eksempel håndtering av faste priser, betaling i avdrag, bokføring av fakturaer fra prosjekter og kopiering av prosjekter.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
 Denne gjennomgangen viser følgende oppgaver:  

### <a name="setting-up-a-job"></a>Konfigurere et prosjekt  
 Opprettelse av et prosjekt blir enkelt når du har definert budsjettstrukturen for prosjekter. Denne gjennomgangen omhandler følgende prosedyrer:  

-   Opprette prosjektoppgavelinjer og planleggingslinjer.  
-   Opprette prosjektspesifikke priser for varer, ressurser og finanskonti.  
-   Fakturering fra et prosjekt  

### <a name="handling-fixed-prices"></a>Håndtere faste priser  
 I prosjektmodulen kan du håndtere faste priser og priser på tjenester og varer som er avtalt med kunder på forhånd. I denne gjennomgangen kan du gjøre følgende:  

-   Vise hvordan kontraktverdier og fakturaverdier fastsettes.  
-   Tillate ekstra arbeid i estimatet som ikke er fakturert.  

### <a name="copying-a-job"></a>Kopiere et prosjekt  
 Denne delen av gjennomgangen fokuserer på hvordan du kopierer deler av et prosjekt eller hele prosjektet for å redusere manuell registrering av data og forbedre korrektheten. Det inkluderer følgende:  

-   Kopiering av deler av et prosjekt til et nytt prosjekt  
-   Kopiering av prosjektspesifikke priser  
-   Kopiering av planleggingslinjer  

### <a name="making-payment-by-installment"></a>Foreta betaling i avdrag  
 Når et stort, kostbart prosjekt varer lenge, gjør kunden ofte en avtale med selskapet om å betale i avdrag. Dette scenariet viser hvordan du definerer betaling i avdrag, og tar for seg følgende:  

-   Opprette betaling i avdrag for et prosjekt.  
-   Fakturering av kunder  
-   Redegjørelse for bruk i et prosjekt konfigurert for betaling i avdrag.  

## <a name="roles"></a>Roller  
 Denne gjennomgangen omfatter oppgaver for følgende roller:  

-   Prosjektleder  
-   Medlem i prosjektgruppen  

## <a name="prerequisites"></a>Forutsetninger  
 Før du kan utføre oppgavene i gjennomgangen, må du gjøre følgende:  

-   Installer demodatabasen CRONUS Norge AS.
-   Opprett eksempeldata ved å bruke fremgangsmåten i neste del.  

## <a name="story"></a>Hovedscenario  
Denne gjennomgangen fokuserer på CRONUS Norge AS, et design- og konsulentfirma som designer og innreder nye infrastrukturer, for eksempel konferanserom og kontorer, med møbler, tilbehør og reoler. Mesteparten av arbeidet er prosjektorientert. Florian er en prosjektleder hos CRONUS. Han bruker prosjekter til å få en oversikt over alle pågående prosjekter som CRONUS har startet, samt ferdige prosjekter. Han er den som vanligvis utarbeider avtaler med kunder og registrerer kjernen av prosjektet, som er oppgave- og planleggingslinjer samt priser, i [!INCLUDE[prod_short](includes/prod_short.md)]. Han synes det er enkelt å opprette, vedlikeholde og gå gjennom informasjon. Florian liker også hvordan [!INCLUDE[prod_short](includes/prod_short.md)] gjør det mulig å kopiere prosjekter og betale i avdrag.

 Marie, som er medlem i prosjektgruppen og rapporterer til Florian, har ansvaret for den daglige overvåkingen av prosjektet. Hun angir sitt eget arbeid i tillegg til arbeidet som utføres av teknikerne på hver oppgave. Hun registrerer varene som de har brukt og de påløpte kostnadene.  

## <a name="preparing-sample-data"></a>Klargjøre eksempeldata  
 Hvis du vil forberede denne gjennomgangen, må du legge til Tricia som en ny ressurs.  

### <a name="to-prepare-the-sample-data"></a>Slik klargjør du eksempeldataene:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny**-handlingen for å opprette et nytt ressurskort.  
3.  Skriv inn følgende informasjon på hurtigfanen **Generelt**:  

    - **Nr.**: **Marie**  
    - **Navn**: **Marie**  
    - **Skriv inn**: **person**  

4.  Velg feltet **Lagerenhet**, og velg **Ny**-handlingen for å åpne siden **Ressursenhet**. Velg **Time** i **Kode**-feltet.  
5.  Skriv inn følgende informasjon på hurtigfanen **Fakturering**:  

    -   **Direkte enhetskost**: **5**  
    -   **Indirekte kost-%**: **4**  
    -   **Enhetskost**: **10**  
    -   **Bokføringsgruppe - vare**: **Service**  
    -   **Mva-bokføringsgruppe – vare**: **mva 25**  

6. Lukk siden.

I neste fremgangsmåte kan du opprette en prosjektkladd for Marie for å bokføre forbruket hennes.  

### <a name="to-create-a-job-journal-batch"></a>Slik oppretter du en prosjektkladd  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2.  Velg **Bunkenavn**-feltet på **Prosjektkladd**-siden. Siden **Prosjektkladder** åpnes.  
3.  Velg **Ny**-handlingen for å opprette en ny linje med følgende informasjon:  

    -   **Navn**: **Marie**  
    -   **Beskrivelse**: **Marie**  
    -   **Nr.serie**: **PKLD-GEN**  

4.  Velg **OK**-knappen for å lagre endringene.

## <a name="setting-up-a-job"></a>Konfigurere et prosjekt  
 I dette scenariet har CRONUS fått i oppdrag av en kunde, Progressive Home Furnishings, å designe et konferanserom og en spisesal. Kunden er basert i USA, og prosjektet krever spesialprogramvare. Prosjektlederen inngår en avtale med kunden og oppretter et prosjekt som er i tråd med avtalen.  

### <a name="to-set-up-a-job"></a>Slik konfigurerer du et prosjekt:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny**-handlingen for å opprette et nytt kort.  
3.  Skriv inn følgende informasjon på hurtigfanen **Generelt**:  

    -   **Beskrivelse**: **Rådgivning om oppsett av konferanserom**  
    -   **Faktura til-kundenr.**: **01445544**  

4.  Skriv inn følgende informasjon på hurtigfanen **Bokføring**:  

    -   **Status**: **Planlegging**  
    -   **Bokføringsgruppe - prosjekt**: **Definere**  
    -   **VIA-metode**: **Kostverdi**  

5.  Skriv inn dagens dato i feltene **Sluttdato** og **Startdato** på hurtigfanen **Varighet**. Disse datoene er til hjelp ved valutaomregning når prosjektet faktureres.  
6.  På hurtigfanen **Utenrikshandel** setter du valutakoden til **USD**. Hvis du velger USD i feltet **Valutakode for faktura**, faktureres prosjektet i amerikanske dollar og planlegges bare i den lokale valutaen til CRONUS.  

 Du kan tilpasse prissettingen for kunder per prosjekt, avhengig av avtalene du har definert. I neste fremgangsmåte angir prosjektlederen en kostpris for Maries tid, angir pris for programvaren som kreves, og legger til i reisekostnadene at kunden har godtatt å betale.  

### <a name="to-customize-pricing"></a>Slik tilpasser du prising:  

1.  Velg **Ressurs**-handlingen på prosjektkortet.  
2.  Skriv inn følgende informasjon på siden **Ressurspriser for prosjekt**:  

    -   **Kode**: **Marie**  
    -   **Enhetspris**: **20**  

3.  Lukk siden.  
4.  Velg handlingen **Vare**.  
5.  Angi følgende informasjon og tilpasset pris på siden **Varepriser for prosjekt**:  

    1.  **Varenr.**: **80201 (Grafikkprogram)**  
    2.  **Enhetspris**: **200**  

6.  Lukk siden.  
7.  Velg **Finanskonto**-handlingen.  
8.  På siden **Finanskontopriser for prosjekt** skriver du inn følgende informasjon og reisekostnadene, som kunden har godtatt å betale kost pluss 25 prosent for:  

    1.  **Finanskonto**: **8430 (Reise)**  
    2.  **Enhetskostfaktor**: **1,25**  

9. Lukk siden.  

 De siste trinnene for konfigurasjon av et prosjekt er å legge til prosjektoppgavene og planleggingslinjene som inngår i hver oppgave. Planleggingslinjene fastsetter hva som faktureres til kunden.  

### <a name="to-add-job-tasks"></a>Slik legger du til prosjektoppgaver:  

1.  På **Prosjekt**-kortet for det nye prosjektet velger du **Prosjektoppgavelinjer**-handlingen.  
2.  Tabellen nedenfor beskriver informasjonen som du bør angi i feltene.  

    |Prosjektoppgavenr.|Beskrivelse|Prosjektoppgavetype|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Konsultasjon om oppsett av rom|Fra-sum|  
    |1010|Konsultasjonsmøte med kunden|Konto|  
    |1020|Utvikling|Konto|  
    |1090|Konsultasjon totalt|Til-sum|  

3.  Hvis du vil vise at noen oppgaver er underkategorier av andre oppgaver, velger du handlingen **Rykk inn prosjektoppgaver**.  

 En planleggingslinje kan være én av følgende typer:  

-   **Estimat**: lagt til i tidsplanen, men ikke fakturert.  
-   **Kontrakt**: fakturert, men ikke lagt til i tidsplanen.  
-   **Både Budsjett og Fakturerbar**: Faktureres og legges til i tidsplanen.  

 I denne gjennomgangen bruker prosjektlederen **Både Budsjett og Fakturerbar**. Han oppretter tre planleggingslinjer for oppgave 1010 og to planleggingslinjer for oppgave 1020.  

### <a name="to-create-planning-lines"></a>Slik oppretter du planleggingslinjer:  

1.  Velg linje 1010 og velg deretter handlingen **Prosjektplanleggingslinjer**. Angi følgende informasjon:  

     **Linje 1**  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Marie**  
    -   **Antall**: **40**  

     **Linje 2**  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Egil**  
    -   **Antall**: **40**  

     **Linje 3**  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Finanskonto**  
    -   **Nr.**: **8430 (reise)**  
    -   **Antall**: **2**  
    -   **Enhetskost**: **400**  

2.  Lukk siden. Totalene oppdateres på siden **Prosjektoppgavelinjer**.  
3.  Velg linje 1020 og velg deretter handlingen **Prosjektplanleggingslinjer**. Angi følgende informasjon:  

     **Linje 1**  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Marie**  
    -   **Antall**: **80**  

     **Linje 2**  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Vare**  
    -   **Nr.**: **80201 (grafikkprogram)**  
    -   **Antall**: **1**  

4.  Lukk siden. Totalene oppdateres på siden **Prosjektoppgavelinjer**.  

## <a name="calculating-remaining-usage"></a>Beregne gjenstående forbruk  
 Marie, medlemmet i prosjektgruppen, har arbeidet på prosjektet en stund og vil registrere timene og forbruket på prosjektet. Hun har ikke arbeidet flere timer enn det som ble avtalt med kunden på forhånd. Hun bruker kjørselen **Beregn gjenstående forbruk** til å beregne gjenstående forbruk for prosjektet i en prosjektkladd. For hver oppgave beregner kjørselen differansen mellom planlagt forbruk av varer, ressurser og finansutgifter og det faktiske forbruket som er bokført i prosjektposter. Det gjenstående forbruket vises deretter i prosjektkladden, som hun kan bokføre det fra.  

### <a name="to-calculate-remaining-usage"></a>Slik beregner du gjenstående forbruk:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2.  Åpne oversikten **Prosjektkladd** i **Bunkenavn**-feltet på siden **Prosjektkladd**. Velg prosjektkladden **Marie**.  
3.  Velg handlingen **Beregn gjenstående forbruk**.  
4.  Velg **Prosjektnr.**-feltet på hurtigfanen **Prosjektoppgave** på siden **Beregn gjenstående forbruk for prosjekt**, og velg det aktuelle prosjektnummeret, for eksempel J00010.  
5.  Skriv inn **J00001** i feltet **Bilagsnr.** på hurtigfanen **Alternativer**. Dette gjør det enklere å spore bokføringen senere.  
6.  Angi dagens dato som bokføringsdato.  
7.  Velg **OK**-knappen. Dermed genereres prosjektkladdelinjer som hentes fra planleggingslinjene som Florian opprettet for prosjektet.  
8.  Velg **OK**-knappen på bekreftelsessiden. De genererte linjene legges til i prosjektkladden.  
9. Kontroller at alle bilagsnumrene er J00001, og velg deretter **Bokfør**-handlingen. Velg **Ja** for å bekrefte bokføringen.  

Linjene er nå bokført.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Opprette og bokføre en salgsfaktura for prosjekt  
 Marie kan deretter opprette en ny faktura for hele prosjektet eller for deler av et prosjekt. Hun kan også knytte fakturaen til en annen faktura for samme kunde og samme prosjekt. I dette tilfellet fakturerer hun for hele prosjektet siden det nå er fullført.  

### <a name="to-create-a-job-sales-invoice"></a>Slik oppretter du en salgsfaktura for prosjekt:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg prosjektet du opprettet tidligere, og velg handlingen **Opprett salgsfaktura for prosjekt**.  
3.  På hurtigfanen **Prosjektoppgave** tømmer du eventuelle filtre på **Prosjektoppgavenr.** for å fakturere prosjektet. Velg det aktuelle prosjektet i **Prosjektnr.**-feltet.  
4.  Fyll ut bokføringsdatoen og definer om du vil opprette én faktura per oppgave eller én enkelt faktura for alle oppgaver, på hurtigfanen **Alternativer**.  
5.  Velg **OK**-knappen for å opprette fakturaen, og velg deretter **OK**-knappen på bekreftelsessiden.  

 Etter at Marie har opprettet fakturaen, kan hun f.eks. få tilgang til den fra rollesenteret **Ordrebehandler**. 

### <a name="to-post-a-new-sales-invoice"></a>Slik bokfører du en ny salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2.  Åpne fakturaen for kundenr. 01445544. Nå kan du se informasjonen som ble registrert på planleggingslinjene.  
3.  Velg handlingen **Bokfør**. Velg **Ja** for å bekrefte bokføringen.  

### <a name="to-view-the-posted-invoice"></a>Slik viser du den bokførte fakturaen:  

1.  Åpne prosjektet, og velg deretter handlingen **Prosjektplanleggingslinjer**.  
2.  Velg en planleggingslinje som er fakturert, og velg deretter handlingen **Salgsfaktura/kreditnota**.
3. På siden **Prosjektfakturaer** velger du handlingen **Åpen salgsfaktura/kreditnota**.  

 Marie har spørsmål om prisene, kostbeløpene og fortjenesten som er relevant for dette bestemte prosjektet, og derfor går hun til denne informasjonen via **Statistikk**-siden.  

### <a name="to-open-the-statistics-page"></a>For å åpne statistikksiden  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Statistikk**. Du kan se gjennom detaljert informasjon om prosjektprisene, kostbeløpene og fortjenesten i både lokal og utenlandsk valuta.  
3.  Velg **Lukk**-knappen for å lukke siden **Prosjektstatistikk**.  

## <a name="handling-fixed-prices"></a>Håndtere faste priser  
 CRONUS har fått i oppdrag å sette opp konferanserom. Som prosjektleder trenger Prakash en god oversikt over oppgavene som kreves i prosjektet, sammen med de tilknyttede budsjetterte og påløpte kostbeløpene for hver oppgave. I tillegg vil han vite salgsbeløpet for prosjektet og beløpet som er fakturert hittil. Han har inngått en avtale med kunden når det gjelder fast pris for prosjektet.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Slik håndterer du faste priser i prosjekter  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg **Tremøbler AS**-prosjektnummeret og velg deretter **Prosjektoppgavelinjer**-handlingen.  
3.  Velg linje 1120, og høyreklikk beløpet i feltet **Estimat (kostbeløp)** og velg **Drilldown**.  

     Ved å gå gjennom planleggingslisten for prosjekt finner Florian ut at han også trenger Marie i 30 timer på dette trinnet i prosjektet. Han avtaler en fast pris med kunden.  

4.  På siden **Prosjektoppgavelinjer** velger du linje 1120, og deretter velger du handlingen **Prosjektplanleggingslinjer**.  
5.  Velg **Ny** for å opprette en ny linje med følgende informasjon:  

    -   **Linjetype**: **Både Budsjett og Fakturerbar**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Marie**  
    -   **Antall**: **30**  

7.  Lukk siden.  
8.  Høyreklikk feltet **Estimat (kostbeløp)**, og velg **Drilldown** på nytt på siden **Prosjektoppgavelinjer**. Vis endringene av estimatet. Du ser at de 30 timene er lagt til i estimatet.  
9. Lukk sidene.  

Etter at Marie er lagt til i estimatet for denne oppgavelinjen, arbeider hun 25 timer på prosjektet. Hun registrerer disse timene i prosjektkladden.  

### <a name="to-enter-hours-in-the-job-journal"></a>Slik angir du timer i prosjektkladden:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2.  Skriv inn følgende informasjon på en ny linje:  

    -   **Linjetype**: **(tom)**  
    -   **Bokføringsdato**: **(dagens dato)**  
    -   **Bilagsnr.**: **J00002**  
    -   **Prosjektnr.**: **Tremøbler AS**  
    -   **Prosjektoppgavenr.**: **1120**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Marie**  
    -   **Antall**: **25**  

3.  Velg handlingen **Bokfør**.  

     Noen få dager senere arbeider Marie 10 timer til på prosjektet. Hun har nå arbeidet 35 timer i alt. Siden avtalen gjelder for 30 timer med kunden, blir kunden bare belastet for 5 av disse timene. Marie legger til de ekstra fem timene hun arbeidet, manuelt i timeplanen.  

4.  Velg handlingen **Beregn gjenstående forbruk** på siden **Prosjektkladd**.  
5.  Angi følgende informasjon på hurtigfanen **Alternativer** på siden **Beregn gjenstående forbruk for prosjekt**:  

    -   **Bilagsnr.**: **J00003**  
    -   **Bokføringsdato**: **(dagens dato)**  

6.  På hurtigfanen **Prosjektoppgave** angir du følgende informasjon:  

    -   **Prosjektnr.**: **Tremøbler AS**  
    -   **Prosjektoppgavenr.**: **1120**  

7. Velg **OK**-knappen for å kjøre beregningen.

    Det gjenstår fem timers arbeid for Marie. **Linjetype**-feltet er tomt, noe som betyr at det bare er forbruket som gjenstår å bli bokført, siden arbeidet allerede er planlagt.  

8.  Opprett en ny linje med følgende informasjon i **Prosjektkladd**-vinduet: Kontroller at begge prosjektnumrene er i fortløpende rekkefølge i forhold til de du allerede har brukt:  

    -   **Linjetype**: **Estimat**  
    -   **Prosjektnr.**: **Tremøbler AS**  
    -   **Prosjektoppgavenr.**: **1120**  
    -   **Type**: **Ressurs**  
    -   **Nr.**: **Marie**  
    -   **Antall**: **5**  

     Estimatkostbeløpene og estimatprisene oppdateres ved hjelp av **Estimat**-linjetypen uten å oppdatere kontraktkostbeløpene og kontraktprisene som er fakturert til kunden.  

9.  Velg handlingen **Bokfør**. Velg **OK**-knappen for å lukke siden.  
10. Åpne **Prosjekter**-listen.  
11. Velg prosjektet TREM., og velg deretter handlingen **Prosjektoppgavelinjer**.  
12. Merk linje 1120, og høyreklikk beløpet i feltet **Estimat (kostbeløp)**. Velg **Drilldown** for å vise informasjonen.  

     Endringer blir automatisk lagt inn på linjen for prosjektoppgavenr. 1120. Fem ekstra timer arbeid av Tricia er lagt til i totalkostnaden for planlagt arbeid i tidsplanen.  

13. Velg **Lukk**-knappen for å lukke siden.  
14. Høyreklikk beløpet i feltet **Kontrakt (kostbeløp)**, og velg **Drilldown** for å vise informasjonen.  

I kontraktens salgsbeløp er bare de opprinnelig avtalte 30 timene tatt med siden dette er det som ble avtalt med kunden.  

## <a name="copying-jobs"></a>Kopiere prosjekter  
 Florian har inngått en avtale med en kunde, Møbelhandleren A/S, om å foreta oppsett av 10 konferanserom. Avtalen ligner på en tidligere jobb. Du sparer derfor tid ved å kopiere den tidligere jobben.  

 På siden **Kopier prosjekt** kan du velge prosjektet og oppgavelinjene du vil kopiere. Du kan også kopiere kildeprosjektposter, som gjør at det blir opprettet planleggingslinjer basert på faktisk forbruk, eller du kan kopiere planleggingslinjer fra kildeprosjektet, slik at de opprinnelige planleggingslinjene blir kopiert til det nye prosjektet. Du kan deretter velge hvilken planleggingslinjetype eller postlinjetype du vil ha med, og velge bare den som er relevant for det nye prosjektet. Til slutt kan du velge prosjektet du vil kopiere til, og angi om priser og antall også skal kopieres.  

### <a name="to-copy-a-job"></a>Slik kopierer du et prosjekt:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny**-handlingen for å opprette et nytt prosjekt. Angi følgende informasjon:  

    -   **Beskrivelse**: **Oppsett av ti konferanserom**  
    -   **Faktura til-kundenr.**: **20000**  

3.  Velg handlingen **Kopier prosjektoppgaver fra**.  
4.  Angi følgende på siden **Kopier prosjektoppgaver**:  

    -   **Prosjektnr.**: **Tremøbler AS**  
    -   **Prosjektoppgavenr. fra**: **1000**  
    -   **Kilde**: **Prosjektplanleggingslinjer**  
    -   **Inkl. planleggingslinjetype**: **Estimat+kontrakt**  
    -   **Til prosjektnr.**: **Tremøbler AS Oppsett av ti konferanserom**  
    -   Velg feltene **Kopier dimensjoner** og **Kopier mengde**.  

5.  Velg **OK**-knappen for å kopiere prosjektet, og velg deretter **OK**-knappen for å lukke bekreftelsessiden.  

Ved å sammenligne priser, prosjektoppgavelinjer og prosjektplanleggingslinjer for de to prosjektene kan du se at informasjonen ble kopiert.  

## <a name="making-payments-by-installments"></a>Foreta betaling i avdrag  
 CRONUS har nettopp fått et stort prosjekt som kommer til å ta et år å fullføre. Siden mange ressurser må avsettes, setter prosjektlederen opp kontrakten slik at kunden betaler en del av prisen på forskudd, en del når prosjektet er halvveis fullført, og den siste delen når prosjektet er fullført.  

### <a name="to-set-up-a-new-account"></a>Slik konfigurerer du et nytt budsjett  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny**-handlingen på siden **Kontoplan** for å opprette et nytt kort.  
3.  Angi følgende informasjon på kortet **Ny finanskonto**:  

    -   **Nr.**: **6630**  
    -   **Navn**: **Prosjektbetaling**  

4.  På hurtigfanen **Bokføring** i feltet **Bokføringsgruppe - vare** velger du **DIV**. Lukk siden.  
5.  Velg **Nr. 6630 Prosjektbetaling** på siden **Kontoplan**, og velg deretter **Innrykk kontoplan**-handlingen. Velg **Ja** for å bekrefte.  

 Fremgangsmåtene nedenfor viser hvordan du oppretter en ny jobb, angir prissetting og deretter definerer betaling i avdrag. Du kan opprette spesifikke linjer som er reservert for betalingen i avdrag, på prosjektoppgavelinjene. Alt fullført arbeid på prosjektet som legges til estimatet, angis på forbrukslinjene. Linjetypen er Kontrakt for hver betalingsoppgavelinje på planleggingslinjene, som betyr at kunden blir fakturert. Angi en ny linje for avdraget. Du kan angi informasjonen for varene og ressursene som er brukt i dette prosjektet, på forbruksoppgavelinjen. Dermed økes estimatet, for eksempel ansattes arbeidstid og antallet varer som er brukt i prosjektet.  

### <a name="to-make-a-payment-by-installment"></a>Slik foretar du betaling i avdrag:  

1.  Opprett et nytt prosjekt.  
2.  Fyll inn følgende informasjon på det nye **Prosjekt**-kortet:  

    -   **Beskrivelse**: **Ny innredning av resepsjon**  
    -   **Faktura til-kundenr.**: **30000**  
    -   **Bokføringsgruppe - prosjekt**: **Definere**  
    -   **VIA-metode**: **Kostverdi**  

3.  Velg **Ressurs**-handlingen på prosjektkortet. Angi følgende informasjon:  

    -   **Kode**: **Marie**  
    -   **Enhetspris**: **10**  

     Lukk siden.  

4.  På **Prosjekt**-kortet velger du handlingen **Prosjektoppgavelinjer**.  

     Følgende tabell beskriver linjene du oppretter.  

    |Linje|Prosjektoppgavenr.|Beskrivelse|Prosjektoppgavetype|  
    |----------|------------------|---------------------------------------|-------------------|  
    |1|1000|Betalingsavdrag|Bokføring|  
    |2|2000|Bruk|Konto|  
    |3|3 000|Betaling - Halvveis|Bokføring|  
    |4|4000|Betaling - fullføring|Bokføring|  

5.  På siden **Prosjektoppgavelinjer** velger du oppgave 1000, og deretter velger du handlingen **Prosjektplanleggingslinjer**.  
6.  Opprett en planleggingslinje med følgende informasjon:  

    -   **Linjetype**: **Kontrakt**  
    -   **Planleggingsdato**: **(dagens dato)**  
    -   **Type**: **Finanskonto**  
    -   **Nr.**: **6630**  
    -   **Antall**: **1**  
    -   **Enhetspris**: **5000**  

     Lukk siden.  

7.  Velg **oppgave 2000** på siden **Prosjektoppgavelinjer**, og åpne **Prosjektplanleggingslinjer** for den.  

     Følgende tabell beskriver planleggingslinjene du oppretter.  

    |Linje|Linjetype|Planleggingsdato|Type|Nr.|Antall|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Estimat|(dagens dato)|Ressurs|Marie|120|  
    |2|Estimat|(dagens dato)|Vare|70104|10|  

     Lukk siden. På siden **Prosjektoppgavelinjer** kan du se at estimatbeløpene har blitt oppdatert.  

8.  På siden **Prosjektoppgavelinjer** velger du **oppgave 3000**.  
9. Opprett en planleggingslinje med følgende informasjon:  

    -   **Linjetype**: **Kontrakt**  
    -   **Planleggingsdato**: **en fremtidig dato**  
    -   **Type**: **Finanskonto**  
    -   **Nr.**: **6630**  
    -   **Antall**: **1**  
    -   **Enhetspris**: **5000**  

     Lukk siden.  

10. Opprett en lignende planleggingslinjepost for prosjektoppgave 4000.  

 Nå som oppgave- og planleggingslinjene er registrert, oppretter Florian en faktura for den første betalingen. Han gjør dette fra prosjektoppgavelinjene for å sikre at fakturaen bare inneholder linjene for den første betalingen. Du kan åpne ordren fra planleggingslinjene eller oppgavelinjene.  

### <a name="to-create-an-invoice"></a>Slik oppretter du en faktura:  

1.  På siden **Prosjektoppgavelinjer** velger du linje 1000, og deretter velger du handlingen **Opprett salgsfaktura**.  
2.  Angi dagens dato som bokføringsdato på siden **Opprett salgsfaktura**, angi **Per oppgave**, og klikk **OK** for å opprette en faktura med standardinformasjon. Velg **OK**-knappen for å lukke bekreftelsessiden.  
3.  Velg handlingen **Salgsfaktura/kreditnota**. I salgsfakturaen kan du se at det bare er avdraget som er tatt med i fakturaen. Du kan nå sende denne til kunden som avtalt.  

## <a name="next-steps"></a>Neste trinn  
 Denne gjennomgangen har vist deg noen av de grunnleggende trinnene for å arbeide med prosjekter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du har lært hvordan du oppretter et nytt prosjekt, hvordan du kopierer et prosjekt og hvordan du håndterer betalinger. Du har også sett en demonstrasjon av hvordan du sporer timer og oppretter fakturaer.  

## <a name="see-also"></a>Se også  
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)   
 [Konfigurere prosjektstyring](projects-setup-projects.md)   
 [Bruke ressurser](projects-how-use-resources.md)   
 [Overvåke fremdrift og prestasjon](projects-how-monitor-progress-performance.md)   
 [Fakturere prosjekter](projects-how-invoice-jobs.md)  
 [Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]