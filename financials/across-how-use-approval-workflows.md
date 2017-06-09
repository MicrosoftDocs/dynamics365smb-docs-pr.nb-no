---
title: Bruke arbeidsflyter for godkjenning| Microsoft-dokumentasjon
description: Bruke arbeidsflyter for godkjenning
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ed08fdb7f78c9f6c338e287cd4ef42d7ce0cb72c
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-approval-workflows"></a>Bruke arbeidsflyter for godkjenning
Når en post, for eksempel et kjøpsdokument eller et kundekort, må godkjennes av en person i organisasjonen, kan du sende en forespørsel om godkjenning som en del av en arbeidsflyt. Avhengig av hvordan arbeidsflyten er konfigurert, gir den riktige godkjenneren deretter beskjed om at posten krever godkjenning.

Du setter opp arbeidsflyter for godkjenning i **Arbeidsflyt**-vinduet.

Kjernearbeidsflyter for godkjenning av kjøpsdokumenter, salgsdokumenter, betalingskladder, kundekort og varekortene, er klar til å starte som assistert oppsett. Hvis du vil ha mer informasjon, kan du se [Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Slik ber du om godkjenning av en post:
Oppgavene nedenfor utføres av en godkjenningsbruker.

1. I vinduet som viser posten, velger du handlingen **Send godkjenningsforespørsel**.
2. Hvis du vil se alle godkjenningsforespørsler, i øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Godkjenningsforespørselsposter**, og deretter velger du den beslektede koblingen.

Statusen for godkjenningsposten oppdateres fra **Opprettet** til **Åpen**. Statusen for posten, for eksempel en kjøpsfaktura, oppdateres fra **Åpen** til **Venter på godkjenning** og forblir låst for behandling til alle godkjennerne har godkjent posten.

Når godkjenneren har godkjent posten, blir statusen endret til **Frigitt**. Du kan deretter fortsette på oppgavene med posten.

## <a name="to-cancel-requests-for-approval"></a>Avbryte forespørsler om godkjenning
Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Det kan hende at en kunde vil endre en bestilling etter at den er sendt til godkjenning. I så fall kan du annullere godkjenningsprosessen og foreta de nødvendige endringene i bestillingen før du ber om godkjenning igjen.

- I vinduet som viser posten, velger du handlingen **Annuller godkjenningsforespørsel**.

Når godkjenningsforespørselen er annullert, endres statusen for den relaterte godkjenningsposten til **Annullert**. Statusen for posten oppdateres fra **Venter på godkjenning** til **Åpen**. Godkjenningsprosessen kan deretter startes på nytt.

## <a name="to-make-minor-changes-to-approved-records"></a>Foreta mindre endringer i godkjente poster
Hvis du vil gjøre en liten endring i en post etter at den er godkjent, kan du åpne posten på nytt, foreta endringen og deretter frigi den. Du kan foreta mindre endringer med knappene **Åpne på nytt** og **Frig**.

1. Åpne vinduet som viser posten, for eksempel en kjøpsfaktura, og velg deretter handlingen **Åpne på nytt**.

    **Dokumentstatus**-feltet endres til **Åpen**.
2. Gjør de nødvendige endringene i posten, for eksempel adressen til leverandøren.
3. Velg handlingen **Frigi**.

Når du åpner kildeoppføringen på nytt, forblir statusen for den relaterte godkjenningsposten Godkjent i vinduet **Godkjenningsposter**.

## <a name="to-approve-or-reject-requests-for-approval"></a>Godkjenne eller avvise forespørsler om godkjenning
Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Du kan behandle forespørsler om godkjenning i vinduet **Forespørsler å godkjenne**, for eksempel for å godkjenne flere forespørsler samtidig. Du kan også behandle hver forespørsel på den relaterte posten, for eksempel vinduet **Kjøpsfaktura**, ved å velge koblingen i meldingen du mottar.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forespørsler å godkjenne**, og deretter velger du den beslektede koblingen.
2. Velg én eller flere linjer for posten eller postene du vil godkjenne eller avvise.
3. Velg handlingen **Godkjenn**, **Avvis** eller **Deleger**.

Når en post er godkjent eller avvist, endres godkjenningsstatusen i **Status**-feltet til **Godkjent** eller **Avvist**.

Hvis det er angitt et godkjennerhierarki, er poststatusen **Venter på godkjenning** til alle godkjennerne har godkjent posten. Poststatusen endres deretter til **Frigitt**.

Samtidig endres godkjenningsstatusen fra **Opprettet** til **Åpen** så snart en godkjenningsforespørsel for posten er opprettet. Hvis forespørselen avvises, endres godkjenningsstatusen til **Avvist**. Statusen forblir **Åpen** eller **Avvist** til alle godkjennerne har godkjent forespørselen.

## <a name="to-delegate-requests-for-approval"></a>Delegere forespørsler om godkjenning
Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Hvis du vil hindre at dokumenter hoper seg opp eller blokkerer arbeidsflyten på andre måter, kan godkjenner og godkjenningsadministrator delegere en godkjenningforespørsel til en stedfortredende godkjenner. Stedfortrederen kan enten være en angitt stedfortreder, den direkte godkjenneren eller godkjenningsadministratoren, i denne rekkefølgen. Du bruker vanligvis denne funksjonen hvis en godkjenner ikke er på kontoret og ikke kan godkjenne forespørsler før forfallsdatoen.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forespørsler å godkjenne**, og deretter velger du den beslektede koblingen.
2. Velg én eller flere linjer for godkjenningsforespørsler du vil delegere til en stedfortredende godkjenner, og velg deretter handlingen **Deleger**.

Et varsel om å godkjenne forespørselen sendes til stedfortredende godkjenner.

## <a name="to-manage-overdue-approval-requests"></a>Håndtere forfalte godkjenningsforespørsler
Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Med jevne mellomrom må du vil påminne brukere av arbeidsflyt for godkjenning om forfalte godkjenningsforespørsler som de må reagere på. Du bruker funksjonen **Send varsler om forfalte godkjenninger** til dette.

Funksjonen **Send varsler om forfalte godkjenninger** kontrolleres om det finnes åpne godkjenningsforespørsler som er forfalt. Hver godkjenner som har minst én forfalt godkjenningspost, mottar en varsling med listen over alle forfalte godkjenningsforespørsler. Varslingen sendes også til godkjenneren og alle som ber om forfalte godkjenninger. Dette hjelper hvis den forfalte godkjenningsposten må delegeres til en stedfortreder.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Forfalte godkjenningsforespørsler**, og deretter velger du den beslektede koblingen.
2. I vinduet **Forfalte godkjenningsforespørsler** velger du handlingen **Send varsler for forfalte godkjenning**.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)    
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

