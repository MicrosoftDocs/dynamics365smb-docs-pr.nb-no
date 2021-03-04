---
title: Arbeidsflytvarslinger
description: Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren. I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: 1dd64213bc38d5d98e6369e97257e53cef04bbd0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753028"
---
# <a name="workflow-notifications"></a>Arbeidsflytvarslinger

Konfigurere arbeidsflytene slik at de automatisk varsler brukere når de må det må utføres handlinger for et trinn i arbeidsflyten. Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren. I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
> Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter varsler som e-post og interne merknader.  

> [!IMPORTANT]  
> Alle arbeidsflytvarsler sendes via en jobbkø. Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler, og at det er merket av for **Start automatisk fra server**. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Konfigurer varslinger

Du kan definere ulike aspekter ved arbeidsflytvarsler på følgende steder:  

* Godkjenner-varsling

    For arbeidsflyter for godkjenning angir du mottakerne av arbeidsflytvarsler ved å fylle en linje på siden **Brukeroppsett for godkjenning** for hver bruker som tar del i arbeidsflyten.  

    Hvis for eksempel bruker 2 er angitt i **Godkjenner-ID**-feltet på linjen for bruker 1, sendes varselet om godkjenningsforespørsel til bruker 1. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  
* Tidsplaner for varsling

    Du kan angi når og hvordan brukere skal motta arbeidsflytvarsler, ved å fylle ut siden **Tidsplan for varsling** for hver arbeidsflytbruker. Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Tilpass e-postvarslingene

    Hvis du vil, kan du tilpasse innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  
* Svaralternativer

    Du definerer det bestemte innholdet og reglene for et arbeidsflytvarsel når du oppretter den aktuelle arbeidsflyten. Dette gjør du ved å velge alternativer på siden **Alternativer for arbeidsflytsvar** for arbeidsflytsvaret som representerer varslingen. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

* Varsle avsender

    For arbeidsflyter for godkjenning legger du til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også

[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)  
[Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Opprette arbeidsflyter](across-how-to-create-workflows.md)  
[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]