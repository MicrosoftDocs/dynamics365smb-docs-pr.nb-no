---
title: Konfigurere nettleseren
description: Beskriver hvordan du konfigurerer nettlesere for å arbeide med Business Central og produkter som integreres med det.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: 17b41653b1b5934e98c82ce8a35430e7b6a5c0d0
ms.sourcegitcommit: 1aac2c5f6773151c011dc1e4069c84d79fe5bda8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839958"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Konfigurere og feilsøke nettleseren for å arbeide med Business Central-nettklienten

Denne artikkelen forklarer hvordan du konfigurerer nettleseren slik at [!INCLUDE[web_client](includes/web_client.md)] og alle funksjonene fungerer som de skal. Les denne artikkelen hvis du har problemer med å åpne [!INCLUDE[web_client](includes/web_client.md)], fordi noen problemer kan være forårsaket av innstillingene i nettleseren.

Artikkelen inneholder detaljer om hvordan du konfigurerer Microsoft Edge, men kravene til JavaScript, informasjonskapsler og popup-vinduer er de samme for alle nettlesere som støttes. Se instruksjonene fra produsenten for andre nettlesere.  

## <a name="use-a-supported-browser"></a>Bruk en nettleser som støttes

Pass på at du bruker en av de støttede nettleserne. Se [Minimumskrav for å bruke Business Central](product-requirements.md#recommended-browsers).  

## <a name="allow-javascript-from-business-central"></a>Tillat JavaScript fra Business Central

*Problem:*

Hvis nettleseren ikke tillater JavaScript, ser du **NotSupported/DisabledJavaScript** på adresselinjen og meldingen **HTTP-feil 404.0 – ikke funnet** når du prøver å åpne [!INCLUDE[prod_short](includes/prod_short.md)] og 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Løsning:*

1. I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **JavaScript**.
2. Gjør ett av følgende: Velg det trinnet som organisasjonen anbefaler:

    - Flytt **Tillatte**-vekslebryteren mot venstre (Av). Deretter velger du **Legg til** og skriver inn adressen (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] i **Område**-boksen. Velg **Legg til** når du er ferdig.
    - Flytt **Tillatte**-vekslebryteren mot høyre (På).

## <a name="allow-cookies-from-business-central"></a>Tillat informasjonskapsler fra Business Central

*Problem:*

Hvis nettleseren ikke tillater informasjonskapsler, får du følgende feilmelding:

**Beklager, siden ble ikke funnet. Kontroller adressen og prøv på nytt.** 

*Løsning:*

1. I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **Informasjonskapsler og områdedata**.
2. Flytt **Tillat områder å lagre og lese informasjonskapseldata**-vekslebryteren mot høyre (På).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Tillat popup-vinduer fra Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] integreres med flere produkter. I noen tilfeller, for eksempel med Microsoft Teams, åpnes [!INCLUDE[prod_short](includes/prod_short.md)] eller popup-vinduer i produktet. Denne funksjonen krever at nettleseren tillater popup-vinduer fra [!INCLUDE[prod_short](includes/prod_short.md)].

*Problem:*

Hvis popup-vinduer for [!INCLUDE[prod_short](includes/prod_short.md)] blokkeres, får du en melding som ligner på følgende melding:

**Noe gikk galt. Det kan hende nettleseren blokkerer popup-vinduer som er nødvendig for Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Løsning:*

1. I Microsoft Edge går du til **Innstillinger** > **Informasjonskapsler og områdetillatelser** > **Popup-vinduer og omdirigeringer**.
2. Flytt **Blokkert**-vekslebryteren mot høyre (På).
3. Velg **Legg til**. I **Område**-boksen skriver du inn `https://businesscentral.dynamics.com` og velger **Legg til**.

## <a name="see-also"></a>Se også

[Feilsøke Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]