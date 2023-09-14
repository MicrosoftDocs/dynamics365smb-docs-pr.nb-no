---
title: Definer timelister og godkjenningen av dem
description: 'Du definerer timelister for å spore tiden som brukes på oppgaver og prosjekter, og dette er til hjelp ved prosjektstyring, bemanning og kapasitet'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77'
ms.date: 12/13/2021
ms.author: bholtorf
---
# Definere timelister

Timelister i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ukentlige intervaller på sju dager. Du kan bruke dem til å spore tiden som brukes på prosjekter, og du kan bruke dem til å registrere enkel registrering av ressurstid. Før du kan bruke timelister, må du angi hvilke brukere som skal sende timelister, og hvordan du vil konfigurere timelister.  

> [!TIP]
> I [!INCLUDE [prod_short](includes/prod_short.md)] er brukerne av timelister *ressurser*. På denne måten kan du for eksempel bruke timelister til å spore arbeidet på ikke-ansatte. For å kunne spore arbeidet til de ansatte eller bruke timelister til å spore ansattfravær må du knytte *ressurser* til *ansatte* i oppsettveiledningen.  

Du kan eventuelt angi om og hvordan timelister skal godkjennes. Avhengig av behovene i organisasjonen, kan du angi:

* En eller flere brukere som administrator for timeliste og godkjenning for alle timelister.
* En godkjenner av timelister for hver ressurs.

Når du har definert timelister, kan du opprette timelister for ressurser, og ressursene kan bokføre timelistelinjer. Alternativt kan du tilordne timelister til prosjektplanleggingslinjer. Hvis du vil ha mer informasjon, kan du se [Bruke timelister](projects-how-use-time-sheets.md).  

## Definer timelister med den assisterte oppsettveiledningen

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

Fra lanseringsbølge 2 for 2021 kan du bruke en veiledning for assistert oppsett til å definere timelister.  

> [!TIP]
> Du må aktivere funksjonen **Funksjonsoppdatering: ny timelistefunksjon** på siden [Funksjonsbehandling](https://businesscentral.dynamics.com/?page=2610) for å bruke denne funksjonen.
>
> Den samme funksjonen gjør det også enkelt å behandle timelister på en mobil enhet.

Åpne veiledningen for assistert oppsett **Definer timelister** fra siden [Assistert oppsett](https://businesscentral.dynamics.com/?page=1801).

I veiledningen for assistert oppsett går du gjennom følgende fremgangsmåte:

1. Konfigurer deltakerne i timelisteprosessene

    Den første siden i guiden viser hvor mange brukere som er i bruk i [!INCLUDE [prod_short](includes/prod_short.md)]. Den viser også annen obligatorisk og valgfri informasjon.  
2. Angi den første dagen i en arbeidsuke i denne organisasjonen

    Den første dagen i en arbeidsuke vil være standard første dag for alle timelister.
3. Angi personen som administrerer timelistene

    Denne personen kan redigere og slette alle timelister. Du kan også legge til samme rolle på siden **Brukeroppsett**.
4. Definer ressursene som skal bruke timelister, og hvem som skal godkjenne timelistene

På slutten av oppsettveiledningen kan du velge å la [!INCLUDE [prod_short](includes/prod_short.md)] opprette timelister basert på konfigurasjonen din. Vis de nye timelistene på siden **Timelister**, som du kan åpne [her](https://businesscentral.dynamics.com/?page=951). Du kan eventuelt kjøre den assisterte oppsettveiledningen på nytt eller fullføre oppsettet manuelt.  

## Definer timelister manuelt

Følgende deler beskriver hvordan du definerer timelister hvis du ikke bruker den assisterte oppsettveiledningen **Definer timelister**.  

### Slik definerer du generell informasjon for timelister manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressursoppsett** og velg den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For feltet **Timeliste etter prosjektgodkjenning** velger du ett av følgende alternativer.

| Alternativ | Beskrivelse |
| --- | --- |
| **Aldri** |Brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet godkjenner timelisten. |
| **Alltid** |Brukeren i feltet **Ansvarlig person** på prosjektkortet godkjenner timelisten. |
| **Bare maskin** |Hvis timelisten for maskin er knyttet til et prosjekt, godkjenner brukeren i feltet **Ansvarlig person** på prosjektkortet, timelisten. Hvis timelisten for maskin er knyttet til en ressurs, godkjenner brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet, timelisten. |

### Slik tilordner du en timelisteadministrator manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett** og velg den relaterte koblingen.  
2. Legg til en ny bruker hvis brukerlisten ikke inkluderer personen som du vil skal være ansvarlig for timelisteregistrering. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).
3. Velg en bruker som administrator for en timeliste, og merk deretter av for **Administrator for timeliste**  

> [!TIP]  
> Det anbefales at du velger bare én bruker som administrator for timelisten i et selskap. I den følgende fremgangsmåten setter du opp en timelisteeier og -godkjenner, der godkjenneren av timelisten er tilordnet for hver ressurs.  

### Slik tilordner du en timelisteeier og -godkjenner manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Merk ressursen du vil definere muligheten til å bruke timelister for, og merk deretter av for **Bruk timeliste**.  
3. Angi ID-en for eieren av timelisten i feltet **Bruker-ID for eier av timeliste:**. Eieren kan angi tidsbruk på en timeliste og sende den til godkjenning. Når ressursen er en person, er denne personen vanligvis også eieren.  
4. Angi ID-en for godkjenneren av timelisten i feltet **Bruker-ID for godkjenner av timeliste**. Godkjenneren kan godkjenne, avvise eller åpne på nytt en timeliste.  

> [!NOTE]  
> Du kan ikke endre IDen for godkjenneren av timelisten hvis det finnes timelister som ennå ikke er behandlet og som har statusen **Sendt** eller **Åpen**.

## Se relatert [Microsoft-opplæring](/training/paths/set-up-jobs-resources/)

## Se også

[Bruke timelister for prosjekter](projects-how-use-time-sheets.md)  
[Slik oppretter du timelister](projects-how-use-time-sheets.md#to-create-time-sheets)  
[Registrere forbruk eller bruk for prosjekter](projects-how-record-job-usage.md)  
[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
