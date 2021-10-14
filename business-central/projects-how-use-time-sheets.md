---
title: Bruke timelister for prosjekter
description: Beskriver hvordan du oppretter en timeliste for et prosjekt, kopierer planleggingslinjer til den, definerer arbeidstyper, fyller ut timelisten og sender den inn til godkjenning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource, time sheets
ms.date: 08/24/2021
ms.author: edupont
ms.openlocfilehash: 3e29d1b745c27f7d6e5f0e8d9e444d70b2218b10
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588835"
---
# <a name="use-time-sheets-for-projects"></a>Bruke timelister for prosjekter

Du bruker kjørselen **Opprett timelister** til å angi timelister for et angitt antall tidsperioder eller uker. Du må ha tillatelser for å kunne opprette timelister.

Du kan kopiere og bruke prosjektplanleggingslinjer i en timeliste. Dermed trenger du bare å skrive inn informasjonen ett sted, og linjeinformasjonen er alltid riktig.

Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjekt- eller ressurskladden.

Før du kan bruke timelister, må du definere generell informasjon og angi administrator og én eller flere godkjennere av timelister. Hvis du vil ha mer informasjon, kan du se [Definere timelister](projects-how-setup-time-sheets.md).  

> [!TIP]
> Fra og med lanseringsbølge 2 for 2021 kan du administrere tildelte timelister på en mobil enhet. Det kan imidlertid hende at administratoren må aktivere funksjonen **Funksjonsoppdatering: ny timelistefunksjon** på siden [Funksjonsbehandling](https://businesscentral.dynamics.com/?page=2610) for å bruke denne funksjonen. Hvis du vil ha mer informasjon, kan du se [Definer timelister](projects-how-setup-time-sheets.md).

## <a name="to-create-time-sheets"></a>Slik oppretter du timelister

Du kan bruke kjørselen **Opprett timelister** til å angi timelister for et angitt antall tidsperioder eller uker. Deretter kan eieren av timelisten åpne den og registrere tid som er brukt på en aktivitet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.
2. På siden **Liste for timeliste** velger du handlingen **Opprett timelister**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Feltene **Bruk timeliste** og **Bruker-ID for eier av timeliste** må fylles ut på kortet for ressursen i timelisten.
4. Velg **OK**.  

Du kan vise timelistene som du har opprettet, på siden **Liste for timeliste**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Slik kopierer du prosjektplanleggingslinjer til en timeliste:
Fremgangsmåten nedenfor beskriver hvordan du raskt legger til prosjektplanleggingslinjer i en timeliste.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Velg en timeliste for den relevante tidsperioden på siden **Liste for timeliste**.  
3. Velg handlingen **Linje**, og velg deretter handlingen **Opprett linjer fra prosjektplanlegging**. Alle typer prosjektplanleggingslinjer i timelisteperioden kopieres til timelisten for personen eller maskinen i feltet **Ressursnr.** i timelisten.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Slik definerer du arbeidstyper og legger til en til en timeliste
Du kan definere arbeidstypen for alle linjer i timelister for prosjekter. På denne måten kan du legge til informasjon du trenger for å kunne fakturere kunden for ulike typer arbeid.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.   
2. Åpne den relevante timelisten.
3. Velg feltet **Beskrivelse**.  
4. På siden **Timelistelinje – prosjektdetaljer** velger du feltet **Arbeidstypekode** og velger en arbeidstype fra listen, for eksempel **Miles**.  
5. Hvis det ikke finnes noen arbeidstyper, velger du handlingen **Ny**.
6. På siden **Arbeidstyper** fyller du ut feltene etter behov.
7. Gjenta trinn 4 for å tilordne den nye arbeidstypen til timelisten.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Slik bruker du timelistelinjer på nytt i andre timelister
Hvis timelisteinformasjon er den samme fra tidsperiode til tidsperiode, kan du spare tid ved å kopiere linjene fra forrige tidsperiode. Deretter angir du bare tidsbruken for den nye perioden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Åpne timelisten for en periode som er senere enn perioden for en eksisterende timeliste med linjer.  
3. Velg handlingen **Linje**, og velg deretter handlingen **Kopier linjer fra forrige timeliste**.

Linjene kopieres, inkludert detaljer som type og beskrivelse. Hvis linjen for eksempel er knyttet til et prosjekt, blir **Prosjektnr.** kopiert. Alle kopierte linjer har statusen **Åpen**. Du kan nå endre linjene etter behov.

## <a name="to-fill-in-time-sheet-lines-and-submit-for-approval"></a>Slik fyller du ut timelistelinjer og sender til godkjenning
Timelisteregistrering spores i timer, som er standard lagerenhet for ressurser. Som standard viser en timeliste vanlige arbeidsdager fra mandag til fredag.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Velg en timeliste for den aktuelle perioden.
3. Fyll ut feltene på en linje etter behov. Angi antall timer som brukes av ressursen for hver dag i uken.  

    > [!TIP]  
    >   Du kan se gjennom summen av timelistetimer som du har angitt i faktaboksen **Faktisk/budsjettert sammendrag**.  
4. Gjenta trinn 3 for arbeidstypene som utføres av ressursen.
5. Velg handlingen **Behandle**, og velg deretter handlingen **Send** og **Alle åpne linjer** for å sende alle linjer, eller handlingen **Bare valgte linjer** for å sende bare linjene som er valgt på siden **Timeliste**.  

    > [!NOTE]  
    >   Du kan bare sende timelistelinjer du har angitt tid for.  
6. Hvis du vil endre informasjon på en linje som er satt til **Sendt**, merker du linjen og velger deretter handlingen **Åpne på nytt**.

    > [!NOTE]  
    >   En leder kan avvise en timelistelinje som er sendt til godkjenning. Hvis en linje har statusen **Avvist**, kan du gjøre endringer på linjen og deretter velge **Send** på nytt.  
7. Velg **OK**.

## <a name="to-approve-or-reject-a-time-sheet"></a>Slik godkjenner eller avviser du timelister:
En timeliste må sendes inn til godkjenning før den kan brukes. Du kan godkjenne og avvise individuelle linjer på en timeliste eller sende dem tilbake til avsenderen for ytterligere handling. En timeliste kan godkjennes på to måter:

* En timelisteadministrator kan godkjenne en hvilken som helst timeliste.
* Personen som er angitt i feltet **Bruker-ID for godkjenner av timeliste** på et ressurskort, kan godkjenne timelister for denne ressursen. Hvis du vil ha mer informasjon, kan du se [Definere timelister](projects-how-setup-time-sheets.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Administrer timelister**, og velg deretter den relaterte koblingen.
2. Velg en timeliste fra listen.  
3. På siden **Timeliste** 
    1. Velg handlingen **Behandle**, og velg deretter **Godkjenn**-handlingen.
    2. Velg handlingen **Alle sendte linjer** for å godkjenne alle linjer eller **Bare valgte linjer** for å godkjenne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**.  
5. Du kan også velge handlingen **Avvis** og følge trinn 4 til 5.  

> [!TIP]  
>   Bruk faktaboksene **Timelistestatus** og **Faktisk/budsjettert sammendrag** til å få oversikt over timelisteinformasjon.

Når du har godkjent eller avvist en timeliste, kan den ikke endres uten at den åpnes på nytt først. Følgende fremgangsmåte forklarer hvordan du åpner en godkjent eller avvist timeliste på nytt.

## <a name="to-reopen-a-time-sheet"></a>Åpne en timeliste på nytt
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Administrer timelister** eller **Timelister**, og velg deretter den relaterte koblingen.
2. Åpne en timeliste fra listen.  

    > [!NOTE]  
    >   Bare linjer som har statusen **Godkjent**, kan åpnes på nytt. Linjer som har statusen **Avvist**, kan ikke åpnes på nytt. Du kan ikke åpne en timeliste på nytt hvis den er bokført.  
3. På siden **Timeliste** velger du handlingen **Åpne på nytt**, og deretter velger du handlingen **Alle sendte linjer** for å åpne alle linjer på nytt, eller handlingen **Bare valgte linjer** for å åpne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**. Statusen for timelistelinjen eller -linjene endres til **Sendt**.  

## <a name="to-view-and-approve-time-sheets-by-job"></a>Slik viser og godkjenner du timelister etter prosjekt

På et prosjekt kan du angi en person som er ansvarlig for prosjektet. Denne informasjonen er knyttet til timelistelinjer, og kan brukes til å lage en liste over timelistene som en prosjektleder må gjennomgå og godkjenne. Prosjektlederen for en prosjektgruppe kan for eksempel ha ansvaret for bestemte prosjekter i selskapet. I dette tilfellet bør lederen velges som **Ansvarlig person** på prosjektkortet. I denne visningen av timelisteinformasjon kan du se prosjektoppgaver som er knyttet til et prosjekt, og antall timer som er brukt.

> [!NOTE]
> For å kunne godkjenne timelister i vinduet **Timeliste for leder etter prosjekt** må du først velge et alternativ for **Timeliste etter jobbgodkjenning** på siden **Ressursoppsett**. Hvis du vil ha mer informasjon, kan du se [Definere ressurser](projects-how-setup-resources.md).

### <a name="to-approve-or-reject-a-time-sheet-by-job"></a>Slik godkjenner eller avviser du timelister etter prosjekt:

1. Skriv inn **Timeliste for leder etter prosjekt** i **Søk**-boksen, og velg deretter den relaterte koblingen. [!INCLUDE[prod_short](includes/prod_short.md)] viser en liste over timelistelinjer som er knyttet til prosjektene du har ansvar for.
2. Velg handlingen **Godkjenn**, og velg deretter handlingen **Alle sendte linjer** for å godkjenne alle linjer, eller handlingen **Bare valgte linjer** for å godkjenne bare linjene som er valgt på siden **Timeliste**.

    > [!NOTE]
    > Du kan bare godkjenne timelister som har statusen **Sendt**.

3. Hvis du vil gi mer informasjon om godkjenningen eller avvisningen, velger du **Relatert**-handlingen, velger **Merknader** og deretter **Linjemerknader** og skriver inn merknader.
4. Velg **OK**-knappen.

> [!NOTE]
> Når du har godkjent eller avvist en timelistelinje etter prosjekt, kan den ikke åpnes på nytt eller endres i vinduet **Timeliste**.

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Slik bokfører du timelistelinjer i en ressurskladd
Når du har godkjent timelisteoppføringer for en ressurs, kan du bokføre dem til den relevante ressurskladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurskladder** og velg den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. På siden **Foreslå ressurskladdelinjer** fyller du ut feltene etter behov.  
4. Velg **OK**-knappen. Det opprettes poster for bruk i ressurskladden, der du kan endre informasjonen etter behov.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Ressursposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Slik bokfører du timelistelinjer i en prosjektkladd
Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjektkladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. På siden **Foreslå prosjektkladdelinjer** fyller du ut feltene etter behov.  
4. Velg **OK**-knappen. Det opprettes poster for bruk i prosjektkladden, der du kan endre informasjonen etter behov.  

    > [!NOTE]  
    >   Informasjon om arbeidstypen og om arbeidet er belastbart, kopieres fra timelistelinjen. Du kan om nødvendig redusere antall timer og foreta en delvis bokføring. Hvis du reduserer antallet, inneholder linjen som opprettes, gjenstående timeantall neste gang du velger handlingen **Foreslå linjer fra timelister**.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Prosjektposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="to-archive-time-sheets"></a>Slik arkiverer du timelister:
Når du har bokført timelister, kan du arkivere dem for fremtidig referanse. Alle timelistelinjer må være bokført før en timeliste kan arkiveres.

> [!NOTE]  
>   Når du arkiverer en timeliste, fjernes den fra listene på siden **Timelister** og **Timelister for leder**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Timelister**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Flytt timelister til arkiv**.  
3. På siden **Flytt timelister til arkiv** fyller du ut feltene etter behov, og deretter velger du **OK**-knappen.  
4. Hvis du vil gå gjennom arkiverte timelister, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Timelistearkiver** eller **Administrer timelistearkiver**, og velg deretter den relaterte koblingen.

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]