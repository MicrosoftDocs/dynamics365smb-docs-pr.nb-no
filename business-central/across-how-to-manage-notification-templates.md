---
title: Administrere varslingsmaler | Microsoft-dokumentasjon
description: Varslinger sendes til brukere i arbeidsflyten for å varsle dem om trinn de må utføre, eller for å informere om statusen for trinn i arbeidsflyten. Du definerer hvem som mottar varsel og når, ved å konfigurere godkjenning av brukere, brukernes varslingstidsplan og svarene i arbeidsflyten for å definere varslingsmottakeren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: across-how-to-specify-when-and-how-to-receive-notifications
ms.openlocfilehash: 562664ad0fd443c3363d103572022e6d819ed357
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "914281"
---
# <a name="manage-notification-templates"></a>Behandle varslingsmaler
Varslinger sendes til brukere i arbeidsflyten for å varsle dem om trinn de må utføre, eller for å informere om statusen for trinn i arbeidsflyten. Du definerer hvem som mottar varsel og når, ved å konfigurere godkjenning av brukere, brukernes varslingstidsplan og svarene i arbeidsflyten for å definere varslingsmottakeren. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md).  

 Varslinger er basert på maler som definerer innholdet i og oppsettet av meldingen. Du kan eksportere innholdet i en varslingsmal, redigere den, og deretter importere til samme eller en ny varslingsmal. Dette er beskrevet i følgende fremgangsmåter.  

 Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder tre varslingmaler, én for å informere om forespørsler om godkjenning, én for å varsle om nye poster og én for å varsle om forfalte godkjenningsforespørsler. Tre forhåndsdefinerte varslingsmaler støtter **E-post** og **Notat** som varslingsmetode. Hvis du vil vise innholdet i de tre varslingsmalene, kan du se delen "Innhold i varslingsmalene" i dette emnet.

## <a name="to-create-a-new-notification-template"></a>Slik oppretter du en ny varslingsmal:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varslingsmaler**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny** på siden **Varslingsmaler**.  
3.  Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Identifiser varslingsmalen.|  
    |**Beskrivelse**|Beskriv varslingsmalen.|  
    |**Varslingsmetode**|Angi om varslingen sendes som en e-post eller et notat.|  
    |**Type**|Angi forretningsprosessen som varslingen skal brukes for.<br /><br /> Velg én av følgende typer:<br /><br /> -   **Godkjenning** angir at malen brukes til å varsle brukere i arbeidsflyter for godkjenning.<br />-   **Ny post** angir at malen skal varsle godkjennere når en ny post, for eksempel et kundekort, trenger deres godkjenning.<br />-   **Forfalt** angir at malen brukes til å varsle brukere om forfalte godkjenningsforespørsler.|  
    |**Standard**|Angi om varslingsmalen vil bli brukt som standard.|  

## <a name="to-modify-a-notification-template"></a>Slik endrer du en varslingsmal:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varslingsmaler**, og velg deretter den relaterte koblingen.  
2.  På siden **Varslingsmaler** velger du varslingsmalen du vil endre.  
3.  Velg **Eksporter malinnhold**.  
4.  På **Eksporter fil**-siden velger du **Lagre**-knappen, og deretter gir du navn til HTML-filen og lagrer den på en passende plassering.  
5.  Høyreklikk filen, velg **Åpne med**, og velg deretter det aktuelle programmet.  

    > [!NOTE]  
    >  Innhold for varslingsmaler av typen E-post er i HTML-format. Innhold for varslingsmaler av typen Notat er i TXT-format.  
6.  Rediger innholdet i varslingsmalen ved å legge til, endre eller fjerne parametervariabler for å definere det ønskede innholdet, og lagre det. Hvis du vil ha mer informasjon, se delen "Innhold i varslingsmalene".  

    Fortsett med å importere det endrede innholdet tilbake til den samme eller en ny varslingsmal.  
7.  Hvis du vil endre varslingsmalen som du eksporterte, velger du malen du valgte i trinn 2, på siden **Varslingsmaler**.  

    Hvis du vil importere det endrede malinnholdet til en ny varslingsmal, kan du eventuelt følge fremgangsmåten for å opprette en ny varslingsmal, og deretter velge den nye varslingsmalen.  
8.  Velg **Importer malinnhold**.  
9. Hvis du endrer en eksisterende varslingsmal, velger du **Ja**-knappen på meldingen om overskriving av den eksisterende malen.  
10. På siden **Velg en fil for import** velger du HTML-filen som du endret i trinn 6, og velger deretter **Åpne**-knappen.  

Den eksisterende eller nye varslingsmalen på siden **Varslingsmaler** er nå oppdatert med det endrede innholdet.  

### <a name="content-of-the-notification-templates"></a>Innhold i varslingsmalene  
De tre varslingsmaltypene **Ny post**, **Godkjenning** og **Forfalt** har forskjellig innhold.  

Parameterverdier settes automatisk inn i varslinger i henhold til typen varslingsmal.  

#### <a name="new-record"></a>Ny post  
 ![NAV&#95;melding&#95;mal&#95;ny&#95;post&#95;type](media/nav_notification_template_new_record.png "NAV_notification_template_new_record")  

#### <a name="approval"></a>Godkjenning  
 ![NAV&#95;varsel&#95;mal&#95;godkjenning&#95;type](media/nav_notification_template_approval_type.png "NAV_notification_template_approval_type")  

#### <a name="overdue"></a>Forfalt  
 ![NAV&#95;varsel&#95;forfalt&#95;type](media/nav_notification_overdue_type.png "NAV_notification_overdue_type")  

## <a name="see-also"></a>Se også  
 [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)   
 [Konfigurere e-post](admin-how-setup-email.md)   
 [Konfigurere arbeidsflytbrukere](across-how-to-set-up-workflow-users.md)   
 [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)   
 [Opprette arbeidsflyter](across-how-to-create-workflows.md)   
 [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)   
 [Arbeidsflyt](across-workflow.md)   
