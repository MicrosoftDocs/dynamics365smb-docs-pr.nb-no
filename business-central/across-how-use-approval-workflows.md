---
title: Godkjenne eller avvise dokumenter i arbeidsflyter
description: 'Be om, avvise eller delegere en godkjenning, for eksempel av et kjøps- eller salgsdokument, som en del av en arbeidsflyt.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: edupont
---
# <a name="how-to-use-approval-workflows" />Bruk arbeidsflyter for godkjenning

Når en post, for eksempel et kjøpsdokument eller et kundekort, må godkjennes av en person i organisasjonen, kan du sende en forespørsel om godkjenning som en del av en arbeidsflyt. Avhengig av hvordan arbeidsflyten er konfigurert, gir den riktige godkjenneren deretter beskjed om at posten krever godkjenning.

Du setter opp arbeidsflyter for godkjenning på **Arbeidsflyt**-siden. Du må også definere godkjenningsbrukere, inkludert eventuelle relevante beløpsgrenser, på siden **Brukeroppsett for godkjenning**. Finn ut mer under [Definer godskjenningsarbeidsflyter](across-set-up-workflows.md).  

I tillegg til godkjenningsarbeidsflytene som beskrives i denne artikkelen, kan du utføre diverse andre arbeidsflytoppgaver. Finn ut mer under [Bruk godkjenningsarbeidsflyter](across-use-workflows.md).

Arbeidsflyter for godkjenning av kjøpsdokumenter, salgsdokumenter, betalingskladder, kundekort og varekort er klar til å starte som veiledninger. Finn ut mer under [Bli klar til å gjøre forretninger](ui-get-ready-business.md).

## <a name="request-a-record-approval" />Be om en oppføringsgodkjenning

Oppgavene nedenfor utføres av en godkjenningsbruker.

1. På siden som viser posten, velger du handlingen **Send godkjenningsforespørsel**.
2. Hvis du vil se alle godkjenningsforespørslene, velger du ikon ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Godkjenningsforespørselsposter**, og velg deretter den relaterte koblingen.  

Statusen for godkjenningsposten oppdateres fra **Opprettet** til **Åpen**. Statusen for posten, som en kjøpsfaktura, oppdateres fra **Åpen** til **Venter på godkjenning** og forblir låst for behandling til alle godkjennerne har godkjent posten.

Når alle påkrevde godkjennerne har godkjent posten, blir statusen endret til **Frigitt**. Du kan deretter fortsette å arbeide med posten.

## <a name="cancel-approval-requests" />Annuller godkjenningsforespørsler

Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Det kan hende at en kunde vil endre en bestilling etter at den er sendt til godkjenning. I så fall kan du annullere godkjenningsprosessen, foreta de nødvendige endringene i bestillingen og be om godkjenning igjen.

- På siden som viser posten, velger du handlingen **Annuller godkjenningsforespørsel**.

Når godkjenningsforespørselen er annullert, endres statusen for den relaterte godkjenningsposten til **Annullert**. Statusen for posten oppdateres fra **Venter på godkjenning** til **Åpen**. På dette punktet kan godkjenningsprosessen startes på nytt.

## <a name="approve-or-reject-approval-requests" />Godkjenn eller avvis godkjenningsforespørsler

Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Du kan behandle forespørsler om godkjenning på siden **Forespørsler å godkjenne**, inkludert å godkjenne flere forespørsler samtidig. Du kan også godkjenne individuelle poster ved å velge koblingen i varselet du mottar.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Forespørsler å godkjenne**, og velg deretter den relaterte koblingen.
2. Velg en eller flere linjer for postene du vil godkjenne eller avvise.
3. Velg handlingen **Godkjenn**, **Avvis** eller **Deleger**.

Når en post er godkjent eller avvist, endres godkjenningsstatusen i **Status**-feltet til henholdsvis **Godkjent** eller **Avvist**.

Hvis det er angitt et godkjennerhierarki, er poststatusen **Venter på godkjenning** til alle de forespurte godkjennerne har godkjent posten. Poststatusen endres deretter til **Frigitt**.

Samtidig endres godkjenningsstatusen fra **Opprettet** til **Åpen** så snart en godkjenningsforespørsel for posten er opprettet. Hvis forespørselen avvises, endres godkjenningsstatusen til **Avvist**. Statusen forblir **Åpen** eller **Avvist** til alle godkjennerne har godkjent forespørselen.

## <a name="delegate-approval-requests" />Deleger godkjenningsforespørsler

Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Hvis du vil hindre at poster hoper seg opp eller blokkerer arbeidsflyten på andre måter, kan godkjenner og godkjenningsadministrator delegere en godkjenningsforespørsel til en stedfortredende godkjenner. Stedfortrederen kan enten være en angitt stedfortreder, den direkte godkjenneren eller godkjenningsadministratoren, i denne rekkefølgen. Du bruker vanligvis denne funksjonen hvis en godkjenner ikke er tilgjengelige eller ikke kan godkjenne forespørsler før forfallsdatoen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Forespørsler å godkjenne**, og velg deretter den relaterte koblingen.
2. Velg en eller flere linjer for godkjenningsforespørsler du vil delegere til en stedfortredende godkjenner, og velg deretter handlingen **Deleger**.

Et varsel om å godkjenne forespørselen sendes til stedfortredende godkjenner.

## <a name="manage-overdue-approval-requests" />Håndter forfalte godkjenningsforespørsler

Oppgavene nedenfor utføres av en godkjenningsbruker med godkjennerrettigheter.

Med jevne mellomrom må du minne om å godkjenningsarbeidsflytbrukere om forfalte godkjenningsforespørsler. Du bruker funksjonen **Send varsler om forfalte godkjenninger** til dette.

Funksjonen **Send varsler om forfalte godkjenninger** kontrolleres om det finnes åpne godkjenningsforespørsler som er forfalt. Hver godkjenner med minst én forfalt godkjenningspost, mottar en varsling med listen over alle forfalte godkjenningsforespørsler. Varslingen sendes også til godkjenneren og alle som ber om forfalte godkjenninger. Dette siste trinnet hjelper hvis den forfalte godkjenningsposten må delegeres til en stedfortreder.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Forfalte godkjenningsforespørsler**, og velg deretter den relaterte koblingen.
2. På siden **Forfalte godkjenningsforespørsler** velger du handlingen **Send varsler for forfalte godkjenning**.

## <a name="see-related-microsoft-trainingtrainingmodulesuse-approval-workflows" />Se relatert [Microsoft-opplæring](/training/modules/use-approval-workflows/)

## <a name="see-also" />Se også

[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  
[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Salg](sales-manage-sales.md)  
[Inngående dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
