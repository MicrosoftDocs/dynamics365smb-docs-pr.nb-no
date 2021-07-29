---
title: Feilsøk tilkobling
description: Beskriver hvordan du bruker feilsøkingssiden til å identifisere og rette opp problemer med tilkobling til Business Central online.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: connectivity, troubleshooting, connection problems
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
ms.openlocfilehash: db7b9e602817d7dddcf6bce1b35ede078bd70aa0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443184"
---
# <a name="troubleshoot-connectivity-for-business-central"></a>Feilsøk tilkobling for Business Central

> **GJELDER:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Denne funksjonen er en forhåndsvisningsfunksjon. Funksjonaliteten og dokumentasjonen kan bli endret i senere utgivelser. Hvis du ønsker å bidra til dokumentasjonen basert på dine egne funn, velger du ![Rediger artikkel i GitHub.](media/github-edit-pencil.png) **Rediger** og foreslå endringer. Deretter tar vi en titt.

[!INCLUDE[prod_short](includes/prod_short.md)] Online inkluderer siden **Feilsøking av tilkobling** som du kan bruke til å identifisere problemer med tilkoblingen til den nettbaserte tjenesten. Det er flere ting som påvirker tilkoblingen til Business Central, som brannmurinnstillingene i konfigurasjonen for nettverket eller domenenavnetjenesten. På siden kan du kjøre en liste over sjekker som vil diagnostisere vanlige problemer med Business Central-tilkobling. Du kan bruke informasjonen til å prøve å løse problemene selv, eller sende den til kundestøtterepresentanten.

> [!NOTE]
> Siden **Feilsøking av tilkobling** tester ikke nettverksytelsen eller påliteligheten, som hastigheten på tilkoblingen. Den kontrollerer bare tilkoblingen til forskjellige ressurser.

## <a name="start-the-connectivity-check"></a>Start tilkoblingskontrollen 

1. Velg [denne koblingen](https://businesscentral.dynamics.com/connectivity) eller åpne nettleseren, og skriv inn følgende URL-adresse i adressen:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

2. Velg **Start kontroll** på siden **Feilsøking av tilkobling**.

    En serie sjekker kjøres, og resultatet av hver sjekk vises:

    - ![Tilkoblingskontrollen var vellykket.](media/connectivity-check.png) angir at sjekken er fullført.
    - ![Tilkoblingskontroll mislyktes.](media/connectivity-failed.png) angir at sjekken er mislykket. Se gjennom meldingen nedenfor sjekken for mer informasjon.
    - ![Tilkoblingskontrollen ble ikke kjørt.](media/connectivity-blocked.png) angir at kontrollen ikke ble kjørt, vanligvis på grunn av en tidligere kontroll. Se gjennom meldingen nedenfor sjekken for mer informasjon.

3. Velg **Start kontroll på nytt** for å kjøre kontrollen på nytt.

De følgende delene forklarer kontrollene som kjøres, og gir noen tips om hvordan du løser eventuelle problemer.

## <a name="basic-internet-connectivity"></a>Grunnleggende Internett-tilkobling

Kontrollerer at du har tilkobling til Internett ved å kontrollere at du får tilgang til et kjent offentlig domene, for eksempel www.bing.com.

|Problem|Ting å prøve|
|-------|-------------|
|Nettleseren støtter ikke denne kontrollen|Åpne siden i en støttet nettleser, og prøv på nytt. Hvis du vil se en liste over nettlesere som støttes, kan du se [Minimumskrav for bruk av Business Central – nettlesere](product-requirements.md#browsers)|
|Kan ikke pinge serveren på følgende URL-adresse: {url}|Kontroller brannmurinnstillingene.|

## <a name="cdn-content-delivery-network-resources-loading"></a>CDN-ressurser (Content Delivery Network) lastes inn

[!INCLUDE[prod_short](includes/prod_short.md)] bruker Azure Content Delivery Network (CDN) til å gi ressurser som kreves for å kjøre Business Central-nettklienten. Denne kontrollen kontrollerer at de nødvendige ressursene er tilgjengelige og tilgjengelige ved å pinge Business Central-forekomsten i CDN.

|Problem|Ting å prøve|
|-------|-------------|
|Nettleseren støtter ikke denne kontrollen|Se kontrollen **Grunnleggende Internett-tilkobling**.|
|Kan ikke pinge serveren på følgende URL-adresse: {url}|Kontroller brannmurinnstillingene.|

## <a name="user-authentication"></a>Brukergodkjenning

Kontrollerer at den gjeldende brukeren har logget på med en gyldig Business Central-konto.

|Problem|Ting å prøve|
|-------|-------------|
|Ingen bruker er godkjent|Logg på Business Central med gyldig brukernavn og passord.|

## <a name="business-central-environments-discovery"></a>Gjenkjenning av Business Central-miljøer

Ser etter Business Central-miljøer som er tilgjengelige for en godkjent bruker, og kontrollerer deretter om brukeren kan godkjennes i miljøet.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problem|Ting å prøve|
|-------|-------------|
|Ingen godkjent bruker å utføre denne kontrollen for|Se **Brukergodkjenning**-kontrollen.|
|Kan ikke hente tilgjengelige miljøer for kontoen.|Se i listen over tilgjengelige miljøer i administrasjonssenteret for Business Central.|
|Brukernavnet eller passordet er feil, eller du har ikke en gyldig konto.| Kontroller at du har logget på med riktig brukernavn og passord.|

## <a name="application-service-connectivity"></a>Tilkobling til programtjenesten

Kontroller at den godkjente brukeren kan koble til et miljø som oppdages, som vanligvis starter med produksjonsmiljøet.

|Problem|Ting å prøve|
|-------|-------------|
|Ingen godkjent bruker å utføre denne kontrollen for|Se **brukergodkjenningskontrollen**.|
|Kan ikke hente tilgjengelige miljøer for kontoen.|Se **Gjenkjenning av Business Central-miljøer**.|
|Ingen klyngeadresse å utføre denne kontrollen for|Se i listen over tilgjengelige miljøer i administrasjonssenteret for Business Central.|
|Versjonsendepunkt finnes ikke|Se i listen over tilgjengelige miljøer i administrasjonssenteret for Business Central.|

## <a name="see-also"></a>Se også

[Ressurser for hjelp og støtte](product-help-and-support.md)  
[Oversikt over oppgaver for å definere Business Central](setup.md)  
[Vanlige spørsmål om å bruke Business Central](across-faq.yml)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Administrasjonssenter for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
