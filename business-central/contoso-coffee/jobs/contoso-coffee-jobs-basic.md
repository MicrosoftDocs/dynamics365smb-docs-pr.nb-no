---
title: Gjennomgang av grunnleggende jobber
description: Denne artikkelen guider deg gjennom flere sentrale prosesser i prosjektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-of-basic-jobs"></a>Gjennomgang av grunnleggende jobber

Denne gjennomgangen viser flere kjerneprosesser:

- Legg til prosjektaktiviteter i prosjekter
- Registrer utgifter for tid og materiale i et prosjekt
- Fakturer et prosjekt

## <a name="adding-a-project-task"></a>Legg til en prosjektoppgave

### <a name="scenario"></a>Scenario

Simon, prosjektlederen, ønsker å bruke minst mulig tid på å lære kunden å bruke espressomaskinen. Simon ønsker å bruke en annen oppgave i prosjektet for å installere en kommersiell maskin på stedet.

### <a name="steps"></a>Trinn

1. Opprett prosjektoppgaven.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
    2. Velg jobb *J00010*.
    3. I området **Områder** velger du handlingen **Ny linje** og angir deretter følgende verdier:
 
    |Prosjektoppgavenr.|Description|Prosjektoppgavetype|
    |------------|-----------|-------------|  
    |220|Opplæring i kunder|Bokføring|

2. Rykk inn prosjektoppgavene.
   1. Finn handlingen **Rykk inn prosjektoppgaver** i Oppgaver-området.
   2. Bekreft at du vil rykke inn oppgaver ved å velge **Ja**.

### <a name="results"></a>Resultater

 - Nå kan tid og utgifter registreres i den nye prosjektoppgaven

## <a name="record-time-and-material-expenses-to-a-project"></a>Registrere tids- og materialutgifter i et prosjekt

### <a name="scenario-1"></a>Scenario

Edgin, teknikeren som installerer maskinen, må registrere tiden sin og materialene som brukes under installasjonen til oppgaven for fakturering. Edgin har allerede lagt til reise og materialer, og må nå legge til tid for opplæring av personalet i hvordan de skal bruke maskinen.

### <a name="steps-1"></a>Trinn

1. Opprett de ekstra prosjektkladdelinjene.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder** og velg den relaterte koblingen.  
    2. Velg kjøreselen *CONTOSO*. Du ser flere linjer med ressurs- og varetyper som gjenspeiler tiden (for teknikeren og kjøretøyet) og materialene (maskinen og forsyningene) som er brukt.
    3. Opprett en ny linje, og skriv inn følgende verdier:
 
    |Prosjektnr.|Prosjektoppgavenr.|Type|Nr.|Description|Antall|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressurs|EDGIN|Kundeopplæring|1|

2. Bokfør tid og utgifter.
   1. Velg handlingen **Bokfør**.
   2. Bekreft at du vil bokføre linjene ved å velge **Ja**.

### <a name="results-1"></a>Resultater

- Prosjektposter og ressursposter av typen *Forbruk* opprettes
- Vareposter opprettes for å justere lagerbeholdningen negativt.
- På prosjektkortet gjenspeiler kostnadene og prisene i oppgaveområdet de nye saldoene som venter på å bli fakturert
- På prosjektkortet gjenspeiler faktaboksen Prosjektdetaljer totalsummene for prisene.

## <a name="creating-a-sales-invoice-for-a-project"></a>Opprett en salgsfaktura for et prosjekt

### <a name="scenario-2"></a>Scenario

Simon må opprette og bokføre en faktura som skal sendes til kunden med tiden og utgiftene fra prosjektet.

### <a name="steps-2"></a>Trinn

1. Opprette salgsfakturaen.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.  
    2. I listen over prosjekter velger du handlingen **Opprett salgsfaktura for prosjekt**.
    3. Angi feltet **Prosjektnummer** til *J00010*.
    4. Velg **OK** for å generere salgsfakturaen. Du mottar en bekreftelse på hvor mange fakturaer som er generert.

2. Bokfør faktura for tid og utgifter.

   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
   2. Velg den siste fakturaen for å åpne den for gjennomgang.
   3. Velg handlingen **Bokfør**.

### <a name="results-2"></a>Resultater

- Prosjektposter og ressursposter av typen *Salg* opprettes.
- På prosjektkortet gjenspeiler kostnadene og prisene i oppgaveområdet de nye saldoene.
- På prosjektkortet gjenspeiler faktaboksen Prosjektdetaljer totalsummene for prisene i delen Fakturert pris
