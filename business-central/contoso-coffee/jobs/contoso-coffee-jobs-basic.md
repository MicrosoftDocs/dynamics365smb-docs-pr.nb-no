---
title: Gjennomgang av grunnleggende jobber
description: Denne artikkelen guider deg gjennom flere sentrale prosesser i prosjektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---
# Gjennomgang av grunnleggende jobber

Denne gjennomgangen viser flere kjerneprosesser:

- Legge til prosjektoppgaver i prosjekter
- Registrere tids- og materialutgifter i et prosjekt
- Fakturering av et prosjekt

## Legge til en prosjektoppgave i et prosjekt

### Scenario  

Simon, prosjektlederen, ønsker å bruke rekordtid på å lære opp kunden i bruk av espressomaskiner til en egen oppgave i jobben med å installere en kommersiell maskin på stedet.

### Trinn

1. Opprette prosjektoppgaven  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
    2. Velg jobb *J00010*.
    3. I området **Oppgaver** velger du handlingen **Ny linje** .  Angi følgende verdier:
 
    |Prosjektoppgavenr.|Description|Prosjektoppgavetype|
    |------------|-----------|-------------|  
    |220|Opplæring i kunder|Bokføring|

2. Rykke inn prosjektoppgaver
   1. Finn handlingen **Rykk inn prosjektoppgaver** i Oppgaver-området
   2. Bekreft at du vil rykke inn oppgaver ved å velge **Ja**.

### Resultater

 - Nå kan tid og utgifter registreres i den nye prosjektoppgaven

## Registrere tids- og materialutgifter i et prosjekt

### Scenario  

Edgin, teknikeren som installerer maskinen, må registrere tiden sin og materialene som brukes under installasjonen til oppgaven for fakturering.  Han har allerede lagt til reise og materialer, og må nå legge til tid for opplæring av personalet i hvordan de skal bruke maskinen.

### Trinn

1. Opprette ekstra prosjektoppgaver

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektkladder**, og velg deretter den relaterte koblingen.  
    2. Velg kjøreselen *CONTOSO*.  Du vil se flere linjer med ressurs- og varetyper som gjenspeiler tiden (for teknikeren og kjøretøyet) og materialene (maskinen og forsyningene) som er brukt.
    3. Opprett en ny linje. Angi følgende verdier:
 
    |Prosjektnr.|Prosjektoppgavenr.|Type|Nr.|Description|Antall|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Ressurs|EDGIN|Kundeopplæring|1|

2. Bokfør tid og utgifter
   1. Velg handlingen **Bokfør**
   2. Bekreft at du vil bokføre linjene ved å velge **Ja**.

### Resultater

 - Prosjektposter og ressursposter av typen *Forbruk* opprettes
 - Vareposter opprettes for å justere lagerbeholdningen negativt
 - På prosjektkortet gjenspeiler kostnadene og prisene i oppgaveområdet de nye saldoene som venter på å bli fakturert
 - På prosjektkortet vil faktaboksen Prosjektdetaljer gjenspeile totalsummene for prisene

## Opprette en salgsfaktura for et prosjekt

### Scenario  
Simon må opprette og bokføre en faktura som skal sendes til kunden med tiden og utgiftene fra jobben.

### Trinn
1. Opprette salgsfakturaen

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
    2. I listen over prosjekter velger du handlingen **Opprett salgsfaktura for prosjekt**.
    3. Angi **Prosjektnr.**-filteret til *J00010*.
    4. Velg **OK** for å generere salgsfakturaen.  Du vil motta en bekreftelse på hvor mange fakturaer som er generert

2. Bokfør faktura for tid og utgifter
   1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
   2. Velg den siste fakturaen for å åpne den for gjennomgang.
   3. Velg handlingen **Bokfør**.

### Resultater

 - Prosjektposter og ressursposter av typen *Salg* opprettes
 - På prosjektkortet gjenspeiler kostnadene og prisene i oppgaveområdet de nye saldoene
 - På prosjektkortet vil faktaboksen Prosjektdetaljer gjenspeile totalsummene for prisene i delen Fakturert pris
