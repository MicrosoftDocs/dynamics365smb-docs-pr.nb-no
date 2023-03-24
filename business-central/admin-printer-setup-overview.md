---
title: Oversikt over skriveroppsett og -behandling
description: Finn ut hva de forskjellige skrivermulighetene er i Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.date: 02/10/2023
ms.custom: bap-template
---

# Oversikt over skriveroppsett og -behandling

Utskrift av dokumenter og rapporter fra [!INCLUDE[prod_short](includes/prod_short.md)] er en viktig oppgave for forretningsbrukere. Du vil vanligvis sende utskriftsjobber direkte til en av skriverne i organisasjonen uansett hvilken [!INCLUDE[prod_short](includes/prod_short.md)]-klient eller -app du bruker. Ettersom [!INCLUDE[prod_short](includes/prod_short.md)] Online er en skytjeneste, kan den ikke kommunisere direkte med lokale skrivere som er koblet til brukernes enheter, men du kan koble til skyaktiverte skrivere.

## Hva er skrivermulighetene i Business Central?

[!INCLUDE[prod_short](includes/prod_short.md)] tilbyr følgende funksjoner for å støtte dine utskriftsbehov:

|Funksjon|Beskrivelse|Webklient| Mobilapp|App for Teams|
|-------|-----------|----------|-----------|--------------|
|Universell utskrift|Universell utskrift er en utskriftsbehandlingsløsning som er tilgjengelig som en skytjeneste fra Microsoft. Med denne funksjonen kan du konfigurere skriverne med Universell utskrift, og deretter registrere dem for bruk i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne funksjonen krever abonnement på Universell utskrift og utvidelsen **Integrering med Universell utskrift**.|![fungerer online.](media/check.png)|![fungerer online.](media/check.png)|![fungerer online](media/check.png)|
|E-postutskrift|Med denne funksjonen kan du konfigurere e-postbaserte skrivere. [!INCLUDE[prod_short](includes/prod_short.md)] sender deretter utskriftsjobber til en skriver ved å bruke e-postadressen til skriveren. Denne funksjonen krever e-postbaserte skrivere og filtypen **Send til e-post**.|![fungerer online.](media/check.png)|![fungerer online](media/check.png)|![fungerer online](media/check.png)|
|Utskrift fra nettleser|Utskriftsjobber håndteres av utskriftsfunksjonaliteten i brukerens nettleser. Hvis en skyskriver ikke er installert og konfigurert, eller hvis en installert skriver mislykkes, blir utskriftsalternativene automatisk angitt for leseren. Feltet **Skriver** på forespørselssiden vil vise *(Håndteres av nettleseren)*.|![fungerer online](media/check.png)|||

Det meste av arbeidet med å opprette skrivere kan gjøres fra siden **Utskriftsbehandling** i [!INCLUDE[prod_short](includes/prod_short.md)]. Selv om du har skrivere for Universell utskrift må du kanskje også arbeide i Microsoft 365-administrasjonssenteret eller på Azure Portal.

> [!IMPORTANT]
> For den lokale versjonen av Business Central kan du bruke universell utskrift og utskrift via e-post der godkjenning med Azure Active Directory (AD) eller NavUserPassword brukes.

## Egendefinerte skriverutvidelser

[!INCLUDE[prod_short](includes/prod_short.md)] støtter også andre egendefinerte skriverinnstillinger som legger til enda flere utskriftsfunksjoner. Hvis du har noen egendefinerte skrivere installert, kan det derfor hende at programmet inneholder utskriftsfunksjoner som ikke er beskrevet i denne artikkelen.

Hvis du er en AL-utvikler og vil finne ut hvordan du oppretter skriverutvidelser, kan du gå til [Utvikle skriverutvidelser i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-reports-printing).

## Neste trinn

- [Konfigurer skrivere for Universell utskrift](admin-printer-setup-universal-print.md)  
- [Konfigurer e-postskrivere](admin-printer-setup-email.md)  
- [Konfigurer standardskrivere](ui-specify-printer-selection-reports.md)