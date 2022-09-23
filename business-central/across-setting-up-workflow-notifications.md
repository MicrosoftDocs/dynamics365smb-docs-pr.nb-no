---
title: Konfigurering av arbeidsflytvarsler
description: Denne artikkelen forteller deg hvordan du konfigurerer arbeidsflytvarsler for å varsle en bruker om at det har oppstått en hendelse som de må reagere på. Det kreves et arbeidsflytsvar.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9405af9c52b17ab34fded263692e3294ed8aaf11
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533971"
---
# <a name="workflow-notifications"></a>Arbeidsflytvarslinger

Konfigurere arbeidsflytene slik at de automatisk varsler brukere når de må det må utføres handlinger for et trinn i arbeidsflyten. Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse de må gjøre noe med.

Du kan for eksempel angi at bruker 2, godkjenningsbrukeren, mottar et varsel hver gang bruker 1 ber om godkjenning for en ny post. I neste arbeidsflyttrinn varsles bruker 3 etter at bruker 2 godkjenner posten for å starte en relatert behandling av posten. Med arbeidsflyttrinn for godkjenning er hvert varsel knyttet til en godkjenningsoppføring. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
> Standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter varsler som e-post og interne merknader.  

> [!IMPORTANT]  
> Alle arbeidsflytvarsler sendes via en jobbkø. Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler, og at det er merket av for **Start automatisk fra server**. Hvis du vil ha mer informasjon, kan du se [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Konfigurer varslinger

Du kan definere ulike aspekter ved arbeidsflytvarsler på følgende steder:  

* Godkjenner-varsling

    For arbeidsflyter for godkjenning angir du mottakerne av arbeidsflytvarsler ved å fylle en linje på siden **Brukeroppsett for godkjenning** for hver bruker som tar del i arbeidsflyten.  

    Hvis for eksempel bruker 2 er angitt i **Godkjenner-ID**-feltet på linjen for bruker 1, sendes varselet om godkjenningsforespørsel til bruker 2. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  
* Tidsplaner for varsling

    Du kan angi når og hvordan brukere skal motta arbeidsflytvarsler, ved å fylle ut siden **Tidsplan for varsling** for hver arbeidsflytbruker. Hvis du vil ha mer informasjon, kan du se [Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Tilpass e-postvarslingene

    Hvis du vil, kan du tilpasse innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Hvis du vil bruke e-post som varslingsmetode, må du konfigurere e-post for både avsenderen og mottakeren i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).

* Svaralternativer

    Du definerer det bestemte innholdet og reglene for et arbeidsflytvarsel når du oppretter den aktuelle arbeidsflyten. Velg tilpasningsalternativene på siden **Arbeidsflytsvar** for arbeidsflytsvaret som representerer varslingen. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md#to-create-a-workflow).  

* Varsle avsender

    For arbeidsflyter for godkjenning legger du til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist. Hvis du vil ha mer informasjon, kan du se trinn 9 i [Opprette arbeidsflyter](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## <a name="see-also"></a>Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurer arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)  
[Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Opprette arbeidsflyter](across-how-to-create-workflows.md)  
[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
