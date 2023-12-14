---
title: Bruk timelister
description: Lær hvordan du oppretter timelister og sender dem til godkjenning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheets'
ms.search.form: '950, 951, 973'
ms.date: 07/27/2023
ms.service: dynamics365-business-central
ms.custom: bap-template
---
# <a name="use-time-sheets"></a>Bruk timelister

Bruk timelister til å spore fravær, og til å spore tid og ressurser som er brukt på et prosjekt. Sporing av tid hjelper deg med å identifisere problemer tidlig og unngå forsinkelser eller kostnadsoverskridelser. Timelister gjør det enkelt for en ressurs å rapportere tidsbruk for en enkeltperson eller en maskin, og at ledere kan se gjennom bruk og tilordning. Denne artikkelen beskriver hvordan du arbeider med timelister.  

Du kan kopiere og bruke prosjektplanleggingslinjer i en timeliste. Dermed trenger du bare å skrive inn informasjonen ett sted, og linjeinformasjonen er alltid riktig. Hvis du vil vite mer, går du til [Slik kopierer du prosjektplanleggingslinjer til en timeliste](#copy-job-planning-lines-to-a-time-sheet).

Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjekt- eller ressurskladden. Hvis du vil ha mer informasjon, kan du gå til [Slik bokfører du timelistelinjer i en prosjektkladd](#to-post-time-sheet-lines-in-a-job-journal) og [Slik bokfører du timelistelinjer i en ressurskladd](#post-time-sheet-lines-in-a-resource-journal).

Før du kan bruke timelister, må du definere generell informasjon og angi administrator og én eller flere godkjennere av timelister. Hvis du vil ha mer informasjon om hvordan du definerer timelister, går du til [Definer timelister](projects-how-setup-time-sheets.md).  

> [!TIP]
> Du kan bruke timelister på en mobil enhet. For å gjøre dette må du kanskje aktivere veksleknappen **Bruk ny timelistefunksjon** på siden [Ressursoppsett](https://businesscentral.dynamics.com/?page=462) .

## <a name="create-time-sheets"></a>Opprette timelister

Du kan bruke siden **Opprett timelister** til å angi timelister for et angitt antall tidsperioder eller uker. Deretter kan eieren av timelisten åpne den og registrere tid som er brukt på en aktivitet. Du kan også [planlegge kjørselen til å kjøres autoamtisk](ui-work-report.md#ScheduleReport).  

> [!IMPORTANT]
> Du må ha tillatelser for å kunne opprette timelister. Hvis du vil ha mer informasjon om tillatelser, går du til [Definere timelister](projects-how-setup-time-sheets.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Opprett timelister**, og velg deretter den relaterte koblingen.

    > [!TIP]
    > Du kan også bruke handlingen **Opprett timelister** på listesidene **Ressurser** og **Ressurskort**.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Før du oppretter timelister for en ressurs, må du kontrollere at feltene **Bruk timeliste** og **Bruker-ID for eier av timeliste** er angitt for dem på **Ressurskort**-siden.

    Hvis du vil, kan du velge handlingen **Planlegg** for å angi hvor ofte oppgaven skal kjøres automatisk. Hvis du for eksempel vil konfigurere at oppgaven kjøres ukentlig i fire uker, angir du feltet **Datoformel for neste kjøring** til **4U** på siden **Planlegg en rapport – opprett timelister**. Hvis du vil lære mer om planlegging av rapporter, går du til [Planlegging av en rapport som skal kjøres](ui-work-report.md#ScheduleReport).  

Du kan vise timelistene som du har opprettet, på siden **Timelister**. Hver time liste består av én eller flere linjer som definerer tiden du vil sende til godkjenning. Tabellen nedenfor beskriver hvilke typer av linjer du kan legge til i timelisten.

| **Felt** | **Beskrivelse** |
|---|---|
| | Brukes til å legge til en merknad eller et merke i **Beskrivelse**-feltet for timelistelinjen. Du kan for eksempel bruke dette feltet til å kategorisere timelisteposter. Hvis du lar **Type**-feltet være tomt for en timelistelinje, kan du ikke kan angi tidsverdier i ukedagfeltene for denne linjen. |
| Fravær | Brukes til å registrere fraværstiden i løpet av en arbeidsuke. Hvis du vil fylle ut informasjonen for linjen, kan du angi typen fravær i **Fraværsårsakskode**-feltet. |
| Monteringsordre | Brukes til å registrere tid for monteringsordrer. En timelistelinje av denne typen opprettes under bokføring av monteringsordrelinjene som ressursen er konfigurert til å bruke timelister for. Du kan ikke velge en linje av denne typen manuelt. |
| Jobb | Brukes til å registrere tidsforbruk for et prosjekt. Hvis du vil fullføre informasjonen for linjen, angir du prosjektnummeret og prosjektoppgavenummeret som du vil registrere tid for. Du kan registrere tiden for linjer som du ikke har planlagt.|
| Ressurs | Brukes til å registrere tidsforbruk for en ressurs. Hvis du vil fylle ut informasjonen for linjen, gir du en beskrivelse av arbeidet. |
| Tjeneste | Brukes til å registrere tidsforbruk for en serviceordre eller servicekreditnota. |

Du kan for eksempel sende inn en timeliste for en uke der du utførte rengjøringsoppgaver og hadde en fridag for en legetime. Tabellen nedenfor viser hvordan du legger til linjer i timelisten.

| Type | Description | Arbeidstypekode | Fraværstypekode |
|--|--|--|--|
| Ressurs | Arbeidstimer | Rengjøring |  |
| Fravær | Fritid |  | Tilstand |
|  | Jeg måtte ha fri tirsdag på grunn av en legetime. |  |  |

I dette hypotetiske eksemplet ville du da registrere de aktuelle timene i løpet av de aktuelle dagene, i feltene for hver enkelt ukedag.  

> [!TIP]
> I de fleste tilfeller vil selskapet ha forhåndsdefinerte arbeidstyper for de ulike linjetypene. I slike tilfeller velger du relevant arbeidstype fra oversikten, og deretter legger du til din egen beskrivelse.  
>
> Velg arbeidstype ved å velge knappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i feltet **Beskrivelse** ved å velge **Aktivitetsdetaljer** og deretter angi den på siden som åpnes, eller ved å velge den i henholdsvis feltet **Arbeidstypekode** eller **Fraværstypekode**. I dette tilfellet kan du ignorere delen [Slik definerer du arbeidstyper og legger til en til en timeliste](#define-work-types-and-add-one-to-a-time-sheet).  

## <a name="reuse-time-sheet-lines-in-other-time-sheets"></a>Bruke timelistelinjer på nytt i andre timelister

Hvis timelisteinformasjon er den samme fra tidsperiode til tidsperiode, kan du spare tid ved å kopiere linjene fra forrige tidsperiode. Deretter angir du bare tidsbruken for den nye perioden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Åpne timelisten for en periode som er senere enn perioden for en eksisterende timeliste med linjer.  
3. Velg handlingen **Kopier linjer fra tidligere timeliste**.

Linjene kopieres, inkludert detaljer som type og beskrivelse. Hvis linjen for eksempel er knyttet til et prosjekt, blir **Prosjektnr.** kopiert. Alle kopierte linjer har statusen **Åpen**. Du kan nå endre linjene etter behov.

## <a name="copy-job-planning-lines-to-a-time-sheet"></a>Kopiere prosjektplanleggingslinjer til en timeliste

Fremgangsmåten nedenfor beskriver hvordan du raskt legger til prosjektplanleggingslinjer i en timeliste.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Velg en timeliste for den relevante tidsperioden på siden **Timelister**.  
3. Velg handlingen **Opprett linjer fra prosjektplanlegging**. Alle typer prosjektplanleggingslinjer i timelisteperioden kopieres til timelisten for personen eller maskinen i feltet **Ressursnr.** i timelisten.

## <a name="define-work-types-and-add-one-to-a-time-sheet"></a>Definere arbeidstyper og legger til en til en timeliste

Du kan definere arbeidstypen for alle timelistelinjer for serviceordrer, prosjektordrer og ressurser. På denne måten kan du legge til informasjon du trenger for å kunne fakturere kunden for ulike typer arbeid.  

1. På siden **Timelister** velger du du den relevante timeliste.
2. På den første linjen i delen **Linjer** velger du feltet **Type**, og deretter velger du den aktuelle typen, for eksempel *Ressurs*.  
3. Velg **Beskrivelse**-feltet, og fyll deretter ut feltene på siden **Ressursdetalj for timelistelinje**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
    1. Hvis det ikke finnes noen arbeidstyper, velger du handlingen **Ny**.
    2. På siden **Arbeidstyper** fyller du ut feltene etter behov, og deretter returnerer du til timelisten.
4. Fyll ut de gjenværende timelistene. Hvis du vil ha mer informasjon, kan du se delen [Slik fyller du ut timelistelinjer og sender til godkjenning](#fill-in-time-sheet-lines-and-submit-for-approval).  

> [!TIP]
> Lignende trinn gjelder når du skal definere fraværskoder.

## <a name="fill-in-time-sheet-lines-and-submit-for-approval"></a>Fylle ut timelistelinjer og sende til godkjenning

Timelisteregistrering spores i timer, som er standard lagerenhet for ressurser. Som standard viser en timeliste vanlige arbeidsdager fra mandag til fredag.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Velg en timeliste for den aktuelle perioden.
3. Fyll ut feltene på en linje etter behov. Angi antall timer som brukes av ressursen for hver dag i uken.  

    I de fleste tilfeller kan du spore arbeid ved å legge til en linje av typen *Ressurs*, og deretter registrerer du timer som er brukt hver dag. Hvis du vil registrere fravær, legger du til en linje av typen *Fravær*.  

    > [!TIP]  
    > Du kan se gjennom summen av timelistetimer som du har angitt i faktaboksen **Faktisk/budsjettert sammendrag**.  
4. Gjenta trinn 3 for arbeidstypene som utføres av ressursen.  

    Deretter bestemmer du om du vil sende inn alle, eller valgte, linjer i timelisten.  

    * Hvis du vil sende timelisten til én eller flere linjer, velger du den relevante linjen og deretter **Send**-handlingen.

        Velg alternativet **Bare valgte linjer**. Linjestatusen endres fra **Åpen** til **Sendt**.
    * Hvis du vil sende tim listen for alle åpne linjer, velger du **Send**-handlingen øverst på **Timeliste**-siden.  

        Bekreft at du vil sende alle åpne linjer i gjeldende timeliste.  

    > [!NOTE]  
    > Du kan bare sende timelistelinjer du har angitt tid for.  
5. Hvis du vil endre informasjon på en linje som er satt til **Sendt**, merker du linjen og velger deretter handlingen **Åpne på nytt**.

    > [!NOTE]  
    > En leder kan avvise en timelistelinje som er sendt til godkjenning. Hvis en linje har statusen **Avvist**, kan du gjøre endringer på linjen og deretter velge **Send** på nytt.  
6. Velg **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Slik godkjenner eller avviser du timelister:

En timeliste må sendes inn til godkjenning før den kan brukes. Du kan godkjenne og avvise individuelle linjer på en timeliste eller sende dem tilbake til avsenderen. En timeliste kan godkjennes på to måter:

* En timelisteadministrator kan godkjenne en hvilken som helst timeliste.
* Personen som er angitt i feltet **Bruker-ID for godkjenner av timeliste** på et ressurskort, kan godkjenne timelister for denne ressursen. Hvis du vil ha mer informasjon om hvordan du definerer godkjenning, går du til [Definer timelister](projects-how-setup-time-sheets.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Administrer timelister**, og velg deretter den relaterte koblingen.
2. Velg en timeliste fra listen.  
3. På siden **Timeliste**: 
    1. Velg handlingen **Behandle**, og velg deretter **Godkjenn**-handlingen.
    2. Velg handlingen **Alle sendte linjer** for å godkjenne alle linjer eller **Bare valgte linjer** for å godkjenne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**.  
5. Du kan også velge handlingen **Avvis** og følge trinn 4 til 5.  

> [!TIP]  
> Bruk faktaboksene **Timelistestatus** og **Faktisk/budsjettert sammendrag** til å få oversikt over timelisteinformasjon.

Når du har godkjent eller avvist en timeliste, kan den ikke endres uten at den åpnes på nytt først. Følgende fremgangsmåte forklarer hvordan du åpner en godkjent eller avvist timeliste på nytt.

## <a name="reopen-a-time-sheet"></a>Åpne en timeliste på nytt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Administrer timelister** eller **Timelister**, og velg deretter den relaterte koblingen.
2. Åpne en timeliste fra listen.  

    > [!NOTE]  
    > Bare linjer som har statusen **Godkjent**, kan åpnes på nytt. Linjer som har statusen **Avvist** eller er bokført, kan ikke åpnes på nytt.  
3. På siden **Timeliste** velger du handlingen **Åpne på nytt**, og deretter velger du handlingen **Alle sendte linjer** for å åpne alle linjer på nytt, eller handlingen **Bare valgte linjer** for å åpne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**. Statusen for timelistelinjen eller -linjene endres til **Sendt**.  

## <a name="view-and-approve-time-sheets-by-job"></a>Vise og godkjenne timelister etter prosjekt

På et prosjekt kan du angi en person som er ansvarlig for prosjektet. Denne informasjonen er koblet til timeregistreringslinjer. Koblingen gir prosjektledere en liste over timelistene som skal godkjennes. Prosjektlederen for en prosjektgruppe kan for eksempel ha ansvaret for bestemte prosjekter i selskapet. I dette tilfellet bør lederen velges som **Ansvarlig person** på prosjektkortsiden. I denne visningen av timelisteinformasjon kan du se prosjektoppgaver som er knyttet til et prosjekt, og antall timer som er brukt.

> [!NOTE]
> For å kunne godkjenne timelister på siden **Timeliste for leder etter prosjekt** må du først velge et alternativ for **Timeliste etter jobbgodkjenning** på siden **Ressursoppsett**. Hvis du vil ha mer informasjon om hvordan du definerer godkjenninger for ressurser, går du til [Definere ressurser](projects-how-setup-resources.md).

### <a name="approve-or-reject-a-time-sheet-by-job"></a>Slik godkjenner eller avviser du timelister etter prosjekt

1. Skriv inn **Timeliste for leder etter prosjekt** i **Søk**-boksen, og velg deretter den relaterte koblingen. [!INCLUDE[prod_short](includes/prod_short.md)] viser en liste over timelistelinjer som er knyttet til prosjektene du har ansvar for.
2. Velg handlingen **Godkjenn**, og velg deretter handlingen **Alle sendte linjer** for å godkjenne alle linjer, eller handlingen **Bare valgte linjer** for å godkjenne bare linjene som er valgt på siden **Timeliste**.

    > [!NOTE]
    > Du kan bare godkjenne timelister som har statusen **Sendt**.

3. Hvis du vil gi mer informasjon om godkjenningen eller avvisningen, velger du **Relatert**-handlingen, velger **Merknader** og deretter **Linjemerknader**.
4. Velg **OK**-knappen.

> [!NOTE]
> Når du har godkjent eller avvist en timelistelinje etter prosjekt, kan den ikke åpnes på nytt eller endres i vinduet **Timeliste**.

## <a name="post-time-sheet-lines-in-a-resource-journal"></a>Slik bokfører du timelistelinjer i en ressurskladd

Når du har godkjent timelisteoppføringer for en ressurs, kan du bokføre dem til den relevante ressurskladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurskladder** og velg den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. På siden **Foreslå ressurskladdelinjer** fyller du ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velg **OK**-knappen. Det opprettes poster for bruk i ressurskladden, der du kan endre informasjonen etter behov.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Ressursposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="post-time-sheet-lines-in-a-job-journal"></a>Slik bokfører du timelistelinjer i en prosjektkladd

Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjektkladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. På siden **Foreslå prosjektkladdelinjer** fyller du ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 
4. Velg **OK**-knappen. Det opprettes poster for bruk i prosjektkladden, der du kan endre informasjonen etter behov.  

    > [!NOTE]  
    > Informasjon om arbeidstypen og om arbeidet er belastbart, kopieres fra timelistelinjen. Du kan om nødvendig redusere antall timer og foreta en delvis bokføring. Hvis du reduserer antallet, inneholder linjen som opprettes, gjenstående timeantall neste gang du velger handlingen **Foreslå linjer fra timelister**.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Prosjektposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="to-archive-time-sheets"></a>Slik arkiverer du timelister:

Når du har bokført timelister, kan du arkivere dem for fremtidig referanse. Du må bokføre alle linjene i en timeliste før du kan arkivere den.

> [!NOTE]  
> Når du arkiverer en timeliste, fjernes den fra listene på siden **Timelister** og **Timelister for leder**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Flytt timelister til arkiv**.  
3. På siden **Flytt timelister til arkiv** fyller du ut feltene etter behov, og deretter velger du **OK**-knappen.  
4. Hvis du vil gå gjennom arkiverte timelister, velger du ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Timelistearkiver** eller **Administrer timelistearkiver**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også

[Prosjektstyring](projects-manage-projects.md)  
[Konfigurer prosjektstyring](projects-setup-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
