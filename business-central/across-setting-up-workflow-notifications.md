---
title: Konfigurering av godkjenningsarbeidsflytvarsler
description: Denne artikkelen forteller deg hvordan du konfigurerer arbeidsflytvarsler for å varsle en bruker om at det har oppstått en hendelse som de må reagere på. Det kreves et arbeidsflytsvar.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Godkjenningsarbeidsflytvarsler

Konfigurere arbeidsflytene slik at de automatisk varsler brukere når de må det må utføres handlinger for et trinn i en arbeidsflyt. Mange arbeidsflytsvar omhandler å varsle brukere om at det har skjedd en hendelse som har skjedd.

Du kan for eksempel angi den slik at bruker 2, godkjenningsbrukeren, mottar et varsel hver gang bruker 1 ber om godkjenning for en ny post. I neste arbeidsflyttrinn varsles bruker 3 og kan begynne en relatert behandling av oppføringen etter at bruker 2 godkjenner posten. Med arbeidsflyttrinn for godkjenning er hvert varsel knyttet til en godkjenningsoppføring. Finn ut mer under [Arbeidsflyt](across-workflow.md).  

> [!NOTE]  
> Standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] støtter varsler i e-post eller som interne merknader.  

> [!IMPORTANT]  
> Alle arbeidsflytvarsler sendes via en jobbkø. Kontroller at jobbkøen i installasjonen er definert til å håndtere arbeidsflytvarsler, og at du har merket av for **Start automatisk fra server**. Finn ut mer under [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## Konfigurer varslinger

Du kan definere ulike aspekter ved arbeidsflytvarsler på følgende steder:  

* Godkjenner-varsling

  For arbeidsflyter for godkjenning angir du mottakerne av arbeidsflytvarsler ved å fylle ut en linje på siden **Brukeroppsett for godkjenning** for hver bruker som tar del i arbeidsflyten.  

  Hvis for eksempel bruker 2 er angitt i **Godkjenner-ID**-feltet på linjen for bruker 1, sendes varselet om godkjenningsforespørsel til bruker 2. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-approval-users.md). 
  
* Tidsplaner for varsling

  Angi når og hvordan brukere skal motta arbeidsflytvarsler, ved å fylle ut siden **Tidsplan for varsling** for hver arbeidsflytbruker. Finn ut mer under [Angi når og hvor du kan motta arbeidsflytvarsler](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Tilpass e-postvarslingene

  Hvis du vil, kan du tilpasse innholdet i e-postvarslet ved å endre rapport 1320, E-postvarsling. Finn ut mer på [Opprett og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Hvis du vil bruke e-post som varslingsmetode, må du konfigurere e-post for både avsenderen og mottakeren i [!INCLUDE [prod_short](includes/prod_short.md)]. Finn ut mer under [Definer e-post](admin-how-setup-email.md).
  
* Svaralternativer

  Definer bestemt innhold for og reglene for et arbeidsflytvarsel når du oppretter den aktuelle arbeidsflyten. Velg tilpasningsalternativene på siden **Arbeidsflytsvar** for arbeidsflytsvaret som representerer varslingen. Finn ut mer fra trinn 9 i delen [Opprett arbeidsflyter](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Varsle avsender

  For arbeidsflyter for godkjenning legger du til et trinn for arbeidsflytsvar for å varsle avsenderen når forespørselen er godkjent eller avvist. Finn ut mer fra trinn 9 i delen [Opprett arbeidsflyter](across-how-to-create-workflows.md#to-create-a-workflow).   

## Se relatert [Microsoft-opplæring](/training/modules/create-workflows/)

## Se også

[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurer arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)  
[Angi når og hvor du kan motta varsler](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Opprett og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)  
[Konfigurere e-post](admin-how-setup-email.md)  
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
