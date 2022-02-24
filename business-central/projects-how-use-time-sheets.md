---
title: Arbeide med timelister for prosjekter| Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en timeliste for et prosjekt, kopierer planleggingslinjer til den, definerer arbeidstyper, fyller ut timelisten og sender den inn til godkjenning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0df593988b7db1f7f02a4c8868df448b8fb1bbc0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312679"
---
# <a name="use-time-sheets-for-jobs"></a>Bruke timelister for prosjekter
Du bruker kjørselen **Opprett timelister** til å angi timelister for et angitt antall tidsperioder eller uker. Du må ha tillatelser for å kunne opprette timelister.

Du kan kopiere og bruke prosjektplanleggingslinjer i en timeliste. Dermed trenger du bare å skrive inn informasjonen ett sted, og linjeinformasjonen er alltid riktig.

Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjekt- eller ressurskladden.

Før du kan bruke timelister, må du definere generell informasjon og angi administrator og én eller flere godkjennere av timelister. Hvis du vil ha mer informasjon, kan du se [Definere timelister](projects-how-setup-time-sheets.md).

## <a name="to-create-a-time-sheet"></a>Slik oppretter du en timeliste
Du kan bruke kjørselen **Opprett timelister** til å angi timelister for et angitt antall tidsperioder eller uker. Deretter kan eieren av timelisten åpne den og registrere tid som er brukt på en aktivitet.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister**, og velg deretter den relaterte koblingen.
2. På siden **Liste for timeliste** velger du handlingen **Opprett timelister**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Feltene **Bruk timeliste** og **Bruker-ID for eier av timeliste** må fylles ut på kortet for ressursen i timelisten.

1. Velg **OK**.  

Du kan vise timelistene som du har opprettet, på siden **Liste for timeliste**.

## <a name="to-copy-job-planning-lines-to-a-time-sheet"></a>Slik kopierer du prosjektplanleggingslinjer til en timeliste:
Fremgangsmåten nedenfor beskriver hvordan du raskt legger til prosjektplanleggingslinjer i en timeliste.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister**, og velg deretter den relaterte koblingen.  
2. På siden **Liste for timeliste** velger du en timeliste for den aktuelle perioden, og deretter velger du handlingen **Rediger timeliste**.  
3. Velg handlingen **Opprett linjer fra prosjektplanlegging**. Alle typer prosjektplanleggingslinjer i timelisteperioden kopieres til timelisten for personen eller maskinen i feltet **Ressursnr.** i timelisten.

## <a name="to-define-work-types-and-add-one-to-a-time-sheet"></a>Slik definerer du arbeidstyper og legger til en til en timeliste
Du kan definere arbeidstypen for alle linjer i timelister for prosjekter. På denne måten kan du legge til informasjon du trenger for å kunne fakturere kunden for ulike typer arbeid.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister**, og velg deretter den relaterte koblingen.   
2. Åpne den relevante timelisten.
3. Velg feltet **Beskrivelse**.  
4. På siden **Timelistelinje – prosjektdetaljer** velger du feltet **Arbeidstypekode** og velger en arbeidstype fra listen, for eksempel **Miles**.  
5. Hvis det ikke finnes noen arbeidstyper, velger du handlingen **Ny**.
6. På siden **Arbeidstyper** fyller du ut feltene etter behov.
7. Gjenta trinn 4 for å tilordne den nye arbeidstypen til timelisten.

## <a name="to-reuse-time-sheet-lines-in-other-time-sheets"></a>Slik bruker du timelistelinjer på nytt i andre timelister
Hvis timelisteinformasjon er den samme fra tidsperiode til tidsperiode, kan du spare tid ved å kopiere linjene fra forrige tidsperiode. Deretter angir du bare tidsbruken for den nye perioden.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Åpne timelisten for en periode som er senere enn perioden for en eksisterende timeliste med linjer.  
3. Velg handlingen **Kopier linjer fra tidligere timeliste**.

Linjene kopieres, inkludert detaljer som type og beskrivelse. Hvis linjen for eksempel er knyttet til et prosjekt, blir **Prosjektnr.** kopiert. Alle kopierte linjer har statusen **Åpen**. Du kan nå endre linjene etter behov.

## <a name="to-fill-in-a-time-sheet-lines-and-submit-for-approval"></a>Slik fyller du ut timelistelinjer og sender til godkjenning
Timelisteregistrering spores i timer, som er standard lagerenhet for ressurser. Som standard viser en timeliste vanlige arbeidsdager fra mandag til fredag.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister**, og velg deretter den relaterte koblingen.  
2. Velg en timeliste for den relevante tidsperioden, og velg deretter handlingen **Rediger timeliste**.  
3. Fyll ut feltene på en linje etter behov. Angi antall timer som brukes av ressursen for hver dag i uken.

    > [!TIP]  
    >   Du kan se gjennom summen av timelistetimer som du har angitt i faktaboksen **Faktisk/budsjettert sammendrag**.  
4. Gjenta trinn 3 for arbeidstypene som utføres av ressursen.
5. Velg handlingen **Send**, og velg deretter handlingen **Alle åpne linjer** for å sende alle linjer, eller handlingen **Bare valgte linjer** for å sende bare linjene som er valgt på siden **Timeliste**.  

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

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister for leder**, og velg deretter den relaterte koblingen.
2. Velg en timeliste fra listen.  
3. På siden **Timeliste** velger du handlingen **Godkjenn**, og deretter velger du handlingen **Alle sendte linjer** for å godkjenne alle linjer, eller handlingen **Bare valgte linjer** for å godkjenne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**.  
5. Du kan også velge handlingen **Avvis** og følge trinn 4 til 5.  

> [!TIP]  
>   Bruk faktaboksene **Timelistestatus** og **Faktisk/budsjettert sammendrag** til å få oversikt over timelisteinformasjon.

Når du har godkjent eller avvist en timeliste, kan den ikke endres uten at den åpnes på nytt først. Følgende fremgangsmåte forklarer hvordan du åpner en godkjent eller avvist timeliste på nytt.

## <a name="to-reopen-a-time-sheet"></a>Åpne en timeliste på nytt
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Timelister for leder** eller **Timelister**, og velg deretter den relaterte koblingen.
2. Åpne en timeliste fra listen.  

    > [!NOTE]  
    >   Bare linjer som har statusen **Godkjent**, kan åpnes på nytt. Linjer som har statusen **Avvist**, kan ikke åpnes på nytt. Du kan ikke åpne en timeliste på nytt hvis den er bokført.  
3. På siden **Timeliste** velger du handlingen **Åpne på nytt**, og deretter velger du handlingen **Alle sendte linjer** for å åpne alle linjer på nytt, eller handlingen **Bare valgte linjer** for å åpne bare linjene som er valgt på siden **Timeliste**.
4. Velg **OK**. Statusen for timelistelinjen eller -linjene endres til **Sendt**.  

## <a name="to-post-time-sheet-lines-in-a-resource-journal"></a>Slik bokfører du timelistelinjer i en ressurskladd
Når du har godkjent timelisteoppføringer for en ressurs, kan du bokføre dem til den relevante ressurskladden.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurskladd**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. Fyll ut feltene etter behov.  
4. Velg **OK**. Det opprettes poster for bruk i ressurskladden, der du kan endre informasjonen etter behov.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Ressursposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="to-post-time-sheet-lines-in-a-job-journal"></a>Slik bokfører du timelistelinjer i en prosjektkladd
Når du har godkjent timelisteoppføringer for et prosjekt, kan du bokføre dem til den relevante prosjektkladden.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjektkladd**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå linjer fra timelister**.  
3. Fyll ut feltene etter behov.  
4. Velg **OK**. Det opprettes poster for bruk i prosjektkladden, der du kan endre informasjonen etter behov.  

    > [!NOTE]  
    >   Informasjon om arbeidstypen og om arbeidet er belastbart, kopieres fra timelistelinjen. Du kan om nødvendig redusere antall timer og foreta en delvis bokføring. Hvis du reduserer antallet, inneholder linjen som opprettes, gjenstående timeantall neste gang du velger handlingen **Foreslå linjer fra timelister**.  
5. Velg handlingen **Bokfør**.  
6. Hvis du vil bekrefte bokføringen, velger du handlingen **Poster**. Siden **Prosjektposter** åpnes med resultatet av bokføringen av ressurskladden.

## <a name="to-archive-time-sheets"></a>Slik arkiverer du timelister:
Når du har bokført timelister, kan du arkivere dem for fremtidig referanse. Alle timelistelinjer må være bokført før en timeliste kan arkiveres.

> [!NOTE]  
>   Når du arkiverer en timeliste, fjernes den fra listene på siden **Timelister** og **Timelister for leder**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Flytt timelister til arkiv**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov, og klikk deretter **OK**.  
3. Hvis du vil vise arkiverte timelister, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Timelistearkiver** eller **Timelistearkiver for leder** og velger deretter den relaterte koblingen.

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Konfigurere prosjektstyring](projects-setup-projects.md)    
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)     
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
