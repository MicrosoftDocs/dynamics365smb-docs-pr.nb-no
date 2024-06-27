---
title: Kjøre oppgaver i bakgrunnen og gjentakende
description: Konfigurer synkronisering av data mellom Business Central og Shopify i bakgrunnen.
ms.date: 05/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
ms.custom: bap-template
---

# Kjør oppgaver i bakgrunnen

Det er effektivt å kjøre enkelte oppgaver samtidig og på en automatisk måte. Du kan utføre slike oppgaver i bakgrunnen og kan også angi en tidsplan når du vil at disse oppgavene skal kjøres automatisk. To moduser er støttet for å kjøre oppgaver i bakgrunnen:

- Manuelt utløste oppgaver planlegges umiddelbart via **prosjektkøposter**.
- Regelmessige aktiviteter planlegges i **prosjektkøposter**.

## Kjør oppgaver i bakgrunnen for en bestemt butikk

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil kjøre synkronisering i bakgrunnen for, for å åpne siden **Shopify-butikkort**.
3. Slå på vekslebryteren **Tillat bakgrunnssynkroniseringer**.

Når synkroniseringshandlingen starter, blir du bedt om å vente i stedet for å kjøre en oppgave i forgrunnen. Når den fullføres, kan du fortsette til neste handling. Oppgaven er opprettet som **jobbkøpost** og starter umiddelbart.

## Slik planlegger du regelmessige oppgaver

Du kan planlegge at følgende regelmessige aktiviteter skal utføres på en automatisk måte. Finn ut mer om å planlegge oppgaver på [Prosjektkø](../admin-job-queues-schedule-tasks.md).

|Oppgave|Objekt|
|------|------------|
|**Synkroniser ordrer fra Shopify**|Rapport 30104 Synkroniser ordrer fra Shopify|
|**Behandle Shopify-ordrer**|Rapport 30103 Shopify opprett salgsordrer|
|**Synkroniser leveringer til Shopify**|Rapport 30109 Synkroniser forsendelse til Shopify|
|**Synkroniser produkter eller priser**|Rapport 30108 Shopify synkroniser produkter|
|**Synkroniser lager**|Rapport 30102 Synkroniser lager til Shopify|
|**Synkroniser bilder**|Rapport 30107 Shopify synkroniser bilder|
|**Synkroniser kunder**|Rapport 30100 Shopify synkroniser kunder|
|**Synkroniser selskaper**|Rapport 30114 Shopify synkroniser selskaper (B2B)|
|**Synkroniser betalinger**|Rapporter 30105 Shopify synkroniser betalinger|
|**Synkroniser kataloger**|Rapport 30115 Shopify synkroniser kataloger (B2B)|
|**Synkroniser katalogpriser**|Rapport 30116 Shopify synkroniser katalogpriser (B2B)|

> [!NOTE]
> Noen elementer kan bli oppdatert av flere oppgaver. For eksempel når du importerer ordrer, avhengig av innstillingen på siden **Shopify-butikkort**, kan systemet også importere og oppdatere kunde- eller produktdata. Husk å bruke den samme prosjektkøkategorien for å unngå konflikter.
>
> Bruk handlingen **Rapportforespørselsside** til å definere filtre. Du kan for eksempel angi at du bare importerer bestillinger når statusen er **Fullt betalt**.

Andre oppgaver som kan være nyttige ved automatisering av ytterligere behandling av salgsdokumenter:

- Rapport 297 Salgsfakturaer – massebokfør
- Rapport 296 Salgsordrer – massebokfør

Du kan bruke feltet **Shopify-ordrenr.** til å identifisere salgsdokumenter som ble importert fra Shopify.

Hvis du vil lære mer om bokføring av ordrer i et parti, går du [Slik oppretter du en jobbkøpost for massebokføring av ordrer](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## Slik kontrollerer du statusen til synkroniseringen

I rollesenteret **Forretnings** inneholder delen **Shopify-aktiviteter** flere bunke-ikoner som kan hjelpe deg med å finne ut om det er problemer med Shopify-koblingen.

- **Ikke-tildelte kunder**: Shopify-kunder importeres, men er ikke knyttet til en tilsvarende kundeoppføring i [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Ikke-tildelte produkter** – Shopify-produkter importeres, men er ikke knyttet til en tilsvarende vareoppføring i [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Ubehandlede ordrer**: Shopify-ordrer importeres, men salgsdokumenter i [!INCLUDE [prod_short](../includes/prod_short.md)] ble ikke opprettet, ofte på grunn av produkter eller kunder som ikke er tildelt.
- **Ubehandlede forsendelser**: Bokførte salgsforsendelser som kommer fra Shopify-ordrer, synkroniseres ikke med Shopify.
- **Forsendelsesfeil**: Shopify-koblingen kunne ikke synkronisere bokførte salgsforsendelser med Shopify.
- **Synkroniseringsfeil**: Det er mislykkede prosjektkøoppføringer relatert til synkronisering med Shopify.

## Se også

[Kom i gang med Shopify-koblingen](get-started.md)  
