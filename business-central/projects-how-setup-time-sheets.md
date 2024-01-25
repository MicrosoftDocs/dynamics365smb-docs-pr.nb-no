---
title: Definer timelister og godkjenningen av dem
description: 'Du definerer timelister for å spore tiden som brukes på oppgaver og prosjekter, og dette er til hjelp ved prosjektstyring, bemanning og kapasitet'
ms.reviewer: jswymer
author: brentholtorf
ms.author: bholtorf
mw.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff, resource, time sheet'
ms.search.form: '977, 462, 76, 77, 462'
ms.date: 07/27/2023
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-time-sheets"></a>Definere timelister

Timelister i [!INCLUDE[prod_short](includes/prod_short.md)] håndterer tidsregistrering i ukentlige intervaller på sju dager. Du kan bruke dem til å spore tiden som brukes på prosjekter, og du kan bruke dem til å registrere enkel registrering av ressurstid. Før du kan bruke timelister, må du angi hvilke brukere som skal sende timelister, og hvordan du vil konfigurere timelister.  

> [!TIP]
> Personer som bruker timeliste, er *ressurser*. La oss for eksempel si at du bruker timelister til å spore arbeidet på ikke-ansatte. For å kunne spore arbeidet til de ansatte eller bruke timelister til å spore ansattfravær må du knytte ansatte til ressurser. Det er en assistert installasjonsveiledning som kan hjelpe deg med å gjøre det. Hvis du vil vite mer om veiledningen, kan du gå til [Definere timelister med veiledningen for assistert oppsett](#set-up-time-sheets-with-the-assisted-setup-guide).  

Du kan eventuelt angi om, og hvordan, timelister skal godkjennes. Avhengig av behovene i organisasjonen, kan du angi:

* En eller flere brukere som administrator for timeliste og godkjenning for alle timelister.
* En godkjenner av timelister for hver ressurs.

Når du har definert timelister, kan du opprette timelister for ressurser, og ressursene kan bokføre timelistelinjer. Alternativt kan du tilordne timelister til prosjektplanleggingslinjer. Hvis du vil ha mer informasjon, kan du gå til [Bruke timelister](projects-how-use-time-sheets.md).  

## <a name="set-up-time-sheets-with-the-assisted-setup-guide"></a>Definer timelister med den assisterte oppsettveiledningen

En assisterte oppsettveiledningen hjelper deg med å opprette timelister.  

> [!TIP]
> Hvis du har en versjon som er tidligere enn lanseringsbølge 1 2023 (v22), må du aktivere funksjonen **Funksjonsoppdatering: ny timelistefunksjon** på siden [Funksjonsbehandling](https://businesscentral.dynamics.com/?page=2610) for å bruke denne funksjonen.
>
> Med denne innstillingen kan du også bruke timelister på mobile enheter.

Åpne veiledningen for assistert oppsett **Definer timelister** fra siden [Assistert oppsett](https://businesscentral.dynamics.com/?page=1801).

I veiledningen for assistert oppsett går du gjennom følgende fremgangsmåte:

1. Konfigurer deltakerne i timelisteprosessene.

    Den første siden i guiden viser hvor mange brukere som er i bruk i [!INCLUDE [prod_short](includes/prod_short.md)]. Den viser også annen obligatorisk og valgfri informasjon.  
2. Angi den første dagen i en arbeidsuke i denne organisasjonen.

    Den første dagen i en arbeidsuke vil være standard første dag for alle timelister.
3. Angi personen som administrerer timelistene.

    Denne personen kan redigere og slette alle timelister. Du kan også legge til samme rolle på siden **Brukeroppsett**.
4. Definer ressursene som skal bruke timelister, og hvem som skal godkjenne timelistene.

På slutten av oppsettveiledningen kan du velge å la [!INCLUDE [prod_short](includes/prod_short.md)] opprette timelister basert på konfigurasjonen din. Vis de nye timelistene på siden **Timelister**, som du kan åpne [her](https://businesscentral.dynamics.com/?page=951). Du kan eventuelt kjøre den assisterte oppsettveiledningen på nytt eller fullføre oppsettet manuelt.

> [!IMPORTANT]
> Hvis du bruker lanseringsbølge 1 (v22) for 2023 eller senere, må du manuelt aktivere alternativet **Bruk ny timelistefunksjon** for å sikre at du kan administrere timelister på mobile enheter, som beskrevet i neste fremgangsmåte.

## <a name="set-up-time-sheets-manually"></a>Definer timelister manuelt

Følgende deler beskriver hvordan du definerer timelister hvis du ikke bruker den assisterte oppsettveiledningen **Definer timelister**.  

### <a name="to-set-up-general-information-for-time-sheets-manually"></a>Slik definerer du generell informasjon for timelister manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressursoppsett** og velg den relaterte koblingen.  
1. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!IMPORTANT]
   > Hvis du bruker lanseringsbølge 1 (v22) for 2023 eller senere, må du slå på alternativet **Bruk ny timelisteopplevelse** for å sikre at du kan administrere timelister på mobile enheter.
1. For feltet **Timeliste etter prosjektgodkjenning** velger du ett av følgende alternativer.

| Alternativ | Beskrivelse |
| --- | --- |
| **Aldri** |Brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet godkjenner timelisten. |
| **Alltid** |Brukeren i feltet **Ansvarlig person** på prosjektkortet godkjenner timelisten. |
| **Bare maskin** |Hvis timelisten for maskin er knyttet til et prosjekt, godkjenner brukeren i feltet **Ansvarlig person** på prosjektkortet, timelisten. Hvis timelisten for maskin er knyttet til en ressurs, godkjenner brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet, timelisten. |

### <a name="to-assign-a-time-sheet-administrator-manually"></a>Slik tilordner du en timelisteadministrator manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett** og velg den relaterte koblingen.  
3. Velg brukeren som skal være timelisteadministrator, og merk deretter av for **Administrasjon av timeliste**.  

> [!TIP]  
> Det anbefales at du velger bare én bruker som administrator for timelisten i et selskap. I den følgende fremgangsmåten setter du opp en timelisteeier og -godkjenner, der godkjenneren av timelisten er tilordnet for hver ressurs.  

### <a name="to-assign-a-time-sheets-owner-and-approver-manually"></a>Slik tilordner du en timelisteeier og -godkjenner manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Merk ressursen du vil definere muligheten til å bruke timelister for, og merk deretter av for **Bruk timeliste**.  
3. Angi ID-en for eieren av timelisten i feltet **Bruker-ID for eier av timeliste:**. Eieren kan angi tidsbruk på en timeliste og sende den til godkjenning. Når ressursen er en person, er denne personen vanligvis også eieren.  
4. Angi ID-en for godkjenneren av timelisten i feltet **Bruker-ID for godkjenner av timeliste**. Godkjenneren kan godkjenne, avvise eller åpne på nytt en timeliste.  

> [!NOTE]  
> Du kan ikke endre IDen for godkjenneren av timelisten hvis det finnes timelister som ennå ikke er behandlet og som har statusen **Sendt** eller **Åpen**.

## <a name="see-also"></a>Se også

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
