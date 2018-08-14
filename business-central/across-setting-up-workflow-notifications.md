---
title: Konfigurere arbeidsflytvarsler | Microsoft-dokumentasjon
description: "Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren. I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: 1a8fd4f75fc1562985412b7e478066aa425c9425
ms.contentlocale: nb-no
ms.lasthandoff: 07/09/2018

---
# <a name="setting-up-workflow-notifications"></a>Konfigurere arbeidsflytvarsler
Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med. I ett arbeidsflyttrinn kan hendelsen for eksempel være at bruker 1 ber om godkjenning av en ny post, og svaret er at det er sendt en melding til bruker 2, godkjenneren. I det neste arbeidsflyttrinnet kan hendelsen være at bruker 2 godkjenner posten, og svaret er at det er sendt en melding til bruker 3 om å starte en relatert behandling av den godkjente posten. Hver varsling er knyttet til en godkjenningspost for arbeidsflyttrinn som omhandler godkjenning. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
>  Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter varsler som e-post og interne merknader.  

> [!IMPORTANT]  
>  Alle arbeidsflytvarsler sendes via en jobbkø. Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler, og at det er merket av for **Start automatisk fra server**. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

Du kan definere ulike aspekter ved arbeidsflytvarsler på følgende steder:  

1.  For arbeidsflyter for godkjenning angir du mottakerne av arbeidsflytvarsler ved å fylle en linje i vinduet **Brukeroppsett for godkjenning** for hver bruker som tar del i arbeidsflyten. Hvis for eksempel bruker 2 er angitt i **Godkjenner-ID**-feltet på linjen for bruker 1, sendes varselet om godkjenningsforespørsel til bruker 1. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  
2.  Du kan angi når og hvordan brukere skal motta arbeidsflytvarsler, ved å fylle ut vinduet **Tidsplan for varsling** for hver arbeidsflytbruker. Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Du definerer det generelle innholdet og oppsettet på varsler, inkludert varsler om forfalte arbeidsflytsvar, ved å definere varslingsmaler i vinduet **Varslingsmaler**. Du kan bruke standardmalene som følger med [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4.  Du definerer det bestemte innholdet og reglene for et arbeidsflytvarsel når du oppretter den aktuelle arbeidsflyten. Dette gjør du ved å velge alternativer i vinduet **Alternativer for arbeidsflytsvar** for arbeidsflytsvaret som representerer varslingen. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også  
 [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)   
 [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)   
 [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Opprette arbeidsflyter](across-how-to-create-workflows.md)   
 [Behandle varslingsmaler](across-how-to-manage-notification-templates.md)   
 [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)   
 [Konfigurere e-post](admin-how-setup-email.md)   
 [Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Arbeidsflyt](across-workflow.md)   

