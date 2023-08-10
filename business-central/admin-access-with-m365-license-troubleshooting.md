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
---

# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Feilsøk tilgang med Microsoft 365-lisenser

## <a name="this-page-uses-data-from-related-tables-that-you-do-not-have-access-to-error-message"></a>Feilmeldingen «Denne siden bruker data fra relaterte tabeller som du ikke har tilgang til»

### <a name="symptoms"></a>Symptomer

Når du får tilgang til en post i Teams, vises det en feilmelding i en fane eller kortdetaljer som ligner følgende:

Denne siden bruker data fra relaterte tabeller som du ikke har tilgang til. Hvis du vil arbeide med alle funksjoner på denne siden, kontakter du administratoren.

### <a name="cause"></a>Årsak

Du mangler mest sannsynlige objekttillatelser for tabeller som nåværende side eller post kobles til.

## <a name="microsoft-365-access-has-been-enabled-but-users-get-a-permission-error"></a>Microsoft 365-tilgang er aktivert, men brukerne får en tillatelsesfeil

### <a name="symptoms-1"></a>Symptomer

Tilgang med Microsoft 365 er aktivert i Business Central, men brukerne får en tillatelsesfeil ved tilgang til en post.

### <a name="cause-1"></a>Årsak

Hvis du aktiverer tilgang i administrasjonssenteret for Business Central, men ikke tildeler tillatelser på siden for **lisenskonfigurasjon**, vil alle som prøver å få tilgang til Business Central-poster i Teams, ha sin brukerpost klargjort uten tillatelse for noen objekter. Business Central er sikret etter utforming: administratorer må først konfigurere hvilke data som kan åpnes i Teams. 

### <a name="resolution"></a>Løsning

Når du tilpasser tillatelser på siden Lisenskonfigurasjon, påvirkes bare nylig opprettede brukere. Du må også tildele de manglende tillatelsene til brukere som allerede er opprettet på siden Liste over brukere. 

## <a name="you-shared-a-link-in-teams-but-users-get-a-message-that-they-can-only-view-data"></a>Du har delt en kobling i Teams, men brukerne får en melding om at de bare kan vise data

### <a name="symptoms-2"></a>Symptomer

Når du deler en kobling i Teams som en Business Central-bruker, får andre feilmeldingen Når du åpner Business Central med en Microsoft 365-lisens, kan du bare vise data i Microsoft Teams.

### <a name="cause-2"></a>Årsak

Når du deler en Business Central-kobling til en Teams-nettprat eller Teams-kanaler, vil det alltid navigeres ut av Microsoft Teams der dataene ikke lenger blir tilgjengelig for en person som har Microsoft 365-lisens.

### <a name="resolution-1"></a>Løsning

Når du deler sider eller poster, må du enten ta med forhåndsvisning av kobling som et kort eller dele data som en fane i nettpratvinduet eller kanalen.

## <a name="card-from-shared-link-is-minimal-and-doesnt-include-details-button"></a>Kort fra delt kobling er minimal, og inkluderer ikke Detaljer-knapp

### <a name="symptoms-3"></a>Symptomer

Når en Microsoft 365-lisensinnehaver uten en Business Central-lisens deler en Business Central-kobling i Teams, utvides den automatisk til et kort som ikke har noe nyttig informasjon, og viser bare Business Central uten noen **Detaljer**-knapp.

### <a name="cause-3"></a>Årsak

Brukere som har en Microsoft 365-lisens, men ingen Business Central-lisens kan dele koblinger som kort. Hvis brukeren har Business Central-appen for Teams installert og limer inn en kobling i skriveområdet, vises bare et minimalt kort. 

## <a name="see-also"></a>Se også

[Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md#minimum-requirements)  
[Konfigurer tilgang med Microsoft 365-lisenser](admin-access-with-m365-license-setup.md)  
[Business Central- og Microsoft Teams-integrering](across-teams-overview.md)
[Deling av Business Central-poster og -sidekoblinger i Microsoft Teams](across-working-with-teams.md)  
[Feilsøk Teams-integrering](admin-teams-troubleshooting.md)  
