---
title: Angi når og hvor du kan motta varsler
description: Når du konfigurerer brukere i godkjenningsarbeidsflyter, må du på sidene Oppsett av varsling og Tidsplan for varsling angi hvordan og når hver enkelt bruker mottar varsler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 52fbabb8e8d2fbb9217bbcd1f9971f8f11037893
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482481"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Angi når og hvor du kan motta varsler
Når du konfigurerer brukere i godkjenningsarbeidsflyter, må du på sidene **Oppsett av varsling** og **Tidsplan for varsling** angi hvordan og når hver enkelt bruker mottar varsler om trinn i godkjenningsarbeidsflyten. Enkeltbrukere kan også endre sine varslingsoppsett ved å velge kappen **Endre varslingsinnstillinger** i et varsel.  

> [!NOTE]
> Varslinger leveres i henhold til varslingsinnstillingene for mottakeren, ikke avsenderen. Det er et viktig skille fordi det betyr at når noen ber om en godkjenning som en del av en arbeidsflyt, sendes ikke nødvendigvis forespørselen umiddelbart. I stedet leveres den i henhold til varslingsplanen som er angitt i godkjennerens varslingsinnstillinger. 

 Før du kan angi varslingsinnstillinger for en godkjenningsbruker, må du må du konfigurere brukeren som en godkjenningsbruker. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  

 Du kan definere oppsettet for e-postvarsler ved å tilpasse rapport 1320, E-postvarsling. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  

 Mange trinn i arbeidsflyten for godkjenning omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. På ett arbeidsflyttrinn kan for eksempel hendelsen være at bruker 1 ber om godkjenning av en ny post. Det relaterte svaret er at det er sendt en varsling til bruker 2, godkjenneren. På det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten. Det relaterte svaret er at det er sendt en varsling til bruker 3 om å starte en prosess med den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]
> Hvis du vil bruke e-post som varslingsmetode, må du konfigurere e-post for både avsenderen og mottakeren i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

## <a name="specify-when-and-how-users-receive-notifications"></a>Angi når og hvor brukere mottar varsler  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.  
2.  Velg linjen for brukeren du vil konfigurere varslingsinnstillinger for, og velg deretter **Oppsett av varsling**.  
3.  På siden **Oppsett av varsling** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Varslingstype**|Angi hvilken type hendelse varslet omhandler.<br /><br /> Velg ett av følgende alternativer:<br /><br /> -   **Ny post** angir at varslet omhandler en ny post, for eksempel et dokument, og at brukeren må gjøre noe med det.<br />-   **Godkjenning** angir at varslet omhandler én eller flere godkjenningsforespørsler.<br />-   **Forfalt** angir at varslet er for å påminne brukere om at de er forsinket med å gjøre noe med en hendelse.|  
    |**Varslingsmetode**|Angi om varslingen er en e-post eller et internt notat.|

    Du kan definere oppsettet for e-postvarsler ved å tilpasse rapport 1320, E-postvarsling. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

    Du har nå angitt hvor brukeren mottar varslinger. Fortsett med å angi når brukeren mottar varslinger.  

4.  Velg handlingen **Tidsplan for varsling**.  
5.  På siden **Tidsplan for varsling** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Gjentakelse**|Angi mønsteret for regelmessighet brukeren mottar varsler etter.|  
    |**Klokkeslett**|Angi hvilket tidspunkt på dagen brukeren mottar varslinger når verdien i feltet **Gjentakelse** ikke er **Umiddelbart**.|  
    |**Daglig intervall**|Angi på hvilken type dager brukeren mottar varsler når verdien i feltet **Gjentakelse** er **Daglig**.<br /><br /> Velg **Ukedag** for å motta varslinger hver arbeidsdag i uken. Velg **Daglig** for å motta varslinger hver dag i uken, herunder helger.|  
    |**Mandag** til **søndag**|Angi på hvilke dager brukeren mottar varsler når verdien i feltet **Gjentakelse** er **Ukentlig**.|  
    |**Dato i måned**|Angi om brukeren mottar varsler på først, siste, eller en bestemt dato i måneden.|  
    |**Dato for månedlig varsel**|Angi datoen i måneden brukeren mottar varsler når verdien i feltet **Dato i måned** er **Egendefinert**.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Endre når og hvor du mottar varsler  
1.  I et av varslene som du har mottatt, enten som e-post eller notat, velger du knappen **Endre varslingsinnstillinger**.  
2.  På siden **Oppsett av varsling** endre du varslingsinnstillinger, som beskrevet i den forrige fremgangsmåten.  

## <a name="see-also"></a>Se også  
 [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)   
 [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)   
 [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)   
 [Konfigurere arbeidsflyter](across-set-up-workflows.md)   
 [Bruke arbeidsflyter](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]