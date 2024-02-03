---
title: Angi når og hvor du kan motta arbeidsflytvarsler
description: 'Når du definerer brukere i arbeidsflyt for godkjenning, kan du angi hvordan og når hver godkjenningsbruker mottar varsler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '663, 1500, 1512, 1513,'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Angi når og hvor du kan motta arbeidsflytvarsler

Når du definerer godkjenningsbrukere i arbeidsflytprosesser der du vil at noen skal godkjenne endringer, for eksempel når nye poster opprettes, eller når noen ber om en godkjenning, må du angi hvordan og når godkjenningsbrukeren skal varsles. Du kan for eksempel angi at en godkjenningsbruker umiddelbart skal motta en e-post når noen oppretter en ny kunde. Du kan også planlegge at varsler skal settes på vent og leveres samtidig, for eksempel ukentlig eller månedlig.

Personer kan også endre sine varslingsoppsett ved å velge **Endre varslingsinnstillinger** i et varsel.  

> [!NOTE]
> Varslinger leveres i henhold til varslingsinnstillingene for mottakeren, ikke avsenderen. Det er et viktig skille fordi det betyr at når noen ber om en godkjenning som en del av en arbeidsflyt, sendes ikke nødvendigvis forespørselen umiddelbart. I stedet leveres den i henhold til varslingsplanen som er angitt i godkjennerens varslingsinnstillinger.

Før du kan angi varslingsinnstillinger for en godkjenningsbruker, må du må du konfigurere brukeren som en godkjenningsbruker. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Hvis du vil bruke e-post som varslingsmetode, må du konfigurere e-post for både avsenderen og mottakeren i [!INCLUDE [prod_short](includes/prod_short.md)]. Finn ut mer under [Definer e-post](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Trinn i arbeidsflyter

Mange trinn i arbeidsflyten for godkjenning omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. På ett arbeidsflyttrinn kan for eksempel hendelsen være at bruker 1 ber om godkjenning av en ny post. Det relaterte svaret er at det er sendt en varsling til bruker 2, godkjenneren. På det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten. Det relaterte svaret er at det er sendt en varsling til bruker 3 om å starte en prosess med den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning. Finn ut mer under [Arbeidsflyt](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications"></a>Angi når og hvor godkjenningsbrukere mottar varsler

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2. Velg linjen for brukeren du vil konfigurere varslingsinnstillinger for, og velg deretter **Oppsett av varsling**.  
3. På siden **Oppsett av arbeidsflytvarsling** fyller du ut feltene som beskrevet i tabellen nedenfor.  

   > [!NOTE]
   > Hvis du åpner siden **Oppsett av arbeidsflytvarsling** fra siden **Brukeroppsett for godkjenning**, er varslingsoppsettet tilknyttet godkjenningsbrukeren. Godkjenningsbrukeren vil alltid motta arbeidsflytvarsler i henhold til varslingsoppsettet. Hvis du bruker funksjonen *Fortell meg* til å åpne **Oppsett av arbeidsflytvarsling**-siden, gjelder varslingsoppsettet alle brukere.

   |Felt|Description|
   |-----|-----------|
   |**Varslingstype**|Angi typen hendelse varslet omhandler.<br /><br /> Velg ett av følgende alternativer:<br /><br /> -   **Ny post** angir at varslet omhandler en ny post, for eksempel et dokument, og at brukeren må gjøre noe med det.<br />-   **Godkjenning** angir at varslet omhandler én eller flere godkjenningsforespørsler.<br />-   **Forfalt** angir at varslet er for å påminne brukere om at de er forsinket med å gjøre noe med en hendelse.|
   |**Varslingsmetode**|Angi om varslingen er en e-post eller et internt notat.|

   Du kan definere oppsettet for e-postvarsler ved å tilpasse rapport 1320, E-postvarsling. Finn ut mer på [Opprett og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

   Du har nå angitt hvor brukeren mottar varslinger. Fortsett med å angi når brukeren mottar varslinger.  
4. Velg handlingen **Tidsplan for varsling**.  
5. På siden **Tidsplan for varsling** fyller du ut feltene som beskrevet i tabellen nedenfor.  

   |Felt|Description|
   |-----|-----------|
   |**Gjentakelse**|Angi mønsteret for regelmessighet som varslene sendes til brukeren.|
   |**Klokkeslett**|Angi hvilket tidspunkt på dagen varslene sendes til brukeren når verdien i feltet **Gjentakelse** ikke er **Umiddelbart**.|
   |**Daglig intervall**|Angi på hvilken type dager brukeren mottar varsler når verdien i feltet **Gjentakelse** er **Daglig**.<br /><br /> Velg **Ukedag** for å motta varslinger hver dag i arbeidsuken. Velg **Daglig** for å motta varslinger hver dag i uken, herunder helger.|
   |**Mandag** til **søndag**|Angi på hvilke dager brukeren mottar varsler når verdien i feltet **Gjentakelse** er **Ukentlig**.|
   |**Dato i måned**|Angi om brukeren mottar varsler på først, siste, eller en bestemt dato i måneden.|
   |**Dato for månedlig varsel**|Angi datoen i måneden brukeren mottar varsler når verdien i feltet **Dato i måned** er **Egendefinert**.|

## <a name="change-when-and-how-you-receive-notifications"></a>Endre når og hvor du mottar varsler

1. I et av varslene som du har mottatt, enten som en e-post eller et notat, velger du **Endre varslingsinnstillinger**.  
2. På siden **Oppsett av arbeidsflytvarsling** endre du varslingsinnstillinger, som beskrevet i trinn 3 til 5 ovenfor.
   1. Kontroller at riktig varsel er valgt under feltet **Varslingstype**.
   2. Velg om du vil motta en e-post eller et notatvarsel under feltet **Varslingsmetode**.
   3. Velg **varslingsplanen** for å endre hyppigheten og gjentakelsen for når varslinger sendes.

## <a name="see-also"></a>Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Opprett og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Konfigurering av godkjenningsarbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
