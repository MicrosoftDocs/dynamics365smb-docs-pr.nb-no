---
title: Kjør oppgaver i bakgrunnen og gjentakende
description: Konfigurer synkronisering av data mellom Business Central og Shopify i bakgrunnen.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# Kjør oppgaver i bakgrunnen

Det er effektivt å kjøre enkelte oppgaver samtidig og på en automatisk måte. Du kan utføre slike oppgaver i bakgrunnen og kan også angi en tidsplan når du vil at disse oppgavene skal kjøres automatisk. To moduser er støttet for å kjøre oppgaver i bakgrunnen:

- Manuelt utløste oppgaver planlegges umiddelbart via **prosjektkøposter**.
- Regelmessige aktiviteter planlegges i **prosjektkøposter**.

## Kjør oppgaver i bakgrunnen for en bestemt butikk

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn navnet på **Shopify-butikken**. Velg butikknavnet fra oversikten.
2. Velg butikken du vil synkronisere varer med for å åpne siden **Shopify-butikkort**.
3. Aktiver vekslebryteren **Tillat bakgrunnssynkroniseringer**.

Når synkroniseringshandlingen utløses, blir du bedt om å vente i stedet for en oppgave som kjører i forgrunnen. Når det er fullført, kan du fortsette til neste handling. Oppgaven er opprettet som en **prosjektkøpost** og starter direkte i en ikke-blokkerende måte.

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
|**Synkroniser betalinger**|Rapporter 30105 Shopify synkroniser betalinger|

> [!NOTE]
> Noen varer kan bli oppdatert av flere oppgaver, for eksempel når du importerer ordrer, avhengig av innstillingen på **Shopify-butikkortet**, kan systemet også importere og oppdatere kunde- eller produktdata. Husk å bruke den samme prosjektkøkategorien for å unngå konflikter.

## Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
