---
title: Feilsøk tilgang med Microsoft 365-lisenser
description: Finn ut hvordan du kan løse problemer med tilgang til Business Central med bare en Microsoft 365-lisens.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.service: dynamics-365-business-central
---

# Feilsøk tilgang med Microsoft 365-lisenser

## Feilmeldingen «Denne siden bruker data fra relaterte tabeller som du ikke har tilgang til»

### Symptomer

Når du får tilgang til en post i Teams, vises det en feilmelding i en fane eller kortdetaljer som ligner følgende:

Denne siden bruker data fra relaterte tabeller som du ikke har tilgang til. Hvis du vil arbeide med alle funksjoner på denne siden, kontakter du administratoren.

### Årsak

Du mangler mest sannsynlige objekttillatelser for tabeller som nåværende side eller post kobles til.

## Microsoft 365-tilgang er aktivert, men brukerne får en tillatelsesfeil

### Symptomer

Tilgang med Microsoft 365 er aktivert i Business Central, men brukerne får en tillatelsesfeil ved tilgang til en post.

### Årsak

Hvis du aktiverer tilgang i administrasjonssenteret for Business Central, men ikke tildeler tillatelser på siden for **lisenskonfigurasjon**, vil alle som prøver å få tilgang til Business Central-poster i Teams, ha sin brukerpost klargjort uten tillatelse for noen objekter. Business Central er sikret etter utforming: administratorer må først konfigurere hvilke data som kan åpnes i Teams. 

### Løsning

Når du tilpasser tillatelser på siden Lisenskonfigurasjon, påvirkes bare nylig opprettede brukere. Du må også tildele de manglende tillatelsene til brukere som allerede er opprettet på siden Liste over brukere. 

## Du har delt en kobling i Teams, men brukerne får en melding om at de bare kan vise data

### Symptomer

Når du deler en kobling i Teams som en Business Central-bruker, får andre feilmeldingen Når du åpner Business Central med en Microsoft 365-lisens, kan du bare vise data i Microsoft Teams.

### Årsak

Når du deler en Business Central-kobling til en Teams-nettprat eller Teams-kanaler, vil det alltid navigeres ut av Microsoft Teams der dataene ikke lenger blir tilgjengelig for en person som har Microsoft 365-lisens.

### Løsning

Når du deler sider eller poster, må du enten ta med forhåndsvisning av kobling som et kort eller dele data som en fane i nettpratvinduet eller kanalen.

## Kort fra delt kobling er minimal, og inkluderer ikke Detaljer-knapp

### Symptomer 

Når en Microsoft 365-lisensinnehaver uten en Business Central-lisens deler en Business Central-kobling i Teams, utvides den automatisk til et kort som ikke har noe nyttig informasjon, og viser bare Business Central uten noen **Detaljer**-knapp.

### Årsak

Brukere som har en Microsoft 365-lisens, men ingen Business Central-lisens kan dele koblinger som kort. Hvis brukeren har Business Central-appen for Teams installert og limer inn en kobling i skriveområdet, vises bare et minimalt kort. 

## Se også

[Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurer tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-setup.md)  
[Business Central- og Microsoft Teams-integrering](across-teams-overview.md)
[Deling av Business Central-poster og -sidekoblinger i Microsoft Teams](across-working-with-teams.md)  
[Feilsøk Teams-integrering](admin-teams-troubleshooting.md)  